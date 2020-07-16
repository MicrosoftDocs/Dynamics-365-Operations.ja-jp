---
title: FormBuildDateControl クラス
description: このトピックでは、FormBuildDateControl クラスについて説明します。
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
ms.openlocfilehash: 50ca2b97f41251eff65dde0772bfc65f4d39fedc
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502968"
---
# <a name="class-formbuilddatecontrol"></a><span data-ttu-id="6bbee-103">クラス FormBuildDateControl</span><span class="sxs-lookup"><span data-stu-id="6bbee-103">Class FormBuildDateControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildDateControl extends FormBuildControl
```

<span data-ttu-id="6bbee-104">FormBuildDateControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-104">The FormBuildDateControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bbee-105">備考</span><span class="sxs-lookup"><span data-stu-id="6bbee-105">Remarks</span></span>

<span data-ttu-id="6bbee-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="6bbee-107">例</span><span class="sxs-lookup"><span data-stu-id="6bbee-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="6bbee-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="6bbee-108">Methods</span></span>

| <span data-ttu-id="6bbee-109">方法</span><span class="sxs-lookup"><span data-stu-id="6bbee-109">Method</span></span>                                                                                                      | <span data-ttu-id="6bbee-110">説明</span><span class="sxs-lookup"><span data-stu-id="6bbee-110">Description</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bbee-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="6bbee-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-112">Determines whether to align the control.</span></span>                                                                                                      |
| <span data-ttu-id="6bbee-113">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-113">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                               |
| <span data-ttu-id="6bbee-114">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-114">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="6bbee-115">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-115">Determines whether the user can change the contents of the control.</span></span>                                                                           |
| <span data-ttu-id="6bbee-116">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-116">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                               |
| <span data-ttu-id="6bbee-117">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-117">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="6bbee-118">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-118">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                            |
| <span data-ttu-id="6bbee-119">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-119">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="6bbee-120">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-120">Gets or sets the background color of the control.</span></span>                                                                                             |
| <span data-ttu-id="6bbee-121">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-121">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="6bbee-122">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-122">Determines whether the control background can be transparent.</span></span>                                                                                 |
| <span data-ttu-id="6bbee-123">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-123">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="6bbee-124">コントロール内のテキストを出力するのに使用されたフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-124">Gets or sets the weight of font that was used to output text in the control.</span></span>                                                                  |
| <span data-ttu-id="6bbee-125">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-125">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="6bbee-126">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-126">Gets or sets the style of the borderline of the control.</span></span>                                                                                      |
| <span data-ttu-id="6bbee-127">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-127">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="6bbee-128">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-128">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="6bbee-129">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-129">Gets or sets the character set of the font.</span></span>                                                                                                   |
| <span data-ttu-id="6bbee-130">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-130">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="6bbee-131">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-131">Gets or sets the color scheme of the control.</span></span>                                                                                                 |
| <span data-ttu-id="6bbee-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="6bbee-133">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-133">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                           |
| <span data-ttu-id="6bbee-134">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="6bbee-134">public int containerId()</span></span>                                                                                    | <span data-ttu-id="6bbee-135">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-135">Retrieves the ID of the parent container for the control.</span></span>                                                                                     |
| <span data-ttu-id="6bbee-136">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-136">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                               |
| <span data-ttu-id="6bbee-137">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-137">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                               |
| <span data-ttu-id="6bbee-138">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-138">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                               |
| <span data-ttu-id="6bbee-139">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-139">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                               |
| <span data-ttu-id="6bbee-140">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-140">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="6bbee-141">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-141">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="6bbee-142">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-142">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                      |
| <span data-ttu-id="6bbee-143">public int dateDay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-143">public int dateDay(\[int value\])</span></span>                                                                           |                                                                                                                                               |
| <span data-ttu-id="6bbee-144">public int dateFormat(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-144">public int dateFormat(\[int value\])</span></span>                                                                        |                                                                                                                                               |
| <span data-ttu-id="6bbee-145">public int dateMonth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-145">public int dateMonth(\[int value\])</span></span>                                                                         |                                                                                                                                               |
| <span data-ttu-id="6bbee-146">public int dateSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-146">public int dateSeparator(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="6bbee-147">public Date dateValue(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-147">public Date dateValue(\[Date value\])</span></span>                                                                       |                                                                                                                                               |
| <span data-ttu-id="6bbee-148">public int dateYear(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-148">public int dateYear(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="6bbee-149">public int direction(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-149">public int direction(\[int value\])</span></span>                                                                         |                                                                                                                                               |
| <span data-ttu-id="6bbee-150">public int displayHeight(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-150">public int displayHeight(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                               |
| <span data-ttu-id="6bbee-151">public AutoMode displayHeightMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-151">public AutoMode displayHeightMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                               |
| <span data-ttu-id="6bbee-152">public int displayHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-152">public int displayHeightValue(\[int value\])</span></span>                                                                |                                                                                                                                               |
| <span data-ttu-id="6bbee-153">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-153">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                               |
| <span data-ttu-id="6bbee-154">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-154">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                               |
| <span data-ttu-id="6bbee-155">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-155">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                               |
| <span data-ttu-id="6bbee-156">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-156">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="6bbee-157">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-157">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="6bbee-158">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-158">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                             |
| <span data-ttu-id="6bbee-159">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-159">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="6bbee-160">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-160">Determines whether to enable or disable the object.</span></span>                                                                                           |
| <span data-ttu-id="6bbee-161">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-161">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                               |
| <span data-ttu-id="6bbee-162">public int fastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-162">public int fastTabSummary(\[int value\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="6bbee-163">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-163">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="6bbee-164">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-164">Gets or sets the name of the font for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="6bbee-165">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-165">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="6bbee-166">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-166">Gets or sets the size of the font for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="6bbee-167">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-167">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="6bbee-168">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-168">Gets or sets the text color for the control to use.</span></span>                                                                                           |
| <span data-ttu-id="6bbee-169">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-169">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="6bbee-170">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-170">Gets or sets the height of the control.</span></span>                                                                                                       |
| <span data-ttu-id="6bbee-171">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-171">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="6bbee-172">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-172">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                |
| <span data-ttu-id="6bbee-173">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-173">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="6bbee-174">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-174">Gets or sets the height of the control.</span></span>                                                                                                       |
| <span data-ttu-id="6bbee-175">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-175">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="6bbee-176">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-176">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="6bbee-177">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-177">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="6bbee-178">public int id()</span><span class="sxs-lookup"><span data-stu-id="6bbee-178">public int id()</span></span>                                                                                             | <span data-ttu-id="6bbee-179">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-179">Retrieves the ID of the control.</span></span>                                                                                                              |
| <span data-ttu-id="6bbee-180">public int iMEMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-180">public int iMEMode(\[int value\])</span></span>                                                                           |                                                                                                                                               |
| <span data-ttu-id="6bbee-181">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="6bbee-181">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="6bbee-182">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-182">Retrieves a value that indicates whether the control is a container control.</span></span>                                                                  |
| <span data-ttu-id="6bbee-183">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-183">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="6bbee-184">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-184">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="6bbee-185">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-185">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="6bbee-186">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-186">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="6bbee-187">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-187">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                               |
| <span data-ttu-id="6bbee-188">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-188">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                               |
| <span data-ttu-id="6bbee-189">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-189">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                               |
| <span data-ttu-id="6bbee-190">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-190">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="6bbee-191">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-191">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                               |
| <span data-ttu-id="6bbee-192">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-192">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                               |
| <span data-ttu-id="6bbee-193">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-193">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                               |
| <span data-ttu-id="6bbee-194">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-194">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="6bbee-195">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-195">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="6bbee-196">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-196">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                               |
| <span data-ttu-id="6bbee-197">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-197">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="6bbee-198">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-198">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                               |
| <span data-ttu-id="6bbee-199">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-199">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                               |
| <span data-ttu-id="6bbee-200">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-200">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="6bbee-201">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-201">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="6bbee-202">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-202">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="6bbee-203">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-203">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="6bbee-204">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-204">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                               |
| <span data-ttu-id="6bbee-205">public int limitText(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-205">public int limitText(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                               |
| <span data-ttu-id="6bbee-206">public AutoMode limitTextMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-206">public AutoMode limitTextMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                               |
| <span data-ttu-id="6bbee-207">public int limitTextValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-207">public int limitTextValue(\[int value\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="6bbee-208">public int lookupButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-208">public int lookupButton(\[int value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="6bbee-209">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-209">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                               |
| <span data-ttu-id="6bbee-210">public str maxDateLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-210">public str maxDateLabel(\[str value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="6bbee-211">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-211">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="6bbee-212">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-212">Gets or sets the name that is used in the code to identify a form, report, table, query, or another application object.</span></span> |
| <span data-ttu-id="6bbee-213">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-213">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="6bbee-214">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-214">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                               |
| <span data-ttu-id="6bbee-215">public boolean replaceOnLookup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-215">public boolean replaceOnLookup(\[boolean value\])</span></span>                                                           |                                                                                                                                               |
| <span data-ttu-id="6bbee-216">public int searchAfterInput(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-216">public int searchAfterInput(\[int value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="6bbee-217">public int searchMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-217">public int searchMode(\[int value\])</span></span>                                                                        |                                                                                                                                               |
| <span data-ttu-id="6bbee-218">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-218">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                               |
| <span data-ttu-id="6bbee-219">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-219">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                               |
| <span data-ttu-id="6bbee-220">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-220">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="6bbee-221">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-221">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>               |
| <span data-ttu-id="6bbee-222">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-222">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                               |
| <span data-ttu-id="6bbee-223">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-223">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="6bbee-224">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-224">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                               |
| <span data-ttu-id="6bbee-225">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-225">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="6bbee-226">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-226">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                               |
| <span data-ttu-id="6bbee-227">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-227">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="6bbee-228">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-228">Sets or returns the underline property for the text in the control.</span></span>                                                                           |
| <span data-ttu-id="6bbee-229">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-229">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="6bbee-230">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-230">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="6bbee-231">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-231">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="6bbee-232">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-232">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                               |
| <span data-ttu-id="6bbee-233">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-233">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                               |
| <span data-ttu-id="6bbee-234">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-234">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                               |
| <span data-ttu-id="6bbee-235">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-235">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="6bbee-236">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-236">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="6bbee-237">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-237">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="6bbee-238">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-238">Gets or sets the width of the control.</span></span>                                                                                                        |
| <span data-ttu-id="6bbee-239">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-239">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="6bbee-240">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-240">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                |
| <span data-ttu-id="6bbee-241">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-241">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="6bbee-242">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-242">Gets or sets the width of the control.</span></span>                                                                                                        |
| <span data-ttu-id="6bbee-243">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="6bbee-243">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                               |

## <a name="method-aligncontrol"></a><span data-ttu-id="6bbee-244">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="6bbee-244">Method alignControl</span></span>

<span data-ttu-id="6bbee-245">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-245">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="6bbee-246">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="6bbee-246">Parameters - alignControl</span></span>

<span data-ttu-id="6bbee-247">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-247">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="6bbee-248">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="6bbee-248">Return Value - alignControl</span></span>

<span data-ttu-id="6bbee-249">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="6bbee-249">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="6bbee-250">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="6bbee-250">Remarks - alignControl</span></span>

<span data-ttu-id="6bbee-251">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-251">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="6bbee-252">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="6bbee-252">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="6bbee-253">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="6bbee-253">Parameters - alignment</span></span>

<span data-ttu-id="6bbee-254">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-254">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="6bbee-255">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="6bbee-255">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="6bbee-256">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="6bbee-256">Method allowEdit</span></span>

<span data-ttu-id="6bbee-257">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-257">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="6bbee-258">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="6bbee-258">Parameters - allowEdit</span></span>

<span data-ttu-id="6bbee-259">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-259">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="6bbee-260">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="6bbee-260">Return Value - allowEdit</span></span>

<span data-ttu-id="6bbee-261">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6bbee-261">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="6bbee-262">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="6bbee-262">Remarks - allowEdit</span></span>

<span data-ttu-id="6bbee-263">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="6bbee-263">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="6bbee-264">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="6bbee-264">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="6bbee-265">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="6bbee-265">Parameters - arrayIndex</span></span>

<span data-ttu-id="6bbee-266">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-266">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="6bbee-267">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="6bbee-267">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="6bbee-268">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6bbee-268">Method autoDeclaration</span></span>

<span data-ttu-id="6bbee-269">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-269">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="6bbee-270">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6bbee-270">Parameters - autoDeclaration</span></span>

<span data-ttu-id="6bbee-271">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-271">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="6bbee-272">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6bbee-272">Return Value - autoDeclaration</span></span>

<span data-ttu-id="6bbee-273">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6bbee-273">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="6bbee-274">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6bbee-274">Remarks - autoDeclaration</span></span>

<span data-ttu-id="6bbee-275">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="6bbee-275">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="6bbee-276">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="6bbee-276">Method backgroundColor</span></span>

<span data-ttu-id="6bbee-277">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-277">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="6bbee-278">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="6bbee-278">Parameters - backgroundColor</span></span>

<span data-ttu-id="6bbee-279">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-279">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="6bbee-280">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="6bbee-280">Return Value - backgroundColor</span></span>

<span data-ttu-id="6bbee-281">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="6bbee-281">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="6bbee-282">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="6bbee-282">Remarks - backgroundColor</span></span>

<span data-ttu-id="6bbee-283">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-283">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="6bbee-284">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6bbee-284">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="6bbee-285">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="6bbee-285">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="6bbee-286">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="6bbee-286">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="6bbee-287">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6bbee-287">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="6bbee-288">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="6bbee-288">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="6bbee-289">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="6bbee-289">Method backStyle</span></span>

<span data-ttu-id="6bbee-290">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-290">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="6bbee-291">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="6bbee-291">Parameters - backStyle</span></span>

<span data-ttu-id="6bbee-292">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-292">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="6bbee-293">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="6bbee-293">Return Value - backStyle</span></span>

<span data-ttu-id="6bbee-294">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="6bbee-294">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="6bbee-295">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="6bbee-295">Method bold</span></span>

<span data-ttu-id="6bbee-296">コントロール内のテキストを出力するのに使用されたフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-296">Gets or sets the weight of font that was used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="6bbee-297">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="6bbee-297">Parameters - bold</span></span>

<span data-ttu-id="6bbee-298">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-298">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="6bbee-299">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="6bbee-299">Return Value - bold</span></span>

<span data-ttu-id="6bbee-300">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="6bbee-300">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="6bbee-301">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="6bbee-301">Remarks - bold</span></span>

<span data-ttu-id="6bbee-302">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-302">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="6bbee-303">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-303">0 Use the default font weight.</span></span>
-   <span data-ttu-id="6bbee-304">1 シン。</span><span class="sxs-lookup"><span data-stu-id="6bbee-304">1 Thin.</span></span>
-   <span data-ttu-id="6bbee-305">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="6bbee-305">2 Extra-light.</span></span>
-   <span data-ttu-id="6bbee-306">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="6bbee-306">3 Light.</span></span>
-   <span data-ttu-id="6bbee-307">4 標準。</span><span class="sxs-lookup"><span data-stu-id="6bbee-307">4 Normal.</span></span>
-   <span data-ttu-id="6bbee-308">5 中。</span><span class="sxs-lookup"><span data-stu-id="6bbee-308">5 Medium.</span></span>
-   <span data-ttu-id="6bbee-309">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="6bbee-309">6 Semibold.</span></span>
-   <span data-ttu-id="6bbee-310">7 太字。</span><span class="sxs-lookup"><span data-stu-id="6bbee-310">7 Bold.</span></span>
-   <span data-ttu-id="6bbee-311">8 極太。</span><span class="sxs-lookup"><span data-stu-id="6bbee-311">8 Extra-bold.</span></span>
-   <span data-ttu-id="6bbee-312">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="6bbee-312">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="6bbee-313">メソッド border</span><span class="sxs-lookup"><span data-stu-id="6bbee-313">Method border</span></span>

<span data-ttu-id="6bbee-314">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-314">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="6bbee-315">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="6bbee-315">Parameters - border</span></span>

<span data-ttu-id="6bbee-316">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-316">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="6bbee-317">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="6bbee-317">Return Value - border</span></span>

<span data-ttu-id="6bbee-318">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="6bbee-318">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="6bbee-319">備考 - border</span><span class="sxs-lookup"><span data-stu-id="6bbee-319">Remarks - border</span></span>

<span data-ttu-id="6bbee-320">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-320">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="6bbee-321">値です。</span><span class="sxs-lookup"><span data-stu-id="6bbee-321">Value.</span></span> | <span data-ttu-id="6bbee-322">説明。</span><span class="sxs-lookup"><span data-stu-id="6bbee-322">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="6bbee-323">0</span><span class="sxs-lookup"><span data-stu-id="6bbee-323">0</span></span>      | <span data-ttu-id="6bbee-324">自動。</span><span class="sxs-lookup"><span data-stu-id="6bbee-324">Auto.</span></span>        |
| <span data-ttu-id="6bbee-325">1</span><span class="sxs-lookup"><span data-stu-id="6bbee-325">1</span></span>      | <span data-ttu-id="6bbee-326">3D。</span><span class="sxs-lookup"><span data-stu-id="6bbee-326">3D.</span></span>          |
| <span data-ttu-id="6bbee-327">2</span><span class="sxs-lookup"><span data-stu-id="6bbee-327">2</span></span>      | <span data-ttu-id="6bbee-328">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="6bbee-328">Single line.</span></span> |
| <span data-ttu-id="6bbee-329">3</span><span class="sxs-lookup"><span data-stu-id="6bbee-329">3</span></span>      | <span data-ttu-id="6bbee-330">均一。</span><span class="sxs-lookup"><span data-stu-id="6bbee-330">Flat.</span></span>        |
| <span data-ttu-id="6bbee-331">4</span><span class="sxs-lookup"><span data-stu-id="6bbee-331">4</span></span>      | <span data-ttu-id="6bbee-332">なし。</span><span class="sxs-lookup"><span data-stu-id="6bbee-332">None.</span></span>        |

## <a name="method-cachedatamethod"></a><span data-ttu-id="6bbee-333">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="6bbee-333">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="6bbee-334">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="6bbee-334">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="6bbee-335">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-335">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="6bbee-336">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="6bbee-336">Return Value - cacheDataMethod</span></span>

## <a name="method-characterset"></a><span data-ttu-id="6bbee-337">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="6bbee-337">Method characterSet</span></span>

<span data-ttu-id="6bbee-338">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-338">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="6bbee-339">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="6bbee-339">Parameters - characterSet</span></span>

<span data-ttu-id="6bbee-340">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-340">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="6bbee-341">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="6bbee-341">Return Value - characterSet</span></span>

<span data-ttu-id="6bbee-342">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bbee-342">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="6bbee-343">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="6bbee-343">Remarks - characterSet</span></span>

<span data-ttu-id="6bbee-344">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-344">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="6bbee-345">値です。</span><span class="sxs-lookup"><span data-stu-id="6bbee-345">Value.</span></span> | <span data-ttu-id="6bbee-346">説明。</span><span class="sxs-lookup"><span data-stu-id="6bbee-346">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="6bbee-347">0</span><span class="sxs-lookup"><span data-stu-id="6bbee-347">0</span></span>      | <span data-ttu-id="6bbee-348">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bbee-348">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="6bbee-349">1</span><span class="sxs-lookup"><span data-stu-id="6bbee-349">1</span></span>      | <span data-ttu-id="6bbee-350">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bbee-350">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="6bbee-351">2</span><span class="sxs-lookup"><span data-stu-id="6bbee-351">2</span></span>      | <span data-ttu-id="6bbee-352">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bbee-352">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="6bbee-353">77</span><span class="sxs-lookup"><span data-stu-id="6bbee-353">77</span></span>     | <span data-ttu-id="6bbee-354">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bbee-354">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="6bbee-355">128</span><span class="sxs-lookup"><span data-stu-id="6bbee-355">128</span></span>    | <span data-ttu-id="6bbee-356">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bbee-356">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="6bbee-357">129</span><span class="sxs-lookup"><span data-stu-id="6bbee-357">129</span></span>    | <span data-ttu-id="6bbee-358">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bbee-358">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="6bbee-359">134</span><span class="sxs-lookup"><span data-stu-id="6bbee-359">134</span></span>    | <span data-ttu-id="6bbee-360">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bbee-360">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="6bbee-361">136</span><span class="sxs-lookup"><span data-stu-id="6bbee-361">136</span></span>    | <span data-ttu-id="6bbee-362">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bbee-362">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="6bbee-363">161</span><span class="sxs-lookup"><span data-stu-id="6bbee-363">161</span></span>    | <span data-ttu-id="6bbee-364">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bbee-364">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="6bbee-365">162</span><span class="sxs-lookup"><span data-stu-id="6bbee-365">162</span></span>    | <span data-ttu-id="6bbee-366">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bbee-366">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="6bbee-367">163</span><span class="sxs-lookup"><span data-stu-id="6bbee-367">163</span></span>    | <span data-ttu-id="6bbee-368">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bbee-368">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="6bbee-369">186</span><span class="sxs-lookup"><span data-stu-id="6bbee-369">186</span></span>    | <span data-ttu-id="6bbee-370">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bbee-370">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="6bbee-371">204</span><span class="sxs-lookup"><span data-stu-id="6bbee-371">204</span></span>    | <span data-ttu-id="6bbee-372">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bbee-372">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="6bbee-373">238</span><span class="sxs-lookup"><span data-stu-id="6bbee-373">238</span></span>    | <span data-ttu-id="6bbee-374">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bbee-374">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="6bbee-375">255</span><span class="sxs-lookup"><span data-stu-id="6bbee-375">255</span></span>    | <span data-ttu-id="6bbee-376">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bbee-376">OEM\_CHARSET</span></span>         |

<span data-ttu-id="6bbee-377">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="6bbee-377">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="6bbee-378">値です。</span><span class="sxs-lookup"><span data-stu-id="6bbee-378">Value.</span></span> | <span data-ttu-id="6bbee-379">説明。</span><span class="sxs-lookup"><span data-stu-id="6bbee-379">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="6bbee-380">130</span><span class="sxs-lookup"><span data-stu-id="6bbee-380">130</span></span>    | <span data-ttu-id="6bbee-381">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bbee-381">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="6bbee-382">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="6bbee-382">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="6bbee-383">値です。</span><span class="sxs-lookup"><span data-stu-id="6bbee-383">Value.</span></span> | <span data-ttu-id="6bbee-384">説明。</span><span class="sxs-lookup"><span data-stu-id="6bbee-384">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="6bbee-385">177</span><span class="sxs-lookup"><span data-stu-id="6bbee-385">177</span></span>    | <span data-ttu-id="6bbee-386">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bbee-386">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="6bbee-387">178</span><span class="sxs-lookup"><span data-stu-id="6bbee-387">178</span></span>    | <span data-ttu-id="6bbee-388">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bbee-388">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="6bbee-389">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="6bbee-389">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="6bbee-390">値です。</span><span class="sxs-lookup"><span data-stu-id="6bbee-390">Value.</span></span> | <span data-ttu-id="6bbee-391">説明。</span><span class="sxs-lookup"><span data-stu-id="6bbee-391">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="6bbee-392">222</span><span class="sxs-lookup"><span data-stu-id="6bbee-392">222</span></span>    | <span data-ttu-id="6bbee-393">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bbee-393">THAI\_CHARSET</span></span> |

<span data-ttu-id="6bbee-394">既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-394">The default character set is set to a value that is based on the current system locale.</span></span> <span data-ttu-id="6bbee-395">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-395">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="6bbee-396">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6bbee-396">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="6bbee-397">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="6bbee-397">Method colorScheme</span></span>

<span data-ttu-id="6bbee-398">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-398">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="6bbee-399">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="6bbee-399">Parameters - colorScheme</span></span>

<span data-ttu-id="6bbee-400">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-400">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="6bbee-401">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="6bbee-401">Return Value - colorScheme</span></span>

<span data-ttu-id="6bbee-402">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="6bbee-402">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="6bbee-403">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="6bbee-403">Remarks - colorScheme</span></span>

<span data-ttu-id="6bbee-404">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-404">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="6bbee-405">値です。</span><span class="sxs-lookup"><span data-stu-id="6bbee-405">Value.</span></span> | <span data-ttu-id="6bbee-406">スタイル。</span><span class="sxs-lookup"><span data-stu-id="6bbee-406">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="6bbee-407">0</span><span class="sxs-lookup"><span data-stu-id="6bbee-407">0</span></span>      | <span data-ttu-id="6bbee-408">既定。</span><span class="sxs-lookup"><span data-stu-id="6bbee-408">Default.</span></span>                       |
| <span data-ttu-id="6bbee-409">1</span><span class="sxs-lookup"><span data-stu-id="6bbee-409">1</span></span>      | <span data-ttu-id="6bbee-410">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="6bbee-410">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="6bbee-411">2</span><span class="sxs-lookup"><span data-stu-id="6bbee-411">2</span></span>      | <span data-ttu-id="6bbee-412">真の配色。</span><span class="sxs-lookup"><span data-stu-id="6bbee-412">The true-color scheme.</span></span>         |

## <a name="method-configurationkey"></a><span data-ttu-id="6bbee-413">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="6bbee-413">Method configurationKey</span></span>

<span data-ttu-id="6bbee-414">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-414">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="6bbee-415">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="6bbee-415">Parameters - configurationKey</span></span>

<span data-ttu-id="6bbee-416">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-416">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="6bbee-417">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="6bbee-417">Return Value - configurationKey</span></span>

<span data-ttu-id="6bbee-418">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="6bbee-418">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="6bbee-419">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="6bbee-419">Remarks - configurationKey</span></span>

<span data-ttu-id="6bbee-420">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-420">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="6bbee-421">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="6bbee-421">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="6bbee-422">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="6bbee-422">Method containerId</span></span>

<span data-ttu-id="6bbee-423">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-423">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="6bbee-424">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="6bbee-424">Return Value - containerId</span></span>

<span data-ttu-id="6bbee-425">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="6bbee-425">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="6bbee-426">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="6bbee-426">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="6bbee-427">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="6bbee-427">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="6bbee-428">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-428">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="6bbee-429">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="6bbee-429">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="6bbee-430">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="6bbee-430">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="6bbee-431">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="6bbee-431">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="6bbee-432">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-432">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="6bbee-433">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="6bbee-433">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="6bbee-434">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="6bbee-434">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="6bbee-435">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="6bbee-435">Parameters - dataField</span></span>

<span data-ttu-id="6bbee-436">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-436">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="6bbee-437">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="6bbee-437">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="6bbee-438">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="6bbee-438">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="6bbee-439">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="6bbee-439">Parameters - dataMethod</span></span>

<span data-ttu-id="6bbee-440">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-440">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="6bbee-441">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="6bbee-441">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="6bbee-442">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="6bbee-442">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="6bbee-443">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="6bbee-443">Parameters - dataRelationPath</span></span>

<span data-ttu-id="6bbee-444">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-444">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="6bbee-445">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="6bbee-445">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="6bbee-446">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="6bbee-446">Method dataSource</span></span>

<span data-ttu-id="6bbee-447">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-447">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="6bbee-448">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="6bbee-448">Parameters - dataSource</span></span>

<span data-ttu-id="6bbee-449">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-449">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="6bbee-450">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="6bbee-450">Return Value - dataSource</span></span>

<span data-ttu-id="6bbee-451">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="6bbee-451">The identifier of the data source that will be used.</span></span>

## <a name="method-dateday"></a><span data-ttu-id="6bbee-452">メソッド dateDay</span><span class="sxs-lookup"><span data-stu-id="6bbee-452">Method dateDay</span></span>

```xpp
public int dateDay([int value])
```

### <a name="parameters---dateday"></a><span data-ttu-id="6bbee-453">パラメーター - dateDay</span><span class="sxs-lookup"><span data-stu-id="6bbee-453">Parameters - dateDay</span></span>

<span data-ttu-id="6bbee-454">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-454">value</span></span>  

### <a name="return-value---dateday"></a><span data-ttu-id="6bbee-455">戻り値 - dateDay</span><span class="sxs-lookup"><span data-stu-id="6bbee-455">Return Value - dateDay</span></span>

## <a name="method-dateformat"></a><span data-ttu-id="6bbee-456">メソッド dateFormat</span><span class="sxs-lookup"><span data-stu-id="6bbee-456">Method dateFormat</span></span>

```xpp
public int dateFormat([int value])
```

### <a name="parameters---dateformat"></a><span data-ttu-id="6bbee-457">パラメーター - dateFormat</span><span class="sxs-lookup"><span data-stu-id="6bbee-457">Parameters - dateFormat</span></span>

<span data-ttu-id="6bbee-458">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-458">value</span></span>  

### <a name="return-value---dateformat"></a><span data-ttu-id="6bbee-459">戻り値 - dateFormat</span><span class="sxs-lookup"><span data-stu-id="6bbee-459">Return Value - dateFormat</span></span>

## <a name="method-datemonth"></a><span data-ttu-id="6bbee-460">メソッド dateMonth</span><span class="sxs-lookup"><span data-stu-id="6bbee-460">Method dateMonth</span></span>

```xpp
public int dateMonth([int value])
```

### <a name="parameters---datemonth"></a><span data-ttu-id="6bbee-461">パラメーター - dateMonth</span><span class="sxs-lookup"><span data-stu-id="6bbee-461">Parameters - dateMonth</span></span>

<span data-ttu-id="6bbee-462">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-462">value</span></span>  

### <a name="return-value---datemonth"></a><span data-ttu-id="6bbee-463">戻り値 - dateMonth</span><span class="sxs-lookup"><span data-stu-id="6bbee-463">Return Value - dateMonth</span></span>

## <a name="method-dateseparator"></a><span data-ttu-id="6bbee-464">メソッド dateSeparator</span><span class="sxs-lookup"><span data-stu-id="6bbee-464">Method dateSeparator</span></span>

```xpp
public int dateSeparator([int value])
```

### <a name="parameters---dateseparator"></a><span data-ttu-id="6bbee-465">パラメーター - dateSeparator</span><span class="sxs-lookup"><span data-stu-id="6bbee-465">Parameters - dateSeparator</span></span>

<span data-ttu-id="6bbee-466">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-466">value</span></span>  

### <a name="return-value---dateseparator"></a><span data-ttu-id="6bbee-467">戻り値 - dateSeparator</span><span class="sxs-lookup"><span data-stu-id="6bbee-467">Return Value - dateSeparator</span></span>

## <a name="method-datevalue"></a><span data-ttu-id="6bbee-468">メソッド dateValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-468">Method dateValue</span></span>

```xpp
public Date dateValue([Date value])
```

### <a name="parameters---datevalue"></a><span data-ttu-id="6bbee-469">パラメーター - dateValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-469">Parameters - dateValue</span></span>

<span data-ttu-id="6bbee-470">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-470">value</span></span>  

### <a name="return-value---datevalue"></a><span data-ttu-id="6bbee-471">戻り値 - dateValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-471">Return Value - dateValue</span></span>

## <a name="method-dateyear"></a><span data-ttu-id="6bbee-472">メソッド dateYear</span><span class="sxs-lookup"><span data-stu-id="6bbee-472">Method dateYear</span></span>

```xpp
public int dateYear([int value])
```

### <a name="parameters---dateyear"></a><span data-ttu-id="6bbee-473">パラメーター - dateYear</span><span class="sxs-lookup"><span data-stu-id="6bbee-473">Parameters - dateYear</span></span>

<span data-ttu-id="6bbee-474">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-474">value</span></span>  

### <a name="return-value---dateyear"></a><span data-ttu-id="6bbee-475">戻り値 - dateYear</span><span class="sxs-lookup"><span data-stu-id="6bbee-475">Return Value - dateYear</span></span>

## <a name="method-direction"></a><span data-ttu-id="6bbee-476">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="6bbee-476">Method direction</span></span>

```xpp
public int direction([int value])
```

### <a name="parameters---direction"></a><span data-ttu-id="6bbee-477">パラメーター - direction</span><span class="sxs-lookup"><span data-stu-id="6bbee-477">Parameters - direction</span></span>

<span data-ttu-id="6bbee-478">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-478">value</span></span>  

### <a name="return-value---direction"></a><span data-ttu-id="6bbee-479">戻り値 - direction</span><span class="sxs-lookup"><span data-stu-id="6bbee-479">Return Value - direction</span></span>

## <a name="method-displayheight"></a><span data-ttu-id="6bbee-480">メソッド displayHeight</span><span class="sxs-lookup"><span data-stu-id="6bbee-480">Method displayHeight</span></span>

```xpp
public int displayHeight([int value], [AutoMode mode])
```

### <a name="parameters---displayheight"></a><span data-ttu-id="6bbee-481">パラメーター - displayHeight</span><span class="sxs-lookup"><span data-stu-id="6bbee-481">Parameters - displayHeight</span></span>

<span data-ttu-id="6bbee-482">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-482">value</span></span>  

<!-- -->

<span data-ttu-id="6bbee-483">モード</span><span class="sxs-lookup"><span data-stu-id="6bbee-483">mode</span></span>  

### <a name="return-value---displayheight"></a><span data-ttu-id="6bbee-484">戻り値 - displayHeight</span><span class="sxs-lookup"><span data-stu-id="6bbee-484">Return Value - displayHeight</span></span>

## <a name="method-displayheightmode"></a><span data-ttu-id="6bbee-485">メソッド displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-485">Method displayHeightMode</span></span>

```xpp
public AutoMode displayHeightMode([AutoMode mode])
```

### <a name="parameters---displayheightmode"></a><span data-ttu-id="6bbee-486">パラメーター - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-486">Parameters - displayHeightMode</span></span>

<span data-ttu-id="6bbee-487">モード</span><span class="sxs-lookup"><span data-stu-id="6bbee-487">mode</span></span>  

### <a name="return-value---displayheightmode"></a><span data-ttu-id="6bbee-488">戻り値 - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-488">Return Value - displayHeightMode</span></span>

## <a name="method-displayheightvalue"></a><span data-ttu-id="6bbee-489">メソッド displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-489">Method displayHeightValue</span></span>

```xpp
public int displayHeightValue([int value])
```

### <a name="parameters---displayheightvalue"></a><span data-ttu-id="6bbee-490">パラメーター - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-490">Parameters - displayHeightValue</span></span>

<span data-ttu-id="6bbee-491">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-491">value</span></span>  

### <a name="return-value---displayheightvalue"></a><span data-ttu-id="6bbee-492">戻り値 - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-492">Return Value - displayHeightValue</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="6bbee-493">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="6bbee-493">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="6bbee-494">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="6bbee-494">Parameters - displayLength</span></span>

<span data-ttu-id="6bbee-495">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-495">value</span></span>  

<!-- -->

<span data-ttu-id="6bbee-496">モード</span><span class="sxs-lookup"><span data-stu-id="6bbee-496">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="6bbee-497">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="6bbee-497">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="6bbee-498">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-498">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="6bbee-499">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-499">Parameters - displayLengthMode</span></span>

<span data-ttu-id="6bbee-500">モード</span><span class="sxs-lookup"><span data-stu-id="6bbee-500">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="6bbee-501">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-501">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="6bbee-502">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-502">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="6bbee-503">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-503">Parameters - displayLengthValue</span></span>

<span data-ttu-id="6bbee-504">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-504">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="6bbee-505">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-505">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="6bbee-506">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="6bbee-506">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="6bbee-507">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="6bbee-507">Parameters - displayTarget</span></span>

<span data-ttu-id="6bbee-508">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-508">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="6bbee-509">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="6bbee-509">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="6bbee-510">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="6bbee-510">Method dragDrop</span></span>

<span data-ttu-id="6bbee-511">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-511">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="6bbee-512">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="6bbee-512">Parameters - dragDrop</span></span>

<span data-ttu-id="6bbee-513">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-513">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="6bbee-514">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="6bbee-514">Return Value - dragDrop</span></span>

<span data-ttu-id="6bbee-515">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="6bbee-515">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="6bbee-516">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="6bbee-516">Method enabled</span></span>

<span data-ttu-id="6bbee-517">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-517">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="6bbee-518">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="6bbee-518">Parameters - enabled</span></span>

<span data-ttu-id="6bbee-519">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-519">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="6bbee-520">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="6bbee-520">Return Value - enabled</span></span>

<span data-ttu-id="6bbee-521">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6bbee-521">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="6bbee-522">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="6bbee-522">Remarks - enabled</span></span>

<span data-ttu-id="6bbee-523">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-523">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="6bbee-524">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-524">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="6bbee-525">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-525">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="6bbee-526">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="6bbee-526">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="6bbee-527">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="6bbee-527">Parameters - extendedDataType</span></span>

<span data-ttu-id="6bbee-528">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-528">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="6bbee-529">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="6bbee-529">Return Value - extendedDataType</span></span>

## <a name="method-fasttabsummary"></a><span data-ttu-id="6bbee-530">メソッド fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="6bbee-530">Method fastTabSummary</span></span>

```xpp
public int fastTabSummary([int value])
```

### <a name="parameters---fasttabsummary"></a><span data-ttu-id="6bbee-531">パラメーター - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="6bbee-531">Parameters - fastTabSummary</span></span>

<span data-ttu-id="6bbee-532">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-532">value</span></span>  

### <a name="return-value---fasttabsummary"></a><span data-ttu-id="6bbee-533">戻り値 - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="6bbee-533">Return Value - fastTabSummary</span></span>

## <a name="method-font"></a><span data-ttu-id="6bbee-534">メソッド font</span><span class="sxs-lookup"><span data-stu-id="6bbee-534">Method font</span></span>

<span data-ttu-id="6bbee-535">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-535">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="6bbee-536">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="6bbee-536">Parameters - font</span></span>

<span data-ttu-id="6bbee-537">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-537">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="6bbee-538">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="6bbee-538">Return Value - font</span></span>

<span data-ttu-id="6bbee-539">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="6bbee-539">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="6bbee-540">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="6bbee-540">Method fontSize</span></span>

<span data-ttu-id="6bbee-541">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-541">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="6bbee-542">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="6bbee-542">Parameters - fontSize</span></span>

<span data-ttu-id="6bbee-543">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-543">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="6bbee-544">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="6bbee-544">Return Value - fontSize</span></span>

<span data-ttu-id="6bbee-545">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="6bbee-545">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="6bbee-546">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="6bbee-546">Method foregroundColor</span></span>

<span data-ttu-id="6bbee-547">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-547">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="6bbee-548">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="6bbee-548">Parameters - foregroundColor</span></span>

<span data-ttu-id="6bbee-549">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-549">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="6bbee-550">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="6bbee-550">Return Value - foregroundColor</span></span>

<span data-ttu-id="6bbee-551">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="6bbee-551">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="6bbee-552">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="6bbee-552">Remarks - foregroundColor</span></span>

<span data-ttu-id="6bbee-553">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-553">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="6bbee-554">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6bbee-554">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="6bbee-555">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="6bbee-555">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="6bbee-556">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="6bbee-556">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="6bbee-557">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6bbee-557">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="6bbee-558">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="6bbee-558">The maximum value for a single byte is 255.</span></span>

## <a name="method-height"></a><span data-ttu-id="6bbee-559">メソッド height</span><span class="sxs-lookup"><span data-stu-id="6bbee-559">Method height</span></span>

<span data-ttu-id="6bbee-560">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-560">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="6bbee-561">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="6bbee-561">Parameters - height</span></span>

<span data-ttu-id="6bbee-562">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-562">value</span></span>  

<!-- -->

<span data-ttu-id="6bbee-563">モード</span><span class="sxs-lookup"><span data-stu-id="6bbee-563">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="6bbee-564">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="6bbee-564">Return Value - height</span></span>

<span data-ttu-id="6bbee-565">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="6bbee-565">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="6bbee-566">備考 - height</span><span class="sxs-lookup"><span data-stu-id="6bbee-566">Remarks - height</span></span>

<span data-ttu-id="6bbee-567">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-567">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="6bbee-568">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="6bbee-568">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="6bbee-569">モード。</span><span class="sxs-lookup"><span data-stu-id="6bbee-569">Mode.</span></span>            | <span data-ttu-id="6bbee-570">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="6bbee-570">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bbee-571">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="6bbee-571">-1 Exact.</span></span>        | <span data-ttu-id="6bbee-572">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-572">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="6bbee-573">0 自動。</span><span class="sxs-lookup"><span data-stu-id="6bbee-573">0 Auto.</span></span>          | <span data-ttu-id="6bbee-574">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-574">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6bbee-575">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="6bbee-575">1 Column height.</span></span> | <span data-ttu-id="6bbee-576">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="6bbee-576">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="6bbee-577">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-577">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="6bbee-578">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-578">Method heightMode</span></span>

<span data-ttu-id="6bbee-579">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-579">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="6bbee-580">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-580">Parameters - heightMode</span></span>

<span data-ttu-id="6bbee-581">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-581">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="6bbee-582">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-582">Return Value - heightMode</span></span>

<span data-ttu-id="6bbee-583">計算モード。</span><span class="sxs-lookup"><span data-stu-id="6bbee-583">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="6bbee-584">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-584">Remarks - heightMode</span></span>

<span data-ttu-id="6bbee-585">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="6bbee-585">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="6bbee-586">モード。</span><span class="sxs-lookup"><span data-stu-id="6bbee-586">Mode.</span></span>          | <span data-ttu-id="6bbee-587">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="6bbee-587">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bbee-588">正確。</span><span class="sxs-lookup"><span data-stu-id="6bbee-588">Exact.</span></span>         | <span data-ttu-id="6bbee-589">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-589">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="6bbee-590">自動。</span><span class="sxs-lookup"><span data-stu-id="6bbee-590">Auto.</span></span>          | <span data-ttu-id="6bbee-591">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-591">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6bbee-592">列の高さ</span><span class="sxs-lookup"><span data-stu-id="6bbee-592">Column height.</span></span> | <span data-ttu-id="6bbee-593">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="6bbee-593">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="6bbee-594">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="6bbee-594">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="6bbee-595">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-595">Method heightValue</span></span>

<span data-ttu-id="6bbee-596">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-596">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="6bbee-597">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-597">Parameters - heightValue</span></span>

<span data-ttu-id="6bbee-598">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-598">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="6bbee-599">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-599">Return Value - heightValue</span></span>

<span data-ttu-id="6bbee-600">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="6bbee-600">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="6bbee-601">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-601">Remarks - heightValue</span></span>

<span data-ttu-id="6bbee-602">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="6bbee-602">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="6bbee-603">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="6bbee-603">Method helpText</span></span>

<span data-ttu-id="6bbee-604">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-604">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="6bbee-605">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="6bbee-605">Parameters - helpText</span></span>

<span data-ttu-id="6bbee-606">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-606">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="6bbee-607">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="6bbee-607">Return Value - helpText</span></span>

<span data-ttu-id="6bbee-608">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="6bbee-608">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="6bbee-609">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="6bbee-609">Remarks - helpText</span></span>

<span data-ttu-id="6bbee-610">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-610">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="6bbee-611">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="6bbee-611">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="6bbee-612">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="6bbee-612">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="6bbee-613">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="6bbee-613">Parameters - hierarchyParent</span></span>

<span data-ttu-id="6bbee-614">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-614">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="6bbee-615">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="6bbee-615">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="6bbee-616">メソッド id</span><span class="sxs-lookup"><span data-stu-id="6bbee-616">Method id</span></span>

<span data-ttu-id="6bbee-617">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-617">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="6bbee-618">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="6bbee-618">Return Value - id</span></span>

<span data-ttu-id="6bbee-619">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="6bbee-619">The ID of the control.</span></span>

## <a name="method-imemode"></a><span data-ttu-id="6bbee-620">メソッド iMEMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-620">Method iMEMode</span></span>

```xpp
public int iMEMode([int value])
```

### <a name="parameters---imemode"></a><span data-ttu-id="6bbee-621">パラメーター - iMEMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-621">Parameters - iMEMode</span></span>

<span data-ttu-id="6bbee-622">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-622">value</span></span>  

### <a name="return-value---imemode"></a><span data-ttu-id="6bbee-623">戻り値 - iMEMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-623">Return Value - iMEMode</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="6bbee-624">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="6bbee-624">Method isContainer</span></span>

<span data-ttu-id="6bbee-625">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-625">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="6bbee-626">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="6bbee-626">Return Value - isContainer</span></span>

<span data-ttu-id="6bbee-627">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bbee-627">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="6bbee-628">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="6bbee-628">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="6bbee-629">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="6bbee-629">Parameters - italic</span></span>

<span data-ttu-id="6bbee-630">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-630">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="6bbee-631">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="6bbee-631">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="6bbee-632">メソッド label</span><span class="sxs-lookup"><span data-stu-id="6bbee-632">Method label</span></span>

<span data-ttu-id="6bbee-633">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-633">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="6bbee-634">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="6bbee-634">Parameters - label</span></span>

<span data-ttu-id="6bbee-635">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-635">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="6bbee-636">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="6bbee-636">Return Value - label</span></span>

<span data-ttu-id="6bbee-637">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="6bbee-637">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="6bbee-638">備考 - label</span><span class="sxs-lookup"><span data-stu-id="6bbee-638">Remarks - label</span></span>

<span data-ttu-id="6bbee-639">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-639">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="6bbee-640">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="6bbee-640">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="6bbee-641">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="6bbee-641">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="6bbee-642">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="6bbee-642">Parameters - labelAlignment</span></span>

<span data-ttu-id="6bbee-643">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-643">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="6bbee-644">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="6bbee-644">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="6bbee-645">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="6bbee-645">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="6bbee-646">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="6bbee-646">Parameters - labelBold</span></span>

<span data-ttu-id="6bbee-647">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-647">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="6bbee-648">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="6bbee-648">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="6bbee-649">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="6bbee-649">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="6bbee-650">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="6bbee-650">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="6bbee-651">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-651">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="6bbee-652">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="6bbee-652">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="6bbee-653">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="6bbee-653">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="6bbee-654">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="6bbee-654">Parameters - labelFont</span></span>

<span data-ttu-id="6bbee-655">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-655">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="6bbee-656">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="6bbee-656">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="6bbee-657">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="6bbee-657">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="6bbee-658">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="6bbee-658">Parameters - labelFontSize</span></span>

<span data-ttu-id="6bbee-659">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-659">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="6bbee-660">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="6bbee-660">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="6bbee-661">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="6bbee-661">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="6bbee-662">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="6bbee-662">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="6bbee-663">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-663">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="6bbee-664">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="6bbee-664">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="6bbee-665">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="6bbee-665">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="6bbee-666">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="6bbee-666">Parameters - labelGuide</span></span>

<span data-ttu-id="6bbee-667">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-667">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="6bbee-668">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="6bbee-668">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="6bbee-669">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="6bbee-669">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="6bbee-670">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="6bbee-670">Parameters - labelHeight</span></span>

<span data-ttu-id="6bbee-671">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-671">value</span></span>  

<!-- -->

<span data-ttu-id="6bbee-672">モード</span><span class="sxs-lookup"><span data-stu-id="6bbee-672">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="6bbee-673">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="6bbee-673">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="6bbee-674">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-674">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="6bbee-675">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-675">Parameters - labelHeightMode</span></span>

<span data-ttu-id="6bbee-676">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-676">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="6bbee-677">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-677">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="6bbee-678">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-678">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="6bbee-679">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-679">Parameters - labelHeightValue</span></span>

<span data-ttu-id="6bbee-680">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-680">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="6bbee-681">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-681">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="6bbee-682">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="6bbee-682">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="6bbee-683">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="6bbee-683">Parameters - labelItalic</span></span>

<span data-ttu-id="6bbee-684">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-684">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="6bbee-685">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="6bbee-685">Return Value - labelItalic</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="6bbee-686">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="6bbee-686">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="6bbee-687">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="6bbee-687">Parameters - labelPosition</span></span>

<span data-ttu-id="6bbee-688">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-688">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="6bbee-689">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="6bbee-689">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="6bbee-690">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="6bbee-690">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="6bbee-691">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="6bbee-691">Parameters - labelUnderline</span></span>

<span data-ttu-id="6bbee-692">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-692">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="6bbee-693">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="6bbee-693">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="6bbee-694">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="6bbee-694">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="6bbee-695">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="6bbee-695">Parameters - labelWidth</span></span>

<span data-ttu-id="6bbee-696">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-696">value</span></span>  

<!-- -->

<span data-ttu-id="6bbee-697">モード</span><span class="sxs-lookup"><span data-stu-id="6bbee-697">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="6bbee-698">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="6bbee-698">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="6bbee-699">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-699">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="6bbee-700">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-700">Parameters - labelWidthMode</span></span>

<span data-ttu-id="6bbee-701">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-701">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="6bbee-702">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-702">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="6bbee-703">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-703">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="6bbee-704">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-704">Parameters - labelWidthValue</span></span>

<span data-ttu-id="6bbee-705">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-705">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="6bbee-706">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-706">Return Value - labelWidthValue</span></span>

## <a name="method-left"></a><span data-ttu-id="6bbee-707">メソッド left</span><span class="sxs-lookup"><span data-stu-id="6bbee-707">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="6bbee-708">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="6bbee-708">Parameters - left</span></span>

<span data-ttu-id="6bbee-709">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-709">value</span></span>  

<!-- -->

<span data-ttu-id="6bbee-710">モード</span><span class="sxs-lookup"><span data-stu-id="6bbee-710">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="6bbee-711">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="6bbee-711">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="6bbee-712">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-712">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="6bbee-713">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-713">Parameters - leftMode</span></span>

<span data-ttu-id="6bbee-714">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-714">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="6bbee-715">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-715">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="6bbee-716">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-716">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="6bbee-717">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-717">Parameters - leftValue</span></span>

<span data-ttu-id="6bbee-718">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-718">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="6bbee-719">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-719">Return Value - leftValue</span></span>

## <a name="method-limittext"></a><span data-ttu-id="6bbee-720">メソッド limitText</span><span class="sxs-lookup"><span data-stu-id="6bbee-720">Method limitText</span></span>

```xpp
public int limitText([int value], [AutoMode mode])
```

### <a name="parameters---limittext"></a><span data-ttu-id="6bbee-721">パラメーター - limitText</span><span class="sxs-lookup"><span data-stu-id="6bbee-721">Parameters - limitText</span></span>

<span data-ttu-id="6bbee-722">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-722">value</span></span>  

<!-- -->

<span data-ttu-id="6bbee-723">モード</span><span class="sxs-lookup"><span data-stu-id="6bbee-723">mode</span></span>  

### <a name="return-value---limittext"></a><span data-ttu-id="6bbee-724">戻り値 - limitText</span><span class="sxs-lookup"><span data-stu-id="6bbee-724">Return Value - limitText</span></span>

## <a name="method-limittextmode"></a><span data-ttu-id="6bbee-725">メソッド limitTextMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-725">Method limitTextMode</span></span>

```xpp
public AutoMode limitTextMode([AutoMode mode])
```

### <a name="parameters---limittextmode"></a><span data-ttu-id="6bbee-726">パラメーター - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-726">Parameters - limitTextMode</span></span>

<span data-ttu-id="6bbee-727">モード</span><span class="sxs-lookup"><span data-stu-id="6bbee-727">mode</span></span>  

### <a name="return-value---limittextmode"></a><span data-ttu-id="6bbee-728">戻り値 - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-728">Return Value - limitTextMode</span></span>

## <a name="method-limittextvalue"></a><span data-ttu-id="6bbee-729">メソッド limitTextValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-729">Method limitTextValue</span></span>

```xpp
public int limitTextValue([int value])
```

### <a name="parameters---limittextvalue"></a><span data-ttu-id="6bbee-730">パラメーター - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-730">Parameters - limitTextValue</span></span>

<span data-ttu-id="6bbee-731">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-731">value</span></span>  

### <a name="return-value---limittextvalue"></a><span data-ttu-id="6bbee-732">戻り値 - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-732">Return Value - limitTextValue</span></span>

## <a name="method-lookupbutton"></a><span data-ttu-id="6bbee-733">メソッド lookupButton</span><span class="sxs-lookup"><span data-stu-id="6bbee-733">Method lookupButton</span></span>

```xpp
public int lookupButton([int value])
```

### <a name="parameters---lookupbutton"></a><span data-ttu-id="6bbee-734">パラメーター - lookupButton</span><span class="sxs-lookup"><span data-stu-id="6bbee-734">Parameters - lookupButton</span></span>

<span data-ttu-id="6bbee-735">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-735">value</span></span>  

### <a name="return-value---lookupbutton"></a><span data-ttu-id="6bbee-736">戻り値 - lookupButton</span><span class="sxs-lookup"><span data-stu-id="6bbee-736">Return Value - lookupButton</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="6bbee-737">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="6bbee-737">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="6bbee-738">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="6bbee-738">Parameters - mandatory</span></span>

<span data-ttu-id="6bbee-739">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-739">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="6bbee-740">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="6bbee-740">Return Value - mandatory</span></span>

## <a name="method-maxdatelabel"></a><span data-ttu-id="6bbee-741">メソッド maxDateLabel</span><span class="sxs-lookup"><span data-stu-id="6bbee-741">Method maxDateLabel</span></span>

```xpp
public str maxDateLabel([str value])
```

### <a name="parameters---maxdatelabel"></a><span data-ttu-id="6bbee-742">パラメーター - maxDateLabel</span><span class="sxs-lookup"><span data-stu-id="6bbee-742">Parameters - maxDateLabel</span></span>

<span data-ttu-id="6bbee-743">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-743">value</span></span>  

### <a name="return-value---maxdatelabel"></a><span data-ttu-id="6bbee-744">戻り値 - maxDateLabel</span><span class="sxs-lookup"><span data-stu-id="6bbee-744">Return Value - maxDateLabel</span></span>

## <a name="method-name"></a><span data-ttu-id="6bbee-745">メソッド名</span><span class="sxs-lookup"><span data-stu-id="6bbee-745">Method name</span></span>

<span data-ttu-id="6bbee-746">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-746">Gets or sets the name that is used in the code to identify a form, report, table, query, or another application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="6bbee-747">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="6bbee-747">Parameters - name</span></span>

<span data-ttu-id="6bbee-748">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-748">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="6bbee-749">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="6bbee-749">Return Value - name</span></span>

<span data-ttu-id="6bbee-750">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="6bbee-750">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="6bbee-751">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="6bbee-751">Remarks - name</span></span>

<span data-ttu-id="6bbee-752">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6bbee-752">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="6bbee-753">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-753">Begins with a letter.</span></span>
-   <span data-ttu-id="6bbee-754">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="6bbee-754">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="6bbee-755">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-755">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="6bbee-756">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="6bbee-756">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="6bbee-757">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="6bbee-757">Tables cannot have the same name as other public objects, such as extended data types, base enumeration types, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="6bbee-758">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="6bbee-758">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="6bbee-759">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="6bbee-759">Parameters - neededPermission</span></span>

<span data-ttu-id="6bbee-760">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-760">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="6bbee-761">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="6bbee-761">Return Value - neededPermission</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="6bbee-762">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="6bbee-762">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="6bbee-763">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="6bbee-763">Parameters - promptrect</span></span>

<span data-ttu-id="6bbee-764">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-764">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="6bbee-765">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="6bbee-765">Return Value - promptrect</span></span>

## <a name="method-replaceonlookup"></a><span data-ttu-id="6bbee-766">メソッド replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="6bbee-766">Method replaceOnLookup</span></span>

```xpp
public boolean replaceOnLookup([boolean value])
```

### <a name="parameters---replaceonlookup"></a><span data-ttu-id="6bbee-767">パラメーター - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="6bbee-767">Parameters - replaceOnLookup</span></span>

<span data-ttu-id="6bbee-768">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-768">value</span></span>  

### <a name="return-value---replaceonlookup"></a><span data-ttu-id="6bbee-769">戻り値 - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="6bbee-769">Return Value - replaceOnLookup</span></span>

## <a name="method-searchafterinput"></a><span data-ttu-id="6bbee-770">メソッド searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="6bbee-770">Method searchAfterInput</span></span>

```xpp
public int searchAfterInput([int value])
```

### <a name="parameters---searchafterinput"></a><span data-ttu-id="6bbee-771">パラメーター - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="6bbee-771">Parameters - searchAfterInput</span></span>

<span data-ttu-id="6bbee-772">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-772">value</span></span>  

### <a name="return-value---searchafterinput"></a><span data-ttu-id="6bbee-773">戻り値 - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="6bbee-773">Return Value - searchAfterInput</span></span>

## <a name="method-searchmode"></a><span data-ttu-id="6bbee-774">メソッド searchMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-774">Method searchMode</span></span>

```xpp
public int searchMode([int value])
```

### <a name="parameters---searchmode"></a><span data-ttu-id="6bbee-775">パラメーター - searchMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-775">Parameters - searchMode</span></span>

<span data-ttu-id="6bbee-776">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-776">value</span></span>  

### <a name="return-value---searchmode"></a><span data-ttu-id="6bbee-777">戻り値 - searchMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-777">Return Value - searchMode</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="6bbee-778">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="6bbee-778">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="6bbee-779">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="6bbee-779">Parameters - securityKey</span></span>

<span data-ttu-id="6bbee-780">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-780">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="6bbee-781">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="6bbee-781">Return Value - securityKey</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="6bbee-782">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="6bbee-782">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="6bbee-783">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="6bbee-783">Parameters - showLabel</span></span>

<span data-ttu-id="6bbee-784">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-784">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="6bbee-785">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="6bbee-785">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="6bbee-786">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="6bbee-786">Method skip</span></span>

<span data-ttu-id="6bbee-787">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-787">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="6bbee-788">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="6bbee-788">Parameters - skip</span></span>

<span data-ttu-id="6bbee-789">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-789">value</span></span>  
<span data-ttu-id="6bbee-790">コントロールの skip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="6bbee-790">The value to assign to the skip property of the control.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="6bbee-791">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="6bbee-791">Return Value - skip</span></span>

<span data-ttu-id="6bbee-792">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6bbee-792">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-style"></a><span data-ttu-id="6bbee-793">メソッド style</span><span class="sxs-lookup"><span data-stu-id="6bbee-793">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="6bbee-794">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="6bbee-794">Parameters - style</span></span>

<span data-ttu-id="6bbee-795">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-795">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="6bbee-796">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="6bbee-796">Return Value - style</span></span>

## <a name="method-top"></a><span data-ttu-id="6bbee-797">メソッド top</span><span class="sxs-lookup"><span data-stu-id="6bbee-797">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="6bbee-798">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="6bbee-798">Parameters - top</span></span>

<span data-ttu-id="6bbee-799">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-799">value</span></span>  

<!-- -->

<span data-ttu-id="6bbee-800">モード</span><span class="sxs-lookup"><span data-stu-id="6bbee-800">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="6bbee-801">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="6bbee-801">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="6bbee-802">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-802">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="6bbee-803">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-803">Parameters - topMode</span></span>

<span data-ttu-id="6bbee-804">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-804">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="6bbee-805">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-805">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="6bbee-806">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-806">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="6bbee-807">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-807">Parameters - topValue</span></span>

<span data-ttu-id="6bbee-808">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-808">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="6bbee-809">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-809">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="6bbee-810">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="6bbee-810">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="6bbee-811">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="6bbee-811">Parameters - type</span></span>

<span data-ttu-id="6bbee-812">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-812">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="6bbee-813">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="6bbee-813">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="6bbee-814">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="6bbee-814">Method underline</span></span>

<span data-ttu-id="6bbee-815">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-815">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="6bbee-816">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="6bbee-816">Parameters - underline</span></span>

<span data-ttu-id="6bbee-817">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-817">value</span></span>  
<span data-ttu-id="6bbee-818">コントロールの underline プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="6bbee-818">The value to assign to the underline property of the control.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="6bbee-819">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="6bbee-819">Return Value - underline</span></span>

<span data-ttu-id="6bbee-820">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6bbee-820">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-userdata"></a><span data-ttu-id="6bbee-821">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="6bbee-821">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="6bbee-822">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="6bbee-822">Parameters - userData</span></span>

<span data-ttu-id="6bbee-823">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-823">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="6bbee-824">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="6bbee-824">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="6bbee-825">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="6bbee-825">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="6bbee-826">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="6bbee-826">Parameters - userDataItem</span></span>

<span data-ttu-id="6bbee-827">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-827">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="6bbee-828">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="6bbee-828">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="6bbee-829">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="6bbee-829">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="6bbee-830">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="6bbee-830">Parameters - userDataItems</span></span>

<span data-ttu-id="6bbee-831">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-831">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="6bbee-832">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="6bbee-832">Return Value - userDataItems</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="6bbee-833">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="6bbee-833">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="6bbee-834">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="6bbee-834">Parameters - verticalSpacing</span></span>

<span data-ttu-id="6bbee-835">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-835">value</span></span>  

<!-- -->

<span data-ttu-id="6bbee-836">モード</span><span class="sxs-lookup"><span data-stu-id="6bbee-836">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="6bbee-837">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="6bbee-837">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="6bbee-838">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-838">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="6bbee-839">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-839">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="6bbee-840">モード</span><span class="sxs-lookup"><span data-stu-id="6bbee-840">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="6bbee-841">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-841">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="6bbee-842">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-842">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="6bbee-843">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-843">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="6bbee-844">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-844">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="6bbee-845">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-845">Return Value - verticalSpacingValue</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="6bbee-846">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-846">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="6bbee-847">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-847">Parameters - viewEditMode</span></span>

<span data-ttu-id="6bbee-848">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-848">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="6bbee-849">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-849">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="6bbee-850">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="6bbee-850">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="6bbee-851">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="6bbee-851">Parameters - visible</span></span>

<span data-ttu-id="6bbee-852">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-852">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="6bbee-853">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="6bbee-853">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="6bbee-854">メソッド width</span><span class="sxs-lookup"><span data-stu-id="6bbee-854">Method width</span></span>

<span data-ttu-id="6bbee-855">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-855">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="6bbee-856">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="6bbee-856">Parameters - width</span></span>

<span data-ttu-id="6bbee-857">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-857">value</span></span>  

<!-- -->

<span data-ttu-id="6bbee-858">モード</span><span class="sxs-lookup"><span data-stu-id="6bbee-858">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="6bbee-859">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="6bbee-859">Return Value - width</span></span>

<span data-ttu-id="6bbee-860">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="6bbee-860">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="6bbee-861">備考 - width</span><span class="sxs-lookup"><span data-stu-id="6bbee-861">Remarks - width</span></span>

<span data-ttu-id="6bbee-862">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-862">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="6bbee-863">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="6bbee-863">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="6bbee-864">モード。</span><span class="sxs-lookup"><span data-stu-id="6bbee-864">Mode.</span></span>           | <span data-ttu-id="6bbee-865">幅計算。</span><span class="sxs-lookup"><span data-stu-id="6bbee-865">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bbee-866">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="6bbee-866">-1 Exact.</span></span>       | <span data-ttu-id="6bbee-867">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-867">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="6bbee-868">0 自動。</span><span class="sxs-lookup"><span data-stu-id="6bbee-868">0 Auto.</span></span>         | <span data-ttu-id="6bbee-869">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-869">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6bbee-870">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="6bbee-870">1 Column width.</span></span> | <span data-ttu-id="6bbee-871">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="6bbee-871">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="6bbee-872">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-872">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="6bbee-873">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-873">Method widthMode</span></span>

<span data-ttu-id="6bbee-874">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-874">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="6bbee-875">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-875">Parameters - widthMode</span></span>

<span data-ttu-id="6bbee-876">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-876">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="6bbee-877">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-877">Return Value - widthMode</span></span>

<span data-ttu-id="6bbee-878">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bbee-878">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="6bbee-879">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="6bbee-879">Remarks - widthMode</span></span>

<span data-ttu-id="6bbee-880">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="6bbee-880">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="6bbee-881">モード。</span><span class="sxs-lookup"><span data-stu-id="6bbee-881">Mode.</span></span>         | <span data-ttu-id="6bbee-882">幅計算。</span><span class="sxs-lookup"><span data-stu-id="6bbee-882">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bbee-883">正確。</span><span class="sxs-lookup"><span data-stu-id="6bbee-883">Exact.</span></span>        | <span data-ttu-id="6bbee-884">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-884">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="6bbee-885">自動。</span><span class="sxs-lookup"><span data-stu-id="6bbee-885">Auto.</span></span>         | <span data-ttu-id="6bbee-886">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6bbee-886">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6bbee-887">列の幅。</span><span class="sxs-lookup"><span data-stu-id="6bbee-887">Column width.</span></span> | <span data-ttu-id="6bbee-888">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="6bbee-888">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="6bbee-889">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="6bbee-889">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="6bbee-890">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-890">Method widthValue</span></span>

<span data-ttu-id="6bbee-891">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-891">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="6bbee-892">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-892">Parameters - widthValue</span></span>

<span data-ttu-id="6bbee-893">値</span><span class="sxs-lookup"><span data-stu-id="6bbee-893">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="6bbee-894">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-894">Return Value - widthValue</span></span>

<span data-ttu-id="6bbee-895">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="6bbee-895">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="6bbee-896">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="6bbee-896">Remarks - widthValue</span></span>

<span data-ttu-id="6bbee-897">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="6bbee-897">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="6bbee-898">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="6bbee-898">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="6bbee-899">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="6bbee-899">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="6bbee-900">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="6bbee-900">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="6bbee-901">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="6bbee-901">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="6bbee-902">overrideObject</span><span class="sxs-lookup"><span data-stu-id="6bbee-902">overrideObject</span></span>  

