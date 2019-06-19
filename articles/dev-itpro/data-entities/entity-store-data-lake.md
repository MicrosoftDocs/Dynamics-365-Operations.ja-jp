---
title: エンティティ格納を Data Lake として使用可能にする
description: このトピックでは、エンティティ格納を Microsoft Azure Data Lake として使用可能にする方法について説明します。
author: MilindaV2
manager: AnnBe
ms.date: 12/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 96283
ms.assetid: ''
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2018-12-03
ms.dyn365.ops.version: Platform Update 23
ms.openlocfilehash: 5bbb4da199391f148f8f6b363f98af43bf6178dc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544270"
---
# <a name="make-entity-store-available-as-a-data-lake"></a><span data-ttu-id="05aa5-103">エンティティ格納を Data Lake として使用可能にする</span><span class="sxs-lookup"><span data-stu-id="05aa5-103">Make Entity store available as a Data Lake</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/private-preview-banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="05aa5-104">このシナリオへのアクセスは、フライティングを通じて利用できます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-104">Access to this scenario is made available via flighting.</span></span> <span data-ttu-id="05aa5-105">シナリオは、複数のプラットフォームの更新プログラムを通じてリリースされます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-105">The scenario is being released through multiple platform updates:</span></span>
>
> - <span data-ttu-id="05aa5-106">**自動化されたエンティティ格納の更新:** プラットフォーム更新 23 で利用可</span><span class="sxs-lookup"><span data-stu-id="05aa5-106">**Automated Entity store refresh:** Available in Platform update 23</span></span>
> - <span data-ttu-id="05aa5-107">**Microsoft Azure Data Lake (フル プッシュ) のエンティティ格納データ:** プラットフォーム更新 23 (制限付き) で利用可</span><span class="sxs-lookup"><span data-stu-id="05aa5-107">**Entity store data in Microsoft Azure Data Lake (full push):** Available in Platform update 23 (Restricted)</span></span>
> - <span data-ttu-id="05aa5-108">**PowerBI.com にあるエンティティ格納スキーマの DataFlows :** 将来のプラットフォーム更新で使用可能</span><span class="sxs-lookup"><span data-stu-id="05aa5-108">**DataFlows for Entity store schemas on PowerBI.com:** Available in a future platform update</span></span>
> - <span data-ttu-id="05aa5-109">**Azure Data Lake (トリクル フィード) のエンティティ格納データ:** 将来のプラットフォーム更新で利用可</span><span class="sxs-lookup"><span data-stu-id="05aa5-109">**Entity store data in Azure Data Lake (trickle feed):** Available in a future platform update</span></span>
> - <span data-ttu-id="05aa5-110">**PowerBI.comを 使用して分析ワークスペースを拡張:** 将来のプラットフォーム更新で使用可能</span><span class="sxs-lookup"><span data-stu-id="05aa5-110">**Extend analytical workspaces by using PowerBI.com:** Available in a future platform update</span></span>

## <a name="automated-entity-store-refresh"></a><span data-ttu-id="05aa5-111">自動化エンティティ格納更新</span><span class="sxs-lookup"><span data-stu-id="05aa5-111">Automated Entity store refresh</span></span>
<span data-ttu-id="05aa5-112">Date Lake 統合を有効にする前に、自動のエンティティ店舗更新を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="05aa5-112">You need to enable automated Entity store refresh before enabling Data Lake integration.</span></span> 
1. <span data-ttu-id="05aa5-113">**システム管理** \> **セットアップ** \> **エンティティ格納** に移動します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-113">Go to **System administration** \> **Set up** \> **Entity store**.</span></span>

    <span data-ttu-id="05aa5-114">**エンティティ店舗** ページで、メッセージに、**自動エンティティ格納更新** オプションに切り替えることができることが示されます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-114">On the **Entity store** page, a message indicates that you can switch to the **Automated Entity store refresh** option.</span></span> <span data-ttu-id="05aa5-115">このオプションは、システムによって管理されます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-115">This option is managed by the system.</span></span> <span data-ttu-id="05aa5-116">管理者は、エンティティ格納更新をスケジュール設定または監視する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="05aa5-116">An admin doesn't have to schedule or monitor the Entity store refresh.</span></span>

