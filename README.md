# ろぼくんアドオン配布部屋

ろぼくんが作ったマイクラ統合版アドオンを配布するサイトです。
GitHub Pages で公開しています。

## アドオンを追加するには（かんたん：管理ページ）

`https://robokun60-del.github.io/Japan-addon/admin.html` を開くと、名前とファイルを選んで「公開する」を押すだけで追加できます（100MB まで）。
削除もそのページからできます。最初の1回だけ、ページの下に書いてある手順でトークンを作って貼り付けてください。

## アドオンを追加するには（手動）

GitHub のサイト上でもできます（ブラウザからのアップロードは 25MB まで）。

### 1. ファイルをアップロードする

1. リポジトリの `addons` フォルダを開く
2. 「Add file」→「Upload files」を押す
3. `.mcaddon` か `.mcpack` のファイルをドラッグして、「Commit changes」を押す

スクリーンショットがあるなら、同じように `images` フォルダにアップロードします（`.png` や `.jpg`）。

> ファイル名は **英語・数字・`-`** にしておくと安全です（例: `japan-village.mcaddon`）。
> 1ファイルの大きさは 100MB までです。

### 2. `addons.json` に書き足す

`addons.json` を開いて、えんぴつマーク（Edit）を押し、こんなふうに書きます。

```json
[
  {
    "name": "日本セット",
    "description": "日本の建物やブロックを追加します。",
    "tag": "建築",
    "version": "1.0.0",
    "minecraft": "1.21",
    "updated": "2026-11-27",
    "file": "addons/japan-set.mcaddon",
    "image": "images/japan-set.png"
  }
]
```

2つ目からは `}` のあとに `,` を付けて、`{ ... }` をもう1つ足します。

| 項目 | 必須 | 意味 |
| --- | --- | --- |
| `name` | ○ | アドオンの名前 |
| `file` | ○ | アップロードしたファイルの場所 |
| `description` |  | 説明文 |
| `tag` |  | 小さいラベル（例: `建築`、`家具`） |
| `version` |  | アドオンのバージョン |
| `minecraft` |  | 対応する Minecraft のバージョン |
| `updated` |  | 更新した日 |
| `image` |  | スクリーンショットの場所 |

「Commit changes」を押すと、1〜2分でサイトに反映されます。

## 公開の設定（最初の1回だけ）

1. リポジトリの「Settings」→ 左メニューの「Pages」を開く
2. 「Branch」で `main`、フォルダは `/ (root)` を選んで「Save」
3. 数分たつと `https://robokun60-del.github.io/Japan-addon/` で見られるようになります
