---
title: Azure Data Lake の Finance and Operations アプリ データ
description: このトピックでは、Data Lakeを実装した Finance and Operations アプリ環境の設定方法を説明します。
author: MilindaV2
manager: AnnBe
ms.date: 03/30/2020
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
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Platform Update 34
ms.openlocfilehash: ee5ad6d1ed6820f9fa30ef7cf3f451ce3490eed6
ms.sourcegitcommit: 88347d0f0ac862a77f269a05f1801d30dc93586e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2020
ms.locfileid: "3260242"
---
# <a name="finance-and-operations-apps-data-in-azure-data-lake"></a><span data-ttu-id="9b813-103">Azure Data Lake の Finance and Operations アプリ データ</span><span class="sxs-lookup"><span data-stu-id="9b813-103">Finance and Operations apps data in Azure Data Lake</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="9b813-104">**Azure Data Lake にエクスポート** 機能を使用すると、Finance and Operations アプリ環境で Data Lake を使用するように構成することができます。</span><span class="sxs-lookup"><span data-stu-id="9b813-104">The **Export to Azure Data Lake** feature lets you configure your Finance and Operations apps environment so that it uses a data lake.</span></span> <span data-ttu-id="9b813-105">構成が完了すると、Data Lake には Finance and Operations アプリのテーブルとエンティティが反映されます。</span><span class="sxs-lookup"><span data-stu-id="9b813-105">After the configuration is completed, your data lake will reflect tables and entities from Finance and Operations apps.</span></span>

> [!NOTE]
> - <span data-ttu-id="9b813-106">**この機能は、すべての地域またはすべての環境で使用できるわけではありません。**</span><span class="sxs-lookup"><span data-stu-id="9b813-106">**This feature might not be available in all regions and/or all environments.**</span></span> <span data-ttu-id="9b813-107">この機能がご利用の環境で表示されない場合、当機能は未対応です。</span><span class="sxs-lookup"><span data-stu-id="9b813-107">If you don't see this feature in your environment, it isn't available yet.</span></span>
> - <span data-ttu-id="9b813-108">Data Lakeで集計測定を使用できるようにするには、[エンティティ ストアを Data Lake として使用可能とする](entity-store-data-lake.md)で説明されている方法でこの機能を引き続き使用します。</span><span class="sxs-lookup"><span data-stu-id="9b813-108">To make aggregate measurements available in a data lake, continue to use the feature in the manner that is described in [Make entity store available as a Data Lake](entity-store-data-lake.md).</span></span>

## <a name="overview"></a><span data-ttu-id="9b813-109">概要</span><span class="sxs-lookup"><span data-stu-id="9b813-109">Overview</span></span>

<span data-ttu-id="9b813-110">このサービスを利用可能とするプロセスには、いくつかの手順があります。</span><span class="sxs-lookup"><span data-stu-id="9b813-110">The process of making this service available has several steps.</span></span>

1. <span data-ttu-id="9b813-111">サブスクリプションに Microsoft Azure Data Lake Storage Gen2 アカウント (ストレージアカウント) を作成します。</span><span class="sxs-lookup"><span data-stu-id="9b813-111">Create a Microsoft Azure Data Lake Storage Gen2 account (a storage account) in your subscription.</span></span>
2. <span data-ttu-id="9b813-112">Azure Data Lake 統合を有効にするには、利用規約に同意してください。</span><span class="sxs-lookup"><span data-stu-id="9b813-112">Accept the offer and terms to turn on the Azure Data Lake integration.</span></span>
3. <span data-ttu-id="9b813-113">**Azure Data Lake へのエクスポート** 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="9b813-113">Turn on the **Export to Azure Data Lake** feature.</span></span>
4. <span data-ttu-id="9b813-114">データ（Data Lake にステージングする必要のあるテーブルとエンティティ）を選択します 。</span><span class="sxs-lookup"><span data-stu-id="9b813-114">Select data (that is, the tables and entities that should be staged in Data Lake).</span></span>
5. <span data-ttu-id="9b813-115">Data Lake のテーブルを監視します。</span><span class="sxs-lookup"><span data-stu-id="9b813-115">Monitor the tables in Data Lake.</span></span>

## <a name="create-a-data-lake-storage-gen2-account-in-your-subscription"></a><span data-ttu-id="9b813-116">サブスクリプションに Data Lake ストレージ（Gen2）を作成します</span><span class="sxs-lookup"><span data-stu-id="9b813-116">Create a Data Lake Storage (Gen2) account in your subscription</span></span>

