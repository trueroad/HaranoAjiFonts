<!-- -*- coding: utf-8 -*- -->
# Harano Aji Fonts generator

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

See [
Harano Aji Fonts generator
](https://github.com/trueroad/HaranoAjiFonts-generator)
for details.

## Release Notes

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

Copyright (C) 2019, 2020 Masamichi Hosoda

The license of the generator is BSD 2-Clause. See [LICENSE](./LICENSE).
The license of the generated fonts is SIL Open Font License 1.1.
