---
title: パラメーター ファイルのアップグレード
description: このトピックでは、Regression suite automation tool (RSAT) で使用されるパラメーター ファイルをアップグレードする方法について説明します。
author: FrankDahl
ms.date: 04/12/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2021-04-12
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d750fc927f3f5f124318bc191702d57a6b88f3cc
ms.sourcegitcommit: 4c880b152e81350f023b944c2ab13e60498e2c7b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2021
ms.locfileid: "6093908"
---
# <a name="upgrade-parameter-files"></a><span data-ttu-id="51e7e-103">パラメーター ファイルのアップグレード</span><span class="sxs-lookup"><span data-stu-id="51e7e-103">Upgrade parameter files</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="51e7e-104">Regression suite automation tool (RSAT) で使用された Microsoft Excel ファイルのパラメーターの形式は、2.0 リリースで変更されました。</span><span class="sxs-lookup"><span data-stu-id="51e7e-104">The format of parameter Microsoft Excel files that are used with Regression suite automation tool (RSAT) changed in the 2.0 release.</span></span> <span data-ttu-id="51e7e-105">現在、形式はより直観的でテスト手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="51e7e-105">The format is now more intuitive and shows test steps.</span></span> <span data-ttu-id="51e7e-106">RSAT バージョン 2.0 以降で作成された新しいテスト ケースによって自動的に新しい形式でパラメーター ファイルが生成されます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-106">New test cases that are created in RSAT version 2.0 and later automatically generate parameter files in the new format.</span></span> <span data-ttu-id="51e7e-107">ただし、バージョン 2.0 より前に作成されたテストでは、古い形式を使用している場合があります。</span><span class="sxs-lookup"><span data-stu-id="51e7e-107">However, you might have tests that were created before version 2.0 and that still use the old format.</span></span> <span data-ttu-id="51e7e-108">古い形式のパラメーター ファイルを使用するテスト ケースの実行は、RSAT によって少なくとも次のメジャー リリースまで引き続きサポートされます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-108">RSAT will continue to support running test cases that use parameter files in the old format at least until the next major release.</span></span> <span data-ttu-id="51e7e-109">RSAT によって古いパラメーター ファイルを新しい形式にアップグレードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-109">RSAT can also upgrade old parameter files to the new format.</span></span>

<span data-ttu-id="51e7e-110">パラメーター ファイルは、Excel で自由に編集できます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-110">Parameter files can be freely edited in Excel.</span></span> <span data-ttu-id="51e7e-111">場合によっては、パラメーター ファイルが完全にアップグレードできなかったり、プロセスを完了するために手作業が必要となります。</span><span class="sxs-lookup"><span data-stu-id="51e7e-111">In some situations, a parameter file can't be fully upgraded, and some manual work is required to complete the process.</span></span> <span data-ttu-id="51e7e-112">次のセクションで、アップグレード プロセスの仕組みについて説明します。</span><span class="sxs-lookup"><span data-stu-id="51e7e-112">The next section explains the mechanics of the upgrade process.</span></span>

## <a name="upgrade-process"></a><span data-ttu-id="51e7e-113">アップグレード プロセス</span><span class="sxs-lookup"><span data-stu-id="51e7e-113">Upgrade process</span></span>

<span data-ttu-id="51e7e-114">アップグレード プロセスでは、フル アップグレードを試行します。</span><span class="sxs-lookup"><span data-stu-id="51e7e-114">The upgrade process tries to do a full upgrade.</span></span> <span data-ttu-id="51e7e-115">ただし、場合によっては、このプロセスを安全に完了できないことがあります。</span><span class="sxs-lookup"><span data-stu-id="51e7e-115">However, in some situations, this process can't be safely completed.</span></span>

<span data-ttu-id="51e7e-116">フル アップグレード プロセスを完了できる場合は、古いパラメーター ファイルが新しいパラメーター ファイルに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-116">When the full upgrade process can be completed, the old parameter file is replaced with a new one.</span></span> <span data-ttu-id="51e7e-117">元のファイルのコピーが作成され、**\_BAK** がファイル名に追加されます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-117">A copy of the original file is created, and **\_BAK** is appended to the file name.</span></span>

