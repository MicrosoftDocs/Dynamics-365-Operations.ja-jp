---
title: "為替手形の裏書による仕入先への支払"
description: "日本では、多くの場合、為替手形 (BOEs) は仕入先に裏書きされ、支払方法として使用されます。 Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition の BOE のリスト ページでは、BOE のライフ サイクルの集中管理を提供します。"
author: yijialuan
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustBillOfExchangeEndorseListPage, CustBillOfExchangeEndorseToVendor
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 28791
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3cb6faa4c282b9868ad9660aaa3f1aeefe04ad6d
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="pay-a-vendor-by-endorsing-a-bill-of-exchange"></a><span data-ttu-id="ae773-104">為替手形の裏書による仕入先への支払</span><span class="sxs-lookup"><span data-stu-id="ae773-104">Pay a vendor by endorsing a bill of exchange</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ae773-105">日本では、多くの場合、為替手形 (BOEs) は仕入先に裏書きされ、支払方法として使用されます。</span><span class="sxs-lookup"><span data-stu-id="ae773-105">In Japan, bills of exchange (BOEs) are often endorsed to a vendor and used as a method of payment.</span></span> <span data-ttu-id="ae773-106">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition の BOE のリスト ページでは、BOE のライフ サイクルの集中管理を提供します。</span><span class="sxs-lookup"><span data-stu-id="ae773-106">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, a list page for BOEs provides centralized management of the BOE lifecycle.</span></span>

<span data-ttu-id="ae773-107">Finance and Operations の BOE の管理を開始するには、受取手形振出仕訳帳を開きます。</span><span class="sxs-lookup"><span data-stu-id="ae773-107">To start managing a BOE in Finance and Operations, open the Draw bill of exchange journal.</span></span> <span data-ttu-id="ae773-108">このタイプの仕訳帳を転記すると、BOE ステータスが**振出**の場合、次のステージの BOE のライフ サイクルを管理できます。</span><span class="sxs-lookup"><span data-stu-id="ae773-108">When this type of journal is posted, if the status of the BOE is **Drawn**, users can manage the BOE lifecycle in following stages.</span></span>

## <a name="endorse-a-boe-to-a-vendor"></a><span data-ttu-id="ae773-109">仕入先に対する BOE の裏書</span><span class="sxs-lookup"><span data-stu-id="ae773-109">Endorse a BOE to a vendor</span></span>
<span data-ttu-id="ae773-110">リスト ページには、振り出された顧客の BOE が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ae773-110">The list page shows customer BOEs that have been drawn.</span></span> <span data-ttu-id="ae773-111">一つ以上の仕入先に裏書きする BOE を選択できます。</span><span class="sxs-lookup"><span data-stu-id="ae773-111">You can select one or more BOEs to endorse to a vendor.</span></span> <span data-ttu-id="ae773-112">ただし、複数の BOE がオンの場合、それらに裏書きする前に、**振出**ステータスがすべてに必要です。</span><span class="sxs-lookup"><span data-stu-id="ae773-112">However, if multiple BOEs are selected, they all must have a status of **Drawn** before you can endorse them.</span></span> <span data-ttu-id="ae773-113">会計伝票は裏書きした BOE の勘定と買掛金勘定の残高の変更を記録するために生成されます。</span><span class="sxs-lookup"><span data-stu-id="ae773-113">An accounting voucher will be generated to record the balance change in the endorsed BOE account and the accounts payable account.</span></span>

## <a name="settle-vendor-transactions"></a><span data-ttu-id="ae773-114">仕入先トランザクションの決済</span><span class="sxs-lookup"><span data-stu-id="ae773-114">Settle vendor transactions</span></span>
<span data-ttu-id="ae773-115">BOE が裏書きされると **裏書済**ステータスに変更されます。</span><span class="sxs-lookup"><span data-stu-id="ae773-115">When a BOE is endorsed, its status changes to **Endorsed**.</span></span> <span data-ttu-id="ae773-116">買掛金勘定のユーザーが仕入先請求書に対して、仕入先トランザクションを決済できます。</span><span class="sxs-lookup"><span data-stu-id="ae773-116">An Accounts payable user can then settle the vendor transaction against a vendor invoice.</span></span> <span data-ttu-id="ae773-117">仕入先トランザクションの決済時に BOE 自体のステータスは変更されません。</span><span class="sxs-lookup"><span data-stu-id="ae773-117">The status of the BOE itself doesn't change when the vendor transaction is settled.</span></span>

## <a name="settle-endorsed-boes"></a><span data-ttu-id="ae773-118">裏書済 BOE の決済</span><span class="sxs-lookup"><span data-stu-id="ae773-118">Settle endorsed BOEs</span></span>
<span data-ttu-id="ae773-119">BOE のライフ サイクルは、BOE が支払われる、または期限切れになった時点で終了します。</span><span class="sxs-lookup"><span data-stu-id="ae773-119">The lifecycle of a BOE ends when the BOE is paid or expires.</span></span> <span data-ttu-id="ae773-120">裏書きした BOE の場合、BOE を選択し、裏書を決済できます。</span><span class="sxs-lookup"><span data-stu-id="ae773-120">For endorsed BOEs, you can select the BOE and settle the endorsement.</span></span> <span data-ttu-id="ae773-121">会計伝票は裏書きした BOE の勘定と振出済 BOE の勘定の残高の変更を記録するために生成されます。</span><span class="sxs-lookup"><span data-stu-id="ae773-121">An accounting voucher will be generated to record the balance change in the endorsed BOE account and the drawn BOE account.</span></span>

## <a name="reserve-endorsement"></a><span data-ttu-id="ae773-122">裏書の引当</span><span class="sxs-lookup"><span data-stu-id="ae773-122">Reserve endorsement</span></span>
<span data-ttu-id="ae773-123">BOE の状態が**裏書済**の場合、裏書引当を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="ae773-123">If the status of a BOE is **Endorsed**, a user can reserve its endorsement.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ae773-124">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="ae773-124">Additional resources</span></span>
- [<span data-ttu-id="ae773-125">顧客の受取手形の裏書による仕入先トランザクションの支払</span><span class="sxs-lookup"><span data-stu-id="ae773-125">Pay a vendor transaction by endorsing a customer bill of exchange</span></span>](./tasks/pay-vendor-transaction.md)
- [<span data-ttu-id="ae773-126">裏書済受取手形の取消</span><span class="sxs-lookup"><span data-stu-id="ae773-126">Reverse an endorsed bill of exchange</span></span>](./tasks/reverse-endorsed-bill-exchange.md)
- [<span data-ttu-id="ae773-127">顧客受取手形の裏書による日本の支払の設定</span><span class="sxs-lookup"><span data-stu-id="ae773-127">Set up Japan payment by endorsing a customer bill of exchange</span></span>](./tasks/setup-japan-payment-endorsing-customer-bill-exchange.md)
- [<span data-ttu-id="ae773-128">裏書済受取手形の決済</span><span class="sxs-lookup"><span data-stu-id="ae773-128">Settle an endorsed bill of exchange</span></span>](./tasks/settle-endorsed-bill-exchange.md)


