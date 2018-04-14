---
title: "集中支払の設定"
description: "ある 1 つの法人で組織内の他の法人に代わって支払を処理するように準備するには、次の手順に従います。"
author: kweekley
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fd6f32e266dcbd78c464e42da50a347bea39fcfc
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-centralized-payments"></a><span data-ttu-id="6c1df-103">集中支払の設定</span><span class="sxs-lookup"><span data-stu-id="6c1df-103">Set up centralized payments</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="6c1df-104">ある 1 つの法人で組織内の他の法人に代わって支払を処理するように準備するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6c1df-104">Follow these steps to prepare to process payments in one legal entity on behalf of other legal entities in your organization.</span></span> <span data-ttu-id="6c1df-105">始める前に、次の設定を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c1df-105">Before you begin, the following setup must be completed:</span></span>

-   <span data-ttu-id="6c1df-106">法人を作成します。</span><span class="sxs-lookup"><span data-stu-id="6c1df-106">Create legal entities.</span></span>
-   <span data-ttu-id="6c1df-107">総勘定元帳パラメーターおよび勘定科目表を設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1df-107">Set up General ledger parameters and charts of accounts.</span></span>
-   <span data-ttu-id="6c1df-108">買掛金勘定パラメーターおよび売掛金勘定パラメータ (集中支払を使用するモジュールに応じて) を設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1df-108">Set up Accounts payable parameters and Accounts receivable parameters (depending on the modules that are using centralized payments).</span></span>
-   <span data-ttu-id="6c1df-109">会社間勘定を設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1df-109">Set up intercompany accounting.</span></span>

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a><span data-ttu-id="6c1df-110">集中支払用の組織階層の設定</span><span class="sxs-lookup"><span data-stu-id="6c1df-110">Set up an organizational hierarchy for centralized payments</span></span>
<span data-ttu-id="6c1df-111">集中支払用の組織階層を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c1df-111">You must set up an organizational hierarchy for centralized payments.</span></span> <span data-ttu-id="6c1df-112">同一の組織階層を使用して、集中仕入先支払と集中顧客支払を処理できます。</span><span class="sxs-lookup"><span data-stu-id="6c1df-112">The same organizational hierarchy is used to process centralized vendor payments and centralized customer payments.</span></span> <span data-ttu-id="6c1df-113">**注:** 集中支払では、階層の構造は重要ではありません。</span><span class="sxs-lookup"><span data-stu-id="6c1df-113">**Note:** For centralized payments, the structure of the hierarchy doesn't matter.</span></span> <span data-ttu-id="6c1df-114">階層内のすべての法人が、階層内のその他の任意の法人に代わって、支払を処理できます。</span><span class="sxs-lookup"><span data-stu-id="6c1df-114">Any legal entity in the hierarchy will be able to process payments on behalf of any other legal entity in the hierarchy.</span></span> <span data-ttu-id="6c1df-115">**組織階層** ページで、新しい組織階層を作成できます。</span><span class="sxs-lookup"><span data-stu-id="6c1df-115">On the **Organization hierarchies** page, you can create a new organization hierarchy.</span></span> <span data-ttu-id="6c1df-116">[**目的**] フィールドで、[**集中支払**] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c1df-116">In the **Purpose** field, you must select **Centralized payments**.</span></span> 

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a><span data-ttu-id="6c1df-117">集中支払用の会社間勘定の設定</span><span class="sxs-lookup"><span data-stu-id="6c1df-117">Set up an intercompany account for centralized payments</span></span>
<span data-ttu-id="6c1df-118">現在の法人の支払トランザクションが別の法人の請求書に対して決済される場合は、適切な借トランザクションと貸トランザクションが法人ごとに作成されます。</span><span class="sxs-lookup"><span data-stu-id="6c1df-118">When payment transactions in the current legal entity are settled against invoices in other legal entities, the appropriate due-to and due-from transactions are created for each legal entity.</span></span> <span data-ttu-id="6c1df-119">現金割引、実現利益、または実現損失が転記される法人を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c1df-119">You must specify the legal entity where any applicable cash discounts and realized gain or loss amounts are posted.</span></span> <span data-ttu-id="6c1df-120">始める前に、仕入先と顧客支払の処理に使用する法人を決定します。</span><span class="sxs-lookup"><span data-stu-id="6c1df-120">Before you begin, decide which legal entity you will use to process vendor and customer payments.</span></span> <span data-ttu-id="6c1df-121">1 つの法人が仕入先支払を処理する場合に、別の法人が顧客支払を処理すると、それぞれの法人を切り替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c1df-121">If one legal entity processes vendor payments but another legal entity processes customer payments, you will have to switch to each legal entity.</span></span> <span data-ttu-id="6c1df-122">[**会社間会計**] ページで、代わりに支払を処理する法人の会社間関係レコードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="6c1df-122">On the **Intercompany accounting** page, you can select an intercompany relationship record for a legal entity that you will process payments on behalf of.</span></span> 

