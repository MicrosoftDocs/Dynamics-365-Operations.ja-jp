---
title: 税計算アドインの使用を開始する
description: このトピックでは、税計算アドインを設定する方法について説明します。
author: wangchen
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 835ae33fba31d4bccb218969aa9aa61eaa7a3061
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832596"
---
# <a name="get-started-with-the-tax-calculation-add-in-preview"></a><span data-ttu-id="48168-103">税計算アドインの使用を開始する (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="48168-103">Get started with the tax calculation add-in (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="48168-104">このトピックでは、税計算アドインの使用を開始する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="48168-104">This topic provides information about how to get started with the tax calculation add-in.</span></span> <span data-ttu-id="48168-105">まず、 Microsoft Dynamics Lifecycle Services (LCS)、Regulatory Configuration Service (RCS)、および Dynamics 365 Finance および Dynamics 365 Supply Chain Management の構成手順について説明し ます。</span><span class="sxs-lookup"><span data-stu-id="48168-105">It first guides you through the configuration steps in Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS), and Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="48168-106">次に、Finance および Supply Chain Management トランザクションで税計算アドインを使用する一般的なプロセスをレビューします。</span><span class="sxs-lookup"><span data-stu-id="48168-106">It then reviews the common process for using the tax calculation add-in in Finance and Supply Chain Management transactions.</span></span>

<span data-ttu-id="48168-107">この設定は、次の 4 つの主要なステップで構成されています。</span><span class="sxs-lookup"><span data-stu-id="48168-107">The setup consists of four main steps:</span></span>

1. <span data-ttu-id="48168-108">LCS で、税計算アドインをインストールします。</span><span class="sxs-lookup"><span data-stu-id="48168-108">In LCS, install the tax calculation add-in.</span></span>
2. <span data-ttu-id="48168-109">RCS で、税計算機能を設定します。</span><span class="sxs-lookup"><span data-stu-id="48168-109">In RCS, set up the tax calculation feature.</span></span> <span data-ttu-id="48168-110">この設定は、法人ごとに固有のものではありません。</span><span class="sxs-lookup"><span data-stu-id="48168-110">This setup isn't specific to a legal entity.</span></span> <span data-ttu-id="48168-111">Finance および Supply Chain Management の法人間で共有できます。</span><span class="sxs-lookup"><span data-stu-id="48168-111">It can be shared across legal entities in Finance and Supply Chain Management.</span></span>
3. <span data-ttu-id="48168-112">Finance および Supply Chain Management で、法人別に税計算アドイン パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="48168-112">In Finance and Supply Chain Management, set up the tax calculation add-in parameters by legal entity.</span></span>
4. <span data-ttu-id="48168-113">Finance および Supply Chain Management で、販売注文などのトランザクションを作成し、税計算アドインを使用して税を決定および計算します。</span><span class="sxs-lookup"><span data-stu-id="48168-113">In Finance and Supply Chain Management, create transactions such as sales orders, and use the tax calculation add-in to determine and calculate taxes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="48168-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="48168-114">Prerequisites</span></span>

<span data-ttu-id="48168-115">このトピックの手順を完了する前に、以下の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="48168-115">Before you can complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="48168-116">LCS アカウントにアクセスし、Dynamics 365 バージョン 10.0.18 以降を実行する第 2 層 (またはそれ以上) の環境を持つ LCS プロジェクトをデプロイしました。</span><span class="sxs-lookup"><span data-stu-id="48168-116">You have access to your LCS account, and you've deployed an LCS project with a Tier 2 (or above) environment that runs Dynamics 365 version 10.0.18 or later.</span></span>
- <span data-ttu-id="48168-117">RCS アカウントへのアクセス権があります。</span><span class="sxs-lookup"><span data-stu-id="48168-117">You have access to your RCS account.</span></span>
- <span data-ttu-id="48168-118">Microsoftに連絡し、デプロイされている Finance or Supply Chain Management 環境でフライティングを有効にしました。</span><span class="sxs-lookup"><span data-stu-id="48168-118">You've contacted Microsoft to enable the flighting in your deployed Finance or Supply Chain Management environment.</span></span>

