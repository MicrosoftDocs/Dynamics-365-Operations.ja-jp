---
title: グローバル在庫会計の使用を開始する
description: このトピックでは、グローバル在庫会計の使用を開始する方法について説明します。
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 59f9db309312bbbc88b4fa47c12c4c02f09e7c6d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301701"
---
# <a name="get-started-with-global-inventory-accounting"></a><span data-ttu-id="e4ab1-103">グローバル在庫会計の使用を開始する</span><span class="sxs-lookup"><span data-stu-id="e4ab1-103">Get started with Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="e4ab1-104">グローバル在庫会計を利用することで、設定したグローバル在庫会計元帳の中で複数の在庫会計を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-104">Global Inventory Accounting lets you do multiple inventory accountings in the Global Inventory Accounting ledgers that you've set up.</span></span> <span data-ttu-id="e4ab1-105">各グローバル在庫会計元帳を *規則* に関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-105">You must associate each Global Inventory Accounting ledger with a *convention*.</span></span> <span data-ttu-id="e4ab1-106">規則とは、次のタイプの会計ポリシーの集合です。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-106">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="e4ab1-107">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="e4ab1-107">Cost object</span></span>
- <span data-ttu-id="e4ab1-108">入力測定基準</span><span class="sxs-lookup"><span data-stu-id="e4ab1-108">Input measurement basis</span></span>
- <span data-ttu-id="e4ab1-109">原価フロー仮定</span><span class="sxs-lookup"><span data-stu-id="e4ab1-109">Cost flow assumption</span></span>
- <span data-ttu-id="e4ab1-110">原価要素</span><span class="sxs-lookup"><span data-stu-id="e4ab1-110">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="e4ab1-111">グローバル在庫会計を有効にした後でも、通常の方法で Microsoft Dynamics 365 Supply Chain Management で在庫会計を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-111">Even after you turn on Global Inventory Accounting, you can still do inventory accounting in Microsoft Dynamics 365 Supply Chain Management in the usual way.</span></span>

<span data-ttu-id="e4ab1-112">グローバル在庫会計はアドインです。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-112">Global Inventory Accounting is an add-in.</span></span> <span data-ttu-id="e4ab1-113">この機能を使用できるようにするには、Microsoft Dynamics Lifecycle Services (LCS) からインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-113">To make its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="e4ab1-114">本番環境で有効にする前に、テスト環境で評価することを選択できます。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-114">You can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="e4ab1-115">グローバル在庫会計は、Supply Chain Management に組み込まれているすべての原価管理機能に対応していません。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-115">Global Inventory Accounting doesn't currently support all the cost management features that are built into Supply Chain Management.</span></span> <span data-ttu-id="e4ab1-116">したがって、現在使用可能な一連の機能が要件を満たすかどうかを評価することが重要となります。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-116">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a><span data-ttu-id="e4ab1-117">グローバル在庫会計のパブリック プレビューの取得方法</span><span class="sxs-lookup"><span data-stu-id="e4ab1-117">How to get the Global Inventory Accounting public preview</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e4ab1-118">グローバル在庫会計を使用するには、LCS が有効になっている高可用性環境 (OneBox 環境ではない) が必要です。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-118">To use Global Inventory Accounting, you must have an LCS-enabled high-availability environment (not a OneBox environment).</span></span> <span data-ttu-id="e4ab1-119">また、Supply Chain Management バージョン 10.0.19 以降を実行している必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-119">Additionally, you must be running Supply Chain Management version 10.0.19 or later.</span></span>

