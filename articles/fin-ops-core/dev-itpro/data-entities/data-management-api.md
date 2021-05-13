---
title: データ管理パッケージ REST API
description: このトピックでは、データ管理フレームワークのパッケージ REST API について説明します。
author: Sunil-Garg
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2017-03-31
ms.dyn365.ops.version: Platform update 5
ms.openlocfilehash: bfe3df6ea19420ea1011171f2f55175cb685496c
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937346"
---
# <a name="data-management-package-rest-api"></a><span data-ttu-id="6c59f-103">データ管理パッケージ REST API</span><span class="sxs-lookup"><span data-stu-id="6c59f-103">Data management package REST API</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c59f-104">このトピックでは、データ管理フレームワークのパッケージの Representational State Transfer (REST) のアプリケーション プログラミング インターフェイス (API) について説明します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-104">This topic describes the Data management framework's package representational state transfer (REST) application programming interface (API).</span></span> <span data-ttu-id="6c59f-105">パッケージ API により、データ パッケージを使用して統合できます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-105">The package API lets you integrate by using data packages.</span></span> <span data-ttu-id="6c59f-106">REST API はクラウド展開とオンプレミスの展開で使用できます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-106">The REST API can be used with both cloud deployments and on-premises deployments.</span></span> 

<span data-ttu-id="6c59f-107">オンプレミス サポートが追加されましたが、API 名は変更されていません。</span><span class="sxs-lookup"><span data-stu-id="6c59f-107">Although on-premises support has been added, API names haven't been changed.</span></span> <span data-ttu-id="6c59f-108">したがって、Microsoft は、クラウド配置とオンプレミス配置の両方に対して単一の API セットを維持することができます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-108">Therefore, Microsoft can keep a single API set for both cloud deployments and on-premises deployments.</span></span>

## <a name="choosing-an-integration-api"></a><span data-ttu-id="6c59f-109">統合 API の選択</span><span class="sxs-lookup"><span data-stu-id="6c59f-109">Choosing an integration API</span></span>

<span data-ttu-id="6c59f-110">ファイル ベースの統合シナリオは、データ管理フレームワークのパッケージ API と定期的な統合 API の 2 つの API によりサポートされます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-110">Two APIs support file-based integration scenarios: the Data management framework's package API and the recurring integrations API.</span></span> <span data-ttu-id="6c59f-111">どちらの API もデータ インポート シナリオとデータ エクスポート シナリオの両方をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="6c59f-111">Both APIs support both data import scenarios and data export scenarios.</span></span> <span data-ttu-id="6c59f-112">次のテーブルでは、使用する API を決定する際に考慮する必要がある主な決定事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-112">The following table describes the main decision points that you should consider when you're trying to decide which API to use.</span></span>

| <span data-ttu-id="6c59f-113">決定ポイント</span><span class="sxs-lookup"><span data-stu-id="6c59f-113">Decision point</span></span>      | <span data-ttu-id="6c59f-114">定期統合 API</span><span class="sxs-lookup"><span data-stu-id="6c59f-114">Recurring integrations API</span></span> | <span data-ttu-id="6c59f-115">データ管理フレームワークのパッケージ API</span><span class="sxs-lookup"><span data-stu-id="6c59f-115">Data management framework's package API</span></span> |
|---------------------|--------------------------------------|-----------------------------|
| <span data-ttu-id="6c59f-116">スケジューリング</span><span class="sxs-lookup"><span data-stu-id="6c59f-116">Scheduling</span></span>          | <span data-ttu-id="6c59f-117">Finance and Operations アプリのスケジューリング</span><span class="sxs-lookup"><span data-stu-id="6c59f-117">Scheduling in Finance and Operations apps</span></span> | <span data-ttu-id="6c59f-118">Finance and Operations アプリ以外のスケジューリング</span><span class="sxs-lookup"><span data-stu-id="6c59f-118">Scheduling outside Finance and Operations apps</span></span> |
| <span data-ttu-id="6c59f-119">Format</span><span class="sxs-lookup"><span data-stu-id="6c59f-119">Format</span></span>              | <span data-ttu-id="6c59f-120">ファイルおよびデータ パッケージ</span><span class="sxs-lookup"><span data-stu-id="6c59f-120">Files and data packages</span></span> | <span data-ttu-id="6c59f-121">データ パッケージのみ</span><span class="sxs-lookup"><span data-stu-id="6c59f-121">Only data packages</span></span> |
| <span data-ttu-id="6c59f-122">変換</span><span class="sxs-lookup"><span data-stu-id="6c59f-122">Transformation</span></span>      | <span data-ttu-id="6c59f-123">データ ファイルが XML 形式の場合の Extensible Stylesheet Language Transformations (XSLT) のサポート</span><span class="sxs-lookup"><span data-stu-id="6c59f-123">Support for Extensible Stylesheet Language Transformations (XSLT) if the data file is in XML format</span></span> | <span data-ttu-id="6c59f-124">システム外部での変換</span><span class="sxs-lookup"><span data-stu-id="6c59f-124">Transformations that are external to the system</span></span> |
| <span data-ttu-id="6c59f-125">サポートされているプロトコル</span><span class="sxs-lookup"><span data-stu-id="6c59f-125">Supported protocols</span></span> | <span data-ttu-id="6c59f-126">SOAP および REST</span><span class="sxs-lookup"><span data-stu-id="6c59f-126">SOAP and REST</span></span> | <span data-ttu-id="6c59f-127">REST</span><span class="sxs-lookup"><span data-stu-id="6c59f-127">REST</span></span> |
| <span data-ttu-id="6c59f-128">サービス タイプ</span><span class="sxs-lookup"><span data-stu-id="6c59f-128">Service type</span></span>        | <span data-ttu-id="6c59f-129">カスタム サービス</span><span class="sxs-lookup"><span data-stu-id="6c59f-129">Custom service</span></span> | <span data-ttu-id="6c59f-130">データ プロトコル (OData) アクションを開きます</span><span class="sxs-lookup"><span data-stu-id="6c59f-130">Open Data Protocol (OData) action</span></span> |

