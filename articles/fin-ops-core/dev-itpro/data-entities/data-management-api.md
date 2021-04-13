---
title: データ管理パッケージ REST API
description: このトピックでは、データ管理フレームワークのパッケージ REST API について説明します。
author: Sunil-Garg
ms.date: 06/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2017-03-31
ms.dyn365.ops.version: Platform update 5
ms.openlocfilehash: 813da7d30fc744792a189431ea2b2ebc57e4cfe2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750984"
---
# <a name="data-management-package-rest-api"></a><span data-ttu-id="14271-103">データ管理パッケージ REST API</span><span class="sxs-lookup"><span data-stu-id="14271-103">Data management package REST API</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14271-104">このトピックでは、データ管理フレームワークのパッケージの Representational State Transfer (REST) のアプリケーション プログラミング インターフェイス (API) について説明します。</span><span class="sxs-lookup"><span data-stu-id="14271-104">This topic describes the Data management framework's package representational state transfer (REST) application programming interface (API).</span></span> <span data-ttu-id="14271-105">パッケージ API により、データ パッケージを使用して統合できます。</span><span class="sxs-lookup"><span data-stu-id="14271-105">The package API lets you integrate by using data packages.</span></span> <span data-ttu-id="14271-106">REST API はクラウド展開とオンプレミスの展開で使用できます。</span><span class="sxs-lookup"><span data-stu-id="14271-106">The REST API can be used with both cloud deployments and on-premises deployments.</span></span> <span data-ttu-id="14271-107">オンプレミス配置では、現在この機能は、Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition プラットフォーム更新プログラム 12 (2017 年 11 月) (バージョン 7.2)、ビルド 7.0.4709.41184 以降で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="14271-107">For on-premises deployments, this functionality is currently available for Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with platform update 12 (November 2017) (version 7.2), build 7.0.4709.41184, and later.</span></span>

<span data-ttu-id="14271-108">オンプレミス サポートが追加されましたが、API 名は変更されていません。</span><span class="sxs-lookup"><span data-stu-id="14271-108">Although on-premises support has been added, API names haven't been changed.</span></span> <span data-ttu-id="14271-109">したがって、Microsoft は、クラウド配置とオンプレミス配置の両方に対して単一の API セットを維持することができます。</span><span class="sxs-lookup"><span data-stu-id="14271-109">Therefore, Microsoft can keep a single API set for both cloud deployments and on-premises deployments.</span></span>

## <a name="choosing-an-integration-api"></a><span data-ttu-id="14271-110">統合 API の選択</span><span class="sxs-lookup"><span data-stu-id="14271-110">Choosing an integration API</span></span>

<span data-ttu-id="14271-111">ファイル ベースの統合シナリオは、データ管理フレームワークのパッケージ API と定期的な統合 API の 2 つの API によりサポートされます。</span><span class="sxs-lookup"><span data-stu-id="14271-111">Two APIs support file-based integration scenarios: the Data management framework's package API and the recurring integrations API.</span></span> <span data-ttu-id="14271-112">どちらの API もデータ インポート シナリオとデータ エクスポート シナリオの両方をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="14271-112">Both APIs support both data import scenarios and data export scenarios.</span></span> <span data-ttu-id="14271-113">次のテーブルでは、使用する API を決定する際に考慮する必要がある主な決定事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="14271-113">The following table describes the main decision points that you should consider when you're trying to decide which API to use.</span></span>

| <span data-ttu-id="14271-114">決定ポイント</span><span class="sxs-lookup"><span data-stu-id="14271-114">Decision point</span></span>      | <span data-ttu-id="14271-115">定期統合 API</span><span class="sxs-lookup"><span data-stu-id="14271-115">Recurring integrations API</span></span> | <span data-ttu-id="14271-116">データ管理フレームワークのパッケージ API</span><span class="sxs-lookup"><span data-stu-id="14271-116">Data management framework's package API</span></span> |
|---------------------|--------------------------------------|-----------------------------|
| <span data-ttu-id="14271-117">スケジューリング</span><span class="sxs-lookup"><span data-stu-id="14271-117">Scheduling</span></span>          | <span data-ttu-id="14271-118">Finance and Operations アプリのスケジューリング</span><span class="sxs-lookup"><span data-stu-id="14271-118">Scheduling in Finance and Operations apps</span></span> | <span data-ttu-id="14271-119">Finance and Operations アプリ以外のスケジューリング</span><span class="sxs-lookup"><span data-stu-id="14271-119">Scheduling outside Finance and Operations apps</span></span> |
| <span data-ttu-id="14271-120">Format</span><span class="sxs-lookup"><span data-stu-id="14271-120">Format</span></span>              | <span data-ttu-id="14271-121">ファイルおよびデータ パッケージ</span><span class="sxs-lookup"><span data-stu-id="14271-121">Files and data packages</span></span> | <span data-ttu-id="14271-122">データ パッケージのみ</span><span class="sxs-lookup"><span data-stu-id="14271-122">Only data packages</span></span> |
| <span data-ttu-id="14271-123">変換</span><span class="sxs-lookup"><span data-stu-id="14271-123">Transformation</span></span>      | <span data-ttu-id="14271-124">データ ファイルが XML 形式の場合の Extensible Stylesheet Language Transformations (XSLT) のサポート</span><span class="sxs-lookup"><span data-stu-id="14271-124">Support for Extensible Stylesheet Language Transformations (XSLT) if the data file is in XML format</span></span> | <span data-ttu-id="14271-125">システム外部での変換</span><span class="sxs-lookup"><span data-stu-id="14271-125">Transformations that are external to the system</span></span> |
| <span data-ttu-id="14271-126">サポートされているプロトコル</span><span class="sxs-lookup"><span data-stu-id="14271-126">Supported protocols</span></span> | <span data-ttu-id="14271-127">SOAP および REST</span><span class="sxs-lookup"><span data-stu-id="14271-127">SOAP and REST</span></span> | <span data-ttu-id="14271-128">REST</span><span class="sxs-lookup"><span data-stu-id="14271-128">REST</span></span> |
| <span data-ttu-id="14271-129">サービス タイプ</span><span class="sxs-lookup"><span data-stu-id="14271-129">Service type</span></span>        | <span data-ttu-id="14271-130">カスタム サービス</span><span class="sxs-lookup"><span data-stu-id="14271-130">Custom service</span></span> | <span data-ttu-id="14271-131">データ プロトコル (OData) アクションを開きます</span><span class="sxs-lookup"><span data-stu-id="14271-131">Open Data Protocol (OData) action</span></span> |
| <span data-ttu-id="14271-132">在庫状態</span><span class="sxs-lookup"><span data-stu-id="14271-132">Availability</span></span>        | <span data-ttu-id="14271-133">Microsoft Dynamics Finance and Operations (2016 年 2 月) およびそれ以降。</span><span class="sxs-lookup"><span data-stu-id="14271-133">Microsoft Dynamics Finance and Operations (February 2016) and later.</span></span> <span data-ttu-id="14271-134">注意: この機能は、オンプレミス バージョンの Dynamics 365 Finance and Operations には対応していません。</span><span class="sxs-lookup"><span data-stu-id="14271-134">Note: This is not supported with the on-premises version of Dynamics 365 Finance and Operations.</span></span> | <span data-ttu-id="14271-135">Microsoft Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 5 (2017 年 3 月) およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="14271-135">Microsoft Dynamics 365 for Finance and Operations with platform update 5 (March 2017) and later</span></span> |

