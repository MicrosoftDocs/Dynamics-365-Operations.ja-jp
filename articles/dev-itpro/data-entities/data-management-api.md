---
title: "データ管理パッケージ REST API"
description: "このトピックでは、データ管理フレームワークのパッケージ REST API について説明します。"
author: Sunil-Garg
ms.date: 08/31/2018
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
ms.sourcegitcommit: 96a9075294c1f2a9cfde03be1aaaa26af90de4c2
ms.openlocfilehash: e714ea9e80acd09f58b2a0a0f9579aed2f8fbcbc
ms.contentlocale: ja-jp
ms.lasthandoff: 09/04/2018

---

# <a name="data-management-package-rest-api"></a><span data-ttu-id="b0a6f-103">データ管理パッケージ REST API</span><span class="sxs-lookup"><span data-stu-id="b0a6f-103">Data management package REST API</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0a6f-104">このトピックでは、データ管理フレームワークのパッケージ表現型状態移行 (REST) のアプリケーション プログラミング インターフェイス (API) について説明します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-104">This topic describes the data management framework's package representational state transfer (REST) application programming interface (API).</span></span> <span data-ttu-id="b0a6f-105">パッケージ API を使用すると、データ パッケージを使用して、Microsoft Dynamics 365 for Finance and Operations と統合することができます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-105">The package API lets you integrate with Microsoft Dynamics 365 for Finance and Operations, by using data packages.</span></span> <span data-ttu-id="b0a6f-106">REST API は、クラウドおよびオンプレミス展開の両方で使用できます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-106">The REST API can be used with both cloud and on-premises deployments.</span></span> <span data-ttu-id="b0a6f-107">オンプレミス配置については、現在この機能はバージョン 7.2、プラットフォーム更新プログラム 12、ビルド 7.0.4709.41184 以降で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-107">For on-premises deployments this functionality is currently available for version 7.2, Platform update 12, build 7.0.4709.41184, and later.</span></span>

<span data-ttu-id="b0a6f-108">オンプレミス サポートは追加されましたが、API の名前は変更されていないため、クラウドおよびオンプレミスの両方の展開は単一の API 設定で保持できます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-108">Although on-premises support has been added, API names have not been changed, so that we can keep a single API set for both cloud and on-premises deployments.</span></span>

## <a name="choosing-an-integration-api"></a><span data-ttu-id="b0a6f-109">統合 API の選択</span><span class="sxs-lookup"><span data-stu-id="b0a6f-109">Choosing an integration API</span></span>
<span data-ttu-id="b0a6f-110">Finance and Operations の 2 つの API は、データ管理フレームワークのパッケージ API と定期的な統合 API というファイル ベースの統合シナリオをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-110">Two APIs in Finance and Operations support file-based integration scenarios: the data management framework's package API and the recurring integrations API.</span></span> <span data-ttu-id="b0a6f-111">どちらの API もデータ インポート シナリオとデータ エクスポート シナリオの両方をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-111">Both APIs support both data import scenarios and data export scenarios.</span></span> <span data-ttu-id="b0a6f-112">次のテーブルでは、使用する API を決定する際に考慮する必要がある主な決定事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-112">The following table describes the main decision points that you should consider when you're trying to decide which API to use.</span></span>

