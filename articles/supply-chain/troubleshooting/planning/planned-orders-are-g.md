---
title: ファントム製品の計画オーダーが生成されるマスター プラン
description: マスター プランが実行された後にファントムの計画オーダーが生成されます。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026684"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a><span data-ttu-id="377ef-103">ファントム製品の計画オーダーが生成されるマスター プラン</span><span class="sxs-lookup"><span data-stu-id="377ef-103">Master planning generates planned orders for phantom products</span></span>

<span data-ttu-id="377ef-104">KB 番号: 4614729</span><span class="sxs-lookup"><span data-stu-id="377ef-104">KB number: 4614729</span></span>

## <a name="symptoms"></a><span data-ttu-id="377ef-105">現象</span><span class="sxs-lookup"><span data-stu-id="377ef-105">Symptoms</span></span>

<span data-ttu-id="377ef-106">マスター プランが実行された後にファントムの計画オーダーが生成されます。</span><span class="sxs-lookup"><span data-stu-id="377ef-106">Planned orders are generated for phantom products after master planning is run.</span></span>

## <a name="resolution"></a><span data-ttu-id="377ef-107">解像度</span><span class="sxs-lookup"><span data-stu-id="377ef-107">Resolution</span></span>

<span data-ttu-id="377ef-108">リリース済製品の **ファントム** オプションの設定が、部品表 (BOM) の既定の行タイプを決定します。</span><span class="sxs-lookup"><span data-stu-id="377ef-108">The setting of the **Phantom** option for released products determines the default line type on the bill of material (BOM).</span></span> <span data-ttu-id="377ef-109">**ファントム** オプションが *はい* に設定されている場合は、システムが品目の計画オーダーを作成しますが、各計画オーダーの **直接派生要件** オプションは *はい* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="377ef-109">When the **Phantom** option is set to *Yes*, the system will still create planned orders for the item, but the **Directly derived requirement** option for each planned order will be set to *Yes*.</span></span> <span data-ttu-id="377ef-110">したがって、計画製造オーダーは自身を確定できません。</span><span class="sxs-lookup"><span data-stu-id="377ef-110">Therefore, the planned production order can't be firmed on its own.</span></span> <span data-ttu-id="377ef-111">代わりに、親製造オーダーが確定された場合は常に自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="377ef-111">Instead, it will always be automatically included when the parent production order is firmed.</span></span> <span data-ttu-id="377ef-112">また、計画ファントム オーダーの BOM 明細行が親製造オーダーの BOM に含まれます。</span><span class="sxs-lookup"><span data-stu-id="377ef-112">Additionally, the BOM lines of the planned phantom order will be included in the BOM of the parent production order.</span></span>
