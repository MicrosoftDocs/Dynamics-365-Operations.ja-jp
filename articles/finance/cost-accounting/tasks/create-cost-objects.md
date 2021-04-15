---
title: 原価オブジェクトの作成
description: この手順は、データコネクター経由でコスト センターの財務分析コードを原価計算にインポートすることによって原価対象を作成する方法を示します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1219cb15ecec7c156579c5cf7c3a3511a141e00b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810057"
---
# <a name="create-cost-objects"></a><span data-ttu-id="4bd51-103">原価オブジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="4bd51-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4bd51-104">この手順は、データコネクター経由でコスト センターの財務分析コードを原価計算にインポートすることによって原価対象を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="4bd51-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="4bd51-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="4bd51-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="4bd51-106">新規原価対象を作成する</span><span class="sxs-lookup"><span data-stu-id="4bd51-106">Create new cost objects</span></span>
1. <span data-ttu-id="4bd51-107">[原価計算] > [分析コード] > [原価対象分析コード] の順序で進みます。</span><span class="sxs-lookup"><span data-stu-id="4bd51-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="4bd51-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4bd51-108">Click New.</span></span>
3. <span data-ttu-id="4bd51-109">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4bd51-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="4bd51-110">[分析コードメンバーのデータコネクター] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4bd51-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="4bd51-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4bd51-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="4bd51-112">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4bd51-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="4bd51-113">データコネクターを構成する</span><span class="sxs-lookup"><span data-stu-id="4bd51-113">Configure the data connector</span></span>
1. <span data-ttu-id="4bd51-114">「分析コード メンバー プロバイダーのコンフィギュレーション」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4bd51-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="4bd51-115">コストセンターを選択し、コストセンターの分析コードを原画計算にインポートします。</span><span class="sxs-lookup"><span data-stu-id="4bd51-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="4bd51-116">[分析コード名称] フィールドでコストを選択します。</span><span class="sxs-lookup"><span data-stu-id="4bd51-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="4bd51-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4bd51-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="4bd51-118">コスト センターをインポートする</span><span class="sxs-lookup"><span data-stu-id="4bd51-118">Import cost centers</span></span>
1. <span data-ttu-id="4bd51-119">[分析コード メンバーをインポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4bd51-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="4bd51-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4bd51-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="4bd51-121">インポートされたコストセンターを表示します。</span><span class="sxs-lookup"><span data-stu-id="4bd51-121">View the imported cost centers</span></span>
1. <span data-ttu-id="4bd51-122">[分析コード メンバーの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4bd51-122">Click View dimension members.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]