<span data-ttu-id="6c59f-131">定期的な統合 API がデータ管理フレームワークのパッケージ API よりも要件を満たしていることを決定した場合、[定期統合](recurring-integrations.md) を参照します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-131">If you decide that the recurring integrations API meets your requirement better than the Data management framework's package API, see [Recurring integrations](recurring-integrations.md).</span></span> <span data-ttu-id="6c59f-132">このトピックの残りの部分では、データ管理フレームワークのパッケージ API について説明します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-132">The rest of this topic discusses the Data management framework's package API.</span></span>

## <a name="authorization"></a><span data-ttu-id="6c59f-133">承認</span><span class="sxs-lookup"><span data-stu-id="6c59f-133">Authorization</span></span>

<span data-ttu-id="6c59f-134">データ管理フレームワークのパッケージ API は、アクセスを認可するために OAuth 2.0 を使用します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-134">The Data management framework's package API uses OAuth 2.0 to authorize access.</span></span> <span data-ttu-id="6c59f-135">API は、有効な OAuth アクセス トークンを使用して呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c59f-135">The API must be called by using a valid OAuth access token.</span></span> <span data-ttu-id="6c59f-136">OAuth 2.0 および Microsoft Azure Active Directory(Azure AD) の詳細については、[OAuth 2.0 と Azure Active Directory を使用して Web アプリケーションへのアクセスを承認](/azure/active-directory/develop/active-directory-protocols-oauth-code) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c59f-136">For more information about OAuth 2.0 and Microsoft Azure Active Directory (Azure AD), see [Authorize access to web applications using OAuth 2.0 and Azure Active Directory](/azure/active-directory/develop/active-directory-protocols-oauth-code).</span></span> <span data-ttu-id="6c59f-137">オンプレミス配置では、Active Directory フェデレーション サービス (AD FS) が承認に使用されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-137">For on-premises deployments, Active Directory Federation Services (AD FS) is used for authorization.</span></span>

> [!NOTE]
> <span data-ttu-id="6c59f-138">クライアント資格情報の付与フローを使用すると、アプリケーションはアクセス制御リストを保持します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-138">When you use the Client Credentials Grant flow, the application maintains an access control list.</span></span> <span data-ttu-id="6c59f-139">アクセス制御リストは、**システム管理** \> **設定** \> **Azure Active Directory アプリケーション** を順にクリックして見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-139">You can find the access control list at **System administration** \> **Setup** \> **Azure Active Directory applications**.</span></span> <span data-ttu-id="6c59f-140">**Azure Active Directory アプリケーション** ページには、承認済クライアント ID と、クライアント資格情報付与フローを使用して API が呼び出されたときに適用する必要があるユーザー セキュリティ マッピングが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-140">The **Azure Active Directory applications** page shows the approved client IDs and the user security mapping that should be enforced when the API is called by using the Client Credentials Grant flow.</span></span>
>
> <span data-ttu-id="6c59f-141">オンプレミス配置については、このリストには AD FS からの有効なクライアント ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="6c59f-141">For on-premises deployments, this list must have a valid client ID from AD FS.</span></span> <span data-ttu-id="6c59f-142">また、オンプレミスで使用する場合は、接続の確立時に、次の例にて示されている **\<baseurl\>** に **/namespaces/AXSF** を付加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c59f-142">Additionally, for on-premises use, **\<baseurl\>** in the following examples must append **/namespaces/AXSF** when a connection is made.</span></span>

## <a name="import-apis"></a><span data-ttu-id="6c59f-143">API のインポート</span><span class="sxs-lookup"><span data-stu-id="6c59f-143">Import APIs</span></span>

<span data-ttu-id="6c59f-144">ファイル (データ パッケージ) のインポートには、次の API が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-144">The following APIs are used to import files (data packages).</span></span>

### <a name="getimportstagingerrorfileurl"></a><span data-ttu-id="6c59f-145">GetImportStagingErrorFileUrl</span><span class="sxs-lookup"><span data-stu-id="6c59f-145">GetImportStagingErrorFileUrl</span></span>

<span data-ttu-id="6c59f-146">GetImportStagingErrorFileUrl API は、エラーファイルのURLを取得します。エラーファイルには単一のエンティティに対するインポートの過程で、ステージング段階で失敗したデータが格納されています。</span><span class="sxs-lookup"><span data-stu-id="6c59f-146">The GetImportStagingErrorFileUrl API is used to get the URL of the error file containing the input records that failed at the source to the staging step of import for a single entity.</span></span> <span data-ttu-id="6c59f-147">エラーファイルが生成されなかった場合は、空の文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-147">An empty string is returned if no error file is generated.</span></span>

<span data-ttu-id="6c59f-148">POST /Data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetImportStagingErrorFileUrl</span><span class="sxs-lookup"><span data-stu-id="6c59f-148">POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetImportStagingErrorFileUrl</span></span>

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

<span data-ttu-id="6c59f-149">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6c59f-149">**Input parameters**</span></span>

