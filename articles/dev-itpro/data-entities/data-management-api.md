---
title: データ管理パッケージ REST API
description: このトピックでは、データ管理フレームワークのパッケージ REST API について説明します。
author: Sunil-Garg
ms.date: 05/09/2019
manager: AnnBe
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2017-03-31
ms.dyn365.ops.version: Platform update 5
ms.openlocfilehash: 98bbe292a662bf96301952ea41bffe7e8aa1a8ef
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850421"
---
# <a name="data-management-package-rest-api"></a><span data-ttu-id="298ea-103">データ管理パッケージ REST API</span><span class="sxs-lookup"><span data-stu-id="298ea-103">Data management package REST API</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="298ea-104">このトピックでは、データ管理フレームワークのパッケージの Representational State Transfer (REST) のアプリケーション プログラミング インターフェイス (API) について説明します。</span><span class="sxs-lookup"><span data-stu-id="298ea-104">This topic describes the Data management framework's package representational state transfer (REST) application programming interface (API).</span></span> <span data-ttu-id="298ea-105">パッケージ API により、データ パッケージを使用して Microsoft Dynamics 365 for Finance and Operations と統合できます。</span><span class="sxs-lookup"><span data-stu-id="298ea-105">The package API lets you integrate with Microsoft Dynamics 365 for Finance and Operations by using data packages.</span></span> <span data-ttu-id="298ea-106">REST API は、クラウド配置とオンプレミス配置の両方で使用できます。</span><span class="sxs-lookup"><span data-stu-id="298ea-106">The REST API can be used with both cloud deployments and on-premises deployments.</span></span> <span data-ttu-id="298ea-107">オンプレミス配置では、現在この機能は、Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition プラットフォーム更新プログラム 12 (2017 年 11 月) (バージョン 7.2)、ビルド 7.0.4709.41184 以降で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="298ea-107">For on-premises deployments, this functionality is currently available for Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with platform update 12 (November 2017) (version 7.2), build 7.0.4709.41184, and later.</span></span>

<span data-ttu-id="298ea-108">オンプレミス サポートが追加されましたが、API 名は変更されていません。</span><span class="sxs-lookup"><span data-stu-id="298ea-108">Although on-premises support has been added, API names haven't been changed.</span></span> <span data-ttu-id="298ea-109">したがって、Microsoft は、クラウド配置とオンプレミス配置の両方に対して単一の API セットを維持することができます。</span><span class="sxs-lookup"><span data-stu-id="298ea-109">Therefore, Microsoft can keep a single API set for both cloud deployments and on-premises deployments.</span></span>

## <a name="choosing-an-integration-api"></a><span data-ttu-id="298ea-110">統合 API の選択</span><span class="sxs-lookup"><span data-stu-id="298ea-110">Choosing an integration API</span></span>

<span data-ttu-id="298ea-111">Finance and Operations の 2 つの API である、データ管理フレームワークのパッケージ API と定期的な統合 API が、ファイル ベースの統合シナリオをサポートします。</span><span class="sxs-lookup"><span data-stu-id="298ea-111">Two APIs in Finance and Operations support file-based integration scenarios: the Data management framework's package API and the recurring integrations API.</span></span> <span data-ttu-id="298ea-112">どちらの API もデータ インポート シナリオとデータ エクスポート シナリオの両方をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="298ea-112">Both APIs support both data import scenarios and data export scenarios.</span></span> <span data-ttu-id="298ea-113">次のテーブルでは、使用する API を決定する際に考慮する必要がある主な決定事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="298ea-113">The following table describes the main decision points that you should consider when you're trying to decide which API to use.</span></span>

| <span data-ttu-id="298ea-114">決定ポイント</span><span class="sxs-lookup"><span data-stu-id="298ea-114">Decision point</span></span>      | <span data-ttu-id="298ea-115">定期統合 API</span><span class="sxs-lookup"><span data-stu-id="298ea-115">Recurring integrations API</span></span> | <span data-ttu-id="298ea-116">データ管理フレームワークのパッケージ API</span><span class="sxs-lookup"><span data-stu-id="298ea-116">Data management framework's package API</span></span> |
|---------------------|--------------------------------------|-----------------------------|
| <span data-ttu-id="298ea-117">スケジューリング</span><span class="sxs-lookup"><span data-stu-id="298ea-117">Scheduling</span></span>          | <span data-ttu-id="298ea-118">Finance and Operations のスケジュール設定</span><span class="sxs-lookup"><span data-stu-id="298ea-118">Scheduling in Finance and Operations</span></span> | <span data-ttu-id="298ea-119">Finance and Operations 外でのスケジュール設定</span><span class="sxs-lookup"><span data-stu-id="298ea-119">Scheduling outside Finance and Operations</span></span> |
| <span data-ttu-id="298ea-120">書式設定</span><span class="sxs-lookup"><span data-stu-id="298ea-120">Format</span></span>              | <span data-ttu-id="298ea-121">ファイルおよびデータ パッケージ</span><span class="sxs-lookup"><span data-stu-id="298ea-121">Files and data packages</span></span> | <span data-ttu-id="298ea-122">データ パッケージのみ</span><span class="sxs-lookup"><span data-stu-id="298ea-122">Only data packages</span></span> |
| <span data-ttu-id="298ea-123">変換</span><span class="sxs-lookup"><span data-stu-id="298ea-123">Transformation</span></span>      | <span data-ttu-id="298ea-124">データ ファイルが XML 形式の場合の Extensible Stylesheet Language Transformations (XSLT) のサポート</span><span class="sxs-lookup"><span data-stu-id="298ea-124">Support for Extensible Stylesheet Language Transformations (XSLT) if the data file is in XML format</span></span> | <span data-ttu-id="298ea-125">システム外部での変換</span><span class="sxs-lookup"><span data-stu-id="298ea-125">Transformations that are external to the system</span></span> |
| <span data-ttu-id="298ea-126">サポートされているプロトコル</span><span class="sxs-lookup"><span data-stu-id="298ea-126">Supported protocols</span></span> | <span data-ttu-id="298ea-127">SOAP および REST</span><span class="sxs-lookup"><span data-stu-id="298ea-127">SOAP and REST</span></span> | <span data-ttu-id="298ea-128">REST</span><span class="sxs-lookup"><span data-stu-id="298ea-128">REST</span></span> |
| <span data-ttu-id="298ea-129">サービス タイプ</span><span class="sxs-lookup"><span data-stu-id="298ea-129">Service type</span></span>        | <span data-ttu-id="298ea-130">顧客サービス</span><span class="sxs-lookup"><span data-stu-id="298ea-130">Custom service</span></span> | <span data-ttu-id="298ea-131">データ プロトコル (OData) アクションを開きます</span><span class="sxs-lookup"><span data-stu-id="298ea-131">Open Data Protocol (OData) action</span></span> |
| <span data-ttu-id="298ea-132">在庫状態</span><span class="sxs-lookup"><span data-stu-id="298ea-132">Availability</span></span>        | <span data-ttu-id="298ea-133">Microsoft Dynamics Finance and Operations (2016年2月) 以降。</span><span class="sxs-lookup"><span data-stu-id="298ea-133">Microsoft Dynamics Finance and Operations (February 2016) and later.</span></span> <span data-ttu-id="298ea-134">注意: この機能は、オンプレミス バージョンの Dynamics 365 for Finance and Operations には対応していません。</span><span class="sxs-lookup"><span data-stu-id="298ea-134">Note: This is not supported with the on-premises version of Dynamics 365 for Finance and Operations.</span></span> | <span data-ttu-id="298ea-135">Microsoft Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 5 (2017 年 3 月) およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="298ea-135">Microsoft Dynamics 365 for Finance and Operations with platform update 5 (March 2017) and later</span></span> |

