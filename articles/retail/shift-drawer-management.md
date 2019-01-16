---
title: "シフトとキャッシュ ドロワーの管理"
description: "このトピックでは、小売販売時点管理 (POS) のシフトの設定および使用方法について説明します。"
author: jblucher
manager: AnnBe
ms.date: 05/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 7ad3c3fd17e88f364be12c122e2f5c155b7b9064
ms.contentlocale: ja-jp
ms.lasthandoff: 01/04/2019

---

# <a name="shift-and-cash-drawer-management"></a><span data-ttu-id="f663b-103">シフトとキャッシュ ドロワーの管理</span><span class="sxs-lookup"><span data-stu-id="f663b-103">Shift and cash drawer management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f663b-104">このトピックでは、小売販売時点管理 (POS) のシフトの設定および使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f663b-104">This topic explains how to set up and use shifts in retail point of sale (POS).</span></span>

<span data-ttu-id="f663b-105">Microsoft Dynamics 365 for Retail で、*シフト*という用語は 2 つの時点間の POS トランザクション データと活動のコレクションを示します。</span><span class="sxs-lookup"><span data-stu-id="f663b-105">In Microsoft Dynamics 365 for Retail, the term *shift* describes the collection of POS transactional data and activities between two points in time.</span></span> <span data-ttu-id="f663b-106">各シフトについて、予測される金額は、カウントおよび申告された金額に対して比較されます。</span><span class="sxs-lookup"><span data-stu-id="f663b-106">For each shift, the amount of money that is expected is compared against the amount that was counted and declared.</span></span>

<span data-ttu-id="f663b-107">通常、シフトは営業日の開始時に開かれます。</span><span class="sxs-lookup"><span data-stu-id="f663b-107">Typically, shifts are opened at the start of the business day.</span></span> <span data-ttu-id="f663b-108">その時点で、ユーザーはキャッシュ ドロワーにある開始金額を申告します。</span><span class="sxs-lookup"><span data-stu-id="f663b-108">At that point, a user declares the starting amount that the cash drawer contains.</span></span> <span data-ttu-id="f663b-109">それから、販売トランザクションは終日にわたって実行されます。</span><span class="sxs-lookup"><span data-stu-id="f663b-109">Sales transactions are then performed throughout the day.</span></span> <span data-ttu-id="f663b-110">最後に、その日の終わりにドロワーをカウントし、終了金額を申告します。</span><span class="sxs-lookup"><span data-stu-id="f663b-110">Finally, at the end of the day, the drawer is counted, and the closing amounts are declared.</span></span> <span data-ttu-id="f663b-111">シフトは閉じられ、Z レポートが生成されます。</span><span class="sxs-lookup"><span data-stu-id="f663b-111">The shift is closed, and a Z report is generated.</span></span> <span data-ttu-id="f663b-112">Z レポートは過不足があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f663b-112">The Z report indicates whether there is an overage or shortage.</span></span>

## <a name="typical-shift-scenarios"></a><span data-ttu-id="f663b-113">標準的なシフトのシナリオ</span><span class="sxs-lookup"><span data-stu-id="f663b-113">Typical shift scenarios</span></span>

<span data-ttu-id="f663b-114">Retail は、複数のコンフィギュレーション オプションおよび POS 操作を提供し、POS の営業終了業務プロセスを幅広くサポートします。</span><span class="sxs-lookup"><span data-stu-id="f663b-114">Retail provides several configuration options and POS operations to support a wide range of end-of-day business processes for the POS.</span></span> <span data-ttu-id="f663b-115">このセクションでは、いくつかの標準的なシフトのシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f663b-115">This section describes some typical shift scenarios.</span></span>

### <a name="fixed-till"></a><span data-ttu-id="f663b-116">固定レジ</span><span class="sxs-lookup"><span data-stu-id="f663b-116">Fixed till</span></span>

