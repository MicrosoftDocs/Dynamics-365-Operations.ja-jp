---
title: データ管理パッケージ REST API
description: このトピックでは、データ管理フレームワークのパッケージ REST API について説明します。
author: Sunil-Garg
ms.date: 06/18/2020
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
ms.openlocfilehash: 86b8ceb54de24db64d01b3280706169685e656b8
ms.sourcegitcommit: 6f0560632092449ca5fc5a36513c68b8e7791528
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/18/2020
ms.locfileid: "3465266"
---
# <a name="data-management-package-rest-api"></a><span data-ttu-id="0601c-103">データ管理パッケージ REST API</span><span class="sxs-lookup"><span data-stu-id="0601c-103">Data management package REST API</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0601c-104">このトピックでは、データ管理フレームワークのパッケージの Representational State Transfer (REST) のアプリケーション プログラミング インターフェイス (API) について説明します。</span><span class="sxs-lookup"><span data-stu-id="0601c-104">This topic describes the Data management framework's package representational state transfer (REST) application programming interface (API).</span></span> <span data-ttu-id="0601c-105">パッケージ API により、データ パッケージを使用して統合できます。</span><span class="sxs-lookup"><span data-stu-id="0601c-105">The package API lets you integrate by using data packages.</span></span> <span data-ttu-id="0601c-106">REST API はクラウド展開とオンプレミスの展開で使用できます。</span><span class="sxs-lookup"><span data-stu-id="0601c-106">The REST API can be used with both cloud deployments and on-premises deployments.</span></span> <span data-ttu-id="0601c-107">オンプレミス配置では、現在この機能は、Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition プラットフォーム更新プログラム 12 (2017 年 11 月) (バージョン 7.2)、ビルド 7.0.4709.41184 以降で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="0601c-107">For on-premises deployments, this functionality is currently available for Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with platform update 12 (November 2017) (version 7.2), build 7.0.4709.41184, and later.</span></span>

<span data-ttu-id="0601c-108">オンプレミス サポートが追加されましたが、API 名は変更されていません。</span><span class="sxs-lookup"><span data-stu-id="0601c-108">Although on-premises support has been added, API names haven't been changed.</span></span> <span data-ttu-id="0601c-109">したがって、Microsoft は、クラウド配置とオンプレミス配置の両方に対して単一の API セットを維持することができます。</span><span class="sxs-lookup"><span data-stu-id="0601c-109">Therefore, Microsoft can keep a single API set for both cloud deployments and on-premises deployments.</span></span>

## <a name="choosing-an-integration-api"></a><span data-ttu-id="0601c-110">統合 API の選択</span><span class="sxs-lookup"><span data-stu-id="0601c-110">Choosing an integration API</span></span>

<span data-ttu-id="0601c-111">ファイル ベースの統合シナリオは、データ管理フレームワークのパッケージ API と定期的な統合 API の 2 つの API によりサポートされます。</span><span class="sxs-lookup"><span data-stu-id="0601c-111">Two APIs support file-based integration scenarios: the Data management framework's package API and the recurring integrations API.</span></span> <span data-ttu-id="0601c-112">どちらの API もデータ インポート シナリオとデータ エクスポート シナリオの両方をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="0601c-112">Both APIs support both data import scenarios and data export scenarios.</span></span> <span data-ttu-id="0601c-113">次のテーブルでは、使用する API を決定する際に考慮する必要がある主な決定事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="0601c-113">The following table describes the main decision points that you should consider when you're trying to decide which API to use.</span></span>

| <span data-ttu-id="0601c-114">決定ポイント</span><span class="sxs-lookup"><span data-stu-id="0601c-114">Decision point</span></span>      | <span data-ttu-id="0601c-115">定期統合 API</span><span class="sxs-lookup"><span data-stu-id="0601c-115">Recurring integrations API</span></span> | <span data-ttu-id="0601c-116">データ管理フレームワークのパッケージ API</span><span class="sxs-lookup"><span data-stu-id="0601c-116">Data management framework's package API</span></span> |
|---------------------|--------------------------------------|-----------------------------|
| <span data-ttu-id="0601c-117">スケジューリング</span><span class="sxs-lookup"><span data-stu-id="0601c-117">Scheduling</span></span>          | <span data-ttu-id="0601c-118">Finance and Operations アプリのスケジューリング</span><span class="sxs-lookup"><span data-stu-id="0601c-118">Scheduling in Finance and Operations apps</span></span> | <span data-ttu-id="0601c-119">Finance and Operations アプリ以外のスケジューリング</span><span class="sxs-lookup"><span data-stu-id="0601c-119">Scheduling outside Finance and Operations apps</span></span> |
| <span data-ttu-id="0601c-120">Format</span><span class="sxs-lookup"><span data-stu-id="0601c-120">Format</span></span>              | <span data-ttu-id="0601c-121">ファイルおよびデータ パッケージ</span><span class="sxs-lookup"><span data-stu-id="0601c-121">Files and data packages</span></span> | <span data-ttu-id="0601c-122">データ パッケージのみ</span><span class="sxs-lookup"><span data-stu-id="0601c-122">Only data packages</span></span> |
| <span data-ttu-id="0601c-123">変換</span><span class="sxs-lookup"><span data-stu-id="0601c-123">Transformation</span></span>      | <span data-ttu-id="0601c-124">データ ファイルが XML 形式の場合の Extensible Stylesheet Language Transformations (XSLT) のサポート</span><span class="sxs-lookup"><span data-stu-id="0601c-124">Support for Extensible Stylesheet Language Transformations (XSLT) if the data file is in XML format</span></span> | <span data-ttu-id="0601c-125">システム外部での変換</span><span class="sxs-lookup"><span data-stu-id="0601c-125">Transformations that are external to the system</span></span> |
| <span data-ttu-id="0601c-126">サポートされているプロトコル</span><span class="sxs-lookup"><span data-stu-id="0601c-126">Supported protocols</span></span> | <span data-ttu-id="0601c-127">SOAP および REST</span><span class="sxs-lookup"><span data-stu-id="0601c-127">SOAP and REST</span></span> | <span data-ttu-id="0601c-128">REST</span><span class="sxs-lookup"><span data-stu-id="0601c-128">REST</span></span> |
| <span data-ttu-id="0601c-129">サービス タイプ</span><span class="sxs-lookup"><span data-stu-id="0601c-129">Service type</span></span>        | <span data-ttu-id="0601c-130">カスタム サービス</span><span class="sxs-lookup"><span data-stu-id="0601c-130">Custom service</span></span> | <span data-ttu-id="0601c-131">データ プロトコル (OData) アクションを開きます</span><span class="sxs-lookup"><span data-stu-id="0601c-131">Open Data Protocol (OData) action</span></span> |
| <span data-ttu-id="0601c-132">在庫状態</span><span class="sxs-lookup"><span data-stu-id="0601c-132">Availability</span></span>        | <span data-ttu-id="0601c-133">Microsoft Dynamics Finance and Operations (2016 年 2 月) およびそれ以降。</span><span class="sxs-lookup"><span data-stu-id="0601c-133">Microsoft Dynamics Finance and Operations (February 2016) and later.</span></span> <span data-ttu-id="0601c-134">注意: この機能は、オンプレミス バージョンの Dynamics 365 Finance and Operations には対応していません。</span><span class="sxs-lookup"><span data-stu-id="0601c-134">Note: This is not supported with the on-premises version of Dynamics 365 Finance and Operations.</span></span> | <span data-ttu-id="0601c-135">Microsoft Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 5 (2017 年 3 月) およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0601c-135">Microsoft Dynamics 365 for Finance and Operations with platform update 5 (March 2017) and later</span></span> |

