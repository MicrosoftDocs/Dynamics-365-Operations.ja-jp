---
title: プリセット レイアウトの使用
description: このトピックでは、Microsoft Dynamics 365 Commerce でのプリセット レイアウトの使用方法について説明します。
author: phinneyridge
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ce54be1032777ffcaac474773cdeeef3b9028110
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793924"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="32d7f-103">プリセット レイアウトの使用</span><span class="sxs-lookup"><span data-stu-id="32d7f-103">Work with preset layouts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="32d7f-104">このトピックでは、Microsoft Dynamics 365 Commerce でのプリセット レイアウトの使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="32d7f-105">このトピックの手順を実行する前に、[プリセットおよびカスタム レイアウト](templates-layouts-overview.md#preset-and-custom-layouts) を必ずお読みください。</span><span class="sxs-lookup"><span data-stu-id="32d7f-105">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="32d7f-106">一般的な概要については、[テンプレートとレイアウトの概要](templates-layouts-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="32d7f-106">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="32d7f-107">新しいプリセット レイアウトの作成</span><span class="sxs-lookup"><span data-stu-id="32d7f-107">Create a new preset layout</span></span>

<span data-ttu-id="32d7f-108">プリセット レイアウトを作成するには 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="32d7f-108">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="32d7f-109">既存のカスタム レイアウトを新しいプリセット レイアウトとして保存するか、またはプリセット レイアウトを最初から作成するかです。</span><span class="sxs-lookup"><span data-stu-id="32d7f-109">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="32d7f-110">既存のカスタム レイアウトからプリセット レイアウトを作成</span><span class="sxs-lookup"><span data-stu-id="32d7f-110">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="32d7f-111">既存のカスタム レイアウトからプリセット レイアウトを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="32d7f-111">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="32d7f-112">現在プリセット レイアウトを使用していないが、サイトの他のページで再利用するモジュール構造を使用している、既存のページを開きます。</span><span class="sxs-lookup"><span data-stu-id="32d7f-112">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="32d7f-113">**編集** を選択してページをチェックアウトします。</span><span class="sxs-lookup"><span data-stu-id="32d7f-113">Select **Edit** to check out the page.</span></span>
1. <span data-ttu-id="32d7f-114">**新しいレイアウトとして保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-114">Select **Save as new layout**.</span></span> <span data-ttu-id="32d7f-115">**新しいレイアウトとして保存** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="32d7f-115">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="32d7f-116">プリセット レイアウトに名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-116">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="32d7f-117">レイアウトから新しいページを作成したり、そのページに切り替えると、入力した値が他の作成者に対して表示されます。</span><span class="sxs-lookup"><span data-stu-id="32d7f-117">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="32d7f-118">したがって、ページ作成者にとって有用な値を入力します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-118">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="32d7f-119">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-119">Select **OK**.</span></span>

<span data-ttu-id="32d7f-120">プリセット レイアウトは、新しいページを作成するとき、または同じテンプレート階層内のページに別のレイアウトを選択するときに、使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="32d7f-120">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="32d7f-121">特定のページが現在プリセット レイアウトにバインドされているかどうかをすばやく確認するには、ページ リスト ビューでページを選択し、右側のプロパティ ウィンドウでレイアウト メタデータを検査します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-121">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="32d7f-122">新しいプリセット レイアウトの作成</span><span class="sxs-lookup"><span data-stu-id="32d7f-122">Create a new preset layout</span></span>

<span data-ttu-id="32d7f-123">プリセット レイアウトを最初から作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="32d7f-123">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="32d7f-124">左のナビゲーション ウィンドウで、**レイアウト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-124">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="32d7f-125">**新しいレイアウト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-125">Select **New Layout**.</span></span> <span data-ttu-id="32d7f-126">**新しいレイアウト** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="32d7f-126">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="32d7f-127">プリセット レイアウトに使用するテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-127">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="32d7f-128">プリセット レイアウトに名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-128">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="32d7f-129">レイアウトから新しいページを作成したり、そのページに切り替えると、入力した値が他の作成者に対して表示されます。</span><span class="sxs-lookup"><span data-stu-id="32d7f-129">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="32d7f-130">したがって、ページ作成者にとって有用な値を入力します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-130">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="32d7f-131">**OK** をクリックして新しいプリセット レイアウトを作成し、レイアウト エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="32d7f-131">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="32d7f-132">レイアウト エディターで、左側のアウトライン ツリーと右側のプロパティ ウィンドウを使用して、モジュールを追加およびコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="32d7f-132">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="32d7f-133">(このプロセスは、テンプレート エディターでテンプレートのモジュールを追加およびコンフィギュレーションするプロセスに似ています。) モジュールの配置とすべてのロックされた既定の設定は、このプリセット レイアウトを使用するすべてのページで、一元化されたモジュール コンフィギュレーションになります。</span><span class="sxs-lookup"><span data-stu-id="32d7f-133">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="32d7f-134">プリセット レイアウトの変更</span><span class="sxs-lookup"><span data-stu-id="32d7f-134">Modify a preset layout</span></span>