<span data-ttu-id="f663b-117">従来、このシナリオは最も頻繁に使用されてきました。</span><span class="sxs-lookup"><span data-stu-id="f663b-117">Traditionally, this scenario has been used most often.</span></span> <span data-ttu-id="f663b-118">まだ広く使用されています。</span><span class="sxs-lookup"><span data-stu-id="f663b-118">It's still extensively used.</span></span> <span data-ttu-id="f663b-119">「固定レジ」のシフトにおいて、シフトおよびレジは特定のレジスターに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="f663b-119">In a "fixed till" shift, the shift and till are associated with a specific register.</span></span> <span data-ttu-id="f663b-120">1 台のレジスターから他には移動されません。</span><span class="sxs-lookup"><span data-stu-id="f663b-120">They aren't moved from one register to another.</span></span> <span data-ttu-id="f663b-121">「固定レジ」シフトは、単一のユーザーによって使用されるか、あるいは複数のユーザー間で共有されます。</span><span class="sxs-lookup"><span data-stu-id="f663b-121">A "fixed till" shift can be used by a single user or shared among multiple users.</span></span> <span data-ttu-id="f663b-122">「固定レジ」シフトに特別なコンフィギュレーションは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="f663b-122">"Fixed till" shifts don't require any special configuration.</span></span>

### <a name="floating-till"></a><span data-ttu-id="f663b-123">フローティング レジ</span><span class="sxs-lookup"><span data-stu-id="f663b-123">Floating till</span></span>

<span data-ttu-id="f663b-124">「フローティング レジ」シフトにおいて、シフトおよびキャッシュ ドロワーは 1 台のレジスターから他に移動できます。</span><span class="sxs-lookup"><span data-stu-id="f663b-124">In a "floating till" shift, the shift and cash drawer can be moved from one register to another.</span></span> <span data-ttu-id="f663b-125">レジスターはキャッシュ ドロワーごとに有効なシフトを 1 つだけ持つことができますが、シフトを中断してから後でまたは別のレジスターで再開することができます。</span><span class="sxs-lookup"><span data-stu-id="f663b-125">Although a register can have only one active shift per cash drawer, shifts can be suspended and then resumed later or on a different register.</span></span>

<span data-ttu-id="f663b-126">たとえば、店舗に 2 つのレジスターがあるとします。</span><span class="sxs-lookup"><span data-stu-id="f663b-126">For example, a store has two registers.</span></span> <span data-ttu-id="f663b-127">各レジスターはその日の開始時に開かれ、レジ担当者は新しいシフトを開いて、開始金額を提供します。</span><span class="sxs-lookup"><span data-stu-id="f663b-127">Each register is opened at the start of the day when the cashier opens a new shift and provides the starting amount.</span></span> <span data-ttu-id="f663b-128">1 人のレジ担当者が休憩を取る場合、そのレジ担当者は自分のシフトを中断し、キャッシュ ドロワーからレジを削除します。</span><span class="sxs-lookup"><span data-stu-id="f663b-128">When one cashier is ready to take a break, that cashier suspends his or her shift and removes the till from the cash drawer.</span></span> <span data-ttu-id="f663b-129">それから、そのレジスターは他のレジ担当者に対して使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="f663b-129">That register then becomes available to other cashiers.</span></span> <span data-ttu-id="f663b-130">他のレジ担当者はサインインし、そのレジスターで自分のシフトを開けます。</span><span class="sxs-lookup"><span data-stu-id="f663b-130">Another cashier can sign in to and open his or her own shift on the register.</span></span> <span data-ttu-id="f663b-131">最初のレジ担当者の休憩が終了した後、そのレジ担当者は他のレジスターが使用可能になった時に自分のシフトを再開できます。</span><span class="sxs-lookup"><span data-stu-id="f663b-131">After the first cashier's break has ended, that cashier can resume his or her shift when one of the other registers becomes available.</span></span> <span data-ttu-id="f663b-132">「フローティング レジ」シフトに特別なコンフィギュレーションあるいはアクセス許可は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="f663b-132">"Floating till" shifts don't require any special configuration or permission.</span></span>

### <a name="single-user"></a><span data-ttu-id="f663b-133">単一のユーザー</span><span class="sxs-lookup"><span data-stu-id="f663b-133">Single user</span></span>

<span data-ttu-id="f663b-134">小売業者の多くはシフトごとに 1 人のユーザーのみ許可し、キャッシュ ドロワーの現金に対する最高レベルの責任の所在を保証しています。</span><span class="sxs-lookup"><span data-stu-id="f663b-134">Many retailers prefer to allow only one user per shift, to help guarantee the highest level of accountability for the cash in the cash drawer.</span></span> <span data-ttu-id="f663b-135">シフトに関連付けられているレジを 1 人のユーザーのみが使用する場合、そのユーザーにはいずれの不一致に対しても一切の責任が課せられます。</span><span class="sxs-lookup"><span data-stu-id="f663b-135">If only one user is allowed to use the till that is associated with a shift, that user can be held solely responsible for any discrepancies.</span></span> <span data-ttu-id="f663b-136">複数のユーザーがシフトを使用している場合、だれがエラーを作成したのか、またはレジから盗難しようとしたのかを特定するのは困難です。</span><span class="sxs-lookup"><span data-stu-id="f663b-136">If more than one user uses a shift, it's difficult to determine who made an error, or who might be trying to steal from the till.</span></span>

