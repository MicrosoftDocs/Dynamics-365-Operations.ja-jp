---
title: 請求金額の自動配賦
description: Microsoft Dynamics 365 Supply Chain Management の請求機能を使用すると、発注書または販売注文に請求金額を自動的に割り当てることができます。
author: dasani-madipalli
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e8d65cc1f946f921523607eff850b29f9ff9bf1
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910164"
---
# <a name="automatic-allocation-of-charges"></a><span data-ttu-id="41d18-103">請求金額の自動配賦</span><span class="sxs-lookup"><span data-stu-id="41d18-103">Automatic allocation of charges</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41d18-104">担当している顧客または販売している品目に基づいて、特定の追加請求金額を適用することができます。</span><span class="sxs-lookup"><span data-stu-id="41d18-104">Based on the customer that you're working with or the item that you're selling, you might want to apply specific additional charges.</span></span> <span data-ttu-id="41d18-105">Microsoft Dynamics 365 Supply Chain Management の *請求* 機能を使用すると、発注書または販売注文に請求金額を自動的に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="41d18-105">The *charges* feature in Microsoft Dynamics 365 Supply Chain Management helps you automatically allocate charges to purchase orders or sales orders.</span></span>

<span data-ttu-id="41d18-106">自動請求と呼ばれる自動請求は、販売注文または発注書の作成時に自動的に適用されます。</span><span class="sxs-lookup"><span data-stu-id="41d18-106">Automatic charges, or auto charges, are automatically applied when you create a sales order or a purchase order.</span></span> <span data-ttu-id="41d18-107">特定の仕入先、顧客、仕入先のグループ、または品目に自動請求を定義できます。</span><span class="sxs-lookup"><span data-stu-id="41d18-107">You can define auto charges for specific vendors, customers, groups of vendors, or items.</span></span> <span data-ttu-id="41d18-108">また、すべての仕入先、顧客、または品目に適用する自動請求を定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="41d18-108">You can also define auto charges that apply to all vendors, customers, or items.</span></span>

## <a name="set-up-charges-codes"></a><span data-ttu-id="41d18-109">諸費用コードの設定</span><span class="sxs-lookup"><span data-stu-id="41d18-109">Set up charges codes</span></span>

<span data-ttu-id="41d18-110">請求金額を割り当てるには、最初に諸費用コードを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="41d18-110">To allocate charges, you must first define charges codes.</span></span>

1. <span data-ttu-id="41d18-111">次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="41d18-111">Follow one of these steps:</span></span>

    - <span data-ttu-id="41d18-112">発注書の場合: **買掛金勘定 \> 諸費用の設定 \> 諸費用コード** に移動します。</span><span class="sxs-lookup"><span data-stu-id="41d18-112">For purchase orders: Go to **Accounts payable \> Charges setup \> Charges code**.</span></span>
    - <span data-ttu-id="41d18-113">販売注文の場合: **売掛金勘定 \> 諸費用の設定 \> 諸費用コード** に移動します。</span><span class="sxs-lookup"><span data-stu-id="41d18-113">For sales orders: Go to **Accounts receivable \> Charges setup \> Charges code**.</span></span>

