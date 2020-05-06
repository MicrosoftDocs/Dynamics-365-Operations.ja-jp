---
title: 受給時の支払仕入先支払の設定と使用
description: このトピックでは、受給時の支払 (PWP) 条件を作成して、顧客支払に基づいて一部の仕入先支払をリリースする方法について説明します。
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 390cec62d2790ed10892669e283f2283c6b8e686
ms.sourcegitcommit: 399f128d90b71bd836a1c8c0c8c257b7f9eeb39a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284116"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a><span data-ttu-id="7df06-103">受給時の支払仕入先支払の設定と使用</span><span class="sxs-lookup"><span data-stu-id="7df06-103">Set up and use pay-when-paid vendor payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7df06-104">仕入先を協力会社としてプロジェクトの作業を承認するとき、プロジェクトの顧客が支払うまで仕入先や協力会社への支払を留保したい場合があります。</span><span class="sxs-lookup"><span data-stu-id="7df06-104">When you approve a vendor to work as a subcontractor, you might want to withhold payment to the vendor until your customer pays you for the project.</span></span> <span data-ttu-id="7df06-105">このシナリオをサポートするためには、仕入先への発注書 (PO) を設定するときに受給時の支払 (PWP) 条件を設定します。</span><span class="sxs-lookup"><span data-stu-id="7df06-105">To support this scenario, you can set up pay-when-paid (PWP) terms when you set up the purchase order (PO) with the vendor.</span></span>

<span data-ttu-id="7df06-106">たとえば、顧客がプロジェクト請求書の金額を支払うと、支払に関連する仕入先請求書金額の一部またはすべてをリリースできます。</span><span class="sxs-lookup"><span data-stu-id="7df06-106">For example, when a customer pays an amount on a project invoice, you can release some or all of the vendor invoice amount.</span></span> <span data-ttu-id="7df06-107">顧客から関連する支払のある割合を受け取ってから、仕入先への支払を指定する PWP 条件を設定できます。</span><span class="sxs-lookup"><span data-stu-id="7df06-107">Just set up PWP terms that specify that the vendor will be paid after you receive a percentage of the related payment from the customer.</span></span> <span data-ttu-id="7df06-108">顧客から一部の支払を受け取ると、支払に関連する仕入先請求書の一部を手動でリリースできます。</span><span class="sxs-lookup"><span data-stu-id="7df06-108">If you receive partial payment from a customer, you can manually release some of the related vendor invoices for payment.</span></span>

<span data-ttu-id="7df06-109">次の例は、PWP 条件が使用された場合のプロセスを示しています。</span><span class="sxs-lookup"><span data-stu-id="7df06-109">The following example outlines the process when PWP terms are used.</span></span>

## <a name="example"></a><span data-ttu-id="7df06-110">例</span><span class="sxs-lookup"><span data-stu-id="7df06-110">Example</span></span>

<span data-ttu-id="7df06-111">あなたの組織では、顧客にソフトウェアがインストールされた 100 台のコンピューターを、コンピューターあたり 150.00 米ドル (USD) の価格で提供することに合意しています。</span><span class="sxs-lookup"><span data-stu-id="7df06-111">Your organization agrees to provide a customer with 100 computers that have software installed, for a price of 150.00 US dollars (USD) per computer.</span></span> <span data-ttu-id="7df06-112">次に、ソフトウェアがインストールされているコンピュータを提供してもらう仕入先を採用します。</span><span class="sxs-lookup"><span data-stu-id="7df06-112">You then hire a vendor to provide you with the computers that have software installed.</span></span> <span data-ttu-id="7df06-113">この合意によると、顧客は貴社に支払をおこなう前に、コンピュータの品質を承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7df06-113">According to the agreement, the customer must approve the quality of the computers before it pays your organization.</span></span> <span data-ttu-id="7df06-114">貴社ポリシーでは、顧客からの支払を受けるまで仕入先への支払を保留します。</span><span class="sxs-lookup"><span data-stu-id="7df06-114">Your organization's policy is to withhold payment to vendors until the customer has paid you.</span></span> <span data-ttu-id="7df06-115">したがって、100 パーセントの PWP 割合を持つようにプロジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="7df06-115">Therefore, you set up the project so that it has a PWP percentage of 100 percent.</span></span>