### <a name="multiple-users"></a><span data-ttu-id="f663b-137">複数のユーザー</span><span class="sxs-lookup"><span data-stu-id="f663b-137">Multiple users</span></span>

<span data-ttu-id="f663b-138">一部の小売業者は、単一ユーザーのシフトによる責任の所在のレベルを犠牲にし、シフトごとに複数のユーザーを許可します。</span><span class="sxs-lookup"><span data-stu-id="f663b-138">Some retailers are willing to sacrifice the level of accountability that single-user shifts provide and to allow more than one user per shift.</span></span> <span data-ttu-id="f663b-139">この方法は、通常、ユーザーが使用可能なレジスターよりも多く、柔軟性および速さの必要性が損失の発生する可能性を上回る場合です。</span><span class="sxs-lookup"><span data-stu-id="f663b-139">This approach is typical when there are more users than available registers, and the need for flexibility and speed outweighs the potential for loss.</span></span> <span data-ttu-id="f663b-140">店舗のマネージャーが自分のシフトを持たないものの、必要に応じて、いずれかのレジ担当者のシフトを使用する場合にも一般的です。</span><span class="sxs-lookup"><span data-stu-id="f663b-140">It's also typical when store managers don't have their own shifts but can, as required, use the shifts of any of their cashiers.</span></span> <span data-ttu-id="f663b-141">サインインし、他のユーザーによって開始されたシフトを使用するには、ユーザーに**複数シフト ログオンを許可** POS アクセス許可がある必要があります。</span><span class="sxs-lookup"><span data-stu-id="f663b-141">To sign in to and use a shift that was opened by another user, a user must have the **Allow multiple shift logon** POS permission.</span></span>

### <a name="shared-shift"></a><span data-ttu-id="f663b-142">共有シフト</span><span class="sxs-lookup"><span data-stu-id="f663b-142">Shared shift</span></span>

<span data-ttu-id="f663b-143">「共有シフト」コンフィギュレーションにより、小売業者は複数のレジスター、キャッシュ ドロワー、およびユーザー間で単一シフトを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="f663b-143">A "shared shift" configuration lets retailers have a single shift across multiple registers, cash drawers, and users.</span></span> <span data-ttu-id="f663b-144">共有シフトには、すべてのキャッシュ ドロワー間で集計された 1 つの開始金額および 1 つの終了金額があります。</span><span class="sxs-lookup"><span data-stu-id="f663b-144">A shared shift has a single starting amount and a single closing amount that are summarized across all cash drawers.</span></span> <span data-ttu-id="f663b-145">モバイル デバイスが使用される場合、共有シフトは最も一般的です。</span><span class="sxs-lookup"><span data-stu-id="f663b-145">Shared shifts are most typical when mobile devices are used.</span></span> <span data-ttu-id="f663b-146">このシナリオでは、各レジスターに個別のキャッシュ ドロワーは予約されていません。</span><span class="sxs-lookup"><span data-stu-id="f663b-146">In this scenario, a separate cash drawer isn't reserved for each register.</span></span> <span data-ttu-id="f663b-147">代わりに、すべてのレジスターは 1 つのキャッシュ ドロワーを共有できます。</span><span class="sxs-lookup"><span data-stu-id="f663b-147">Instead, all registers can share one cash drawer.</span></span>

<span data-ttu-id="f663b-148">店舗で使用される共有シフトについて、キャッシュ ドロワーは、**小売 \> チャンネル設定 \> POS 設定 \> POS プロファイル \> ハードウェア プロファイル \> ドロワー**で、「共有シフトのドロワー」としてコンフィギュレーションされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f663b-148">For shared shifts to be used in a store, the cash drawer must be configured as a "shared shift drawer" at **Retail \> Channel setup \> POS setup \> POS profiles \> Hardware profiles \> Drawer**.</span></span> <span data-ttu-id="f663b-149">また、ユーザーは共有シフトのアクセス許可 (共有シフトの管理の許可および共有シフトの使用の許可) のどちらか 1 つまたは両方が必要です。</span><span class="sxs-lookup"><span data-stu-id="f663b-149">Additionally, users must have one or both of the shared shift permissions (Allow manage shared shift and Allow use shared shift).</span></span>

