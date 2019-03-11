---
title: データ管理パッケージ REST API
description: このトピックでは、データ管理フレームワークのパッケージ REST API について説明します。
author: Sunil-Garg
ms.date: 12/26/2018
manager: AnnBe
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2017-03-31
ms.dyn365.ops.version: Platform update 5
ms.openlocfilehash: b705a7b3004c75d6dbc2a407fc24dbed0bec043f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369816"
---
# <a name="data-management-package-rest-api"></a><span data-ttu-id="97fd3-103">データ管理パッケージ REST API</span><span class="sxs-lookup"><span data-stu-id="97fd3-103">Data management package REST API</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97fd3-104">このトピックでは、データ管理フレームワークのパッケージの Representational State Transfer (REST) のアプリケーション プログラミング インターフェイス (API) について説明します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-104">This topic describes the Data management framework's package representational state transfer (REST) application programming interface (API).</span></span> <span data-ttu-id="97fd3-105">パッケージ API により、データ パッケージを使用して Microsoft Dynamics 365 for Finance and Operations と統合できます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-105">The package API lets you integrate with Microsoft Dynamics 365 for Finance and Operations by using data packages.</span></span> <span data-ttu-id="97fd3-106">REST API は、クラウド配置とオンプレミス配置の両方で使用できます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-106">The REST API can be used with both cloud deployments and on-premises deployments.</span></span> <span data-ttu-id="97fd3-107">オンプレミス配置では、現在この機能は、Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition プラットフォーム更新プログラム 12 (2017 年 11 月) (バージョン 7.2)、ビルド 7.0.4709.41184 以降で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="97fd3-107">For on-premises deployments, this functionality is currently available for Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with platform update 12 (November 2017) (version 7.2), build 7.0.4709.41184, and later.</span></span>

<span data-ttu-id="97fd3-108">オンプレミス サポートが追加されましたが、API 名は変更されていません。</span><span class="sxs-lookup"><span data-stu-id="97fd3-108">Although on-premises support has been added, API names haven't been changed.</span></span> <span data-ttu-id="97fd3-109">したがって、Microsoft は、クラウド配置とオンプレミス配置の両方に対して単一の API セットを維持することができます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-109">Therefore, Microsoft can keep a single API set for both cloud deployments and on-premises deployments.</span></span>

## <a name="choosing-an-integration-api"></a><span data-ttu-id="97fd3-110">統合 API の選択</span><span class="sxs-lookup"><span data-stu-id="97fd3-110">Choosing an integration API</span></span>

<span data-ttu-id="97fd3-111">Finance and Operations の 2 つの API である、データ管理フレームワークのパッケージ API と定期的な統合 API が、ファイル ベースの統合シナリオをサポートします。</span><span class="sxs-lookup"><span data-stu-id="97fd3-111">Two APIs in Finance and Operations support file-based integration scenarios: the Data management framework's package API and the recurring integrations API.</span></span> <span data-ttu-id="97fd3-112">どちらの API もデータ インポート シナリオとデータ エクスポート シナリオの両方をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="97fd3-112">Both APIs support both data import scenarios and data export scenarios.</span></span> <span data-ttu-id="97fd3-113">次のテーブルでは、使用する API を決定する際に考慮する必要がある主な決定事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-113">The following table describes the main decision points that you should consider when you're trying to decide which API to use.</span></span>

