2.5dBUTTON
==========
Using [**Ligature Symbols**][Ligature Symbols], a unique button library.
They have a push button-like style, so you can use them to display clickable buttons in place of link text.

There are 239 types of icons including items utilizing the GUI and corporate logos,
and can be utilized by simply typing the corresponding word.
There is no need to use image types such as png and gif.

With only HTML and SCSS configuration, you can easily customize it.
And with [**Modernizr.js**][Modernizr.js] plugin, you can support touch devices easily.


Installation
============
* Download ZIP
* Download created buttons with [**2.5dBUTTON**][2.5dBUTTON] Generator.

Usage:HTML
==========
Give a distinct name to the elements you would like to make into a button, and input `<div class="button-content">` and child elements.

    <a class="general-button">
      <div class="button-content">
        <span class="icon-font">view</span>
        <span class="button-text">SAMPLE1</span>
      </div>
    </a>

ICON
----
You can use Ligature Symbols.
References [**Ligature Symbols**][Ligature Symbols], input a corresponding word for the icon to `<span class="icon-font"></span>`.
If the icon is not assigned, please delete `<span class="icon-font"></span>`.

    <span class="icon-font">view</span>

TEXT
----
Input text to `<span class="button-text"></span>`.
If the text is not assigned, please delete `<span class="button-text"></span>`.

    <span class="button-text">SAMPLE1</span>

Usage:SCSS
==========
Import `scss/general_button.scss' to your scss.
Please modify '@import' path in accordance with the environment.

Add the distinctly named element configured in HTML to '@include.'

    @import "scss/general_button.scss"

    .general-button {
      $label-size:;
      $icon-size:;
      $label-color:;
      $popup-dist:;
      $horizontal-padding:;
      $vertical-padding:;
      $radius:;
      $speed:;
      $button-color:;
      $side-darkness:;
      @include general-button($label-size, $icon-size, $label-color, $popup-dist, $horizontal-padding, $vertical-padding, $radius, $speed, $button-color, $side-darkness)
    }

Variables
------------

* $label-size: `px`
* $icon-size: `px`
* $label-color: `Hex`
* $popup-dist: `px`
* $horizontal-padding: `px`
* $vertical-padding: `px`
* $radius: `px`
* $speed: `ms`
* $button-color: `Hex`
* $side-darkness: `%`

Every variable element of the buttons is set up.
Referencing the above list, input values for each variable.

    .general-button {
      $label-size: 18px;
      $icon-size: 27px;
      $label-color: #4385bf;
      $popup-dist: 3px;
      $horizontal-padding: 2px;
      $vertical-padding: 10px;
      $radius: 3px;
      $speed: 50ms;
      $button-color: #ffffff;
      $side-darkness: 15%;
      @include general-button($label-size, $icon-size, $label-color, $popup-dist, $horizontal-padding, $vertical-padding, $radius, $speed, $button-color, $side-darkness)
    }


ICON
----
Ligature Symbols is applied to '@font-face' '.icon-font' inside 'general_button.scss'.
Please modify the font path in accordance with the environment.

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

Usage:JS
==========
If you want to support "Touch devices", please include modernizr.js.
Please modify the script path in accordance with the environment.

    <head>
      <script type="text/javascript" src="js/modernizr-2.6.2.min.js"></script>
    </head>


Operability confirmed
=====================

Browser Support
* Google Chrome
* Firefox
* Safari
* Opera
* Internet Explorer 10+

Author
======

**Yuhei Yamamori**

License
=======

[**2.5dBUTTON**][2.5dBUTTON] is lisenced under [the MIT License (MIT)][MIT_license].
Copyright NOHT CO.,LTD.

The fonts bundled here are not distributed under the terms of the MIT License.
They were created by @kudakurage and are available under the terms of the SIL Open Font License (OFL).

[**Modernizr.js**][Modernizr.js] is lisenced under [the MIT License (MIT)][MIT_license].

[2.5dBUTTON]: http://www.noht.co.jp/2_5dbutton/ "2.5dBUTTON"
[Ligature Symbols]: http://kudakurage.com/ligature_symbols/ "Ligature Symbols"
[MIT_license]: http://opensource.org/licenses/MIT "MIT_license"
[Open Font License 1.1]: http://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&id=OFL "Open Font License 1.1"
[Modernizr.js]: http://modernizr.com/ "Modernizr.js"
