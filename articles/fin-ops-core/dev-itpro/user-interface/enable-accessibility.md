---
title: フォーム、製品、およびコントロールのユーザー補助機能
description: このトピックは、フォーム、製品、またはコントロールのユーザー補助機能を有効にするためのベスト プラクティスについて説明します。 アクセシビリティ チェックリストも含まれます。
author: RobinARH
manager: AnnBe
ms.date: 08/13/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 104943
ms.assetid: 5b97c471-212a-4487-baef-120d01063319
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 15d0eb32fb6588d82f2c3bd0cb3c3c97c47ab1e2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686608"
---
# <a name="accessibility-in-forms-products-and-controls"></a><span data-ttu-id="d3ec3-104">フォーム、製品、およびコントロールのユーザー補助機能</span><span class="sxs-lookup"><span data-stu-id="d3ec3-104">Accessibility in forms, products, and controls</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3ec3-105">このトピックは、フォーム、製品、またはコントロールのユーザー補助機能を有効にするためのベスト プラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-105">This topic describes best practices for enabling accessibility in your form, product, or control.</span></span> <span data-ttu-id="d3ec3-106">アクセシビリティ チェックリストも含まれます。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-106">An accessibility checklist is also included.</span></span>

<span data-ttu-id="d3ec3-107">ユーザー補助は包括的です。つまり、障害のある人は、障害のない人と同じタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-107">Accessibility is about inclusion, that is, a person with a disability can perform the same task as a person without that disability.</span></span> <span data-ttu-id="d3ec3-108">アクセス可能なコントロールまたはフォームの作成は、セキュリティで保護され、高性能、または理解しやすい基本的なものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-108">Making an accessible control or form should be as fundamental as making it secure, high-performing, or easy-to-understand.</span></span>

## <a name="keyboard"></a><span data-ttu-id="d3ec3-109">キーボード</span><span class="sxs-lookup"><span data-stu-id="d3ec3-109">Keyboard</span></span>

<span data-ttu-id="d3ec3-110">アクセシビリティの基盤はキーボード専用アクセスです。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-110">The bedrock of accessibility is keyboard-only access.</span></span> <span data-ttu-id="d3ec3-111">キーボードを使用してフォームのすべてのアクションを実行できるとき、全盲の人または手の使用に制限がある人がこのフォームを利用できます。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-111">When you can use the keyboard to perform all the actions of a form, then it can be utilized by a non-sighted person or a person with restricted or limited use of their hands.</span></span> <span data-ttu-id="d3ec3-112">これは、タブ シーケンス、直接アクション (保存の **Ctrl + S** など)、またはユーザーがナビゲーション ペイン、アプリ バー、メッセージ センター、メッセージ バーなどのコントロールに移動できるようにする他のショートカット キーを使用してすべてのコントロールに到達できることを意味します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-112">This means that all controls can be reached via the tab sequence, direct action (such as **Ctrl+S** for Save), or through some other shortcut key that enables the user to move to a control, such as Navigation Pane, App Bar, Message Center, or Message Bar.</span></span> <span data-ttu-id="d3ec3-113">簡単なテストでは、単にマウスを取り外し、キーボードのみを使用してすべてのコア シナリオとセカンダリ シナリオを完了します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-113">A simple test is to simply disconnect your mouse and complete all core and secondary scenarios using only the keyboard.</span></span>

## <a name="color"></a><span data-ttu-id="d3ec3-114">色</span><span class="sxs-lookup"><span data-stu-id="d3ec3-114">Color</span></span>

<span data-ttu-id="d3ec3-115">色の使用が推奨されており、記録やその他の情報の状態や状態を表す一般的な方法です。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-115">The use of color is encouraged and is a common way to express state or status of a record or other piece of information.</span></span> <span data-ttu-id="d3ec3-116">ただし、色は、状態またはステータスが伝達される唯一の方法ではありません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-116">However, color cannot be the only way that state or status is communicated.</span></span> <span data-ttu-id="d3ec3-117">付属記号、ヘルプ テキスト、または追加の列に、状態またはステータスのテキスト説明を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-117">An accompanying symbol, help text, or additional column should include a textual description of the state or status.</span></span> <span data-ttu-id="d3ec3-118">簡単なテストは、システムのすべての色の使用を識別し、色が状態またはステータスを表すために使用されていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-118">A simple test is to identify all use of color in your system and ensure that color isn't being used to express a state or status.</span></span> <span data-ttu-id="d3ec3-119">一般的な例では、赤色は「注意が必要」を表し、緑色は「OK」の状態を意味します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-119">A common example is to use the color red to indicate "needs attention," or the color green to mean an "OK" status.</span></span>

