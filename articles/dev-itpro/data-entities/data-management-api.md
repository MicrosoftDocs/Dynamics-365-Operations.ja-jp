---
title: "データ管理パッケージ統合 API"
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 644c0fb6ff197d4666b7875e2a89e3c3c04d0b6f
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="data-management-package-api"></a><span data-ttu-id="8576c-103">データ管理パッケージ API</span><span class="sxs-lookup"><span data-stu-id="8576c-103">Data management package API</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8576c-104">このトピックでは、データ管理フレームワークのパッケージ表現型状態移行 (REST) のアプリケーション プログラミング インターフェイス (API) について説明します。</span><span class="sxs-lookup"><span data-stu-id="8576c-104">This topic describes the data management framework's package representational state transfer (REST) application programming interface (API).</span></span> <span data-ttu-id="8576c-105">パッケージ API を使用すると、データ パッケージを使用して、Microsoft Dynamics 365 for Finance and Operations と統合することができます。</span><span class="sxs-lookup"><span data-stu-id="8576c-105">The package API lets you integrate with Microsoft Dynamics 365 for Finance and Operations, by using data packages.</span></span> <span data-ttu-id="8576c-106">REST API は、クラウドおよびオンプレミス展開の両方で使用できます。</span><span class="sxs-lookup"><span data-stu-id="8576c-106">The REST API can be used with both cloud and on-premises deployments.</span></span> <span data-ttu-id="8576c-107">オンプレミス配置については、現在この機能はバージョン 7.2、プラットフォーム更新プログラム 12、ビルド 7.0.4709.41184 以降で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="8576c-107">For on-premises deployments this functionality is currently available for version 7.2, Platform update 12, build 7.0.4709.41184, and later.</span></span>

<span data-ttu-id="8576c-108">オンプレミス サポートは追加されましたが、API の名前は変更されていないため、クラウドおよびオンプレミスの両方の展開は単一の API 設定で保持できます。</span><span class="sxs-lookup"><span data-stu-id="8576c-108">Although on-premises support has been added, API names have not been changed, so that we can keep a single API set for both cloud and on-premises deployments.</span></span>

## <a name="choosing-an-integration-api"></a><span data-ttu-id="8576c-109">統合 API の選択</span><span class="sxs-lookup"><span data-stu-id="8576c-109">Choosing an integration API</span></span>
<span data-ttu-id="8576c-110">Finance and Operations の 2 つの API は、データ管理フレームワークのパッケージ API と定期的な統合 API というファイル ベースの統合シナリオをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="8576c-110">Two APIs in Finance and Operations support file-based integration scenarios: the data management framework's package API and the recurring integrations API.</span></span> <span data-ttu-id="8576c-111">どちらの API もデータ インポート シナリオとデータ エクスポート シナリオの両方をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="8576c-111">Both APIs support both data import scenarios and data export scenarios.</span></span> <span data-ttu-id="8576c-112">次のテーブルでは、使用する API を決定する際に考慮する必要がある主な決定事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="8576c-112">The following table describes the main decision points that you should consider when you're trying to decide which API to use.</span></span> 

