---
title: 1 つのレシートの複数の作業ヘッダーに対して印刷されるラベルは 1 つのみである
description: 1 つのレシートの複数の作業ヘッダーに対して印刷されるラベルは 1 つのみです。
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026676"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a><span data-ttu-id="63653-103">1 つのレシートの複数の作業ヘッダーに対して印刷されるラベルは 1 つのみである</span><span class="sxs-lookup"><span data-stu-id="63653-103">Only one label is printed for multiple work headers on a single receipt</span></span>

<span data-ttu-id="63653-104">KB 番号: 4614667</span><span class="sxs-lookup"><span data-stu-id="63653-104">KB number: 4614667</span></span>

## <a name="symptoms"></a><span data-ttu-id="63653-105">現象</span><span class="sxs-lookup"><span data-stu-id="63653-105">Symptoms</span></span>

<span data-ttu-id="63653-106">単一の倉庫アプリ受信イベントの一環で、同じターゲット ライセンス 契約に対して複数の作業ヘッダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="63653-106">Multiple work headers are created for the same target license plate as part of a single warehouse app receiving event.</span></span> <span data-ttu-id="63653-107">ただし、製品を入庫する際に印刷されるライセンス ラベルは 1 つのみです。</span><span class="sxs-lookup"><span data-stu-id="63653-107">However, only one license plate label is printed when the product is received.</span></span>

## <a name="resolution"></a><span data-ttu-id="63653-108">解像度</span><span class="sxs-lookup"><span data-stu-id="63653-108">Resolution</span></span>

<span data-ttu-id="63653-109">システムはデザイン通り動作しています。</span><span class="sxs-lookup"><span data-stu-id="63653-109">The system is behaving as designed.</span></span>

<span data-ttu-id="63653-110">現在の設計では、作業ヘッダーと作業ラインに存在する組み合わせの数に関係なく、常に 1 つのライセンス ラベルが生成されます。</span><span class="sxs-lookup"><span data-stu-id="63653-110">In the current design, a single license plate label is always generated, regardless of the number of work header and work line combinations that exist.</span></span> <span data-ttu-id="63653-111">生成されたラベルには、1 つの組み合わせについての情報だけが含まれます。</span><span class="sxs-lookup"><span data-stu-id="63653-111">The generated label includes the information for only one combination.</span></span>

<span data-ttu-id="63653-112">この問題を回避するには、作業ヘッダーの作成が常に 1 つのターゲット ライセンス契約にマッピングされるようにします。</span><span class="sxs-lookup"><span data-stu-id="63653-112">To work around this issue, make sure that work header creation is always mapped to just one target license plate.</span></span>
