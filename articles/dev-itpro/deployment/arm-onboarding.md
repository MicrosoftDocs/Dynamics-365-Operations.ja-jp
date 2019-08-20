---
title: Azure Resource Manager (ARM) の研修プロセスを完了します。
description: このトピックでは、コネクタの Azure Resource Manager (ARM) 登録プロセスを完了する方法について説明します。
author: sarvanisathish
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 141093
ms.assetid: dcd23629-246d-4fbc-adf5-7245bb2121e4
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: d62fdafb8b9cc7713a609b36aab0eedc77b5ff90
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862918"
---
# <a name="complete-the-azure-resource-manager-arm-onboarding-process"></a><span data-ttu-id="31ef7-103">Azure Resource Manager (ARM) の研修プロセスを完了します。</span><span class="sxs-lookup"><span data-stu-id="31ef7-103">Complete the Azure Resource Manager (ARM) onboarding process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31ef7-104">このトピックでは、コネクタの Azure Resource Manager (ARM) 登録プロセスを完了する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="31ef7-104">This topic explains how to complete the Azure Resource Manager (ARM) onboarding process for your connectors.</span></span> 

<span data-ttu-id="31ef7-105">Microsoft Dynamics 365 for Operations プラットフォーム 更新プログラム 2 (2016 年 8 月) を含む Microsoft Azure Resource Manager (ARM) トポロジを配置するには、ユーザーのコネクタのために ARM 研修プロセスを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31ef7-105">To deploy Microsoft Azure Resource Manager (ARM) topologies, which include Microsoft Dynamics 365 for Operations Platform update 2 (August 2016), you must complete the ARM onboarding process for your connectors.</span></span> <span data-ttu-id="31ef7-106">オンボード プロセスを開始するには、次の項目が必要です。</span><span class="sxs-lookup"><span data-stu-id="31ef7-106">To start the onboarding process, you must have the following items:</span></span>

-   <span data-ttu-id="31ef7-107">展開する Azure サブスクリプション ID</span><span class="sxs-lookup"><span data-stu-id="31ef7-107">The Azure subscription ID that you're deploying to</span></span>
-   <span data-ttu-id="31ef7-108">Azure サブスクリプションの所有権、またはサブスクリプション所有者へのアクセス。共同作成者ワークフロー、およびアップロード管理証明書を追加できるようにします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-108">Ownership of the Azure subscription, or access to the subscription owner, so that you can add contributor workflows, and the Upload Management certificate</span></span>
-   <span data-ttu-id="31ef7-109">テナント管理者が管理者同意ワークフローを実行する</span><span class="sxs-lookup"><span data-stu-id="31ef7-109">The tenant administrator, to work through the admin consent workflow</span></span>

## <a name="arm-onboarding-process"></a><span data-ttu-id="31ef7-110">ARM 研修プロセス</span><span class="sxs-lookup"><span data-stu-id="31ef7-110">ARM onboarding process</span></span>
<span data-ttu-id="31ef7-111">ARM オンボードは、各ステップに独自のサブ手順がある、2 ステップ手順とみなすことできます。</span><span class="sxs-lookup"><span data-stu-id="31ef7-111">You can consider ARM onboarding a two-step procedure, where each step has its own sub-procedures.</span></span> <span data-ttu-id="31ef7-112">Microsoft Dynamics Lifecycle Services (LCS) プロジェクトに追加するすべてのサブスクリプションに対してこれらすべてのを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31ef7-112">You must complete all these procedures for every subscription that you add to the Microsoft Dynamics Lifecycle Services (LCS) project.</span></span>

