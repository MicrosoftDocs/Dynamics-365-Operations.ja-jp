---
title: 在庫棚卸の理由コード
description: このトピックでは、棚卸タスクに理由コードを設定および適用する方法について説明します。
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f4332432ad73861cd9b6b6452685d3175ace56b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "320837"
---
# <a name="reason-codes-for-inventory-counting"></a><span data-ttu-id="b356f-103">在庫棚卸の理由コード</span><span class="sxs-lookup"><span data-stu-id="b356f-103">Reason codes for inventory counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b356f-104">理由コードにより、棚卸プロセスおよびそのプロセス中に発生する任意の不一致の結果を分析できます。</span><span class="sxs-lookup"><span data-stu-id="b356f-104">Reason codes let you analyze the results of a counting process and any discrepancies that occur during that process.</span></span> <span data-ttu-id="b356f-105">パレットの破損または在庫サンプルに基づく在庫調整などの、棚卸を行うための理由を指定できます。</span><span class="sxs-lookup"><span data-stu-id="b356f-105">You can specify the reason for doing the count, such as a broken pallet or a stock adjustment that is based on inventory samples.</span></span>

## <a name="recommendation"></a><span data-ttu-id="b356f-106">推奨事項</span><span class="sxs-lookup"><span data-stu-id="b356f-106">Recommendation</span></span>

<span data-ttu-id="b356f-107">システムを設定する前に、理由コードを操作するための戦略を定義することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b356f-107">Before you set up the system, we recommend that you define a strategy for working with reason codes.</span></span> <span data-ttu-id="b356f-108">たとえば、次の質問に回答してください。</span><span class="sxs-lookup"><span data-stu-id="b356f-108">For example, try to answer the following questions:</span></span>

- <span data-ttu-id="b356f-109">理由コードは倉庫で必須ですか。</span><span class="sxs-lookup"><span data-stu-id="b356f-109">Should reason codes be mandatory on warehouses?</span></span>
- <span data-ttu-id="b356f-110">理由コードは一部の品目に必須またはオプションですか。</span><span class="sxs-lookup"><span data-stu-id="b356f-110">Should reason codes be mandatory or optional on some items?</span></span>
- <span data-ttu-id="b356f-111">理由コードがいくつ必要ですか。</span><span class="sxs-lookup"><span data-stu-id="b356f-111">How many reason codes do you require?</span></span>
- <span data-ttu-id="b356f-112">バーコード スキャナーのユーザーはどの理由コードを使用する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="b356f-112">How should users of barcode scanners use reason codes?</span></span> <span data-ttu-id="b356f-113">理由コードは事前に選択された、必須、または編集不可能のどれであるべきですか。</span><span class="sxs-lookup"><span data-stu-id="b356f-113">Should the reason codes be preselected, mandatory, or not editable?</span></span>
- <span data-ttu-id="b356f-114">倉庫作業者にはモバイル スキャナーでさまざまな理由コード動作が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="b356f-114">Do warehouse workers require different reason code behavior on mobile scanners?</span></span> <span data-ttu-id="b356f-115">答えがはいの場合は、複数のメニュー項目を作成し、さまざまな人々に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="b356f-115">If the answer is yes, you can create more menu items and assign them to different people.</span></span>

## <a name="where-reason-codes-apply"></a><span data-ttu-id="b356f-116">理由コードが適用される場所</span><span class="sxs-lookup"><span data-stu-id="b356f-116">Where reason codes apply</span></span>

<span data-ttu-id="b356f-117">複数の理由コード ポリシーを作成でき、各理由コード ポリシーは 2 つの棚卸の理由コード ポリシーを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="b356f-117">You can create multiple reason code policies, and each reason code policy can have two counting reason code policies.</span></span> <span data-ttu-id="b356f-118">倉庫レベルまたは品目レベルで、棚卸の理由コード ポリシーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b356f-118">The counting reason code policies can be used at the warehouse level or the item level.</span></span>

## <a name="set-up-reason-code-policies"></a><span data-ttu-id="b356f-119">理由コード ポリシーの設定</span><span class="sxs-lookup"><span data-stu-id="b356f-119">Set up reason code policies</span></span>