| <span data-ttu-id="97fd3-114">決定ポイント</span><span class="sxs-lookup"><span data-stu-id="97fd3-114">Decision point</span></span>      | <span data-ttu-id="97fd3-115">定期統合 API</span><span class="sxs-lookup"><span data-stu-id="97fd3-115">Recurring integrations API</span></span> | <span data-ttu-id="97fd3-116">データ管理フレームワークのパッケージ API</span><span class="sxs-lookup"><span data-stu-id="97fd3-116">Data management framework's package API</span></span> |
|---------------------|--------------------------------------|-----------------------------|
| <span data-ttu-id="97fd3-117">スケジューリング</span><span class="sxs-lookup"><span data-stu-id="97fd3-117">Scheduling</span></span>          | <span data-ttu-id="97fd3-118">Finance and Operations のスケジュール設定</span><span class="sxs-lookup"><span data-stu-id="97fd3-118">Scheduling in Finance and Operations</span></span> | <span data-ttu-id="97fd3-119">Finance and Operations 外でのスケジュール設定</span><span class="sxs-lookup"><span data-stu-id="97fd3-119">Scheduling outside Finance and Operations</span></span> |
| <span data-ttu-id="97fd3-120">書式設定</span><span class="sxs-lookup"><span data-stu-id="97fd3-120">Format</span></span>              | <span data-ttu-id="97fd3-121">ファイルおよびデータ パッケージ</span><span class="sxs-lookup"><span data-stu-id="97fd3-121">Files and data packages</span></span> | <span data-ttu-id="97fd3-122">データ パッケージのみ</span><span class="sxs-lookup"><span data-stu-id="97fd3-122">Only data packages</span></span> |
| <span data-ttu-id="97fd3-123">変換</span><span class="sxs-lookup"><span data-stu-id="97fd3-123">Transformation</span></span>      | <span data-ttu-id="97fd3-124">データ ファイルが XML 形式の場合の Extensible Stylesheet Language Transformations (XSLT) のサポート</span><span class="sxs-lookup"><span data-stu-id="97fd3-124">Support for Extensible Stylesheet Language Transformations (XSLT) if the data file is in XML format</span></span> | <span data-ttu-id="97fd3-125">システム外部での変換</span><span class="sxs-lookup"><span data-stu-id="97fd3-125">Transformations that are external to the system</span></span> |
| <span data-ttu-id="97fd3-126">サポートされているプロトコル</span><span class="sxs-lookup"><span data-stu-id="97fd3-126">Supported protocols</span></span> | <span data-ttu-id="97fd3-127">SOAP および REST</span><span class="sxs-lookup"><span data-stu-id="97fd3-127">SOAP and REST</span></span> | <span data-ttu-id="97fd3-128">REST</span><span class="sxs-lookup"><span data-stu-id="97fd3-128">REST</span></span> |
| <span data-ttu-id="97fd3-129">サービス タイプ</span><span class="sxs-lookup"><span data-stu-id="97fd3-129">Service type</span></span>        | <span data-ttu-id="97fd3-130">顧客サービス</span><span class="sxs-lookup"><span data-stu-id="97fd3-130">Custom service</span></span> | <span data-ttu-id="97fd3-131">データ プロトコル (OData) アクションを開きます</span><span class="sxs-lookup"><span data-stu-id="97fd3-131">Open Data Protocol (OData) action</span></span> |
| <span data-ttu-id="97fd3-132">在庫状態</span><span class="sxs-lookup"><span data-stu-id="97fd3-132">Availability</span></span>        | <span data-ttu-id="97fd3-133">Microsoft Dynamics AX 7.0 (2016 年 2 月) (RTW) およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="97fd3-133">Microsoft Dynamics AX 7.0 (February 2016) (RTW) and later</span></span> | <span data-ttu-id="97fd3-134">Microsoft Dynamics 365 for Operations プラットフォーム更新プログラム 5 (2017 年 3 月) およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="97fd3-134">Microsoft Dynamics 365 for Operations with platform update 5 (March 2017) and later</span></span> |

<span data-ttu-id="97fd3-135">定期的な統合 API がデータ管理フレームワークのパッケージ API よりも要件を満たしていることを決定した場合、[定期統合](recurring-integrations.md) を参照します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-135">If you decide that the recurring integrations API meets your requirement better than the Data management framework's package API, see [Recurring integrations](recurring-integrations.md).</span></span> <span data-ttu-id="97fd3-136">このトピックの残りの部分では、データ管理フレームワークのパッケージ API について説明します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-136">The rest of this topic discusses the Data management framework's package API.</span></span>

## <a name="authorization"></a><span data-ttu-id="97fd3-137">承認</span><span class="sxs-lookup"><span data-stu-id="97fd3-137">Authorization</span></span>

<span data-ttu-id="97fd3-138">データ管理フレームワークのパッケージ API は、アクセスを認可するために OAuth 2.0 を使用します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-138">The Data management framework's package API uses OAuth 2.0 to authorize access.</span></span> <span data-ttu-id="97fd3-139">API は、有効な OAuth アクセス トークンを使用して呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="97fd3-139">The API must be called by using a valid OAuth access token.</span></span> <span data-ttu-id="97fd3-140">OAuth 2.0 および Microsoft Azure Active Directory(Azure AD) の詳細については、[OAuth 2.0 と Azure Active Directory を使用して Web アプリケーションへのアクセスを承認](/azure/active-directory/develop/active-directory-protocols-oauth-code) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="97fd3-140">For more information about OAuth 2.0 and Microsoft Azure Active Directory (Azure AD), see [Authorize access to web applications using OAuth 2.0 and Azure Active Directory](/azure/active-directory/develop/active-directory-protocols-oauth-code).</span></span> <span data-ttu-id="97fd3-141">オンプレミス配置では、Active Directory フェデレーション サービス (AD FS) が承認に使用されます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-141">For on-premises deployments, Active Directory Federation Services (AD FS) is used for authorization.</span></span>