<span data-ttu-id="e4ab1-120">グローバル在庫会計パブリック プレビューにサインアップするには、[グローバル在庫会計チーム](mailto:GlobalInventoryAccounting@service.microsoft.com)に電子メールで LCS 環境 ID を送信します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-120">To sign up for the Global Inventory Accounting public preview, send your LCS environment ID by email to the [Global Inventory Accounting team](mailto:GlobalInventoryAccounting@service.microsoft.com).</span></span> <span data-ttu-id="e4ab1-121">プログラムに承認された後、チームはグローバル在庫会計ベータ キーおよびサービス エンドポイントを含むフォローアップ電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-121">After you're approved for the program, the team will send you a follow-up email that contains a Global Inventory Accounting beta key and your service endpoints.</span></span> <span data-ttu-id="e4ab1-122">ベータ キーを受信した後に、[アドインをインストール](#install)できます。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-122">After you receive the beta key, you can [install the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="e4ab1-123">ライセンス</span><span class="sxs-lookup"><span data-stu-id="e4ab1-123">Licensing</span></span>

<span data-ttu-id="e4ab1-124">グローバル在庫会計は、Supply Chain Management に使用できる棚卸し会計の標準機能と共にライセンス供与されます。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-124">Global Inventory Accounting is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="e4ab1-125">グローバル在庫会計を使用するのに、追加のライセンスを購入する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-125">You don't have to purchase an additional license to use Global Inventory Accounting.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e4ab1-126">必要条件</span><span class="sxs-lookup"><span data-stu-id="e4ab1-126">Prerequisites</span></span>

### <a name="set-up-microsoft-power-platform-integration"></a><span data-ttu-id="e4ab1-127">Microsoft Power Platform 統合の設定</span><span class="sxs-lookup"><span data-stu-id="e4ab1-127">Set up Microsoft Power Platform integration</span></span>

<span data-ttu-id="e4ab1-128">アドイン機能を有効にする前に、次の手順に従って Microsoft Power Platform と統合する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-128">Before you can enable add-in functionality, you must integrate with Microsoft Power Platform by following these steps.</span></span>

1. <span data-ttu-id="e4ab1-129">サービスを追加する LCS 環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-129">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="e4ab1-130">**完全な詳細** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="e4ab1-131">**Power Platform の統合** セクションで、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-131">In the **Power Platform Integration** section, select **Setup**.</span></span>
1. <span data-ttu-id="e4ab1-132">**Power Platform環境の設定** ダイアログ ボックスでチェック ボックスをオンにし、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-132">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="e4ab1-133">通常、設定には 60分 から 90分かかります。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-133">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="e4ab1-134">Microsoft Power Platform 環境の設定が完了すると、環境の名前がページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-134">After setup of the Microsoft Power Platform environment is completed, the page shows the name of your environment.</span></span> <span data-ttu-id="e4ab1-135">また、**Power Platform 統合セクション** に、「Power Platform 環境の設定が完了しました」と表示されます。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-135">Additionally, the **Power Platform Integration** section shows the statement, "Power Platform environment setup is complete."</span></span> <span data-ttu-id="e4ab1-136">グローバル在庫会計に、二重書き込みアプリケーションは必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-136">Global Inventory Accounting doesn't require a dual-write application.</span></span>