1. <span data-ttu-id="b356f-120">**在庫管理** \> **設定** \> **在庫** \> **棚卸の理由コード ポリシー** の順に選択し、新しい理由コード ポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="b356f-120">Select **Inventory management** \> **Setup** \> **Inventory** \> **Counting reason code policies**, and create a new reason code policy.</span></span>
2. <span data-ttu-id="b356f-121">**棚卸の理由コード ポリシー** フィールドで、**必須** または **オプション** のいずれかを選択し、次の棚卸仕訳帳のうちの 1 つで理由コードの選択がオプションまたは必須アクションであるべきかを指定します。</span><span class="sxs-lookup"><span data-stu-id="b356f-121">In the **Counting reason code type** field, select either **Mandatory** or **Optional** to specify whether selection of a reason code should be an optional or mandatory action in one of the following counting journals:</span></span>

    - <span data-ttu-id="b356f-122">循環棚卸 (モバイル デバイス)</span><span class="sxs-lookup"><span data-stu-id="b356f-122">Cycle Count (mobile device)</span></span>
    - <span data-ttu-id="b356f-123">スポット棚卸 (モバイル デバイス)</span><span class="sxs-lookup"><span data-stu-id="b356f-123">Spot Count (mobile device)</span></span>
    - <span data-ttu-id="b356f-124">しきい値棚卸 (モバイル デバイス)</span><span class="sxs-lookup"><span data-stu-id="b356f-124">Threshold Count (mobile device)</span></span>
    - <span data-ttu-id="b356f-125">調整内 (モバイル デバイス)</span><span class="sxs-lookup"><span data-stu-id="b356f-125">Adjustment In (mobile device)</span></span>
    - <span data-ttu-id="b356f-126">調整外 (モバイル デバイス)</span><span class="sxs-lookup"><span data-stu-id="b356f-126">Adjustment Out (mobile device)</span></span>
    - <span data-ttu-id="b356f-127">棚卸仕訳帳 (リッチ クライアント)</span><span class="sxs-lookup"><span data-stu-id="b356f-127">Counting Journal (rich client)</span></span>

<span data-ttu-id="b356f-128">個々の倉庫および製品に対して、理由コードを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="b356f-128">You can also set up reason codes for individual warehouses and for products.</span></span> <span data-ttu-id="b356f-129">製品の理由コードの設定では、倉庫の設定を無視できます。</span><span class="sxs-lookup"><span data-stu-id="b356f-129">The reason code setup for products can disregard the setup for warehouses.</span></span>

## <a name="mandatory-reason-codes"></a><span data-ttu-id="b356f-130">必須の理由コード</span><span class="sxs-lookup"><span data-stu-id="b356f-130">Mandatory reason codes</span></span>

<span data-ttu-id="b356f-131">**必須** パラメーターが、倉庫または品目の理由コードのコンフィギュレーションで設定されている場合、理由コードが提供されるまで棚卸仕訳帳を完了し閉じることはできません。</span><span class="sxs-lookup"><span data-stu-id="b356f-131">If the **Mandatory** parameter is set in the configuration of reason codes for warehouses or items, the counting journal can't be completed and closed until a reason code is provided.</span></span>

### <a name="set-up-reason-codes-for-warehouses"></a><span data-ttu-id="b356f-132">倉庫の理由コードの設定</span><span class="sxs-lookup"><span data-stu-id="b356f-132">Set up reason codes for warehouses</span></span>

1. <span data-ttu-id="b356f-133">**在庫管理** \> **設定** \> **在庫詳細** \> **倉庫** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b356f-133">Select **Inventory Management** \> **Setup** \> **Inventory breakdown** \> **Warehouses**.</span></span>
2. <span data-ttu-id="b356f-134">**棚卸理由コード ポリシー** フィールドの **倉庫** タブで、次のオプションのいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="b356f-134">On the **Warehouse** tab, in the **Counting reason code policy** field, select one of the following options:</span></span>

    - <span data-ttu-id="b356f-135">**空白** – 棚卸仕訳帳が製品に対して必須かどうかを決定するために、品目に対して設定されるパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="b356f-135">**Blank** – The parameter that is set up for the item is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="b356f-136">**必須** – 倉庫の棚卸仕訳帳では、理由コードは常に必要です。</span><span class="sxs-lookup"><span data-stu-id="b356f-136">**Mandatory** – A reason code is always required on counting journals for the warehouse.</span></span>
    - <span data-ttu-id="b356f-137">**オプション** – 倉庫の棚卸仕訳帳では、理由コードは必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="b356f-137">**Optional** – A reason code isn't required on counting journals for the warehouse.</span></span>

