---
title: 支払請求書の作成
description: このトピックでは、月次リースの請求書を作成する方法を説明します。 個々のリースに対する請求書の作成や、バッチ プロセスを使用して複数のリースに対して請求書を作成することもできます。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 32618814d00cb1e1f1082169a64b187cce1e76b4
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445374"
---
# <a name="create-payment-invoices"></a><span data-ttu-id="e89a9-104">支払請求書の作成</span><span class="sxs-lookup"><span data-stu-id="e89a9-104">Create payment invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e89a9-105">月次のリースに対する請求書の作成や、バッチ プロセスを使用して複数のリースに対して請求書を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="e89a9-105">You can create monthly invoices for individual leases, or you can use a batch process to create them for multiple leases.</span></span> <span data-ttu-id="e89a9-106">以下の手順では、**リース帳簿の設定** ページで **仕入先への支払い** パラメーターをオンにした場合に、個々のリース支払項目を作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="e89a9-106">The following procedure shows how to create an individual lease payment entry when the **Pay to Vendor** parameter on the **Lease book setup** page is turned on.</span></span>

1. <span data-ttu-id="e89a9-107">**リースの概要** ページで、リースを選択し、**帳簿 \> 支払スケジュール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e89a9-107">On the **Lease summary** page, select a lease, and then select **Books \> Payment schedule**.</span></span>
2. <span data-ttu-id="e89a9-108">実行する必要がある支払を選択し、**仕訳の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e89a9-108">Select the payment that must be made, and then select **Create journal**.</span></span> <span data-ttu-id="e89a9-109">選択した支払に対して仕訳が作成されたことを示すメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e89a9-109">You receive a message that states that a journal was created against the selected payment.</span></span>
3. <span data-ttu-id="e89a9-110">**請求書の仕訳** を選択し、支払を行う必要がある請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="e89a9-110">Select **Invoice journals**, and then select the invoice that must be paid.</span></span>
4. <span data-ttu-id="e89a9-111">**明細行** タブで、仕訳入力を一般会計に転記する前に確認します。</span><span class="sxs-lookup"><span data-stu-id="e89a9-111">On the **Lines** tab, review the journal entry before you post it to the general ledger.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e89a9-112">既定では、作成された仕入先請求書の明細行では、**買掛金勘定パラメーター** ページの仕入先転記プロファイルが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e89a9-112">By default, the vendor invoice lines that are created use the vendor posting profile from the **Accounts payable parameters** page.</span></span>

5. <span data-ttu-id="e89a9-113">適切な仕訳 を選択し、支払を行う必要がある請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="e89a9-113">Select the correct journal, and then select the invoice that must be paid.</span></span>

    <span data-ttu-id="e89a9-114">この例では、リース帳簿の **仕入先への支払** パラメーターがオンになっています。</span><span class="sxs-lookup"><span data-stu-id="e89a9-114">For this example, the **Pay to Vendor** parameter on the lease book is turned on.</span></span> <span data-ttu-id="e89a9-115">したがって、請求書は請求書の仕訳に含まれます。</span><span class="sxs-lookup"><span data-stu-id="e89a9-115">Therefore, the invoice will be in the invoice journal.</span></span> <span data-ttu-id="e89a9-116">**概要** セクションには仕訳入力の概要が表示され、**明細行** セクションには実際の仕訳帳明細行の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e89a9-116">The **Overview** section shows a summary of the journal entry, and the **Lines** section shows details of the actual journal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e89a9-117">**仕入先への支払** パラメーターがオフになっている場合は、支払仕訳入力がリース帳簿の **資産リース** ページに一覧表示され、請求書の代わりにシステムによって資産リースの入力が作成されます。</span><span class="sxs-lookup"><span data-stu-id="e89a9-117">If the **Pay to Vendor** parameter is turned off, payment journal entries will be listed on the **Asset leasing** page for the lease book, and the system will create an asset leasing entry instead of an invoice.</span></span> <span data-ttu-id="e89a9-118">**月々のリース仕訳** フィールドに指定されている仕訳帳名に、リース支払の入力が転記され ます。</span><span class="sxs-lookup"><span data-stu-id="e89a9-118">The lease payment entry will be posted to the journal name that is specified in the **Monthly lease journal** field.</span></span>

6. <span data-ttu-id="e89a9-119">トランザクションが転記された後は、 リース帳簿の **負債トランザクション** を選択すると、取引情報やリース負債の帳簿価額を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="e89a9-119">After the transaction is posted, you can view the transaction information and the carrying value of the lease liability by selecting **Liability transactions** in the lease book.</span></span>

    <span data-ttu-id="e89a9-120">支払スケジュールで、**転記済仕訳帳** チェック ボックスがオンになり、明細行に請求仕訳帳番号が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e89a9-120">In the payment schedule, the **Journal posted** check box will be selected, and the line will show the invoice journal number.</span></span> <span data-ttu-id="e89a9-121">支払仕訳とその仕訳の入力が作成された後は、再作成する前に入力を取り消す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e89a9-121">After a payment journal and an entry for that journal have been created, you must reverse the entry before it can be re-created.</span></span>
