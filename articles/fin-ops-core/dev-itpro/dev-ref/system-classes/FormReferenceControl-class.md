---
title: FormReferenceControl クラス
description: このトピックでは、FormReferenceControl クラスについて説明します。
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
ms.openlocfilehash: 2d27eb7d69fa3bdfa56d501bbf874f87e1e1504d
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502624"
---
# <a name="class-formreferencecontrol"></a><span data-ttu-id="2ca5e-103">クラス FormReferenceControl</span><span class="sxs-lookup"><span data-stu-id="2ca5e-103">Class FormReferenceControl</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class FormReferenceControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="2ca5e-104">備考</span><span class="sxs-lookup"><span data-stu-id="2ca5e-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="2ca5e-105">例</span><span class="sxs-lookup"><span data-stu-id="2ca5e-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="2ca5e-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="2ca5e-106">Methods</span></span>

| <span data-ttu-id="2ca5e-107">方法</span><span class="sxs-lookup"><span data-stu-id="2ca5e-107">Method</span></span>                                                                           | <span data-ttu-id="2ca5e-108">説明</span><span class="sxs-lookup"><span data-stu-id="2ca5e-108">Description</span></span>                                                                                                                                                             |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca5e-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-109">public boolean alignControl(\[boolean value\])</span></span>                                   | <span data-ttu-id="2ca5e-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="2ca5e-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-111">public boolean allowEdit(\[boolean value\])</span></span>                                      | <span data-ttu-id="2ca5e-112">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-112">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="2ca5e-113">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-113">public boolean autoDeclaration(\[boolean value\])</span></span>                                | <span data-ttu-id="2ca5e-114">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-114">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="2ca5e-115">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-115">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>         | <span data-ttu-id="2ca5e-116">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-116">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="2ca5e-117">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-117">public str countryRegionCodes(\[str value\])</span></span>                                     | <span data-ttu-id="2ca5e-118">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-118">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="2ca5e-119">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-119">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                      |                                                                                                                                                                         |
| <span data-ttu-id="2ca5e-120">public int dataField()</span><span class="sxs-lookup"><span data-stu-id="2ca5e-120">public int dataField()</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="2ca5e-121">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-121">public str dataRelationPath(\[str value\])</span></span>                                       | <span data-ttu-id="2ca5e-122">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-122">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="2ca5e-123">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-123">public int dataSource(\[AnyType value\])</span></span>                                         | <span data-ttu-id="2ca5e-124">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-124">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="2ca5e-125">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-125">public int displayTarget(\[int value\])</span></span>                                          | <span data-ttu-id="2ca5e-126">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-126">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="2ca5e-127">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-127">public int dragDrop(\[int value\])</span></span>                                               | <span data-ttu-id="2ca5e-128">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-128">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="2ca5e-129">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-129">public boolean enabled(\[boolean value\])</span></span>                                        | <span data-ttu-id="2ca5e-130">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-130">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="2ca5e-131">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-131">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                 |                                                                                                                                                                         |
| <span data-ttu-id="2ca5e-132">public FilterValue filterValue(FieldBinding fieldBinding)</span><span class="sxs-lookup"><span data-stu-id="2ca5e-132">public FilterValue filterValue(FieldBinding fieldBinding)</span></span>                        |                                                                                                                                                                         |
| <span data-ttu-id="2ca5e-133">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-133">public int height(int value, \[int mode\])</span></span>                                       | <span data-ttu-id="2ca5e-134">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-134">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="2ca5e-135">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-135">public int heightMode(\[int value\])</span></span>                                             | <span data-ttu-id="2ca5e-136">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-136">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="2ca5e-137">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-137">public int heightValue(\[int value\])</span></span>                                            | <span data-ttu-id="2ca5e-138">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-138">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="2ca5e-139">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-139">public str helpText(\[str value\])</span></span>                                               | <span data-ttu-id="2ca5e-140">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-140">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="2ca5e-141">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-141">public str hierarchyParent(\[str value\])</span></span>                                        | <span data-ttu-id="2ca5e-142">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-142">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="2ca5e-143">public boolean isResolvingReference()</span><span class="sxs-lookup"><span data-stu-id="2ca5e-143">public boolean isResolvingReference()</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="2ca5e-144">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-144">public int left(int value, \[int mode\])</span></span>                                         | <span data-ttu-id="2ca5e-145">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-145">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="2ca5e-146">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-146">public int leftMode(\[int value\])</span></span>                                               | <span data-ttu-id="2ca5e-147">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-147">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="2ca5e-148">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-148">public int leftValue(\[int value\])</span></span>                                              | <span data-ttu-id="2ca5e-149">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-149">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="2ca5e-150">public Common lookupReference()</span><span class="sxs-lookup"><span data-stu-id="2ca5e-150">public Common lookupReference()</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="2ca5e-151">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-151">public boolean mandatory(\[boolean value\])</span></span>                                      |                                                                                                                                                                         |
| <span data-ttu-id="2ca5e-152">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-152">public str name(\[str value\])</span></span>                                                   | <span data-ttu-id="2ca5e-153">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-153">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="2ca5e-154">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-154">public int neededPermission(\[int value\])</span></span>                                       |                                                                                                                                                                         |
| <span data-ttu-id="2ca5e-155">public FormObjectSet referenceDataSource()</span><span class="sxs-lookup"><span data-stu-id="2ca5e-155">public FormObjectSet referenceDataSource()</span></span>                                       |                                                                                                                                                                         |
| <span data-ttu-id="2ca5e-156">public FieldId referenceField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-156">public FieldId referenceField(\[FieldId value\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="2ca5e-157">public str replacementFieldGroup(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-157">public str replacementFieldGroup(\[str value\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="2ca5e-158">public Common resolveReference()</span><span class="sxs-lookup"><span data-stu-id="2ca5e-158">public Common resolveReference()</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="2ca5e-159">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-159">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                        | <span data-ttu-id="2ca5e-160">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-160">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="2ca5e-161">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-161">public boolean skip(\[boolean value\])</span></span>                                           | <span data-ttu-id="2ca5e-162">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-162">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="2ca5e-163">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-163">public int top(int value, \[int mode\])</span></span>                                          | <span data-ttu-id="2ca5e-164">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-164">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="2ca5e-165">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-165">public int topMode(\[int value\])</span></span>                                                | <span data-ttu-id="2ca5e-166">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-166">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="2ca5e-167">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-167">public int topValue(\[int value\])</span></span>                                               | <span data-ttu-id="2ca5e-168">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-168">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="2ca5e-169">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-169">public int type(\[int value\])</span></span>                                                   |                                                                                                                                                                         |
| <span data-ttu-id="2ca5e-170">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-170">public int userData(\[int value\])</span></span>                                               | <span data-ttu-id="2ca5e-171">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-171">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="2ca5e-172">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-172">public int userDataItem(\[int value\])</span></span>                                           | <span data-ttu-id="2ca5e-173">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-173">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="2ca5e-174">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-174">public int userDataItems(\[int value\])</span></span>                                          | <span data-ttu-id="2ca5e-175">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-175">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="2ca5e-176">public Int64 value(\[Int64 value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-176">public Int64 value(\[Int64 value\])</span></span>                                              |                                                                                                                                                                         |
| <span data-ttu-id="2ca5e-177">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-177">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                     | <span data-ttu-id="2ca5e-178">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-178">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="2ca5e-179">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-179">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                           | <span data-ttu-id="2ca5e-180">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-180">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="2ca5e-181">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-181">public int verticalSpacingValue(\[int value\])</span></span>                                   | <span data-ttu-id="2ca5e-182">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-182">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="2ca5e-183">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-183">public boolean visible(\[boolean value\])</span></span>                                        | <span data-ttu-id="2ca5e-184">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-184">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="2ca5e-185">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-185">public int width(int value, \[int mode\])</span></span>                                        | <span data-ttu-id="2ca5e-186">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-186">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="2ca5e-187">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-187">public int widthMode(\[int value\])</span></span>                                              | <span data-ttu-id="2ca5e-188">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-188">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="2ca5e-189">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2ca5e-189">public int widthValue(\[int value\])</span></span>                                             | <span data-ttu-id="2ca5e-190">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-190">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="2ca5e-191">::public static boolean CanUserAdd(FormDataSource formDataSource, str fieldName)</span><span class="sxs-lookup"><span data-stu-id="2ca5e-191">::public static boolean CanUserAdd(FormDataSource formDataSource, str fieldName)</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="2ca5e-192">public void resolveChanges()</span><span class="sxs-lookup"><span data-stu-id="2ca5e-192">public void resolveChanges()</span></span>                                                     |                                                                                                                                                                         |
| <span data-ttu-id="2ca5e-193">public void performFormLookup(xFormRun form)</span><span class="sxs-lookup"><span data-stu-id="2ca5e-193">public void performFormLookup(xFormRun form)</span></span>                                     |                                                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="2ca5e-194">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="2ca5e-194">Method alignControl</span></span>

<span data-ttu-id="2ca5e-195">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-195">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="2ca5e-196">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="2ca5e-196">Parameters - alignControl</span></span>

<span data-ttu-id="2ca5e-197">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-197">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="2ca5e-198">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="2ca5e-198">Return Value - alignControl</span></span>

<span data-ttu-id="2ca5e-199">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-199">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="2ca5e-200">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="2ca5e-200">Remarks - alignControl</span></span>

<span data-ttu-id="2ca5e-201">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-201">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="2ca5e-202">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="2ca5e-202">Method allowEdit</span></span>

<span data-ttu-id="2ca5e-203">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-203">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="2ca5e-204">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="2ca5e-204">Parameters - allowEdit</span></span>

<span data-ttu-id="2ca5e-205">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-205">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="2ca5e-206">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="2ca5e-206">Return Value - allowEdit</span></span>

<span data-ttu-id="2ca5e-207">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-207">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="2ca5e-208">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="2ca5e-208">Remarks - allowEdit</span></span>

<span data-ttu-id="2ca5e-209">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-209">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="2ca5e-210">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="2ca5e-210">Method autoDeclaration</span></span>

<span data-ttu-id="2ca5e-211">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-211">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="2ca5e-212">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="2ca5e-212">Parameters - autoDeclaration</span></span>

<span data-ttu-id="2ca5e-213">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-213">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="2ca5e-214">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="2ca5e-214">Return Value - autoDeclaration</span></span>

<span data-ttu-id="2ca5e-215">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-215">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="2ca5e-216">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="2ca5e-216">Remarks - autoDeclaration</span></span>

<span data-ttu-id="2ca5e-217">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-217">Controls cannot have identical names.</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="2ca5e-218">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="2ca5e-218">Method configurationKey</span></span>

<span data-ttu-id="2ca5e-219">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-219">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="2ca5e-220">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="2ca5e-220">Parameters - configurationKey</span></span>

<span data-ttu-id="2ca5e-221">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-221">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="2ca5e-222">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="2ca5e-222">Return Value - configurationKey</span></span>

<span data-ttu-id="2ca5e-223">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-223">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="2ca5e-224">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="2ca5e-224">Remarks - configurationKey</span></span>

<span data-ttu-id="2ca5e-225">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-225">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="2ca5e-226">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-226">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="2ca5e-227">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="2ca5e-227">Method countryRegionCodes</span></span>

<span data-ttu-id="2ca5e-228">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-228">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="2ca5e-229">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="2ca5e-229">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="2ca5e-230">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-230">value</span></span>  
<span data-ttu-id="2ca5e-231">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-231">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="2ca5e-232">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="2ca5e-232">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="2ca5e-233">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-233">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="2ca5e-234">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="2ca5e-234">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="2ca5e-235">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="2ca5e-235">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="2ca5e-236">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-236">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="2ca5e-237">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="2ca5e-237">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="2ca5e-238">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="2ca5e-238">Method dataField</span></span>

```xpp
public int dataField()
```

### <a name="return-value---datafield"></a><span data-ttu-id="2ca5e-239">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="2ca5e-239">Return Value - dataField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="2ca5e-240">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="2ca5e-240">Method dataRelationPath</span></span>

<span data-ttu-id="2ca5e-241">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-241">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="2ca5e-242">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="2ca5e-242">Parameters - dataRelationPath</span></span>

<span data-ttu-id="2ca5e-243">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-243">value</span></span>  
<span data-ttu-id="2ca5e-244">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-244">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="2ca5e-245">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="2ca5e-245">Return Value - dataRelationPath</span></span>

<span data-ttu-id="2ca5e-246">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-246">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="2ca5e-247">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="2ca5e-247">Remarks - dataRelationPath</span></span>

<span data-ttu-id="2ca5e-248">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-248">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="2ca5e-249">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-249">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="2ca5e-250">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="2ca5e-250">Method dataSource</span></span>

<span data-ttu-id="2ca5e-251">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-251">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="2ca5e-252">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="2ca5e-252">Parameters - dataSource</span></span>

<span data-ttu-id="2ca5e-253">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-253">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="2ca5e-254">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="2ca5e-254">Return Value - dataSource</span></span>

<span data-ttu-id="2ca5e-255">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-255">The identifier of the data source to be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="2ca5e-256">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="2ca5e-256">Method displayTarget</span></span>

<span data-ttu-id="2ca5e-257">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-257">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="2ca5e-258">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="2ca5e-258">Parameters - displayTarget</span></span>

<span data-ttu-id="2ca5e-259">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-259">value</span></span>  
<span data-ttu-id="2ca5e-260">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-260">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="2ca5e-261">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="2ca5e-261">Return Value - displayTarget</span></span>

<span data-ttu-id="2ca5e-262">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-262">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="2ca5e-263">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="2ca5e-263">Method dragDrop</span></span>

<span data-ttu-id="2ca5e-264">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-264">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="2ca5e-265">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="2ca5e-265">Parameters - dragDrop</span></span>

<span data-ttu-id="2ca5e-266">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-266">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="2ca5e-267">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="2ca5e-267">Return Value - dragDrop</span></span>

<span data-ttu-id="2ca5e-268">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-268">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="2ca5e-269">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="2ca5e-269">Method enabled</span></span>

<span data-ttu-id="2ca5e-270">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-270">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="2ca5e-271">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="2ca5e-271">Parameters - enabled</span></span>

<span data-ttu-id="2ca5e-272">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-272">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="2ca5e-273">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="2ca5e-273">Return Value - enabled</span></span>

<span data-ttu-id="2ca5e-274">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-274">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="2ca5e-275">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="2ca5e-275">Remarks - enabled</span></span>

<span data-ttu-id="2ca5e-276">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-276">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="2ca5e-277">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-277">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="2ca5e-278">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-278">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="2ca5e-279">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="2ca5e-279">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="2ca5e-280">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="2ca5e-280">Parameters - extendedDataType</span></span>

<span data-ttu-id="2ca5e-281">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-281">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="2ca5e-282">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="2ca5e-282">Return Value - extendedDataType</span></span>

## <a name="method-filtervalue"></a><span data-ttu-id="2ca5e-283">メソッド filterValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-283">Method filterValue</span></span>

```xpp
public FilterValue filterValue(FieldBinding fieldBinding)
```

### <a name="parameters---filtervalue"></a><span data-ttu-id="2ca5e-284">パラメーター - filterValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-284">Parameters - filterValue</span></span>

<span data-ttu-id="2ca5e-285">fieldBinding</span><span class="sxs-lookup"><span data-stu-id="2ca5e-285">fieldBinding</span></span>  

### <a name="return-value---filtervalue"></a><span data-ttu-id="2ca5e-286">戻り値 - filterValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-286">Return Value - filterValue</span></span>

## <a name="method-height"></a><span data-ttu-id="2ca5e-287">メソッド height</span><span class="sxs-lookup"><span data-stu-id="2ca5e-287">Method height</span></span>

<span data-ttu-id="2ca5e-288">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-288">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="2ca5e-289">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="2ca5e-289">Parameters - height</span></span>

<span data-ttu-id="2ca5e-290">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-290">value</span></span>  

<!-- -->

<span data-ttu-id="2ca5e-291">モード</span><span class="sxs-lookup"><span data-stu-id="2ca5e-291">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="2ca5e-292">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="2ca5e-292">Return Value - height</span></span>

<span data-ttu-id="2ca5e-293">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-293">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="2ca5e-294">備考 - height</span><span class="sxs-lookup"><span data-stu-id="2ca5e-294">Remarks - height</span></span>

<span data-ttu-id="2ca5e-295">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-295">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="2ca5e-296">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-296">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="2ca5e-297">モード</span><span class="sxs-lookup"><span data-stu-id="2ca5e-297">Mode</span></span>            | <span data-ttu-id="2ca5e-298">高さの計算</span><span class="sxs-lookup"><span data-stu-id="2ca5e-298">Height calculation</span></span>                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca5e-299">-1 正確</span><span class="sxs-lookup"><span data-stu-id="2ca5e-299">-1 Exact</span></span>        | <span data-ttu-id="2ca5e-300">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-300">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="2ca5e-301">0 自動</span><span class="sxs-lookup"><span data-stu-id="2ca5e-301">0 Auto</span></span>          | <span data-ttu-id="2ca5e-302">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-302">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="2ca5e-303">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="2ca5e-303">1 Column height</span></span> | <span data-ttu-id="2ca5e-304">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-304">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="2ca5e-305">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-305">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="2ca5e-306">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="2ca5e-306">Method heightMode</span></span>

<span data-ttu-id="2ca5e-307">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-307">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="2ca5e-308">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="2ca5e-308">Parameters - heightMode</span></span>

<span data-ttu-id="2ca5e-309">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-309">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="2ca5e-310">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="2ca5e-310">Return Value - heightMode</span></span>

<span data-ttu-id="2ca5e-311">計算モード。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-311">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="2ca5e-312">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="2ca5e-312">Remarks - heightMode</span></span>

<span data-ttu-id="2ca5e-313">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-313">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="2ca5e-314">モード</span><span class="sxs-lookup"><span data-stu-id="2ca5e-314">Mode</span></span>          | <span data-ttu-id="2ca5e-315">高さの計算</span><span class="sxs-lookup"><span data-stu-id="2ca5e-315">Height calculation</span></span>                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca5e-316">正確</span><span class="sxs-lookup"><span data-stu-id="2ca5e-316">Exact</span></span>         | <span data-ttu-id="2ca5e-317">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-317">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="2ca5e-318">自動</span><span class="sxs-lookup"><span data-stu-id="2ca5e-318">Auto</span></span>          | <span data-ttu-id="2ca5e-319">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-319">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="2ca5e-320">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="2ca5e-320">Column height</span></span> | <span data-ttu-id="2ca5e-321">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-321">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="2ca5e-322">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-322">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="2ca5e-323">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-323">Method heightValue</span></span>

<span data-ttu-id="2ca5e-324">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-324">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="2ca5e-325">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-325">Parameters - heightValue</span></span>

<span data-ttu-id="2ca5e-326">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-326">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="2ca5e-327">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-327">Return Value - heightValue</span></span>

<span data-ttu-id="2ca5e-328">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-328">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="2ca5e-329">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-329">Remarks - heightValue</span></span>

<span data-ttu-id="2ca5e-330">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-330">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="2ca5e-331">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="2ca5e-331">Method helpText</span></span>

<span data-ttu-id="2ca5e-332">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-332">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="2ca5e-333">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="2ca5e-333">Parameters - helpText</span></span>

<span data-ttu-id="2ca5e-334">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-334">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="2ca5e-335">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="2ca5e-335">Return Value - helpText</span></span>

<span data-ttu-id="2ca5e-336">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-336">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="2ca5e-337">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="2ca5e-337">Remarks - helpText</span></span>

<span data-ttu-id="2ca5e-338">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-338">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="2ca5e-339">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-339">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="2ca5e-340">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="2ca5e-340">Method hierarchyParent</span></span>

<span data-ttu-id="2ca5e-341">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-341">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="2ca5e-342">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="2ca5e-342">Parameters - hierarchyParent</span></span>

<span data-ttu-id="2ca5e-343">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-343">value</span></span>  
<span data-ttu-id="2ca5e-344">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-344">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="2ca5e-345">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="2ca5e-345">Return Value - hierarchyParent</span></span>

<span data-ttu-id="2ca5e-346">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-346">The HierarchyParent property value of the control.</span></span>

## <a name="method-isresolvingreference"></a><span data-ttu-id="2ca5e-347">メソッド isResolvingReference</span><span class="sxs-lookup"><span data-stu-id="2ca5e-347">Method isResolvingReference</span></span>

```xpp
public boolean isResolvingReference()
```

### <a name="return-value---isresolvingreference"></a><span data-ttu-id="2ca5e-348">戻り値 - isResolvingReference</span><span class="sxs-lookup"><span data-stu-id="2ca5e-348">Return Value - isResolvingReference</span></span>

## <a name="method-left"></a><span data-ttu-id="2ca5e-349">メソッド left</span><span class="sxs-lookup"><span data-stu-id="2ca5e-349">Method left</span></span>

<span data-ttu-id="2ca5e-350">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-350">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="2ca5e-351">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="2ca5e-351">Parameters - left</span></span>

<span data-ttu-id="2ca5e-352">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-352">value</span></span>  
<span data-ttu-id="2ca5e-353">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-353">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="2ca5e-354">モード</span><span class="sxs-lookup"><span data-stu-id="2ca5e-354">mode</span></span>  
<span data-ttu-id="2ca5e-355">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-355">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="2ca5e-356">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="2ca5e-356">Return Value - left</span></span>

<span data-ttu-id="2ca5e-357">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-357">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="2ca5e-358">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="2ca5e-358">Method leftMode</span></span>

<span data-ttu-id="2ca5e-359">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-359">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="2ca5e-360">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="2ca5e-360">Parameters - leftMode</span></span>

<span data-ttu-id="2ca5e-361">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-361">value</span></span>  
<span data-ttu-id="2ca5e-362">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-362">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="2ca5e-363">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="2ca5e-363">Return Value - leftMode</span></span>

<span data-ttu-id="2ca5e-364">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-364">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="2ca5e-365">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-365">Method leftValue</span></span>

<span data-ttu-id="2ca5e-366">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-366">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="2ca5e-367">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-367">Parameters - leftValue</span></span>

<span data-ttu-id="2ca5e-368">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-368">value</span></span>  
<span data-ttu-id="2ca5e-369">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-369">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="2ca5e-370">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-370">Return Value - leftValue</span></span>

<span data-ttu-id="2ca5e-371">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-371">The horizontal position of the control in the form.</span></span>

## <a name="method-lookupreference"></a><span data-ttu-id="2ca5e-372">メソッド lookupReference</span><span class="sxs-lookup"><span data-stu-id="2ca5e-372">Method lookupReference</span></span>

```xpp
public Common lookupReference()
```

### <a name="return-value---lookupreference"></a><span data-ttu-id="2ca5e-373">戻り値 - lookupReference</span><span class="sxs-lookup"><span data-stu-id="2ca5e-373">Return Value - lookupReference</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="2ca5e-374">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="2ca5e-374">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="2ca5e-375">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="2ca5e-375">Parameters - mandatory</span></span>

<span data-ttu-id="2ca5e-376">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-376">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="2ca5e-377">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="2ca5e-377">Return Value - mandatory</span></span>

## <a name="method-name"></a><span data-ttu-id="2ca5e-378">メソッド名</span><span class="sxs-lookup"><span data-stu-id="2ca5e-378">Method name</span></span>

<span data-ttu-id="2ca5e-379">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-379">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="2ca5e-380">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="2ca5e-380">Parameters - name</span></span>

<span data-ttu-id="2ca5e-381">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-381">value</span></span>  
<span data-ttu-id="2ca5e-382">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-382">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="2ca5e-383">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="2ca5e-383">Return Value - name</span></span>

<span data-ttu-id="2ca5e-384">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-384">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="2ca5e-385">備考 - name</span><span class="sxs-lookup"><span data-stu-id="2ca5e-385">Remarks - name</span></span>

<span data-ttu-id="2ca5e-386">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-386">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="2ca5e-387">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-387">It must start with a letter.</span></span>
-   <span data-ttu-id="2ca5e-388">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-388">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="2ca5e-389">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-389">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="2ca5e-390">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-390">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="2ca5e-391">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-391">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="2ca5e-392">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="2ca5e-392">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="2ca5e-393">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="2ca5e-393">Parameters - neededPermission</span></span>

<span data-ttu-id="2ca5e-394">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-394">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="2ca5e-395">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="2ca5e-395">Return Value - neededPermission</span></span>

## <a name="method-referencedatasource"></a><span data-ttu-id="2ca5e-396">メソッド referenceDataSource</span><span class="sxs-lookup"><span data-stu-id="2ca5e-396">Method referenceDataSource</span></span>

```xpp
public FormObjectSet referenceDataSource()
```

### <a name="return-value---referencedatasource"></a><span data-ttu-id="2ca5e-397">戻り値 - referenceDataSource</span><span class="sxs-lookup"><span data-stu-id="2ca5e-397">Return Value - referenceDataSource</span></span>

## <a name="method-referencefield"></a><span data-ttu-id="2ca5e-398">メソッド referenceField</span><span class="sxs-lookup"><span data-stu-id="2ca5e-398">Method referenceField</span></span>

```xpp
public FieldId referenceField([FieldId value])
```

### <a name="parameters---referencefield"></a><span data-ttu-id="2ca5e-399">パラメーター - referenceField</span><span class="sxs-lookup"><span data-stu-id="2ca5e-399">Parameters - referenceField</span></span>

<span data-ttu-id="2ca5e-400">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-400">value</span></span>  

### <a name="return-value---referencefield"></a><span data-ttu-id="2ca5e-401">戻り値 - referenceField</span><span class="sxs-lookup"><span data-stu-id="2ca5e-401">Return Value - referenceField</span></span>

## <a name="method-replacementfieldgroup"></a><span data-ttu-id="2ca5e-402">メソッド replacementFieldGroup</span><span class="sxs-lookup"><span data-stu-id="2ca5e-402">Method replacementFieldGroup</span></span>

```xpp
public str replacementFieldGroup([str value])
```

### <a name="parameters---replacementfieldgroup"></a><span data-ttu-id="2ca5e-403">パラメーター - replacementFieldGroup</span><span class="sxs-lookup"><span data-stu-id="2ca5e-403">Parameters - replacementFieldGroup</span></span>

<span data-ttu-id="2ca5e-404">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-404">value</span></span>  

### <a name="return-value---replacementfieldgroup"></a><span data-ttu-id="2ca5e-405">戻り値 - replacementFieldGroup</span><span class="sxs-lookup"><span data-stu-id="2ca5e-405">Return Value - replacementFieldGroup</span></span>

## <a name="method-resolvereference"></a><span data-ttu-id="2ca5e-406">メソッド resolveReference</span><span class="sxs-lookup"><span data-stu-id="2ca5e-406">Method resolveReference</span></span>

```xpp
public Common resolveReference()
```

### <a name="return-value---resolvereference"></a><span data-ttu-id="2ca5e-407">戻り値 - resolveReference</span><span class="sxs-lookup"><span data-stu-id="2ca5e-407">Return Value - resolveReference</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="2ca5e-408">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="2ca5e-408">Method securityKey</span></span>

<span data-ttu-id="2ca5e-409">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-409">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="2ca5e-410">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="2ca5e-410">Parameters - securityKey</span></span>

<span data-ttu-id="2ca5e-411">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-411">value</span></span>  
<span data-ttu-id="2ca5e-412">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-412">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="2ca5e-413">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="2ca5e-413">Return Value - securityKey</span></span>

<span data-ttu-id="2ca5e-414">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-414">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-skip"></a><span data-ttu-id="2ca5e-415">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="2ca5e-415">Method skip</span></span>

<span data-ttu-id="2ca5e-416">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-416">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="2ca5e-417">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="2ca5e-417">Parameters - skip</span></span>

<span data-ttu-id="2ca5e-418">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-418">value</span></span>  
<span data-ttu-id="2ca5e-419">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-419">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="2ca5e-420">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="2ca5e-420">Return Value - skip</span></span>

<span data-ttu-id="2ca5e-421">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-421">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="2ca5e-422">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="2ca5e-422">Remarks - skip</span></span>

<span data-ttu-id="2ca5e-423">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-423">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-top"></a><span data-ttu-id="2ca5e-424">メソッド top</span><span class="sxs-lookup"><span data-stu-id="2ca5e-424">Method top</span></span>

<span data-ttu-id="2ca5e-425">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-425">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="2ca5e-426">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="2ca5e-426">Parameters - top</span></span>

<span data-ttu-id="2ca5e-427">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-427">value</span></span>  
<span data-ttu-id="2ca5e-428">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-428">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="2ca5e-429">モード</span><span class="sxs-lookup"><span data-stu-id="2ca5e-429">mode</span></span>  
<span data-ttu-id="2ca5e-430">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-430">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="2ca5e-431">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="2ca5e-431">Return Value - top</span></span>

<span data-ttu-id="2ca5e-432">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-432">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="2ca5e-433">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="2ca5e-433">Method topMode</span></span>

<span data-ttu-id="2ca5e-434">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-434">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="2ca5e-435">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="2ca5e-435">Parameters - topMode</span></span>

<span data-ttu-id="2ca5e-436">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-436">value</span></span>  
<span data-ttu-id="2ca5e-437">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-437">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="2ca5e-438">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="2ca5e-438">Return Value - topMode</span></span>

<span data-ttu-id="2ca5e-439">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-439">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="2ca5e-440">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-440">Method topValue</span></span>

<span data-ttu-id="2ca5e-441">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-441">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="2ca5e-442">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-442">Parameters - topValue</span></span>

<span data-ttu-id="2ca5e-443">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-443">value</span></span>  
<span data-ttu-id="2ca5e-444">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-444">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="2ca5e-445">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-445">Return Value - topValue</span></span>

<span data-ttu-id="2ca5e-446">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-446">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="2ca5e-447">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="2ca5e-447">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="2ca5e-448">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="2ca5e-448">Parameters - type</span></span>

<span data-ttu-id="2ca5e-449">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-449">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="2ca5e-450">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="2ca5e-450">Return Value - type</span></span>

## <a name="method-userdata"></a><span data-ttu-id="2ca5e-451">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="2ca5e-451">Method userData</span></span>

<span data-ttu-id="2ca5e-452">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-452">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="2ca5e-453">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="2ca5e-453">Parameters - userData</span></span>

<span data-ttu-id="2ca5e-454">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-454">value</span></span>  
<span data-ttu-id="2ca5e-455">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-455">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="2ca5e-456">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="2ca5e-456">Return Value - userData</span></span>

<span data-ttu-id="2ca5e-457">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-457">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="2ca5e-458">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="2ca5e-458">Method userDataItem</span></span>

<span data-ttu-id="2ca5e-459">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-459">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="2ca5e-460">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="2ca5e-460">Parameters - userDataItem</span></span>

<span data-ttu-id="2ca5e-461">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-461">value</span></span>  
<span data-ttu-id="2ca5e-462">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-462">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="2ca5e-463">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="2ca5e-463">Return Value - userDataItem</span></span>

<span data-ttu-id="2ca5e-464">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-464">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="2ca5e-465">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="2ca5e-465">Method userDataItems</span></span>

<span data-ttu-id="2ca5e-466">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-466">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="2ca5e-467">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="2ca5e-467">Parameters - userDataItems</span></span>

<span data-ttu-id="2ca5e-468">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-468">value</span></span>  
<span data-ttu-id="2ca5e-469">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-469">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="2ca5e-470">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="2ca5e-470">Return Value - userDataItems</span></span>

<span data-ttu-id="2ca5e-471">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-471">The number of user data items for the control.</span></span>

## <a name="method-value"></a><span data-ttu-id="2ca5e-472">メソッド value</span><span class="sxs-lookup"><span data-stu-id="2ca5e-472">Method value</span></span>

```xpp
public Int64 value([Int64 value])
```

### <a name="parameters---value"></a><span data-ttu-id="2ca5e-473">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="2ca5e-473">Parameters - value</span></span>

<span data-ttu-id="2ca5e-474">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-474">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="2ca5e-475">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="2ca5e-475">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="2ca5e-476">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="2ca5e-476">Method verticalSpacing</span></span>

<span data-ttu-id="2ca5e-477">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-477">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="2ca5e-478">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="2ca5e-478">Parameters - verticalSpacing</span></span>

<span data-ttu-id="2ca5e-479">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-479">value</span></span>  
<span data-ttu-id="2ca5e-480">コントロールの AutoMode を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-480">An integer value that indicates the AutoMode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="2ca5e-481">モード</span><span class="sxs-lookup"><span data-stu-id="2ca5e-481">mode</span></span>  
<span data-ttu-id="2ca5e-482">コントロールの AutoMode を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-482">An integer value that indicates the AutoMode for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="2ca5e-483">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="2ca5e-483">Return Value - verticalSpacing</span></span>

<span data-ttu-id="2ca5e-484">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-484">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="2ca5e-485">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="2ca5e-485">Method verticalSpacingMode</span></span>

<span data-ttu-id="2ca5e-486">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-486">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="2ca5e-487">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="2ca5e-487">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="2ca5e-488">モード</span><span class="sxs-lookup"><span data-stu-id="2ca5e-488">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="2ca5e-489">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="2ca5e-489">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="2ca5e-490">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-490">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="2ca5e-491">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-491">Method verticalSpacingValue</span></span>

<span data-ttu-id="2ca5e-492">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-492">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="2ca5e-493">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-493">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="2ca5e-494">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-494">value</span></span>  
<span data-ttu-id="2ca5e-495">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-495">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="2ca5e-496">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-496">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="2ca5e-497">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-497">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="2ca5e-498">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="2ca5e-498">Method visible</span></span>

<span data-ttu-id="2ca5e-499">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-499">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="2ca5e-500">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="2ca5e-500">Parameters - visible</span></span>

<span data-ttu-id="2ca5e-501">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-501">value</span></span>  
<span data-ttu-id="2ca5e-502">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-502">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="2ca5e-503">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="2ca5e-503">Return Value - visible</span></span>

<span data-ttu-id="2ca5e-504">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-504">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="2ca5e-505">メソッド width</span><span class="sxs-lookup"><span data-stu-id="2ca5e-505">Method width</span></span>

<span data-ttu-id="2ca5e-506">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-506">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="2ca5e-507">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="2ca5e-507">Parameters - width</span></span>

<span data-ttu-id="2ca5e-508">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-508">value</span></span>  

<!-- -->

<span data-ttu-id="2ca5e-509">モード</span><span class="sxs-lookup"><span data-stu-id="2ca5e-509">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="2ca5e-510">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="2ca5e-510">Return Value - width</span></span>

<span data-ttu-id="2ca5e-511">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-511">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="2ca5e-512">備考 - width</span><span class="sxs-lookup"><span data-stu-id="2ca5e-512">Remarks - width</span></span>

<span data-ttu-id="2ca5e-513">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-513">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="2ca5e-514">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-514">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="2ca5e-515">モード</span><span class="sxs-lookup"><span data-stu-id="2ca5e-515">Mode</span></span>           | <span data-ttu-id="2ca5e-516">幅計算</span><span class="sxs-lookup"><span data-stu-id="2ca5e-516">Width calculation</span></span>                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca5e-517">-1 正確</span><span class="sxs-lookup"><span data-stu-id="2ca5e-517">-1 Exact</span></span>       | <span data-ttu-id="2ca5e-518">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-518">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="2ca5e-519">0 自動</span><span class="sxs-lookup"><span data-stu-id="2ca5e-519">0 Auto</span></span>         | <span data-ttu-id="2ca5e-520">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-520">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="2ca5e-521">1 列の幅</span><span class="sxs-lookup"><span data-stu-id="2ca5e-521">1 Column width</span></span> | <span data-ttu-id="2ca5e-522">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-522">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="2ca5e-523">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-523">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="2ca5e-524">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="2ca5e-524">Method widthMode</span></span>

<span data-ttu-id="2ca5e-525">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-525">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="2ca5e-526">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="2ca5e-526">Parameters - widthMode</span></span>

<span data-ttu-id="2ca5e-527">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-527">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="2ca5e-528">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="2ca5e-528">Return Value - widthMode</span></span>

<span data-ttu-id="2ca5e-529">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-529">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="2ca5e-530">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="2ca5e-530">Remarks - widthMode</span></span>

<span data-ttu-id="2ca5e-531">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-531">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="2ca5e-532">モード</span><span class="sxs-lookup"><span data-stu-id="2ca5e-532">Mode</span></span>         | <span data-ttu-id="2ca5e-533">幅計算</span><span class="sxs-lookup"><span data-stu-id="2ca5e-533">Width calculation</span></span>                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca5e-534">正確</span><span class="sxs-lookup"><span data-stu-id="2ca5e-534">Exact</span></span>        | <span data-ttu-id="2ca5e-535">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-535">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="2ca5e-536">自動</span><span class="sxs-lookup"><span data-stu-id="2ca5e-536">Auto</span></span>         | <span data-ttu-id="2ca5e-537">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-537">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="2ca5e-538">列の幅</span><span class="sxs-lookup"><span data-stu-id="2ca5e-538">Column width</span></span> | <span data-ttu-id="2ca5e-539">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-539">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="2ca5e-540">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-540">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="2ca5e-541">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-541">Method widthValue</span></span>

<span data-ttu-id="2ca5e-542">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-542">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="2ca5e-543">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-543">Parameters - widthValue</span></span>

<span data-ttu-id="2ca5e-544">値</span><span class="sxs-lookup"><span data-stu-id="2ca5e-544">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="2ca5e-545">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-545">Return Value - widthValue</span></span>

<span data-ttu-id="2ca5e-546">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-546">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="2ca5e-547">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="2ca5e-547">Remarks - widthValue</span></span>

<span data-ttu-id="2ca5e-548">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="2ca5e-548">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-canuseradd"></a><span data-ttu-id="2ca5e-549">メソッド CanUserAdd</span><span class="sxs-lookup"><span data-stu-id="2ca5e-549">Method CanUserAdd</span></span>

```xpp
public static boolean CanUserAdd(FormDataSource formDataSource, str fieldName)
```

### <a name="parameters---canuseradd"></a><span data-ttu-id="2ca5e-550">パラメーター - CanUserAdd</span><span class="sxs-lookup"><span data-stu-id="2ca5e-550">Parameters - CanUserAdd</span></span>

<span data-ttu-id="2ca5e-551">formDataSource</span><span class="sxs-lookup"><span data-stu-id="2ca5e-551">formDataSource</span></span>  

<!-- -->

<span data-ttu-id="2ca5e-552">fieldName</span><span class="sxs-lookup"><span data-stu-id="2ca5e-552">fieldName</span></span>  

### <a name="return-value---canuseradd"></a><span data-ttu-id="2ca5e-553">戻り値 - CanUserAdd</span><span class="sxs-lookup"><span data-stu-id="2ca5e-553">Return Value - CanUserAdd</span></span>

## <a name="method-resolvechanges"></a><span data-ttu-id="2ca5e-554">メソッド resolveChanges</span><span class="sxs-lookup"><span data-stu-id="2ca5e-554">Method resolveChanges</span></span>

```xpp
public void resolveChanges()
```

## <a name="method-performformlookup"></a><span data-ttu-id="2ca5e-555">メソッド performFormLookup</span><span class="sxs-lookup"><span data-stu-id="2ca5e-555">Method performFormLookup</span></span>

```xpp
public void performFormLookup(xFormRun form)
```

### <a name="parameters---performformlookup"></a><span data-ttu-id="2ca5e-556">パラメーター - performFormLookup</span><span class="sxs-lookup"><span data-stu-id="2ca5e-556">Parameters - performFormLookup</span></span>

<span data-ttu-id="2ca5e-557">フォーム</span><span class="sxs-lookup"><span data-stu-id="2ca5e-557">form</span></span>  