### <a name="set-up-reason-codes-for-products"></a><span data-ttu-id="b356f-138">製品の理由コードの設定</span><span class="sxs-lookup"><span data-stu-id="b356f-138">Set up reason codes for products</span></span>

1. <span data-ttu-id="b356f-139">**製品情報管理** \> **製品** \> **リリースされた製品** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b356f-139">Select **Product information management** \> **Products** \> **Released products**.</span></span>
2. <span data-ttu-id="b356f-140"> *\*倉庫** タブで *\*棚卸理由コード ポリシー** を選択し、次に以下のオプションのいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="b356f-140">On the **Product** tab, select **Counting reason code policy**, and then select one of the following options:</span></span>

    - <span data-ttu-id="b356f-141">**空白** – 棚卸仕訳帳が製品に対して必須かどうかを決定するために、倉庫に対して設定されるパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="b356f-141">**Blank** – The parameter that is set up for the warehouse is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="b356f-142">**必須** – 製品の棚卸仕訳帳では、理由コードは常に必要です。</span><span class="sxs-lookup"><span data-stu-id="b356f-142">**Mandatory** – A reason code is always required on counting journals for the product.</span></span> <span data-ttu-id="b356f-143">この設定は、倉庫レベルで任意の理由コード設定を上書きします。</span><span class="sxs-lookup"><span data-stu-id="b356f-143">This setting overrides any reason code setting at the warehouse level.</span></span>
    - <span data-ttu-id="b356f-144">**オプション** – 製品の棚卸仕訳帳では、理由コードは必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="b356f-144">**Optional** – A reason code isn't required on counting journals for the product.</span></span> <span data-ttu-id="b356f-145">この設定は、倉庫レベルで任意の理由コード設定を上書きします。</span><span class="sxs-lookup"><span data-stu-id="b356f-145">This setting overrides any reason code setting at the warehouse level.</span></span>

### <a name="use-reason-codes-in-counting-journals"></a><span data-ttu-id="b356f-146">棚卸仕訳帳で理由コードを使用する</span><span class="sxs-lookup"><span data-stu-id="b356f-146">Use reason codes in counting journals</span></span>

<span data-ttu-id="b356f-147">棚卸仕訳帳では、次のタイプの棚卸の理由コードを追加できます。</span><span class="sxs-lookup"><span data-stu-id="b356f-147">In a counting journal, you can add reason codes for counts of the following types:</span></span>

- <span data-ttu-id="b356f-148">循環棚卸</span><span class="sxs-lookup"><span data-stu-id="b356f-148">Cycle Count</span></span>
- <span data-ttu-id="b356f-149">スポット棚卸</span><span class="sxs-lookup"><span data-stu-id="b356f-149">Spot Count</span></span>
- <span data-ttu-id="b356f-150">しきい値棚卸</span><span class="sxs-lookup"><span data-stu-id="b356f-150">Threshold Count</span></span>
- <span data-ttu-id="b356f-151">調整内</span><span class="sxs-lookup"><span data-stu-id="b356f-151">Adjustment In</span></span>
- <span data-ttu-id="b356f-152">調整外</span><span class="sxs-lookup"><span data-stu-id="b356f-152">Adjustment Out</span></span>

<span data-ttu-id="b356f-153">理由コードは、**棚卸仕訳帳** タイプの棚卸仕訳帳の仕訳帳明細行に追加されます。</span><span class="sxs-lookup"><span data-stu-id="b356f-153">Reason codes are added to the journal lines in counting journals of the **Counting journal** type.</span></span>

1. <span data-ttu-id="b356f-154">**在庫管理** \> **仕訳入力** \> **品目棚卸** \> **棚卸** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b356f-154">Select **Inventory management** \> **Journal entries** \> **Item counting** \> **Counting**.</span></span>
2. <span data-ttu-id="b356f-155">**棚卸理由コード** フィールドの棚卸仕訳帳の明細行の詳細で、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b356f-155">In the line details of the counting journal, in the **Counting reason code** field, select an option.</span></span>

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a><span data-ttu-id="b356f-156">理由コードにより記録される棚卸履歴を表示します。</span><span class="sxs-lookup"><span data-stu-id="b356f-156">View the counting history as it's recorded by reason codes</span></span>

