---
title: 転記されたリース トランザクションの取消
description: このトピックでは、転記されたリース トランザクションを取り消す方法について説明します。 資産リースで作成されたすべてのトランザクションを取り消すことができます。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeaseTransactions
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 55eb7c5f2419bf1cb2ac0a33a82ab931a3ef380f
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881545"
---
# <a name="reverse-posted-lease-transactions"></a><span data-ttu-id="f221d-104">転記されたリース トランザクションの取消</span><span class="sxs-lookup"><span data-stu-id="f221d-104">Reverse posted lease transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f221d-105">資産リースで作成されたすべてのトランザクションを取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="f221d-105">Any transaction that is created through Asset leasing can be reversed.</span></span> <span data-ttu-id="f221d-106">資産リースで取り消されたトランザクションは、リース データを更新します。</span><span class="sxs-lookup"><span data-stu-id="f221d-106">Transactions that are reversed through Asset leasing update your lease data.</span></span> <span data-ttu-id="f221d-107">したがって、リース負債および使用権 (ROU) 資産のキャリー額も更新されます。</span><span class="sxs-lookup"><span data-stu-id="f221d-107">Therefore, they also update the carrying values of the lease liability and right-of-use (ROU) asset.</span></span>

<span data-ttu-id="f221d-108">リースのトランザクションを取り消すには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f221d-108">To create a reversing transaction for a lease, follow these steps.</span></span>

1. <span data-ttu-id="f221d-109">**資産トランザクション** ページまたは **負債トランザクション** ページでトランザクションを選択し、**トランザクションの取り消し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f221d-109">On either the **Asset transactions** page or the **Liability transactions** page, select the transaction, and then select **Reverse transaction**.</span></span>
2. <span data-ttu-id="f221d-110">表示されるダイアログ ボックスで、逆仕訳入力が転記される日付を編集できます。</span><span class="sxs-lookup"><span data-stu-id="f221d-110">In the dialog box that appears, you can edit the date when the reversing entry will be posted.</span></span> <span data-ttu-id="f221d-111">既定では、**日付** フィールドは、選択したトランザクションのトランザクション転記日付に設定されます。</span><span class="sxs-lookup"><span data-stu-id="f221d-111">By default, the **Date** field is set to the transaction posting date of the transaction that you selected.</span></span> <span data-ttu-id="f221d-112">逆仕訳入力は、選択されたトランザクションの元の転記日付よりも前に転記することはできません。</span><span class="sxs-lookup"><span data-stu-id="f221d-112">The reversing entry can't be posted earlier than the original posting date of the selected transaction.</span></span>
3. <span data-ttu-id="f221d-113">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f221d-113">Select **OK**.</span></span> <span data-ttu-id="f221d-114">仕訳入力は、選択した入力の取消を転記します。</span><span class="sxs-lookup"><span data-stu-id="f221d-114">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="f221d-115">取消は **資産トランザクション** または **負債トランザクション** ページに表示され、そのページにある現在の正味残高合計は更新済みです。</span><span class="sxs-lookup"><span data-stu-id="f221d-115">The reversal is shown on the **Asset transactions** or **Liability transactions** page, and the net total of the current balance that is shown on the page is updated.</span></span>

<span data-ttu-id="f221d-116">**追跡の取消** を選択すると、*追跡番号* と呼ばれるリンク番号と一緒に、ダイアログ ボックスに元のトランザクションと取り消されたトランザクションの両方が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f221d-116">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked number that is known as a *trace number*.</span></span> <span data-ttu-id="f221d-117">取消をわかりやすくし、可視性を向上させるために、リース スケジュールを使用して取消を追跡することもできます。</span><span class="sxs-lookup"><span data-stu-id="f221d-117">To make the reversals easier to understand and to improve visibility, you can also track reversals by using the lease schedules.</span></span>

<span data-ttu-id="f221d-118">**スケジュール** ページにある **最新の仕訳帳番号** フィールドに、トランザクションの仕訳帳番号が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f221d-118">The **Latest journal number** field on the **Schedule** page shows the journal numbers of transactions.</span></span> <span data-ttu-id="f221d-119">トランザクションが取り消されると、このフィールドは、取消トランザクションの仕訳帳番号で更新されます。</span><span class="sxs-lookup"><span data-stu-id="f221d-119">When a transaction is reversed, this field is updated with the journal number of a reversing transaction.</span></span> <span data-ttu-id="f221d-120">さらに、トランザクションの取り消しを意味する **取る消し済み** のチェック ボックスが選択され、**転記済み** フィールドが選択されます。</span><span class="sxs-lookup"><span data-stu-id="f221d-120">Additionally, the **Reversed** check box is selected to indicate that the transaction is reversed, and the **Posted** field is selected.</span></span>

