---
title: エンジニアリングの変更管理機能のチュートリアル
description: このトピックでは、エンジニアリング変更管理の使用方法を示す、エンド ツー エンドのチュートリアルを示します。
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 56e868f3050432db8d3b1721da435665f554d90d
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487924"
---
# <a name="engineering-change-management-feature-walkthrough"></a><span data-ttu-id="59756-103">エンジニアリングの変更管理機能のチュートリアル</span><span class="sxs-lookup"><span data-stu-id="59756-103">Engineering change management feature walkthrough</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59756-104">このトピックでは、エンジニアリング変更管理の使用方法を示す、エンド ツー エンドのチュートリアルを示します。</span><span class="sxs-lookup"><span data-stu-id="59756-104">This topic provides an end-to-end walkthrough that shows how to work with engineering change management.</span></span> <span data-ttu-id="59756-105">最も重要なシナリオは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="59756-105">It goes through each of the most important scenarios:</span></span>

- <span data-ttu-id="59756-106">基本機能の構成</span><span class="sxs-lookup"><span data-stu-id="59756-106">Basic feature configuration</span></span>
- <span data-ttu-id="59756-107">エンジニアリング会社が新しいエンジニアリング製品を作成する方法</span><span class="sxs-lookup"><span data-stu-id="59756-107">How an engineering company creates a new engineering product</span></span>
- <span data-ttu-id="59756-108">エンジニアリング会社が社内の会社に対してエンジニアリング製品をリリースする方法</span><span class="sxs-lookup"><span data-stu-id="59756-108">How an engineering company releases an engineering product to a local company</span></span>
- <span data-ttu-id="59756-109">地域の会社がエンジニアリング会社からリリースされた製品を確認および承認する方法</span><span class="sxs-lookup"><span data-stu-id="59756-109">How a local company can review and accept a product that has been released to it by an engineering company</span></span>
- <span data-ttu-id="59756-110">ローカル会社が標準トランザクションでエンジニアリング製品を使用する方法</span><span class="sxs-lookup"><span data-stu-id="59756-110">How a local company can use an engineering product in standard transactions</span></span>
- <span data-ttu-id="59756-111">販売注文にエンジニアリング製品を追加する方法</span><span class="sxs-lookup"><span data-stu-id="59756-111">How to add an engineering product to a sales order</span></span>
- <span data-ttu-id="59756-112">エンジニアリング変更要求を作成してエンジニアリング製品に変更を依頼する方法</span><span class="sxs-lookup"><span data-stu-id="59756-112">How to request changes to an engineering product by creating an engineering change request</span></span>
- <span data-ttu-id="59756-113">エンジニアリング変更オーダーを作成して、要求された変更をスケジュールし実装する方法</span><span class="sxs-lookup"><span data-stu-id="59756-113">How to schedule and implement requested changes by creating an engineering change order</span></span>
- <span data-ttu-id="59756-114">変更された製品のリリース方法</span><span class="sxs-lookup"><span data-stu-id="59756-114">How to release a product that has been changed</span></span>

<span data-ttu-id="59756-115">このトピックのすべての演習では、Microsoft Dynamics 365 Supply Chain Management に用意されている標準的なサンプルデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="59756-115">All the exercises in this topic use the standard sample data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="59756-116">また、各手順は前の手順に基づいて構築されています。</span><span class="sxs-lookup"><span data-stu-id="59756-116">Additionally, each exercise builds on the previous exercise.</span></span> <span data-ttu-id="59756-117">したがって、特にエンジニアリング変更管理機能を使用したことがない場合は、最初から最後までのこの演習をおこなうことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="59756-117">Therefore, we recommend that you work through the exercises in order, from beginning to end, especially if you've never used the engineering change management feature before.</span></span> <span data-ttu-id="59756-118">これにより、この機能を完全に理解することができます。</span><span class="sxs-lookup"><span data-stu-id="59756-118">In this way, you will gain a complete understanding of the feature.</span></span>

## <a name="set-up-for-the-sample-scenario"></a><span data-ttu-id="59756-119">このサンプル シナリオに設定する</span><span class="sxs-lookup"><span data-stu-id="59756-119">Set up for the sample scenario</span></span>

<span data-ttu-id="59756-120">このトピックで説明されているサンプル シナリオに従うには、最初にデモ データを使用できるようにし、いくつかのカスタム レコードを追加して、機能を準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59756-120">To follow the sample scenario that is provided in this topic, you must first prepare the feature by making demo data available and adding a few custom records.</span></span>

<span data-ttu-id="59756-121">このトピックの残りの部分で演習を行う前に、次のすべてのサブセクションの手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="59756-121">Before you try to do any of the exercises in the rest of this topic, follow the instructions in all the following subsections.</span></span> <span data-ttu-id="59756-122">また、これらのサブサイトでは、自分の組織のエンジニアリング変更管理を設定する際に使用するいくつかの重要な設定ページも紹介します。</span><span class="sxs-lookup"><span data-stu-id="59756-122">These subsections also introduce several important settings pages that you will use when you set up engineering change management for your own organization.</span></span>

### <a name="make-standard-demo-data-available"></a><span data-ttu-id="59756-123">標準デモ データを有効化する</span><span class="sxs-lookup"><span data-stu-id="59756-123">Make standard demo data available</span></span>