- <span data-ttu-id="b356f-157">**在庫管理** \> **照会およびレポート** \> **棚卸履歴** の順に選択し、次に **棚卸理由コード** フィールドで、理由コードを使用して記録された棚卸履歴を表示します。</span><span class="sxs-lookup"><span data-stu-id="b356f-157">Select **Inventory management** \> **Inquiries and reports** \> **Counting history**, and then, in the **Counting reason code** field, view the counting history that has been recorded through a reason code.</span></span>

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a><span data-ttu-id="b356f-158">数量調整に理由コードを使用する</span><span class="sxs-lookup"><span data-stu-id="b356f-158">Use a reason code for a quantity adjustment</span></span>

1. <span data-ttu-id="b356f-159">**手持在庫** ページで、**数量調整** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b356f-159">On the **On-hand inventory** page, select **Adjust quantity**.</span></span> <span data-ttu-id="b356f-160">いくつかの方法で **手持在庫** ページを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="b356f-160">You can open the **On-hand inventory** page in several ways.</span></span> <span data-ttu-id="b356f-161">たとえば、**在庫管理** \> **照会およびレポート** \> **手持在庫** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b356f-161">For example, select **Inventory management** \> **Inquiries and reports** \> **On-hand inventory**.</span></span>
2. <span data-ttu-id="b356f-162">**数量調整** を選択し、次に **棚卸理由コード** フィールドで、理由コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="b356f-162">Select **Adjust quantity**, and then, in the **Counting reason code** field, select a reason code.</span></span>

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a><span data-ttu-id="b356f-163">モバイル デバイス メニュー項目の理由コードをコンフィギュレーションします</span><span class="sxs-lookup"><span data-stu-id="b356f-163">Configure reason codes for mobile device menu items</span></span>

<span data-ttu-id="b356f-164">モバイル デバイス メニュー項目の棚卸の任意のタイプに対する理由コードをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="b356f-164">You can configure reason codes for any type of count on a mobile device menu item.</span></span> <span data-ttu-id="b356f-165">モバイル デバイス メニュー項目のコンフィギュレーションには、次の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b356f-165">The configuration of the mobile device menu item includes the following information:</span></span>

- <span data-ttu-id="b356f-166">棚卸の際に、モバイル デバイスの作業者に理由コードが表示されているかどうか。</span><span class="sxs-lookup"><span data-stu-id="b356f-166">Whether the reason code is shown to the mobile device worker during counting.</span></span>
- <span data-ttu-id="b356f-167">既定の理由コードがモバイル デバイス メニュー項目に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b356f-167">The default reason code that is shown on a mobile device menu item.</span></span>
- <span data-ttu-id="b356f-168">ユーザーが理由コードを編集できるかどうか。</span><span class="sxs-lookup"><span data-stu-id="b356f-168">Whether the user can edit the reason code.</span></span>

### <a name="set-up-reason-codes-on-a-mobile-device"></a><span data-ttu-id="b356f-169">モバイル デバイスで理由コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="b356f-169">Set up reason codes on a mobile device</span></span>

1. <span data-ttu-id="b356f-170">**倉庫管理** \> **設定** \> **モバイル デバイス** \> **モバイル デバイスのメニュー品目** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b356f-170">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="b356f-171">**循環棚卸** タブで、**循環棚卸** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b356f-171">On the **Cycle count** tab, select **Cycle counting**.</span></span>
3. <span data-ttu-id="b356f-172">**既定の棚卸理由コード** フィールドで、棚卸がモバイル デバイス メニュー項目を使用して行われるときに記録されるべき、既定の理由コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="b356f-172">In the **Default counting reason code** field, set the default reason code that should be recorded when counting is done by using the mobile device menu item.</span></span>
4. <span data-ttu-id="b356f-173">**棚卸理由コードを表示する** フィールドで、**明細行** を選択し、各差異が記録された後に、理由コードを表示します。</span><span class="sxs-lookup"><span data-stu-id="b356f-173">In the **Display counting reason code** field, select **Line** to show the reason code after each variance is recorded.</span></span> <span data-ttu-id="b356f-174">または、理由コードを表示する必要がない場合、**非表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b356f-174">Alternatively, select **Hide** if the reason code shouldn't be shown.</span></span>
5. <span data-ttu-id="b356f-175">**棚卸理由コードを編集する** オプションを **はい** または **いいえ** のいずれかに設定します。</span><span class="sxs-lookup"><span data-stu-id="b356f-175">Set the **Edit counting reason code** option to either **Yes** or **No**.</span></span> <span data-ttu-id="b356f-176">このオプションを **はい** に設定した場合、作業者は、棚卸中にモバイル デバイスで表示される際に理由コードを編集できます。</span><span class="sxs-lookup"><span data-stu-id="b356f-176">If you set this option to **Yes**, the worker can edit the reason code when it's shown on the mobile device during counting.</span></span>