1. <span data-ttu-id="41d18-114">アクション パネルにて **新規** を選択して諸費用コードを作成します。</span><span class="sxs-lookup"><span data-stu-id="41d18-114">On the Action Pane, select **New** to create a charges code.</span></span>
1. <span data-ttu-id="41d18-115">新規レコードのヘッダーで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="41d18-115">In the header of the new record, set the following fields:</span></span>

    - <span data-ttu-id="41d18-116">**諸費用コード** – 諸費用のコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="41d18-116">**Charges code** – Enter a code for the charges.</span></span>
    - <span data-ttu-id="41d18-117">**説明** – 諸費用の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="41d18-117">**Description** – Enter a description of the charges.</span></span>
    - <span data-ttu-id="41d18-118">**品目消費税グループ** – 品目消費税グループを選択します (該当する場合)。</span><span class="sxs-lookup"><span data-stu-id="41d18-118">**Item sales tax group** – Select an item sales tax group, if applicable.</span></span>
    - <span data-ttu-id="41d18-119">**比例配分** – 請求金額を比例配分にする場合は、このオプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="41d18-119">**Prorate** – Set this option to *Yes* if you want to prorate your charges.</span></span> <span data-ttu-id="41d18-120">このオプションは、販売注文に対してのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="41d18-120">This option is available only for sales orders.</span></span>
    - <span data-ttu-id="41d18-121">**最大金額** – 諸費用コードに引き当てる最大金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="41d18-121">**Maximum amount** – Enter the maximum amount that is allowed for the charges code.</span></span> <span data-ttu-id="41d18-122">仕入先請求書の雑費の検証にはこのフィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="41d18-122">This field is used to validate charges for vendor invoices.</span></span> <span data-ttu-id="41d18-123">発注書に対してのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="41d18-123">It's available only for purchase orders.</span></span>

        > [!NOTE]
        > <span data-ttu-id="41d18-124">発注書の請求金額を検証する機能を有効にするには、**買掛金勘定 \> 設定 \> 買掛金勘定パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="41d18-124">To turn on the functionality for validating charges for purchase orders, go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span> <span data-ttu-id="41d18-125">**請求書の検証** セクションの **請求書の検証** クイック タブで、**請求書照合検証の有効化** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="41d18-125">On the **Invoice validation** FastTab, in the **Invoice validation** section, set the **Enable invoice matching validation** option to *Yes*.</span></span>

1. <span data-ttu-id="41d18-126">**転記** クイック タブには、**借方** セクションと **貸方** セクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="41d18-126">The **Posting** FastTab includes **Debit** and **Credit** sections.</span></span> <span data-ttu-id="41d18-127">請求金額の転記先となる元帳に応じて、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="41d18-127">Set the following fields, depending on the ledger that you want to post the charges to:</span></span>

    - <span data-ttu-id="41d18-128">**タイプ** – 転記する勘定のタイプ (*元帳*、*顧客*、または *品目*) を選択します。</span><span class="sxs-lookup"><span data-stu-id="41d18-128">**Type** – Select the type of account that you're posting to (*Ledger*, *Customer*, or *Item*).</span></span>
    - <span data-ttu-id="41d18-129">**転記** – 作成する転記のタイプ (*ブローカー手数料* または *顧客決済* など) を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="41d18-129">**Posting** – Select the type of postings to create (such as *Broker fee* or *Customer settlement*).</span></span>
    - <span data-ttu-id="41d18-130">**勘定** – 諸費用を転記する勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="41d18-130">**Account** – Select the account to post the charge for.</span></span>

1. <span data-ttu-id="41d18-131">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="41d18-131">On the Action Pane, select **Save**.</span></span>

## <a name="create-charge-groups"></a><span data-ttu-id="41d18-132">請求金額グループの作成</span><span class="sxs-lookup"><span data-stu-id="41d18-132">Create charge groups</span></span>

<span data-ttu-id="41d18-133">請求金額グループは、顧客または仕入先のグループに対して、特定の諸費用を自動的に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="41d18-133">Charge groups automatically allocate specific charges to a group of customers or vendors.</span></span> <span data-ttu-id="41d18-134">次のサブセクションでは、請求金額グループを作成および割り当てる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="41d18-134">The following subsections describe how to create and assign these charge groups.</span></span>

### <a name="charge-groups-for-purchase-orders"></a><span data-ttu-id="41d18-135">発注書の請求金額グループ</span><span class="sxs-lookup"><span data-stu-id="41d18-135">Charge groups for purchase orders</span></span>

<span data-ttu-id="41d18-136">発注書の請求金額グループを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="41d18-136">To create charge groups for purchase orders, follow these steps.</span></span>

