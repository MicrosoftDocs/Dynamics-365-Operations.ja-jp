---
title: 在庫の視覚化アドイン
description: このトピックでは、Dynamics 365 Supply Chain Management の在庫の視覚化アドインのインストールおよび構成方法を説明します。
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e588be2ac5aae395ca66e3c9a743a67d71db7c0
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574225"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="4f1fa-103">在庫の視覚化アドイン</span><span class="sxs-lookup"><span data-stu-id="4f1fa-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="4f1fa-104">Inventory Visibility Add-in は、リアルタイムで手持在庫を追跡可能できる独立したスケーラブルなマイクロサービスで、グローバルなビューの在庫表示が実現します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="4f1fa-105">手持在庫に関連するすべての情報は、低レベルの SQL 統合を通じて準リアルタイムでサービスにエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="4f1fa-106">外部システムは RESTful APIs を通じてサービスにアクセスし、指定された分析コードの組み合わせに関する手持在庫情報にクエリを実行します。こうすることで使用可能な手持在庫の一覧を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="4f1fa-107">Inventory Visibility は、Microsoft Dataverse に構築されたマイクロサービスなので、Power Apps を構築および Power BI を適用することで拡張し、カスタマイズした機能を提供して、業務要件を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="4f1fa-108">インデックスをアップグレードして在庫クエリを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="4f1fa-109">Inventory Visibility には、複数のサードパーティ システムと統合できる構成オプションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="4f1fa-110">このオプションでは、標準化された在庫分析コード、カスタマイズされた拡張性、標準化され構成可能な計算済の数量がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="4f1fa-111">このトピックでは、Inventory Visibility Add-in for Dynamics 365 Supply Chain Management のインストールおよび構成方法、およびアプリケーション プログラミング インターフェイス (API) の使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="4f1fa-112">Inventory Visibility Add-in をインストールする</span><span class="sxs-lookup"><span data-stu-id="4f1fa-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="4f1fa-113">Microsoft Dynamics Lifecycle Services (LCS) を使用して、 Inventory Visibility Add-in をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="4f1fa-114">LCS が提供する環境や定期的に更新されるサービスにより、Dynamics 365 Finance and Operations アプリのアプリケーション ライフサイクルを管理するのが楽になります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="4f1fa-115">詳細については、 [Lifecycle Services のリソース](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="4f1fa-116">必要条件</span><span class="sxs-lookup"><span data-stu-id="4f1fa-116">Prerequisites</span></span>

<span data-ttu-id="4f1fa-117">Inventory Visibility Add-in をインストールする前に、以下を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="4f1fa-118">少なくとも 1 つの環境が配置されている LCS 実装プロジェクトを取得する。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="4f1fa-119">[アドインの概要](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)で提供されるアドインを設定するための前提条件が完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="4f1fa-120">在庫の視覚化にデュアル書き込みリンクは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="4f1fa-121">[inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) から在庫の視覚化チームに連絡して、次の 3 つの必要なファイルを入手してください。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>

    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="4f1fa-122">`Inventory Visibility Integration.zip` (実行している Supply Chain Management がバージョン 10.0.18 より以前のバージョンの場合)</span><span class="sxs-lookup"><span data-stu-id="4f1fa-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>

> [!NOTE]
> <span data-ttu-id="4f1fa-123">現在サポートされている国や地域には、カナダ、米国、欧州連合 (EU) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-123">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="4f1fa-124">これらの前提条件について質問がある場合は、Inventory Visibility 製品チームに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-124">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="4f1fa-125">Dataverse を設定する</span><span class="sxs-lookup"><span data-stu-id="4f1fa-125">Set up Dataverse</span></span>

