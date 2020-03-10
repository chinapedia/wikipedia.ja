> この記事は[ID3](https://ja.wikipedia.org/wiki/ID3)から翻訳されています。


**ID3タグ**（アイディースリータグ、*ID3 tag*）は、[MP3](../Page/MP3.md "wikilink")[ファイルの中に](../Page/音声ファイルフォーマット.md "wikilink")、アーティスト・作成年・曲名等の情報を書き込むための規格である。

## 概要

ID3タグはMP3ファイルに元々組み込まれていた仕様ではなく、1996年に公開された「Studio3」という[ソフトウェア](../Page/ソフトウェア.md "wikilink")に組み込まれたのが始まりである。以後、様々なバージョンの規格が作られた。

ID3を追加したり、書き換えたりするソフトウェアはいくつか存在する。代表的な物は[Winamp](https://ja.wikipedia.org/wiki/Winamp "wikilink")、SuperTagEditorシリーズ、[mp3infp](http://win32lab.com/)、[Mp3tag](https://ja.wikipedia.org/wiki/Mp3tag "wikilink")等。

## バージョン

ID3はいくつかのバージョンが存在する。このうち、ID3v1はファイルの末尾に、ID3v2はファイルの先頭に書かれるため、同時に1つのファイルに含めることができる。

### ID3v1

もっとも広く対応されている形式。サイズは128バイト固定で制限が厳しいため、多くの情報は記録できない。 文字列には日本語を使用することができるが、文字コードに関する定義がないため、プラットフォームをまたぐ際に互換性の面で問題が生じることがある。

| 開始位置 | 長さ | 説明 |- align="center"| | 0 | 3 | “TAG” の識別子3文字 |- align="center"| | 3 | 30 | 曲名文字列。 |- align="center"| | 33 | 30 | アーティスト文字列。 |- align="center"| | 63 | 30 | アルバム文字列。 |- align="center"| | 93 | 4 | 日付文字列。 |- align="center"| | 97 | 30 | コメント文字列。 |- align="center"| | 127 | 1 | ジャンル番号。 |
| ---- | -- | --------------------- | - | - | -------------------------------- | - | -- | ------------------------- | -- | -- | ----------------------------- | -- | -- | --------------------------- | -- | - | ------------------------- | -- | -- | --------------------------- | --- | - | ------- |

ID3v1 形式

### ID3v1.1

v1 のコメントを 2 バイト短縮し、トラック番号を記録できるようにした形式。 短縮した 2 バイトのうち、先の 1 バイトには必ず 0 (NULL) を格納し\[1\]、残りの 1 バイトにトラック番号を記録する。 仕様上、v1 形式で 29 バイト以上のコメントが入力されたファイルとの互換は完全には保てず、 トラック番号を記録して v1.1 形式に移行した時点でコメントの 29 、30 バイト目のデータが消失する。

| 開始位置 | 長さ | 説明 |- align="center"| | 0 | 3 | “TAG” の識別子3文字 |- align="center"| | 3 | 30 | 曲名文字列。 |- align="center"| | 33 | 30 | アーティスト文字列。 |- align="center"| | 63 | 30 | アルバム文字列。 |- align="center"| | 93 | 4 | 日付文字列。 |- align="center"| | 97 | 28 | コメント文字列。 |- align="center"| | 125 | 1 | 0 (NULL) が格納される\[2\]。 |- align="center"| | 126 | 1 | トラック番号。 |- align="center"| | 127 | 1 | ジャンル番号。 |
| ---- | -- | --------------------- | - | - | -------------------------------- | - | -- | ------------------------- | -- | -- | ----------------------------- | -- | -- | --------------------------- | -- | - | ------------------------- | -- | -- | --------------------------- | --- | - | ---------------------------------------- | --- | - | -------------------------- | --- | - | ------- |

ID3v1.1 形式

#### ジャンル番号一覧

<table>
<thead>
<tr class="header">
<th><p>’型 ID #</p></th>
<th><p>型</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0</p></td>
<td><p><a href="../Page/ブルース.md" title="wikilink">Blues</a></p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
<td><p><a href="../Page/クラシック・ロック.md" title="wikilink">Classic Rock</a></p></td>
</tr>
<tr class="odd">
<td><p>2</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/カントリー・ミュージック" title="wikilink">Country</a></p></td>
</tr>
<tr class="even">
<td><p>3</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ダンス・ミュージック" title="wikilink">Dance</a></p></td>
</tr>
<tr class="odd">
<td><p>4</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ディスコ_(音楽)" title="wikilink">Disco</a></p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p><a href="../Page/ファンク.md" title="wikilink">Funk</a></p></td>
</tr>
<tr class="odd">
<td><p>6</p></td>
<td><p><a href="../Page/グランジ.md" title="wikilink">Grunge</a></p></td>
</tr>
<tr class="even">
<td><p>7</p></td>
<td><p><a href="../Page/ヒップホップ.md" title="wikilink">Hip-Hop</a></p></td>
</tr>
<tr class="odd">
<td><p>8</p></td>
<td><p><a href="../Page/ジャズ.md" title="wikilink">Jazz</a></p></td>
</tr>
<tr class="even">
<td><p>9</p></td>
<td><p><a href="../Page/ヘヴィメタル.md" title="wikilink">Metal</a></p></td>
</tr>
<tr class="odd">
<td><p>10</p></td>
<td><p><a href="../Page/ニューエイジ・ミュージック.md" title="wikilink">New Age</a></p></td>
</tr>
<tr class="even">
<td><p>11</p></td>
<td><p><a href="../Page/オールディーズ.md" title="wikilink">Oldies</a></p></td>
</tr>
<tr class="odd">
<td><p>12</p></td>
<td><p>Other（その他）</p></td>
</tr>
<tr class="even">
<td><p>13</p></td>
<td><p><a href="../Page/ポップ・ミュージック.md" title="wikilink">Pop</a></p></td>
</tr>
<tr class="odd">
<td><p>14</p></td>
<td><p><a href="../Page/リズム・アンド・ブルース.md" title="wikilink">R&amp;B</a></p></td>
</tr>
<tr class="even">
<td><p>15</p></td>
<td><p><a href="../Page/ラップ.md" title="wikilink">Rap</a></p></td>
</tr>
<tr class="odd">
<td><p>16</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/レゲエ" title="wikilink">Reggae</a></p></td>
</tr>
<tr class="even">
<td><p>17</p></td>
<td><p><a href="../Page/ロック_(音楽).md" title="wikilink">Rock</a></p></td>
</tr>
<tr class="odd">
<td><p>18</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/テクノ_(ダンスミュージック)" title="wikilink">Techno</a></p></td>
</tr>
<tr class="even">
<td><p>19</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/インダストリアル" title="wikilink">Industrial</a></p></td>
</tr>
<tr class="odd">
<td><p>20</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/オルタナティヴ・ミュージック" title="wikilink">Alternative</a></p></td>
</tr>
<tr class="even">
<td><p>21</p></td>
<td><p><a href="../Page/スカ.md" title="wikilink">Ska</a></p></td>
</tr>
<tr class="odd">
<td><p>22</p></td>
<td><p><a href="../Page/デスメタル.md" title="wikilink">Death Metal</a></p></td>
</tr>
<tr class="even">
<td><p>23</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>24</p></td>
<td><p><a href="../Page/サウンドトラック.md" title="wikilink">Soundtrack</a></p></td>
</tr>
<tr class="even">
<td><p>25</p></td>
<td><p>Euro-<a href="https://ja.wikipedia.org/wiki/テクノ_(ダンスミュージック)" title="wikilink">Techno</a></p></td>
</tr>
<tr class="odd">
<td><p>26</p></td>
<td><p><a href="../Page/環境音楽.md" title="wikilink">Ambient</a></p></td>
</tr>
<tr class="even">
<td><p>27</p></td>
<td><p><a href="../Page/トリップ・ホップ.md" title="wikilink">Trip-Hop</a></p></td>
</tr>
<tr class="odd">
<td><p>28</p></td>
<td><p><a href="../Page/声楽.md" title="wikilink">Vocal</a></p></td>
</tr>
<tr class="even">
<td><p>29</p></td>
<td><p><a href="../Page/ジャズ・ファンク.md" title="wikilink">Jazz-funk</a></p></td>
</tr>
<tr class="odd">
<td><p>30</p></td>
<td><p><a href="../Page/フュージョン_(音楽).md" title="wikilink">Fusion</a></p></td>
</tr>
<tr class="even">
<td><p>31</p></td>
<td><p><a href="../Page/トランス_(音楽).md" title="wikilink">Trance</a></p></td>
</tr>
<tr class="odd">
<td><p>32</p></td>
<td><p><a href="../Page/クラシック音楽.md" title="wikilink">Classical</a></p></td>
</tr>
<tr class="even">
<td><p>33</p></td>
<td><p><a href="../Page/器楽曲.md" title="wikilink">Instrumental</a></p></td>
</tr>
<tr class="odd">
<td><p>34</p></td>
<td><p><a href="../Page/アシッド・ハウス.md" title="wikilink">Acid</a></p></td>
</tr>
<tr class="even">
<td><p>35</p></td>
<td><p><a href="../Page/ハウス_(音楽).md" title="wikilink">House</a></p></td>
</tr>
<tr class="odd">
<td><p>36</p></td>
<td><p><a href="../Page/ゲームミュージック.md" title="wikilink">Game</a></p></td>
</tr>
<tr class="even">
<td><p>37</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>38</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ゴスペル_(音楽)" title="wikilink">Gospel</a></p></td>
</tr>
<tr class="even">
<td><p>39</p></td>
<td><p><a href="../Page/ノイズミュージック.md" title="wikilink">Noise</a></p></td>
</tr>
<tr class="odd">
<td><p>40</p></td>
<td><p><a href="../Page/オルタナティヴ・ロック.md" title="wikilink">Alt. Rock</a></p></td>
</tr>
<tr class="even">
<td><p>41</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ベース・ミュージック" title="wikilink">Bass</a></p></td>
</tr>
<tr class="odd">
<td><p>42</p></td>
<td><p><a href="../Page/ソウルミュージック.md" title="wikilink">Soul</a></p></td>
</tr>
<tr class="even">
<td><p>43</p></td>
<td><p><a href="../Page/パンク・ロック.md" title="wikilink">Punk</a></p></td>
</tr>
<tr class="odd">
<td><p>44</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>45</p></td>
<td><p><a href="../Page/瞑想.md" title="wikilink">Meditative</a></p></td>
</tr>
<tr class="odd">
<td><p>46</p></td>
<td><p>Instrumental pop</p></td>
</tr>
<tr class="even">
<td><p>47</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>48</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/民俗音楽" title="wikilink">Ethnic</a></p></td>
</tr>
<tr class="even">
<td><p>49</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ゴシック・ロック" title="wikilink">Gothic</a></p></td>
</tr>
<tr class="odd">
<td><p>50</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>51</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ハードコア・テクノ" title="wikilink">Techno-Industrial</a></p></td>
</tr>
<tr class="odd">
<td><p>52</p></td>
<td><p><a href="../Page/電子音楽.md" title="wikilink">Electronic</a></p></td>
</tr>
<tr class="even">
<td><p>53</p></td>
<td><p><a href="../Page/ポップ・フォーク.md" title="wikilink">Pop-folk</a></p></td>
</tr>
<tr class="odd">
<td><p>54</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ユーロ・ダンス" title="wikilink">Eurodance</a></p></td>
</tr>
<tr class="even">
<td><p>55</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ドリーム・ポップ" title="wikilink">Dream</a></p></td>
</tr>
<tr class="odd">
<td><p>56</p></td>
<td><p><a href="../Page/サザン・ロック.md" title="wikilink">Southern Rock</a></p></td>
</tr>
<tr class="even">
<td><p>57</p></td>
<td><p><a href="../Page/喜劇.md" title="wikilink">Comedy</a></p></td>
</tr>
<tr class="odd">
<td><p>58</p></td>
<td><p><a href="../Page/カルト.md" title="wikilink">Cult</a></p></td>
</tr>
<tr class="even">
<td><p>59</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ギャングスタ・ラップ" title="wikilink">Gangsta</a></p></td>
</tr>
<tr class="odd">
<td><p>60</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/トップ40" title="wikilink">Top 40</a></p></td>
</tr>
<tr class="even">
<td><p>61</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/クリスチャン・ヒップホップ" title="wikilink">Christian Rap</a></p></td>
</tr>
<tr class="odd">
<td><p>62</p></td>
<td><p>Pop/Funk</p></td>
</tr>
<tr class="even">
<td><p>63</p></td>
<td><p><a href="../Page/ジャングル_(音楽).md" title="wikilink">Jungle</a></p></td>
</tr>
<tr class="odd">
<td><p>64</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/w:Indigenous_music_of_North_America" title="wikilink">Native American</a></p></td>
</tr>
<tr class="even">
<td><p>65</p></td>
<td><p><a href="../Page/キャバレー.md" title="wikilink">Cabaret</a> |-Acid Jazz</p></td>
</tr>
<tr class="odd">
<td><p>67</p></td>
<td><p><a href="../Page/サイケデリック・ミュージック.md" title="wikilink">Psychedelic</a></p></td>
</tr>
<tr class="even">
<td><p>68</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>69</p></td>
<td><p><a href="../Page/ショー・チューン.md" title="wikilink">Showtunes</a></p></td>
</tr>
<tr class="even">
<td><p>70</p></td>
<td><p><a href="../Page/予告編.md" title="wikilink">Trailer</a></p></td>
</tr>
<tr class="odd">
<td><p>71</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Lo-Fi" title="wikilink">Lo-Fi</a></p></td>
</tr>
<tr class="even">
<td><p>72</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>73</p></td>
<td><p><a href="../Page/ガレージロック.md" title="wikilink">Acid Punk</a></p></td>
</tr>
<tr class="even">
<td><p>74</p></td>
<td><p><a href="../Page/アシッドジャズ.md" title="wikilink">Acid Jazz</a></p></td>
</tr>
<tr class="odd">
<td><p>75</p></td>
<td><p><a href="../Page/ポルカ.md" title="wikilink">Polka</a></p></td>
</tr>
<tr class="even">
<td><p>76</p></td>
<td><p><a href="../Page/レトロ.md" title="wikilink">Retro</a></p></td>
</tr>
<tr class="odd">
<td><p>77</p></td>
<td><p><a href="../Page/ミュージカル.md" title="wikilink">Musical</a></p></td>
</tr>
<tr class="even">
<td><p>78</p></td>
<td><p><a href="../Page/ロックンロール.md" title="wikilink">Rock &amp; Roll</a></p></td>
</tr>
<tr class="odd">
<td><p>79</p></td>
<td><p><a href="../Page/ハードロック.md" title="wikilink">Hard Rock</a></p></td>
</tr>
<tr class="even">
<td><p>80</p></td>
<td><p><a href="../Page/フォークソング.md" title="wikilink">Folk</a></p></td>
</tr>
<tr class="odd">
<td><p>81</p></td>
<td><p><a href="../Page/フォークロック.md" title="wikilink">Folk-Rock</a></p></td>
</tr>
<tr class="even">
<td><p>82</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>83</p></td>
<td><p><a href="../Page/スウィング・ジャズ.md" title="wikilink">Swing</a></p></td>
</tr>
<tr class="even">
<td><p>84</p></td>
<td><p>Fast Fusion</p></td>
</tr>
<tr class="odd">
<td><p>85</p></td>
<td><p><a href="../Page/ビバップ.md" title="wikilink">Bebob</a></p></td>
</tr>
<tr class="even">
<td><p>86</p></td>
<td><p><a href="../Page/ラテン音楽.md" title="wikilink">Latin</a></p></td>
</tr>
<tr class="odd">
<td><p>87</p></td>
<td><p>Revival</p></td>
</tr>
<tr class="even">
<td><p>88</p></td>
<td><p><a href="../Page/ケルト音楽.md" title="wikilink">Celtic</a></p></td>
</tr>
<tr class="odd">
<td><p>89</p></td>
<td><p><a href="../Page/ブルーグラス.md" title="wikilink">Bluegrass</a></p></td>
</tr>
<tr class="even">
<td><p>90</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/w:Avant-garde_music" title="wikilink">Avantgarde</a></p></td>
</tr>
<tr class="odd">
<td><p>91</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ゴシック・ロック" title="wikilink">Gothic Rock</a></p></td>
</tr>
<tr class="even">
<td><p>92</p></td>
<td><p><a href="../Page/プログレッシブ・ロック.md" title="wikilink">Progressive Rock</a></p></td>
</tr>
<tr class="odd">
<td><p>93</p></td>
<td><p><a href="../Page/サイケデリック・ロック.md" title="wikilink">Psychedelic Rock</a></p></td>
</tr>
<tr class="even">
<td><p>94</p></td>
<td><p><a href="../Page/シンフォニック・ロック.md" title="wikilink">Symphonic Rock</a></p></td>
</tr>
<tr class="odd">
<td><p>95</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/w:Slow_rock" title="wikilink">Slow Rock</a></p></td>
</tr>
<tr class="even">
<td><p>96</p></td>
<td><p><a href="../Page/ビッグバンド.md" title="wikilink">Big Band</a></p></td>
</tr>
<tr class="odd">
<td><p>97</p></td>
<td><p><a href="../Page/合唱.md" title="wikilink">Chorus</a></p></td>
</tr>
<tr class="even">
<td><p>98</p></td>
<td><p><a href="../Page/イージーリスニング.md" title="wikilink">Easy Listening</a></p></td>
</tr>
<tr class="odd">
<td><p>99</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/アンプラグド" title="wikilink">Acoustic</a></p></td>
</tr>
<tr class="even">
<td><p>100</p></td>
<td><p><a href="../Page/ユーモア.md" title="wikilink">Humour</a></p></td>
</tr>
<tr class="odd">
<td><p>101</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/w:Speech" title="wikilink">Speech</a></p></td>
</tr>
<tr class="even">
<td><p>102</p></td>
<td><p><a href="../Page/シャンソン.md" title="wikilink">Chanson</a></p></td>
</tr>
<tr class="odd">
<td><p>103</p></td>
<td><p><a href="../Page/オペラ.md" title="wikilink">Opera</a></p></td>
</tr>
<tr class="even">
<td><p>104</p></td>
<td><p><a href="../Page/重奏.md" title="wikilink">Chamber Music</a></p></td>
</tr>
<tr class="odd">
<td><p>105</p></td>
<td><p><a href="../Page/ソナタ.md" title="wikilink">Sonata</a></p></td>
</tr>
<tr class="even">
<td><p>106</p></td>
<td><p><a href="../Page/交響曲.md" title="wikilink">Symphony</a></p></td>
</tr>
<tr class="odd">
<td><p>107</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/w:Booty_bass" title="wikilink">Booty Bass</a></p></td>
</tr>
<tr class="even">
<td><p>108</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/w:Primus" title="wikilink">Primus</a></p></td>
</tr>
<tr class="odd">
<td><p>109</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/w:Porn_groove" title="wikilink">Porn Groove</a></p></td>
</tr>
<tr class="even">
<td><p>110</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/風刺" title="wikilink">Satire</a></p></td>
</tr>
<tr class="odd">
<td><p>111</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/w:Slow_jam" title="wikilink">Slow Jam</a></p></td>
</tr>
<tr class="even">
<td><p>112</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/w:Club_music" title="wikilink">Club</a></p></td>
</tr>
<tr class="odd">
<td><p>113</p></td>
<td><p><a href="../Page/タンゴ.md" title="wikilink">Tango</a></p></td>
</tr>
<tr class="even">
<td><p>114</p></td>
<td><p><a href="../Page/サンバ_(ブラジル).md" title="wikilink">Samba</a></p></td>
</tr>
<tr class="odd">
<td><p>115</p></td>
<td><p><a href="../Page/フォルクローレ.md" title="wikilink">Folklore</a></p></td>
</tr>
<tr class="even">
<td><p>116</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/バラッド" title="wikilink">Ballad</a></p></td>
</tr>
<tr class="odd">
<td><p>117</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/w:Power_ballad" title="wikilink">Power Ballad</a></p></td>
</tr>
<tr class="even">
<td><p>118</p></td>
<td><p>Rhythmic Soul</p></td>
</tr>
<tr class="odd">
<td><p>119</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/w:Freestyle_music" title="wikilink">Freestyle</a></p></td>
</tr>
<tr class="even">
<td><p>120</p></td>
<td><p><a href="../Page/デュエット.md" title="wikilink">Duet</a></p></td>
</tr>
<tr class="odd">
<td><p>121</p></td>
<td><p><a href="../Page/パンク・ロック.md" title="wikilink">Punk Rock</a></p></td>
</tr>
<tr class="even">
<td><p>122</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/w:Drum_solo" title="wikilink">Drum Solo</a></p></td>
</tr>
<tr class="odd">
<td><p>123</p></td>
<td><p><a href="../Page/ア・カペラ.md" title="wikilink">A capella</a></p></td>
</tr>
<tr class="even">
<td><p>124</p></td>
<td><p>Euro-<a href="../Page/ハウス_(音楽).md" title="wikilink">House</a></p></td>
</tr>
<tr class="odd">
<td><p>125</p></td>
<td><p><a href="../Page/ダンスホールレゲエ.md" title="wikilink">Dance Hall</a></p></td>
</tr>
<tr class="even">
<td><p>126</p></td>
<td><p><a href="../Page/ゴアトランス.md" title="wikilink">Goa</a></p></td>
</tr>
<tr class="odd">
<td><p>127</p></td>
<td><p><a href="../Page/ドラムンベース.md" title="wikilink">Drum &amp; Bass</a></p></td>
</tr>
<tr class="even">
<td><p>128</p></td>
<td><p>Club-<a href="../Page/ハウス_(音楽).md" title="wikilink">House</a></p></td>
</tr>
<tr class="odd">
<td><p>129</p></td>
<td><p><a href="../Page/ハードコア・パンク.md" title="wikilink">Hardcore</a></p></td>
</tr>
<tr class="even">
<td><p>130</p></td>
<td><p>Terror</p></td>
</tr>
<tr class="odd">
<td><p>131</p></td>
<td><p><a href="../Page/インディーズ.md" title="wikilink">Indie</a></p></td>
</tr>
<tr class="even">
<td><p>132</p></td>
<td><p><a href="../Page/ブリットポップ.md" title="wikilink">BritPop</a></p></td>
</tr>
<tr class="odd">
<td><p>133</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/w:Afro-punk" title="wikilink">Afro-punk</a></p></td>
</tr>
<tr class="even">
<td><p>134</p></td>
<td><p>Polsk Punk</p></td>
</tr>
<tr class="odd">
<td><p>135</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/w:Beat_music" title="wikilink">Beat</a></p></td>
</tr>
<tr class="even">
<td><p>136</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/クリスチャン・ヒップホップ" title="wikilink">Christian gangsta rap</a></p></td>
</tr>
<tr class="odd">
<td><p>137</p></td>
<td><p><a href="../Page/ヘヴィメタル.md" title="wikilink">Heavy Metal</a></p></td>
</tr>
<tr class="even">
<td><p>138</p></td>
<td><p><a href="../Page/ブラックメタル.md" title="wikilink">Black Metal</a></p></td>
</tr>
<tr class="odd">
<td><p>139</p></td>
<td><p><a href="../Page/クロスオーバー_(音楽).md" title="wikilink">Crossover</a></p></td>
</tr>
<tr class="even">
<td><p>140</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/コンテンポラリー・クリスチャン・ミュージック" title="wikilink">Contemporary Christian</a></p></td>
</tr>
<tr class="odd">
<td><p>141</p></td>
<td><p><a href="../Page/クリスチャン・ロック.md" title="wikilink">Christian Rock</a></p></td>
</tr>
<tr class="even">
<td><p>142</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/メレンゲ_(音楽)" title="wikilink">Merengue</a></p></td>
</tr>
<tr class="odd">
<td><p>143</p></td>
<td><p><a href="../Page/サルサ_(音楽).md" title="wikilink">Salsa</a></p></td>
</tr>
<tr class="even">
<td><p>144</p></td>
<td><p><a href="../Page/スラッシュメタル.md" title="wikilink">Thrash Metal</a></p></td>
</tr>
<tr class="odd">
<td><p>145</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/アニメソング" title="wikilink">Anime</a></p></td>
</tr>
<tr class="even">
<td><p>146</p></td>
<td><p><a href="../Page/J-POP.md" title="wikilink">JPop</a></p></td>
</tr>
<tr class="odd">
<td><p>147</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/シンセポップ" title="wikilink">Synthpop</a></p></td>
</tr>
</tbody>
</table>

### ID3v2

ID3v1.1を拡張、改良した形式。ID3v1のネックだった字数制限がほぼ無くなり、[Unicode](../Page/Unicode.md "wikilink")のサポートなど非常に便利になっている。しかし、タグを記録するときに増えるファイルサイズがID3v1より大きかったり、古いプレイヤーでは表示に対応していないものがある。

#### v1からの主な変更点

  - 項目別のサイズ制限は16MB、全体のタグサイズ制限は256MBになった
  - 記入できる項目の増加
  - Unicodeのサポート
  - 画像が含められる（ただし、対応しているプレイヤーは少ない）

#### バージョン番号

現在、ID3v2には「ID3v2.2」「ID3v2.3」「ID3v2.4」の3つがある。仕様書\[3\]によれば、例えば「ID3v2.3」というバージョン表記は、「ID3v2」という規格の「メジャーバージョン3」となる。決して「ID3」の「バージョン2.3」ではない。

前記仕様書によれば、メジャーバージョン間の[前方互換](https://ja.wikipedia.org/wiki/前方互換 "wikilink")性は保証されていない。そのため、例えば「ID3v2.3」をサポートするソフトウェアは「ID3v2.4」のタグ情報は読み込めない。この場合、サポートするメジャーバージョンより大きなバージョンのタグを読み込もうとする場合は、単純にタグ全体を読み飛ばすべきと記述されている。

各バージョン間の違いは、「ID3v2.2」から「ID3v2.3」に変更されたとき、フレームIDが3桁から4桁に増えた。このため、メジャーバージョン2と3ではフレームIDに互換性がなくなった。「ID3v2.3」から「ID3v2.4」に変更されたとき、メジャーバージョン4からは文字コードとして[UTF-8](../Page/UTF-8.md "wikilink")のサポートが追加された（これ以前のユニコード対応は[UTF-16](../Page/UTF-16.md "wikilink")のみ）。

ID3タグを制定している組織「ID3.org」によれば、現在最も普及しているバージョンは「ID3v2.3」である。最新バージョンとなる「ID3v2.4」は、一部の改訂箇所に不同意があったり、ソフト・ハードウェア市場がなかなか対応を行おうとしないため、いまだ普及に至っていない、と説明されている\[4\]。

#### 仕様

ID3v2タグはファイルの先頭に配置され、大まかに分けて、ID3v2ヘッダ、拡張ヘッダ、フレーム(複数)、パディング領域の4領域から構成され、この順に並んでいる。以下に各領域ごとの詳細を示す。

| 開始位置 | 長さ | 説明 |- align="center"| | 0 | 3 | “ID3” の[マジックナンバー](https://ja.wikipedia.org/wiki/マジックナンバー_\(フォーマット識別子\) "wikilink")3文字 |- align="center"| | 3 | 2 | バージョン |- align="center"| | 5 | 1 | フラグ |- align="center"| | 6 | 4 | サイズ |
| ---- | -- | --------------------- | - | - | -------------------------------------------------------------------------------------------------------- | - | - | ------------------------ | - | - | ---------------------- | - | - | --- |

ID3v2ヘッダ

計10バイト。サイズは各バイトの最上位ビットが無効であり、有効な値は28ビットとなる。

| 開始位置 | 長さ | 説明 |- align="center"| | 0 | 4 | この拡張ヘッダのサイズ |- align="center"| | 4 | 2 | 拡張フラグ |- align="center"| | 6 | 4 | パディング領域のサイズ |
| ---- | -- | --------------------- | - | - | ------------------------------ | - | - | ------------------------ | - | - | ----------- |

拡張ヘッダ

| offset | 長さ | 記述 |- align="center"| | 0 | 4 | フレームID(種別1バイト+ネーム3バイト) |- align="center"| | 4 | 4 | フレームサイズ |- align="center"| | 8 | 2 | フラグ |- align="center"| | 10 | 可変長 | フレームデータ |
| ------ | -- | --------------------- | - | - | ----------------------------------------- | - | - | -------------------------- | - | - | ---------------------- | -- | --- | ------- |

各フレーム

| Frame | Description                                                                                                                    | Notes                             |
| ----- | ------------------------------------------------------------------------------------------------------------------------------ | --------------------------------- |
| AENC  | Audio encryption                                                                                                               |                                   |
| APIC  | Attached picture                                                                                                               |                                   |
| COMM  | Comments                                                                                                                       |                                   |
| COMR  | Commercial frame                                                                                                               |                                   |
| ENCR  | Encryption method registration                                                                                                 |                                   |
| EQUA  | Equalization                                                                                                                   | replaced by EQU2 in v2.4          |
| ETCO  | Event timing codes                                                                                                             |                                   |
| GEOB  | General encapsulated object                                                                                                    |                                   |
| GRID  | Group identification registration                                                                                              |                                   |
| IPLS  | Involved people list                                                                                                           | replaced by TMCL and TIPL in v2.4 |
| LINK  | Linked information                                                                                                             |                                   |
| MCDI  | Music CD identifier                                                                                                            |                                   |
| MLLT  | MPEG location lookup table                                                                                                     |                                   |
| OWNE  | Ownership frame                                                                                                                |                                   |
| PRIV  | Private frame                                                                                                                  |                                   |
| PCNT  | Play counter                                                                                                                   |                                   |
| POPM  | Popularimeter                                                                                                                  |                                   |
| POSS  | Position synchronisation frame                                                                                                 |                                   |
| RBUF  | Recommended buffer size                                                                                                        |                                   |
| RVAD  | Relative volume adjustment                                                                                                     | replaced by RVA2 in v2.4          |
| RVRB  | Reverb                                                                                                                         |                                   |
| SYLT  | Synchronized lyric/text                                                                                                        |                                   |
| SYTC  | Synchronized tempo codes                                                                                                       |                                   |
| TALB  | Album/Movie/Show title                                                                                                         |                                   |
| TBPM  | [Beats per minute](https://ja.wikipedia.org/wiki/Beats_per_minute "wikilink") (BPM)                                            |                                   |
| TCOM  | Composer                                                                                                                       |                                   |
| TCON  | Content type                                                                                                                   |                                   |
| TCOP  | Copyright message                                                                                                              |                                   |
| TDAT  | Date                                                                                                                           | replaced by TDRC in v2.4          |
| TDLY  | Playlist delay                                                                                                                 |                                   |
| TENC  | Encoded by                                                                                                                     |                                   |
| TEXT  | Lyricist/Text writer                                                                                                           |                                   |
| TFLT  | File type                                                                                                                      |                                   |
| TIME  | Time                                                                                                                           | replaced by TDRC in v2.4          |
| TIT1  | Content group description                                                                                                      |                                   |
| TIT2  | Title/songname/content description                                                                                             |                                   |
| TIT3  | Subtitle/Description refinement                                                                                                |                                   |
| TKEY  | [Initial key](https://ja.wikipedia.org/wiki/musical_key "wikilink")                                                            |                                   |
| TLAN  | Language(s)                                                                                                                    |                                   |
| TLEN  | Length                                                                                                                         |                                   |
| TMED  | Media type                                                                                                                     |                                   |
| TOAL  | Original album/movie/show title                                                                                                |                                   |
| TOFN  | Original filename                                                                                                              |                                   |
| TOLY  | Original lyricist(s)/text writer(s)                                                                                            |                                   |
| TOPE  | Original artist(s)/performer(s)                                                                                                |                                   |
| TORY  | Original release year                                                                                                          | replaced by TDOR in v2.4          |
| TOWN  | File owner/licensee                                                                                                            |                                   |
| TPE1  | Lead performer(s)/Soloist(s)                                                                                                   |                                   |
| TPE2  | Band/orchestra/accompaniment                                                                                                   |                                   |
| TPE3  | Conductor/performer refinement                                                                                                 |                                   |
| TPE4  | Interpreted, remixed, or otherwise modified by                                                                                 |                                   |
| TPOS  | Part of a set                                                                                                                  |                                   |
| TPUB  | Publisher                                                                                                                      |                                   |
| TRCK  | Track number/Position in set                                                                                                   |                                   |
| TRDA  | Recording dates                                                                                                                | replaced by TDRC in v2.4          |
| TRSN  | Internet radio station name                                                                                                    |                                   |
| TRSO  | Internet radio station owner                                                                                                   |                                   |
| TSIZ  | Size                                                                                                                           | deprecated in v2.4                |
| TSRC  | [International Standard Recording Code](https://ja.wikipedia.org/wiki/International_Standard_Recording_Code "wikilink") (ISRC) |                                   |
| TSSE  | Software/Hardware and settings used for encoding                                                                               |                                   |
| TYER  | Year                                                                                                                           | replaced by TDRC in v2.4          |
| TXXX  | User defined text information frame                                                                                            |                                   |
| UFID  | Unique file identifier                                                                                                         |                                   |
| USER  | Terms of use                                                                                                                   |                                   |
| USLT  | Unsynchronized lyric/text transcription                                                                                        |                                   |
| WCOM  | Commercial information                                                                                                         |                                   |
| WCOP  | Copyright/Legal information                                                                                                    |                                   |
| WOAF  | Official audio file webpage                                                                                                    |                                   |
| WOAR  | Official artist/performer webpage                                                                                              |                                   |
| WOAS  | Official audio source webpage                                                                                                  |                                   |
| WORS  | Official internet radio station homepage                                                                                       |                                   |
| WPAY  | Payment                                                                                                                        |                                   |
| WPUB  | Publishers official webpage                                                                                                    |                                   |
| WXXX  | User defined URL link frame                                                                                                    |                                   |

項目

## 参考

<references/>

## 外部リンク

  - [ID3.org（英語）](http://www.id3.org/)

[Category:メタデータ](https://ja.wikipedia.org/wiki/Category:メタデータ "wikilink")

1.  v1 でコメントが最大文字数に満たない場合、 残りが 0 (NULL) になることを利用し、v1 にしか対応しないソフトウェアにそこでコメントが終わったと判断させ、 トラック番号の部分をコメントと認識しないようにするためのものである。
2.
3.  [セクション3.1. ID3v2 header](http://www.id3.org/d3v2.3.0)
4.  [ID3.orgのWelcomeの節](http://www.id3.org/Home/)