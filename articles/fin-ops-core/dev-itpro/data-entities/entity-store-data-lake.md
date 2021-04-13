---
title: エンティティ格納を Data Lake として使用可能にする
description: このトピックでは、エンティティ格納を Microsoft Azure Data Lake として使用可能にする方法について説明します。
author: MilindaV2
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 96283
ms.assetid: ''
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2018-12-03
ms.dyn365.ops.version: Platform Update 23
ms.openlocfilehash: 41f3db7495693dd1b974b0632de4c67a09d6da58
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750578"
---
# <a name="make-entity-store-available-as-a-data-lake"></a><span data-ttu-id="db1cf-103">エンティティ格納を Data Lake として使用可能にする</span><span class="sxs-lookup"><span data-stu-id="db1cf-103">Make Entity store available as a Data Lake</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="db1cf-104">この機能は現在パブリック プレビューにあります。</span><span class="sxs-lookup"><span data-stu-id="db1cf-104">This feature is currently in public preview.</span></span> <span data-ttu-id="db1cf-105">この機能は、次のコンポーネントで構成されています。</span><span class="sxs-lookup"><span data-stu-id="db1cf-105">This feature is comprised of the following components:</span></span>
>
> - <span data-ttu-id="db1cf-106">**自動化されたエンティティ格納の更新** - プラットフォーム更新 23 で利用可。</span><span class="sxs-lookup"><span data-stu-id="db1cf-106">**Automated Entity store refresh** - Available in Platform update 23.</span></span>
> - <span data-ttu-id="db1cf-107">**Microsoft Azure Data Lake (フル プッシュ) のエンティティ格納データ** - プラットフォーム更新 26 で利用可。</span><span class="sxs-lookup"><span data-stu-id="db1cf-107">**Entity store data in Microsoft Azure Data Lake (full push)** - Available in Platform update 26.</span></span> 
> - <span data-ttu-id="db1cf-108">**PowerBI.com にあるエンティティ格納スキーマの DataFlows** - 将来のプラットフォーム更新で使用可能。</span><span class="sxs-lookup"><span data-stu-id="db1cf-108">**DataFlows for Entity store schemas on PowerBI.com** - Available in a future platform update.</span></span>
> - <span data-ttu-id="db1cf-109">**Azure Data Lake (トリクル フィード) のエンティティ格納データ** - プラットフォーム更新 28 で利用可。</span><span class="sxs-lookup"><span data-stu-id="db1cf-109">**Entity store data in Azure Data Lake (trickle feed)** - Available in Platform update 28.</span></span>
> - <span data-ttu-id="db1cf-110">**PowerBI.comを 使用して分析ワークスペースを拡張** - 将来のプラットフォーム更新で使用可能。</span><span class="sxs-lookup"><span data-stu-id="db1cf-110">**Extend analytical workspaces by using PowerBI.com** - Available in a future platform update.</span></span>

## <a name="automated-entity-store-refresh"></a><span data-ttu-id="db1cf-111">自動化エンティティ格納更新</span><span class="sxs-lookup"><span data-stu-id="db1cf-111">Automated Entity store refresh</span></span>
<span data-ttu-id="db1cf-112">Date Lake 統合を有効にする前に、自動のエンティティ店舗更新を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="db1cf-112">You need to enable automated Entity store refresh before enabling Data Lake integration.</span></span> 
1. <span data-ttu-id="db1cf-113">**システム管理** \> **セットアップ** \> **エンティティ格納** に移動します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-113">Go to **System administration** \> **Set up** \> **Entity store**.</span></span>

    <span data-ttu-id="db1cf-114">**エンティティ店舗** ページで、メッセージに、**自動エンティティ格納更新** オプションに切り替えることができることが示されます。</span><span class="sxs-lookup"><span data-stu-id="db1cf-114">On the **Entity store** page, a message indicates that you can switch to the **Automated Entity store refresh** option.</span></span> <span data-ttu-id="db1cf-115">このオプションは、システムによって管理されます。</span><span class="sxs-lookup"><span data-stu-id="db1cf-115">This option is managed by the system.</span></span> <span data-ttu-id="db1cf-116">管理者は、エンティティ格納更新をスケジュール設定または監視する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="db1cf-116">An admin doesn't have to schedule or monitor the Entity store refresh.</span></span>