1. <span data-ttu-id="41d18-137">**買掛金勘定 \> 諸費用の設定 \> 仕入先請求金額グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="41d18-137">Go to **Accounts payable \> Charges setup \> Vendor charges group**.</span></span>
1. <span data-ttu-id="41d18-138">アクション ウィンドウで、**新規** を選択して行をグリッドに追加し、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="41d18-138">On the Action Pane, select **New** to add a row to the grid, and then set the following fields:</span></span>

    - <span data-ttu-id="41d18-139">**請求金額グループ** – 請求金額グループの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="41d18-139">**Charges group** – Enter the name of the charge group.</span></span>
    - <span data-ttu-id="41d18-140">**説明** – 請求金額グループの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="41d18-140">**Description** – Enter a description of the charge group.</span></span>

1. <span data-ttu-id="41d18-141">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="41d18-141">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="41d18-142">**買掛金勘定 \> 仕入先 \> すべての仕入先** に移動して、既存の仕入先を開くか、新しい仕入先を作成します。</span><span class="sxs-lookup"><span data-stu-id="41d18-142">Go to **Accounts payable \> Vendors \> All vendors**, and either open an existing vendor or create a new vendor.</span></span>
1. <span data-ttu-id="41d18-143">**発注書** セクションにある **発注書の既定値** クイック タブで、**請求金額グループ** フィールドを作成した請求金額グループに設定します。</span><span class="sxs-lookup"><span data-stu-id="41d18-143">On the **Purchase order defaults** FastTab, in the **Purchase order** section, set the **Charges group** field to the charge group that you just created.</span></span>

### <a name="charge-groups-for-sales-orders"></a><span data-ttu-id="41d18-144">販売注文の請求金額グループ</span><span class="sxs-lookup"><span data-stu-id="41d18-144">Charge groups for sales orders</span></span>

<span data-ttu-id="41d18-145">販売注文の請求金額グループを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="41d18-145">To create charge groups for sales orders, follow these steps.</span></span>

1. <span data-ttu-id="41d18-146">**売掛金勘定 \> 諸費用の設定 \> 顧客請求金額グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="41d18-146">Go to **Accounts receivable \> Charges setup \> Customer charge groups**.</span></span>
1. <span data-ttu-id="41d18-147">アクション ウィンドウで、**新規** を選択して行をグリッドに追加し、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="41d18-147">On the Action Pane, select **New** to add a row to the grid, and then set the following fields:</span></span>

    - <span data-ttu-id="41d18-148">**請求金額グループ** – 請求金額グループの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="41d18-148">**Charges group** – Enter the name of the charge group.</span></span>
    - <span data-ttu-id="41d18-149">**説明** – 請求金額グループの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="41d18-149">**Description** – Enter a description of the charge group.</span></span>

1. <span data-ttu-id="41d18-150">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="41d18-150">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="41d18-151">**売掛金勘定 \> 顧客 \> すべての顧客** に移動し、既存の顧客を開くか、新しい顧客を作成します。</span><span class="sxs-lookup"><span data-stu-id="41d18-151">Go to **Accounts receivable \> Customers \> All customers**, and either open an existing customer or create a new customer.</span></span>
1. <span data-ttu-id="41d18-152">**販売注文** セクションにある **発注書の既定値** クイック タブで、**請求金額グループ** フィールドを作成した請求金額グループに設定します。</span><span class="sxs-lookup"><span data-stu-id="41d18-152">On the **Purchase order defaults** FastTab, in the **Sales order** section, set the **Charges group** field to the charge group that you just created.</span></span>

## <a name="define-auto-charges"></a><span data-ttu-id="41d18-153">自動請求を定義する</span><span class="sxs-lookup"><span data-stu-id="41d18-153">Define auto charges</span></span>

<span data-ttu-id="41d18-154">諸費用コードが設定されたら、次の手順に従って自動雑費を定義します。</span><span class="sxs-lookup"><span data-stu-id="41d18-154">After your charges codes are set up, follow these steps to define the auto charges.</span></span>

