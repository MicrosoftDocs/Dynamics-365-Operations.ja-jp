---
title: 日本での受取手形の裏書による仕入先への支払
description: このトピックには、日本で仕入先に支払うための受取手形 (BOE) の裏書に関する情報が含まれています。
author: yijialuan
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustBillOfExchangeEndorseListPage, CustBillOfExchangeEndorseToVendor
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 28791
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7959d69abab2b2ec8808d1664b541c58061bfbe
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550764"
---
# <a name="pay-a-vendor-by-endorsing-a-bill-of-exchange-for-japan"></a><span data-ttu-id="f40e5-103">日本での受取手形の裏書による仕入先への支払</span><span class="sxs-lookup"><span data-stu-id="f40e5-103">Pay a vendor by endorsing a bill of exchange for Japan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f40e5-104">日本では、多くの場合、為替手形 (BOE) は仕入先に裏書きされ、支払方法として使用されます。</span><span class="sxs-lookup"><span data-stu-id="f40e5-104">In Japan, bills of exchange (BOE) are often endorsed to a vendor and used as a method of payment.</span></span> <span data-ttu-id="f40e5-105">Microsoft Dynamics 365 for Finance and Operations の BOEs のリスト ページでは、BOE のライフ サイクルの集中管理を提供します。</span><span class="sxs-lookup"><span data-stu-id="f40e5-105">In Microsoft Dynamics 365 for Finance and Operations, a list page for BOEs provides centralized management of the BOE lifecycle.</span></span>

<span data-ttu-id="f40e5-106">Finance and Operations の BOE の管理を開始するには、受取手形振出仕訳帳を開きます。</span><span class="sxs-lookup"><span data-stu-id="f40e5-106">To start managing a BOE in Finance and Operations, open the Draw bill of exchange journal.</span></span> <span data-ttu-id="f40e5-107">このタイプの仕訳帳を転記すると、BOE ステータスが**振出**の場合、次のステージの BOE のライフ サイクルを管理できます。</span><span class="sxs-lookup"><span data-stu-id="f40e5-107">When this type of journal is posted, if the status of the BOE is **Drawn**, users can manage the BOE lifecycle in following stages.</span></span>

## <a name="endorsea-boe-to-a-vendor"></a><span data-ttu-id="f40e5-108">仕入先に対する BOE の裏書</span><span class="sxs-lookup"><span data-stu-id="f40e5-108">Endorse a BOE to a vendor</span></span>
<span data-ttu-id="f40e5-109">リスト ページには、振り出された顧客の BOE が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f40e5-109">The list page shows customer BOEs that have been drawn.</span></span> <span data-ttu-id="f40e5-110">一つ以上の仕入先に裏書きする BOE を選択できます。</span><span class="sxs-lookup"><span data-stu-id="f40e5-110">You can select one or more BOEs to endorse to a vendor.</span></span> <span data-ttu-id="f40e5-111">ただし、複数の BOE がオンの場合、それらに裏書きする前に、**振出**ステータスがすべてに必要です。</span><span class="sxs-lookup"><span data-stu-id="f40e5-111">However, if multiple BOEs are selected, they all must have a status of **Drawn** before you can endorse them.</span></span> <span data-ttu-id="f40e5-112">会計伝票は裏書きした BOE の勘定と買掛金勘定の残高の変更を記録するために生成されます。</span><span class="sxs-lookup"><span data-stu-id="f40e5-112">An accounting voucher will be generated to record the balance change in the endorsed BOE account and the accounts payable account.</span></span>

## <a name="settle-vendor-transactions"></a><span data-ttu-id="f40e5-113">仕入先トランザクションの決済</span><span class="sxs-lookup"><span data-stu-id="f40e5-113">Settle vendor transactions</span></span>
<span data-ttu-id="f40e5-114">BOE が裏書きされると **裏書済**ステータスに変更されます。</span><span class="sxs-lookup"><span data-stu-id="f40e5-114">When a BOE is endorsed, its status changes to **Endorsed**.</span></span> <span data-ttu-id="f40e5-115">買掛金勘定のユーザーが仕入先請求書に対して、仕入先トランザクションを決済できます。</span><span class="sxs-lookup"><span data-stu-id="f40e5-115">An Accounts payable user can then settle the vendor transaction against a vendor invoice.</span></span> <span data-ttu-id="f40e5-116">仕入先トランザクションの決済時に BOE 自体のステータスは変更されません。</span><span class="sxs-lookup"><span data-stu-id="f40e5-116">The status of the BOE itself doesn't change when the vendor transaction is settled.</span></span>

## <a name="settle-endorsed-boes"></a><span data-ttu-id="f40e5-117">裏書済 BOE の決済</span><span class="sxs-lookup"><span data-stu-id="f40e5-117">Settle endorsed BOEs</span></span>
<span data-ttu-id="f40e5-118">BOE のライフ サイクルは、BOE が支払われる、または期限切れになった時点で終了します。</span><span class="sxs-lookup"><span data-stu-id="f40e5-118">The lifecycle of a BOE ends when the BOE is paid or expires.</span></span> <span data-ttu-id="f40e5-119">裏書きした BOE の場合、BOE を選択し、裏書を決済できます。</span><span class="sxs-lookup"><span data-stu-id="f40e5-119">For endorsed BOEs, you can select the BOE and settle the endorsement.</span></span> <span data-ttu-id="f40e5-120">会計伝票は裏書きした BOE の勘定と振出済 BOE の勘定の残高の変更を記録するために生成されます。</span><span class="sxs-lookup"><span data-stu-id="f40e5-120">An accounting voucher will be generated to record the balance change in the endorsed BOE account and the drawn BOE account.</span></span>

## <a name="reserve-endorsement"></a><span data-ttu-id="f40e5-121">裏書の引当</span><span class="sxs-lookup"><span data-stu-id="f40e5-121">Reserve endorsement</span></span>
<span data-ttu-id="f40e5-122">BOE の状態が**裏書済**の場合、裏書引当を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f40e5-122">If the status of a BOE is **Endorsed**, a user can reserve its endorsement.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f40e5-123">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="f40e5-123">Additional resources</span></span>
- [<span data-ttu-id="f40e5-124">顧客の受取手形の裏書による仕入先トランザクションの支払</span><span class="sxs-lookup"><span data-stu-id="f40e5-124">Pay a vendor transaction by endorsing a customer bill of exchange</span></span>](./tasks/pay-vendor-transaction.md)
- [<span data-ttu-id="f40e5-125">裏書済受取手形の取消</span><span class="sxs-lookup"><span data-stu-id="f40e5-125">Reverse an endorsed bill of exchange</span></span>](./tasks/reverse-endorsed-bill-exchange.md)
- [<span data-ttu-id="f40e5-126">顧客受取手形の裏書による日本の支払の設定</span><span class="sxs-lookup"><span data-stu-id="f40e5-126">Set up Japan payment by endorsing a customer bill of exchange</span></span>](./tasks/setup-japan-payment-endorsing-customer-bill-exchange.md)
- [<span data-ttu-id="f40e5-127">裏書済受取手形の決済</span><span class="sxs-lookup"><span data-stu-id="f40e5-127">Settle an endorsed bill of exchange</span></span>](./tasks/settle-endorsed-bill-exchange.md)

