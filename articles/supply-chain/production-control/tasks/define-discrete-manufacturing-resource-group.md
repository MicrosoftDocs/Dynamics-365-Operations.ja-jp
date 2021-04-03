---
title: 個別の製造リソース グループの定義
description: リソース グループは、通常、作業セルの物理的な構成に対応する、作業現場フロアで黄色のラインで示される一連の運営リソースです。
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 24097cbb6f0ffae7b1b52bd3c70b7e054b3ce86c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257318"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="ca2c2-103">個別の製造リソース グループの定義</span><span class="sxs-lookup"><span data-stu-id="ca2c2-103">Define discrete manufacturing resource group</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ca2c2-104">リソース グループは、通常、作業セルの物理的な構成に対応する、作業現場フロアで黄色のラインで示される一連の運営リソースです。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="ca2c2-105">この手順では、個別生産で使用するリソース グループを定義する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="ca2c2-106">デモ データ会社 USMF または独自のデータを使用して、この手順の説明を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="ca2c2-107">[リソース グループ] に移動します。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="ca2c2-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-108">Click New.</span></span>
3. <span data-ttu-id="ca2c2-109">[リソース グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="ca2c2-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ca2c2-111">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="ca2c2-112">[生産単位] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="ca2c2-113">既定の工程パラメーターの定義</span><span class="sxs-lookup"><span data-stu-id="ca2c2-113">Define default operational parameters</span></span>
1. <span data-ttu-id="ca2c2-114">[操作] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="ca2c2-115">[仕損率] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="ca2c2-116">[段取りカテゴリ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="ca2c2-117">[実行時間カテゴリ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="ca2c2-118">[工程のスケジューリング率] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="ca2c2-119">工程時間の定義</span><span class="sxs-lookup"><span data-stu-id="ca2c2-119">Define operating hours</span></span>
1. <span data-ttu-id="ca2c2-120">[カレンダー] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="ca2c2-121">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-121">Click Add.</span></span>
3. <span data-ttu-id="ca2c2-122">[カレンダー] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="ca2c2-123">運営リソースの追加</span><span class="sxs-lookup"><span data-stu-id="ca2c2-123">Add operations resources</span></span>
1. <span data-ttu-id="ca2c2-124">[リソース] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="ca2c2-125">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-125">Click Add.</span></span>
3. <span data-ttu-id="ca2c2-126">[リソース] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="ca2c2-127">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-127">Click Add.</span></span>
5. <span data-ttu-id="ca2c2-128">[リソース] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="ca2c2-129">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ca2c2-130">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ca2c2-130">In the list, click the link in the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]