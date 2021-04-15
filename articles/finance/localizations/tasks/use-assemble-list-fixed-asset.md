---
title: 固定資産の組み立て一覧の使用
description: 日本では、在庫品目を固定資産に移転できます。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetComponentList_JP, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 70efba7ecb429767102b2e7804c8526dfc7c1255
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813407"
---
# <a name="use-assemble-list-of-a-fixed-asset"></a><span data-ttu-id="95743-103">固定資産の組み立て一覧の使用</span><span class="sxs-lookup"><span data-stu-id="95743-103">Use assemble list of a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="95743-104">日本では、在庫品目を固定資産に移転できます。</span><span class="sxs-lookup"><span data-stu-id="95743-104">In Japan, you can transfer an inventory item to a fixed asset.</span></span> 



<span data-ttu-id="95743-105">このタスクでは、組み立てリストを使用して在庫品目を使用すると同時に、固定資産を作成するプロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="95743-105">This task walks you through using the assembly list to consume inventory items and create the fixed asset at the same time.</span></span>



<span data-ttu-id="95743-106">このタスクは デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="95743-106">This task was created using the demo data company JPMF.</span></span>


## <a name="assign-component-in-an-assembly-list"></a><span data-ttu-id="95743-107">組み立て一覧のコンポーネントの割り当て</span><span class="sxs-lookup"><span data-stu-id="95743-107">Assign component in an assembly list</span></span>
1. <span data-ttu-id="95743-108">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="95743-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="95743-109">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="95743-109">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="95743-110">組み立てリストを割り当てる固定資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="95743-110">Select the fixed asset that you want to assign the assembly list to.</span></span>  
3. <span data-ttu-id="95743-111">[アクション] ウィンドウで、[固定資産] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="95743-111">On the Action Pane, click Fixed asset.</span></span>
4. <span data-ttu-id="95743-112">[コンポーネント] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="95743-112">Click Components.</span></span>
5. <span data-ttu-id="95743-113">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="95743-113">Click Add.</span></span>
6. <span data-ttu-id="95743-114">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="95743-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="95743-115">たとえば、「D0001」を入力します。</span><span class="sxs-lookup"><span data-stu-id="95743-115">For example: enter 'D0001'</span></span>  
7. <span data-ttu-id="95743-116">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="95743-116">Click Save.</span></span>

## <a name="use-the-assembly-list-to-post-a-fixed-asset-write-up-transaction"></a><span data-ttu-id="95743-117">組み立て一覧を使用した固定資産評価増トランザクションの転記</span><span class="sxs-lookup"><span data-stu-id="95743-117">Use the assembly list to post a fixed asset write-up transaction</span></span>
1. <span data-ttu-id="95743-118">次の順に移動します: [固定資産] ></span><span class="sxs-lookup"><span data-stu-id="95743-118">Go to Fixed assets > ..</span></span> <span data-ttu-id="95743-119">> [固定資産仕訳帳]。</span><span class="sxs-lookup"><span data-stu-id="95743-119">> Fixed assets journal.</span></span>
2. <span data-ttu-id="95743-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="95743-120">Click New.</span></span>
3. <span data-ttu-id="95743-121">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="95743-121">In the Name field, type a value.</span></span>
4. <span data-ttu-id="95743-122">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="95743-122">Click Lines.</span></span>
5. <span data-ttu-id="95743-123">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="95743-123">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="95743-124">[トランザクション タイプ] フィールドで [評価増調整] を選択します。</span><span class="sxs-lookup"><span data-stu-id="95743-124">In the Transaction type field, select 'Write up adjustment'.</span></span>
7. <span data-ttu-id="95743-125">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="95743-125">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="95743-126">組み立てリストに割り当てた固定資産番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="95743-126">Select the fixed asset number that you have assigned to the assembly list.</span></span>  
8. <span data-ttu-id="95743-127">[借方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="95743-127">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="95743-128">在庫品目の原価を入力します。</span><span class="sxs-lookup"><span data-stu-id="95743-128">Enter the cost of the inventory item.</span></span>  
9. <span data-ttu-id="95743-129">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="95743-129">Click Post.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]