| <span data-ttu-id="b0a6f-113">決定ポイント</span><span class="sxs-lookup"><span data-stu-id="b0a6f-113">Decision point</span></span>      | <span data-ttu-id="b0a6f-114">定期統合 API</span><span class="sxs-lookup"><span data-stu-id="b0a6f-114">Recurring integrations API</span></span> | <span data-ttu-id="b0a6f-115">データ管理フレームワークのパッケージ API</span><span class="sxs-lookup"><span data-stu-id="b0a6f-115">Data management framework's package API</span></span> |
|---------------------|--------------------------------------|-----------------------------|
| <span data-ttu-id="b0a6f-116">スケジューリング</span><span class="sxs-lookup"><span data-stu-id="b0a6f-116">Scheduling</span></span>          | <span data-ttu-id="b0a6f-117">Finance and Operations のスケジュール設定</span><span class="sxs-lookup"><span data-stu-id="b0a6f-117">Scheduling in Finance and Operations</span></span> | <span data-ttu-id="b0a6f-118">Finance and Operations 外でのスケジュール設定</span><span class="sxs-lookup"><span data-stu-id="b0a6f-118">Scheduling outside Finance and Operations</span></span> |
| <span data-ttu-id="b0a6f-119">書式設定</span><span class="sxs-lookup"><span data-stu-id="b0a6f-119">Format</span></span>              | <span data-ttu-id="b0a6f-120">ファイルおよびデータ パッケージ</span><span class="sxs-lookup"><span data-stu-id="b0a6f-120">Files and data packages</span></span> | <span data-ttu-id="b0a6f-121">データ パッケージのみ</span><span class="sxs-lookup"><span data-stu-id="b0a6f-121">Only data packages</span></span> |
| <span data-ttu-id="b0a6f-122">変換</span><span class="sxs-lookup"><span data-stu-id="b0a6f-122">Transformation</span></span>      | <span data-ttu-id="b0a6f-123">データ ファイルが XML 形式の場合の Extensible Stylesheet Language Transformations (XSLT) のサポート</span><span class="sxs-lookup"><span data-stu-id="b0a6f-123">Support for Extensible Stylesheet Language Transformations (XSLT) if the data file is in XML format</span></span> | <span data-ttu-id="b0a6f-124">システム外部での変換</span><span class="sxs-lookup"><span data-stu-id="b0a6f-124">Transformations that are external to the system</span></span> |
| <span data-ttu-id="b0a6f-125">サポートされているプロトコル</span><span class="sxs-lookup"><span data-stu-id="b0a6f-125">Supported protocols</span></span> | <span data-ttu-id="b0a6f-126">SOAP および REST</span><span class="sxs-lookup"><span data-stu-id="b0a6f-126">SOAP and REST</span></span> | <span data-ttu-id="b0a6f-127">REST</span><span class="sxs-lookup"><span data-stu-id="b0a6f-127">REST</span></span> |
| <span data-ttu-id="b0a6f-128">サービス タイプ</span><span class="sxs-lookup"><span data-stu-id="b0a6f-128">Service type</span></span>        | <span data-ttu-id="b0a6f-129">顧客サービス</span><span class="sxs-lookup"><span data-stu-id="b0a6f-129">Custom service</span></span> | <span data-ttu-id="b0a6f-130">データ プロトコル (OData) アクションを開きます</span><span class="sxs-lookup"><span data-stu-id="b0a6f-130">Open Data Protocol (OData) action</span></span> |
| <span data-ttu-id="b0a6f-131">適用の対象</span><span class="sxs-lookup"><span data-stu-id="b0a6f-131">Availability</span></span>        | <span data-ttu-id="b0a6f-132">2016 年 2 月リリース (RTW) 以降</span><span class="sxs-lookup"><span data-stu-id="b0a6f-132">February 2016 release (RTW) and later</span></span> | <span data-ttu-id="b0a6f-133">プラットフォーム更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="b0a6f-133">Platform update 5 and later</span></span> |

<span data-ttu-id="b0a6f-134">定期的な統合 API がデータ管理のフレームワーク パッケージ API の要件を満たしている場合、「[定期統合](recurring-integrations.md)」を参照します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-134">If you decide that the recurring integrations API meets your requirement better than the data management framework's package API, see [Recurring integrations](recurring-integrations.md).</span></span> <span data-ttu-id="b0a6f-135">このトピックの残りの部分では、データ管理フレームワークのパッケージ API について説明します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-135">The rest of this topic discusses the data management framework's package API.</span></span>