## <a name="images"></a><span data-ttu-id="d3ec3-120">イメージ</span><span class="sxs-lookup"><span data-stu-id="d3ec3-120">Images</span></span>

<span data-ttu-id="d3ec3-121">画像を表示するとき、画像を説明するラベルが必要です。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-121">When showing an image there should be a label that describes the image.</span></span> <span data-ttu-id="d3ec3-122">イメージがレコードの状態またはステータスを表す場合は、付随するヘルプ テキストまたは追加の列に、状態またはステータスの説明文を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-122">If the image expresses state or status of a record, then accompanying help text or an additional column should include a textual description of the state or status.</span></span> <span data-ttu-id="d3ec3-123">イメージがロゴのような記号である場合は、説明は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-123">If the image is symbolic, like a logo, then it doesn’t require a textual description.</span></span> <span data-ttu-id="d3ec3-124">「進行中」などのステータスを伝えるフォームまたはグリッド上にイメージがある場合、スクリーン リーダーを使用している人に読み取られるツールチップがイメージにあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-124">If you have an image on a form or grid to convey a status, such as "in progress", ensure that the image has a tooltip that can then be read to someone who is utilizing a screen reader.</span></span>

```xpp
public display container statusImageDataMethod()
{
    ImageReference statusImage;
    if (this.Status == NoYes::Yes)
    {
        statusImage = ImageReference::constructForSymbol(ImageReferenceSymbol::Accept, "Accept");
        // a product ready example would use a label in place of an embedded string
    }
    else
    {
        statusImage = ImageReference::constructForSymbol(ImageReferenceSymbol::Cancel, "Cancel");  
        // a product ready example would use a label in place of an embedded string
    }
    return statusImage.pack();
}
```

## <a name="extensible-controls"></a><span data-ttu-id="d3ec3-125">拡張可能なコントロール</span><span class="sxs-lookup"><span data-stu-id="d3ec3-125">Extensible controls</span></span>

<span data-ttu-id="d3ec3-126">拡張可能なコントロールは、単にフレームワークによって提供されるコントロールの拡張子ですが、同じ使いやすさとアクセシビリティが必要です。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-126">Extensible controls are simply an extension of the controls that are provided by the framework, but require the same usability and accessibility.</span></span> <span data-ttu-id="d3ec3-127">さらに、セグメント化されたエントリ コントロールやグラフなどのウィジェットまたは他の視覚的にリッチなコントロールは、目が見えるユーザーから非表示になるアクセス可能リッチ インターネット アプリケーション (ARIA) タグを提供する必要がありますが、目の見えないユーザーにはスクリーン リーダーを通じてコントロールの使用について説明を提示します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-127">In addition, widgets or other visually rich controls, such as segmented entry controls or charts, should provide an Accessible Rich Internet Applications (ARIA) tag that is hidden from the sighted user, but provides an introduction to the blind user through a screen reader that describes the use of the control.</span></span> <span data-ttu-id="d3ec3-128">拡張可能コントロールのすべてのアクションは、キーボードで可能でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-128">Every action in an extensible control must be possible with a keyboard.</span></span>

## <a name="layout-and-dynamic-management-of-forms"></a><span data-ttu-id="d3ec3-129">フォームのレイアウトと動的管理</span><span class="sxs-lookup"><span data-stu-id="d3ec3-129">Layout and dynamic management of forms</span></span>

<span data-ttu-id="d3ec3-130">視覚に障害があるまたは盲人のユーザーが、値の選択や入力などのアクションによって、大幅にまたは予期せずにフォームの再レイアウトをするとしても驚くことはありません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-130">A visually impaired or blind user cannot be surprised by significant or unexpected re-laying out of a form based on an action such as selecting a value or entering input.</span></span>