<span data-ttu-id="298ea-136">定期的な統合 API がデータ管理フレームワークのパッケージ API よりも要件を満たしていることを決定した場合、[定期統合](recurring-integrations.md) を参照します。</span><span class="sxs-lookup"><span data-stu-id="298ea-136">If you decide that the recurring integrations API meets your requirement better than the Data management framework's package API, see [Recurring integrations](recurring-integrations.md).</span></span> <span data-ttu-id="298ea-137">このトピックの残りの部分では、データ管理フレームワークのパッケージ API について説明します。</span><span class="sxs-lookup"><span data-stu-id="298ea-137">The rest of this topic discusses the Data management framework's package API.</span></span>

## <a name="authorization"></a><span data-ttu-id="298ea-138">承認</span><span class="sxs-lookup"><span data-stu-id="298ea-138">Authorization</span></span>

<span data-ttu-id="298ea-139">データ管理フレームワークのパッケージ API は、アクセスを認可するために OAuth 2.0 を使用します。</span><span class="sxs-lookup"><span data-stu-id="298ea-139">The Data management framework's package API uses OAuth 2.0 to authorize access.</span></span> <span data-ttu-id="298ea-140">API は、有効な OAuth アクセス トークンを使用して呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="298ea-140">The API must be called by using a valid OAuth access token.</span></span> <span data-ttu-id="298ea-141">OAuth 2.0 および Microsoft Azure Active Directory(Azure AD) の詳細については、[OAuth 2.0 と Azure Active Directory を使用して Web アプリケーションへのアクセスを承認](/azure/active-directory/develop/active-directory-protocols-oauth-code) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="298ea-141">For more information about OAuth 2.0 and Microsoft Azure Active Directory (Azure AD), see [Authorize access to web applications using OAuth 2.0 and Azure Active Directory](/azure/active-directory/develop/active-directory-protocols-oauth-code).</span></span> <span data-ttu-id="298ea-142">オンプレミス配置では、Active Directory フェデレーション サービス (AD FS) が承認に使用されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-142">For on-premises deployments, Active Directory Federation Services (AD FS) is used for authorization.</span></span>

> [!NOTE]
> <span data-ttu-id="298ea-143">クライアント資格情報の付与フローを使用すると、Finance and Operations はアクセス制御リストを保持します。</span><span class="sxs-lookup"><span data-stu-id="298ea-143">When you use the Client Credentials Grant flow, Finance and Operations maintains an access control list.</span></span> <span data-ttu-id="298ea-144">アクセス制御リストは、**システム管理** \> **設定** \> **Azure Active Directory アプリケーション** を順にクリックして見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="298ea-144">You can find the access control list at **System administration** \> **Setup** \> **Azure Active Directory applications**.</span></span> <span data-ttu-id="298ea-145">**Azure Active Directory アプリケーション** ページには、承認済クライアント ID と、クライアント資格情報付与フローを使用して API が呼び出されたときに適用する必要があるユーザー セキュリティ マッピングが表示されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-145">The **Azure Active Directory applications** page shows the approved client IDs and the user security mapping that should be enforced when the API is called by using the Client Credentials Grant flow.</span></span>
>
> <span data-ttu-id="298ea-146">オンプレミス配置については、このリストには AD FS からの有効なクライアント ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="298ea-146">For on-premises deployments, this list must have a valid client ID from AD FS.</span></span> <span data-ttu-id="298ea-147">また、オンプレミスでの使用の場合、Finance and Operations に接続するとき、次の例の **\<baseurl\>** に **/namespaces/AXSF** を付加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="298ea-147">Additionally, for on-premises use, **\<baseurl\>** in the following examples must append **/namespaces/AXSF** when a connection is made to Finance and Operations.</span></span>

## <a name="import-apis"></a><span data-ttu-id="298ea-148">API のインポート</span><span class="sxs-lookup"><span data-stu-id="298ea-148">Import APIs</span></span>