2. <span data-ttu-id="db1cf-117">**今すぐ切り替える** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-117">Select **Switch now**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="db1cf-118">このアクションは、元に戻すことはできません。</span><span class="sxs-lookup"><span data-stu-id="db1cf-118">This action isn't reversible.</span></span> <span data-ttu-id="db1cf-119">**自動エンティティ格納更新** オプションに切り替えた後、古いユーザー インターフェイス (UI) エクスペリエンスに戻すことはできません。</span><span class="sxs-lookup"><span data-stu-id="db1cf-119">After you switch to the **Automated Entity store refresh** option, you can't revert to the old user interface (UI) experience.</span></span>

3. <span data-ttu-id="db1cf-120">**はい** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-120">Select **Yes** to continue.</span></span>

<span data-ttu-id="db1cf-121">新しいエクスペリエンスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="db1cf-121">You will now see the new experience.</span></span>

![新しい UI エクスペリエンス](./media/entity-store-data-lake-03.png)

<span data-ttu-id="db1cf-123">新しいエクスペリエンスをオンにすると、それぞれの集計の測定で更新を定義できます。</span><span class="sxs-lookup"><span data-stu-id="db1cf-123">After the new experience is turned on, you can define the refresh for each aggregate measurement.</span></span> <span data-ttu-id="db1cf-124">次の更新オプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="db1cf-124">The following refresh options are available:</span></span>

- <span data-ttu-id="db1cf-125">1 時間ごと</span><span class="sxs-lookup"><span data-stu-id="db1cf-125">Every hour</span></span>
- <span data-ttu-id="db1cf-126">1 日に 2 回</span><span class="sxs-lookup"><span data-stu-id="db1cf-126">Twice a day</span></span>
- <span data-ttu-id="db1cf-127">1 日に 1 回</span><span class="sxs-lookup"><span data-stu-id="db1cf-127">Once a day</span></span>
- <span data-ttu-id="db1cf-128">1 週間に 1 回</span><span class="sxs-lookup"><span data-stu-id="db1cf-128">Once a week</span></span>

<span data-ttu-id="db1cf-129">加えて、**更新** ボタンを選択することにより、管理者が必要に応じて集計の測定を更新できます。</span><span class="sxs-lookup"><span data-stu-id="db1cf-129">In addition, an admin can refresh any aggregate measurement on demand by selecting the **Refresh** button.</span></span> <span data-ttu-id="db1cf-130">追加のオプションは、将来のプラットフォーム更新プログラムで追加されます。</span><span class="sxs-lookup"><span data-stu-id="db1cf-130">Additional options will be added in future platform updates.</span></span> <span data-ttu-id="db1cf-131">これらのオプションには、リアルタイム更新のオプションが含められます。</span><span class="sxs-lookup"><span data-stu-id="db1cf-131">These options will include options for real-time refresh.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="db1cf-132">自動化更新を有効にすると、システムは集計測定の更新を無効にすることがあります。</span><span class="sxs-lookup"><span data-stu-id="db1cf-132">When the automated refresh is enabled, in some cases the system may disable refresh of Aggregate measurements.</span></span> <span data-ttu-id="db1cf-133">集計測定に戻って、適切な更新間隔がシステムに適用されていることを検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="db1cf-133">You must revisit aggregate measurements and validate that appropriate refresh intervals have been applied by the system.</span></span>
>

## <a name="entity-store-data-in-azure-data-lake-full-push-and-trickle-feed"></a><span data-ttu-id="db1cf-134">Azure Data Lake (フル プッシュおよびトリクル フィード) のエンティティ格納データ</span><span class="sxs-lookup"><span data-stu-id="db1cf-134">Entity store data in Azure Data Lake (full push and trickle feed)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="db1cf-135">この機能は現在パブリック プレビューにあります。</span><span class="sxs-lookup"><span data-stu-id="db1cf-135">This feature is currently in public preview.</span></span> <span data-ttu-id="db1cf-136">運用環境では、この機能を有効にしないでください。</span><span class="sxs-lookup"><span data-stu-id="db1cf-136">Do not enable this feature in production environments.</span></span>

