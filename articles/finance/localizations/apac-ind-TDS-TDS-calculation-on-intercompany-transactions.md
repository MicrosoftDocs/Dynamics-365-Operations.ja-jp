---
title: 会社間取引の TDS の算出
description: このトピックでは、段階的に行われる企業間取引の源泉徴収 (TDS) の計算プロセスについて説明します。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 0e304747cc93bfe0a39beababc3182ca14664b11
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023391"
---
# <a name="tds-calculation-on-intercompany-transactions"></a><span data-ttu-id="c4b75-103">会社間取引の TDS の算出</span><span class="sxs-lookup"><span data-stu-id="c4b75-103">TDS calculation on intercompany transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4b75-104">このトピックでは、段階的に行われる企業間取引の源泉徴収 (TDS) の計算プロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c4b75-104">This topic describes the process that is used to calculate Tax Deducted at Source (TDS) on intercompany transactions in phases.</span></span>

<span data-ttu-id="c4b75-105">企業間取引の注文書または販売注文書が作成されると、顧客や仕入先に定義されている既定の TDS グループが TDS 額の計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="c4b75-105">When an intercompany purchase order or sales order is created, the default TDS group that is defined for the customer or vendor is used to calculate the TDS amount.</span></span> <span data-ttu-id="c4b75-106">TDS の金額は、請求書が転記された後に回収可能勘定または買掛金勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="c4b75-106">The TDS amount is posted to the recoverable or payable accounts after the invoice is posted.</span></span>

<span data-ttu-id="c4b75-107">会社間販売注文や会社間発注書は、元の発注書または販売注文に対して自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="c4b75-107">An intercompany sales order or purchase order is automatically created for the original purchase order or sales order.</span></span> <span data-ttu-id="c4b75-108">既定の TDS グループが会社間注文に表示され、TDS を計算できます。</span><span class="sxs-lookup"><span data-stu-id="c4b75-108">The default TDS group is shown on the intercompany order, so that TDS can be calculated.</span></span> <span data-ttu-id="c4b75-109">TDS のグループは変更できます。</span><span class="sxs-lookup"><span data-stu-id="c4b75-109">You can change the TDS group.</span></span> <span data-ttu-id="c4b75-110">自動的に作成された会社間注文の正味請求額が、元の注文の正味請求額と一致した場合にのみ、請求書を転記することができます。</span><span class="sxs-lookup"><span data-stu-id="c4b75-110">The invoice can be posted only if the net invoice amount on the intercompany order that is automatically created matches the net invoice amount on the original order.</span></span> <span data-ttu-id="c4b75-111">(正味金額は、TDS が控除された後の請求金額です。)</span><span class="sxs-lookup"><span data-stu-id="c4b75-111">(The net amount is the invoice amount after TDS is deducted.)</span></span>

<span data-ttu-id="c4b75-112">たとえば、50,000 円の売上請求書が作成され、**10%** の TDS グループが関連付けられたとします。</span><span class="sxs-lookup"><span data-stu-id="c4b75-112">For example, a sales invoice is created for 50,000, and the **10%** TDS group is attached to it.</span></span> <span data-ttu-id="c4b75-113">転記された請求金額は 45,000 で、売上請求書の転記された TDS の額は 5,000 です。</span><span class="sxs-lookup"><span data-stu-id="c4b75-113">The posted invoice amount is 45,000, and the posted TDS amount for the sales invoice is 5,000.</span></span> <span data-ttu-id="c4b75-114">会社間取引の注文書には自動的に注文書が作成され、 **10%** のTDSグループが関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="c4b75-114">A purchase order is automatically created for the intercompany sales order, and the  **10%** TDS group is attached to it.</span></span> <span data-ttu-id="c4b75-115">TDS グループを **15%** に変更すると、自動的に作成された会社間販売注文の正味請求金額が元販売注文の正味請求金額と一致しないため、請求書を転記できません。</span><span class="sxs-lookup"><span data-stu-id="c4b75-115">If you change the TDS group to **15%**, you can't post the invoice, because the net invoice amount of the intercompany sales order that was automatically created doesn't match the net invoice amount of the original sales order.</span></span>

<span data-ttu-id="c4b75-116">会社間請求書に対して作成された支払仕訳帳は自動的に転記されます。</span><span class="sxs-lookup"><span data-stu-id="c4b75-116">A payment journal that is created for an intercompany invoice is automatically posted.</span></span> <span data-ttu-id="c4b75-117">この支払仕訳帳は、その支払仕訳帳の正味支払金額が元の支払仕訳帳の正味支払金額と一致している場合にのみ転記できます。</span><span class="sxs-lookup"><span data-stu-id="c4b75-117">That payment journal can be posted only if the net payment amount on it matches the net payment amount on the original payment journal.</span></span>