<span data-ttu-id="298ea-149">ファイル (データ パッケージ) のインポートには、次の API が使用されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-149">The following APIs are used to import files (data packages).</span></span>

### <a name="getimportstagingerrorfileurl"></a><span data-ttu-id="298ea-150">GetImportStagingErrorFileUrl</span><span class="sxs-lookup"><span data-stu-id="298ea-150">GetImportStagingErrorFileUrl</span></span>

<span data-ttu-id="298ea-151">GetImportStagingErrorFileUrl API は、エラーファイルのURLを取得します。エラーファイルには単一のエンティティに対するインポートの過程で、ステージング段階で失敗したデータが格納されています。</span><span class="sxs-lookup"><span data-stu-id="298ea-151">The GetImportStagingErrorFileUrl API is used to get the URL of the error file containing the input records that failed at the source to the staging step of import for a single entity.</span></span> <span data-ttu-id="298ea-152">エラーファイルが生成されなかった場合は、空の文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-152">An empty string is returned if no error file is generated.</span></span>

<span data-ttu-id="298ea-153">POST /Data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetImportStagingErrorFileUrl</span><span class="sxs-lookup"><span data-stu-id="298ea-153">POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetImportStagingErrorFileUrl</span></span>

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

<span data-ttu-id="298ea-154">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="298ea-154">**Input parameters**</span></span>

| <span data-ttu-id="298ea-155">パラメーター</span><span class="sxs-lookup"><span data-stu-id="298ea-155">Parameter</span></span>     | <span data-ttu-id="298ea-156">説明</span><span class="sxs-lookup"><span data-stu-id="298ea-156">Description</span></span> |
|---------------------|--------------------------------------|
| <span data-ttu-id="298ea-157">string executionId</span><span class="sxs-lookup"><span data-stu-id="298ea-157">string executionId</span></span>          | <span data-ttu-id="298ea-158">インポート処理の実行ID。</span><span class="sxs-lookup"><span data-stu-id="298ea-158">Execution ID of import.</span></span> |
| <span data-ttu-id="298ea-159">string entityName</span><span class="sxs-lookup"><span data-stu-id="298ea-159">string entityName</span></span>        | <span data-ttu-id="298ea-160">エラー ファイルの取得対象となるエンティティの名前。</span><span class="sxs-lookup"><span data-stu-id="298ea-160">Name of the entity for which to get the error file.</span></span> |


<span data-ttu-id="298ea-161">**出力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="298ea-161">**Output parameters**</span></span>

| <span data-ttu-id="298ea-162">パラメーター</span><span class="sxs-lookup"><span data-stu-id="298ea-162">Parameter</span></span>         | <span data-ttu-id="298ea-163">説明</span><span class="sxs-lookup"><span data-stu-id="298ea-163">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="298ea-164">string errorkeysfileurl</span><span class="sxs-lookup"><span data-stu-id="298ea-164">string errorkeysfileurl</span></span> | <span data-ttu-id="298ea-165">エラーファイルのURL。</span><span class="sxs-lookup"><span data-stu-id="298ea-165">The URL of the error file.</span></span> <span data-ttu-id="298ea-166">エラーファイルが生成されなかった場合は、空の戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-166">The return value is empty if an error file was not generated.</span></span> |


### <a name="generateimporttargeterrorkeysfile"></a><span data-ttu-id="298ea-167">GenerateImportTargetErrorKeysFile</span><span class="sxs-lookup"><span data-stu-id="298ea-167">GenerateImportTargetErrorKeysFile</span></span>

<span data-ttu-id="298ea-168">GenerateImportTargetErrorKeysFile API は、エラーファイルを生成します。エラーファイルには単一のエンティティに対するインポートの過程で、ステージングからターゲットの段階で失敗したインポート レコードのキーが格納されています。</span><span class="sxs-lookup"><span data-stu-id="298ea-168">The GenerateImportTargetErrorKeysFile API is used to generate an error file containing the keys of the import records that failed at the staging to target step of import for a single entity.</span></span>  

<span data-ttu-id="298ea-169">このAPIがtrueを返す場合は、GetImportTargetErrorKeysFileUrl API を使用して、生成されたエラーキーファイルのURLを取得します。</span><span class="sxs-lookup"><span data-stu-id="298ea-169">If this API returns true, then use the GetImportTargetErrorKeysFileUrl API to get the URL of the generated error keys file.</span></span>


<span data-ttu-id="298ea-170">POST /Data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GenerateImportTargetErrorKeysFile</span><span class="sxs-lookup"><span data-stu-id="298ea-170">POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GenerateImportTargetErrorKeysFile</span></span>

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

<span data-ttu-id="298ea-171">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="298ea-171">**Input parameters**</span></span>

| <span data-ttu-id="298ea-172">パラメーター</span><span class="sxs-lookup"><span data-stu-id="298ea-172">Parameter</span></span>     | <span data-ttu-id="298ea-173">説明</span><span class="sxs-lookup"><span data-stu-id="298ea-173">Description</span></span> |
|---------------------|--------------------------------------|
| <span data-ttu-id="298ea-174">string executionId</span><span class="sxs-lookup"><span data-stu-id="298ea-174">string executionId</span></span>          | <span data-ttu-id="298ea-175">インポート処理の実行ID。</span><span class="sxs-lookup"><span data-stu-id="298ea-175">Execution ID of import</span></span> |
| <span data-ttu-id="298ea-176">string entityName</span><span class="sxs-lookup"><span data-stu-id="298ea-176">string entityName</span></span>        | <span data-ttu-id="298ea-177">エラー ファイルの取得対象となるエンティティの名前。</span><span class="sxs-lookup"><span data-stu-id="298ea-177">Name of the entity for which to get the error file</span></span> |