<span data-ttu-id="db1cf-137">この機能が有効になると、エンティティ格納データは、Microsoft サブスクリプションでリレーショナル エンティティ格納データベースに入力されません。</span><span class="sxs-lookup"><span data-stu-id="db1cf-137">When this feature is turned on, Entity store data isn't populated in the relational Entity store database in the Microsoft subscription.</span></span> <span data-ttu-id="db1cf-138">代わりに、独自のサブスクリプションの Azure Data Lake Storage Gen2 アカウントに入力されます。</span><span class="sxs-lookup"><span data-stu-id="db1cf-138">Instead, it's populated in an Azure Data Lake Storage Gen2 account in your own subscription.</span></span> <span data-ttu-id="db1cf-139">PowerBI.com およびその他の Azure ツールのすべての機能をエンティティ格納で使用できます。</span><span class="sxs-lookup"><span data-stu-id="db1cf-139">You can use the full capabilities of PowerBI.com and other Azure tools to work with Entity store.</span></span>

<span data-ttu-id="db1cf-140">開始する前に、Azure ポータルでこれらのタスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="db1cf-140">Before you start, you must complete these tasks in the Azure portal.</span></span>

1. <span data-ttu-id="db1cf-141">**ストレージ アカウントを作成する。**</span><span class="sxs-lookup"><span data-stu-id="db1cf-141">**Create storage accounts.**</span></span> <span data-ttu-id="db1cf-142">環境がプロビジョニングされているのと同じデータ センター内のストレージ アカウントのプロビジョニング。</span><span class="sxs-lookup"><span data-stu-id="db1cf-142">Provision a storage account in the same data center where your environment is provisioned.</span></span> <span data-ttu-id="db1cf-143">その後で指定する必要があるため、ストレージ アカウントの接続文字列をメモします。</span><span class="sxs-lookup"><span data-stu-id="db1cf-143">Make a note of the connection string for the storage account, because you will have to provide it later.</span></span>
2. <span data-ttu-id="db1cf-144">**Key Vault およびシークレットを作成する。**</span><span class="sxs-lookup"><span data-stu-id="db1cf-144">**Create a Key Vault and a secret.**</span></span> <span data-ttu-id="db1cf-145">独自のサブスクリプションで Azure Key Vault をプロビジョニングします。</span><span class="sxs-lookup"><span data-stu-id="db1cf-145">Provision Azure Key Vault in your own subscription.</span></span> <span data-ttu-id="db1cf-146">作成した Key Vault エントリのドメイン ネーム システム (DNS) 名が必要になります。</span><span class="sxs-lookup"><span data-stu-id="db1cf-146">You will need the Domain Name System (DNS) name of the Key Vault entry that you created.</span></span> <span data-ttu-id="db1cf-147">さらに、Key Vault にシークレットを追加します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-147">Also add a secret to Key Vault.</span></span> <span data-ttu-id="db1cf-148">値として、前のタスクで書き留めた接続文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-148">As the value, specify the connection string that you made a note of in the previous task.</span></span> <span data-ttu-id="db1cf-149">その後で指定する必要があるため、シークレットの名前をメモします。</span><span class="sxs-lookup"><span data-stu-id="db1cf-149">Make a note of the name of the secret, because you will have to provide it later.</span></span>
3. <span data-ttu-id="db1cf-150">**アプリを登録する。**</span><span class="sxs-lookup"><span data-stu-id="db1cf-150">**Register the app.**</span></span> <span data-ttu-id="db1cf-151">Azure Active Directory (Azure AD) アプリケーションを作成し、Key Vault にアプリケーション プログラミング インターフェイス (API) アクセスを付与します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-151">Create an Azure Active Directory (Azure AD) application, and grant application programming interface (API) access to Key vault.</span></span> <span data-ttu-id="db1cf-152">後でを入力する必要があるため、アプリケーション IDとそのアプリケーション キー (シークレット) をメモします。</span><span class="sxs-lookup"><span data-stu-id="db1cf-152">Make a note of the application ID and its application key (secret), because you will have to provide them later.</span></span>
4. <span data-ttu-id="db1cf-153">**サービス プリンシパルを Key Vault に追加する。**</span><span class="sxs-lookup"><span data-stu-id="db1cf-153">**Add a service principal to Key Vault.**</span></span> <span data-ttu-id="db1cf-154">Key Vault で、**アクセス ポリシー** オプションを使用して、Azure AD アプリケーションに **取得** および **リスト** アクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-154">In Key Vault, use the **Access policies** option to grant the Azure AD application **Get** and **List** permissions.</span></span> <span data-ttu-id="db1cf-155">この方法で、アプリケーションは、Key Vault 内のシークレットにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="db1cf-155">In this way, the application will have access to the secrets in Key Vault.</span></span>