## <a name="set-up-the-tax-calculation-add-in-in-lcs"></a><span data-ttu-id="48168-119">LCS で税計算アドインを設定する</span><span class="sxs-lookup"><span data-stu-id="48168-119">Set up the tax calculation add-in in LCS</span></span>

1. <span data-ttu-id="48168-120">[LCS](https://lcs.dynamics.com)にサインインします。</span><span class="sxs-lookup"><span data-stu-id="48168-120">Sign in to [LCS](https://lcs.dynamics.com)</span></span>
2. <span data-ttu-id="48168-121">Microsoft Power Platform 統合の設定を完了します。</span><span class="sxs-lookup"><span data-stu-id="48168-121">Complete the setup for Microsoft Power Platform integration.</span></span> <span data-ttu-id="48168-122">詳細については、[アドインの概要](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48168-122">For more information, see [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
3. <span data-ttu-id="48168-123">デプロイされている非運用環境のいずれかを選択し、**新しいアドインのインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-123">Select one of your deployed non-production environments, and then select **Install a new add-in**.</span></span>
4. <span data-ttu-id="48168-124">**税計算サービス (プレビュー)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-124">Select **Tax calculation (preview)**.</span></span>
5. <span data-ttu-id="48168-125">契約条件を読んで合意し、**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-125">Read and agree to the terms and conditions, and then select **Install**.</span></span>

## <a name="set-up-the-tax-calculation-add-in-in-rcs"></a><span data-ttu-id="48168-126">RCS で税計算アドインを設定する</span><span class="sxs-lookup"><span data-stu-id="48168-126">Set up the tax calculation add-in in RCS</span></span>

<span data-ttu-id="48168-127">このセクションの手順は、特定の法人に関連しています。</span><span class="sxs-lookup"><span data-stu-id="48168-127">The steps in this section aren't related to a specific legal entity.</span></span> <span data-ttu-id="48168-128">この手順を実行する必要があるのは 1 回だけであり、RCS のどの法人でもこれを実行できます。</span><span class="sxs-lookup"><span data-stu-id="48168-128">You must complete this procedure only one time, and you can complete it in any legal entity in RCS.</span></span>

1. <span data-ttu-id="48168-129">[RCS](https://marketing.configure.global.dynamics.com/) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="48168-129">Sign in to [RCS](https://marketing.configure.global.dynamics.com/).</span></span>
2. <span data-ttu-id="48168-130">Finance の **電子申告** ワークスペースで、新しいコンフィギュレーション プロバイダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="48168-130">In Finance, in the **Electronic reporting** workspace, add a new configuration provider.</span></span> <span data-ttu-id="48168-131">会社名をプロバイダーの名前として使用します。</span><span class="sxs-lookup"><span data-stu-id="48168-131">Use your company name as the name of the provider.</span></span> <span data-ttu-id="48168-132">詳細については、[構成プロバイダーを作成して、有効としてマークする](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48168-132">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="48168-133">作成したコンフィギュレーション プロバイダーを選択し、**有効に設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-133">Select the configuration provider that you just created, and then select **Set active**.</span></span>
4. <span data-ttu-id="48168-134">**Microsoft** コンフィギュレーション プロバイダーを選択し、**リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-134">Select the **Microsoft** configuration provider, and then select **Repositories**.</span></span>
5. <span data-ttu-id="48168-135">**タイプ** フィールドで、**グローバル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-135">In the **Type** field, select **Global**.</span></span>
6. <span data-ttu-id="48168-136">**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-136">Select **Open**.</span></span>
7. <span data-ttu-id="48168-137">**税データ モデル** に移動し、ファイル ツリーを展開して、 **税コンフィギュレーション - ヨーロッパ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-137">Go to **Tax Data Model**, expand the file tree, and then select **Tax Configuration - Europe**.</span></span>
8. <span data-ttu-id="48168-138">最新バージョンを選択して、**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-138">Select the latest version, and then select **Import**.</span></span>
9. <span data-ttu-id="48168-139">**グローバリゼーション機能 (プレビュー)** ワークスペースに戻り、**機能** を選択し、**税計算** ウィンドウを選択して、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-139">Return to the **Globalization features (Preview)** workspace, select **Features**, select the **Tax calculation** tile, and then select **Add**.</span></span>
10. <span data-ttu-id="48168-140">次のいずれかの機能タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-140">Select one of the following feature types:</span></span>

    - <span data-ttu-id="48168-141">**新機能** - 空のコンテンツを含む機能の設定を作成します。</span><span class="sxs-lookup"><span data-stu-id="48168-141">**New feature** – Create a feature setup that has blank content.</span></span>
    - <span data-ttu-id="48168-142">**既存の機能に基づく** - 既存の機能から機能を作成し、既存の機能設定からコンテンツをコピーします。</span><span class="sxs-lookup"><span data-stu-id="48168-142">**Based on existing feature** – Create a feature from an existing feature, and copy the content from the existing feature setup.</span></span>

11. <span data-ttu-id="48168-143">機能の名前と説明を入力して、**機能の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-143">Enter a name and description for the feature, and then select **Create feature**.</span></span>

    <span data-ttu-id="48168-144">機能作成後に、ドラフト バージョンが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="48168-144">After the feature is created, a draft version of it is automatically created.</span></span>

12. <span data-ttu-id="48168-145">機能のドラフト バージョンを選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-145">Select the draft version of the feature, and then select **Edit**.</span></span> <span data-ttu-id="48168-146">**税計算の設定** ページのフィールドが自動入力されます。</span><span class="sxs-lookup"><span data-stu-id="48168-146">The **Tax calculation setup** page is filled in.</span></span>
13. <span data-ttu-id="48168-147">**コンフィギュレーション バージョン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-147">Select **Configuration version**.</span></span> <span data-ttu-id="48168-148">手順 8 でインポートしたコンフィギュレーション バージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="48168-148">You should see the configuration version that you imported in step 8.</span></span>

    <span data-ttu-id="48168-149">Microsoft は、税計算アドインの既定の税コンフィギュレーションを提供します。</span><span class="sxs-lookup"><span data-stu-id="48168-149">Microsoft provides a default tax configuration for the tax calculation add-in.</span></span> <span data-ttu-id="48168-150">このコンフィギュレーションでは、税計算動作に関する要件のほとんどがカバーされます。</span><span class="sxs-lookup"><span data-stu-id="48168-150">This configuration covers most of the requirements for tax calculation behaviors.</span></span> <span data-ttu-id="48168-151">これは、市場フィードバックに基づいて更新されます。</span><span class="sxs-lookup"><span data-stu-id="48168-151">It will be updated based on market feedbacks.</span></span> <span data-ttu-id="48168-152">特定の要件を満たすためにコンフィギュレーションを拡張する必要がある場合、独自の税コンフィギュレーションを生成および選択する方法の詳細については、[税務サービスの拡張機能を構築する方法 ](https://go.microsoft.com/fwlink/?linkid=2138483)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48168-152">If you must extend the configuration to meet specific requirements, see [How to build extension in tax service](https://go.microsoft.com/fwlink/?linkid=2138483) for information about how to generate and select your own tax configuration.</span></span>

    <span data-ttu-id="48168-153">**コンフィギュレーション バージョン** を選択すると、いくつかのタブが表示されます。</span><span class="sxs-lookup"><span data-stu-id="48168-153">After you select **Configuration version**, several additional tabs appear:</span></span>

    - <span data-ttu-id="48168-154">**税コード** - 税計算サービスで、このタブは必須です。</span><span class="sxs-lookup"><span data-stu-id="48168-154">**Tax codes** – This tab is mandatory for the tax calculation service.</span></span> <span data-ttu-id="48168-155">税コードのマスター データを管理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="48168-155">It's used to maintain master data for tax codes.</span></span> <span data-ttu-id="48168-156">法人で現在のバージョンの税機能設定を有効にした場合、このタブで作成された税コードはすべて Finance に自動的に同期されます。</span><span class="sxs-lookup"><span data-stu-id="48168-156">All tax codes that are created on this tab are automatically synced to Finance when you enable the current version of the tax feature setup in the legal entity.</span></span>
    - <span data-ttu-id="48168-157">**税コード適用性** - 税計算アドインに対してこのタブは必須です。</span><span class="sxs-lookup"><span data-stu-id="48168-157">**Tax codes applicability** – This tab is mandatory for the tax calculation add-in.</span></span> <span data-ttu-id="48168-158">税コード、税グループ、および品目別税グループを決定するマトリックスを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="48168-158">It's used to define a matrix that determines the tax code, tax group, and item tax group.</span></span> <span data-ttu-id="48168-159">決定された税コードは、税額の計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="48168-159">The tax code that is determined is used to calculate the tax amount.</span></span> <span data-ttu-id="48168-160">**税コード**、**税グループ**、および **品目別税グループ** の各フィールドの値が Finance に返されます。</span><span class="sxs-lookup"><span data-stu-id="48168-160">The values of the **Tax code**, **Tax group**, and **Item tax group** fields are returned to Finance.</span></span>
    - <span data-ttu-id="48168-161">**顧客税登録番号の適用性** - 税計算アドインに対してこのタブはオプションです。</span><span class="sxs-lookup"><span data-stu-id="48168-161">**Customer tax registration number applicability** – This tab is optional for the tax calculation add-in.</span></span> <span data-ttu-id="48168-162">1 件の顧客に複数の税登録番号がある場合は、税計算アドインによって正しい税登録番号を自動的に決定できます。</span><span class="sxs-lookup"><span data-stu-id="48168-162">If you have multiple tax registration numbers for one customer, the tax calculation add-in can automatically determine the correct tax registration number.</span></span> <span data-ttu-id="48168-163">このタブのマトリックスでは、アドインが決定を行うのに使用するルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="48168-163">In the matrix on this tab, you define the rules that the add-in uses to make the determination.</span></span> <span data-ttu-id="48168-164">このオプションを選択しない場合、Finance および Supply Chain Management は引き続き、販売トランザクションの課税対象ドキュメントに既定の税登録番号を使用します。</span><span class="sxs-lookup"><span data-stu-id="48168-164">Otherwise, Finance and Supply Chain Management will continue to use the default tax registration number on taxable documents for sales transactions.</span></span>
    - <span data-ttu-id="48168-165">**仕入先税登録番号の適用性** - 税計算アドインに対してこのタブはオプションです。</span><span class="sxs-lookup"><span data-stu-id="48168-165">**Vendor tax registration number applicability** – This tab is optional for the tax calculation add-in.</span></span> <span data-ttu-id="48168-166">1 件の仕入先に複数の税登録番号がある場合は、税計算アドインによって正しい税登録番号を自動的に決定できます。</span><span class="sxs-lookup"><span data-stu-id="48168-166">If you have multiple tax registration numbers for one vendor, the tax calculation add-in can automatically determine the correct tax registration number.</span></span> <span data-ttu-id="48168-167">このタブのマトリックスでは、アドインが決定を行うのに使用するルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="48168-167">In the matrix on this tab, you define the rules that the add-in uses to make the determination.</span></span> <span data-ttu-id="48168-168">このオプションを選択しない場合、Finance および Supply Chain Management は引き続き、購入トランザクションの課税対象ドキュメントに既定の税登録番号を使用します。</span><span class="sxs-lookup"><span data-stu-id="48168-168">Otherwise, Finance and Supply Chain Management will continue to use the default tax registration number on taxable documents for purchase transactions.</span></span>
    - <span data-ttu-id="48168-169">**リスト コード適用性** - 税計算アドインに対してこのタブはオプションです。</span><span class="sxs-lookup"><span data-stu-id="48168-169">**List code applicability** – This tab is optional for the tax calculation add-in.</span></span> <span data-ttu-id="48168-170">より柔軟で構成可能なルールによって、**リスト コード** フィールドの値が自動的に特定されるのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="48168-170">It can help automatically determine the value of the **List code** field through more flexible and configurable rules.</span></span> <span data-ttu-id="48168-171">このタブのマトリックスでは、アドインが決定を行うのに使用するルールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="48168-171">In the matrix on this tab, you can define the rules that the add-in uses to make the determination.</span></span> <span data-ttu-id="48168-172">このオプションを選択しない場合、Finance および Supply Chain Management は引き続き、課税対象ドキュメントに既定のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="48168-172">Otherwise, Finance and Supply Chain Management will continue to use the default code on taxable documents.</span></span>

14. <span data-ttu-id="48168-173">**税コード** タブで、**追加** を選択し、税コードと説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="48168-173">On the **Tax codes** tab, select **Add**, and enter the tax code and a description.</span></span>
15. <span data-ttu-id="48168-174">**税コンポーネント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-174">Select **Tax component**.</span></span> <span data-ttu-id="48168-175">税コンポーネントは、選択された税コンフィギュレーションの以前のバージョンで定義された一連の税計算方法です。</span><span class="sxs-lookup"><span data-stu-id="48168-175">The tax component is a group of tax calculation methods that was defined in the previous version of the selected tax configuration.</span></span> <span data-ttu-id="48168-176">次の税コンポーネントを使用できます。</span><span class="sxs-lookup"><span data-stu-id="48168-176">The following tax components are available:</span></span>

    - <span data-ttu-id="48168-177">正味金額別</span><span class="sxs-lookup"><span data-stu-id="48168-177">By net amount</span></span>
    - <span data-ttu-id="48168-178">総額別</span><span class="sxs-lookup"><span data-stu-id="48168-178">By gross amount</span></span>
    - <span data-ttu-id="48168-179">数量別</span><span class="sxs-lookup"><span data-stu-id="48168-179">By quantity</span></span>
    - <span data-ttu-id="48168-180">利益幅別</span><span class="sxs-lookup"><span data-stu-id="48168-180">By margin</span></span>
    - <span data-ttu-id="48168-181">税の税</span><span class="sxs-lookup"><span data-stu-id="48168-181">Tax on tax</span></span>

16. <span data-ttu-id="48168-182">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-182">Select **Save**.</span></span> <span data-ttu-id="48168-183">選択した税コンポーネントに基づいて、使用可能なフィールドが増加します。</span><span class="sxs-lookup"><span data-stu-id="48168-183">More fields become available, based on the tax component that you selected.</span></span>
17. <span data-ttu-id="48168-184">次のオプションを使用して、税コードの性質を識別します。</span><span class="sxs-lookup"><span data-stu-id="48168-184">Use the following options to identify the nature of the tax code:</span></span>

    - <span data-ttu-id="48168-185">免税対象である</span><span class="sxs-lookup"><span data-stu-id="48168-185">Is Exempt</span></span>
    - <span data-ttu-id="48168-186">利用税である</span><span class="sxs-lookup"><span data-stu-id="48168-186">Is Use tax</span></span>
    - <span data-ttu-id="48168-187">逆請求である</span><span class="sxs-lookup"><span data-stu-id="48168-187">Is Reverse Charge</span></span>
    - <span data-ttu-id="48168-188">基準額計算から除外</span><span class="sxs-lookup"><span data-stu-id="48168-188">Exclude in Base Amount Calculation</span></span>

    <span data-ttu-id="48168-189">利用税のシナリオでは、正の税率を持つ単一の税コードを設定し、**利用税である** とマークします。</span><span class="sxs-lookup"><span data-stu-id="48168-189">For a use tax scenario, set up a single tax code that has a positive tax rate, and mark it as **Is Use tax**.</span></span>

    <span data-ttu-id="48168-190">逆請求のシナリオでは、2 つの税コードを設定します。税コードの 1 つは正の税率で、もう一方の税コードには負の税率が設定されますが、税率は同じです。</span><span class="sxs-lookup"><span data-stu-id="48168-190">For a reverse charge scenario, set up two tax codes, one of which has a positive tax rate, and the other of which has a negative tax rate but the same rate value.</span></span> <span data-ttu-id="48168-191">負の税コードを **逆請求である** してマークします。</span><span class="sxs-lookup"><span data-stu-id="48168-191">Mark the negative tax code as **Is reverse charge**.</span></span> <span data-ttu-id="48168-192">Finance の逆請求ソリューションの詳細については 、[VAT/GST スキームの逆請求メカニズム](emea-reverse-charge.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48168-192">For more information about the reverse charge solution in Finance, see [Reverse charge mechanism for VAT/GST scheme](emea-reverse-charge.md).</span></span>
    
    <span data-ttu-id="48168-193">価格内税トランザクションの税基準額計算で除外する必要がある一部の税タイプ (一部の国の関税など) については、**基準額計算で除外** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="48168-193">For some tax types which should be excluded in the tax base amount calculation for price inclusive transactions, like custom duty in some countries, select the **Exclude in Base Amount Calculation** check box.</span></span>

    <span data-ttu-id="48168-194">この税コードの税率と税額の上限を管理します。</span><span class="sxs-lookup"><span data-stu-id="48168-194">Maintain tax rates and the tax amount limits for this tax code.</span></span>

18. <span data-ttu-id="48168-195">手順 14 ～ 17 を繰り返して、必要なすべての税コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="48168-195">Repeat steps 14 through 17 to add all other tax codes that are required.</span></span>
19. <span data-ttu-id="48168-196">**税コードの適用性** タブで、正しい税コードを決定するために必要な列を選択し、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-196">On the **Tax codes applicability** tab, select the columns that are required to determine the correct tax code, and then select **Add**.</span></span>
20. <span data-ttu-id="48168-197">各列の値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-197">Enter or select values for each column.</span></span> <span data-ttu-id="48168-198">**税コード**、**税グループ**、および **品目別税グループ** の各フィールドは、マトリックスの出力となります。</span><span class="sxs-lookup"><span data-stu-id="48168-198">The **Tax code**, **Tax group**, and **Item tax group** fields will be the output of this matrix.</span></span>
21. <span data-ttu-id="48168-199">手順 19～20 を繰り返して、顧客税登録番号、仕入先税登録番号、およびリスト コードの適用方法を設定します。</span><span class="sxs-lookup"><span data-stu-id="48168-199">Repeat steps 19 through 20 to set up the applicability of customer tax registration numbers, vendor tax registration numbers, and list codes.</span></span>
22. <span data-ttu-id="48168-200">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="48168-200">Select **Save**, and then close the page.</span></span>
23. <span data-ttu-id="48168-201">**ステータスの変更** \> **完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-201">Select **Change status** \> **Complete**.</span></span> <span data-ttu-id="48168-202">ステータスが **完了** に変更された後は、バージョンを編集できなくなります。</span><span class="sxs-lookup"><span data-stu-id="48168-202">After the status is changed to **Complete**, the version can no longer be edited.</span></span>
24. <span data-ttu-id="48168-203">**状態の変更** \> **公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-203">Select **Change status** \> **Publish**.</span></span> <span data-ttu-id="48168-204">このバージョンの税機能の設定は、グローバル リポジトリにプッシュされ、Finance の各法人に表示されます。</span><span class="sxs-lookup"><span data-stu-id="48168-204">This version of the tax feature setup will be pushed to the global repository and will be visible to each legal entity in Finance.</span></span>

## <a name="dynamics-365-setup"></a><span data-ttu-id="48168-205">Dynamics 365 の設定</span><span class="sxs-lookup"><span data-stu-id="48168-205">Dynamics 365 setup</span></span>

<span data-ttu-id="48168-206">前のセクションで説明したように、RCS の設定が完了すると、税機能の公開済みバージョンが完成します。</span><span class="sxs-lookup"><span data-stu-id="48168-206">After you complete the setup in RCS, as described in the previous section, you will have a published version of the tax feature.</span></span> <span data-ttu-id="48168-207">Finance で税計算アドインを設定する手順に従います。</span><span class="sxs-lookup"><span data-stu-id="48168-207">Follow these steps to set up the tax calculation add-in in Finance.</span></span>

<span data-ttu-id="48168-208">このセクションの設定は法人が行います。</span><span class="sxs-lookup"><span data-stu-id="48168-208">The setup in this section is done by legal entity.</span></span> <span data-ttu-id="48168-209">Finance で税計算アドインを有効にした法人ごとに、この機能を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48168-209">You must configure it for each legal entity that you want to enable the tax calculation add-in for in Finance.</span></span>

1. <span data-ttu-id="48168-210">Finance では、**税** \> **設定**\>**税コンフィギュレーション**\>**の税計算アドインの設定 (プレビュー)** に移動します。</span><span class="sxs-lookup"><span data-stu-id="48168-210">In Finance, go to **Tax** \> **Setup** \> **Tax configuration** \> **Tax calcluation add-in setup (Preview)**.</span></span>
2. <span data-ttu-id="48168-211">**一般** タブで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="48168-211">On the **General** tab, set the following fields:</span></span>

    - <span data-ttu-id="48168-212">**税計算アドインの有効化** - 法人に対して税計算アドインを有効にするには 、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="48168-212">**Enable tax calculation add-in** – Select this check box to enable the tax calculation add-in for the legal entity.</span></span> <span data-ttu-id="48168-213">現在の法人に対して税計算アドインが有効になっていない場合、法人は引き続き既存の税エンジンを使用して税金を決定および計算します。</span><span class="sxs-lookup"><span data-stu-id="48168-213">If the tax calculation add-in isn't enabled for the current legal entity, the legal entity will continue to use the existing tax engine to determine and calculate tax.</span></span>
    - <span data-ttu-id="48168-214">**機能の設定** - 法人用に対して公開済みの税機能の設定とバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-214">**Feature setup** – Select a published tax feature setup and version for the legal entity.</span></span> <span data-ttu-id="48168-215">公開された税機能の設定方法と完了方法の詳細については、このトピックの前のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="48168-215">For more information about how to set up and complete a published tax feature, see the previous section of this topic.</span></span>
    - <span data-ttu-id="48168-216">**業務プロセス** - 税計算アドインで有効にする業務プロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="48168-216">**Business Process** – Select the business processes to enable for the tax calculation add-in.</span></span>
    - <span data-ttu-id="48168-217">**税コード調整の有効化** - 売上税ページで税コード調整を有効にするには、このオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="48168-217">**Enable tax code adjustment** – Set this option to **Yes** to enable tax code adjustments on the sales tax page.</span></span>

3. <span data-ttu-id="48168-218">**計算** タブで、法人に対して予想される丸めルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="48168-218">On the **Calculation** tab, define the expected rounding rule for the legal entity.</span></span>
4. <span data-ttu-id="48168-219">**エラー処理** タブ で、法人に対して予想されるエラー処理方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="48168-219">On the **Error handling** tab, define the expected error handling method for the legal entity.</span></span> <span data-ttu-id="48168-220">税計算アドインの結果コードごとに 3 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="48168-220">Three options are available for each result code from the tax calculation add-in:</span></span>

    - <span data-ttu-id="48168-221">なし</span><span class="sxs-lookup"><span data-stu-id="48168-221">No</span></span>
    - <span data-ttu-id="48168-222">警告</span><span class="sxs-lookup"><span data-stu-id="48168-222">Warning</span></span>
    - <span data-ttu-id="48168-223">エラー</span><span class="sxs-lookup"><span data-stu-id="48168-223">Error</span></span>

5. <span data-ttu-id="48168-224">税計算アドイン設定を保存します。</span><span class="sxs-lookup"><span data-stu-id="48168-224">Save the tax calculation add-in setup.</span></span>
6. <span data-ttu-id="48168-225">追加の法人ごとに手順 1 から 5 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="48168-225">Repeat steps 1 through 5 for each additional legal entity.</span></span>

## <a name="transaction-processing"></a><span data-ttu-id="48168-226">トランザクションの処理</span><span class="sxs-lookup"><span data-stu-id="48168-226">Transaction processing</span></span>

<span data-ttu-id="48168-227">すべての設定手順が完了したら、税計算アドインを使用して Finance の税金を決定および計算できます。</span><span class="sxs-lookup"><span data-stu-id="48168-227">After you've completed all the setup procedures, you can use the tax calculation add-in to determine and calculate tax in Finance.</span></span> <span data-ttu-id="48168-228">トランザクションを処理する手順は変わりません。</span><span class="sxs-lookup"><span data-stu-id="48168-228">The steps to process transactions remain the same.</span></span> <span data-ttu-id="48168-229">Finance バージョン 10.0.18 でサポートされるトランザクションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="48168-229">The following transactions are supported in Finance version 10.0.18:</span></span>

- <span data-ttu-id="48168-230">販売プロセス</span><span class="sxs-lookup"><span data-stu-id="48168-230">Sales process</span></span>

    - <span data-ttu-id="48168-231">販売見積</span><span class="sxs-lookup"><span data-stu-id="48168-231">Sales quotation</span></span>
    - <span data-ttu-id="48168-232">販売注文</span><span class="sxs-lookup"><span data-stu-id="48168-232">Sales order</span></span>
    - <span data-ttu-id="48168-233">確認書</span><span class="sxs-lookup"><span data-stu-id="48168-233">Confirmation</span></span>
    - <span data-ttu-id="48168-234">ピッキング リスト</span><span class="sxs-lookup"><span data-stu-id="48168-234">Picking list</span></span>
    - <span data-ttu-id="48168-235">梱包明細</span><span class="sxs-lookup"><span data-stu-id="48168-235">Packing slip</span></span>
    - <span data-ttu-id="48168-236">売上請求書</span><span class="sxs-lookup"><span data-stu-id="48168-236">Sales invoice</span></span>
    - <span data-ttu-id="48168-237">訂正票</span><span class="sxs-lookup"><span data-stu-id="48168-237">Credit note</span></span>
    - <span data-ttu-id="48168-238">返品注文</span><span class="sxs-lookup"><span data-stu-id="48168-238">Return order</span></span>
    - <span data-ttu-id="48168-239">ヘッダー請求金額</span><span class="sxs-lookup"><span data-stu-id="48168-239">Header charge</span></span>
    - <span data-ttu-id="48168-240">明細行請求金額</span><span class="sxs-lookup"><span data-stu-id="48168-240">Line charge</span></span>

- <span data-ttu-id="48168-241">購入プロセス</span><span class="sxs-lookup"><span data-stu-id="48168-241">Purchase process</span></span>

    - <span data-ttu-id="48168-242">発注書</span><span class="sxs-lookup"><span data-stu-id="48168-242">Purchase order</span></span>
    - <span data-ttu-id="48168-243">確認書</span><span class="sxs-lookup"><span data-stu-id="48168-243">Confirmation</span></span>
    - <span data-ttu-id="48168-244">入庫リスト</span><span class="sxs-lookup"><span data-stu-id="48168-244">Receipts list</span></span>
    - <span data-ttu-id="48168-245">製品受領書</span><span class="sxs-lookup"><span data-stu-id="48168-245">Product receipt</span></span>
    - <span data-ttu-id="48168-246">仕入請求書</span><span class="sxs-lookup"><span data-stu-id="48168-246">Purchase invoice</span></span>
    - <span data-ttu-id="48168-247">ヘッダー請求金額</span><span class="sxs-lookup"><span data-stu-id="48168-247">Header charge</span></span>
    - <span data-ttu-id="48168-248">明細行請求金額</span><span class="sxs-lookup"><span data-stu-id="48168-248">Line charge</span></span>
    - <span data-ttu-id="48168-249">訂正票</span><span class="sxs-lookup"><span data-stu-id="48168-249">Credit note</span></span>
    - <span data-ttu-id="48168-250">返品注文</span><span class="sxs-lookup"><span data-stu-id="48168-250">Return order</span></span>
    - <span data-ttu-id="48168-251">購買要求</span><span class="sxs-lookup"><span data-stu-id="48168-251">Purchase requisition</span></span>
    - <span data-ttu-id="48168-252">購買要求明細行の請求金額</span><span class="sxs-lookup"><span data-stu-id="48168-252">Purchase requisition line charge</span></span>
    - <span data-ttu-id="48168-253">見積依頼</span><span class="sxs-lookup"><span data-stu-id="48168-253">Request for quotation</span></span>
    - <span data-ttu-id="48168-254">見積依頼ヘッダーの請求金額</span><span class="sxs-lookup"><span data-stu-id="48168-254">Request for quotation header charge</span></span>
    - <span data-ttu-id="48168-255">見積依頼行の請求金額</span><span class="sxs-lookup"><span data-stu-id="48168-255">Request for quotation line charge</span></span>

- <span data-ttu-id="48168-256">在庫プロセス</span><span class="sxs-lookup"><span data-stu-id="48168-256">Inventory process</span></span>

    - <span data-ttu-id="48168-257">移動オーダー - 出荷</span><span class="sxs-lookup"><span data-stu-id="48168-257">Transfer order – ship</span></span>
    - <span data-ttu-id="48168-258">移動オーダー - 入庫</span><span class="sxs-lookup"><span data-stu-id="48168-258">Transfer order - receive</span></span>
