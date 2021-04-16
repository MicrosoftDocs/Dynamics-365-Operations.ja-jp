---
title: 日本での受取手形の裏書による仕入先への支払
description: このトピックには、日本で仕入先に支払うための受取手形 (BOE) の裏書に関する情報が含まれています。
author: yijialuan
ms.date: 03/21/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustBillOfExchangeEndorseListPage, CustBillOfExchangeEndorseToVendor
audience: Application User
ms.reviewer: kfend
ms.custom: 28791
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88030bf67bd28f9370a2459a48fd789a4ff0a424
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834368"
---
# <a name="pay-a-vendor-by-endorsing-a-bill-of-exchange-for-japan"></a><span data-ttu-id="98bfd-103">日本での受取手形の裏書による仕入先への支払</span><span class="sxs-lookup"><span data-stu-id="98bfd-103">Pay a vendor by endorsing a bill of exchange for Japan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98bfd-104">日本では、多くの場合、為替手形 (BOE) は仕入先に裏書きされ、支払方法として使用されます。</span><span class="sxs-lookup"><span data-stu-id="98bfd-104">In Japan, bills of exchange (BOE) are often endorsed to a vendor and used as a method of payment.</span></span> <span data-ttu-id="98bfd-105">BOEs のリスト ページでは、BOE のライフ サイクルの集中管理を提供します。</span><span class="sxs-lookup"><span data-stu-id="98bfd-105">A list page for BOEs provides centralized management of the BOE lifecycle.</span></span>

<span data-ttu-id="98bfd-106">BOE の管理を開始するには、為替手形振出仕訳帳を開きます。</span><span class="sxs-lookup"><span data-stu-id="98bfd-106">To start managing a BOE, open the Draw bill of exchange journal.</span></span> <span data-ttu-id="98bfd-107">このタイプの仕訳帳を転記すると、BOE ステータスが **振出** の場合、次のステージの BOE のライフ サイクルを管理できます。</span><span class="sxs-lookup"><span data-stu-id="98bfd-107">When this type of journal is posted, if the status of the BOE is **Drawn**, users can manage the BOE lifecycle in following stages.</span></span>

## <a name="endorse-a-boe-to-a-vendor"></a><span data-ttu-id="98bfd-108">仕入先に対する BOE を裏書きする</span><span class="sxs-lookup"><span data-stu-id="98bfd-108">Endorse a BOE to a vendor</span></span>
<span data-ttu-id="98bfd-109">リスト ページには、振り出された顧客の BOE が表示されます。</span><span class="sxs-lookup"><span data-stu-id="98bfd-109">The list page shows customer BOEs that have been drawn.</span></span> <span data-ttu-id="98bfd-110">仕入先に裏書きする 1 つ以上の BOE を選択できます。</span><span class="sxs-lookup"><span data-stu-id="98bfd-110">You can select one or more BOEs to endorse to a vendor.</span></span> <span data-ttu-id="98bfd-111">ただし、複数の BOE が選択されている場合、裏書きする前にすべてが **振出** の状態である必要があります。</span><span class="sxs-lookup"><span data-stu-id="98bfd-111">However, if multiple BOEs are selected, they all must have a status of **Drawn** before you can endorse them.</span></span> <span data-ttu-id="98bfd-112">会計伝票は裏書きした BOE の勘定と買掛金勘定の残高の変更を記録するために生成されます。</span><span class="sxs-lookup"><span data-stu-id="98bfd-112">An accounting voucher will be generated to record the balance change in the endorsed BOE account and the accounts payable account.</span></span>

## <a name="settle-vendor-transactions"></a><span data-ttu-id="98bfd-113">仕入先トランザクションの決済</span><span class="sxs-lookup"><span data-stu-id="98bfd-113">Settle vendor transactions</span></span>
<span data-ttu-id="98bfd-114">BOE が裏書きされると **裏書済** ステータスに変更されます。</span><span class="sxs-lookup"><span data-stu-id="98bfd-114">When a BOE is endorsed, its status changes to **Endorsed**.</span></span> <span data-ttu-id="98bfd-115">買掛金勘定のユーザーが仕入先の請求書に対して、仕入先トランザクションを決済できます。</span><span class="sxs-lookup"><span data-stu-id="98bfd-115">An Accounts payable user can then settle the vendor transaction against a vendor invoice.</span></span> <span data-ttu-id="98bfd-116">仕入先トランザクションの決済時に BOE 自体のステータスは変更されません。</span><span class="sxs-lookup"><span data-stu-id="98bfd-116">The status of the BOE itself doesn't change when the vendor transaction is settled.</span></span>

## <a name="settle-endorsed-boes"></a><span data-ttu-id="98bfd-117">裏書済 BOE の決済</span><span class="sxs-lookup"><span data-stu-id="98bfd-117">Settle endorsed BOEs</span></span>
<span data-ttu-id="98bfd-118">BOE のライフ サイクルは、BOE が支払われる、または期限切れになった時点で終了します。</span><span class="sxs-lookup"><span data-stu-id="98bfd-118">The lifecycle of a BOE ends when the BOE is paid or expires.</span></span> <span data-ttu-id="98bfd-119">裏書きした BOE の場合、BOE を選択し、裏書を決済できます。</span><span class="sxs-lookup"><span data-stu-id="98bfd-119">For endorsed BOEs, you can select the BOE and settle the endorsement.</span></span> <span data-ttu-id="98bfd-120">会計伝票は裏書きした BOE 勘定と振出済 BOE 勘定の残高の変更を記録するために生成されます。</span><span class="sxs-lookup"><span data-stu-id="98bfd-120">An accounting voucher will be generated to record the balance change in the endorsed BOE account and the drawn BOE account.</span></span>

## <a name="reserve-endorsement"></a><span data-ttu-id="98bfd-121">裏書の引当</span><span class="sxs-lookup"><span data-stu-id="98bfd-121">Reserve endorsement</span></span>
<span data-ttu-id="98bfd-122">BOE の状態が **裏書済** の場合、裏書引当を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="98bfd-122">If the status of a BOE is **Endorsed**, a user can reserve its endorsement.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98bfd-123">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="98bfd-123">Additional resources</span></span>
- [<span data-ttu-id="98bfd-124">顧客の受取手形の裏書による仕入先トランザクションの支払</span><span class="sxs-lookup"><span data-stu-id="98bfd-124">Pay a vendor transaction by endorsing a customer bill of exchange</span></span>](./tasks/pay-vendor-transaction.md)
- [<span data-ttu-id="98bfd-125">裏書済受取手形の取消</span><span class="sxs-lookup"><span data-stu-id="98bfd-125">Reverse an endorsed bill of exchange</span></span>](./tasks/reverse-endorsed-bill-exchange.md)
- [<span data-ttu-id="98bfd-126">顧客の為替手形の裏書きによって日本の支払を設定します</span><span class="sxs-lookup"><span data-stu-id="98bfd-126">Setup Japan payment by endorsing a customer bill of exchange</span></span>](./tasks/setup-japan-payment-endorsing-customer-bill-exchange.md)
- [<span data-ttu-id="98bfd-127">裏書済受取手形の決済</span><span class="sxs-lookup"><span data-stu-id="98bfd-127">Settle an endorsed bill of exchange</span></span>](./tasks/settle-endorsed-bill-exchange.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]