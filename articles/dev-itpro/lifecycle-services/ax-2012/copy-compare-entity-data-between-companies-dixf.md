---
title: "企業間のエンティティ データのコピーと比較 (AX 2012)"
description: "このトピックでは、Microsoft Dynamics AX 2012 R2 および Microsoft Dynamics AX 2012 R3 の企業間でエンティティ データをコピーする方法についての情報を提供します。"
author: kfend
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 17841
ms.assetid: 6b2d300e-daec-441d-b19f-d3701296623d
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c430bafdb4acb3be7e30531e291633231662fa13
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="copying-and-comparing-entity-data-between-companies-ax-2012"></a><span data-ttu-id="986f8-103">企業間のエンティティ データのコピーと比較 (AX 2012)</span><span class="sxs-lookup"><span data-stu-id="986f8-103">Copying and comparing entity data between companies (AX 2012)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="986f8-104">企業間でエンティティ データをコピーするこのプロセスは、Microsoft Dynamics AX 2012 R2 および Microsoft Dynamics AX 2012 R3 でのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="986f8-104">This process for copying entity data between companies is supported only for Microsoft Dynamics AX 2012 R2 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="986f8-105">データのインポート/エクスポート フレームワークの以前のバージョンを実行している場合は、「[チュートリアル: (DIXF、DMF) の会社間でデータをコピー](copy-data-between-companies-dixf.md)」の指示を参照します。</span><span class="sxs-lookup"><span data-stu-id="986f8-105">If you are running an earlier version of the Data Import/Export Framework, see the instructions in [Walkthrough: Copy data between companies (DIXF, DMF)](copy-data-between-companies-dixf.md).</span></span> <span data-ttu-id="986f8-106">このトピックでは、次のプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="986f8-106">This topic describes the following processes:</span></span>

-   <span data-ttu-id="986f8-107">会社間でエンティティ データをコピーします</span><span class="sxs-lookup"><span data-stu-id="986f8-107">Copy entity data between companies</span></span>
-   <span data-ttu-id="986f8-108">会社間でエンティティ データを比較します</span><span class="sxs-lookup"><span data-stu-id="986f8-108">Compare entity data between companies</span></span>

## <a name="copy-entity-data-between-companies"></a><span data-ttu-id="986f8-109">会社間でエンティティ データをコピーします</span><span class="sxs-lookup"><span data-stu-id="986f8-109">Copy entity data between companies</span></span>
<span data-ttu-id="986f8-110">会社または法人間でエンティティ データをコピーするには、[会社間でエンティティ データをコピー] ウィザードを使用します。</span><span class="sxs-lookup"><span data-stu-id="986f8-110">To copy entity data between companies or legal entities, use the Copy entity data between companies wizard.</span></span>

1.  <span data-ttu-id="986f8-111">**データのインポート/エクスポート フレームワーク** &gt; **共通** &gt; **会社間でエンティティ データをコピー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="986f8-111">Click **Data import export framework** &gt; **Common** &gt; **Copy entity data between companies**.</span></span> <span data-ttu-id="986f8-112">**会社間でのエンティティ データのコピー** **ウィザード**が開きます。</span><span class="sxs-lookup"><span data-stu-id="986f8-112">The **Copy entity data between companies** **Wizard** opens.</span></span>
2.  <span data-ttu-id="986f8-113">**次へ&gt;** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="986f8-113">Click **Next &gt;**.</span></span>
3.  <span data-ttu-id="986f8-114">**比較処理グループの名前指定**ページで、比較処理グループに後で識別用の名前を指定し、**次へ&gt;** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="986f8-114">On the **Name the comparison processing group** page, provide a name for the processing group, so that you can identify it later, and then click **Next &gt;**.</span></span>
4.  <span data-ttu-id="986f8-115">**比較するエンティティの選択**ページで、コピーする 1 つまたは複数のソース エンティティを選択して、**&gt;** をクリックしてそれらをコピーするエンティティの一覧に追加し、**次へ&gt;** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="986f8-115">On the **Select entities to compare** page, select one or more source entities to copy, click **&gt;** to add them to the list of entities to copy, and then click **Next &gt;**.</span></span>
5.  <span data-ttu-id="986f8-116">**ソースとターゲットの会社の選択**ページで、1 つのソースの会社、および 1 つまたは複数ターゲット会社がデータをコピーします。</span><span class="sxs-lookup"><span data-stu-id="986f8-116">On the **Select source and target companies** page, select one source company, and one or more target companies to copy the data to.</span></span>
6.  <span data-ttu-id="986f8-117">バッチ ジョブのパラメーターを入力し、実行時に使用するバッチ タスクの数を入力して**次 &gt;** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="986f8-117">Enter parameters for the batch job, enter the number of batch tasks to use when the batch is run, and then click **Next &gt;**.</span></span>
7.  <span data-ttu-id="986f8-118">エンティティ データを他の会社にコピーするには、**完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="986f8-118">Click **Finish** to copy the entity data to the other companies.</span></span> <span data-ttu-id="986f8-119">ターゲット企業にステージングするために挿入されたレコードの数を示す情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="986f8-119">An Infolog message is displayed that describes how many records were inserted into staging then into the target company.</span></span> <span data-ttu-id="986f8-120">**コピー処理グループ** フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="986f8-120">The **Copy processing group** form opens.</span></span>
8.  <span data-ttu-id="986f8-121">**実行履歴**をクリックし、コピーされたエンティティを確認します。</span><span class="sxs-lookup"><span data-stu-id="986f8-121">Click **Execution history** to review the entities that have been copied.</span></span>