<span data-ttu-id="59756-124">[標準のデモ データがインストールされている](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) システムで作業します。</span><span class="sxs-lookup"><span data-stu-id="59756-124">Work on a system where the [standard demo data is installed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span></span> <span data-ttu-id="59756-125">標準のデモ データによって、複数のデモ法人 (会社および組織) のデータが追加されます。</span><span class="sxs-lookup"><span data-stu-id="59756-125">The standard demo data adds data for several demo legal entities (companies and organizations).</span></span> <span data-ttu-id="59756-126">この演習では、右側にある会社の選択を使用して、*エンジニアリング組織* として設定されている1つの会社 (*DEMF*) *運営組織* として設定されている別の会社 (*USMF*) を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="59756-126">As you work through the exercises, you will use the company picker on the right side of the navigation bar to switch between one company (*DEMF*) that is set up as an *engineering organization* and another company (*USMF*) that is set up as an *operational organization*.</span></span>

### <a name="set-up-an-engineering-organization"></a><span data-ttu-id="59756-127">エンジニアリング組織の設定</span><span class="sxs-lookup"><span data-stu-id="59756-127">Set up an engineering organization</span></span>

<span data-ttu-id="59756-128">エンジニアリング組織はエンジニアリング データを所有し、製品デザインと製品の変更を担当します。</span><span class="sxs-lookup"><span data-stu-id="59756-128">An engineering organization owns the engineering data, and is responsible for product design and product changes.</span></span> <span data-ttu-id="59756-129">エンジニアリング組織を設定するには、以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="59756-129">To set up your engineering organizations, follow these steps.</span></span>

1. <span data-ttu-id="59756-130">**エンジニアリング変更管理 &gt; 設定 &gt; エンジニアリング組織** に移動します。</span><span class="sxs-lookup"><span data-stu-id="59756-130">Go to **Engineering change management &gt; Setup &gt; Engineering organizations**.</span></span>
1. <span data-ttu-id="59756-131">**新規** を選択して、グリッドに行を追加して、それに次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-131">Select **New** to add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="59756-132">**エンジニアリング組織:** *DEMF*</span><span class="sxs-lookup"><span data-stu-id="59756-132">**Engineering organization:** *DEMF*</span></span>
    - <span data-ttu-id="59756-133">**組織名:** *Contoso Entertainment System Germany*</span><span class="sxs-lookup"><span data-stu-id="59756-133">**Organization name:** *Contoso Entertainment System Germany*</span></span>

    <span data-ttu-id="59756-134">![エンジニアリング組織の追加](media/engineering-org.png "エンジニアリング組織の追加")</span><span class="sxs-lookup"><span data-stu-id="59756-134">![Adding an engineering organization](media/engineering-org.png "Adding an engineering organization")</span></span>

### <a name="set-up-the-version-product-dimension-group"></a><span data-ttu-id="59756-135">バージョンの製品分析コード グループの設定</span><span class="sxs-lookup"><span data-stu-id="59756-135">Set up the version product dimension group</span></span>

1. <span data-ttu-id="59756-136">**製品情報管理 &gt; 設定 &gt; 分析コードとバリアント グループ &gt; 製品分析コード グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="59756-136">Go to **Product information management &gt; Setup &gt; Dimensions and variant groups &gt; Product dimension groups**.</span></span>
1. <span data-ttu-id="59756-137">**新規** を選択して、製品分析コードグループを作成します。</span><span class="sxs-lookup"><span data-stu-id="59756-137">Select **New** to create a product dimension group.</span></span>
1. <span data-ttu-id="59756-138">**名前** フィールドを *バージョン* に設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-138">Set the **Name** field to *Version*.</span></span>
1. <span data-ttu-id="59756-139">**保存** を選択して、新しい分析コードを保存し、**製品分析コード** クイックタブに値を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="59756-139">Select **Save** to save the new dimension and load values onto the **Product dimensions** FastTab.</span></span>
1. <span data-ttu-id="59756-140">**製品分析コード** クイックタブで、有効な製品分析コードとして **バージョン** を設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-140">On the **Product dimensions** FastTab, set **Version** as an active product dimension.</span></span>

    <span data-ttu-id="59756-141">![製品分析コード グループの追加](media/product-dimension-groups.png "製品分析コード グループの追加")</span><span class="sxs-lookup"><span data-stu-id="59756-141">![Adding a product dimension group](media/product-dimension-groups.png "Adding a product dimension group")</span></span>

### <a name="set-up-product-lifecycle-states"></a><span data-ttu-id="59756-142">製品ライフサイクルの状態の設定</span><span class="sxs-lookup"><span data-stu-id="59756-142">Set up product lifecycle states</span></span>

<span data-ttu-id="59756-143">エンジニアリング製品はライフサイクルを通じて、ライフサイクル状態ごとに許可するトランザクションを制御できるようにすることが重要です。</span><span class="sxs-lookup"><span data-stu-id="59756-143">As an engineering product goes through its lifecycle, it's important that you be able to control which transactions are allowed for each lifecycle state.</span></span> <span data-ttu-id="59756-144">製品ライフサイクル状態を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="59756-144">To set up the product lifecycle states, follow these steps.</span></span>

1. <span data-ttu-id="59756-145">**エンジニアリング変更管理 &gt; 設定 &gt; 製造ライフサイクルの状態** に移動します。</span><span class="sxs-lookup"><span data-stu-id="59756-145">Go to **Engineering change management &gt; Setup &gt; Product lifecycle state**.</span></span>
1. <span data-ttu-id="59756-146">**新規** を選択して、ライフサイクルの状態を追加して、それに次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-146">Select **New** to add a lifecycle state, and set the following values for it:</span></span>

    - <span data-ttu-id="59756-147">**状態:** *操作*</span><span class="sxs-lookup"><span data-stu-id="59756-147">**State:** *Operational*</span></span>
    - <span data-ttu-id="59756-148">**説明:** *操作*</span><span class="sxs-lookup"><span data-stu-id="59756-148">**Description:** *Operational*</span></span>

1. <span data-ttu-id="59756-149">**保存** を選択して、新しいライフサイクルの状態を保存し、**有効化されたビジネス プロセス** クイックタブに値を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="59756-149">Select **Save** to save the new lifecycle state and load values onto the **Enabled business processes** FastTab.</span></span>
1. <span data-ttu-id="59756-150">**有効化されたビジネス プロセス** クイックタブで、使用できるビジネス プロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-150">On the **Enabled business processes** FastTab, select the business processes that should be available.</span></span> <span data-ttu-id="59756-151">この例では、すべてのビジネス プロセスに対して **ポリシー** フィールドを *有効化* にしておきます。</span><span class="sxs-lookup"><span data-stu-id="59756-151">For this example, leave the **Policy** field set to *Enabled* for all business processes.</span></span>

    <span data-ttu-id="59756-152">![ライフサイクルの状態のビジネス プロセスの有効化](media/product-lifecycle-states-1.png "ライフサイクルの状態のビジネス プロセスの有効化")</span><span class="sxs-lookup"><span data-stu-id="59756-152">![Enabling business processes for a lifecycle state](media/product-lifecycle-states-1.png "Enabling business processes for a lifecycle state")</span></span>

1. <span data-ttu-id="59756-153">**新規** を選択して、他のライフサイクルの状態を追加して、それに次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-153">Select **New** to add another lifecycle state, and set the following values for it:</span></span>

    - <span data-ttu-id="59756-154">**状態:** *プロトタイプ*</span><span class="sxs-lookup"><span data-stu-id="59756-154">**State:** *Prototype*</span></span>
    - <span data-ttu-id="59756-155">**説明:** *プロトタイプ*</span><span class="sxs-lookup"><span data-stu-id="59756-155">**Description:** *Prototype*</span></span>

1. <span data-ttu-id="59756-156">**保存** を選択して、新しいライフサイクルの状態を保存し、**有効化されたビジネス プロセス** クイックタブに値を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="59756-156">Select **Save** to save the new lifecycle state and load values onto the **Enabled business processes** FastTab.</span></span>
1. <span data-ttu-id="59756-157">**有効化されたビジネス プロセス** クイックタブで、使用できるビジネス プロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-157">On the **Enabled business processes** FastTab, select the business processes that should be available.</span></span> <span data-ttu-id="59756-158">この例では、すべてのビジネス プロセスに対して **ポリシー** フィールドを *警告付きで有効化* にしておきます。</span><span class="sxs-lookup"><span data-stu-id="59756-158">For this example, set the **Policy** field to *Enabled with warning* for all business processes.</span></span>

    <span data-ttu-id="59756-159">![ライフサイクルの状態のビジネス プロセスの有効化 (警告付き)](media/product-lifecycle-states-2.png "ライフサイクルの状態のビジネス プロセスの有効化 (警告付き)")</span><span class="sxs-lookup"><span data-stu-id="59756-159">![Enabling (with warnings) business processes for a lifecycle state](media/product-lifecycle-states-2.png "Enabling (with warnings) business processes for a lifecycle state")</span></span>

### <a name="set-up-a-version-number-rule"></a><span data-ttu-id="59756-160">バージョン番号ルールの設定</span><span class="sxs-lookup"><span data-stu-id="59756-160">Set up a version number rule</span></span>

1. <span data-ttu-id="59756-161">**エンジニアリング変更管理 &gt; 設定 &gt; 製品バージョン番号ルール** に移動します。</span><span class="sxs-lookup"><span data-stu-id="59756-161">Go to **Engineering change management &gt; Setup &gt; Product version number rule**.</span></span>
1. <span data-ttu-id="59756-162">**新規** を選択して、ルールを追加して、それに次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-162">Select **New** to add a rule, and set the following values for it:</span></span>

    - <span data-ttu-id="59756-163">**名前:** *自動*</span><span class="sxs-lookup"><span data-stu-id="59756-163">**Name:** *Auto*</span></span>
    - <span data-ttu-id="59756-164">**番号ルール:** *自動*</span><span class="sxs-lookup"><span data-stu-id="59756-164">**Number rule:** *Auto*</span></span>
    - <span data-ttu-id="59756-165">**フォーマット:** *V-\#\#*</span><span class="sxs-lookup"><span data-stu-id="59756-165">**Format:** *V-\#\#*</span></span>

    <span data-ttu-id="59756-166">![製品バージョン番号ルールの追加](media/version-number-rule.png "製品バージョン番号ルールの追加")</span><span class="sxs-lookup"><span data-stu-id="59756-166">![Adding a product version number rule](media/version-number-rule.png "Adding a product version number rule")</span></span>

### <a name="set-up-a-product-release-policy"></a><span data-ttu-id="59756-167">製品リリース ポリシーの設定</span><span class="sxs-lookup"><span data-stu-id="59756-167">Set up a product release policy</span></span>

1. <span data-ttu-id="59756-168">**エンジニアリング変更管理 &gt; 設定 &gt; 製品リリースポリシー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="59756-168">Go to **Engineering change management &gt; Setup &gt; Product release policies**.</span></span>
1. <span data-ttu-id="59756-169">**新規** を選択して、リリース ポリシーの状態を追加して、それに次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-169">Select **New** to add a release policy, and set the following values for it:</span></span>

    - <span data-ttu-id="59756-170">**名前:** *コンポーネント*</span><span class="sxs-lookup"><span data-stu-id="59756-170">**Name:** *Components*</span></span>
    - <span data-ttu-id="59756-171">**説明:** *コンポーネント*</span><span class="sxs-lookup"><span data-stu-id="59756-171">**Description:** *Components*</span></span>

1. <span data-ttu-id="59756-172">**一般** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-172">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="59756-173">**製品タイプ :** *品目*</span><span class="sxs-lookup"><span data-stu-id="59756-173">**Product type:** *Item*</span></span>
    - <span data-ttu-id="59756-174">**テンプレートの適用:** *常に*</span><span class="sxs-lookup"><span data-stu-id="59756-174">**Apply templates:** *Always*</span></span>
    - <span data-ttu-id="59756-175">**有効:** *はい*</span><span class="sxs-lookup"><span data-stu-id="59756-175">**Active:** *Yes*</span></span>

1. <span data-ttu-id="59756-176">**すべての製品** クイック タブで、**追加** を選択して明細行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-176">On the **All products** FastTab, select **Add** to add a line, and set the following values for it:</span></span>

    - <span data-ttu-id="59756-177">**企業:** *DEMF*</span><span class="sxs-lookup"><span data-stu-id="59756-177">**Company:** *DEMF*</span></span>
    - <span data-ttu-id="59756-178">**テンプレートリリース製品:** *D0006*</span><span class="sxs-lookup"><span data-stu-id="59756-178">**Template released product:** *D0006*</span></span>

1. <span data-ttu-id="59756-179">**追加** を選択して別の明細行を追加し、それに対して次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-179">Select **Add** to add another line, and set the following values for it:</span></span>

    - <span data-ttu-id="59756-180">**会社アカウント ID:** *USMF*</span><span class="sxs-lookup"><span data-stu-id="59756-180">**Company accounts ID:** *USMF*</span></span>
    - <span data-ttu-id="59756-181">**テンプレートリリース製品:** *D0006*</span><span class="sxs-lookup"><span data-stu-id="59756-181">**Template released product:** *D0006*</span></span>
    - <span data-ttu-id="59756-182">**BOM の受取:** このチェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-182">**Receive BOM:** Select this check box.</span></span>
    - <span data-ttu-id="59756-183">**BOM 承認のコピー:** このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="59756-183">**Copy BOM approval:** Select this check box.</span></span>
    - <span data-ttu-id="59756-184">**BOM 承認のコピー:** このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="59756-184">**Copy BOM activation:** Select this check box.</span></span>
    - <span data-ttu-id="59756-185">**ルートの受取:** このチェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-185">**Receive route:** Select this check box.</span></span>
    - <span data-ttu-id="59756-186">**ルート承認のコピー:** このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="59756-186">**Copy route approval:** Select this check box.</span></span>
    - <span data-ttu-id="59756-187">**ルートのアクティブ化のコピー:** このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="59756-187">**Copy route activation:** Select this check box.</span></span>

    <span data-ttu-id="59756-188">![製品リリース ポリシーの追加](media/product-release-policy.png "製品リリース ポリシーの追加")</span><span class="sxs-lookup"><span data-stu-id="59756-188">![Adding a product release policy](media/product-release-policy.png "Adding a product release policy")</span></span>

### <a name="set-up-an-engineering-product-category"></a><span data-ttu-id="59756-189">エンジニアリング製品カテゴリの設定</span><span class="sxs-lookup"><span data-stu-id="59756-189">Set up an engineering product category</span></span> 

<span data-ttu-id="59756-190">エンジニアリング製品カテゴリは、エンジニアリング製品 (技術変更管理によってバージョン指定されて制御される製品) を作成するための基礎となります。</span><span class="sxs-lookup"><span data-stu-id="59756-190">Engineering product categories provide the basis for creating engineering products (that is, products that are versioned and controlled through engineering change management).</span></span> <span data-ttu-id="59756-191">エンジニアリング製品カテゴリを設定するには、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="59756-191">To set up engineering product categories, follow these steps.</span></span>

1. <span data-ttu-id="59756-192">**エンジニアリング変更管理 &gt;エンジニアリング製品カテゴリの詳細** に移動します。</span><span class="sxs-lookup"><span data-stu-id="59756-192">Go to **Engineering change management &gt; Engineering product category details**.</span></span>
1. <span data-ttu-id="59756-193">**新規** を選択してカテゴリを作成します。</span><span class="sxs-lookup"><span data-stu-id="59756-193">Select **New** to create a category.</span></span>
1. <span data-ttu-id="59756-194">**詳細** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-194">On the **Details** FastTab, set the following values:</span></span>

    - <span data-ttu-id="59756-195">**名前:** *コンポーネント*</span><span class="sxs-lookup"><span data-stu-id="59756-195">**Name:** *Components*</span></span>
    - <span data-ttu-id="59756-196">**エンジニアリング組織:** *DEMF*</span><span class="sxs-lookup"><span data-stu-id="59756-196">**Engineering organization:** *DEMF*</span></span>
    - <span data-ttu-id="59756-197">**製品タイプ :** *品目*</span><span class="sxs-lookup"><span data-stu-id="59756-197">**Product type:** *Item*</span></span>
    - <span data-ttu-id="59756-198">**トランザクションのトラック バージョン:** *はい*</span><span class="sxs-lookup"><span data-stu-id="59756-198">**Track version in transactions:** *Yes*</span></span>
    - <span data-ttu-id="59756-199">**製品分析コード グループ:** *バージョン*</span><span class="sxs-lookup"><span data-stu-id="59756-199">**Product dimension group:** *Version*</span></span>
    - <span data-ttu-id="59756-200">**作成時の製品ライフサイクルの状態:** *操作可能*</span><span class="sxs-lookup"><span data-stu-id="59756-200">**Product lifecycle state at creation:** *Operational*</span></span>
    - <span data-ttu-id="59756-201">**バージョン番号ルール:** *自動*</span><span class="sxs-lookup"><span data-stu-id="59756-201">**Version number rule:** *Auto*</span></span>
    - <span data-ttu-id="59756-202">**効力を発揮する:** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="59756-202">**Enforce effectivity:** *No*</span></span>
    - <span data-ttu-id="59756-203">**番号ルール命名法を使用する:** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="59756-203">**Use number rule nomenclature:** *No*</span></span>
    - <span data-ttu-id="59756-204">**名前ルール命名法を使用する:** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="59756-204">**Use name rule nomenclature:** *No*</span></span>
    - <span data-ttu-id="59756-205">**番号ルール命名法を使用する:** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="59756-205">**Use description rule nomenclature:** *No*</span></span>

1. <span data-ttu-id="59756-206">**リリース ポリシー** クイックタブで、**製品リリースポリシー** フィールドを *コンポーネント* に設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-206">On the **Release policy** FastTab, set the **Product release policy** field to *Components*.</span></span>
1. <span data-ttu-id="59756-207">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-207">Select **Save**.</span></span>

    <span data-ttu-id="59756-208">![エンジニアリング製品カテゴリの追加](media/product-category-details.png "エンジニアリング製品カテゴリの追加")</span><span class="sxs-lookup"><span data-stu-id="59756-208">![Adding an engineering product category](media/product-category-details.png "Adding an engineering product category")</span></span>

### <a name="set-up-product-acceptance-conditions"></a><span data-ttu-id="59756-209">製品受け入れ条件の設定</span><span class="sxs-lookup"><span data-stu-id="59756-209">Set up product acceptance conditions</span></span>

1. <span data-ttu-id="59756-210">ナビゲーションバーの右側にある会社のピッカーを使用して、*USMF* 法人 (会社) に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="59756-210">Use the company picker on the right side of the navigation bar to switch to the *USMF* legal entity (company).</span></span>
1. <span data-ttu-id="59756-211">**エンジニアリング変更管理 &gt; 設定 &gt; エンジニアリング変更管理パラメータ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="59756-211">Go to **Engineering change management &gt; Setup &gt; Engineering change management parameters**.</span></span>
1. <span data-ttu-id="59756-212">**リリース管理** タブの **製品の受け入れ** セクションで、**製品の承認** フィールドを *手動* に設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-212">On the **Release control** tab, in the **Product acceptance** section, set the **Product acceptance** field to *Manual*.</span></span>

    <span data-ttu-id="59756-213">![製品受け入れ条件の設定](media/engineering-change-management-parameters.png "製品受け入れ条件の設定")</span><span class="sxs-lookup"><span data-stu-id="59756-213">![Setting up product acceptance conditions](media/engineering-change-management-parameters.png "Setting up product acceptance conditions")</span></span>

## <a name="create-a-new-engineering-product"></a><span data-ttu-id="59756-214">新しいエンジニアリング製品を作成する</span><span class="sxs-lookup"><span data-stu-id="59756-214">Create a new engineering product</span></span>

<span data-ttu-id="59756-215">エンジニアリング製品は、エンジニアリング変更管理を通じてバージョン管理と管理される製品です。</span><span class="sxs-lookup"><span data-stu-id="59756-215">An engineering product is a product that is versioned and controlled through engineering change management.</span></span> <span data-ttu-id="59756-216">つまり、変更はその期間中に制御でき、変更情報はエンジニアリング変更オーダーを使用して保存されます。</span><span class="sxs-lookup"><span data-stu-id="59756-216">In other words, you can control the changes during its life, and the change information will be saved using engineering change orders.</span></span> <span data-ttu-id="59756-217">エンジニアリング製品を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="59756-217">To create engineering products, follow these steps.</span></span>

1. <span data-ttu-id="59756-218">エンジニアリング組織の法人に所属していることを確認してください (この例の場合は *DEMF*)。</span><span class="sxs-lookup"><span data-stu-id="59756-218">Make sure that you're in the legal entity of your engineering organization (*DEMF* for this example).</span></span> <span data-ttu-id="59756-219">必要に応じて、ナビゲーションバーの右側にある会社ピッカーを使用します。</span><span class="sxs-lookup"><span data-stu-id="59756-219">Use the company picker on the right side of the navigation bar as required.</span></span>
1. <span data-ttu-id="59756-220">**リリース済製品** ページを、次の手順のいずれかを実行して開きます。</span><span class="sxs-lookup"><span data-stu-id="59756-220">Open the **Released products** page by following one of these steps:</span></span>

    - <span data-ttu-id="59756-221">**製品管理情報 &gt; 製品 &gt; リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="59756-221">Go to **Product information management &gt; Products &gt; Released products**.</span></span>
    - <span data-ttu-id="59756-222">**エンジニアリング変更管理 &gt; 共通 &gt; リリース済み製品** に移動します。</span><span class="sxs-lookup"><span data-stu-id="59756-222">Go to **Engineering change management &gt; Common &gt; Released products**.</span></span>

1. <span data-ttu-id="59756-223">アクション ペインで、**製品** タブの **新規** グループで、**エンジニアリング製品** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-223">On the Action Pane, on the **Product** tab, in the **New** group, select **Engineering product**.</span></span>
1. <span data-ttu-id="59756-224">**新しい製品** ダイアログ ボックスに次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-224">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="59756-225">**エンジニアリング製品カテゴリ:** *コンポーネント*</span><span class="sxs-lookup"><span data-stu-id="59756-225">**Engineering Product Category:** *Components*</span></span>
    - <span data-ttu-id="59756-226">**製品番号 :** *Z0001*</span><span class="sxs-lookup"><span data-stu-id="59756-226">**Product number:** *Z0001*</span></span>
    - <span data-ttu-id="59756-227">**製品名:** *スピーカー セット*</span><span class="sxs-lookup"><span data-stu-id="59756-227">**Product name:** *Speaker set*</span></span>

    <span data-ttu-id="59756-228">![エンジニアリング製品カテゴリの追加](media/new-product-dialog.png "エンジニアリング製品カテゴリの追加")</span><span class="sxs-lookup"><span data-stu-id="59756-228">![Adding an engineering product](media/new-product-dialog.png "Adding an engineering product")</span></span>

    <span data-ttu-id="59756-229">**バージョン** フィールドは、前に設定した製品バージョン番号のルールを使用して自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="59756-229">Note that the **Version** field is automatically set by using the product version number rule that you set up earlier.</span></span>

1. <span data-ttu-id="59756-230">**OK** を選択して製品を作成し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="59756-230">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="59756-231">新しい製品の詳細ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="59756-231">The details page for the new product is opened.</span></span> <span data-ttu-id="59756-232">**保管分析コードグループ**、**追跡用分析コードグループ**、**品目モデルグループ** など、一部のフィールドでは、値が既に入力されていますので注意してください。</span><span class="sxs-lookup"><span data-stu-id="59756-232">Notice that values are already filled in for some fields, such as **Storage dimension group**, **Tracking dimension group**, and/or **Item model group**.</span></span> <span data-ttu-id="59756-233">これらのフィールドは、製品が *DEMF*  法人でリリースされており、*コンポーネント* エンジニアリング製品カテゴリに関連付けられている *コンポーネント* 製品関連ポリシーを使用しています。</span><span class="sxs-lookup"><span data-stu-id="59756-233">These fields were automatically set because the product is being released in the *DEMF* legal entity and uses the *Components* product release policy, which is associated with the *Components* engineering product category.</span></span> <span data-ttu-id="59756-234">以前に、品目 *D0006* をテンプレートとして使用して *DEMF* 法人の行を設定しているため、入力された値が品目 *D0006* から取得されました。</span><span class="sxs-lookup"><span data-stu-id="59756-234">Because you previously used item *D0006* as a template to set up a line for the *DEMF* legal entity, the values that were filled in were taken from item *D0006*.</span></span>

    <span data-ttu-id="59756-235">![リリース済製品の詳細](media/product-details.png "リリース済製品の詳細")</span><span class="sxs-lookup"><span data-stu-id="59756-235">![Released product details](media/product-details.png "Released product details")</span></span>

1. <span data-ttu-id="59756-236">アクション ペインの **エンジニア** タブの **エンジニアリング変更管理** グループで、製品のバージョンを表示する **エンジニアリング バージョン** を選択して、製品のバージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="59756-236">On the Action Pane, on the **Engineer** tab, in the **Engineering change management** group, select **Engineering versions** to view the versions of the product.</span></span>

    <span data-ttu-id="59756-237">![エンジニアリング バージョン](media/engineering-versions-list.png "エンジニアリング バージョン")</span><span class="sxs-lookup"><span data-stu-id="59756-237">![Engineering versions](media/engineering-versions-list.png "Engineering versions")</span></span>

1. <span data-ttu-id="59756-238">**エンジニアリング バージョン** ページで、製品のバージョンは 1 つだけであり、有効になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="59756-238">On the **Engineering versions** page, notice that there is only one version for the product, and it's active.</span></span>
1. <span data-ttu-id="59756-239">バージョンを選択して、その詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="59756-239">Select the version to view its details.</span></span>

    <span data-ttu-id="59756-240">![エンジニアリング バージョンの詳細](media/engineering-version-details.png "エンジニアリング バージョンの詳細")</span><span class="sxs-lookup"><span data-stu-id="59756-240">![Engineering version details](media/engineering-version-details.png "Engineering version details")</span></span>

1. <span data-ttu-id="59756-241">**エンジニアリング バージョン** ページで、**部品表** クイックタブで、**BOM の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-241">On the **Engineering version** page, on the **Bill of material** FastTab, select **Create BOM**.</span></span>
1. <span data-ttu-id="59756-242">**BOM の作成** ダイアログ ボックスに次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-242">In the **Create BOM** dialog box, set the following values:</span></span>

    - <span data-ttu-id="59756-243">**BOM 番号:** Z0001</span><span class="sxs-lookup"><span data-stu-id="59756-243">**BOM number:** Z0001</span></span>
    - <span data-ttu-id="59756-244">**名前:** スピーカー セット</span><span class="sxs-lookup"><span data-stu-id="59756-244">**Name:** Speaker set</span></span>
    - <span data-ttu-id="59756-245">**サイト:** 1</span><span class="sxs-lookup"><span data-stu-id="59756-245">**Site:** 1</span></span>

    <span data-ttu-id="59756-246">![BOM の作成](media/create-bom.png "BOM の作成")</span><span class="sxs-lookup"><span data-stu-id="59756-246">![Creating a BOM](media/create-bom.png "Creating a BOM")</span></span>

1. <span data-ttu-id="59756-247">**OK** を選択して、BOM を作成し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="59756-247">Select **OK** to add the BOM and close the dialog box.</span></span>
1. <span data-ttu-id="59756-248">**部品表** クイックタブで、**部品表** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-248">On the **Bill of materials** FastTab, select **Bill of material**.</span></span>
1. <span data-ttu-id="59756-249">**部品表** ページの、**部品表明細行** クイックタブで、3 明細行、それぞれに対して *D0001*、*D0003*、*D0006* の品目番号を追加します。</span><span class="sxs-lookup"><span data-stu-id="59756-249">On the **Bill of materials** page, on the **Bill of materials lines** FastTab, add three lines, one each for item numbers *D0001*, *D0003*, and *D0006*.</span></span>

    <span data-ttu-id="59756-250">![BOM 明細行の追加](media/bom.png "BOM 明細行の追加")</span><span class="sxs-lookup"><span data-stu-id="59756-250">![Adding BOM lines](media/bom.png "Adding BOM lines")</span></span>

1. <span data-ttu-id="59756-251">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-251">Select **Save**.</span></span>
1. <span data-ttu-id="59756-252">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="59756-252">Close the page.</span></span>
1. <span data-ttu-id="59756-253">**エンジニアリング バージョン** ページで、**部品表** クイックタブで、**承認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-253">On the **Engineering version** page, on the **Bill of material** FastTab, select **Approve**.</span></span>
1. <span data-ttu-id="59756-254">表示されるダイアログ ボックスで、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-254">In the dialog box that appears, select **OK**.</span></span>

    <span data-ttu-id="59756-255">![BOM の承認](media/approve-dialog.png "BOM の承認")</span><span class="sxs-lookup"><span data-stu-id="59756-255">![Approving the BOM](media/approve-dialog.png "Approving the BOM")</span></span>

1. <span data-ttu-id="59756-256">**エンジニアリング バージョン** ページで、**部品表** クイックタブで、**アクティブにする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-256">On the **Engineering version** page, on the **Bill of material** FastTab, select **Activate**.</span></span>
1. <span data-ttu-id="59756-257">**アクティブにする** と **承認済** チェック ボックスが BOM に対して選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="59756-257">Notice that the **Active** and **Approved** check boxes are selected for the BOM.</span></span>

    <span data-ttu-id="59756-258">![BOM のアクティブ化と承認](media/approved-bom.png "BOM のアクティブ化と承認")</span><span class="sxs-lookup"><span data-stu-id="59756-258">![Active and approved BOM](media/approved-bom.png "Active and approved BOM")</span></span>

1. <span data-ttu-id="59756-259">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="59756-259">Close the page.</span></span>

## <a name="release-an-engineering-product-to-a-local-company"></a><a name="release"></a><span data-ttu-id="59756-260">ローカル会社へのエンジニアリング製品のリリース</span><span class="sxs-lookup"><span data-stu-id="59756-260">Release an engineering product to a local company</span></span>

<span data-ttu-id="59756-261">この製品は、現在エンジニアリング部門によって設計されています。</span><span class="sxs-lookup"><span data-stu-id="59756-261">The product has now been designed by the Engineering department.</span></span> <span data-ttu-id="59756-262">この例では、製品はエンジニアリングによって顧客向けに設計されたプロトタイプです。</span><span class="sxs-lookup"><span data-stu-id="59756-262">For this example, the product is a prototype that engineering has designed for a customer.</span></span> <span data-ttu-id="59756-263">顧客は *USFM* 法人の顧客であるため、製品をその法人にリリースする必要があります。</span><span class="sxs-lookup"><span data-stu-id="59756-263">Because the customer is a customer of the *USMF* legal entity, the product must be released to that legal entity.</span></span>

1. <span data-ttu-id="59756-264">法人は *DEMF* に設定したままにします。</span><span class="sxs-lookup"><span data-stu-id="59756-264">Keep the legal entity set to *DEMF*.</span></span> <span data-ttu-id="59756-265">(必要に応じて、ナビゲーション バーの右側にある会社ピッカーを使用します。)</span><span class="sxs-lookup"><span data-stu-id="59756-265">(Use the company picker on the right side of the navigation bar as required.)</span></span>
1. <span data-ttu-id="59756-266">**製品管理情報 &gt; 製品 &gt; リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="59756-266">Go to **Product information management &gt; Products &gt; Released products**.</span></span>
1. <span data-ttu-id="59756-267">製品 *Z0001* を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-267">Select product *Z0001*.</span></span>
1. <span data-ttu-id="59756-268">アクション ペインで **製品** タブの **管理** グループで、**製品構造のリリース** を選択して **製品リリース** ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="59756-268">On the Action Pane, on the **Product** tab, in the **Maintain** group, select **Release product structure** to open the **Release products** wizard.</span></span>
1. <span data-ttu-id="59756-269">**リリースするエンジニアリング製品の選択** ページで、製品 *Z0001* に対して **選択** チェックボックスを選択して。</span><span class="sxs-lookup"><span data-stu-id="59756-269">On the **Select engineering products to release** page, select the **Select** check box for product *Z0001*.</span></span>

    <span data-ttu-id="59756-270">![リリースするエンジニアリング製品の選択](media/select-eng-product-to-release.png "リリースするエンジニアリング製品の選択")</span><span class="sxs-lookup"><span data-stu-id="59756-270">![Selecting the engineering products to release](media/select-eng-product-to-release.png "Selecting the engineering products to release")</span></span>

1. <span data-ttu-id="59756-271">**リリースの詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-271">Select **Release details**.</span></span>
1. <span data-ttu-id="59756-272">**製品リリース詳細** ページが表示され、リリースされる製品の詳細と、その製品構造を確認できます。</span><span class="sxs-lookup"><span data-stu-id="59756-272">The **Product release details** page appears, where you can review the details of the product that will be released, and its product structure.</span></span> <span data-ttu-id="59756-273">**BOM を送る** オプションが *はい* に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="59756-273">Notice that the **Send BOM** option is set to *Yes*.</span></span> <span data-ttu-id="59756-274">したがって、BOM の製品 *Z0001* とすべての子品目がリリースされます。</span><span class="sxs-lookup"><span data-stu-id="59756-274">Therefore, both product *Z0001* and all its child items from the BOM will be released.</span></span>

    <span data-ttu-id="59756-275">左ウィンドウで任意の子項目を選択して、その詳細を確認できます。</span><span class="sxs-lookup"><span data-stu-id="59756-275">You can select any child item in the left pane to review its details.</span></span> <span data-ttu-id="59756-276">いずれかの子品目に BOM がある場合は、その子品目の BOM をリリースするように選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="59756-276">If any child item has a BOM, you can also select to release the BOM of that child item.</span></span>

    <span data-ttu-id="59756-277">![製品リリースの詳細の確認](media/product-release-details.png "製品リリースの詳細の確認")</span><span class="sxs-lookup"><span data-stu-id="59756-277">![Reviewing the product release details](media/product-release-details.png "Reviewing the product release details")</span></span>

1. <span data-ttu-id="59756-278">ページを閉じて、**リリース済み製品** ウィザードに戻ります。</span><span class="sxs-lookup"><span data-stu-id="59756-278">Close the page to return to the **Release products** wizard.</span></span>
1. <span data-ttu-id="59756-279">**次へ** を選択して、**リリースする製品を選択する** ページを選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-279">Select **Next** to open the **Select products to release** page.</span></span> <span data-ttu-id="59756-280">標準 (エンジニアリング以外) 製品を選択した場合は、このページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="59756-280">If you had selected any standard (non-engineering) products, they would appear on this page.</span></span> <span data-ttu-id="59756-281">**製品構造のリリース** を選択して標準製品をリリースすると 、BOM と工順もリリースされます。</span><span class="sxs-lookup"><span data-stu-id="59756-281">Note that when you release a standard product by selecting **Release product structure**, its BOM and route are also released.</span></span>

    <span data-ttu-id="59756-282">![リリースする標準製品の選択](media/select-std-product-to-release.png "リリースする標準製品の選択")</span><span class="sxs-lookup"><span data-stu-id="59756-282">![Selecting the standard products to release](media/select-std-product-to-release.png "Selecting the standard products to release")</span></span>

1. <span data-ttu-id="59756-283">**次へ** を選択して、**リリースする製品バリアントを選択する** ページを選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-283">Select **Next** to open the **Select product variants to release** page.</span></span> <span data-ttu-id="59756-284">この例では、バリアントは存在しません。</span><span class="sxs-lookup"><span data-stu-id="59756-284">For this example, there aren't any variants.</span></span>
1. <span data-ttu-id="59756-285">**次へ** を選択して、**会社を選択する** ページを選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-285">Select **Next** to open the **Select companies** page.</span></span>
1. <span data-ttu-id="59756-286">製品をリリースすべき会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-286">Select the companies that the product should be released to.</span></span> <span data-ttu-id="59756-287">この例の場合、**USMF** のチェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-287">For this example, select the check box for **USMF**.</span></span>

    <span data-ttu-id="59756-288">![リリース先の会社の選択](media/select-release-companies.png "リリース先の会社の選択")</span><span class="sxs-lookup"><span data-stu-id="59756-288">![Selecting the companies to release to](media/select-release-companies.png "Selecting the companies to release to")</span></span>

1. <span data-ttu-id="59756-289">**次へ** を選択して、**選択を確認する** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="59756-289">Select **Next** to open the **Confirm selection** page.</span></span>
1. <span data-ttu-id="59756-290">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-290">Select **Finish**.</span></span>

## <a name="review-and-accept-the-product-before-you-release-it-in-the-local-company"></a><a name="accept"></a><span data-ttu-id="59756-291">ローカル会社でリリースする前に製品をレビューして承認を行ってください</span><span class="sxs-lookup"><span data-stu-id="59756-291">Review and accept the product before you release it in the local company</span></span>

<span data-ttu-id="59756-292">これで、現在エンジニアリング部門は、製品が使用されるローカル会社に情報をリリースしています。</span><span class="sxs-lookup"><span data-stu-id="59756-292">The Engineering department has now released the information to the local companies where the product will be used.</span></span> <span data-ttu-id="59756-293">この例では、ローカル会社は *USMF* です。</span><span class="sxs-lookup"><span data-stu-id="59756-293">For this example, the local company is *USMF*.</span></span>

<span data-ttu-id="59756-294">*USMF* 会社の **エンジニアリング変更管理パラメータ** ページで **製品承認** フィールドを *手動* に設定しているため、製品をその会社にリリースする前に手動で承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59756-294">Because you set the **Product acceptance** field to *Manual* on the **Engineering change management parameters** page for the *USMF* company, products must be manually accepted before they are released to that company.</span></span> <span data-ttu-id="59756-295">つまり、リリース製品になる前に確認して承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59756-295">In other words, they must be reviewed and accepted before they become released products.</span></span>

<span data-ttu-id="59756-296">製品を確認して *USMF* 会社でリリースするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="59756-296">To review the product and release it in the *USMF* company, follow these steps.</span></span>

1. <span data-ttu-id="59756-297">法人は *USMF* に設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-297">Set the legal entity to *USMF*.</span></span> <span data-ttu-id="59756-298">(ナビゲーション バーの右側にある会社ピッカーを使用します。)</span><span class="sxs-lookup"><span data-stu-id="59756-298">(Use the company picker on the right side of the navigation bar.)</span></span>
1. <span data-ttu-id="59756-299">**エンジニアリング変更管理 &gt;共通 &gt; の製品リリース &gt; 未処理の製品リリース** に移動します。</span><span class="sxs-lookup"><span data-stu-id="59756-299">Go to **Engineering change management &gt; Common &gt; Product releases &gt; Open product releases**.</span></span>

    <span data-ttu-id="59756-300">**未処理の製品リリース** ページには、*承認待ちのステータス* を持つ製品 *Z0001* が表示されます。</span><span class="sxs-lookup"><span data-stu-id="59756-300">The **Open product releases** page shows product *Z0001*, which has a status of *Pending acceptance*.</span></span>

    <span data-ttu-id="59756-301">![製品リリースを開く](media/open-product-releases.png "製品リリースを開く")</span><span class="sxs-lookup"><span data-stu-id="59756-301">![Open product releases](media/open-product-releases.png "Open product releases")</span></span>

1. <span data-ttu-id="59756-302">**製品番号** 列の値を選択して、**製品リリースの詳細** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="59756-302">Select the value in the **Product number** column to open the **Product release details** page.</span></span> <span data-ttu-id="59756-303">次の詳細に留意してください。</span><span class="sxs-lookup"><span data-stu-id="59756-303">Notice the following details:</span></span>

    - <span data-ttu-id="59756-304">**一般** クイックタブには、製品リリースに関する情報 (この例では *DEMF*)、リリースするサイト (*1*)、入荷サイト (*1*) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="59756-304">The **General** FastTab shows information about the product release, such as the releasing company (*DEMF* for this example), the releasing site (*1*), and the receiving site (*1*).</span></span> <span data-ttu-id="59756-305">**製品のリリース** ウィザードでは、受信サイトを指定しなかったので、リリース後のサイトの値が受信サイトにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="59756-305">Because you didn't specify a receiving site in the **Release products** wizard, the the releasing site value is copied to the receiving site.</span></span>
    - <span data-ttu-id="59756-306">**リリースの詳細** クイックタブには、製品とリリースされたバージョンに関する情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="59756-306">The **Release details** FastTab shows information about the product and the version that was released.</span></span> <span data-ttu-id="59756-307">ここでは、有効期間の日付などの設定を変更できます。</span><span class="sxs-lookup"><span data-stu-id="59756-307">Here, you can modify settings such as the effectivity dates.</span></span>
    - <span data-ttu-id="59756-308">**工順** クイックタブには、製品の工順が表示されます。</span><span class="sxs-lookup"><span data-stu-id="59756-308">The **Route** FastTab shows the route of the product.</span></span> <span data-ttu-id="59756-309">ただし、この例では、工順がリリースされていません。</span><span class="sxs-lookup"><span data-stu-id="59756-309">However, for this example, you didn't release any routes.</span></span>

    <span data-ttu-id="59756-310">![製品リリースの詳細](media/product-release-details-2.png "製品リリースの詳細")</span><span class="sxs-lookup"><span data-stu-id="59756-310">![Product release details](media/product-release-details-2.png "Product release details")</span></span>

1. <span data-ttu-id="59756-311">情報の確認が完了したら、製品を承認して、*USMF* 会社でリリースする準備ができていることになります。</span><span class="sxs-lookup"><span data-stu-id="59756-311">When you've finished reviewing the information, you're ready to accept the product and, in this way, release it in the *USMF* company.</span></span> <span data-ttu-id="59756-312">アクション ペインで、**アクション &gt; 承認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-312">On the Action Pane, select **Actions &gt; Accept**.</span></span>
1. <span data-ttu-id="59756-313">*USMF* 会社で製品が今リリースされています。</span><span class="sxs-lookup"><span data-stu-id="59756-313">The product is now released in the *USMF* company.</span></span> <span data-ttu-id="59756-314">**製品管理情報 &gt; 製品 &gt; リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="59756-314">Go to **Product information management &gt;Products &gt; Released products**.</span></span> <span data-ttu-id="59756-315">品目 *Z0001* が表示されます。</span><span class="sxs-lookup"><span data-stu-id="59756-315">You should see item *Z0001*.</span></span>

## <a name="use-the-product-in-transactions-in-the-local-company"></a><span data-ttu-id="59756-316">ローカル会社のトランザクションでの製品の使用</span><span class="sxs-lookup"><span data-stu-id="59756-316">Use the product in transactions in the local company</span></span>

<span data-ttu-id="59756-317">*USMF* 会社のマスタ データ マネージャは、製品が *プロトタイプ* 状態にあることを確認して、ユーザーが作業中のプロセスに誤って追加した場合に警告が表示されるようにしたいと考えています。</span><span class="sxs-lookup"><span data-stu-id="59756-317">The master data manager for the *USMF* company wants to make sure that the product is in a *Prototype* state, to ensure that users will be warned if they accidentally add it to processes that they are working on.</span></span>

1. <span data-ttu-id="59756-318">**製品管理情報 &gt; 製品 &gt; リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="59756-318">Go to **Product information management &gt; Products &gt; Released products**.</span></span>
1. <span data-ttu-id="59756-319">製品 *Z0001* を選択して詳細ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="59756-319">Select product *Z0001* to open its details page.</span></span> <span data-ttu-id="59756-320">(このフィルターを使用して製品を検索できます。)</span><span class="sxs-lookup"><span data-stu-id="59756-320">(You can use the filter to find the product.)</span></span>
1. <span data-ttu-id="59756-321">アクション ペインの **エンジニア** タブの **エンジニアリング変更管理** グループで、**エンジニアリング バージョン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-321">On the Action Pane, on the **Engineer** tab, in the **Engineering change management** group, select **Engineering versions**.</span></span>
1. <span data-ttu-id="59756-322">**エンジニアリング バージョン** ページで、バージョン番号 *V-01* を選択して、詳細ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="59756-322">On the **Engineering versions** page, select version number *V-01* to open its details page.</span></span>
1. <span data-ttu-id="59756-323">アクション ペインで、**ライフサイクルの状態** グループにある **製品** タブで、**ライフサイクルの状態** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-323">On the Action Pane, on the **Product** tab, in the **Lifecycle state** group, select **Change lifecycle state**.</span></span>
1. <span data-ttu-id="59756-324">**ライフサイクル状態の変更** のダイアログ ボックスで、**状態** フィールドを *プロトタイプ* に設定し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-324">In the **Change lifecycle state** drop-down dialog box, set the **State** field to *Prototype*, and then select **OK**.</span></span>

    <span data-ttu-id="59756-325">![ライフサイクルの状態の変更](media/change-lifecycle-state.png "ライフサイクルの状態の変更")</span><span class="sxs-lookup"><span data-stu-id="59756-325">![Changing the lifecycle state](media/change-lifecycle-state.png "Changing the lifecycle state")</span></span>

## <a name="add-the-engineering-product-to-a-sales-order"></a><span data-ttu-id="59756-326">販売注文にエンジニアリング製品を追加する</span><span class="sxs-lookup"><span data-stu-id="59756-326">Add the engineering product to a sales order</span></span>

<span data-ttu-id="59756-327">これで、製品を顧客に販売できるようになります。</span><span class="sxs-lookup"><span data-stu-id="59756-327">The product can now be sold to a customer.</span></span> <span data-ttu-id="59756-328">販売注文ヘッダーに製品を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="59756-328">To add the product to a sales order, follow these steps.</span></span>

1. <span data-ttu-id="59756-329">**販売とマーケティング &gt; 販売注文 &gt; すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="59756-329">Go to **Sales and marketing &gt; Sales orders &gt; All sales orders**.</span></span>
1. <span data-ttu-id="59756-330">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-330">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="59756-331">**販売注文の作成** ダイアログボックスで、**顧客アカウント** フィールドを *US-0002* に設定して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-331">In the **Create sales order** dialog box, set the **Customer account** field to *US-0002*, and then select **OK**.</span></span>
1. <span data-ttu-id="59756-332">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="59756-332">The new sales order is opened.</span></span> <span data-ttu-id="59756-333">**販売注文明細行** クイックタブで、行を追加し、その行の **品目番号** フィールドを *Z000* を設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-333">On the **Sales order lines** FastTab, add a row, and set the **Item number** field to *Z000* for it.</span></span>
1. <span data-ttu-id="59756-334">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-334">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="59756-335">品目に *プロトタイプ* のステータスがあることを通知する警告メッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="59756-335">You receive a warning message that informs you that the item has a status of *Prototype*.</span></span> <span data-ttu-id="59756-336">ただし、このメッセージは単なる警告であり、販売注文が作成されています。</span><span class="sxs-lookup"><span data-stu-id="59756-336">However, because the message is just a warning, the sales order was still created.</span></span>

    <span data-ttu-id="59756-337">![エンジニアリング製品の販売注文](media/sales-order-eng-product.png "エンジニアリング製品の販売注文")</span><span class="sxs-lookup"><span data-stu-id="59756-337">![Sales order for an engineering product](media/sales-order-eng-product.png "Sales order for an engineering product")</span></span>

## <a name="request-changes-in-the-engineering-product"></a><span data-ttu-id="59756-338">エンジニアリング製品の変更の要求</span><span class="sxs-lookup"><span data-stu-id="59756-338">Request changes in the engineering product</span></span>

<span data-ttu-id="59756-339">この製品は顧客に送付されましたが、顧客は完全に満足しておらず、改善のための提案を含むフィードバックを提供します。</span><span class="sxs-lookup"><span data-stu-id="59756-339">The product was sent to a customer, but the customer wasn't completely satisfied and provides feedback that includes suggestions for improvement.</span></span> <span data-ttu-id="59756-340">顧客は電話で販売係と話していますが、販売係は顧客が説明している変更を要求できます。</span><span class="sxs-lookup"><span data-stu-id="59756-340">While the customer is speaking with a sales clerk on the phone, the sales clerk can request the changes that the customer is describing.</span></span>

1. <span data-ttu-id="59756-341">**販売とマーケティング &gt; 販売注文 &gt; すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="59756-341">Go to **Sales and marketing &gt; Sales orders &gt; All sales orders**.</span></span>
1. <span data-ttu-id="59756-342">前の演習で作成した販売注文を検索して開きます。</span><span class="sxs-lookup"><span data-stu-id="59756-342">Find and open the sales order that you created in the previous exercise.</span></span>
1. <span data-ttu-id="59756-343">**販売注文明細行** クイックタブで、**エンジニアリング変更管理 &gt; 新規エンジニアリング変更要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-343">On the **Sales order lines** FastTab, select **Engineering change management &gt; New engineering change request**.</span></span>

    <span data-ttu-id="59756-344">![販売注文からのエンジニアリング変更依頼の作成](media/sales-order-eng-change-request.png "販売注文からのエンジニアリング変更依頼の作成")</span><span class="sxs-lookup"><span data-stu-id="59756-344">![Creating an engineering change request from a sales order](media/sales-order-eng-change-request.png "Creating an engineering change request from a sales order")</span></span>

1. <span data-ttu-id="59756-345">顧客からのフィードバックに基づいて、エンジニアリング変更要求を入力します。</span><span class="sxs-lookup"><span data-stu-id="59756-345">Fill in the engineering change request, based on the customer's feedback.</span></span> <span data-ttu-id="59756-346">この例では、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-346">For this example, set the following values:</span></span>

    - <span data-ttu-id="59756-347">**変更要求:** *555*</span><span class="sxs-lookup"><span data-stu-id="59756-347">**Change request:** *555*</span></span>
    - <span data-ttu-id="59756-348">**タイトル:** *Z0001 顧客の変更*</span><span class="sxs-lookup"><span data-stu-id="59756-348">**Title:** *Z0001 customer change*</span></span>
    - <span data-ttu-id="59756-349">**優先度:** *低*</span><span class="sxs-lookup"><span data-stu-id="59756-349">**Priority:** *low*</span></span>
    - <span data-ttu-id="59756-350">**カテゴリ:** 変更の設定</span><span class="sxs-lookup"><span data-stu-id="59756-350">**Category:** set change</span></span>
    - <span data-ttu-id="59756-351">**重要度:** *中*</span><span class="sxs-lookup"><span data-stu-id="59756-351">**Severity:** *Medium*</span></span>

1. <span data-ttu-id="59756-352">**情報** クイック タブで、**新規 &gt; メモ** を選択してグリッドにメモを追加します。</span><span class="sxs-lookup"><span data-stu-id="59756-352">On the **Information** FastTab, select **New &gt; Note** to add a note to the grid.</span></span>
1. <span data-ttu-id="59756-353">新しい注記の **説明** フィールドで、品目 *D0003* を BOM から削除するように指定します。</span><span class="sxs-lookup"><span data-stu-id="59756-353">In the **Description** field for the new note, indicate that item *D0003* should be deleted from the BOM.</span></span> <span data-ttu-id="59756-354">メモの詳細情報を追加する必要がある場合は、**メモ** フィールドにテキストを入力できます。</span><span class="sxs-lookup"><span data-stu-id="59756-354">If you must add more information for the note, you can enter text in the **Notes** field.</span></span>

    <span data-ttu-id="59756-355">![エンジニアリング変更要求](media/eng-change-request.png "エンジニアリング変更要求")</span><span class="sxs-lookup"><span data-stu-id="59756-355">![Engineering change request](media/eng-change-request.png "Engineering change request")</span></span>

1. <span data-ttu-id="59756-356">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-356">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="59756-357">**製品** クイックタブに品目が自動的に追加され、エンジニアリング変更要求のソース (販売注文) が **製品** クイックタブに追加されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="59756-357">Notice that the item has automatically been added on the **Products** FastTab, and that the source of the engineering change request (the sales order) has been added on the **Source** FastTab.</span></span>

## <a name="make-changes-to-the-product-by-using-an-engineering-change-order"></a><span data-ttu-id="59756-358">エンジニアリング変更指示を使用して製品に変更を加える</span><span class="sxs-lookup"><span data-stu-id="59756-358">Make changes to the product by using an engineering change order</span></span>

<span data-ttu-id="59756-359">販売係は、製品が重要であり、それが顧客のために特別設計されたことを知っています。</span><span class="sxs-lookup"><span data-stu-id="59756-359">The sales clerk knows that the product is important and was designed especially for the customer.</span></span> <span data-ttu-id="59756-360">したがって、販売係は、*DEMF* 会社のエンジニアに変更依頼についての通知を依頼します。</span><span class="sxs-lookup"><span data-stu-id="59756-360">Therefore, the sales clerk calls an engineer in the *DEMF* company to notify them about the change request.</span></span> <span data-ttu-id="59756-361">このようにして、エンジニアはプロセスを高速化することができます。</span><span class="sxs-lookup"><span data-stu-id="59756-361">In this way, the engineer can speed up the process.</span></span>

<span data-ttu-id="59756-362">エンジニアは、顧客から要求を確認し、製品の変更オーダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="59756-362">The engineer now reviews the request from the customer and creates a change order for the product.</span></span>

1. <span data-ttu-id="59756-363">エンジニアが *DEMF* 会社で作業を行うため、法人を *DEMF* に設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-363">Because the engineer works in the *DEMF* company, set the legal entity to *DEMF*.</span></span> <span data-ttu-id="59756-364">(ナビゲーション バーの右側にある会社ピッカーを使用します。)</span><span class="sxs-lookup"><span data-stu-id="59756-364">(Use the company picker on the right side of the navigation bar.)</span></span>
1. <span data-ttu-id="59756-365">**エンジニアリング変更管理 &gt; 共通 &gt; エンジニアリング変更要求** に移動します。</span><span class="sxs-lookup"><span data-stu-id="59756-365">Go to **Engineering change management &gt; Common &gt; Engineering change requests**.</span></span>
1. <span data-ttu-id="59756-366">変更要求 *555* を開きます。</span><span class="sxs-lookup"><span data-stu-id="59756-366">Open change request *555*.</span></span>
1. <span data-ttu-id="59756-367">情報を確認し、変更を承認します。</span><span class="sxs-lookup"><span data-stu-id="59756-367">Review the information, and then approve the change.</span></span> <span data-ttu-id="59756-368">アクション ペインの **変更要求** タブで、**状態の変更** グループで、**承認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-368">On the Action Pane, on the **Change request** tab, in the **Change status** group, select **Approve**.</span></span>
1. <span data-ttu-id="59756-369">**エンジニアリング変更管理 &gt; 共通 &gt; エンジニアリング変更オーダー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="59756-369">Go to **Engineering change management &gt; Common &gt; Engineering change orders**.</span></span>
1. <span data-ttu-id="59756-370">アクション ペインで、変更オーダーを作成するために **新規** を選択して、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-370">On the Action Pane, select **New** to create a change order, and set the following values for it:</span></span>

    - <span data-ttu-id="59756-371">**変更オーダー:** *555*</span><span class="sxs-lookup"><span data-stu-id="59756-371">**Change order:** *555*</span></span>
    - <span data-ttu-id="59756-372">**タイトル:** *Z0001 顧客の変更*</span><span class="sxs-lookup"><span data-stu-id="59756-372">**Title:** *Z0001 customer change*</span></span>
    - <span data-ttu-id="59756-373">**カテゴリ:** *顧客変更*</span><span class="sxs-lookup"><span data-stu-id="59756-373">**Category:** *Customer change*</span></span>
    - <span data-ttu-id="59756-374">**優先度:** *低*</span><span class="sxs-lookup"><span data-stu-id="59756-374">**Priority:** *Low*</span></span>
    - <span data-ttu-id="59756-375">**重要度:** *中*</span><span class="sxs-lookup"><span data-stu-id="59756-375">**Severity:** *Medium*</span></span>

1. <span data-ttu-id="59756-376">**影響を受ける製品** クイックタブで、**新規 &gt; 既存の製品を追加** を選択して、グリッドに行を追加して次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59756-376">On the **Impacted products** FastTab, select **New &gt; Add existing product** to add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="59756-377">**製品:** *Z0001*</span><span class="sxs-lookup"><span data-stu-id="59756-377">**Product:** *Z0001*</span></span>
    - <span data-ttu-id="59756-378">**影響:** *新規バージョン*</span><span class="sxs-lookup"><span data-stu-id="59756-378">**Impact:** *New version*</span></span>

    <span data-ttu-id="59756-379">![エンジニアリング変更オーダーの作成](media/eng-change-order.png "エンジニアリング変更オーダーの作成")</span><span class="sxs-lookup"><span data-stu-id="59756-379">![Creating an engineering change order](media/eng-change-order.png "Creating an engineering change order")</span></span>

1. <span data-ttu-id="59756-380">**影響** フィールドを *新バージョン* に設定しているため、**製品の詳細** クイックタブの **詳細** タブにある **製品の詳細** フィールドには、新しいバージョン番号 (この例では *V-02* ) が何かが表示されます。</span><span class="sxs-lookup"><span data-stu-id="59756-380">Notice that, because you set the **Impact** field to *New version*, the **New version** field on the **Details** tab of the **Product details** FastTab shows what the new version number will be (*V-02* for this example).</span></span>

    <span data-ttu-id="59756-381">![エンジニアリング変更オーダーの製品詳細](media/eng-change-order-product-details.png "エンジニアリング変更オーダーの製品詳細")</span><span class="sxs-lookup"><span data-stu-id="59756-381">![Product details for an engineering change order](media/eng-change-order-product-details.png "Product details for an engineering change order")</span></span>

1. <span data-ttu-id="59756-382">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-382">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="59756-383">**製品の詳細** クイックタブの **部品表** タブで、**明細行** を選択して、製品 *Z0001* のバージョン *V-01* の BOM を開き ます。</span><span class="sxs-lookup"><span data-stu-id="59756-383">On the **Product details** FastTab, on the **Bill of material** tab, select **Lines** to open the BOM for version *V-01* of product *Z0001*.</span></span>

    <span data-ttu-id="59756-384">![エンジニアリング製品 BOM 明細行](media/eng-product-bom-lines.png "エンジニアリング製品 BOM 明細行")</span><span class="sxs-lookup"><span data-stu-id="59756-384">![Engineering product BOM lines](media/eng-product-bom-lines.png "Engineering product BOM lines")</span></span>

1. <span data-ttu-id="59756-385">品目番号 *D0003* の明細行を選択し、アクション ペインで **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-385">Select the line for item number *D0003*, and then, on the Action Pane, select **Delete**.</span></span> <span data-ttu-id="59756-386">この明細行の **種類の変更** フィールドの値が *削除済み* に変わります。</span><span class="sxs-lookup"><span data-stu-id="59756-386">The value of the **Change type** field for this line changes to *Deleted*.</span></span>
1. <span data-ttu-id="59756-387">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-387">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="59756-388">![変更されたエンジニアリング製品 BOM 明細行](media/eng-product-bom-lines-modified.png "変更されたエンジニアリング製品 BOM 明細行")</span><span class="sxs-lookup"><span data-stu-id="59756-388">![Modified engineering product BOM lines](media/eng-product-bom-lines-modified.png "Modified engineering product BOM lines")</span></span>

1. <span data-ttu-id="59756-389">**BOM 明細行** ページを閉じて、**エンジニアリング変更オーダー** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="59756-389">Close the **BOM line** page to return to the **Engineering change order** page.</span></span>
1. <span data-ttu-id="59756-390">**製品の詳細** クイックタブの **部品表** タブで、BOM *Z0001* の **変更タイプ** フィールドの値が、*変更済み* になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="59756-390">On the **Product details** FastTab, on the **Bill of material** tab, notice that the value of the **Change type** field for BOM *Z0001* is now *Changed*.</span></span>

    <span data-ttu-id="59756-391">![変更された BOM を含むエンジニアリング変更オーダー](media/eng-change-order-changed-bom.png "変更された BOM を含むエンジニアリング変更オーダー")</span><span class="sxs-lookup"><span data-stu-id="59756-391">![Engineering change order that includes a changed BOM](media/eng-change-order-changed-bom.png "Engineering change order that includes a changed BOM")</span></span>

    <span data-ttu-id="59756-392">このオーダーは変更を処理する前に承認される必要があります。</span><span class="sxs-lookup"><span data-stu-id="59756-392">The order must now be approved before the changes can be processed.</span></span> <span data-ttu-id="59756-393">変更が処理されると、エンジニアリング変更オーダーに含まれる変更で製品が更新されます。</span><span class="sxs-lookup"><span data-stu-id="59756-393">When the changes are processed, the products are updated with the changes that are included in the engineering change order.</span></span> <span data-ttu-id="59756-394">この例では、エンジニアリングの変更オーダーを作成した人物が承認者として指定されています。</span><span class="sxs-lookup"><span data-stu-id="59756-394">For this example, the person who creates the engineering change order has been specified as the approver.</span></span>

1. <span data-ttu-id="59756-395">アクション ペインの **変更―ダー** タブ、**状態の変更** グループで、**承認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-395">On the Action Pane, on the **Change order** tab, in the **Change status** group, select **Approve**.</span></span>
1. <span data-ttu-id="59756-396">**プロセス** を選択して、製品の情報を更新します。</span><span class="sxs-lookup"><span data-stu-id="59756-396">Select **Process** to update the product's information.</span></span>

## <a name="release-the-changed-product"></a><span data-ttu-id="59756-397">変更した製品のリリース</span><span class="sxs-lookup"><span data-stu-id="59756-397">Release the changed product</span></span>

<span data-ttu-id="59756-398">これで、製品は *USMF* 会社に再度リリースでき、顧客に送付できるようになります。</span><span class="sxs-lookup"><span data-stu-id="59756-398">The product can now be released again to the *USMF* company and then sent to the customer.</span></span> <span data-ttu-id="59756-399">エンジニアリング変更指示書から製品を直接リリースするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="59756-399">To release the product directly from the engineering change order, follow these steps.</span></span>

1. <span data-ttu-id="59756-400">前の手順で作成したエンジニアリング変更順序を開きます (まだ開いていない場合)。</span><span class="sxs-lookup"><span data-stu-id="59756-400">Open the engineering change order that you created in the previous exercise, if it isn't already open.</span></span>
1. <span data-ttu-id="59756-401">アクション ペインの **変更オーダー** タブ、**製品リリース** グループで、**検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-401">On the Action Pane, on the **Change order** tab, in the **Product releases** group, select **Search**.</span></span>
1. <span data-ttu-id="59756-402">この検索結果には、影響を受ける製品がどの会社にリリースされたかが示されます。</span><span class="sxs-lookup"><span data-stu-id="59756-402">The search results show which companies the affected products have been released to.</span></span> <span data-ttu-id="59756-403">検索結果を閉じます。</span><span class="sxs-lookup"><span data-stu-id="59756-403">Close the search results.</span></span>
1. <span data-ttu-id="59756-404">アクション ペインの **変更オーダー** タブ、**製品リリース** グループで、**表示** を選択して、**リリース** ダイアログボックスを開きます。ここでは前の検索の結果を表示できます。</span><span class="sxs-lookup"><span data-stu-id="59756-404">On the Action Pane, on the **Change order** tab, in the **Product releases** group, select **View** to open the **Releases** dialog box, where you can view the results of the previous search.</span></span>
1. <span data-ttu-id="59756-405">製品をリリースする各会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-405">Select each company that you want to release products to.</span></span>
1. <span data-ttu-id="59756-406">**OK** を選択し、**リリース**  ダイアログ ボックスを閉じて、偏光オーダーに戻ります。</span><span class="sxs-lookup"><span data-stu-id="59756-406">Select **OK** to close the **Releases** dialog box and return to the change order.</span></span>
1. <span data-ttu-id="59756-407">アクション ペインの、**変更オーダー** タブ、**製品リリース** グループで、**プロセス** を選択して、影響を受ける製品を選択した会社にリリースします。</span><span class="sxs-lookup"><span data-stu-id="59756-407">On the Action Pane, on the **Change order** tab, in the **Product releases** group, select **Process** to release the affected products to the selected companies.</span></span> <span data-ttu-id="59756-408">または、**製品構造のリリース** を選択してリリースプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="59756-408">Alternatively, select **Release product structure** to start the release process.</span></span>

## <a name="complete-the-change-order"></a><span data-ttu-id="59756-409">変更オーダーの完了</span><span class="sxs-lookup"><span data-stu-id="59756-409">Complete the change order</span></span>

<span data-ttu-id="59756-410">変更オーダーを完了としてマークして、それ以上のアクションが残っていないことを示す場合は、アクション ウィンドウで **完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59756-410">To mark the change order as completed, which indicates that no further actions remain, select **Complete** on the Action Pane.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
