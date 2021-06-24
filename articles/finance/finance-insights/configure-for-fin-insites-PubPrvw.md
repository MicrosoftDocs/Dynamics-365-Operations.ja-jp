---
title: パブリック プレビュー (プレビュー) で使用する Finance insights の構成 - バージョン 10.0.20 以降
description: このトピックでは、バージョン 10.0.20 以降のパブリック プレビュー版 Finance Insights で利用可能な機能を使用するために、システムを設定する方法について説明します。
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
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 613bd4816e2f0c4fbb56cf79779a08c6a09592bd
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222615"
---
# <a name="configuration-for-finance-insights-for-public-preview-preview---version-10020-and-later"></a><span data-ttu-id="7a554-103">パブリック プレビュー (プレビュー) で使用する Finance insights の構成 - バージョン 10.0.20 以降</span><span class="sxs-lookup"><span data-stu-id="7a554-103">Configuration for Finance insights for public preview (preview) - version 10.0.20 and later</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="7a554-104">Finance insights では、Dataverse を使用した Microsoft Dynamics 365 Finance、Azure、AI Builder の機能を組み合わせて、強力な予測ツールを提供します。</span><span class="sxs-lookup"><span data-stu-id="7a554-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="7a554-105">このトピックでは、Dynamics 365 Finance のバージョン 10.0.20 を設定して、Finance Insights のパブリックプレビューで利用可能な機能をシステムで使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7a554-105">This topic explains how to configure Dynamics 365 Finance version 10.0.20 so that your system can use the capabilities that are available in Finance insights public preview.</span></span>