> [!NOTE]
> <span data-ttu-id="97fd3-142">クライアント資格情報の付与フローを使用すると、Finance and Operations はアクセス制御リストを保持します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-142">When you use the Client Credentials Grant flow, Finance and Operations maintains an access control list.</span></span> <span data-ttu-id="97fd3-143">アクセス制御リストは、**システム管理** \> **設定** \> **Azure Active Directory アプリケーション** を順にクリックして見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-143">You can find the access control list at **System administration** \> **Setup** \> **Azure Active Directory applications**.</span></span> <span data-ttu-id="97fd3-144">**Azure Active Directory アプリケーション** ページには、承認済クライアント ID と、クライアント資格情報付与フローを使用して API が呼び出されたときに適用する必要があるユーザー セキュリティ マッピングが表示されます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-144">The **Azure Active Directory applications** page shows the approved client IDs and the user security mapping that should be enforced when the API is called by using the Client Credentials Grant flow.</span></span>
>
> <span data-ttu-id="97fd3-145">オンプレミス配置については、このリストには AD FS からの有効なクライアント ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="97fd3-145">For on-premises deployments, this list must have a valid client ID from AD FS.</span></span> <span data-ttu-id="97fd3-146">また、オンプレミスでの使用の場合、Finance and Operations に接続するとき、次の例の **\<baseurl\>** に **/namespaces/AXSF** を付加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97fd3-146">Additionally, for on-premises use, **\<baseurl\>** in the following examples must append **/namespaces/AXSF** when a connection is made to Finance and Operations.</span></span>

## <a name="import-apis"></a><span data-ttu-id="97fd3-147">API のインポート</span><span class="sxs-lookup"><span data-stu-id="97fd3-147">Import APIs</span></span>

<span data-ttu-id="97fd3-148">ファイル (データ パッケージ) のインポートには、次の API が使用されます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-148">The following APIs are used to import files (data packages).</span></span>

### <a name="getimporttargeterrorkeysfileurl"></a><span data-ttu-id="97fd3-149">GetImportTargetErrorKeysFileUrl</span><span class="sxs-lookup"><span data-stu-id="97fd3-149">GetImportTargetErrorKeysFileUrl</span></span>

<span data-ttu-id="97fd3-150">**GetImportTargetErrorKeysFileUrl** API を使用して、単一のエンティティに対するインポートのステージングからターゲットへのステップで失敗したインポート レコードのキーが格納されているエラー ファイルの URL を取得します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-150">The **GetImportTargetErrorKeysFileUrl** API is used to get the URL of the error file that contains the keys of the import records that failed at the staging-to-target step of import for a single entity.</span></span>

<span data-ttu-id="97fd3-151">エラー ファイルが使用可能な場合、この API はその URL を返します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-151">If the error file is available, this API returns the URL.</span></span> <span data-ttu-id="97fd3-152">エラー ファイルがまだ生成中の場合、またはエラー ファイルが存在しない場合は、API は空の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-152">If the error file is still being generated, or if there is no error file, the API returns an empty string.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="97fd3-153">この API を呼び出す前に、**GenerateImportTargetErrorKeysFile** API を呼出して、エラー ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-153">Before you call this API, call the **GenerateImportTargetErrorKeysFile** API to generate the error file.</span></span> <span data-ttu-id="97fd3-154">**GenerateImportTargetErrorKeysFile** API が **true** を返した場合、空でない文字列が返されるまで、ループでこの API を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-154">If the **GenerateImportTargetErrorKeysFile** API returns **true**, call this API in a loop until it returns a non-empty string.</span></span> <span data-ttu-id="97fd3-155">**GenerateImportTargetErrorKeysFile** API が **false** を返した場合、エラーがないため、この API は空の文字列をかならず返します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-155">If the **GenerateImportTargetErrorKeysFile** API returns **false**, this API will always return an empty string, because there are no errors.</span></span>

<span data-ttu-id="97fd3-156">**疑似コードの例**</span><span class="sxs-lookup"><span data-stu-id="97fd3-156">**Pseudocode example**</span></span>

```
errorsExist = GenerateImportTargetErrorKeysFile(executionId, entityName)

if (errorsExist)
{
    errorFileUrl = null

    while (errorFileUrl is not a non-empty string)
    {
        errorFileUrl = GetImportTargetErrorKeysFileUrl(executionId, entityName)
        if (errorFileUrl is not a non-empty string)
        {
            wait for some time before retrying
        }
    }
}
```

```CSharp
POST
/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetImportTargetErrorKeysFileUrl

Body
{
    "executionId":"<string>",
    "entityName":"<string>"
}
```

