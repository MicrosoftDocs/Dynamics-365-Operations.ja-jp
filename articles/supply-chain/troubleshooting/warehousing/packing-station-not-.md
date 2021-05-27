---
title: 梱包ステーションに製品の注記が表示されない
description: 梱包ステーションに製品の注記が表示されません。
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSPack
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: bf64de3e67c1000dad9d5b37fffe622ae0e300b3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026674"
---
# <a name="packing-station-doesnt-show-product-notes"></a><span data-ttu-id="6bc2e-103">梱包ステーションに製品の注記が表示されない</span><span class="sxs-lookup"><span data-stu-id="6bc2e-103">Packing station doesn't show product notes</span></span>

<span data-ttu-id="6bc2e-104">KB 番号: 4614615</span><span class="sxs-lookup"><span data-stu-id="6bc2e-104">KB number: 4614615</span></span>

## <a name="symptoms"></a><span data-ttu-id="6bc2e-105">現象</span><span class="sxs-lookup"><span data-stu-id="6bc2e-105">Symptoms</span></span>

<span data-ttu-id="6bc2e-106">梱包指示が製品マスターまたは製品バリアントの関連付けとして追加された場合、梱包明細は梱包フォームに表示されません。</span><span class="sxs-lookup"><span data-stu-id="6bc2e-106">Packing notes aren't shown in the packing form when the packing instructions are added as an attachment to a product master or a product variant.</span></span>

## <a name="resolution"></a><span data-ttu-id="6bc2e-107">解像度</span><span class="sxs-lookup"><span data-stu-id="6bc2e-107">Resolution</span></span>

<span data-ttu-id="6bc2e-108">システムはデザイン通り動作しています。</span><span class="sxs-lookup"><span data-stu-id="6bc2e-108">The system is behaving as designed.</span></span>

<span data-ttu-id="6bc2e-109">梱包フォームに梱包明細を表示する現在のロジックには、注記が出荷に関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6bc2e-109">The current logic for showing packing notes in the packing form requires that the notes be associated with the shipments.</span></span>
