--- 
title: "新しい製品の作成"
description: "このタスクは、新しい共有製品を作成する方法を示します。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/08/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 81224eb80ba5a66837fa3476c4cb799aa578cec3
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-new-product"></a><span data-ttu-id="cdf84-103">新しい製品の作成</span><span class="sxs-lookup"><span data-stu-id="cdf84-103">Create a new product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cdf84-104">このタスクは、新しい共有製品を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="cdf84-104">This task shows how to create a new shared product.</span></span> <span data-ttu-id="cdf84-105">これは通常、製品デザイナーが実行します。</span><span class="sxs-lookup"><span data-stu-id="cdf84-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="cdf84-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="cdf84-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="cdf84-107">[製品情報管理] > [製品] > [製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cdf84-107">Go to Product information management > Products > Products.</span></span>

## <a name="create-a-product"></a><span data-ttu-id="cdf84-108">製品の作成</span><span class="sxs-lookup"><span data-stu-id="cdf84-108">Create a product</span></span>
1. <span data-ttu-id="cdf84-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cdf84-109">Click New.</span></span>
2. <span data-ttu-id="cdf84-110">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cdf84-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="cdf84-111">番号順序が製品番号に対して設定されていない場合は、手動で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdf84-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
3. <span data-ttu-id="cdf84-112">[製品名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cdf84-112">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="cdf84-113">製品名が検索名の既定値になります。</span><span class="sxs-lookup"><span data-stu-id="cdf84-113">The product name defaults to the search name.</span></span> <span data-ttu-id="cdf84-114">必要に応じて手動でこれを変更できます。</span><span class="sxs-lookup"><span data-stu-id="cdf84-114">You can change this if needed.</span></span>  
4. <span data-ttu-id="cdf84-115">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cdf84-115">Click OK.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="cdf84-116">分析コード グループの設定</span><span class="sxs-lookup"><span data-stu-id="cdf84-116">Set up dimension groups</span></span>
1. <span data-ttu-id="cdf84-117">[分析コード グループ] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="cdf84-117">Click Dimension groups to open the drop dialog.</span></span>
2. <span data-ttu-id="cdf84-118">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cdf84-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf84-119">保管分析コード グループにより、製品の各トランザクションに入力する必要がある保管分析コードと、在庫で追跡される方法が決まります。</span><span class="sxs-lookup"><span data-stu-id="cdf84-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="cdf84-120">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cdf84-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf84-121">追跡用分析コード グループにより、製品の各トランザクションに入力する必要がある追跡用分析コードと、在庫で処理される方法が決まります。</span><span class="sxs-lookup"><span data-stu-id="cdf84-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="cdf84-122">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cdf84-122">Click OK.</span></span>


