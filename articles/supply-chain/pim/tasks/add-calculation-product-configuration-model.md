--- 
title: "製品コンフィギュレーション モデルへの計算の追加"
description: "この手順は、製品コンフィギュレーション モデルに新しい計算を追加する方法を表示します。"
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 123ae1315c95693af09d7d7c96a071d606ac98f8
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="6b7a8-103">製品コンフィギュレーション モデルへの計算の追加</span><span class="sxs-lookup"><span data-stu-id="6b7a8-103">Add a calculation to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b7a8-104">この手順は、製品コンフィギュレーション モデルに新しい計算を追加する方法を表示します。</span><span class="sxs-lookup"><span data-stu-id="6b7a8-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="6b7a8-105">スピーカーの高さを、白いスピーカーは 10 に、他のすべてのキャビネットの仕上げは 15 に設定するため、「If」 演算子を使用して論理式を作成する方法を表示します。</span><span class="sxs-lookup"><span data-stu-id="6b7a8-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="6b7a8-106">その手順は、デモ会社 USMF で [ハイエンド スピーカー] コンポーネントを使用します。</span><span class="sxs-lookup"><span data-stu-id="6b7a8-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="6b7a8-107">計算の追加</span><span class="sxs-lookup"><span data-stu-id="6b7a8-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="6b7a8-108">計算式の作成</span><span class="sxs-lookup"><span data-stu-id="6b7a8-108">Create calculation expression</span></span>
1. <span data-ttu-id="6b7a8-109">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b7a8-109">Click Edit expression.</span></span>
2. <span data-ttu-id="6b7a8-110">[ConstraintBody] フィールドで、「If[CabinetFinish=="White", 10, 15]」を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b7a8-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="6b7a8-111">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b7a8-111">Click Validate.</span></span>
4. <span data-ttu-id="6b7a8-112">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b7a8-112">Click Close.</span></span>
5. <span data-ttu-id="6b7a8-113">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b7a8-113">Click OK.</span></span>


