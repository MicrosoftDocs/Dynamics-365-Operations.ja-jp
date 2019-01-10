## <a name="self-service-database-export"></a>データベースのセルフ サービスエクスポート

サンド ボックス環境詳細ページで、**管理** メニューをクリックし、**データベースの移動** を選択します。  
<img src="../database/media/DBMovement_Menu.png" width="400px" alt="Move database menu" />

**エクスポート データベース**アクションが使用できるページでスライダー ウィンドウが開きます。
<br/>
<img src="../database/media/Export_Menu.png" width="400px" alt="Export database menu"/>

サンド ボックスの更新やパッケージの展開などの他のサービス操作はこの間実行できません。 ソース環境は Dynamics ユーザーの観点から使用可能になります。  

エクスポートが正常に完了すると、**環境の詳細** ページで実行している操作からサインオフされます。 **データベースのバックアップ** セクションの **資産ライブラリ** で資産を確認できます。
<img src="../database/media/AssetLibrary_Backups.png" width="800px" alt="Asset library backup files"/>

.bacpac ファイルではここに保存され、レベル 1 開発者環境に手動でダウンロードすることができます。 今後、Microsoft は、エクスポート アクションをトリガーし、資産ライブラリで使用可能なバックアップ ファイルを一覧表示するための API を提供します。 これには、バックアップ資産ファイルを自動でダウンロードするための、または Microsoft Azure Storage SDK を使用して、独自のセキュリティで保護された BLOB ストレージに直接コピーするための、セキュリティで保護された URL が含まれます。
