# 株式自動売買システム

このプロジェクトは、特定の条件に基づいて株式の自動売買を行うPythonスクリプトです。
github actionsで自動化することで、通称ランドゲームをまったく株ゲームをやらずに楽しめます。

## ファイル構成

- `login.py`: ログイン、注文送信、株データ取得、資産合計取得、ランド社の株価取得などの主要な機能を含むスクリプト。
- `config.py`: ログインURL、注文URL、ログイン成功テキスト、ログインデータ、注文データなどの設定を含むスクリプト。

## 必要なライブラリ

以下のPythonライブラリが必要です。

- `requests`
- `beautifulsoup4`
- `yfinance`

インストールは以下のコマンドで行えます。

```sh
pip install requests beautifulsoup4 yfinance
```

## 使用方法

1. `config.py` ファイルでログイン情報や注文情報を設定します。
2. `login.py` スクリプトを実行します。

```sh
python login.py
```

## 機能

- **ログイン**: 指定されたURLとデータを使用してログインを試みます。
- **注文送信**: 指定されたURLとデータを使用して注文を送信します。
- **株データ取得**: 保有している株のデータを取得します。
- **資産合計取得**: 資産の合計を取得します。
- **ランド社の株価取得**: ランド社の最新の株価を取得します。

## 注意事項

- このスクリプトは教育目的で提供されており、実際の取引に使用する際は自己責任で行ってください。
- ログイン情報や注文情報は適切に管理し、第三者に漏洩しないように注意してください。

## ライセンス

このプロジェクトはMITライセンスの下で提供されています。
## 設定方法

1. **`config.py`の編集**:
    - `LOGIN_URL`: ログインに使用するURLを設定します。
    - `ORDER_URL`: 注文送信に使用するURLを設定します。
    - `LOGIN_DATA`: ログイン時に送信するデータを設定します（例: ユーザー名、パスワード）。
    - `ORDER_DATA`: 注文送信時に必要なデータを設定します（例: 銘柄コード、注文数量）。

2. **環境変数の利用**:
    - センシティブな情報は環境変数として設定することを推奨します。

## 実行例

以下はスクリプトの実行例です。

```sh
$ python login.py
ログイン成功
注文条件を満たさないため注文を送信しませんでした
```

## よくある質問

### Q: ログインに失敗します。どうすればいいですか？

A: `config.py`で設定したログイン情報が正しいか確認してください。また、ログインURLが変更されていないか確認してください。

## コントリビューション

貢献を歓迎します。バグ報告や機能提案は、Issueを作成してください。プルリクエストもお待ちしております。