<span data-ttu-id="e4ab1-137">詳細については、[環境配置後の設定](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-137">For more information, see [Set up after environment deployment](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span></span>

### <a name="set-up-dataverse"></a><span data-ttu-id="e4ab1-138">Dataverse の設定</span><span class="sxs-lookup"><span data-stu-id="e4ab1-138">Set up Dataverse</span></span>

<span data-ttu-id="e4ab1-139">Dataverse を設定する前に、次の手順に従って、グローバル在庫会計サービス プリンシプルをテナントに追加します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-139">Before you set up Dataverse, add the Global Inventory Accounting service principles to your tenant by following these steps.</span></span>

1. <span data-ttu-id="e4ab1-140">[Graph 用 Azure Active Directory PowerShell をインストールする](/powershell/azure/active-directory/install-adv2)に記載の手順に従って Windows PowerShell v2 用 Azure AD モジュールをインストールします。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-140">Install Azure AD Module for Windows PowerShell v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
1. <span data-ttu-id="e4ab1-141">次の PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-141">Run the following PowerShell command.</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

<span data-ttu-id="e4ab1-142">次に、次の手順に従って、Dataverse でグローバル在庫会計用のアプリケーション ユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-142">Next, create application users for Global Inventory Accounting in Dataverse by following these steps.</span></span>

1. <span data-ttu-id="e4ab1-143">Dataverse 環境の URLを開きます。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-143">Open the URL of your Dataverse environment.</span></span>
1. <span data-ttu-id="e4ab1-144">**詳細設定 \> システム \> セキュリティ \> ユーザー** の順に移動し、アプリケーション ユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-144">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="e4ab1-145">**表示** フィールドを使用して、ページ ビューを *アプリケーション ユーザー* に変更します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-145">Use the **View** field to change the page view to *Application users*.</span></span>
1. <span data-ttu-id="e4ab1-146">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-146">Select **New**.</span></span>
1. <span data-ttu-id="e4ab1-147">**アプリケーション ID** を *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9* に設定します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-147">Set the **Application ID** field to *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span></span>
1. <span data-ttu-id="e4ab1-148">**ロールの割り当て** を選択してから、*システム管理者* を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-148">Select **Assign Role**, and then select *System Administrator*.</span></span> <span data-ttu-id="e4ab1-149">*Common Data Service ユーザー* という名前のロールがある場合は、それも選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-149">If there is a role that is named *Common Data Service User*, select it too.</span></span>
1. <span data-ttu-id="e4ab1-150">上記の手順を繰り返しますが、**アプリケーション ID** フィールドは *5f58fc56-0202-49a8-ac9e-0946b049718b* に設定します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-150">Repeat the preceding steps, but set the **Application ID** field to *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span></span>

<span data-ttu-id="e4ab1-151">詳細については、「[アプリケーション ユーザーの作成](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-151">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

<span data-ttu-id="e4ab1-152">Dataverse インストールの既定の言語が英語ではない場合、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-152">If the default language of your Dataverse installation isn't English, follow these steps.</span></span>

1. <span data-ttu-id="e4ab1-153">**詳細設定 \> 管理 \> 言語** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-153">Go to **Advanced Setting \> Administration \> Languages**.</span></span>
1. <span data-ttu-id="e4ab1-154">*英語* (*LanguageCode=1033*) を選択し、**適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-154">Select *English* (*LanguageCode=1033*), and then select **Apply**.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="e4ab1-155">アドインのインストール</span><span class="sxs-lookup"><span data-stu-id="e4ab1-155">Install the add-in</span></span>

<span data-ttu-id="e4ab1-156">グローバル在庫会計を使用できるようにするには、以下の手順に従ってアドインをインストールします。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-156">Follow these steps to install the add-in so that you can use Global Inventory Accounting.</span></span>

1. <span data-ttu-id="e4ab1-157">グローバル在庫会計のパブリック プレビューへの[サインアップ](#sign-up)。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-157">[Sign up](#sign-up) for the Global Inventory Accounting public preview.</span></span>
1. <span data-ttu-id="e4ab1-158">[LCS](https://lcs.dynamics.com/Logon/Index) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-158">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="e4ab1-159">**プレビュー機能管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-159">Go to **Preview feature management**.</span></span>
1. <span data-ttu-id="e4ab1-160">プラス記号 (**+**) を選択してください。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-160">Select the plus sign (**+**).</span></span>
1. <span data-ttu-id="e4ab1-161">**コード** フィールドに、グローバル在庫会計用のアドイン ベータ キーを入力します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-161">In the **Code** field, enter your add-in beta key for Global Inventory Accounting.</span></span> <span data-ttu-id="e4ab1-162">(サインアップ時に電子メールでベータ キーを受け取っている必要があります。)</span><span class="sxs-lookup"><span data-stu-id="e4ab1-162">(You should have received your beta key by email when you signed up.)</span></span>
1. <span data-ttu-id="e4ab1-163">**ブロック解除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-163">Select **Unblock**.</span></span>
1. <span data-ttu-id="e4ab1-164">サービスを追加する LCS 環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-164">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="e4ab1-165">**完全な詳細** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-165">Go to **Full details**.</span></span>
1. <span data-ttu-id="e4ab1-166">**Power Platform 統合** に移動し、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-166">Go to **Power Platform Integration**, and select **Setup**.</span></span>
1. <span data-ttu-id="e4ab1-167">**Power Platform環境の設定** ダイアログ ボックスでチェック ボックスをオンにし、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-167">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="e4ab1-168">通常、設定には 60分 から 90分かかります。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-168">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="e4ab1-169">Microsoft Power Platform 環境の設定が完了した後、**環境アドイン** クイックタブで、**新しいアドインをインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-169">After setup of the Microsoft Power Platform environment is completed, on the **Environment add-ins** FastTab, select **Install a new add-in**.</span></span>
1. <span data-ttu-id="e4ab1-170">**グローバル在庫会計** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-170">Select **Global inventory accounting**.</span></span>
1. <span data-ttu-id="e4ab1-171">インストール ガイドに従って、契約条件に同意します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-171">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="e4ab1-172">**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-172">Select **Install**.</span></span>
1. <span data-ttu-id="e4ab1-173">**環境アドイン** クイックタブで、グローバル在庫会計がインストール中であることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-173">On the **Environment add-ins** FastTab, you should see that Global Inventory Accounting is being installed.</span></span> <span data-ttu-id="e4ab1-174">数分後、状態が *インストール中* から *インストール済* に変わります。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-174">After a few minutes, the status should change from *Installing* to *Installed*.</span></span> <span data-ttu-id="e4ab1-175">(この変更を表示するには、ページを更新する必要がある場合があります。) その時点で、グローバル在庫会計を使用する準備が整っています。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-175">(You might have to refresh the page to see this change.) At that point, Global Inventory Accounting is ready to use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="e4ab1-176">統合を設定する</span><span class="sxs-lookup"><span data-stu-id="e4ab1-176">Set up the integration</span></span>

<span data-ttu-id="e4ab1-177">以下の手順に従って、グローバル在庫会計と Supply Chain Management の統合を設定します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-177">Follow these steps to set up the integration between Global Inventory Accounting and Supply Chain Management.</span></span>

1. <span data-ttu-id="e4ab1-178">Supply Chain Management にサインインします。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-178">Sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="e4ab1-179">**システム管理 \> 機能管理** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-179">Go to **System administration \> Feature Management**.</span></span>
1. <span data-ttu-id="e4ab1-180">**更新プログラムの確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-180">Select **Check for updates**.</span></span>
1. <span data-ttu-id="e4ab1-181">**すべて** タブで、*グローバル在庫会計* という名前の機能を検索します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-181">On the **All** tab, search for the feature that is named *Global inventory accounting*.</span></span>
1. <span data-ttu-id="e4ab1-182">**直ちに有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-182">Select **Enable now**.</span></span>
1. <span data-ttu-id="e4ab1-183">**グローバル在庫会計 \> 設定 \> グローバル在庫会計パラメーター \> 統合パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-183">Go to **Global inventory accounting \> Setup \> Global inventory accounting parameters \> Integrations parameters**.</span></span>
1. <span data-ttu-id="e4ab1-184">**データ サービス エンドポイント** および **グローバル在庫会計エンドポイント** フィールドに、プレビューへのサインアップ時にグローバル在庫会計チームが送信した電子メールの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-184">In the **Data service endpoint** and **Global inventory accounting endpoint** fields, enter the URLs from the email that the Global Inventory Accounting team sent when you signed up for the preview.</span></span>

<span data-ttu-id="e4ab1-185">グローバル在庫会計を使用する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="e4ab1-185">Global Inventory Accounting is now ready to use.</span></span>