<span data-ttu-id="4f1fa-126">Dataverse を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-126">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="4f1fa-127">テナントにサービス プリンシパルを追加します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-127">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="4f1fa-128">[Graph 用 Azure Active Directory  PowerShell をインストールする](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2)に記載の手順に従って Azure AD PowerShell モジュール v2 をインストールします。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-128">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="4f1fa-129">次の PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-129">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="4f1fa-130">Dataverse で在庫の視覚化のアプリケーション ユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-130">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="4f1fa-131">Dataverse 環境の URLを開きます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-131">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="4f1fa-132">**詳細設定 \> システム \> セキュリティ \> ユーザー** の順に移動し、アプリケーション ユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-132">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="4f1fa-133">表示メニューを使用して、ページ ビューを **アプリケーション ユーザー** に変更します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-133">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="4f1fa-134">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-134">Select **New**.</span></span> <span data-ttu-id="4f1fa-135">アプリケーション ID を *3022308a-b9bd-4a18-b8ac-2ddedb2075e1* に設定します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-135">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="4f1fa-136">(変更を保存すると、オブジェクト ID が自動的に読み込まれます。) 名前はカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-136">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="4f1fa-137">たとえば、*在庫の視覚化* に変更できます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-137">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="4f1fa-138">完了したら、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-138">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="4f1fa-139">**ロールの割り当て** を選択してから、**システム管理者** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-139">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="4f1fa-140">**Common Data Service ユーザー** という名前のロールがある場合は、それも選択します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-140">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="4f1fa-141">詳細については、「[アプリケーション ユーザーの作成](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-141">For more information, see [Create an application user](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="4f1fa-142">Dataverse 構成関連エンティティと Power Apps を含む `Inventory Visibility Dataverse Solution.zip` ファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-142">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="4f1fa-143">**ソリューション** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-143">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="4f1fa-144">**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-144">Select **Import**.</span></span>

1. <span data-ttu-id="4f1fa-145">構成のアップグレード トリガー フローをインポートします。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-145">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="4f1fa-146">Microsoft Flow ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-146">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="4f1fa-147">*Dataverse (レガシ)* という名前の接続が存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-147">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="4f1fa-148">(存在しない場合は作成します。)</span><span class="sxs-lookup"><span data-stu-id="4f1fa-148">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="4f1fa-149">`Inventory Visibility Configuration Trigger.zip` ファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-149">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="4f1fa-150">インポートすると、トリガーが **マイ フロー** の下に表示されます 。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-150">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="4f1fa-151">環境情報に基づいて、次の 4 つの変数を初期化します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-151">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="4f1fa-152">Azure テナント ID</span><span class="sxs-lookup"><span data-stu-id="4f1fa-152">Azure Tenant ID</span></span>
        - <span data-ttu-id="4f1fa-153">Azure アプリケーション クライアント ID</span><span class="sxs-lookup"><span data-stu-id="4f1fa-153">Azure Application Client ID</span></span>
        - <span data-ttu-id="4f1fa-154">Azure アプリケーション クライアント シークレット</span><span class="sxs-lookup"><span data-stu-id="4f1fa-154">Azure Application Client Secret</span></span>
        - <span data-ttu-id="4f1fa-155">在庫の視覚化エンドポイント</span><span class="sxs-lookup"><span data-stu-id="4f1fa-155">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="4f1fa-156">この変数の詳細については、このトピックで後述する[在庫の視覚化統合の設定](#setup-inventory-visibility-integration) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-156">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="4f1fa-157">![構成トリガー](media/configuration-trigger.png "構成トリガー")</span><span class="sxs-lookup"><span data-stu-id="4f1fa-157">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="4f1fa-158">**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-158">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="4f1fa-159">アドインのインストール</span><span class="sxs-lookup"><span data-stu-id="4f1fa-159">Install the add-in</span></span>

<span data-ttu-id="4f1fa-160">Inventory Visibility Add-in をインストールするには、以下を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-160">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="4f1fa-161">[Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) ポータルにサインインします。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-161">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="4f1fa-162">ホーム ページで、環境が展開されているプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-162">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="4f1fa-163">プロジェクト ページで、アドインをインストールする環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-163">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="4f1fa-164">環境ページで、**Power Platform 統合** セクションの **環境アドイン** セクションが表示されるまで下にスクロールします。このセクションでは Dataverse 環境名を検索できます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-164">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="4f1fa-165">**環境アドイン** セクションで、**新しいアドインのインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-165">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="4f1fa-166">![LCS の環境ページ](media/inventory-visibility-environment.png "LCS の環境ページ")</span><span class="sxs-lookup"><span data-stu-id="4f1fa-166">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="4f1fa-167">**新しいアドインのインストール** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-167">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="4f1fa-168">使用可能なアドインの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-168">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="4f1fa-169">一覧で **在庫の視覚化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-169">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="4f1fa-170">環境に対して次のフィールドの値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-170">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="4f1fa-171">**AAD アプリケーション (クライアント) ID**</span><span class="sxs-lookup"><span data-stu-id="4f1fa-171">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="4f1fa-172">**AAD テナント ID**</span><span class="sxs-lookup"><span data-stu-id="4f1fa-172">**AAD tenant ID**</span></span>

    <span data-ttu-id="4f1fa-173">![セットアップ ページに追加](media/inventory-visibility-setup.png "アドイン セットアップ ページ")</span><span class="sxs-lookup"><span data-stu-id="4f1fa-173">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="4f1fa-174">**使用条件** チェック ボックスを選択して、使用条件に同意します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-174">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="4f1fa-175">**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-175">Select **Install**.</span></span> <span data-ttu-id="4f1fa-176">アドインの状態は、**インストール中** として表示されます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-176">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="4f1fa-177">完了したらページを更新して、状態が **インストール済み** に変わっているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-177">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="4f1fa-178">アドインのアンインストール</span><span class="sxs-lookup"><span data-stu-id="4f1fa-178">Uninstall the add-in</span></span>

<span data-ttu-id="4f1fa-179">アドインをアンインストールするには、**アンインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-179">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="4f1fa-180">LCS を更新すると、在庫の視覚化アドインが削除されます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-180">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="4f1fa-181">アンインストールのプロセスでは、アドイン登録が削除され、サービスに格納されているすべてのビジネス データをクリーンアップするジョブが開始されます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-181">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="4f1fa-182">Supply Chain Management からの手持在庫データの消費</span><span class="sxs-lookup"><span data-stu-id="4f1fa-182">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="4f1fa-183">在庫の視覚化統合パッケージの配置</span><span class="sxs-lookup"><span data-stu-id="4f1fa-183">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="4f1fa-184">Supply Chain Management バージョン 10.0.17 以前を実行している場合、[inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) で在庫の視覚化のオンボード サポート チームに連絡してパッケージ ファイルを取得してください。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-184">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="4f1fa-185">その後、LCS にパッケージを配置します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-185">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="4f1fa-186">配置中にバージョンの不一致エラーが発生した場合は、X++ プロジェクトを手動で開発環境にインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-186">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="4f1fa-187">その後、配置可能パッケージを開発環境に作成し、それを実稼働環境に配置します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-187">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="4f1fa-188">このコードは Supply Chain Management バージョン 10.0.18 に含まれています。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-188">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="4f1fa-189">そのバージョン以降を実行する場合、配置は必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-189">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="4f1fa-190">Supply Chain Management 環境で次の機能が有効になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-190">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="4f1fa-191">(既定では、有効になっています。)</span><span class="sxs-lookup"><span data-stu-id="4f1fa-191">(By default, they are turned on.)</span></span>

| <span data-ttu-id="4f1fa-192">機能の説明</span><span class="sxs-lookup"><span data-stu-id="4f1fa-192">Feature description</span></span> | <span data-ttu-id="4f1fa-193">コード バージョン</span><span class="sxs-lookup"><span data-stu-id="4f1fa-193">Code version</span></span> | <span data-ttu-id="4f1fa-194">トグル クラス</span><span class="sxs-lookup"><span data-stu-id="4f1fa-194">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="4f1fa-195">InventSum テーブルで在庫分析コードの使用の有効化または無効化</span><span class="sxs-lookup"><span data-stu-id="4f1fa-195">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="4f1fa-196">10.0.11</span><span class="sxs-lookup"><span data-stu-id="4f1fa-196">10.0.11</span></span> | <span data-ttu-id="4f1fa-197">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="4f1fa-197">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="4f1fa-198">InventSumDelta テーブルで在庫分析コードの使用の有効化または無効化</span><span class="sxs-lookup"><span data-stu-id="4f1fa-198">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="4f1fa-199">10.0.12</span><span class="sxs-lookup"><span data-stu-id="4f1fa-199">10.0.12</span></span> | <span data-ttu-id="4f1fa-200">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="4f1fa-200">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="4f1fa-201">Inventory Visibility 統合の設定</span><span class="sxs-lookup"><span data-stu-id="4f1fa-201">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="4f1fa-202">Supply Chain Management で、**[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** ワークスペースを開き、在庫の可視性の **在庫の視覚化統合** 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-202">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="4f1fa-203">**在庫管理 \> 設定 \>在庫の視覚化統合パラメーター** の順に移動し、実行している在庫の視覚化で環境の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-203">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="4f1fa-204">LCS 環境の Azure リージョンを検索してから、URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-204">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="4f1fa-205">URL には次のフォームがあります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-205">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="4f1fa-206">たとえば、ヨーロッパにいる場合、環境には次のいずれかの URL が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-206">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com/`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="4f1fa-207">現在、以下のリージョンが利用可能です。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-207">The following regions are currently available.</span></span>

    | <span data-ttu-id="4f1fa-208">Azure リージョン</span><span class="sxs-lookup"><span data-stu-id="4f1fa-208">Azure region</span></span> | <span data-ttu-id="4f1fa-209">リージョンの短縮名</span><span class="sxs-lookup"><span data-stu-id="4f1fa-209">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="4f1fa-210">オーストラリア東部</span><span class="sxs-lookup"><span data-stu-id="4f1fa-210">Australia east</span></span> | <span data-ttu-id="4f1fa-211">eau</span><span class="sxs-lookup"><span data-stu-id="4f1fa-211">eau</span></span> |
    | <span data-ttu-id="4f1fa-212">オーストラリア南東部</span><span class="sxs-lookup"><span data-stu-id="4f1fa-212">Australia southeast</span></span> | <span data-ttu-id="4f1fa-213">seau</span><span class="sxs-lookup"><span data-stu-id="4f1fa-213">seau</span></span> |
    | <span data-ttu-id="4f1fa-214">カナダ中部</span><span class="sxs-lookup"><span data-stu-id="4f1fa-214">Canada central</span></span> | <span data-ttu-id="4f1fa-215">cca</span><span class="sxs-lookup"><span data-stu-id="4f1fa-215">cca</span></span> |
    | <span data-ttu-id="4f1fa-216">カナダ東部</span><span class="sxs-lookup"><span data-stu-id="4f1fa-216">Canada east</span></span> | <span data-ttu-id="4f1fa-217">eca</span><span class="sxs-lookup"><span data-stu-id="4f1fa-217">eca</span></span> |
    | <span data-ttu-id="4f1fa-218">北ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="4f1fa-218">North Europe</span></span> | <span data-ttu-id="4f1fa-219">neu</span><span class="sxs-lookup"><span data-stu-id="4f1fa-219">neu</span></span> |
    | <span data-ttu-id="4f1fa-220">西ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="4f1fa-220">West Europe</span></span> | <span data-ttu-id="4f1fa-221">weu</span><span class="sxs-lookup"><span data-stu-id="4f1fa-221">weu</span></span> |
    | <span data-ttu-id="4f1fa-222">米国東部</span><span class="sxs-lookup"><span data-stu-id="4f1fa-222">East US</span></span> | <span data-ttu-id="4f1fa-223">eus</span><span class="sxs-lookup"><span data-stu-id="4f1fa-223">eus</span></span> |
    | <span data-ttu-id="4f1fa-224">米国西部</span><span class="sxs-lookup"><span data-stu-id="4f1fa-224">West US</span></span> | <span data-ttu-id="4f1fa-225">wus</span><span class="sxs-lookup"><span data-stu-id="4f1fa-225">wus</span></span> |

1. <span data-ttu-id="4f1fa-226">**在庫管理 \> 定期処理 \> 在庫の視覚化統合** の順に移動し、ジョブを有効します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-226">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="4f1fa-227">Supply Chain Management からのすべての在庫変更イベントが在庫の視覚化に転記されるようになります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-227">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="4f1fa-228">在庫の視覚化アドイン パブリック API</span><span class="sxs-lookup"><span data-stu-id="4f1fa-228">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="4f1fa-229">在庫の視覚化アドインのパブリック REST API は、特定の統合エンドポイントを複数提供します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-229">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="4f1fa-230">次の 3 つの主要な相互作用タイプをサポートします。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-230">It supports three main interaction types:</span></span>

- <span data-ttu-id="4f1fa-231">外部システムから、手持在庫の変更をアドインに転記する</span><span class="sxs-lookup"><span data-stu-id="4f1fa-231">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="4f1fa-232">外部システムから現在の手持在庫数量を問い合わせる</span><span class="sxs-lookup"><span data-stu-id="4f1fa-232">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="4f1fa-233">Supply Chain Management 手持在庫との自動同期</span><span class="sxs-lookup"><span data-stu-id="4f1fa-233">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="4f1fa-234">自動同期はパブリック API の一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-234">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="4f1fa-235">代わりに、在庫の視覚化アドインが有効になっている環境のバックグラウンドで処理されます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-235">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="4f1fa-236">認証</span><span class="sxs-lookup"><span data-stu-id="4f1fa-236">Authentication</span></span>

<span data-ttu-id="4f1fa-237">プラットフォーム セキュリティ トークンは、在庫の視覚化アドインを呼び出すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-237">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="4f1fa-238">したがって、Azure AD アプリケーションを使用して *Azure Active Directory (Azure AD) トークン* を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-238">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="4f1fa-239">その後、この Azure AD トークンを使用して、セキュリティ サービスから *アクセス トークン* を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-239">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="4f1fa-240">セキュリティ サービス トークンを取得するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-240">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="4f1fa-241">Azure ポータルにサインインし、このサインインを使用して Supply Chain Management アプリケーションの `clientId` と `clientSecret` を検索します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-241">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="4f1fa-242">次のプロパティを持つ HTTP 要求を送信することにより、 Azure Active Directory トークン (`aadToken`) をフェッチします。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-242">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="4f1fa-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="4f1fa-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="4f1fa-244">**メソッド** - `GET`</span><span class="sxs-lookup"><span data-stu-id="4f1fa-244">**Method** - `GET`</span></span>
    - <span data-ttu-id="4f1fa-245">**本文の内容 (フォーム データ)**:</span><span class="sxs-lookup"><span data-stu-id="4f1fa-245">**Body content (form data)**:</span></span>

        | <span data-ttu-id="4f1fa-246">キー</span><span class="sxs-lookup"><span data-stu-id="4f1fa-246">key</span></span> | <span data-ttu-id="4f1fa-247">値</span><span class="sxs-lookup"><span data-stu-id="4f1fa-247">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="4f1fa-248">クライアント ID</span><span class="sxs-lookup"><span data-stu-id="4f1fa-248">client_id</span></span> | <span data-ttu-id="4f1fa-249">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="4f1fa-249">${aadAppId}</span></span> |
        | <span data-ttu-id="4f1fa-250">クライアント シークレット</span><span class="sxs-lookup"><span data-stu-id="4f1fa-250">client_secret</span></span> | <span data-ttu-id="4f1fa-251">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="4f1fa-251">${aadAppSecret}</span></span> |
        | <span data-ttu-id="4f1fa-252">付与タイプ</span><span class="sxs-lookup"><span data-stu-id="4f1fa-252">grant_type</span></span> | <span data-ttu-id="4f1fa-253">client_credentials</span><span class="sxs-lookup"><span data-stu-id="4f1fa-253">client_credentials</span></span> |
        | <span data-ttu-id="4f1fa-254">リソース</span><span class="sxs-lookup"><span data-stu-id="4f1fa-254">resource</span></span> | <span data-ttu-id="4f1fa-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="4f1fa-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="4f1fa-256">応答で `aadToken` を受け取っている必要があります。これは次の例と似ています。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-256">You should receive an `aadToken` in response, which resembles the following example.</span></span>

    ```json
    {
    "token_type": "Bearer",
    "expires_in": "3599",
    "ext_expires_in": "3599",
    "expires_on": "1610466645",
    "not_before": "1610462745",
    "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
    "access_token": "eyJ0eX...8WQ"
    }
    ```

1. <span data-ttu-id="4f1fa-257">次に似た JSON 要求を形成します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-257">Formulate a JSON request that resembles the following:</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    <span data-ttu-id="4f1fa-258">場所:</span><span class="sxs-lookup"><span data-stu-id="4f1fa-258">Where:</span></span>
    - <span data-ttu-id="4f1fa-259">`client_assertion` 値は、前の手順で受け取った `aadToken` である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-259">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="4f1fa-260">この `context` 値は、アドインを配置する環境 ID である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-260">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="4f1fa-261">例に示すように、他のすべての値を設定します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-261">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="4f1fa-262">次のプロパティを使用して HTTP 要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-262">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="4f1fa-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="4f1fa-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="4f1fa-264">**メソッド** - `POST`</span><span class="sxs-lookup"><span data-stu-id="4f1fa-264">**Method** - `POST`</span></span>
    - <span data-ttu-id="4f1fa-265">**HTTP ヘッダー** - API バージョンを含めます (キーは `Api-Version` で値は `1.0` です)</span><span class="sxs-lookup"><span data-stu-id="4f1fa-265">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="4f1fa-266">**本文の内容** - 前の手順で作成した JSON 要求を含めます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-266">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="4f1fa-267">`access_token` を取得します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-267">You will get an `access_token` in response.</span></span> <span data-ttu-id="4f1fa-268">これは、Inventory Visibility API を呼び出すためのベアラー トークンとして必要なものです。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-268">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="4f1fa-269">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-269">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="4f1fa-270">Inventory Visibility API の構成</span><span class="sxs-lookup"><span data-stu-id="4f1fa-270">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="4f1fa-271">このサービスを使用する前に、次のサブセクションで説明する構成を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-271">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="4f1fa-272">環境の詳細によって、構成が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-272">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="4f1fa-273">主に 4 つの部分から構成されます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-273">It primarily includes four parts:</span></span>

- [<span data-ttu-id="4f1fa-274">パーティション分割</span><span class="sxs-lookup"><span data-stu-id="4f1fa-274">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="4f1fa-275">分析コードの構成</span><span class="sxs-lookup"><span data-stu-id="4f1fa-275">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="4f1fa-276">インデックスの作成中</span><span class="sxs-lookup"><span data-stu-id="4f1fa-276">Indexing</span></span>](#indexing)
- [<span data-ttu-id="4f1fa-277">カスタム測定</span><span class="sxs-lookup"><span data-stu-id="4f1fa-277">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="4f1fa-278">パーティション分割</span><span class="sxs-lookup"><span data-stu-id="4f1fa-278">Partitioning</span></span>

<span data-ttu-id="4f1fa-279">パーティション分割は、Inventory Visibility API のパフォーマンスに大きな影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-279">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="4f1fa-280">有意義なデータ クエリの使用を妥協せずに、データを小規模にグループ化できるスキームを定義することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-280">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="4f1fa-281">`organizationId` (Supply Chain Management の `dataAreaId`) は、常にパーティション分割に含まれており、Inventory Visibility は既定で、*サイト + 場所* として分析コードごとのパーティション分割が設定されているので、</span><span class="sxs-lookup"><span data-stu-id="4f1fa-281">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="4f1fa-282">フィルターで定義された分析コードで、サービスを常にクエリを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-282">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="4f1fa-283">*サイト* および *場所* は、Inventory Visibility で使用する 2 つの既定の標準分析コードです。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-283">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="4f1fa-284">Supply Chain Management では、これらの分析コードは *サイト* ( `InventSiteId`) および *倉庫* (`InventLocationId`) と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-284">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="4f1fa-285">分析コードの構成</span><span class="sxs-lookup"><span data-stu-id="4f1fa-285">Dimension configurations</span></span>

<span data-ttu-id="4f1fa-286">Inventory Visibility に既定の標準分析コードの一覧が用意されており、複数のソース システムの統合を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-286">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="4f1fa-287">次のテーブルでは、Inventory Visibility で既定の分析コード名となる在庫分析コードを一覧表示しています。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-287">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="4f1fa-288">分析コード タイプ</span><span class="sxs-lookup"><span data-stu-id="4f1fa-288">Dimension type</span></span> | <span data-ttu-id="4f1fa-289">分析コード名</span><span class="sxs-lookup"><span data-stu-id="4f1fa-289">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="4f1fa-290">品目</span><span class="sxs-lookup"><span data-stu-id="4f1fa-290">Product</span></span> | `ColorId` |
| <span data-ttu-id="4f1fa-291">品目</span><span class="sxs-lookup"><span data-stu-id="4f1fa-291">Product</span></span> | `SizeId` |
| <span data-ttu-id="4f1fa-292">品目</span><span class="sxs-lookup"><span data-stu-id="4f1fa-292">Product</span></span> | `StyleId` |
| <span data-ttu-id="4f1fa-293">品目</span><span class="sxs-lookup"><span data-stu-id="4f1fa-293">Product</span></span> | `ConfigId` |
| <span data-ttu-id="4f1fa-294">追跡</span><span class="sxs-lookup"><span data-stu-id="4f1fa-294">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="4f1fa-295">追跡</span><span class="sxs-lookup"><span data-stu-id="4f1fa-295">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="4f1fa-296">保管場所</span><span class="sxs-lookup"><span data-stu-id="4f1fa-296">Location</span></span> | `LocationId` |
| <span data-ttu-id="4f1fa-297">保管場所</span><span class="sxs-lookup"><span data-stu-id="4f1fa-297">Location</span></span> | `SiteId` |
| <span data-ttu-id="4f1fa-298">在庫状態</span><span class="sxs-lookup"><span data-stu-id="4f1fa-298">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="4f1fa-299">倉庫固有</span><span class="sxs-lookup"><span data-stu-id="4f1fa-299">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="4f1fa-300">倉庫固有</span><span class="sxs-lookup"><span data-stu-id="4f1fa-300">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="4f1fa-301">倉庫固有</span><span class="sxs-lookup"><span data-stu-id="4f1fa-301">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="4f1fa-302">前のテーブルで表示されていた分析コード タイプは、参照のみに使用されます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-302">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="4f1fa-303">Inventory Visibility で分析コード タイプを定義する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-303">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="4f1fa-304">カスタム分析コードが存在し、Inventory Visibility で使用したときに既定値に送る必要がある場合は、Inventory Visibility で **カスタム分析コード** 名を構成できます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-304">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="4f1fa-305">RESTful APIs を使用して外部システムが Inventory Visibility へアクセスし、クエリを実行する特定の分析コードに関する手持在庫情報を入手できます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-305">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="4f1fa-306">統合に関しては、Inventory Visibility を使用すると、Inventory Visibility で *ターゲット分析コード* への *外部チャネル データソース* とソース分析コードを構成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-306">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="4f1fa-307">ターゲット分析コードは、次のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-307">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="4f1fa-308">Inventory Visibility の既定分析コード</span><span class="sxs-lookup"><span data-stu-id="4f1fa-308">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="4f1fa-309">カスタム分析コード</span><span class="sxs-lookup"><span data-stu-id="4f1fa-309">Custom dimensions</span></span>

<span data-ttu-id="4f1fa-310">分析コードを構成する目的は、分析コードおよび分析コードを含む転記イベントに関するクエリで使用する複数のシステム統合を標準化することです。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-310">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="4f1fa-311">インデックスの作成中</span><span class="sxs-lookup"><span data-stu-id="4f1fa-311">Indexing</span></span>

<span data-ttu-id="4f1fa-312">ほとんどの場合、手持在庫クエリは、最高 "合計" レベルのみだけではなく、在庫分析コードに基づいて集計された結果も表示することができます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-312">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="4f1fa-313">Inventory Visibility を使用すると、分析コードまたは分析コードの組み合わせに基づいてインデックスを設定できるので、柔軟性を高めることができます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-313">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="4f1fa-314">現在構成できるインデックスは、最大でわずか 5 つです。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-314">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="4f1fa-315">業務上のニーズを満たすには、実装する前に、どの分析コードまたは分析コードの組み合わせを使用するかを慎重に検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-315">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="4f1fa-316">たとえば、次のように製品にクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-316">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="4f1fa-317">*色* と *サイズ* の分析コード別に、集計された製品の手持在庫にクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-317">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="4f1fa-318">場合によっては、製品全体にクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-318">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="4f1fa-319">次のように定義されているインデックスが 2 つあるとします。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-319">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="4f1fa-320">空の括弧は、パーティションの製品 ID に基づいて集計されます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-320">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="4f1fa-321">インデックスは、`groupBy` クエリ設定に基づいた結果をどのようにグループ化できるかを定義します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-321">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="4f1fa-322">どの `groupBy` 値も定義しない場合、`productid` 別に合計が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-322">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="4f1fa-323">それ以外の場合は、`groupBy` を `groupBy=ColorId&groupBy=SizeId` として定義すると、システム内の異なる色とサイズの組み合わせに基づいて複数の明細行が返されます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-323">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="4f1fa-324">要求本文にクエリの基準を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-324">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="4f1fa-325">色とサイズを組み合わせた製品のサンプル クエリです。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-325">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a><span data-ttu-id="4f1fa-326">カスタム測定</span><span class="sxs-lookup"><span data-stu-id="4f1fa-326">Custom measurement</span></span>

<span data-ttu-id="4f1fa-327">既定の測定数量は Supply Chain Management にリンクされています。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-327">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="4f1fa-328">ただし、既定の測定値の組み合わせにより構成される数量が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-328">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="4f1fa-329">そのためには、カスタム数量を構成し、手持在庫クエリの出力に追加します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-329">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="4f1fa-330">この機能により、追加または削除される一連の測定を定義して、カスタム測定を作成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-330">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="4f1fa-331">たとえば、次のクエリ条件では、消費システムが使用できるように `MyCustomAvailableforReservation` としてカスタム測定数量を構成します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-331">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="4f1fa-332">消費システム</span><span class="sxs-lookup"><span data-stu-id="4f1fa-332">Consumption system</span></span> | <span data-ttu-id="4f1fa-333">計算済測定</span><span class="sxs-lookup"><span data-stu-id="4f1fa-333">Calculated measurers</span></span> | <span data-ttu-id="4f1fa-334">データ ソース</span><span class="sxs-lookup"><span data-stu-id="4f1fa-334">Data source</span></span> | <span data-ttu-id="4f1fa-335">モディファイアー</span><span class="sxs-lookup"><span data-stu-id="4f1fa-335">Modifier</span></span> | <span data-ttu-id="4f1fa-336">モディファイアーの計算タイプ</span><span class="sxs-lookup"><span data-stu-id="4f1fa-336">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="4f1fa-337">追加</span><span class="sxs-lookup"><span data-stu-id="4f1fa-337">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="4f1fa-338">追加</span><span class="sxs-lookup"><span data-stu-id="4f1fa-338">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="4f1fa-339">減算</span><span class="sxs-lookup"><span data-stu-id="4f1fa-339">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="4f1fa-340">追加</span><span class="sxs-lookup"><span data-stu-id="4f1fa-340">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="4f1fa-341">減算</span><span class="sxs-lookup"><span data-stu-id="4f1fa-341">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="4f1fa-342">追加</span><span class="sxs-lookup"><span data-stu-id="4f1fa-342">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="4f1fa-343">追加</span><span class="sxs-lookup"><span data-stu-id="4f1fa-343">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="4f1fa-344">減算</span><span class="sxs-lookup"><span data-stu-id="4f1fa-344">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="4f1fa-345">減算</span><span class="sxs-lookup"><span data-stu-id="4f1fa-345">Subtraction</span></span> |

<span data-ttu-id="4f1fa-346">これを使用すると、カスタム測定数量に対するクエリが次の出力を返します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-346">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="4f1fa-347">`MyCustomAvailableforReservation` 出力は、次のようにカスタム測定の計算設定に基づいています。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-347">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="4f1fa-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="4f1fa-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="4f1fa-349">手持在庫変更の転記</span><span class="sxs-lookup"><span data-stu-id="4f1fa-349">Posting on-hand changes</span></span>

<span data-ttu-id="4f1fa-350">イベントが転記される正確な URL は、地理的領域によって異なります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-350">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="4f1fa-351">フォームを使用します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-351">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="4f1fa-352">認証されると、この URL を HTTP `POST` メソッドと一緒に使用し、手持在庫変更のイベントをサービスに送信することができます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-352">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="4f1fa-353">特別なヘッダーは、HTTP 要求を通じた Dynamics 365 サービスとの通信に使用され、データがリンクされている Supply Chain Management インスタンスの環境 ID を表しています。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-353">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="4f1fa-354">例:</span><span class="sxs-lookup"><span data-stu-id="4f1fa-354">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="4f1fa-355">手持在庫変更クエリの転記に関する例 1</span><span class="sxs-lookup"><span data-stu-id="4f1fa-355">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="4f1fa-356">この例では、Power Apps で分析コードの構成を設定するシナリオを紹介します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-356">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="4f1fa-357">次のクエリを使用して、Power Apps で分析コードのマッピングを構成します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-357">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="4f1fa-358">これで、クエリにある `dimensionDataSource` を指定してカスタム分析コード使用できます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-358">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="4f1fa-359">システムが、カスタム分析コードをベース分析コードに自動的に変換します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-359">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="4f1fa-360">手持在庫変更クエリの転記に関する例 2</span><span class="sxs-lookup"><span data-stu-id="4f1fa-360">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="4f1fa-361">この例では、Power Apps で分析コードの構成に必要なマッピングが設定されていないシナリオを示します。この場合、転記する場合もベース分析コードを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-361">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="4f1fa-362">`dimensionDataSource` フィールドが null 値、空白、または空白の場合は、すべての分析コードがベース分析コードである必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-362">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="4f1fa-363">JSON ドキュメント フィールド プロパティ</span><span class="sxs-lookup"><span data-stu-id="4f1fa-363">JSON document field properties</span></span>

<span data-ttu-id="4f1fa-364">以前に例として説明した JSON クエリのフィールドには、次のテーブルに表示されているプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-364">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="4f1fa-365">フィールド ID</span><span class="sxs-lookup"><span data-stu-id="4f1fa-365">Field ID</span></span> | <span data-ttu-id="4f1fa-366">説明</span><span class="sxs-lookup"><span data-stu-id="4f1fa-366">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="4f1fa-367">特定の変更イベントの固有 ID。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-367">A unique ID for the specific change event.</span></span> <span data-ttu-id="4f1fa-368">この ID を使用してサービスとの通信が転記時に失敗した場合にイベントを再送信しても、同じイベントがシステムで 2 回カウントされることはありません。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-368">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="4f1fa-369">イベントにリンクされている組織の ID。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-369">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="4f1fa-370">これは、Supply Chain Management 組織またはデータ領域 ID にマップされます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-370">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="4f1fa-371">問題の製品 ID。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-371">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="4f1fa-372">手持在庫を変更する必要のある数量。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-372">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="4f1fa-373">たとえば、新たにベーグルを棚に 10 個載せると、この値は 10 になります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-373">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="4f1fa-374">その後、ベーグルを 3 つ棚から取るか売れた場合、この値は 3 になります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-374">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="4f1fa-375">イベントやクエリ変更の転記で使用する分析コードのデータ ソース。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-375">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="4f1fa-376">データ ソースを指定する場合は、指定されたデータ ソースのカスタム分析コードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-376">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="4f1fa-377">分析コードの構成を使用して、Inventory Visibility はカスタム分析コードを既定の標準分析コードにマップできます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-377">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="4f1fa-378">`dimensionDataSource` が指定されていない場合は、クエリで既定の標準分析コードのみを使用できます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-378">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="4f1fa-379">キーと値のペアの動的なバッグ。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-379">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="4f1fa-380">これらは、Supply Chain Management の一部の分析コードにマップされますが、イベントを Supply Chain Management または外部システムから取得した場合に表示されることがあるカスタム分析コード (*ソース* など) を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-380">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="4f1fa-381">現在の手持在庫に対するクエリの実行</span><span class="sxs-lookup"><span data-stu-id="4f1fa-381">Querying current on-hand</span></span>

<span data-ttu-id="4f1fa-382">現在の手持在庫に対してクエリを実行するためのエンドポイントは、次のような URL です。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-382">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="4f1fa-383">HTTP `POST` メソッドでクエリが実行されます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-383">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="4f1fa-384">現在の手持在庫に対するクエリ例 1</span><span class="sxs-lookup"><span data-stu-id="4f1fa-384">Current on-hand query example 1</span></span>

<span data-ttu-id="4f1fa-385">この例では、Power Apps で分析コードの構成がすでに完了しているシナリオを紹介します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-385">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="4f1fa-386">次のクエリを使用して、Power Apps で分析コードのマッピングを構成します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-386">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="4f1fa-387">これで、クエリにある `dimensionDataSource` を指定してカスタム分析コード使用できます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-387">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="4f1fa-388">システムが、カスタム分析コードをベース分析コードに自動的に変換します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-388">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="4f1fa-389">`filters` で `DimensionDataSource` を指定し、`filters` および `groupByValues` の両方でカスタム分析コードを指定できます。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-389">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="4f1fa-390">システムが、カスタム分析コードをベース分析コードに自動的に変換します。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-390">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="4f1fa-391">現在の手持在庫に対するクエリ例 2</span><span class="sxs-lookup"><span data-stu-id="4f1fa-391">Current on-hand query example 2</span></span>

<span data-ttu-id="4f1fa-392">この例では、Power Apps で分析コードの構成に必要なマッピングが設定されていないシナリオを示します。この場合、転記する場合もベース分析コードを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-392">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="4f1fa-393">`filters` にある `dimensionDataSource` フィールドが null 値、空白、または空白の場合は、すべての分析コードがベース分析コードである必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-393">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="4f1fa-394">例: 返された結果</span><span class="sxs-lookup"><span data-stu-id="4f1fa-394">Example return result</span></span>

<span data-ttu-id="4f1fa-395">前の例のクエリを実行すると、次のような結果が返される場合があります。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-395">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="4f1fa-396">"数量" フィールドは、測定とそれに関連付けられた値のディクショナリとして構成されています。</span><span class="sxs-lookup"><span data-stu-id="4f1fa-396">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
