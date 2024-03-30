# Template-Master(v01.03.02)
新しいサイトの制作を行う場合、こちらのディレクトリを複製してからWEB開発を行うこと。
テンプレート化することで、安定したクオリティーのWEBサイトを制作できる。
* アップデート内容
> テンプレートサイトのCMS化を考慮し、「Imagesフォルダ」の構造を見直した。
> コンテンツタイトルの下線部のボーダー色を調節できるように変更した。.c-contents_titleクラスと一緒に.-b-btmクラスを使う事でボーダーを付与できる。また、同じく.-c01や.-c02などを指定するとそれに対応した色に変化する。
> 「fontフォルダ」の構造を見直した。

## directory
* SCSSディレクトリ構成は、下記の通り。
* サイト制作を行う際には、まずvscordの拡張機能から『Live Sass Compiler』をインストール。
* その後、setting.jsonでpassを設定して、必ず「プロジェクトのルートディレクトリ」からVsCordを開く。
* SassCompilerを起動。（成功すると、Cssディレクトリが自動生成される。）



```
プロジェクトディレクトリ
      |
      |-- Images
      |     |---- f-view（各ページ > ファーストビュー）
      |     |---- item（アイテム関係）
      |     |---- logo（ロゴ関係）------------ SVG （支店ロゴ）
      |     |
      |     |---- pic (写真関係) ------------- top             New
      |     |        |----------------------- concept         New
      |     |        |----------------------- layout          New
      |     |        |----------------------- build           New
      |     |        |----------------------- plan            New
      |     |        |----------------------- equipment       New
      |     |        |----------------------- location        New
      |     |        |----------------------- quality         New
      |     |
      |     |---- slider (スライダー関係)
      |     |        |----------------------- top             New
      |     |        |----------------------- concept         New
      |     |        |----------------------- layout          New
      |     |        |----------------------- build           New
      |     |        |----------------------- plan            New
      |     |        |----------------------- equipment       New
      |     |        |----------------------- location        New
      |     |        |----------------------- quality         New
      |     |
      |     |---- sns (サイト外の表示関係)
      |     |---- SVG（描画のクオリティが求められるもの&テキストのみ）
      |     |
      |     |---- tab (タブ関係)
      |     |        |----------------------- top             New
      |     |        |----------------------- concept         New
      |     |        |----------------------- layout          New
      |     |        |----------------------- build           New
      |     |        |----------------------- plan            New
      |     |        |----------------------- equipment       New
      |     |        |----------------------- location        New
      |     |        |----------------------- quality         New
      |
      |-- js ---- swiper.min.js     (スライダー)
      |     |----- micromodal.min.js (物件概要用ポップアップ)
      |     |----- luminous.min.js   (画像表示用ポップアップ)
      |
      |-- scss -- style.scss(まとめ)
            |
            |---- setting(基本設定) ---------- _color.scss      (色)
            |        |----------------------- _gap.scss        (間隔)
            |        |----------------------- _reset.scss      (リセットCSS)
            |        |----------------------- _structure.scss  (横幅)
            |        |----------------------- _typography.scss (テキスト)
            |
            |---- components(各パーツ) ------- _common.scss   (共有)
            |        |----------------------- _header.scss   (ヘッダー)
            |        |----------------------- _footer.scss   (フッター)
            |        |----------------------- _nav.scss      (ナビゲーション)
            |        |----------------------- _title.scss    (タイトル)
            |        |----------------------- _contents.scss (コンテンツ)
            |        |----------------------- _flex.scss     (フレックス)
            |        |----------------------- _banner.scss   (バナー)
            |        |----------------------- _btn.scss      (ボタン)
            |        |----------------------- _contact.scss  (お問い合わせ)
            |        |----------------------- _link.scss     (リンク先)
            |        |----------------------- _tab.scss      (タブ)
            |        |----------------------- _modal.scss    (micromodal関係 > オリジナル)
            |        |----------------------- _popup.scss    (luminous関係 > オリジナル)
            |        |----------------------- _slider.scss   (swiper関係 > オリジナル)
            |        |----------------------- _video.scss    (動画)
            |        |----------------------- _tab.scss      (タブ)
            |        |----------------------- _dropmenu.scss (ドロップメニュー)
            |
            |---- introduction(外部ソース) --- _swiper.min.scss   (スライダー)
            |        |----------------------- _luminous.min.scss (画像＋キャプション用ポップアップ)
            |        |----------------------- 未定
            |        |----------------------- 未定
            |        |----------------------- 未定
            |        |----------------------- 未定
            |
            |---- page(各ページ独自) --------- _top.scss       (トップページ)
            |        |----------------------- _concept.scss   (コンセプトページ)
            |        |----------------------- _layout.scss    (区画図・間取りページ)
            |        |----------------------- _build.scss     (新築分譲ページ)　New
            |        |----------------------- _plan.scss      (参考プランページ)
            |        |----------------------- _equipment.scss (設備・仕様ページ)
            |        |----------------------- _location.scss  (周辺環境ページ)
            |        |----------------------- _quality.scss   (住協の家づくりページ)
            |        |----------------------- _overview.scss  (物件概要ページ)
            |
            |---- animation(アニメーション) --- _common.scss   (共通)
                     |------------------------ _color.scss    (「カラー」アニメーション)
                     |------------------------ _fade.scss     (「フェード」アニメーション)
                     |------------------------ _flip.scss     (「めくり」アニメーション)
                     |------------------------ _img.scss      (「画像」アニメーション)
                     |------------------------ _move.scss     (「動作」アニメーション)
                     |------------------------ _original.scss (「オリジナル」アニメーション)
                     |------------------------ _scroll.scss   (「スクロール」アニメーション)
                     |------------------------ _slide.scss    (「スライド」アニメーション)
                     |------------------------ _zoom.scss     (「拡大」アニメーション)
```

