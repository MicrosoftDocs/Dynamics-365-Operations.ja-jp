---
title: 生産現場の実行ユーザー インターフェイス コントロールのスタイル
description: このトピックでは、既定の生産フロア実行スタイルが適用されるように、フォーム コントロールを構成する方法について説明します。
author: inkharki
ms.date: 02/22/2021
ms.topic: article
ms.service: dynamics-365-supply-chain
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: inkharki
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 9124f6d20c851f54fd54c6b2487f41f321af931c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814694"
---
# <a name="user-interface-control-styles-for-production-floor-execution"></a><span data-ttu-id="70feb-103">生産現場の実行ユーザー インターフェイス コントロールのスタイル</span><span class="sxs-lookup"><span data-stu-id="70feb-103">User interface control styles for production floor execution</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70feb-104">このトピックでは、既定の生産フロア実行スタイルが適用されるように、フォーム コントロールを構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="70feb-104">The topic explains how to configure form controls so that the default production floor execution styles are applied to them.</span></span>

## <a name="grid"></a><span data-ttu-id="70feb-105">グリッド</span><span class="sxs-lookup"><span data-stu-id="70feb-105">Grid</span></span>

<span data-ttu-id="70feb-106">スタイルは自動的に適用されます。</span><span class="sxs-lookup"><span data-stu-id="70feb-106">Styles are automatically applied.</span></span> <span data-ttu-id="70feb-107">固有のコンフィギュレーションは必要はありません。</span><span class="sxs-lookup"><span data-stu-id="70feb-107">No specific configuration is required.</span></span>

## <a name="card-view"></a><span data-ttu-id="70feb-108">カード ビュー</span><span class="sxs-lookup"><span data-stu-id="70feb-108">Card view</span></span>

<span data-ttu-id="70feb-109">スタイルは、次の要件が満たされている場合にのみ、カード ビュー コントロールに適用されます。</span><span class="sxs-lookup"><span data-stu-id="70feb-109">Styles can be applied to card view controls only if the following requirements are met:</span></span>

+ <span data-ttu-id="70feb-110">各カード ビューはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="70feb-110">Each card view is contained in a form group.</span></span>
+ <span data-ttu-id="70feb-111">グループ名が **CardGroup** で始まる (**CardGroupJobsView** など)。</span><span class="sxs-lookup"><span data-stu-id="70feb-111">The group name starts with **CardGroup** (for example, **CardGroupJobsView**).</span></span>

<span data-ttu-id="70feb-112">次の図は、その中にコントロールがないカード ビューを示しています。</span><span class="sxs-lookup"><span data-stu-id="70feb-112">The following illustration shows a card view that has no controls inside it.</span></span>

![要素のないカード ビュー](media/pfe-styles-empty-card.png)

<span data-ttu-id="70feb-114">次の図は、その中にコントロールを含んでいるカード ビューを示しています。</span><span class="sxs-lookup"><span data-stu-id="70feb-114">The following illustrations show card views that have controls inside them.</span></span>

![Hz を示す要素を含むカード](media/pfe-styles-elements.png)

