---
title: 製品コンフィギュレーション モデルへの計算の追加
description: この手順は、製品コンフィギュレーション モデルに新しい計算を追加する方法を表示します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 268baa4b518f6df52d4393f7278a79cbe1733844
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812680"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="76603-103">製品コンフィギュレーション モデルへの計算の追加</span><span class="sxs-lookup"><span data-stu-id="76603-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="76603-104">この手順は、製品コンフィギュレーション モデルに新しい計算を追加する方法を表示します。</span><span class="sxs-lookup"><span data-stu-id="76603-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="76603-105">スピーカーの高さを、白いスピーカーは 10 に、他のすべてのキャビネットの仕上げは 15 に設定するため、「If」 演算子を使用して論理式を作成する方法を表示します。</span><span class="sxs-lookup"><span data-stu-id="76603-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="76603-106">その手順は、デモ会社 USMF で [ハイエンド スピーカー] コンポーネントを使用します。</span><span class="sxs-lookup"><span data-stu-id="76603-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="76603-107">計算の追加</span><span class="sxs-lookup"><span data-stu-id="76603-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="76603-108">計算式の作成</span><span class="sxs-lookup"><span data-stu-id="76603-108">Create calculation expression</span></span>
1. <span data-ttu-id="76603-109">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="76603-109">Click Edit expression.</span></span>
2. <span data-ttu-id="76603-110">ConstraintBody フィールドで、「If[CabinetFinish=="White", 10, 15]」を入力します。</span><span class="sxs-lookup"><span data-stu-id="76603-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="76603-111">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="76603-111">Click Validate.</span></span>
4. <span data-ttu-id="76603-112">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="76603-112">Click Close.</span></span>
5. <span data-ttu-id="76603-113">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="76603-113">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]