| <span data-ttu-id="6c59f-150">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c59f-150">Parameter</span></span>     | <span data-ttu-id="6c59f-151">説明</span><span class="sxs-lookup"><span data-stu-id="6c59f-151">Description</span></span> |
|---------------------|--------------------------------------|
| <span data-ttu-id="6c59f-152">string executionId</span><span class="sxs-lookup"><span data-stu-id="6c59f-152">string executionId</span></span>          | <span data-ttu-id="6c59f-153">インポート処理の実行ID。</span><span class="sxs-lookup"><span data-stu-id="6c59f-153">Execution ID of import.</span></span> <span data-ttu-id="6c59f-154">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-154">This is called as Job ID in the UI.</span></span> |
| <span data-ttu-id="6c59f-155">string entityName</span><span class="sxs-lookup"><span data-stu-id="6c59f-155">string entityName</span></span>        | <span data-ttu-id="6c59f-156">エラー ファイルの取得対象となるエンティティの名前。</span><span class="sxs-lookup"><span data-stu-id="6c59f-156">Name of the entity for which to get the error file.</span></span> |


<span data-ttu-id="6c59f-157">**出力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6c59f-157">**Output parameters**</span></span>

| <span data-ttu-id="6c59f-158">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c59f-158">Parameter</span></span>         | <span data-ttu-id="6c59f-159">説明</span><span class="sxs-lookup"><span data-stu-id="6c59f-159">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="6c59f-160">string errorkeysfileurl</span><span class="sxs-lookup"><span data-stu-id="6c59f-160">string errorkeysfileurl</span></span> | <span data-ttu-id="6c59f-161">エラーファイルのURL。</span><span class="sxs-lookup"><span data-stu-id="6c59f-161">The URL of the error file.</span></span> <span data-ttu-id="6c59f-162">エラーファイルが生成されなかった場合は、空の戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-162">The return value is empty if an error file was not generated.</span></span> |


### <a name="generateimporttargeterrorkeysfile"></a><span data-ttu-id="6c59f-163">GenerateImportTargetErrorKeysFile</span><span class="sxs-lookup"><span data-stu-id="6c59f-163">GenerateImportTargetErrorKeysFile</span></span>

<span data-ttu-id="6c59f-164">GenerateImportTargetErrorKeysFile API は、エラーファイルを生成します。エラーファイルには単一のエンティティに対するインポートの過程で、ステージングからターゲットの段階で失敗したインポート レコードのキーが格納されています。</span><span class="sxs-lookup"><span data-stu-id="6c59f-164">The GenerateImportTargetErrorKeysFile API is used to generate an error file containing the keys of the import records that failed at the staging to target step of import for a single entity.</span></span>  

<span data-ttu-id="6c59f-165">このAPIがtrueを返す場合は、GetImportTargetErrorKeysFileUrl API を使用して、生成されたエラーキーファイルのURLを取得します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-165">If this API returns true, then use the GetImportTargetErrorKeysFileUrl API to get the URL of the generated error keys file.</span></span>


<span data-ttu-id="6c59f-166">POST /Data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GenerateImportTargetErrorKeysFile</span><span class="sxs-lookup"><span data-stu-id="6c59f-166">POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GenerateImportTargetErrorKeysFile</span></span>

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

<span data-ttu-id="6c59f-167">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6c59f-167">**Input parameters**</span></span>

| <span data-ttu-id="6c59f-168">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c59f-168">Parameter</span></span>     | <span data-ttu-id="6c59f-169">説明</span><span class="sxs-lookup"><span data-stu-id="6c59f-169">Description</span></span> |
|---------------------|--------------------------------------|
| <span data-ttu-id="6c59f-170">string executionId</span><span class="sxs-lookup"><span data-stu-id="6c59f-170">string executionId</span></span>          | <span data-ttu-id="6c59f-171">インポート処理の実行ID。</span><span class="sxs-lookup"><span data-stu-id="6c59f-171">Execution ID of import</span></span> |
| <span data-ttu-id="6c59f-172">string entityName</span><span class="sxs-lookup"><span data-stu-id="6c59f-172">string entityName</span></span>        | <span data-ttu-id="6c59f-173">エラー ファイルの取得対象となるエンティティの名前。</span><span class="sxs-lookup"><span data-stu-id="6c59f-173">Name of the entity for which to get the error file</span></span> |

<span data-ttu-id="6c59f-174">**出力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6c59f-174">**Output parameters**</span></span>

| <span data-ttu-id="6c59f-175">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c59f-175">Parameter</span></span>     | <span data-ttu-id="6c59f-176">説明</span><span class="sxs-lookup"><span data-stu-id="6c59f-176">Description</span></span> |
|---------------------|--------------------------------------|
| <span data-ttu-id="6c59f-177">ブール値エラーが発生しています</span><span class="sxs-lookup"><span data-stu-id="6c59f-177">Boolean errorsExist</span></span>     | <span data-ttu-id="6c59f-178">インポートエラーが発生した場合はtrue、 インポートエラーが発生しなかった場合はfalseとします</span><span class="sxs-lookup"><span data-stu-id="6c59f-178">true if there are import errors; false if there are no errors</span></span> |

### <a name="getimporttargeterrorkeysfileurl"></a><span data-ttu-id="6c59f-179">GetImportTargetErrorKeysFileUrl</span><span class="sxs-lookup"><span data-stu-id="6c59f-179">GetImportTargetErrorKeysFileUrl</span></span>

<span data-ttu-id="6c59f-180">**GetImportTargetErrorKeysFileUrl** API を使用して、単一のエンティティに対するインポートのステージングからターゲットへのステップで失敗したインポート レコードのキーが格納されているエラー ファイルの URL を取得します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-180">The **GetImportTargetErrorKeysFileUrl** API is used to get the URL of the error file that contains the keys of the import records that failed at the staging-to-target step of import for a single entity.</span></span>

