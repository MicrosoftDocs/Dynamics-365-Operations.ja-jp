開発環境から標準ユーザー承認テスト (UAT) まで準備されたデータベース、または UAT 環境から前回エクスポートしたデータベースをインポートするには、次のステップに従います。

1. ターゲット サンドボックスの **環境詳細** ページを開き、 メニュー オプションから **管理** > **データベースの移動** を選択します。
2. **データベースのインポート**を選択し、資産ライブラリからソース データベースのバックアップ (.bacpac形式) ファイルを選択します。
3. 警告に注意してください。 バックアップ ファイルからクリーンアップされたデータ要素の一覧を確認します。
4. インポート操作をすぐに開始します。


データベース バックアップ (.bacpac) ファイルをダウンロードした後、データベースを開発環境にインポートするには、レベル 1 環境の手動インポート操作の開始が可能です。 データベースをインポートするときは、これらのガイドラインに従うことお勧めします。

- 必要な場合は、後で戻すことができるように、既存の AxDB データベースのコピーを保持します。
- **AxDB\_fromProd** などの新しい名前の下に新しいデータベースをインポートします。

最良のパフォーマンスを確実にするためには、\*.bacpac ファイルをインポート元のコンピューターにコピーします。 sqlpackage .NET Core for Windows を [Get sqlpackage .NET Core for Windows](https://docs.microsoft.com/sql/tools/sqlpackage-download?view=sql-server-ver15#get-sqlpackage-net-core-for-windows) からダウンロードします。 **コマンド プロンプト** ウィンドウを開き、sqlpackage .NET Core フォルダーから次のコマンドを実行します。

```

SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:localhost /tdn:<target database name> /p:CommandTimeout=1200
```

パラメータの説明を以下に示します。

- **tsn (ターゲット サーバー名)** – インポートする Microsoft SQL Server インスタンスの名前。
- **tdn(ターゲット データベース名)** – インポートするデータベースの名前。 データベースが既に存在していては**いけません**。
- **sf(ソース ファイル)** – インポートするファイルのパスと名前。

> [!NOTE]
> インポート中に、ユーザー名およびパスワードは必要ありません。 既定では、SQL Server は、現在サインインしているユーザーに対して Microsoft Windows 認証を使用します。

レベル 1 の環境に手動インポート処理を実行する方法については、[データベースのインポート](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/database/dbmovement-scenario-exportuat#import-the-database) を参照してください。 
