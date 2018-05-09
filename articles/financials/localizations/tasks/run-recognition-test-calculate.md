--- 
title: "認識テストの実行と個別資産の減損損失の計算 (日本)"
description: "このタスクは、認識テストの実行方法および個々の資産の減損金額の計算方法について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 83d4577ecde0984f08aa1495d4eee325dbcf7ce9
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="run-the-recognition-test-and-calculate-the-impairment-amount-on-individual-assets-japan"></a><span data-ttu-id="7f0b3-103">認識テストの実行と個別資産の減損損失の計算 (日本)</span><span class="sxs-lookup"><span data-stu-id="7f0b3-103">Run the recognition test and calculate the impairment amount on individual assets (Japan)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7f0b3-104">このタスクは、認識テストの実行方法および個々の資産の減損金額の計算方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7f0b3-104">This task walks you through running the recognition test and calculating the impairment amount on individual assets.</span></span>



<span data-ttu-id="7f0b3-105">このタスクを完了するには、個々の資産の減損インジケーターを管理しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f0b3-105">Before you can complete this task, you must maintain impairment indicators on individual assets.</span></span>



<span data-ttu-id="7f0b3-106">このタスクは デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="7f0b3-106">This task was created using the demo data company JPMF.</span></span>


## <a name="impairment-recognition-test"></a><span data-ttu-id="7f0b3-107">減損認識テスト</span><span class="sxs-lookup"><span data-stu-id="7f0b3-107">Impairment recognition test</span></span>
1. <span data-ttu-id="7f0b3-108">[固定資産] > [定期処理タスク] > [個別資産の減損] > [減損認識テスト] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f0b3-108">Go to Fixed assets > Periodic tasks > Impairment on individual assets > Impairment recognition test.</span></span>
2. <span data-ttu-id="7f0b3-109">[クエリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f0b3-109">Click Query.</span></span>
3. <span data-ttu-id="7f0b3-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="7f0b3-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7f0b3-111">この例では、[固定資産グループ] 行を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f0b3-111">For this example, select the Fixed asset group row.</span></span>  
4. <span data-ttu-id="7f0b3-112">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f0b3-112">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="7f0b3-113">例: TOOL-M</span><span class="sxs-lookup"><span data-stu-id="7f0b3-113">Example: TOOL-M</span></span>  
5. <span data-ttu-id="7f0b3-114">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f0b3-114">Click OK.</span></span>
    * <span data-ttu-id="7f0b3-115">減損インジケーターを構成済の、3つの固定資産が表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f0b3-115">Confirm that three fixed assets with impairment indicators configured will be displayed.</span></span>  
    * <span data-ttu-id="7f0b3-116">TOOLM-000006 に減損損失調整はありませんが、TOOLM-000007 および TOOLM-000008 の減損損失調整はそれぞれ -1,750,000.00 と -2,250,000.00 です。</span><span class="sxs-lookup"><span data-stu-id="7f0b3-116">TOOLM-000006 does not have any impairment adjustment, whereas TOOLM-000007 and TOOLM-000008 have -1,750,000.00 and -2,250,000.00 respectively.</span></span>  
6. <span data-ttu-id="7f0b3-117">[減損の保存] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="7f0b3-117">Click Save impairment to open the drop dialog.</span></span>
7. <span data-ttu-id="7f0b3-118">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f0b3-118">In the Description field, type a value.</span></span>
8. <span data-ttu-id="7f0b3-119">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f0b3-119">In the Date field, enter a date.</span></span>
9. <span data-ttu-id="7f0b3-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f0b3-120">Click OK.</span></span>
    * <span data-ttu-id="7f0b3-121">減損固定資産の確認フォームが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7f0b3-121">The Confirmation form of the impaired fixed assets is displayed.</span></span>  
    * <span data-ttu-id="7f0b3-122">[減損テスト ID] は有効です。</span><span class="sxs-lookup"><span data-stu-id="7f0b3-122">The Impairment test ID is issued.</span></span>     <span data-ttu-id="7f0b3-123">後に [提案と転記] で使用するため、[減損テスト ID] を忘れないでください。</span><span class="sxs-lookup"><span data-stu-id="7f0b3-123">Remember the Impairment_test_ID for later use in Propose and post.</span></span>   