<span data-ttu-id="7df06-116">この仕入先から、ソフトウェアがインストールされている 100 台のコンピューターと、10,000.00 米ドルの請求書がユーザーに送信されます。</span><span class="sxs-lookup"><span data-stu-id="7df06-116">The vendor sends you the 100 computers that have software installed, together with an invoice for 10,000.00 USD.</span></span> <span data-ttu-id="7df06-117">PWP 条件はプロジェクトに対して設定されているため、コンピューターの入荷時に仕入先に支払はおこないません。</span><span class="sxs-lookup"><span data-stu-id="7df06-117">Because PWP terms are set up for your project, you don't pay the vendor upon receipt of the computers.</span></span> <span data-ttu-id="7df06-118">その代わりに、15,000.00 ドルの請求書と共に、コンピューターを顧客に発送します。</span><span class="sxs-lookup"><span data-stu-id="7df06-118">Instead, you send the computers to the customer, together with an invoice for 15,000.00.</span></span> <span data-ttu-id="7df06-119">顧客はコンピューターを検査して、プロジェクト請求書の全額を承認します。</span><span class="sxs-lookup"><span data-stu-id="7df06-119">The customer inspects the computers and approves the full amount of the project invoice.</span></span>

<span data-ttu-id="7df06-120">顧客から全額の支払を受け取った後、仕入先に仕入先請求書の全額の 10,000.00 ドルを支払います。</span><span class="sxs-lookup"><span data-stu-id="7df06-120">After you receive the full payment from the customer, you pay the vendor 10,000.00, the full amount of the vendor invoice.</span></span>

## <a name="set-up-pwp-terms-for-a-project"></a><span data-ttu-id="7df06-121">プロジェクトに PWP 条件を設定する</span><span class="sxs-lookup"><span data-stu-id="7df06-121">Set up PWP terms for a project</span></span>

<span data-ttu-id="7df06-122">プロジェクトの PWP 条件を設定する場合は、仕入先への支払を行う前に顧客がプロジェクトに対して支払う必要のある最低額を割合で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7df06-122">When you set up PWP terms for a project, you must specify, as a percentage, the minimum amount that a customer must pay you for the project before you will pay the vendor.</span></span> <span data-ttu-id="7df06-123">このしきい値の金額は、プロジェクトに対して作成される顧客請求書で自動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="7df06-123">The threshold amount is automatically calculated on the customer invoices for the project.</span></span> <span data-ttu-id="7df06-124">PWP 条件のしきい値の割合を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7df06-124">Follow these steps to set up the threshold percentage for PWP terms.</span></span>

1. <span data-ttu-id="7df06-125">**プロジェクト管理および会計** \> **プロジェクト** \> **すべてのプロジェクト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7df06-125">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="7df06-126">PWP 条件を設定するプロジェクトを検索して開きます。</span><span class="sxs-lookup"><span data-stu-id="7df06-126">Find and open the project that you want to set up PWP terms for.</span></span>
3. <span data-ttu-id="7df06-127">**仕入先契約** クイック タブで、**行の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7df06-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="7df06-128">**[口座コード]** フィールドで、次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="7df06-128">In the **Account code** field, select one of the following options:</span></span>

    - <span data-ttu-id="7df06-129">**テーブル** - PWP 条件は、1 つの仕入先に適用されます。</span><span class="sxs-lookup"><span data-stu-id="7df06-129">**Table** – The PWP terms apply to a single vendor.</span></span>
    - <span data-ttu-id="7df06-130">**グループ** ‐ PWP 条件は、仕入先グループ内のすべての仕入先に適用されます。</span><span class="sxs-lookup"><span data-stu-id="7df06-130">**Group** – The PWP terms apply to all vendors in a vendor group.</span></span>
    - <span data-ttu-id="7df06-131">**すべて** - PWP 条件は、すべての仕入先に適用されます。</span><span class="sxs-lookup"><span data-stu-id="7df06-131">**All** – The PWP terms apply to all vendors.</span></span>

