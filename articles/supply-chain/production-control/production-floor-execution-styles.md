---
title: 生産現場の実行インターフェースのスタイル
description: このトピックでは、既定の生産フロア実行スタイルが適用されるように、フォーム コントロールを構成する方法について説明します。
author: johanhoffmann
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 3ff7187bdd035a639ed8bb1eb61d643136db76c4
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115037"
---
# <a name="style-the-production-floor-execution-interface"></a><span data-ttu-id="71fa7-103">生産現場の実行インターフェースのスタイル</span><span class="sxs-lookup"><span data-stu-id="71fa7-103">Style the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71fa7-104">このトピックでは、既定の生産フロア実行スタイルが適用されるように、フォーム コントロールを構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="71fa7-104">The topic explains how to configure form controls so that the default production floor execution styles are applied to them.</span></span>

## <a name="forms-and-dialogs"></a><span data-ttu-id="71fa7-105">フォームおよびダイアログ</span><span class="sxs-lookup"><span data-stu-id="71fa7-105">Forms and dialogs</span></span>

<span data-ttu-id="71fa7-106">スタイルは、次の要件が満たされている場合にのみ、フォームまたはダイアログに適用されます。</span><span class="sxs-lookup"><span data-stu-id="71fa7-106">Styles can be applied to a form or dialog only if the following requirements are met:</span></span>

- <span data-ttu-id="71fa7-107">フォームが既存のレポートの進行状況フォームと類似している場合は、フォームまたはダイアログの名前を **JmgProductionFloorExecutionCustomInputDialog** で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="71fa7-107">If the form should resemble the existing report progress form, then the name of your form or dialog must start with **JmgProductionFloorExecutionCustomInputDialog**.</span></span>
- <span data-ttu-id="71fa7-108">フォームまたはダイアログには、詳細フォームのパーツを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="71fa7-108">The form or dialog can contain a detail form part.</span></span> <span data-ttu-id="71fa7-109">スタイルを適用するには、詳細フォームのパーツの名前を **JmgProductionFloorExecutionCustomDetailsDialog** で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="71fa7-109">To apply styles to it, the name of the detail form part must start with **JmgProductionFloorExecutionCustomDetailsDialog**.</span></span>
- <span data-ttu-id="71fa7-110">フォームまたはダイアログに簡単なビューを表示する必要がある場合は、簡易ビューの名前を **JmgProductionFloorExecutionCustomDialog** で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="71fa7-110">If the form or dialog should have a simple view, then the name of the simple view must start with **JmgProductionFloorExecutionCustomDialog**.</span></span> <span data-ttu-id="71fa7-111">簡易ビューを持つフォームの例としては、開始フォームおよび間接活動フォームがあります。</span><span class="sxs-lookup"><span data-stu-id="71fa7-111">Examples of forms that have a simple view include the start form and the indirect activity form.</span></span>
- <span data-ttu-id="71fa7-112">ダイアログのすべてのコントロールをこのトピックで説明されているように構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71fa7-112">All the controls in the dialog  must be configured as described in this topic.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="71fa7-113">このリストの最初の 2 つのポイントで述べた機能には、Supply Chain Management バージョン 10.0.19 以降が必要です。</span><span class="sxs-lookup"><span data-stu-id="71fa7-113">The features mentioned in the first two bullet points of this list require Supply Chain Management version 10.0.19 or later.</span></span>

<span data-ttu-id="71fa7-114">スタイルは、次の要件が満たされている場合にのみ、ダイアログの **OK** ボタンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="71fa7-114">Styles can be applied to the **OK** button in a dialog only if the following requirements are met:</span></span>

- <span data-ttu-id="71fa7-115">ボタンはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-115">The button is contained in a form group.</span></span>
- <span data-ttu-id="71fa7-116">グループ名が **OkButtonGroup** で始まる。</span><span class="sxs-lookup"><span data-stu-id="71fa7-116">The group name starts with **OkButtonGroup**.</span></span>

<span data-ttu-id="71fa7-117">スタイルは、次の要件が満たされている場合にのみ、ダイアログ ボックスの **キャンセル** ボタンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="71fa7-117">Styles can be applied to the **Cancel** button in a dialog box only if the following requirements are met:</span></span>

