---
title: チャンルごとの自動請求の有効化とコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 Commerce でチャネルごとに自動請求を有効にしてコンフィギュレーションする方法について説明します。
author: gvrmohanreddy
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 23d02cf96faf3753303435acc148bf71e487d791
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799918"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a><span data-ttu-id="bcb09-103">チャンルごとの自動請求の有効化とコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="bcb09-103">Enable and configure auto charges by channel</span></span>

<span data-ttu-id="bcb09-104">このトピックでは、Microsoft Dynamics 365 Commerce でチャネルごとに自動請求 (自動請求) を有効にしてコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-104">This topic explains how to enable and configure automatic charges (auto charges) by channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bcb09-105">概要</span><span class="sxs-lookup"><span data-stu-id="bcb09-105">Overview</span></span>

<span data-ttu-id="bcb09-106">特定の州 (たとえば、カリフォルニア) のすべてまたは一部の店舗で販売されている製品グループに、リサイクル料金やその他の料金が適用されるシナリオがあります。</span><span class="sxs-lookup"><span data-stu-id="bcb09-106">You might have scenarios where recycling fees or other fees must be applied to a group of products that are sold in all or some stores in a specific state (for example, California).</span></span> <span data-ttu-id="bcb09-107">Commerce の **チャネルごとの自動請求フィルターの有効化** 機能を使用すると、チャネルごとに自動請求を指定できます (たとえば、特定の従来型のチャネル)。</span><span class="sxs-lookup"><span data-stu-id="bcb09-107">The **Enable filter auto charges by channel** feature in Commerce lets you specify auto charges by channel (for example, a specific brick-and-mortar channel).</span></span> <span data-ttu-id="bcb09-108">この機能は、Dynamics 365 Commerce バージョン 10.0.10 以降 で利用できます。</span><span class="sxs-lookup"><span data-stu-id="bcb09-108">This feature is available in Dynamics 365 Commerce version 10.0.10 and later.</span></span>

<span data-ttu-id="bcb09-109">チャネルごとの自動請求を有効にしてコンフィギュレーションするには、次のタスクを完了する必要があります:</span><span class="sxs-lookup"><span data-stu-id="bcb09-109">To enable and configure auto charges by channel, you must complete the following tasks:</span></span>

- <span data-ttu-id="bcb09-110">**チャネルごとの自動請求フィルターの有効化** 機能をオンにします。</span><span class="sxs-lookup"><span data-stu-id="bcb09-110">Turn on the **Enable filter auto charges by channel** feature.</span></span>
- <span data-ttu-id="bcb09-111">組織階層の目的をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="bcb09-111">Configure the organization hierarchy purpose.</span></span>
- <span data-ttu-id="bcb09-112">チャネルごとの自動請求を定義します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-112">Define auto charges by channel.</span></span>

> [!NOTE]
> <span data-ttu-id="bcb09-113">**チャネルごとの自動請求フィルターの有効化** 機能は、高度な自動請求機能も有効になっている場合にのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-113">The **Enable filter auto charges by channel** feature works only if the advanced auto charges feature is also turned on.</span></span> <span data-ttu-id="bcb09-114">高度な自動請求機能を有効にする方法については、[オムニ チャネルの高度な自動請求](omni-auto-charges.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bcb09-114">For information about how to turn on the advanced auto charges feature, see [Omni-channel advanced auto charges](omni-auto-charges.md).</span></span>

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a><span data-ttu-id="bcb09-115">チャネルごとの自動請求フィルターの有効化機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="bcb09-115">Turn on the Enable filter auto charges by channel feature</span></span>