<span data-ttu-id="298ea-178">**出力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="298ea-178">**Output parameters**</span></span>

| <span data-ttu-id="298ea-179">パラメーター</span><span class="sxs-lookup"><span data-stu-id="298ea-179">Parameter</span></span>     | <span data-ttu-id="298ea-180">説明</span><span class="sxs-lookup"><span data-stu-id="298ea-180">Description</span></span> |
|---------------------|--------------------------------------|
| <span data-ttu-id="298ea-181">ブール値エラーが発生しています</span><span class="sxs-lookup"><span data-stu-id="298ea-181">Boolean errorsExist</span></span>     | <span data-ttu-id="298ea-182">インポートエラーが発生した場合はtrue、 インポートエラーが発生しなかった場合はfalseとします</span><span class="sxs-lookup"><span data-stu-id="298ea-182">true if there are import errors; false if there are no errors</span></span> |

### <a name="getimporttargeterrorkeysfileurl"></a><span data-ttu-id="298ea-183">GetImportTargetErrorKeysFileUrl</span><span class="sxs-lookup"><span data-stu-id="298ea-183">GetImportTargetErrorKeysFileUrl</span></span>

<span data-ttu-id="298ea-184">**GetImportTargetErrorKeysFileUrl** API を使用して、単一のエンティティに対するインポートのステージングからターゲットへのステップで失敗したインポート レコードのキーが格納されているエラー ファイルの URL を取得します。</span><span class="sxs-lookup"><span data-stu-id="298ea-184">The **GetImportTargetErrorKeysFileUrl** API is used to get the URL of the error file that contains the keys of the import records that failed at the staging-to-target step of import for a single entity.</span></span>

<span data-ttu-id="298ea-185">エラー ファイルが使用可能な場合、この API はその URL を返します。</span><span class="sxs-lookup"><span data-stu-id="298ea-185">If the error file is available, this API returns the URL.</span></span> <span data-ttu-id="298ea-186">エラー ファイルがまだ生成中の場合、またはエラー ファイルが存在しない場合は、API は空の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="298ea-186">If the error file is still being generated, or if there is no error file, the API returns an empty string.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="298ea-187">この API を呼び出す前に、**GenerateImportTargetErrorKeysFile** API を呼出して、エラー ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="298ea-187">Before you call this API, call the **GenerateImportTargetErrorKeysFile** API to generate the error file.</span></span> <span data-ttu-id="298ea-188">**GenerateImportTargetErrorKeysFile** API が **true** を返した場合、空でない文字列が返されるまで、ループでこの API を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="298ea-188">If the **GenerateImportTargetErrorKeysFile** API returns **true**, call this API in a loop until it returns a non-empty string.</span></span> <span data-ttu-id="298ea-189">**GenerateImportTargetErrorKeysFile** API が **false** を返した場合、エラーがないため、この API は空の文字列をかならず返します。</span><span class="sxs-lookup"><span data-stu-id="298ea-189">If the **GenerateImportTargetErrorKeysFile** API returns **false**, this API will always return an empty string, because there are no errors.</span></span>

<span data-ttu-id="298ea-190">**疑似コードの例**</span><span class="sxs-lookup"><span data-stu-id="298ea-190">**Pseudocode example**</span></span>

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