<span data-ttu-id="6c1df-123">[**集中支払**] タブで、現金割引の支払法人への転記 (または仕入先勘定の残高を減額するその他のトランザクション)、または請求法人への転記 (または仕入先勘定の残高を増額するその他のトランザクション) のいずれを行うかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="6c1df-123">On the **Centralized payments** tab, you can select whether to post cash discounts to the legal entity of the payment (or other transaction that decreases the balance of the vendor account) or the legal entity of the invoice (or other transaction that increases the balance of the vendor account).</span></span> <span data-ttu-id="6c1df-124">この選択は、**買掛金勘定パラメータ** ページと **売掛金勘定パラメータ** ページの [**現金割引管理**] フィールドと共に使用します。</span><span class="sxs-lookup"><span data-stu-id="6c1df-124">This selection works together with the **Cash discount administration** field on the **Accounts payable parameters** and **Accounts receivable parameters** pages.</span></span> <span data-ttu-id="6c1df-125">過剰支払と少額の許容誤差については、支払の法人の設定が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6c1df-125">For overpayments and penny difference tolerances, the setting in the legal entity of the payment is used.</span></span> <span data-ttu-id="6c1df-126">過少支払と少額の許容誤差については、請求書の法人の設定が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6c1df-126">For underpayments and penny difference tolerances, the setting in the legal entity of the invoice is used.</span></span>

## <a name="map-vendor-accounts-across-legal-entities"></a><span data-ttu-id="6c1df-127">法人間での仕入先勘定のマッピング</span><span class="sxs-lookup"><span data-stu-id="6c1df-127">Map vendor accounts across legal entities</span></span>
<span data-ttu-id="6c1df-128">ある法人から仕入先に支払を行っているときに、その仕入先の請求書を別の法人で選択する場合は、該当する仕入先勘定が、各法人ですべて同じアドレス帳 ID を使用していることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c1df-128">If you pay a vendor from one legal entity and want to select invoices for that vendor in other legal entities, you must make sure that all the corresponding vendor accounts in each legal entity use the same address book ID.</span></span> <span data-ttu-id="6c1df-129">複数の法人で請求書を支払う顧客から支払を受け取る場合、該当する顧客勘定がすべての法人で同じアドレス ブック ID を使用していることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c1df-129">If you receive a payment from a customer that pays invoices in more than one legal entity, you must make sure that all the corresponding customer accounts in each legal entity use the same address book ID.</span></span>