<span data-ttu-id="97fd3-157">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-157">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":"<errorkeysfileurl>"
}
```

<span data-ttu-id="97fd3-158">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="97fd3-158">**Input parameters**</span></span>

| <span data-ttu-id="97fd3-159">パラメーター</span><span class="sxs-lookup"><span data-stu-id="97fd3-159">Parameter</span></span>         | <span data-ttu-id="97fd3-160">説明</span><span class="sxs-lookup"><span data-stu-id="97fd3-160">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="97fd3-161">string executionId</span><span class="sxs-lookup"><span data-stu-id="97fd3-161">string executionId</span></span> | <span data-ttu-id="97fd3-162">インポートの実行 ID。</span><span class="sxs-lookup"><span data-stu-id="97fd3-162">The execution ID of the import.</span></span> |
| <span data-ttu-id="97fd3-163">string entityName</span><span class="sxs-lookup"><span data-stu-id="97fd3-163">string entityName</span></span> | <span data-ttu-id="97fd3-164">エラー ファイルを取得する対象のエンティティの名前。</span><span class="sxs-lookup"><span data-stu-id="97fd3-164">The name of the entity to get the error file for.</span></span> |

<span data-ttu-id="97fd3-165">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="97fd3-165">**Output parameters**</span></span>

| <span data-ttu-id="97fd3-166">パラメーター</span><span class="sxs-lookup"><span data-stu-id="97fd3-166">Parameter</span></span>         | <span data-ttu-id="97fd3-167">説明</span><span class="sxs-lookup"><span data-stu-id="97fd3-167">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="97fd3-168">string errorkeysfileurl</span><span class="sxs-lookup"><span data-stu-id="97fd3-168">string errorkeysfileurl</span></span> | <span data-ttu-id="97fd3-169">エラー キー ファイルが使用可能な場合、そのファイルの URL。</span><span class="sxs-lookup"><span data-stu-id="97fd3-169">The URL of the error keys file, if the file is available.</span></span> <span data-ttu-id="97fd3-170">エラー ファイルがまだ生成中の場合、またはエラー ファイルが存在しない場合は、このメソッドは空の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-170">If the error file is still being generated, or if no errors exist, the method returns an empty string.</span></span> |

### <a name="getazurewritableurl"></a><span data-ttu-id="97fd3-171">GetAzureWritableUrl</span><span class="sxs-lookup"><span data-stu-id="97fd3-171">GetAzureWritableUrl</span></span>

<span data-ttu-id="97fd3-172">**GetAzureWritableUrl** API は、書き込み可能な Blob URL を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-172">The **GetAzureWritableUrl** API is used to get a writable blob URL.</span></span> <span data-ttu-id="97fd3-173">このメソッドには、URL に埋め込まれた共有アクセス署名 (SAS) トークンが含まれています。</span><span class="sxs-lookup"><span data-stu-id="97fd3-173">The method includes a shared access signature (SAS) token that is embedded in the URL.</span></span> <span data-ttu-id="97fd3-174">この方法を使用すると、Finance and Operations の Azure Blob Storage コンテナーにデータ パッケージをアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-174">You can use this method to upload a data package to the Azure Blob storage container for Finance and Operations.</span></span> <span data-ttu-id="97fd3-175">オンプレミス配置の場合、この API はローカル ストレージに取り込まれた URL を引き続き返します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-175">For on-premises deployments, this API will still return the URL that has been abstracted to local storage.</span></span>

> [!NOTE]
> <span data-ttu-id="97fd3-176">SAS は有効期限の時間枠中にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="97fd3-176">An SAS is valid only during an expiry time window.</span></span> <span data-ttu-id="97fd3-177">ウィンドウが経過した後に発行されるすべての要求はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-177">Any request that is issued after the window has passed returns an error.</span></span> <span data-ttu-id="97fd3-178">詳細については、[共有アクセス署名 (SA) の使用](/azure/storage/common/storage-dotnet-shared-access-signature-part-1) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="97fd3-178">For more information, see [Using shared access signatures (SAS)](/azure/storage/common/storage-dotnet-shared-access-signature-part-1).</span></span>

```CSharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetAzureWriteUrl
BODY
{
    "uniqueFileName":"<string>",
}
```

<span data-ttu-id="97fd3-179">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-179">Here is an example of a successful response.</span></span>

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

<span data-ttu-id="97fd3-180">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="97fd3-180">**Input parameters**</span></span>

| <span data-ttu-id="97fd3-181">パラメーター</span><span class="sxs-lookup"><span data-stu-id="97fd3-181">Parameter</span></span>         | <span data-ttu-id="97fd3-182">説明</span><span class="sxs-lookup"><span data-stu-id="97fd3-182">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="97fd3-183">string packageUrl</span><span class="sxs-lookup"><span data-stu-id="97fd3-183">string packageUrl</span></span> | <span data-ttu-id="97fd3-184">BLOB ID を追跡するために使用される一意のファイル名。</span><span class="sxs-lookup"><span data-stu-id="97fd3-184">A unique file name that is used to track blob IDs.</span></span> <span data-ttu-id="97fd3-185">一意のファイル名であることを保証するため、グローバル一意識別子 (GUID) を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-185">You can include a globally unique identifier (GUID) to help guarantee a unique file name.</span></span> |

<span data-ttu-id="97fd3-186">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="97fd3-186">**Output parameters**</span></span>

| <span data-ttu-id="97fd3-187">パラメーター</span><span class="sxs-lookup"><span data-stu-id="97fd3-187">Parameter</span></span>      | <span data-ttu-id="97fd3-188">説明</span><span class="sxs-lookup"><span data-stu-id="97fd3-188">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="97fd3-189">string BlobId</span><span class="sxs-lookup"><span data-stu-id="97fd3-189">string BlobId</span></span>  | <span data-ttu-id="97fd3-190">割り当てられた BLOB コンテナーの BLOB ID。</span><span class="sxs-lookup"><span data-stu-id="97fd3-190">The blob ID of the allocated blob container.</span></span> |
| <span data-ttu-id="97fd3-191">string BlobUrl</span><span class="sxs-lookup"><span data-stu-id="97fd3-191">string BlobUrl</span></span> | <span data-ttu-id="97fd3-192">埋め込みの SAS トークンを持つ URL。</span><span class="sxs-lookup"><span data-stu-id="97fd3-192">A URL that has an embedded SAS token.</span></span> <span data-ttu-id="97fd3-193">URL を使用 して Blob ストレージに書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-193">The URL can be used to write to Blob storage.</span></span> |

### <a name="importfrompackage"></a><span data-ttu-id="97fd3-194">ImportFromPackage</span><span class="sxs-lookup"><span data-stu-id="97fd3-194">ImportFromPackage</span></span>

<span data-ttu-id="97fd3-195">**ImportFromPackage** API は、Finance and Operations の実装に関連付けられている Blob ストレージにアップロードされるデータ パッケージからインポートを開始するために使用します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-195">The **ImportFromPackage** API is used to initiate an import from the data package that is uploaded to the Blob storage that is associated with your implementation of Finance and Operations.</span></span> <span data-ttu-id="97fd3-196">オンプレミス配置の場合、ファイルが以前アップロードされたローカル ストレージから、インポートが開始されます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-196">For on-premises deployments, the import will be initiated from the local storage that the file was uploaded previously to.</span></span>

> [!NOTE]
> <span data-ttu-id="97fd3-197">プラットフォーム更新プログラム 12 を起動すると、**ImportFromPackage** API は複合エンティティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="97fd3-197">Starting in Platform update 12, the **ImportFromPackage** API supports composite entities.</span></span> <span data-ttu-id="97fd3-198">ただし、1 つのパッケージで 1 つの複合エンティティのみという制限があります。</span><span class="sxs-lookup"><span data-stu-id="97fd3-198">However, the limitation is that there can be only one composite entity in a package.</span></span>

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

<span data-ttu-id="97fd3-199">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-199">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"<executionId>"
    }
}
```