| <span data-ttu-id="8576c-113">決定ポイント</span><span class="sxs-lookup"><span data-stu-id="8576c-113">Decision point</span></span>      | <span data-ttu-id="8576c-114">定期統合 API</span><span class="sxs-lookup"><span data-stu-id="8576c-114">Recurring integrations API</span></span> | <span data-ttu-id="8576c-115">データ管理フレームワークのパッケージ API</span><span class="sxs-lookup"><span data-stu-id="8576c-115">Data management framework's package API</span></span> |
|---------------------|----------------------------|-----------------------------|
| <span data-ttu-id="8576c-116">スケジューリング</span><span class="sxs-lookup"><span data-stu-id="8576c-116">Scheduling</span></span>          | <span data-ttu-id="8576c-117">Finance and Operations のスケジュール設定</span><span class="sxs-lookup"><span data-stu-id="8576c-117">Scheduling in Finance and Operations</span></span> | <span data-ttu-id="8576c-118">Finance and Operations 外でのスケジュール設定</span><span class="sxs-lookup"><span data-stu-id="8576c-118">Scheduling outside Finance and Operations</span></span> |
| <span data-ttu-id="8576c-119">書式設定</span><span class="sxs-lookup"><span data-stu-id="8576c-119">Format</span></span>              | <span data-ttu-id="8576c-120">ファイルおよびデータ パッケージ</span><span class="sxs-lookup"><span data-stu-id="8576c-120">Files and data packages</span></span> | <span data-ttu-id="8576c-121">データ パッケージのみ</span><span class="sxs-lookup"><span data-stu-id="8576c-121">Only data packages</span></span>  |
| <span data-ttu-id="8576c-122">変換</span><span class="sxs-lookup"><span data-stu-id="8576c-122">Transformation</span></span>      | <span data-ttu-id="8576c-123">データ ファイルが XML 形式の場合の Extensible Stylesheet Language Transformations (XSLT) のサポート</span><span class="sxs-lookup"><span data-stu-id="8576c-123">Support for Extensible Stylesheet Language Transformations (XSLT) if the data file is in XML format</span></span> | <span data-ttu-id="8576c-124">システム外部での変換</span><span class="sxs-lookup"><span data-stu-id="8576c-124">Transformations that are external to the system</span></span> |
| <span data-ttu-id="8576c-125">サポートされているプロトコル</span><span class="sxs-lookup"><span data-stu-id="8576c-125">Supported protocols</span></span> | <span data-ttu-id="8576c-126">SOAP および REST</span><span class="sxs-lookup"><span data-stu-id="8576c-126">SOAP and REST</span></span> | <span data-ttu-id="8576c-127">REST</span><span class="sxs-lookup"><span data-stu-id="8576c-127">REST</span></span> |
| <span data-ttu-id="8576c-128">サービス タイプ</span><span class="sxs-lookup"><span data-stu-id="8576c-128">Service type</span></span>        | <span data-ttu-id="8576c-129">顧客サービス</span><span class="sxs-lookup"><span data-stu-id="8576c-129">Custom service</span></span> | <span data-ttu-id="8576c-130">データ プロトコル (OData) アクションを開きます</span><span class="sxs-lookup"><span data-stu-id="8576c-130">Open Data Protocol (OData) action</span></span> |
| <span data-ttu-id="8576c-131">適用の対象</span><span class="sxs-lookup"><span data-stu-id="8576c-131">Availability</span></span>        | <span data-ttu-id="8576c-132">2016 年 2 月リリース (RTW) 以降</span><span class="sxs-lookup"><span data-stu-id="8576c-132">February 2016 release (RTW) and later</span></span> | <span data-ttu-id="8576c-133">プラットフォーム更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="8576c-133">Platform update 5 and later</span></span>  |

<span data-ttu-id="8576c-134">定期的な統合 API がデータ管理のフレームワーク パッケージ API の要件を満たしている場合、「[定期統合](recurring-integrations.md)」を参照します。</span><span class="sxs-lookup"><span data-stu-id="8576c-134">If you decide that the recurring integrations API meets your requirement better than the data management framework's package API, see [Recurring integrations](recurring-integrations.md).</span></span> <span data-ttu-id="8576c-135">このトピックの残りの部分では、データ管理フレームワークのパッケージ API について説明します。</span><span class="sxs-lookup"><span data-stu-id="8576c-135">The rest of this topic discusses the data management framework's package API.</span></span>

## <a name="authorization"></a><span data-ttu-id="8576c-136">認証</span><span class="sxs-lookup"><span data-stu-id="8576c-136">Authorization</span></span>
<span data-ttu-id="8576c-137">データ管理フレームワークのパッケージ API は、アクセスを認可するために OAuth 2.0 を使用します。</span><span class="sxs-lookup"><span data-stu-id="8576c-137">The data management framework's package API uses OAuth 2.0 for authorizing access.</span></span> <span data-ttu-id="8576c-138">API は、有効な OAuth アクセス トークンを使用して呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8576c-138">The API must be called by using a valid OAuth access token.</span></span> <span data-ttu-id="8576c-139">OAuth 2.0 および Microsoft Azure Active Directory (Azure AD) に関する詳細については、[OAuth 2.0 および Azure Active Directory を使用してWeb アプリケーションへのアクセスを承認する](/azure/active-directory/develop/active-directory-protocols-oauth-code) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8576c-139">For more details about OAuth 2.0 and Microsoft Azure Active Directory (Azure AD), see [Authorize access to web applications using OAuth 2.0 and Azure Active Directory](/azure/active-directory/develop/active-directory-protocols-oauth-code).</span></span> <span data-ttu-id="8576c-140">オンプレミス配置については、Active Directory フェデレーション サービス (AD FS) が認証に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8576c-140">For on-premises deployments, Active Directory Federation Services (AD FS) will be used for authorization.</span></span> 

