---
title: FormBuildFunctionButtonControl クラス
description: このトピックでは、FormBuildFunctionButtonControl クラスについて説明します。
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
ms.openlocfilehash: 41c5e3c93a6fac011781d32d7e9b80b5415bcfb6
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502649"
---
# <a name="class-formbuildfunctionbuttoncontrol"></a><span data-ttu-id="29fb5-103">クラス FormBuildFunctionButtonControl</span><span class="sxs-lookup"><span data-stu-id="29fb5-103">Class FormBuildFunctionButtonControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildFunctionButtonControl extends FormBuildControl
```

<span data-ttu-id="29fb5-104">FormBuildFunctionButtonControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-104">The FormBuildFunctionButtonControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="29fb5-105">備考</span><span class="sxs-lookup"><span data-stu-id="29fb5-105">Remarks</span></span>

<span data-ttu-id="29fb5-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="29fb5-107">例</span><span class="sxs-lookup"><span data-stu-id="29fb5-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="29fb5-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="29fb5-108">Methods</span></span>

| <span data-ttu-id="29fb5-109">方法</span><span class="sxs-lookup"><span data-stu-id="29fb5-109">Method</span></span>                                                                                                      | <span data-ttu-id="29fb5-110">説明</span><span class="sxs-lookup"><span data-stu-id="29fb5-110">Description</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29fb5-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="29fb5-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-112">Determines whether to align the control.</span></span>                                                                                                  |
| <span data-ttu-id="29fb5-113">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-113">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="29fb5-114">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-114">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="29fb5-115">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-115">Determines whether the user can change the contents of the control.</span></span>                                                                       |
| <span data-ttu-id="29fb5-116">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-116">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="29fb5-117">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-117">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                        |
| <span data-ttu-id="29fb5-118">public boolean autoRefreshData(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-118">public boolean autoRefreshData(\[boolean value\])</span></span>                                                           |                                                                                                                                           |
| <span data-ttu-id="29fb5-119">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-119">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="29fb5-120">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-120">Gets or sets the background color of the control.</span></span>                                                                                         |
| <span data-ttu-id="29fb5-121">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-121">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="29fb5-122">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-122">Determines whether the control background can be transparent.</span></span>                                                                            |
| <span data-ttu-id="29fb5-123">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-123">public boolean big(\[boolean value\])</span></span>                                                                       |                                                                                                                                           |
| <span data-ttu-id="29fb5-124">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-124">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="29fb5-125">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-125">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                               |
| <span data-ttu-id="29fb5-126">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-126">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="29fb5-127">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-127">Gets or sets the style of the borderline of the control.</span></span>                                                                                  |
| <span data-ttu-id="29fb5-128">public int buttonDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-128">public int buttonDisplay(\[int value\])</span></span>                                                                     | <span data-ttu-id="29fb5-129">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-129">Gets or sets the appearance of the button control.</span></span>                                                                                        |
| <span data-ttu-id="29fb5-130">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-130">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="29fb5-131">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-131">Gets or set the caption of the control.</span></span>                                                                                                   |
| <span data-ttu-id="29fb5-132">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-132">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="29fb5-133">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-133">Gets or sets the character set of the font.</span></span>                                                                                               |
| <span data-ttu-id="29fb5-134">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-134">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="29fb5-135">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-135">Gets or sets the color scheme of the control.</span></span>                                                                                             |
| <span data-ttu-id="29fb5-136">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-136">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="29fb5-137">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-137">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                       |
| <span data-ttu-id="29fb5-138">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="29fb5-138">public int containerId()</span></span>                                                                                    | <span data-ttu-id="29fb5-139">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-139">Retrieves the ID of the parent container for the control.</span></span>                                                                                 |
| <span data-ttu-id="29fb5-140">public int copyCallerQuery(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-140">public int copyCallerQuery(\[int value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="29fb5-141">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-141">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="29fb5-142">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-142">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                           |
| <span data-ttu-id="29fb5-143">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-143">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="29fb5-144">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-144">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="29fb5-145">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-145">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                  |
| <span data-ttu-id="29fb5-146">public boolean defaultButton(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-146">public boolean defaultButton(\[boolean value\])</span></span>                                                             | <span data-ttu-id="29fb5-147">ボタンをフォーム上の既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-147">Determines whether the button should be the default button on the form.</span></span>                                                                   |
| <span data-ttu-id="29fb5-148">public str disabledImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-148">public str disabledImage(\[str value\])</span></span>                                                                     | <span data-ttu-id="29fb5-149">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-149">Gets or sets the disabled image of the button.</span></span>                                                                                            |
| <span data-ttu-id="29fb5-150">public int disabledImageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-150">public int disabledImageLocation(\[int value\])</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="29fb5-151">public int disabledResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-151">public int disabledResource(\[int value\])</span></span>                                                                  | <span data-ttu-id="29fb5-152">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-152">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>                                                            |
| <span data-ttu-id="29fb5-153">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-153">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="29fb5-154">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-154">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="29fb5-155">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-155">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                         |
| <span data-ttu-id="29fb5-156">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-156">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="29fb5-157">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-157">Determines whether to enable or disable the object.</span></span>                                                                                       |
| <span data-ttu-id="29fb5-158">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-158">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="29fb5-159">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-159">Gets or sets the name of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="29fb5-160">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-160">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="29fb5-161">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-161">Gets or sets the size of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="29fb5-162">public boolean forcedToOverflow(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-162">public boolean forcedToOverflow(\[boolean value\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="29fb5-163">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-163">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="29fb5-164">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-164">Gets or sets the text color for the control to use.</span></span>                                                                                       |
| <span data-ttu-id="29fb5-165">public int formViewOption(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-165">public int formViewOption(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="29fb5-166">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-166">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="29fb5-167">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-167">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="29fb5-168">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-168">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="29fb5-169">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-169">Gets or sets a calculation mode for the height of the control.</span></span>                                                                            |
| <span data-ttu-id="29fb5-170">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-170">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="29fb5-171">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-171">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="29fb5-172">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-172">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="29fb5-173">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-173">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="29fb5-174">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-174">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="29fb5-175">public int id()</span><span class="sxs-lookup"><span data-stu-id="29fb5-175">public int id()</span></span>                                                                                             | <span data-ttu-id="29fb5-176">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-176">Retrieves the ID of the control.</span></span>                                                                                                          |
| <span data-ttu-id="29fb5-177">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-177">public int imageLocation(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="29fb5-178">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="29fb5-178">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="29fb5-179">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-179">Retrieves a value that indicates whether the control is a container control.</span></span>                                                              |
| <span data-ttu-id="29fb5-180">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-180">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="29fb5-181">public str keyTip(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-181">public str keyTip(\[str value\])</span></span>                                                                            |                                                                                                                                           |
| <span data-ttu-id="29fb5-182">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-182">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="29fb5-183">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-183">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="29fb5-184">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-184">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="29fb5-185">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-185">public str menuItemName(\[str value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="29fb5-186">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-186">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                                                    |                                                                                                                                           |
| <span data-ttu-id="29fb5-187">public int multiSelect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-187">public int multiSelect(\[int value\])</span></span>                                                                       |                                                                                                                                           |
| <span data-ttu-id="29fb5-188">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-188">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="29fb5-189">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-189">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="29fb5-190">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-190">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="29fb5-191">public int needsRecord(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-191">public int needsRecord(\[int value\])</span></span>                                                                       |                                                                                                                                           |
| <span data-ttu-id="29fb5-192">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-192">public str normalImage(\[str value\])</span></span>                                                                       |                                                                                                                                           |
| <span data-ttu-id="29fb5-193">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-193">public int normalResource(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="29fb5-194">public int openMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-194">public int openMode(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="29fb5-195">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-195">public str parameters(\[str value\])</span></span>                                                                        | <span data-ttu-id="29fb5-196">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-196">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                    |
| <span data-ttu-id="29fb5-197">public boolean primary(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-197">public boolean primary(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="29fb5-198">public boolean saveRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-198">public boolean saveRecord(\[boolean value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="29fb5-199">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-199">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                           |
| <span data-ttu-id="29fb5-200">public boolean sendExternalContext(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-200">public boolean sendExternalContext(\[boolean value\])</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="29fb5-201">public int shortkey(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-201">public int shortkey(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="29fb5-202">public boolean showShortCut(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-202">public boolean showShortCut(\[boolean value\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="29fb5-203">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-203">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="29fb5-204">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-204">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>           |
| <span data-ttu-id="29fb5-205">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-205">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                           |
| <span data-ttu-id="29fb5-206">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-206">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="29fb5-207">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-207">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="29fb5-208">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-208">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                           |
| <span data-ttu-id="29fb5-209">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-209">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="29fb5-210">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-210">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="29fb5-211">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-211">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="29fb5-212">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-212">Sets or returns the underline property for the text in the control.</span></span>                                                                       |
| <span data-ttu-id="29fb5-213">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-213">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="29fb5-214">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-214">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="29fb5-215">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-215">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="29fb5-216">public boolean value(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-216">public boolean value(\[boolean value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="29fb5-217">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-217">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="29fb5-218">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-218">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="29fb5-219">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-219">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="29fb5-220">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-220">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="29fb5-221">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-221">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="29fb5-222">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-222">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="29fb5-223">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-223">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="29fb5-224">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-224">Gets or sets the calculation mode of the width of the control.</span></span>                                                                            |
| <span data-ttu-id="29fb5-225">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-225">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="29fb5-226">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-226">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="29fb5-227">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="29fb5-227">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                           |

## <a name="method-aligncontrol"></a><span data-ttu-id="29fb5-228">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="29fb5-228">Method alignControl</span></span>

<span data-ttu-id="29fb5-229">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-229">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="29fb5-230">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="29fb5-230">Parameters - alignControl</span></span>

<span data-ttu-id="29fb5-231">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-231">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="29fb5-232">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="29fb5-232">Return Value - alignControl</span></span>

<span data-ttu-id="29fb5-233">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="29fb5-233">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="29fb5-234">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="29fb5-234">Remarks - alignControl</span></span>

<span data-ttu-id="29fb5-235">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-235">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="29fb5-236">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="29fb5-236">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="29fb5-237">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="29fb5-237">Parameters - alignment</span></span>

<span data-ttu-id="29fb5-238">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-238">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="29fb5-239">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="29fb5-239">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="29fb5-240">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="29fb5-240">Method allowEdit</span></span>

<span data-ttu-id="29fb5-241">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-241">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="29fb5-242">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="29fb5-242">Parameters - allowEdit</span></span>

<span data-ttu-id="29fb5-243">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-243">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="29fb5-244">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="29fb5-244">Return Value - allowEdit</span></span>

<span data-ttu-id="29fb5-245">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="29fb5-245">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="29fb5-246">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="29fb5-246">Remarks - allowEdit</span></span>

<span data-ttu-id="29fb5-247">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="29fb5-247">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="29fb5-248">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="29fb5-248">Method autoDeclaration</span></span>

<span data-ttu-id="29fb5-249">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-249">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="29fb5-250">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="29fb5-250">Parameters - autoDeclaration</span></span>

<span data-ttu-id="29fb5-251">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-251">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="29fb5-252">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="29fb5-252">Return Value - autoDeclaration</span></span>

<span data-ttu-id="29fb5-253">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="29fb5-253">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="29fb5-254">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="29fb5-254">Remarks - autoDeclaration</span></span>

<span data-ttu-id="29fb5-255">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="29fb5-255">Controls cannot have identical names.</span></span>

## <a name="method-autorefreshdata"></a><span data-ttu-id="29fb5-256">メソッド autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="29fb5-256">Method autoRefreshData</span></span>

```xpp
public boolean autoRefreshData([boolean value])
```

### <a name="parameters---autorefreshdata"></a><span data-ttu-id="29fb5-257">パラメーター - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="29fb5-257">Parameters - autoRefreshData</span></span>

<span data-ttu-id="29fb5-258">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-258">value</span></span>  

### <a name="return-value---autorefreshdata"></a><span data-ttu-id="29fb5-259">戻り値 - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="29fb5-259">Return Value - autoRefreshData</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="29fb5-260">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="29fb5-260">Method backgroundColor</span></span>

<span data-ttu-id="29fb5-261">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-261">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="29fb5-262">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="29fb5-262">Parameters - backgroundColor</span></span>

<span data-ttu-id="29fb5-263">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-263">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="29fb5-264">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="29fb5-264">Return Value - backgroundColor</span></span>

<span data-ttu-id="29fb5-265">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="29fb5-265">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="29fb5-266">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="29fb5-266">Remarks - backgroundColor</span></span>

<span data-ttu-id="29fb5-267">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-267">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="29fb5-268">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="29fb5-268">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="29fb5-269">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="29fb5-269">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="29fb5-270">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="29fb5-270">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="29fb5-271">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="29fb5-271">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="29fb5-272">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="29fb5-272">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="29fb5-273">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="29fb5-273">Method backStyle</span></span>

<span data-ttu-id="29fb5-274">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-274">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="29fb5-275">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="29fb5-275">Parameters - backStyle</span></span>

<span data-ttu-id="29fb5-276">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-276">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="29fb5-277">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="29fb5-277">Return Value - backStyle</span></span>

<span data-ttu-id="29fb5-278">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="29fb5-278">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-big"></a><span data-ttu-id="29fb5-279">メソッド big</span><span class="sxs-lookup"><span data-stu-id="29fb5-279">Method big</span></span>

```xpp
public boolean big([boolean value])
```

### <a name="parameters---big"></a><span data-ttu-id="29fb5-280">パラメーター - big</span><span class="sxs-lookup"><span data-stu-id="29fb5-280">Parameters - big</span></span>

<span data-ttu-id="29fb5-281">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-281">value</span></span>  

### <a name="return-value---big"></a><span data-ttu-id="29fb5-282">戻り値 - big</span><span class="sxs-lookup"><span data-stu-id="29fb5-282">Return Value - big</span></span>

## <a name="method-bold"></a><span data-ttu-id="29fb5-283">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="29fb5-283">Method bold</span></span>

<span data-ttu-id="29fb5-284">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-284">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="29fb5-285">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="29fb5-285">Parameters - bold</span></span>

<span data-ttu-id="29fb5-286">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-286">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="29fb5-287">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="29fb5-287">Return Value - bold</span></span>

<span data-ttu-id="29fb5-288">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="29fb5-288">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="29fb5-289">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="29fb5-289">Remarks - bold</span></span>

<span data-ttu-id="29fb5-290">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-290">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="29fb5-291">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-291">0 Use the default font weight.</span></span>
-   <span data-ttu-id="29fb5-292">1 シン。</span><span class="sxs-lookup"><span data-stu-id="29fb5-292">1 Thin.</span></span>
-   <span data-ttu-id="29fb5-293">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="29fb5-293">2 Extra-light.</span></span>
-   <span data-ttu-id="29fb5-294">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="29fb5-294">3 Light.</span></span>
-   <span data-ttu-id="29fb5-295">4 標準。</span><span class="sxs-lookup"><span data-stu-id="29fb5-295">4 Normal.</span></span>
-   <span data-ttu-id="29fb5-296">5 中。</span><span class="sxs-lookup"><span data-stu-id="29fb5-296">5 Medium.</span></span>
-   <span data-ttu-id="29fb5-297">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="29fb5-297">6 Semibold.</span></span>
-   <span data-ttu-id="29fb5-298">7 太字。</span><span class="sxs-lookup"><span data-stu-id="29fb5-298">7 Bold.</span></span>
-   <span data-ttu-id="29fb5-299">8 極太。</span><span class="sxs-lookup"><span data-stu-id="29fb5-299">8 Extra-bold.</span></span>
-   <span data-ttu-id="29fb5-300">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="29fb5-300">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="29fb5-301">メソッド border</span><span class="sxs-lookup"><span data-stu-id="29fb5-301">Method border</span></span>

<span data-ttu-id="29fb5-302">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-302">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="29fb5-303">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="29fb5-303">Parameters - border</span></span>

<span data-ttu-id="29fb5-304">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-304">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="29fb5-305">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="29fb5-305">Return Value - border</span></span>

<span data-ttu-id="29fb5-306">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="29fb5-306">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="29fb5-307">備考 - border</span><span class="sxs-lookup"><span data-stu-id="29fb5-307">Remarks - border</span></span>

<span data-ttu-id="29fb5-308">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-308">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="29fb5-309">値です。</span><span class="sxs-lookup"><span data-stu-id="29fb5-309">Value.</span></span> | <span data-ttu-id="29fb5-310">説明。</span><span class="sxs-lookup"><span data-stu-id="29fb5-310">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="29fb5-311">0</span><span class="sxs-lookup"><span data-stu-id="29fb5-311">0</span></span>      | <span data-ttu-id="29fb5-312">自動。</span><span class="sxs-lookup"><span data-stu-id="29fb5-312">Auto.</span></span>        |
| <span data-ttu-id="29fb5-313">1</span><span class="sxs-lookup"><span data-stu-id="29fb5-313">1</span></span>      | <span data-ttu-id="29fb5-314">3D。</span><span class="sxs-lookup"><span data-stu-id="29fb5-314">3D.</span></span>          |
| <span data-ttu-id="29fb5-315">2</span><span class="sxs-lookup"><span data-stu-id="29fb5-315">2</span></span>      | <span data-ttu-id="29fb5-316">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="29fb5-316">Single line.</span></span> |
| <span data-ttu-id="29fb5-317">3</span><span class="sxs-lookup"><span data-stu-id="29fb5-317">3</span></span>      | <span data-ttu-id="29fb5-318">均一。</span><span class="sxs-lookup"><span data-stu-id="29fb5-318">Flat.</span></span>        |
| <span data-ttu-id="29fb5-319">4</span><span class="sxs-lookup"><span data-stu-id="29fb5-319">4</span></span>      | <span data-ttu-id="29fb5-320">なし。</span><span class="sxs-lookup"><span data-stu-id="29fb5-320">None.</span></span>        |

## <a name="method-buttondisplay"></a><span data-ttu-id="29fb5-321">メソッド buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="29fb5-321">Method buttonDisplay</span></span>

<span data-ttu-id="29fb5-322">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-322">Gets or sets the appearance of the button control.</span></span>

```xpp
public int buttonDisplay([int value])
```

### <a name="parameters---buttondisplay"></a><span data-ttu-id="29fb5-323">パラメーター - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="29fb5-323">Parameters - buttonDisplay</span></span>

<span data-ttu-id="29fb5-324">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-324">value</span></span>  

### <a name="return-value---buttondisplay"></a><span data-ttu-id="29fb5-325">戻り値 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="29fb5-325">Return Value - buttonDisplay</span></span>

<span data-ttu-id="29fb5-326">ゼロから 5 までの整数。</span><span class="sxs-lookup"><span data-stu-id="29fb5-326">An integer between zero and five, inclusive.</span></span>

### <a name="remarks---buttondisplay"></a><span data-ttu-id="29fb5-327">備考 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="29fb5-327">Remarks - buttonDisplay</span></span>

<span data-ttu-id="29fb5-328">プロパティ値は、テキスト、画像、またはその両方のいずれをボタンに表示するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-328">The value of the property defines whether the text, the image, or both should be displayed on the button.</span></span> <span data-ttu-id="29fb5-329">このプロパティは、テキストと画像の両方が表示されている場合は、テキストと画像の相対位置も制御します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-329">This property also controls relative positions of text and image if both are displayed.</span></span> <span data-ttu-id="29fb5-330">返される整数値には、次のようなボタン コントロールの外観が含まれます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-330">The integer value that is returned contains the appearance of the button control as follows:</span></span>

| <span data-ttu-id="29fb5-331">値です。</span><span class="sxs-lookup"><span data-stu-id="29fb5-331">Value.</span></span> | <span data-ttu-id="29fb5-332">説明。</span><span class="sxs-lookup"><span data-stu-id="29fb5-332">Description.</span></span>                                                     |
|--------|------------------------------------------------------------------|
| <span data-ttu-id="29fb5-333">0</span><span class="sxs-lookup"><span data-stu-id="29fb5-333">0</span></span>      | <span data-ttu-id="29fb5-334">テキストのみ。</span><span class="sxs-lookup"><span data-stu-id="29fb5-334">Text only.</span></span>                                                       |
| <span data-ttu-id="29fb5-335">1</span><span class="sxs-lookup"><span data-stu-id="29fb5-335">1</span></span>      | <span data-ttu-id="29fb5-336">イメージのみ。</span><span class="sxs-lookup"><span data-stu-id="29fb5-336">Image Only.</span></span>                                                      |
| <span data-ttu-id="29fb5-337">2</span><span class="sxs-lookup"><span data-stu-id="29fb5-337">2</span></span>      | <span data-ttu-id="29fb5-338">テキストと画像。画像はテキストの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-338">Text and image; the image is displayed below the text.</span></span>           |
| <span data-ttu-id="29fb5-339">3</span><span class="sxs-lookup"><span data-stu-id="29fb5-339">3</span></span>      | <span data-ttu-id="29fb5-340">テキストと画像。画像はテキストの上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-340">Text and image; the image is displayed above the text.</span></span>           |
| <span data-ttu-id="29fb5-341">4</span><span class="sxs-lookup"><span data-stu-id="29fb5-341">4</span></span>      | <span data-ttu-id="29fb5-342">テキストと画像。画像はテキストの左に表示されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-342">Text and image; the image is displayed to the left of the text.</span></span>  |
| <span data-ttu-id="29fb5-343">5</span><span class="sxs-lookup"><span data-stu-id="29fb5-343">5</span></span>      | <span data-ttu-id="29fb5-344">テキストと画像。画像はテキストの右に表示されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-344">Text and image; the image is displayed to the right of the text.</span></span> |

## <a name="method-caption"></a><span data-ttu-id="29fb5-345">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="29fb5-345">Method caption</span></span>

<span data-ttu-id="29fb5-346">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-346">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="29fb5-347">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="29fb5-347">Parameters - caption</span></span>

<span data-ttu-id="29fb5-348">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-348">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="29fb5-349">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="29fb5-349">Return Value - caption</span></span>

<span data-ttu-id="29fb5-350">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="29fb5-350">The string that is used as the caption of the control.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="29fb5-351">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="29fb5-351">Method characterSet</span></span>

<span data-ttu-id="29fb5-352">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-352">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="29fb5-353">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="29fb5-353">Parameters - characterSet</span></span>

<span data-ttu-id="29fb5-354">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-354">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="29fb5-355">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="29fb5-355">Return Value - characterSet</span></span>

<span data-ttu-id="29fb5-356">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29fb5-356">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="29fb5-357">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="29fb5-357">Remarks - characterSet</span></span>

<span data-ttu-id="29fb5-358">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-358">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="29fb5-359">値です。</span><span class="sxs-lookup"><span data-stu-id="29fb5-359">Value.</span></span> | <span data-ttu-id="29fb5-360">説明。</span><span class="sxs-lookup"><span data-stu-id="29fb5-360">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="29fb5-361">0</span><span class="sxs-lookup"><span data-stu-id="29fb5-361">0</span></span>      | <span data-ttu-id="29fb5-362">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="29fb5-362">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="29fb5-363">1</span><span class="sxs-lookup"><span data-stu-id="29fb5-363">1</span></span>      | <span data-ttu-id="29fb5-364">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="29fb5-364">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="29fb5-365">2</span><span class="sxs-lookup"><span data-stu-id="29fb5-365">2</span></span>      | <span data-ttu-id="29fb5-366">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="29fb5-366">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="29fb5-367">77</span><span class="sxs-lookup"><span data-stu-id="29fb5-367">77</span></span>     | <span data-ttu-id="29fb5-368">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="29fb5-368">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="29fb5-369">128</span><span class="sxs-lookup"><span data-stu-id="29fb5-369">128</span></span>    | <span data-ttu-id="29fb5-370">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="29fb5-370">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="29fb5-371">129</span><span class="sxs-lookup"><span data-stu-id="29fb5-371">129</span></span>    | <span data-ttu-id="29fb5-372">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="29fb5-372">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="29fb5-373">134</span><span class="sxs-lookup"><span data-stu-id="29fb5-373">134</span></span>    | <span data-ttu-id="29fb5-374">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="29fb5-374">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="29fb5-375">136</span><span class="sxs-lookup"><span data-stu-id="29fb5-375">136</span></span>    | <span data-ttu-id="29fb5-376">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="29fb5-376">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="29fb5-377">161</span><span class="sxs-lookup"><span data-stu-id="29fb5-377">161</span></span>    | <span data-ttu-id="29fb5-378">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="29fb5-378">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="29fb5-379">162</span><span class="sxs-lookup"><span data-stu-id="29fb5-379">162</span></span>    | <span data-ttu-id="29fb5-380">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="29fb5-380">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="29fb5-381">163</span><span class="sxs-lookup"><span data-stu-id="29fb5-381">163</span></span>    | <span data-ttu-id="29fb5-382">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="29fb5-382">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="29fb5-383">186</span><span class="sxs-lookup"><span data-stu-id="29fb5-383">186</span></span>    | <span data-ttu-id="29fb5-384">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="29fb5-384">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="29fb5-385">204</span><span class="sxs-lookup"><span data-stu-id="29fb5-385">204</span></span>    | <span data-ttu-id="29fb5-386">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="29fb5-386">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="29fb5-387">238</span><span class="sxs-lookup"><span data-stu-id="29fb5-387">238</span></span>    | <span data-ttu-id="29fb5-388">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="29fb5-388">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="29fb5-389">255</span><span class="sxs-lookup"><span data-stu-id="29fb5-389">255</span></span>    | <span data-ttu-id="29fb5-390">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="29fb5-390">OEM\_CHARSET</span></span>         |

<span data-ttu-id="29fb5-391">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="29fb5-391">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="29fb5-392">値です。</span><span class="sxs-lookup"><span data-stu-id="29fb5-392">Value.</span></span> | <span data-ttu-id="29fb5-393">説明。</span><span class="sxs-lookup"><span data-stu-id="29fb5-393">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="29fb5-394">130</span><span class="sxs-lookup"><span data-stu-id="29fb5-394">130</span></span>    | <span data-ttu-id="29fb5-395">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="29fb5-395">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="29fb5-396">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="29fb5-396">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="29fb5-397">値です。</span><span class="sxs-lookup"><span data-stu-id="29fb5-397">Value.</span></span> | <span data-ttu-id="29fb5-398">説明。</span><span class="sxs-lookup"><span data-stu-id="29fb5-398">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="29fb5-399">177</span><span class="sxs-lookup"><span data-stu-id="29fb5-399">177</span></span>    | <span data-ttu-id="29fb5-400">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="29fb5-400">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="29fb5-401">178</span><span class="sxs-lookup"><span data-stu-id="29fb5-401">178</span></span>    | <span data-ttu-id="29fb5-402">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="29fb5-402">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="29fb5-403">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="29fb5-403">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="29fb5-404">値です。</span><span class="sxs-lookup"><span data-stu-id="29fb5-404">Value.</span></span> | <span data-ttu-id="29fb5-405">説明。</span><span class="sxs-lookup"><span data-stu-id="29fb5-405">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="29fb5-406">222</span><span class="sxs-lookup"><span data-stu-id="29fb5-406">222</span></span>    | <span data-ttu-id="29fb5-407">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="29fb5-407">THAI\_CHARSET</span></span> |

<span data-ttu-id="29fb5-408">既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-408">The default character set is set to a value that is based on the current system locale.</span></span> <span data-ttu-id="29fb5-409">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-409">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="29fb5-410">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="29fb5-410">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="29fb5-411">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="29fb5-411">Method colorScheme</span></span>

<span data-ttu-id="29fb5-412">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-412">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="29fb5-413">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="29fb5-413">Parameters - colorScheme</span></span>

<span data-ttu-id="29fb5-414">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-414">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="29fb5-415">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="29fb5-415">Return Value - colorScheme</span></span>

<span data-ttu-id="29fb5-416">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="29fb5-416">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="29fb5-417">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="29fb5-417">Remarks - colorScheme</span></span>

<span data-ttu-id="29fb5-418">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-418">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="29fb5-419">値です。</span><span class="sxs-lookup"><span data-stu-id="29fb5-419">Value.</span></span> | <span data-ttu-id="29fb5-420">スタイル。</span><span class="sxs-lookup"><span data-stu-id="29fb5-420">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="29fb5-421">0</span><span class="sxs-lookup"><span data-stu-id="29fb5-421">0</span></span>      | <span data-ttu-id="29fb5-422">既定。</span><span class="sxs-lookup"><span data-stu-id="29fb5-422">Default.</span></span>                      |
| <span data-ttu-id="29fb5-423">1</span><span class="sxs-lookup"><span data-stu-id="29fb5-423">1</span></span>      | <span data-ttu-id="29fb5-424">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="29fb5-424">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="29fb5-425">2</span><span class="sxs-lookup"><span data-stu-id="29fb5-425">2</span></span>      | <span data-ttu-id="29fb5-426">真の配色。</span><span class="sxs-lookup"><span data-stu-id="29fb5-426">The true-color scheme.</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="29fb5-427">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="29fb5-427">Method configurationKey</span></span>

<span data-ttu-id="29fb5-428">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-428">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="29fb5-429">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="29fb5-429">Parameters - configurationKey</span></span>

<span data-ttu-id="29fb5-430">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-430">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="29fb5-431">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="29fb5-431">Return Value - configurationKey</span></span>

<span data-ttu-id="29fb5-432">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="29fb5-432">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="29fb5-433">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="29fb5-433">Remarks - configurationKey</span></span>

<span data-ttu-id="29fb5-434">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-434">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="29fb5-435">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="29fb5-435">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="29fb5-436">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="29fb5-436">Method containerId</span></span>

<span data-ttu-id="29fb5-437">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-437">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="29fb5-438">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="29fb5-438">Return Value - containerId</span></span>

<span data-ttu-id="29fb5-439">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="29fb5-439">The ID of the parent container.</span></span>

## <a name="method-copycallerquery"></a><span data-ttu-id="29fb5-440">メソッド copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="29fb5-440">Method copyCallerQuery</span></span>

```xpp
public int copyCallerQuery([int value])
```

### <a name="parameters---copycallerquery"></a><span data-ttu-id="29fb5-441">パラメーター - copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="29fb5-441">Parameters - copyCallerQuery</span></span>

<span data-ttu-id="29fb5-442">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-442">value</span></span>  

### <a name="return-value---copycallerquery"></a><span data-ttu-id="29fb5-443">戻り値 - copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="29fb5-443">Return Value - copyCallerQuery</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="29fb5-444">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="29fb5-444">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="29fb5-445">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="29fb5-445">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="29fb5-446">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-446">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="29fb5-447">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="29fb5-447">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="29fb5-448">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="29fb5-448">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="29fb5-449">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="29fb5-449">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="29fb5-450">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-450">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="29fb5-451">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="29fb5-451">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="29fb5-452">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="29fb5-452">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="29fb5-453">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="29fb5-453">Parameters - dataRelationPath</span></span>

<span data-ttu-id="29fb5-454">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-454">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="29fb5-455">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="29fb5-455">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="29fb5-456">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="29fb5-456">Method dataSource</span></span>

<span data-ttu-id="29fb5-457">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-457">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="29fb5-458">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="29fb5-458">Parameters - dataSource</span></span>

<span data-ttu-id="29fb5-459">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-459">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="29fb5-460">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="29fb5-460">Return Value - dataSource</span></span>

<span data-ttu-id="29fb5-461">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="29fb5-461">The identifier of the data source that will be used.</span></span>

## <a name="method-defaultbutton"></a><span data-ttu-id="29fb5-462">メソッド defaultButton</span><span class="sxs-lookup"><span data-stu-id="29fb5-462">Method defaultButton</span></span>

<span data-ttu-id="29fb5-463">ボタンをフォーム上の既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-463">Determines whether the button should be the default button on the form.</span></span>

```xpp
public boolean defaultButton([boolean value])
```

### <a name="parameters---defaultbutton"></a><span data-ttu-id="29fb5-464">パラメーター - defaultButton</span><span class="sxs-lookup"><span data-stu-id="29fb5-464">Parameters - defaultButton</span></span>

<span data-ttu-id="29fb5-465">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-465">value</span></span>  

### <a name="return-value---defaultbutton"></a><span data-ttu-id="29fb5-466">戻り値 - defaultButton</span><span class="sxs-lookup"><span data-stu-id="29fb5-466">Return Value - defaultButton</span></span>

<span data-ttu-id="29fb5-467">ボタンが既定のボタンである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="29fb5-467">true if the button should be the default button; otherwise, false.</span></span>

## <a name="method-disabledimage"></a><span data-ttu-id="29fb5-468">メソッド disabledImage</span><span class="sxs-lookup"><span data-stu-id="29fb5-468">Method disabledImage</span></span>

<span data-ttu-id="29fb5-469">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-469">Gets or sets the disabled image of the button.</span></span>

```xpp
public str disabledImage([str value])
```

### <a name="parameters---disabledimage"></a><span data-ttu-id="29fb5-470">パラメーター - disabledImage</span><span class="sxs-lookup"><span data-stu-id="29fb5-470">Parameters - disabledImage</span></span>

<span data-ttu-id="29fb5-471">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-471">value</span></span>  

### <a name="return-value---disabledimage"></a><span data-ttu-id="29fb5-472">戻り値 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="29fb5-472">Return Value - disabledImage</span></span>

<span data-ttu-id="29fb5-473">画像ファイルのフル ネーム。</span><span class="sxs-lookup"><span data-stu-id="29fb5-473">The full name of an image file.</span></span> <span data-ttu-id="29fb5-474">システムは、GDI でサポートされているすべてのイメージ形式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="29fb5-474">The system supports all of the GDI-supported image formats.</span></span>

### <a name="remarks---disabledimage"></a><span data-ttu-id="29fb5-475">備考 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="29fb5-475">Remarks - disabledImage</span></span>

<span data-ttu-id="29fb5-476">このプロパティは、disabledResource プロパティに優先します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-476">This property has precedence over the disabledResource property .</span></span> <span data-ttu-id="29fb5-477">これらのプロパティの両方が設定されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-477">It is used if both of these properties are set.</span></span>

## <a name="method-disabledimagelocation"></a><span data-ttu-id="29fb5-478">メソッド disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="29fb5-478">Method disabledImageLocation</span></span>

```xpp
public int disabledImageLocation([int value])
```

### <a name="parameters---disabledimagelocation"></a><span data-ttu-id="29fb5-479">パラメーター - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="29fb5-479">Parameters - disabledImageLocation</span></span>

<span data-ttu-id="29fb5-480">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-480">value</span></span>  

### <a name="return-value---disabledimagelocation"></a><span data-ttu-id="29fb5-481">戻り値 - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="29fb5-481">Return Value - disabledImageLocation</span></span>

## <a name="method-disabledresource"></a><span data-ttu-id="29fb5-482">メソッド disabledResource</span><span class="sxs-lookup"><span data-stu-id="29fb5-482">Method disabledResource</span></span>

<span data-ttu-id="29fb5-483">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-483">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>

```xpp
public int disabledResource([int value])
```

### <a name="parameters---disabledresource"></a><span data-ttu-id="29fb5-484">パラメーター - disabledResource</span><span class="sxs-lookup"><span data-stu-id="29fb5-484">Parameters - disabledResource</span></span>

<span data-ttu-id="29fb5-485">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-485">value</span></span>  

### <a name="return-value---disabledresource"></a><span data-ttu-id="29fb5-486">戻り値 - disabledResource</span><span class="sxs-lookup"><span data-stu-id="29fb5-486">Return Value - disabledResource</span></span>

<span data-ttu-id="29fb5-487">無効なボタン画像として使用する画像リソース ID。</span><span class="sxs-lookup"><span data-stu-id="29fb5-487">The resource ID of the image to use as the disabled button image.</span></span> <span data-ttu-id="29fb5-488">アイコンとビットマップ イメージの両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-488">Both icon and bitmap images are supported.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="29fb5-489">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="29fb5-489">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="29fb5-490">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="29fb5-490">Parameters - displayTarget</span></span>

<span data-ttu-id="29fb5-491">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-491">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="29fb5-492">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="29fb5-492">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="29fb5-493">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="29fb5-493">Method dragDrop</span></span>

<span data-ttu-id="29fb5-494">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-494">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="29fb5-495">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="29fb5-495">Parameters - dragDrop</span></span>

<span data-ttu-id="29fb5-496">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-496">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="29fb5-497">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="29fb5-497">Return Value - dragDrop</span></span>

<span data-ttu-id="29fb5-498">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="29fb5-498">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="29fb5-499">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="29fb5-499">Method enabled</span></span>

<span data-ttu-id="29fb5-500">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-500">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="29fb5-501">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="29fb5-501">Parameters - enabled</span></span>

<span data-ttu-id="29fb5-502">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-502">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="29fb5-503">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="29fb5-503">Return Value - enabled</span></span>

<span data-ttu-id="29fb5-504">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="29fb5-504">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="29fb5-505">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="29fb5-505">Remarks - enabled</span></span>

<span data-ttu-id="29fb5-506">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-506">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="29fb5-507">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-507">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="29fb5-508">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-508">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="29fb5-509">メソッド font</span><span class="sxs-lookup"><span data-stu-id="29fb5-509">Method font</span></span>

<span data-ttu-id="29fb5-510">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-510">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="29fb5-511">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="29fb5-511">Parameters - font</span></span>

<span data-ttu-id="29fb5-512">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-512">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="29fb5-513">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="29fb5-513">Return Value - font</span></span>

<span data-ttu-id="29fb5-514">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="29fb5-514">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="29fb5-515">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="29fb5-515">Method fontSize</span></span>

<span data-ttu-id="29fb5-516">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-516">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="29fb5-517">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="29fb5-517">Parameters - fontSize</span></span>

<span data-ttu-id="29fb5-518">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-518">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="29fb5-519">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="29fb5-519">Return Value - fontSize</span></span>

<span data-ttu-id="29fb5-520">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="29fb5-520">The height of the font in points.</span></span>

## <a name="method-forcedtooverflow"></a><span data-ttu-id="29fb5-521">メソッド forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="29fb5-521">Method forcedToOverflow</span></span>

```xpp
public boolean forcedToOverflow([boolean value])
```

### <a name="parameters---forcedtooverflow"></a><span data-ttu-id="29fb5-522">パラメーター - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="29fb5-522">Parameters - forcedToOverflow</span></span>

<span data-ttu-id="29fb5-523">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-523">value</span></span>  

### <a name="return-value---forcedtooverflow"></a><span data-ttu-id="29fb5-524">戻り値 - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="29fb5-524">Return Value - forcedToOverflow</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="29fb5-525">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="29fb5-525">Method foregroundColor</span></span>

<span data-ttu-id="29fb5-526">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-526">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="29fb5-527">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="29fb5-527">Parameters - foregroundColor</span></span>

<span data-ttu-id="29fb5-528">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-528">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="29fb5-529">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="29fb5-529">Return Value - foregroundColor</span></span>

<span data-ttu-id="29fb5-530">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="29fb5-530">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="29fb5-531">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="29fb5-531">Remarks - foregroundColor</span></span>

<span data-ttu-id="29fb5-532">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-532">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="29fb5-533">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="29fb5-533">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="29fb5-534">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="29fb5-534">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="29fb5-535">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="29fb5-535">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="29fb5-536">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="29fb5-536">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="29fb5-537">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="29fb5-537">The maximum value for a single byte is 255.</span></span>

## <a name="method-formviewoption"></a><span data-ttu-id="29fb5-538">メソッド formViewOption</span><span class="sxs-lookup"><span data-stu-id="29fb5-538">Method formViewOption</span></span>

```xpp
public int formViewOption([int value])
```

### <a name="parameters---formviewoption"></a><span data-ttu-id="29fb5-539">パラメータ-formViewOption</span><span class="sxs-lookup"><span data-stu-id="29fb5-539">Parameters - formViewOption</span></span>

<span data-ttu-id="29fb5-540">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-540">value</span></span>  

### <a name="return-value---formviewoption"></a><span data-ttu-id="29fb5-541">戻り値 - formViewOption</span><span class="sxs-lookup"><span data-stu-id="29fb5-541">Return Value - formViewOption</span></span>

## <a name="method-height"></a><span data-ttu-id="29fb5-542">メソッド height</span><span class="sxs-lookup"><span data-stu-id="29fb5-542">Method height</span></span>

<span data-ttu-id="29fb5-543">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-543">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="29fb5-544">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="29fb5-544">Parameters - height</span></span>

<span data-ttu-id="29fb5-545">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-545">value</span></span>  

<!-- -->

<span data-ttu-id="29fb5-546">モード</span><span class="sxs-lookup"><span data-stu-id="29fb5-546">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="29fb5-547">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="29fb5-547">Return Value - height</span></span>

<span data-ttu-id="29fb5-548">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="29fb5-548">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="29fb5-549">備考 - height</span><span class="sxs-lookup"><span data-stu-id="29fb5-549">Remarks - height</span></span>

<span data-ttu-id="29fb5-550">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-550">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="29fb5-551">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="29fb5-551">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="29fb5-552">モード。</span><span class="sxs-lookup"><span data-stu-id="29fb5-552">Mode.</span></span>            | <span data-ttu-id="29fb5-553">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="29fb5-553">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="29fb5-554">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="29fb5-554">-1 Exact.</span></span>        | <span data-ttu-id="29fb5-555">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-555">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="29fb5-556">0 自動。</span><span class="sxs-lookup"><span data-stu-id="29fb5-556">0 Auto.</span></span>          | <span data-ttu-id="29fb5-557">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-557">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="29fb5-558">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="29fb5-558">1 Column height.</span></span> | <span data-ttu-id="29fb5-559">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="29fb5-559">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="29fb5-560">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-560">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="29fb5-561">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="29fb5-561">Method heightMode</span></span>

<span data-ttu-id="29fb5-562">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-562">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="29fb5-563">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="29fb5-563">Parameters - heightMode</span></span>

<span data-ttu-id="29fb5-564">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-564">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="29fb5-565">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="29fb5-565">Return Value - heightMode</span></span>

<span data-ttu-id="29fb5-566">計算モード。</span><span class="sxs-lookup"><span data-stu-id="29fb5-566">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="29fb5-567">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="29fb5-567">Remarks - heightMode</span></span>

<span data-ttu-id="29fb5-568">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="29fb5-568">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="29fb5-569">モード。</span><span class="sxs-lookup"><span data-stu-id="29fb5-569">Mode.</span></span>          | <span data-ttu-id="29fb5-570">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="29fb5-570">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="29fb5-571">正確。</span><span class="sxs-lookup"><span data-stu-id="29fb5-571">Exact.</span></span>         | <span data-ttu-id="29fb5-572">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-572">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="29fb5-573">自動。</span><span class="sxs-lookup"><span data-stu-id="29fb5-573">Auto.</span></span>          | <span data-ttu-id="29fb5-574">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-574">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="29fb5-575">列の高さ</span><span class="sxs-lookup"><span data-stu-id="29fb5-575">Column height.</span></span> | <span data-ttu-id="29fb5-576">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="29fb5-576">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="29fb5-577">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="29fb5-577">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="29fb5-578">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="29fb5-578">Method heightValue</span></span>

<span data-ttu-id="29fb5-579">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-579">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="29fb5-580">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="29fb5-580">Parameters - heightValue</span></span>

<span data-ttu-id="29fb5-581">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-581">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="29fb5-582">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="29fb5-582">Return Value - heightValue</span></span>

<span data-ttu-id="29fb5-583">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="29fb5-583">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="29fb5-584">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="29fb5-584">Remarks - heightValue</span></span>

<span data-ttu-id="29fb5-585">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="29fb5-585">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="29fb5-586">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="29fb5-586">Method helpText</span></span>

<span data-ttu-id="29fb5-587">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-587">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="29fb5-588">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="29fb5-588">Parameters - helpText</span></span>

<span data-ttu-id="29fb5-589">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-589">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="29fb5-590">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="29fb5-590">Return Value - helpText</span></span>

<span data-ttu-id="29fb5-591">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="29fb5-591">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="29fb5-592">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="29fb5-592">Remarks - helpText</span></span>

<span data-ttu-id="29fb5-593">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-593">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="29fb5-594">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="29fb5-594">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="29fb5-595">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="29fb5-595">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="29fb5-596">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="29fb5-596">Parameters - hierarchyParent</span></span>

<span data-ttu-id="29fb5-597">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-597">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="29fb5-598">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="29fb5-598">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="29fb5-599">メソッド id</span><span class="sxs-lookup"><span data-stu-id="29fb5-599">Method id</span></span>

<span data-ttu-id="29fb5-600">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-600">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="29fb5-601">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="29fb5-601">Return Value - id</span></span>

<span data-ttu-id="29fb5-602">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="29fb5-602">The ID of the control.</span></span>

## <a name="method-imagelocation"></a><span data-ttu-id="29fb5-603">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="29fb5-603">Method imageLocation</span></span>

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a><span data-ttu-id="29fb5-604">パラメーター - imageLocation</span><span class="sxs-lookup"><span data-stu-id="29fb5-604">Parameters - imageLocation</span></span>

<span data-ttu-id="29fb5-605">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-605">value</span></span>  

### <a name="return-value---imagelocation"></a><span data-ttu-id="29fb5-606">戻り値 - imageLocation</span><span class="sxs-lookup"><span data-stu-id="29fb5-606">Return Value - imageLocation</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="29fb5-607">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="29fb5-607">Method isContainer</span></span>

<span data-ttu-id="29fb5-608">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-608">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="29fb5-609">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="29fb5-609">Return Value - isContainer</span></span>

<span data-ttu-id="29fb5-610">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="29fb5-610">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="29fb5-611">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="29fb5-611">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="29fb5-612">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="29fb5-612">Parameters - italic</span></span>

<span data-ttu-id="29fb5-613">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-613">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="29fb5-614">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="29fb5-614">Return Value - italic</span></span>

## <a name="method-keytip"></a><span data-ttu-id="29fb5-615">メソッド keyTip</span><span class="sxs-lookup"><span data-stu-id="29fb5-615">Method keyTip</span></span>

```xpp
public str keyTip([str value])
```

### <a name="parameters---keytip"></a><span data-ttu-id="29fb5-616">パラメーター - keyTip</span><span class="sxs-lookup"><span data-stu-id="29fb5-616">Parameters - keyTip</span></span>

<span data-ttu-id="29fb5-617">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-617">value</span></span>  

### <a name="return-value---keytip"></a><span data-ttu-id="29fb5-618">戻り値 - keyTip</span><span class="sxs-lookup"><span data-stu-id="29fb5-618">Return Value - keyTip</span></span>

## <a name="method-left"></a><span data-ttu-id="29fb5-619">メソッド left</span><span class="sxs-lookup"><span data-stu-id="29fb5-619">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="29fb5-620">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="29fb5-620">Parameters - left</span></span>

<span data-ttu-id="29fb5-621">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-621">value</span></span>  

<!-- -->

<span data-ttu-id="29fb5-622">モード</span><span class="sxs-lookup"><span data-stu-id="29fb5-622">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="29fb5-623">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="29fb5-623">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="29fb5-624">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="29fb5-624">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="29fb5-625">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="29fb5-625">Parameters - leftMode</span></span>

<span data-ttu-id="29fb5-626">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-626">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="29fb5-627">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="29fb5-627">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="29fb5-628">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="29fb5-628">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="29fb5-629">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="29fb5-629">Parameters - leftValue</span></span>

<span data-ttu-id="29fb5-630">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-630">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="29fb5-631">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="29fb5-631">Return Value - leftValue</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="29fb5-632">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="29fb5-632">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="29fb5-633">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="29fb5-633">Parameters - menuItemName</span></span>

<span data-ttu-id="29fb5-634">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-634">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="29fb5-635">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="29fb5-635">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="29fb5-636">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="29fb5-636">Method menuItemType</span></span>

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="29fb5-637">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="29fb5-637">Parameters - menuItemType</span></span>

<span data-ttu-id="29fb5-638">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-638">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="29fb5-639">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="29fb5-639">Return Value - menuItemType</span></span>

## <a name="method-multiselect"></a><span data-ttu-id="29fb5-640">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="29fb5-640">Method multiSelect</span></span>

```xpp
public int multiSelect([int value])
```

### <a name="parameters---multiselect"></a><span data-ttu-id="29fb5-641">パラメーター - multiSelect</span><span class="sxs-lookup"><span data-stu-id="29fb5-641">Parameters - multiSelect</span></span>

<span data-ttu-id="29fb5-642">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-642">value</span></span>  

### <a name="return-value---multiselect"></a><span data-ttu-id="29fb5-643">戻り値 - multiSelect</span><span class="sxs-lookup"><span data-stu-id="29fb5-643">Return Value - multiSelect</span></span>

## <a name="method-name"></a><span data-ttu-id="29fb5-644">メソッド名</span><span class="sxs-lookup"><span data-stu-id="29fb5-644">Method name</span></span>

<span data-ttu-id="29fb5-645">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-645">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="29fb5-646">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="29fb5-646">Parameters - name</span></span>

<span data-ttu-id="29fb5-647">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-647">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="29fb5-648">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="29fb5-648">Return Value - name</span></span>

<span data-ttu-id="29fb5-649">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="29fb5-649">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="29fb5-650">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="29fb5-650">Remarks - name</span></span>

<span data-ttu-id="29fb5-651">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="29fb5-651">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="29fb5-652">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="29fb5-652">It must start with a letter.</span></span>
-   <span data-ttu-id="29fb5-653">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="29fb5-653">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="29fb5-654">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-654">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="29fb5-655">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="29fb5-655">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="29fb5-656">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="29fb5-656">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="29fb5-657">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="29fb5-657">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="29fb5-658">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="29fb5-658">Parameters - neededPermission</span></span>

<span data-ttu-id="29fb5-659">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-659">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="29fb5-660">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="29fb5-660">Return Value - neededPermission</span></span>

## <a name="method-needsrecord"></a><span data-ttu-id="29fb5-661">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="29fb5-661">Method needsRecord</span></span>

```xpp
public int needsRecord([int value])
```

### <a name="parameters---needsrecord"></a><span data-ttu-id="29fb5-662">パラメーター - needsRecord</span><span class="sxs-lookup"><span data-stu-id="29fb5-662">Parameters - needsRecord</span></span>

<span data-ttu-id="29fb5-663">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-663">value</span></span>  

### <a name="return-value---needsrecord"></a><span data-ttu-id="29fb5-664">戻り値 - needsRecord</span><span class="sxs-lookup"><span data-stu-id="29fb5-664">Return Value - needsRecord</span></span>

## <a name="method-normalimage"></a><span data-ttu-id="29fb5-665">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="29fb5-665">Method normalImage</span></span>

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a><span data-ttu-id="29fb5-666">パラメーター - normalImage</span><span class="sxs-lookup"><span data-stu-id="29fb5-666">Parameters - normalImage</span></span>

<span data-ttu-id="29fb5-667">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-667">value</span></span>  

### <a name="return-value---normalimage"></a><span data-ttu-id="29fb5-668">戻り値 - normalImage</span><span class="sxs-lookup"><span data-stu-id="29fb5-668">Return Value - normalImage</span></span>

## <a name="method-normalresource"></a><span data-ttu-id="29fb5-669">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="29fb5-669">Method normalResource</span></span>

```xpp
public int normalResource([int value])
```

### <a name="parameters---normalresource"></a><span data-ttu-id="29fb5-670">パラメーター - normalResource</span><span class="sxs-lookup"><span data-stu-id="29fb5-670">Parameters - normalResource</span></span>

<span data-ttu-id="29fb5-671">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-671">value</span></span>  

### <a name="return-value---normalresource"></a><span data-ttu-id="29fb5-672">戻り値 - normalResource</span><span class="sxs-lookup"><span data-stu-id="29fb5-672">Return Value - normalResource</span></span>

## <a name="method-openmode"></a><span data-ttu-id="29fb5-673">メソッド openMode</span><span class="sxs-lookup"><span data-stu-id="29fb5-673">Method openMode</span></span>

```xpp
public int openMode([int value])
```

### <a name="parameters---openmode"></a><span data-ttu-id="29fb5-674">パラメーター - openMode</span><span class="sxs-lookup"><span data-stu-id="29fb5-674">Parameters - openMode</span></span>

<span data-ttu-id="29fb5-675">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-675">value</span></span>  

### <a name="return-value---openmode"></a><span data-ttu-id="29fb5-676">戻り値 - openMode</span><span class="sxs-lookup"><span data-stu-id="29fb5-676">Return Value - openMode</span></span>

## <a name="method-parameters"></a><span data-ttu-id="29fb5-677">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="29fb5-677">Method parameters</span></span>

<span data-ttu-id="29fb5-678">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-678">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

```xpp
public str parameters([str value])
```

### <a name="parameters---parameters"></a><span data-ttu-id="29fb5-679">パラメーター - parameters</span><span class="sxs-lookup"><span data-stu-id="29fb5-679">Parameters - parameters</span></span>

<span data-ttu-id="29fb5-680">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-680">value</span></span>  

### <a name="return-value---parameters"></a><span data-ttu-id="29fb5-681">戻り値 - parameters</span><span class="sxs-lookup"><span data-stu-id="29fb5-681">Return Value - parameters</span></span>

<span data-ttu-id="29fb5-682">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="29fb5-682">The list of parameters that are passed to the object.</span></span>

### <a name="remarks---parameters"></a><span data-ttu-id="29fb5-683">備考 - パラメータ</span><span class="sxs-lookup"><span data-stu-id="29fb5-683">Remarks - parameters</span></span>

<span data-ttu-id="29fb5-684">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="29fb5-684">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="29fb5-685">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-685">Objects ignore passed, unrecognized parameters.</span></span>

## <a name="method-primary"></a><span data-ttu-id="29fb5-686">メソッド primary</span><span class="sxs-lookup"><span data-stu-id="29fb5-686">Method primary</span></span>

```xpp
public boolean primary([boolean value])
```

### <a name="parameters---primary"></a><span data-ttu-id="29fb5-687">パラメーター - primary</span><span class="sxs-lookup"><span data-stu-id="29fb5-687">Parameters - primary</span></span>

<span data-ttu-id="29fb5-688">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-688">value</span></span>  

### <a name="return-value---primary"></a><span data-ttu-id="29fb5-689">戻り値 - primary</span><span class="sxs-lookup"><span data-stu-id="29fb5-689">Return Value - primary</span></span>

## <a name="method-saverecord"></a><span data-ttu-id="29fb5-690">メソッド saveRecord</span><span class="sxs-lookup"><span data-stu-id="29fb5-690">Method saveRecord</span></span>

```xpp
public boolean saveRecord([boolean value])
```

### <a name="parameters---saverecord"></a><span data-ttu-id="29fb5-691">パラメーター - saveRecord</span><span class="sxs-lookup"><span data-stu-id="29fb5-691">Parameters - saveRecord</span></span>

<span data-ttu-id="29fb5-692">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-692">value</span></span>  

### <a name="return-value---saverecord"></a><span data-ttu-id="29fb5-693">戻り値 - saveRecord</span><span class="sxs-lookup"><span data-stu-id="29fb5-693">Return Value - saveRecord</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="29fb5-694">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="29fb5-694">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="29fb5-695">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="29fb5-695">Parameters - securityKey</span></span>

<span data-ttu-id="29fb5-696">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-696">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="29fb5-697">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="29fb5-697">Return Value - securityKey</span></span>

## <a name="method-sendexternalcontext"></a><span data-ttu-id="29fb5-698">メソッド sendExternalContext</span><span class="sxs-lookup"><span data-stu-id="29fb5-698">Method sendExternalContext</span></span>

```xpp
public boolean sendExternalContext([boolean value])
```

### <a name="parameters---sendexternalcontext"></a><span data-ttu-id="29fb5-699">パラメーター - sendExternalContext</span><span class="sxs-lookup"><span data-stu-id="29fb5-699">Parameters - sendExternalContext</span></span>

<span data-ttu-id="29fb5-700">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-700">value</span></span>  

### <a name="return-value---sendexternalcontext"></a><span data-ttu-id="29fb5-701">戻り値 - sendExternalContext</span><span class="sxs-lookup"><span data-stu-id="29fb5-701">Return Value - sendExternalContext</span></span>

## <a name="method-shortkey"></a><span data-ttu-id="29fb5-702">メソッド shortkey</span><span class="sxs-lookup"><span data-stu-id="29fb5-702">Method shortkey</span></span>

```xpp
public int shortkey([int value])
```

### <a name="parameters---shortkey"></a><span data-ttu-id="29fb5-703">パラメーター - shortkey</span><span class="sxs-lookup"><span data-stu-id="29fb5-703">Parameters - shortkey</span></span>

<span data-ttu-id="29fb5-704">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-704">value</span></span>  

### <a name="return-value---shortkey"></a><span data-ttu-id="29fb5-705">戻り値 - shortkey</span><span class="sxs-lookup"><span data-stu-id="29fb5-705">Return Value - shortkey</span></span>

## <a name="method-showshortcut"></a><span data-ttu-id="29fb5-706">メソッド showShortCut</span><span class="sxs-lookup"><span data-stu-id="29fb5-706">Method showShortCut</span></span>

```xpp
public boolean showShortCut([boolean value])
```

### <a name="parameters---showshortcut"></a><span data-ttu-id="29fb5-707">パラメーター - showShortCut</span><span class="sxs-lookup"><span data-stu-id="29fb5-707">Parameters - showShortCut</span></span>

<span data-ttu-id="29fb5-708">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-708">value</span></span>  

### <a name="return-value---showshortcut"></a><span data-ttu-id="29fb5-709">戻り値 - showShortCut</span><span class="sxs-lookup"><span data-stu-id="29fb5-709">Return Value - showShortCut</span></span>

## <a name="method-skip"></a><span data-ttu-id="29fb5-710">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="29fb5-710">Method skip</span></span>

<span data-ttu-id="29fb5-711">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-711">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="29fb5-712">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="29fb5-712">Parameters - skip</span></span>

<span data-ttu-id="29fb5-713">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-713">value</span></span>  
<span data-ttu-id="29fb5-714">コントロールの skip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="29fb5-714">The value to assign to the skip property of the control.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="29fb5-715">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="29fb5-715">Return Value - skip</span></span>

<span data-ttu-id="29fb5-716">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="29fb5-716">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-style"></a><span data-ttu-id="29fb5-717">メソッド style</span><span class="sxs-lookup"><span data-stu-id="29fb5-717">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="29fb5-718">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="29fb5-718">Parameters - style</span></span>

<span data-ttu-id="29fb5-719">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-719">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="29fb5-720">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="29fb5-720">Return Value - style</span></span>

## <a name="method-text"></a><span data-ttu-id="29fb5-721">メソッド text</span><span class="sxs-lookup"><span data-stu-id="29fb5-721">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="29fb5-722">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="29fb5-722">Parameters - text</span></span>

<span data-ttu-id="29fb5-723">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-723">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="29fb5-724">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="29fb5-724">Return Value - text</span></span>

## <a name="method-top"></a><span data-ttu-id="29fb5-725">メソッド top</span><span class="sxs-lookup"><span data-stu-id="29fb5-725">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="29fb5-726">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="29fb5-726">Parameters - top</span></span>

<span data-ttu-id="29fb5-727">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-727">value</span></span>  

<!-- -->

<span data-ttu-id="29fb5-728">モード</span><span class="sxs-lookup"><span data-stu-id="29fb5-728">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="29fb5-729">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="29fb5-729">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="29fb5-730">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="29fb5-730">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="29fb5-731">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="29fb5-731">Parameters - topMode</span></span>

<span data-ttu-id="29fb5-732">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-732">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="29fb5-733">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="29fb5-733">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="29fb5-734">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="29fb5-734">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="29fb5-735">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="29fb5-735">Parameters - topValue</span></span>

<span data-ttu-id="29fb5-736">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-736">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="29fb5-737">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="29fb5-737">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="29fb5-738">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="29fb5-738">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="29fb5-739">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="29fb5-739">Parameters - type</span></span>

<span data-ttu-id="29fb5-740">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-740">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="29fb5-741">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="29fb5-741">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="29fb5-742">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="29fb5-742">Method underline</span></span>

<span data-ttu-id="29fb5-743">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-743">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="29fb5-744">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="29fb5-744">Parameters - underline</span></span>

<span data-ttu-id="29fb5-745">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-745">value</span></span>  
<span data-ttu-id="29fb5-746">コントロールの underline プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="29fb5-746">The value to assign to the underline property of the control.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="29fb5-747">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="29fb5-747">Return Value - underline</span></span>

<span data-ttu-id="29fb5-748">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="29fb5-748">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-userdata"></a><span data-ttu-id="29fb5-749">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="29fb5-749">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="29fb5-750">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="29fb5-750">Parameters - userData</span></span>

<span data-ttu-id="29fb5-751">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-751">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="29fb5-752">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="29fb5-752">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="29fb5-753">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="29fb5-753">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="29fb5-754">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="29fb5-754">Parameters - userDataItem</span></span>

<span data-ttu-id="29fb5-755">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-755">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="29fb5-756">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="29fb5-756">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="29fb5-757">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="29fb5-757">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="29fb5-758">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="29fb5-758">Parameters - userDataItems</span></span>

<span data-ttu-id="29fb5-759">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-759">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="29fb5-760">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="29fb5-760">Return Value - userDataItems</span></span>

## <a name="method-value"></a><span data-ttu-id="29fb5-761">メソッド value</span><span class="sxs-lookup"><span data-stu-id="29fb5-761">Method value</span></span>

```xpp
public boolean value([boolean value])
```

### <a name="parameters---value"></a><span data-ttu-id="29fb5-762">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="29fb5-762">Parameters - value</span></span>

<span data-ttu-id="29fb5-763">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-763">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="29fb5-764">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="29fb5-764">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="29fb5-765">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="29fb5-765">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="29fb5-766">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="29fb5-766">Parameters - verticalSpacing</span></span>

<span data-ttu-id="29fb5-767">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-767">value</span></span>  

<!-- -->

<span data-ttu-id="29fb5-768">モード</span><span class="sxs-lookup"><span data-stu-id="29fb5-768">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="29fb5-769">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="29fb5-769">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="29fb5-770">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="29fb5-770">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="29fb5-771">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="29fb5-771">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="29fb5-772">モード</span><span class="sxs-lookup"><span data-stu-id="29fb5-772">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="29fb5-773">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="29fb5-773">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="29fb5-774">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="29fb5-774">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="29fb5-775">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="29fb5-775">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="29fb5-776">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-776">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="29fb5-777">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="29fb5-777">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="29fb5-778">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="29fb5-778">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="29fb5-779">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="29fb5-779">Parameters - visible</span></span>

<span data-ttu-id="29fb5-780">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-780">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="29fb5-781">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="29fb5-781">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="29fb5-782">メソッド width</span><span class="sxs-lookup"><span data-stu-id="29fb5-782">Method width</span></span>

<span data-ttu-id="29fb5-783">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-783">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="29fb5-784">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="29fb5-784">Parameters - width</span></span>

<span data-ttu-id="29fb5-785">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-785">value</span></span>  

<!-- -->

<span data-ttu-id="29fb5-786">モード</span><span class="sxs-lookup"><span data-stu-id="29fb5-786">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="29fb5-787">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="29fb5-787">Return Value - width</span></span>

<span data-ttu-id="29fb5-788">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="29fb5-788">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="29fb5-789">備考 - width</span><span class="sxs-lookup"><span data-stu-id="29fb5-789">Remarks - width</span></span>

<span data-ttu-id="29fb5-790">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-790">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="29fb5-791">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="29fb5-791">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="29fb5-792">モード。</span><span class="sxs-lookup"><span data-stu-id="29fb5-792">Mode.</span></span>           | <span data-ttu-id="29fb5-793">幅計算。</span><span class="sxs-lookup"><span data-stu-id="29fb5-793">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="29fb5-794">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="29fb5-794">-1 Exact.</span></span>       | <span data-ttu-id="29fb5-795">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-795">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="29fb5-796">0 自動。</span><span class="sxs-lookup"><span data-stu-id="29fb5-796">0 Auto.</span></span>         | <span data-ttu-id="29fb5-797">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-797">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="29fb5-798">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="29fb5-798">1 Column width.</span></span> | <span data-ttu-id="29fb5-799">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="29fb5-799">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="29fb5-800">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-800">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="29fb5-801">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="29fb5-801">Method widthMode</span></span>

<span data-ttu-id="29fb5-802">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-802">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="29fb5-803">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="29fb5-803">Parameters - widthMode</span></span>

<span data-ttu-id="29fb5-804">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-804">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="29fb5-805">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="29fb5-805">Return Value - widthMode</span></span>

<span data-ttu-id="29fb5-806">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="29fb5-806">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="29fb5-807">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="29fb5-807">Remarks - widthMode</span></span>

<span data-ttu-id="29fb5-808">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="29fb5-808">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="29fb5-809">モード。</span><span class="sxs-lookup"><span data-stu-id="29fb5-809">Mode.</span></span>         | <span data-ttu-id="29fb5-810">幅計算。</span><span class="sxs-lookup"><span data-stu-id="29fb5-810">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="29fb5-811">正確。</span><span class="sxs-lookup"><span data-stu-id="29fb5-811">Exact.</span></span>        | <span data-ttu-id="29fb5-812">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-812">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="29fb5-813">自動。</span><span class="sxs-lookup"><span data-stu-id="29fb5-813">Auto.</span></span>         | <span data-ttu-id="29fb5-814">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="29fb5-814">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="29fb5-815">列の幅。</span><span class="sxs-lookup"><span data-stu-id="29fb5-815">Column width.</span></span> | <span data-ttu-id="29fb5-816">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="29fb5-816">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="29fb5-817">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="29fb5-817">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="29fb5-818">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="29fb5-818">Method widthValue</span></span>

<span data-ttu-id="29fb5-819">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-819">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="29fb5-820">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="29fb5-820">Parameters - widthValue</span></span>

<span data-ttu-id="29fb5-821">値</span><span class="sxs-lookup"><span data-stu-id="29fb5-821">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="29fb5-822">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="29fb5-822">Return Value - widthValue</span></span>

<span data-ttu-id="29fb5-823">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="29fb5-823">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="29fb5-824">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="29fb5-824">Remarks - widthValue</span></span>

<span data-ttu-id="29fb5-825">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="29fb5-825">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="29fb5-826">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="29fb5-826">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="29fb5-827">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="29fb5-827">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="29fb5-828">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="29fb5-828">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="29fb5-829">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="29fb5-829">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="29fb5-830">overrideObject</span><span class="sxs-lookup"><span data-stu-id="29fb5-830">overrideObject</span></span>  