2. <span data-ttu-id="05aa5-117">**今すぐ切り替える** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-117">Select **Switch now**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="05aa5-118">このアクションは、元に戻すことはできません。</span><span class="sxs-lookup"><span data-stu-id="05aa5-118">This action isn't reversible.</span></span> <span data-ttu-id="05aa5-119">**自動エンティティ格納更新** オプションに切り替えた後、古いユーザー インターフェイス (UI) エクスペリエンスに戻すことはできません。</span><span class="sxs-lookup"><span data-stu-id="05aa5-119">After you switch to the **Automated Entity store refresh** option, you can't revert to the old user interface (UI) experience.</span></span>

3. <span data-ttu-id="05aa5-120">**はい** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-120">Select **Yes** to continue.</span></span>

<span data-ttu-id="05aa5-121">新しいエクスペリエンスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-121">You will now see the new experience.</span></span>

![新しい UI エクスペリエンス](./media/entity-store-data-lake-03.png)

<span data-ttu-id="05aa5-123">新しいエクスペリエンスをオンにすると、それぞれの集計の測定で更新を定義できます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-123">After the new experience is turned on, you can define the refresh for each aggregate measurement.</span></span> <span data-ttu-id="05aa5-124">次の更新オプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-124">The following refresh options are available:</span></span>

- <span data-ttu-id="05aa5-125">1 時間ごと</span><span class="sxs-lookup"><span data-stu-id="05aa5-125">Every hour</span></span>
- <span data-ttu-id="05aa5-126">1 日に 2 回</span><span class="sxs-lookup"><span data-stu-id="05aa5-126">Twice a day</span></span>
- <span data-ttu-id="05aa5-127">1 日に 1 回</span><span class="sxs-lookup"><span data-stu-id="05aa5-127">Once a day</span></span>
- <span data-ttu-id="05aa5-128">1 週間に 1 回</span><span class="sxs-lookup"><span data-stu-id="05aa5-128">Once a week</span></span>

<span data-ttu-id="05aa5-129">加えて、**更新** ボタンを選択することにより、管理者が必要に応じて集計の測定を更新できます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-129">In addition, an admin can refresh any aggregate measurement on demand by selecting the **Refresh** button.</span></span> <span data-ttu-id="05aa5-130">追加のオプションは、将来のプラットフォーム更新プログラムで追加されます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-130">Additional options will be added in future platform updates.</span></span> <span data-ttu-id="05aa5-131">これらのオプションには、リアルタイム更新のオプションが含められます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-131">These options will include options for real-time refresh.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05aa5-132">自動化更新を有効にすると、システムは集計測定の更新を無効にすることがあります。</span><span class="sxs-lookup"><span data-stu-id="05aa5-132">When the automated refresh is enabled, in some cases the system may disable refresh of Aggregate measurements.</span></span> <span data-ttu-id="05aa5-133">集計測定に戻って、適切な更新間隔がシステムに適用されていることを検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05aa5-133">You must revisit aggregate measurements and validate that appropriate refresh intervals have been applied by the system.</span></span>
>

## <a name="entity-store-data-in-azure-data-lake-full-push"></a><span data-ttu-id="05aa5-134">Azure Data Lake 内のエンティティ格納データ (フル プッシュ)</span><span class="sxs-lookup"><span data-stu-id="05aa5-134">Entity store data in Azure Data Lake (full push)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05aa5-135">この制限機能は、フライティング経由でオンにします。</span><span class="sxs-lookup"><span data-stu-id="05aa5-135">This restricted feature is turned on via flighting.</span></span> <span data-ttu-id="05aa5-136">この機能は、環境がフライトに含まれている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-136">This feature is available only if your environment is included in the flight.</span></span>

<span data-ttu-id="05aa5-137">この機能が有効になると、エンティティ格納データは、Microsoft サブスクリプションでリレーショナル エンティティ格納データベースに入力されません。</span><span class="sxs-lookup"><span data-stu-id="05aa5-137">When this feature is turned on, Entity store data isn't populated in the relational Entity store database in the Microsoft subscription.</span></span> <span data-ttu-id="05aa5-138">代わりに、独自のサブスクリプションの Azure Data Lake Storage Gen2 アカウントに入力されます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-138">Instead, it's populated in an Azure Data Lake Storage Gen2 account in your own subscription.</span></span> <span data-ttu-id="05aa5-139">PowerBI.com およびその他の Azure ツールのすべての機能をエンティティ格納で使用できます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-139">You can use the full capabilities of PowerBI.com and other Azure tools to work with Entity store.</span></span>