## <a name="authorization"></a><span data-ttu-id="b0a6f-136">認証</span><span class="sxs-lookup"><span data-stu-id="b0a6f-136">Authorization</span></span>
<span data-ttu-id="b0a6f-137">データ管理フレームワークのパッケージ API は、アクセスを認可するために OAuth 2.0 を使用します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-137">The data management framework's package API uses OAuth 2.0 for authorizing access.</span></span> <span data-ttu-id="b0a6f-138">API は、有効な OAuth アクセス トークンを使用して呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-138">The API must be called by using a valid OAuth access token.</span></span> <span data-ttu-id="b0a6f-139">OAuth 2.0 および Microsoft Azure Active Directory (Azure AD) に関する詳細については、[OAuth 2.0 および Azure Active Directory を使用してWeb アプリケーションへのアクセスを承認する](/azure/active-directory/develop/active-directory-protocols-oauth-code) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-139">For more details about OAuth 2.0 and Microsoft Azure Active Directory (Azure AD), see [Authorize access to web applications using OAuth 2.0 and Azure Active Directory](/azure/active-directory/develop/active-directory-protocols-oauth-code).</span></span> <span data-ttu-id="b0a6f-140">オンプレミス配置については、Active Directory フェデレーション サービス (AD FS) が認証に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-140">For on-premises deployments, Active Directory Federation Services (AD FS) will be used for authorization.</span></span>

> [!NOTE]
> <span data-ttu-id="b0a6f-141">クライアント資格情報の付与フローを使用すると、Finance and Operations はアクセス制御リストを保持します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-141">When you use the Client Credentials Grant flow, Finance and Operations maintains an access control list.</span></span> <span data-ttu-id="b0a6f-142">アクセス制御リストは **システム管理** \> **設定** \> **Azure Active Directory アプリケーション** で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-142">You can find the access control list at **System administration** \> **Setup** \> **Azure Active Directory applications**.</span></span> <span data-ttu-id="b0a6f-143">**Azure Active Directory アプリケーション** ページには、承認済クライアント ID と、クライアント資格情報付与フローを使用して API が呼び出されたときに適用する必要があるユーザー セキュリティ マッピングが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-143">The **Azure Active Directory applications** page shows the approved client IDs and the user security mapping that should be enforced when the API is called by using the Client Credentials Grant flow.</span></span>
>
> <span data-ttu-id="b0a6f-144">オンプレミス配置については、このリストには AD FS からの有効なクライアント ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-144">For on-premises deployments, this list must have a valid client ID from AD FS.</span></span> <span data-ttu-id="b0a6f-145">また、オンプレミス用途では、Dynamics 365 for Finance and Operations に接続するとき、次の例の <baseurl> に /namespaces/AXSF を付加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-145">Also, for on-premise use, the <baseurl> in the following examples must also append /namespaces/AXSF when connecting to Dynamics 365 for Finance and Operations.</span></span>


## <a name="import-apis"></a><span data-ttu-id="b0a6f-146">API のインポート</span><span class="sxs-lookup"><span data-stu-id="b0a6f-146">Import APIs</span></span>
<span data-ttu-id="b0a6f-147">ファイル (データ パッケージ) のインポートには、次の API が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-147">The following APIs are used to do file (data package) imports.</span></span>

### <a name="getazurewritableurl"></a><span data-ttu-id="b0a6f-148">GetAzureWritableUrl</span><span class="sxs-lookup"><span data-stu-id="b0a6f-148">GetAzureWritableUrl</span></span>
<span data-ttu-id="b0a6f-149">**GetAzureWritableUrl** API は、書き込み可能な Blob URL を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-149">The **GetAzureWritableUrl** API is used to get a writable blob URL.</span></span> <span data-ttu-id="b0a6f-150">このメソッドには、URL に埋め込まれた共有アクセス署名 (SAS) トークンが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-150">This method includes a shared access signature (SAS) token that is embedded in the URL.</span></span> <span data-ttu-id="b0a6f-151">この方法を使用すると、Finance and Operations の Azure Blob Storage コンテナーにデータ パッケージをアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-151">You can use this method to upload a data package to the Azure Blob storage container for Finance and Operations.</span></span> <span data-ttu-id="b0a6f-152">オンプレミス配置については、この API はローカル ストレージに取り除かれた URL を引き続き返します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-152">For on-premises deployments, this API will still return the URL which has been abstracted to local storage.</span></span>

> [!NOTE]
> <span data-ttu-id="b0a6f-153">SAS は有効期限の時間枠中にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-153">An SAS is valid only during an expiry time window.</span></span> <span data-ttu-id="b0a6f-154">ウィンドウが経過した後に発行されるすべての要求はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-154">Any request that is issued after the window has passed returns an error.</span></span> <span data-ttu-id="b0a6f-155">詳細については、[共有アクセス署名 (SA) の使用](/azure/storage/common/storage-dotnet-shared-access-signature-part-1) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-155">For more information, see [Using shared access signatures (SAS)](/azure/storage/common/storage-dotnet-shared-access-signature-part-1).</span></span>

```CSharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetAzureWriteUrl
BODY
{
    "uniqueFileName":"<string>",
}
```

<span data-ttu-id="b0a6f-156">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-156">Here is an example of a successful response.</span></span>

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

<span data-ttu-id="b0a6f-157">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="b0a6f-157">**Input parameters**</span></span>

| <span data-ttu-id="b0a6f-158">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b0a6f-158">Parameter</span></span>         | <span data-ttu-id="b0a6f-159">説明</span><span class="sxs-lookup"><span data-stu-id="b0a6f-159">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="b0a6f-160">string packageUrl</span><span class="sxs-lookup"><span data-stu-id="b0a6f-160">string packageUrl</span></span> | <span data-ttu-id="b0a6f-161">BLOB ID を追跡するために使用される一意のファイル名。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-161">A unique file name that is used to track blob IDs.</span></span> <span data-ttu-id="b0a6f-162">一意のファイル名であることを保証するため、グローバル一意識別子 (GUID) を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-162">You can include a globally unique identifier (GUID) to help guarantee a unique file name.</span></span> |

<span data-ttu-id="b0a6f-163">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="b0a6f-163">**Output parameters**</span></span>

| <span data-ttu-id="b0a6f-164">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b0a6f-164">Parameter</span></span>      | <span data-ttu-id="b0a6f-165">説明</span><span class="sxs-lookup"><span data-stu-id="b0a6f-165">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="b0a6f-166">string BlobId</span><span class="sxs-lookup"><span data-stu-id="b0a6f-166">string BlobId</span></span>  | <span data-ttu-id="b0a6f-167">割り当てられた BLOB コンテナーの BLOB ID。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-167">The blob ID of the allocated blob container.</span></span> |
| <span data-ttu-id="b0a6f-168">string BlobUrl</span><span class="sxs-lookup"><span data-stu-id="b0a6f-168">string BlobUrl</span></span> | <span data-ttu-id="b0a6f-169">埋め込まれた SAS トークンを持つ URL。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-169">A URL with an embedded SAS token.</span></span> <span data-ttu-id="b0a6f-170">URL を使用 して BLOB ストレージに書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-170">The URL can be used to write to blob storage.</span></span> |

### <a name="importfrompackage"></a><span data-ttu-id="b0a6f-171">ImportFromPackage</span><span class="sxs-lookup"><span data-stu-id="b0a6f-171">ImportFromPackage</span></span>
<span data-ttu-id="b0a6f-172">**ImportFromPackage** API は、Finance and Operations の実装に関連付けられている Azure Blob Storage にアップロードされるデータ パッケージからインポートを開始するために使用します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-172">The **ImportFromPackage** API is used to initiate an import from the data package that is uploaded to the Azure Blob storage that is associated with your implementation of Finance and Operations.</span></span> <span data-ttu-id="b0a6f-173">オンプレミス配置については、ファイルが以前にアップロードされたローカル ストレージから、インポートが開始されます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-173">For on-premises deployments, the import will be initiated from the local storage to which the file was uploaded previously.</span></span>

> [!NOTE]
> <span data-ttu-id="b0a6f-174">プラットフォーム更新プログラム 12 を開始すると、ImportFromPackage は複合エンティティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-174">Starting platform update 12, ImportFromPackage will support composite entity.</span></span> <span data-ttu-id="b0a6f-175">ただし、パッケージで 1 つの複合エンティティのみを持つという制限があります。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-175">However, the limitation is to have only one composite entity in a package.</span></span>

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

