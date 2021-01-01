<!-- -*- coding: utf-8 -*- -->
# 原ノ味フォント / Harano Aji Fonts

[ Japanese （日本語） / [English](README.en.md) ]

源ノ明朝・源ノ角ゴシック（以下、源ノフォント）を
Adobe-Japan1 （以下、AJ1）フォントになるように組み替えた
「原ノ味フォント（原ノ味明朝、原ノ味角ゴシック）」
を作ってみました。
CID の対応がとれないため抜けてしまうグリフがありますが、
素の pTeX / pLaTeX で和文フォントとして使う分には
すべてのグリフが揃っています。

「原ノ味」というのは、
源ノフォントからグリフやテーブルが抜けていることを表すために
「氵（さんずい）」を取り、
AJ1 をもじって AJI にして
音から「味」という字をあてたものです。

## フォントファイルの配布

* 原ノ味フォントの配布
    - TeX Live
        - TeX Live 2020 以降に含まれており、
          （ごく一部のエンジンを除き）和文のデフォルトフォントになっています
        - TeX Live 2019 では 2020 年 2 月中旬以降の更新に含まれています
          （デフォルトフォントではありません）
    - W32TeX
        - 2020 年 3 月 23 日以降に含まれています
    - CTAN
        - 主要 7 フォント（各種 TeX 用プリセット設定で使うウェイト）
            - [
https://www.ctan.org/pkg/haranoaji
](https://www.ctan.org/pkg/haranoaji)
        - 追加 7 フォント（プリセットでは使わないウェイト）
            - [
https://www.ctan.org/pkg/haranoaji-extra
](https://www.ctan.org/pkg/haranoaji-extra)
    - GitHub
        - [
https://github.com/trueroad/HaranoAjiFonts
](https://github.com/trueroad/HaranoAjiFonts)

フォントファイルはサイズが大き目で、全 14 フォントあるため、
リポジトリの容量が大きくなりがちと考えており、
GitHub では古いバージョンのフォントは随時消していきたいと思っています。
そのため、新しいフォントをリリースする際には
master ブランチを forced update する運用にし、
余裕があるのであれば tag で古いフォントにアクセスできるように
しておくつもりです。

その他、以下のファイルも配布しています。

* [
各種 TeX ファイル
](https://github.com/trueroad/HaranoAjiFonts-generator/tree/master/tex)
    + ドキュメント、サンプル、テストファイルなど
* fontspec 用ファイル
    + [
HaranoAjiMincho.fontspec
](https://github.com/trueroad/HaranoAjiFonts-generator/tree/master/tex/HaranoAjiMincho.fontspec),
      [
HaranoAjiGothic.fontspec
](https://github.com/trueroad/HaranoAjiFonts-generator/tree/master/tex/HaranoAjiGothic.fontspec)
    + `luatexja-preset` などのプリセット設定を使う場合は不要です

pTeX / pLaTeX 用マップファイルは
[ptex-fontmaps](https://www.ctan.org/pkg/ptex-fontmaps)
20200217.0 以降に入っています。

**実験的**に生成した中国語簡体字、中国語繁体字、韓国語フォントがあります。

* （実験的）中国語簡体字 (CN)：Adobe-GB1 対応
    + [
https://github.com/trueroad/HaranoAjiFontsCN
](https://github.com/trueroad/HaranoAjiFontsCN)
* （実験的）中国語繁体字 (TW)：Adobe-CNS1 対応
    + [
https://github.com/trueroad/HaranoAjiFontsTW
](https://github.com/trueroad/HaranoAjiFontsTW)
* （実験的）韓国語 (KR)：Adobe-KR 対応
    + [
https://github.com/trueroad/HaranoAjiFontsKR
](https://github.com/trueroad/HaranoAjiFontsKR)
* （実験的）韓国語 (K1)：Adobe-Korea1 対応
    + [
https://github.com/trueroad/HaranoAjiFontsK1
](https://github.com/trueroad/HaranoAjiFontsK1)

詳細は[
原ノ味フォント生成プログラム
](https://github.com/trueroad/HaranoAjiFonts-generator)
をご覧ください。

## 搭載グリフ

源ノフォントが搭載しているグリフ、かつ、
AJ1 への対応が取れたものを搭載します。

* 漢字
    + Adobe-Japan1-6 漢字グリフはすべて搭載
        + \<U+6CE8 U+E0102\> (AJ1 CID+12869) ルビ用の「注」は非搭載
            + これは AJ1 の「漢字グリフ」範囲外で漢字扱いではありません。
    + JIS X 0208、JIS X 0213 の全漢字グリフを搭載
* 非漢字（ひらがな、カタカナ、英数字、記号類など）
    + JIS X 0208 横書きグリフすべて搭載
    + JIS X 0208 縦書きグリフすべて搭載（20200418 版以降）
    + JIS X 0213 の非漢字グリフには抜けているものがあります。
    + その他 Adobe-Japan1-6 非漢字グリフには抜けているものがあります。

非漢字のうち、かなグリフ（ひらがな、カタカナ）は以下のようになっています。
分類は AJ1-7 によります。
全角とプロポーショナルで搭載していない
小書き「こ」と小書き「コ」は源ノフォントに存在せず、
加工元にできるグリフがありません。

* 半角かな
    + 横組み用
        - 濁点・半濁点のつかないカタカナなどを搭載
        - ひらがな、濁点・半濁点付きなどは非搭載
    + 縦組み用
        - すべて非搭載
* （通常の）全角かな
    + 横組み用
        - 2 グリフのみ非搭載（小書き「こ」小書き「コ」）
        - 他はすべて搭載
        - 源ノの横組み用かなを割り当てている
        - 注：AJ1 の「（通常の）全角かな横組み用」は小書き等を除き縦横両用
    + 縦組み用
        - 2 グリフのみ非搭載（小書き「こ」小書き「コ」）
        - 他はすべて搭載
        - 源ノの縦組み用かなを割り当てている
        - 注：AJ1 の「（通常の）全角かな縦組み用」は
          小書き等の横組み用ではマズい一部のグリフのみが存在し、
          それ以外は「（通常の）全角かな横組み用」を使うようになっている
* 組方向ごとに最適化した全角かな
    + 横組み用（20210101 版以降）
        - 2 グリフのみ非搭載（小書き「こ」小書き「コ」）
        - 他はすべて搭載
        - 源ノの横組み用かなを割り当てている
        - そのため「（通常の）全角かな横組み用」と同じグリフを搭載
    + 縦組み用（20210101 版以降）
        - 2 グリフのみ非搭載（小書き「こ」小書き「コ」）
        - 他はすべて搭載
        - 源ノの縦組み用かなを割り当てている
        - そのため、小書き等の「（通常の）全角かな縦組み用」に
          存在するもののみ同じグリフを搭載、それ以外は別グリフを搭載
* プロポーショナルかな
    + 横組み用（20210101 版以降、一部は 20200524 版以降）
        - 2 グリフのみ非搭載（小書き「こ」小書き「コ」）
        - 他はすべて搭載
        - 源ノの横組み用かなで palt があるものは加工し、
          ないものはそのまま搭載
    + 縦組み用（20210101 版以降）
        - 2 グリフのみ非搭載（小書き「こ」小書き「コ」）
        - 他はすべて搭載
        - 源ノの縦組み用かなで vpal があるものは加工し、
          ないものはそのまま搭載
        - 注：LuaTeX でも XeTeX でもうまく扱えないようで動作確認未
* ルビかな
    + 横組み用
        - すべて非搭載
    + 縦組み用
        - すべて非搭載
* U-PRESSかな
    + 横組み用
        - すべて非搭載

以下の縦書きグリフは、横書きグリフを加工したものを搭載しています
（20200418 版以降）。

* `‖` AJ1 CID+7895 U+2016 'DOUBLE VERTICAL LINE'
    + AJ1 CID+666 を右90度回転
* `°` AJ1 CID+8269 U+00B0 'DEGREE SIGN'
    + AJ1 CID+707 を平行移動
* `′` AJ1 CID+8273 U+2032 'PRIME'
    + AJ1 CID+708 を平行移動
* `″` AJ1 CID+8283 U+2033 'DOUBLE PRIME'
    + AJ1 CID+709 を平行移動
* `✂` AJ1 CID+12178 U+2702 'BLACK SCISSORS'
    + AJ1 CID+12176 を右90度回転

抜けているグリフのCIDにはダミーグリフ
（.notdef と同じで四角の中に×が入ったような形）が入っています。
そのほとんどは
源ノフォントが搭載していないため原ノ味フォントに搭載できないものです。

非漢字の搭載グリフの一部で、
源ノフォントの文字幅が AJ1 の文字幅に合わなくて、
強制的に AJ1 に合わせたものがあります（20190824 版以降）。
AJ1 でプロポーショナル幅とされているグリフは変更していません。
さらに、単純に幅を上書きするだけでなく、
グリフによって中央寄せなどの位置調整を行いました（20200215 版以降）。
このため、幅が広くなったグリフは隙間ができたり、
幅が狭くなったグリフは左右がはみ出て前後の文字と重なるなどの現象が発生したり、
不格好な表示になることがあります。
とはいえ、幅としては正しくなっているため、
後続文字の位置がズレるなどといった、組版への影響は発生しません。
以下に該当のグリフを示します。

+ ギリシャ文字
+ キリル文字
+ `¨` AJ1 CID+647 U+00A8 'DIAERESIS'
+ `°` AJ1 CID+707 U+00B0 'DEGREE SIGN'
+ `´` AJ1 CID+645 U+00B4 'ACUTE ACCENT'
+ `′` AJ1 CID+708 U+2032 'PRIME'
+ `″` AJ1 CID+709 U+2033 'DOUBLE PRIME'
+ `‼` AJ1 CID+12111 U+203C 'DOUBLE EXCLAMATION MARK'
+ `⁇` AJ1 CID+16278 U+2047 'DOUBLE QUESTION MARK'
+ `⁈` AJ1 CID+16279 U+2048 'QUESTION EXCLAMATION MARK'
+ `⁉` AJ1 CID+12112 U+2049 'EXCLAMATION QUESTION MARK'
+ `ℓ` AJ1 CID+8025 U+2113 'SCRIPT SMALL L'
+ `№` AJ1 CID+7610 U+2116 'NUMERO SIGN'
+ `−` AJ1 CID+693 U+2212 'MINUS SIGN'
+ `✓` AJ1 CID+16270 U+2713 'CHECK MARK'

以下については、源ノフォントでは幅がゼロの合成用グリフですが、
AJ1 で全角幅の CID に割り当たったため、
幅を全角幅で上書きし（20190824 版以降）位置調整をし（20200215 版以降）
他の AJ1 フォントと同じような位置になるよう再調整しました（20200418 版以降）。
そのため、不格好な表示になることがあります。

+ AJ1 CID+16328 U+20DD 'COMBINING ENCLOSING CIRCLE'
+ AJ1 CID+11035 U+20DE 'COMBINING ENCLOSING SQUARE'
    + CID+11035 は、
      原ノ味角ゴシックのみ幅ゼロの合成用グリフが割り当たったため
      全角幅で上書きおよび位置調整を実施し、
      原ノ味明朝は全角幅グリフが割り当たったため
      幅上書きや位置調整をしていません
+ AJ1 CID+16326 U+3099 'COMBINING KATAKANA-HIRAGANA VOICED SOUND MARK'
+ AJ1 CID+16327 U+309A 'COMBINING KATAKANA-HIRAGANA SEMI-VOICED SOUND MARK'

原ノ味フォント 20200524 からプロポーショナルかなを搭載しています。
源ノフォントの palt に従って幅と位置を調整したものです。
原ノ味フォント 20210101 からプロポーショナルかな縦組み用を搭載しています。
源ノフォントの vpal に従って高さと位置を調整したものです。
なお、プロポーショナルかな縦組み用は LuaTeX でも XeTeX でも
うまく扱うことができなかったため、動作確認ができていません。

原ノ味フォント 20210101 から AJ1 「組方向ごとに最適化した全角かな」
を搭載しています。
源ノフォントは、
全角かなには横組み用と縦組み用で別々のグリフが用意されていますが、
AJ1 のような「（通常の）全角かな」と「組方向ごとに最適化した全角かな」
の区別はありません。そこで、源ノの横組み用を
「（通常の）全角かな横組み用」と「組方向ごとに最適化した全角かな横組み用」に、
源ノの縦組み用を
「（通常の）全角かな縦組み用」と「組方向ごとに最適化した全角かな縦組み用」に、
それぞれ割り当てました。

また、ダミーグリフは全角幅ですが、
これも AJ1 の文字幅で上書きしています。

## pTeX / pLaTeX

源ノフォントと異なり比較的簡単に使うことができます。
TeX Live 2020 以降ではデフォルトフォントになっているので、
何もしなくてもそのままで使えます。
ただし搭載しない（抜けている）グリフを使うことはできません。

* OTF パッケージを使わない場合
    + JIS90 字形 / JIS2004 字形、横書き / 縦書き、
      いずれの組み合わせでも全グリフ使えます（20200418 版以降）。
* OTF パッケージを使う場合
    + Adobe-Japan1-6 全漢字グリフから CID 直接指定などで
      呼び出すことができます。
        + AJ1 CID+12869 （ルビ用の「注」）は使えません。
    + 非漢字（ひらがな、カタカナ、英数字、記号類など）には
      使えないグリフもあります。

詳細は「搭載グリフ」も参照してください。

TeX Live をお使いの場合、
[ptex-fontmaps](https://www.ctan.org/pkg/ptex-fontmaps)
が 20200217.0 以降になっていて sudo で管理者権限が使えるなら、

```
$ sudo kanji-config-updmap-sys --jis2004 haranoaji
```

のようにすることで原ノ味フォントに切り替わります。

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
20210101
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20210101)
(JP, CN, TW, KR, K1)
    + 源ノ角ゴシック 2.002 に対応 (JP, CN, TW, KR, K1)
        - ベースとなる源ノ角ゴシックを 2.001 から 2.002 に変更しました。
    + かなグリフを大幅強化 (JP)
        - AJ1-7 「組方向ごとに最適化した全角かな横組み用」グリフの
          大部分となる 211 グリフを搭載しました（非搭載は 2 グリフ）。
          これはすべて通常の全角かな横組み用と同じもので、
          今回新たに搭載したものです。
        - AJ1-7 「組方向ごとに最適化した全角かな縦組み用」グリフの
          大部分となる 211 グリフを搭載しました（非搭載は 2 グリフ）。
          これは、源ノが持っている全角かな縦組み用グリフで、
          これまで原ノ味のグリフに割り当てていなかった 169 グリフ
          を今回新たに割り当てました。
          残り 42 グリフは、
          通常の全角かな縦組み用と同じグリフを今回新たに搭載しました。
        - AJ1-7 「プロポーショナルかな横組み用」グリフの
          大部分となる 213 グリフを搭載しました（非搭載は 2 グリフ）。
          これまで、palt を持つ全角グリフについて palt で幅と横位置を加工して
          プロポーショナルなグリフとして搭載していました。
          また、palt を持たない全角グリフでも、
          同じ CID が別のウェイトで palt を持っていれば、
          全角と同じグリフをプロポーショナルとして搭載していました。
          しかし、全ウェイトで palt を持たない
          全角かな横組み用グリフが 15 あったため、
          これらについても同じグリフを今回新たに搭載しました。
        - AJ1-7 「プロポーショナルかな縦組み用」グリフの
          大部分となる 213 グリフを搭載しました（非搭載は 2 グリフ）。
          これは、横組み用と同様に vpal を持つ全角グリフについて
          vpal で高さと縦位置を加工して
          プロポーショナルなグリフとして今回新たに搭載しました。
          また、vpal を持たない全角グリフについても
          プロポーショナルかな縦組みに紐づけられるものは
          全角と同じグリフをプロポーショナルとして今回新たに搭載しました。
          両方あわせて 213 グリフです。
    + GSUB による OpenType feature 対応を強化 (JP)
        - expt, hojo, trad を追加しました。AJ1-7 の GSUB と同内容です。
        - pkna, hkna, vkna を追加しました。AJ1-7 の GSUB とほぼ同内容
          （欠けているものがあるのでサブセット）です。
        - vert に「プロポーショナルかな縦組み用」を追加しました。
          追加したのは AJ1-7 の GSUB とほぼ同内容
          （欠けているものがあるのでサブセット）です。
          先に pwid または pkna を適用してから vert を適用することで
          「プロポーショナルかな縦組み用」グリフが選択できます
          （これは AJ1-7 GSUB と同じです）。
          また、OpenType 規格で GSUB feature は Lookup テーブルの順番で
          適用することになっており、それにあわせ pwid や pkna が
          vert より先にくるようにしています
          （これも AJ1-7 GSUB と同じです）。
        - Issue [縦組み 「：」が倒れていない
          ](https://github.com/trueroad/HaranoAjiFonts/issues/6)
          に対応しました。
          源ノの vert には複数のテーブルがあり、
          そのうちの 1 つだけが vrt2 に入っているため、
          vrt2 が vert のサブセットになっていました。
          OpenType 規格的にはサブセットではマズいのですが、
          vrt2 は単一テーブルでなければならないという制約があること、
          vrt2 が無いと一部アプリの縦組みで問題が発生することから、
          妥協してわざと規格に反する状態にしているようでした
          （詳細はリンク先の Issue や、そこからリンクが張られている源ノの
          Issue を参照してください）。
          そこで原ノ味では、複数の vert テーブルを 1 つに統合し、
          vrt2 が vert と同じ内容になるようにしました。
    + バージョンアップ
        + 源ノ角ゴシック 2.002
        + ttx 4.18.2
    + グリフ数 (JP)
        + 原ノ味明朝：17554
          （変換 16862 ＋グリフ加工 691 ＋ .notdef 1）
        + 原ノ味角ゴシック：17559
          （変換 16867 ＋グリフ加工 691 ＋ .notdef 1）
        + 上記により、変換 169 グリフ、加工 481 グリフ、
          計 650 グリフ増加しています
* [
20200912
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20200912)
(JP)
    + [
小書きの「プ」
](https://twitter.com/zr_tex8r/status/1303694108465135616)、
半濁点のか行、カ行、「セ」、「ツ」、「ト」のグリフを追加しました
        + 小書きの「プ」は、縦書き用と pwid （加工）も追加しています
        + これは[単独の Unicode コードポイントを持たず、
リガチャ置き換えのみでアクセス可能な
CID](https://twitter.com/trueroad_jp/status/1304001557822730241)
の変換に対応したことによるものです
        + この対応で JP 以外はグリフ変更ありませんでした
    + バージョンアップ
        + ttx 4.14.0
    + グリフ数 (JP)
        + 原ノ味明朝：16904
          （変換 16693 ＋グリフ加工 210 ＋ .notdef 1）
        + 原ノ味角ゴシック：16909
          （変換 16698 ＋グリフ加工 210 ＋ .notdef 1）
        + 上記により、変換 15 グリフ、加工 1 グリフ、
          計 16 グリフ増加しています
* [
20200612
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20200612)
(JP, CN, TW, KR, K1)
    + `cmap` テーブルが AJ1 などの CMap と比較して不足しているところを追加、
      食い違っていたところを修正しました
      (JP, CN, TW, KR, K1)
        + これにより `cmap` テーブルに U+FF0D 'FULLWIDTH HYPHEN-MINUS'
          が搭載されていない[
問題
](https://github.com/trueroad/HaranoAjiFonts/issues/4)が修正されました
        + これまでと同じくグリフを搭載していない（ダミーグリフの）
          CID に紐づく Unicode コードポイントは `cmap` に搭載していません
    + AJ1 CID+151 を AJ1 CID+14 からのコピーで追加しました (JP)
    + `cmap` テーブル format 4 がサイズ制限を超える場合の対策を変更しました
      (TW, KR)
    + `GPOS` テーブルを搭載しました (KR)
    + 生成プログラムの改良をしました
        + 各フォントの生成をシェルスクリプトから make に変更しました
        + ビルドディレクトリ、ログファイル、中間ファイルの名称を変更しました
    + バージョンアップ
        + ttx 4.12.0
    + グリフ数 (JP)
        + 原ノ味明朝：16888
          （変換 16678 ＋グリフ加工 209 ＋ .notdef 1）
        + 原ノ味角ゴシック：16893
          （変換 16683 ＋グリフ加工 209 ＋ .notdef 1）
        + 上記 1 グリフ追加に伴い増加しています
* [
20200524
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20200524)
(JP, CN, TW, KR, K1)
    + プロポーショナルかなのグリフを追加しました (JP)
    + 一部のスペースグリフを追加しました (JP, KR)
    + palt などの `GPOS` テーブルが壊れていたのを修正しました (JP, CN, TW, KR)
    + **実験的な**韓国語フォントで Monospaced グリフの幅を変更しました (KR)
    + **実験的に**韓国語フォントのバリエーションを追加しました (K1)
    + これまで Adobe-KR 対応でサフィックス KR のフォントがありましたが、
      Adobe-Korea1 対応でサフィックス K1 のフォントを追加しました
        + 韓国語：Adobe-Korea1 対応、サフィックス K1
            + UniKS-UTF32-H 1.008
    + バージョンアップ
        - ttx 4.10.2
    + グリフ数 (JP)
        - 原ノ味明朝：16887
          （変換 16678 ＋グリフ加工 208 ＋ .notdef 1）
        - 原ノ味角ゴシック：16892
          （変換 16683 ＋グリフ加工 208 ＋ .notdef 1）
* 20200516 (CN, TW, KR)
    + **実験的に**中国語簡体字、中国語繁体字、韓国語フォントを
      生成できるようにしました
    + 各言語版のフォント名は、サフィックスにベースとした源ノフォントと同じ
      アルファベット 2 文字を付けています
        + 中国語簡体字：Adobe-GB1 対応、サフィックス CN
            + UniGB-UTF32-H 1.016
        + 中国語繁体字：Adobe-CNS1 対応、サフィックス TW
            + UniCNS-UTF32-H 1.019
        + 韓国語：Adobe-KR 対応、サフィックス KR
            + UniAKR-UTF32-H 1.002
    + 日本語は変更なし、今回のリリースもありません
    + 今後は各言語版の略称にサフィックスを使います
        + 日本語版はフォント名にサフィックスありませんが略称 JP とします
    + バージョンアップ
        - ttx 4.10.0
* [
20200418
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20200418)
    + 縦書き用 5 グリフを追加しました
        + 素の pTeX で使用できるすべてのグリフが揃いました
        + いずれも横書き用のグリフを加工（右90度回転または平行移動）
          したものです
            + `‖` AJ1 CID+7895 U+2016 'DOUBLE VERTICAL LINE'
            + `°` AJ1 CID+8269 U+00B0 'DEGREE SIGN'
            + `′` AJ1 CID+8273 U+2032 'PRIME'
            + `″` AJ1 CID+8283 U+2033 'DOUBLE PRIME'
            + `✂` AJ1 CID+12178 U+2702 'BLACK SCISSORS'
    + ファイルサイズを低減しました
        + 14フォント合計で 79.1 MBから 72.3 MB になり 6.8 MB （約 9 %）減
        + CharString でダミーグリフを展開せず、
          サブルーチン呼び出しに変更したことによります
    + 2グリフの描画位置を再調整しました
        + 20200215 版では位置調整の結果ボックス内右上隅に寄っていましたが、
          他の AJ1 フォントではボックス内左上隅に寄っていたため再調整しました
            + AJ1 CID+16326 U+3099
              'COMBINING KATAKANA-HIRAGANA VOICED SOUND MARK'
            + AJ1 CID+16327 U+309A
              'COMBINING KATAKANA-HIRAGANA SEMI-VOICED SOUND MARK'
    + 位置調整したグリフの LSB （左サイドベアリング）を修正しました
        + 20200215 版では、位置調整したグリフについて `hmtx` テーブルの
          LSB も修正すべきでしたが、していませんでした
        + 平行移動や回転したグリフも合わせて LSB と
          `vmtx` テーブルの TSB （上サイドベアリング）
          を計算して修正するようにしました
    + 幅上書き・位置調整したグリフを `GPOS` テーブルから取り除きました
        + 20190824 版で幅上書き、20200215 版で位置調整したグリフが、
          `GPOS` テーブルに上書き・調整前のパラメータのまま残っていたため、
          OpenType feature の指定によっては位置がおかしくなることがありました
        + `GPOS` テーブルから削除したので問題なくなりました
    + バージョンアップ
        - ttx 4.7.0
    + グリフ数
        - 原ノ味明朝：16684
        - 原ノ味角ゴシック：16689
        - 上記 5 グリフ追加に伴い増加しています
* [
20200215
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20200215)
    + 横幅を上書きしたグリフについて、中央揃えにするなどの位置調整をしました
        + [@h20y6m](https://github.com/h20y6m) さんの
          [#2](https://github.com/trueroad/HaranoAjiFonts-generator/issues/2),
          [#3](https://github.com/trueroad/HaranoAjiFonts-generator/pull/3)
          によるものです
            - Python3 が必要になります
    + バージョンアップ
        - ttx 4.3.0, UniJIS2004-UTF32-H 1.021
            - 前の 20190824 では UniJIS2004-UTF32-H のバージョンが
              1.020 のまま変わっていない状態でビルドしていました
            - UniJIS2004-UTF32-H 1.020 から 1.021 への変更により、
              原ノ味明朝では AJ1 CID+127 が増え、
              原ノ味角ゴシックでは AJ1 CID+127 が紐づくグリフが変更
              （AI0 CID+253 から AI0 CID+247）になっています
    + グリフ数
        - 原ノ味明朝：16679
        - 原ノ味角ゴシック：16684
        - 上記 UniJIS2004-UTF32-H のアップデートに伴い、
          原ノ味明朝で 1 グリフ増えています
* [
20190824
](https://github.com/trueroad/HaranoAjiFonts/releases/tag/20190824)
    + グリフの横幅を AJ1 の定義に従うようにしました
        + これまで一部のグリフで AJ1 の横幅と食い違っているものがあり、
          [
後続文字の位置がズレて組版結果がおかしくなる
](https://twitter.com/trueroad_jp/status/1164525246319251456)
          ことがありました。
        + 単純に横幅を上書きしただけなので、
          該当のグリフを使うと、左に寄って表示されたり、
          前後の文字に重なったり、不格好な表示になることがありますが、
          他のグリフの位置には影響を及ぼさなくなっているハズです。
    + AJ1-7 の GSUB 情報
        + AJ1-7 の GSUB 情報が公開されたので、
          それを利用するようにしました。
    + バージョンアップ
        - ttx 4.0.0, ~~UniJIS2004-UTF32-H 1.021~~
            - UniJIS2004-UTF32-H は 1.020 のままでした（20200215 追記）
    + グリフ数
        - 原ノ味明朝：16678
        - 原ノ味角ゴシック：16684
        - カウント方法を変更しましたが、数は同じです。
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

Copyright (C) 2019-2021
Masamichi Hosoda, with Reserved Font Name 'Harano Aji'.

Copyright 2014-2020 Adobe (http://www.adobe.com/),
with Reserved Font Name 'Source'.

Copyright 2017 Adobe Systems Incorporated (http://www.adobe.com/),
with Reserved Font Name 'Source'.

Source is a trademark of Adobe in the United States and/or other countries.

This Font Software is licensed under the SIL Open Font License, Version 1.1.
See [LICENSE](LICENSE).

原ノ味フォントは源ノフォントの派生フォントになるため
SIL Open Font License 1.1 です。