<span data-ttu-id="05aa5-140">開始する前に、Azure ポータルでこれらのタスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05aa5-140">Before you start, you must complete these tasks in the Azure portal.</span></span>

1. <span data-ttu-id="05aa5-141">**ストレージ アカウントを作成する。**</span><span class="sxs-lookup"><span data-stu-id="05aa5-141">**Create storage accounts.**</span></span> <span data-ttu-id="05aa5-142">Microsoft Dynamics 365 for Finance and Operations 環境が準備されているのと同じデータ センター内のストレージ アカウントの準備。</span><span class="sxs-lookup"><span data-stu-id="05aa5-142">Provision a storage account in the same data center where your Microsoft Dynamics 365 for Finance and Operations environment is provisioned.</span></span> <span data-ttu-id="05aa5-143">その後で指定する必要があるため、ストレージ アカウントの接続文字列をメモします。</span><span class="sxs-lookup"><span data-stu-id="05aa5-143">Make a note of the connection string for the storage account, because you will have to provide it later.</span></span>
2. <span data-ttu-id="05aa5-144">**Key Vault およびシークレットを作成する。**</span><span class="sxs-lookup"><span data-stu-id="05aa5-144">**Create a Key Vault and a secret.**</span></span> <span data-ttu-id="05aa5-145">独自のサブスクリプションで Azure Key Vault をプロビジョニングします。</span><span class="sxs-lookup"><span data-stu-id="05aa5-145">Provision Azure Key Vault in your own subscription.</span></span> <span data-ttu-id="05aa5-146">作成した Key Vault エントリのドメイン ネーム システム (DNS) 名が必要になります。</span><span class="sxs-lookup"><span data-stu-id="05aa5-146">You will need the Domain Name System (DNS) name of the Key Vault entry that you created.</span></span> <span data-ttu-id="05aa5-147">さらに、Key Vault にシークレットを追加します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-147">Also add a secret to Key Vault.</span></span> <span data-ttu-id="05aa5-148">値として、前のタスクで書き留めた接続文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-148">As the value, specify the connection string that you made a note of in the previous task.</span></span> <span data-ttu-id="05aa5-149">その後で指定する必要があるため、シークレットの名前をメモします。</span><span class="sxs-lookup"><span data-stu-id="05aa5-149">Make a note of the name of the secret, because you will have to provide it later.</span></span>
3. <span data-ttu-id="05aa5-150">**アプリを登録する。**</span><span class="sxs-lookup"><span data-stu-id="05aa5-150">**Register the app.**</span></span> <span data-ttu-id="05aa5-151">Azure Active Directory (Azure AD) アプリケーションを作成し、Key Vault にアプリケーション プログラミング インターフェイス (API) アクセスを付与します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-151">Create an Azure Active Directory (Azure AD) application, and grant application programming interface (API) access to Key vault.</span></span> <span data-ttu-id="05aa5-152">後でを入力する必要があるため、アプリケーション IDとそのアプリケーション キー (シークレット) をメモします。</span><span class="sxs-lookup"><span data-stu-id="05aa5-152">Make a note of the application ID and its application key (secret), because you will have to provide them later.</span></span>
4. <span data-ttu-id="05aa5-153">**サービス プリンシパルを Key Vault に追加する。**</span><span class="sxs-lookup"><span data-stu-id="05aa5-153">**Add a service principal to Key Vault.**</span></span> <span data-ttu-id="05aa5-154">Key Vault で、**アクセス ポリシー** オプションを使用して、Azure AD アプリケーションに**取得**および**リスト**アクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-154">In Key Vault, use the **Access policies** option to grant the Azure AD application **Get** and **List** permissions.</span></span> <span data-ttu-id="05aa5-155">この方法で、アプリケーションは、Key Vault 内のシークレットにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-155">In this way, the application will have access to the secrets in Key Vault.</span></span>

<span data-ttu-id="05aa5-156">次のセクションでは、それぞれのタスクについて詳細に説明します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-156">The following sections describe each task in more detail.</span></span>