1. <span data-ttu-id="41d18-155">次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="41d18-155">Follow one of these steps:</span></span>

    - <span data-ttu-id="41d18-156">発注書の場合: **調達 \> 設定 \> 諸費用 \> 自動請求** に移動します。</span><span class="sxs-lookup"><span data-stu-id="41d18-156">For purchase orders: Go to **Procurement and sourcing \> Setup \> Charges \> Automatic charges**.</span></span>
    - <span data-ttu-id="41d18-157">販売注文の場合: **売掛金勘定 \> 設定 \> 諸費用の設定 \> 自動請求** に移動します。</span><span class="sxs-lookup"><span data-stu-id="41d18-157">For sales orders: Go to **Accounts receivable \> Setup \> Charges setup \> Auto charges**.</span></span>

1. <span data-ttu-id="41d18-158">リスト ウィンドウの **レベル** フィールドで、自動請求が適用されるレベルを選択します。</span><span class="sxs-lookup"><span data-stu-id="41d18-158">In the list pane, in the **Level** field, select the level where your auto charge applies:</span></span>

    - <span data-ttu-id="41d18-159">*メイン* – 注文ヘッダーに請求を適用します。</span><span class="sxs-lookup"><span data-stu-id="41d18-159">*Main* – Apply charges to the order header.</span></span>
    - <span data-ttu-id="41d18-160">*明細行* – 注文明細行に請求を適用します。</span><span class="sxs-lookup"><span data-stu-id="41d18-160">*Line* – Apply charges to the order lines.</span></span>

1. <span data-ttu-id="41d18-161">既存の自動請求を選択して編集するか、**新規** を選択して新しい自動請求を定義します。</span><span class="sxs-lookup"><span data-stu-id="41d18-161">Select an existing auto charge to edit it, or select **New** to define a new auto charge.</span></span>
1. <span data-ttu-id="41d18-162">**アカウント コード** 一覧で、次のいずれかの値を選択して、影響を受ける勘定の範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="41d18-162">In the **Account code** list, select one of the following values to specify the scope of accounts that will be affected:</span></span>

    - <span data-ttu-id="41d18-163">*テーブル* – 特定の顧客または仕入先に請求を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="41d18-163">*Table* – Assign charges to a specific customer or vendor.</span></span>
    - <span data-ttu-id="41d18-164">*グループ* – 雑費グループに請求を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="41d18-164">*Group* – Assign charges to a miscellaneous charges group.</span></span>
    - <span data-ttu-id="41d18-165">*すべて* – すべての顧客または仕入先に請求を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="41d18-165">*All* – Assign charges to all customers or vendors.</span></span>

1. <span data-ttu-id="41d18-166">**顧客関係** または **仕入先関係** フィールドで、**アカウント コード** フィールドを *テーブル* に設定する場合は、特定の顧客または仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="41d18-166">In the **Customer relation** or **Vendor relation** field, select a specific customer or vendor if you set the **Account code** field to *Table*.</span></span> <span data-ttu-id="41d18-167">**アカウント コード** フィールドを *グループ* に設定する場合は、顧客または仕入先の請求金額グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="41d18-167">If you set the **Account code** field to *Group*, select a customer or vendor charges group.</span></span>
1. <span data-ttu-id="41d18-168">**品目コード** フィールドで、次のいずれかの値を選択して、影響を受ける品目の範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="41d18-168">In the **Item code** field, select one of the following values to specify the scope of items that will be affected.</span></span> <span data-ttu-id="41d18-169">明細行レベルで自動請求を定義した場合にのみ品目コードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="41d18-169">You can select an item code only when you define auto charges at the line level.</span></span>

    - <span data-ttu-id="41d18-170">*テーブル* – 特定の品目に請求を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="41d18-170">*Table* – Assign charges to a specific item.</span></span>
    - <span data-ttu-id="41d18-171">*グループ* – 品目の請求グループに請求を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="41d18-171">*Group* – Assign charges to an item charges group.</span></span>
    - <span data-ttu-id="41d18-172">*すべて* – すべての品目に請求を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="41d18-172">*All* – Assign charges to all items.</span></span>

