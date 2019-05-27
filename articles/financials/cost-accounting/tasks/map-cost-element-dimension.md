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
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52b9f6a5b71349d404fe9621b58f58aab843a71f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570696"
---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="e4ed0-103">原価要素分析コードのマップ</span><span class="sxs-lookup"><span data-stu-id="e4ed0-103">Map a cost element dimension</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e4ed0-104">原価管理者は、この手順を使用して、MXMF 法人の原価要素分析コードに原価要素分析コードをマップします。</span><span class="sxs-lookup"><span data-stu-id="e4ed0-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="e4ed0-105">この記録では、USP2 デモ データ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="e4ed0-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="e4ed0-106">[原価計算] > [分析コード] > [コスト要素分析コード] の順序で進みます。</span><span class="sxs-lookup"><span data-stu-id="e4ed0-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="e4ed0-107">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ed0-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e4ed0-108">この例の場合、[原価要素] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ed0-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="e4ed0-109">[分析コード マッピング] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4ed0-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="e4ed0-110">この分析コードから、[コンフィギュレーション マッピング] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4ed0-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="e4ed0-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4ed0-111">Click New.</span></span>
6. <span data-ttu-id="e4ed0-112">[移動先分析コード] フィールドでは、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ed0-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="e4ed0-113">この例の場合、[MXMF 原価要素] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ed0-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="e4ed0-114">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4ed0-114">Click New.</span></span>
8. <span data-ttu-id="e4ed0-115">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="e4ed0-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="e4ed0-116">[移動元分析コード メンバー] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ed0-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="e4ed0-117">この例の場合、分析コード メンバー 606400 [電話 & ファックスの費用] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ed0-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="e4ed0-118">[移動先分析コード メンバー] フィールドでは、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ed0-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="e4ed0-119">この例の場合、分析コード メンバー6001004 [Telefono] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4ed0-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="e4ed0-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4ed0-120">Click Save.</span></span>