<span data-ttu-id="bcb09-116">Commerce でチャネルごとの自動請求を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-116">To enable auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="bcb09-117">**システム管理者 \> ワークスペース \> 機能管理** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-117">Go to **System administrator \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="bcb09-118">**無効** タブの **機能名** 一覧で、**チャネルごとの自動請求フィルターの有効化** を見つけて選択します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-118">On the **Not enabled** tab, in the **Feature name** list, find and select **Enable filter auto charges by channel**.</span></span>
1. <span data-ttu-id="bcb09-119">右下隅の **直ちに有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-119">In the lower-right corner, select **Enable now**.</span></span> <span data-ttu-id="bcb09-120">機能が有効になると、**すべて** タブの一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="bcb09-120">After the feature has been turned on, it will appear in the list on the **All** tab.</span></span>
1. <span data-ttu-id="bcb09-121">**Retail とコマース \> Retail とコマース IT \> 配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-121">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="bcb09-122">左ウィンドウで、**1110** (**グローバル コンフィギュレーション**) ジョブを見つけて選択します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-122">In the left pane, find and select the **1110** (**Global configuration**) job.</span></span>
1. <span data-ttu-id="bcb09-123">アクション ウィンドウで、**今すぐ実行** を選択して、コンフィギュレーションの変更を反映します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-123">On the Action Pane, select **Run now** to propagate the configuration changes.</span></span>

> [!WARNING]
> <span data-ttu-id="bcb09-124">使用後に、**チャネルごとの自動請求フィルターの有効化** 機能をオフにすると、**自動請求** の **小売チャネル リレーション** フィールドは表示されなくなり、既存のコンフィギュレーションはすべて失われます。</span><span class="sxs-lookup"><span data-stu-id="bcb09-124">If you turn off the **Enable filter auto charges by channel** feature after you've already used it, the **Retail channel relation** field under **Auto charges** will no longer appear, and you will lose all existing configurations.</span></span> <span data-ttu-id="bcb09-125">**小売チャネル リレーション** コンフィギュレーションの削除によって自動請求ルールが重複する場合、この機能をオフにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="bcb09-125">If removal of the **Retail channel relation** configurations will cause auto charges rules to be duplicated, an attempt to turn off the feature will fail.</span></span> <span data-ttu-id="bcb09-126">この機能をオフにする前に、すべての自動請求ルールを確認し、必要な変更を行うようにしてください。</span><span class="sxs-lookup"><span data-stu-id="bcb09-126">Before you turn off the feature, be sure to review all auto charges rules and make any required changes.</span></span>

## <a name="configure-the-organization-hierarchy-purpose"></a><span data-ttu-id="bcb09-127">組織階層の目的をコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="bcb09-127">Configure the organization hierarchy purpose</span></span>

<span data-ttu-id="bcb09-128">**小売自動請求** という名前の新しい組織階層の目的が、チャンネルごとの自動請求の階層を管理するために作成されました。</span><span class="sxs-lookup"><span data-stu-id="bcb09-128">A new organization hierarchy purpose that is named **Retail auto charge** has been created to manage the hierarchy for auto charges by channel.</span></span>

<span data-ttu-id="bcb09-129">Commerce の組織階層の目的に既定の階層を割り当てるには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-129">To assign a default hierarchy to an organization hierarchy purpose in Commerce, follow these steps.</span></span>
        
1. <span data-ttu-id="bcb09-130">**組織管理 \> 組織 \> 組織階層の目的** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-130">Go to **Organization administration \> Organizations \> Organization hierarchy purposes**.</span></span>
1. <span data-ttu-id="bcb09-131">左ウィンドウで **小売自動請求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-131">In the left pane, select **Retail auto charge**.</span></span>
1. <span data-ttu-id="bcb09-132">**割り当て済の階層** で **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-132">Under **Assigned hierarchies**, select **Add**.</span></span>
1. <span data-ttu-id="bcb09-133">**組織階層** ダイアログ ボックスで、組織階層 (たとえば **地域ごとの小売店舗**) を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-133">In the **Organization hierarchies** dialog box, select an organization hierarchy (for example, **Retail Stores by Region**), and then select **OK**.</span></span>
1. <span data-ttu-id="bcb09-134">**割り当て済の階層** で **既定として設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-134">Under **Assigned hierarchies**, select **Set as default**.</span></span>
1. <span data-ttu-id="bcb09-135">**Retail とコマース \> Retail とコマース IT \> 配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="bcb09-136">左ウィンドウで、**1040** (**製品**) ジョブを見つけて選択します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-136">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="bcb09-137">アクション ウィンドウで、**今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-137">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="bcb09-138">前の 2 つの手順を繰り返して、**1070** (**チャンネル コンフィギュレーション**) と **1110** (**グローバル コンフィギュレーション**) ジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-138">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>