<span data-ttu-id="14271-136">定期的な統合 API がデータ管理フレームワークのパッケージ API よりも要件を満たしていることを決定した場合、[定期統合](recurring-integrations.md) を参照します。</span><span class="sxs-lookup"><span data-stu-id="14271-136">If you decide that the recurring integrations API meets your requirement better than the Data management framework's package API, see [Recurring integrations](recurring-integrations.md).</span></span> <span data-ttu-id="14271-137">このトピックの残りの部分では、データ管理フレームワークのパッケージ API について説明します。</span><span class="sxs-lookup"><span data-stu-id="14271-137">The rest of this topic discusses the Data management framework's package API.</span></span>

## <a name="authorization"></a><span data-ttu-id="14271-138">承認</span><span class="sxs-lookup"><span data-stu-id="14271-138">Authorization</span></span>

<span data-ttu-id="14271-139">データ管理フレームワークのパッケージ API は、アクセスを認可するために OAuth 2.0 を使用します。</span><span class="sxs-lookup"><span data-stu-id="14271-139">The Data management framework's package API uses OAuth 2.0 to authorize access.</span></span> <span data-ttu-id="14271-140">API は、有効な OAuth アクセス トークンを使用して呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="14271-140">The API must be called by using a valid OAuth access token.</span></span> <span data-ttu-id="14271-141">OAuth 2.0 および Microsoft Azure Active Directory(Azure AD) の詳細については、[OAuth 2.0 と Azure Active Directory を使用して Web アプリケーションへのアクセスを承認](/azure/active-directory/develop/active-directory-protocols-oauth-code) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="14271-141">For more information about OAuth 2.0 and Microsoft Azure Active Directory (Azure AD), see [Authorize access to web applications using OAuth 2.0 and Azure Active Directory](/azure/active-directory/develop/active-directory-protocols-oauth-code).</span></span> <span data-ttu-id="14271-142">オンプレミス配置では、Active Directory フェデレーション サービス (AD FS) が承認に使用されます。</span><span class="sxs-lookup"><span data-stu-id="14271-142">For on-premises deployments, Active Directory Federation Services (AD FS) is used for authorization.</span></span>

> [!NOTE]
> <span data-ttu-id="14271-143">クライアント資格情報の付与フローを使用すると、アプリケーションはアクセス制御リストを保持します。</span><span class="sxs-lookup"><span data-stu-id="14271-143">When you use the Client Credentials Grant flow, the application maintains an access control list.</span></span> <span data-ttu-id="14271-144">アクセス制御リストは、**システム管理** \> **設定** \> **Azure Active Directory アプリケーション** を順にクリックして見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="14271-144">You can find the access control list at **System administration** \> **Setup** \> **Azure Active Directory applications**.</span></span> <span data-ttu-id="14271-145">**Azure Active Directory アプリケーション** ページには、承認済クライアント ID と、クライアント資格情報付与フローを使用して API が呼び出されたときに適用する必要があるユーザー セキュリティ マッピングが表示されます。</span><span class="sxs-lookup"><span data-stu-id="14271-145">The **Azure Active Directory applications** page shows the approved client IDs and the user security mapping that should be enforced when the API is called by using the Client Credentials Grant flow.</span></span>
>
> <span data-ttu-id="14271-146">オンプレミス配置については、このリストには AD FS からの有効なクライアント ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="14271-146">For on-premises deployments, this list must have a valid client ID from AD FS.</span></span> <span data-ttu-id="14271-147">また、オンプレミスで使用する場合は、接続の確立時に、次の例にて示されている **\<baseurl\>** に **/namespaces/AXSF** を付加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="14271-147">Additionally, for on-premises use, **\<baseurl\>** in the following examples must append **/namespaces/AXSF** when a connection is made.</span></span>

## <a name="import-apis"></a><span data-ttu-id="14271-148">API のインポート</span><span class="sxs-lookup"><span data-stu-id="14271-148">Import APIs</span></span>

<span data-ttu-id="14271-149">ファイル (データ パッケージ) のインポートには、次の API が使用されます。</span><span class="sxs-lookup"><span data-stu-id="14271-149">The following APIs are used to import files (data packages).</span></span>

### <a name="getimportstagingerrorfileurl"></a><span data-ttu-id="14271-150">GetImportStagingErrorFileUrl</span><span class="sxs-lookup"><span data-stu-id="14271-150">GetImportStagingErrorFileUrl</span></span>