<span data-ttu-id="b0a6f-176">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-176">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"<executionId>"
    }
}
```

<span data-ttu-id="b0a6f-177">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="b0a6f-177">**Input parameters**</span></span>

| <span data-ttu-id="b0a6f-178">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b0a6f-178">Parameter</span></span>                | <span data-ttu-id="b0a6f-179">説明</span><span class="sxs-lookup"><span data-stu-id="b0a6f-179">Description</span></span> |
|--------------------------|-------------|
| <span data-ttu-id="b0a6f-180">string packageUrl</span><span class="sxs-lookup"><span data-stu-id="b0a6f-180">string packageUrl</span></span>        | <span data-ttu-id="b0a6f-181">Finance and Operations に関連付けられている Azure BLOB Storage 内のデータ パッケージの URL。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-181">The URL of the data package in the Azure Blob storage that is associated with Finance and Operations.</span></span> |
| <span data-ttu-id="b0a6f-182">string definitionGroupId</span><span class="sxs-lookup"><span data-stu-id="b0a6f-182">string definitionGroupId</span></span> | <span data-ttu-id="b0a6f-183">インポート用のデータ プロジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-183">The name of the data project for import.</span></span> |
| <span data-ttu-id="b0a6f-184">string executionId</span><span class="sxs-lookup"><span data-stu-id="b0a6f-184">string executionId</span></span>       | <span data-ttu-id="b0a6f-185">ジョブに使用する ID。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-185">The ID to use for the job.</span></span> <span data-ttu-id="b0a6f-186">空の ID が割り当てられている場合は、新しい実行 ID が作成されます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-186">If an empty ID is assigned, a new execution ID will be created.</span></span> |
| <span data-ttu-id="b0a6f-187">bool execute</span><span class="sxs-lookup"><span data-stu-id="b0a6f-187">bool execute</span></span>             | <span data-ttu-id="b0a6f-188">このパラメーターを **True** に設定して対象の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-188">Set this parameter to **True** to run the target step.</span></span> <span data-ttu-id="b0a6f-189">それ以外の場合、**False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-189">Otherwise, set it to **False**.</span></span> |
| <span data-ttu-id="b0a6f-190">bool overwrite</span><span class="sxs-lookup"><span data-stu-id="b0a6f-190">bool overwrite</span></span>           | <span data-ttu-id="b0a6f-191">パッケージ内で複合エンティティを使用する場合は、常に **False** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-191">This must always be set to **False** when using a composite entity in a package.</span></span> <span data-ttu-id="b0a6f-192">それ以外の場合、**True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-192">Otherwise, set it to **True**</span></span> |
| <span data-ttu-id="b0a6f-193">string legalEntityId</span><span class="sxs-lookup"><span data-stu-id="b0a6f-193">string legalEntityId</span></span>     | <span data-ttu-id="b0a6f-194">データ インポートの法人。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-194">The legal entity for the data import.</span></span> |

<span data-ttu-id="b0a6f-195">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="b0a6f-195">**Output parameters**</span></span>

| <span data-ttu-id="b0a6f-196">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b0a6f-196">Parameter</span></span>          | <span data-ttu-id="b0a6f-197">説明</span><span class="sxs-lookup"><span data-stu-id="b0a6f-197">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="b0a6f-198">string executionId</span><span class="sxs-lookup"><span data-stu-id="b0a6f-198">string executionId</span></span> | <span data-ttu-id="b0a6f-199">データ インポートの実行 ID。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-199">The execution ID of the data import.</span></span> |

> [!NOTE]
> <span data-ttu-id="b0a6f-200">ImportFromPacakge() はバッチを使用してインポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-200">ImportFromPacakge() uses a batch to perform the import.</span></span> <span data-ttu-id="b0a6f-201">つまり、並行インポートを実行するためにデータ管理で並列処理ルールを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-201">This means that parallel processing rules in data management must be used to perform parallel imports.</span></span> <span data-ttu-id="b0a6f-202">ImportFromPackage() は、エラーになるため並列スレッドで呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-202">ImportFromPackage() must not be called in parallel threads, as this will result in failure.</span></span> 

## <a name="export-apis"></a><span data-ttu-id="b0a6f-203">API をエキスポート</span><span class="sxs-lookup"><span data-stu-id="b0a6f-203">Export APIs</span></span>
<span data-ttu-id="b0a6f-204">ファイル (データ パッケージ) のエクスポートには、次の API が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-204">The following APIs are used to do file (data package) exports.</span></span>

### <a name="exporttopackage"></a><span data-ttu-id="b0a6f-205">ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="b0a6f-205">ExportToPackage</span></span>
<span data-ttu-id="b0a6f-206">**ExportToPackage** API は、データ パッケージのエクスポートを開始するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-206">The **ExportToPackage** API is used to initiate an export of a data package.</span></span> <span data-ttu-id="b0a6f-207">これは、クラウドとオンプレミスの両方の展開に適用されます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-207">This is applicable to both cloud and on-premises deployments.</span></span>

- <span data-ttu-id="b0a6f-208">この API を呼び出す前に、エクスポート データ プロジェクトを Finance and Operations で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-208">The export data project must be created in Finance and Operations before you call this API.</span></span> <span data-ttu-id="b0a6f-209">プロジェクトが存在しない場合、API の呼び出しには、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-209">If the project doesn't exist, a call to the API returns an error.</span></span>
- <span data-ttu-id="b0a6f-210">変更履歴がオンの場合は、最後の実行後に更新または作成されたレコードのみがエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-210">If change tracking has been turned on, only records that have been created or updated since the last run are exported.</span></span> <span data-ttu-id="b0a6f-211">(つまり、デルタのみが返されます。)</span><span class="sxs-lookup"><span data-stu-id="b0a6f-211">(In other words, only the delta is returned.)</span></span>

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

<span data-ttu-id="b0a6f-212">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-212">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"<executionId>"
    }
}
```