<span data-ttu-id="0601c-136">定期的な統合 API がデータ管理フレームワークのパッケージ API よりも要件を満たしていることを決定した場合、[定期統合](recurring-integrations.md) を参照します。</span><span class="sxs-lookup"><span data-stu-id="0601c-136">If you decide that the recurring integrations API meets your requirement better than the Data management framework's package API, see [Recurring integrations](recurring-integrations.md).</span></span> <span data-ttu-id="0601c-137">このトピックの残りの部分では、データ管理フレームワークのパッケージ API について説明します。</span><span class="sxs-lookup"><span data-stu-id="0601c-137">The rest of this topic discusses the Data management framework's package API.</span></span>

## <a name="authorization"></a><span data-ttu-id="0601c-138">承認</span><span class="sxs-lookup"><span data-stu-id="0601c-138">Authorization</span></span>

<span data-ttu-id="0601c-139">データ管理フレームワークのパッケージ API は、アクセスを認可するために OAuth 2.0 を使用します。</span><span class="sxs-lookup"><span data-stu-id="0601c-139">The Data management framework's package API uses OAuth 2.0 to authorize access.</span></span> <span data-ttu-id="0601c-140">API は、有効な OAuth アクセス トークンを使用して呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0601c-140">The API must be called by using a valid OAuth access token.</span></span> <span data-ttu-id="0601c-141">OAuth 2.0 および Microsoft Azure Active Directory(Azure AD) の詳細については、[OAuth 2.0 と Azure Active Directory を使用して Web アプリケーションへのアクセスを承認](/azure/active-directory/develop/active-directory-protocols-oauth-code) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0601c-141">For more information about OAuth 2.0 and Microsoft Azure Active Directory (Azure AD), see [Authorize access to web applications using OAuth 2.0 and Azure Active Directory](/azure/active-directory/develop/active-directory-protocols-oauth-code).</span></span> <span data-ttu-id="0601c-142">オンプレミス配置では、Active Directory フェデレーション サービス (AD FS) が承認に使用されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-142">For on-premises deployments, Active Directory Federation Services (AD FS) is used for authorization.</span></span>

> [!NOTE]
> <span data-ttu-id="0601c-143">クライアント資格情報の付与フローを使用すると、アプリケーションはアクセス制御リストを保持します。</span><span class="sxs-lookup"><span data-stu-id="0601c-143">When you use the Client Credentials Grant flow, the application maintains an access control list.</span></span> <span data-ttu-id="0601c-144">アクセス制御リストは、**システム管理** \> **設定** \> **Azure Active Directory アプリケーション** を順にクリックして見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="0601c-144">You can find the access control list at **System administration** \> **Setup** \> **Azure Active Directory applications**.</span></span> <span data-ttu-id="0601c-145">**Azure Active Directory アプリケーション** ページには、承認済クライアント ID と、クライアント資格情報付与フローを使用して API が呼び出されたときに適用する必要があるユーザー セキュリティ マッピングが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-145">The **Azure Active Directory applications** page shows the approved client IDs and the user security mapping that should be enforced when the API is called by using the Client Credentials Grant flow.</span></span>
>
> <span data-ttu-id="0601c-146">オンプレミス配置については、このリストには AD FS からの有効なクライアント ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="0601c-146">For on-premises deployments, this list must have a valid client ID from AD FS.</span></span> <span data-ttu-id="0601c-147">また、オンプレミスで使用する場合は、接続の確立時に、次の例にて示されている **\<baseurl\>** に **/namespaces/AXSF** を付加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0601c-147">Additionally, for on-premises use, **\<baseurl\>** in the following examples must append **/namespaces/AXSF** when a connection is made.</span></span>

## <a name="import-apis"></a><span data-ttu-id="0601c-148">API のインポート</span><span class="sxs-lookup"><span data-stu-id="0601c-148">Import APIs</span></span>

<span data-ttu-id="0601c-149">ファイル (データ パッケージ) のインポートには、次の API が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-149">The following APIs are used to import files (data packages).</span></span>

