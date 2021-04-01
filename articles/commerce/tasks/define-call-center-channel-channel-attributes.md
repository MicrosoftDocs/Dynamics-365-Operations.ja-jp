---
title: コール センター チャネルの作成およびチャネル属性の定義
description: この手順では、新しいチャネルを作成し、チャネル属性を定義する方法を説明します。
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e4ef84abcfd0948c46c5312078f2a940840144
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256952"
---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="123b3-103">コール センター チャネルの作成およびチャネル属性の定義</span><span class="sxs-lookup"><span data-stu-id="123b3-103">Create call center channels and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="123b3-104">この手順では、新しい Commerce チャネルを作成し、チャネル属性を定義する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="123b3-104">This procedure walks through creating a new commerce channel and defining channel attributes.</span></span> <span data-ttu-id="123b3-105">このタスクの作成に使用するデモ データの会社は USRT です。</span><span class="sxs-lookup"><span data-stu-id="123b3-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="123b3-106">この手順は、Commerce IT ロールを対象としています。</span><span class="sxs-lookup"><span data-stu-id="123b3-106">This procedure is intended for the Commerce IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="123b3-107">新しい店舗の作成</span><span class="sxs-lookup"><span data-stu-id="123b3-107">Create new store</span></span>
1. <span data-ttu-id="123b3-108">[すべてのワークスペース] > [チャンネルの配置] に移動します。</span><span class="sxs-lookup"><span data-stu-id="123b3-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="123b3-109">[新しいチャネル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-109">Click New channel.</span></span>
3. <span data-ttu-id="123b3-110">[店舗] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-110">Click Store.</span></span>
4. <span data-ttu-id="123b3-111">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="123b3-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="123b3-112">[店舗番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="123b3-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="123b3-113">[倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="123b3-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="123b3-114">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="123b3-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="123b3-115">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="123b3-116">[ストア タイムゾーン] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="123b3-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="123b3-117">[チャネル プロファイル] フィールドで、ドロップ ダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="123b3-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="123b3-118">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="123b3-119">[言語] フィールドで、ドロップ ダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="123b3-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="123b3-120">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="123b3-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="123b3-121">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="123b3-122">[売上税グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="123b3-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="123b3-123">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="123b3-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="123b3-124">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="123b3-125">[顧客のアドレス帳] フィールドで、ドロップ ダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="123b3-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="123b3-126">この店舗に顧客をリンクするために使用するアドレス帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="123b3-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="123b3-127">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="123b3-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="123b3-128">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="123b3-129">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-129">Click Select.</span></span>
22. <span data-ttu-id="123b3-130">[従業員のアドレス帳] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="123b3-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="123b3-131">このチャネルにレジ担当者をリンクするために使用するアドレス帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="123b3-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="123b3-132">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="123b3-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="123b3-133">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="123b3-134">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-134">Click Select.</span></span>
26. <span data-ttu-id="123b3-135">[既定の顧客] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="123b3-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="123b3-136">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="123b3-137">[画面レイアウト] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="123b3-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="123b3-138">[画面レイアウト ID] フィールドで、ドロップ ダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="123b3-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="123b3-139">この店舗の既定の POS の画面レイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="123b3-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="123b3-140">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="123b3-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="123b3-141">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="123b3-142">アクション ペインで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="123b3-143">[チャネル属性] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="123b3-144">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-144">Click New.</span></span>
35. <span data-ttu-id="123b3-145">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="123b3-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="123b3-146">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="123b3-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="123b3-147">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="123b3-148">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-148">Click Save.</span></span>
39. <span data-ttu-id="123b3-149">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="123b3-149">Close the page.</span></span>
40. <span data-ttu-id="123b3-150">アクション ペインで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="123b3-151">[支払方法] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-151">Click Payment methods.</span></span>
42. <span data-ttu-id="123b3-152">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-152">Click New.</span></span>
43. <span data-ttu-id="123b3-153">[支払方法] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="123b3-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="123b3-154">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="123b3-155">[転記] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="123b3-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="123b3-156">[口座番号] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="123b3-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="123b3-157">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-157">Click Save.</span></span>
48. <span data-ttu-id="123b3-158">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="123b3-158">Close the page.</span></span>
49. <span data-ttu-id="123b3-159">アクション ペインで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="123b3-160">[現金申告] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="123b3-161">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-161">Click New.</span></span>
52. <span data-ttu-id="123b3-162">[トランザクション通貨の金額] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="123b3-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="123b3-163">[通貨] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="123b3-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="123b3-164">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="123b3-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="123b3-165">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="123b3-166">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-166">Click Save.</span></span>
57. <span data-ttu-id="123b3-167">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="123b3-167">Close the page.</span></span>
58. <span data-ttu-id="123b3-168">アクション ペインで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="123b3-169">[店舗ロケーター グループの割り当て] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="123b3-170">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-170">Click New.</span></span>
61. <span data-ttu-id="123b3-171">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="123b3-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="123b3-172">[ロケーター グループ] フィールドで、ドロップ ダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="123b3-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="123b3-173">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="123b3-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="123b3-174">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="123b3-175">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="123b3-175">Click Save.</span></span>
66. <span data-ttu-id="123b3-176">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="123b3-176">Close the page.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]