> [!NOTE]
> <span data-ttu-id="f663b-150">各店舗で一度に 1 つの共有シフトしか開くことはできません。</span><span class="sxs-lookup"><span data-stu-id="f663b-150">Only one shared shift can be open at a time in each store.</span></span> <span data-ttu-id="f663b-151">共有シフトとスタンドアロンのシフトは同じ店舗で使用できます。</span><span class="sxs-lookup"><span data-stu-id="f663b-151">Shared shifts and stand-alone shifts can be used in the same store.</span></span>

## <a name="shift-and-drawer-operations"></a><span data-ttu-id="f663b-152">シフトとドロワーの操作</span><span class="sxs-lookup"><span data-stu-id="f663b-152">Shift and drawer operations</span></span>

<span data-ttu-id="f663b-153">さまざまな操作によってシフトの状態の変更、またはキャッシュ ドロワーの合計金額の増減を実行することができます。</span><span class="sxs-lookup"><span data-stu-id="f663b-153">Various operations can be performed to change the state of a shift, or to increase or decrease the amount of money in the cash drawer.</span></span> <span data-ttu-id="f663b-154">このセクションでは、Retail Modern POS およびクラウド POS に対する Microsoft Dynamics 365 に対するこれらのシフト操作について説明します。</span><span class="sxs-lookup"><span data-stu-id="f663b-154">This section describes these shift operations for Microsoft Dynamics 365 for Retail Modern POS and Cloud POS.</span></span>

### <a name="open-shift"></a><span data-ttu-id="f663b-155">オープン シフト</span><span class="sxs-lookup"><span data-stu-id="f663b-155">Open shift</span></span>

<span data-ttu-id="f663b-156">POS では、販売、返品、顧客注文などの財務トランザクションを作成する操作を実行するために、ユーザーは有効で開かれたシフトを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="f663b-156">The POS requires that users have an active, open shift in order to perform any operations that will produce a financial transaction, such as a sale, return, or customer order.</span></span>

<span data-ttu-id="f663b-157">ユーザーが POS にサインインすると、システムは最初に、現在のレジスター上でそのユーザーの有効なシフトが使用可能かをチェックします。</span><span class="sxs-lookup"><span data-stu-id="f663b-157">When a user signs in to the POS, the system first verifies whether an active shift is available for that user on the current register.</span></span> <span data-ttu-id="f663b-158">有効なシフトが使用可能でない場合、システム コンフィギュレーションおよびユーザーのアクセス許可に応じて、ユーザーは新しいシフトを開くか、既存のシフトを再開するか、または「ドロワー以外」モードでサインインすることができます。</span><span class="sxs-lookup"><span data-stu-id="f663b-158">If an active shift isn't available, the user can open a new shift, resume an existing shift, or sign in in "non-drawer" mode, depending on the system configuration and the user's permissions.</span></span>

### <a name="declare-start-amount"></a><span data-ttu-id="f663b-159">開始金額の申告</span><span class="sxs-lookup"><span data-stu-id="f663b-159">Declare start amount</span></span>

<span data-ttu-id="f663b-160">多くの場合、この操作は新しく開かれたシフトに実行される最初の操作になります。</span><span class="sxs-lookup"><span data-stu-id="f663b-160">This operation is often the first operation that is performed for a newly opened shift.</span></span> <span data-ttu-id="f663b-161">この操作により、ユーザはシフトのキャッシュ ドロワー内の現金の開始金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="f663b-161">For this operation, users specify the starting cash amount in the cash drawer for the shift.</span></span> <span data-ttu-id="f663b-162">シフトが閉じられる際に行われる過不足計算が開始金額を考慮するため、この操作は重要です。</span><span class="sxs-lookup"><span data-stu-id="f663b-162">This operation is important because the overage/shortage calculation that occurs when a shift is closed considers the start amount.</span></span>

### <a name="float-entry"></a><span data-ttu-id="f663b-163">釣銭入力</span><span class="sxs-lookup"><span data-stu-id="f663b-163">Float entry</span></span>

