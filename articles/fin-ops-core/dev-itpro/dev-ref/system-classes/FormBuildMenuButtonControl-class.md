---
title: FormBuildMenuButtonControl クラス
description: このトピックでは、FormBuildMenuButtonControl クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7f89a68ed1f9eef812f008d5018461a6d6371ae
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502963"
---
# <a name="class-formbuildmenubuttoncontrol"></a><span data-ttu-id="b3ab7-103">クラス FormBuildMenuButtonControl</span><span class="sxs-lookup"><span data-stu-id="b3ab7-103">Class FormBuildMenuButtonControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildMenuButtonControl extends FormBuildControl
```

<span data-ttu-id="b3ab7-104">FormBuildMenuButtonControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-104">The FormBuildMenuButtonControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3ab7-105">備考</span><span class="sxs-lookup"><span data-stu-id="b3ab7-105">Remarks</span></span>

<span data-ttu-id="b3ab7-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="b3ab7-107">例</span><span class="sxs-lookup"><span data-stu-id="b3ab7-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="b3ab7-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="b3ab7-108">Methods</span></span>

| <span data-ttu-id="b3ab7-109">方法</span><span class="sxs-lookup"><span data-stu-id="b3ab7-109">Method</span></span>                                                                                                      | <span data-ttu-id="b3ab7-110">説明</span><span class="sxs-lookup"><span data-stu-id="b3ab7-110">Description</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ab7-111">public int acquireFocus(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-111">public int acquireFocus(\[int value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="b3ab7-112">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-112">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="b3ab7-113">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-113">Determines whether to align the control.</span></span>                                                                                                      |
| <span data-ttu-id="b3ab7-114">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-114">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                               |
| <span data-ttu-id="b3ab7-115">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-115">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="b3ab7-116">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-116">Determines whether the user can change the contents of the control.</span></span>                                                                           |
| <span data-ttu-id="b3ab7-117">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-117">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="b3ab7-118">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-118">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                            |
| <span data-ttu-id="b3ab7-119">public boolean autoRefreshData(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-119">public boolean autoRefreshData(\[boolean value\])</span></span>                                                           |                                                                                                                                               |
| <span data-ttu-id="b3ab7-120">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-120">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="b3ab7-121">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-121">Gets or sets the background color of the control.</span></span>                                                                                             |
| <span data-ttu-id="b3ab7-122">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-122">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="b3ab7-123">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-123">Determines whether the control background can be transparent.</span></span>                                                                                 |
| <span data-ttu-id="b3ab7-124">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-124">public boolean big(\[boolean value\])</span></span>                                                                       |                                                                                                                                               |
| <span data-ttu-id="b3ab7-125">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-125">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="b3ab7-126">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-126">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                                   |
| <span data-ttu-id="b3ab7-127">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-127">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="b3ab7-128">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-128">Gets or sets the style of the borderline of the control.</span></span>                                                                                      |
| <span data-ttu-id="b3ab7-129">public int bottomMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-129">public int bottomMargin(\[int value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="b3ab7-130">public int buttonDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-130">public int buttonDisplay(\[int value\])</span></span>                                                                     | <span data-ttu-id="b3ab7-131">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-131">Gets or sets the appearance of the button control.</span></span>                                                                                            |
| <span data-ttu-id="b3ab7-132">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-132">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="b3ab7-133">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-133">Gets or sets the character set of the font.</span></span>                                                                                                   |
| <span data-ttu-id="b3ab7-134">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-134">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="b3ab7-135">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-135">Gets or sets the color scheme of the control.</span></span>                                                                                                 |
| <span data-ttu-id="b3ab7-136">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-136">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="b3ab7-137">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-137">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                           |
| <span data-ttu-id="b3ab7-138">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="b3ab7-138">public int containerId()</span></span>                                                                                    | <span data-ttu-id="b3ab7-139">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-139">Retrieves the ID of the parent container for the control.</span></span>                                                                                     |
| <span data-ttu-id="b3ab7-140">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-140">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                               |
| <span data-ttu-id="b3ab7-141">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-141">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="b3ab7-142">public boolean defaultButton(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-142">public boolean defaultButton(\[boolean value\])</span></span>                                                             | <span data-ttu-id="b3ab7-143">ボタンをフォーム上の既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-143">Determines whether the button should be the default button on the form.</span></span>                                                                       |
| <span data-ttu-id="b3ab7-144">public str disabledImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-144">public str disabledImage(\[str value\])</span></span>                                                                     | <span data-ttu-id="b3ab7-145">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-145">Gets or sets the disabled image of the button.</span></span>                                                                                                |
| <span data-ttu-id="b3ab7-146">public int disabledImageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-146">public int disabledImageLocation(\[int value\])</span></span>                                                             |                                                                                                                                               |
| <span data-ttu-id="b3ab7-147">public int disabledResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-147">public int disabledResource(\[int value\])</span></span>                                                                  | <span data-ttu-id="b3ab7-148">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-148">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>                                                                |
| <span data-ttu-id="b3ab7-149">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-149">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="b3ab7-150">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-150">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="b3ab7-151">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-151">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                             |
| <span data-ttu-id="b3ab7-152">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-152">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="b3ab7-153">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-153">Determines whether to enable or disable the object.</span></span>                                                                                           |
| <span data-ttu-id="b3ab7-154">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-154">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="b3ab7-155">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-155">Gets or sets the name of the font for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="b3ab7-156">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-156">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="b3ab7-157">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-157">Gets or sets the size of the font for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="b3ab7-158">public boolean forcedToOverflow(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-158">public boolean forcedToOverflow(\[boolean value\])</span></span>                                                          |                                                                                                                                               |
| <span data-ttu-id="b3ab7-159">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-159">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="b3ab7-160">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-160">Gets or sets the text color for the control to use.</span></span>                                                                                           |
| <span data-ttu-id="b3ab7-161">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-161">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="b3ab7-162">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-162">Gets or sets the height of the control.</span></span>                                                                                                       |
| <span data-ttu-id="b3ab7-163">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-163">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="b3ab7-164">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-164">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                |
| <span data-ttu-id="b3ab7-165">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-165">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="b3ab7-166">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-166">Gets or sets the height of the control.</span></span>                                                                                                       |
| <span data-ttu-id="b3ab7-167">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-167">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="b3ab7-168">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-168">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="b3ab7-169">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-169">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="b3ab7-170">public int id()</span><span class="sxs-lookup"><span data-stu-id="b3ab7-170">public int id()</span></span>                                                                                             | <span data-ttu-id="b3ab7-171">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-171">Retrieves the ID of the control.</span></span>                                                                                                              |
| <span data-ttu-id="b3ab7-172">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-172">public int imageLocation(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="b3ab7-173">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="b3ab7-173">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="b3ab7-174">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-174">Retrieves a value that indicates whether the control is a container control.</span></span>                                                                  |
| <span data-ttu-id="b3ab7-175">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-175">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="b3ab7-176">public str keyTip(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-176">public str keyTip(\[str value\])</span></span>                                                                            |                                                                                                                                               |
| <span data-ttu-id="b3ab7-177">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-177">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="b3ab7-178">public int leftMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-178">public int leftMargin(\[int value\])</span></span>                                                                        |                                                                                                                                               |
| <span data-ttu-id="b3ab7-179">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-179">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="b3ab7-180">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-180">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                               |
| <span data-ttu-id="b3ab7-181">public int moveControl(int controlId, \[int insertAfterControlId\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-181">public int moveControl(int controlId, \[int insertAfterControlId\])</span></span>                                         | <span data-ttu-id="b3ab7-182">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-182">Moves a specified control to the control.</span></span>                                                                                                     |
| <span data-ttu-id="b3ab7-183">public int multiSelect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-183">public int multiSelect(\[int value\])</span></span>                                                                       |                                                                                                                                               |
| <span data-ttu-id="b3ab7-184">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-184">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="b3ab7-185">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-185">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="b3ab7-186">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-186">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="b3ab7-187">public int needsRecord(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-187">public int needsRecord(\[int value\])</span></span>                                                                       |                                                                                                                                               |
| <span data-ttu-id="b3ab7-188">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-188">public str normalImage(\[str value\])</span></span>                                                                       |                                                                                                                                               |
| <span data-ttu-id="b3ab7-189">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-189">public int normalResource(\[int value\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="b3ab7-190">public boolean primary(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-190">public boolean primary(\[boolean value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="b3ab7-191">public int rightMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-191">public int rightMargin(\[int value\])</span></span>                                                                       |                                                                                                                                               |
| <span data-ttu-id="b3ab7-192">public boolean saveRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-192">public boolean saveRecord(\[boolean value\])</span></span>                                                                |                                                                                                                                               |
| <span data-ttu-id="b3ab7-193">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-193">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                               |
| <span data-ttu-id="b3ab7-194">public int shortkey(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-194">public int shortkey(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="b3ab7-195">public boolean showShortCut(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-195">public boolean showShortCut(\[boolean value\])</span></span>                                                              |                                                                                                                                               |
| <span data-ttu-id="b3ab7-196">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-196">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="b3ab7-197">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-197">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>               |
| <span data-ttu-id="b3ab7-198">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-198">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                               |
| <span data-ttu-id="b3ab7-199">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-199">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                               |
| <span data-ttu-id="b3ab7-200">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-200">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="b3ab7-201">public int topMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-201">public int topMargin(\[int value\])</span></span>                                                                         |                                                                                                                                               |
| <span data-ttu-id="b3ab7-202">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-202">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                               |
| <span data-ttu-id="b3ab7-203">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-203">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="b3ab7-204">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-204">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                               |
| <span data-ttu-id="b3ab7-205">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-205">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="b3ab7-206">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-206">Sets or returns the underline property for the text in the control.</span></span>                                                                           |
| <span data-ttu-id="b3ab7-207">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-207">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="b3ab7-208">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-208">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="b3ab7-209">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-209">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="b3ab7-210">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-210">public boolean useUserLayout(\[boolean value\])</span></span>                                                             |                                                                                                                                               |
| <span data-ttu-id="b3ab7-211">public boolean value(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-211">public boolean value(\[boolean value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="b3ab7-212">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-212">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                               |
| <span data-ttu-id="b3ab7-213">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-213">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                               |
| <span data-ttu-id="b3ab7-214">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-214">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                               |
| <span data-ttu-id="b3ab7-215">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-215">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="b3ab7-216">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-216">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="b3ab7-217">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-217">Gets or sets the width of the control.</span></span>                                                                                                        |
| <span data-ttu-id="b3ab7-218">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-218">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="b3ab7-219">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-219">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                |
| <span data-ttu-id="b3ab7-220">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-220">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="b3ab7-221">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-221">Gets or sets the width of the control.</span></span>                                                                                                        |
| <span data-ttu-id="b3ab7-222">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="b3ab7-222">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                               |

## <a name="method-acquirefocus"></a><span data-ttu-id="b3ab7-223">メソッド acquireFocus</span><span class="sxs-lookup"><span data-stu-id="b3ab7-223">Method acquireFocus</span></span>

```xpp
public int acquireFocus([int value])
```

### <a name="parameters---acquirefocus"></a><span data-ttu-id="b3ab7-224">パラメーター - acquireFocus</span><span class="sxs-lookup"><span data-stu-id="b3ab7-224">Parameters - acquireFocus</span></span>

<span data-ttu-id="b3ab7-225">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-225">value</span></span>  

### <a name="return-value---acquirefocus"></a><span data-ttu-id="b3ab7-226">戻り値 - acquireFocus</span><span class="sxs-lookup"><span data-stu-id="b3ab7-226">Return Value - acquireFocus</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="b3ab7-227">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="b3ab7-227">Method alignControl</span></span>

<span data-ttu-id="b3ab7-228">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-228">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="b3ab7-229">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="b3ab7-229">Parameters - alignControl</span></span>

<span data-ttu-id="b3ab7-230">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-230">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="b3ab7-231">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="b3ab7-231">Return Value - alignControl</span></span>

<span data-ttu-id="b3ab7-232">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-232">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="b3ab7-233">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="b3ab7-233">Remarks - alignControl</span></span>

<span data-ttu-id="b3ab7-234">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-234">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="b3ab7-235">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="b3ab7-235">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="b3ab7-236">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="b3ab7-236">Parameters - alignment</span></span>

<span data-ttu-id="b3ab7-237">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-237">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="b3ab7-238">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="b3ab7-238">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="b3ab7-239">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="b3ab7-239">Method allowEdit</span></span>

<span data-ttu-id="b3ab7-240">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-240">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="b3ab7-241">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="b3ab7-241">Parameters - allowEdit</span></span>

<span data-ttu-id="b3ab7-242">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-242">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="b3ab7-243">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="b3ab7-243">Return Value - allowEdit</span></span>

<span data-ttu-id="b3ab7-244">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-244">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="b3ab7-245">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="b3ab7-245">Remarks - allowEdit</span></span>

<span data-ttu-id="b3ab7-246">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-246">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="b3ab7-247">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b3ab7-247">Method autoDeclaration</span></span>

<span data-ttu-id="b3ab7-248">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-248">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="b3ab7-249">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b3ab7-249">Parameters - autoDeclaration</span></span>

<span data-ttu-id="b3ab7-250">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-250">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="b3ab7-251">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b3ab7-251">Return Value - autoDeclaration</span></span>

<span data-ttu-id="b3ab7-252">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-252">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="b3ab7-253">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b3ab7-253">Remarks - autoDeclaration</span></span>

<span data-ttu-id="b3ab7-254">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-254">Controls cannot have identical names.</span></span>

## <a name="method-autorefreshdata"></a><span data-ttu-id="b3ab7-255">メソッド autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="b3ab7-255">Method autoRefreshData</span></span>

```xpp
public boolean autoRefreshData([boolean value])
```

### <a name="parameters---autorefreshdata"></a><span data-ttu-id="b3ab7-256">パラメーター - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="b3ab7-256">Parameters - autoRefreshData</span></span>

<span data-ttu-id="b3ab7-257">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-257">value</span></span>  

### <a name="return-value---autorefreshdata"></a><span data-ttu-id="b3ab7-258">戻り値 - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="b3ab7-258">Return Value - autoRefreshData</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="b3ab7-259">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b3ab7-259">Method backgroundColor</span></span>

<span data-ttu-id="b3ab7-260">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-260">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="b3ab7-261">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b3ab7-261">Parameters - backgroundColor</span></span>

<span data-ttu-id="b3ab7-262">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-262">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="b3ab7-263">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b3ab7-263">Return Value - backgroundColor</span></span>

<span data-ttu-id="b3ab7-264">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-264">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="b3ab7-265">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b3ab7-265">Remarks - backgroundColor</span></span>

<span data-ttu-id="b3ab7-266">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-266">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="b3ab7-267">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-267">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="b3ab7-268">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-268">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="b3ab7-269">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-269">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="b3ab7-270">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-270">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="b3ab7-271">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-271">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="b3ab7-272">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="b3ab7-272">Method backStyle</span></span>

<span data-ttu-id="b3ab7-273">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-273">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="b3ab7-274">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="b3ab7-274">Parameters - backStyle</span></span>

<span data-ttu-id="b3ab7-275">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-275">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="b3ab7-276">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="b3ab7-276">Return Value - backStyle</span></span>

<span data-ttu-id="b3ab7-277">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-277">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-big"></a><span data-ttu-id="b3ab7-278">メソッド big</span><span class="sxs-lookup"><span data-stu-id="b3ab7-278">Method big</span></span>

```xpp
public boolean big([boolean value])
```

### <a name="parameters---big"></a><span data-ttu-id="b3ab7-279">パラメーター - big</span><span class="sxs-lookup"><span data-stu-id="b3ab7-279">Parameters - big</span></span>

<span data-ttu-id="b3ab7-280">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-280">value</span></span>  

### <a name="return-value---big"></a><span data-ttu-id="b3ab7-281">戻り値 - big</span><span class="sxs-lookup"><span data-stu-id="b3ab7-281">Return Value - big</span></span>

## <a name="method-bold"></a><span data-ttu-id="b3ab7-282">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="b3ab7-282">Method bold</span></span>

<span data-ttu-id="b3ab7-283">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-283">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="b3ab7-284">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="b3ab7-284">Parameters - bold</span></span>

<span data-ttu-id="b3ab7-285">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-285">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="b3ab7-286">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="b3ab7-286">Return Value - bold</span></span>

<span data-ttu-id="b3ab7-287">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-287">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="b3ab7-288">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="b3ab7-288">Remarks - bold</span></span>

<span data-ttu-id="b3ab7-289">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-289">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="b3ab7-290">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-290">0 Use the default font weight.</span></span>
-   <span data-ttu-id="b3ab7-291">1 シン。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-291">1 Thin.</span></span>
-   <span data-ttu-id="b3ab7-292">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-292">2 Extra-light.</span></span>
-   <span data-ttu-id="b3ab7-293">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-293">3 Light.</span></span>
-   <span data-ttu-id="b3ab7-294">4 標準。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-294">4 Normal.</span></span>
-   <span data-ttu-id="b3ab7-295">5 中。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-295">5 Medium.</span></span>
-   <span data-ttu-id="b3ab7-296">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-296">6 Semibold.</span></span>
-   <span data-ttu-id="b3ab7-297">7 太字。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-297">7 Bold.</span></span>
-   <span data-ttu-id="b3ab7-298">8 極太。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-298">8 Extra-bold.</span></span>
-   <span data-ttu-id="b3ab7-299">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-299">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="b3ab7-300">メソッド border</span><span class="sxs-lookup"><span data-stu-id="b3ab7-300">Method border</span></span>

<span data-ttu-id="b3ab7-301">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-301">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="b3ab7-302">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="b3ab7-302">Parameters - border</span></span>

<span data-ttu-id="b3ab7-303">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-303">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="b3ab7-304">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="b3ab7-304">Return Value - border</span></span>

<span data-ttu-id="b3ab7-305">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-305">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="b3ab7-306">備考 - border</span><span class="sxs-lookup"><span data-stu-id="b3ab7-306">Remarks - border</span></span>

<span data-ttu-id="b3ab7-307">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-307">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="b3ab7-308">値です。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-308">Value.</span></span> | <span data-ttu-id="b3ab7-309">説明。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-309">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="b3ab7-310">0</span><span class="sxs-lookup"><span data-stu-id="b3ab7-310">0</span></span>      | <span data-ttu-id="b3ab7-311">自動。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-311">Auto.</span></span>        |
| <span data-ttu-id="b3ab7-312">1</span><span class="sxs-lookup"><span data-stu-id="b3ab7-312">1</span></span>      | <span data-ttu-id="b3ab7-313">3D。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-313">3D.</span></span>          |
| <span data-ttu-id="b3ab7-314">2</span><span class="sxs-lookup"><span data-stu-id="b3ab7-314">2</span></span>      | <span data-ttu-id="b3ab7-315">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-315">Single line.</span></span> |
| <span data-ttu-id="b3ab7-316">3</span><span class="sxs-lookup"><span data-stu-id="b3ab7-316">3</span></span>      | <span data-ttu-id="b3ab7-317">均一。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-317">Flat.</span></span>        |
| <span data-ttu-id="b3ab7-318">4</span><span class="sxs-lookup"><span data-stu-id="b3ab7-318">4</span></span>      | <span data-ttu-id="b3ab7-319">なし。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-319">None.</span></span>        |

## <a name="method-bottommargin"></a><span data-ttu-id="b3ab7-320">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="b3ab7-320">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="b3ab7-321">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="b3ab7-321">Parameters - bottomMargin</span></span>

<span data-ttu-id="b3ab7-322">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-322">value</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="b3ab7-323">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="b3ab7-323">Return Value - bottomMargin</span></span>

## <a name="method-buttondisplay"></a><span data-ttu-id="b3ab7-324">メソッド buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="b3ab7-324">Method buttonDisplay</span></span>

<span data-ttu-id="b3ab7-325">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-325">Gets or sets the appearance of the button control.</span></span>

```xpp
public int buttonDisplay([int value])
```

### <a name="parameters---buttondisplay"></a><span data-ttu-id="b3ab7-326">パラメーター - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="b3ab7-326">Parameters - buttonDisplay</span></span>

<span data-ttu-id="b3ab7-327">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-327">value</span></span>  

### <a name="return-value---buttondisplay"></a><span data-ttu-id="b3ab7-328">戻り値 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="b3ab7-328">Return Value - buttonDisplay</span></span>

<span data-ttu-id="b3ab7-329">ゼロから 5 までの整数。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-329">An integer between zero and five, inclusive.</span></span>

### <a name="remarks---buttondisplay"></a><span data-ttu-id="b3ab7-330">備考 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="b3ab7-330">Remarks - buttonDisplay</span></span>

<span data-ttu-id="b3ab7-331">プロパティ値は、テキスト、画像、またはその両方のいずれをボタンに表示するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-331">The value of the property defines whether the text, the image, or both should be displayed on the button.</span></span> <span data-ttu-id="b3ab7-332">このプロパティは、テキストと画像の両方が表示されている場合は、テキストと画像の相対位置も制御します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-332">This property also controls relative positions of text and image if both are displayed.</span></span> <span data-ttu-id="b3ab7-333">返される整数値には、次のようなボタン コントロールの外観が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-333">The integer value that is returned contains the appearance of the button control as follows:</span></span>

| <span data-ttu-id="b3ab7-334">値です。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-334">Value.</span></span> | <span data-ttu-id="b3ab7-335">説明。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-335">Description.</span></span>                                                     |
|--------|------------------------------------------------------------------|
| <span data-ttu-id="b3ab7-336">0</span><span class="sxs-lookup"><span data-stu-id="b3ab7-336">0</span></span>      | <span data-ttu-id="b3ab7-337">テキストのみ。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-337">Text only.</span></span>                                                       |
| <span data-ttu-id="b3ab7-338">1</span><span class="sxs-lookup"><span data-stu-id="b3ab7-338">1</span></span>      | <span data-ttu-id="b3ab7-339">イメージのみ。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-339">Image Only.</span></span>                                                      |
| <span data-ttu-id="b3ab7-340">2</span><span class="sxs-lookup"><span data-stu-id="b3ab7-340">2</span></span>      | <span data-ttu-id="b3ab7-341">テキストと画像。画像はテキストの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-341">Text and image; the image is displayed under the text.</span></span>           |
| <span data-ttu-id="b3ab7-342">3</span><span class="sxs-lookup"><span data-stu-id="b3ab7-342">3</span></span>      | <span data-ttu-id="b3ab7-343">テキストと画像。画像はテキストの上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-343">Text and image; the image is displayed above the text.</span></span>           |
| <span data-ttu-id="b3ab7-344">4</span><span class="sxs-lookup"><span data-stu-id="b3ab7-344">4</span></span>      | <span data-ttu-id="b3ab7-345">テキストと画像。画像はテキストの左に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-345">Text and image; the image is displayed to the left of the text.</span></span>  |
| <span data-ttu-id="b3ab7-346">5</span><span class="sxs-lookup"><span data-stu-id="b3ab7-346">5</span></span>      | <span data-ttu-id="b3ab7-347">テキストと画像。画像はテキストの右に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-347">Text and image; the image is displayed to the right of the text.</span></span> |

## <a name="method-characterset"></a><span data-ttu-id="b3ab7-348">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="b3ab7-348">Method characterSet</span></span>

<span data-ttu-id="b3ab7-349">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-349">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="b3ab7-350">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="b3ab7-350">Parameters - characterSet</span></span>

<span data-ttu-id="b3ab7-351">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-351">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="b3ab7-352">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="b3ab7-352">Return Value - characterSet</span></span>

<span data-ttu-id="b3ab7-353">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-353">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="b3ab7-354">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="b3ab7-354">Remarks - characterSet</span></span>

<span data-ttu-id="b3ab7-355">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-355">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="b3ab7-356">値です。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-356">Value.</span></span> | <span data-ttu-id="b3ab7-357">説明。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-357">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="b3ab7-358">0</span><span class="sxs-lookup"><span data-stu-id="b3ab7-358">0</span></span>      | <span data-ttu-id="b3ab7-359">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b3ab7-359">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="b3ab7-360">1</span><span class="sxs-lookup"><span data-stu-id="b3ab7-360">1</span></span>      | <span data-ttu-id="b3ab7-361">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b3ab7-361">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="b3ab7-362">2</span><span class="sxs-lookup"><span data-stu-id="b3ab7-362">2</span></span>      | <span data-ttu-id="b3ab7-363">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b3ab7-363">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="b3ab7-364">77</span><span class="sxs-lookup"><span data-stu-id="b3ab7-364">77</span></span>     | <span data-ttu-id="b3ab7-365">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b3ab7-365">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="b3ab7-366">128</span><span class="sxs-lookup"><span data-stu-id="b3ab7-366">128</span></span>    | <span data-ttu-id="b3ab7-367">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b3ab7-367">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="b3ab7-368">129</span><span class="sxs-lookup"><span data-stu-id="b3ab7-368">129</span></span>    | <span data-ttu-id="b3ab7-369">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b3ab7-369">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="b3ab7-370">134</span><span class="sxs-lookup"><span data-stu-id="b3ab7-370">134</span></span>    | <span data-ttu-id="b3ab7-371">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b3ab7-371">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="b3ab7-372">136</span><span class="sxs-lookup"><span data-stu-id="b3ab7-372">136</span></span>    | <span data-ttu-id="b3ab7-373">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b3ab7-373">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="b3ab7-374">161</span><span class="sxs-lookup"><span data-stu-id="b3ab7-374">161</span></span>    | <span data-ttu-id="b3ab7-375">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b3ab7-375">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="b3ab7-376">162</span><span class="sxs-lookup"><span data-stu-id="b3ab7-376">162</span></span>    | <span data-ttu-id="b3ab7-377">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b3ab7-377">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="b3ab7-378">163</span><span class="sxs-lookup"><span data-stu-id="b3ab7-378">163</span></span>    | <span data-ttu-id="b3ab7-379">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b3ab7-379">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="b3ab7-380">186</span><span class="sxs-lookup"><span data-stu-id="b3ab7-380">186</span></span>    | <span data-ttu-id="b3ab7-381">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b3ab7-381">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="b3ab7-382">204</span><span class="sxs-lookup"><span data-stu-id="b3ab7-382">204</span></span>    | <span data-ttu-id="b3ab7-383">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b3ab7-383">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="b3ab7-384">238</span><span class="sxs-lookup"><span data-stu-id="b3ab7-384">238</span></span>    | <span data-ttu-id="b3ab7-385">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b3ab7-385">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="b3ab7-386">255</span><span class="sxs-lookup"><span data-stu-id="b3ab7-386">255</span></span>    | <span data-ttu-id="b3ab7-387">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b3ab7-387">OEM\_CHARSET</span></span>         |

<span data-ttu-id="b3ab7-388">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-388">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="b3ab7-389">値です。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-389">Value.</span></span> | <span data-ttu-id="b3ab7-390">説明。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-390">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="b3ab7-391">130</span><span class="sxs-lookup"><span data-stu-id="b3ab7-391">130</span></span>    | <span data-ttu-id="b3ab7-392">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b3ab7-392">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="b3ab7-393">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-393">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="b3ab7-394">値です。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-394">Value.</span></span> | <span data-ttu-id="b3ab7-395">説明。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-395">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="b3ab7-396">177</span><span class="sxs-lookup"><span data-stu-id="b3ab7-396">177</span></span>    | <span data-ttu-id="b3ab7-397">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b3ab7-397">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="b3ab7-398">178</span><span class="sxs-lookup"><span data-stu-id="b3ab7-398">178</span></span>    | <span data-ttu-id="b3ab7-399">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b3ab7-399">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="b3ab7-400">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-400">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="b3ab7-401">値です。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-401">Value.</span></span> | <span data-ttu-id="b3ab7-402">説明。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-402">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="b3ab7-403">222</span><span class="sxs-lookup"><span data-stu-id="b3ab7-403">222</span></span>    | <span data-ttu-id="b3ab7-404">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b3ab7-404">THAI\_CHARSET</span></span> |

<span data-ttu-id="b3ab7-405">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-405">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="b3ab7-406">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-406">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="b3ab7-407">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-407">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="b3ab7-408">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="b3ab7-408">Method colorScheme</span></span>

<span data-ttu-id="b3ab7-409">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-409">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="b3ab7-410">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="b3ab7-410">Parameters - colorScheme</span></span>

<span data-ttu-id="b3ab7-411">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-411">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="b3ab7-412">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="b3ab7-412">Return Value - colorScheme</span></span>

<span data-ttu-id="b3ab7-413">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-413">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="b3ab7-414">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="b3ab7-414">Remarks - colorScheme</span></span>

<span data-ttu-id="b3ab7-415">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-415">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="b3ab7-416">値です。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-416">Value.</span></span> | <span data-ttu-id="b3ab7-417">スタイル。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-417">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="b3ab7-418">0</span><span class="sxs-lookup"><span data-stu-id="b3ab7-418">0</span></span>      | <span data-ttu-id="b3ab7-419">既定。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-419">Default.</span></span>                      |
| <span data-ttu-id="b3ab7-420">1</span><span class="sxs-lookup"><span data-stu-id="b3ab7-420">1</span></span>      | <span data-ttu-id="b3ab7-421">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-421">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="b3ab7-422">2</span><span class="sxs-lookup"><span data-stu-id="b3ab7-422">2</span></span>      | <span data-ttu-id="b3ab7-423">真の配色。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-423">The true-color scheme.</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="b3ab7-424">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="b3ab7-424">Method configurationKey</span></span>

<span data-ttu-id="b3ab7-425">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-425">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="b3ab7-426">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="b3ab7-426">Parameters - configurationKey</span></span>

<span data-ttu-id="b3ab7-427">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-427">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="b3ab7-428">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="b3ab7-428">Return Value - configurationKey</span></span>

<span data-ttu-id="b3ab7-429">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-429">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="b3ab7-430">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="b3ab7-430">Remarks - configurationKey</span></span>

<span data-ttu-id="b3ab7-431">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-431">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="b3ab7-432">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-432">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="b3ab7-433">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="b3ab7-433">Method containerId</span></span>

<span data-ttu-id="b3ab7-434">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-434">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="b3ab7-435">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="b3ab7-435">Return Value - containerId</span></span>

<span data-ttu-id="b3ab7-436">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-436">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="b3ab7-437">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="b3ab7-437">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="b3ab7-438">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="b3ab7-438">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="b3ab7-439">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-439">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="b3ab7-440">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="b3ab7-440">Return Value - countryRegionCodes</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="b3ab7-441">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="b3ab7-441">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="b3ab7-442">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="b3ab7-442">Parameters - dataRelationPath</span></span>

<span data-ttu-id="b3ab7-443">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-443">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="b3ab7-444">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="b3ab7-444">Return Value - dataRelationPath</span></span>

## <a name="method-defaultbutton"></a><span data-ttu-id="b3ab7-445">メソッド defaultButton</span><span class="sxs-lookup"><span data-stu-id="b3ab7-445">Method defaultButton</span></span>

<span data-ttu-id="b3ab7-446">ボタンをフォーム上の既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-446">Determines whether the button should be the default button on the form.</span></span>

```xpp
public boolean defaultButton([boolean value])
```

### <a name="parameters---defaultbutton"></a><span data-ttu-id="b3ab7-447">パラメーター - defaultButton</span><span class="sxs-lookup"><span data-stu-id="b3ab7-447">Parameters - defaultButton</span></span>

<span data-ttu-id="b3ab7-448">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-448">value</span></span>  

### <a name="return-value---defaultbutton"></a><span data-ttu-id="b3ab7-449">戻り値 - defaultButton</span><span class="sxs-lookup"><span data-stu-id="b3ab7-449">Return Value - defaultButton</span></span>

<span data-ttu-id="b3ab7-450">ボタンが既定のボタンである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-450">true if the button should be the default button; otherwise, false.</span></span>

## <a name="method-disabledimage"></a><span data-ttu-id="b3ab7-451">メソッド disabledImage</span><span class="sxs-lookup"><span data-stu-id="b3ab7-451">Method disabledImage</span></span>

<span data-ttu-id="b3ab7-452">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-452">Gets or sets the disabled image of the button.</span></span>

```xpp
public str disabledImage([str value])
```

### <a name="parameters---disabledimage"></a><span data-ttu-id="b3ab7-453">パラメーター - disabledImage</span><span class="sxs-lookup"><span data-stu-id="b3ab7-453">Parameters - disabledImage</span></span>

<span data-ttu-id="b3ab7-454">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-454">value</span></span>  

### <a name="return-value---disabledimage"></a><span data-ttu-id="b3ab7-455">戻り値 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="b3ab7-455">Return Value - disabledImage</span></span>

<span data-ttu-id="b3ab7-456">画像ファイルのフル ネーム。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-456">The full name of an image file.</span></span> <span data-ttu-id="b3ab7-457">システムは、GDI でサポートされているすべてのイメージ形式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-457">The system supports all of the GDI-supported image formats.</span></span>

### <a name="remarks---disabledimage"></a><span data-ttu-id="b3ab7-458">備考 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="b3ab7-458">Remarks - disabledImage</span></span>

<span data-ttu-id="b3ab7-459">このプロパティは、disabledResource プロパティに優先します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-459">This property has precedence over the disabledResource property .</span></span> <span data-ttu-id="b3ab7-460">これらのプロパティの両方が設定されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-460">It is used if both of these properties are set.</span></span>

## <a name="method-disabledimagelocation"></a><span data-ttu-id="b3ab7-461">メソッド disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="b3ab7-461">Method disabledImageLocation</span></span>

```xpp
public int disabledImageLocation([int value])
```

### <a name="parameters---disabledimagelocation"></a><span data-ttu-id="b3ab7-462">パラメーター - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="b3ab7-462">Parameters - disabledImageLocation</span></span>

<span data-ttu-id="b3ab7-463">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-463">value</span></span>  

### <a name="return-value---disabledimagelocation"></a><span data-ttu-id="b3ab7-464">戻り値 - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="b3ab7-464">Return Value - disabledImageLocation</span></span>

## <a name="method-disabledresource"></a><span data-ttu-id="b3ab7-465">メソッド disabledResource</span><span class="sxs-lookup"><span data-stu-id="b3ab7-465">Method disabledResource</span></span>

<span data-ttu-id="b3ab7-466">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-466">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>

```xpp
public int disabledResource([int value])
```

### <a name="parameters---disabledresource"></a><span data-ttu-id="b3ab7-467">パラメーター - disabledResource</span><span class="sxs-lookup"><span data-stu-id="b3ab7-467">Parameters - disabledResource</span></span>

<span data-ttu-id="b3ab7-468">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-468">value</span></span>  

### <a name="return-value---disabledresource"></a><span data-ttu-id="b3ab7-469">戻り値 - disabledResource</span><span class="sxs-lookup"><span data-stu-id="b3ab7-469">Return Value - disabledResource</span></span>

<span data-ttu-id="b3ab7-470">無効なボタン画像として使用する画像リソース ID。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-470">The resource ID of the image to use as the disabled button image.</span></span> <span data-ttu-id="b3ab7-471">アイコンとビットマップ イメージの両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-471">Both icon and bitmap images are supported.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="b3ab7-472">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="b3ab7-472">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="b3ab7-473">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="b3ab7-473">Parameters - displayTarget</span></span>

<span data-ttu-id="b3ab7-474">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-474">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="b3ab7-475">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="b3ab7-475">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="b3ab7-476">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="b3ab7-476">Method dragDrop</span></span>

<span data-ttu-id="b3ab7-477">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-477">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="b3ab7-478">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="b3ab7-478">Parameters - dragDrop</span></span>

<span data-ttu-id="b3ab7-479">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-479">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="b3ab7-480">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="b3ab7-480">Return Value - dragDrop</span></span>

<span data-ttu-id="b3ab7-481">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-481">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="b3ab7-482">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="b3ab7-482">Method enabled</span></span>

<span data-ttu-id="b3ab7-483">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-483">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="b3ab7-484">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="b3ab7-484">Parameters - enabled</span></span>

<span data-ttu-id="b3ab7-485">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-485">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="b3ab7-486">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="b3ab7-486">Return Value - enabled</span></span>

<span data-ttu-id="b3ab7-487">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-487">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="b3ab7-488">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="b3ab7-488">Remarks - enabled</span></span>

<span data-ttu-id="b3ab7-489">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-489">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="b3ab7-490">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-490">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="b3ab7-491">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-491">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="b3ab7-492">メソッド font</span><span class="sxs-lookup"><span data-stu-id="b3ab7-492">Method font</span></span>

<span data-ttu-id="b3ab7-493">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-493">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="b3ab7-494">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="b3ab7-494">Parameters - font</span></span>

<span data-ttu-id="b3ab7-495">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-495">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="b3ab7-496">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="b3ab7-496">Return Value - font</span></span>

<span data-ttu-id="b3ab7-497">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-497">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="b3ab7-498">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="b3ab7-498">Method fontSize</span></span>

<span data-ttu-id="b3ab7-499">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-499">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="b3ab7-500">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="b3ab7-500">Parameters - fontSize</span></span>

<span data-ttu-id="b3ab7-501">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-501">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="b3ab7-502">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="b3ab7-502">Return Value - fontSize</span></span>

<span data-ttu-id="b3ab7-503">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-503">The height of the font in points.</span></span>

## <a name="method-forcedtooverflow"></a><span data-ttu-id="b3ab7-504">メソッド forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="b3ab7-504">Method forcedToOverflow</span></span>

```xpp
public boolean forcedToOverflow([boolean value])
```

### <a name="parameters---forcedtooverflow"></a><span data-ttu-id="b3ab7-505">パラメーター - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="b3ab7-505">Parameters - forcedToOverflow</span></span>

<span data-ttu-id="b3ab7-506">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-506">value</span></span>  

### <a name="return-value---forcedtooverflow"></a><span data-ttu-id="b3ab7-507">戻り値 - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="b3ab7-507">Return Value - forcedToOverflow</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="b3ab7-508">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="b3ab7-508">Method foregroundColor</span></span>

<span data-ttu-id="b3ab7-509">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-509">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="b3ab7-510">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="b3ab7-510">Parameters - foregroundColor</span></span>

<span data-ttu-id="b3ab7-511">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-511">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="b3ab7-512">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="b3ab7-512">Return Value - foregroundColor</span></span>

<span data-ttu-id="b3ab7-513">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-513">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="b3ab7-514">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="b3ab7-514">Remarks - foregroundColor</span></span>

<span data-ttu-id="b3ab7-515">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-515">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="b3ab7-516">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-516">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="b3ab7-517">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-517">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="b3ab7-518">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-518">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="b3ab7-519">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-519">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="b3ab7-520">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-520">The maximum value for a single byte is 255.</span></span>

## <a name="method-height"></a><span data-ttu-id="b3ab7-521">メソッド height</span><span class="sxs-lookup"><span data-stu-id="b3ab7-521">Method height</span></span>

<span data-ttu-id="b3ab7-522">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-522">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="b3ab7-523">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="b3ab7-523">Parameters - height</span></span>

<span data-ttu-id="b3ab7-524">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-524">value</span></span>  

<!-- -->

<span data-ttu-id="b3ab7-525">モード</span><span class="sxs-lookup"><span data-stu-id="b3ab7-525">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="b3ab7-526">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="b3ab7-526">Return Value - height</span></span>

<span data-ttu-id="b3ab7-527">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-527">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="b3ab7-528">備考 - height</span><span class="sxs-lookup"><span data-stu-id="b3ab7-528">Remarks - height</span></span>

<span data-ttu-id="b3ab7-529">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-529">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="b3ab7-530">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="b3ab7-530">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="b3ab7-531">モード。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-531">Mode.</span></span>            | <span data-ttu-id="b3ab7-532">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-532">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ab7-533">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-533">-1 Exact.</span></span>        | <span data-ttu-id="b3ab7-534">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-534">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b3ab7-535">0 自動。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-535">0 Auto.</span></span>          | <span data-ttu-id="b3ab7-536">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-536">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b3ab7-537">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-537">1 Column height.</span></span> | <span data-ttu-id="b3ab7-538">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-538">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="b3ab7-539">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-539">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="b3ab7-540">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="b3ab7-540">Method heightMode</span></span>

<span data-ttu-id="b3ab7-541">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-541">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="b3ab7-542">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="b3ab7-542">Parameters - heightMode</span></span>

<span data-ttu-id="b3ab7-543">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-543">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="b3ab7-544">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="b3ab7-544">Return Value - heightMode</span></span>

<span data-ttu-id="b3ab7-545">計算モード。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-545">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="b3ab7-546">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="b3ab7-546">Remarks - heightMode</span></span>

<span data-ttu-id="b3ab7-547">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="b3ab7-547">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="b3ab7-548">モード。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-548">Mode.</span></span>          | <span data-ttu-id="b3ab7-549">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-549">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ab7-550">正確。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-550">Exact.</span></span>         | <span data-ttu-id="b3ab7-551">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-551">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b3ab7-552">自動。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-552">Auto.</span></span>          | <span data-ttu-id="b3ab7-553">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-553">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b3ab7-554">列の高さ</span><span class="sxs-lookup"><span data-stu-id="b3ab7-554">Column height.</span></span> | <span data-ttu-id="b3ab7-555">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-555">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="b3ab7-556">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-556">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="b3ab7-557">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="b3ab7-557">Method heightValue</span></span>

<span data-ttu-id="b3ab7-558">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-558">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="b3ab7-559">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="b3ab7-559">Parameters - heightValue</span></span>

<span data-ttu-id="b3ab7-560">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-560">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="b3ab7-561">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="b3ab7-561">Return Value - heightValue</span></span>

<span data-ttu-id="b3ab7-562">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-562">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="b3ab7-563">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="b3ab7-563">Remarks - heightValue</span></span>

<span data-ttu-id="b3ab7-564">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-564">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="b3ab7-565">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="b3ab7-565">Method helpText</span></span>

<span data-ttu-id="b3ab7-566">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-566">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="b3ab7-567">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="b3ab7-567">Parameters - helpText</span></span>

<span data-ttu-id="b3ab7-568">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-568">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="b3ab7-569">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="b3ab7-569">Return Value - helpText</span></span>

<span data-ttu-id="b3ab7-570">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-570">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="b3ab7-571">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="b3ab7-571">Remarks - helpText</span></span>

<span data-ttu-id="b3ab7-572">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-572">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="b3ab7-573">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-573">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="b3ab7-574">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="b3ab7-574">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="b3ab7-575">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="b3ab7-575">Parameters - hierarchyParent</span></span>

<span data-ttu-id="b3ab7-576">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-576">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="b3ab7-577">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="b3ab7-577">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="b3ab7-578">メソッド id</span><span class="sxs-lookup"><span data-stu-id="b3ab7-578">Method id</span></span>

<span data-ttu-id="b3ab7-579">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-579">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="b3ab7-580">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="b3ab7-580">Return Value - id</span></span>

<span data-ttu-id="b3ab7-581">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-581">The ID of the control.</span></span>

## <a name="method-imagelocation"></a><span data-ttu-id="b3ab7-582">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="b3ab7-582">Method imageLocation</span></span>

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a><span data-ttu-id="b3ab7-583">パラメーター - imageLocation</span><span class="sxs-lookup"><span data-stu-id="b3ab7-583">Parameters - imageLocation</span></span>

<span data-ttu-id="b3ab7-584">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-584">value</span></span>  

### <a name="return-value---imagelocation"></a><span data-ttu-id="b3ab7-585">戻り値 - imageLocation</span><span class="sxs-lookup"><span data-stu-id="b3ab7-585">Return Value - imageLocation</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="b3ab7-586">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="b3ab7-586">Method isContainer</span></span>

<span data-ttu-id="b3ab7-587">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-587">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="b3ab7-588">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="b3ab7-588">Return Value - isContainer</span></span>

<span data-ttu-id="b3ab7-589">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-589">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="b3ab7-590">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="b3ab7-590">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="b3ab7-591">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="b3ab7-591">Parameters - italic</span></span>

<span data-ttu-id="b3ab7-592">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-592">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="b3ab7-593">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="b3ab7-593">Return Value - italic</span></span>

## <a name="method-keytip"></a><span data-ttu-id="b3ab7-594">メソッド keyTip</span><span class="sxs-lookup"><span data-stu-id="b3ab7-594">Method keyTip</span></span>

```xpp
public str keyTip([str value])
```

### <a name="parameters---keytip"></a><span data-ttu-id="b3ab7-595">パラメーター - keyTip</span><span class="sxs-lookup"><span data-stu-id="b3ab7-595">Parameters - keyTip</span></span>

<span data-ttu-id="b3ab7-596">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-596">value</span></span>  

### <a name="return-value---keytip"></a><span data-ttu-id="b3ab7-597">戻り値 - keyTip</span><span class="sxs-lookup"><span data-stu-id="b3ab7-597">Return Value - keyTip</span></span>

## <a name="method-left"></a><span data-ttu-id="b3ab7-598">メソッド left</span><span class="sxs-lookup"><span data-stu-id="b3ab7-598">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="b3ab7-599">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="b3ab7-599">Parameters - left</span></span>

<span data-ttu-id="b3ab7-600">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-600">value</span></span>  

<!-- -->

<span data-ttu-id="b3ab7-601">モード</span><span class="sxs-lookup"><span data-stu-id="b3ab7-601">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="b3ab7-602">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="b3ab7-602">Return Value - left</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="b3ab7-603">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="b3ab7-603">Method leftMargin</span></span>

```xpp
public int leftMargin([int value])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="b3ab7-604">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="b3ab7-604">Parameters - leftMargin</span></span>

