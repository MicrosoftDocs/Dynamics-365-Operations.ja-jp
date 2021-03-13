---
title: 分析コードベースのコンフィギュレーションの作成
description: この手順では、分析コード ベース製品のコンフィギュレーションを定義する方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 74ac3b2202a6a8c99d0a4ddce60b305f7d2a48f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011275"
---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="338e0-103">分析コードベースのコンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="338e0-103">Create dimension-based configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="338e0-104">この手順では、分析コード ベース製品のコンフィギュレーションを定義する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="338e0-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="338e0-105">これは、分析コード ベースのコンフィギュレーションでの組み合わせの作成方法を説明するシリーズの最後の手順です。</span><span class="sxs-lookup"><span data-stu-id="338e0-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="338e0-106">この手順の実行は前の 7 つの記録で作成されているデータに依存します。</span><span class="sxs-lookup"><span data-stu-id="338e0-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="338e0-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="338e0-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="338e0-108">分析コード ベースの製品マスターを検索します</span><span class="sxs-lookup"><span data-stu-id="338e0-108">Find the dimension-based product master</span></span>
1. <span data-ttu-id="338e0-109">[リリース済製品の保守] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="338e0-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="338e0-110">[リリース済製品] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="338e0-110">Click Released products.</span></span>
3. <span data-ttu-id="338e0-111">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="338e0-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="338e0-112">この一連の 8 つの記録において、最初の記録を作成した分析コード ベースの製品マスターを選択します。</span><span class="sxs-lookup"><span data-stu-id="338e0-112">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="338e0-113">コンフィギュレーションを作成します</span><span class="sxs-lookup"><span data-stu-id="338e0-113">Create configurations</span></span>
1. <span data-ttu-id="338e0-114">[技術アクション ペイン] で、[コンフィギュレーション管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="338e0-114">On the Engineering Action Pane, click Maintain configurations.</span></span>
2. <span data-ttu-id="338e0-115">[コンフィギュレーション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="338e0-115">Click Configure.</span></span>
3. <span data-ttu-id="338e0-116">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="338e0-116">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="338e0-117">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="338e0-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="338e0-118">最初のコンフィギュレーション グループのどの品目も選択できます。</span><span class="sxs-lookup"><span data-stu-id="338e0-118">Select any of the items in the first configuration group.</span></span>  
5. <span data-ttu-id="338e0-119">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="338e0-119">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="338e0-120">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="338e0-120">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="338e0-121">2 番目のコンフィギュレーション グループから任意の品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="338e0-121">Select any item from the second configuration group.</span></span>  
7. <span data-ttu-id="338e0-122">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="338e0-122">Click OK.</span></span>
8. <span data-ttu-id="338e0-123">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="338e0-123">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="338e0-124">[コンフィギュレーション] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="338e0-124">In the Configuration field, type a value.</span></span>
    * <span data-ttu-id="338e0-125">コンフィギュレーションの識別を容易にするためコンフィギュレーション名を入力します。</span><span class="sxs-lookup"><span data-stu-id="338e0-125">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
10. <span data-ttu-id="338e0-126">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="338e0-126">In the Description field, type a value.</span></span>
    * <span data-ttu-id="338e0-127">内容を説明するために、コンフィギュレーションの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="338e0-127">Enter a description of the configuration to explain what it contains.</span></span>  
11. <span data-ttu-id="338e0-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="338e0-128">Click OK.</span></span>