- <span data-ttu-id="71fa7-118">ボタンはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-118">The button is contained in a form group.</span></span>
- <span data-ttu-id="71fa7-119">グループ名が **CancelButtonGroup** で始まる。</span><span class="sxs-lookup"><span data-stu-id="71fa7-119">The group name starts with **CancelButtonGroup**.</span></span>

## <a name="grid"></a><span data-ttu-id="71fa7-120">グリッド</span><span class="sxs-lookup"><span data-stu-id="71fa7-120">Grid</span></span>

<span data-ttu-id="71fa7-121">スタイルは自動的に適用されます。</span><span class="sxs-lookup"><span data-stu-id="71fa7-121">Styles are automatically applied.</span></span> <span data-ttu-id="71fa7-122">固有のコンフィギュレーションは必要はありません。</span><span class="sxs-lookup"><span data-stu-id="71fa7-122">No specific configuration is required.</span></span>

## <a name="card-view"></a><span data-ttu-id="71fa7-123">カード ビュー</span><span class="sxs-lookup"><span data-stu-id="71fa7-123">Card view</span></span>

<span data-ttu-id="71fa7-124">スタイルは、次の要件が満たされている場合にのみ、カード ビュー コントロールに適用されます。</span><span class="sxs-lookup"><span data-stu-id="71fa7-124">Styles can be applied to card view controls only if the following requirements are met:</span></span>

- <span data-ttu-id="71fa7-125">各カード ビューはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-125">Each card view is contained in a form group.</span></span>
- <span data-ttu-id="71fa7-126">グループ名が **CardGroup** で始まる (**CardGroupJobsView** など)。</span><span class="sxs-lookup"><span data-stu-id="71fa7-126">The group name starts with **CardGroup** (for example, **CardGroupJobsView**).</span></span>

<span data-ttu-id="71fa7-127">次の図は、その中にコントロールがないカード ビューを示しています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-127">The following illustration shows a card view that has no controls inside it.</span></span>

![要素のないカード ビュー](media/pfe-styles-empty-card.png)

<span data-ttu-id="71fa7-129">次の図は、その中にコントロールを含んでいるカード ビューを示しています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-129">The following illustrations show card views that have controls inside them.</span></span>

![Hz を示す要素を含むカード](media/pfe-styles-elements.png)

