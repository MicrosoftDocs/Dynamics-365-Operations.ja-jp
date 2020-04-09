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
ms.openlocfilehash: 1a5805b7d86979389f1eb7496a63e3f4e7056c92
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3137871"
---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="0306c-103">原価要素分析コードのマップ</span><span class="sxs-lookup"><span data-stu-id="0306c-103">Map a cost element dimension</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0306c-104">原価管理者は、この手順を使用して、MXMF 法人の原価要素分析コードに原価要素分析コードをマップします。</span><span class="sxs-lookup"><span data-stu-id="0306c-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="0306c-105">この記録では、USP2 デモ データ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="0306c-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="0306c-106">[原価計算] > [分析コード] > [コスト要素分析コード] の順序で進みます。</span><span class="sxs-lookup"><span data-stu-id="0306c-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="0306c-107">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="0306c-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0306c-108">この例の場合、[原価要素] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0306c-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="0306c-109">[分析コード マッピング] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0306c-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="0306c-110">この分析コードから、[コンフィギュレーション マッピング] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0306c-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="0306c-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0306c-111">Click New.</span></span>
6. <span data-ttu-id="0306c-112">[移動先分析コード] フィールドでは、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="0306c-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="0306c-113">この例の場合、[MXMF 原価要素] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0306c-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="0306c-114">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0306c-114">Click New.</span></span>
8. <span data-ttu-id="0306c-115">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="0306c-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="0306c-116">[移動元分析コード メンバー] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="0306c-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="0306c-117">この例の場合、分析コード メンバー 606400 [電話 & ファックスの費用] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0306c-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="0306c-118">[移動先分析コード メンバー] フィールドでは、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="0306c-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="0306c-119">この例の場合、分析コード メンバー6001004 [Telefono] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0306c-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="0306c-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0306c-120">Click Save.</span></span>

