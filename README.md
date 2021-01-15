# atcoder_env

本リポジトリは Atcoder を Python で取り組むための環境になります

## 内容

- devcontainer
- lint
  - black
- online-judge-tools
- atcoder-python-snippets
- atcoder-cli

## 環境詳細

- Python : 3.8.2

## 事前準備

- Docker インストール
- VSCode インストール
- VSCode の拡張機能「Remote - Containers」インストール
  - https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers
- 本リポジトリの clone

## 使用方法

1. VSCode 起動
2. 左下の緑色のアイコンクリック
3. 「Remote-Containersa: Reopen in Container」クリック
4. しばらく待つ
   - 初回の場合コンテナ image の取得や作成が行われる
5. 起動したら開発可能
6. ログイン
   - `acc login`
   - `oj login https://atcoder.jp/`
7. contestID を取得
   - `https://atcoder.jp/contests/abs` の場合、 `abs`
8. ディレクトリ作成（問題を選択）
   - `acc new ${contestID}`
   - 例: `acc new abs`
9. 回答する問題のディレクトリに移動
   - `cd {contestID}/{問題}`
10. 回答を作成
    - 例: `cd abs/practicea`
    - ファイル名は何でも良い
    - 例: `main.py`
11. 回答をテスト
    - `oj t -c "python main.py -d ./tests/"`
12. 回答を提出
    - `acc submit main.py`

### 使用例

```
acc new abs
cd abs/practicea/
vi main.py
oj t -c "python ./a.py" -d ./tests/
acc submit main.py
```