<span data-ttu-id="b3ab7-605">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-605">value</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="b3ab7-606">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="b3ab7-606">Return Value - leftMargin</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="b3ab7-607">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="b3ab7-607">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="b3ab7-608">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="b3ab7-608">Parameters - leftMode</span></span>

<span data-ttu-id="b3ab7-609">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-609">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="b3ab7-610">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="b3ab7-610">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="b3ab7-611">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="b3ab7-611">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="b3ab7-612">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="b3ab7-612">Parameters - leftValue</span></span>

<span data-ttu-id="b3ab7-613">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-613">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="b3ab7-614">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="b3ab7-614">Return Value - leftValue</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="b3ab7-615">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="b3ab7-615">Method moveControl</span></span>

<span data-ttu-id="b3ab7-616">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-616">Moves a specified control to the control.</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterControlId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="b3ab7-617">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="b3ab7-617">Parameters - moveControl</span></span>

<span data-ttu-id="b3ab7-618">controlId</span><span class="sxs-lookup"><span data-stu-id="b3ab7-618">controlId</span></span>  

<!-- -->

<span data-ttu-id="b3ab7-619">insertAfterControlId</span><span class="sxs-lookup"><span data-stu-id="b3ab7-619">insertAfterControlId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="b3ab7-620">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="b3ab7-620">Return Value - moveControl</span></span>