![メンテナンス要求の要素を含むカード](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a><span data-ttu-id="70feb-117">ビジネス カード</span><span class="sxs-lookup"><span data-stu-id="70feb-117">Business card</span></span>

<span data-ttu-id="70feb-118">スタイルは、次の要件が満たされている場合にのみ、ビジネス カード コントロールに適用されます。</span><span class="sxs-lookup"><span data-stu-id="70feb-118">Styles can be applied to business card controls only if the following requirements are met:</span></span>

+ <span data-ttu-id="70feb-119">各ビジネス カードはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="70feb-119">Each business card is contained in a form group.</span></span>
+ <span data-ttu-id="70feb-120">グループ名が **BusinessCardGroup** で始まる (**BusinessCardGroupJobsList** など)。</span><span class="sxs-lookup"><span data-stu-id="70feb-120">The group name starts with **BusinessCardGroup** (for example, **BusinessCardGroupJobsList**).</span></span>

<span data-ttu-id="70feb-121">ビジネス カードで以下のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="70feb-121">Set the following properties on the business card:</span></span>

- <span data-ttu-id="70feb-122">**スタイル**: **リスト**</span><span class="sxs-lookup"><span data-stu-id="70feb-122">**Style**: **list**</span></span>
- <span data-ttu-id="70feb-123">**拡張スタイル**: **cardList**</span><span class="sxs-lookup"><span data-stu-id="70feb-123">**Extended style**: **cardList**</span></span>
- <span data-ttu-id="70feb-124">**複数選択**: **いいえ**</span><span class="sxs-lookup"><span data-stu-id="70feb-124">**Multi Select**: **No**</span></span>
- <span data-ttu-id="70feb-125">**列ラベルの表示**: **いいえ**</span><span class="sxs-lookup"><span data-stu-id="70feb-125">**Show Col Labels**: **No**</span></span>

![ビジネス カード](media/pfe-styles-business-card.png)

## <a name="radio-button"></a><span data-ttu-id="70feb-127">オプション ボタン</span><span class="sxs-lookup"><span data-stu-id="70feb-127">Radio button</span></span>

<span data-ttu-id="70feb-128">スタイルは、次の要件が満たされている場合にのみ、ラジオ ボタンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="70feb-128">Styles can be applied to radio buttons only if the following requirements are met:</span></span>

+ <span data-ttu-id="70feb-129">各ラジオ ボタンはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="70feb-129">Each radio button is contained in a form group.</span></span>
+ <span data-ttu-id="70feb-130">グループ名が、テキストを表示させる場所に応じて、**RadioTextBelow** または **RadioTextRight** で始まる。</span><span class="sxs-lookup"><span data-stu-id="70feb-130">The group name starts with **RadioTextBelow** or **RadioTextRight**, depending on where you want the text to appear.</span></span>

<span data-ttu-id="70feb-131">ラジオ ボタンに以下のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="70feb-131">Set the following properties on the radio button:</span></span>

- <span data-ttu-id="70feb-132">**トグル ボタン**: **チェック**</span><span class="sxs-lookup"><span data-stu-id="70feb-132">**Toggle button**: **Check**</span></span>
- <span data-ttu-id="70feb-133">**トグル値**: ラジオ ボタンを選択する必要がある場合は **オン**、それ以外の場合は **オフ**</span><span class="sxs-lookup"><span data-stu-id="70feb-133">**Toggle value**: **On** if the radio button should be selected; otherwise, **Off**</span></span>

<span data-ttu-id="70feb-134">次の図は、テキストがラジオ ボタンの下に表示される例を示しています。</span><span class="sxs-lookup"><span data-stu-id="70feb-134">The following illustration shows an example where the text appears below the radio buttons.</span></span>

![下にテキストが表示されているラジオ ボタン](media/pfe-styles-radio-text-below.png)

<span data-ttu-id="70feb-136">次の図は、テキストがラジオ ボタンの右に表示される例を示しています。</span><span class="sxs-lookup"><span data-stu-id="70feb-136">The following illustration shows an example where the text appears to the right of the radio buttons.</span></span>

![右にテキストが表示されているラジオ ボタン](media/pfe-styles-radio-text-right.png)

### <a name="radio-buttons-in-internet-explorer"></a><span data-ttu-id="70feb-138">Internet Explorer のラジオ ボタン</span><span class="sxs-lookup"><span data-stu-id="70feb-138">Radio buttons in Internet Explorer</span></span>

<span data-ttu-id="70feb-139">ラジオ ボタン スタイルは Internet Explorer ではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="70feb-139">Radio button styles aren't supported in Internet Explorer.</span></span> <span data-ttu-id="70feb-140">次の図は、ラジオ ボタンが Internet Explorer でどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="70feb-140">The following illustration shows what radio buttons look like in Internet Explorer.</span></span>

![Internet Explorer のラジオ ボタン](media/pfe-styles-browser.png)

## <a name="buttons"></a><span data-ttu-id="70feb-142">ボタン</span><span class="sxs-lookup"><span data-stu-id="70feb-142">Buttons</span></span>

<span data-ttu-id="70feb-143">スタイルは、次の要件が満たされている場合にのみ、ボタンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="70feb-143">Styles can be applied to buttons only if the following requirements are met:</span></span>

+ <span data-ttu-id="70feb-144">各ボタン グループはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="70feb-144">Each group of buttons is contained in a form group.</span></span> <span data-ttu-id="70feb-145">グループ内のすべてのボタンは同じスタイルになります。</span><span class="sxs-lookup"><span data-stu-id="70feb-145">All the buttons in the group will have the same style.</span></span>
+ <span data-ttu-id="70feb-146">グループ名に関する要件はありません。</span><span class="sxs-lookup"><span data-stu-id="70feb-146">There are no requirements about the name of the group.</span></span>

<span data-ttu-id="70feb-147">ボタンに以下のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="70feb-147">Set the following properties on the buttons:</span></span>

- <span data-ttu-id="70feb-148">**ボタン表示**: **TextWithImageLeft**。</span><span class="sxs-lookup"><span data-stu-id="70feb-148">**Button Display**: **TextWithImageLeft**.</span></span>
- <span data-ttu-id="70feb-149">**通常のイメージ**: このプロパティを空白にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="70feb-149">**Normal Image**: This property can't be blank.</span></span> <span data-ttu-id="70feb-150">たとえば、**CoffeeScript** を使用します。</span><span class="sxs-lookup"><span data-stu-id="70feb-150">For example, use **CoffeeScript**.</span></span>
- <span data-ttu-id="70feb-151">**テキスト**: このプロパティを空白にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="70feb-151">**Text**: This property can't be blank.</span></span> <span data-ttu-id="70feb-152">たとえば、**分割の開始** を使用します。</span><span class="sxs-lookup"><span data-stu-id="70feb-152">For example, use **Start Break**.</span></span>
- <span data-ttu-id="70feb-153">**幅**: **自動**。</span><span class="sxs-lookup"><span data-stu-id="70feb-153">**Width**: **Auto**.</span></span>
- <span data-ttu-id="70feb-154">**高さ**: **自動**。</span><span class="sxs-lookup"><span data-stu-id="70feb-154">**Height**: **Auto**.</span></span>

### <a name="primary-button"></a><span data-ttu-id="70feb-155">プライマリ ボタン</span><span class="sxs-lookup"><span data-stu-id="70feb-155">Primary button</span></span>

<span data-ttu-id="70feb-156">スタイルは、次の要件が満たされている場合にのみ、基本ボタンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="70feb-156">Styles can be applied to a primary button only if the following requirements are met:</span></span>

+ <span data-ttu-id="70feb-157">ボタンはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="70feb-157">The button is contained in a form group.</span></span>
+ <span data-ttu-id="70feb-158">グループ名が **DefaultButtonGroup** または **PrimaryButtonGroup** で始まる (**DefaultButtonGroup10** など)。</span><span class="sxs-lookup"><span data-stu-id="70feb-158">The group name starts with **DefaultButtonGroup** or **PrimaryButtonGroup** (for example, **DefaultButtonGroup10**).</span></span>

![プライマリ ボタン](media/pfe-styles-first.png)

### <a name="secondary-button"></a><span data-ttu-id="70feb-160">セカンダリ ボタン</span><span class="sxs-lookup"><span data-stu-id="70feb-160">Secondary button</span></span>

<span data-ttu-id="70feb-161">スタイルは、次の要件が満たされている場合にのみ、二次ボタンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="70feb-161">Styles can be applied to a secondary button only if the following requirements are met:</span></span>

+ <span data-ttu-id="70feb-162">ボタンはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="70feb-162">The button is contained in a form group.</span></span>
+ <span data-ttu-id="70feb-163">グループが **右側のパネル** と名前が付けられている、またはグループ名が **SecondaryButtonGroup** で始まる。</span><span class="sxs-lookup"><span data-stu-id="70feb-163">The group is named **Right panel**, or the group name starts with **SecondaryButtonGroup**.</span></span>

![セカンダリ ボタン](media/pfe-styles-second.png)

### <a name="third-group-button"></a><span data-ttu-id="70feb-165">3 番目のグループ ボタン</span><span class="sxs-lookup"><span data-stu-id="70feb-165">Third-group button</span></span>

<span data-ttu-id="70feb-166">スタイルは、次の要件が満たされている場合にのみ、3 番目のグループのボタンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="70feb-166">Styles can be applied to a third-group button only if the following requirements are met:</span></span>

+ <span data-ttu-id="70feb-167">ボタンはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="70feb-167">The button is contained in a form group.</span></span>
+ <span data-ttu-id="70feb-168">グループが **左側のパネル** と名前が付けられている、またはグループ名が **ThirdButtonGroup** で始まる。</span><span class="sxs-lookup"><span data-stu-id="70feb-168">The group is named **Left panel**, or the group name starts with **ThirdButtonGroup**.</span></span>

![3 番目のグループのボタン](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a><span data-ttu-id="70feb-170">4 番目のグループのボタン</span><span class="sxs-lookup"><span data-stu-id="70feb-170">Fourth-group button</span></span>

<span data-ttu-id="70feb-171">スタイルは、次の要件が満たされている場合にのみ、4 番目のグループのボタンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="70feb-171">Styles can be applied to a fourth-group button only if the following requirements are met:</span></span>

+ <span data-ttu-id="70feb-172">ボタンはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="70feb-172">The button is contained in a form group.</span></span>
+ <span data-ttu-id="70feb-173">グループ名が **FourthButtonGroup** で始まる。</span><span class="sxs-lookup"><span data-stu-id="70feb-173">The group name starts with **FourthButtonGroup**.</span></span>

<span data-ttu-id="70feb-174">ボタンに以下のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="70feb-174">Set the following properties on the button:</span></span>

- <span data-ttu-id="70feb-175">**ボタン表示**: **TextOnly**。</span><span class="sxs-lookup"><span data-stu-id="70feb-175">**Button Display**: **TextOnly**.</span></span>
- <span data-ttu-id="70feb-176">**通常のイメージ**: このプロパティは空白にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="70feb-176">**Normal Image**: This property must be blank.</span></span>
- <span data-ttu-id="70feb-177">**テキスト**: このプロパティを空白にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="70feb-177">**Text**: This property can't be blank.</span></span> <span data-ttu-id="70feb-178">たとえば、**表示** または **編集** を使用します。</span><span class="sxs-lookup"><span data-stu-id="70feb-178">For example, use **View** or **Edit**.</span></span>
- <span data-ttu-id="70feb-179">**幅**: **自動**。</span><span class="sxs-lookup"><span data-stu-id="70feb-179">**Width**: **Auto**.</span></span>
- <span data-ttu-id="70feb-180">**高さ**: **自動**。</span><span class="sxs-lookup"><span data-stu-id="70feb-180">**Height**: **Auto**.</span></span>

![4 番目のグループ ボタン](media/pfe-styles-fourth.png)

### <a name="flat-button"></a><span data-ttu-id="70feb-182">フラット ボタン</span><span class="sxs-lookup"><span data-stu-id="70feb-182">Flat button</span></span>

<span data-ttu-id="70feb-183">スタイルは、次の要件が満たされている場合にのみ、フラット ボタンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="70feb-183">Styles can be applied to a flat button only if the following requirements are met:</span></span>

+ <span data-ttu-id="70feb-184">ボタンはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="70feb-184">The button is contained in a form group.</span></span>
+ <span data-ttu-id="70feb-185">グループ名が **FlatButtonGroup** で始まる。</span><span class="sxs-lookup"><span data-stu-id="70feb-185">The group name starts with **FlatButtonGroup**.</span></span>

<span data-ttu-id="70feb-186">ボタンに以下のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="70feb-186">Set the following properties on the button:</span></span>

- <span data-ttu-id="70feb-187">**ボタン表示**: **ImageOnly**。</span><span class="sxs-lookup"><span data-stu-id="70feb-187">**Button Display**: **ImageOnly**.</span></span>
- <span data-ttu-id="70feb-188">**通常のイメージ**: このプロパティを空白にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="70feb-188">**Normal Image**: This property can't be blank.</span></span> <span data-ttu-id="70feb-189">たとえば、**CoffeeScript** を使用します。</span><span class="sxs-lookup"><span data-stu-id="70feb-189">For example, use **CoffeeScript**.</span></span>
- <span data-ttu-id="70feb-190">**テキスト**: このプロパティは空白にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="70feb-190">**Text**: This property must be blank.</span></span>
- <span data-ttu-id="70feb-191">**幅**: **自動**。</span><span class="sxs-lookup"><span data-stu-id="70feb-191">**Width**: **Auto**.</span></span>
- <span data-ttu-id="70feb-192">**高さ**: **自動**。</span><span class="sxs-lookup"><span data-stu-id="70feb-192">**Height**: **Auto**.</span></span>

![フラット ボタン](media/pfe-styles-flat-button.png)

## <a name="combo-box"></a><span data-ttu-id="70feb-194">コンボ ボックス</span><span class="sxs-lookup"><span data-stu-id="70feb-194">Combo box</span></span>

<span data-ttu-id="70feb-195">コンボ ボックスは、入力コントロール、入力コントロールをクリアするボタン、および検索を実行するボタンの 3 つのコントロールの組み合わせです。</span><span class="sxs-lookup"><span data-stu-id="70feb-195">A combo box is a combination of three controls: an input control, a button that clears the input control, and a button that runs a search.</span></span>

<span data-ttu-id="70feb-196">スタイルは、次の要件が満たされている場合にのみ、コンボ ボックスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="70feb-196">Styles can be applied to a combo box only if the following requirements are met:</span></span>

+ <span data-ttu-id="70feb-197">コンボ ボックスはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="70feb-197">The combo box is contained in a form group.</span></span>
+ <span data-ttu-id="70feb-198">グループ名は **Combobox** で始まります。</span><span class="sxs-lookup"><span data-stu-id="70feb-198">The group name starts with **Combobox**.</span></span>
+ <span data-ttu-id="70feb-199">グループ内で、最初のコントロールは **AxFormStringControl** です。</span><span class="sxs-lookup"><span data-stu-id="70feb-199">Inside the group, the first control is an **AxFormStringControl** control.</span></span> <span data-ttu-id="70feb-200">このコントロールは現在の値を表示し、ユーザーは必要な値を入力します。</span><span class="sxs-lookup"><span data-stu-id="70feb-200">This control shows the current value, and it's where the user enters the required value.</span></span>
+ <span data-ttu-id="70feb-201">2 つ目のコントロールは **CommonButton** コントロールで、名前は **ClearButton** で始まります。</span><span class="sxs-lookup"><span data-stu-id="70feb-201">The second control is a **CommonButton** control, and its name starts with **ClearButton**.</span></span> <span data-ttu-id="70feb-202">このボタンには、ボタンを表示または非表示にする **enable** プロパティを使用するコードが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="70feb-202">This button must contain code that uses the **enable** property to show or hide the button.</span></span> <span data-ttu-id="70feb-203">たとえば、ユーザーが入力コントロールに情報を入力している間に **クリア** ボタンを表示または非表示にするには、次のコードを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="70feb-203">For example, to show or hide the **Clear** button while the user is typing information in the input control, you can use the following code.</span></span>

    ```xpp
    public void textChange()
    {
        super();
        ClearButtonSerial.enabled(this.text()? true : false);
    }
    ```

    <span data-ttu-id="70feb-204">入力コントロールでデータを設定する方法が 1 つ必要です。</span><span class="sxs-lookup"><span data-stu-id="70feb-204">You should have one method where the data is set in the input control.</span></span> <span data-ttu-id="70feb-205">そのメソッドの **クリア** ボタンを有効にします。</span><span class="sxs-lookup"><span data-stu-id="70feb-205">Enable the **Clear** button in that method.</span></span> <span data-ttu-id="70feb-206">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="70feb-206">Here is an example.</span></span>

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

    <span data-ttu-id="70feb-207">**クリア** ボタンの **clicked** メソッドには次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="70feb-207">Use the following code for the **clicked** method of the **Clear** button.</span></span>

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    <span data-ttu-id="70feb-208">フォームを **init** メソッドを使用して初期化するときに、入力コントロール **AxFormStringControl** の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="70feb-208">Set the value of the input control, **AxFormStringControl**, when the form is initialized by using the **init** method.</span></span> <span data-ttu-id="70feb-209">値が空白でない場合は、**クリア** ボタンを有効にします。</span><span class="sxs-lookup"><span data-stu-id="70feb-209">If the value isn't blank, enable the **Clear** button.</span></span> <span data-ttu-id="70feb-210">値が空白の場合は、**クリア** ボタンを無効にします。</span><span class="sxs-lookup"><span data-stu-id="70feb-210">If the value is blank, disable the **Clear** button.</span></span>

+ <span data-ttu-id="70feb-211">3 つ目のコントロールは **CommonButton** コントロールで、名前は **SearchButton** で始まります。</span><span class="sxs-lookup"><span data-stu-id="70feb-211">The third control is a **CommonButton** control, and its name starts with **SearchButton**.</span></span>

<span data-ttu-id="70feb-212">次の図は、2 つのコンボ ボックス コントロールを示します。</span><span class="sxs-lookup"><span data-stu-id="70feb-212">The following illustration shows two combo box controls.</span></span> <span data-ttu-id="70feb-213">左側のコンボ ボックスには空のテキスト ボックスがあり、**クリア** ボタンは無効になっています。</span><span class="sxs-lookup"><span data-stu-id="70feb-213">The combo box on the left has an empty text box, and the **Clear** button is disabled.</span></span> <span data-ttu-id="70feb-214">右側のコンボ ボックスにはテキスト ボックスにテキストがあり、**クリア** ボタンが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="70feb-214">The combo box on the right has text in the text box, and the **Clear** button is enabled.</span></span>

![クリア ボタン付き、またはなしのコンボ ボックス](media/pfe-styles-combo.png)

## <a name="dialog"></a><span data-ttu-id="70feb-216">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="70feb-216">Dialog</span></span>

<span data-ttu-id="70feb-217">スタイルは、次の要件が満たされている場合にのみ、ダイアログに適用されます。</span><span class="sxs-lookup"><span data-stu-id="70feb-217">Styles can be applied to a dialog only if the following requirements are met:</span></span>

+ <span data-ttu-id="70feb-218">ダイアログの名前が **JmgProductionFloorExecutionDialog** で始まる (**JmgProductionFloorExecutionDialogBatchNumberLookup** など)。</span><span class="sxs-lookup"><span data-stu-id="70feb-218">The name of the dialog starts with **JmgProductionFloorExecutionDialog** (for example, **JmgProductionFloorExecutionDialogBatchNumberLookup**).</span></span>
+ <span data-ttu-id="70feb-219">ダイアログのすべてのコントロールは、このトピックで説明されているように構成されます。</span><span class="sxs-lookup"><span data-stu-id="70feb-219">All the controls in the dialog are configured as described in this topic.</span></span>

<span data-ttu-id="70feb-220">スタイルは、次の要件が満たされている場合にのみ、ダイアログの **OK** ボタンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="70feb-220">Styles can be applied to the **OK** button in a dialog only if the following requirements are met:</span></span>

+ <span data-ttu-id="70feb-221">ボタンはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="70feb-221">The button is contained in a form group.</span></span>
+ <span data-ttu-id="70feb-222">グループ名が **OkButtonGroup** で始まる。</span><span class="sxs-lookup"><span data-stu-id="70feb-222">The group name starts with **OkButtonGroup**.</span></span>

<span data-ttu-id="70feb-223">スタイルは、次の要件が満たされている場合にのみ、ダイアログの **キャンセル** ボタンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="70feb-223">Styles can be applied to the **Cancel** button in a dialog only if the following requirements are met:</span></span>

+ <span data-ttu-id="70feb-224">ボタンはフォーム グループに含まれています。</span><span class="sxs-lookup"><span data-stu-id="70feb-224">The button is contained in a form group.</span></span>
+ <span data-ttu-id="70feb-225">グループ名が **CancelButtonGroup** で始まる。</span><span class="sxs-lookup"><span data-stu-id="70feb-225">The group name starts with **CancelButtonGroup**.</span></span>
