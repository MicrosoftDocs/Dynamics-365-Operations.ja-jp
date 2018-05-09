--- 
title: "原価要素の作成"
description: "原価計算の原価要素を作成するにはいくつかの方法があります。"
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f9eda5f8a2ebf428d7b9b8197a2c8c5f817b9799
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="create-cost-elements"></a><span data-ttu-id="48fd8-103">原価要素の作成</span><span class="sxs-lookup"><span data-stu-id="48fd8-103">Create cost elements</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48fd8-104">原価計算の原価要素を作成するにはいくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="48fd8-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="48fd8-105">この手順では、データ コネクタ経由で主勘定をインポートしてコスト要素を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="48fd8-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="48fd8-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="48fd8-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="48fd8-107">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された原価会計機能です。</span><span class="sxs-lookup"><span data-stu-id="48fd8-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="48fd8-108">新規コスト要素を作成する</span><span class="sxs-lookup"><span data-stu-id="48fd8-108">Create new cost elements</span></span>
1. <span data-ttu-id="48fd8-109">[原価計算] > [分析コード] > [コスト要素分析コード] の順序で進みます。</span><span class="sxs-lookup"><span data-stu-id="48fd8-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="48fd8-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48fd8-110">Click New.</span></span>
3. <span data-ttu-id="48fd8-111">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="48fd8-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="48fd8-112">[分析コードメンバーのデータコネクター] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="48fd8-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="48fd8-113">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="48fd8-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="48fd8-114">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48fd8-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="48fd8-115">データコネクターを構成する</span><span class="sxs-lookup"><span data-stu-id="48fd8-115">Configure the data connector</span></span>
1. <span data-ttu-id="48fd8-116">「分析コード メンバー プロバイダーのコンフィギュレーション」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48fd8-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="48fd8-117">[勘定科目表] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="48fd8-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="48fd8-118">[共有勘定科目表使用の共有] を選択します。</span><span class="sxs-lookup"><span data-stu-id="48fd8-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="48fd8-119">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48fd8-119">Click New.</span></span>
4. <span data-ttu-id="48fd8-120">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="48fd8-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="48fd8-121">基準を満たす口座にフィルターを適用できます。</span><span class="sxs-lookup"><span data-stu-id="48fd8-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="48fd8-122">[主勘定から] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="48fd8-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="48fd8-123">[主勘定へ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="48fd8-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="48fd8-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48fd8-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="48fd8-125">主勘定のインポート</span><span class="sxs-lookup"><span data-stu-id="48fd8-125">Import main accounts</span></span>
1. <span data-ttu-id="48fd8-126">[分析コード メンバーをインポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48fd8-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="48fd8-127">主勘定は原価計算にインポートされ、コスト要素として使用されます。</span><span class="sxs-lookup"><span data-stu-id="48fd8-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="48fd8-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48fd8-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="48fd8-129">コスト要素としてインポートされた勘定を表示する</span><span class="sxs-lookup"><span data-stu-id="48fd8-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="48fd8-130">[分析コード メンバーの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48fd8-130">Click View dimension members.</span></span>
    * <span data-ttu-id="48fd8-131">原価が適用される事業のコスト要素として、インポートされた勘定科目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="48fd8-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  