<span data-ttu-id="b3ab7-621">コントロールが正常に移動した場合は 1、それ以外の場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-621">1 if the control was moved successfully; otherwise, 0.</span></span>

### <a name="remarks---movecontrol"></a><span data-ttu-id="b3ab7-622">備考 - moveControl</span><span class="sxs-lookup"><span data-stu-id="b3ab7-622">Remarks - moveControl</span></span>

<span data-ttu-id="b3ab7-623">一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-623">In general, if the specified control can be contained in the control and can be moved from the container that it is currently in, this method should succeed.</span></span> <span data-ttu-id="b3ab7-624">ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-624">However, in some cases, such as for the reference group control instance, controls cannot be moved.</span></span>

## <a name="method-multiselect"></a><span data-ttu-id="b3ab7-625">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="b3ab7-625">Method multiSelect</span></span>

```xpp
public int multiSelect([int value])
```

### <a name="parameters---multiselect"></a><span data-ttu-id="b3ab7-626">パラメーター - multiSelect</span><span class="sxs-lookup"><span data-stu-id="b3ab7-626">Parameters - multiSelect</span></span>

<span data-ttu-id="b3ab7-627">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-627">value</span></span>  

### <a name="return-value---multiselect"></a><span data-ttu-id="b3ab7-628">戻り値 - multiSelect</span><span class="sxs-lookup"><span data-stu-id="b3ab7-628">Return Value - multiSelect</span></span>