1.  <span data-ttu-id="31ef7-113">Azure サブスクリプションで作業を行う LCS 配置サービス (DSU) を承認します。</span><span class="sxs-lookup"><span data-stu-id="31ef7-113">Authorize the LCS Deployment Service (DSU) to work on the Azure subscription.</span></span>
    1.  <span data-ttu-id="31ef7-114">ワークフローを認証します。</span><span class="sxs-lookup"><span data-stu-id="31ef7-114">Authorize the workflow.</span></span>
    2.  <span data-ttu-id="31ef7-115">投稿者ワークフローを設定します。</span><span class="sxs-lookup"><span data-stu-id="31ef7-115">Set the contributor workflow.</span></span>

2.  <span data-ttu-id="31ef7-116">ARM リソースを配置する Azure サブスクリプションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-116">Enable the Azure subscription to deploy ARM resources.</span></span>
    1.  <span data-ttu-id="31ef7-117">Azure コネクタを有効にし、LCS ユーザーを追加にします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-117">Enable the Azure connector, and add an LCS user.</span></span>
    2.  <span data-ttu-id="31ef7-118">オプション: 管理証明書をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-118">Optional: Upload the Management certificate.</span></span>
    3.  <span data-ttu-id="31ef7-119">配置設定をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-119">Configure deployment settings.</span></span>

### <a name="authorize-the-lcs-dsu-to-work-on-the-azure-subscription"></a><span data-ttu-id="31ef7-120">Azure サブスクリプションで作業を行う LCS DSU を承認する</span><span class="sxs-lookup"><span data-stu-id="31ef7-120">Authorize the LCS DSU to work on the Azure subscription</span></span>

<span data-ttu-id="31ef7-121">Azure サブスクリプションで動作するよう LCS DSU を承認するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="31ef7-121">Complete the following procedures to authorize the LCS DSU to work on the Azure subscription.</span></span>

#### <a name="authorize-the-workflow"></a><span data-ttu-id="31ef7-122">ワークフローを認証する</span><span class="sxs-lookup"><span data-stu-id="31ef7-122">Authorize the workflow</span></span>

<span data-ttu-id="31ef7-123">テナントの管理者は、次の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31ef7-123">The administrator of the tenant must complete the following procedure.</span></span>

1.  <span data-ttu-id="31ef7-124">LCS で、**プロジェクト** ページの **環境** セクションにある **Microsoft Azure 設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-124">In LCS, on the **Project** page, in the **Environments** section, click **Microsoft Azure settings**.</span></span>
2.  <span data-ttu-id="31ef7-125">**プロジェクト設定**ページでは、**Azure コネクタ**タブの、**組織リスト**グループで、**承認**をクリックして ARM 貢献者ワークフローを開始します。</span><span class="sxs-lookup"><span data-stu-id="31ef7-125">On the **Project settings** page, on the **Azure connectors** tab, in the **Organization list** group, click **Authorize** to start the ARM Contributor workflow.</span></span> <span data-ttu-id="31ef7-126">このワークフローでは、DSU のアクセス許可が設定されるため、DSU を自分の代わりにサブスクリプションに展開できます。</span><span class="sxs-lookup"><span data-stu-id="31ef7-126">This workflow sets up permissions for the DSU, so that it can deploy to your subscription on your behalf.</span></span>
3.  <span data-ttu-id="31ef7-127">**管理者の同意の付与**ページで、**承認**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-127">On the **Grant admin consent** page, click **Authorize**.</span></span> <span data-ttu-id="31ef7-128">次に、接続する Azure サブスクリプションの管理者アカウントを使用してサインインし、**承諾** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-128">Then sign in by using the administrator account of the Azure subscription that you must connect to, and click **Accept**.</span></span> <span data-ttu-id="31ef7-129">これで、承認が完了として表示されます。</span><span class="sxs-lookup"><span data-stu-id="31ef7-129">The authorization is now shown as completed.</span></span>

#### <a name="set-the-contributor-workflow"></a><span data-ttu-id="31ef7-130">投稿者ワークフローを設定</span><span class="sxs-lookup"><span data-stu-id="31ef7-130">Set the contributor workflow</span></span>

