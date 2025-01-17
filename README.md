# 課題
Mermaidを触ってみよう

マークダウンファイルを編集して、Mermaidで図を描いてみよう

# 取り組み方
* 本プロジェクトをforkしてください。
* README.mdを編集して、Mermaidを使いこなしてください
* できたらプルリクエストを出します

# 課題項目
## 流れ図
### 条件
- 開始と終了ノードをつける
- 条件分岐を組み込む
- 5ノード以上
- カッコいいほど高得点

## 解答
```mermaid
flowchart LR;
  A([開始]) --> B[スライムが現れた];
  B -- 戦う --> C[スライムに5ダメージを与えた];
  C --> D[スライムを倒した];
  B -- 逃げる --> E[逃げられなかった];
  E --> F[勇者は全滅した];
  D --> G([終了]);
  F --> G;
```

## シーケンス図
### 条件
- 3人以上
- メッセージをやり取りしない人がいないように
- 自己呼び出しを含むこと
- カッコいいほど高得点

## 解答
```mermaid
sequenceDiagram
    actor 太郎
    actor 花子
    actor 悠斗
    actor 雄太
    太郎->>花子: おはよう！
    activate 花子
    花子-->>太郎: おはようございます!
    deactivate 花子
    花子->>悠斗: 調子はどう？
    activate 悠斗
    悠斗-->>花子: 絶好調だよ！
    deactivate 悠斗
    悠斗->>雄太: 昨日の野球見た？
    activate 雄太
    雄太-->>悠斗: 凄かったよね
    deactivate 雄太
```

## クラス図

### 条件
- 3つ以上
- 汎化と集約を含むこと
- カッコいいほど高得点

## 解答
```mermaid
classDiagram
    プレイヤー o-- アイテム
    アイテム o-- 武器
    武器 <|-- 剣
    武器 <|-- 斧
    武器 <|-- 弓
    プレイヤー  o-- ステータス
    ステータス : HP
    ステータス : MP
    ステータス : 力
    ステータス : 魔力
    ステータス : 防御
    ステータス : 素早さ
```