<span data-ttu-id="b0a6f-213">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="b0a6f-213">**Input parameters**</span></span>

| <span data-ttu-id="b0a6f-214">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b0a6f-214">Parameter</span></span>                | <span data-ttu-id="b0a6f-215">説明</span><span class="sxs-lookup"><span data-stu-id="b0a6f-215">Description</span></span> |
|--------------------------|-------------|
| <span data-ttu-id="b0a6f-216">string definitionGroupId</span><span class="sxs-lookup"><span data-stu-id="b0a6f-216">string definitionGroupId</span></span> | <span data-ttu-id="b0a6f-217">エクスポート用のデータ プロジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-217">The name of the data project for export.</span></span> |
| <span data-ttu-id="b0a6f-218">string packageName</span><span class="sxs-lookup"><span data-stu-id="b0a6f-218">string packageName</span></span>       | <span data-ttu-id="b0a6f-219">エクスポートされたデータ パッケージの名前。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-219">The name of the exported data package.</span></span> |
| <span data-ttu-id="b0a6f-220">string executionId</span><span class="sxs-lookup"><span data-stu-id="b0a6f-220">string executionId</span></span>       | <span data-ttu-id="b0a6f-221">ジョブに使用する ID。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-221">The ID to use for the job.</span></span> <span data-ttu-id="b0a6f-222">空の ID が割り当てられている場合は、新しい実行 ID が作成されます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-222">If an empty ID is assigned, a new execution ID will be created.</span></span> |
| <span data-ttu-id="b0a6f-223">bool reExecute</span><span class="sxs-lookup"><span data-stu-id="b0a6f-223">bool reExecute</span></span>           | <span data-ttu-id="b0a6f-224">このパラメーターを **True** に設定して対象の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-224">Set this parameter to **True** to run the target step.</span></span> <span data-ttu-id="b0a6f-225">それ以外の場合、**False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-225">Otherwise, set it to **False**.</span></span> |
| <span data-ttu-id="b0a6f-226">string legalEntityId</span><span class="sxs-lookup"><span data-stu-id="b0a6f-226">string legalEntityId</span></span>     | <span data-ttu-id="b0a6f-227">データ インポートの法人。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-227">The legal entity for the data import.</span></span> |
    
<span data-ttu-id="b0a6f-228">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="b0a6f-228">**Output parameters**</span></span>

| <span data-ttu-id="b0a6f-229">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b0a6f-229">Parameter</span></span>          | <span data-ttu-id="b0a6f-230">説明</span><span class="sxs-lookup"><span data-stu-id="b0a6f-230">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="b0a6f-231">string executionId</span><span class="sxs-lookup"><span data-stu-id="b0a6f-231">string executionId</span></span> | <span data-ttu-id="b0a6f-232">データ エクスポートの実行 ID。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-232">The execution ID of the data export.</span></span> |

