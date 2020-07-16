---
title: FormBuildTreeControl クラス
description: このトピックでは、FormBuildTreeControl クラスについて説明します。
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
ms.openlocfilehash: 324e4a307332ad30996894292008cf15a96aa4b4
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502635"
---
# <a name="class-formbuildtreecontrol"></a><span data-ttu-id="3f57c-103">クラス FormBuildTreeControl</span><span class="sxs-lookup"><span data-stu-id="3f57c-103">Class FormBuildTreeControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildTreeControl extends FormBuildControl
```

<span data-ttu-id="3f57c-104">FormBuildTreeControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-104">The FormBuildTreeControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f57c-105">備考</span><span class="sxs-lookup"><span data-stu-id="3f57c-105">Remarks</span></span>

<span data-ttu-id="3f57c-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="3f57c-107">例</span><span class="sxs-lookup"><span data-stu-id="3f57c-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="3f57c-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="3f57c-108">Methods</span></span>

| <span data-ttu-id="3f57c-109">方法</span><span class="sxs-lookup"><span data-stu-id="3f57c-109">Method</span></span>                                                                                                      | <span data-ttu-id="3f57c-110">説明</span><span class="sxs-lookup"><span data-stu-id="3f57c-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f57c-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="3f57c-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-112">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="3f57c-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="3f57c-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-114">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="3f57c-115">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-115">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="3f57c-116">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-116">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="3f57c-117">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-117">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="3f57c-118">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-118">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="3f57c-119">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-119">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="3f57c-120">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-120">Determines whether the control background can be transparent.</span></span>                                                                           |
| <span data-ttu-id="3f57c-121">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-121">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="3f57c-122">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-122">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                             |
| <span data-ttu-id="3f57c-123">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-123">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="3f57c-124">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-124">Gets or sets the style of the borderline of the control.</span></span>                                                                                |
| <span data-ttu-id="3f57c-125">public boolean canScroll(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-125">public boolean canScroll(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="3f57c-126">public boolean cascadeSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-126">public boolean cascadeSelect(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="3f57c-127">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-127">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="3f57c-128">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-128">Gets or sets the character set of the font.</span></span>                                                                                             |
| <span data-ttu-id="3f57c-129">public boolean checkBox(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-129">public boolean checkBox(\[boolean value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="3f57c-130">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-130">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="3f57c-131">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-131">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="3f57c-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="3f57c-133">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-133">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="3f57c-134">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="3f57c-134">public int containerId()</span></span>                                                                                    | <span data-ttu-id="3f57c-135">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-135">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="3f57c-136">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-136">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="3f57c-137">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-137">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="3f57c-138">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-138">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="3f57c-139">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-139">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="3f57c-140">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-140">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="3f57c-141">public boolean editLabels(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-141">public boolean editLabels(\[boolean value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="3f57c-142">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-142">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="3f57c-143">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-143">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="3f57c-144">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-144">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="3f57c-145">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-145">Gets or sets the name of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="3f57c-146">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-146">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="3f57c-147">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-147">Gets or sets the size of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="3f57c-148">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-148">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="3f57c-149">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-149">Gets or sets the text color for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="3f57c-150">public boolean hasButtons(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-150">public boolean hasButtons(\[boolean value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="3f57c-151">public boolean hasLines(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-151">public boolean hasLines(\[boolean value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="3f57c-152">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-152">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="3f57c-153">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-153">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="3f57c-154">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-154">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="3f57c-155">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-155">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="3f57c-156">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-156">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="3f57c-157">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-157">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="3f57c-158">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-158">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="3f57c-159">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-159">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="3f57c-160">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-160">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="3f57c-161">public int id()</span><span class="sxs-lookup"><span data-stu-id="3f57c-161">public int id()</span></span>                                                                                             | <span data-ttu-id="3f57c-162">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-162">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="3f57c-163">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="3f57c-163">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="3f57c-164">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-164">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="3f57c-165">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-165">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="3f57c-166">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-166">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="3f57c-167">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-167">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="3f57c-168">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-168">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="3f57c-169">public boolean linesAtRoot(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-169">public boolean linesAtRoot(\[boolean value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="3f57c-170">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-170">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="3f57c-171">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-171">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="3f57c-172">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-172">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="3f57c-173">public boolean rowSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-173">public boolean rowSelect(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="3f57c-174">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-174">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="3f57c-175">public boolean showSelAlways(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-175">public boolean showSelAlways(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="3f57c-176">public boolean singleSelection(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-176">public boolean singleSelection(\[boolean value\])</span></span>                                                           |                                                                                                                                         |
| <span data-ttu-id="3f57c-177">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-177">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="3f57c-178">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-178">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="3f57c-179">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-179">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="3f57c-180">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-180">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="3f57c-181">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-181">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="3f57c-182">public boolean trackSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-182">public boolean trackSelect(\[boolean value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="3f57c-183">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-183">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="3f57c-184">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-184">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="3f57c-185">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-185">Sets or returns the underline property for the text in the control.</span></span>                                                                     |
| <span data-ttu-id="3f57c-186">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-186">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="3f57c-187">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-187">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="3f57c-188">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-188">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="3f57c-189">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-189">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="3f57c-190">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-190">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="3f57c-191">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-191">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="3f57c-192">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-192">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="3f57c-193">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-193">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="3f57c-194">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-194">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="3f57c-195">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-195">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="3f57c-196">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-196">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="3f57c-197">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-197">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="3f57c-198">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-198">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="3f57c-199">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="3f57c-199">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="3f57c-200">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="3f57c-200">Method alignControl</span></span>

<span data-ttu-id="3f57c-201">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-201">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="3f57c-202">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="3f57c-202">Parameters - alignControl</span></span>

<span data-ttu-id="3f57c-203">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-203">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="3f57c-204">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="3f57c-204">Return Value - alignControl</span></span>

<span data-ttu-id="3f57c-205">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="3f57c-205">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="3f57c-206">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="3f57c-206">Remarks - alignControl</span></span>

<span data-ttu-id="3f57c-207">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-207">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="3f57c-208">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="3f57c-208">Method allowEdit</span></span>

<span data-ttu-id="3f57c-209">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-209">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="3f57c-210">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="3f57c-210">Parameters - allowEdit</span></span>

<span data-ttu-id="3f57c-211">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-211">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="3f57c-212">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="3f57c-212">Return Value - allowEdit</span></span>

<span data-ttu-id="3f57c-213">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3f57c-213">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="3f57c-214">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="3f57c-214">Remarks - allowEdit</span></span>

<span data-ttu-id="3f57c-215">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="3f57c-215">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="3f57c-216">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="3f57c-216">Method autoDeclaration</span></span>

<span data-ttu-id="3f57c-217">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-217">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="3f57c-218">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="3f57c-218">Parameters - autoDeclaration</span></span>

<span data-ttu-id="3f57c-219">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-219">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="3f57c-220">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="3f57c-220">Return Value - autoDeclaration</span></span>

<span data-ttu-id="3f57c-221">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3f57c-221">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="3f57c-222">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="3f57c-222">Remarks - autoDeclaration</span></span>

<span data-ttu-id="3f57c-223">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="3f57c-223">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="3f57c-224">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="3f57c-224">Method backgroundColor</span></span>

<span data-ttu-id="3f57c-225">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-225">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="3f57c-226">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="3f57c-226">Parameters - backgroundColor</span></span>

<span data-ttu-id="3f57c-227">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-227">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="3f57c-228">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="3f57c-228">Return Value - backgroundColor</span></span>

<span data-ttu-id="3f57c-229">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="3f57c-229">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="3f57c-230">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="3f57c-230">Remarks - backgroundColor</span></span>

<span data-ttu-id="3f57c-231">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-231">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="3f57c-232">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3f57c-232">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="3f57c-233">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="3f57c-233">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="3f57c-234">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="3f57c-234">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="3f57c-235">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="3f57c-235">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="3f57c-236">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="3f57c-236">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="3f57c-237">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="3f57c-237">Method backStyle</span></span>

<span data-ttu-id="3f57c-238">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-238">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="3f57c-239">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="3f57c-239">Parameters - backStyle</span></span>

<span data-ttu-id="3f57c-240">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-240">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="3f57c-241">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="3f57c-241">Return Value - backStyle</span></span>

<span data-ttu-id="3f57c-242">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="3f57c-242">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="3f57c-243">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="3f57c-243">Method bold</span></span>

<span data-ttu-id="3f57c-244">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-244">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="3f57c-245">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="3f57c-245">Parameters - bold</span></span>

<span data-ttu-id="3f57c-246">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-246">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="3f57c-247">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="3f57c-247">Return Value - bold</span></span>

<span data-ttu-id="3f57c-248">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="3f57c-248">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="3f57c-249">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="3f57c-249">Remarks - bold</span></span>

<span data-ttu-id="3f57c-250">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-250">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="3f57c-251">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-251">0 Use the default font weight.</span></span>
-   <span data-ttu-id="3f57c-252">1 シン。</span><span class="sxs-lookup"><span data-stu-id="3f57c-252">1 Thin.</span></span>
-   <span data-ttu-id="3f57c-253">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="3f57c-253">2 Extra-light.</span></span>
-   <span data-ttu-id="3f57c-254">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="3f57c-254">3 Light.</span></span>
-   <span data-ttu-id="3f57c-255">4 標準。</span><span class="sxs-lookup"><span data-stu-id="3f57c-255">4 Normal.</span></span>
-   <span data-ttu-id="3f57c-256">5 中。</span><span class="sxs-lookup"><span data-stu-id="3f57c-256">5 Medium.</span></span>
-   <span data-ttu-id="3f57c-257">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="3f57c-257">6 Semibold.</span></span>
-   <span data-ttu-id="3f57c-258">7 太字。</span><span class="sxs-lookup"><span data-stu-id="3f57c-258">7 Bold.</span></span>
-   <span data-ttu-id="3f57c-259">8 極太。</span><span class="sxs-lookup"><span data-stu-id="3f57c-259">8 Extra-bold.</span></span>
-   <span data-ttu-id="3f57c-260">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="3f57c-260">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="3f57c-261">メソッド border</span><span class="sxs-lookup"><span data-stu-id="3f57c-261">Method border</span></span>

<span data-ttu-id="3f57c-262">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-262">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="3f57c-263">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="3f57c-263">Parameters - border</span></span>

<span data-ttu-id="3f57c-264">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-264">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="3f57c-265">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="3f57c-265">Return Value - border</span></span>

<span data-ttu-id="3f57c-266">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="3f57c-266">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="3f57c-267">備考 - border</span><span class="sxs-lookup"><span data-stu-id="3f57c-267">Remarks - border</span></span>

<span data-ttu-id="3f57c-268">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-268">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="3f57c-269">値です。</span><span class="sxs-lookup"><span data-stu-id="3f57c-269">Value.</span></span> | <span data-ttu-id="3f57c-270">説明。</span><span class="sxs-lookup"><span data-stu-id="3f57c-270">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="3f57c-271">0</span><span class="sxs-lookup"><span data-stu-id="3f57c-271">0</span></span>      | <span data-ttu-id="3f57c-272">自動。</span><span class="sxs-lookup"><span data-stu-id="3f57c-272">Auto.</span></span>        |
| <span data-ttu-id="3f57c-273">1</span><span class="sxs-lookup"><span data-stu-id="3f57c-273">1</span></span>      | <span data-ttu-id="3f57c-274">3D。</span><span class="sxs-lookup"><span data-stu-id="3f57c-274">3D.</span></span>          |
| <span data-ttu-id="3f57c-275">2</span><span class="sxs-lookup"><span data-stu-id="3f57c-275">2</span></span>      | <span data-ttu-id="3f57c-276">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="3f57c-276">Single line.</span></span> |
| <span data-ttu-id="3f57c-277">3</span><span class="sxs-lookup"><span data-stu-id="3f57c-277">3</span></span>      | <span data-ttu-id="3f57c-278">均一。</span><span class="sxs-lookup"><span data-stu-id="3f57c-278">Flat.</span></span>        |
| <span data-ttu-id="3f57c-279">4</span><span class="sxs-lookup"><span data-stu-id="3f57c-279">4</span></span>      | <span data-ttu-id="3f57c-280">なし。</span><span class="sxs-lookup"><span data-stu-id="3f57c-280">None.</span></span>        |

## <a name="method-canscroll"></a><span data-ttu-id="3f57c-281">メソッド canScroll</span><span class="sxs-lookup"><span data-stu-id="3f57c-281">Method canScroll</span></span>

```xpp
public boolean canScroll([boolean value])
```

### <a name="parameters---canscroll"></a><span data-ttu-id="3f57c-282">パラメーター - canScroll</span><span class="sxs-lookup"><span data-stu-id="3f57c-282">Parameters - canScroll</span></span>

<span data-ttu-id="3f57c-283">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-283">value</span></span>  

### <a name="return-value---canscroll"></a><span data-ttu-id="3f57c-284">戻り値 - canScroll</span><span class="sxs-lookup"><span data-stu-id="3f57c-284">Return Value - canScroll</span></span>

## <a name="method-cascadeselect"></a><span data-ttu-id="3f57c-285">メソッド cascadeSelect</span><span class="sxs-lookup"><span data-stu-id="3f57c-285">Method cascadeSelect</span></span>

```xpp
public boolean cascadeSelect([boolean value])
```

### <a name="parameters---cascadeselect"></a><span data-ttu-id="3f57c-286">パラメーター - cascadeSelect</span><span class="sxs-lookup"><span data-stu-id="3f57c-286">Parameters - cascadeSelect</span></span>

<span data-ttu-id="3f57c-287">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-287">value</span></span>  

### <a name="return-value---cascadeselect"></a><span data-ttu-id="3f57c-288">戻り値 - cascadeSelect</span><span class="sxs-lookup"><span data-stu-id="3f57c-288">Return Value - cascadeSelect</span></span>

## <a name="method-characterset"></a><span data-ttu-id="3f57c-289">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="3f57c-289">Method characterSet</span></span>

<span data-ttu-id="3f57c-290">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-290">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="3f57c-291">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="3f57c-291">Parameters - characterSet</span></span>

<span data-ttu-id="3f57c-292">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-292">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="3f57c-293">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="3f57c-293">Return Value - characterSet</span></span>

<span data-ttu-id="3f57c-294">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3f57c-294">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="3f57c-295">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="3f57c-295">Remarks - characterSet</span></span>

<span data-ttu-id="3f57c-296">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-296">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="3f57c-297">値です。</span><span class="sxs-lookup"><span data-stu-id="3f57c-297">Value.</span></span> | <span data-ttu-id="3f57c-298">説明。</span><span class="sxs-lookup"><span data-stu-id="3f57c-298">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="3f57c-299">0</span><span class="sxs-lookup"><span data-stu-id="3f57c-299">0</span></span>      | <span data-ttu-id="3f57c-300">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3f57c-300">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="3f57c-301">1</span><span class="sxs-lookup"><span data-stu-id="3f57c-301">1</span></span>      | <span data-ttu-id="3f57c-302">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3f57c-302">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="3f57c-303">2</span><span class="sxs-lookup"><span data-stu-id="3f57c-303">2</span></span>      | <span data-ttu-id="3f57c-304">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3f57c-304">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="3f57c-305">77</span><span class="sxs-lookup"><span data-stu-id="3f57c-305">77</span></span>     | <span data-ttu-id="3f57c-306">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3f57c-306">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="3f57c-307">128</span><span class="sxs-lookup"><span data-stu-id="3f57c-307">128</span></span>    | <span data-ttu-id="3f57c-308">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3f57c-308">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="3f57c-309">129</span><span class="sxs-lookup"><span data-stu-id="3f57c-309">129</span></span>    | <span data-ttu-id="3f57c-310">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3f57c-310">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="3f57c-311">134</span><span class="sxs-lookup"><span data-stu-id="3f57c-311">134</span></span>    | <span data-ttu-id="3f57c-312">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3f57c-312">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="3f57c-313">136</span><span class="sxs-lookup"><span data-stu-id="3f57c-313">136</span></span>    | <span data-ttu-id="3f57c-314">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3f57c-314">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="3f57c-315">161</span><span class="sxs-lookup"><span data-stu-id="3f57c-315">161</span></span>    | <span data-ttu-id="3f57c-316">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3f57c-316">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="3f57c-317">162</span><span class="sxs-lookup"><span data-stu-id="3f57c-317">162</span></span>    | <span data-ttu-id="3f57c-318">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3f57c-318">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="3f57c-319">163</span><span class="sxs-lookup"><span data-stu-id="3f57c-319">163</span></span>    | <span data-ttu-id="3f57c-320">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3f57c-320">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="3f57c-321">186</span><span class="sxs-lookup"><span data-stu-id="3f57c-321">186</span></span>    | <span data-ttu-id="3f57c-322">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3f57c-322">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="3f57c-323">204</span><span class="sxs-lookup"><span data-stu-id="3f57c-323">204</span></span>    | <span data-ttu-id="3f57c-324">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3f57c-324">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="3f57c-325">238</span><span class="sxs-lookup"><span data-stu-id="3f57c-325">238</span></span>    | <span data-ttu-id="3f57c-326">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3f57c-326">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="3f57c-327">255</span><span class="sxs-lookup"><span data-stu-id="3f57c-327">255</span></span>    | <span data-ttu-id="3f57c-328">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3f57c-328">OEM\_CHARSET</span></span>         |

<span data-ttu-id="3f57c-329">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="3f57c-329">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="3f57c-330">値です。</span><span class="sxs-lookup"><span data-stu-id="3f57c-330">Value.</span></span> | <span data-ttu-id="3f57c-331">説明。</span><span class="sxs-lookup"><span data-stu-id="3f57c-331">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="3f57c-332">130</span><span class="sxs-lookup"><span data-stu-id="3f57c-332">130</span></span>    | <span data-ttu-id="3f57c-333">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3f57c-333">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="3f57c-334">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="3f57c-334">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="3f57c-335">値です。</span><span class="sxs-lookup"><span data-stu-id="3f57c-335">Value.</span></span> | <span data-ttu-id="3f57c-336">説明。</span><span class="sxs-lookup"><span data-stu-id="3f57c-336">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="3f57c-337">177</span><span class="sxs-lookup"><span data-stu-id="3f57c-337">177</span></span>    | <span data-ttu-id="3f57c-338">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3f57c-338">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="3f57c-339">178</span><span class="sxs-lookup"><span data-stu-id="3f57c-339">178</span></span>    | <span data-ttu-id="3f57c-340">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3f57c-340">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="3f57c-341">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="3f57c-341">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="3f57c-342">値です。</span><span class="sxs-lookup"><span data-stu-id="3f57c-342">Value.</span></span> | <span data-ttu-id="3f57c-343">説明。</span><span class="sxs-lookup"><span data-stu-id="3f57c-343">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="3f57c-344">222</span><span class="sxs-lookup"><span data-stu-id="3f57c-344">222</span></span>    | <span data-ttu-id="3f57c-345">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3f57c-345">THAI\_CHARSET</span></span> |

<span data-ttu-id="3f57c-346">既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-346">The default character set is set to values that are based on the current system locale.</span></span> <span data-ttu-id="3f57c-347">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-347">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="3f57c-348">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f57c-348">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-checkbox"></a><span data-ttu-id="3f57c-349">メソッド checkBox</span><span class="sxs-lookup"><span data-stu-id="3f57c-349">Method checkBox</span></span>

```xpp
public boolean checkBox([boolean value])
```

### <a name="parameters---checkbox"></a><span data-ttu-id="3f57c-350">パラメーター - checkBox</span><span class="sxs-lookup"><span data-stu-id="3f57c-350">Parameters - checkBox</span></span>

<span data-ttu-id="3f57c-351">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-351">value</span></span>  

### <a name="return-value---checkbox"></a><span data-ttu-id="3f57c-352">戻り値- checkBox</span><span class="sxs-lookup"><span data-stu-id="3f57c-352">Return Value - checkBox</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="3f57c-353">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="3f57c-353">Method colorScheme</span></span>

<span data-ttu-id="3f57c-354">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-354">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="3f57c-355">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="3f57c-355">Parameters - colorScheme</span></span>

<span data-ttu-id="3f57c-356">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-356">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="3f57c-357">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="3f57c-357">Return Value - colorScheme</span></span>

<span data-ttu-id="3f57c-358">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="3f57c-358">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="3f57c-359">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="3f57c-359">Remarks - colorScheme</span></span>

<span data-ttu-id="3f57c-360">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-360">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="3f57c-361">値です。</span><span class="sxs-lookup"><span data-stu-id="3f57c-361">Value.</span></span> | <span data-ttu-id="3f57c-362">スタイル。</span><span class="sxs-lookup"><span data-stu-id="3f57c-362">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="3f57c-363">0</span><span class="sxs-lookup"><span data-stu-id="3f57c-363">0</span></span>      | <span data-ttu-id="3f57c-364">既定。</span><span class="sxs-lookup"><span data-stu-id="3f57c-364">Default.</span></span>                       |
| <span data-ttu-id="3f57c-365">1</span><span class="sxs-lookup"><span data-stu-id="3f57c-365">1</span></span>      | <span data-ttu-id="3f57c-366">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="3f57c-366">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="3f57c-367">2</span><span class="sxs-lookup"><span data-stu-id="3f57c-367">2</span></span>      | <span data-ttu-id="3f57c-368">真の配色。</span><span class="sxs-lookup"><span data-stu-id="3f57c-368">The true-color scheme.</span></span>         |

## <a name="method-configurationkey"></a><span data-ttu-id="3f57c-369">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="3f57c-369">Method configurationKey</span></span>

<span data-ttu-id="3f57c-370">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-370">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="3f57c-371">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="3f57c-371">Parameters - configurationKey</span></span>

<span data-ttu-id="3f57c-372">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-372">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="3f57c-373">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="3f57c-373">Return Value - configurationKey</span></span>

<span data-ttu-id="3f57c-374">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="3f57c-374">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="3f57c-375">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="3f57c-375">Remarks - configurationKey</span></span>

<span data-ttu-id="3f57c-376">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-376">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="3f57c-377">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="3f57c-377">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="3f57c-378">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="3f57c-378">Method containerId</span></span>

<span data-ttu-id="3f57c-379">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-379">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="3f57c-380">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="3f57c-380">Return Value - containerId</span></span>

<span data-ttu-id="3f57c-381">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="3f57c-381">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="3f57c-382">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="3f57c-382">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="3f57c-383">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="3f57c-383">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="3f57c-384">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-384">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="3f57c-385">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="3f57c-385">Return Value - countryRegionCodes</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="3f57c-386">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="3f57c-386">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="3f57c-387">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="3f57c-387">Parameters - dataRelationPath</span></span>

<span data-ttu-id="3f57c-388">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-388">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="3f57c-389">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="3f57c-389">Return Value - dataRelationPath</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="3f57c-390">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="3f57c-390">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="3f57c-391">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="3f57c-391">Parameters - displayTarget</span></span>

<span data-ttu-id="3f57c-392">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-392">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="3f57c-393">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="3f57c-393">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="3f57c-394">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="3f57c-394">Method dragDrop</span></span>

<span data-ttu-id="3f57c-395">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-395">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="3f57c-396">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="3f57c-396">Parameters - dragDrop</span></span>

<span data-ttu-id="3f57c-397">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-397">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="3f57c-398">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="3f57c-398">Return Value - dragDrop</span></span>

<span data-ttu-id="3f57c-399">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="3f57c-399">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-editlabels"></a><span data-ttu-id="3f57c-400">メソッド editLabels</span><span class="sxs-lookup"><span data-stu-id="3f57c-400">Method editLabels</span></span>

```xpp
public boolean editLabels([boolean value])
```

### <a name="parameters---editlabels"></a><span data-ttu-id="3f57c-401">パラメーター - editLabels</span><span class="sxs-lookup"><span data-stu-id="3f57c-401">Parameters - editLabels</span></span>

<span data-ttu-id="3f57c-402">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-402">value</span></span>  

### <a name="return-value---editlabels"></a><span data-ttu-id="3f57c-403">戻り値 - editLabels</span><span class="sxs-lookup"><span data-stu-id="3f57c-403">Return Value - editLabels</span></span>

## <a name="method-enabled"></a><span data-ttu-id="3f57c-404">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="3f57c-404">Method enabled</span></span>

<span data-ttu-id="3f57c-405">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-405">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="3f57c-406">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="3f57c-406">Parameters - enabled</span></span>

<span data-ttu-id="3f57c-407">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-407">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="3f57c-408">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="3f57c-408">Return Value - enabled</span></span>

<span data-ttu-id="3f57c-409">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3f57c-409">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="3f57c-410">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="3f57c-410">Remarks - enabled</span></span>

<span data-ttu-id="3f57c-411">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-411">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="3f57c-412">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-412">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="3f57c-413">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-413">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="3f57c-414">メソッド font</span><span class="sxs-lookup"><span data-stu-id="3f57c-414">Method font</span></span>

<span data-ttu-id="3f57c-415">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-415">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="3f57c-416">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="3f57c-416">Parameters - font</span></span>

<span data-ttu-id="3f57c-417">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-417">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="3f57c-418">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="3f57c-418">Return Value - font</span></span>

<span data-ttu-id="3f57c-419">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="3f57c-419">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="3f57c-420">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="3f57c-420">Method fontSize</span></span>

<span data-ttu-id="3f57c-421">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-421">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="3f57c-422">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="3f57c-422">Parameters - fontSize</span></span>

<span data-ttu-id="3f57c-423">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-423">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="3f57c-424">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="3f57c-424">Return Value - fontSize</span></span>

<span data-ttu-id="3f57c-425">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="3f57c-425">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="3f57c-426">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="3f57c-426">Method foregroundColor</span></span>

<span data-ttu-id="3f57c-427">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-427">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="3f57c-428">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="3f57c-428">Parameters - foregroundColor</span></span>

<span data-ttu-id="3f57c-429">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-429">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="3f57c-430">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="3f57c-430">Return Value - foregroundColor</span></span>

<span data-ttu-id="3f57c-431">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="3f57c-431">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="3f57c-432">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="3f57c-432">Remarks - foregroundColor</span></span>

<span data-ttu-id="3f57c-433">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-433">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="3f57c-434">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3f57c-434">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="3f57c-435">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="3f57c-435">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="3f57c-436">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="3f57c-436">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="3f57c-437">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="3f57c-437">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="3f57c-438">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="3f57c-438">The maximum value for a single byte is 255.</span></span>

## <a name="method-hasbuttons"></a><span data-ttu-id="3f57c-439">メソッド hasButtons</span><span class="sxs-lookup"><span data-stu-id="3f57c-439">Method hasButtons</span></span>

```xpp
public boolean hasButtons([boolean value])
```

### <a name="parameters---hasbuttons"></a><span data-ttu-id="3f57c-440">パラメーター - hasButtons</span><span class="sxs-lookup"><span data-stu-id="3f57c-440">Parameters - hasButtons</span></span>

<span data-ttu-id="3f57c-441">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-441">value</span></span>  

### <a name="return-value---hasbuttons"></a><span data-ttu-id="3f57c-442">戻り値 - hasButtons</span><span class="sxs-lookup"><span data-stu-id="3f57c-442">Return Value - hasButtons</span></span>

## <a name="method-haslines"></a><span data-ttu-id="3f57c-443">メソッド hasLines</span><span class="sxs-lookup"><span data-stu-id="3f57c-443">Method hasLines</span></span>

```xpp
public boolean hasLines([boolean value])
```

### <a name="parameters---haslines"></a><span data-ttu-id="3f57c-444">パラメーター - hasLines</span><span class="sxs-lookup"><span data-stu-id="3f57c-444">Parameters - hasLines</span></span>

<span data-ttu-id="3f57c-445">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-445">value</span></span>  

### <a name="return-value---haslines"></a><span data-ttu-id="3f57c-446">戻り値 - hasLines</span><span class="sxs-lookup"><span data-stu-id="3f57c-446">Return Value - hasLines</span></span>

## <a name="method-height"></a><span data-ttu-id="3f57c-447">メソッド height</span><span class="sxs-lookup"><span data-stu-id="3f57c-447">Method height</span></span>

<span data-ttu-id="3f57c-448">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-448">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="3f57c-449">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="3f57c-449">Parameters - height</span></span>

<span data-ttu-id="3f57c-450">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-450">value</span></span>  

<!-- -->

<span data-ttu-id="3f57c-451">モード</span><span class="sxs-lookup"><span data-stu-id="3f57c-451">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="3f57c-452">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="3f57c-452">Return Value - height</span></span>

<span data-ttu-id="3f57c-453">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="3f57c-453">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="3f57c-454">備考 - height</span><span class="sxs-lookup"><span data-stu-id="3f57c-454">Remarks - height</span></span>

<span data-ttu-id="3f57c-455">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-455">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="3f57c-456">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="3f57c-456">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="3f57c-457">モード。</span><span class="sxs-lookup"><span data-stu-id="3f57c-457">Mode.</span></span>            | <span data-ttu-id="3f57c-458">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="3f57c-458">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f57c-459">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="3f57c-459">-1 Exact.</span></span>        | <span data-ttu-id="3f57c-460">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-460">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="3f57c-461">0 自動。</span><span class="sxs-lookup"><span data-stu-id="3f57c-461">0 Auto.</span></span>          | <span data-ttu-id="3f57c-462">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-462">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="3f57c-463">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="3f57c-463">1 Column height.</span></span> | <span data-ttu-id="3f57c-464">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="3f57c-464">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="3f57c-465">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-465">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="3f57c-466">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="3f57c-466">Method heightMode</span></span>

<span data-ttu-id="3f57c-467">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-467">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="3f57c-468">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="3f57c-468">Parameters - heightMode</span></span>

<span data-ttu-id="3f57c-469">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-469">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="3f57c-470">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="3f57c-470">Return Value - heightMode</span></span>

<span data-ttu-id="3f57c-471">計算モード。</span><span class="sxs-lookup"><span data-stu-id="3f57c-471">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="3f57c-472">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="3f57c-472">Remarks - heightMode</span></span>

<span data-ttu-id="3f57c-473">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="3f57c-473">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="3f57c-474">モード。</span><span class="sxs-lookup"><span data-stu-id="3f57c-474">Mode.</span></span>          | <span data-ttu-id="3f57c-475">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="3f57c-475">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f57c-476">正確。</span><span class="sxs-lookup"><span data-stu-id="3f57c-476">Exact.</span></span>         | <span data-ttu-id="3f57c-477">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-477">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="3f57c-478">自動。</span><span class="sxs-lookup"><span data-stu-id="3f57c-478">Auto.</span></span>          | <span data-ttu-id="3f57c-479">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-479">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="3f57c-480">列の高さ</span><span class="sxs-lookup"><span data-stu-id="3f57c-480">Column height.</span></span> | <span data-ttu-id="3f57c-481">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="3f57c-481">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="3f57c-482">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="3f57c-482">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="3f57c-483">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="3f57c-483">Method heightValue</span></span>

<span data-ttu-id="3f57c-484">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-484">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="3f57c-485">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="3f57c-485">Parameters - heightValue</span></span>

<span data-ttu-id="3f57c-486">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-486">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="3f57c-487">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="3f57c-487">Return Value - heightValue</span></span>

<span data-ttu-id="3f57c-488">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="3f57c-488">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="3f57c-489">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="3f57c-489">Remarks - heightValue</span></span>

<span data-ttu-id="3f57c-490">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="3f57c-490">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="3f57c-491">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="3f57c-491">Method helpText</span></span>

<span data-ttu-id="3f57c-492">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-492">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="3f57c-493">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="3f57c-493">Parameters - helpText</span></span>

<span data-ttu-id="3f57c-494">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-494">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="3f57c-495">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="3f57c-495">Return Value - helpText</span></span>

<span data-ttu-id="3f57c-496">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="3f57c-496">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="3f57c-497">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="3f57c-497">Remarks - helpText</span></span>

<span data-ttu-id="3f57c-498">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-498">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="3f57c-499">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="3f57c-499">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="3f57c-500">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="3f57c-500">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="3f57c-501">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="3f57c-501">Parameters - hierarchyParent</span></span>

<span data-ttu-id="3f57c-502">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-502">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="3f57c-503">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="3f57c-503">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="3f57c-504">メソッド id</span><span class="sxs-lookup"><span data-stu-id="3f57c-504">Method id</span></span>

<span data-ttu-id="3f57c-505">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-505">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="3f57c-506">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="3f57c-506">Return Value - id</span></span>

<span data-ttu-id="3f57c-507">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="3f57c-507">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="3f57c-508">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="3f57c-508">Method isContainer</span></span>

<span data-ttu-id="3f57c-509">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-509">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="3f57c-510">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="3f57c-510">Return Value - isContainer</span></span>

<span data-ttu-id="3f57c-511">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3f57c-511">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="3f57c-512">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="3f57c-512">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="3f57c-513">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="3f57c-513">Parameters - italic</span></span>

<span data-ttu-id="3f57c-514">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-514">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="3f57c-515">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="3f57c-515">Return Value - italic</span></span>

## <a name="method-left"></a><span data-ttu-id="3f57c-516">メソッド left</span><span class="sxs-lookup"><span data-stu-id="3f57c-516">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="3f57c-517">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="3f57c-517">Parameters - left</span></span>

<span data-ttu-id="3f57c-518">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-518">value</span></span>  

<!-- -->

<span data-ttu-id="3f57c-519">モード</span><span class="sxs-lookup"><span data-stu-id="3f57c-519">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="3f57c-520">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="3f57c-520">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="3f57c-521">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="3f57c-521">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="3f57c-522">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="3f57c-522">Parameters - leftMode</span></span>

<span data-ttu-id="3f57c-523">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-523">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="3f57c-524">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="3f57c-524">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="3f57c-525">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="3f57c-525">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="3f57c-526">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="3f57c-526">Parameters - leftValue</span></span>

<span data-ttu-id="3f57c-527">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-527">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="3f57c-528">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="3f57c-528">Return Value - leftValue</span></span>

## <a name="method-linesatroot"></a><span data-ttu-id="3f57c-529">メソッド linesAtRoot</span><span class="sxs-lookup"><span data-stu-id="3f57c-529">Method linesAtRoot</span></span>

```xpp
public boolean linesAtRoot([boolean value])
```

### <a name="parameters---linesatroot"></a><span data-ttu-id="3f57c-530">パラメーター - linesAtRoot</span><span class="sxs-lookup"><span data-stu-id="3f57c-530">Parameters - linesAtRoot</span></span>

<span data-ttu-id="3f57c-531">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-531">value</span></span>  

### <a name="return-value---linesatroot"></a><span data-ttu-id="3f57c-532">戻り値 - linesAtRoot</span><span class="sxs-lookup"><span data-stu-id="3f57c-532">Return Value - linesAtRoot</span></span>

## <a name="method-name"></a><span data-ttu-id="3f57c-533">メソッド名</span><span class="sxs-lookup"><span data-stu-id="3f57c-533">Method name</span></span>

<span data-ttu-id="3f57c-534">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-534">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="3f57c-535">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="3f57c-535">Parameters - name</span></span>

<span data-ttu-id="3f57c-536">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-536">value</span></span>  
<span data-ttu-id="3f57c-537">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="3f57c-537">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="3f57c-538">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="3f57c-538">Return Value - name</span></span>

<span data-ttu-id="3f57c-539">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="3f57c-539">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="3f57c-540">備考 - name</span><span class="sxs-lookup"><span data-stu-id="3f57c-540">Remarks - name</span></span>

<span data-ttu-id="3f57c-541">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f57c-541">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="3f57c-542">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f57c-542">It must start with a letter.</span></span>
-   <span data-ttu-id="3f57c-543">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="3f57c-543">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="3f57c-544">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-544">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="3f57c-545">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="3f57c-545">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="3f57c-546">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="3f57c-546">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="3f57c-547">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="3f57c-547">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="3f57c-548">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="3f57c-548">Parameters - neededPermission</span></span>

<span data-ttu-id="3f57c-549">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-549">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="3f57c-550">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="3f57c-550">Return Value - neededPermission</span></span>

## <a name="method-rowselect"></a><span data-ttu-id="3f57c-551">メソッド rowSelect</span><span class="sxs-lookup"><span data-stu-id="3f57c-551">Method rowSelect</span></span>

```xpp
public boolean rowSelect([boolean value])
```

### <a name="parameters---rowselect"></a><span data-ttu-id="3f57c-552">パラメーター - rowSelect</span><span class="sxs-lookup"><span data-stu-id="3f57c-552">Parameters - rowSelect</span></span>

<span data-ttu-id="3f57c-553">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-553">value</span></span>  

### <a name="return-value---rowselect"></a><span data-ttu-id="3f57c-554">戻り値 - rowSelect</span><span class="sxs-lookup"><span data-stu-id="3f57c-554">Return Value - rowSelect</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="3f57c-555">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="3f57c-555">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="3f57c-556">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="3f57c-556">Parameters - securityKey</span></span>

<span data-ttu-id="3f57c-557">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-557">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="3f57c-558">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="3f57c-558">Return Value - securityKey</span></span>

## <a name="method-showselalways"></a><span data-ttu-id="3f57c-559">メソッド showSelAlways</span><span class="sxs-lookup"><span data-stu-id="3f57c-559">Method showSelAlways</span></span>

```xpp
public boolean showSelAlways([boolean value])
```

### <a name="parameters---showselalways"></a><span data-ttu-id="3f57c-560">パラメーター - showSelAlways</span><span class="sxs-lookup"><span data-stu-id="3f57c-560">Parameters - showSelAlways</span></span>

<span data-ttu-id="3f57c-561">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-561">value</span></span>  

### <a name="return-value---showselalways"></a><span data-ttu-id="3f57c-562">戻り値 - showSelAlways</span><span class="sxs-lookup"><span data-stu-id="3f57c-562">Return Value - showSelAlways</span></span>

## <a name="method-singleselection"></a><span data-ttu-id="3f57c-563">メソッド singleSelection</span><span class="sxs-lookup"><span data-stu-id="3f57c-563">Method singleSelection</span></span>

```xpp
public boolean singleSelection([boolean value])
```

### <a name="parameters---singleselection"></a><span data-ttu-id="3f57c-564">パラメーター - singleSelection</span><span class="sxs-lookup"><span data-stu-id="3f57c-564">Parameters - singleSelection</span></span>

<span data-ttu-id="3f57c-565">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-565">value</span></span>  

### <a name="return-value---singleselection"></a><span data-ttu-id="3f57c-566">戻り値 - singleSelection</span><span class="sxs-lookup"><span data-stu-id="3f57c-566">Return Value - singleSelection</span></span>

## <a name="method-skip"></a><span data-ttu-id="3f57c-567">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="3f57c-567">Method skip</span></span>

<span data-ttu-id="3f57c-568">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-568">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="3f57c-569">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="3f57c-569">Parameters - skip</span></span>

<span data-ttu-id="3f57c-570">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-570">value</span></span>  
<span data-ttu-id="3f57c-571">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3f57c-571">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="3f57c-572">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="3f57c-572">Return Value - skip</span></span>

<span data-ttu-id="3f57c-573">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3f57c-573">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-top"></a><span data-ttu-id="3f57c-574">メソッド top</span><span class="sxs-lookup"><span data-stu-id="3f57c-574">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="3f57c-575">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="3f57c-575">Parameters - top</span></span>

<span data-ttu-id="3f57c-576">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-576">value</span></span>  

<!-- -->

<span data-ttu-id="3f57c-577">モード</span><span class="sxs-lookup"><span data-stu-id="3f57c-577">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="3f57c-578">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="3f57c-578">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="3f57c-579">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="3f57c-579">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="3f57c-580">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="3f57c-580">Parameters - topMode</span></span>

<span data-ttu-id="3f57c-581">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-581">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="3f57c-582">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="3f57c-582">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="3f57c-583">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="3f57c-583">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="3f57c-584">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="3f57c-584">Parameters - topValue</span></span>

<span data-ttu-id="3f57c-585">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-585">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="3f57c-586">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="3f57c-586">Return Value - topValue</span></span>

## <a name="method-trackselect"></a><span data-ttu-id="3f57c-587">メソッド trackSelect</span><span class="sxs-lookup"><span data-stu-id="3f57c-587">Method trackSelect</span></span>

```xpp
public boolean trackSelect([boolean value])
```

### <a name="parameters---trackselect"></a><span data-ttu-id="3f57c-588">パラメーター - trackSelect</span><span class="sxs-lookup"><span data-stu-id="3f57c-588">Parameters - trackSelect</span></span>

<span data-ttu-id="3f57c-589">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-589">value</span></span>  

### <a name="return-value---trackselect"></a><span data-ttu-id="3f57c-590">戻り値 - trackSelect</span><span class="sxs-lookup"><span data-stu-id="3f57c-590">Return Value - trackSelect</span></span>

## <a name="method-type"></a><span data-ttu-id="3f57c-591">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="3f57c-591">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="3f57c-592">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="3f57c-592">Parameters - type</span></span>

<span data-ttu-id="3f57c-593">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-593">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="3f57c-594">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="3f57c-594">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="3f57c-595">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="3f57c-595">Method underline</span></span>

<span data-ttu-id="3f57c-596">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-596">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="3f57c-597">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="3f57c-597">Parameters - underline</span></span>

<span data-ttu-id="3f57c-598">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-598">value</span></span>  
<span data-ttu-id="3f57c-599">コントロールの underline プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3f57c-599">The value to assign to the underline property of the control; optional.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="3f57c-600">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="3f57c-600">Return Value - underline</span></span>

<span data-ttu-id="3f57c-601">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3f57c-601">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-userdata"></a><span data-ttu-id="3f57c-602">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="3f57c-602">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="3f57c-603">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="3f57c-603">Parameters - userData</span></span>

<span data-ttu-id="3f57c-604">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-604">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="3f57c-605">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="3f57c-605">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="3f57c-606">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="3f57c-606">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="3f57c-607">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="3f57c-607">Parameters - userDataItem</span></span>

<span data-ttu-id="3f57c-608">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-608">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="3f57c-609">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="3f57c-609">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="3f57c-610">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="3f57c-610">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="3f57c-611">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="3f57c-611">Parameters - userDataItems</span></span>

<span data-ttu-id="3f57c-612">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-612">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="3f57c-613">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="3f57c-613">Return Value - userDataItems</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="3f57c-614">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="3f57c-614">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="3f57c-615">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="3f57c-615">Parameters - verticalSpacing</span></span>

<span data-ttu-id="3f57c-616">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-616">value</span></span>  

<!-- -->

<span data-ttu-id="3f57c-617">モード</span><span class="sxs-lookup"><span data-stu-id="3f57c-617">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="3f57c-618">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="3f57c-618">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="3f57c-619">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="3f57c-619">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="3f57c-620">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="3f57c-620">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="3f57c-621">モード</span><span class="sxs-lookup"><span data-stu-id="3f57c-621">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="3f57c-622">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="3f57c-622">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="3f57c-623">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="3f57c-623">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="3f57c-624">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="3f57c-624">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="3f57c-625">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-625">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="3f57c-626">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="3f57c-626">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="3f57c-627">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="3f57c-627">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="3f57c-628">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="3f57c-628">Parameters - visible</span></span>

<span data-ttu-id="3f57c-629">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-629">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="3f57c-630">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="3f57c-630">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="3f57c-631">メソッド width</span><span class="sxs-lookup"><span data-stu-id="3f57c-631">Method width</span></span>

<span data-ttu-id="3f57c-632">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-632">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="3f57c-633">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="3f57c-633">Parameters - width</span></span>

<span data-ttu-id="3f57c-634">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-634">value</span></span>  

<!-- -->

<span data-ttu-id="3f57c-635">モード</span><span class="sxs-lookup"><span data-stu-id="3f57c-635">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="3f57c-636">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="3f57c-636">Return Value - width</span></span>

<span data-ttu-id="3f57c-637">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="3f57c-637">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="3f57c-638">備考 - width</span><span class="sxs-lookup"><span data-stu-id="3f57c-638">Remarks - width</span></span>

<span data-ttu-id="3f57c-639">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-639">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="3f57c-640">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="3f57c-640">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="3f57c-641">モード。</span><span class="sxs-lookup"><span data-stu-id="3f57c-641">Mode.</span></span>           | <span data-ttu-id="3f57c-642">幅計算。</span><span class="sxs-lookup"><span data-stu-id="3f57c-642">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f57c-643">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="3f57c-643">-1 Exact.</span></span>       | <span data-ttu-id="3f57c-644">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-644">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="3f57c-645">0 自動。</span><span class="sxs-lookup"><span data-stu-id="3f57c-645">0 Auto.</span></span>         | <span data-ttu-id="3f57c-646">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-646">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="3f57c-647">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="3f57c-647">1 Column width.</span></span> | <span data-ttu-id="3f57c-648">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="3f57c-648">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="3f57c-649">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-649">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="3f57c-650">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="3f57c-650">Method widthMode</span></span>

<span data-ttu-id="3f57c-651">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-651">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="3f57c-652">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="3f57c-652">Parameters - widthMode</span></span>

<span data-ttu-id="3f57c-653">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-653">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="3f57c-654">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="3f57c-654">Return Value - widthMode</span></span>

<span data-ttu-id="3f57c-655">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3f57c-655">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="3f57c-656">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="3f57c-656">Remarks - widthMode</span></span>

<span data-ttu-id="3f57c-657">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="3f57c-657">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="3f57c-658">モード。</span><span class="sxs-lookup"><span data-stu-id="3f57c-658">Mode.</span></span>         | <span data-ttu-id="3f57c-659">幅計算。</span><span class="sxs-lookup"><span data-stu-id="3f57c-659">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f57c-660">正確。</span><span class="sxs-lookup"><span data-stu-id="3f57c-660">Exact.</span></span>        | <span data-ttu-id="3f57c-661">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-661">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="3f57c-662">自動。</span><span class="sxs-lookup"><span data-stu-id="3f57c-662">Auto.</span></span>         | <span data-ttu-id="3f57c-663">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="3f57c-663">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="3f57c-664">列の幅。</span><span class="sxs-lookup"><span data-stu-id="3f57c-664">Column width.</span></span> | <span data-ttu-id="3f57c-665">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="3f57c-665">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="3f57c-666">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="3f57c-666">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="3f57c-667">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="3f57c-667">Method widthValue</span></span>

<span data-ttu-id="3f57c-668">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-668">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="3f57c-669">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="3f57c-669">Parameters - widthValue</span></span>

<span data-ttu-id="3f57c-670">値</span><span class="sxs-lookup"><span data-stu-id="3f57c-670">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="3f57c-671">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="3f57c-671">Return Value - widthValue</span></span>

<span data-ttu-id="3f57c-672">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="3f57c-672">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="3f57c-673">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="3f57c-673">Remarks - widthValue</span></span>

<span data-ttu-id="3f57c-674">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="3f57c-674">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="3f57c-675">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="3f57c-675">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="3f57c-676">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="3f57c-676">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="3f57c-677">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="3f57c-677">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="3f57c-678">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="3f57c-678">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="3f57c-679">overrideObject</span><span class="sxs-lookup"><span data-stu-id="3f57c-679">overrideObject</span></span>  

