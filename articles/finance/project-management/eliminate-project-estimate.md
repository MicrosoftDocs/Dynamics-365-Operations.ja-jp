---
title: プロジェクト見積の削除
description: このトピックでは、完了後のプロジェクト見積の削除について説明します。
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410238"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="0305b-103">プロジェクト見積の削除</span><span class="sxs-lookup"><span data-stu-id="0305b-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0305b-104">プロジェクト見積は、プロジェクトに対して見積もりおよび予定されている作業の財務ビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="0305b-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="0305b-105">プロジェクトの見積を使用するには、プロジェクトを見積プロジェクトに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="0305b-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="0305b-106">見積プロジェクトは、常に既存のプロジェクトをベースに作成しますが、複数のプロジェクトが 1 つの見積プロジェクトを参照できます。</span><span class="sxs-lookup"><span data-stu-id="0305b-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="0305b-107">見積プロジェクトに関連付けることができるのは固定価格プロジェクトと投資プロジェクトのみで、これらのプロジェクトは、見積プロジェクトと同じプロジェクト グループに属している必要があります。</span><span class="sxs-lookup"><span data-stu-id="0305b-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="0305b-108">見積プロジェクトを削除するには、完了している必要があります。</span><span class="sxs-lookup"><span data-stu-id="0305b-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="0305b-109">次の手順では、見積を削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0305b-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="0305b-110">**プロジェクト管理および会計** > **すべてのプロジェクト** の順に移動し、プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="0305b-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="0305b-111">**管理** タブで、**見積** を選択し、**見積** ページで **削除** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="0305b-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="0305b-112">**一般** タブの **見積の削除** ページで 、次のオプションを設定します:</span><span class="sxs-lookup"><span data-stu-id="0305b-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="0305b-113">**期間コード**: 期間コードを選択して、適切な見積プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="0305b-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="0305b-114">**見積日付**: 削除の適切な見積日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="0305b-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="0305b-115">**WIP 警告での削除**: このオプションを有効にすると、進行中の作業 (WIP) に関連付けられた見積が削除されるときに通知されます。</span><span class="sxs-lookup"><span data-stu-id="0305b-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="0305b-116">このオプションが有効でない場合、見積済ではないトランザクションが存在すると、削除を続行できません。</span><span class="sxs-lookup"><span data-stu-id="0305b-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="0305b-117">このオプションは、削除が見積プロジェクトに適用される場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="0305b-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="0305b-118">定期処理転記を使用している場合は使用できません。</span><span class="sxs-lookup"><span data-stu-id="0305b-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="0305b-119">この設定は、**プロジェクト パラメータ** ページの **見積** タブの **見積済みではないトランザクションが存在する場合削除を許可する** フィールド グループの設定と連動します。</span><span class="sxs-lookup"><span data-stu-id="0305b-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="0305b-120">**ステージを完了に設定**: このオプションを有効にすると、削除を実行した後、見積プロジェクトのステージを **完了済** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="0305b-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="0305b-121">**見積リストを印刷**: 見積リストを印刷するときに含める情報を選択します。</span><span class="sxs-lookup"><span data-stu-id="0305b-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="0305b-122">**情報ログの表示**: このオプションを有効にすると、情報ログが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0305b-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="0305b-123">**転記日付**: 見積の元帳転記日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="0305b-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="0305b-124">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0305b-124">Select **OK**.</span></span>
5. <span data-ttu-id="0305b-125">削除プロセスが完了すると、削除済見積プロジェクトが負の値で表示されます。</span><span class="sxs-lookup"><span data-stu-id="0305b-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="0305b-126">見積を削除する予定がない場合は、削除された見積を選択し、**削除の取消** を選択できます。</span><span class="sxs-lookup"><span data-stu-id="0305b-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