1. <span data-ttu-id="41d18-173">**商品関係** フィールドで、**品目コード** を *テーブル* に設定する場合は、特定の品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="41d18-173">In the **Item relation** field, select a specific item if you set the **Item code** field to *Table*.</span></span> <span data-ttu-id="41d18-174">**品目コード** フィールドを *グループ* に設定する場合は、品目請求金額グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="41d18-174">If you set the **Item code** field to *Group*, select an item charges group.</span></span>
1. <span data-ttu-id="41d18-175">**販売注文の場合のみ:** **荷渡方法コード** フィールドで、次のいずれかの値を選択して、影響を受ける荷渡方法モードの範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="41d18-175">**For sales orders only:** In the **Mode of delivery code** field, select one of the following values to specify the scope of delivery modes that will be affected:</span></span>

    - <span data-ttu-id="41d18-176">*テーブル* – 特定の荷渡方法に請求を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="41d18-176">*Table* – Assign charges to a specific mode of delivery.</span></span>
    - <span data-ttu-id="41d18-177">*グループ* – 荷渡方法グループに請求を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="41d18-177">*Group* – Assign charges to a mode of delivery group.</span></span>
    - <span data-ttu-id="41d18-178">*すべて* – すべての荷渡方法に請求を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="41d18-178">*All* – Assign charges to all modes of delivery.</span></span>

