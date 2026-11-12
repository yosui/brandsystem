# Typography

3つの書体に、それぞれ役割を1つだけ持たせます。数字は硬く、言葉は人懐っこく。

## 3つの書体と役割

| 役割 | 書体 | 担当するもの | 性格 |
| --- | --- | --- | --- |
| Display（`--font-display`） | Big Shoulders Display | 残高・レート・英字の大見出し | 硬い、重い、縦に詰まっている |
| Voice（`--font-voice`） | Darker Grotesque | あいさつ・ボタン・英字の小見出し | 背が低く、クセがある、人懐っこい |
| Text（`--font-text`） | M PLUS 1 | 和文すべて・本文・UIの小さい文字 | ニュートラル、読みやすい |

- **和文はすべて M PLUS 1:** Display と Voice のフォント指定には M PLUS 1 を続けて書いてあるので、英字と和文が混ざった文でも、和文の部分は自動で M PLUS 1 になります。
- **太さは見出しで振り切る:** 見出しは 800〜900、本文は 400、ラベルは 500 です。600〜700 の中間の太さは使いません。

## スケール

Typography のページに全スタイルがあります。要点は次のとおりです。

- **`display-xl` 80px / `display-l` 52px:** 英字は必ず大文字にします。行送りは 0.85〜0.88 まで詰めます。1画面に1つだけです。
- **`amount-hero` 64px / `amount-l` 32px:** 画面の主役になる金額は1つだけにします。
- **`voice-l` 34px / `voice-m` 24px / `button` 20px / `button-s` 18px:** 字間を少し詰めて（`voice-l` は -0.5px）、背の低さを生かします。
- **`ja-display` 36px / `ja-h1` 26px / `ja-h2` 20px / `ja-h3` 17px:** 和文の見出しは行送り 1.25〜1.45 です。英字見出しのように詰めすぎると、漢字の上下がぶつかります。
- **`body-l` 17px / `body` 15px / `figure` 15px / `label` 13px / `caption` 12px:** 12px より小さい文字は作りません。

## 守ること

1. **Darker Grotesque は 18px 以上:** x-height（小文字の高さ）が低いので、小さくすると一気に読めなくなります。小さいボタンでも `button-s` の 18px が下限です。
2. **縦に並ぶ金額は `figure`:** Big Shoulders Display と Darker Grotesque は数字の幅がそろっていません。取引一覧のように金額が縦に並ぶ場所では、M PLUS 1 に `font-variant-numeric: tabular-nums` を付けた `figure` を使い、桁をそろえます。
3. **Big Shoulders Display の英字は大文字:** 小文字だと細長さが目立ち、重さが出ません。和文と数字はそのままです。
4. **見出しの文字色は `ink`、補足は `ink-muted`:** 数字を強調するときだけ `overlap` を使います。

## 組み方の例

```html
<p class="voice-m" style="color: var(--ink)">Good morning</p>
<p class="amount-hero" style="color: var(--ink)">¥128,000</p>
<p class="label" style="color: var(--ink-muted)">総残高</p>

<p class="ja-h2" style="color: var(--ink)">お金を動かそう。</p>
<p class="body" style="color: var(--ink-muted)">手数料は表示どおり。隠れたコストなし。</p>

<span class="figure" style="font-variant-numeric: tabular-nums">¥12,400</span>
```

## フォントのライセンス

3書体とも SIL Open Font License 1.1 のもとで公開されている Google Fonts の書体で、商用利用も、アプリやWebへの埋め込みも無料です。`fonts/` に入っているのは、Google Fonts のリポジトリにある可変フォント（太さを自由に変えられるフォント）を woff2 形式に変換したものです。M PLUS 1 は日本語の全文字を含むため 1.7MB あります。Web で使うときは、Google Fonts から読み込むと必要な文字だけが分割配信されます。
