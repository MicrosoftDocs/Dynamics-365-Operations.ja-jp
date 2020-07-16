---
title: FormBuildDropDialogButtonControl クラス
description: このトピックでは、FormBuildDropDialogButtonControl クラスについて説明します。
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
ms.openlocfilehash: 732440a4dbcf7b26bb703588d76c379abe558c0f
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502654"
---
# <a name="class-formbuilddropdialogbuttoncontrol"></a><span data-ttu-id="d7b3d-103">クラス FormBuildDropDialogButtonControl</span><span class="sxs-lookup"><span data-stu-id="d7b3d-103">Class FormBuildDropDialogButtonControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildDropDialogButtonControl extends FormBuildControl
```

## <a name="remarks"></a><span data-ttu-id="d7b3d-104">備考</span><span class="sxs-lookup"><span data-stu-id="d7b3d-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="d7b3d-105">例</span><span class="sxs-lookup"><span data-stu-id="d7b3d-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="d7b3d-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="d7b3d-106">Methods</span></span>

| <span data-ttu-id="d7b3d-107">方法</span><span class="sxs-lookup"><span data-stu-id="d7b3d-107">Method</span></span>                                                                                                      | <span data-ttu-id="d7b3d-108">説明</span><span class="sxs-lookup"><span data-stu-id="d7b3d-108">Description</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b3d-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="d7b3d-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-110">Determines whether to align the control.</span></span>                                                                                                  |
| <span data-ttu-id="d7b3d-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-111">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="d7b3d-112">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-112">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="d7b3d-113">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-113">Determines whether the user can change the contents of the control.</span></span>                                                                       |
| <span data-ttu-id="d7b3d-114">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-114">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="d7b3d-115">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-115">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                        |
| <span data-ttu-id="d7b3d-116">public boolean autoRefreshData(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-116">public boolean autoRefreshData(\[boolean value\])</span></span>                                                           |                                                                                                                                           |
| <span data-ttu-id="d7b3d-117">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-117">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="d7b3d-118">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-118">Gets or sets the background color of the control.</span></span>                                                                                         |
| <span data-ttu-id="d7b3d-119">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-119">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="d7b3d-120">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-120">Determines whether the control background can be transparent.</span></span>                                                                             |
| <span data-ttu-id="d7b3d-121">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-121">public boolean big(\[boolean value\])</span></span>                                                                       |                                                                                                                                           |
| <span data-ttu-id="d7b3d-122">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-122">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="d7b3d-123">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-123">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                               |
| <span data-ttu-id="d7b3d-124">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-124">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="d7b3d-125">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-125">Gets or sets the style of the borderline of the control.</span></span>                                                                                  |
| <span data-ttu-id="d7b3d-126">public int buttonDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-126">public int buttonDisplay(\[int value\])</span></span>                                                                     | <span data-ttu-id="d7b3d-127">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-127">Gets or sets the appearance of the button control.</span></span>                                                                                        |
| <span data-ttu-id="d7b3d-128">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-128">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="d7b3d-129">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-129">Gets or set the caption of the control.</span></span>                                                                                                   |
| <span data-ttu-id="d7b3d-130">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-130">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="d7b3d-131">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-131">Gets or sets the character set of the font.</span></span>                                                                                               |
| <span data-ttu-id="d7b3d-132">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-132">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="d7b3d-133">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-133">Gets or sets the color scheme of the control.</span></span>                                                                                             |
| <span data-ttu-id="d7b3d-134">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-134">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="d7b3d-135">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-135">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                       |
| <span data-ttu-id="d7b3d-136">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="d7b3d-136">public int containerId()</span></span>                                                                                    | <span data-ttu-id="d7b3d-137">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-137">Retrieves the ID of the parent container for the control.</span></span>                                                                                 |
| <span data-ttu-id="d7b3d-138">public int copyCallerQuery(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-138">public int copyCallerQuery(\[int value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="d7b3d-139">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-139">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="d7b3d-140">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-140">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                           |
| <span data-ttu-id="d7b3d-141">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-141">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="d7b3d-142">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-142">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="d7b3d-143">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-143">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                  |
| <span data-ttu-id="d7b3d-144">public boolean defaultButton(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-144">public boolean defaultButton(\[boolean value\])</span></span>                                                             | <span data-ttu-id="d7b3d-145">ボタンをフォーム上の既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-145">Determines whether the button should be the default button on the form.</span></span>                                                                   |
| <span data-ttu-id="d7b3d-146">public str disabledImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-146">public str disabledImage(\[str value\])</span></span>                                                                     | <span data-ttu-id="d7b3d-147">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-147">Gets or sets the disabled image of the button.</span></span>                                                                                            |
| <span data-ttu-id="d7b3d-148">public int disabledImageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-148">public int disabledImageLocation(\[int value\])</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="d7b3d-149">public int disabledResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-149">public int disabledResource(\[int value\])</span></span>                                                                  | <span data-ttu-id="d7b3d-150">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-150">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>                                                            |
| <span data-ttu-id="d7b3d-151">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-151">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="d7b3d-152">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-152">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="d7b3d-153">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-153">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                         |
| <span data-ttu-id="d7b3d-154">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-154">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="d7b3d-155">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-155">Determines whether to enable or disable the object.</span></span>                                                                                       |
| <span data-ttu-id="d7b3d-156">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-156">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="d7b3d-157">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-157">Gets or sets the name of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="d7b3d-158">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-158">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="d7b3d-159">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-159">Gets or sets the size of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="d7b3d-160">public boolean forcedToOverflow(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-160">public boolean forcedToOverflow(\[boolean value\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="d7b3d-161">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-161">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="d7b3d-162">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-162">Gets or sets the text color for the control to use.</span></span>                                                                                       |
| <span data-ttu-id="d7b3d-163">public int formViewOption(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-163">public int formViewOption(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="d7b3d-164">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-164">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="d7b3d-165">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-165">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="d7b3d-166">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-166">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="d7b3d-167">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-167">Gets or sets a calculation mode for the height of the control.</span></span>                                                                            |
| <span data-ttu-id="d7b3d-168">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-168">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="d7b3d-169">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-169">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="d7b3d-170">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-170">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="d7b3d-171">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-171">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="d7b3d-172">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-172">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="d7b3d-173">public int id()</span><span class="sxs-lookup"><span data-stu-id="d7b3d-173">public int id()</span></span>                                                                                             | <span data-ttu-id="d7b3d-174">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-174">Retrieves the ID of the control.</span></span>                                                                                                          |
| <span data-ttu-id="d7b3d-175">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-175">public int imageLocation(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="d7b3d-176">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="d7b3d-176">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="d7b3d-177">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-177">Retrieves a value that indicates whether the control is a container control.</span></span>                                                              |
| <span data-ttu-id="d7b3d-178">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-178">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="d7b3d-179">public str keyTip(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-179">public str keyTip(\[str value\])</span></span>                                                                            |                                                                                                                                           |
| <span data-ttu-id="d7b3d-180">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-180">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="d7b3d-181">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-181">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="d7b3d-182">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-182">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="d7b3d-183">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-183">public str menuItemName(\[str value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="d7b3d-184">public int multiSelect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-184">public int multiSelect(\[int value\])</span></span>                                                                       |                                                                                                                                           |
| <span data-ttu-id="d7b3d-185">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-185">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="d7b3d-186">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-186">Gets or sets the name that is used in code to identify a form, report, table, query, or another application object.</span></span> |
| <span data-ttu-id="d7b3d-187">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-187">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="d7b3d-188">public int needsRecord(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-188">public int needsRecord(\[int value\])</span></span>                                                                       |                                                                                                                                           |
| <span data-ttu-id="d7b3d-189">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-189">public str normalImage(\[str value\])</span></span>                                                                       |                                                                                                                                           |
| <span data-ttu-id="d7b3d-190">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-190">public int normalResource(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="d7b3d-191">public int openMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-191">public int openMode(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="d7b3d-192">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-192">public str parameters(\[str value\])</span></span>                                                                        | <span data-ttu-id="d7b3d-193">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-193">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                    |
| <span data-ttu-id="d7b3d-194">public boolean primary(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-194">public boolean primary(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="d7b3d-195">public boolean saveRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-195">public boolean saveRecord(\[boolean value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="d7b3d-196">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-196">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                           |
| <span data-ttu-id="d7b3d-197">public boolean sendExternalContext(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-197">public boolean sendExternalContext(\[boolean value\])</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="d7b3d-198">public int shortkey(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-198">public int shortkey(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="d7b3d-199">public boolean showShortCut(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-199">public boolean showShortCut(\[boolean value\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="d7b3d-200">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-200">public boolean skip(\[boolean value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="d7b3d-201">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-201">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                           |
| <span data-ttu-id="d7b3d-202">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-202">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="d7b3d-203">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-203">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="d7b3d-204">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-204">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                           |
| <span data-ttu-id="d7b3d-205">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-205">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="d7b3d-206">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-206">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="d7b3d-207">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-207">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="d7b3d-208">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-208">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="d7b3d-209">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-209">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="d7b3d-210">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-210">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="d7b3d-211">public boolean value(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-211">public boolean value(\[boolean value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="d7b3d-212">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-212">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="d7b3d-213">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-213">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="d7b3d-214">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-214">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="d7b3d-215">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-215">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="d7b3d-216">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-216">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="d7b3d-217">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-217">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="d7b3d-218">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-218">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="d7b3d-219">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-219">Gets or sets the calculation mode of the width of the control.</span></span>                                                                            |
| <span data-ttu-id="d7b3d-220">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-220">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="d7b3d-221">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-221">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="d7b3d-222">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="d7b3d-222">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                           |

## <a name="method-aligncontrol"></a><span data-ttu-id="d7b3d-223">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="d7b3d-223">Method alignControl</span></span>

<span data-ttu-id="d7b3d-224">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-224">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="d7b3d-225">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="d7b3d-225">Parameters - alignControl</span></span>

<span data-ttu-id="d7b3d-226">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-226">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="d7b3d-227">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="d7b3d-227">Return Value - alignControl</span></span>

<span data-ttu-id="d7b3d-228">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-228">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="d7b3d-229">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="d7b3d-229">Remarks - alignControl</span></span>

<span data-ttu-id="d7b3d-230">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-230">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="d7b3d-231">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="d7b3d-231">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="d7b3d-232">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="d7b3d-232">Parameters - alignment</span></span>

<span data-ttu-id="d7b3d-233">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-233">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="d7b3d-234">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="d7b3d-234">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="d7b3d-235">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="d7b3d-235">Method allowEdit</span></span>

<span data-ttu-id="d7b3d-236">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-236">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="d7b3d-237">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="d7b3d-237">Parameters - allowEdit</span></span>

<span data-ttu-id="d7b3d-238">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-238">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="d7b3d-239">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="d7b3d-239">Return Value - allowEdit</span></span>

<span data-ttu-id="d7b3d-240">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-240">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="d7b3d-241">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="d7b3d-241">Remarks - allowEdit</span></span>

<span data-ttu-id="d7b3d-242">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-242">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="d7b3d-243">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="d7b3d-243">Method autoDeclaration</span></span>

<span data-ttu-id="d7b3d-244">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-244">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="d7b3d-245">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="d7b3d-245">Parameters - autoDeclaration</span></span>

<span data-ttu-id="d7b3d-246">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-246">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="d7b3d-247">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="d7b3d-247">Return Value - autoDeclaration</span></span>

<span data-ttu-id="d7b3d-248">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-248">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="d7b3d-249">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="d7b3d-249">Remarks - autoDeclaration</span></span>

<span data-ttu-id="d7b3d-250">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-250">Controls cannot have identical names.</span></span>

## <a name="method-autorefreshdata"></a><span data-ttu-id="d7b3d-251">メソッド autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="d7b3d-251">Method autoRefreshData</span></span>

```xpp
public boolean autoRefreshData([boolean value])
```

### <a name="parameters---autorefreshdata"></a><span data-ttu-id="d7b3d-252">パラメーター - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="d7b3d-252">Parameters - autoRefreshData</span></span>

<span data-ttu-id="d7b3d-253">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-253">value</span></span>  

### <a name="return-value---autorefreshdata"></a><span data-ttu-id="d7b3d-254">戻り値 - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="d7b3d-254">Return Value - autoRefreshData</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="d7b3d-255">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="d7b3d-255">Method backgroundColor</span></span>

<span data-ttu-id="d7b3d-256">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-256">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="d7b3d-257">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="d7b3d-257">Parameters - backgroundColor</span></span>

<span data-ttu-id="d7b3d-258">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-258">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="d7b3d-259">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="d7b3d-259">Return Value - backgroundColor</span></span>

<span data-ttu-id="d7b3d-260">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-260">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="d7b3d-261">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="d7b3d-261">Remarks - backgroundColor</span></span>

<span data-ttu-id="d7b3d-262">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-262">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="d7b3d-263">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-263">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="d7b3d-264">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-264">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="d7b3d-265">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-265">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="d7b3d-266">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-266">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="d7b3d-267">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-267">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="d7b3d-268">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="d7b3d-268">Method backStyle</span></span>

<span data-ttu-id="d7b3d-269">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-269">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="d7b3d-270">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="d7b3d-270">Parameters - backStyle</span></span>

<span data-ttu-id="d7b3d-271">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-271">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="d7b3d-272">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="d7b3d-272">Return Value - backStyle</span></span>

<span data-ttu-id="d7b3d-273">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-273">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-big"></a><span data-ttu-id="d7b3d-274">メソッド big</span><span class="sxs-lookup"><span data-stu-id="d7b3d-274">Method big</span></span>

```xpp
public boolean big([boolean value])
```

### <a name="parameters---big"></a><span data-ttu-id="d7b3d-275">パラメーター - big</span><span class="sxs-lookup"><span data-stu-id="d7b3d-275">Parameters - big</span></span>

<span data-ttu-id="d7b3d-276">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-276">value</span></span>  

### <a name="return-value---big"></a><span data-ttu-id="d7b3d-277">戻り値 - big</span><span class="sxs-lookup"><span data-stu-id="d7b3d-277">Return Value - big</span></span>

## <a name="method-bold"></a><span data-ttu-id="d7b3d-278">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="d7b3d-278">Method bold</span></span>

<span data-ttu-id="d7b3d-279">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-279">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="d7b3d-280">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="d7b3d-280">Parameters - bold</span></span>

<span data-ttu-id="d7b3d-281">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-281">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="d7b3d-282">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="d7b3d-282">Return Value - bold</span></span>

<span data-ttu-id="d7b3d-283">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-283">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="d7b3d-284">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="d7b3d-284">Remarks - bold</span></span>

<span data-ttu-id="d7b3d-285">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-285">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="d7b3d-286">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-286">0 Use the default font weight.</span></span>
-   <span data-ttu-id="d7b3d-287">1 シン。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-287">1 Thin.</span></span>
-   <span data-ttu-id="d7b3d-288">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-288">2 Extra-light.</span></span>
-   <span data-ttu-id="d7b3d-289">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-289">3 Light.</span></span>
-   <span data-ttu-id="d7b3d-290">4 標準。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-290">4 Normal.</span></span>
-   <span data-ttu-id="d7b3d-291">5 中。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-291">5 Medium.</span></span>
-   <span data-ttu-id="d7b3d-292">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-292">6 Semibold.</span></span>
-   <span data-ttu-id="d7b3d-293">7 太字。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-293">7 Bold.</span></span>
-   <span data-ttu-id="d7b3d-294">8 極太。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-294">8 Extra-bold.</span></span>
-   <span data-ttu-id="d7b3d-295">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-295">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="d7b3d-296">メソッド border</span><span class="sxs-lookup"><span data-stu-id="d7b3d-296">Method border</span></span>

<span data-ttu-id="d7b3d-297">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-297">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="d7b3d-298">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="d7b3d-298">Parameters - border</span></span>

<span data-ttu-id="d7b3d-299">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-299">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="d7b3d-300">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="d7b3d-300">Return Value - border</span></span>

<span data-ttu-id="d7b3d-301">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-301">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="d7b3d-302">備考 - border</span><span class="sxs-lookup"><span data-stu-id="d7b3d-302">Remarks - border</span></span>

<span data-ttu-id="d7b3d-303">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-303">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="d7b3d-304">値です。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-304">Value.</span></span> | <span data-ttu-id="d7b3d-305">説明。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-305">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="d7b3d-306">0</span><span class="sxs-lookup"><span data-stu-id="d7b3d-306">0</span></span>      | <span data-ttu-id="d7b3d-307">自動。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-307">Auto.</span></span>        |
| <span data-ttu-id="d7b3d-308">1</span><span class="sxs-lookup"><span data-stu-id="d7b3d-308">1</span></span>      | <span data-ttu-id="d7b3d-309">3D。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-309">3D.</span></span>          |
| <span data-ttu-id="d7b3d-310">2</span><span class="sxs-lookup"><span data-stu-id="d7b3d-310">2</span></span>      | <span data-ttu-id="d7b3d-311">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-311">Single line.</span></span> |
| <span data-ttu-id="d7b3d-312">3</span><span class="sxs-lookup"><span data-stu-id="d7b3d-312">3</span></span>      | <span data-ttu-id="d7b3d-313">均一。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-313">Flat.</span></span>        |
| <span data-ttu-id="d7b3d-314">4</span><span class="sxs-lookup"><span data-stu-id="d7b3d-314">4</span></span>      | <span data-ttu-id="d7b3d-315">なし。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-315">None.</span></span>        |

## <a name="method-buttondisplay"></a><span data-ttu-id="d7b3d-316">メソッド buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="d7b3d-316">Method buttonDisplay</span></span>

<span data-ttu-id="d7b3d-317">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-317">Gets or sets the appearance of the button control.</span></span>

```xpp
public int buttonDisplay([int value])
```

### <a name="parameters---buttondisplay"></a><span data-ttu-id="d7b3d-318">パラメーター - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="d7b3d-318">Parameters - buttonDisplay</span></span>

<span data-ttu-id="d7b3d-319">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-319">value</span></span>  

### <a name="return-value---buttondisplay"></a><span data-ttu-id="d7b3d-320">戻り値 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="d7b3d-320">Return Value - buttonDisplay</span></span>

<span data-ttu-id="d7b3d-321">ゼロから 5 までの整数。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-321">An integer between zero and five, inclusive.</span></span>

### <a name="remarks---buttondisplay"></a><span data-ttu-id="d7b3d-322">備考 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="d7b3d-322">Remarks - buttonDisplay</span></span>

<span data-ttu-id="d7b3d-323">プロパティ値は、テキスト、画像、またはその両方のいずれをボタンに表示するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-323">The value of the property defines whether the text, the image, or both should be displayed on the button.</span></span> <span data-ttu-id="d7b3d-324">このプロパティは、テキストと画像の両方が表示されている場合は、テキストと画像の相対位置も制御します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-324">This property also controls relative positions of text and image if both are displayed.</span></span> <span data-ttu-id="d7b3d-325">返される整数値には、次のようなボタン コントロールの外観が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-325">The integer value that is returned contains the appearance of the button control as follows:</span></span>

| <span data-ttu-id="d7b3d-326">値です。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-326">Value.</span></span> | <span data-ttu-id="d7b3d-327">説明。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-327">Description.</span></span>                                                     |
|--------|------------------------------------------------------------------|
| <span data-ttu-id="d7b3d-328">0</span><span class="sxs-lookup"><span data-stu-id="d7b3d-328">0</span></span>      | <span data-ttu-id="d7b3d-329">テキストのみ。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-329">Text only.</span></span>                                                       |
| <span data-ttu-id="d7b3d-330">1</span><span class="sxs-lookup"><span data-stu-id="d7b3d-330">1</span></span>      | <span data-ttu-id="d7b3d-331">イメージのみ。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-331">Image Only.</span></span>                                                      |
| <span data-ttu-id="d7b3d-332">2</span><span class="sxs-lookup"><span data-stu-id="d7b3d-332">2</span></span>      | <span data-ttu-id="d7b3d-333">テキストと画像。画像はテキストの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-333">Text and image; the image is displayed below the text.</span></span>           |
| <span data-ttu-id="d7b3d-334">3</span><span class="sxs-lookup"><span data-stu-id="d7b3d-334">3</span></span>      | <span data-ttu-id="d7b3d-335">テキストと画像。画像はテキストの上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-335">Text and image; the image is displayed above the text.</span></span>           |
| <span data-ttu-id="d7b3d-336">4</span><span class="sxs-lookup"><span data-stu-id="d7b3d-336">4</span></span>      | <span data-ttu-id="d7b3d-337">テキストと画像。画像はテキストの左に表示されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-337">Text and image; the image is displayed to the left of the text.</span></span>  |
| <span data-ttu-id="d7b3d-338">5</span><span class="sxs-lookup"><span data-stu-id="d7b3d-338">5</span></span>      | <span data-ttu-id="d7b3d-339">テキストと画像。画像はテキストの右に表示されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-339">Text and image; the image is displayed to the right of the text.</span></span> |

## <a name="method-caption"></a><span data-ttu-id="d7b3d-340">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="d7b3d-340">Method caption</span></span>

<span data-ttu-id="d7b3d-341">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-341">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="d7b3d-342">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="d7b3d-342">Parameters - caption</span></span>

<span data-ttu-id="d7b3d-343">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-343">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="d7b3d-344">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="d7b3d-344">Return Value - caption</span></span>

<span data-ttu-id="d7b3d-345">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-345">The string that is used as the caption of the control.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="d7b3d-346">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="d7b3d-346">Method characterSet</span></span>

<span data-ttu-id="d7b3d-347">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-347">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="d7b3d-348">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="d7b3d-348">Parameters - characterSet</span></span>

<span data-ttu-id="d7b3d-349">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-349">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="d7b3d-350">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="d7b3d-350">Return Value - characterSet</span></span>

<span data-ttu-id="d7b3d-351">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-351">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="d7b3d-352">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="d7b3d-352">Remarks - characterSet</span></span>

<span data-ttu-id="d7b3d-353">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-353">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="d7b3d-354">値です。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-354">Value.</span></span> | <span data-ttu-id="d7b3d-355">説明。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-355">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="d7b3d-356">0</span><span class="sxs-lookup"><span data-stu-id="d7b3d-356">0</span></span>      | <span data-ttu-id="d7b3d-357">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d7b3d-357">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="d7b3d-358">1</span><span class="sxs-lookup"><span data-stu-id="d7b3d-358">1</span></span>      | <span data-ttu-id="d7b3d-359">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d7b3d-359">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="d7b3d-360">2</span><span class="sxs-lookup"><span data-stu-id="d7b3d-360">2</span></span>      | <span data-ttu-id="d7b3d-361">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d7b3d-361">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="d7b3d-362">77</span><span class="sxs-lookup"><span data-stu-id="d7b3d-362">77</span></span>     | <span data-ttu-id="d7b3d-363">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d7b3d-363">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="d7b3d-364">128</span><span class="sxs-lookup"><span data-stu-id="d7b3d-364">128</span></span>    | <span data-ttu-id="d7b3d-365">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d7b3d-365">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="d7b3d-366">129</span><span class="sxs-lookup"><span data-stu-id="d7b3d-366">129</span></span>    | <span data-ttu-id="d7b3d-367">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d7b3d-367">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="d7b3d-368">134</span><span class="sxs-lookup"><span data-stu-id="d7b3d-368">134</span></span>    | <span data-ttu-id="d7b3d-369">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d7b3d-369">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="d7b3d-370">136</span><span class="sxs-lookup"><span data-stu-id="d7b3d-370">136</span></span>    | <span data-ttu-id="d7b3d-371">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d7b3d-371">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="d7b3d-372">161</span><span class="sxs-lookup"><span data-stu-id="d7b3d-372">161</span></span>    | <span data-ttu-id="d7b3d-373">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d7b3d-373">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="d7b3d-374">162</span><span class="sxs-lookup"><span data-stu-id="d7b3d-374">162</span></span>    | <span data-ttu-id="d7b3d-375">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d7b3d-375">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="d7b3d-376">163</span><span class="sxs-lookup"><span data-stu-id="d7b3d-376">163</span></span>    | <span data-ttu-id="d7b3d-377">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d7b3d-377">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="d7b3d-378">186</span><span class="sxs-lookup"><span data-stu-id="d7b3d-378">186</span></span>    | <span data-ttu-id="d7b3d-379">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d7b3d-379">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="d7b3d-380">204</span><span class="sxs-lookup"><span data-stu-id="d7b3d-380">204</span></span>    | <span data-ttu-id="d7b3d-381">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d7b3d-381">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="d7b3d-382">238</span><span class="sxs-lookup"><span data-stu-id="d7b3d-382">238</span></span>    | <span data-ttu-id="d7b3d-383">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d7b3d-383">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="d7b3d-384">255</span><span class="sxs-lookup"><span data-stu-id="d7b3d-384">255</span></span>    | <span data-ttu-id="d7b3d-385">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d7b3d-385">OEM\_CHARSET</span></span>         |

<span data-ttu-id="d7b3d-386">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-386">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="d7b3d-387">値です。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-387">Value.</span></span> | <span data-ttu-id="d7b3d-388">説明。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-388">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="d7b3d-389">130</span><span class="sxs-lookup"><span data-stu-id="d7b3d-389">130</span></span>    | <span data-ttu-id="d7b3d-390">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d7b3d-390">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="d7b3d-391">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-391">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="d7b3d-392">値です。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-392">Value.</span></span> | <span data-ttu-id="d7b3d-393">説明。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-393">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="d7b3d-394">177</span><span class="sxs-lookup"><span data-stu-id="d7b3d-394">177</span></span>    | <span data-ttu-id="d7b3d-395">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d7b3d-395">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="d7b3d-396">178</span><span class="sxs-lookup"><span data-stu-id="d7b3d-396">178</span></span>    | <span data-ttu-id="d7b3d-397">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d7b3d-397">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="d7b3d-398">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-398">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="d7b3d-399">値です。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-399">Value.</span></span> | <span data-ttu-id="d7b3d-400">説明。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-400">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="d7b3d-401">222</span><span class="sxs-lookup"><span data-stu-id="d7b3d-401">222</span></span>    | <span data-ttu-id="d7b3d-402">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d7b3d-402">THAI\_CHARSET</span></span> |

<span data-ttu-id="d7b3d-403">既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-403">The default character set is set to a value that is based on the current system locale.</span></span> <span data-ttu-id="d7b3d-404">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-404">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="d7b3d-405">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-405">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="d7b3d-406">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="d7b3d-406">Method colorScheme</span></span>

<span data-ttu-id="d7b3d-407">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-407">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="d7b3d-408">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="d7b3d-408">Parameters - colorScheme</span></span>

<span data-ttu-id="d7b3d-409">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-409">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="d7b3d-410">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="d7b3d-410">Return Value - colorScheme</span></span>

<span data-ttu-id="d7b3d-411">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-411">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="d7b3d-412">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="d7b3d-412">Remarks - colorScheme</span></span>

<span data-ttu-id="d7b3d-413">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-413">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="d7b3d-414">値です。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-414">Value.</span></span> | <span data-ttu-id="d7b3d-415">スタイル。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-415">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="d7b3d-416">0</span><span class="sxs-lookup"><span data-stu-id="d7b3d-416">0</span></span>      | <span data-ttu-id="d7b3d-417">既定。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-417">Default.</span></span>                       |
| <span data-ttu-id="d7b3d-418">1</span><span class="sxs-lookup"><span data-stu-id="d7b3d-418">1</span></span>      | <span data-ttu-id="d7b3d-419">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-419">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="d7b3d-420">2</span><span class="sxs-lookup"><span data-stu-id="d7b3d-420">2</span></span>      | <span data-ttu-id="d7b3d-421">真の配色。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-421">The true-color scheme.</span></span>         |

## <a name="method-configurationkey"></a><span data-ttu-id="d7b3d-422">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="d7b3d-422">Method configurationKey</span></span>

<span data-ttu-id="d7b3d-423">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-423">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="d7b3d-424">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="d7b3d-424">Parameters - configurationKey</span></span>

<span data-ttu-id="d7b3d-425">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-425">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="d7b3d-426">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="d7b3d-426">Return Value - configurationKey</span></span>

<span data-ttu-id="d7b3d-427">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-427">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="d7b3d-428">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="d7b3d-428">Remarks - configurationKey</span></span>

<span data-ttu-id="d7b3d-429">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-429">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="d7b3d-430">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-430">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="d7b3d-431">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="d7b3d-431">Method containerId</span></span>

<span data-ttu-id="d7b3d-432">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-432">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="d7b3d-433">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="d7b3d-433">Return Value - containerId</span></span>

<span data-ttu-id="d7b3d-434">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-434">The ID of the parent container.</span></span>

## <a name="method-copycallerquery"></a><span data-ttu-id="d7b3d-435">メソッド copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="d7b3d-435">Method copyCallerQuery</span></span>

```xpp
public int copyCallerQuery([int value])
```

### <a name="parameters---copycallerquery"></a><span data-ttu-id="d7b3d-436">パラメーター - copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="d7b3d-436">Parameters - copyCallerQuery</span></span>

<span data-ttu-id="d7b3d-437">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-437">value</span></span>  

### <a name="return-value---copycallerquery"></a><span data-ttu-id="d7b3d-438">戻り値 - copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="d7b3d-438">Return Value - copyCallerQuery</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="d7b3d-439">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="d7b3d-439">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="d7b3d-440">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="d7b3d-440">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="d7b3d-441">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-441">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="d7b3d-442">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="d7b3d-442">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="d7b3d-443">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="d7b3d-443">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="d7b3d-444">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="d7b3d-444">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="d7b3d-445">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-445">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="d7b3d-446">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="d7b3d-446">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="d7b3d-447">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="d7b3d-447">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="d7b3d-448">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="d7b3d-448">Parameters - dataRelationPath</span></span>

<span data-ttu-id="d7b3d-449">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-449">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="d7b3d-450">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="d7b3d-450">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="d7b3d-451">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="d7b3d-451">Method dataSource</span></span>

<span data-ttu-id="d7b3d-452">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-452">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="d7b3d-453">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="d7b3d-453">Parameters - dataSource</span></span>

<span data-ttu-id="d7b3d-454">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-454">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="d7b3d-455">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="d7b3d-455">Return Value - dataSource</span></span>

<span data-ttu-id="d7b3d-456">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-456">The identifier of the data source that will be used.</span></span>

## <a name="method-defaultbutton"></a><span data-ttu-id="d7b3d-457">メソッド defaultButton</span><span class="sxs-lookup"><span data-stu-id="d7b3d-457">Method defaultButton</span></span>

<span data-ttu-id="d7b3d-458">ボタンをフォーム上の既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-458">Determines whether the button should be the default button on the form.</span></span>

```xpp
public boolean defaultButton([boolean value])
```

### <a name="parameters---defaultbutton"></a><span data-ttu-id="d7b3d-459">パラメーター - defaultButton</span><span class="sxs-lookup"><span data-stu-id="d7b3d-459">Parameters - defaultButton</span></span>

<span data-ttu-id="d7b3d-460">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-460">value</span></span>  

### <a name="return-value---defaultbutton"></a><span data-ttu-id="d7b3d-461">戻り値 - defaultButton</span><span class="sxs-lookup"><span data-stu-id="d7b3d-461">Return Value - defaultButton</span></span>

<span data-ttu-id="d7b3d-462">ボタンが既定のボタンである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-462">true if the button should be the default button; otherwise, false.</span></span>

## <a name="method-disabledimage"></a><span data-ttu-id="d7b3d-463">メソッド disabledImage</span><span class="sxs-lookup"><span data-stu-id="d7b3d-463">Method disabledImage</span></span>

<span data-ttu-id="d7b3d-464">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-464">Gets or sets the disabled image of the button.</span></span>

```xpp
public str disabledImage([str value])
```

### <a name="parameters---disabledimage"></a><span data-ttu-id="d7b3d-465">パラメーター - disabledImage</span><span class="sxs-lookup"><span data-stu-id="d7b3d-465">Parameters - disabledImage</span></span>

<span data-ttu-id="d7b3d-466">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-466">value</span></span>  

### <a name="return-value---disabledimage"></a><span data-ttu-id="d7b3d-467">戻り値 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="d7b3d-467">Return Value - disabledImage</span></span>

<span data-ttu-id="d7b3d-468">画像ファイルのフル ネーム。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-468">The full name of an image file.</span></span> <span data-ttu-id="d7b3d-469">システムは、GDI でサポートされているすべてのイメージ形式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-469">The system supports all of the GDI-supported image formats.</span></span>

### <a name="remarks---disabledimage"></a><span data-ttu-id="d7b3d-470">備考 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="d7b3d-470">Remarks - disabledImage</span></span>

<span data-ttu-id="d7b3d-471">このプロパティは、disabledResourceproperty に優先します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-471">This property has precedence over the disabledResourceproperty.</span></span> <span data-ttu-id="d7b3d-472">これらのプロパティの両方が設定されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-472">It is used if both of these properties are set.</span></span>

## <a name="method-disabledimagelocation"></a><span data-ttu-id="d7b3d-473">メソッド disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="d7b3d-473">Method disabledImageLocation</span></span>

```xpp
public int disabledImageLocation([int value])
```

### <a name="parameters---disabledimagelocation"></a><span data-ttu-id="d7b3d-474">パラメーター - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="d7b3d-474">Parameters - disabledImageLocation</span></span>

<span data-ttu-id="d7b3d-475">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-475">value</span></span>  

### <a name="return-value---disabledimagelocation"></a><span data-ttu-id="d7b3d-476">戻り値 - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="d7b3d-476">Return Value - disabledImageLocation</span></span>

## <a name="method-disabledresource"></a><span data-ttu-id="d7b3d-477">メソッド disabledResource</span><span class="sxs-lookup"><span data-stu-id="d7b3d-477">Method disabledResource</span></span>

<span data-ttu-id="d7b3d-478">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-478">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>

```xpp
public int disabledResource([int value])
```

### <a name="parameters---disabledresource"></a><span data-ttu-id="d7b3d-479">パラメーター - disabledResource</span><span class="sxs-lookup"><span data-stu-id="d7b3d-479">Parameters - disabledResource</span></span>

<span data-ttu-id="d7b3d-480">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-480">value</span></span>  

### <a name="return-value---disabledresource"></a><span data-ttu-id="d7b3d-481">戻り値 - disabledResource</span><span class="sxs-lookup"><span data-stu-id="d7b3d-481">Return Value - disabledResource</span></span>

<span data-ttu-id="d7b3d-482">無効なボタン画像として使用する画像リソース ID。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-482">The resource ID of the image to use as the disabled button image.</span></span> <span data-ttu-id="d7b3d-483">アイコンとビットマップ イメージの両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-483">Both icon and bitmap images are supported.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="d7b3d-484">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="d7b3d-484">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="d7b3d-485">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="d7b3d-485">Parameters - displayTarget</span></span>

<span data-ttu-id="d7b3d-486">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-486">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="d7b3d-487">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="d7b3d-487">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="d7b3d-488">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="d7b3d-488">Method dragDrop</span></span>

<span data-ttu-id="d7b3d-489">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-489">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="d7b3d-490">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="d7b3d-490">Parameters - dragDrop</span></span>

<span data-ttu-id="d7b3d-491">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-491">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="d7b3d-492">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="d7b3d-492">Return Value - dragDrop</span></span>

<span data-ttu-id="d7b3d-493">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-493">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="d7b3d-494">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="d7b3d-494">Method enabled</span></span>

<span data-ttu-id="d7b3d-495">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-495">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="d7b3d-496">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="d7b3d-496">Parameters - enabled</span></span>

<span data-ttu-id="d7b3d-497">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-497">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="d7b3d-498">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="d7b3d-498">Return Value - enabled</span></span>

<span data-ttu-id="d7b3d-499">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-499">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="d7b3d-500">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="d7b3d-500">Remarks - enabled</span></span>

<span data-ttu-id="d7b3d-501">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-501">The enabled property enables controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="d7b3d-502">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-502">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="d7b3d-503">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-503">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="d7b3d-504">メソッド font</span><span class="sxs-lookup"><span data-stu-id="d7b3d-504">Method font</span></span>

<span data-ttu-id="d7b3d-505">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-505">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="d7b3d-506">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="d7b3d-506">Parameters - font</span></span>

<span data-ttu-id="d7b3d-507">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-507">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="d7b3d-508">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="d7b3d-508">Return Value - font</span></span>

<span data-ttu-id="d7b3d-509">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-509">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="d7b3d-510">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="d7b3d-510">Method fontSize</span></span>

<span data-ttu-id="d7b3d-511">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-511">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="d7b3d-512">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="d7b3d-512">Parameters - fontSize</span></span>

<span data-ttu-id="d7b3d-513">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-513">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="d7b3d-514">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="d7b3d-514">Return Value - fontSize</span></span>

<span data-ttu-id="d7b3d-515">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-515">The height of the font in points.</span></span>

## <a name="method-forcedtooverflow"></a><span data-ttu-id="d7b3d-516">メソッド forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="d7b3d-516">Method forcedToOverflow</span></span>

```xpp
public boolean forcedToOverflow([boolean value])
```

### <a name="parameters---forcedtooverflow"></a><span data-ttu-id="d7b3d-517">パラメーター - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="d7b3d-517">Parameters - forcedToOverflow</span></span>

<span data-ttu-id="d7b3d-518">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-518">value</span></span>  

### <a name="return-value---forcedtooverflow"></a><span data-ttu-id="d7b3d-519">戻り値 - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="d7b3d-519">Return Value - forcedToOverflow</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="d7b3d-520">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="d7b3d-520">Method foregroundColor</span></span>

<span data-ttu-id="d7b3d-521">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-521">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="d7b3d-522">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="d7b3d-522">Parameters - foregroundColor</span></span>

<span data-ttu-id="d7b3d-523">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-523">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="d7b3d-524">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="d7b3d-524">Return Value - foregroundColor</span></span>

<span data-ttu-id="d7b3d-525">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-525">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="d7b3d-526">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="d7b3d-526">Remarks - foregroundColor</span></span>

<span data-ttu-id="d7b3d-527">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-527">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="d7b3d-528">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-528">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="d7b3d-529">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-529">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="d7b3d-530">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-530">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="d7b3d-531">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-531">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="d7b3d-532">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-532">The maximum value for a single byte is 255.</span></span>

## <a name="method-formviewoption"></a><span data-ttu-id="d7b3d-533">メソッド formViewOption</span><span class="sxs-lookup"><span data-stu-id="d7b3d-533">Method formViewOption</span></span>

```xpp
public int formViewOption([int value])
```

### <a name="parameters---formviewoption"></a><span data-ttu-id="d7b3d-534">パラメータ-formViewOption</span><span class="sxs-lookup"><span data-stu-id="d7b3d-534">Parameters - formViewOption</span></span>

<span data-ttu-id="d7b3d-535">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-535">value</span></span>  

### <a name="return-value---formviewoption"></a><span data-ttu-id="d7b3d-536">戻り値 - formViewOption</span><span class="sxs-lookup"><span data-stu-id="d7b3d-536">Return Value - formViewOption</span></span>

## <a name="method-height"></a><span data-ttu-id="d7b3d-537">メソッド height</span><span class="sxs-lookup"><span data-stu-id="d7b3d-537">Method height</span></span>

<span data-ttu-id="d7b3d-538">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-538">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="d7b3d-539">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="d7b3d-539">Parameters - height</span></span>

<span data-ttu-id="d7b3d-540">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-540">value</span></span>  

<!-- -->

<span data-ttu-id="d7b3d-541">モード</span><span class="sxs-lookup"><span data-stu-id="d7b3d-541">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="d7b3d-542">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="d7b3d-542">Return Value - height</span></span>

<span data-ttu-id="d7b3d-543">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-543">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="d7b3d-544">備考 - height</span><span class="sxs-lookup"><span data-stu-id="d7b3d-544">Remarks - height</span></span>

<span data-ttu-id="d7b3d-545">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-545">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="d7b3d-546">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="d7b3d-546">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="d7b3d-547">モード。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-547">Mode.</span></span>            | <span data-ttu-id="d7b3d-548">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-548">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b3d-549">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-549">-1 Exact.</span></span>        | <span data-ttu-id="d7b3d-550">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-550">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="d7b3d-551">0 自動。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-551">0 Auto.</span></span>          | <span data-ttu-id="d7b3d-552">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-552">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="d7b3d-553">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-553">1 Column height.</span></span> | <span data-ttu-id="d7b3d-554">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-554">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="d7b3d-555">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-555">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="d7b3d-556">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="d7b3d-556">Method heightMode</span></span>

<span data-ttu-id="d7b3d-557">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-557">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="d7b3d-558">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="d7b3d-558">Parameters - heightMode</span></span>

<span data-ttu-id="d7b3d-559">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-559">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="d7b3d-560">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="d7b3d-560">Return Value - heightMode</span></span>

<span data-ttu-id="d7b3d-561">計算モード。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-561">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="d7b3d-562">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="d7b3d-562">Remarks - heightMode</span></span>

<span data-ttu-id="d7b3d-563">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="d7b3d-563">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="d7b3d-564">モード。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-564">Mode.</span></span>          | <span data-ttu-id="d7b3d-565">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-565">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b3d-566">正確。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-566">Exact.</span></span>         | <span data-ttu-id="d7b3d-567">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-567">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="d7b3d-568">自動。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-568">Auto.</span></span>          | <span data-ttu-id="d7b3d-569">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-569">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="d7b3d-570">列の高さ</span><span class="sxs-lookup"><span data-stu-id="d7b3d-570">Column height.</span></span> | <span data-ttu-id="d7b3d-571">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-571">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="d7b3d-572">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-572">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="d7b3d-573">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="d7b3d-573">Method heightValue</span></span>

<span data-ttu-id="d7b3d-574">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-574">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="d7b3d-575">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="d7b3d-575">Parameters - heightValue</span></span>

<span data-ttu-id="d7b3d-576">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-576">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="d7b3d-577">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="d7b3d-577">Return Value - heightValue</span></span>

<span data-ttu-id="d7b3d-578">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-578">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="d7b3d-579">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="d7b3d-579">Remarks - heightValue</span></span>

<span data-ttu-id="d7b3d-580">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-580">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="d7b3d-581">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="d7b3d-581">Method helpText</span></span>

<span data-ttu-id="d7b3d-582">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-582">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="d7b3d-583">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="d7b3d-583">Parameters - helpText</span></span>

<span data-ttu-id="d7b3d-584">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-584">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="d7b3d-585">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="d7b3d-585">Return Value - helpText</span></span>

<span data-ttu-id="d7b3d-586">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-586">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="d7b3d-587">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="d7b3d-587">Remarks - helpText</span></span>

<span data-ttu-id="d7b3d-588">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-588">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="d7b3d-589">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-589">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="d7b3d-590">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="d7b3d-590">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="d7b3d-591">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="d7b3d-591">Parameters - hierarchyParent</span></span>

<span data-ttu-id="d7b3d-592">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-592">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="d7b3d-593">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="d7b3d-593">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="d7b3d-594">メソッド id</span><span class="sxs-lookup"><span data-stu-id="d7b3d-594">Method id</span></span>

<span data-ttu-id="d7b3d-595">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-595">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="d7b3d-596">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="d7b3d-596">Return Value - id</span></span>

<span data-ttu-id="d7b3d-597">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-597">The ID of the control.</span></span>

## <a name="method-imagelocation"></a><span data-ttu-id="d7b3d-598">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="d7b3d-598">Method imageLocation</span></span>

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a><span data-ttu-id="d7b3d-599">パラメーター - imageLocation</span><span class="sxs-lookup"><span data-stu-id="d7b3d-599">Parameters - imageLocation</span></span>

<span data-ttu-id="d7b3d-600">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-600">value</span></span>  

### <a name="return-value---imagelocation"></a><span data-ttu-id="d7b3d-601">戻り値 - imageLocation</span><span class="sxs-lookup"><span data-stu-id="d7b3d-601">Return Value - imageLocation</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="d7b3d-602">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="d7b3d-602">Method isContainer</span></span>

<span data-ttu-id="d7b3d-603">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-603">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="d7b3d-604">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="d7b3d-604">Return Value - isContainer</span></span>

<span data-ttu-id="d7b3d-605">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-605">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="d7b3d-606">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="d7b3d-606">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="d7b3d-607">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="d7b3d-607">Parameters - italic</span></span>

<span data-ttu-id="d7b3d-608">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-608">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="d7b3d-609">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="d7b3d-609">Return Value - italic</span></span>

## <a name="method-keytip"></a><span data-ttu-id="d7b3d-610">メソッド keyTip</span><span class="sxs-lookup"><span data-stu-id="d7b3d-610">Method keyTip</span></span>

```xpp
public str keyTip([str value])
```

### <a name="parameters---keytip"></a><span data-ttu-id="d7b3d-611">パラメーター - keyTip</span><span class="sxs-lookup"><span data-stu-id="d7b3d-611">Parameters - keyTip</span></span>

<span data-ttu-id="d7b3d-612">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-612">value</span></span>  

### <a name="return-value---keytip"></a><span data-ttu-id="d7b3d-613">戻り値 - keyTip</span><span class="sxs-lookup"><span data-stu-id="d7b3d-613">Return Value - keyTip</span></span>

## <a name="method-left"></a><span data-ttu-id="d7b3d-614">メソッド left</span><span class="sxs-lookup"><span data-stu-id="d7b3d-614">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="d7b3d-615">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="d7b3d-615">Parameters - left</span></span>

<span data-ttu-id="d7b3d-616">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-616">value</span></span>  

<!-- -->

<span data-ttu-id="d7b3d-617">モード</span><span class="sxs-lookup"><span data-stu-id="d7b3d-617">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="d7b3d-618">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="d7b3d-618">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="d7b3d-619">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="d7b3d-619">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="d7b3d-620">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="d7b3d-620">Parameters - leftMode</span></span>

<span data-ttu-id="d7b3d-621">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-621">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="d7b3d-622">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="d7b3d-622">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="d7b3d-623">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="d7b3d-623">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="d7b3d-624">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="d7b3d-624">Parameters - leftValue</span></span>

<span data-ttu-id="d7b3d-625">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-625">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="d7b3d-626">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="d7b3d-626">Return Value - leftValue</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="d7b3d-627">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="d7b3d-627">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="d7b3d-628">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="d7b3d-628">Parameters - menuItemName</span></span>

<span data-ttu-id="d7b3d-629">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-629">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="d7b3d-630">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="d7b3d-630">Return Value - menuItemName</span></span>

## <a name="method-multiselect"></a><span data-ttu-id="d7b3d-631">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="d7b3d-631">Method multiSelect</span></span>

```xpp
public int multiSelect([int value])
```

### <a name="parameters---multiselect"></a><span data-ttu-id="d7b3d-632">パラメーター - multiSelect</span><span class="sxs-lookup"><span data-stu-id="d7b3d-632">Parameters - multiSelect</span></span>

<span data-ttu-id="d7b3d-633">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-633">value</span></span>  

### <a name="return-value---multiselect"></a><span data-ttu-id="d7b3d-634">戻り値 - multiSelect</span><span class="sxs-lookup"><span data-stu-id="d7b3d-634">Return Value - multiSelect</span></span>

## <a name="method-name"></a><span data-ttu-id="d7b3d-635">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d7b3d-635">Method name</span></span>

<span data-ttu-id="d7b3d-636">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-636">Gets or sets the name that is used in code to identify a form, report, table, query, or another application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="d7b3d-637">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="d7b3d-637">Parameters - name</span></span>

<span data-ttu-id="d7b3d-638">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-638">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="d7b3d-639">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="d7b3d-639">Return Value - name</span></span>

<span data-ttu-id="d7b3d-640">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-640">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="d7b3d-641">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="d7b3d-641">Remarks - name</span></span>

<span data-ttu-id="d7b3d-642">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-642">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="d7b3d-643">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-643">It must start with a letter.</span></span>
-   <span data-ttu-id="d7b3d-644">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-644">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="d7b3d-645">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-645">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="d7b3d-646">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-646">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="d7b3d-647">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-647">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="d7b3d-648">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="d7b3d-648">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="d7b3d-649">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="d7b3d-649">Parameters - neededPermission</span></span>

<span data-ttu-id="d7b3d-650">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-650">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="d7b3d-651">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="d7b3d-651">Return Value - neededPermission</span></span>

## <a name="method-needsrecord"></a><span data-ttu-id="d7b3d-652">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="d7b3d-652">Method needsRecord</span></span>

```xpp
public int needsRecord([int value])
```

### <a name="parameters---needsrecord"></a><span data-ttu-id="d7b3d-653">パラメーター - needsRecord</span><span class="sxs-lookup"><span data-stu-id="d7b3d-653">Parameters - needsRecord</span></span>

<span data-ttu-id="d7b3d-654">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-654">value</span></span>  

### <a name="return-value---needsrecord"></a><span data-ttu-id="d7b3d-655">戻り値 - needsRecord</span><span class="sxs-lookup"><span data-stu-id="d7b3d-655">Return Value - needsRecord</span></span>

## <a name="method-normalimage"></a><span data-ttu-id="d7b3d-656">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="d7b3d-656">Method normalImage</span></span>

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a><span data-ttu-id="d7b3d-657">パラメーター - normalImage</span><span class="sxs-lookup"><span data-stu-id="d7b3d-657">Parameters - normalImage</span></span>

<span data-ttu-id="d7b3d-658">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-658">value</span></span>  

### <a name="return-value---normalimage"></a><span data-ttu-id="d7b3d-659">戻り値 - normalImage</span><span class="sxs-lookup"><span data-stu-id="d7b3d-659">Return Value - normalImage</span></span>

## <a name="method-normalresource"></a><span data-ttu-id="d7b3d-660">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="d7b3d-660">Method normalResource</span></span>

```xpp
public int normalResource([int value])
```

### <a name="parameters---normalresource"></a><span data-ttu-id="d7b3d-661">パラメーター - normalResource</span><span class="sxs-lookup"><span data-stu-id="d7b3d-661">Parameters - normalResource</span></span>

<span data-ttu-id="d7b3d-662">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-662">value</span></span>  

### <a name="return-value---normalresource"></a><span data-ttu-id="d7b3d-663">戻り値 - normalResource</span><span class="sxs-lookup"><span data-stu-id="d7b3d-663">Return Value - normalResource</span></span>

## <a name="method-openmode"></a><span data-ttu-id="d7b3d-664">メソッド openMode</span><span class="sxs-lookup"><span data-stu-id="d7b3d-664">Method openMode</span></span>

```xpp
public int openMode([int value])
```

### <a name="parameters---openmode"></a><span data-ttu-id="d7b3d-665">パラメーター - openMode</span><span class="sxs-lookup"><span data-stu-id="d7b3d-665">Parameters - openMode</span></span>

<span data-ttu-id="d7b3d-666">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-666">value</span></span>  

### <a name="return-value---openmode"></a><span data-ttu-id="d7b3d-667">戻り値 - openMode</span><span class="sxs-lookup"><span data-stu-id="d7b3d-667">Return Value - openMode</span></span>

## <a name="method-parameters"></a><span data-ttu-id="d7b3d-668">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="d7b3d-668">Method parameters</span></span>

<span data-ttu-id="d7b3d-669">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-669">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

```xpp
public str parameters([str value])
```

### <a name="parameters---parameters"></a><span data-ttu-id="d7b3d-670">パラメーター - parameters</span><span class="sxs-lookup"><span data-stu-id="d7b3d-670">Parameters - parameters</span></span>

<span data-ttu-id="d7b3d-671">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-671">value</span></span>  

### <a name="return-value---parameters"></a><span data-ttu-id="d7b3d-672">戻り値 - parameters</span><span class="sxs-lookup"><span data-stu-id="d7b3d-672">Return Value - parameters</span></span>

<span data-ttu-id="d7b3d-673">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-673">The list of parameters that are passed to the object.</span></span>

### <a name="remarks---parameters"></a><span data-ttu-id="d7b3d-674">備考 - パラメータ</span><span class="sxs-lookup"><span data-stu-id="d7b3d-674">Remarks - parameters</span></span>

<span data-ttu-id="d7b3d-675">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-675">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="d7b3d-676">ignore が渡された場合、パラメータが認識されません。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-676">If ignore is passed, unrecognized parameters.</span></span>

## <a name="method-primary"></a><span data-ttu-id="d7b3d-677">メソッド primary</span><span class="sxs-lookup"><span data-stu-id="d7b3d-677">Method primary</span></span>

```xpp
public boolean primary([boolean value])
```

### <a name="parameters---primary"></a><span data-ttu-id="d7b3d-678">パラメーター - primary</span><span class="sxs-lookup"><span data-stu-id="d7b3d-678">Parameters - primary</span></span>

<span data-ttu-id="d7b3d-679">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-679">value</span></span>  

### <a name="return-value---primary"></a><span data-ttu-id="d7b3d-680">戻り値 - primary</span><span class="sxs-lookup"><span data-stu-id="d7b3d-680">Return Value - primary</span></span>

## <a name="method-saverecord"></a><span data-ttu-id="d7b3d-681">メソッド saveRecord</span><span class="sxs-lookup"><span data-stu-id="d7b3d-681">Method saveRecord</span></span>

```xpp
public boolean saveRecord([boolean value])
```

### <a name="parameters---saverecord"></a><span data-ttu-id="d7b3d-682">パラメーター - saveRecord</span><span class="sxs-lookup"><span data-stu-id="d7b3d-682">Parameters - saveRecord</span></span>

<span data-ttu-id="d7b3d-683">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-683">value</span></span>  

### <a name="return-value---saverecord"></a><span data-ttu-id="d7b3d-684">戻り値 - saveRecord</span><span class="sxs-lookup"><span data-stu-id="d7b3d-684">Return Value - saveRecord</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="d7b3d-685">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="d7b3d-685">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="d7b3d-686">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="d7b3d-686">Parameters - securityKey</span></span>

<span data-ttu-id="d7b3d-687">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-687">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="d7b3d-688">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="d7b3d-688">Return Value - securityKey</span></span>

## <a name="method-sendexternalcontext"></a><span data-ttu-id="d7b3d-689">メソッド sendExternalContext</span><span class="sxs-lookup"><span data-stu-id="d7b3d-689">Method sendExternalContext</span></span>

```xpp
public boolean sendExternalContext([boolean value])
```

### <a name="parameters---sendexternalcontext"></a><span data-ttu-id="d7b3d-690">パラメーター - sendExternalContext</span><span class="sxs-lookup"><span data-stu-id="d7b3d-690">Parameters - sendExternalContext</span></span>

<span data-ttu-id="d7b3d-691">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-691">value</span></span>  

### <a name="return-value---sendexternalcontext"></a><span data-ttu-id="d7b3d-692">戻り値 - sendExternalContext</span><span class="sxs-lookup"><span data-stu-id="d7b3d-692">Return Value - sendExternalContext</span></span>

## <a name="method-shortkey"></a><span data-ttu-id="d7b3d-693">メソッド shortkey</span><span class="sxs-lookup"><span data-stu-id="d7b3d-693">Method shortkey</span></span>

```xpp
public int shortkey([int value])
```

### <a name="parameters---shortkey"></a><span data-ttu-id="d7b3d-694">パラメーター - shortkey</span><span class="sxs-lookup"><span data-stu-id="d7b3d-694">Parameters - shortkey</span></span>

<span data-ttu-id="d7b3d-695">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-695">value</span></span>  

### <a name="return-value---shortkey"></a><span data-ttu-id="d7b3d-696">戻り値 - shortkey</span><span class="sxs-lookup"><span data-stu-id="d7b3d-696">Return Value - shortkey</span></span>

## <a name="method-showshortcut"></a><span data-ttu-id="d7b3d-697">メソッド showShortCut</span><span class="sxs-lookup"><span data-stu-id="d7b3d-697">Method showShortCut</span></span>

```xpp
public boolean showShortCut([boolean value])
```

### <a name="parameters---showshortcut"></a><span data-ttu-id="d7b3d-698">パラメーター - showShortCut</span><span class="sxs-lookup"><span data-stu-id="d7b3d-698">Parameters - showShortCut</span></span>

<span data-ttu-id="d7b3d-699">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-699">value</span></span>  

### <a name="return-value---showshortcut"></a><span data-ttu-id="d7b3d-700">戻り値 - showShortCut</span><span class="sxs-lookup"><span data-stu-id="d7b3d-700">Return Value - showShortCut</span></span>

## <a name="method-skip"></a><span data-ttu-id="d7b3d-701">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="d7b3d-701">Method skip</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="d7b3d-702">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="d7b3d-702">Parameters - skip</span></span>

<span data-ttu-id="d7b3d-703">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-703">value</span></span>  

### <a name="return-value---skip"></a><span data-ttu-id="d7b3d-704">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="d7b3d-704">Return Value - skip</span></span>

## <a name="method-style"></a><span data-ttu-id="d7b3d-705">メソッド style</span><span class="sxs-lookup"><span data-stu-id="d7b3d-705">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="d7b3d-706">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="d7b3d-706">Parameters - style</span></span>

<span data-ttu-id="d7b3d-707">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-707">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="d7b3d-708">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="d7b3d-708">Return Value - style</span></span>

## <a name="method-text"></a><span data-ttu-id="d7b3d-709">メソッド text</span><span class="sxs-lookup"><span data-stu-id="d7b3d-709">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="d7b3d-710">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="d7b3d-710">Parameters - text</span></span>

<span data-ttu-id="d7b3d-711">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-711">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="d7b3d-712">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="d7b3d-712">Return Value - text</span></span>

## <a name="method-top"></a><span data-ttu-id="d7b3d-713">メソッド top</span><span class="sxs-lookup"><span data-stu-id="d7b3d-713">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="d7b3d-714">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="d7b3d-714">Parameters - top</span></span>

<span data-ttu-id="d7b3d-715">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-715">value</span></span>  

<!-- -->

<span data-ttu-id="d7b3d-716">モード</span><span class="sxs-lookup"><span data-stu-id="d7b3d-716">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="d7b3d-717">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="d7b3d-717">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="d7b3d-718">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="d7b3d-718">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="d7b3d-719">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="d7b3d-719">Parameters - topMode</span></span>

<span data-ttu-id="d7b3d-720">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-720">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="d7b3d-721">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="d7b3d-721">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="d7b3d-722">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="d7b3d-722">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="d7b3d-723">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="d7b3d-723">Parameters - topValue</span></span>

<span data-ttu-id="d7b3d-724">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-724">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="d7b3d-725">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="d7b3d-725">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="d7b3d-726">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="d7b3d-726">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="d7b3d-727">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="d7b3d-727">Parameters - type</span></span>

<span data-ttu-id="d7b3d-728">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-728">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="d7b3d-729">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="d7b3d-729">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="d7b3d-730">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="d7b3d-730">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="d7b3d-731">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="d7b3d-731">Parameters - underline</span></span>

<span data-ttu-id="d7b3d-732">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-732">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="d7b3d-733">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="d7b3d-733">Return Value - underline</span></span>

## <a name="method-userdata"></a><span data-ttu-id="d7b3d-734">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="d7b3d-734">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="d7b3d-735">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="d7b3d-735">Parameters - userData</span></span>

<span data-ttu-id="d7b3d-736">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-736">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="d7b3d-737">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="d7b3d-737">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="d7b3d-738">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="d7b3d-738">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="d7b3d-739">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="d7b3d-739">Parameters - userDataItem</span></span>

<span data-ttu-id="d7b3d-740">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-740">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="d7b3d-741">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="d7b3d-741">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="d7b3d-742">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="d7b3d-742">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="d7b3d-743">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="d7b3d-743">Parameters - userDataItems</span></span>

<span data-ttu-id="d7b3d-744">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-744">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="d7b3d-745">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="d7b3d-745">Return Value - userDataItems</span></span>

## <a name="method-value"></a><span data-ttu-id="d7b3d-746">メソッド value</span><span class="sxs-lookup"><span data-stu-id="d7b3d-746">Method value</span></span>

```xpp
public boolean value([boolean value])
```

### <a name="parameters---value"></a><span data-ttu-id="d7b3d-747">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="d7b3d-747">Parameters - value</span></span>

<span data-ttu-id="d7b3d-748">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-748">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="d7b3d-749">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="d7b3d-749">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="d7b3d-750">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="d7b3d-750">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="d7b3d-751">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="d7b3d-751">Parameters - verticalSpacing</span></span>

<span data-ttu-id="d7b3d-752">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-752">value</span></span>  

<!-- -->

<span data-ttu-id="d7b3d-753">モード</span><span class="sxs-lookup"><span data-stu-id="d7b3d-753">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="d7b3d-754">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="d7b3d-754">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="d7b3d-755">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="d7b3d-755">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="d7b3d-756">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="d7b3d-756">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="d7b3d-757">モード</span><span class="sxs-lookup"><span data-stu-id="d7b3d-757">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="d7b3d-758">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="d7b3d-758">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="d7b3d-759">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="d7b3d-759">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="d7b3d-760">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="d7b3d-760">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="d7b3d-761">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-761">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="d7b3d-762">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="d7b3d-762">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="d7b3d-763">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="d7b3d-763">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="d7b3d-764">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="d7b3d-764">Parameters - visible</span></span>

<span data-ttu-id="d7b3d-765">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-765">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="d7b3d-766">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="d7b3d-766">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="d7b3d-767">メソッド width</span><span class="sxs-lookup"><span data-stu-id="d7b3d-767">Method width</span></span>

<span data-ttu-id="d7b3d-768">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-768">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="d7b3d-769">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="d7b3d-769">Parameters - width</span></span>

<span data-ttu-id="d7b3d-770">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-770">value</span></span>  

<!-- -->

<span data-ttu-id="d7b3d-771">モード</span><span class="sxs-lookup"><span data-stu-id="d7b3d-771">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="d7b3d-772">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="d7b3d-772">Return Value - width</span></span>

<span data-ttu-id="d7b3d-773">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-773">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="d7b3d-774">備考 - width</span><span class="sxs-lookup"><span data-stu-id="d7b3d-774">Remarks - width</span></span>

<span data-ttu-id="d7b3d-775">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-775">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="d7b3d-776">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="d7b3d-776">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="d7b3d-777">モード。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-777">Mode.</span></span>           | <span data-ttu-id="d7b3d-778">幅計算。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-778">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b3d-779">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-779">-1 Exact.</span></span>       | <span data-ttu-id="d7b3d-780">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-780">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="d7b3d-781">0 自動。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-781">0 Auto.</span></span>         | <span data-ttu-id="d7b3d-782">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-782">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="d7b3d-783">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-783">1 Column width.</span></span> | <span data-ttu-id="d7b3d-784">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-784">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="d7b3d-785">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-785">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="d7b3d-786">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="d7b3d-786">Method widthMode</span></span>

<span data-ttu-id="d7b3d-787">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-787">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="d7b3d-788">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="d7b3d-788">Parameters - widthMode</span></span>

<span data-ttu-id="d7b3d-789">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-789">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="d7b3d-790">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="d7b3d-790">Return Value - widthMode</span></span>

<span data-ttu-id="d7b3d-791">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-791">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="d7b3d-792">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="d7b3d-792">Remarks - widthMode</span></span>

<span data-ttu-id="d7b3d-793">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="d7b3d-793">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="d7b3d-794">モード。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-794">Mode.</span></span>         | <span data-ttu-id="d7b3d-795">幅計算。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-795">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b3d-796">正確。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-796">Exact.</span></span>        | <span data-ttu-id="d7b3d-797">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-797">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="d7b3d-798">自動。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-798">Auto.</span></span>         | <span data-ttu-id="d7b3d-799">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-799">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="d7b3d-800">列の幅。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-800">Column width.</span></span> | <span data-ttu-id="d7b3d-801">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-801">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="d7b3d-802">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-802">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="d7b3d-803">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="d7b3d-803">Method widthValue</span></span>

<span data-ttu-id="d7b3d-804">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-804">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="d7b3d-805">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="d7b3d-805">Parameters - widthValue</span></span>

<span data-ttu-id="d7b3d-806">値</span><span class="sxs-lookup"><span data-stu-id="d7b3d-806">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="d7b3d-807">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="d7b3d-807">Return Value - widthValue</span></span>

<span data-ttu-id="d7b3d-808">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-808">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="d7b3d-809">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="d7b3d-809">Remarks - widthValue</span></span>

<span data-ttu-id="d7b3d-810">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="d7b3d-810">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="d7b3d-811">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="d7b3d-811">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="d7b3d-812">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="d7b3d-812">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="d7b3d-813">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="d7b3d-813">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="d7b3d-814">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="d7b3d-814">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="d7b3d-815">overrideObject</span><span class="sxs-lookup"><span data-stu-id="d7b3d-815">overrideObject</span></span>  

