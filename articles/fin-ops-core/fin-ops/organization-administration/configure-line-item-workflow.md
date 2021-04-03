---
title: 明細行品目ワークフローのコンフィギュレーション
description: このトピックでは、行項目ワークフローの要素をコンフィギュレーションする方法を説明します。
author: ChrisGarty
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46de2bc3683ed907f1879afc13c60adce261d402
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567018"
---
# <a name="configure-line-item-workflows"></a><span data-ttu-id="f3da2-103">明細行品目ワークフローのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="f3da2-103">Configure line-item workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3da2-104">このトピックでは、行項目ワークフローの要素をコンフィギュレーションする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="f3da2-104">This topic explains how to configure a line-item workflow element.</span></span>

<span data-ttu-id="f3da2-105">行項目ワークフローの要素をコンフィギュレーションするには、ワークフロー エディターで要素を右クリックし、**プロパティ** をクリックして、**プロパティ** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="f3da2-105">To configure a line-item workflow element, in the workflow editor, right-click the element, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="f3da2-106">次の手順に従って、行項目ワークフローの要素をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="f3da2-106">Then use the following procedures to configure the properties of the line-item workflow element.</span></span>

## <a name="name-the-line-item-workflow-element"></a><span data-ttu-id="f3da2-107">行項目ワークフロー要素に名前を付ける</span><span class="sxs-lookup"><span data-stu-id="f3da2-107">Name the line-item workflow element</span></span>

<span data-ttu-id="f3da2-108">行項目ワークフロー要素の名前を入力するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f3da2-108">Follow these steps to enter a name for the line-item workflow element.</span></span>

1. <span data-ttu-id="f3da2-109">左ウィンドウで **基本設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3da2-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="f3da2-110">**名前** フィールドに、行項目ワークフロー要素の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f3da2-110">In the **Name** field, enter a unique name for the line-item workflow element.</span></span>

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a><span data-ttu-id="f3da2-111">同じワークフローですべての行項目を処理するかどうかを指定する</span><span class="sxs-lookup"><span data-stu-id="f3da2-111">Specify whether the same workflow is used to process all line items</span></span>

<span data-ttu-id="f3da2-112">ドキュメントのすべての行項目の処理に、同じワークフローを使用するかどうかを指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f3da2-112">Follow these steps to specify whether the same workflow is used to process all the line items on a document.</span></span>

1. <span data-ttu-id="f3da2-113">左ウィンドウで **基本設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3da2-113">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="f3da2-114">ドキュメントのすべての行項目を同じワークフローで処理する場合は、**すべての品目に対して単一のワークフローを呼び出す** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3da2-114">If the same workflow should process all the line items on a document, click **Invoke a single workflow for all line-items**.</span></span> <span data-ttu-id="f3da2-115">その後、行項目の処理に使用するワークフローを選択します。</span><span class="sxs-lookup"><span data-stu-id="f3da2-115">Then select the workflow to use to process the line items.</span></span>
3. <span data-ttu-id="f3da2-116">ある特定の条件セットを満たす行項目を特定のワークフローで処理する場合は、**それぞれの品目に対してワークフローを呼び出す** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3da2-116">If a specific workflow should process line items that meet a specific set of conditions, click **Invoke a workflow for each line-item**.</span></span> <span data-ttu-id="f3da2-117">次に条件セットを定義するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f3da2-117">Then follow these steps to define the set of conditions:</span></span>

    1. <span data-ttu-id="f3da2-118">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3da2-118">Click **Add**.</span></span>
    2. <span data-ttu-id="f3da2-119">テーブル内の条件を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3da2-119">Select the condition in the table.</span></span>
    3. <span data-ttu-id="f3da2-120">**条件名** タブで、定義する条件セットの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f3da2-120">On the **Condition name** tab, enter a name for the set of conditions that you're defining.</span></span>
    4. <span data-ttu-id="f3da2-121">**条件の追加** をクリックして、条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="f3da2-121">Click **Add condition** to enter a condition.</span></span>
    5. <span data-ttu-id="f3da2-122">必要に応じて、追加条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="f3da2-122">Enter any additional conditions that are required.</span></span>
    6. <span data-ttu-id="f3da2-123">入力した条件セットが正しく構成されていることを検証するには、**テスト** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3da2-123">To verify that the set of conditions that you entered is configured correctly, click **Test**.</span></span> <span data-ttu-id="f3da2-124">**ワークフロー条件のテスト** ページの、**条件の検証** 領域で、レコードを選択して、**テスト** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3da2-124">On the **Test workflow condition** page, in the **Validate condition** area, select a record, and then click **Test**.</span></span> <span data-ttu-id="f3da2-125">システムによってレコードが評価され、定義した条件を満たすかどうかが判定されます。</span><span class="sxs-lookup"><span data-stu-id="f3da2-125">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span> <span data-ttu-id="f3da2-126">**OK**、または **キャンセル** をクリックして、**プロパティ** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="f3da2-126">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

    <span data-ttu-id="f3da2-127">**ワークフロー** タブで、定義した条件セットを満たす行項目の処理に使用するワークフローを選択します。</span><span class="sxs-lookup"><span data-stu-id="f3da2-127">On the **Workflow** tab, select the workflow select the workflow to use to process line items that meet the set of conditions that you defined.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]