> [!NOTE]
> <span data-ttu-id="8576c-141">クライアント資格情報の付与フローを使用すると、Finance and Operations はアクセス制御リストを保持します。</span><span class="sxs-lookup"><span data-stu-id="8576c-141">When you use the Client Credentials Grant flow, Finance and Operations maintains an access control list.</span></span> <span data-ttu-id="8576c-142">アクセス制御リストは **システム管理** > **設定** > **Azure Active Directory アプリケーション** で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="8576c-142">You can find the access control list at **System administration** > **Setup** > **Azure Active Directory applications**.</span></span> <span data-ttu-id="8576c-143">**Azure Active Directory アプリケーション** ページには、承認済クライアント ID と、クライアント資格情報付与フローを使用して API が呼び出されたときに適用する必要があるユーザー セキュリティ マッピングが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8576c-143">The **Azure Active Directory applications** page shows the approved client IDs and the user security mapping that should be enforced when the API is called by using the Client Credentials Grant flow.</span></span> <span data-ttu-id="8576c-144">オンプレミス配置については、このリストには AD FS からの有効なクライアント ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="8576c-144">For on-premises deployments, this list must have a valid client ID from AD FS.</span></span>

## <a name="import-apis"></a><span data-ttu-id="8576c-145">API のインポート</span><span class="sxs-lookup"><span data-stu-id="8576c-145">Import APIs</span></span>
<span data-ttu-id="8576c-146">ファイル (データ パッケージ) のインポートには、次の API が使用されます。</span><span class="sxs-lookup"><span data-stu-id="8576c-146">The following APIs are used to do file (data package) imports.</span></span>

### <a name="getazurewritableurl"></a><span data-ttu-id="8576c-147">GetAzureWritableUrl</span><span class="sxs-lookup"><span data-stu-id="8576c-147">GetAzureWritableUrl</span></span>
<span data-ttu-id="8576c-148">**GetAzureWritableUrl** API は、書き込み可能な Blob URL を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8576c-148">The **GetAzureWritableUrl** API is used to get a writable blob URL.</span></span> <span data-ttu-id="8576c-149">このメソッドには、URL に埋め込まれた共有アクセス署名 (SAS) トークンが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8576c-149">This method includes a shared access signature (SAS) token that is embedded in the URL.</span></span> <span data-ttu-id="8576c-150">この方法を使用すると、Finance and Operations の Azure Blob Storage コンテナーにデータ パッケージをアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="8576c-150">You can use this method to upload a data package to the Azure Blob storage container for Finance and Operations.</span></span> <span data-ttu-id="8576c-151">オンプレミス配置については、この API はローカル ストレージに取り除かれた URL を引き続き返します。</span><span class="sxs-lookup"><span data-stu-id="8576c-151">For on-premises deployments, this API will still return the URL which has been abstracted to local storage.</span></span> 

> [!NOTE]
> <span data-ttu-id="8576c-152">SAS は有効期限の時間枠中にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="8576c-152">An SAS is valid only during an expiry time window.</span></span> <span data-ttu-id="8576c-153">ウィンドウが経過した後に発行されるすべての要求はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="8576c-153">Any request that is issued after the window has passed returns an error.</span></span> <span data-ttu-id="8576c-154">詳細については、[共有アクセス署名 (SA) の使用](/azure/storage/common/storage-dotnet-shared-access-signature-part-1) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8576c-154">For more information, see [Using shared access signatures (SAS)](/azure/storage/common/storage-dotnet-shared-access-signature-part-1).</span></span>

```CSharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetAzureWriteUrl
BODY
{
    "uniqueFileName":"<string>",
}
```

<span data-ttu-id="8576c-155">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="8576c-155">Here is an example of a successful response.</span></span>

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

<span data-ttu-id="8576c-156">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="8576c-156">**Input parameters**</span></span>

| <span data-ttu-id="8576c-157">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8576c-157">Parameter</span></span>         | <span data-ttu-id="8576c-158">説明</span><span class="sxs-lookup"><span data-stu-id="8576c-158">Description</span></span>  |
|-------------------|--------------|
| <span data-ttu-id="8576c-159">string packageUrl</span><span class="sxs-lookup"><span data-stu-id="8576c-159">string packageUrl</span></span> | <span data-ttu-id="8576c-160">BLOB ID を追跡するために使用される一意のファイル名。</span><span class="sxs-lookup"><span data-stu-id="8576c-160">A unique file name that is used to track blob IDs.</span></span> <span data-ttu-id="8576c-161">一意のファイル名であることを保証するため、グローバル一意識別子 (GUID) を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="8576c-161">You can include a globally unique identifier (GUID) to help guarantee a unique file name.</span></span> |

<span data-ttu-id="8576c-162">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="8576c-162">**Output parameters**</span></span>

| <span data-ttu-id="8576c-163">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8576c-163">Parameter</span></span>      | <span data-ttu-id="8576c-164">説明</span><span class="sxs-lookup"><span data-stu-id="8576c-164">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="8576c-165">string BlobId</span><span class="sxs-lookup"><span data-stu-id="8576c-165">string BlobId</span></span>  | <span data-ttu-id="8576c-166">割り当てられた BLOB コンテナーの BLOB ID。</span><span class="sxs-lookup"><span data-stu-id="8576c-166">The blob ID of the allocated blob container.</span></span> |
| <span data-ttu-id="8576c-167">string BlobUrl</span><span class="sxs-lookup"><span data-stu-id="8576c-167">string BlobUrl</span></span> | <span data-ttu-id="8576c-168">埋め込まれた SAS トークンを持つ URL。</span><span class="sxs-lookup"><span data-stu-id="8576c-168">A URL with an embedded SAS token.</span></span> <span data-ttu-id="8576c-169">URL を使用 して BLOB ストレージに書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="8576c-169">The URL can be used to write to blob storage.</span></span> |


### <a name="importfrompackage"></a><span data-ttu-id="8576c-170">ImportFromPackage</span><span class="sxs-lookup"><span data-stu-id="8576c-170">ImportFromPackage</span></span>
<span data-ttu-id="8576c-171">**ImportFromPackage** API は、Finance and Operations の実装に関連付けられている Azure Blob Storage にアップロードされるデータ パッケージからインポートを開始するために使用します。</span><span class="sxs-lookup"><span data-stu-id="8576c-171">The **ImportFromPackage** API is used to initiate an import from the data package that is uploaded to the Azure Blob storage that is associated with your implementation of Finance and Operations.</span></span> <span data-ttu-id="8576c-172">オンプレミス配置については、ファイルが以前にアップロードされたローカル ストレージから、インポートが開始されます。</span><span class="sxs-lookup"><span data-stu-id="8576c-172">For on-premises deployments, the import will be initiated from the local storage to which the file was uploaded previously.</span></span>

<span data-ttu-id="8576c-173">注記: プラットフォーム更新プログラム 12 を開始すると、ImportFromPackage は複合エンティティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="8576c-173">Note: Starting platform update 12, ImportFromPackage will support composite entity.</span></span> <span data-ttu-id="8576c-174">ただし、パッケージで 1 つの複合エンティティのみを持つという制限があります。</span><span class="sxs-lookup"><span data-stu-id="8576c-174">However, the limitation is to have only one composite entity in a package.</span></span>

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

