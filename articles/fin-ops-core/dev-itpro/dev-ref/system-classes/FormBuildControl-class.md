---
title: FormBuildControl クラス
description: このトピックでは、FormBuildControl クラスについて説明します。
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
ms.openlocfilehash: 8a2d9dd0aa0f8d5ebc81e5b0a233b2b7071e9a31
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502970"
---
# <a name="class-formbuildcontrol"></a><span data-ttu-id="c32c7-103">クラス FormBuildControl</span><span class="sxs-lookup"><span data-stu-id="c32c7-103">Class FormBuildControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildControl extends Object
```

<span data-ttu-id="c32c7-104">FormBuildControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="c32c7-104">The FormBuildControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="c32c7-105">備考</span><span class="sxs-lookup"><span data-stu-id="c32c7-105">Remarks</span></span>

<span data-ttu-id="c32c7-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="c32c7-107">例</span><span class="sxs-lookup"><span data-stu-id="c32c7-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="c32c7-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="c32c7-108">Methods</span></span>

| <span data-ttu-id="c32c7-109">方法</span><span class="sxs-lookup"><span data-stu-id="c32c7-109">Method</span></span>                                                                                                                                    | <span data-ttu-id="c32c7-110">説明</span><span class="sxs-lookup"><span data-stu-id="c32c7-110">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c32c7-111">public FormBuildControl addControl(FormControlType controlType, str controlName, \[FormBuildControl insertAfter\], \[boolean pushFront\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-111">public FormBuildControl addControl(FormControlType controlType, str controlName, \[FormBuildControl insertAfter\], \[boolean pushFront\])</span></span> | <span data-ttu-id="c32c7-112">指定したコントロール タイプに基づいて、コントロールにコントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-112">Adds a control to the control, based on the specified control type.</span></span>                                                                                |
| <span data-ttu-id="c32c7-113">public FormBuildControl addControlEx(str controlClass, str controlName, \[FormBuildControl insertAfter\], \[boolean pushFront\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-113">public FormBuildControl addControlEx(str controlClass, str controlName, \[FormBuildControl insertAfter\], \[boolean pushFront\])</span></span>          |                                                                                                                                                    |
| <span data-ttu-id="c32c7-114">public FormBuildControl addDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-114">public FormBuildControl addDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span></span>                                               | <span data-ttu-id="c32c7-115">指定したデータ フィールド情報に基づいて、コントロールにコントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-115">Adds a control to the control, based on the specified data field information.</span></span>                                                                      |
| <span data-ttu-id="c32c7-116">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-116">public boolean allowEdit(\[boolean value\])</span></span>                                                                                               |                                                                                                                                                    |
| <span data-ttu-id="c32c7-117">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-117">public boolean autoDeclaration(\[boolean value\])</span></span>                                                                                         |                                                                                                                                                    |
| <span data-ttu-id="c32c7-118">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-118">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span></span>                                                     | <span data-ttu-id="c32c7-119">指定されたデータ フィールドを、子コントロールとしてコントロールに追加できるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-119">Retrieves a value that indicates whether the specified data field can be added as a child control to the control.</span></span>                                  |
| <span data-ttu-id="c32c7-120">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-120">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                                                  |                                                                                                                                                    |
| <span data-ttu-id="c32c7-121">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="c32c7-121">public int containerId()</span></span>                                                                                                                  | <span data-ttu-id="c32c7-122">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-122">Retrieves the ID of the parent container for the control.</span></span>                                                                                          |
| <span data-ttu-id="c32c7-123">public int controlCount()</span><span class="sxs-lookup"><span data-stu-id="c32c7-123">public int controlCount()</span></span>                                                                                                                 | <span data-ttu-id="c32c7-124">コントロールに含まれるコントロールの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-124">Retrieves the number of controls that are contained in the control.</span></span>                                                                                |
| <span data-ttu-id="c32c7-125">public FormBuildControl controlNum(int controlNo)</span><span class="sxs-lookup"><span data-stu-id="c32c7-125">public FormBuildControl controlNum(int controlNo)</span></span>                                                                                         | <span data-ttu-id="c32c7-126">指定したインデックスを使用して、上位のコントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-126">Retrieves a contained control by using the specified index.</span></span>                                                                                        |
| <span data-ttu-id="c32c7-127">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-127">public str countryRegionCodes(\[str value\])</span></span>                                                                                              |                                                                                                                                                    |
| <span data-ttu-id="c32c7-128">public boolean editAutoPostback(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-128">public boolean editAutoPostback(\[boolean value\])</span></span>                                                                                        |                                                                                                                                                    |
| <span data-ttu-id="c32c7-129">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-129">public boolean enabled(\[boolean value\])</span></span>                                                                                                 |                                                                                                                                                    |
| <span data-ttu-id="c32c7-130">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-130">public str helpText(\[str value\])</span></span>                                                                                                        |                                                                                                                                                    |
| <span data-ttu-id="c32c7-131">public str extendedStyle(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-131">public str extendedStyle(\[str value\])</span></span>                                                                                                   |                                                                                                                                                    |
| <span data-ttu-id="c32c7-132">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-132">public int height(int value, \[int mode\])</span></span>                                                                                                |                                                                                                                                                    |
| <span data-ttu-id="c32c7-133">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-133">public int heightMode(\[int value\])</span></span>                                                                                                      |                                                                                                                                                    |
| <span data-ttu-id="c32c7-134">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-134">public int heightValue(\[int value\])</span></span>                                                                                                     |                                                                                                                                                    |
| <span data-ttu-id="c32c7-135">public str GetXppILImplementation()</span><span class="sxs-lookup"><span data-stu-id="c32c7-135">public str GetXppILImplementation()</span></span>                                                                                                       |                                                                                                                                                    |
| <span data-ttu-id="c32c7-136">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="c32c7-136">public boolean hasUserSetting()</span></span>                                                                                                           | <span data-ttu-id="c32c7-137">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-137">Indicates whether the control has custom user settings.</span></span>                                                                                            |
| <span data-ttu-id="c32c7-138">public int id()</span><span class="sxs-lookup"><span data-stu-id="c32c7-138">public int id()</span></span>                                                                                                                           | <span data-ttu-id="c32c7-139">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-139">Retrieves the ID of the control.</span></span>                                                                                                                   |
| <span data-ttu-id="c32c7-140">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="c32c7-140">public boolean isContainer()</span></span>                                                                                                              | <span data-ttu-id="c32c7-141">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-141">Retrieves a value that indicates whether the control is a container control.</span></span>                                                                       |
| <span data-ttu-id="c32c7-142">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-142">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                                                           | <span data-ttu-id="c32c7-143">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="c32c7-143">Marks or unmarks the control as a user-added control.</span></span>                                                                                              |
| <span data-ttu-id="c32c7-144">public int moveControl(int controlId, \[int insertAfterId\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-144">public int moveControl(int controlId, \[int insertAfterId\])</span></span>                                                                              | <span data-ttu-id="c32c7-145">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-145">Moves a specified control to the control.</span></span>                                                                                                          |
| <span data-ttu-id="c32c7-146">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-146">public str name(\[str value\])</span></span>                                                                                                            |                                                                                                                                                    |
| <span data-ttu-id="c32c7-147">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-147">public int neededPermission(\[int value\])</span></span>                                                                                                |                                                                                                                                                    |
| <span data-ttu-id="c32c7-148">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="c32c7-148">public container SysObsoleteAttribute()</span></span>                                                                                                   |                                                                                                                                                    |
| <span data-ttu-id="c32c7-149">public str previewPartRef(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-149">public str previewPartRef(\[str value\])</span></span>                                                                                                  |                                                                                                                                                    |
| <span data-ttu-id="c32c7-150">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-150">public boolean skip(\[boolean value\])</span></span>                                                                                                    |                                                                                                                                                    |
| <span data-ttu-id="c32c7-151">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="c32c7-151">public boolean SysObsoleteAttribute(container data)</span></span>                                                                                       |                                                                                                                                                    |
| <span data-ttu-id="c32c7-152">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-152">public int userDisable(\[int value\])</span></span>                                                                                                     | <span data-ttu-id="c32c7-153">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-153">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                |
| <span data-ttu-id="c32c7-154">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-154">public int userHeight(\[int value\])</span></span>                                                                                                      | <span data-ttu-id="c32c7-155">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-155">Gets or sets the custom user height for the control.</span></span>                                                                                               |
| <span data-ttu-id="c32c7-156">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-156">public int userHide(\[int value\])</span></span>                                                                                                        | <span data-ttu-id="c32c7-157">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-157">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                 |
| <span data-ttu-id="c32c7-158">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-158">public int userOrgContainer(\[int value\])</span></span>                                                                                                | <span data-ttu-id="c32c7-159">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-159">Gets or sets the organization container for the control.</span></span>                                                                                           |
| <span data-ttu-id="c32c7-160">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-160">public int userOrgSibling(\[int value\])</span></span>                                                                                                  | <span data-ttu-id="c32c7-161">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-161">Gets or sets the organization sibling for the control.</span></span>                                                                                             |
| <span data-ttu-id="c32c7-162">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-162">public str userPromptText(\[str value\])</span></span>                                                                                                  | <span data-ttu-id="c32c7-163">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-163">Gets or sets the user label text for the control.</span></span>                                                                                                  |
| <span data-ttu-id="c32c7-164">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-164">public int userSecurityLevel(\[int value\])</span></span>                                                                                               | <span data-ttu-id="c32c7-165">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-165">Gets or sets the user security level for the control.</span></span>                                                                                              |
| <span data-ttu-id="c32c7-166">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-166">public int userSkip(\[int value\])</span></span>                                                                                                        | <span data-ttu-id="c32c7-167">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-167">Sets or returns the value that indicates whether the form control is skipped when the user press the TAB key to navigate the controls on the form.</span></span> |
| <span data-ttu-id="c32c7-168">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-168">public int userWidth(\[int value\])</span></span>                                                                                                       | <span data-ttu-id="c32c7-169">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-169">Sets or returns the width of the control in pixels.</span></span>                                                                                                |
| <span data-ttu-id="c32c7-170">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-170">public boolean visible(\[boolean value\])</span></span>                                                                                                 |                                                                                                                                                    |
| <span data-ttu-id="c32c7-171">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-171">public int width(int value, \[int mode\])</span></span>                                                                                                 |                                                                                                                                                    |
| <span data-ttu-id="c32c7-172">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-172">public int widthMode(\[int value\])</span></span>                                                                                                       |                                                                                                                                                    |
| <span data-ttu-id="c32c7-173">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c32c7-173">public int widthValue(\[int value\])</span></span>                                                                                                      |                                                                                                                                                    |
| <span data-ttu-id="c32c7-174">public void RegisterXppILImplementation(str className)</span><span class="sxs-lookup"><span data-stu-id="c32c7-174">public void RegisterXppILImplementation(str className)</span></span>                                                                                    |                                                                                                                                                    |
| <span data-ttu-id="c32c7-175">public void new(FormContainer container)</span><span class="sxs-lookup"><span data-stu-id="c32c7-175">public void new(FormContainer container)</span></span>                                                                                                  |                                                                                                                                                    |
| <span data-ttu-id="c32c7-176">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="c32c7-176">public void resetUserSetting()</span></span>                                                                                                            | <span data-ttu-id="c32c7-177">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="c32c7-177">Resets the user settings for the control.</span></span>                                                                                                          |

## <a name="method-addcontrol"></a><span data-ttu-id="c32c7-178">メソッド addControl</span><span class="sxs-lookup"><span data-stu-id="c32c7-178">Method addControl</span></span>

<span data-ttu-id="c32c7-179">指定したコントロール タイプに基づいて、コントロールにコントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-179">Adds a control to the control, based on the specified control type.</span></span>

```xpp
public FormBuildControl addControl(FormControlType controlType, str controlName, [FormBuildControl insertAfter], [boolean pushFront])
```

### <a name="parameters---addcontrol"></a><span data-ttu-id="c32c7-180">パラメーター - addControl</span><span class="sxs-lookup"><span data-stu-id="c32c7-180">Parameters - addControl</span></span>

<span data-ttu-id="c32c7-181">controlType</span><span class="sxs-lookup"><span data-stu-id="c32c7-181">controlType</span></span>  
<span data-ttu-id="c32c7-182">新しいコントロールの名前を設定する文字列値。</span><span class="sxs-lookup"><span data-stu-id="c32c7-182">The string value to set the name of the new control to.</span></span>

<!-- -->

<span data-ttu-id="c32c7-183">controlName</span><span class="sxs-lookup"><span data-stu-id="c32c7-183">controlName</span></span>  
<span data-ttu-id="c32c7-184">新しいコントロールの名前を設定する文字列値。</span><span class="sxs-lookup"><span data-stu-id="c32c7-184">The string value to set the name of the new control to.</span></span>

<!-- -->

<span data-ttu-id="c32c7-185">insertAfter</span><span class="sxs-lookup"><span data-stu-id="c32c7-185">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="c32c7-186">pushFront</span><span class="sxs-lookup"><span data-stu-id="c32c7-186">pushFront</span></span>  

### <a name="return-value---addcontrol"></a><span data-ttu-id="c32c7-187">戻り値 - addControl</span><span class="sxs-lookup"><span data-stu-id="c32c7-187">Return Value - addControl</span></span>

<span data-ttu-id="c32c7-188">新たに追加されたコントロールを表す FormBuildControl オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="c32c7-188">A FormBuildControl object that represents the newly added control.</span></span>

## <a name="method-addcontrolex"></a><span data-ttu-id="c32c7-189">メソッド addControlEx</span><span class="sxs-lookup"><span data-stu-id="c32c7-189">Method addControlEx</span></span>

```xpp
public FormBuildControl addControlEx(str controlClass, str controlName, [FormBuildControl insertAfter], [boolean pushFront])
```

### <a name="parameters---addcontrolex"></a><span data-ttu-id="c32c7-190">パラメーター - addControlEx</span><span class="sxs-lookup"><span data-stu-id="c32c7-190">Parameters - addControlEx</span></span>

<span data-ttu-id="c32c7-191">controlClass</span><span class="sxs-lookup"><span data-stu-id="c32c7-191">controlClass</span></span>  

<!-- -->

<span data-ttu-id="c32c7-192">controlName</span><span class="sxs-lookup"><span data-stu-id="c32c7-192">controlName</span></span>  

<!-- -->

<span data-ttu-id="c32c7-193">insertAfter</span><span class="sxs-lookup"><span data-stu-id="c32c7-193">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="c32c7-194">pushFront</span><span class="sxs-lookup"><span data-stu-id="c32c7-194">pushFront</span></span>  

### <a name="return-value---addcontrolex"></a><span data-ttu-id="c32c7-195">戻り値 - addControlEx</span><span class="sxs-lookup"><span data-stu-id="c32c7-195">Return Value - addControlEx</span></span>

## <a name="method-adddatafield"></a><span data-ttu-id="c32c7-196">メソッド addDataField</span><span class="sxs-lookup"><span data-stu-id="c32c7-196">Method addDataField</span></span>

<span data-ttu-id="c32c7-197">指定したデータ フィールド情報に基づいて、コントロールにコントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-197">Adds a control to the control, based on the specified data field information.</span></span>

```xpp
public FormBuildControl addDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---adddatafield"></a><span data-ttu-id="c32c7-198">パラメーター - addDataField</span><span class="sxs-lookup"><span data-stu-id="c32c7-198">Parameters - addDataField</span></span>

