---

# CarRacing-v2 

このリポジトリは、強化学習を使用して **CarRacing-v2** ゲームをプレイするAIモデルを訓練および評価するためのソリューションを提供します。このプロジェクトでは、TensorFlowとOpenAI Gymを使用してエージェントの訓練と評価のパイプラインを実装しています。

---

## 特徴

- **深層強化学習**: Actor-Criticアーキテクチャを使用した意思決定モデル。
- **シミュレーション環境**: OpenAI Gymの`CarRacing-v2`環境を活用。
- **ビデオ録画**: `gym.wrappers.RecordVideo`を使用してプレイ映像を記録。
- **事前訓練モデルのサポート**: 訓練済みモデルをロードして評価する機能を含む。

---

## インストール

1. リポジトリをクローンします:
   ```bash
   git clone https://github.com/yourusername/CarRacing-AI.git
   cd CarRacing-AI
   ```

2. 必要な依存関係をインストールします:
   ```bash
   pip install swig
   pip install gym[box2d]
   pip install -U pyvirtualdisplay
   pip install gym-notebook-wrapper
   ```

3. システム依存パッケージをインストールします:
   ```bash
   sudo apt update
   sudo apt install -y xvfb
   ```

---

## 使用方法

### モデルの訓練

モデルを新規に訓練するか、保存された重みから続きの訓練を行うには以下の手順を行います。
1. スクリプト内のモデル保存・読み込みパス（`model_path`）を確認して適宜変更してください。
2. 訓練スクリプトを実行します:
   ```bash
   python train_car_racing.py
   ```

### 訓練済みモデルでのテスト

1. 訓練済みモデルファイル（`actor.h5`、`critic.h5`など）が指定されたパス（デフォルトでは`/content/drive/MyDrive/DQN_save/`）に存在することを確認してください。

2. テスト後、ゲームプレイ映像が`./mp4`フォルダに保存されます。

---

## 結果

- 訓練および評価のログは実行中に表示されます。
- 評価中に生成されるゲームプレイ映像は、`./mp4`ディレクトリに保存されます。