<span data-ttu-id="6c59f-181">エラー ファイルが使用可能な場合、この API はその URL を返します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-181">If the error file is available, this API returns the URL.</span></span> <span data-ttu-id="6c59f-182">エラー ファイルがまだ生成中の場合、またはエラー ファイルが存在しない場合は、API は空の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-182">If the error file is still being generated, or if there is no error file, the API returns an empty string.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="6c59f-183">この API を呼び出す前に、**GenerateImportTargetErrorKeysFile** API を呼出して、エラー ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-183">Before you call this API, call the **GenerateImportTargetErrorKeysFile** API to generate the error file.</span></span> <span data-ttu-id="6c59f-184">**GenerateImportTargetErrorKeysFile** API が **true** を返した場合、空でない文字列が返されるまで、ループでこの API を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-184">If the **GenerateImportTargetErrorKeysFile** API returns **true**, call this API in a loop until it returns a non-empty string.</span></span> <span data-ttu-id="6c59f-185">**GenerateImportTargetErrorKeysFile** API が **false** を返した場合、エラーがないため、この API は空の文字列をかならず返します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-185">If the **GenerateImportTargetErrorKeysFile** API returns **false**, this API will always return an empty string, because there are no errors.</span></span>

<span data-ttu-id="6c59f-186">**疑似コードの例**</span><span class="sxs-lookup"><span data-stu-id="6c59f-186">**Pseudocode example**</span></span>

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

<span data-ttu-id="6c59f-187">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-187">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":"<errorkeysfileurl>"
}
```

<span data-ttu-id="6c59f-188">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6c59f-188">**Input parameters**</span></span>

| <span data-ttu-id="6c59f-189">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c59f-189">Parameter</span></span>         | <span data-ttu-id="6c59f-190">説明</span><span class="sxs-lookup"><span data-stu-id="6c59f-190">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="6c59f-191">string executionId</span><span class="sxs-lookup"><span data-stu-id="6c59f-191">string executionId</span></span> | <span data-ttu-id="6c59f-192">インポートの実行 ID。</span><span class="sxs-lookup"><span data-stu-id="6c59f-192">The execution ID of the import.</span></span> <span data-ttu-id="6c59f-193">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-193">This is called as Job ID in the UI.</span></span>|
| <span data-ttu-id="6c59f-194">string entityName</span><span class="sxs-lookup"><span data-stu-id="6c59f-194">string entityName</span></span> | <span data-ttu-id="6c59f-195">エラー ファイルを取得する対象のエンティティの名前。</span><span class="sxs-lookup"><span data-stu-id="6c59f-195">The name of the entity to get the error file for.</span></span> |

<span data-ttu-id="6c59f-196">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="6c59f-196">**Output parameters**</span></span>

| <span data-ttu-id="6c59f-197">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c59f-197">Parameter</span></span>         | <span data-ttu-id="6c59f-198">説明</span><span class="sxs-lookup"><span data-stu-id="6c59f-198">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="6c59f-199">string errorkeysfileurl</span><span class="sxs-lookup"><span data-stu-id="6c59f-199">string errorkeysfileurl</span></span> | <span data-ttu-id="6c59f-200">エラー キー ファイルが使用可能な場合、そのファイルの URL。</span><span class="sxs-lookup"><span data-stu-id="6c59f-200">The URL of the error keys file, if the file is available.</span></span> <span data-ttu-id="6c59f-201">エラー ファイルがまだ生成中の場合、またはエラー ファイルが存在しない場合は、このメソッドは空の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-201">If the error file is still being generated, or if no errors exist, the method returns an empty string.</span></span> |


### <a name="getazurewritableurl"></a><span data-ttu-id="6c59f-202">GetAzureWritableUrl</span><span class="sxs-lookup"><span data-stu-id="6c59f-202">GetAzureWritableUrl</span></span>

<span data-ttu-id="6c59f-203">**GetAzureWritableUrl** API は、書き込み可能な Blob URL を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-203">The **GetAzureWritableUrl** API is used to get a writable blob URL.</span></span> <span data-ttu-id="6c59f-204">このメソッドには、URL に埋め込まれた共有アクセス署名 (SAS) トークンが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6c59f-204">The method includes a shared access signature (SAS) token that is embedded in the URL.</span></span> <span data-ttu-id="6c59f-205">この方法を使用すると、Azure Blob Storage コンテナーにデータ パッケージをアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-205">You can use this method to upload a data package to the Azure Blob storage container.</span></span> <span data-ttu-id="6c59f-206">オンプレミス配置の場合、この API はローカル ストレージに取り込まれた URL を引き続き返します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-206">For on-premises deployments, this API will still return the URL that has been abstracted to local storage.</span></span>

> [!NOTE]
> <span data-ttu-id="6c59f-207">SAS は有効期限の時間枠中にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="6c59f-207">An SAS is valid only during an expiry time window.</span></span> <span data-ttu-id="6c59f-208">ウィンドウが経過した後に発行されるすべての要求はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-208">Any request that is issued after the window has passed returns an error.</span></span> <span data-ttu-id="6c59f-209">詳細については、[共有アクセス署名 (SA) の使用](/azure/storage/common/storage-dotnet-shared-access-signature-part-1) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c59f-209">For more information, see [Using shared access signatures (SAS)](/azure/storage/common/storage-dotnet-shared-access-signature-part-1).</span></span>

```csharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetAzureWriteUrl
BODY
{
    "uniqueFileName":"<string>"
}
```

<span data-ttu-id="6c59f-210">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-210">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value": "{\"BlobId\":\"{<GUID>}\",\"BlobUrl\":\"https://<baseurl_id>.blob.core.windows.net/dmf/<uniqueFileName>?<SAS Token>\"}"
    }
}
```

