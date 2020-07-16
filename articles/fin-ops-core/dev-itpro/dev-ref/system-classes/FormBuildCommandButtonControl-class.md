---
title: FormBuildCommandButtonControl クラス
description: このトピックでは、FormBuildCommandButtonControl クラスについて説明します。
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
ms.openlocfilehash: 7cebcac2d66214b4b5b9ff3a0ded7af6f0ed19ce
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502972"
---
# <a name="class-formbuildcommandbuttoncontrol"></a><span data-ttu-id="59272-103">クラス FormBuildCommandButtonControl</span><span class="sxs-lookup"><span data-stu-id="59272-103">Class FormBuildCommandButtonControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildCommandButtonControl extends FormBuildControl
```

<span data-ttu-id="59272-104">FormBuildCommandButtonControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="59272-104">The FormBuildCommandButtonControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="59272-105">備考</span><span class="sxs-lookup"><span data-stu-id="59272-105">Remarks</span></span>

<span data-ttu-id="59272-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="59272-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="59272-107">例</span><span class="sxs-lookup"><span data-stu-id="59272-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="59272-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="59272-108">Methods</span></span>

| <span data-ttu-id="59272-109">方法</span><span class="sxs-lookup"><span data-stu-id="59272-109">Method</span></span>                                                                                                      | <span data-ttu-id="59272-110">説明</span><span class="sxs-lookup"><span data-stu-id="59272-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59272-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="59272-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="59272-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="59272-112">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="59272-113">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-113">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="59272-114">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="59272-114">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="59272-115">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="59272-115">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="59272-116">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="59272-116">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="59272-117">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="59272-117">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="59272-118">public boolean autoRefreshData(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="59272-118">public boolean autoRefreshData(\[boolean value\])</span></span>                                                           |                                                                                                                                         |
| <span data-ttu-id="59272-119">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-119">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="59272-120">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-120">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="59272-121">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-121">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="59272-122">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="59272-122">Determines whether the control background can be transparent.</span></span>                                                                          |
| <span data-ttu-id="59272-123">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="59272-123">public boolean big(\[boolean value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="59272-124">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-124">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="59272-125">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-125">Gets or sets the weight of font used to output text in the control.</span></span>                                                                     |
| <span data-ttu-id="59272-126">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-126">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="59272-127">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-127">Gets or sets the style of the borderline of the control.</span></span>                                                                                |
| <span data-ttu-id="59272-128">public int buttonDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-128">public int buttonDisplay(\[int value\])</span></span>                                                                     | <span data-ttu-id="59272-129">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-129">Gets or sets the appearance of the button control.</span></span>                                                                                      |
| <span data-ttu-id="59272-130">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="59272-130">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="59272-131">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-131">Gets or set the caption of the control.</span></span>                                                                                                 |
| <span data-ttu-id="59272-132">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-132">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="59272-133">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-133">Gets or sets the character set of the font.</span></span>                                                                                             |
| <span data-ttu-id="59272-134">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-134">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="59272-135">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-135">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="59272-136">public int command(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-136">public int command(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="59272-137">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="59272-137">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="59272-138">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-138">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="59272-139">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="59272-139">public int containerId()</span></span>                                                                                    | <span data-ttu-id="59272-140">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="59272-140">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="59272-141">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="59272-141">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="59272-142">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="59272-142">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="59272-143">public boolean defaultButton(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="59272-143">public boolean defaultButton(\[boolean value\])</span></span>                                                             | <span data-ttu-id="59272-144">ボタンをフォーム上の既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="59272-144">Determines whether the button should be the default button on the form.</span></span>                                                                 |
| <span data-ttu-id="59272-145">public str disabledImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="59272-145">public str disabledImage(\[str value\])</span></span>                                                                     | <span data-ttu-id="59272-146">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-146">Gets or sets the disabled image of the button.</span></span>                                                                                          |
| <span data-ttu-id="59272-147">public int disabledImageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-147">public int disabledImageLocation(\[int value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="59272-148">public int disabledResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-148">public int disabledResource(\[int value\])</span></span>                                                                  | <span data-ttu-id="59272-149">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-149">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>                                                          |
| <span data-ttu-id="59272-150">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-150">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="59272-151">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-151">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="59272-152">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="59272-152">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="59272-153">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="59272-153">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="59272-154">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="59272-154">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="59272-155">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="59272-155">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="59272-156">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-156">Gets or sets the name of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="59272-157">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-157">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="59272-158">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-158">Gets or sets the size of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="59272-159">public boolean forcedToOverflow(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="59272-159">public boolean forcedToOverflow(\[boolean value\])</span></span>                                                          |                                                                                                                                         |
| <span data-ttu-id="59272-160">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-160">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="59272-161">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-161">Gets or sets the text color for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="59272-162">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="59272-162">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="59272-163">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-163">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="59272-164">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-164">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="59272-165">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-165">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="59272-166">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-166">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="59272-167">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-167">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="59272-168">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="59272-168">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="59272-169">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-169">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="59272-170">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="59272-170">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="59272-171">public int id()</span><span class="sxs-lookup"><span data-stu-id="59272-171">public int id()</span></span>                                                                                             | <span data-ttu-id="59272-172">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="59272-172">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="59272-173">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-173">public int imageLocation(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="59272-174">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="59272-174">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="59272-175">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="59272-175">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="59272-176">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="59272-176">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="59272-177">public str keyTip(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="59272-177">public str keyTip(\[str value\])</span></span>                                                                            |                                                                                                                                         |
| <span data-ttu-id="59272-178">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="59272-178">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="59272-179">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-179">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="59272-180">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-180">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="59272-181">public int multiSelect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-181">public int multiSelect(\[int value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="59272-182">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="59272-182">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="59272-183">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-183">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="59272-184">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-184">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="59272-185">public int needsRecord(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-185">public int needsRecord(\[int value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="59272-186">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="59272-186">public str normalImage(\[str value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="59272-187">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-187">public int normalResource(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="59272-188">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="59272-188">public str parameters(\[str value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="59272-189">public boolean primary(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="59272-189">public boolean primary(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="59272-190">public boolean saveRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="59272-190">public boolean saveRecord(\[boolean value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="59272-191">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="59272-191">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="59272-192">public int shortkey(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-192">public int shortkey(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="59272-193">public boolean showShortCut(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="59272-193">public boolean showShortCut(\[boolean value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="59272-194">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="59272-194">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="59272-195">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="59272-195">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="59272-196">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-196">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="59272-197">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="59272-197">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="59272-198">public int toggleButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-198">public int toggleButton(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="59272-199">public int toggleValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-199">public int toggleValue(\[int value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="59272-200">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="59272-200">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="59272-201">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-201">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="59272-202">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-202">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="59272-203">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-203">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="59272-204">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="59272-204">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="59272-205">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="59272-205">Sets or returns the underline property for the text in the control.</span></span>                                                                     |
| <span data-ttu-id="59272-206">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-206">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="59272-207">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-207">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="59272-208">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-208">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="59272-209">public boolean value(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="59272-209">public boolean value(\[boolean value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="59272-210">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="59272-210">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="59272-211">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="59272-211">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="59272-212">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-212">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="59272-213">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="59272-213">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="59272-214">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="59272-214">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="59272-215">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-215">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="59272-216">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-216">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="59272-217">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-217">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="59272-218">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="59272-218">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="59272-219">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-219">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="59272-220">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="59272-220">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="59272-221">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="59272-221">Method alignControl</span></span>

<span data-ttu-id="59272-222">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="59272-222">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="59272-223">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="59272-223">Parameters - alignControl</span></span>

<span data-ttu-id="59272-224">値</span><span class="sxs-lookup"><span data-stu-id="59272-224">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="59272-225">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="59272-225">Return Value - alignControl</span></span>

<span data-ttu-id="59272-226">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="59272-226">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="59272-227">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="59272-227">Remarks - alignControl</span></span>

<span data-ttu-id="59272-228">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="59272-228">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="59272-229">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="59272-229">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="59272-230">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="59272-230">Parameters - alignment</span></span>

<span data-ttu-id="59272-231">値</span><span class="sxs-lookup"><span data-stu-id="59272-231">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="59272-232">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="59272-232">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="59272-233">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="59272-233">Method allowEdit</span></span>

<span data-ttu-id="59272-234">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="59272-234">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="59272-235">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="59272-235">Parameters - allowEdit</span></span>

<span data-ttu-id="59272-236">値</span><span class="sxs-lookup"><span data-stu-id="59272-236">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="59272-237">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="59272-237">Return Value - allowEdit</span></span>

<span data-ttu-id="59272-238">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="59272-238">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="59272-239">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="59272-239">Remarks - allowEdit</span></span>

<span data-ttu-id="59272-240">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="59272-240">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="59272-241">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="59272-241">Method autoDeclaration</span></span>

<span data-ttu-id="59272-242">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="59272-242">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="59272-243">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="59272-243">Parameters - autoDeclaration</span></span>

<span data-ttu-id="59272-244">値</span><span class="sxs-lookup"><span data-stu-id="59272-244">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="59272-245">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="59272-245">Return Value - autoDeclaration</span></span>

<span data-ttu-id="59272-246">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="59272-246">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="59272-247">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="59272-247">Remarks - autoDeclaration</span></span>

<span data-ttu-id="59272-248">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="59272-248">Controls cannot have identical names.</span></span>

## <a name="method-autorefreshdata"></a><span data-ttu-id="59272-249">メソッド autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="59272-249">Method autoRefreshData</span></span>

```xpp
public boolean autoRefreshData([boolean value])
```

### <a name="parameters---autorefreshdata"></a><span data-ttu-id="59272-250">パラメーター - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="59272-250">Parameters - autoRefreshData</span></span>

<span data-ttu-id="59272-251">値</span><span class="sxs-lookup"><span data-stu-id="59272-251">value</span></span>  

### <a name="return-value---autorefreshdata"></a><span data-ttu-id="59272-252">戻り値 - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="59272-252">Return Value - autoRefreshData</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="59272-253">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="59272-253">Method backgroundColor</span></span>

<span data-ttu-id="59272-254">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-254">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="59272-255">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="59272-255">Parameters - backgroundColor</span></span>

<span data-ttu-id="59272-256">値</span><span class="sxs-lookup"><span data-stu-id="59272-256">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="59272-257">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="59272-257">Return Value - backgroundColor</span></span>

<span data-ttu-id="59272-258">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="59272-258">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="59272-259">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="59272-259">Remarks - backgroundColor</span></span>

<span data-ttu-id="59272-260">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="59272-260">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="59272-261">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="59272-261">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="59272-262">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="59272-262">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="59272-263">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="59272-263">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="59272-264">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="59272-264">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="59272-265">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="59272-265">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="59272-266">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="59272-266">Method backStyle</span></span>

<span data-ttu-id="59272-267">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="59272-267">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="59272-268">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="59272-268">Parameters - backStyle</span></span>

<span data-ttu-id="59272-269">値</span><span class="sxs-lookup"><span data-stu-id="59272-269">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="59272-270">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="59272-270">Return Value - backStyle</span></span>

<span data-ttu-id="59272-271">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="59272-271">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-big"></a><span data-ttu-id="59272-272">メソッド big</span><span class="sxs-lookup"><span data-stu-id="59272-272">Method big</span></span>

```xpp
public boolean big([boolean value])
```

### <a name="parameters---big"></a><span data-ttu-id="59272-273">パラメーター - big</span><span class="sxs-lookup"><span data-stu-id="59272-273">Parameters - big</span></span>

<span data-ttu-id="59272-274">値</span><span class="sxs-lookup"><span data-stu-id="59272-274">value</span></span>  

### <a name="return-value---big"></a><span data-ttu-id="59272-275">戻り値 - big</span><span class="sxs-lookup"><span data-stu-id="59272-275">Return Value - big</span></span>

## <a name="method-bold"></a><span data-ttu-id="59272-276">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="59272-276">Method bold</span></span>

<span data-ttu-id="59272-277">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-277">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="59272-278">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="59272-278">Parameters - bold</span></span>

<span data-ttu-id="59272-279">値</span><span class="sxs-lookup"><span data-stu-id="59272-279">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="59272-280">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="59272-280">Return Value - bold</span></span>

<span data-ttu-id="59272-281">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="59272-281">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="59272-282">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="59272-282">Remarks - bold</span></span>

<span data-ttu-id="59272-283">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="59272-283">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="59272-284">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="59272-284">0 Use the default font weight.</span></span>
-   <span data-ttu-id="59272-285">1 シン。</span><span class="sxs-lookup"><span data-stu-id="59272-285">1 Thin.</span></span>
-   <span data-ttu-id="59272-286">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="59272-286">2 Extra-light.</span></span>
-   <span data-ttu-id="59272-287">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="59272-287">3 Light.</span></span>
-   <span data-ttu-id="59272-288">4 標準。</span><span class="sxs-lookup"><span data-stu-id="59272-288">4 Normal.</span></span>
-   <span data-ttu-id="59272-289">5 中。</span><span class="sxs-lookup"><span data-stu-id="59272-289">5 Medium.</span></span>
-   <span data-ttu-id="59272-290">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="59272-290">6 Semibold.</span></span>
-   <span data-ttu-id="59272-291">7 太字。</span><span class="sxs-lookup"><span data-stu-id="59272-291">7 Bold.</span></span>
-   <span data-ttu-id="59272-292">8 極太。</span><span class="sxs-lookup"><span data-stu-id="59272-292">8 Extra-bold.</span></span>
-   <span data-ttu-id="59272-293">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="59272-293">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="59272-294">メソッド border</span><span class="sxs-lookup"><span data-stu-id="59272-294">Method border</span></span>

<span data-ttu-id="59272-295">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-295">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="59272-296">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="59272-296">Parameters - border</span></span>

<span data-ttu-id="59272-297">値</span><span class="sxs-lookup"><span data-stu-id="59272-297">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="59272-298">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="59272-298">Return Value - border</span></span>

<span data-ttu-id="59272-299">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="59272-299">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="59272-300">備考 - border</span><span class="sxs-lookup"><span data-stu-id="59272-300">Remarks - border</span></span>

<span data-ttu-id="59272-301">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="59272-301">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="59272-302">値です。</span><span class="sxs-lookup"><span data-stu-id="59272-302">Value.</span></span> | <span data-ttu-id="59272-303">説明。</span><span class="sxs-lookup"><span data-stu-id="59272-303">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="59272-304">0</span><span class="sxs-lookup"><span data-stu-id="59272-304">0</span></span>      | <span data-ttu-id="59272-305">自動。</span><span class="sxs-lookup"><span data-stu-id="59272-305">Auto.</span></span>        |
| <span data-ttu-id="59272-306">1</span><span class="sxs-lookup"><span data-stu-id="59272-306">1</span></span>      | <span data-ttu-id="59272-307">3D。</span><span class="sxs-lookup"><span data-stu-id="59272-307">3D.</span></span>          |
| <span data-ttu-id="59272-308">2</span><span class="sxs-lookup"><span data-stu-id="59272-308">2</span></span>      | <span data-ttu-id="59272-309">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="59272-309">Single line.</span></span> |
| <span data-ttu-id="59272-310">3</span><span class="sxs-lookup"><span data-stu-id="59272-310">3</span></span>      | <span data-ttu-id="59272-311">均一。</span><span class="sxs-lookup"><span data-stu-id="59272-311">Flat.</span></span>        |
| <span data-ttu-id="59272-312">4</span><span class="sxs-lookup"><span data-stu-id="59272-312">4</span></span>      | <span data-ttu-id="59272-313">なし。</span><span class="sxs-lookup"><span data-stu-id="59272-313">None.</span></span>        |

## <a name="method-buttondisplay"></a><span data-ttu-id="59272-314">メソッド buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="59272-314">Method buttonDisplay</span></span>

<span data-ttu-id="59272-315">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-315">Gets or sets the appearance of the button control.</span></span>

```xpp
public int buttonDisplay([int value])
```

### <a name="parameters---buttondisplay"></a><span data-ttu-id="59272-316">パラメーター - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="59272-316">Parameters - buttonDisplay</span></span>

<span data-ttu-id="59272-317">値</span><span class="sxs-lookup"><span data-stu-id="59272-317">value</span></span>  

### <a name="return-value---buttondisplay"></a><span data-ttu-id="59272-318">戻り値 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="59272-318">Return Value - buttonDisplay</span></span>

<span data-ttu-id="59272-319">ゼロから 5 までの整数。</span><span class="sxs-lookup"><span data-stu-id="59272-319">An integer between zero and five, inclusive.</span></span>

### <a name="remarks---buttondisplay"></a><span data-ttu-id="59272-320">備考 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="59272-320">Remarks - buttonDisplay</span></span>

<span data-ttu-id="59272-321">プロパティ値は、テキスト、画像、またはその両方のいずれをボタンに表示するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="59272-321">The value of the property defines whether the text, the image, or both should be displayed on the button.</span></span> <span data-ttu-id="59272-322">このプロパティは、テキストと画像の両方が表示されている場合は、テキストと画像の相対位置も制御します。</span><span class="sxs-lookup"><span data-stu-id="59272-322">This property also controls relative positions of text and image if both are displayed.</span></span> <span data-ttu-id="59272-323">返される整数値には、次のようなボタン コントロールの外観が含まれます。</span><span class="sxs-lookup"><span data-stu-id="59272-323">The integer value that is returned contains the appearance of the button control as follows.</span></span>

| <span data-ttu-id="59272-324">値です。</span><span class="sxs-lookup"><span data-stu-id="59272-324">Value.</span></span> | <span data-ttu-id="59272-325">説明。</span><span class="sxs-lookup"><span data-stu-id="59272-325">Description.</span></span>                                                     |
|--------|------------------------------------------------------------------|
| <span data-ttu-id="59272-326">0</span><span class="sxs-lookup"><span data-stu-id="59272-326">0</span></span>      | <span data-ttu-id="59272-327">テキストのみ。</span><span class="sxs-lookup"><span data-stu-id="59272-327">Text only.</span></span>                                                       |
| <span data-ttu-id="59272-328">1</span><span class="sxs-lookup"><span data-stu-id="59272-328">1</span></span>      | <span data-ttu-id="59272-329">イメージのみ。</span><span class="sxs-lookup"><span data-stu-id="59272-329">Image only.</span></span>                                                      |
| <span data-ttu-id="59272-330">2</span><span class="sxs-lookup"><span data-stu-id="59272-330">2</span></span>      | <span data-ttu-id="59272-331">テキストと画像。画像はテキストの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="59272-331">Text and image; the image is displayed below the text.</span></span>           |
| <span data-ttu-id="59272-332">3</span><span class="sxs-lookup"><span data-stu-id="59272-332">3</span></span>      | <span data-ttu-id="59272-333">テキストと画像。画像はテキストの上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="59272-333">Text and image; the image is displayed above the text.</span></span>           |
| <span data-ttu-id="59272-334">4</span><span class="sxs-lookup"><span data-stu-id="59272-334">4</span></span>      | <span data-ttu-id="59272-335">テキストと画像。画像はテキストの左に表示されます。</span><span class="sxs-lookup"><span data-stu-id="59272-335">Text and image; the image is displayed to the left of the text.</span></span>  |
| <span data-ttu-id="59272-336">5</span><span class="sxs-lookup"><span data-stu-id="59272-336">5</span></span>      | <span data-ttu-id="59272-337">テキストと画像。画像はテキストの右に表示されます。</span><span class="sxs-lookup"><span data-stu-id="59272-337">Text and image; the image is displayed to the right of the text.</span></span> |

## <a name="method-caption"></a><span data-ttu-id="59272-338">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="59272-338">Method caption</span></span>

<span data-ttu-id="59272-339">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-339">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="59272-340">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="59272-340">Parameters - caption</span></span>

<span data-ttu-id="59272-341">値</span><span class="sxs-lookup"><span data-stu-id="59272-341">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="59272-342">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="59272-342">Return Value - caption</span></span>

<span data-ttu-id="59272-343">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="59272-343">The string that is used as the caption of the control.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="59272-344">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="59272-344">Method characterSet</span></span>

<span data-ttu-id="59272-345">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-345">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="59272-346">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="59272-346">Parameters - characterSet</span></span>

<span data-ttu-id="59272-347">値</span><span class="sxs-lookup"><span data-stu-id="59272-347">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="59272-348">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="59272-348">Return Value - characterSet</span></span>

<span data-ttu-id="59272-349">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="59272-349">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="59272-350">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="59272-350">Remarks - characterSet</span></span>

<span data-ttu-id="59272-351">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="59272-351">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="59272-352">値です。</span><span class="sxs-lookup"><span data-stu-id="59272-352">Value.</span></span> | <span data-ttu-id="59272-353">説明。</span><span class="sxs-lookup"><span data-stu-id="59272-353">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="59272-354">0</span><span class="sxs-lookup"><span data-stu-id="59272-354">0</span></span>      | <span data-ttu-id="59272-355">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="59272-355">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="59272-356">1</span><span class="sxs-lookup"><span data-stu-id="59272-356">1</span></span>      | <span data-ttu-id="59272-357">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="59272-357">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="59272-358">2</span><span class="sxs-lookup"><span data-stu-id="59272-358">2</span></span>      | <span data-ttu-id="59272-359">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="59272-359">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="59272-360">77</span><span class="sxs-lookup"><span data-stu-id="59272-360">77</span></span>     | <span data-ttu-id="59272-361">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="59272-361">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="59272-362">128</span><span class="sxs-lookup"><span data-stu-id="59272-362">128</span></span>    | <span data-ttu-id="59272-363">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="59272-363">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="59272-364">129</span><span class="sxs-lookup"><span data-stu-id="59272-364">129</span></span>    | <span data-ttu-id="59272-365">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="59272-365">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="59272-366">134</span><span class="sxs-lookup"><span data-stu-id="59272-366">134</span></span>    | <span data-ttu-id="59272-367">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="59272-367">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="59272-368">136</span><span class="sxs-lookup"><span data-stu-id="59272-368">136</span></span>    | <span data-ttu-id="59272-369">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="59272-369">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="59272-370">161</span><span class="sxs-lookup"><span data-stu-id="59272-370">161</span></span>    | <span data-ttu-id="59272-371">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="59272-371">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="59272-372">162</span><span class="sxs-lookup"><span data-stu-id="59272-372">162</span></span>    | <span data-ttu-id="59272-373">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="59272-373">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="59272-374">163</span><span class="sxs-lookup"><span data-stu-id="59272-374">163</span></span>    | <span data-ttu-id="59272-375">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="59272-375">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="59272-376">186</span><span class="sxs-lookup"><span data-stu-id="59272-376">186</span></span>    | <span data-ttu-id="59272-377">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="59272-377">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="59272-378">204</span><span class="sxs-lookup"><span data-stu-id="59272-378">204</span></span>    | <span data-ttu-id="59272-379">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="59272-379">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="59272-380">238</span><span class="sxs-lookup"><span data-stu-id="59272-380">238</span></span>    | <span data-ttu-id="59272-381">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="59272-381">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="59272-382">255</span><span class="sxs-lookup"><span data-stu-id="59272-382">255</span></span>    | <span data-ttu-id="59272-383">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="59272-383">OEM\_CHARSET</span></span>         |

<span data-ttu-id="59272-384">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="59272-384">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="59272-385">値です。</span><span class="sxs-lookup"><span data-stu-id="59272-385">Value.</span></span> | <span data-ttu-id="59272-386">説明。</span><span class="sxs-lookup"><span data-stu-id="59272-386">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="59272-387">130</span><span class="sxs-lookup"><span data-stu-id="59272-387">130</span></span>    | <span data-ttu-id="59272-388">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="59272-388">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="59272-389">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="59272-389">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="59272-390">値です。</span><span class="sxs-lookup"><span data-stu-id="59272-390">Value.</span></span> | <span data-ttu-id="59272-391">説明。</span><span class="sxs-lookup"><span data-stu-id="59272-391">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="59272-392">177</span><span class="sxs-lookup"><span data-stu-id="59272-392">177</span></span>    | <span data-ttu-id="59272-393">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="59272-393">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="59272-394">178</span><span class="sxs-lookup"><span data-stu-id="59272-394">178</span></span>    | <span data-ttu-id="59272-395">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="59272-395">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="59272-396">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="59272-396">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="59272-397">値です。</span><span class="sxs-lookup"><span data-stu-id="59272-397">Value.</span></span> | <span data-ttu-id="59272-398">説明。</span><span class="sxs-lookup"><span data-stu-id="59272-398">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="59272-399">222</span><span class="sxs-lookup"><span data-stu-id="59272-399">222</span></span>    | <span data-ttu-id="59272-400">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="59272-400">THAI\_CHARSET</span></span> |

<span data-ttu-id="59272-401">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="59272-401">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="59272-402">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="59272-402">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="59272-403">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="59272-403">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="59272-404">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="59272-404">Method colorScheme</span></span>

<span data-ttu-id="59272-405">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-405">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="59272-406">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="59272-406">Parameters - colorScheme</span></span>

<span data-ttu-id="59272-407">値</span><span class="sxs-lookup"><span data-stu-id="59272-407">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="59272-408">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="59272-408">Return Value - colorScheme</span></span>

<span data-ttu-id="59272-409">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="59272-409">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="59272-410">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="59272-410">Remarks - colorScheme</span></span>

<span data-ttu-id="59272-411">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="59272-411">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="59272-412">値です。</span><span class="sxs-lookup"><span data-stu-id="59272-412">Value.</span></span> | <span data-ttu-id="59272-413">スタイル。</span><span class="sxs-lookup"><span data-stu-id="59272-413">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="59272-414">0</span><span class="sxs-lookup"><span data-stu-id="59272-414">0</span></span>      | <span data-ttu-id="59272-415">既定。</span><span class="sxs-lookup"><span data-stu-id="59272-415">Default.</span></span>                       |
| <span data-ttu-id="59272-416">1</span><span class="sxs-lookup"><span data-stu-id="59272-416">1</span></span>      | <span data-ttu-id="59272-417">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="59272-417">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="59272-418">2</span><span class="sxs-lookup"><span data-stu-id="59272-418">2</span></span>      | <span data-ttu-id="59272-419">真の配色。</span><span class="sxs-lookup"><span data-stu-id="59272-419">The true-color scheme.</span></span>         |

## <a name="method-command"></a><span data-ttu-id="59272-420">メソッド command</span><span class="sxs-lookup"><span data-stu-id="59272-420">Method command</span></span>

```xpp
public int command([int value])
```

### <a name="parameters---command"></a><span data-ttu-id="59272-421">パラメーター - command</span><span class="sxs-lookup"><span data-stu-id="59272-421">Parameters - command</span></span>

<span data-ttu-id="59272-422">値</span><span class="sxs-lookup"><span data-stu-id="59272-422">value</span></span>  

### <a name="return-value---command"></a><span data-ttu-id="59272-423">戻り値 - command</span><span class="sxs-lookup"><span data-stu-id="59272-423">Return Value - command</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="59272-424">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="59272-424">Method configurationKey</span></span>

<span data-ttu-id="59272-425">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-425">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="59272-426">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="59272-426">Parameters - configurationKey</span></span>

<span data-ttu-id="59272-427">値</span><span class="sxs-lookup"><span data-stu-id="59272-427">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="59272-428">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="59272-428">Return Value - configurationKey</span></span>

<span data-ttu-id="59272-429">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="59272-429">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="59272-430">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="59272-430">Remarks - configurationKey</span></span>

<span data-ttu-id="59272-431">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="59272-431">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="59272-432">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="59272-432">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="59272-433">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="59272-433">Method containerId</span></span>

<span data-ttu-id="59272-434">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="59272-434">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="59272-435">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="59272-435">Return Value - containerId</span></span>

<span data-ttu-id="59272-436">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="59272-436">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="59272-437">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="59272-437">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="59272-438">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="59272-438">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="59272-439">値</span><span class="sxs-lookup"><span data-stu-id="59272-439">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="59272-440">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="59272-440">Return Value - countryRegionCodes</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="59272-441">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="59272-441">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="59272-442">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="59272-442">Parameters - dataRelationPath</span></span>

<span data-ttu-id="59272-443">値</span><span class="sxs-lookup"><span data-stu-id="59272-443">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="59272-444">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="59272-444">Return Value - dataRelationPath</span></span>

## <a name="method-defaultbutton"></a><span data-ttu-id="59272-445">メソッド defaultButton</span><span class="sxs-lookup"><span data-stu-id="59272-445">Method defaultButton</span></span>

<span data-ttu-id="59272-446">ボタンをフォーム上の既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="59272-446">Determines whether the button should be the default button on the form.</span></span>

```xpp
public boolean defaultButton([boolean value])
```

### <a name="parameters---defaultbutton"></a><span data-ttu-id="59272-447">パラメーター - defaultButton</span><span class="sxs-lookup"><span data-stu-id="59272-447">Parameters - defaultButton</span></span>

<span data-ttu-id="59272-448">値</span><span class="sxs-lookup"><span data-stu-id="59272-448">value</span></span>  

### <a name="return-value---defaultbutton"></a><span data-ttu-id="59272-449">戻り値 - defaultButton</span><span class="sxs-lookup"><span data-stu-id="59272-449">Return Value - defaultButton</span></span>

<span data-ttu-id="59272-450">ボタンが既定のボタンである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="59272-450">true if the button should be the default button; otherwise, false.</span></span>

## <a name="method-disabledimage"></a><span data-ttu-id="59272-451">メソッド disabledImage</span><span class="sxs-lookup"><span data-stu-id="59272-451">Method disabledImage</span></span>

<span data-ttu-id="59272-452">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-452">Gets or sets the disabled image of the button.</span></span>

```xpp
public str disabledImage([str value])
```

### <a name="parameters---disabledimage"></a><span data-ttu-id="59272-453">パラメーター - disabledImage</span><span class="sxs-lookup"><span data-stu-id="59272-453">Parameters - disabledImage</span></span>

<span data-ttu-id="59272-454">値</span><span class="sxs-lookup"><span data-stu-id="59272-454">value</span></span>  

### <a name="return-value---disabledimage"></a><span data-ttu-id="59272-455">戻り値 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="59272-455">Return Value - disabledImage</span></span>

<span data-ttu-id="59272-456">画像ファイルのフル ネーム。</span><span class="sxs-lookup"><span data-stu-id="59272-456">The full name of an image file.</span></span> <span data-ttu-id="59272-457">システムは、GDI でサポートされているすべてのイメージ形式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="59272-457">The system supports all of the GDI-supported image formats.</span></span>

### <a name="remarks---disabledimage"></a><span data-ttu-id="59272-458">備考 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="59272-458">Remarks - disabledImage</span></span>

<span data-ttu-id="59272-459">このプロパティは、disabledResource プロパティに優先します。</span><span class="sxs-lookup"><span data-stu-id="59272-459">This property has precedence over the disabledResource property.</span></span> <span data-ttu-id="59272-460">これらのプロパティの両方が設定されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="59272-460">It is used if both of these properties are set.</span></span>

## <a name="method-disabledimagelocation"></a><span data-ttu-id="59272-461">メソッド disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="59272-461">Method disabledImageLocation</span></span>

```xpp
public int disabledImageLocation([int value])
```

### <a name="parameters---disabledimagelocation"></a><span data-ttu-id="59272-462">パラメーター - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="59272-462">Parameters - disabledImageLocation</span></span>

<span data-ttu-id="59272-463">値</span><span class="sxs-lookup"><span data-stu-id="59272-463">value</span></span>  

### <a name="return-value---disabledimagelocation"></a><span data-ttu-id="59272-464">戻り値 - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="59272-464">Return Value - disabledImageLocation</span></span>

## <a name="method-disabledresource"></a><span data-ttu-id="59272-465">メソッド disabledResource</span><span class="sxs-lookup"><span data-stu-id="59272-465">Method disabledResource</span></span>

<span data-ttu-id="59272-466">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-466">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>

```xpp
public int disabledResource([int value])
```

### <a name="parameters---disabledresource"></a><span data-ttu-id="59272-467">パラメーター - disabledResource</span><span class="sxs-lookup"><span data-stu-id="59272-467">Parameters - disabledResource</span></span>

<span data-ttu-id="59272-468">値</span><span class="sxs-lookup"><span data-stu-id="59272-468">value</span></span>  

### <a name="return-value---disabledresource"></a><span data-ttu-id="59272-469">戻り値 - disabledResource</span><span class="sxs-lookup"><span data-stu-id="59272-469">Return Value - disabledResource</span></span>

<span data-ttu-id="59272-470">無効なボタン画像として使用する画像リソース ID。</span><span class="sxs-lookup"><span data-stu-id="59272-470">The resource ID of the image to use as the disabled button image.</span></span> <span data-ttu-id="59272-471">アイコンとビットマップ イメージの両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="59272-471">Both icon and bitmap images are supported.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="59272-472">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="59272-472">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="59272-473">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="59272-473">Parameters - displayTarget</span></span>

<span data-ttu-id="59272-474">値</span><span class="sxs-lookup"><span data-stu-id="59272-474">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="59272-475">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="59272-475">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="59272-476">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="59272-476">Method dragDrop</span></span>

<span data-ttu-id="59272-477">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="59272-477">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="59272-478">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="59272-478">Parameters - dragDrop</span></span>

<span data-ttu-id="59272-479">値</span><span class="sxs-lookup"><span data-stu-id="59272-479">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="59272-480">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="59272-480">Return Value - dragDrop</span></span>

<span data-ttu-id="59272-481">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="59272-481">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="59272-482">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="59272-482">Method enabled</span></span>

<span data-ttu-id="59272-483">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="59272-483">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="59272-484">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="59272-484">Parameters - enabled</span></span>

<span data-ttu-id="59272-485">値</span><span class="sxs-lookup"><span data-stu-id="59272-485">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="59272-486">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="59272-486">Return Value - enabled</span></span>

<span data-ttu-id="59272-487">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="59272-487">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="59272-488">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="59272-488">Remarks - enabled</span></span>

<span data-ttu-id="59272-489">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="59272-489">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="59272-490">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="59272-490">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="59272-491">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="59272-491">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="59272-492">メソッド font</span><span class="sxs-lookup"><span data-stu-id="59272-492">Method font</span></span>

<span data-ttu-id="59272-493">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-493">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="59272-494">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="59272-494">Parameters - font</span></span>

<span data-ttu-id="59272-495">値</span><span class="sxs-lookup"><span data-stu-id="59272-495">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="59272-496">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="59272-496">Return Value - font</span></span>

<span data-ttu-id="59272-497">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="59272-497">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="59272-498">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="59272-498">Method fontSize</span></span>

<span data-ttu-id="59272-499">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-499">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="59272-500">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="59272-500">Parameters - fontSize</span></span>

<span data-ttu-id="59272-501">値</span><span class="sxs-lookup"><span data-stu-id="59272-501">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="59272-502">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="59272-502">Return Value - fontSize</span></span>

<span data-ttu-id="59272-503">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="59272-503">The height of the font in points.</span></span>

## <a name="method-forcedtooverflow"></a><span data-ttu-id="59272-504">メソッド forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="59272-504">Method forcedToOverflow</span></span>

```xpp
public boolean forcedToOverflow([boolean value])
```

### <a name="parameters---forcedtooverflow"></a><span data-ttu-id="59272-505">パラメーター - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="59272-505">Parameters - forcedToOverflow</span></span>

<span data-ttu-id="59272-506">値</span><span class="sxs-lookup"><span data-stu-id="59272-506">value</span></span>  

### <a name="return-value---forcedtooverflow"></a><span data-ttu-id="59272-507">戻り値 - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="59272-507">Return Value - forcedToOverflow</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="59272-508">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="59272-508">Method foregroundColor</span></span>

<span data-ttu-id="59272-509">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-509">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="59272-510">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="59272-510">Parameters - foregroundColor</span></span>

<span data-ttu-id="59272-511">値</span><span class="sxs-lookup"><span data-stu-id="59272-511">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="59272-512">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="59272-512">Return Value - foregroundColor</span></span>

<span data-ttu-id="59272-513">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="59272-513">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="59272-514">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="59272-514">Remarks - foregroundColor</span></span>

<span data-ttu-id="59272-515">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="59272-515">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="59272-516">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="59272-516">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="59272-517">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="59272-517">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="59272-518">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="59272-518">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="59272-519">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="59272-519">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="59272-520">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="59272-520">The maximum value for a single byte is 255.</span></span>

## <a name="method-height"></a><span data-ttu-id="59272-521">メソッド height</span><span class="sxs-lookup"><span data-stu-id="59272-521">Method height</span></span>

<span data-ttu-id="59272-522">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-522">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="59272-523">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="59272-523">Parameters - height</span></span>

<span data-ttu-id="59272-524">値</span><span class="sxs-lookup"><span data-stu-id="59272-524">value</span></span>  

<!-- -->

<span data-ttu-id="59272-525">モード</span><span class="sxs-lookup"><span data-stu-id="59272-525">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="59272-526">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="59272-526">Return Value - height</span></span>

<span data-ttu-id="59272-527">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="59272-527">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="59272-528">備考 - height</span><span class="sxs-lookup"><span data-stu-id="59272-528">Remarks - height</span></span>

<span data-ttu-id="59272-529">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="59272-529">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="59272-530">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="59272-530">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="59272-531">モード。</span><span class="sxs-lookup"><span data-stu-id="59272-531">Mode.</span></span>            | <span data-ttu-id="59272-532">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="59272-532">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="59272-533">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="59272-533">-1 Exact.</span></span>        | <span data-ttu-id="59272-534">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="59272-534">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="59272-535">0 自動。</span><span class="sxs-lookup"><span data-stu-id="59272-535">0 Auto.</span></span>          | <span data-ttu-id="59272-536">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="59272-536">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="59272-537">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="59272-537">1 Column height.</span></span> | <span data-ttu-id="59272-538">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="59272-538">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="59272-539">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="59272-539">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="59272-540">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="59272-540">Method heightMode</span></span>

<span data-ttu-id="59272-541">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-541">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="59272-542">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="59272-542">Parameters - heightMode</span></span>

<span data-ttu-id="59272-543">値</span><span class="sxs-lookup"><span data-stu-id="59272-543">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="59272-544">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="59272-544">Return Value - heightMode</span></span>

<span data-ttu-id="59272-545">計算モード。</span><span class="sxs-lookup"><span data-stu-id="59272-545">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="59272-546">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="59272-546">Remarks - heightMode</span></span>

<span data-ttu-id="59272-547">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="59272-547">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="59272-548">モード。</span><span class="sxs-lookup"><span data-stu-id="59272-548">Mode.</span></span>          | <span data-ttu-id="59272-549">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="59272-549">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="59272-550">正確。</span><span class="sxs-lookup"><span data-stu-id="59272-550">Exact.</span></span>         | <span data-ttu-id="59272-551">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="59272-551">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="59272-552">自動。</span><span class="sxs-lookup"><span data-stu-id="59272-552">Auto.</span></span>          | <span data-ttu-id="59272-553">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="59272-553">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="59272-554">列の高さ</span><span class="sxs-lookup"><span data-stu-id="59272-554">Column height.</span></span> | <span data-ttu-id="59272-555">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="59272-555">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="59272-556">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="59272-556">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="59272-557">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="59272-557">Method heightValue</span></span>

<span data-ttu-id="59272-558">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-558">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="59272-559">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="59272-559">Parameters - heightValue</span></span>

<span data-ttu-id="59272-560">値</span><span class="sxs-lookup"><span data-stu-id="59272-560">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="59272-561">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="59272-561">Return Value - heightValue</span></span>

<span data-ttu-id="59272-562">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="59272-562">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="59272-563">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="59272-563">Remarks - heightValue</span></span>

<span data-ttu-id="59272-564">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="59272-564">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="59272-565">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="59272-565">Method helpText</span></span>

<span data-ttu-id="59272-566">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-566">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="59272-567">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="59272-567">Parameters - helpText</span></span>

<span data-ttu-id="59272-568">値</span><span class="sxs-lookup"><span data-stu-id="59272-568">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="59272-569">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="59272-569">Return Value - helpText</span></span>

<span data-ttu-id="59272-570">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="59272-570">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="59272-571">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="59272-571">Remarks - helpText</span></span>

<span data-ttu-id="59272-572">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-572">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="59272-573">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="59272-573">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="59272-574">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="59272-574">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="59272-575">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="59272-575">Parameters - hierarchyParent</span></span>

<span data-ttu-id="59272-576">値</span><span class="sxs-lookup"><span data-stu-id="59272-576">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="59272-577">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="59272-577">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="59272-578">メソッド id</span><span class="sxs-lookup"><span data-stu-id="59272-578">Method id</span></span>

<span data-ttu-id="59272-579">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="59272-579">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="59272-580">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="59272-580">Return Value - id</span></span>

<span data-ttu-id="59272-581">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="59272-581">The ID of the control.</span></span>

## <a name="method-imagelocation"></a><span data-ttu-id="59272-582">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="59272-582">Method imageLocation</span></span>

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a><span data-ttu-id="59272-583">パラメーター - imageLocation</span><span class="sxs-lookup"><span data-stu-id="59272-583">Parameters - imageLocation</span></span>

<span data-ttu-id="59272-584">値</span><span class="sxs-lookup"><span data-stu-id="59272-584">value</span></span>  

### <a name="return-value---imagelocation"></a><span data-ttu-id="59272-585">戻り値 - imageLocation</span><span class="sxs-lookup"><span data-stu-id="59272-585">Return Value - imageLocation</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="59272-586">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="59272-586">Method isContainer</span></span>

<span data-ttu-id="59272-587">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="59272-587">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="59272-588">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="59272-588">Return Value - isContainer</span></span>

<span data-ttu-id="59272-589">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="59272-589">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="59272-590">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="59272-590">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="59272-591">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="59272-591">Parameters - italic</span></span>

<span data-ttu-id="59272-592">値</span><span class="sxs-lookup"><span data-stu-id="59272-592">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="59272-593">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="59272-593">Return Value - italic</span></span>

## <a name="method-keytip"></a><span data-ttu-id="59272-594">メソッド keyTip</span><span class="sxs-lookup"><span data-stu-id="59272-594">Method keyTip</span></span>

```xpp
public str keyTip([str value])
```

### <a name="parameters---keytip"></a><span data-ttu-id="59272-595">パラメーター - keyTip</span><span class="sxs-lookup"><span data-stu-id="59272-595">Parameters - keyTip</span></span>

<span data-ttu-id="59272-596">値</span><span class="sxs-lookup"><span data-stu-id="59272-596">value</span></span>  

### <a name="return-value---keytip"></a><span data-ttu-id="59272-597">戻り値 - keyTip</span><span class="sxs-lookup"><span data-stu-id="59272-597">Return Value - keyTip</span></span>

## <a name="method-left"></a><span data-ttu-id="59272-598">メソッド left</span><span class="sxs-lookup"><span data-stu-id="59272-598">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="59272-599">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="59272-599">Parameters - left</span></span>

<span data-ttu-id="59272-600">値</span><span class="sxs-lookup"><span data-stu-id="59272-600">value</span></span>  

<!-- -->

<span data-ttu-id="59272-601">モード</span><span class="sxs-lookup"><span data-stu-id="59272-601">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="59272-602">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="59272-602">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="59272-603">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="59272-603">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="59272-604">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="59272-604">Parameters - leftMode</span></span>

<span data-ttu-id="59272-605">値</span><span class="sxs-lookup"><span data-stu-id="59272-605">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="59272-606">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="59272-606">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="59272-607">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="59272-607">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="59272-608">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="59272-608">Parameters - leftValue</span></span>

<span data-ttu-id="59272-609">値</span><span class="sxs-lookup"><span data-stu-id="59272-609">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="59272-610">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="59272-610">Return Value - leftValue</span></span>

## <a name="method-multiselect"></a><span data-ttu-id="59272-611">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="59272-611">Method multiSelect</span></span>

```xpp
public int multiSelect([int value])
```

### <a name="parameters---multiselect"></a><span data-ttu-id="59272-612">パラメーター - multiSelect</span><span class="sxs-lookup"><span data-stu-id="59272-612">Parameters - multiSelect</span></span>

<span data-ttu-id="59272-613">値</span><span class="sxs-lookup"><span data-stu-id="59272-613">value</span></span>  

### <a name="return-value---multiselect"></a><span data-ttu-id="59272-614">戻り値 - multiSelect</span><span class="sxs-lookup"><span data-stu-id="59272-614">Return Value - multiSelect</span></span>

## <a name="method-name"></a><span data-ttu-id="59272-615">メソッド名</span><span class="sxs-lookup"><span data-stu-id="59272-615">Method name</span></span>

<span data-ttu-id="59272-616">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-616">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="59272-617">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="59272-617">Parameters - name</span></span>

<span data-ttu-id="59272-618">値</span><span class="sxs-lookup"><span data-stu-id="59272-618">value</span></span>  
<span data-ttu-id="59272-619">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="59272-619">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="59272-620">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="59272-620">Return Value - name</span></span>

<span data-ttu-id="59272-621">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="59272-621">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="59272-622">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="59272-622">Remarks - name</span></span>

<span data-ttu-id="59272-623">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="59272-623">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="59272-624">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="59272-624">It must start with a letter.</span></span>
-   <span data-ttu-id="59272-625">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="59272-625">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="59272-626">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="59272-626">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="59272-627">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="59272-627">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="59272-628">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="59272-628">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="59272-629">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="59272-629">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="59272-630">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="59272-630">Parameters - neededPermission</span></span>

<span data-ttu-id="59272-631">値</span><span class="sxs-lookup"><span data-stu-id="59272-631">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="59272-632">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="59272-632">Return Value - neededPermission</span></span>

## <a name="method-needsrecord"></a><span data-ttu-id="59272-633">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="59272-633">Method needsRecord</span></span>

```xpp
public int needsRecord([int value])
```

### <a name="parameters---needsrecord"></a><span data-ttu-id="59272-634">パラメーター - needsRecord</span><span class="sxs-lookup"><span data-stu-id="59272-634">Parameters - needsRecord</span></span>

<span data-ttu-id="59272-635">値</span><span class="sxs-lookup"><span data-stu-id="59272-635">value</span></span>  

### <a name="return-value---needsrecord"></a><span data-ttu-id="59272-636">戻り値 - needsRecord</span><span class="sxs-lookup"><span data-stu-id="59272-636">Return Value - needsRecord</span></span>

## <a name="method-normalimage"></a><span data-ttu-id="59272-637">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="59272-637">Method normalImage</span></span>

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a><span data-ttu-id="59272-638">パラメーター - normalImage</span><span class="sxs-lookup"><span data-stu-id="59272-638">Parameters - normalImage</span></span>

<span data-ttu-id="59272-639">値</span><span class="sxs-lookup"><span data-stu-id="59272-639">value</span></span>  

### <a name="return-value---normalimage"></a><span data-ttu-id="59272-640">戻り値 - normalImage</span><span class="sxs-lookup"><span data-stu-id="59272-640">Return Value - normalImage</span></span>

## <a name="method-normalresource"></a><span data-ttu-id="59272-641">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="59272-641">Method normalResource</span></span>

```xpp
public int normalResource([int value])
```

### <a name="parameters---normalresource"></a><span data-ttu-id="59272-642">パラメーター - normalResource</span><span class="sxs-lookup"><span data-stu-id="59272-642">Parameters - normalResource</span></span>

<span data-ttu-id="59272-643">値</span><span class="sxs-lookup"><span data-stu-id="59272-643">value</span></span>  

### <a name="return-value---normalresource"></a><span data-ttu-id="59272-644">戻り値 - normalResource</span><span class="sxs-lookup"><span data-stu-id="59272-644">Return Value - normalResource</span></span>

## <a name="method-parameters"></a><span data-ttu-id="59272-645">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="59272-645">Method parameters</span></span>

```xpp
public str parameters([str value])
```

### <a name="parameters---parameters"></a><span data-ttu-id="59272-646">パラメーター - parameters</span><span class="sxs-lookup"><span data-stu-id="59272-646">Parameters - parameters</span></span>

<span data-ttu-id="59272-647">値</span><span class="sxs-lookup"><span data-stu-id="59272-647">value</span></span>  

### <a name="return-value---parameters"></a><span data-ttu-id="59272-648">戻り値 - parameters</span><span class="sxs-lookup"><span data-stu-id="59272-648">Return Value - parameters</span></span>

## <a name="method-primary"></a><span data-ttu-id="59272-649">メソッド primary</span><span class="sxs-lookup"><span data-stu-id="59272-649">Method primary</span></span>

```xpp
public boolean primary([boolean value])
```

### <a name="parameters---primary"></a><span data-ttu-id="59272-650">パラメーター - primary</span><span class="sxs-lookup"><span data-stu-id="59272-650">Parameters - primary</span></span>

<span data-ttu-id="59272-651">値</span><span class="sxs-lookup"><span data-stu-id="59272-651">value</span></span>  

### <a name="return-value---primary"></a><span data-ttu-id="59272-652">戻り値 - primary</span><span class="sxs-lookup"><span data-stu-id="59272-652">Return Value - primary</span></span>

## <a name="method-saverecord"></a><span data-ttu-id="59272-653">メソッド saveRecord</span><span class="sxs-lookup"><span data-stu-id="59272-653">Method saveRecord</span></span>

```xpp
public boolean saveRecord([boolean value])
```

### <a name="parameters---saverecord"></a><span data-ttu-id="59272-654">パラメーター - saveRecord</span><span class="sxs-lookup"><span data-stu-id="59272-654">Parameters - saveRecord</span></span>

<span data-ttu-id="59272-655">値</span><span class="sxs-lookup"><span data-stu-id="59272-655">value</span></span>  

### <a name="return-value---saverecord"></a><span data-ttu-id="59272-656">戻り値 - saveRecord</span><span class="sxs-lookup"><span data-stu-id="59272-656">Return Value - saveRecord</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="59272-657">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="59272-657">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="59272-658">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="59272-658">Parameters - securityKey</span></span>

<span data-ttu-id="59272-659">値</span><span class="sxs-lookup"><span data-stu-id="59272-659">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="59272-660">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="59272-660">Return Value - securityKey</span></span>

## <a name="method-shortkey"></a><span data-ttu-id="59272-661">メソッド shortkey</span><span class="sxs-lookup"><span data-stu-id="59272-661">Method shortkey</span></span>

```xpp
public int shortkey([int value])
```

### <a name="parameters---shortkey"></a><span data-ttu-id="59272-662">パラメーター - shortkey</span><span class="sxs-lookup"><span data-stu-id="59272-662">Parameters - shortkey</span></span>

<span data-ttu-id="59272-663">値</span><span class="sxs-lookup"><span data-stu-id="59272-663">value</span></span>  

### <a name="return-value---shortkey"></a><span data-ttu-id="59272-664">戻り値 - shortkey</span><span class="sxs-lookup"><span data-stu-id="59272-664">Return Value - shortkey</span></span>

## <a name="method-showshortcut"></a><span data-ttu-id="59272-665">メソッド showShortCut</span><span class="sxs-lookup"><span data-stu-id="59272-665">Method showShortCut</span></span>

```xpp
public boolean showShortCut([boolean value])
```

### <a name="parameters---showshortcut"></a><span data-ttu-id="59272-666">パラメーター - showShortCut</span><span class="sxs-lookup"><span data-stu-id="59272-666">Parameters - showShortCut</span></span>

<span data-ttu-id="59272-667">値</span><span class="sxs-lookup"><span data-stu-id="59272-667">value</span></span>  

### <a name="return-value---showshortcut"></a><span data-ttu-id="59272-668">戻り値 - showShortCut</span><span class="sxs-lookup"><span data-stu-id="59272-668">Return Value - showShortCut</span></span>

## <a name="method-skip"></a><span data-ttu-id="59272-669">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="59272-669">Method skip</span></span>

<span data-ttu-id="59272-670">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="59272-670">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="59272-671">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="59272-671">Parameters - skip</span></span>

<span data-ttu-id="59272-672">値</span><span class="sxs-lookup"><span data-stu-id="59272-672">value</span></span>  
<span data-ttu-id="59272-673">コントロールの skip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="59272-673">The value to assign to the skip property of the control.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="59272-674">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="59272-674">Return Value - skip</span></span>

<span data-ttu-id="59272-675">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="59272-675">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-style"></a><span data-ttu-id="59272-676">メソッド style</span><span class="sxs-lookup"><span data-stu-id="59272-676">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="59272-677">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="59272-677">Parameters - style</span></span>

<span data-ttu-id="59272-678">値</span><span class="sxs-lookup"><span data-stu-id="59272-678">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="59272-679">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="59272-679">Return Value - style</span></span>

## <a name="method-text"></a><span data-ttu-id="59272-680">メソッド text</span><span class="sxs-lookup"><span data-stu-id="59272-680">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="59272-681">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="59272-681">Parameters - text</span></span>

<span data-ttu-id="59272-682">値</span><span class="sxs-lookup"><span data-stu-id="59272-682">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="59272-683">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="59272-683">Return Value - text</span></span>

## <a name="method-togglebutton"></a><span data-ttu-id="59272-684">メソッド toggleButton</span><span class="sxs-lookup"><span data-stu-id="59272-684">Method toggleButton</span></span>

```xpp
public int toggleButton([int value])
```

### <a name="parameters---togglebutton"></a><span data-ttu-id="59272-685">パラメーター - toggleButton</span><span class="sxs-lookup"><span data-stu-id="59272-685">Parameters - toggleButton</span></span>

<span data-ttu-id="59272-686">値</span><span class="sxs-lookup"><span data-stu-id="59272-686">value</span></span>  

### <a name="return-value---togglebutton"></a><span data-ttu-id="59272-687">戻り値 - toggleButton</span><span class="sxs-lookup"><span data-stu-id="59272-687">Return Value - toggleButton</span></span>

## <a name="method-togglevalue"></a><span data-ttu-id="59272-688">メソッド toggleValue</span><span class="sxs-lookup"><span data-stu-id="59272-688">Method toggleValue</span></span>

```xpp
public int toggleValue([int value])
```

### <a name="parameters---togglevalue"></a><span data-ttu-id="59272-689">パラメーター - toggleValue</span><span class="sxs-lookup"><span data-stu-id="59272-689">Parameters - toggleValue</span></span>

<span data-ttu-id="59272-690">値</span><span class="sxs-lookup"><span data-stu-id="59272-690">value</span></span>  

### <a name="return-value---togglevalue"></a><span data-ttu-id="59272-691">戻り値 - toggleValue</span><span class="sxs-lookup"><span data-stu-id="59272-691">Return Value - toggleValue</span></span>

## <a name="method-top"></a><span data-ttu-id="59272-692">メソッド top</span><span class="sxs-lookup"><span data-stu-id="59272-692">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="59272-693">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="59272-693">Parameters - top</span></span>

<span data-ttu-id="59272-694">値</span><span class="sxs-lookup"><span data-stu-id="59272-694">value</span></span>  

<!-- -->

<span data-ttu-id="59272-695">モード</span><span class="sxs-lookup"><span data-stu-id="59272-695">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="59272-696">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="59272-696">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="59272-697">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="59272-697">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="59272-698">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="59272-698">Parameters - topMode</span></span>

<span data-ttu-id="59272-699">値</span><span class="sxs-lookup"><span data-stu-id="59272-699">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="59272-700">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="59272-700">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="59272-701">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="59272-701">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="59272-702">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="59272-702">Parameters - topValue</span></span>

<span data-ttu-id="59272-703">値</span><span class="sxs-lookup"><span data-stu-id="59272-703">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="59272-704">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="59272-704">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="59272-705">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="59272-705">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="59272-706">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="59272-706">Parameters - type</span></span>

<span data-ttu-id="59272-707">値</span><span class="sxs-lookup"><span data-stu-id="59272-707">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="59272-708">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="59272-708">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="59272-709">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="59272-709">Method underline</span></span>

<span data-ttu-id="59272-710">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="59272-710">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="59272-711">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="59272-711">Parameters - underline</span></span>

<span data-ttu-id="59272-712">値</span><span class="sxs-lookup"><span data-stu-id="59272-712">value</span></span>  
<span data-ttu-id="59272-713">コントロールの underline プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="59272-713">The value to assign to the underline property of the control.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="59272-714">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="59272-714">Return Value - underline</span></span>

<span data-ttu-id="59272-715">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="59272-715">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-userdata"></a><span data-ttu-id="59272-716">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="59272-716">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="59272-717">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="59272-717">Parameters - userData</span></span>

<span data-ttu-id="59272-718">値</span><span class="sxs-lookup"><span data-stu-id="59272-718">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="59272-719">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="59272-719">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="59272-720">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="59272-720">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="59272-721">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="59272-721">Parameters - userDataItem</span></span>

<span data-ttu-id="59272-722">値</span><span class="sxs-lookup"><span data-stu-id="59272-722">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="59272-723">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="59272-723">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="59272-724">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="59272-724">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="59272-725">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="59272-725">Parameters - userDataItems</span></span>

<span data-ttu-id="59272-726">値</span><span class="sxs-lookup"><span data-stu-id="59272-726">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="59272-727">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="59272-727">Return Value - userDataItems</span></span>

## <a name="method-value"></a><span data-ttu-id="59272-728">メソッド value</span><span class="sxs-lookup"><span data-stu-id="59272-728">Method value</span></span>

```xpp
public boolean value([boolean value])
```

### <a name="parameters---value"></a><span data-ttu-id="59272-729">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="59272-729">Parameters - value</span></span>

<span data-ttu-id="59272-730">値</span><span class="sxs-lookup"><span data-stu-id="59272-730">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="59272-731">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="59272-731">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="59272-732">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="59272-732">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="59272-733">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="59272-733">Parameters - verticalSpacing</span></span>

<span data-ttu-id="59272-734">値</span><span class="sxs-lookup"><span data-stu-id="59272-734">value</span></span>  

<!-- -->

<span data-ttu-id="59272-735">モード</span><span class="sxs-lookup"><span data-stu-id="59272-735">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="59272-736">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="59272-736">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="59272-737">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="59272-737">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="59272-738">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="59272-738">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="59272-739">モード</span><span class="sxs-lookup"><span data-stu-id="59272-739">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="59272-740">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="59272-740">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="59272-741">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="59272-741">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="59272-742">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="59272-742">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="59272-743">値</span><span class="sxs-lookup"><span data-stu-id="59272-743">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="59272-744">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="59272-744">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="59272-745">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="59272-745">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="59272-746">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="59272-746">Parameters - visible</span></span>

<span data-ttu-id="59272-747">値</span><span class="sxs-lookup"><span data-stu-id="59272-747">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="59272-748">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="59272-748">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="59272-749">メソッド width</span><span class="sxs-lookup"><span data-stu-id="59272-749">Method width</span></span>

<span data-ttu-id="59272-750">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-750">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="59272-751">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="59272-751">Parameters - width</span></span>

<span data-ttu-id="59272-752">値</span><span class="sxs-lookup"><span data-stu-id="59272-752">value</span></span>  

<!-- -->

<span data-ttu-id="59272-753">モード</span><span class="sxs-lookup"><span data-stu-id="59272-753">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="59272-754">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="59272-754">Return Value - width</span></span>

<span data-ttu-id="59272-755">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="59272-755">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="59272-756">備考 - width</span><span class="sxs-lookup"><span data-stu-id="59272-756">Remarks - width</span></span>

<span data-ttu-id="59272-757">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="59272-757">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="59272-758">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="59272-758">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="59272-759">モード。</span><span class="sxs-lookup"><span data-stu-id="59272-759">Mode.</span></span>           | <span data-ttu-id="59272-760">幅計算。</span><span class="sxs-lookup"><span data-stu-id="59272-760">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="59272-761">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="59272-761">-1 Exact.</span></span>       | <span data-ttu-id="59272-762">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="59272-762">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="59272-763">0 自動。</span><span class="sxs-lookup"><span data-stu-id="59272-763">0 Auto.</span></span>         | <span data-ttu-id="59272-764">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="59272-764">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="59272-765">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="59272-765">1 Column width.</span></span> | <span data-ttu-id="59272-766">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="59272-766">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="59272-767">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="59272-767">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="59272-768">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="59272-768">Method widthMode</span></span>

<span data-ttu-id="59272-769">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-769">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="59272-770">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="59272-770">Parameters - widthMode</span></span>

<span data-ttu-id="59272-771">値</span><span class="sxs-lookup"><span data-stu-id="59272-771">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="59272-772">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="59272-772">Return Value - widthMode</span></span>

<span data-ttu-id="59272-773">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="59272-773">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="59272-774">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="59272-774">Remarks - widthMode</span></span>

<span data-ttu-id="59272-775">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="59272-775">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="59272-776">モード。</span><span class="sxs-lookup"><span data-stu-id="59272-776">Mode.</span></span>         | <span data-ttu-id="59272-777">幅計算。</span><span class="sxs-lookup"><span data-stu-id="59272-777">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="59272-778">正確。</span><span class="sxs-lookup"><span data-stu-id="59272-778">Exact.</span></span>        | <span data-ttu-id="59272-779">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="59272-779">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="59272-780">自動。</span><span class="sxs-lookup"><span data-stu-id="59272-780">Auto.</span></span>         | <span data-ttu-id="59272-781">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="59272-781">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="59272-782">列の幅。</span><span class="sxs-lookup"><span data-stu-id="59272-782">Column width.</span></span> | <span data-ttu-id="59272-783">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="59272-783">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="59272-784">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="59272-784">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="59272-785">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="59272-785">Method widthValue</span></span>

<span data-ttu-id="59272-786">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="59272-786">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="59272-787">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="59272-787">Parameters - widthValue</span></span>

<span data-ttu-id="59272-788">値</span><span class="sxs-lookup"><span data-stu-id="59272-788">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="59272-789">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="59272-789">Return Value - widthValue</span></span>

<span data-ttu-id="59272-790">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="59272-790">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="59272-791">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="59272-791">Remarks - widthValue</span></span>

<span data-ttu-id="59272-792">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="59272-792">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="59272-793">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="59272-793">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="59272-794">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="59272-794">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="59272-795">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="59272-795">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="59272-796">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="59272-796">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="59272-797">overrideObject</span><span class="sxs-lookup"><span data-stu-id="59272-797">overrideObject</span></span>  