### <a name="create-storage-accounts"></a><span data-ttu-id="05aa5-157">ストレージ アカウントを作成する</span><span class="sxs-lookup"><span data-stu-id="05aa5-157">Create storage accounts</span></span>

1. <span data-ttu-id="05aa5-158">Azure ポータルで、新しいストレージ アカウントを作成します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-158">In the Azure portal, create a new storage account.</span></span>
2. <span data-ttu-id="05aa5-159">**ストレージ アカウントを作成** ダイアログ ボックスで、次のパラメーター フィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-159">In the **Create storage account** dialog box, provide values for the following parameter fields:</span></span>

    - <span data-ttu-id="05aa5-160">**場所:** Finance and Operations 環境があるデータ センターを選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-160">**Location:** Select the data center where your Finance and Operations environment is located.</span></span> <span data-ttu-id="05aa5-161">選択したデータ センターが異なる Azure リージョンにある場合、追加のデータ移動コストが発生します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-161">If the data center that you select is in a different Azure region, you will incur additional data movement costs.</span></span> <span data-ttu-id="05aa5-162">Microsoft Power BI やデータ ウェアハウスが別の地域にある場合、地域間でストレージを移動するためにレプリケーションを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-162">If your Microsoft Power BI and/or your data warehouse is in a different region, you can use replication to move storage between regions.</span></span>
    - <span data-ttu-id="05aa5-163">**パフォーマンス:** **標準**を選択することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="05aa5-163">**Performance:** We recommend that you select **Standard**.</span></span>
    - <span data-ttu-id="05aa5-164">**アカウントの種類:** **StorageV2** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05aa5-164">**Account kind:** You must select **StorageV2**.</span></span>

3. <span data-ttu-id="05aa5-165">**詳細オプション** ダイアログ ボックスで、**Data Lake ストレージ Gen2 (プレビュー)** オプションをオフにします。</span><span class="sxs-lookup"><span data-stu-id="05aa5-165">In the **Advanced options** dialog box, turn off the **Data Lake storage Gen2 (preview)** option.</span></span>

    > [!NOTE]
    > <span data-ttu-id="05aa5-166">これは、今後の更新で使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="05aa5-166">This will be made available in a later update.</span></span> <span data-ttu-id="05aa5-167">それまでは、Azure Data Lake Storage API を使用してデータを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="05aa5-167">Until then, you can't consume data by using Azure Data Lake Storage APIs.</span></span>
    >
    > <span data-ttu-id="05aa5-168">Data Lake Storage Gen2 のプレビュー プログラムに参加していない場合、**Data Lake ストレージ Gen2 (プレビュー)** オプションが表示されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="05aa5-168">If you aren't part of the preview program for Data Lake Storage Gen2, you might not see the **Data Lake storage Gen2 (preview)** option.</span></span>

4. <span data-ttu-id="05aa5-169">**確認して作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-169">Select **Review and create**.</span></span> <span data-ttu-id="05aa5-170">配置が完了したら、新しいリソースが Azure ポータルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-170">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
5. <span data-ttu-id="05aa5-171">リソースを選択し、**設定** \> **アクセス キー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-171">Select the resource, and then select **Settings** \> **Access keys**.</span></span>
6. <span data-ttu-id="05aa5-172">その後で指定する必要があるため、接続文字列値を書き留めます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-172">Make a note of the connection string value, because you will have to provide it later.</span></span>

### <a name="create-a-key-vault-and-a-secret"></a><span data-ttu-id="05aa5-173">Key Vault およびシークレットを作成する</span><span class="sxs-lookup"><span data-stu-id="05aa5-173">Create a Key Vault and a secret</span></span>