## <a name="method-name"></a><span data-ttu-id="b3ab7-629">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b3ab7-629">Method name</span></span>

<span data-ttu-id="b3ab7-630">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-630">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="b3ab7-631">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="b3ab7-631">Parameters - name</span></span>

<span data-ttu-id="b3ab7-632">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-632">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="b3ab7-633">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="b3ab7-633">Return Value - name</span></span>

<span data-ttu-id="b3ab7-634">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-634">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="b3ab7-635">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="b3ab7-635">Remarks - name</span></span>

<span data-ttu-id="b3ab7-636">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-636">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="b3ab7-637">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-637">Begins with a letter.</span></span>
-   <span data-ttu-id="b3ab7-638">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-638">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="b3ab7-639">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-639">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="b3ab7-640">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-640">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="b3ab7-641">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-641">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="b3ab7-642">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="b3ab7-642">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="b3ab7-643">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="b3ab7-643">Parameters - neededPermission</span></span>

<span data-ttu-id="b3ab7-644">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-644">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="b3ab7-645">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="b3ab7-645">Return Value - neededPermission</span></span>

## <a name="method-needsrecord"></a><span data-ttu-id="b3ab7-646">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="b3ab7-646">Method needsRecord</span></span>

```xpp
public int needsRecord([int value])
```