<span data-ttu-id="298ea-191">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="298ea-191">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":"<errorkeysfileurl>"
}
```

<span data-ttu-id="298ea-192">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="298ea-192">**Input parameters**</span></span>

| <span data-ttu-id="298ea-193">パラメーター</span><span class="sxs-lookup"><span data-stu-id="298ea-193">Parameter</span></span>         | <span data-ttu-id="298ea-194">説明</span><span class="sxs-lookup"><span data-stu-id="298ea-194">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="298ea-195">string executionId</span><span class="sxs-lookup"><span data-stu-id="298ea-195">string executionId</span></span> | <span data-ttu-id="298ea-196">インポートの実行 ID。</span><span class="sxs-lookup"><span data-stu-id="298ea-196">The execution ID of the import.</span></span> |
| <span data-ttu-id="298ea-197">string entityName</span><span class="sxs-lookup"><span data-stu-id="298ea-197">string entityName</span></span> | <span data-ttu-id="298ea-198">エラー ファイルを取得する対象のエンティティの名前。</span><span class="sxs-lookup"><span data-stu-id="298ea-198">The name of the entity to get the error file for.</span></span> |

<span data-ttu-id="298ea-199">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="298ea-199">**Output parameters**</span></span>

| <span data-ttu-id="298ea-200">パラメーター</span><span class="sxs-lookup"><span data-stu-id="298ea-200">Parameter</span></span>         | <span data-ttu-id="298ea-201">説明</span><span class="sxs-lookup"><span data-stu-id="298ea-201">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="298ea-202">string errorkeysfileurl</span><span class="sxs-lookup"><span data-stu-id="298ea-202">string errorkeysfileurl</span></span> | <span data-ttu-id="298ea-203">エラー キー ファイルが使用可能な場合、そのファイルの URL。</span><span class="sxs-lookup"><span data-stu-id="298ea-203">The URL of the error keys file, if the file is available.</span></span> <span data-ttu-id="298ea-204">エラー ファイルがまだ生成中の場合、またはエラー ファイルが存在しない場合は、このメソッドは空の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="298ea-204">If the error file is still being generated, or if no errors exist, the method returns an empty string.</span></span> |


### <a name="getazurewritableurl"></a><span data-ttu-id="298ea-205">GetAzureWritableUrl</span><span class="sxs-lookup"><span data-stu-id="298ea-205">GetAzureWritableUrl</span></span>

<span data-ttu-id="298ea-206">**GetAzureWritableUrl** API は、書き込み可能な Blob URL を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-206">The **GetAzureWritableUrl** API is used to get a writable blob URL.</span></span> <span data-ttu-id="298ea-207">このメソッドには、URL に埋め込まれた共有アクセス署名 (SAS) トークンが含まれています。</span><span class="sxs-lookup"><span data-stu-id="298ea-207">The method includes a shared access signature (SAS) token that is embedded in the URL.</span></span> <span data-ttu-id="298ea-208">この方法を使用すると、Finance and Operations の Azure Blob Storage コンテナーにデータ パッケージをアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="298ea-208">You can use this method to upload a data package to the Azure Blob storage container for Finance and Operations.</span></span> <span data-ttu-id="298ea-209">オンプレミス配置の場合、この API はローカル ストレージに取り込まれた URL を引き続き返します。</span><span class="sxs-lookup"><span data-stu-id="298ea-209">For on-premises deployments, this API will still return the URL that has been abstracted to local storage.</span></span>

> [!NOTE]
> <span data-ttu-id="298ea-210">SAS は有効期限の時間枠中にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="298ea-210">An SAS is valid only during an expiry time window.</span></span> <span data-ttu-id="298ea-211">ウィンドウが経過した後に発行されるすべての要求はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="298ea-211">Any request that is issued after the window has passed returns an error.</span></span> <span data-ttu-id="298ea-212">詳細については、[共有アクセス署名 (SA) の使用](/azure/storage/common/storage-dotnet-shared-access-signature-part-1) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="298ea-212">For more information, see [Using shared access signatures (SAS)](/azure/storage/common/storage-dotnet-shared-access-signature-part-1).</span></span>

```CSharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetAzureWriteUrl
BODY
{
    "uniqueFileName":"<string>"
}
```

<span data-ttu-id="298ea-213">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="298ea-213">Here is an example of a successful response.</span></span>

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

<span data-ttu-id="298ea-214">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="298ea-214">**Input parameters**</span></span>

| <span data-ttu-id="298ea-215">パラメーター</span><span class="sxs-lookup"><span data-stu-id="298ea-215">Parameter</span></span>         | <span data-ttu-id="298ea-216">説明</span><span class="sxs-lookup"><span data-stu-id="298ea-216">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="298ea-217">string packageUrl</span><span class="sxs-lookup"><span data-stu-id="298ea-217">string packageUrl</span></span> | <span data-ttu-id="298ea-218">BLOB ID を追跡するために使用される一意のファイル名。</span><span class="sxs-lookup"><span data-stu-id="298ea-218">A unique file name that is used to track blob IDs.</span></span> <span data-ttu-id="298ea-219">一意のファイル名であることを保証するため、グローバル一意識別子 (GUID) を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="298ea-219">You can include a globally unique identifier (GUID) to help guarantee a unique file name.</span></span> |

<span data-ttu-id="298ea-220">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="298ea-220">**Output parameters**</span></span>

| <span data-ttu-id="298ea-221">パラメーター</span><span class="sxs-lookup"><span data-stu-id="298ea-221">Parameter</span></span>      | <span data-ttu-id="298ea-222">説明</span><span class="sxs-lookup"><span data-stu-id="298ea-222">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="298ea-223">string BlobId</span><span class="sxs-lookup"><span data-stu-id="298ea-223">string BlobId</span></span>  | <span data-ttu-id="298ea-224">割り当てられた BLOB コンテナーの BLOB ID。</span><span class="sxs-lookup"><span data-stu-id="298ea-224">The blob ID of the allocated blob container.</span></span> |
| <span data-ttu-id="298ea-225">string BlobUrl</span><span class="sxs-lookup"><span data-stu-id="298ea-225">string BlobUrl</span></span> | <span data-ttu-id="298ea-226">埋め込みの SAS トークンを持つ URL。</span><span class="sxs-lookup"><span data-stu-id="298ea-226">A URL that has an embedded SAS token.</span></span> <span data-ttu-id="298ea-227">URL を使用 して Blob ストレージに書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="298ea-227">The URL can be used to write to Blob storage.</span></span> |

### <a name="importfrompackage"></a><span data-ttu-id="298ea-228">ImportFromPackage</span><span class="sxs-lookup"><span data-stu-id="298ea-228">ImportFromPackage</span></span>

<span data-ttu-id="298ea-229">**ImportFromPackage** API は、Finance and Operations の実装に関連付けられている Blob ストレージにアップロードされるデータ パッケージからインポートを開始するために使用します。</span><span class="sxs-lookup"><span data-stu-id="298ea-229">The **ImportFromPackage** API is used to initiate an import from the data package that is uploaded to the Blob storage that is associated with your implementation of Finance and Operations.</span></span> <span data-ttu-id="298ea-230">オンプレミス配置の場合、ファイルが以前アップロードされたローカル ストレージから、インポートが開始されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-230">For on-premises deployments, the import will be initiated from the local storage that the file was uploaded previously to.</span></span>

> [!NOTE]
> <span data-ttu-id="298ea-231">プラットフォーム更新プログラム 12 を起動すると、**ImportFromPackage** API は複合エンティティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="298ea-231">Starting in Platform update 12, the **ImportFromPackage** API supports composite entities.</span></span> <span data-ttu-id="298ea-232">ただし、1 つのパッケージで 1 つの複合エンティティのみという制限があります。</span><span class="sxs-lookup"><span data-stu-id="298ea-232">However, the limitation is that there can be only one composite entity in a package.</span></span>

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

<span data-ttu-id="298ea-233">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="298ea-233">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"<executionId>"
    }
}
```

<span data-ttu-id="298ea-234">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="298ea-234">**Input parameters**</span></span>

