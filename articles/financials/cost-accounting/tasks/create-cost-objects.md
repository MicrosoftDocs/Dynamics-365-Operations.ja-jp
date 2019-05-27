---
title: 原価オブジェクトの作成
description: この手順では、データ コネクタ経由で Dynamics 365 for Finance and Operations Enterprise Edition コスト センターの財務分析コードを原価計算にインポートすることによって原価対象を作成する方法を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12de1d51658092fb19f652cef7c1cc78b255b5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543774"
---
# <a name="create-cost-objects"></a><span data-ttu-id="25b02-103">原価オブジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="25b02-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25b02-104">この手順では、データ コネクタ経由で Dynamics 365 for Finance and Operations Enterprise Edition コスト センターの財務分析コードを原価計算にインポートすることによって原価対象を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="25b02-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="25b02-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="25b02-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="25b02-106">この手順は Dynamics 365 for Operations バージョン 1611 に追加された原価計算の機能についての手順です。</span><span class="sxs-lookup"><span data-stu-id="25b02-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="25b02-107">新規原価対象を作成する</span><span class="sxs-lookup"><span data-stu-id="25b02-107">Create new cost objects</span></span>
1. <span data-ttu-id="25b02-108">[原価計算] > [分析コード] > [原価対象分析コード] の順序で進みます。</span><span class="sxs-lookup"><span data-stu-id="25b02-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="25b02-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="25b02-109">Click New.</span></span>
3. <span data-ttu-id="25b02-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="25b02-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="25b02-111">[分析コードメンバーのデータコネクター] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="25b02-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="25b02-112">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="25b02-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="25b02-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="25b02-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="25b02-114">データコネクターを構成する</span><span class="sxs-lookup"><span data-stu-id="25b02-114">Configure the data connector</span></span>
1. <span data-ttu-id="25b02-115">「分析コード メンバー プロバイダーのコンフィギュレーション」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="25b02-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="25b02-116">コストセンターを選択し、コストセンターの分析コードを原画計算にインポートします。</span><span class="sxs-lookup"><span data-stu-id="25b02-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="25b02-117">[分析コード名称] フィールドでコストを選択します。</span><span class="sxs-lookup"><span data-stu-id="25b02-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="25b02-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="25b02-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="25b02-119">コスト センターをインポートする</span><span class="sxs-lookup"><span data-stu-id="25b02-119">Import cost centers</span></span>
1. <span data-ttu-id="25b02-120">[分析コード メンバーをインポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="25b02-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="25b02-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="25b02-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="25b02-122">インポートされたコストセンターを表示します。</span><span class="sxs-lookup"><span data-stu-id="25b02-122">View the imported cost centers</span></span>
1. <span data-ttu-id="25b02-123">[分析コード メンバーの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="25b02-123">Click View dimension members.</span></span>