4. <span data-ttu-id="7df06-132">前の手順で **テーブル** または **グループ** を選択した場合、**仕入先/仕入先グループ** フィールドで、PWP 条件が適用される仕入先または仕入先グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="7df06-132">If you selected **Table** or **Group** in the previous step, in the **Vendor/Vendor group** field, select the vendor or vendor group that the PWP terms apply to.</span></span> <span data-ttu-id="7df06-133">前の手順で **すべて** を選択した場合、**仕入先/仕入先グループ** フィールドは編集できません。</span><span class="sxs-lookup"><span data-stu-id="7df06-133">If you selected **All** in the previous step, the **Vendor/Vendor group** field can't be edited.</span></span>
5. <span data-ttu-id="7df06-134">また、プロジェクトで、仕入先の留保条件が  **仕入先留保条件** フィールドで設定されている場合は、留保条件のルール IDを選択します。</span><span class="sxs-lookup"><span data-stu-id="7df06-134">If vendor retention terms are set up for the vendor in the project, in the **Vendor retention terms** field, select the rule ID for the retention terms.</span></span>
6. <span data-ttu-id="7df06-135">**[PWP しきい値の割合]** フィールドに、プロジェクトのしきい値の割合を入力します。</span><span class="sxs-lookup"><span data-stu-id="7df06-135">In the **PWP threshold percentage** field, enter the threshold percentage for the project.</span></span> <span data-ttu-id="7df06-136">プロジェクトに対して入力する割合によって、仕入先へ支払う前に顧客が支払う必要がある最低金額が設定されます。</span><span class="sxs-lookup"><span data-stu-id="7df06-136">The percentage that you enter for the project defines the minimum amount that the customer must pay you before you will pay the vendor.</span></span>

## <a name="create-a-po-that-has-pwp-terms"></a><span data-ttu-id="7df06-137">PWP 条件を含む PO の作成</span><span class="sxs-lookup"><span data-stu-id="7df06-137">Create a PO that has PWP terms</span></span>

<span data-ttu-id="7df06-138">仕入先からの請求書を転記するとき、その仕入先が PWP 条件の対象の場合、その条件が PO の明細行に表示されます。</span><span class="sxs-lookup"><span data-stu-id="7df06-138">When you post an invoice from a vendor, if the vendor is subject to PWP terms, those terms are shown on the PO lines.</span></span> <span data-ttu-id="7df06-139">PWP 条件を持つ PO を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7df06-139">To create a PO that has PWP terms, follow these steps.</span></span>

1. <span data-ttu-id="7df06-140">**調達** \> **発注書** \> **すべての発注書** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7df06-140">Go to **Procurement and sourcing** \> **Purchase orders** \> **All purchase orders**.</span></span>
2. <span data-ttu-id="7df06-141">アクション ウィンドウで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7df06-141">On the Action Pane, select **New**.</span></span> <span data-ttu-id="7df06-142">次に、**発注書の作成** ダイアログボックスで、必要な情報を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7df06-142">Then, in the **Create purchase order** dialog box, enter the required information, and select **OK**.</span></span>

    <span data-ttu-id="7df06-143">または、**すべての発注書"** 一覧ページで既存の PO を開きます。</span><span class="sxs-lookup"><span data-stu-id="7df06-143">Alternatively, open an existing PO on the **All purchase orders** list page.</span></span>