### <a name="parameters---needsrecord"></a><span data-ttu-id="b3ab7-647">パラメーター - needsRecord</span><span class="sxs-lookup"><span data-stu-id="b3ab7-647">Parameters - needsRecord</span></span>

<span data-ttu-id="b3ab7-648">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-648">value</span></span>  

### <a name="return-value---needsrecord"></a><span data-ttu-id="b3ab7-649">戻り値 - needsRecord</span><span class="sxs-lookup"><span data-stu-id="b3ab7-649">Return Value - needsRecord</span></span>

## <a name="method-normalimage"></a><span data-ttu-id="b3ab7-650">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="b3ab7-650">Method normalImage</span></span>

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a><span data-ttu-id="b3ab7-651">パラメーター - normalImage</span><span class="sxs-lookup"><span data-stu-id="b3ab7-651">Parameters - normalImage</span></span>

<span data-ttu-id="b3ab7-652">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-652">value</span></span>  

### <a name="return-value---normalimage"></a><span data-ttu-id="b3ab7-653">戻り値 - normalImage</span><span class="sxs-lookup"><span data-stu-id="b3ab7-653">Return Value - normalImage</span></span>

## <a name="method-normalresource"></a><span data-ttu-id="b3ab7-654">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="b3ab7-654">Method normalResource</span></span>

