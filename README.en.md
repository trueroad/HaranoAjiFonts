<!-- -*- coding: utf-8 -*- -->
# Harano Aji Fonts

[ [Japanese （日本語）](README.md) / English ]

Harano Aji Fonts (Harano Aji Mincho and Harano Aji Gothic)
are fonts obtained by replacing Adobe-Identity-0 (AI0) CIDs
of Source Han fonts (Source Han Serif and Source Han Sans)
with Adobe-Japan1 (AJ1) CIDs.

There are 14 fonts, 7 weights each for Mincho and Gothic.

## Distribution

* Distribution of Harano Aji Fonts
    - TeX Live
        - Contained in TeX Live 2020 and later.
          Default font for Japanese except for a few engines.
        - For TeX Live 2019, contained in updates since mid-February 2020.
          (Not the default font.)
    - W32TeX
        - Contained after March 23, 2020.
    - CTAN
        - The major 7 fonts used in the preset settings in some packages.
            - [
https://www.ctan.org/pkg/haranoaji
](https://www.ctan.org/pkg/haranoaji)
        - The remaining 7 fonts.
            - [
https://www.ctan.org/pkg/haranoaji-extra
](https://www.ctan.org/pkg/haranoaji-extra)
    - GitHub
        - [
https://github.com/trueroad/HaranoAjiFonts
](https://github.com/trueroad/HaranoAjiFonts)

The following files are also distributed.

* [
Various TeX files
](https://github.com/trueroad/HaranoAjiFonts-generator/tree/master/tex)
    + Document, samples, test files, etc.
* fontspec file
    + [
HaranoAjiMincho.fontspec
](https://github.com/trueroad/HaranoAjiFonts-generator/tree/master/tex/HaranoAjiMincho.fontspec),
      [
HaranoAjiGothic.fontspec
](https://github.com/trueroad/HaranoAjiFonts-generator/tree/master/tex/HaranoAjiGothic.fontspec)
    + Not required when using preset settings such as `luatexja-preset`

Map files for pTeX / pLaTeX are contained in
[ptex-fontmaps](https://www.ctan.org/pkg/ptex-fontmaps)
20200217.0 or later.

There are **experimentally** generated Simplified Chinese,
Traditional Chinese, and Korean fonts.

* (Experimental) Simplified Chinese (CN): Adobe-GB1
    + [
https://github.com/trueroad/HaranoAjiFontsCN
](https://github.com/trueroad/HaranoAjiFontsCN)
* (Experimental) Traditional Chinese (TW): Adobe-CNS1
    + [
https://github.com/trueroad/HaranoAjiFontsTW
](https://github.com/trueroad/HaranoAjiFontsTW)
* (Experimental) Korean (KR): Adobe-KR
    + [
https://github.com/trueroad/HaranoAjiFontsKR
](https://github.com/trueroad/HaranoAjiFontsKR)
* (Experimental) Korean (K1): Adobe-Korea1
    + [
https://github.com/trueroad/HaranoAjiFontsK1
](https://github.com/trueroad/HaranoAjiFontsK1)

See [
Harano Aji Fonts generator
](https://github.com/trueroad/HaranoAjiFonts-generator)
for details.

## Release Notes

* [
20220220
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20220220)
(JP, CN, TW, KR, K1)
    + Add glyphs by 180 and 270 (-90) degree rotation (JP)
    + Add kana similar CIDs to pwid and pwidvert (JP)
    + Fix making conversion table from GSUB single feature (CN, K1)
    + Improve adding GSUB vert substituion (JP, CN, TW, KR)
    + Update
        + ttx 4.29.1
    + Number of contained glyphs (JP)
        - HaranoAjiMincho: 17567
          (conversion 16867 + glyph processing 699 + .notdef 1)
        - HaranoAjiGothic: 17567
          (conversion 16866 + glyph processing 700 + .notdef 1)
* [
20220130
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20220130)
(JP, CN, TW, KR, K1) test release
    + Based on SourceHanSerif 2.001 (JP, CN, TW, KR, K1)
        + JP: CID+13729 and CID+14019 are now contained again.
    + Update
        + SourceHanSerif 2.001
        + ttx 4.29.0
        + Python 3.9.10
    + Number of contained glyphs (JP)
        - HaranoAjiMincho: 17559
          (conversion 16867 + glyph processing 691 + .notdef 1)
        - HaranoAjiGothic: 17559
          (conversion 16866 + glyph processing 692 + .notdef 1)
* [
20211103
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20211103)
(JP, CN, TW, KR, K1) test release
    + This is a test release.
        + There is a major change due to a major version up of
          SourceHanSerif 2.000.
        + JP: CID+13729 and CID+14019 are missing.
        + Please test.
    + Based on SourceHanSerif 2.000 (JP, CN, TW, KR, K1)
    + Based on SourceHanSans 2.004 (JP, CN, TW, KR, K1)
    + Update
        + SourceHanSerif 2.000
        + SourceHanSans 2.004
        + ttx 4.27.1
    + Number of contained glyphs (JP)
        - HaranoAjiMincho: 17557
          (conversion 16865 + glyph processing 691 + .notdef 1)
        - HaranoAjiGothic: 17559
          (conversion 16866 + glyph processing 692 + .notdef 1)
* [
20210410
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20210410)
(JP, CN, TW, KR, K1)
    + Based on SourceHanSans 2.003 (JP, CN, TW, KR, K1)
    + Update
        + SourceHanSans 2.003
        + ttx 4.22.0
    + Number of contained glyphs (JP)
        - HaranoAjiMincho: 17554
          (conversion 16862 + glyph processing 691 + .notdef 1)
        - HaranoAjiGothic: 17559
          (conversion 16866 + glyph processing 692 + .notdef 1)
* [
20210130
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20210130)
(JP)
    + Fix GPOS vpal feature for vertical Kana glyphs
    + Fix GSUB vkna feature from [fixing Adobe-Japan1-7
GSUB feature](https://github.com/adobe-type-tools/Adobe-Japan1/pull/4)
    + Update
        + ttx 4.19.1
        + aj17-gsub-jp04.fea (2021-01-25)
    + Number of contained glyphs (JP)
        - HaranoAjiMincho: 17554
          (conversion 16862 + glyph processing 691 + .notdef 1)
        - HaranoAjiGothic: 17559
          (conversion 16867 + glyph processing 691 + .notdef 1)
* [
20210102
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20210102)
(JP)
    + Fix proportional vertical GSUB substitution
    + Fix proportional vertical Kana glyph
    + Number of contained glyphs (JP)
        - HaranoAjiMincho: 17554
          (conversion 16862 + glyph processing 691 + .notdef 1)
        - HaranoAjiGothic: 17559
          (conversion 16867 + glyph processing 691 + .notdef 1)
* [
20210101
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20210101)
(JP, CN, TW, KR, K1)
    + Based on SourceHanSans 2.002 (JP, CN, TW, KR, K1)
    + Add many Kana glyphs (JP)
    + Add many GSUB features and entries (JP)
    + Update
        + SourceHanSans 2.002
        + ttx 4.18.2
    + Number of contained glyphs (JP)
        - HaranoAjiMincho: 17554
          (conversion 16862 + glyph processing 691 + .notdef 1)
        - HaranoAjiGothic: 17559
          (conversion 16867 + glyph processing 691 + .notdef 1)
* [
20200912
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20200912)
(JP)
    + Add glyphs that don't have a single Unicode code point
      and are accessible only by ligature substitute in the `GSUB` table (JP)
    + Update
        + ttx 4.14.0
    + Number of contained glyphs (JP)
        - HaranoAjiMincho: 16904
          (conversion 16693 + glyph processing 210 + .notdef 1)
        - HaranoAjiGothic: 16909
          (conversion 16698 + glyph processing 210 + .notdef 1)
* [
20200612
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20200612)
(JP, CN, TW, KR, K1)
    + Add `cmap` table from CMap such as AJ1
      and change CID in `cmap` table according to CMap (JP, CN, TW, KR, K1)
    + Add AJ1 CID+151 by copying from AJ1 CID+14 (JP)
    + Change size reducing method for size exceeded `cmap` table format 4
      (TW, KR)
    + Add `GPOS` table (KR)
    + Improve generator
    + Update
        + ttx 4.12.0
    + Number of contained glyphs (JP)
        - HaranoAjiMincho: 16888
          (conversion 16678 + glyph processing 209 + .notdef 1)
        - HaranoAjiGothic: 16893
          (conversion 16683 + glyph processing 209 + .notdef 1)
* [
20200524
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20200524)
(JP, CN, TW, KR, K1)
    + Add proportional Kana glyphs (JP)
    + Add some space glyphs (JP, KR)
    + Fix broken `GPOS` table such as palt (JP, CN, TW, KR)
    + Change width of Monospaced glyphs in **experimental** Korean font (KR)
    + Add **experimental** Korean font variation (K1)
        + Korean: Adobe-Korea1, suffix K1
            + UniKS-UTF32-H 1.008
    + Update
        + ttx 4.10.2
    + Number of contained glyphs (JP)
        - HaranoAjiMincho: 16887
          (conversion 16678 + glyph processing 208 + .notdef 1)
        - HaranoAjiGothic: 16892
          (conversion 16683 + glyph processing 208 + .notdef 1)
* 20200516 (CN, TW, KR)
    + The generator can now generate **experimental**
      Simplified Chinese, Traditional Chinese, and Korean fonts.
    + The font name for each langulage has the two letter suffix
      same as Source Han fonts.
        + Simplified Chinese: Adobe-GB1, suffix CN
            + UniGB-UTF32-H 1.016
        + Traditional Chinese: Adobe-CNS1, suffix TW
            + UniCNS-UTF32-H 1.019
        + Korean: Adobe-KR, suffix KR
            + UniAKR-UTF32-H 1.002
    + No change for Japanese version, no release this time.
    + The suffix is used as an abbreviation for each language font.
        + The Japanese font name has no suffix,
          but the abbreviation is JP.
    + Update
        - ttx 4.10.0
* [
20200418
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20200418)
    + Add 5 glyphs for vertical writing
    + Reduce file size
    + Readjust the drawing position of 2 glyphs
    + Fix LSB/TSB of adjusted glyphs
    + Remove adjusted glyphs from `GPOS` table
    + Update
        - ttx 4.7.0
    + Number of contained glyphs
        - HaranoAjiMincho: 16684
        - HaranoAjiGothic: 16689
* [
20200215
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20200215)
    + For glyphs with overwritten width, position adjustment such as centering
        + Contribution from [@h20y6m](https://github.com/h20y6m)
    + Update
        - ttx 4.3.0, UniJIS2004-UTF32-H 1.021
    + Number of contained glyphs
        - HaranoAjiMincho: 16679
        - HaranoAjiGothic: 16684
* [
20190824
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20190824)
    + Overwrite glyph width with AJ1 definition
    + Use AJ1-7 GSUB
    + Update
        - ttx 4.0.0, ~~UniJIS2004-UTF32-H 1.021~~
    + Number of contained glyphs
        - HaranoAjiMincho: 16678
        - HaranoAjiGothic: 16684
        - Changed counting method
* [
20190501
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20190501)
    + Become full set fonts with dummy glyph
    + Update
        - ttx 3.41.0
    + Number of contained glyphs
        - It shouldn't change, but it's difficult to count
          the number of glyphs due to the effect of dummy glyphs...
* [
20190413
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20190413)
    + Support Adobe-Japan1-7
    + Based on SourceHanSans 2.001
    + Update
        - SourceHanSans 2.001
        - ttx 3.40.0
    + Number of contained glyphs
        - HaranoAjiMincho: 16678
        - HaranoAjiGothic: 16684

* [
20190324
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20190324)
    + Support Variation Selector
    + Support OpenType feature
    + Support JIS X 0208 glyphs
    + Add map files for pTeX / pLaTeX and .tex files
    + Update
        - ttx 3.39.0
    + Number of contained glyphs
        - HaranoAjiMincho: 16678
        - HaranoAjiGothic: 16683

* [
20190310
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20190310)
    + Add some glyphs for vertical writing etc.
    + Number of contained glyphs
        - HaranoAjiMincho: 16678
        - HaranoAjiGothic: 16683

* [
20190309
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20190309)
    + Contain all Adobe-Japan1-6 kanji glyphs
    + Add `BASE`, `VORG`, `vhea`, `vmtx` tables
    + Number of contained glyphs
        - HaranoAjiMincho: 16425
        - HaranoAjiGothic: 16429

* [
20190303
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20190303)
    + First release
        - Based on SourceHanSerif 1.001, SourceHanSans 2.000
        - ttx 3.38.0, UniJIS2004-UTF32-H 1.020
    + Number of contained glyphs
        - HaranoAjiMincho: 15213
        - HaranoAjiGothic: 15215

## LICENSE

Copyright (C) 2019-2022
Masamichi Hosoda, with Reserved Font Name 'Harano Aji'.

Copyright 2014-2021 Adobe (http://www.adobe.com/),
with Reserved Font Name 'Source'.

Copyright 2017-2022 Adobe (http://www.adobe.com/),
with Reserved Font Name 'Source'.

Source is a trademark of Adobe in the United States and/or other countries.

This Font Software is licensed under the SIL Open Font License, Version 1.1.
See [LICENSE](LICENSE).
