---
title: 陸揚原価の照会
description: このトピックでは、陸揚原価モジュールで使用できるさまざまなタイプの照会を検索して使用する方法について説明します。
author: sherry-zheng
manager: tfehr
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMLine, ITMItemTracking, ITMContainerActivityTracking, ITMContainerTracking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 10f5948b4e3df089aef982269143254d9ac1e8a9
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500359"
---
# <a name="landed-cost-inquiries"></a><span data-ttu-id="9b1fd-103">陸揚原価の照会</span><span class="sxs-lookup"><span data-stu-id="9b1fd-103">Landed cost inquiries</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="voyage-line-inquiries"></a><span data-ttu-id="9b1fd-104">航海明細行の照会</span><span class="sxs-lookup"><span data-stu-id="9b1fd-104">Voyage line inquiries</span></span>

<span data-ttu-id="9b1fd-105">**航海明細行** 照会には、在庫に関連するすべての航海明細行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-105">The **Voyage lines** inquiry shows all voyage lines as they pertain to inventory.</span></span> <span data-ttu-id="9b1fd-106">この照会は、品目、発注書、または他の役立つ情報を検索するのに役立つフィルターとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-106">This inquiry can be used as a filter to help you find an item, purchase order, or other useful piece of information.</span></span> <span data-ttu-id="9b1fd-107">また、複数の航海上の品目の配送予定日を識別するためにも使用できます。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-107">It can also be used to identify the expected delivery date of an item that might be on one or more voyages.</span></span> <span data-ttu-id="9b1fd-108">これにより、予想在庫の入庫を管理できます。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-108">In this way, it can help you manage expected inventory receiving.</span></span>

<span data-ttu-id="9b1fd-109">この照会を開くには、**陸揚原価 \> 照会 \> 航海明細行** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-109">To open this inquiry, go to **Landed cost \> Inquiries \> Voyage lines**.</span></span>

### <a name="overview-tab"></a><span data-ttu-id="9b1fd-110">[概要] タブ</span><span class="sxs-lookup"><span data-stu-id="9b1fd-110">Overview tab</span></span>

<span data-ttu-id="9b1fd-111">**航海明細行** 照会ページの **概要** タブには、関連する各航海明細行に関する基本情報を示すグリッドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-111">The **Overview** tab of the **Voyage lines** inquiry page includes a grid that shows basic information about each relevant voyage line.</span></span> <span data-ttu-id="9b1fd-112">次のテーブルでは、グリッドの列について説明します。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-112">The following table describes the columns in the grid.</span></span>

| <span data-ttu-id="9b1fd-113">円柱</span><span class="sxs-lookup"><span data-stu-id="9b1fd-113">Column</span></span> | <span data-ttu-id="9b1fd-114">説明</span><span class="sxs-lookup"><span data-stu-id="9b1fd-114">Description</span></span> |
|---|---|
| <span data-ttu-id="9b1fd-115">**品目番号**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-115">**Item number**</span></span> | <span data-ttu-id="9b1fd-116">航海明細行の品目。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-116">The item for the voyage line.</span></span> |
| <span data-ttu-id="9b1fd-117">**参照**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-117">**Reference**</span></span> | <span data-ttu-id="9b1fd-118">注文のタイプ (発注書または移動オーダー)。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-118">The type of order (purchase order or transfer order).</span></span> |
| <span data-ttu-id="9b1fd-119">**番号**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-119">**Number**</span></span> | <span data-ttu-id="9b1fd-120">発注書番号または移動オーダー番号。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-120">The purchase order number or transfer order number.</span></span> |
| <span data-ttu-id="9b1fd-121">**フォリオ**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-121">**Folio**</span></span> | <span data-ttu-id="9b1fd-122">航海明細行に関連付けられているフォリオ。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-122">The folio that is associated with the voyage line.</span></span> |
| <span data-ttu-id="9b1fd-123">**出荷コンテナー**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-123">**Shipping container**</span></span> | <span data-ttu-id="9b1fd-124">航海明細行に関連付けられている出荷コンテナー。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-124">The shipping container that is associated with the voyage line.</span></span> |
| <span data-ttu-id="9b1fd-125">**航海**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-125">**Voyage**</span></span> | <span data-ttu-id="9b1fd-126">航海明細行に関連付けられている航海。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-126">The voyage that is associated with the voyage line.</span></span> |
| <span data-ttu-id="9b1fd-127">**件数**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-127">**Quantity**</span></span> | <span data-ttu-id="9b1fd-128">航海明細行の品目の数量。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-128">The quantity of the item for the voyage line.</span></span> |
| <span data-ttu-id="9b1fd-129">(他の分析コード)</span><span class="sxs-lookup"><span data-stu-id="9b1fd-129">(Other dimensions)</span></span> | <span data-ttu-id="9b1fd-130">必要に応じて、追加の分析コードの列を表示できます。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-130">You can show columns for additional dimensions as you require.</span></span> <span data-ttu-id="9b1fd-131">これらの分析コードには、バッチ番号、在庫状態、および倉庫が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-131">Those dimensions include batch number, inventory status, and warehouse.</span></span> <span data-ttu-id="9b1fd-132">アクション ウィンドウで、**在庫 \> 表示分析コード** を選択して、含める分析コードを選択できるダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-132">On the Action Pane, select **Inventory \> Display dimensions** to open a dialog box where you can select the dimensions to include.</span></span> |