```xpp
public int normalResource([int value])
```

### <a name="parameters---normalresource"></a><span data-ttu-id="b3ab7-655">パラメーター - normalResource</span><span class="sxs-lookup"><span data-stu-id="b3ab7-655">Parameters - normalResource</span></span>

<span data-ttu-id="b3ab7-656">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-656">value</span></span>  

### <a name="return-value---normalresource"></a><span data-ttu-id="b3ab7-657">戻り値 - normalResource</span><span class="sxs-lookup"><span data-stu-id="b3ab7-657">Return Value - normalResource</span></span>

## <a name="method-primary"></a><span data-ttu-id="b3ab7-658">メソッド primary</span><span class="sxs-lookup"><span data-stu-id="b3ab7-658">Method primary</span></span>

```xpp
public boolean primary([boolean value])
```

### <a name="parameters---primary"></a><span data-ttu-id="b3ab7-659">パラメーター - primary</span><span class="sxs-lookup"><span data-stu-id="b3ab7-659">Parameters - primary</span></span>

<span data-ttu-id="b3ab7-660">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-660">value</span></span>  

### <a name="return-value---primary"></a><span data-ttu-id="b3ab7-661">戻り値 - primary</span><span class="sxs-lookup"><span data-stu-id="b3ab7-661">Return Value - primary</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="b3ab7-662">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="b3ab7-662">Method rightMargin</span></span>