<span data-ttu-id="51e7e-118">パラメーター ファイルの一部のみを安全にアップグレードできる場合、元のファイルは変更されません。</span><span class="sxs-lookup"><span data-stu-id="51e7e-118">If only part of the parameter file can be safely upgraded, the original file isn't changed.</span></span> <span data-ttu-id="51e7e-119">代わりに新しいファイルが作成され、**\_PARTIAL** がファイル名に追加されます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-119">Instead, a new file is created, and **\_PARTIAL** is appended to the file name.</span></span> <span data-ttu-id="51e7e-120">部分ファイルには、アップグレードされる可能性がある情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="51e7e-120">The partial file contains the information that could be upgraded.</span></span> <span data-ttu-id="51e7e-121">部分ファイルを使用して元のファイルから欠落している部分を手動で転送し、新しいファイルを完成できます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-121">You can use the partial file to manually transfer missing parts from the original file and complete the new file.</span></span> <span data-ttu-id="51e7e-122">完了したら、元のファイルの名前をバックアップ名に変更します (たとえば、ファイル名に **\_BAK** を追加します)。</span><span class="sxs-lookup"><span data-stu-id="51e7e-122">When you've finished, rename the original file to a backup name (for example, append **\_BAK** to the file name).</span></span> <span data-ttu-id="51e7e-123">その後、ファイル名から **\_PARTIAL** を削除して新しいファイルの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="51e7e-123">Then rename the new file by removing **\_PARTIAL** from the file name.</span></span> <span data-ttu-id="51e7e-124">その結果、新しいファイルは新しいパラメーター ファイルになります。</span><span class="sxs-lookup"><span data-stu-id="51e7e-124">The new file then becomes the new parameter file.</span></span>

> [!NOTE]
> <span data-ttu-id="51e7e-125">古いパラメーター ファイルは、新しいファイルの準備ができるまでそのまま使用できます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-125">You can continue to use the old parameter file until the new file is ready.</span></span> <span data-ttu-id="51e7e-126">パラメーター ファイル用の古いフォーマットが、RSAT によって少なくとも次のメジャー リリースまで引き続きサポートされます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-126">RSAT will continue to support the old format for parameter files at least until the next major release.</span></span>

<span data-ttu-id="51e7e-127">通常、アップグレード プロセスでは未編集のパラメーター ファイルをアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-127">The upgrade process can usually upgrade unedited parameter files.</span></span> <span data-ttu-id="51e7e-128">また、ファイル内でセル値だけが変更されたファイルをアップグレードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-128">It can also upgrade files where only cell values have been changed in the file.</span></span> <span data-ttu-id="51e7e-129">ただし、追加のセルが追加され参照されている場合は、アップグレード プロセスを自動的に完了することはできません。</span><span class="sxs-lookup"><span data-stu-id="51e7e-129">However, if additional cells have been added and referenced, the upgrade process can't be completed automatically.</span></span> <span data-ttu-id="51e7e-130">この場合、部分ファイルには **\#MISSING** の値を持つセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-130">In this case, the partial file will include cells that have the value **\#MISSING**.</span></span> <span data-ttu-id="51e7e-131">この値は、セル参照が欠落していることを示します。</span><span class="sxs-lookup"><span data-stu-id="51e7e-131">This value indicates that cell references are missing.</span></span> <span data-ttu-id="51e7e-132">元のパラメーター ファイルの情報を新しい部分ファイルに手動で追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="51e7e-132">You must manually add the information from the original parameter file to the new partial file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="51e7e-133">今から、部分ファイルに追加するのと同様に、パラメーター ファイルの新しい **CustomParameters** シートに新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="51e7e-133">From now on, add new cells to the new **CustomParameters** sheet in the parameter file, just as they are added in the partial file.</span></span>

