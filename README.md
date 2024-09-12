## atcoder-cli,online-judge-tools による AtCoder のローカル自動テスト用のリポジトリ


## 参考リンク
- [AtCoder コンテスト一覧](https://atcoder.jp/contests)
- [online-judge-tools ドキュメント](https://github.com/online-judge-tools/oj/blob/master/docs/getting-started.ja.md)


## 作業手順

### 1. 問題のダウンロード
`contests`ディレクトリで以下のコマンドを実行します。
atcoder.jp/contest/の後にくるのが、コンテストID。

```
acc new <contest_id>
```


### 2. 回答ファイルの作成
ダウンロードされた問題のディレクトリに移動し、sample.ts をコピーして main.ts を作成します。

```
cp sample.ts main.ts
```

### 3. コードの記述
main.ts ファイルに解答を記述します。


### 4. テストの実行
以下のコマンドでテストを実行します。


```
oj t -c "npx ts-node main.ts" -d ./tests/ -N
```
注: -N オプションはスペースと改行の違いを無視します。


### 5. 回答の提出
Node.js環境の場合。

```
acc submit main.ts -- -l 5058
```
