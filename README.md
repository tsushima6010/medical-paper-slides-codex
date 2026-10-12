# medical-paper-slides（Codex版）

医学論文のPDFから、論文内容の**要約スライド**（日本語・pptx）を作るCodex用スキル。
作成されるのは論文の要約であり、そのまま学会発表に使うことは想定していない。

Claude版はこちら：https://github.com/tsushima6010/medical-paper-slides

## できること
- 論文の要点を短時間で把握できる**要約スライド**（pptx）を作る
- 1枚ごとに「論点 → 答え → 根拠」が成立する構成にする
- 出典（ページ・表・図）をスピーカーノートに残す

## 前提
- PDFの読み取りとpptxの組み立ては、Codex標準の **pdf スキル** と **Presentations スキル** を使うため、それらが使える環境が前提

## 導入
Codex にこのページのURLを貼って「このスキルを medical-paper-slides という名前で入れて」と頼めば導入できる
（Codex標準の skill-installer が `~/.codex/skills/medical-paper-slides` に入れる。導入後は新しいセッションで認識される）。

手動で入れる場合は、次のどちらかで `~/.codex/skills/medical-paper-slides` に置く。
- git を使う：
  ```
  git clone https://github.com/tsushima6010/medical-paper-slides-codex.git $HOME/.codex/skills/medical-paper-slides
  ```
  更新は `git -C $HOME/.codex/skills/medical-paper-slides pull`
- zipを使う：最新版を下記からダウンロードし、解凍した `medical-paper-slides` フォルダを `~/.codex/skills/` に置く
  https://github.com/tsushima6010/medical-paper-slides-codex/releases/latest/download/medical-paper-slides-codex.zip

## 使い方
論文PDFを渡して「スライドにして」と依頼する。
指定がなければ、作業中のフォルダにpptxが保存される。

## 注意
- 患者情報・未発表データを含むファイルは使用しない
- 数値・統計値・引用は必ず原著と照合する

## ライセンス
[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.ja)（全文は [LICENSE](LICENSE)）

- 個人・業務での利用、改変、商用利用は自由。このスキルで作成したスライドに表示義務はない
- スキル自体（原版・改変版）を再配布・公開する場合は、次のように出典を表示すること
  > 本スキルは tsushima6010「medical-paper-slides（Codex版）」（https://github.com/tsushima6010/medical-paper-slides-codex 、CC BY 4.0）を改変したものです。
- 無保証。本スキルを用いて作成したスライドの内容の正確性は利用者が確認すること
