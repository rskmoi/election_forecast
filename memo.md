# DeepLearningBook 10章
## 前書き
- Recurrent neural networks, RNN
- 時系列
- 可変長にも対応できる

時間のインデックスの値それぞれに対して別々のパラメータを用意すると、訓練時とは異なる長さのデータに対して一般化ができない

### 確認
- RNNとは？時間のインデックスが1-τ,ベクトルx(t)

## 10.1
### 計算グラフ
- 10.5式のように、ひとつ前の隠れ層と現在の入力で出力が決まる計算グラフ

メリット
- 状態の長さにかかわらず、入力サイズが一緒
- すべての時間ステップにおいて同じパラメータによるfを使用できる

## 10.2
### 図10.3
代表的な例。

チューリングマシンの話（わからん）

ロスは,1-τの全部のロスの合計

BPTTは強力な分、計算量が多い

勾配計算は、ざっくり概念だけ伝えればいいか

### 図10.4
説明oが非常に高次元で表現力が高くない場合
→oが非常に高次元であるために十分な表現力を持つ場合を除き、くらい？
10.3と比較したデメリット：情報が失われる
メリット：計算コストが低い（並列化できる）

出力が自分自身に戻る回帰的な接続を持つモデルは、teacher forcingで訓練できる

訓練：真の出力
テスト：予測

freerunninngってなに。。

## 10.2.3
過去の出力すべてが効いてくる場合に有用

https://www.slideshare.net/unnonouno/nip2015endtoend-memory-networks
https://www.slideshare.net/tsubosaka/deeplearning-60419659
http://deeplearning.hatenablog.com/entry/memory_networks
https://qiita.com/t_Signull/items/21b82be280b46f467d1b
