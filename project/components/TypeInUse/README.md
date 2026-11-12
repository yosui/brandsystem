# TypeInUse

ホーム画面を例に、3つの書体とスタイルを実際にどう組み合わせるかを示す見本です。

- **あいさつ:** `voice-m`（Darker Grotesque）
- **残高:** `amount-hero`（Big Shoulders Display）と、その下にラベルの `label`
- **カード見出しと説明:** `ja-h2` と `body`（M PLUS 1）
- **強調する数字1つ:** `amount-l` を `overlap` の文字色で
- **ボタン:** `button`。主ボタンは `jade` の塗りに `ink` の文字、副ボタンは `fill-subtle` の淡い塗り
- **縦に並ぶ金額:** `figure` に `font-variant-numeric: tabular-nums`。桁がそろいます
- **注記:** `caption`

使う側が用意するもの：`tokens.css` の読み込み（書体と色のトークンが入っています）と、右上のブランド図形のSVG（`jade` と `violet` の円、重なり部分を `overlap`）です。
