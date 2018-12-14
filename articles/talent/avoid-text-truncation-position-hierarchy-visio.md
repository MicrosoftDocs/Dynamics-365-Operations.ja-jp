---
title: "職位階層および Visio へのエクスポートでのテキストの切り捨てを回避します。"
description: "このトピックでは、顧客が Microsoft Dynamics 365 for Talent で職位階層を表示したときに、個人名と職位の名前が切り捨てられる問題を解決する方法について説明します。 テキストの切り捨ては、スクリーン ショットを取ったり、階層を印刷するのを難しくする可能性があります。"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: b688a396e3b384aedb06c470b1634150ae7aa038
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---

# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a><span data-ttu-id="f9bab-104">職位階層および Visio へのエクスポートでのテキストの切り捨てを回避します。</span><span class="sxs-lookup"><span data-stu-id="f9bab-104">Avoid text truncation on the position hierarchy and export to Visio</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f9bab-105">**払出**</span><span class="sxs-lookup"><span data-stu-id="f9bab-105">**Issue**</span></span>

<span data-ttu-id="f9bab-106">顧客が Microsoft Dynamics 365 for Talent で職位階層を表示するとき、個人名と職位の名前は切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="f9bab-106">When a customer views the position hierarchy in Microsoft Dynamics 365 for Talent, the names of individuals and positions are truncated.</span></span> <span data-ttu-id="f9bab-107">したがって、スクリーン ショットを取ったり、階層を印刷および配布することが難しくなります。</span><span class="sxs-lookup"><span data-stu-id="f9bab-107">Therefore, it can be difficult to take a screenshot, or to print and distribute the hierarchy.</span></span>

![職位階層](media/position-h.png)

<span data-ttu-id="f9bab-109">**原因**</span><span class="sxs-lookup"><span data-stu-id="f9bab-109">**Cause**</span></span>

<span data-ttu-id="f9bab-110">この動作は仕様です。</span><span class="sxs-lookup"><span data-stu-id="f9bab-110">This behavior is by design.</span></span>

<span data-ttu-id="f9bab-111">**解像度**</span><span class="sxs-lookup"><span data-stu-id="f9bab-111">**Resolution**</span></span>

<span data-ttu-id="f9bab-112">残念ながら、ユーザーがテキストのサイズを簡単に変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="f9bab-112">Unfortunately, users can't easily change the size of the text.</span></span> <span data-ttu-id="f9bab-113">ただし、Talent から職位階層をエクスポートし、Microsoft Visio にインポートすることはできます。</span><span class="sxs-lookup"><span data-stu-id="f9bab-113">However, you can export the position hierarchy out of Talent and then import it into Microsoft Visio.</span></span> <span data-ttu-id="f9bab-114">次の記事は Microsoft Dynamics AX 2012 用に書かれたものですが、そのプロセスは Talent にも適用されます: [Microsoft Visio に職位階層をエクスポートする](https://docs.microsoft.com/en-us/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio)。</span><span class="sxs-lookup"><span data-stu-id="f9bab-114">Although the following article was written for Microsoft Dynamics AX 2012, the process still applies to Talent: [Export a position hierarchy to Microsoft Visio](https://docs.microsoft.com/en-us/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span></span>

<span data-ttu-id="f9bab-115">Visio にエクスポートするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f9bab-115">Follow these steps to export to Visio.</span></span>

1. <span data-ttu-id="f9bab-116">Talent で、**職位**リスト ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="f9bab-116">In Talent, open the **Positions** list page.</span></span>

    <span data-ttu-id="f9bab-117">組織構造図に詳細情報を含めるには、**職位**リストにフィールドを追加して、この手順の後半でウィザードを使用するときに利用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="f9bab-117">To include more information in the organization structure diagram, add fields to the **Positions** list, so that they are available when you use the wizard later in this procedure.</span></span>

2. <span data-ttu-id="f9bab-118">アクション ウィンドウで、**Microsoft Office で開く**ボタンを選択し、次に **Excel にエクスポート**で、**職位**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9bab-118">On the Action Pane, select the **Open in Microsoft Office** button, and then, under **Export to Excel**, select **Positions**.</span></span> <span data-ttu-id="f9bab-119">または、Ctrl + T キーを押します。</span><span class="sxs-lookup"><span data-stu-id="f9bab-119">Alternatively, press Ctrl+T.</span></span>

    ![Excel に職位リスト ページをエクスポートする](media/org-admin.png)

3. <span data-ttu-id="f9bab-121">エクスポートする Excel ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="f9bab-121">Save the Excel file that is exported.</span></span>

    ![Excel のダイアログ ボックスへエクスポートする](media/export-excel.png)