1. <span data-ttu-id="05aa5-174">Azure ポータルで、新しい Key Vault を作成します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-174">In the Azure portal, create a new Key Vault.</span></span>
2. <span data-ttu-id="05aa5-175">**Key Vault の作成** ダイアログ ボックスの **場所** フィールドで、Finance and Operations 環境があるデータ センターを選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-175">In the **Create key vault** dialog box, in the **Location** field, select the data center where your Finance and Operations environment is located.</span></span>
3. <span data-ttu-id="05aa5-176">Key Vault が作成されたら、一覧で選択して **シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-176">After Key Vault is created, select it in the list, and then select **Secrets**.</span></span>
4. <span data-ttu-id="05aa5-177">**生成/インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-177">Select **Generate/Import**.</span></span>
5. <span data-ttu-id="05aa5-178">**シークレットを作成** ダイアログ ボックスの **アップロード オプション** フィールドで、**手動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-178">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
6. <span data-ttu-id="05aa5-179">シークレットの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-179">Enter a name for the secret.</span></span> <span data-ttu-id="05aa5-180">その後で指定する必要があるため、名前をメモします。</span><span class="sxs-lookup"><span data-stu-id="05aa5-180">Make a note of the name, because you will have to provide it later.</span></span>
7. <span data-ttu-id="05aa5-181">値フィールドに、前の手順でストレージ アカウントから取得した接続文字列を入力します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-181">In the value field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
8. <span data-ttu-id="05aa5-182">**有効** を選択し、**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-182">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="05aa5-183">シークレットが作成され、Key Vault に追加されます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-183">The secret is created and added to Key Vault.</span></span>

### <a name="register-the-app"></a><span data-ttu-id="05aa5-184">アプリを登録する</span><span class="sxs-lookup"><span data-stu-id="05aa5-184">Register the app</span></span>

1. <span data-ttu-id="05aa5-185">Azure ポータルで、**Azure Active Directory** を選択し、**アプリケーション登録**を選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-185">In the Azure portal, select **Azure Active Directory**, and then select **App registrations**.</span></span>
2. <span data-ttu-id="05aa5-186">**新しいアプリケーションの登録** を選択し、以下の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-186">Select **New application registration**, and enter the following information:</span></span>

    - <span data-ttu-id="05aa5-187">**名前:** アプリの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-187">**Name:** Enter the name of the app.</span></span>
    - <span data-ttu-id="05aa5-188">**アプリケーション タイプ:** **Web API** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-188">**Application type:** Select **Web API**.</span></span>
    - <span data-ttu-id="05aa5-189">**サインオン URL:** Finance and Operations のルート URL をコピーしてここに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-189">**Sign-on URL:** Copy the root URL for Finance and Operations, and paste it here.</span></span>

3. <span data-ttu-id="05aa5-190">アプリケーションが作成されたら選択し、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-190">After the application is created, select it, and then select **Settings**.</span></span>
4. <span data-ttu-id="05aa5-191">**必要なアクセス許可** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-191">Select the **Required permissions** option.</span></span>
5. <span data-ttu-id="05aa5-192">表示されたダイアログ ボックスで、**オプションの追加** を選択し、**API の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-192">In the dialog box that appears, select **Add option**, and then select **Add API**.</span></span>
6. <span data-ttu-id="05aa5-193">API のリストで **Azure Key Vault** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-193">In the list of APIs, select **Azure Key Vault**.</span></span>
7. <span data-ttu-id="05aa5-194">**委任アクセス許可** チェック ボックスをオンにしてアクセス許可を付与し、**完了** を選択して変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-194">Select the **Delegated permissions** check box, select to grant permissions, and then select **Done** to save your changes.</span></span>
8. <span data-ttu-id="05aa5-195">新しいアプリケーションの **アプリケーション** メニューで、**キー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-195">On the **Application** menu of the new app, select **Keys**.</span></span>
9. <span data-ttu-id="05aa5-196">**キーの説明** フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-196">In the **Key Description** field, enter a name.</span></span>
10. <span data-ttu-id="05aa5-197">期間を選択し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-197">Select a duration, and then select **Save**.</span></span> <span data-ttu-id="05aa5-198">シークレットが **値** フィールドに生成されます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-198">A secret is generated in the **Value** field.</span></span>
11. <span data-ttu-id="05aa5-199">1、2 分以内に削除されるので、すぐにシークレットをクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="05aa5-199">Immediately copy the secret to the clipboard, because it will disappear within one or two minutes.</span></span> <span data-ttu-id="05aa5-200">後でアプリケーションにこのキーを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05aa5-200">You will have to provide this key to the application later.</span></span>

