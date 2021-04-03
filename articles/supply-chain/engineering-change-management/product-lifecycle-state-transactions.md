---
title: 製品ライフサイクルの状態とトランザクション
description: このトピックでは、エンジニアリング製品がライフサイクルを通過するときに、ライフサイクル状態ごとに許可されるトランザクションを制御する方法について説明します。
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEcoResProductLifecycleStateChange
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 9c6ba9831b84e1220ee158d8186675107b490124
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5266178"
---
# <a name="product-lifecycle-states-and-transactions"></a><span data-ttu-id="d5024-103">製品ライフサイクルの状態とトランザクション</span><span class="sxs-lookup"><span data-stu-id="d5024-103">Product lifecycle states and transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5024-104">エンジニアリング製品はライフサイクルを通じて、ライフサイクル状態ごとに許可するトランザクションを制御できるようにすることが重要です。</span><span class="sxs-lookup"><span data-stu-id="d5024-104">As an engineering product goes through its lifecycle, it's important that you be able to control which transactions are allowed for each lifecycle state.</span></span> <span data-ttu-id="d5024-105">たとえば、まだ成熟していない製品を販売注文にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="d5024-105">For example, products that aren't yet in a mature state should not be put on a sales order.</span></span> <span data-ttu-id="d5024-106">また、製品がライフサイクル終了の状態に達した場合は、その製品のインフローを制御する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5024-106">Alternatively, if a product is reaching its end-of-life state, you might want to control the inflow of that product.</span></span>

<span data-ttu-id="d5024-107">エンジニアリング製品の場合、ライフサイクルの状態の変更は、製品のエンジニアリング バージョンに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="d5024-107">For an engineering product, changes to the lifecycle state are connected to the product's engineering versions.</span></span> <span data-ttu-id="d5024-108">したがって、製品のライフサイクルの状態は、そのエンジニアリング バージョンに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="d5024-108">Therefore, the product's lifecycle state can also be connected to its engineering versions.</span></span> <span data-ttu-id="d5024-109">製品ライフサイクルの状態がエンジニアリング バージョンに関連付けられている場合は、ライフサイクルの状態を使用して、エンジニアリングのバージョンに許可されるトランザクションを制御できます。</span><span class="sxs-lookup"><span data-stu-id="d5024-109">When the product lifecycle state is connected to an engineering version, you can use the lifecycle state to control which transactions are allowed for the engineering version.</span></span>

## <a name="create-and-manage-product-lifecycle-states"></a><span data-ttu-id="d5024-110">製品ライフサイクルの状態の作成と管理</span><span class="sxs-lookup"><span data-stu-id="d5024-110">Create and manage product lifecycle states</span></span>

<span data-ttu-id="d5024-111">製品ライフサイクルの状態を使用するには、**エンジニアリング変更管理 \> 設定 \> 製品ライフサイクルの状態** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d5024-111">To work with product lifecycle states, go to **Engineering change management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="d5024-112">そして、次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="d5024-112">Then follow one of these steps.</span></span>

- <span data-ttu-id="d5024-113">新しい製品ライフサイクルの状態を作成するには、アクション ペインで **新規** を選択し、次のセクションの説明に従ってフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="d5024-113">To create a new lifecycle state, select **New** on the Action Pane, and then set the fields as described in the following subsections.</span></span>
- <span data-ttu-id="d5024-114">既存の製品ライフサイクルの状態を編集するには、リスト ペインでカテゴリを選択し、アクション ペインで **編集** を選択して、次のセクションの説明に従ってフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="d5024-114">To edit an existing lifecycle state, select it in the list pane, select **Edit** on the Action Pane, and then set the fields as described in the following subsections.</span></span>
- <span data-ttu-id="d5024-115">既存の製品ライフサイクルの状態を削除するには、リスト ペインでルールセットを選択し、アクション ペインで **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5024-115">To delete an existing lifecycle state, select it in the list pane, and then select **Delete** on the Action Pane.</span></span>

