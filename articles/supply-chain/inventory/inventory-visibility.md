---
title: 在庫の視覚化アドイン
description: このトピックでは、Dynamics 365 Supply Chain Management の在庫の視覚化アドインのインストールおよび構成方法を説明します。
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d09c7be5de75511b10d7a69d4b8ac12917b0dbe8
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910428"
---
# <a name="inventory-visibility-add-in"></a>在庫の視覚化アドイン

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Inventory Visibility Add-in は、リアルタイムで手持在庫を追跡可能できる独立したスケーラブルなマイクロサービスで、グローバルなビューの在庫表示が実現します。

手持在庫に関連するすべての情報は、低レベルの SQL 統合を通じて準リアルタイムでサービスにエクスポートされます。 外部システムは RESTful APIs を通じてサービスにアクセスし、指定された分析コードの組み合わせに関する手持在庫情報にクエリを実行します。こうすることで使用可能な手持在庫の一覧を取得することができます。

Inventory Visibility は、Microsoft Dataverse に構築されたマイクロサービスなので、Power Apps を構築および Power BI を適用することで拡張し、カスタマイズした機能を提供して、業務要件を満たすことができます。 インデックスをアップグレードして在庫クエリを実行することもできます。

Inventory Visibility には、複数のサードパーティ システムと統合できる構成オプションが用意されています。 このオプションでは、標準化された在庫分析コード、カスタマイズされた拡張性、標準化され構成可能な計算済の数量がサポートされます。

このトピックでは、Inventory Visibility Add-in for Dynamics 365 Supply Chain Management のインストールおよび構成方法、およびアプリケーション プログラミング インターフェイス (API) の使用方法について説明します。

## <a name="install-the-inventory-visibility-add-in"></a>Inventory Visibility Add-in をインストールする

Microsoft Dynamics Lifecycle Services (LCS) を使用して、 Inventory Visibility Add-in をインストールする必要があります。 LCS が提供する環境や定期的に更新されるサービスにより、Dynamics 365 Finance and Operations アプリのアプリケーション ライフサイクルを管理するのが楽になります。

詳細については、 [Lifecycle Services のリソース](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md) を参照してください。

### <a name="prerequisites"></a>必要条件

Inventory Visibility Add-in をインストールする前に、以下を実行する必要があります。

- 少なくとも 1 つの環境が配置されている LCS 実装プロジェクトを取得する。
- [アドインの概要](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)で提供されるアドインを設定するための前提条件が完了したことを確認します。 在庫の視覚化にデュアル書き込みリンクは必要ありません。
- [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) から在庫の視覚化チームに連絡して、次の 3 つの必要なファイルを入手してください。
    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - `Inventory Visibility Integration.zip` (実行している Supply Chain Management がバージョン 10.0.18 より以前のバージョンの場合)
