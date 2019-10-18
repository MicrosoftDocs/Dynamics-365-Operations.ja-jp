---
title: 原価要素の作成
description: 原価計算の原価要素を作成するにはいくつかの方法があります。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cceec1d52e1b5b2a05525c8d96f46dece17363b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187800"
---
# <a name="create-cost-elements"></a><span data-ttu-id="9ccf0-103">原価要素の作成</span><span class="sxs-lookup"><span data-stu-id="9ccf0-103">Create cost elements</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9ccf0-104">原価計算の原価要素を作成するにはいくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="9ccf0-105">この手順では、データ コネクタ経由で主勘定をインポートしてコスト要素を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="9ccf0-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="9ccf0-107">この手順は Dynamics 365 for Operations バージョン 1611 に追加された原価計算の機能についての手順です。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="9ccf0-108">新規コスト要素を作成する</span><span class="sxs-lookup"><span data-stu-id="9ccf0-108">Create new cost elements</span></span>
1. <span data-ttu-id="9ccf0-109">[原価計算] > [分析コード] > [コスト要素分析コード] の順序で進みます。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="9ccf0-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-110">Click New.</span></span>
3. <span data-ttu-id="9ccf0-111">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9ccf0-112">[分析コードメンバーのデータコネクター] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="9ccf0-113">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="9ccf0-114">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="9ccf0-115">データコネクターを構成する</span><span class="sxs-lookup"><span data-stu-id="9ccf0-115">Configure the data connector</span></span>
1. <span data-ttu-id="9ccf0-116">「分析コード メンバー プロバイダーのコンフィギュレーション」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="9ccf0-117">[勘定科目表] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="9ccf0-118">[共有勘定科目表使用の共有] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="9ccf0-119">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-119">Click New.</span></span>
4. <span data-ttu-id="9ccf0-120">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9ccf0-121">基準を満たす口座にフィルターを適用できます。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="9ccf0-122">[主勘定から] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="9ccf0-123">[主勘定へ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="9ccf0-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="9ccf0-125">主勘定のインポート</span><span class="sxs-lookup"><span data-stu-id="9ccf0-125">Import main accounts</span></span>
1. <span data-ttu-id="9ccf0-126">[分析コード メンバーをインポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="9ccf0-127">主勘定は原価計算にインポートされ、コスト要素として使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="9ccf0-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="9ccf0-129">コスト要素としてインポートされた勘定を表示する</span><span class="sxs-lookup"><span data-stu-id="9ccf0-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="9ccf0-130">[分析コード メンバーの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-130">Click View dimension members.</span></span>
    * <span data-ttu-id="9ccf0-131">原価が適用される事業のコスト要素として、インポートされた勘定科目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9ccf0-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  

