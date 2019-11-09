---
title: 原価要素分析コードのマップ
description: 原価管理者は、この手順を使用して、MXMF 法人の原価要素分析コードに原価要素分析コードをマップします。
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 346c64ffb19e320d0babf886c15f1b46959b4f32
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178655"
---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="0db60-103">原価要素分析コードのマップ</span><span class="sxs-lookup"><span data-stu-id="0db60-103">Map a cost element dimension</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0db60-104">原価管理者は、この手順を使用して、MXMF 法人の原価要素分析コードに原価要素分析コードをマップします。</span><span class="sxs-lookup"><span data-stu-id="0db60-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="0db60-105">この記録では、USP2 デモ データ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="0db60-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="0db60-106">[原価計算] > [分析コード] > [コスト要素分析コード] の順序で進みます。</span><span class="sxs-lookup"><span data-stu-id="0db60-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="0db60-107">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="0db60-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0db60-108">この例の場合、[原価要素] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0db60-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="0db60-109">[分析コード マッピング] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0db60-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="0db60-110">この分析コードから、[コンフィギュレーション マッピング] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0db60-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="0db60-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0db60-111">Click New.</span></span>
6. <span data-ttu-id="0db60-112">[移動先分析コード] フィールドでは、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="0db60-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="0db60-113">この例の場合、[MXMF 原価要素] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0db60-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="0db60-114">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0db60-114">Click New.</span></span>
8. <span data-ttu-id="0db60-115">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="0db60-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="0db60-116">[移動元分析コード メンバー] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="0db60-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="0db60-117">この例の場合、分析コード メンバー 606400 [電話 & ファックスの費用] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0db60-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="0db60-118">[移動先分析コード メンバー] フィールドでは、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="0db60-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="0db60-119">この例の場合、分析コード メンバー6001004 [Telefono] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0db60-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="0db60-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0db60-120">Click Save.</span></span>