![メンテナンス要求の要素を含むカード](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a><span data-ttu-id="71fa7-132">ビジネス カード</span><span class="sxs-lookup"><span data-stu-id="71fa7-132">Business card</span></span>

<span data-ttu-id="71fa7-133">スタイルは、次の要件が満たされている場合にのみ、ビジネス カード コントロールに適用されます。</span><span class="sxs-lookup"><span data-stu-id="71fa7-133">Styles can be applied to business card controls only if the following requirements are met:</span></span>

- <span data-ttu-id="71fa7-134">各ビジネス カードはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-134">Each business card is contained in a form group.</span></span>
- <span data-ttu-id="71fa7-135">グループ名が **BusinessCardGroup** で始まる (**BusinessCardGroupJobsList** など)。</span><span class="sxs-lookup"><span data-stu-id="71fa7-135">The group name starts with **BusinessCardGroup** (for example, **BusinessCardGroupJobsList**).</span></span>

<span data-ttu-id="71fa7-136">ビジネス カードで以下のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="71fa7-136">Set the following properties on the business card:</span></span>

- <span data-ttu-id="71fa7-137">**スタイル**: **リスト**</span><span class="sxs-lookup"><span data-stu-id="71fa7-137">**Style**: **list**</span></span>
- <span data-ttu-id="71fa7-138">**拡張スタイル**: **cardList**</span><span class="sxs-lookup"><span data-stu-id="71fa7-138">**Extended style**: **cardList**</span></span>
- <span data-ttu-id="71fa7-139">**複数選択**: **いいえ**</span><span class="sxs-lookup"><span data-stu-id="71fa7-139">**Multi Select**: **No**</span></span>
- <span data-ttu-id="71fa7-140">**列ラベルの表示**: **いいえ**</span><span class="sxs-lookup"><span data-stu-id="71fa7-140">**Show Col Labels**: **No**</span></span>

![ビジネス カード](media/pfe-styles-business-card.png)

## <a name="radio-button"></a><span data-ttu-id="71fa7-142">オプション ボタン</span><span class="sxs-lookup"><span data-stu-id="71fa7-142">Radio button</span></span>

<span data-ttu-id="71fa7-143">スタイルは、次の要件が満たされている場合にのみ、ラジオ ボタンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="71fa7-143">Styles can be applied to radio buttons only if the following requirements are met:</span></span>

- <span data-ttu-id="71fa7-144">各ラジオ ボタンはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-144">Each radio button is contained in a form group.</span></span>
- <span data-ttu-id="71fa7-145">グループ名が、テキストを表示させる場所に応じて、**RadioTextBelow** または **RadioTextRight** で始まる。</span><span class="sxs-lookup"><span data-stu-id="71fa7-145">The group name starts with **RadioTextBelow** or **RadioTextRight**, depending on where you want the text to appear.</span></span>

<span data-ttu-id="71fa7-146">ラジオ ボタンに以下のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="71fa7-146">Set the following properties on the radio button:</span></span>

- <span data-ttu-id="71fa7-147">**トグル ボタン**: **チェック**</span><span class="sxs-lookup"><span data-stu-id="71fa7-147">**Toggle button**: **Check**</span></span>
- <span data-ttu-id="71fa7-148">**トグル値**: ラジオ ボタンを選択する必要がある場合は **オン**、それ以外の場合は **オフ**</span><span class="sxs-lookup"><span data-stu-id="71fa7-148">**Toggle value**: **On** if the radio button should be selected; otherwise, **Off**</span></span>

<span data-ttu-id="71fa7-149">次の図は、テキストがラジオ ボタンの下に表示される例を示しています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-149">The following illustration shows an example where the text appears below the radio buttons.</span></span>

![下にテキストが表示されているラジオ ボタン](media/pfe-styles-radio-text-below.png)

<span data-ttu-id="71fa7-151">次の図は、テキストがラジオ ボタンの右に表示される例を示しています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-151">The following illustration shows an example where the text appears to the right of the radio buttons.</span></span>

![右にテキストが表示されているラジオ ボタン](media/pfe-styles-radio-text-right.png)

### <a name="radio-buttons-in-internet-explorer"></a><span data-ttu-id="71fa7-153">Internet Explorer のラジオ ボタン</span><span class="sxs-lookup"><span data-stu-id="71fa7-153">Radio buttons in Internet Explorer</span></span>

<span data-ttu-id="71fa7-154">ラジオ ボタン スタイルは Internet Explorer ではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="71fa7-154">Radio button styles aren't supported in Internet Explorer.</span></span> <span data-ttu-id="71fa7-155">次の図は、ラジオ ボタンが Internet Explorer でどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-155">The following illustration shows what radio buttons look like in Internet Explorer.</span></span>

![Internet Explorer のラジオ ボタン](media/pfe-styles-browser.png)

## <a name="buttons"></a><span data-ttu-id="71fa7-157">ボタン</span><span class="sxs-lookup"><span data-stu-id="71fa7-157">Buttons</span></span>

<span data-ttu-id="71fa7-158">スタイルは、次の要件が満たされている場合にのみ、ボタンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="71fa7-158">Styles can be applied to buttons only if the following requirements are met:</span></span>

- <span data-ttu-id="71fa7-159">各ボタン グループはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-159">Each group of buttons is contained in a form group.</span></span> <span data-ttu-id="71fa7-160">グループ内のすべてのボタンは同じスタイルになります。</span><span class="sxs-lookup"><span data-stu-id="71fa7-160">All the buttons in the group will have the same style.</span></span>
- <span data-ttu-id="71fa7-161">グループ名に関する要件はありません。</span><span class="sxs-lookup"><span data-stu-id="71fa7-161">There are no requirements about the name of the group.</span></span>

<span data-ttu-id="71fa7-162">ボタンに以下のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="71fa7-162">Set the following properties on the buttons:</span></span>

- <span data-ttu-id="71fa7-163">**ボタン表示**: **TextWithImageLeft**。</span><span class="sxs-lookup"><span data-stu-id="71fa7-163">**Button Display**: **TextWithImageLeft**.</span></span>
- <span data-ttu-id="71fa7-164">**通常のイメージ**: このプロパティを空白にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="71fa7-164">**Normal Image**: This property can't be blank.</span></span> <span data-ttu-id="71fa7-165">たとえば、**CoffeeScript** を使用します。</span><span class="sxs-lookup"><span data-stu-id="71fa7-165">For example, use **CoffeeScript**.</span></span>
- <span data-ttu-id="71fa7-166">**テキスト**: このプロパティを空白にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="71fa7-166">**Text**: This property can't be blank.</span></span> <span data-ttu-id="71fa7-167">たとえば、**分割の開始** を使用します。</span><span class="sxs-lookup"><span data-stu-id="71fa7-167">For example, use **Start Break**.</span></span>
- <span data-ttu-id="71fa7-168">**幅**: **自動**。</span><span class="sxs-lookup"><span data-stu-id="71fa7-168">**Width**: **Auto**.</span></span>
- <span data-ttu-id="71fa7-169">**高さ**: **自動**。</span><span class="sxs-lookup"><span data-stu-id="71fa7-169">**Height**: **Auto**.</span></span>

### <a name="primary-button"></a><span data-ttu-id="71fa7-170">プライマリ ボタン</span><span class="sxs-lookup"><span data-stu-id="71fa7-170">Primary button</span></span>

<span data-ttu-id="71fa7-171">スタイルは、次の要件が満たされている場合にのみ、基本ボタンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="71fa7-171">Styles can be applied to a primary button only if the following requirements are met:</span></span>

- <span data-ttu-id="71fa7-172">ボタンはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-172">The button is contained in a form group.</span></span>
- <span data-ttu-id="71fa7-173">グループ名が **DefaultButtonGroup** または **PrimaryButtonGroup** で始まる (**DefaultButtonGroup10** など)。</span><span class="sxs-lookup"><span data-stu-id="71fa7-173">The group name starts with **DefaultButtonGroup** or **PrimaryButtonGroup** (for example, **DefaultButtonGroup10**).</span></span>

![プライマリ ボタン](media/pfe-styles-first.png)

### <a name="secondary-button"></a><span data-ttu-id="71fa7-175">セカンダリ ボタン</span><span class="sxs-lookup"><span data-stu-id="71fa7-175">Secondary button</span></span>

<span data-ttu-id="71fa7-176">スタイルは、次の要件が満たされている場合にのみ、二次ボタンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="71fa7-176">Styles can be applied to a secondary button only if the following requirements are met:</span></span>

- <span data-ttu-id="71fa7-177">ボタンはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-177">The button is contained in a form group.</span></span>
- <span data-ttu-id="71fa7-178">グループが **右側のパネル** と名前が付けられている、またはグループ名が **SecondaryButtonGroup** で始まる。</span><span class="sxs-lookup"><span data-stu-id="71fa7-178">The group is named **Right panel**, or the group name starts with **SecondaryButtonGroup**.</span></span>

![セカンダリ ボタン](media/pfe-styles-second.png)

### <a name="third-group-button"></a><span data-ttu-id="71fa7-180">3 番目のグループ ボタン</span><span class="sxs-lookup"><span data-stu-id="71fa7-180">Third-group button</span></span>

<span data-ttu-id="71fa7-181">スタイルは、次の要件が満たされている場合にのみ、3 番目のグループのボタンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="71fa7-181">Styles can be applied to a third-group button only if the following requirements are met:</span></span>

- <span data-ttu-id="71fa7-182">ボタンはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-182">The button is contained in a form group.</span></span>
- <span data-ttu-id="71fa7-183">グループが **左側のパネル** と名前が付けられている、またはグループ名が **ThirdButtonGroup** で始まる。</span><span class="sxs-lookup"><span data-stu-id="71fa7-183">The group is named **Left panel**, or the group name starts with **ThirdButtonGroup**.</span></span>

![3 番目のグループのボタン](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a><span data-ttu-id="71fa7-185">4 番目のグループのボタン</span><span class="sxs-lookup"><span data-stu-id="71fa7-185">Fourth-group button</span></span>

<span data-ttu-id="71fa7-186">スタイルは、次の要件が満たされている場合にのみ、4 番目のグループのボタンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="71fa7-186">Styles can be applied to a fourth-group button only if the following requirements are met:</span></span>

- <span data-ttu-id="71fa7-187">ボタンはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-187">The button is contained in a form group.</span></span>
- <span data-ttu-id="71fa7-188">グループ名が **FourthButtonGroup** で始まる。</span><span class="sxs-lookup"><span data-stu-id="71fa7-188">The group name starts with **FourthButtonGroup**.</span></span>

<span data-ttu-id="71fa7-189">ボタンに以下のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="71fa7-189">Set the following properties on the button:</span></span>

- <span data-ttu-id="71fa7-190">**ボタン表示**: **TextOnly**。</span><span class="sxs-lookup"><span data-stu-id="71fa7-190">**Button Display**: **TextOnly**.</span></span>
- <span data-ttu-id="71fa7-191">**通常のイメージ**: このプロパティは空白にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="71fa7-191">**Normal Image**: This property must be blank.</span></span>
- <span data-ttu-id="71fa7-192">**テキスト**: このプロパティを空白にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="71fa7-192">**Text**: This property can't be blank.</span></span> <span data-ttu-id="71fa7-193">たとえば、**表示** または **編集** を使用します。</span><span class="sxs-lookup"><span data-stu-id="71fa7-193">For example, use **View** or **Edit**.</span></span>
- <span data-ttu-id="71fa7-194">**幅**: **自動**。</span><span class="sxs-lookup"><span data-stu-id="71fa7-194">**Width**: **Auto**.</span></span>
- <span data-ttu-id="71fa7-195">**高さ**: **自動**。</span><span class="sxs-lookup"><span data-stu-id="71fa7-195">**Height**: **Auto**.</span></span>

![4 番目のグループ ボタン](media/pfe-styles-fourth.png)

### <a name="flat-button"></a><span data-ttu-id="71fa7-197">フラット ボタン</span><span class="sxs-lookup"><span data-stu-id="71fa7-197">Flat button</span></span>

<span data-ttu-id="71fa7-198">スタイルは、次の要件が満たされている場合にのみ、フラット ボタンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="71fa7-198">Styles can be applied to a flat button only if the following requirements are met:</span></span>

- <span data-ttu-id="71fa7-199">ボタンはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-199">The button is contained in a form group.</span></span>
- <span data-ttu-id="71fa7-200">グループ名が **FlatButtonGroup** で始まる。</span><span class="sxs-lookup"><span data-stu-id="71fa7-200">The group name starts with **FlatButtonGroup**.</span></span>

<span data-ttu-id="71fa7-201">ボタンに以下のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="71fa7-201">Set the following properties on the button:</span></span>

- <span data-ttu-id="71fa7-202">**ボタン表示**: **ImageOnly**。</span><span class="sxs-lookup"><span data-stu-id="71fa7-202">**Button Display**: **ImageOnly**.</span></span>
- <span data-ttu-id="71fa7-203">**通常のイメージ**: このプロパティを空白にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="71fa7-203">**Normal Image**: This property can't be blank.</span></span> <span data-ttu-id="71fa7-204">たとえば、**CoffeeScript** を使用します。</span><span class="sxs-lookup"><span data-stu-id="71fa7-204">For example, use **CoffeeScript**.</span></span>
- <span data-ttu-id="71fa7-205">**テキスト**: このプロパティは空白にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="71fa7-205">**Text**: This property must be blank.</span></span>
- <span data-ttu-id="71fa7-206">**幅**: **自動**。</span><span class="sxs-lookup"><span data-stu-id="71fa7-206">**Width**: **Auto**.</span></span>
- <span data-ttu-id="71fa7-207">**高さ**: **自動**。</span><span class="sxs-lookup"><span data-stu-id="71fa7-207">**Height**: **Auto**.</span></span>

![フラット ボタン](media/pfe-styles-flat-button.png)

## <a name="combo-box"></a><span data-ttu-id="71fa7-209">コンボ ボックス</span><span class="sxs-lookup"><span data-stu-id="71fa7-209">Combo box</span></span>

<span data-ttu-id="71fa7-210">コンボ ボックスは、入力コントロール、入力コントロールをクリアするボタン、および検索を実行するボタンの 3 つのコントロールの組み合わせです。</span><span class="sxs-lookup"><span data-stu-id="71fa7-210">A combo box is a combination of three controls: an input control, a button that clears the input control, and a button that runs a search.</span></span>

<span data-ttu-id="71fa7-211">スタイルは、次の要件が満たされている場合にのみ、コンボ ボックスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="71fa7-211">Styles can be applied to a combo box only if the following requirements are met:</span></span>

- <span data-ttu-id="71fa7-212">コンボ ボックスはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-212">The combo box is contained in a form group.</span></span>
- <span data-ttu-id="71fa7-213">グループ名は **Combobox** で始まります。</span><span class="sxs-lookup"><span data-stu-id="71fa7-213">The group name starts with **Combobox**.</span></span>
- <span data-ttu-id="71fa7-214">グループ内で、最初のコントロールは **AxFormStringControl** です。</span><span class="sxs-lookup"><span data-stu-id="71fa7-214">Inside the group, the first control is an **AxFormStringControl** control.</span></span> <span data-ttu-id="71fa7-215">このコントロールは現在の値を表示し、ユーザーは必要な値を入力します。</span><span class="sxs-lookup"><span data-stu-id="71fa7-215">This control shows the current value, and it's where the user enters the required value.</span></span>
- <span data-ttu-id="71fa7-216">2 つ目のコントロールは **CommonButton** コントロールで、名前は **ClearButton** で始まります。</span><span class="sxs-lookup"><span data-stu-id="71fa7-216">The second control is a **CommonButton** control, and its name starts with **ClearButton**.</span></span> <span data-ttu-id="71fa7-217">このボタンには、ボタンを表示または非表示にする **enable** プロパティを使用するコードが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="71fa7-217">This button must contain code that uses the **enable** property to show or hide the button.</span></span> <span data-ttu-id="71fa7-218">たとえば、ユーザーが入力コントロールに情報を入力している間に **クリア** ボタンを表示または非表示にするには、次のコードを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="71fa7-218">For example, to show or hide the **Clear** button while the user is typing information in the input control, you can use the following code.</span></span>

    ```xpp
    public void textChange()
    {
        super();
        ClearButtonSerial.enabled(this.text()? true : false);
    }
    ```

    <span data-ttu-id="71fa7-219">入力コントロールでデータを設定する方法が 1 つ必要です。</span><span class="sxs-lookup"><span data-stu-id="71fa7-219">You should have one method where the data is set in the input control.</span></span> <span data-ttu-id="71fa7-220">そのメソッドの **クリア** ボタンを有効にします。</span><span class="sxs-lookup"><span data-stu-id="71fa7-220">Enable the **Clear** button in that method.</span></span> <span data-ttu-id="71fa7-221">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="71fa7-221">Here is an example.</span></span>

    ```xpp
    public void setSerialId(str _serialId)
    {
        JmgTmpJobBundleProdFeedback.InventSerial = _serialId;
        ClearButtonSerial.enabled(_serialId? true : false);

        if (_serialId)
        {
            this.addSerialNumber();
        }
    }
    ```

    <span data-ttu-id="71fa7-222">**クリア** ボタンの **clicked** メソッドには次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="71fa7-222">Use the following code for the **clicked** method of the **Clear** button.</span></span>

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    <span data-ttu-id="71fa7-223">フォームを **init** メソッドを使用して初期化するときに、入力コントロール **AxFormStringControl** の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="71fa7-223">Set the value of the input control, **AxFormStringControl**, when the form is initialized by using the **init** method.</span></span> <span data-ttu-id="71fa7-224">値が空白でない場合は、**クリア** ボタンを有効にします。</span><span class="sxs-lookup"><span data-stu-id="71fa7-224">If the value isn't blank, enable the **Clear** button.</span></span> <span data-ttu-id="71fa7-225">値が空白の場合は、**クリア** ボタンを無効にします。</span><span class="sxs-lookup"><span data-stu-id="71fa7-225">If the value is blank, disable the **Clear** button.</span></span>

- <span data-ttu-id="71fa7-226">3 つ目のコントロールは **CommonButton** コントロールで、名前は **SearchButton** で始まります。</span><span class="sxs-lookup"><span data-stu-id="71fa7-226">The third control is a **CommonButton** control, and its name starts with **SearchButton**.</span></span>

<span data-ttu-id="71fa7-227">次の図は、2 つのコンボ ボックス コントロールを示します。</span><span class="sxs-lookup"><span data-stu-id="71fa7-227">The following illustration shows two combo box controls.</span></span> <span data-ttu-id="71fa7-228">左側のコンボ ボックスには空のテキスト ボックスがあり、**クリア** ボタンは無効になっています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-228">The combo box on the left has an empty text box, and the **Clear** button is disabled.</span></span> <span data-ttu-id="71fa7-229">右側のコンボ ボックスにはテキスト ボックスにテキストがあり、**クリア** ボタンが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-229">The combo box on the right has text in the text box, and the **Clear** button is enabled.</span></span>

![クリア ボタン付き、またはなしのコンボ ボックス](media/pfe-styles-combo.png)

## <a name="quick-filter"></a><span data-ttu-id="71fa7-231">クイック フィルター</span><span class="sxs-lookup"><span data-stu-id="71fa7-231">Quick filter</span></span>

<span data-ttu-id="71fa7-232">クイック フィルター コントロールによって、ページに検索フィールドが追加されます。</span><span class="sxs-lookup"><span data-stu-id="71fa7-232">The quick filter control adds a search field to the page.</span></span> <span data-ttu-id="71fa7-233">次の要件が満たされている場合、クイック フィルターにスタイルを適用できます。</span><span class="sxs-lookup"><span data-stu-id="71fa7-233">You can apply styles to a quick filter provided the following requirements are met:</span></span>

- <span data-ttu-id="71fa7-234">クイック フィルターはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="71fa7-234">The quick filter is contained in a form group.</span></span>
- <span data-ttu-id="71fa7-235">グループ名は **SearchInput** で始まります。</span><span class="sxs-lookup"><span data-stu-id="71fa7-235">The group name starts with **SearchInput**.</span></span>
- <span data-ttu-id="71fa7-236">グループ内で、最初のコントロールは **QuickFilter** コントロールです。</span><span class="sxs-lookup"><span data-stu-id="71fa7-236">Inside the group, the first control is a **QuickFilter** control.</span></span> <span data-ttu-id="71fa7-237">(これはユーザーが検索文字列を入力する場所です。)</span><span class="sxs-lookup"><span data-stu-id="71fa7-237">(This is where the user enters the search string.)</span></span>
- <span data-ttu-id="71fa7-238">2 つ目のコントロールは **FormStaticTextControl** で、名前は **NumberOfResults** で始まります。</span><span class="sxs-lookup"><span data-stu-id="71fa7-238">The second control is a **FormStaticTextControl** with the name **NumberOfResults**.</span></span> <span data-ttu-id="71fa7-239">(これはオプションで、検出された品目の数が含まれている場合は表示されます。)</span><span class="sxs-lookup"><span data-stu-id="71fa7-239">(This is optional and shows the number of found items if included.)</span></span>
- <span data-ttu-id="71fa7-240">3 つ目のコントロールは **CommonButton** コントロールで、名前は **ClearButton** で始まります。</span><span class="sxs-lookup"><span data-stu-id="71fa7-240">The third control is a **CommonButton** control with a name that starts with **ClearButton**.</span></span>

<span data-ttu-id="71fa7-241">次の図は、2 つのクイック フィルター コントロールを示します。</span><span class="sxs-lookup"><span data-stu-id="71fa7-241">The following illustration shows two quick filter controls.</span></span> <span data-ttu-id="71fa7-242">左側のクイック フィルターは空になっており、結果の数は表示されません。</span><span class="sxs-lookup"><span data-stu-id="71fa7-242">The quick filter on the left has an empty quick filter, and the number of results isn't visible.</span></span> <span data-ttu-id="71fa7-243">右側のクイック フィルターには検索文字列が含まれるので、結果の数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="71fa7-243">The quick filter on the right contains a search string and shows the number of results.</span></span>

<span data-ttu-id="71fa7-244">![検索文字列を使用した場合および使用しない場合のクイック フィルター コントロールの例](media/pfe-styles-quick-filter.png "検索文字列を使用した場合および使用しない場合のクイック フィルター コントロールの例")</span><span class="sxs-lookup"><span data-stu-id="71fa7-244">![Examples of a quick filter control with and without a search string](media/pfe-styles-quick-filter.png "Examples of a quick filter control with and without a search string")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