<span data-ttu-id="97fd3-200">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="97fd3-200">**Input parameters**</span></span>

| <span data-ttu-id="97fd3-201">パラメーター</span><span class="sxs-lookup"><span data-stu-id="97fd3-201">Parameter</span></span>                | <span data-ttu-id="97fd3-202">説明</span><span class="sxs-lookup"><span data-stu-id="97fd3-202">Description</span></span> |
|--------------------------|-------------|
| <span data-ttu-id="97fd3-203">string packageUrl</span><span class="sxs-lookup"><span data-stu-id="97fd3-203">string packageUrl</span></span>        | <span data-ttu-id="97fd3-204">Finance and Operations に関連付けられている Blob Storage 内のデータ パッケージの URL。</span><span class="sxs-lookup"><span data-stu-id="97fd3-204">The URL of the data package in the Blob storage that is associated with Finance and Operations.</span></span> |
| <span data-ttu-id="97fd3-205">string definitionGroupId</span><span class="sxs-lookup"><span data-stu-id="97fd3-205">string definitionGroupId</span></span> | <span data-ttu-id="97fd3-206">インポート用のデータ プロジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="97fd3-206">The name of the data project for import.</span></span> |
| <span data-ttu-id="97fd3-207">string executionId</span><span class="sxs-lookup"><span data-stu-id="97fd3-207">string executionId</span></span>       | <span data-ttu-id="97fd3-208">ジョブに使用する ID。</span><span class="sxs-lookup"><span data-stu-id="97fd3-208">The ID to use for the job.</span></span> <span data-ttu-id="97fd3-209">空の ID が割り当てられている場合は、新しい実行 ID が作成されます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-209">If an empty ID is assigned, a new execution ID will be created.</span></span> |
| <span data-ttu-id="97fd3-210">bool execute</span><span class="sxs-lookup"><span data-stu-id="97fd3-210">bool execute</span></span>             | <span data-ttu-id="97fd3-211">このパラメーターを **True** に設定して対象の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-211">Set this parameter to **True** to run the target step.</span></span> <span data-ttu-id="97fd3-212">それ以外の場合、**False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-212">Otherwise, set it to **False**.</span></span> |
| <span data-ttu-id="97fd3-213">bool overwrite</span><span class="sxs-lookup"><span data-stu-id="97fd3-213">bool overwrite</span></span>           | <span data-ttu-id="97fd3-214">パッケージ内で複合エンティティを使用する場合は、このパラメーターを常に **False** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97fd3-214">This parameter must always be set to **False** when a composite entity is used in a package.</span></span> <span data-ttu-id="97fd3-215">それ以外の場合、**True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-215">Otherwise, set it to **True**.</span></span> |
| <span data-ttu-id="97fd3-216">string legalEntityId</span><span class="sxs-lookup"><span data-stu-id="97fd3-216">string legalEntityId</span></span>     | <span data-ttu-id="97fd3-217">データ インポートの法人。</span><span class="sxs-lookup"><span data-stu-id="97fd3-217">The legal entity for the data import.</span></span> |