<span data-ttu-id="8576c-175">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="8576c-175">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"<executionId>"
    }
}
```

<span data-ttu-id="8576c-176">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="8576c-176">**Input parameters**</span></span>

| <span data-ttu-id="8576c-177">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8576c-177">Parameter</span></span>                | <span data-ttu-id="8576c-178">説明</span><span class="sxs-lookup"><span data-stu-id="8576c-178">Description</span></span> |
|--------------------------|-------------|
| <span data-ttu-id="8576c-179">string packageUrl</span><span class="sxs-lookup"><span data-stu-id="8576c-179">string packageUrl</span></span>        | <span data-ttu-id="8576c-180">Finance and Operations に関連付けられている Azure BLOB Storage 内のデータ パッケージの URL。</span><span class="sxs-lookup"><span data-stu-id="8576c-180">The URL of the data package in the Azure Blob storage that is associated with Finance and Operations.</span></span> |
| <span data-ttu-id="8576c-181">string definitionGroupId</span><span class="sxs-lookup"><span data-stu-id="8576c-181">string definitionGroupId</span></span> | <span data-ttu-id="8576c-182">インポート用のデータ プロジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="8576c-182">The name of the data project for import.</span></span> |
| <span data-ttu-id="8576c-183">string executionId</span><span class="sxs-lookup"><span data-stu-id="8576c-183">string executionId</span></span>       | <span data-ttu-id="8576c-184">ジョブに使用する ID。</span><span class="sxs-lookup"><span data-stu-id="8576c-184">The ID to use for the job.</span></span> <span data-ttu-id="8576c-185">空の ID が割り当てられている場合は、新しい実行 ID が作成されます。</span><span class="sxs-lookup"><span data-stu-id="8576c-185">If an empty ID is assigned, a new execution ID will be created.</span></span> |
| <span data-ttu-id="8576c-186">bool execute</span><span class="sxs-lookup"><span data-stu-id="8576c-186">bool execute</span></span>             | <span data-ttu-id="8576c-187">このパラメーターを **True** に設定して対象の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8576c-187">Set this parameter to **True** to run the target step.</span></span> <span data-ttu-id="8576c-188">それ以外の場合、**False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8576c-188">Otherwise, set it to **False**.</span></span> |
| <span data-ttu-id="8576c-189">bool overwrite</span><span class="sxs-lookup"><span data-stu-id="8576c-189">bool overwrite</span></span>           | <span data-ttu-id="8576c-190">パッケージ内で複合エンティティを使用する場合は、常に **False** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8576c-190">This must always be set to **False** when using a composite entity in a package.</span></span> <span data-ttu-id="8576c-191">それ以外の場合、**True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8576c-191">Otherwise, set it to **True**</span></span> |
| <span data-ttu-id="8576c-192">string legalEntityId</span><span class="sxs-lookup"><span data-stu-id="8576c-192">string legalEntityId</span></span>     | <span data-ttu-id="8576c-193">データ インポートの法人。</span><span class="sxs-lookup"><span data-stu-id="8576c-193">The legal entity for the data import.</span></span> |             

<span data-ttu-id="8576c-194">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="8576c-194">**Output parameters**</span></span>

| <span data-ttu-id="8576c-195">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8576c-195">Parameter</span></span>          | <span data-ttu-id="8576c-196">説明</span><span class="sxs-lookup"><span data-stu-id="8576c-196">Description</span></span>  |
|--------------------|--------------|
| <span data-ttu-id="8576c-197">string executionId</span><span class="sxs-lookup"><span data-stu-id="8576c-197">string executionId</span></span> | <span data-ttu-id="8576c-198">データ インポートの実行 ID。</span><span class="sxs-lookup"><span data-stu-id="8576c-198">The execution ID of the data import.</span></span> |

## <a name="export-apis"></a><span data-ttu-id="8576c-199">API をエキスポート</span><span class="sxs-lookup"><span data-stu-id="8576c-199">Export APIs</span></span>
<span data-ttu-id="8576c-200">ファイル (データ パッケージ) のエクスポートには、次の API が使用されます。</span><span class="sxs-lookup"><span data-stu-id="8576c-200">The following APIs are used to do file (data package) exports.</span></span>

### <a name="exporttopackage"></a><span data-ttu-id="8576c-201">ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="8576c-201">ExportToPackage</span></span>
<span data-ttu-id="8576c-202">**ExportToPackage** API は、データ パッケージのエクスポートを開始するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8576c-202">The **ExportToPackage** API is used to initiate an export of a data package.</span></span> <span data-ttu-id="8576c-203">これは、クラウドとオンプレミスの両方の展開に適用されます。</span><span class="sxs-lookup"><span data-stu-id="8576c-203">This is applicable to both cloud and on-premises deployments.</span></span>

- <span data-ttu-id="8576c-204">この API を呼び出す前に、エクスポート データ プロジェクトを Finance and Operations で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8576c-204">The export data project must be created in Finance and Operations before you call this API.</span></span> <span data-ttu-id="8576c-205">プロジェクトが存在しない場合、API の呼び出しには、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="8576c-205">If the project doesn't exist, a call to the API returns an error.</span></span>
- <span data-ttu-id="8576c-206">変更履歴がオンの場合は、最後の実行後に更新または作成されたレコードのみがエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="8576c-206">If change tracking has been turned on, only records that have been created or updated since the last run are exported.</span></span> <span data-ttu-id="8576c-207">(つまり、デルタのみが返されます。)</span><span class="sxs-lookup"><span data-stu-id="8576c-207">(In other words, only the delta is returned.)</span></span>

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

<span data-ttu-id="8576c-208">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="8576c-208">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"<executionId>"
    }
}
```