### <a name="getimportstagingerrorfileurl"></a><span data-ttu-id="0601c-150">GetImportStagingErrorFileUrl</span><span class="sxs-lookup"><span data-stu-id="0601c-150">GetImportStagingErrorFileUrl</span></span>

<span data-ttu-id="0601c-151">GetImportStagingErrorFileUrl API は、エラーファイルのURLを取得します。エラーファイルには単一のエンティティに対するインポートの過程で、ステージング段階で失敗したデータが格納されています。</span><span class="sxs-lookup"><span data-stu-id="0601c-151">The GetImportStagingErrorFileUrl API is used to get the URL of the error file containing the input records that failed at the source to the staging step of import for a single entity.</span></span> <span data-ttu-id="0601c-152">エラーファイルが生成されなかった場合は、空の文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-152">An empty string is returned if no error file is generated.</span></span>

<span data-ttu-id="0601c-153">POST /Data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetImportStagingErrorFileUrl</span><span class="sxs-lookup"><span data-stu-id="0601c-153">POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetImportStagingErrorFileUrl</span></span>

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

<span data-ttu-id="0601c-154">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="0601c-154">**Input parameters**</span></span>

| <span data-ttu-id="0601c-155">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0601c-155">Parameter</span></span>     | <span data-ttu-id="0601c-156">説明</span><span class="sxs-lookup"><span data-stu-id="0601c-156">Description</span></span> |
|---------------------|--------------------------------------|
| <span data-ttu-id="0601c-157">string executionId</span><span class="sxs-lookup"><span data-stu-id="0601c-157">string executionId</span></span>          | <span data-ttu-id="0601c-158">インポート処理の実行ID。</span><span class="sxs-lookup"><span data-stu-id="0601c-158">Execution ID of import.</span></span> <span data-ttu-id="0601c-159">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0601c-159">This is called as Job ID in the UI.</span></span> |
| <span data-ttu-id="0601c-160">string entityName</span><span class="sxs-lookup"><span data-stu-id="0601c-160">string entityName</span></span>        | <span data-ttu-id="0601c-161">エラー ファイルの取得対象となるエンティティの名前。</span><span class="sxs-lookup"><span data-stu-id="0601c-161">Name of the entity for which to get the error file.</span></span> |


<span data-ttu-id="0601c-162">**出力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="0601c-162">**Output parameters**</span></span>

| <span data-ttu-id="0601c-163">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0601c-163">Parameter</span></span>         | <span data-ttu-id="0601c-164">説明</span><span class="sxs-lookup"><span data-stu-id="0601c-164">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="0601c-165">string errorkeysfileurl</span><span class="sxs-lookup"><span data-stu-id="0601c-165">string errorkeysfileurl</span></span> | <span data-ttu-id="0601c-166">エラーファイルのURL。</span><span class="sxs-lookup"><span data-stu-id="0601c-166">The URL of the error file.</span></span> <span data-ttu-id="0601c-167">エラーファイルが生成されなかった場合は、空の戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-167">The return value is empty if an error file was not generated.</span></span> |


### <a name="generateimporttargeterrorkeysfile"></a><span data-ttu-id="0601c-168">GenerateImportTargetErrorKeysFile</span><span class="sxs-lookup"><span data-stu-id="0601c-168">GenerateImportTargetErrorKeysFile</span></span>

<span data-ttu-id="0601c-169">GenerateImportTargetErrorKeysFile API は、エラーファイルを生成します。エラーファイルには単一のエンティティに対するインポートの過程で、ステージングからターゲットの段階で失敗したインポート レコードのキーが格納されています。</span><span class="sxs-lookup"><span data-stu-id="0601c-169">The GenerateImportTargetErrorKeysFile API is used to generate an error file containing the keys of the import records that failed at the staging to target step of import for a single entity.</span></span>  

<span data-ttu-id="0601c-170">このAPIがtrueを返す場合は、GetImportTargetErrorKeysFileUrl API を使用して、生成されたエラーキーファイルのURLを取得します。</span><span class="sxs-lookup"><span data-stu-id="0601c-170">If this API returns true, then use the GetImportTargetErrorKeysFileUrl API to get the URL of the generated error keys file.</span></span>


<span data-ttu-id="0601c-171">POST /Data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GenerateImportTargetErrorKeysFile</span><span class="sxs-lookup"><span data-stu-id="0601c-171">POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GenerateImportTargetErrorKeysFile</span></span>

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

<span data-ttu-id="0601c-172">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="0601c-172">**Input parameters**</span></span>

| <span data-ttu-id="0601c-173">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0601c-173">Parameter</span></span>     | <span data-ttu-id="0601c-174">説明</span><span class="sxs-lookup"><span data-stu-id="0601c-174">Description</span></span> |
|---------------------|--------------------------------------|
| <span data-ttu-id="0601c-175">string executionId</span><span class="sxs-lookup"><span data-stu-id="0601c-175">string executionId</span></span>          | <span data-ttu-id="0601c-176">インポート処理の実行ID。</span><span class="sxs-lookup"><span data-stu-id="0601c-176">Execution ID of import</span></span> |
| <span data-ttu-id="0601c-177">string entityName</span><span class="sxs-lookup"><span data-stu-id="0601c-177">string entityName</span></span>        | <span data-ttu-id="0601c-178">エラー ファイルの取得対象となるエンティティの名前。</span><span class="sxs-lookup"><span data-stu-id="0601c-178">Name of the entity for which to get the error file</span></span> |

<span data-ttu-id="0601c-179">**出力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="0601c-179">**Output parameters**</span></span>