<span data-ttu-id="32d7f-135">プリセット レイアウトを変更するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="32d7f-135">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="32d7f-136">左のナビゲーション ウィンドウで、**レイアウト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-136">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="32d7f-137">レイアウト エディターの、左側にあるアウトライン ツリーで、変更するモジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-137">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="32d7f-138">そして、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-138">Then follow any of these steps:</span></span>

    - <span data-ttu-id="32d7f-139">親モジュール内でモジュールを上下に移動するには、モジュールの省略記号ボタン (**...**) をクリックし、**上へ移動** または **下へ移動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-139">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="32d7f-140">モジュールの既定の設定を変更するには、プロパティ ウィンドウを使用して既定値を入力し、必要に応じてすべての下流ページでロックします。</span><span class="sxs-lookup"><span data-stu-id="32d7f-140">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="32d7f-141">コンテナー モジュールに新しいモジュールまたはフラグメントを追加するには、省略記号ボタンを選択し、**モジュールの追加** または **フラグメントの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-141">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="32d7f-142">レイアウトからモジュールを削除するには、省略記号ボタンを選択し、**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-142">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="32d7f-143">プリセット レイアウトのテーマ変更</span><span class="sxs-lookup"><span data-stu-id="32d7f-143">Change a preset layout theme</span></span>

<span data-ttu-id="32d7f-144">プリセット レイアウトを使用するすべてのページに既定のテーマを設定するのが一般的な方法です。</span><span class="sxs-lookup"><span data-stu-id="32d7f-144">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="32d7f-145">プリセット レイアウトを使用するすべての子ページのテーマを設定または変更するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="32d7f-145">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="32d7f-146">レイアウト エディターの、左側にあるアウトライン ツリーで、ページ コンテナー モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-146">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="32d7f-147">(通常、このモジュールは 2 番目のノードであり、**既定のページ** として名づけられます。)</span><span class="sxs-lookup"><span data-stu-id="32d7f-147">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="32d7f-148">右側のプロパティ ウィンドウの **テーマ** フィールドで、テーマを選択します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-148">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="32d7f-149">プリセット レイアウトの保存、チェック イン、プレビュー、および公開</span><span class="sxs-lookup"><span data-stu-id="32d7f-149">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="32d7f-150">プリセット レイアウトを保存してチェック インするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="32d7f-150">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="32d7f-151">レイアウト エディターの上部にある **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-151">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="32d7f-152">保存された変更は、チェック インされるまで下流ページに影響しません。</span><span class="sxs-lookup"><span data-stu-id="32d7f-152">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="32d7f-153">**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-153">Select **Finish editing**.</span></span> <span data-ttu-id="32d7f-154">下流のワークフローで変更が検出可能になりました。</span><span class="sxs-lookup"><span data-stu-id="32d7f-154">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="32d7f-155">変更をプレビューするには、プリセット レイアウトを使用している既存のページを開くか、レイアウトから新しいページを作成します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-155">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="32d7f-156">プリセット レイアウトの変更をプレビューしたら、次のいずれかの手順に従って、実際のサイトにレイアウトを発行します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-156">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="32d7f-157">**レイアウト** に移動し、レイアウトを選択して、**公開** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32d7f-157">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="32d7f-158">レイアウト名を選択してレイアウト エディターを開き、**発行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-158">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="32d7f-159">未公開のレイアウトを参照するページを公開します。</span><span class="sxs-lookup"><span data-stu-id="32d7f-159">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="32d7f-160">レイアウトは自動的に公開されます。</span><span class="sxs-lookup"><span data-stu-id="32d7f-160">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="32d7f-161">複数のページから、プリセット レイアウトを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="32d7f-161">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="32d7f-162">プリセット レイアウトを発行する場合は、複数のページのレイアウトに影響を与える可能性があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="32d7f-162">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="32d7f-163">追加リソース</span><span class="sxs-lookup"><span data-stu-id="32d7f-163">Additional resources</span></span>

[<span data-ttu-id="32d7f-164">テンプレートとレイアウトの概要</span><span class="sxs-lookup"><span data-stu-id="32d7f-164">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="32d7f-165">テンプレートの使用</span><span class="sxs-lookup"><span data-stu-id="32d7f-165">Work with templates</span></span>](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
