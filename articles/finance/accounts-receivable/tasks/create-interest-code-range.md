---
title: 範囲のある利息コードの作成
description: 利息コードは値の範囲によって異なる利息金額を計算するように設定できます。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d684eedd5b40ee9775ab779c243d05cdc6e01f58
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188858"
---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="4ef17-103">範囲のある利息コードの作成</span><span class="sxs-lookup"><span data-stu-id="4ef17-103">Create an interest code with a range</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4ef17-104">利息コードは値の範囲によって異なる利息金額を計算するように設定できます。</span><span class="sxs-lookup"><span data-stu-id="4ef17-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="4ef17-105">この手順は、利息コードを追加し、その範囲を追加する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="4ef17-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="4ef17-106">[貸方転記および取立] > [利息] > [利息コードの設定] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4ef17-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="4ef17-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ef17-107">Click New.</span></span>
3. <span data-ttu-id="4ef17-108">[利息コード] フィールドで、利息コードの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ef17-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="4ef17-109">[説明] フィールドに、利息コードの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ef17-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="4ef17-110">[月] を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ef17-110">Select Month.</span></span>
6. <span data-ttu-id="4ef17-111">[所得] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="4ef17-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="4ef17-112">[通貨別受取利息] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="4ef17-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="4ef17-113">[元帳転記勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ef17-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="4ef17-114">[範囲別の利息] フィールドで「月」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ef17-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="4ef17-115">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ef17-115">Click Add.</span></span>
11. <span data-ttu-id="4ef17-116">[説明] フィールドに、この通貨と範囲の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ef17-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="4ef17-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ef17-117">Click Save.</span></span>
13. <span data-ttu-id="4ef17-118">[範囲] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ef17-118">Click Ranges.</span></span>
14. <span data-ttu-id="4ef17-119">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ef17-119">Click New.</span></span>
15. <span data-ttu-id="4ef17-120">[開始値] に 0 を入力し、利息を計算するのに使用される月ごとの利率を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ef17-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="4ef17-121">この例の場合、1.5 です。</span><span class="sxs-lookup"><span data-stu-id="4ef17-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="4ef17-122">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ef17-122">Click New.</span></span>
17. <span data-ttu-id="4ef17-123">次の [開始値] に 4 を入力します。これは新しい利息金額の計算をする最初の月です。</span><span class="sxs-lookup"><span data-stu-id="4ef17-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="4ef17-124">4 の月からの利息の計算に使う、月ごとの利率を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ef17-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="4ef17-125">この例の場合、2.0 です。</span><span class="sxs-lookup"><span data-stu-id="4ef17-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="4ef17-126">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ef17-126">Click New.</span></span>
20. <span data-ttu-id="4ef17-127">次の [開始値] に 7 を入力します。これは新しい利息金額の計算をする次の月です。</span><span class="sxs-lookup"><span data-stu-id="4ef17-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="4ef17-128">7 の月からの利息の計算に使う、月ごとの利率を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ef17-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="4ef17-129">この例の場合、2.5 です。</span><span class="sxs-lookup"><span data-stu-id="4ef17-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="4ef17-130">設定を完了するには、[終了] をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="4ef17-130">Click Close to complete the setup.</span></span>