- [クイック スタート: Microsoft ID プラットフォームにアプリケーションを登録](/azure/active-directory/develop/quickstart-register-app) の指示に従って、アプリケーションを登録し、Azure サブスクリプションで AAD にクライアント シークレットを起動します。
    - [アプリケーションを登録する](/azure/active-directory/develop/quickstart-register-app)
    - [クライアント シークレットの追加](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
    - **アプリケーション (クライアント) ID**、**クライアント シークレット** と **テナント ID** は次の手順でを使用されます。

> [!NOTE]
> 現在サポートされている国や地域には、カナダ、米国、欧州連合 (EU) が含まれます。

これらの前提条件について質問がある場合は、Inventory Visibility 製品チームに問い合わせてください。

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>Dataverse を設定する

Dataverse を設定するには、次の手順に従います。

1. テナントにサービス プリンシパルを追加します。

    1. [Graph 用 Azure Active Directory  PowerShell をインストールする](/powershell/azure/active-directory/install-adv2)に記載の手順に従って Azure AD PowerShell モジュール v2 をインストールします。
    1. 次の PowerShell コマンドを実行します。

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. Dataverse で在庫の視覚化のアプリケーション ユーザーを作成します。

    1. Dataverse 環境の URLを開きます。
    1. **詳細設定 \> システム \> セキュリティ \> ユーザー** の順に移動し、アプリケーション ユーザーを作成します。 表示メニューを使用して、ページ ビューを **アプリケーション ユーザー** に変更します。
    1. **新規** を選択します。 アプリケーション ID を *3022308a-b9bd-4a18-b8ac-2ddedb2075e1* に設定します。 (変更を保存すると、オブジェクト ID が自動的に読み込まれます。) 名前はカスタマイズできます。 たとえば、*在庫の視覚化* に変更できます。 完了したら、**保存** を選択します。
    1. **ロールの割り当て** を選択してから、**システム管理者** を選択します。 **Common Data Service ユーザー** という名前のロールがある場合は、それも選択します。

    詳細については、「[アプリケーション ユーザーの作成](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user)」を参照してください。

1. Dataverse の既定の言語が **英語** ではない場合:

    1. **詳細設定 \> 管理 \> 言語** に移動します、
    1. **英語 (LanguageCode=1033)** を選択し、**適用** を選択します。

1. Dataverse 構成関連エンティティと Power Apps を含む `Inventory Visibility Dataverse Solution.zip` ファイルをインポートします。

    1. **ソリューション** ページに移動します。
    1. **インポート** を選択します。

1. 構成のアップグレード トリガー フローをインポートします。

    1. Microsoft Flow ページに移動します。
    1. *Dataverse (レガシ)* という名前の接続が存在することを確認します。 (存在しない場合は作成します。)
    1. `Inventory Visibility Configuration Trigger.zip` ファイルをインポートします。 インポートすると、トリガーが **マイ フロー** の下に表示されます 。
    1. 環境情報に基づいて、次の 4 つの変数を初期化します。

        - Azure テナント ID
        - Azure アプリケーション クライアント ID
        - Azure アプリケーション クライアント シークレット
        - 在庫の視覚化エンドポイント

            この変数の詳細については、このトピックで後述する[在庫の視覚化統合の設定](#setup-inventory-visibility-integration) を参照してください。

        ![構成トリガー](media/configuration-trigger.png "構成トリガー")

    1. **有効化** を選択します。

### <a name="install-the-add-in"></a><a name="install-add-in"></a>アドインのインストール

Inventory Visibility Add-in をインストールするには、以下を実行する必要があります。

1. [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) ポータルにサインインします。
1. ホーム ページで、環境が展開されているプロジェクトを選択します。
1. プロジェクト ページで、アドインをインストールする環境を選択します。
1. 環境ページで、**Power Platform 統合** セクションの **環境アドイン** セクションが表示されるまで下にスクロールします。このセクションでは Dataverse 環境名を検索できます。
1. **環境アドイン** セクションで、**新しいアドインのインストール** を選択します。

    ![LCS の環境ページ](media/inventory-visibility-environment.png "LCS の環境ページ")

1. **新しいアドインのインストール** リンクを選択します。 使用可能なアドインの一覧が表示されます。
1. 一覧で **在庫の視覚化** を選択します。
1. 環境に対して次のフィールドの値を入力します。

    - **AAD アプリケーション (クライアント) ID**
    - **AAD テナント ID**

    ![セットアップ ページに追加](media/inventory-visibility-setup.png "アドイン セットアップ ページ")

1. **使用条件** チェック ボックスを選択して、使用条件に同意します。
1. **インストール** を選択します。 アドインの状態は、**インストール中** として表示されます。 完了したらページを更新して、状態が **インストール済み** に変わっているかを確認します。

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a>アドインのアンインストール

アドインをアンインストールするには、**アンインストール** を選択します。 LCS を更新すると、在庫の視覚化アドインが削除されます。 アンインストールのプロセスでは、アドイン登録が削除され、サービスに格納されているすべてのビジネス データをクリーンアップするジョブが開始されます。

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a>Supply Chain Management からの手持在庫データの消費

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>在庫の視覚化統合パッケージの配置

Supply Chain Management バージョン 10.0.17 以前を実行している場合、[inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) で在庫の視覚化のオンボード サポート チームに連絡してパッケージ ファイルを取得してください。 その後、LCS にパッケージを配置します。

> [!NOTE]
> 配置中にバージョンの不一致エラーが発生した場合は、X++ プロジェクトを手動で開発環境にインポートする必要があります。 その後、配置可能パッケージを開発環境に作成し、それを実稼働環境に配置します。
> 
> このコードは Supply Chain Management バージョン 10.0.18 に含まれています。 そのバージョン以降を実行する場合、配置は必須ではありません。

Supply Chain Management 環境で次の機能が有効になっていることを確認してください。 (既定では、有効になっています。)

| 機能の説明 | コード バージョン | トグル クラス |
|---|---|---|
| InventSum テーブルで在庫分析コードの使用の有効化または無効化 | 10.0.11 | InventUseDimOfInventSumToggle |
| InventSumDelta テーブルで在庫分析コードの使用の有効化または無効化 | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Inventory Visibility 統合の設定

1. Supply Chain Management で、**[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** ワークスペースを開き、在庫の可視性の **在庫の視覚化統合** 機能を有効にします。
1. **在庫管理 \> 設定 \>在庫の視覚化統合パラメーター** の順に移動し、実行している在庫の視覚化で環境の URL を入力します。

    LCS 環境の Azure リージョンを検索してから、URL を入力します。 URL には次のフォームがあります。

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    たとえば、ヨーロッパにいる場合、環境には次のいずれかの URL が表示されます。

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    現在、以下のリージョンが利用可能です。

    | Azure リージョン | リージョンの短縮名 |
    |---|---|
    | オーストラリア東部 | eau |
    | オーストラリア南東部 | seau |
    | カナダ中部 | cca |
    | カナダ東部 | eca |
    | 北ヨーロッパ | neu |
    | 西ヨーロッパ | weu |
    | 米国東部 | eus |
    | 米国西部 | wus |

1. **在庫管理 \> 定期処理 \> 在庫の視覚化統合** の順に移動し、ジョブを有効します。 Supply Chain Management からのすべての在庫変更イベントが在庫の視覚化に転記されるようになります。

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a>在庫の視覚化アドイン パブリック API

在庫の視覚化アドインのパブリック REST API は、特定の統合エンドポイントを複数提供します。 次の 3 つの主要な相互作用タイプをサポートします。

- 外部システムから、手持在庫の変更をアドインに転記する
- 外部システムから現在の手持在庫数量を問い合わせる
- Supply Chain Management 手持在庫との自動同期

自動同期はパブリック API の一部ではありません。 代わりに、在庫の視覚化アドインが有効になっている環境のバックグラウンドで処理されます。

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a>認証

プラットフォーム セキュリティ トークンは、在庫の視覚化アドインを呼び出すために使用されます。 したがって、Azure AD アプリケーションを使用して *Azure Active Directory (Azure AD) トークン* を生成する必要があります。 その後、この Azure AD トークンを使用して、セキュリティ サービスから *アクセス トークン* を取得する必要があります。

セキュリティ サービス トークンを取得するには、次の操作を行います。

1. Azure ポータルにサインインし、このサインインを使用して Supply Chain Management アプリケーションの `clientId` と `clientSecret` を検索します。
1. 次のプロパティを持つ HTTP 要求を送信することにより、 Azure Active Directory トークン (`aadToken`) をフェッチします。
    - **URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **メソッド** - `GET`
    - **本文の内容 (フォーム データ)**:

        | キー | 値 |
        | --- | --- |
        | クライアント ID | ${aadAppId} |
        | クライアント シークレット | ${aadAppSecret} |
        | 付与タイプ | client_credentials |
        | リソース | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
1. 応答で `aadToken` を受け取っている必要があります。これは次の例と似ています。

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "expires_on": "1610466645",
        "not_before": "1610462745",
        "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
        "access_token": "eyJ0eX...8WQ"
    }
    ```

1. 次に似た JSON 要求を形成します。

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    場所:
    - `client_assertion` 値は、前の手順で受け取った `aadToken` である必要があります。
    - この `context` 値は、アドインを配置する環境 ID である必要があります。
    - 例に示すように、他のすべての値を設定します。

1. 次のプロパティを使用して HTTP 要求を送信します。
    - **URL** - `https://securityservice.operations365.dynamics.com/token`
    - **メソッド** - `POST`
    - **HTTP ヘッダー** - API バージョンを含めます (キーは `Api-Version` で値は `1.0` です)
    - **本文の内容** - 前の手順で作成した JSON 要求を含めます。

1. `access_token` を取得します。 これは、Inventory Visibility API を呼び出すためのベアラー トークンとして必要なものです。 次に例を示します。

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a> サンプル要求

参考までに、ここにサンプルの http リクエストがあります。``Postman`` など、任意のツールまたはコーディング言語を使用してこの要求を送信できます。

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a>Inventory Visibility API の構成

このサービスを使用する前に、次のサブセクションで説明する構成を完了する必要があります。 環境の詳細によって、構成が異なる場合があります。 主に 4 つの部分から構成されます。

- [パーティション分割](#partitioning)
- [分析コードの構成](#dimension-configurations)
- [インデックスの作成中](#indexing)
- [カスタム測定](#custom-measurement)

#### <a name="partitioning"></a>パーティション分割

パーティション分割は、Inventory Visibility API のパフォーマンスに大きな影響を与える可能性があります。 有意義なデータ クエリの使用を妥協せずに、データを小規模にグループ化できるスキームを定義することをお勧めします。

`organizationId` (Supply Chain Management の `dataAreaId`) は、常にパーティション分割に含まれており、Inventory Visibility は既定で、*サイト + 場所* として分析コードごとのパーティション分割が設定されているので、 フィルターで定義された分析コードで、サービスを常にクエリを実行する必要があります。

> [!NOTE]
> *サイト* および *場所* は、Inventory Visibility で使用する 2 つの既定の標準分析コードです。 Supply Chain Management では、これらの分析コードは *サイト* ( `InventSiteId`) および *倉庫* (`InventLocationId`) と呼ばれます。

### <a name="dimension-configurations"></a>分析コードの構成

Inventory Visibility に既定の標準分析コードの一覧が用意されており、複数のソース システムの統合を有効にすることができます。

次のテーブルでは、Inventory Visibility で既定の分析コード名となる在庫分析コードを一覧表示しています。

| 分析コード タイプ | 分析コード名 |
|---|---|
| 品目 | `ColorId` |
| 品目 | `SizeId` |
| 品目 | `StyleId` |
| 品目 | `ConfigId` |
| 追跡 | `BatchId` |
| 追跡 | `SerialId` |
| 保管場所 | `LocationId` |
| 保管場所 | `SiteId` |
| 在庫状態 | `StatusId` |
| 倉庫固有 | `WMSLocationId` |
| 倉庫固有 | `WMSPalletId` |
| 倉庫固有 | `LicensePlateId` |

> [!NOTE]
> 前のテーブルで表示されていた分析コード タイプは、参照のみに使用されます。 Inventory Visibility で分析コード タイプを定義する必要はありません。

カスタム分析コードが存在し、Inventory Visibility で使用したときに既定値に送る必要がある場合は、Inventory Visibility で **カスタム分析コード** 名を構成できます。

RESTful APIs を使用して外部システムが Inventory Visibility へアクセスし、クエリを実行する特定の分析コードに関する手持在庫情報を入手できます。 統合に関しては、Inventory Visibility を使用すると、Inventory Visibility で *ターゲット分析コード* への *外部チャネル データソース* とソース分析コードを構成できるようになります。

ターゲット分析コードは、次のいずれかである必要があります。

- Inventory Visibility の既定分析コード
- カスタム分析コード

分析コードを構成する目的は、分析コードおよび分析コードを含む転記イベントに関するクエリで使用する複数のシステム統合を標準化することです。

#### <a name="indexing"></a>インデックスの作成中

ほとんどの場合、手持在庫クエリは、最高 "合計" レベルのみだけではなく、在庫分析コードに基づいて集計された結果も表示することができます。

Inventory Visibility を使用すると、分析コードまたは分析コードの組み合わせに基づいてインデックスを設定できるので、柔軟性を高めることができます。

> [!NOTE]
> 現在構成できるインデックスは、最大でわずか 5 つです。 業務上のニーズを満たすには、実装する前に、どの分析コードまたは分析コードの組み合わせを使用するかを慎重に検討する必要があります。 たとえば、次のように製品にクエリを実行します。

- *色* と *サイズ* の分析コード別に、集計された製品の手持在庫にクエリを実行します。
- 場合によっては、製品全体にクエリを実行します。

次のように定義されているインデックスが 2 つあるとします。

- `["ColorId", "SizeId"]`
- `[]`

空の括弧は、パーティションの製品 ID に基づいて集計されます。

インデックスは、`groupBy` クエリ設定に基づいた結果をどのようにグループ化できるかを定義します。 どの `groupBy` 値も定義しない場合、`productid` 別に合計が表示されます。 それ以外の場合は、`groupBy` を `groupBy=ColorId&groupBy=SizeId` として定義すると、システム内の異なる色とサイズの組み合わせに基づいて複数の明細行が返されます。

要求本文にクエリの基準を含めることができます。

色とサイズを組み合わせた製品のサンプル クエリです。

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

`filters` フィールドの場合、現在、`ProductId` のみが複数の値をサポートしています。 `ProductId` が空の配列の場合、すべての製品が照会されます。

#### <a name="custom-measurement"></a>カスタム測定

既定の測定数量は Supply Chain Management にリンクされています。 ただし、既定の測定値の組み合わせにより構成される数量が必要な場合があります。 そのためには、カスタム数量を構成し、手持在庫クエリの出力に追加します。

この機能により、追加または削除される一連の測定を定義して、カスタム測定を作成できるようになります。

たとえば、次のクエリ条件では、消費システムが使用できるように `MyCustomAvailableforReservation` としてカスタム測定数量を構成します。

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| 消費システム | 計算済測定 | データ ソース | モディファイアー | モディファイアーの計算タイプ |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | 追加 |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | 追加 |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | 減算 |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | 追加 |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | 減算 |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | 追加 |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | 追加 |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | 減算 |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | 減算 |

これを使用すると、カスタム測定数量に対するクエリが次の出力を返します。

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

`MyCustomAvailableforReservation` 出力は、次のようにカスタム測定の計算設定に基づいています。  
 *100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*

### <a name="posting-on-hand-changes"></a>手持在庫変更の転記

イベントが転記される正確な URL は、地理的領域によって異なります。 フォームを使用します。

`https://{serviceURL}/api/environment/{environmentId}/onhand`

認証されると、この URL を HTTP `POST` メソッドと一緒に使用し、手持在庫変更のイベントをサービスに送信することができます。

特別なヘッダーは、HTTP 要求を通じた Dynamics 365 サービスとの通信に使用され、データがリンクされている Supply Chain Management インスタンスの環境 ID を表しています。 例:

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a>手持在庫変更クエリの転記に関する例 1

この例では、Power Apps で分析コードの構成を設定するシナリオを紹介します。

次のクエリを使用して、Power Apps で分析コードのマッピングを構成します。

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

これで、クエリにある `dimensionDataSource` を指定してカスタム分析コード使用できます。 システムが、カスタム分析コードをベース分析コードに自動的に変換します。

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a>手持在庫変更クエリの転記に関する例 2

この例では、Power Apps で分析コードの構成に必要なマッピングが設定されていないシナリオを示します。この場合、転記する場合もベース分析コードを使用する必要があります。 `dimensionDataSource` フィールドが null 値、空白、または空白の場合は、すべての分析コードがベース分析コードである必要があります。

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a>JSON ドキュメント フィールド プロパティ

以前に例として説明した JSON クエリのフィールドには、次のテーブルに表示されているプロパティがあります。

| フィールド ID | 説明 |
|---|---|
| `id` | 特定の変更イベントの固有 ID。 この ID を使用してサービスとの通信が転記時に失敗した場合にイベントを再送信しても、同じイベントがシステムで 2 回カウントされることはありません。 |
| `organizationId` | イベントにリンクされている組織の ID。 これは、Supply Chain Management 組織またはデータ領域 ID にマップされます。 |
| `productId` | 問題の製品 ID。 |
| `quantity` | 手持在庫を変更する必要のある数量。 たとえば、新たにベーグルを棚に 10 個載せると、この値は 10 になります。 その後、ベーグルを 3 つ棚から取るか売れた場合、この値は 3 になります。 |
| `dimensionDataSource` | イベントやクエリ変更の転記で使用する分析コードのデータ ソース。 データ ソースを指定する場合は、指定されたデータ ソースのカスタム分析コードを使用できます。 分析コードの構成を使用して、Inventory Visibility はカスタム分析コードを既定の標準分析コードにマップできます。 `dimensionDataSource` が指定されていない場合は、クエリで既定の標準分析コードのみを使用できます。   |
| `dimensions` | キーと値のペアの動的なバッグ。 これらは、Supply Chain Management の一部の分析コードにマップされますが、イベントを Supply Chain Management または外部システムから取得した場合に表示されることがあるカスタム分析コード (*ソース* など) を追加することもできます。 |

### <a name="querying-current-on-hand"></a>現在の手持在庫に対するクエリの実行

現在の手持在庫に対してクエリを実行するためのエンドポイントは、次のような URL です。

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

HTTP `POST` メソッドでクエリが実行されます。

#### <a name="current-on-hand-query-example-1"></a>現在の手持在庫に対するクエリ例 1

この例では、Power Apps で分析コードの構成がすでに完了しているシナリオを紹介します。

次のクエリを使用して、Power Apps で分析コードのマッピングを構成します。

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

これで、クエリにある `dimensionDataSource` を指定してカスタム分析コード使用できます。 システムが、カスタム分析コードをベース分析コードに自動的に変換します。 `filters` で `DimensionDataSource` を指定し、`filters` および `groupByValues` の両方でカスタム分析コードを指定できます。 システムが、カスタム分析コードをベース分析コードに自動的に変換します。

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a>現在の手持在庫に対するクエリ例 2

この例では、Power Apps で分析コードの構成に必要なマッピングが設定されていないシナリオを示します。この場合、転記する場合もベース分析コードを使用する必要があります。 `filters` にある `dimensionDataSource` フィールドが null 値、空白、または空白の場合は、すべての分析コードがベース分析コードである必要があります。

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a>例: 返された結果

前の例のクエリを実行すると、次のような結果が返される場合があります。

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

"数量" フィールドは、測定とそれに関連付けられた値のディクショナリとして構成されています。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]