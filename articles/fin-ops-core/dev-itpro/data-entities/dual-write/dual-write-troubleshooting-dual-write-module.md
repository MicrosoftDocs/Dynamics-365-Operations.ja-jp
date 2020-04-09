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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172763"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="cd55c-103">Finance and Operations アプリのデュアル書き込みモジュールに関する問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="cd55c-103">Troubleshoot issues with the Dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="cd55c-104">このトピックでは、Finance and Operations アプリと Common Data Service 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="cd55c-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="cd55c-105">このトピックでは、Finance and Operations アプリの **デュアル書き込み** モジュールの問題修正に特化したトラブルシューティング情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="cd55c-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd55c-106">このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="cd55c-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="cd55c-107">各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。</span><span class="sxs-lookup"><span data-stu-id="cd55c-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="cd55c-108">Finance and Operations アプリでデュアル書き込みのモジュールを読み込むことができない</span><span class="sxs-lookup"><span data-stu-id="cd55c-108">You can't load the Dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="cd55c-109">**データ管理** ワークスペースで **デュアル書き込み** タイルを選択しても**デュアル書き込み** のページを開くことができない場合は、データ統合サービスがダウンしている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cd55c-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="cd55c-110">サポートチケットを作成して、データ統合サービスの再起動を要求してください。</span><span class="sxs-lookup"><span data-stu-id="cd55c-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a><span data-ttu-id="cd55c-111">新しいエンティティのマッピングを作成しようとするとエラーが発生する</span><span class="sxs-lookup"><span data-stu-id="cd55c-111">Error when you try to create a new entity mapping</span></span>

<span data-ttu-id="cd55c-112">**問題の解決に必要な資格情報：** Azure ADテナント管理者</span><span class="sxs-lookup"><span data-stu-id="cd55c-112">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="cd55c-113">新しいエンティティをデュアル書き込み用で構成する場合に、次のエラーメッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="cd55c-113">You might receive the following error message when you try to configure a new entity for dual-write:</span></span>

<span data-ttu-id="cd55c-114">*応答状態コードが成功とならない: 401 (権限なし)*</span><span class="sxs-lookup"><span data-stu-id="cd55c-114">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>

<span data-ttu-id="cd55c-115">このエラーが発生する原因は、新しいエンティティのマッピングを追加できるのが、Azure AD テナント管理者のみであるためです。</span><span class="sxs-lookup"><span data-stu-id="cd55c-115">This error occurs because only an Azure AD tenant admin can add a new entity mapping.</span></span>

<span data-ttu-id="cd55c-116">この問題を解決するには、Finance and Operations アプリに Azure AD 管理テナントでログインしてください。</span><span class="sxs-lookup"><span data-stu-id="cd55c-116">To fix the issue, sign in to the Finance and Operations app as an Azure AD admin tenant.</span></span> <span data-ttu-id="cd55c-117">また、web.PowerApps.com にアクセスし、接続の再検証をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd55c-117">You must also go to web.PowerApps.com and revalidate your connection.</span></span>

## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="cd55c-118">デュアル書き込みのユーザー インターフェイスを開くとエラーが発生する</span><span class="sxs-lookup"><span data-stu-id="cd55c-118">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="cd55c-119">**データ管理**ワークスペースからデュアル書き込みにアクセスすると、次のエラーメッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="cd55c-119">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="cd55c-120">*login.microsoftonline.com が接続を拒否しました。*</span><span class="sxs-lookup"><span data-stu-id="cd55c-120">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="cd55c-121">この問題を修正するには、Microsoft Edge の InPrivate を使用してサインインするか、Chromium の incognito ウィンドウを使用するか、Google Chrome のincognitoウィンドウを使用してください。</span><span class="sxs-lookup"><span data-stu-id="cd55c-121">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="cd55c-122">また、サードパーティの cookie のブロックを解除、クリアする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd55c-122">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="cd55c-123">環境をデュアル書き込みにリンクする際、または新しいエンティティのマッピングを追加する際にエラーが発生する</span><span class="sxs-lookup"><span data-stu-id="cd55c-123">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="cd55c-124">**問題の解決に必要な資格情報：** Azure ADテナント管理者</span><span class="sxs-lookup"><span data-stu-id="cd55c-124">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="cd55c-125">マッピングをリンクまたは作成する際に、次のエラーが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="cd55c-125">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="cd55c-126">*応答状態コードが成功とならない: 403 (tokenexchange) 。<br>セッション ID: \<セッション ID\><br>ルート アクティビティ ID: \<ご利用のルート アクティビティ ID\>*</span><span class="sxs-lookup"><span data-stu-id="cd55c-126">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="cd55c-127">このエラーは、デュアル書き込みへのリンクと、マッピングを作成する十分なアクセス権限がない場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cd55c-127">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="cd55c-128">Azure AD のテナントの管理者アカウントを作成して環境をリンクし、エンティティのマッピングを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd55c-128">You must use an Azure AD tenant admin account to link environments and add new entity mappings.</span></span> <span data-ttu-id="cd55c-129">この設定後は、非管理者のアカウントを使用してステータスを監視し、マッピングを編集することができます。</span><span class="sxs-lookup"><span data-stu-id="cd55c-129">However, after setup, you can use a non-admin account to monitor status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="cd55c-130">エンティティ マッピングを停止した際のエラー</span><span class="sxs-lookup"><span data-stu-id="cd55c-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="cd55c-131">エンティティのマッピングを停止した際に、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="cd55c-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="cd55c-132">*\[禁止されています\]、\[{状態: 403、"ソース": ""、"メッセージ": "トークン変換エラー: ユーザーに dynamicscrmonline/xxxxxx-xxxx-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx への接続許可がありません"}\]、リモート サーバーがエラーを返しました：(403) 許可されていません。*</span><span class="sxs-lookup"><span data-stu-id="cd55c-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="cd55c-133">このエラーは、リンクされた Common Data Service 環境が使用できない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="cd55c-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="cd55c-134">この問題を修正するには、チケットを作成してデータ統合チームに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="cd55c-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="cd55c-135">データ統合チームがマッピンがバックエンドで **実行されていない** ことを識別できるように、ネットワークのトレースを添付してください。</span><span class="sxs-lookup"><span data-stu-id="cd55c-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>
