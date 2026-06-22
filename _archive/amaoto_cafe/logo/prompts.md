# 雨音Cafe ロゴ生成プロンプト（方式A：3ツール用 3変種）

各ツールで2〜4枚ずつ回して計10枚生成 → KEIが選定 → gpt-imageで最終仕上げ。
**共通の必須条件**：
- テキストは必ず「**雨音Cafe**」。「雨音」の漢字が崩れていないものだけ採用（誤字チェック必須）。
- 背景は**純白(#FFFFFF) または 純黒のフラット・影なし**。ロゴのみ中央、周囲に余白。
- 切り抜きしやすい**高解像度PNG**。透過前提なのでフラット背景厳守。
- 世界観：どうぶつの森的なほのぼの・ふわふわ。

---

## 変種① ChatGPT (gpt-image) 向け — 自然言語・関係性重視

```
かわいいロゴデザイン。テキストは日本語で「雨音Cafe」。
「雨音」の部分は、水色の光沢グラデーション＋白の極太フチを持つ、ぷっくり丸い団扇文字（推し文字）風の太ゴシック。文字のまわりに雨だれの粒と星のキラキラを散らす。
「Cafe」の部分は、温かい茶色のグラデーションの丸文字で、クリーム色のフチ。すぐ横に湯気が立つ小さなコーヒーカップ。
黒猫のしっぽが文字にくるんと巻きつく、ほのぼのした「あつまれ どうぶつの森」風のやわらかい世界観。
背景は純白でフラット、影なし。ロゴだけを中央に置き、周囲に余白。高解像度、切り抜きしやすい仕様。
漢字「雨音」は正確に、崩さない。
```

## 変種② Google Gemini (Imagen) 向け — 視覚記述・スタイル語強め

```
A cute kawaii Japanese logo with the exact text "雨音Cafe".
"雨音" (Japanese kanji): puffy rounded bubble lettering, glossy light-blue gradient fill with a thick white outline, decorated with small raindrops and sparkling stars. Soft, plump "uchiwa moji" idol-style typography.
"Cafe": warm brown gradient rounded letters with a cream outline, next to a tiny steaming coffee cup.
A black cat's tail curls around the letters. Soft, cozy "Animal Crossing" aesthetic, pastel and fluffy.
Flat pure-white (#FFFFFF) background, no shadow, logo centered with margin around it.
High resolution, clean edges for easy cutout. Render the kanji 雨音 accurately, do not distort it.
```

## 変種③ xAI Grok 向け — 簡潔・要素列挙

```
Kawaii logo, text "雨音Cafe".
- "雨音": glossy light-blue gradient, thick white outline, puffy rounded bubble font, raindrops + sparkles.
- "Cafe": warm brown gradient rounded font, cream outline, small steaming coffee cup beside it.
- A black cat tail wrapping around the text.
- Animal-Crossing-style cozy fluffy mood.
- Flat pure white background, no shadow, centered with margin, high-res PNG, clean cutout edges.
- Accurate Japanese kanji 雨音, no distortion.
```

---

## 選定メモ（KEI記入用）

| # | ツール | 採用候補 | コメント（漢字OK? 色味? フチ?） |
|---|--------|---------|------------------------------|
| 1 |        |         |                              |
| 2 |        |         |                              |
| … |        |         |                              |

最終：選んだ1枚を gpt-image で「フチの均一化・背景完全フラット化・解像度UP」して納品。