<span data-ttu-id="8576c-209">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="8576c-209">**Input parameters**</span></span>

| <span data-ttu-id="8576c-210">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8576c-210">Parameter</span></span>                | <span data-ttu-id="8576c-211">説明</span><span class="sxs-lookup"><span data-stu-id="8576c-211">Description</span></span> |
|--------------------------|-------------|
| <span data-ttu-id="8576c-212">string definitionGroupId</span><span class="sxs-lookup"><span data-stu-id="8576c-212">string definitionGroupId</span></span> | <span data-ttu-id="8576c-213">エクスポート用のデータ プロジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="8576c-213">The name of the data project for export.</span></span> |
| <span data-ttu-id="8576c-214">string packageName</span><span class="sxs-lookup"><span data-stu-id="8576c-214">string packageName</span></span>       | <span data-ttu-id="8576c-215">エクスポートされたデータ パッケージの名前。</span><span class="sxs-lookup"><span data-stu-id="8576c-215">The name of the exported data package.</span></span> |
| <span data-ttu-id="8576c-216">string executionId</span><span class="sxs-lookup"><span data-stu-id="8576c-216">string executionId</span></span>       | <span data-ttu-id="8576c-217">ジョブに使用する ID。</span><span class="sxs-lookup"><span data-stu-id="8576c-217">The ID to use for the job.</span></span> <span data-ttu-id="8576c-218">空の ID が割り当てられている場合は、新しい実行 ID が作成されます。</span><span class="sxs-lookup"><span data-stu-id="8576c-218">If an empty ID is assigned, a new execution ID will be created.</span></span> |
| <span data-ttu-id="8576c-219">bool reExecute</span><span class="sxs-lookup"><span data-stu-id="8576c-219">bool reExecute</span></span>           | <span data-ttu-id="8576c-220">このパラメーターを **True** に設定して対象の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8576c-220">Set this parameter to **True** to run the target step.</span></span> <span data-ttu-id="8576c-221">それ以外の場合、**False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8576c-221">Otherwise, set it to **False**.</span></span> |
| <span data-ttu-id="8576c-222">string legalEntityId</span><span class="sxs-lookup"><span data-stu-id="8576c-222">string legalEntityId</span></span>     | <span data-ttu-id="8576c-223">データ インポートの法人。</span><span class="sxs-lookup"><span data-stu-id="8576c-223">The legal entity for the data import.</span></span> |
    
<span data-ttu-id="8576c-224">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="8576c-224">**Output parameters**</span></span>

| <span data-ttu-id="8576c-225">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8576c-225">Parameter</span></span>          | <span data-ttu-id="8576c-226">説明</span><span class="sxs-lookup"><span data-stu-id="8576c-226">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="8576c-227">string executionId</span><span class="sxs-lookup"><span data-stu-id="8576c-227">string executionId</span></span> | <span data-ttu-id="8576c-228">データ エクスポートの実行 ID。</span><span class="sxs-lookup"><span data-stu-id="8576c-228">The execution ID of the data export.</span></span> |