<span data-ttu-id="6c59f-211">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6c59f-211">**Input parameters**</span></span>

| <span data-ttu-id="6c59f-212">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c59f-212">Parameter</span></span>         | <span data-ttu-id="6c59f-213">説明</span><span class="sxs-lookup"><span data-stu-id="6c59f-213">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="6c59f-214">文字列 uniqueFileName</span><span class="sxs-lookup"><span data-stu-id="6c59f-214">string uniqueFileName</span></span> | <span data-ttu-id="6c59f-215">BLOB ID を追跡するために使用される一意のファイル名。</span><span class="sxs-lookup"><span data-stu-id="6c59f-215">A unique file name that is used to track blob IDs.</span></span> <span data-ttu-id="6c59f-216">一意のファイル名であることを保証するため、グローバル一意識別子 (GUID) を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-216">You can include a globally unique identifier (GUID) to help guarantee a unique file name.</span></span> |

<span data-ttu-id="6c59f-217">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="6c59f-217">**Output parameters**</span></span>

| <span data-ttu-id="6c59f-218">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c59f-218">Parameter</span></span>      | <span data-ttu-id="6c59f-219">説明</span><span class="sxs-lookup"><span data-stu-id="6c59f-219">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="6c59f-220">string BlobId</span><span class="sxs-lookup"><span data-stu-id="6c59f-220">string BlobId</span></span>  | <span data-ttu-id="6c59f-221">割り当てられた BLOB コンテナーの BLOB ID。</span><span class="sxs-lookup"><span data-stu-id="6c59f-221">The blob ID of the allocated blob container.</span></span> |
| <span data-ttu-id="6c59f-222">string BlobUrl</span><span class="sxs-lookup"><span data-stu-id="6c59f-222">string BlobUrl</span></span> | <span data-ttu-id="6c59f-223">埋め込みの SAS トークンを持つ URL。</span><span class="sxs-lookup"><span data-stu-id="6c59f-223">A URL that has an embedded SAS token.</span></span> <span data-ttu-id="6c59f-224">URL を使用 して Blob ストレージに書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-224">The URL can be used to write to Blob storage.</span></span> |

### <a name="importfrompackage"></a><span data-ttu-id="6c59f-225">ImportFromPackage</span><span class="sxs-lookup"><span data-stu-id="6c59f-225">ImportFromPackage</span></span>

<span data-ttu-id="6c59f-226">**ImportFromPackage** API は、実装に関連付けられている Blob ストレージにアップロードされるデータ パッケージからインポートを開始するために使用します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-226">The **ImportFromPackage** API is used to initiate an import from the data package that is uploaded to the Blob storage that is associated with your implementation.</span></span> <span data-ttu-id="6c59f-227">オンプレミス配置の場合、ファイルが以前アップロードされたローカル ストレージから、インポートが開始されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-227">For on-premises deployments, the import will be initiated from the local storage that the file was uploaded previously to.</span></span>

> [!NOTE]
> <span data-ttu-id="6c59f-228">**ImportFromPackage** API は、複合エンティティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6c59f-228">The **ImportFromPackage** API supports composite entities.</span></span> <span data-ttu-id="6c59f-229">ただし、1 つのパッケージで 1 つの複合エンティティのみという制限があります。</span><span class="sxs-lookup"><span data-stu-id="6c59f-229">However, the limitation is that there can be only one composite entity in a package.</span></span>

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