<span data-ttu-id="9b813-117">ストレージ アカウントはデータの格納に使用されます。</span><span class="sxs-lookup"><span data-stu-id="9b813-117">The storage account will be used to store data.</span></span> <span data-ttu-id="9b813-118">ストレージ アカウントを手動で作成するには、Azure サブスクリプションに対して管理者権限を持つユーザーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b813-118">To manually create a storage account, you must be a user who has administrative rights to your organization's Azure subscription.</span></span> <span data-ttu-id="9b813-119">（最終的には、システムがユーザーに代わって自身の Azure サブスクリプションにストレージ アカウントを作成することができます）</span><span class="sxs-lookup"><span data-stu-id="9b813-119">(Eventually, the system will be able to create a storage account in your own Azure subscription on your behalf.)</span></span>

### <a name="manually-create-a-storage-account"></a><span data-ttu-id="9b813-120">ストレージ アカウントの手動作成</span><span class="sxs-lookup"><span data-stu-id="9b813-120">Manually create a storage account</span></span>

<span data-ttu-id="9b813-121">ご利用の Azure サブスクリプションにストレージ アカウントを作成し、Key Vault を使用してそのアカウントをシステムに提供することができます。</span><span class="sxs-lookup"><span data-stu-id="9b813-121">You can create a storage account in your own Azure subscription and use a key vault to provide that account to the system.</span></span> <span data-ttu-id="9b813-122">続いて、ストレージ アカウントのルートへのアクセスを許可するAzure Active Directory (Azure AD) のアプリケーション ID を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b813-122">Next, you must create an Azure Active Directory (Azure AD) application ID that grants access to the root of your storage account.</span></span> <span data-ttu-id="9b813-123">システムでは、Azure AD アプリケーションを使用して、フォルダ構造の作成とデータの書き込みを行います。</span><span class="sxs-lookup"><span data-stu-id="9b813-123">The system will use the Azure AD application to create the folder structure and write data.</span></span> <span data-ttu-id="9b813-124">最後に、サブスクリプションに Key Vault を作成し、ストレージ アカウントに関する情報と、Microsoft Dynamics Lifecycle Services (LCS) の Data Lake 条件に同意してください。</span><span class="sxs-lookup"><span data-stu-id="9b813-124">Finally, you will create a key vault in your subscription, and provide information about your storage account and the application to the Data Lake offer in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="9b813-125">ストレージ アカウントを作成する。</span><span class="sxs-lookup"><span data-stu-id="9b813-125">Create a storage account.</span></span> <span data-ttu-id="9b813-126">手順については、[ストレージ アカウントの作成](entity-store-data-lake.md#create-storage-accounts) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b813-126">For instructions, see [Create storage accounts](entity-store-data-lake.md#create-storage-accounts).</span></span>
2. <span data-ttu-id="9b813-127">ご利用の Azure AD 環境のテナント ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="9b813-127">Provide the Azure AD tenant ID of your environment.</span></span> <span data-ttu-id="9b813-128">Azure AD テナント ID は Azure ポータルで確認できます。</span><span class="sxs-lookup"><span data-stu-id="9b813-128">You can find your Azure AD tenant ID in the Azure portal.</span></span> <span data-ttu-id="9b813-129">Azure portal にログインし、**Azure Active Directory** サービスを開きます。</span><span class="sxs-lookup"><span data-stu-id="9b813-129">Sign in to the Azure portal, and open the **Azure Active Directory** service.</span></span> <span data-ttu-id="9b813-130">**プロパティ** ページを開き、**ディレクトリ ID** フィールドの値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="9b813-130">Open the **Properties** page, and copy the value in the **Directory ID** field.</span></span>
3. <span data-ttu-id="9b813-131">Key Vault とシークレットを作成します。</span><span class="sxs-lookup"><span data-stu-id="9b813-131">Create a key vault and a secret.</span></span> <span data-ttu-id="9b813-132">手順については、 [Key Vault とシークレットを作成する](entity-store-data-lake.md#create-a-key-vault-and-a-secret)。</span><span class="sxs-lookup"><span data-stu-id="9b813-132">For instructions, see [Create a key vault and a secret](entity-store-data-lake.md#create-a-key-vault-and-a-secret).</span></span> <span data-ttu-id="9b813-133">Key Vault のドメイン名システム (DNS) 名と秘密名を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b813-133">You must provide the key vault's Domain Name System (DNS) name and the secret name.</span></span>

<!--### Let the system create a storage account -->

<!--Instead of manually creating a storage account, you can have the system create a storage account in your own subscription on your behalf. This option will be made available in a future release. -->

## <a name="accept-the-offer-and-terms-to-turn-on-the-data-lake-integration"></a><span data-ttu-id="9b813-134">Data Lake 統合を有効にするには、利用規約に同意してください</span><span class="sxs-lookup"><span data-stu-id="9b813-134">Accept the offer and terms to turn on the Data Lake integration</span></span>

<span data-ttu-id="9b813-135">Data Lake 統合を構成するには、LCS の Data Lake の規約に同意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b813-135">Before you can configure the Data Lake integration, you must accept the Data Lake offer in LCS.</span></span> <span data-ttu-id="9b813-136">このタスクを完了するには、Finance and Operations アプリの環境管理者である必要があります。また、LCS ポータルにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b813-136">To complete this task, you must be an environment admin for Finance and Operations apps, and you must have access to the LCS portal.</span></span>

1. <span data-ttu-id="9b813-137">[LCS](https://lcs.dynamics.com) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="9b813-137">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
2. <span data-ttu-id="9b813-138">**環境** ページで、**環境のアドイン** クイック タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="9b813-138">On the **Environment** page, select the **Environment add-ins** FastTab.</span></span> <span data-ttu-id="9b813-139">**Azure Data Lake** が一覧に表示されている場合は、Data Lake アドインが既にインストールされているため、この手順の残りの部分は省略できます。</span><span class="sxs-lookup"><span data-stu-id="9b813-139">If **Azure Data Lake** appears in the list, the Data Lake add-in is already installed, and you can skip the rest of this procedure.</span></span> <span data-ttu-id="9b813-140">それ以外の場合は、残りの手順に従って Data Lake アドインをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="9b813-140">Otherwise, follow the remaining steps to install the Data Lake add-in.</span></span>

    ![Data Lake アドインがインストールされていることを確認する](./media/LCS-EnvironmentPage-with-Addins.png)

3. <span data-ttu-id="9b813-142">**新しいアドインのインストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b813-142">Select **Install a new add-in**.</span></span>
4. <span data-ttu-id="9b813-143">**インストールするアドインの選択**ダイアログ ボックスで、一覧から **Azure Data lake** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b813-143">In the **Select an add-in to install** dialog box, select **Azure Data lake** in the list.</span></span> <span data-ttu-id="9b813-144">表示されない場合は、環境に対して当機能が未対応となっている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9b813-144">If it isn't listed, the feature might not yet be available for your environment.</span></span>

    ![Azure Data Lake のオプションを選択する](./media/LCS-EnvironmentPage-with-DataLake-Flyover.png)

5. <span data-ttu-id="9b813-146">**設定のアドイン** ダイアログ ボックスで、必要な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="9b813-146">In the **Setup add-in** dialog box, provide the required information.</span></span> <span data-ttu-id="9b813-147">質問に答えるには、既にストレージ アカウントが作成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b813-147">To answer the questions, you must already have a storage account.</span></span> <span data-ttu-id="9b813-148">ストレージ アカウントをまだ持っていない場合は、作成するか、管理者にアカウントの作成代行を依頼してください。</span><span class="sxs-lookup"><span data-stu-id="9b813-148">If you don't already have a storage account, create one, or ask your admin to create one on your behalf.</span></span>

    ![Data Lake アドインの詳細を入力する](./media/azure-data-lake-addin.png)

6. <span data-ttu-id="9b813-150">チェック ボックスをオンにしてサービス条件を承認し、**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b813-150">Accept the terms of the offer by selecting the check box, and then select **Install**.</span></span>

<span data-ttu-id="9b813-151">システムが、ご利用の環境に Data Lake をインストールし構成します。</span><span class="sxs-lookup"><span data-stu-id="9b813-151">The system installs and configures the data lake for the environment.</span></span> <span data-ttu-id="9b813-152">インストールと構成が完了すると、 **環境** のページに **Azure Data Lake** の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9b813-152">After installation and configuration are completed, you should see **Azure Data Lake** listed on the **Environment** page.</span></span>

## <a name="turn-on-the-export-data-to-azure-data-lake-feature"></a><span data-ttu-id="9b813-153">Azure Data Lake へのデータのエクスポート機能を有効にします</span><span class="sxs-lookup"><span data-stu-id="9b813-153">Turn on the Export Data to Azure Data Lake feature</span></span>

<span data-ttu-id="9b813-154">Finance and Operations アプリのすべての新機能については、管理者は事前に **Azure Data Lake へのエクスポート** 機能を有効化しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b813-154">As for all new features in Finance and Operations apps, an admin must turn on the **Export to Azure Data Lake** feature before it can be activated.</span></span>

- <span data-ttu-id="9b813-155">**機能の管理** ワークスペースにて、**Azure Data Lake にデータをエクスポート** 機能を選択し、**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b813-155">In the **Feature management** workspace, find and select the **Export Data to Azure Data lake** feature, and then select **Enable**.</span></span>

<span data-ttu-id="9b813-156">この機能を有効にすると、**システムの管理** の配下に **Azure Data Lake にエクスポートする** オプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9b813-156">After the feature is turned on, you should see the **Export to Azure Data Lake** option under **System administration**.</span></span>

## <a name="select-data"></a><span data-ttu-id="9b813-157">データの選択</span><span class="sxs-lookup"><span data-stu-id="9b813-157">Select data</span></span>

<span data-ttu-id="9b813-158">Data Lake にステージングする必要のあるテーブルとエンティティを選択することができます 。</span><span class="sxs-lookup"><span data-stu-id="9b813-158">You can select the tables and entities that should be staged in Data Lake.</span></span>

1. <span data-ttu-id="9b813-159">ご利用の環境で、**システム管理** \> **Azure Data Lake にエクスポートする** へと移動します。</span><span class="sxs-lookup"><span data-stu-id="9b813-159">In your environment, go to **System Administration** \> **Export to Azure Data Lake**.</span></span>
2. <span data-ttu-id="9b813-160">**Data Lake にエクスポートするデータフィードの構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b813-160">Select **Configure Data feeds for export to Lake**.</span></span>
3. <span data-ttu-id="9b813-161">**Data Lakeへのデータフィードの構成** ページの **テーブルの選択** ページで、Data Lake にステージングするデータ テーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="9b813-161">On the **Configure data feeds to Data lake** page, on the **Choose Tables** tab, select the data tables that should be staged in Data Lake.</span></span> <span data-ttu-id="9b813-162">テーブルは、表示名またはシステム名で検索できます。</span><span class="sxs-lookup"><span data-stu-id="9b813-162">You can search for tables by display name or system name.</span></span> <span data-ttu-id="9b813-163">テーブルが既に同期されているかどうかを確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="9b813-163">You can also see whether a table is already being synced.</span></span> <span data-ttu-id="9b813-164">完了後に、**テーブルの追加** を選択し、選択したテーブルを Data Lake に追加します。</span><span class="sxs-lookup"><span data-stu-id="9b813-164">When you've finished, select **Add Tables** to add the selected tables to Data Lake.</span></span>

    ![テーブルの選択](./media/Export-Tables-toData-lake-unselected.png)

    <span data-ttu-id="9b813-166">また、必要な特定のテーブルについて詳しくない場合は、エンティティを使用してテーブルを選択できます。</span><span class="sxs-lookup"><span data-stu-id="9b813-166">Alternatively, if you aren't familiar with the specific tables that you require, you can select tables by using entities.</span></span> <span data-ttu-id="9b813-167">エンティティはデータの抽象度が高く、複数のテーブルを含む場合があります。</span><span class="sxs-lookup"><span data-stu-id="9b813-167">Entities are a higher-level abstraction of data and might include multiple tables.</span></span> <span data-ttu-id="9b813-168">エンティティを選択することで、それを構成するテーブルも選択することになります。</span><span class="sxs-lookup"><span data-stu-id="9b813-168">By selecting entities, you're also selecting the tables that comprise them.</span></span>
    
    - <span data-ttu-id="9b813-169">**使用するエンティティの選択** タブでエンティティを選択し、**エンティティを使用してテーブルを追加する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b813-169">On the **Choose using Entities** tab, select entities, and then select **Add Tables using Entities**.</span></span>

    ![エンティティを使用したテーブルの選択](./media/Export-Entities-toData-lake-unselected.png)

    <span data-ttu-id="9b813-171">テーブルを選択する方法を問わず、Data Lake ではテーブルがステージングされます。</span><span class="sxs-lookup"><span data-stu-id="9b813-171">Regardless of the method that you use to select tables, the tables will be staged in Data Lake.</span></span>

## <a name="monitor-the-tables-in-data-lake"></a><span data-ttu-id="9b813-172">Data Lake のテーブルを監視する</span><span class="sxs-lookup"><span data-stu-id="9b813-172">Monitor the tables in Data Lake</span></span>

<span data-ttu-id="9b813-173">システムが Data Lake でデータの更新を維持しているため、データのエクスポートの監視や、スケジュールを設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="9b813-173">You don't have to monitor or schedule data exports, because the system keeps the data updated in Data Lake.</span></span> <span data-ttu-id="9b813-174">ただし、**Data Lake へのデータフィードの設定** ページの **アクティブ** タブで、進行中のデータ エクスポートの状態を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="9b813-174">However, you can view the status of ongoing data exports on the **Active** tab of the **Configure data feeds to Data lake** page.</span></span>

![テーブルの監視の進行状況](./media/Export-Tables-toData-lake-monitor.png)