<span data-ttu-id="14271-151">GetImportStagingErrorFileUrl API は、エラーファイルのURLを取得します。エラーファイルには単一のエンティティに対するインポートの過程で、ステージング段階で失敗したデータが格納されています。</span><span class="sxs-lookup"><span data-stu-id="14271-151">The GetImportStagingErrorFileUrl API is used to get the URL of the error file containing the input records that failed at the source to the staging step of import for a single entity.</span></span> <span data-ttu-id="14271-152">エラーファイルが生成されなかった場合は、空の文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="14271-152">An empty string is returned if no error file is generated.</span></span>

<span data-ttu-id="14271-153">POST /Data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetImportStagingErrorFileUrl</span><span class="sxs-lookup"><span data-stu-id="14271-153">POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetImportStagingErrorFileUrl</span></span>

```json
Body
{
    "executionId":"<string>",
    "entityName":"<string>"
}

Successful Response:

HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":"<errorfileurl>"
}
```

<span data-ttu-id="14271-154">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="14271-154">**Input parameters**</span></span>

| <span data-ttu-id="14271-155">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14271-155">Parameter</span></span>     | <span data-ttu-id="14271-156">説明</span><span class="sxs-lookup"><span data-stu-id="14271-156">Description</span></span> |
|---------------------|--------------------------------------|
| <span data-ttu-id="14271-157">string executionId</span><span class="sxs-lookup"><span data-stu-id="14271-157">string executionId</span></span>          | <span data-ttu-id="14271-158">インポート処理の実行ID。</span><span class="sxs-lookup"><span data-stu-id="14271-158">Execution ID of import.</span></span> <span data-ttu-id="14271-159">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="14271-159">This is called as Job ID in the UI.</span></span> |
| <span data-ttu-id="14271-160">string entityName</span><span class="sxs-lookup"><span data-stu-id="14271-160">string entityName</span></span>        | <span data-ttu-id="14271-161">エラー ファイルの取得対象となるエンティティの名前。</span><span class="sxs-lookup"><span data-stu-id="14271-161">Name of the entity for which to get the error file.</span></span> |


<span data-ttu-id="14271-162">**出力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="14271-162">**Output parameters**</span></span>

| <span data-ttu-id="14271-163">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14271-163">Parameter</span></span>         | <span data-ttu-id="14271-164">説明</span><span class="sxs-lookup"><span data-stu-id="14271-164">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="14271-165">string errorkeysfileurl</span><span class="sxs-lookup"><span data-stu-id="14271-165">string errorkeysfileurl</span></span> | <span data-ttu-id="14271-166">エラーファイルのURL。</span><span class="sxs-lookup"><span data-stu-id="14271-166">The URL of the error file.</span></span> <span data-ttu-id="14271-167">エラーファイルが生成されなかった場合は、空の戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="14271-167">The return value is empty if an error file was not generated.</span></span> |


### <a name="generateimporttargeterrorkeysfile"></a><span data-ttu-id="14271-168">GenerateImportTargetErrorKeysFile</span><span class="sxs-lookup"><span data-stu-id="14271-168">GenerateImportTargetErrorKeysFile</span></span>

<span data-ttu-id="14271-169">GenerateImportTargetErrorKeysFile API は、エラーファイルを生成します。エラーファイルには単一のエンティティに対するインポートの過程で、ステージングからターゲットの段階で失敗したインポート レコードのキーが格納されています。</span><span class="sxs-lookup"><span data-stu-id="14271-169">The GenerateImportTargetErrorKeysFile API is used to generate an error file containing the keys of the import records that failed at the staging to target step of import for a single entity.</span></span>  

<span data-ttu-id="14271-170">このAPIがtrueを返す場合は、GetImportTargetErrorKeysFileUrl API を使用して、生成されたエラーキーファイルのURLを取得します。</span><span class="sxs-lookup"><span data-stu-id="14271-170">If this API returns true, then use the GetImportTargetErrorKeysFileUrl API to get the URL of the generated error keys file.</span></span>


<span data-ttu-id="14271-171">POST /Data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GenerateImportTargetErrorKeysFile</span><span class="sxs-lookup"><span data-stu-id="14271-171">POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GenerateImportTargetErrorKeysFile</span></span>

```json
Body

{
    "executionId":"<string>",
    "entityName":"<string>"
}

Successful Response:

HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.Boolean",
    "value": <errorsExist>
}
```

<span data-ttu-id="14271-172">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="14271-172">**Input parameters**</span></span>

| <span data-ttu-id="14271-173">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14271-173">Parameter</span></span>     | <span data-ttu-id="14271-174">説明</span><span class="sxs-lookup"><span data-stu-id="14271-174">Description</span></span> |
|---------------------|--------------------------------------|
| <span data-ttu-id="14271-175">string executionId</span><span class="sxs-lookup"><span data-stu-id="14271-175">string executionId</span></span>          | <span data-ttu-id="14271-176">インポート処理の実行ID。</span><span class="sxs-lookup"><span data-stu-id="14271-176">Execution ID of import</span></span> |
| <span data-ttu-id="14271-177">string entityName</span><span class="sxs-lookup"><span data-stu-id="14271-177">string entityName</span></span>        | <span data-ttu-id="14271-178">エラー ファイルの取得対象となるエンティティの名前。</span><span class="sxs-lookup"><span data-stu-id="14271-178">Name of the entity for which to get the error file</span></span> |

<span data-ttu-id="14271-179">**出力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="14271-179">**Output parameters**</span></span>

