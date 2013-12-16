2.5dBUTTON
==========
[**Ligature Symbols**][Ligature Symbols]を使用した、浮き上がるボタンのライブラリです。  
実際の押しボタンのように側面が表示されるので、リンクテキストなどを押下可能なボタンとして表示できます。

アイコンはGUIに使用されているものや、企業ロゴなど239種類。  
該当する単語を入力するだけで簡単に使用できます。  
png, gifなどの画像は必要ありません。

HTML, SCSSのみの構成で、簡単にカスタマイズできます。

ジェネレーターによるWEBページでの作成はこちらから  
[**2.5dBUTTON**][2.5dBUTTON]

Installation
============
* ZIPでダウンロード

* [**2.5dBUTTON**][2.5dBUTTON]にてジェネレーターで作成してダウンロード

Usage:HTML
==========
ボタンとして使用したい要素に固有の名前をつけ、`<div class="button-content">`とその子要素を入れます。

    <a class="pattern-1">  
      <div class="button-content">
        <span class="icon-font">view</span>
        <span class="button-text">SAMPLE1</span>
      </div>
    </a>  

ICON
----
Ligature Symbolsを使用しています。  
[**Ligature Symbols**][Ligature Symbols]のウェブサイトを参照して`<span class="icon-font"></span>`に、アイコンに該当する単語を入力してください。  
アイコンを指定しない場合は`<span class="icon-font"></span>`を削除してください。  

    <span class="icon-font">view</span>  

TEXT
----
`<span class="button-text"></span>`内に入力します。  
テキストを指定しない場合は`<span class="button-text"></span>`を削除してください。

    <span class="button-text">SAMPLE1</span>  

Usage:SCSS
==========
`@mixin general-button`を、固有の名前を持つ要素に`@include`して使います。  

    @mixin general-button($label-size, $icon-size, $label-color, $popup-dist, $horizontal-padding, $vertical-padding, $radius, $speed, $button-color, $side-darkness, $darken: darken($button-color, $side-darkness)) {
    
    ...

    }

    .pattern-1 {
      @include general-button(15px, 27px, #f8f8f8, 5px, 1px, 14px, 5px, 50ms, #b5c23a, 15%)
    }


変更できる値  
------------

* $label-size: テキストの大きさ  
* $icon-size: アイコンの大きさ  
* $label-color: テキストの色  
* $popup-dist: ホバー時の移動距離  
* $horizontal-padding: 上下の間隔  
* $vertical-padding: 左右の間隔  
* $radius: 角の丸さ  
* $speed: ホバーの速度  
* $button-color: 背景色  
* $side-darkness: ボタン側面の影の濃さ  

ICON
----
Ligature Symbolsを適用します。  
`@fontface`と`.icon-font`をSCSS内に入れてください。  
`@font-face`では`font`ディレクトリのパスを指定しています。  
ディレクトリを移動・変更した場合は書き換えてください。

    @font-face {
      font-family: "LigatureSymbols";
      src: url("../font/LigatureSymbols-2.11.eot");
      src: url("../font/LigatureSymbols-2.11.eot?#iefix") format("embedded-opentype"),
           url("../font/LigatureSymbols-2.11.woff") format("woff"),
           url("../font/LigatureSymbols-2.11.ttf") format("truetype"),
           url("../font/LigatureSymbols-2.11.svg#LigatureSymbols") format("svg");
      font-weight: normal;
      font-style: normal;
    }
  
    .icon-font {
      font-family: "LigatureSymbols";
      -webkit-text-rendering: optimizeLegibility;
      -moz-text-rendering: optimizeLegibility;
      -ms-text-rendering: optimizeLegibility;
      -o-text-rendering: optimizeLegibility;
      text-rendering: optimizeLegibility;
      -webkit-font-smoothing: antialiased;
      -moz-font-smoothing: antialiased;
      -ms-font-smoothing: antialiased;
      -o-font-smoothing: antialiased;
      font-smoothing: antialiased;
      -webkit-font-feature-settings: "liga" 1, "dlig" 1;
      -moz-font-feature-settings: "liga=1, dlig=1";
      -ms-font-feature-settings: "liga" 1, "dlig" 1;
      -o-font-feature-settings: "liga" 1, "dlig" 1;
      font-feature-settings: "liga" 1, "dlig" 1;
    }

Author
======

**NOHT CO.,LTD.**

License
=======

[**2.5dBUTTON**][2.5dBUTTON] is lisenced under [the MIT License (MIT)][MIT_license]  
Copyright (c) 2013 NOHT CO.,LTD.  

[**Ligature Symbols**][Ligature Symbols] is lisenced under [the SIL Open Font License 1.1][Open Font License 1.1]  
`font`ディレクトリ内の以下のファイルはLigature Symbolsの著作物です。

    LigatureSymbols-2.11.eot  
    LigatureSymbols-2.11.otf  
    LigatureSymbols-2.11.svg  
    LigatureSymbols-2.11.ttf  
    LigatureSymbols-2.11.woff  

[2.5dBUTTON]: http:// "2.5dBUTTON"  
[Ligature Symbols]: http://kudakurage.com/ligature_symbols/ "Ligature Symbols"  
[MIT_license]: http:// "MTT_license"  
[Open Font License 1.1]: http://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&id=OFL "Open Font License 1.1"