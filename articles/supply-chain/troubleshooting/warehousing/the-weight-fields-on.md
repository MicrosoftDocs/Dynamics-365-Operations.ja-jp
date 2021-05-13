---
title: 積荷明細行の重量フィールドが積荷の重量フィールドと一致しない
description: 積荷明細行の重量フィールドが積荷の重量フィールドと一致しない
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 639b82a9d46b74f179d6904d2c3b8e7dfb813b58
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924354"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a><span data-ttu-id="b6bd1-103">積荷明細行の重量フィールドが積荷の重量フィールドと一致しない</span><span class="sxs-lookup"><span data-stu-id="b6bd1-103">The weight fields on load lines don't match the weight fields on the load</span></span>

<span data-ttu-id="b6bd1-104">エラー コード: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span><span class="sxs-lookup"><span data-stu-id="b6bd1-104">Error codes: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span></span>

## <a name="symptoms"></a><span data-ttu-id="b6bd1-105">現象</span><span class="sxs-lookup"><span data-stu-id="b6bd1-105">Symptoms</span></span>

<span data-ttu-id="b6bd1-106">システムは次のエラー メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-106">The system shows the following error message:</span></span>

> <span data-ttu-id="b6bd1-107">積荷明細行の重量フィールドが積荷 %1 の重量フィールドと一致しません。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-107">The weight fields on load lines do not match the weight fields on load %1.</span></span> <span data-ttu-id="b6bd1-108">倉庫の積荷重量の整合性チェックを実行して、重量フィールドを再計算します。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-108">Run the Warehouse load weight consistency check to recalculate the weight fields.</span></span>

## <a name="cause"></a><span data-ttu-id="b6bd1-109">原因</span><span class="sxs-lookup"><span data-stu-id="b6bd1-109">Cause</span></span>

<span data-ttu-id="b6bd1-110">**正味重量** フィールドおよび **風袋重量** フィールドは、積荷明細行で *0* (ゼロ) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-110">The **Net weight** and **Tara weight** fields are set to *0* (zero) on the load line.</span></span> <span data-ttu-id="b6bd1-111">ただし、製品の重量測定では、重量フィールドが *0* に設定されていません。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-111">However, the weight fields aren't set to *0* for the weight measurements on the product.</span></span> <span data-ttu-id="b6bd1-112">重量フィールドが積荷明細行に設定されていない場合、積荷明細行の数量を修正すると、積荷に対する重量の計算が不正確になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-112">When weight fields aren't set on the load line, any corrections of the quantity on the load line might cause incorrect weight calculation on the load.</span></span> <span data-ttu-id="b6bd1-113">この問題は、積荷明細行の作成後に製品の重量が変更された場合に発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-113">This issue might occur if the weights on the product have been changed since the load line was created.</span></span>

## <a name="resolution"></a><span data-ttu-id="b6bd1-114">解像度</span><span class="sxs-lookup"><span data-stu-id="b6bd1-114">Resolution</span></span>

<span data-ttu-id="b6bd1-115">既定では、積荷明細行を作成すると、製品の重量フィールドが積荷明細行に入力されます。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-115">By default, when a load line is created, the weight fields from the product are entered on it.</span></span> <span data-ttu-id="b6bd1-116">重量が 0 の場合は、*倉庫積荷重量の整合性チェック* 機能を使用して再計算できます。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-116">If the weight is zero, you can recalculate it by using the *Warehouse load weight consistency check* functionality.</span></span>

1. <span data-ttu-id="b6bd1-117">**システム管理 \> 定期処理のタスク \> データベース \> 整合性チェック** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-117">Go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="b6bd1-118">**整合性チェック** ダイアログ ボックスで、**モジュール** フィールドを *倉庫管理* に設定します。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-118">In the **Consistency check** dialog box, set the **Module** field to *Warehouse management*.</span></span>
1. <span data-ttu-id="b6bd1-119">**確認/修正** フィールドを *エラーの修正* に設定します。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-119">Set the **Check/Fix** field to *Fix error*.</span></span>
1. <span data-ttu-id="b6bd1-120">チェック ボックス リストで、**倉庫積荷重量の整合性チェック** チェックボックスをオンにし、このチェック ボックスの行だけが強調表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-120">In the checkbox list, select the **Warehouse load weight consistency check** checkbox, and make sure that only the row for this checkbox is highlighted.</span></span>
1. <span data-ttu-id="b6bd1-121">チェックボックス リストの上部にある省略記号ボタン (**...**) を選択し、メニューの **ダイアログ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-121">At the top of the checkbox list, select the ellipsis button (**...**), and then select **Dialog** on the menu.</span></span>
1. <span data-ttu-id="b6bd1-122">**倉庫積荷重量の整合性チェック** ダイアログ ボックスで、次のフィールドを設定して、整合性チェックを実行する基準を指定します。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-122">In the **Warehouse load weight consistency check** dialog box, set the following fields to specify the criteria that the consistency check should run for:</span></span>

    - <span data-ttu-id="b6bd1-123">**積荷 ID**: 積荷 ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-123">**Load ID:** Specify a load ID.</span></span> <span data-ttu-id="b6bd1-124">すべての積荷 ID を確認するには、これを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-124">Leave this blank to check all load IDs.</span></span>
    - <span data-ttu-id="b6bd1-125">**品目番号**: 品目番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-125">**Item number:** Specify an item number.</span></span> <span data-ttu-id="b6bd1-126">すべての積荷を確認するには、これを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-126">Leave this blank to check all items.</span></span>
    - <span data-ttu-id="b6bd1-127">**積荷の重量を常に再計算する**: このオプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-127">**Always recalculate weight on loads:** Set this option to *Yes*.</span></span>
    - <span data-ttu-id="b6bd1-128">**積荷明細行の重量の上書きを許可する**: このオプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-128">**Allow overwrite of weight on load lines:** Set this option to *Yes*.</span></span>

1. <span data-ttu-id="b6bd1-129">**OK** を選択して、**倉庫積荷重量の整合性チェック** ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-129">Select **OK** to close the **Warehouse load weight consistency check** dialog box.</span></span>
1. <span data-ttu-id="b6bd1-130">省略記号ボタンを選択して、メニューの **実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-130">Select the ellipsis button, and then select **Execute** on the menu.</span></span>

<span data-ttu-id="b6bd1-131">重量は、指定した基準に基づいて再計算されます。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-131">The weight is recalculated based on the criteria that you specified.</span></span> <span data-ttu-id="b6bd1-132">**メッセージの詳細** リンクを選択して、整合性チェックの結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="b6bd1-132">Select the **Message details** link to view the result of the consistency check.</span></span>