### <a name="getexportedpackageurl"></a><span data-ttu-id="8576c-229">GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="8576c-229">GetExportedPackageUrl</span></span>
<span data-ttu-id="8576c-230">**GetExportedPackageUrl** API は、**ExportToPackage** を呼び出すことでエクスポートされたデータ パッケージの URL を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8576c-230">The **GetExportedPackageUrl** API is used to get the URL of the data package that was exported by a call to **ExportToPackage**.</span></span> <span data-ttu-id="8576c-231">これは、クラウドとオンプレミスの両方の展開に適用されます。</span><span class="sxs-lookup"><span data-stu-id="8576c-231">This is applicable to both cloud and on-premises deployments.</span></span>

```CSharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
BODY
{"executionId":"<Execution Id>"}
```

<span data-ttu-id="8576c-232">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="8576c-232">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"https://<baseurl_id>.blob.core.windows.net/dmf/<uniqueFileName>?<SAS Token>"
    }
}
```

<span data-ttu-id="8576c-233">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="8576c-233">**Input parameters**</span></span>

| <span data-ttu-id="8576c-234">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8576c-234">Parameter</span></span>          | <span data-ttu-id="8576c-235">説明</span><span class="sxs-lookup"><span data-stu-id="8576c-235">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="8576c-236">string executionId</span><span class="sxs-lookup"><span data-stu-id="8576c-236">string executionId</span></span> | <span data-ttu-id="8576c-237">データ プロジェクト実行の実行 ID。</span><span class="sxs-lookup"><span data-stu-id="8576c-237">The execution ID of the data project run.</span></span> |

<span data-ttu-id="8576c-238">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="8576c-238">**Output parameters**</span></span>

| <span data-ttu-id="8576c-239">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8576c-239">Parameter</span></span>      | <span data-ttu-id="8576c-240">説明</span><span class="sxs-lookup"><span data-stu-id="8576c-240">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="8576c-241">string BlobUrl</span><span class="sxs-lookup"><span data-stu-id="8576c-241">string BlobUrl</span></span> | <span data-ttu-id="8576c-242">埋め込みの SAS トークンを持つ blob URL。</span><span class="sxs-lookup"><span data-stu-id="8576c-242">A blob URL that has an embedded SAS token.</span></span> <span data-ttu-id="8576c-243">URL を使用して、エクスポートしたデータ パッケージをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="8576c-243">The URL can be used to download the exported data package.</span></span> |

## <a name="status-check-api"></a><span data-ttu-id="8576c-244">ステータス チェック API</span><span class="sxs-lookup"><span data-stu-id="8576c-244">Status check API</span></span> 
<span data-ttu-id="8576c-245">状態を確認するには、次の API を使用します。</span><span class="sxs-lookup"><span data-stu-id="8576c-245">The following APIs are used to check status.</span></span> <span data-ttu-id="8576c-246">これらは、インポート フローとエクスポート フローの両方で使用されます。</span><span class="sxs-lookup"><span data-stu-id="8576c-246">They are used during both import flows and export flows.</span></span>

### <a name="getexecutionsummarystatus"></a><span data-ttu-id="8576c-247">GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="8576c-247">GetExecutionSummaryStatus</span></span>
<span data-ttu-id="8576c-248">**GetExecutionSummaryStatus** API は、データ プロジェクト実行ジョブのステータスを確認するためにインポート ジョブおよびエクスポート ジョブの両方に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8576c-248">The **GetExecutionSummaryStatus** API is used for both import jobs and export jobs to check the status of a data project execution job.</span></span> <span data-ttu-id="8576c-249">これは、クラウドとオンプレミスの両方の展開に適用されます。</span><span class="sxs-lookup"><span data-stu-id="8576c-249">This is applicable to both cloud and on-premises deployments.</span></span>

```CSharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
BODY
{"executionId":"<executionId>"}
```

<span data-ttu-id="8576c-250">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="8576c-250">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"<executionStatus>"
    }
}
```