<span data-ttu-id="c32c7-199">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="c32c7-199">dataSourceId</span></span>  
<span data-ttu-id="c32c7-200">データ フィールド型のインデックスを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c32c7-200">An integer value that indicates the index of the data field type; optional.</span></span>

<!-- -->

<span data-ttu-id="c32c7-201">fieldId</span><span class="sxs-lookup"><span data-stu-id="c32c7-201">fieldId</span></span>  
<span data-ttu-id="c32c7-202">データ フィールド型のインデックスを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c32c7-202">An integer value that indicates the index of the data field type; optional.</span></span>

<!-- -->

<span data-ttu-id="c32c7-203">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="c32c7-203">arrayIndex</span></span>  
<span data-ttu-id="c32c7-204">データ フィールド型のインデックスを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c32c7-204">An integer value that indicates the index of the data field type; optional.</span></span>

### <a name="return-value---adddatafield"></a><span data-ttu-id="c32c7-205">戻り値 - addDataField</span><span class="sxs-lookup"><span data-stu-id="c32c7-205">Return Value - addDataField</span></span>

<span data-ttu-id="c32c7-206">新たに追加されたコントロールを表す FormBuildControl オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="c32c7-206">A FormBuildControl object that represents the newly added control.</span></span>

### <a name="remarks---adddatafield"></a><span data-ttu-id="c32c7-207">備考 - addDataField</span><span class="sxs-lookup"><span data-stu-id="c32c7-207">Remarks - addDataField</span></span>