| <span data-ttu-id="298ea-235">パラメーター</span><span class="sxs-lookup"><span data-stu-id="298ea-235">Parameter</span></span>                | <span data-ttu-id="298ea-236">説明</span><span class="sxs-lookup"><span data-stu-id="298ea-236">Description</span></span> |
|--------------------------|-------------|
| <span data-ttu-id="298ea-237">string packageUrl</span><span class="sxs-lookup"><span data-stu-id="298ea-237">string packageUrl</span></span>        | <span data-ttu-id="298ea-238">Finance and Operations に関連付けられている Blob Storage 内のデータ パッケージの URL。</span><span class="sxs-lookup"><span data-stu-id="298ea-238">The URL of the data package in the Blob storage that is associated with Finance and Operations.</span></span> |
| <span data-ttu-id="298ea-239">string definitionGroupId</span><span class="sxs-lookup"><span data-stu-id="298ea-239">string definitionGroupId</span></span> | <span data-ttu-id="298ea-240">インポート用のデータ プロジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="298ea-240">The name of the data project for import.</span></span> |
| <span data-ttu-id="298ea-241">string executionId</span><span class="sxs-lookup"><span data-stu-id="298ea-241">string executionId</span></span>       | <span data-ttu-id="298ea-242">ジョブに使用する ID。</span><span class="sxs-lookup"><span data-stu-id="298ea-242">The ID to use for the job.</span></span> <span data-ttu-id="298ea-243">空の ID が割り当てられている場合は、新しい実行 ID が作成されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-243">If an empty ID is assigned, a new execution ID will be created.</span></span> |
| <span data-ttu-id="298ea-244">bool execute</span><span class="sxs-lookup"><span data-stu-id="298ea-244">bool execute</span></span>             | <span data-ttu-id="298ea-245">このパラメーターを **True** に設定して対象の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="298ea-245">Set this parameter to **True** to run the target step.</span></span> <span data-ttu-id="298ea-246">それ以外の場合、**False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="298ea-246">Otherwise, set it to **False**.</span></span> |
| <span data-ttu-id="298ea-247">bool overwrite</span><span class="sxs-lookup"><span data-stu-id="298ea-247">bool overwrite</span></span>           | <span data-ttu-id="298ea-248">パッケージ内で複合エンティティを使用する場合は、このパラメーターを常に **False** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="298ea-248">This parameter must always be set to **False** when a composite entity is used in a package.</span></span> <span data-ttu-id="298ea-249">それ以外の場合、**True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="298ea-249">Otherwise, set it to **True**.</span></span> |
| <span data-ttu-id="298ea-250">string legalEntityId</span><span class="sxs-lookup"><span data-stu-id="298ea-250">string legalEntityId</span></span>     | <span data-ttu-id="298ea-251">データ インポートの法人。</span><span class="sxs-lookup"><span data-stu-id="298ea-251">The legal entity for the data import.</span></span> |

<span data-ttu-id="298ea-252">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="298ea-252">**Output parameters**</span></span>

| <span data-ttu-id="298ea-253">パラメーター</span><span class="sxs-lookup"><span data-stu-id="298ea-253">Parameter</span></span>          | <span data-ttu-id="298ea-254">説明</span><span class="sxs-lookup"><span data-stu-id="298ea-254">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="298ea-255">string executionId</span><span class="sxs-lookup"><span data-stu-id="298ea-255">string executionId</span></span> | <span data-ttu-id="298ea-256">データ インポートの実行 ID。</span><span class="sxs-lookup"><span data-stu-id="298ea-256">The execution ID of the data import.</span></span> |

> [!NOTE]
> <span data-ttu-id="298ea-257">**ImportFromPackage()** はバッチを使用してインポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="298ea-257">**ImportFromPackage()** uses a batch to perform the import.</span></span> <span data-ttu-id="298ea-258">したがって、並行インポートを実行するために、データ管理で並列処理ルールを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="298ea-258">Therefore, parallel processing rules must be used in Data management to perform parallel imports.</span></span> <span data-ttu-id="298ea-259">**ImportFromPackage()** を並列スレッドで呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="298ea-259">**ImportFromPackage()** must not be called in parallel threads.</span></span> <span data-ttu-id="298ea-260">それ以外の場合、これは失敗します。</span><span class="sxs-lookup"><span data-stu-id="298ea-260">Otherwise, it will fail.</span></span>

## <a name="export-apis"></a><span data-ttu-id="298ea-261">API をエキスポート</span><span class="sxs-lookup"><span data-stu-id="298ea-261">Export APIs</span></span>

<span data-ttu-id="298ea-262">ファイル (データ パッケージ) のエクスポートには、次の API が使用されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-262">The following APIs are used to export files (data packages).</span></span>

### <a name="exporttopackage"></a><span data-ttu-id="298ea-263">ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="298ea-263">ExportToPackage</span></span>

<span data-ttu-id="298ea-264">**ExportToPackage** API は、データ パッケージのエクスポートを開始するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-264">The **ExportToPackage** API is used to initiate an export of a data package.</span></span> <span data-ttu-id="298ea-265">この API は、クラウド配置とオンプレミス配置の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-265">This API is applicable to both cloud deployments and on-premises deployments.</span></span>

- <span data-ttu-id="298ea-266">この API を呼び出す前に、エクスポート データ プロジェクトを Finance and Operations で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="298ea-266">The export data project must be created in Finance and Operations before you call this API.</span></span> <span data-ttu-id="298ea-267">プロジェクトが存在しない場合、API の呼び出しには、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-267">If the project doesn't exist, a call to the API returns an error.</span></span>
- <span data-ttu-id="298ea-268">変更履歴がオンの場合は、最後の実行後に更新または作成されたレコードのみがエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="298ea-268">If change tracking has been turned on, only records that have been created or updated since the last run are exported.</span></span> <span data-ttu-id="298ea-269">(つまり、デルタのみが返されます。)</span><span class="sxs-lookup"><span data-stu-id="298ea-269">(In other words, only the delta is returned.)</span></span>

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