### <a name="accessibility-checklist"></a><span data-ttu-id="d3ec3-131">アクセシビリティ チェックリスト</span><span class="sxs-lookup"><span data-stu-id="d3ec3-131">Accessibility checklist</span></span>

| <span data-ttu-id="d3ec3-132">措置</span><span class="sxs-lookup"><span data-stu-id="d3ec3-132">Measure</span></span> | <span data-ttu-id="d3ec3-133">説明</span><span class="sxs-lookup"><span data-stu-id="d3ec3-133">Description</span></span> | <span data-ttu-id="d3ec3-134">成功基準</span><span class="sxs-lookup"><span data-stu-id="d3ec3-134">Success criteria</span></span> | <span data-ttu-id="d3ec3-135">検証済み (x)</span><span class="sxs-lookup"><span data-stu-id="d3ec3-135">Validated (x)</span></span> |
|---|--------------|----------------------|-------------------|
| <span data-ttu-id="d3ec3-136">すべての機能に対するキーボードのみのアクセス</span><span class="sxs-lookup"><span data-stu-id="d3ec3-136">Keyboard-only access to all functions</span></span> | <span data-ttu-id="d3ec3-137">ドリル ダウン、ルックアップ、ハイパーリンク、データ入力アクション、およびショートカットキー。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-137">Drill downs, lookups, hyperlinks, data input actions, and shortcut keys.</span></span>         | <span data-ttu-id="d3ec3-138">すべてのアクションはマウスを使用せずに完了することができます。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-138">All action may be completed without the use of a mouse.</span></span>     | |
| <span data-ttu-id="d3ec3-139">表示されているフォーカス インジケーター</span><span class="sxs-lookup"><span data-stu-id="d3ec3-139">Visible focus indicator</span></span>       |    | <span data-ttu-id="d3ec3-140">どのコントロールがフォーカスされているか常に明らかになります。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-140">It’s always apparent which control has focus.</span></span>               | |
| <span data-ttu-id="d3ec3-141">フォーカス注文</span><span class="sxs-lookup"><span data-stu-id="d3ec3-141">Focus order</span></span>           | <span data-ttu-id="d3ec3-142">非論理的な場所に「ジャンプ」することはできません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-142">Cannot “jump to” a non-logical location.</span></span>           | <span data-ttu-id="d3ec3-143">タブ移動では、非論理的部分またはフォームの予期しない部分にはジャンプしません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-143">Tabbing doesn’t jump to a non-logical portion or unexpected portion of the form.</span></span>  | |
| <span data-ttu-id="d3ec3-144">フォーカス トラッピング</span><span class="sxs-lookup"><span data-stu-id="d3ec3-144">Focus trapping</span></span>                | <span data-ttu-id="d3ec3-145">コントロールに「トラップ」することはできませんが、フォーカスはキーボードを使用して管理外にできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-145">Cannot be “trapped” in a control, focus must be able to move out of control using the keyboard.</span></span>            | <span data-ttu-id="d3ec3-146">コントロールにタブ移動した場合、タブ アウトや、エスケープを可能にする同等のショートカット キーを許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-146">Tabbing into a control should allow tabbing out or a keyboard equivalent that lets them escape.</span></span>             | |
| <span data-ttu-id="d3ec3-147">テキストのイメージ</span><span class="sxs-lookup"><span data-stu-id="d3ec3-147">Images of text</span></span>                | <span data-ttu-id="d3ec3-148">イメージを使ってテキストを表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-148">Cannot use an image to display text.</span></span>               | <span data-ttu-id="d3ec3-149">たとえば、テキストの画像であるボタン ラベルを持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-149">For example, you cannot have a button label that is an image of text.</span></span> <span data-ttu-id="d3ec3-150">ロゴは除外されます。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-150">Logos are exempt.</span></span>  | |
| <span data-ttu-id="d3ec3-151">色の使用</span><span class="sxs-lookup"><span data-stu-id="d3ec3-151">Using color</span></span>           | <span data-ttu-id="d3ec3-152">色だけではステータスや状態を伝えることはできません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-152">Color alone cannot be used to convey status or state.</span></span>      | <span data-ttu-id="d3ec3-153">フォームまたはグリッド上のすべてのステータス インジケーターはユニークな形状または各色のためのテクスチャを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-153">All status indicators on a form or grid must have unique shape or texture for each color.</span></span> <span data-ttu-id="d3ec3-154">詳細については、このドキュメントの「色」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-154">See the "Color" section in this document for more information.</span></span>            | |
| <span data-ttu-id="d3ec3-155">テキストのコントラスト</span><span class="sxs-lookup"><span data-stu-id="d3ec3-155">Text contrast</span></span>                 | <span data-ttu-id="d3ec3-156">最低 4.5:1 の比率です。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-156">Minimum 4.5:1 ratio.</span></span>     | <span data-ttu-id="d3ec3-157">拡張可能なコントロールは、コンプライアンスを確実にするためにフレームワーク カラーのテーマを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-157">Extensible controls should use framework color theming to ensure compliance.</span></span>      | |
| <span data-ttu-id="d3ec3-158">ユーザー入力の手順</span><span class="sxs-lookup"><span data-stu-id="d3ec3-158">User input instructions</span></span>       | <span data-ttu-id="d3ec3-159">ウィジェットまたは他のマルチ ステップ コントロールには、ユーザビリティ概要ラベルまたはヘルプ テキスト (ARIA タグ内に埋め込み可能) が必要です。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-159">Widgets or other multi-step controls must have a usability overview label or help text (can be embedded in ARIA tag).</span></span>            | <span data-ttu-id="d3ec3-160">スクリーン リーダーを使用するとき、コントロールを導入とそのラベルまたは目的の説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-160">When using a screen reader, the control must be introduced and its label or purpose described.</span></span>              | |
| <span data-ttu-id="d3ec3-161">コンテキストの変更</span><span class="sxs-lookup"><span data-stu-id="d3ec3-161">Change of context</span></span>             | <span data-ttu-id="d3ec3-162">UI コンポーネントの設定変更、またはUI コンポーネントへのデータ入力が、自動的に予期せぬコンテキストの変更を自動的に引き起こし、コンテキストの変更が発生することをユーザに最初に知らせずにユーザーを混乱させることはありません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-162">Changing the setting of, or entering data into any UI component must not automatically cause an unexpected change of context that might disorient the user without first notifying the user that the change of context will occur.</span></span> | <span data-ttu-id="d3ec3-163">たとえば、ドロップダウン ボックスで値を選択またはチェック ボックスをクリックしても、フォームのレイアウトが予期せずにまたは非標準の方法で変更されることはありません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-163">For example, selecting a value in a drop-down box or clicking a check box shouldn’t change the layout of the form unexpectedly or in a non-standard way.</span></span>            | |
| <span data-ttu-id="d3ec3-164">整合性のある UI</span><span class="sxs-lookup"><span data-stu-id="d3ec3-164">Consistent UI</span></span>                 | <span data-ttu-id="d3ec3-165">ウィジェットまたは他の要素は製品全体で一貫して動作する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-165">Widgets or other elements must work consistently across the product.</span></span> <span data-ttu-id="d3ec3-166">異なる動作をする、2 つの類似した外観やモデル化された要素は存在できません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-166">There cannot be two similar looking or modeled elements that behave differently.</span></span>              | <span data-ttu-id="d3ec3-167">たとえば、チェック ボックスを選択してもウィンドウは開きません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-167">For example, selecting a check box shouldn’t open a window.</span></span>         | |
| <span data-ttu-id="d3ec3-168">優れたモーター制御</span><span class="sxs-lookup"><span data-stu-id="d3ec3-168">Fine motor control</span></span>            | <span data-ttu-id="d3ec3-169">マウスを使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-169">Cannot require use of the mouse.</span></span> <span data-ttu-id="d3ec3-170">「固定キー」をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-170">Must support “sticky keys.”</span></span>             | <span data-ttu-id="d3ec3-171">ユーザーは、移動するターゲットをクリックするように強制したり (プル右)、マウスを必要とするその他のアクションを強制したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-171">User cannot be forced to click a moving target (pull right) or any other action that requires a mouse.</span></span> <span data-ttu-id="d3ec3-172">キーボードでも同じ操作が可能でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-172">The same action must also be possible with the keyboard.</span></span>             | |
| <span data-ttu-id="d3ec3-173">ビデオの使用</span><span class="sxs-lookup"><span data-stu-id="d3ec3-173">Use of video</span></span>          | <span data-ttu-id="d3ec3-174">ビデオ (オーディオ付き) はテキスト付きである必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-174">Video (with audio) must have accompanied text.</span></span>     | <span data-ttu-id="d3ec3-175">あらかじめ記録されたコンテンツを表示するとき、聴覚に障害のある人は、コンテンツを使用するためにサポートするテキストが必要です。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-175">When showing pre-recorded content, the deaf person must have supporting text to consume the content.</span></span>                | |
| <span data-ttu-id="d3ec3-176">イメージの使用</span><span class="sxs-lookup"><span data-stu-id="d3ec3-176">Use of images</span></span>                 |    | <span data-ttu-id="d3ec3-177">すべてのイメージは特定のコンテンツを説明するテキストに添付される必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-177">All images must be accompanied by text that describes the specific content.</span></span> <span data-ttu-id="d3ec3-178">たとえば、状態またはステータスを説明および一致するグリッドでの「ツールヒント」または副次列。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-178">For example, a “tooltip” or secondary column in a grid that describes and matches the state or status.</span></span>  | |
| <span data-ttu-id="d3ec3-179">通信</span><span class="sxs-lookup"><span data-stu-id="d3ec3-179">Communication</span></span>                 | <span data-ttu-id="d3ec3-180">Skype などの VoIP やその他の電気通信デバイスやソフトウェアは、キーボードからアクセス可能で利用可能でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-180">Use of VoIP or other telecommunication device or software, such as Skype, must be accessible and usable from the keyboard.</span></span>       | <span data-ttu-id="d3ec3-181">VoIP または電気通信の使用は法的義務です。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-181">Any use of VoIP or telecommunication is a legal obligation.</span></span>         | |
| <span data-ttu-id="d3ec3-182">ナビゲーション</span><span class="sxs-lookup"><span data-stu-id="d3ec3-182">Navigation</span></span>            |    | <span data-ttu-id="d3ec3-183">ナビゲーション コントロールは、実行された場合にナビゲーションが発生することを通信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-183">Navigation controls must communicate that navigation will occur if executed.</span></span>      | |

