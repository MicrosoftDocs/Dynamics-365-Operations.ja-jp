---
title: "データ管理パッケージ REST API"
description: "このトピックでは、データ管理フレームワークのパッケージ REST API について説明します。"
author: Sunil-Garg
ms.date: 03/30/2018
manager: AnnBe
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2017-03-31
ms.dyn365.ops.version: Platform update 5
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 74e490696ac8e80fcba9011ff6846f87bb0753a3
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="data-management-package-rest-api"></a>データ管理パッケージ REST API

[!include [banner](../includes/banner.md)]

このトピックでは、データ管理フレームワークのパッケージ表現型状態移行 (REST) のアプリケーション プログラミング インターフェイス (API) について説明します。 パッケージ API を使用すると、データ パッケージを使用して、Microsoft Dynamics 365 for Finance and Operations と統合することができます。 REST API は、クラウドおよびオンプレミス展開の両方で使用できます。 オンプレミス配置については、現在この機能はバージョン 7.2、プラットフォーム更新プログラム 12、ビルド 7.0.4709.41184 以降で利用可能です。

オンプレミス サポートは追加されましたが、API の名前は変更されていないため、クラウドおよびオンプレミスの両方の展開は単一の API 設定で保持できます。

## <a name="choosing-an-integration-api"></a>統合 API の選択
Finance and Operations の 2 つの API は、データ管理フレームワークのパッケージ API と定期的な統合 API というファイル ベースの統合シナリオをサポートしています。 どちらの API もデータ インポート シナリオとデータ エクスポート シナリオの両方をサポートしています。 次のテーブルでは、使用する API を決定する際に考慮する必要がある主な決定事項について説明します。 

| 決定ポイント      | 定期統合 API | データ管理フレームワークのパッケージ API |
|---------------------|----------------------------|-----------------------------|
| スケジューリング          | Finance and Operations のスケジュール設定 | Finance and Operations 外でのスケジュール設定 |
| 書式設定              | ファイルおよびデータ パッケージ | データ パッケージのみ  |
| 変換      | データ ファイルが XML 形式の場合の Extensible Stylesheet Language Transformations (XSLT) のサポート | システム外部での変換 |
| サポートされているプロトコル | SOAP および REST | REST |
| サービス タイプ        | 顧客サービス | データ プロトコル (OData) アクションを開きます |
| 適用の対象        | 2016 年 2 月リリース (RTW) 以降 | プラットフォーム更新プログラム 5 以降  |

定期的な統合 API がデータ管理のフレームワーク パッケージ API の要件を満たしている場合、「[定期統合](recurring-integrations.md)」を参照します。 このトピックの残りの部分では、データ管理フレームワークのパッケージ API について説明します。

## <a name="authorization"></a>認証
データ管理フレームワークのパッケージ API は、アクセスを認可するために OAuth 2.0 を使用します。 API は、有効な OAuth アクセス トークンを使用して呼び出す必要があります。 OAuth 2.0 および Microsoft Azure Active Directory (Azure AD) に関する詳細については、[OAuth 2.0 および Azure Active Directory を使用してWeb アプリケーションへのアクセスを承認する](/azure/active-directory/develop/active-directory-protocols-oauth-code) を参照してください。 オンプレミス配置については、Active Directory フェデレーション サービス (AD FS) が認証に使用されます。 

> [!NOTE]
> クライアント資格情報の付与フローを使用すると、Finance and Operations はアクセス制御リストを保持します。 アクセス制御リストは **システム管理** > **設定** > **Azure Active Directory アプリケーション** で見つけることができます。 **Azure Active Directory アプリケーション** ページには、承認済クライアント ID と、クライアント資格情報付与フローを使用して API が呼び出されたときに適用する必要があるユーザー セキュリティ マッピングが表示されます。 オンプレミス配置については、このリストには AD FS からの有効なクライアント ID が必要です。

## <a name="import-apis"></a>API のインポート
ファイル (データ パッケージ) のインポートには、次の API が使用されます。

