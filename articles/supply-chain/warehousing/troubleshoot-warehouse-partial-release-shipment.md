---
title: 部分的なリリースと部分的な出荷に関するトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management での部分的なリリースと部分的な出荷の処理中に発生する可能性がある問題を修正する方法について説明します。
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 33323a8aed44cf19db6c2c937abcb09f7e05b6c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993955"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="46e24-103">部分的なリリースと部分的な出荷に関するトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="46e24-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46e24-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management での部分的なリリースと部分的な出荷の処理中に発生する可能性がある問題を修正する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="46e24-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="46e24-105">販売注文のリリース ステータスは、販売注文の請求が行われた後も部分的にリリースされたままになります。</span><span class="sxs-lookup"><span data-stu-id="46e24-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="46e24-106">問題の説明</span><span class="sxs-lookup"><span data-stu-id="46e24-106">Issue description</span></span>

<span data-ttu-id="46e24-107">販売注文は出荷注文ですが、その中の 1 つ以上の品目の荷渡方法が異なります。</span><span class="sxs-lookup"><span data-stu-id="46e24-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="46e24-108">注文が請求された後も、まだリリース ステータスが *部分的にリリース済み* になっています。</span><span class="sxs-lookup"><span data-stu-id="46e24-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="46e24-109">たとえば、販売注文には配送用と集荷用の 2 つの項目があります。</span><span class="sxs-lookup"><span data-stu-id="46e24-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="46e24-110">出荷と集荷の両方が完了しています。</span><span class="sxs-lookup"><span data-stu-id="46e24-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="46e24-111">したがって、両方の明細行が請求されています。</span><span class="sxs-lookup"><span data-stu-id="46e24-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="46e24-112">ただし、リリース ステータスはまだ *部分的にリリース済み* と表示されますが、これは誤解を招くことになります。</span><span class="sxs-lookup"><span data-stu-id="46e24-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="46e24-113">問題の解決</span><span class="sxs-lookup"><span data-stu-id="46e24-113">Issue resolution</span></span>

<span data-ttu-id="46e24-114">リリース ステータスは、品目が倉庫管理に対して有効になっている注文明細行に対してのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="46e24-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="46e24-115">したがって、このシナリオではリリース ステータスが *部分的にリリース済み* の ままになります。</span><span class="sxs-lookup"><span data-stu-id="46e24-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="46e24-116">Microsoft は、この問題を評価し、それが機能上の制限であることを確認しました。</span><span class="sxs-lookup"><span data-stu-id="46e24-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="46e24-117">リリース ステータスを更新するには、梱包明細および請求プロセスの一部として拡張機能を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="46e24-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>