| <span data-ttu-id="0601c-180">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0601c-180">Parameter</span></span>     | <span data-ttu-id="0601c-181">説明</span><span class="sxs-lookup"><span data-stu-id="0601c-181">Description</span></span> |
|---------------------|--------------------------------------|
| <span data-ttu-id="0601c-182">ブール値エラーが発生しています</span><span class="sxs-lookup"><span data-stu-id="0601c-182">Boolean errorsExist</span></span>     | <span data-ttu-id="0601c-183">インポートエラーが発生した場合はtrue、 インポートエラーが発生しなかった場合はfalseとします</span><span class="sxs-lookup"><span data-stu-id="0601c-183">true if there are import errors; false if there are no errors</span></span> |

### <a name="getimporttargeterrorkeysfileurl"></a><span data-ttu-id="0601c-184">GetImportTargetErrorKeysFileUrl</span><span class="sxs-lookup"><span data-stu-id="0601c-184">GetImportTargetErrorKeysFileUrl</span></span>

<span data-ttu-id="0601c-185">**GetImportTargetErrorKeysFileUrl** API を使用して、単一のエンティティに対するインポートのステージングからターゲットへのステップで失敗したインポート レコードのキーが格納されているエラー ファイルの URL を取得します。</span><span class="sxs-lookup"><span data-stu-id="0601c-185">The **GetImportTargetErrorKeysFileUrl** API is used to get the URL of the error file that contains the keys of the import records that failed at the staging-to-target step of import for a single entity.</span></span>

<span data-ttu-id="0601c-186">エラー ファイルが使用可能な場合、この API はその URL を返します。</span><span class="sxs-lookup"><span data-stu-id="0601c-186">If the error file is available, this API returns the URL.</span></span> <span data-ttu-id="0601c-187">エラー ファイルがまだ生成中の場合、またはエラー ファイルが存在しない場合は、API は空の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="0601c-187">If the error file is still being generated, or if there is no error file, the API returns an empty string.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="0601c-188">この API を呼び出す前に、**GenerateImportTargetErrorKeysFile** API を呼出して、エラー ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="0601c-188">Before you call this API, call the **GenerateImportTargetErrorKeysFile** API to generate the error file.</span></span> <span data-ttu-id="0601c-189">**GenerateImportTargetErrorKeysFile** API が **true** を返した場合、空でない文字列が返されるまで、ループでこの API を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0601c-189">If the **GenerateImportTargetErrorKeysFile** API returns **true**, call this API in a loop until it returns a non-empty string.</span></span> <span data-ttu-id="0601c-190">**GenerateImportTargetErrorKeysFile** API が **false** を返した場合、エラーがないため、この API は空の文字列をかならず返します。</span><span class="sxs-lookup"><span data-stu-id="0601c-190">If the **GenerateImportTargetErrorKeysFile** API returns **false**, this API will always return an empty string, because there are no errors.</span></span>

<span data-ttu-id="0601c-191">**疑似コードの例**</span><span class="sxs-lookup"><span data-stu-id="0601c-191">**Pseudocode example**</span></span>

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

<span data-ttu-id="0601c-192">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0601c-192">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":"<errorkeysfileurl>"
}
```

<span data-ttu-id="0601c-193">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="0601c-193">**Input parameters**</span></span>

| <span data-ttu-id="0601c-194">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0601c-194">Parameter</span></span>         | <span data-ttu-id="0601c-195">説明</span><span class="sxs-lookup"><span data-stu-id="0601c-195">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="0601c-196">string executionId</span><span class="sxs-lookup"><span data-stu-id="0601c-196">string executionId</span></span> | <span data-ttu-id="0601c-197">インポートの実行 ID。</span><span class="sxs-lookup"><span data-stu-id="0601c-197">The execution ID of the import.</span></span> <span data-ttu-id="0601c-198">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0601c-198">This is called as Job ID in the UI.</span></span>|
| <span data-ttu-id="0601c-199">string entityName</span><span class="sxs-lookup"><span data-stu-id="0601c-199">string entityName</span></span> | <span data-ttu-id="0601c-200">エラー ファイルを取得する対象のエンティティの名前。</span><span class="sxs-lookup"><span data-stu-id="0601c-200">The name of the entity to get the error file for.</span></span> |

<span data-ttu-id="0601c-201">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="0601c-201">**Output parameters**</span></span>

| <span data-ttu-id="0601c-202">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0601c-202">Parameter</span></span>         | <span data-ttu-id="0601c-203">説明</span><span class="sxs-lookup"><span data-stu-id="0601c-203">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="0601c-204">string errorkeysfileurl</span><span class="sxs-lookup"><span data-stu-id="0601c-204">string errorkeysfileurl</span></span> | <span data-ttu-id="0601c-205">エラー キー ファイルが使用可能な場合、そのファイルの URL。</span><span class="sxs-lookup"><span data-stu-id="0601c-205">The URL of the error keys file, if the file is available.</span></span> <span data-ttu-id="0601c-206">エラー ファイルがまだ生成中の場合、またはエラー ファイルが存在しない場合は、このメソッドは空の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="0601c-206">If the error file is still being generated, or if no errors exist, the method returns an empty string.</span></span> |


### <a name="getazurewritableurl"></a><span data-ttu-id="0601c-207">GetAzureWritableUrl</span><span class="sxs-lookup"><span data-stu-id="0601c-207">GetAzureWritableUrl</span></span>

<span data-ttu-id="0601c-208">**GetAzureWritableUrl** API は、書き込み可能な Blob URL を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-208">The **GetAzureWritableUrl** API is used to get a writable blob URL.</span></span> <span data-ttu-id="0601c-209">このメソッドには、URL に埋め込まれた共有アクセス署名 (SAS) トークンが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0601c-209">The method includes a shared access signature (SAS) token that is embedded in the URL.</span></span> <span data-ttu-id="0601c-210">この方法を使用すると、Azure Blob Storage コンテナーにデータ パッケージをアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="0601c-210">You can use this method to upload a data package to the Azure Blob storage container.</span></span> <span data-ttu-id="0601c-211">オンプレミス配置の場合、この API はローカル ストレージに取り込まれた URL を引き続き返します。</span><span class="sxs-lookup"><span data-stu-id="0601c-211">For on-premises deployments, this API will still return the URL that has been abstracted to local storage.</span></span>

> [!NOTE]
> <span data-ttu-id="0601c-212">SAS は有効期限の時間枠中にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="0601c-212">An SAS is valid only during an expiry time window.</span></span> <span data-ttu-id="0601c-213">ウィンドウが経過した後に発行されるすべての要求はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="0601c-213">Any request that is issued after the window has passed returns an error.</span></span> <span data-ttu-id="0601c-214">詳細については、[共有アクセス署名 (SA) の使用](/azure/storage/common/storage-dotnet-shared-access-signature-part-1) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0601c-214">For more information, see [Using shared access signatures (SAS)](/azure/storage/common/storage-dotnet-shared-access-signature-part-1).</span></span>

```csharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetAzureWriteUrl
BODY
{
    "uniqueFileName":"<string>"
}
```

<span data-ttu-id="0601c-215">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0601c-215">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value": "{\"BlobId\":\"{<GUID>}\",\"BlobUrl\":\"https://<baseurl_id>.blob.core.windows.net/dmf/<uniqueFileName>?<SAS Token>\"}"
    }
}
```

