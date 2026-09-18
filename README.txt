道路陥没 簡易計算 ― ホーム画面アプリ（PWA）の置き方

■ 中身
  index.html      本体（road_collapse_lite.html と同じ計算）
  manifest.json   アプリ名・アイコンの定義
  sw.js           オフライン用（一度開けば圏外でも動く）
  icon-*.png      アイコン

■ GitHub Pages に置く（推測できないURLにする）
 1. github.com にログイン → 右上「+」→ New repository
 2. Repository name に長いランダムな名前を付ける
    例: kanbotsu-7f3k9q2mzx8vb4nt   ← これがURLの一部になるので推測されにくい名前に
    Public を選ぶ（Pagesの無料枠はPublicのみ。リンクを張らなければ人目に触れない）
    「Add a README file」は付けない → Create repository
 3. 「uploading an existing file」をクリック → この5つのファイルをまとめてドラッグ → Commit changes
 4. Settings → Pages → Branch を「main」「/(root)」にして Save
 5. 1〜2分待つと上部に URL が出る
    https://ユーザー名.github.io/kanbotsu-7f3k9q2mzx8vb4nt/

■ スマホでアプリにする
 iPhone: Safari で URL を開く → 共有ボタン → 「ホーム画面に追加」
 Android: Chrome で URL を開く → メニュー → 「ホーム画面に追加」または「アプリをインストール」
 以後はアイコンから起動。一度開いていればオフラインでも動く。

■ 更新するとき
 GitHub で index.html を差し替えて Commit。sw.js の 'kanbotsu-v1' を 'v2' に変えると
 スマホ側のキャッシュが更新される。

■ 注意
 リポジトリ名を後で変えるとURLも変わり、ホーム画面のアイコンが開かなくなる。
