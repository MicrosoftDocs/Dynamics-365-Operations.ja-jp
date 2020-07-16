---
title: FormBuildButtonControl クラス
description: このトピックでは、FormBuildButtonControl クラスについて説明します。
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
ms.openlocfilehash: 70534730e909d62fa29ff25a40ac8ed35bc678af
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502656"
---
# <a name="class-formbuildbuttoncontrol"></a><span data-ttu-id="dc9fe-103">クラス FormBuildButtonControl</span><span class="sxs-lookup"><span data-stu-id="dc9fe-103">Class FormBuildButtonControl</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class FormBuildButtonControl extends FormBuildControl
```

<span data-ttu-id="dc9fe-104">FormBuildButtonControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-104">The FormBuildButtonControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc9fe-105">備考</span><span class="sxs-lookup"><span data-stu-id="dc9fe-105">Remarks</span></span>

<span data-ttu-id="dc9fe-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="dc9fe-107">例</span><span class="sxs-lookup"><span data-stu-id="dc9fe-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="dc9fe-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="dc9fe-108">Methods</span></span>

| <span data-ttu-id="dc9fe-109">方法</span><span class="sxs-lookup"><span data-stu-id="dc9fe-109">Method</span></span>                                                                                                      | <span data-ttu-id="dc9fe-110">説明</span><span class="sxs-lookup"><span data-stu-id="dc9fe-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9fe-111">public int acquireFocus(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-111">public int acquireFocus(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="dc9fe-112">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-112">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="dc9fe-113">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-113">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="dc9fe-114">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-114">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="dc9fe-115">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-115">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="dc9fe-116">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-116">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="dc9fe-117">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-117">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="dc9fe-118">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-118">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="dc9fe-119">public boolean autoRefreshData(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-119">public boolean autoRefreshData(\[boolean value\])</span></span>                                                           |                                                                                                                                         |
| <span data-ttu-id="dc9fe-120">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-120">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="dc9fe-121">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-121">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="dc9fe-122">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-122">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="dc9fe-123">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-123">Determines whether the control background can be transparent.</span></span>                                                                           |
| <span data-ttu-id="dc9fe-124">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-124">public boolean big(\[boolean value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="dc9fe-125">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-125">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="dc9fe-126">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-126">Gets or sets the weight of font used to output text in the control.</span></span>                                                                     |
| <span data-ttu-id="dc9fe-127">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-127">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="dc9fe-128">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-128">Gets or sets the style of the borderline of the control.</span></span>                                                                                |
| <span data-ttu-id="dc9fe-129">public int buttonDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-129">public int buttonDisplay(\[int value\])</span></span>                                                                     | <span data-ttu-id="dc9fe-130">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-130">Gets or sets the appearance of the button control.</span></span>                                                                                      |
| <span data-ttu-id="dc9fe-131">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-131">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="dc9fe-132">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-132">Gets or sets the character set of the font.</span></span>                                                                                             |
| <span data-ttu-id="dc9fe-133">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-133">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="dc9fe-134">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-134">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="dc9fe-135">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-135">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="dc9fe-136">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-136">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="dc9fe-137">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="dc9fe-137">public int containerId()</span></span>                                                                                    | <span data-ttu-id="dc9fe-138">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-138">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="dc9fe-139">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-139">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="dc9fe-140">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-140">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="dc9fe-141">public boolean defaultButton(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-141">public boolean defaultButton(\[boolean value\])</span></span>                                                             | <span data-ttu-id="dc9fe-142">ボタンをフォーム上の既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-142">Determines whether the button should be the default button on the form.</span></span>                                                                 |
| <span data-ttu-id="dc9fe-143">public str disabledImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-143">public str disabledImage(\[str value\])</span></span>                                                                     | <span data-ttu-id="dc9fe-144">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-144">Gets or sets the disabled image of the button.</span></span>                                                                                          |
| <span data-ttu-id="dc9fe-145">public int disabledImageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-145">public int disabledImageLocation(\[int value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="dc9fe-146">public int disabledResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-146">public int disabledResource(\[int value\])</span></span>                                                                  | <span data-ttu-id="dc9fe-147">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-147">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>                                                          |
| <span data-ttu-id="dc9fe-148">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-148">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="dc9fe-149">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-149">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="dc9fe-150">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-150">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="dc9fe-151">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-151">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="dc9fe-152">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-152">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="dc9fe-153">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-153">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="dc9fe-154">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-154">Gets or sets the name of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="dc9fe-155">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-155">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="dc9fe-156">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-156">Gets or sets the size of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="dc9fe-157">public boolean forcedToOverflow(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-157">public boolean forcedToOverflow(\[boolean value\])</span></span>                                                          |                                                                                                                                         |
| <span data-ttu-id="dc9fe-158">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-158">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="dc9fe-159">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-159">Gets or sets the text color for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="dc9fe-160">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-160">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="dc9fe-161">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-161">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="dc9fe-162">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-162">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="dc9fe-163">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-163">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="dc9fe-164">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-164">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="dc9fe-165">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-165">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="dc9fe-166">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-166">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="dc9fe-167">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-167">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="dc9fe-168">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-168">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="dc9fe-169">public int id()</span><span class="sxs-lookup"><span data-stu-id="dc9fe-169">public int id()</span></span>                                                                                             | <span data-ttu-id="dc9fe-170">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-170">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="dc9fe-171">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-171">public int imageLocation(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="dc9fe-172">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="dc9fe-172">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="dc9fe-173">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-173">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="dc9fe-174">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-174">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="dc9fe-175">public str keyTip(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-175">public str keyTip(\[str value\])</span></span>                                                                            |                                                                                                                                         |
| <span data-ttu-id="dc9fe-176">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-176">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="dc9fe-177">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-177">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="dc9fe-178">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-178">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="dc9fe-179">public int multiSelect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-179">public int multiSelect(\[int value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="dc9fe-180">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-180">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="dc9fe-181">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-181">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="dc9fe-182">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-182">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="dc9fe-183">public int needsRecord(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-183">public int needsRecord(\[int value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="dc9fe-184">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-184">public str normalImage(\[str value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="dc9fe-185">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-185">public int normalResource(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="dc9fe-186">public boolean primary(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-186">public boolean primary(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="dc9fe-187">public boolean saveRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-187">public boolean saveRecord(\[boolean value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="dc9fe-188">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-188">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="dc9fe-189">public int shortkey(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-189">public int shortkey(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="dc9fe-190">public boolean showShortCut(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-190">public boolean showShortCut(\[boolean value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="dc9fe-191">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-191">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="dc9fe-192">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-192">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="dc9fe-193">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-193">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="dc9fe-194">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-194">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="dc9fe-195">public int toggleButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-195">public int toggleButton(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="dc9fe-196">public int toggleValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-196">public int toggleValue(\[int value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="dc9fe-197">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-197">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="dc9fe-198">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-198">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="dc9fe-199">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-199">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="dc9fe-200">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-200">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="dc9fe-201">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-201">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="dc9fe-202">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-202">Sets or returns the underline property for the text in the control.</span></span>                                                                     |
| <span data-ttu-id="dc9fe-203">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-203">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="dc9fe-204">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-204">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="dc9fe-205">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-205">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="dc9fe-206">public boolean value(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-206">public boolean value(\[boolean value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="dc9fe-207">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-207">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="dc9fe-208">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-208">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="dc9fe-209">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-209">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="dc9fe-210">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-210">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="dc9fe-211">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-211">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="dc9fe-212">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-212">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="dc9fe-213">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-213">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="dc9fe-214">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-214">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="dc9fe-215">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-215">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="dc9fe-216">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-216">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="dc9fe-217">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="dc9fe-217">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-acquirefocus"></a><span data-ttu-id="dc9fe-218">メソッド acquireFocus</span><span class="sxs-lookup"><span data-stu-id="dc9fe-218">Method acquireFocus</span></span>

```xpp
public int acquireFocus([int value])
```

### <a name="parameters---acquirefocus"></a><span data-ttu-id="dc9fe-219">パラメーター - acquireFocus</span><span class="sxs-lookup"><span data-stu-id="dc9fe-219">Parameters - acquireFocus</span></span>

<span data-ttu-id="dc9fe-220">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-220">value</span></span>  

### <a name="return-value---acquirefocus"></a><span data-ttu-id="dc9fe-221">戻り値 - acquireFocus</span><span class="sxs-lookup"><span data-stu-id="dc9fe-221">Return Value - acquireFocus</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="dc9fe-222">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="dc9fe-222">Method alignControl</span></span>

<span data-ttu-id="dc9fe-223">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-223">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="dc9fe-224">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="dc9fe-224">Parameters - alignControl</span></span>

<span data-ttu-id="dc9fe-225">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-225">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="dc9fe-226">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="dc9fe-226">Return Value - alignControl</span></span>

<span data-ttu-id="dc9fe-227">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-227">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="dc9fe-228">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="dc9fe-228">Remarks - alignControl</span></span>

<span data-ttu-id="dc9fe-229">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-229">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="dc9fe-230">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="dc9fe-230">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="dc9fe-231">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="dc9fe-231">Parameters - alignment</span></span>

<span data-ttu-id="dc9fe-232">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-232">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="dc9fe-233">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="dc9fe-233">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="dc9fe-234">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="dc9fe-234">Method allowEdit</span></span>

<span data-ttu-id="dc9fe-235">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-235">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="dc9fe-236">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="dc9fe-236">Parameters - allowEdit</span></span>

<span data-ttu-id="dc9fe-237">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-237">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="dc9fe-238">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="dc9fe-238">Return Value - allowEdit</span></span>

<span data-ttu-id="dc9fe-239">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-239">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="dc9fe-240">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="dc9fe-240">Remarks - allowEdit</span></span>

<span data-ttu-id="dc9fe-241">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-241">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="dc9fe-242">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="dc9fe-242">Method autoDeclaration</span></span>

<span data-ttu-id="dc9fe-243">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-243">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="dc9fe-244">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="dc9fe-244">Parameters - autoDeclaration</span></span>

<span data-ttu-id="dc9fe-245">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-245">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="dc9fe-246">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="dc9fe-246">Return Value - autoDeclaration</span></span>

<span data-ttu-id="dc9fe-247">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-247">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="dc9fe-248">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="dc9fe-248">Remarks - autoDeclaration</span></span>

<span data-ttu-id="dc9fe-249">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-249">Controls cannot have identical names.</span></span>

## <a name="method-autorefreshdata"></a><span data-ttu-id="dc9fe-250">メソッド autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="dc9fe-250">Method autoRefreshData</span></span>

```xpp
public boolean autoRefreshData([boolean value])
```

### <a name="parameters---autorefreshdata"></a><span data-ttu-id="dc9fe-251">パラメーター - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="dc9fe-251">Parameters - autoRefreshData</span></span>

<span data-ttu-id="dc9fe-252">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-252">value</span></span>  

### <a name="return-value---autorefreshdata"></a><span data-ttu-id="dc9fe-253">戻り値 - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="dc9fe-253">Return Value - autoRefreshData</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="dc9fe-254">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="dc9fe-254">Method backgroundColor</span></span>

<span data-ttu-id="dc9fe-255">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-255">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="dc9fe-256">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="dc9fe-256">Parameters - backgroundColor</span></span>

<span data-ttu-id="dc9fe-257">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-257">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="dc9fe-258">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="dc9fe-258">Return Value - backgroundColor</span></span>

<span data-ttu-id="dc9fe-259">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-259">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="dc9fe-260">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="dc9fe-260">Remarks - backgroundColor</span></span>

<span data-ttu-id="dc9fe-261">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-261">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="dc9fe-262">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-262">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="dc9fe-263">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-263">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="dc9fe-264">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-264">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="dc9fe-265">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-265">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="dc9fe-266">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-266">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="dc9fe-267">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="dc9fe-267">Method backStyle</span></span>

<span data-ttu-id="dc9fe-268">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-268">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="dc9fe-269">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="dc9fe-269">Parameters - backStyle</span></span>

<span data-ttu-id="dc9fe-270">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-270">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="dc9fe-271">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="dc9fe-271">Return Value - backStyle</span></span>

<span data-ttu-id="dc9fe-272">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-272">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-big"></a><span data-ttu-id="dc9fe-273">メソッド big</span><span class="sxs-lookup"><span data-stu-id="dc9fe-273">Method big</span></span>

```xpp
public boolean big([boolean value])
```

### <a name="parameters---big"></a><span data-ttu-id="dc9fe-274">パラメーター - big</span><span class="sxs-lookup"><span data-stu-id="dc9fe-274">Parameters - big</span></span>

<span data-ttu-id="dc9fe-275">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-275">value</span></span>  

### <a name="return-value---big"></a><span data-ttu-id="dc9fe-276">戻り値 - big</span><span class="sxs-lookup"><span data-stu-id="dc9fe-276">Return Value - big</span></span>

## <a name="method-bold"></a><span data-ttu-id="dc9fe-277">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="dc9fe-277">Method bold</span></span>

<span data-ttu-id="dc9fe-278">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-278">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="dc9fe-279">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="dc9fe-279">Parameters - bold</span></span>

<span data-ttu-id="dc9fe-280">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-280">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="dc9fe-281">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="dc9fe-281">Return Value - bold</span></span>

<span data-ttu-id="dc9fe-282">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-282">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="dc9fe-283">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="dc9fe-283">Remarks - bold</span></span>

<span data-ttu-id="dc9fe-284">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-284">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="dc9fe-285">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-285">0 Use the default font weight.</span></span>
-   <span data-ttu-id="dc9fe-286">1 シン。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-286">1 Thin.</span></span>
-   <span data-ttu-id="dc9fe-287">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-287">2 Extra-light.</span></span>
-   <span data-ttu-id="dc9fe-288">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-288">3 Light.</span></span>
-   <span data-ttu-id="dc9fe-289">4 標準。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-289">4 Normal.</span></span>
-   <span data-ttu-id="dc9fe-290">5 中。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-290">5 Medium.</span></span>
-   <span data-ttu-id="dc9fe-291">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-291">6 Semibold.</span></span>
-   <span data-ttu-id="dc9fe-292">7 太字。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-292">7 Bold.</span></span>
-   <span data-ttu-id="dc9fe-293">8 極太。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-293">8 Extra-bold.</span></span>
-   <span data-ttu-id="dc9fe-294">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-294">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="dc9fe-295">メソッド border</span><span class="sxs-lookup"><span data-stu-id="dc9fe-295">Method border</span></span>

<span data-ttu-id="dc9fe-296">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-296">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="dc9fe-297">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="dc9fe-297">Parameters - border</span></span>

<span data-ttu-id="dc9fe-298">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-298">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="dc9fe-299">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="dc9fe-299">Return Value - border</span></span>

<span data-ttu-id="dc9fe-300">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-300">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="dc9fe-301">備考 - border</span><span class="sxs-lookup"><span data-stu-id="dc9fe-301">Remarks - border</span></span>

<span data-ttu-id="dc9fe-302">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-302">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="dc9fe-303">値です。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-303">Value.</span></span> | <span data-ttu-id="dc9fe-304">説明。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-304">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="dc9fe-305">0</span><span class="sxs-lookup"><span data-stu-id="dc9fe-305">0</span></span>      | <span data-ttu-id="dc9fe-306">自動。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-306">Auto.</span></span>        |
| <span data-ttu-id="dc9fe-307">1</span><span class="sxs-lookup"><span data-stu-id="dc9fe-307">1</span></span>      | <span data-ttu-id="dc9fe-308">3D。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-308">3D.</span></span>          |
| <span data-ttu-id="dc9fe-309">2</span><span class="sxs-lookup"><span data-stu-id="dc9fe-309">2</span></span>      | <span data-ttu-id="dc9fe-310">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-310">Single line.</span></span> |
| <span data-ttu-id="dc9fe-311">3</span><span class="sxs-lookup"><span data-stu-id="dc9fe-311">3</span></span>      | <span data-ttu-id="dc9fe-312">均一。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-312">Flat.</span></span>        |
| <span data-ttu-id="dc9fe-313">4</span><span class="sxs-lookup"><span data-stu-id="dc9fe-313">4</span></span>      | <span data-ttu-id="dc9fe-314">なし。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-314">None.</span></span>        |

## <a name="method-buttondisplay"></a><span data-ttu-id="dc9fe-315">メソッド buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="dc9fe-315">Method buttonDisplay</span></span>

<span data-ttu-id="dc9fe-316">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-316">Gets or sets the appearance of the button control.</span></span>

```xpp
public int buttonDisplay([int value])
```

### <a name="parameters---buttondisplay"></a><span data-ttu-id="dc9fe-317">パラメーター - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="dc9fe-317">Parameters - buttonDisplay</span></span>

<span data-ttu-id="dc9fe-318">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-318">value</span></span>  

### <a name="return-value---buttondisplay"></a><span data-ttu-id="dc9fe-319">戻り値 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="dc9fe-319">Return Value - buttonDisplay</span></span>

<span data-ttu-id="dc9fe-320">ゼロから 5 までの整数。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-320">An integer between zero and five, inclusive.</span></span>

### <a name="remarks---buttondisplay"></a><span data-ttu-id="dc9fe-321">備考 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="dc9fe-321">Remarks - buttonDisplay</span></span>

<span data-ttu-id="dc9fe-322">プロパティ値は、テキスト、画像、またはその両方のいずれをボタンに表示するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-322">The value of the property defines whether the text, the image, or both should be displayed on the button.</span></span> <span data-ttu-id="dc9fe-323">このプロパティは、テキストと画像の両方が表示されている場合は、テキストと画像の相対位置も制御します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-323">This property also controls relative positions of text and image if both are displayed.</span></span> <span data-ttu-id="dc9fe-324">返される整数値には、次のようなボタン コントロールの外観が含まれます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-324">The integer value that is returned contains the appearance of the button control as follows:</span></span>

| <span data-ttu-id="dc9fe-325">値です。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-325">Value.</span></span> | <span data-ttu-id="dc9fe-326">説明。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-326">Description.</span></span>                                                     |
|--------|------------------------------------------------------------------|
| <span data-ttu-id="dc9fe-327">0</span><span class="sxs-lookup"><span data-stu-id="dc9fe-327">0</span></span>      | <span data-ttu-id="dc9fe-328">テキストのみ。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-328">Text only.</span></span>                                                       |
| <span data-ttu-id="dc9fe-329">1</span><span class="sxs-lookup"><span data-stu-id="dc9fe-329">1</span></span>      | <span data-ttu-id="dc9fe-330">イメージのみ。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-330">Image Only.</span></span>                                                      |
| <span data-ttu-id="dc9fe-331">2</span><span class="sxs-lookup"><span data-stu-id="dc9fe-331">2</span></span>      | <span data-ttu-id="dc9fe-332">テキストと画像。画像はテキストの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-332">Text and image; the image is displayed below the text.</span></span>           |
| <span data-ttu-id="dc9fe-333">3</span><span class="sxs-lookup"><span data-stu-id="dc9fe-333">3</span></span>      | <span data-ttu-id="dc9fe-334">テキストと画像。画像はテキストの上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-334">Text and image; the image is displayed above the text.</span></span>           |
| <span data-ttu-id="dc9fe-335">4</span><span class="sxs-lookup"><span data-stu-id="dc9fe-335">4</span></span>      | <span data-ttu-id="dc9fe-336">テキストと画像。画像はテキストの左に表示されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-336">Text and image; the image is displayed to the left of the text.</span></span>  |
| <span data-ttu-id="dc9fe-337">5</span><span class="sxs-lookup"><span data-stu-id="dc9fe-337">5</span></span>      | <span data-ttu-id="dc9fe-338">テキストと画像。画像はテキストの右に表示されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-338">Text and image; the image is displayed to the right of the text.</span></span> |

## <a name="method-characterset"></a><span data-ttu-id="dc9fe-339">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="dc9fe-339">Method characterSet</span></span>

<span data-ttu-id="dc9fe-340">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-340">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="dc9fe-341">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="dc9fe-341">Parameters - characterSet</span></span>

<span data-ttu-id="dc9fe-342">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-342">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="dc9fe-343">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="dc9fe-343">Return Value - characterSet</span></span>

<span data-ttu-id="dc9fe-344">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-344">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="dc9fe-345">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="dc9fe-345">Remarks - characterSet</span></span>

<span data-ttu-id="dc9fe-346">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-346">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="dc9fe-347">値です。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-347">Value.</span></span> | <span data-ttu-id="dc9fe-348">説明。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-348">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="dc9fe-349">0</span><span class="sxs-lookup"><span data-stu-id="dc9fe-349">0</span></span>      | <span data-ttu-id="dc9fe-350">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dc9fe-350">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="dc9fe-351">1</span><span class="sxs-lookup"><span data-stu-id="dc9fe-351">1</span></span>      | <span data-ttu-id="dc9fe-352">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dc9fe-352">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="dc9fe-353">2</span><span class="sxs-lookup"><span data-stu-id="dc9fe-353">2</span></span>      | <span data-ttu-id="dc9fe-354">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dc9fe-354">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="dc9fe-355">77</span><span class="sxs-lookup"><span data-stu-id="dc9fe-355">77</span></span>     | <span data-ttu-id="dc9fe-356">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dc9fe-356">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="dc9fe-357">128</span><span class="sxs-lookup"><span data-stu-id="dc9fe-357">128</span></span>    | <span data-ttu-id="dc9fe-358">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dc9fe-358">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="dc9fe-359">129</span><span class="sxs-lookup"><span data-stu-id="dc9fe-359">129</span></span>    | <span data-ttu-id="dc9fe-360">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dc9fe-360">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="dc9fe-361">134</span><span class="sxs-lookup"><span data-stu-id="dc9fe-361">134</span></span>    | <span data-ttu-id="dc9fe-362">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dc9fe-362">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="dc9fe-363">136</span><span class="sxs-lookup"><span data-stu-id="dc9fe-363">136</span></span>    | <span data-ttu-id="dc9fe-364">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dc9fe-364">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="dc9fe-365">161</span><span class="sxs-lookup"><span data-stu-id="dc9fe-365">161</span></span>    | <span data-ttu-id="dc9fe-366">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dc9fe-366">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="dc9fe-367">162</span><span class="sxs-lookup"><span data-stu-id="dc9fe-367">162</span></span>    | <span data-ttu-id="dc9fe-368">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dc9fe-368">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="dc9fe-369">163</span><span class="sxs-lookup"><span data-stu-id="dc9fe-369">163</span></span>    | <span data-ttu-id="dc9fe-370">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dc9fe-370">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="dc9fe-371">186</span><span class="sxs-lookup"><span data-stu-id="dc9fe-371">186</span></span>    | <span data-ttu-id="dc9fe-372">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dc9fe-372">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="dc9fe-373">204</span><span class="sxs-lookup"><span data-stu-id="dc9fe-373">204</span></span>    | <span data-ttu-id="dc9fe-374">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dc9fe-374">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="dc9fe-375">238</span><span class="sxs-lookup"><span data-stu-id="dc9fe-375">238</span></span>    | <span data-ttu-id="dc9fe-376">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dc9fe-376">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="dc9fe-377">255</span><span class="sxs-lookup"><span data-stu-id="dc9fe-377">255</span></span>    | <span data-ttu-id="dc9fe-378">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dc9fe-378">OEM\_CHARSET</span></span>         |

<span data-ttu-id="dc9fe-379">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-379">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="dc9fe-380">値です。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-380">Value.</span></span> | <span data-ttu-id="dc9fe-381">説明。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-381">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="dc9fe-382">130</span><span class="sxs-lookup"><span data-stu-id="dc9fe-382">130</span></span>    | <span data-ttu-id="dc9fe-383">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dc9fe-383">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="dc9fe-384">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-384">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="dc9fe-385">値です。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-385">Value.</span></span> | <span data-ttu-id="dc9fe-386">説明。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-386">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="dc9fe-387">177</span><span class="sxs-lookup"><span data-stu-id="dc9fe-387">177</span></span>    | <span data-ttu-id="dc9fe-388">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dc9fe-388">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="dc9fe-389">178</span><span class="sxs-lookup"><span data-stu-id="dc9fe-389">178</span></span>    | <span data-ttu-id="dc9fe-390">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dc9fe-390">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="dc9fe-391">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-391">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="dc9fe-392">値です。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-392">Value.</span></span> | <span data-ttu-id="dc9fe-393">説明。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-393">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="dc9fe-394">222</span><span class="sxs-lookup"><span data-stu-id="dc9fe-394">222</span></span>    | <span data-ttu-id="dc9fe-395">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dc9fe-395">THAI\_CHARSET</span></span> |

<span data-ttu-id="dc9fe-396">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-396">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="dc9fe-397">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-397">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="dc9fe-398">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-398">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="dc9fe-399">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="dc9fe-399">Method colorScheme</span></span>

<span data-ttu-id="dc9fe-400">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-400">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="dc9fe-401">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="dc9fe-401">Parameters - colorScheme</span></span>

<span data-ttu-id="dc9fe-402">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-402">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="dc9fe-403">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="dc9fe-403">Return Value - colorScheme</span></span>

<span data-ttu-id="dc9fe-404">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-404">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="dc9fe-405">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="dc9fe-405">Remarks - colorScheme</span></span>

<span data-ttu-id="dc9fe-406">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-406">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="dc9fe-407">値です。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-407">Value.</span></span> | <span data-ttu-id="dc9fe-408">スタイル。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-408">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="dc9fe-409">0</span><span class="sxs-lookup"><span data-stu-id="dc9fe-409">0</span></span>      | <span data-ttu-id="dc9fe-410">既定。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-410">Default.</span></span>                       |
| <span data-ttu-id="dc9fe-411">1</span><span class="sxs-lookup"><span data-stu-id="dc9fe-411">1</span></span>      | <span data-ttu-id="dc9fe-412">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-412">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="dc9fe-413">2</span><span class="sxs-lookup"><span data-stu-id="dc9fe-413">2</span></span>      | <span data-ttu-id="dc9fe-414">真の配色。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-414">The true-color scheme.</span></span>         |

## <a name="method-configurationkey"></a><span data-ttu-id="dc9fe-415">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="dc9fe-415">Method configurationKey</span></span>

<span data-ttu-id="dc9fe-416">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-416">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="dc9fe-417">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="dc9fe-417">Parameters - configurationKey</span></span>

<span data-ttu-id="dc9fe-418">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-418">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="dc9fe-419">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="dc9fe-419">Return Value - configurationKey</span></span>

<span data-ttu-id="dc9fe-420">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-420">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="dc9fe-421">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="dc9fe-421">Remarks - configurationKey</span></span>

<span data-ttu-id="dc9fe-422">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-422">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="dc9fe-423">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-423">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="dc9fe-424">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="dc9fe-424">Method containerId</span></span>

<span data-ttu-id="dc9fe-425">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-425">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="dc9fe-426">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="dc9fe-426">Return Value - containerId</span></span>

<span data-ttu-id="dc9fe-427">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-427">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="dc9fe-428">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="dc9fe-428">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="dc9fe-429">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="dc9fe-429">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="dc9fe-430">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-430">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="dc9fe-431">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="dc9fe-431">Return Value - countryRegionCodes</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="dc9fe-432">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="dc9fe-432">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="dc9fe-433">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="dc9fe-433">Parameters - dataRelationPath</span></span>

<span data-ttu-id="dc9fe-434">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-434">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="dc9fe-435">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="dc9fe-435">Return Value - dataRelationPath</span></span>

## <a name="method-defaultbutton"></a><span data-ttu-id="dc9fe-436">メソッド defaultButton</span><span class="sxs-lookup"><span data-stu-id="dc9fe-436">Method defaultButton</span></span>

<span data-ttu-id="dc9fe-437">ボタンをフォーム上の既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-437">Determines whether the button should be the default button on the form.</span></span>

```xpp
public boolean defaultButton([boolean value])
```

### <a name="parameters---defaultbutton"></a><span data-ttu-id="dc9fe-438">パラメーター - defaultButton</span><span class="sxs-lookup"><span data-stu-id="dc9fe-438">Parameters - defaultButton</span></span>

<span data-ttu-id="dc9fe-439">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-439">value</span></span>  

### <a name="return-value---defaultbutton"></a><span data-ttu-id="dc9fe-440">戻り値 - defaultButton</span><span class="sxs-lookup"><span data-stu-id="dc9fe-440">Return Value - defaultButton</span></span>

<span data-ttu-id="dc9fe-441">ボタンが既定のボタンである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-441">true if the button should be the default button; otherwise, false.</span></span>

## <a name="method-disabledimage"></a><span data-ttu-id="dc9fe-442">メソッド disabledImage</span><span class="sxs-lookup"><span data-stu-id="dc9fe-442">Method disabledImage</span></span>

<span data-ttu-id="dc9fe-443">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-443">Gets or sets the disabled image of the button.</span></span>

```xpp
public str disabledImage([str value])
```

### <a name="parameters---disabledimage"></a><span data-ttu-id="dc9fe-444">パラメーター - disabledImage</span><span class="sxs-lookup"><span data-stu-id="dc9fe-444">Parameters - disabledImage</span></span>

<span data-ttu-id="dc9fe-445">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-445">value</span></span>  

### <a name="return-value---disabledimage"></a><span data-ttu-id="dc9fe-446">戻り値 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="dc9fe-446">Return Value - disabledImage</span></span>

<span data-ttu-id="dc9fe-447">画像ファイルのフル ネーム。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-447">The full name of an image file.</span></span> <span data-ttu-id="dc9fe-448">システムは、GDI でサポートされているすべてのイメージ形式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-448">The system supports all of the GDI-supported image formats.</span></span>

### <a name="remarks---disabledimage"></a><span data-ttu-id="dc9fe-449">備考 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="dc9fe-449">Remarks - disabledImage</span></span>

<span data-ttu-id="dc9fe-450">このプロパティは、disabledResource プロパティに優先します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-450">This property has precedence over the disabledResource property .</span></span> <span data-ttu-id="dc9fe-451">これらのプロパティの両方が設定されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-451">It is used if both of these properties are set.</span></span>

## <a name="method-disabledimagelocation"></a><span data-ttu-id="dc9fe-452">メソッド disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="dc9fe-452">Method disabledImageLocation</span></span>

```xpp
public int disabledImageLocation([int value])
```

### <a name="parameters---disabledimagelocation"></a><span data-ttu-id="dc9fe-453">パラメーター - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="dc9fe-453">Parameters - disabledImageLocation</span></span>

<span data-ttu-id="dc9fe-454">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-454">value</span></span>  

### <a name="return-value---disabledimagelocation"></a><span data-ttu-id="dc9fe-455">戻り値 - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="dc9fe-455">Return Value - disabledImageLocation</span></span>

## <a name="method-disabledresource"></a><span data-ttu-id="dc9fe-456">メソッド disabledResource</span><span class="sxs-lookup"><span data-stu-id="dc9fe-456">Method disabledResource</span></span>

<span data-ttu-id="dc9fe-457">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-457">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>

```xpp
public int disabledResource([int value])
```

### <a name="parameters---disabledresource"></a><span data-ttu-id="dc9fe-458">パラメーター - disabledResource</span><span class="sxs-lookup"><span data-stu-id="dc9fe-458">Parameters - disabledResource</span></span>

<span data-ttu-id="dc9fe-459">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-459">value</span></span>  

### <a name="return-value---disabledresource"></a><span data-ttu-id="dc9fe-460">戻り値 - disabledResource</span><span class="sxs-lookup"><span data-stu-id="dc9fe-460">Return Value - disabledResource</span></span>

<span data-ttu-id="dc9fe-461">無効なボタン画像として使用する画像リソース ID。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-461">The resource ID of the image to use as the disabled button image.</span></span> <span data-ttu-id="dc9fe-462">アイコンとビットマップ イメージの両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-462">Both icon and bitmap images are supported.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="dc9fe-463">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="dc9fe-463">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="dc9fe-464">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="dc9fe-464">Parameters - displayTarget</span></span>

<span data-ttu-id="dc9fe-465">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-465">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="dc9fe-466">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="dc9fe-466">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="dc9fe-467">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="dc9fe-467">Method dragDrop</span></span>

<span data-ttu-id="dc9fe-468">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-468">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="dc9fe-469">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="dc9fe-469">Parameters - dragDrop</span></span>

<span data-ttu-id="dc9fe-470">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-470">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="dc9fe-471">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="dc9fe-471">Return Value - dragDrop</span></span>

<span data-ttu-id="dc9fe-472">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-472">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="dc9fe-473">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="dc9fe-473">Method enabled</span></span>

<span data-ttu-id="dc9fe-474">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-474">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="dc9fe-475">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="dc9fe-475">Parameters - enabled</span></span>

<span data-ttu-id="dc9fe-476">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-476">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="dc9fe-477">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="dc9fe-477">Return Value - enabled</span></span>

<span data-ttu-id="dc9fe-478">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-478">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="dc9fe-479">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="dc9fe-479">Remarks - enabled</span></span>

<span data-ttu-id="dc9fe-480">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-480">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="dc9fe-481">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-481">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="dc9fe-482">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-482">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="dc9fe-483">メソッド font</span><span class="sxs-lookup"><span data-stu-id="dc9fe-483">Method font</span></span>

<span data-ttu-id="dc9fe-484">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-484">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="dc9fe-485">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="dc9fe-485">Parameters - font</span></span>

<span data-ttu-id="dc9fe-486">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-486">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="dc9fe-487">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="dc9fe-487">Return Value - font</span></span>

<span data-ttu-id="dc9fe-488">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-488">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="dc9fe-489">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="dc9fe-489">Method fontSize</span></span>

<span data-ttu-id="dc9fe-490">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-490">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="dc9fe-491">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="dc9fe-491">Parameters - fontSize</span></span>

<span data-ttu-id="dc9fe-492">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-492">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="dc9fe-493">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="dc9fe-493">Return Value - fontSize</span></span>

<span data-ttu-id="dc9fe-494">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-494">The height of the font in points.</span></span>

## <a name="method-forcedtooverflow"></a><span data-ttu-id="dc9fe-495">メソッド forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="dc9fe-495">Method forcedToOverflow</span></span>

```xpp
public boolean forcedToOverflow([boolean value])
```

### <a name="parameters---forcedtooverflow"></a><span data-ttu-id="dc9fe-496">パラメーター - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="dc9fe-496">Parameters - forcedToOverflow</span></span>

<span data-ttu-id="dc9fe-497">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-497">value</span></span>  

### <a name="return-value---forcedtooverflow"></a><span data-ttu-id="dc9fe-498">戻り値 - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="dc9fe-498">Return Value - forcedToOverflow</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="dc9fe-499">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="dc9fe-499">Method foregroundColor</span></span>

<span data-ttu-id="dc9fe-500">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-500">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="dc9fe-501">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="dc9fe-501">Parameters - foregroundColor</span></span>

<span data-ttu-id="dc9fe-502">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-502">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="dc9fe-503">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="dc9fe-503">Return Value - foregroundColor</span></span>

<span data-ttu-id="dc9fe-504">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-504">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="dc9fe-505">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="dc9fe-505">Remarks - foregroundColor</span></span>

<span data-ttu-id="dc9fe-506">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-506">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="dc9fe-507">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-507">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="dc9fe-508">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-508">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="dc9fe-509">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-509">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="dc9fe-510">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-510">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="dc9fe-511">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-511">The maximum value for a single byte is 255.</span></span>

## <a name="method-height"></a><span data-ttu-id="dc9fe-512">メソッド height</span><span class="sxs-lookup"><span data-stu-id="dc9fe-512">Method height</span></span>

<span data-ttu-id="dc9fe-513">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-513">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="dc9fe-514">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="dc9fe-514">Parameters - height</span></span>

<span data-ttu-id="dc9fe-515">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-515">value</span></span>  

<!-- -->

<span data-ttu-id="dc9fe-516">モード</span><span class="sxs-lookup"><span data-stu-id="dc9fe-516">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="dc9fe-517">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="dc9fe-517">Return Value - height</span></span>

<span data-ttu-id="dc9fe-518">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-518">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="dc9fe-519">備考 - height</span><span class="sxs-lookup"><span data-stu-id="dc9fe-519">Remarks - height</span></span>

<span data-ttu-id="dc9fe-520">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-520">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="dc9fe-521">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="dc9fe-521">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="dc9fe-522">モード。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-522">Mode.</span></span>            | <span data-ttu-id="dc9fe-523">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-523">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9fe-524">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-524">-1 Exact.</span></span>        | <span data-ttu-id="dc9fe-525">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-525">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="dc9fe-526">0 自動。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-526">0 Auto.</span></span>          | <span data-ttu-id="dc9fe-527">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-527">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="dc9fe-528">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-528">1 Column height.</span></span> | <span data-ttu-id="dc9fe-529">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-529">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="dc9fe-530">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-530">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="dc9fe-531">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="dc9fe-531">Method heightMode</span></span>

<span data-ttu-id="dc9fe-532">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-532">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="dc9fe-533">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="dc9fe-533">Parameters - heightMode</span></span>

<span data-ttu-id="dc9fe-534">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-534">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="dc9fe-535">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="dc9fe-535">Return Value - heightMode</span></span>

<span data-ttu-id="dc9fe-536">計算モード。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-536">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="dc9fe-537">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="dc9fe-537">Remarks - heightMode</span></span>

<span data-ttu-id="dc9fe-538">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="dc9fe-538">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="dc9fe-539">モード。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-539">Mode.</span></span>          | <span data-ttu-id="dc9fe-540">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-540">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9fe-541">正確。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-541">Exact.</span></span>         | <span data-ttu-id="dc9fe-542">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-542">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="dc9fe-543">自動。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-543">Auto.</span></span>          | <span data-ttu-id="dc9fe-544">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-544">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="dc9fe-545">列の高さ</span><span class="sxs-lookup"><span data-stu-id="dc9fe-545">Column height.</span></span> | <span data-ttu-id="dc9fe-546">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-546">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="dc9fe-547">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-547">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="dc9fe-548">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-548">Method heightValue</span></span>

<span data-ttu-id="dc9fe-549">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-549">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="dc9fe-550">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-550">Parameters - heightValue</span></span>

<span data-ttu-id="dc9fe-551">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-551">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="dc9fe-552">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-552">Return Value - heightValue</span></span>

<span data-ttu-id="dc9fe-553">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-553">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="dc9fe-554">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-554">Remarks - heightValue</span></span>

<span data-ttu-id="dc9fe-555">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-555">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="dc9fe-556">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="dc9fe-556">Method helpText</span></span>

<span data-ttu-id="dc9fe-557">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-557">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="dc9fe-558">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="dc9fe-558">Parameters - helpText</span></span>

<span data-ttu-id="dc9fe-559">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-559">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="dc9fe-560">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="dc9fe-560">Return Value - helpText</span></span>

<span data-ttu-id="dc9fe-561">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-561">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="dc9fe-562">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="dc9fe-562">Remarks - helpText</span></span>

<span data-ttu-id="dc9fe-563">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-563">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="dc9fe-564">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-564">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="dc9fe-565">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="dc9fe-565">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="dc9fe-566">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="dc9fe-566">Parameters - hierarchyParent</span></span>

<span data-ttu-id="dc9fe-567">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-567">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="dc9fe-568">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="dc9fe-568">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="dc9fe-569">メソッド id</span><span class="sxs-lookup"><span data-stu-id="dc9fe-569">Method id</span></span>

<span data-ttu-id="dc9fe-570">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-570">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="dc9fe-571">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="dc9fe-571">Return Value - id</span></span>

<span data-ttu-id="dc9fe-572">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-572">The ID of the control.</span></span>

## <a name="method-imagelocation"></a><span data-ttu-id="dc9fe-573">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="dc9fe-573">Method imageLocation</span></span>

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a><span data-ttu-id="dc9fe-574">パラメーター - imageLocation</span><span class="sxs-lookup"><span data-stu-id="dc9fe-574">Parameters - imageLocation</span></span>

<span data-ttu-id="dc9fe-575">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-575">value</span></span>  

### <a name="return-value---imagelocation"></a><span data-ttu-id="dc9fe-576">戻り値 - imageLocation</span><span class="sxs-lookup"><span data-stu-id="dc9fe-576">Return Value - imageLocation</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="dc9fe-577">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="dc9fe-577">Method isContainer</span></span>

<span data-ttu-id="dc9fe-578">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-578">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="dc9fe-579">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="dc9fe-579">Return Value - isContainer</span></span>

<span data-ttu-id="dc9fe-580">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-580">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="dc9fe-581">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="dc9fe-581">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="dc9fe-582">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="dc9fe-582">Parameters - italic</span></span>

<span data-ttu-id="dc9fe-583">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-583">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="dc9fe-584">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="dc9fe-584">Return Value - italic</span></span>

## <a name="method-keytip"></a><span data-ttu-id="dc9fe-585">メソッド keyTip</span><span class="sxs-lookup"><span data-stu-id="dc9fe-585">Method keyTip</span></span>

```xpp
public str keyTip([str value])
```

### <a name="parameters---keytip"></a><span data-ttu-id="dc9fe-586">パラメーター - keyTip</span><span class="sxs-lookup"><span data-stu-id="dc9fe-586">Parameters - keyTip</span></span>

<span data-ttu-id="dc9fe-587">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-587">value</span></span>  

### <a name="return-value---keytip"></a><span data-ttu-id="dc9fe-588">戻り値 - keyTip</span><span class="sxs-lookup"><span data-stu-id="dc9fe-588">Return Value - keyTip</span></span>

## <a name="method-left"></a><span data-ttu-id="dc9fe-589">メソッド left</span><span class="sxs-lookup"><span data-stu-id="dc9fe-589">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="dc9fe-590">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="dc9fe-590">Parameters - left</span></span>

<span data-ttu-id="dc9fe-591">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-591">value</span></span>  

<!-- -->

<span data-ttu-id="dc9fe-592">モード</span><span class="sxs-lookup"><span data-stu-id="dc9fe-592">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="dc9fe-593">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="dc9fe-593">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="dc9fe-594">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="dc9fe-594">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="dc9fe-595">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="dc9fe-595">Parameters - leftMode</span></span>

<span data-ttu-id="dc9fe-596">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-596">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="dc9fe-597">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="dc9fe-597">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="dc9fe-598">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-598">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="dc9fe-599">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-599">Parameters - leftValue</span></span>

<span data-ttu-id="dc9fe-600">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-600">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="dc9fe-601">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-601">Return Value - leftValue</span></span>

## <a name="method-multiselect"></a><span data-ttu-id="dc9fe-602">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="dc9fe-602">Method multiSelect</span></span>

```xpp
public int multiSelect([int value])
```

### <a name="parameters---multiselect"></a><span data-ttu-id="dc9fe-603">パラメーター - multiSelect</span><span class="sxs-lookup"><span data-stu-id="dc9fe-603">Parameters - multiSelect</span></span>

<span data-ttu-id="dc9fe-604">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-604">value</span></span>  

### <a name="return-value---multiselect"></a><span data-ttu-id="dc9fe-605">戻り値 - multiSelect</span><span class="sxs-lookup"><span data-stu-id="dc9fe-605">Return Value - multiSelect</span></span>

## <a name="method-name"></a><span data-ttu-id="dc9fe-606">メソッド名</span><span class="sxs-lookup"><span data-stu-id="dc9fe-606">Method name</span></span>

<span data-ttu-id="dc9fe-607">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-607">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="dc9fe-608">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="dc9fe-608">Parameters - name</span></span>

<span data-ttu-id="dc9fe-609">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-609">value</span></span>  
<span data-ttu-id="dc9fe-610">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-610">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="dc9fe-611">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="dc9fe-611">Return Value - name</span></span>

<span data-ttu-id="dc9fe-612">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-612">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="dc9fe-613">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="dc9fe-613">Remarks - name</span></span>

<span data-ttu-id="dc9fe-614">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-614">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="dc9fe-615">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-615">It must start with a letter.</span></span>
-   <span data-ttu-id="dc9fe-616">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-616">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="dc9fe-617">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-617">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="dc9fe-618">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-618">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="dc9fe-619">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-619">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="dc9fe-620">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="dc9fe-620">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="dc9fe-621">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="dc9fe-621">Parameters - neededPermission</span></span>

<span data-ttu-id="dc9fe-622">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-622">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="dc9fe-623">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="dc9fe-623">Return Value - neededPermission</span></span>

## <a name="method-needsrecord"></a><span data-ttu-id="dc9fe-624">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="dc9fe-624">Method needsRecord</span></span>

```xpp
public int needsRecord([int value])
```

### <a name="parameters---needsrecord"></a><span data-ttu-id="dc9fe-625">パラメーター - needsRecord</span><span class="sxs-lookup"><span data-stu-id="dc9fe-625">Parameters - needsRecord</span></span>

<span data-ttu-id="dc9fe-626">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-626">value</span></span>  

### <a name="return-value---needsrecord"></a><span data-ttu-id="dc9fe-627">戻り値 - needsRecord</span><span class="sxs-lookup"><span data-stu-id="dc9fe-627">Return Value - needsRecord</span></span>

## <a name="method-normalimage"></a><span data-ttu-id="dc9fe-628">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="dc9fe-628">Method normalImage</span></span>

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a><span data-ttu-id="dc9fe-629">パラメーター - normalImage</span><span class="sxs-lookup"><span data-stu-id="dc9fe-629">Parameters - normalImage</span></span>

<span data-ttu-id="dc9fe-630">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-630">value</span></span>  

### <a name="return-value---normalimage"></a><span data-ttu-id="dc9fe-631">戻り値 - normalImage</span><span class="sxs-lookup"><span data-stu-id="dc9fe-631">Return Value - normalImage</span></span>

## <a name="method-normalresource"></a><span data-ttu-id="dc9fe-632">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="dc9fe-632">Method normalResource</span></span>

```xpp
public int normalResource([int value])
```

### <a name="parameters---normalresource"></a><span data-ttu-id="dc9fe-633">パラメーター - normalResource</span><span class="sxs-lookup"><span data-stu-id="dc9fe-633">Parameters - normalResource</span></span>

<span data-ttu-id="dc9fe-634">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-634">value</span></span>  

### <a name="return-value---normalresource"></a><span data-ttu-id="dc9fe-635">戻り値 - normalResource</span><span class="sxs-lookup"><span data-stu-id="dc9fe-635">Return Value - normalResource</span></span>

## <a name="method-primary"></a><span data-ttu-id="dc9fe-636">メソッド primary</span><span class="sxs-lookup"><span data-stu-id="dc9fe-636">Method primary</span></span>

```xpp
public boolean primary([boolean value])
```

### <a name="parameters---primary"></a><span data-ttu-id="dc9fe-637">パラメーター - primary</span><span class="sxs-lookup"><span data-stu-id="dc9fe-637">Parameters - primary</span></span>

<span data-ttu-id="dc9fe-638">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-638">value</span></span>  

### <a name="return-value---primary"></a><span data-ttu-id="dc9fe-639">戻り値 - primary</span><span class="sxs-lookup"><span data-stu-id="dc9fe-639">Return Value - primary</span></span>

## <a name="method-saverecord"></a><span data-ttu-id="dc9fe-640">メソッド saveRecord</span><span class="sxs-lookup"><span data-stu-id="dc9fe-640">Method saveRecord</span></span>

```xpp
public boolean saveRecord([boolean value])
```

### <a name="parameters---saverecord"></a><span data-ttu-id="dc9fe-641">パラメーター - saveRecord</span><span class="sxs-lookup"><span data-stu-id="dc9fe-641">Parameters - saveRecord</span></span>

<span data-ttu-id="dc9fe-642">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-642">value</span></span>  

### <a name="return-value---saverecord"></a><span data-ttu-id="dc9fe-643">戻り値 - saveRecord</span><span class="sxs-lookup"><span data-stu-id="dc9fe-643">Return Value - saveRecord</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="dc9fe-644">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="dc9fe-644">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="dc9fe-645">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="dc9fe-645">Parameters - securityKey</span></span>

<span data-ttu-id="dc9fe-646">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-646">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="dc9fe-647">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="dc9fe-647">Return Value - securityKey</span></span>

## <a name="method-shortkey"></a><span data-ttu-id="dc9fe-648">メソッド shortkey</span><span class="sxs-lookup"><span data-stu-id="dc9fe-648">Method shortkey</span></span>

```xpp
public int shortkey([int value])
```

### <a name="parameters---shortkey"></a><span data-ttu-id="dc9fe-649">パラメーター - shortkey</span><span class="sxs-lookup"><span data-stu-id="dc9fe-649">Parameters - shortkey</span></span>

<span data-ttu-id="dc9fe-650">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-650">value</span></span>  

### <a name="return-value---shortkey"></a><span data-ttu-id="dc9fe-651">戻り値 - shortkey</span><span class="sxs-lookup"><span data-stu-id="dc9fe-651">Return Value - shortkey</span></span>

## <a name="method-showshortcut"></a><span data-ttu-id="dc9fe-652">メソッド showShortCut</span><span class="sxs-lookup"><span data-stu-id="dc9fe-652">Method showShortCut</span></span>

```xpp
public boolean showShortCut([boolean value])
```

### <a name="parameters---showshortcut"></a><span data-ttu-id="dc9fe-653">パラメーター - showShortCut</span><span class="sxs-lookup"><span data-stu-id="dc9fe-653">Parameters - showShortCut</span></span>

<span data-ttu-id="dc9fe-654">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-654">value</span></span>  

### <a name="return-value---showshortcut"></a><span data-ttu-id="dc9fe-655">戻り値 - showShortCut</span><span class="sxs-lookup"><span data-stu-id="dc9fe-655">Return Value - showShortCut</span></span>

## <a name="method-skip"></a><span data-ttu-id="dc9fe-656">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="dc9fe-656">Method skip</span></span>

<span data-ttu-id="dc9fe-657">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-657">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="dc9fe-658">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="dc9fe-658">Parameters - skip</span></span>

<span data-ttu-id="dc9fe-659">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-659">value</span></span>  
<span data-ttu-id="dc9fe-660">コントロールの skip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-660">The value to assign to the skip property of the control.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="dc9fe-661">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="dc9fe-661">Return Value - skip</span></span>

<span data-ttu-id="dc9fe-662">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-662">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-style"></a><span data-ttu-id="dc9fe-663">メソッド style</span><span class="sxs-lookup"><span data-stu-id="dc9fe-663">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="dc9fe-664">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="dc9fe-664">Parameters - style</span></span>

<span data-ttu-id="dc9fe-665">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-665">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="dc9fe-666">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="dc9fe-666">Return Value - style</span></span>

## <a name="method-text"></a><span data-ttu-id="dc9fe-667">メソッド text</span><span class="sxs-lookup"><span data-stu-id="dc9fe-667">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="dc9fe-668">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="dc9fe-668">Parameters - text</span></span>

<span data-ttu-id="dc9fe-669">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-669">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="dc9fe-670">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="dc9fe-670">Return Value - text</span></span>

## <a name="method-togglebutton"></a><span data-ttu-id="dc9fe-671">メソッド toggleButton</span><span class="sxs-lookup"><span data-stu-id="dc9fe-671">Method toggleButton</span></span>

```xpp
public int toggleButton([int value])
```

### <a name="parameters---togglebutton"></a><span data-ttu-id="dc9fe-672">パラメーター - toggleButton</span><span class="sxs-lookup"><span data-stu-id="dc9fe-672">Parameters - toggleButton</span></span>

<span data-ttu-id="dc9fe-673">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-673">value</span></span>  

### <a name="return-value---togglebutton"></a><span data-ttu-id="dc9fe-674">戻り値 - toggleButton</span><span class="sxs-lookup"><span data-stu-id="dc9fe-674">Return Value - toggleButton</span></span>

## <a name="method-togglevalue"></a><span data-ttu-id="dc9fe-675">メソッド toggleValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-675">Method toggleValue</span></span>

```xpp
public int toggleValue([int value])
```

### <a name="parameters---togglevalue"></a><span data-ttu-id="dc9fe-676">パラメーター - toggleValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-676">Parameters - toggleValue</span></span>

<span data-ttu-id="dc9fe-677">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-677">value</span></span>  

### <a name="return-value---togglevalue"></a><span data-ttu-id="dc9fe-678">戻り値 - toggleValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-678">Return Value - toggleValue</span></span>

## <a name="method-top"></a><span data-ttu-id="dc9fe-679">メソッド top</span><span class="sxs-lookup"><span data-stu-id="dc9fe-679">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="dc9fe-680">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="dc9fe-680">Parameters - top</span></span>

<span data-ttu-id="dc9fe-681">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-681">value</span></span>  

<!-- -->

<span data-ttu-id="dc9fe-682">モード</span><span class="sxs-lookup"><span data-stu-id="dc9fe-682">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="dc9fe-683">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="dc9fe-683">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="dc9fe-684">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="dc9fe-684">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="dc9fe-685">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="dc9fe-685">Parameters - topMode</span></span>

<span data-ttu-id="dc9fe-686">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-686">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="dc9fe-687">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="dc9fe-687">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="dc9fe-688">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-688">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="dc9fe-689">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-689">Parameters - topValue</span></span>

<span data-ttu-id="dc9fe-690">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-690">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="dc9fe-691">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-691">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="dc9fe-692">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="dc9fe-692">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="dc9fe-693">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="dc9fe-693">Parameters - type</span></span>

<span data-ttu-id="dc9fe-694">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-694">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="dc9fe-695">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="dc9fe-695">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="dc9fe-696">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="dc9fe-696">Method underline</span></span>

<span data-ttu-id="dc9fe-697">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-697">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="dc9fe-698">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="dc9fe-698">Parameters - underline</span></span>

<span data-ttu-id="dc9fe-699">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-699">value</span></span>  
<span data-ttu-id="dc9fe-700">コントロールの underline プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-700">The value to assign to the underline property of the control.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="dc9fe-701">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="dc9fe-701">Return Value - underline</span></span>

<span data-ttu-id="dc9fe-702">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-702">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-userdata"></a><span data-ttu-id="dc9fe-703">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="dc9fe-703">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="dc9fe-704">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="dc9fe-704">Parameters - userData</span></span>

<span data-ttu-id="dc9fe-705">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-705">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="dc9fe-706">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="dc9fe-706">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="dc9fe-707">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="dc9fe-707">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="dc9fe-708">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="dc9fe-708">Parameters - userDataItem</span></span>

<span data-ttu-id="dc9fe-709">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-709">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="dc9fe-710">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="dc9fe-710">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="dc9fe-711">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="dc9fe-711">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="dc9fe-712">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="dc9fe-712">Parameters - userDataItems</span></span>

<span data-ttu-id="dc9fe-713">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-713">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="dc9fe-714">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="dc9fe-714">Return Value - userDataItems</span></span>

## <a name="method-value"></a><span data-ttu-id="dc9fe-715">メソッド value</span><span class="sxs-lookup"><span data-stu-id="dc9fe-715">Method value</span></span>

```xpp
public boolean value([boolean value])
```

### <a name="parameters---value"></a><span data-ttu-id="dc9fe-716">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="dc9fe-716">Parameters - value</span></span>

<span data-ttu-id="dc9fe-717">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-717">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="dc9fe-718">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="dc9fe-718">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="dc9fe-719">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="dc9fe-719">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="dc9fe-720">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="dc9fe-720">Parameters - verticalSpacing</span></span>

<span data-ttu-id="dc9fe-721">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-721">value</span></span>  

<!-- -->

<span data-ttu-id="dc9fe-722">モード</span><span class="sxs-lookup"><span data-stu-id="dc9fe-722">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="dc9fe-723">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="dc9fe-723">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="dc9fe-724">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="dc9fe-724">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="dc9fe-725">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="dc9fe-725">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="dc9fe-726">モード</span><span class="sxs-lookup"><span data-stu-id="dc9fe-726">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="dc9fe-727">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="dc9fe-727">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="dc9fe-728">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-728">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="dc9fe-729">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-729">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="dc9fe-730">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-730">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="dc9fe-731">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-731">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="dc9fe-732">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="dc9fe-732">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="dc9fe-733">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="dc9fe-733">Parameters - visible</span></span>

<span data-ttu-id="dc9fe-734">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-734">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="dc9fe-735">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="dc9fe-735">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="dc9fe-736">メソッド width</span><span class="sxs-lookup"><span data-stu-id="dc9fe-736">Method width</span></span>

<span data-ttu-id="dc9fe-737">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-737">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="dc9fe-738">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="dc9fe-738">Parameters - width</span></span>

<span data-ttu-id="dc9fe-739">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-739">value</span></span>  

<!-- -->

<span data-ttu-id="dc9fe-740">モード</span><span class="sxs-lookup"><span data-stu-id="dc9fe-740">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="dc9fe-741">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="dc9fe-741">Return Value - width</span></span>

<span data-ttu-id="dc9fe-742">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-742">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="dc9fe-743">備考 - width</span><span class="sxs-lookup"><span data-stu-id="dc9fe-743">Remarks - width</span></span>

<span data-ttu-id="dc9fe-744">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-744">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="dc9fe-745">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="dc9fe-745">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="dc9fe-746">モード。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-746">Mode.</span></span>           | <span data-ttu-id="dc9fe-747">幅計算。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-747">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9fe-748">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-748">-1 Exact.</span></span>       | <span data-ttu-id="dc9fe-749">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-749">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="dc9fe-750">0 自動。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-750">0 Auto.</span></span>         | <span data-ttu-id="dc9fe-751">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-751">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="dc9fe-752">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-752">1 Column width.</span></span> | <span data-ttu-id="dc9fe-753">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-753">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="dc9fe-754">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-754">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="dc9fe-755">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="dc9fe-755">Method widthMode</span></span>

<span data-ttu-id="dc9fe-756">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-756">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="dc9fe-757">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-757">Parameters - widthMode</span></span>

<span data-ttu-id="dc9fe-758">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-758">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="dc9fe-759">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="dc9fe-759">Return Value - widthMode</span></span>

<span data-ttu-id="dc9fe-760">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-760">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="dc9fe-761">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="dc9fe-761">Remarks - widthMode</span></span>

<span data-ttu-id="dc9fe-762">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="dc9fe-762">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="dc9fe-763">モード。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-763">Mode.</span></span>         | <span data-ttu-id="dc9fe-764">幅計算。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-764">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9fe-765">正確。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-765">Exact.</span></span>        | <span data-ttu-id="dc9fe-766">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-766">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="dc9fe-767">自動。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-767">Auto.</span></span>         | <span data-ttu-id="dc9fe-768">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-768">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="dc9fe-769">列の幅。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-769">Column width.</span></span> | <span data-ttu-id="dc9fe-770">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-770">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="dc9fe-771">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-771">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="dc9fe-772">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-772">Method widthValue</span></span>

<span data-ttu-id="dc9fe-773">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-773">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="dc9fe-774">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-774">Parameters - widthValue</span></span>

<span data-ttu-id="dc9fe-775">値</span><span class="sxs-lookup"><span data-stu-id="dc9fe-775">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="dc9fe-776">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-776">Return Value - widthValue</span></span>

<span data-ttu-id="dc9fe-777">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-777">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="dc9fe-778">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="dc9fe-778">Remarks - widthValue</span></span>

<span data-ttu-id="dc9fe-779">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="dc9fe-779">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="dc9fe-780">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="dc9fe-780">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="dc9fe-781">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="dc9fe-781">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="dc9fe-782">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="dc9fe-782">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="dc9fe-783">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="dc9fe-783">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="dc9fe-784">overrideObject</span><span class="sxs-lookup"><span data-stu-id="dc9fe-784">overrideObject</span></span>  