<span data-ttu-id="f663b-164">*釣銭入力*は、有効なシフトで実行される販売以外のトランザクションであり、キャッシュ ドロワー内の現金額を増やします。</span><span class="sxs-lookup"><span data-stu-id="f663b-164">*Float entries* are non-sales transactions that are performed in an active shift to increase the amount of cash in the cash drawer.</span></span> <span data-ttu-id="f663b-165">釣銭入力の一般的な例は、ドロワーが少ない場合にドロワーに追加の変更を加えるトランザクションです。</span><span class="sxs-lookup"><span data-stu-id="f663b-165">A typical example of a float entry is a transaction to add additional change to the drawer when it's running low.</span></span>

### <a name="tender-removal"></a><span data-ttu-id="f663b-166">支払/入金の削除</span><span class="sxs-lookup"><span data-stu-id="f663b-166">Tender removal</span></span>

<span data-ttu-id="f663b-167">*支払/入金の削除*は、キャッシュ ドロワー内の現金額を減らすために有効なシフトで実行される販売以外のトランザクションです。</span><span class="sxs-lookup"><span data-stu-id="f663b-167">*Tender removals* are non-sales transactions that are performed in an active shift to reduce the amount of cash in the cash drawer.</span></span> <span data-ttu-id="f663b-168">この操作は、異なるシフトの釣銭入力操作と組み合わせて最も頻繁に使用されます。</span><span class="sxs-lookup"><span data-stu-id="f663b-168">This operation is most often used in conjunction with a Float entry operation on a different shift.</span></span> <span data-ttu-id="f663b-169">たとえば、レジスター 1 は変化が少ないため、レジスター 2 のユーザーが自分のドロワー内の金額を削減するために支払/入金の削除を行います。</span><span class="sxs-lookup"><span data-stu-id="f663b-169">For example, because register 1 is running low on change, the user on register 2 does a tender removal to reduce the amount in his or her cash drawer.</span></span> <span data-ttu-id="f663b-170">それから、レジスター 1 のユーザーは自分のキャッシュ ドロワー内の金額を増加させるため釣銭入力を行います。</span><span class="sxs-lookup"><span data-stu-id="f663b-170">The user on register 1 then does a float entry to increase the amount in his or her cash drawer.</span></span>

### <a name="suspend-shift"></a><span data-ttu-id="f663b-171">シフトの中断</span><span class="sxs-lookup"><span data-stu-id="f663b-171">Suspend shift</span></span>

<span data-ttu-id="f663b-172">ユーザーは、有効なシフトを中断して、別のユーザーの現在の登録を解放したり、別の登録にシフトを移すことができます (この場合、通常は「フローティング レジ」シフトと呼ばれます)。</span><span class="sxs-lookup"><span data-stu-id="f663b-172">Users can suspend their active shift to free up the current register for another user, or to move their shift to a different register (in this case, the shift is often referred to as a "floating till" shift).</span></span>

<span data-ttu-id="f663b-173">シフトの中断により、再開されるまで、新しいトランザクションやシフトの変更が防止されます。</span><span class="sxs-lookup"><span data-stu-id="f663b-173">Suspension of a shift prevents any new transactions or changes to the shift until it's resumed.</span></span>

### <a name="resume-shift"></a><span data-ttu-id="f663b-174">シフトの再開</span><span class="sxs-lookup"><span data-stu-id="f663b-174">Resume shift</span></span>

<span data-ttu-id="f663b-175">この操作により、ユーザーは、有効なシフトをまだ持っていないどのレジスターでも以前に中断したシフトを再開することができます。</span><span class="sxs-lookup"><span data-stu-id="f663b-175">This operation lets users resume a previously suspended shift on any register that doesn't already have an active shift.</span></span>

### <a name="tender-declaration"></a><span data-ttu-id="f663b-176">支払/入金申告</span><span class="sxs-lookup"><span data-stu-id="f663b-176">Tender declaration</span></span>

<span data-ttu-id="f663b-177">この操作を実行して、現在キャッシュ ドロワー内にある金額の合計金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="f663b-177">This operation is performed to specify the total amount of money that is currently in the cash drawer.</span></span> <span data-ttu-id="f663b-178">ユーザーは、ほとんどの場合、シフトを閉じる前にこの操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="f663b-178">Users most often perform this operation before they close a shift.</span></span> <span data-ttu-id="f663b-179">指定された金額は、過不足額を計算するため、予測されるシフトの金額と比較されます。</span><span class="sxs-lookup"><span data-stu-id="f663b-179">The specified amount is compared against the expected shift amount to calculate the overage/shortage amount.</span></span>