### <a name="general-tab"></a><span data-ttu-id="9b1fd-133">[全般] タブ</span><span class="sxs-lookup"><span data-stu-id="9b1fd-133">General tab</span></span>

<span data-ttu-id="9b1fd-134">**全般** タブを選択して、**概要** タブで現在選択されている明細行の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-134">Select the **General** tab to view more information about the line that is currently selected on the **Overview** tab.</span></span>

### <a name="dimensions-tab"></a><span data-ttu-id="9b1fd-135">分析コード タブ</span><span class="sxs-lookup"><span data-stu-id="9b1fd-135">Dimensions tab</span></span>

<span data-ttu-id="9b1fd-136">**分析コード** タブを選択して、このタブで選択した分析コードにかかわらず、**概要** タブで現在選択された明細行のすべての利用可能な在庫分析コードの値を表示します。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-136">Select the **Dimensions** tab to view values for all available dimensions for the line that is currently selected on the **Overview** tab, regardless of the dimensions that you've selected to show on that tab.</span></span>

## <a name="cost-estimate-inquiries"></a><span data-ttu-id="9b1fd-137">原価見積の照会</span><span class="sxs-lookup"><span data-stu-id="9b1fd-137">Cost estimate inquiries</span></span>

<span data-ttu-id="9b1fd-138">原価見積を生成すると、その見積が **原価見積** の照会ページに追加されます。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-138">Every time that you generate a cost estimate, the estimate is added to the **Cost estimates** inquiry page.</span></span> <span data-ttu-id="9b1fd-139">原価見積 (照会ページの見積を含む) を生成、表示、および使用する方法の詳細については、[陸揚原価の見積および管理](estimate-manage-landed-costs.md)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-139">For complete details about how to generate, view, and work with cost estimates (including estimates on the inquiry page), see [Estimate and manage landed costs](estimate-manage-landed-costs.md).</span></span>

## <a name="item-tracking"></a><span data-ttu-id="9b1fd-140">品目追跡</span><span class="sxs-lookup"><span data-stu-id="9b1fd-140">Item tracking</span></span>

<span data-ttu-id="9b1fd-141">**品目追跡** ページを使用して、オープン発注書明細行とその現在の状態を表示します。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-141">Use the **Item tracking** page to view open purchase orders lines and their current status.</span></span> <span data-ttu-id="9b1fd-142">明細行は、ここに表示される航海に関連付けられる必要はありません。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-142">Lines don't have to be associated with a voyage to appear here.</span></span> <span data-ttu-id="9b1fd-143">ただし、品目が航海に関連付けられている場合、品目追跡レコードの明細行には航海 ID が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-143">However, if an item is associated with a voyage, the item tracking record line shows the voyage ID.</span></span>

<span data-ttu-id="9b1fd-144">このページを開くには、**陸揚原価 \> 照会 \> 追跡 \> 品目追跡** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-144">To open this page, go to **Landed cost \> Inquiries \> Tracking \> Item tracking**.</span></span>

<span data-ttu-id="9b1fd-145">発注書明細行が大量に含まれている可能性が高いシステムでは、最初はレコードが表示されない **品目追跡** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-145">Because your system probably contains a very large number of purchase order lines, the **Item tracking** page initially shows no records.</span></span> <span data-ttu-id="9b1fd-146">ページ上部のフィルター フィールドを使用して、検索する発注書明細行のセットを定義し始めます。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-146">Start by using the filter fields at the top of the page to define the set of purchase order lines that you're looking for.</span></span> <span data-ttu-id="9b1fd-147">その後、アクション ウィンドウの **更新** を選択して一覧を生成します。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-147">Then select **Update** on the Action Pane to generate the list.</span></span> <span data-ttu-id="9b1fd-148">アスタリスク (\*) をフィルター フィールドのいずれかでワイルドカード文字として使用できます。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-148">You can use an asterisk (\*) as a wildcard character in any of the filter fields.</span></span> <span data-ttu-id="9b1fd-149">たとえば、名前に "DVD" という語を含む品目のすべての発注書明細行を検索するには、**タイプ** フィールドを **製品名** に設定し、**フィールド値** フィールドに *\*DVD\** と入力します。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-149">For example, to find all purchase order lines for items that include the word "DVD" in their name, set the **Type** field to **Product name**, and enter *\*DVD\** in the **Field value** field.</span></span>