## <a name="extensible-controls--insights-for-accessibility"></a><span data-ttu-id="d3ec3-184">拡張可能なコントロール - アクセシビリティのインサイト</span><span class="sxs-lookup"><span data-stu-id="d3ec3-184">Extensible controls – insights for accessibility</span></span>

<span data-ttu-id="d3ec3-185">拡張可能コントロールは、単にフレームワークの拡張です。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-185">An extensible control is simply an extension of the framework.</span></span> <span data-ttu-id="d3ec3-186">拡張可能なコントロールの相互作用は、他のどのフレームワーク コントロールとも変わらないと考えられるべきです。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-186">The interaction of the extensible control should be considered no different than any other framework control.</span></span> <span data-ttu-id="d3ec3-187">コントロールがマウス アクションを提供する視覚的にリッチなウィジェットであるとき、作成者は、同等のキーボード アクセス機能を使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-187">When the control is a visually-rich widget that offers mouse actions, the author needs to ensure that equivalent, keyboard access functionality is available.</span></span> <span data-ttu-id="d3ec3-188">ウィジェットは、標準的なプレゼンテーションとは異なる「アクセス可能モード」で実行されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-188">A widget may not run in an “accessible mode” that is different than the standard presentation.</span></span> <span data-ttu-id="d3ec3-189">代わりに、ウィジェットはコントロールの状態を有効化したり切り替えたりする必要なく同様の機能を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-189">Instead the widget must offer similar functionality without the need to activate or toggle state of the control.</span></span> <span data-ttu-id="d3ec3-190">すべてのカラーの使用はテーマ カラーに基づいている必要があります。モードが「ハイ コントラスト」の場合、配色がテーマの変更と一致します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-190">All uses of color should be based on themed colors so that when the mode is “High Contrast” your color scheme matches the theme change.</span></span> <span data-ttu-id="d3ec3-191">World Wide Web コンソーシアム (W3C) Web サイトは、[サポートされている状態およびプロパティ](https://www.w3.org/WAI/PF/aria-1.1/states_and_properties) のガイダンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-191">The World Wide Web Consortium (WC3) website provides guidance for [Supported States and Properties](https://www.w3.org/WAI/PF/aria-1.1/states_and_properties).</span></span> <span data-ttu-id="d3ec3-192">このサイトは、ARIA タグの役に立つリソースであり、以下に示す定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-192">This site is a helpful resource for ARIA tags and provides the definitions that you see below.</span></span>

### <a name="controls-should-do-this"></a><span data-ttu-id="d3ec3-193">コントロールが行う必要がある操作</span><span class="sxs-lookup"><span data-stu-id="d3ec3-193">Controls should do this</span></span>

#### <a name="introduce-itself"></a><span data-ttu-id="d3ec3-194">それ自体を導入します</span><span class="sxs-lookup"><span data-stu-id="d3ec3-194">Introduce itself</span></span>

<span data-ttu-id="d3ec3-195">重要なことは、コントロールを名前で識別するだけではなく、(ラベルまたは ARIA タグを使用して) 動作の簡単な概要を示すべきであることです。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-195">Importantly, your control should not only identify itself by name, but (using a label or ARIA tag) give a brief introduction on how it works.</span></span> <span data-ttu-id="d3ec3-196">説明テキストがローカライズ用のフレームワーク ラベル経由で指定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-196">Make sure your descriptive text is supplied via a framework label for localization.</span></span>

- <span data-ttu-id="d3ec3-197">*aria describedby* - オブジェクトを説明する要素 (または複数の要素) を識別します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-197">*aria-describedby* - Identifies the element (or elements) that describes the object.</span></span>

#### <a name="introduce-itself---example"></a><span data-ttu-id="d3ec3-198">それ自体の導入 - 例</span><span class="sxs-lookup"><span data-stu-id="d3ec3-198">Introduce itself - example</span></span>

```html
<http://www.w3.org/TR/WCAG20-TECHS/ARIA1.html>
<button aria-label="Close" aria-describedby="descriptionClose" onclick="myDialog.close()"></button>
<div id="descriptionClose">Closing this window will discard any information entered and return you to the main page</div>
```

#### <a name="indicate-when-it-is-busy"></a><span data-ttu-id="d3ec3-199">ビジー状態であることを示します</span><span class="sxs-lookup"><span data-stu-id="d3ec3-199">Indicate when it is busy</span></span>

<span data-ttu-id="d3ec3-200">視覚障害のあるユーザーにとって、なぜコントロールが反応しないのかは、必ずしも明確ではないかもしれません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-200">It may not always be clear to the visually-impaired user why the control isn’t responsive.</span></span> <span data-ttu-id="d3ec3-201">「ビジー」のメッセージを指定すると、そのような場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-201">Providing a “busy” message helps in these cases.</span></span>

- <span data-ttu-id="d3ec3-202">*aria-busy (状態)* - 要素とそのサブツリーが現在更新されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-202">*aria-busy (state)* - Indicates whether an element, and its subtree, are currently being updated.</span></span>

#### <a name="indicate-when-it-is-busy---example"></a><span data-ttu-id="d3ec3-203">ビジー状態であることを示す - 例</span><span class="sxs-lookup"><span data-stu-id="d3ec3-203">Indicate when it is busy - example</span></span>

```html
<p aria-live=”polite” aria-busy=”true”></p>
```

#### <a name="indicate-that-the-contents-have-been-validated-and-are-invalid"></a><span data-ttu-id="d3ec3-204">内容が検証されて、有効でないことを示す</span><span class="sxs-lookup"><span data-stu-id="d3ec3-204">Indicate that the contents have been validated and are invalid</span></span>

<span data-ttu-id="d3ec3-205">非同期の性質により、フィールド状態の動的な変化が発生します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-205">The async nature will result in a dynamic field state change.</span></span> <span data-ttu-id="d3ec3-206">メッセージ バーは、それ自体を視覚障害のあるユーザーに紹介し、コントロール自体は無効な状態を表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-206">The message bar will introduce itself to the visually-impaired user, and the control itself should express an invalid state.</span></span>

- <span data-ttu-id="d3ec3-207">*aria-invalid (状態)* - 入力された値が、アプリケーションが予期している形式に準拠していないことを示します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-207">*aria-invalid (state)* - Indicates the entered value does not conform to the format expected by the application.</span></span>

#### <a name="indicate-when-a-field-is-readonly"></a><span data-ttu-id="d3ec3-208">フィールドが読み取りであることを示します</span><span class="sxs-lookup"><span data-stu-id="d3ec3-208">Indicate when a field is readonly</span></span>

- <span data-ttu-id="d3ec3-209">*aria-readonly* - 要素が編集可能ではなく、操作可能であることを示します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-209">*aria-readonly* - Indicates that the element is not editable, but is otherwise operable.</span></span> <span data-ttu-id="d3ec3-210">関連する *aria-disabled* を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-210">See related *aria-disabled*.</span></span>

#### <a name="indicate-that-the-field-requires-input-mandatory"></a><span data-ttu-id="d3ec3-211">フィールドに入力が必要であることを示します (必須)</span><span class="sxs-lookup"><span data-stu-id="d3ec3-211">Indicate that the field requires input (mandatory)</span></span>

<span data-ttu-id="d3ec3-212">視覚的なシンボルによって、目の見えるユーザーはフィールドが必須であることを理解できます。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-212">The sighted user understands that a field is mandatory through a visual symbol.</span></span> <span data-ttu-id="d3ec3-213">盲目のユーザーには識別タグが必要です。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-213">The non-sighted user will need an identifying tag.</span></span>

- <span data-ttu-id="d3ec3-214">*aria-required* - フォームが送信される前に、要素にユーザー 入力が必要であることを示します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-214">*aria-required* - Indicates that user input is required on the element before a form may be submitted.</span></span>

#### <a name="describe-the-state-of-a-toggled-value"></a><span data-ttu-id="d3ec3-215">切り替えられた値の状態を説明</span><span class="sxs-lookup"><span data-stu-id="d3ec3-215">Describe the state of a toggled value</span></span>

<span data-ttu-id="d3ec3-216">切り替えコントロールには切り替え状態があります。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-216">A toggle control has a toggled state.</span></span> <span data-ttu-id="d3ec3-217">このタグがその状態が表わしています。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-217">This tag will express that state.</span></span>

- <span data-ttu-id="d3ec3-218">*aria-pressed (状態)* - 切り替えボタンの現在の「押された」状態を示します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-218">*aria-pressed (state)* - Indicates the current "pressed" state of toggle buttons.</span></span> <span data-ttu-id="d3ec3-219">関連する *aria-checked* および *aria-selected* を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-219">See related *aria-checked* and *aria-selected*.</span></span>

- <span data-ttu-id="d3ec3-220">*aria-valuenow* - 範囲ウィジェットの現在の値を定義します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-220">*aria-valuenow* - Defines the current value for a range widget.</span></span> <span data-ttu-id="d3ec3-221">関連する *aria-valuetext* を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-221">See related *aria-valuetext*.</span></span>

- <span data-ttu-id="d3ec3-222">*aria-valuetext* - 範囲ウィジェットに *aria-valuenow* の人が判読可能な代替テキストを定義します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-222">*aria-valuetext* - Defines the human readable text alternative of *aria-valuenow* for a range widget.</span></span>

### <a name="controls-could-do-this"></a><span data-ttu-id="d3ec3-223">コントロールが行うことができる操作</span><span class="sxs-lookup"><span data-stu-id="d3ec3-223">Controls could do this</span></span>

#### <a name="indicate-an-expanded-state"></a><span data-ttu-id="d3ec3-224">展開された状態の表示</span><span class="sxs-lookup"><span data-stu-id="d3ec3-224">Indicate an expanded state</span></span>

<span data-ttu-id="d3ec3-225">複雑な相互作用を学習できますが、現在の状態は実験なしでは決して簡単に判断できません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-225">Complex interactions can be learned, but current state isn’t always easy to determine without experimentation.</span></span> <span data-ttu-id="d3ec3-226">*aria-expanded* タグを使用するとき、コントロールがその現在の状態を説明します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-226">When using an *aria-expanded* tag, the control describes its current state.</span></span> <span data-ttu-id="d3ec3-227">例として、コントロールのタブまたはクイック タブ セクションへのタブ移動があります。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-227">An example is tabbing to a tab or FastTab section of a control.</span></span>

- <span data-ttu-id="d3ec3-228">*aria-expanded (状態)* - 要素または別のグループ化されている要素が、現在展開されているか折りたたまれているかを示します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-228">*aria-expanded (state)* - Indicates whether the element, or another grouping element it controls, is currently expanded or collapsed.</span></span>

#### <a name="describe-applicable-context-menu"></a><span data-ttu-id="d3ec3-229">適用できるコンテキスト メニューの説明</span><span class="sxs-lookup"><span data-stu-id="d3ec3-229">Describe applicable context menu</span></span>

<span data-ttu-id="d3ec3-230">Finance and Operations アプリはコンテキスト メニューを提供します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-230">Finance and Operations apps provide a context menu.</span></span> <span data-ttu-id="d3ec3-231">アプリケーション作成者が現在のコントロールまたはコンテキストに機能を提供したときに、ユーザーはその機能を公表することができます。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-231">When the application author has provided functionality to the current control or context, you can announce that functionality.</span></span>

- <span data-ttu-id="d3ec3-232">*aria-haspopup* - 要素にポップアップ コンテキスト メニューまたはサブ レベルのメニューがあることを示します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-232">*aria-haspopup* - Indicates that the element has a pop-up context menu or sub-level menu.</span></span>

### <a name="other-miscellaneous-controls"></a><span data-ttu-id="d3ec3-233">その他のコントロール</span><span class="sxs-lookup"><span data-stu-id="d3ec3-233">Other miscellaneous controls</span></span>

- <span data-ttu-id="d3ec3-234">*aria-live* - 要素が更新されることを示し、ユーザー エージェント、支援テクノロジー、およびユーザーがライブ リージョンから期待できる更新の種類を示します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-234">*aria-live* - Indicates that an element will be updated, and describes the types of updates the user agents, assistive technologies, and user can expect from the live region.</span></span>

- <span data-ttu-id="d3ec3-235">*aria-multiline* - テキスト ボックスが複数行の入力を受け入れるか、一行だけを受け入れるかを示します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-235">*aria-multiline* - Indicates whether a text box accepts multiple lines of input or only a single line.</span></span>

- <span data-ttu-id="d3ec3-236">*aria-multiselectable* - ユーザーが現在選択可能な子孫からひとつ以上の項目を選択できることを示します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-236">*aria-multiselectable* - Indicates that the user may select more than one item from the current selectable descendants.</span></span>

- <span data-ttu-id="d3ec3-237">*aria-orientation* - 要素と方向が水平か垂直かを示します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-237">*aria-orientation* - Indicates whether the element and orientation is horizontal or vertical.</span></span>

- <span data-ttu-id="d3ec3-238">*aria-setsize* - 現在の listitems および treeitem のセット内の項目の数を定義します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-238">*aria-setsize* - Defines the number of items in the current set of listitems or treeitems.</span></span> <span data-ttu-id="d3ec3-239">セット内のすべての要素が DOM にある場合は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-239">Not required if all elements in the set are present in the DOM.</span></span> <span data-ttu-id="d3ec3-240">関連する *aria-posinset* を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-240">See related *aria-posinset*.</span></span>

- <span data-ttu-id="d3ec3-241">*aria-sort* - テーブルまたはグリッド内の項目を昇順または降順でソートするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-241">*aria-sort* - Indicates if items in a table or grid are sorted in ascending or descending order.</span></span>

- <span data-ttu-id="d3ec3-242">*aria-valuemax* - 範囲ウィジェットの最大許容値を定義します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-242">*aria-valuemax* - Defines the maximum allowed value for a range widget.</span></span>

- <span data-ttu-id="d3ec3-243">*aria-valuemin* - 範囲ウィジェットの最小許容値を定義します。</span><span class="sxs-lookup"><span data-stu-id="d3ec3-243">*aria-valuemin* - Defines the minimum allowed value for a range widget.</span></span>