| <span data-ttu-id="14271-180">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14271-180">Parameter</span></span>     | <span data-ttu-id="14271-181">説明</span><span class="sxs-lookup"><span data-stu-id="14271-181">Description</span></span> |
|---------------------|--------------------------------------|
| <span data-ttu-id="14271-182">ブール値エラーが発生しています</span><span class="sxs-lookup"><span data-stu-id="14271-182">Boolean errorsExist</span></span>     | <span data-ttu-id="14271-183">インポートエラーが発生した場合はtrue、 インポートエラーが発生しなかった場合はfalseとします</span><span class="sxs-lookup"><span data-stu-id="14271-183">true if there are import errors; false if there are no errors</span></span> |

### <a name="getimporttargeterrorkeysfileurl"></a><span data-ttu-id="14271-184">GetImportTargetErrorKeysFileUrl</span><span class="sxs-lookup"><span data-stu-id="14271-184">GetImportTargetErrorKeysFileUrl</span></span>

<span data-ttu-id="14271-185">**GetImportTargetErrorKeysFileUrl** API を使用して、単一のエンティティに対するインポートのステージングからターゲットへのステップで失敗したインポート レコードのキーが格納されているエラー ファイルの URL を取得します。</span><span class="sxs-lookup"><span data-stu-id="14271-185">The **GetImportTargetErrorKeysFileUrl** API is used to get the URL of the error file that contains the keys of the import records that failed at the staging-to-target step of import for a single entity.</span></span>

<span data-ttu-id="14271-186">エラー ファイルが使用可能な場合、この API はその URL を返します。</span><span class="sxs-lookup"><span data-stu-id="14271-186">If the error file is available, this API returns the URL.</span></span> <span data-ttu-id="14271-187">エラー ファイルがまだ生成中の場合、またはエラー ファイルが存在しない場合は、API は空の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="14271-187">If the error file is still being generated, or if there is no error file, the API returns an empty string.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="14271-188">この API を呼び出す前に、**GenerateImportTargetErrorKeysFile** API を呼出して、エラー ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="14271-188">Before you call this API, call the **GenerateImportTargetErrorKeysFile** API to generate the error file.</span></span> <span data-ttu-id="14271-189">**GenerateImportTargetErrorKeysFile** API が **true** を返した場合、空でない文字列が返されるまで、ループでこの API を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="14271-189">If the **GenerateImportTargetErrorKeysFile** API returns **true**, call this API in a loop until it returns a non-empty string.</span></span> <span data-ttu-id="14271-190">**GenerateImportTargetErrorKeysFile** API が **false** を返した場合、エラーがないため、この API は空の文字列をかならず返します。</span><span class="sxs-lookup"><span data-stu-id="14271-190">If the **GenerateImportTargetErrorKeysFile** API returns **false**, this API will always return an empty string, because there are no errors.</span></span>

<span data-ttu-id="14271-191">**疑似コードの例**</span><span class="sxs-lookup"><span data-stu-id="14271-191">**Pseudocode example**</span></span>

```csharp
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

```csharp
POST
/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetImportTargetErrorKeysFileUrl

Body
{
    "executionId":"<string>",
    "entityName":"<string>"
}
```

<span data-ttu-id="14271-192">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="14271-192">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":"<errorkeysfileurl>"
}
```

<span data-ttu-id="14271-193">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="14271-193">**Input parameters**</span></span>

| <span data-ttu-id="14271-194">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14271-194">Parameter</span></span>         | <span data-ttu-id="14271-195">説明</span><span class="sxs-lookup"><span data-stu-id="14271-195">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="14271-196">string executionId</span><span class="sxs-lookup"><span data-stu-id="14271-196">string executionId</span></span> | <span data-ttu-id="14271-197">インポートの実行 ID。</span><span class="sxs-lookup"><span data-stu-id="14271-197">The execution ID of the import.</span></span> <span data-ttu-id="14271-198">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="14271-198">This is called as Job ID in the UI.</span></span>|
| <span data-ttu-id="14271-199">string entityName</span><span class="sxs-lookup"><span data-stu-id="14271-199">string entityName</span></span> | <span data-ttu-id="14271-200">エラー ファイルを取得する対象のエンティティの名前。</span><span class="sxs-lookup"><span data-stu-id="14271-200">The name of the entity to get the error file for.</span></span> |

<span data-ttu-id="14271-201">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="14271-201">**Output parameters**</span></span>

| <span data-ttu-id="14271-202">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14271-202">Parameter</span></span>         | <span data-ttu-id="14271-203">説明</span><span class="sxs-lookup"><span data-stu-id="14271-203">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="14271-204">string errorkeysfileurl</span><span class="sxs-lookup"><span data-stu-id="14271-204">string errorkeysfileurl</span></span> | <span data-ttu-id="14271-205">エラー キー ファイルが使用可能な場合、そのファイルの URL。</span><span class="sxs-lookup"><span data-stu-id="14271-205">The URL of the error keys file, if the file is available.</span></span> <span data-ttu-id="14271-206">エラー ファイルがまだ生成中の場合、またはエラー ファイルが存在しない場合は、このメソッドは空の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="14271-206">If the error file is still being generated, or if no errors exist, the method returns an empty string.</span></span> |


### <a name="getazurewritableurl"></a><span data-ttu-id="14271-207">GetAzureWritableUrl</span><span class="sxs-lookup"><span data-stu-id="14271-207">GetAzureWritableUrl</span></span>

<span data-ttu-id="14271-208">**GetAzureWritableUrl** API は、書き込み可能な Blob URL を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="14271-208">The **GetAzureWritableUrl** API is used to get a writable blob URL.</span></span> <span data-ttu-id="14271-209">このメソッドには、URL に埋め込まれた共有アクセス署名 (SAS) トークンが含まれています。</span><span class="sxs-lookup"><span data-stu-id="14271-209">The method includes a shared access signature (SAS) token that is embedded in the URL.</span></span> <span data-ttu-id="14271-210">この方法を使用すると、Azure Blob Storage コンテナーにデータ パッケージをアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="14271-210">You can use this method to upload a data package to the Azure Blob storage container.</span></span> <span data-ttu-id="14271-211">オンプレミス配置の場合、この API はローカル ストレージに取り込まれた URL を引き続き返します。</span><span class="sxs-lookup"><span data-stu-id="14271-211">For on-premises deployments, this API will still return the URL that has been abstracted to local storage.</span></span>

