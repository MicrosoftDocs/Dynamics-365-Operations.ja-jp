---
title: 情報ボックスのフォーム パターン
description: このトピックでは、FactBox フォームのパターンについて説明します。 情報ボックスはレコードに関連情報を指定するために使用されます。
author: jasongre
manager: AnnBe
ms.date: 11/09/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 14721
ms.assetid: b3d527bf-6b56-42fb-a135-493a62eb1435
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84c2cb8536c7f2e37ede9287940baa08422a06d3
ms.sourcegitcommit: dd960cf07d8be791fd27c7bb72e6baa2d63ccd51
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/14/2019
ms.locfileid: "2578263"
---
# <a name="factbox-form-patterns"></a><span data-ttu-id="3c349-104">情報ボックスのフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="3c349-104">FactBox form patterns</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c349-105">このトピックでは、FactBox フォームのパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3c349-105">This topic provides information about the FactBox form patterns.</span></span> <span data-ttu-id="3c349-106">情報ボックスはレコードに関連情報を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3c349-106">FactBoxes are used to provide related information for a record.</span></span>

<a name="usage"></a><span data-ttu-id="3c349-107">用途</span><span class="sxs-lookup"><span data-stu-id="3c349-107">Usage</span></span>
-----

<span data-ttu-id="3c349-108">一般に、情報ボックスはレコードに「関連情報」を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3c349-108">In general, FactBoxes are used to provide “related information” for a record.</span></span> <span data-ttu-id="3c349-109">これらは、合計、残高、期限切れの注文、メール アドレスなどの重要な情報を得るために、追加のフォームを開く必要がないことを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="3c349-109">They help guarantee that the user doesn't have to open additional forms to get important information, such as totals, balances, overdue orders, and email addresses.</span></span> <span data-ttu-id="3c349-110">情報ボックス グリッド パターンは、関連情報の子コレクション (複数行の可能性がある) がある場合に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c349-110">The Factbox Grid pattern should be used when there is a child collection (potential for multiple rows) of related information.</span></span> <span data-ttu-id="3c349-111">このドキュメントでは、2 つのパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3c349-111">Two patterns are described in this document:</span></span>

-   <span data-ttu-id="3c349-112">**フォーム パターン 情報ボックス グリッド** – この情報ボックス パターンは、関連情報の子コレクション (複数行の可能性がある) がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="3c349-112">**Form Part FactBox Grid** – This FactBox pattern is used when there is a child collection (potential for multiple rows) of related information.</span></span>

<!-- -->

-   <span data-ttu-id="3c349-113">**フォーム パターン 情報ボックス カード** – この情報ボックス パターンは、表示する必要がある一連の関連するフィールドがある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="3c349-113">**Form Part FactBox Card** – This FactBox pattern is used when there is just a set of related fields that must be shown.</span></span>

## <a name="wireframe"></a><span data-ttu-id="3c349-114">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="3c349-114">Wireframe</span></span>
### <a name="form-part-factbox-grid"></a><span data-ttu-id="3c349-115">フォーム パート 情報ボックス グリッド</span><span class="sxs-lookup"><span data-stu-id="3c349-115">Form Part FactBox Grid</span></span>

<span data-ttu-id="3c349-116">[![フォーム パート情報ボックス グリッドの図](./media/factbox1.png)](./media/factbox1.png)</span><span class="sxs-lookup"><span data-stu-id="3c349-116">[![Illustration of Form Part FactBox grid](./media/factbox1.png)](./media/factbox1.png)</span></span>

### <a name="form-part-factbox-card"></a><span data-ttu-id="3c349-117">フォーム パート 情報ボックス カード</span><span class="sxs-lookup"><span data-stu-id="3c349-117">Form Part FactBox Card</span></span>