```xpp
public int rightMargin([int value])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="b3ab7-663">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="b3ab7-663">Parameters - rightMargin</span></span>

<span data-ttu-id="b3ab7-664">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-664">value</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="b3ab7-665">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="b3ab7-665">Return Value - rightMargin</span></span>

## <a name="method-saverecord"></a><span data-ttu-id="b3ab7-666">メソッド saveRecord</span><span class="sxs-lookup"><span data-stu-id="b3ab7-666">Method saveRecord</span></span>

```xpp
public boolean saveRecord([boolean value])
```

### <a name="parameters---saverecord"></a><span data-ttu-id="b3ab7-667">パラメーター - saveRecord</span><span class="sxs-lookup"><span data-stu-id="b3ab7-667">Parameters - saveRecord</span></span>

<span data-ttu-id="b3ab7-668">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-668">value</span></span>  

### <a name="return-value---saverecord"></a><span data-ttu-id="b3ab7-669">戻り値 - saveRecord</span><span class="sxs-lookup"><span data-stu-id="b3ab7-669">Return Value - saveRecord</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="b3ab7-670">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="b3ab7-670">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="b3ab7-671">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="b3ab7-671">Parameters - securityKey</span></span>

<span data-ttu-id="b3ab7-672">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-672">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="b3ab7-673">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="b3ab7-673">Return Value - securityKey</span></span>

## <a name="method-shortkey"></a><span data-ttu-id="b3ab7-674">メソッド shortkey</span><span class="sxs-lookup"><span data-stu-id="b3ab7-674">Method shortkey</span></span>

```xpp
public int shortkey([int value])
```

### <a name="parameters---shortkey"></a><span data-ttu-id="b3ab7-675">パラメーター - shortkey</span><span class="sxs-lookup"><span data-stu-id="b3ab7-675">Parameters - shortkey</span></span>

<span data-ttu-id="b3ab7-676">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-676">value</span></span>  

### <a name="return-value---shortkey"></a><span data-ttu-id="b3ab7-677">戻り値 - shortkey</span><span class="sxs-lookup"><span data-stu-id="b3ab7-677">Return Value - shortkey</span></span>

## <a name="method-showshortcut"></a><span data-ttu-id="b3ab7-678">メソッド showShortCut</span><span class="sxs-lookup"><span data-stu-id="b3ab7-678">Method showShortCut</span></span>

```xpp
public boolean showShortCut([boolean value])
```

### <a name="parameters---showshortcut"></a><span data-ttu-id="b3ab7-679">パラメーター - showShortCut</span><span class="sxs-lookup"><span data-stu-id="b3ab7-679">Parameters - showShortCut</span></span>

<span data-ttu-id="b3ab7-680">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-680">value</span></span>  

### <a name="return-value---showshortcut"></a><span data-ttu-id="b3ab7-681">戻り値 - showShortCut</span><span class="sxs-lookup"><span data-stu-id="b3ab7-681">Return Value - showShortCut</span></span>

## <a name="method-skip"></a><span data-ttu-id="b3ab7-682">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="b3ab7-682">Method skip</span></span>

<span data-ttu-id="b3ab7-683">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-683">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="b3ab7-684">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="b3ab7-684">Parameters - skip</span></span>

<span data-ttu-id="b3ab7-685">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-685">value</span></span>  
<span data-ttu-id="b3ab7-686">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-686">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="b3ab7-687">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="b3ab7-687">Return Value - skip</span></span>

<span data-ttu-id="b3ab7-688">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-688">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-style"></a><span data-ttu-id="b3ab7-689">メソッド style</span><span class="sxs-lookup"><span data-stu-id="b3ab7-689">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="b3ab7-690">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="b3ab7-690">Parameters - style</span></span>

<span data-ttu-id="b3ab7-691">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-691">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="b3ab7-692">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="b3ab7-692">Return Value - style</span></span>

## <a name="method-text"></a><span data-ttu-id="b3ab7-693">メソッド text</span><span class="sxs-lookup"><span data-stu-id="b3ab7-693">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="b3ab7-694">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="b3ab7-694">Parameters - text</span></span>

<span data-ttu-id="b3ab7-695">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-695">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="b3ab7-696">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="b3ab7-696">Return Value - text</span></span>

## <a name="method-top"></a><span data-ttu-id="b3ab7-697">メソッド top</span><span class="sxs-lookup"><span data-stu-id="b3ab7-697">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="b3ab7-698">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="b3ab7-698">Parameters - top</span></span>

<span data-ttu-id="b3ab7-699">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-699">value</span></span>  

<!-- -->

<span data-ttu-id="b3ab7-700">モード</span><span class="sxs-lookup"><span data-stu-id="b3ab7-700">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="b3ab7-701">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="b3ab7-701">Return Value - top</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="b3ab7-702">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="b3ab7-702">Method topMargin</span></span>

```xpp
public int topMargin([int value])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="b3ab7-703">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="b3ab7-703">Parameters - topMargin</span></span>

