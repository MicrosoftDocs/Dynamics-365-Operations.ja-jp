--- 
title: "特別償却プロファイルのある固定資産の作成 (日本)"
description: "日本では、特定の条件下で特別減価償却額を固定資産に転記できます。この手順では、特別償却プロファイルがある固定資産の作成方法について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: bab26cad2491cd4bf2663c65254abb295718deaf
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-fixed-asset-with-special-depreciation-profile-japan"></a><span data-ttu-id="82842-103">特別償却プロファイルのある固定資産の作成 (日本)</span><span class="sxs-lookup"><span data-stu-id="82842-103">Create a fixed asset with special depreciation profile (Japan)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82842-104">日本では、特定の条件下で特別償却額を固定資産に転記できます。</span><span class="sxs-lookup"><span data-stu-id="82842-104">In Japan, you can post a special depreciation amount to a fixed asset, under certain conditions</span></span>



<span data-ttu-id="82842-105">この手順を使用して、特別償却プロファイルのある固定資産の作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="82842-105">Use this procedure to learn how to create a fixed asset with special depreciation profile.</span></span>



<span data-ttu-id="82842-106">この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="82842-106">To complete this procedure, the Fixed Assets configuration key must be selected.</span></span>



<span data-ttu-id="82842-107">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="82842-107">This procedure uses the JPMF demo company data.</span></span>

1. <span data-ttu-id="82842-108">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="82842-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="82842-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="82842-109">Click New.</span></span>
3. <span data-ttu-id="82842-110">[固定資産グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="82842-110">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="82842-111">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="82842-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="82842-112">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="82842-112">Click Save.</span></span>
6. <span data-ttu-id="82842-113">[価値モデル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="82842-113">Click Value models.</span></span>
7. <span data-ttu-id="82842-114">[減価償却] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="82842-114">Expand or collapse the Depreciation section.</span></span>
    * <span data-ttu-id="82842-115">特別減価償却プロファイルとして [特別償却プロファイル] を選択します。</span><span class="sxs-lookup"><span data-stu-id="82842-115">Select a Special depreciation profile as Extraordinary depreciation profile.</span></span>  
    * <span data-ttu-id="82842-116">EQUP-M と 200NDB_CSR には、すでに既定のコンフィギュレーションとしてデモ データに SpeRE-1M があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="82842-116">Note that the EQUP-M and 200NDB_CSR already has the SpeRE-1M as default configuration in the demo data.</span></span>  
    * <span data-ttu-id="82842-117">[取崩開始]、[取崩基準]、および[取崩期数] には既定が入力されます。</span><span class="sxs-lookup"><span data-stu-id="82842-117">Allocation start convention, Allocation unit, and Allocation periods fill with default values.</span></span> <span data-ttu-id="82842-118">これらは必要に応じて変更できます。</span><span class="sxs-lookup"><span data-stu-id="82842-118">You can change them if needed.</span></span> <span data-ttu-id="82842-119">これらは特別減価償却の引当メソッド固有のものです。</span><span class="sxs-lookup"><span data-stu-id="82842-119">These are specific to the Reserve method for special depreciation.</span></span>  


