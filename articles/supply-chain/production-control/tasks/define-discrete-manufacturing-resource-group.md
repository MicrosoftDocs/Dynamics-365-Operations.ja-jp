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
ms.openlocfilehash: d1930999604fb2605a88bad9a5972afd3579976a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975113"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="d0d1e-103">個別の製造リソース グループの定義</span><span class="sxs-lookup"><span data-stu-id="d0d1e-103">Define discrete manufacturing resource group</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d0d1e-104">リソース グループは、通常、作業セルの物理的な構成に対応する、作業現場フロアで黄色のラインで示される一連の運営リソースです。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="d0d1e-105">この手順では、個別生産で使用するリソース グループを定義する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="d0d1e-106">デモ データ会社 USMF または独自のデータを使用して、この手順の説明を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="d0d1e-107">[リソース グループ] に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="d0d1e-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-108">Click New.</span></span>
3. <span data-ttu-id="d0d1e-109">[リソース グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="d0d1e-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d0d1e-111">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="d0d1e-112">[生産単位] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="d0d1e-113">既定の工程パラメーターの定義</span><span class="sxs-lookup"><span data-stu-id="d0d1e-113">Define default operational parameters</span></span>
1. <span data-ttu-id="d0d1e-114">[操作] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="d0d1e-115">[仕損率] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="d0d1e-116">[段取りカテゴリ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="d0d1e-117">[実行時間カテゴリ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="d0d1e-118">[工程のスケジューリング率] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="d0d1e-119">工程時間の定義</span><span class="sxs-lookup"><span data-stu-id="d0d1e-119">Define operating hours</span></span>
1. <span data-ttu-id="d0d1e-120">[カレンダー] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="d0d1e-121">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-121">Click Add.</span></span>
3. <span data-ttu-id="d0d1e-122">[カレンダー] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="d0d1e-123">運営リソースの追加</span><span class="sxs-lookup"><span data-stu-id="d0d1e-123">Add operations resources</span></span>
1. <span data-ttu-id="d0d1e-124">[リソース] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="d0d1e-125">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-125">Click Add.</span></span>
3. <span data-ttu-id="d0d1e-126">[リソース] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="d0d1e-127">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-127">Click Add.</span></span>
5. <span data-ttu-id="d0d1e-128">[リソース] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="d0d1e-129">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="d0d1e-130">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0d1e-130">In the list, click the link in the selected row.</span></span>

