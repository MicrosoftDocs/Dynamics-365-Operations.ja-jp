---
title: FormBuildWindowControl クラス
description: このトピックでは、FormBuildWindowControl クラスについて説明します。
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
ms.openlocfilehash: 1b056e834b46202c750554541be9d61983e86d66
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502956"
---
# <a name="class-formbuildwindowcontrol"></a><span data-ttu-id="b0fbf-103">クラス FormBuildWindowControl</span><span class="sxs-lookup"><span data-stu-id="b0fbf-103">Class FormBuildWindowControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildWindowControl extends FormBuildControl
```

<span data-ttu-id="b0fbf-104">FormBuildWindoControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-104">The FormBuildWindoControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0fbf-105">備考</span><span class="sxs-lookup"><span data-stu-id="b0fbf-105">Remarks</span></span>

<span data-ttu-id="b0fbf-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="b0fbf-107">例</span><span class="sxs-lookup"><span data-stu-id="b0fbf-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="b0fbf-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="b0fbf-108">Methods</span></span>

| <span data-ttu-id="b0fbf-109">方法</span><span class="sxs-lookup"><span data-stu-id="b0fbf-109">Method</span></span>                                                                                                      | <span data-ttu-id="b0fbf-110">説明</span><span class="sxs-lookup"><span data-stu-id="b0fbf-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0fbf-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="b0fbf-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-112">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="b0fbf-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="b0fbf-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-114">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="b0fbf-115">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-115">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="b0fbf-116">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-116">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="b0fbf-117">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-117">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="b0fbf-118">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-118">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="b0fbf-119">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-119">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="b0fbf-120">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-120">Determines whether the control background can be transparent.</span></span>                                                                           |
| <span data-ttu-id="b0fbf-121">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-121">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="b0fbf-122">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-122">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="b0fbf-123">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-123">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="b0fbf-124">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-124">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="b0fbf-125">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-125">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="b0fbf-126">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="b0fbf-126">public int containerId()</span></span>                                                                                    | <span data-ttu-id="b0fbf-127">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-127">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="b0fbf-128">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-128">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="b0fbf-129">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-129">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                         |
| <span data-ttu-id="b0fbf-130">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-130">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="b0fbf-131">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-131">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="b0fbf-132">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-132">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="b0fbf-133">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-133">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="b0fbf-134">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-134">Gets or sets a data source that is used by the control or the form.</span></span>                                                                     |
| <span data-ttu-id="b0fbf-135">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-135">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="b0fbf-136">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-136">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="b0fbf-137">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-137">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="b0fbf-138">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-138">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="b0fbf-139">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-139">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="b0fbf-140">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-140">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="b0fbf-141">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-141">Gets or sets the text color for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="b0fbf-142">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-142">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="b0fbf-143">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-143">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="b0fbf-144">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-144">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="b0fbf-145">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-145">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="b0fbf-146">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-146">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="b0fbf-147">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-147">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="b0fbf-148">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-148">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="b0fbf-149">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-149">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="b0fbf-150">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-150">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="b0fbf-151">public int id()</span><span class="sxs-lookup"><span data-stu-id="b0fbf-151">public int id()</span></span>                                                                                             | <span data-ttu-id="b0fbf-152">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-152">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="b0fbf-153">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-153">public int imageLocation(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="b0fbf-154">public int imagemode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-154">public int imagemode(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="b0fbf-155">public str imageName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-155">public str imageName(\[str value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="b0fbf-156">public int imageResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-156">public int imageResource(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="b0fbf-157">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="b0fbf-157">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="b0fbf-158">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-158">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="b0fbf-159">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-159">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="b0fbf-160">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-160">Gets or sets the label for a control.</span></span>                                                                                                   |
| <span data-ttu-id="b0fbf-161">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-161">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="b0fbf-162">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-162">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="b0fbf-163">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-163">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="b0fbf-164">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-164">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="b0fbf-165">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-165">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="b0fbf-166">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-166">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="b0fbf-167">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-167">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="b0fbf-168">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-168">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="b0fbf-169">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-169">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="b0fbf-170">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-170">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="b0fbf-171">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-171">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="b0fbf-172">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-172">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="b0fbf-173">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-173">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="b0fbf-174">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-174">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="b0fbf-175">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-175">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="b0fbf-176">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-176">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="b0fbf-177">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-177">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="b0fbf-178">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-178">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="b0fbf-179">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-179">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="b0fbf-180">public str location(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-180">public str location(\[str value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="b0fbf-181">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-181">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="b0fbf-182">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-182">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="b0fbf-183">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-183">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="b0fbf-184">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-184">public str normalImage(\[str value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="b0fbf-185">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-185">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="b0fbf-186">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-186">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="b0fbf-187">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-187">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="b0fbf-188">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-188">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="b0fbf-189">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-189">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="b0fbf-190">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-190">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="b0fbf-191">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-191">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="b0fbf-192">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-192">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="b0fbf-193">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-193">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="b0fbf-194">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-194">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="b0fbf-195">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-195">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="b0fbf-196">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-196">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="b0fbf-197">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-197">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="b0fbf-198">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-198">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="b0fbf-199">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-199">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="b0fbf-200">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-200">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="b0fbf-201">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-201">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="b0fbf-202">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-202">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="b0fbf-203">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-203">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="b0fbf-204">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-204">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="b0fbf-205">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-205">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="b0fbf-206">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-206">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="b0fbf-207">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="b0fbf-207">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="b0fbf-208">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="b0fbf-208">Method alignControl</span></span>

<span data-ttu-id="b0fbf-209">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-209">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="b0fbf-210">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="b0fbf-210">Parameters - alignControl</span></span>

<span data-ttu-id="b0fbf-211">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-211">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="b0fbf-212">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="b0fbf-212">Return Value - alignControl</span></span>

<span data-ttu-id="b0fbf-213">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-213">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="b0fbf-214">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="b0fbf-214">Remarks - alignControl</span></span>

<span data-ttu-id="b0fbf-215">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-215">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="b0fbf-216">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="b0fbf-216">Method allowEdit</span></span>

<span data-ttu-id="b0fbf-217">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-217">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="b0fbf-218">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="b0fbf-218">Parameters - allowEdit</span></span>

<span data-ttu-id="b0fbf-219">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-219">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="b0fbf-220">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="b0fbf-220">Return Value - allowEdit</span></span>

<span data-ttu-id="b0fbf-221">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-221">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="b0fbf-222">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="b0fbf-222">Remarks - allowEdit</span></span>

<span data-ttu-id="b0fbf-223">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-223">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="b0fbf-224">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b0fbf-224">Method autoDeclaration</span></span>

<span data-ttu-id="b0fbf-225">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-225">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="b0fbf-226">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b0fbf-226">Parameters - autoDeclaration</span></span>

<span data-ttu-id="b0fbf-227">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-227">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="b0fbf-228">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b0fbf-228">Return Value - autoDeclaration</span></span>

<span data-ttu-id="b0fbf-229">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-229">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="b0fbf-230">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b0fbf-230">Remarks - autoDeclaration</span></span>

<span data-ttu-id="b0fbf-231">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-231">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="b0fbf-232">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b0fbf-232">Method backgroundColor</span></span>

<span data-ttu-id="b0fbf-233">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-233">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="b0fbf-234">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b0fbf-234">Parameters - backgroundColor</span></span>

<span data-ttu-id="b0fbf-235">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-235">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="b0fbf-236">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b0fbf-236">Return Value - backgroundColor</span></span>

<span data-ttu-id="b0fbf-237">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-237">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="b0fbf-238">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b0fbf-238">Remarks - backgroundColor</span></span>

<span data-ttu-id="b0fbf-239">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-239">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="b0fbf-240">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-240">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="b0fbf-241">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-241">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="b0fbf-242">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-242">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="b0fbf-243">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-243">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="b0fbf-244">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-244">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="b0fbf-245">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="b0fbf-245">Method backStyle</span></span>

<span data-ttu-id="b0fbf-246">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-246">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="b0fbf-247">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="b0fbf-247">Parameters - backStyle</span></span>

<span data-ttu-id="b0fbf-248">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-248">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="b0fbf-249">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="b0fbf-249">Return Value - backStyle</span></span>

<span data-ttu-id="b0fbf-250">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-250">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-cachedatamethod"></a><span data-ttu-id="b0fbf-251">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="b0fbf-251">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="b0fbf-252">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="b0fbf-252">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="b0fbf-253">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-253">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="b0fbf-254">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="b0fbf-254">Return Value - cacheDataMethod</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="b0fbf-255">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="b0fbf-255">Method colorScheme</span></span>

<span data-ttu-id="b0fbf-256">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-256">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="b0fbf-257">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="b0fbf-257">Parameters - colorScheme</span></span>

<span data-ttu-id="b0fbf-258">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-258">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="b0fbf-259">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="b0fbf-259">Return Value - colorScheme</span></span>

<span data-ttu-id="b0fbf-260">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-260">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="b0fbf-261">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="b0fbf-261">Remarks - colorScheme</span></span>

<span data-ttu-id="b0fbf-262">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-262">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="b0fbf-263">値です。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-263">Value.</span></span> | <span data-ttu-id="b0fbf-264">スタイル。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-264">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="b0fbf-265">0</span><span class="sxs-lookup"><span data-stu-id="b0fbf-265">0</span></span>      | <span data-ttu-id="b0fbf-266">既定。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-266">Default.</span></span>                      |
| <span data-ttu-id="b0fbf-267">1</span><span class="sxs-lookup"><span data-stu-id="b0fbf-267">1</span></span>      | <span data-ttu-id="b0fbf-268">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-268">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="b0fbf-269">2</span><span class="sxs-lookup"><span data-stu-id="b0fbf-269">2</span></span>      | <span data-ttu-id="b0fbf-270">真の配色。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-270">The true-color scheme.</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="b0fbf-271">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="b0fbf-271">Method configurationKey</span></span>

<span data-ttu-id="b0fbf-272">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-272">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="b0fbf-273">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="b0fbf-273">Parameters - configurationKey</span></span>

<span data-ttu-id="b0fbf-274">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-274">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="b0fbf-275">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="b0fbf-275">Return Value - configurationKey</span></span>

<span data-ttu-id="b0fbf-276">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-276">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="b0fbf-277">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="b0fbf-277">Remarks - configurationKey</span></span>

<span data-ttu-id="b0fbf-278">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-278">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="b0fbf-279">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-279">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="b0fbf-280">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="b0fbf-280">Method containerId</span></span>

<span data-ttu-id="b0fbf-281">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-281">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="b0fbf-282">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="b0fbf-282">Return Value - containerId</span></span>

<span data-ttu-id="b0fbf-283">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-283">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="b0fbf-284">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="b0fbf-284">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="b0fbf-285">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="b0fbf-285">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="b0fbf-286">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-286">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="b0fbf-287">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="b0fbf-287">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="b0fbf-288">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="b0fbf-288">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="b0fbf-289">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="b0fbf-289">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="b0fbf-290">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-290">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="b0fbf-291">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="b0fbf-291">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="b0fbf-292">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="b0fbf-292">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="b0fbf-293">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="b0fbf-293">Parameters - dataField</span></span>

<span data-ttu-id="b0fbf-294">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-294">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="b0fbf-295">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="b0fbf-295">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="b0fbf-296">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="b0fbf-296">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="b0fbf-297">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="b0fbf-297">Parameters - dataMethod</span></span>

<span data-ttu-id="b0fbf-298">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-298">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="b0fbf-299">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="b0fbf-299">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="b0fbf-300">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="b0fbf-300">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="b0fbf-301">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="b0fbf-301">Parameters - dataRelationPath</span></span>

<span data-ttu-id="b0fbf-302">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-302">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="b0fbf-303">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="b0fbf-303">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="b0fbf-304">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="b0fbf-304">Method dataSource</span></span>

<span data-ttu-id="b0fbf-305">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-305">Gets or sets a data source that is used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="b0fbf-306">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="b0fbf-306">Parameters - dataSource</span></span>

<span data-ttu-id="b0fbf-307">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-307">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="b0fbf-308">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="b0fbf-308">Return Value - dataSource</span></span>

<span data-ttu-id="b0fbf-309">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-309">The identifier of the data source to use.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="b0fbf-310">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="b0fbf-310">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="b0fbf-311">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="b0fbf-311">Parameters - displayTarget</span></span>

<span data-ttu-id="b0fbf-312">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-312">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="b0fbf-313">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="b0fbf-313">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="b0fbf-314">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="b0fbf-314">Method dragDrop</span></span>

<span data-ttu-id="b0fbf-315">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-315">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="b0fbf-316">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="b0fbf-316">Parameters - dragDrop</span></span>

<span data-ttu-id="b0fbf-317">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-317">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="b0fbf-318">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="b0fbf-318">Return Value - dragDrop</span></span>

<span data-ttu-id="b0fbf-319">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-319">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="b0fbf-320">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="b0fbf-320">Method enabled</span></span>

<span data-ttu-id="b0fbf-321">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-321">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="b0fbf-322">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="b0fbf-322">Parameters - enabled</span></span>

<span data-ttu-id="b0fbf-323">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-323">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="b0fbf-324">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="b0fbf-324">Return Value - enabled</span></span>

<span data-ttu-id="b0fbf-325">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-325">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="b0fbf-326">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="b0fbf-326">Remarks - enabled</span></span>

<span data-ttu-id="b0fbf-327">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-327">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="b0fbf-328">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-328">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="b0fbf-329">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-329">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="b0fbf-330">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="b0fbf-330">Method foregroundColor</span></span>

<span data-ttu-id="b0fbf-331">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-331">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="b0fbf-332">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="b0fbf-332">Parameters - foregroundColor</span></span>

<span data-ttu-id="b0fbf-333">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-333">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="b0fbf-334">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="b0fbf-334">Return Value - foregroundColor</span></span>

<span data-ttu-id="b0fbf-335">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-335">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="b0fbf-336">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="b0fbf-336">Remarks - foregroundColor</span></span>

<span data-ttu-id="b0fbf-337">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-337">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="b0fbf-338">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-338">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="b0fbf-339">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-339">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="b0fbf-340">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-340">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="b0fbf-341">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-341">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="b0fbf-342">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-342">The maximum value for a single byte is 255.</span></span>

## <a name="method-height"></a><span data-ttu-id="b0fbf-343">メソッド height</span><span class="sxs-lookup"><span data-stu-id="b0fbf-343">Method height</span></span>

<span data-ttu-id="b0fbf-344">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-344">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="b0fbf-345">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="b0fbf-345">Parameters - height</span></span>

<span data-ttu-id="b0fbf-346">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-346">value</span></span>  

<!-- -->

<span data-ttu-id="b0fbf-347">モード</span><span class="sxs-lookup"><span data-stu-id="b0fbf-347">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="b0fbf-348">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="b0fbf-348">Return Value - height</span></span>

<span data-ttu-id="b0fbf-349">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-349">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="b0fbf-350">備考 - height</span><span class="sxs-lookup"><span data-stu-id="b0fbf-350">Remarks - height</span></span>

<span data-ttu-id="b0fbf-351">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-351">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="b0fbf-352">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="b0fbf-352">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="b0fbf-353">モード。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-353">Mode.</span></span>            | <span data-ttu-id="b0fbf-354">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-354">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0fbf-355">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-355">-1 Exact.</span></span>        | <span data-ttu-id="b0fbf-356">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-356">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b0fbf-357">0 自動。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-357">0 Auto.</span></span>          | <span data-ttu-id="b0fbf-358">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-358">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b0fbf-359">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-359">1 Column height.</span></span> | <span data-ttu-id="b0fbf-360">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-360">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="b0fbf-361">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-361">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="b0fbf-362">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-362">Method heightMode</span></span>

<span data-ttu-id="b0fbf-363">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-363">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="b0fbf-364">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-364">Parameters - heightMode</span></span>

<span data-ttu-id="b0fbf-365">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-365">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="b0fbf-366">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-366">Return Value - heightMode</span></span>

<span data-ttu-id="b0fbf-367">計算モード。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-367">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="b0fbf-368">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-368">Remarks - heightMode</span></span>

<span data-ttu-id="b0fbf-369">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="b0fbf-369">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="b0fbf-370">モード。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-370">Mode.</span></span>          | <span data-ttu-id="b0fbf-371">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-371">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0fbf-372">正確。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-372">Exact.</span></span>         | <span data-ttu-id="b0fbf-373">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-373">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b0fbf-374">自動。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-374">Auto.</span></span>          | <span data-ttu-id="b0fbf-375">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-375">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b0fbf-376">列の高さ</span><span class="sxs-lookup"><span data-stu-id="b0fbf-376">Column height.</span></span> | <span data-ttu-id="b0fbf-377">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-377">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="b0fbf-378">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-378">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="b0fbf-379">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-379">Method heightValue</span></span>

<span data-ttu-id="b0fbf-380">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-380">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="b0fbf-381">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-381">Parameters - heightValue</span></span>

<span data-ttu-id="b0fbf-382">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-382">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="b0fbf-383">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-383">Return Value - heightValue</span></span>

<span data-ttu-id="b0fbf-384">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-384">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="b0fbf-385">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-385">Remarks - heightValue</span></span>

<span data-ttu-id="b0fbf-386">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-386">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="b0fbf-387">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="b0fbf-387">Method helpText</span></span>

<span data-ttu-id="b0fbf-388">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-388">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="b0fbf-389">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="b0fbf-389">Parameters - helpText</span></span>

<span data-ttu-id="b0fbf-390">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-390">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="b0fbf-391">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="b0fbf-391">Return Value - helpText</span></span>

<span data-ttu-id="b0fbf-392">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-392">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="b0fbf-393">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="b0fbf-393">Remarks - helpText</span></span>

<span data-ttu-id="b0fbf-394">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-394">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="b0fbf-395">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-395">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="b0fbf-396">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="b0fbf-396">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="b0fbf-397">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="b0fbf-397">Parameters - hierarchyParent</span></span>

<span data-ttu-id="b0fbf-398">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-398">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="b0fbf-399">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="b0fbf-399">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="b0fbf-400">メソッド id</span><span class="sxs-lookup"><span data-stu-id="b0fbf-400">Method id</span></span>

<span data-ttu-id="b0fbf-401">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-401">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="b0fbf-402">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="b0fbf-402">Return Value - id</span></span>

<span data-ttu-id="b0fbf-403">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-403">The ID of the control.</span></span>

## <a name="method-imagelocation"></a><span data-ttu-id="b0fbf-404">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="b0fbf-404">Method imageLocation</span></span>

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a><span data-ttu-id="b0fbf-405">パラメーター - imageLocation</span><span class="sxs-lookup"><span data-stu-id="b0fbf-405">Parameters - imageLocation</span></span>

<span data-ttu-id="b0fbf-406">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-406">value</span></span>  

### <a name="return-value---imagelocation"></a><span data-ttu-id="b0fbf-407">戻り値 - imageLocation</span><span class="sxs-lookup"><span data-stu-id="b0fbf-407">Return Value - imageLocation</span></span>

## <a name="method-imagemode"></a><span data-ttu-id="b0fbf-408">メソッド imagemode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-408">Method imagemode</span></span>

```xpp
public int imagemode([int value])
```

### <a name="parameters---imagemode"></a><span data-ttu-id="b0fbf-409">パラメーター - imagemode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-409">Parameters - imagemode</span></span>

<span data-ttu-id="b0fbf-410">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-410">value</span></span>  

### <a name="return-value---imagemode"></a><span data-ttu-id="b0fbf-411">戻り値 - imagemode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-411">Return Value - imagemode</span></span>

## <a name="method-imagename"></a><span data-ttu-id="b0fbf-412">メソッド imageName</span><span class="sxs-lookup"><span data-stu-id="b0fbf-412">Method imageName</span></span>

```xpp
public str imageName([str value])
```

### <a name="parameters---imagename"></a><span data-ttu-id="b0fbf-413">パラメーター - imageName</span><span class="sxs-lookup"><span data-stu-id="b0fbf-413">Parameters - imageName</span></span>

<span data-ttu-id="b0fbf-414">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-414">value</span></span>  

### <a name="return-value---imagename"></a><span data-ttu-id="b0fbf-415">戻り値 - imageName</span><span class="sxs-lookup"><span data-stu-id="b0fbf-415">Return Value - imageName</span></span>

## <a name="method-imageresource"></a><span data-ttu-id="b0fbf-416">メソッド imageResource</span><span class="sxs-lookup"><span data-stu-id="b0fbf-416">Method imageResource</span></span>

```xpp
public int imageResource([int value])
```

### <a name="parameters---imageresource"></a><span data-ttu-id="b0fbf-417">パラメーター - imageResource</span><span class="sxs-lookup"><span data-stu-id="b0fbf-417">Parameters - imageResource</span></span>

<span data-ttu-id="b0fbf-418">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-418">value</span></span>  

### <a name="return-value---imageresource"></a><span data-ttu-id="b0fbf-419">戻り値 - imageResource</span><span class="sxs-lookup"><span data-stu-id="b0fbf-419">Return Value - imageResource</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="b0fbf-420">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="b0fbf-420">Method isContainer</span></span>

<span data-ttu-id="b0fbf-421">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-421">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="b0fbf-422">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="b0fbf-422">Return Value - isContainer</span></span>

<span data-ttu-id="b0fbf-423">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-423">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-label"></a><span data-ttu-id="b0fbf-424">メソッド label</span><span class="sxs-lookup"><span data-stu-id="b0fbf-424">Method label</span></span>

<span data-ttu-id="b0fbf-425">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-425">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="b0fbf-426">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="b0fbf-426">Parameters - label</span></span>

<span data-ttu-id="b0fbf-427">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-427">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="b0fbf-428">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="b0fbf-428">Return Value - label</span></span>

<span data-ttu-id="b0fbf-429">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-429">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="b0fbf-430">備考 - label</span><span class="sxs-lookup"><span data-stu-id="b0fbf-430">Remarks - label</span></span>

<span data-ttu-id="b0fbf-431">ラベルは、コントロールに表示されるテキスト、またはプロパティ値が 250 文字を超えることができないラベルの横にあるテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-431">The label determines which text is displayed in the control or adjacent to the label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="b0fbf-432">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="b0fbf-432">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="b0fbf-433">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="b0fbf-433">Parameters - labelAlignment</span></span>

<span data-ttu-id="b0fbf-434">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-434">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="b0fbf-435">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="b0fbf-435">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="b0fbf-436">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="b0fbf-436">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="b0fbf-437">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="b0fbf-437">Parameters - labelBold</span></span>

<span data-ttu-id="b0fbf-438">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-438">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="b0fbf-439">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="b0fbf-439">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="b0fbf-440">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="b0fbf-440">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="b0fbf-441">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="b0fbf-441">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="b0fbf-442">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-442">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="b0fbf-443">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="b0fbf-443">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="b0fbf-444">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="b0fbf-444">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="b0fbf-445">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="b0fbf-445">Parameters - labelFont</span></span>

<span data-ttu-id="b0fbf-446">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-446">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="b0fbf-447">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="b0fbf-447">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="b0fbf-448">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="b0fbf-448">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="b0fbf-449">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="b0fbf-449">Parameters - labelFontSize</span></span>

<span data-ttu-id="b0fbf-450">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-450">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="b0fbf-451">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="b0fbf-451">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="b0fbf-452">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="b0fbf-452">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="b0fbf-453">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="b0fbf-453">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="b0fbf-454">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-454">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="b0fbf-455">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="b0fbf-455">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="b0fbf-456">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="b0fbf-456">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="b0fbf-457">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="b0fbf-457">Parameters - labelGuide</span></span>

<span data-ttu-id="b0fbf-458">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-458">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="b0fbf-459">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="b0fbf-459">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="b0fbf-460">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="b0fbf-460">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="b0fbf-461">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="b0fbf-461">Parameters - labelHeight</span></span>

<span data-ttu-id="b0fbf-462">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-462">value</span></span>  

<!-- -->

<span data-ttu-id="b0fbf-463">モード</span><span class="sxs-lookup"><span data-stu-id="b0fbf-463">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="b0fbf-464">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="b0fbf-464">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="b0fbf-465">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-465">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="b0fbf-466">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-466">Parameters - labelHeightMode</span></span>

<span data-ttu-id="b0fbf-467">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-467">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="b0fbf-468">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-468">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="b0fbf-469">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-469">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="b0fbf-470">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-470">Parameters - labelHeightValue</span></span>

<span data-ttu-id="b0fbf-471">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-471">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="b0fbf-472">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-472">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="b0fbf-473">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="b0fbf-473">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="b0fbf-474">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="b0fbf-474">Parameters - labelItalic</span></span>

<span data-ttu-id="b0fbf-475">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-475">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="b0fbf-476">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="b0fbf-476">Return Value - labelItalic</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="b0fbf-477">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="b0fbf-477">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="b0fbf-478">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="b0fbf-478">Parameters - labelPosition</span></span>

<span data-ttu-id="b0fbf-479">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-479">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="b0fbf-480">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="b0fbf-480">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="b0fbf-481">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="b0fbf-481">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="b0fbf-482">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="b0fbf-482">Parameters - labelUnderline</span></span>

<span data-ttu-id="b0fbf-483">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-483">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="b0fbf-484">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="b0fbf-484">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="b0fbf-485">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="b0fbf-485">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="b0fbf-486">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="b0fbf-486">Parameters - labelWidth</span></span>

<span data-ttu-id="b0fbf-487">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-487">value</span></span>  

<!-- -->

<span data-ttu-id="b0fbf-488">モード</span><span class="sxs-lookup"><span data-stu-id="b0fbf-488">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="b0fbf-489">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="b0fbf-489">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="b0fbf-490">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-490">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="b0fbf-491">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-491">Parameters - labelWidthMode</span></span>

<span data-ttu-id="b0fbf-492">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-492">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="b0fbf-493">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-493">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="b0fbf-494">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-494">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="b0fbf-495">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-495">Parameters - labelWidthValue</span></span>

<span data-ttu-id="b0fbf-496">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-496">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="b0fbf-497">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-497">Return Value - labelWidthValue</span></span>

## <a name="method-left"></a><span data-ttu-id="b0fbf-498">メソッド left</span><span class="sxs-lookup"><span data-stu-id="b0fbf-498">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="b0fbf-499">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="b0fbf-499">Parameters - left</span></span>

<span data-ttu-id="b0fbf-500">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-500">value</span></span>  

<!-- -->

<span data-ttu-id="b0fbf-501">モード</span><span class="sxs-lookup"><span data-stu-id="b0fbf-501">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="b0fbf-502">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="b0fbf-502">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="b0fbf-503">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-503">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="b0fbf-504">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-504">Parameters - leftMode</span></span>

<span data-ttu-id="b0fbf-505">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-505">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="b0fbf-506">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-506">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="b0fbf-507">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-507">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="b0fbf-508">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-508">Parameters - leftValue</span></span>

<span data-ttu-id="b0fbf-509">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-509">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="b0fbf-510">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-510">Return Value - leftValue</span></span>

## <a name="method-location"></a><span data-ttu-id="b0fbf-511">メソッド location</span><span class="sxs-lookup"><span data-stu-id="b0fbf-511">Method location</span></span>

```xpp
public str location([str value])
```

### <a name="parameters---location"></a><span data-ttu-id="b0fbf-512">パラメーター - location</span><span class="sxs-lookup"><span data-stu-id="b0fbf-512">Parameters - location</span></span>

<span data-ttu-id="b0fbf-513">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-513">value</span></span>  

### <a name="return-value---location"></a><span data-ttu-id="b0fbf-514">戻り値 - location</span><span class="sxs-lookup"><span data-stu-id="b0fbf-514">Return Value - location</span></span>

## <a name="method-name"></a><span data-ttu-id="b0fbf-515">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b0fbf-515">Method name</span></span>

<span data-ttu-id="b0fbf-516">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-516">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="b0fbf-517">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="b0fbf-517">Parameters - name</span></span>

<span data-ttu-id="b0fbf-518">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-518">value</span></span>  
<span data-ttu-id="b0fbf-519">コントロールに割り当てる名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-519">The name to assign to the control; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="b0fbf-520">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="b0fbf-520">Return Value - name</span></span>

<span data-ttu-id="b0fbf-521">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-521">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="b0fbf-522">備考 - name</span><span class="sxs-lookup"><span data-stu-id="b0fbf-522">Remarks - name</span></span>

<span data-ttu-id="b0fbf-523">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-523">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="b0fbf-524">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-524">It must start with a letter.</span></span>
-   <span data-ttu-id="b0fbf-525">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-525">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="b0fbf-526">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-526">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="b0fbf-527">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-527">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="b0fbf-528">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-528">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="b0fbf-529">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="b0fbf-529">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="b0fbf-530">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="b0fbf-530">Parameters - neededPermission</span></span>

<span data-ttu-id="b0fbf-531">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-531">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="b0fbf-532">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="b0fbf-532">Return Value - neededPermission</span></span>

## <a name="method-normalimage"></a><span data-ttu-id="b0fbf-533">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="b0fbf-533">Method normalImage</span></span>

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a><span data-ttu-id="b0fbf-534">パラメーター - normalImage</span><span class="sxs-lookup"><span data-stu-id="b0fbf-534">Parameters - normalImage</span></span>

<span data-ttu-id="b0fbf-535">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-535">value</span></span>  

### <a name="return-value---normalimage"></a><span data-ttu-id="b0fbf-536">戻り値 - normalImage</span><span class="sxs-lookup"><span data-stu-id="b0fbf-536">Return Value - normalImage</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="b0fbf-537">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="b0fbf-537">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="b0fbf-538">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="b0fbf-538">Parameters - promptrect</span></span>

<span data-ttu-id="b0fbf-539">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-539">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="b0fbf-540">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="b0fbf-540">Return Value - promptrect</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="b0fbf-541">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="b0fbf-541">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="b0fbf-542">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="b0fbf-542">Parameters - securityKey</span></span>

<span data-ttu-id="b0fbf-543">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-543">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="b0fbf-544">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="b0fbf-544">Return Value - securityKey</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="b0fbf-545">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="b0fbf-545">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="b0fbf-546">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="b0fbf-546">Parameters - showLabel</span></span>

<span data-ttu-id="b0fbf-547">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-547">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="b0fbf-548">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="b0fbf-548">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="b0fbf-549">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="b0fbf-549">Method skip</span></span>

<span data-ttu-id="b0fbf-550">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-550">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="b0fbf-551">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="b0fbf-551">Parameters - skip</span></span>

<span data-ttu-id="b0fbf-552">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-552">value</span></span>  
<span data-ttu-id="b0fbf-553">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-553">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="b0fbf-554">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="b0fbf-554">Return Value - skip</span></span>

<span data-ttu-id="b0fbf-555">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-555">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-top"></a><span data-ttu-id="b0fbf-556">メソッド top</span><span class="sxs-lookup"><span data-stu-id="b0fbf-556">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="b0fbf-557">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="b0fbf-557">Parameters - top</span></span>

<span data-ttu-id="b0fbf-558">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-558">value</span></span>  

<!-- -->

<span data-ttu-id="b0fbf-559">モード</span><span class="sxs-lookup"><span data-stu-id="b0fbf-559">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="b0fbf-560">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="b0fbf-560">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="b0fbf-561">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-561">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="b0fbf-562">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-562">Parameters - topMode</span></span>

<span data-ttu-id="b0fbf-563">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-563">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="b0fbf-564">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-564">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="b0fbf-565">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-565">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="b0fbf-566">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-566">Parameters - topValue</span></span>

<span data-ttu-id="b0fbf-567">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-567">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="b0fbf-568">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-568">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="b0fbf-569">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="b0fbf-569">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="b0fbf-570">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="b0fbf-570">Parameters - type</span></span>

<span data-ttu-id="b0fbf-571">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-571">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="b0fbf-572">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="b0fbf-572">Return Value - type</span></span>

## <a name="method-userdata"></a><span data-ttu-id="b0fbf-573">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="b0fbf-573">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="b0fbf-574">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="b0fbf-574">Parameters - userData</span></span>

<span data-ttu-id="b0fbf-575">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-575">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="b0fbf-576">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="b0fbf-576">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="b0fbf-577">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="b0fbf-577">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="b0fbf-578">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="b0fbf-578">Parameters - userDataItem</span></span>

<span data-ttu-id="b0fbf-579">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-579">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="b0fbf-580">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="b0fbf-580">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="b0fbf-581">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="b0fbf-581">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="b0fbf-582">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="b0fbf-582">Parameters - userDataItems</span></span>

<span data-ttu-id="b0fbf-583">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-583">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="b0fbf-584">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="b0fbf-584">Return Value - userDataItems</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="b0fbf-585">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="b0fbf-585">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="b0fbf-586">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="b0fbf-586">Parameters - verticalSpacing</span></span>

<span data-ttu-id="b0fbf-587">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-587">value</span></span>  

<!-- -->

<span data-ttu-id="b0fbf-588">モード</span><span class="sxs-lookup"><span data-stu-id="b0fbf-588">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="b0fbf-589">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="b0fbf-589">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="b0fbf-590">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-590">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="b0fbf-591">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-591">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="b0fbf-592">モード</span><span class="sxs-lookup"><span data-stu-id="b0fbf-592">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="b0fbf-593">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-593">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="b0fbf-594">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-594">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="b0fbf-595">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-595">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="b0fbf-596">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-596">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="b0fbf-597">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-597">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="b0fbf-598">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="b0fbf-598">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="b0fbf-599">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="b0fbf-599">Parameters - visible</span></span>

<span data-ttu-id="b0fbf-600">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-600">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="b0fbf-601">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="b0fbf-601">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="b0fbf-602">メソッド width</span><span class="sxs-lookup"><span data-stu-id="b0fbf-602">Method width</span></span>

<span data-ttu-id="b0fbf-603">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-603">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="b0fbf-604">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="b0fbf-604">Parameters - width</span></span>

<span data-ttu-id="b0fbf-605">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-605">value</span></span>  

<!-- -->

<span data-ttu-id="b0fbf-606">モード</span><span class="sxs-lookup"><span data-stu-id="b0fbf-606">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="b0fbf-607">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="b0fbf-607">Return Value - width</span></span>

<span data-ttu-id="b0fbf-608">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-608">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="b0fbf-609">備考 - width</span><span class="sxs-lookup"><span data-stu-id="b0fbf-609">Remarks - width</span></span>

<span data-ttu-id="b0fbf-610">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-610">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="b0fbf-611">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="b0fbf-611">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="b0fbf-612">モード。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-612">Mode.</span></span>           | <span data-ttu-id="b0fbf-613">幅計算。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-613">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0fbf-614">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-614">-1 Exact.</span></span>       | <span data-ttu-id="b0fbf-615">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-615">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b0fbf-616">0 自動。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-616">0 Auto.</span></span>         | <span data-ttu-id="b0fbf-617">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-617">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b0fbf-618">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-618">1 Column width.</span></span> | <span data-ttu-id="b0fbf-619">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-619">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="b0fbf-620">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-620">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="b0fbf-621">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-621">Method widthMode</span></span>

<span data-ttu-id="b0fbf-622">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-622">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="b0fbf-623">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-623">Parameters - widthMode</span></span>

<span data-ttu-id="b0fbf-624">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-624">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="b0fbf-625">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-625">Return Value - widthMode</span></span>

<span data-ttu-id="b0fbf-626">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-626">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="b0fbf-627">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="b0fbf-627">Remarks - widthMode</span></span>

<span data-ttu-id="b0fbf-628">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="b0fbf-628">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="b0fbf-629">モード。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-629">Mode.</span></span>         | <span data-ttu-id="b0fbf-630">幅計算。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-630">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0fbf-631">正確。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-631">Exact.</span></span>        | <span data-ttu-id="b0fbf-632">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-632">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b0fbf-633">自動。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-633">Auto.</span></span>         | <span data-ttu-id="b0fbf-634">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-634">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b0fbf-635">列の幅。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-635">Column width.</span></span> | <span data-ttu-id="b0fbf-636">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-636">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="b0fbf-637">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-637">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="b0fbf-638">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-638">Method widthValue</span></span>

<span data-ttu-id="b0fbf-639">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-639">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="b0fbf-640">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-640">Parameters - widthValue</span></span>

<span data-ttu-id="b0fbf-641">値</span><span class="sxs-lookup"><span data-stu-id="b0fbf-641">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="b0fbf-642">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-642">Return Value - widthValue</span></span>

<span data-ttu-id="b0fbf-643">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-643">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="b0fbf-644">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="b0fbf-644">Remarks - widthValue</span></span>

<span data-ttu-id="b0fbf-645">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="b0fbf-645">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="b0fbf-646">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="b0fbf-646">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="b0fbf-647">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="b0fbf-647">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="b0fbf-648">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="b0fbf-648">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="b0fbf-649">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="b0fbf-649">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="b0fbf-650">overrideObject</span><span class="sxs-lookup"><span data-stu-id="b0fbf-650">overrideObject</span></span>  