> [!NOTE]
> <span data-ttu-id="14271-212">SAS は有効期限の時間枠中にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="14271-212">An SAS is valid only during an expiry time window.</span></span> <span data-ttu-id="14271-213">ウィンドウが経過した後に発行されるすべての要求はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="14271-213">Any request that is issued after the window has passed returns an error.</span></span> <span data-ttu-id="14271-214">詳細については、[共有アクセス署名 (SA) の使用](/azure/storage/common/storage-dotnet-shared-access-signature-part-1) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="14271-214">For more information, see [Using shared access signatures (SAS)](/azure/storage/common/storage-dotnet-shared-access-signature-part-1).</span></span>

```csharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetAzureWriteUrl
BODY
{
    "uniqueFileName":"<string>"
}
```

<span data-ttu-id="14271-215">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="14271-215">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value": "{\"BlobId\":\"{<GUID>}\",\"BlobUrl\":\"https://<baseurl_id>.blob.core.windows.net/dmf/<uniqueFileName>?<SAS Token>\"}"
    }
}
```

<span data-ttu-id="14271-216">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="14271-216">**Input parameters**</span></span>

| <span data-ttu-id="14271-217">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14271-217">Parameter</span></span>         | <span data-ttu-id="14271-218">説明</span><span class="sxs-lookup"><span data-stu-id="14271-218">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="14271-219">文字列 uniqueFileName</span><span class="sxs-lookup"><span data-stu-id="14271-219">string uniqueFileName</span></span> | <span data-ttu-id="14271-220">BLOB ID を追跡するために使用される一意のファイル名。</span><span class="sxs-lookup"><span data-stu-id="14271-220">A unique file name that is used to track blob IDs.</span></span> <span data-ttu-id="14271-221">一意のファイル名であることを保証するため、グローバル一意識別子 (GUID) を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="14271-221">You can include a globally unique identifier (GUID) to help guarantee a unique file name.</span></span> |

<span data-ttu-id="14271-222">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="14271-222">**Output parameters**</span></span>

| <span data-ttu-id="14271-223">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14271-223">Parameter</span></span>      | <span data-ttu-id="14271-224">説明</span><span class="sxs-lookup"><span data-stu-id="14271-224">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="14271-225">string BlobId</span><span class="sxs-lookup"><span data-stu-id="14271-225">string BlobId</span></span>  | <span data-ttu-id="14271-226">割り当てられた BLOB コンテナーの BLOB ID。</span><span class="sxs-lookup"><span data-stu-id="14271-226">The blob ID of the allocated blob container.</span></span> |
| <span data-ttu-id="14271-227">string BlobUrl</span><span class="sxs-lookup"><span data-stu-id="14271-227">string BlobUrl</span></span> | <span data-ttu-id="14271-228">埋め込みの SAS トークンを持つ URL。</span><span class="sxs-lookup"><span data-stu-id="14271-228">A URL that has an embedded SAS token.</span></span> <span data-ttu-id="14271-229">URL を使用 して Blob ストレージに書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="14271-229">The URL can be used to write to Blob storage.</span></span> |

### <a name="importfrompackage"></a><span data-ttu-id="14271-230">ImportFromPackage</span><span class="sxs-lookup"><span data-stu-id="14271-230">ImportFromPackage</span></span>

<span data-ttu-id="14271-231">**ImportFromPackage** API は、実装に関連付けられている Blob ストレージにアップロードされるデータ パッケージからインポートを開始するために使用します。</span><span class="sxs-lookup"><span data-stu-id="14271-231">The **ImportFromPackage** API is used to initiate an import from the data package that is uploaded to the Blob storage that is associated with your implementation.</span></span> <span data-ttu-id="14271-232">オンプレミス配置の場合、ファイルが以前アップロードされたローカル ストレージから、インポートが開始されます。</span><span class="sxs-lookup"><span data-stu-id="14271-232">For on-premises deployments, the import will be initiated from the local storage that the file was uploaded previously to.</span></span>

> [!NOTE]
> <span data-ttu-id="14271-233">プラットフォーム更新プログラム 12 を起動すると、**ImportFromPackage** API は複合エンティティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="14271-233">Starting in Platform update 12, the **ImportFromPackage** API supports composite entities.</span></span> <span data-ttu-id="14271-234">ただし、1 つのパッケージで 1 つの複合エンティティのみという制限があります。</span><span class="sxs-lookup"><span data-stu-id="14271-234">However, the limitation is that there can be only one composite entity in a package.</span></span>

```csharp
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