<span data-ttu-id="0601c-216">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="0601c-216">**Input parameters**</span></span>

| <span data-ttu-id="0601c-217">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0601c-217">Parameter</span></span>         | <span data-ttu-id="0601c-218">説明</span><span class="sxs-lookup"><span data-stu-id="0601c-218">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="0601c-219">文字列 uniqueFileName</span><span class="sxs-lookup"><span data-stu-id="0601c-219">string uniqueFileName</span></span> | <span data-ttu-id="0601c-220">BLOB ID を追跡するために使用される一意のファイル名。</span><span class="sxs-lookup"><span data-stu-id="0601c-220">A unique file name that is used to track blob IDs.</span></span> <span data-ttu-id="0601c-221">一意のファイル名であることを保証するため、グローバル一意識別子 (GUID) を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="0601c-221">You can include a globally unique identifier (GUID) to help guarantee a unique file name.</span></span> |

<span data-ttu-id="0601c-222">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="0601c-222">**Output parameters**</span></span>

| <span data-ttu-id="0601c-223">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0601c-223">Parameter</span></span>      | <span data-ttu-id="0601c-224">説明</span><span class="sxs-lookup"><span data-stu-id="0601c-224">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="0601c-225">string BlobId</span><span class="sxs-lookup"><span data-stu-id="0601c-225">string BlobId</span></span>  | <span data-ttu-id="0601c-226">割り当てられた BLOB コンテナーの BLOB ID。</span><span class="sxs-lookup"><span data-stu-id="0601c-226">The blob ID of the allocated blob container.</span></span> |
| <span data-ttu-id="0601c-227">string BlobUrl</span><span class="sxs-lookup"><span data-stu-id="0601c-227">string BlobUrl</span></span> | <span data-ttu-id="0601c-228">埋め込みの SAS トークンを持つ URL。</span><span class="sxs-lookup"><span data-stu-id="0601c-228">A URL that has an embedded SAS token.</span></span> <span data-ttu-id="0601c-229">URL を使用 して Blob ストレージに書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="0601c-229">The URL can be used to write to Blob storage.</span></span> |

### <a name="importfrompackage"></a><span data-ttu-id="0601c-230">ImportFromPackage</span><span class="sxs-lookup"><span data-stu-id="0601c-230">ImportFromPackage</span></span>

<span data-ttu-id="0601c-231">**ImportFromPackage** API は、実装に関連付けられている Blob ストレージにアップロードされるデータ パッケージからインポートを開始するために使用します。</span><span class="sxs-lookup"><span data-stu-id="0601c-231">The **ImportFromPackage** API is used to initiate an import from the data package that is uploaded to the Blob storage that is associated with your implementation.</span></span> <span data-ttu-id="0601c-232">オンプレミス配置の場合、ファイルが以前アップロードされたローカル ストレージから、インポートが開始されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-232">For on-premises deployments, the import will be initiated from the local storage that the file was uploaded previously to.</span></span>

> [!NOTE]
> <span data-ttu-id="0601c-233">プラットフォーム更新プログラム 12 を起動すると、**ImportFromPackage** API は複合エンティティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="0601c-233">Starting in Platform update 12, the **ImportFromPackage** API supports composite entities.</span></span> <span data-ttu-id="0601c-234">ただし、1 つのパッケージで 1 つの複合エンティティのみという制限があります。</span><span class="sxs-lookup"><span data-stu-id="0601c-234">However, the limitation is that there can be only one composite entity in a package.</span></span>

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