<span data-ttu-id="db1cf-156">次のセクションでは、それぞれのタスクについて詳細に説明します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-156">The following sections describe each task in more detail.</span></span>

### <a name="create-storage-accounts"></a><span data-ttu-id="db1cf-157">ストレージ アカウントを作成する</span><span class="sxs-lookup"><span data-stu-id="db1cf-157">Create storage accounts</span></span>

1. <span data-ttu-id="db1cf-158">Azure ポータルで、新しいストレージ アカウントを作成します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-158">In the Azure portal, create a new storage account.</span></span>
2. <span data-ttu-id="db1cf-159">**ストレージ アカウントを作成** ダイアログ ボックスで、次のパラメーター フィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-159">In the **Create storage account** dialog box, provide values for the following parameter fields:</span></span>

    - <span data-ttu-id="db1cf-160">**場所:** 環境があるデータ センターを選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-160">**Location:** Select the data center where your environment is located.</span></span> <span data-ttu-id="db1cf-161">選択したデータ センターが異なる Azure リージョンにある場合、追加のデータ移動コストが発生します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-161">If the data center that you select is in a different Azure region, you will incur additional data movement costs.</span></span> <span data-ttu-id="db1cf-162">Microsoft Power BI やデータ ウェアハウスが別の地域にある場合は、地域間でのストレージ移動にはレプリケーションを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="db1cf-162">If your Microsoft Power BI and/or your data warehouse is in a different region, you can use replication to move storage between regions.</span></span>
    - <span data-ttu-id="db1cf-163">**パフォーマンス:** **標準** を選択することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="db1cf-163">**Performance:** We recommend that you select **Standard**.</span></span>
    - <span data-ttu-id="db1cf-164">**アカウントの種類:** **StorageV2** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="db1cf-164">**Account kind:** You must select **StorageV2**.</span></span>

3. <span data-ttu-id="db1cf-165">**詳細オプション** ダイアログ ボックスで、**Data Lake ストレージ Gen2** オプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="db1cf-165">In the **Advanced options** dialog box, you will see the **Data Lake storage Gen2** option.</span></span> <span data-ttu-id="db1cf-166">階層の名前空間機能で、**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-166">Select **Enable** under the Hierarchical namespaces feature.</span></span> <span data-ttu-id="db1cf-167">このオプションを無効にすると、Power BI データ フローなどのサービスを含む Finance and Operations アプリによって書き込まれたデータを使用することができません。</span><span class="sxs-lookup"><span data-stu-id="db1cf-167">If you disable this option, you can't consume data written by Finance and Operations apps with services such as Power BI data flows.</span></span> 
4. <span data-ttu-id="db1cf-168">**確認して作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-168">Select **Review and create**.</span></span> <span data-ttu-id="db1cf-169">配置が完了したら、新しいリソースが Azure ポータルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="db1cf-169">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
5. <span data-ttu-id="db1cf-170">リソースを選択し、**設定** \> **アクセス キー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-170">Select the resource, and then select **Settings** \> **Access keys**.</span></span>
6. <span data-ttu-id="db1cf-171">その後で指定する必要があるため、接続文字列値を書き留めます。</span><span class="sxs-lookup"><span data-stu-id="db1cf-171">Make a note of the connection string value, because you will have to provide it later.</span></span>

### <a name="create-a-key-vault-and-a-secret"></a><span data-ttu-id="db1cf-172">Key Vault およびシークレットを作成する</span><span class="sxs-lookup"><span data-stu-id="db1cf-172">Create a Key Vault and a secret</span></span>