![小売自動請求の組織階層の目的をコンフィギュレーションする](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a><span data-ttu-id="bcb09-140">チャネルごとの自動請求を定義する</span><span class="sxs-lookup"><span data-stu-id="bcb09-140">Define auto charges by channel</span></span>

<span data-ttu-id="bcb09-141">**チャネルごとの自動請求フィルターの有効化** 機能をオンにして、**小売自動請求** の組織階層の目的をコンフィギュレーションすると、チャンネルごとの自動請求は、注文ヘッダー レベルまたは注文明細行レベルで定義できます。</span><span class="sxs-lookup"><span data-stu-id="bcb09-141">After you've turned on the **Enable filter auto charges by channel** feature and configured the **Retail auto charge** organization hierarchy purpose, auto charges by channel can be defined at either the order header level or the order line level.</span></span>

<span data-ttu-id="bcb09-142">Commerce でチャネルごとの自動請求を定義にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-142">To define auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="bcb09-143">**売掛金 \> 諸費用の設定 \> 自動請求** に移動します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-143">Go to **Accounts receivable \> Charges setup \> Auto charges**.</span></span>
1. <span data-ttu-id="bcb09-144">左ウィンドウの **レベル** フィールドで、業務要件に応じて **ヘッダー** または **明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-144">In the left pane, in the **Level** field, select either **Header** or **Line**, depending on your business requirements.</span></span>
1. <span data-ttu-id="bcb09-145">**小売チャネル コード** フィールドで、適切なチャンネル コード (たとえば、**テーブル**、**グループ**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-145">In the **Retail channel code** field, select the appropriate channel code (for example, **Table** or **Group**).</span></span> <span data-ttu-id="bcb09-146">既定の設定の **すべて** が使用されている場合、すべてのチャネルに請求ルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="bcb09-146">If the default setting, **All**, is used, charge rules are applied to all channels.</span></span>

    - <span data-ttu-id="bcb09-147">**グループ** を選択した場合は、小売チャンネルの請求金額グループが **Retail と Commerce \> チャネル設定 \> 請求金額 \> 小売チャンネルの請求金額グループ** で作成されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="bcb09-147">If you select **Group**, make sure that a retail channel charges group is created at **Retail and Commerce \> Channel setup \> Charges \> Retail channel charge groups**.</span></span>
    - <span data-ttu-id="bcb09-148">**テーブル** を選択した場合は、**小売チャネル リレーション** フィールドで特定のチャネル (たとえば、**サンフランシスコ**) を選択できます。</span><span class="sxs-lookup"><span data-stu-id="bcb09-148">If you select **Table**, you can select a specific channel (for example, **San Francisco**) in the **Retail channel relation** field.</span></span>

1. <span data-ttu-id="bcb09-149">**Retail とコマース \> Retail とコマース IT \> 配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-149">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="bcb09-150">左ウィンドウで、**1040** (**製品**) ジョブを見つけて選択します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-150">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="bcb09-151">アクション ウィンドウで、**今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-151">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="bcb09-152">前の 2 つの手順を繰り返して、**1070** (**チャンネル コンフィギュレーション**) と **1110** (**グローバル コンフィギュレーション**) ジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-152">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>
    
![チャネルによって定義された自動請求](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a><span data-ttu-id="bcb09-154">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="bcb09-154">Example scenario</span></span>

<span data-ttu-id="bcb09-155">次の例では、製品がサンフランシスコの従来型チャネルで販売される場合にリサイクル料金が請求されるように、製品をコンフィギュレーションするために必要な手順の概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-155">The following example outlines the steps that are required to configure a product so that recycling fees are charged when the product is sold through a San Francisco brick-and-mortar channel.</span></span> <span data-ttu-id="bcb09-156">この例では、コマース販売時点管理 (POS) アプリケーションでの自動請求の表示方法も示しています。</span><span class="sxs-lookup"><span data-stu-id="bcb09-156">The example also shows how the auto charges appear in the Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="bcb09-157">次の図に示すように、組織は、**リサイクル** という名前の費用コードを定義します。</span><span class="sxs-lookup"><span data-stu-id="bcb09-157">The organization defines a charges code that is named **RECYCLE**, as shown in the following illustration.</span></span>

![リサイクル 費用コード](media/Auto-charges-charge-code.png)

<span data-ttu-id="bcb09-159">自動請求は明細行レベルで作成されます。</span><span class="sxs-lookup"><span data-stu-id="bcb09-159">An auto charge is created at the line level.</span></span> <span data-ttu-id="bcb09-160">次のコンフィギュレーションがあります:</span><span class="sxs-lookup"><span data-stu-id="bcb09-160">It has the following configuration:</span></span>

- <span data-ttu-id="bcb09-161">**アカウント コード** フィールドは **すべて** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="bcb09-161">The **Account code** field is set to **All**.</span></span>
- <span data-ttu-id="bcb09-162">**品目コード** フィールドは **テーブル** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="bcb09-162">The **Item code** field is set to **Table**.</span></span>
- <span data-ttu-id="bcb09-163">**商品関係** フィールドは、製品 ID **91001** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="bcb09-163">The **Item relation** field is set to product ID **91001**.</span></span>
- <span data-ttu-id="bcb09-164">**荷渡方法のコード** フィールドは **すべて** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="bcb09-164">The **Mode of delivery code** field is set to **All**.</span></span>
- <span data-ttu-id="bcb09-165">**小売チャネル コード** フィールドは **テーブル** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="bcb09-165">The **Retail channel code** field is set to **Table**.</span></span>
- <span data-ttu-id="bcb09-166">**小売チャネル リレーション** フィールドは **サンフランシスコ** の店舗に設定されています。</span><span class="sxs-lookup"><span data-stu-id="bcb09-166">The **Retail channel relation** field is set to the **San Francisco** store.</span></span>

<span data-ttu-id="bcb09-167">自動請求明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="bcb09-167">An auto charges line is created.</span></span> <span data-ttu-id="bcb09-168">次のコンフィギュレーションがあります:</span><span class="sxs-lookup"><span data-stu-id="bcb09-168">It has the following configuration:</span></span>

- <span data-ttu-id="bcb09-169">**通貨** フィールドは **USD** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="bcb09-169">The **Currency** field is set to **USD**.</span></span>
- <span data-ttu-id="bcb09-170">**諸費用コード** フィールドは **リサイクル** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="bcb09-170">The **Charges code** field is set to **RECYCLE**.</span></span>
- <span data-ttu-id="bcb09-171">**カテゴリ** フィールドは **固定** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="bcb09-171">The **Category** field is set to **Fixed**.</span></span>
- <span data-ttu-id="bcb09-172">**諸費用** フィールドは **$6.25** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="bcb09-172">The **Charges** field is set to **$6.25**.</span></span>

![明細行レベルの自動請求と自動請求明細行のコンフィギュレーション](media/Auto-charges-recyclingfee-line-fee.png)

<span data-ttu-id="bcb09-174">POS アプリケーションでは、**サンフランシスコ** の店舗チャネルで販売注文が作成されます。</span><span class="sxs-lookup"><span data-stu-id="bcb09-174">In the POS application, a sales order is created in the **San Francisco** store channel.</span></span> <span data-ttu-id="bcb09-175">**諸費用** 明細行には、**$6.25** のリサイクル料金が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bcb09-175">The **Charges** line shows the recycling fee of **$6.25**.</span></span>

<span data-ttu-id="bcb09-176">POS アプリケーションで **トランザクション オプション \> 諸費用 \> 諸費用の管理** を選択すると、リサイクル料金の諸費用コードと説明を表示できます。</span><span class="sxs-lookup"><span data-stu-id="bcb09-176">By selecting **Transaction options \> Charges \> Manage charges** in the POS application, you can view the charges code and description for the recycling fee.</span></span>

![POS アプリケーションのリサイクル料金](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a><span data-ttu-id="bcb09-178">追加リソース</span><span class="sxs-lookup"><span data-stu-id="bcb09-178">Additional resources</span></span>

[<span data-ttu-id="bcb09-179">オムニ チャネルの高度な自動請求</span><span class="sxs-lookup"><span data-stu-id="bcb09-179">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="bcb09-180">ヘッダー請求金額を一致する販売明細行に比例配分する</span><span class="sxs-lookup"><span data-stu-id="bcb09-180">Prorate header charges to matching sales lines</span></span>](pro-rate-charges-matching-lines.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]