---
title: 認識テストの作成および確認
description: 日本では、減損は 2 つの主要なステップにより処理されます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetImpairmentManageTestResult_JP, AssetImpairmentRecognition_JP
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9dbeb757794c2d3a065d35666d0f8175c72f0a65
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849014"
---
# <a name="create-and-confirm-recognition-test"></a><span data-ttu-id="f2fc3-103">認識テストの作成および確認</span><span class="sxs-lookup"><span data-stu-id="f2fc3-103">Create and confirm recognition test</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2fc3-104">日本では、減損は 2 つの主要なステップにより処理されます。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-104">For Japan, impairment is conducted in two main steps.</span></span> <span data-ttu-id="f2fc3-105">最初のステップは、減損が必要かどうかをテストすることです。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-105">The first step is to test whether an impairment is needed.</span></span> <span data-ttu-id="f2fc3-106">2 番目のステップでは、必要に応じて減損金額を計算します。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-106">The second step is to calculate the impairment amount if needed.</span></span> 



<span data-ttu-id="f2fc3-107">このタスクでは、認識テストでの 2 つのステップのプロセスの実行および転記の準備方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-107">Use this task to learn how to run the two step process in a recognition test and get it ready for posting.</span></span> 



<span data-ttu-id="f2fc3-108">この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-108">In order to complete this procedure, the Fixed Asset configuration key must be selected.</span></span>



<span data-ttu-id="f2fc3-109">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-109">This procedure was created using the demo data company JPMF.</span></span>

1. <span data-ttu-id="f2fc3-110">[固定資産] > [定期処理タスク] > [減損の認識] の順に移動します (方法 I: CGU より大きいグループを使用)。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-110">Go to Fixed assets > Periodic tasks > Impairment recognition (Method I: on a bigger group than CGU).</span></span>
    * <span data-ttu-id="f2fc3-111">方法 2 の場合は、[固定資産] > [定期処理タスク] > [減損認識] の順に移動します (方法 II: CGU への共有資産/営業権の帳簿価額の配賦)。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-111">For method 2, go to Fixed assets > Periodic tasks > Impairment recognition (Method II: Allocate carrying amount of shared asset / goodwill to CGUs).</span></span>  
2. <span data-ttu-id="f2fc3-112">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-112">Click New.</span></span>
3. <span data-ttu-id="f2fc3-113">[CGU グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-113">In the CGU group field, type a value.</span></span>
4. <span data-ttu-id="f2fc3-114">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-114">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="f2fc3-115">減損トランザクションを転記する日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-115">Enter the date on which to post the impairment transaction.</span></span>  
5. <span data-ttu-id="f2fc3-116">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-116">In the Description field, type a value.</span></span>
6. <span data-ttu-id="f2fc3-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-117">Click Save.</span></span>
7. <span data-ttu-id="f2fc3-118">[認識テスト] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-118">Click Recognition test.</span></span>
8. <span data-ttu-id="f2fc3-119">[テストの実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-119">Click Run test.</span></span>
    * <span data-ttu-id="f2fc3-120">認識テストでは、正味簿価額の合計を各資産グループの値引前キャッシュ フローと比較して、減損額の計算が必要かどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-120">The recognition test will compare the sum of the net book value with the undiscounted cash flow of each cash generating unit to determine if calculation of the impairment amount is needed.</span></span>  
9. <span data-ttu-id="f2fc3-121">[計算] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-121">Click Calculate.</span></span>
    * <span data-ttu-id="f2fc3-122">テスト結果が「はい」の場合は、認識テストでは正味簿価額から回収可能金額を差し引いて減損の調整金額を決定します。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-122">If the test result is 'Yes', then the recognition test will subtract the recoverable amount from the net book value to determine the impairment adjustment amount.</span></span> <span data-ttu-id="f2fc3-123">減損の調整額は転記のため、固定資産ごとに配分されます。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-123">The impairment adjustment amount is distributed to each of the fixed assets for posting.</span></span>  
10. <span data-ttu-id="f2fc3-124">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-124">Click Confirm.</span></span>
    * <span data-ttu-id="f2fc3-125">確認済の認識テストだけを転記することができます。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-125">You only can post confirmed recognition tests.</span></span>  
11. <span data-ttu-id="f2fc3-126">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2fc3-126">Click Yes.</span></span>