4. <span data-ttu-id="7df06-144">**発注書** ページで、**発注書の明細行** クイック タブで、その仕入先の PO 明細行の詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="7df06-144">On the **Purchase order** page, on the **Purchase order lines** FastTab, review the details of the PO line for the vendor.</span></span> <span data-ttu-id="7df06-145">**受給時に支払** オプションが自動的に選択され、**PWP しきい値割合** フィールドが **プロジェクト** ページの **PWP しきい値割合** フィールドから自動的にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="7df06-145">The **Pay when paid** option is automatically selected, and the value in the **PWP threshold percentage** field is automatically copied from the **PWP threshold percentage** field on the **Projects** page.</span></span>
6. <span data-ttu-id="7df06-146">PO 明細行の仕入先に PWP 条件を適用しない場合は、**受給時に支払** オプションをオフにします。</span><span class="sxs-lookup"><span data-stu-id="7df06-146">If you don't want to apply PWP terms to the vendor for a PO line, clear the **Pay when paid** option.</span></span> <span data-ttu-id="7df06-147">この場合、PO 明細行の **PWP しきい値割合** フィールドは、0 (ゼロ) にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="7df06-147">In this case, the **PWP threshold percentage** field for the PO line will be reset to 0 (zero).</span></span>

## <a name="update-a-customer-payment-and-pay-the-vendor"></a><span data-ttu-id="7df06-148">顧客支払情報の更新および仕入先への支払の更新</span><span class="sxs-lookup"><span data-stu-id="7df06-148">Update a customer payment and pay the vendor</span></span>

<span data-ttu-id="7df06-149">仕入先がプロジェクトの作業を完了し、請求書を送付してきた場合、プロジェクトの状態と顧客請求書を精査してプロジェクトが PWP 条件を満たしているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="7df06-149">When a vendor completes its work on a project and sends you an invoice, you must review the project status and customer invoices to determine whether the PWP terms have been met for the project.</span></span> <span data-ttu-id="7df06-150">仕入先の PWP 条件が満たされている場合は、プロジェクトの顧客支払に基づいて、支払の対象となる仕入先請求書の明細行を決定できます。</span><span class="sxs-lookup"><span data-stu-id="7df06-150">If the PWP terms for the vendor were met, you can determine which lines on the vendor invoice to pay, based on the customer payments for the project.</span></span> <span data-ttu-id="7df06-151">PWP 条件が満たされなくても仕入先に支払うことにした場合は、**受給時に支払の仕入先請求書** ページで PWP 条件を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="7df06-151">If you decide to pay the vendor even though the PWP terms weren't met, you can override the PWP terms on the **Vendor invoice with pay when paid** page.</span></span>

1. <span data-ttu-id="7df06-152">**プロジェクト管理および会計** \> **照会およびレポート** \> **保管の照会** \> **受給時に支払の仕入先請求書** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7df06-152">Go to **Project management and accounting** \> **Inquiries and reports** \> **Retention inquiries** \> **Vendor invoice with pay when paid**.</span></span>
2. <span data-ttu-id="7df06-153">**受給時に支払の仕入先請求書** ページで、確認対象の仕入先請求書を検索するためのフィルタ値を入力し、**検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7df06-153">On the **Vendor invoices with pay when paid** page, in the search field, enter values to find the vendor invoice that you want to review, and then select **Search**.</span></span>
3. <span data-ttu-id="7df06-154">**仕入先請求書の明細行** クイック タブで、変更する明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="7df06-154">On the **Vendor invoice lines** FastTab, select the lines that you want to change.</span></span>
4. <span data-ttu-id="7df06-155">請求明細行に対して **受給時の支払** 条件が満たされた場合、**仕入先支払のリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7df06-155">If the **Pay when paid** conditions are met for the invoice line, select **Release vendor payment**.</span></span> <span data-ttu-id="7df06-156">この **受給時の支払** オプションがオフで、**支払の準備完了** フィールドの値が **はい** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="7df06-156">The **Pay when paid** option is cleared, and the value of the **Ready for payment** field is changed to **Yes**.</span></span>
