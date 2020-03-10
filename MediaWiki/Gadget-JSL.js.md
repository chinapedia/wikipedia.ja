> この記事は[MediaWiki:Gadget-JSL.js](https://ja.wikipedia.org/wiki/MediaWiki:Gadget-JSL.js)から翻訳されています。


// (C) Andrea Giammarchi - JSL 1.4b var undefined; function $JSL(){

`   this.inArray=function(){`
`       var tmp=false,i=arguments[1].length;`
`       while(i&&!tmp)tmp=arguments[1][--i]===arguments[0];`
`       return tmp;`
`   };`
`   this.has=function(str){return $JSL.inArray(str,$has)};`
`   this.random=function(elm){`
`       var tmp=$JSL.$random();`
`       while(typeof(elm[tmp])!=="undefined")tmp=$JSL.$random();`
`       return tmp;`
`   };`
`   this.$random=function(){return (Math.random()*1234567890).toString()};`
`   this.reverse=function(str){return str.split("").reverse().join("")};`
`   this.replace=function(str){`
`       var tmp=str.split(""),i=tmp.length;`
`       while(i>0)tmp[--i]=$JSL.$replace(tmp[i]);`
`       return tmp.join("");`
`   };`
`   this.$replace=function(tmp){`
`       var i=tmp.length===1?tmp.charCodeAt(0):0;`
`       switch(i) {`
`           case 8  :tmp="\\b";break;`
`           case 10 :tmp="\\n";break;`
`           case 11 :tmp="\\v";break;`
`           case 12 :tmp="\\f";break;`
`           case 13 :tmp="\\r";break;`
`           case 34 :tmp="\\\"";break;`
`           case 92 :tmp="\\\\";break;`
`           default:`
`               tmp=tmp.replace(/([\x00-\x07]|[\x0E-\x1F]|[\x7F-\xFF])/g,function(a,b){return "\\x"+$JSL.charCodeAt(b)}).`
`                   replace(/([\u0100-\uFFFF])/g,function(a,b){b=$JSL.charCodeAt(b);return b.length<4?"\\u0"+b:"\\u"+b});`
`               break;`
`       };`
`       return tmp;`
`   };`
`   this.charCodeAt=function(str){return $JSL.$charCodeAt(str.charCodeAt(0))};`
`   this.$charCodeAt=function(i){`
`       var str=i.toString(16).toUpperCase();`
`       return str.length<2?"0"+str:str;`
`   };`
`   this.$toSource=function(elm){return elm.toSource().replace(/^(`\(new \w+\()([^\000]+)(\)`\))$/,"$2")};`
`   this.$toInternalSource=function(elm){`
`       var tmp=null;`
`       switch(elm.constructor) {`
`           case Boolean:`
`           case Number:`
`               tmp=elm;`
`               break;`
`           case String:`
`               tmp=$JSL.$toSource(elm);`
`               break;`
`           default:`
`               tmp=elm.toSource();`
`               break;`
`       };`
`       return tmp;`
`   };`
`   this.getElementsByTagName=function(scope,i,elm,str){`
`       var tmp=$JSL.$getElementsByTagName(scope),j=tmp.length,$tmp=[];`
`       while(i<j){if(tmp[i][str]===elm||elm==="*")$tmp.push($JSL.$getElementsByName(tmp[i]));++i};`
`       if(!$tmp.item){if(!$JSL.has("item"))$has.push("item");$tmp.item=function(tmp){return this[tmp]}};`
`       return $tmp;`
`   };`
`   this.$getElementsByTagName=function(scope){return scope.layers||scope.all};`
`   this.$getElementsByName=function(elm) {`
`       if(!elm.getElementsByTagName)   elm.getElementsByTagName=document.getElementsByTagName;`
`       return elm;`
`   };`
`   this.encodeURI=function(str){return str.replace(/"/g,"%22").replace(/\\/g,"%5C")};`
`   this.$encodeURI=function(str){return $JSL.$charCodeAt(str)};`
`   this.$encodeURIComponent=function(a,b){`
`       var i=b.charCodeAt(0),str=[];`
`       if(i<128)       str.push(i);`
`       else if(i<2048)     str.push(0xC0+(i>>6),0x80+(i&0x3F));`
`       else if(i<65536)    str.push(0xE0+(i>>12),0x80+(i>>6&0x3F),0x80+(i&0x3F));`
`       else            str.push(0xF0+(i>>18),0x80+(i>>12&0x3F),0x80+(i>>6&0x3F),0x80+(i&0x3F));`
`       return "%"+str.map($JSL.$encodeURI).join("%");`
`   };`
`   this.$decodeURIComponent=function(a,b,c,d,e){`
`       var i=0;`
`       if(e)     i=parseInt(e.substr(1,2),16);`
`       else if(d)i=((parseInt(d.substr(1,2),16)-0xC0)<<6)+(parseInt(d.substr(4,2),16)-0x80);`
`       else if(c)i=((parseInt(c.substr(1,2),16)-0xE0)<<12)+((parseInt(c.substr(4,2),16)-0x80)<<6)+(parseInt(c.substr(7,2),16)-0x80);`
`       else      i=((parseInt(b.substr(1,2),16)-0xF0)<<18)+((parseInt(b.substr(4,2),16)-0x80)<<12)+((parseInt(b.substr(7,2),16)-0x80)<<6)+(parseInt(b.substr(10,2),16)-0x80);`
`       return String.fromCharCode(i);`
`   };`
`   var $has=[];`
`   if(!Function.prototype.apply){$has[$has.length]="apply";Function.prototype.apply=function(){`
`       var i=arguments.length===2?arguments[1].length:0,str,tmp=[],elm=(""+this).replace(/[^\(]+/,"function");`
`       if(!arguments[0])arguments[0]={};`
`       while(i)tmp.unshift("arguments[1]["+(--i)+"]");`
`       do{str="__".concat($JSL.random(arguments[0]).replace(/\./,"_"),"__")}while(new RegExp(str).test(elm));`
`       eval("var ".concat(str,"=arguments[0];tmp=(",elm.replace(/([^$])\bthis\b([^$])/g,"$1".concat(str,"$2")),")(",tmp.join(","),")"));`
`       return tmp;`
`   }};`
`   if(!Function.prototype.call){$has[$has.length]="call";Function.prototype.call=function(){`
`       var i=arguments.length,tmp=[];`
`       while(i>1)tmp.unshift(arguments[--i]);`
`       return this.apply((i?arguments[0]:{}),tmp);`
`   }};`
`   if(!Array.prototype.pop){$has[$has.length]="pop";Array.prototype.pop=function(){`
`       var a=this.length,r=this[--a];`
`       if(a>=0)this.length=a;`
`       return r;`
`   }};`
`   if(!Array.prototype.push){$has[$has.length]="push";Array.prototype.push=function(){`
`       var a=0,b=arguments.length,r=this.length;`
`       while(a<b)this[r++]=arguments[a++];`
`       return r;`
`   }};`
`   if(!Array.prototype.shift){$has[$has.length]="shift";Array.prototype.shift=function(){`
`       this.reverse();`
`       var r=this.pop();`
`       this.reverse();`
`       return r;`
`   }};`
`   if(!Array.prototype.splice){$has[$has.length]="splice";Array.prototype.splice=function(){`
`       var a,b,c,d=arguments.length,tmp=[],r=[];`
`       if(d>1){`
`           arguments[0]=parseInt(arguments[0]);`
`           arguments[1]=parseInt(arguments[1]);`
`           c=arguments[0]+arguments[1];`
`           for(a=0,b=this.length;a<b;a++){`
`               if(a<arguments[0]||a>=c){`
`                   if(a===c&&d>2){`
`                       for(a=2;a<d;a++)tmp.push(arguments[a]);`
`                       a=c;`
`                   };`
`                   tmp.push(this[a]);`
`               }`
`               else`
`                   r.push(this[a]);`
`           };`
`           for(a=0,b=tmp.length;a<b;a++)`
`               this[a]=tmp[a];`
`           this.length = a;`
`       };`
`       return r;`
`   }};`
`   if(!Array.prototype.unshift){$has[$has.length]="unshift";Array.prototype.unshift=function(){`
`       var i=arguments.length;`
`       this.reverse();`
`       while(i>0)this.push(arguments[--i]);`
`       this.reverse();`
`       return this.length;`
`   }};`
`   if(!Array.prototype.indexOf){$has[$has.length]="indexOf";Array.prototype.indexOf=function(elm,i){`
`       var j=this.length;`
`       if(!i)i=0;`
`       if(i>=0){while(i<j){if(this[i++]===elm){`
`           i=i-1+j;j=i-j;`
`       }}}`
`       else`
`           j=this.indexOf(elm,j+i);`
`       return j!==this.length?j:-1;`
`   }};`
`   if(!Array.prototype.lastIndexOf){$has[$has.length]="lastIndexOf";Array.prototype.lastIndexOf=function(elm,i){`
`       var j=-1;`
`       if(!i)i=this.length;`
`       if(i>=0){do{if(this[i--]===elm){`
`           j=i+1;i=0;`
`       }}while(i>0)}`
`       else if(i>-this.length)`
`           j=this.lastIndexOf(elm,this.length+i);`
`       return j;`
`   }};`
`   if(!Array.prototype.every){$has[$has.length]="every";Array.prototype.every=function(callback,elm){`
`       var b=false,i=0,j=this.length;`
`       if(!elm){   while(i<j&&!b)  b=!callback(this[i]||this.charAt(i),i++,this)}`
`       else {      while(i<j&&!b)  b=!callback.apply(elm,[this[i]||this.charAt(i),i++,this]);}`
`       return !b;`
`   }};`
`   if(!Array.prototype.filter){$has[$has.length]="filter";Array.prototype.filter=function(callback,elm){`
`       var r=[],i=0,j=this.length;`
`       if(!elm){while(i<j){if(callback(this[i],i++,this))`
`           r.push(this[i-1]);`
`       }} else {while(i<j){if(callback.apply(elm,[this[i],i++,this]))`
`           r.push(this[i-1]);`
`       }}`
`       return r;`
`   }};`
`   if(!Array.prototype.forEach){$has[$has.length]="forEach";Array.prototype.forEach=function(callback,elm){`
`       var i=0,j=this.length;`
`       if(!elm){   while(i<j)  callback(this[i],i++,this)}`
`       else {      while(i<j)  callback.apply(elm,[this[i],i++,this]);}`
`   }};`
`   if(!Array.prototype.map){$has[$has.length]="map";Array.prototype.map=function(callback,elm){`
`       var r=[],i=0,j=this.length;`
`       if(!elm){   while(i<j)  r.push(callback(this[i],i++,this))}`
`       else {      while(i<j)  r.push(callback.apply(elm,[this[i],i++,this]));}`
`       return r;`
`   }};`
`   if(!Array.prototype.some){$has[$has.length]="some";Array.prototype.some=function(callback,elm){`
`       var b=false,i=0,j=this.length;`
`       if(!elm){   while(i<j&&!b)  b=callback(this[i],i++,this)}`
`       else {      while(i<j&&!b)  b=callback.apply(elm,[this[i],i++,this]);}`
`       return b;`
`   }};`
`   if(!String.prototype.lastIndexOf){if(!this.inArray("lastIndexOf",$has))$has[$has.length]="lastIndexOf";String.prototype.lastIndexOf=function(elm,i){`
`       var str=$JSL.reverse(this),elm=$JSL.reverse(elm),r=str.indexOf(elm,i);`
`       return r<0?r:this.length-r;`
`   }};`
`   if("aa".replace(/\w/g,function(){return arguments[1]+" "})!=="0 1 "){$has[$has.length]="replace";String.prototype.replace=function(replace){return function(reg,func){`
`       var r="",tmp=$JSL.random(String);`
`       String.prototype[tmp]=replace;`
`       if(func.constructor!==Function)`
`           r=this[tmp](reg,func);`
`       else {`
`           function getMatches(reg,pos,a) {`
`               function io() {`
`                   var a=reg.indexOf("(",pos),b=a;`
`                   while(a>0&&reg.charAt(--a)==="\\"){};`
`                   pos=b!==-1?b+1:b;`
`                   return (b-a)%2===1?1:0;`
`               };`
`               do{a+=io()}while(pos!==-1);`
`               return a;`
`           };`
`           function $replace(str){`
`               var j=str.length-1;`
`               while(j>0)str[--j]='"'+str[j].substr(1,str[j--].length-2)[tmp](/(\\|")/g,'\\$1')+'"';`
`               return str.join("");`
`           };`
`           var p=-1,i=getMatches(""+reg,0,0),args=[],$match=this.match(reg),elm=$JSL.$random()[tmp](/\./,'_AG_');`
`           while(this.indexOf(elm)!==-1)elm=$JSL.$random()[tmp](/\./,'_AG_');`
`           while(i)args[--i]=[elm,'"$',(i+1),'"',elm].join("");`
`           if(!args.length)r="$match[i],(p=this.indexOf($match[i++],p+1)),this";`
`           else        r="$match[i],"+args.join(",")+",(p=this.indexOf($match[i++],p+1)),this";`
`           r=eval('['+$replace((elm+('"'+this[tmp](reg,'"'+elm+',func('+r+'),'+elm+'"')+'"')+elm).split(elm))[tmp](/\n/g,'\\n')[tmp](/\r/g,'\\r')+'].join("")');`
`       };`
`       delete String.prototype[tmp];`
`       return r;`
`   }}(String.prototype.replace)};`
`   if((new Date().getYear()).toString().length===4){$has[$has.length]="getYear";Date.prototype.getYear=function(){`
`       return this.getFullYear()-1900;`
`   }};`

};$JSL=new $JSL(); if(typeof(encodeURI)==="undefined"){function encodeURI(str){

`   var elm=/([\x00-\x20]|[\x25|\x3C|\x3E|\x5B|\x5D|\x5E|\x60|\x7F]|[\x7B-\x7D]|[\x80-\uFFFF])/g;`
`   return $JSL.encodeURI(str.toString().replace(elm,$JSL.$encodeURIComponent));`

}}; if(typeof(encodeURIComponent)==="undefined"){function encodeURIComponent(str){

`   var elm=/([\x23|\x24|\x26|\x2B|\x2C|\x2F|\x3A|\x3B|\x3D|\x3F|\x40])/g;`
`   return $JSL.encodeURI(encodeURI(str).replace(elm,function(a,b){return "%"+$JSL.charCodeAt(b)}));`

}}; if(typeof(decodeURIComponent)==="undefined"){function decodeURIComponent(str){

`   var elm=/(%F[0-9A-F]%E[0-9A-F]%[A-B][0-9A-F]%[8-9A-B][0-9A-F])|(%E[0-9A-F]%[A-B][0-9A-F]%[8-9A-B][0-9A-F])|(%[C-D][0-9A-F]%[8-9A-B][0-9A-F])|(%[0-9A-F]{2})/g;`
`   return str.toString().replace(elm,$JSL.$decodeURIComponent);`

}}; if(typeof(decodeURI)==="undefined"){function decodeURI(str){

`   return decodeURIComponent(str);`

}}; if(\!document.getElementById){document.getElementById=function(elm){

`   return $JSL.$getElementsByName($JSL.$getElementsByTagName(this)[elm]);`

}}; if(\!document.getElementsByTagName){document.getElementsByTagName=function(elm){

`   return $JSL.getElementsByTagName(this,0,elm.toUpperCase(),"tagName");`

}}; if(\!document.getElementsByName){document.getElementsByName=function(elm){

`   return $JSL.getElementsByTagName(this,0,elm,"name");`

}}; if(typeof(XMLHttpRequest)==="undefined"){XMLHttpRequest=function(){

`   var tmp=null,elm=navigator.userAgent;`
`   if(elm.toUpperCase().indexOf("MSIE 4")<0&&window.ActiveXObject)`
`       tmp=elm.indexOf("MSIE 5")<0?new ActiveXObject("Msxml2.XMLHTTP"):new ActiveXObject("Microsoft.XMLHTTP");`
`   return tmp;`

}}; if(typeof(Error)==="undefined")Error=function(){}; Error = function(base){return function(message){

`   var tmp=new base();`
`   tmp.message=message||"";`
`   if(!tmp.fileName)`
`       tmp.fileName=document.location.href;`
`   if(!tmp.lineNumber)`
`       tmp.lineNumber=0;`
`   if(!tmp.stack)`
`       tmp.stack="Error()@:0\n(\""+this.message+"\")@"+tmp.fileName+":"+this.lineNumber+"\n@"+tmp.fileName+":"+this.lineNumber;`
`   if(!tmp.name)`
`       tmp.name="Error";`
`   return tmp;`

}}(Error);