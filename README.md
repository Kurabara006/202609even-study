# 202609even-study

Even G2（Even Hub）向けプロトタイプ。公式 minimal テンプレート相当のタップカウンターです。

## セットアップ

```bash
npm install
```

## シミュレータで試す

```bash
# ターミナル 1
npm run dev

# ターミナル 2
npm run simulate
```

576×288 の緑キャンバスに表示されます。クリックでカウント、ダブルクリックで終了確認です。

## 実メガネ（QR sideload）

スマホと PC（または dev サーバー）が **同じネットワークから届く** URL を QR に入れます。

```bash
npm run dev
# 例: 手元 PC の LAN IP
npx evenhub qr --url "http://192.168.x.x:5173"
# QR を PNG に保存する場合
npx evenhub qr --url "http://192.168.x.x:5173" -e -s 8
```

Even Realities アプリの **Scan QR** で読み取ります。

クラウド VM 上で dev している場合は、ngrok 等で公開 URL を取り、`--url` にその URL を指定してください。

## パッケージ（.ehpk）

```bash
npm run pack
```

`even-study.ehpk` が生成されます。