<span data-ttu-id="14271-235">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="14271-235">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":"<executionId>"
}
```

<span data-ttu-id="14271-236">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="14271-236">**Input parameters**</span></span>

| <span data-ttu-id="14271-237">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14271-237">Parameter</span></span>                | <span data-ttu-id="14271-238">説明</span><span class="sxs-lookup"><span data-stu-id="14271-238">Description</span></span> |
|--------------------------|-------------|
| <span data-ttu-id="14271-239">string packageUrl</span><span class="sxs-lookup"><span data-stu-id="14271-239">string packageUrl</span></span>        | <span data-ttu-id="14271-240">Finance and Operations アプリに関連付けられている Blob Storage 内のデータ パッケージの URL。</span><span class="sxs-lookup"><span data-stu-id="14271-240">The URL of the data package in the Blob storage that is associated with a Finance and Operations app.</span></span> |
| <span data-ttu-id="14271-241">string definitionGroupId</span><span class="sxs-lookup"><span data-stu-id="14271-241">string definitionGroupId</span></span> | <span data-ttu-id="14271-242">インポート用のデータ プロジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="14271-242">The name of the data project for import.</span></span> |
| <span data-ttu-id="14271-243">string executionId</span><span class="sxs-lookup"><span data-stu-id="14271-243">string executionId</span></span>       | <span data-ttu-id="14271-244">ジョブに使用する ID。</span><span class="sxs-lookup"><span data-stu-id="14271-244">The ID to use for the job.</span></span> <span data-ttu-id="14271-245">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="14271-245">This is called as Job ID in the UI.</span></span> <span data-ttu-id="14271-246">空の ID が割り当てられている場合は、新しい実行 ID が作成されます。</span><span class="sxs-lookup"><span data-stu-id="14271-246">If an empty ID is assigned, a new execution ID will be created.</span></span> |
| <span data-ttu-id="14271-247">bool execute</span><span class="sxs-lookup"><span data-stu-id="14271-247">bool execute</span></span>             | <span data-ttu-id="14271-248">このパラメーターを **True** に設定して対象の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="14271-248">Set this parameter to **True** to run the target step.</span></span> <span data-ttu-id="14271-249">それ以外の場合、**False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="14271-249">Otherwise, set it to **False**.</span></span> |
| <span data-ttu-id="14271-250">bool overwrite</span><span class="sxs-lookup"><span data-stu-id="14271-250">bool overwrite</span></span>           | <span data-ttu-id="14271-251">パッケージ内で複合エンティティを使用する場合は、このパラメーターを常に **False** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="14271-251">This parameter must always be set to **False** when a composite entity is used in a package.</span></span> <span data-ttu-id="14271-252">それ以外の場合、**True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="14271-252">Otherwise, set it to **True**.</span></span> |
| <span data-ttu-id="14271-253">string legalEntityId</span><span class="sxs-lookup"><span data-stu-id="14271-253">string legalEntityId</span></span>     | <span data-ttu-id="14271-254">データ インポートの法人。</span><span class="sxs-lookup"><span data-stu-id="14271-254">The legal entity for the data import.</span></span> |

<span data-ttu-id="14271-255">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="14271-255">**Output parameters**</span></span>

| <span data-ttu-id="14271-256">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14271-256">Parameter</span></span>          | <span data-ttu-id="14271-257">説明</span><span class="sxs-lookup"><span data-stu-id="14271-257">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="14271-258">string executionId</span><span class="sxs-lookup"><span data-stu-id="14271-258">string executionId</span></span> | <span data-ttu-id="14271-259">データ インポートの実行 ID。</span><span class="sxs-lookup"><span data-stu-id="14271-259">The execution ID of the data import.</span></span> <span data-ttu-id="14271-260">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="14271-260">This is called as Job ID in the UI.</span></span> |

> [!NOTE]
> <span data-ttu-id="14271-261">**ImportFromPackage()** はバッチを使用してインポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="14271-261">**ImportFromPackage()** uses a batch to perform the import.</span></span> <span data-ttu-id="14271-262">したがって、並行インポートを実行するために、データ管理で並列処理ルールを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="14271-262">Therefore, parallel processing rules must be used in Data management to perform parallel imports.</span></span> <span data-ttu-id="14271-263">**ImportFromPackage()** を並列スレッドで呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="14271-263">**ImportFromPackage()** must not be called in parallel threads.</span></span> <span data-ttu-id="14271-264">それ以外の場合、これは失敗します。</span><span class="sxs-lookup"><span data-stu-id="14271-264">Otherwise, it will fail.</span></span>

## <a name="export-apis"></a><span data-ttu-id="14271-265">API をエキスポート</span><span class="sxs-lookup"><span data-stu-id="14271-265">Export APIs</span></span>

<span data-ttu-id="14271-266">ファイル (データ パッケージ) のエクスポートには、次の API が使用されます。</span><span class="sxs-lookup"><span data-stu-id="14271-266">The following APIs are used to export files (data packages).</span></span>

### <a name="exporttopackage"></a><span data-ttu-id="14271-267">ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="14271-267">ExportToPackage</span></span>

<span data-ttu-id="14271-268">**ExportToPackage** API は、データ パッケージのエクスポートを開始するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="14271-268">The **ExportToPackage** API is used to initiate an export of a data package.</span></span> <span data-ttu-id="14271-269">この API は、クラウド配置とオンプレミス配置の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="14271-269">This API is applicable to both cloud deployments and on-premises deployments.</span></span>

- <span data-ttu-id="14271-270">この API を呼び出す前に、エクスポート データ プロジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="14271-270">The export data project must be created before you call this API.</span></span> <span data-ttu-id="14271-271">プロジェクトが存在しない場合、API の呼び出しには、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="14271-271">If the project doesn't exist, a call to the API returns an error.</span></span>
- <span data-ttu-id="14271-272">変更履歴がオンの場合は、最後の実行後に更新または作成されたレコードのみがエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="14271-272">If change tracking has been turned on, only records that have been created or updated since the last run are exported.</span></span> <span data-ttu-id="14271-273">(つまり、デルタのみが返されます。)</span><span class="sxs-lookup"><span data-stu-id="14271-273">(In other words, only the delta is returned.)</span></span>

```csharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage
BODY
{
    "definitionGroupId":"<Data project name>",
    "packageName":"<Name to use for downloaded file.>",
    "executionId":"<Execution Id if it is a rerun>",
    "reExecute":<bool>,
    "legalEntityId":"<Legal entity Id>"
}
```

<span data-ttu-id="14271-274">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="14271-274">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"<executionId>"
    }
}
```

<span data-ttu-id="14271-275">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="14271-275">**Input parameters**</span></span>