## <a name="set-up-posting-profiles-for-centralized-payments"></a><span data-ttu-id="6c1df-130">集中支払用の転記プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="6c1df-130">Set up posting profiles for centralized payments</span></span>
<span data-ttu-id="6c1df-131">ある法人の中で、他の法人の請求書を決済する支払を作成する場合は、両方の法人の転記プロファイル ID が同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c1df-131">When you create a payment in one legal entity that settles invoices in other legal entities, the posting profile IDs must be the same in both legal entities.</span></span> <span data-ttu-id="6c1df-132">支払が正常に作成されることを保証するために、支払の法人で使用されている転記プロファイルに対応する転記プロファイルを、各請求法人に設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1df-132">To help guarantee that payments are created correctly, in each legal entity of the invoice, set up a posting profile that corresponds to the posting profiles that are used in the legal entity of the payment.</span></span> <span data-ttu-id="6c1df-133">最初の請求書の法人に切り替えてから、[**仕入先転記プロファイル**] ページで、新しい転記プロファイルを作成するか、または既存の転記プロファイルを編集できます。</span><span class="sxs-lookup"><span data-stu-id="6c1df-133">Switch to the first legal entity of the invoice, and then, on the **Vendor posting profiles** page, you can create a new posting profile or edit an existing posting profile.</span></span> <span data-ttu-id="6c1df-134">請求書の法人の転記プロファイルで行う選択は、支払の法人に設定された転記プロファイルに一致させる必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6c1df-134">The selections that you make for the posting profile in the legal entity of the invoice don't have to match the setup of the posting profile in the legal entity of the payment.</span></span>

## <a name="set-up-methods-of-payment-for-centralized-payments"></a><span data-ttu-id="6c1df-135">集中支払用の支払方法の設定</span><span class="sxs-lookup"><span data-stu-id="6c1df-135">Set up methods of payment for centralized payments</span></span>
<span data-ttu-id="6c1df-136">ある法人の中で、他の法人の請求書を決済する支払を作成する場合は、両方の法人の支払方法 ID が同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c1df-136">When you create a payment in one legal entity that settles invoices in other legal entities, the method of payment IDs must be the same in both legal entities.</span></span> <span data-ttu-id="6c1df-137">支払が正常に作成されることを保証するために、支払の法人で使用されている支払方法に対応する支払方法を、請求書の各法人に設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1df-137">To help guarantee that payments are created correctly, in each legal entity of the invoice, set up a method of payment that corresponds to the methods of payment that are used in the legal entity of the payment.</span></span> <span data-ttu-id="6c1df-138">最初の請求書の法人に切り替えてから、**支払方法** ページで、新しい支払方法を作成するか、または既存の支払方法を編集できます。</span><span class="sxs-lookup"><span data-stu-id="6c1df-138">Switch to the first legal entity of the invoice, and then, on the **Methods of payment** page, you can create a new method of payment or edit an existing method of payment.</span></span> <span data-ttu-id="6c1df-139">請求書の法人の支払方法で行う選択は、支払の法人に設定された支払方法の設定方法と一致させる必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6c1df-139">The selections that you make for the method of payment in the legal entity of the invoice don't have to match the setup of the method of payment in the legal entity of the payment.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="6c1df-140">既定の説明を設定</span><span class="sxs-lookup"><span data-stu-id="6c1df-140">Set up default descriptions</span></span>
<span data-ttu-id="6c1df-141">会社間決済伝票用の既定の説明を定義できます。</span><span class="sxs-lookup"><span data-stu-id="6c1df-141">You can define default descriptions for intercompany settlement vouchers.</span></span> <span data-ttu-id="6c1df-142">この既定の説明は、会社間決済プロセス中の借トランザクションと貸トランザクションに含まれます。</span><span class="sxs-lookup"><span data-stu-id="6c1df-142">The default description is included on the due-to and due-from transactions during the cross-company settlement process.</span></span> <span data-ttu-id="6c1df-143">**既定の説明** ページで、言語を選択しテキストを入力することにより、[**会社間顧客決済**] および [**会社間仕入先決済**] の両方で新しい説明を作成できます。</span><span class="sxs-lookup"><span data-stu-id="6c1df-143">On the **Default descriptions** page, you can create new descriptions for both **Intercompany customer settlement** and **Intercompany vendor settlement** by selecting a language and then entering text.</span></span>




