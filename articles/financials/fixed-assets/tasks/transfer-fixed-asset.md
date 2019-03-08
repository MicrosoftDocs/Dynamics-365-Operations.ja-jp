---
title: 固定資産の移動
description: このタスク ガイドは、財務分析コード セットのいずれかから新しい財務分析コード セットに、固定資産帳簿の財務情報を転送します。
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb8a5b94d9a0bb510daa2a698524e0c380597991
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "357200"
---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="f9bd0-103">固定資産の移動</span><span class="sxs-lookup"><span data-stu-id="f9bd0-103">Transfer a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9bd0-104">このタスク ガイドは、財務分析コード セットのいずれかから新しい財務分析コード セットに、固定資産帳簿の財務情報を転送します。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="f9bd0-105">これは USMF の法人に対して経理担当ロールとデモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="f9bd0-106">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-106">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="f9bd0-107">一覧で、固定資産の移動先の場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="f9bd0-108">[アクション] ウィンドウで、[固定資産] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-108">On the Action Pane, click Fixed asset.</span></span>
4. <span data-ttu-id="f9bd0-109">[固定資産の移動] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-109">Click Transfer fixed assets.</span></span>
5. <span data-ttu-id="f9bd0-110">[移動日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-110">In the Transfer date field, enter a date.</span></span>
6. <span data-ttu-id="f9bd0-111">転送についてのコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-111">Enter comments to describe the transfer.</span></span>
    * <span data-ttu-id="f9bd0-112">この一覧には、固定資産のすべての帳簿が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="f9bd0-113">新しい財務分析コード セットに転送する帳簿をマークします。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="f9bd0-114">この一覧には、選択した帳簿の既存の財務分析コード値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="f9bd0-115">選択した固定資産帳簿の更新に必要な財務分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="f9bd0-116">[財務分析コード] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-116">In the Financial dimension field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="f9bd0-117">必要に応じて他の財務分析コード値を設定します。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="f9bd0-118">転送が行われると、値が入力されているか、または空白のままであるかに関わらず、すべての財務分析コード値が変更されます。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="f9bd0-119">たとえば、「BusinessUnit」の値を入力し、「CostCenter」と「財務分析コード部門」を空白のままにした場合。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="f9bd0-120">勘定構造により CostCenter と部門に空白の値を入力できる場合は、転送によって各価値モデルの CostCenter に新しい値が挿入され、BusinessUnit および部門は空白となります。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="f9bd0-121">[更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-121">Click Update.</span></span>
    * <span data-ttu-id="f9bd0-122">転送を終了する前に変更をプレビューする機会があります。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="f9bd0-123">固定資産の帳簿を転送する前に結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="f9bd0-124">[転送] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9bd0-124">Click Transfer.</span></span>