> [!NOTE]
> <span data-ttu-id="b356f-177">棚卸の実行時に任意のモバイル デバイス メニュー項目で **循環棚卸** ボタンを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b356f-177">The **Cycle counting** button can be enabled on any mobile device menu item where counting can be done.</span></span> <span data-ttu-id="b356f-178">例には、スポット棚卸、ユーザー主導作業、およびシステム主導作業のメニュー項目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b356f-178">Example include the menu items for spot counts, user-directed work, and system-directed work.</span></span>

## <a name="cycle-count-approvals"></a><span data-ttu-id="b356f-179">循環棚卸の承認</span><span class="sxs-lookup"><span data-stu-id="b356f-179">Cycle count approvals</span></span>

<span data-ttu-id="b356f-180">棚卸が承認される前に、ユーザーは、棚卸に関連付けられている理由コードを変更できます。</span><span class="sxs-lookup"><span data-stu-id="b356f-180">Before a count is approved, the user can change the reason code that is associated with the count.</span></span> <span data-ttu-id="b356f-181">棚卸が承認されると、棚卸仕訳帳明細行に理由コードが入力されます。</span><span class="sxs-lookup"><span data-stu-id="b356f-181">When the count is approved, the reason code is entered on the counting journal lines.</span></span>

### <a name="modify-cycle-count-approvals"></a><span data-ttu-id="b356f-182">循環棚卸の承認の変更</span><span class="sxs-lookup"><span data-stu-id="b356f-182">Modify cycle count approvals</span></span>

1. <span data-ttu-id="b356f-183">**倉庫管理** \> **循環棚卸** \> **循環棚卸作業が検討保留** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b356f-183">Select **Warehouse management** \> **Cycle counting** \> **Cycle count work pending review**.</span></span>
2. <span data-ttu-id="b356f-184">**循環棚卸** を選択し、次に **理由コード** フィールドで、新しい理由コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="b356f-184">Select **Cycle counting**, and then, in the **Reason code** field, select a new reason code.</span></span>

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a><span data-ttu-id="b356f-185">調整内および調整外のモバイル デバイス メニュー項目を変更します。</span><span class="sxs-lookup"><span data-stu-id="b356f-185">Modify the mobile device menu item for Adjustment in and Adjustment out</span></span>

1. <span data-ttu-id="b356f-186">**倉庫管理** \> **設定** \> **モバイル デバイス** \> **モバイル デバイス メニュー項目** の順に選択し、次に **調整内と調整外** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b356f-186">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**, and then select **Adjustment in and out**.</span></span>
2. <span data-ttu-id="b356f-187">**既存の作業を使用** オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b356f-187">Set the **Use existing work** option to **No**.</span></span>
3. <span data-ttu-id="b356f-188">**作業作成プロセス** フィールドで、**調整内** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b356f-188">In the **Work creation process** field, select **Adjustment in**.</span></span>

<span data-ttu-id="b356f-189">作業作成プロセス中に **調整内** または **調整外** が選択されている場合、次のフィールドがモバイル デバイス メニュー品目に追加されます。。</span><span class="sxs-lookup"><span data-stu-id="b356f-189">The following fields will be added to the mobile device menu item when **Adjustment in** or **Adjustment out** is selected during the work creation process:</span></span>

- <span data-ttu-id="b356f-190">既定の棚卸理由コード</span><span class="sxs-lookup"><span data-stu-id="b356f-190">Default counting reason code</span></span>
- <span data-ttu-id="b356f-191">棚卸理由コードを表示する</span><span class="sxs-lookup"><span data-stu-id="b356f-191">Display counting reason code</span></span>
- <span data-ttu-id="b356f-192">棚卸理由コードを編集する</span><span class="sxs-lookup"><span data-stu-id="b356f-192">Edit counting reason code</span></span>