### <a name="getexportedpackageurl"></a><span data-ttu-id="b0a6f-233">GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="b0a6f-233">GetExportedPackageUrl</span></span>
<span data-ttu-id="b0a6f-234">**GetExportedPackageUrl** API は、**ExportToPackage** を呼び出すことでエクスポートされたデータ パッケージの URL を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-234">The **GetExportedPackageUrl** API is used to get the URL of the data package that was exported by a call to **ExportToPackage**.</span></span> <span data-ttu-id="b0a6f-235">これは、クラウドとオンプレミスの両方の展開に適用されます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-235">This is applicable to both cloud and on-premises deployments.</span></span>

```CSharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
BODY
{"executionId":"<Execution Id>"}
```

<span data-ttu-id="b0a6f-236">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-236">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"https://<baseurl_id>.blob.core.windows.net/dmf/<uniqueFileName>?<SAS Token>"
    }
}
```

<span data-ttu-id="b0a6f-237">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="b0a6f-237">**Input parameters**</span></span>

| <span data-ttu-id="b0a6f-238">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b0a6f-238">Parameter</span></span>          | <span data-ttu-id="b0a6f-239">説明</span><span class="sxs-lookup"><span data-stu-id="b0a6f-239">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="b0a6f-240">string executionId</span><span class="sxs-lookup"><span data-stu-id="b0a6f-240">string executionId</span></span> | <span data-ttu-id="b0a6f-241">データ プロジェクト実行の実行 ID。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-241">The execution ID of the data project run.</span></span> |

<span data-ttu-id="b0a6f-242">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="b0a6f-242">**Output parameters**</span></span>

| <span data-ttu-id="b0a6f-243">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b0a6f-243">Parameter</span></span>      | <span data-ttu-id="b0a6f-244">説明</span><span class="sxs-lookup"><span data-stu-id="b0a6f-244">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="b0a6f-245">string BlobUrl</span><span class="sxs-lookup"><span data-stu-id="b0a6f-245">string BlobUrl</span></span> | <span data-ttu-id="b0a6f-246">埋め込みの SAS トークンを持つ blob URL。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-246">A blob URL that has an embedded SAS token.</span></span> <span data-ttu-id="b0a6f-247">URL を使用して、エクスポートしたデータ パッケージをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-247">The URL can be used to download the exported data package.</span></span> |

## <a name="status-check-api"></a><span data-ttu-id="b0a6f-248">ステータス チェック API</span><span class="sxs-lookup"><span data-stu-id="b0a6f-248">Status check API</span></span> 
<span data-ttu-id="b0a6f-249">状態を確認するには、次の API を使用します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-249">The following APIs are used to check status.</span></span> <span data-ttu-id="b0a6f-250">これらは、インポート フローとエクスポート フローの両方で使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-250">They are used during both import flows and export flows.</span></span>

### <a name="getexecutionsummarystatus"></a><span data-ttu-id="b0a6f-251">GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="b0a6f-251">GetExecutionSummaryStatus</span></span>
<span data-ttu-id="b0a6f-252">**GetExecutionSummaryStatus** API は、データ プロジェクト実行ジョブのステータスを確認するためにインポート ジョブおよびエクスポート ジョブの両方に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-252">The **GetExecutionSummaryStatus** API is used for both import jobs and export jobs to check the status of a data project execution job.</span></span> <span data-ttu-id="b0a6f-253">これは、クラウドとオンプレミスの両方の展開に適用されます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-253">This is applicable to both cloud and on-premises deployments.</span></span>

```CSharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
BODY
{"executionId":"<executionId>"}
```

<span data-ttu-id="b0a6f-254">成功した応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-254">Here is an example of a successful response.</span></span>

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"<executionStatus>"
    }
}
```

<span data-ttu-id="b0a6f-255">**入力パラメーター**</span><span class="sxs-lookup"><span data-stu-id="b0a6f-255">**Input parameters**</span></span>