<span data-ttu-id="6c59f-230">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-230">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":"<executionId>"
}
```

<span data-ttu-id="6c59f-231">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6c59f-231">**Input parameters**</span></span>

| <span data-ttu-id="6c59f-232">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c59f-232">Parameter</span></span>                | <span data-ttu-id="6c59f-233">説明</span><span class="sxs-lookup"><span data-stu-id="6c59f-233">Description</span></span> |
|--------------------------|-------------|
| <span data-ttu-id="6c59f-234">string packageUrl</span><span class="sxs-lookup"><span data-stu-id="6c59f-234">string packageUrl</span></span>        | <span data-ttu-id="6c59f-235">Finance and Operations アプリに関連付けられている Blob Storage 内のデータ パッケージの URL。</span><span class="sxs-lookup"><span data-stu-id="6c59f-235">The URL of the data package in the Blob storage that is associated with a Finance and Operations app.</span></span> |
| <span data-ttu-id="6c59f-236">string definitionGroupId</span><span class="sxs-lookup"><span data-stu-id="6c59f-236">string definitionGroupId</span></span> | <span data-ttu-id="6c59f-237">インポート用のデータ プロジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="6c59f-237">The name of the data project for import.</span></span> |
| <span data-ttu-id="6c59f-238">string executionId</span><span class="sxs-lookup"><span data-stu-id="6c59f-238">string executionId</span></span>       | <span data-ttu-id="6c59f-239">ジョブに使用する ID。</span><span class="sxs-lookup"><span data-stu-id="6c59f-239">The ID to use for the job.</span></span> <span data-ttu-id="6c59f-240">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-240">This is called as Job ID in the UI.</span></span> <span data-ttu-id="6c59f-241">空の ID が割り当てられている場合は、新しい実行 ID が作成されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-241">If an empty ID is assigned, a new execution ID will be created.</span></span> |
| <span data-ttu-id="6c59f-242">bool execute</span><span class="sxs-lookup"><span data-stu-id="6c59f-242">bool execute</span></span>             | <span data-ttu-id="6c59f-243">このパラメーターを **True** に設定して対象の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-243">Set this parameter to **True** to run the target step.</span></span> <span data-ttu-id="6c59f-244">それ以外の場合、**False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-244">Otherwise, set it to **False**.</span></span> |
| <span data-ttu-id="6c59f-245">bool overwrite</span><span class="sxs-lookup"><span data-stu-id="6c59f-245">bool overwrite</span></span>           | <span data-ttu-id="6c59f-246">パッケージ内で複合エンティティを使用する場合は、このパラメーターを常に **False** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c59f-246">This parameter must always be set to **False** when a composite entity is used in a package.</span></span> <span data-ttu-id="6c59f-247">それ以外の場合、**True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-247">Otherwise, set it to **True**.</span></span> |
| <span data-ttu-id="6c59f-248">string legalEntityId</span><span class="sxs-lookup"><span data-stu-id="6c59f-248">string legalEntityId</span></span>     | <span data-ttu-id="6c59f-249">データ インポートの法人。</span><span class="sxs-lookup"><span data-stu-id="6c59f-249">The legal entity for the data import.</span></span> |

<span data-ttu-id="6c59f-250">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="6c59f-250">**Output parameters**</span></span>

| <span data-ttu-id="6c59f-251">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c59f-251">Parameter</span></span>          | <span data-ttu-id="6c59f-252">説明</span><span class="sxs-lookup"><span data-stu-id="6c59f-252">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="6c59f-253">string executionId</span><span class="sxs-lookup"><span data-stu-id="6c59f-253">string executionId</span></span> | <span data-ttu-id="6c59f-254">データ インポートの実行 ID。</span><span class="sxs-lookup"><span data-stu-id="6c59f-254">The execution ID of the data import.</span></span> <span data-ttu-id="6c59f-255">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-255">This is called as Job ID in the UI.</span></span> |

> [!NOTE]
> <span data-ttu-id="6c59f-256">**ImportFromPackage()** はバッチを使用してインポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-256">**ImportFromPackage()** uses a batch to perform the import.</span></span> <span data-ttu-id="6c59f-257">したがって、並行インポートを実行するために、データ管理で並列処理ルールを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c59f-257">Therefore, parallel processing rules must be used in Data management to perform parallel imports.</span></span> <span data-ttu-id="6c59f-258">**ImportFromPackage()** を並列スレッドで呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="6c59f-258">**ImportFromPackage()** must not be called in parallel threads.</span></span> <span data-ttu-id="6c59f-259">それ以外の場合、これは失敗します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-259">Otherwise, it will fail.</span></span>

## <a name="export-apis"></a><span data-ttu-id="6c59f-260">API をエキスポート</span><span class="sxs-lookup"><span data-stu-id="6c59f-260">Export APIs</span></span>

<span data-ttu-id="6c59f-261">ファイル (データ パッケージ) のエクスポートには、次の API が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-261">The following APIs are used to export files (data packages).</span></span>

### <a name="exporttopackage"></a><span data-ttu-id="6c59f-262">ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="6c59f-262">ExportToPackage</span></span>

<span data-ttu-id="6c59f-263">**ExportToPackage** API は、データ パッケージのエクスポートを開始するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-263">The **ExportToPackage** API is used to initiate an export of a data package.</span></span> <span data-ttu-id="6c59f-264">この API は、クラウド配置とオンプレミス配置の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-264">This API is applicable to both cloud deployments and on-premises deployments.</span></span>

- <span data-ttu-id="6c59f-265">この API を呼び出す前に、エクスポート データ プロジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c59f-265">The export data project must be created before you call this API.</span></span> <span data-ttu-id="6c59f-266">プロジェクトが存在しない場合、API の呼び出しには、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-266">If the project doesn't exist, a call to the API returns an error.</span></span>
- <span data-ttu-id="6c59f-267">変更履歴がオンの場合は、最後の実行後に更新または作成されたレコードのみがエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-267">If change tracking has been turned on, only records that have been created or updated since the last run are exported.</span></span> <span data-ttu-id="6c59f-268">(つまり、デルタのみが返されます。)</span><span class="sxs-lookup"><span data-stu-id="6c59f-268">(In other words, only the delta is returned.)</span></span>

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

<span data-ttu-id="6c59f-269">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-269">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"<executionId>"
    }
}
```

<span data-ttu-id="6c59f-270">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6c59f-270">**Input parameters**</span></span>

