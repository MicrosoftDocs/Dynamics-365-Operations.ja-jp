---
title: FormDropDialogButtonControl クラス
description: このトピックでは、FormDropDialogButtonControl クラスについて説明します。
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
ms.openlocfilehash: cf7e47aed9fd752579d177c0c7994ba1257f13d4
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502945"
---
# <a name="class-formdropdialogbuttoncontrol"></a><span data-ttu-id="9fd74-103">クラス FormDropDialogButtonControl</span><span class="sxs-lookup"><span data-stu-id="9fd74-103">Class FormDropDialogButtonControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormDropDialogButtonControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="9fd74-104">備考</span><span class="sxs-lookup"><span data-stu-id="9fd74-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="9fd74-105">例</span><span class="sxs-lookup"><span data-stu-id="9fd74-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="9fd74-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="9fd74-106">Methods</span></span>

| <span data-ttu-id="9fd74-107">方法</span><span class="sxs-lookup"><span data-stu-id="9fd74-107">Method</span></span>                                                                                                      | <span data-ttu-id="9fd74-108">説明</span><span class="sxs-lookup"><span data-stu-id="9fd74-108">Description</span></span>                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd74-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="9fd74-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-110">Determines whether to align the control.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="9fd74-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-111">public int alignment(\[int value\])</span></span>                                                                         | <span data-ttu-id="9fd74-112">コントロール内のテキストの配置を変更します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-112">Changes the alignment of the text in the control.</span></span> <span data-ttu-id="9fd74-113">値は左、右、または中央であり、コントロールを適切に揃えます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-113">Values are Left, right, or center, to align the control appropriately.</span></span>                                                                                              |
| <span data-ttu-id="9fd74-114">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-114">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="9fd74-115">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-115">Determines whether the user can change the contents of the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="9fd74-116">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="9fd74-116">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="9fd74-117">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-117">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                                                                   |
| <span data-ttu-id="9fd74-118">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-118">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="9fd74-119">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-119">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                                                                    |
| <span data-ttu-id="9fd74-120">public boolean autoRefreshData(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-120">public boolean autoRefreshData(\[boolean value\])</span></span>                                                           | <span data-ttu-id="9fd74-121">ボタンをクリックしたときに、コントロールに関連付けられているデータ ソースのデータを更新するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-121">Specifies whether the data from the data source that is associated with the control will be refreshed when the button is clicked.</span></span> <span data-ttu-id="9fd74-122">既定値はいいえです。</span><span class="sxs-lookup"><span data-stu-id="9fd74-122">The default value is No.</span></span>                                                            |
| <span data-ttu-id="9fd74-123">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-123">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="9fd74-124">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-124">Gets or sets the background color of the control.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="9fd74-125">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-125">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="9fd74-126">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-126">Determines whether the control background can be transparent.</span></span>                                                                                                                                                        |
| <span data-ttu-id="9fd74-127">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="9fd74-127">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="9fd74-128">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-128">Is called when the user starts to drag a form control.</span></span>                                                                                                                                                                |
| <span data-ttu-id="9fd74-129">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-129">public boolean big(\[boolean value\])</span></span>                                                                       |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-130">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-130">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="9fd74-131">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-131">Gets or sets the weight of font used to output text in the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="9fd74-132">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-132">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="9fd74-133">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-133">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                                                              |
| <span data-ttu-id="9fd74-134">public int buttonDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-134">public int buttonDisplay(\[int value\])</span></span>                                                                     | <span data-ttu-id="9fd74-135">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-135">Gets or sets the appearance of the button control.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="9fd74-136">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="9fd74-136">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="9fd74-137">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-137">Retrieves the size of the control.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="9fd74-138">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-138">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="9fd74-139">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-139">Gets or set the caption of the control.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="9fd74-140">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-140">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="9fd74-141">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-141">Gets or sets the character set of the font.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="9fd74-142">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-142">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="9fd74-143">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-143">Gets or sets the color scheme of the control.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="9fd74-144">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-144">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="9fd74-145">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-145">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="9fd74-146">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="9fd74-146">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="9fd74-147">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-147">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                                                                      |
| <span data-ttu-id="9fd74-148">public int copyCallerQuery(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-148">public int copyCallerQuery(\[int value\])</span></span>                                                                   | <span data-ttu-id="9fd74-149">ターゲット フォームへの呼び出し元のフォームからクエリをコピーするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-149">Specifies whether to copy the query from the calling form to the target form.</span></span> <span data-ttu-id="9fd74-150">これにより、ターゲット フォームは、元のフォームで表示されていたものと同じデータを照会できます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-150">This enables the target form to display the same data that was being viewed in the original form.</span></span> <span data-ttu-id="9fd74-151">既定値は自動です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-151">The default value is Auto.</span></span>            |
| <span data-ttu-id="9fd74-152">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-152">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="9fd74-153">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-153">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                                                                        |
| <span data-ttu-id="9fd74-154">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-154">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 | <span data-ttu-id="9fd74-155">国のコンテキストを識別するために使用されるフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-155">Specifies the field that will be used to identify the country context.</span></span> <span data-ttu-id="9fd74-156">CountryRegionCodes を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9fd74-156">See CountryRegionCodes.</span></span>                                                                                                                        |
| <span data-ttu-id="9fd74-157">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-157">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="9fd74-158">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-158">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                                                                         |
| <span data-ttu-id="9fd74-159">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-159">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="9fd74-160">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-160">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                                                                     |
| <span data-ttu-id="9fd74-161">public boolean defaultButton(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-161">public boolean defaultButton(\[boolean value\])</span></span>                                                             | <span data-ttu-id="9fd74-162">ボタンをフォームの既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-162">Determines whether the button should be the default button in the form.</span></span>                                                                                                                                               |
| <span data-ttu-id="9fd74-163">public str disabledImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-163">public str disabledImage(\[str value\])</span></span>                                                                     | <span data-ttu-id="9fd74-164">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-164">Gets or sets the disabled image of the button.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="9fd74-165">public int disabledImageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-165">public int disabledImageLocation(\[int value\])</span></span>                                                             |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-166">public int disabledResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-166">public int disabledResource(\[int value\])</span></span>                                                                  | <span data-ttu-id="9fd74-167">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-167">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>                                                                                                                                        |
| <span data-ttu-id="9fd74-168">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-168">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="9fd74-169">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-169">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>                                               |
| <span data-ttu-id="9fd74-170">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-170">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="9fd74-171">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-171">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                                                                     |
| <span data-ttu-id="9fd74-172">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="9fd74-172">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="9fd74-173">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-173">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                                                                        |
| <span data-ttu-id="9fd74-174">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="9fd74-174">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="9fd74-175">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-175">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                                                                      |
| <span data-ttu-id="9fd74-176">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="9fd74-176">public str dragText()</span></span>                                                                                       | <span data-ttu-id="9fd74-177">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-177">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                                                                |
| <span data-ttu-id="9fd74-178">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-178">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="9fd74-179">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-179">Determines whether to enable or disable the object.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="9fd74-180">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-180">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="9fd74-181">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-181">Gets or sets the name of the font for the control to use.</span></span>                                                                                                                                                             |
| <span data-ttu-id="9fd74-182">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-182">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="9fd74-183">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-183">Gets or sets the size of the font for the control to use.</span></span>                                                                                                                                                             |
| <span data-ttu-id="9fd74-184">public boolean forcedToOverflow(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-184">public boolean forcedToOverflow(\[boolean value\])</span></span>                                                          |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-185">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-185">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="9fd74-186">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-186">Gets or sets the text color for the control to use.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="9fd74-187">public int formViewOption(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-187">public int formViewOption(\[int value\])</span></span>                                                                    | <span data-ttu-id="9fd74-188">使用するフォーム モードを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-188">Specifies the form mode to use.</span></span> <span data-ttu-id="9fd74-189">オプションには、[自動]、[グリッド]、および [詳細] が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-189">Options include Auto, Grid, and Details.</span></span> <span data-ttu-id="9fd74-190">既定は自動です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-190">The default is Auto.</span></span>                                                                                                                         |
| <span data-ttu-id="9fd74-191">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-191">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="9fd74-192">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-192">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                                                              |
| <span data-ttu-id="9fd74-193">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="9fd74-193">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="9fd74-194">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-194">Indicates whether the control has custom user settings.</span></span>                                                                                                                                                               |
| <span data-ttu-id="9fd74-195">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-195">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="9fd74-196">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-196">Gets or sets the height of the control.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="9fd74-197">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-197">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="9fd74-198">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-198">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                                                                        |
| <span data-ttu-id="9fd74-199">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-199">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="9fd74-200">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-200">Gets or sets the height of the control.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="9fd74-201">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="9fd74-201">public str helpField()</span></span>                                                                                      | <span data-ttu-id="9fd74-202">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-202">Retrieves the Help text for the control.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="9fd74-203">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-203">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="9fd74-204">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-204">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                                                              |
| <span data-ttu-id="9fd74-205">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-205">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="9fd74-206">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-206">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                                                                       |
| <span data-ttu-id="9fd74-207">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="9fd74-207">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="9fd74-208">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-208">Retrieves the Windows handle for the control.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="9fd74-209">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-209">public int imageLocation(\[int value\])</span></span>                                                                     |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-210">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="9fd74-210">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-211">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="9fd74-211">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="9fd74-212">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-212">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                                                                    |
| <span data-ttu-id="9fd74-213">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="9fd74-213">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="9fd74-214">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-214">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                                                                   |
| <span data-ttu-id="9fd74-215">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="9fd74-215">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="9fd74-216">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-216">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                                                                 |
| <span data-ttu-id="9fd74-217">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-217">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-218">public str keyTip(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-218">public str keyTip(\[str value\])</span></span>                                                                            |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-219">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-219">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="9fd74-220">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-220">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                                                                      |
| <span data-ttu-id="9fd74-221">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-221">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="9fd74-222">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-222">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                                                                         |
| <span data-ttu-id="9fd74-223">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-223">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="9fd74-224">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-224">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                                                                      |
| <span data-ttu-id="9fd74-225">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-225">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="9fd74-226">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="9fd74-226">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="9fd74-227">public xMenuFunction menufunction()</span><span class="sxs-lookup"><span data-stu-id="9fd74-227">public xMenuFunction menufunction()</span></span>                                                                         |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-228">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-228">public str menuItemName(\[str value\])</span></span>                                                                      | <span data-ttu-id="9fd74-229">DropDialogButton コントロールに対して実行されるメニュー項目を決定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-229">Determines which menu item is run for a DropDialogButton control.</span></span>                                                                                                                                                     |
| <span data-ttu-id="9fd74-230">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="9fd74-230">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="9fd74-231">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-231">Is called when the control is double-clicked by the user.</span></span>                                                                                                                                                             |
| <span data-ttu-id="9fd74-232">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="9fd74-232">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="9fd74-233">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-233">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                                                                     |
| <span data-ttu-id="9fd74-234">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="9fd74-234">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="9fd74-235">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-235">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                                                                     |
| <span data-ttu-id="9fd74-236">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="9fd74-236">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="9fd74-237">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-237">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                                                              |
| <span data-ttu-id="9fd74-238">public int multiSelect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-238">public int multiSelect(\[int value\])</span></span>                                                                       |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-239">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-239">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="9fd74-240">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-240">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                                                               |
| <span data-ttu-id="9fd74-241">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-241">public int neededPermission(\[int value\])</span></span>                                                                  | <span data-ttu-id="9fd74-242">コントロールへのアクセスを許可するために必要な最小限のアクセス許可レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-242">Specifies the minimum permission level that is required to be allowed access to the control.</span></span>                                                                                                                          |
| <span data-ttu-id="9fd74-243">public int needsRecord(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-243">public int needsRecord(\[int value\])</span></span>                                                                       | <span data-ttu-id="9fd74-244">レコードが存在しない場合、ボタンを有効にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-244">Specifies whether a button is enabled if no record is present.</span></span> <span data-ttu-id="9fd74-245">既定値はいいえです。</span><span class="sxs-lookup"><span data-stu-id="9fd74-245">The default value is No.</span></span>                                                                                                                               |
| <span data-ttu-id="9fd74-246">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-246">public str normalImage(\[str value\])</span></span>                                                                       |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-247">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-247">public int normalResource(\[int value\])</span></span>                                                                    |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-248">public int openMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-248">public int openMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="9fd74-249">ターゲット フォームの表示モードを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-249">Specifies the view mode of the target form.</span></span> <span data-ttu-id="9fd74-250">使用可能な値には、Auto、View、Edit、および New が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-250">The possible values include Auto, View, Edit, and New.</span></span> <span data-ttu-id="9fd74-251">既定は自動です。このプロパティを使用して、ターゲット フォームを編集モードまたは読み取り専用モードのいずれで開くかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-251">The default is Auto. You may use this property to specify whether the target form opens in edit or read-only mode.</span></span> |
| <span data-ttu-id="9fd74-252">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="9fd74-252">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-253">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-253">public str parameters(\[str value\])</span></span>                                                                        | <span data-ttu-id="9fd74-254">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-254">Gets or sets the list of parameters that are passed to objects taht are run by the MenuFunction class.</span></span>                                                                                                                |
| <span data-ttu-id="9fd74-255">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="9fd74-255">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="9fd74-256">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-256">Retrieves the parent control for the control.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="9fd74-257">public boolean primary(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-257">public boolean primary(\[boolean value\])</span></span>                                                                   |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-258">public boolean saveRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-258">public boolean saveRecord(\[boolean value\])</span></span>                                                                |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-259">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-259">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="9fd74-260">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-260">Sets or returns the ID of the security key for the control.</span></span>                                                                                                                                                           |
| <span data-ttu-id="9fd74-261">public boolean sendExternalContext(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-261">public boolean sendExternalContext(\[boolean value\])</span></span>                                                       | <span data-ttu-id="9fd74-262">このフォームの外部レコード コンテキストをメニュー項目の外部レコード コンテキストとして使用するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-262">Specifies whether the external record context of this form should be used as the menu item external record context.</span></span> <span data-ttu-id="9fd74-263">既定値はいいえです。</span><span class="sxs-lookup"><span data-stu-id="9fd74-263">The default value is No.</span></span>                                                                          |
| <span data-ttu-id="9fd74-264">public int shortkey(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-264">public int shortkey(\[int value\])</span></span>                                                                          |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-265">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="9fd74-265">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="9fd74-266">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-266">Shows the shortcut menu for the control.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="9fd74-267">public boolean showShortCut(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-267">public boolean showShortCut(\[boolean value\])</span></span>                                                              |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-268">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-268">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="9fd74-269">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-269">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                                                                       |
| <span data-ttu-id="9fd74-270">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-270">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-271">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-271">public int style(\[int value\])</span></span>                                                                             | <span data-ttu-id="9fd74-272">フォームのスタイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-272">Specifies the style of the form.</span></span> <span data-ttu-id="9fd74-273">このプロパティは、フォームで使用されているフォーム設計パターンを制御します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-273">This property controls the form design pattern being used with the form.</span></span> <span data-ttu-id="9fd74-274">既定は自動です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-274">The default is Auto.</span></span>                                                                                        |
| <span data-ttu-id="9fd74-275">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-275">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-276">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="9fd74-276">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="9fd74-277">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-277">Retrieves the tooltip text for the control.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="9fd74-278">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-278">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="9fd74-279">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-279">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                                                                        |
| <span data-ttu-id="9fd74-280">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-280">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="9fd74-281">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-281">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                                                                           |
| <span data-ttu-id="9fd74-282">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-282">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="9fd74-283">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-283">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                                                                        |
| <span data-ttu-id="9fd74-284">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-284">public int type(\[int value\])</span></span>                                                                              | <span data-ttu-id="9fd74-285">コントロールのタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-285">Specifies the type of the control.</span></span> <span data-ttu-id="9fd74-286">読み取り専用。</span><span class="sxs-lookup"><span data-stu-id="9fd74-286">Read-only.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="9fd74-287">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-287">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-288">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="9fd74-288">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-289">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-289">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="9fd74-290">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-290">Gets or sets the user data for the control.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="9fd74-291">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-291">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="9fd74-292">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-292">Gets or sets the user data item for the control.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="9fd74-293">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-293">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="9fd74-294">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-294">Gets or sets the number of user data items for the control.</span></span>                                                                                                                                                           |
| <span data-ttu-id="9fd74-295">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-295">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="9fd74-296">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-296">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                                                                   |
| <span data-ttu-id="9fd74-297">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-297">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="9fd74-298">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-298">Gets or sets the custom user height for the control.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="9fd74-299">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-299">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="9fd74-300">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-300">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                                                                    |
| <span data-ttu-id="9fd74-301">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-301">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="9fd74-302">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-302">Gets or sets the organization container for the control.</span></span>                                                                                                                                                              |
| <span data-ttu-id="9fd74-303">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-303">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="9fd74-304">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-304">Gets or sets the organization sibling for the control.</span></span>                                                                                                                                                                |
| <span data-ttu-id="9fd74-305">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-305">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="9fd74-306">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-306">Gets or sets the user label text for the control.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="9fd74-307">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-307">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="9fd74-308">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-308">Gets or sets the user security level for the control.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="9fd74-309">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-309">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="9fd74-310">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-310">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                                                                  |
| <span data-ttu-id="9fd74-311">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-311">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="9fd74-312">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-312">Sets or returns the width of the control in pixels.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="9fd74-313">public boolean value(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-313">public boolean value(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-314">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-314">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="9fd74-315">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-315">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                                                                         |
| <span data-ttu-id="9fd74-316">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-316">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="9fd74-317">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-317">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                                                                           |
| <span data-ttu-id="9fd74-318">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-318">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="9fd74-319">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-319">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                                                                         |
| <span data-ttu-id="9fd74-320">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-320">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="9fd74-321">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-321">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                                                                |
| <span data-ttu-id="9fd74-322">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-322">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="9fd74-323">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-323">Gets or sets the width of the control.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="9fd74-324">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-324">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="9fd74-325">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-325">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                                                                        |
| <span data-ttu-id="9fd74-326">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-326">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="9fd74-327">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-327">Gets or sets the width of the control.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="9fd74-328">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="9fd74-328">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="9fd74-329">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-329">Indicates that the control has received focus.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="9fd74-330">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="9fd74-330">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="9fd74-331">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-331">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                                                               |
| <span data-ttu-id="9fd74-332">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-332">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-333">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="9fd74-333">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="9fd74-334">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-334">Specifies the preferred column width and height for the form control.</span></span>                                                                                                                                                 |
| <span data-ttu-id="9fd74-335">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="9fd74-335">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="9fd74-336">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-336">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                                                                    |
| <span data-ttu-id="9fd74-337">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="9fd74-337">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="9fd74-338">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-338">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                                                                |
| <span data-ttu-id="9fd74-339">private void OnDialogClosed(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-339">private void OnDialogClosed(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                             |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-340">public void clicked()</span><span class="sxs-lookup"><span data-stu-id="9fd74-340">public void clicked()</span></span>                                                                                       |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-341">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-341">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-342">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="9fd74-342">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="9fd74-343">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-343">Indicates that the control has lost focus.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="9fd74-344">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="9fd74-344">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-345">public void context()</span><span class="sxs-lookup"><span data-stu-id="9fd74-345">public void context()</span></span>                                                                                       | <span data-ttu-id="9fd74-346">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-346">Shows the shortcut menu for the control.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="9fd74-347">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="9fd74-347">public void displayControl()</span></span>                                                                                | <span data-ttu-id="9fd74-348">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-348">Displays the control.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="9fd74-349">public void dialogClosed(xFormRun formRun)</span><span class="sxs-lookup"><span data-stu-id="9fd74-349">public void dialogClosed(xFormRun formRun)</span></span>                                                                  |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-350">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="9fd74-350">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="9fd74-351">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-351">Is called when the user has finished dragging a form control.</span></span>                                                                                                                                                         |
| <span data-ttu-id="9fd74-352">public void dialogInitialized(xFormRun formRun)</span><span class="sxs-lookup"><span data-stu-id="9fd74-352">public void dialogInitialized(xFormRun formRun)</span></span>                                                             |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-353">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-353">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-354">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="9fd74-354">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="9fd74-355">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-355">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                                                                  |
| <span data-ttu-id="9fd74-356">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-356">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                                                                       |
| <span data-ttu-id="9fd74-357">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="9fd74-357">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="9fd74-358">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="9fd74-358">Resets the user settings for the control.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="9fd74-359">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="9fd74-359">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="9fd74-360">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-360">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                                                                |
| <span data-ttu-id="9fd74-361">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="9fd74-361">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="9fd74-362">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-362">Sets the focus on the control.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="9fd74-363">public void cut()</span><span class="sxs-lookup"><span data-stu-id="9fd74-363">public void cut()</span></span>                                                                                           | <span data-ttu-id="9fd74-364">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="9fd74-364">Cuts the contents of the control.</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="9fd74-365">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="9fd74-365">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="9fd74-366">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-366">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                                                                      |
| <span data-ttu-id="9fd74-367">public void paste()</span><span class="sxs-lookup"><span data-stu-id="9fd74-367">public void paste()</span></span>                                                                                         | <span data-ttu-id="9fd74-368">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-368">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                                                                |
| <span data-ttu-id="9fd74-369">public void copy()</span><span class="sxs-lookup"><span data-stu-id="9fd74-369">public void copy()</span></span>                                                                                          | <span data-ttu-id="9fd74-370">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="9fd74-370">Copies the contents of the control to the clipboard.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="9fd74-371">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="9fd74-371">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                                                                       |

## <a name="method-aligncontrol"></a><span data-ttu-id="9fd74-372">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="9fd74-372">Method alignControl</span></span>

<span data-ttu-id="9fd74-373">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-373">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="9fd74-374">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="9fd74-374">Parameters - alignControl</span></span>

<span data-ttu-id="9fd74-375">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-375">value</span></span>  
<span data-ttu-id="9fd74-376">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9fd74-376">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="9fd74-377">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="9fd74-377">Return Value - alignControl</span></span>

<span data-ttu-id="9fd74-378">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="9fd74-378">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="9fd74-379">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="9fd74-379">Remarks - alignControl</span></span>

<span data-ttu-id="9fd74-380">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-380">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="9fd74-381">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="9fd74-381">Method alignment</span></span>

<span data-ttu-id="9fd74-382">コントロール内のテキストの配置を変更します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-382">Changes the alignment of the text in the control.</span></span> <span data-ttu-id="9fd74-383">値は左、右、または中央であり、コントロールを適切に揃えます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-383">Values are Left, right, or center, to align the control appropriately.</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="9fd74-384">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="9fd74-384">Parameters - alignment</span></span>

<span data-ttu-id="9fd74-385">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-385">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="9fd74-386">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="9fd74-386">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="9fd74-387">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="9fd74-387">Method allowEdit</span></span>

<span data-ttu-id="9fd74-388">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-388">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="9fd74-389">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="9fd74-389">Parameters - allowEdit</span></span>

<span data-ttu-id="9fd74-390">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-390">value</span></span>  
<span data-ttu-id="9fd74-391">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-391">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="9fd74-392">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="9fd74-392">Return Value - allowEdit</span></span>

<span data-ttu-id="9fd74-393">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="9fd74-393">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="9fd74-394">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="9fd74-394">Remarks - allowEdit</span></span>

<span data-ttu-id="9fd74-395">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="9fd74-395">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="9fd74-396">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="9fd74-396">Method allowSysSetup</span></span>

<span data-ttu-id="9fd74-397">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-397">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="9fd74-398">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="9fd74-398">Return Value - allowSysSetup</span></span>

<span data-ttu-id="9fd74-399">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="9fd74-399">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="9fd74-400">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="9fd74-400">Method autoDeclaration</span></span>

<span data-ttu-id="9fd74-401">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-401">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="9fd74-402">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="9fd74-402">Parameters - autoDeclaration</span></span>

<span data-ttu-id="9fd74-403">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-403">value</span></span>  
<span data-ttu-id="9fd74-404">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9fd74-404">The new value of the property; optional.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="9fd74-405">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="9fd74-405">Return Value - autoDeclaration</span></span>

<span data-ttu-id="9fd74-406">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="9fd74-406">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="9fd74-407">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="9fd74-407">Remarks - autoDeclaration</span></span>

<span data-ttu-id="9fd74-408">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="9fd74-408">Controls cannot have identical names.</span></span>

## <a name="method-autorefreshdata"></a><span data-ttu-id="9fd74-409">メソッド autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="9fd74-409">Method autoRefreshData</span></span>

<span data-ttu-id="9fd74-410">ボタンをクリックしたときに、コントロールに関連付けられているデータ ソースのデータを更新するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-410">Specifies whether the data from the data source that is associated with the control will be refreshed when the button is clicked.</span></span> <span data-ttu-id="9fd74-411">既定値はいいえです。</span><span class="sxs-lookup"><span data-stu-id="9fd74-411">The default value is No.</span></span>

```xpp
public boolean autoRefreshData([boolean value])
```

### <a name="parameters---autorefreshdata"></a><span data-ttu-id="9fd74-412">パラメーター - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="9fd74-412">Parameters - autoRefreshData</span></span>

<span data-ttu-id="9fd74-413">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-413">value</span></span>  

### <a name="return-value---autorefreshdata"></a><span data-ttu-id="9fd74-414">戻り値 - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="9fd74-414">Return Value - autoRefreshData</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="9fd74-415">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="9fd74-415">Method backgroundColor</span></span>

<span data-ttu-id="9fd74-416">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-416">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="9fd74-417">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="9fd74-417">Parameters - backgroundColor</span></span>

<span data-ttu-id="9fd74-418">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-418">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="9fd74-419">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="9fd74-419">Return Value - backgroundColor</span></span>

<span data-ttu-id="9fd74-420">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="9fd74-420">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="9fd74-421">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="9fd74-421">Remarks - backgroundColor</span></span>

<span data-ttu-id="9fd74-422">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-422">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="9fd74-423">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9fd74-423">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="9fd74-424">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="9fd74-424">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="9fd74-425">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="9fd74-425">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="9fd74-426">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="9fd74-426">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="9fd74-427">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-427">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="9fd74-428">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="9fd74-428">Method backStyle</span></span>

<span data-ttu-id="9fd74-429">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-429">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="9fd74-430">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="9fd74-430">Parameters - backStyle</span></span>

<span data-ttu-id="9fd74-431">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-431">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="9fd74-432">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="9fd74-432">Return Value - backStyle</span></span>

<span data-ttu-id="9fd74-433">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-433">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="9fd74-434">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="9fd74-434">Method beginDrag</span></span>

<span data-ttu-id="9fd74-435">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-435">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="9fd74-436">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="9fd74-436">Parameters - beginDrag</span></span>

<span data-ttu-id="9fd74-437">x</span><span class="sxs-lookup"><span data-stu-id="9fd74-437">x</span></span>  
<span data-ttu-id="9fd74-438">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-438">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="9fd74-439">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="9fd74-439">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="9fd74-440">y</span><span class="sxs-lookup"><span data-stu-id="9fd74-440">y</span></span>  
<span data-ttu-id="9fd74-441">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-441">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="9fd74-442">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="9fd74-442">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="9fd74-443">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="9fd74-443">Return Value - beginDrag</span></span>

<span data-ttu-id="9fd74-444">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-444">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="9fd74-445">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="9fd74-445">Remarks - beginDrag</span></span>

<span data-ttu-id="9fd74-446">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="9fd74-446">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="9fd74-447">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-447">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-big"></a><span data-ttu-id="9fd74-448">メソッド big</span><span class="sxs-lookup"><span data-stu-id="9fd74-448">Method big</span></span>

```xpp
public boolean big([boolean value])
```

### <a name="parameters---big"></a><span data-ttu-id="9fd74-449">パラメーター - big</span><span class="sxs-lookup"><span data-stu-id="9fd74-449">Parameters - big</span></span>

<span data-ttu-id="9fd74-450">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-450">value</span></span>  

### <a name="return-value---big"></a><span data-ttu-id="9fd74-451">戻り値 - big</span><span class="sxs-lookup"><span data-stu-id="9fd74-451">Return Value - big</span></span>

## <a name="method-bold"></a><span data-ttu-id="9fd74-452">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="9fd74-452">Method bold</span></span>

<span data-ttu-id="9fd74-453">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-453">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="9fd74-454">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="9fd74-454">Parameters - bold</span></span>

<span data-ttu-id="9fd74-455">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-455">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="9fd74-456">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="9fd74-456">Return Value - bold</span></span>

<span data-ttu-id="9fd74-457">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-457">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="9fd74-458">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="9fd74-458">Remarks - bold</span></span>

<span data-ttu-id="9fd74-459">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-459">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="9fd74-460">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-460">0 Use the default font weight.</span></span>
-   <span data-ttu-id="9fd74-461">1 シン。</span><span class="sxs-lookup"><span data-stu-id="9fd74-461">1 Thin.</span></span>
-   <span data-ttu-id="9fd74-462">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="9fd74-462">2 Extra-light.</span></span>
-   <span data-ttu-id="9fd74-463">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="9fd74-463">3 Light.</span></span>
-   <span data-ttu-id="9fd74-464">4 標準。</span><span class="sxs-lookup"><span data-stu-id="9fd74-464">4 Normal.</span></span>
-   <span data-ttu-id="9fd74-465">5 中。</span><span class="sxs-lookup"><span data-stu-id="9fd74-465">5 Medium.</span></span>
-   <span data-ttu-id="9fd74-466">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="9fd74-466">6 Semibold.</span></span>
-   <span data-ttu-id="9fd74-467">7 太字。</span><span class="sxs-lookup"><span data-stu-id="9fd74-467">7 Bold.</span></span>
-   <span data-ttu-id="9fd74-468">8 極太。</span><span class="sxs-lookup"><span data-stu-id="9fd74-468">8 Extra-bold.</span></span>
-   <span data-ttu-id="9fd74-469">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="9fd74-469">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="9fd74-470">メソッド border</span><span class="sxs-lookup"><span data-stu-id="9fd74-470">Method border</span></span>

<span data-ttu-id="9fd74-471">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-471">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="9fd74-472">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="9fd74-472">Parameters - border</span></span>

<span data-ttu-id="9fd74-473">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-473">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="9fd74-474">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="9fd74-474">Return Value - border</span></span>

<span data-ttu-id="9fd74-475">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="9fd74-475">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="9fd74-476">備考 - border</span><span class="sxs-lookup"><span data-stu-id="9fd74-476">Remarks - border</span></span>

<span data-ttu-id="9fd74-477">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-477">The integer that is returned contains the style of the borderline of the control as follows.</span></span>

| <span data-ttu-id="9fd74-478">値です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-478">Value.</span></span> | <span data-ttu-id="9fd74-479">説明。</span><span class="sxs-lookup"><span data-stu-id="9fd74-479">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="9fd74-480">0</span><span class="sxs-lookup"><span data-stu-id="9fd74-480">0</span></span>      | <span data-ttu-id="9fd74-481">自動。</span><span class="sxs-lookup"><span data-stu-id="9fd74-481">Auto.</span></span>        |
| <span data-ttu-id="9fd74-482">1</span><span class="sxs-lookup"><span data-stu-id="9fd74-482">1</span></span>      | <span data-ttu-id="9fd74-483">3D。</span><span class="sxs-lookup"><span data-stu-id="9fd74-483">3D.</span></span>          |
| <span data-ttu-id="9fd74-484">2</span><span class="sxs-lookup"><span data-stu-id="9fd74-484">2</span></span>      | <span data-ttu-id="9fd74-485">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="9fd74-485">Single line.</span></span> |
| <span data-ttu-id="9fd74-486">3</span><span class="sxs-lookup"><span data-stu-id="9fd74-486">3</span></span>      | <span data-ttu-id="9fd74-487">均一。</span><span class="sxs-lookup"><span data-stu-id="9fd74-487">Flat.</span></span>        |
| <span data-ttu-id="9fd74-488">4</span><span class="sxs-lookup"><span data-stu-id="9fd74-488">4</span></span>      | <span data-ttu-id="9fd74-489">なし。</span><span class="sxs-lookup"><span data-stu-id="9fd74-489">None.</span></span>        |

## <a name="method-buttondisplay"></a><span data-ttu-id="9fd74-490">メソッド buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="9fd74-490">Method buttonDisplay</span></span>

<span data-ttu-id="9fd74-491">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-491">Gets or sets the appearance of the button control.</span></span>

```xpp
public int buttonDisplay([int value])
```

### <a name="parameters---buttondisplay"></a><span data-ttu-id="9fd74-492">パラメーター - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="9fd74-492">Parameters - buttonDisplay</span></span>

<span data-ttu-id="9fd74-493">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-493">value</span></span>  

### <a name="return-value---buttondisplay"></a><span data-ttu-id="9fd74-494">戻り値 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="9fd74-494">Return Value - buttonDisplay</span></span>

<span data-ttu-id="9fd74-495">ゼロから 5 までの整数。</span><span class="sxs-lookup"><span data-stu-id="9fd74-495">An integer between zero and five, inclusive.</span></span>

### <a name="remarks---buttondisplay"></a><span data-ttu-id="9fd74-496">備考 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="9fd74-496">Remarks - buttonDisplay</span></span>

<span data-ttu-id="9fd74-497">プロパティ値は、テキスト、画像、またはその両方のいずれをボタンに表示するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-497">The value of the property defines whether the text, the image, or both should be displayed on the button.</span></span> <span data-ttu-id="9fd74-498">このプロパティは、テキストと画像の両方が表示されている場合は、テキストと画像の相対位置も制御します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-498">This property also controls relative positions of text and image if both are displayed.</span></span> <span data-ttu-id="9fd74-499">返される整数値には、次のようなボタン コントロールの外観が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-499">The integer value that is returned contains the appearance of the button control as follows.</span></span>

| <span data-ttu-id="9fd74-500">値です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-500">Value.</span></span> | <span data-ttu-id="9fd74-501">説明。</span><span class="sxs-lookup"><span data-stu-id="9fd74-501">Description.</span></span>                                                     |
|--------|------------------------------------------------------------------|
| <span data-ttu-id="9fd74-502">0</span><span class="sxs-lookup"><span data-stu-id="9fd74-502">0</span></span>      | <span data-ttu-id="9fd74-503">テキストのみ。</span><span class="sxs-lookup"><span data-stu-id="9fd74-503">Text only.</span></span>                                                       |
| <span data-ttu-id="9fd74-504">1</span><span class="sxs-lookup"><span data-stu-id="9fd74-504">1</span></span>      | <span data-ttu-id="9fd74-505">イメージのみ。</span><span class="sxs-lookup"><span data-stu-id="9fd74-505">Image Only.</span></span>                                                      |
| <span data-ttu-id="9fd74-506">2</span><span class="sxs-lookup"><span data-stu-id="9fd74-506">2</span></span>      | <span data-ttu-id="9fd74-507">テキストと画像。画像はテキストの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-507">Text and image; the image is displayed below the text.</span></span>           |
| <span data-ttu-id="9fd74-508">3</span><span class="sxs-lookup"><span data-stu-id="9fd74-508">3</span></span>      | <span data-ttu-id="9fd74-509">テキストと画像。画像はテキストの上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-509">Text and image; the image is displayed above the text.</span></span>           |
| <span data-ttu-id="9fd74-510">4</span><span class="sxs-lookup"><span data-stu-id="9fd74-510">4</span></span>      | <span data-ttu-id="9fd74-511">テキストと画像。画像はテキストの左に表示されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-511">Text and image; the image is displayed to the left of the text.</span></span>  |
| <span data-ttu-id="9fd74-512">5</span><span class="sxs-lookup"><span data-stu-id="9fd74-512">5</span></span>      | <span data-ttu-id="9fd74-513">テキストと画像。画像はテキストの右に表示されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-513">Text and image; the image is displayed to the right of the text.</span></span> |

## <a name="method-calccontrolsize"></a><span data-ttu-id="9fd74-514">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="9fd74-514">Method calcControlSize</span></span>

<span data-ttu-id="9fd74-515">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-515">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="9fd74-516">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="9fd74-516">Parameters - calcControlSize</span></span>

<span data-ttu-id="9fd74-517">chars</span><span class="sxs-lookup"><span data-stu-id="9fd74-517">chars</span></span>  
<span data-ttu-id="9fd74-518">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="9fd74-518">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="9fd74-519">明細行</span><span class="sxs-lookup"><span data-stu-id="9fd74-519">lines</span></span>  
<span data-ttu-id="9fd74-520">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="9fd74-520">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="9fd74-521">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="9fd74-521">Return Value - calcControlSize</span></span>

<span data-ttu-id="9fd74-522">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="9fd74-522">The container that holds the width and height.</span></span>

## <a name="method-caption"></a><span data-ttu-id="9fd74-523">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="9fd74-523">Method caption</span></span>

<span data-ttu-id="9fd74-524">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-524">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="9fd74-525">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="9fd74-525">Parameters - caption</span></span>

<span data-ttu-id="9fd74-526">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-526">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="9fd74-527">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="9fd74-527">Return Value - caption</span></span>

<span data-ttu-id="9fd74-528">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="9fd74-528">The string that is used as the caption of the control.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="9fd74-529">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="9fd74-529">Method characterSet</span></span>

<span data-ttu-id="9fd74-530">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-530">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="9fd74-531">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="9fd74-531">Parameters - characterSet</span></span>

<span data-ttu-id="9fd74-532">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-532">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="9fd74-533">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="9fd74-533">Return Value - characterSet</span></span>

<span data-ttu-id="9fd74-534">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-534">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="9fd74-535">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="9fd74-535">Remarks - characterSet</span></span>

<span data-ttu-id="9fd74-536">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-536">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="9fd74-537">値です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-537">Value.</span></span> | <span data-ttu-id="9fd74-538">説明。</span><span class="sxs-lookup"><span data-stu-id="9fd74-538">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="9fd74-539">0</span><span class="sxs-lookup"><span data-stu-id="9fd74-539">0</span></span>      | <span data-ttu-id="9fd74-540">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="9fd74-540">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="9fd74-541">1</span><span class="sxs-lookup"><span data-stu-id="9fd74-541">1</span></span>      | <span data-ttu-id="9fd74-542">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="9fd74-542">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="9fd74-543">2</span><span class="sxs-lookup"><span data-stu-id="9fd74-543">2</span></span>      | <span data-ttu-id="9fd74-544">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="9fd74-544">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="9fd74-545">77</span><span class="sxs-lookup"><span data-stu-id="9fd74-545">77</span></span>     | <span data-ttu-id="9fd74-546">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="9fd74-546">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="9fd74-547">128</span><span class="sxs-lookup"><span data-stu-id="9fd74-547">128</span></span>    | <span data-ttu-id="9fd74-548">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="9fd74-548">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="9fd74-549">129</span><span class="sxs-lookup"><span data-stu-id="9fd74-549">129</span></span>    | <span data-ttu-id="9fd74-550">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="9fd74-550">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="9fd74-551">134</span><span class="sxs-lookup"><span data-stu-id="9fd74-551">134</span></span>    | <span data-ttu-id="9fd74-552">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="9fd74-552">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="9fd74-553">136</span><span class="sxs-lookup"><span data-stu-id="9fd74-553">136</span></span>    | <span data-ttu-id="9fd74-554">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="9fd74-554">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="9fd74-555">161</span><span class="sxs-lookup"><span data-stu-id="9fd74-555">161</span></span>    | <span data-ttu-id="9fd74-556">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="9fd74-556">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="9fd74-557">162</span><span class="sxs-lookup"><span data-stu-id="9fd74-557">162</span></span>    | <span data-ttu-id="9fd74-558">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="9fd74-558">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="9fd74-559">163</span><span class="sxs-lookup"><span data-stu-id="9fd74-559">163</span></span>    | <span data-ttu-id="9fd74-560">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="9fd74-560">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="9fd74-561">186</span><span class="sxs-lookup"><span data-stu-id="9fd74-561">186</span></span>    | <span data-ttu-id="9fd74-562">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="9fd74-562">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="9fd74-563">204</span><span class="sxs-lookup"><span data-stu-id="9fd74-563">204</span></span>    | <span data-ttu-id="9fd74-564">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="9fd74-564">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="9fd74-565">238</span><span class="sxs-lookup"><span data-stu-id="9fd74-565">238</span></span>    | <span data-ttu-id="9fd74-566">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="9fd74-566">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="9fd74-567">255</span><span class="sxs-lookup"><span data-stu-id="9fd74-567">255</span></span>    | <span data-ttu-id="9fd74-568">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="9fd74-568">OEM\_CHARSET</span></span>         |

<span data-ttu-id="9fd74-569">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-569">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="9fd74-570">値です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-570">Value.</span></span> | <span data-ttu-id="9fd74-571">説明。</span><span class="sxs-lookup"><span data-stu-id="9fd74-571">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="9fd74-572">130</span><span class="sxs-lookup"><span data-stu-id="9fd74-572">130</span></span>    | <span data-ttu-id="9fd74-573">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="9fd74-573">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="9fd74-574">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-574">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="9fd74-575">値です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-575">Value.</span></span> | <span data-ttu-id="9fd74-576">説明。</span><span class="sxs-lookup"><span data-stu-id="9fd74-576">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="9fd74-577">177</span><span class="sxs-lookup"><span data-stu-id="9fd74-577">177</span></span>    | <span data-ttu-id="9fd74-578">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="9fd74-578">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="9fd74-579">178</span><span class="sxs-lookup"><span data-stu-id="9fd74-579">178</span></span>    | <span data-ttu-id="9fd74-580">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="9fd74-580">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="9fd74-581">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-581">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="9fd74-582">値です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-582">Value.</span></span> | <span data-ttu-id="9fd74-583">説明。</span><span class="sxs-lookup"><span data-stu-id="9fd74-583">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="9fd74-584">222</span><span class="sxs-lookup"><span data-stu-id="9fd74-584">222</span></span>    | <span data-ttu-id="9fd74-585">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="9fd74-585">THAI\_CHARSET</span></span> |

<span data-ttu-id="9fd74-586">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-586">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="9fd74-587">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-587">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="9fd74-588">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9fd74-588">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="9fd74-589">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="9fd74-589">Method colorScheme</span></span>

<span data-ttu-id="9fd74-590">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-590">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="9fd74-591">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="9fd74-591">Parameters - colorScheme</span></span>

<span data-ttu-id="9fd74-592">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-592">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="9fd74-593">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="9fd74-593">Return Value - colorScheme</span></span>

<span data-ttu-id="9fd74-594">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="9fd74-594">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="9fd74-595">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="9fd74-595">Remarks - colorScheme</span></span>

<span data-ttu-id="9fd74-596">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-596">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="9fd74-597">値です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-597">Value.</span></span> | <span data-ttu-id="9fd74-598">スタイル。</span><span class="sxs-lookup"><span data-stu-id="9fd74-598">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="9fd74-599">0</span><span class="sxs-lookup"><span data-stu-id="9fd74-599">0</span></span>      | <span data-ttu-id="9fd74-600">既定。</span><span class="sxs-lookup"><span data-stu-id="9fd74-600">Default.</span></span>                       |
| <span data-ttu-id="9fd74-601">1</span><span class="sxs-lookup"><span data-stu-id="9fd74-601">1</span></span>      | <span data-ttu-id="9fd74-602">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="9fd74-602">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="9fd74-603">2</span><span class="sxs-lookup"><span data-stu-id="9fd74-603">2</span></span>      | <span data-ttu-id="9fd74-604">真の配色。</span><span class="sxs-lookup"><span data-stu-id="9fd74-604">The true-color scheme.</span></span>         |

## <a name="method-configurationkey"></a><span data-ttu-id="9fd74-605">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="9fd74-605">Method configurationKey</span></span>

<span data-ttu-id="9fd74-606">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-606">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="9fd74-607">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="9fd74-607">Parameters - configurationKey</span></span>

<span data-ttu-id="9fd74-608">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-608">value</span></span>  
<span data-ttu-id="9fd74-609">コントロールに割り当てられているコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-609">The ID of the configuration key being assigned to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="9fd74-610">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="9fd74-610">Return Value - configurationKey</span></span>

<span data-ttu-id="9fd74-611">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="9fd74-611">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="9fd74-612">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="9fd74-612">Remarks - configurationKey</span></span>

<span data-ttu-id="9fd74-613">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-613">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="9fd74-614">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="9fd74-614">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="9fd74-615">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="9fd74-615">Method configurationKeyEx</span></span>

<span data-ttu-id="9fd74-616">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-616">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="9fd74-617">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="9fd74-617">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="9fd74-618">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="9fd74-618">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="9fd74-619">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="9fd74-619">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="9fd74-620">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="9fd74-620">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="9fd74-621">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-621">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="9fd74-622">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-622">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-copycallerquery"></a><span data-ttu-id="9fd74-623">メソッド copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="9fd74-623">Method copyCallerQuery</span></span>

<span data-ttu-id="9fd74-624">ターゲット フォームへの呼び出し元のフォームからクエリをコピーするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-624">Specifies whether to copy the query from the calling form to the target form.</span></span> <span data-ttu-id="9fd74-625">これにより、ターゲット フォームは、元のフォームで表示されていたものと同じデータを照会できます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-625">This enables the target form to display the same data that was being viewed in the original form.</span></span> <span data-ttu-id="9fd74-626">既定値は自動です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-626">The default value is Auto.</span></span>

```xpp
public int copyCallerQuery([int value])
```

### <a name="parameters---copycallerquery"></a><span data-ttu-id="9fd74-627">パラメーター - copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="9fd74-627">Parameters - copyCallerQuery</span></span>

<span data-ttu-id="9fd74-628">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-628">value</span></span>  

### <a name="return-value---copycallerquery"></a><span data-ttu-id="9fd74-629">戻り値 - copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="9fd74-629">Return Value - copyCallerQuery</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="9fd74-630">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="9fd74-630">Method countryRegionCodes</span></span>

<span data-ttu-id="9fd74-631">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-631">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="9fd74-632">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="9fd74-632">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="9fd74-633">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-633">value</span></span>  
<span data-ttu-id="9fd74-634">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9fd74-634">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="9fd74-635">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="9fd74-635">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="9fd74-636">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="9fd74-636">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="9fd74-637">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="9fd74-637">Method countryRegionContextField</span></span>

<span data-ttu-id="9fd74-638">国のコンテキストを識別するために使用されるフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-638">Specifies the field that will be used to identify the country context.</span></span> <span data-ttu-id="9fd74-639">CountryRegionCodes を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9fd74-639">See CountryRegionCodes.</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="9fd74-640">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="9fd74-640">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="9fd74-641">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-641">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="9fd74-642">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="9fd74-642">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="9fd74-643">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="9fd74-643">Method dataRelationPath</span></span>

<span data-ttu-id="9fd74-644">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-644">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="9fd74-645">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="9fd74-645">Parameters - dataRelationPath</span></span>

<span data-ttu-id="9fd74-646">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-646">value</span></span>  
<span data-ttu-id="9fd74-647">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9fd74-647">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="9fd74-648">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="9fd74-648">Return Value - dataRelationPath</span></span>

<span data-ttu-id="9fd74-649">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="9fd74-649">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="9fd74-650">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="9fd74-650">Remarks - dataRelationPath</span></span>

<span data-ttu-id="9fd74-651">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-651">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="9fd74-652">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="9fd74-652">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="9fd74-653">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="9fd74-653">Method dataSource</span></span>

<span data-ttu-id="9fd74-654">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-654">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="9fd74-655">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="9fd74-655">Parameters - dataSource</span></span>

<span data-ttu-id="9fd74-656">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-656">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="9fd74-657">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="9fd74-657">Return Value - dataSource</span></span>

<span data-ttu-id="9fd74-658">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="9fd74-658">The identifier of the data source to be used.</span></span>

## <a name="method-defaultbutton"></a><span data-ttu-id="9fd74-659">メソッド defaultButton</span><span class="sxs-lookup"><span data-stu-id="9fd74-659">Method defaultButton</span></span>

<span data-ttu-id="9fd74-660">ボタンをフォームの既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-660">Determines whether the button should be the default button in the form.</span></span>

```xpp
public boolean defaultButton([boolean value])
```

### <a name="parameters---defaultbutton"></a><span data-ttu-id="9fd74-661">パラメーター - defaultButton</span><span class="sxs-lookup"><span data-stu-id="9fd74-661">Parameters - defaultButton</span></span>

<span data-ttu-id="9fd74-662">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-662">value</span></span>  

### <a name="return-value---defaultbutton"></a><span data-ttu-id="9fd74-663">戻り値 - defaultButton</span><span class="sxs-lookup"><span data-stu-id="9fd74-663">Return Value - defaultButton</span></span>

<span data-ttu-id="9fd74-664">ボタンが既定のボタンである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="9fd74-664">true if the button should be the default button; otherwise, false.</span></span>

## <a name="method-disabledimage"></a><span data-ttu-id="9fd74-665">メソッド disabledImage</span><span class="sxs-lookup"><span data-stu-id="9fd74-665">Method disabledImage</span></span>

<span data-ttu-id="9fd74-666">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-666">Gets or sets the disabled image of the button.</span></span>

```xpp
public str disabledImage([str value])
```

### <a name="parameters---disabledimage"></a><span data-ttu-id="9fd74-667">パラメーター - disabledImage</span><span class="sxs-lookup"><span data-stu-id="9fd74-667">Parameters - disabledImage</span></span>

<span data-ttu-id="9fd74-668">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-668">value</span></span>  

### <a name="return-value---disabledimage"></a><span data-ttu-id="9fd74-669">戻り値 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="9fd74-669">Return Value - disabledImage</span></span>

<span data-ttu-id="9fd74-670">画像ファイルのフル ネーム。</span><span class="sxs-lookup"><span data-stu-id="9fd74-670">The full name of an image file.</span></span> <span data-ttu-id="9fd74-671">システムは、GDI でサポートされているすべてのイメージ形式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9fd74-671">The system supports all of the GDI-supported image formats.</span></span>

### <a name="remarks---disabledimage"></a><span data-ttu-id="9fd74-672">備考 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="9fd74-672">Remarks - disabledImage</span></span>

<span data-ttu-id="9fd74-673">このプロパティは、disabledResource プロパティに優先します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-673">This property has precedence over the disabledResource property.</span></span> <span data-ttu-id="9fd74-674">これらのプロパティの両方が設定されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-674">It is used if both of these properties are set.</span></span>

## <a name="method-disabledimagelocation"></a><span data-ttu-id="9fd74-675">メソッド disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="9fd74-675">Method disabledImageLocation</span></span>

```xpp
public int disabledImageLocation([int value])
```

### <a name="parameters---disabledimagelocation"></a><span data-ttu-id="9fd74-676">パラメーター - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="9fd74-676">Parameters - disabledImageLocation</span></span>

<span data-ttu-id="9fd74-677">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-677">value</span></span>  

### <a name="return-value---disabledimagelocation"></a><span data-ttu-id="9fd74-678">戻り値 - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="9fd74-678">Return Value - disabledImageLocation</span></span>

## <a name="method-disabledresource"></a><span data-ttu-id="9fd74-679">メソッド disabledResource</span><span class="sxs-lookup"><span data-stu-id="9fd74-679">Method disabledResource</span></span>

<span data-ttu-id="9fd74-680">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-680">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>

```xpp
public int disabledResource([int value])
```

### <a name="parameters---disabledresource"></a><span data-ttu-id="9fd74-681">パラメーター - disabledResource</span><span class="sxs-lookup"><span data-stu-id="9fd74-681">Parameters - disabledResource</span></span>

<span data-ttu-id="9fd74-682">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-682">value</span></span>  

### <a name="return-value---disabledresource"></a><span data-ttu-id="9fd74-683">戻り値 - disabledResource</span><span class="sxs-lookup"><span data-stu-id="9fd74-683">Return Value - disabledResource</span></span>

<span data-ttu-id="9fd74-684">無効なボタン画像として使用する画像リソース ID。</span><span class="sxs-lookup"><span data-stu-id="9fd74-684">The resource ID of the image to use as the disabled button image.</span></span> <span data-ttu-id="9fd74-685">アイコンとビットマップ イメージの両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-685">Both icon and bitmap images are supported.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="9fd74-686">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="9fd74-686">Method displayTarget</span></span>

<span data-ttu-id="9fd74-687">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-687">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="9fd74-688">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="9fd74-688">Parameters - displayTarget</span></span>

<span data-ttu-id="9fd74-689">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-689">value</span></span>  
<span data-ttu-id="9fd74-690">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-690">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="9fd74-691">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="9fd74-691">Return Value - displayTarget</span></span>

<span data-ttu-id="9fd74-692">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-692">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="9fd74-693">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="9fd74-693">Method dragDrop</span></span>

<span data-ttu-id="9fd74-694">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-694">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="9fd74-695">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="9fd74-695">Parameters - dragDrop</span></span>

<span data-ttu-id="9fd74-696">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-696">value</span></span>  
<span data-ttu-id="9fd74-697">ドラッグ アンド ドロップの動作を有効にするかどうかを示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-697">An integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="9fd74-698">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="9fd74-698">Return Value - dragDrop</span></span>

<span data-ttu-id="9fd74-699">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-699">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="9fd74-700">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="9fd74-700">Remarks - dragDrop</span></span>

<span data-ttu-id="9fd74-701">dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-701">Use the dragLeave , the dragOver, and the dragOverEx to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="9fd74-702">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="9fd74-702">Method dragOver</span></span>

<span data-ttu-id="9fd74-703">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-703">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="9fd74-704">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="9fd74-704">Parameters - dragOver</span></span>

<span data-ttu-id="9fd74-705">dragSource</span><span class="sxs-lookup"><span data-stu-id="9fd74-705">dragSource</span></span>  
<span data-ttu-id="9fd74-706">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-706">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="9fd74-707">dragMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-707">dragMode</span></span>  
<span data-ttu-id="9fd74-708">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-708">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="9fd74-709">x</span><span class="sxs-lookup"><span data-stu-id="9fd74-709">x</span></span>  
<span data-ttu-id="9fd74-710">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-710">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="9fd74-711">y</span><span class="sxs-lookup"><span data-stu-id="9fd74-711">y</span></span>  
<span data-ttu-id="9fd74-712">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-712">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="9fd74-713">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="9fd74-713">Return Value - dragOver</span></span>

<span data-ttu-id="9fd74-714">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-714">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="9fd74-715">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="9fd74-715">Method dragOverEx</span></span>

<span data-ttu-id="9fd74-716">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-716">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="9fd74-717">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="9fd74-717">Parameters - dragOverEx</span></span>

<span data-ttu-id="9fd74-718">dragSource</span><span class="sxs-lookup"><span data-stu-id="9fd74-718">dragSource</span></span>  
<span data-ttu-id="9fd74-719">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-719">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="9fd74-720">dragMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-720">dragMode</span></span>  
<span data-ttu-id="9fd74-721">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-721">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="9fd74-722">x</span><span class="sxs-lookup"><span data-stu-id="9fd74-722">x</span></span>  
<span data-ttu-id="9fd74-723">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-723">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="9fd74-724">y</span><span class="sxs-lookup"><span data-stu-id="9fd74-724">y</span></span>  
<span data-ttu-id="9fd74-725">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-725">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="9fd74-726">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="9fd74-726">Return Value - dragOverEx</span></span>

<span data-ttu-id="9fd74-727">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-727">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="9fd74-728">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="9fd74-728">Method dragText</span></span>

<span data-ttu-id="9fd74-729">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-729">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="9fd74-730">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="9fd74-730">Return Value - dragText</span></span>

<span data-ttu-id="9fd74-731">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="9fd74-731">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="9fd74-732">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="9fd74-732">Method enabled</span></span>

<span data-ttu-id="9fd74-733">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-733">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="9fd74-734">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="9fd74-734">Parameters - enabled</span></span>

<span data-ttu-id="9fd74-735">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-735">value</span></span>  
<span data-ttu-id="9fd74-736">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-736">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="9fd74-737">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="9fd74-737">Return Value - enabled</span></span>

<span data-ttu-id="9fd74-738">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="9fd74-738">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="9fd74-739">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="9fd74-739">Remarks - enabled</span></span>

<span data-ttu-id="9fd74-740">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-740">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="9fd74-741">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-741">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="9fd74-742">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-742">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="9fd74-743">メソッド font</span><span class="sxs-lookup"><span data-stu-id="9fd74-743">Method font</span></span>

<span data-ttu-id="9fd74-744">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-744">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="9fd74-745">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="9fd74-745">Parameters - font</span></span>

<span data-ttu-id="9fd74-746">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-746">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="9fd74-747">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="9fd74-747">Return Value - font</span></span>

<span data-ttu-id="9fd74-748">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="9fd74-748">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="9fd74-749">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="9fd74-749">Method fontSize</span></span>

<span data-ttu-id="9fd74-750">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-750">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="9fd74-751">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="9fd74-751">Parameters - fontSize</span></span>

<span data-ttu-id="9fd74-752">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-752">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="9fd74-753">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="9fd74-753">Return Value - fontSize</span></span>

<span data-ttu-id="9fd74-754">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="9fd74-754">The height of the font in points.</span></span>

## <a name="method-forcedtooverflow"></a><span data-ttu-id="9fd74-755">メソッド forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="9fd74-755">Method forcedToOverflow</span></span>

```xpp
public boolean forcedToOverflow([boolean value])
```

### <a name="parameters---forcedtooverflow"></a><span data-ttu-id="9fd74-756">パラメーター - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="9fd74-756">Parameters - forcedToOverflow</span></span>

<span data-ttu-id="9fd74-757">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-757">value</span></span>  

### <a name="return-value---forcedtooverflow"></a><span data-ttu-id="9fd74-758">戻り値 - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="9fd74-758">Return Value - forcedToOverflow</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="9fd74-759">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="9fd74-759">Method foregroundColor</span></span>

<span data-ttu-id="9fd74-760">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-760">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="9fd74-761">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="9fd74-761">Parameters - foregroundColor</span></span>

<span data-ttu-id="9fd74-762">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-762">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="9fd74-763">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="9fd74-763">Return Value - foregroundColor</span></span>

<span data-ttu-id="9fd74-764">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="9fd74-764">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="9fd74-765">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="9fd74-765">Remarks - foregroundColor</span></span>

<span data-ttu-id="9fd74-766">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-766">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="9fd74-767">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9fd74-767">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="9fd74-768">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="9fd74-768">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="9fd74-769">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="9fd74-769">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="9fd74-770">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="9fd74-770">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="9fd74-771">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-771">The maximum value for a single byte is 255.</span></span>

## <a name="method-formviewoption"></a><span data-ttu-id="9fd74-772">メソッド formViewOption</span><span class="sxs-lookup"><span data-stu-id="9fd74-772">Method formViewOption</span></span>

<span data-ttu-id="9fd74-773">使用するフォーム モードを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-773">Specifies the form mode to use.</span></span> <span data-ttu-id="9fd74-774">オプションには、[自動]、[グリッド]、および [詳細] が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-774">Options include Auto, Grid, and Details.</span></span> <span data-ttu-id="9fd74-775">既定は自動です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-775">The default is Auto.</span></span>

```xpp
public int formViewOption([int value])
```

### <a name="parameters---formviewoption"></a><span data-ttu-id="9fd74-776">パラメーター - formViewOption</span><span class="sxs-lookup"><span data-stu-id="9fd74-776">Parameters - formViewOption</span></span>

<span data-ttu-id="9fd74-777">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-777">value</span></span>  

### <a name="return-value---formviewoption"></a><span data-ttu-id="9fd74-778">戻り値 - formViewOption</span><span class="sxs-lookup"><span data-stu-id="9fd74-778">Return Value - formViewOption</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="9fd74-779">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="9fd74-779">Method hasChanged</span></span>

<span data-ttu-id="9fd74-780">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-780">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="9fd74-781">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="9fd74-781">Parameters - hasChanged</span></span>

<span data-ttu-id="9fd74-782">val</span><span class="sxs-lookup"><span data-stu-id="9fd74-782">val</span></span>  
<span data-ttu-id="9fd74-783">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9fd74-783">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="9fd74-784">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="9fd74-784">Return Value - hasChanged</span></span>

<span data-ttu-id="9fd74-785">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="9fd74-785">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="9fd74-786">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="9fd74-786">Method hasUserSetting</span></span>

<span data-ttu-id="9fd74-787">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-787">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="9fd74-788">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="9fd74-788">Return Value - hasUserSetting</span></span>

<span data-ttu-id="9fd74-789">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="9fd74-789">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="9fd74-790">メソッド height</span><span class="sxs-lookup"><span data-stu-id="9fd74-790">Method height</span></span>

<span data-ttu-id="9fd74-791">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-791">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="9fd74-792">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="9fd74-792">Parameters - height</span></span>

<span data-ttu-id="9fd74-793">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-793">value</span></span>  
<span data-ttu-id="9fd74-794">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-794">An integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="9fd74-795">モード</span><span class="sxs-lookup"><span data-stu-id="9fd74-795">mode</span></span>  
<span data-ttu-id="9fd74-796">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-796">An integer that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="9fd74-797">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="9fd74-797">Return Value - height</span></span>

<span data-ttu-id="9fd74-798">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="9fd74-798">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="9fd74-799">備考 - height</span><span class="sxs-lookup"><span data-stu-id="9fd74-799">Remarks - height</span></span>

<span data-ttu-id="9fd74-800">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-800">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="9fd74-801">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="9fd74-801">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="9fd74-802">モード。</span><span class="sxs-lookup"><span data-stu-id="9fd74-802">Mode.</span></span>            | <span data-ttu-id="9fd74-803">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="9fd74-803">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd74-804">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="9fd74-804">-1 Exact.</span></span>        | <span data-ttu-id="9fd74-805">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-805">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="9fd74-806">0 自動。</span><span class="sxs-lookup"><span data-stu-id="9fd74-806">0 Auto.</span></span>          | <span data-ttu-id="9fd74-807">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-807">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="9fd74-808">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="9fd74-808">1 Column height.</span></span> | <span data-ttu-id="9fd74-809">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="9fd74-809">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="9fd74-810">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-810">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="9fd74-811">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-811">Method heightMode</span></span>

<span data-ttu-id="9fd74-812">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-812">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="9fd74-813">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-813">Parameters - heightMode</span></span>

<span data-ttu-id="9fd74-814">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-814">value</span></span>  
<span data-ttu-id="9fd74-815">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-815">An integer value that indicates how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="9fd74-816">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-816">Return Value - heightMode</span></span>

<span data-ttu-id="9fd74-817">計算モード。</span><span class="sxs-lookup"><span data-stu-id="9fd74-817">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="9fd74-818">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-818">Remarks - heightMode</span></span>

<span data-ttu-id="9fd74-819">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="9fd74-819">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="9fd74-820">モード。</span><span class="sxs-lookup"><span data-stu-id="9fd74-820">Mode.</span></span>          | <span data-ttu-id="9fd74-821">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="9fd74-821">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd74-822">正確。</span><span class="sxs-lookup"><span data-stu-id="9fd74-822">Exact.</span></span>         | <span data-ttu-id="9fd74-823">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-823">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="9fd74-824">自動。</span><span class="sxs-lookup"><span data-stu-id="9fd74-824">Auto.</span></span>          | <span data-ttu-id="9fd74-825">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-825">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="9fd74-826">列の高さ</span><span class="sxs-lookup"><span data-stu-id="9fd74-826">Column height.</span></span> | <span data-ttu-id="9fd74-827">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="9fd74-827">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="9fd74-828">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="9fd74-828">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="9fd74-829">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="9fd74-829">Method heightValue</span></span>

<span data-ttu-id="9fd74-830">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-830">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="9fd74-831">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="9fd74-831">Parameters - heightValue</span></span>

<span data-ttu-id="9fd74-832">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-832">value</span></span>  
<span data-ttu-id="9fd74-833">高さをピクセル単位で指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-833">An integer that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="9fd74-834">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="9fd74-834">Return Value - heightValue</span></span>

<span data-ttu-id="9fd74-835">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="9fd74-835">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="9fd74-836">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="9fd74-836">Remarks - heightValue</span></span>

<span data-ttu-id="9fd74-837">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="9fd74-837">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="9fd74-838">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="9fd74-838">Method helpField</span></span>

<span data-ttu-id="9fd74-839">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-839">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="9fd74-840">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="9fd74-840">Return Value - helpField</span></span>

<span data-ttu-id="9fd74-841">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="9fd74-841">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="9fd74-842">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="9fd74-842">Remarks - helpField</span></span>

<span data-ttu-id="9fd74-843">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="9fd74-843">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="9fd74-844">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-844">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="9fd74-845">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="9fd74-845">Method helpText</span></span>

<span data-ttu-id="9fd74-846">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-846">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="9fd74-847">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="9fd74-847">Parameters - helpText</span></span>

<span data-ttu-id="9fd74-848">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-848">value</span></span>  
<span data-ttu-id="9fd74-849">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-849">The value that is assigned as the Help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="9fd74-850">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="9fd74-850">Return Value - helpText</span></span>

<span data-ttu-id="9fd74-851">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="9fd74-851">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="9fd74-852">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="9fd74-852">Remarks - helpText</span></span>

<span data-ttu-id="9fd74-853">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-853">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="9fd74-854">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="9fd74-854">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="9fd74-855">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="9fd74-855">Method hierarchyParent</span></span>

<span data-ttu-id="9fd74-856">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-856">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="9fd74-857">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="9fd74-857">Parameters - hierarchyParent</span></span>

<span data-ttu-id="9fd74-858">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-858">value</span></span>  
<span data-ttu-id="9fd74-859">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-859">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="9fd74-860">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="9fd74-860">Return Value - hierarchyParent</span></span>

<span data-ttu-id="9fd74-861">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-861">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="9fd74-862">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="9fd74-862">Method hWnd</span></span>

<span data-ttu-id="9fd74-863">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-863">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="9fd74-864">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="9fd74-864">Return Value - hWnd</span></span>

<span data-ttu-id="9fd74-865">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="9fd74-865">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="9fd74-866">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="9fd74-866">Remarks - hWnd</span></span>

<span data-ttu-id="9fd74-867">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-867">The handle can be used with the Windows API.</span></span>

## <a name="method-imagelocation"></a><span data-ttu-id="9fd74-868">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="9fd74-868">Method imageLocation</span></span>

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a><span data-ttu-id="9fd74-869">パラメーター - imageLocation</span><span class="sxs-lookup"><span data-stu-id="9fd74-869">Parameters - imageLocation</span></span>

<span data-ttu-id="9fd74-870">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-870">value</span></span>  

### <a name="return-value---imagelocation"></a><span data-ttu-id="9fd74-871">戻り値 - imageLocation</span><span class="sxs-lookup"><span data-stu-id="9fd74-871">Return Value - imageLocation</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="9fd74-872">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="9fd74-872">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="9fd74-873">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="9fd74-873">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="9fd74-874">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="9fd74-874">Method isDisplayed</span></span>

<span data-ttu-id="9fd74-875">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-875">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="9fd74-876">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="9fd74-876">Return Value - isDisplayed</span></span>

<span data-ttu-id="9fd74-877">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="9fd74-877">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="9fd74-878">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="9fd74-878">Remarks - isDisplayed</span></span>

<span data-ttu-id="9fd74-879">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-879">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="9fd74-880">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="9fd74-880">Method isRestricted</span></span>

<span data-ttu-id="9fd74-881">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-881">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="9fd74-882">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="9fd74-882">Return Value - isRestricted</span></span>

<span data-ttu-id="9fd74-883">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="9fd74-883">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="9fd74-884">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="9fd74-884">Method isUserSetupEnabled</span></span>

<span data-ttu-id="9fd74-885">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-885">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="9fd74-886">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="9fd74-886">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="9fd74-887">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="9fd74-887">neededSetupRights</span></span>  
<span data-ttu-id="9fd74-888">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-888">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="9fd74-889">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="9fd74-889">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="9fd74-890">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="9fd74-890">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="9fd74-891">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="9fd74-891">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="9fd74-892">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-892">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd74-893">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="9fd74-893">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="9fd74-894">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="9fd74-894">No changes can be made to the control.</span></span> <span data-ttu-id="9fd74-895">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-895">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="9fd74-896">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="9fd74-896">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="9fd74-897">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-897">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="9fd74-898">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="9fd74-898">The user cannot move the control.</span></span>   |
| <span data-ttu-id="9fd74-899">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="9fd74-899">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="9fd74-900">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-900">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="9fd74-901">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-901">The user can also move the control.</span></span> |

<span data-ttu-id="9fd74-902">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="9fd74-902">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-italic"></a><span data-ttu-id="9fd74-903">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="9fd74-903">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="9fd74-904">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="9fd74-904">Parameters - italic</span></span>

<span data-ttu-id="9fd74-905">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-905">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="9fd74-906">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="9fd74-906">Return Value - italic</span></span>

## <a name="method-keytip"></a><span data-ttu-id="9fd74-907">メソッド keyTip</span><span class="sxs-lookup"><span data-stu-id="9fd74-907">Method keyTip</span></span>

```xpp
public str keyTip([str value])
```

### <a name="parameters---keytip"></a><span data-ttu-id="9fd74-908">パラメーター - keyTip</span><span class="sxs-lookup"><span data-stu-id="9fd74-908">Parameters - keyTip</span></span>

<span data-ttu-id="9fd74-909">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-909">value</span></span>  

### <a name="return-value---keytip"></a><span data-ttu-id="9fd74-910">戻り値 - keyTip</span><span class="sxs-lookup"><span data-stu-id="9fd74-910">Return Value - keyTip</span></span>

## <a name="method-left"></a><span data-ttu-id="9fd74-911">メソッド left</span><span class="sxs-lookup"><span data-stu-id="9fd74-911">Method left</span></span>

<span data-ttu-id="9fd74-912">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-912">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="9fd74-913">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="9fd74-913">Parameters - left</span></span>

<span data-ttu-id="9fd74-914">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-914">value</span></span>  
<span data-ttu-id="9fd74-915">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-915">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="9fd74-916">モード</span><span class="sxs-lookup"><span data-stu-id="9fd74-916">mode</span></span>  
<span data-ttu-id="9fd74-917">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-917">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="9fd74-918">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="9fd74-918">Return Value - left</span></span>

<span data-ttu-id="9fd74-919">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="9fd74-919">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="9fd74-920">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-920">Method leftMode</span></span>

<span data-ttu-id="9fd74-921">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-921">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="9fd74-922">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-922">Parameters - leftMode</span></span>

<span data-ttu-id="9fd74-923">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-923">value</span></span>  
<span data-ttu-id="9fd74-924">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-924">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="9fd74-925">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-925">Return Value - leftMode</span></span>

<span data-ttu-id="9fd74-926">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="9fd74-926">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="9fd74-927">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="9fd74-927">Method leftValue</span></span>

<span data-ttu-id="9fd74-928">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-928">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="9fd74-929">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="9fd74-929">Parameters - leftValue</span></span>

<span data-ttu-id="9fd74-930">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-930">value</span></span>  
<span data-ttu-id="9fd74-931">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-931">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="9fd74-932">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="9fd74-932">Return Value - leftValue</span></span>

<span data-ttu-id="9fd74-933">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="9fd74-933">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="9fd74-934">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="9fd74-934">Method markAsUserAdd</span></span>

<span data-ttu-id="9fd74-935">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="9fd74-935">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="9fd74-936">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="9fd74-936">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="9fd74-937">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-937">value</span></span>  
<span data-ttu-id="9fd74-938">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-938">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="9fd74-939">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="9fd74-939">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="9fd74-940">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="9fd74-940">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-menufunction"></a><span data-ttu-id="9fd74-941">メソッド menufunction</span><span class="sxs-lookup"><span data-stu-id="9fd74-941">Method menufunction</span></span>

```xpp
public xMenuFunction menufunction()
```

### <a name="return-value---menufunction"></a><span data-ttu-id="9fd74-942">戻り値 - menufunction</span><span class="sxs-lookup"><span data-stu-id="9fd74-942">Return Value - menufunction</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="9fd74-943">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="9fd74-943">Method menuItemName</span></span>

<span data-ttu-id="9fd74-944">DropDialogButton コントロールに対して実行されるメニュー項目を決定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-944">Determines which menu item is run for a DropDialogButton control.</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="9fd74-945">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="9fd74-945">Parameters - menuItemName</span></span>

<span data-ttu-id="9fd74-946">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-946">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="9fd74-947">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="9fd74-947">Return Value - menuItemName</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="9fd74-948">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="9fd74-948">Method mouseDblClick</span></span>

<span data-ttu-id="9fd74-949">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-949">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="9fd74-950">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="9fd74-950">Parameters - mouseDblClick</span></span>

<span data-ttu-id="9fd74-951">x</span><span class="sxs-lookup"><span data-stu-id="9fd74-951">x</span></span>  
<span data-ttu-id="9fd74-952">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-952">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-953">y</span><span class="sxs-lookup"><span data-stu-id="9fd74-953">y</span></span>  
<span data-ttu-id="9fd74-954">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-954">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-955">ボタン</span><span class="sxs-lookup"><span data-stu-id="9fd74-955">button</span></span>  
<span data-ttu-id="9fd74-956">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-956">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-957">Ctrl</span><span class="sxs-lookup"><span data-stu-id="9fd74-957">Ctrl</span></span>  
<span data-ttu-id="9fd74-958">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-958">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-959">シフト</span><span class="sxs-lookup"><span data-stu-id="9fd74-959">Shift</span></span>  
<span data-ttu-id="9fd74-960">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-960">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="9fd74-961">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="9fd74-961">Return Value - mouseDblClick</span></span>

<span data-ttu-id="9fd74-962">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-962">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="9fd74-963">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="9fd74-963">Remarks - mouseDblClick</span></span>

<span data-ttu-id="9fd74-964">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-964">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="9fd74-965">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="9fd74-965">Method mouseDown</span></span>

<span data-ttu-id="9fd74-966">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-966">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="9fd74-967">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="9fd74-967">Parameters - mouseDown</span></span>

<span data-ttu-id="9fd74-968">x</span><span class="sxs-lookup"><span data-stu-id="9fd74-968">x</span></span>  
<span data-ttu-id="9fd74-969">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-969">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-970">y</span><span class="sxs-lookup"><span data-stu-id="9fd74-970">y</span></span>  
<span data-ttu-id="9fd74-971">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-971">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-972">ボタン</span><span class="sxs-lookup"><span data-stu-id="9fd74-972">button</span></span>  
<span data-ttu-id="9fd74-973">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-973">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-974">Ctrl</span><span class="sxs-lookup"><span data-stu-id="9fd74-974">Ctrl</span></span>  
<span data-ttu-id="9fd74-975">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-975">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-976">シフト</span><span class="sxs-lookup"><span data-stu-id="9fd74-976">Shift</span></span>  
<span data-ttu-id="9fd74-977">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-977">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="9fd74-978">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="9fd74-978">Return Value - mouseDown</span></span>

<span data-ttu-id="9fd74-979">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-979">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="9fd74-980">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="9fd74-980">Remarks - mouseDown</span></span>

<span data-ttu-id="9fd74-981">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-981">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="9fd74-982">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-982">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="9fd74-983">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="9fd74-983">Method mouseMove</span></span>

<span data-ttu-id="9fd74-984">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-984">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="9fd74-985">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="9fd74-985">Parameters - mouseMove</span></span>

<span data-ttu-id="9fd74-986">x</span><span class="sxs-lookup"><span data-stu-id="9fd74-986">x</span></span>  
<span data-ttu-id="9fd74-987">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-987">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-988">y</span><span class="sxs-lookup"><span data-stu-id="9fd74-988">y</span></span>  
<span data-ttu-id="9fd74-989">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-989">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-990">ボタン</span><span class="sxs-lookup"><span data-stu-id="9fd74-990">button</span></span>  
<span data-ttu-id="9fd74-991">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-991">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-992">Ctrl</span><span class="sxs-lookup"><span data-stu-id="9fd74-992">Ctrl</span></span>  
<span data-ttu-id="9fd74-993">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-993">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-994">シフト</span><span class="sxs-lookup"><span data-stu-id="9fd74-994">Shift</span></span>  
<span data-ttu-id="9fd74-995">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-995">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="9fd74-996">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="9fd74-996">Return Value - mouseMove</span></span>

<span data-ttu-id="9fd74-997">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-997">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="9fd74-998">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="9fd74-998">Remarks - mouseMove</span></span>

<span data-ttu-id="9fd74-999">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-999">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="9fd74-1000">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="9fd74-1000">Method mouseUp</span></span>

<span data-ttu-id="9fd74-1001">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1001">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="9fd74-1002">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="9fd74-1002">Parameters - mouseUp</span></span>

<span data-ttu-id="9fd74-1003">x</span><span class="sxs-lookup"><span data-stu-id="9fd74-1003">x</span></span>  
<span data-ttu-id="9fd74-1004">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1004">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-1005">y</span><span class="sxs-lookup"><span data-stu-id="9fd74-1005">y</span></span>  
<span data-ttu-id="9fd74-1006">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1006">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-1007">ボタン</span><span class="sxs-lookup"><span data-stu-id="9fd74-1007">button</span></span>  
<span data-ttu-id="9fd74-1008">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1008">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-1009">Ctrl</span><span class="sxs-lookup"><span data-stu-id="9fd74-1009">Ctrl</span></span>  
<span data-ttu-id="9fd74-1010">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1010">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-1011">シフト</span><span class="sxs-lookup"><span data-stu-id="9fd74-1011">Shift</span></span>  
<span data-ttu-id="9fd74-1012">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1012">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="9fd74-1013">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="9fd74-1013">Return Value - mouseUp</span></span>

<span data-ttu-id="9fd74-1014">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1014">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="9fd74-1015">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="9fd74-1015">Remarks - mouseUp</span></span>

<span data-ttu-id="9fd74-1016">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1016">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="9fd74-1017">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1017">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-multiselect"></a><span data-ttu-id="9fd74-1018">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="9fd74-1018">Method multiSelect</span></span>

```xpp
public int multiSelect([int value])
```

### <a name="parameters---multiselect"></a><span data-ttu-id="9fd74-1019">パラメーター - multiSelect</span><span class="sxs-lookup"><span data-stu-id="9fd74-1019">Parameters - multiSelect</span></span>

<span data-ttu-id="9fd74-1020">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1020">value</span></span>  

### <a name="return-value---multiselect"></a><span data-ttu-id="9fd74-1021">戻り値 - multiSelect</span><span class="sxs-lookup"><span data-stu-id="9fd74-1021">Return Value - multiSelect</span></span>

## <a name="method-name"></a><span data-ttu-id="9fd74-1022">メソッド名</span><span class="sxs-lookup"><span data-stu-id="9fd74-1022">Method name</span></span>

<span data-ttu-id="9fd74-1023">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1023">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="9fd74-1024">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="9fd74-1024">Parameters - name</span></span>

<span data-ttu-id="9fd74-1025">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1025">value</span></span>  
<span data-ttu-id="9fd74-1026">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1026">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="9fd74-1027">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="9fd74-1027">Return Value - name</span></span>

<span data-ttu-id="9fd74-1028">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1028">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="9fd74-1029">備考 - name</span><span class="sxs-lookup"><span data-stu-id="9fd74-1029">Remarks - name</span></span>

<span data-ttu-id="9fd74-1030">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1030">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="9fd74-1031">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1031">It must begin with a letter.</span></span>
-   <span data-ttu-id="9fd74-1032">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1032">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="9fd74-1033">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1033">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="9fd74-1034">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1034">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="9fd74-1035">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1035">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="9fd74-1036">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="9fd74-1036">Method neededPermission</span></span>

<span data-ttu-id="9fd74-1037">コントロールへのアクセスを許可するために必要な最小限のアクセス許可レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1037">Specifies the minimum permission level that is required to be allowed access to the control.</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="9fd74-1038">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="9fd74-1038">Parameters - neededPermission</span></span>

<span data-ttu-id="9fd74-1039">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1039">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="9fd74-1040">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="9fd74-1040">Return Value - neededPermission</span></span>

### <a name="remarks---neededpermission"></a><span data-ttu-id="9fd74-1041">備考 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="9fd74-1041">Remarks - neededPermission</span></span>

<span data-ttu-id="9fd74-1042">可能なフィールドの値は次のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1042">The possible values are as follows:</span></span>

-   <span data-ttu-id="9fd74-1043">None</span><span class="sxs-lookup"><span data-stu-id="9fd74-1043">None</span></span>
-   <span data-ttu-id="9fd74-1044">既読</span><span class="sxs-lookup"><span data-stu-id="9fd74-1044">Read</span></span>
-   <span data-ttu-id="9fd74-1045">Update</span><span class="sxs-lookup"><span data-stu-id="9fd74-1045">Update</span></span>
-   <span data-ttu-id="9fd74-1046">新規</span><span class="sxs-lookup"><span data-stu-id="9fd74-1046">Create</span></span>
-   <span data-ttu-id="9fd74-1047">修正</span><span class="sxs-lookup"><span data-stu-id="9fd74-1047">Correct</span></span>
-   <span data-ttu-id="9fd74-1048">消去</span><span class="sxs-lookup"><span data-stu-id="9fd74-1048">Delete</span></span>
-   <span data-ttu-id="9fd74-1049">マニュアル</span><span class="sxs-lookup"><span data-stu-id="9fd74-1049">Manual</span></span>

<span data-ttu-id="9fd74-1050">既定値はなしです。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1050">The default value is None.</span></span>

## <a name="method-needsrecord"></a><span data-ttu-id="9fd74-1051">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="9fd74-1051">Method needsRecord</span></span>

<span data-ttu-id="9fd74-1052">レコードが存在しない場合、ボタンを有効にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1052">Specifies whether a button is enabled if no record is present.</span></span> <span data-ttu-id="9fd74-1053">既定値はいいえです。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1053">The default value is No.</span></span>

```xpp
public int needsRecord([int value])
```

### <a name="parameters---needsrecord"></a><span data-ttu-id="9fd74-1054">パラメーター - needsRecord</span><span class="sxs-lookup"><span data-stu-id="9fd74-1054">Parameters - needsRecord</span></span>

<span data-ttu-id="9fd74-1055">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1055">value</span></span>  

### <a name="return-value---needsrecord"></a><span data-ttu-id="9fd74-1056">戻り値 - needsRecord</span><span class="sxs-lookup"><span data-stu-id="9fd74-1056">Return Value - needsRecord</span></span>

## <a name="method-normalimage"></a><span data-ttu-id="9fd74-1057">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="9fd74-1057">Method normalImage</span></span>

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a><span data-ttu-id="9fd74-1058">パラメーター - normalImage</span><span class="sxs-lookup"><span data-stu-id="9fd74-1058">Parameters - normalImage</span></span>

<span data-ttu-id="9fd74-1059">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1059">value</span></span>  

### <a name="return-value---normalimage"></a><span data-ttu-id="9fd74-1060">戻り値 - normalImage</span><span class="sxs-lookup"><span data-stu-id="9fd74-1060">Return Value - normalImage</span></span>

## <a name="method-normalresource"></a><span data-ttu-id="9fd74-1061">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="9fd74-1061">Method normalResource</span></span>

```xpp
public int normalResource([int value])
```

### <a name="parameters---normalresource"></a><span data-ttu-id="9fd74-1062">パラメーター - normalResource</span><span class="sxs-lookup"><span data-stu-id="9fd74-1062">Parameters - normalResource</span></span>

<span data-ttu-id="9fd74-1063">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1063">value</span></span>  

### <a name="return-value---normalresource"></a><span data-ttu-id="9fd74-1064">戻り値 - normalResource</span><span class="sxs-lookup"><span data-stu-id="9fd74-1064">Return Value - normalResource</span></span>

## <a name="method-openmode"></a><span data-ttu-id="9fd74-1065">メソッド openMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-1065">Method openMode</span></span>

<span data-ttu-id="9fd74-1066">ターゲット フォームの表示モードを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1066">Specifies the view mode of the target form.</span></span> <span data-ttu-id="9fd74-1067">使用可能な値には、Auto、View、Edit、および New が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1067">The possible values include Auto, View, Edit, and New.</span></span> <span data-ttu-id="9fd74-1068">既定は自動です。このプロパティを使用して、ターゲット フォームを編集モードまたは読み取り専用モードのいずれで開くかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1068">The default is Auto. You may use this property to specify whether the target form opens in edit or read-only mode.</span></span>

```xpp
public int openMode([int value])
```

### <a name="parameters---openmode"></a><span data-ttu-id="9fd74-1069">パラメーター - openMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-1069">Parameters - openMode</span></span>

<span data-ttu-id="9fd74-1070">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1070">value</span></span>  

### <a name="return-value---openmode"></a><span data-ttu-id="9fd74-1071">戻り値 - openMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-1071">Return Value - openMode</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="9fd74-1072">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="9fd74-1072">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="9fd74-1073">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="9fd74-1073">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parameters"></a><span data-ttu-id="9fd74-1074">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="9fd74-1074">Method parameters</span></span>

<span data-ttu-id="9fd74-1075">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1075">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

```xpp
public str parameters([str value])
```

### <a name="parameters---parameters"></a><span data-ttu-id="9fd74-1076">パラメーター - parameters</span><span class="sxs-lookup"><span data-stu-id="9fd74-1076">Parameters - parameters</span></span>

<span data-ttu-id="9fd74-1077">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1077">value</span></span>  

### <a name="return-value---parameters"></a><span data-ttu-id="9fd74-1078">戻り値 - parameters</span><span class="sxs-lookup"><span data-stu-id="9fd74-1078">Return Value - parameters</span></span>

<span data-ttu-id="9fd74-1079">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1079">The list of parameters that are passed to the object.</span></span>

### <a name="remarks---parameters"></a><span data-ttu-id="9fd74-1080">備考 - parameters</span><span class="sxs-lookup"><span data-stu-id="9fd74-1080">Remarks - parameters</span></span>

<span data-ttu-id="9fd74-1081">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1081">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="9fd74-1082">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1082">Objects ignore passed, unrecognized parameters.</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="9fd74-1083">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="9fd74-1083">Method parentControl</span></span>

<span data-ttu-id="9fd74-1084">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1084">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="9fd74-1085">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="9fd74-1085">Return Value - parentControl</span></span>

<span data-ttu-id="9fd74-1086">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1086">The parent control for the control.</span></span>

## <a name="method-primary"></a><span data-ttu-id="9fd74-1087">メソッド primary</span><span class="sxs-lookup"><span data-stu-id="9fd74-1087">Method primary</span></span>

```xpp
public boolean primary([boolean value])
```

### <a name="parameters---primary"></a><span data-ttu-id="9fd74-1088">パラメーター - primary</span><span class="sxs-lookup"><span data-stu-id="9fd74-1088">Parameters - primary</span></span>

<span data-ttu-id="9fd74-1089">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1089">value</span></span>  

### <a name="return-value---primary"></a><span data-ttu-id="9fd74-1090">戻り値 - primary</span><span class="sxs-lookup"><span data-stu-id="9fd74-1090">Return Value - primary</span></span>

## <a name="method-saverecord"></a><span data-ttu-id="9fd74-1091">メソッド saveRecord</span><span class="sxs-lookup"><span data-stu-id="9fd74-1091">Method saveRecord</span></span>

```xpp
public boolean saveRecord([boolean value])
```

### <a name="parameters---saverecord"></a><span data-ttu-id="9fd74-1092">パラメーター - saveRecord</span><span class="sxs-lookup"><span data-stu-id="9fd74-1092">Parameters - saveRecord</span></span>

<span data-ttu-id="9fd74-1093">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1093">value</span></span>  

### <a name="return-value---saverecord"></a><span data-ttu-id="9fd74-1094">戻り値 - saveRecord</span><span class="sxs-lookup"><span data-stu-id="9fd74-1094">Return Value - saveRecord</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="9fd74-1095">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="9fd74-1095">Method securityKey</span></span>

<span data-ttu-id="9fd74-1096">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1096">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="9fd74-1097">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="9fd74-1097">Parameters - securityKey</span></span>

<span data-ttu-id="9fd74-1098">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1098">value</span></span>  
<span data-ttu-id="9fd74-1099">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1099">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="9fd74-1100">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="9fd74-1100">Return Value - securityKey</span></span>

<span data-ttu-id="9fd74-1101">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1101">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-sendexternalcontext"></a><span data-ttu-id="9fd74-1102">メソッド sendExternalContext</span><span class="sxs-lookup"><span data-stu-id="9fd74-1102">Method sendExternalContext</span></span>

<span data-ttu-id="9fd74-1103">このフォームの外部レコード コンテキストをメニュー項目の外部レコード コンテキストとして使用するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1103">Specifies whether the external record context of this form should be used as the menu item external record context.</span></span> <span data-ttu-id="9fd74-1104">既定値はいいえです。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1104">The default value is No.</span></span>

```xpp
public boolean sendExternalContext([boolean value])
```

### <a name="parameters---sendexternalcontext"></a><span data-ttu-id="9fd74-1105">パラメーター - sendExternalContext</span><span class="sxs-lookup"><span data-stu-id="9fd74-1105">Parameters - sendExternalContext</span></span>

<span data-ttu-id="9fd74-1106">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1106">value</span></span>  

### <a name="return-value---sendexternalcontext"></a><span data-ttu-id="9fd74-1107">戻り値 - sendExternalContext</span><span class="sxs-lookup"><span data-stu-id="9fd74-1107">Return Value - sendExternalContext</span></span>

## <a name="method-shortkey"></a><span data-ttu-id="9fd74-1108">メソッド shortkey</span><span class="sxs-lookup"><span data-stu-id="9fd74-1108">Method shortkey</span></span>

```xpp
public int shortkey([int value])
```

### <a name="parameters---shortkey"></a><span data-ttu-id="9fd74-1109">パラメーター - shortkey</span><span class="sxs-lookup"><span data-stu-id="9fd74-1109">Parameters - shortkey</span></span>

<span data-ttu-id="9fd74-1110">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1110">value</span></span>  

### <a name="return-value---shortkey"></a><span data-ttu-id="9fd74-1111">戻り値 - shortkey</span><span class="sxs-lookup"><span data-stu-id="9fd74-1111">Return Value - shortkey</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="9fd74-1112">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="9fd74-1112">Method showContextMenu</span></span>

<span data-ttu-id="9fd74-1113">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1113">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="9fd74-1114">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="9fd74-1114">Parameters - showContextMenu</span></span>

<span data-ttu-id="9fd74-1115">menuHandle</span><span class="sxs-lookup"><span data-stu-id="9fd74-1115">menuHandle</span></span>  
<span data-ttu-id="9fd74-1116">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1116">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="9fd74-1117">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="9fd74-1117">Return Value - showContextMenu</span></span>

<span data-ttu-id="9fd74-1118">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1118">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showshortcut"></a><span data-ttu-id="9fd74-1119">メソッド showShortCut</span><span class="sxs-lookup"><span data-stu-id="9fd74-1119">Method showShortCut</span></span>

```xpp
public boolean showShortCut([boolean value])
```

### <a name="parameters---showshortcut"></a><span data-ttu-id="9fd74-1120">パラメーター - showShortCut</span><span class="sxs-lookup"><span data-stu-id="9fd74-1120">Parameters - showShortCut</span></span>

<span data-ttu-id="9fd74-1121">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1121">value</span></span>  

### <a name="return-value---showshortcut"></a><span data-ttu-id="9fd74-1122">戻り値 - showShortCut</span><span class="sxs-lookup"><span data-stu-id="9fd74-1122">Return Value - showShortCut</span></span>

## <a name="method-skip"></a><span data-ttu-id="9fd74-1123">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="9fd74-1123">Method skip</span></span>

<span data-ttu-id="9fd74-1124">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1124">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="9fd74-1125">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="9fd74-1125">Parameters - skip</span></span>

<span data-ttu-id="9fd74-1126">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1126">value</span></span>  
<span data-ttu-id="9fd74-1127">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1127">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="9fd74-1128">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="9fd74-1128">Return Value - skip</span></span>

<span data-ttu-id="9fd74-1129">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1129">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="9fd74-1130">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="9fd74-1130">Remarks - skip</span></span>

<span data-ttu-id="9fd74-1131">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1131">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-sort"></a><span data-ttu-id="9fd74-1132">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="9fd74-1132">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="9fd74-1133">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="9fd74-1133">Parameters - sort</span></span>

<span data-ttu-id="9fd74-1134">sortDirection</span><span class="sxs-lookup"><span data-stu-id="9fd74-1134">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="9fd74-1135">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="9fd74-1135">Return Value - sort</span></span>

## <a name="method-style"></a><span data-ttu-id="9fd74-1136">メソッド style</span><span class="sxs-lookup"><span data-stu-id="9fd74-1136">Method style</span></span>

<span data-ttu-id="9fd74-1137">フォームのスタイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1137">Specifies the style of the form.</span></span> <span data-ttu-id="9fd74-1138">このプロパティは、フォームで使用されているフォーム設計パターンを制御します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1138">This property controls the form design pattern being used with the form.</span></span> <span data-ttu-id="9fd74-1139">既定は自動です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1139">The default is Auto.</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="9fd74-1140">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="9fd74-1140">Parameters - style</span></span>

<span data-ttu-id="9fd74-1141">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1141">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="9fd74-1142">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="9fd74-1142">Return Value - style</span></span>

## <a name="method-text"></a><span data-ttu-id="9fd74-1143">メソッド text</span><span class="sxs-lookup"><span data-stu-id="9fd74-1143">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="9fd74-1144">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="9fd74-1144">Parameters - text</span></span>

<span data-ttu-id="9fd74-1145">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1145">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="9fd74-1146">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="9fd74-1146">Return Value - text</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="9fd74-1147">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="9fd74-1147">Method toolTip</span></span>

<span data-ttu-id="9fd74-1148">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1148">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="9fd74-1149">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="9fd74-1149">Return Value - toolTip</span></span>

<span data-ttu-id="9fd74-1150">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1150">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="9fd74-1151">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="9fd74-1151">Remarks - toolTip</span></span>

<span data-ttu-id="9fd74-1152">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1152">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="9fd74-1153">メソッド top</span><span class="sxs-lookup"><span data-stu-id="9fd74-1153">Method top</span></span>

<span data-ttu-id="9fd74-1154">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1154">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="9fd74-1155">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="9fd74-1155">Parameters - top</span></span>

<span data-ttu-id="9fd74-1156">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1156">value</span></span>  
<span data-ttu-id="9fd74-1157">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1157">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="9fd74-1158">モード</span><span class="sxs-lookup"><span data-stu-id="9fd74-1158">mode</span></span>  
<span data-ttu-id="9fd74-1159">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1159">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="9fd74-1160">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="9fd74-1160">Return Value - top</span></span>

<span data-ttu-id="9fd74-1161">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1161">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="9fd74-1162">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-1162">Method topMode</span></span>

<span data-ttu-id="9fd74-1163">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1163">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="9fd74-1164">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-1164">Parameters - topMode</span></span>

<span data-ttu-id="9fd74-1165">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1165">value</span></span>  
<span data-ttu-id="9fd74-1166">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1166">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="9fd74-1167">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-1167">Return Value - topMode</span></span>

<span data-ttu-id="9fd74-1168">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1168">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="9fd74-1169">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="9fd74-1169">Method topValue</span></span>

<span data-ttu-id="9fd74-1170">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1170">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="9fd74-1171">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="9fd74-1171">Parameters - topValue</span></span>

<span data-ttu-id="9fd74-1172">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1172">value</span></span>  
<span data-ttu-id="9fd74-1173">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1173">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="9fd74-1174">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="9fd74-1174">Return Value - topValue</span></span>

<span data-ttu-id="9fd74-1175">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1175">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="9fd74-1176">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="9fd74-1176">Method type</span></span>

<span data-ttu-id="9fd74-1177">コントロールのタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1177">Specifies the type of the control.</span></span> <span data-ttu-id="9fd74-1178">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9fd74-1178">Read-only.</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="9fd74-1179">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="9fd74-1179">Parameters - type</span></span>

<span data-ttu-id="9fd74-1180">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1180">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="9fd74-1181">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="9fd74-1181">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="9fd74-1182">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="9fd74-1182">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="9fd74-1183">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="9fd74-1183">Parameters - underline</span></span>

<span data-ttu-id="9fd74-1184">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1184">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="9fd74-1185">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="9fd74-1185">Return Value - underline</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="9fd74-1186">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="9fd74-1186">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="9fd74-1187">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="9fd74-1187">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="9fd74-1188">データ</span><span class="sxs-lookup"><span data-stu-id="9fd74-1188">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="9fd74-1189">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="9fd74-1189">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="9fd74-1190">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="9fd74-1190">Method userData</span></span>

<span data-ttu-id="9fd74-1191">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1191">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="9fd74-1192">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="9fd74-1192">Parameters - userData</span></span>

<span data-ttu-id="9fd74-1193">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1193">value</span></span>  
<span data-ttu-id="9fd74-1194">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1194">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="9fd74-1195">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="9fd74-1195">Return Value - userData</span></span>

<span data-ttu-id="9fd74-1196">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1196">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="9fd74-1197">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="9fd74-1197">Method userDataItem</span></span>

<span data-ttu-id="9fd74-1198">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1198">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="9fd74-1199">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="9fd74-1199">Parameters - userDataItem</span></span>

<span data-ttu-id="9fd74-1200">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1200">value</span></span>  
<span data-ttu-id="9fd74-1201">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1201">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="9fd74-1202">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="9fd74-1202">Return Value - userDataItem</span></span>

<span data-ttu-id="9fd74-1203">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1203">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="9fd74-1204">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="9fd74-1204">Method userDataItems</span></span>

<span data-ttu-id="9fd74-1205">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1205">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="9fd74-1206">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="9fd74-1206">Parameters - userDataItems</span></span>

<span data-ttu-id="9fd74-1207">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1207">value</span></span>  
<span data-ttu-id="9fd74-1208">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1208">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="9fd74-1209">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="9fd74-1209">Return Value - userDataItems</span></span>

<span data-ttu-id="9fd74-1210">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1210">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="9fd74-1211">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="9fd74-1211">Method userDisable</span></span>

<span data-ttu-id="9fd74-1212">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1212">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="9fd74-1213">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="9fd74-1213">Parameters - userDisable</span></span>

<span data-ttu-id="9fd74-1214">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1214">value</span></span>  
<span data-ttu-id="9fd74-1215">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1215">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="9fd74-1216">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="9fd74-1216">Return Value - userDisable</span></span>

<span data-ttu-id="9fd74-1217">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1217">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="9fd74-1218">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="9fd74-1218">Method userHeight</span></span>

<span data-ttu-id="9fd74-1219">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1219">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="9fd74-1220">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="9fd74-1220">Parameters - userHeight</span></span>

<span data-ttu-id="9fd74-1221">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1221">value</span></span>  
<span data-ttu-id="9fd74-1222">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1222">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="9fd74-1223">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="9fd74-1223">Return Value - userHeight</span></span>

<span data-ttu-id="9fd74-1224">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1224">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="9fd74-1225">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="9fd74-1225">Method userHide</span></span>

<span data-ttu-id="9fd74-1226">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1226">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="9fd74-1227">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="9fd74-1227">Parameters - userHide</span></span>

<span data-ttu-id="9fd74-1228">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1228">value</span></span>  
<span data-ttu-id="9fd74-1229">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1229">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="9fd74-1230">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="9fd74-1230">Return Value - userHide</span></span>

<span data-ttu-id="9fd74-1231">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1231">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="9fd74-1232">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="9fd74-1232">Remarks - userHide</span></span>

<span data-ttu-id="9fd74-1233">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1233">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="9fd74-1234">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1234">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="9fd74-1235">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1235">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="9fd74-1236">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="9fd74-1236">Method userOrgContainer</span></span>

<span data-ttu-id="9fd74-1237">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1237">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="9fd74-1238">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="9fd74-1238">Parameters - userOrgContainer</span></span>

<span data-ttu-id="9fd74-1239">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1239">value</span></span>  
<span data-ttu-id="9fd74-1240">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1240">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="9fd74-1241">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="9fd74-1241">Return Value - userOrgContainer</span></span>

<span data-ttu-id="9fd74-1242">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1242">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="9fd74-1243">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="9fd74-1243">Method userOrgSibling</span></span>

<span data-ttu-id="9fd74-1244">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1244">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="9fd74-1245">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="9fd74-1245">Parameters - userOrgSibling</span></span>

<span data-ttu-id="9fd74-1246">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1246">value</span></span>  
<span data-ttu-id="9fd74-1247">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1247">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="9fd74-1248">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="9fd74-1248">Return Value - userOrgSibling</span></span>

<span data-ttu-id="9fd74-1249">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1249">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="9fd74-1250">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="9fd74-1250">Method userPromptText</span></span>

<span data-ttu-id="9fd74-1251">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1251">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="9fd74-1252">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="9fd74-1252">Parameters - userPromptText</span></span>

<span data-ttu-id="9fd74-1253">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1253">value</span></span>  
<span data-ttu-id="9fd74-1254">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1254">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="9fd74-1255">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="9fd74-1255">Return Value - userPromptText</span></span>

<span data-ttu-id="9fd74-1256">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1256">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="9fd74-1257">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="9fd74-1257">Method userSecurityLevel</span></span>

<span data-ttu-id="9fd74-1258">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1258">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="9fd74-1259">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="9fd74-1259">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="9fd74-1260">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1260">value</span></span>  
<span data-ttu-id="9fd74-1261">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1261">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="9fd74-1262">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="9fd74-1262">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="9fd74-1263">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1263">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="9fd74-1264">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="9fd74-1264">Method userSkip</span></span>

<span data-ttu-id="9fd74-1265">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1265">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="9fd74-1266">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="9fd74-1266">Parameters - userSkip</span></span>

<span data-ttu-id="9fd74-1267">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1267">value</span></span>  
<span data-ttu-id="9fd74-1268">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1268">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="9fd74-1269">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1269">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="9fd74-1270">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="9fd74-1270">Return Value - userSkip</span></span>

<span data-ttu-id="9fd74-1271">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1271">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="9fd74-1272">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="9fd74-1272">Method userWidth</span></span>

<span data-ttu-id="9fd74-1273">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1273">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="9fd74-1274">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="9fd74-1274">Parameters - userWidth</span></span>

<span data-ttu-id="9fd74-1275">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1275">value</span></span>  
<span data-ttu-id="9fd74-1276">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1276">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="9fd74-1277">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="9fd74-1277">Return Value - userWidth</span></span>

<span data-ttu-id="9fd74-1278">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1278">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="9fd74-1279">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="9fd74-1279">Remarks - userWidth</span></span>

<span data-ttu-id="9fd74-1280">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1280">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="9fd74-1281">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1281">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="9fd74-1282">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1282">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-value"></a><span data-ttu-id="9fd74-1283">メソッド value</span><span class="sxs-lookup"><span data-stu-id="9fd74-1283">Method value</span></span>

```xpp
public boolean value([boolean value])
```

### <a name="parameters---value"></a><span data-ttu-id="9fd74-1284">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="9fd74-1284">Parameters - value</span></span>

<span data-ttu-id="9fd74-1285">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1285">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="9fd74-1286">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="9fd74-1286">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="9fd74-1287">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="9fd74-1287">Method verticalSpacing</span></span>

<span data-ttu-id="9fd74-1288">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1288">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="9fd74-1289">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="9fd74-1289">Parameters - verticalSpacing</span></span>

<span data-ttu-id="9fd74-1290">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1290">value</span></span>  
<span data-ttu-id="9fd74-1291">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1291">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="9fd74-1292">モード</span><span class="sxs-lookup"><span data-stu-id="9fd74-1292">mode</span></span>  
<span data-ttu-id="9fd74-1293">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1293">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="9fd74-1294">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="9fd74-1294">Return Value - verticalSpacing</span></span>

<span data-ttu-id="9fd74-1295">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1295">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="9fd74-1296">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-1296">Method verticalSpacingMode</span></span>

<span data-ttu-id="9fd74-1297">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1297">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="9fd74-1298">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-1298">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="9fd74-1299">モード</span><span class="sxs-lookup"><span data-stu-id="9fd74-1299">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="9fd74-1300">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-1300">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="9fd74-1301">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1301">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="9fd74-1302">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="9fd74-1302">Method verticalSpacingValue</span></span>

<span data-ttu-id="9fd74-1303">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1303">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="9fd74-1304">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="9fd74-1304">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="9fd74-1305">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1305">value</span></span>  
<span data-ttu-id="9fd74-1306">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1306">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="9fd74-1307">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="9fd74-1307">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="9fd74-1308">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1308">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="9fd74-1309">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="9fd74-1309">Method visible</span></span>

<span data-ttu-id="9fd74-1310">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1310">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="9fd74-1311">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="9fd74-1311">Parameters - visible</span></span>

<span data-ttu-id="9fd74-1312">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1312">value</span></span>  
<span data-ttu-id="9fd74-1313">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1313">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="9fd74-1314">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="9fd74-1314">Return Value - visible</span></span>

<span data-ttu-id="9fd74-1315">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1315">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="9fd74-1316">メソッド width</span><span class="sxs-lookup"><span data-stu-id="9fd74-1316">Method width</span></span>

<span data-ttu-id="9fd74-1317">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1317">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="9fd74-1318">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="9fd74-1318">Parameters - width</span></span>

<span data-ttu-id="9fd74-1319">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1319">value</span></span>  
<span data-ttu-id="9fd74-1320">幅の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1320">An integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="9fd74-1321">モード</span><span class="sxs-lookup"><span data-stu-id="9fd74-1321">mode</span></span>  
<span data-ttu-id="9fd74-1322">幅の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1322">An integer that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="9fd74-1323">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="9fd74-1323">Return Value - width</span></span>

<span data-ttu-id="9fd74-1324">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1324">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="9fd74-1325">備考 - width</span><span class="sxs-lookup"><span data-stu-id="9fd74-1325">Remarks - width</span></span>

<span data-ttu-id="9fd74-1326">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1326">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="9fd74-1327">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="9fd74-1327">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="9fd74-1328">モード。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1328">Mode.</span></span>           | <span data-ttu-id="9fd74-1329">幅計算。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1329">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd74-1330">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1330">-1 Exact.</span></span>       | <span data-ttu-id="9fd74-1331">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1331">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="9fd74-1332">0 自動。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1332">0 Auto.</span></span>         | <span data-ttu-id="9fd74-1333">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1333">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="9fd74-1334">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1334">1 Column width.</span></span> | <span data-ttu-id="9fd74-1335">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1335">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="9fd74-1336">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1336">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="9fd74-1337">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-1337">Method widthMode</span></span>

<span data-ttu-id="9fd74-1338">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1338">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="9fd74-1339">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-1339">Parameters - widthMode</span></span>

<span data-ttu-id="9fd74-1340">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1340">value</span></span>  
<span data-ttu-id="9fd74-1341">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1341">An integer value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="9fd74-1342">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-1342">Return Value - widthMode</span></span>

<span data-ttu-id="9fd74-1343">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1343">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="9fd74-1344">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-1344">Remarks - widthMode</span></span>

<span data-ttu-id="9fd74-1345">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="9fd74-1345">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="9fd74-1346">モード。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1346">Mode.</span></span>         | <span data-ttu-id="9fd74-1347">幅計算。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1347">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd74-1348">正確。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1348">Exact.</span></span>        | <span data-ttu-id="9fd74-1349">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1349">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="9fd74-1350">自動。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1350">Auto.</span></span>         | <span data-ttu-id="9fd74-1351">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1351">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="9fd74-1352">列の幅。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1352">Column width.</span></span> | <span data-ttu-id="9fd74-1353">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1353">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="9fd74-1354">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1354">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="9fd74-1355">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="9fd74-1355">Method widthValue</span></span>

<span data-ttu-id="9fd74-1356">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1356">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="9fd74-1357">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="9fd74-1357">Parameters - widthValue</span></span>

<span data-ttu-id="9fd74-1358">値</span><span class="sxs-lookup"><span data-stu-id="9fd74-1358">value</span></span>  
<span data-ttu-id="9fd74-1359">幅をピクセル単位で指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1359">An integer that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="9fd74-1360">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="9fd74-1360">Return Value - widthValue</span></span>

<span data-ttu-id="9fd74-1361">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1361">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="9fd74-1362">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="9fd74-1362">Remarks - widthValue</span></span>

<span data-ttu-id="9fd74-1363">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1363">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-gotfocus"></a><span data-ttu-id="9fd74-1364">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="9fd74-1364">Method gotFocus</span></span>

<span data-ttu-id="9fd74-1365">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1365">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-inputsearch"></a><span data-ttu-id="9fd74-1366">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="9fd74-1366">Method inputSearch</span></span>

<span data-ttu-id="9fd74-1367">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1367">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="9fd74-1368">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="9fd74-1368">Parameters - inputSearch</span></span>

<span data-ttu-id="9fd74-1369">searchStr</span><span class="sxs-lookup"><span data-stu-id="9fd74-1369">searchStr</span></span>  
<span data-ttu-id="9fd74-1370">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1370">The string value to use to filter data; optional.</span></span>

## <a name="method-filter"></a><span data-ttu-id="9fd74-1371">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="9fd74-1371">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="9fd74-1372">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="9fd74-1372">Parameters - filter</span></span>

<span data-ttu-id="9fd74-1373">filterStr</span><span class="sxs-lookup"><span data-stu-id="9fd74-1373">filterStr</span></span>  

## <a name="method-prefcolumnsize"></a><span data-ttu-id="9fd74-1374">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="9fd74-1374">Method prefColumnSize</span></span>

<span data-ttu-id="9fd74-1375">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1375">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="9fd74-1376">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="9fd74-1376">Parameters - prefColumnSize</span></span>

<span data-ttu-id="9fd74-1377">width</span><span class="sxs-lookup"><span data-stu-id="9fd74-1377">width</span></span>  
<span data-ttu-id="9fd74-1378">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1378">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="9fd74-1379">height</span><span class="sxs-lookup"><span data-stu-id="9fd74-1379">height</span></span>  
<span data-ttu-id="9fd74-1380">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1380">The preferred height of the control.</span></span>

## <a name="method-drop"></a><span data-ttu-id="9fd74-1381">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="9fd74-1381">Method drop</span></span>

<span data-ttu-id="9fd74-1382">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1382">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="9fd74-1383">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="9fd74-1383">Parameters - drop</span></span>

<span data-ttu-id="9fd74-1384">dragSource</span><span class="sxs-lookup"><span data-stu-id="9fd74-1384">dragSource</span></span>  
<span data-ttu-id="9fd74-1385">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1385">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="9fd74-1386">dragMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-1386">dragMode</span></span>  
<span data-ttu-id="9fd74-1387">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1387">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="9fd74-1388">x</span><span class="sxs-lookup"><span data-stu-id="9fd74-1388">x</span></span>  
<span data-ttu-id="9fd74-1389">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1389">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="9fd74-1390">y</span><span class="sxs-lookup"><span data-stu-id="9fd74-1390">y</span></span>  
<span data-ttu-id="9fd74-1391">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1391">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-mouseleave"></a><span data-ttu-id="9fd74-1392">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="9fd74-1392">Method mouseLeave</span></span>

<span data-ttu-id="9fd74-1393">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1393">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-ondialogclosed"></a><span data-ttu-id="9fd74-1394">メソッド OnDialogClosed</span><span class="sxs-lookup"><span data-stu-id="9fd74-1394">Method OnDialogClosed</span></span>

```xpp
private void OnDialogClosed([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ondialogclosed"></a><span data-ttu-id="9fd74-1395">パラメーター - OnDialogClosed</span><span class="sxs-lookup"><span data-stu-id="9fd74-1395">Parameters - OnDialogClosed</span></span>

<span data-ttu-id="9fd74-1396">sender</span><span class="sxs-lookup"><span data-stu-id="9fd74-1396">sender</span></span>  

<!-- -->

<span data-ttu-id="9fd74-1397">e</span><span class="sxs-lookup"><span data-stu-id="9fd74-1397">e</span></span>  

## <a name="method-clicked"></a><span data-ttu-id="9fd74-1398">メソッド clicked</span><span class="sxs-lookup"><span data-stu-id="9fd74-1398">Method clicked</span></span>

```xpp
public void clicked()
```

## <a name="method-onclicked"></a><span data-ttu-id="9fd74-1399">メソッド OnClicked</span><span class="sxs-lookup"><span data-stu-id="9fd74-1399">Method OnClicked</span></span>

```xpp
private void OnClicked([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onclicked"></a><span data-ttu-id="9fd74-1400">パラメーター - OnClicked</span><span class="sxs-lookup"><span data-stu-id="9fd74-1400">Parameters - OnClicked</span></span>

<span data-ttu-id="9fd74-1401">sender</span><span class="sxs-lookup"><span data-stu-id="9fd74-1401">sender</span></span>  

<!-- -->

<span data-ttu-id="9fd74-1402">e</span><span class="sxs-lookup"><span data-stu-id="9fd74-1402">e</span></span>  

## <a name="method-lostfocus"></a><span data-ttu-id="9fd74-1403">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="9fd74-1403">Method lostFocus</span></span>

<span data-ttu-id="9fd74-1404">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1404">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-jumpref"></a><span data-ttu-id="9fd74-1405">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="9fd74-1405">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-context"></a><span data-ttu-id="9fd74-1406">メソッド context</span><span class="sxs-lookup"><span data-stu-id="9fd74-1406">Method context</span></span>

<span data-ttu-id="9fd74-1407">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1407">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-displaycontrol"></a><span data-ttu-id="9fd74-1408">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="9fd74-1408">Method displayControl</span></span>

<span data-ttu-id="9fd74-1409">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1409">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-dialogclosed"></a><span data-ttu-id="9fd74-1410">メソッド dialogClosed</span><span class="sxs-lookup"><span data-stu-id="9fd74-1410">Method dialogClosed</span></span>

```xpp
public void dialogClosed(xFormRun formRun)
```

### <a name="parameters---dialogclosed"></a><span data-ttu-id="9fd74-1411">パラメーター - dialogClosed</span><span class="sxs-lookup"><span data-stu-id="9fd74-1411">Parameters - dialogClosed</span></span>

<span data-ttu-id="9fd74-1412">formRun</span><span class="sxs-lookup"><span data-stu-id="9fd74-1412">formRun</span></span>  

## <a name="method-enddrag"></a><span data-ttu-id="9fd74-1413">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="9fd74-1413">Method endDrag</span></span>

<span data-ttu-id="9fd74-1414">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1414">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="9fd74-1415">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="9fd74-1415">Remarks - endDrag</span></span>

<span data-ttu-id="9fd74-1416">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1416">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="9fd74-1417">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1417">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-dialoginitialized"></a><span data-ttu-id="9fd74-1418">メソッド dialogInitialized</span><span class="sxs-lookup"><span data-stu-id="9fd74-1418">Method dialogInitialized</span></span>

```xpp
public void dialogInitialized(xFormRun formRun)
```

### <a name="parameters---dialoginitialized"></a><span data-ttu-id="9fd74-1419">パラメーター - dialogInitialized</span><span class="sxs-lookup"><span data-stu-id="9fd74-1419">Parameters - dialogInitialized</span></span>

<span data-ttu-id="9fd74-1420">formRun</span><span class="sxs-lookup"><span data-stu-id="9fd74-1420">formRun</span></span>  

## <a name="method-onlostfocus"></a><span data-ttu-id="9fd74-1421">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="9fd74-1421">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="9fd74-1422">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="9fd74-1422">Parameters - OnLostFocus</span></span>

<span data-ttu-id="9fd74-1423">sender</span><span class="sxs-lookup"><span data-stu-id="9fd74-1423">sender</span></span>  

<!-- -->

<span data-ttu-id="9fd74-1424">e</span><span class="sxs-lookup"><span data-stu-id="9fd74-1424">e</span></span>  

## <a name="method-dropex"></a><span data-ttu-id="9fd74-1425">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="9fd74-1425">Method dropEx</span></span>

<span data-ttu-id="9fd74-1426">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1426">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="9fd74-1427">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="9fd74-1427">Parameters - dropEx</span></span>

<span data-ttu-id="9fd74-1428">dragSource</span><span class="sxs-lookup"><span data-stu-id="9fd74-1428">dragSource</span></span>  
<span data-ttu-id="9fd74-1429">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1429">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="9fd74-1430">dragMode</span><span class="sxs-lookup"><span data-stu-id="9fd74-1430">dragMode</span></span>  
<span data-ttu-id="9fd74-1431">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1431">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="9fd74-1432">x</span><span class="sxs-lookup"><span data-stu-id="9fd74-1432">x</span></span>  
<span data-ttu-id="9fd74-1433">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1433">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="9fd74-1434">y</span><span class="sxs-lookup"><span data-stu-id="9fd74-1434">y</span></span>  
<span data-ttu-id="9fd74-1435">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1435">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-ongotfocus"></a><span data-ttu-id="9fd74-1436">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="9fd74-1436">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="9fd74-1437">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="9fd74-1437">Parameters - OnGotFocus</span></span>

<span data-ttu-id="9fd74-1438">sender</span><span class="sxs-lookup"><span data-stu-id="9fd74-1438">sender</span></span>  

<!-- -->

<span data-ttu-id="9fd74-1439">e</span><span class="sxs-lookup"><span data-stu-id="9fd74-1439">e</span></span>  

## <a name="method-resetusersetting"></a><span data-ttu-id="9fd74-1440">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="9fd74-1440">Method resetUserSetting</span></span>

<span data-ttu-id="9fd74-1441">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1441">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-mouseenter"></a><span data-ttu-id="9fd74-1442">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="9fd74-1442">Method mouseEnter</span></span>

<span data-ttu-id="9fd74-1443">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1443">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="9fd74-1444">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="9fd74-1444">Parameters - mouseEnter</span></span>

<span data-ttu-id="9fd74-1445">x</span><span class="sxs-lookup"><span data-stu-id="9fd74-1445">x</span></span>  
<span data-ttu-id="9fd74-1446">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1446">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-1447">y</span><span class="sxs-lookup"><span data-stu-id="9fd74-1447">y</span></span>  
<span data-ttu-id="9fd74-1448">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1448">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-1449">ボタン</span><span class="sxs-lookup"><span data-stu-id="9fd74-1449">button</span></span>  
<span data-ttu-id="9fd74-1450">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1450">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-1451">Ctrl</span><span class="sxs-lookup"><span data-stu-id="9fd74-1451">Ctrl</span></span>  
<span data-ttu-id="9fd74-1452">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1452">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="9fd74-1453">シフト</span><span class="sxs-lookup"><span data-stu-id="9fd74-1453">Shift</span></span>  
<span data-ttu-id="9fd74-1454">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1454">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-setfocus"></a><span data-ttu-id="9fd74-1455">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="9fd74-1455">Method setFocus</span></span>

<span data-ttu-id="9fd74-1456">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1456">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-cut"></a><span data-ttu-id="9fd74-1457">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="9fd74-1457">Method cut</span></span>

<span data-ttu-id="9fd74-1458">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1458">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-dragleave"></a><span data-ttu-id="9fd74-1459">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="9fd74-1459">Method dragLeave</span></span>

<span data-ttu-id="9fd74-1460">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1460">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-paste"></a><span data-ttu-id="9fd74-1461">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="9fd74-1461">Method paste</span></span>

<span data-ttu-id="9fd74-1462">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1462">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-copy"></a><span data-ttu-id="9fd74-1463">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="9fd74-1463">Method copy</span></span>

<span data-ttu-id="9fd74-1464">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="9fd74-1464">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="9fd74-1465">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="9fd74-1465">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="9fd74-1466">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="9fd74-1466">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="9fd74-1467">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="9fd74-1467">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="9fd74-1468">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="9fd74-1468">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="9fd74-1469">overrideObject</span><span class="sxs-lookup"><span data-stu-id="9fd74-1469">overrideObject</span></span>  

