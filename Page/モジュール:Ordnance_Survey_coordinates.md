> この記事は[モジュール:Ordnance Survey coordinates](https://ja.wikipedia.org/wiki/モジュール:Ordnance_Survey_coordinates)から翻訳されています。


\-- Lat Long functions in Lua

\-- Ported to Lua from PHP by Wikipedia User Hike395, 18 Aug 2019

\-- found by RWH at <http://www.megalithia.com/search/llfuncshighlight.php>

\-- With thanks to Andy, G4JNT for inspiration in GEOG, and to the OSGB for their white paper on coordinate transformation -- describing the iterative method used -- thanks to the Ordnance survey of Ireland for details of the true and false origins of the Irish grid

\-- You may use and redistribute this code under the terms of the GPL see <http://www.gnu.org/copyleft/gpl.html>

\-- Written by Richard -- www.megalithia.com -- v0.something 27/2/2000 -- v 1.01 28 June 2004 -- v 1.02 6 Aug 2004 line 89 add "0" to chars in ngr=stripcharsnotinbag Thx Andy -- v 1.03 9 Mar 2005 Jan (Klingon) added conversion to WGS84 map datum and removed limitation of digits of the grid ref -- v 1.04 10 Aug 2005 Richard correct error trapping (only manifest on malformed ngrs

\-- This code is predicated on the assumption that your are ONLY feeding it Irish or UK Grid references. -- It uses the single char prefix of Irish grid refs to tell the difference, UK grid refs have a two letter prefix. -- We would like an even number of digits for the rest of the grid ref. -- Anything in the NGR other than 0-9, A-Z, a-z is eliminated. -- WARNING this assumes there are no decimal points in your NGR components.

\-- The transformation from OSGB36/Ireland 1965 to WGS84 is more precise than 5 m.

\-- The function is case insensitive

local oscoord = {} local getArgs = require('Module:Arguments').getArgs local namespace = mw.title.getCurrentTitle().namespace;

local function northeast(lett,num,shift)

`  -- split into northings and eastings`
`  local le=string.len(num)`
`  if le%2 == 1 then`
`    return "Malformed numerical part of NGR"`
`  end`
`  local pr=le/2`
`  local n = string.sub(num,pr+1)`
`  local e = string.sub(num,1,pr)`
`  -- Hack to move to center of square: append a 5 to northings and eastings`
`  if shift ~= nil and shift > 0 then`
`    n = n.."5"`
`    e = e.."5"`
`    pr = pr+1`
`  end`
`  -- end hack`
`  if string.len(n) == 0 then`
`    n = 0`
`  end`
`  if string.len(e) == 0 then`
`    e = 0`
`  end`
`  pr = math.pow(10.0,(5.0-pr))`
`  local T1 = string.byte(string.sub(lett,1,1))-65`
`  if T1>8 then`
`    T1 = T1-1`
`  end`
`  local T2 = nil`
`  if string.len(lett)>1 then`
`    T2 = string.byte(string.sub(lett,2))-65`
`    if T2>8 then`
`      T2 = T2-1`
`    end`
`  end`
`  return nil,n,e,pr,T1,T2`

end

local function GBEN2LL(e,n)

`  local pow,sqrt,abs=math.pow,math.sqrt,math.abs`
`  local sin,cos,tan,atan=math.sin,math.cos,math.tan,math.atan`
`  local dr = math.deg(1.0)`
`  -- True Origin is 2 deg W`
`  local phi0uk=-2.0`
`  -- True Origin is 49 deg N`
`  local lambda0uk=49.0`
`  -- scale factor @ central meridian`
`  local F0uk=0.9996012717`
`  -- True origin in 400 km E of false origin`
`  local E0uk=400000.0`
`  --True origin is 100 km S of false origin`
`  local N0uk=-100000.0`
`  -- semi-major axis (in line to equator) 0.996012717 is yer scale @ central meridian`
`  local auk=6377563.396*F0uk`
`  --semi-minor axis (in line to poles)`
`  local buk=6356256.91*F0uk`
`  -- flatness=a1-b1/(a1+b1)`
`  local n1uk=0.00167322025032508731869331280635710896296`
`  -- first eccentricity squared=2*f-f^2where f=(a1-b1)/a1`
`  local e2uk=0.006670539761597529073698869358812557054558`
`  local k=(n-N0uk)/auk+lambda0uk/dr`
`  local nextcounter=0`
`  local j3, j4, j5, j6, m`
`  repeat`
`    nextcounter=nextcounter+1`
`    local k3=k-lambda0uk/dr`
`    local k4=k+lambda0uk/dr`
`    j3=(1.0+n1uk+1.25*pow(n1uk,2.0)+1.25*pow(n1uk,3.0))*k3`
`    j4=(3.0*n1uk+3.0*pow(n1uk,2.0)+2.625*pow(n1uk,3.0))*sin(k3)*cos(k4)`
`    j5=(1.875*pow(n1uk,2.0)+1.875*pow(n1uk,3.0))*sin(2.0*k3)*cos(2.0*k4)`
`    j6=35.0/24.0*pow(n1uk,3.0)*sin(3.0*k3)*cos(3.0*k4)`
`    m=buk*(j3-j4+j5-j6)`
`    k=k+(n-N0uk-m)/auk`
`  until abs(n-N0uk-m)<=0.000000001 or nextcounter>=100`
`  local v=auk/sqrt(1.0-e2uk*pow(sin(k),2.0))`
`  local r=v*(1.0-e2uk)/(1.0-e2uk*pow(sin(k),2.0))`
`  local h2=v/r-1.0`
`  local y1=e-E0uk`
`  j3=tan(k)/(2.0*r*v)`
`  j4=tan(k)/(24.0*r*pow(v,3.0))*(5.0+3.0*pow(tan(k),2.0)+h2-9.0*pow(tan(k),2.0)*h2)`
`  j5=tan(k)/(720.0*r*pow(v,5.0))*(61.0+90.0*pow(tan(k),2.0)+45.0*pow(tan(k),4.0))`
`  local k9=k-y1*y1*j3+pow(y1,4.0)*j4-pow(y1,6.0)*j5`
`  j6=1.0/(cos(k)*v)`
`  local j7=1.0/(cos(k)*6.0*pow(v,3.0))*(v/r+2.0*pow(tan(k),2.0))`
`  local j8=1.0/(cos(k)*120.0*pow(v,5.0))*(5.0+28.0*pow(tan(k),2.0)+24.0*pow(tan(k),4.0))`
`  local j9=1.0/(cos(k)*5040.0*pow(v,7.0))`
`  local j9=j9*(61.0+662.0*pow(tan(k),2.0)+1320.0*pow(tan(k),4.0)+720.0*pow(tan(k),6.0))`
`  local long=phi0uk+dr*(y1*j6-y1*y1*y1*j7+pow(y1,5.0)*j8-pow(y1,7.0)*j9)`
`  local lat=k9*dr`
`  local v=6377563.396/sqrt(1.0-e2uk*pow(sin(k),2.0))`
`  local cartxa=v*cos(k9)*cos(long/dr)`
`  local cartya=v*cos(k9)*sin(long/dr)`
`  local cartza=(1.0-e2uk)*v*sin(k9)`
`  -- Helmert-Transformation from OSGB36 to WGS84 map date`
`  local rotx=-0.1502/3600.0/dr`
`  local roty=-0.2470/3600.0/dr`
`  local rotz=-0.8421/3600.0/dr`
`  local scale=-20.4894/1000000.0`
`  local cartxb=446.448+(1.0+scale)*cartxa+rotz*cartya-roty*cartza`
`  local cartyb=-125.157-rotz*cartxa+(1.0+scale)*cartya+rotx*cartza`
`  local cartzb=542.06+roty*cartxa-rotx*cartya+(1.0+scale)*cartza`
`  -- convert Cartesian to long/lat`
`  local awgs84=6378137.0`
`  local bwgs84=6356752.3141`
`  local e2wgs84=0.00669438003551279089034150031998869922791`
`  local lambdaradwgs84=atan(cartyb/cartxb)`
`  long=lambdaradwgs84*dr`
`  local pxy=sqrt(pow(cartxb,2.0)+pow(cartyb,2.0))`
`  local phiradwgs84`
`  local phinewwgs84=atan(cartzb/pxy/(1.0-e2wgs84))`
`  nextcounter=0`
`  repeat`
`    phiradwgs84=phinewwgs84`
`    nextcounter=nextcounter+1`
`    v=awgs84/sqrt(1.0-e2wgs84*pow(sin(phiradwgs84),2.0))`
`    phinewwgs84=atan((cartzb+e2wgs84*v*sin(phiradwgs84))/pxy)`
`  until abs(phinewwgs84-phiradwgs84)<=0.000000000001 or nextcounter>=100`
`  lat=phinewwgs84*dr`
`  return "GB",nil,lat,long`

end

local function GB2LL(lett,num)

`  -- British OS to Lat+Long`
`  -- first caclulate e,n`
`  -- computing e and n exactly, to get SW corner of box`
`  local err, n, e, pr, T1, T2 = northeast(lett,num,0)`
`  if err ~= nil then`
`    return "GB",err,0.0,0.0`
`  end`
`  -- use British definition of e and n`
`  e=500000.0*(T1%5)+100000.0*(T2%5)-1000000.0+e*pr`
`  n=1900000.0-500000.0*math.floor(T1/5)-100000.0*math.floor(T2/5)+n*pr`
`  return GBEN2LL(e,n)`

end

local function IrishEN2LL(e,n)

`  local pow,sqrt,abs=math.pow,math.sqrt,math.abs`
`  local sin,cos,tan,atan=math.sin,math.cos,math.tan,math.atan`
`  local dr=math.deg(1.0)`
`  -- True Origin is 8 deg W`
`  local phi0ir=-8.0`
`  -- True Origin is 53.5 deg N`
`  local lambda0ir=53.5`
`  -- scale factor @ central meridian`
`  local F0ir=1.000035`
`  -- True origin in 200 km E of false origin`
`  local E0ir=200000.0`
`  --True origin is 250km N of false origin`
`  local N0ir=250000.0`
`  -- semi-major axis (in line to equator) 1.000035 is yer scale @ central meridian`
`  local air=6377340.189*F0ir`
`  --semi-minor axis (in line to poles)`
`  local bir=6356034.447*F0ir`
`  -- flatness=a1-b1/(a1 + b1)`
`  local n1ir=0.001673220384152058651484728058385228837777`
`  -- first eccentricity squared=2*f-f^2 where f=(a1-b1)/a1`
`  local e2ir=0.006670540293336110419293763349975612794125`
`  local k=(n-N0ir)/air+lambda0ir/dr`
`  local nextcounter=0`
`  local j3,j4,j5,j6,m`
`  repeat`
`    nextcounter=nextcounter+1`
`    local k3=k-lambda0ir/dr`
`    local k4=k+lambda0ir/dr`
`    j3=(1.0+n1ir+1.25*pow(n1ir,2.0)+1.25*pow(n1ir,3.0))*k3`
`    j4=(3.0*n1ir+3.0*pow(n1ir,2.0)+2.625*pow(n1ir,3.0))*sin(k3)*cos(k4)`
`    j5=(1.875*pow(n1ir,2.0)+1.875*pow(n1ir,3.0))*sin(2.0*k3)*cos(2.0*k4)`
`    j6=35.0/24.0*pow(n1ir,3.0)*sin(3.0*k3)*cos(3.0*k4)`
`    m=bir*(j3-j4+j5-j6)`
`    k=k+(n-N0ir-m)/air`
`  until abs(n-N0ir-m)<=0.000000000001 or nextcounter>=10000`
`  local v=air/sqrt(1.0-e2ir*pow(sin(k),2.0))`
`  local r=v*(1.0-e2ir)/(1.0-e2ir*pow(sin(k),2.0))`
`  local h2=v/r-1.0`
`  local y1=e-E0ir`
`  j3=tan(k)/(2.0*r*v)`
`  j4=tan(k)/(24.0*r*pow(v,3.0))*(5.0+3.0*pow(tan(k),2.0)+h2-9.0*pow(tan(k),2.0)*h2)`
`  j5=tan(k)/(720.0*r*pow(v,5.0))*(61.0+90.0*pow(tan(k),2.0)+45.0*pow(tan(k),4.0))`
`  local k9=k-y1*y1*j3+pow(y1,4.0)*j4-pow(y1,6.0)*j5`
`  j6=1.0/(cos(k)*v)`
`  local j7=1.0/(cos(k)*6.0*pow(v,3.0))*(v/r+2.0*pow(tan(k),2.0))`
`  local j8=1.0/(cos(k)*120.0*pow(v,5.0))*(5.0+28.0*pow(tan(k),2.0)+24.0*pow(tan(k),4.0))`
`  local j9=1.0/(cos(k)*5040.0*pow(v,7.0))`
`  local j9=j9*(61.0+662.0*pow(tan(k),2.0)+1320.0*pow(tan(k),4.0)+720.0*pow(tan(k),6.0))`
`  local long=phi0ir+dr*(y1*j6-y1*y1*y1*j7+pow(y1,5.0)*j8-pow(y1,7.0)*j9)`
`  local lat=k9*dr`
`  -- convert long/lat to Cartesian coordinates`
`  v=6377340.189/sqrt(1.0-e2ir*pow(sin(k),2.0))`
`  local cartxa=v*cos(k9)*cos(long/dr)`
`  local cartya=v*cos(k9)*sin(long/dr)`
`  local cartza=(1.0-e2ir)*v*sin(k9)`
`  -- Helmert-Transformation from Ireland 1965 to WGS84 map date`
`  local rotx=1.042/3600.0/dr`
`  local roty=0.214/3600.0/dr`
`  local rotz=0.631/3600.0/dr`
`  local scale=8.15/1000000.0`
`  local cartxb=482.53+(1.0+scale)*cartxa+rotz*cartya-roty*cartza`
`  local cartyb=-130.596-rotz*cartxa+(1.0+scale)*cartya+rotx*cartza`
`  local cartzb=564.557+roty*cartxa-rotx*cartya+(1.0+scale)*cartza`
`  -- convert Cartesian to long/lat`
`  local awgs84=6378137.0`
`  local bwgs84=6356752.3141`
`  local e2wgs84=0.00669438003551279089034150031998869922791`
`  local lambdaradwgs84=atan(cartyb/cartxb)`
`  long=lambdaradwgs84*dr`
`  local pxy=sqrt(pow(cartxb,2.0)+pow(cartyb,2.0))`
`  local phinewwgs84=atan(cartzb/pxy/(1.0-e2wgs84))`
`  local phiradwgs84`
`  nextcounter=0`
`  repeat`
`    phiradwgs84=phinewwgs84`
`    nextcounter=nextcounter+1`
`    v=awgs84/sqrt(1.0-e2wgs84*pow(sin(phiradwgs84),2.0))`
`    phinewwgs84=atan((cartzb+e2wgs84*v*sin(phiradwgs84))/pxy)`
`  until abs(phinewwgs84-phiradwgs84)<=0.000000000001 or nextcounter>=10000`
`  lat=phinewwgs84*dr`
`  return "IE",nil,lat,long`

end

local function Irish2LL(lett,num)

`  -- Irish OS to Lat+Long`
`  -- first caclulate e,n`
`  -- computing e and n exactly, to get SW corner of box`
`  local err, n, e, pr, T1 = northeast(lett,num,0)`
`  if err ~= nil then`
`    return "IE",err,0.0,0.0`
`  end`
`  -- use Irish definition of northing and easting`
`  local e=100000.0*(T1%5.0)+e*pr`
`  local n=n*pr+100000.0*(4.0-math.floor(T1/5.0))`
`  return IrishEN2LL(e,n)`

end

local function NGR2LL(ngr) -- returns a country,error,lat,long list

` ngr = string.gsub(string.upper(ngr),"[^%d%u]","")`
` local lett = string.gsub(ngr,"[^%u]","")`
` local num = string.gsub(ngr,"[^%d]","")`
` if string.len(lett) == 1 then`
`   return Irish2LL(lett,num)`
` end`
` if string.len(lett) == 2 then`
`   return GB2LL(lett,num)`
` end`
` return nil,"Malformed NGR",0.0,0.0`

end

local function split(s,sep) -- split a string s into chunks, separated by sep

` if sep == nil then`
`    sep = "%s"`
` end`
` local t = {}`
` for chunk in string.gmatch(s,"([^"..sep.."]+)") do`
`   table.insert(t,chunk)`
` end`
` return t`

end

local function trim(s)

` s = string.gsub(s,"^%s+","")`
` s = string.gsub(s,"%s+$","")`
` return s`

end

local function alldigits(s)

` return string.find(s,"%D") == nil`

end

local function warning(errmsg)

` local frame = mw.getCurrentFrame():getParent()`
` local html = ""`
` local msg = errmsg`
` if errmsg == nil then`
`   msg = "Empty OS grid ref"`
` end`
` if frame:preprocess( "``" ) == "" then `
`   html = '`

<div style="color:red">

<strong>Warning:</strong> '..msg

`   html = html..' `<small>`(this message is shown only in preview)`</small>

</div>

'

` end`
` if namespace == 0 and errmsg ~= nil then`
`   html = html..''`
` end`
` return html`

end

function oscoord.main(frame)

` local args = getArgs(frame,{parentFirst=true,parentOnly=false,frameOnly=false})`
` local input = args[1]`
` if input == nil or string.len(input)==0 then`
`   return warning(nil)`
` end`
` local linktitle = args[2]`
` local args = split(input,'_')`
` local LL`
` local restargs = 1`
` local current_page = mw.title.getCurrentTitle()`
` local pagename = mw.uri.encode( current_page.prefixedText, 'WIKI' );`
` if #args >= 2 and alldigits(args[2]) then`
`   if string.sub(args[1],1,1) == 'i' then`
`     local firstArg = string.sub(args[1],2)`
`     if alldigits(firstArg) then`
`       LL = {IrishEN2LL(firstArg,args[2])}`
`       restargs = 3`
`       if linktitle == nil or string.len(linktitle) == 0 then`
`         linktitle=args[1]..'_'..args[2]`
`       end`
`     end`
`   elseif alldigits(args[1]) then`
`     LL = {GBEN2LL(args[1],args[2])}`
`     restargs = 3`
`     if linktitle == nil or string.len(linktitle) == 0 then`
`       linktitle=args[1]..'_'..args[2]`
`     end`
`   end`
` else`
`   LL = {NGR2LL(args[1])}`
`   restargs = 2`
`   if linktitle == nil or string.len(linktitle) == 0 then`
`     linktitle=args[1]`
`   end`
` end`
` linktitle = trim(linktitle)`
` if LL[2] ~= nil then`
`   local html = linktitle`
`   html = html..warning(LL[2])`
`   return html`
` end`
` local url = '[`<https://tools.wmflabs.org/geohack/ja/>`'..LL[3]..';'..LL[4]`
` for i = restargs,#args do`
`   url = url..'_'..args[i]`
` end`
` if string.find(input,"region") == nil then`
`   url = url..'_region:'..LL[1]`
` end`
` if pagename ~= nil then`
`   url = url..'?pagename='..pagename`
` end`
` url = url..' '..linktitle..']'`
` return url`

end

return oscoord

[Category:Pages_with_malformed_OS_coordinates](https://ja.wikipedia.org/wiki/Category:Pages_with_malformed_OS_coordinates "wikilink")