---
title: 資産エラー原価管理
description: このトピックでは、資産管理の資産エラー原価管理について説明します。
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 597e30db346e882a7002709be52ad1c2d0576099
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019955"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="d8691-103">資産エラー原価管理</span><span class="sxs-lookup"><span data-stu-id="d8691-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d8691-104">資産管理では、資産エラー登録で原価を計算して、予算原価と比較した実際原価の概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="d8691-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs.</span></span> <span data-ttu-id="d8691-105">実際原価は、転記されたトランザクションに基づいています。</span><span class="sxs-lookup"><span data-stu-id="d8691-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="d8691-106">日付は、現象が記録されたエラー日付を示します。</span><span class="sxs-lookup"><span data-stu-id="d8691-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="d8691-107">**資産管理** > **照会** > **資産エラー** > **資産エラー原価管理** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="d8691-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="d8691-108">**資産エラー原価管理** ダイアログでは、必要に応じて計算に含める財務分析コード セットを選択します。</span><span class="sxs-lookup"><span data-stu-id="d8691-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="d8691-109">原価がゼロの結果を表示しない場合は、**ゼロをスキップ** トグル ボタンで "はい" を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8691-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="d8691-110">**レベル** フィールドを使用すると、機能的な場所に関する原価管理明細行の詳細度を指定できます。</span><span class="sxs-lookup"><span data-stu-id="d8691-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="d8691-111">たとえば、フィールドに "1" の番号を挿入し、複数レベルの機能的な場所構造がある場合、機能的な場所に対するすべての資産エラー原価管理の明細行が最上位レベルに表示されます。したがって明細行の時間は、下位レベルにある機能的な場所から追加される場合があります。</span><span class="sxs-lookup"><span data-stu-id="d8691-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="d8691-112">**レベル** フィールドに数値 "0" を挿入すると、関連するすべての機能的な場所レベルですべての資産エラー原価管理の明細行を示す、詳細な結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d8691-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="d8691-113">検索を制限する場合は、**対象に含めるレコード** クイック タブで特定の資産、エラー日付、およびエラーの原因を選択できます。</span><span class="sxs-lookup"><span data-stu-id="d8691-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="d8691-114">**OK** をクリックして、計算を開始します。</span><span class="sxs-lookup"><span data-stu-id="d8691-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="d8691-115">**グループ化** ボタンをクリックすると、計算の必要な詳細レベルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d8691-115">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="d8691-116">選択した **グループ化** ボタンが強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="d8691-116">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="d8691-117">ボタンをクリックして、有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="d8691-117">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="d8691-118">例</span><span class="sxs-lookup"><span data-stu-id="d8691-118">Example</span></span>

<span data-ttu-id="d8691-119">この例では、資産エラー原価管理の計算を示します。</span><span class="sxs-lookup"><span data-stu-id="d8691-119">This example shows an asset fault cost control calculation.</span></span>

- <span data-ttu-id="d8691-120">**元の予算** フィールドでは、作業指示書予測からの予算原価が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d8691-120">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="d8691-121">**実際原価** フィールドには、作業指示書の転記済原価が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d8691-121">The **Actual cost** field shows posted costs on work orders.</span></span> 
- <span data-ttu-id="d8691-122">**確定済み費用** フィールドには、作業指示書に関連して会社が確定した原価合計が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d8691-122">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>

    ![図 1](media/05-controlling-and-reporting.png)

<span data-ttu-id="d8691-124">エラーの設定方法に関しては、[エラー管理](../setup-for-work-orders/fault-management.md) トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d8691-124">For information about how to set up faults, see the [Fault management](../setup-for-work-orders/fault-management.md) topic.</span></span>