### <a name="getazurewritableurl"></a>GetAzureWritableUrl
**GetAzureWritableUrl** API は、書き込み可能な Blob URL を取得するために使用されます。 このメソッドには、URL に埋め込まれた共有アクセス署名 (SAS) トークンが含まれています。 この方法を使用すると、Finance and Operations の Azure Blob Storage コンテナーにデータ パッケージをアップロードすることができます。 オンプレミス配置については、この API はローカル ストレージに取り除かれた URL を引き続き返します。 

> [!NOTE]
> SAS は有効期限の時間枠中にのみ有効です。 ウィンドウが経過した後に発行されるすべての要求はエラーを返します。 詳細については、[共有アクセス署名 (SA) の使用](/azure/storage/common/storage-dotnet-shared-access-signature-part-1) を参照してください。

```CSharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetAzureWriteUrl
BODY
{
    "uniqueFileName":"<string>",
}
```

成功した応答の例を次に示します。

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "BlobId":"{<GUID>}",
        "BlobUrl":"https://<baseurl_id>.blob.core.windows.net/dmf/<uniqueFileName>?<SAS Token>"
    }
}
```

**入力パラメーター**

| パラメーター         | 説明  |
|-------------------|--------------|
| string packageUrl | BLOB ID を追跡するために使用される一意のファイル名。 一意のファイル名であることを保証するため、グローバル一意識別子 (GUID) を含めることができます。 |

**出力パラメータ**

| パラメーター      | 説明 |
|----------------|-------------|
| string BlobId  | 割り当てられた BLOB コンテナーの BLOB ID。 |
| string BlobUrl | 埋め込まれた SAS トークンを持つ URL。 URL を使用 して BLOB ストレージに書き込むことができます。 |


### <a name="importfrompackage"></a>ImportFromPackage
**ImportFromPackage** API は、Finance and Operations の実装に関連付けられている Azure Blob Storage にアップロードされるデータ パッケージからインポートを開始するために使用します。 オンプレミス配置については、ファイルが以前にアップロードされたローカル ストレージから、インポートが開始されます。

注記: プラットフォーム更新プログラム 12 を開始すると、ImportFromPackage は複合エンティティをサポートします。 ただし、パッケージで 1 つの複合エンティティのみを持つという制限があります。

```CSharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ImportFromPackage
BODY
{
    "packageUrl":"<string>",
    "definitionGroupId":"<string>",
    "executionId":"<string>",
    "execute":<bool>,
    "overwrite":<bool>,
    "legalEntityId":"<string>"
}
```

成功した応答の例を次に示します。

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"<executionId>"
    }
}
```

**入力パラメーター**

| パラメーター                | 説明 |
|--------------------------|-------------|
| string packageUrl        | Finance and Operations に関連付けられている Azure BLOB Storage 内のデータ パッケージの URL。 |
| string definitionGroupId | インポート用のデータ プロジェクトの名前。 |
| string executionId       | ジョブに使用する ID。 空の ID が割り当てられている場合は、新しい実行 ID が作成されます。 |
| bool execute             | このパラメーターを **True** に設定して対象の手順を実行します。 それ以外の場合、**False** に設定します。 |
| bool overwrite           | パッケージ内で複合エンティティを使用する場合は、常に **False** に設定する必要があります。 それ以外の場合、**True** に設定します。 |
| string legalEntityId     | データ インポートの法人。 |             

**出力パラメータ**

| パラメーター          | 説明  |
|--------------------|--------------|
| string executionId | データ インポートの実行 ID。 |

## <a name="export-apis"></a>API をエキスポート
ファイル (データ パッケージ) のエクスポートには、次の API が使用されます。

### <a name="exporttopackage"></a>ExportToPackage
**ExportToPackage** API は、データ パッケージのエクスポートを開始するために使用されます。 これは、クラウドとオンプレミスの両方の展開に適用されます。

- この API を呼び出す前に、エクスポート データ プロジェクトを Finance and Operations で作成する必要があります。 プロジェクトが存在しない場合、API の呼び出しには、エラーが返されます。
- 変更履歴がオンの場合は、最後の実行後に更新または作成されたレコードのみがエクスポートされます。 (つまり、デルタのみが返されます。)

```CSharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage
BODY
{
    "definitionGroupId":"<Data project Id>",
    "packageName":"<Name to use for downloaded file.>",
    "executionId":"<Execution Id if it is a rerun>",
    "reExecute":<bool>,
    "legalEntityId":"<Legal entity Id>"
}
```

成功した応答の例を次に示します。

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"<executionId>"
    }
}
```

**入力パラメーター**

| パラメーター                | 説明 |
|--------------------------|-------------|
| string definitionGroupId | エクスポート用のデータ プロジェクトの名前。 |
| string packageName       | エクスポートされたデータ パッケージの名前。 |
| string executionId       | ジョブに使用する ID。 空の ID が割り当てられている場合は、新しい実行 ID が作成されます。 |
| bool reExecute           | このパラメーターを **True** に設定して対象の手順を実行します。 それ以外の場合、**False** に設定します。 |
| string legalEntityId     | データ インポートの法人。 |
    
**出力パラメータ**

| パラメーター          | 説明 |
|--------------------|-------------|
| string executionId | データ エクスポートの実行 ID。 |

### <a name="getexportedpackageurl"></a>GetExportedPackageUrl
**GetExportedPackageUrl** API は、**ExportToPackage** を呼び出すことでエクスポートされたデータ パッケージの URL を取得するために使用されます。 これは、クラウドとオンプレミスの両方の展開に適用されます。

```CSharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
BODY
{"executionId":"<Execution Id>"}
```

成功した応答の例を次に示します。

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"https://<baseurl_id>.blob.core.windows.net/dmf/<uniqueFileName>?<SAS Token>"
    }
}
```

**入力パラメーター**

| パラメーター          | 説明 |
|--------------------|-------------|
| string executionId | データ プロジェクト実行の実行 ID。 |

**出力パラメータ**

| パラメーター      | 説明 |
|----------------|-------------|
| string BlobUrl | 埋め込みの SAS トークンを持つ blob URL。 URL を使用して、エクスポートしたデータ パッケージをダウンロードできます。 |

## <a name="status-check-api"></a>ステータス チェック API 
状態を確認するには、次の API を使用します。 これらは、インポート フローとエクスポート フローの両方で使用されます。

### <a name="getexecutionsummarystatus"></a>GetExecutionSummaryStatus
**GetExecutionSummaryStatus** API は、データ プロジェクト実行ジョブのステータスを確認するためにインポート ジョブおよびエクスポート ジョブの両方に使用されます。 これは、クラウドとオンプレミスの両方の展開に適用されます。

```CSharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
BODY
{"executionId":"<executionId>"}
```

成功した応答の例を次に示します。

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"<executionStatus>"
    }
}
```

**入力パラメーター**

| パラメーター          | 説明 |
|--------------------|-------------|
| string executionId | データ プロジェクト実行の実行 ID。 |

**出力パラメータ**

| パラメーター                                 | 説明 |
|-------------------------------------------|-------------|
| DMFExecutionSummaryStatus executionStatus | 実行のステータス。 |

実行状態の使用可能な値を次に示します。

- 不明
- NotRun
- 実行
- 成功
- PartiallySucceeded
- 失敗
- 取消済 

## <a name="import-and-export-processes"></a>プロセスのインポートとエクスポート 
次の図は、データ管理パッケージ メソッドを使用してデータ パッケージをインポートする方法を示しています。

![データ管理パッケージ メソッドを使用するデータ パッケージ ファイルのインポート](./media/data-package-import.png)
 
次の図は、データ管理パッケージ メソッドを使用してデータ パッケージをエクスポートする方法を示しています。

![管理パッケージ メソッドを使用するデータ パッケージ ファイルのエクスポート](./media/data-package-export.png)
 
サンプル コンソール アプリケーションは、データのインポートとデータのエクスポートのメソッドを紹介する GitHub から入手できます。 詳細については、「<https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/FileBasedIntegrationSamples/ConsoleAppSamples>」に移動してください。

