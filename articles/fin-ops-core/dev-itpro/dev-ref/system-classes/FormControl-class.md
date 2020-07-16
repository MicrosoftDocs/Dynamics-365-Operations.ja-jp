---
title: FormControl クラス
description: このトピックでは、FormControl クラスについて説明します。
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
ms.openlocfilehash: 32733802fde280f73fc9b84eaa22a74e7d649cb7
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502947"
---
# <a name="class-formcontrol"></a><span data-ttu-id="e50e9-103">クラス FormControl</span><span class="sxs-lookup"><span data-stu-id="e50e9-103">Class FormControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormControl extends Object
```

<span data-ttu-id="e50e9-104">FormControl クラスは、すべてのフォーム コントロールの基本クラスとして機能します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-104">The FormControl class serves as the base class for all form controls.</span></span>

## <a name="remarks"></a><span data-ttu-id="e50e9-105">備考</span><span class="sxs-lookup"><span data-stu-id="e50e9-105">Remarks</span></span>

<span data-ttu-id="e50e9-106">このクラスのインスタンスは作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="e50e9-106">You should not create an instance of this class.</span></span> <span data-ttu-id="e50e9-107">代わりに特定のコントロールを使用します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-107">Use the specific control instead.</span></span>

## <a name="examples"></a><span data-ttu-id="e50e9-108">例</span><span class="sxs-lookup"><span data-stu-id="e50e9-108">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="e50e9-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="e50e9-109">Methods</span></span>

| <span data-ttu-id="e50e9-110">方法</span><span class="sxs-lookup"><span data-stu-id="e50e9-110">Method</span></span>                                                                                                                                                 | <span data-ttu-id="e50e9-111">説明</span><span class="sxs-lookup"><span data-stu-id="e50e9-111">Description</span></span>                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e50e9-112">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-112">public boolean alignControl(\[boolean value\])</span></span>                                                                                                         | <span data-ttu-id="e50e9-113">コントロールを揃える必要があるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-113">Determines whether the control should be aligned.</span></span>                                                                                                                       |
| <span data-ttu-id="e50e9-114">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-114">public boolean allowEdit(\[boolean value\])</span></span>                                                                                                            | <span data-ttu-id="e50e9-115">ユーザーがコントロールの内容を修正できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-115">Determines whether the user can modify the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="e50e9-116">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="e50e9-116">public boolean allowSysSetup()</span></span>                                                                                                                         | <span data-ttu-id="e50e9-117">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-117">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="e50e9-118">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-118">public boolean autoDeclaration(\[boolean value\])</span></span>                                                                                                      | <span data-ttu-id="e50e9-119">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-119">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="e50e9-120">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="e50e9-120">public int beginDrag(int x, int y)</span></span>                                                                                                                     | <span data-ttu-id="e50e9-121">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-121">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="e50e9-122">public FormBuildControl build()</span><span class="sxs-lookup"><span data-stu-id="e50e9-122">public FormBuildControl build()</span></span>                                                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-123">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="e50e9-123">public container calcControlSize(int chars, int lines)</span></span>                                                                                                 | <span data-ttu-id="e50e9-124">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-124">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="e50e9-125">public FormChangeTracker changeTracker()</span><span class="sxs-lookup"><span data-stu-id="e50e9-125">public FormChangeTracker changeTracker()</span></span>                                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-126">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-126">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                                                               | <span data-ttu-id="e50e9-127">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-127">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="e50e9-128">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="e50e9-128">public List configurationKeyEx()</span></span>                                                                                                                       | <span data-ttu-id="e50e9-129">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-129">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="e50e9-130">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="e50e9-130">public int containerId()</span></span>                                                                                                                               | <span data-ttu-id="e50e9-131">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-131">Retrieves the ID of the parent container for the control.</span></span>                                                                                                               |
| <span data-ttu-id="e50e9-132">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-132">public str countryRegionCodes(\[str value\])</span></span>                                                                                                           | <span data-ttu-id="e50e9-133">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-133">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="e50e9-134">public int currentRow()</span><span class="sxs-lookup"><span data-stu-id="e50e9-134">public int currentRow()</span></span>                                                                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-135">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-135">public str dataRelationPath(\[str value\])</span></span>                                                                                                             | <span data-ttu-id="e50e9-136">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-136">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="e50e9-137">public FormDataSource dataSourceObject()</span><span class="sxs-lookup"><span data-stu-id="e50e9-137">public FormDataSource dataSourceObject()</span></span>                                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-138">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-138">public int displayTarget(\[int value\])</span></span>                                                                                                                | <span data-ttu-id="e50e9-139">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-139">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="e50e9-140">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-140">public int dragDrop(\[int value\])</span></span>                                                                                                                     | <span data-ttu-id="e50e9-141">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-141">Determines whether drag-and-drop operations are enabled or disabled for the control.</span></span>                                                                                    |
| <span data-ttu-id="e50e9-142">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="e50e9-142">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                                                      | <span data-ttu-id="e50e9-143">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-143">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="e50e9-144">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="e50e9-144">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                                                          | <span data-ttu-id="e50e9-145">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-145">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="e50e9-146">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="e50e9-146">public str dragText()</span></span>                                                                                                                                  | <span data-ttu-id="e50e9-147">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-147">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="e50e9-148">public boolean editAutoPostback(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-148">public boolean editAutoPostback(\[boolean value\])</span></span>                                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-149">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-149">public boolean enabled(\[boolean value\])</span></span>                                                                                                              | <span data-ttu-id="e50e9-150">オブジェクトが有効か無効かを決定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-150">Determines whether the object is enabled or disabled.</span></span>                                                                                                                   |
| <span data-ttu-id="e50e9-151">public str extendedStyle(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-151">public str extendedStyle(\[str value\])</span></span>                                                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-152">public FieldBinding fieldBinding()</span><span class="sxs-lookup"><span data-stu-id="e50e9-152">public FieldBinding fieldBinding()</span></span>                                                                                                                     | <span data-ttu-id="e50e9-153">FieldBinding 派生クラスへのコントロールのテーブルおよびフィールド バインディングを取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-153">Retrieves the table and field bindings of the control into a FieldBinding derived class.</span></span>                                                                                |
| <span data-ttu-id="e50e9-154">public str formatStr(\[int rowNumber\], \[boolean display\], \[int maxWidth\], \[boolean forceSignWhenDisplaceNegative\], \[boolean formatForExport\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-154">public str formatStr(\[int rowNumber\], \[boolean display\], \[int maxWidth\], \[boolean forceSignWhenDisplaceNegative\], \[boolean formatForExport\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-155">public xFormRun formRun()</span><span class="sxs-lookup"><span data-stu-id="e50e9-155">public xFormRun formRun()</span></span>                                                                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-156">public FormBinding getBinding(str propertyName)</span><span class="sxs-lookup"><span data-stu-id="e50e9-156">public FormBinding getBinding(str propertyName)</span></span>                                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-157">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-157">public boolean hasChanged(\[boolean val\])</span></span>                                                                                                             | <span data-ttu-id="e50e9-158">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-158">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="e50e9-159">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="e50e9-159">public boolean hasUserSetting()</span></span>                                                                                                                        | <span data-ttu-id="e50e9-160">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-160">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="e50e9-161">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-161">public int height(int value, \[int mode\])</span></span>                                                                                                             | <span data-ttu-id="e50e9-162">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-162">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="e50e9-163">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-163">public int heightMode(\[int value\])</span></span>                                                                                                                   | <span data-ttu-id="e50e9-164">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-164">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="e50e9-165">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-165">public int heightValue(\[int value\])</span></span>                                                                                                                  | <span data-ttu-id="e50e9-166">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-166">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="e50e9-167">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="e50e9-167">public str helpField()</span></span>                                                                                                                                 | <span data-ttu-id="e50e9-168">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-168">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="e50e9-169">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-169">public str helpText(\[str value\])</span></span>                                                                                                                     | <span data-ttu-id="e50e9-170">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-170">Gets or sets the Help text that is displayed at the bottom of the screen when a field or control is pointed to.</span></span>                                                         |
| <span data-ttu-id="e50e9-171">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-171">public str hierarchyParent(\[str value\])</span></span>                                                                                                              | <span data-ttu-id="e50e9-172">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-172">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="e50e9-173">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="e50e9-173">public int hWnd()</span></span>                                                                                                                                      | <span data-ttu-id="e50e9-174">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-174">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="e50e9-175">public int id()</span><span class="sxs-lookup"><span data-stu-id="e50e9-175">public int id()</span></span>                                                                                                                                        | <span data-ttu-id="e50e9-176">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-176">Retrieves the ID of the control.</span></span>                                                                                                                                        |
| <span data-ttu-id="e50e9-177">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="e50e9-177">public boolean isDisplayed()</span></span>                                                                                                                           | <span data-ttu-id="e50e9-178">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-178">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="e50e9-179">public boolean isEditable()</span><span class="sxs-lookup"><span data-stu-id="e50e9-179">public boolean isEditable()</span></span>                                                                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-180">public boolean isEnabled()</span><span class="sxs-lookup"><span data-stu-id="e50e9-180">public boolean isEnabled()</span></span>                                                                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-181">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="e50e9-181">public boolean isRestricted()</span></span>                                                                                                                          | <span data-ttu-id="e50e9-182">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-182">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="e50e9-183">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="e50e9-183">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                                                               | <span data-ttu-id="e50e9-184">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-184">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="e50e9-185">public boolean isVisible()</span><span class="sxs-lookup"><span data-stu-id="e50e9-185">public boolean isVisible()</span></span>                                                                                                                             | <span data-ttu-id="e50e9-186">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-186">Retrieves a value that indicates whether the control is visible.</span></span>                                                                                                        |
| <span data-ttu-id="e50e9-187">public boolean isVisibleOnClient()</span><span class="sxs-lookup"><span data-stu-id="e50e9-187">public boolean isVisibleOnClient()</span></span>                                                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-188">public str labelText()</span><span class="sxs-lookup"><span data-stu-id="e50e9-188">public str labelText()</span></span>                                                                                                                                 | <span data-ttu-id="e50e9-189">コントロールのラベル テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-189">Retrieves the label text for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="e50e9-190">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-190">public int left(int value, \[int mode\])</span></span>                                                                                                               | <span data-ttu-id="e50e9-191">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-191">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="e50e9-192">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-192">public int leftMode(\[int value\])</span></span>                                                                                                                     | <span data-ttu-id="e50e9-193">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-193">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="e50e9-194">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-194">public int leftValue(\[int value\])</span></span>                                                                                                                    | <span data-ttu-id="e50e9-195">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-195">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="e50e9-196">public boolean lockWindowUpdate(boolean lock)</span><span class="sxs-lookup"><span data-stu-id="e50e9-196">public boolean lockWindowUpdate(boolean lock)</span></span>                                                                                                          | <span data-ttu-id="e50e9-197">更新のコントロールのウィンドウをロックまたはロック解除します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-197">Locks or unlocks the window of the control for update.</span></span>                                                                                                                  |
| <span data-ttu-id="e50e9-198">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-198">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                                                                        | <span data-ttu-id="e50e9-199">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="e50e9-199">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="e50e9-200">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="e50e9-200">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                                                        | <span data-ttu-id="e50e9-201">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-201">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="e50e9-202">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="e50e9-202">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                                                            | <span data-ttu-id="e50e9-203">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-203">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="e50e9-204">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="e50e9-204">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                                                            | <span data-ttu-id="e50e9-205">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-205">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="e50e9-206">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="e50e9-206">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                                                              | <span data-ttu-id="e50e9-207">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-207">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="e50e9-208">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-208">public str name(\[str value\])</span></span>                                                                                                                         | <span data-ttu-id="e50e9-209">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-209">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="e50e9-210">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-210">public int neededPermission(\[int value\])</span></span>                                                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-211">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="e50e9-211">public container SysObsoleteAttribute()</span></span>                                                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-212">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="e50e9-212">public FormControl parentControl()</span></span>                                                                                                                     | <span data-ttu-id="e50e9-213">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-213">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="e50e9-214">public str resourceBundleName()</span><span class="sxs-lookup"><span data-stu-id="e50e9-214">public str resourceBundleName()</span></span>                                                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-215">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-215">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                                                              | <span data-ttu-id="e50e9-216">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-216">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="e50e9-217">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="e50e9-217">public int showContextMenu(int menuHandle)</span></span>                                                                                                             | <span data-ttu-id="e50e9-218">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-218">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="e50e9-219">public str getContextMenuOptions()</span><span class="sxs-lookup"><span data-stu-id="e50e9-219">public str getContextMenuOptions()</span></span>                                                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-220">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-220">public boolean skip(\[boolean value\])</span></span>                                                                                                                 | <span data-ttu-id="e50e9-221">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-221">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="e50e9-222">public str templateId()</span><span class="sxs-lookup"><span data-stu-id="e50e9-222">public str templateId()</span></span>                                                                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-223">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="e50e9-223">public str toolTip()</span></span>                                                                                                                                   | <span data-ttu-id="e50e9-224">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-224">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="e50e9-225">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-225">public int top(int value, \[int mode\])</span></span>                                                                                                                | <span data-ttu-id="e50e9-226">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-226">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="e50e9-227">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-227">public int topMode(\[int value\])</span></span>                                                                                                                      | <span data-ttu-id="e50e9-228">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-228">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="e50e9-229">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-229">public int topValue(\[int value\])</span></span>                                                                                                                     | <span data-ttu-id="e50e9-230">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-230">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="e50e9-231">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-231">public int type(\[int value\])</span></span>                                                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-232">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="e50e9-232">public boolean SysObsoleteAttribute(container data)</span></span>                                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-233">public int updateWindow()</span><span class="sxs-lookup"><span data-stu-id="e50e9-233">public int updateWindow()</span></span>                                                                                                                              | <span data-ttu-id="e50e9-234">コントロールのウィンドウを更新します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-234">Updates the window for the control.</span></span>                                                                                                                                     |
| <span data-ttu-id="e50e9-235">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-235">public int userData(\[int value\])</span></span>                                                                                                                     | <span data-ttu-id="e50e9-236">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-236">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="e50e9-237">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-237">public int userDataItem(\[int value\])</span></span>                                                                                                                 | <span data-ttu-id="e50e9-238">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-238">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="e50e9-239">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-239">public int userDataItems(\[int value\])</span></span>                                                                                                                | <span data-ttu-id="e50e9-240">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-240">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="e50e9-241">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-241">public int userDisable(\[int value\])</span></span>                                                                                                                  | <span data-ttu-id="e50e9-242">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-242">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="e50e9-243">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-243">public int userHeight(\[int value\])</span></span>                                                                                                                   | <span data-ttu-id="e50e9-244">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-244">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="e50e9-245">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-245">public int userHide(\[int value\])</span></span>                                                                                                                     | <span data-ttu-id="e50e9-246">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-246">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="e50e9-247">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-247">public int userOrgContainer(\[int value\])</span></span>                                                                                                             | <span data-ttu-id="e50e9-248">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-248">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="e50e9-249">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-249">public int userOrgSibling(\[int value\])</span></span>                                                                                                               | <span data-ttu-id="e50e9-250">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-250">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="e50e9-251">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-251">public str userPromptText(\[str value\])</span></span>                                                                                                               | <span data-ttu-id="e50e9-252">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-252">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="e50e9-253">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-253">public int userSecurityLevel(\[int value\])</span></span>                                                                                                            | <span data-ttu-id="e50e9-254">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-254">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="e50e9-255">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-255">public int userSkip(\[int value\])</span></span>                                                                                                                     | <span data-ttu-id="e50e9-256">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-256">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="e50e9-257">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-257">public int userWidth(\[int value\])</span></span>                                                                                                                    | <span data-ttu-id="e50e9-258">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-258">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="e50e9-259">public str valueStr()</span><span class="sxs-lookup"><span data-stu-id="e50e9-259">public str valueStr()</span></span>                                                                                                                                  | <span data-ttu-id="e50e9-260">文字列形式のコントロールの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-260">Retrieves the value of the control in string format.</span></span>                                                                                                                    |
| <span data-ttu-id="e50e9-261">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-261">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                                                           | <span data-ttu-id="e50e9-262">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-262">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="e50e9-263">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-263">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                                                                 | <span data-ttu-id="e50e9-264">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-264">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="e50e9-265">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-265">public int verticalSpacingValue(\[int value\])</span></span>                                                                                                         | <span data-ttu-id="e50e9-266">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-266">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="e50e9-267">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-267">public boolean visible(\[boolean value\])</span></span>                                                                                                              | <span data-ttu-id="e50e9-268">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-268">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="e50e9-269">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-269">public int width(int value, \[int mode\])</span></span>                                                                                                              | <span data-ttu-id="e50e9-270">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-270">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="e50e9-271">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-271">public int widthMode(\[int value\])</span></span>                                                                                                                    | <span data-ttu-id="e50e9-272">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-272">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="e50e9-273">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-273">public int widthValue(\[int value\])</span></span>                                                                                                                   | <span data-ttu-id="e50e9-274">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-274">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="e50e9-275">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="e50e9-275">public void displayControl()</span></span>                                                                                                                           | <span data-ttu-id="e50e9-276">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-276">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="e50e9-277">public void copy()</span><span class="sxs-lookup"><span data-stu-id="e50e9-277">public void copy()</span></span>                                                                                                                                     | <span data-ttu-id="e50e9-278">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="e50e9-278">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="e50e9-279">public void paste()</span><span class="sxs-lookup"><span data-stu-id="e50e9-279">public void paste()</span></span>                                                                                                                                    | <span data-ttu-id="e50e9-280">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-280">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="e50e9-281">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="e50e9-281">public void setFocus()</span></span>                                                                                                                                 | <span data-ttu-id="e50e9-282">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-282">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="e50e9-283">public void cut()</span><span class="sxs-lookup"><span data-stu-id="e50e9-283">public void cut()</span></span>                                                                                                                                      | <span data-ttu-id="e50e9-284">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="e50e9-284">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="e50e9-285">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="e50e9-285">public void gotFocus()</span></span>                                                                                                                                 | <span data-ttu-id="e50e9-286">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-286">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="e50e9-287">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="e50e9-287">public void dragLeave()</span></span>                                                                                                                                | <span data-ttu-id="e50e9-288">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-288">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="e50e9-289">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="e50e9-289">public void lostFocus()</span></span>                                                                                                                                | <span data-ttu-id="e50e9-290">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-290">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="e50e9-291">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="e50e9-291">public void inputSearch(str searchStr)</span></span>                                                                                                                 | <span data-ttu-id="e50e9-292">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-292">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="e50e9-293">public void setTemplateId(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-293">public void setTemplateId(\[str value\])</span></span>                                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-294">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="e50e9-294">public void prefColumnSize(int width, int height)</span></span>                                                                                                      | <span data-ttu-id="e50e9-295">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-295">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="e50e9-296">public void update()</span><span class="sxs-lookup"><span data-stu-id="e50e9-296">public void update()</span></span>                                                                                                                                   | <span data-ttu-id="e50e9-297">コントロールを更新します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-297">Updates the control.</span></span>                                                                                                                                                    |
| <span data-ttu-id="e50e9-298">public void run()</span><span class="sxs-lookup"><span data-stu-id="e50e9-298">public void run()</span></span>                                                                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-299">public void lock()</span><span class="sxs-lookup"><span data-stu-id="e50e9-299">public void lock()</span></span>                                                                                                                                     | <span data-ttu-id="e50e9-300">フォーム コントロールをロックします。</span><span class="sxs-lookup"><span data-stu-id="e50e9-300">Locks the form control.</span></span>                                                                                                                                                 |
| <span data-ttu-id="e50e9-301">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="e50e9-301">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                                                          | <span data-ttu-id="e50e9-302">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-302">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="e50e9-303">public void applyBuild()</span><span class="sxs-lookup"><span data-stu-id="e50e9-303">public void applyBuild()</span></span>                                                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-304">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="e50e9-304">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                                                              | <span data-ttu-id="e50e9-305">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-305">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="e50e9-306">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="e50e9-306">public void resetUserSetting()</span></span>                                                                                                                         | <span data-ttu-id="e50e9-307">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="e50e9-307">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="e50e9-308">public void new(FormBuildControl build, xFormRun formRun)</span><span class="sxs-lookup"><span data-stu-id="e50e9-308">public void new(FormBuildControl build, xFormRun formRun)</span></span>                                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-309">public void context()</span><span class="sxs-lookup"><span data-stu-id="e50e9-309">public void context()</span></span>                                                                                                                                  | <span data-ttu-id="e50e9-310">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-310">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="e50e9-311">public void unLock(boolean update)</span><span class="sxs-lookup"><span data-stu-id="e50e9-311">public void unLock(boolean update)</span></span>                                                                                                                     | <span data-ttu-id="e50e9-312">フォーム コントロールのロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-312">Unlocks a form control.</span></span>                                                                                                                                                 |
| <span data-ttu-id="e50e9-313">public void setResourceBundleName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-313">public void setResourceBundleName(\[str value\])</span></span>                                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-314">public void selectedMenuOption(int selectedOption)</span><span class="sxs-lookup"><span data-stu-id="e50e9-314">public void selectedMenuOption(int selectedOption)</span></span>                                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-315">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="e50e9-315">public void mouseLeave()</span></span>                                                                                                                               | <span data-ttu-id="e50e9-316">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-316">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="e50e9-317">public void onPropChanged(\[str propName\])</span><span class="sxs-lookup"><span data-stu-id="e50e9-317">public void onPropChanged(\[str propName\])</span></span>                                                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-318">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="e50e9-318">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                                                                  | <span data-ttu-id="e50e9-319">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-319">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="e50e9-320">public void initialize()</span><span class="sxs-lookup"><span data-stu-id="e50e9-320">public void initialize()</span></span>                                                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="e50e9-321">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="e50e9-321">public void endDrag()</span></span>                                                                                                                                  | <span data-ttu-id="e50e9-322">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-322">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |

## <a name="method-aligncontrol"></a><span data-ttu-id="e50e9-323">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="e50e9-323">Method alignControl</span></span>

<span data-ttu-id="e50e9-324">コントロールを揃える必要があるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-324">Determines whether the control should be aligned.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="e50e9-325">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="e50e9-325">Parameters - alignControl</span></span>

<span data-ttu-id="e50e9-326">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-326">value</span></span>  
<span data-ttu-id="e50e9-327">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="e50e9-327">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="e50e9-328">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="e50e9-328">Return Value - alignControl</span></span>

<span data-ttu-id="e50e9-329">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="e50e9-329">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="e50e9-330">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="e50e9-330">Remarks - alignControl</span></span>

<span data-ttu-id="e50e9-331">コントロールの左上隅は、最も長いラベルに基づいて配置されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-331">The upper-left corner of the control is aligned based on the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="e50e9-332">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="e50e9-332">Method allowEdit</span></span>

<span data-ttu-id="e50e9-333">ユーザーがコントロールの内容を修正できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-333">Determines whether the user can modify the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="e50e9-334">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="e50e9-334">Parameters - allowEdit</span></span>

<span data-ttu-id="e50e9-335">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-335">value</span></span>  
<span data-ttu-id="e50e9-336">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-336">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="e50e9-337">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="e50e9-337">Return Value - allowEdit</span></span>

<span data-ttu-id="e50e9-338">コントロールを変更することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="e50e9-338">true if the control can be modified; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="e50e9-339">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="e50e9-339">Remarks - allowEdit</span></span>

<span data-ttu-id="e50e9-340">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="e50e9-340">If this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

### <a name="examples---allowedit"></a><span data-ttu-id="e50e9-341">例 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="e50e9-341">Examples - allowEdit</span></span>

<span data-ttu-id="e50e9-342">次の例は、allowEdit プロパティの値を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-342">The following example shows how to return and set the value of the allowEdit property.</span></span>

```xpp
// Return the value. 
info (strfmt("allowEdit: %1", this.allowEdit())); 
// Set the value. 
this.allowEdit(false);
```

## <a name="method-allowsyssetup"></a><span data-ttu-id="e50e9-343">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="e50e9-343">Method allowSysSetup</span></span>

<span data-ttu-id="e50e9-344">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-344">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="e50e9-345">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="e50e9-345">Return Value - allowSysSetup</span></span>

<span data-ttu-id="e50e9-346">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="e50e9-346">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="e50e9-347">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="e50e9-347">Method autoDeclaration</span></span>

<span data-ttu-id="e50e9-348">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-348">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="e50e9-349">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="e50e9-349">Parameters - autoDeclaration</span></span>

<span data-ttu-id="e50e9-350">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-350">value</span></span>  
<span data-ttu-id="e50e9-351">値が指定されている場合は、プロパティを設定する値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-351">The value to set the property to, if a value is supplied.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="e50e9-352">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="e50e9-352">Return Value - autoDeclaration</span></span>

<span data-ttu-id="e50e9-353">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="e50e9-353">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="e50e9-354">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="e50e9-354">Remarks - autoDeclaration</span></span>

<span data-ttu-id="e50e9-355">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="e50e9-355">Controls cannot have identical names.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="e50e9-356">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="e50e9-356">Method beginDrag</span></span>

<span data-ttu-id="e50e9-357">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-357">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="e50e9-358">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="e50e9-358">Parameters - beginDrag</span></span>

<span data-ttu-id="e50e9-359">x</span><span class="sxs-lookup"><span data-stu-id="e50e9-359">x</span></span>  
<span data-ttu-id="e50e9-360">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-360">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="e50e9-361">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-361">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="e50e9-362">y</span><span class="sxs-lookup"><span data-stu-id="e50e9-362">y</span></span>  
<span data-ttu-id="e50e9-363">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-363">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="e50e9-364">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-364">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="e50e9-365">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="e50e9-365">Return Value - beginDrag</span></span>

<span data-ttu-id="e50e9-366">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="e50e9-366">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="e50e9-367">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="e50e9-367">Remarks - beginDrag</span></span>

<span data-ttu-id="e50e9-368">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="e50e9-368">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="e50e9-369">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-369">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="examples---begindrag"></a><span data-ttu-id="e50e9-370">例 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="e50e9-370">Examples - beginDrag</span></span>

<span data-ttu-id="e50e9-371">次の例では、ユーザーがフォーム コントロールのドラッグを開始したときに、Infolog の x 座標と y 座標を表示します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-371">The following example displays the x-coordinates and y-coordinates in the Infolog when the user starts to drag the form control.</span></span>

```xpp
public int beginDrag(int _x, int _y) 
{ 
    int ret; 
    info(strfmt("beginDrag (x, y) : (%1, %2)", _x, _y)); 
    ret = super(_x, _y); 
    return ret; 
}
```

## <a name="method-build"></a><span data-ttu-id="e50e9-372">メソッド build</span><span class="sxs-lookup"><span data-stu-id="e50e9-372">Method build</span></span>

```xpp
public FormBuildControl build()
```

### <a name="return-value---build"></a><span data-ttu-id="e50e9-373">戻り値 - build</span><span class="sxs-lookup"><span data-stu-id="e50e9-373">Return Value - build</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="e50e9-374">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="e50e9-374">Method calcControlSize</span></span>

<span data-ttu-id="e50e9-375">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-375">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="e50e9-376">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="e50e9-376">Parameters - calcControlSize</span></span>

<span data-ttu-id="e50e9-377">chars</span><span class="sxs-lookup"><span data-stu-id="e50e9-377">chars</span></span>  
<span data-ttu-id="e50e9-378">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="e50e9-378">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="e50e9-379">明細行</span><span class="sxs-lookup"><span data-stu-id="e50e9-379">lines</span></span>  
<span data-ttu-id="e50e9-380">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="e50e9-380">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="e50e9-381">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="e50e9-381">Return Value - calcControlSize</span></span>

<span data-ttu-id="e50e9-382">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="e50e9-382">The container that holds the width and height.</span></span>

## <a name="method-changetracker"></a><span data-ttu-id="e50e9-383">メソッド changeTracker</span><span class="sxs-lookup"><span data-stu-id="e50e9-383">Method changeTracker</span></span>

```xpp
public FormChangeTracker changeTracker()
```

### <a name="return-value---changetracker"></a><span data-ttu-id="e50e9-384">戻り値 - changeTracker</span><span class="sxs-lookup"><span data-stu-id="e50e9-384">Return Value - changeTracker</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="e50e9-385">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="e50e9-385">Method configurationKey</span></span>

<span data-ttu-id="e50e9-386">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-386">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="e50e9-387">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="e50e9-387">Parameters - configurationKey</span></span>

<span data-ttu-id="e50e9-388">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-388">value</span></span>  
<span data-ttu-id="e50e9-389">コントロールに割り当てるコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-389">The ID of the configuration key to assign to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="e50e9-390">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="e50e9-390">Return Value - configurationKey</span></span>

<span data-ttu-id="e50e9-391">コントロールに割り当てられるコンフィギュレーション キーの ID。</span><span class="sxs-lookup"><span data-stu-id="e50e9-391">The ID of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="e50e9-392">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="e50e9-392">Remarks - configurationKey</span></span>

<span data-ttu-id="e50e9-393">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-393">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="e50e9-394">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="e50e9-394">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="examples---configurationkey"></a><span data-ttu-id="e50e9-395">例 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="e50e9-395">Examples - configurationKey</span></span>

<span data-ttu-id="e50e9-396">次の例は、コントロールのコンフィギュレーション キーを設定して取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-396">The following example shows how to set and retrieve the configuration key for a control.</span></span>

```xpp
DictConfigurationKey dck; 
configurationKeyId cki; 
// objCtrl previously assigned. 
// Assign a configuration key to the control. 
objCtrl.configurationKey(configurationkeynum(BankDeposit)); 
// Retrieve the configuration key ID from the control. 
cki = objCtrl.configurationKey(); 
if (cki != 0) 
{ 
    dck = new DictConfigurationKey(cki); 
    if (dck) 
    { 
    print strfmt("Configuration Key ID: %1 Configuration Key Name: %2", 
                  cki, 
                  dck.name()); 
    } 
}
```

## <a name="method-configurationkeyex"></a><span data-ttu-id="e50e9-397">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="e50e9-397">Method configurationKeyEx</span></span>

<span data-ttu-id="e50e9-398">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-398">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="e50e9-399">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="e50e9-399">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="e50e9-400">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="e50e9-400">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="e50e9-401">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="e50e9-401">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="e50e9-402">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="e50e9-402">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="e50e9-403">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-403">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="e50e9-404">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-404">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

### <a name="examples---configurationkeyex"></a><span data-ttu-id="e50e9-405">例 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="e50e9-405">Examples - configurationKeyEx</span></span>

<span data-ttu-id="e50e9-406">次の例は、コントロールのコンフィギュレーション キー ID を取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-406">The following example shows how to retrieve the configuration key IDs for a control.</span></span>

```xpp
DictConfigurationKey dck; 
configurationKeyId cki; 
List list; 
ListEnumerator enum; 
// objCtrl previously assigned. 
list = objCtrl.configurationKeyEx(); 
if (0 != list.elements()) 
{ 
    enum = list.getEnumerator(); 
    while (enum.moveNext()) 
    { 
       dck = new DictConfigurationKey(enum.current()); 
       if (dck) 
       { 
        print strfmt("Configuration Key ID: %1 Configuration Key Name: %2", 
                     enum.current(), 
                     dck.name() ); 
       } 
    } 
}
```

## <a name="method-containerid"></a><span data-ttu-id="e50e9-407">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="e50e9-407">Method containerId</span></span>

<span data-ttu-id="e50e9-408">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-408">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="e50e9-409">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="e50e9-409">Return Value - containerId</span></span>

<span data-ttu-id="e50e9-410">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="e50e9-410">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="e50e9-411">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="e50e9-411">Method countryRegionCodes</span></span>

<span data-ttu-id="e50e9-412">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-412">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="e50e9-413">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="e50e9-413">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="e50e9-414">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-414">value</span></span>  
<span data-ttu-id="e50e9-415">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="e50e9-415">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="e50e9-416">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="e50e9-416">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="e50e9-417">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="e50e9-417">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-currentrow"></a><span data-ttu-id="e50e9-418">メソッド currentRow</span><span class="sxs-lookup"><span data-stu-id="e50e9-418">Method currentRow</span></span>

```xpp
public int currentRow()
```

### <a name="return-value---currentrow"></a><span data-ttu-id="e50e9-419">戻り値 - currentRow</span><span class="sxs-lookup"><span data-stu-id="e50e9-419">Return Value - currentRow</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="e50e9-420">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="e50e9-420">Method dataRelationPath</span></span>

<span data-ttu-id="e50e9-421">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-421">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="e50e9-422">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="e50e9-422">Parameters - dataRelationPath</span></span>

<span data-ttu-id="e50e9-423">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-423">value</span></span>  
<span data-ttu-id="e50e9-424">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="e50e9-424">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="e50e9-425">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="e50e9-425">Return Value - dataRelationPath</span></span>

<span data-ttu-id="e50e9-426">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="e50e9-426">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="e50e9-427">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="e50e9-427">Remarks - dataRelationPath</span></span>

<span data-ttu-id="e50e9-428">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-428">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="e50e9-429">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="e50e9-429">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasourceobject"></a><span data-ttu-id="e50e9-430">メソッド dataSourceObject</span><span class="sxs-lookup"><span data-stu-id="e50e9-430">Method dataSourceObject</span></span>

```xpp
public FormDataSource dataSourceObject()
```

### <a name="return-value---datasourceobject"></a><span data-ttu-id="e50e9-431">戻り値 - dataSourceObject</span><span class="sxs-lookup"><span data-stu-id="e50e9-431">Return Value - dataSourceObject</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="e50e9-432">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="e50e9-432">Method displayTarget</span></span>

<span data-ttu-id="e50e9-433">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-433">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="e50e9-434">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="e50e9-434">Parameters - displayTarget</span></span>

<span data-ttu-id="e50e9-435">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-435">value</span></span>  
<span data-ttu-id="e50e9-436">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-436">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="e50e9-437">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="e50e9-437">Return Value - displayTarget</span></span>

<span data-ttu-id="e50e9-438">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-438">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="e50e9-439">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="e50e9-439">Method dragDrop</span></span>

<span data-ttu-id="e50e9-440">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-440">Determines whether drag-and-drop operations are enabled or disabled for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="e50e9-441">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="e50e9-441">Parameters - dragDrop</span></span>

<span data-ttu-id="e50e9-442">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-442">value</span></span>  
<span data-ttu-id="e50e9-443">ドラッグ アンド ドロップの動作が有効かどうかを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-443">An integer value that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="e50e9-444">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="e50e9-444">Return Value - dragDrop</span></span>

<span data-ttu-id="e50e9-445">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="e50e9-445">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="examples---dragdrop"></a><span data-ttu-id="e50e9-446">例 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="e50e9-446">Examples - dragDrop</span></span>

<span data-ttu-id="e50e9-447">次の例は、ドラッグ アンド ドロップの動作が有効かどうかを示す値を返すか、設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-447">The following example shows how to return or set the value that indicates whether drag-and-drop behavior is enabled.</span></span>

```xpp
boolean dDragDrop; 
// The ctrl variable was previously assigned  
// as a FormControl value. 
// Retrieve the drag-and-drop-enabled value. 
dDragDrop = ctrl.dragDrop(); 
// Set the drag�and�drop-enabled value. 
ctrl.dragDrop(true);
```

## <a name="method-dragover"></a><span data-ttu-id="e50e9-448">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="e50e9-448">Method dragOver</span></span>

<span data-ttu-id="e50e9-449">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-449">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="e50e9-450">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="e50e9-450">Parameters - dragOver</span></span>

<span data-ttu-id="e50e9-451">dragSource</span><span class="sxs-lookup"><span data-stu-id="e50e9-451">dragSource</span></span>  
<span data-ttu-id="e50e9-452">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-452">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="e50e9-453">dragMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-453">dragMode</span></span>  
<span data-ttu-id="e50e9-454">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-454">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="e50e9-455">x</span><span class="sxs-lookup"><span data-stu-id="e50e9-455">x</span></span>  
<span data-ttu-id="e50e9-456">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-456">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="e50e9-457">y</span><span class="sxs-lookup"><span data-stu-id="e50e9-457">y</span></span>  
<span data-ttu-id="e50e9-458">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-458">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="e50e9-459">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="e50e9-459">Return Value - dragOver</span></span>

<span data-ttu-id="e50e9-460">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-460">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="e50e9-461">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="e50e9-461">Method dragOverEx</span></span>

<span data-ttu-id="e50e9-462">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-462">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="e50e9-463">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="e50e9-463">Parameters - dragOverEx</span></span>

<span data-ttu-id="e50e9-464">dragSource</span><span class="sxs-lookup"><span data-stu-id="e50e9-464">dragSource</span></span>  
<span data-ttu-id="e50e9-465">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-465">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="e50e9-466">dragMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-466">dragMode</span></span>  
<span data-ttu-id="e50e9-467">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-467">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="e50e9-468">x</span><span class="sxs-lookup"><span data-stu-id="e50e9-468">x</span></span>  
<span data-ttu-id="e50e9-469">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-469">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="e50e9-470">y</span><span class="sxs-lookup"><span data-stu-id="e50e9-470">y</span></span>  
<span data-ttu-id="e50e9-471">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-471">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="e50e9-472">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="e50e9-472">Return Value - dragOverEx</span></span>

<span data-ttu-id="e50e9-473">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-473">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="e50e9-474">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="e50e9-474">Method dragText</span></span>

<span data-ttu-id="e50e9-475">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-475">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="e50e9-476">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="e50e9-476">Return Value - dragText</span></span>

<span data-ttu-id="e50e9-477">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="e50e9-477">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-editautopostback"></a><span data-ttu-id="e50e9-478">メソッド editAutoPostback</span><span class="sxs-lookup"><span data-stu-id="e50e9-478">Method editAutoPostback</span></span>

```xpp
public boolean editAutoPostback([boolean value])
```

### <a name="parameters---editautopostback"></a><span data-ttu-id="e50e9-479">パラメーター - editAutoPostback</span><span class="sxs-lookup"><span data-stu-id="e50e9-479">Parameters - editAutoPostback</span></span>

<span data-ttu-id="e50e9-480">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-480">value</span></span>  

### <a name="return-value---editautopostback"></a><span data-ttu-id="e50e9-481">戻り値 - editAutoPostback</span><span class="sxs-lookup"><span data-stu-id="e50e9-481">Return Value - editAutoPostback</span></span>

## <a name="method-enabled"></a><span data-ttu-id="e50e9-482">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="e50e9-482">Method enabled</span></span>

<span data-ttu-id="e50e9-483">オブジェクトが有効か無効かを決定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-483">Determines whether the object is enabled or disabled.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="e50e9-484">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="e50e9-484">Parameters - enabled</span></span>

<span data-ttu-id="e50e9-485">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-485">value</span></span>  
<span data-ttu-id="e50e9-486">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-486">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="e50e9-487">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="e50e9-487">Return Value - enabled</span></span>

<span data-ttu-id="e50e9-488">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="e50e9-488">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="e50e9-489">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="e50e9-489">Remarks - enabled</span></span>

<span data-ttu-id="e50e9-490">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-490">The enabled property lets you enable or disable controls at run time.</span></span> <span data-ttu-id="e50e9-491">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-491">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="e50e9-492">また、読み取り専用情報を提供するエラー メッセージなど、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-492">You can also disable a control that is used only for display purposes, such as an error message that provides read-only information.</span></span>

### <a name="examples---enabled"></a><span data-ttu-id="e50e9-493">例 - enabled</span><span class="sxs-lookup"><span data-stu-id="e50e9-493">Examples - enabled</span></span>

<span data-ttu-id="e50e9-494">次の例は、コントロールの有効なプロパティを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-494">The following example shows how to return and set the enabled property for a control.</span></span>

```xpp
// Return the value of the enabled property. 
info(strfmt("enabled: %1",this.enabled())); 
// Set the enabled property. 
this.enabled(false);
```

## <a name="method-extendedstyle"></a><span data-ttu-id="e50e9-495">メソッド extendedStyle</span><span class="sxs-lookup"><span data-stu-id="e50e9-495">Method extendedStyle</span></span>

```xpp
public str extendedStyle([str value])
```

### <a name="parameters---extendedstyle"></a><span data-ttu-id="e50e9-496">パラメーター - extendedStyle</span><span class="sxs-lookup"><span data-stu-id="e50e9-496">Parameters - extendedStyle</span></span>

<span data-ttu-id="e50e9-497">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-497">value</span></span>  

### <a name="return-value---extendedstyle"></a><span data-ttu-id="e50e9-498">戻り値 - extendedStyle</span><span class="sxs-lookup"><span data-stu-id="e50e9-498">Return Value - extendedStyle</span></span>

## <a name="method-fieldbinding"></a><span data-ttu-id="e50e9-499">メソッド fieldBinding</span><span class="sxs-lookup"><span data-stu-id="e50e9-499">Method fieldBinding</span></span>

<span data-ttu-id="e50e9-500">FieldBinding 派生クラスへのコントロールのテーブルおよびフィールド バインディングを取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-500">Retrieves the table and field bindings of the control into a FieldBinding derived class.</span></span>

```xpp
public FieldBinding fieldBinding()
```

### <a name="return-value---fieldbinding"></a><span data-ttu-id="e50e9-501">戻り値 - fieldBinding</span><span class="sxs-lookup"><span data-stu-id="e50e9-501">Return Value - fieldBinding</span></span>

<span data-ttu-id="e50e9-502">コントロールのテーブルおよびフィールド バインディングを含む FieldBinding 派生クラス。</span><span class="sxs-lookup"><span data-stu-id="e50e9-502">A FieldBinding derived class that contains the table and field bindings of the control.</span></span>

## <a name="method-formatstr"></a><span data-ttu-id="e50e9-503">メソッド formatStr</span><span class="sxs-lookup"><span data-stu-id="e50e9-503">Method formatStr</span></span>

```xpp
public str formatStr([int rowNumber], [boolean display], [int maxWidth], [boolean forceSignWhenDisplaceNegative], [boolean formatForExport])
```

### <a name="parameters---formatstr"></a><span data-ttu-id="e50e9-504">パラメーター - formatStr</span><span class="sxs-lookup"><span data-stu-id="e50e9-504">Parameters - formatStr</span></span>

<span data-ttu-id="e50e9-505">rowNumber</span><span class="sxs-lookup"><span data-stu-id="e50e9-505">rowNumber</span></span>  

<!-- -->

<span data-ttu-id="e50e9-506">表示</span><span class="sxs-lookup"><span data-stu-id="e50e9-506">display</span></span>  

<!-- -->

<span data-ttu-id="e50e9-507">maxWidth</span><span class="sxs-lookup"><span data-stu-id="e50e9-507">maxWidth</span></span>  

<!-- -->

<span data-ttu-id="e50e9-508">forceSignWhenDisplaceNegative</span><span class="sxs-lookup"><span data-stu-id="e50e9-508">forceSignWhenDisplaceNegative</span></span>  

<!-- -->

<span data-ttu-id="e50e9-509">formatForExport</span><span class="sxs-lookup"><span data-stu-id="e50e9-509">formatForExport</span></span>  

### <a name="return-value---formatstr"></a><span data-ttu-id="e50e9-510">戻り値 - formatStr</span><span class="sxs-lookup"><span data-stu-id="e50e9-510">Return Value - formatStr</span></span>

## <a name="method-formrun"></a><span data-ttu-id="e50e9-511">メソッド formRun</span><span class="sxs-lookup"><span data-stu-id="e50e9-511">Method formRun</span></span>

```xpp
public xFormRun formRun()
```

### <a name="return-value---formrun"></a><span data-ttu-id="e50e9-512">戻り値 - formRun</span><span class="sxs-lookup"><span data-stu-id="e50e9-512">Return Value - formRun</span></span>

## <a name="method-getbinding"></a><span data-ttu-id="e50e9-513">メソッド getBinding</span><span class="sxs-lookup"><span data-stu-id="e50e9-513">Method getBinding</span></span>

```xpp
public FormBinding getBinding(str propertyName)
```

### <a name="parameters---getbinding"></a><span data-ttu-id="e50e9-514">パラメーター - getBinding</span><span class="sxs-lookup"><span data-stu-id="e50e9-514">Parameters - getBinding</span></span>

<span data-ttu-id="e50e9-515">propertyName</span><span class="sxs-lookup"><span data-stu-id="e50e9-515">propertyName</span></span>  

### <a name="return-value---getbinding"></a><span data-ttu-id="e50e9-516">戻り値 - getBinding</span><span class="sxs-lookup"><span data-stu-id="e50e9-516">Return Value - getBinding</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="e50e9-517">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="e50e9-517">Method hasChanged</span></span>

<span data-ttu-id="e50e9-518">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-518">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="e50e9-519">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="e50e9-519">Parameters - hasChanged</span></span>

<span data-ttu-id="e50e9-520">val</span><span class="sxs-lookup"><span data-stu-id="e50e9-520">val</span></span>  
<span data-ttu-id="e50e9-521">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="e50e9-521">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="e50e9-522">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="e50e9-522">Return Value - hasChanged</span></span>

<span data-ttu-id="e50e9-523">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="e50e9-523">true if the contents of the control have changed; otherwise, false.</span></span>

### <a name="examples---haschanged"></a><span data-ttu-id="e50e9-524">例 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="e50e9-524">Examples - hasChanged</span></span>

<span data-ttu-id="e50e9-525">次の例は、コントロールの内容が変更されたかどうかを示す値を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-525">The following example shows how to return and set the value that indicates whether the contents of the control have changed.</span></span>

```xpp
boolean bHasChanged; 
// The ctrl variable was previously assigned 
// as a FormControl value. 
// Retrieve the hasChanged value. 
bHasChanged = ctrl.hasChanged(); 
// Modify the hasChanged value. 
ctrl.hasChanged(true);
```

## <a name="method-hasusersetting"></a><span data-ttu-id="e50e9-526">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="e50e9-526">Method hasUserSetting</span></span>

<span data-ttu-id="e50e9-527">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-527">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="e50e9-528">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="e50e9-528">Return Value - hasUserSetting</span></span>

<span data-ttu-id="e50e9-529">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="e50e9-529">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="e50e9-530">メソッド height</span><span class="sxs-lookup"><span data-stu-id="e50e9-530">Method height</span></span>

<span data-ttu-id="e50e9-531">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-531">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="e50e9-532">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="e50e9-532">Parameters - height</span></span>

<span data-ttu-id="e50e9-533">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-533">value</span></span>  
<span data-ttu-id="e50e9-534">高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-534">An integer value that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="e50e9-535">モード</span><span class="sxs-lookup"><span data-stu-id="e50e9-535">mode</span></span>  
<span data-ttu-id="e50e9-536">高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-536">An integer value that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="e50e9-537">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="e50e9-537">Return Value - height</span></span>

<span data-ttu-id="e50e9-538">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="e50e9-538">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="e50e9-539">備考 - height</span><span class="sxs-lookup"><span data-stu-id="e50e9-539">Remarks - height</span></span>

<span data-ttu-id="e50e9-540">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-540">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="e50e9-541">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-541">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="e50e9-542">モード</span><span class="sxs-lookup"><span data-stu-id="e50e9-542">Mode</span></span>              | <span data-ttu-id="e50e9-543">高さの計算</span><span class="sxs-lookup"><span data-stu-id="e50e9-543">Height calculation</span></span>                                                                         |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e50e9-544">-1 � 正確</span><span class="sxs-lookup"><span data-stu-id="e50e9-544">-1 � Exact</span></span>        | <span data-ttu-id="e50e9-545">ピクセル単位のコントロールの正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-545">The exact height of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="e50e9-546">0 � 自動</span><span class="sxs-lookup"><span data-stu-id="e50e9-546">0 � Auto</span></span>          | <span data-ttu-id="e50e9-547">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-547">The height of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="e50e9-548">1 � 列の高さ</span><span class="sxs-lookup"><span data-stu-id="e50e9-548">1 � Column height</span></span> | <span data-ttu-id="e50e9-549">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="e50e9-549">The layout of the form determines the height of the control.</span></span>                               |

<span data-ttu-id="e50e9-550">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-550">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="e50e9-551">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-551">Method heightMode</span></span>

<span data-ttu-id="e50e9-552">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-552">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="e50e9-553">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-553">Parameters - heightMode</span></span>

<span data-ttu-id="e50e9-554">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-554">value</span></span>  
<span data-ttu-id="e50e9-555">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-555">An integer value that indicates how the control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="e50e9-556">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-556">Return Value - heightMode</span></span>

<span data-ttu-id="e50e9-557">計算モード。</span><span class="sxs-lookup"><span data-stu-id="e50e9-557">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="e50e9-558">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-558">Remarks - heightMode</span></span>

<span data-ttu-id="e50e9-559">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-559">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="e50e9-560">モード</span><span class="sxs-lookup"><span data-stu-id="e50e9-560">Mode</span></span>          | <span data-ttu-id="e50e9-561">高さの計算</span><span class="sxs-lookup"><span data-stu-id="e50e9-561">Height calculation</span></span>                                                                         |
|---------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e50e9-562">正確</span><span class="sxs-lookup"><span data-stu-id="e50e9-562">Exact</span></span>         | <span data-ttu-id="e50e9-563">ピクセル単位のコントロールの正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-563">The exact height of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="e50e9-564">自動</span><span class="sxs-lookup"><span data-stu-id="e50e9-564">Auto</span></span>          | <span data-ttu-id="e50e9-565">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-565">The height of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="e50e9-566">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="e50e9-566">Column height</span></span> | <span data-ttu-id="e50e9-567">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="e50e9-567">The layout of the form determines the height of the control.</span></span>                               |

<span data-ttu-id="e50e9-568">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="e50e9-568">The height of the control might change when the calculation mode is set to Auto or Column height.</span></span>

### <a name="examples---heightmode"></a><span data-ttu-id="e50e9-569">例 - heightMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-569">Examples - heightMode</span></span>

<span data-ttu-id="e50e9-570">次の例は、フォーム コントロールの高さ計算モードを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-570">The following example shows how to return and set the height calculation mode for a form control.</span></span>

```xpp
int nHeightMode; 
// The ctrl variable was previously assigned 
// as a form control variable. 
// Retrieve the height mode. 
nHeightMode = ctrl.HeightMode(); 
// Set the height mode. 
ctrl.heightMode(-1); 
// Set the height. 
ctrl.heightValue(16);
```

## <a name="method-heightvalue"></a><span data-ttu-id="e50e9-571">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="e50e9-571">Method heightValue</span></span>

<span data-ttu-id="e50e9-572">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-572">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="e50e9-573">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="e50e9-573">Parameters - heightValue</span></span>

<span data-ttu-id="e50e9-574">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-574">value</span></span>  
<span data-ttu-id="e50e9-575">高さをピクセル単位で指定する整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-575">An integer value that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="e50e9-576">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="e50e9-576">Return Value - heightValue</span></span>

<span data-ttu-id="e50e9-577">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="e50e9-577">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="e50e9-578">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="e50e9-578">Remarks - heightValue</span></span>

<span data-ttu-id="e50e9-579">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="e50e9-579">The height of the control is not changed unless the Exact height calculation mode is used.</span></span>

### <a name="examples---heightvalue"></a><span data-ttu-id="e50e9-580">例 - heightValue</span><span class="sxs-lookup"><span data-stu-id="e50e9-580">Examples - heightValue</span></span>

<span data-ttu-id="e50e9-581">次の例は、フォーム コントロールの高さの値を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-581">The following example shows how to return and set the height value of a form control.</span></span>

```xpp
int nHeightValue; 
// The ctrl variable was previously assigned 
// as a form control variable. 
// Retrieve the height value. 
nHeightValue = ctrl.heightValue(); 
// Set the height value. 
ctrl.heightMode(-1); 
ctrl.heightValue(22);
```

## <a name="method-helpfield"></a><span data-ttu-id="e50e9-582">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="e50e9-582">Method helpField</span></span>

<span data-ttu-id="e50e9-583">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-583">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="e50e9-584">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="e50e9-584">Return Value - helpField</span></span>

<span data-ttu-id="e50e9-585">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="e50e9-585">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="e50e9-586">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="e50e9-586">Remarks - helpField</span></span>

<span data-ttu-id="e50e9-587">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="e50e9-587">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="e50e9-588">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-588">Use the helpText method to set the value of the Help text.</span></span>

### <a name="examples---helpfield"></a><span data-ttu-id="e50e9-589">例 - helpField</span><span class="sxs-lookup"><span data-stu-id="e50e9-589">Examples - helpField</span></span>

<span data-ttu-id="e50e9-590">次の例は、helpField メソッドの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-590">The following example shows how to use the helpField method.</span></span>

```xpp
str strHelp; 
strHelp = this.helpField();
```

## <a name="method-helptext"></a><span data-ttu-id="e50e9-591">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="e50e9-591">Method helpText</span></span>

<span data-ttu-id="e50e9-592">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-592">Gets or sets the Help text that is displayed at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="e50e9-593">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="e50e9-593">Parameters - helpText</span></span>

<span data-ttu-id="e50e9-594">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-594">value</span></span>  
<span data-ttu-id="e50e9-595">コントロールのヘルプ テキストとして割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-595">The value to assign as the Help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="e50e9-596">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="e50e9-596">Return Value - helpText</span></span>

<span data-ttu-id="e50e9-597">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="e50e9-597">The string that should be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="e50e9-598">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="e50e9-598">Remarks - helpText</span></span>

<span data-ttu-id="e50e9-599">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-599">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="e50e9-600">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="e50e9-600">The Help text must not exceed 250 characters.</span></span>

### <a name="examples---helptext"></a><span data-ttu-id="e50e9-601">例 - helpText</span><span class="sxs-lookup"><span data-stu-id="e50e9-601">Examples - helpText</span></span>

<span data-ttu-id="e50e9-602">次の例は、コントロールのヘルプ テキストを設定して返す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-602">The following example shows how to set and return the Help text for a control.</span></span>

```xpp
// objCtrl previously assigned to a control 
// Retrieve existing help text. 
print objCtrl.helpText(); 
// Specify new help text. 
objCtrl.helpText("My new help text");
```

## <a name="method-hierarchyparent"></a><span data-ttu-id="e50e9-603">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="e50e9-603">Method hierarchyParent</span></span>

<span data-ttu-id="e50e9-604">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-604">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="e50e9-605">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="e50e9-605">Parameters - hierarchyParent</span></span>

<span data-ttu-id="e50e9-606">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-606">value</span></span>  
<span data-ttu-id="e50e9-607">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-607">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="e50e9-608">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="e50e9-608">Return Value - hierarchyParent</span></span>

<span data-ttu-id="e50e9-609">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-609">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="e50e9-610">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="e50e9-610">Method hWnd</span></span>

<span data-ttu-id="e50e9-611">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-611">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="e50e9-612">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="e50e9-612">Return Value - hWnd</span></span>

<span data-ttu-id="e50e9-613">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="e50e9-613">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="e50e9-614">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="e50e9-614">Remarks - hWnd</span></span>

<span data-ttu-id="e50e9-615">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-615">The handle can be used with the Windows API.</span></span>

### <a name="examples---hwnd"></a><span data-ttu-id="e50e9-616">例 - hWnd</span><span class="sxs-lookup"><span data-stu-id="e50e9-616">Examples - hWnd</span></span>

<span data-ttu-id="e50e9-617">次の例は、コントロールの Windows ハンドルを取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-617">The following example shows how to retrieve the Windows handle for a control.</span></span>

```xpp
int h; 
h = this.hWnd(); 
info (strfmt("hWnd: %1", h));
```

## <a name="method-id"></a><span data-ttu-id="e50e9-618">メソッド id</span><span class="sxs-lookup"><span data-stu-id="e50e9-618">Method id</span></span>

<span data-ttu-id="e50e9-619">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-619">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="e50e9-620">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="e50e9-620">Return Value - id</span></span>

<span data-ttu-id="e50e9-621">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="e50e9-621">The ID of the control.</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="e50e9-622">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="e50e9-622">Method isDisplayed</span></span>

<span data-ttu-id="e50e9-623">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-623">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="e50e9-624">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="e50e9-624">Return Value - isDisplayed</span></span>

<span data-ttu-id="e50e9-625">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="e50e9-625">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="e50e9-626">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="e50e9-626">Remarks - isDisplayed</span></span>

<span data-ttu-id="e50e9-627">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-627">To modify the visible state of the control, call the visible method.</span></span>

### <a name="examples---isdisplayed"></a><span data-ttu-id="e50e9-628">例 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="e50e9-628">Examples - isDisplayed</span></span>

<span data-ttu-id="e50e9-629">次の例は、コントロールが可視かどうかを判断する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-629">The following example shows how to determine whether a control is visible.</span></span>

```xpp
info(strfmt("isDisplayed: %1", this.isDisplayed()));
```

## <a name="method-iseditable"></a><span data-ttu-id="e50e9-630">メソッド isEditable</span><span class="sxs-lookup"><span data-stu-id="e50e9-630">Method isEditable</span></span>

```xpp
public boolean isEditable()
```

### <a name="return-value---iseditable"></a><span data-ttu-id="e50e9-631">戻り値 - isEditable</span><span class="sxs-lookup"><span data-stu-id="e50e9-631">Return Value - isEditable</span></span>

## <a name="method-isenabled"></a><span data-ttu-id="e50e9-632">メソッド isEnabled</span><span class="sxs-lookup"><span data-stu-id="e50e9-632">Method isEnabled</span></span>

```xpp
public boolean isEnabled()
```

### <a name="return-value---isenabled"></a><span data-ttu-id="e50e9-633">戻り値 - isEnabled</span><span class="sxs-lookup"><span data-stu-id="e50e9-633">Return Value - isEnabled</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="e50e9-634">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="e50e9-634">Method isRestricted</span></span>

<span data-ttu-id="e50e9-635">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-635">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="e50e9-636">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="e50e9-636">Return Value - isRestricted</span></span>

<span data-ttu-id="e50e9-637">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="e50e9-637">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="e50e9-638">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="e50e9-638">Method isUserSetupEnabled</span></span>

<span data-ttu-id="e50e9-639">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-639">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="e50e9-640">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="e50e9-640">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="e50e9-641">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="e50e9-641">neededSetupRights</span></span>  
<span data-ttu-id="e50e9-642">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-642">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="e50e9-643">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="e50e9-643">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="e50e9-644">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="e50e9-644">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="e50e9-645">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="e50e9-645">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="e50e9-646">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-646">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e50e9-647">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="e50e9-647">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="e50e9-648">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="e50e9-648">No changes can be made to the control.</span></span> <span data-ttu-id="e50e9-649">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-649">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="e50e9-650">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="e50e9-650">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="e50e9-651">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-651">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="e50e9-652">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="e50e9-652">The user cannot move the control.</span></span>   |
| <span data-ttu-id="e50e9-653">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="e50e9-653">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="e50e9-654">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-654">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="e50e9-655">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-655">The user can also move the control.</span></span> |

<span data-ttu-id="e50e9-656">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="e50e9-656">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

### <a name="examples---isusersetupenabled"></a><span data-ttu-id="e50e9-657">例 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="e50e9-657">Examples - isUserSetupEnabled</span></span>

<span data-ttu-id="e50e9-658">次の例は、コントロールのユーザー設定権限を決定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-658">The following example shows how to determine the user setup rights for a control.</span></span>

```xpp
FormAllowUserSetup formAllowUserSetup = FormAllowUserSetup::No; 
switch (true) 
{ 
    case this.isUserSetupEnabled(FormAllowUserSetup::Yes): 
        formAllowUserSetup = FormAllowUserSetup::Yes; 
        break; 
    case this.isUserSetupEnabled(FormAllowUserSetup::Restricted): 
        formAllowUserSetup = FormAllowUserSetup::Restricted; 
        break; 
    case this.isUserSetupEnabled(FormAllowUserSetup::No): 
       formAllowUserSetup = FormAllowUserSetup::No; 
        break; 
} 
info (strfmt("formAllowUserSetup: %1", formAllowUserSetup));
```

## <a name="method-isvisible"></a><span data-ttu-id="e50e9-659">メソッド isVisible</span><span class="sxs-lookup"><span data-stu-id="e50e9-659">Method isVisible</span></span>

<span data-ttu-id="e50e9-660">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-660">Retrieves a value that indicates whether the control is visible.</span></span>

```xpp
public boolean isVisible()
```

### <a name="return-value---isvisible"></a><span data-ttu-id="e50e9-661">戻り値 - isVisible</span><span class="sxs-lookup"><span data-stu-id="e50e9-661">Return Value - isVisible</span></span>

<span data-ttu-id="e50e9-662">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="e50e9-662">true if the control is visible; otherwise, false.</span></span>

## <a name="method-isvisibleonclient"></a><span data-ttu-id="e50e9-663">メソッド isVisibleOnClient</span><span class="sxs-lookup"><span data-stu-id="e50e9-663">Method isVisibleOnClient</span></span>

```xpp
public boolean isVisibleOnClient()
```

### <a name="return-value---isvisibleonclient"></a><span data-ttu-id="e50e9-664">戻り値 - isVisibleOnClient</span><span class="sxs-lookup"><span data-stu-id="e50e9-664">Return Value - isVisibleOnClient</span></span>

## <a name="method-labeltext"></a><span data-ttu-id="e50e9-665">メソッド labelText</span><span class="sxs-lookup"><span data-stu-id="e50e9-665">Method labelText</span></span>

<span data-ttu-id="e50e9-666">コントロールのラベル テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-666">Retrieves the label text for the control.</span></span>

```xpp
public str labelText()
```

### <a name="return-value---labeltext"></a><span data-ttu-id="e50e9-667">戻り値 - labelText</span><span class="sxs-lookup"><span data-stu-id="e50e9-667">Return Value - labelText</span></span>

<span data-ttu-id="e50e9-668">コントロールのラベル テキスト。コントロールにラベル テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="e50e9-668">The label text for the control; an empty string if there is no label text for the control.</span></span>

## <a name="method-left"></a><span data-ttu-id="e50e9-669">メソッド left</span><span class="sxs-lookup"><span data-stu-id="e50e9-669">Method left</span></span>

<span data-ttu-id="e50e9-670">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-670">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="e50e9-671">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="e50e9-671">Parameters - left</span></span>

<span data-ttu-id="e50e9-672">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-672">value</span></span>  
<span data-ttu-id="e50e9-673">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-673">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="e50e9-674">モード</span><span class="sxs-lookup"><span data-stu-id="e50e9-674">mode</span></span>  
<span data-ttu-id="e50e9-675">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-675">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="e50e9-676">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="e50e9-676">Return Value - left</span></span>

<span data-ttu-id="e50e9-677">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="e50e9-677">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="e50e9-678">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-678">Method leftMode</span></span>

<span data-ttu-id="e50e9-679">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-679">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="e50e9-680">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-680">Parameters - leftMode</span></span>

<span data-ttu-id="e50e9-681">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-681">value</span></span>  
<span data-ttu-id="e50e9-682">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-682">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="e50e9-683">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-683">Return Value - leftMode</span></span>

<span data-ttu-id="e50e9-684">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="e50e9-684">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="e50e9-685">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="e50e9-685">Method leftValue</span></span>

<span data-ttu-id="e50e9-686">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-686">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="e50e9-687">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="e50e9-687">Parameters - leftValue</span></span>

<span data-ttu-id="e50e9-688">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-688">value</span></span>  
<span data-ttu-id="e50e9-689">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-689">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="e50e9-690">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="e50e9-690">Return Value - leftValue</span></span>

<span data-ttu-id="e50e9-691">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="e50e9-691">The horizontal position of the control in the form.</span></span>

## <a name="method-lockwindowupdate"></a><span data-ttu-id="e50e9-692">メソッド lockWindowUpdate</span><span class="sxs-lookup"><span data-stu-id="e50e9-692">Method lockWindowUpdate</span></span>

<span data-ttu-id="e50e9-693">更新のコントロールのウィンドウをロックまたはロック解除します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-693">Locks or unlocks the window of the control for update.</span></span>

```xpp
public boolean lockWindowUpdate(boolean lock)
```

### <a name="parameters---lockwindowupdate"></a><span data-ttu-id="e50e9-694">パラメーター - lockWindowUpdate</span><span class="sxs-lookup"><span data-stu-id="e50e9-694">Parameters - lockWindowUpdate</span></span>

<span data-ttu-id="e50e9-695">lock</span><span class="sxs-lookup"><span data-stu-id="e50e9-695">lock</span></span>  
<span data-ttu-id="e50e9-696">ブール値: ウィンドウをロックする場合は true、ウィンドウをロック解除するには false。</span><span class="sxs-lookup"><span data-stu-id="e50e9-696">A Boolean value: true to lock the window, and false to unlock the window.</span></span>

### <a name="return-value---lockwindowupdate"></a><span data-ttu-id="e50e9-697">戻り値 - lockWindowUpdate</span><span class="sxs-lookup"><span data-stu-id="e50e9-697">Return Value - lockWindowUpdate</span></span>

<span data-ttu-id="e50e9-698">操作が成功した場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="e50e9-698">true if the operation was successful; otherwise, false.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="e50e9-699">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="e50e9-699">Method markAsUserAdd</span></span>

<span data-ttu-id="e50e9-700">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="e50e9-700">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="e50e9-701">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="e50e9-701">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="e50e9-702">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-702">value</span></span>  
<span data-ttu-id="e50e9-703">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-703">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="e50e9-704">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="e50e9-704">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="e50e9-705">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="e50e9-705">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="e50e9-706">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="e50e9-706">Method mouseDblClick</span></span>

<span data-ttu-id="e50e9-707">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-707">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="e50e9-708">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="e50e9-708">Parameters - mouseDblClick</span></span>

<span data-ttu-id="e50e9-709">x</span><span class="sxs-lookup"><span data-stu-id="e50e9-709">x</span></span>  
<span data-ttu-id="e50e9-710">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-710">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-711">y</span><span class="sxs-lookup"><span data-stu-id="e50e9-711">y</span></span>  
<span data-ttu-id="e50e9-712">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-712">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-713">ボタン</span><span class="sxs-lookup"><span data-stu-id="e50e9-713">button</span></span>  
<span data-ttu-id="e50e9-714">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-714">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-715">Ctrl</span><span class="sxs-lookup"><span data-stu-id="e50e9-715">Ctrl</span></span>  
<span data-ttu-id="e50e9-716">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-716">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-717">シフト</span><span class="sxs-lookup"><span data-stu-id="e50e9-717">Shift</span></span>  
<span data-ttu-id="e50e9-718">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-718">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="e50e9-719">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="e50e9-719">Return Value - mouseDblClick</span></span>

<span data-ttu-id="e50e9-720">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="e50e9-720">0 (zero) if the event has been handled.</span></span>

### <a name="examples---mousedblclick"></a><span data-ttu-id="e50e9-721">例 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="e50e9-721">Examples - mouseDblClick</span></span>

<span data-ttu-id="e50e9-722">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-722">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="e50e9-723">次の例は、Infolog に mouseDblClick イベントのパラメーターを表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-723">The following example shows how to display the parameters of a mouseDblClick event in the Infolog.</span></span>

```xpp
public int mouseDblClick(int x,  
                         int y,  
                         int button, 
                         boolean Ctrl, 
                         boolean Shift) 
{ 
    int ret; 
    if (Shift) 
    { 
        info("Shift set"); 
    } 
    if (Ctrl) 
    { 
        info("Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-mousedown"></a><span data-ttu-id="e50e9-724">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="e50e9-724">Method mouseDown</span></span>

<span data-ttu-id="e50e9-725">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-725">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="e50e9-726">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="e50e9-726">Parameters - mouseDown</span></span>

<span data-ttu-id="e50e9-727">x</span><span class="sxs-lookup"><span data-stu-id="e50e9-727">x</span></span>  
<span data-ttu-id="e50e9-728">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-728">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-729">y</span><span class="sxs-lookup"><span data-stu-id="e50e9-729">y</span></span>  
<span data-ttu-id="e50e9-730">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-730">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-731">ボタン</span><span class="sxs-lookup"><span data-stu-id="e50e9-731">button</span></span>  
<span data-ttu-id="e50e9-732">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-732">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-733">Ctrl</span><span class="sxs-lookup"><span data-stu-id="e50e9-733">Ctrl</span></span>  
<span data-ttu-id="e50e9-734">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-734">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-735">シフト</span><span class="sxs-lookup"><span data-stu-id="e50e9-735">Shift</span></span>  
<span data-ttu-id="e50e9-736">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-736">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="e50e9-737">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="e50e9-737">Return Value - mouseDown</span></span>

<span data-ttu-id="e50e9-738">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="e50e9-738">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="e50e9-739">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="e50e9-739">Remarks - mouseDown</span></span>

<span data-ttu-id="e50e9-740">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-740">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="e50e9-741">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-741">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="examples---mousedown"></a><span data-ttu-id="e50e9-742">例 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="e50e9-742">Examples - mouseDown</span></span>

<span data-ttu-id="e50e9-743">次の例は、Infolog に mouseDown イベントのパラメーターを表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-743">The following example shows how to display the parameters of a mouseDown event in the Infolog.</span></span>

```xpp
public int mouseDown(int x,  
                              int y,  
                              int button, 
                              boolean Ctrl, 
                              boolean Shift) 
{ 
    int ret; 
    if (Shift) 
    { 
        info("Shift set"); 
    } 
    if (Ctrl) 
    { 
        info("Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-mousemove"></a><span data-ttu-id="e50e9-744">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="e50e9-744">Method mouseMove</span></span>

<span data-ttu-id="e50e9-745">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-745">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="e50e9-746">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="e50e9-746">Parameters - mouseMove</span></span>

<span data-ttu-id="e50e9-747">x</span><span class="sxs-lookup"><span data-stu-id="e50e9-747">x</span></span>  
<span data-ttu-id="e50e9-748">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-748">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-749">y</span><span class="sxs-lookup"><span data-stu-id="e50e9-749">y</span></span>  
<span data-ttu-id="e50e9-750">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-750">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-751">ボタン</span><span class="sxs-lookup"><span data-stu-id="e50e9-751">button</span></span>  
<span data-ttu-id="e50e9-752">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-752">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-753">Ctrl</span><span class="sxs-lookup"><span data-stu-id="e50e9-753">Ctrl</span></span>  
<span data-ttu-id="e50e9-754">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-754">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-755">シフト</span><span class="sxs-lookup"><span data-stu-id="e50e9-755">Shift</span></span>  
<span data-ttu-id="e50e9-756">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-756">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="e50e9-757">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="e50e9-757">Return Value - mouseMove</span></span>

<span data-ttu-id="e50e9-758">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="e50e9-758">0 (zero) if the event has been handled.</span></span>

### <a name="examples---mousemove"></a><span data-ttu-id="e50e9-759">例 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="e50e9-759">Examples - mouseMove</span></span>

<span data-ttu-id="e50e9-760">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-760">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="e50e9-761">次の例は、Infolog に mouseMove イベントのパラメーターを表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-761">The following example shows how to display the parameters of a mouseMove event in the Infolog.</span></span>

```xpp
public int mouseMove(int x,  
                     int y,  
                     int button, 
                     boolean Ctrl, 
                     boolean Shift) 
{ 
    int ret; 
    if (Shift) 
    { 
        info("Shift set"); 
    } 
    if (Ctrl) 
    { 
        info("Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-mouseup"></a><span data-ttu-id="e50e9-762">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="e50e9-762">Method mouseUp</span></span>

<span data-ttu-id="e50e9-763">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-763">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="e50e9-764">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="e50e9-764">Parameters - mouseUp</span></span>

<span data-ttu-id="e50e9-765">x</span><span class="sxs-lookup"><span data-stu-id="e50e9-765">x</span></span>  
<span data-ttu-id="e50e9-766">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-766">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-767">y</span><span class="sxs-lookup"><span data-stu-id="e50e9-767">y</span></span>  
<span data-ttu-id="e50e9-768">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-768">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-769">ボタン</span><span class="sxs-lookup"><span data-stu-id="e50e9-769">button</span></span>  
<span data-ttu-id="e50e9-770">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-770">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-771">Ctrl</span><span class="sxs-lookup"><span data-stu-id="e50e9-771">Ctrl</span></span>  
<span data-ttu-id="e50e9-772">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-772">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-773">シフト</span><span class="sxs-lookup"><span data-stu-id="e50e9-773">Shift</span></span>  
<span data-ttu-id="e50e9-774">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-774">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="e50e9-775">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="e50e9-775">Return Value - mouseUp</span></span>

<span data-ttu-id="e50e9-776">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="e50e9-776">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="e50e9-777">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="e50e9-777">Remarks - mouseUp</span></span>

<span data-ttu-id="e50e9-778">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-778">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="e50e9-779">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-779">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="examples---mouseup"></a><span data-ttu-id="e50e9-780">例 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="e50e9-780">Examples - mouseUp</span></span>

<span data-ttu-id="e50e9-781">次の例は、Infolog に mouseUp イベントのパラメーターを表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-781">The following example shows how to display the parameters of a mouseUp event in the Infolog.</span></span>

```xpp
public int mouseUp(int x,  
                   int y,  
                   int button, 
                   boolean Ctrl, 
                   boolean Shift) 
{ 
    int ret; 
    if (Shift) 
    { 
        info("Shift set"); 
    } 
    if (Ctrl) 
    { 
        info("Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-name"></a><span data-ttu-id="e50e9-782">メソッド名</span><span class="sxs-lookup"><span data-stu-id="e50e9-782">Method name</span></span>

<span data-ttu-id="e50e9-783">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-783">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="e50e9-784">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="e50e9-784">Parameters - name</span></span>

<span data-ttu-id="e50e9-785">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-785">value</span></span>  
<span data-ttu-id="e50e9-786">コントロールに割り当てる名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="e50e9-786">The name to assign to the control; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="e50e9-787">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="e50e9-787">Return Value - name</span></span>

<span data-ttu-id="e50e9-788">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="e50e9-788">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="e50e9-789">備考 - name</span><span class="sxs-lookup"><span data-stu-id="e50e9-789">Remarks - name</span></span>

<span data-ttu-id="e50e9-790">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e50e9-790">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="e50e9-791">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="e50e9-791">It must start with a letter.</span></span>
-   <span data-ttu-id="e50e9-792">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="e50e9-792">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="e50e9-793">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-793">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="e50e9-794">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="e50e9-794">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="e50e9-795">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="e50e9-795">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="e50e9-796">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="e50e9-796">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="e50e9-797">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="e50e9-797">Parameters - neededPermission</span></span>

<span data-ttu-id="e50e9-798">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-798">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="e50e9-799">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="e50e9-799">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="e50e9-800">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="e50e9-800">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="e50e9-801">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="e50e9-801">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="e50e9-802">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="e50e9-802">Method parentControl</span></span>

<span data-ttu-id="e50e9-803">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-803">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="e50e9-804">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="e50e9-804">Return Value - parentControl</span></span>

<span data-ttu-id="e50e9-805">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="e50e9-805">The parent control for the control.</span></span>

## <a name="method-resourcebundlename"></a><span data-ttu-id="e50e9-806">メソッド resourceBundleName</span><span class="sxs-lookup"><span data-stu-id="e50e9-806">Method resourceBundleName</span></span>

```xpp
public str resourceBundleName()
```

### <a name="return-value---resourcebundlename"></a><span data-ttu-id="e50e9-807">戻り値 - resourceBundleName</span><span class="sxs-lookup"><span data-stu-id="e50e9-807">Return Value - resourceBundleName</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="e50e9-808">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="e50e9-808">Method securityKey</span></span>

<span data-ttu-id="e50e9-809">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-809">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="e50e9-810">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="e50e9-810">Parameters - securityKey</span></span>

<span data-ttu-id="e50e9-811">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-811">value</span></span>  
<span data-ttu-id="e50e9-812">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-812">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="e50e9-813">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="e50e9-813">Return Value - securityKey</span></span>

<span data-ttu-id="e50e9-814">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="e50e9-814">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

### <a name="examples---securitykey"></a><span data-ttu-id="e50e9-815">例 - securityKey</span><span class="sxs-lookup"><span data-stu-id="e50e9-815">Examples - securityKey</span></span>

<span data-ttu-id="e50e9-816">次の例では、コントロールのセキュリティ キー IDを取得して割り当てる方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-816">The following example shows how to retrieve and assign a security key ID for a control.</span></span>

```xpp
DictSecurityKey dsk; 
securityKeyId ski; 
// objCtrl previously assigned. 
// Assign a security key ID to the control. 
objCtrl.securityKey(securitykeynum(AdminDaily)); 
// Retrieve the security key ID from the control. 
ski = objCtrl.securityKey(); 
if (ski != 0) 
{ 
    dsk = new DictSecurityKey(ski); 
    if (dsk) 
    { 
        print strfmt("Security Key ID: %1 Security Key Name: %2", 
                     ski, 
                     dsk.name()); 
    } 
}
```

## <a name="method-showcontextmenu"></a><span data-ttu-id="e50e9-817">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="e50e9-817">Method showContextMenu</span></span>

<span data-ttu-id="e50e9-818">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-818">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="e50e9-819">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="e50e9-819">Parameters - showContextMenu</span></span>

<span data-ttu-id="e50e9-820">menuHandle</span><span class="sxs-lookup"><span data-stu-id="e50e9-820">menuHandle</span></span>  
<span data-ttu-id="e50e9-821">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="e50e9-821">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="e50e9-822">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="e50e9-822">Return Value - showContextMenu</span></span>

<span data-ttu-id="e50e9-823">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-823">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-getcontextmenuoptions"></a><span data-ttu-id="e50e9-824">メソッド getContextMenuOptions</span><span class="sxs-lookup"><span data-stu-id="e50e9-824">Method getContextMenuOptions</span></span>

```xpp
public str getContextMenuOptions()
```

### <a name="return-value---getcontextmenuoptions"></a><span data-ttu-id="e50e9-825">戻り値 - getContextMenuOptions</span><span class="sxs-lookup"><span data-stu-id="e50e9-825">Return Value - getContextMenuOptions</span></span>

## <a name="method-skip"></a><span data-ttu-id="e50e9-826">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="e50e9-826">Method skip</span></span>

<span data-ttu-id="e50e9-827">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-827">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="e50e9-828">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="e50e9-828">Parameters - skip</span></span>

<span data-ttu-id="e50e9-829">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-829">value</span></span>  
<span data-ttu-id="e50e9-830">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="e50e9-830">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="e50e9-831">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="e50e9-831">Return Value - skip</span></span>

<span data-ttu-id="e50e9-832">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="e50e9-832">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="e50e9-833">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="e50e9-833">Remarks - skip</span></span>

<span data-ttu-id="e50e9-834">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-834">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

### <a name="examples---skip"></a><span data-ttu-id="e50e9-835">例 - skip</span><span class="sxs-lookup"><span data-stu-id="e50e9-835">Examples - skip</span></span>

<span data-ttu-id="e50e9-836">次のコード例は、コントロールのスキップ プロパティを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-836">The following code example shows how to return and set the skip property of a control.</span></span>

```xpp
// Return the value of the skip property. 
info(strfmt("skip: %1", this.skip())); 
// Set the value of the skip property. 
this.skip(true);
```

## <a name="method-templateid"></a><span data-ttu-id="e50e9-837">メソッド templateId</span><span class="sxs-lookup"><span data-stu-id="e50e9-837">Method templateId</span></span>

```xpp
public str templateId()
```

### <a name="return-value---templateid"></a><span data-ttu-id="e50e9-838">戻り値 - templateId</span><span class="sxs-lookup"><span data-stu-id="e50e9-838">Return Value - templateId</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="e50e9-839">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="e50e9-839">Method toolTip</span></span>

<span data-ttu-id="e50e9-840">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-840">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="e50e9-841">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="e50e9-841">Return Value - toolTip</span></span>

<span data-ttu-id="e50e9-842">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="e50e9-842">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="e50e9-843">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="e50e9-843">Remarks - toolTip</span></span>

<span data-ttu-id="e50e9-844">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-844">The method might be overridden to provide a value to the toolTip method.</span></span>

### <a name="examples---tooltip"></a><span data-ttu-id="e50e9-845">例 - toolTip</span><span class="sxs-lookup"><span data-stu-id="e50e9-845">Examples - toolTip</span></span>

<span data-ttu-id="e50e9-846">次の例は、toolTip メソッドを上書きする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-846">The following example shows how to override the toolTip method.</span></span>

```xpp
str toolTip() 
{ 
    return "Account numbers of customers eligible for discount"; 
}
```

## <a name="method-top"></a><span data-ttu-id="e50e9-847">メソッド top</span><span class="sxs-lookup"><span data-stu-id="e50e9-847">Method top</span></span>

<span data-ttu-id="e50e9-848">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-848">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="e50e9-849">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="e50e9-849">Parameters - top</span></span>

<span data-ttu-id="e50e9-850">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-850">value</span></span>  
<span data-ttu-id="e50e9-851">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-851">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="e50e9-852">モード</span><span class="sxs-lookup"><span data-stu-id="e50e9-852">mode</span></span>  
<span data-ttu-id="e50e9-853">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-853">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="e50e9-854">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="e50e9-854">Return Value - top</span></span>

<span data-ttu-id="e50e9-855">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="e50e9-855">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="e50e9-856">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-856">Method topMode</span></span>

<span data-ttu-id="e50e9-857">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-857">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="e50e9-858">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-858">Parameters - topMode</span></span>

<span data-ttu-id="e50e9-859">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-859">value</span></span>  
<span data-ttu-id="e50e9-860">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-860">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="e50e9-861">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-861">Return Value - topMode</span></span>

<span data-ttu-id="e50e9-862">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="e50e9-862">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="e50e9-863">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="e50e9-863">Method topValue</span></span>

<span data-ttu-id="e50e9-864">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-864">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="e50e9-865">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="e50e9-865">Parameters - topValue</span></span>

<span data-ttu-id="e50e9-866">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-866">value</span></span>  
<span data-ttu-id="e50e9-867">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-867">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="e50e9-868">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="e50e9-868">Return Value - topValue</span></span>

<span data-ttu-id="e50e9-869">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="e50e9-869">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="e50e9-870">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="e50e9-870">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="e50e9-871">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="e50e9-871">Parameters - type</span></span>

<span data-ttu-id="e50e9-872">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-872">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="e50e9-873">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="e50e9-873">Return Value - type</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="e50e9-874">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="e50e9-874">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="e50e9-875">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="e50e9-875">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="e50e9-876">データ</span><span class="sxs-lookup"><span data-stu-id="e50e9-876">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="e50e9-877">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="e50e9-877">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-updatewindow"></a><span data-ttu-id="e50e9-878">メソッド updateWindow</span><span class="sxs-lookup"><span data-stu-id="e50e9-878">Method updateWindow</span></span>

<span data-ttu-id="e50e9-879">コントロールのウィンドウを更新します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-879">Updates the window for the control.</span></span>

```xpp
public int updateWindow()
```

### <a name="return-value---updatewindow"></a><span data-ttu-id="e50e9-880">戻り値 - updateWindow</span><span class="sxs-lookup"><span data-stu-id="e50e9-880">Return Value - updateWindow</span></span>

<span data-ttu-id="e50e9-881">更新が成功した場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="e50e9-881">1 if the update was successful; otherwise, 0.</span></span>

## <a name="method-userdata"></a><span data-ttu-id="e50e9-882">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="e50e9-882">Method userData</span></span>

<span data-ttu-id="e50e9-883">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-883">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="e50e9-884">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="e50e9-884">Parameters - userData</span></span>

<span data-ttu-id="e50e9-885">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-885">value</span></span>  
<span data-ttu-id="e50e9-886">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-886">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="e50e9-887">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="e50e9-887">Return Value - userData</span></span>

<span data-ttu-id="e50e9-888">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="e50e9-888">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="e50e9-889">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="e50e9-889">Method userDataItem</span></span>

<span data-ttu-id="e50e9-890">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-890">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="e50e9-891">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="e50e9-891">Parameters - userDataItem</span></span>

<span data-ttu-id="e50e9-892">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-892">value</span></span>  
<span data-ttu-id="e50e9-893">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-893">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="e50e9-894">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="e50e9-894">Return Value - userDataItem</span></span>

<span data-ttu-id="e50e9-895">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="e50e9-895">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="e50e9-896">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="e50e9-896">Method userDataItems</span></span>

<span data-ttu-id="e50e9-897">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-897">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="e50e9-898">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="e50e9-898">Parameters - userDataItems</span></span>

<span data-ttu-id="e50e9-899">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-899">value</span></span>  
<span data-ttu-id="e50e9-900">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-900">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="e50e9-901">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="e50e9-901">Return Value - userDataItems</span></span>

<span data-ttu-id="e50e9-902">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="e50e9-902">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="e50e9-903">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="e50e9-903">Method userDisable</span></span>

<span data-ttu-id="e50e9-904">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-904">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="e50e9-905">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="e50e9-905">Parameters - userDisable</span></span>

<span data-ttu-id="e50e9-906">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-906">value</span></span>  
<span data-ttu-id="e50e9-907">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="e50e9-907">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="e50e9-908">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="e50e9-908">Return Value - userDisable</span></span>

<span data-ttu-id="e50e9-909">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="e50e9-909">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="e50e9-910">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="e50e9-910">Method userHeight</span></span>

<span data-ttu-id="e50e9-911">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-911">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="e50e9-912">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="e50e9-912">Parameters - userHeight</span></span>

<span data-ttu-id="e50e9-913">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-913">value</span></span>  
<span data-ttu-id="e50e9-914">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="e50e9-914">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="e50e9-915">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="e50e9-915">Return Value - userHeight</span></span>

<span data-ttu-id="e50e9-916">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="e50e9-916">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="e50e9-917">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="e50e9-917">Method userHide</span></span>

<span data-ttu-id="e50e9-918">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-918">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="e50e9-919">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="e50e9-919">Parameters - userHide</span></span>

<span data-ttu-id="e50e9-920">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-920">value</span></span>  
<span data-ttu-id="e50e9-921">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="e50e9-921">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="e50e9-922">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="e50e9-922">Return Value - userHide</span></span>

<span data-ttu-id="e50e9-923">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="e50e9-923">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="e50e9-924">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="e50e9-924">Remarks - userHide</span></span>

<span data-ttu-id="e50e9-925">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-925">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="e50e9-926">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-926">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="e50e9-927">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-927">This method lets you programmatically determine and set the value.</span></span>

### <a name="examples---userhide"></a><span data-ttu-id="e50e9-928">例 - userHide</span><span class="sxs-lookup"><span data-stu-id="e50e9-928">Examples - userHide</span></span>

<span data-ttu-id="e50e9-929">次の例は、コントロールがユーザーから隠されているかどうかを示す値を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-929">The following example shows how to return and set the value that indicates whether the control is hidden from the user.</span></span>

```xpp
int nUserHide; 
// The ctrl variable was previously assigned  
// as a control variable. 
// Retrieve the userHide value. 
nUserHide = ctrl.userHide(); 
// Set the userHide value. 
ctrl.userHide(1);
```

## <a name="method-userorgcontainer"></a><span data-ttu-id="e50e9-930">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="e50e9-930">Method userOrgContainer</span></span>

<span data-ttu-id="e50e9-931">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-931">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="e50e9-932">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="e50e9-932">Parameters - userOrgContainer</span></span>

<span data-ttu-id="e50e9-933">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-933">value</span></span>  
<span data-ttu-id="e50e9-934">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="e50e9-934">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="e50e9-935">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="e50e9-935">Return Value - userOrgContainer</span></span>

<span data-ttu-id="e50e9-936">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="e50e9-936">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="e50e9-937">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="e50e9-937">Method userOrgSibling</span></span>

<span data-ttu-id="e50e9-938">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-938">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="e50e9-939">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="e50e9-939">Parameters - userOrgSibling</span></span>

<span data-ttu-id="e50e9-940">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-940">value</span></span>  
<span data-ttu-id="e50e9-941">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="e50e9-941">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="e50e9-942">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="e50e9-942">Return Value - userOrgSibling</span></span>

<span data-ttu-id="e50e9-943">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="e50e9-943">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="e50e9-944">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="e50e9-944">Method userPromptText</span></span>

<span data-ttu-id="e50e9-945">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-945">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="e50e9-946">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="e50e9-946">Parameters - userPromptText</span></span>

<span data-ttu-id="e50e9-947">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-947">value</span></span>  
<span data-ttu-id="e50e9-948">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="e50e9-948">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="e50e9-949">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="e50e9-949">Return Value - userPromptText</span></span>

<span data-ttu-id="e50e9-950">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="e50e9-950">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="e50e9-951">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="e50e9-951">Method userSecurityLevel</span></span>

<span data-ttu-id="e50e9-952">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-952">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="e50e9-953">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="e50e9-953">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="e50e9-954">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-954">value</span></span>  
<span data-ttu-id="e50e9-955">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="e50e9-955">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="e50e9-956">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="e50e9-956">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="e50e9-957">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="e50e9-957">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="e50e9-958">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="e50e9-958">Method userSkip</span></span>

<span data-ttu-id="e50e9-959">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-959">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="e50e9-960">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="e50e9-960">Parameters - userSkip</span></span>

<span data-ttu-id="e50e9-961">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-961">value</span></span>  
<span data-ttu-id="e50e9-962">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="e50e9-962">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="e50e9-963">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="e50e9-963">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="e50e9-964">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="e50e9-964">Return Value - userSkip</span></span>

<span data-ttu-id="e50e9-965">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="e50e9-965">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

### <a name="examples---userskip"></a><span data-ttu-id="e50e9-966">例 - userSkip</span><span class="sxs-lookup"><span data-stu-id="e50e9-966">Examples - userSkip</span></span>

<span data-ttu-id="e50e9-967">次の例は、userSkip プロパティを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-967">The following example shows how to return and set the userSkip property.</span></span>

```xpp
int nUserSkip 
// The ctrl variable was previously assigned  
// as a FormControl value. 
// Return the userSkip property. 
nUserSkip = ctrl.userSkip(); 
// Set the userSkip property. 
ctrl.userSkip(1);
```

## <a name="method-userwidth"></a><span data-ttu-id="e50e9-968">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="e50e9-968">Method userWidth</span></span>

<span data-ttu-id="e50e9-969">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-969">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="e50e9-970">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="e50e9-970">Parameters - userWidth</span></span>

<span data-ttu-id="e50e9-971">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-971">value</span></span>  
<span data-ttu-id="e50e9-972">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="e50e9-972">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="e50e9-973">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="e50e9-973">Return Value - userWidth</span></span>

<span data-ttu-id="e50e9-974">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="e50e9-974">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="e50e9-975">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="e50e9-975">Remarks - userWidth</span></span>

<span data-ttu-id="e50e9-976">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-976">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="e50e9-977">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="e50e9-977">For example, if the user has specified 30 characters as the width for the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="e50e9-978">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-978">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

### <a name="examples---userwidth"></a><span data-ttu-id="e50e9-979">例 - userWidth</span><span class="sxs-lookup"><span data-stu-id="e50e9-979">Examples - userWidth</span></span>

<span data-ttu-id="e50e9-980">次の例は、フォーム コントロールのユーザーの幅を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-980">The following example shows how to return and set the user width of a form control.</span></span>

```xpp
int nWidth; 
// The ctrl variable was previously defined 
// as a FormControl value. 
// Return the width. 
nWidth = ctrl.userWidth(); 
// Specify the width. 
ctrl.userWidth(90);  // 15 characters * 6 pixels == 90
```

## <a name="method-valuestr"></a><span data-ttu-id="e50e9-981">メソッド valueStr</span><span class="sxs-lookup"><span data-stu-id="e50e9-981">Method valueStr</span></span>

<span data-ttu-id="e50e9-982">文字列形式のコントロールの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-982">Retrieves the value of the control in string format.</span></span>

```xpp
public str valueStr()
```

### <a name="return-value---valuestr"></a><span data-ttu-id="e50e9-983">戻り値 - valueStr</span><span class="sxs-lookup"><span data-stu-id="e50e9-983">Return Value - valueStr</span></span>

<span data-ttu-id="e50e9-984">文字列形式のコントロールの値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-984">The value of the control in string format.</span></span>

### <a name="remarks---valuestr"></a><span data-ttu-id="e50e9-985">備考 - valueStr</span><span class="sxs-lookup"><span data-stu-id="e50e9-985">Remarks - valueStr</span></span>

<span data-ttu-id="e50e9-986">valueStr メソッドは、データ ソースにバインドできます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-986">The valueStr method can be bound to the data source.</span></span> <span data-ttu-id="e50e9-987">valueStr メソッドは、コントロールの検証メソッドでは使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="e50e9-987">The valueStr method should never be used in control validation methods.</span></span> <span data-ttu-id="e50e9-988">代わりに、管理検証メソッドでテキスト メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-988">Instead, use the text method in control validation methods.</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="e50e9-989">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="e50e9-989">Method verticalSpacing</span></span>

<span data-ttu-id="e50e9-990">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-990">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="e50e9-991">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="e50e9-991">Parameters - verticalSpacing</span></span>

<span data-ttu-id="e50e9-992">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-992">value</span></span>  
<span data-ttu-id="e50e9-993">コントロールの AutoMode を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-993">An integer value that indicates the AutoMode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="e50e9-994">モード</span><span class="sxs-lookup"><span data-stu-id="e50e9-994">mode</span></span>  
<span data-ttu-id="e50e9-995">コントロールの AutoMode を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-995">An integer value that indicates the AutoMode for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="e50e9-996">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="e50e9-996">Return Value - verticalSpacing</span></span>

<span data-ttu-id="e50e9-997">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="e50e9-997">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="e50e9-998">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-998">Method verticalSpacingMode</span></span>

<span data-ttu-id="e50e9-999">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-999">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="e50e9-1000">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-1000">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="e50e9-1001">モード</span><span class="sxs-lookup"><span data-stu-id="e50e9-1001">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="e50e9-1002">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-1002">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="e50e9-1003">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1003">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="e50e9-1004">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="e50e9-1004">Method verticalSpacingValue</span></span>

<span data-ttu-id="e50e9-1005">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1005">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="e50e9-1006">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="e50e9-1006">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="e50e9-1007">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-1007">value</span></span>  
<span data-ttu-id="e50e9-1008">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1008">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="e50e9-1009">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="e50e9-1009">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="e50e9-1010">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1010">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="e50e9-1011">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="e50e9-1011">Method visible</span></span>

<span data-ttu-id="e50e9-1012">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1012">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="e50e9-1013">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="e50e9-1013">Parameters - visible</span></span>

<span data-ttu-id="e50e9-1014">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-1014">value</span></span>  
<span data-ttu-id="e50e9-1015">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1015">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="e50e9-1016">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="e50e9-1016">Return Value - visible</span></span>

<span data-ttu-id="e50e9-1017">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1017">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="e50e9-1018">メソッド width</span><span class="sxs-lookup"><span data-stu-id="e50e9-1018">Method width</span></span>

<span data-ttu-id="e50e9-1019">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1019">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="e50e9-1020">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="e50e9-1020">Parameters - width</span></span>

<span data-ttu-id="e50e9-1021">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-1021">value</span></span>  
<span data-ttu-id="e50e9-1022">幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1022">An integer value that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="e50e9-1023">モード</span><span class="sxs-lookup"><span data-stu-id="e50e9-1023">mode</span></span>  
<span data-ttu-id="e50e9-1024">幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1024">An integer value that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="e50e9-1025">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="e50e9-1025">Return Value - width</span></span>

<span data-ttu-id="e50e9-1026">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1026">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="e50e9-1027">備考 - width</span><span class="sxs-lookup"><span data-stu-id="e50e9-1027">Remarks - width</span></span>

<span data-ttu-id="e50e9-1028">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1028">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="e50e9-1029">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1029">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="e50e9-1030">モード</span><span class="sxs-lookup"><span data-stu-id="e50e9-1030">Mode</span></span>             | <span data-ttu-id="e50e9-1031">幅計算</span><span class="sxs-lookup"><span data-stu-id="e50e9-1031">Width calculation</span></span>                                                                         |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e50e9-1032">-1 � 正確</span><span class="sxs-lookup"><span data-stu-id="e50e9-1032">-1 � Exact</span></span>       | <span data-ttu-id="e50e9-1033">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1033">The exact width of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="e50e9-1034">0 � 自動</span><span class="sxs-lookup"><span data-stu-id="e50e9-1034">0 � Auto</span></span>         | <span data-ttu-id="e50e9-1035">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1035">The width of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="e50e9-1036">1 � 列の幅</span><span class="sxs-lookup"><span data-stu-id="e50e9-1036">1 � Column width</span></span> | <span data-ttu-id="e50e9-1037">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1037">The layout of the form determines the width of the control.</span></span>                               |

<span data-ttu-id="e50e9-1038">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1038">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="e50e9-1039">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-1039">Method widthMode</span></span>

<span data-ttu-id="e50e9-1040">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1040">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="e50e9-1041">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-1041">Parameters - widthMode</span></span>

<span data-ttu-id="e50e9-1042">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-1042">value</span></span>  
<span data-ttu-id="e50e9-1043">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1043">An integer value that indicates how the control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="e50e9-1044">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-1044">Return Value - widthMode</span></span>

<span data-ttu-id="e50e9-1045">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1045">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="e50e9-1046">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-1046">Remarks - widthMode</span></span>

<span data-ttu-id="e50e9-1047">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1047">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="e50e9-1048">モード</span><span class="sxs-lookup"><span data-stu-id="e50e9-1048">Mode</span></span>         | <span data-ttu-id="e50e9-1049">幅計算</span><span class="sxs-lookup"><span data-stu-id="e50e9-1049">Width calculation</span></span>                                                                         |
|--------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e50e9-1050">正確</span><span class="sxs-lookup"><span data-stu-id="e50e9-1050">Exact</span></span>        | <span data-ttu-id="e50e9-1051">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1051">The exact width of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="e50e9-1052">自動</span><span class="sxs-lookup"><span data-stu-id="e50e9-1052">Auto</span></span>         | <span data-ttu-id="e50e9-1053">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1053">The width of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="e50e9-1054">列の幅</span><span class="sxs-lookup"><span data-stu-id="e50e9-1054">Column width</span></span> | <span data-ttu-id="e50e9-1055">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1055">The layout of the form determines the width of the control.</span></span>                               |

<span data-ttu-id="e50e9-1056">計算モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1056">The width of the control might change when the calculation mode is set to Auto or Column width.</span></span>

### <a name="examples---widthmode"></a><span data-ttu-id="e50e9-1057">例 - widthMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-1057">Examples - widthMode</span></span>

<span data-ttu-id="e50e9-1058">次の例は、フォーム コントロールの幅計算モードを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1058">The following example shows how to return and set the width calculation mode for a form control.</span></span>

```xpp
int nWidthMode; 
// The ctrl variable was previously assigned 
// as a form control variable. 
// Retrieve the width mode. 
nWidthMode = ctrl.widthMode (); 
// Set the width mode. 
ctrl.widthMode(-1); 
// Set the width. 
ctrl.widthValue(180);
```

## <a name="method-widthvalue"></a><span data-ttu-id="e50e9-1059">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="e50e9-1059">Method widthValue</span></span>

<span data-ttu-id="e50e9-1060">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1060">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="e50e9-1061">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="e50e9-1061">Parameters - widthValue</span></span>

<span data-ttu-id="e50e9-1062">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-1062">value</span></span>  
<span data-ttu-id="e50e9-1063">幅をピクセル単位で指定する整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1063">An integer value that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="e50e9-1064">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="e50e9-1064">Return Value - widthValue</span></span>

<span data-ttu-id="e50e9-1065">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1065">The width of the control in pixels.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="e50e9-1066">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="e50e9-1066">Remarks - widthValue</span></span>

<span data-ttu-id="e50e9-1067">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1067">To change the width of the control, use the Exact width calculation mode.</span></span>

### <a name="examples---widthvalue"></a><span data-ttu-id="e50e9-1068">例 - widthValue</span><span class="sxs-lookup"><span data-stu-id="e50e9-1068">Examples - widthValue</span></span>

<span data-ttu-id="e50e9-1069">次の例は、フォーム コントロールの幅の値を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1069">The following example shows how to return and set the width value of a form control.</span></span>

```xpp
int nWidthValue; 
// The ctrl variable was previously assigned 
// as a form control value. 
// Retrieve the width value. 
nWidthValue = ctrl.widthValue(); 
// Set the width value. 
ctrl.widthMode(-1); 
ctrl.widthValue(160);
```

## <a name="method-displaycontrol"></a><span data-ttu-id="e50e9-1070">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="e50e9-1070">Method displayControl</span></span>

<span data-ttu-id="e50e9-1071">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1071">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-copy"></a><span data-ttu-id="e50e9-1072">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="e50e9-1072">Method copy</span></span>

<span data-ttu-id="e50e9-1073">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1073">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-paste"></a><span data-ttu-id="e50e9-1074">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="e50e9-1074">Method paste</span></span>

<span data-ttu-id="e50e9-1075">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1075">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-setfocus"></a><span data-ttu-id="e50e9-1076">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="e50e9-1076">Method setFocus</span></span>

<span data-ttu-id="e50e9-1077">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1077">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-cut"></a><span data-ttu-id="e50e9-1078">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="e50e9-1078">Method cut</span></span>

<span data-ttu-id="e50e9-1079">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1079">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-gotfocus"></a><span data-ttu-id="e50e9-1080">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="e50e9-1080">Method gotFocus</span></span>

<span data-ttu-id="e50e9-1081">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1081">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-dragleave"></a><span data-ttu-id="e50e9-1082">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="e50e9-1082">Method dragLeave</span></span>

<span data-ttu-id="e50e9-1083">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1083">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-lostfocus"></a><span data-ttu-id="e50e9-1084">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="e50e9-1084">Method lostFocus</span></span>

<span data-ttu-id="e50e9-1085">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1085">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-inputsearch"></a><span data-ttu-id="e50e9-1086">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="e50e9-1086">Method inputSearch</span></span>

<span data-ttu-id="e50e9-1087">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1087">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="e50e9-1088">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="e50e9-1088">Parameters - inputSearch</span></span>

<span data-ttu-id="e50e9-1089">searchStr</span><span class="sxs-lookup"><span data-stu-id="e50e9-1089">searchStr</span></span>  
<span data-ttu-id="e50e9-1090">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1090">The string value to use to filter data; optional.</span></span>

## <a name="method-settemplateid"></a><span data-ttu-id="e50e9-1091">メソッド setTemplateId</span><span class="sxs-lookup"><span data-stu-id="e50e9-1091">Method setTemplateId</span></span>

```xpp
public void setTemplateId([str value])
```

### <a name="parameters---settemplateid"></a><span data-ttu-id="e50e9-1092">パラメーター - setTemplateId</span><span class="sxs-lookup"><span data-stu-id="e50e9-1092">Parameters - setTemplateId</span></span>

<span data-ttu-id="e50e9-1093">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-1093">value</span></span>  

## <a name="method-prefcolumnsize"></a><span data-ttu-id="e50e9-1094">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="e50e9-1094">Method prefColumnSize</span></span>

<span data-ttu-id="e50e9-1095">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1095">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="e50e9-1096">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="e50e9-1096">Parameters - prefColumnSize</span></span>

<span data-ttu-id="e50e9-1097">width</span><span class="sxs-lookup"><span data-stu-id="e50e9-1097">width</span></span>  
<span data-ttu-id="e50e9-1098">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1098">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="e50e9-1099">height</span><span class="sxs-lookup"><span data-stu-id="e50e9-1099">height</span></span>  
<span data-ttu-id="e50e9-1100">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1100">The preferred height of the control.</span></span>

### <a name="examples---prefcolumnsize"></a><span data-ttu-id="e50e9-1101">例 - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="e50e9-1101">Examples - prefColumnSize</span></span>

<span data-ttu-id="e50e9-1102">次の例は、フォーム コントロールの優先幅と高さを設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1102">The following example shows how to set the preferred width and height of a form control.</span></span>

```xpp
// nWidth and nHeight are previously assigned int variables. 
// ctrl is a previously assigned FormControl variable. 
ctrl.prefColumnSize( nWidth, nHeight);
```

## <a name="method-update"></a><span data-ttu-id="e50e9-1103">メソッド update</span><span class="sxs-lookup"><span data-stu-id="e50e9-1103">Method update</span></span>

<span data-ttu-id="e50e9-1104">コントロールを更新します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1104">Updates the control.</span></span>

```xpp
public void update()
```

## <a name="method-run"></a><span data-ttu-id="e50e9-1105">メソッド run</span><span class="sxs-lookup"><span data-stu-id="e50e9-1105">Method run</span></span>

```xpp
public void run()
```

## <a name="method-lock"></a><span data-ttu-id="e50e9-1106">メソッド lock</span><span class="sxs-lookup"><span data-stu-id="e50e9-1106">Method lock</span></span>

<span data-ttu-id="e50e9-1107">フォーム コントロールをロックします。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1107">Locks the form control.</span></span>

```xpp
public void lock()
```

### <a name="remarks---lock"></a><span data-ttu-id="e50e9-1108">備考 - lock</span><span class="sxs-lookup"><span data-stu-id="e50e9-1108">Remarks - lock</span></span>

<span data-ttu-id="e50e9-1109">オブジェクトを変更し、他のユーザーが変更を加えるかどうか確信が持てない場合には、Lock コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1109">Use the Lock command when you modify an object and are not sure whether another user is about to make updates.</span></span> <span data-ttu-id="e50e9-1110">更新内容の保存が完了したら、ロック解除コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1110">When you have saved your updates, use the Unlock command.</span></span>

## <a name="method-mouseenter"></a><span data-ttu-id="e50e9-1111">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="e50e9-1111">Method mouseEnter</span></span>

<span data-ttu-id="e50e9-1112">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1112">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="e50e9-1113">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="e50e9-1113">Parameters - mouseEnter</span></span>

<span data-ttu-id="e50e9-1114">x</span><span class="sxs-lookup"><span data-stu-id="e50e9-1114">x</span></span>  
<span data-ttu-id="e50e9-1115">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1115">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-1116">y</span><span class="sxs-lookup"><span data-stu-id="e50e9-1116">y</span></span>  
<span data-ttu-id="e50e9-1117">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1117">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-1118">ボタン</span><span class="sxs-lookup"><span data-stu-id="e50e9-1118">button</span></span>  
<span data-ttu-id="e50e9-1119">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1119">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-1120">Ctrl</span><span class="sxs-lookup"><span data-stu-id="e50e9-1120">Ctrl</span></span>  
<span data-ttu-id="e50e9-1121">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1121">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="e50e9-1122">シフト</span><span class="sxs-lookup"><span data-stu-id="e50e9-1122">Shift</span></span>  
<span data-ttu-id="e50e9-1123">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1123">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="examples---mouseenter"></a><span data-ttu-id="e50e9-1124">例 - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="e50e9-1124">Examples - mouseEnter</span></span>

<span data-ttu-id="e50e9-1125">次の例は、Infolog に mouseEnter イベントのパラメーターを表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1125">The following example shows how to display the parameters of a mouseEnter event in the Infolog.</span></span>

```xpp
public void mouseEnter(int x,  
                      int y,  
                      int button, 
                      boolean Ctrl, 
                      boolean Shift) 
{ 
    if (Shift) 
    { 
        info("Shift set"); 
    } 
    if (Ctrl) 
    { 
        info("Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
}
```

## <a name="method-applybuild"></a><span data-ttu-id="e50e9-1126">メソッド applyBuild</span><span class="sxs-lookup"><span data-stu-id="e50e9-1126">Method applyBuild</span></span>

```xpp
public void applyBuild()
```

## <a name="method-drop"></a><span data-ttu-id="e50e9-1127">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="e50e9-1127">Method drop</span></span>

<span data-ttu-id="e50e9-1128">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1128">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="e50e9-1129">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="e50e9-1129">Parameters - drop</span></span>

<span data-ttu-id="e50e9-1130">dragSource</span><span class="sxs-lookup"><span data-stu-id="e50e9-1130">dragSource</span></span>  
<span data-ttu-id="e50e9-1131">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1131">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="e50e9-1132">dragMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-1132">dragMode</span></span>  
<span data-ttu-id="e50e9-1133">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1133">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="e50e9-1134">x</span><span class="sxs-lookup"><span data-stu-id="e50e9-1134">x</span></span>  
<span data-ttu-id="e50e9-1135">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1135">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="e50e9-1136">y</span><span class="sxs-lookup"><span data-stu-id="e50e9-1136">y</span></span>  
<span data-ttu-id="e50e9-1137">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1137">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-resetusersetting"></a><span data-ttu-id="e50e9-1138">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="e50e9-1138">Method resetUserSetting</span></span>

<span data-ttu-id="e50e9-1139">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1139">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-new"></a><span data-ttu-id="e50e9-1140">メソッド new</span><span class="sxs-lookup"><span data-stu-id="e50e9-1140">Method new</span></span>

```xpp
public void new(FormBuildControl build, xFormRun formRun)
```

### <a name="parameters---new"></a><span data-ttu-id="e50e9-1141">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="e50e9-1141">Parameters - new</span></span>

<span data-ttu-id="e50e9-1142">build</span><span class="sxs-lookup"><span data-stu-id="e50e9-1142">build</span></span>  

<!-- -->

<span data-ttu-id="e50e9-1143">formRun</span><span class="sxs-lookup"><span data-stu-id="e50e9-1143">formRun</span></span>  

## <a name="method-context"></a><span data-ttu-id="e50e9-1144">メソッド context</span><span class="sxs-lookup"><span data-stu-id="e50e9-1144">Method context</span></span>

<span data-ttu-id="e50e9-1145">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1145">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-unlock"></a><span data-ttu-id="e50e9-1146">メソッド unLock</span><span class="sxs-lookup"><span data-stu-id="e50e9-1146">Method unLock</span></span>

<span data-ttu-id="e50e9-1147">フォーム コントロールのロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1147">Unlocks a form control.</span></span>

```xpp
public void unLock(boolean update)
```

### <a name="parameters---unlock"></a><span data-ttu-id="e50e9-1148">パラメーター - unLock</span><span class="sxs-lookup"><span data-stu-id="e50e9-1148">Parameters - unLock</span></span>

<span data-ttu-id="e50e9-1149">更新</span><span class="sxs-lookup"><span data-stu-id="e50e9-1149">update</span></span>  
<span data-ttu-id="e50e9-1150">コントロールに加えられる変更を保存するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1150">A Boolean value that indicates whether to save the changes that are made to the control.</span></span>

## <a name="method-setresourcebundlename"></a><span data-ttu-id="e50e9-1151">メソッド setResourceBundleName</span><span class="sxs-lookup"><span data-stu-id="e50e9-1151">Method setResourceBundleName</span></span>

```xpp
public void setResourceBundleName([str value])
```

### <a name="parameters---setresourcebundlename"></a><span data-ttu-id="e50e9-1152">パラメーター - setResourceBundleName</span><span class="sxs-lookup"><span data-stu-id="e50e9-1152">Parameters - setResourceBundleName</span></span>

<span data-ttu-id="e50e9-1153">値</span><span class="sxs-lookup"><span data-stu-id="e50e9-1153">value</span></span>  

## <a name="method-selectedmenuoption"></a><span data-ttu-id="e50e9-1154">メソッド selectedMenuOption</span><span class="sxs-lookup"><span data-stu-id="e50e9-1154">Method selectedMenuOption</span></span>

```xpp
public void selectedMenuOption(int selectedOption)
```

### <a name="parameters---selectedmenuoption"></a><span data-ttu-id="e50e9-1155">パラメーター - selectedMenuOption</span><span class="sxs-lookup"><span data-stu-id="e50e9-1155">Parameters - selectedMenuOption</span></span>

<span data-ttu-id="e50e9-1156">selectedOption</span><span class="sxs-lookup"><span data-stu-id="e50e9-1156">selectedOption</span></span>  

## <a name="method-mouseleave"></a><span data-ttu-id="e50e9-1157">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="e50e9-1157">Method mouseLeave</span></span>

<span data-ttu-id="e50e9-1158">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1158">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-onpropchanged"></a><span data-ttu-id="e50e9-1159">メソッド onPropChanged</span><span class="sxs-lookup"><span data-stu-id="e50e9-1159">Method onPropChanged</span></span>

```xpp
public void onPropChanged([str propName])
```

### <a name="parameters---onpropchanged"></a><span data-ttu-id="e50e9-1160">パラメーター - onPropChanged</span><span class="sxs-lookup"><span data-stu-id="e50e9-1160">Parameters - onPropChanged</span></span>

<span data-ttu-id="e50e9-1161">propName</span><span class="sxs-lookup"><span data-stu-id="e50e9-1161">propName</span></span>  

## <a name="method-dropex"></a><span data-ttu-id="e50e9-1162">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="e50e9-1162">Method dropEx</span></span>

<span data-ttu-id="e50e9-1163">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1163">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="e50e9-1164">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="e50e9-1164">Parameters - dropEx</span></span>

<span data-ttu-id="e50e9-1165">dragSource</span><span class="sxs-lookup"><span data-stu-id="e50e9-1165">dragSource</span></span>  
<span data-ttu-id="e50e9-1166">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1166">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="e50e9-1167">dragMode</span><span class="sxs-lookup"><span data-stu-id="e50e9-1167">dragMode</span></span>  
<span data-ttu-id="e50e9-1168">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1168">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="e50e9-1169">x</span><span class="sxs-lookup"><span data-stu-id="e50e9-1169">x</span></span>  
<span data-ttu-id="e50e9-1170">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1170">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="e50e9-1171">y</span><span class="sxs-lookup"><span data-stu-id="e50e9-1171">y</span></span>  
<span data-ttu-id="e50e9-1172">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1172">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-initialize"></a><span data-ttu-id="e50e9-1173">メソッド initialize</span><span class="sxs-lookup"><span data-stu-id="e50e9-1173">Method initialize</span></span>

```xpp
public void initialize()
```

## <a name="method-enddrag"></a><span data-ttu-id="e50e9-1174">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="e50e9-1174">Method endDrag</span></span>

<span data-ttu-id="e50e9-1175">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1175">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="e50e9-1176">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="e50e9-1176">Remarks - endDrag</span></span>

<span data-ttu-id="e50e9-1177">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1177">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="e50e9-1178">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1178">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="examples---enddrag"></a><span data-ttu-id="e50e9-1179">例 - endDrag</span><span class="sxs-lookup"><span data-stu-id="e50e9-1179">Examples - endDrag</span></span>

<span data-ttu-id="e50e9-1180">次の例では、ユーザーがフォーム コントロールのドラッグを終了したときに、Infolog にメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="e50e9-1180">The following example displays a message in the Infolog when the user has finished dragging the form control.</span></span>

```xpp
public void endDrag() 
{  
    info("EndDrag completed"); 
    super(); 
}
```

