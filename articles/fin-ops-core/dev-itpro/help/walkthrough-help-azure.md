---
title: Azure にカスタム ヘルプを展開
description: この記事では、Microsoft Dynamics 365 ヘルプ コンテンツを Azure Web アプリに展開する方法を示す例を紹介します。
author: edupont04
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Operations
ms.openlocfilehash: b06d615a8b4956cc8edbceac3dc4ab8285cd5441
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284470"
---
# <a name="deploy-custom-help-to-azure"></a>Azure にカスタム ヘルプを展開

[!include [banner](../includes/banner.md)]

この記事では、コンテンツをホストする Web アプリを設定する手順と、コンテンツを製品内の **ヘルプ** ウィンドウで検出可能にするように検索サービスを設定する手順について説明します。 Microsoft Azure Web アプリを設定した後、その Web アプリを使用して、製品内の **ヘルプ** ウィンドウに接続されたコンテンツをホストします。

[Azure サブスクリプション](/azure/guides/developer/azure-developer-guide#understanding-accounts-subscriptions-and-billing)をお持ちでない場合は、この記事の手順を実行する前にアカウントを作成してください。 12 か月間は無料のアカウントで開始できます。 詳細については、[今すぐ Azure 無料アカウントを作成する](https://azure.microsoft.com/free/) を参照してください。

## <a name="get-started"></a>概要

[ヘルプ ウィンドウで使用するコンテンツの準備](preparing-content.md)の記事では、製品内の **ヘルプ** ウィンドウで使用できるようにヘルプ コンテンツを準備する手順について説明します。 一連の HTML ファイルとそれに相当する JavaScript Object Notation (JSON) ファイルを取得したら、Web アプリと検索サービスを設定できます。

### <a name="process-overview"></a>プロセスの概要

Azure リソースを作成するための一般的なプロセスは、次の手順で構成されます:

1. Azure ポータルで、[リソース グループを作成します](#resgr)。
2. Azure ポータルで、[Web アプリを作成](#webapp)、[ストレージ アカウント](#jsonstorage)、[検索サービス](#searchservice) を作成します。

    - Web アプリは、HTML ファイルを格納して提供します。 HTML ファイルには、ヘルプ コンテンツが含まれています。
    - ストレージ アカウントは、BLOB コンテナーを使用して JSON ファイルを格納します。 JSON ファイルは、JSON 形式に変換された後のヘルプ ファイルであり、検索目的でコンテンツのインデックスを生成するために使用できます。 詳細については、[カスタム ヘルプ ツールキット: ConvertHtmlToJson ツール](custom-help-toolkit-ConvertHtmlToJson.md) を参照してください。
    - 検索サービスは、ヘルプ コンテンツのインデックスを作成します。 インデックスを使用すると、製品内の **ヘルプ** ウィンドウでコンテンツを検索できるようになります。 詳細については、[Azure Cognitive Search で基本的なインデックスを作成する](/azure/search/search-what-is-an-index) を参照してください。

3. ファイル転送プロトコル (File Transfer Protocol: FTP) を使用して Web アプリに [HTML ファイルをアップロード](#uploadhtml) します。

    この手順を完了すると、コンテンツが作成されたロケールに基づいて、HTML ファイルを関連する言語のサブフォルダーに配置します。 これらのサブフォルダーに使用する名前の詳細については、[製品およびヘルプの言語およびロケール記述子](language-locale.md) を参照してください。

4. HTML ファイルの言語サブフォルダーに対応するサブフォルダーで、ストレージ コンテナーの Azure Blob Storage に [JSON ファイルをアップロード](#jsonstorage) します。
5. REST アプリケーション プログラミング インターフェイス (API) を使用して、検索サービスにデータ ソース、インデックス、インデクサーが含まれるように、[検索サービスを設定](#searchconfig) します。

    この例では、[Postman](https://www.postman.com/) という名前の API ツールを使用してREST API 呼び出しを行います。 言語固有のインデックス アナライザーを使用するには、言語固有のインデックスを作成する必要があります。

この記事の残りのセクションでは、Azure アカウントと有効なサブスクリプションを持っていることを前提としています。 [Azure サブスクリプション](/azure/guides/developer/azure-developer-guide#understanding-accounts-subscriptions-and-billing) をお持ちでない場合は、始める前にアカウントを作成してください。 12 か月間は無料のアカウントで開始できます。 詳細については、[今すぐ Azure 無料アカウントを作成する](https://azure.microsoft.com/free/) を参照してください。

## <a name="create-a-resource-group"></a><a name="resgr"></a>リソース グループを作成する

Web アプリ、検索サービス、ストレージ アカウントをホストするには、最初に 1 つ以上のリソース グループを作成する必要があります。 管理を容易にするために、単一のリソース グループにすべてのリソースを作成することをお勧めします。 詳細については、[リソース グループの作成](/azure/azure-resource-manager/management/manage-resource-groups-portal#create-resource-groups) を参照してください。

1. [Azure ポータル](https://portal.azure.com/) で、**リソース グループ** を選択し、**追加** を選択して、**MyCustomHelp** などのリソース グループの名前を指定します。
2. リソース グループの作成を完了するには、**レビュー + 作成** を選択します。

## <a name="create-a-web-app"></a><a name="webapp"></a>Web アプリの作成

コンテンツをホストするには、Azure で Web アプリを作成する必要があります。 詳細については、[Azure で静的 HTML Web アプリを作成する](/azure/app-service/app-service-web-get-started-html) を参照してください。

### <a name="create-the-web-app"></a>Web アプリの作成

1. [Azure ポータル](https://portal.azure.com/) で、リソース グループに移動し、**追加**、**Web アプリ** の順に選択して、ランタイム スタックと **MyCustomHelpWebApp** などの Web アプリの名前を指定します。

    ランタイム スタックとして任意の .Net Core スタックを使用できます。 詳細については、[Azure で ASP.NET Core Web アプリを作成する](/azure/app-service/app-service-web-get-started-dotnet) を参照してください。

2. 展開が完了したら、**リソースに移動** を選択します。
3. ページの左側で、**展開センター** を選択します。 **手動での展開 (プッシュ/同期)** で、**FTP** を選択してから、**ダッシュボード** を選択します。

    *アプリ資格情報* または *ユーザーの資格情報* を使用して、コンテンツを Web アプリ にアップロードできます。 アプリ資格情報を使用することをお勧めします。 コンテンツをアップロードするには、FTP/FTPS エンドポイント、ユーザー名、パスワードが必要です。

    続行する前に、ユーザー名とパスワードを一時的な場所にコピーすることもできます。 また、展開を完了した後に資格情報をリセットすることをお勧めします。 詳細については、[Azure App Service の展開資格情報を設定する](/azure/app-service/deploy-configure-credentials) を参照してください。

次に、HTML ファイルを Web アプリに追加します。 [FileZilla](https://filezilla-project.org/)、[Visual Studio](https://www.visualstudio.com/vs/community/)、[Cyberduck](https://cyberduck.io/)、あるいは [WinSCP](https://winscp.net/index.php) などの FTP クライアントを使用できます。 詳細については、[FTP/S を使用してアプリを Azure App Service に展開する](/azure/app-service/deploy-ftp) を参照してください。

### <a name="upload-html-files"></a><a name="uploadhtml"></a>HTML ファイルのアップロード

1. 使用する FTP クライアントを開きます。 Web アプリへのファイルのアップロードに関連するベスト プラクティスについては、[FTP/S を使用してアプリを Azure App Service に展開する](/azure/app-service/deploy-ftp) を参照してください。
2. ホスト (Web アプリの展開センターからの FTPS エンドポイント値)、ユーザー名、パスワードを入力し、接続します。
3. ホストの **/site/wwwroot** の下に、カスタム ヘルプ Web サイトがサポートする必要のある言語ごとの言語フォルダを作成します。 HTML ファイルおよびその他の関連ファイルを各言語フォルダーにアップロードします。

    > [!IMPORTANT]
    > クライアントが必要とする言語に対応するフォルダ名を使用してください。 詳細については、[製品およびヘルプの言語およびロケール記述子](language-locale.md) を参照してください。

これで、カスタム ヘルプ Web サイトが Azure に展開され、ブラウザーに表示されます。

## <a name="create-a-storage-account"></a><a name="jsonstorage"></a>ストレージ アカウントを作成する

次に、BLOB コンテナーを使用して、検索サービスが使用する JSON ファイルを格納するストレージ アカウントを作成します。 Azure Storage の詳細については、[Azure Storage ドキュメント](/azure/storage/) を参照してください。

カスタム ヘルプ ツールキット の一部である [ConvertHtmlToJson](custom-help-toolkit-ConvertHtmlToJson.md) ツールを使用して、HTML ヘルプ ファイルから JSON ファイルを生成できます。

1. [Azure ポータル](https://portal.azure.com/) で、リソース グループに移動し、**追加**、**ストレージ アカウント** の順に選択して、**mycustomhelpstorage** などのストレージ アカウントの名前を指定します。 次に、**レビュー + 作成** を選択します。 詳細については、[ストレージ アカウントを作成する](/azure/storage/common/storage-account-create#create-a-storage-account) を参照してください。
2. ストレージアカウントを検証および作成します。

    展開が完了したら、新しいストレージ アカウントがリソース グループの下に一覧表示されます。

3. ストレージ アカウントを選択し、ページの左側の **BLOB サービス** で **コンテナー** を選択します。 コンテナーを追加し、**mycustomhelpcontainer** などの名前を指定します。 詳細については、[クイックスタート: Azure ポータルで Blob をアップロード、ダウンロード、一覧表示する](/azure/storage/blobs/storage-quickstart-blobs-portal) を参照してください。

これで、JSON ファイルをアップロードできるようになりました。 使用するフォルダー構造は、ソリューションの言語に一致するように、HTML ファイル用に作成したフォルダ構造と一致する必要があります。 たとえば、Web アプリの **en-US** フォルダーに HTML ファイルがある場合、コンテナーに **en-US** フォルダーを作成し、このフォルダーに en-US JSON ファイルをアップロードします。

JSON ファイルを BLOB コンテナーにアップロードするには、いくつかの方法があります。 ユーザー インターフェイス (UI) を使用する場合、[Azure Storage エクスプローラー](/azure/storage/blobs/storage-quickstart-blobs-storage-explorer) は、Azure Storage を使用してファイル操作を管理できる便利なツールです。 コマンド ライン オプションを使用する場合、AzCopy を使用できます。 詳細については、[Windows の AzCopy からデータの転送](/azure/storage/common/storage-use-azcopy) を参照してください。

## <a name="create-a-search-service"></a><a name="searchservice"></a>検索サービスの作成

次に、コンテンツにインデックスを作成して、製品内の **ヘルプ** ウィンドウで検索できるように、検索サービスを作成します。 詳細については、[Azure Cognitive Search とは?](/azure/search/search-what-is-azure-search) を参照してください

- [Azure ポータル](https://portal.azure.com/) で、リソース グループに移動し、**追加**、**Azure Cognitive Search** の順に選択して、**URL** で **mycustomhelpsearch** などのサービスの名前を指定します。 次に、**レビュー + 作成** を選択します。

    サービスがリソース グループに追加されます。

## <a name="configure-the-search-service"></a><a name="searchconfig"></a>検索サービスを設定する

前のセクションでは、検索サービスを作成しました。 このセクションでは、ロケールごとに [データソース](#searchdatasource)、[インデックス](#searchindex)、[インデクサー](#searchindexer) を作成して、それを設定します。 これにより、BLOB コンテナーにアップロードした JSON ファイルはインデックスされ、検索可能になります。 次の例では、[Postman](https://www.getpostman.com/) ツールを使用して、いくつかの API 呼び出しを行います。 ただし、独自のメソッドを使用して、これらの API を呼び出すことができます。

### <a name="create-a-data-source"></a><a name="searchdatasource"></a>データ ソースを作成する

1. Postman を開いて、新しい POST 要求を作成します。 このツールに慣れていない場合は、[Postman を使用して Azure Cognitive Search REST API の探索](/azure/search/search-get-started-postman) を参照してください。
2. **リクエスト URL の入力** フィールドで、`https://[AzureSearchServicename].search.windows.net/datasources?api-version=2017-11-11` と入力します。 **\[AzureSearchServicename\]** を、この記事の [検索サービスの作成](#searchservice)セクションで作成した検索サービスの名前 (例えば、**mycustomhelpsearch**) に置き換えます。
3. **ヘッダー** タブで、**"Content-type"** を **application/json** に設定し、Azure Cognitive Search サービスからのキーに対して **api-key** を設定します。 キーは、検索サービスの左側にある **設定** の **アクセス キー** にあります。
4. **認証** タブで、**タイプ** を **非認証** に設定します。
5. **本文** タブで、次のテキストを貼り付けます。

    ```json
    {
        "name" : "[datasourcename]",
        "type" : "azureblob",
        "credentials" :
        {
            "connectionString" : "DefaultEndpointsProtocol=https;AccountName=[StorageAccountName];AccountKey=[key];EndpointSuffix=core.windows.net"
        },
        "container" :
        {
            "name" : "[JSONStorageContainerName]"
        }
    }
    ```

    次のパラメータを関連する値に置き換えます:

    - **\[datasourcename\]** – **mycustomhelpdatasource** などの、データ ソースの名前を指定します。
    - **\[StorageAccountName\]** – [ストレージ アカウントの作成](#jsonstorage) セクションで作成したストレージ アカウントの名前 (例えば、**mycustomhelpstorage**) を指定します。
    - **\[key\]** – ストレージ アカウントのアクセス キーを指定します。 キーは、ストレージ アカウントの左側にある **設定** の **キー** にあります。
    - **\[JSONStorageContainerName\]** – [ストレージ アカウントの作成](#jsonstorage) セクションで作成した BLOB コンテナー の名前 (例えば、**mycustomhelpcontainer**) を指定します。

6. **送信** を選択し、**ステータス** フィールドの値が **201 Created** であることを確認します。

次に、サポートする各ロケールのコンテンツのインデックスを持つように、検索サービスを設定します。

### <a name="create-an-index"></a><a name="searchindex"></a>インデックスの作成

1. Postman で、次のパラメータを持つ新しい POST 要求を作成します:

    - **URL**: `https://[AzureSearchServicename].search.windows.net/indexes?api-version=2017-11-11` (**\[AzureSearchServicename\]** を検索サービスの名前に置き換えます。)
    - **タイプ** (**認証** タブ): **非認証**
    - **コンテンツ タイプ** (**ヘッダー** タブ): **application/json**
    - **api-key** (**ヘッダー** タブ): Azure Cognitive Search サービスのキー

2. **本文** タブで、次のテキストを貼り付けます。

    ```json
    {
        "name" : "[IndexName]",
        "fields": [
            { "name": "id", "type": "Edm.String", "key": true,"searchable": true, "filterable": true, "sortable": true, "facetable": true },
            { "name": "title", "type": "Edm.String", "searchable": true, "filterable": true, "sortable": true, "facetable": true, "analyzer":"[AnalyzerName]" },
            { "name": "description", "type": "Edm.String", "searchable": true, "filterable": true, "sortable": true, "facetable": true, "analyzer":"[AnalyzerName]" },
            { "name": "ms_search_form", "type": "Edm.String", "searchable": true, "filterable": true, "sortable": true, "facetable": true },
            { "name": "ms_search_region", "type": "Edm.String", "searchable": true, "filterable": true, "sortable": true, "facetable": true },
            { "name": "ms_locale", "type": "Edm.String", "searchable": true, "filterable": true, "sortable": true, "facetable": true },
            { "name": "metadata_storage_path", "type": "Edm.String", "searchable": true, "filterable": true, "sortable": true, "facetable": true },
            { "name": "metadata_storage_name", "type": "Edm.String", "searchable": true, "filterable": true, "sortable": true, "facetable": true },
            { "name": "metadata_storage_content_type", "type": "Edm.String", "searchable": true, "filterable": false, "sortable": false, "facetable": false }
        ]
    }
    ```

    次のパラメータを関連する値に置き換えます:

    - **\[IndexName\]** – **indexenus** など、作成するインデックスの名前を指定します。
    - **\[AnalyzerName\]** – **en.microsoft** など、使用する言語アナライザーの名前を指定します。

    > [!NOTE]
    > インデックスは、言語固有です。 **タイトル** と **説明** フィールドには翻訳が含まれており、対応する言語アナライザーの値を設定することが重要です。 作成するインデックスの言語に基づいて適切な値を使用します。 言語アナライザーの一覧については、[アナライザー リスト](/azure/search/index-add-language-analyzers#analyzer-list)を参照してください。

3. **送信** を選択し、**ステータス** フィールドが **201 Created** に設定されていることを確認します。
4. 複数の言語用のカスタム ヘルプ コンテンツを用意した場合、これらの手順を繰り返して、言語ごとに固有インデックスを作成します。

インデックスは、インデクサーによって処理されるまでインデックスではありません。 リファレンス ブックの目次を考えてみてください。 本のさまざまなセクションを見つけるためのページ番号もリストされていなければ、実際には役に立ちません。 同様に、検索サービスのインデクサーは、検索に基づいてインデックスを入力します。 詳細については、[Azure Cognitive Search のインデクサー](/azure/search/search-indexer-overview) を参照してください。

### <a name="create-an-indexer"></a><a name="searchindexer"></a>インデクサーの作成

1. Postman で、次のパラメータを持つ新しい POST 要求を作成します:

    - **URL**: `https://[AzureSearchServicename].search.windows.net/indexers?api-version=2017-11-11` (**\[AzureSearchServicename\]** を検索サービスの名前に置き換えます。)
    - **タイプ** (**認証** タブ): **非認証**
    - **コンテンツ タイプ** (**ヘッダー** タブ): **application/json**
    - **api-key** (**ヘッダー** タブ): Azure Cognitive Search サービスのキー

2. **本文** タブで、次のテキストを貼り付けます。

    ```json
    {
        "name" : "[IndexerName]",
        "dataSourceName" : "[DatasourceName]",
        "targetIndexName" : "[IndexName]",
        "schedule" : { "interval" : "PT10H" },
        "parameters" : { "configuration" : { "parsingMode" : "json" } },
        "fieldMappings" : [
            { "sourceFieldName" : "/title", "targetFieldName" : "title" },
            { "sourceFieldName" : "/ms.search.form", "targetFieldName" : "ms_search_form" },
            { "sourceFieldName" : "/ms.search.region", "targetFieldName" : "ms_search_region" },
            { "sourceFieldName" : "/ms.locale", "targetFieldName" : "ms_locale" },
            { "sourceFieldName" : "/description", "targetFieldName" : "description" }
        ]
    }
    ```

    次のパラメータを関連する値に置き換えます:

    - **\[IndexerName\]** – **indexerenus** など、作成するインデクサーの名前を指定します。
    - **\[DatasourceName\]** – **mycustomhelpdatasource** など、作成したデータ ソースの名前を指定します。
    - **\[IndexName\]** – **indexenus** など、作成したインデックスの名前を指定します。

    > [!NOTE]
    > このコンフィギュレーションでは、10 時間ごとに実行するようにスケジュールされたインデクサーを設定します (**"schedule" : { "interval" : "PT10H" }**)。 ただし、間隔は必要に応じて調整できます。

3. **送信** を選択し、**ステータス** フィールドが **201 Created** に設定されていることを確認します。
4. 複数の言語用のカスタム ヘルプ コンテンツを用意した場合、これらの手順を繰り返して、インデックスごとに固有のインデクサーを作成します。

> [!NOTE]
> インデックスには、インデクサーが実行された後にのみデータが含まれます。 インデックスをすぐにテストする場合は、インデクサーを手動で実行することができます。

> [!IMPORTANT]
> コンテンツを更新する場合は、JSON ファイルを再生成して、保管サービスにアップロードしてください。 コンテンツを追加する場合は、インデクサーを手動で実行するか、次のスケジュールされた実行を待つことができます。 更新されたコンテンツは、インデクサーが次に実行されるまで検索結果で利用できません。

オプションで、Postman を使用して検索をテストできます。 テストに Postman を使用する方法を示す例については、[JSON ファイルの検索](/azure/search/search-semi-structured-data#6---search-your-json-files) を参照してください。

## <a name="next-steps"></a>次のステップ

この記事のすべての手順を完了すると、ヘルプ コンテンツが Azure Web アプリ にアップロードされ、インデックスが作成されます。

次の手順では、コンテンツを検出できるように **ヘルプ** ウィンドウを拡張します。 このようにして、ユーザーが Dynamics 365 ソリューションの **ヘルプ** ウィンドウを開くと、製品内の **ヘルプ** ウィンドウは、ヘルプへの状況依存リンクを生成できます。 詳細については、[カスタム ヘルプ Web サイトを ヘルプ ウィンドウに接続する](connect-help-pane.md) を参照してください。

## <a name="see-also"></a>参照

[カスタム ヘルプの概要](custom-help-overview.md)  
[カスタム ヘルプ ツールキット](custom-help-toolkit.md)  
[製品およびヘルプの言語およびロケール記述子](language-locale.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