| <span data-ttu-id="14271-276">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14271-276">Parameter</span></span>                | <span data-ttu-id="14271-277">説明</span><span class="sxs-lookup"><span data-stu-id="14271-277">Description</span></span> |
|--------------------------|-------------|
| <span data-ttu-id="14271-278">string definitionGroupId</span><span class="sxs-lookup"><span data-stu-id="14271-278">string definitionGroupId</span></span> | <span data-ttu-id="14271-279">エクスポート用のデータ プロジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="14271-279">The name of the data project for export.</span></span> |
| <span data-ttu-id="14271-280">string packageName</span><span class="sxs-lookup"><span data-stu-id="14271-280">string packageName</span></span>       | <span data-ttu-id="14271-281">エクスポートされたデータ パッケージの名前。</span><span class="sxs-lookup"><span data-stu-id="14271-281">The name of the exported data package.</span></span> |
| <span data-ttu-id="14271-282">string executionId</span><span class="sxs-lookup"><span data-stu-id="14271-282">string executionId</span></span>       | <span data-ttu-id="14271-283">ジョブに使用する ID。</span><span class="sxs-lookup"><span data-stu-id="14271-283">The ID to use for the job.</span></span> <span data-ttu-id="14271-284">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="14271-284">This is called as Job ID in the UI.</span></span> <span data-ttu-id="14271-285">空の ID が割り当てられている場合は、新しい実行 ID が作成されます。</span><span class="sxs-lookup"><span data-stu-id="14271-285">If an empty ID is assigned, a new execution ID will be created.</span></span> |
| <span data-ttu-id="14271-286">bool reExecute</span><span class="sxs-lookup"><span data-stu-id="14271-286">bool reExecute</span></span>           | <span data-ttu-id="14271-287">このパラメーターを **True** に設定して対象の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="14271-287">Set this parameter to **True** to run the target step.</span></span> <span data-ttu-id="14271-288">それ以外の場合、**False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="14271-288">Otherwise, set it to **False**.</span></span> |
| <span data-ttu-id="14271-289">string legalEntityId</span><span class="sxs-lookup"><span data-stu-id="14271-289">string legalEntityId</span></span>     | <span data-ttu-id="14271-290">データ インポートの法人。</span><span class="sxs-lookup"><span data-stu-id="14271-290">The legal entity for the data import.</span></span> |
    
<span data-ttu-id="14271-291">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="14271-291">**Output parameters**</span></span>

| <span data-ttu-id="14271-292">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14271-292">Parameter</span></span>          | <span data-ttu-id="14271-293">説明</span><span class="sxs-lookup"><span data-stu-id="14271-293">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="14271-294">string executionId</span><span class="sxs-lookup"><span data-stu-id="14271-294">string executionId</span></span> | <span data-ttu-id="14271-295">データ エクスポートの実行 ID。</span><span class="sxs-lookup"><span data-stu-id="14271-295">The execution ID of the data export.</span></span> <span data-ttu-id="14271-296">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="14271-296">This is called as Job ID in the UI.</span></span> |

### <a name="getexportedpackageurl"></a><span data-ttu-id="14271-297">GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="14271-297">GetExportedPackageUrl</span></span>

<span data-ttu-id="14271-298">**GetExportedPackageUrl** API は、**ExportToPackage** を呼び出すことでエクスポートされたデータ パッケージの URL を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="14271-298">The **GetExportedPackageUrl** API is used to get the URL of the data package that was exported by a call to **ExportToPackage**.</span></span> <span data-ttu-id="14271-299">この API は、クラウド配置とオンプレミス配置の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="14271-299">This API is applicable to both cloud deployments and on-premises deployments.</span></span>

```csharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
BODY
{"executionId":"<Execution Id>"}
```

<span data-ttu-id="14271-300">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="14271-300">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"https://<baseurl_id>.blob.core.windows.net/dmf/<uniqueFileName>?<SAS Token>"
    }
}
```

<span data-ttu-id="14271-301">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="14271-301">**Input parameters**</span></span>

| <span data-ttu-id="14271-302">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14271-302">Parameter</span></span>          | <span data-ttu-id="14271-303">説明</span><span class="sxs-lookup"><span data-stu-id="14271-303">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="14271-304">string executionId</span><span class="sxs-lookup"><span data-stu-id="14271-304">string executionId</span></span> | <span data-ttu-id="14271-305">データ プロジェクト実行の実行 ID。</span><span class="sxs-lookup"><span data-stu-id="14271-305">The execution ID of the data project run.</span></span> <span data-ttu-id="14271-306">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="14271-306">This is called as Job ID in the UI.</span></span> |

<span data-ttu-id="14271-307">**出力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="14271-307">**Output parameters**</span></span>

| <span data-ttu-id="14271-308">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14271-308">Parameter</span></span>      | <span data-ttu-id="14271-309">説明</span><span class="sxs-lookup"><span data-stu-id="14271-309">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="14271-310">string BlobUrl</span><span class="sxs-lookup"><span data-stu-id="14271-310">string BlobUrl</span></span> | <span data-ttu-id="14271-311">埋め込みの SAS トークンを持つ blob URL。</span><span class="sxs-lookup"><span data-stu-id="14271-311">A blob URL that has an embedded SAS token.</span></span> <span data-ttu-id="14271-312">URL を使用して、エクスポートしたデータ パッケージをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="14271-312">The URL can be used to download the exported data package.</span></span> |

## <a name="status-check-api"></a><span data-ttu-id="14271-313">ステータス チェック API</span><span class="sxs-lookup"><span data-stu-id="14271-313">Status check API</span></span> 

<span data-ttu-id="14271-314">状態を確認するには、次の API を使用します。</span><span class="sxs-lookup"><span data-stu-id="14271-314">The following APIs are used to check status.</span></span> <span data-ttu-id="14271-315">これらは、インポート フローとエクスポート フローの両方で使用されます。</span><span class="sxs-lookup"><span data-stu-id="14271-315">They are used during both import flows and export flows.</span></span>

### <a name="getexecutionsummarystatus"></a><span data-ttu-id="14271-316">GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="14271-316">GetExecutionSummaryStatus</span></span>

<span data-ttu-id="14271-317">**GetExecutionSummaryStatus** API は、インポート ジョブとエクスポート ジョブの両方に使用されます。</span><span class="sxs-lookup"><span data-stu-id="14271-317">The **GetExecutionSummaryStatus** API is used for both import jobs and export jobs.</span></span> <span data-ttu-id="14271-318">これは、データ プロジェクト実行ジョブのステータスの確認に使用されます。</span><span class="sxs-lookup"><span data-stu-id="14271-318">It's used to check the status of a data project execution job.</span></span> <span data-ttu-id="14271-319">この API は、クラウド配置とオンプレミス配置の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="14271-319">This API is applicable to both cloud deployments and on-premises deployments.</span></span>

```csharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
BODY
{"executionId":"<executionId>"}
```

<span data-ttu-id="14271-320">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="14271-320">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":"<executionStatus>"
}
```