<span data-ttu-id="298ea-270">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="298ea-270">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"<executionId>"
    }
}
```

<span data-ttu-id="298ea-271">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="298ea-271">**Input parameters**</span></span>

| <span data-ttu-id="298ea-272">パラメーター</span><span class="sxs-lookup"><span data-stu-id="298ea-272">Parameter</span></span>                | <span data-ttu-id="298ea-273">説明</span><span class="sxs-lookup"><span data-stu-id="298ea-273">Description</span></span> |
|--------------------------|-------------|
| <span data-ttu-id="298ea-274">string definitionGroupId</span><span class="sxs-lookup"><span data-stu-id="298ea-274">string definitionGroupId</span></span> | <span data-ttu-id="298ea-275">エクスポート用のデータ プロジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="298ea-275">The name of the data project for export.</span></span> |
| <span data-ttu-id="298ea-276">string packageName</span><span class="sxs-lookup"><span data-stu-id="298ea-276">string packageName</span></span>       | <span data-ttu-id="298ea-277">エクスポートされたデータ パッケージの名前。</span><span class="sxs-lookup"><span data-stu-id="298ea-277">The name of the exported data package.</span></span> |
| <span data-ttu-id="298ea-278">string executionId</span><span class="sxs-lookup"><span data-stu-id="298ea-278">string executionId</span></span>       | <span data-ttu-id="298ea-279">ジョブに使用する ID。</span><span class="sxs-lookup"><span data-stu-id="298ea-279">The ID to use for the job.</span></span> <span data-ttu-id="298ea-280">空の ID が割り当てられている場合は、新しい実行 ID が作成されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-280">If an empty ID is assigned, a new execution ID will be created.</span></span> |
| <span data-ttu-id="298ea-281">bool reExecute</span><span class="sxs-lookup"><span data-stu-id="298ea-281">bool reExecute</span></span>           | <span data-ttu-id="298ea-282">このパラメーターを **True** に設定して対象の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="298ea-282">Set this parameter to **True** to run the target step.</span></span> <span data-ttu-id="298ea-283">それ以外の場合、**False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="298ea-283">Otherwise, set it to **False**.</span></span> |
| <span data-ttu-id="298ea-284">string legalEntityId</span><span class="sxs-lookup"><span data-stu-id="298ea-284">string legalEntityId</span></span>     | <span data-ttu-id="298ea-285">データ インポートの法人。</span><span class="sxs-lookup"><span data-stu-id="298ea-285">The legal entity for the data import.</span></span> |
    
<span data-ttu-id="298ea-286">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="298ea-286">**Output parameters**</span></span>

| <span data-ttu-id="298ea-287">パラメーター</span><span class="sxs-lookup"><span data-stu-id="298ea-287">Parameter</span></span>          | <span data-ttu-id="298ea-288">説明</span><span class="sxs-lookup"><span data-stu-id="298ea-288">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="298ea-289">string executionId</span><span class="sxs-lookup"><span data-stu-id="298ea-289">string executionId</span></span> | <span data-ttu-id="298ea-290">データ エクスポートの実行 ID。</span><span class="sxs-lookup"><span data-stu-id="298ea-290">The execution ID of the data export.</span></span> |

### <a name="getexportedpackageurl"></a><span data-ttu-id="298ea-291">GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="298ea-291">GetExportedPackageUrl</span></span>

<span data-ttu-id="298ea-292">**GetExportedPackageUrl** API は、**ExportToPackage** を呼び出すことでエクスポートされたデータ パッケージの URL を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-292">The **GetExportedPackageUrl** API is used to get the URL of the data package that was exported by a call to **ExportToPackage**.</span></span> <span data-ttu-id="298ea-293">この API は、クラウド配置とオンプレミス配置の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-293">This API is applicable to both cloud deployments and on-premises deployments.</span></span>

```CSharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
BODY
{"executionId":"<Execution Id>"}
```

<span data-ttu-id="298ea-294">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="298ea-294">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"https://<baseurl_id>.blob.core.windows.net/dmf/<uniqueFileName>?<SAS Token>"
    }
}
```

<span data-ttu-id="298ea-295">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="298ea-295">**Input parameters**</span></span>

| <span data-ttu-id="298ea-296">パラメーター</span><span class="sxs-lookup"><span data-stu-id="298ea-296">Parameter</span></span>          | <span data-ttu-id="298ea-297">説明</span><span class="sxs-lookup"><span data-stu-id="298ea-297">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="298ea-298">string executionId</span><span class="sxs-lookup"><span data-stu-id="298ea-298">string executionId</span></span> | <span data-ttu-id="298ea-299">データ プロジェクト実行の実行 ID。</span><span class="sxs-lookup"><span data-stu-id="298ea-299">The execution ID of the data project run.</span></span> |

<span data-ttu-id="298ea-300">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="298ea-300">**Output parameters**</span></span>

| <span data-ttu-id="298ea-301">パラメーター</span><span class="sxs-lookup"><span data-stu-id="298ea-301">Parameter</span></span>      | <span data-ttu-id="298ea-302">説明</span><span class="sxs-lookup"><span data-stu-id="298ea-302">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="298ea-303">string BlobUrl</span><span class="sxs-lookup"><span data-stu-id="298ea-303">string BlobUrl</span></span> | <span data-ttu-id="298ea-304">埋め込みの SAS トークンを持つ blob URL。</span><span class="sxs-lookup"><span data-stu-id="298ea-304">A blob URL that has an embedded SAS token.</span></span> <span data-ttu-id="298ea-305">URL を使用して、エクスポートしたデータ パッケージをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="298ea-305">The URL can be used to download the exported data package.</span></span> |

## <a name="status-check-api"></a><span data-ttu-id="298ea-306">ステータス チェック API</span><span class="sxs-lookup"><span data-stu-id="298ea-306">Status check API</span></span> 