<span data-ttu-id="3c349-118">[![フォーム パート情報ボックス カードの図](./media/factbox2.png)](./media/factbox2.png)</span><span class="sxs-lookup"><span data-stu-id="3c349-118">[![Illustration of Form Part FactBox card](./media/factbox2.png)](./media/factbox2.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="3c349-119">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="3c349-119">Pattern changes</span></span>
<span data-ttu-id="3c349-120">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="3c349-120">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="3c349-121">ボタンを配置しやすくするオプション ボタンのグループが追加されました。</span><span class="sxs-lookup"><span data-stu-id="3c349-121">A group has been added around the optional button to make it easier to position the button.</span></span>

## <a name="model"></a><span data-ttu-id="3c349-122">モデル</span><span class="sxs-lookup"><span data-stu-id="3c349-122">Model</span></span>
### <a name="form-part-factbox-grid--high-level-structure"></a><span data-ttu-id="3c349-123">フォーム パート 情報ボックス グリッド – 高レベルの構造</span><span class="sxs-lookup"><span data-stu-id="3c349-123">Form Part FactBox Grid – High-level structure</span></span>

- <span data-ttu-id="3c349-124">デザイン</span><span class="sxs-lookup"><span data-stu-id="3c349-124">Design</span></span>

    - <span data-ttu-id="3c349-125">グリッド</span><span class="sxs-lookup"><span data-stu-id="3c349-125">Grid</span></span>
    - <span data-ttu-id="3c349-126">*GridDefaultAction (ボタン) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="3c349-126">*GridDefaultAction (Button) \[Optional\]*</span></span>
    - <span data-ttu-id="3c349-127">*ButtonGroup (ButtonGroup) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="3c349-127">*ButtonGroup (ButtonGroup) \[Optional\]*</span></span>

        - <span data-ttu-id="3c349-128">ボタン</span><span class="sxs-lookup"><span data-stu-id="3c349-128">Button</span></span>

###  <a name="form-part-factbox-card--high-level-structure"></a><span data-ttu-id="3c349-129">フォーム パート 情報ボックス カード – 高レベルの構造</span><span class="sxs-lookup"><span data-stu-id="3c349-129">Form Part FactBox Card – High-level structure</span></span>

- <span data-ttu-id="3c349-130">デザイン</span><span class="sxs-lookup"><span data-stu-id="3c349-130">Design</span></span>

    - <span data-ttu-id="3c349-131">*フィールド グループ (グループ)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="3c349-131">*FieldGroups (Group) \[0..N\]*</span></span>

        - <span data-ttu-id="3c349-132">フィールド ($Fields、1..N)</span><span class="sxs-lookup"><span data-stu-id="3c349-132">Fields ($Fields, 1..N)</span></span>

    - <span data-ttu-id="3c349-133">*フィールド ($ フィールド)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="3c349-133">*Fields ($Field) \[0..N\]*</span></span>
    - <span data-ttu-id="3c349-134">*ButtonGroup (ButtonGroup) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="3c349-134">*ButtonGroup (ButtonGroup) \[Optional\]*</span></span>

        - <span data-ttu-id="3c349-135">ボタン</span><span class="sxs-lookup"><span data-stu-id="3c349-135">Button</span></span>

### <a name="core-components"></a><span data-ttu-id="3c349-136">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="3c349-136">Core components</span></span>

-   <span data-ttu-id="3c349-137">**Form.Design** に情報ボックス パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="3c349-137">Apply the FactBox pattern on **Form.Design**.</span></span>
-   <span data-ttu-id="3c349-138">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="3c349-138">Address BP Warnings:</span></span>
    -   <span data-ttu-id="3c349-139">**Design.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="3c349-139">**Design.Caption** isn't empty.</span></span>
    -   <span data-ttu-id="3c349-140">**Grid.DataSource** が空ではありません。</span><span class="sxs-lookup"><span data-stu-id="3c349-140">**Grid.DataSource** isn't empty.</span></span>

## <a name="ux-guidelines"></a><span data-ttu-id="3c349-141">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="3c349-141">UX guidelines</span></span>
<span data-ttu-id="3c349-142">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="3c349-142">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="3c349-143">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="3c349-143">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="3c349-144">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="3c349-144">Open the form in the browser, and walk through these steps.</span></span> <span data-ttu-id="3c349-145">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="3c349-145">**Standard form guidelines:**</span></span>

-   <span data-ttu-id="3c349-146">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="3c349-146">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="3c349-147">**情報ボックス** **全般的なガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="3c349-147">**FactBox** **general guidelines:**</span></span>

-   <span data-ttu-id="3c349-148">バッキング フォームが存在する場合、情報ボックスには適切なバッキング フォームに進むたまの **(その他...)** リンクが定義されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c349-148">If a backing form exists, the FactBox should have a **(More…)** link defined that goes to the appropriate backing form.</span></span> <span data-ttu-id="3c349-149">情報ボックスとバッキングフォームの名前は似ている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c349-149">The names of the FactBox and backing form should be similar.</span></span>
-   <span data-ttu-id="3c349-150">タイトルは動詞または動詞句にはできません。</span><span class="sxs-lookup"><span data-stu-id="3c349-150">The title should not be a verb or a verb phrase.</span></span>
-   <span data-ttu-id="3c349-151">タイトルには、特定のレコードのラベルを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="3c349-151">The title should not contain a label to a specific record.</span></span>
-   <span data-ttu-id="3c349-152">情報ボックスでは、キーボードで入力することでユーザーがデータを入力できるようにするフィールドを表示すべきではありません。</span><span class="sxs-lookup"><span data-stu-id="3c349-152">FactBoxes should not display fields that let a user enter data by typing with the keyboard.</span></span>
-   <span data-ttu-id="3c349-153">タイトルはコンテンツを正確に記述する必要があり、FactBox 領域が規定サイズのときは切り捨てるべきではありません。</span><span class="sxs-lookup"><span data-stu-id="3c349-153">The title should accurately describe the content and should not be truncated when the FactBox area is at its default size.</span></span>

<span data-ttu-id="3c349-154">**情報ボックス グリッド ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="3c349-154">**FactBox grid guidelines:**</span></span>

-   <span data-ttu-id="3c349-155">1 列から 4 列が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3c349-155">One to four columns should be displayed.</span></span>

<span data-ttu-id="3c349-156">**情報ボックス カード ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="3c349-156">**FactBox card guidelines:**</span></span>

-   <span data-ttu-id="3c349-157">各フィールドには、ラベルが必要です。</span><span class="sxs-lookup"><span data-stu-id="3c349-157">Each field should have a label.</span></span>
-   <span data-ttu-id="3c349-158">情報ボックスにコンテンツが表示されているヘッダーおよび行の ID と名前は、表示されません。</span><span class="sxs-lookup"><span data-stu-id="3c349-158">The ID and name of the header or the line that content is displayed for in the FactBox should not be displayed.</span></span>
-   <span data-ttu-id="3c349-159">2 ~ 10 フィールドが表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c349-159">Two to ten fields should be displayed.</span></span>
-   <span data-ttu-id="3c349-160">通貨インジケータ フィールドは、情報ボックスの最後のフィールドとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="3c349-160">Currency indicator fields should be displayed as the last field in the FactBox.</span></span>

## <a name="examples"></a><span data-ttu-id="3c349-161">例</span><span class="sxs-lookup"><span data-stu-id="3c349-161">Examples</span></span>
### <a name="form-part-factbox-grid"></a><span data-ttu-id="3c349-162">フォーム パート 情報ボックス グリッド</span><span class="sxs-lookup"><span data-stu-id="3c349-162">Form Part FactBox Grid</span></span>

<span data-ttu-id="3c349-163">フォーム: **CustTable** &gt; **ContactsInfoPart**</span><span class="sxs-lookup"><span data-stu-id="3c349-163">Form: **CustTable** &gt; **ContactsInfoPart**</span></span> 

<span data-ttu-id="3c349-164">[![フォーム パート情報ボックス グリッドの例](./media/factbox3.png)](./media/factbox3.png)</span><span class="sxs-lookup"><span data-stu-id="3c349-164">[![Example of Form Part FactBox grid](./media/factbox3.png)](./media/factbox3.png)</span></span>

### <a name="form-part-factbox-card"></a><span data-ttu-id="3c349-165">フォーム パート 情報ボックス カード</span><span class="sxs-lookup"><span data-stu-id="3c349-165">Form Part FactBox Card</span></span>

<span data-ttu-id="3c349-166">フォーム: **CustTable** &gt; **CustStatisticsStatistics**</span><span class="sxs-lookup"><span data-stu-id="3c349-166">Form: **CustTable** &gt; **CustStatisticsStatistics**</span></span> 

<span data-ttu-id="3c349-167">[![フォーム パート情報ボックス カードの例](./media/factbox4.png)](./media/factbox4.png)</span><span class="sxs-lookup"><span data-stu-id="3c349-167">[![Example of Form Part FactBox card](./media/factbox4.png)](./media/factbox4.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="3c349-168">付録</span><span class="sxs-lookup"><span data-stu-id="3c349-168">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="3c349-169">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="3c349-169">Frequently asked questions</span></span>

<span data-ttu-id="3c349-170">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="3c349-170">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

-   <span data-ttu-id="3c349-171">**詳細ボタンを動作させる方法。**</span><span class="sxs-lookup"><span data-stu-id="3c349-171">**How do I make the More button work?**</span></span>
    -   <span data-ttu-id="3c349-172">情報ボックスの下部にある **詳細** ボタンをクリックすると、関連するレコードの完全な一覧を含むバッキング フォームに移動します。</span><span class="sxs-lookup"><span data-stu-id="3c349-172">The **More** button at the bottom of the FactBox takes the user to a backing form that contains the full list of related records.</span></span> <span data-ttu-id="3c349-173">このボタンは、次の例のように **クリック済み** メソッドをオーバーライドする通常のボタン コントロールを使用して実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c349-173">This button should be implemented by using a regular Button control that overrides the **clicked** method as shown in the following example.</span></span> <span data-ttu-id="3c349-174">グリッドのデータを提供するテーブルの **TableRef** および **ListPageRef** プロパティに必ず入力してください。</span><span class="sxs-lookup"><span data-stu-id="3c349-174">Be sure to fill in the **TableRef** and **ListPageRef** properties on the table that provides data for the grid.</span></span>

            [Control("Button")]
            class More
            {
            public void clicked()
                   {    
                        super();  
                        FormPartUtil::openShowMoreForm(element, <TableName>);     
                   }
            }

### <a name="open-issues"></a><span data-ttu-id="3c349-175">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="3c349-175">Open issues</span></span>

-   <span data-ttu-id="3c349-176">**フィールド ラベルはコンパクト ビジュアルをサポートするために情報ボックスの左側に置くべきですか。**</span><span class="sxs-lookup"><span data-stu-id="3c349-176">**Should field labels be on the left side in FactBoxes to support a more compact visual?**</span></span>
    -   <span data-ttu-id="3c349-177">Factbox 内で **LabelPosition**=**左** と設定できるようにする予定です。</span><span class="sxs-lookup"><span data-stu-id="3c349-177">We plan to allow **LabelPosition**=**Left** inside FactBoxes.</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="3c349-178">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="3c349-178">AX 2012 content</span></span>

#### <a name="ax-2012-links"></a><span data-ttu-id="3c349-179">AX 2012 リンク</span><span class="sxs-lookup"><span data-stu-id="3c349-179">AX 2012 links</span></span>

-   [<span data-ttu-id="3c349-180">AX 2012 MSDN リスト ページ ガイドライン (FactBoxes を含む)</span><span class="sxs-lookup"><span data-stu-id="3c349-180">AX 2012 MSDN List Page Guidelines (including FactBoxes)</span></span>](https://msdn.microsoft.com/library/gg853328.aspx)

#### <a name="ax-2012-example"></a><span data-ttu-id="3c349-181">AX 2012 の例</span><span class="sxs-lookup"><span data-stu-id="3c349-181">AX 2012 example</span></span>

<span data-ttu-id="3c349-182">**CustTable** &gt; **ContactsInfoPart**</span><span class="sxs-lookup"><span data-stu-id="3c349-182">**CustTable** &gt; **ContactsInfoPart**</span></span> 

<span data-ttu-id="3c349-183">[![情報ボックスの例](./media/factbox5.png)](./media/factbox5.png)</span><span class="sxs-lookup"><span data-stu-id="3c349-183">[![Example of FactBox](./media/factbox5.png)](./media/factbox5.png)</span></span>