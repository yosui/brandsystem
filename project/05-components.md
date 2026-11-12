# Components

部品の種類・使い分け・寸法は、Wise が公開している部品ライブラリ（Neptune）の構成に合わせています。色と書体だけがこのブランドのものです。各部品の見本と使い方は Components のページにあります。

## 部品の一覧

| 分類 | 部品 |
| --- | --- |
| 行動（Actions） | Button、CircularButton、IconButton、Chips、SegmentedControl、Tabs |
| 入力（Forms） | TextInput、MoneyInput、SelectInput、Checkbox、Radio、Switch、DateInput、Upload |
| 内容（Content） | ListItem、AvatarView、Card、PromoCard、Tile、Decision、Header、Divider、Accordion、DefinitionList、InstructionsList、Stepper、Table |
| お知らせ（Feedback） | InfoPrompt、InlinePrompt、CriticalBanner、Snackbar、StatusIcon、ProgressBar、Loader、Nudge |
| 重ねて出すもの（Overlays） | Modal、Drawer、Popover、Tooltip |
| 組み合わせ（Patterns） | SectionRhythm、TypeInUse、BrandMark |

## どれを使うか迷ったとき

- **行動させたい:** 1つなら Button。よく使う3〜4個を並べるなら CircularButton。
- **選ばせたい:** 2〜5個で違いを説明したいなら Radio か Decision。多いなら SelectInput。絞り込みなら Chips。表示の切り替えなら SegmentedControl。
- **すぐに切り替わる設定:** Switch。保存が必要なら Checkbox。
- **伝えたい:** 画面の中に残すなら InfoPrompt、入力欄の下なら InlinePrompt、操作の直後に一瞬なら Snackbar、緊急なら CriticalBanner。
- **確認させたい:** パソコンは Modal、スマートフォンは Drawer。
- **一覧:** スマートフォンは ListItem、パソコンで比べるなら Table。

## すべての部品に共通すること

- **押せる範囲は 48px 以上。**
- **色だけで状態を伝えない:** 記号か言葉を添える。
- **影は使わない:** 縁は `ring`。
- **フォーカスは `ring-focus`。**
- **金額は `tabular-nums` で桁をそろえる。** 主役の金額だけ Big Shoulders Display。
