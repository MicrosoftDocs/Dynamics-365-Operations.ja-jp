---
title: プリセット レイアウトの使用
description: このトピックでは、Microsoft Dynamics 365 Commerce でのプリセット レイアウトの使用方法について説明します。
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f31dfa1fdbb3732610748abe4a9de851033f2b89
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269892"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="eb4a5-103">プリセット レイアウトの使用</span><span class="sxs-lookup"><span data-stu-id="eb4a5-103">Work with preset layouts</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="eb4a5-104">このトピックでは、Microsoft Dynamics 365 Commerce でのプリセット レイアウトの使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="eb4a5-105">概要</span><span class="sxs-lookup"><span data-stu-id="eb4a5-105">Overview</span></span>

<span data-ttu-id="eb4a5-106">このトピックの手順を実行する前に、[プリセットおよびカスタム レイアウト](templates-layouts-overview.md#preset-and-custom-layouts) を必ずお読みください。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-106">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="eb4a5-107">一般的な概要については、[テンプレートとレイアウトの概要](templates-layouts-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-107">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="eb4a5-108">新しいプリセット レイアウトの作成</span><span class="sxs-lookup"><span data-stu-id="eb4a5-108">Create a new preset layout</span></span>

<span data-ttu-id="eb4a5-109">プリセット レイアウトを作成するには 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-109">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="eb4a5-110">既存のカスタム レイアウトを新しいプリセット レイアウトとして保存するか、またはプリセット レイアウトを最初から作成するかです。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-110">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="eb4a5-111">既存のカスタム レイアウトからプリセット レイアウトを作成</span><span class="sxs-lookup"><span data-stu-id="eb4a5-111">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="eb4a5-112">既存のカスタム レイアウトからプリセット レイアウトを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-112">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="eb4a5-113">現在プリセット レイアウトを使用していないが、サイトの他のページで再利用するモジュール構造を使用している、既存のページを開きます。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-113">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="eb4a5-114">**編集** を選択してページをチェックアウトします。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-114">Select **Edit** to check out the page.</span></span>
1. <span data-ttu-id="eb4a5-115">**新しいレイアウトとして保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-115">Select **Save as new layout**.</span></span> <span data-ttu-id="eb4a5-116">**新しいレイアウトとして保存**ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-116">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="eb4a5-117">プリセット レイアウトに名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-117">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="eb4a5-118">レイアウトから新しいページを作成したり、そのページに切り替えると、入力した値が他の作成者に対して表示されます。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-118">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="eb4a5-119">したがって、ページ作成者にとって有用な値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-119">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="eb4a5-120">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-120">Select **OK**.</span></span>

<span data-ttu-id="eb4a5-121">プリセット レイアウトは、新しいページを作成するとき、または同じテンプレート階層内のページに別のレイアウトを選択するときに、使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-121">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="eb4a5-122">特定のページが現在プリセット レイアウトにバインドされているかどうかをすばやく確認するには、ページ リスト ビューでページを選択し、右側のプロパティ ウィンドウでレイアウト メタデータを検査します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-122">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="eb4a5-123">新しいプリセット レイアウトの作成</span><span class="sxs-lookup"><span data-stu-id="eb4a5-123">Create a new preset layout</span></span>

<span data-ttu-id="eb4a5-124">プリセット レイアウトを最初から作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-124">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="eb4a5-125">左のナビゲーション ウィンドウで、**レイアウト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-125">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="eb4a5-126">**新しいレイアウト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-126">Select **New Layout**.</span></span> <span data-ttu-id="eb4a5-127">**新しいレイアウト**ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-127">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="eb4a5-128">プリセット レイアウトに使用するテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-128">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="eb4a5-129">プリセット レイアウトに名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-129">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="eb4a5-130">レイアウトから新しいページを作成したり、そのページに切り替えると、入力した値が他の作成者に対して表示されます。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-130">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="eb4a5-131">したがって、ページ作成者にとって有用な値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-131">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="eb4a5-132">**OK** をクリックして新しいプリセット レイアウトを作成し、レイアウト エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-132">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="eb4a5-133">レイアウト エディターで、左側のアウトライン ツリーと右側のプロパティ ウィンドウを使用して、モジュールを追加およびコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-133">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="eb4a5-134">(このプロセスは、テンプレート エディターでテンプレートのモジュールを追加およびコンフィギュレーションするプロセスに似ています。) モジュールの配置とすべてのロックされた既定の設定は、このプリセット レイアウトを使用するすべてのページで、一元化されたモジュール コンフィギュレーションになります。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-134">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="eb4a5-135">プリセット レイアウトの変更</span><span class="sxs-lookup"><span data-stu-id="eb4a5-135">Modify a preset layout</span></span>

<span data-ttu-id="eb4a5-136">プリセット レイアウトを変更するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-136">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="eb4a5-137">左のナビゲーション ウィンドウで、**レイアウト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-137">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="eb4a5-138">レイアウト エディターの、左側にあるアウトライン ツリーで、変更するモジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-138">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="eb4a5-139">そして、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-139">Then follow any of these steps:</span></span>

    - <span data-ttu-id="eb4a5-140">親モジュール内でモジュールを上下に移動するには、モジュールの省略記号ボタン (**...**) をクリックし、**上へ移動**または**下へ移動**を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-140">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="eb4a5-141">モジュールの既定の設定を変更するには、プロパティ ウィンドウを使用して既定値を入力し、必要に応じてすべての下流ページでロックします。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-141">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="eb4a5-142">コンテナー モジュールに新しいモジュールまたはフラグメントを追加するには、省略記号ボタンを選択し、**モジュールの追加**または**フラグメントの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-142">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="eb4a5-143">レイアウトからモジュールを削除するには、省略記号ボタンを選択し、**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-143">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="eb4a5-144">プリセット レイアウトのテーマ変更</span><span class="sxs-lookup"><span data-stu-id="eb4a5-144">Change a preset layout theme</span></span>

<span data-ttu-id="eb4a5-145">プリセット レイアウトを使用するすべてのページに既定のテーマを設定するのが一般的な方法です。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-145">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="eb4a5-146">プリセット レイアウトを使用するすべての子ページのテーマを設定または変更するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-146">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="eb4a5-147">レイアウト エディターの、左側にあるアウトライン ツリーで、ページ コンテナー モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-147">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="eb4a5-148">(通常、このモジュールは 2 番目のノードであり、**既定のページ**として名づけられます。)</span><span class="sxs-lookup"><span data-stu-id="eb4a5-148">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="eb4a5-149">右側のプロパティ ウィンドウの**テーマ** フィールドで、テーマを選択します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-149">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="eb4a5-150">プリセット レイアウトの保存、チェック イン、プレビュー、および公開</span><span class="sxs-lookup"><span data-stu-id="eb4a5-150">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="eb4a5-151">プリセット レイアウトを保存してチェック インするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-151">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="eb4a5-152">レイアウト エディターの上部にある**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-152">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="eb4a5-153">保存された変更は、チェック インされるまで下流ページに影響しません。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-153">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="eb4a5-154">**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-154">Select **Finish editing**.</span></span> <span data-ttu-id="eb4a5-155">下流のワークフローで変更が検出可能になりました。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-155">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="eb4a5-156">変更をプレビューするには、プリセット レイアウトを使用している既存のページを開くか、レイアウトから新しいページを作成します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-156">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="eb4a5-157">プリセット レイアウトの変更をプレビューしたら、次のいずれかの手順に従って、実際のサイトにレイアウトを発行します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-157">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="eb4a5-158">**レイアウト**に移動し、レイアウトを選択して、**公開**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-158">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="eb4a5-159">レイアウト名を選択してレイアウト エディターを開き、**発行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-159">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="eb4a5-160">未公開のレイアウトを参照するページを公開します。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-160">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="eb4a5-161">レイアウトは自動的に公開されます。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-161">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="eb4a5-162">複数のページから、プリセット レイアウトを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-162">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="eb4a5-163">プリセット レイアウトを発行する場合は、複数のページのレイアウトに影響を与える可能性があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="eb4a5-163">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb4a5-164">追加リソース</span><span class="sxs-lookup"><span data-stu-id="eb4a5-164">Additional resources</span></span>

[<span data-ttu-id="eb4a5-165">テンプレートとレイアウトの概要</span><span class="sxs-lookup"><span data-stu-id="eb4a5-165">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="eb4a5-166">テンプレートの使用</span><span class="sxs-lookup"><span data-stu-id="eb4a5-166">Work with templates</span></span>](work-with-templates.md)
