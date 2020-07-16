---
title: FormGroupControl クラス
description: このトピックでは、FormGroupControl クラスについて説明します。
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
ms.openlocfilehash: df8a5376ecadfa5b98f51bee3506e175e2727d26
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502942"
---
# <a name="class-formgroupcontrol"></a><span data-ttu-id="6ee3b-103">クラス FormGroupControl</span><span class="sxs-lookup"><span data-stu-id="6ee3b-103">Class FormGroupControl</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class FormGroupControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="6ee3b-104">備考</span><span class="sxs-lookup"><span data-stu-id="6ee3b-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="6ee3b-105">例</span><span class="sxs-lookup"><span data-stu-id="6ee3b-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="6ee3b-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="6ee3b-106">Methods</span></span>

| <span data-ttu-id="6ee3b-107">方法</span><span class="sxs-lookup"><span data-stu-id="6ee3b-107">Method</span></span>                                                                                                              | <span data-ttu-id="6ee3b-108">説明</span><span class="sxs-lookup"><span data-stu-id="6ee3b-108">Description</span></span>                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee3b-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span></span>            | <span data-ttu-id="6ee3b-110">フォーム グループ コントロールにフォームのコントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-110">Adds a form control to a form group control.</span></span>                                                                                                                                                        |
| <span data-ttu-id="6ee3b-111">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-111">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span></span>                     |                                                                                                                                                                                                     |
| <span data-ttu-id="6ee3b-112">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-112">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span></span> | <span data-ttu-id="6ee3b-113">テーブル フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-113">Adds a table field.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="6ee3b-114">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-114">public boolean alignChild(\[boolean value\])</span></span>                                                                        | <span data-ttu-id="6ee3b-115">フォーム グループ コントロールが、フォーム内の他のコントロールと同じ方法で一致しているかどうかを示すブール値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-115">Sets or returns a Boolean value that indicates whether a form group control is aligned in the same manner as other controls in a form.</span></span>                                                              |
| <span data-ttu-id="6ee3b-116">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-116">public boolean alignChildren(\[boolean value\])</span></span>                                                                     | <span data-ttu-id="6ee3b-117">子コントロールが一致しているかどうかを示すブール値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-117">Sets or returns a Boolean value that indicates whether the child controls are aligned.</span></span>                                                                                                              |
| <span data-ttu-id="6ee3b-118">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-118">public boolean alignControl(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="6ee3b-119">コントロールが他のコントロールと揃っているかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-119">Determines whether the control is aligned with other controls.</span></span>                                                                                                                                      |
| <span data-ttu-id="6ee3b-120">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-120">public boolean allowEdit(\[boolean value\])</span></span>                                                                         | <span data-ttu-id="6ee3b-121">ユーザーがコントロールの内容を修正できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-121">Determines whether the user can modify the contents of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="6ee3b-122">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-122">public boolean allowSysSetup()</span></span>                                                                                      | <span data-ttu-id="6ee3b-123">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-123">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                                                 |
| <span data-ttu-id="6ee3b-124">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-124">public int allowUserSetup(\[int value\])</span></span>                                                                            | <span data-ttu-id="6ee3b-125">フォーム グループ コントロールに実行できる変更のレベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-125">Sets or gets the level of modification that can be performed for a form group control.</span></span>                                                                                                              |
| <span data-ttu-id="6ee3b-126">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-126">public int arrangeGuide(\[int value\])</span></span>                                                                              |                                                                                                                                                                                                     |
| <span data-ttu-id="6ee3b-127">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-127">public int arrangeMethod(\[int value\])</span></span>                                                                             | <span data-ttu-id="6ee3b-128">フォーム グループ コントロールのコントロールを配置する方法を示す整数値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-128">Sets or returns an integer value that indicates how controls in a form group control are arranged.</span></span>                                                                                                  |
| <span data-ttu-id="6ee3b-129">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-129">public int arrangeWhen(\[int value\])</span></span>                                                                               | <span data-ttu-id="6ee3b-130">コントロールが配置されるタイミングを指定する整数値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-130">Sets or returns an integer value that specifies when the controls are arranged.</span></span>                                                                                                                     |
| <span data-ttu-id="6ee3b-131">public boolean autoDataGroup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-131">public boolean autoDataGroup(\[boolean value\])</span></span>                                                                     | <span data-ttu-id="6ee3b-132">フォーム グループ コントロールに、コントロールに対して指定されているデータ グループ内のフィールドのみ含めることができるかどうかを指定するブール値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-132">Sets or returns a Boolean value that specifies whether a form group control can contain only the fields in the data group that are specified for the control.</span></span>                                       |
| <span data-ttu-id="6ee3b-133">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-133">public boolean autoDeclaration(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="6ee3b-134">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-134">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                                                  |
| <span data-ttu-id="6ee3b-135">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-135">public int backgroundColor(\[int value\])</span></span>                                                                           | <span data-ttu-id="6ee3b-136">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-136">Gets or sets the background color of the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="6ee3b-137">public Image backgroundImage(\[Image image\], \[int drawMode\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-137">public Image backgroundImage(\[Image image\], \[int drawMode\])</span></span>                                                     | <span data-ttu-id="6ee3b-138">フォーム グループ コントロールの背景イメージを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-138">Specifies the background image for a form group control.</span></span>                                                                                                                                            |
| <span data-ttu-id="6ee3b-139">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-139">public int backStyle(\[int value\])</span></span>                                                                                 | <span data-ttu-id="6ee3b-140">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-140">Determines whether the control background can be transparent.</span></span>                                                                                                                                       |
| <span data-ttu-id="6ee3b-141">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="6ee3b-141">public int beginDrag(int x, int y)</span></span>                                                                                  | <span data-ttu-id="6ee3b-142">ユーザーがフォーム グループ コントロールの移動を始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-142">Is called when the user starts to move a form group control.</span></span>                                                                                                                                        |
| <span data-ttu-id="6ee3b-143">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-143">public int bold(\[int value\])</span></span>                                                                                      | <span data-ttu-id="6ee3b-144">コントロール内のテキストを表示するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-144">Gets or sets the weight of font that is used to display text in the control.</span></span>                                                                                                                        |
| <span data-ttu-id="6ee3b-145">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-145">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                           | <span data-ttu-id="6ee3b-146">フォーム グループ コントロールの下余白をピクセル単位で設定するか返し、余白が自動的に調整されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-146">Sets or returns the bottom margin of a form group control in pixels and specifies whether the margin is automatically adjusted.</span></span>                                                                     |
| <span data-ttu-id="6ee3b-147">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-147">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                                 | <span data-ttu-id="6ee3b-148">下余白が自動的に調整されるかどうかを示す AutoMode 列挙値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-148">Sets or returns an AutoMode enumeration value that indicates whether the bottom margin is automatically adjusted.</span></span>                                                                                   |
| <span data-ttu-id="6ee3b-149">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-149">public int bottomMarginValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="6ee3b-150">フォーム グループ コントロールの下余白をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-150">Sets or returns the bottom margin of a form group control in pixels.</span></span>                                                                                                                                |
| <span data-ttu-id="6ee3b-151">public boolean breakable(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-151">public boolean breakable(\[boolean value\])</span></span>                                                                         |                                                                                                                                                                                                     |
| <span data-ttu-id="6ee3b-152">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="6ee3b-152">public container calcControlSize(int chars, int lines)</span></span>                                                              | <span data-ttu-id="6ee3b-153">文字数と明細行数に基づいて、フォーム グループ コントロールのフォント サイズを計算します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-153">Calculates the size of a form group control, based on the number of characters and the number of lines.</span></span>                                                                                             |
| <span data-ttu-id="6ee3b-154">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-154">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span></span>                               | <span data-ttu-id="6ee3b-155">テーブル フィールドを追加できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-155">Indicates whether a table field can be added.</span></span>                                                                                                                                                       |
| <span data-ttu-id="6ee3b-156">public boolean canContain(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="6ee3b-156">public boolean canContain(FormControl control)</span></span>                                                                      | <span data-ttu-id="6ee3b-157">フォーム グループ コントロールに指定されたフォーム コントロールを含めることができるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-157">Specifies whether a form group control can contain the specified form control.</span></span>                                                                                                                      |
| <span data-ttu-id="6ee3b-158">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-158">public str caption(\[str value\])</span></span>                                                                                   | <span data-ttu-id="6ee3b-159">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-159">Gets or set the caption of the control.</span></span>                                                                                                                                                             |
| <span data-ttu-id="6ee3b-160">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-160">public int characterSet(\[int value\])</span></span>                                                                              | <span data-ttu-id="6ee3b-161">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-161">Gets or sets the character set of the font.</span></span>                                                                                                                                                         |
| <span data-ttu-id="6ee3b-162">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-162">public int colorScheme(\[int value\])</span></span>                                                                               | <span data-ttu-id="6ee3b-163">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-163">Gets or sets the color scheme of the control.</span></span>                                                                                                                                                       |
| <span data-ttu-id="6ee3b-164">public int columns(\[int value\], \[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-164">public int columns(\[int value\], \[ColumnsMode mode\])</span></span>                                                             | <span data-ttu-id="6ee3b-165">フォーム グループ コントロールの列の数をピクセル単位で設定するか返し、数が自動的に調整されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-165">Sets or returns the number of columns in a form group control in pixels, and specifies whether the number is automatically adjusted.</span></span>                                                                |
| <span data-ttu-id="6ee3b-166">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-166">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span></span>                                                                | <span data-ttu-id="6ee3b-167">フォーム グループ コントロール内の列数が固定されているかどうか、またはフォーム サイズなどのオプション、他のフォーム設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-167">Sets or returns a value that indicates whether the number of columns in a form group control is fixed, or whether it is automatically adjusted based on other form settings, such as the form size.</span></span> |
| <span data-ttu-id="6ee3b-168">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-168">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                            | <span data-ttu-id="6ee3b-169">フォーム グループ コントロール内の列間のスペースの量をピクセル単位で設定するか返し、フォント サイズなどの他のフォーム設定に基づいてスペースが自動的に調整されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-169">Sets or returns the amount of space between columns in a form group control in pixels and indicates whether the space is automatically adjusted based on other form settings, such the font size.</span></span>   |
| <span data-ttu-id="6ee3b-170">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-170">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                                  | <span data-ttu-id="6ee3b-171">フォーム グループ コントロール内の列間のスペースの量が自動的に調整されるかどうかを示す AutoMode 列挙値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-171">Sets or returns an AutoMode enumeration value that indicates whether the amount of space between columns in a form group control is automatically adjusted.</span></span>                                         |
| <span data-ttu-id="6ee3b-172">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-172">public int columnspaceValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="6ee3b-173">ピクセルでフォーム グループ コントロール内の列間のスペースの量を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-173">Sets or returns the amount of space between columns in a form group control in pixels.</span></span>                                                                                                              |
| <span data-ttu-id="6ee3b-174">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-174">public int columnsValue(\[int value\])</span></span>                                                                              | <span data-ttu-id="6ee3b-175">フォーム グループ コントロール内のコントロールの数を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-175">Sets or returns the number of columns in a form group control.</span></span>                                                                                                                                      |
| <span data-ttu-id="6ee3b-176">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-176">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                            | <span data-ttu-id="6ee3b-177">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-177">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="6ee3b-178">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-178">public List configurationKeyEx()</span></span>                                                                                    | <span data-ttu-id="6ee3b-179">フォーム グループ コントロールのために有効化されたコンフィギュレーション キーの ID を含むリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-179">Retrieves a list that contains the IDs of configuration keys that are activated for a form group control.</span></span>                                                                                           |
| <span data-ttu-id="6ee3b-180">public boolean contains(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="6ee3b-180">public boolean contains(FormControl control)</span></span>                                                                        | <span data-ttu-id="6ee3b-181">フォーム グループ コントロールに指定されたフォーム コントロールが含まれるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-181">Specifies whether a form group control contains a specified form control.</span></span>                                                                                                                           |
| <span data-ttu-id="6ee3b-182">public int controlCount()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-182">public int controlCount()</span></span>                                                                                           | <span data-ttu-id="6ee3b-183">フォーム グループ コントロール内のコントロールの数を返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-183">Returns the number of controls in a form group control.</span></span>                                                                                                                                             |
| <span data-ttu-id="6ee3b-184">public FormControl controlNum(int controlNo)</span><span class="sxs-lookup"><span data-stu-id="6ee3b-184">public FormControl controlNum(int controlNo)</span></span>                                                                        | <span data-ttu-id="6ee3b-185">フォーム グループ コントロールで指定したコントロールの FormControl オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-185">Returns a FormControl object for a specified control in a form group control.</span></span>                                                                                                                       |
| <span data-ttu-id="6ee3b-186">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-186">public str countryRegionCodes(\[str value\])</span></span>                                                                        | <span data-ttu-id="6ee3b-187">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-187">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                                                      |
| <span data-ttu-id="6ee3b-188">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-188">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                         |                                                                                                                                                                                                     |
| <span data-ttu-id="6ee3b-189">public str dataGroup(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-189">public str dataGroup(\[str value\])</span></span>                                                                                 | <span data-ttu-id="6ee3b-190">フォーム グループ コントロールのデータのグループを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-190">Sets or returns a data group for a form group control.</span></span>                                                                                                                                              |
| <span data-ttu-id="6ee3b-191">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-191">public str dataRelationPath(\[str value\])</span></span>                                                                          | <span data-ttu-id="6ee3b-192">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-192">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                                                       |
| <span data-ttu-id="6ee3b-193">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-193">public int dataSource(\[AnyType value\])</span></span>                                                                            | <span data-ttu-id="6ee3b-194">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-194">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                                                                            |
| <span data-ttu-id="6ee3b-195">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-195">public int displayTarget(\[int value\])</span></span>                                                                             | <span data-ttu-id="6ee3b-196">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-196">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>                             |
| <span data-ttu-id="6ee3b-197">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-197">public int dragDrop(\[int value\])</span></span>                                                                                  | <span data-ttu-id="6ee3b-198">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-198">Determines whether drag-and-drop operations are enabled or disabled for the control.</span></span>                                                                                                                |
| <span data-ttu-id="6ee3b-199">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="6ee3b-199">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="6ee3b-200">オブジェクトがフォーム グループ コントロールの境界上にドラッグされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-200">Is called when an object is dragged over the bounds of a form group control.</span></span>                                                                                                                        |
| <span data-ttu-id="6ee3b-201">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="6ee3b-201">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="6ee3b-202">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-202">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                                                    |
| <span data-ttu-id="6ee3b-203">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-203">public str dragText()</span></span>                                                                                               | <span data-ttu-id="6ee3b-204">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-204">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                                              |
| <span data-ttu-id="6ee3b-205">public boolean enableChilds(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-205">public boolean enableChilds(\[boolean enable\])</span></span>                                                                     | <span data-ttu-id="6ee3b-206">フォーム グループ コントロールの子コントロールが有効かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-206">Specifies whether the child controls are enabled for a form group control.</span></span>                                                                                                                          |
| <span data-ttu-id="6ee3b-207">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-207">public boolean enabled(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="6ee3b-208">オブジェクトが有効か無効かを決定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-208">Determines whether the object is enabled or disabled.</span></span>                                                                                                                                               |
| <span data-ttu-id="6ee3b-209">public boolean expand(\[boolean expand\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-209">public boolean expand(\[boolean expand\])</span></span>                                                                           | <span data-ttu-id="6ee3b-210">フォーム グループ コントロールが展開されているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-210">Specifies whether a form group control is expanded.</span></span>                                                                                                                                                 |
| <span data-ttu-id="6ee3b-211">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-211">public str font(\[str value\])</span></span>                                                                                      | <span data-ttu-id="6ee3b-212">コントロール内のテキストに使用されるフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-212">Gets or sets the name of the font that is used for text in a control.</span></span>                                                                                                                               |
| <span data-ttu-id="6ee3b-213">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-213">public int fontSize(\[int value\])</span></span>                                                                                  | <span data-ttu-id="6ee3b-214">コントロール内のテキストに使用するフォント サイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-214">Gets or sets the font size to use for text in a control.</span></span>                                                                                                                                            |
| <span data-ttu-id="6ee3b-215">public int frameOptionButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-215">public int frameOptionButton(\[int value\])</span></span>                                                                         | <span data-ttu-id="6ee3b-216">フォーム グループ コントロールのオプション ボタンを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-216">Sets or returns the option button for a form group control.</span></span>                                                                                                                                         |
| <span data-ttu-id="6ee3b-217">public int framePosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-217">public int framePosition(\[int value\])</span></span>                                                                             | <span data-ttu-id="6ee3b-218">フォーム グループ コントロールのフレームの位置を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-218">Sets or returns the location of the frame for a form group control.</span></span>                                                                                                                                 |
| <span data-ttu-id="6ee3b-219">public int frameType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-219">public int frameType(\[int value\])</span></span>                                                                                 | <span data-ttu-id="6ee3b-220">フォーム グループ コントロールのフレーム スタイルを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-220">Sets or returns the frame style for a form group control.</span></span>                                                                                                                                           |
| <span data-ttu-id="6ee3b-221">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-221">public boolean hasChanged(\[boolean val\])</span></span>                                                                          | <span data-ttu-id="6ee3b-222">フォーム グループ コントロールの内容が変更されたかどうかを示すブール値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-222">Sets or returns a Boolean value that indicates whether the contents of a form group control have changed.</span></span>                                                                                           |
| <span data-ttu-id="6ee3b-223">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-223">public boolean hasUserSetting()</span></span>                                                                                     | <span data-ttu-id="6ee3b-224">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-224">Indicates whether the control has custom user settings.</span></span>                                                                                                                                             |
| <span data-ttu-id="6ee3b-225">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-225">public int height(int value, \[int mode\])</span></span>                                                                          | <span data-ttu-id="6ee3b-226">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-226">Gets or sets the height of the control.</span></span>                                                                                                                                                             |
| <span data-ttu-id="6ee3b-227">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-227">public int heightMode(\[int value\])</span></span>                                                                                | <span data-ttu-id="6ee3b-228">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-228">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="6ee3b-229">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-229">public int heightValue(\[int value\])</span></span>                                                                               | <span data-ttu-id="6ee3b-230">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-230">Gets or sets the height of the control.</span></span>                                                                                                                                                             |
| <span data-ttu-id="6ee3b-231">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-231">public str helpField()</span></span>                                                                                              | <span data-ttu-id="6ee3b-232">フォーム グループ コントロールが選択されている場合にステータス バーに表示されるヘルプ テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-232">Returns the Help text that is displayed in the status bar when a form group control is selected.</span></span>                                                                                                    |
| <span data-ttu-id="6ee3b-233">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-233">public str helpText(\[str value\])</span></span>                                                                                  | <span data-ttu-id="6ee3b-234">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-234">Gets or sets the Help text that is displayed at the bottom of the screen when a field or control is pointed to.</span></span>                                                                                     |
| <span data-ttu-id="6ee3b-235">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-235">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                                       | <span data-ttu-id="6ee3b-236">グループ内のコントロールが表示されないときフォーム グループ コントロールを表示するかどうかを示すブール値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-236">Sets or gets a Boolean value that indicates whether a form group control is visible when the controls in the group are not visible.</span></span>                                                                 |
| <span data-ttu-id="6ee3b-237">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-237">public str hierarchyParent(\[str value\])</span></span>                                                                           | <span data-ttu-id="6ee3b-238">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-238">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                                                     |
| <span data-ttu-id="6ee3b-239">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-239">public int hWnd()</span></span>                                                                                                   | <span data-ttu-id="6ee3b-240">フォーム グループ コントロールのハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-240">Returns a handle for a form group control.</span></span>                                                                                                                                                          |
| <span data-ttu-id="6ee3b-241">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-241">public boolean isContainer()</span></span>                                                                                        | <span data-ttu-id="6ee3b-242">フォーム グループ コントロールがコンテナーであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-242">Indicates whether a form group control is a container.</span></span>                                                                                                                                              |
| <span data-ttu-id="6ee3b-243">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-243">public boolean isDisplayed()</span></span>                                                                                        | <span data-ttu-id="6ee3b-244">フォーム グループ コントロールが表示されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-244">Indicates whether a form group control is displayed.</span></span>                                                                                                                                                |
| <span data-ttu-id="6ee3b-245">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-245">public boolean isRestricted()</span></span>                                                                                       | <span data-ttu-id="6ee3b-246">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-246">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                                                 |
| <span data-ttu-id="6ee3b-247">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="6ee3b-247">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                            | <span data-ttu-id="6ee3b-248">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-248">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                                                 |
| <span data-ttu-id="6ee3b-249">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-249">public boolean italic(\[boolean value\])</span></span>                                                                            | <span data-ttu-id="6ee3b-250">フォーム グループ コントロールのテキストが斜体であるかどうかを示すブール値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-250">Sets or returns a Boolean value that indicates whether the text for a form group control is italic.</span></span>                                                                                                 |
| <span data-ttu-id="6ee3b-251">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-251">public int labelBold(\[int value\])</span></span>                                                                                 | <span data-ttu-id="6ee3b-252">フォーム グループ コントロールのラベル テキストのフォントの太さを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-252">Sets or returns the font weight of the label text for a form group control.</span></span>                                                                                                                         |
| <span data-ttu-id="6ee3b-253">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-253">public int labelCharacterSet(\[int value\])</span></span>                                                                         | <span data-ttu-id="6ee3b-254">フォーム グループ コントロールのラベル テキストのフォントの文字セットを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-254">Sets or returns the character set of the font for the label text for a form group control.</span></span>                                                                                                          |
| <span data-ttu-id="6ee3b-255">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-255">public str labelFont(\[str value\])</span></span>                                                                                 | <span data-ttu-id="6ee3b-256">フォーム グループ コントロールのラベル テキストのフォントを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-256">Sets or returns the font for the label text for a form group control.</span></span>                                                                                                                               |
| <span data-ttu-id="6ee3b-257">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-257">public int labelFontSize(\[int value\])</span></span>                                                                             | <span data-ttu-id="6ee3b-258">フォーム グループ コントロールのラベル テキストのフォント サイズを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-258">Sets or returns the font size of the label text for a form group control.</span></span>                                                                                                                           |
| <span data-ttu-id="6ee3b-259">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-259">public boolean labelItalic(\[boolean value\])</span></span>                                                                       | <span data-ttu-id="6ee3b-260">フォーム グループ コントロールのラベル テキストが斜体であるかどうかを示すブール値データ型を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-260">Sets or returns a Boolean data type that indicates whether the label text for a form group control is italic.</span></span>                                                                                       |
| <span data-ttu-id="6ee3b-261">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-261">public boolean labelUnderline(\[boolean value\])</span></span>                                                                    | <span data-ttu-id="6ee3b-262">フォーム グループ コントロールのラベル テキストが下線付きであるかどうかを示すブール値データ型を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-262">Sets or returns a Boolean data type that indicates whether the label text for a form group control is underlined.</span></span>                                                                                   |
| <span data-ttu-id="6ee3b-263">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-263">public boolean leave()</span></span>                                                                                              | <span data-ttu-id="6ee3b-264">ユーザーがマウス ポインターをフォーム グループ コントロールから離すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-264">Is called when the user moves the mouse pointer out of a form group control.</span></span>                                                                                                                        |
| <span data-ttu-id="6ee3b-265">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-265">public int left(int value, \[int mode\])</span></span>                                                                            | <span data-ttu-id="6ee3b-266">フォーム グループ コントロールの水平位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-266">Sets or returns the horizontal position of a form group control in pixels and specifies how the position is calculated.</span></span>                                                                             |
| <span data-ttu-id="6ee3b-267">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-267">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                             | <span data-ttu-id="6ee3b-268">フォーム グループ コントロールの左余白のサイズをピクセル単位で設定するか返し、サイズが自動的に調整されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-268">Sets or returns the size of the left margin for a form group control in pixels and specifies whether the size is automatically adjusted.</span></span>                                                            |
| <span data-ttu-id="6ee3b-269">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-269">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                                   | <span data-ttu-id="6ee3b-270">フォーム グループ コントロールの左余白のサイズが固定されているかどうか、またはフォーム プロパティ設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-270">Sets or returns a value that indicates whether the size of the left margin for a form group control is fixed, or whether it is automatically adjusted based on other form property settings.</span></span>        |
| <span data-ttu-id="6ee3b-271">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-271">public int leftMarginValue(\[int value\])</span></span>                                                                           | <span data-ttu-id="6ee3b-272">フォーム グループ コントロールの左余白のサイズをピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-272">Sets or returns the size of the left margin for a form group control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="6ee3b-273">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-273">public int leftMode(\[int value\])</span></span>                                                                                  | <span data-ttu-id="6ee3b-274">フォーム グループ コントロールの水平位置を計算する方法を示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-274">Sets or returns a value that indicates how the horizontal position of a form group control is calculated.</span></span>                                                                                           |
| <span data-ttu-id="6ee3b-275">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-275">public int leftValue(\[int value\])</span></span>                                                                                 | <span data-ttu-id="6ee3b-276">フォーム グループ コントロールの水平位置をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-276">Sets or returns the horizontal position of a form group control in pixels.</span></span>                                                                                                                          |
| <span data-ttu-id="6ee3b-277">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-277">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                                     | <span data-ttu-id="6ee3b-278">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-278">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                                               |
| <span data-ttu-id="6ee3b-279">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="6ee3b-279">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                     | <span data-ttu-id="6ee3b-280">ユーザーがフォーム グループ コントロールをダブルクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-280">Is called when the user double-clicks a form group control.</span></span>                                                                                                                                         |
| <span data-ttu-id="6ee3b-281">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="6ee3b-281">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="6ee3b-282">ユーザーがフォーム グループ コントロールでマウス ボタンを押すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-282">Is called when the user presses the mouse button in a form group control.</span></span>                                                                                                                           |
| <span data-ttu-id="6ee3b-283">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="6ee3b-283">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="6ee3b-284">ユーザーがマウス ポインターをフォーム グループ コントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-284">Is called when the user moves the mouse pointer over a form group control.</span></span>                                                                                                                          |
| <span data-ttu-id="6ee3b-285">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="6ee3b-285">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                           | <span data-ttu-id="6ee3b-286">ユーザーがマウス ボタンをフォーム グループ コントロール上で放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-286">Is called when the user releases the mouse button over a form group control.</span></span>                                                                                                                        |
| <span data-ttu-id="6ee3b-287">public int moveControl(int controlId, \[int insertAfterId\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-287">public int moveControl(int controlId, \[int insertAfterId\])</span></span>                                                        | <span data-ttu-id="6ee3b-288">指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-288">Moves a specified control.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="6ee3b-289">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-289">public str name(\[str value\])</span></span>                                                                                      | <span data-ttu-id="6ee3b-290">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-290">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                                             |
| <span data-ttu-id="6ee3b-291">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-291">public int neededPermission(\[int value\])</span></span>                                                                          |                                                                                                                                                                                                     |
| <span data-ttu-id="6ee3b-292">public int optionValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-292">public int optionValue(\[int value\])</span></span>                                                                               | <span data-ttu-id="6ee3b-293">フォーム グループ コントロールに関連付けられているオプション ボタンの値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-293">Sets or returns the value for the option button that is associated with a form group control.</span></span>                                                                                                       |
| <span data-ttu-id="6ee3b-294">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-294">public container SysObsoleteAttribute()</span></span>                                                                             |                                                                                                                                                                                                     |
| <span data-ttu-id="6ee3b-295">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-295">public FormControl parentControl()</span></span>                                                                                  | <span data-ttu-id="6ee3b-296">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-296">Retrieves the parent control for the control.</span></span>                                                                                                                                                       |
| <span data-ttu-id="6ee3b-297">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-297">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                            | <span data-ttu-id="6ee3b-298">フォーム グループ コントロールの右余白のサイズをピクセル単位で設定するか返し、サイズが自動的に調整されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-298">Sets or returns the size of the right margin for a form group control in pixels and specifies whether the size is automatically adjusted.</span></span>                                                           |
| <span data-ttu-id="6ee3b-299">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-299">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                                  | <span data-ttu-id="6ee3b-300">フォーム グループ コントロールの右余白のサイズが固定されているかどうか、またはフォーム プロパティ設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-300">Sets or returns a value that indicates whether the size of the right margin for a form group control is fixed, or whether it is automatically adjusted based on other form property settings.</span></span>       |
| <span data-ttu-id="6ee3b-301">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-301">public int rightMarginValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="6ee3b-302">フォーム グループ コントロールの右余白のサイズをピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-302">Sets or returns the size of the right margin for a form group control in pixels.</span></span>                                                                                                                    |
| <span data-ttu-id="6ee3b-303">public boolean saveFilter(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-303">public boolean saveFilter(\[boolean value\])</span></span>                                                                        |                                                                                                                                                                                                     |
| <span data-ttu-id="6ee3b-304">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-304">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                           | <span data-ttu-id="6ee3b-305">フォーム グループ コントロールのセキュリティ キー ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-305">Sets or returns the security key ID for a form group control.</span></span>                                                                                                                                       |
| <span data-ttu-id="6ee3b-306">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="6ee3b-306">public int showContextMenu(int menuHandle)</span></span>                                                                          | <span data-ttu-id="6ee3b-307">フォーム グループ コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-307">Shows a shortcut menu for a form group control.</span></span>                                                                                                                                                     |
| <span data-ttu-id="6ee3b-308">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-308">public boolean skip(\[boolean value\])</span></span>                                                                              | <span data-ttu-id="6ee3b-309">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示すブール値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-309">Sets or returns a Boolean value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                                             |
| <span data-ttu-id="6ee3b-310">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-310">public int sort(\[SortOrder sortDirection\])</span></span>                                                                        | <span data-ttu-id="6ee3b-311">フォーム グループ コントロールに格納されているコントロールを並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-311">Sorts the controls that are contained in a form group control.</span></span>                                                                                                                                      |
| <span data-ttu-id="6ee3b-312">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-312">public int style(\[int value\])</span></span>                                                                                     |                                                                                                                                                                                                     |
| <span data-ttu-id="6ee3b-313">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-313">public str toolTip()</span></span>                                                                                                | <span data-ttu-id="6ee3b-314">フォーム グループ コントロールのツールヒントのテキスト文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-314">Returns the text string for the tooltip for a form group control.</span></span>                                                                                                                                   |
| <span data-ttu-id="6ee3b-315">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-315">public int top(int value, \[int mode\])</span></span>                                                                             | <span data-ttu-id="6ee3b-316">フォーム グループ コントロールの垂直位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-316">Sets or returns the vertical position of a form group control in pixels and specifies how the position is calculated.</span></span>                                                                               |
| <span data-ttu-id="6ee3b-317">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-317">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                              | <span data-ttu-id="6ee3b-318">フォーム グループ コントロールの上余白をピクセル単位で設定するか返し、サイズが自動的に調整されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-318">Sets or returns the top margin for a form group control in pixels and specifies whether the size is automatically adjusted.</span></span>                                                                         |
| <span data-ttu-id="6ee3b-319">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-319">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                                    | <span data-ttu-id="6ee3b-320">フォーム グループ コントロールの上余白のサイズが固定されているかどうか、またはフォーム プロパティ設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-320">Sets or returns a value that indicates whether the size of the top margin for a form group control is fixed, or whether it is automatically adjusted based on other form property settings.</span></span>         |
| <span data-ttu-id="6ee3b-321">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-321">public int topMarginValue(\[int value\])</span></span>                                                                            |                                                                                                                                                                                                     |
| <span data-ttu-id="6ee3b-322">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-322">public int topMode(\[int value\])</span></span>                                                                                   | <span data-ttu-id="6ee3b-323">フォーム グループ コントロールの垂直位置を計算する方法を示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-323">Sets or returns a value that indicates how the vertical position of a form group control is calculated.</span></span>                                                                                             |
| <span data-ttu-id="6ee3b-324">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-324">public int topValue(\[int value\])</span></span>                                                                                  | <span data-ttu-id="6ee3b-325">フォーム グループ コントロールの垂直位置をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-325">Sets or returns the vertical position of a form group control in pixels.</span></span>                                                                                                                            |
| <span data-ttu-id="6ee3b-326">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-326">public int type(\[int value\])</span></span>                                                                                      |                                                                                                                                                                                                     |
| <span data-ttu-id="6ee3b-327">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-327">public boolean underline(\[boolean value\])</span></span>                                                                         | <span data-ttu-id="6ee3b-328">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-328">Sets or returns the underline property for the text in the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="6ee3b-329">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="6ee3b-329">public boolean SysObsoleteAttribute(container data)</span></span>                                                                 |                                                                                                                                                                                                     |
| <span data-ttu-id="6ee3b-330">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-330">public int userData(\[int value\])</span></span>                                                                                  | <span data-ttu-id="6ee3b-331">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-331">Gets or sets the user data for the control.</span></span>                                                                                                                                                         |
| <span data-ttu-id="6ee3b-332">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-332">public int userDataItem(\[int value\])</span></span>                                                                              | <span data-ttu-id="6ee3b-333">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-333">Gets or sets the user data item for the control.</span></span>                                                                                                                                                    |
| <span data-ttu-id="6ee3b-334">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-334">public int userDataItems(\[int value\])</span></span>                                                                             | <span data-ttu-id="6ee3b-335">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-335">Gets or sets the number of user data items for the control.</span></span>                                                                                                                                         |
| <span data-ttu-id="6ee3b-336">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-336">public int userDisable(\[int value\])</span></span>                                                                               | <span data-ttu-id="6ee3b-337">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-337">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                                                 |
| <span data-ttu-id="6ee3b-338">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-338">public int userHeight(\[int value\])</span></span>                                                                                | <span data-ttu-id="6ee3b-339">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-339">Gets or sets the custom user height for the control.</span></span>                                                                                                                                                |
| <span data-ttu-id="6ee3b-340">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-340">public int userHide(\[int value\])</span></span>                                                                                  | <span data-ttu-id="6ee3b-341">コントロールがユーザーから非表示になっているかどうかを示す整数データ型を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-341">Sets or returns an integer data type that indicates whether a control is hidden from the user.</span></span>                                                                                                      |
| <span data-ttu-id="6ee3b-342">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-342">public int userOrgContainer(\[int value\])</span></span>                                                                          | <span data-ttu-id="6ee3b-343">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-343">Gets or sets the organization container for the control.</span></span>                                                                                                                                            |
| <span data-ttu-id="6ee3b-344">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-344">public int userOrgSibling(\[int value\])</span></span>                                                                            | <span data-ttu-id="6ee3b-345">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-345">Gets or sets the organization sibling for the control.</span></span>                                                                                                                                              |
| <span data-ttu-id="6ee3b-346">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-346">public str userPromptText(\[str value\])</span></span>                                                                            | <span data-ttu-id="6ee3b-347">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-347">Gets or sets the user label text for the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="6ee3b-348">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-348">public int userSecurityLevel(\[int value\])</span></span>                                                                         | <span data-ttu-id="6ee3b-349">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-349">Gets or sets the user security level for the control.</span></span>                                                                                                                                               |
| <span data-ttu-id="6ee3b-350">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-350">public int userSkip(\[int value\])</span></span>                                                                                  | <span data-ttu-id="6ee3b-351">ユーザーが Tab キーを押してコントロールに移動するときにフォーム グループ コントロールがスキップされるかどうかを示す整数を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-351">Sets or returns an integer that indicates whether the form group control is skipped when the user presses the TAB key to move to controls.</span></span>                                                          |
| <span data-ttu-id="6ee3b-352">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-352">public int userWidth(\[int value\])</span></span>                                                                                 | <span data-ttu-id="6ee3b-353">フォーム グループ コントロールの幅をピクセル単位で示す整数を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-353">Sets or returns an integer that indicates the width of a form group control in pixels.</span></span>                                                                                                              |
| <span data-ttu-id="6ee3b-354">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-354">public boolean useUserLayout(\[boolean value\])</span></span>                                                                     | <span data-ttu-id="6ee3b-355">フォーム グループ コントロールのユーザー指定レイアウトを使用するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-355">Specifies whether to use the user-specified layout of a form group control.</span></span>                                                                                                                         |
| <span data-ttu-id="6ee3b-356">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-356">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                        | <span data-ttu-id="6ee3b-357">ピクセルでフォーム グループ コントロールの上と下のスペースの量を取得または設定し、スペースを計算する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-357">Gets or sets the amount of space above and below a form group control in pixels, and specifies how the space is calculated.</span></span>                                                                         |
| <span data-ttu-id="6ee3b-358">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-358">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                              | <span data-ttu-id="6ee3b-359">フォーム グループ コントロールの上と下のスペースの量を計算する方法を示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-359">Sets or returns a value that indicates how the amount of space above and below a form group control is calculated.</span></span>                                                                                  |
| <span data-ttu-id="6ee3b-360">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-360">public int verticalSpacingValue(\[int value\])</span></span>                                                                      | <span data-ttu-id="6ee3b-361">ピクセルでフォーム グループ コントロールの上と下のスペースの量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-361">Gets or sets the amount of space above and below a form group control in pixels.</span></span>                                                                                                                    |
| <span data-ttu-id="6ee3b-362">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-362">public int viewEditMode(\[int value\])</span></span>                                                                              |                                                                                                                                                                                                     |
| <span data-ttu-id="6ee3b-363">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-363">public boolean visible(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="6ee3b-364">フォーム グループ コントロールを表示または非表示にするブール値データ型を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-364">Gets or sets a Boolean data type that displays or hides a form group control.</span></span>                                                                                                                       |
| <span data-ttu-id="6ee3b-365">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-365">public int width(int value, \[int mode\])</span></span>                                                                           | <span data-ttu-id="6ee3b-366">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-366">Gets or sets the width of the control.</span></span>                                                                                                                                                              |
| <span data-ttu-id="6ee3b-367">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-367">public int widthMode(\[int value\])</span></span>                                                                                 | <span data-ttu-id="6ee3b-368">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-368">Gets or sets the calculation mode for the width of the control.</span></span>                                                                                                                                     |
| <span data-ttu-id="6ee3b-369">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-369">public int widthValue(\[int value\])</span></span>                                                                                | <span data-ttu-id="6ee3b-370">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-370">Gets or sets the width of the control.</span></span>                                                                                                                                                              |
| <span data-ttu-id="6ee3b-371">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-371">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span>         |                                                                                                                                                                                                     |
| <span data-ttu-id="6ee3b-372">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="6ee3b-372">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                           | <span data-ttu-id="6ee3b-373">ユーザーがフォーム グループ コントロールまたはフォーム グループ コントロールのアイテムを新しい位置にドロップすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-373">Is called when a user drops a form group control or an item in a form group control into a new position.</span></span>                                                                                            |
| <span data-ttu-id="6ee3b-374">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-374">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                        |                                                                                                                                                                                                     |
| <span data-ttu-id="6ee3b-375">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-375">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                            |                                                                                                                                                                                                     |
| <span data-ttu-id="6ee3b-376">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-376">public void mouseLeave()</span></span>                                                                                            | <span data-ttu-id="6ee3b-377">ユーザーがマウス ポインターをコントロールから離すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-377">Is called when the user moves the mouse pointer away from the control.</span></span>                                                                                                                              |
| <span data-ttu-id="6ee3b-378">public void context()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-378">public void context()</span></span>                                                                                               | <span data-ttu-id="6ee3b-379">ユーザーがフォーム グループ コントロールを右クリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-379">Is called when the user right-clicks a form group control.</span></span>                                                                                                                                          |
| <span data-ttu-id="6ee3b-380">public void copy()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-380">public void copy()</span></span>                                                                                                  | <span data-ttu-id="6ee3b-381">フォーム グループ コントロールをコピーします。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-381">Copies a form group control.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="6ee3b-382">public void cut()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-382">public void cut()</span></span>                                                                                                   | <span data-ttu-id="6ee3b-383">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-383">Cuts the contents of the control.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="6ee3b-384">public void paste()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-384">public void paste()</span></span>                                                                                                 | <span data-ttu-id="6ee3b-385">フォーム グループ コントロールを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-385">Pastes a form group control.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="6ee3b-386">public void arrange()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-386">public void arrange()</span></span>                                                                                               |                                                                                                                                                                                                     |
| <span data-ttu-id="6ee3b-387">public void clicked()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-387">public void clicked()</span></span>                                                                                               | <span data-ttu-id="6ee3b-388">フォーム グループ コントロールがユーザーにクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-388">Is called when a form group control is clicked by the user.</span></span>                                                                                                                                         |
| <span data-ttu-id="6ee3b-389">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-389">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                          |                                                                                                                                                                                                     |
| <span data-ttu-id="6ee3b-390">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="6ee3b-390">public void inputSearch(str searchStr)</span></span>                                                                              | <span data-ttu-id="6ee3b-391">ユーザーがバインドされたコントロールに検索文字列を入力すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-391">Is called when the user enters a search string in a bound control.</span></span>                                                                                                                                  |
| <span data-ttu-id="6ee3b-392">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-392">public void resetUserSetting()</span></span>                                                                                      | <span data-ttu-id="6ee3b-393">フォーム グループ コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-393">Resets the user settings for a form group control.</span></span>                                                                                                                                                  |
| <span data-ttu-id="6ee3b-394">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-394">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                          |                                                                                                                                                                                                     |
| <span data-ttu-id="6ee3b-395">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-395">public void lostFocus()</span></span>                                                                                             | <span data-ttu-id="6ee3b-396">ユーザーがフォーム グループ コントロールをフォーカス外に持っていくと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-396">Is called when the user brings a form group control out of focus.</span></span>                                                                                                                                   |
| <span data-ttu-id="6ee3b-397">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="6ee3b-397">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                               | <span data-ttu-id="6ee3b-398">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-398">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                                                |
| <span data-ttu-id="6ee3b-399">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-399">public void endDrag()</span></span>                                                                                               | <span data-ttu-id="6ee3b-400">ユーザーがフォーム グループ コントロールの移動を終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-400">Is called when the user has finished moving a form group control.</span></span>                                                                                                                                   |
| <span data-ttu-id="6ee3b-401">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-401">public void jumpRef()</span></span>                                                                                               | <span data-ttu-id="6ee3b-402">ユーザーがフォーム グループ コントロールのコントロール ショートカット メニューでメイン テーブルへ移動フォーム コマンドをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-402">Is called when a user clicks the Go to the Main Table Form command on a control shortcut menu in a form group control.</span></span>                                                                              |
| <span data-ttu-id="6ee3b-403">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-403">public void setFocus()</span></span>                                                                                              | <span data-ttu-id="6ee3b-404">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-404">Sets the focus on the control.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="6ee3b-405">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-405">public void filter(\[str filterStr\])</span></span>                                                                               | <span data-ttu-id="6ee3b-406">ユーザーがフォーム グループ コントロールを右クリックしてから選択フィルタをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-406">Is called when the user right-clicks a form group control and then clicks Filter By Selection.</span></span>                                                                                                      |
| <span data-ttu-id="6ee3b-407">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-407">public void displayControl()</span></span>                                                                                        | <span data-ttu-id="6ee3b-408">フォーム グループ コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-408">Displays a form group control.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="6ee3b-409">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-409">public void gotFocus()</span></span>                                                                                              | <span data-ttu-id="6ee3b-410">ユーザーがフォーム グループ コントロールにフォーカスを移すタイミングを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-410">Determines when the user brings a form group control into focus.</span></span>                                                                                                                                    |
| <span data-ttu-id="6ee3b-411">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="6ee3b-411">public void prefColumnSize(int width, int height)</span></span>                                                                   | <span data-ttu-id="6ee3b-412">フォーム グループ コントロールの列の高さと幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-412">Specifies the height and width of columns for a form group control.</span></span>                                                                                                                                 |
| <span data-ttu-id="6ee3b-413">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-413">public void dragLeave()</span></span>                                                                                             | <span data-ttu-id="6ee3b-414">ユーザーがフォーム グループ コントロールの境界からオブジェクトをドラッグすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-414">Is called when the user drags an object out of the bounds of a form group control.</span></span>                                                                                                                  |
| <span data-ttu-id="6ee3b-415">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="6ee3b-415">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                         |                                                                                                                                                                                                     |
| <span data-ttu-id="6ee3b-416">public void enter()</span><span class="sxs-lookup"><span data-stu-id="6ee3b-416">public void enter()</span></span>                                                                                                 | <span data-ttu-id="6ee3b-417">ユーザーがフォーム グループ コントロールにフォーカスを移動すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-417">Is called when the user moves focus to a form group control.</span></span>                                                                                                                                        |
| <span data-ttu-id="6ee3b-418">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="6ee3b-418">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                       | <span data-ttu-id="6ee3b-419">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-419">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                                              |

## <a name="method-addcontrol"></a><span data-ttu-id="6ee3b-420">メソッド addControl</span><span class="sxs-lookup"><span data-stu-id="6ee3b-420">Method addControl</span></span>

<span data-ttu-id="6ee3b-421">フォーム グループ コントロールにフォームのコントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-421">Adds a form control to a form group control.</span></span>

```xpp
public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrol"></a><span data-ttu-id="6ee3b-422">パラメーター - addControl</span><span class="sxs-lookup"><span data-stu-id="6ee3b-422">Parameters - addControl</span></span>

<span data-ttu-id="6ee3b-423">controlType</span><span class="sxs-lookup"><span data-stu-id="6ee3b-423">controlType</span></span>  
<span data-ttu-id="6ee3b-424">コントロールの位置を示す値、オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-424">A value that indicates the position of the control; optional.</span></span> <span data-ttu-id="6ee3b-425">既定値は、nullNothingnullptrunita null 参照 (Visual Basic にはない) です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-425">The default value is nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

<!-- -->

<span data-ttu-id="6ee3b-426">controlName</span><span class="sxs-lookup"><span data-stu-id="6ee3b-426">controlName</span></span>  
<span data-ttu-id="6ee3b-427">コントロールの位置を示す値、オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-427">A value that indicates the position of the control; optional.</span></span> <span data-ttu-id="6ee3b-428">既定値は、nullNothingnullptrunita null 参照 (Visual Basic にはない) です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-428">The default value is nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

<!-- -->

<span data-ttu-id="6ee3b-429">insertAfter</span><span class="sxs-lookup"><span data-stu-id="6ee3b-429">insertAfter</span></span>  
<span data-ttu-id="6ee3b-430">コントロールの位置を示す値、オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-430">A value that indicates the position of the control; optional.</span></span> <span data-ttu-id="6ee3b-431">既定値は、nullNothingnullptrunita null 参照 (Visual Basic にはない) です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-431">The default value is nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

### <a name="return-value---addcontrol"></a><span data-ttu-id="6ee3b-432">戻り値 - addControl</span><span class="sxs-lookup"><span data-stu-id="6ee3b-432">Return Value - addControl</span></span>

<span data-ttu-id="6ee3b-433">フォーム コントロールを構成する FormControl オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-433">A FormControl object that configures form controls.</span></span>

## <a name="method-addcontrolex"></a><span data-ttu-id="6ee3b-434">メソッド addControlEx</span><span class="sxs-lookup"><span data-stu-id="6ee3b-434">Method addControlEx</span></span>

```xpp
public FormControl addControlEx(str controlClass, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrolex"></a><span data-ttu-id="6ee3b-435">パラメーター - addControlEx</span><span class="sxs-lookup"><span data-stu-id="6ee3b-435">Parameters - addControlEx</span></span>

<span data-ttu-id="6ee3b-436">controlClass</span><span class="sxs-lookup"><span data-stu-id="6ee3b-436">controlClass</span></span>  

<!-- -->

<span data-ttu-id="6ee3b-437">controlName</span><span class="sxs-lookup"><span data-stu-id="6ee3b-437">controlName</span></span>  

<!-- -->

<span data-ttu-id="6ee3b-438">insertAfter</span><span class="sxs-lookup"><span data-stu-id="6ee3b-438">insertAfter</span></span>  

### <a name="return-value---addcontrolex"></a><span data-ttu-id="6ee3b-439">戻り値 - addControlEx</span><span class="sxs-lookup"><span data-stu-id="6ee3b-439">Return Value - addControlEx</span></span>

## <a name="method-adddatafield"></a><span data-ttu-id="6ee3b-440">メソッド addDataField</span><span class="sxs-lookup"><span data-stu-id="6ee3b-440">Method addDataField</span></span>

<span data-ttu-id="6ee3b-441">テーブル フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-441">Adds a table field.</span></span>

```xpp
public FormControl addDataField(int dataSourceId, FieldId fieldId, [FormControl insertAfter], [int arrayIndex])
```

### <a name="parameters---adddatafield"></a><span data-ttu-id="6ee3b-442">パラメーター - addDataField</span><span class="sxs-lookup"><span data-stu-id="6ee3b-442">Parameters - addDataField</span></span>

<span data-ttu-id="6ee3b-443">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="6ee3b-443">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="6ee3b-444">fieldId</span><span class="sxs-lookup"><span data-stu-id="6ee3b-444">fieldId</span></span>  

<!-- -->

<span data-ttu-id="6ee3b-445">insertAfter</span><span class="sxs-lookup"><span data-stu-id="6ee3b-445">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="6ee3b-446">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="6ee3b-446">arrayIndex</span></span>  

### <a name="return-value---adddatafield"></a><span data-ttu-id="6ee3b-447">戻り値 - addDataField</span><span class="sxs-lookup"><span data-stu-id="6ee3b-447">Return Value - addDataField</span></span>

<span data-ttu-id="6ee3b-448">フォーム コントロールを変更する FormControl オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-448">A FormControl object that modifies a form control.</span></span>

## <a name="method-alignchild"></a><span data-ttu-id="6ee3b-449">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="6ee3b-449">Method alignChild</span></span>

<span data-ttu-id="6ee3b-450">フォーム グループ コントロールが、フォーム内の他のコントロールと同じ方法で一致しているかどうかを示すブール値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-450">Sets or returns a Boolean value that indicates whether a form group control is aligned in the same manner as other controls in a form.</span></span>

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a><span data-ttu-id="6ee3b-451">パラメーター - alignChild</span><span class="sxs-lookup"><span data-stu-id="6ee3b-451">Parameters - alignChild</span></span>

<span data-ttu-id="6ee3b-452">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-452">value</span></span>  
<span data-ttu-id="6ee3b-453">フォーム グループ コントロールが、フォーム内の他のコントロールと同じ方法で一致しているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-453">A Boolean value that indicates whether a form group control is aligned in the same manner as other controls in a form; optional.</span></span>

### <a name="return-value---alignchild"></a><span data-ttu-id="6ee3b-454">戻り値 - alignChild</span><span class="sxs-lookup"><span data-stu-id="6ee3b-454">Return Value - alignChild</span></span>

<span data-ttu-id="6ee3b-455">コントロールがアラインされた場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-455">true if a control is aligned; otherwise, false.</span></span>

## <a name="method-alignchildren"></a><span data-ttu-id="6ee3b-456">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="6ee3b-456">Method alignChildren</span></span>

<span data-ttu-id="6ee3b-457">子コントロールが一致しているかどうかを示すブール値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-457">Sets or returns a Boolean value that indicates whether the child controls are aligned.</span></span>

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a><span data-ttu-id="6ee3b-458">パラメーター - alignChildren</span><span class="sxs-lookup"><span data-stu-id="6ee3b-458">Parameters - alignChildren</span></span>

<span data-ttu-id="6ee3b-459">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-459">value</span></span>  
<span data-ttu-id="6ee3b-460">子コントロールが一致しているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-460">A Boolean value that indicates whether the child controls are aligned; optional.</span></span>

### <a name="return-value---alignchildren"></a><span data-ttu-id="6ee3b-461">戻り値 - alignChildren</span><span class="sxs-lookup"><span data-stu-id="6ee3b-461">Return Value - alignChildren</span></span>

<span data-ttu-id="6ee3b-462">子コントロールがアラインされた場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-462">true if the child controls are aligned; otherwise, false.</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="6ee3b-463">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="6ee3b-463">Method alignControl</span></span>

<span data-ttu-id="6ee3b-464">コントロールが他のコントロールと揃っているかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-464">Determines whether the control is aligned with other controls.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="6ee3b-465">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="6ee3b-465">Parameters - alignControl</span></span>

<span data-ttu-id="6ee3b-466">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-466">value</span></span>  
<span data-ttu-id="6ee3b-467">フォーム グループ コントロールが他のコントロールと一致しているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-467">A Boolean value that indicates whether a form group control is aligned with other controls.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="6ee3b-468">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="6ee3b-468">Return Value - alignControl</span></span>

<span data-ttu-id="6ee3b-469">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-469">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="6ee3b-470">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="6ee3b-470">Remarks - alignControl</span></span>

<span data-ttu-id="6ee3b-471">コントロールの左上隅は、最も長いラベルに基づいて配置されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-471">The upper-left corner of the control is aligned based on the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="6ee3b-472">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="6ee3b-472">Method allowEdit</span></span>

<span data-ttu-id="6ee3b-473">ユーザーがコントロールの内容を修正できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-473">Determines whether the user can modify the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="6ee3b-474">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="6ee3b-474">Parameters - allowEdit</span></span>

<span data-ttu-id="6ee3b-475">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-475">value</span></span>  
<span data-ttu-id="6ee3b-476">データを変更できるかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-476">A Boolean value that indicates whether data can be modified; optional.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="6ee3b-477">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="6ee3b-477">Return Value - allowEdit</span></span>

<span data-ttu-id="6ee3b-478">コントロールを変更することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-478">true if the control can be modified; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="6ee3b-479">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="6ee3b-479">Remarks - allowEdit</span></span>

<span data-ttu-id="6ee3b-480">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-480">If this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="6ee3b-481">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="6ee3b-481">Method allowSysSetup</span></span>

<span data-ttu-id="6ee3b-482">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-482">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="6ee3b-483">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="6ee3b-483">Return Value - allowSysSetup</span></span>

<span data-ttu-id="6ee3b-484">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-484">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-allowusersetup"></a><span data-ttu-id="6ee3b-485">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="6ee3b-485">Method allowUserSetup</span></span>

<span data-ttu-id="6ee3b-486">フォーム グループ コントロールに実行できる変更のレベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-486">Sets or gets the level of modification that can be performed for a form group control.</span></span>

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a><span data-ttu-id="6ee3b-487">パラメーター - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="6ee3b-487">Parameters - allowUserSetup</span></span>

<span data-ttu-id="6ee3b-488">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-488">value</span></span>  
<span data-ttu-id="6ee3b-489">実行可能な変更のレベルを示す整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-489">An Integer data type that indicates the level of modification that can be performed; optional.</span></span>

### <a name="return-value---allowusersetup"></a><span data-ttu-id="6ee3b-490">戻り値 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="6ee3b-490">Return Value - allowUserSetup</span></span>

<span data-ttu-id="6ee3b-491">実行可能な変更のレベルを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-491">An integer value that indicates the level of modification that can be performed.</span></span>

### <a name="remarks---allowusersetup"></a><span data-ttu-id="6ee3b-492">備考 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="6ee3b-492">Remarks - allowUserSetup</span></span>

<span data-ttu-id="6ee3b-493">値パラメーターのために FormAllowUserSetup 列挙型値を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-493">You can use a FormAllowUserSetup enumeration value for the value parameter.</span></span>

## <a name="method-arrangeguide"></a><span data-ttu-id="6ee3b-494">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="6ee3b-494">Method arrangeGuide</span></span>

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a><span data-ttu-id="6ee3b-495">パラメーター - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="6ee3b-495">Parameters - arrangeGuide</span></span>

<span data-ttu-id="6ee3b-496">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-496">value</span></span>  

### <a name="return-value---arrangeguide"></a><span data-ttu-id="6ee3b-497">戻り値 - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="6ee3b-497">Return Value - arrangeGuide</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="6ee3b-498">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="6ee3b-498">Method arrangeMethod</span></span>

<span data-ttu-id="6ee3b-499">フォーム グループ コントロールのコントロールを配置する方法を示す整数値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-499">Sets or returns an integer value that indicates how controls in a form group control are arranged.</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="6ee3b-500">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="6ee3b-500">Parameters - arrangeMethod</span></span>

<span data-ttu-id="6ee3b-501">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-501">value</span></span>  
<span data-ttu-id="6ee3b-502">フォーム グループ コントロールのコントロールを配置する方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-502">An integer value that indicates how controls in a form group control are arranged; optional.</span></span>

### <a name="return-value---arrangemethod"></a><span data-ttu-id="6ee3b-503">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="6ee3b-503">Return Value - arrangeMethod</span></span>

<span data-ttu-id="6ee3b-504">フォーム グループ コントロールのコントロールを配置する方法を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-504">An integer value that indicates how controls in a form group control are arranged.</span></span>

### <a name="remarks---arrangemethod"></a><span data-ttu-id="6ee3b-505">備考 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="6ee3b-505">Remarks - arrangeMethod</span></span>

<span data-ttu-id="6ee3b-506">\_value パラメーターのために ArrangeMethod 列挙型値を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-506">You can use an ArrangeMethod enumeration value for the \_value parameter.</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="6ee3b-507">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="6ee3b-507">Method arrangeWhen</span></span>

<span data-ttu-id="6ee3b-508">コントロールが配置されるタイミングを指定する整数値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-508">Sets or returns an integer value that specifies when the controls are arranged.</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="6ee3b-509">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="6ee3b-509">Parameters - arrangeWhen</span></span>

<span data-ttu-id="6ee3b-510">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-510">value</span></span>  
<span data-ttu-id="6ee3b-511">コントロールが配置されるタイミングを指定する整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-511">An integer value that specifies when the controls are arranged; optional.</span></span>

### <a name="return-value---arrangewhen"></a><span data-ttu-id="6ee3b-512">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="6ee3b-512">Return Value - arrangeWhen</span></span>

<span data-ttu-id="6ee3b-513">コントロールが配置されるタイミングを指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-513">An integer value that specifies when the controls are arranged.</span></span>

## <a name="method-autodatagroup"></a><span data-ttu-id="6ee3b-514">メソッド autoDataGroup</span><span class="sxs-lookup"><span data-stu-id="6ee3b-514">Method autoDataGroup</span></span>

<span data-ttu-id="6ee3b-515">フォーム グループ コントロールに、コントロールに対して指定されているデータ グループ内のフィールドのみ含めることができるかどうかを指定するブール値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-515">Sets or returns a Boolean value that specifies whether a form group control can contain only the fields in the data group that are specified for the control.</span></span>

```xpp
public boolean autoDataGroup([boolean value])
```

### <a name="parameters---autodatagroup"></a><span data-ttu-id="6ee3b-516">パラメーター - autoDataGroup</span><span class="sxs-lookup"><span data-stu-id="6ee3b-516">Parameters - autoDataGroup</span></span>

<span data-ttu-id="6ee3b-517">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-517">value</span></span>  
<span data-ttu-id="6ee3b-518">フォーム グループ コントロールがデータ グループ内のフィールドのみを含めることができるかどうかを示すブール値データ型。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-518">A Boolean data type that indicates whether a form group control can contain only fields in the data group; optional.</span></span>

### <a name="return-value---autodatagroup"></a><span data-ttu-id="6ee3b-519">戻り値 - autoDataGroup</span><span class="sxs-lookup"><span data-stu-id="6ee3b-519">Return Value - autoDataGroup</span></span>

<span data-ttu-id="6ee3b-520">フォーム グループ コントロールにデータ グループ内のフィールドのみを含めることができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-520">true if a form group control can contain only fields in the data group; otherwise, false.</span></span>

### <a name="remarks---autodatagroup"></a><span data-ttu-id="6ee3b-521">備考 - autoDataGroup</span><span class="sxs-lookup"><span data-stu-id="6ee3b-521">Remarks - autoDataGroup</span></span>

<span data-ttu-id="6ee3b-522">フォーム グループ コントロールのデータ グループを設定または取得するには、FormGroupControl.dataGroup メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-522">You use the FormGroupControl.dataGroup method to set or return a data group for a form group control.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="6ee3b-523">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6ee3b-523">Method autoDeclaration</span></span>

<span data-ttu-id="6ee3b-524">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-524">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="6ee3b-525">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6ee3b-525">Parameters - autoDeclaration</span></span>

<span data-ttu-id="6ee3b-526">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-526">value</span></span>  
<span data-ttu-id="6ee3b-527">フォーム グループ コントロールと同じ名前の変数を、システムが宣言するかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-527">A Boolean value that indicates whether the system declares a variable of the same name as a form group control; optional.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="6ee3b-528">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6ee3b-528">Return Value - autoDeclaration</span></span>

<span data-ttu-id="6ee3b-529">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-529">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="6ee3b-530">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6ee3b-530">Remarks - autoDeclaration</span></span>

<span data-ttu-id="6ee3b-531">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-531">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="6ee3b-532">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="6ee3b-532">Method backgroundColor</span></span>

<span data-ttu-id="6ee3b-533">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-533">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="6ee3b-534">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="6ee3b-534">Parameters - backgroundColor</span></span>

<span data-ttu-id="6ee3b-535">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-535">value</span></span>  
<span data-ttu-id="6ee3b-536">背景色を指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-536">An Integer data type that specifies the background color; optional.</span></span>

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="6ee3b-537">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="6ee3b-537">Return Value - backgroundColor</span></span>

<span data-ttu-id="6ee3b-538">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-538">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="6ee3b-539">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="6ee3b-539">Remarks - backgroundColor</span></span>

<span data-ttu-id="6ee3b-540">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-540">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="6ee3b-541">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-541">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="6ee3b-542">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-542">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="6ee3b-543">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-543">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="6ee3b-544">上位バイトは 0 (ゼロ) でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-544">The high-order byte must be 0 (zero).</span></span>
-   <span data-ttu-id="6ee3b-545">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-545">The maximum value for a single byte is 255.</span></span>

## <a name="method-backgroundimage"></a><span data-ttu-id="6ee3b-546">メソッド backgroundImage</span><span class="sxs-lookup"><span data-stu-id="6ee3b-546">Method backgroundImage</span></span>

<span data-ttu-id="6ee3b-547">フォーム グループ コントロールの背景イメージを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-547">Specifies the background image for a form group control.</span></span>

```xpp
public Image backgroundImage([Image image], [int drawMode])
```

### <a name="parameters---backgroundimage"></a><span data-ttu-id="6ee3b-548">パラメーター - backgroundImage</span><span class="sxs-lookup"><span data-stu-id="6ee3b-548">Parameters - backgroundImage</span></span>

<span data-ttu-id="6ee3b-549">画像</span><span class="sxs-lookup"><span data-stu-id="6ee3b-549">image</span></span>  
<span data-ttu-id="6ee3b-550">画像の描画方法を指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-550">An Integer data type that specifies how the image is drawn; optional.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-551">drawMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-551">drawMode</span></span>  
<span data-ttu-id="6ee3b-552">画像の描画方法を指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-552">An Integer data type that specifies how the image is drawn; optional.</span></span>

### <a name="return-value---backgroundimage"></a><span data-ttu-id="6ee3b-553">戻り値 - backgroundImage</span><span class="sxs-lookup"><span data-stu-id="6ee3b-553">Return Value - backgroundImage</span></span>

<span data-ttu-id="6ee3b-554">イメージ オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-554">An Image object.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="6ee3b-555">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="6ee3b-555">Method backStyle</span></span>

<span data-ttu-id="6ee3b-556">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-556">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="6ee3b-557">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="6ee3b-557">Parameters - backStyle</span></span>

<span data-ttu-id="6ee3b-558">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-558">value</span></span>  
<span data-ttu-id="6ee3b-559">背景スタイル示す整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-559">An Integer data type that indicates the background style; optional.</span></span>

### <a name="return-value---backstyle"></a><span data-ttu-id="6ee3b-560">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="6ee3b-560">Return Value - backStyle</span></span>

<span data-ttu-id="6ee3b-561">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-561">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="6ee3b-562">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="6ee3b-562">Method beginDrag</span></span>

<span data-ttu-id="6ee3b-563">ユーザーがフォーム グループ コントロールの移動を始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-563">Is called when the user starts to move a form group control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="6ee3b-564">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="6ee3b-564">Parameters - beginDrag</span></span>

<span data-ttu-id="6ee3b-565">x</span><span class="sxs-lookup"><span data-stu-id="6ee3b-565">x</span></span>  
<span data-ttu-id="6ee3b-566">移動イベントの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-566">An integer value that indicates the y-coordinate for the move event.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-567">y</span><span class="sxs-lookup"><span data-stu-id="6ee3b-567">y</span></span>  
<span data-ttu-id="6ee3b-568">移動イベントの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-568">An integer value that indicates the y-coordinate for the move event.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="6ee3b-569">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="6ee3b-569">Return Value - beginDrag</span></span>

<span data-ttu-id="6ee3b-570">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-570">0 (zero) if the event has been handled.</span></span>

## <a name="method-bold"></a><span data-ttu-id="6ee3b-571">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="6ee3b-571">Method bold</span></span>

<span data-ttu-id="6ee3b-572">コントロール内のテキストを表示するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-572">Gets or sets the weight of font that is used to display text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="6ee3b-573">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="6ee3b-573">Parameters - bold</span></span>

<span data-ttu-id="6ee3b-574">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-574">value</span></span>  
<span data-ttu-id="6ee3b-575">フォントの太さを指定する整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-575">An integer value that specifies the font weight; optional.</span></span>

### <a name="return-value---bold"></a><span data-ttu-id="6ee3b-576">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="6ee3b-576">Return Value - bold</span></span>

<span data-ttu-id="6ee3b-577">0 (ゼロ) から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-577">An integer value between 0 (zero) and 9, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="6ee3b-578">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="6ee3b-578">Remarks - bold</span></span>

<span data-ttu-id="6ee3b-579">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-579">The integer that is returned contains the font weight as follows:</span></span>

-   <span data-ttu-id="6ee3b-580">0 � 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-580">0 � Use the default font weight.</span></span>
-   <span data-ttu-id="6ee3b-581">1 � シン。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-581">1 � Thin.</span></span>
-   <span data-ttu-id="6ee3b-582">2 � エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-582">2 � Extra-light.</span></span>
-   <span data-ttu-id="6ee3b-583">3 � ライト。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-583">3 � Light.</span></span>
-   <span data-ttu-id="6ee3b-584">4 � 標準。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-584">4 � Normal.</span></span>
-   <span data-ttu-id="6ee3b-585">5 � 中。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-585">5 � Medium.</span></span>
-   <span data-ttu-id="6ee3b-586">6 � セミボールド。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-586">6 � Semibold.</span></span>
-   <span data-ttu-id="6ee3b-587">7 � 太字。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-587">7 � Bold.</span></span>
-   <span data-ttu-id="6ee3b-588">8 � 極太。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-588">8 � Extra-bold.</span></span>
-   <span data-ttu-id="6ee3b-589">9 � ヘビー。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-589">9 � Heavy.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="6ee3b-590">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="6ee3b-590">Method bottomMargin</span></span>

<span data-ttu-id="6ee3b-591">フォーム グループ コントロールの下余白をピクセル単位で設定するか返し、余白が自動的に調整されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-591">Sets or returns the bottom margin of a form group control in pixels and specifies whether the margin is automatically adjusted.</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="6ee3b-592">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="6ee3b-592">Parameters - bottomMargin</span></span>

<span data-ttu-id="6ee3b-593">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-593">value</span></span>  
<span data-ttu-id="6ee3b-594">下余白が固定されているかどうか、またはフォント サイズ、オプションなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-594">An AutoMode enumeration value that indicates whether the bottom margin is fixed, or whether it is automatically adjusted based on other form settings, such as the font size; optional.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-595">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-595">mode</span></span>  
<span data-ttu-id="6ee3b-596">下余白が固定されているかどうか、またはフォント サイズ、オプションなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-596">An AutoMode enumeration value that indicates whether the bottom margin is fixed, or whether it is automatically adjusted based on other form settings, such as the font size; optional.</span></span>

### <a name="return-value---bottommargin"></a><span data-ttu-id="6ee3b-597">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="6ee3b-597">Return Value - bottomMargin</span></span>

<span data-ttu-id="6ee3b-598">ピクセル単位の下余白を指定する整数データ型値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-598">An Integer data type value that specifies the bottom margin in pixels.</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="6ee3b-599">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-599">Method bottomMarginMode</span></span>

<span data-ttu-id="6ee3b-600">下余白が自動的に調整されるかどうかを示す AutoMode 列挙値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-600">Sets or returns an AutoMode enumeration value that indicates whether the bottom margin is automatically adjusted.</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="6ee3b-601">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-601">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="6ee3b-602">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-602">mode</span></span>  
<span data-ttu-id="6ee3b-603">下余白が固定されているかどうか、またはフォント サイズ、オプションなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-603">An AutoMode enumeration value that indicates whether the bottom margin is fixed, or whether it is automatically adjusted based on other form settings, such as the font size; optional.</span></span>

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="6ee3b-604">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-604">Return Value - bottomMarginMode</span></span>

<span data-ttu-id="6ee3b-605">フォント サイズなどの他のフォーム設定に基づいて余白が自動的に調整される場合は AutoMode::Auto です。それ以外の場合は、AutoMode::Fixed です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-605">AutoMode::Auto if the margin is automatically adjusted based on other form settings, such as the font size; otherwise, AutoMode::Fixed.</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="6ee3b-606">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-606">Method bottomMarginValue</span></span>

<span data-ttu-id="6ee3b-607">フォーム グループ コントロールの下余白をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-607">Sets or returns the bottom margin of a form group control in pixels.</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="6ee3b-608">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-608">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="6ee3b-609">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-609">value</span></span>  
<span data-ttu-id="6ee3b-610">ピクセルの下余白を指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-610">An Integer data type that specifies the bottom margin in pixels; optional.</span></span>

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="6ee3b-611">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-611">Return Value - bottomMarginValue</span></span>

<span data-ttu-id="6ee3b-612">ピクセル単位の下余白を指定する整数データ型値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-612">An Integer data type value that specifies the bottom margin in pixels.</span></span>

## <a name="method-breakable"></a><span data-ttu-id="6ee3b-613">メソッド breakable</span><span class="sxs-lookup"><span data-stu-id="6ee3b-613">Method breakable</span></span>

```xpp
public boolean breakable([boolean value])
```

### <a name="parameters---breakable"></a><span data-ttu-id="6ee3b-614">パラメーター - breakable</span><span class="sxs-lookup"><span data-stu-id="6ee3b-614">Parameters - breakable</span></span>

<span data-ttu-id="6ee3b-615">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-615">value</span></span>  

### <a name="return-value---breakable"></a><span data-ttu-id="6ee3b-616">戻り値 - breakable</span><span class="sxs-lookup"><span data-stu-id="6ee3b-616">Return Value - breakable</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="6ee3b-617">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="6ee3b-617">Method calcControlSize</span></span>

<span data-ttu-id="6ee3b-618">文字数と明細行数に基づいて、フォーム グループ コントロールのフォント サイズを計算します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-618">Calculates the size of a form group control, based on the number of characters and the number of lines.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="6ee3b-619">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="6ee3b-619">Parameters - calcControlSize</span></span>

<span data-ttu-id="6ee3b-620">chars</span><span class="sxs-lookup"><span data-stu-id="6ee3b-620">chars</span></span>  
<span data-ttu-id="6ee3b-621">行数を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-621">An Integer data type that specifies the number of lines.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-622">明細行</span><span class="sxs-lookup"><span data-stu-id="6ee3b-622">lines</span></span>  
<span data-ttu-id="6ee3b-623">行数を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-623">An Integer data type that specifies the number of lines.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="6ee3b-624">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="6ee3b-624">Return Value - calcControlSize</span></span>

<span data-ttu-id="6ee3b-625">フォーム グループ コントロールのサイズを指定するコンテナー データ型値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-625">A Container data type value that specifies the size of a form group control.</span></span>

## <a name="method-canadddatafield"></a><span data-ttu-id="6ee3b-626">メソッド canAddDataField</span><span class="sxs-lookup"><span data-stu-id="6ee3b-626">Method canAddDataField</span></span>

<span data-ttu-id="6ee3b-627">テーブル フィールドを追加できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-627">Indicates whether a table field can be added.</span></span>

```xpp
public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---canadddatafield"></a><span data-ttu-id="6ee3b-628">パラメーター - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="6ee3b-628">Parameters - canAddDataField</span></span>

<span data-ttu-id="6ee3b-629">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="6ee3b-629">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="6ee3b-630">fieldId</span><span class="sxs-lookup"><span data-stu-id="6ee3b-630">fieldId</span></span>  

<!-- -->

<span data-ttu-id="6ee3b-631">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="6ee3b-631">arrayIndex</span></span>  

### <a name="return-value---canadddatafield"></a><span data-ttu-id="6ee3b-632">戻り値 - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="6ee3b-632">Return Value - canAddDataField</span></span>

<span data-ttu-id="6ee3b-633">テーブルを追加できる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-633">true if a table field can be added; otherwise, false.</span></span>

## <a name="method-cancontain"></a><span data-ttu-id="6ee3b-634">メソッド canContain</span><span class="sxs-lookup"><span data-stu-id="6ee3b-634">Method canContain</span></span>

<span data-ttu-id="6ee3b-635">フォーム グループ コントロールに指定されたフォーム コントロールを含めることができるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-635">Specifies whether a form group control can contain the specified form control.</span></span>

```xpp
public boolean canContain(FormControl control)
```

### <a name="parameters---cancontain"></a><span data-ttu-id="6ee3b-636">パラメーター - canContain</span><span class="sxs-lookup"><span data-stu-id="6ee3b-636">Parameters - canContain</span></span>

<span data-ttu-id="6ee3b-637">control</span><span class="sxs-lookup"><span data-stu-id="6ee3b-637">control</span></span>  
<span data-ttu-id="6ee3b-638">フォーム コントロールを指定する FormControl オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-638">A FormControl object that specifies a form control.</span></span>

### <a name="return-value---cancontain"></a><span data-ttu-id="6ee3b-639">戻り値 - canContain</span><span class="sxs-lookup"><span data-stu-id="6ee3b-639">Return Value - canContain</span></span>

<span data-ttu-id="6ee3b-640">フォーム グループ コントロールに指定フォーム コントロールを含めることができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-640">true if a form group control can contain the specified form control; otherwise, false.</span></span>

## <a name="method-caption"></a><span data-ttu-id="6ee3b-641">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="6ee3b-641">Method caption</span></span>

<span data-ttu-id="6ee3b-642">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-642">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="6ee3b-643">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="6ee3b-643">Parameters - caption</span></span>

<span data-ttu-id="6ee3b-644">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-644">value</span></span>  
<span data-ttu-id="6ee3b-645">キャプション テキストを指定する文字列データ型; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-645">A String data type that specifies the caption text; optional.</span></span>

### <a name="return-value---caption"></a><span data-ttu-id="6ee3b-646">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="6ee3b-646">Return Value - caption</span></span>

<span data-ttu-id="6ee3b-647">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-647">The string that is used as the caption of the control.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="6ee3b-648">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="6ee3b-648">Method characterSet</span></span>

<span data-ttu-id="6ee3b-649">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-649">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="6ee3b-650">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="6ee3b-650">Parameters - characterSet</span></span>

<span data-ttu-id="6ee3b-651">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-651">value</span></span>  
<span data-ttu-id="6ee3b-652">テキスト フォントの文字セットを指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-652">An Integer data type that specifies the character set for the text font; optional.</span></span>

### <a name="return-value---characterset"></a><span data-ttu-id="6ee3b-653">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="6ee3b-653">Return Value - characterSet</span></span>

<span data-ttu-id="6ee3b-654">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-654">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="6ee3b-655">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="6ee3b-655">Remarks - characterSet</span></span>

<span data-ttu-id="6ee3b-656">返される整数の値は、次のテーブルに示されるように文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-656">The values for the integer that is returned indicate the character set, as shown in the following table.</span></span>

| <span data-ttu-id="6ee3b-657">先頭値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-657">Value</span></span> | <span data-ttu-id="6ee3b-658">説明</span><span class="sxs-lookup"><span data-stu-id="6ee3b-658">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="6ee3b-659">0</span><span class="sxs-lookup"><span data-stu-id="6ee3b-659">0</span></span>     | <span data-ttu-id="6ee3b-660">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6ee3b-660">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="6ee3b-661">1</span><span class="sxs-lookup"><span data-stu-id="6ee3b-661">1</span></span>     | <span data-ttu-id="6ee3b-662">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6ee3b-662">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="6ee3b-663">2</span><span class="sxs-lookup"><span data-stu-id="6ee3b-663">2</span></span>     | <span data-ttu-id="6ee3b-664">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6ee3b-664">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="6ee3b-665">77</span><span class="sxs-lookup"><span data-stu-id="6ee3b-665">77</span></span>    | <span data-ttu-id="6ee3b-666">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6ee3b-666">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="6ee3b-667">128</span><span class="sxs-lookup"><span data-stu-id="6ee3b-667">128</span></span>   | <span data-ttu-id="6ee3b-668">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6ee3b-668">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="6ee3b-669">129</span><span class="sxs-lookup"><span data-stu-id="6ee3b-669">129</span></span>   | <span data-ttu-id="6ee3b-670">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6ee3b-670">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="6ee3b-671">134</span><span class="sxs-lookup"><span data-stu-id="6ee3b-671">134</span></span>   | <span data-ttu-id="6ee3b-672">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6ee3b-672">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="6ee3b-673">136</span><span class="sxs-lookup"><span data-stu-id="6ee3b-673">136</span></span>   | <span data-ttu-id="6ee3b-674">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6ee3b-674">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="6ee3b-675">161</span><span class="sxs-lookup"><span data-stu-id="6ee3b-675">161</span></span>   | <span data-ttu-id="6ee3b-676">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6ee3b-676">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="6ee3b-677">162</span><span class="sxs-lookup"><span data-stu-id="6ee3b-677">162</span></span>   | <span data-ttu-id="6ee3b-678">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6ee3b-678">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="6ee3b-679">163</span><span class="sxs-lookup"><span data-stu-id="6ee3b-679">163</span></span>   | <span data-ttu-id="6ee3b-680">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6ee3b-680">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="6ee3b-681">186</span><span class="sxs-lookup"><span data-stu-id="6ee3b-681">186</span></span>   | <span data-ttu-id="6ee3b-682">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6ee3b-682">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="6ee3b-683">204</span><span class="sxs-lookup"><span data-stu-id="6ee3b-683">204</span></span>   | <span data-ttu-id="6ee3b-684">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6ee3b-684">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="6ee3b-685">238</span><span class="sxs-lookup"><span data-stu-id="6ee3b-685">238</span></span>   | <span data-ttu-id="6ee3b-686">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6ee3b-686">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="6ee3b-687">255</span><span class="sxs-lookup"><span data-stu-id="6ee3b-687">255</span></span>   | <span data-ttu-id="6ee3b-688">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6ee3b-688">OEM\_CHARSET</span></span>         |

<span data-ttu-id="6ee3b-689">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-689">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="6ee3b-690">金額</span><span class="sxs-lookup"><span data-stu-id="6ee3b-690">Value</span></span> | <span data-ttu-id="6ee3b-691">説明</span><span class="sxs-lookup"><span data-stu-id="6ee3b-691">Description</span></span>    |
|-------|----------------|
| <span data-ttu-id="6ee3b-692">130</span><span class="sxs-lookup"><span data-stu-id="6ee3b-692">130</span></span>   | <span data-ttu-id="6ee3b-693">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6ee3b-693">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="6ee3b-694">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-694">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="6ee3b-695">先頭値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-695">Value</span></span> | <span data-ttu-id="6ee3b-696">説明</span><span class="sxs-lookup"><span data-stu-id="6ee3b-696">Description</span></span>     |
|-------|-----------------|
| <span data-ttu-id="6ee3b-697">177</span><span class="sxs-lookup"><span data-stu-id="6ee3b-697">177</span></span>   | <span data-ttu-id="6ee3b-698">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6ee3b-698">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="6ee3b-699">178</span><span class="sxs-lookup"><span data-stu-id="6ee3b-699">178</span></span>   | <span data-ttu-id="6ee3b-700">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6ee3b-700">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="6ee3b-701">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-701">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="6ee3b-702">先頭値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-702">Value</span></span> | <span data-ttu-id="6ee3b-703">説明</span><span class="sxs-lookup"><span data-stu-id="6ee3b-703">Description</span></span>   |
|-------|---------------|
| <span data-ttu-id="6ee3b-704">222</span><span class="sxs-lookup"><span data-stu-id="6ee3b-704">222</span></span>   | <span data-ttu-id="6ee3b-705">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6ee3b-705">THAI\_CHARSET</span></span> |

<span data-ttu-id="6ee3b-706">既定の文字が設定される値は、現在のシステム ロケールに応じて設定されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-706">The value that the default character is set to depends on the current system locale.</span></span> <span data-ttu-id="6ee3b-707">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-707">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="6ee3b-708">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-708">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="6ee3b-709">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="6ee3b-709">Method colorScheme</span></span>

<span data-ttu-id="6ee3b-710">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-710">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="6ee3b-711">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="6ee3b-711">Parameters - colorScheme</span></span>

<span data-ttu-id="6ee3b-712">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-712">value</span></span>  
<span data-ttu-id="6ee3b-713">フォーム グループ コントロールのカラー パレットを指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-713">An Integer data type that specifies the color palette for a form group control; optional.</span></span>

### <a name="return-value---colorscheme"></a><span data-ttu-id="6ee3b-714">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="6ee3b-714">Return Value - colorScheme</span></span>

<span data-ttu-id="6ee3b-715">0 (ゼロ) から 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-715">An integer between 0 (zero) and 2, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="6ee3b-716">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="6ee3b-716">Remarks - colorScheme</span></span>

<span data-ttu-id="6ee3b-717">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-717">The color scheme is defined according to the following table.</span></span>

| <span data-ttu-id="6ee3b-718">先頭値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-718">Value</span></span> | <span data-ttu-id="6ee3b-719">スタイル</span><span class="sxs-lookup"><span data-stu-id="6ee3b-719">Style</span></span>                  |
|-------|------------------------|
| <span data-ttu-id="6ee3b-720">0</span><span class="sxs-lookup"><span data-stu-id="6ee3b-720">0</span></span>     | <span data-ttu-id="6ee3b-721">既定。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-721">Default.</span></span>               |
| <span data-ttu-id="6ee3b-722">1</span><span class="sxs-lookup"><span data-stu-id="6ee3b-722">1</span></span>     | <span data-ttu-id="6ee3b-723">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-723">The Windows palette.</span></span>   |
| <span data-ttu-id="6ee3b-724">2</span><span class="sxs-lookup"><span data-stu-id="6ee3b-724">2</span></span>     | <span data-ttu-id="6ee3b-725">真の配色。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-725">The true-color scheme.</span></span> |

## <a name="method-columns"></a><span data-ttu-id="6ee3b-726">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="6ee3b-726">Method columns</span></span>

<span data-ttu-id="6ee3b-727">フォーム グループ コントロールの列の数をピクセル単位で設定するか返し、数が自動的に調整されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-727">Sets or returns the number of columns in a form group control in pixels, and specifies whether the number is automatically adjusted.</span></span>

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="6ee3b-728">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="6ee3b-728">Parameters - columns</span></span>

<span data-ttu-id="6ee3b-729">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-729">value</span></span>  
<span data-ttu-id="6ee3b-730">列数が固定されているかどうか、またはフォーム サイズなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-730">An AutoMode enumeration value that specifies whether the number of columns is fixed, or whether it is automatically adjusted based on other form settings, such as the form size.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-731">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-731">mode</span></span>  
<span data-ttu-id="6ee3b-732">列数が固定されているかどうか、またはフォーム サイズなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-732">An AutoMode enumeration value that specifies whether the number of columns is fixed, or whether it is automatically adjusted based on other form settings, such as the form size.</span></span>

### <a name="return-value---columns"></a><span data-ttu-id="6ee3b-733">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="6ee3b-733">Return Value - columns</span></span>

<span data-ttu-id="6ee3b-734">フォーム グループ コントロール内の列数をピクセル単位で指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-734">An integer value that specifies the number of columns in a form group control in pixels.</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="6ee3b-735">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-735">Method columnsMode</span></span>

<span data-ttu-id="6ee3b-736">フォーム グループ コントロール内の列数が固定されているかどうか、またはフォーム サイズなどのオプション、他のフォーム設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-736">Sets or returns a value that indicates whether the number of columns in a form group control is fixed, or whether it is automatically adjusted based on other form settings, such as the form size.</span></span>

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="6ee3b-737">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-737">Parameters - columnsMode</span></span>

<span data-ttu-id="6ee3b-738">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-738">mode</span></span>  
<span data-ttu-id="6ee3b-739">列数が固定されているかどうか、またはフォーム サイズなどのオプション、他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-739">An AutoMode enumeration value that specifies whether the number of columns is fixed, or whether it is automatically adjusted based on other form settings, such as the form size; optional.</span></span>

### <a name="return-value---columnsmode"></a><span data-ttu-id="6ee3b-740">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-740">Return Value - columnsMode</span></span>

<span data-ttu-id="6ee3b-741">列の数が自動的に調整される場合は Automode::Auto、それ以外の場合は Automode::Fixed となります。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-741">Automode::Auto if the number of columns is automatically adjusted; otherwise, Automode::Fixed.</span></span>

## <a name="method-columnspace"></a><span data-ttu-id="6ee3b-742">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="6ee3b-742">Method columnspace</span></span>

<span data-ttu-id="6ee3b-743">フォーム グループ コントロール内の列間のスペースの量をピクセル単位で設定するか返し、フォント サイズなどの他のフォーム設定に基づいてスペースが自動的に調整されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-743">Sets or returns the amount of space between columns in a form group control in pixels and indicates whether the space is automatically adjusted based on other form settings, such the font size.</span></span>

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a><span data-ttu-id="6ee3b-744">パラメーター - columnspace</span><span class="sxs-lookup"><span data-stu-id="6ee3b-744">Parameters - columnspace</span></span>

<span data-ttu-id="6ee3b-745">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-745">value</span></span>  
<span data-ttu-id="6ee3b-746">列の間にスペースの量が固定されているかどうか、またはフォント サイズ、オプションなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-746">An AutoMode enumeration value that indicates whether the amount of space between columns is fixed, or whether it is automatically adjusted based on other form settings, such as the font size; optional.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-747">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-747">mode</span></span>  
<span data-ttu-id="6ee3b-748">列の間にスペースの量が固定されているかどうか、またはフォント サイズ、オプションなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-748">An AutoMode enumeration value that indicates whether the amount of space between columns is fixed, or whether it is automatically adjusted based on other form settings, such as the font size; optional.</span></span>

### <a name="return-value---columnspace"></a><span data-ttu-id="6ee3b-749">戻り値 - columnspace</span><span class="sxs-lookup"><span data-stu-id="6ee3b-749">Return Value - columnspace</span></span>

<span data-ttu-id="6ee3b-750">フォーム グループ コントロール内の列の間のスペースをピクセル単位で指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-750">An integer value that specifies the space between columns in a form group control in pixels.</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="6ee3b-751">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-751">Method columnspaceMode</span></span>

<span data-ttu-id="6ee3b-752">フォーム グループ コントロール内の列間のスペースの量が自動的に調整されるかどうかを示す AutoMode 列挙値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-752">Sets or returns an AutoMode enumeration value that indicates whether the amount of space between columns in a form group control is automatically adjusted.</span></span>

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="6ee3b-753">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-753">Parameters - columnspaceMode</span></span>

<span data-ttu-id="6ee3b-754">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-754">mode</span></span>  
<span data-ttu-id="6ee3b-755">列の間にスペースの量が固定されているかどうか、またはフォント サイズ、オプションなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-755">An AutoMode enumeration value that indicates whether the amount of space between columns is fixed, or whether it is automatically adjusted based on other form settings, such as the font size; optional.</span></span>

### <a name="return-value---columnspacemode"></a><span data-ttu-id="6ee3b-756">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-756">Return Value - columnspaceMode</span></span>

<span data-ttu-id="6ee3b-757">容量が自動的に調整される場合は AutoMode::Auto です。それ以外の場合は、AutoMode::Fixed です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-757">AutoMode::Auto if the amount of space is automatically adjusted; otherwise, AutoMode::Fixed.</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="6ee3b-758">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-758">Method columnspaceValue</span></span>

<span data-ttu-id="6ee3b-759">ピクセルでフォーム グループ コントロール内の列間のスペースの量を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-759">Sets or returns the amount of space between columns in a form group control in pixels.</span></span>

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="6ee3b-760">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-760">Parameters - columnspaceValue</span></span>

<span data-ttu-id="6ee3b-761">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-761">value</span></span>  
<span data-ttu-id="6ee3b-762">ピクセルにフォーム グループ コントロール内の列間のスペース量を指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-762">An Integer data type that specifies the amount of space between columns in a form group control in pixels; optional.</span></span>

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="6ee3b-763">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-763">Return Value - columnspaceValue</span></span>

<span data-ttu-id="6ee3b-764">フォーム グループ コントロール内のピクセル単位で列の間の容量を指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-764">An integer value that specifies the amount of space between columns in a form group control in pixels.</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="6ee3b-765">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-765">Method columnsValue</span></span>

<span data-ttu-id="6ee3b-766">フォーム グループ コントロール内のコントロールの数を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-766">Sets or returns the number of columns in a form group control.</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="6ee3b-767">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-767">Parameters - columnsValue</span></span>

<span data-ttu-id="6ee3b-768">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-768">value</span></span>  
<span data-ttu-id="6ee3b-769">フォーム グループ コントロールの列数を指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-769">An Integer data type that specifies the number of columns in a form group control; optional.</span></span>

### <a name="return-value---columnsvalue"></a><span data-ttu-id="6ee3b-770">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-770">Return Value - columnsValue</span></span>

<span data-ttu-id="6ee3b-771">フォーム グループ コントロールの列数を指定する整数データ型値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-771">An Integer data type value that specifies the number of columns in a form group control.</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="6ee3b-772">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="6ee3b-772">Method configurationKey</span></span>

<span data-ttu-id="6ee3b-773">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-773">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="6ee3b-774">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="6ee3b-774">Parameters - configurationKey</span></span>

<span data-ttu-id="6ee3b-775">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-775">value</span></span>  
<span data-ttu-id="6ee3b-776">コンフィギュレーション キーの ID を特定する configurationKeyId システム データ型; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-776">A configurationKeyId system data type that specifies the configuration key ID; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="6ee3b-777">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="6ee3b-777">Return Value - configurationKey</span></span>

<span data-ttu-id="6ee3b-778">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-778">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="6ee3b-779">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="6ee3b-779">Remarks - configurationKey</span></span>

<span data-ttu-id="6ee3b-780">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-780">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="6ee3b-781">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-781">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="6ee3b-782">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="6ee3b-782">Method configurationKeyEx</span></span>

<span data-ttu-id="6ee3b-783">フォーム グループ コントロールのために有効化されたコンフィギュレーション キーの ID を含むリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-783">Retrieves a list that contains the IDs of configuration keys that are activated for a form group control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="6ee3b-784">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="6ee3b-784">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="6ee3b-785">フォーム グループ コントロールのために有効化されたコンフィギュレーション キーの ID を含むリスト オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-785">A List object that contains the IDs of configuration keys that are activated for a form group control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="6ee3b-786">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="6ee3b-786">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="6ee3b-787">リストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-787">The list does not contain duplicate IDs.</span></span> <span data-ttu-id="6ee3b-788">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-788">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="6ee3b-789">さらに、返されたリストには、拡張データ型に適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-789">In addition, the returned list contains any configuration key IDs that are applied to the extended data type.</span></span>

## <a name="method-contains"></a><span data-ttu-id="6ee3b-790">メソッド contains</span><span class="sxs-lookup"><span data-stu-id="6ee3b-790">Method contains</span></span>

<span data-ttu-id="6ee3b-791">フォーム グループ コントロールに指定されたフォーム コントロールが含まれるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-791">Specifies whether a form group control contains a specified form control.</span></span>

```xpp
public boolean contains(FormControl control)
```

### <a name="parameters---contains"></a><span data-ttu-id="6ee3b-792">パラメーター - contains</span><span class="sxs-lookup"><span data-stu-id="6ee3b-792">Parameters - contains</span></span>

<span data-ttu-id="6ee3b-793">control</span><span class="sxs-lookup"><span data-stu-id="6ee3b-793">control</span></span>  
<span data-ttu-id="6ee3b-794">フォーム コントロールを指定する FormControl オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-794">A FormControl object that specifies a form control.</span></span>

### <a name="return-value---contains"></a><span data-ttu-id="6ee3b-795">戻り値 - contains</span><span class="sxs-lookup"><span data-stu-id="6ee3b-795">Return Value - contains</span></span>

<span data-ttu-id="6ee3b-796">フォーム グループ コントロールに指定フォーム コントロールが含まれる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-796">true if a form group control contains the specified form control; otherwise, false.</span></span>

## <a name="method-controlcount"></a><span data-ttu-id="6ee3b-797">メソッド controlCount</span><span class="sxs-lookup"><span data-stu-id="6ee3b-797">Method controlCount</span></span>

<span data-ttu-id="6ee3b-798">フォーム グループ コントロール内のコントロールの数を返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-798">Returns the number of controls in a form group control.</span></span>

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a><span data-ttu-id="6ee3b-799">戻り値 - controlCount</span><span class="sxs-lookup"><span data-stu-id="6ee3b-799">Return Value - controlCount</span></span>

<span data-ttu-id="6ee3b-800">フォーム グループ コントロールのコントロールの数を指定する整数データ型値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-800">An Integer data type value that specifies the number of controls in a form group control.</span></span>

### <a name="remarks---controlcount"></a><span data-ttu-id="6ee3b-801">備考 - controlCount</span><span class="sxs-lookup"><span data-stu-id="6ee3b-801">Remarks - controlCount</span></span>

<span data-ttu-id="6ee3b-802">FormGroupControl.addControl メソッドを使用することにより、フォーム グループ コントロールに対してコントロールを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-802">You can add a control to a form group control by using the FormGroupControl.addControl method.</span></span>

## <a name="method-controlnum"></a><span data-ttu-id="6ee3b-803">メソッド controlNum</span><span class="sxs-lookup"><span data-stu-id="6ee3b-803">Method controlNum</span></span>

<span data-ttu-id="6ee3b-804">フォーム グループ コントロールで指定したコントロールの FormControl オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-804">Returns a FormControl object for a specified control in a form group control.</span></span>

```xpp
public FormControl controlNum(int controlNo)
```

### <a name="parameters---controlnum"></a><span data-ttu-id="6ee3b-805">パラメーター - controlNum</span><span class="sxs-lookup"><span data-stu-id="6ee3b-805">Parameters - controlNum</span></span>

<span data-ttu-id="6ee3b-806">controlNo</span><span class="sxs-lookup"><span data-stu-id="6ee3b-806">controlNo</span></span>  
<span data-ttu-id="6ee3b-807">フォーム グループ コントロール内で管理を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-807">An Integer data type that specifies a control in a form group control.</span></span>

### <a name="return-value---controlnum"></a><span data-ttu-id="6ee3b-808">戻り値 - controlNum</span><span class="sxs-lookup"><span data-stu-id="6ee3b-808">Return Value - controlNum</span></span>

<span data-ttu-id="6ee3b-809">フォーム コントロールに関する情報を変更および提供するために使用できる FormControl オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-809">A FormControl object that can be used to modify and provide information about a form control.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="6ee3b-810">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="6ee3b-810">Method countryRegionCodes</span></span>

<span data-ttu-id="6ee3b-811">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-811">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="6ee3b-812">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="6ee3b-812">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="6ee3b-813">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-813">value</span></span>  
<span data-ttu-id="6ee3b-814">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-814">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="6ee3b-815">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="6ee3b-815">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="6ee3b-816">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-816">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="6ee3b-817">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="6ee3b-817">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="6ee3b-818">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="6ee3b-818">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="6ee3b-819">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-819">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="6ee3b-820">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="6ee3b-820">Return Value - countryRegionContextField</span></span>

## <a name="method-datagroup"></a><span data-ttu-id="6ee3b-821">メソッド dataGroup</span><span class="sxs-lookup"><span data-stu-id="6ee3b-821">Method dataGroup</span></span>

<span data-ttu-id="6ee3b-822">フォーム グループ コントロールのデータのグループを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-822">Sets or returns a data group for a form group control.</span></span>

```xpp
public str dataGroup([str value])
```

### <a name="parameters---datagroup"></a><span data-ttu-id="6ee3b-823">パラメーター - dataGroup</span><span class="sxs-lookup"><span data-stu-id="6ee3b-823">Parameters - dataGroup</span></span>

<span data-ttu-id="6ee3b-824">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-824">value</span></span>  
<span data-ttu-id="6ee3b-825">データ グループを指定する文字列データ型; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-825">A String data type that specifies the data group; optional.</span></span>

### <a name="return-value---datagroup"></a><span data-ttu-id="6ee3b-826">戻り値 - dataGroup</span><span class="sxs-lookup"><span data-stu-id="6ee3b-826">Return Value - dataGroup</span></span>

<span data-ttu-id="6ee3b-827">データ グループを指定する文字列データ型値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-827">A String data type value that specifies the data group.</span></span>

### <a name="remarks---datagroup"></a><span data-ttu-id="6ee3b-828">備考 - dataGroup</span><span class="sxs-lookup"><span data-stu-id="6ee3b-828">Remarks - dataGroup</span></span>

<span data-ttu-id="6ee3b-829">データ グループは、フォームのデータ ソースであるテーブルのフィールド グループに対応します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-829">A data group corresponds to a field group on a table that is a data source for the form.</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="6ee3b-830">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="6ee3b-830">Method dataRelationPath</span></span>

<span data-ttu-id="6ee3b-831">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-831">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="6ee3b-832">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="6ee3b-832">Parameters - dataRelationPath</span></span>

<span data-ttu-id="6ee3b-833">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-833">value</span></span>  
<span data-ttu-id="6ee3b-834">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-834">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="6ee3b-835">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="6ee3b-835">Return Value - dataRelationPath</span></span>

<span data-ttu-id="6ee3b-836">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-836">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="6ee3b-837">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="6ee3b-837">Remarks - dataRelationPath</span></span>

<span data-ttu-id="6ee3b-838">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-838">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="6ee3b-839">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-839">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="6ee3b-840">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="6ee3b-840">Method dataSource</span></span>

<span data-ttu-id="6ee3b-841">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-841">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="6ee3b-842">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="6ee3b-842">Parameters - dataSource</span></span>

<span data-ttu-id="6ee3b-843">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-843">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="6ee3b-844">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="6ee3b-844">Return Value - dataSource</span></span>

<span data-ttu-id="6ee3b-845">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-845">The identifier of the data source that will be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="6ee3b-846">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="6ee3b-846">Method displayTarget</span></span>

<span data-ttu-id="6ee3b-847">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-847">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="6ee3b-848">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="6ee3b-848">Parameters - displayTarget</span></span>

<span data-ttu-id="6ee3b-849">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-849">value</span></span>  
<span data-ttu-id="6ee3b-850">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-850">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="6ee3b-851">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="6ee3b-851">Return Value - displayTarget</span></span>

<span data-ttu-id="6ee3b-852">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-852">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="6ee3b-853">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="6ee3b-853">Method dragDrop</span></span>

<span data-ttu-id="6ee3b-854">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-854">Determines whether drag-and-drop operations are enabled or disabled for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="6ee3b-855">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="6ee3b-855">Parameters - dragDrop</span></span>

<span data-ttu-id="6ee3b-856">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-856">value</span></span>  
<span data-ttu-id="6ee3b-857">ドラッグ アンド ドロップの動作が有効かどうかを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-857">An integer value that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="6ee3b-858">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="6ee3b-858">Return Value - dragDrop</span></span>

<span data-ttu-id="6ee3b-859">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-859">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="6ee3b-860">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="6ee3b-860">Remarks - dragDrop</span></span>

<span data-ttu-id="6ee3b-861">動作を指定するには、FormGroupControl.dragLeave および FormGroupControl.dragOver メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-861">You use the FormGroupControl.dragLeave and FormGroupControl.dragOver methods to specify the behavior.</span></span> <span data-ttu-id="6ee3b-862">値パラメーターに true または false の値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-862">You can pass a value of true or false for the value parameter.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="6ee3b-863">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="6ee3b-863">Method dragOver</span></span>

<span data-ttu-id="6ee3b-864">オブジェクトがフォーム グループ コントロールの境界上にドラッグされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-864">Is called when an object is dragged over the bounds of a form group control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="6ee3b-865">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="6ee3b-865">Parameters - dragOver</span></span>

<span data-ttu-id="6ee3b-866">dragSource</span><span class="sxs-lookup"><span data-stu-id="6ee3b-866">dragSource</span></span>  
<span data-ttu-id="6ee3b-867">オブジェクト位置の y 座標を示す整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-867">An Integer data type that indicates the y-coordinate of the object position.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-868">dragMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-868">dragMode</span></span>  
<span data-ttu-id="6ee3b-869">オブジェクト位置の y 座標を示す整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-869">An Integer data type that indicates the y-coordinate of the object position.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-870">x</span><span class="sxs-lookup"><span data-stu-id="6ee3b-870">x</span></span>  
<span data-ttu-id="6ee3b-871">オブジェクト位置の y 座標を示す整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-871">An Integer data type that indicates the y-coordinate of the object position.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-872">y</span><span class="sxs-lookup"><span data-stu-id="6ee3b-872">y</span></span>  
<span data-ttu-id="6ee3b-873">オブジェクト位置の y 座標を示す整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-873">An Integer data type that indicates the y-coordinate of the object position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="6ee3b-874">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="6ee3b-874">Return Value - dragOver</span></span>

<span data-ttu-id="6ee3b-875">オブジェクトが移動、コピー、または指定された位置に移動されていないかどうかを示す FormDrag システム列挙値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-875">A FormDrag system enumeration value that indicates whether the object is moved, copied, or not moved to a specified position.</span></span>

### <a name="remarks---dragover"></a><span data-ttu-id="6ee3b-876">備考 - dragOver</span><span class="sxs-lookup"><span data-stu-id="6ee3b-876">Remarks - dragOver</span></span>

<span data-ttu-id="6ee3b-877">コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、dragOver をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-877">You can override this method in a form group control by right-clicking the Methods node below the control, clicking Override Method, and then clicking dragOver.</span></span> <span data-ttu-id="6ee3b-878">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-878">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="6ee3b-879">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="6ee3b-879">Method dragOverEx</span></span>

<span data-ttu-id="6ee3b-880">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-880">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="6ee3b-881">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="6ee3b-881">Parameters - dragOverEx</span></span>

<span data-ttu-id="6ee3b-882">dragSource</span><span class="sxs-lookup"><span data-stu-id="6ee3b-882">dragSource</span></span>  
<span data-ttu-id="6ee3b-883">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-883">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-884">dragMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-884">dragMode</span></span>  
<span data-ttu-id="6ee3b-885">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-885">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-886">x</span><span class="sxs-lookup"><span data-stu-id="6ee3b-886">x</span></span>  
<span data-ttu-id="6ee3b-887">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-887">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-888">y</span><span class="sxs-lookup"><span data-stu-id="6ee3b-888">y</span></span>  
<span data-ttu-id="6ee3b-889">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-889">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="6ee3b-890">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="6ee3b-890">Return Value - dragOverEx</span></span>

<span data-ttu-id="6ee3b-891">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-891">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="6ee3b-892">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="6ee3b-892">Method dragText</span></span>

<span data-ttu-id="6ee3b-893">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-893">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="6ee3b-894">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="6ee3b-894">Return Value - dragText</span></span>

<span data-ttu-id="6ee3b-895">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-895">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enablechilds"></a><span data-ttu-id="6ee3b-896">メソッド enableChilds</span><span class="sxs-lookup"><span data-stu-id="6ee3b-896">Method enableChilds</span></span>

<span data-ttu-id="6ee3b-897">フォーム グループ コントロールの子コントロールが有効かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-897">Specifies whether the child controls are enabled for a form group control.</span></span>

```xpp
public boolean enableChilds([boolean enable])
```

### <a name="parameters---enablechilds"></a><span data-ttu-id="6ee3b-898">パラメーター - enableChilds</span><span class="sxs-lookup"><span data-stu-id="6ee3b-898">Parameters - enableChilds</span></span>

<span data-ttu-id="6ee3b-899">enable</span><span class="sxs-lookup"><span data-stu-id="6ee3b-899">enable</span></span>  
<span data-ttu-id="6ee3b-900">子コントロールが有効かどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-900">A Boolean value that indicates whether the child controls are enabled; optional.</span></span>

### <a name="return-value---enablechilds"></a><span data-ttu-id="6ee3b-901">戻り値 - enableChilds</span><span class="sxs-lookup"><span data-stu-id="6ee3b-901">Return Value - enableChilds</span></span>

<span data-ttu-id="6ee3b-902">子コントロールが有効にされた場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-902">true if the child controls are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="6ee3b-903">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="6ee3b-903">Method enabled</span></span>

<span data-ttu-id="6ee3b-904">オブジェクトが有効か無効かを決定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-904">Determines whether the object is enabled or disabled.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="6ee3b-905">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="6ee3b-905">Parameters - enabled</span></span>

<span data-ttu-id="6ee3b-906">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-906">value</span></span>  
<span data-ttu-id="6ee3b-907">フォーム グループ コントロールが有効かどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-907">A Boolean value that indicates whether a form group control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="6ee3b-908">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="6ee3b-908">Return Value - enabled</span></span>

<span data-ttu-id="6ee3b-909">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-909">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="6ee3b-910">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="6ee3b-910">Remarks - enabled</span></span>

<span data-ttu-id="6ee3b-911">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-911">The enabled property lets you enable or disable controls at run time.</span></span> <span data-ttu-id="6ee3b-912">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-912">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="6ee3b-913">また、読み取り専用情報を提供するエラー メッセージなど、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-913">You can also disable a control that is used only for display purposes, such as an error message that provides read-only information.</span></span>

## <a name="method-expand"></a><span data-ttu-id="6ee3b-914">メソッド expand</span><span class="sxs-lookup"><span data-stu-id="6ee3b-914">Method expand</span></span>

<span data-ttu-id="6ee3b-915">フォーム グループ コントロールが展開されているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-915">Specifies whether a form group control is expanded.</span></span>

```xpp
public boolean expand([boolean expand])
```

### <a name="parameters---expand"></a><span data-ttu-id="6ee3b-916">パラメーター - expand</span><span class="sxs-lookup"><span data-stu-id="6ee3b-916">Parameters - expand</span></span>

<span data-ttu-id="6ee3b-917">expand</span><span class="sxs-lookup"><span data-stu-id="6ee3b-917">expand</span></span>  
<span data-ttu-id="6ee3b-918">フォーム グループ コントロールが展開されているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-918">A Boolean value that indicates whether a form group control is expanded; optional.</span></span>

### <a name="return-value---expand"></a><span data-ttu-id="6ee3b-919">戻り値 - expand</span><span class="sxs-lookup"><span data-stu-id="6ee3b-919">Return Value - expand</span></span>

<span data-ttu-id="6ee3b-920">フォーム グループ コントロールが拡張されている場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-920">true if a form group control is expanded; otherwise, false.</span></span>

## <a name="method-font"></a><span data-ttu-id="6ee3b-921">メソッド font</span><span class="sxs-lookup"><span data-stu-id="6ee3b-921">Method font</span></span>

<span data-ttu-id="6ee3b-922">コントロール内のテキストに使用されるフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-922">Gets or sets the name of the font that is used for text in a control.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="6ee3b-923">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="6ee3b-923">Parameters - font</span></span>

<span data-ttu-id="6ee3b-924">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-924">value</span></span>  
<span data-ttu-id="6ee3b-925">フォーム グループ コントロール内のテキストのフォントを示す文字列データ型; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-925">A String data type that indicates the font for text in a form group control; optional.</span></span>

### <a name="return-value---font"></a><span data-ttu-id="6ee3b-926">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="6ee3b-926">Return Value - font</span></span>

<span data-ttu-id="6ee3b-927">Tahoma や Verdana など、使用されるべきフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-927">The name of the font that should be used, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="6ee3b-928">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="6ee3b-928">Method fontSize</span></span>

<span data-ttu-id="6ee3b-929">コントロール内のテキストに使用するフォント サイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-929">Gets or sets the font size to use for text in a control.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="6ee3b-930">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="6ee3b-930">Parameters - fontSize</span></span>

<span data-ttu-id="6ee3b-931">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-931">value</span></span>  
<span data-ttu-id="6ee3b-932">フォーム グループ コントロール内のテキストのフォント サイズをポイントで示す整数値。 オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-932">An integer value that indicates the font size in points for text in a form group control; optional.</span></span>

### <a name="return-value---fontsize"></a><span data-ttu-id="6ee3b-933">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="6ee3b-933">Return Value - fontSize</span></span>

<span data-ttu-id="6ee3b-934">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-934">The height of the font in points.</span></span>

## <a name="method-frameoptionbutton"></a><span data-ttu-id="6ee3b-935">メソッド frameOptionButton</span><span class="sxs-lookup"><span data-stu-id="6ee3b-935">Method frameOptionButton</span></span>

<span data-ttu-id="6ee3b-936">フォーム グループ コントロールのオプション ボタンを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-936">Sets or returns the option button for a form group control.</span></span>

```xpp
public int frameOptionButton([int value])
```

### <a name="parameters---frameoptionbutton"></a><span data-ttu-id="6ee3b-937">パラメーター - frameOptionButton</span><span class="sxs-lookup"><span data-stu-id="6ee3b-937">Parameters - frameOptionButton</span></span>

<span data-ttu-id="6ee3b-938">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-938">value</span></span>  
<span data-ttu-id="6ee3b-939">オプション ボタンのタイプを指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-939">An Integer data type that specifies the type of option button; optional.</span></span>

### <a name="return-value---frameoptionbutton"></a><span data-ttu-id="6ee3b-940">戻り値 - frameOptionButton</span><span class="sxs-lookup"><span data-stu-id="6ee3b-940">Return Value - frameOptionButton</span></span>

<span data-ttu-id="6ee3b-941">オプション ボタンのタイプを指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-941">An integer value that specifies the type of option button.</span></span>

### <a name="remarks---frameoptionbutton"></a><span data-ttu-id="6ee3b-942">備考 - frameOptionButton</span><span class="sxs-lookup"><span data-stu-id="6ee3b-942">Remarks - frameOptionButton</span></span>

<span data-ttu-id="6ee3b-943">値パラメーターのために FormFrameOptionButton 列挙型値を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-943">You can use a FormFrameOptionButton enumeration value for the value parameter.</span></span>

## <a name="method-frameposition"></a><span data-ttu-id="6ee3b-944">メソッド framePosition</span><span class="sxs-lookup"><span data-stu-id="6ee3b-944">Method framePosition</span></span>

<span data-ttu-id="6ee3b-945">フォーム グループ コントロールのフレームの位置を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-945">Sets or returns the location of the frame for a form group control.</span></span>

```xpp
public int framePosition([int value])
```

### <a name="parameters---frameposition"></a><span data-ttu-id="6ee3b-946">パラメーター - framePosition</span><span class="sxs-lookup"><span data-stu-id="6ee3b-946">Parameters - framePosition</span></span>

<span data-ttu-id="6ee3b-947">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-947">value</span></span>  
<span data-ttu-id="6ee3b-948">フレームの場所を指定する整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-948">An integer value that specifies the location of the frame; optional.</span></span>

### <a name="return-value---frameposition"></a><span data-ttu-id="6ee3b-949">戻り値 - framePosition</span><span class="sxs-lookup"><span data-stu-id="6ee3b-949">Return Value - framePosition</span></span>

<span data-ttu-id="6ee3b-950">フレームの場所を指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-950">An integer value that specifies the location of the frame.</span></span>

## <a name="method-frametype"></a><span data-ttu-id="6ee3b-951">メソッド frameType</span><span class="sxs-lookup"><span data-stu-id="6ee3b-951">Method frameType</span></span>

<span data-ttu-id="6ee3b-952">フォーム グループ コントロールのフレーム スタイルを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-952">Sets or returns the frame style for a form group control.</span></span>

```xpp
public int frameType([int value])
```

### <a name="parameters---frametype"></a><span data-ttu-id="6ee3b-953">パラメーター - frameType</span><span class="sxs-lookup"><span data-stu-id="6ee3b-953">Parameters - frameType</span></span>

<span data-ttu-id="6ee3b-954">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-954">value</span></span>  
<span data-ttu-id="6ee3b-955">フォーム グループ コントロールのフレーム スタイルを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-955">An integer value that indicates the frame style for a form group control; optional.</span></span>

### <a name="return-value---frametype"></a><span data-ttu-id="6ee3b-956">戻り値 - frameType</span><span class="sxs-lookup"><span data-stu-id="6ee3b-956">Return Value - frameType</span></span>

<span data-ttu-id="6ee3b-957">フォーム グループ コントロールのフレーム スタイルを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-957">An integer value that indicates the frame style for a form group control.</span></span>

### <a name="remarks---frametype"></a><span data-ttu-id="6ee3b-958">備考 - frameType</span><span class="sxs-lookup"><span data-stu-id="6ee3b-958">Remarks - frameType</span></span>

<span data-ttu-id="6ee3b-959">値パラメーターのために FormFrameType 列挙型値を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-959">You can use a FormFrameType enumeration value for the value parameter.</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="6ee3b-960">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="6ee3b-960">Method hasChanged</span></span>

<span data-ttu-id="6ee3b-961">フォーム グループ コントロールの内容が変更されたかどうかを示すブール値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-961">Sets or returns a Boolean value that indicates whether the contents of a form group control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="6ee3b-962">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="6ee3b-962">Parameters - hasChanged</span></span>

<span data-ttu-id="6ee3b-963">val</span><span class="sxs-lookup"><span data-stu-id="6ee3b-963">val</span></span>  
<span data-ttu-id="6ee3b-964">フォーム グループ コントロールの内容が変更されたかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-964">A Boolean value that indicates whether the contents of a form group control have changed; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="6ee3b-965">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="6ee3b-965">Return Value - hasChanged</span></span>

<span data-ttu-id="6ee3b-966">内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-966">true if the contents have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="6ee3b-967">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="6ee3b-967">Method hasUserSetting</span></span>

<span data-ttu-id="6ee3b-968">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-968">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="6ee3b-969">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="6ee3b-969">Return Value - hasUserSetting</span></span>

<span data-ttu-id="6ee3b-970">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-970">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="6ee3b-971">メソッド height</span><span class="sxs-lookup"><span data-stu-id="6ee3b-971">Method height</span></span>

<span data-ttu-id="6ee3b-972">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-972">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="6ee3b-973">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="6ee3b-973">Parameters - height</span></span>

<span data-ttu-id="6ee3b-974">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-974">value</span></span>  
<span data-ttu-id="6ee3b-975">高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-975">An integer value that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-976">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-976">mode</span></span>  
<span data-ttu-id="6ee3b-977">高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-977">An integer value that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="6ee3b-978">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="6ee3b-978">Return Value - height</span></span>

<span data-ttu-id="6ee3b-979">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-979">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="6ee3b-980">備考 - height</span><span class="sxs-lookup"><span data-stu-id="6ee3b-980">Remarks - height</span></span>

<span data-ttu-id="6ee3b-981">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-981">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="6ee3b-982">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-982">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="6ee3b-983">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-983">Mode</span></span>              | <span data-ttu-id="6ee3b-984">高さの計算</span><span class="sxs-lookup"><span data-stu-id="6ee3b-984">Height calculation</span></span>                                                                         |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee3b-985">-1 � 正確</span><span class="sxs-lookup"><span data-stu-id="6ee3b-985">-1 � Exact</span></span>        | <span data-ttu-id="6ee3b-986">ピクセル単位のコントロールの正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-986">The exact height of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="6ee3b-987">0 � 自動</span><span class="sxs-lookup"><span data-stu-id="6ee3b-987">0 � Auto</span></span>          | <span data-ttu-id="6ee3b-988">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-988">The height of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6ee3b-989">1 � 列の高さ</span><span class="sxs-lookup"><span data-stu-id="6ee3b-989">1 � Column height</span></span> | <span data-ttu-id="6ee3b-990">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-990">The layout of the form determines the height of the control.</span></span>                               |

<span data-ttu-id="6ee3b-991">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-991">The height and the height calculation mode can be set separately.</span></span>

### <a name="examples---height"></a><span data-ttu-id="6ee3b-992">例 - height</span><span class="sxs-lookup"><span data-stu-id="6ee3b-992">Examples - height</span></span>

<span data-ttu-id="6ee3b-993">次の例は、コントロールの高さを 120 ピクセルに設定する height メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-993">The following example shows a call to the height method to the set the control height to 120 pixels.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildStringControl formBuildStringControl; 
    FormBuildGroupControl formBuildGroupControl; 
    FormGroupControl formGroupControl; 
    int idx; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add controls. 
    formBuildGroupControl = 
 formBuildDesign.addControl(FormControlType::Group,"Group"); 
    idx = formBuildGroupControl.id(); 
    formBuildStringControl = 
 formBuildGroupControl.addControl(FormControlType::String,"String"); 
    // Add data fields to the controls. 
    formBuildGroupControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataField(2); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formGroupControl = formRun.control(idx); 
    formGroupControl.height(120, -1); 
}
```

## <a name="method-heightmode"></a><span data-ttu-id="6ee3b-994">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-994">Method heightMode</span></span>

<span data-ttu-id="6ee3b-995">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-995">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="6ee3b-996">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-996">Parameters - heightMode</span></span>

<span data-ttu-id="6ee3b-997">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-997">value</span></span>  
<span data-ttu-id="6ee3b-998">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-998">An integer value that indicates how the height of the control is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="6ee3b-999">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-999">Return Value - heightMode</span></span>

<span data-ttu-id="6ee3b-1000">計算モード。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1000">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="6ee3b-1001">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1001">Remarks - heightMode</span></span>

<span data-ttu-id="6ee3b-1002">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1002">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="6ee3b-1003">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1003">Mode</span></span>          | <span data-ttu-id="6ee3b-1004">高さの計算</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1004">Height calculation</span></span>                                                                         |
|---------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee3b-1005">正確</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1005">Exact</span></span>         | <span data-ttu-id="6ee3b-1006">ピクセル単位のコントロールの正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1006">The exact height of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="6ee3b-1007">自動</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1007">Auto</span></span>          | <span data-ttu-id="6ee3b-1008">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1008">The height of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6ee3b-1009">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1009">Column height</span></span> | <span data-ttu-id="6ee3b-1010">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1010">The layout of the form determines the height of the control.</span></span>                               |

<span data-ttu-id="6ee3b-1011">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1011">The height of the control might change when the calculation mode is set to Auto or Column height.</span></span>

### <a name="examples---heightmode"></a><span data-ttu-id="6ee3b-1012">例 - heightMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1012">Examples - heightMode</span></span>

<span data-ttu-id="6ee3b-1013">次の例は、正確なピクセル値に基づいてコントロールの高さを調整する heightMode メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1013">The following example shows a call to the heightMode method to adjust the control height, based on an exact pixel value.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildStringControl formBuildStringControl; 
    FormBuildGroupControl formBuildGroupControl; 
    FormGroupControl formGroupControl; 
    int idx; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add controls. 
    formBuildGroupControl = 
 formBuildDesign.addControl(FormControlType::Group,"Group"); 
    idx = formBuildGroupControl.id(); 
    formBuildStringControl = 
 formBuildGroupControl.addControl(FormControlType::String,"String"); 
    // Add data fields to the controls. 
    formBuildGroupControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataField(2); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formGroupControl = formRun.control(idx); 
    formGroupControl.heightMode(-1); 
    formGroupControl.heightValue(120); 
}
```

## <a name="method-heightvalue"></a><span data-ttu-id="6ee3b-1014">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1014">Method heightValue</span></span>

<span data-ttu-id="6ee3b-1015">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1015">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="6ee3b-1016">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1016">Parameters - heightValue</span></span>

<span data-ttu-id="6ee3b-1017">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1017">value</span></span>  
<span data-ttu-id="6ee3b-1018">高さをピクセル単位で指定する整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1018">An integer value that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="6ee3b-1019">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1019">Return Value - heightValue</span></span>

<span data-ttu-id="6ee3b-1020">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1020">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="6ee3b-1021">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1021">Remarks - heightValue</span></span>

<span data-ttu-id="6ee3b-1022">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1022">The height of the control is not changed unless the Exact height calculation mode is used.</span></span>

### <a name="examples---heightvalue"></a><span data-ttu-id="6ee3b-1023">例 - heightValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1023">Examples - heightValue</span></span>

<span data-ttu-id="6ee3b-1024">次の例は、高さを 5 ピクセルに設定する heightValue メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1024">The following example shows a call to the heightValue method that sets the height to 5 pixels.</span></span>

```xpp
static void createForm(Args _args) 
{ 
   Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildStringControl formBuildStringControl; 
    FormBuildGroupControl formBuildGroupControl; 
    FormGroupControl formGroupControl; 
    int idx; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add controls. 
    formBuildGroupControl = 
 formBuildDesign.addControl(FormControlType::Group,"Group"); 
    idx = formBuildGroupControl.id(); 
    formBuildStringControl = 
 formBuildGroupControl.addControl(FormControlType::String,"String"); 
    // Add data fields to the controls. 
    formBuildGroupControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataField(2); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formGroupControl = formRun.control(idx); 
    formGroupControl.heightMode(-1); 
    formGroupControl.heightValue(120); 
}
```

## <a name="method-helpfield"></a><span data-ttu-id="6ee3b-1025">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1025">Method helpField</span></span>

<span data-ttu-id="6ee3b-1026">フォーム グループ コントロールが選択されている場合にステータス バーに表示されるヘルプ テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1026">Returns the Help text that is displayed in the status bar when a form group control is selected.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="6ee3b-1027">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1027">Return Value - helpField</span></span>

<span data-ttu-id="6ee3b-1028">ヘルプ テキストを含む文字列データ型値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1028">A String data type value that contains the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="6ee3b-1029">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1029">Method helpText</span></span>

<span data-ttu-id="6ee3b-1030">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1030">Gets or sets the Help text that is displayed at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="6ee3b-1031">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1031">Parameters - helpText</span></span>

<span data-ttu-id="6ee3b-1032">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1032">value</span></span>  
<span data-ttu-id="6ee3b-1033">ヘルプ テキストを含む文字列データ型値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1033">A String data type value that contains the Help text.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="6ee3b-1034">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1034">Return Value - helpText</span></span>

<span data-ttu-id="6ee3b-1035">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1035">The string that should be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="6ee3b-1036">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1036">Remarks - helpText</span></span>

<span data-ttu-id="6ee3b-1037">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1037">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="6ee3b-1038">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1038">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="6ee3b-1039">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1039">Method hideIfEmpty</span></span>

<span data-ttu-id="6ee3b-1040">グループ内のコントロールが表示されないときフォーム グループ コントロールを表示するかどうかを示すブール値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1040">Sets or gets a Boolean value that indicates whether a form group control is visible when the controls in the group are not visible.</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="6ee3b-1041">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1041">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="6ee3b-1042">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1042">value</span></span>  
<span data-ttu-id="6ee3b-1043">フォーム グループ コントロールが表示されているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1043">A Boolean value that indicates whether a form group control is visible; optional.</span></span>

### <a name="return-value---hideifempty"></a><span data-ttu-id="6ee3b-1044">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1044">Return Value - hideIfEmpty</span></span>

<span data-ttu-id="6ee3b-1045">フォーム グループ コントロールが表示されない場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1045">true if the form group control is not visible; otherwise, false.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="6ee3b-1046">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1046">Method hierarchyParent</span></span>

<span data-ttu-id="6ee3b-1047">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1047">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="6ee3b-1048">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1048">Parameters - hierarchyParent</span></span>

<span data-ttu-id="6ee3b-1049">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1049">value</span></span>  
<span data-ttu-id="6ee3b-1050">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1050">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="6ee3b-1051">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1051">Return Value - hierarchyParent</span></span>

<span data-ttu-id="6ee3b-1052">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1052">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="6ee3b-1053">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1053">Method hWnd</span></span>

<span data-ttu-id="6ee3b-1054">フォーム グループ コントロールのハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1054">Returns a handle for a form group control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="6ee3b-1055">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1055">Return Value - hWnd</span></span>

<span data-ttu-id="6ee3b-1056">ハンドルを指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1056">An integer value that specifies the handle.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="6ee3b-1057">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1057">Method isContainer</span></span>

<span data-ttu-id="6ee3b-1058">フォーム グループ コントロールがコンテナーであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1058">Indicates whether a form group control is a container.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="6ee3b-1059">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1059">Return Value - isContainer</span></span>

<span data-ttu-id="6ee3b-1060">フォーム グループ コントロールがコンテナーである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1060">true if a form group control is a container; otherwise, false.</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="6ee3b-1061">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1061">Method isDisplayed</span></span>

<span data-ttu-id="6ee3b-1062">フォーム グループ コントロールが表示されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1062">Indicates whether a form group control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="6ee3b-1063">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1063">Return Value - isDisplayed</span></span>

<span data-ttu-id="6ee3b-1064">フォーム グループ コントロールが表示されている場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1064">true if a form group is displayed; otherwise, false.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="6ee3b-1065">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1065">Method isRestricted</span></span>

<span data-ttu-id="6ee3b-1066">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1066">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="6ee3b-1067">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1067">Return Value - isRestricted</span></span>

<span data-ttu-id="6ee3b-1068">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1068">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="6ee3b-1069">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1069">Method isUserSetupEnabled</span></span>

<span data-ttu-id="6ee3b-1070">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1070">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="6ee3b-1071">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1071">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="6ee3b-1072">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1072">neededSetupRights</span></span>  
<span data-ttu-id="6ee3b-1073">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1073">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="6ee3b-1074">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1074">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="6ee3b-1075">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1075">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span> <span data-ttu-id="6ee3b-1076">「true」を返すこのメソッドについては、デザインおよびすべての親コンテナの AllowUserSetup プロパティが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1076">For this method to return true, the AllowUserSetup property for the design and for all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="6ee3b-1077">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1077">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="6ee3b-1078">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1078">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee3b-1079">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1079">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="6ee3b-1080">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1080">No changes can be made to the control.</span></span> <span data-ttu-id="6ee3b-1081">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1081">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="6ee3b-1082">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1082">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="6ee3b-1083">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1083">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="6ee3b-1084">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1084">The user cannot move the control.</span></span>   |
| <span data-ttu-id="6ee3b-1085">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1085">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="6ee3b-1086">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1086">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="6ee3b-1087">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1087">The user can also move the control.</span></span> |

### <a name="examples---isusersetupenabled"></a><span data-ttu-id="6ee3b-1088">例 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1088">Examples - isUserSetupEnabled</span></span>

<span data-ttu-id="6ee3b-1089">次の例は、コントロールのユーザー設定権限を決定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1089">The following example shows how to determine the user setup rights for a control.</span></span>

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

## <a name="method-italic"></a><span data-ttu-id="6ee3b-1090">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1090">Method italic</span></span>

<span data-ttu-id="6ee3b-1091">フォーム グループ コントロールのテキストが斜体であるかどうかを示すブール値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1091">Sets or returns a Boolean value that indicates whether the text for a form group control is italic.</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="6ee3b-1092">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1092">Parameters - italic</span></span>

<span data-ttu-id="6ee3b-1093">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1093">value</span></span>  
<span data-ttu-id="6ee3b-1094">フォーム グループ コントロールのテキストが斜体であるかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1094">A Boolean value that indicates whether the text for a form group control is italic; optional.</span></span>

### <a name="return-value---italic"></a><span data-ttu-id="6ee3b-1095">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1095">Return Value - italic</span></span>

<span data-ttu-id="6ee3b-1096">テキストが斜体である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1096">true if the text is italic; otherwise, false.</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="6ee3b-1097">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1097">Method labelBold</span></span>

<span data-ttu-id="6ee3b-1098">フォーム グループ コントロールのラベル テキストのフォントの太さを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1098">Sets or returns the font weight of the label text for a form group control.</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="6ee3b-1099">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1099">Parameters - labelBold</span></span>

<span data-ttu-id="6ee3b-1100">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1100">value</span></span>  
<span data-ttu-id="6ee3b-1101">ラベル テキストのフォントの太さを指定する整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1101">An integer value that specifies the font weight of the label text; optional.</span></span>

### <a name="return-value---labelbold"></a><span data-ttu-id="6ee3b-1102">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1102">Return Value - labelBold</span></span>

<span data-ttu-id="6ee3b-1103">ラベル テキストのフォントの太さを指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1103">An integer value that specifies the font weight of the label text.</span></span>

### <a name="remarks---labelbold"></a><span data-ttu-id="6ee3b-1104">備考 - labelBold</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1104">Remarks - labelBold</span></span>

<span data-ttu-id="6ee3b-1105">値パラメーターおよび戻り値の使用可能な値の詳細については、太字のメソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1105">For more information about possible values for the value parameter and return value, see the bold method.</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="6ee3b-1106">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1106">Method labelCharacterSet</span></span>

<span data-ttu-id="6ee3b-1107">フォーム グループ コントロールのラベル テキストのフォントの文字セットを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1107">Sets or returns the character set of the font for the label text for a form group control.</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="6ee3b-1108">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1108">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="6ee3b-1109">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1109">value</span></span>  
<span data-ttu-id="6ee3b-1110">ラベル テキストのフォントの文字セットを指定する整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1110">An integer value that specifies the character set of the font for the label text; optional.</span></span>

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="6ee3b-1111">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1111">Return Value - labelCharacterSet</span></span>

<span data-ttu-id="6ee3b-1112">ラベル テキストのフォントの文字セットを指定する整数データ型値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1112">An Integer data type value that specifies the character set of the font for the label text.</span></span>

### <a name="remarks---labelcharacterset"></a><span data-ttu-id="6ee3b-1113">備考 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1113">Remarks - labelCharacterSet</span></span>

<span data-ttu-id="6ee3b-1114">文字セットは、共通の関係を持つアルファベット、数字、およびその他の文字のグループです。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1114">A character set is a group of alphabetical, numeric, and other characters that have some relationship in common.</span></span> <span data-ttu-id="6ee3b-1115">たとえば、特定の国/地域または言語に対して文字セットを使用する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1115">For example, a character set might be used for a specific country/region or language.</span></span> <span data-ttu-id="6ee3b-1116">値パラメーターの可能な値の一覧については、characterSet メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1116">For a list of possible values for the value parameter, see the characterSet method.</span></span> <span data-ttu-id="6ee3b-1117">可能な戻り値の一覧については、characterSet メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1117">For a list of possible return values, see the characterSet method.</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="6ee3b-1118">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1118">Method labelFont</span></span>

<span data-ttu-id="6ee3b-1119">フォーム グループ コントロールのラベル テキストのフォントを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1119">Sets or returns the font for the label text for a form group control.</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="6ee3b-1120">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1120">Parameters - labelFont</span></span>

<span data-ttu-id="6ee3b-1121">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1121">value</span></span>  
<span data-ttu-id="6ee3b-1122">ラベル テキストのフォントを指定する文字列データ型; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1122">A String data type that specifies the font for the label text; optional.</span></span>

### <a name="return-value---labelfont"></a><span data-ttu-id="6ee3b-1123">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1123">Return Value - labelFont</span></span>

<span data-ttu-id="6ee3b-1124">ラベル テキストのフォントを指定する文字列データ型値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1124">A String data type value that specifies the font for the label text.</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="6ee3b-1125">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1125">Method labelFontSize</span></span>

<span data-ttu-id="6ee3b-1126">フォーム グループ コントロールのラベル テキストのフォント サイズを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1126">Sets or returns the font size of the label text for a form group control.</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="6ee3b-1127">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1127">Parameters - labelFontSize</span></span>

<span data-ttu-id="6ee3b-1128">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1128">value</span></span>  
<span data-ttu-id="6ee3b-1129">ラベル テキストのフォント サイズを指定する整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1129">An integer value that specifies the font size of the label text; optional.</span></span>

### <a name="return-value---labelfontsize"></a><span data-ttu-id="6ee3b-1130">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1130">Return Value - labelFontSize</span></span>

<span data-ttu-id="6ee3b-1131">ラベル テキストのフォント サイズを指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1131">An integer value that specifies the font size of the label text.</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="6ee3b-1132">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1132">Method labelItalic</span></span>

<span data-ttu-id="6ee3b-1133">フォーム グループ コントロールのラベル テキストが斜体であるかどうかを示すブール値データ型を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1133">Sets or returns a Boolean data type that indicates whether the label text for a form group control is italic.</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="6ee3b-1134">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1134">Parameters - labelItalic</span></span>

<span data-ttu-id="6ee3b-1135">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1135">value</span></span>  
<span data-ttu-id="6ee3b-1136">ラベル テキストが斜体かどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1136">A Boolean value that indicates whether the label text is italic; optional.</span></span>

### <a name="return-value---labelitalic"></a><span data-ttu-id="6ee3b-1137">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1137">Return Value - labelItalic</span></span>

<span data-ttu-id="6ee3b-1138">ラベル テキストが斜体である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1138">true if the label text is italic; otherwise, false.</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="6ee3b-1139">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1139">Method labelUnderline</span></span>

<span data-ttu-id="6ee3b-1140">フォーム グループ コントロールのラベル テキストが下線付きであるかどうかを示すブール値データ型を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1140">Sets or returns a Boolean data type that indicates whether the label text for a form group control is underlined.</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="6ee3b-1141">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1141">Parameters - labelUnderline</span></span>

<span data-ttu-id="6ee3b-1142">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1142">value</span></span>  
<span data-ttu-id="6ee3b-1143">ラベル テキストに下線が引かれているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1143">A Boolean value that indicates whether the label text is underlined; optional.</span></span>

### <a name="return-value---labelunderline"></a><span data-ttu-id="6ee3b-1144">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1144">Return Value - labelUnderline</span></span>

<span data-ttu-id="6ee3b-1145">ラベル テキストが下線付きである場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1145">true if the label text is underlined; otherwise, false.</span></span>

## <a name="method-leave"></a><span data-ttu-id="6ee3b-1146">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1146">Method leave</span></span>

<span data-ttu-id="6ee3b-1147">ユーザーがマウス ポインターをフォーム グループ コントロールから離すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1147">Is called when the user moves the mouse pointer out of a form group control.</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="6ee3b-1148">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1148">Return Value - leave</span></span>

<span data-ttu-id="6ee3b-1149">マウス ポインターがフォーム グループ コントロールの外に移動する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1149">true if the mouse pointer is moved out of a form group control; otherwise, false.</span></span>

### <a name="remarks---leave"></a><span data-ttu-id="6ee3b-1150">備考 - leave</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1150">Remarks - leave</span></span>

<span data-ttu-id="6ee3b-1151">コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、leave をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1151">You can override this method in a form group control by right-clicking the Methods node below the control, clicking Override Method, and then clicking leave.</span></span> <span data-ttu-id="6ee3b-1152">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1152">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-left"></a><span data-ttu-id="6ee3b-1153">メソッド left</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1153">Method left</span></span>

<span data-ttu-id="6ee3b-1154">フォーム グループ コントロールの水平位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1154">Sets or returns the horizontal position of a form group control in pixels and specifies how the position is calculated.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="6ee3b-1155">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1155">Parameters - left</span></span>

<span data-ttu-id="6ee3b-1156">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1156">value</span></span>  
<span data-ttu-id="6ee3b-1157">位置の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1157">An integer value that indicates how the position is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1158">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1158">mode</span></span>  
<span data-ttu-id="6ee3b-1159">位置の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1159">An integer value that indicates how the position is calculated; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="6ee3b-1160">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1160">Return Value - left</span></span>

<span data-ttu-id="6ee3b-1161">フォーム グループ コントロールの水平位置をピクセル単位で示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1161">An integer value that indicates the horizontal position of a form group control in pixels.</span></span>

### <a name="remarks---left"></a><span data-ttu-id="6ee3b-1162">備考 - left</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1162">Remarks - left</span></span>

<span data-ttu-id="6ee3b-1163">mode パラメーターは、次の値のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1163">The mode parameter can be one of the following values:</span></span>

-   <span data-ttu-id="6ee3b-1164">-1 (既定) � 値パラメーターの値が正確に使用される Exact モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1164">-1 (default) � Use Exact mode, where the value of the value parameter is used exactly.</span></span>
-   <span data-ttu-id="6ee3b-1165">FormLeft 列挙値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1165">A FormLeft enumeration value.</span></span>

### <a name="examples---left"></a><span data-ttu-id="6ee3b-1166">例 - left</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1166">Examples - left</span></span>

<span data-ttu-id="6ee3b-1167">次の例は、水平方向の位置を 50 ピクセルに設定する left メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1167">The following example shows a call to the left method that sets the horizontal position to 50 pixels.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildStringControl formBuildStringControl; 
    FormBuildGroupControl formBuildGroupControl; 
    FormGroupControl formGroupControl; 
    int idx; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add controls. 
    formBuildGroupControl = 
 formBuildDesign.addControl(FormControlType::Group,"Group"); 
    idx = formBuildGroupControl.id(); 
    formBuildStringControl = 
 formBuildGroupControl.addControl(FormControlType::String,"String"); 
    // Add data fields to the controls. 
    formBuildGroupControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataField(2); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formGroupControl = formRun.control(idx); 
    formGroupControl.left(50,-1); 
}
```

## <a name="method-leftmargin"></a><span data-ttu-id="6ee3b-1168">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1168">Method leftMargin</span></span>

<span data-ttu-id="6ee3b-1169">フォーム グループ コントロールの左余白のサイズをピクセル単位で設定するか返し、サイズが自動的に調整されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1169">Sets or returns the size of the left margin for a form group control in pixels and specifies whether the size is automatically adjusted.</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="6ee3b-1170">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1170">Parameters - leftMargin</span></span>

<span data-ttu-id="6ee3b-1171">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1171">value</span></span>  
<span data-ttu-id="6ee3b-1172">左余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1172">An AutoMode enumeration value that specifies whether the size of the left margin is fixed, or whether it is automatically adjusted based on other form property settings; optional.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1173">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1173">mode</span></span>  
<span data-ttu-id="6ee3b-1174">左余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1174">An AutoMode enumeration value that specifies whether the size of the left margin is fixed, or whether it is automatically adjusted based on other form property settings; optional.</span></span>

### <a name="return-value---leftmargin"></a><span data-ttu-id="6ee3b-1175">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1175">Return Value - leftMargin</span></span>

<span data-ttu-id="6ee3b-1176">フォーム グループ コントロールの左余白のサイズをピクセル単位で指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1176">An integer value that specifies the size of the left margin for a form group control in pixels.</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="6ee3b-1177">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1177">Method leftMarginMode</span></span>

<span data-ttu-id="6ee3b-1178">フォーム グループ コントロールの左余白のサイズが固定されているかどうか、またはフォーム プロパティ設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1178">Sets or returns a value that indicates whether the size of the left margin for a form group control is fixed, or whether it is automatically adjusted based on other form property settings.</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="6ee3b-1179">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1179">Parameters - leftMarginMode</span></span>

<span data-ttu-id="6ee3b-1180">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1180">mode</span></span>  
<span data-ttu-id="6ee3b-1181">左余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1181">An AutoMode enumeration value that specifies whether the size of the left margin is fixed, or whether it is automatically adjusted based on other form property settings; optional.</span></span>

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="6ee3b-1182">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1182">Return Value - leftMarginMode</span></span>

<span data-ttu-id="6ee3b-1183">左余白のサイズが自動的に調整される場合は Automode::Auto、それ以外の場合は Automode::Fixed となります。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1183">Automode::Auto if the size of the left margin is automatically adjusted; otherwise, Automode::Fixed.</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="6ee3b-1184">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1184">Method leftMarginValue</span></span>

<span data-ttu-id="6ee3b-1185">フォーム グループ コントロールの左余白のサイズをピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1185">Sets or returns the size of the left margin for a form group control in pixels.</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="6ee3b-1186">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1186">Parameters - leftMarginValue</span></span>

<span data-ttu-id="6ee3b-1187">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1187">value</span></span>  
<span data-ttu-id="6ee3b-1188">フォーム グループ コントロールの左余白のサイズをピクセル単位で指定する整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1188">An integer value that specifies the size of the left margin for a form group control in pixels; optional.</span></span>

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="6ee3b-1189">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1189">Return Value - leftMarginValue</span></span>

<span data-ttu-id="6ee3b-1190">フォーム グループ コントロールの左余白のサイズをピクセル単位で指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1190">An integer value that specifies the size of the left margin for a form group control in pixels.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="6ee3b-1191">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1191">Method leftMode</span></span>

<span data-ttu-id="6ee3b-1192">フォーム グループ コントロールの水平位置を計算する方法を示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1192">Sets or returns a value that indicates how the horizontal position of a form group control is calculated.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="6ee3b-1193">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1193">Parameters - leftMode</span></span>

<span data-ttu-id="6ee3b-1194">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1194">value</span></span>  
<span data-ttu-id="6ee3b-1195">水平位置の計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1195">An Integer data type that indicates how the horizontal position is calculated; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="6ee3b-1196">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1196">Return Value - leftMode</span></span>

<span data-ttu-id="6ee3b-1197">水平位置の計算方法を示す整数データ型値です。正確なピクセル値、または FormLeft 列挙値は -1 のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1197">An Integer data type value that indicates how the horizontal position is calculated: -1 for an exact pixel value, or a FormLeft enumeration value.</span></span>

### <a name="examples---leftmode"></a><span data-ttu-id="6ee3b-1198">例 - leftMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1198">Examples - leftMode</span></span>

<span data-ttu-id="6ee3b-1199">次の例は、正確なピクセル値に基づいて、フォーム グループ コントロールの水平方向位置を計算する leftMode メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1199">The following example shows a call to the leftMode method that calculates the horizontal position of a form group control, based on an exact pixel value.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildStringControl formBuildStringControl; 
    FormBuildGroupControl formBuildGroupControl; 
    FormGroupControl formGroupControl; 
    int idx; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add controls. 
    formBuildGroupControl = 
 formBuildDesign.addControl(FormControlType::Group,"Group"); 
    idx = formBuildGroupControl.id(); 
    formBuildStringControl = 
 formBuildGroupControl.addControl(FormControlType::String,"String"); 
    // Add data fields to the controls. 
    formBuildGroupControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataField(2); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formGroupControl = formRun.control(idx); 
    formGroupControl.leftMode(-1); 
    formGroupControl.leftValue(50); 
}
```

## <a name="method-leftvalue"></a><span data-ttu-id="6ee3b-1200">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1200">Method leftValue</span></span>

<span data-ttu-id="6ee3b-1201">フォーム グループ コントロールの水平位置をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1201">Sets or returns the horizontal position of a form group control in pixels.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="6ee3b-1202">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1202">Parameters - leftValue</span></span>

<span data-ttu-id="6ee3b-1203">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1203">value</span></span>  
<span data-ttu-id="6ee3b-1204">水平位置をピクセル単位で示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1204">An integer value that indicates the horizontal position in pixels; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="6ee3b-1205">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1205">Return Value - leftValue</span></span>

<span data-ttu-id="6ee3b-1206">水平位置をピクセル単位で示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1206">An integer value that indicates the horizontal position in pixels.</span></span>

### <a name="remarks---leftvalue"></a><span data-ttu-id="6ee3b-1207">備考 - leftValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1207">Remarks - leftValue</span></span>

<span data-ttu-id="6ee3b-1208">正確なピクセル値に左モードが設定されていない限り、水平位置は変更されません。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1208">The horizontal position is not changed unless the left mode is set for an exact pixel value.</span></span>

### <a name="examples---leftvalue"></a><span data-ttu-id="6ee3b-1209">例 - leftValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1209">Examples - leftValue</span></span>

<span data-ttu-id="6ee3b-1210">次の例は、水平方向の位置を 50 ピクセルに設定する leftValue メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1210">The following example shows a call to the leftValue method that sets the horizontal position to 50 pixels.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildStringControl formBuildStringControl; 
    FormBuildGroupControl formBuildGroupControl; 
    FormGroupControl formGroupControl; 
    int idx; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add controls. 
    formBuildGroupControl = 
 formBuildDesign.addControl(FormControlType::Group,"Group"); 
    idx = formBuildGroupControl.id(); 
    formBuildStringControl = 
 formBuildGroupControl.addControl(FormControlType::String,"String"); 
    // Add data fields to the controls. 
    formBuildGroupControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataField(2); 
    args = new Args(); 
    args.object(form); 
    //C reate the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formGroupControl = formRun.control(idx); 
    formGroupControl.leftMode(-1); 
    formGroupControl.leftValue(50); 
}
```

## <a name="method-markasuseradd"></a><span data-ttu-id="6ee3b-1211">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1211">Method markAsUserAdd</span></span>

<span data-ttu-id="6ee3b-1212">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1212">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="6ee3b-1213">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1213">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="6ee3b-1214">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1214">value</span></span>  
<span data-ttu-id="6ee3b-1215">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1215">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="6ee3b-1216">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1216">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="6ee3b-1217">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1217">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="6ee3b-1218">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1218">Method mouseDblClick</span></span>

<span data-ttu-id="6ee3b-1219">ユーザーがフォーム グループ コントロールをダブルクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1219">Is called when the user double-clicks a form group control.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="6ee3b-1220">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1220">Parameters - mouseDblClick</span></span>

<span data-ttu-id="6ee3b-1221">x</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1221">x</span></span>  
<span data-ttu-id="6ee3b-1222">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1222">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1223">y</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1223">y</span></span>  
<span data-ttu-id="6ee3b-1224">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1224">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1225">ボタン</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1225">button</span></span>  
<span data-ttu-id="6ee3b-1226">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1226">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1227">Ctrl</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1227">Ctrl</span></span>  
<span data-ttu-id="6ee3b-1228">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1228">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1229">シフト</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1229">Shift</span></span>  
<span data-ttu-id="6ee3b-1230">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1230">A Boolean value that specifies whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="6ee3b-1231">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1231">Return Value - mouseDblClick</span></span>

<span data-ttu-id="6ee3b-1232">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1232">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="6ee3b-1233">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1233">Remarks - mouseDblClick</span></span>

<span data-ttu-id="6ee3b-1234">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1234">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="6ee3b-1235">button パラメーターに指定できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1235">The following are the possible values for the button parameter.</span></span>

|     |                      |
|-----|----------------------|
| <span data-ttu-id="6ee3b-1236">1</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1236">1</span></span>   | <span data-ttu-id="6ee3b-1237">マウスの左ボタン</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1237">Left mouse button.</span></span>   |
| <span data-ttu-id="6ee3b-1238">2</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1238">2</span></span>   | <span data-ttu-id="6ee3b-1239">マウスの中央ボタン。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1239">Middle mouse button.</span></span> |
| <span data-ttu-id="6ee3b-1240">3</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1240">3</span></span>   | <span data-ttu-id="6ee3b-1241">マウスの右ボタン</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1241">Right mouse button.</span></span>  |

<span data-ttu-id="6ee3b-1242">コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、mouseDblClick をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1242">You can override this method in a form group control by right-clicking the Methods node below the control, clicking Override Method, and then clicking mouseDblClick.</span></span> <span data-ttu-id="6ee3b-1243">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1243">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="6ee3b-1244">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1244">Method mouseDown</span></span>

<span data-ttu-id="6ee3b-1245">ユーザーがフォーム グループ コントロールでマウス ボタンを押すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1245">Is called when the user presses the mouse button in a form group control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="6ee3b-1246">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1246">Parameters - mouseDown</span></span>

<span data-ttu-id="6ee3b-1247">x</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1247">x</span></span>  
<span data-ttu-id="6ee3b-1248">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1248">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1249">y</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1249">y</span></span>  
<span data-ttu-id="6ee3b-1250">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1250">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1251">ボタン</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1251">button</span></span>  
<span data-ttu-id="6ee3b-1252">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1252">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1253">Ctrl</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1253">Ctrl</span></span>  
<span data-ttu-id="6ee3b-1254">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1254">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1255">シフト</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1255">Shift</span></span>  
<span data-ttu-id="6ee3b-1256">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1256">A Boolean value that specifies whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="6ee3b-1257">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1257">Return Value - mouseDown</span></span>

<span data-ttu-id="6ee3b-1258">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1258">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="6ee3b-1259">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1259">Remarks - mouseDown</span></span>

<span data-ttu-id="6ee3b-1260">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1260">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="6ee3b-1261">button パラメーターに指定できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1261">The following are the possible values for the button parameter.</span></span>

|     |                      |
|-----|----------------------|
| <span data-ttu-id="6ee3b-1262">1</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1262">1</span></span>   | <span data-ttu-id="6ee3b-1263">マウスの左ボタン</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1263">Left mouse button.</span></span>   |
| <span data-ttu-id="6ee3b-1264">2</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1264">2</span></span>   | <span data-ttu-id="6ee3b-1265">マウスの中央ボタン。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1265">Middle mouse button.</span></span> |
| <span data-ttu-id="6ee3b-1266">3</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1266">3</span></span>   | <span data-ttu-id="6ee3b-1267">マウスの右ボタン</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1267">Right mouse button.</span></span>  |

<span data-ttu-id="6ee3b-1268">コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、mouseDown をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1268">You can override this method in a form group control by right-clicking the Methods node below the control, clicking Override Method, and then clicking mouseDown.</span></span> <span data-ttu-id="6ee3b-1269">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1269">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="6ee3b-1270">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1270">Method mouseMove</span></span>

<span data-ttu-id="6ee3b-1271">ユーザーがマウス ポインターをフォーム グループ コントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1271">Is called when the user moves the mouse pointer over a form group control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="6ee3b-1272">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1272">Parameters - mouseMove</span></span>

<span data-ttu-id="6ee3b-1273">x</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1273">x</span></span>  
<span data-ttu-id="6ee3b-1274">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1274">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1275">y</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1275">y</span></span>  
<span data-ttu-id="6ee3b-1276">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1276">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1277">ボタン</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1277">button</span></span>  
<span data-ttu-id="6ee3b-1278">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1278">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1279">Ctrl</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1279">Ctrl</span></span>  
<span data-ttu-id="6ee3b-1280">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1280">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1281">シフト</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1281">Shift</span></span>  
<span data-ttu-id="6ee3b-1282">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1282">A Boolean value that specifies whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="6ee3b-1283">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1283">Return Value - mouseMove</span></span>

<span data-ttu-id="6ee3b-1284">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1284">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="6ee3b-1285">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1285">Remarks - mouseMove</span></span>

<span data-ttu-id="6ee3b-1286">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1286">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="6ee3b-1287">\_button パラメーターに指定できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1287">The following are the possible values for the \_button parameter.</span></span>

|     |                      |
|-----|----------------------|
| <span data-ttu-id="6ee3b-1288">1</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1288">1</span></span>   | <span data-ttu-id="6ee3b-1289">マウスの左ボタン</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1289">Left mouse button.</span></span>   |
| <span data-ttu-id="6ee3b-1290">2</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1290">2</span></span>   | <span data-ttu-id="6ee3b-1291">マウスの中央ボタン。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1291">Middle mouse button.</span></span> |
| <span data-ttu-id="6ee3b-1292">3</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1292">3</span></span>   | <span data-ttu-id="6ee3b-1293">マウスの右ボタン</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1293">Right mouse button.</span></span>  |

<span data-ttu-id="6ee3b-1294">コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、mouseMove をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1294">You can override this method in a form group control by right-clicking the Methods node below the control, clicking Override Method, and then clicking mouseMove.</span></span> <span data-ttu-id="6ee3b-1295">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1295">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="6ee3b-1296">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1296">Method mouseUp</span></span>

<span data-ttu-id="6ee3b-1297">ユーザーがマウス ボタンをフォーム グループ コントロール上で放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1297">Is called when the user releases the mouse button over a form group control.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="6ee3b-1298">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1298">Parameters - mouseUp</span></span>

<span data-ttu-id="6ee3b-1299">x</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1299">x</span></span>  
<span data-ttu-id="6ee3b-1300">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1300">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1301">y</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1301">y</span></span>  
<span data-ttu-id="6ee3b-1302">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1302">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1303">ボタン</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1303">button</span></span>  
<span data-ttu-id="6ee3b-1304">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1304">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1305">Ctrl</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1305">Ctrl</span></span>  
<span data-ttu-id="6ee3b-1306">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1306">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1307">シフト</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1307">Shift</span></span>  
<span data-ttu-id="6ee3b-1308">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1308">A Boolean value that specifies whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="6ee3b-1309">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1309">Return Value - mouseUp</span></span>

<span data-ttu-id="6ee3b-1310">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1310">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="6ee3b-1311">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1311">Remarks - mouseUp</span></span>

<span data-ttu-id="6ee3b-1312">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1312">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="6ee3b-1313">\_button パラメーターに指定できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1313">The following are the possible values for the \_button parameter.</span></span>

|     |                      |
|-----|----------------------|
| <span data-ttu-id="6ee3b-1314">1</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1314">1</span></span>   | <span data-ttu-id="6ee3b-1315">マウスの左ボタン</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1315">Left mouse button.</span></span>   |
| <span data-ttu-id="6ee3b-1316">2</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1316">2</span></span>   | <span data-ttu-id="6ee3b-1317">マウスの中央ボタン。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1317">Middle mouse button.</span></span> |
| <span data-ttu-id="6ee3b-1318">3</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1318">3</span></span>   | <span data-ttu-id="6ee3b-1319">マウスの右ボタン</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1319">Right mouse button.</span></span>  |

<span data-ttu-id="6ee3b-1320">コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、mouseUp をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1320">You can override this method in a form group control by right-clicking the Methods node below the control, clicking Override Method, and then clicking mouseUp.</span></span> <span data-ttu-id="6ee3b-1321">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1321">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="6ee3b-1322">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1322">Method moveControl</span></span>

<span data-ttu-id="6ee3b-1323">指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1323">Moves a specified control.</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="6ee3b-1324">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1324">Parameters - moveControl</span></span>

<span data-ttu-id="6ee3b-1325">controlId</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1325">controlId</span></span>  
<span data-ttu-id="6ee3b-1326">指定されたコントロールが後で挿入されるコントロールを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1326">An integer value that indicates which control the specified control is inserted after; optional.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1327">insertAfterId</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1327">insertAfterId</span></span>  
<span data-ttu-id="6ee3b-1328">指定されたコントロールが後で挿入されるコントロールを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1328">An integer value that indicates which control the specified control is inserted after; optional.</span></span>

### <a name="return-value---movecontrol"></a><span data-ttu-id="6ee3b-1329">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1329">Return Value - moveControl</span></span>

<span data-ttu-id="6ee3b-1330">コントロール ID を指定する整数データ型値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1330">An Integer data type value that specifies the control ID.</span></span>

## <a name="method-name"></a><span data-ttu-id="6ee3b-1331">メソッド名</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1331">Method name</span></span>

<span data-ttu-id="6ee3b-1332">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1332">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="6ee3b-1333">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1333">Parameters - name</span></span>

<span data-ttu-id="6ee3b-1334">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1334">value</span></span>  
<span data-ttu-id="6ee3b-1335">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1335">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="6ee3b-1336">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1336">Return Value - name</span></span>

<span data-ttu-id="6ee3b-1337">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1337">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="6ee3b-1338">備考 - name</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1338">Remarks - name</span></span>

<span data-ttu-id="6ee3b-1339">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1339">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="6ee3b-1340">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1340">It must begin with a letter.</span></span>
-   <span data-ttu-id="6ee3b-1341">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1341">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="6ee3b-1342">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1342">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="6ee3b-1343">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1343">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="6ee3b-1344">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1344">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="6ee3b-1345">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1345">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="6ee3b-1346">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1346">Parameters - neededPermission</span></span>

<span data-ttu-id="6ee3b-1347">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1347">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="6ee3b-1348">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1348">Return Value - neededPermission</span></span>

## <a name="method-optionvalue"></a><span data-ttu-id="6ee3b-1349">メソッド optionValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1349">Method optionValue</span></span>

<span data-ttu-id="6ee3b-1350">フォーム グループ コントロールに関連付けられているオプション ボタンの値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1350">Sets or returns the value for the option button that is associated with a form group control.</span></span>

```xpp
public int optionValue([int value])
```

### <a name="parameters---optionvalue"></a><span data-ttu-id="6ee3b-1351">パラメーター - optionValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1351">Parameters - optionValue</span></span>

<span data-ttu-id="6ee3b-1352">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1352">value</span></span>  
<span data-ttu-id="6ee3b-1353">オプション ボタンの値を指定する整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1353">An integer value that specifies the value for the option button; optional.</span></span>

### <a name="return-value---optionvalue"></a><span data-ttu-id="6ee3b-1354">戻り値 - optionValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1354">Return Value - optionValue</span></span>

<span data-ttu-id="6ee3b-1355">オプション ボタンの値を指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1355">An integer value that specifies the value for the option button.</span></span>

### <a name="remarks---optionvalue"></a><span data-ttu-id="6ee3b-1356">備考 - optionValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1356">Remarks - optionValue</span></span>

<span data-ttu-id="6ee3b-1357">フォーム グループ コントロールのオプション ボタンを設定または返すには、FormGroupControl.frameOptionButton メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1357">Use the FormGroupControl.frameOptionButton method to set or return the option button for a form group control.</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="6ee3b-1358">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1358">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="6ee3b-1359">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1359">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="6ee3b-1360">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1360">Method parentControl</span></span>

<span data-ttu-id="6ee3b-1361">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1361">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="6ee3b-1362">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1362">Return Value - parentControl</span></span>

<span data-ttu-id="6ee3b-1363">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1363">The parent control for the control.</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="6ee3b-1364">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1364">Method rightMargin</span></span>

<span data-ttu-id="6ee3b-1365">フォーム グループ コントロールの右余白のサイズをピクセル単位で設定するか返し、サイズが自動的に調整されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1365">Sets or returns the size of the right margin for a form group control in pixels and specifies whether the size is automatically adjusted.</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="6ee3b-1366">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1366">Parameters - rightMargin</span></span>

<span data-ttu-id="6ee3b-1367">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1367">value</span></span>  
<span data-ttu-id="6ee3b-1368">右余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1368">An AutoMode enumeration value that specifies whether the size of the right margin is fixed, or whether it is automatically adjusted based on other form property settings; optional.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1369">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1369">mode</span></span>  
<span data-ttu-id="6ee3b-1370">右余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1370">An AutoMode enumeration value that specifies whether the size of the right margin is fixed, or whether it is automatically adjusted based on other form property settings; optional.</span></span>

### <a name="return-value---rightmargin"></a><span data-ttu-id="6ee3b-1371">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1371">Return Value - rightMargin</span></span>

<span data-ttu-id="6ee3b-1372">フォーム グループ コントロールの右余白のサイズをピクセル単位で指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1372">An integer value that specifies the size of the right margin for a form group control in pixels.</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="6ee3b-1373">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1373">Method rightMarginMode</span></span>

<span data-ttu-id="6ee3b-1374">フォーム グループ コントロールの右余白のサイズが固定されているかどうか、またはフォーム プロパティ設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1374">Sets or returns a value that indicates whether the size of the right margin for a form group control is fixed, or whether it is automatically adjusted based on other form property settings.</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="6ee3b-1375">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1375">Parameters - rightMarginMode</span></span>

<span data-ttu-id="6ee3b-1376">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1376">mode</span></span>  
<span data-ttu-id="6ee3b-1377">右余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1377">An AutoMode enumeration value that specifies whether the size of the right margin is fixed, or whether it is automatically adjusted based on other form property settings; optional.</span></span>

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="6ee3b-1378">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1378">Return Value - rightMarginMode</span></span>

<span data-ttu-id="6ee3b-1379">右余白のサイズを固定したかどうか、または自動的に調整するかどうかを指定する Automode 列挙値です。右余白のサイズが自動的に調整される場合は自動、そうでなければ、固定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1379">An Automode enumeration value that specifies whether the size of the right margin is fixed, or whether it is automatically adjusted: Auto if the size of the right margin is automatically adjusted; otherwise, Fixed.</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="6ee3b-1380">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1380">Method rightMarginValue</span></span>

<span data-ttu-id="6ee3b-1381">フォーム グループ コントロールの右余白のサイズをピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1381">Sets or returns the size of the right margin for a form group control in pixels.</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="6ee3b-1382">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1382">Parameters - rightMarginValue</span></span>

<span data-ttu-id="6ee3b-1383">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1383">value</span></span>  
<span data-ttu-id="6ee3b-1384">フォーム グループ コントロールの右余白のサイズをピクセル単位で指定する整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1384">An integer value that specifies the size of the right margin for a form group control in pixels; optional.</span></span>

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="6ee3b-1385">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1385">Return Value - rightMarginValue</span></span>

<span data-ttu-id="6ee3b-1386">フォーム グループ コントロールの右余白のサイズをピクセル単位で指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1386">An integer value that specifies the size of the right margin for a form group control in pixels.</span></span>

## <a name="method-savefilter"></a><span data-ttu-id="6ee3b-1387">メソッド saveFilter</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1387">Method saveFilter</span></span>

```xpp
public boolean saveFilter([boolean value])
```

### <a name="parameters---savefilter"></a><span data-ttu-id="6ee3b-1388">パラメーター - saveFilter</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1388">Parameters - saveFilter</span></span>

<span data-ttu-id="6ee3b-1389">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1389">value</span></span>  

### <a name="return-value---savefilter"></a><span data-ttu-id="6ee3b-1390">戻り値 - saveFilter</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1390">Return Value - saveFilter</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="6ee3b-1391">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1391">Method securityKey</span></span>

<span data-ttu-id="6ee3b-1392">フォーム グループ コントロールのセキュリティ キー ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1392">Sets or returns the security key ID for a form group control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="6ee3b-1393">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1393">Parameters - securityKey</span></span>

<span data-ttu-id="6ee3b-1394">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1394">value</span></span>  
<span data-ttu-id="6ee3b-1395">ID を含む SecurityKeyId データ型、オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1395">A securityKeyId data type that contains the ID; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="6ee3b-1396">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1396">Return Value - securityKey</span></span>

<span data-ttu-id="6ee3b-1397">ID を含む SecurityKeyId データ型の値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1397">A securityKeyId data type value that contains the ID.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="6ee3b-1398">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1398">Method showContextMenu</span></span>

<span data-ttu-id="6ee3b-1399">フォーム グループ コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1399">Shows a shortcut menu for a form group control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="6ee3b-1400">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1400">Parameters - showContextMenu</span></span>

<span data-ttu-id="6ee3b-1401">menuHandle</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1401">menuHandle</span></span>  
<span data-ttu-id="6ee3b-1402">ショートカット メニューのハンドルを指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1402">An integer value that specifies the handle for the shortcut menu.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="6ee3b-1403">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1403">Return Value - showContextMenu</span></span>

<span data-ttu-id="6ee3b-1404">ユーザーの選択を指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1404">An integer value that specifies the selection of the user.</span></span>

## <a name="method-skip"></a><span data-ttu-id="6ee3b-1405">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1405">Method skip</span></span>

<span data-ttu-id="6ee3b-1406">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示すブール値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1406">Sets or returns a Boolean value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="6ee3b-1407">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1407">Parameters - skip</span></span>

<span data-ttu-id="6ee3b-1408">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1408">value</span></span>  
<span data-ttu-id="6ee3b-1409">コントロールがスキップされたかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1409">A Boolean value that indicates whether the control is skipped; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="6ee3b-1410">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1410">Return Value - skip</span></span>

<span data-ttu-id="6ee3b-1411">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1411">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-sort"></a><span data-ttu-id="6ee3b-1412">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1412">Method sort</span></span>

<span data-ttu-id="6ee3b-1413">フォーム グループ コントロールに格納されているコントロールを並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1413">Sorts the controls that are contained in a form group control.</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="6ee3b-1414">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1414">Parameters - sort</span></span>

<span data-ttu-id="6ee3b-1415">sortDirection</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1415">sortDirection</span></span>  
<span data-ttu-id="6ee3b-1416">コントロールの並べ替え順序を示すシステム列挙値、オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1416">A system enumeration value that indicates the sort order for controls; optional.</span></span>

### <a name="return-value---sort"></a><span data-ttu-id="6ee3b-1417">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1417">Return Value - sort</span></span>

<span data-ttu-id="6ee3b-1418">並べ替え順序を含む整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1418">An integer value that contains the sort order.</span></span>

## <a name="method-style"></a><span data-ttu-id="6ee3b-1419">メソッド style</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1419">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="6ee3b-1420">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1420">Parameters - style</span></span>

<span data-ttu-id="6ee3b-1421">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1421">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="6ee3b-1422">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1422">Return Value - style</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="6ee3b-1423">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1423">Method toolTip</span></span>

<span data-ttu-id="6ee3b-1424">フォーム グループ コントロールのツールヒントのテキスト文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1424">Returns the text string for the tooltip for a form group control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="6ee3b-1425">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1425">Return Value - toolTip</span></span>

<span data-ttu-id="6ee3b-1426">ツールヒントのテキストを含む文字列値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1426">A string value that contains the text for the tooltip.</span></span>

## <a name="method-top"></a><span data-ttu-id="6ee3b-1427">メソッド top</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1427">Method top</span></span>

<span data-ttu-id="6ee3b-1428">フォーム グループ コントロールの垂直位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1428">Sets or returns the vertical position of a form group control in pixels and specifies how the position is calculated.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="6ee3b-1429">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1429">Parameters - top</span></span>

<span data-ttu-id="6ee3b-1430">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1430">value</span></span>  
<span data-ttu-id="6ee3b-1431">垂直位置の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1431">An integer value that indicates how the vertical position is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1432">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1432">mode</span></span>  
<span data-ttu-id="6ee3b-1433">垂直位置の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1433">An integer value that indicates how the vertical position is calculated; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="6ee3b-1434">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1434">Return Value - top</span></span>

<span data-ttu-id="6ee3b-1435">フォーム グループ コントロールの垂直位置をピクセル単位で示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1435">An integer value that indicates the vertical position of a form group control in pixels.</span></span>

### <a name="remarks---top"></a><span data-ttu-id="6ee3b-1436">備考 - top</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1436">Remarks - top</span></span>

<span data-ttu-id="6ee3b-1437">mode パラメーターは、次の値のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1437">The mode parameter can be one of the following values:</span></span>

-   <span data-ttu-id="6ee3b-1438">-1 (既定) � 値パラメーターの値が正確に使用される Exact モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1438">-1 (default) � Use Exact mode, where the value of the value parameter is used exactly.</span></span>
-   <span data-ttu-id="6ee3b-1439">FormTop 列挙値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1439">A FormTop enumeration value.</span></span>

### <a name="examples---top"></a><span data-ttu-id="6ee3b-1440">例 - top</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1440">Examples - top</span></span>

<span data-ttu-id="6ee3b-1441">次の例では、上位メソッドを呼び出して、垂直位置を 50 ピクセルに設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1441">The following example calls the top method to set the vertical position to 50 pixels.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildStringControl formBuildStringControl; 
    FormBuildGroupControl formBuildGroupControl; 
    FormGroupControl formGroupControl; 
    int idx; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add controls. 
    formBuildGroupControl = 
 formBuildDesign.addControl(FormControlType::Group,"Group"); 
    idx = formBuildGroupControl.id(); 
    formBuildStringControl = 
 formBuildGroupControl.addControl(FormControlType::String,"String"); 
    // Add data fields to the controls. 
    formBuildGroupControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataField(2); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formGroupControl = formRun.control(idx); 
    formGroupControl.top(50,-1); 
}
```

## <a name="method-topmargin"></a><span data-ttu-id="6ee3b-1442">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1442">Method topMargin</span></span>

<span data-ttu-id="6ee3b-1443">フォーム グループ コントロールの上余白をピクセル単位で設定するか返し、サイズが自動的に調整されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1443">Sets or returns the top margin for a form group control in pixels and specifies whether the size is automatically adjusted.</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="6ee3b-1444">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1444">Parameters - topMargin</span></span>

<span data-ttu-id="6ee3b-1445">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1445">value</span></span>  
<span data-ttu-id="6ee3b-1446">上余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1446">An AutoMode enumeration value that specifies whether the size of the top margin is fixed, or whether it is automatically adjusted based on other form property settings; optional.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1447">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1447">mode</span></span>  
<span data-ttu-id="6ee3b-1448">上余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1448">An AutoMode enumeration value that specifies whether the size of the top margin is fixed, or whether it is automatically adjusted based on other form property settings; optional.</span></span>

### <a name="return-value---topmargin"></a><span data-ttu-id="6ee3b-1449">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1449">Return Value - topMargin</span></span>

<span data-ttu-id="6ee3b-1450">フォーム グループ コントロールの上余白のサイズをピクセル単位で指定する整数。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1450">An integer that specifies the size of the top margin for a form group control in pixels.</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="6ee3b-1451">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1451">Method topMarginMode</span></span>

<span data-ttu-id="6ee3b-1452">フォーム グループ コントロールの上余白のサイズが固定されているかどうか、またはフォーム プロパティ設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1452">Sets or returns a value that indicates whether the size of the top margin for a form group control is fixed, or whether it is automatically adjusted based on other form property settings.</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="6ee3b-1453">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1453">Parameters - topMarginMode</span></span>

<span data-ttu-id="6ee3b-1454">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1454">mode</span></span>  
<span data-ttu-id="6ee3b-1455">上余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す Automode 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1455">An Automode enumeration value that specifies whether the size of the top margin is fixed, or whether it is automatically adjusted based on other form property settings; optional.</span></span>

### <a name="return-value---topmarginmode"></a><span data-ttu-id="6ee3b-1456">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1456">Return Value - topMarginMode</span></span>

<span data-ttu-id="6ee3b-1457">左余白のサイズが自動的に調整される場合は自動の Automode 列挙値、そうでない場合は、固定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1457">An Automode enumeration value of Auto if the size of the top margin is automatically adjusted; otherwise, Fixed.</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="6ee3b-1458">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1458">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="6ee3b-1459">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1459">Parameters - topMarginValue</span></span>

<span data-ttu-id="6ee3b-1460">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1460">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="6ee3b-1461">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1461">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="6ee3b-1462">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1462">Method topMode</span></span>

<span data-ttu-id="6ee3b-1463">フォーム グループ コントロールの垂直位置を計算する方法を示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1463">Sets or returns a value that indicates how the vertical position of a form group control is calculated.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="6ee3b-1464">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1464">Parameters - topMode</span></span>

<span data-ttu-id="6ee3b-1465">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1465">value</span></span>  
<span data-ttu-id="6ee3b-1466">垂直位置の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1466">An integer that indicates how the vertical position is calculated; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="6ee3b-1467">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1467">Return Value - topMode</span></span>

<span data-ttu-id="6ee3b-1468">垂直位置の計算方法を示す整数値。正確なピクセル値、または FormTop 列挙値は -1 。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1468">An integer value that indicates how the vertical position is calculated: -1 for an exact pixel value, or a FormTop enumeration value.</span></span>

### <a name="examples---topmode"></a><span data-ttu-id="6ee3b-1469">例 - topMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1469">Examples - topMode</span></span>

<span data-ttu-id="6ee3b-1470">次の例は、正確なピクセル値に基づいて、垂直位置を計算する topMode メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1470">The following example shows a call to the topMode method that calculates the vertical position, based on an exact pixel value.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildStringControl formBuildStringControl; 
    FormBuildGroupControl formBuildGroupControl; 
    FormGroupControl formGroupControl; 
    int idx; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add controls. 
    formBuildGroupControl = 
 formBuildDesign.addControl(FormControlType::Group,"Group"); 
    idx = formBuildGroupControl.id(); 
    formBuildStringControl = 
 formBuildGroupControl.addControl(FormControlType::String,"String"); 
    // Add data fields to the controls. 
    formBuildGroupControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataField(2); 
    args = new Args(); 
    args.object(form); 
    // Create the run time-form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formGroupControl = formRun.control(idx); 
    formGroupControl.topMode(-1); 
    formGroupControl.topValue(50); 
}
```

## <a name="method-topvalue"></a><span data-ttu-id="6ee3b-1471">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1471">Method topValue</span></span>

<span data-ttu-id="6ee3b-1472">フォーム グループ コントロールの垂直位置をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1472">Sets or returns the vertical position of a form group control in pixels.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="6ee3b-1473">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1473">Parameters - topValue</span></span>

<span data-ttu-id="6ee3b-1474">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1474">value</span></span>  
<span data-ttu-id="6ee3b-1475">垂直位置を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1475">An Integer data type that specifies the vertical position.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="6ee3b-1476">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1476">Return Value - topValue</span></span>

<span data-ttu-id="6ee3b-1477">フォーム グループ コントロールの垂直位置を指定する整数データ型値です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1477">An Integer data type value that specifies the vertical position of a form group control.</span></span>

### <a name="remarks---topvalue"></a><span data-ttu-id="6ee3b-1478">備考 - topValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1478">Remarks - topValue</span></span>

<span data-ttu-id="6ee3b-1479">正確なピクセル値に上部モードが設定されていない限り、垂直位置は変更されません。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1479">The vertical position is not changed unless the top mode is set for an exact pixel value.</span></span> <span data-ttu-id="6ee3b-1480">詳細については、「topMode メソッド」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1480">For more information, see the topMode method.</span></span>

### <a name="examples---topvalue"></a><span data-ttu-id="6ee3b-1481">例 - topValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1481">Examples - topValue</span></span>

<span data-ttu-id="6ee3b-1482">次の例は、垂直位置を 50 ピクセルに設定する topValue メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1482">The following example shows a call to the topValue method that sets the vertical position to 50 pixels.</span></span>

```xpp
void FormGoupControl() 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildStringControl formBuildStringControl; 
    FormBuildGroupControl formBuildGroupControl; 
    FormGroupControl formGroupControl; 
    int idx; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add controls. 
    formBuildGroupControl = 
 formBuildDesign.addControl(FormControlType::Group,"Group"); 
    idx = formBuildGroupControl.id(); 
    formBuildStringControl = 
 formBuildGroupControl.addControl(FormControlType::String,"String"); 
    // Add data fields to the controls. 
    formBuildGroupControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataField(2); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formGroupControl = formRun.control(idx); 
    formGroupControl.topMode(-1); 
    formGroupControl.topValue(50); 
}
```

## <a name="method-type"></a><span data-ttu-id="6ee3b-1483">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1483">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="6ee3b-1484">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1484">Parameters - type</span></span>

<span data-ttu-id="6ee3b-1485">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1485">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="6ee3b-1486">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1486">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="6ee3b-1487">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1487">Method underline</span></span>

<span data-ttu-id="6ee3b-1488">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1488">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="6ee3b-1489">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1489">Parameters - underline</span></span>

<span data-ttu-id="6ee3b-1490">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1490">value</span></span>  
<span data-ttu-id="6ee3b-1491">コントロールの underline プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1491">The value to assign to the underline property of the control; optional.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="6ee3b-1492">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1492">Return Value - underline</span></span>

<span data-ttu-id="6ee3b-1493">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1493">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="6ee3b-1494">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1494">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="6ee3b-1495">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1495">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="6ee3b-1496">データ</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1496">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="6ee3b-1497">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1497">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="6ee3b-1498">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1498">Method userData</span></span>

<span data-ttu-id="6ee3b-1499">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1499">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="6ee3b-1500">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1500">Parameters - userData</span></span>

<span data-ttu-id="6ee3b-1501">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1501">value</span></span>  
<span data-ttu-id="6ee3b-1502">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1502">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="6ee3b-1503">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1503">Return Value - userData</span></span>

<span data-ttu-id="6ee3b-1504">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1504">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="6ee3b-1505">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1505">Method userDataItem</span></span>

<span data-ttu-id="6ee3b-1506">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1506">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="6ee3b-1507">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1507">Parameters - userDataItem</span></span>

<span data-ttu-id="6ee3b-1508">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1508">value</span></span>  
<span data-ttu-id="6ee3b-1509">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1509">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="6ee3b-1510">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1510">Return Value - userDataItem</span></span>

<span data-ttu-id="6ee3b-1511">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1511">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="6ee3b-1512">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1512">Method userDataItems</span></span>

<span data-ttu-id="6ee3b-1513">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1513">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="6ee3b-1514">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1514">Parameters - userDataItems</span></span>

<span data-ttu-id="6ee3b-1515">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1515">value</span></span>  
<span data-ttu-id="6ee3b-1516">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1516">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="6ee3b-1517">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1517">Return Value - userDataItems</span></span>

<span data-ttu-id="6ee3b-1518">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1518">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="6ee3b-1519">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1519">Method userDisable</span></span>

<span data-ttu-id="6ee3b-1520">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1520">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="6ee3b-1521">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1521">Parameters - userDisable</span></span>

<span data-ttu-id="6ee3b-1522">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1522">value</span></span>  
<span data-ttu-id="6ee3b-1523">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1523">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="6ee3b-1524">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1524">Return Value - userDisable</span></span>

<span data-ttu-id="6ee3b-1525">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1525">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="6ee3b-1526">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1526">Method userHeight</span></span>

<span data-ttu-id="6ee3b-1527">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1527">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="6ee3b-1528">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1528">Parameters - userHeight</span></span>

<span data-ttu-id="6ee3b-1529">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1529">value</span></span>  
<span data-ttu-id="6ee3b-1530">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1530">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="6ee3b-1531">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1531">Return Value - userHeight</span></span>

<span data-ttu-id="6ee3b-1532">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1532">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="6ee3b-1533">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1533">Method userHide</span></span>

<span data-ttu-id="6ee3b-1534">コントロールがユーザーから非表示になっているかどうかを示す整数データ型を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1534">Sets or returns an integer data type that indicates whether a control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="6ee3b-1535">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1535">Parameters - userHide</span></span>

<span data-ttu-id="6ee3b-1536">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1536">value</span></span>  
<span data-ttu-id="6ee3b-1537">フォーム グループ コントロールはユーザーから隠されているかどうかを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1537">An integer value that indicates whether a form group control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="6ee3b-1538">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1538">Return Value - userHide</span></span>

<span data-ttu-id="6ee3b-1539">フォーム グループ コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1539">1 if the form group control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="6ee3b-1540">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1540">Remarks - userHide</span></span>

<span data-ttu-id="6ee3b-1541">ユーザーは、コントロールを右クリックして [非表示] をクリックして、フォーム グループ コントロールを非表示にできます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1541">The user can hide a form group control by right-clicking the control and then clicking Hide.</span></span> <span data-ttu-id="6ee3b-1542">このメソッドでは、プログラムを使用してコントロールが非表示にするかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1542">This method lets you programmatically determine whether the control is hidden.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="6ee3b-1543">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1543">Method userOrgContainer</span></span>

<span data-ttu-id="6ee3b-1544">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1544">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="6ee3b-1545">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1545">Parameters - userOrgContainer</span></span>

<span data-ttu-id="6ee3b-1546">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1546">value</span></span>  
<span data-ttu-id="6ee3b-1547">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1547">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="6ee3b-1548">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1548">Return Value - userOrgContainer</span></span>

<span data-ttu-id="6ee3b-1549">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1549">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="6ee3b-1550">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1550">Method userOrgSibling</span></span>

<span data-ttu-id="6ee3b-1551">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1551">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="6ee3b-1552">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1552">Parameters - userOrgSibling</span></span>

<span data-ttu-id="6ee3b-1553">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1553">value</span></span>  
<span data-ttu-id="6ee3b-1554">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1554">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="6ee3b-1555">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1555">Return Value - userOrgSibling</span></span>

<span data-ttu-id="6ee3b-1556">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1556">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="6ee3b-1557">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1557">Method userPromptText</span></span>

<span data-ttu-id="6ee3b-1558">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1558">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="6ee3b-1559">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1559">Parameters - userPromptText</span></span>

<span data-ttu-id="6ee3b-1560">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1560">value</span></span>  
<span data-ttu-id="6ee3b-1561">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1561">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="6ee3b-1562">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1562">Return Value - userPromptText</span></span>

<span data-ttu-id="6ee3b-1563">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1563">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="6ee3b-1564">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1564">Method userSecurityLevel</span></span>

<span data-ttu-id="6ee3b-1565">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1565">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="6ee3b-1566">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1566">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="6ee3b-1567">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1567">value</span></span>  
<span data-ttu-id="6ee3b-1568">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1568">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="6ee3b-1569">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1569">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="6ee3b-1570">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1570">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="6ee3b-1571">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1571">Method userSkip</span></span>

<span data-ttu-id="6ee3b-1572">ユーザーが Tab キーを押してコントロールに移動するときにフォーム グループ コントロールがスキップされるかどうかを示す整数を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1572">Sets or returns an integer that indicates whether the form group control is skipped when the user presses the TAB key to move to controls.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="6ee3b-1573">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1573">Parameters - userSkip</span></span>

<span data-ttu-id="6ee3b-1574">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1574">value</span></span>  
<span data-ttu-id="6ee3b-1575">フォーム グループ コントロールをスキップするかどうかのユーザー設定を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1575">An integer that indicates the user setting for whether a form group control is skipped; optional.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="6ee3b-1576">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1576">Return Value - userSkip</span></span>

<span data-ttu-id="6ee3b-1577">フォーム グループ コントロールがスキップされる場合は 1、それ以外の場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1577">1 if the form group control is skipped; otherwise, 0.</span></span>

### <a name="remarks---userskip"></a><span data-ttu-id="6ee3b-1578">備考 - userSkip</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1578">Remarks - userSkip</span></span>

<span data-ttu-id="6ee3b-1579">ユーザーは、ユーザー設定フォームを使用してフォーム グループ コントロールをスキップするかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1579">The user chooses whether to skip a form group control by using the User setup form.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="6ee3b-1580">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1580">Method userWidth</span></span>

<span data-ttu-id="6ee3b-1581">フォーム グループ コントロールの幅をピクセル単位で示す整数を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1581">Sets or returns an integer that indicates the width of a form group control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="6ee3b-1582">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1582">Parameters - userWidth</span></span>

<span data-ttu-id="6ee3b-1583">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1583">value</span></span>  
<span data-ttu-id="6ee3b-1584">フォーム グループ コントロールの幅をピクセル単位で示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1584">An integer that indicates the width of a form group control in pixels; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="6ee3b-1585">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1585">Return Value - userWidth</span></span>

<span data-ttu-id="6ee3b-1586">フォーム グループ コントロールの幅をピクセル単位で示す整数値。ユーザーが幅を指定していない場合は 0 (ゼロ) 。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1586">An integer value that indicates the width of a form group control in pixels; 0 (zero) if the user did not specify a width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="6ee3b-1587">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1587">Remarks - userWidth</span></span>

<span data-ttu-id="6ee3b-1588">ユーザーは、ユーザー設定フォームを使用して文字の幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1588">The user specifies the width in characters by using the User setup form.</span></span> <span data-ttu-id="6ee3b-1589">このメソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1589">This method returns the width in pixels, based on six times the number of characters.</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="6ee3b-1590">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1590">Method useUserLayout</span></span>

<span data-ttu-id="6ee3b-1591">フォーム グループ コントロールのユーザー指定レイアウトを使用するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1591">Specifies whether to use the user-specified layout of a form group control.</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="6ee3b-1592">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1592">Parameters - useUserLayout</span></span>

<span data-ttu-id="6ee3b-1593">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1593">value</span></span>  
<span data-ttu-id="6ee3b-1594">フォーム グループ コントロールのユーザー指定のレイアウトを使用するかどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1594">A Boolean value that specifies whether to use the user-specified layout of a form group control; optional.</span></span>

### <a name="return-value---useuserlayout"></a><span data-ttu-id="6ee3b-1595">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1595">Return Value - useUserLayout</span></span>

<span data-ttu-id="6ee3b-1596">フォーム グループ コントロールのユーザー指定レイアウトが使用される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1596">true if the user-specified layout of a form group control is used; otherwise, false.</span></span>

### <a name="remarks---useuserlayout"></a><span data-ttu-id="6ee3b-1597">備考 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1597">Remarks - useUserLayout</span></span>

<span data-ttu-id="6ee3b-1598">ユーザーは、ユーザー設定フォームを使用してレイアウトを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1598">The user specifies the layout by using the User setup form.</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="6ee3b-1599">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1599">Method verticalSpacing</span></span>

<span data-ttu-id="6ee3b-1600">ピクセルでフォーム グループ コントロールの上と下のスペースの量を取得または設定し、スペースを計算する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1600">Gets or sets the amount of space above and below a form group control in pixels, and specifies how the space is calculated.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="6ee3b-1601">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1601">Parameters - verticalSpacing</span></span>

<span data-ttu-id="6ee3b-1602">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1602">value</span></span>  
<span data-ttu-id="6ee3b-1603">領域の計算方法を示す AutoMode システムの列挙値、オプションです。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1603">An AutoMode system enumeration value that indicates how the space is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1604">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1604">mode</span></span>  
<span data-ttu-id="6ee3b-1605">領域の計算方法を示す AutoMode システムの列挙値、オプションです。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1605">An AutoMode system enumeration value that indicates how the space is calculated; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="6ee3b-1606">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1606">Return Value - verticalSpacing</span></span>

<span data-ttu-id="6ee3b-1607">コントロールの上と下のスペースの量を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1607">An integer value that indicates the amount of space above and below a control.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="6ee3b-1608">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1608">Method verticalSpacingMode</span></span>

<span data-ttu-id="6ee3b-1609">フォーム グループ コントロールの上と下のスペースの量を計算する方法を示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1609">Sets or returns a value that indicates how the amount of space above and below a form group control is calculated.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="6ee3b-1610">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1610">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="6ee3b-1611">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1611">mode</span></span>  
<span data-ttu-id="6ee3b-1612">領域の計算方法を示す AutoMode システムの列挙値、オプションです。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1612">An AutoMode system enumeration value that indicates how the space is calculated; optional.</span></span>

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="6ee3b-1613">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1613">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="6ee3b-1614">フォント サイズなどの他のフォーム設定に基づいてスペースが自動的に調整される場合 AutoMode 列挙は自動に設定しますが、それ以外の場合は、固定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1614">An AutoMode enumeration that is set to Auto if the space is automatically adjusted based on other form settings, such as the font size; otherwise, Fixed.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="6ee3b-1615">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1615">Method verticalSpacingValue</span></span>

<span data-ttu-id="6ee3b-1616">ピクセルでフォーム グループ コントロールの上と下のスペースの量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1616">Gets or sets the amount of space above and below a form group control in pixels.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="6ee3b-1617">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1617">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="6ee3b-1618">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1618">value</span></span>  
<span data-ttu-id="6ee3b-1619">コントロールの上と下のスペースの量を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1619">An integer that indicates the amount of space above and below a control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="6ee3b-1620">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1620">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="6ee3b-1621">コントロールの上と下のスペースの量を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1621">An integer value that indicates the amount of space above and below a control.</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="6ee3b-1622">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1622">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="6ee3b-1623">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1623">Parameters - viewEditMode</span></span>

<span data-ttu-id="6ee3b-1624">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1624">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="6ee3b-1625">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1625">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="6ee3b-1626">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1626">Method visible</span></span>

<span data-ttu-id="6ee3b-1627">フォーム グループ コントロールを表示または非表示にするブール値データ型を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1627">Gets or sets a Boolean data type that displays or hides a form group control.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="6ee3b-1628">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1628">Parameters - visible</span></span>

<span data-ttu-id="6ee3b-1629">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1629">value</span></span>  
<span data-ttu-id="6ee3b-1630">フォーム グループ コントロールを表示または非表示にするブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1630">A Boolean value that displays or hides a form group control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="6ee3b-1631">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1631">Return Value - visible</span></span>

<span data-ttu-id="6ee3b-1632">フォーム グループ コントロールが表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1632">true if the form group control is displayed; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="6ee3b-1633">メソッド width</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1633">Method width</span></span>

<span data-ttu-id="6ee3b-1634">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1634">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="6ee3b-1635">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1635">Parameters - width</span></span>

<span data-ttu-id="6ee3b-1636">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1636">value</span></span>  
<span data-ttu-id="6ee3b-1637">幅の計算方法を示す整数。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1637">An integer that indicates how the width is calculated.</span></span> <span data-ttu-id="6ee3b-1638">これは、次のいずれかの値になります。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1638">This can be one of the following values:</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1639">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1639">mode</span></span>  
<span data-ttu-id="6ee3b-1640">幅の計算方法を示す整数。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1640">An integer that indicates how the width is calculated.</span></span> <span data-ttu-id="6ee3b-1641">これは、次のいずれかの値になります。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1641">This can be one of the following values:</span></span>

### <a name="return-value---width"></a><span data-ttu-id="6ee3b-1642">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1642">Return Value - width</span></span>

<span data-ttu-id="6ee3b-1643">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1643">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="6ee3b-1644">備考 - width</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1644">Remarks - width</span></span>

<span data-ttu-id="6ee3b-1645">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1645">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="6ee3b-1646">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1646">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="6ee3b-1647">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1647">Mode</span></span>             | <span data-ttu-id="6ee3b-1648">幅計算</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1648">Width calculation</span></span>                                                                         |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee3b-1649">-1 � 正確</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1649">-1 � Exact</span></span>       | <span data-ttu-id="6ee3b-1650">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1650">The exact width of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="6ee3b-1651">0 � 自動</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1651">0 � Auto</span></span>         | <span data-ttu-id="6ee3b-1652">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1652">The width of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6ee3b-1653">1 � 列の幅</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1653">1 � Column width</span></span> | <span data-ttu-id="6ee3b-1654">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1654">The layout of the form determines the width of the control.</span></span>                               |

<span data-ttu-id="6ee3b-1655">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1655">The width and the width calculation mode can be set separately.</span></span>

### <a name="examples---width"></a><span data-ttu-id="6ee3b-1656">例 - width</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1656">Examples - width</span></span>

<span data-ttu-id="6ee3b-1657">次の例は、コントロールの幅を 200 ピクセルに設定する width メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1657">The following example shows a call to the width method to set the control width to 200 pixels.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildStringControl formBuildStringControl; 
    FormBuildGroupControl formBuildGroupControl; 
    FormGroupControl formGroupControl; 
    int idx; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add controls. 
    formBuildGroupControl = 
 formBuildDesign.addControl(FormControlType::Group,"Group"); 
    idx = formBuildGroupControl.id(); 
    formBuildStringControl = 
 formBuildGroupControl.addControl(FormControlType::String,"String"); 
    // Add data fields to the controls. 
    formBuildGroupControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataField(2); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formGroupControl = formRun.control(idx); 
    formGroupControl.width(200,-1); 
}
```

## <a name="method-widthmode"></a><span data-ttu-id="6ee3b-1658">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1658">Method widthMode</span></span>

<span data-ttu-id="6ee3b-1659">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1659">Gets or sets the calculation mode for the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="6ee3b-1660">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1660">Parameters - widthMode</span></span>

<span data-ttu-id="6ee3b-1661">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1661">value</span></span>  
<span data-ttu-id="6ee3b-1662">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1662">An integer value that indicates how the control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="6ee3b-1663">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1663">Return Value - widthMode</span></span>

<span data-ttu-id="6ee3b-1664">現在の計算モードの幅を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1664">An integer value that indicates the width current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="6ee3b-1665">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1665">Remarks - widthMode</span></span>

<span data-ttu-id="6ee3b-1666">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1666">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="6ee3b-1667">モード</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1667">Mode</span></span>         | <span data-ttu-id="6ee3b-1668">幅計算</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1668">Width calculation</span></span>                                                                         |
|--------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee3b-1669">正確</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1669">Exact</span></span>        | <span data-ttu-id="6ee3b-1670">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1670">The exact width of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="6ee3b-1671">自動</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1671">Auto</span></span>         | <span data-ttu-id="6ee3b-1672">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1672">The width of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6ee3b-1673">列の幅</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1673">Column width</span></span> | <span data-ttu-id="6ee3b-1674">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1674">The layout of the form determines the width of the control.</span></span>                               |

<span data-ttu-id="6ee3b-1675">計算モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1675">The width of the control might change when the calculation mode is set to Auto or Column width.</span></span>

### <a name="examples---widthmode"></a><span data-ttu-id="6ee3b-1676">例 - widthMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1676">Examples - widthMode</span></span>

<span data-ttu-id="6ee3b-1677">次の例は、正確なピクセル値に基づいて、コントロールの幅を計算する widthMode メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1677">The following example shows a call to the widthMode method to calculate the control width, based on an exact pixel value.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildStringControl formBuildStringControl; 
    FormBuildGroupControl formBuildGroupControl; 
    FormGroupControl formGroupControl; 
    int idx; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add controls. 
    formBuildGroupControl = 
 formBuildDesign.addControl(FormControlType::Group,"Group"); 
    idx = formBuildGroupControl.id(); 
    formBuildStringControl = 
 formBuildGroupControl.addControl(FormControlType::String,"String"); 
    // Add data fields to the controls. 
    formBuildGroupControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataField(2); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formGroupControl = formRun.control(idx); 
    formGroupControl.widthMode(-1); 
    formGroupControl.widthValue(200); 
}
```

## <a name="method-widthvalue"></a><span data-ttu-id="6ee3b-1678">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1678">Method widthValue</span></span>

<span data-ttu-id="6ee3b-1679">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1679">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="6ee3b-1680">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1680">Parameters - widthValue</span></span>

<span data-ttu-id="6ee3b-1681">値</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1681">value</span></span>  
<span data-ttu-id="6ee3b-1682">コントロールの幅をピクセル単位で指定する整数。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1682">An integer that specifies the width of the control in pixels.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="6ee3b-1683">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1683">Return Value - widthValue</span></span>

<span data-ttu-id="6ee3b-1684">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1684">The width of the control in pixels.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="6ee3b-1685">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1685">Remarks - widthValue</span></span>

<span data-ttu-id="6ee3b-1686">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1686">To change the width of the control, use the Exact width calculation mode.</span></span>

### <a name="examples---widthvalue"></a><span data-ttu-id="6ee3b-1687">例 - widthValue</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1687">Examples - widthValue</span></span>

<span data-ttu-id="6ee3b-1688">次の例は、コントロールの幅を 200 ピクセルに設定する widthValue メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1688">The following example shows a call to the widthValue method that sets the control width to 200 pixels.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildStringControl formBuildStringControl; 
    FormBuildGroupControl formBuildGroupControl; 
    FormGroupControl formGroupControl; 
    int idx; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add controls. 
    formBuildGroupControl = 
 formBuildDesign.addControl(FormControlType::Group,"Group"); 
    idx = formBuildGroupControl.id(); 
    formBuildStringControl = 
 formBuildGroupControl.addControl(FormControlType::String,"String"); 
    // Add data fields to the controls. 
    formBuildGroupControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataSource(formBuildDataSource.id()); 
    formBuildStringControl.dataField(2); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formGroupControl = formRun.control(idx); 
    formGroupControl.widthMode(-1); 
    formGroupControl.widthValue(200); 
}
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="6ee3b-1689">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1689">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="6ee3b-1690">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1690">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="6ee3b-1691">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1691">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="6ee3b-1692">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1692">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="6ee3b-1693">overrideObject</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1693">overrideObject</span></span>  

## <a name="method-drop"></a><span data-ttu-id="6ee3b-1694">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1694">Method drop</span></span>

<span data-ttu-id="6ee3b-1695">ユーザーがフォーム グループ コントロールまたはフォーム グループ コントロールのアイテムを新しい位置にドロップすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1695">Is called when a user drops a form group control or an item in a form group control into a new position.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="6ee3b-1696">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1696">Parameters - drop</span></span>

<span data-ttu-id="6ee3b-1697">dragSource</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1697">dragSource</span></span>  
<span data-ttu-id="6ee3b-1698">オブジェクト位置の y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1698">An integer value that indicates the y-coordinate of the object position.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1699">dragMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1699">dragMode</span></span>  
<span data-ttu-id="6ee3b-1700">オブジェクト位置の y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1700">An integer value that indicates the y-coordinate of the object position.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1701">x</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1701">x</span></span>  
<span data-ttu-id="6ee3b-1702">オブジェクト位置の y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1702">An integer value that indicates the y-coordinate of the object position.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1703">y</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1703">y</span></span>  
<span data-ttu-id="6ee3b-1704">オブジェクト位置の y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1704">An integer value that indicates the y-coordinate of the object position.</span></span>

### <a name="remarks---drop"></a><span data-ttu-id="6ee3b-1705">備考 - drop</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1705">Remarks - drop</span></span>

<span data-ttu-id="6ee3b-1706">コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、drop をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1706">You can override this method in a form group control by right-clicking the Methods node below the control, clicking Override Method, and then clicking drop.</span></span> <span data-ttu-id="6ee3b-1707">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1707">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-onlostfocus"></a><span data-ttu-id="6ee3b-1708">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1708">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="6ee3b-1709">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1709">Parameters - OnLostFocus</span></span>

<span data-ttu-id="6ee3b-1710">sender</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1710">sender</span></span>  

<!-- -->

<span data-ttu-id="6ee3b-1711">e</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1711">e</span></span>  

## <a name="method-onenter"></a><span data-ttu-id="6ee3b-1712">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1712">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="6ee3b-1713">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1713">Parameters - OnEnter</span></span>

<span data-ttu-id="6ee3b-1714">sender</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1714">sender</span></span>  

<!-- -->

<span data-ttu-id="6ee3b-1715">e</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1715">e</span></span>  

## <a name="method-mouseleave"></a><span data-ttu-id="6ee3b-1716">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1716">Method mouseLeave</span></span>

<span data-ttu-id="6ee3b-1717">ユーザーがマウス ポインターをコントロールから離すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1717">Is called when the user moves the mouse pointer away from the control.</span></span>

```xpp
public void mouseLeave()
```

### <a name="remarks---mouseleave"></a><span data-ttu-id="6ee3b-1718">備考 - mouseLeave</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1718">Remarks - mouseLeave</span></span>

<span data-ttu-id="6ee3b-1719">コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、mouseLeave をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1719">You can override this method in a form group control by right-clicking the Methods node below the control, clicking Override Method, and then clicking mouseLeave.</span></span> <span data-ttu-id="6ee3b-1720">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1720">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-context"></a><span data-ttu-id="6ee3b-1721">メソッド context</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1721">Method context</span></span>

<span data-ttu-id="6ee3b-1722">ユーザーがフォーム グループ コントロールを右クリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1722">Is called when the user right-clicks a form group control.</span></span>

```xpp
public void context()
```

### <a name="remarks---context"></a><span data-ttu-id="6ee3b-1723">備考 - context</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1723">Remarks - context</span></span>

<span data-ttu-id="6ee3b-1724">コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、コンテキストをクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1724">You can override this method in a form group control by right-clicking the Methods node below the control, clicking Override Method, and then clicking context.</span></span> <span data-ttu-id="6ee3b-1725">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1725">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-copy"></a><span data-ttu-id="6ee3b-1726">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1726">Method copy</span></span>

<span data-ttu-id="6ee3b-1727">フォーム グループ コントロールをコピーします。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1727">Copies a form group control.</span></span>

```xpp
public void copy()
```

## <a name="method-cut"></a><span data-ttu-id="6ee3b-1728">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1728">Method cut</span></span>

<span data-ttu-id="6ee3b-1729">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1729">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-paste"></a><span data-ttu-id="6ee3b-1730">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1730">Method paste</span></span>

<span data-ttu-id="6ee3b-1731">フォーム グループ コントロールを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1731">Pastes a form group control.</span></span>

```xpp
public void paste()
```

## <a name="method-arrange"></a><span data-ttu-id="6ee3b-1732">メソッド arrange</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1732">Method arrange</span></span>

```xpp
public void arrange()
```

## <a name="method-clicked"></a><span data-ttu-id="6ee3b-1733">メソッド clicked</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1733">Method clicked</span></span>

<span data-ttu-id="6ee3b-1734">フォーム グループ コントロールがユーザーにクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1734">Is called when a form group control is clicked by the user.</span></span>

```xpp
public void clicked()
```

## <a name="method-onleaving"></a><span data-ttu-id="6ee3b-1735">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1735">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="6ee3b-1736">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1736">Parameters - OnLeaving</span></span>

<span data-ttu-id="6ee3b-1737">sender</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1737">sender</span></span>  

<!-- -->

<span data-ttu-id="6ee3b-1738">e</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1738">e</span></span>  

## <a name="method-inputsearch"></a><span data-ttu-id="6ee3b-1739">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1739">Method inputSearch</span></span>

<span data-ttu-id="6ee3b-1740">ユーザーがバインドされたコントロールに検索文字列を入力すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1740">Is called when the user enters a search string in a bound control.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="6ee3b-1741">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1741">Parameters - inputSearch</span></span>

<span data-ttu-id="6ee3b-1742">searchStr</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1742">searchStr</span></span>  
<span data-ttu-id="6ee3b-1743">検索テキストを含む文字列データ型; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1743">A String data type that contains search text; optional.</span></span>

### <a name="remarks---inputsearch"></a><span data-ttu-id="6ee3b-1744">備考 - inputSearch</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1744">Remarks - inputSearch</span></span>

<span data-ttu-id="6ee3b-1745">コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、inputSearch をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1745">You can override this method in a form group control by right-clicking the Methods node below the control, clicking Override Method, and then clicking inputSearch.</span></span> <span data-ttu-id="6ee3b-1746">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1746">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-resetusersetting"></a><span data-ttu-id="6ee3b-1747">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1747">Method resetUserSetting</span></span>

<span data-ttu-id="6ee3b-1748">フォーム グループ コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1748">Resets the user settings for a form group control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-onclicked"></a><span data-ttu-id="6ee3b-1749">メソッド OnClicked</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1749">Method OnClicked</span></span>

```xpp
private void OnClicked([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onclicked"></a><span data-ttu-id="6ee3b-1750">パラメーター - OnClicked</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1750">Parameters - OnClicked</span></span>

<span data-ttu-id="6ee3b-1751">sender</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1751">sender</span></span>  

<!-- -->

<span data-ttu-id="6ee3b-1752">e</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1752">e</span></span>  

## <a name="method-lostfocus"></a><span data-ttu-id="6ee3b-1753">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1753">Method lostFocus</span></span>

<span data-ttu-id="6ee3b-1754">ユーザーがフォーム グループ コントロールをフォーカス外に持っていくと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1754">Is called when the user brings a form group control out of focus.</span></span>

```xpp
public void lostFocus()
```

### <a name="remarks---lostfocus"></a><span data-ttu-id="6ee3b-1755">備考 - lostFocus</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1755">Remarks - lostFocus</span></span>

<span data-ttu-id="6ee3b-1756">コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、lostFocus をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1756">You can override this method in a form group control by right-clicking the Methods node below the control, clicking Override Method, and then clicking lostFocus.</span></span> <span data-ttu-id="6ee3b-1757">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」フォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1757">For information about best practices for forms and code, see the No Code in Forms form.</span></span>

## <a name="method-dropex"></a><span data-ttu-id="6ee3b-1758">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1758">Method dropEx</span></span>

<span data-ttu-id="6ee3b-1759">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1759">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="6ee3b-1760">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1760">Parameters - dropEx</span></span>

<span data-ttu-id="6ee3b-1761">dragSource</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1761">dragSource</span></span>  
<span data-ttu-id="6ee3b-1762">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1762">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1763">dragMode</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1763">dragMode</span></span>  
<span data-ttu-id="6ee3b-1764">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1764">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1765">x</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1765">x</span></span>  
<span data-ttu-id="6ee3b-1766">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1766">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1767">y</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1767">y</span></span>  
<span data-ttu-id="6ee3b-1768">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1768">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-enddrag"></a><span data-ttu-id="6ee3b-1769">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1769">Method endDrag</span></span>

<span data-ttu-id="6ee3b-1770">ユーザーがフォーム グループ コントロールの移動を終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1770">Is called when the user has finished moving a form group control.</span></span>

```xpp
public void endDrag()
```

## <a name="method-jumpref"></a><span data-ttu-id="6ee3b-1771">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1771">Method jumpRef</span></span>

<span data-ttu-id="6ee3b-1772">ユーザーがフォーム グループ コントロールのコントロール ショートカット メニューでメイン テーブルへ移動フォーム コマンドをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1772">Is called when a user clicks the Go to the Main Table Form command on a control shortcut menu in a form group control.</span></span>

```xpp
public void jumpRef()
```

## <a name="method-setfocus"></a><span data-ttu-id="6ee3b-1773">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1773">Method setFocus</span></span>

<span data-ttu-id="6ee3b-1774">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1774">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-filter"></a><span data-ttu-id="6ee3b-1775">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1775">Method filter</span></span>

<span data-ttu-id="6ee3b-1776">ユーザーがフォーム グループ コントロールを右クリックしてから選択フィルタをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1776">Is called when the user right-clicks a form group control and then clicks Filter By Selection.</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="6ee3b-1777">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1777">Parameters - filter</span></span>

<span data-ttu-id="6ee3b-1778">filterStr</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1778">filterStr</span></span>  
<span data-ttu-id="6ee3b-1779">フィルターのテキストを指定する文字列データ型; オプション。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1779">A String data type that specifies the text for the filter; optional.</span></span>

### <a name="remarks---filter"></a><span data-ttu-id="6ee3b-1780">備考 - filter</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1780">Remarks - filter</span></span>

<span data-ttu-id="6ee3b-1781">コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、filter をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1781">You can override this method in a form group control by right-clicking the Methods node below the control, clicking Override Method, and then clicking filter.</span></span> <span data-ttu-id="6ee3b-1782">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1782">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-displaycontrol"></a><span data-ttu-id="6ee3b-1783">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1783">Method displayControl</span></span>

<span data-ttu-id="6ee3b-1784">フォーム グループ コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1784">Displays a form group control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-gotfocus"></a><span data-ttu-id="6ee3b-1785">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1785">Method gotFocus</span></span>

<span data-ttu-id="6ee3b-1786">ユーザーがフォーム グループ コントロールにフォーカスを移すタイミングを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1786">Determines when the user brings a form group control into focus.</span></span>

```xpp
public void gotFocus()
```

### <a name="remarks---gotfocus"></a><span data-ttu-id="6ee3b-1787">備考 - gotFocus</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1787">Remarks - gotFocus</span></span>

<span data-ttu-id="6ee3b-1788">コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、gotFocus をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1788">You can override this method in a form group control by right-clicking the Methods node below the control, clicking Override Method, and then clicking gotFocus.</span></span> <span data-ttu-id="6ee3b-1789">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1789">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-prefcolumnsize"></a><span data-ttu-id="6ee3b-1790">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1790">Method prefColumnSize</span></span>

<span data-ttu-id="6ee3b-1791">フォーム グループ コントロールの列の高さと幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1791">Specifies the height and width of columns for a form group control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="6ee3b-1792">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1792">Parameters - prefColumnSize</span></span>

<span data-ttu-id="6ee3b-1793">width</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1793">width</span></span>  
<span data-ttu-id="6ee3b-1794">列の高さを指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1794">An integer value that specifies the height of columns.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1795">height</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1795">height</span></span>  
<span data-ttu-id="6ee3b-1796">列の高さを指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1796">An integer value that specifies the height of columns.</span></span>

## <a name="method-dragleave"></a><span data-ttu-id="6ee3b-1797">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1797">Method dragLeave</span></span>

<span data-ttu-id="6ee3b-1798">ユーザーがフォーム グループ コントロールの境界からオブジェクトをドラッグすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1798">Is called when the user drags an object out of the bounds of a form group control.</span></span>

```xpp
public void dragLeave()
```

### <a name="remarks---dragleave"></a><span data-ttu-id="6ee3b-1799">備考 - dragLeave</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1799">Remarks - dragLeave</span></span>

<span data-ttu-id="6ee3b-1800">コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、dragLeave をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1800">You can override this method in a form group control by right-clicking the Methods node below the control, clicking Override Method, and then clicking dragLeave.</span></span> <span data-ttu-id="6ee3b-1801">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1801">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-ongotfocus"></a><span data-ttu-id="6ee3b-1802">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1802">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="6ee3b-1803">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1803">Parameters - OnGotFocus</span></span>

<span data-ttu-id="6ee3b-1804">sender</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1804">sender</span></span>  

<!-- -->

<span data-ttu-id="6ee3b-1805">e</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1805">e</span></span>  

## <a name="method-enter"></a><span data-ttu-id="6ee3b-1806">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1806">Method enter</span></span>

<span data-ttu-id="6ee3b-1807">ユーザーがフォーム グループ コントロールにフォーカスを移動すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1807">Is called when the user moves focus to a form group control.</span></span>

```xpp
public void enter()
```

### <a name="remarks---enter"></a><span data-ttu-id="6ee3b-1808">備考 - enter</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1808">Remarks - enter</span></span>

<span data-ttu-id="6ee3b-1809">コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、enter をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1809">You can override this method in a form group control by right-clicking the Methods node below the control, clicking Override Method, and then clicking enter.</span></span> <span data-ttu-id="6ee3b-1810">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1810">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-mouseenter"></a><span data-ttu-id="6ee3b-1811">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1811">Method mouseEnter</span></span>

<span data-ttu-id="6ee3b-1812">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1812">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="6ee3b-1813">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1813">Parameters - mouseEnter</span></span>

<span data-ttu-id="6ee3b-1814">x</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1814">x</span></span>  
<span data-ttu-id="6ee3b-1815">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1815">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1816">y</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1816">y</span></span>  
<span data-ttu-id="6ee3b-1817">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1817">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1818">ボタン</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1818">button</span></span>  
<span data-ttu-id="6ee3b-1819">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1819">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1820">Ctrl</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1820">Ctrl</span></span>  
<span data-ttu-id="6ee3b-1821">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1821">A Boolean value that specifies whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6ee3b-1822">シフト</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1822">Shift</span></span>  
<span data-ttu-id="6ee3b-1823">Shift キーが押されているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1823">A Boolean value that specifies whether the SHIFT key is down.</span></span>

### <a name="remarks---mouseenter"></a><span data-ttu-id="6ee3b-1824">備考 - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1824">Remarks - mouseEnter</span></span>

<span data-ttu-id="6ee3b-1825">button パラメーターに指定できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1825">The following are the possible values for the button parameter.</span></span>

|     |                      |
|-----|----------------------|
| <span data-ttu-id="6ee3b-1826">1</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1826">1</span></span>   | <span data-ttu-id="6ee3b-1827">マウスの左ボタン</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1827">Left mouse button.</span></span>   |
| <span data-ttu-id="6ee3b-1828">2</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1828">2</span></span>   | <span data-ttu-id="6ee3b-1829">マウスの中央ボタン。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1829">Middle mouse button.</span></span> |
| <span data-ttu-id="6ee3b-1830">3</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1830">3</span></span>   | <span data-ttu-id="6ee3b-1831">マウスの右ボタン</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1831">Right mouse button.</span></span>  |

<span data-ttu-id="6ee3b-1832">コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、mouseEnter をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1832">You can override this method in a form group control by right-clicking the Methods node below the control, clicking Override Method, and then clicking mouseEnter.</span></span> <span data-ttu-id="6ee3b-1833">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ee3b-1833">For information about best practices for forms and code, see No Code in Forms.</span></span>