> [!NOTE]
> <span data-ttu-id="d5024-116">エンジニアリング製品では、標準 (非エンジニアリング) 製品と同じ製品ライフサイクルの状態を使用します。</span><span class="sxs-lookup"><span data-stu-id="d5024-116">Engineering products use the same product lifecycle states as standard (non-engineering) products.</span></span> <span data-ttu-id="d5024-117">このトピックで説明されている **製品ライフサイクルの状態** ページを開くには、**製品情報管理 \> 設定 \>製品ライフサイクルの状態** を参照することもできます。</span><span class="sxs-lookup"><span data-stu-id="d5024-117">You can also open the **Product lifecycle state** page that is described in this topic by going to **Product information management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="d5024-118">製品ライフサイクルの状態の詳細については、エンジニアリング製品と標準製品の両方について、[製品ライフサイクルの状態の概要](../pim/product-lifecycle.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5024-118">For more information about product lifecycle states, for both engineering products and standard products, see [Product lifecycle state overview](../pim/product-lifecycle.md).</span></span>

### <a name="header"></a><span data-ttu-id="d5024-119">表題</span><span class="sxs-lookup"><span data-stu-id="d5024-119">Header</span></span>

<span data-ttu-id="d5024-120">製品ライフサイクルの状態のヘッダーには、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="d5024-120">Set the following fields on the header of a product lifecycle state.</span></span>

| <span data-ttu-id="d5024-121">フィールド</span><span class="sxs-lookup"><span data-stu-id="d5024-121">Field</span></span> | <span data-ttu-id="d5024-122">説明</span><span class="sxs-lookup"><span data-stu-id="d5024-122">Description</span></span> |
|---|---|
| <span data-ttu-id="d5024-123">行政単位 (区画)</span><span class="sxs-lookup"><span data-stu-id="d5024-123">State</span></span> | <span data-ttu-id="d5024-124">製品ライフサイクルの状態の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="d5024-124">Enter a name for the product lifecycle state.</span></span> |
| <span data-ttu-id="d5024-125">説明</span><span class="sxs-lookup"><span data-stu-id="d5024-125">Description</span></span> | <span data-ttu-id="d5024-126">製品ライフサイクルの状態の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="d5024-126">Enter a description of the product lifecycle state.</span></span> |

### <a name="general-fasttab"></a><span data-ttu-id="d5024-127">全般クイック タブ</span><span class="sxs-lookup"><span data-stu-id="d5024-127">General FastTab</span></span>

<span data-ttu-id="d5024-128">**一般** クイック タブで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="d5024-128">Set the following fields on the **General** FastTab.</span></span>

| <span data-ttu-id="d5024-129">フィールド</span><span class="sxs-lookup"><span data-stu-id="d5024-129">Field</span></span> | <span data-ttu-id="d5024-130">説明</span><span class="sxs-lookup"><span data-stu-id="d5024-130">Description</span></span> |
|---|---|
| <span data-ttu-id="d5024-131">法人にリリースされたときの既定</span><span class="sxs-lookup"><span data-stu-id="d5024-131">Default when released to a legal entity</span></span> | <span data-ttu-id="d5024-132">標準製品の場合、このライフサイクルの状態が最初にリリースされたときに既定ですべての製品に適用される場合は、このオプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="d5024-132">For standard products, set this option to *Yes* if this lifecycle state should be applied to all products by default when they are first released.</span></span> <span data-ttu-id="d5024-133">このライフサイクルの状態が後で手動で適用される場合は、*いいえ* に設定します。</span><span class="sxs-lookup"><span data-stu-id="d5024-133">Set it to *No* if this lifecycle state will be manually applied later.</span></span><p><span data-ttu-id="d5024-134">この設定は、エンジニアリング製品には適用されません。</span><span class="sxs-lookup"><span data-stu-id="d5024-134">This setting isn't applicable to engineering products.</span></span> <span data-ttu-id="d5024-135">エンジニアリング会社で作成されたエンジニアリング製品バージョンのライフサイクル状態は、エンジニアリング変更カテゴリで指定されています。</span><span class="sxs-lookup"><span data-stu-id="d5024-135">The lifecycle state of an engineering product version after it's created in the engineering company is specified in its engineering change category.</span></span> <span data-ttu-id="d5024-136">製品が運営会社にリリースされると、製品のライフサイクルの状態がコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d5024-136">When the product is released to an operational company, the lifecycle state of the product is copied.</span></span> <span data-ttu-id="d5024-137">つまり、エンジニアリング製品が運用会社にリリースされると、エンジニアリング会社のライフサイクルの状態は同じになります。</span><span class="sxs-lookup"><span data-stu-id="d5024-137">In other words, when an engineering product is released to an operational company, it has the same lifecycle state that it had in the engineering company.</span></span> <span data-ttu-id="d5024-138">ライフサイクルの状態は、運用会社で上書きできます。</span><span class="sxs-lookup"><span data-stu-id="d5024-138">The lifecycle state can be overwritten in the operational company.</span></span></p> |
| <span data-ttu-id="d5024-139">計画に対して有効です。</span><span class="sxs-lookup"><span data-stu-id="d5024-139">Is active for planning</span></span> | <span data-ttu-id="d5024-140">このオプションを *はい* に設定すると、このライフサイクルの状態の製品が、マスター プランおよび部品表 (BOM) レベルの計算に含まれます。</span><span class="sxs-lookup"><span data-stu-id="d5024-140">Set this option to *Yes* to include products that are in this lifecycle state in calculations at the master planning and bill of materials (BOM) levels.</span></span> <span data-ttu-id="d5024-141">このライフサイクル状態の製品を計算から除外する場合は、*いいえ* を設定します。</span><span class="sxs-lookup"><span data-stu-id="d5024-141">Set it to *No* to exclude products that are in this lifecycle state from the calculations.</span></span> |

### <a name="enabled-business-processes-fasttab"></a><span data-ttu-id="d5024-142">有効になっている業務プロセス クイック タブ</span><span class="sxs-lookup"><span data-stu-id="d5024-142">Enabled business processes FastTab</span></span>

<span data-ttu-id="d5024-143">**有効な業務プロセス** クイック タブを使用して、現在のライフサイクル状態の製品で使用できる業務プロセスを制御します。</span><span class="sxs-lookup"><span data-stu-id="d5024-143">Use the **Enabled business processes** FastTab to control which of the available business processes can be used with products in the current lifecycle state.</span></span> <span data-ttu-id="d5024-144">このクイック タブに表示されるプロセスは、次の方法で自動的に検出されます。</span><span class="sxs-lookup"><span data-stu-id="d5024-144">The processes that are listed on this FastTab are automatically found in the following way:</span></span>

- <span data-ttu-id="d5024-145">新しいライフサイクルの状態を初めて保存すると、現在使用可能な業務プロセスがページに読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="d5024-145">The first time that you save a new lifecycle state, the page loads the business processes that are currently available.</span></span>
- <span data-ttu-id="d5024-146">システムに新しい業務プロセスを追加する場合は、アクション ペインで **更新の確認** を選択することにより、既存のライフサイクル状態に対して **有効になっている業務プロセス** クイック タブのリストを更新できます。</span><span class="sxs-lookup"><span data-stu-id="d5024-146">If you add new business processes to your system, you can update the list on the **Enabled business processes** FastTab for an existing lifecycle state by selecting **Check for updates** on the Action Pane.</span></span>

<span data-ttu-id="d5024-147">**有効な業務プロセス** クイック タブに表示されているプロセスごとに、次のフィールドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d5024-147">The following fields are available for each process that is listed on the **Enabled business processes** FastTab.</span></span>

| <span data-ttu-id="d5024-148">フィールド</span><span class="sxs-lookup"><span data-stu-id="d5024-148">Field</span></span> | <span data-ttu-id="d5024-149">説明</span><span class="sxs-lookup"><span data-stu-id="d5024-149">Description</span></span> |
|---|---|
| <span data-ttu-id="d5024-150">処理</span><span class="sxs-lookup"><span data-stu-id="d5024-150">Process</span></span> | <span data-ttu-id="d5024-151">この読み取り専用フィールドには、既存の業務プロセスの名前が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d5024-151">This read-only field shows the name of an existing business process.</span></span> |
| <span data-ttu-id="d5024-152">プロセス領域</span><span class="sxs-lookup"><span data-stu-id="d5024-152">Process area</span></span> | <span data-ttu-id="d5024-153">この読み取り専用フィールドには、既存のプロセス領域の名前が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d5024-153">This read-only field shows the name of an existing process area.</span></span> |
| <span data-ttu-id="d5024-154">保険証書</span><span class="sxs-lookup"><span data-stu-id="d5024-154">Policy</span></span> | <span data-ttu-id="d5024-155">次のいずれかの値を選択して、このライフサイクル状態の製品に対して現在のプロセスを許可するかどうか、およびどのように許可するかを制御します。</span><span class="sxs-lookup"><span data-stu-id="d5024-155">Select one of the following values to control whether and how the current process will be permitted for products that are in this lifecycle state:</span></span><ul><li><span data-ttu-id="d5024-156">**有効** – 業務プロセスは許可されます。</span><span class="sxs-lookup"><span data-stu-id="d5024-156">**Enabled** – The business process is allowed.</span></span></li><li><span data-ttu-id="d5024-157">**ブロック** – プロセスは許可されていません。</span><span class="sxs-lookup"><span data-stu-id="d5024-157">**Blocked** – The process isn't allowed.</span></span> <span data-ttu-id="d5024-158">このライフサイクル状態の製品に対してプロセスを使用しようとすると、システムはそのユーザーをブロックし、代わりにエラーを表示します。</span><span class="sxs-lookup"><span data-stu-id="d5024-158">If a user tries to use the process on a product that is in this lifecycle state, the system will block the attempt and show an error instead.</span></span> <span data-ttu-id="d5024-159">たとえば、製品版の購入を中止することができます。</span><span class="sxs-lookup"><span data-stu-id="d5024-159">For example, you might block end-of-life products from being purchased.</span></span></li><li><span data-ttu-id="d5024-160">**警告付きで有効化** – プロセスは許可されますが、警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d5024-160">**Enabled with warning** – The process is allowed, but a warning will be shown.</span></span> <span data-ttu-id="d5024-161">たとえば、研究開発部門によって作成された製造オーダーにプロトタイプ製品を配置することができます。</span><span class="sxs-lookup"><span data-stu-id="d5024-161">For example, you might want a prototype product to be put on a production order that is created by the Research and Development department.</span></span> <span data-ttu-id="d5024-162">ただし、他の部門は、まだ製品を生産しないようにする必要があることを認識しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5024-162">However, other departments should be aware that they should not produce the product yet.</span></span></li></ul> |

<span data-ttu-id="d5024-163">ライフサイクル状態のルールをカスタマイズとして追加している場合は、上部ウィンドウで **プロセスの更新** を選択することにより、ユーザーインターフェイス (UI) にそれらのルールを表示できます。</span><span class="sxs-lookup"><span data-stu-id="d5024-163">If you're adding more lifecycle state rules as a customization, you can view those rules in the user interface (UI) by selecting **Refresh processes** in the upper pane.</span></span> <span data-ttu-id="d5024-164">**プロセスの更新** ボタンは、管理者のみが使用できます。</span><span class="sxs-lookup"><span data-stu-id="d5024-164">The **Refresh processes** button is available only to administrators.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]