<span data-ttu-id="298ea-307">状態を確認するには、次の API を使用します。</span><span class="sxs-lookup"><span data-stu-id="298ea-307">The following APIs are used to check status.</span></span> <span data-ttu-id="298ea-308">これらは、インポート フローとエクスポート フローの両方で使用されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-308">They are used during both import flows and export flows.</span></span>

### <a name="getexecutionsummarystatus"></a><span data-ttu-id="298ea-309">GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="298ea-309">GetExecutionSummaryStatus</span></span>

<span data-ttu-id="298ea-310">**GetExecutionSummaryStatus** API は、インポート ジョブとエクスポート ジョブの両方に使用されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-310">The **GetExecutionSummaryStatus** API is used for both import jobs and export jobs.</span></span> <span data-ttu-id="298ea-311">これは、データ プロジェクト実行ジョブのステータスの確認に使用されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-311">It's used to check the status of a data project execution job.</span></span> <span data-ttu-id="298ea-312">この API は、クラウド配置とオンプレミス配置の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-312">This API is applicable to both cloud deployments and on-premises deployments.</span></span>

```CSharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
BODY
{"executionId":"<executionId>"}
```

<span data-ttu-id="298ea-313">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="298ea-313">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"<executionStatus>"
    }
}
```

<span data-ttu-id="298ea-314">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="298ea-314">**Input parameters**</span></span>

| <span data-ttu-id="298ea-315">パラメーター</span><span class="sxs-lookup"><span data-stu-id="298ea-315">Parameter</span></span>          | <span data-ttu-id="298ea-316">説明</span><span class="sxs-lookup"><span data-stu-id="298ea-316">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="298ea-317">string executionId</span><span class="sxs-lookup"><span data-stu-id="298ea-317">string executionId</span></span> | <span data-ttu-id="298ea-318">データ プロジェクト実行の実行 ID。</span><span class="sxs-lookup"><span data-stu-id="298ea-318">The execution ID of the data project run.</span></span> |

<span data-ttu-id="298ea-319">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="298ea-319">**Output parameters**</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="298ea-320">パラメーター</span><span class="sxs-lookup"><span data-stu-id="298ea-320">Parameter</span></span></th>
<th><span data-ttu-id="298ea-321">説明</span><span class="sxs-lookup"><span data-stu-id="298ea-321">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="298ea-322">DMFExecutionSummaryStatus executionStatus</span><span class="sxs-lookup"><span data-stu-id="298ea-322">DMFExecutionSummaryStatus executionStatus</span></span></td>
<td><span data-ttu-id="298ea-323">実行のステータス。</span><span class="sxs-lookup"><span data-stu-id="298ea-323">The execution status.</span></span> <span data-ttu-id="298ea-324">以下に使用可能な値を示します。</span><span class="sxs-lookup"><span data-stu-id="298ea-324">Here are the possible values:</span></span>
<ul>
<li><span data-ttu-id="298ea-325">不明</span><span class="sxs-lookup"><span data-stu-id="298ea-325">Unknown</span></span></li>
<li><span data-ttu-id="298ea-326">NotRun</span><span class="sxs-lookup"><span data-stu-id="298ea-326">NotRun</span></span></li>
<li><span data-ttu-id="298ea-327">実行中</span><span class="sxs-lookup"><span data-stu-id="298ea-327">Executing</span></span></li>
<li><span data-ttu-id="298ea-328">成功</span><span class="sxs-lookup"><span data-stu-id="298ea-328">Succeeded</span></span></li>
<li><span data-ttu-id="298ea-329">PartiallySucceeded</span><span class="sxs-lookup"><span data-stu-id="298ea-329">PartiallySucceeded</span></span></li>
<li><span data-ttu-id="298ea-330">失敗</span><span class="sxs-lookup"><span data-stu-id="298ea-330">Failed</span></span></li>
<li><span data-ttu-id="298ea-331">取消済</span><span class="sxs-lookup"><span data-stu-id="298ea-331">Canceled</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="298ea-332">Blob ストレージ内のファイルはストレージに 7 日間残ります。</span><span class="sxs-lookup"><span data-stu-id="298ea-332">The file in Blob storage will remain there for seven days.</span></span> <span data-ttu-id="298ea-333">次に、そのファイルは自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="298ea-333">It will then be automatically deleted.</span></span>

## <a name="import-and-export-processes"></a><span data-ttu-id="298ea-334">プロセスのインポートとエクスポート</span><span class="sxs-lookup"><span data-stu-id="298ea-334">Import and export processes</span></span>

<span data-ttu-id="298ea-335">次の図は、データ管理パッケージ メソッドを使用してデータ パッケージをインポートする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="298ea-335">The following illustration shows how the Data management package methods can be used to import data packages.</span></span>

![データ管理パッケージ メソッドを使用するデータ パッケージ ファイルのインポート](./media/data-package-import.png)

<span data-ttu-id="298ea-337">次の図は、データ管理パッケージ メソッドを使用してデータ パッケージをエクスポートする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="298ea-337">The following illustration shows how the Data management package methods can be used to export data packages.</span></span>

![データ管理パッケージ メソッドを使用するデータ パッケージ ファイルのエクスポート](./media/data-package-export.png)

<span data-ttu-id="298ea-339">データのインポートとデータのエクスポートのメソッドを紹介するサンプルのコンソール アプリケーションは、 GitHub から入手できます。</span><span class="sxs-lookup"><span data-stu-id="298ea-339">A sample console application that showcases the data import and data export methods is available on GitHub.</span></span> <span data-ttu-id="298ea-340">詳細については、「<https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/FileBasedIntegrationSamples/ConsoleAppSamples>」に移動してください。</span><span class="sxs-lookup"><span data-stu-id="298ea-340">For more information, go to <https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/FileBasedIntegrationSamples/ConsoleAppSamples>.</span></span>