## <a name="compare-entity-data-between-companies"></a><span data-ttu-id="986f8-122">会社間でエンティティ データを比較します</span><span class="sxs-lookup"><span data-stu-id="986f8-122">Compare entity data between companies</span></span>
<span data-ttu-id="986f8-123">企業または法人のエンティティ データを比較するには、**企業間のエンティティ データを比較** **ウィザード**を使用します。</span><span class="sxs-lookup"><span data-stu-id="986f8-123">To compare entity data between companies or legal entities, use the **Compare entity data between companies** **Wizard**.</span></span> <span data-ttu-id="986f8-124">データを比較した後は、特定の値を選択し他のシステムにコピーできます。</span><span class="sxs-lookup"><span data-stu-id="986f8-124">After you have compared data, you can select specific values to copy to the other system.</span></span>

1.  <span data-ttu-id="986f8-125">**データのインポート/エクスポート フレームワーク** &gt; **共通** &gt; **会社間でエンティティ データを比較**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="986f8-125">Click **Data import export framework** &gt; **Common** &gt; **Compare entity data between companies**.</span></span> <span data-ttu-id="986f8-126">**会社間でのエンティティ データの比較** ウィザードが開きます。</span><span class="sxs-lookup"><span data-stu-id="986f8-126">The **Compare entity data between companies** wizard opens.</span></span>
2.  <span data-ttu-id="986f8-127">**次へ&gt;** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="986f8-127">Click **Next &gt;**.</span></span>
3.  <span data-ttu-id="986f8-128">**比較処理グループの名前指定**ページで、比較処理グループに後で識別用の名前を指定し、**次へ&gt;** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="986f8-128">On the **Name the comparison processing group** page, provide a name for the comparison processing group, so that you can identify it later, and then click **Next &gt;**.</span></span>
4.  <span data-ttu-id="986f8-129">**比較するエンティティの選択**ページの、使用可能なエンティティの一覧で、比較する 1 つ以上のソース エンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="986f8-129">On the **Select entities to compare** page, in the list of available entities, select one or more source entities to compare.</span></span> <span data-ttu-id="986f8-130">選択したエンティティを比較するためにエンティティのリストに追加するには **&gt;** をクリックし、**次へ &gt;** をクリックします</span><span class="sxs-lookup"><span data-stu-id="986f8-130">Click **&gt;** to add the selected entities to the list of entities to compare, and then click **Next &gt;**.</span></span>
5.  <span data-ttu-id="986f8-131">**ソースとターゲットの会社の選択**ページで、1 つのソースの会社、および 1 つまたは複数ターゲット会社とデータを比較します。</span><span class="sxs-lookup"><span data-stu-id="986f8-131">On the **Select source and target companies** page, select one source company, and one or more target companies to compare the data to.</span></span>
6.  <span data-ttu-id="986f8-132">バッチ ジョブのパラメーターを入力し、実行時に使用するバッチ タスクの数を入力して**次 &gt;** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="986f8-132">Enter parameters for the batch job, enter the number of batch tasks to use when the batch is run, and then click **Next &gt;**.</span></span>
7.  <span data-ttu-id="986f8-133">エンティティ データを他の会社の情報と比較する処理グループを作成するには、**完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="986f8-133">Click **Finish** to create the processing group that compares the entity data to the information in the other companies.</span></span> <span data-ttu-id="986f8-134">**比較処理グループ** フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="986f8-134">The **Comparison processing group** form opens.</span></span>

    | <span data-ttu-id="986f8-135">**メモ**</span><span class="sxs-lookup"><span data-stu-id="986f8-135">**Note**</span></span>                                                                                                                                                   |
    |------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="986f8-136">**比較処理グループ**が処理グループをリストしない場合、それを閉じて**会社間でのエンティティのデータを比較**をクリックしてを再び開きます。</span><span class="sxs-lookup"><span data-stu-id="986f8-136">If the **Comparison processing group** does not list a processing group, then close it, and click **Compare entity data between companies** to re-open it.</span></span> |