<span data-ttu-id="0601c-235">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0601c-235">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":"<executionId>"
}
```

<span data-ttu-id="0601c-236">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="0601c-236">**Input parameters**</span></span>

| <span data-ttu-id="0601c-237">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0601c-237">Parameter</span></span>                | <span data-ttu-id="0601c-238">説明</span><span class="sxs-lookup"><span data-stu-id="0601c-238">Description</span></span> |
|--------------------------|-------------|
| <span data-ttu-id="0601c-239">string packageUrl</span><span class="sxs-lookup"><span data-stu-id="0601c-239">string packageUrl</span></span>        | <span data-ttu-id="0601c-240">Finance and Operations アプリに関連付けられている Blob Storage 内のデータ パッケージの URL。</span><span class="sxs-lookup"><span data-stu-id="0601c-240">The URL of the data package in the Blob storage that is associated with a Finance and Operations app.</span></span> |
| <span data-ttu-id="0601c-241">string definitionGroupId</span><span class="sxs-lookup"><span data-stu-id="0601c-241">string definitionGroupId</span></span> | <span data-ttu-id="0601c-242">インポート用のデータ プロジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="0601c-242">The name of the data project for import.</span></span> |
| <span data-ttu-id="0601c-243">string executionId</span><span class="sxs-lookup"><span data-stu-id="0601c-243">string executionId</span></span>       | <span data-ttu-id="0601c-244">ジョブに使用する ID。</span><span class="sxs-lookup"><span data-stu-id="0601c-244">The ID to use for the job.</span></span> <span data-ttu-id="0601c-245">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0601c-245">This is called as Job ID in the UI.</span></span> <span data-ttu-id="0601c-246">空の ID が割り当てられている場合は、新しい実行 ID が作成されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-246">If an empty ID is assigned, a new execution ID will be created.</span></span> |
| <span data-ttu-id="0601c-247">bool execute</span><span class="sxs-lookup"><span data-stu-id="0601c-247">bool execute</span></span>             | <span data-ttu-id="0601c-248">このパラメーターを **True** に設定して対象の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0601c-248">Set this parameter to **True** to run the target step.</span></span> <span data-ttu-id="0601c-249">それ以外の場合、**False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="0601c-249">Otherwise, set it to **False**.</span></span> |
| <span data-ttu-id="0601c-250">bool overwrite</span><span class="sxs-lookup"><span data-stu-id="0601c-250">bool overwrite</span></span>           | <span data-ttu-id="0601c-251">パッケージ内で複合エンティティを使用する場合は、このパラメーターを常に **False** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0601c-251">This parameter must always be set to **False** when a composite entity is used in a package.</span></span> <span data-ttu-id="0601c-252">それ以外の場合、**True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="0601c-252">Otherwise, set it to **True**.</span></span> |
| <span data-ttu-id="0601c-253">string legalEntityId</span><span class="sxs-lookup"><span data-stu-id="0601c-253">string legalEntityId</span></span>     | <span data-ttu-id="0601c-254">データ インポートの法人。</span><span class="sxs-lookup"><span data-stu-id="0601c-254">The legal entity for the data import.</span></span> |

<span data-ttu-id="0601c-255">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="0601c-255">**Output parameters**</span></span>

| <span data-ttu-id="0601c-256">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0601c-256">Parameter</span></span>          | <span data-ttu-id="0601c-257">説明</span><span class="sxs-lookup"><span data-stu-id="0601c-257">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="0601c-258">string executionId</span><span class="sxs-lookup"><span data-stu-id="0601c-258">string executionId</span></span> | <span data-ttu-id="0601c-259">データ インポートの実行 ID。</span><span class="sxs-lookup"><span data-stu-id="0601c-259">The execution ID of the data import.</span></span> <span data-ttu-id="0601c-260">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0601c-260">This is called as Job ID in the UI.</span></span> |

> [!NOTE]
> <span data-ttu-id="0601c-261">**ImportFromPackage()** はバッチを使用してインポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="0601c-261">**ImportFromPackage()** uses a batch to perform the import.</span></span> <span data-ttu-id="0601c-262">したがって、並行インポートを実行するために、データ管理で並列処理ルールを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0601c-262">Therefore, parallel processing rules must be used in Data management to perform parallel imports.</span></span> <span data-ttu-id="0601c-263">**ImportFromPackage()** を並列スレッドで呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="0601c-263">**ImportFromPackage()** must not be called in parallel threads.</span></span> <span data-ttu-id="0601c-264">それ以外の場合、これは失敗します。</span><span class="sxs-lookup"><span data-stu-id="0601c-264">Otherwise, it will fail.</span></span>

## <a name="export-apis"></a><span data-ttu-id="0601c-265">API をエキスポート</span><span class="sxs-lookup"><span data-stu-id="0601c-265">Export APIs</span></span>

<span data-ttu-id="0601c-266">ファイル (データ パッケージ) のエクスポートには、次の API が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-266">The following APIs are used to export files (data packages).</span></span>

### <a name="exporttopackage"></a><span data-ttu-id="0601c-267">ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="0601c-267">ExportToPackage</span></span>

<span data-ttu-id="0601c-268">**ExportToPackage** API は、データ パッケージのエクスポートを開始するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-268">The **ExportToPackage** API is used to initiate an export of a data package.</span></span> <span data-ttu-id="0601c-269">この API は、クラウド配置とオンプレミス配置の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-269">This API is applicable to both cloud deployments and on-premises deployments.</span></span>

- <span data-ttu-id="0601c-270">この API を呼び出す前に、エクスポート データ プロジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0601c-270">The export data project must be created before you call this API.</span></span> <span data-ttu-id="0601c-271">プロジェクトが存在しない場合、API の呼び出しには、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-271">If the project doesn't exist, a call to the API returns an error.</span></span>
- <span data-ttu-id="0601c-272">変更履歴がオンの場合は、最後の実行後に更新または作成されたレコードのみがエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="0601c-272">If change tracking has been turned on, only records that have been created or updated since the last run are exported.</span></span> <span data-ttu-id="0601c-273">(つまり、デルタのみが返されます。)</span><span class="sxs-lookup"><span data-stu-id="0601c-273">(In other words, only the delta is returned.)</span></span>

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

<span data-ttu-id="0601c-274">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0601c-274">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"<executionId>"
    }
}
```

<span data-ttu-id="0601c-275">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="0601c-275">**Input parameters**</span></span>