<span data-ttu-id="14271-321">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="14271-321">**Input parameters**</span></span>

| <span data-ttu-id="14271-322">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14271-322">Parameter</span></span>          | <span data-ttu-id="14271-323">説明</span><span class="sxs-lookup"><span data-stu-id="14271-323">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="14271-324">string executionId</span><span class="sxs-lookup"><span data-stu-id="14271-324">string executionId</span></span> | <span data-ttu-id="14271-325">データ プロジェクト実行の実行 ID。</span><span class="sxs-lookup"><span data-stu-id="14271-325">The execution ID of the data project run.</span></span> <span data-ttu-id="14271-326">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="14271-326">This is called as Job ID in the UI.</span></span> |

<span data-ttu-id="14271-327">**出力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="14271-327">**Output parameters**</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="14271-328">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14271-328">Parameter</span></span></th>
<th><span data-ttu-id="14271-329">説明</span><span class="sxs-lookup"><span data-stu-id="14271-329">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14271-330">DMFExecutionSummaryStatus executionStatus</span><span class="sxs-lookup"><span data-stu-id="14271-330">DMFExecutionSummaryStatus executionStatus</span></span></td>
<td><span data-ttu-id="14271-331">実行のステータス。</span><span class="sxs-lookup"><span data-stu-id="14271-331">The execution status.</span></span> <span data-ttu-id="14271-332">以下に使用可能な値を示します。</span><span class="sxs-lookup"><span data-stu-id="14271-332">Here are the possible values:</span></span>
<ul>
<li><span data-ttu-id="14271-333">不明</span><span class="sxs-lookup"><span data-stu-id="14271-333">Unknown</span></span></li>
<li><span data-ttu-id="14271-334">NotRun</span><span class="sxs-lookup"><span data-stu-id="14271-334">NotRun</span></span></li>
<li><span data-ttu-id="14271-335">実行中</span><span class="sxs-lookup"><span data-stu-id="14271-335">Executing</span></span></li>
<li><span data-ttu-id="14271-336">成功</span><span class="sxs-lookup"><span data-stu-id="14271-336">Succeeded</span></span></li>
<li><span data-ttu-id="14271-337">PartiallySucceeded</span><span class="sxs-lookup"><span data-stu-id="14271-337">PartiallySucceeded</span></span></li>
<li><span data-ttu-id="14271-338">失敗</span><span class="sxs-lookup"><span data-stu-id="14271-338">Failed</span></span></li>
<li><span data-ttu-id="14271-339">取消済</span><span class="sxs-lookup"><span data-stu-id="14271-339">Canceled</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="14271-340">Blob ストレージ内のファイルはストレージに 7 日間残ります。</span><span class="sxs-lookup"><span data-stu-id="14271-340">The file in Blob storage will remain there for seven days.</span></span> <span data-ttu-id="14271-341">次に、そのファイルは自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="14271-341">It will then be automatically deleted.</span></span>

## <a name="getting-the-list-of-errors"></a><span data-ttu-id="14271-342">エラーの一覧を取得する</span><span class="sxs-lookup"><span data-stu-id="14271-342">Getting the list of errors</span></span>
<span data-ttu-id="14271-343">GetExecutionErrors は、ジョブ実行のエラーのリストを取得するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="14271-343">GetExecutionErrors can be used to get the list of errors in a job execution.</span></span> <span data-ttu-id="14271-344">API は、Execution ID をパラメーターとして取り、JSON リストでエラー メッセージのセットを返します。</span><span class="sxs-lookup"><span data-stu-id="14271-344">The API takes the Execution ID as the parameter, and returns a set of error messages in a JSON list.</span></span>

```json
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionErrors
BODY
{"executionId":"<executionId>"}
```

## <a name="import-and-export-processes"></a><span data-ttu-id="14271-345">プロセスのインポートとエクスポート</span><span class="sxs-lookup"><span data-stu-id="14271-345">Import and export processes</span></span>

<span data-ttu-id="14271-346">次の図は、データ管理パッケージ メソッドを使用してデータ パッケージをインポートする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="14271-346">The following illustration shows how the Data management package methods can be used to import data packages.</span></span>

![データ管理パッケージ メソッドを使用するデータ パッケージ ファイルのインポート](./media/data-package-import.png)

<span data-ttu-id="14271-348">次の図は、データ管理パッケージ メソッドを使用してデータ パッケージをエクスポートする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="14271-348">The following illustration shows how the Data management package methods can be used to export data packages.</span></span>

![データ管理パッケージ メソッドを使用するデータ パッケージ ファイルのエクスポート](./media/data-package-export.png)

<span data-ttu-id="14271-350">データのインポートとデータのエクスポートのメソッドを紹介するサンプルのコンソール アプリケーションは、 GitHub から入手できます。</span><span class="sxs-lookup"><span data-stu-id="14271-350">A sample console application that showcases the data import and data export methods is available on GitHub.</span></span> <span data-ttu-id="14271-351">詳細については、「<https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/FileBasedIntegrationSamples/ConsoleAppSamples>」に移動してください。</span><span class="sxs-lookup"><span data-stu-id="14271-351">For more information, go to <https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/FileBasedIntegrationSamples/ConsoleAppSamples>.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]