<span data-ttu-id="51e7e-134">RSAT の 2.2 以降のリリースで、パラメーター ファイルには **CustomParameters** という名前のシートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="51e7e-134">In RSAT release 2.2 and later, the parameter file has a sheet that is named **CustomParameters**.</span></span> <span data-ttu-id="51e7e-135">このシートは、将来のパラメーター ファイルのアップグレードに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-135">This sheet is included to help future-proof the upgrade of parameter files.</span></span> <span data-ttu-id="51e7e-136">セルを追加する場合は、このシートにセルを追加します。</span><span class="sxs-lookup"><span data-stu-id="51e7e-136">If you add cells, add them to this sheet.</span></span>

<span data-ttu-id="51e7e-137">古いパラメーター ファイルにセルを追加してそのセルに名前を割り当てた場合、名前付きセルはその値が他のセルを参照しない限りアップグレード中に自動的に **CustomParameters** シートに移動されます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-137">If you added a cell to the old parameter file and assigned a name to that cell, the named cell is automatically moved to the **CustomParameters** sheet during the upgrade, provided that its value doesn't reference other cells.</span></span>

<span data-ttu-id="51e7e-138">追加したセルの部分ファイルへの移動を完了した後、**TestCaseSteps** シートの参照に **\#MISSING** という値がある場合、**CustomParameters** シートの関連するセルに一致するように参照を変更します。</span><span class="sxs-lookup"><span data-stu-id="51e7e-138">After you've finished moving your added cells to the partial file, if any references on the **TestCaseSteps** sheet have **\#MISSING** as the value, change the references so that they match the relevant cells on the **CustomParameters** sheet.</span></span> <span data-ttu-id="51e7e-139">原則的には、セル識別子 (たとえば、**E4**) ではなく、割り当てられた名前 (たとえば、**MyQuantity**) でセルを参照します。</span><span class="sxs-lookup"><span data-stu-id="51e7e-139">Ideally, you should always reference cells by their assigned name (for example, **MyQuantity**), not by the cell identifier (for example, **E4**).</span></span>

> [!NOTE]
> <span data-ttu-id="51e7e-140">ベスト プラクティスとして、**ComstomerParameters** シートに追加されるすべてのセルに名前を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="51e7e-140">As a best practice, you should assign names to any cells that are added to the **CustomerParameters** sheet.</span></span> <span data-ttu-id="51e7e-141">その後、テスト ケース ステップから名前でセルを参照します。</span><span class="sxs-lookup"><span data-stu-id="51e7e-141">Then reference the cells by name from test case steps.</span></span>

<span data-ttu-id="51e7e-142">アップグレード後、テスト ケースを実行して、新しいパラメーター ファイルによって予期される結果が生成されるのを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="51e7e-142">After the upgrade, you should run your test cases to make sure that the new parameter file produces the expected results.</span></span> <span data-ttu-id="51e7e-143">アップグレードが完全に完了した場合と、アップグレードで手作業が必要な場合の両方にこの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="51e7e-143">Complete this step both when the upgrade was fully completed and when the upgrade required manual work.</span></span>

<span data-ttu-id="51e7e-144">新しいファイルの作成とテストが完了すると、バックアップと部分ファイルを削除できます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-144">When you've finished creating and testing the new files, you can delete the backup and partial files.</span></span>

## <a name="run-the-parameter-file-upgrade-process"></a><span data-ttu-id="51e7e-145">パラメーター ファイルのアップグレード プロセスの実行</span><span class="sxs-lookup"><span data-stu-id="51e7e-145">Run the parameter file upgrade process</span></span>

<span data-ttu-id="51e7e-146">パラメーター ファイルをアップグレードするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="51e7e-146">To upgrade the parameter files, follow these steps.</span></span>

1. <span data-ttu-id="51e7e-147">RSAT を開きます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-147">Open RSAT.</span></span>
2. <span data-ttu-id="51e7e-148">アップグレードするパラメーター ファイルがあるテスト ケースを選択します。</span><span class="sxs-lookup"><span data-stu-id="51e7e-148">Select that test cases that have the parameter files that you want to upgrade.</span></span>
3. <span data-ttu-id="51e7e-149">**新規** メニューで、**パラメーター ファイルのアップグレード (テスト実行ファイルの自動生成)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="51e7e-149">On the **New** menu, select **Upgrade Parameter files (will auto generate Test Execution files)**.</span></span>

    ![新規メニューのパラメーター ファイルのアップグレード (テスト実行ファイルの自動生成) コマンド](media/new_dropdown_menu.png)