| <span data-ttu-id="b0a6f-256">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b0a6f-256">Parameter</span></span>          | <span data-ttu-id="b0a6f-257">説明</span><span class="sxs-lookup"><span data-stu-id="b0a6f-257">Description</span></span> |
|--------------------|-------------|
| <span data-ttu-id="b0a6f-258">string executionId</span><span class="sxs-lookup"><span data-stu-id="b0a6f-258">string executionId</span></span> | <span data-ttu-id="b0a6f-259">データ プロジェクト実行の実行 ID。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-259">The execution ID of the data project run.</span></span> |

<span data-ttu-id="b0a6f-260">**出力パラメータ**</span><span class="sxs-lookup"><span data-stu-id="b0a6f-260">**Output parameters**</span></span>

| <span data-ttu-id="b0a6f-261">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b0a6f-261">Parameter</span></span>                                 | <span data-ttu-id="b0a6f-262">説明</span><span class="sxs-lookup"><span data-stu-id="b0a6f-262">Description</span></span> |
|-------------------------------------------|-------------|
| <span data-ttu-id="b0a6f-263">DMFExecutionSummaryStatus executionStatus</span><span class="sxs-lookup"><span data-stu-id="b0a6f-263">DMFExecutionSummaryStatus executionStatus</span></span> | <span data-ttu-id="b0a6f-264">実行のステータス。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-264">The execution status.</span></span> |

<span data-ttu-id="b0a6f-265">実行状態の使用可能な値を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-265">Here are the possible values for the execution status:</span></span>

- <span data-ttu-id="b0a6f-266">不明</span><span class="sxs-lookup"><span data-stu-id="b0a6f-266">Unknown</span></span>
- <span data-ttu-id="b0a6f-267">NotRun</span><span class="sxs-lookup"><span data-stu-id="b0a6f-267">NotRun</span></span>
- <span data-ttu-id="b0a6f-268">実行</span><span class="sxs-lookup"><span data-stu-id="b0a6f-268">Executing</span></span>
- <span data-ttu-id="b0a6f-269">成功</span><span class="sxs-lookup"><span data-stu-id="b0a6f-269">Succeeded</span></span>
- <span data-ttu-id="b0a6f-270">PartiallySucceeded</span><span class="sxs-lookup"><span data-stu-id="b0a6f-270">PartiallySucceeded</span></span>
- <span data-ttu-id="b0a6f-271">失敗</span><span class="sxs-lookup"><span data-stu-id="b0a6f-271">Failed</span></span>
- <span data-ttu-id="b0a6f-272">取消済</span><span class="sxs-lookup"><span data-stu-id="b0a6f-272">Canceled</span></span>

> [!NOTE]
> <span data-ttu-id="b0a6f-273">BLOB ストレージ内のファイルは、ストレージに 7 日間残ります。その後、自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-273">The file in the blob storage will remain in the storage for seven days, after which it will be automatically deleted.</span></span>

## <a name="import-and-export-processes"></a><span data-ttu-id="b0a6f-274">プロセスのインポートとエクスポート</span><span class="sxs-lookup"><span data-stu-id="b0a6f-274">Import and export processes</span></span> 
<span data-ttu-id="b0a6f-275">次の図は、データ管理パッケージ メソッドを使用してデータ パッケージをインポートする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-275">The following illustration shows how the data management package methods can be used to import data packages.</span></span>

![データ管理パッケージ メソッドを使用するデータ パッケージ ファイルのインポート](./media/data-package-import.png)

<span data-ttu-id="b0a6f-277">次の図は、データ管理パッケージ メソッドを使用してデータ パッケージをエクスポートする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-277">The following illustration shows how the data management package methods can be used to export data packages.</span></span>

![管理パッケージ メソッドを使用するデータ パッケージ ファイルのエクスポート](./media/data-package-export.png)

<span data-ttu-id="b0a6f-279">サンプル コンソール アプリケーションは、データのインポートとデータのエクスポートのメソッドを紹介する GitHub から入手できます。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-279">A sample console application is available on GitHub to showcase the data import and data export methods.</span></span> <span data-ttu-id="b0a6f-280">詳細については、「<https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/FileBasedIntegrationSamples/ConsoleAppSamples>」に移動してください。</span><span class="sxs-lookup"><span data-stu-id="b0a6f-280">For more information, go to <https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/FileBasedIntegrationSamples/ConsoleAppSamples>.</span></span>