## <a name="revoke-a-reversed-transaction"></a><span data-ttu-id="f221d-121">取り消されたトランザクションの破棄</span><span class="sxs-lookup"><span data-stu-id="f221d-121">Revoke a reversed transaction</span></span>

<span data-ttu-id="f221d-122">取り消されたトランザクションを破棄するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f221d-122">To revoke a reversed transaction, follow these steps.</span></span>

1. <span data-ttu-id="f221d-123">**スケジュール** ページまたは **トランザクション** ページで、元のトランザクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="f221d-123">On either the **Schedule** page or the **Transactions** page, select the original transaction.</span></span>
2. <span data-ttu-id="f221d-124">次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="f221d-124">Follow one of these steps:</span></span>

    - <span data-ttu-id="f221d-125">**スケジュール** ページで、 [トランザクション] を選択した場合は、[月次仕訳入力のバッチ作成](create-monthly-journals-batch.md) で仕訳帳の作成手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f221d-125">If you selected the transaction on the **Schedule** page, follow the steps for creating a journal in [Create monthly journal entries in a batch](create-monthly-journals-batch.md).</span></span> <span data-ttu-id="f221d-126">仕訳帳は手動で転記する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f221d-126">You must manually post the journal.</span></span>
    - <span data-ttu-id="f221d-127">**トランザクション** ページで [トランザクション] を選択した場合は **トランザクションの取消** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f221d-127">If you selected the transaction on the **Transactions** page, select **Reverse transaction**.</span></span> <span data-ttu-id="f221d-128">この破棄が以前の取消の破棄であることが記載されたメッセージが表示されます。また、この破棄の転記日付を編集することもできます。</span><span class="sxs-lookup"><span data-stu-id="f221d-128">You receive a message that states that this revocation is a revocation of an earlier reversal, and that you can edit the posting date for this revocation.</span></span> <span data-ttu-id="f221d-129">ただし、一般的な業務の検証は、 **日付** フィールドに入力された日付に影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="f221d-129">However, general business validations affect the dates that can be entered in the **Date** field.</span></span> 

3. <span data-ttu-id="f221d-130">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f221d-130">Select **OK**.</span></span> <span data-ttu-id="f221d-131">仕訳入力は、選択した入力の取消を転記します。</span><span class="sxs-lookup"><span data-stu-id="f221d-131">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="f221d-132">取消は **トランザクション** ページで表示され、現在の正味残高合計が最初の取消の前の金額に戻されます。</span><span class="sxs-lookup"><span data-stu-id="f221d-132">The reversal is shown on the **Transactions** page, and the net total current balance is restored to what it was before the first reversal.</span></span> <span data-ttu-id="f221d-133">したがって、残高に対する取消の影響は否定されます。</span><span class="sxs-lookup"><span data-stu-id="f221d-133">Therefore, the impact that the reversal had on the balances is negated.</span></span>

<span data-ttu-id="f221d-134">**追跡の取消** を選択すると、リンクされた追跡番号と一緒に、ダイアログ ボックスに元のトランザクションと取り消されたトランザクションの両方が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f221d-134">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked trace number.</span></span>

<span data-ttu-id="f221d-135">適切な **スケジュール** ページを使用すると、破棄を追跡することもできます。</span><span class="sxs-lookup"><span data-stu-id="f221d-135">You can also track revocations by using the appropriate **Schedules** page.</span></span> <span data-ttu-id="f221d-136">**取消** フィールドはクリアですが、**仕訳転記済** フィールドが選択されます。</span><span class="sxs-lookup"><span data-stu-id="f221d-136">The **Reverse** field is cleared, whereas the **Journal posted** field is selected.</span></span> <span data-ttu-id="f221d-137">さらに、**最新の仕訳帳番号** フィールドが破棄トランザクションの仕訳帳番号で更新され、**仕訳帳番号** フィールドが取消仕訳帳番号で更新されます。</span><span class="sxs-lookup"><span data-stu-id="f221d-137">Additionally, the **Latest journal number** field is updated with the journal number of the revocation transaction, and the **Journal number** field is updated with the reversal journal number.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