<span data-ttu-id="8576c-251">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="8576c-251">**Input parameters**</span></span>

| <span data-ttu-id="8576c-252">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8576c-252">Parameter</span></span>          | <span data-ttu-id="8576c-253">説明</span><span class="sxs-lookup"><span data-stu-id="8576c-253">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="8576c-254">string executionId</span><span class="sxs-lookup"><span data-stu-id="8576c-254">string executionId</span></span> | <span data-ttu-id="8576c-255">データ プロジェクト実行の実行 ID。</span><span class="sxs-lookup"><span data-stu-id="8576c-255">The execution ID of the data project run.</span></span> |

<span data-ttu-id="8576c-256">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="8576c-256">**Output parameters**</span></span>

| <span data-ttu-id="8576c-257">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8576c-257">Parameter</span></span>                                 | <span data-ttu-id="8576c-258">説明</span><span class="sxs-lookup"><span data-stu-id="8576c-258">Description</span></span> |
|-------------------------------------------|-------------|
| <span data-ttu-id="8576c-259">DMFExecutionSummaryStatus executionStatus</span><span class="sxs-lookup"><span data-stu-id="8576c-259">DMFExecutionSummaryStatus executionStatus</span></span> | <span data-ttu-id="8576c-260">実行のステータス。</span><span class="sxs-lookup"><span data-stu-id="8576c-260">The execution status.</span></span> |

<span data-ttu-id="8576c-261">実行状態の使用可能な値を次に示します。</span><span class="sxs-lookup"><span data-stu-id="8576c-261">Here are the possible values for the execution status:</span></span>

- <span data-ttu-id="8576c-262">不明</span><span class="sxs-lookup"><span data-stu-id="8576c-262">Unknown</span></span>
- <span data-ttu-id="8576c-263">NotRun</span><span class="sxs-lookup"><span data-stu-id="8576c-263">NotRun</span></span>
- <span data-ttu-id="8576c-264">実行</span><span class="sxs-lookup"><span data-stu-id="8576c-264">Executing</span></span>
- <span data-ttu-id="8576c-265">成功</span><span class="sxs-lookup"><span data-stu-id="8576c-265">Succeeded</span></span>
- <span data-ttu-id="8576c-266">PartiallySucceeded</span><span class="sxs-lookup"><span data-stu-id="8576c-266">PartiallySucceeded</span></span>
- <span data-ttu-id="8576c-267">失敗</span><span class="sxs-lookup"><span data-stu-id="8576c-267">Failed</span></span>
- <span data-ttu-id="8576c-268">取消済</span><span class="sxs-lookup"><span data-stu-id="8576c-268">Canceled</span></span> 

## <a name="import-and-export-processes"></a><span data-ttu-id="8576c-269">プロセスのインポートとエクスポート</span><span class="sxs-lookup"><span data-stu-id="8576c-269">Import and export processes</span></span> 
<span data-ttu-id="8576c-270">次の図は、データ管理パッケージ メソッドを使用してデータ パッケージをインポートする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8576c-270">The following illustration shows how the data management package methods can be used to import data packages.</span></span>

![データ管理パッケージ メソッドを使用するデータ パッケージ ファイルのインポート](./media/data-package-import.png)
 
<span data-ttu-id="8576c-272">次の図は、データ管理パッケージ メソッドを使用してデータ パッケージをエクスポートする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8576c-272">The following illustration shows how the data management package methods can be used to export data packages.</span></span>

![管理パッケージ メソッドを使用するデータ パッケージ ファイルのエクスポート](./media/data-package-export.png)
 
<span data-ttu-id="8576c-274">サンプル コンソール アプリケーションは、データのインポートとデータのエクスポートのメソッドを紹介する GitHub から入手できます。</span><span class="sxs-lookup"><span data-stu-id="8576c-274">A sample console application is available on GitHub to showcase the data import and data export methods.</span></span> <span data-ttu-id="8576c-275">詳細については、「<https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/FileBasedIntegrationSamples/ConsoleAppSamples>」に移動してください。</span><span class="sxs-lookup"><span data-stu-id="8576c-275">For more information, go to <https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/FileBasedIntegrationSamples/ConsoleAppSamples>.</span></span>
