---
title: 特別償却プロファイルのある固定資産の作成
description: 日本では、特定の条件下で特別償却額を固定資産に転記できます この手順を使用して、特別償却プロファイルのある固定資産の作成方法を説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 321bb8d3501d9d8bec3e2725d81a025c5ff0c544
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571088"
---
# <a name="create-a-fixed-asset-with-special-depreciation-profile"></a><span data-ttu-id="e5f00-104">特別償却プロファイルのある固定資産の作成</span><span class="sxs-lookup"><span data-stu-id="e5f00-104">Create a fixed asset with special depreciation profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e5f00-105">日本では、特定の条件下で特別償却額を固定資産に転記できます</span><span class="sxs-lookup"><span data-stu-id="e5f00-105">In Japan, you can post a special depreciation amount to a fixed asset, under certain conditions.</span></span>

<span data-ttu-id="e5f00-106">この手順を使用して、特別償却プロファイルのある固定資産の作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="e5f00-106">Use this procedure to learn how to create a fixed asset with special depreciation profile.</span></span>

<span data-ttu-id="e5f00-107">この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5f00-107">To complete this procedure, the Fixed Assets configuration key must be selected.</span></span>

<span data-ttu-id="e5f00-108">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="e5f00-108">This procedure uses the JPMF demo company data.</span></span>

1. <span data-ttu-id="e5f00-109">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="e5f00-109">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="e5f00-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5f00-110">Click New.</span></span>
3. <span data-ttu-id="e5f00-111">[固定資産グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5f00-111">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="e5f00-112">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5f00-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e5f00-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5f00-113">Click Save.</span></span>
6. <span data-ttu-id="e5f00-114">[価値モデル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5f00-114">Click Value models.</span></span>
7. <span data-ttu-id="e5f00-115">[減価償却] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="e5f00-115">Expand or collapse the Depreciation section.</span></span>
    * <span data-ttu-id="e5f00-116">特別減価償却プロファイルとして [特別償却プロファイル] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5f00-116">Select a Special depreciation profile as Extraordinary depreciation profile.</span></span>  
    * <span data-ttu-id="e5f00-117">EQUP-M と 200NDB_CSR には、すでに既定のコンフィギュレーションとしてデモ データに SpeRE-1M があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e5f00-117">Note that the EQUP-M and 200NDB_CSR already has the SpeRE-1M as default configuration in the demo data.</span></span>  
    * <span data-ttu-id="e5f00-118">[取崩開始]、[取崩基準]、および[取崩期数] には既定が入力されます。</span><span class="sxs-lookup"><span data-stu-id="e5f00-118">Allocation start convention, Allocation unit, and Allocation periods fill with default values.</span></span> <span data-ttu-id="e5f00-119">これらは必要に応じて変更できます。</span><span class="sxs-lookup"><span data-stu-id="e5f00-119">You can change them if needed.</span></span> <span data-ttu-id="e5f00-120">これらは特別減価償却の引当メソッド固有のものです。</span><span class="sxs-lookup"><span data-stu-id="e5f00-120">These are specific to the Reserve method for special depreciation.</span></span>  