1. <span data-ttu-id="41d18-179">**販売注文のみの場合:** **荷渡方法の関係** フィールドで、**荷渡方法のコード** フィールドを *テーブル* に設定する場合は、特定の荷渡方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="41d18-179">**For sales orders only:** In the **Mode of delivery relation** field, select a specific mode of delivery if you set the **Mode of delivery code** field to *Table*.</span></span> <span data-ttu-id="41d18-180">**荷渡方法のコード** フィールドを *グループ* に設定する場合、荷渡方法のグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="41d18-180">If you set the **Mode of delivery code** field to *Group*, select a mode of delivery group.</span></span>
1. <span data-ttu-id="41d18-181">**明細行** クイック タブで、現在の自動請求の適用時に使用する請求と請求金額のレートを定義します。</span><span class="sxs-lookup"><span data-stu-id="41d18-181">On the **Lines** FastTab, define the charges and the charges rates that will be used when the current auto charge is applied.</span></span> <span data-ttu-id="41d18-182">このクイック タブのツール バーを使用して、必要な数だけ明細行を追加できます。</span><span class="sxs-lookup"><span data-stu-id="41d18-182">You can use the toolbar on this FastTab to add as many lines as you require.</span></span> <span data-ttu-id="41d18-183">各明細行で、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="41d18-183">For each line, set the following fields:</span></span>

    - <span data-ttu-id="41d18-184">**通貨** – 請求金額の計算に使用する通貨を選択します。</span><span class="sxs-lookup"><span data-stu-id="41d18-184">**Currency** – Select the currency that should be used to calculate the charge.</span></span>
    - <span data-ttu-id="41d18-185">**諸費用コード** – 請求金額のコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="41d18-185">**Charges code** – Select the code for the charge.</span></span>
    - <span data-ttu-id="41d18-186">**カテゴリ** – 次の値からいずれか 1 つを選択します。</span><span class="sxs-lookup"><span data-stu-id="41d18-186">**Category** – Select one of the following values:</span></span>

        - <span data-ttu-id="41d18-187">*固定金額* – 請求金額は、明細行の固定金額として入力します。</span><span class="sxs-lookup"><span data-stu-id="41d18-187">*Fixed* – The charge is entered as a fixed amount on the line.</span></span> <span data-ttu-id="41d18-188">固定された請求金額は、注文ヘッダーと注文明細行の両方を請求金額で使用できます。</span><span class="sxs-lookup"><span data-stu-id="41d18-188">Fixed charges can be used on charges both in the order header and on the order lines.</span></span>
        - <span data-ttu-id="41d18-189">*個数* – 請求金額は単位に基づきます。</span><span class="sxs-lookup"><span data-stu-id="41d18-189">*Pcs* – The charge is based on the unit.</span></span> <span data-ttu-id="41d18-190">これらの請求金額は、注文明細行でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="41d18-190">These charges can be used only on order lines.</span></span> <span data-ttu-id="41d18-191">注文の合計を計算すると表示されます。</span><span class="sxs-lookup"><span data-stu-id="41d18-191">They will appear when you calculate the order total.</span></span>
        - <span data-ttu-id="41d18-192">*割合* – 請求金額は、明細行の割合として入力します。</span><span class="sxs-lookup"><span data-stu-id="41d18-192">*Percent* – The charge is entered as a percentage on the line.</span></span> <span data-ttu-id="41d18-193">請求金額の割合は、注文ヘッダーと注文明細行の両方を請求金額で使用できます。</span><span class="sxs-lookup"><span data-stu-id="41d18-193">Percentage charges can be used on charges both in the order header and on the order lines.</span></span>
        - <span data-ttu-id="41d18-194">*会社間の割合* – 請求金額は、会社間発注書の明細行の割合として入力します。</span><span class="sxs-lookup"><span data-stu-id="41d18-194">*Intercompany percent* – The charge is entered as a percentage on the line for intercompany orders.</span></span> <span data-ttu-id="41d18-195">会社間の請求金額の割合は、注文明細行でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="41d18-195">Intercompany percentage charges can be used only on order lines.</span></span>
        - <span data-ttu-id="41d18-196">*外部* – 請求金額は、1 つ以上の出荷配送業者に関連付けられているサード パーティ サービスによって計算されます。</span><span class="sxs-lookup"><span data-stu-id="41d18-196">*External* – The charge is calculated by a third-party service that is associated with one or more shipping carriers.</span></span>

    - <span data-ttu-id="41d18-197">**請求金額の値** – 選択したカテゴリに基づいて請求金額の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="41d18-197">**Charges value** – Enter the charge value, based on the category that you selected.</span></span>
    - <span data-ttu-id="41d18-198">**請求金額通貨コード** – **通貨** フィールドで指定した通貨以外の通貨を使用する場合は、請求金額の通貨を指定します。</span><span class="sxs-lookup"><span data-stu-id="41d18-198">**Charges currency code** – Specify a currency for the charge if you want to use a currency other than the currency that you specified in the **Currency** field.</span></span> <span data-ttu-id="41d18-199">選択した諸費用コードの **借方タイプ** または **貸方タイプ** フィールドが、*勘定科目* または *品目* のいずれかに設定されている場合のみ、異なる通貨を使用できます。</span><span class="sxs-lookup"><span data-stu-id="41d18-199">You can use a different currency only if the **Debit type** or **Credit type** field is set to either *Ledger account* or *Item* for the selected charges code.</span></span>
    - <span data-ttu-id="41d18-200">**開始金額** – 自動請求を適用する開始金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="41d18-200">**From amount** – Specify a starting amount to apply the auto charge to.</span></span> <span data-ttu-id="41d18-201">このコンテキストでは、金額は注文の合計を示します。</span><span class="sxs-lookup"><span data-stu-id="41d18-201">In this context, the amount refers to the order total.</span></span>
    - <span data-ttu-id="41d18-202">**終了金額** – 自動請求を適用する終了金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="41d18-202">**To amount** – Specify the ending amount to apply the auto charge to.</span></span> <span data-ttu-id="41d18-203">このコンテキストでは、金額は注文の合計を示します。</span><span class="sxs-lookup"><span data-stu-id="41d18-203">In this context, the amount refers to the order total.</span></span>
    - <span data-ttu-id="41d18-204">**消費税グループ** – 消費税グループを指定します。</span><span class="sxs-lookup"><span data-stu-id="41d18-204">**Sales tax group** – Specify a sales tax group.</span></span>
    - <span data-ttu-id="41d18-205">**サイト** と **倉庫** – 特定のサイトと倉庫に対してのみに請求金額を適用する場合は、サイトと倉庫を指定します。</span><span class="sxs-lookup"><span data-stu-id="41d18-205">**Site** and **Warehouse** – Specify a site and warehouse if charges should be applied only for a specific site and warehouse.</span></span>
    - <span data-ttu-id="41d18-206">**保存** – チェック ボックスをオンにして請求完了後に請求トランザクションを保存すると、選択した顧客 ID に対して新しい請求書を作成するたびに請求が適用されるようになります。</span><span class="sxs-lookup"><span data-stu-id="41d18-206">**Keep** – Select this check box to keep the charges transactions after invoicing is completed, so that the charge will be applied every time that you create a new invoice for the selected customer account.</span></span>