| <span data-ttu-id="0601c-276">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0601c-276">Parameter</span></span>                | <span data-ttu-id="0601c-277">説明</span><span class="sxs-lookup"><span data-stu-id="0601c-277">Description</span></span> |
|--------------------------|-------------|
| <span data-ttu-id="0601c-278">string definitionGroupId</span><span class="sxs-lookup"><span data-stu-id="0601c-278">string definitionGroupId</span></span> | <span data-ttu-id="0601c-279">エクスポート用のデータ プロジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="0601c-279">The name of the data project for export.</span></span> |
| <span data-ttu-id="0601c-280">string packageName</span><span class="sxs-lookup"><span data-stu-id="0601c-280">string packageName</span></span>       | <span data-ttu-id="0601c-281">エクスポートされたデータ パッケージの名前。</span><span class="sxs-lookup"><span data-stu-id="0601c-281">The name of the exported data package.</span></span> |
| <span data-ttu-id="0601c-282">string executionId</span><span class="sxs-lookup"><span data-stu-id="0601c-282">string executionId</span></span>       | <span data-ttu-id="0601c-283">ジョブに使用する ID。</span><span class="sxs-lookup"><span data-stu-id="0601c-283">The ID to use for the job.</span></span> <span data-ttu-id="0601c-284">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0601c-284">This is called as Job ID in the UI.</span></span> <span data-ttu-id="0601c-285">空の ID が割り当てられている場合は、新しい実行 ID が作成されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-285">If an empty ID is assigned, a new execution ID will be created.</span></span> |
| <span data-ttu-id="0601c-286">bool reExecute</span><span class="sxs-lookup"><span data-stu-id="0601c-286">bool reExecute</span></span>           | <span data-ttu-id="0601c-287">このパラメーターを **True** に設定して対象の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0601c-287">Set this parameter to **True** to run the target step.</span></span> <span data-ttu-id="0601c-288">それ以外の場合、**False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="0601c-288">Otherwise, set it to **False**.</span></span> |
| <span data-ttu-id="0601c-289">string legalEntityId</span><span class="sxs-lookup"><span data-stu-id="0601c-289">string legalEntityId</span></span>     | <span data-ttu-id="0601c-290">データ インポートの法人。</span><span class="sxs-lookup"><span data-stu-id="0601c-290">The legal entity for the data import.</span></span> |
    
<span data-ttu-id="0601c-291">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="0601c-291">**Output parameters**</span></span>

| <span data-ttu-id="0601c-292">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0601c-292">Parameter</span></span>          | <span data-ttu-id="0601c-293">説明</span><span class="sxs-lookup"><span data-stu-id="0601c-293">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="0601c-294">string executionId</span><span class="sxs-lookup"><span data-stu-id="0601c-294">string executionId</span></span> | <span data-ttu-id="0601c-295">データ エクスポートの実行 ID。</span><span class="sxs-lookup"><span data-stu-id="0601c-295">The execution ID of the data export.</span></span> <span data-ttu-id="0601c-296">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0601c-296">This is called as Job ID in the UI.</span></span> |

### <a name="getexportedpackageurl"></a><span data-ttu-id="0601c-297">GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="0601c-297">GetExportedPackageUrl</span></span>

<span data-ttu-id="0601c-298">**GetExportedPackageUrl** API は、**ExportToPackage** を呼び出すことでエクスポートされたデータ パッケージの URL を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-298">The **GetExportedPackageUrl** API is used to get the URL of the data package that was exported by a call to **ExportToPackage**.</span></span> <span data-ttu-id="0601c-299">この API は、クラウド配置とオンプレミス配置の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-299">This API is applicable to both cloud deployments and on-premises deployments.</span></span>

```csharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
BODY
{"executionId":"<Execution Id>"}
```

<span data-ttu-id="0601c-300">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0601c-300">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"https://<baseurl_id>.blob.core.windows.net/dmf/<uniqueFileName>?<SAS Token>"
    }
}
```

<span data-ttu-id="0601c-301">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="0601c-301">**Input parameters**</span></span>

| <span data-ttu-id="0601c-302">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0601c-302">Parameter</span></span>          | <span data-ttu-id="0601c-303">説明</span><span class="sxs-lookup"><span data-stu-id="0601c-303">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="0601c-304">string executionId</span><span class="sxs-lookup"><span data-stu-id="0601c-304">string executionId</span></span> | <span data-ttu-id="0601c-305">データ プロジェクト実行の実行 ID。</span><span class="sxs-lookup"><span data-stu-id="0601c-305">The execution ID of the data project run.</span></span> <span data-ttu-id="0601c-306">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0601c-306">This is called as Job ID in the UI.</span></span> |

<span data-ttu-id="0601c-307">**出力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="0601c-307">**Output parameters**</span></span>

| <span data-ttu-id="0601c-308">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0601c-308">Parameter</span></span>      | <span data-ttu-id="0601c-309">説明</span><span class="sxs-lookup"><span data-stu-id="0601c-309">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="0601c-310">string BlobUrl</span><span class="sxs-lookup"><span data-stu-id="0601c-310">string BlobUrl</span></span> | <span data-ttu-id="0601c-311">埋め込みの SAS トークンを持つ blob URL。</span><span class="sxs-lookup"><span data-stu-id="0601c-311">A blob URL that has an embedded SAS token.</span></span> <span data-ttu-id="0601c-312">URL を使用して、エクスポートしたデータ パッケージをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="0601c-312">The URL can be used to download the exported data package.</span></span> |

## <a name="status-check-api"></a><span data-ttu-id="0601c-313">ステータス チェック API</span><span class="sxs-lookup"><span data-stu-id="0601c-313">Status check API</span></span> 

<span data-ttu-id="0601c-314">状態を確認するには、次の API を使用します。</span><span class="sxs-lookup"><span data-stu-id="0601c-314">The following APIs are used to check status.</span></span> <span data-ttu-id="0601c-315">これらは、インポート フローとエクスポート フローの両方で使用されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-315">They are used during both import flows and export flows.</span></span>

### <a name="getexecutionsummarystatus"></a><span data-ttu-id="0601c-316">GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="0601c-316">GetExecutionSummaryStatus</span></span>

<span data-ttu-id="0601c-317">**GetExecutionSummaryStatus** API は、インポート ジョブとエクスポート ジョブの両方に使用されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-317">The **GetExecutionSummaryStatus** API is used for both import jobs and export jobs.</span></span> <span data-ttu-id="0601c-318">これは、データ プロジェクト実行ジョブのステータスの確認に使用されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-318">It's used to check the status of a data project execution job.</span></span> <span data-ttu-id="0601c-319">この API は、クラウド配置とオンプレミス配置の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-319">This API is applicable to both cloud deployments and on-premises deployments.</span></span>

```csharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
BODY
{"executionId":"<executionId>"}
```

<span data-ttu-id="0601c-320">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0601c-320">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":"<executionStatus>"
}
```

