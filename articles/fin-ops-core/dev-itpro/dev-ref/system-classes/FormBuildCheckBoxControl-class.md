---
title: FormBuildCheckBoxControl クラス
description: このトピックでは、FormBuildCheckBoxControl クラスについて説明します。
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
ms.openlocfilehash: c892e0b3a7ab96ce64513e3704a9a95d1043c8b5
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502973"
---
# <a name="class-formbuildcheckboxcontrol"></a><span data-ttu-id="535f5-103">クラス FormBuildCheckBoxControl</span><span class="sxs-lookup"><span data-stu-id="535f5-103">Class FormBuildCheckBoxControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildCheckBoxControl extends FormBuildControl
```

<span data-ttu-id="535f5-104">FormBuildCheckBoxControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="535f5-104">The FormBuildCheckBoxControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="535f5-105">備考</span><span class="sxs-lookup"><span data-stu-id="535f5-105">Remarks</span></span>

<span data-ttu-id="535f5-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="535f5-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="535f5-107">例</span><span class="sxs-lookup"><span data-stu-id="535f5-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="535f5-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="535f5-108">Methods</span></span>

| <span data-ttu-id="535f5-109">方法</span><span class="sxs-lookup"><span data-stu-id="535f5-109">Method</span></span>                                                                                                      | <span data-ttu-id="535f5-110">説明</span><span class="sxs-lookup"><span data-stu-id="535f5-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="535f5-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="535f5-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-112">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="535f5-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="535f5-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-114">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="535f5-115">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-115">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="535f5-116">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-116">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="535f5-117">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-117">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="535f5-118">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-118">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="535f5-119">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-119">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="535f5-120">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-120">Determines whether the control background can be transparent.</span></span>                                                                           |
| <span data-ttu-id="535f5-121">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-121">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="535f5-122">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-122">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="535f5-123">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-123">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="535f5-124">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-124">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="535f5-125">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-125">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="535f5-126">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="535f5-126">public int containerId()</span></span>                                                                                    | <span data-ttu-id="535f5-127">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="535f5-127">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="535f5-128">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-128">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="535f5-129">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-129">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                         |
| <span data-ttu-id="535f5-130">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-130">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="535f5-131">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-131">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="535f5-132">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-132">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="535f5-133">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-133">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="535f5-134">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-134">Gets or sets a data source that is used by the control or the form.</span></span>                                                                     |
| <span data-ttu-id="535f5-135">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-135">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="535f5-136">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-136">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="535f5-137">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-137">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="535f5-138">public boolean drawFocusRect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-138">public boolean drawFocusRect(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="535f5-139">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-139">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="535f5-140">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-140">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="535f5-141">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-141">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="535f5-142">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-142">Gets or sets the text color for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="535f5-143">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="535f5-143">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="535f5-144">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-144">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="535f5-145">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-145">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="535f5-146">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-146">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="535f5-147">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-147">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="535f5-148">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-148">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="535f5-149">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-149">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="535f5-150">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-150">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="535f5-151">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-151">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="535f5-152">public int id()</span><span class="sxs-lookup"><span data-stu-id="535f5-152">public int id()</span></span>                                                                                             | <span data-ttu-id="535f5-153">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="535f5-153">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="535f5-154">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="535f5-154">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="535f5-155">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="535f5-155">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="535f5-156">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-156">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="535f5-157">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-157">Gets or sets the label for a control.</span></span>                                                                                                   |
| <span data-ttu-id="535f5-158">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-158">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="535f5-159">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-159">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="535f5-160">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-160">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="535f5-161">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-161">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="535f5-162">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-162">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="535f5-163">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-163">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="535f5-164">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-164">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="535f5-165">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="535f5-165">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="535f5-166">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-166">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="535f5-167">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-167">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="535f5-168">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-168">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="535f5-169">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-169">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="535f5-170">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-170">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="535f5-171">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="535f5-171">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="535f5-172">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-172">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="535f5-173">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-173">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="535f5-174">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="535f5-174">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="535f5-175">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-175">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="535f5-176">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-176">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="535f5-177">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-177">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="535f5-178">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-178">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="535f5-179">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-179">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="535f5-180">public boolean optionalRecordControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-180">public boolean optionalRecordControl(\[boolean value\])</span></span>                                                     |                                                                                                                                         |
| <span data-ttu-id="535f5-181">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-181">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="535f5-182">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-182">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="535f5-183">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-183">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="535f5-184">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-184">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="535f5-185">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="535f5-185">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="535f5-186">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-186">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="535f5-187">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="535f5-187">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="535f5-188">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-188">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="535f5-189">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-189">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="535f5-190">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-190">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="535f5-191">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-191">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="535f5-192">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-192">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="535f5-193">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-193">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="535f5-194">public int value(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-194">public int value(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="535f5-195">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="535f5-195">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="535f5-196">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="535f5-196">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="535f5-197">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-197">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="535f5-198">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-198">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="535f5-199">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-199">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="535f5-200">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="535f5-200">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="535f5-201">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-201">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="535f5-202">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-202">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="535f5-203">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-203">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="535f5-204">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="535f5-204">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="535f5-205">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-205">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="535f5-206">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="535f5-206">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="535f5-207">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="535f5-207">Method alignControl</span></span>

<span data-ttu-id="535f5-208">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-208">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="535f5-209">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="535f5-209">Parameters - alignControl</span></span>

<span data-ttu-id="535f5-210">値</span><span class="sxs-lookup"><span data-stu-id="535f5-210">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="535f5-211">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="535f5-211">Return Value - alignControl</span></span>

<span data-ttu-id="535f5-212">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="535f5-212">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="535f5-213">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="535f5-213">Remarks - alignControl</span></span>

<span data-ttu-id="535f5-214">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="535f5-214">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="535f5-215">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="535f5-215">Method allowEdit</span></span>

<span data-ttu-id="535f5-216">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-216">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="535f5-217">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="535f5-217">Parameters - allowEdit</span></span>

<span data-ttu-id="535f5-218">値</span><span class="sxs-lookup"><span data-stu-id="535f5-218">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="535f5-219">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="535f5-219">Return Value - allowEdit</span></span>

<span data-ttu-id="535f5-220">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="535f5-220">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="535f5-221">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="535f5-221">Remarks - allowEdit</span></span>

<span data-ttu-id="535f5-222">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="535f5-222">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="535f5-223">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="535f5-223">Method autoDeclaration</span></span>

<span data-ttu-id="535f5-224">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-224">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="535f5-225">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="535f5-225">Parameters - autoDeclaration</span></span>

<span data-ttu-id="535f5-226">値</span><span class="sxs-lookup"><span data-stu-id="535f5-226">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="535f5-227">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="535f5-227">Return Value - autoDeclaration</span></span>

<span data-ttu-id="535f5-228">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="535f5-228">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="535f5-229">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="535f5-229">Remarks - autoDeclaration</span></span>

<span data-ttu-id="535f5-230">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="535f5-230">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="535f5-231">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="535f5-231">Method backgroundColor</span></span>

<span data-ttu-id="535f5-232">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-232">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="535f5-233">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="535f5-233">Parameters - backgroundColor</span></span>

<span data-ttu-id="535f5-234">値</span><span class="sxs-lookup"><span data-stu-id="535f5-234">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="535f5-235">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="535f5-235">Return Value - backgroundColor</span></span>

<span data-ttu-id="535f5-236">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="535f5-236">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="535f5-237">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="535f5-237">Remarks - backgroundColor</span></span>

<span data-ttu-id="535f5-238">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="535f5-238">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="535f5-239">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="535f5-239">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="535f5-240">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="535f5-240">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="535f5-241">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="535f5-241">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="535f5-242">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="535f5-242">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="535f5-243">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="535f5-243">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="535f5-244">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="535f5-244">Method backStyle</span></span>

<span data-ttu-id="535f5-245">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-245">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="535f5-246">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="535f5-246">Parameters - backStyle</span></span>

<span data-ttu-id="535f5-247">値</span><span class="sxs-lookup"><span data-stu-id="535f5-247">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="535f5-248">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="535f5-248">Return Value - backStyle</span></span>

<span data-ttu-id="535f5-249">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="535f5-249">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-cachedatamethod"></a><span data-ttu-id="535f5-250">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="535f5-250">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="535f5-251">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="535f5-251">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="535f5-252">値</span><span class="sxs-lookup"><span data-stu-id="535f5-252">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="535f5-253">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="535f5-253">Return Value - cacheDataMethod</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="535f5-254">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="535f5-254">Method colorScheme</span></span>

<span data-ttu-id="535f5-255">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-255">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="535f5-256">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="535f5-256">Parameters - colorScheme</span></span>

<span data-ttu-id="535f5-257">値</span><span class="sxs-lookup"><span data-stu-id="535f5-257">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="535f5-258">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="535f5-258">Return Value - colorScheme</span></span>

<span data-ttu-id="535f5-259">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="535f5-259">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="535f5-260">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="535f5-260">Remarks - colorScheme</span></span>

<span data-ttu-id="535f5-261">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="535f5-261">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="535f5-262">値です。</span><span class="sxs-lookup"><span data-stu-id="535f5-262">Value.</span></span> | <span data-ttu-id="535f5-263">スタイル。</span><span class="sxs-lookup"><span data-stu-id="535f5-263">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="535f5-264">0</span><span class="sxs-lookup"><span data-stu-id="535f5-264">0</span></span>      | <span data-ttu-id="535f5-265">既定。</span><span class="sxs-lookup"><span data-stu-id="535f5-265">Default.</span></span>                      |
| <span data-ttu-id="535f5-266">1</span><span class="sxs-lookup"><span data-stu-id="535f5-266">1</span></span>      | <span data-ttu-id="535f5-267">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="535f5-267">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="535f5-268">2</span><span class="sxs-lookup"><span data-stu-id="535f5-268">2</span></span>      | <span data-ttu-id="535f5-269">真の配色。</span><span class="sxs-lookup"><span data-stu-id="535f5-269">The true-color scheme.</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="535f5-270">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="535f5-270">Method configurationKey</span></span>

<span data-ttu-id="535f5-271">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-271">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="535f5-272">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="535f5-272">Parameters - configurationKey</span></span>

<span data-ttu-id="535f5-273">値</span><span class="sxs-lookup"><span data-stu-id="535f5-273">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="535f5-274">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="535f5-274">Return Value - configurationKey</span></span>

<span data-ttu-id="535f5-275">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="535f5-275">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="535f5-276">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="535f5-276">Remarks - configurationKey</span></span>

<span data-ttu-id="535f5-277">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="535f5-277">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="535f5-278">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="535f5-278">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="535f5-279">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="535f5-279">Method containerId</span></span>

<span data-ttu-id="535f5-280">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="535f5-280">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="535f5-281">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="535f5-281">Return Value - containerId</span></span>

<span data-ttu-id="535f5-282">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="535f5-282">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="535f5-283">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="535f5-283">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="535f5-284">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="535f5-284">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="535f5-285">値</span><span class="sxs-lookup"><span data-stu-id="535f5-285">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="535f5-286">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="535f5-286">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="535f5-287">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="535f5-287">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="535f5-288">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="535f5-288">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="535f5-289">値</span><span class="sxs-lookup"><span data-stu-id="535f5-289">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="535f5-290">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="535f5-290">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="535f5-291">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="535f5-291">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="535f5-292">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="535f5-292">Parameters - dataField</span></span>

<span data-ttu-id="535f5-293">値</span><span class="sxs-lookup"><span data-stu-id="535f5-293">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="535f5-294">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="535f5-294">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="535f5-295">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="535f5-295">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="535f5-296">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="535f5-296">Parameters - dataMethod</span></span>

<span data-ttu-id="535f5-297">値</span><span class="sxs-lookup"><span data-stu-id="535f5-297">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="535f5-298">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="535f5-298">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="535f5-299">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="535f5-299">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="535f5-300">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="535f5-300">Parameters - dataRelationPath</span></span>

<span data-ttu-id="535f5-301">値</span><span class="sxs-lookup"><span data-stu-id="535f5-301">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="535f5-302">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="535f5-302">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="535f5-303">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="535f5-303">Method dataSource</span></span>

<span data-ttu-id="535f5-304">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-304">Gets or sets a data source that is used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="535f5-305">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="535f5-305">Parameters - dataSource</span></span>

<span data-ttu-id="535f5-306">値</span><span class="sxs-lookup"><span data-stu-id="535f5-306">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="535f5-307">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="535f5-307">Return Value - dataSource</span></span>

<span data-ttu-id="535f5-308">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="535f5-308">The identifier of the data source to use.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="535f5-309">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="535f5-309">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="535f5-310">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="535f5-310">Parameters - displayTarget</span></span>

<span data-ttu-id="535f5-311">値</span><span class="sxs-lookup"><span data-stu-id="535f5-311">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="535f5-312">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="535f5-312">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="535f5-313">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="535f5-313">Method dragDrop</span></span>

<span data-ttu-id="535f5-314">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-314">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="535f5-315">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="535f5-315">Parameters - dragDrop</span></span>

<span data-ttu-id="535f5-316">値</span><span class="sxs-lookup"><span data-stu-id="535f5-316">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="535f5-317">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="535f5-317">Return Value - dragDrop</span></span>

<span data-ttu-id="535f5-318">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="535f5-318">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-drawfocusrect"></a><span data-ttu-id="535f5-319">メソッド drawFocusRect</span><span class="sxs-lookup"><span data-stu-id="535f5-319">Method drawFocusRect</span></span>

```xpp
public boolean drawFocusRect([boolean value])
```

### <a name="parameters---drawfocusrect"></a><span data-ttu-id="535f5-320">パラメーター - drawFocusRect</span><span class="sxs-lookup"><span data-stu-id="535f5-320">Parameters - drawFocusRect</span></span>

<span data-ttu-id="535f5-321">値</span><span class="sxs-lookup"><span data-stu-id="535f5-321">value</span></span>  

### <a name="return-value---drawfocusrect"></a><span data-ttu-id="535f5-322">戻り値 - drawFocusRect</span><span class="sxs-lookup"><span data-stu-id="535f5-322">Return Value - drawFocusRect</span></span>

## <a name="method-enabled"></a><span data-ttu-id="535f5-323">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="535f5-323">Method enabled</span></span>

<span data-ttu-id="535f5-324">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-324">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="535f5-325">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="535f5-325">Parameters - enabled</span></span>

<span data-ttu-id="535f5-326">値</span><span class="sxs-lookup"><span data-stu-id="535f5-326">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="535f5-327">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="535f5-327">Return Value - enabled</span></span>

<span data-ttu-id="535f5-328">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="535f5-328">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="535f5-329">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="535f5-329">Remarks - enabled</span></span>

<span data-ttu-id="535f5-330">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="535f5-330">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="535f5-331">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="535f5-331">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="535f5-332">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="535f5-332">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="535f5-333">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="535f5-333">Method foregroundColor</span></span>

<span data-ttu-id="535f5-334">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-334">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="535f5-335">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="535f5-335">Parameters - foregroundColor</span></span>

<span data-ttu-id="535f5-336">値</span><span class="sxs-lookup"><span data-stu-id="535f5-336">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="535f5-337">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="535f5-337">Return Value - foregroundColor</span></span>

<span data-ttu-id="535f5-338">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="535f5-338">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="535f5-339">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="535f5-339">Remarks - foregroundColor</span></span>

<span data-ttu-id="535f5-340">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="535f5-340">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="535f5-341">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="535f5-341">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="535f5-342">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="535f5-342">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="535f5-343">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="535f5-343">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="535f5-344">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="535f5-344">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="535f5-345">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="535f5-345">The maximum value for a single byte is 255.</span></span>

## <a name="method-height"></a><span data-ttu-id="535f5-346">メソッド height</span><span class="sxs-lookup"><span data-stu-id="535f5-346">Method height</span></span>

<span data-ttu-id="535f5-347">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-347">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="535f5-348">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="535f5-348">Parameters - height</span></span>

<span data-ttu-id="535f5-349">値</span><span class="sxs-lookup"><span data-stu-id="535f5-349">value</span></span>  

<!-- -->

<span data-ttu-id="535f5-350">モード</span><span class="sxs-lookup"><span data-stu-id="535f5-350">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="535f5-351">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="535f5-351">Return Value - height</span></span>

<span data-ttu-id="535f5-352">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="535f5-352">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="535f5-353">備考 - height</span><span class="sxs-lookup"><span data-stu-id="535f5-353">Remarks - height</span></span>

<span data-ttu-id="535f5-354">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="535f5-354">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="535f5-355">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="535f5-355">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="535f5-356">モード。</span><span class="sxs-lookup"><span data-stu-id="535f5-356">Mode.</span></span>            | <span data-ttu-id="535f5-357">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="535f5-357">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="535f5-358">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="535f5-358">-1 Exact.</span></span>        | <span data-ttu-id="535f5-359">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="535f5-359">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="535f5-360">0 自動。</span><span class="sxs-lookup"><span data-stu-id="535f5-360">0 Auto.</span></span>          | <span data-ttu-id="535f5-361">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="535f5-361">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="535f5-362">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="535f5-362">1 Column height.</span></span> | <span data-ttu-id="535f5-363">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="535f5-363">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="535f5-364">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="535f5-364">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="535f5-365">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="535f5-365">Method heightMode</span></span>

<span data-ttu-id="535f5-366">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-366">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="535f5-367">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="535f5-367">Parameters - heightMode</span></span>

<span data-ttu-id="535f5-368">値</span><span class="sxs-lookup"><span data-stu-id="535f5-368">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="535f5-369">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="535f5-369">Return Value - heightMode</span></span>

<span data-ttu-id="535f5-370">計算モード。</span><span class="sxs-lookup"><span data-stu-id="535f5-370">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="535f5-371">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="535f5-371">Remarks - heightMode</span></span>

<span data-ttu-id="535f5-372">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="535f5-372">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="535f5-373">モード。</span><span class="sxs-lookup"><span data-stu-id="535f5-373">Mode.</span></span>          | <span data-ttu-id="535f5-374">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="535f5-374">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="535f5-375">正確。</span><span class="sxs-lookup"><span data-stu-id="535f5-375">Exact.</span></span>         | <span data-ttu-id="535f5-376">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="535f5-376">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="535f5-377">自動。</span><span class="sxs-lookup"><span data-stu-id="535f5-377">Auto.</span></span>          | <span data-ttu-id="535f5-378">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="535f5-378">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="535f5-379">列の高さ</span><span class="sxs-lookup"><span data-stu-id="535f5-379">Column height.</span></span> | <span data-ttu-id="535f5-380">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="535f5-380">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="535f5-381">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="535f5-381">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="535f5-382">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="535f5-382">Method heightValue</span></span>

<span data-ttu-id="535f5-383">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-383">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="535f5-384">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="535f5-384">Parameters - heightValue</span></span>

<span data-ttu-id="535f5-385">値</span><span class="sxs-lookup"><span data-stu-id="535f5-385">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="535f5-386">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="535f5-386">Return Value - heightValue</span></span>

<span data-ttu-id="535f5-387">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="535f5-387">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="535f5-388">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="535f5-388">Remarks - heightValue</span></span>

<span data-ttu-id="535f5-389">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="535f5-389">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="535f5-390">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="535f5-390">Method helpText</span></span>

<span data-ttu-id="535f5-391">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-391">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="535f5-392">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="535f5-392">Parameters - helpText</span></span>

<span data-ttu-id="535f5-393">値</span><span class="sxs-lookup"><span data-stu-id="535f5-393">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="535f5-394">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="535f5-394">Return Value - helpText</span></span>

<span data-ttu-id="535f5-395">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="535f5-395">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="535f5-396">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="535f5-396">Remarks - helpText</span></span>

<span data-ttu-id="535f5-397">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-397">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="535f5-398">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="535f5-398">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="535f5-399">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="535f5-399">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="535f5-400">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="535f5-400">Parameters - hierarchyParent</span></span>

<span data-ttu-id="535f5-401">値</span><span class="sxs-lookup"><span data-stu-id="535f5-401">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="535f5-402">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="535f5-402">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="535f5-403">メソッド id</span><span class="sxs-lookup"><span data-stu-id="535f5-403">Method id</span></span>

<span data-ttu-id="535f5-404">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="535f5-404">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="535f5-405">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="535f5-405">Return Value - id</span></span>

<span data-ttu-id="535f5-406">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="535f5-406">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="535f5-407">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="535f5-407">Method isContainer</span></span>

<span data-ttu-id="535f5-408">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="535f5-408">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="535f5-409">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="535f5-409">Return Value - isContainer</span></span>

<span data-ttu-id="535f5-410">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="535f5-410">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-label"></a><span data-ttu-id="535f5-411">メソッド label</span><span class="sxs-lookup"><span data-stu-id="535f5-411">Method label</span></span>

<span data-ttu-id="535f5-412">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-412">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="535f5-413">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="535f5-413">Parameters - label</span></span>

<span data-ttu-id="535f5-414">値</span><span class="sxs-lookup"><span data-stu-id="535f5-414">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="535f5-415">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="535f5-415">Return Value - label</span></span>

<span data-ttu-id="535f5-416">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="535f5-416">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="535f5-417">備考 - label</span><span class="sxs-lookup"><span data-stu-id="535f5-417">Remarks - label</span></span>

<span data-ttu-id="535f5-418">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-418">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="535f5-419">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="535f5-419">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="535f5-420">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="535f5-420">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="535f5-421">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="535f5-421">Parameters - labelAlignment</span></span>

<span data-ttu-id="535f5-422">値</span><span class="sxs-lookup"><span data-stu-id="535f5-422">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="535f5-423">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="535f5-423">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="535f5-424">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="535f5-424">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="535f5-425">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="535f5-425">Parameters - labelBold</span></span>

<span data-ttu-id="535f5-426">値</span><span class="sxs-lookup"><span data-stu-id="535f5-426">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="535f5-427">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="535f5-427">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="535f5-428">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="535f5-428">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="535f5-429">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="535f5-429">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="535f5-430">値</span><span class="sxs-lookup"><span data-stu-id="535f5-430">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="535f5-431">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="535f5-431">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="535f5-432">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="535f5-432">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="535f5-433">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="535f5-433">Parameters - labelFont</span></span>

<span data-ttu-id="535f5-434">値</span><span class="sxs-lookup"><span data-stu-id="535f5-434">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="535f5-435">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="535f5-435">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="535f5-436">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="535f5-436">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="535f5-437">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="535f5-437">Parameters - labelFontSize</span></span>

<span data-ttu-id="535f5-438">値</span><span class="sxs-lookup"><span data-stu-id="535f5-438">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="535f5-439">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="535f5-439">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="535f5-440">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="535f5-440">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="535f5-441">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="535f5-441">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="535f5-442">値</span><span class="sxs-lookup"><span data-stu-id="535f5-442">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="535f5-443">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="535f5-443">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="535f5-444">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="535f5-444">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="535f5-445">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="535f5-445">Parameters - labelGuide</span></span>

<span data-ttu-id="535f5-446">値</span><span class="sxs-lookup"><span data-stu-id="535f5-446">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="535f5-447">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="535f5-447">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="535f5-448">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="535f5-448">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="535f5-449">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="535f5-449">Parameters - labelHeight</span></span>

<span data-ttu-id="535f5-450">値</span><span class="sxs-lookup"><span data-stu-id="535f5-450">value</span></span>  

<!-- -->

<span data-ttu-id="535f5-451">モード</span><span class="sxs-lookup"><span data-stu-id="535f5-451">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="535f5-452">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="535f5-452">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="535f5-453">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="535f5-453">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="535f5-454">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="535f5-454">Parameters - labelHeightMode</span></span>

<span data-ttu-id="535f5-455">値</span><span class="sxs-lookup"><span data-stu-id="535f5-455">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="535f5-456">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="535f5-456">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="535f5-457">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="535f5-457">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="535f5-458">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="535f5-458">Parameters - labelHeightValue</span></span>

<span data-ttu-id="535f5-459">値</span><span class="sxs-lookup"><span data-stu-id="535f5-459">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="535f5-460">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="535f5-460">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="535f5-461">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="535f5-461">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="535f5-462">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="535f5-462">Parameters - labelItalic</span></span>

<span data-ttu-id="535f5-463">値</span><span class="sxs-lookup"><span data-stu-id="535f5-463">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="535f5-464">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="535f5-464">Return Value - labelItalic</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="535f5-465">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="535f5-465">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="535f5-466">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="535f5-466">Parameters - labelPosition</span></span>

<span data-ttu-id="535f5-467">値</span><span class="sxs-lookup"><span data-stu-id="535f5-467">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="535f5-468">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="535f5-468">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="535f5-469">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="535f5-469">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="535f5-470">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="535f5-470">Parameters - labelUnderline</span></span>

<span data-ttu-id="535f5-471">値</span><span class="sxs-lookup"><span data-stu-id="535f5-471">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="535f5-472">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="535f5-472">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="535f5-473">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="535f5-473">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="535f5-474">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="535f5-474">Parameters - labelWidth</span></span>

<span data-ttu-id="535f5-475">値</span><span class="sxs-lookup"><span data-stu-id="535f5-475">value</span></span>  

<!-- -->

<span data-ttu-id="535f5-476">モード</span><span class="sxs-lookup"><span data-stu-id="535f5-476">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="535f5-477">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="535f5-477">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="535f5-478">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="535f5-478">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="535f5-479">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="535f5-479">Parameters - labelWidthMode</span></span>

<span data-ttu-id="535f5-480">値</span><span class="sxs-lookup"><span data-stu-id="535f5-480">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="535f5-481">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="535f5-481">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="535f5-482">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="535f5-482">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="535f5-483">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="535f5-483">Parameters - labelWidthValue</span></span>

<span data-ttu-id="535f5-484">値</span><span class="sxs-lookup"><span data-stu-id="535f5-484">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="535f5-485">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="535f5-485">Return Value - labelWidthValue</span></span>

## <a name="method-left"></a><span data-ttu-id="535f5-486">メソッド left</span><span class="sxs-lookup"><span data-stu-id="535f5-486">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="535f5-487">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="535f5-487">Parameters - left</span></span>

<span data-ttu-id="535f5-488">値</span><span class="sxs-lookup"><span data-stu-id="535f5-488">value</span></span>  

<!-- -->

<span data-ttu-id="535f5-489">モード</span><span class="sxs-lookup"><span data-stu-id="535f5-489">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="535f5-490">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="535f5-490">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="535f5-491">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="535f5-491">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="535f5-492">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="535f5-492">Parameters - leftMode</span></span>

<span data-ttu-id="535f5-493">値</span><span class="sxs-lookup"><span data-stu-id="535f5-493">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="535f5-494">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="535f5-494">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="535f5-495">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="535f5-495">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="535f5-496">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="535f5-496">Parameters - leftValue</span></span>

<span data-ttu-id="535f5-497">値</span><span class="sxs-lookup"><span data-stu-id="535f5-497">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="535f5-498">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="535f5-498">Return Value - leftValue</span></span>

## <a name="method-name"></a><span data-ttu-id="535f5-499">メソッド名</span><span class="sxs-lookup"><span data-stu-id="535f5-499">Method name</span></span>

<span data-ttu-id="535f5-500">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-500">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="535f5-501">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="535f5-501">Parameters - name</span></span>

<span data-ttu-id="535f5-502">値</span><span class="sxs-lookup"><span data-stu-id="535f5-502">value</span></span>  
<span data-ttu-id="535f5-503">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="535f5-503">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="535f5-504">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="535f5-504">Return Value - name</span></span>

<span data-ttu-id="535f5-505">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="535f5-505">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="535f5-506">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="535f5-506">Remarks - name</span></span>

<span data-ttu-id="535f5-507">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="535f5-507">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="535f5-508">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="535f5-508">It must start with a letter.</span></span>
-   <span data-ttu-id="535f5-509">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="535f5-509">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="535f5-510">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="535f5-510">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="535f5-511">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="535f5-511">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="535f5-512">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="535f5-512">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="535f5-513">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="535f5-513">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="535f5-514">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="535f5-514">Parameters - neededPermission</span></span>

<span data-ttu-id="535f5-515">値</span><span class="sxs-lookup"><span data-stu-id="535f5-515">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="535f5-516">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="535f5-516">Return Value - neededPermission</span></span>

## <a name="method-optionalrecordcontrol"></a><span data-ttu-id="535f5-517">メソッド optionalRecordControl</span><span class="sxs-lookup"><span data-stu-id="535f5-517">Method optionalRecordControl</span></span>

```xpp
public boolean optionalRecordControl([boolean value])
```

### <a name="parameters---optionalrecordcontrol"></a><span data-ttu-id="535f5-518">パラメーター - optionalRecordControl</span><span class="sxs-lookup"><span data-stu-id="535f5-518">Parameters - optionalRecordControl</span></span>

<span data-ttu-id="535f5-519">値</span><span class="sxs-lookup"><span data-stu-id="535f5-519">value</span></span>  

### <a name="return-value---optionalrecordcontrol"></a><span data-ttu-id="535f5-520">戻り値 - optionalRecordControl</span><span class="sxs-lookup"><span data-stu-id="535f5-520">Return Value - optionalRecordControl</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="535f5-521">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="535f5-521">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="535f5-522">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="535f5-522">Parameters - promptrect</span></span>

<span data-ttu-id="535f5-523">値</span><span class="sxs-lookup"><span data-stu-id="535f5-523">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="535f5-524">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="535f5-524">Return Value - promptrect</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="535f5-525">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="535f5-525">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="535f5-526">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="535f5-526">Parameters - securityKey</span></span>

<span data-ttu-id="535f5-527">値</span><span class="sxs-lookup"><span data-stu-id="535f5-527">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="535f5-528">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="535f5-528">Return Value - securityKey</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="535f5-529">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="535f5-529">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="535f5-530">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="535f5-530">Parameters - showLabel</span></span>

<span data-ttu-id="535f5-531">値</span><span class="sxs-lookup"><span data-stu-id="535f5-531">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="535f5-532">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="535f5-532">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="535f5-533">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="535f5-533">Method skip</span></span>

<span data-ttu-id="535f5-534">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="535f5-534">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="535f5-535">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="535f5-535">Parameters - skip</span></span>

<span data-ttu-id="535f5-536">値</span><span class="sxs-lookup"><span data-stu-id="535f5-536">value</span></span>  
<span data-ttu-id="535f5-537">コントロールの skip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="535f5-537">The value to assign to the skip property of the control.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="535f5-538">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="535f5-538">Return Value - skip</span></span>

<span data-ttu-id="535f5-539">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="535f5-539">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-style"></a><span data-ttu-id="535f5-540">メソッド style</span><span class="sxs-lookup"><span data-stu-id="535f5-540">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="535f5-541">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="535f5-541">Parameters - style</span></span>

<span data-ttu-id="535f5-542">値</span><span class="sxs-lookup"><span data-stu-id="535f5-542">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="535f5-543">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="535f5-543">Return Value - style</span></span>

## <a name="method-top"></a><span data-ttu-id="535f5-544">メソッド top</span><span class="sxs-lookup"><span data-stu-id="535f5-544">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="535f5-545">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="535f5-545">Parameters - top</span></span>

<span data-ttu-id="535f5-546">値</span><span class="sxs-lookup"><span data-stu-id="535f5-546">value</span></span>  

<!-- -->

<span data-ttu-id="535f5-547">モード</span><span class="sxs-lookup"><span data-stu-id="535f5-547">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="535f5-548">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="535f5-548">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="535f5-549">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="535f5-549">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="535f5-550">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="535f5-550">Parameters - topMode</span></span>

<span data-ttu-id="535f5-551">値</span><span class="sxs-lookup"><span data-stu-id="535f5-551">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="535f5-552">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="535f5-552">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="535f5-553">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="535f5-553">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="535f5-554">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="535f5-554">Parameters - topValue</span></span>

<span data-ttu-id="535f5-555">値</span><span class="sxs-lookup"><span data-stu-id="535f5-555">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="535f5-556">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="535f5-556">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="535f5-557">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="535f5-557">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="535f5-558">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="535f5-558">Parameters - type</span></span>

<span data-ttu-id="535f5-559">値</span><span class="sxs-lookup"><span data-stu-id="535f5-559">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="535f5-560">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="535f5-560">Return Value - type</span></span>

## <a name="method-userdata"></a><span data-ttu-id="535f5-561">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="535f5-561">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="535f5-562">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="535f5-562">Parameters - userData</span></span>

<span data-ttu-id="535f5-563">値</span><span class="sxs-lookup"><span data-stu-id="535f5-563">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="535f5-564">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="535f5-564">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="535f5-565">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="535f5-565">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="535f5-566">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="535f5-566">Parameters - userDataItem</span></span>

<span data-ttu-id="535f5-567">値</span><span class="sxs-lookup"><span data-stu-id="535f5-567">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="535f5-568">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="535f5-568">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="535f5-569">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="535f5-569">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="535f5-570">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="535f5-570">Parameters - userDataItems</span></span>

<span data-ttu-id="535f5-571">値</span><span class="sxs-lookup"><span data-stu-id="535f5-571">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="535f5-572">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="535f5-572">Return Value - userDataItems</span></span>

## <a name="method-value"></a><span data-ttu-id="535f5-573">メソッド value</span><span class="sxs-lookup"><span data-stu-id="535f5-573">Method value</span></span>

```xpp
public int value([int value])
```

### <a name="parameters---value"></a><span data-ttu-id="535f5-574">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="535f5-574">Parameters - value</span></span>

<span data-ttu-id="535f5-575">値</span><span class="sxs-lookup"><span data-stu-id="535f5-575">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="535f5-576">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="535f5-576">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="535f5-577">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="535f5-577">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="535f5-578">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="535f5-578">Parameters - verticalSpacing</span></span>

<span data-ttu-id="535f5-579">値</span><span class="sxs-lookup"><span data-stu-id="535f5-579">value</span></span>  

<!-- -->

<span data-ttu-id="535f5-580">モード</span><span class="sxs-lookup"><span data-stu-id="535f5-580">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="535f5-581">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="535f5-581">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="535f5-582">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="535f5-582">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="535f5-583">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="535f5-583">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="535f5-584">モード</span><span class="sxs-lookup"><span data-stu-id="535f5-584">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="535f5-585">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="535f5-585">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="535f5-586">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="535f5-586">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="535f5-587">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="535f5-587">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="535f5-588">値</span><span class="sxs-lookup"><span data-stu-id="535f5-588">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="535f5-589">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="535f5-589">Return Value - verticalSpacingValue</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="535f5-590">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="535f5-590">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="535f5-591">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="535f5-591">Parameters - viewEditMode</span></span>

<span data-ttu-id="535f5-592">値</span><span class="sxs-lookup"><span data-stu-id="535f5-592">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="535f5-593">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="535f5-593">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="535f5-594">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="535f5-594">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="535f5-595">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="535f5-595">Parameters - visible</span></span>

<span data-ttu-id="535f5-596">値</span><span class="sxs-lookup"><span data-stu-id="535f5-596">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="535f5-597">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="535f5-597">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="535f5-598">メソッド width</span><span class="sxs-lookup"><span data-stu-id="535f5-598">Method width</span></span>

<span data-ttu-id="535f5-599">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-599">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="535f5-600">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="535f5-600">Parameters - width</span></span>

<span data-ttu-id="535f5-601">値</span><span class="sxs-lookup"><span data-stu-id="535f5-601">value</span></span>  

<!-- -->

<span data-ttu-id="535f5-602">モード</span><span class="sxs-lookup"><span data-stu-id="535f5-602">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="535f5-603">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="535f5-603">Return Value - width</span></span>

<span data-ttu-id="535f5-604">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="535f5-604">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="535f5-605">備考 - width</span><span class="sxs-lookup"><span data-stu-id="535f5-605">Remarks - width</span></span>

<span data-ttu-id="535f5-606">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="535f5-606">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="535f5-607">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="535f5-607">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="535f5-608">モード。</span><span class="sxs-lookup"><span data-stu-id="535f5-608">Mode.</span></span>           | <span data-ttu-id="535f5-609">幅計算。</span><span class="sxs-lookup"><span data-stu-id="535f5-609">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="535f5-610">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="535f5-610">-1 Exact.</span></span>       | <span data-ttu-id="535f5-611">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="535f5-611">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="535f5-612">0 自動。</span><span class="sxs-lookup"><span data-stu-id="535f5-612">0 Auto.</span></span>         | <span data-ttu-id="535f5-613">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="535f5-613">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="535f5-614">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="535f5-614">1 Column width.</span></span> | <span data-ttu-id="535f5-615">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="535f5-615">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="535f5-616">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="535f5-616">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="535f5-617">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="535f5-617">Method widthMode</span></span>

<span data-ttu-id="535f5-618">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-618">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="535f5-619">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="535f5-619">Parameters - widthMode</span></span>

<span data-ttu-id="535f5-620">値</span><span class="sxs-lookup"><span data-stu-id="535f5-620">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="535f5-621">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="535f5-621">Return Value - widthMode</span></span>

<span data-ttu-id="535f5-622">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="535f5-622">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="535f5-623">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="535f5-623">Remarks - widthMode</span></span>

<span data-ttu-id="535f5-624">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="535f5-624">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="535f5-625">モード。</span><span class="sxs-lookup"><span data-stu-id="535f5-625">Mode.</span></span>         | <span data-ttu-id="535f5-626">幅計算。</span><span class="sxs-lookup"><span data-stu-id="535f5-626">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="535f5-627">正確。</span><span class="sxs-lookup"><span data-stu-id="535f5-627">Exact.</span></span>        | <span data-ttu-id="535f5-628">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="535f5-628">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="535f5-629">自動。</span><span class="sxs-lookup"><span data-stu-id="535f5-629">Auto.</span></span>         | <span data-ttu-id="535f5-630">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="535f5-630">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="535f5-631">列の幅。</span><span class="sxs-lookup"><span data-stu-id="535f5-631">Column width.</span></span> | <span data-ttu-id="535f5-632">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="535f5-632">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="535f5-633">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="535f5-633">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="535f5-634">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="535f5-634">Method widthValue</span></span>

<span data-ttu-id="535f5-635">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="535f5-635">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="535f5-636">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="535f5-636">Parameters - widthValue</span></span>

<span data-ttu-id="535f5-637">値</span><span class="sxs-lookup"><span data-stu-id="535f5-637">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="535f5-638">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="535f5-638">Return Value - widthValue</span></span>

<span data-ttu-id="535f5-639">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="535f5-639">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="535f5-640">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="535f5-640">Remarks - widthValue</span></span>

<span data-ttu-id="535f5-641">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="535f5-641">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="535f5-642">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="535f5-642">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="535f5-643">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="535f5-643">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="535f5-644">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="535f5-644">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="535f5-645">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="535f5-645">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="535f5-646">overrideObject</span><span class="sxs-lookup"><span data-stu-id="535f5-646">overrideObject</span></span>  