<span data-ttu-id="51e7e-151">選択したケースすべてのパラメーター ファイルがアップグレードされます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-151">The parameter files for all the selected cases are upgraded.</span></span>

<span data-ttu-id="51e7e-152">アップグレード プロセスでは、パラメーター ファイルが既に新しい形式であるテスト ケースがスキップされます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-152">The upgrade process skips test cases where the parameter file is already in the new format.</span></span> <span data-ttu-id="51e7e-153">パラメーター ファイルは、**Custom Parameters** シートを含む場合アップグレードされたと見なされます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-153">A parameter file is considered upgraded if it contains the **CustomParameters** sheet.</span></span>

<span data-ttu-id="51e7e-154">アップグレード プロセスが完了した場合、概要を示すメッセージ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-154">When the upgrade process is completed, a message box appears that shows a summary.</span></span> <span data-ttu-id="51e7e-155">この概要には、次の情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="51e7e-155">The summary includes the following information:</span></span>

+ <span data-ttu-id="51e7e-156">アップグレード用にマークされた選択済みのテスト ケースの総数。</span><span class="sxs-lookup"><span data-stu-id="51e7e-156">The total number of selected test cases that were marked for upgrade.</span></span>
+ <span data-ttu-id="51e7e-157">正常にアップグレードされた数。</span><span class="sxs-lookup"><span data-stu-id="51e7e-157">The number of successful upgrades.</span></span> <span data-ttu-id="51e7e-158">これらのアップグレード用として、新しいパラメーター ファイルおよび **\_BAK** ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="51e7e-158">For these upgrades, there are new parameter files and **\_BAK** files.</span></span>
+ <span data-ttu-id="51e7e-159">失敗したアップグレードの数。</span><span class="sxs-lookup"><span data-stu-id="51e7e-159">The number of failed upgrades.</span></span> <span data-ttu-id="51e7e-160">これらのアップグレード用として、新しい **\_PARTIAL** ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="51e7e-160">For these upgrades, there are new **\_PARTIAL** files.</span></span>
+ <span data-ttu-id="51e7e-161">スキップされたアップグレードの数。</span><span class="sxs-lookup"><span data-stu-id="51e7e-161">The number of skipped upgrades.</span></span>
+ <span data-ttu-id="51e7e-162">結果の説明。</span><span class="sxs-lookup"><span data-stu-id="51e7e-162">An explanation of the results.</span></span>

<span data-ttu-id="51e7e-163">次の図は、メッセージ ボックスの概要の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="51e7e-163">The following illustration shows an example of the summary message box.</span></span>

![メッセージ ボックスの概要](media/upgrade_summary.png)

<span data-ttu-id="51e7e-165">失敗したアップグレードについては、テスト ケース タイトルの横にある黄色の三角警告記号を選択することで、詳細情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-165">For a failed upgrade, you can find more information by selecting the yellow triangular warning symbol next to the test case title.</span></span> <span data-ttu-id="51e7e-166">次の図は、表示されるメッセージ ボックスの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="51e7e-166">The following illustration shows an example of the message box that appears.</span></span>

![失敗したアップグレードに対する警告メッセージ ボックス](media/upgrade_triangle_error.png)

> [!IMPORTANT]
> <span data-ttu-id="51e7e-168">アップグレードは、繰り返し実行できます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-168">You can run the upgrade repeatedly.</span></span> <span data-ttu-id="51e7e-169">この場合、新しくアップグレードされたパラメーター ファイルはスキップされます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-169">In this case, newly upgraded parameter files will be skipped.</span></span> <span data-ttu-id="51e7e-170">ただし、新しい部分ファイルによって既存の部分ファイルが上書きされます。</span><span class="sxs-lookup"><span data-stu-id="51e7e-170">However, new partial files will overwrite existing partial files.</span></span> <span data-ttu-id="51e7e-171">アップグレードを再実行する前に、すべての部分ファイルを完成し、名前を変更することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="51e7e-171">We recommend that you complete all partial files and rename them before you rerun the upgrade.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