1. <span data-ttu-id="db1cf-173">Azure ポータルで、新しい Key Vault を作成します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-173">In the Azure portal, create a new Key Vault.</span></span>
2. <span data-ttu-id="db1cf-174">**Key Vault の作成** ダイアログ ボックスの **場所** フィールドで、環境があるデータ センターを選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-174">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
3. <span data-ttu-id="db1cf-175">Key Vault が作成されたら、一覧で選択して **シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-175">After Key Vault is created, select it in the list, and then select **Secrets**.</span></span>
4. <span data-ttu-id="db1cf-176">**生成/インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-176">Select **Generate/Import**.</span></span>
5. <span data-ttu-id="db1cf-177">**シークレットを作成** ダイアログ ボックスの **アップロード オプション** フィールドで、**手動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-177">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
6. <span data-ttu-id="db1cf-178">シークレットの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-178">Enter a name for the secret.</span></span> <span data-ttu-id="db1cf-179">その後で指定する必要があるため、名前をメモします。</span><span class="sxs-lookup"><span data-stu-id="db1cf-179">Make a note of the name, because you will have to provide it later.</span></span>
7. <span data-ttu-id="db1cf-180">値フィールドに、前の手順でストレージ アカウントから取得した接続文字列を入力します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-180">In the value field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
8. <span data-ttu-id="db1cf-181">**有効** を選択し、**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-181">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="db1cf-182">シークレットが作成され、Key Vault に追加されます。</span><span class="sxs-lookup"><span data-stu-id="db1cf-182">The secret is created and added to Key Vault.</span></span>

### <a name="register-the-app"></a><span data-ttu-id="db1cf-183">アプリを登録する</span><span class="sxs-lookup"><span data-stu-id="db1cf-183">Register the app</span></span>

1. <span data-ttu-id="db1cf-184">Azure ポータルで、**Azure Active Directory** を選択し、**アプリケーション登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-184">In the Azure portal, select **Azure Active Directory**, and then select **App registrations**.</span></span>
2. <span data-ttu-id="db1cf-185">メニュー上部の **新しいアプリケーション** を選択し、以下の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-185">Select **New registration** at the top of the menu, and enter the following information:</span></span>

    - <span data-ttu-id="db1cf-186">**名前** - アプリのフレンドリ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-186">**Name** - Enter a friendly name for the app.</span></span>
    - <span data-ttu-id="db1cf-187">ストレージ アカウントと Dynamics 環境が異なる Azure Active Directory ドメインにある場合を除き、**この組織ディレクトリのアカウントのみ** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="db1cf-187">Select **Accounts in this Organizational directory only** unless your storage account and your Dynamics environment are in different Azure Active Directory domains.</span></span>

3. <span data-ttu-id="db1cf-188">アプリケーションが作成されたら、**API のアクセス許可** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-188">After the application is created, select **API permissions**.</span></span>
4. <span data-ttu-id="db1cf-189">表示されるダイアログ ボックスで、**アクセス許可の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-189">In the dialog box that appears, select **Add a permission**.</span></span>
5. <span data-ttu-id="db1cf-190">API のリストを含むダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="db1cf-190">You will see a dialog box with a list of APIs.</span></span> <span data-ttu-id="db1cf-191">リストで **Azure Key Vault** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-191">In the list, select **Azure Key Vault**.</span></span>
6. <span data-ttu-id="db1cf-192">**委任されたアクセス許可** ボックスを選択し、**user_impersonation** を選択してから、**アクセス許可の追加** を選択して変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-192">Select the **Delegated permissions** box, select **user_impersonation**, and then select **Add permissions** to save your changes.</span></span>
7. <span data-ttu-id="db1cf-193">左側のナビゲーション ウィンドウで **証明書とシークレット** メニューを選択し、**新しいクライアント シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-193">Select the **Certificates & secrets** menu on the left navigation pane, and then select **New client secret**.</span></span>
8. <span data-ttu-id="db1cf-194">**説明** フィールドに、名前を入力し、有効機嫌を選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-194">In the **Description** field, enter a name and choose an expiry period.</span></span> <span data-ttu-id="db1cf-195">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-195">Select **Add**.</span></span>
10. <span data-ttu-id="db1cf-196">シークレットが生成され、**値** フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="db1cf-196">A secret is generated and shown in the **Value** field.</span></span>
11. <span data-ttu-id="db1cf-197">1、2 分以内に削除されるので、すぐにシークレットをクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="db1cf-197">Immediately copy the secret to the clipboard, because it will disappear within one or two minutes.</span></span> <span data-ttu-id="db1cf-198">後でアプリケーションにこのキーを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="db1cf-198">You will have to provide this key to the application later.</span></span>

