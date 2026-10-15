# 作業署名アプリ デモ（PWA）

このフォルダをそのまま HTTPS のサーバーに置けば動きます（GitHub Pages、Netlify、社内Webサーバーなど）。
Service Worker は HTTPS（または localhost）でないと動きません。

- ローカル確認: `python3 -m http.server 8080` → http://localhost:8080/
- iPad: Safari で開く → 共有 → 「ホーム画面に追加」。ホーム画面から起動すると枠なしの全画面で表示されます。
- 一度開けばオフラインでも起動できます。データは端末のブラウザ内（localStorage）に保存されます。
- PC で全画面表示を試すときは `index.html?app=1` を開きます。
- ファイルを更新したら `sw.js` の `VERSION` を上げてください（古いキャッシュが入れ替わります）。