<span data-ttu-id="b3ab7-704">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-704">value</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="b3ab7-705">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="b3ab7-705">Return Value - topMargin</span></span>

## <a name="method-topmode"></a><span data-ttu-id="b3ab7-706">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="b3ab7-706">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="b3ab7-707">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="b3ab7-707">Parameters - topMode</span></span>

<span data-ttu-id="b3ab7-708">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-708">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="b3ab7-709">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="b3ab7-709">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="b3ab7-710">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="b3ab7-710">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="b3ab7-711">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="b3ab7-711">Parameters - topValue</span></span>

<span data-ttu-id="b3ab7-712">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-712">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="b3ab7-713">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="b3ab7-713">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="b3ab7-714">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="b3ab7-714">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="b3ab7-715">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="b3ab7-715">Parameters - type</span></span>

<span data-ttu-id="b3ab7-716">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-716">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="b3ab7-717">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="b3ab7-717">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="b3ab7-718">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="b3ab7-718">Method underline</span></span>

<span data-ttu-id="b3ab7-719">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-719">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="b3ab7-720">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="b3ab7-720">Parameters - underline</span></span>

<span data-ttu-id="b3ab7-721">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-721">value</span></span>  
<span data-ttu-id="b3ab7-722">コントロールの underline プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-722">The value to assign to the underline property of the control.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="b3ab7-723">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="b3ab7-723">Return Value - underline</span></span>

<span data-ttu-id="b3ab7-724">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-724">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-userdata"></a><span data-ttu-id="b3ab7-725">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="b3ab7-725">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="b3ab7-726">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="b3ab7-726">Parameters - userData</span></span>

<span data-ttu-id="b3ab7-727">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-727">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="b3ab7-728">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="b3ab7-728">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="b3ab7-729">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="b3ab7-729">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="b3ab7-730">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="b3ab7-730">Parameters - userDataItem</span></span>

<span data-ttu-id="b3ab7-731">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-731">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="b3ab7-732">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="b3ab7-732">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="b3ab7-733">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="b3ab7-733">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="b3ab7-734">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="b3ab7-734">Parameters - userDataItems</span></span>

<span data-ttu-id="b3ab7-735">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-735">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="b3ab7-736">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="b3ab7-736">Return Value - userDataItems</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="b3ab7-737">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="b3ab7-737">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="b3ab7-738">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="b3ab7-738">Parameters - useUserLayout</span></span>

<span data-ttu-id="b3ab7-739">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-739">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="b3ab7-740">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="b3ab7-740">Return Value - useUserLayout</span></span>

## <a name="method-value"></a><span data-ttu-id="b3ab7-741">メソッド value</span><span class="sxs-lookup"><span data-stu-id="b3ab7-741">Method value</span></span>

```xpp
public boolean value([boolean value])
```

### <a name="parameters---value"></a><span data-ttu-id="b3ab7-742">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="b3ab7-742">Parameters - value</span></span>

<span data-ttu-id="b3ab7-743">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-743">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="b3ab7-744">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="b3ab7-744">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="b3ab7-745">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="b3ab7-745">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="b3ab7-746">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="b3ab7-746">Parameters - verticalSpacing</span></span>

<span data-ttu-id="b3ab7-747">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-747">value</span></span>  

<!-- -->

<span data-ttu-id="b3ab7-748">モード</span><span class="sxs-lookup"><span data-stu-id="b3ab7-748">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="b3ab7-749">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="b3ab7-749">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="b3ab7-750">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="b3ab7-750">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="b3ab7-751">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="b3ab7-751">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="b3ab7-752">モード</span><span class="sxs-lookup"><span data-stu-id="b3ab7-752">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="b3ab7-753">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="b3ab7-753">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="b3ab7-754">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="b3ab7-754">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="b3ab7-755">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="b3ab7-755">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="b3ab7-756">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-756">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="b3ab7-757">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="b3ab7-757">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="b3ab7-758">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="b3ab7-758">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="b3ab7-759">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="b3ab7-759">Parameters - visible</span></span>

<span data-ttu-id="b3ab7-760">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-760">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="b3ab7-761">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="b3ab7-761">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="b3ab7-762">メソッド width</span><span class="sxs-lookup"><span data-stu-id="b3ab7-762">Method width</span></span>

<span data-ttu-id="b3ab7-763">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-763">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="b3ab7-764">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="b3ab7-764">Parameters - width</span></span>

<span data-ttu-id="b3ab7-765">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-765">value</span></span>  

<!-- -->

<span data-ttu-id="b3ab7-766">モード</span><span class="sxs-lookup"><span data-stu-id="b3ab7-766">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="b3ab7-767">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="b3ab7-767">Return Value - width</span></span>

<span data-ttu-id="b3ab7-768">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-768">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="b3ab7-769">備考 - width</span><span class="sxs-lookup"><span data-stu-id="b3ab7-769">Remarks - width</span></span>

<span data-ttu-id="b3ab7-770">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-770">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="b3ab7-771">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="b3ab7-771">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="b3ab7-772">モード。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-772">Mode.</span></span>           | <span data-ttu-id="b3ab7-773">幅計算。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-773">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ab7-774">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-774">-1 Exact.</span></span>       | <span data-ttu-id="b3ab7-775">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-775">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b3ab7-776">0 自動。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-776">0 Auto.</span></span>         | <span data-ttu-id="b3ab7-777">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-777">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b3ab7-778">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-778">1 Column width.</span></span> | <span data-ttu-id="b3ab7-779">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-779">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="b3ab7-780">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-780">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="b3ab7-781">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="b3ab7-781">Method widthMode</span></span>

<span data-ttu-id="b3ab7-782">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-782">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="b3ab7-783">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="b3ab7-783">Parameters - widthMode</span></span>

<span data-ttu-id="b3ab7-784">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-784">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="b3ab7-785">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="b3ab7-785">Return Value - widthMode</span></span>

<span data-ttu-id="b3ab7-786">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-786">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="b3ab7-787">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="b3ab7-787">Remarks - widthMode</span></span>

<span data-ttu-id="b3ab7-788">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="b3ab7-788">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="b3ab7-789">モード。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-789">Mode.</span></span>         | <span data-ttu-id="b3ab7-790">幅計算。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-790">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ab7-791">正確。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-791">Exact.</span></span>        | <span data-ttu-id="b3ab7-792">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-792">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b3ab7-793">自動。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-793">Auto.</span></span>         | <span data-ttu-id="b3ab7-794">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-794">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b3ab7-795">列の幅。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-795">Column width.</span></span> | <span data-ttu-id="b3ab7-796">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-796">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="b3ab7-797">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-797">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="b3ab7-798">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="b3ab7-798">Method widthValue</span></span>

<span data-ttu-id="b3ab7-799">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-799">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="b3ab7-800">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="b3ab7-800">Parameters - widthValue</span></span>

<span data-ttu-id="b3ab7-801">値</span><span class="sxs-lookup"><span data-stu-id="b3ab7-801">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="b3ab7-802">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="b3ab7-802">Return Value - widthValue</span></span>

<span data-ttu-id="b3ab7-803">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-803">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="b3ab7-804">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="b3ab7-804">Remarks - widthValue</span></span>

<span data-ttu-id="b3ab7-805">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="b3ab7-805">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="b3ab7-806">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="b3ab7-806">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="b3ab7-807">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="b3ab7-807">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="b3ab7-808">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="b3ab7-808">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="b3ab7-809">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="b3ab7-809">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="b3ab7-810">overrideObject</span><span class="sxs-lookup"><span data-stu-id="b3ab7-810">overrideObject</span></span>  

