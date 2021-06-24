---
title: Finance Insights の構成 (10.0.19 までのバージョン)
description: このトピックでは、Finance Insights (10.0.19 までのバージョン) で使用できる機能をシステムで使用するための構成手順について説明します。
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 6ad06bb6d041fc060b3a99538f6d4d0af333180f
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186423"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="d3a29-103">Finance Insights の構成 (プレビュー版)</span><span class="sxs-lookup"><span data-stu-id="d3a29-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="d3a29-104">次の Finance Insights の設定方法は、Microsoft Dynamics 365 Finance の 10.0.19 までのバージョンに有効です。</span><span class="sxs-lookup"><span data-stu-id="d3a29-104">The following procedures for setting up Finance insights are valid for Microsoft Dynamics 365 Finance versions up to 10.0.19.</span></span> <span data-ttu-id="d3a29-105">バージョン 10.0.20 以降で Finance Insights を設定するには、[Finance Insights の構成 (プレビュー) - バージョン 10.0.20 以降](configure-for-fin-insites-PubPrvw.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3a29-105">To set up Finance insights on version 10.0.20 and later, see [Configuration for Finance Insights (preview) - versions 10.0.20 and beyond](configure-for-fin-insites-PubPrvw.md).</span></span>

<span data-ttu-id="d3a29-106">Finance insights では、Microsoft Dataverse を使用した Microsoft Dynamics 365 Finance、Azure、AI Builder の機能を組み合わせて、強力な予測ツールを提供します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-106">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="d3a29-107">このトピックでは、Finance Insights で使用できる機能をシステムで使用できるようにするための構成手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-107">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="d3a29-108">Dynamics 365 Finance のデプロイ</span><span class="sxs-lookup"><span data-stu-id="d3a29-108">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="d3a29-109">環境をデプロイするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d3a29-109">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="d3a29-110">Microsoft Dynamics Lifecycle Services (LCS) で、Dynamics 365 Finance 環境を作成または更新します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="d3a29-111">この環境では、アプリ バージョン10.0.11/プラットフォーム更新プログラム 35またはそれ以降が必要となります。</span><span class="sxs-lookup"><span data-stu-id="d3a29-111">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="d3a29-112">この環境は、サンドボックスの高可用性 (HA) 環境である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3a29-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="d3a29-113">(このタイプの環境は、Tier 2 環境とも呼ばれます)。詳細については、[環境の計画](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3a29-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="d3a29-114">サンドボックス環境で Finance insights を構成している場合は、予測を機能させるには、本番データをその環境にコピーする必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="d3a29-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="d3a29-115">予測モデルでは、複数年分のデータを用いて予測値を構築します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="d3a29-116">Contoso のデモ データには、予測モデルを適切にトレーニングさせるだけの十分な過去のデータが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="d3a29-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="d3a29-117">Dataverse のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d3a29-117">Configure Dataverse</span></span>

<span data-ttu-id="d3a29-118">Finance Insights の Dataverse のコンフィギュレーションを行うには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d3a29-118">Use the following steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="d3a29-119">LCS の環境ページを開き、**Power Platform 統合** セクションが既に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-119">Open the environment page in LCS and verify that the **Power Platform Integration** section is already setup.</span></span>
    1. <span data-ttu-id="d3a29-120">既に設定されている場合、Dynamics 365 Finance 環境にリンクされている Dataverse 環境名が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-120">If it is already set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="d3a29-121">Dataverse 環境名をコピーします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-121">Copy the Dataverse environment name.</span></span>
    2. <span data-ttu-id="d3a29-122">設定されていない場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d3a29-122">If it is not set up, follow these steps:</span></span>
        1. <span data-ttu-id="d3a29-123">Power Platform 統合セクションで、**設定** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-123">Select the **Setup** button in the Power Platform Integration section.</span></span> <span data-ttu-id="d3a29-124">環境の設定には、最大で 1 時間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d3a29-124">It may take up to an hour for the environment to be set up.</span></span>
        2. <span data-ttu-id="d3a29-125">Dataverse 環境が正常に設定されている場合、Dynamics 365 Finance 環境にリンクされている Dataverse 環境名が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-125">If the Dataverse environment is successfully set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="d3a29-126">Dataverse 環境名をコピーします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-126">Copy the Dataverse environment name.</span></span>
> [!NOTE]
> <span data-ttu-id="d3a29-127">環境の設定が完了した後、**アプリの CDS にリンク** ボタンを選択 **しないでください**。</span><span class="sxs-lookup"><span data-stu-id="d3a29-127">After completing the environment set up, **DO NOT** select the **Link to CDS for Apps** button.</span></span> <span data-ttu-id="d3a29-128">これは Finance Insights には必要なく、LCS で必要な環境アドインを完了する機能を無効にします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-128">This is not needed for Finance Insights and will disable the ability to complete the required Environment Add-ins in LCS.</span></span>

2. <span data-ttu-id="d3a29-129">[Power Platform 管理センター ](https://admin.powerplatform.microsoft.com/)を開き、次の手順に従って、同じ Active Directory テナントに新しい Dataverse 環境を作成します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-129">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="d3a29-130">**環境** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-130">Open the **Environments** page.</span></span>

        <span data-ttu-id="d3a29-131">[![ 環境ページ](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="d3a29-131">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="d3a29-132">上記で作成した Dataverse 環境を選択してから、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-132">Select the Dataverse environment created above and then select **Settings**.</span></span>
    3. <span data-ttu-id="d3a29-133">**リソース \> すべてのレガシー設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-133">Select **Resources \> All Legacy Settings**.</span></span>
    4. <span data-ttu-id="d3a29-134">トップ ナビゲーションバーで、**設定** を選択し、**カスタマイズ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-134">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    5. <span data-ttu-id="d3a29-135">**開発者リソース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-135">Select **Developer Resources**.</span></span>
    6. <span data-ttu-id="d3a29-136">**Dataverse 組織 ID** の値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-136">Copy the **Dataverse organization ID** value.</span></span>
    7. <span data-ttu-id="d3a29-137">ブラウザーのアドレスバーで、Dataverse 組織の URL をメモします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-137">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="d3a29-138">URL は次のようなものになるでしょう: [`https://org42b2b3d3.crm.dynamics.com`]。</span><span class="sxs-lookup"><span data-stu-id="d3a29-138">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

3. <span data-ttu-id="d3a29-139">キャッシュフロー予測機能や予算予測機能を使用する場合は、次の手順に従って、注釈の制限を少なくとも 50 メガバイト (MB) に更新してください。</span><span class="sxs-lookup"><span data-stu-id="d3a29-139">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="d3a29-140">[Power Apps ポータル](https://make.powerapps.com)を開きます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-140">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="d3a29-141">作成した環境を選択し、 **詳細設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-141">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="d3a29-142">**設定 \> 電子メールの構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-142">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="d3a29-143">**最大ファイルサイズ** フィールドの値を **51,200** に変更します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-143">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="d3a29-144">(値は、キロバイト \[KB\] で表されます。)</span><span class="sxs-lookup"><span data-stu-id="d3a29-144">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="d3a29-145">**OK** を選択して変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-145">Select **OK** to save your changes.</span></span>

## <a name="configure-the-azure-setup"></a><span data-ttu-id="d3a29-146">Azure の設定を構成する</span><span class="sxs-lookup"><span data-stu-id="d3a29-146">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="d3a29-147">Dataverse ディレクトリ ID とユーザーの Azure AD オブジェクト ID を入力します</span><span class="sxs-lookup"><span data-stu-id="d3a29-147">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="d3a29-148">Dataverse ディレクトリ ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-148">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="d3a29-149">[Azure ポータル](https://portal.azure.com)を開きます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-149">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="d3a29-150">Dataverse 環境の作成に使用したユーザー ID を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-150">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="d3a29-151">**Azure Active Directory** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-151">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="d3a29-152">**テナント ID** の値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-152">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="d3a29-153">ユーザーの Azure Active Directory (Azure AD) オブジェクト ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-153">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="d3a29-154">[Azure portal](https://portal.azure.com)で、**ユーザー** に移動して電子メールアドレスでユーザーを検索します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-154">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="d3a29-155">ユーザーの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-155">Select the user's name.</span></span>
    3. <span data-ttu-id="d3a29-156">**オブジェクト ID** の値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-156">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="d3a29-157">Azure Cloud Shell を使用した Finance insights Data Lake リソースの設定</span><span class="sxs-lookup"><span data-stu-id="d3a29-157">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="d3a29-158">Windows PowerShell スクリプトを使用する</span><span class="sxs-lookup"><span data-stu-id="d3a29-158">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="d3a29-159">Windows PowerShell スクリプトが指定されているため、[Azure Data Lakeへのエクスポートの構成](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md)で説明されているように Azure リソースを簡単に設定できます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-159">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="d3a29-160">手動による設定を行う場合は、この手順を省略して、[手動設定](#manual-setup)の手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-160">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="d3a29-161">PowerShell スクリプトを実行するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-161">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="d3a29-162">Azure CLI の "Try it" オプション、または PC 上でのスクリプト実行ができない場合があります。</span><span class="sxs-lookup"><span data-stu-id="d3a29-162">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="d3a29-163">Windows PowerShell スクリプトを使用して Azure をコ構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d3a29-163">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="d3a29-164">Azure リソース グループ、Azure リソース、 Azure AD アプリケーションを作成する権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3a29-164">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="d3a29-165">必要なアクセス許可については、[Azure AD のアクセス許可の確認](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3a29-165">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="d3a29-166">[Azure portal](https://portal.azure.com)で、対象の Azure サブスクリプションにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-166">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="d3a29-167">**検索** フィールドの右側にある **Cloud Shell** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-167">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="d3a29-168">**PowerShell** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-168">Select **PowerShell**.</span></span>
3. <span data-ttu-id="d3a29-169">求められた場合は、ストレージを作成します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-169">Create storage if you're prompted to do so.</span></span>
4. <span data-ttu-id="d3a29-170">**Azure CLI** タブで **コピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-170">Go to the **Azure CLI** tab and select **Copy**.</span></span>  
5. <span data-ttu-id="d3a29-171">メモ帳を開き、PowerShell スクリプトを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-171">Open Notepad and paste the PowerShell script.</span></span> <span data-ttu-id="d3a29-172">ファイルを ConfigureDataDatae.ps1 として保存します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-172">Save the file as ConfigureDataLake.ps1.</span></span>
6. <span data-ttu-id="d3a29-173">Cloud Shell のアップロード用メニュー オプションを使用して、Windows PowerShell スクリプトをセッションにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-173">Upload the Windows PowerShell script to the session using the menu option for upload in Cloud Shell.</span></span>
7. <span data-ttu-id="d3a29-174">.\ConfigureDataDatae.ps1 スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-174">Run the script .\ConfigureDataLake.ps1.</span></span>
8. <span data-ttu-id="d3a29-175">プロンプトに従ってスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-175">Follow the prompts to run the script.</span></span>
9. <span data-ttu-id="d3a29-176">スクリプト出力の情報を使用して、LCS に **Data Lake にエクスポートする** アドインをインストールします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-176">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
10. <span data-ttu-id="d3a29-177">スクリプト出力の情報を使用して、Finance (**システム管理 \> システムパラメーター \> データ接続**) の **データ接続** ページのエンティティストアを有効にします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-177">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="d3a29-178">手動設定</span><span class="sxs-lookup"><span data-stu-id="d3a29-178">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="d3a29-179">Azure AD テナントへのアプリケーションの追加</span><span class="sxs-lookup"><span data-stu-id="d3a29-179">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="d3a29-180">[Azure ポータル](https://portal.azure.com)で **Azure Active Directory** にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-180">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="d3a29-181">**管理 \> エンタープライズ アプリケーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-181">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="d3a29-182">次のアプリケーションをアプリ ID で検索します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-182">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="d3a29-183">申請書</span><span class="sxs-lookup"><span data-stu-id="d3a29-183">Application</span></span>                              | <span data-ttu-id="d3a29-184">アプリ ID</span><span class="sxs-lookup"><span data-stu-id="d3a29-184">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="d3a29-185">Microsoft Dynamics ERP マイクロサービス</span><span class="sxs-lookup"><span data-stu-id="d3a29-185">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="d3a29-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="d3a29-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="d3a29-187">Microsoft Dynamics ERP マイクロサービス CDS</span><span class="sxs-lookup"><span data-stu-id="d3a29-187">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="d3a29-188">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="d3a29-188">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="d3a29-189">AI Builder の承認サービス</span><span class="sxs-lookup"><span data-stu-id="d3a29-189">AI Builder Authorization Service</span></span>         | <span data-ttu-id="d3a29-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="d3a29-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="d3a29-191">前述のアプリケーションが見つからない場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-191">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="d3a29-192">ローカル コンピューターで、**スタート**  メニューを選択し、**powershell** を検索します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-192">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="d3a29-193">**Windows PowerShell** を右クリックし、**管理者として実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-193">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="d3a29-194">以下のコマンドを実行して **AzureAD** モジュールをインストールします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-194">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="d3a29-195">NuGet プロバイダーを続行する必要がある場合は、**Y** を選択してインストールします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-195">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="d3a29-196">「信頼できないリポジトリ」のメッセージが表示された場合は、**Y** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-196">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="d3a29-197">追加の必要がある各アプリケーションについては、以下のコマンドを実行してアプリケーションを Azure AD に追加します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-197">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="d3a29-198">プロンプトが表示されたら、管理者で Azure AD にログインします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-198">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="d3a29-199">Azure リソースの作成</span><span class="sxs-lookup"><span data-stu-id="d3a29-199">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="d3a29-200">Dataverse 環境と同じ Azure AD インスタンスで次のリソースを作成してください。</span><span class="sxs-lookup"><span data-stu-id="d3a29-200">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="d3a29-201">別の Azure AD インスタンスのリソースを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="d3a29-201">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="d3a29-202">新しいストレージ アカウントを作成する方法:</span><span class="sxs-lookup"><span data-stu-id="d3a29-202">Create a new storage account:</span></span>

    1. <span data-ttu-id="d3a29-203">[Azure ポータル](https://portal.azure.com)で、新しいストレージ アカウントを作成します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-203">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="d3a29-204">**ストレージ アカウントの作成** ダイアログ ボックスで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-204">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="d3a29-205">**場所** - ご利用の環境が設置されているデータセンターを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-205">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="d3a29-206">**パフォーマンス** - **標準** を選択することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-206">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="d3a29-207">**アカウントの種類** - 必ず **Storage V2** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="d3a29-207">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="d3a29-208">**詳細オプション** ダイアログボックスの **Data Lake storage Gen2** オプションで、**階層型名前空間** 機能配下の **有効** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-208">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="d3a29-209">この機能を無効にすると、Power BI データ フローなどのサービスを含む Finance and Operations アプリが書き込んだデータを使用することができません。</span><span class="sxs-lookup"><span data-stu-id="d3a29-209">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="d3a29-210">**確認して作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-210">Select **Review and create**.</span></span> <span data-ttu-id="d3a29-211">配置が完了したら、新しいリソースが Azure ポータルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-211">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="d3a29-212">作成したストレージ アカウントに移動します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-212">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="d3a29-213">左側のメニューで、**アクセス キー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-213">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="d3a29-214">**Key1** または **Key2** の接続文字列をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-214">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="d3a29-215">ストレージアカウント名をコピーして保存し ます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-215">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="d3a29-216">新しいキー コンテナーの作成:</span><span class="sxs-lookup"><span data-stu-id="d3a29-216">Create a new key vault:</span></span>

    1. <span data-ttu-id="d3a29-217">[Azure portal](https://portal.azure.com)で、新しいキー コンテナーを作成します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-217">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="d3a29-218">**Key Vault の作成** ダイアログ ボックスの **場所** フィールドで、環境があるデータ センターを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-218">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="d3a29-219">キー コンテナーが作成されたら、一覧で選択し、**シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-219">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="d3a29-220">**生成/インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-220">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="d3a29-221">**シークレットを作成** ダイアログ ボックスの **アップロード オプション** フィールドで、**手動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-221">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="d3a29-222">シークレットの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-222">Enter a name for the secret.</span></span> <span data-ttu-id="d3a29-223">その後で指定する必要があるため、名前をメモします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-223">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="d3a29-224">**値** フィールドに、前述の手順でストレージ アカウントから取得した接続文字列を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-224">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="d3a29-225">**有効** を選択し、**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-225">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="d3a29-226">シークレットが作成され、Key Vault に追加されます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-226">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="d3a29-227">**キー コンテナーの概要** を開き、DNS 名を控えておきます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-227">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="d3a29-228">Azure AD アプリケーションを作成、登録します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-228">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="d3a29-229">[Azure portal](https://portal.azure.com) で、**Azure Active Directory** にアクセスし、**App registrations** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-229">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="d3a29-230">**新規アプリケーションの登録** を選択し、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-230">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="d3a29-231">**名前** - アプリの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-231">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="d3a29-232">**アプリケーション タイプ** - **Web API** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-232">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="d3a29-233">**リダイレクト URI の設定** - Dynamics 365 インスタンスの URL を入力します (例: `https://yourdynamicsinstance.dynamics.com/auth` )。</span><span class="sxs-lookup"><span data-stu-id="d3a29-233">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="d3a29-234">作成したアプリに移動し、**アプリケーション (クライアント) ID** の値をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-234">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="d3a29-235">後続の処理でキー コンテナーを設定する際に、このシークレットの値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3a29-235">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="d3a29-236">**API アクセス許可** に移動し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d3a29-236">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="d3a29-237">**アクセス許可の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-237">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="d3a29-238">**Azure Key vault** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-238">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="d3a29-239">[委任されたアクセス許可] を選択した後、**ユーザー\_なりすまし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-239">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="d3a29-240">**アクセス許可の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-240">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="d3a29-241">アプリのメニューで、**証明書\&シークレット** を選択し、次の手順に従ってキー コンテナーのシークレットを作成します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-241">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="d3a29-242">**新しいクライアント シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-242">Select **New client secret**.</span></span>
        2. <span data-ttu-id="d3a29-243">**キーの説明** フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-243">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="d3a29-244">期間を選択し、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-244">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="d3a29-245">シークレットが **値** フィールドに生成されます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-245">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="d3a29-246">シークレットの値をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-246">Copy and save the secret value.</span></span>

4. <span data-ttu-id="d3a29-247">新しいキー コンテナーの作成:</span><span class="sxs-lookup"><span data-stu-id="d3a29-247">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="d3a29-248">前述の手順で作成したキー コンテナーに移動し、**シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-248">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="d3a29-249">次の表の各シークレットに対して、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-249">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="d3a29-250">**生成/インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-250">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="d3a29-251">**シークレットを作成** ダイアログ ボックスの **アップロード オプション** フィールドで、**手動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-251">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="d3a29-252">次の表から、シークレットの名前と値を作成します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-252">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="d3a29-253">**有効** を選択し、**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-253">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="d3a29-254">シークレットが作成され、Key Vault に追加されます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-254">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="d3a29-255">シークレット名</span><span class="sxs-lookup"><span data-stu-id="d3a29-255">Secret name</span></span>                       | <span data-ttu-id="d3a29-256">シークレットの値</span><span class="sxs-lookup"><span data-stu-id="d3a29-256">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="d3a29-257">アプリ ID</span><span class="sxs-lookup"><span data-stu-id="d3a29-257">app-id</span></span>                            | <span data-ttu-id="d3a29-258">作成済みのアプリケーション アプリ ID</span><span class="sxs-lookup"><span data-stu-id="d3a29-258">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="d3a29-259">アプリのシークレット</span><span class="sxs-lookup"><span data-stu-id="d3a29-259">app-secret</span></span>                        | <span data-ttu-id="d3a29-260">前述の手順で保存したクライアント シークレット</span><span class="sxs-lookup"><span data-stu-id="d3a29-260">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="d3a29-261">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="d3a29-261">storage-account-name</span></span>              | <span data-ttu-id="d3a29-262">前に作成したストレージアカウントの名前 (例: **sstorageaccount1**)</span><span class="sxs-lookup"><span data-stu-id="d3a29-262">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="d3a29-263">ストレージ - アカウント - 接続 - 文字列</span><span class="sxs-lookup"><span data-stu-id="d3a29-263">storage-account-connection-string</span></span> | <span data-ttu-id="d3a29-264">ストレージ アカウントの **アクセス キー** ページからコピーした接続文字列</span><span class="sxs-lookup"><span data-stu-id="d3a29-264">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="d3a29-265">アプリケーションを承認してキー コンテナーにアクセスする方法:</span><span class="sxs-lookup"><span data-stu-id="d3a29-265">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="d3a29-266">[Azure portal](https://portal.azure.com)で、作成済のキー コンテナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-266">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="d3a29-267">アクセス ポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-267">Select the access policies.</span></span>
    3. <span data-ttu-id="d3a29-268">次のアプリケーションに対して、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-268">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="d3a29-269">**アクセス ポリシー** を選択し、アクセス ポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-269">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="d3a29-270">**シークレットのアクセス許可** フィールドで、次の表からアクセス許可を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-270">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="d3a29-271">**プリンシパルの選択** フィールドで、次の表からアプリケーションの表示名を検索します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-271">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="d3a29-272">**選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-272">Select **Select**.</span></span>
        5. <span data-ttu-id="d3a29-273">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-273">Select **Add**.</span></span>
        6. <span data-ttu-id="d3a29-274">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-274">Select **Save**.</span></span>

        | <span data-ttu-id="d3a29-275">申請書</span><span class="sxs-lookup"><span data-stu-id="d3a29-275">Application</span></span>                                              | <span data-ttu-id="d3a29-276">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="d3a29-276">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="d3a29-277">作成した新しいアプリケーションの表示名称</span><span class="sxs-lookup"><span data-stu-id="d3a29-277">The display name of the new application that you created</span></span> | <span data-ttu-id="d3a29-278">取得、リスト表示</span><span class="sxs-lookup"><span data-stu-id="d3a29-278">Get, List</span></span>   |
        | <span data-ttu-id="d3a29-279">**Microsoft Dynamics ERP マイクロサービス**</span><span class="sxs-lookup"><span data-stu-id="d3a29-279">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="d3a29-280">取得、リスト表示</span><span class="sxs-lookup"><span data-stu-id="d3a29-280">Get, List</span></span>   |

6. <span data-ttu-id="d3a29-281">ストレージ アカウントにアクセスするロールを割り当てるには、次の操作を行います:</span><span class="sxs-lookup"><span data-stu-id="d3a29-281">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="d3a29-282">[Azure ポータル](https://portal.azure.com)で、作成済のストレージ アカウントを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-282">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="d3a29-283">**アクセスの制御 (IAM)** を選択し 、**ロールの割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-283">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="d3a29-284">**追加、 ロールの割り当ての追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-284">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="d3a29-285">次のアプリケーションに対して、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-285">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="d3a29-286">以下の表からロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-286">Select the role from the following table.</span></span>
        2. <span data-ttu-id="d3a29-287">**アクセス権の割り当て先** シールドは、**Azure AD ユーザー、グループ、またはサービス プリンシパル** のままにします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-287">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="d3a29-288">**選択** フィールドで、次の表からアプリケーションを入力します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-288">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="d3a29-289">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-289">Select **Save**.</span></span>

        | <span data-ttu-id="d3a29-290">申請書</span><span class="sxs-lookup"><span data-stu-id="d3a29-290">Application</span></span>                                              | <span data-ttu-id="d3a29-291">役割</span><span class="sxs-lookup"><span data-stu-id="d3a29-291">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="d3a29-292">作成した新しいアプリケーションの表示名称</span><span class="sxs-lookup"><span data-stu-id="d3a29-292">The display name of the new application that you created</span></span> | <span data-ttu-id="d3a29-293">所有者</span><span class="sxs-lookup"><span data-stu-id="d3a29-293">Owner</span></span>                       |
        | <span data-ttu-id="d3a29-294">作成した新しいアプリケーションの表示名称</span><span class="sxs-lookup"><span data-stu-id="d3a29-294">The display name of the new application that you created</span></span> | <span data-ttu-id="d3a29-295">寄稿者</span><span class="sxs-lookup"><span data-stu-id="d3a29-295">Contributor</span></span>                 |
        | <span data-ttu-id="d3a29-296">作成した新しいアプリケーションの表示名称</span><span class="sxs-lookup"><span data-stu-id="d3a29-296">The display name of the new application that you created</span></span> | <span data-ttu-id="d3a29-297">ストレージ アカウントの共同作成者</span><span class="sxs-lookup"><span data-stu-id="d3a29-297">Storage Account Contributor</span></span> |
        | <span data-ttu-id="d3a29-298">作成した新しいアプリケーションの表示名称</span><span class="sxs-lookup"><span data-stu-id="d3a29-298">The display name of the new application that you created</span></span> | <span data-ttu-id="d3a29-299">ストレージ BLOB データの所有者</span><span class="sxs-lookup"><span data-stu-id="d3a29-299">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="d3a29-300">**AI Builder の承認サービス**</span><span class="sxs-lookup"><span data-stu-id="d3a29-300">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="d3a29-301">ストレージ BLOB データの読み取り</span><span class="sxs-lookup"><span data-stu-id="d3a29-301">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="d3a29-302">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="d3a29-302">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}

```
---



## <a name="configure-the-data-lake"></a><span data-ttu-id="d3a29-303">Data Lake を構成する</span><span class="sxs-lookup"><span data-stu-id="d3a29-303">Configure the data lake</span></span>

<span data-ttu-id="d3a29-304">LCS を使用して Azure Data Lake アドインを環境に追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d3a29-304">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="d3a29-305">LCS にログインし、ページの右側にある環境名の下の **完全な詳細** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-305">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="d3a29-306">**環境アドイン** セクションで、**新しいアドインのインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-306">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="d3a29-307">**Data Lake へのエクスポート** アドインを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-307">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="d3a29-308">次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-308">Enter the following values.</span></span>

    | <span data-ttu-id="d3a29-309">先頭値</span><span class="sxs-lookup"><span data-stu-id="d3a29-309">Value</span></span>                                                              | <span data-ttu-id="d3a29-310">説明</span><span class="sxs-lookup"><span data-stu-id="d3a29-310">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="d3a29-311">キーの保管場所がある Azure サブスクリプションのテナント ID</span><span class="sxs-lookup"><span data-stu-id="d3a29-311">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="d3a29-312">ストレージ アカウント、アプリ、キーコンテナーが配置されているテナント ID です。</span><span class="sxs-lookup"><span data-stu-id="d3a29-312">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="d3a29-313">この値を検索するには、[Azure portal](https://portal.azure.com) を開き、**Azure Active Directory** に移動し、**テナント ID** の値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-313">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="d3a29-314">Key Vault の DNS 名を指定する</span><span class="sxs-lookup"><span data-stu-id="d3a29-314">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="d3a29-315">キー コンテナーの DNS 名 (例:  `https://customkeyvault.vault.azure.net/`)。</span><span class="sxs-lookup"><span data-stu-id="d3a29-315">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="d3a29-316">(この値は、エンティティ ストアで使用されている DNS 名と同一のものです。)</span><span class="sxs-lookup"><span data-stu-id="d3a29-316">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="d3a29-317">ストレージ アカウントの名前を含むシークレットを指定します</span><span class="sxs-lookup"><span data-stu-id="d3a29-317">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="d3a29-318">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="d3a29-318">**storage-account-name**</span></span> |
    | <span data-ttu-id="d3a29-319">Data Lake へのアクセスに使用するアプリ ID のシークレット名</span><span class="sxs-lookup"><span data-stu-id="d3a29-319">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="d3a29-320">**アプリの ID**</span><span class="sxs-lookup"><span data-stu-id="d3a29-320">**app-id**</span></span> |
    | <span data-ttu-id="d3a29-321">アプリの ID に使用するシークレット名</span><span class="sxs-lookup"><span data-stu-id="d3a29-321">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="d3a29-322">**アプリのシークレット**</span><span class="sxs-lookup"><span data-stu-id="d3a29-322">**app-secret**</span></span> |

5. <span data-ttu-id="d3a29-323">条件に同意し、**インストール** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-323">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="d3a29-324">このアドインは数分以内にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-324">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="d3a29-325">AI Builder の構成</span><span class="sxs-lookup"><span data-stu-id="d3a29-325">Configure AI Builder</span></span>

1. <span data-ttu-id="d3a29-326">LCS にサインインし、**環境の詳細** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-326">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="d3a29-327">**環境アドイン** セクションまでスクロールします。</span><span class="sxs-lookup"><span data-stu-id="d3a29-327">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="d3a29-328">この環境に既にインストールされているアドインが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-328">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="d3a29-329">**Data Lake にエクスポートする** アドインがない場合は、このアドインを構成します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-329">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="d3a29-330">**分析情報の取得** アドインを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-330">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="d3a29-331">**分析情報の取得** アドインの詳細ページで、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-331">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="d3a29-332">先頭値</span><span class="sxs-lookup"><span data-stu-id="d3a29-332">Value</span></span>                                                    | <span data-ttu-id="d3a29-333">説明</span><span class="sxs-lookup"><span data-stu-id="d3a29-333">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="d3a29-334">CDS 組織の URL</span><span class="sxs-lookup"><span data-stu-id="d3a29-334">CDS Organization URL</span></span>                                     | <span data-ttu-id="d3a29-335">上記からコピーした Dataverse 組織の URL です。</span><span class="sxs-lookup"><span data-stu-id="d3a29-335">The Dataverse organization URL copied from above.</span></span> |
    | <span data-ttu-id="d3a29-336">CDS Org ID</span><span class="sxs-lookup"><span data-stu-id="d3a29-336">CDS Org ID</span></span>                                               | <span data-ttu-id="d3a29-337">上記からコピーした Dataverse 組織の ID です。</span><span class="sxs-lookup"><span data-stu-id="d3a29-337">The Dataverse organization ID copied from above.</span></span> |
5. <span data-ttu-id="d3a29-338">有効化 **これはテナントの既定の環境ですか**。</span><span class="sxs-lookup"><span data-stu-id="d3a29-338">Enable **Is this the default environment for you Tenant**.</span></span>
    
## <a name="configure-the-entity-store"></a><span data-ttu-id="d3a29-339">エンティティの保存を構成する</span><span class="sxs-lookup"><span data-stu-id="d3a29-339">Configure the entity store</span></span>

<span data-ttu-id="d3a29-340">Finance 環境でエンティティの保存を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d3a29-340">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="d3a29-341">**システム管理 \> 設定 \> システム パラメーター \> データ接続** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-341">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="d3a29-342">次のキー コンテナー フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-342">Set the following key vault fields:</span></span>

    - <span data-ttu-id="d3a29-343">**アプリケーション (クライアント) ID**: 以前に作成したアプリケーションクライアント ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-343">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="d3a29-344">**アプリケーションのシークレット** - 以前に作成したアプリケーションで使用する保存済みのシークレットを入力します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-344">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="d3a29-345">**DNS 名** - ドメイン ネーム システム (DNS) 名は、前述の手順で作成したアプリケーションの [アプリケーションの詳細] ページで確認できます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-345">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="d3a29-346">**シークレット名** - **ストレージ アカウントの接続文字列** を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-346">**Secret name** – Enter **storage-account-connection-string**.</span></span>
3. <span data-ttu-id="d3a29-347">有効化 **Data Lake 統合を有効にします**。</span><span class="sxs-lookup"><span data-stu-id="d3a29-347">Enable **Enable Data Lake integration**.</span></span>
4. <span data-ttu-id="d3a29-348">**Azure Key Vault のテスト** を選択し、エラーがないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-348">Select **Test Azure Key Vault** and verify there are no errors.</span></span>
5. <span data-ttu-id="d3a29-349">**Azure Storage のテスト** を選択し、エラーがないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="d3a29-349">Select **Test Azure storage** and verify there are no errors.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="d3a29-350">フィードバックとサポート</span><span class="sxs-lookup"><span data-stu-id="d3a29-350">Feedback and support</span></span>

<span data-ttu-id="d3a29-351">フィードバックの提供またはサポートが必要な場合は、[顧客支払い分析情報 (プレビュー)](mailto:fiap@microsoft.com) に電子メールを送信してください。</span><span class="sxs-lookup"><span data-stu-id="d3a29-351">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="d3a29-352">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="d3a29-352">Privacy notice</span></span>

<span data-ttu-id="d3a29-353">プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよび少ないセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル アグリーメント (SLA) には含まれておらず、(3) 個人データや、その他の法律上またはコンプライアンス要件の対象となるデータの処理に使用されず、(4) サポートが制限されます。</span><span class="sxs-lookup"><span data-stu-id="d3a29-353">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
