---
title: FormBuildListBoxControl クラス
description: このトピックでは、FormBuildListBoxControl クラスについて説明します。
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
ms.openlocfilehash: edbe67819433c580cda33df505658272cc46646c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502965"
---
# <a name="class-formbuildlistboxcontrol"></a><span data-ttu-id="00d02-103">クラス FormBuildListBoxControl</span><span class="sxs-lookup"><span data-stu-id="00d02-103">Class FormBuildListBoxControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildListBoxControl extends FormBuildControl
```

<span data-ttu-id="00d02-104">FormBuildListBoxControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="00d02-104">The FormBuildListBoxControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="00d02-105">備考</span><span class="sxs-lookup"><span data-stu-id="00d02-105">Remarks</span></span>

<span data-ttu-id="00d02-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00d02-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="00d02-107">例</span><span class="sxs-lookup"><span data-stu-id="00d02-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="00d02-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="00d02-108">Methods</span></span>

| <span data-ttu-id="00d02-109">方法</span><span class="sxs-lookup"><span data-stu-id="00d02-109">Method</span></span>                                                                                                      | <span data-ttu-id="00d02-110">説明</span><span class="sxs-lookup"><span data-stu-id="00d02-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d02-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="00d02-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-112">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="00d02-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="00d02-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-114">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="00d02-115">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-115">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="00d02-116">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-116">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="00d02-117">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-117">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="00d02-118">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-118">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="00d02-119">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-119">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="00d02-120">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-120">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="00d02-121">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-121">Determines whether the control background can be transparent.</span></span>                                                                          |
| <span data-ttu-id="00d02-122">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-122">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="00d02-123">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-123">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                             |
| <span data-ttu-id="00d02-124">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-124">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="00d02-125">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-125">Gets or sets the style of the borderline of the control.</span></span>                                                                                |
| <span data-ttu-id="00d02-126">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-126">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="00d02-127">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-127">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="00d02-128">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-128">Gets or sets the character set of the font.</span></span>                                                                                             |
| <span data-ttu-id="00d02-129">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-129">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="00d02-130">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-130">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="00d02-131">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-131">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="00d02-132">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-132">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="00d02-133">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="00d02-133">public int containerId()</span></span>                                                                                    | <span data-ttu-id="00d02-134">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="00d02-134">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="00d02-135">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-135">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="00d02-136">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-136">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                         |
| <span data-ttu-id="00d02-137">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-137">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="00d02-138">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-138">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="00d02-139">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-139">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="00d02-140">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-140">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="00d02-141">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-141">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                |
| <span data-ttu-id="00d02-142">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="00d02-142">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                         |
| <span data-ttu-id="00d02-143">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="00d02-143">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                         |
| <span data-ttu-id="00d02-144">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-144">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="00d02-145">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-145">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="00d02-146">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-146">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="00d02-147">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-147">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="00d02-148">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-148">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="00d02-149">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-149">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="00d02-150">public EnumId enumType(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-150">public EnumId enumType(\[EnumId value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="00d02-151">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-151">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                         |
| <span data-ttu-id="00d02-152">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-152">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="00d02-153">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-153">Gets or sets the name of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="00d02-154">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-154">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="00d02-155">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-155">Gets or sets the size of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="00d02-156">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-156">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="00d02-157">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-157">Gets or sets the text color for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="00d02-158">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="00d02-158">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="00d02-159">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-159">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="00d02-160">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-160">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="00d02-161">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-161">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="00d02-162">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-162">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="00d02-163">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-163">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="00d02-164">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-164">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="00d02-165">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-165">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="00d02-166">public boolean hideFirstEntry(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-166">public boolean hideFirstEntry(\[boolean value\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="00d02-167">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-167">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="00d02-168">public int id()</span><span class="sxs-lookup"><span data-stu-id="00d02-168">public int id()</span></span>                                                                                             | <span data-ttu-id="00d02-169">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="00d02-169">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="00d02-170">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="00d02-170">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="00d02-171">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="00d02-171">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="00d02-172">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-172">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="00d02-173">public int item(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-173">public int item(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="00d02-174">public int items(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-174">public int items(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="00d02-175">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-175">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="00d02-176">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-176">Gets or sets the label for a control.</span></span>                                                                                                   |
| <span data-ttu-id="00d02-177">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-177">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="00d02-178">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-178">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="00d02-179">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-179">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="00d02-180">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-180">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="00d02-181">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-181">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="00d02-182">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-182">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="00d02-183">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-183">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="00d02-184">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="00d02-184">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="00d02-185">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-185">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="00d02-186">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-186">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="00d02-187">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-187">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="00d02-188">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-188">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="00d02-189">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-189">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="00d02-190">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="00d02-190">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="00d02-191">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-191">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="00d02-192">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-192">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="00d02-193">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="00d02-193">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="00d02-194">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-194">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="00d02-195">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-195">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="00d02-196">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-196">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="00d02-197">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-197">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="00d02-198">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-198">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="00d02-199">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-199">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="00d02-200">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-200">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="00d02-201">public int selection(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-201">public int selection(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="00d02-202">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-202">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="00d02-203">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-203">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="00d02-204">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="00d02-204">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="00d02-205">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-205">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="00d02-206">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="00d02-206">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="00d02-207">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-207">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="00d02-208">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-208">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="00d02-209">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-209">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="00d02-210">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-210">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="00d02-211">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="00d02-211">Sets or returns the underline property for the text in the control.</span></span>                                                                     |
| <span data-ttu-id="00d02-212">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-212">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="00d02-213">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-213">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="00d02-214">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-214">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="00d02-215">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="00d02-215">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="00d02-216">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="00d02-216">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="00d02-217">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-217">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="00d02-218">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-218">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="00d02-219">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-219">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="00d02-220">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="00d02-220">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="00d02-221">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-221">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="00d02-222">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-222">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="00d02-223">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-223">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="00d02-224">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="00d02-224">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="00d02-225">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-225">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="00d02-226">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="00d02-226">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="00d02-227">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="00d02-227">Method alignControl</span></span>

<span data-ttu-id="00d02-228">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-228">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="00d02-229">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="00d02-229">Parameters - alignControl</span></span>

<span data-ttu-id="00d02-230">値</span><span class="sxs-lookup"><span data-stu-id="00d02-230">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="00d02-231">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="00d02-231">Return Value - alignControl</span></span>

<span data-ttu-id="00d02-232">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="00d02-232">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="00d02-233">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="00d02-233">Remarks - alignControl</span></span>

<span data-ttu-id="00d02-234">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="00d02-234">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="00d02-235">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="00d02-235">Method allowEdit</span></span>

<span data-ttu-id="00d02-236">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-236">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="00d02-237">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="00d02-237">Parameters - allowEdit</span></span>

<span data-ttu-id="00d02-238">値</span><span class="sxs-lookup"><span data-stu-id="00d02-238">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="00d02-239">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="00d02-239">Return Value - allowEdit</span></span>

<span data-ttu-id="00d02-240">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="00d02-240">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="00d02-241">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="00d02-241">Remarks - allowEdit</span></span>

<span data-ttu-id="00d02-242">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="00d02-242">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="00d02-243">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="00d02-243">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="00d02-244">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="00d02-244">Parameters - arrayIndex</span></span>

<span data-ttu-id="00d02-245">値</span><span class="sxs-lookup"><span data-stu-id="00d02-245">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="00d02-246">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="00d02-246">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="00d02-247">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="00d02-247">Method autoDeclaration</span></span>

<span data-ttu-id="00d02-248">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-248">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="00d02-249">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="00d02-249">Parameters - autoDeclaration</span></span>

<span data-ttu-id="00d02-250">値</span><span class="sxs-lookup"><span data-stu-id="00d02-250">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="00d02-251">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="00d02-251">Return Value - autoDeclaration</span></span>

<span data-ttu-id="00d02-252">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="00d02-252">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="00d02-253">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="00d02-253">Remarks - autoDeclaration</span></span>

<span data-ttu-id="00d02-254">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="00d02-254">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="00d02-255">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="00d02-255">Method backgroundColor</span></span>

<span data-ttu-id="00d02-256">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-256">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="00d02-257">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="00d02-257">Parameters - backgroundColor</span></span>

<span data-ttu-id="00d02-258">値</span><span class="sxs-lookup"><span data-stu-id="00d02-258">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="00d02-259">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="00d02-259">Return Value - backgroundColor</span></span>

<span data-ttu-id="00d02-260">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="00d02-260">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="00d02-261">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="00d02-261">Remarks - backgroundColor</span></span>

<span data-ttu-id="00d02-262">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="00d02-262">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="00d02-263">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="00d02-263">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="00d02-264">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="00d02-264">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="00d02-265">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="00d02-265">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="00d02-266">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="00d02-266">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="00d02-267">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="00d02-267">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="00d02-268">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="00d02-268">Method backStyle</span></span>

<span data-ttu-id="00d02-269">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-269">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="00d02-270">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="00d02-270">Parameters - backStyle</span></span>

<span data-ttu-id="00d02-271">値</span><span class="sxs-lookup"><span data-stu-id="00d02-271">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="00d02-272">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="00d02-272">Return Value - backStyle</span></span>

<span data-ttu-id="00d02-273">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="00d02-273">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="00d02-274">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="00d02-274">Method bold</span></span>

<span data-ttu-id="00d02-275">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-275">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="00d02-276">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="00d02-276">Parameters - bold</span></span>

<span data-ttu-id="00d02-277">値</span><span class="sxs-lookup"><span data-stu-id="00d02-277">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="00d02-278">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="00d02-278">Return Value - bold</span></span>

<span data-ttu-id="00d02-279">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="00d02-279">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="00d02-280">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="00d02-280">Remarks - bold</span></span>

<span data-ttu-id="00d02-281">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="00d02-281">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="00d02-282">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="00d02-282">0 Use the default font weight.</span></span>
-   <span data-ttu-id="00d02-283">1 シン。</span><span class="sxs-lookup"><span data-stu-id="00d02-283">1 Thin.</span></span>
-   <span data-ttu-id="00d02-284">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="00d02-284">2 Extra-light.</span></span>
-   <span data-ttu-id="00d02-285">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="00d02-285">3 Light.</span></span>
-   <span data-ttu-id="00d02-286">4 標準。</span><span class="sxs-lookup"><span data-stu-id="00d02-286">4 Normal.</span></span>
-   <span data-ttu-id="00d02-287">5 中。</span><span class="sxs-lookup"><span data-stu-id="00d02-287">5 Medium.</span></span>
-   <span data-ttu-id="00d02-288">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="00d02-288">6 Semibold.</span></span>
-   <span data-ttu-id="00d02-289">7 太字。</span><span class="sxs-lookup"><span data-stu-id="00d02-289">7 Bold.</span></span>
-   <span data-ttu-id="00d02-290">8 極太。</span><span class="sxs-lookup"><span data-stu-id="00d02-290">8 Extra-bold.</span></span>
-   <span data-ttu-id="00d02-291">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="00d02-291">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="00d02-292">メソッド border</span><span class="sxs-lookup"><span data-stu-id="00d02-292">Method border</span></span>

<span data-ttu-id="00d02-293">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-293">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="00d02-294">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="00d02-294">Parameters - border</span></span>

<span data-ttu-id="00d02-295">値</span><span class="sxs-lookup"><span data-stu-id="00d02-295">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="00d02-296">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="00d02-296">Return Value - border</span></span>

<span data-ttu-id="00d02-297">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="00d02-297">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="00d02-298">備考 - border</span><span class="sxs-lookup"><span data-stu-id="00d02-298">Remarks - border</span></span>

<span data-ttu-id="00d02-299">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="00d02-299">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="00d02-300">値です。</span><span class="sxs-lookup"><span data-stu-id="00d02-300">Value.</span></span> | <span data-ttu-id="00d02-301">説明。</span><span class="sxs-lookup"><span data-stu-id="00d02-301">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="00d02-302">0</span><span class="sxs-lookup"><span data-stu-id="00d02-302">0</span></span>      | <span data-ttu-id="00d02-303">自動。</span><span class="sxs-lookup"><span data-stu-id="00d02-303">Auto.</span></span>        |
| <span data-ttu-id="00d02-304">1</span><span class="sxs-lookup"><span data-stu-id="00d02-304">1</span></span>      | <span data-ttu-id="00d02-305">3D。</span><span class="sxs-lookup"><span data-stu-id="00d02-305">3D.</span></span>          |
| <span data-ttu-id="00d02-306">2</span><span class="sxs-lookup"><span data-stu-id="00d02-306">2</span></span>      | <span data-ttu-id="00d02-307">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="00d02-307">Single line.</span></span> |
| <span data-ttu-id="00d02-308">3</span><span class="sxs-lookup"><span data-stu-id="00d02-308">3</span></span>      | <span data-ttu-id="00d02-309">均一。</span><span class="sxs-lookup"><span data-stu-id="00d02-309">Flat.</span></span>        |
| <span data-ttu-id="00d02-310">4</span><span class="sxs-lookup"><span data-stu-id="00d02-310">4</span></span>      | <span data-ttu-id="00d02-311">なし。</span><span class="sxs-lookup"><span data-stu-id="00d02-311">None.</span></span>        |

## <a name="method-cachedatamethod"></a><span data-ttu-id="00d02-312">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="00d02-312">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="00d02-313">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="00d02-313">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="00d02-314">値</span><span class="sxs-lookup"><span data-stu-id="00d02-314">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="00d02-315">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="00d02-315">Return Value - cacheDataMethod</span></span>

## <a name="method-characterset"></a><span data-ttu-id="00d02-316">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="00d02-316">Method characterSet</span></span>

<span data-ttu-id="00d02-317">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-317">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="00d02-318">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="00d02-318">Parameters - characterSet</span></span>

<span data-ttu-id="00d02-319">値</span><span class="sxs-lookup"><span data-stu-id="00d02-319">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="00d02-320">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="00d02-320">Return Value - characterSet</span></span>

<span data-ttu-id="00d02-321">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="00d02-321">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="00d02-322">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="00d02-322">Remarks - characterSet</span></span>

<span data-ttu-id="00d02-323">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="00d02-323">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="00d02-324">値です。</span><span class="sxs-lookup"><span data-stu-id="00d02-324">Value.</span></span> | <span data-ttu-id="00d02-325">説明。</span><span class="sxs-lookup"><span data-stu-id="00d02-325">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="00d02-326">0</span><span class="sxs-lookup"><span data-stu-id="00d02-326">0</span></span>      | <span data-ttu-id="00d02-327">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="00d02-327">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="00d02-328">1</span><span class="sxs-lookup"><span data-stu-id="00d02-328">1</span></span>      | <span data-ttu-id="00d02-329">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="00d02-329">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="00d02-330">2</span><span class="sxs-lookup"><span data-stu-id="00d02-330">2</span></span>      | <span data-ttu-id="00d02-331">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="00d02-331">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="00d02-332">77</span><span class="sxs-lookup"><span data-stu-id="00d02-332">77</span></span>     | <span data-ttu-id="00d02-333">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="00d02-333">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="00d02-334">128</span><span class="sxs-lookup"><span data-stu-id="00d02-334">128</span></span>    | <span data-ttu-id="00d02-335">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="00d02-335">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="00d02-336">129</span><span class="sxs-lookup"><span data-stu-id="00d02-336">129</span></span>    | <span data-ttu-id="00d02-337">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="00d02-337">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="00d02-338">134</span><span class="sxs-lookup"><span data-stu-id="00d02-338">134</span></span>    | <span data-ttu-id="00d02-339">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="00d02-339">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="00d02-340">136</span><span class="sxs-lookup"><span data-stu-id="00d02-340">136</span></span>    | <span data-ttu-id="00d02-341">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="00d02-341">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="00d02-342">161</span><span class="sxs-lookup"><span data-stu-id="00d02-342">161</span></span>    | <span data-ttu-id="00d02-343">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="00d02-343">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="00d02-344">162</span><span class="sxs-lookup"><span data-stu-id="00d02-344">162</span></span>    | <span data-ttu-id="00d02-345">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="00d02-345">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="00d02-346">163</span><span class="sxs-lookup"><span data-stu-id="00d02-346">163</span></span>    | <span data-ttu-id="00d02-347">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="00d02-347">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="00d02-348">186</span><span class="sxs-lookup"><span data-stu-id="00d02-348">186</span></span>    | <span data-ttu-id="00d02-349">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="00d02-349">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="00d02-350">204</span><span class="sxs-lookup"><span data-stu-id="00d02-350">204</span></span>    | <span data-ttu-id="00d02-351">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="00d02-351">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="00d02-352">238</span><span class="sxs-lookup"><span data-stu-id="00d02-352">238</span></span>    | <span data-ttu-id="00d02-353">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="00d02-353">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="00d02-354">255</span><span class="sxs-lookup"><span data-stu-id="00d02-354">255</span></span>    | <span data-ttu-id="00d02-355">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="00d02-355">OEM\_CHARSET</span></span>         |

<span data-ttu-id="00d02-356">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="00d02-356">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="00d02-357">値です。</span><span class="sxs-lookup"><span data-stu-id="00d02-357">Value.</span></span> | <span data-ttu-id="00d02-358">説明。</span><span class="sxs-lookup"><span data-stu-id="00d02-358">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="00d02-359">130</span><span class="sxs-lookup"><span data-stu-id="00d02-359">130</span></span>    | <span data-ttu-id="00d02-360">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="00d02-360">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="00d02-361">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="00d02-361">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="00d02-362">値です。</span><span class="sxs-lookup"><span data-stu-id="00d02-362">Value.</span></span> | <span data-ttu-id="00d02-363">説明。</span><span class="sxs-lookup"><span data-stu-id="00d02-363">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="00d02-364">177</span><span class="sxs-lookup"><span data-stu-id="00d02-364">177</span></span>    | <span data-ttu-id="00d02-365">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="00d02-365">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="00d02-366">178</span><span class="sxs-lookup"><span data-stu-id="00d02-366">178</span></span>    | <span data-ttu-id="00d02-367">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="00d02-367">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="00d02-368">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="00d02-368">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="00d02-369">値です。</span><span class="sxs-lookup"><span data-stu-id="00d02-369">Value.</span></span> | <span data-ttu-id="00d02-370">説明。</span><span class="sxs-lookup"><span data-stu-id="00d02-370">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="00d02-371">222</span><span class="sxs-lookup"><span data-stu-id="00d02-371">222</span></span>    | <span data-ttu-id="00d02-372">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="00d02-372">THAI\_CHARSET</span></span> |

<span data-ttu-id="00d02-373">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="00d02-373">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="00d02-374">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="00d02-374">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="00d02-375">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00d02-375">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="00d02-376">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="00d02-376">Method colorScheme</span></span>

<span data-ttu-id="00d02-377">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-377">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="00d02-378">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="00d02-378">Parameters - colorScheme</span></span>

<span data-ttu-id="00d02-379">値</span><span class="sxs-lookup"><span data-stu-id="00d02-379">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="00d02-380">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="00d02-380">Return Value - colorScheme</span></span>

<span data-ttu-id="00d02-381">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="00d02-381">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="00d02-382">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="00d02-382">Remarks - colorScheme</span></span>

<span data-ttu-id="00d02-383">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="00d02-383">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="00d02-384">値です。</span><span class="sxs-lookup"><span data-stu-id="00d02-384">Value.</span></span> | <span data-ttu-id="00d02-385">スタイル。</span><span class="sxs-lookup"><span data-stu-id="00d02-385">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="00d02-386">0</span><span class="sxs-lookup"><span data-stu-id="00d02-386">0</span></span>      | <span data-ttu-id="00d02-387">既定。</span><span class="sxs-lookup"><span data-stu-id="00d02-387">Default.</span></span>                      |
| <span data-ttu-id="00d02-388">1</span><span class="sxs-lookup"><span data-stu-id="00d02-388">1</span></span>      | <span data-ttu-id="00d02-389">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="00d02-389">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="00d02-390">2</span><span class="sxs-lookup"><span data-stu-id="00d02-390">2</span></span>      | <span data-ttu-id="00d02-391">真の配色。</span><span class="sxs-lookup"><span data-stu-id="00d02-391">The true-color scheme.</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="00d02-392">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="00d02-392">Method configurationKey</span></span>

<span data-ttu-id="00d02-393">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-393">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="00d02-394">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="00d02-394">Parameters - configurationKey</span></span>

<span data-ttu-id="00d02-395">値</span><span class="sxs-lookup"><span data-stu-id="00d02-395">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="00d02-396">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="00d02-396">Return Value - configurationKey</span></span>

<span data-ttu-id="00d02-397">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="00d02-397">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="00d02-398">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="00d02-398">Remarks - configurationKey</span></span>

<span data-ttu-id="00d02-399">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="00d02-399">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="00d02-400">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="00d02-400">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="00d02-401">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="00d02-401">Method containerId</span></span>

<span data-ttu-id="00d02-402">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="00d02-402">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="00d02-403">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="00d02-403">Return Value - containerId</span></span>

<span data-ttu-id="00d02-404">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="00d02-404">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="00d02-405">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="00d02-405">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="00d02-406">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="00d02-406">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="00d02-407">値</span><span class="sxs-lookup"><span data-stu-id="00d02-407">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="00d02-408">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="00d02-408">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="00d02-409">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="00d02-409">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="00d02-410">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="00d02-410">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="00d02-411">値</span><span class="sxs-lookup"><span data-stu-id="00d02-411">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="00d02-412">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="00d02-412">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="00d02-413">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="00d02-413">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="00d02-414">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="00d02-414">Parameters - dataField</span></span>

<span data-ttu-id="00d02-415">値</span><span class="sxs-lookup"><span data-stu-id="00d02-415">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="00d02-416">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="00d02-416">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="00d02-417">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="00d02-417">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="00d02-418">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="00d02-418">Parameters - dataMethod</span></span>

<span data-ttu-id="00d02-419">値</span><span class="sxs-lookup"><span data-stu-id="00d02-419">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="00d02-420">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="00d02-420">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="00d02-421">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="00d02-421">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="00d02-422">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="00d02-422">Parameters - dataRelationPath</span></span>

<span data-ttu-id="00d02-423">値</span><span class="sxs-lookup"><span data-stu-id="00d02-423">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="00d02-424">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="00d02-424">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="00d02-425">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="00d02-425">Method dataSource</span></span>

<span data-ttu-id="00d02-426">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-426">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="00d02-427">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="00d02-427">Parameters - dataSource</span></span>

<span data-ttu-id="00d02-428">値</span><span class="sxs-lookup"><span data-stu-id="00d02-428">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="00d02-429">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="00d02-429">Return Value - dataSource</span></span>

<span data-ttu-id="00d02-430">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="00d02-430">The identifier of the data source that will be used.</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="00d02-431">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="00d02-431">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="00d02-432">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="00d02-432">Parameters - displayLength</span></span>

<span data-ttu-id="00d02-433">値</span><span class="sxs-lookup"><span data-stu-id="00d02-433">value</span></span>  

<!-- -->

<span data-ttu-id="00d02-434">モード</span><span class="sxs-lookup"><span data-stu-id="00d02-434">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="00d02-435">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="00d02-435">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="00d02-436">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="00d02-436">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="00d02-437">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="00d02-437">Parameters - displayLengthMode</span></span>

<span data-ttu-id="00d02-438">モード</span><span class="sxs-lookup"><span data-stu-id="00d02-438">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="00d02-439">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="00d02-439">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="00d02-440">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="00d02-440">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="00d02-441">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="00d02-441">Parameters - displayLengthValue</span></span>

<span data-ttu-id="00d02-442">値</span><span class="sxs-lookup"><span data-stu-id="00d02-442">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="00d02-443">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="00d02-443">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="00d02-444">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="00d02-444">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="00d02-445">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="00d02-445">Parameters - displayTarget</span></span>

<span data-ttu-id="00d02-446">値</span><span class="sxs-lookup"><span data-stu-id="00d02-446">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="00d02-447">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="00d02-447">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="00d02-448">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="00d02-448">Method dragDrop</span></span>

<span data-ttu-id="00d02-449">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-449">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="00d02-450">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="00d02-450">Parameters - dragDrop</span></span>

<span data-ttu-id="00d02-451">値</span><span class="sxs-lookup"><span data-stu-id="00d02-451">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="00d02-452">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="00d02-452">Return Value - dragDrop</span></span>

<span data-ttu-id="00d02-453">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="00d02-453">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="00d02-454">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="00d02-454">Method enabled</span></span>

<span data-ttu-id="00d02-455">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-455">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="00d02-456">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="00d02-456">Parameters - enabled</span></span>

<span data-ttu-id="00d02-457">値</span><span class="sxs-lookup"><span data-stu-id="00d02-457">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="00d02-458">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="00d02-458">Return Value - enabled</span></span>

<span data-ttu-id="00d02-459">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="00d02-459">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="00d02-460">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="00d02-460">Remarks - enabled</span></span>

<span data-ttu-id="00d02-461">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="00d02-461">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="00d02-462">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="00d02-462">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="00d02-463">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="00d02-463">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-enumtype"></a><span data-ttu-id="00d02-464">メソッド enumType</span><span class="sxs-lookup"><span data-stu-id="00d02-464">Method enumType</span></span>

```xpp
public EnumId enumType([EnumId value])
```

### <a name="parameters---enumtype"></a><span data-ttu-id="00d02-465">パラメーター - enumType</span><span class="sxs-lookup"><span data-stu-id="00d02-465">Parameters - enumType</span></span>

<span data-ttu-id="00d02-466">値</span><span class="sxs-lookup"><span data-stu-id="00d02-466">value</span></span>  

### <a name="return-value---enumtype"></a><span data-ttu-id="00d02-467">戻り値 - enumType</span><span class="sxs-lookup"><span data-stu-id="00d02-467">Return Value - enumType</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="00d02-468">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="00d02-468">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="00d02-469">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="00d02-469">Parameters - extendedDataType</span></span>

<span data-ttu-id="00d02-470">値</span><span class="sxs-lookup"><span data-stu-id="00d02-470">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="00d02-471">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="00d02-471">Return Value - extendedDataType</span></span>

## <a name="method-font"></a><span data-ttu-id="00d02-472">メソッド font</span><span class="sxs-lookup"><span data-stu-id="00d02-472">Method font</span></span>

<span data-ttu-id="00d02-473">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-473">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="00d02-474">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="00d02-474">Parameters - font</span></span>

<span data-ttu-id="00d02-475">値</span><span class="sxs-lookup"><span data-stu-id="00d02-475">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="00d02-476">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="00d02-476">Return Value - font</span></span>

<span data-ttu-id="00d02-477">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="00d02-477">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="00d02-478">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="00d02-478">Method fontSize</span></span>

<span data-ttu-id="00d02-479">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-479">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="00d02-480">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="00d02-480">Parameters - fontSize</span></span>

<span data-ttu-id="00d02-481">値</span><span class="sxs-lookup"><span data-stu-id="00d02-481">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="00d02-482">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="00d02-482">Return Value - fontSize</span></span>

<span data-ttu-id="00d02-483">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="00d02-483">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="00d02-484">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="00d02-484">Method foregroundColor</span></span>

<span data-ttu-id="00d02-485">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-485">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="00d02-486">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="00d02-486">Parameters - foregroundColor</span></span>

<span data-ttu-id="00d02-487">値</span><span class="sxs-lookup"><span data-stu-id="00d02-487">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="00d02-488">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="00d02-488">Return Value - foregroundColor</span></span>

<span data-ttu-id="00d02-489">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="00d02-489">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="00d02-490">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="00d02-490">Remarks - foregroundColor</span></span>

<span data-ttu-id="00d02-491">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="00d02-491">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="00d02-492">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="00d02-492">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="00d02-493">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="00d02-493">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="00d02-494">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="00d02-494">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="00d02-495">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="00d02-495">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="00d02-496">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="00d02-496">The maximum value for a single byte is 255.</span></span>

## <a name="method-height"></a><span data-ttu-id="00d02-497">メソッド height</span><span class="sxs-lookup"><span data-stu-id="00d02-497">Method height</span></span>

<span data-ttu-id="00d02-498">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-498">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="00d02-499">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="00d02-499">Parameters - height</span></span>

<span data-ttu-id="00d02-500">値</span><span class="sxs-lookup"><span data-stu-id="00d02-500">value</span></span>  

<!-- -->

<span data-ttu-id="00d02-501">モード</span><span class="sxs-lookup"><span data-stu-id="00d02-501">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="00d02-502">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="00d02-502">Return Value - height</span></span>

<span data-ttu-id="00d02-503">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="00d02-503">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="00d02-504">備考 - height</span><span class="sxs-lookup"><span data-stu-id="00d02-504">Remarks - height</span></span>

<span data-ttu-id="00d02-505">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="00d02-505">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="00d02-506">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="00d02-506">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="00d02-507">モード。</span><span class="sxs-lookup"><span data-stu-id="00d02-507">Mode.</span></span>            | <span data-ttu-id="00d02-508">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="00d02-508">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d02-509">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="00d02-509">-1 Exact.</span></span>        | <span data-ttu-id="00d02-510">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="00d02-510">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="00d02-511">0 自動。</span><span class="sxs-lookup"><span data-stu-id="00d02-511">0 Auto.</span></span>          | <span data-ttu-id="00d02-512">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="00d02-512">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="00d02-513">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="00d02-513">1 Column height.</span></span> | <span data-ttu-id="00d02-514">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="00d02-514">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="00d02-515">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="00d02-515">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="00d02-516">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="00d02-516">Method heightMode</span></span>

<span data-ttu-id="00d02-517">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-517">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="00d02-518">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="00d02-518">Parameters - heightMode</span></span>

<span data-ttu-id="00d02-519">値</span><span class="sxs-lookup"><span data-stu-id="00d02-519">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="00d02-520">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="00d02-520">Return Value - heightMode</span></span>

<span data-ttu-id="00d02-521">計算モード。</span><span class="sxs-lookup"><span data-stu-id="00d02-521">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="00d02-522">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="00d02-522">Remarks - heightMode</span></span>

<span data-ttu-id="00d02-523">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="00d02-523">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="00d02-524">モード。</span><span class="sxs-lookup"><span data-stu-id="00d02-524">Mode.</span></span>          | <span data-ttu-id="00d02-525">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="00d02-525">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d02-526">正確。</span><span class="sxs-lookup"><span data-stu-id="00d02-526">Exact.</span></span>         | <span data-ttu-id="00d02-527">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="00d02-527">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="00d02-528">自動。</span><span class="sxs-lookup"><span data-stu-id="00d02-528">Auto.</span></span>          | <span data-ttu-id="00d02-529">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="00d02-529">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="00d02-530">列の高さ</span><span class="sxs-lookup"><span data-stu-id="00d02-530">Column height.</span></span> | <span data-ttu-id="00d02-531">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="00d02-531">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="00d02-532">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="00d02-532">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="00d02-533">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="00d02-533">Method heightValue</span></span>

<span data-ttu-id="00d02-534">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-534">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="00d02-535">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="00d02-535">Parameters - heightValue</span></span>

<span data-ttu-id="00d02-536">値</span><span class="sxs-lookup"><span data-stu-id="00d02-536">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="00d02-537">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="00d02-537">Return Value - heightValue</span></span>

<span data-ttu-id="00d02-538">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="00d02-538">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="00d02-539">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="00d02-539">Remarks - heightValue</span></span>

<span data-ttu-id="00d02-540">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="00d02-540">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="00d02-541">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="00d02-541">Method helpText</span></span>

<span data-ttu-id="00d02-542">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-542">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="00d02-543">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="00d02-543">Parameters - helpText</span></span>

<span data-ttu-id="00d02-544">値</span><span class="sxs-lookup"><span data-stu-id="00d02-544">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="00d02-545">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="00d02-545">Return Value - helpText</span></span>

<span data-ttu-id="00d02-546">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="00d02-546">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="00d02-547">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="00d02-547">Remarks - helpText</span></span>

<span data-ttu-id="00d02-548">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-548">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="00d02-549">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="00d02-549">The help text must not exceed 250 characters.</span></span>

## <a name="method-hidefirstentry"></a><span data-ttu-id="00d02-550">メソッド hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="00d02-550">Method hideFirstEntry</span></span>

```xpp
public boolean hideFirstEntry([boolean value])
```

### <a name="parameters---hidefirstentry"></a><span data-ttu-id="00d02-551">パラメーター - hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="00d02-551">Parameters - hideFirstEntry</span></span>

<span data-ttu-id="00d02-552">値</span><span class="sxs-lookup"><span data-stu-id="00d02-552">value</span></span>  

### <a name="return-value---hidefirstentry"></a><span data-ttu-id="00d02-553">戻り値 - hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="00d02-553">Return Value - hideFirstEntry</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="00d02-554">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="00d02-554">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="00d02-555">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="00d02-555">Parameters - hierarchyParent</span></span>

<span data-ttu-id="00d02-556">値</span><span class="sxs-lookup"><span data-stu-id="00d02-556">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="00d02-557">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="00d02-557">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="00d02-558">メソッド id</span><span class="sxs-lookup"><span data-stu-id="00d02-558">Method id</span></span>

<span data-ttu-id="00d02-559">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="00d02-559">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="00d02-560">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="00d02-560">Return Value - id</span></span>

<span data-ttu-id="00d02-561">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="00d02-561">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="00d02-562">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="00d02-562">Method isContainer</span></span>

<span data-ttu-id="00d02-563">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="00d02-563">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="00d02-564">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="00d02-564">Return Value - isContainer</span></span>

<span data-ttu-id="00d02-565">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="00d02-565">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="00d02-566">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="00d02-566">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="00d02-567">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="00d02-567">Parameters - italic</span></span>

<span data-ttu-id="00d02-568">値</span><span class="sxs-lookup"><span data-stu-id="00d02-568">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="00d02-569">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="00d02-569">Return Value - italic</span></span>

## <a name="method-item"></a><span data-ttu-id="00d02-570">メソッド item</span><span class="sxs-lookup"><span data-stu-id="00d02-570">Method item</span></span>

```xpp
public int item([int value])
```

### <a name="parameters---item"></a><span data-ttu-id="00d02-571">パラメーター - item</span><span class="sxs-lookup"><span data-stu-id="00d02-571">Parameters - item</span></span>

<span data-ttu-id="00d02-572">値</span><span class="sxs-lookup"><span data-stu-id="00d02-572">value</span></span>  

### <a name="return-value---item"></a><span data-ttu-id="00d02-573">戻り値 - item</span><span class="sxs-lookup"><span data-stu-id="00d02-573">Return Value - item</span></span>

## <a name="method-items"></a><span data-ttu-id="00d02-574">メソッド items</span><span class="sxs-lookup"><span data-stu-id="00d02-574">Method items</span></span>

```xpp
public int items([int value])
```

### <a name="parameters---items"></a><span data-ttu-id="00d02-575">パラメーター - items</span><span class="sxs-lookup"><span data-stu-id="00d02-575">Parameters - items</span></span>

<span data-ttu-id="00d02-576">値</span><span class="sxs-lookup"><span data-stu-id="00d02-576">value</span></span>  

### <a name="return-value---items"></a><span data-ttu-id="00d02-577">戻り値 - items</span><span class="sxs-lookup"><span data-stu-id="00d02-577">Return Value - items</span></span>

## <a name="method-label"></a><span data-ttu-id="00d02-578">メソッド label</span><span class="sxs-lookup"><span data-stu-id="00d02-578">Method label</span></span>

<span data-ttu-id="00d02-579">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-579">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="00d02-580">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="00d02-580">Parameters - label</span></span>

<span data-ttu-id="00d02-581">値</span><span class="sxs-lookup"><span data-stu-id="00d02-581">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="00d02-582">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="00d02-582">Return Value - label</span></span>

<span data-ttu-id="00d02-583">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="00d02-583">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="00d02-584">備考 - label</span><span class="sxs-lookup"><span data-stu-id="00d02-584">Remarks - label</span></span>

<span data-ttu-id="00d02-585">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-585">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="00d02-586">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="00d02-586">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="00d02-587">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="00d02-587">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="00d02-588">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="00d02-588">Parameters - labelAlignment</span></span>

<span data-ttu-id="00d02-589">値</span><span class="sxs-lookup"><span data-stu-id="00d02-589">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="00d02-590">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="00d02-590">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="00d02-591">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="00d02-591">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="00d02-592">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="00d02-592">Parameters - labelBold</span></span>

<span data-ttu-id="00d02-593">値</span><span class="sxs-lookup"><span data-stu-id="00d02-593">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="00d02-594">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="00d02-594">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="00d02-595">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="00d02-595">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="00d02-596">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="00d02-596">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="00d02-597">値</span><span class="sxs-lookup"><span data-stu-id="00d02-597">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="00d02-598">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="00d02-598">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="00d02-599">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="00d02-599">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="00d02-600">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="00d02-600">Parameters - labelFont</span></span>

<span data-ttu-id="00d02-601">値</span><span class="sxs-lookup"><span data-stu-id="00d02-601">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="00d02-602">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="00d02-602">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="00d02-603">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="00d02-603">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="00d02-604">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="00d02-604">Parameters - labelFontSize</span></span>

<span data-ttu-id="00d02-605">値</span><span class="sxs-lookup"><span data-stu-id="00d02-605">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="00d02-606">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="00d02-606">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="00d02-607">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="00d02-607">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="00d02-608">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="00d02-608">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="00d02-609">値</span><span class="sxs-lookup"><span data-stu-id="00d02-609">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="00d02-610">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="00d02-610">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="00d02-611">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="00d02-611">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="00d02-612">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="00d02-612">Parameters - labelGuide</span></span>

<span data-ttu-id="00d02-613">値</span><span class="sxs-lookup"><span data-stu-id="00d02-613">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="00d02-614">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="00d02-614">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="00d02-615">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="00d02-615">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="00d02-616">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="00d02-616">Parameters - labelHeight</span></span>

<span data-ttu-id="00d02-617">値</span><span class="sxs-lookup"><span data-stu-id="00d02-617">value</span></span>  

<!-- -->

<span data-ttu-id="00d02-618">モード</span><span class="sxs-lookup"><span data-stu-id="00d02-618">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="00d02-619">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="00d02-619">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="00d02-620">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="00d02-620">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="00d02-621">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="00d02-621">Parameters - labelHeightMode</span></span>

<span data-ttu-id="00d02-622">値</span><span class="sxs-lookup"><span data-stu-id="00d02-622">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="00d02-623">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="00d02-623">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="00d02-624">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="00d02-624">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="00d02-625">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="00d02-625">Parameters - labelHeightValue</span></span>

<span data-ttu-id="00d02-626">値</span><span class="sxs-lookup"><span data-stu-id="00d02-626">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="00d02-627">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="00d02-627">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="00d02-628">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="00d02-628">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="00d02-629">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="00d02-629">Parameters - labelItalic</span></span>

<span data-ttu-id="00d02-630">値</span><span class="sxs-lookup"><span data-stu-id="00d02-630">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="00d02-631">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="00d02-631">Return Value - labelItalic</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="00d02-632">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="00d02-632">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="00d02-633">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="00d02-633">Parameters - labelPosition</span></span>

<span data-ttu-id="00d02-634">値</span><span class="sxs-lookup"><span data-stu-id="00d02-634">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="00d02-635">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="00d02-635">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="00d02-636">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="00d02-636">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="00d02-637">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="00d02-637">Parameters - labelUnderline</span></span>

<span data-ttu-id="00d02-638">値</span><span class="sxs-lookup"><span data-stu-id="00d02-638">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="00d02-639">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="00d02-639">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="00d02-640">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="00d02-640">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="00d02-641">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="00d02-641">Parameters - labelWidth</span></span>

<span data-ttu-id="00d02-642">値</span><span class="sxs-lookup"><span data-stu-id="00d02-642">value</span></span>  

<!-- -->

<span data-ttu-id="00d02-643">モード</span><span class="sxs-lookup"><span data-stu-id="00d02-643">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="00d02-644">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="00d02-644">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="00d02-645">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="00d02-645">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="00d02-646">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="00d02-646">Parameters - labelWidthMode</span></span>

<span data-ttu-id="00d02-647">値</span><span class="sxs-lookup"><span data-stu-id="00d02-647">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="00d02-648">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="00d02-648">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="00d02-649">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="00d02-649">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="00d02-650">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="00d02-650">Parameters - labelWidthValue</span></span>

<span data-ttu-id="00d02-651">値</span><span class="sxs-lookup"><span data-stu-id="00d02-651">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="00d02-652">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="00d02-652">Return Value - labelWidthValue</span></span>

## <a name="method-left"></a><span data-ttu-id="00d02-653">メソッド left</span><span class="sxs-lookup"><span data-stu-id="00d02-653">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="00d02-654">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="00d02-654">Parameters - left</span></span>

<span data-ttu-id="00d02-655">値</span><span class="sxs-lookup"><span data-stu-id="00d02-655">value</span></span>  

<!-- -->

<span data-ttu-id="00d02-656">モード</span><span class="sxs-lookup"><span data-stu-id="00d02-656">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="00d02-657">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="00d02-657">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="00d02-658">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="00d02-658">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="00d02-659">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="00d02-659">Parameters - leftMode</span></span>

<span data-ttu-id="00d02-660">値</span><span class="sxs-lookup"><span data-stu-id="00d02-660">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="00d02-661">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="00d02-661">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="00d02-662">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="00d02-662">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="00d02-663">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="00d02-663">Parameters - leftValue</span></span>

<span data-ttu-id="00d02-664">値</span><span class="sxs-lookup"><span data-stu-id="00d02-664">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="00d02-665">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="00d02-665">Return Value - leftValue</span></span>

## <a name="method-name"></a><span data-ttu-id="00d02-666">メソッド名</span><span class="sxs-lookup"><span data-stu-id="00d02-666">Method name</span></span>

<span data-ttu-id="00d02-667">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-667">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="00d02-668">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="00d02-668">Parameters - name</span></span>

<span data-ttu-id="00d02-669">値</span><span class="sxs-lookup"><span data-stu-id="00d02-669">value</span></span>  
<span data-ttu-id="00d02-670">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="00d02-670">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="00d02-671">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="00d02-671">Return Value - name</span></span>

<span data-ttu-id="00d02-672">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="00d02-672">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="00d02-673">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="00d02-673">Remarks - name</span></span>

<span data-ttu-id="00d02-674">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="00d02-674">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="00d02-675">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="00d02-675">It must start with a letter.</span></span>
-   <span data-ttu-id="00d02-676">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="00d02-676">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="00d02-677">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="00d02-677">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="00d02-678">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="00d02-678">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="00d02-679">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="00d02-679">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="00d02-680">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="00d02-680">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="00d02-681">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="00d02-681">Parameters - neededPermission</span></span>

<span data-ttu-id="00d02-682">値</span><span class="sxs-lookup"><span data-stu-id="00d02-682">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="00d02-683">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="00d02-683">Return Value - neededPermission</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="00d02-684">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="00d02-684">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="00d02-685">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="00d02-685">Parameters - promptrect</span></span>

<span data-ttu-id="00d02-686">値</span><span class="sxs-lookup"><span data-stu-id="00d02-686">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="00d02-687">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="00d02-687">Return Value - promptrect</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="00d02-688">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="00d02-688">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="00d02-689">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="00d02-689">Parameters - securityKey</span></span>

<span data-ttu-id="00d02-690">値</span><span class="sxs-lookup"><span data-stu-id="00d02-690">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="00d02-691">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="00d02-691">Return Value - securityKey</span></span>

## <a name="method-selection"></a><span data-ttu-id="00d02-692">メソッド selection</span><span class="sxs-lookup"><span data-stu-id="00d02-692">Method selection</span></span>

```xpp
public int selection([int value])
```

### <a name="parameters---selection"></a><span data-ttu-id="00d02-693">パラメーター - selection</span><span class="sxs-lookup"><span data-stu-id="00d02-693">Parameters - selection</span></span>

<span data-ttu-id="00d02-694">値</span><span class="sxs-lookup"><span data-stu-id="00d02-694">value</span></span>  

### <a name="return-value---selection"></a><span data-ttu-id="00d02-695">戻り値 - selection</span><span class="sxs-lookup"><span data-stu-id="00d02-695">Return Value - selection</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="00d02-696">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="00d02-696">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="00d02-697">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="00d02-697">Parameters - showLabel</span></span>

<span data-ttu-id="00d02-698">値</span><span class="sxs-lookup"><span data-stu-id="00d02-698">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="00d02-699">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="00d02-699">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="00d02-700">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="00d02-700">Method skip</span></span>

<span data-ttu-id="00d02-701">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="00d02-701">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="00d02-702">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="00d02-702">Parameters - skip</span></span>

<span data-ttu-id="00d02-703">値</span><span class="sxs-lookup"><span data-stu-id="00d02-703">value</span></span>  
<span data-ttu-id="00d02-704">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="00d02-704">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="00d02-705">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="00d02-705">Return Value - skip</span></span>

<span data-ttu-id="00d02-706">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="00d02-706">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-text"></a><span data-ttu-id="00d02-707">メソッド text</span><span class="sxs-lookup"><span data-stu-id="00d02-707">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="00d02-708">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="00d02-708">Parameters - text</span></span>

<span data-ttu-id="00d02-709">値</span><span class="sxs-lookup"><span data-stu-id="00d02-709">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="00d02-710">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="00d02-710">Return Value - text</span></span>

## <a name="method-top"></a><span data-ttu-id="00d02-711">メソッド top</span><span class="sxs-lookup"><span data-stu-id="00d02-711">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="00d02-712">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="00d02-712">Parameters - top</span></span>

<span data-ttu-id="00d02-713">値</span><span class="sxs-lookup"><span data-stu-id="00d02-713">value</span></span>  

<!-- -->

<span data-ttu-id="00d02-714">モード</span><span class="sxs-lookup"><span data-stu-id="00d02-714">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="00d02-715">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="00d02-715">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="00d02-716">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="00d02-716">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="00d02-717">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="00d02-717">Parameters - topMode</span></span>

<span data-ttu-id="00d02-718">値</span><span class="sxs-lookup"><span data-stu-id="00d02-718">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="00d02-719">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="00d02-719">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="00d02-720">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="00d02-720">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="00d02-721">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="00d02-721">Parameters - topValue</span></span>

<span data-ttu-id="00d02-722">値</span><span class="sxs-lookup"><span data-stu-id="00d02-722">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="00d02-723">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="00d02-723">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="00d02-724">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="00d02-724">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="00d02-725">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="00d02-725">Parameters - type</span></span>

<span data-ttu-id="00d02-726">値</span><span class="sxs-lookup"><span data-stu-id="00d02-726">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="00d02-727">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="00d02-727">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="00d02-728">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="00d02-728">Method underline</span></span>

<span data-ttu-id="00d02-729">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="00d02-729">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="00d02-730">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="00d02-730">Parameters - underline</span></span>

<span data-ttu-id="00d02-731">値</span><span class="sxs-lookup"><span data-stu-id="00d02-731">value</span></span>  
<span data-ttu-id="00d02-732">コントロールの underline プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="00d02-732">The value to assign to the underline property of the control; optional.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="00d02-733">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="00d02-733">Return Value - underline</span></span>

<span data-ttu-id="00d02-734">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="00d02-734">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-userdata"></a><span data-ttu-id="00d02-735">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="00d02-735">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="00d02-736">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="00d02-736">Parameters - userData</span></span>

<span data-ttu-id="00d02-737">値</span><span class="sxs-lookup"><span data-stu-id="00d02-737">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="00d02-738">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="00d02-738">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="00d02-739">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="00d02-739">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="00d02-740">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="00d02-740">Parameters - userDataItem</span></span>

<span data-ttu-id="00d02-741">値</span><span class="sxs-lookup"><span data-stu-id="00d02-741">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="00d02-742">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="00d02-742">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="00d02-743">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="00d02-743">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="00d02-744">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="00d02-744">Parameters - userDataItems</span></span>

<span data-ttu-id="00d02-745">値</span><span class="sxs-lookup"><span data-stu-id="00d02-745">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="00d02-746">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="00d02-746">Return Value - userDataItems</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="00d02-747">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="00d02-747">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="00d02-748">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="00d02-748">Parameters - verticalSpacing</span></span>

<span data-ttu-id="00d02-749">値</span><span class="sxs-lookup"><span data-stu-id="00d02-749">value</span></span>  

<!-- -->

<span data-ttu-id="00d02-750">モード</span><span class="sxs-lookup"><span data-stu-id="00d02-750">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="00d02-751">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="00d02-751">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="00d02-752">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="00d02-752">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="00d02-753">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="00d02-753">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="00d02-754">モード</span><span class="sxs-lookup"><span data-stu-id="00d02-754">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="00d02-755">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="00d02-755">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="00d02-756">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="00d02-756">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="00d02-757">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="00d02-757">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="00d02-758">値</span><span class="sxs-lookup"><span data-stu-id="00d02-758">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="00d02-759">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="00d02-759">Return Value - verticalSpacingValue</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="00d02-760">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="00d02-760">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="00d02-761">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="00d02-761">Parameters - viewEditMode</span></span>

<span data-ttu-id="00d02-762">値</span><span class="sxs-lookup"><span data-stu-id="00d02-762">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="00d02-763">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="00d02-763">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="00d02-764">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="00d02-764">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="00d02-765">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="00d02-765">Parameters - visible</span></span>

<span data-ttu-id="00d02-766">値</span><span class="sxs-lookup"><span data-stu-id="00d02-766">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="00d02-767">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="00d02-767">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="00d02-768">メソッド width</span><span class="sxs-lookup"><span data-stu-id="00d02-768">Method width</span></span>

<span data-ttu-id="00d02-769">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-769">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="00d02-770">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="00d02-770">Parameters - width</span></span>

<span data-ttu-id="00d02-771">値</span><span class="sxs-lookup"><span data-stu-id="00d02-771">value</span></span>  

<!-- -->

<span data-ttu-id="00d02-772">モード</span><span class="sxs-lookup"><span data-stu-id="00d02-772">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="00d02-773">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="00d02-773">Return Value - width</span></span>

<span data-ttu-id="00d02-774">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="00d02-774">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="00d02-775">備考 - width</span><span class="sxs-lookup"><span data-stu-id="00d02-775">Remarks - width</span></span>

<span data-ttu-id="00d02-776">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="00d02-776">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="00d02-777">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="00d02-777">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="00d02-778">モード。</span><span class="sxs-lookup"><span data-stu-id="00d02-778">Mode.</span></span>           | <span data-ttu-id="00d02-779">幅計算。</span><span class="sxs-lookup"><span data-stu-id="00d02-779">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d02-780">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="00d02-780">-1 Exact.</span></span>       | <span data-ttu-id="00d02-781">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="00d02-781">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="00d02-782">0 自動。</span><span class="sxs-lookup"><span data-stu-id="00d02-782">0 Auto.</span></span>         | <span data-ttu-id="00d02-783">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="00d02-783">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="00d02-784">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="00d02-784">1 Column width.</span></span> | <span data-ttu-id="00d02-785">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="00d02-785">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="00d02-786">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="00d02-786">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="00d02-787">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="00d02-787">Method widthMode</span></span>

<span data-ttu-id="00d02-788">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-788">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="00d02-789">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="00d02-789">Parameters - widthMode</span></span>

<span data-ttu-id="00d02-790">値</span><span class="sxs-lookup"><span data-stu-id="00d02-790">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="00d02-791">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="00d02-791">Return Value - widthMode</span></span>

<span data-ttu-id="00d02-792">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="00d02-792">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="00d02-793">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="00d02-793">Remarks - widthMode</span></span>

<span data-ttu-id="00d02-794">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="00d02-794">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="00d02-795">モード。</span><span class="sxs-lookup"><span data-stu-id="00d02-795">Mode.</span></span>         | <span data-ttu-id="00d02-796">幅計算。</span><span class="sxs-lookup"><span data-stu-id="00d02-796">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d02-797">正確。</span><span class="sxs-lookup"><span data-stu-id="00d02-797">Exact.</span></span>        | <span data-ttu-id="00d02-798">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="00d02-798">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="00d02-799">自動。</span><span class="sxs-lookup"><span data-stu-id="00d02-799">Auto.</span></span>         | <span data-ttu-id="00d02-800">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="00d02-800">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="00d02-801">列の幅。</span><span class="sxs-lookup"><span data-stu-id="00d02-801">Column width.</span></span> | <span data-ttu-id="00d02-802">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="00d02-802">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="00d02-803">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="00d02-803">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="00d02-804">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="00d02-804">Method widthValue</span></span>

<span data-ttu-id="00d02-805">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="00d02-805">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="00d02-806">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="00d02-806">Parameters - widthValue</span></span>

<span data-ttu-id="00d02-807">値</span><span class="sxs-lookup"><span data-stu-id="00d02-807">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="00d02-808">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="00d02-808">Return Value - widthValue</span></span>

<span data-ttu-id="00d02-809">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="00d02-809">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="00d02-810">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="00d02-810">Remarks - widthValue</span></span>

<span data-ttu-id="00d02-811">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="00d02-811">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="00d02-812">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="00d02-812">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="00d02-813">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="00d02-813">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="00d02-814">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="00d02-814">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="00d02-815">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="00d02-815">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="00d02-816">overrideObject</span><span class="sxs-lookup"><span data-stu-id="00d02-816">overrideObject</span></span>  