### <a name="safe-drop"></a><span data-ttu-id="f663b-180">金庫保管</span><span class="sxs-lookup"><span data-stu-id="f663b-180">Safe drop</span></span>

<span data-ttu-id="f663b-181">金庫保管はいつでも有効なシフトで行えます。</span><span class="sxs-lookup"><span data-stu-id="f663b-181">Safe drops can be done on an active shift at any time.</span></span> <span data-ttu-id="f663b-182">この操作はキャッシュ ドロワーから金銭を取り出すので、奥の部屋の金庫など、より安全な場所に移動することができます。</span><span class="sxs-lookup"><span data-stu-id="f663b-182">This operation removes money from the cash drawer so that it can be transferred to a more secure location, such as a safe in the back room.</span></span> <span data-ttu-id="f663b-183">金庫保管に記録された合計金額はシフト合計に含まれますが、支払/入金申告の一部としてカウントする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f663b-183">The total amount that is recorded for safe drops is included in shift totals, but it doesn't have to be counted as part of the tender declaration.</span></span>

### <a name="bank-drop"></a><span data-ttu-id="f663b-184">銀行入金</span><span class="sxs-lookup"><span data-stu-id="f663b-184">Bank drop</span></span>

<span data-ttu-id="f663b-185">金庫保管のように、銀行入金は有効なシフトで行われます。</span><span class="sxs-lookup"><span data-stu-id="f663b-185">Like safe drops, bank drops are done on active shifts.</span></span> <span data-ttu-id="f663b-186">この操作により、シフトからの金銭が取り出され、銀行預金の準備が整います。</span><span class="sxs-lookup"><span data-stu-id="f663b-186">This operation removes money from the shift to prepare for the bank deposit.</span></span>

### <a name="blind-close-shift"></a><span data-ttu-id="f663b-187">シフトのブラインド クローズ</span><span class="sxs-lookup"><span data-stu-id="f663b-187">Blind close shift</span></span>

<span data-ttu-id="f663b-188">*ブラインド クローズ済シフト*は無効ですが、完全には終了していません。</span><span class="sxs-lookup"><span data-stu-id="f663b-188">*Blind-closed shifts* are no longer active but haven't been fully closed.</span></span> <span data-ttu-id="f663b-189">中断されたシフトとは異なり、ブラインド クローズ済シフトを再開することはできません。</span><span class="sxs-lookup"><span data-stu-id="f663b-189">Unlike suspended shifts, blind-closed shifts can't be resumed.</span></span> <span data-ttu-id="f663b-190">ただし、開始金額の宣言などの操作および支払/入金申告は、後でまたは異なるレジスターから実行することができます。</span><span class="sxs-lookup"><span data-stu-id="f663b-190">However, operations such as Declare start amount and Tender declaration can be performed on them later or from a different register.</span></span>

<span data-ttu-id="f663b-191">ブラインド クローズ済シフトは、最初にこのシフトの完全なカウント、調整、クローズをすることなく、新しいユーザーまたはシフト用にレジスターを解放するためによく使用されます。</span><span class="sxs-lookup"><span data-stu-id="f663b-191">Blind-closed shifts are often used to free up a register for a new user or shift without first having to fully count, reconcile, and close the shift.</span></span>

### <a name="close-shift"></a><span data-ttu-id="f663b-192">シフトのクローズ</span><span class="sxs-lookup"><span data-stu-id="f663b-192">Close shift</span></span>

<span data-ttu-id="f663b-193">この操作により、シフト合計および過不足額が計算され、有効またはブラインド クローズ済シフトが完了します。</span><span class="sxs-lookup"><span data-stu-id="f663b-193">This operation calculates shift totals and overage/shortage amounts, and then finalizes an active or blind-closed shift.</span></span> <span data-ttu-id="f663b-194">ユーザーのアクセス許可に応じて、Z レポートはシフトにも印刷されます。</span><span class="sxs-lookup"><span data-stu-id="f663b-194">Depending on the user's permissions, a Z report is also printed for the shift.</span></span> <span data-ttu-id="f663b-195">クローズ済シフトの再開または変更はできません。</span><span class="sxs-lookup"><span data-stu-id="f663b-195">Closed shifts can't be resumed or modified.</span></span>

