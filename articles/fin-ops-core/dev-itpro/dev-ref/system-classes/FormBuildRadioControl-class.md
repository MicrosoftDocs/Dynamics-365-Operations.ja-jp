---
title: FormBuildRadioControl クラス
description: このトピックでは、FormBuildRadioControl クラスについて説明します。
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
ms.openlocfilehash: 60a222351e8b1f8692094c822b1804615a9b57a3
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502646"
---
# <a name="class-formbuildradiocontrol"></a><span data-ttu-id="feee2-103">クラス FormBuildRadioControl</span><span class="sxs-lookup"><span data-stu-id="feee2-103">Class FormBuildRadioControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildRadioControl extends FormBuildControl
```

<span data-ttu-id="feee2-104">FormBuildRadioControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="feee2-104">The FormBuildRadioControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="feee2-105">備考</span><span class="sxs-lookup"><span data-stu-id="feee2-105">Remarks</span></span>

<span data-ttu-id="feee2-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="feee2-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="feee2-107">例</span><span class="sxs-lookup"><span data-stu-id="feee2-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="feee2-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="feee2-108">Methods</span></span>

| <span data-ttu-id="feee2-109">方法</span><span class="sxs-lookup"><span data-stu-id="feee2-109">Method</span></span>                                                                                                      | <span data-ttu-id="feee2-110">説明</span><span class="sxs-lookup"><span data-stu-id="feee2-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feee2-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="feee2-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-112">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="feee2-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="feee2-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-114">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="feee2-115">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-115">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="feee2-116">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-116">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="feee2-117">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-117">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="feee2-118">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-118">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="feee2-119">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-119">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="feee2-120">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-120">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="feee2-121">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-121">Determines whether the control background can be transparent.</span></span>                                                                           |
| <span data-ttu-id="feee2-122">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-122">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="feee2-123">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-123">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                             |
| <span data-ttu-id="feee2-124">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="feee2-124">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="feee2-125">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="feee2-125">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                         |                                                                                                                                         |
| <span data-ttu-id="feee2-126">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-126">public int bottomMarginValue(\[int value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="feee2-127">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-127">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="feee2-128">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-128">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="feee2-129">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-129">Gets or set the caption of the control.</span></span>                                                                                                 |
| <span data-ttu-id="feee2-130">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-130">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="feee2-131">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-131">Gets or sets the character set of the font.</span></span>                                                                                             |
| <span data-ttu-id="feee2-132">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-132">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="feee2-133">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-133">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="feee2-134">public int columns(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-134">public int columns(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="feee2-135">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-135">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="feee2-136">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-136">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="feee2-137">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="feee2-137">public int containerId()</span></span>                                                                                    | <span data-ttu-id="feee2-138">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="feee2-138">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="feee2-139">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-139">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="feee2-140">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-140">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                         |
| <span data-ttu-id="feee2-141">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-141">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="feee2-142">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-142">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="feee2-143">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-143">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="feee2-144">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-144">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="feee2-145">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-145">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                |
| <span data-ttu-id="feee2-146">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="feee2-146">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                         |
| <span data-ttu-id="feee2-147">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="feee2-147">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                         |
| <span data-ttu-id="feee2-148">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-148">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="feee2-149">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-149">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="feee2-150">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-150">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="feee2-151">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-151">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="feee2-152">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-152">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="feee2-153">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-153">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="feee2-154">public EnumId enumType(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-154">public EnumId enumType(\[EnumId value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="feee2-155">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-155">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                         |
| <span data-ttu-id="feee2-156">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-156">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="feee2-157">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-157">Gets or sets the name of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="feee2-158">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-158">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="feee2-159">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-159">Gets or sets the size of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="feee2-160">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-160">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="feee2-161">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-161">Gets or sets the text color for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="feee2-162">public int framePosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-162">public int framePosition(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="feee2-163">public int frameType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-163">public int frameType(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="feee2-164">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="feee2-164">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="feee2-165">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-165">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="feee2-166">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-166">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="feee2-167">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-167">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="feee2-168">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-168">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="feee2-169">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-169">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="feee2-170">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-170">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="feee2-171">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-171">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="feee2-172">public boolean hideFirstEntry(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-172">public boolean hideFirstEntry(\[boolean value\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="feee2-173">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-173">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="feee2-174">public int id()</span><span class="sxs-lookup"><span data-stu-id="feee2-174">public int id()</span></span>                                                                                             | <span data-ttu-id="feee2-175">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="feee2-175">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="feee2-176">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="feee2-176">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="feee2-177">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="feee2-177">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="feee2-178">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-178">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="feee2-179">public int item(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-179">public int item(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="feee2-180">public int items(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-180">public int items(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="feee2-181">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="feee2-181">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="feee2-182">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="feee2-182">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                     |                                                                                                                                         |
| <span data-ttu-id="feee2-183">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="feee2-183">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                           |                                                                                                                                         |
| <span data-ttu-id="feee2-184">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-184">public int leftMarginValue(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="feee2-185">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-185">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="feee2-186">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-186">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="feee2-187">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-187">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="feee2-188">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-188">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="feee2-189">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-189">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="feee2-190">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="feee2-190">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                         |
| <span data-ttu-id="feee2-191">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="feee2-191">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                         |
| <span data-ttu-id="feee2-192">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-192">public int rightMarginValue(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="feee2-193">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-193">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="feee2-194">public int selection(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-194">public int selection(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="feee2-195">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-195">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="feee2-196">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="feee2-196">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="feee2-197">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-197">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="feee2-198">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="feee2-198">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="feee2-199">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="feee2-199">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="feee2-200">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="feee2-200">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="feee2-201">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-201">public int topMarginValue(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="feee2-202">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-202">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="feee2-203">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-203">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="feee2-204">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-204">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="feee2-205">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-205">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="feee2-206">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="feee2-206">Sets or returns the underline property for the text in the control.</span></span>                                                                     |
| <span data-ttu-id="feee2-207">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-207">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="feee2-208">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-208">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="feee2-209">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-209">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="feee2-210">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="feee2-210">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="feee2-211">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="feee2-211">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="feee2-212">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-212">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="feee2-213">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-213">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="feee2-214">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-214">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="feee2-215">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="feee2-215">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="feee2-216">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-216">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="feee2-217">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-217">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="feee2-218">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-218">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="feee2-219">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="feee2-219">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="feee2-220">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-220">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="feee2-221">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="feee2-221">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="feee2-222">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="feee2-222">Method alignControl</span></span>

<span data-ttu-id="feee2-223">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-223">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="feee2-224">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="feee2-224">Parameters - alignControl</span></span>

<span data-ttu-id="feee2-225">値</span><span class="sxs-lookup"><span data-stu-id="feee2-225">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="feee2-226">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="feee2-226">Return Value - alignControl</span></span>

<span data-ttu-id="feee2-227">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="feee2-227">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="feee2-228">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="feee2-228">Remarks - alignControl</span></span>

<span data-ttu-id="feee2-229">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="feee2-229">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="feee2-230">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="feee2-230">Method allowEdit</span></span>

<span data-ttu-id="feee2-231">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-231">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="feee2-232">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="feee2-232">Parameters - allowEdit</span></span>

<span data-ttu-id="feee2-233">値</span><span class="sxs-lookup"><span data-stu-id="feee2-233">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="feee2-234">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="feee2-234">Return Value - allowEdit</span></span>

<span data-ttu-id="feee2-235">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="feee2-235">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="feee2-236">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="feee2-236">Remarks - allowEdit</span></span>

<span data-ttu-id="feee2-237">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="feee2-237">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="feee2-238">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="feee2-238">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="feee2-239">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="feee2-239">Parameters - arrayIndex</span></span>

<span data-ttu-id="feee2-240">値</span><span class="sxs-lookup"><span data-stu-id="feee2-240">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="feee2-241">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="feee2-241">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="feee2-242">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="feee2-242">Method autoDeclaration</span></span>

<span data-ttu-id="feee2-243">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-243">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="feee2-244">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="feee2-244">Parameters - autoDeclaration</span></span>

<span data-ttu-id="feee2-245">値</span><span class="sxs-lookup"><span data-stu-id="feee2-245">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="feee2-246">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="feee2-246">Return Value - autoDeclaration</span></span>

<span data-ttu-id="feee2-247">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="feee2-247">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="feee2-248">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="feee2-248">Remarks - autoDeclaration</span></span>

<span data-ttu-id="feee2-249">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="feee2-249">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="feee2-250">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="feee2-250">Method backgroundColor</span></span>

<span data-ttu-id="feee2-251">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-251">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="feee2-252">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="feee2-252">Parameters - backgroundColor</span></span>

<span data-ttu-id="feee2-253">値</span><span class="sxs-lookup"><span data-stu-id="feee2-253">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="feee2-254">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="feee2-254">Return Value - backgroundColor</span></span>

<span data-ttu-id="feee2-255">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="feee2-255">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="feee2-256">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="feee2-256">Remarks - backgroundColor</span></span>

<span data-ttu-id="feee2-257">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="feee2-257">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="feee2-258">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="feee2-258">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="feee2-259">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="feee2-259">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="feee2-260">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="feee2-260">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="feee2-261">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="feee2-261">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="feee2-262">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="feee2-262">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="feee2-263">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="feee2-263">Method backStyle</span></span>

<span data-ttu-id="feee2-264">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-264">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="feee2-265">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="feee2-265">Parameters - backStyle</span></span>

<span data-ttu-id="feee2-266">値</span><span class="sxs-lookup"><span data-stu-id="feee2-266">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="feee2-267">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="feee2-267">Return Value - backStyle</span></span>

<span data-ttu-id="feee2-268">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="feee2-268">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="feee2-269">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="feee2-269">Method bold</span></span>

<span data-ttu-id="feee2-270">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-270">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="feee2-271">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="feee2-271">Parameters - bold</span></span>

<span data-ttu-id="feee2-272">値</span><span class="sxs-lookup"><span data-stu-id="feee2-272">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="feee2-273">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="feee2-273">Return Value - bold</span></span>

<span data-ttu-id="feee2-274">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="feee2-274">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="feee2-275">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="feee2-275">Remarks - bold</span></span>

<span data-ttu-id="feee2-276">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="feee2-276">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="feee2-277">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="feee2-277">0 Use the default font weight.</span></span>
-   <span data-ttu-id="feee2-278">1 シン。</span><span class="sxs-lookup"><span data-stu-id="feee2-278">1 Thin.</span></span>
-   <span data-ttu-id="feee2-279">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="feee2-279">2 Extra-light.</span></span>
-   <span data-ttu-id="feee2-280">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="feee2-280">3 Light.</span></span>
-   <span data-ttu-id="feee2-281">4 標準。</span><span class="sxs-lookup"><span data-stu-id="feee2-281">4 Normal.</span></span>
-   <span data-ttu-id="feee2-282">5 中。</span><span class="sxs-lookup"><span data-stu-id="feee2-282">5 Medium.</span></span>
-   <span data-ttu-id="feee2-283">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="feee2-283">6 Semibold.</span></span>
-   <span data-ttu-id="feee2-284">7 太字。</span><span class="sxs-lookup"><span data-stu-id="feee2-284">7 Bold.</span></span>
-   <span data-ttu-id="feee2-285">8 極太。</span><span class="sxs-lookup"><span data-stu-id="feee2-285">8 Extra-bold.</span></span>
-   <span data-ttu-id="feee2-286">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="feee2-286">9 Heavy.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="feee2-287">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="feee2-287">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="feee2-288">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="feee2-288">Parameters - bottomMargin</span></span>

<span data-ttu-id="feee2-289">値</span><span class="sxs-lookup"><span data-stu-id="feee2-289">value</span></span>  

<!-- -->

<span data-ttu-id="feee2-290">モード</span><span class="sxs-lookup"><span data-stu-id="feee2-290">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="feee2-291">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="feee2-291">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="feee2-292">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="feee2-292">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="feee2-293">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="feee2-293">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="feee2-294">モード</span><span class="sxs-lookup"><span data-stu-id="feee2-294">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="feee2-295">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="feee2-295">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="feee2-296">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="feee2-296">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="feee2-297">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="feee2-297">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="feee2-298">値</span><span class="sxs-lookup"><span data-stu-id="feee2-298">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="feee2-299">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="feee2-299">Return Value - bottomMarginValue</span></span>

## <a name="method-cachedatamethod"></a><span data-ttu-id="feee2-300">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="feee2-300">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="feee2-301">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="feee2-301">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="feee2-302">値</span><span class="sxs-lookup"><span data-stu-id="feee2-302">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="feee2-303">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="feee2-303">Return Value - cacheDataMethod</span></span>

## <a name="method-caption"></a><span data-ttu-id="feee2-304">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="feee2-304">Method caption</span></span>

<span data-ttu-id="feee2-305">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-305">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="feee2-306">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="feee2-306">Parameters - caption</span></span>

<span data-ttu-id="feee2-307">値</span><span class="sxs-lookup"><span data-stu-id="feee2-307">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="feee2-308">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="feee2-308">Return Value - caption</span></span>

<span data-ttu-id="feee2-309">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="feee2-309">The string that is used as the caption of the control.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="feee2-310">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="feee2-310">Method characterSet</span></span>

<span data-ttu-id="feee2-311">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-311">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="feee2-312">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="feee2-312">Parameters - characterSet</span></span>

<span data-ttu-id="feee2-313">値</span><span class="sxs-lookup"><span data-stu-id="feee2-313">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="feee2-314">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="feee2-314">Return Value - characterSet</span></span>

<span data-ttu-id="feee2-315">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="feee2-315">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="feee2-316">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="feee2-316">Remarks - characterSet</span></span>

<span data-ttu-id="feee2-317">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="feee2-317">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="feee2-318">値です。</span><span class="sxs-lookup"><span data-stu-id="feee2-318">Value.</span></span> | <span data-ttu-id="feee2-319">説明。</span><span class="sxs-lookup"><span data-stu-id="feee2-319">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="feee2-320">0</span><span class="sxs-lookup"><span data-stu-id="feee2-320">0</span></span>      | <span data-ttu-id="feee2-321">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="feee2-321">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="feee2-322">1</span><span class="sxs-lookup"><span data-stu-id="feee2-322">1</span></span>      | <span data-ttu-id="feee2-323">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="feee2-323">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="feee2-324">2</span><span class="sxs-lookup"><span data-stu-id="feee2-324">2</span></span>      | <span data-ttu-id="feee2-325">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="feee2-325">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="feee2-326">77</span><span class="sxs-lookup"><span data-stu-id="feee2-326">77</span></span>     | <span data-ttu-id="feee2-327">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="feee2-327">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="feee2-328">128</span><span class="sxs-lookup"><span data-stu-id="feee2-328">128</span></span>    | <span data-ttu-id="feee2-329">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="feee2-329">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="feee2-330">129</span><span class="sxs-lookup"><span data-stu-id="feee2-330">129</span></span>    | <span data-ttu-id="feee2-331">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="feee2-331">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="feee2-332">134</span><span class="sxs-lookup"><span data-stu-id="feee2-332">134</span></span>    | <span data-ttu-id="feee2-333">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="feee2-333">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="feee2-334">136</span><span class="sxs-lookup"><span data-stu-id="feee2-334">136</span></span>    | <span data-ttu-id="feee2-335">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="feee2-335">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="feee2-336">161</span><span class="sxs-lookup"><span data-stu-id="feee2-336">161</span></span>    | <span data-ttu-id="feee2-337">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="feee2-337">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="feee2-338">162</span><span class="sxs-lookup"><span data-stu-id="feee2-338">162</span></span>    | <span data-ttu-id="feee2-339">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="feee2-339">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="feee2-340">163</span><span class="sxs-lookup"><span data-stu-id="feee2-340">163</span></span>    | <span data-ttu-id="feee2-341">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="feee2-341">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="feee2-342">186</span><span class="sxs-lookup"><span data-stu-id="feee2-342">186</span></span>    | <span data-ttu-id="feee2-343">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="feee2-343">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="feee2-344">204</span><span class="sxs-lookup"><span data-stu-id="feee2-344">204</span></span>    | <span data-ttu-id="feee2-345">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="feee2-345">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="feee2-346">238</span><span class="sxs-lookup"><span data-stu-id="feee2-346">238</span></span>    | <span data-ttu-id="feee2-347">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="feee2-347">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="feee2-348">255</span><span class="sxs-lookup"><span data-stu-id="feee2-348">255</span></span>    | <span data-ttu-id="feee2-349">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="feee2-349">OEM\_CHARSET</span></span>         |

<span data-ttu-id="feee2-350">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="feee2-350">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="feee2-351">値です。</span><span class="sxs-lookup"><span data-stu-id="feee2-351">Value.</span></span> | <span data-ttu-id="feee2-352">説明。</span><span class="sxs-lookup"><span data-stu-id="feee2-352">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="feee2-353">130</span><span class="sxs-lookup"><span data-stu-id="feee2-353">130</span></span>    | <span data-ttu-id="feee2-354">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="feee2-354">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="feee2-355">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="feee2-355">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="feee2-356">値です。</span><span class="sxs-lookup"><span data-stu-id="feee2-356">Value.</span></span> | <span data-ttu-id="feee2-357">説明。</span><span class="sxs-lookup"><span data-stu-id="feee2-357">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="feee2-358">177</span><span class="sxs-lookup"><span data-stu-id="feee2-358">177</span></span>    | <span data-ttu-id="feee2-359">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="feee2-359">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="feee2-360">178</span><span class="sxs-lookup"><span data-stu-id="feee2-360">178</span></span>    | <span data-ttu-id="feee2-361">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="feee2-361">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="feee2-362">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="feee2-362">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="feee2-363">値です。</span><span class="sxs-lookup"><span data-stu-id="feee2-363">Value.</span></span> | <span data-ttu-id="feee2-364">説明。</span><span class="sxs-lookup"><span data-stu-id="feee2-364">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="feee2-365">222</span><span class="sxs-lookup"><span data-stu-id="feee2-365">222</span></span>    | <span data-ttu-id="feee2-366">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="feee2-366">THAI\_CHARSET</span></span> |

<span data-ttu-id="feee2-367">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="feee2-367">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="feee2-368">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="feee2-368">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="feee2-369">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="feee2-369">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="feee2-370">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="feee2-370">Method colorScheme</span></span>

<span data-ttu-id="feee2-371">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-371">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="feee2-372">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="feee2-372">Parameters - colorScheme</span></span>

<span data-ttu-id="feee2-373">値</span><span class="sxs-lookup"><span data-stu-id="feee2-373">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="feee2-374">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="feee2-374">Return Value - colorScheme</span></span>

<span data-ttu-id="feee2-375">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="feee2-375">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="feee2-376">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="feee2-376">Remarks - colorScheme</span></span>

<span data-ttu-id="feee2-377">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="feee2-377">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="feee2-378">値です。</span><span class="sxs-lookup"><span data-stu-id="feee2-378">Value.</span></span> | <span data-ttu-id="feee2-379">スタイル。</span><span class="sxs-lookup"><span data-stu-id="feee2-379">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="feee2-380">0</span><span class="sxs-lookup"><span data-stu-id="feee2-380">0</span></span>      | <span data-ttu-id="feee2-381">既定。</span><span class="sxs-lookup"><span data-stu-id="feee2-381">Default.</span></span>                      |
| <span data-ttu-id="feee2-382">1</span><span class="sxs-lookup"><span data-stu-id="feee2-382">1</span></span>      | <span data-ttu-id="feee2-383">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="feee2-383">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="feee2-384">2</span><span class="sxs-lookup"><span data-stu-id="feee2-384">2</span></span>      | <span data-ttu-id="feee2-385">真の配色。</span><span class="sxs-lookup"><span data-stu-id="feee2-385">The true-color scheme.</span></span>        |

## <a name="method-columns"></a><span data-ttu-id="feee2-386">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="feee2-386">Method columns</span></span>

```xpp
public int columns([int value])
```

### <a name="parameters---columns"></a><span data-ttu-id="feee2-387">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="feee2-387">Parameters - columns</span></span>

<span data-ttu-id="feee2-388">値</span><span class="sxs-lookup"><span data-stu-id="feee2-388">value</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="feee2-389">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="feee2-389">Return Value - columns</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="feee2-390">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="feee2-390">Method configurationKey</span></span>

<span data-ttu-id="feee2-391">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-391">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="feee2-392">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="feee2-392">Parameters - configurationKey</span></span>

<span data-ttu-id="feee2-393">値</span><span class="sxs-lookup"><span data-stu-id="feee2-393">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="feee2-394">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="feee2-394">Return Value - configurationKey</span></span>

<span data-ttu-id="feee2-395">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="feee2-395">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="feee2-396">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="feee2-396">Remarks - configurationKey</span></span>

<span data-ttu-id="feee2-397">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="feee2-397">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="feee2-398">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="feee2-398">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="feee2-399">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="feee2-399">Method containerId</span></span>

<span data-ttu-id="feee2-400">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="feee2-400">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="feee2-401">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="feee2-401">Return Value - containerId</span></span>

<span data-ttu-id="feee2-402">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="feee2-402">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="feee2-403">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="feee2-403">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="feee2-404">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="feee2-404">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="feee2-405">値</span><span class="sxs-lookup"><span data-stu-id="feee2-405">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="feee2-406">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="feee2-406">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="feee2-407">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="feee2-407">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="feee2-408">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="feee2-408">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="feee2-409">値</span><span class="sxs-lookup"><span data-stu-id="feee2-409">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="feee2-410">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="feee2-410">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="feee2-411">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="feee2-411">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="feee2-412">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="feee2-412">Parameters - dataField</span></span>

<span data-ttu-id="feee2-413">値</span><span class="sxs-lookup"><span data-stu-id="feee2-413">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="feee2-414">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="feee2-414">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="feee2-415">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="feee2-415">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="feee2-416">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="feee2-416">Parameters - dataMethod</span></span>

<span data-ttu-id="feee2-417">値</span><span class="sxs-lookup"><span data-stu-id="feee2-417">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="feee2-418">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="feee2-418">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="feee2-419">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="feee2-419">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="feee2-420">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="feee2-420">Parameters - dataRelationPath</span></span>

<span data-ttu-id="feee2-421">値</span><span class="sxs-lookup"><span data-stu-id="feee2-421">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="feee2-422">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="feee2-422">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="feee2-423">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="feee2-423">Method dataSource</span></span>

<span data-ttu-id="feee2-424">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-424">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="feee2-425">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="feee2-425">Parameters - dataSource</span></span>

<span data-ttu-id="feee2-426">値</span><span class="sxs-lookup"><span data-stu-id="feee2-426">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="feee2-427">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="feee2-427">Return Value - dataSource</span></span>

<span data-ttu-id="feee2-428">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="feee2-428">The identifier of the data source that will be used.</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="feee2-429">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="feee2-429">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="feee2-430">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="feee2-430">Parameters - displayLength</span></span>

<span data-ttu-id="feee2-431">値</span><span class="sxs-lookup"><span data-stu-id="feee2-431">value</span></span>  

<!-- -->

<span data-ttu-id="feee2-432">モード</span><span class="sxs-lookup"><span data-stu-id="feee2-432">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="feee2-433">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="feee2-433">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="feee2-434">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="feee2-434">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="feee2-435">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="feee2-435">Parameters - displayLengthMode</span></span>

<span data-ttu-id="feee2-436">モード</span><span class="sxs-lookup"><span data-stu-id="feee2-436">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="feee2-437">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="feee2-437">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="feee2-438">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="feee2-438">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="feee2-439">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="feee2-439">Parameters - displayLengthValue</span></span>

<span data-ttu-id="feee2-440">値</span><span class="sxs-lookup"><span data-stu-id="feee2-440">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="feee2-441">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="feee2-441">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="feee2-442">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="feee2-442">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="feee2-443">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="feee2-443">Parameters - displayTarget</span></span>

<span data-ttu-id="feee2-444">値</span><span class="sxs-lookup"><span data-stu-id="feee2-444">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="feee2-445">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="feee2-445">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="feee2-446">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="feee2-446">Method dragDrop</span></span>

<span data-ttu-id="feee2-447">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-447">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="feee2-448">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="feee2-448">Parameters - dragDrop</span></span>

<span data-ttu-id="feee2-449">値</span><span class="sxs-lookup"><span data-stu-id="feee2-449">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="feee2-450">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="feee2-450">Return Value - dragDrop</span></span>

<span data-ttu-id="feee2-451">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="feee2-451">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="feee2-452">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="feee2-452">Method enabled</span></span>

<span data-ttu-id="feee2-453">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-453">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="feee2-454">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="feee2-454">Parameters - enabled</span></span>

<span data-ttu-id="feee2-455">値</span><span class="sxs-lookup"><span data-stu-id="feee2-455">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="feee2-456">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="feee2-456">Return Value - enabled</span></span>

<span data-ttu-id="feee2-457">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="feee2-457">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="feee2-458">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="feee2-458">Remarks - enabled</span></span>

<span data-ttu-id="feee2-459">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="feee2-459">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="feee2-460">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="feee2-460">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="feee2-461">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="feee2-461">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-enumtype"></a><span data-ttu-id="feee2-462">メソッド enumType</span><span class="sxs-lookup"><span data-stu-id="feee2-462">Method enumType</span></span>

```xpp
public EnumId enumType([EnumId value])
```

### <a name="parameters---enumtype"></a><span data-ttu-id="feee2-463">パラメーター - enumType</span><span class="sxs-lookup"><span data-stu-id="feee2-463">Parameters - enumType</span></span>

<span data-ttu-id="feee2-464">値</span><span class="sxs-lookup"><span data-stu-id="feee2-464">value</span></span>  

### <a name="return-value---enumtype"></a><span data-ttu-id="feee2-465">戻り値 - enumType</span><span class="sxs-lookup"><span data-stu-id="feee2-465">Return Value - enumType</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="feee2-466">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="feee2-466">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="feee2-467">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="feee2-467">Parameters - extendedDataType</span></span>

<span data-ttu-id="feee2-468">値</span><span class="sxs-lookup"><span data-stu-id="feee2-468">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="feee2-469">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="feee2-469">Return Value - extendedDataType</span></span>

## <a name="method-font"></a><span data-ttu-id="feee2-470">メソッド font</span><span class="sxs-lookup"><span data-stu-id="feee2-470">Method font</span></span>

<span data-ttu-id="feee2-471">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-471">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="feee2-472">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="feee2-472">Parameters - font</span></span>

<span data-ttu-id="feee2-473">値</span><span class="sxs-lookup"><span data-stu-id="feee2-473">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="feee2-474">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="feee2-474">Return Value - font</span></span>

<span data-ttu-id="feee2-475">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="feee2-475">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="feee2-476">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="feee2-476">Method fontSize</span></span>

<span data-ttu-id="feee2-477">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-477">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="feee2-478">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="feee2-478">Parameters - fontSize</span></span>

<span data-ttu-id="feee2-479">値</span><span class="sxs-lookup"><span data-stu-id="feee2-479">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="feee2-480">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="feee2-480">Return Value - fontSize</span></span>

<span data-ttu-id="feee2-481">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="feee2-481">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="feee2-482">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="feee2-482">Method foregroundColor</span></span>

<span data-ttu-id="feee2-483">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-483">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="feee2-484">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="feee2-484">Parameters - foregroundColor</span></span>

<span data-ttu-id="feee2-485">値</span><span class="sxs-lookup"><span data-stu-id="feee2-485">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="feee2-486">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="feee2-486">Return Value - foregroundColor</span></span>

<span data-ttu-id="feee2-487">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="feee2-487">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="feee2-488">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="feee2-488">Remarks - foregroundColor</span></span>

<span data-ttu-id="feee2-489">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="feee2-489">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="feee2-490">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="feee2-490">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="feee2-491">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="feee2-491">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="feee2-492">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="feee2-492">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="feee2-493">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="feee2-493">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="feee2-494">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="feee2-494">The maximum value for a single byte is 255.</span></span>

## <a name="method-frameposition"></a><span data-ttu-id="feee2-495">メソッド framePosition</span><span class="sxs-lookup"><span data-stu-id="feee2-495">Method framePosition</span></span>

```xpp
public int framePosition([int value])
```

### <a name="parameters---frameposition"></a><span data-ttu-id="feee2-496">パラメーター - framePosition</span><span class="sxs-lookup"><span data-stu-id="feee2-496">Parameters - framePosition</span></span>

<span data-ttu-id="feee2-497">値</span><span class="sxs-lookup"><span data-stu-id="feee2-497">value</span></span>  

### <a name="return-value---frameposition"></a><span data-ttu-id="feee2-498">戻り値 - framePosition</span><span class="sxs-lookup"><span data-stu-id="feee2-498">Return Value - framePosition</span></span>

## <a name="method-frametype"></a><span data-ttu-id="feee2-499">メソッド frameType</span><span class="sxs-lookup"><span data-stu-id="feee2-499">Method frameType</span></span>

```xpp
public int frameType([int value])
```

### <a name="parameters---frametype"></a><span data-ttu-id="feee2-500">パラメーター - frameType</span><span class="sxs-lookup"><span data-stu-id="feee2-500">Parameters - frameType</span></span>

<span data-ttu-id="feee2-501">値</span><span class="sxs-lookup"><span data-stu-id="feee2-501">value</span></span>  

### <a name="return-value---frametype"></a><span data-ttu-id="feee2-502">戻り値 - frameType</span><span class="sxs-lookup"><span data-stu-id="feee2-502">Return Value - frameType</span></span>

## <a name="method-height"></a><span data-ttu-id="feee2-503">メソッド height</span><span class="sxs-lookup"><span data-stu-id="feee2-503">Method height</span></span>

<span data-ttu-id="feee2-504">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-504">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="feee2-505">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="feee2-505">Parameters - height</span></span>

<span data-ttu-id="feee2-506">値</span><span class="sxs-lookup"><span data-stu-id="feee2-506">value</span></span>  

<!-- -->

<span data-ttu-id="feee2-507">モード</span><span class="sxs-lookup"><span data-stu-id="feee2-507">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="feee2-508">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="feee2-508">Return Value - height</span></span>

<span data-ttu-id="feee2-509">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="feee2-509">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="feee2-510">備考 - height</span><span class="sxs-lookup"><span data-stu-id="feee2-510">Remarks - height</span></span>

<span data-ttu-id="feee2-511">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="feee2-511">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="feee2-512">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="feee2-512">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="feee2-513">モード。</span><span class="sxs-lookup"><span data-stu-id="feee2-513">Mode.</span></span>            | <span data-ttu-id="feee2-514">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="feee2-514">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="feee2-515">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="feee2-515">-1 Exact.</span></span>        | <span data-ttu-id="feee2-516">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="feee2-516">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="feee2-517">0 自動。</span><span class="sxs-lookup"><span data-stu-id="feee2-517">0 Auto.</span></span>          | <span data-ttu-id="feee2-518">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="feee2-518">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="feee2-519">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="feee2-519">1 Column height.</span></span> | <span data-ttu-id="feee2-520">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="feee2-520">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="feee2-521">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="feee2-521">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="feee2-522">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="feee2-522">Method heightMode</span></span>

<span data-ttu-id="feee2-523">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-523">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="feee2-524">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="feee2-524">Parameters - heightMode</span></span>

<span data-ttu-id="feee2-525">値</span><span class="sxs-lookup"><span data-stu-id="feee2-525">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="feee2-526">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="feee2-526">Return Value - heightMode</span></span>

<span data-ttu-id="feee2-527">計算モード。</span><span class="sxs-lookup"><span data-stu-id="feee2-527">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="feee2-528">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="feee2-528">Remarks - heightMode</span></span>

<span data-ttu-id="feee2-529">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="feee2-529">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="feee2-530">モード。</span><span class="sxs-lookup"><span data-stu-id="feee2-530">Mode.</span></span>          | <span data-ttu-id="feee2-531">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="feee2-531">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="feee2-532">正確。</span><span class="sxs-lookup"><span data-stu-id="feee2-532">Exact.</span></span>         | <span data-ttu-id="feee2-533">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="feee2-533">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="feee2-534">自動。</span><span class="sxs-lookup"><span data-stu-id="feee2-534">Auto.</span></span>          | <span data-ttu-id="feee2-535">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="feee2-535">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="feee2-536">列の高さ</span><span class="sxs-lookup"><span data-stu-id="feee2-536">Column height.</span></span> | <span data-ttu-id="feee2-537">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="feee2-537">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="feee2-538">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="feee2-538">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="feee2-539">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="feee2-539">Method heightValue</span></span>

<span data-ttu-id="feee2-540">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-540">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="feee2-541">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="feee2-541">Parameters - heightValue</span></span>

<span data-ttu-id="feee2-542">値</span><span class="sxs-lookup"><span data-stu-id="feee2-542">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="feee2-543">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="feee2-543">Return Value - heightValue</span></span>

<span data-ttu-id="feee2-544">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="feee2-544">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="feee2-545">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="feee2-545">Remarks - heightValue</span></span>

<span data-ttu-id="feee2-546">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="feee2-546">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="feee2-547">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="feee2-547">Method helpText</span></span>

<span data-ttu-id="feee2-548">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-548">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="feee2-549">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="feee2-549">Parameters - helpText</span></span>

<span data-ttu-id="feee2-550">値</span><span class="sxs-lookup"><span data-stu-id="feee2-550">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="feee2-551">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="feee2-551">Return Value - helpText</span></span>

<span data-ttu-id="feee2-552">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="feee2-552">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="feee2-553">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="feee2-553">Remarks - helpText</span></span>

<span data-ttu-id="feee2-554">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-554">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="feee2-555">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="feee2-555">The help text must not exceed 250 characters.</span></span>

## <a name="method-hidefirstentry"></a><span data-ttu-id="feee2-556">メソッド hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="feee2-556">Method hideFirstEntry</span></span>

```xpp
public boolean hideFirstEntry([boolean value])
```

### <a name="parameters---hidefirstentry"></a><span data-ttu-id="feee2-557">パラメーター - hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="feee2-557">Parameters - hideFirstEntry</span></span>

<span data-ttu-id="feee2-558">値</span><span class="sxs-lookup"><span data-stu-id="feee2-558">value</span></span>  

### <a name="return-value---hidefirstentry"></a><span data-ttu-id="feee2-559">戻り値 - hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="feee2-559">Return Value - hideFirstEntry</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="feee2-560">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="feee2-560">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="feee2-561">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="feee2-561">Parameters - hierarchyParent</span></span>

<span data-ttu-id="feee2-562">値</span><span class="sxs-lookup"><span data-stu-id="feee2-562">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="feee2-563">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="feee2-563">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="feee2-564">メソッド id</span><span class="sxs-lookup"><span data-stu-id="feee2-564">Method id</span></span>

<span data-ttu-id="feee2-565">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="feee2-565">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="feee2-566">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="feee2-566">Return Value - id</span></span>

<span data-ttu-id="feee2-567">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="feee2-567">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="feee2-568">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="feee2-568">Method isContainer</span></span>

<span data-ttu-id="feee2-569">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="feee2-569">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="feee2-570">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="feee2-570">Return Value - isContainer</span></span>

<span data-ttu-id="feee2-571">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="feee2-571">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="feee2-572">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="feee2-572">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="feee2-573">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="feee2-573">Parameters - italic</span></span>

<span data-ttu-id="feee2-574">値</span><span class="sxs-lookup"><span data-stu-id="feee2-574">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="feee2-575">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="feee2-575">Return Value - italic</span></span>

## <a name="method-item"></a><span data-ttu-id="feee2-576">メソッド item</span><span class="sxs-lookup"><span data-stu-id="feee2-576">Method item</span></span>

```xpp
public int item([int value])
```

### <a name="parameters---item"></a><span data-ttu-id="feee2-577">パラメーター - item</span><span class="sxs-lookup"><span data-stu-id="feee2-577">Parameters - item</span></span>

<span data-ttu-id="feee2-578">値</span><span class="sxs-lookup"><span data-stu-id="feee2-578">value</span></span>  

### <a name="return-value---item"></a><span data-ttu-id="feee2-579">戻り値 - item</span><span class="sxs-lookup"><span data-stu-id="feee2-579">Return Value - item</span></span>

## <a name="method-items"></a><span data-ttu-id="feee2-580">メソッド items</span><span class="sxs-lookup"><span data-stu-id="feee2-580">Method items</span></span>

```xpp
public int items([int value])
```

### <a name="parameters---items"></a><span data-ttu-id="feee2-581">パラメーター - items</span><span class="sxs-lookup"><span data-stu-id="feee2-581">Parameters - items</span></span>

<span data-ttu-id="feee2-582">値</span><span class="sxs-lookup"><span data-stu-id="feee2-582">value</span></span>  

### <a name="return-value---items"></a><span data-ttu-id="feee2-583">戻り値 - items</span><span class="sxs-lookup"><span data-stu-id="feee2-583">Return Value - items</span></span>

## <a name="method-left"></a><span data-ttu-id="feee2-584">メソッド left</span><span class="sxs-lookup"><span data-stu-id="feee2-584">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="feee2-585">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="feee2-585">Parameters - left</span></span>

<span data-ttu-id="feee2-586">値</span><span class="sxs-lookup"><span data-stu-id="feee2-586">value</span></span>  

<!-- -->

<span data-ttu-id="feee2-587">モード</span><span class="sxs-lookup"><span data-stu-id="feee2-587">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="feee2-588">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="feee2-588">Return Value - left</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="feee2-589">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="feee2-589">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="feee2-590">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="feee2-590">Parameters - leftMargin</span></span>

<span data-ttu-id="feee2-591">値</span><span class="sxs-lookup"><span data-stu-id="feee2-591">value</span></span>  

<!-- -->

<span data-ttu-id="feee2-592">モード</span><span class="sxs-lookup"><span data-stu-id="feee2-592">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="feee2-593">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="feee2-593">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="feee2-594">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="feee2-594">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="feee2-595">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="feee2-595">Parameters - leftMarginMode</span></span>

<span data-ttu-id="feee2-596">モード</span><span class="sxs-lookup"><span data-stu-id="feee2-596">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="feee2-597">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="feee2-597">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="feee2-598">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="feee2-598">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="feee2-599">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="feee2-599">Parameters - leftMarginValue</span></span>

<span data-ttu-id="feee2-600">値</span><span class="sxs-lookup"><span data-stu-id="feee2-600">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="feee2-601">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="feee2-601">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="feee2-602">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="feee2-602">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="feee2-603">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="feee2-603">Parameters - leftMode</span></span>

<span data-ttu-id="feee2-604">値</span><span class="sxs-lookup"><span data-stu-id="feee2-604">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="feee2-605">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="feee2-605">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="feee2-606">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="feee2-606">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="feee2-607">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="feee2-607">Parameters - leftValue</span></span>

<span data-ttu-id="feee2-608">値</span><span class="sxs-lookup"><span data-stu-id="feee2-608">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="feee2-609">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="feee2-609">Return Value - leftValue</span></span>

## <a name="method-name"></a><span data-ttu-id="feee2-610">メソッド名</span><span class="sxs-lookup"><span data-stu-id="feee2-610">Method name</span></span>

<span data-ttu-id="feee2-611">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-611">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="feee2-612">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="feee2-612">Parameters - name</span></span>

<span data-ttu-id="feee2-613">値</span><span class="sxs-lookup"><span data-stu-id="feee2-613">value</span></span>  
<span data-ttu-id="feee2-614">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="feee2-614">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="feee2-615">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="feee2-615">Return Value - name</span></span>

<span data-ttu-id="feee2-616">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="feee2-616">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="feee2-617">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="feee2-617">Remarks - name</span></span>

<span data-ttu-id="feee2-618">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="feee2-618">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="feee2-619">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="feee2-619">It must start with a letter.</span></span>
-   <span data-ttu-id="feee2-620">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="feee2-620">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="feee2-621">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="feee2-621">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="feee2-622">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="feee2-622">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="feee2-623">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="feee2-623">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="feee2-624">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="feee2-624">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="feee2-625">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="feee2-625">Parameters - neededPermission</span></span>

<span data-ttu-id="feee2-626">値</span><span class="sxs-lookup"><span data-stu-id="feee2-626">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="feee2-627">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="feee2-627">Return Value - neededPermission</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="feee2-628">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="feee2-628">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="feee2-629">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="feee2-629">Parameters - rightMargin</span></span>

<span data-ttu-id="feee2-630">値</span><span class="sxs-lookup"><span data-stu-id="feee2-630">value</span></span>  

<!-- -->

<span data-ttu-id="feee2-631">モード</span><span class="sxs-lookup"><span data-stu-id="feee2-631">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="feee2-632">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="feee2-632">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="feee2-633">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="feee2-633">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="feee2-634">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="feee2-634">Parameters - rightMarginMode</span></span>

<span data-ttu-id="feee2-635">モード</span><span class="sxs-lookup"><span data-stu-id="feee2-635">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="feee2-636">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="feee2-636">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="feee2-637">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="feee2-637">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="feee2-638">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="feee2-638">Parameters - rightMarginValue</span></span>

<span data-ttu-id="feee2-639">値</span><span class="sxs-lookup"><span data-stu-id="feee2-639">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="feee2-640">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="feee2-640">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="feee2-641">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="feee2-641">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="feee2-642">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="feee2-642">Parameters - securityKey</span></span>

<span data-ttu-id="feee2-643">値</span><span class="sxs-lookup"><span data-stu-id="feee2-643">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="feee2-644">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="feee2-644">Return Value - securityKey</span></span>

## <a name="method-selection"></a><span data-ttu-id="feee2-645">メソッド selection</span><span class="sxs-lookup"><span data-stu-id="feee2-645">Method selection</span></span>

```xpp
public int selection([int value])
```

### <a name="parameters---selection"></a><span data-ttu-id="feee2-646">パラメーター - selection</span><span class="sxs-lookup"><span data-stu-id="feee2-646">Parameters - selection</span></span>

<span data-ttu-id="feee2-647">値</span><span class="sxs-lookup"><span data-stu-id="feee2-647">value</span></span>  

### <a name="return-value---selection"></a><span data-ttu-id="feee2-648">戻り値 - selection</span><span class="sxs-lookup"><span data-stu-id="feee2-648">Return Value - selection</span></span>

## <a name="method-skip"></a><span data-ttu-id="feee2-649">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="feee2-649">Method skip</span></span>

<span data-ttu-id="feee2-650">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="feee2-650">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="feee2-651">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="feee2-651">Parameters - skip</span></span>

<span data-ttu-id="feee2-652">値</span><span class="sxs-lookup"><span data-stu-id="feee2-652">value</span></span>  
<span data-ttu-id="feee2-653">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="feee2-653">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="feee2-654">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="feee2-654">Return Value - skip</span></span>

<span data-ttu-id="feee2-655">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="feee2-655">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-text"></a><span data-ttu-id="feee2-656">メソッド text</span><span class="sxs-lookup"><span data-stu-id="feee2-656">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="feee2-657">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="feee2-657">Parameters - text</span></span>

<span data-ttu-id="feee2-658">値</span><span class="sxs-lookup"><span data-stu-id="feee2-658">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="feee2-659">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="feee2-659">Return Value - text</span></span>

## <a name="method-top"></a><span data-ttu-id="feee2-660">メソッド top</span><span class="sxs-lookup"><span data-stu-id="feee2-660">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="feee2-661">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="feee2-661">Parameters - top</span></span>

<span data-ttu-id="feee2-662">値</span><span class="sxs-lookup"><span data-stu-id="feee2-662">value</span></span>  

<!-- -->

<span data-ttu-id="feee2-663">モード</span><span class="sxs-lookup"><span data-stu-id="feee2-663">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="feee2-664">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="feee2-664">Return Value - top</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="feee2-665">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="feee2-665">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="feee2-666">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="feee2-666">Parameters - topMargin</span></span>

<span data-ttu-id="feee2-667">値</span><span class="sxs-lookup"><span data-stu-id="feee2-667">value</span></span>  

<!-- -->

<span data-ttu-id="feee2-668">モード</span><span class="sxs-lookup"><span data-stu-id="feee2-668">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="feee2-669">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="feee2-669">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="feee2-670">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="feee2-670">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="feee2-671">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="feee2-671">Parameters - topMarginMode</span></span>

<span data-ttu-id="feee2-672">モード</span><span class="sxs-lookup"><span data-stu-id="feee2-672">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="feee2-673">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="feee2-673">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="feee2-674">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="feee2-674">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="feee2-675">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="feee2-675">Parameters - topMarginValue</span></span>

<span data-ttu-id="feee2-676">値</span><span class="sxs-lookup"><span data-stu-id="feee2-676">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="feee2-677">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="feee2-677">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="feee2-678">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="feee2-678">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="feee2-679">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="feee2-679">Parameters - topMode</span></span>

<span data-ttu-id="feee2-680">値</span><span class="sxs-lookup"><span data-stu-id="feee2-680">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="feee2-681">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="feee2-681">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="feee2-682">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="feee2-682">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="feee2-683">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="feee2-683">Parameters - topValue</span></span>

<span data-ttu-id="feee2-684">値</span><span class="sxs-lookup"><span data-stu-id="feee2-684">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="feee2-685">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="feee2-685">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="feee2-686">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="feee2-686">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="feee2-687">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="feee2-687">Parameters - type</span></span>

<span data-ttu-id="feee2-688">値</span><span class="sxs-lookup"><span data-stu-id="feee2-688">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="feee2-689">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="feee2-689">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="feee2-690">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="feee2-690">Method underline</span></span>

<span data-ttu-id="feee2-691">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="feee2-691">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="feee2-692">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="feee2-692">Parameters - underline</span></span>

<span data-ttu-id="feee2-693">値</span><span class="sxs-lookup"><span data-stu-id="feee2-693">value</span></span>  
<span data-ttu-id="feee2-694">コントロールの underline プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="feee2-694">The value to assign to the underline property of the control; optional.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="feee2-695">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="feee2-695">Return Value - underline</span></span>

<span data-ttu-id="feee2-696">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="feee2-696">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-userdata"></a><span data-ttu-id="feee2-697">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="feee2-697">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="feee2-698">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="feee2-698">Parameters - userData</span></span>

<span data-ttu-id="feee2-699">値</span><span class="sxs-lookup"><span data-stu-id="feee2-699">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="feee2-700">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="feee2-700">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="feee2-701">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="feee2-701">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="feee2-702">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="feee2-702">Parameters - userDataItem</span></span>

<span data-ttu-id="feee2-703">値</span><span class="sxs-lookup"><span data-stu-id="feee2-703">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="feee2-704">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="feee2-704">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="feee2-705">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="feee2-705">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="feee2-706">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="feee2-706">Parameters - userDataItems</span></span>

<span data-ttu-id="feee2-707">値</span><span class="sxs-lookup"><span data-stu-id="feee2-707">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="feee2-708">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="feee2-708">Return Value - userDataItems</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="feee2-709">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="feee2-709">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="feee2-710">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="feee2-710">Parameters - verticalSpacing</span></span>

<span data-ttu-id="feee2-711">値</span><span class="sxs-lookup"><span data-stu-id="feee2-711">value</span></span>  

<!-- -->

<span data-ttu-id="feee2-712">モード</span><span class="sxs-lookup"><span data-stu-id="feee2-712">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="feee2-713">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="feee2-713">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="feee2-714">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="feee2-714">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="feee2-715">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="feee2-715">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="feee2-716">モード</span><span class="sxs-lookup"><span data-stu-id="feee2-716">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="feee2-717">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="feee2-717">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="feee2-718">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="feee2-718">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="feee2-719">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="feee2-719">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="feee2-720">値</span><span class="sxs-lookup"><span data-stu-id="feee2-720">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="feee2-721">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="feee2-721">Return Value - verticalSpacingValue</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="feee2-722">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="feee2-722">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="feee2-723">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="feee2-723">Parameters - viewEditMode</span></span>

<span data-ttu-id="feee2-724">値</span><span class="sxs-lookup"><span data-stu-id="feee2-724">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="feee2-725">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="feee2-725">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="feee2-726">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="feee2-726">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="feee2-727">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="feee2-727">Parameters - visible</span></span>

<span data-ttu-id="feee2-728">値</span><span class="sxs-lookup"><span data-stu-id="feee2-728">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="feee2-729">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="feee2-729">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="feee2-730">メソッド width</span><span class="sxs-lookup"><span data-stu-id="feee2-730">Method width</span></span>

<span data-ttu-id="feee2-731">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-731">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="feee2-732">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="feee2-732">Parameters - width</span></span>

<span data-ttu-id="feee2-733">値</span><span class="sxs-lookup"><span data-stu-id="feee2-733">value</span></span>  

<!-- -->

<span data-ttu-id="feee2-734">モード</span><span class="sxs-lookup"><span data-stu-id="feee2-734">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="feee2-735">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="feee2-735">Return Value - width</span></span>

<span data-ttu-id="feee2-736">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="feee2-736">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="feee2-737">備考 - width</span><span class="sxs-lookup"><span data-stu-id="feee2-737">Remarks - width</span></span>

<span data-ttu-id="feee2-738">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="feee2-738">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="feee2-739">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="feee2-739">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="feee2-740">モード。</span><span class="sxs-lookup"><span data-stu-id="feee2-740">Mode.</span></span>           | <span data-ttu-id="feee2-741">幅計算。</span><span class="sxs-lookup"><span data-stu-id="feee2-741">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="feee2-742">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="feee2-742">-1 Exact.</span></span>       | <span data-ttu-id="feee2-743">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="feee2-743">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="feee2-744">0 自動。</span><span class="sxs-lookup"><span data-stu-id="feee2-744">0 Auto.</span></span>         | <span data-ttu-id="feee2-745">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="feee2-745">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="feee2-746">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="feee2-746">1 Column width.</span></span> | <span data-ttu-id="feee2-747">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="feee2-747">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="feee2-748">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="feee2-748">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="feee2-749">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="feee2-749">Method widthMode</span></span>

<span data-ttu-id="feee2-750">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-750">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="feee2-751">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="feee2-751">Parameters - widthMode</span></span>

<span data-ttu-id="feee2-752">値</span><span class="sxs-lookup"><span data-stu-id="feee2-752">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="feee2-753">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="feee2-753">Return Value - widthMode</span></span>

<span data-ttu-id="feee2-754">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="feee2-754">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="feee2-755">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="feee2-755">Remarks - widthMode</span></span>

<span data-ttu-id="feee2-756">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="feee2-756">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="feee2-757">モード。</span><span class="sxs-lookup"><span data-stu-id="feee2-757">Mode.</span></span>         | <span data-ttu-id="feee2-758">幅計算。</span><span class="sxs-lookup"><span data-stu-id="feee2-758">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="feee2-759">正確。</span><span class="sxs-lookup"><span data-stu-id="feee2-759">Exact.</span></span>        | <span data-ttu-id="feee2-760">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="feee2-760">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="feee2-761">自動。</span><span class="sxs-lookup"><span data-stu-id="feee2-761">Auto.</span></span>         | <span data-ttu-id="feee2-762">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="feee2-762">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="feee2-763">列の幅。</span><span class="sxs-lookup"><span data-stu-id="feee2-763">Column width.</span></span> | <span data-ttu-id="feee2-764">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="feee2-764">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="feee2-765">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="feee2-765">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="feee2-766">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="feee2-766">Method widthValue</span></span>

<span data-ttu-id="feee2-767">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="feee2-767">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="feee2-768">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="feee2-768">Parameters - widthValue</span></span>

<span data-ttu-id="feee2-769">値</span><span class="sxs-lookup"><span data-stu-id="feee2-769">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="feee2-770">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="feee2-770">Return Value - widthValue</span></span>

<span data-ttu-id="feee2-771">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="feee2-771">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="feee2-772">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="feee2-772">Remarks - widthValue</span></span>

<span data-ttu-id="feee2-773">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="feee2-773">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="feee2-774">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="feee2-774">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="feee2-775">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="feee2-775">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="feee2-776">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="feee2-776">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="feee2-777">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="feee2-777">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="feee2-778">overrideObject</span><span class="sxs-lookup"><span data-stu-id="feee2-778">overrideObject</span></span>  

