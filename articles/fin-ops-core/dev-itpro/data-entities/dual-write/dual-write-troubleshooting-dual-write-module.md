---
title: Finance and Operations アプリのデュアル書き込みモジュールに関する問題のトラブルシューティング
description: このトピックでは、アプリの Finance and Operations デュアル書き込みモジュールの問題修正に役立つトラブルシューティング情報を提供します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f99f3760e75ec1bbf2ccdea497cf2eec3e28e233
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997377"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="120e4-103">Finance and Operations アプリのデュアル書き込みモジュールに関する問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="120e4-103">Troubleshoot issues with the dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="120e4-104">このトピックでは、Finance and Operations アプリと Common Data Service 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="120e4-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="120e4-105">このトピックでは、Finance and Operations アプリの **デュアル書き込み** モジュールの問題修正に特化したトラブルシューティング情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="120e4-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="120e4-106">このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="120e4-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="120e4-107">各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。</span><span class="sxs-lookup"><span data-stu-id="120e4-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="120e4-108">Finance and Operations アプリでデュアル書き込みのモジュールを読み込むことができない</span><span class="sxs-lookup"><span data-stu-id="120e4-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="120e4-109">**データ管理** ワークスペースで **デュアル書き込み** タイルを選択しても **デュアル書き込み** のページを開くことができない場合は、データ統合サービスがダウンしている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="120e4-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="120e4-110">サポートチケットを作成して、データ統合サービスの再起動を要求してください。</span><span class="sxs-lookup"><span data-stu-id="120e4-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-map"></a><span data-ttu-id="120e4-111">新規エンティティのマッピングを作成しようとするとエラーが発生する</span><span class="sxs-lookup"><span data-stu-id="120e4-111">Error when you try to create a new entity map</span></span>

<span data-ttu-id="120e4-112">**問題の修正に必要な資格情報：** デュアル書き込みを設定したのと同じユーザー。</span><span class="sxs-lookup"><span data-stu-id="120e4-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="120e4-113">新しいエンティティをデュアル書き込みで構成する場合に、次のエラーメッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="120e4-113">You might receive the following error message when you try to configure a new entity for dual-write.</span></span> <span data-ttu-id="120e4-114">マッピングを作成できるのは、デュアル書き込み接続を設定したユーザーだけです。</span><span class="sxs-lookup"><span data-stu-id="120e4-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="120e4-115">*応答状態コードが成功とならない: 401 (権限なし)*</span><span class="sxs-lookup"><span data-stu-id="120e4-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="120e4-116">デュアル書き込みのユーザー インターフェイスを開くとエラーが発生する</span><span class="sxs-lookup"><span data-stu-id="120e4-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="120e4-117">**データ管理** ワークスペースからデュアル書き込みにアクセスすると、次のエラーメッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="120e4-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="120e4-118">*login.microsoftonline.com が接続を拒否しました。*</span><span class="sxs-lookup"><span data-stu-id="120e4-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="120e4-119">この問題を修正するには、Microsoft Edge の InPrivate を使用してサインインするか、Chromium の incognito ウィンドウを使用するか、Google Chrome のincognitoウィンドウを使用してください。</span><span class="sxs-lookup"><span data-stu-id="120e4-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="120e4-120">また、サードパーティの cookie のブロックを解除、クリアする必要があります。</span><span class="sxs-lookup"><span data-stu-id="120e4-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="120e4-121">環境をデュアル書き込みにリンクする際、または新しいエンティティのマッピングを追加する際にエラーが発生する</span><span class="sxs-lookup"><span data-stu-id="120e4-121">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="120e4-122">**問題の修正に必要なロール:** Finance and Operations アプリと Common Data Service 両方のシステム管理者権限。</span><span class="sxs-lookup"><span data-stu-id="120e4-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="120e4-123">マッピングをリンクまたは作成する際に、次のエラーが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="120e4-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="120e4-124">*応答状態コードが成功とならない: 403 (tokenexchange)。<br> セッション ID: \<your session id\><br> ルート アクティビティ ID: \<your root activity id\>*</span><span class="sxs-lookup"><span data-stu-id="120e4-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="120e4-125">このエラーは、デュアル書き込みへのリンクと、マッピングを作成する十分なアクセス権限がない場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="120e4-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="120e4-126">このエラーは、リンク解除によるデュアル書き込みを行わずに Common Data Service 環境をリセットした場合にも発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="120e4-126">This error can also occur if the Common Data Service environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="120e4-127">Finance and Operations アプリと Common Data Service の両方でシステム管理者ロールを持つすべてのユーザーが、環境をリンクできます。</span><span class="sxs-lookup"><span data-stu-id="120e4-127">Any user with system administrator role in both Finance and Operations apps and Common Data Service can link the environments.</span></span> <span data-ttu-id="120e4-128">デュアル書き込み接続を設定したユーザーだけが、新しいエンティティのマッピングを追加できます。</span><span class="sxs-lookup"><span data-stu-id="120e4-128">Only the user who setup the dual-write connection can add new entity maps.</span></span> <span data-ttu-id="120e4-129">設定後、システム管理者のロールを持つユーザーはステータスを監視し、マッピングを編集できます。</span><span class="sxs-lookup"><span data-stu-id="120e4-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="120e4-130">エンティティ マッピングを停止した際のエラー</span><span class="sxs-lookup"><span data-stu-id="120e4-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="120e4-131">エンティティのマッピングを停止した際に、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="120e4-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="120e4-132">*\[禁止されています\]、\[{状態: 403、"ソース": ""、"メッセージ": "トークン変換エラー: ユーザーに dynamicscrmonline/xxxxxx-xxxx-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx への接続許可がありません"}\]、リモート サーバーがエラーを返しました：(403) 許可されていません。*</span><span class="sxs-lookup"><span data-stu-id="120e4-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="120e4-133">このエラーは、リンクされた Common Data Service 環境が使用できない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="120e4-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="120e4-134">この問題を修正するには、チケットを作成してデータ統合チームに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="120e4-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="120e4-135">データ統合チームがマッピンがバックエンドで **実行されていない** ことを識別できるように、ネットワークのトレースを添付してください。</span><span class="sxs-lookup"><span data-stu-id="120e4-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-an-entity-mapping"></a><span data-ttu-id="120e4-136">エンティティ マッピングの開始中にエラーが発生する</span><span class="sxs-lookup"><span data-stu-id="120e4-136">Error while trying to start an entity mapping</span></span>

