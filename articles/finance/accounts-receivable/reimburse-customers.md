---
title: 顧客への払戻し
description: この記事では、顧客グループの払い戻しトランザクションを作成する方法を説明します。 顧客に貸方残高がある場合、顧客に残高金額を払い戻すことができます。
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca087b5a39432eec6b2711cc4c4decf23932b611
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251124"
---
# <a name="reimburse-customers"></a><span data-ttu-id="1ddbf-104">顧客への払戻し</span><span class="sxs-lookup"><span data-stu-id="1ddbf-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ddbf-105">この記事では、顧客グループの払い戻しトランザクションを作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="1ddbf-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="1ddbf-106">顧客に貸方残高がある場合、顧客に残高金額を払い戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="1ddbf-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="1ddbf-107">次の表に、開始する前に準備が整っている必要のある前提条件を示します。</span><span class="sxs-lookup"><span data-stu-id="1ddbf-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="1ddbf-108">前提条件</span><span class="sxs-lookup"><span data-stu-id="1ddbf-108">Prerequisite</span></span>                                                            | <span data-ttu-id="1ddbf-109">説明</span><span class="sxs-lookup"><span data-stu-id="1ddbf-109">Description</span></span> |
|-------------------------------------------------------------------------|-------------|
| <span data-ttu-id="1ddbf-110">法人の最低払い戻し金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="1ddbf-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="1ddbf-111">**売掛金勘定パラメータ** ページで、**一般** エリアの **最低払い戻し金額** フィールドに、顧客の超過支払の場合に払い戻すことができる最低金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="1ddbf-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="1ddbf-112">オプション: 払い戻しを受けることができる各顧客に仕入先勘定を追加します。</span><span class="sxs-lookup"><span data-stu-id="1ddbf-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="1ddbf-113">**顧客** のページの **その他の詳細** クイック タブの **仕入先** フィールドで、顧客の仕入先勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="1ddbf-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span> |

<span data-ttu-id="1ddbf-114">払い戻しトランザクションを作成するとき、仕入先請求書が貸方残高金額に対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="1ddbf-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="1ddbf-115">払い戻し処理により、顧客口座の貸付残高が削除され、顧客に対応する仕入先の差引請求額が作成されます。</span><span class="sxs-lookup"><span data-stu-id="1ddbf-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1. <span data-ttu-id="1ddbf-116">売掛金勘定で、**払い戻し** プロセス (**売掛金勘定 \>定期処理タスク \> 払い戻し**) を実行します。</span><span class="sxs-lookup"><span data-stu-id="1ddbf-116">In Accounts receivable, run the **Reimbursement** process (**Accounts receivable \> Periodic tasks \> Reimbursement**).</span></span>
2. <span data-ttu-id="1ddbf-117">元帳分析コードに関係なくすべてのトランザクションをグループ化するには、**顧客の集計** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1ddbf-117">To group all transactions, regardless of ledger dimensions, set the **Summarize customer** option to **Yes**.</span></span> <span data-ttu-id="1ddbf-118">類似した元帳分析コードが設定されているトランザクションのみをグループ化するには、オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1ddbf-118">To group only transactions that have similar ledger dimensions, set the option to **No**.</span></span>
3. <span data-ttu-id="1ddbf-119">**未処理の借方トランザクションのある顧客を含める** を選択して、未決済の借方金額のある顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="1ddbf-119">Select **Include customers with outstanding debit transactions** to select customers who have unsettled debit amounts.</span></span>
4. <span data-ttu-id="1ddbf-120">特定の顧客勘定を払い戻すには、**含めるレコード** クイックタブで、**フィルター** を選択してからクエリで顧客勘定を指定します。</span><span class="sxs-lookup"><span data-stu-id="1ddbf-120">To reimburse specific customer accounts, on the **Records to include** FastTab, select **Filter**, and then specify the customer accounts in the query.</span></span>

    <span data-ttu-id="1ddbf-121">貸方金額が顧客の仕入先勘定に転送され、通常の支払として処理されます。</span><span class="sxs-lookup"><span data-stu-id="1ddbf-121">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="1ddbf-122">顧客が仕入先勘定を持たない場合、その顧客の一時仕入先勘定が自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="1ddbf-122">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>

5. <span data-ttu-id="1ddbf-123">作成された払い戻しトランザクションを表示するには、**払い戻し** レポート (**売掛金勘定 \> 照会およびレポート \> 払い戻しレポート**) を使用します。</span><span class="sxs-lookup"><span data-stu-id="1ddbf-123">To view the reimbursement transactions that were created, use the **Reimbursement** report (**Accounts Receivable \> Inquiries and reports \> Reimbursement report**).</span></span>
6. <span data-ttu-id="1ddbf-124">買掛金勘定で、払い戻しプロセスの結果として作成された仕入先請求書に対する支払を作成します。</span><span class="sxs-lookup"><span data-stu-id="1ddbf-124">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span> <span data-ttu-id="1ddbf-125">仕入先への支払方法の詳細については、[仕入先への支払に関する概要](../accounts-payable/Vendor-payments-workspace.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1ddbf-125">For information about how to pay vendors, see [Vendor payment overview](../accounts-payable/Vendor-payments-workspace.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]