8.  <span data-ttu-id="986f8-137">**&gt;&gt;** をクリックし、**比較結果**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="986f8-137">Click **&gt;&gt;**, and then click **Comparison results**.</span></span> <span data-ttu-id="986f8-138">**比較結果** フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="986f8-138">The **Comparison results** form opens.</span></span> <span data-ttu-id="986f8-139">このフォームは、比較されたソース会社とエンティティをリストし、エンティティがソースにのみ表示されるのか、ターゲットにのみ表示されるのか、そして同じ値が存在するのか、異なる値が存在するのかを示します。</span><span class="sxs-lookup"><span data-stu-id="986f8-139">This form lists the source company and the entities that were compared, and indicates whether an entity appears only in the source or only in the target, and whether identical values exist or different values exist.</span></span>
9.  <span data-ttu-id="986f8-140">詳細を表示し、特定の行のデータをある企業から別の企業にコピーするには、一覧から 1 つの企業のエンティティを選択し、**詳細** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="986f8-140">To view details, and copy specific rows of data from one company to another, select an entity from one company in the list, and then click **Details**.</span></span> <span data-ttu-id="986f8-141">**比較** フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="986f8-141">The **Comparison** form opens.</span></span> <span data-ttu-id="986f8-142">タイトルで比較されているエンティティを一覧表示し、そこには**ソース内のみ**、**ターゲット内のみ**、**合致**、および**異なる**タブがあります。</span><span class="sxs-lookup"><span data-stu-id="986f8-142">It lists the entities being compared in the title, and has **Only in source**, **Only in target**, **Identical**, and **Different** tabs.</span></span> <span data-ttu-id="986f8-143">**合致**を除くすべてのタブで、**移動ステータス**列があり、エンティティの列が続きます。</span><span class="sxs-lookup"><span data-stu-id="986f8-143">On all tabs, except **Identical**, there is a **Transfer status** column, followed by the columns for the entity.</span></span> <span data-ttu-id="986f8-144">条件を満たすに各レコードは、該当するタブに表示されます。**異なる**タブ上で、エンティティの各列は 2 回リストされます。</span><span class="sxs-lookup"><span data-stu-id="986f8-144">Each record that meets the criteria is listed on the appropriate tab. On the **Different** tab, each column in the entity is listed twice.</span></span> <span data-ttu-id="986f8-145">ソース システムからのデータは左側にあり、ターゲット システムからのデータは右側にあります。</span><span class="sxs-lookup"><span data-stu-id="986f8-145">Data from the source system is on the left, and data from the target system is on the right.</span></span>
10. <span data-ttu-id="986f8-146">レコードをソースからターゲットにコピーするには、**Only in source** タブでコピーするレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="986f8-146">To copy a record from source to target, select the records that you want to copy in the **Only in source** tab.</span></span>
11. <span data-ttu-id="986f8-147">レコードをターゲットからソースにコピーするには、**Only in target** タブでコピーするレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="986f8-147">To copy a record from target to source, select the records that you want to copy in the **Only in target** tab.</span></span>
12. <span data-ttu-id="986f8-148">両方のシステムに存在するレコードをソース システムと一致するように更新するには、コピーするレコードを **別の** タブで選択します。</span><span class="sxs-lookup"><span data-stu-id="986f8-148">To update a record that exists in both systems to match the source system, select the records that you want to copy in the **Different** tab.</span></span>
13. <span data-ttu-id="986f8-149">変更するすべてのレコードの選択が完了したら、**更新** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="986f8-149">When you have selected all of the records that you would like to modify, click **Update**.</span></span>
14. <span data-ttu-id="986f8-150">**ソースからターゲットにデータを出力**フォームで、バッチ処理を使用するかどうかを決定し、バッチ グループを識別して **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="986f8-150">In the **Write data from source to target** form, determine whether to use batch processing, identify a batch group, and then click **OK**.</span></span> <span data-ttu-id="986f8-151">データは指定したシステムに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="986f8-151">The data will be written to the specified systems.</span></span> <span data-ttu-id="986f8-152">データを変更した後、行の**移動ステータス**は、**完了**に変更されます。</span><span class="sxs-lookup"><span data-stu-id="986f8-152">After the data has been modified, the **Transfer status** for a row will change to **Completed**.</span></span>