<span data-ttu-id="31ef7-131">**寄稿者**ロールを **Dynamics 配置サービス \[wsfed 有効 \]** アプリケーションに割り当てるため、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="31ef7-131">Follow these steps to assign the **Contributor** role to the **Dynamics Deployment Services \[wsfed-enabled\]** application.</span></span>

1.  <span data-ttu-id="31ef7-132">[Azure ポータル](https://portal.azure.com)の**サブスクリプション** タブで、Azure サブスクリプションを選択してから**アクセス制御 (IAM)** 行項目をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-132">In the [Azure portal](https://portal.azure.com), on the **Subscription** tab, select the Azure subscription, and then click the **Access Control (IAM)** line item.</span></span>
2.  <span data-ttu-id="31ef7-133">**Add** をクリックして **ロール割り当ての追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31ef7-133">Click **Add**, select **Add role assignment**.</span></span> <span data-ttu-id="31ef7-134">ダイアログ ボックスで、**ロール** を **貢献者** に、**アクセス権の割り当て先** を **Azure AD ユーザー、グループ、サービス プリンシパル** に設定します。</span><span class="sxs-lookup"><span data-stu-id="31ef7-134">In the dialog box, set **Role** to **Contributor** and set **Assign access to** to **Azure AD user, group, or service principal**.</span></span> <span data-ttu-id="31ef7-135">**選択** フィールドで **Dynamics 配置サービス \[wsfed 有効\]** を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="31ef7-135">In the **Select** field, search for and select **Dynamics Deployment Services \[wsfed-enabled\]**.</span></span> <span data-ttu-id="31ef7-136">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31ef7-136">Select **Save**.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="31ef7-137">一部の Azure サブスクリプションには **アクセス制御 (IAM)** セクションではなく **ユーザー** セクションがあります。</span><span class="sxs-lookup"><span data-stu-id="31ef7-137">Some Azure subscriptions have a **Users** section instead of an **Access control (IAM)** section.</span></span> <span data-ttu-id="31ef7-138">この場合、**ユーザーの追加** ダイアログ ボックスの **選択** フィールドに、**Dynamics 配置サービス \[wsfed 有効\]** と入力して **選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31ef7-138">In this case, in the **Add users** dialog box, in the **Select** field, enter **Dynamics Deployment Services \[wsfed-enabled\]**, and then select **Select**.</span></span>
    
<span data-ttu-id="31ef7-139">[![Dynamics 配置サービス \[wsfed 有効\]](./media/arm_redo_02.png)](./media/arm_redo_02.png)</span><span class="sxs-lookup"><span data-stu-id="31ef7-139">[![Dynamics Deployment Services \[wsfed-enabled\]](./media/arm_redo_02.png)](./media/arm_redo_02.png)</span></span>

3.  <span data-ttu-id="31ef7-140">**ロールの割り当て** タブで、アプリは **貢献者** として割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="31ef7-140">On the **Role assignments** tab, the App is assigned as a **Contributor**.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="31ef7-141">Dynamics 配置サービス \[wsfed 有効\] が表示されない場合、承認プロセスは完了していないか、別の Azure サブスクリプションで完了しています。</span><span class="sxs-lookup"><span data-stu-id="31ef7-141">If Dynamics Deployment Services \[wsfed-enabled\] doesn't appear, the authorize process hasn't been completed, or it was completed on another Azure subscription.</span></span> 

### <a name="enable-the-azure-subscription-to-deploy-arm-resources"></a><span data-ttu-id="31ef7-142">ARM リソースを配置する Azure サブスクリプションの有効化</span><span class="sxs-lookup"><span data-stu-id="31ef7-142">Enable the Azure subscription to deploy ARM resources</span></span>

<span data-ttu-id="31ef7-143">Azure サブスクリプションを有効にして ARM リソースを展開できるようにするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="31ef7-143">Complete the following procedures to enable the Azure subscription to deploy ARM resources.</span></span>

#### <a name="enable-the-azure-connector-and-add-an-lcs-user"></a><span data-ttu-id="31ef7-144">Azure コネクタを有効、および LCS ユーザーを追加</span><span class="sxs-lookup"><span data-stu-id="31ef7-144">Enable the Azure connector and add an LCS user</span></span>

<span data-ttu-id="31ef7-145">Azure コネクタを有効にし、必要に応じて LCS ユーザーを追加するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="31ef7-145">Follow these steps to enable the Azure Connector and, as required, add an LCS user.</span></span>

1.  <span data-ttu-id="31ef7-146">LCS で、**プロジェクト** ページの **環境** セクションにある **Microsoft Azure 設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-146">In LCS, on the **Project** page, in the **Environments** section, click **Microsoft Azure settings**.</span></span>
2.  <span data-ttu-id="31ef7-147">**プロジェクト設定**ページでは、**Azure コネクタ**タブで、**Azure コネクタ**の**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-147">On the **Project settings** page, on the **Azure connectors** tab, under **Azure connectors**, click **Add**.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="31ef7-148">既存のコネクタで ARM を有効にしている場合は、**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-148">If you're enabling ARM for an existing connector, click **Edit**.</span></span>
3.  <span data-ttu-id="31ef7-149">コネクタ名および配置する Azure サブスクリプション ID を入力し、**Azure Resource Manager を使用するコンフィギュレーション**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="31ef7-149">Enter the connector name, enter the Azure subscription ID to deploy to, and set the **Configure to use Azure Resource manager** option to **Yes**.</span></span>
4.  <span data-ttu-id="31ef7-150">**Azure サブスクリプション AAD テナント ドメイン** フィールドで、Azure サブスクリプション アカウント管理者のドメイン名を入力してから**次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-150">In the **Azure subscription AAD Tenant domain** field, enter the domain name of the Azure subscription account admin, and then click **Next**.</span></span>
5.  <span data-ttu-id="31ef7-151">Azure サブスクリプションに LCS ユーザーを追加するか管理証明書を使用して、サブスクリプションへのアクセスを認証します。</span><span class="sxs-lookup"><span data-stu-id="31ef7-151">Authorize access to the subscription, either by adding the LCS user to the Azure subscription or by using the Management certificate.</span></span> <span data-ttu-id="31ef7-152">**重要:** LCS ユーザーを追加する場合は、手順 6 に進みます。</span><span class="sxs-lookup"><span data-stu-id="31ef7-152">**Important:** If you're adding an LCS user, continue with step 6.</span></span> <span data-ttu-id="31ef7-153">管理証明書をアップロードする必要がある場合は、この手順のステップ 6 から 8 を実行しないようにします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-153">If you must upload a Management certificate, don't complete steps 6 through 8 of this procedure.</span></span> <span data-ttu-id="31ef7-154">代わりに、「管理証明書のアップロード」という次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="31ef7-154">Instead, complete the next procedure, "Upload the Management certificate."</span></span>
6.  <span data-ttu-id="31ef7-155">[Azure ポータル](https://portal.azure.com)の**サブスクリプション** タブで、Azure サブスクリプションを選択してから**アクセス制御 (IAM)** 行項目をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-155">In the [Azure portal](https://portal.azure.com), on the **Subscription** tab, select the Azure subscription, and then click the **Access Control (IAM)** line item.</span></span>
7.  <span data-ttu-id="31ef7-156">**アクセス制御 (IAM)** ダイアログ ボックスで、**追加**をクリックし、**寄稿者**を選択してから、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-156">In the **Access Control (IAM)** dialog box, click **Add**, select **Contributor**, and then click **OK**.</span></span>
8.  <span data-ttu-id="31ef7-157">**ユーザーの追加**ダイアログ ボックスの**選択**フィールドで、LCS ユーザーを入力してから Enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="31ef7-157">In the **Add users** dialog box, in the **Select** field, enter the LCS user, and then press Enter.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="31ef7-158">ユーザーを明確に入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31ef7-158">You must specifically enter a user.</span></span> <span data-ttu-id="31ef7-159">ユーザーがメンバーであるグループを追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="31ef7-159">You can't just add a group that the user is a member of.</span></span> <span data-ttu-id="31ef7-160">**ユーザー** ページが開いたとき、ユーザーが **寄稿者** として割り当てられていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="31ef7-160">When the **Users** page opens, you can see that the user is assigned as a **Contributor**.</span></span>

#### <a name="upload-the-management-certificate"></a><span data-ttu-id="31ef7-161">管理証明書のアップロード</span><span class="sxs-lookup"><span data-stu-id="31ef7-161">Upload the Management certificate</span></span>

<span data-ttu-id="31ef7-162">前の手順「Azure コネクタを有効にし LCS ユーザーを追加する」の手順 6 から 8 を完了していない場合にのみ、この手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="31ef7-162">Complete this procedure only if you didn't complete steps 6 through 8 of the previous procedure, "Enable the Azure Connector and add an LCS user."</span></span>

1.  <span data-ttu-id="31ef7-163">LCS で、**Microsoft Azure 設定** ページの **ダウンロード** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-163">In LCS, on the **Microsoft Azure setup** page, click **Download**.</span></span> <span data-ttu-id="31ef7-164">証明書ファイルをダウンロードした場所をメモしておきます。</span><span class="sxs-lookup"><span data-stu-id="31ef7-164">Make a note of the location of the certificate file that is downloaded.</span></span> <span data-ttu-id="31ef7-165">この情報を使用して、証明書を Azure サブスクリプションにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-165">You will use this information to upload the certificate to the Azure subscription.</span></span>
2.  <span data-ttu-id="31ef7-166">[Azure クラシック ポータル](https://manage.windowsazure.com/)の左ウィンドウで**設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-166">In the [Azure classic portal](https://manage.windowsazure.com/), in the left pane, click **Settings**.</span></span>
3.  <span data-ttu-id="31ef7-167">使用する Azure サブスクリプションへフィルター処理をし、次に、**管理証明書**タブで、**アップロード**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-167">Filter to the Azure subscription that is used, and then, on the **Management certificates** tab, click **Upload**.</span></span>
4.  <span data-ttu-id="31ef7-168">手順 1 でダウンロードした管理証明書を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-168">Select the Management certificate that you downloaded in step 1, and then click **OK**.</span></span>

#### <a name="configure-deployment-settings"></a><span data-ttu-id="31ef7-169">配置設定のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="31ef7-169">Configure deployment settings</span></span>

1.  <span data-ttu-id="31ef7-170">LCS で、**プロジェクト** ページの **環境** セクションにある **Microsoft Azure 設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-170">In LCS, on the **Project** page, in the **Environments** section, click **Microsoft Azure settings**.</span></span>
2.  <span data-ttu-id="31ef7-171">**Microsoft Azure 設定** ページで、配置する地域を選択してから、**接続** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31ef7-171">On the **Microsoft Azure setup** page, select the region to deploy to, and then click **Connect**.</span></span> <span data-ttu-id="31ef7-172">ARM オンボーディング フローが完了しました。</span><span class="sxs-lookup"><span data-stu-id="31ef7-172">The ARM onboarding flow is now completed.</span></span> <span data-ttu-id="31ef7-173">**Azure コネクタ** リストにサブスクリプションが追加されたのが確認できるはずです。</span><span class="sxs-lookup"><span data-stu-id="31ef7-173">You should now see that the subscription has been added to the **Azure connectors** list.</span></span> <span data-ttu-id="31ef7-174">また、チェック マークは **ARM 有効**で表示されます。</span><span class="sxs-lookup"><span data-stu-id="31ef7-174">Additionally, a check mark should appear under **ARM Enabled**.</span></span>