<span data-ttu-id="97fd3-218">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="97fd3-218">**Output parameters**</span></span>

| <span data-ttu-id="97fd3-219">パラメーター</span><span class="sxs-lookup"><span data-stu-id="97fd3-219">Parameter</span></span>          | <span data-ttu-id="97fd3-220">説明</span><span class="sxs-lookup"><span data-stu-id="97fd3-220">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="97fd3-221">string executionId</span><span class="sxs-lookup"><span data-stu-id="97fd3-221">string executionId</span></span> | <span data-ttu-id="97fd3-222">データ インポートの実行 ID。</span><span class="sxs-lookup"><span data-stu-id="97fd3-222">The execution ID of the data import.</span></span> |

> [!NOTE]
> <span data-ttu-id="97fd3-223">**ImportFromPackage()** はバッチを使用してインポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-223">**ImportFromPackage()** uses a batch to perform the import.</span></span> <span data-ttu-id="97fd3-224">したがって、並行インポートを実行するために、データ管理で並列処理ルールを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97fd3-224">Therefore, parallel processing rules must be used in Data management to perform parallel imports.</span></span> <span data-ttu-id="97fd3-225">**ImportFromPackage()** を並列スレッドで呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="97fd3-225">**ImportFromPackage()** must not be called in parallel threads.</span></span> <span data-ttu-id="97fd3-226">それ以外の場合、これは失敗します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-226">Otherwise, it will fail.</span></span>

## <a name="export-apis"></a><span data-ttu-id="97fd3-227">API をエキスポート</span><span class="sxs-lookup"><span data-stu-id="97fd3-227">Export APIs</span></span>

<span data-ttu-id="97fd3-228">ファイル (データ パッケージ) のエクスポートには、次の API が使用されます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-228">The following APIs are used to export files (data packages).</span></span>

### <a name="exporttopackage"></a><span data-ttu-id="97fd3-229">ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="97fd3-229">ExportToPackage</span></span>

<span data-ttu-id="97fd3-230">**ExportToPackage** API は、データ パッケージのエクスポートを開始するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-230">The **ExportToPackage** API is used to initiate an export of a data package.</span></span> <span data-ttu-id="97fd3-231">この API は、クラウド配置とオンプレミス配置の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-231">This API is applicable to both cloud deployments and on-premises deployments.</span></span>

- <span data-ttu-id="97fd3-232">この API を呼び出す前に、エクスポート データ プロジェクトを Finance and Operations で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97fd3-232">The export data project must be created in Finance and Operations before you call this API.</span></span> <span data-ttu-id="97fd3-233">プロジェクトが存在しない場合、API の呼び出しには、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-233">If the project doesn't exist, a call to the API returns an error.</span></span>
- <span data-ttu-id="97fd3-234">変更履歴がオンの場合は、最後の実行後に更新または作成されたレコードのみがエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-234">If change tracking has been turned on, only records that have been created or updated since the last run are exported.</span></span> <span data-ttu-id="97fd3-235">(つまり、デルタのみが返されます。)</span><span class="sxs-lookup"><span data-stu-id="97fd3-235">(In other words, only the delta is returned.)</span></span>

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

