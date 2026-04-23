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
---

## 周回2 Plan(2026-04-23)

### 構想(たっぺい)
既存の index.html に Contact ボタンを1つ追加する。
- 配置: 自己紹介文の少し下、右カラム内
- 左の画像(200×200)の下端を縦方向で越えない
- カラー: 白基調
- 文字サイズ: 自己紹介文より大きい
- クリックしやすいサイズ感

### 技術仕様(Claude翻訳)
- 追加要素: button タグ、テキスト「Contact」
- 配置: .profile 内の3行pタグの直後(右カラム内)
- .profile に align-items: flex-start を追加(上寄せ)
- 色: 背景 #F2F7FA / 文字 #1F6FB8 / 枠線なし
- ホバー時: 背景 #FFFFFF / 文字 #1F6FB8 維持
- サイズ: padding 12px 28px / font-size 16px / font-weight 600
- border-radius: 6px
- cursor: pointer
- transition: all 0.2s ease
- ボタンと自己紹介文の間隔: margin-top 20px
- クリック動作: なし(周回4で追加予定)

### 禁則
- JavaScript はまだ使わない(周回4で解禁)
- 外部ライブラリ使わない
- プレーンな HTML + CSS
- hair helpman世界観(海×女神×波)の色は使わない

### 検証方法
- ブラウザで表示 → ボタンが自己紹介文の下に見える
- 右カラム全体が画像(200px)の下端を越えていない
- ボタンの文字が自己紹介3行より大きい
- マウスホバーで背景が純白に変化する
- ボタンの上にカーソルを置くと指マークに変わる