## 内容

1. TOP
* メインキャッチコピー
* ビジュアルイメージ（スライダー）

2. CONCEPT
* ビジュアルイメージ
* サブキャッチコピー
* コンセプト文

3. LAYOUT
* 区画図
* 外構仕様
* 間取り図

4. BUILD　New
* 新築分譲住宅
* 各号棟の紹介
* 外観写真スライダー（画像表示:ポップアップ＋スライダー）
* 内観写真スライダー（画像表示:ポップアップ＋スライダー）

5. PLAN
* 参考プラン
* 内装仕様
* 建築プラン例の紹介
* 施工例スライダー（画像表示:ポップアップ＋スライダー）

6. EQUIPMENT（設備・仕様）
* 設備
* 特別仕様

7. LOCATION
* 地域紹介
* おすすめスポット紹介
* 周辺環境
* アクセス
* 各LPへの誘導リンク

8. QUALITY（外部リンク）

9. OVERVIEW（物件概要:ポップアップ）

10. video
* 動画コンテンツ


## Rule
* 自身のGithubアカウントで『Create a new repository』からプロジェクトを作成し、
  ローカルにCloneしてから開発開始すること。
* Scssを使用して、Cssへのコンパイルを行うこと。
* コンパイルには、『Live Sass Compiler』を使うこと。
* 設定 > setting.jsonを編集 → "liveSassCompile.settings.formats"内のパスを合わせること。
* 本番環境にデプロイするまでのFlowを守ること。

#### 〈 デプロイまでのFlow 〉
1. Githubで『Create a new repository』からプロジェクトを作成。
2. Github Desktopからローカル環境にCloneする。（例： C:user/ユーザー/desktop/htdocs）
3. 開発終了後は、まず社内サーバーにUPして、支店担当者にて確認。
4. 確認後、社内サーバーにupしたデータを本番環境にデプロイする。
5. 本番環境から落とす際は、社内サーバー内の『■終了---一次保管』ディレクトリにデータを移すこと。
6. 極力アニメーションに関しては、外部ソースを流用せず自作で使用してください。(Jsとの兼ね合いでうまく表示されない可能性があるので)
7. 基本的に脱JQueryとする。
* カルーセルは『Swiper.js』のみ。
* モーダルは『Micromodal.js（iframe）』と『luminous.js（画像表示）』の2種類。


## Note
* Cssコーディングには「Scss」を用いているため、コンパイルできる環境が必須となる。（VsCordの拡張機能である「Live Sass Compiler」を推奨する。）
* 仮想サーバーを使用すると、「 Global site tag (gtag.js) - Google Analytics」の影響でエラーが発生してしまうので、更新のタイミングで「Ctrl + r」でリロード確認をすること。

## 各支店情報
* 入間支店　　　0120-38-6651
* 大泉支店　　　0120-07-6566
* 飯能支店　　　0120-74-5900
* 小手指支店　　0120-29-8815
* 東久留米支店　0120-569-888
* 狭山支店　　　0120-59-3611
* 新所沢支店　　0120-28-7311
* 川越支店　　　0120-38-0041
* ふじみ野支店　0120-53-2277
* 朝霞台支店　　0120-64-1200

## ベーシック認証
* Ryot21
* passwd

## Author
* 作成者：前田 龍汰
* 所属　：広報部
* E-mail：maeda-r@jyukyo.com