<span data-ttu-id="97fd3-236">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-236">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"<executionId>"
    }
}
```

<span data-ttu-id="97fd3-237">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="97fd3-237">**Input parameters**</span></span>

| <span data-ttu-id="97fd3-238">パラメーター</span><span class="sxs-lookup"><span data-stu-id="97fd3-238">Parameter</span></span>                | <span data-ttu-id="97fd3-239">説明</span><span class="sxs-lookup"><span data-stu-id="97fd3-239">Description</span></span> |
|--------------------------|-------------|
| <span data-ttu-id="97fd3-240">string definitionGroupId</span><span class="sxs-lookup"><span data-stu-id="97fd3-240">string definitionGroupId</span></span> | <span data-ttu-id="97fd3-241">エクスポート用のデータ プロジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="97fd3-241">The name of the data project for export.</span></span> |
| <span data-ttu-id="97fd3-242">string packageName</span><span class="sxs-lookup"><span data-stu-id="97fd3-242">string packageName</span></span>       | <span data-ttu-id="97fd3-243">エクスポートされたデータ パッケージの名前。</span><span class="sxs-lookup"><span data-stu-id="97fd3-243">The name of the exported data package.</span></span> |
| <span data-ttu-id="97fd3-244">string executionId</span><span class="sxs-lookup"><span data-stu-id="97fd3-244">string executionId</span></span>       | <span data-ttu-id="97fd3-245">ジョブに使用する ID。</span><span class="sxs-lookup"><span data-stu-id="97fd3-245">The ID to use for the job.</span></span> <span data-ttu-id="97fd3-246">空の ID が割り当てられている場合は、新しい実行 ID が作成されます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-246">If an empty ID is assigned, a new execution ID will be created.</span></span> |
| <span data-ttu-id="97fd3-247">bool reExecute</span><span class="sxs-lookup"><span data-stu-id="97fd3-247">bool reExecute</span></span>           | <span data-ttu-id="97fd3-248">このパラメーターを **True** に設定して対象の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-248">Set this parameter to **True** to run the target step.</span></span> <span data-ttu-id="97fd3-249">それ以外の場合、**False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-249">Otherwise, set it to **False**.</span></span> |
| <span data-ttu-id="97fd3-250">string legalEntityId</span><span class="sxs-lookup"><span data-stu-id="97fd3-250">string legalEntityId</span></span>     | <span data-ttu-id="97fd3-251">データ インポートの法人。</span><span class="sxs-lookup"><span data-stu-id="97fd3-251">The legal entity for the data import.</span></span> |
    
<span data-ttu-id="97fd3-252">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="97fd3-252">**Output parameters**</span></span>

| <span data-ttu-id="97fd3-253">パラメーター</span><span class="sxs-lookup"><span data-stu-id="97fd3-253">Parameter</span></span>          | <span data-ttu-id="97fd3-254">説明</span><span class="sxs-lookup"><span data-stu-id="97fd3-254">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="97fd3-255">string executionId</span><span class="sxs-lookup"><span data-stu-id="97fd3-255">string executionId</span></span> | <span data-ttu-id="97fd3-256">データ エクスポートの実行 ID。</span><span class="sxs-lookup"><span data-stu-id="97fd3-256">The execution ID of the data export.</span></span> |

### <a name="getexportedpackageurl"></a><span data-ttu-id="97fd3-257">GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="97fd3-257">GetExportedPackageUrl</span></span>

<span data-ttu-id="97fd3-258">**GetExportedPackageUrl** API は、**ExportToPackage** を呼び出すことでエクスポートされたデータ パッケージの URL を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-258">The **GetExportedPackageUrl** API is used to get the URL of the data package that was exported by a call to **ExportToPackage**.</span></span> <span data-ttu-id="97fd3-259">この API は、クラウド配置とオンプレミス配置の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-259">This API is applicable to both cloud deployments and on-premises deployments.</span></span>

```CSharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
BODY
{"executionId":"<Execution Id>"}
```

<span data-ttu-id="97fd3-260">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-260">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"https://<baseurl_id>.blob.core.windows.net/dmf/<uniqueFileName>?<SAS Token>"
    }
}
```

<span data-ttu-id="97fd3-261">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="97fd3-261">**Input parameters**</span></span>

| <span data-ttu-id="97fd3-262">パラメーター</span><span class="sxs-lookup"><span data-stu-id="97fd3-262">Parameter</span></span>          | <span data-ttu-id="97fd3-263">説明</span><span class="sxs-lookup"><span data-stu-id="97fd3-263">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="97fd3-264">string executionId</span><span class="sxs-lookup"><span data-stu-id="97fd3-264">string executionId</span></span> | <span data-ttu-id="97fd3-265">データ プロジェクト実行の実行 ID。</span><span class="sxs-lookup"><span data-stu-id="97fd3-265">The execution ID of the data project run.</span></span> |

<span data-ttu-id="97fd3-266">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="97fd3-266">**Output parameters**</span></span>

| <span data-ttu-id="97fd3-267">パラメーター</span><span class="sxs-lookup"><span data-stu-id="97fd3-267">Parameter</span></span>      | <span data-ttu-id="97fd3-268">説明</span><span class="sxs-lookup"><span data-stu-id="97fd3-268">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="97fd3-269">string BlobUrl</span><span class="sxs-lookup"><span data-stu-id="97fd3-269">string BlobUrl</span></span> | <span data-ttu-id="97fd3-270">埋め込みの SAS トークンを持つ blob URL。</span><span class="sxs-lookup"><span data-stu-id="97fd3-270">A blob URL that has an embedded SAS token.</span></span> <span data-ttu-id="97fd3-271">URL を使用して、エクスポートしたデータ パッケージをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-271">The URL can be used to download the exported data package.</span></span> |

## <a name="status-check-api"></a><span data-ttu-id="97fd3-272">ステータス チェック API</span><span class="sxs-lookup"><span data-stu-id="97fd3-272">Status check API</span></span> 

<span data-ttu-id="97fd3-273">状態を確認するには、次の API を使用します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-273">The following APIs are used to check status.</span></span> <span data-ttu-id="97fd3-274">これらは、インポート フローとエクスポート フローの両方で使用されます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-274">They are used during both import flows and export flows.</span></span>

### <a name="getexecutionsummarystatus"></a><span data-ttu-id="97fd3-275">GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="97fd3-275">GetExecutionSummaryStatus</span></span>

<span data-ttu-id="97fd3-276">**GetExecutionSummaryStatus** API は、インポート ジョブとエクスポート ジョブの両方に使用されます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-276">The **GetExecutionSummaryStatus** API is used for both import jobs and export jobs.</span></span> <span data-ttu-id="97fd3-277">これは、データ プロジェクト実行ジョブのステータスの確認に使用されます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-277">It's used to check the status of a data project execution job.</span></span> <span data-ttu-id="97fd3-278">この API は、クラウド配置とオンプレミス配置の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-278">This API is applicable to both cloud deployments and on-premises deployments.</span></span>

```CSharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
BODY
{"executionId":"<executionId>"}
```

<span data-ttu-id="97fd3-279">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-279">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"<executionStatus>"
    }
}
```

<span data-ttu-id="97fd3-280">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="97fd3-280">**Input parameters**</span></span>

| <span data-ttu-id="97fd3-281">パラメーター</span><span class="sxs-lookup"><span data-stu-id="97fd3-281">Parameter</span></span>          | <span data-ttu-id="97fd3-282">説明</span><span class="sxs-lookup"><span data-stu-id="97fd3-282">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="97fd3-283">string executionId</span><span class="sxs-lookup"><span data-stu-id="97fd3-283">string executionId</span></span> | <span data-ttu-id="97fd3-284">データ プロジェクト実行の実行 ID。</span><span class="sxs-lookup"><span data-stu-id="97fd3-284">The execution ID of the data project run.</span></span> |

<span data-ttu-id="97fd3-285">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="97fd3-285">**Output parameters**</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="97fd3-286">パラメーター</span><span class="sxs-lookup"><span data-stu-id="97fd3-286">Parameter</span></span></th>
<th><span data-ttu-id="97fd3-287">説明</span><span class="sxs-lookup"><span data-stu-id="97fd3-287">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="97fd3-288">DMFExecutionSummaryStatus executionStatus</span><span class="sxs-lookup"><span data-stu-id="97fd3-288">DMFExecutionSummaryStatus executionStatus</span></span></td>
<td><span data-ttu-id="97fd3-289">実行のステータス。</span><span class="sxs-lookup"><span data-stu-id="97fd3-289">The execution status.</span></span> <span data-ttu-id="97fd3-290">以下に使用可能な値を示します。</span><span class="sxs-lookup"><span data-stu-id="97fd3-290">Here are the possible values:</span></span>
<ul>
<li><span data-ttu-id="97fd3-291">不明</span><span class="sxs-lookup"><span data-stu-id="97fd3-291">Unknown</span></span></li>
<li><span data-ttu-id="97fd3-292">NotRun</span><span class="sxs-lookup"><span data-stu-id="97fd3-292">NotRun</span></span></li>
<li><span data-ttu-id="97fd3-293">実行中</span><span class="sxs-lookup"><span data-stu-id="97fd3-293">Executing</span></span></li>
<li><span data-ttu-id="97fd3-294">成功</span><span class="sxs-lookup"><span data-stu-id="97fd3-294">Succeeded</span></span></li>
<li><span data-ttu-id="97fd3-295">PartiallySucceeded</span><span class="sxs-lookup"><span data-stu-id="97fd3-295">PartiallySucceeded</span></span></li>
<li><span data-ttu-id="97fd3-296">失敗</span><span class="sxs-lookup"><span data-stu-id="97fd3-296">Failed</span></span></li>
<li><span data-ttu-id="97fd3-297">取消済</span><span class="sxs-lookup"><span data-stu-id="97fd3-297">Canceled</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="97fd3-298">Blob ストレージ内のファイルはストレージに 7 日間残ります。</span><span class="sxs-lookup"><span data-stu-id="97fd3-298">The file in Blob storage will remain there for seven days.</span></span> <span data-ttu-id="97fd3-299">次に、そのファイルは自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-299">It will then be automatically deleted.</span></span>

## <a name="import-and-export-processes"></a><span data-ttu-id="97fd3-300">プロセスのインポートとエクスポート</span><span class="sxs-lookup"><span data-stu-id="97fd3-300">Import and export processes</span></span>

<span data-ttu-id="97fd3-301">次の図は、データ管理パッケージ メソッドを使用してデータ パッケージをインポートする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="97fd3-301">The following illustration shows how the Data management package methods can be used to import data packages.</span></span>

![データ管理パッケージ メソッドを使用するデータ パッケージ ファイルのインポート](./media/data-package-import.png)

<span data-ttu-id="97fd3-303">次の図は、データ管理パッケージ メソッドを使用してデータ パッケージをエクスポートする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="97fd3-303">The following illustration shows how the Data management package methods can be used to export data packages.</span></span>

![データ管理パッケージ メソッドを使用するデータ パッケージ ファイルのエクスポート](./media/data-package-export.png)

<span data-ttu-id="97fd3-305">データのインポートとデータのエクスポートのメソッドを紹介するサンプルのコンソール アプリケーションは、 GitHub から入手できます。</span><span class="sxs-lookup"><span data-stu-id="97fd3-305">A sample console application that showcases the data import and data export methods is available on GitHub.</span></span> <span data-ttu-id="97fd3-306">詳細については、「<https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/FileBasedIntegrationSamples/ConsoleAppSamples>」に移動してください。</span><span class="sxs-lookup"><span data-stu-id="97fd3-306">For more information, go to <https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/FileBasedIntegrationSamples/ConsoleAppSamples>.</span></span>
