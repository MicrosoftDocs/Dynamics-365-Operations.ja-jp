---
title: 分析コードベースのコンフィギュレーションの作成
description: この手順では、分析コード ベース製品のコンフィギュレーションを定義する方法を示します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 584bb558ee0afeaffaeb003e9f1d1b0bca42d19d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920684"
---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="4a66f-103">分析コードベースのコンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="4a66f-103">Create dimension-based configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4a66f-104">この手順では、分析コード ベース製品のコンフィギュレーションを定義する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="4a66f-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="4a66f-105">これは、分析コード ベースのコンフィギュレーションでの組み合わせの作成方法を説明するシリーズの最後の手順です。</span><span class="sxs-lookup"><span data-stu-id="4a66f-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="4a66f-106">この手順の実行は前の 7 つの記録で作成されているデータに依存します。</span><span class="sxs-lookup"><span data-stu-id="4a66f-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="4a66f-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="4a66f-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="4a66f-108">分析コード ベースの製品マスターを検索します</span><span class="sxs-lookup"><span data-stu-id="4a66f-108">Find the dimension-based product master</span></span>

1. <span data-ttu-id="4a66f-109">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4a66f-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="4a66f-110">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="4a66f-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="4a66f-111">この一連の 8 つの記録において、最初の記録を作成した分析コード ベースの製品マスターを選択します。</span><span class="sxs-lookup"><span data-stu-id="4a66f-111">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="4a66f-112">コンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="4a66f-112">Create configurations</span></span>

1. <span data-ttu-id="4a66f-113">**技術** アクション ペインで、**コンフィギュレーション管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a66f-113">On the **Engineering** Action Pane, select **Maintain configurations**.</span></span>
1. <span data-ttu-id="4a66f-114">**コンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a66f-114">Select **Configure**.</span></span>
1. <span data-ttu-id="4a66f-115">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="4a66f-115">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="4a66f-116">**品目番号グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4a66f-116">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="4a66f-117">最初のコンフィギュレーション グループのどの品目も選択できます。</span><span class="sxs-lookup"><span data-stu-id="4a66f-117">Select any of the items in the first configuration group.</span></span>  
1. <span data-ttu-id="4a66f-118">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="4a66f-118">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="4a66f-119">**品目番号グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4a66f-119">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="4a66f-120">2 番目のコンフィギュレーション グループから任意の品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a66f-120">Select any item from the second configuration group.</span></span>  
1. <span data-ttu-id="4a66f-121">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a66f-121">Select **OK**.</span></span>
1. <span data-ttu-id="4a66f-122">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="4a66f-122">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="4a66f-123">**コンフィギュレーション** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a66f-123">In the **Configuration** field, type a value.</span></span>
    * <span data-ttu-id="4a66f-124">コンフィギュレーションの識別を容易にするためコンフィギュレーション名を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a66f-124">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
1. <span data-ttu-id="4a66f-125">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a66f-125">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="4a66f-126">内容を説明するために、コンフィギュレーションの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a66f-126">Enter a description of the configuration to explain what it contains.</span></span>  
1. <span data-ttu-id="4a66f-127">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a66f-127">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]