### <a name="add-a-service-principal-to-key-vault"></a><span data-ttu-id="db1cf-199">サービス プリンシパルを Key Vault に追加する</span><span class="sxs-lookup"><span data-stu-id="db1cf-199">Add a service principal to Key Vault</span></span>

1. <span data-ttu-id="db1cf-200">Azure ポータルで、以前に作成した Key Vault を開きます。</span><span class="sxs-lookup"><span data-stu-id="db1cf-200">In the Azure portal, open Key Vault that you created earlier.</span></span>
2. <span data-ttu-id="db1cf-201">**アクセス ポリシー** を選択し、**追加** を選択して新しいアクセス許可ポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-201">Select **Access policies**, and then select **Add** to create a new access policy.</span></span>
3. <span data-ttu-id="db1cf-202">**プリンシパルの選択** フィールドに、以前に登録したアプリケーションの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-202">In the **Select principal** field, select the name of the application that you previously registered.</span></span>
4. <span data-ttu-id="db1cf-203">**キーのアクセス許可** フィールドで、**取得** および **リスト** のアクセス許可を選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-203">In the **Key permissions** field, select **Get** and **List** permissions.</span></span>
5. <span data-ttu-id="db1cf-204">**シークレットのアクセス許可** フィールドで、**取得** および **リスト** のアクセス許可を選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-204">In the **Secret permissions** field, select **Get** and **List** permissions.</span></span>

    ![取得およびリストのアクセス許可](./media/entity-store-data-lake-05.png)

6. <span data-ttu-id="db1cf-206">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-206">Select **Save**.</span></span>

## <a name="work-in-entity-store-in-a-data-lake"></a><span data-ttu-id="db1cf-207">Data Lake のエンティティ格納で作業する</span><span class="sxs-lookup"><span data-stu-id="db1cf-207">Work in Entity store in a Data Lake</span></span>

1. <span data-ttu-id="db1cf-208">**システム管理** \> **設定** \> **システム パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-208">Go to **System administration** \> **Set up** \> **System parameters**.</span></span>
2. <span data-ttu-id="db1cf-209">**データ接続** タブで、このトピックの前の部分でメモした次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-209">On the **Data connections** tab, enter the following information that you made a note of earlier in this topic:</span></span>

    - <span data-ttu-id="db1cf-210">**アプリケーション ID:** 前に登録した Azure AD アプリケーションのアプリケーション ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-210">**Application ID:** Enter the application ID of the Azure AD application that you registered earlier.</span></span>
    - <span data-ttu-id="db1cf-211">**アプリケーション シークレット:** Azure AD アプリケーションのアプリケーション キー (秘密) を入力します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-211">**Application Secret:** Enter the application key (secret) for the Azure AD application.</span></span>
    - <span data-ttu-id="db1cf-212">**DNS 名:** Key Vault の DNS 名を入力します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-212">**DNS name:** Enter the DNS name of Key Vault.</span></span>
    - <span data-ttu-id="db1cf-213">**シークレット名:** 接続文字列情報と共に Key Vault に追加したシークレットの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-213">**Secret name:** Enter the name of the secret that you added to Key Vault together with connection string information.</span></span>

    ![[システム パラメーター] ページの [データ接続] タブ](./media/entity-store-data-lake-04.png)

3. <span data-ttu-id="db1cf-215">**Azure Key Vault のテスト** および **Azure Storage のテスト** リンクを選択し、指定した構成情報にシステムがアクセスできることを検証します。</span><span class="sxs-lookup"><span data-stu-id="db1cf-215">Select the **Test Azure Key Vault** and **Test Azure Storage** links to validate that system can access the configuration information that you provided.</span></span>
4. <span data-ttu-id="db1cf-216">**データ接続を有効にする** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="db1cf-216">Select the **Enable data connection** check box.</span></span>

<span data-ttu-id="db1cf-217">エンティティ格納データが、リレーショナル エンティティ格納データベースではなく、指定したストレージ場所に入力されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="db1cf-217">Entity store data should now be populated in the storage location that you provided, not in the relational Entity store database.</span></span>

<span data-ttu-id="db1cf-218">集計の測定と、エンティティ格納 UI で選択した更新オプションが、Data Lake にコピーされたデータに適用されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="db1cf-218">The aggregate measurements and refresh options that you select in the Entity store UI should now apply to data that is copied to Data Lake.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]