### <a name="print-x"></a><span data-ttu-id="f663b-196">X の印刷</span><span class="sxs-lookup"><span data-stu-id="f663b-196">Print X</span></span>

<span data-ttu-id="f663b-197">この操作は、現在の有効なシフトの X レポートの生成および印刷を行います。</span><span class="sxs-lookup"><span data-stu-id="f663b-197">This operation generates and prints an X report for the current active shift.</span></span>

### <a name="reprint-z"></a><span data-ttu-id="f663b-198">再印刷 Z</span><span class="sxs-lookup"><span data-stu-id="f663b-198">Reprint Z</span></span>

<span data-ttu-id="f663b-199">この操作は、シフトがクローズされた際にシステムが最後に生成した Z レポートを再印刷します。</span><span class="sxs-lookup"><span data-stu-id="f663b-199">This operation reprints the last Z report that the system generated when a shift was closed.</span></span>

### <a name="manage-shifts"></a><span data-ttu-id="f663b-200">シフトを管理する</span><span class="sxs-lookup"><span data-stu-id="f663b-200">Manage shifts</span></span>

<span data-ttu-id="f663b-201">この操作により、ユーザーは店舗のすべての有効、中断、およびブラインド クローズされたシフトを表示できます。</span><span class="sxs-lookup"><span data-stu-id="f663b-201">This operation lets users view all active, suspended, and blind-closed shifts for the store.</span></span> <span data-ttu-id="f663b-202">アクセス許可に応じて、ユーザーはブラインド クローズ済シフトの支払/入金申告およびシフトのクローズ操作などの最終決算手続きを実行できます。</span><span class="sxs-lookup"><span data-stu-id="f663b-202">Depending on their permissions, users can perform their final closing procedures, such as Tender declaration and Close shift operations for blind-closed shifts.</span></span> <span data-ttu-id="f663b-203">この操作により、オフライン モードとオンライン モードの切り替え後にシフトが不適切な状態のままになっているまれなイベントの際に、無効なシフトの表示および削除もできるようになります。</span><span class="sxs-lookup"><span data-stu-id="f663b-203">This operation also lets users view and delete invalid shifts, in the rare event that shifts are left in a bad state after a switch between offline and online modes.</span></span> <span data-ttu-id="f663b-204">これらの無効なシフトには、調整に必要とされる財務情報またはトランザクション データは含まれません。</span><span class="sxs-lookup"><span data-stu-id="f663b-204">These invalid shifts don't contain any financial information or transactional data that is required for reconciliation.</span></span>

## <a name="shift-and-drawer-permissions"></a><span data-ttu-id="f663b-205">シフトとドロワーのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="f663b-205">Shift and drawer permissions</span></span>

<span data-ttu-id="f663b-206">次の POS のアクセス許可は、さまざまなシナリオにおいてユーザーが行えることと行えないことに影響します。</span><span class="sxs-lookup"><span data-stu-id="f663b-206">The following POS permissions affect what a user can and can't do in various scenarios:</span></span>

- <span data-ttu-id="f663b-207">**ブラインド クローズを許可**</span><span class="sxs-lookup"><span data-stu-id="f663b-207">**Allow blind close**</span></span>
- <span data-ttu-id="f663b-208">**X レポートの印刷を許可する**</span><span class="sxs-lookup"><span data-stu-id="f663b-208">**Allow X-report printing**</span></span>
- <span data-ttu-id="f663b-209">**Z レポートの印刷を許可**</span><span class="sxs-lookup"><span data-stu-id="f663b-209">**Allow Z-report printing**</span></span>
- <span data-ttu-id="f663b-210">**支払/入金申告を許可する**</span><span class="sxs-lookup"><span data-stu-id="f663b-210">**Allow tender declaration**</span></span>
- <span data-ttu-id="f663b-211">**釣銭申告を許可する**</span><span class="sxs-lookup"><span data-stu-id="f663b-211">**Allow floating declaration**</span></span>
- <span data-ttu-id="f663b-212">**販売なしでドロワーを開く**</span><span class="sxs-lookup"><span data-stu-id="f663b-212">**Open drawer without sale**</span></span>
- <span data-ttu-id="f663b-213">**複数シフト ログオンを許可** – このアクセス許可により、ユーザーはサインインして、異なるユーザーが開始したシフトを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f663b-213">**Allow multiple shift logon** – This permission allows the user to sign in to and use a shift that a different user opened.</span></span> <span data-ttu-id="f663b-214">このアクセス許可を持たないユーザーはサインインすると、自分で開いたシフトのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f663b-214">Users who don't have this permission can sign in to and use only shifts that they have opened.</span></span>
- <span data-ttu-id="f663b-215">**共有シフトの管理を許可** – ユーザーは共有シフトを開く、または閉じるのにこのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="f663b-215">**Allow manage shared shift** – Users must have this permission to open or close a shared shift.</span></span>
- <span data-ttu-id="f663b-216">**共有シフトの使用を許可** – ユーザーは共有シフトにサインインし使用するのに、このアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="f663b-216">**Allow use shared shift** – Users must have this permission to sign in to and use a shared shift.</span></span>