<span data-ttu-id="120e4-137">マッピングの状態を **実行中** に設定しようとすると、次のようなエラーが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="120e4-137">You might receive an error like the following when you try to set that state of a mapping to **Running** :</span></span>

<span data-ttu-id="120e4-138">*初期データの同期を完了できません。エラー: デュアル書き込みエラー ― プラグインの登録に失敗しました: デュアル書き込みルックアップのメタデータをビルドできません。エラーオブジェクト参照がオブジェクトのインスタンスに設定されていません。*</span><span class="sxs-lookup"><span data-stu-id="120e4-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="120e4-139">このエラーの修正方法は、エラーの原因によって異なります。</span><span class="sxs-lookup"><span data-stu-id="120e4-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="120e4-140">マッピングに依存マッピングが含まれている場合は、このエンティティ マッピングの依存マッピングを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="120e4-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this entity mapping.</span></span>
+ <span data-ttu-id="120e4-141">マッピング元、またはマッピング先のフィールドがない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="120e4-141">The mapping might be missing source or destination fields.</span></span> <span data-ttu-id="120e4-142">Finance and Operations アプリのフィールドが見つからない場合は、[マッピングにおけるエンティティ フィールドの欠落](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps) のセクションに記載されている手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="120e4-142">If a field in the Finance and Operations app is missing, then follow the steps in the section [Missing entity fields issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span></span> <span data-ttu-id="120e4-143">Common Data Service でフィールドが表示されていない場合は、[マッピング] の **エンティティの更新** をクリックして、フィールドが自動的にマッピングに反映されるようにします。</span><span class="sxs-lookup"><span data-stu-id="120e4-143">If a field in Common Data Service is missing, then click **Refresh entities** button on the mapping so that the fields are automatically populated back into the mapping.</span></span>
