---
title: 作業指示書へのエラーの追加
description: このトピックでは、資産管理における作業指示書へのエラー登録を追加する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 083ceca9605ad044c172ba7aa23739d170f8c301
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019307"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="0905e-103">作業指示書へのエラーの追加</span><span class="sxs-lookup"><span data-stu-id="0905e-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="0905e-104">エラー デザイナーで設定されたエラーを作業指示書に追加できます。</span><span class="sxs-lookup"><span data-stu-id="0905e-104">You can add faults that were set up in the fault designer to a work order.</span></span> <span data-ttu-id="0905e-105">1 つ以上のエラー レコードを、作業指示書で選択された資産に使用される資産タイプに接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0905e-105">One or more fault records must be connected to the asset types that are used for the asset that is selected in the work order.</span></span> <span data-ttu-id="0905e-106">設定の詳細については、[エラー管理](../setup-for-work-orders/fault-management.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0905e-106">For more information about the setup, see [Fault management](../setup-for-work-orders/fault-management.md).</span></span>

1. <span data-ttu-id="0905e-107">**資産管理** > **共通** > **作業指示書** > **すべての作業指示書** または **有効な作業指示書** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="0905e-107">Select **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="0905e-108">エラー登録を行う作業指示書を選択し、アクション ウィンドウの **作業指示書** タブの、**資産** グループで **資産エラー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0905e-108">Select the work order to make a fault registration on, and then, on the Action Pane, on the **Work order** tab, in the **Asset** group, select **Asset fault**.</span></span>

3. <span data-ttu-id="0905e-109">**現象** クイック タブの、**明細行の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0905e-109">On the **Symptoms** FastTab, select **Add line**.</span></span> <span data-ttu-id="0905e-110">**エラー** フィールドには、エラー番号が連番で自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="0905e-110">A sequential fault number is automatically entered in the **Fault** field.</span></span>

4. <span data-ttu-id="0905e-111">**エラー現象** フィールドで、該当する現象を選択します。</span><span class="sxs-lookup"><span data-stu-id="0905e-111">In the **Fault symptom** field, select the relevant symptom.</span></span>

5. <span data-ttu-id="0905e-112">**エラー領域** フィールドおよび **エラー タイプ** フィールドで、適切な値を選択します。</span><span class="sxs-lookup"><span data-stu-id="0905e-112">In the **Fault area** and **Fault type** fields, select the appropriate values.</span></span>

6. <span data-ttu-id="0905e-113">**エラー日付** フィールドには、現在の日付が自動的に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="0905e-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="0905e-114">必要に応じて別の日付を選択できます。</span><span class="sxs-lookup"><span data-stu-id="0905e-114">You can select a different date as you require.</span></span>

7. <span data-ttu-id="0905e-115">**選択した現象の原因** クイック タブで、問題の原因を説明する明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0905e-115">On the **Causes for selected symptom** FastTab, add a line to describe the cause of the issue.</span></span>

8. <span data-ttu-id="0905e-116">**選択した現象の救済** クイック タブで、問題の実行可能なソリューションを説明する明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0905e-116">On the **Remedies for selected symptom** FastTab, add a line to describe a possible solution to the issue.</span></span>

9. <span data-ttu-id="0905e-117">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0905e-117">Select **Save**.</span></span>

<span data-ttu-id="0905e-118">下の図は、エラー登録の例を示します。</span><span class="sxs-lookup"><span data-stu-id="0905e-118">The illustration below shows an example of a fault registration.</span></span>

![図 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="0905e-120">資産エラーの表示</span><span class="sxs-lookup"><span data-stu-id="0905e-120">View asset faults</span></span>

<span data-ttu-id="0905e-121">**資産エラー** の一覧では、資産に登録されているすべてのエラーの概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="0905e-121">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="0905e-122">**資産エラー** リスト ページでは、資産に登録されているすべてのエラーの概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="0905e-122">On the **Asset faults** list page, you can get an overview of all faults that have been registered on assets.</span></span> <span data-ttu-id="0905e-123">ページを開くには、**資産管理** > **照会** > **資産エラー** > **資産エラー** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="0905e-123">To open the page, select **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="0905e-124">資産エラー レポートの印刷</span><span class="sxs-lookup"><span data-stu-id="0905e-124">Print asset fault report</span></span>

<span data-ttu-id="0905e-125">**すべての資産** リスト ページから、すべてのエラー登録を表示する資産エラー レポートおよびエラー統計のグラフィカルな概要を印刷できます。</span><span class="sxs-lookup"><span data-stu-id="0905e-125">From the **All assets** list page, you can print an asset fault report that shows all fault registrations and a graphical overview of fault statistics.</span></span>

1. <span data-ttu-id="0905e-126">**資産管理** >  **共通** >  **資産** > **全資産** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="0905e-126">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="0905e-127">エラー レポートを印刷する資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="0905e-127">Select the asset to print a fault report for.</span></span>

3. <span data-ttu-id="0905e-128">アクション ウィンドウで、**一般** タブの **レポート** グループで、**資産エラー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0905e-128">On the Action Pane, on the **General** tab, in the **Reports** group, select **Asset fault**.</span></span>

4. <span data-ttu-id="0905e-129">特定の期間を入力するか、エラー タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="0905e-129">Enter a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="0905e-130">**OK** を選択してレポートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="0905e-130">Select **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="0905e-131">**資産管理** > **レポート** > **資産** > **資産エラー** の順に選択して、複数の資産または資産タイプに対するエラー レポートを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="0905e-131">To print a fault report for several assets or asset types, select **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