| <span data-ttu-id="6c59f-271">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c59f-271">Parameter</span></span>                | <span data-ttu-id="6c59f-272">説明</span><span class="sxs-lookup"><span data-stu-id="6c59f-272">Description</span></span> |
|--------------------------|-------------|
| <span data-ttu-id="6c59f-273">string definitionGroupId</span><span class="sxs-lookup"><span data-stu-id="6c59f-273">string definitionGroupId</span></span> | <span data-ttu-id="6c59f-274">エクスポート用のデータ プロジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="6c59f-274">The name of the data project for export.</span></span> |
| <span data-ttu-id="6c59f-275">string packageName</span><span class="sxs-lookup"><span data-stu-id="6c59f-275">string packageName</span></span>       | <span data-ttu-id="6c59f-276">エクスポートされたデータ パッケージの名前。</span><span class="sxs-lookup"><span data-stu-id="6c59f-276">The name of the exported data package.</span></span> |
| <span data-ttu-id="6c59f-277">string executionId</span><span class="sxs-lookup"><span data-stu-id="6c59f-277">string executionId</span></span>       | <span data-ttu-id="6c59f-278">ジョブに使用する ID。</span><span class="sxs-lookup"><span data-stu-id="6c59f-278">The ID to use for the job.</span></span> <span data-ttu-id="6c59f-279">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-279">This is called as Job ID in the UI.</span></span> <span data-ttu-id="6c59f-280">空の ID が割り当てられている場合は、新しい実行 ID が作成されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-280">If an empty ID is assigned, a new execution ID will be created.</span></span> |
| <span data-ttu-id="6c59f-281">bool reExecute</span><span class="sxs-lookup"><span data-stu-id="6c59f-281">bool reExecute</span></span>           | <span data-ttu-id="6c59f-282">このパラメーターを **True** に設定して対象の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-282">Set this parameter to **True** to run the target step.</span></span> <span data-ttu-id="6c59f-283">それ以外の場合、**False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-283">Otherwise, set it to **False**.</span></span> |
| <span data-ttu-id="6c59f-284">string legalEntityId</span><span class="sxs-lookup"><span data-stu-id="6c59f-284">string legalEntityId</span></span>     | <span data-ttu-id="6c59f-285">データ インポートの法人。</span><span class="sxs-lookup"><span data-stu-id="6c59f-285">The legal entity for the data import.</span></span> |
    
<span data-ttu-id="6c59f-286">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="6c59f-286">**Output parameters**</span></span>

| <span data-ttu-id="6c59f-287">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c59f-287">Parameter</span></span>          | <span data-ttu-id="6c59f-288">説明</span><span class="sxs-lookup"><span data-stu-id="6c59f-288">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="6c59f-289">string executionId</span><span class="sxs-lookup"><span data-stu-id="6c59f-289">string executionId</span></span> | <span data-ttu-id="6c59f-290">データ エクスポートの実行 ID。</span><span class="sxs-lookup"><span data-stu-id="6c59f-290">The execution ID of the data export.</span></span> <span data-ttu-id="6c59f-291">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-291">This is called as Job ID in the UI.</span></span> |

### <a name="getexportedpackageurl"></a><span data-ttu-id="6c59f-292">GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="6c59f-292">GetExportedPackageUrl</span></span>

<span data-ttu-id="6c59f-293">**GetExportedPackageUrl** API は、**ExportToPackage** を呼び出すことでエクスポートされたデータ パッケージの URL を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-293">The **GetExportedPackageUrl** API is used to get the URL of the data package that was exported by a call to **ExportToPackage**.</span></span> <span data-ttu-id="6c59f-294">この API は、クラウド配置とオンプレミス配置の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-294">This API is applicable to both cloud deployments and on-premises deployments.</span></span>

```csharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
BODY
{"executionId":"<Execution Id>"}
```

<span data-ttu-id="6c59f-295">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-295">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"https://<baseurl_id>.blob.core.windows.net/dmf/<uniqueFileName>?<SAS Token>"
    }
}
```

<span data-ttu-id="6c59f-296">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6c59f-296">**Input parameters**</span></span>

| <span data-ttu-id="6c59f-297">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c59f-297">Parameter</span></span>          | <span data-ttu-id="6c59f-298">説明</span><span class="sxs-lookup"><span data-stu-id="6c59f-298">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="6c59f-299">string executionId</span><span class="sxs-lookup"><span data-stu-id="6c59f-299">string executionId</span></span> | <span data-ttu-id="6c59f-300">データ プロジェクト実行の実行 ID。</span><span class="sxs-lookup"><span data-stu-id="6c59f-300">The execution ID of the data project run.</span></span> <span data-ttu-id="6c59f-301">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-301">This is called as Job ID in the UI.</span></span> |

<span data-ttu-id="6c59f-302">**出力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6c59f-302">**Output parameters**</span></span>

| <span data-ttu-id="6c59f-303">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c59f-303">Parameter</span></span>      | <span data-ttu-id="6c59f-304">説明</span><span class="sxs-lookup"><span data-stu-id="6c59f-304">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="6c59f-305">string BlobUrl</span><span class="sxs-lookup"><span data-stu-id="6c59f-305">string BlobUrl</span></span> | <span data-ttu-id="6c59f-306">埋め込みの SAS トークンを持つ blob URL。</span><span class="sxs-lookup"><span data-stu-id="6c59f-306">A blob URL that has an embedded SAS token.</span></span> <span data-ttu-id="6c59f-307">URL を使用して、エクスポートしたデータ パッケージをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-307">The URL can be used to download the exported data package.</span></span> |

## <a name="status-check-api"></a><span data-ttu-id="6c59f-308">ステータス チェック API</span><span class="sxs-lookup"><span data-stu-id="6c59f-308">Status check API</span></span> 

<span data-ttu-id="6c59f-309">状態を確認するには、次の API を使用します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-309">The following APIs are used to check status.</span></span> <span data-ttu-id="6c59f-310">これらは、インポート フローとエクスポート フローの両方で使用されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-310">They are used during both import flows and export flows.</span></span>

### <a name="getexecutionsummarystatus"></a><span data-ttu-id="6c59f-311">GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="6c59f-311">GetExecutionSummaryStatus</span></span>

<span data-ttu-id="6c59f-312">**GetExecutionSummaryStatus** API は、インポート ジョブとエクスポート ジョブの両方に使用されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-312">The **GetExecutionSummaryStatus** API is used for both import jobs and export jobs.</span></span> <span data-ttu-id="6c59f-313">これは、データ プロジェクト実行ジョブのステータスの確認に使用されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-313">It's used to check the status of a data project execution job.</span></span> <span data-ttu-id="6c59f-314">この API は、クラウド配置とオンプレミス配置の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-314">This API is applicable to both cloud deployments and on-premises deployments.</span></span>

```csharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
BODY
{"executionId":"<executionId>"}
```

<span data-ttu-id="6c59f-315">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-315">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":"<executionStatus>"
}
```