> [!NOTE]
> <span data-ttu-id="9b1fd-150">現時点では、受注残には販売注文のみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-150">Currently, backorders include only sales orders.</span></span> <span data-ttu-id="9b1fd-151">販売見積は、受注残として表示または考慮されません。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-151">Sales quotations aren't shown or considered backorders.</span></span>

<span data-ttu-id="9b1fd-152">次の表では、**品目追跡** ページのグリッド内の列について説明します。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-152">The following table describes the columns in the grid on the **Item tracking** page.</span></span>

| <span data-ttu-id="9b1fd-153">円柱</span><span class="sxs-lookup"><span data-stu-id="9b1fd-153">Column</span></span> | <span data-ttu-id="9b1fd-154">説明</span><span class="sxs-lookup"><span data-stu-id="9b1fd-154">Description</span></span> |
|---|---|
| <span data-ttu-id="9b1fd-155">**出荷先港**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-155">**To port**</span></span> | <span data-ttu-id="9b1fd-156">最終目的地。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-156">The final destination.</span></span> |
| <span data-ttu-id="9b1fd-157">**確定済**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-157">**Confirmed**</span></span> | <span data-ttu-id="9b1fd-158">発注書明細行の確定済日付。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-158">The confirmed date of the purchase order line.</span></span> |
| <span data-ttu-id="9b1fd-159">**配送日**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-159">**Delivery Date**</span></span> | <span data-ttu-id="9b1fd-160">発注書明細行の配送日。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-160">The delivery date of the purchase order line.</span></span> |
| <span data-ttu-id="9b1fd-161">**航海**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-161">**Voyage**</span></span> | <span data-ttu-id="9b1fd-162">明細行が航海に関連付けられている場合の航海 ID。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-162">If the line is associated with a voyage, the voyage ID.</span></span> |
| <span data-ttu-id="9b1fd-163">**出荷コンテナー**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-163">**Shipping Container**</span></span> | <span data-ttu-id="9b1fd-164">明細行が出荷コンテナーに関連付けられている場合のコンテナー ID。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-164">If the line is attached to a shipping container, the container ID.</span></span> |
| <span data-ttu-id="9b1fd-165">**出荷港**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-165">**Shipping port**</span></span> | <span data-ttu-id="9b1fd-166">追跡フォームの最初の区間に基づく現在の港。発注書明細行に関連付けられている出荷コンテナーの実際の日付は設定されていません。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-166">The current port, based on the first leg in the tracking form where no actual date is set for the shipping container that is associated with the purchase order line.</span></span> |
| <span data-ttu-id="9b1fd-167">**活動**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-167">**Activity**</span></span> | <span data-ttu-id="9b1fd-168">追跡フォームの最初の区間に基づく現在の活動。発注書明細行に関連付けられている出荷コンテナーの実際の日付は設定されていません。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-168">The current activity, based on the first leg in the tracking form where no actual date is set for the shipping container that is associated with the purchase order line.</span></span> |
| <span data-ttu-id="9b1fd-169">**見積終了日**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-169">**Estimated end date**</span></span> | <span data-ttu-id="9b1fd-170">航海が出荷先倉庫に入庫する予定日。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-170">The date when the voyage is expected to be received at the destination warehouse.</span></span> |
| <span data-ttu-id="9b1fd-171">**氏名**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-171">**Name**</span></span> | <span data-ttu-id="9b1fd-172">仕入先の名前。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-172">The name of the vendor.</span></span> |
| <span data-ttu-id="9b1fd-173">**航海状態**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-173">**Voyage Status**</span></span> | <span data-ttu-id="9b1fd-174">発注書明細行に関連付けられている出荷状態。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-174">The shipment status that is attached to the purchase order line.</span></span> |
| <span data-ttu-id="9b1fd-175">**品目番号**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-175">**Item number**</span></span> | <span data-ttu-id="9b1fd-176">発注書明細行の品目番号。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-176">The item number for the purchase order line.</span></span> |
| <span data-ttu-id="9b1fd-177">**外部品目番号**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-177">**External**</span></span> | <span data-ttu-id="9b1fd-178">仕入先の品目名。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-178">The vendor's item name.</span></span> |
| <span data-ttu-id="9b1fd-179">**製品名**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-179">**Product Name**</span></span> | <span data-ttu-id="9b1fd-180">発注書明細行の品目の名前。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-180">The name of the item for the purchase order line.</span></span> |
| <span data-ttu-id="9b1fd-181">**件数**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-181">**Quantity**</span></span> | <span data-ttu-id="9b1fd-182">発注書明細行の発注書明細行数。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-182">The purchase order line quantity for the purchase order line.</span></span> |
| <span data-ttu-id="9b1fd-183">**単位**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-183">**Unit**</span></span> | <span data-ttu-id="9b1fd-184">発注書明細行の測定単位。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-184">The unit of measure for the purchase order line.</span></span> |
| <span data-ttu-id="9b1fd-185">**参照**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-185">**Reference**</span></span> | <span data-ttu-id="9b1fd-186">注文のタイプ (発注書または移動オーダー)</span><span class="sxs-lookup"><span data-stu-id="9b1fd-186">The type of order (purchase order or transfer order)</span></span> |
| <span data-ttu-id="9b1fd-187">**参照番号**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-187">**Reference number**</span></span> | <span data-ttu-id="9b1fd-188">発注書番号または移動オーダー番号。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-188">The purchase order number or transfer order number.</span></span> |
| <span data-ttu-id="9b1fd-189">**オーダー残**</span><span class="sxs-lookup"><span data-stu-id="9b1fd-189">**Backorder**</span></span> | <span data-ttu-id="9b1fd-190">記号は、その品目の販売オーダー残があることを示します。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-190">A symbol indicates that there are sales backorders for the item.</span></span> |
| <span data-ttu-id="9b1fd-191">(他の分析コード)</span><span class="sxs-lookup"><span data-stu-id="9b1fd-191">(Other dimensions)</span></span> | <span data-ttu-id="9b1fd-192">必要に応じて、追加の分析コードの列を表示できます。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-192">You can show columns for additional dimensions as you require.</span></span> <span data-ttu-id="9b1fd-193">これらの分析コードには、バッチ番号、在庫状態、および倉庫が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-193">Those dimensions include batch number, inventory status, and warehouse.</span></span> <span data-ttu-id="9b1fd-194">アクション ウィンドウで、**分析コードの表示** を選択して、含める分析コードを選択できるダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-194">On the Action Pane, select **Display dimensions** to open a dialog box where you can select the dimensions to include.</span></span> |

