---
title: FormBuildListControl クラス
description: このトピックでは、FormBuildListControl クラスについて説明します。
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
ms.openlocfilehash: 8e115e6c802eed1387eb127deb096f59603b18f6
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502962"
---
# <a name="class-formbuildlistcontrol"></a><span data-ttu-id="1a77a-103">クラス FormBuildListControl</span><span class="sxs-lookup"><span data-stu-id="1a77a-103">Class FormBuildListControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildListControl extends FormBuildControl
```

<span data-ttu-id="1a77a-104">FormBuildListControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-104">The FormBuildListControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a77a-105">備考</span><span class="sxs-lookup"><span data-stu-id="1a77a-105">Remarks</span></span>

<span data-ttu-id="1a77a-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="1a77a-107">例</span><span class="sxs-lookup"><span data-stu-id="1a77a-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="1a77a-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="1a77a-108">Methods</span></span>

| <span data-ttu-id="1a77a-109">方法</span><span class="sxs-lookup"><span data-stu-id="1a77a-109">Method</span></span>                                                                                                      | <span data-ttu-id="1a77a-110">説明</span><span class="sxs-lookup"><span data-stu-id="1a77a-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a77a-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="1a77a-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-112">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="1a77a-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="1a77a-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-114">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="1a77a-115">public boolean autoArrange(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-115">public boolean autoArrange(\[boolean value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="1a77a-116">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-116">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="1a77a-117">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-117">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="1a77a-118">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-118">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="1a77a-119">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-119">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="1a77a-120">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-120">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="1a77a-121">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-121">Determines whether the control background can be transparent.</span></span>                                                                           |
| <span data-ttu-id="1a77a-122">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-122">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="1a77a-123">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-123">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                             |
| <span data-ttu-id="1a77a-124">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-124">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="1a77a-125">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-125">Gets or sets the style of the borderline of the control.</span></span>                                                                                |
| <span data-ttu-id="1a77a-126">public boolean canScroll(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-126">public boolean canScroll(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="1a77a-127">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-127">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="1a77a-128">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-128">Gets or sets the character set of the font.</span></span>                                                                                             |
| <span data-ttu-id="1a77a-129">public boolean checkBox(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-129">public boolean checkBox(\[boolean value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="1a77a-130">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-130">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="1a77a-131">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-131">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="1a77a-132">public boolean columnHeader(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-132">public boolean columnHeader(\[boolean value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="1a77a-133">public boolean columnHeaderButton(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-133">public boolean columnHeaderButton(\[boolean value\])</span></span>                                                        |                                                                                                                                         |
| <span data-ttu-id="1a77a-134">public boolean columnImages(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-134">public boolean columnImages(\[boolean value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="1a77a-135">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-135">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="1a77a-136">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-136">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="1a77a-137">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="1a77a-137">public int containerId()</span></span>                                                                                    | <span data-ttu-id="1a77a-138">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-138">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="1a77a-139">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-139">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="1a77a-140">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-140">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="1a77a-141">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-141">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="1a77a-142">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-142">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="1a77a-143">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-143">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="1a77a-144">public boolean editLabels(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-144">public boolean editLabels(\[boolean value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="1a77a-145">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-145">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="1a77a-146">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-146">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="1a77a-147">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-147">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="1a77a-148">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-148">Gets or sets the name of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="1a77a-149">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-149">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="1a77a-150">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-150">Gets or sets the size of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="1a77a-151">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-151">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="1a77a-152">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-152">Gets or sets the text color for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="1a77a-153">public boolean gridLines(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-153">public boolean gridLines(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="1a77a-154">public boolean headerdragdrop(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-154">public boolean headerdragdrop(\[boolean value\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="1a77a-155">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-155">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="1a77a-156">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-156">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="1a77a-157">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-157">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="1a77a-158">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-158">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="1a77a-159">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-159">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="1a77a-160">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-160">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="1a77a-161">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-161">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="1a77a-162">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-162">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="1a77a-163">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-163">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="1a77a-164">public int id()</span><span class="sxs-lookup"><span data-stu-id="1a77a-164">public int id()</span></span>                                                                                             | <span data-ttu-id="1a77a-165">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-165">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="1a77a-166">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="1a77a-166">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="1a77a-167">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-167">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="1a77a-168">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-168">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="1a77a-169">public int itemAlign(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-169">public int itemAlign(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="1a77a-170">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-170">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="1a77a-171">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-171">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="1a77a-172">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-172">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="1a77a-173">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-173">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="1a77a-174">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-174">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="1a77a-175">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-175">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="1a77a-176">public boolean oneClickActivate(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-176">public boolean oneClickActivate(\[boolean value\])</span></span>                                                          |                                                                                                                                         |
| <span data-ttu-id="1a77a-177">public boolean rowSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-177">public boolean rowSelect(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="1a77a-178">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-178">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="1a77a-179">public boolean showSelAlways(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-179">public boolean showSelAlways(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="1a77a-180">public boolean singleSelection(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-180">public boolean singleSelection(\[boolean value\])</span></span>                                                           |                                                                                                                                         |
| <span data-ttu-id="1a77a-181">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-181">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="1a77a-182">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-182">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="1a77a-183">public int sort(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-183">public int sort(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="1a77a-184">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-184">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="1a77a-185">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-185">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="1a77a-186">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-186">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="1a77a-187">public boolean trackSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-187">public boolean trackSelect(\[boolean value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="1a77a-188">public boolean twoClickActivate(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-188">public boolean twoClickActivate(\[boolean value\])</span></span>                                                          |                                                                                                                                         |
| <span data-ttu-id="1a77a-189">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-189">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="1a77a-190">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-190">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="1a77a-191">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-191">Sets or returns the underline property for the text in the control.</span></span>                                                                     |
| <span data-ttu-id="1a77a-192">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-192">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="1a77a-193">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-193">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="1a77a-194">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-194">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="1a77a-195">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-195">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="1a77a-196">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-196">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="1a77a-197">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-197">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="1a77a-198">public int viewType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-198">public int viewType(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="1a77a-199">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-199">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="1a77a-200">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-200">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="1a77a-201">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-201">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="1a77a-202">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-202">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="1a77a-203">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-203">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="1a77a-204">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-204">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="1a77a-205">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-205">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="1a77a-206">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="1a77a-206">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="1a77a-207">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="1a77a-207">Method alignControl</span></span>

<span data-ttu-id="1a77a-208">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-208">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="1a77a-209">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="1a77a-209">Parameters - alignControl</span></span>

<span data-ttu-id="1a77a-210">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-210">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="1a77a-211">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="1a77a-211">Return Value - alignControl</span></span>

<span data-ttu-id="1a77a-212">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="1a77a-212">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="1a77a-213">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="1a77a-213">Remarks - alignControl</span></span>

<span data-ttu-id="1a77a-214">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-214">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="1a77a-215">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="1a77a-215">Method allowEdit</span></span>

<span data-ttu-id="1a77a-216">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-216">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="1a77a-217">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="1a77a-217">Parameters - allowEdit</span></span>

<span data-ttu-id="1a77a-218">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-218">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="1a77a-219">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="1a77a-219">Return Value - allowEdit</span></span>

<span data-ttu-id="1a77a-220">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="1a77a-220">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="1a77a-221">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="1a77a-221">Remarks - allowEdit</span></span>

<span data-ttu-id="1a77a-222">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="1a77a-222">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-autoarrange"></a><span data-ttu-id="1a77a-223">メソッド autoArrange</span><span class="sxs-lookup"><span data-stu-id="1a77a-223">Method autoArrange</span></span>

```xpp
public boolean autoArrange([boolean value])
```

### <a name="parameters---autoarrange"></a><span data-ttu-id="1a77a-224">パラメーター - autoArrange</span><span class="sxs-lookup"><span data-stu-id="1a77a-224">Parameters - autoArrange</span></span>

<span data-ttu-id="1a77a-225">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-225">value</span></span>  

### <a name="return-value---autoarrange"></a><span data-ttu-id="1a77a-226">戻り値 - autoArrange</span><span class="sxs-lookup"><span data-stu-id="1a77a-226">Return Value - autoArrange</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="1a77a-227">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="1a77a-227">Method autoDeclaration</span></span>

<span data-ttu-id="1a77a-228">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-228">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="1a77a-229">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="1a77a-229">Parameters - autoDeclaration</span></span>

<span data-ttu-id="1a77a-230">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-230">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="1a77a-231">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="1a77a-231">Return Value - autoDeclaration</span></span>

<span data-ttu-id="1a77a-232">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="1a77a-232">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="1a77a-233">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="1a77a-233">Remarks - autoDeclaration</span></span>

<span data-ttu-id="1a77a-234">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="1a77a-234">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="1a77a-235">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="1a77a-235">Method backgroundColor</span></span>

<span data-ttu-id="1a77a-236">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-236">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="1a77a-237">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="1a77a-237">Parameters - backgroundColor</span></span>

<span data-ttu-id="1a77a-238">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-238">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="1a77a-239">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="1a77a-239">Return Value - backgroundColor</span></span>

<span data-ttu-id="1a77a-240">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="1a77a-240">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="1a77a-241">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="1a77a-241">Remarks - backgroundColor</span></span>

<span data-ttu-id="1a77a-242">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-242">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="1a77a-243">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1a77a-243">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="1a77a-244">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="1a77a-244">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="1a77a-245">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="1a77a-245">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="1a77a-246">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="1a77a-246">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="1a77a-247">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="1a77a-247">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="1a77a-248">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="1a77a-248">Method backStyle</span></span>

<span data-ttu-id="1a77a-249">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-249">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="1a77a-250">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="1a77a-250">Parameters - backStyle</span></span>

<span data-ttu-id="1a77a-251">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-251">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="1a77a-252">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="1a77a-252">Return Value - backStyle</span></span>

<span data-ttu-id="1a77a-253">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="1a77a-253">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="1a77a-254">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="1a77a-254">Method bold</span></span>

<span data-ttu-id="1a77a-255">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-255">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="1a77a-256">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="1a77a-256">Parameters - bold</span></span>

<span data-ttu-id="1a77a-257">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-257">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="1a77a-258">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="1a77a-258">Return Value - bold</span></span>

<span data-ttu-id="1a77a-259">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="1a77a-259">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="1a77a-260">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="1a77a-260">Remarks - bold</span></span>

<span data-ttu-id="1a77a-261">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-261">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="1a77a-262">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-262">0 Use the default font weight.</span></span>
-   <span data-ttu-id="1a77a-263">1 シン。</span><span class="sxs-lookup"><span data-stu-id="1a77a-263">1 Thin.</span></span>
-   <span data-ttu-id="1a77a-264">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="1a77a-264">2 Extra-light.</span></span>
-   <span data-ttu-id="1a77a-265">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="1a77a-265">3 Light.</span></span>
-   <span data-ttu-id="1a77a-266">4 標準。</span><span class="sxs-lookup"><span data-stu-id="1a77a-266">4 Normal.</span></span>
-   <span data-ttu-id="1a77a-267">5 中。</span><span class="sxs-lookup"><span data-stu-id="1a77a-267">5 Medium.</span></span>
-   <span data-ttu-id="1a77a-268">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="1a77a-268">6 Semibold.</span></span>
-   <span data-ttu-id="1a77a-269">7 太字。</span><span class="sxs-lookup"><span data-stu-id="1a77a-269">7 Bold.</span></span>
-   <span data-ttu-id="1a77a-270">8 極太。</span><span class="sxs-lookup"><span data-stu-id="1a77a-270">8 Extra-bold.</span></span>
-   <span data-ttu-id="1a77a-271">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="1a77a-271">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="1a77a-272">メソッド border</span><span class="sxs-lookup"><span data-stu-id="1a77a-272">Method border</span></span>

<span data-ttu-id="1a77a-273">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-273">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="1a77a-274">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="1a77a-274">Parameters - border</span></span>

<span data-ttu-id="1a77a-275">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-275">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="1a77a-276">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="1a77a-276">Return Value - border</span></span>

<span data-ttu-id="1a77a-277">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="1a77a-277">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="1a77a-278">備考 - border</span><span class="sxs-lookup"><span data-stu-id="1a77a-278">Remarks - border</span></span>

<span data-ttu-id="1a77a-279">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-279">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="1a77a-280">値です。</span><span class="sxs-lookup"><span data-stu-id="1a77a-280">Value.</span></span> | <span data-ttu-id="1a77a-281">説明。</span><span class="sxs-lookup"><span data-stu-id="1a77a-281">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="1a77a-282">0</span><span class="sxs-lookup"><span data-stu-id="1a77a-282">0</span></span>      | <span data-ttu-id="1a77a-283">自動。</span><span class="sxs-lookup"><span data-stu-id="1a77a-283">Auto.</span></span>        |
| <span data-ttu-id="1a77a-284">1</span><span class="sxs-lookup"><span data-stu-id="1a77a-284">1</span></span>      | <span data-ttu-id="1a77a-285">3D。</span><span class="sxs-lookup"><span data-stu-id="1a77a-285">3D.</span></span>          |
| <span data-ttu-id="1a77a-286">2</span><span class="sxs-lookup"><span data-stu-id="1a77a-286">2</span></span>      | <span data-ttu-id="1a77a-287">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="1a77a-287">Single line.</span></span> |
| <span data-ttu-id="1a77a-288">3</span><span class="sxs-lookup"><span data-stu-id="1a77a-288">3</span></span>      | <span data-ttu-id="1a77a-289">均一。</span><span class="sxs-lookup"><span data-stu-id="1a77a-289">Flat.</span></span>        |
| <span data-ttu-id="1a77a-290">4</span><span class="sxs-lookup"><span data-stu-id="1a77a-290">4</span></span>      | <span data-ttu-id="1a77a-291">なし。</span><span class="sxs-lookup"><span data-stu-id="1a77a-291">None.</span></span>        |

## <a name="method-canscroll"></a><span data-ttu-id="1a77a-292">メソッド canScroll</span><span class="sxs-lookup"><span data-stu-id="1a77a-292">Method canScroll</span></span>

```xpp
public boolean canScroll([boolean value])
```

### <a name="parameters---canscroll"></a><span data-ttu-id="1a77a-293">パラメーター - canScroll</span><span class="sxs-lookup"><span data-stu-id="1a77a-293">Parameters - canScroll</span></span>

<span data-ttu-id="1a77a-294">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-294">value</span></span>  

### <a name="return-value---canscroll"></a><span data-ttu-id="1a77a-295">戻り値 - canScroll</span><span class="sxs-lookup"><span data-stu-id="1a77a-295">Return Value - canScroll</span></span>

## <a name="method-characterset"></a><span data-ttu-id="1a77a-296">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="1a77a-296">Method characterSet</span></span>

<span data-ttu-id="1a77a-297">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-297">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="1a77a-298">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="1a77a-298">Parameters - characterSet</span></span>

<span data-ttu-id="1a77a-299">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-299">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="1a77a-300">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="1a77a-300">Return Value - characterSet</span></span>

<span data-ttu-id="1a77a-301">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="1a77a-301">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="1a77a-302">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="1a77a-302">Remarks - characterSet</span></span>

<span data-ttu-id="1a77a-303">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-303">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="1a77a-304">値です。</span><span class="sxs-lookup"><span data-stu-id="1a77a-304">Value.</span></span> | <span data-ttu-id="1a77a-305">説明。</span><span class="sxs-lookup"><span data-stu-id="1a77a-305">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="1a77a-306">0</span><span class="sxs-lookup"><span data-stu-id="1a77a-306">0</span></span>      | <span data-ttu-id="1a77a-307">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a77a-307">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="1a77a-308">1</span><span class="sxs-lookup"><span data-stu-id="1a77a-308">1</span></span>      | <span data-ttu-id="1a77a-309">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a77a-309">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="1a77a-310">2</span><span class="sxs-lookup"><span data-stu-id="1a77a-310">2</span></span>      | <span data-ttu-id="1a77a-311">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a77a-311">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="1a77a-312">77</span><span class="sxs-lookup"><span data-stu-id="1a77a-312">77</span></span>     | <span data-ttu-id="1a77a-313">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a77a-313">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="1a77a-314">128</span><span class="sxs-lookup"><span data-stu-id="1a77a-314">128</span></span>    | <span data-ttu-id="1a77a-315">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a77a-315">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="1a77a-316">129</span><span class="sxs-lookup"><span data-stu-id="1a77a-316">129</span></span>    | <span data-ttu-id="1a77a-317">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a77a-317">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="1a77a-318">134</span><span class="sxs-lookup"><span data-stu-id="1a77a-318">134</span></span>    | <span data-ttu-id="1a77a-319">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a77a-319">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="1a77a-320">136</span><span class="sxs-lookup"><span data-stu-id="1a77a-320">136</span></span>    | <span data-ttu-id="1a77a-321">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a77a-321">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="1a77a-322">161</span><span class="sxs-lookup"><span data-stu-id="1a77a-322">161</span></span>    | <span data-ttu-id="1a77a-323">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a77a-323">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="1a77a-324">162</span><span class="sxs-lookup"><span data-stu-id="1a77a-324">162</span></span>    | <span data-ttu-id="1a77a-325">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a77a-325">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="1a77a-326">163</span><span class="sxs-lookup"><span data-stu-id="1a77a-326">163</span></span>    | <span data-ttu-id="1a77a-327">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a77a-327">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="1a77a-328">186</span><span class="sxs-lookup"><span data-stu-id="1a77a-328">186</span></span>    | <span data-ttu-id="1a77a-329">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a77a-329">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="1a77a-330">204</span><span class="sxs-lookup"><span data-stu-id="1a77a-330">204</span></span>    | <span data-ttu-id="1a77a-331">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a77a-331">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="1a77a-332">238</span><span class="sxs-lookup"><span data-stu-id="1a77a-332">238</span></span>    | <span data-ttu-id="1a77a-333">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a77a-333">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="1a77a-334">255</span><span class="sxs-lookup"><span data-stu-id="1a77a-334">255</span></span>    | <span data-ttu-id="1a77a-335">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a77a-335">OEM\_CHARSET</span></span>         |

<span data-ttu-id="1a77a-336">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="1a77a-336">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="1a77a-337">値です。</span><span class="sxs-lookup"><span data-stu-id="1a77a-337">Value.</span></span> | <span data-ttu-id="1a77a-338">説明。</span><span class="sxs-lookup"><span data-stu-id="1a77a-338">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="1a77a-339">130</span><span class="sxs-lookup"><span data-stu-id="1a77a-339">130</span></span>    | <span data-ttu-id="1a77a-340">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a77a-340">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="1a77a-341">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="1a77a-341">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="1a77a-342">値です。</span><span class="sxs-lookup"><span data-stu-id="1a77a-342">Value.</span></span> | <span data-ttu-id="1a77a-343">説明。</span><span class="sxs-lookup"><span data-stu-id="1a77a-343">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="1a77a-344">177</span><span class="sxs-lookup"><span data-stu-id="1a77a-344">177</span></span>    | <span data-ttu-id="1a77a-345">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a77a-345">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="1a77a-346">178</span><span class="sxs-lookup"><span data-stu-id="1a77a-346">178</span></span>    | <span data-ttu-id="1a77a-347">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a77a-347">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="1a77a-348">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="1a77a-348">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="1a77a-349">値です。</span><span class="sxs-lookup"><span data-stu-id="1a77a-349">Value.</span></span> | <span data-ttu-id="1a77a-350">説明。</span><span class="sxs-lookup"><span data-stu-id="1a77a-350">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="1a77a-351">222</span><span class="sxs-lookup"><span data-stu-id="1a77a-351">222</span></span>    | <span data-ttu-id="1a77a-352">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a77a-352">THAI\_CHARSET</span></span> |

<span data-ttu-id="1a77a-353">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-353">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="1a77a-354">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-354">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="1a77a-355">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1a77a-355">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-checkbox"></a><span data-ttu-id="1a77a-356">メソッド checkBox</span><span class="sxs-lookup"><span data-stu-id="1a77a-356">Method checkBox</span></span>

```xpp
public boolean checkBox([boolean value])
```

### <a name="parameters---checkbox"></a><span data-ttu-id="1a77a-357">パラメーター - checkBox</span><span class="sxs-lookup"><span data-stu-id="1a77a-357">Parameters - checkBox</span></span>

<span data-ttu-id="1a77a-358">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-358">value</span></span>  

### <a name="return-value---checkbox"></a><span data-ttu-id="1a77a-359">戻り値- checkBox</span><span class="sxs-lookup"><span data-stu-id="1a77a-359">Return Value - checkBox</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="1a77a-360">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="1a77a-360">Method colorScheme</span></span>

<span data-ttu-id="1a77a-361">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-361">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="1a77a-362">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="1a77a-362">Parameters - colorScheme</span></span>

<span data-ttu-id="1a77a-363">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-363">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="1a77a-364">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="1a77a-364">Return Value - colorScheme</span></span>

<span data-ttu-id="1a77a-365">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="1a77a-365">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="1a77a-366">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="1a77a-366">Remarks - colorScheme</span></span>

<span data-ttu-id="1a77a-367">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-367">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="1a77a-368">値です。</span><span class="sxs-lookup"><span data-stu-id="1a77a-368">Value.</span></span> | <span data-ttu-id="1a77a-369">スタイル。</span><span class="sxs-lookup"><span data-stu-id="1a77a-369">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="1a77a-370">0</span><span class="sxs-lookup"><span data-stu-id="1a77a-370">0</span></span>      | <span data-ttu-id="1a77a-371">既定。</span><span class="sxs-lookup"><span data-stu-id="1a77a-371">Default.</span></span>                       |
| <span data-ttu-id="1a77a-372">1</span><span class="sxs-lookup"><span data-stu-id="1a77a-372">1</span></span>      | <span data-ttu-id="1a77a-373">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="1a77a-373">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="1a77a-374">2</span><span class="sxs-lookup"><span data-stu-id="1a77a-374">2</span></span>      | <span data-ttu-id="1a77a-375">真の配色。</span><span class="sxs-lookup"><span data-stu-id="1a77a-375">The true-color scheme.</span></span>         |

## <a name="method-columnheader"></a><span data-ttu-id="1a77a-376">メソッド columnHeader</span><span class="sxs-lookup"><span data-stu-id="1a77a-376">Method columnHeader</span></span>

```xpp
public boolean columnHeader([boolean value])
```

### <a name="parameters---columnheader"></a><span data-ttu-id="1a77a-377">パラメーター - columnHeader</span><span class="sxs-lookup"><span data-stu-id="1a77a-377">Parameters - columnHeader</span></span>

<span data-ttu-id="1a77a-378">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-378">value</span></span>  

### <a name="return-value---columnheader"></a><span data-ttu-id="1a77a-379">戻り値 - columnHeader</span><span class="sxs-lookup"><span data-stu-id="1a77a-379">Return Value - columnHeader</span></span>

## <a name="method-columnheaderbutton"></a><span data-ttu-id="1a77a-380">メソッド columnHeaderButton</span><span class="sxs-lookup"><span data-stu-id="1a77a-380">Method columnHeaderButton</span></span>

```xpp
public boolean columnHeaderButton([boolean value])
```

### <a name="parameters---columnheaderbutton"></a><span data-ttu-id="1a77a-381">パラメーター - columnHeaderButton</span><span class="sxs-lookup"><span data-stu-id="1a77a-381">Parameters - columnHeaderButton</span></span>

<span data-ttu-id="1a77a-382">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-382">value</span></span>  

### <a name="return-value---columnheaderbutton"></a><span data-ttu-id="1a77a-383">戻り値 - columnHeaderButton</span><span class="sxs-lookup"><span data-stu-id="1a77a-383">Return Value - columnHeaderButton</span></span>

## <a name="method-columnimages"></a><span data-ttu-id="1a77a-384">メソッド columnImages</span><span class="sxs-lookup"><span data-stu-id="1a77a-384">Method columnImages</span></span>

```xpp
public boolean columnImages([boolean value])
```

### <a name="parameters---columnimages"></a><span data-ttu-id="1a77a-385">パラメーター - columnImages</span><span class="sxs-lookup"><span data-stu-id="1a77a-385">Parameters - columnImages</span></span>

<span data-ttu-id="1a77a-386">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-386">value</span></span>  

### <a name="return-value---columnimages"></a><span data-ttu-id="1a77a-387">戻り値 - columnImages</span><span class="sxs-lookup"><span data-stu-id="1a77a-387">Return Value - columnImages</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="1a77a-388">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="1a77a-388">Method configurationKey</span></span>

<span data-ttu-id="1a77a-389">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-389">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="1a77a-390">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="1a77a-390">Parameters - configurationKey</span></span>

<span data-ttu-id="1a77a-391">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-391">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="1a77a-392">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="1a77a-392">Return Value - configurationKey</span></span>

<span data-ttu-id="1a77a-393">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="1a77a-393">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="1a77a-394">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="1a77a-394">Remarks - configurationKey</span></span>

<span data-ttu-id="1a77a-395">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-395">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="1a77a-396">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="1a77a-396">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="1a77a-397">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="1a77a-397">Method containerId</span></span>

<span data-ttu-id="1a77a-398">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-398">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="1a77a-399">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="1a77a-399">Return Value - containerId</span></span>

<span data-ttu-id="1a77a-400">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="1a77a-400">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="1a77a-401">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="1a77a-401">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="1a77a-402">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="1a77a-402">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="1a77a-403">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-403">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="1a77a-404">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="1a77a-404">Return Value - countryRegionCodes</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="1a77a-405">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="1a77a-405">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="1a77a-406">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="1a77a-406">Parameters - dataRelationPath</span></span>

<span data-ttu-id="1a77a-407">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-407">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="1a77a-408">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="1a77a-408">Return Value - dataRelationPath</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="1a77a-409">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="1a77a-409">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="1a77a-410">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="1a77a-410">Parameters - displayTarget</span></span>

<span data-ttu-id="1a77a-411">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-411">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="1a77a-412">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="1a77a-412">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="1a77a-413">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="1a77a-413">Method dragDrop</span></span>

<span data-ttu-id="1a77a-414">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-414">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="1a77a-415">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="1a77a-415">Parameters - dragDrop</span></span>

<span data-ttu-id="1a77a-416">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-416">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="1a77a-417">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="1a77a-417">Return Value - dragDrop</span></span>

<span data-ttu-id="1a77a-418">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="1a77a-418">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-editlabels"></a><span data-ttu-id="1a77a-419">メソッド editLabels</span><span class="sxs-lookup"><span data-stu-id="1a77a-419">Method editLabels</span></span>

```xpp
public boolean editLabels([boolean value])
```

### <a name="parameters---editlabels"></a><span data-ttu-id="1a77a-420">パラメーター - editLabels</span><span class="sxs-lookup"><span data-stu-id="1a77a-420">Parameters - editLabels</span></span>

<span data-ttu-id="1a77a-421">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-421">value</span></span>  

### <a name="return-value---editlabels"></a><span data-ttu-id="1a77a-422">戻り値 - editLabels</span><span class="sxs-lookup"><span data-stu-id="1a77a-422">Return Value - editLabels</span></span>

## <a name="method-enabled"></a><span data-ttu-id="1a77a-423">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="1a77a-423">Method enabled</span></span>

<span data-ttu-id="1a77a-424">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-424">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="1a77a-425">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="1a77a-425">Parameters - enabled</span></span>

<span data-ttu-id="1a77a-426">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-426">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="1a77a-427">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="1a77a-427">Return Value - enabled</span></span>

<span data-ttu-id="1a77a-428">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="1a77a-428">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="1a77a-429">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="1a77a-429">Remarks - enabled</span></span>

<span data-ttu-id="1a77a-430">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-430">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="1a77a-431">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-431">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="1a77a-432">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-432">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="1a77a-433">メソッド font</span><span class="sxs-lookup"><span data-stu-id="1a77a-433">Method font</span></span>

<span data-ttu-id="1a77a-434">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-434">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="1a77a-435">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="1a77a-435">Parameters - font</span></span>

<span data-ttu-id="1a77a-436">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-436">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="1a77a-437">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="1a77a-437">Return Value - font</span></span>

<span data-ttu-id="1a77a-438">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="1a77a-438">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="1a77a-439">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="1a77a-439">Method fontSize</span></span>

<span data-ttu-id="1a77a-440">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-440">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="1a77a-441">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="1a77a-441">Parameters - fontSize</span></span>

<span data-ttu-id="1a77a-442">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-442">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="1a77a-443">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="1a77a-443">Return Value - fontSize</span></span>

<span data-ttu-id="1a77a-444">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="1a77a-444">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="1a77a-445">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="1a77a-445">Method foregroundColor</span></span>

<span data-ttu-id="1a77a-446">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-446">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="1a77a-447">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="1a77a-447">Parameters - foregroundColor</span></span>

<span data-ttu-id="1a77a-448">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-448">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="1a77a-449">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="1a77a-449">Return Value - foregroundColor</span></span>

<span data-ttu-id="1a77a-450">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="1a77a-450">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="1a77a-451">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="1a77a-451">Remarks - foregroundColor</span></span>

<span data-ttu-id="1a77a-452">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-452">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="1a77a-453">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1a77a-453">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="1a77a-454">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="1a77a-454">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="1a77a-455">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="1a77a-455">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="1a77a-456">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="1a77a-456">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="1a77a-457">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="1a77a-457">The maximum value for a single byte is 255.</span></span>

## <a name="method-gridlines"></a><span data-ttu-id="1a77a-458">メソッド gridLines</span><span class="sxs-lookup"><span data-stu-id="1a77a-458">Method gridLines</span></span>

```xpp
public boolean gridLines([boolean value])
```

### <a name="parameters---gridlines"></a><span data-ttu-id="1a77a-459">パラメーター - gridLines</span><span class="sxs-lookup"><span data-stu-id="1a77a-459">Parameters - gridLines</span></span>

<span data-ttu-id="1a77a-460">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-460">value</span></span>  

### <a name="return-value---gridlines"></a><span data-ttu-id="1a77a-461">戻り値 - gridLines</span><span class="sxs-lookup"><span data-stu-id="1a77a-461">Return Value - gridLines</span></span>

## <a name="method-headerdragdrop"></a><span data-ttu-id="1a77a-462">メソッド headerdragdrop</span><span class="sxs-lookup"><span data-stu-id="1a77a-462">Method headerdragdrop</span></span>

```xpp
public boolean headerdragdrop([boolean value])
```

### <a name="parameters---headerdragdrop"></a><span data-ttu-id="1a77a-463">パラメーター - headerdragdrop</span><span class="sxs-lookup"><span data-stu-id="1a77a-463">Parameters - headerdragdrop</span></span>

<span data-ttu-id="1a77a-464">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-464">value</span></span>  

### <a name="return-value---headerdragdrop"></a><span data-ttu-id="1a77a-465">戻り値 - headerdragdrop</span><span class="sxs-lookup"><span data-stu-id="1a77a-465">Return Value - headerdragdrop</span></span>

## <a name="method-height"></a><span data-ttu-id="1a77a-466">メソッド height</span><span class="sxs-lookup"><span data-stu-id="1a77a-466">Method height</span></span>

<span data-ttu-id="1a77a-467">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-467">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="1a77a-468">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="1a77a-468">Parameters - height</span></span>

<span data-ttu-id="1a77a-469">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-469">value</span></span>  

<!-- -->

<span data-ttu-id="1a77a-470">モード</span><span class="sxs-lookup"><span data-stu-id="1a77a-470">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="1a77a-471">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="1a77a-471">Return Value - height</span></span>

<span data-ttu-id="1a77a-472">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="1a77a-472">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="1a77a-473">備考 - height</span><span class="sxs-lookup"><span data-stu-id="1a77a-473">Remarks - height</span></span>

<span data-ttu-id="1a77a-474">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-474">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="1a77a-475">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="1a77a-475">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="1a77a-476">モード。</span><span class="sxs-lookup"><span data-stu-id="1a77a-476">Mode.</span></span>            | <span data-ttu-id="1a77a-477">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="1a77a-477">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a77a-478">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="1a77a-478">-1 Exact.</span></span>        | <span data-ttu-id="1a77a-479">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-479">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="1a77a-480">0 自動。</span><span class="sxs-lookup"><span data-stu-id="1a77a-480">0 Auto.</span></span>          | <span data-ttu-id="1a77a-481">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-481">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="1a77a-482">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="1a77a-482">1 Column height.</span></span> | <span data-ttu-id="1a77a-483">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="1a77a-483">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="1a77a-484">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-484">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="1a77a-485">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="1a77a-485">Method heightMode</span></span>

<span data-ttu-id="1a77a-486">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-486">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="1a77a-487">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="1a77a-487">Parameters - heightMode</span></span>

<span data-ttu-id="1a77a-488">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-488">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="1a77a-489">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="1a77a-489">Return Value - heightMode</span></span>

<span data-ttu-id="1a77a-490">計算モード。</span><span class="sxs-lookup"><span data-stu-id="1a77a-490">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="1a77a-491">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="1a77a-491">Remarks - heightMode</span></span>

<span data-ttu-id="1a77a-492">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="1a77a-492">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="1a77a-493">モード。</span><span class="sxs-lookup"><span data-stu-id="1a77a-493">Mode.</span></span>          | <span data-ttu-id="1a77a-494">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="1a77a-494">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a77a-495">正確。</span><span class="sxs-lookup"><span data-stu-id="1a77a-495">Exact.</span></span>         | <span data-ttu-id="1a77a-496">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-496">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="1a77a-497">自動。</span><span class="sxs-lookup"><span data-stu-id="1a77a-497">Auto.</span></span>          | <span data-ttu-id="1a77a-498">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-498">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="1a77a-499">列の高さ</span><span class="sxs-lookup"><span data-stu-id="1a77a-499">Column height.</span></span> | <span data-ttu-id="1a77a-500">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="1a77a-500">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="1a77a-501">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="1a77a-501">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="1a77a-502">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="1a77a-502">Method heightValue</span></span>

<span data-ttu-id="1a77a-503">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-503">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="1a77a-504">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="1a77a-504">Parameters - heightValue</span></span>

<span data-ttu-id="1a77a-505">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-505">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="1a77a-506">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="1a77a-506">Return Value - heightValue</span></span>

<span data-ttu-id="1a77a-507">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="1a77a-507">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="1a77a-508">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="1a77a-508">Remarks - heightValue</span></span>

<span data-ttu-id="1a77a-509">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="1a77a-509">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="1a77a-510">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="1a77a-510">Method helpText</span></span>

<span data-ttu-id="1a77a-511">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-511">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="1a77a-512">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="1a77a-512">Parameters - helpText</span></span>

<span data-ttu-id="1a77a-513">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-513">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="1a77a-514">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="1a77a-514">Return Value - helpText</span></span>

<span data-ttu-id="1a77a-515">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="1a77a-515">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="1a77a-516">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="1a77a-516">Remarks - helpText</span></span>

<span data-ttu-id="1a77a-517">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-517">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="1a77a-518">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="1a77a-518">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="1a77a-519">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="1a77a-519">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="1a77a-520">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="1a77a-520">Parameters - hierarchyParent</span></span>

<span data-ttu-id="1a77a-521">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-521">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="1a77a-522">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="1a77a-522">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="1a77a-523">メソッド id</span><span class="sxs-lookup"><span data-stu-id="1a77a-523">Method id</span></span>

<span data-ttu-id="1a77a-524">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-524">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="1a77a-525">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="1a77a-525">Return Value - id</span></span>

<span data-ttu-id="1a77a-526">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="1a77a-526">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="1a77a-527">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="1a77a-527">Method isContainer</span></span>

<span data-ttu-id="1a77a-528">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-528">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="1a77a-529">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="1a77a-529">Return Value - isContainer</span></span>

<span data-ttu-id="1a77a-530">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="1a77a-530">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="1a77a-531">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="1a77a-531">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="1a77a-532">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="1a77a-532">Parameters - italic</span></span>

<span data-ttu-id="1a77a-533">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-533">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="1a77a-534">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="1a77a-534">Return Value - italic</span></span>

## <a name="method-itemalign"></a><span data-ttu-id="1a77a-535">メソッド itemAlign</span><span class="sxs-lookup"><span data-stu-id="1a77a-535">Method itemAlign</span></span>

```xpp
public int itemAlign([int value])
```

### <a name="parameters---itemalign"></a><span data-ttu-id="1a77a-536">パラメーター - itemAlign</span><span class="sxs-lookup"><span data-stu-id="1a77a-536">Parameters - itemAlign</span></span>

<span data-ttu-id="1a77a-537">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-537">value</span></span>  

### <a name="return-value---itemalign"></a><span data-ttu-id="1a77a-538">戻り値 - itemAlign</span><span class="sxs-lookup"><span data-stu-id="1a77a-538">Return Value - itemAlign</span></span>

## <a name="method-left"></a><span data-ttu-id="1a77a-539">メソッド left</span><span class="sxs-lookup"><span data-stu-id="1a77a-539">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="1a77a-540">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="1a77a-540">Parameters - left</span></span>

<span data-ttu-id="1a77a-541">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-541">value</span></span>  

<!-- -->

<span data-ttu-id="1a77a-542">モード</span><span class="sxs-lookup"><span data-stu-id="1a77a-542">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="1a77a-543">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="1a77a-543">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="1a77a-544">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="1a77a-544">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="1a77a-545">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="1a77a-545">Parameters - leftMode</span></span>

<span data-ttu-id="1a77a-546">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-546">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="1a77a-547">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="1a77a-547">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="1a77a-548">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="1a77a-548">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="1a77a-549">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="1a77a-549">Parameters - leftValue</span></span>

<span data-ttu-id="1a77a-550">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-550">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="1a77a-551">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="1a77a-551">Return Value - leftValue</span></span>

## <a name="method-name"></a><span data-ttu-id="1a77a-552">メソッド名</span><span class="sxs-lookup"><span data-stu-id="1a77a-552">Method name</span></span>

<span data-ttu-id="1a77a-553">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-553">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="1a77a-554">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="1a77a-554">Parameters - name</span></span>

<span data-ttu-id="1a77a-555">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-555">value</span></span>  
<span data-ttu-id="1a77a-556">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="1a77a-556">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="1a77a-557">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="1a77a-557">Return Value - name</span></span>

<span data-ttu-id="1a77a-558">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="1a77a-558">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="1a77a-559">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="1a77a-559">Remarks - name</span></span>

<span data-ttu-id="1a77a-560">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a77a-560">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="1a77a-561">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a77a-561">It must start with a letter.</span></span>
-   <span data-ttu-id="1a77a-562">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="1a77a-562">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="1a77a-563">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-563">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="1a77a-564">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="1a77a-564">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="1a77a-565">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="1a77a-565">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="1a77a-566">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="1a77a-566">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="1a77a-567">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="1a77a-567">Parameters - neededPermission</span></span>

<span data-ttu-id="1a77a-568">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-568">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="1a77a-569">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="1a77a-569">Return Value - neededPermission</span></span>

## <a name="method-oneclickactivate"></a><span data-ttu-id="1a77a-570">メソッド oneClickActivate</span><span class="sxs-lookup"><span data-stu-id="1a77a-570">Method oneClickActivate</span></span>

```xpp
public boolean oneClickActivate([boolean value])
```

### <a name="parameters---oneclickactivate"></a><span data-ttu-id="1a77a-571">パラメーター - oneClickActivate</span><span class="sxs-lookup"><span data-stu-id="1a77a-571">Parameters - oneClickActivate</span></span>

<span data-ttu-id="1a77a-572">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-572">value</span></span>  

### <a name="return-value---oneclickactivate"></a><span data-ttu-id="1a77a-573">戻り値 - oneClickActivate</span><span class="sxs-lookup"><span data-stu-id="1a77a-573">Return Value - oneClickActivate</span></span>

## <a name="method-rowselect"></a><span data-ttu-id="1a77a-574">メソッド rowSelect</span><span class="sxs-lookup"><span data-stu-id="1a77a-574">Method rowSelect</span></span>

```xpp
public boolean rowSelect([boolean value])
```

### <a name="parameters---rowselect"></a><span data-ttu-id="1a77a-575">パラメーター - rowSelect</span><span class="sxs-lookup"><span data-stu-id="1a77a-575">Parameters - rowSelect</span></span>

<span data-ttu-id="1a77a-576">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-576">value</span></span>  

### <a name="return-value---rowselect"></a><span data-ttu-id="1a77a-577">戻り値 - rowSelect</span><span class="sxs-lookup"><span data-stu-id="1a77a-577">Return Value - rowSelect</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="1a77a-578">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="1a77a-578">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="1a77a-579">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="1a77a-579">Parameters - securityKey</span></span>

<span data-ttu-id="1a77a-580">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-580">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="1a77a-581">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="1a77a-581">Return Value - securityKey</span></span>

## <a name="method-showselalways"></a><span data-ttu-id="1a77a-582">メソッド showSelAlways</span><span class="sxs-lookup"><span data-stu-id="1a77a-582">Method showSelAlways</span></span>

```xpp
public boolean showSelAlways([boolean value])
```

### <a name="parameters---showselalways"></a><span data-ttu-id="1a77a-583">/パラメーター - showSelAlways</span><span class="sxs-lookup"><span data-stu-id="1a77a-583">Parameters - showSelAlways</span></span>

<span data-ttu-id="1a77a-584">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-584">value</span></span>  

### <a name="return-value---showselalways"></a><span data-ttu-id="1a77a-585">戻り値 - showSelAlways</span><span class="sxs-lookup"><span data-stu-id="1a77a-585">Return Value - showSelAlways</span></span>

## <a name="method-singleselection"></a><span data-ttu-id="1a77a-586">メソッド singleSelection</span><span class="sxs-lookup"><span data-stu-id="1a77a-586">Method singleSelection</span></span>

```xpp
public boolean singleSelection([boolean value])
```

### <a name="parameters---singleselection"></a><span data-ttu-id="1a77a-587">パラメーター - singleSelection</span><span class="sxs-lookup"><span data-stu-id="1a77a-587">Parameters - singleSelection</span></span>

<span data-ttu-id="1a77a-588">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-588">value</span></span>  

### <a name="return-value---singleselection"></a><span data-ttu-id="1a77a-589">戻り値 - singleSelection</span><span class="sxs-lookup"><span data-stu-id="1a77a-589">Return Value - singleSelection</span></span>

## <a name="method-skip"></a><span data-ttu-id="1a77a-590">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="1a77a-590">Method skip</span></span>

<span data-ttu-id="1a77a-591">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-591">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="1a77a-592">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="1a77a-592">Parameters - skip</span></span>

<span data-ttu-id="1a77a-593">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-593">value</span></span>  
<span data-ttu-id="1a77a-594">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="1a77a-594">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="1a77a-595">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="1a77a-595">Return Value - skip</span></span>

<span data-ttu-id="1a77a-596">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="1a77a-596">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-sort"></a><span data-ttu-id="1a77a-597">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="1a77a-597">Method sort</span></span>

```xpp
public int sort([int value])
```

### <a name="parameters---sort"></a><span data-ttu-id="1a77a-598">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="1a77a-598">Parameters - sort</span></span>

<span data-ttu-id="1a77a-599">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-599">value</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="1a77a-600">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="1a77a-600">Return Value - sort</span></span>

## <a name="method-top"></a><span data-ttu-id="1a77a-601">メソッド top</span><span class="sxs-lookup"><span data-stu-id="1a77a-601">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="1a77a-602">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="1a77a-602">Parameters - top</span></span>

<span data-ttu-id="1a77a-603">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-603">value</span></span>  

<!-- -->

<span data-ttu-id="1a77a-604">モード</span><span class="sxs-lookup"><span data-stu-id="1a77a-604">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="1a77a-605">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="1a77a-605">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="1a77a-606">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="1a77a-606">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="1a77a-607">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="1a77a-607">Parameters - topMode</span></span>

<span data-ttu-id="1a77a-608">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-608">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="1a77a-609">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="1a77a-609">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="1a77a-610">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="1a77a-610">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="1a77a-611">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="1a77a-611">Parameters - topValue</span></span>

<span data-ttu-id="1a77a-612">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-612">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="1a77a-613">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="1a77a-613">Return Value - topValue</span></span>

## <a name="method-trackselect"></a><span data-ttu-id="1a77a-614">メソッド trackSelect</span><span class="sxs-lookup"><span data-stu-id="1a77a-614">Method trackSelect</span></span>

```xpp
public boolean trackSelect([boolean value])
```

### <a name="parameters---trackselect"></a><span data-ttu-id="1a77a-615">パラメーター - trackSelect</span><span class="sxs-lookup"><span data-stu-id="1a77a-615">Parameters - trackSelect</span></span>

<span data-ttu-id="1a77a-616">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-616">value</span></span>  

### <a name="return-value---trackselect"></a><span data-ttu-id="1a77a-617">戻り値 - trackSelect</span><span class="sxs-lookup"><span data-stu-id="1a77a-617">Return Value - trackSelect</span></span>

## <a name="method-twoclickactivate"></a><span data-ttu-id="1a77a-618">メソッド twoClickActivate</span><span class="sxs-lookup"><span data-stu-id="1a77a-618">Method twoClickActivate</span></span>

```xpp
public boolean twoClickActivate([boolean value])
```

### <a name="parameters---twoclickactivate"></a><span data-ttu-id="1a77a-619">パラメーター - twoClickActivate</span><span class="sxs-lookup"><span data-stu-id="1a77a-619">Parameters - twoClickActivate</span></span>

<span data-ttu-id="1a77a-620">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-620">value</span></span>  

### <a name="return-value---twoclickactivate"></a><span data-ttu-id="1a77a-621">戻り値 - twoClickActivate</span><span class="sxs-lookup"><span data-stu-id="1a77a-621">Return Value - twoClickActivate</span></span>

## <a name="method-type"></a><span data-ttu-id="1a77a-622">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="1a77a-622">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="1a77a-623">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="1a77a-623">Parameters - type</span></span>

<span data-ttu-id="1a77a-624">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-624">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="1a77a-625">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="1a77a-625">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="1a77a-626">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="1a77a-626">Method underline</span></span>

<span data-ttu-id="1a77a-627">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-627">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="1a77a-628">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="1a77a-628">Parameters - underline</span></span>

<span data-ttu-id="1a77a-629">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-629">value</span></span>  
<span data-ttu-id="1a77a-630">コントロールの underline プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="1a77a-630">The value to assign to the underline property of the control; optional.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="1a77a-631">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="1a77a-631">Return Value - underline</span></span>

<span data-ttu-id="1a77a-632">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="1a77a-632">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-userdata"></a><span data-ttu-id="1a77a-633">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="1a77a-633">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="1a77a-634">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="1a77a-634">Parameters - userData</span></span>

<span data-ttu-id="1a77a-635">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-635">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="1a77a-636">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="1a77a-636">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="1a77a-637">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="1a77a-637">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="1a77a-638">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="1a77a-638">Parameters - userDataItem</span></span>

<span data-ttu-id="1a77a-639">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-639">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="1a77a-640">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="1a77a-640">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="1a77a-641">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="1a77a-641">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="1a77a-642">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="1a77a-642">Parameters - userDataItems</span></span>

<span data-ttu-id="1a77a-643">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-643">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="1a77a-644">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="1a77a-644">Return Value - userDataItems</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="1a77a-645">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="1a77a-645">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="1a77a-646">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="1a77a-646">Parameters - verticalSpacing</span></span>

<span data-ttu-id="1a77a-647">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-647">value</span></span>  

<!-- -->

<span data-ttu-id="1a77a-648">モード</span><span class="sxs-lookup"><span data-stu-id="1a77a-648">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="1a77a-649">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="1a77a-649">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="1a77a-650">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="1a77a-650">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="1a77a-651">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="1a77a-651">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="1a77a-652">モード</span><span class="sxs-lookup"><span data-stu-id="1a77a-652">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="1a77a-653">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="1a77a-653">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="1a77a-654">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="1a77a-654">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="1a77a-655">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="1a77a-655">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="1a77a-656">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-656">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="1a77a-657">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="1a77a-657">Return Value - verticalSpacingValue</span></span>

## <a name="method-viewtype"></a><span data-ttu-id="1a77a-658">メソッド viewType</span><span class="sxs-lookup"><span data-stu-id="1a77a-658">Method viewType</span></span>

```xpp
public int viewType([int value])
```

### <a name="parameters---viewtype"></a><span data-ttu-id="1a77a-659">パラメーター - viewType</span><span class="sxs-lookup"><span data-stu-id="1a77a-659">Parameters - viewType</span></span>

<span data-ttu-id="1a77a-660">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-660">value</span></span>  

### <a name="return-value---viewtype"></a><span data-ttu-id="1a77a-661">戻り値 - viewType</span><span class="sxs-lookup"><span data-stu-id="1a77a-661">Return Value - viewType</span></span>

## <a name="method-visible"></a><span data-ttu-id="1a77a-662">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="1a77a-662">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="1a77a-663">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="1a77a-663">Parameters - visible</span></span>

<span data-ttu-id="1a77a-664">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-664">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="1a77a-665">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="1a77a-665">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="1a77a-666">メソッド width</span><span class="sxs-lookup"><span data-stu-id="1a77a-666">Method width</span></span>

<span data-ttu-id="1a77a-667">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-667">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="1a77a-668">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="1a77a-668">Parameters - width</span></span>

<span data-ttu-id="1a77a-669">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-669">value</span></span>  

<!-- -->

<span data-ttu-id="1a77a-670">モード</span><span class="sxs-lookup"><span data-stu-id="1a77a-670">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="1a77a-671">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="1a77a-671">Return Value - width</span></span>

<span data-ttu-id="1a77a-672">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="1a77a-672">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="1a77a-673">備考 - width</span><span class="sxs-lookup"><span data-stu-id="1a77a-673">Remarks - width</span></span>

<span data-ttu-id="1a77a-674">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-674">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="1a77a-675">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="1a77a-675">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="1a77a-676">モード。</span><span class="sxs-lookup"><span data-stu-id="1a77a-676">Mode.</span></span>           | <span data-ttu-id="1a77a-677">幅計算。</span><span class="sxs-lookup"><span data-stu-id="1a77a-677">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a77a-678">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="1a77a-678">-1 Exact.</span></span>       | <span data-ttu-id="1a77a-679">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-679">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="1a77a-680">0 自動。</span><span class="sxs-lookup"><span data-stu-id="1a77a-680">0 Auto.</span></span>         | <span data-ttu-id="1a77a-681">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-681">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="1a77a-682">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="1a77a-682">1 Column width.</span></span> | <span data-ttu-id="1a77a-683">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="1a77a-683">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="1a77a-684">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-684">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="1a77a-685">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="1a77a-685">Method widthMode</span></span>

<span data-ttu-id="1a77a-686">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-686">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="1a77a-687">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="1a77a-687">Parameters - widthMode</span></span>

<span data-ttu-id="1a77a-688">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-688">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="1a77a-689">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="1a77a-689">Return Value - widthMode</span></span>

<span data-ttu-id="1a77a-690">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="1a77a-690">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="1a77a-691">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="1a77a-691">Remarks - widthMode</span></span>

<span data-ttu-id="1a77a-692">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="1a77a-692">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="1a77a-693">モード。</span><span class="sxs-lookup"><span data-stu-id="1a77a-693">Mode.</span></span>         | <span data-ttu-id="1a77a-694">幅計算。</span><span class="sxs-lookup"><span data-stu-id="1a77a-694">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a77a-695">正確。</span><span class="sxs-lookup"><span data-stu-id="1a77a-695">Exact.</span></span>        | <span data-ttu-id="1a77a-696">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-696">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="1a77a-697">自動。</span><span class="sxs-lookup"><span data-stu-id="1a77a-697">Auto.</span></span>         | <span data-ttu-id="1a77a-698">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="1a77a-698">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="1a77a-699">列の幅。</span><span class="sxs-lookup"><span data-stu-id="1a77a-699">Column width.</span></span> | <span data-ttu-id="1a77a-700">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="1a77a-700">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="1a77a-701">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="1a77a-701">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="1a77a-702">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="1a77a-702">Method widthValue</span></span>

<span data-ttu-id="1a77a-703">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-703">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="1a77a-704">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="1a77a-704">Parameters - widthValue</span></span>

<span data-ttu-id="1a77a-705">値</span><span class="sxs-lookup"><span data-stu-id="1a77a-705">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="1a77a-706">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="1a77a-706">Return Value - widthValue</span></span>

<span data-ttu-id="1a77a-707">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="1a77a-707">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="1a77a-708">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="1a77a-708">Remarks - widthValue</span></span>

<span data-ttu-id="1a77a-709">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="1a77a-709">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="1a77a-710">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="1a77a-710">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="1a77a-711">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="1a77a-711">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="1a77a-712">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="1a77a-712">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="1a77a-713">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="1a77a-713">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="1a77a-714">overrideObject</span><span class="sxs-lookup"><span data-stu-id="1a77a-714">overrideObject</span></span>  