<span data-ttu-id="c32c7-208">追加するコントロールのタイプは、指定されたデータ フィールド情報に基づいて自動的に決定されます。</span><span class="sxs-lookup"><span data-stu-id="c32c7-208">The type of control that should be added is determined automatically, based on the specified data field information.</span></span> <span data-ttu-id="c32c7-209">値が指定されていないときは、arrayIndex パラメーターが既定値の 1 であるため、最初のインデックスが想定されます。</span><span class="sxs-lookup"><span data-stu-id="c32c7-209">The arrayIndex parameter has a default value of 1 when a value is not specified, so that the first index is assumed.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="c32c7-210">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="c32c7-210">Method allowEdit</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="c32c7-211">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="c32c7-211">Parameters - allowEdit</span></span>

<span data-ttu-id="c32c7-212">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-212">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="c32c7-213">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="c32c7-213">Return Value - allowEdit</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="c32c7-214">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="c32c7-214">Method autoDeclaration</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="c32c7-215">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="c32c7-215">Parameters - autoDeclaration</span></span>

<span data-ttu-id="c32c7-216">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-216">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="c32c7-217">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="c32c7-217">Return Value - autoDeclaration</span></span>

## <a name="method-canadddatafield"></a><span data-ttu-id="c32c7-218">メソッド canAddDataField</span><span class="sxs-lookup"><span data-stu-id="c32c7-218">Method canAddDataField</span></span>