<span data-ttu-id="6c59f-316">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6c59f-316">**Input parameters**</span></span>

| <span data-ttu-id="6c59f-317">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c59f-317">Parameter</span></span>          | <span data-ttu-id="6c59f-318">説明</span><span class="sxs-lookup"><span data-stu-id="6c59f-318">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="6c59f-319">string executionId</span><span class="sxs-lookup"><span data-stu-id="6c59f-319">string executionId</span></span> | <span data-ttu-id="6c59f-320">データ プロジェクト実行の実行 ID。</span><span class="sxs-lookup"><span data-stu-id="6c59f-320">The execution ID of the data project run.</span></span> <span data-ttu-id="6c59f-321">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-321">This is called as Job ID in the UI.</span></span> |

<span data-ttu-id="6c59f-322">**出力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="6c59f-322">**Output parameters**</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6c59f-323">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c59f-323">Parameter</span></span></th>
<th><span data-ttu-id="6c59f-324">説明</span><span class="sxs-lookup"><span data-stu-id="6c59f-324">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c59f-325">DMFExecutionSummaryStatus executionStatus</span><span class="sxs-lookup"><span data-stu-id="6c59f-325">DMFExecutionSummaryStatus executionStatus</span></span></td>
<td><span data-ttu-id="6c59f-326">実行のステータス。</span><span class="sxs-lookup"><span data-stu-id="6c59f-326">The execution status.</span></span> <span data-ttu-id="6c59f-327">以下に使用可能な値を示します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-327">Here are the possible values:</span></span>
<ul>
<li><span data-ttu-id="6c59f-328">不明</span><span class="sxs-lookup"><span data-stu-id="6c59f-328">Unknown</span></span></li>
<li><span data-ttu-id="6c59f-329">NotRun</span><span class="sxs-lookup"><span data-stu-id="6c59f-329">NotRun</span></span></li>
<li><span data-ttu-id="6c59f-330">実行中</span><span class="sxs-lookup"><span data-stu-id="6c59f-330">Executing</span></span></li>
<li><span data-ttu-id="6c59f-331">成功</span><span class="sxs-lookup"><span data-stu-id="6c59f-331">Succeeded</span></span></li>
<li><span data-ttu-id="6c59f-332">PartiallySucceeded</span><span class="sxs-lookup"><span data-stu-id="6c59f-332">PartiallySucceeded</span></span></li>
<li><span data-ttu-id="6c59f-333">失敗</span><span class="sxs-lookup"><span data-stu-id="6c59f-333">Failed</span></span></li>
<li><span data-ttu-id="6c59f-334">取消済</span><span class="sxs-lookup"><span data-stu-id="6c59f-334">Canceled</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6c59f-335">Blob ストレージ内のファイルはストレージに 7 日間残ります。</span><span class="sxs-lookup"><span data-stu-id="6c59f-335">The file in Blob storage will remain there for seven days.</span></span> <span data-ttu-id="6c59f-336">次に、そのファイルは自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-336">It will then be automatically deleted.</span></span>

## <a name="getting-the-list-of-errors"></a><span data-ttu-id="6c59f-337">エラーの一覧を取得する</span><span class="sxs-lookup"><span data-stu-id="6c59f-337">Getting the list of errors</span></span>
<span data-ttu-id="6c59f-338">GetExecutionErrors は、ジョブ実行のエラーのリストを取得するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-338">GetExecutionErrors can be used to get the list of errors in a job execution.</span></span> <span data-ttu-id="6c59f-339">API は、Execution ID をパラメーターとして取り、JSON リストでエラー メッセージのセットを返します。</span><span class="sxs-lookup"><span data-stu-id="6c59f-339">The API takes the Execution ID as the parameter, and returns a set of error messages in a JSON list.</span></span>

```json
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionErrors
BODY
{"executionId":"<executionId>"}
```

## <a name="import-and-export-processes"></a><span data-ttu-id="6c59f-340">プロセスのインポートとエクスポート</span><span class="sxs-lookup"><span data-stu-id="6c59f-340">Import and export processes</span></span>

<span data-ttu-id="6c59f-341">次の図は、データ管理パッケージ メソッドを使用してデータ パッケージをインポートする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="6c59f-341">The following illustration shows how the Data management package methods can be used to import data packages.</span></span>

![データ管理パッケージ メソッドを使用するデータ パッケージ ファイルのインポート](./media/data-package-import.png)

<span data-ttu-id="6c59f-343">次の図は、データ管理パッケージ メソッドを使用してデータ パッケージをエクスポートする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="6c59f-343">The following illustration shows how the Data management package methods can be used to export data packages.</span></span>

![データ管理パッケージ メソッドを使用するデータ パッケージ ファイルのエクスポート](./media/data-package-export.png)

<span data-ttu-id="6c59f-345">データのインポートとデータのエクスポートのメソッドを紹介するサンプルのコンソール アプリケーションは、 GitHub から入手できます。</span><span class="sxs-lookup"><span data-stu-id="6c59f-345">A sample console application that showcases the data import and data export methods is available on GitHub.</span></span> <span data-ttu-id="6c59f-346">詳細については、「<https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/FileBasedIntegrationSamples/ConsoleAppSamples>」に移動してください。</span><span class="sxs-lookup"><span data-stu-id="6c59f-346">For more information, go to <https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/FileBasedIntegrationSamples/ConsoleAppSamples>.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