### <a name="related-information-about-backorders"></a><span data-ttu-id="9b1fd-195">オーダー残の関連情報</span><span class="sxs-lookup"><span data-stu-id="9b1fd-195">Related information about backorders</span></span>

<span data-ttu-id="9b1fd-196">オーダー残の詳細を表示するには、ページの右側にある **関連情報** タブを選択してから、**オーダー残** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-196">To view more information about backorders, select the **Related information** tab on the right side of the page, and then select **Backorders**.</span></span> <span data-ttu-id="9b1fd-197">特定のオーダー残に関する詳細情報を表示するには、そのオーダー残の行を選択してから、**詳細** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-197">To view even more information about a specific backorder, select the row for it, and then select the **More** link.</span></span>

## <a name="individual-shipping-container-tracking"></a><span data-ttu-id="9b1fd-198">個別出荷コンテナー トラッキング</span><span class="sxs-lookup"><span data-stu-id="9b1fd-198">Individual shipping container tracking</span></span>

<span data-ttu-id="9b1fd-199">**個別出荷コンテナー トラッキング** の照会では、出荷コンテナーを検索してから、そのコンテナー内のすべての航海行を識別できるフィルターを提供します。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-199">The **Individual shipping container tracking** inquiry provides a filter that lets you find a shipping container and then identify all the voyage lines in that container.</span></span>

<span data-ttu-id="9b1fd-200">この紹介を開くには、**陸揚原価 \> 照会 \> 追跡 \> 個別出荷コンテナー トラッキング** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-200">To open this inquiry, go to **Landed cost \> Inquiries \> Tracking \> Individual shipping container tracking**.</span></span>

## <a name="multiple-shipping-container-tracking"></a><span data-ttu-id="9b1fd-201">複数出荷コンテナー トラッキング</span><span class="sxs-lookup"><span data-stu-id="9b1fd-201">Multiple shipping container tracking</span></span>

<span data-ttu-id="9b1fd-202">**複数出荷コンテナー トラッキング** の照会では、出荷コンテナーのコレクションを検索してから、それらのコンテナー内のすべての航海行を識別できるフィルターを提供します。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-202">The **Multiple shipping container tracking** inquiry provides a filter that lets you find a collection of shipping containers and then identify all the voyage lines in those containers.</span></span>

<span data-ttu-id="9b1fd-203">この紹介を開くには、**陸揚原価 \> 照会 \> 追跡 \> 複数出荷コンテナー トラッキング** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9b1fd-203">To open this inquiry, go to **Landed cost \> Inquiries \> Tracking \> Multiple shipping container tracking**.</span></span>