<span data-ttu-id="c32c7-219">指定されたデータ フィールドを、子コントロールとしてコントロールに追加できるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-219">Retrieves a value that indicates whether the specified data field can be added as a child control to the control.</span></span>

```xpp
public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---canadddatafield"></a><span data-ttu-id="c32c7-220">パラメーター - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="c32c7-220">Parameters - canAddDataField</span></span>

<span data-ttu-id="c32c7-221">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="c32c7-221">dataSourceId</span></span>  
<span data-ttu-id="c32c7-222">データ フィールド型のインデックスを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c32c7-222">An integer value that indicates the index of the data field type; optional.</span></span>

<!-- -->

<span data-ttu-id="c32c7-223">fieldId</span><span class="sxs-lookup"><span data-stu-id="c32c7-223">fieldId</span></span>  
<span data-ttu-id="c32c7-224">データ フィールド型のインデックスを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c32c7-224">An integer value that indicates the index of the data field type; optional.</span></span>

<!-- -->

<span data-ttu-id="c32c7-225">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="c32c7-225">arrayIndex</span></span>  
<span data-ttu-id="c32c7-226">データ フィールド型のインデックスを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c32c7-226">An integer value that indicates the index of the data field type; optional.</span></span>

### <a name="return-value---canadddatafield"></a><span data-ttu-id="c32c7-227">戻り値 - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="c32c7-227">Return Value - canAddDataField</span></span>

<span data-ttu-id="c32c7-228">指定されたデータ フィールドを、子コントロールとしてコントロールに追加できるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c32c7-228">A Boolean value that indicates whether the specified data field can be added as a child control to the control.</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="c32c7-229">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="c32c7-229">Method configurationKey</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="c32c7-230">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="c32c7-230">Parameters - configurationKey</span></span>

<span data-ttu-id="c32c7-231">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-231">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="c32c7-232">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="c32c7-232">Return Value - configurationKey</span></span>

## <a name="method-containerid"></a><span data-ttu-id="c32c7-233">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="c32c7-233">Method containerId</span></span>

<span data-ttu-id="c32c7-234">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-234">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="c32c7-235">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="c32c7-235">Return Value - containerId</span></span>

<span data-ttu-id="c32c7-236">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="c32c7-236">The ID of the parent container.</span></span>

## <a name="method-controlcount"></a><span data-ttu-id="c32c7-237">メソッド controlCount</span><span class="sxs-lookup"><span data-stu-id="c32c7-237">Method controlCount</span></span>

<span data-ttu-id="c32c7-238">コントロールに含まれるコントロールの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-238">Retrieves the number of controls that are contained in the control.</span></span>

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a><span data-ttu-id="c32c7-239">戻り値 - controlCount</span><span class="sxs-lookup"><span data-stu-id="c32c7-239">Return Value - controlCount</span></span>

<span data-ttu-id="c32c7-240">コンテナー コントロールの場合、コントロール内に含まれているコントロールの数を示す整数値。それ以外の場合は、0 。</span><span class="sxs-lookup"><span data-stu-id="c32c7-240">An integer value that indicates the number of controls that are contained in the control if it is a container control; otherwise, 0.</span></span>

## <a name="method-controlnum"></a><span data-ttu-id="c32c7-241">メソッド controlNum</span><span class="sxs-lookup"><span data-stu-id="c32c7-241">Method controlNum</span></span>

<span data-ttu-id="c32c7-242">指定したインデックスを使用して、上位のコントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-242">Retrieves a contained control by using the specified index.</span></span>

```xpp
public FormBuildControl controlNum(int controlNo)
```

### <a name="parameters---controlnum"></a><span data-ttu-id="c32c7-243">パラメーター - controlNum</span><span class="sxs-lookup"><span data-stu-id="c32c7-243">Parameters - controlNum</span></span>

<span data-ttu-id="c32c7-244">controlNo</span><span class="sxs-lookup"><span data-stu-id="c32c7-244">controlNo</span></span>  
<span data-ttu-id="c32c7-245">取得する子コントロールのインデックスを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c32c7-245">An integer value that indicates the index of the child control to retrieve.</span></span>

### <a name="return-value---controlnum"></a><span data-ttu-id="c32c7-246">戻り値 - controlNum</span><span class="sxs-lookup"><span data-stu-id="c32c7-246">Return Value - controlNum</span></span>

<span data-ttu-id="c32c7-247">コンテナー コントロールである場合は、指定されたインデックスを持つ子コントロールを表す FormBuildControl オブジェクト; それ以外の場合は、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="c32c7-247">A FormBuildControl object that represents the child control that has the specified index if this is a container control; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

### <a name="remarks---controlnum"></a><span data-ttu-id="c32c7-248">備考 - controlNum</span><span class="sxs-lookup"><span data-stu-id="c32c7-248">Remarks - controlNum</span></span>

<span data-ttu-id="c32c7-249">指定した controlNo パラメーターが範囲外にある場合は、例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-249">If the specified controlNo parameter is out of range, an exception is raised.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="c32c7-250">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="c32c7-250">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="c32c7-251">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="c32c7-251">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="c32c7-252">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-252">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="c32c7-253">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="c32c7-253">Return Value - countryRegionCodes</span></span>

## <a name="method-editautopostback"></a><span data-ttu-id="c32c7-254">メソッド editAutoPostback</span><span class="sxs-lookup"><span data-stu-id="c32c7-254">Method editAutoPostback</span></span>

```xpp
public boolean editAutoPostback([boolean value])
```

### <a name="parameters---editautopostback"></a><span data-ttu-id="c32c7-255">パラメーター - editAutoPostback</span><span class="sxs-lookup"><span data-stu-id="c32c7-255">Parameters - editAutoPostback</span></span>

<span data-ttu-id="c32c7-256">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-256">value</span></span>  

### <a name="return-value---editautopostback"></a><span data-ttu-id="c32c7-257">戻り値 - editAutoPostback</span><span class="sxs-lookup"><span data-stu-id="c32c7-257">Return Value - editAutoPostback</span></span>

## <a name="method-enabled"></a><span data-ttu-id="c32c7-258">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="c32c7-258">Method enabled</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="c32c7-259">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="c32c7-259">Parameters - enabled</span></span>

<span data-ttu-id="c32c7-260">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-260">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="c32c7-261">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="c32c7-261">Return Value - enabled</span></span>

## <a name="method-helptext"></a><span data-ttu-id="c32c7-262">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="c32c7-262">Method helpText</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="c32c7-263">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="c32c7-263">Parameters - helpText</span></span>

<span data-ttu-id="c32c7-264">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-264">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="c32c7-265">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="c32c7-265">Return Value - helpText</span></span>

## <a name="method-extendedstyle"></a><span data-ttu-id="c32c7-266">メソッド extendedStyle</span><span class="sxs-lookup"><span data-stu-id="c32c7-266">Method extendedStyle</span></span>

```xpp
public str extendedStyle([str value])
```

### <a name="parameters---extendedstyle"></a><span data-ttu-id="c32c7-267">パラメーター - extendedStyle</span><span class="sxs-lookup"><span data-stu-id="c32c7-267">Parameters - extendedStyle</span></span>

<span data-ttu-id="c32c7-268">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-268">value</span></span>  

### <a name="return-value---extendedstyle"></a><span data-ttu-id="c32c7-269">戻り値 - extendedStyle</span><span class="sxs-lookup"><span data-stu-id="c32c7-269">Return Value - extendedStyle</span></span>

## <a name="method-height"></a><span data-ttu-id="c32c7-270">メソッド height</span><span class="sxs-lookup"><span data-stu-id="c32c7-270">Method height</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="c32c7-271">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="c32c7-271">Parameters - height</span></span>

<span data-ttu-id="c32c7-272">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-272">value</span></span>  

<!-- -->

<span data-ttu-id="c32c7-273">モード</span><span class="sxs-lookup"><span data-stu-id="c32c7-273">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="c32c7-274">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="c32c7-274">Return Value - height</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="c32c7-275">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="c32c7-275">Method heightMode</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="c32c7-276">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="c32c7-276">Parameters - heightMode</span></span>

<span data-ttu-id="c32c7-277">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-277">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="c32c7-278">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="c32c7-278">Return Value - heightMode</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="c32c7-279">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="c32c7-279">Method heightValue</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="c32c7-280">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="c32c7-280">Parameters - heightValue</span></span>

<span data-ttu-id="c32c7-281">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-281">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="c32c7-282">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="c32c7-282">Return Value - heightValue</span></span>

## <a name="method-getxppilimplementation"></a><span data-ttu-id="c32c7-283">メソッド GetXppILImplementation</span><span class="sxs-lookup"><span data-stu-id="c32c7-283">Method GetXppILImplementation</span></span>

```xpp
public str GetXppILImplementation()
```

### <a name="return-value---getxppilimplementation"></a><span data-ttu-id="c32c7-284">戻り値 - GetXppILImplementation</span><span class="sxs-lookup"><span data-stu-id="c32c7-284">Return Value - GetXppILImplementation</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="c32c7-285">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="c32c7-285">Method hasUserSetting</span></span>

<span data-ttu-id="c32c7-286">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-286">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="c32c7-287">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="c32c7-287">Return Value - hasUserSetting</span></span>

<span data-ttu-id="c32c7-288">コントロールにカスタム ユーザー設定があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c32c7-288">A Boolean value that indicates whether the control has custom user settings.</span></span>

## <a name="method-id"></a><span data-ttu-id="c32c7-289">メソッド id</span><span class="sxs-lookup"><span data-stu-id="c32c7-289">Method id</span></span>

<span data-ttu-id="c32c7-290">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-290">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="c32c7-291">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="c32c7-291">Return Value - id</span></span>

<span data-ttu-id="c32c7-292">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="c32c7-292">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="c32c7-293">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="c32c7-293">Method isContainer</span></span>

<span data-ttu-id="c32c7-294">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-294">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="c32c7-295">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="c32c7-295">Return Value - isContainer</span></span>

<span data-ttu-id="c32c7-296">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c32c7-296">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="c32c7-297">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="c32c7-297">Method markAsUserAdd</span></span>

<span data-ttu-id="c32c7-298">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="c32c7-298">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="c32c7-299">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="c32c7-299">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="c32c7-300">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-300">value</span></span>  
<span data-ttu-id="c32c7-301">コントロールをユーザーが追加したコントロールとしてマークするかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c32c7-301">A Boolean value that indicates whether to mark the control as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="c32c7-302">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="c32c7-302">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="c32c7-303">ユーザーが追加したコントロールとして、コントロールがマークされたかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c32c7-303">A Boolean value that indicates whether the control was marked as a user-added control.</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="c32c7-304">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="c32c7-304">Method moveControl</span></span>

<span data-ttu-id="c32c7-305">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-305">Moves a specified control to the control.</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="c32c7-306">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="c32c7-306">Parameters - moveControl</span></span>

<span data-ttu-id="c32c7-307">controlId</span><span class="sxs-lookup"><span data-stu-id="c32c7-307">controlId</span></span>  
<span data-ttu-id="c32c7-308">後にコントロールを挿入するコントロールの ID を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c32c7-308">An integer value that indicates the ID of the control to insert the control after; optional.</span></span>

<!-- -->

<span data-ttu-id="c32c7-309">insertAfterId</span><span class="sxs-lookup"><span data-stu-id="c32c7-309">insertAfterId</span></span>  
<span data-ttu-id="c32c7-310">後にコントロールを挿入するコントロールの ID を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="c32c7-310">An integer value that indicates the ID of the control to insert the control after; optional.</span></span>

### <a name="return-value---movecontrol"></a><span data-ttu-id="c32c7-311">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="c32c7-311">Return Value - moveControl</span></span>

<span data-ttu-id="c32c7-312">コントロールが正常に移動した場合は 1、それ以外の場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="c32c7-312">1 if the control was moved successfully; otherwise, 0.</span></span>

### <a name="remarks---movecontrol"></a><span data-ttu-id="c32c7-313">備考 - moveControl</span><span class="sxs-lookup"><span data-stu-id="c32c7-313">Remarks - moveControl</span></span>

<span data-ttu-id="c32c7-314">一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-314">In general, if the specified control can be contained in the control and can be moved from the container that it is currently in, this method should succeed.</span></span> <span data-ttu-id="c32c7-315">ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="c32c7-315">However, in some cases, such as for the reference group control instance, controls cannot be moved.</span></span>

## <a name="method-name"></a><span data-ttu-id="c32c7-316">メソッド名</span><span class="sxs-lookup"><span data-stu-id="c32c7-316">Method name</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="c32c7-317">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="c32c7-317">Parameters - name</span></span>

<span data-ttu-id="c32c7-318">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-318">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="c32c7-319">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="c32c7-319">Return Value - name</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="c32c7-320">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="c32c7-320">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="c32c7-321">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="c32c7-321">Parameters - neededPermission</span></span>

<span data-ttu-id="c32c7-322">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-322">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="c32c7-323">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="c32c7-323">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="c32c7-324">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="c32c7-324">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="c32c7-325">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="c32c7-325">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-previewpartref"></a><span data-ttu-id="c32c7-326">メソッド previewPartRef</span><span class="sxs-lookup"><span data-stu-id="c32c7-326">Method previewPartRef</span></span>

```xpp
public str previewPartRef([str value])
```

### <a name="parameters---previewpartref"></a><span data-ttu-id="c32c7-327">パラメーター - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="c32c7-327">Parameters - previewPartRef</span></span>

<span data-ttu-id="c32c7-328">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-328">value</span></span>  

### <a name="return-value---previewpartref"></a><span data-ttu-id="c32c7-329">戻り値 - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="c32c7-329">Return Value - previewPartRef</span></span>

## <a name="method-skip"></a><span data-ttu-id="c32c7-330">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="c32c7-330">Method skip</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="c32c7-331">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="c32c7-331">Parameters - skip</span></span>

<span data-ttu-id="c32c7-332">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-332">value</span></span>  

### <a name="return-value---skip"></a><span data-ttu-id="c32c7-333">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="c32c7-333">Return Value - skip</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="c32c7-334">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="c32c7-334">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="c32c7-335">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="c32c7-335">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="c32c7-336">データ</span><span class="sxs-lookup"><span data-stu-id="c32c7-336">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="c32c7-337">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="c32c7-337">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="c32c7-338">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="c32c7-338">Method userDisable</span></span>

<span data-ttu-id="c32c7-339">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-339">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="c32c7-340">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="c32c7-340">Parameters - userDisable</span></span>

<span data-ttu-id="c32c7-341">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-341">value</span></span>  
<span data-ttu-id="c32c7-342">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c32c7-342">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="c32c7-343">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="c32c7-343">Return Value - userDisable</span></span>

<span data-ttu-id="c32c7-344">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="c32c7-344">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="c32c7-345">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="c32c7-345">Method userHeight</span></span>

<span data-ttu-id="c32c7-346">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-346">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="c32c7-347">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="c32c7-347">Parameters - userHeight</span></span>

<span data-ttu-id="c32c7-348">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-348">value</span></span>  
<span data-ttu-id="c32c7-349">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c32c7-349">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="c32c7-350">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="c32c7-350">Return Value - userHeight</span></span>

<span data-ttu-id="c32c7-351">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="c32c7-351">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="c32c7-352">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="c32c7-352">Method userHide</span></span>

<span data-ttu-id="c32c7-353">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-353">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="c32c7-354">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="c32c7-354">Parameters - userHide</span></span>

<span data-ttu-id="c32c7-355">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-355">value</span></span>  
<span data-ttu-id="c32c7-356">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c32c7-356">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="c32c7-357">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="c32c7-357">Return Value - userHide</span></span>

<span data-ttu-id="c32c7-358">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="c32c7-358">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="c32c7-359">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="c32c7-359">Remarks - userHide</span></span>

<span data-ttu-id="c32c7-360">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-360">The user specifies whether a control is hidden by right-clicking the control when it is viewable or right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="c32c7-361">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="c32c7-361">The right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="c32c7-362">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="c32c7-362">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="c32c7-363">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="c32c7-363">Method userOrgContainer</span></span>

<span data-ttu-id="c32c7-364">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-364">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="c32c7-365">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="c32c7-365">Parameters - userOrgContainer</span></span>

<span data-ttu-id="c32c7-366">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-366">value</span></span>  
<span data-ttu-id="c32c7-367">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c32c7-367">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="c32c7-368">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="c32c7-368">Return Value - userOrgContainer</span></span>

<span data-ttu-id="c32c7-369">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="c32c7-369">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="c32c7-370">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="c32c7-370">Method userOrgSibling</span></span>

<span data-ttu-id="c32c7-371">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-371">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="c32c7-372">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="c32c7-372">Parameters - userOrgSibling</span></span>

<span data-ttu-id="c32c7-373">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-373">value</span></span>  
<span data-ttu-id="c32c7-374">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c32c7-374">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="c32c7-375">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="c32c7-375">Return Value - userOrgSibling</span></span>

<span data-ttu-id="c32c7-376">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="c32c7-376">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="c32c7-377">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="c32c7-377">Method userPromptText</span></span>

<span data-ttu-id="c32c7-378">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-378">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="c32c7-379">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="c32c7-379">Parameters - userPromptText</span></span>

<span data-ttu-id="c32c7-380">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-380">value</span></span>  
<span data-ttu-id="c32c7-381">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c32c7-381">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="c32c7-382">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="c32c7-382">Return Value - userPromptText</span></span>

<span data-ttu-id="c32c7-383">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="c32c7-383">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="c32c7-384">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="c32c7-384">Method userSecurityLevel</span></span>

<span data-ttu-id="c32c7-385">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-385">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="c32c7-386">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="c32c7-386">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="c32c7-387">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-387">value</span></span>  
<span data-ttu-id="c32c7-388">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c32c7-388">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="c32c7-389">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="c32c7-389">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="c32c7-390">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="c32c7-390">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="c32c7-391">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="c32c7-391">Method userSkip</span></span>

<span data-ttu-id="c32c7-392">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-392">Sets or returns the value that indicates whether the form control is skipped when the user press the TAB key to navigate the controls on the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="c32c7-393">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="c32c7-393">Parameters - userSkip</span></span>

<span data-ttu-id="c32c7-394">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-394">value</span></span>  
<span data-ttu-id="c32c7-395">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c32c7-395">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="c32c7-396">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="c32c7-396">The value is 1 if the user setting to skip the control is in effect; otherwise, it is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="c32c7-397">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="c32c7-397">Return Value - userSkip</span></span>

<span data-ttu-id="c32c7-398">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="c32c7-398">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="c32c7-399">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="c32c7-399">Method userWidth</span></span>

<span data-ttu-id="c32c7-400">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-400">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="c32c7-401">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="c32c7-401">Parameters - userWidth</span></span>

<span data-ttu-id="c32c7-402">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-402">value</span></span>  
<span data-ttu-id="c32c7-403">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c32c7-403">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="c32c7-404">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="c32c7-404">Return Value - userWidth</span></span>

<span data-ttu-id="c32c7-405">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="c32c7-405">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="c32c7-406">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="c32c7-406">Remarks - userWidth</span></span>

<span data-ttu-id="c32c7-407">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="c32c7-407">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="c32c7-408">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="c32c7-408">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="c32c7-409">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="c32c7-409">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-visible"></a><span data-ttu-id="c32c7-410">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="c32c7-410">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="c32c7-411">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="c32c7-411">Parameters - visible</span></span>

<span data-ttu-id="c32c7-412">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-412">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="c32c7-413">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="c32c7-413">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="c32c7-414">メソッド width</span><span class="sxs-lookup"><span data-stu-id="c32c7-414">Method width</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="c32c7-415">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="c32c7-415">Parameters - width</span></span>

<span data-ttu-id="c32c7-416">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-416">value</span></span>  

<!-- -->

<span data-ttu-id="c32c7-417">モード</span><span class="sxs-lookup"><span data-stu-id="c32c7-417">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="c32c7-418">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="c32c7-418">Return Value - width</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="c32c7-419">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="c32c7-419">Method widthMode</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="c32c7-420">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="c32c7-420">Parameters - widthMode</span></span>

<span data-ttu-id="c32c7-421">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-421">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="c32c7-422">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="c32c7-422">Return Value - widthMode</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="c32c7-423">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="c32c7-423">Method widthValue</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="c32c7-424">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="c32c7-424">Parameters - widthValue</span></span>

<span data-ttu-id="c32c7-425">値</span><span class="sxs-lookup"><span data-stu-id="c32c7-425">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="c32c7-426">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="c32c7-426">Return Value - widthValue</span></span>

## <a name="method-registerxppilimplementation"></a><span data-ttu-id="c32c7-427">メソッド RegisterXppILImplementation</span><span class="sxs-lookup"><span data-stu-id="c32c7-427">Method RegisterXppILImplementation</span></span>

```xpp
public void RegisterXppILImplementation(str className)
```

### <a name="parameters---registerxppilimplementation"></a><span data-ttu-id="c32c7-428">パラメーター - RegisterXppILImplementation</span><span class="sxs-lookup"><span data-stu-id="c32c7-428">Parameters - RegisterXppILImplementation</span></span>

<span data-ttu-id="c32c7-429">className</span><span class="sxs-lookup"><span data-stu-id="c32c7-429">className</span></span>  

## <a name="method-new"></a><span data-ttu-id="c32c7-430">メソッド new</span><span class="sxs-lookup"><span data-stu-id="c32c7-430">Method new</span></span>

```xpp
public void new(FormContainer container)
```

### <a name="parameters---new"></a><span data-ttu-id="c32c7-431">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="c32c7-431">Parameters - new</span></span>

<span data-ttu-id="c32c7-432">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c32c7-432">container</span></span>  

## <a name="method-resetusersetting"></a><span data-ttu-id="c32c7-433">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="c32c7-433">Method resetUserSetting</span></span>

<span data-ttu-id="c32c7-434">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="c32c7-434">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