### <a name="add-a-service-principal-to-key-vault"></a><span data-ttu-id="05aa5-201">サービス プリンシパルを Key Vault に追加する</span><span class="sxs-lookup"><span data-stu-id="05aa5-201">Add a service principal to Key Vault</span></span>

1. <span data-ttu-id="05aa5-202">Azure ポータルで、以前に作成した Key Vault を開きます。</span><span class="sxs-lookup"><span data-stu-id="05aa5-202">In the Azure portal, open Key Vault that you created earlier.</span></span>
2. <span data-ttu-id="05aa5-203">**アクセス ポリシー** を選択し、**追加** を選択して新しいアクセス許可ポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-203">Select **Access policies**, and then select **Add** to create a new access policy.</span></span>
3. <span data-ttu-id="05aa5-204">**プリンシパルの選択** フィールドに、以前に登録したアプリケーションの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-204">In the **Select principal** field, select the name of the application that you previously registered.</span></span>
4. <span data-ttu-id="05aa5-205">**キーのアクセス許可** フィールドで、**取得** および **リスト** のアクセス許可を選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-205">In the **Key permissions** field, select **Get** and **List** permissions.</span></span>
5. <span data-ttu-id="05aa5-206">**シークレットのアクセス許可** フィールドで、**取得** および **リスト** のアクセス許可を選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-206">In the **Secret permissions** field, select **Get** and **List** permissions.</span></span>

    ![取得およびリストのアクセス許可](./media/entity-store-data-lake-05.png)

6. <span data-ttu-id="05aa5-208">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-208">Select **Save**.</span></span>

## <a name="work-in-entity-store-in-a-data-lake"></a><span data-ttu-id="05aa5-209">Data Lake のエンティティ格納で作業する</span><span class="sxs-lookup"><span data-stu-id="05aa5-209">Work in Entity store in a Data Lake</span></span>

1. <span data-ttu-id="05aa5-210">**システム管理** \> **設定** \> **システム パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-210">Go to **System administration** \> **Set up** \> **System parameters**.</span></span>
2. <span data-ttu-id="05aa5-211">**データ接続** タブで、このトピックの前の部分でメモした次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-211">On the **Data connections** tab, enter the following information that you made a note of earlier in this topic:</span></span>

    - <span data-ttu-id="05aa5-212">**アプリケーション ID:** 前に登録した Azure AD アプリケーションのアプリケーション ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-212">**Application ID:** Enter the application ID of the Azure AD application that you registered earlier.</span></span>
    - <span data-ttu-id="05aa5-213">**アプリケーション シークレット:** Azure AD アプリケーションのアプリケーション キー (秘密) を入力します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-213">**Application Secret:** Enter the application key (secret) for the Azure AD application.</span></span>
    - <span data-ttu-id="05aa5-214">**DNS 名:** Key Vault の DNS 名を入力します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-214">**DNS name:** Enter the DNS name of Key Vault.</span></span>
    - <span data-ttu-id="05aa5-215">**シークレット名:** 接続文字列情報と共に Key Vault に追加したシークレットの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-215">**Secret name:** Enter the name of the secret that you added to Key Vault together with connection string information.</span></span>

    ![[システム パラメーター] ページの [データ接続] タブ](./media/entity-store-data-lake-04.png)

3. <span data-ttu-id="05aa5-217">**Azure Key Vault のテスト** および **Azure Storage のテスト** リンクを選択し、指定した構成情報にシステムがアクセスできることを検証します。</span><span class="sxs-lookup"><span data-stu-id="05aa5-217">Select the **Test Azure Key Vault** and **Test Azure Storage** links to validate that system can access the configuration information that you provided.</span></span>
4. <span data-ttu-id="05aa5-218">**データ接続を有効にする** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="05aa5-218">Select the **Enable data connection** check box.</span></span>

<span data-ttu-id="05aa5-219">エンティティ格納データが、リレーショナル エンティティ格納データベースではなく、指定したストレージ場所に入力されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="05aa5-219">Entity store data should now be populated in the storage location that you provided, not in the relational Entity store database.</span></span>

<span data-ttu-id="05aa5-220">集計の測定と、エンティティ格納 UI で選択した更新オプションが、Data Lake にコピーされたデータに適用されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="05aa5-220">The aggregate measurements and refresh options that you select in the Entity store UI should now apply to data that is copied to Data Lake.</span></span>