4. <span data-ttu-id="f9bab-123">Visio では、**Visio - 新規作成**を選択してから、**業務**テンプレート カテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="f9bab-123">In Visio, select **Visio - Create New**, and select the **Business** template category.</span></span>

    ![新しいダイアグラム](media/new.png)

5. <span data-ttu-id="f9bab-125">**組織図のウィザード**を選択してから、**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9bab-125">Select **Organization Chart Wizard**, and then select **Create**.</span></span>

    ![組織図のウィザードのダイアログ ボックス](media/orgchart-wizard.png)

6. <span data-ttu-id="f9bab-127">**既にファイルまたはデータベースに保存されている情報**を選択してから、**次へ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9bab-127">Select **Information that's already stored in a file or database**, and then select **Next**.</span></span>

    ![組織図のウィザード 1](media/orgchart-wizard7.png)

7. <span data-ttu-id="f9bab-129">**テキスト、Org Plus (\*.txt)、または Excel ファイル**を選択してから**次へ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9bab-129">Choose **A text, Org Plus (\*.txt), or Excel file**, and then select **Next**.</span></span>

    ![組織図のウィザード 2](media/orgchart-wizard3.png)

8. <span data-ttu-id="f9bab-131">職位階層を含む、エクスポートした Excel ファイルを参照して選択し、**次へ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9bab-131">Browse to select the exported Excel file that contains the position hierarchy, and then select **Next**.</span></span>

    ![組織図のウィザード 3](media/orgchart-wizard2.png)

9. <span data-ttu-id="f9bab-133">**名前**フィールドを**職位**に設定し、**報告先**フィールドを**報告先職位**に設定してから、**次へ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9bab-133">Set the **Name** field to **Position**, set the **Reports to** field to **Reports to position**, and then select **Next**.</span></span>

    ![組織図のウィザード 4](media/orgchart-wizard1.png)

10. <span data-ttu-id="f9bab-135">各ノードに表示するフィールドを選択してから、**次へ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9bab-135">Select the fields that should be shown on each node, and then select **Next**.</span></span>

    ![組織図のウィザード 5](media/orgchart-wizard5.png)

11. <span data-ttu-id="f9bab-137">**職位**列に**図形のデータ フィールド**リストを追加してから、**次へ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9bab-137">Add the **Position** column to the **Shape Data fields** list, and then select **Next**.</span></span>

    ![組織図のウィザード 6](media/orgchart-wizard6.png)

12. <span data-ttu-id="f9bab-139">図は現在使用できません。</span><span class="sxs-lookup"><span data-stu-id="f9bab-139">Pictures aren't currently available.</span></span> <span data-ttu-id="f9bab-140">このため、次のページで**次へ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9bab-140">Therefore, on the next page, select **Next**.</span></span>
13. <span data-ttu-id="f9bab-141">**ウィザードで組織図をページに自動的に分割する**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9bab-141">Select **I want the wizard to automatically break my organization chart across pages**.</span></span>

    ![組織図のウィザード 7](media/orgchart-wizard4.png)

14. <span data-ttu-id="f9bab-143">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9bab-143">Select **Finish**.</span></span>

    <span data-ttu-id="f9bab-144">構造にない職位がある場合、ダイアグラムに含めることが求められます。</span><span class="sxs-lookup"><span data-stu-id="f9bab-144">If there are any positions that aren't in the structure, you're asked to include them in the diagram.</span></span>

<span data-ttu-id="f9bab-145">Visio で生成されたダイアグラムは、個別のワークシートに各マネージャを表示します。</span><span class="sxs-lookup"><span data-stu-id="f9bab-145">The diagram that is generated in Visio shows each manager on a separate worksheet.</span></span>

<span data-ttu-id="f9bab-146">ダイアグラムに含めるように選択したフィールドに基づいて、各ノードは Visio ファイルが生成されるときに適切な情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="f9bab-146">Based on the fields that you selected to include in the diagram, each node shows the appropriate information when the Visio file is generated.</span></span>

![階層ダイアグラム](media/hierarchy.png)

<span data-ttu-id="f9bab-148">**追加のオプション**</span><span class="sxs-lookup"><span data-stu-id="f9bab-148">**Additional option**</span></span>

<span data-ttu-id="f9bab-149">Talent では、**人員**ワークスペースを使用して、いくつかの階層関連の情報を表示できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="f9bab-149">In Talent, you might also be able to use the **People** workspace to view some hierarchy-related information.</span></span>

