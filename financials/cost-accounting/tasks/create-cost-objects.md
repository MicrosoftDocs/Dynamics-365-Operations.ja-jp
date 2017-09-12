--- 
title: "原価オブジェクトの作成"
description: "この手順では、データ コネクタ経由で Dynamics 365 for Finance and Operations、Enterprise Edition コスト センターの財務分析コードを原価計算にインポートすることによって原価対象を作成する方法を示します。"
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 5d43274aed2edbb91fd4e399cb8d45e91646b055
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-cost-objects"></a><span data-ttu-id="8ff55-103">原価オブジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="8ff55-103">Create cost objects</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8ff55-104">この手順では、データ コネクタ経由で Dynamics 365 for Finance and Operations、Enterprise Edition コスト センターの財務分析コードを原価計算にインポートすることによって原価対象を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="8ff55-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="8ff55-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="8ff55-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="8ff55-106">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された原価会計機能です。</span><span class="sxs-lookup"><span data-stu-id="8ff55-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="8ff55-107">新規原価対象を作成する</span><span class="sxs-lookup"><span data-stu-id="8ff55-107">Create new cost objects</span></span>
1. <span data-ttu-id="8ff55-108">[原価計算] > [分析コード] > [原価対象分析コード] の順序で進みます。</span><span class="sxs-lookup"><span data-stu-id="8ff55-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="8ff55-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ff55-109">Click New.</span></span>
3. <span data-ttu-id="8ff55-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8ff55-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="8ff55-111">[分析コードメンバーのデータコネクター] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8ff55-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="8ff55-112">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8ff55-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="8ff55-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ff55-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="8ff55-114">データコネクターを構成する</span><span class="sxs-lookup"><span data-stu-id="8ff55-114">Configure the data connector</span></span>
1. <span data-ttu-id="8ff55-115">「分析コード メンバー プロバイダーのコンフィギュレーション」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ff55-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="8ff55-116">コストセンターを選択し、コストセンターの分析コードを原画計算にインポートします。</span><span class="sxs-lookup"><span data-stu-id="8ff55-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="8ff55-117">[分析コード名称] フィールドでコストを選択します。</span><span class="sxs-lookup"><span data-stu-id="8ff55-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="8ff55-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ff55-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="8ff55-119">コスト センターをインポートする</span><span class="sxs-lookup"><span data-stu-id="8ff55-119">Import cost centers</span></span>
1. <span data-ttu-id="8ff55-120">[分析コード メンバーをインポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ff55-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="8ff55-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ff55-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="8ff55-122">インポートされたコストセンターを表示します。</span><span class="sxs-lookup"><span data-stu-id="8ff55-122">View the imported cost centers</span></span>
1. <span data-ttu-id="8ff55-123">[分析コード メンバーの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ff55-123">Click View dimension members.</span></span>