<span data-ttu-id="0601c-321">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="0601c-321">**Input parameters**</span></span>

| <span data-ttu-id="0601c-322">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0601c-322">Parameter</span></span>          | <span data-ttu-id="0601c-323">説明</span><span class="sxs-lookup"><span data-stu-id="0601c-323">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="0601c-324">string executionId</span><span class="sxs-lookup"><span data-stu-id="0601c-324">string executionId</span></span> | <span data-ttu-id="0601c-325">データ プロジェクト実行の実行 ID。</span><span class="sxs-lookup"><span data-stu-id="0601c-325">The execution ID of the data project run.</span></span> <span data-ttu-id="0601c-326">これは、UI ではジョブ ID と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0601c-326">This is called as Job ID in the UI.</span></span> |

<span data-ttu-id="0601c-327">**出力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="0601c-327">**Output parameters**</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0601c-328">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0601c-328">Parameter</span></span></th>
<th><span data-ttu-id="0601c-329">説明</span><span class="sxs-lookup"><span data-stu-id="0601c-329">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0601c-330">DMFExecutionSummaryStatus executionStatus</span><span class="sxs-lookup"><span data-stu-id="0601c-330">DMFExecutionSummaryStatus executionStatus</span></span></td>
<td><span data-ttu-id="0601c-331">実行のステータス。</span><span class="sxs-lookup"><span data-stu-id="0601c-331">The execution status.</span></span> <span data-ttu-id="0601c-332">以下に使用可能な値を示します。</span><span class="sxs-lookup"><span data-stu-id="0601c-332">Here are the possible values:</span></span>
<ul>
<li><span data-ttu-id="0601c-333">不明</span><span class="sxs-lookup"><span data-stu-id="0601c-333">Unknown</span></span></li>
<li><span data-ttu-id="0601c-334">NotRun</span><span class="sxs-lookup"><span data-stu-id="0601c-334">NotRun</span></span></li>
<li><span data-ttu-id="0601c-335">実行中</span><span class="sxs-lookup"><span data-stu-id="0601c-335">Executing</span></span></li>
<li><span data-ttu-id="0601c-336">成功</span><span class="sxs-lookup"><span data-stu-id="0601c-336">Succeeded</span></span></li>
<li><span data-ttu-id="0601c-337">PartiallySucceeded</span><span class="sxs-lookup"><span data-stu-id="0601c-337">PartiallySucceeded</span></span></li>
<li><span data-ttu-id="0601c-338">失敗</span><span class="sxs-lookup"><span data-stu-id="0601c-338">Failed</span></span></li>
<li><span data-ttu-id="0601c-339">取消済</span><span class="sxs-lookup"><span data-stu-id="0601c-339">Canceled</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="0601c-340">Blob ストレージ内のファイルはストレージに 7 日間残ります。</span><span class="sxs-lookup"><span data-stu-id="0601c-340">The file in Blob storage will remain there for seven days.</span></span> <span data-ttu-id="0601c-341">次に、そのファイルは自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="0601c-341">It will then be automatically deleted.</span></span>

## <a name="getting-the-list-of-errors"></a><span data-ttu-id="0601c-342">エラーの一覧を取得する</span><span class="sxs-lookup"><span data-stu-id="0601c-342">Getting the list of errors</span></span>
<span data-ttu-id="0601c-343">GetExecutionErrors は、ジョブ実行のエラーのリストを取得するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="0601c-343">GetExecutionErrors can be used to get the list of errors in a job execution.</span></span> <span data-ttu-id="0601c-344">API は、Execution ID をパラメーターとして取り、JSON リストでエラー メッセージのセットを返します。</span><span class="sxs-lookup"><span data-stu-id="0601c-344">The API takes the Execution ID as the parameter, and returns a set of error messages in a JSON list.</span></span>

```json
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionErrors
BODY
{"executionId":"<executionId>"}
```

## <a name="import-and-export-processes"></a><span data-ttu-id="0601c-345">プロセスのインポートとエクスポート</span><span class="sxs-lookup"><span data-stu-id="0601c-345">Import and export processes</span></span>

<span data-ttu-id="0601c-346">次の図は、データ管理パッケージ メソッドを使用してデータ パッケージをインポートする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="0601c-346">The following illustration shows how the Data management package methods can be used to import data packages.</span></span>

![データ管理パッケージ メソッドを使用するデータ パッケージ ファイルのインポート](./media/data-package-import.png)

<span data-ttu-id="0601c-348">次の図は、データ管理パッケージ メソッドを使用してデータ パッケージをエクスポートする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="0601c-348">The following illustration shows how the Data management package methods can be used to export data packages.</span></span>

![データ管理パッケージ メソッドを使用するデータ パッケージ ファイルのエクスポート](./media/data-package-export.png)

<span data-ttu-id="0601c-350">データのインポートとデータのエクスポートのメソッドを紹介するサンプルのコンソール アプリケーションは、 GitHub から入手できます。</span><span class="sxs-lookup"><span data-stu-id="0601c-350">A sample console application that showcases the data import and data export methods is available on GitHub.</span></span> <span data-ttu-id="0601c-351">詳細については、「<https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/FileBasedIntegrationSamples/ConsoleAppSamples>」に移動してください。</span><span class="sxs-lookup"><span data-stu-id="0601c-351">For more information, go to <https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/FileBasedIntegrationSamples/ConsoleAppSamples>.</span></span>