1. <span data-ttu-id="41d18-207">**販売注文の場合のみ:** 階層化された請求金額を計算する場合は、[販売注文の階層化された請求金額](/dynamicsax-2012/appuser-itpro/about-tiered-charges-on-sales-orders) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="41d18-207">**For sales orders only:** If you want to calculate tiered charges, see [Tiered charges on sales orders](/dynamicsax-2012/appuser-itpro/about-tiered-charges-on-sales-orders) for information.</span></span>

## <a name="allocate-charges-from-the-header-to-a-line"></a><span data-ttu-id="41d18-208">ヘッダーから明細行に諸費用を配賦</span><span class="sxs-lookup"><span data-stu-id="41d18-208">Allocate charges from the header to a line</span></span>

<span data-ttu-id="41d18-209">次の手順では、ヘッダーレベルの諸費用を明細行に配賦する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="41d18-209">The following procedure shows how to allocate header-level charges to a line.</span></span> <span data-ttu-id="41d18-210">この手順を開始する前に、*固定金額* タイプのヘッダーレベルの請求金額と、その請求金額が適用される注文がすでに準備されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="41d18-210">Before you start this procedure, you should already have a header-level charge of the *fixed amount* type and an order where that charge is applied.</span></span> <span data-ttu-id="41d18-211">また、注文には少なくとも 1 つの明細書の品目が既に含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="41d18-211">Additionally, the order should already include at least one line item.</span></span>

1. <span data-ttu-id="41d18-212">発注書または請求書を開きます。</span><span class="sxs-lookup"><span data-stu-id="41d18-212">Open the purchase order or charge order.</span></span>
1. <span data-ttu-id="41d18-213">アクション ウィンドウで、次のいずれかのステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="41d18-213">On the Action Pane, follow one of these steps:</span></span>

    - <span data-ttu-id="41d18-214">発注書の場合: **購入** タブの **請求金額** グループで、**諸費用の配賦** を選択します。</span><span class="sxs-lookup"><span data-stu-id="41d18-214">For purchase orders: On the **Purchase** tab, in the **Charges** group, select **Allocate charges**.</span></span>
    - <span data-ttu-id="41d18-215">販売注文の場合: **販売** タブの **請求金額** グループで、**諸費用の配賦** を選択します。</span><span class="sxs-lookup"><span data-stu-id="41d18-215">For sales orders: On the **Sell** tab, in the **Charges** group, select **Allocate charges**.</span></span>