## <a name="back-office-end-of-day-considerations"></a><span data-ttu-id="f663b-217">バック オフィスの営業終了時の考慮事項</span><span class="sxs-lookup"><span data-stu-id="f663b-217">Back-office end-of-day considerations</span></span>

<span data-ttu-id="f663b-218">POS でシフトおよびキャッシュ ドロワーの調整が使用される方法は、明細書の計算中にトランザクション データが集計される方法とは異なります。</span><span class="sxs-lookup"><span data-stu-id="f663b-218">The way that shifts and cash drawer reconciliation are used in the POS differs from the way that transaction data is summarized during statement calculation.</span></span> <span data-ttu-id="f663b-219">この相違点を理解することは重要です。</span><span class="sxs-lookup"><span data-stu-id="f663b-219">It's important that you understand this difference.</span></span> <span data-ttu-id="f663b-220">コンフィギュレーションおよび業務プロセスに応じて、POS のシフト データ (Zレポート) およびバック オフィスで計算される明細書の結果は異なります。</span><span class="sxs-lookup"><span data-stu-id="f663b-220">Depending on your configuration and your business processes, the shift data in the POS (the Z report) and a calculated statement in the back office can give you different results.</span></span> <span data-ttu-id="f663b-221">この相違点は、必ずしもシフト データまたは計算された明細書のいずれかが正しくないこと、またはデータに問題があることを意味しているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="f663b-221">This difference doesn't necessarily mean that either the shift data or the calculated statement is incorrect, or that there is a problem with the data.</span></span> <span data-ttu-id="f663b-222">指定されたパラメーターが追加のトランザクションを含んでいる、またはトランザクションが少ないか、トランザクションが異なる方法で集計されたことを示しているだけです。</span><span class="sxs-lookup"><span data-stu-id="f663b-222">It just means that the parameters that are provided might be including additional transaction or fewer transactions, or that the transactions have been summarized differently.</span></span>

<span data-ttu-id="f663b-223">すべての小売業者には異なる業務要件がありますが、このタイプの差異が発生する状況を回避するため、次の方法でシステムを設定すること推奨します。</span><span class="sxs-lookup"><span data-stu-id="f663b-223">Although every retailer has different business requirements, we recommend that you set up your system in the following way to avoid situations where differences of this type occur:</span></span>

<span data-ttu-id="f663b-224">**小売 \> チャンネル \> 小売店舗 \> すべての小売店舗 \> 明細書/決済**に移動し、各店舗に**明細書の方法**フィールドおよび**決済方法**フィールドの両方を**シフト**に設定します。</span><span class="sxs-lookup"><span data-stu-id="f663b-224">Go to **Retail \> Channels \> Retail stores \> All retail stores \> Statement/closing**, and for each store, set both the **Statement method** field and the **Closing method** field to **Shift**.</span></span>

<span data-ttu-id="f663b-225">この設定により、バック オフィスの明細書が POS のシフトと同じトランザクションを含み、データがそのシフトごとに集計されていることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="f663b-225">This setup helps guarantee that back-office statements include the same transactions as shifts in the POS, and that the data is summarized by that shift.</span></span>

<span data-ttu-id="f663b-226">明細書および決済方法の詳細については、[小売明細書の店舗のコンフィギュレーション](https://docs.microsoft.com/dynamics365/unified-operations/retail/tasks/store-configurations-retail-statements) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f663b-226">For more information about statement and closing methods, see [Store configurations for Retail statement](https://docs.microsoft.com/dynamics365/unified-operations/retail/tasks/store-configurations-retail-statements).</span></span>