> [!NOTE]
> <span data-ttu-id="7a554-106">このトピックで説明する構成手順は、Finance のバージョン 10.0.20 以降にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="7a554-106">The configuration steps that are described in this topic apply only to Finance version 10.0.20 and later.</span></span> <span data-ttu-id="7a554-107">バージョン 10.0.19 およびそれ以前で Finance Insights を設定するには、[Finance Insights の構成 - バージョン 10.0.18 まで](configure-for-fin-insites.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a554-107">'To set up Finance insights on version 10.0.19 and earlier, see [Configuration for Finance insights - versions up to 10.0.18](configure-for-fin-insites.md).</span></span>

## <a name="deploy-finance"></a><span data-ttu-id="7a554-108">Finance のデプロイ</span><span class="sxs-lookup"><span data-stu-id="7a554-108">Deploy Finance</span></span>

<span data-ttu-id="7a554-109">環境をデプロイするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7a554-109">Follow these steps to deploy the environments.</span></span>

1. <span data-ttu-id="7a554-110">Microsoft Dynamics Lifecycle Services (LCS) で、 Finance 環境を作成、または更新します。</span><span class="sxs-lookup"><span data-stu-id="7a554-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Finance environment.</span></span> <span data-ttu-id="7a554-111">この環境では、Finance and Operations のアプリのバージョン 10.0.20 以降が必要です。</span><span class="sxs-lookup"><span data-stu-id="7a554-111">The environment requires app version 10.0.20 or later of Finance and Operations apps.</span></span>
2. <span data-ttu-id="7a554-112">この環境は、サンドボックスの高可用性 (HA) 環境である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a554-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="7a554-113">(このタイプの環境は、Tier 2 環境とも呼ばれます)。詳細については、[環境の計画](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a554-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="7a554-114">サンドボックス環境で Finance insights を構成している場合は、予測を機能させるには、本番データをその環境にコピーする必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="7a554-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="7a554-115">予測モデルでは、複数年分のデータを用いて予測値を構築します。</span><span class="sxs-lookup"><span data-stu-id="7a554-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="7a554-116">Contoso のデモ データには、予測モデルを適切にトレーニングさせるだけの十分な過去のデータが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="7a554-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="7a554-117">Dataverse のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7a554-117">Configure Dataverse</span></span>

<span data-ttu-id="7a554-118">以下の手順で、Finance insights に Dataverse を構成します。</span><span class="sxs-lookup"><span data-stu-id="7a554-118">Follow these steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="7a554-119">LCS で、環境のページを開き、**Power Platform 統合** のセクションがすでに設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7a554-119">In LCS, open the environment page, and verify that the **Power Platform Integration** section is already set up.</span></span>

    - <span data-ttu-id="7a554-120">既に設定されている場合、 Finance 環境にリンクされている Dataverse の環境名が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7a554-120">If it's already set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>
    - <span data-ttu-id="7a554-121">まだ設定されていない場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7a554-121">If it isn't yet set up, follow these steps:</span></span>

        1. <span data-ttu-id="7a554-122">**Power Platform の統合** セクションで、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-122">In the **Power Platform Integration** section, select **Setup**.</span></span> <span data-ttu-id="7a554-123">環境の設定には最大で 1 時間ほどかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="7a554-123">Setup of the environment might take up to an hour.</span></span>
        2. <span data-ttu-id="7a554-124">Dataverse 環境が正常に設定されている場合、Finance 環境にリンクされている Dataverse の環境名が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7a554-124">If the Dataverse environment is successfully set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>

        > [!NOTE]
        > <span data-ttu-id="7a554-125">環境の設定が完了した後は、**CDS for Apps へのリンク** を選択 **しないでください**。</span><span class="sxs-lookup"><span data-stu-id="7a554-125">After you complete the environment setup, do **not** select **Link to CDS for Apps**.</span></span> <span data-ttu-id="7a554-126">このボタンは、Finance Insights には必要ありません。</span><span class="sxs-lookup"><span data-stu-id="7a554-126">This button isn't required for Finance insights.</span></span> <span data-ttu-id="7a554-127">このオプションを選択すると、LCS で必要となる環境アドインを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="7a554-127">If you select it, you won't be able to configure the required environment add-ins in LCS.</span></span>

## <a name="configure-azure"></a><span data-ttu-id="7a554-128">Azure の構成</span><span class="sxs-lookup"><span data-stu-id="7a554-128">Configure Azure</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="7a554-129">Azure Cloud Shell を使用した Finance insights Data Lake リソースの設定</span><span class="sxs-lookup"><span data-stu-id="7a554-129">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="7a554-130">Windows PowerShell スクリプトを使用する</span><span class="sxs-lookup"><span data-stu-id="7a554-130">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="7a554-131">Windows PowerShell スクリプトが用意されているので、[Azure Data Lake へのエクスポートの構成](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) で説明されているように Azure のリソースを簡単に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="7a554-131">A Windows PowerShell script has been provided so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="7a554-132">手動による設定を行う場合は、この手順を省略して、[手動設定](#manual-setup) に記載の手順を完了してください。</span><span class="sxs-lookup"><span data-stu-id="7a554-132">If you prefer to do the setup manually, skip this procedure, and complete the procedure in the [Manual setup](#manual-setup) section instead.</span></span>

> [!NOTE]
> <span data-ttu-id="7a554-133">以下の手順で Windows PowerShell スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7a554-133">Use the following procedure to run the Windows PowerShell script.</span></span> <span data-ttu-id="7a554-134">Azure CLI の **Try it** オプションを使用した場合や、コンピュータ上でスクリプトを実行した場合は、設定がうまくいかないことがあります。</span><span class="sxs-lookup"><span data-stu-id="7a554-134">The setup might not work if you use the **Try it** option in Azure CLI or if you run the script on your computer.</span></span>

<span data-ttu-id="7a554-135">以下の手順で、Windows PowerShell スクリプトを使用して Azure を構成します。</span><span class="sxs-lookup"><span data-stu-id="7a554-135">Follow these steps to use the Windows PowerShell script to configure Azure.</span></span> <span data-ttu-id="7a554-136">Azure リソース グループ、Azure リソース、 Azure AD アプリケーションを作成する権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a554-136">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="7a554-137">必要なアクセス許可については、[Azure AD のアクセス許可の確認](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a554-137">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="7a554-138">[Azure portal](https://portal.azure.com)で、対象の Azure サブスクリプションにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="7a554-138">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span>
2. <span data-ttu-id="7a554-139">**検索** フィールドの右側にある **Cloud Shell** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-139">Select **Cloud Shell** to the right of the **Search** field.</span></span>
3. <span data-ttu-id="7a554-140">**PowerShell** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-140">Select **PowerShell**.</span></span>
4. <span data-ttu-id="7a554-141">ストレージの作成を促された場合は、作成します。</span><span class="sxs-lookup"><span data-stu-id="7a554-141">Create storage if you're prompted to create it.</span></span>
5. <span data-ttu-id="7a554-142">**Azure CLI** タブで、**コピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-142">On the **Azure CLI** tab, select **Copy**.</span></span>
6. <span data-ttu-id="7a554-143">メモ帳で新しいファイルを開き、Windows PowerShell スクリプトに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="7a554-143">In Notepad, open a new file, and paste in the Windows PowerShell script.</span></span>
7. <span data-ttu-id="7a554-144">ファイルを **ConfigureDataLake.ps1** として保存します。</span><span class="sxs-lookup"><span data-stu-id="7a554-144">Save the file as **ConfigureDataLake.ps1**.</span></span>
8. <span data-ttu-id="7a554-145">Windows PowerShell スクリプトをセッションにアップロードするには、Cloud Shell のメニュー オプションであるアップロードを使用します。</span><span class="sxs-lookup"><span data-stu-id="7a554-145">Upload the Windows PowerShell script to the session by using the menu option for upload in Cloud Shell.</span></span>
9. <span data-ttu-id="7a554-146">**.\ConfigureDataLake.ps1** スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7a554-146">Run the **.\ConfigureDataLake.ps1** script.</span></span>
10. <span data-ttu-id="7a554-147">プロンプトに従ってスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7a554-147">Follow the prompts to run the script.</span></span>
11. <span data-ttu-id="7a554-148">スクリプト出力の情報を使用して、LCS に Data Lake にエクスポートするアドインをインストールします。</span><span class="sxs-lookup"><span data-stu-id="7a554-148">Use the information from the script output to install the Export to Data Lake add-in in LCS.</span></span>

### <a name="manual-setup"></a><span data-ttu-id="7a554-149">手動設定</span><span class="sxs-lookup"><span data-stu-id="7a554-149">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="7a554-150">Azure AD テナントへのアプリケーションの追加</span><span class="sxs-lookup"><span data-stu-id="7a554-150">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="7a554-151">[Azure ポータル](https://portal.azure.com)で **Azure Active Directory** にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="7a554-151">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="7a554-152">**管理 \> エンタープライズ アプリケーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-152">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="7a554-153">次のアプリケーションをアプリ ID で検索します。</span><span class="sxs-lookup"><span data-stu-id="7a554-153">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="7a554-154">申請書</span><span class="sxs-lookup"><span data-stu-id="7a554-154">Application</span></span>                              | <span data-ttu-id="7a554-155">アプリ ID</span><span class="sxs-lookup"><span data-stu-id="7a554-155">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="7a554-156">Microsoft Dynamics ERP マイクロサービス</span><span class="sxs-lookup"><span data-stu-id="7a554-156">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="7a554-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="7a554-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="7a554-158">Microsoft Dynamics ERP マイクロサービス CDS</span><span class="sxs-lookup"><span data-stu-id="7a554-158">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="7a554-159">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="7a554-159">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="7a554-160">AI Builder の承認サービス</span><span class="sxs-lookup"><span data-stu-id="7a554-160">AI Builder Authorization Service</span></span>         | <span data-ttu-id="7a554-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="7a554-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="7a554-162">前述のアプリケーションが見つからない場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7a554-162">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="7a554-163">ローカル コンピューターで、**スタート** メニューを開き、**powershell** を検索します。</span><span class="sxs-lookup"><span data-stu-id="7a554-163">On your local computer, on the **Start** menu, search for **powershell**.</span></span>
2. <span data-ttu-id="7a554-164">**Windows PowerShell** を右クリックし、**管理者として実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-164">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="7a554-165">以下のコマンドを実行して **AzureAD** モジュールをインストールします。</span><span class="sxs-lookup"><span data-stu-id="7a554-165">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="7a554-166">NuGet プロバイダーを続行する必要がある場合は、**Y** を選択してインストールします。</span><span class="sxs-lookup"><span data-stu-id="7a554-166">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="7a554-167">「信頼できないリポジトリ」のメッセージが表示された場合は、**Y** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="7a554-167">If you receive an "Untrusted repository" message, select **Y** to continue.</span></span>
6. <span data-ttu-id="7a554-168">追加の必要がある各アプリケーションについては、以下のコマンドを実行してアプリケーションを Azure AD に追加します。</span><span class="sxs-lookup"><span data-stu-id="7a554-168">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="7a554-169">プロンプトが表示されたら、管理者で Azure AD にログインします。</span><span class="sxs-lookup"><span data-stu-id="7a554-169">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="7a554-170">Azure リソースの作成</span><span class="sxs-lookup"><span data-stu-id="7a554-170">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="7a554-171">Dataverse 環境と同じ Azure AD インスタンスに以下のリソースが作成されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7a554-171">Make sure that you create the following resources in the same Azure AD instance that the Dataverse environment is in.</span></span> <span data-ttu-id="7a554-172">別の Azure AD インスタンスのリソースを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="7a554-172">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="7a554-173">ストレージ アカウントを作成します。</span><span class="sxs-lookup"><span data-stu-id="7a554-173">Create a storage account:</span></span>

    1. <span data-ttu-id="7a554-174">[Azure ポータル](https://portal.azure.com)で、新しいストレージ アカウントを作成します。</span><span class="sxs-lookup"><span data-stu-id="7a554-174">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="7a554-175">**ストレージ アカウントの作成** ダイアログ ボックスで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="7a554-175">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="7a554-176">**場所** - ご利用の環境が設置されているデータセンターを選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-176">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="7a554-177">**パフォーマンス** - **標準** を選択することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7a554-177">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="7a554-178">**アカウントの種類** - 必ず **Storage V2** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="7a554-178">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="7a554-179">**詳細オプション** ダイアログボックスの **Data Lake storage Gen2** オプションで、**階層型名前空間** 機能配下の **有効** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-179">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="7a554-180">この機能を有効にしないと、Finance and Operations アプリが書いたデータを Power BI データ フローなどのサービスを使って使用することができません。</span><span class="sxs-lookup"><span data-stu-id="7a554-180">If you don't enable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="7a554-181">**確認して作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-181">Select **Review and create**.</span></span> <span data-ttu-id="7a554-182">デプロイが完了したら、新しいリソースが Azure ポータルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="7a554-182">When the deployment is completed, the new resource is shown in the Azure portal.</span></span>
    5. <span data-ttu-id="7a554-183">作成したストレージ アカウントに移動します。</span><span class="sxs-lookup"><span data-stu-id="7a554-183">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="7a554-184">左側のメニューで、**アクセス キー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-184">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="7a554-185">ストレージのアカウント名をコピーして保存し ます。</span><span class="sxs-lookup"><span data-stu-id="7a554-185">Copy and save the name of the storage account.</span></span> <span data-ttu-id="7a554-186">後続の処理でキー コンテナーを設定する際に、このシークレットの値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a554-186">You will have to provide this value later, when you set up key vault secrets.</span></span>

2. <span data-ttu-id="7a554-187">キー コンテナーの作成:</span><span class="sxs-lookup"><span data-stu-id="7a554-187">Create a key vault:</span></span>

    1. <span data-ttu-id="7a554-188">[Azure portal](https://portal.azure.com)で、新しいキー コンテナーを作成します。</span><span class="sxs-lookup"><span data-stu-id="7a554-188">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="7a554-189">**Key Vault の作成** ダイアログ ボックスの **場所** フィールドで、環境があるデータ センターを選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-189">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="7a554-190">キー コンテナーの作成後、**キー コンテナーの概要** に移動し、DNS 名をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="7a554-190">After key vault is created, go to **Key Vault Overview**, and copy and save the DNS name.</span></span> <span data-ttu-id="7a554-191">後続の処理でData Lake アドインを設定する際に、このシークレットの値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a554-191">You will have to provide this value later, when you set up the Data Lake add-in.</span></span>

3. <span data-ttu-id="7a554-192">Azure AD アプリケーションを作成、登録します。</span><span class="sxs-lookup"><span data-stu-id="7a554-192">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="7a554-193">[Azure portal](https://portal.azure.com) で、**Azure Active Directory** にアクセスし、**App registrations** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-193">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="7a554-194">**新規アプリケーションの登録** を選択し、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="7a554-194">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="7a554-195">**名前** - アプリの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="7a554-195">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="7a554-196">**アプリケーション タイプ** - **Web API** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-196">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="7a554-197">**リダイレクト URI の設定** - Dynamics 365 インスタンスの URL を入力します (例: `https://yourdynamicsinstance.dynamics.com/auth` )。</span><span class="sxs-lookup"><span data-stu-id="7a554-197">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="7a554-198">作成したアプリに移動し、**アプリケーション (クライアント) ID** の値をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="7a554-198">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="7a554-199">後続の処理でキー コンテナーを設定する際に、このシークレットの値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a554-199">You will have to provide this value later, when you set up key vault secrets.</span></span>
    4. <span data-ttu-id="7a554-200">**API アクセス許可** に移動し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7a554-200">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="7a554-201">**アクセス許可の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-201">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="7a554-202">**Azure Key vault** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-202">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="7a554-203">[委任されたアクセス許可] を選択した後、**ユーザー\_なりすまし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-203">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="7a554-204">**アクセス許可の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-204">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="7a554-205">アプリのメニューで、**証明書\&シークレット** を選択し、次の手順に従ってキー コンテナーのシークレットを作成します。</span><span class="sxs-lookup"><span data-stu-id="7a554-205">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="7a554-206">**新しいクライアント シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-206">Select **New client secret**.</span></span>
        2. <span data-ttu-id="7a554-207">**キーの説明** フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="7a554-207">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="7a554-208">期間を選択し、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-208">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="7a554-209">シークレットが **値** フィールドに生成されます。</span><span class="sxs-lookup"><span data-stu-id="7a554-209">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="7a554-210">クライアントのシークレットの値をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="7a554-210">Copy and save the client secret value.</span></span> <span data-ttu-id="7a554-211">後続の処理でキー コンテナーを設定する際に、このシークレットの値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a554-211">You will have to provide this value later, when you set up key vault secrets.</span></span>

4. <span data-ttu-id="7a554-212">新しいキー コンテナーの作成:</span><span class="sxs-lookup"><span data-stu-id="7a554-212">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="7a554-213">前述の手順で作成したキー コンテナーに移動し、**シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-213">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="7a554-214">次の表の各シークレットに対して、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7a554-214">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="7a554-215">**生成/インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-215">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="7a554-216">**シークレットを作成** ダイアログ ボックスの **アップロード オプション** フィールドで、**手動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-216">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="7a554-217">次の表から、シークレットの名前と値を作成します。</span><span class="sxs-lookup"><span data-stu-id="7a554-217">Create the secret name and value from the table.</span></span>
        4. <span data-ttu-id="7a554-218">**有効** を選択し、**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-218">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="7a554-219">シークレットが作成され、Key Vault に追加されます。</span><span class="sxs-lookup"><span data-stu-id="7a554-219">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="7a554-220">シークレット名</span><span class="sxs-lookup"><span data-stu-id="7a554-220">Secret name</span></span>                       | <span data-ttu-id="7a554-221">シークレットの値</span><span class="sxs-lookup"><span data-stu-id="7a554-221">Secret value</span></span>                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | <span data-ttu-id="7a554-222">アプリ ID</span><span class="sxs-lookup"><span data-stu-id="7a554-222">app-id</span></span>                            | <span data-ttu-id="7a554-223">先ほど作成したアプリケーションのアプリ ID です。</span><span class="sxs-lookup"><span data-stu-id="7a554-223">The app ID of the application that you created earlier.</span></span>                                      |
        | <span data-ttu-id="7a554-224">アプリのシークレット</span><span class="sxs-lookup"><span data-stu-id="7a554-224">app-secret</span></span>                        | <span data-ttu-id="7a554-225">先ほど保存したクライアント シークレットです。</span><span class="sxs-lookup"><span data-stu-id="7a554-225">The client secret that you saved earlier.</span></span>                                                    |
        | <span data-ttu-id="7a554-226">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="7a554-226">storage-account-name</span></span>              | <span data-ttu-id="7a554-227">前に作成したストレージ アカウントの名前です (例: **sstorageaccount1**)。</span><span class="sxs-lookup"><span data-stu-id="7a554-227">The name of the storage account that you created earlier, such as **storageaccount1**.</span></span>       |

5. <span data-ttu-id="7a554-228">アプリケーションを承認してキー コンテナーにアクセスする方法:</span><span class="sxs-lookup"><span data-stu-id="7a554-228">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="7a554-229">[Azure portal](https://portal.azure.com)で、作成済のキー コンテナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="7a554-229">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="7a554-230">アクセス ポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-230">Select the access policies.</span></span>
    3. <span data-ttu-id="7a554-231">次のアプリケーションに対して、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7a554-231">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="7a554-232">**アクセス ポリシー** を選択し、アクセス ポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="7a554-232">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="7a554-233">**シークレットのアクセス許可** フィールドで、テーブルからアクセス許可を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-233">In the **Secret permissions** field, select the permissions from the table.</span></span>
        3. <span data-ttu-id="7a554-234">**プリンシパルの選択** フィールドで、テーブルからアプリケーションの表示名を検索します。</span><span class="sxs-lookup"><span data-stu-id="7a554-234">In the **Select principal** field, search for the application display name from the table.</span></span>
        4. <span data-ttu-id="7a554-235">**選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-235">Select **Select**.</span></span>
        5. <span data-ttu-id="7a554-236">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-236">Select **Add**.</span></span>
        6. <span data-ttu-id="7a554-237">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-237">Select **Save**.</span></span>

        | <span data-ttu-id="7a554-238">申請書</span><span class="sxs-lookup"><span data-stu-id="7a554-238">Application</span></span>                                              | <span data-ttu-id="7a554-239">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="7a554-239">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="7a554-240">作成した新しいアプリケーションの表示名称</span><span class="sxs-lookup"><span data-stu-id="7a554-240">The display name of the new application that you created</span></span> | <span data-ttu-id="7a554-241">取得、リスト表示</span><span class="sxs-lookup"><span data-stu-id="7a554-241">Get, List</span></span>   |
        | <span data-ttu-id="7a554-242">**Microsoft Dynamics ERP マイクロサービス**</span><span class="sxs-lookup"><span data-stu-id="7a554-242">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="7a554-243">取得、リスト表示</span><span class="sxs-lookup"><span data-stu-id="7a554-243">Get, List</span></span>   |

6. <span data-ttu-id="7a554-244">ストレージ アカウントにアクセスするロールを割り当てるには、次の操作を行います:</span><span class="sxs-lookup"><span data-stu-id="7a554-244">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="7a554-245">[Azure ポータル](https://portal.azure.com)で、作成済のストレージ アカウントを開きます。</span><span class="sxs-lookup"><span data-stu-id="7a554-245">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="7a554-246">**アクセスの制御 (IAM)** を選択し 、**ロールの割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-246">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="7a554-247">**追加、 ロールの割り当ての追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-247">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="7a554-248">次のアプリケーションに対して、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7a554-248">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="7a554-249">テーブルからロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-249">Select the role from the table.</span></span>
        2. <span data-ttu-id="7a554-250">**アクセス権の割り当て先** シールドは、**Azure AD ユーザー、グループ、またはサービス プリンシパル** のままにします。</span><span class="sxs-lookup"><span data-stu-id="7a554-250">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="7a554-251">**選択** フィールドで、テーブルからアプリケーションを入力します。</span><span class="sxs-lookup"><span data-stu-id="7a554-251">In the **Select** field, enter the application from the table.</span></span>
        4. <span data-ttu-id="7a554-252">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-252">Select **Save**.</span></span>

        | <span data-ttu-id="7a554-253">申請書</span><span class="sxs-lookup"><span data-stu-id="7a554-253">Application</span></span>                                              | <span data-ttu-id="7a554-254">役割</span><span class="sxs-lookup"><span data-stu-id="7a554-254">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="7a554-255">作成した新しいアプリケーションの表示名称</span><span class="sxs-lookup"><span data-stu-id="7a554-255">The display name of the new application that you created</span></span> | <span data-ttu-id="7a554-256">所有者</span><span class="sxs-lookup"><span data-stu-id="7a554-256">Owner</span></span>                       |
        | <span data-ttu-id="7a554-257">作成した新しいアプリケーションの表示名称</span><span class="sxs-lookup"><span data-stu-id="7a554-257">The display name of the new application that you created</span></span> | <span data-ttu-id="7a554-258">寄稿者</span><span class="sxs-lookup"><span data-stu-id="7a554-258">Contributor</span></span>                 |
        | <span data-ttu-id="7a554-259">作成した新しいアプリケーションの表示名称</span><span class="sxs-lookup"><span data-stu-id="7a554-259">The display name of the new application that you created</span></span> | <span data-ttu-id="7a554-260">ストレージ アカウントの共同作成者</span><span class="sxs-lookup"><span data-stu-id="7a554-260">Storage Account Contributor</span></span> |
        | <span data-ttu-id="7a554-261">作成した新しいアプリケーションの表示名称</span><span class="sxs-lookup"><span data-stu-id="7a554-261">The display name of the new application that you created</span></span> | <span data-ttu-id="7a554-262">ストレージ BLOB データの所有者</span><span class="sxs-lookup"><span data-stu-id="7a554-262">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="7a554-263">**AI Builder の承認サービス**</span><span class="sxs-lookup"><span data-stu-id="7a554-263">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="7a554-264">ストレージ BLOB データの読み取り</span><span class="sxs-lookup"><span data-stu-id="7a554-264">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="7a554-265">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="7a554-265">Azure CLI</span></span>](#tab/azure-azure-cli)

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

## <a name="configure-the-export-to-data-lake-add-in"></a><span data-ttu-id="7a554-266">Data Lake アドインへのエクスポートの構成</span><span class="sxs-lookup"><span data-stu-id="7a554-266">Configure the Export to Data Lake add-in</span></span>

<span data-ttu-id="7a554-267">LCS を使用して Data Lake アドインを環境へのエクスポートを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7a554-267">Follow these steps to use LCS to add the Export to Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="7a554-268">LCS にログインし、ページの右側にある環境名の下の **完全な詳細** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="7a554-268">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="7a554-269">**環境アドイン** セクションで、**新しいアドインのインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-269">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="7a554-270">**Data Lake へのエクスポート** アドインを選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-270">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="7a554-271">次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7a554-271">Enter the following values.</span></span>

    | <span data-ttu-id="7a554-272">先頭値</span><span class="sxs-lookup"><span data-stu-id="7a554-272">Value</span></span>                                                              | <span data-ttu-id="7a554-273">説明</span><span class="sxs-lookup"><span data-stu-id="7a554-273">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="7a554-274">キーの保管場所がある Azure サブスクリプションのテナント ID</span><span class="sxs-lookup"><span data-stu-id="7a554-274">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="7a554-275">ストレージ アカウント、アプリ、キーコンテナーが配置されているテナント ID です。</span><span class="sxs-lookup"><span data-stu-id="7a554-275">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="7a554-276">この値を取得するには、[Azure portal](https://portal.azure.com) を開き、**Azure Active Directory** に移動し、**テナント ID** の値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="7a554-276">To obtain this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="7a554-277">Key Vault の DNS 名を指定する</span><span class="sxs-lookup"><span data-stu-id="7a554-277">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="7a554-278">キー コンテナーの DNS 名 (例:  `https://customkeyvault.vault.azure.net/`)。</span><span class="sxs-lookup"><span data-stu-id="7a554-278">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> |
    | <span data-ttu-id="7a554-279">ストレージ アカウントの名前を含むシークレットを指定します</span><span class="sxs-lookup"><span data-stu-id="7a554-279">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="7a554-280">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="7a554-280">**storage-account-name**</span></span> |
    | <span data-ttu-id="7a554-281">Data Lake へのアクセスに使用するアプリ ID のシークレット名</span><span class="sxs-lookup"><span data-stu-id="7a554-281">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="7a554-282">**アプリの ID**</span><span class="sxs-lookup"><span data-stu-id="7a554-282">**app-id**</span></span> |
    | <span data-ttu-id="7a554-283">アプリケーションのクライアント シークレットのシークレット名</span><span class="sxs-lookup"><span data-stu-id="7a554-283">Secret name for App client secret</span></span>                                  | <span data-ttu-id="7a554-284">**アプリのシークレット**</span><span class="sxs-lookup"><span data-stu-id="7a554-284">**app-secret**</span></span> |

5. <span data-ttu-id="7a554-285">条件に同意し、**インストール** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="7a554-285">Agree to the terms, and then select **Install**.</span></span>

<span data-ttu-id="7a554-286">このアドインは数分以内にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="7a554-286">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-the-finance-insights-add-in"></a><span data-ttu-id="7a554-287">Finance Insights アドインの構成</span><span class="sxs-lookup"><span data-stu-id="7a554-287">Configure the Finance insights add-in</span></span>

> [!NOTE]
> <span data-ttu-id="7a554-288">既に Get insights アドインをインストールしていた場合は、アンインストールしてから次の手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="7a554-288">If you previously installed the Get insights add-in, uninstall it before you complete the following procedure.</span></span>

<span data-ttu-id="7a554-289">以下の手順で Finance insights アドインをインストールします。</span><span class="sxs-lookup"><span data-stu-id="7a554-289">Follow these steps to install the Finance insights add-in.</span></span>

1. <span data-ttu-id="7a554-290">LCS にログインし、ページの右側にある環境名の下の **完全な詳細** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="7a554-290">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="7a554-291">**環境アドイン** セクションで、**新しいアドインのインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-291">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="7a554-292">**Finance insights** アドインを選択します。</span><span class="sxs-lookup"><span data-stu-id="7a554-292">Select the **Finance insights** add-in.</span></span>
4. <span data-ttu-id="7a554-293">条件に同意し、**インストール** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="7a554-293">Agree to the terms, and then select **Install**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="7a554-294">フィードバックとサポート</span><span class="sxs-lookup"><span data-stu-id="7a554-294">Feedback and support</span></span>

<span data-ttu-id="7a554-295">フィードバックに興味のある方、サポートが必要な方は、[Finance insights (プレビュー)](mailto:fiap@microsoft.com) にメールでお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="7a554-295">If you're interested in providing feedback, or if you require support, send an email to [Finance insights (Preview)](mailto:fiap@microsoft.com).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