1. <span data-ttu-id="41d18-216">**諸費用を注文明細行に配賦** ダイアログ ボックスで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="41d18-216">In the **Allocate charges to order lines** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="41d18-217">**諸費用の配賦** – 諸費用の配賦方法を指定するには、次のいずれかの値を選択します。</span><span class="sxs-lookup"><span data-stu-id="41d18-217">**Charges allocation** – Select one of the following values to specify how the charges should be allocated:</span></span>

        - <span data-ttu-id="41d18-218">*正味金額* – 合計正味金額に対する明細行の金額ごとに諸費用を配賦します。</span><span class="sxs-lookup"><span data-stu-id="41d18-218">*Net amount* – Allocate charges according to each line amount relative to the total net amount.</span></span>
        - <span data-ttu-id="41d18-219">*数量* – 合計単位数に対する各明細行の個数に応じて諸費用を配賦します。</span><span class="sxs-lookup"><span data-stu-id="41d18-219">*Quantity* – Allocate charges according to the number of units for each line relative to the total number of units.</span></span>
        - <span data-ttu-id="41d18-220">*明細行ごと* – 明細行の合計数の間で諸費用が均等に配賦されます。</span><span class="sxs-lookup"><span data-stu-id="41d18-220">*Per line* – Allocate charges equally among the total number of lines.</span></span>

    - <span data-ttu-id="41d18-221">**諸費用を明細行に配賦** – 諸費用をすべての明細行に配賦するか、正の明細行のみに配賦するか、または負の明細行のみに配賦するかを指定する値を選択します。</span><span class="sxs-lookup"><span data-stu-id="41d18-221">**Allocate charges to lines** – Select a value to specify whether charges should be allocated to all lines, to positive lines only, or to negative lines only.</span></span>
    - <span data-ttu-id="41d18-222">**すべてを配賦** – 諸費用コードが *品目* 以外の借方タイプである場合でも、諸費用を注文明細行に配賦する場合は、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="41d18-222">**Allocate all** – Select this check box to allocate charges to order lines even if the charges code has a debit type other than *Item*.</span></span>
    - <span data-ttu-id="41d18-223">**受取済** – 受入済注文明細行にのみ諸費用を配賦する場合は、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="41d18-223">**Received** – Select this check box to allocate charges only to received order lines.</span></span>
    - <span data-ttu-id="41d18-224">**在庫** – 在庫注文明細行にのみ諸費用を配賦する場合は、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="41d18-224">**Stocked** – Select this check box to allocate charges to only inventoried order lines.</span></span>
    - <span data-ttu-id="41d18-225">**選択の表示および特定の明細行の削除** – この配賦から特定の明細行を除外するには、このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="41d18-225">**Show selections and clear specific lines** – Select this check box to exclude specific lines from this allocation.</span></span> <span data-ttu-id="41d18-226">このチェックボックスをオンにすると、**配賦から除外する明細行の選択** グリッドが開きます。</span><span class="sxs-lookup"><span data-stu-id="41d18-226">When you select this check box, the **Choose lines to exclude from allocation** grid is opened.</span></span> <span data-ttu-id="41d18-227">グリッドには、**諸費用を明細行に配賦** および **在庫** 設定によって定義された基準に一致する明細行のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="41d18-227">This grid includes only lines that match the criteria that are defined by the **Allocate charges to lines** and **Stocked** settings.</span></span> <span data-ttu-id="41d18-228">たとえば **諸費用を明細行に配賦** フィールドを *正の明細行* に設定し **在庫** チェックボックスをオンにすると、正で在庫された明細行だけがグリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="41d18-228">For example, if you set the **Allocate charges to lines** field to *Positive lines* and select the **Stocked** check box, the grid shows only lines that are both positive and inventoried.</span></span> <span data-ttu-id="41d18-229">さらに、すべての数量が既に受入済である明細行がグリッドによって自動的に除外されます。</span><span class="sxs-lookup"><span data-stu-id="41d18-229">In addition, the grid automatically filters out any lines that the full quantity has already been received for.</span></span> <span data-ttu-id="41d18-230">グリッドが開いている間に、配賦から除外する各明細行の **含める** チェックボックスをクリアにします。</span><span class="sxs-lookup"><span data-stu-id="41d18-230">While the grid is open, clear the **Include** check box for each line that should be excluded from allocation.</span></span> 

        > [!IMPORTANT]
        > <span data-ttu-id="41d18-231">**配賦から除外する明細行の選択** グリッドを使用する場合は、**配賦** を選択するまで、グリッドを開いたままにしておいてください。</span><span class="sxs-lookup"><span data-stu-id="41d18-231">When you work with the **Choose lines to exclude from allocation** grid, be sure to leave the grid open until you select **Allocate**.</span></span> <span data-ttu-id="41d18-232">**配賦** を選択する前にグリッドを閉じると、グリッドの設定が失われます。</span><span class="sxs-lookup"><span data-stu-id="41d18-232">If you close the grid before you select **Allocate**, your settings in the grid will be lost.</span></span> <span data-ttu-id="41d18-233">したがって、諸費用は以前に定義した基準に基づいて配賦されます。</span><span class="sxs-lookup"><span data-stu-id="41d18-233">Therefore, charges will be allocated based on the criteria that you previously defined.</span></span>

1. <span data-ttu-id="41d18-234">**配賦** を選択して設定を適用し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="41d18-234">Select **Allocate** to apply your settings and close the dialog box.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]