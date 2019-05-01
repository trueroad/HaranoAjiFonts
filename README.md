<!-- -*- coding: utf-8 -*- -->
# 原ノ味フォント / Harano Aji Fonts

源ノ明朝・源ノ角ゴシック（以下、源ノフォント）を
Adobe-Japan1 （以下、AJ1）フォントになるように組み替えた
「原ノ味フォント（原ノ味明朝、原ノ味角ゴシック）」
を作ってみました。
CID の対応がとれないため抜けてしまうグリフがありますが、
素の pTeX / pLaTeX で和文フォントとして使う分には
ほぼすべてのグリフが揃っています。

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

その他、以下のファイルも配布しています。

* [
pTeX / pLaTeX 用マップファイル
](https://github.com/trueroad/HaranoAjiFonts-generator/tree/master/tex/map)
* [
各種 TeX 用テストファイル
](https://github.com/trueroad/HaranoAjiFonts-generator/tree/master/tex)

詳細は[
原ノ味フォント生成プログラム
](https://github.com/trueroad/HaranoAjiFonts-generator)
をご覧ください。

## 搭載グリフ

源ノフォントが搭載しているグリフ、かつ、
AJ1 への対応が取れたものを搭載します。

* 漢字
    + Adobe-Japan1-6 漢字グリフは以下の 1 グリフを除きすべて搭載
        + \<U+6CE8 U+E0102\> (AJ1 CID+12869) 「注」の異字体
    + JIS X 0208、JIS X 0213 の全漢字グリフを搭載
* 非漢字（ひらがな、カタカナ、英数字、記号類など）
    + JIS X 0208 横書きグリフはすべて搭載
        + JIS90 字形（CMap file `H` を使った場合）すべて搭載
        + JIS2004 字形（CMap file `2004-H` を使った場合）すべて搭載
    + JIS X 0208 縦書きグリフは以下の 4 グリフを除きすべて搭載
        + JIS90 字形（CMap file `V` を使った場合）
            + `‖` 01-34 U+2016 'DOUBLE VERTICAL LINE'
              (AJ1 CID+7895)
        + JIS2004 字形（CMap file `2004-V` を使った場合）
            + `‖` 01-34 U+2016 'DOUBLE VERTICAL LINE'
              (AJ1 CID+7895)
            + `°` 01-75 U+00B0 'DEGREE SIGN'
              (AJ1 CID+8269)
            + `′` 01-76 U+2032 'PRIME'
              (AJ1 CID+8273)
            + `″` 01-77 U+2033 'DOUBLE PRIME'
              (AJ1 CID+8283)
    + JIS X 0213 の非漢字グリフには抜けているものがあります。
    + その他 Adobe-Japan1-6 非漢字グリフには抜けているものがあります。

抜けているグリフのCIDにはダミーグリフ
（.notdef と同じで四角の中に×が入ったような形）が入っています。
上記で具体的に記載した非搭載グリフ（漢字 1 グリフ、非漢字縦書き 4 グリフ）は
いずれも源ノフォントが搭載していないため原ノ味フォントに搭載できないものです。
`H`, `V` は[
Adobe が配布する CMap file
](https://github.com/adobe-type-tools/cmap-resources)
で、TeX Live などにも含まれています。
`2004-H`, `2004-V` は[
Japanese TeX Development Community が配布する CMap file
（のようなもの）
](https://github.com/texjporg/jfontmaps/tree/master/cmap)
で、TeX Live にも含まれています。

## pTeX / pLaTeX

源ノフォントと異なり比較的簡単に使うことができます。
フォントファイルとマップファイルを適切に配置すれば普通に使えます。
ただし搭載しない（抜けている）グリフを使うことはできません。

* OTF パッケージを使わない場合
    + JIS90 字形（マップファイル `ptex-haranoaji.map` を使った場合）
        + 横書きは全グリフ使えます。
        + 縦書きは 1 グリフ `‖` だけ使えません。
    + JIS2004 字形（マップファイル `ptex-haranoaji-04.map` を使った場合）
        + 横書きは全グリフ使えます。
        + 縦書きは 4 グリフ `‖`, `°`, `′`, `″` 使えません。
* OTF パッケージを使う場合
    + Adobe-Japan1-6 全漢字グリフから 1 グリフを除き CID 直接指定などで
      呼び出すことができます。
        + AJ1 CID+12869 （「注」の異字体）だけ使えません。
    + 非漢字（ひらがな、カタカナ、英数字、記号類など）には
      使えないグリフもあります。

詳細は「搭載グリフ」も参照してください。

### ipsj.cls

ipsj.cls の場合は下記のマップファイル

```
rml	H	HaranoAjiMincho-Light.otf
gbm	H	HaranoAjiGothic-Regular.otf
futomin-b	H	HaranoAjiMincho-Regular.otf
futogo-b	H	HaranoAjiGothic-Medium.otf
```

を使い、クラスオプションから `submit` を外すと
[
本物っぽくなると思います
](https://twitter.com/trueroad_jp/status/1111612471763066880)
。

## 履歴

* [
20190501
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20190501)
    + フルセットフォント化
        - これまで AJ1 CID で抜けているグリフは欠番にする
          「サブセットフォント」にしていました。
          これをダミーグリフを入れることにより CID に欠番のない
          「フルセットフォント」にしました。
        - 通常の AJ1 フォントはフルセットフォントなのに対して、
          サブセットフォントだと一部挙動が異なるソフトウェアが
          あるようなのでフルセットに変えることにしました。
            - サブセットフォントだと CID ≠ GID になるのですが、
              これが原因で[
かなり特殊なことをしようとすると変になる
](https://twitter.com/trueroad_jp/status/1123484898386427904)
              ことがあるようです。普通に使う分には問題ありませんでした。
        - これまでは欠番 CID を使用しようとすると警告が出ていたような
          ツールでもフルセット化により警告が出なくなります。
          無警告でダミーグリフが使われることで
          意図しない結果になる恐れがあります。ご注意ください。
        - 原ノ味明朝は Adobe-Japan1-7 を名乗っていますが、
          CID+23058, CID+23059 が無いので実はサブセットフォントです。
          ただし、AJ1-6 の範囲は（ダミーを含めることで）すべて埋まっていて
          CID ＝ GID なので、これが原因で変になることはありません。
    + バージョンアップ
        - ttx 3.41.0
    + グリフ数
        - 変わってないはずですが、
          ダミーグリフの影響でグリフ数を数えるのが難しくなりました。。。
* [
20190413
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20190413)
    + Adobe-Japan1-7 に対応
        - `CFF` テーブルの ROS を Adobe-Japan1-7 に変更しました。
        - あわせて Adobe-Japan1-7 で追加されたグリフの GSUB 情報を
          使うようにしました。
    + 源ノ角ゴシック 2.001 に対応
        - ベースとなる源ノ角ゴシックを 2.000 から 2.001 に変更しました。
        - これにより「令和」の合字 (U+32FF) に対応、
          横書き (AJ1 CID+23058) 縦書き (AJ1 CID+23059) とも搭載。
            - 原ノ味角ゴシックのみです。
            - 原ノ味明朝も Adobe-Japan1-7 フォントになりましたが
              源ノ明朝が搭載しないため搭載していません。
        - 原ノ味角ゴシックのグリフ数は 1 グリフしか増えませんでした。
          これは源ノ角ゴシック 2.000 にはダミーのグリフが含まれており
          原ノ味角ゴシックにもダミーの横書きグリフが含まれていたためです。
          今回のバージョンアップで、横書きグリフはダミーから
          正式なグリフに変更になったためグリフ数が増加せず、
          縦書きは追加の GSUB 情報で紐づけができるようになり
          グリフ数が増加したものです。
    + バージョンアップ
        - 源ノ角ゴシック 2.001
        - ttx 3.40.0
    + グリフ数
        - 原ノ味明朝：16678
        - 原ノ味角ゴシック：16684

* [
20190324
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20190324)
    + 異字体セレクタ に対応
        - cmap format 14 を変換するようにしたため
          異字体セレクタを使うことができるようになりました。
    + OpenType feature に対応
        - `GDEF`, `GPOS`, `GSUB` を変換するようにしたため
          OpenType feature を使うことができるようになりました。
    + JIS X 0208 グリフに対応
        - JISX0208-SourceHan-Mapping.txt 2019-03-14
        - 元々この範囲のグリフには対応できていましたが、
          マッピングファイルを作っていただいたのでそれを使って
          生成するようにしました。
          本件によるグリフ数の増加や変更はありません。
    + [pTeX / pLaTeX 用マップファイルを配布
](https://github.com/trueroad/HaranoAjiFonts-generator/tree/20190324/tex/map)
        - [各種 TeX 用テストファイル
](https://github.com/trueroad/HaranoAjiFonts-generator/tree/20190324/tex)
          もあります。
    + バージョンアップ
        - ttx 3.39.0
    + グリフ数
        - 原ノ味明朝：16678
        - 原ノ味角ゴシック：16683

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
