<!-- -*- coding: utf-8 -*- -->
# 原ノ味フォント / Harano Aji Fonts

源ノ明朝・源ノ角ゴシック（以下、源ノフォント）を
Adobe-Japan1 （以下、AJ1）フォントになるように組み替えた
「原ノ味フォント（原ノ味明朝、原ノ味角ゴシック）」
を作ってみました。
CID の対応がとれないため抜けてしまうグリフがある、
いくつかの OpenType テーブルを落としている、
などがあるため実験的なフォントにとどまっています。

「原ノ味」というのは、
源ノフォントからグリフやテーブルが抜けていることを表すために
「氵（さんずい）」を取り、
AJ1 をもじって AJI にして
音から「味」という字をあてたものです。

## フォントファイルの配布

原ノ味フォントは
[
https://github.com/trueroad/HaranoAjiFonts
](https://github.com/trueroad/HaranoAjiFonts)
で配布しています。
フォントファイルはサイズが大き目で、全 14 フォントあるため、
リポジトリの容量が大きくなりがちと考えており、
古いバージョンのフォントは随時消していきたいと思っています。
そのため、新しいフォントをリリースする際には
上記リポジトリの master ブランチを forced update する運用にし、
余裕があるのであれば tag で古いフォントにアクセスできるように
しておくつもりです。

## 詳細

詳細は[
原ノ味フォント生成プログラム
](https://github.com/trueroad/HaranoAjiFonts-generator)
をご覧ください。

## 履歴

* [
20190310
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20190310)
    + 縦書きなどのグリフに対応
        - OpenType feature `fwid`, `hwid`, `pwid`, `ruby`, `vert`
          を読み込んで対応付けするグリフを増やしました。
          ただし OpenType feature そのものには対応していませんので、
          今回追加されたグリフにアクセスするには
          CID を直接指定する、 V 系の CMap ファイルを経由する、
          などの必要があります。
    + グリフ数
        - 原ノ味明朝：16678
        - 原ノ味角ゴシック：16683

* [
20190309
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20190309)
    + Adobe-Japan1-6 全漢字グリフに対応
        - 異字体セレクタや OpenType feature には対応していませんので、
          今回追加されたグリフにアクセスするには
          CID を直接指定する必要があります。
    + `BASE`, `VORG`, `vhea`, `vmtx` テーブルを追加
    + グリフ数
        - 原ノ味明朝：16425
        - 原ノ味角ゴシック：16429

* [
20190303
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20190303)
    + 初版
        - 源ノ明朝 1.001、源ノ角ゴシック 2.000
        - ttx 3.38.0, UniJIS2004-UTF32-H 1.020
    + グリフ数
        - 原ノ味明朝：15213
        - 原ノ味角ゴシック：15215

## ライセンス / LICENSE

Copyright (C) 2019 Masamichi Hosoda, with Reserved Font Name 'Harano Aji'.

Copyright 2014, 2015, 2018 Adobe (http://www.adobe.com/),
with Reserved Font Name 'Source'.

Copyright 2017 Adobe Systems Incorporated (http://www.adobe.com/),
with Reserved Font Name 'Source'.

Source is a trademark of Adobe in the United States and/or other countries.

This Font Software is licensed under the SIL Open Font License, Version 1.1.
See [LICENSE](LICENSE).

原ノ味フォントは源ノフォントの派生フォントになるため
SIL Open Font License 1.1 です。
