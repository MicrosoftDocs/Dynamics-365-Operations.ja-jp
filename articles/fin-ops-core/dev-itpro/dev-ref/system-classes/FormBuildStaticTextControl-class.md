---
title: FormBuildStaticTextControl クラス
description: このトピックでは、FormBuildStaticTextControl クラスについて説明します。
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
ms.openlocfilehash: 316e88bdbc70e673fb98fcb6a822f5ac0990a75e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502642"
---
# <a name="class-formbuildstatictextcontrol"></a><span data-ttu-id="60180-103">クラス FormBuildStaticTextControl</span><span class="sxs-lookup"><span data-stu-id="60180-103">Class FormBuildStaticTextControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildStaticTextControl extends FormBuildControl
```

<span data-ttu-id="60180-104">FormBuildStaticTextControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="60180-104">The FormBuildStaticTextControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="60180-105">備考</span><span class="sxs-lookup"><span data-stu-id="60180-105">Remarks</span></span>

<span data-ttu-id="60180-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="60180-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="60180-107">例</span><span class="sxs-lookup"><span data-stu-id="60180-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="60180-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="60180-108">Methods</span></span>

| <span data-ttu-id="60180-109">方法</span><span class="sxs-lookup"><span data-stu-id="60180-109">Method</span></span>                                                                                                      | <span data-ttu-id="60180-110">説明</span><span class="sxs-lookup"><span data-stu-id="60180-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60180-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="60180-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="60180-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="60180-112">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="60180-113">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-113">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="60180-114">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="60180-114">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="60180-115">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="60180-115">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="60180-116">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="60180-116">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="60180-117">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="60180-117">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="60180-118">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-118">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="60180-119">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-119">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="60180-120">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-120">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="60180-121">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="60180-121">Determines whether the control background can be transparent.</span></span>                                                                          |
| <span data-ttu-id="60180-122">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-122">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="60180-123">コントロール内のテキストを出力するのに使用されたフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-123">Gets or sets the weight of font that was used to output text in the control.</span></span>                                                            |
| <span data-ttu-id="60180-124">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-124">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="60180-125">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-125">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="60180-126">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-126">Gets or sets the character set of the font.</span></span>                                                                                             |
| <span data-ttu-id="60180-127">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-127">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="60180-128">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-128">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="60180-129">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="60180-129">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="60180-130">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-130">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="60180-131">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="60180-131">public int containerId()</span></span>                                                                                    | <span data-ttu-id="60180-132">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="60180-132">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="60180-133">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="60180-133">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="60180-134">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="60180-134">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                         |
| <span data-ttu-id="60180-135">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="60180-135">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="60180-136">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="60180-136">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="60180-137">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="60180-137">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="60180-138">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="60180-138">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="60180-139">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-139">Gets or sets a data source to be used by the control or the form.</span></span>                                                                       |
| <span data-ttu-id="60180-140">public int displayHeight(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="60180-140">public int displayHeight(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                         |
| <span data-ttu-id="60180-141">public AutoMode displayHeightMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="60180-141">public AutoMode displayHeightMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                         |
| <span data-ttu-id="60180-142">public int displayHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-142">public int displayHeightValue(\[int value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="60180-143">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="60180-143">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                         |
| <span data-ttu-id="60180-144">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="60180-144">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                         |
| <span data-ttu-id="60180-145">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-145">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="60180-146">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-146">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="60180-147">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-147">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="60180-148">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="60180-148">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="60180-149">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="60180-149">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="60180-150">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="60180-150">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="60180-151">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="60180-151">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="60180-152">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-152">Gets or sets the name of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="60180-153">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-153">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="60180-154">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-154">Gets or sets the size of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="60180-155">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-155">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="60180-156">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-156">Gets or sets the text color for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="60180-157">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="60180-157">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="60180-158">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-158">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="60180-159">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-159">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="60180-160">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-160">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="60180-161">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-161">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="60180-162">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-162">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="60180-163">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="60180-163">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="60180-164">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-164">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="60180-165">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="60180-165">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="60180-166">public int id()</span><span class="sxs-lookup"><span data-stu-id="60180-166">public int id()</span></span>                                                                                             | <span data-ttu-id="60180-167">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="60180-167">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="60180-168">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="60180-168">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="60180-169">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="60180-169">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="60180-170">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="60180-170">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="60180-171">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="60180-171">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="60180-172">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-172">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="60180-173">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-173">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="60180-174">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="60180-174">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="60180-175">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-175">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="60180-176">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-176">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="60180-177">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="60180-177">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="60180-178">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="60180-178">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="60180-179">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="60180-179">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="60180-180">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-180">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="60180-181">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="60180-181">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="60180-182">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="60180-182">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="60180-183">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-183">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="60180-184">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-184">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="60180-185">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-185">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="60180-186">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="60180-186">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="60180-187">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="60180-187">Sets or returns the underline property for the text in the control.</span></span>                                                                     |
| <span data-ttu-id="60180-188">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-188">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="60180-189">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-189">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="60180-190">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-190">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="60180-191">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="60180-191">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="60180-192">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="60180-192">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="60180-193">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-193">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="60180-194">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="60180-194">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="60180-195">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="60180-195">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="60180-196">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-196">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="60180-197">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-197">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="60180-198">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-198">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="60180-199">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="60180-199">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="60180-200">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-200">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="60180-201">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="60180-201">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="60180-202">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="60180-202">Method alignControl</span></span>

<span data-ttu-id="60180-203">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="60180-203">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="60180-204">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="60180-204">Parameters - alignControl</span></span>

<span data-ttu-id="60180-205">値</span><span class="sxs-lookup"><span data-stu-id="60180-205">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="60180-206">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="60180-206">Return Value - alignControl</span></span>

<span data-ttu-id="60180-207">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="60180-207">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="60180-208">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="60180-208">Remarks - alignControl</span></span>

<span data-ttu-id="60180-209">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="60180-209">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="60180-210">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="60180-210">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="60180-211">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="60180-211">Parameters - alignment</span></span>

<span data-ttu-id="60180-212">値</span><span class="sxs-lookup"><span data-stu-id="60180-212">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="60180-213">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="60180-213">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="60180-214">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="60180-214">Method allowEdit</span></span>

<span data-ttu-id="60180-215">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="60180-215">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="60180-216">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="60180-216">Parameters - allowEdit</span></span>

<span data-ttu-id="60180-217">値</span><span class="sxs-lookup"><span data-stu-id="60180-217">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="60180-218">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="60180-218">Return Value - allowEdit</span></span>

<span data-ttu-id="60180-219">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="60180-219">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="60180-220">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="60180-220">Remarks - allowEdit</span></span>

<span data-ttu-id="60180-221">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="60180-221">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="60180-222">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="60180-222">Method autoDeclaration</span></span>

<span data-ttu-id="60180-223">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="60180-223">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="60180-224">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="60180-224">Parameters - autoDeclaration</span></span>

<span data-ttu-id="60180-225">値</span><span class="sxs-lookup"><span data-stu-id="60180-225">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="60180-226">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="60180-226">Return Value - autoDeclaration</span></span>

<span data-ttu-id="60180-227">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="60180-227">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="60180-228">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="60180-228">Remarks - autoDeclaration</span></span>

<span data-ttu-id="60180-229">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="60180-229">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="60180-230">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="60180-230">Method backgroundColor</span></span>

<span data-ttu-id="60180-231">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-231">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="60180-232">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="60180-232">Parameters - backgroundColor</span></span>

<span data-ttu-id="60180-233">値</span><span class="sxs-lookup"><span data-stu-id="60180-233">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="60180-234">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="60180-234">Return Value - backgroundColor</span></span>

<span data-ttu-id="60180-235">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="60180-235">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="60180-236">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="60180-236">Remarks - backgroundColor</span></span>

<span data-ttu-id="60180-237">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="60180-237">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="60180-238">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="60180-238">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="60180-239">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="60180-239">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="60180-240">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="60180-240">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="60180-241">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="60180-241">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="60180-242">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="60180-242">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="60180-243">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="60180-243">Method backStyle</span></span>

<span data-ttu-id="60180-244">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="60180-244">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="60180-245">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="60180-245">Parameters - backStyle</span></span>

<span data-ttu-id="60180-246">値</span><span class="sxs-lookup"><span data-stu-id="60180-246">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="60180-247">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="60180-247">Return Value - backStyle</span></span>

<span data-ttu-id="60180-248">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="60180-248">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="60180-249">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="60180-249">Method bold</span></span>

<span data-ttu-id="60180-250">コントロール内のテキストを出力するのに使用されたフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-250">Gets or sets the weight of font that was used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="60180-251">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="60180-251">Parameters - bold</span></span>

<span data-ttu-id="60180-252">値</span><span class="sxs-lookup"><span data-stu-id="60180-252">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="60180-253">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="60180-253">Return Value - bold</span></span>

<span data-ttu-id="60180-254">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="60180-254">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="60180-255">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="60180-255">Remarks - bold</span></span>

<span data-ttu-id="60180-256">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="60180-256">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="60180-257">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="60180-257">0 Use the default font weight.</span></span>
-   <span data-ttu-id="60180-258">1 シン。</span><span class="sxs-lookup"><span data-stu-id="60180-258">1 Thin.</span></span>
-   <span data-ttu-id="60180-259">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="60180-259">2 Extra-light.</span></span>
-   <span data-ttu-id="60180-260">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="60180-260">3 Light.</span></span>
-   <span data-ttu-id="60180-261">4 標準。</span><span class="sxs-lookup"><span data-stu-id="60180-261">4 Normal.</span></span>
-   <span data-ttu-id="60180-262">5 中。</span><span class="sxs-lookup"><span data-stu-id="60180-262">5 Medium.</span></span>
-   <span data-ttu-id="60180-263">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="60180-263">6 Semibold.</span></span>
-   <span data-ttu-id="60180-264">7 太字。</span><span class="sxs-lookup"><span data-stu-id="60180-264">7 Bold.</span></span>
-   <span data-ttu-id="60180-265">8 極太。</span><span class="sxs-lookup"><span data-stu-id="60180-265">8 Extra-bold.</span></span>
-   <span data-ttu-id="60180-266">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="60180-266">9 Heavy.</span></span>

## <a name="method-cachedatamethod"></a><span data-ttu-id="60180-267">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="60180-267">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="60180-268">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="60180-268">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="60180-269">値</span><span class="sxs-lookup"><span data-stu-id="60180-269">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="60180-270">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="60180-270">Return Value - cacheDataMethod</span></span>

## <a name="method-characterset"></a><span data-ttu-id="60180-271">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="60180-271">Method characterSet</span></span>

<span data-ttu-id="60180-272">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-272">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="60180-273">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="60180-273">Parameters - characterSet</span></span>

<span data-ttu-id="60180-274">値</span><span class="sxs-lookup"><span data-stu-id="60180-274">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="60180-275">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="60180-275">Return Value - characterSet</span></span>

<span data-ttu-id="60180-276">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="60180-276">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="60180-277">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="60180-277">Remarks - characterSet</span></span>

<span data-ttu-id="60180-278">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="60180-278">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="60180-279">値です。</span><span class="sxs-lookup"><span data-stu-id="60180-279">Value.</span></span> | <span data-ttu-id="60180-280">説明。</span><span class="sxs-lookup"><span data-stu-id="60180-280">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="60180-281">0</span><span class="sxs-lookup"><span data-stu-id="60180-281">0</span></span>      | <span data-ttu-id="60180-282">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="60180-282">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="60180-283">1</span><span class="sxs-lookup"><span data-stu-id="60180-283">1</span></span>      | <span data-ttu-id="60180-284">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="60180-284">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="60180-285">2</span><span class="sxs-lookup"><span data-stu-id="60180-285">2</span></span>      | <span data-ttu-id="60180-286">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="60180-286">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="60180-287">77</span><span class="sxs-lookup"><span data-stu-id="60180-287">77</span></span>     | <span data-ttu-id="60180-288">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="60180-288">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="60180-289">128</span><span class="sxs-lookup"><span data-stu-id="60180-289">128</span></span>    | <span data-ttu-id="60180-290">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="60180-290">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="60180-291">129</span><span class="sxs-lookup"><span data-stu-id="60180-291">129</span></span>    | <span data-ttu-id="60180-292">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="60180-292">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="60180-293">134</span><span class="sxs-lookup"><span data-stu-id="60180-293">134</span></span>    | <span data-ttu-id="60180-294">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="60180-294">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="60180-295">136</span><span class="sxs-lookup"><span data-stu-id="60180-295">136</span></span>    | <span data-ttu-id="60180-296">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="60180-296">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="60180-297">161</span><span class="sxs-lookup"><span data-stu-id="60180-297">161</span></span>    | <span data-ttu-id="60180-298">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="60180-298">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="60180-299">162</span><span class="sxs-lookup"><span data-stu-id="60180-299">162</span></span>    | <span data-ttu-id="60180-300">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="60180-300">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="60180-301">163</span><span class="sxs-lookup"><span data-stu-id="60180-301">163</span></span>    | <span data-ttu-id="60180-302">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="60180-302">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="60180-303">186</span><span class="sxs-lookup"><span data-stu-id="60180-303">186</span></span>    | <span data-ttu-id="60180-304">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="60180-304">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="60180-305">204</span><span class="sxs-lookup"><span data-stu-id="60180-305">204</span></span>    | <span data-ttu-id="60180-306">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="60180-306">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="60180-307">238</span><span class="sxs-lookup"><span data-stu-id="60180-307">238</span></span>    | <span data-ttu-id="60180-308">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="60180-308">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="60180-309">255</span><span class="sxs-lookup"><span data-stu-id="60180-309">255</span></span>    | <span data-ttu-id="60180-310">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="60180-310">OEM\_CHARSET</span></span>         |

<span data-ttu-id="60180-311">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="60180-311">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="60180-312">値です。</span><span class="sxs-lookup"><span data-stu-id="60180-312">Value.</span></span> | <span data-ttu-id="60180-313">説明。</span><span class="sxs-lookup"><span data-stu-id="60180-313">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="60180-314">130</span><span class="sxs-lookup"><span data-stu-id="60180-314">130</span></span>    | <span data-ttu-id="60180-315">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="60180-315">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="60180-316">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="60180-316">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="60180-317">値です。</span><span class="sxs-lookup"><span data-stu-id="60180-317">Value.</span></span> | <span data-ttu-id="60180-318">説明。</span><span class="sxs-lookup"><span data-stu-id="60180-318">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="60180-319">177</span><span class="sxs-lookup"><span data-stu-id="60180-319">177</span></span>    | <span data-ttu-id="60180-320">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="60180-320">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="60180-321">178</span><span class="sxs-lookup"><span data-stu-id="60180-321">178</span></span>    | <span data-ttu-id="60180-322">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="60180-322">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="60180-323">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="60180-323">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="60180-324">値です。</span><span class="sxs-lookup"><span data-stu-id="60180-324">Value.</span></span> | <span data-ttu-id="60180-325">説明。</span><span class="sxs-lookup"><span data-stu-id="60180-325">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="60180-326">222</span><span class="sxs-lookup"><span data-stu-id="60180-326">222</span></span>    | <span data-ttu-id="60180-327">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="60180-327">THAI\_CHARSET</span></span> |

<span data-ttu-id="60180-328">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="60180-328">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="60180-329">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="60180-329">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="60180-330">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="60180-330">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="60180-331">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="60180-331">Method colorScheme</span></span>

<span data-ttu-id="60180-332">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-332">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="60180-333">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="60180-333">Parameters - colorScheme</span></span>

<span data-ttu-id="60180-334">値</span><span class="sxs-lookup"><span data-stu-id="60180-334">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="60180-335">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="60180-335">Return Value - colorScheme</span></span>

<span data-ttu-id="60180-336">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="60180-336">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="60180-337">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="60180-337">Remarks - colorScheme</span></span>

<span data-ttu-id="60180-338">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="60180-338">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="60180-339">値です。</span><span class="sxs-lookup"><span data-stu-id="60180-339">Value.</span></span> | <span data-ttu-id="60180-340">スタイル。</span><span class="sxs-lookup"><span data-stu-id="60180-340">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="60180-341">0</span><span class="sxs-lookup"><span data-stu-id="60180-341">0</span></span>      | <span data-ttu-id="60180-342">既定。</span><span class="sxs-lookup"><span data-stu-id="60180-342">Default.</span></span>                      |
| <span data-ttu-id="60180-343">1</span><span class="sxs-lookup"><span data-stu-id="60180-343">1</span></span>      | <span data-ttu-id="60180-344">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="60180-344">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="60180-345">2</span><span class="sxs-lookup"><span data-stu-id="60180-345">2</span></span>      | <span data-ttu-id="60180-346">真の配色。</span><span class="sxs-lookup"><span data-stu-id="60180-346">The true-color scheme.</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="60180-347">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="60180-347">Method configurationKey</span></span>

<span data-ttu-id="60180-348">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-348">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="60180-349">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="60180-349">Parameters - configurationKey</span></span>

<span data-ttu-id="60180-350">値</span><span class="sxs-lookup"><span data-stu-id="60180-350">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="60180-351">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="60180-351">Return Value - configurationKey</span></span>

<span data-ttu-id="60180-352">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="60180-352">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="60180-353">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="60180-353">Remarks - configurationKey</span></span>

<span data-ttu-id="60180-354">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="60180-354">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="60180-355">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="60180-355">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="60180-356">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="60180-356">Method containerId</span></span>

<span data-ttu-id="60180-357">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="60180-357">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="60180-358">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="60180-358">Return Value - containerId</span></span>

<span data-ttu-id="60180-359">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="60180-359">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="60180-360">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="60180-360">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="60180-361">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="60180-361">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="60180-362">値</span><span class="sxs-lookup"><span data-stu-id="60180-362">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="60180-363">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="60180-363">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="60180-364">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="60180-364">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="60180-365">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="60180-365">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="60180-366">値</span><span class="sxs-lookup"><span data-stu-id="60180-366">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="60180-367">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="60180-367">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="60180-368">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="60180-368">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="60180-369">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="60180-369">Parameters - dataField</span></span>

<span data-ttu-id="60180-370">値</span><span class="sxs-lookup"><span data-stu-id="60180-370">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="60180-371">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="60180-371">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="60180-372">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="60180-372">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="60180-373">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="60180-373">Parameters - dataMethod</span></span>

<span data-ttu-id="60180-374">値</span><span class="sxs-lookup"><span data-stu-id="60180-374">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="60180-375">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="60180-375">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="60180-376">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="60180-376">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="60180-377">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="60180-377">Parameters - dataRelationPath</span></span>

<span data-ttu-id="60180-378">値</span><span class="sxs-lookup"><span data-stu-id="60180-378">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="60180-379">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="60180-379">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="60180-380">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="60180-380">Method dataSource</span></span>

<span data-ttu-id="60180-381">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-381">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="60180-382">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="60180-382">Parameters - dataSource</span></span>

<span data-ttu-id="60180-383">値</span><span class="sxs-lookup"><span data-stu-id="60180-383">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="60180-384">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="60180-384">Return Value - dataSource</span></span>

<span data-ttu-id="60180-385">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="60180-385">The identifier of the data source to be used.</span></span>

## <a name="method-displayheight"></a><span data-ttu-id="60180-386">メソッド displayHeight</span><span class="sxs-lookup"><span data-stu-id="60180-386">Method displayHeight</span></span>

```xpp
public int displayHeight([int value], [AutoMode mode])
```

### <a name="parameters---displayheight"></a><span data-ttu-id="60180-387">パラメーター - displayHeight</span><span class="sxs-lookup"><span data-stu-id="60180-387">Parameters - displayHeight</span></span>

<span data-ttu-id="60180-388">値</span><span class="sxs-lookup"><span data-stu-id="60180-388">value</span></span>  

<!-- -->

<span data-ttu-id="60180-389">モード</span><span class="sxs-lookup"><span data-stu-id="60180-389">mode</span></span>  

### <a name="return-value---displayheight"></a><span data-ttu-id="60180-390">戻り値 - displayHeight</span><span class="sxs-lookup"><span data-stu-id="60180-390">Return Value - displayHeight</span></span>

## <a name="method-displayheightmode"></a><span data-ttu-id="60180-391">メソッド displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="60180-391">Method displayHeightMode</span></span>

```xpp
public AutoMode displayHeightMode([AutoMode mode])
```

### <a name="parameters---displayheightmode"></a><span data-ttu-id="60180-392">パラメーター - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="60180-392">Parameters - displayHeightMode</span></span>

<span data-ttu-id="60180-393">モード</span><span class="sxs-lookup"><span data-stu-id="60180-393">mode</span></span>  

### <a name="return-value---displayheightmode"></a><span data-ttu-id="60180-394">戻り値 - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="60180-394">Return Value - displayHeightMode</span></span>

## <a name="method-displayheightvalue"></a><span data-ttu-id="60180-395">メソッド displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="60180-395">Method displayHeightValue</span></span>

```xpp
public int displayHeightValue([int value])
```

### <a name="parameters---displayheightvalue"></a><span data-ttu-id="60180-396">パラメーター - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="60180-396">Parameters - displayHeightValue</span></span>

<span data-ttu-id="60180-397">値</span><span class="sxs-lookup"><span data-stu-id="60180-397">value</span></span>  

### <a name="return-value---displayheightvalue"></a><span data-ttu-id="60180-398">戻り値 - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="60180-398">Return Value - displayHeightValue</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="60180-399">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="60180-399">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="60180-400">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="60180-400">Parameters - displayLength</span></span>

<span data-ttu-id="60180-401">値</span><span class="sxs-lookup"><span data-stu-id="60180-401">value</span></span>  

<!-- -->

<span data-ttu-id="60180-402">モード</span><span class="sxs-lookup"><span data-stu-id="60180-402">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="60180-403">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="60180-403">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="60180-404">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="60180-404">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="60180-405">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="60180-405">Parameters - displayLengthMode</span></span>

<span data-ttu-id="60180-406">モード</span><span class="sxs-lookup"><span data-stu-id="60180-406">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="60180-407">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="60180-407">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="60180-408">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="60180-408">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="60180-409">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="60180-409">Parameters - displayLengthValue</span></span>

<span data-ttu-id="60180-410">値</span><span class="sxs-lookup"><span data-stu-id="60180-410">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="60180-411">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="60180-411">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="60180-412">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="60180-412">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="60180-413">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="60180-413">Parameters - displayTarget</span></span>

<span data-ttu-id="60180-414">値</span><span class="sxs-lookup"><span data-stu-id="60180-414">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="60180-415">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="60180-415">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="60180-416">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="60180-416">Method dragDrop</span></span>

<span data-ttu-id="60180-417">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="60180-417">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="60180-418">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="60180-418">Parameters - dragDrop</span></span>

<span data-ttu-id="60180-419">値</span><span class="sxs-lookup"><span data-stu-id="60180-419">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="60180-420">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="60180-420">Return Value - dragDrop</span></span>

<span data-ttu-id="60180-421">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="60180-421">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="60180-422">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="60180-422">Method enabled</span></span>

<span data-ttu-id="60180-423">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="60180-423">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="60180-424">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="60180-424">Parameters - enabled</span></span>

<span data-ttu-id="60180-425">値</span><span class="sxs-lookup"><span data-stu-id="60180-425">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="60180-426">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="60180-426">Return Value - enabled</span></span>

<span data-ttu-id="60180-427">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="60180-427">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="60180-428">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="60180-428">Remarks - enabled</span></span>

<span data-ttu-id="60180-429">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="60180-429">The enabled property gives controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="60180-430">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="60180-430">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="60180-431">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="60180-431">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="60180-432">メソッド font</span><span class="sxs-lookup"><span data-stu-id="60180-432">Method font</span></span>

<span data-ttu-id="60180-433">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-433">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="60180-434">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="60180-434">Parameters - font</span></span>

<span data-ttu-id="60180-435">値</span><span class="sxs-lookup"><span data-stu-id="60180-435">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="60180-436">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="60180-436">Return Value - font</span></span>

<span data-ttu-id="60180-437">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="60180-437">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="60180-438">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="60180-438">Method fontSize</span></span>

<span data-ttu-id="60180-439">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-439">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="60180-440">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="60180-440">Parameters - fontSize</span></span>

<span data-ttu-id="60180-441">値</span><span class="sxs-lookup"><span data-stu-id="60180-441">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="60180-442">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="60180-442">Return Value - fontSize</span></span>

<span data-ttu-id="60180-443">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="60180-443">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="60180-444">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="60180-444">Method foregroundColor</span></span>

<span data-ttu-id="60180-445">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-445">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="60180-446">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="60180-446">Parameters - foregroundColor</span></span>

<span data-ttu-id="60180-447">値</span><span class="sxs-lookup"><span data-stu-id="60180-447">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="60180-448">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="60180-448">Return Value - foregroundColor</span></span>

<span data-ttu-id="60180-449">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="60180-449">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="60180-450">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="60180-450">Remarks - foregroundColor</span></span>

<span data-ttu-id="60180-451">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="60180-451">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="60180-452">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="60180-452">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="60180-453">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="60180-453">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="60180-454">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="60180-454">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="60180-455">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="60180-455">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="60180-456">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="60180-456">The maximum value for a single byte is 255.</span></span>

## <a name="method-height"></a><span data-ttu-id="60180-457">メソッド height</span><span class="sxs-lookup"><span data-stu-id="60180-457">Method height</span></span>

<span data-ttu-id="60180-458">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-458">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="60180-459">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="60180-459">Parameters - height</span></span>

<span data-ttu-id="60180-460">値</span><span class="sxs-lookup"><span data-stu-id="60180-460">value</span></span>  

<!-- -->

<span data-ttu-id="60180-461">モード</span><span class="sxs-lookup"><span data-stu-id="60180-461">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="60180-462">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="60180-462">Return Value - height</span></span>

<span data-ttu-id="60180-463">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="60180-463">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="60180-464">備考 - height</span><span class="sxs-lookup"><span data-stu-id="60180-464">Remarks - height</span></span>

<span data-ttu-id="60180-465">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="60180-465">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="60180-466">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="60180-466">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="60180-467">モード。</span><span class="sxs-lookup"><span data-stu-id="60180-467">Mode.</span></span>            | <span data-ttu-id="60180-468">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="60180-468">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="60180-469">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="60180-469">-1 Exact.</span></span>        | <span data-ttu-id="60180-470">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="60180-470">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="60180-471">0 自動。</span><span class="sxs-lookup"><span data-stu-id="60180-471">0 Auto.</span></span>          | <span data-ttu-id="60180-472">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="60180-472">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="60180-473">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="60180-473">1 Column height.</span></span> | <span data-ttu-id="60180-474">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="60180-474">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="60180-475">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="60180-475">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="60180-476">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="60180-476">Method heightMode</span></span>

<span data-ttu-id="60180-477">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-477">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="60180-478">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="60180-478">Parameters - heightMode</span></span>

<span data-ttu-id="60180-479">値</span><span class="sxs-lookup"><span data-stu-id="60180-479">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="60180-480">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="60180-480">Return Value - heightMode</span></span>

<span data-ttu-id="60180-481">計算モード。</span><span class="sxs-lookup"><span data-stu-id="60180-481">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="60180-482">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="60180-482">Remarks - heightMode</span></span>

<span data-ttu-id="60180-483">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="60180-483">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="60180-484">モード。</span><span class="sxs-lookup"><span data-stu-id="60180-484">Mode.</span></span>          | <span data-ttu-id="60180-485">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="60180-485">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="60180-486">正確。</span><span class="sxs-lookup"><span data-stu-id="60180-486">Exact.</span></span>         | <span data-ttu-id="60180-487">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="60180-487">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="60180-488">自動。</span><span class="sxs-lookup"><span data-stu-id="60180-488">Auto.</span></span>          | <span data-ttu-id="60180-489">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="60180-489">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="60180-490">列の高さ</span><span class="sxs-lookup"><span data-stu-id="60180-490">Column height.</span></span> | <span data-ttu-id="60180-491">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="60180-491">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="60180-492">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="60180-492">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="60180-493">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="60180-493">Method heightValue</span></span>

<span data-ttu-id="60180-494">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-494">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="60180-495">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="60180-495">Parameters - heightValue</span></span>

<span data-ttu-id="60180-496">値</span><span class="sxs-lookup"><span data-stu-id="60180-496">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="60180-497">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="60180-497">Return Value - heightValue</span></span>

<span data-ttu-id="60180-498">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="60180-498">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="60180-499">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="60180-499">Remarks - heightValue</span></span>

<span data-ttu-id="60180-500">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="60180-500">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="60180-501">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="60180-501">Method helpText</span></span>

<span data-ttu-id="60180-502">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-502">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="60180-503">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="60180-503">Parameters - helpText</span></span>

<span data-ttu-id="60180-504">値</span><span class="sxs-lookup"><span data-stu-id="60180-504">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="60180-505">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="60180-505">Return Value - helpText</span></span>

<span data-ttu-id="60180-506">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="60180-506">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="60180-507">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="60180-507">Remarks - helpText</span></span>

<span data-ttu-id="60180-508">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-508">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="60180-509">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="60180-509">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="60180-510">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="60180-510">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="60180-511">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="60180-511">Parameters - hierarchyParent</span></span>

<span data-ttu-id="60180-512">値</span><span class="sxs-lookup"><span data-stu-id="60180-512">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="60180-513">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="60180-513">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="60180-514">メソッド id</span><span class="sxs-lookup"><span data-stu-id="60180-514">Method id</span></span>

<span data-ttu-id="60180-515">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="60180-515">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="60180-516">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="60180-516">Return Value - id</span></span>

<span data-ttu-id="60180-517">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="60180-517">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="60180-518">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="60180-518">Method isContainer</span></span>

<span data-ttu-id="60180-519">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="60180-519">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="60180-520">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="60180-520">Return Value - isContainer</span></span>

<span data-ttu-id="60180-521">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="60180-521">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="60180-522">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="60180-522">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="60180-523">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="60180-523">Parameters - italic</span></span>

<span data-ttu-id="60180-524">値</span><span class="sxs-lookup"><span data-stu-id="60180-524">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="60180-525">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="60180-525">Return Value - italic</span></span>

## <a name="method-left"></a><span data-ttu-id="60180-526">メソッド left</span><span class="sxs-lookup"><span data-stu-id="60180-526">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="60180-527">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="60180-527">Parameters - left</span></span>

<span data-ttu-id="60180-528">値</span><span class="sxs-lookup"><span data-stu-id="60180-528">value</span></span>  

<!-- -->

<span data-ttu-id="60180-529">モード</span><span class="sxs-lookup"><span data-stu-id="60180-529">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="60180-530">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="60180-530">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="60180-531">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="60180-531">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="60180-532">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="60180-532">Parameters - leftMode</span></span>

<span data-ttu-id="60180-533">値</span><span class="sxs-lookup"><span data-stu-id="60180-533">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="60180-534">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="60180-534">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="60180-535">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="60180-535">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="60180-536">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="60180-536">Parameters - leftValue</span></span>

<span data-ttu-id="60180-537">値</span><span class="sxs-lookup"><span data-stu-id="60180-537">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="60180-538">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="60180-538">Return Value - leftValue</span></span>

## <a name="method-name"></a><span data-ttu-id="60180-539">メソッド名</span><span class="sxs-lookup"><span data-stu-id="60180-539">Method name</span></span>

<span data-ttu-id="60180-540">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-540">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="60180-541">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="60180-541">Parameters - name</span></span>

<span data-ttu-id="60180-542">値</span><span class="sxs-lookup"><span data-stu-id="60180-542">value</span></span>  
<span data-ttu-id="60180-543">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="60180-543">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="60180-544">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="60180-544">Return Value - name</span></span>

<span data-ttu-id="60180-545">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="60180-545">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="60180-546">備考 - name</span><span class="sxs-lookup"><span data-stu-id="60180-546">Remarks - name</span></span>

<span data-ttu-id="60180-547">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="60180-547">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="60180-548">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="60180-548">It must start with a letter.</span></span>
-   <span data-ttu-id="60180-549">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="60180-549">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="60180-550">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="60180-550">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="60180-551">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="60180-551">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="60180-552">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="60180-552">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="60180-553">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="60180-553">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="60180-554">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="60180-554">Parameters - neededPermission</span></span>

<span data-ttu-id="60180-555">値</span><span class="sxs-lookup"><span data-stu-id="60180-555">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="60180-556">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="60180-556">Return Value - neededPermission</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="60180-557">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="60180-557">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="60180-558">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="60180-558">Parameters - securityKey</span></span>

<span data-ttu-id="60180-559">値</span><span class="sxs-lookup"><span data-stu-id="60180-559">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="60180-560">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="60180-560">Return Value - securityKey</span></span>

## <a name="method-skip"></a><span data-ttu-id="60180-561">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="60180-561">Method skip</span></span>

<span data-ttu-id="60180-562">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="60180-562">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="60180-563">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="60180-563">Parameters - skip</span></span>

<span data-ttu-id="60180-564">値</span><span class="sxs-lookup"><span data-stu-id="60180-564">value</span></span>  
<span data-ttu-id="60180-565">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="60180-565">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="60180-566">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="60180-566">Return Value - skip</span></span>

<span data-ttu-id="60180-567">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="60180-567">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-style"></a><span data-ttu-id="60180-568">メソッド style</span><span class="sxs-lookup"><span data-stu-id="60180-568">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="60180-569">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="60180-569">Parameters - style</span></span>

<span data-ttu-id="60180-570">値</span><span class="sxs-lookup"><span data-stu-id="60180-570">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="60180-571">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="60180-571">Return Value - style</span></span>

## <a name="method-text"></a><span data-ttu-id="60180-572">メソッド text</span><span class="sxs-lookup"><span data-stu-id="60180-572">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="60180-573">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="60180-573">Parameters - text</span></span>

<span data-ttu-id="60180-574">値</span><span class="sxs-lookup"><span data-stu-id="60180-574">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="60180-575">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="60180-575">Return Value - text</span></span>

## <a name="method-top"></a><span data-ttu-id="60180-576">メソッド top</span><span class="sxs-lookup"><span data-stu-id="60180-576">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="60180-577">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="60180-577">Parameters - top</span></span>

<span data-ttu-id="60180-578">値</span><span class="sxs-lookup"><span data-stu-id="60180-578">value</span></span>  

<!-- -->

<span data-ttu-id="60180-579">モード</span><span class="sxs-lookup"><span data-stu-id="60180-579">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="60180-580">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="60180-580">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="60180-581">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="60180-581">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="60180-582">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="60180-582">Parameters - topMode</span></span>

<span data-ttu-id="60180-583">値</span><span class="sxs-lookup"><span data-stu-id="60180-583">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="60180-584">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="60180-584">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="60180-585">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="60180-585">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="60180-586">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="60180-586">Parameters - topValue</span></span>

<span data-ttu-id="60180-587">値</span><span class="sxs-lookup"><span data-stu-id="60180-587">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="60180-588">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="60180-588">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="60180-589">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="60180-589">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="60180-590">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="60180-590">Parameters - type</span></span>

<span data-ttu-id="60180-591">値</span><span class="sxs-lookup"><span data-stu-id="60180-591">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="60180-592">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="60180-592">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="60180-593">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="60180-593">Method underline</span></span>

<span data-ttu-id="60180-594">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="60180-594">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="60180-595">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="60180-595">Parameters - underline</span></span>

<span data-ttu-id="60180-596">値</span><span class="sxs-lookup"><span data-stu-id="60180-596">value</span></span>  
<span data-ttu-id="60180-597">コントロールの underline プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="60180-597">The value to assign to the underline property of the control; optional.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="60180-598">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="60180-598">Return Value - underline</span></span>

<span data-ttu-id="60180-599">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="60180-599">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-userdata"></a><span data-ttu-id="60180-600">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="60180-600">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="60180-601">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="60180-601">Parameters - userData</span></span>

<span data-ttu-id="60180-602">値</span><span class="sxs-lookup"><span data-stu-id="60180-602">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="60180-603">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="60180-603">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="60180-604">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="60180-604">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="60180-605">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="60180-605">Parameters - userDataItem</span></span>

<span data-ttu-id="60180-606">値</span><span class="sxs-lookup"><span data-stu-id="60180-606">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="60180-607">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="60180-607">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="60180-608">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="60180-608">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="60180-609">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="60180-609">Parameters - userDataItems</span></span>

<span data-ttu-id="60180-610">値</span><span class="sxs-lookup"><span data-stu-id="60180-610">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="60180-611">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="60180-611">Return Value - userDataItems</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="60180-612">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="60180-612">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="60180-613">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="60180-613">Parameters - verticalSpacing</span></span>

<span data-ttu-id="60180-614">値</span><span class="sxs-lookup"><span data-stu-id="60180-614">value</span></span>  

<!-- -->

<span data-ttu-id="60180-615">モード</span><span class="sxs-lookup"><span data-stu-id="60180-615">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="60180-616">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="60180-616">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="60180-617">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="60180-617">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="60180-618">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="60180-618">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="60180-619">モード</span><span class="sxs-lookup"><span data-stu-id="60180-619">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="60180-620">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="60180-620">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="60180-621">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="60180-621">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="60180-622">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="60180-622">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="60180-623">値</span><span class="sxs-lookup"><span data-stu-id="60180-623">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="60180-624">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="60180-624">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="60180-625">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="60180-625">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="60180-626">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="60180-626">Parameters - visible</span></span>

<span data-ttu-id="60180-627">値</span><span class="sxs-lookup"><span data-stu-id="60180-627">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="60180-628">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="60180-628">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="60180-629">メソッド width</span><span class="sxs-lookup"><span data-stu-id="60180-629">Method width</span></span>

<span data-ttu-id="60180-630">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-630">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="60180-631">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="60180-631">Parameters - width</span></span>

<span data-ttu-id="60180-632">値</span><span class="sxs-lookup"><span data-stu-id="60180-632">value</span></span>  

<!-- -->

<span data-ttu-id="60180-633">モード</span><span class="sxs-lookup"><span data-stu-id="60180-633">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="60180-634">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="60180-634">Return Value - width</span></span>

<span data-ttu-id="60180-635">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="60180-635">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="60180-636">備考 - width</span><span class="sxs-lookup"><span data-stu-id="60180-636">Remarks - width</span></span>

<span data-ttu-id="60180-637">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="60180-637">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="60180-638">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="60180-638">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="60180-639">モード。</span><span class="sxs-lookup"><span data-stu-id="60180-639">Mode.</span></span>           | <span data-ttu-id="60180-640">幅計算。</span><span class="sxs-lookup"><span data-stu-id="60180-640">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="60180-641">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="60180-641">-1 Exact.</span></span>       | <span data-ttu-id="60180-642">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="60180-642">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="60180-643">0 自動。</span><span class="sxs-lookup"><span data-stu-id="60180-643">0 Auto.</span></span>         | <span data-ttu-id="60180-644">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="60180-644">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="60180-645">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="60180-645">1 Column width.</span></span> | <span data-ttu-id="60180-646">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="60180-646">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="60180-647">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="60180-647">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="60180-648">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="60180-648">Method widthMode</span></span>

<span data-ttu-id="60180-649">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-649">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="60180-650">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="60180-650">Parameters - widthMode</span></span>

<span data-ttu-id="60180-651">値</span><span class="sxs-lookup"><span data-stu-id="60180-651">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="60180-652">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="60180-652">Return Value - widthMode</span></span>

<span data-ttu-id="60180-653">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="60180-653">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="60180-654">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="60180-654">Remarks - widthMode</span></span>

<span data-ttu-id="60180-655">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="60180-655">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="60180-656">モード。</span><span class="sxs-lookup"><span data-stu-id="60180-656">Mode.</span></span>         | <span data-ttu-id="60180-657">幅計算。</span><span class="sxs-lookup"><span data-stu-id="60180-657">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="60180-658">正確。</span><span class="sxs-lookup"><span data-stu-id="60180-658">Exact.</span></span>        | <span data-ttu-id="60180-659">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="60180-659">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="60180-660">自動。</span><span class="sxs-lookup"><span data-stu-id="60180-660">Auto.</span></span>         | <span data-ttu-id="60180-661">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="60180-661">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="60180-662">列の幅。</span><span class="sxs-lookup"><span data-stu-id="60180-662">Column width.</span></span> | <span data-ttu-id="60180-663">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="60180-663">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="60180-664">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="60180-664">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="60180-665">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="60180-665">Method widthValue</span></span>

<span data-ttu-id="60180-666">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="60180-666">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="60180-667">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="60180-667">Parameters - widthValue</span></span>

<span data-ttu-id="60180-668">値</span><span class="sxs-lookup"><span data-stu-id="60180-668">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="60180-669">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="60180-669">Return Value - widthValue</span></span>

<span data-ttu-id="60180-670">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="60180-670">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="60180-671">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="60180-671">Remarks - widthValue</span></span>

<span data-ttu-id="60180-672">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="60180-672">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="60180-673">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="60180-673">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="60180-674">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="60180-674">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="60180-675">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="60180-675">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="60180-676">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="60180-676">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="60180-677">overrideObject</span><span class="sxs-lookup"><span data-stu-id="60180-677">overrideObject</span></span>  

