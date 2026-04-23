# Phase 01 - 周回1 Plan

## 目的
Cursor Agent Mode に Plan → Execute → Verify の型で指示を出し、
意図通りの画面を生成させる初めての経験を作る。

## 作るもの
1枚の自己紹介カードページ(TAPPEI's Card)

## 作成ファイル
- index.html : 構造(タイトル、画像、自己紹介文)
- style.css : 見た目(色、配置、フォント)

## 指示内容の要件
- タイトル: TAPPEI's Card(h1)
- 画像: ダミー画像 https://placehold.co/200x200 を1枚
- 自己紹介3行:
  1. YRKTチーム実装担当
  2. hair helpmanプロジェクト
  3. Phase 01 周回1 - Cursor Agent初指示
- 背景色: #1F6FB8(海の青系、hair helpman世界観は不可侵)
- 文字色: #F2F7FA(白系)
- レイアウト: max-width 720px、中央寄せ、padding 32px
- 画像と文章は flexbox で横並び
- フォント: system-ui, sans-serif

## 禁則
- JavaScript を使わない
- 外部ライブラリ(Bootstrap、Tailwindなど)を使わない
- プレーンな HTML + CSS のみ

## 検証方法
ブラウザで index.html を開いて、上記5要件すべてが目視確認できること　
---

## 周回ログ

### 周回1 完了(2026-04-23)
- 指示内容: 自己紹介カード(TAPPEI's Card)の生成
- 使用技術: HTML + CSS
- Agent挙動: Plan復唱 → 承認 → index.html / style.css 自動生成
- 検証結果: 5点すべてOK
- 学び: Agentへの指示はPLAN.md参照方式で通る