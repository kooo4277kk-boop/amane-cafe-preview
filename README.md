# 雨音Cafe ポモドーロ素材 — README

KEIのVRChat背景動画に**重ねるオーバーレイ素材**。全素材は透過前提。

## フォルダ構成
```
assets/
  timer/timer.html          … 25分タイマー本体（パラメータ化）
  cat/cat_walk_loop.html    … 白猫の歩行ループ
  logo/prompts.md           … ロゴ生成プロンプト（方式A：3ツール3変種）
  README.md                 … このファイル
```
※ `*_alpha.mov` / `*_alpha.webm` / `*_green.mp4` は**KEIのOK後**に書き出す（まだ無い）。

---

## 1. プレビューのしかた（ブラウザで開くだけ）

各 .html を **Chrome にドラッグ**すれば動く。確認用に市松模様(checker)背景が既定なので、透過部分が一目で分かる。

- タイマーを**素早く確認**したい時（25分待たない）:
  `timer.html?workMin=1&bgMode=checker`
  → 1分版で出現→カウント→消滅まで通しで見られる。
- 透過の見え方を緑クロマで確認: `timer.html?bgMode=green`
- 猫の速度・大きさ確認: `cat_walk_loop.html?bgMode=green&walkSpeed=0.8&size=1.3`

## 2. パラメータ調整（量産）
各HTMLの先頭 `CONFIG` を書き換えるだけ。
- timer: `workMin` を 50 / 10 等に変えれば別分数版が即作れる。`bgMode` で透過/緑/青を切替。
- cat: `walkSpeed`（1ループ秒数）, `size`, `tailSwing`, `bgMode`。

## 3. 透過書き出し（KEIのOK後にリンが実行）
このPCには **ffmpeg** と **playwright-core** があるので、ヘッドレスChromeでフレーム連番をキャプチャ→ffmpegで:
- **透過mov（ProRes4444）** … Premiere本命納品
- **透過webm（VP9 alpha）** … 軽量ループ素材（猫）
- **緑mp4** … 画面収録代替

タイマーは `window.__TIMER_DONE__` / `document.title='DONE'`、猫は `window.__LOOP_SEC__` で1ループ尺を検知できるよう実装済み。

## 4. Premiereへの載せ方
1. 背景動画（VRChat撮影）を最下レイヤーに置く。
2. その上に `timer_25min_alpha.mov`（透過）を重ねる。位置はタイマー側 `CONFIG.position` 相当でプロジェクト内移動。
3. 猫ループ `cat_walk_loop_alpha.webm` を別トラックで重ね、必要尺ぶんリピート。
4. ロゴPNGを四隅などに配置。

## 5. 順番ルール（厳守）
止め絵/HTML → **KEI確認** → OK後に動画書き出し。確認前に書き出さない。
