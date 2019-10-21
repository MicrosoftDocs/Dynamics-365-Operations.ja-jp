---
title: P クラス
description: 文字 P で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 52231
ms.assetid: 50842cd5-c27f-43aa-8a6d-bc9d3b02fd60
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aca67fe11e075a452d5eb45cfe90b1435b1f9e53
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183363"
---
# <a name="p-classes"></a><span data-ttu-id="d033e-103">P クラス</span><span class="sxs-lookup"><span data-stu-id="d033e-103">P classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d033e-104">文字 P で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="d033e-104">System API classes that start with the letter P.</span></span>

<a name="class-page"></a><span data-ttu-id="d033e-105">クラス ページ</span><span class="sxs-lookup"><span data-stu-id="d033e-105">Class Page</span></span>
----------

    class Page extends Object

<span data-ttu-id="d033e-106">このページ クラスでは、作成、読み取り、更新、および X++ コードおよびメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="d033e-106">This Page class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="d033e-107">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-107">Remarks</span></span>

<span data-ttu-id="d033e-108">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d033e-108">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="d033e-109">例</span><span class="sxs-lookup"><span data-stu-id="d033e-109">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d033e-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="d033e-110">Methods</span></span>

| <span data-ttu-id="d033e-111">方法</span><span class="sxs-lookup"><span data-stu-id="d033e-111">Method</span></span>                                                                        | <span data-ttu-id="d033e-112">説明</span><span class="sxs-lookup"><span data-stu-id="d033e-112">Description</span></span>                                                              |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="d033e-113">public boolean actionPaneControlEnabled(str controlName, \[boolean enabled\])</span><span class="sxs-lookup"><span data-stu-id="d033e-113">public boolean actionPaneControlEnabled(str controlName, \[boolean enabled\])</span></span> | <span data-ttu-id="d033e-114">アクション ウィンドウ上のコントロールの有効なプロパティの値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="d033e-114">Sets or gets the enabled property value of a control on the Action Pane.</span></span> |
| <span data-ttu-id="d033e-115">public boolean actionPaneControlVisible(str controlName, \[boolean visible\])</span><span class="sxs-lookup"><span data-stu-id="d033e-115">public boolean actionPaneControlVisible(str controlName, \[boolean visible\])</span></span> | <span data-ttu-id="d033e-116">アクション ウィンドウ上のコントロールの表示されるプロパティの値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="d033e-116">Sets or gets the visible property value of a control on the Action Pane.</span></span> |
| <span data-ttu-id="d033e-117">public Array activeActionPaneTabNames()</span><span class="sxs-lookup"><span data-stu-id="d033e-117">public Array activeActionPaneTabNames()</span></span>                                       |                                                                          |
| <span data-ttu-id="d033e-118">public Common activeRecord(str dataSourceName)</span><span class="sxs-lookup"><span data-stu-id="d033e-118">public Common activeRecord(str dataSourceName)</span></span>                                | <span data-ttu-id="d033e-119">特定のデータ ソース名の有効なレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="d033e-119">Gets the active record for the given data source name.</span></span>                   |
| <span data-ttu-id="d033e-120">public str name()</span><span class="sxs-lookup"><span data-stu-id="d033e-120">public str name()</span></span>                                                             | <span data-ttu-id="d033e-121">ページの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="d033e-121">Gets the name of the page.</span></span>                                               |
| <span data-ttu-id="d033e-122">public PageArgs pageArgs()</span><span class="sxs-lookup"><span data-stu-id="d033e-122">public PageArgs pageArgs()</span></span>                                                    | <span data-ttu-id="d033e-123">page 引数を取得します。</span><span class="sxs-lookup"><span data-stu-id="d033e-123">Gets the page arguments.</span></span>                                                 |
| <span data-ttu-id="d033e-124">public xFormRun formRun()</span><span class="sxs-lookup"><span data-stu-id="d033e-124">public xFormRun formRun()</span></span>                                                     |                                                                          |

### <a name="method-actionpanecontrolenabled"></a><span data-ttu-id="d033e-125">メソッド actionPaneControlEnabled</span><span class="sxs-lookup"><span data-stu-id="d033e-125">Method actionPaneControlEnabled</span></span>

<span data-ttu-id="d033e-126">アクション ウィンドウ上のコントロールの有効なプロパティの値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="d033e-126">Sets or gets the enabled property value of a control on the Action Pane.</span></span>

    public boolean actionPaneControlEnabled(str controlName, [boolean enabled])

#### <a name="parameters"></a><span data-ttu-id="d033e-127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-127">Parameters</span></span>

<span data-ttu-id="d033e-128">controlName</span><span class="sxs-lookup"><span data-stu-id="d033e-128">controlName</span></span>  
<span data-ttu-id="d033e-129">アクション ウィンドウ コントロールが有効かどうかを指定する値、オプション。</span><span class="sxs-lookup"><span data-stu-id="d033e-129">A value that specifies whether the Action Pane control is enabled; optional.</span></span>

<!-- -->

<span data-ttu-id="d033e-130">有効</span><span class="sxs-lookup"><span data-stu-id="d033e-130">enabled</span></span>  
<span data-ttu-id="d033e-131">アクション ウィンドウ コントロールが有効かどうかを指定する値、オプション。</span><span class="sxs-lookup"><span data-stu-id="d033e-131">A value that specifies whether the Action Pane control is enabled; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d033e-132">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-132">Return Value</span></span>

<span data-ttu-id="d033e-133">アクション ペイン コントロールが有効かどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="d033e-133">A Boolean value that indicates whether the Action Pane control is enabled.</span></span>

### <a name="method-actionpanecontrolvisible"></a><span data-ttu-id="d033e-134">メソッド actionPaneControlVisible</span><span class="sxs-lookup"><span data-stu-id="d033e-134">Method actionPaneControlVisible</span></span>

<span data-ttu-id="d033e-135">アクション ウィンドウ上のコントロールの表示されるプロパティの値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="d033e-135">Sets or gets the visible property value of a control on the Action Pane.</span></span>

    public boolean actionPaneControlVisible(str controlName, [boolean visible])

#### <a name="parameters"></a><span data-ttu-id="d033e-136">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-136">Parameters</span></span>

<span data-ttu-id="d033e-137">controlName</span><span class="sxs-lookup"><span data-stu-id="d033e-137">controlName</span></span>  
<span data-ttu-id="d033e-138">アクション ウィンドウ コントロールが表示されるかどうかを指定する値、オプション。</span><span class="sxs-lookup"><span data-stu-id="d033e-138">A value that specifies whether the Action Pane control is visible; optional.</span></span>

<!-- -->

<span data-ttu-id="d033e-139">表示</span><span class="sxs-lookup"><span data-stu-id="d033e-139">visible</span></span>  
<span data-ttu-id="d033e-140">アクション ウィンドウ コントロールが表示されるかどうかを指定する値、オプション。</span><span class="sxs-lookup"><span data-stu-id="d033e-140">A value that specifies whether the Action Pane control is visible; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d033e-141">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-141">Return Value</span></span>

<span data-ttu-id="d033e-142">アクション ペイン コントロールが表示されるかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="d033e-142">A Boolean value that indicates whether the Action Pane control is visible.</span></span>

### <a name="method-activeactionpanetabnames"></a><span data-ttu-id="d033e-143">メソッド activeActionPaneTabNames</span><span class="sxs-lookup"><span data-stu-id="d033e-143">Method activeActionPaneTabNames</span></span>

    public Array activeActionPaneTabNames()

#### <a name="return-value"></a><span data-ttu-id="d033e-144">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-144">Return Value</span></span>

### <a name="method-activerecord"></a><span data-ttu-id="d033e-145">メソッド activeRecord</span><span class="sxs-lookup"><span data-stu-id="d033e-145">Method activeRecord</span></span>

<span data-ttu-id="d033e-146">特定のデータ ソース名の有効なレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="d033e-146">Gets the active record for the given data source name.</span></span>

    public Common activeRecord(str dataSourceName)

#### <a name="parameters"></a><span data-ttu-id="d033e-147">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-147">Parameters</span></span>

<span data-ttu-id="d033e-148">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="d033e-148">dataSourceName</span></span>  
<span data-ttu-id="d033e-149">検索するデータ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="d033e-149">The name of the data source to search on.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d033e-150">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-150">Return Value</span></span>

<span data-ttu-id="d033e-151">特定のデータ ソース用の有効なレコード。</span><span class="sxs-lookup"><span data-stu-id="d033e-151">The active record for the given data source.</span></span>

### <a name="method-name"></a><span data-ttu-id="d033e-152">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d033e-152">Method name</span></span>

<span data-ttu-id="d033e-153">ページの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="d033e-153">Gets the name of the page.</span></span>

    public str name()

#### <a name="return-value"></a><span data-ttu-id="d033e-154">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-154">Return Value</span></span>

<span data-ttu-id="d033e-155">ページ名。</span><span class="sxs-lookup"><span data-stu-id="d033e-155">The page name.</span></span>

### <a name="method-pageargs"></a><span data-ttu-id="d033e-156">メソッド pageArgs</span><span class="sxs-lookup"><span data-stu-id="d033e-156">Method pageArgs</span></span>

<span data-ttu-id="d033e-157">page 引数を取得します。</span><span class="sxs-lookup"><span data-stu-id="d033e-157">Gets the page arguments.</span></span>

    public PageArgs pageArgs()

#### <a name="return-value"></a><span data-ttu-id="d033e-158">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-158">Return Value</span></span>

<span data-ttu-id="d033e-159">page 引数。</span><span class="sxs-lookup"><span data-stu-id="d033e-159">The page arguments.</span></span>

### <a name="method-formrun"></a><span data-ttu-id="d033e-160">メソッド formRun</span><span class="sxs-lookup"><span data-stu-id="d033e-160">Method formRun</span></span>

    public xFormRun formRun()

#### <a name="return-value"></a><span data-ttu-id="d033e-161">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-161">Return Value</span></span>

## <a name="class-pageargs"></a><span data-ttu-id="d033e-162">クラス PageArgs</span><span class="sxs-lookup"><span data-stu-id="d033e-162">Class PageArgs</span></span>
    class PageArgs extends Object

<span data-ttu-id="d033e-163">PageArgs クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="d033e-163">The PageArgs class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="d033e-164">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-164">Remarks</span></span>

<span data-ttu-id="d033e-165">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d033e-165">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="d033e-166">例</span><span class="sxs-lookup"><span data-stu-id="d033e-166">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d033e-167">メソッド</span><span class="sxs-lookup"><span data-stu-id="d033e-167">Methods</span></span>

| <span data-ttu-id="d033e-168">方法</span><span class="sxs-lookup"><span data-stu-id="d033e-168">Method</span></span>                                         | <span data-ttu-id="d033e-169">説明</span><span class="sxs-lookup"><span data-stu-id="d033e-169">Description</span></span>                                                                                                 |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d033e-170">public int enumParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d033e-170">public int enumParameter(\[int value\])</span></span>        | <span data-ttu-id="d033e-171">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-171">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span> |
| <span data-ttu-id="d033e-172">public int enumTypeParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d033e-172">public int enumTypeParameter(\[int value\])</span></span>    | <span data-ttu-id="d033e-173">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-173">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>                                     |
| <span data-ttu-id="d033e-174">public Common externalRecord(\[Common value\])</span><span class="sxs-lookup"><span data-stu-id="d033e-174">public Common externalRecord(\[Common value\])</span></span> |                                                                                                             |
| <span data-ttu-id="d033e-175">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d033e-175">public str menuItemName(\[str value\])</span></span>         |                                                                                                             |
| <span data-ttu-id="d033e-176">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d033e-176">public str parameters(\[str value\])</span></span>           | <span data-ttu-id="d033e-177">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-177">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>      |
| <span data-ttu-id="d033e-178">public void new()</span><span class="sxs-lookup"><span data-stu-id="d033e-178">public void new()</span></span>                              | <span data-ttu-id="d033e-179">PageArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-179">Initializes a new instance of the PageArgs class.</span></span>                                                           |

### <a name="method-enumparameter"></a><span data-ttu-id="d033e-180">メソッド enumParameter</span><span class="sxs-lookup"><span data-stu-id="d033e-180">Method enumParameter</span></span>

<span data-ttu-id="d033e-181">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-181">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

    public int enumParameter([int value])

#### <a name="parameters"></a><span data-ttu-id="d033e-182">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-182">Parameters</span></span>

<span data-ttu-id="d033e-183">値</span><span class="sxs-lookup"><span data-stu-id="d033e-183">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-184">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-184">Return Value</span></span>

<span data-ttu-id="d033e-185">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="d033e-185">The enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

### <a name="method-enumtypeparameter"></a><span data-ttu-id="d033e-186">メソッド enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="d033e-186">Method enumTypeParameter</span></span>

<span data-ttu-id="d033e-187">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-187">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>

    public int enumTypeParameter([int value])

#### <a name="parameters"></a><span data-ttu-id="d033e-188">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-188">Parameters</span></span>

<span data-ttu-id="d033e-189">値</span><span class="sxs-lookup"><span data-stu-id="d033e-189">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-190">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-190">Return Value</span></span>

<span data-ttu-id="d033e-191">MenuFunction クラスの enumTypeParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="d033e-191">The enumTypeParameter property for the MenuFunction class.</span></span>

### <a name="method-externalrecord"></a><span data-ttu-id="d033e-192">メソッド externalRecord</span><span class="sxs-lookup"><span data-stu-id="d033e-192">Method externalRecord</span></span>

    public Common externalRecord([Common value])

#### <a name="parameters"></a><span data-ttu-id="d033e-193">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-193">Parameters</span></span>

<span data-ttu-id="d033e-194">値</span><span class="sxs-lookup"><span data-stu-id="d033e-194">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-195">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-195">Return Value</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="d033e-196">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="d033e-196">Method menuItemName</span></span>

    public str menuItemName([str value])

#### <a name="parameters"></a><span data-ttu-id="d033e-197">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-197">Parameters</span></span>

<span data-ttu-id="d033e-198">値</span><span class="sxs-lookup"><span data-stu-id="d033e-198">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-199">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-199">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="d033e-200">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="d033e-200">Method parameters</span></span>

<span data-ttu-id="d033e-201">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-201">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="d033e-202">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-202">Parameters</span></span>

<span data-ttu-id="d033e-203">値</span><span class="sxs-lookup"><span data-stu-id="d033e-203">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-204">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-204">Return Value</span></span>

<span data-ttu-id="d033e-205">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="d033e-205">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-206">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-206">Remarks</span></span>

<span data-ttu-id="d033e-207">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="d033e-207">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="d033e-208">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="d033e-208">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-new"></a><span data-ttu-id="d033e-209">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d033e-209">Method new</span></span>

<span data-ttu-id="d033e-210">PageArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-210">Initializes a new instance of the PageArgs class.</span></span>

    public void new()

## <a name="class-pageinteraction"></a><span data-ttu-id="d033e-211">クラス PageInteraction</span><span class="sxs-lookup"><span data-stu-id="d033e-211">Class PageInteraction</span></span>
    class PageInteraction extends Object

<span data-ttu-id="d033e-212">PageInteraction クラスは、リスト ページとやり取りするための機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="d033e-212">The PageInteraction class provides functionality for interacting with a list page.</span></span>

### <a name="remarks"></a><span data-ttu-id="d033e-213">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-213">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d033e-214">例</span><span class="sxs-lookup"><span data-stu-id="d033e-214">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d033e-215">メソッド</span><span class="sxs-lookup"><span data-stu-id="d033e-215">Methods</span></span>

| <span data-ttu-id="d033e-216">方法</span><span class="sxs-lookup"><span data-stu-id="d033e-216">Method</span></span>                                           | <span data-ttu-id="d033e-217">説明</span><span class="sxs-lookup"><span data-stu-id="d033e-217">Description</span></span>                                                        |
|--------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d033e-218">public Page page()</span><span class="sxs-lookup"><span data-stu-id="d033e-218">public Page page()</span></span>                               | <span data-ttu-id="d033e-219">ListPage インスタンスを取得します。</span><span class="sxs-lookup"><span data-stu-id="d033e-219">Gets the ListPage instance.</span></span>                                        |
| <span data-ttu-id="d033e-220">public void tabChanged(container activeTabNames)</span><span class="sxs-lookup"><span data-stu-id="d033e-220">public void tabChanged(container activeTabNames)</span></span> |                                                                    |
| <span data-ttu-id="d033e-221">public void new(Page page)</span><span class="sxs-lookup"><span data-stu-id="d033e-221">public void new(Page page)</span></span>                       | <span data-ttu-id="d033e-222">リスト ページ上で動作する新しい PageInteraction オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="d033e-222">Creates a new PageInteraction object that operates on a list page.</span></span> |

### <a name="method-page"></a><span data-ttu-id="d033e-223">メソッド page</span><span class="sxs-lookup"><span data-stu-id="d033e-223">Method page</span></span>

<span data-ttu-id="d033e-224">ListPage インスタンスを取得します。</span><span class="sxs-lookup"><span data-stu-id="d033e-224">Gets the ListPage instance.</span></span>

    public Page page()

#### <a name="return-value"></a><span data-ttu-id="d033e-225">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-225">Return Value</span></span>

<span data-ttu-id="d033e-226">この PageInteraction インスタンスの ListPage インスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-226">Returns the ListPage instance for this PageInteraction instance.</span></span>

### <a name="method-tabchanged"></a><span data-ttu-id="d033e-227">メソッド tabChanged</span><span class="sxs-lookup"><span data-stu-id="d033e-227">Method tabChanged</span></span>

    public void tabChanged(container activeTabNames)

#### <a name="parameters"></a><span data-ttu-id="d033e-228">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-228">Parameters</span></span>

<span data-ttu-id="d033e-229">activeTabNames</span><span class="sxs-lookup"><span data-stu-id="d033e-229">activeTabNames</span></span>  

### <a name="method-new"></a><span data-ttu-id="d033e-230">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d033e-230">Method new</span></span>

<span data-ttu-id="d033e-231">リスト ページ上で動作する新しい PageInteraction オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="d033e-231">Creates a new PageInteraction object that operates on a list page.</span></span>

    public void new(Page page)

#### <a name="parameters"></a><span data-ttu-id="d033e-232">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-232">Parameters</span></span>

<span data-ttu-id="d033e-233">ページ</span><span class="sxs-lookup"><span data-stu-id="d033e-233">page</span></span>  

## <a name="class-partlist"></a><span data-ttu-id="d033e-234">クラス PartList</span><span class="sxs-lookup"><span data-stu-id="d033e-234">Class PartList</span></span>
    class PartList extends Object

### <a name="remarks"></a><span data-ttu-id="d033e-235">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-235">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d033e-236">例</span><span class="sxs-lookup"><span data-stu-id="d033e-236">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d033e-237">メソッド</span><span class="sxs-lookup"><span data-stu-id="d033e-237">Methods</span></span>

| <span data-ttu-id="d033e-238">方法</span><span class="sxs-lookup"><span data-stu-id="d033e-238">Method</span></span>                                        | <span data-ttu-id="d033e-239">説明</span><span class="sxs-lookup"><span data-stu-id="d033e-239">Description</span></span>                                     |
|-----------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="d033e-240">public xFormRun getPartById(int id)</span><span class="sxs-lookup"><span data-stu-id="d033e-240">public xFormRun getPartById(int id)</span></span>           |                                                 |
| <span data-ttu-id="d033e-241">public FormControl getPartControlById(int id)</span><span class="sxs-lookup"><span data-stu-id="d033e-241">public FormControl getPartControlById(int id)</span></span> |                                                 |
| <span data-ttu-id="d033e-242">public int partCount()</span><span class="sxs-lookup"><span data-stu-id="d033e-242">public int partCount()</span></span>                        |                                                 |
| <span data-ttu-id="d033e-243">public void new(xFormRun form)</span><span class="sxs-lookup"><span data-stu-id="d033e-243">public void new(xFormRun form)</span></span>                | <span data-ttu-id="d033e-244">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-244">Initializes a new instance of the Object class.</span></span> |
| <span data-ttu-id="d033e-245">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="d033e-245">public void finalize()</span></span>                        |                                                 |

### <a name="method-getpartbyid"></a><span data-ttu-id="d033e-246">メソッド getPartById</span><span class="sxs-lookup"><span data-stu-id="d033e-246">Method getPartById</span></span>

    public xFormRun getPartById(int id)

#### <a name="parameters"></a><span data-ttu-id="d033e-247">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-247">Parameters</span></span>

<span data-ttu-id="d033e-248">id</span><span class="sxs-lookup"><span data-stu-id="d033e-248">id</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-249">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-249">Return Value</span></span>

### <a name="method-getpartcontrolbyid"></a><span data-ttu-id="d033e-250">メソッド getPartControlById</span><span class="sxs-lookup"><span data-stu-id="d033e-250">Method getPartControlById</span></span>

    public FormControl getPartControlById(int id)

#### <a name="parameters"></a><span data-ttu-id="d033e-251">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-251">Parameters</span></span>

<span data-ttu-id="d033e-252">id</span><span class="sxs-lookup"><span data-stu-id="d033e-252">id</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-253">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-253">Return Value</span></span>

### <a name="method-partcount"></a><span data-ttu-id="d033e-254">メソッド partCount</span><span class="sxs-lookup"><span data-stu-id="d033e-254">Method partCount</span></span>

    public int partCount()

#### <a name="return-value"></a><span data-ttu-id="d033e-255">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-255">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d033e-256">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d033e-256">Method new</span></span>

<span data-ttu-id="d033e-257">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-257">Initializes a new instance of the Object class.</span></span>

    public void new(xFormRun form)

#### <a name="parameters"></a><span data-ttu-id="d033e-258">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-258">Parameters</span></span>

<span data-ttu-id="d033e-259">フォーム</span><span class="sxs-lookup"><span data-stu-id="d033e-259">form</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="d033e-260">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="d033e-260">Method finalize</span></span>

    public void finalize()

## <a name="class-percentbar"></a><span data-ttu-id="d033e-261">クラス Percentbar</span><span class="sxs-lookup"><span data-stu-id="d033e-261">Class Percentbar</span></span>
    class Percentbar extends Object

### <a name="remarks"></a><span data-ttu-id="d033e-262">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-262">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d033e-263">例</span><span class="sxs-lookup"><span data-stu-id="d033e-263">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d033e-264">メソッド</span><span class="sxs-lookup"><span data-stu-id="d033e-264">Methods</span></span>

| <span data-ttu-id="d033e-265">方法</span><span class="sxs-lookup"><span data-stu-id="d033e-265">Method</span></span>                                   | <span data-ttu-id="d033e-266">説明</span><span class="sxs-lookup"><span data-stu-id="d033e-266">Description</span></span>                                         |
|------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="d033e-267">public void new(int maxCount, str title)</span><span class="sxs-lookup"><span data-stu-id="d033e-267">public void new(int maxCount, str title)</span></span> | <span data-ttu-id="d033e-268">Percentbar クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-268">Initializes a new instance of the Percentbar class.</span></span> |
| <span data-ttu-id="d033e-269">public void set(int count)</span><span class="sxs-lookup"><span data-stu-id="d033e-269">public void set(int count)</span></span>               |                                                     |
| <span data-ttu-id="d033e-270">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="d033e-270">public void finalize()</span></span>                   |                                                     |

### <a name="method-new"></a><span data-ttu-id="d033e-271">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d033e-271">Method new</span></span>

<span data-ttu-id="d033e-272">Percentbar クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-272">Initializes a new instance of the Percentbar class.</span></span>

    public void new(int maxCount, str title)

#### <a name="parameters"></a><span data-ttu-id="d033e-273">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-273">Parameters</span></span>

<span data-ttu-id="d033e-274">maxCount</span><span class="sxs-lookup"><span data-stu-id="d033e-274">maxCount</span></span>  

<!-- -->

<span data-ttu-id="d033e-275">title</span><span class="sxs-lookup"><span data-stu-id="d033e-275">title</span></span>  

### <a name="method-set"></a><span data-ttu-id="d033e-276">メソッド set</span><span class="sxs-lookup"><span data-stu-id="d033e-276">Method set</span></span>

    public void set(int count)

#### <a name="parameters"></a><span data-ttu-id="d033e-277">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-277">Parameters</span></span>

<span data-ttu-id="d033e-278">カウント</span><span class="sxs-lookup"><span data-stu-id="d033e-278">count</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="d033e-279">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="d033e-279">Method finalize</span></span>

    public void finalize()

## <a name="class-performancemonitor"></a><span data-ttu-id="d033e-280">クラス PerformanceMonitor</span><span class="sxs-lookup"><span data-stu-id="d033e-280">Class PerformanceMonitor</span></span>
    class PerformanceMonitor extends Object

<span data-ttu-id="d033e-281">PerformanceMonitor クラスは、システムで実行されているプロセスのデータをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="d033e-281">The PerformanceMonitor class fetches data for processes that are running on the system.</span></span>

### <a name="remarks"></a><span data-ttu-id="d033e-282">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-282">Remarks</span></span>

<span data-ttu-id="d033e-283">いつでもシステムのスナップショットを取得して、システムで実行されている任意のプロセスのカウンター上で移動することができます。</span><span class="sxs-lookup"><span data-stu-id="d033e-283">You can take a snapshot of the system at any time and traverse the counters for any process that is running on the system.</span></span>

### <a name="examples"></a><span data-ttu-id="d033e-284">例</span><span class="sxs-lookup"><span data-stu-id="d033e-284">Examples</span></span>

<span data-ttu-id="d033e-285">次の例は、現在実行中のすべてのプロセスの processId および workingset 値を出力します。</span><span class="sxs-lookup"><span data-stu-id="d033e-285">The following example prints the processId and workingset values for all the currently running processes.</span></span>

    static void pvPerformanceMonitorTest(args a) 
    { 
        int i, j;  
        PerformanceMonitorInstance instance;  
        PerformanceMonitorCounter counter1, counter2;  
        PerformanceMonitor pm = new PerformanceMonitor();  
        // Take a current snapshot of the system. 
        pm.takeSnapshot ();  
        // Traverse all the running processes. 
        for (i= 1; i <= pm.instanceCount(); i++)  
        {  
            instance = pm.instance(i);  
            counter1 = instance.getCounter("ID Process");  
            counter2 = instance.getCounter("Working Set");  
            print instance.name(), " ",  
            counter1.intData(), " ",  
            counter2.intData();  
        } 
        pause;  
    }

### <a name="methods"></a><span data-ttu-id="d033e-286">メソッド</span><span class="sxs-lookup"><span data-stu-id="d033e-286">Methods</span></span>

| <span data-ttu-id="d033e-287">方法</span><span class="sxs-lookup"><span data-stu-id="d033e-287">Method</span></span>                                                     | <span data-ttu-id="d033e-288">説明</span><span class="sxs-lookup"><span data-stu-id="d033e-288">Description</span></span>                                                                                    |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d033e-289">public PerformanceMonitorInstance instance(int instanceNo)</span><span class="sxs-lookup"><span data-stu-id="d033e-289">public PerformanceMonitorInstance instance(int instanceNo)</span></span> |                                                                                                |
| <span data-ttu-id="d033e-290">public int instanceCount()</span><span class="sxs-lookup"><span data-stu-id="d033e-290">public int instanceCount()</span></span>                                 | <span data-ttu-id="d033e-291">インスタンス数 (現在のスナップショットのプロセスの数) を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-291">Returns the instance count, which is the number of processes in the current snapshot.</span></span>          |
| <span data-ttu-id="d033e-292">public int processId()</span><span class="sxs-lookup"><span data-stu-id="d033e-292">public int processId()</span></span>                                     | <span data-ttu-id="d033e-293">このメソッドを実行しているプロセスの processId 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-293">Returns the processId value of the process that is running this method.</span></span>                        |
| <span data-ttu-id="d033e-294">public str systemName()</span><span class="sxs-lookup"><span data-stu-id="d033e-294">public str systemName()</span></span>                                    |                                                                                                |
| <span data-ttu-id="d033e-295">public boolean takeSnapshot(\[str processName\])</span><span class="sxs-lookup"><span data-stu-id="d033e-295">public boolean takeSnapshot(\[str processName\])</span></span>           |                                                                                                |
| <span data-ttu-id="d033e-296">public str toString()</span><span class="sxs-lookup"><span data-stu-id="d033e-296">public str toString()</span></span>                                      | <span data-ttu-id="d033e-297">クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-297">Returns a string that contains the class handle and name, and possibly additional information.</span></span> |
| <span data-ttu-id="d033e-298">public void new()</span><span class="sxs-lookup"><span data-stu-id="d033e-298">public void new()</span></span>                                          | <span data-ttu-id="d033e-299">PerformanceMonitor クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-299">Initializes a new instance of the PerformanceMonitor class.</span></span>                                    |

### <a name="method-instance"></a><span data-ttu-id="d033e-300">メソッド instance</span><span class="sxs-lookup"><span data-stu-id="d033e-300">Method instance</span></span>

    public PerformanceMonitorInstance instance(int instanceNo)

#### <a name="parameters"></a><span data-ttu-id="d033e-301">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-301">Parameters</span></span>

<span data-ttu-id="d033e-302">instanceNo</span><span class="sxs-lookup"><span data-stu-id="d033e-302">instanceNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-303">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-303">Return Value</span></span>

### <a name="method-instancecount"></a><span data-ttu-id="d033e-304">メソッド instanceCount</span><span class="sxs-lookup"><span data-stu-id="d033e-304">Method instanceCount</span></span>

<span data-ttu-id="d033e-305">インスタンス数 (現在のスナップショットのプロセスの数) を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-305">Returns the instance count, which is the number of processes in the current snapshot.</span></span>

    public int instanceCount()

#### <a name="return-value"></a><span data-ttu-id="d033e-306">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-306">Return Value</span></span>

<span data-ttu-id="d033e-307">現在のスナップショット内のプロセス数。</span><span class="sxs-lookup"><span data-stu-id="d033e-307">The number of processes in the current snapshot.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-308">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-308">Remarks</span></span>

<span data-ttu-id="d033e-309">現在実行中のプロセスのスナップショットを取得するには、takeSnapshot メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d033e-309">Use the takeSnapshot method to take a snapshot of the currently running processes.</span></span>

#### <a name="examples"></a><span data-ttu-id="d033e-310">例</span><span class="sxs-lookup"><span data-stu-id="d033e-310">Examples</span></span>

    static void pvPerformanceMonitorTest(args a) 
    { 
        int i, j; 
        PerformanceMonitorInstance instance; 
        PerformanceMonitorCounter counter1, counter2; 
        PerformanceMonitor pm = new PerformanceMonitor(); 
        // Take a current snapshot of the system. 
        pm.takeSnapshot (); 
        // Traverse all the running processes. 
        for (i= 1; i <= pm.instanceCount(); i++) 
        { 
            instance = pm.instance(i); 
            counter1 = instance.getCounter("ID Process"); 
            counter2 = instance.getCounter("Working Set"); 
            print instance.name(), " ",  
                counter1.intData(), " ",  
                counter2.intData(); 
        } 
        pause; 
    }

### <a name="method-processid"></a><span data-ttu-id="d033e-311">メソッド processId</span><span class="sxs-lookup"><span data-stu-id="d033e-311">Method processId</span></span>

<span data-ttu-id="d033e-312">このメソッドを実行しているプロセスの processId 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-312">Returns the processId value of the process that is running this method.</span></span>

    public int processId()

#### <a name="return-value"></a><span data-ttu-id="d033e-313">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-313">Return Value</span></span>

<span data-ttu-id="d033e-314">このメソッドを実行しているプロセスの processId 値です。</span><span class="sxs-lookup"><span data-stu-id="d033e-314">The processId value of the process that is running this method.</span></span>

#### <a name="examples"></a><span data-ttu-id="d033e-315">例</span><span class="sxs-lookup"><span data-stu-id="d033e-315">Examples</span></span>

    static void processIdDemo(args a) 
    { 
        PerformanceMonitor pm = new PerformanceMonitor(); 
        print pm.processId(); 
        pause; 
    }

### <a name="method-systemname"></a><span data-ttu-id="d033e-316">メソッド systemName</span><span class="sxs-lookup"><span data-stu-id="d033e-316">Method systemName</span></span>

    public str systemName()

#### <a name="return-value"></a><span data-ttu-id="d033e-317">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-317">Return Value</span></span>

### <a name="method-takesnapshot"></a><span data-ttu-id="d033e-318">メソッド takeSnapshot</span><span class="sxs-lookup"><span data-stu-id="d033e-318">Method takeSnapshot</span></span>

    public boolean takeSnapshot([str processName])

#### <a name="parameters"></a><span data-ttu-id="d033e-319">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-319">Parameters</span></span>

<span data-ttu-id="d033e-320">processName</span><span class="sxs-lookup"><span data-stu-id="d033e-320">processName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-321">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-321">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="d033e-322">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="d033e-322">Method toString</span></span>

<span data-ttu-id="d033e-323">クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-323">Returns a string that contains the class handle and name, and possibly additional information.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="d033e-324">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-324">Return Value</span></span>

<span data-ttu-id="d033e-325">クラスのテキストの説明。</span><span class="sxs-lookup"><span data-stu-id="d033e-325">A textual description of the class.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-326">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-326">Remarks</span></span>

<span data-ttu-id="d033e-327">既定では、ほとんどのクラスは、toString メソッドがクラス ハンドルおよび名前を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-327">By default, for most classes, the toString method returns a string that contains the class handle and name.</span></span> <span data-ttu-id="d033e-328">ただし、一部のクラスでは、追加情報が文字列で返されます。</span><span class="sxs-lookup"><span data-stu-id="d033e-328">However, in some classes, additional information is returned in the string.</span></span>

### <a name="method-new"></a><span data-ttu-id="d033e-329">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d033e-329">Method new</span></span>

<span data-ttu-id="d033e-330">PerformanceMonitor クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-330">Initializes a new instance of the PerformanceMonitor class.</span></span>

    public void new()

## <a name="class-performancemonitorcounter"></a><span data-ttu-id="d033e-331">クラス PerformanceMonitorCounter</span><span class="sxs-lookup"><span data-stu-id="d033e-331">Class PerformanceMonitorCounter</span></span>
    class PerformanceMonitorCounter extends Object

<span data-ttu-id="d033e-332">PerformanceMonitorCounter クラスでは、特定のスナップショットの特定のインスタンスに割り当てられているカウンターを識別します。</span><span class="sxs-lookup"><span data-stu-id="d033e-332">The PerformanceMonitorCounter class identifies a counter that is assigned to a particular instance of a particular snapshot.</span></span>

### <a name="remarks"></a><span data-ttu-id="d033e-333">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-333">Remarks</span></span>

<span data-ttu-id="d033e-334">get メソッドを使用してデータを取得できます。</span><span class="sxs-lookup"><span data-stu-id="d033e-334">The data can be fetched by using the get methods.</span></span>

### <a name="examples"></a><span data-ttu-id="d033e-335">例</span><span class="sxs-lookup"><span data-stu-id="d033e-335">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d033e-336">メソッド</span><span class="sxs-lookup"><span data-stu-id="d033e-336">Methods</span></span>

| <span data-ttu-id="d033e-337">方法</span><span class="sxs-lookup"><span data-stu-id="d033e-337">Method</span></span>                 | <span data-ttu-id="d033e-338">説明</span><span class="sxs-lookup"><span data-stu-id="d033e-338">Description</span></span>                                                                                    |
|------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d033e-339">public int intData()</span><span class="sxs-lookup"><span data-stu-id="d033e-339">public int intData()</span></span>   |                                                                                                |
| <span data-ttu-id="d033e-340">public str name()</span><span class="sxs-lookup"><span data-stu-id="d033e-340">public str name()</span></span>      |                                                                                                |
| <span data-ttu-id="d033e-341">public Time timeData()</span><span class="sxs-lookup"><span data-stu-id="d033e-341">public Time timeData()</span></span> |                                                                                                |
| <span data-ttu-id="d033e-342">public str toString()</span><span class="sxs-lookup"><span data-stu-id="d033e-342">public str toString()</span></span>  | <span data-ttu-id="d033e-343">クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-343">Returns a string that contains the class handle and name, and possibly additional information.</span></span> |

### <a name="method-intdata"></a><span data-ttu-id="d033e-344">メソッド intData</span><span class="sxs-lookup"><span data-stu-id="d033e-344">Method intData</span></span>

    public int intData()

#### <a name="return-value"></a><span data-ttu-id="d033e-345">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-345">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="d033e-346">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d033e-346">Method name</span></span>

    public str name()

#### <a name="return-value"></a><span data-ttu-id="d033e-347">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-347">Return Value</span></span>

### <a name="method-timedata"></a><span data-ttu-id="d033e-348">メソッド timeData</span><span class="sxs-lookup"><span data-stu-id="d033e-348">Method timeData</span></span>

    public Time timeData()

#### <a name="return-value"></a><span data-ttu-id="d033e-349">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-349">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="d033e-350">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="d033e-350">Method toString</span></span>

<span data-ttu-id="d033e-351">クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-351">Returns a string that contains the class handle and name, and possibly additional information.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="d033e-352">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-352">Return Value</span></span>

<span data-ttu-id="d033e-353">クラスのテキストの説明。</span><span class="sxs-lookup"><span data-stu-id="d033e-353">A textual description of the class.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-354">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-354">Remarks</span></span>

<span data-ttu-id="d033e-355">既定では、ほとんどのクラスは、toString メソッドがクラス ハンドルおよび名前を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-355">By default, for most classes, the toString method returns a string that contains the class handle and name.</span></span> <span data-ttu-id="d033e-356">ただし、一部のクラスでは、追加情報が文字列で返されます。</span><span class="sxs-lookup"><span data-stu-id="d033e-356">However, in some classes additional information is returned in the string.</span></span>

## <a name="class-performancemonitorinstance"></a><span data-ttu-id="d033e-357">クラス PerformanceMonitorInstance</span><span class="sxs-lookup"><span data-stu-id="d033e-357">Class PerformanceMonitorInstance</span></span>
    class PerformanceMonitorInstance extends Object

<span data-ttu-id="d033e-358">PerformanceMonitorInstance クラスは、プロセス モニターが実行されるコンピューターで実行されているプロセスを表します。</span><span class="sxs-lookup"><span data-stu-id="d033e-358">The PerformanceMonitorInstance class represents a process that is running on the machine on which the Process Monitor runs.</span></span>

### <a name="remarks"></a><span data-ttu-id="d033e-359">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-359">Remarks</span></span>

<span data-ttu-id="d033e-360">このクラスは、プロセス カウンターのクエリを可能にします。</span><span class="sxs-lookup"><span data-stu-id="d033e-360">This class allows for queries of the process counters.</span></span> <span data-ttu-id="d033e-361">このクラスのオブジェクトを使用してプロセス カウンターをクエリすることができます。</span><span class="sxs-lookup"><span data-stu-id="d033e-361">You can use objects of this class to query the processes counters.</span></span> <span data-ttu-id="d033e-362">各カウンターは、プロセス パラメーターを表します。</span><span class="sxs-lookup"><span data-stu-id="d033e-362">Each counter represents a process parameter.</span></span>

### <a name="examples"></a><span data-ttu-id="d033e-363">例</span><span class="sxs-lookup"><span data-stu-id="d033e-363">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d033e-364">メソッド</span><span class="sxs-lookup"><span data-stu-id="d033e-364">Methods</span></span>

| <span data-ttu-id="d033e-365">方法</span><span class="sxs-lookup"><span data-stu-id="d033e-365">Method</span></span>                                                       | <span data-ttu-id="d033e-366">説明</span><span class="sxs-lookup"><span data-stu-id="d033e-366">Description</span></span>                                                                                    |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d033e-367">public PerformanceMonitorCounter getCounter(str counterName)</span><span class="sxs-lookup"><span data-stu-id="d033e-367">public PerformanceMonitorCounter getCounter(str counterName)</span></span> |                                                                                                |
| <span data-ttu-id="d033e-368">public str name()</span><span class="sxs-lookup"><span data-stu-id="d033e-368">public str name()</span></span>                                            |                                                                                                |
| <span data-ttu-id="d033e-369">public str toString()</span><span class="sxs-lookup"><span data-stu-id="d033e-369">public str toString()</span></span>                                        | <span data-ttu-id="d033e-370">クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-370">Returns a string that contains the class handle and name, and possibly additional information.</span></span> |

### <a name="method-getcounter"></a><span data-ttu-id="d033e-371">メソッド getCounter</span><span class="sxs-lookup"><span data-stu-id="d033e-371">Method getCounter</span></span>

    public PerformanceMonitorCounter getCounter(str counterName)

#### <a name="parameters"></a><span data-ttu-id="d033e-372">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-372">Parameters</span></span>

<span data-ttu-id="d033e-373">counterName</span><span class="sxs-lookup"><span data-stu-id="d033e-373">counterName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-374">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-374">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="d033e-375">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d033e-375">Method name</span></span>

    public str name()

#### <a name="return-value"></a><span data-ttu-id="d033e-376">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-376">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="d033e-377">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="d033e-377">Method toString</span></span>

<span data-ttu-id="d033e-378">クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-378">Returns a string that contains the class handle and name, and possibly additional information.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="d033e-379">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-379">Return Value</span></span>

<span data-ttu-id="d033e-380">クラスのテキストの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-380">Returns a textual description of the class.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-381">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-381">Remarks</span></span>

<span data-ttu-id="d033e-382">既定では、ほとんどのクラスは、toString メソッドがクラス ハンドルおよび名前を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-382">By default, for most classes, the toString method returns a string that contains the class handle and name.</span></span> <span data-ttu-id="d033e-383">ただし、一部のクラスでは、追加情報が文字列で返されます。</span><span class="sxs-lookup"><span data-stu-id="d033e-383">However, in some classes additional information is returned in the string.</span></span>

## <a name="class-pipeclient"></a><span data-ttu-id="d033e-384">クラス PipeClient</span><span class="sxs-lookup"><span data-stu-id="d033e-384">Class PipeClient</span></span>
    class PipeClient extends Object

### <a name="remarks"></a><span data-ttu-id="d033e-385">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-385">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d033e-386">例</span><span class="sxs-lookup"><span data-stu-id="d033e-386">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d033e-387">メソッド</span><span class="sxs-lookup"><span data-stu-id="d033e-387">Methods</span></span>

| <span data-ttu-id="d033e-388">方法</span><span class="sxs-lookup"><span data-stu-id="d033e-388">Method</span></span>                                                              | <span data-ttu-id="d033e-389">説明</span><span class="sxs-lookup"><span data-stu-id="d033e-389">Description</span></span>                                         |
|---------------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="d033e-390">public boolean blockingMode(\[boolean block\])</span><span class="sxs-lookup"><span data-stu-id="d033e-390">public boolean blockingMode(\[boolean block\])</span></span>                      |                                                     |
| <span data-ttu-id="d033e-391">public int errorCode()</span><span class="sxs-lookup"><span data-stu-id="d033e-391">public int errorCode()</span></span>                                              |                                                     |
| <span data-ttu-id="d033e-392">public str read()</span><span class="sxs-lookup"><span data-stu-id="d033e-392">public str read()</span></span>                                                   |                                                     |
| <span data-ttu-id="d033e-393">public boolean write(str buffer)</span><span class="sxs-lookup"><span data-stu-id="d033e-393">public boolean write(str buffer)</span></span>                                    |                                                     |
| <span data-ttu-id="d033e-394">public void new(str servername, str pipename, \[boolean blocking\])</span><span class="sxs-lookup"><span data-stu-id="d033e-394">public void new(str servername, str pipename, \[boolean blocking\])</span></span> | <span data-ttu-id="d033e-395">PipeClient クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-395">Initializes a new instance of the PipeClient class.</span></span> |

### <a name="method-blockingmode"></a><span data-ttu-id="d033e-396">メソッド blockingMode</span><span class="sxs-lookup"><span data-stu-id="d033e-396">Method blockingMode</span></span>

    public boolean blockingMode([boolean block])

#### <a name="parameters"></a><span data-ttu-id="d033e-397">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-397">Parameters</span></span>

<span data-ttu-id="d033e-398">block</span><span class="sxs-lookup"><span data-stu-id="d033e-398">block</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-399">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-399">Return Value</span></span>

### <a name="method-errorcode"></a><span data-ttu-id="d033e-400">メソッド errorCode</span><span class="sxs-lookup"><span data-stu-id="d033e-400">Method errorCode</span></span>

    public int errorCode()

#### <a name="return-value"></a><span data-ttu-id="d033e-401">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-401">Return Value</span></span>

### <a name="method-read"></a><span data-ttu-id="d033e-402">メソッド read</span><span class="sxs-lookup"><span data-stu-id="d033e-402">Method read</span></span>

    public str read()

#### <a name="return-value"></a><span data-ttu-id="d033e-403">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-403">Return Value</span></span>

### <a name="method-write"></a><span data-ttu-id="d033e-404">メソッド write</span><span class="sxs-lookup"><span data-stu-id="d033e-404">Method write</span></span>

    public boolean write(str buffer)

#### <a name="parameters"></a><span data-ttu-id="d033e-405">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-405">Parameters</span></span>

<span data-ttu-id="d033e-406">バッファ</span><span class="sxs-lookup"><span data-stu-id="d033e-406">buffer</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-407">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-407">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d033e-408">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d033e-408">Method new</span></span>

<span data-ttu-id="d033e-409">PipeClient クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-409">Initializes a new instance of the PipeClient class.</span></span>

    public void new(str servername, str pipename, [boolean blocking])

#### <a name="parameters"></a><span data-ttu-id="d033e-410">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-410">Parameters</span></span>

<span data-ttu-id="d033e-411">servername</span><span class="sxs-lookup"><span data-stu-id="d033e-411">servername</span></span>  

<!-- -->

<span data-ttu-id="d033e-412">pipename</span><span class="sxs-lookup"><span data-stu-id="d033e-412">pipename</span></span>  

<!-- -->

<span data-ttu-id="d033e-413">ブロック</span><span class="sxs-lookup"><span data-stu-id="d033e-413">blocking</span></span>  

## <a name="class-pipeserver"></a><span data-ttu-id="d033e-414">クラス PipeServer</span><span class="sxs-lookup"><span data-stu-id="d033e-414">Class PipeServer</span></span>
    class PipeServer extends Object

<span data-ttu-id="d033e-415">PipeServer クラスでは、名前付きパイプのサーバー側がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d033e-415">The PipeServer class supports the server side of a named pipe connection.</span></span>

### <a name="remarks"></a><span data-ttu-id="d033e-416">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-416">Remarks</span></span>

<span data-ttu-id="d033e-417">PipeServer オブジェクトが PipeServer.new メソッドを使用して作成されたときに、名前付きパイプが作成されます。</span><span class="sxs-lookup"><span data-stu-id="d033e-417">A named pipe is created when a PipeServer object is created by using the PipeServer.new method.</span></span> <span data-ttu-id="d033e-418">作成されるパイプは、読み取りアクセス権を保有し、メッセージ モードの状態にあります。</span><span class="sxs-lookup"><span data-stu-id="d033e-418">The pipe that is created has read access and is in message mode.</span></span> <span data-ttu-id="d033e-419">パイプの名前には自動的に接頭語 \\\\.\\pipe\\Dynamics が付けられます。</span><span class="sxs-lookup"><span data-stu-id="d033e-419">The name of the pipe is automatically prefixed with \\\\.\\pipe\\Dynamics.</span></span> <span data-ttu-id="d033e-420">現在のセッション SID は名前の接尾辞になります。</span><span class="sxs-lookup"><span data-stu-id="d033e-420">The current session SID is postfixed to the name.</span></span> <span data-ttu-id="d033e-421">サーバーのパイプ接続に提供されるサポートは、以下のセキュリティ上の理由により制限されています。</span><span class="sxs-lookup"><span data-stu-id="d033e-421">The support that is provided for pipe connections on the server is restricted for the following security reasons:</span></span>

-   <span data-ttu-id="d033e-422">パイプは、セッションが作成されたコンピュータ上の現在のログオン セッションのみに対してサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d033e-422">The pipe is supported only for the current logon session on the computer that the session was created on.</span></span>
-   <span data-ttu-id="d033e-423">パイプを作成するユーザーは、そのパイプと通信できる唯一のユーザーです。</span><span class="sxs-lookup"><span data-stu-id="d033e-423">The user who creates the pipe is the only person who can communicate with that pipe.</span></span>

### <a name="examples"></a><span data-ttu-id="d033e-424">例</span><span class="sxs-lookup"><span data-stu-id="d033e-424">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d033e-425">メソッド</span><span class="sxs-lookup"><span data-stu-id="d033e-425">Methods</span></span>

| <span data-ttu-id="d033e-426">方法</span><span class="sxs-lookup"><span data-stu-id="d033e-426">Method</span></span>                                              | <span data-ttu-id="d033e-427">説明</span><span class="sxs-lookup"><span data-stu-id="d033e-427">Description</span></span>                                                                  |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d033e-428">public boolean blockingMode(\[boolean block\])</span><span class="sxs-lookup"><span data-stu-id="d033e-428">public boolean blockingMode(\[boolean block\])</span></span>      |                                                                              |
| <span data-ttu-id="d033e-429">public boolean connect()</span><span class="sxs-lookup"><span data-stu-id="d033e-429">public boolean connect()</span></span>                            | <span data-ttu-id="d033e-430">クライアントが名前付きパイプに接続するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="d033e-430">Waits for a client to connect to the named pipe.</span></span>                             |
| <span data-ttu-id="d033e-431">public boolean disconnect()</span><span class="sxs-lookup"><span data-stu-id="d033e-431">public boolean disconnect()</span></span>                         | <span data-ttu-id="d033e-432">名前付きパイプ インスタンスのサーバー側をクライアント プロセスから切断します。</span><span class="sxs-lookup"><span data-stu-id="d033e-432">Disconnects the server end of the named pipe instance from a client process.</span></span> |
| <span data-ttu-id="d033e-433">public int errorCode()</span><span class="sxs-lookup"><span data-stu-id="d033e-433">public int errorCode()</span></span>                              |                                                                              |
| <span data-ttu-id="d033e-434">public str read()</span><span class="sxs-lookup"><span data-stu-id="d033e-434">public str read()</span></span>                                   | <span data-ttu-id="d033e-435">パイプ クライアントによって書き込まれたとおりに、名前付きパイプからデータを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="d033e-435">Reads data from the named pipe, as written by a pipe client.</span></span>                 |
| <span data-ttu-id="d033e-436">public void new(str pipename, \[boolean blocking\])</span><span class="sxs-lookup"><span data-stu-id="d033e-436">public void new(str pipename, \[boolean blocking\])</span></span> | <span data-ttu-id="d033e-437">PipeServer クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="d033e-437">Creates a new instance of the PipeServer class.</span></span>                              |

### <a name="method-blockingmode"></a><span data-ttu-id="d033e-438">メソッド blockingMode</span><span class="sxs-lookup"><span data-stu-id="d033e-438">Method blockingMode</span></span>

    public boolean blockingMode([boolean block])

#### <a name="parameters"></a><span data-ttu-id="d033e-439">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-439">Parameters</span></span>

<span data-ttu-id="d033e-440">block</span><span class="sxs-lookup"><span data-stu-id="d033e-440">block</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-441">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-441">Return Value</span></span>

### <a name="method-connect"></a><span data-ttu-id="d033e-442">メソッド connect</span><span class="sxs-lookup"><span data-stu-id="d033e-442">Method connect</span></span>

<span data-ttu-id="d033e-443">クライアントが名前付きパイプに接続するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="d033e-443">Waits for a client to connect to the named pipe.</span></span>

    public boolean connect()

#### <a name="return-value"></a><span data-ttu-id="d033e-444">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-444">Return Value</span></span>

<span data-ttu-id="d033e-445">メソッドが成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d033e-445">true if the method succeeds; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-446">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-446">Remarks</span></span>

<span data-ttu-id="d033e-447">クライアントが接続するのを待機している場合は、現在のスレッドをブロックしない場合、PipeServer.connect メソッドを使用しないようにし、代わりに PipeServer.read メソッドを使用してポーリングします。</span><span class="sxs-lookup"><span data-stu-id="d033e-447">If you do not want to block the current thread if it is waiting for a client to connect, avoid using the PipeServer.connect method, and poll by using the PipeServer.read method instead.</span></span>

### <a name="method-disconnect"></a><span data-ttu-id="d033e-448">メソッド disconnect</span><span class="sxs-lookup"><span data-stu-id="d033e-448">Method disconnect</span></span>

<span data-ttu-id="d033e-449">名前付きパイプ インスタンスのサーバー側をクライアント プロセスから切断します。</span><span class="sxs-lookup"><span data-stu-id="d033e-449">Disconnects the server end of the named pipe instance from a client process.</span></span>

    public boolean disconnect()

#### <a name="return-value"></a><span data-ttu-id="d033e-450">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-450">Return Value</span></span>

<span data-ttu-id="d033e-451">メソッドが成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d033e-451">true if the method succeeds; otherwise, false.</span></span>

### <a name="method-errorcode"></a><span data-ttu-id="d033e-452">メソッド errorCode</span><span class="sxs-lookup"><span data-stu-id="d033e-452">Method errorCode</span></span>

    public int errorCode()

#### <a name="return-value"></a><span data-ttu-id="d033e-453">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-453">Return Value</span></span>

### <a name="method-read"></a><span data-ttu-id="d033e-454">メソッド read</span><span class="sxs-lookup"><span data-stu-id="d033e-454">Method read</span></span>

<span data-ttu-id="d033e-455">パイプ クライアントによって書き込まれたとおりに、名前付きパイプからデータを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="d033e-455">Reads data from the named pipe, as written by a pipe client.</span></span>

    public str read()

#### <a name="return-value"></a><span data-ttu-id="d033e-456">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-456">Return Value</span></span>

<span data-ttu-id="d033e-457">データが読み取られた場合に、パイプから読み取られるデータ。</span><span class="sxs-lookup"><span data-stu-id="d033e-457">The data that is read from the pipe, if any data is read.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-458">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-458">Remarks</span></span>

<span data-ttu-id="d033e-459">クライアントが名前付きパイプに接続されていないために、このメソッドが呼び出されたときにデータを使用できないことがあります。</span><span class="sxs-lookup"><span data-stu-id="d033e-459">Data might not be available when this method is called, perhaps because no client has connected to the named pipe.</span></span> <span data-ttu-id="d033e-460">クライアントへの接続を待機する場合は、接続方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="d033e-460">If you want to wait for a client to connect, use the connect method.</span></span> <span data-ttu-id="d033e-461">ただし、クライアントの接続を待機している現在のスレッドをブロックしない場合、読み取りメソッドを使用してポーリングします。</span><span class="sxs-lookup"><span data-stu-id="d033e-461">However, if you do not want to block the current thread that is waiting for a client to connect, poll by using the read method.</span></span>

### <a name="method-new"></a><span data-ttu-id="d033e-462">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d033e-462">Method new</span></span>

<span data-ttu-id="d033e-463">PipeServer クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="d033e-463">Creates a new instance of the PipeServer class.</span></span>

    public void new(str pipename, [boolean blocking])

#### <a name="parameters"></a><span data-ttu-id="d033e-464">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-464">Parameters</span></span>

<span data-ttu-id="d033e-465">pipename</span><span class="sxs-lookup"><span data-stu-id="d033e-465">pipename</span></span>  
<span data-ttu-id="d033e-466">ブロック動作を使用するかどうかを示すブール値フラグ。</span><span class="sxs-lookup"><span data-stu-id="d033e-466">A Boolean flag that indicates whether blocking behavior should be used.</span></span> <span data-ttu-id="d033e-467">非ブロック モードは、Microsoft LAN Manager バージョン 2.0 との互換性をサポートしており、名前付きパイプで非同期入出力を達成するために使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="d033e-467">Non-blocking mode is supported for compatibility with Microsoft LAN Manager version 2.0 and should not be used to achieve asynchronous I/O with named pipes.</span></span> <span data-ttu-id="d033e-468">代わりに、ポーリング技術を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d033e-468">Instead, a polling technique should be used.</span></span> <span data-ttu-id="d033e-469">読み取りメソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d033e-469">See the read method.</span></span>

<!-- -->

<span data-ttu-id="d033e-470">ブロック</span><span class="sxs-lookup"><span data-stu-id="d033e-470">blocking</span></span>  
<span data-ttu-id="d033e-471">ブロック動作を使用するかどうかを示すブール値フラグ。</span><span class="sxs-lookup"><span data-stu-id="d033e-471">A Boolean flag that indicates whether blocking behavior should be used.</span></span> <span data-ttu-id="d033e-472">非ブロック モードは、Microsoft LAN Manager バージョン 2.0 との互換性をサポートしており、名前付きパイプで非同期入出力を達成するために使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="d033e-472">Non-blocking mode is supported for compatibility with Microsoft LAN Manager version 2.0 and should not be used to achieve asynchronous I/O with named pipes.</span></span> <span data-ttu-id="d033e-473">代わりに、ポーリング技術を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d033e-473">Instead, a polling technique should be used.</span></span> <span data-ttu-id="d033e-474">読み取りメソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d033e-474">See the read method.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-475">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-475">Remarks</span></span>

<span data-ttu-id="d033e-476">いくつかの制限が適用されます。</span><span class="sxs-lookup"><span data-stu-id="d033e-476">Some restrictions apply.</span></span> <span data-ttu-id="d033e-477">PipeServer クラスの一般的な説明の例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d033e-477">See the example in the general description of the PipeServer class.</span></span>

## <a name="class-presenceinfo"></a><span data-ttu-id="d033e-478">クラス PresenceInfo</span><span class="sxs-lookup"><span data-stu-id="d033e-478">Class PresenceInfo</span></span>
    class PresenceInfo extends Object

### <a name="remarks"></a><span data-ttu-id="d033e-479">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-479">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d033e-480">例</span><span class="sxs-lookup"><span data-stu-id="d033e-480">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d033e-481">メソッド</span><span class="sxs-lookup"><span data-stu-id="d033e-481">Methods</span></span>

| <span data-ttu-id="d033e-482">方法</span><span class="sxs-lookup"><span data-stu-id="d033e-482">Method</span></span>                                                                | <span data-ttu-id="d033e-483">説明</span><span class="sxs-lookup"><span data-stu-id="d033e-483">Description</span></span>                                           |
|-----------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="d033e-484">public str contactName(\[str contactName\])</span><span class="sxs-lookup"><span data-stu-id="d033e-484">public str contactName(\[str contactName\])</span></span>                           |                                                       |
| <span data-ttu-id="d033e-485">public str emailAddress(int index)</span><span class="sxs-lookup"><span data-stu-id="d033e-485">public str emailAddress(int index)</span></span>                                    |                                                       |
| <span data-ttu-id="d033e-486">public str emailAlias(int index)</span><span class="sxs-lookup"><span data-stu-id="d033e-486">public str emailAlias(int index)</span></span>                                      |                                                       |
| <span data-ttu-id="d033e-487">public int emailCount()</span><span class="sxs-lookup"><span data-stu-id="d033e-487">public int emailCount()</span></span>                                               |                                                       |
| <span data-ttu-id="d033e-488">public str phoneAlias(int index)</span><span class="sxs-lookup"><span data-stu-id="d033e-488">public str phoneAlias(int index)</span></span>                                      |                                                       |
| <span data-ttu-id="d033e-489">public int phoneCount()</span><span class="sxs-lookup"><span data-stu-id="d033e-489">public int phoneCount()</span></span>                                               |                                                       |
| <span data-ttu-id="d033e-490">public str phoneNumber(int index)</span><span class="sxs-lookup"><span data-stu-id="d033e-490">public str phoneNumber(int index)</span></span>                                     |                                                       |
| <span data-ttu-id="d033e-491">public str sipAddress(\[str sipAddress\])</span><span class="sxs-lookup"><span data-stu-id="d033e-491">public str sipAddress(\[str sipAddress\])</span></span>                             |                                                       |
| <span data-ttu-id="d033e-492">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="d033e-492">public void finalize()</span></span>                                                |                                                       |
| <span data-ttu-id="d033e-493">public void new()</span><span class="sxs-lookup"><span data-stu-id="d033e-493">public void new()</span></span>                                                     | <span data-ttu-id="d033e-494">PresenceInfo クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-494">Initializes a new instance of the PresenceInfo class.</span></span> |
| <span data-ttu-id="d033e-495">public void addEmailAddress(\[str emailAlias\], \[str emailAddress\])</span><span class="sxs-lookup"><span data-stu-id="d033e-495">public void addEmailAddress(\[str emailAlias\], \[str emailAddress\])</span></span> |                                                       |
| <span data-ttu-id="d033e-496">public void addPhoneNumber(\[str phoneAlias\], \[str phoneNumber\])</span><span class="sxs-lookup"><span data-stu-id="d033e-496">public void addPhoneNumber(\[str phoneAlias\], \[str phoneNumber\])</span></span>   |                                                       |

### <a name="method-contactname"></a><span data-ttu-id="d033e-497">メソッド contactName</span><span class="sxs-lookup"><span data-stu-id="d033e-497">Method contactName</span></span>

    public str contactName([str contactName])

#### <a name="parameters"></a><span data-ttu-id="d033e-498">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-498">Parameters</span></span>

<span data-ttu-id="d033e-499">contactName</span><span class="sxs-lookup"><span data-stu-id="d033e-499">contactName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-500">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-500">Return Value</span></span>

### <a name="method-emailaddress"></a><span data-ttu-id="d033e-501">メソッド emailAddress</span><span class="sxs-lookup"><span data-stu-id="d033e-501">Method emailAddress</span></span>

    public str emailAddress(int index)

#### <a name="parameters"></a><span data-ttu-id="d033e-502">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-502">Parameters</span></span>

<span data-ttu-id="d033e-503">指数</span><span class="sxs-lookup"><span data-stu-id="d033e-503">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-504">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-504">Return Value</span></span>

### <a name="method-emailalias"></a><span data-ttu-id="d033e-505">メソッド emailAlias</span><span class="sxs-lookup"><span data-stu-id="d033e-505">Method emailAlias</span></span>

    public str emailAlias(int index)

#### <a name="parameters"></a><span data-ttu-id="d033e-506">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-506">Parameters</span></span>

<span data-ttu-id="d033e-507">指数</span><span class="sxs-lookup"><span data-stu-id="d033e-507">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-508">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-508">Return Value</span></span>

### <a name="method-emailcount"></a><span data-ttu-id="d033e-509">メソッド emailCount</span><span class="sxs-lookup"><span data-stu-id="d033e-509">Method emailCount</span></span>

    public int emailCount()

#### <a name="return-value"></a><span data-ttu-id="d033e-510">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-510">Return Value</span></span>

### <a name="method-phonealias"></a><span data-ttu-id="d033e-511">メソッド phoneAlias</span><span class="sxs-lookup"><span data-stu-id="d033e-511">Method phoneAlias</span></span>

    public str phoneAlias(int index)

#### <a name="parameters"></a><span data-ttu-id="d033e-512">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-512">Parameters</span></span>

<span data-ttu-id="d033e-513">指数</span><span class="sxs-lookup"><span data-stu-id="d033e-513">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-514">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-514">Return Value</span></span>

### <a name="method-phonecount"></a><span data-ttu-id="d033e-515">メソッド phoneCount</span><span class="sxs-lookup"><span data-stu-id="d033e-515">Method phoneCount</span></span>

    public int phoneCount()

#### <a name="return-value"></a><span data-ttu-id="d033e-516">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-516">Return Value</span></span>

### <a name="method-phonenumber"></a><span data-ttu-id="d033e-517">メソッド phoneNumber</span><span class="sxs-lookup"><span data-stu-id="d033e-517">Method phoneNumber</span></span>

    public str phoneNumber(int index)

#### <a name="parameters"></a><span data-ttu-id="d033e-518">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-518">Parameters</span></span>

<span data-ttu-id="d033e-519">指数</span><span class="sxs-lookup"><span data-stu-id="d033e-519">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-520">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-520">Return Value</span></span>

### <a name="method-sipaddress"></a><span data-ttu-id="d033e-521">メソッド sipAddress</span><span class="sxs-lookup"><span data-stu-id="d033e-521">Method sipAddress</span></span>

    public str sipAddress([str sipAddress])

#### <a name="parameters"></a><span data-ttu-id="d033e-522">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-522">Parameters</span></span>

<span data-ttu-id="d033e-523">sipAddress</span><span class="sxs-lookup"><span data-stu-id="d033e-523">sipAddress</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-524">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-524">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="d033e-525">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="d033e-525">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="d033e-526">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d033e-526">Method new</span></span>

<span data-ttu-id="d033e-527">PresenceInfo クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-527">Initializes a new instance of the PresenceInfo class.</span></span>

    public void new()

### <a name="method-addemailaddress"></a><span data-ttu-id="d033e-528">メソッド addEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d033e-528">Method addEmailAddress</span></span>

    public void addEmailAddress([str emailAlias], [str emailAddress])

#### <a name="parameters"></a><span data-ttu-id="d033e-529">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-529">Parameters</span></span>

<span data-ttu-id="d033e-530">emailAlias</span><span class="sxs-lookup"><span data-stu-id="d033e-530">emailAlias</span></span>  

<!-- -->

<span data-ttu-id="d033e-531">emailAddress</span><span class="sxs-lookup"><span data-stu-id="d033e-531">emailAddress</span></span>  

### <a name="method-addphonenumber"></a><span data-ttu-id="d033e-532">メソッド addPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="d033e-532">Method addPhoneNumber</span></span>

    public void addPhoneNumber([str phoneAlias], [str phoneNumber])

#### <a name="parameters"></a><span data-ttu-id="d033e-533">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-533">Parameters</span></span>

<span data-ttu-id="d033e-534">phoneAlias</span><span class="sxs-lookup"><span data-stu-id="d033e-534">phoneAlias</span></span>  

<!-- -->

<span data-ttu-id="d033e-535">phoneNumber</span><span class="sxs-lookup"><span data-stu-id="d033e-535">phoneNumber</span></span>  

## <a name="class-printjobsettings"></a><span data-ttu-id="d033e-536">クラス PrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="d033e-536">Class PrintJobSettings</span></span>
    class PrintJobSettings extends Object

<span data-ttu-id="d033e-537">PrintJobSettings クラスを使用すると、ユーザーがプリンターおよびそのデバイス設定にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d033e-537">The PrintJobSettings class lets users access printers and their device settings.</span></span>

### <a name="remarks"></a><span data-ttu-id="d033e-538">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-538">Remarks</span></span>

<span data-ttu-id="d033e-539">PrintJobSettings は、SysPrintForm フォームにより使用されます。</span><span class="sxs-lookup"><span data-stu-id="d033e-539">PrintJobSettings is used by the SysPrintForm form.</span></span>

### <a name="examples"></a><span data-ttu-id="d033e-540">例</span><span class="sxs-lookup"><span data-stu-id="d033e-540">Examples</span></span>

<span data-ttu-id="d033e-541">次の例では、既定のプリンターの名前を書き込み、使用可能なプリンターを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="d033e-541">The following example writes the name of the default printer and lists the available printers.</span></span>

    void printerInfo() 
    {    
        printJobSettings pjs; 
        int i; 
        pjs = new PrintJobSettings(); 
        print "The default printer is ", pjs.DeviceName(); 
        print "There are ", pjs.GetNumberOfPrinters(), " printers"; 
        i = 1; 
        while (i<=pjs.GetNumberOfPrinters())  
        { 
            print "Printer No. ", i, " is ", pjs.GetPrinter(i);  
            i++; 
        } 
        pause; 
    }

### <a name="methods"></a><span data-ttu-id="d033e-542">メソッド</span><span class="sxs-lookup"><span data-stu-id="d033e-542">Methods</span></span>

| <span data-ttu-id="d033e-543">方法</span><span class="sxs-lookup"><span data-stu-id="d033e-543">Method</span></span>                                                                                                  | <span data-ttu-id="d033e-544">説明</span><span class="sxs-lookup"><span data-stu-id="d033e-544">Description</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d033e-545">public boolean allPages(\[boolean all\])</span><span class="sxs-lookup"><span data-stu-id="d033e-545">public boolean allPages(\[boolean all\])</span></span>                                                                | <span data-ttu-id="d033e-546">sysPrintForm を実行するときに、すべてまたはページのオプション ボタンを選択するかどうかをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="d033e-546">Controls whether the All or Pages option button should be selected when you run the sysPrintForm.</span></span> |
| <span data-ttu-id="d033e-547">public boolean appendToTextFile(\[boolean append\])</span><span class="sxs-lookup"><span data-stu-id="d033e-547">public boolean appendToTextFile(\[boolean append\])</span></span>                                                     |                                                                                                   |
| <span data-ttu-id="d033e-548">public boolean banding()</span><span class="sxs-lookup"><span data-stu-id="d033e-548">public boolean banding()</span></span>                                                                                |                                                                                                   |
| <span data-ttu-id="d033e-549">public PrintJobSettings clientPrintJobSettings()</span><span class="sxs-lookup"><span data-stu-id="d033e-549">public PrintJobSettings clientPrintJobSettings()</span></span>                                                        |                                                                                                   |
| <span data-ttu-id="d033e-550">public boolean collate(\[boolean collate\])</span><span class="sxs-lookup"><span data-stu-id="d033e-550">public boolean collate(\[boolean collate\])</span></span>                                                             |                                                                                                   |
| <span data-ttu-id="d033e-551">public int copies(\[int numberOfCopies\])</span><span class="sxs-lookup"><span data-stu-id="d033e-551">public int copies(\[int numberOfCopies\])</span></span>                                                               |                                                                                                   |
| <span data-ttu-id="d033e-552">public str copyDescription(int number, \[str description\])</span><span class="sxs-lookup"><span data-stu-id="d033e-552">public str copyDescription(int number, \[str description\])</span></span>                                             |                                                                                                   |
| <span data-ttu-id="d033e-553">public str deviceName(\[str device\], \[ClassRunMode runOn\])</span><span class="sxs-lookup"><span data-stu-id="d033e-553">public str deviceName(\[str device\], \[ClassRunMode runOn\])</span></span>                                           | <span data-ttu-id="d033e-554">プリンターを選択するか、選択されているプリンター デバイス名を取得します。</span><span class="sxs-lookup"><span data-stu-id="d033e-554">Selects a printer or retrieves the deviceName of the selected printer.</span></span>                            |
| <span data-ttu-id="d033e-555">public boolean doNotOverwrite(\[boolean warn\])</span><span class="sxs-lookup"><span data-stu-id="d033e-555">public boolean doNotOverwrite(\[boolean warn\])</span></span>                                                         |                                                                                                   |
| <span data-ttu-id="d033e-556">public boolean enableCopies(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="d033e-556">public boolean enableCopies(\[boolean enable\])</span></span>                                                         |                                                                                                   |
| <span data-ttu-id="d033e-557">public boolean enableDevice(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="d033e-557">public boolean enableDevice(\[boolean enable\])</span></span>                                                         |                                                                                                   |
| <span data-ttu-id="d033e-558">public boolean enablePages(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="d033e-558">public boolean enablePages(\[boolean enable\])</span></span>                                                          |                                                                                                   |
| <span data-ttu-id="d033e-559">public boolean enableProperties(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="d033e-559">public boolean enableProperties(\[boolean enable\])</span></span>                                                     |                                                                                                   |
| <span data-ttu-id="d033e-560">public boolean enableStoreInPrintArchive(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="d033e-560">public boolean enableStoreInPrintArchive(\[boolean enable\])</span></span>                                            |                                                                                                   |
| <span data-ttu-id="d033e-561">public boolean enableTarget(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="d033e-561">public boolean enableTarget(\[boolean enable\])</span></span>                                                         |                                                                                                   |
| <span data-ttu-id="d033e-562">public int facename2number(\[str facename\])</span><span class="sxs-lookup"><span data-stu-id="d033e-562">public int facename2number(\[str facename\])</span></span>                                                            |                                                                                                   |
| <span data-ttu-id="d033e-563">public str fileName(\[str FileName\])</span><span class="sxs-lookup"><span data-stu-id="d033e-563">public str fileName(\[str FileName\])</span></span>                                                                   |                                                                                                   |
| <span data-ttu-id="d033e-564">public boolean fitToPage(\[boolean fit\])</span><span class="sxs-lookup"><span data-stu-id="d033e-564">public boolean fitToPage(\[boolean fit\])</span></span>                                                               |                                                                                                   |
| <span data-ttu-id="d033e-565">public PrintFormat format(\[PrintFormat format\])</span><span class="sxs-lookup"><span data-stu-id="d033e-565">public PrintFormat format(\[PrintFormat format\])</span></span>                                                       |                                                                                                   |
| <span data-ttu-id="d033e-566">public int from(\[int fromPage\])</span><span class="sxs-lookup"><span data-stu-id="d033e-566">public int from(\[int fromPage\])</span></span>                                                                       |                                                                                                   |
| <span data-ttu-id="d033e-567">public str getFacename(int number)</span><span class="sxs-lookup"><span data-stu-id="d033e-567">public str getFacename(int number)</span></span>                                                                      |                                                                                                   |
| <span data-ttu-id="d033e-568">public str getFacenameInfo(int number)</span><span class="sxs-lookup"><span data-stu-id="d033e-568">public str getFacenameInfo(int number)</span></span>                                                                  |                                                                                                   |
| <span data-ttu-id="d033e-569">public Struct getFontInfo(str fontName)</span><span class="sxs-lookup"><span data-stu-id="d033e-569">public Struct getFontInfo(str fontName)</span></span>                                                                 |                                                                                                   |
| <span data-ttu-id="d033e-570">public Array getGlyphWidthsArray(str fontName, int firstChar, int lastChar)</span><span class="sxs-lookup"><span data-stu-id="d033e-570">public Array getGlyphWidthsArray(str fontName, int firstChar, int lastChar)</span></span>                             |                                                                                                   |
| <span data-ttu-id="d033e-571">public int getNumberOfClientPrinters()</span><span class="sxs-lookup"><span data-stu-id="d033e-571">public int getNumberOfClientPrinters()</span></span>                                                                  |                                                                                                   |
| <span data-ttu-id="d033e-572">public int getNumberOfFacenames()</span><span class="sxs-lookup"><span data-stu-id="d033e-572">public int getNumberOfFacenames()</span></span>                                                                       |                                                                                                   |
| <span data-ttu-id="d033e-573">public int getNumberOfPrinters()</span><span class="sxs-lookup"><span data-stu-id="d033e-573">public int getNumberOfPrinters()</span></span>                                                                        | <span data-ttu-id="d033e-574">コンピューターに設定されているプリンターの数を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-574">Returns the number of printers that are set up on the computer.</span></span>                                   |
| <span data-ttu-id="d033e-575">public int getNumberOfServerPrinters()</span><span class="sxs-lookup"><span data-stu-id="d033e-575">public int getNumberOfServerPrinters()</span></span>                                                                  |                                                                                                   |
| <span data-ttu-id="d033e-576">public int getNumberOfTrays()</span><span class="sxs-lookup"><span data-stu-id="d033e-576">public int getNumberOfTrays()</span></span>                                                                           |                                                                                                   |
| <span data-ttu-id="d033e-577">public str getPrinter(int number)</span><span class="sxs-lookup"><span data-stu-id="d033e-577">public str getPrinter(int number)</span></span>                                                                       | <span data-ttu-id="d033e-578">プリンターの deviceName を取得します。</span><span class="sxs-lookup"><span data-stu-id="d033e-578">Gets the deviceName of a printer.</span></span>                                                                 |
| <span data-ttu-id="d033e-579">public ClassRunMode getRunOn(int number)</span><span class="sxs-lookup"><span data-stu-id="d033e-579">public ClassRunMode getRunOn(int number)</span></span>                                                                |                                                                                                   |
| <span data-ttu-id="d033e-580">public PrintMedium getTarget()</span><span class="sxs-lookup"><span data-stu-id="d033e-580">public PrintMedium getTarget()</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="d033e-581">public int getTray(int number)</span><span class="sxs-lookup"><span data-stu-id="d033e-581">public int getTray(int number)</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="d033e-582">public str getTrayName(int number)</span><span class="sxs-lookup"><span data-stu-id="d033e-582">public str getTrayName(int number)</span></span>                                                                      |                                                                                                   |
| <span data-ttu-id="d033e-583">public Int64 hDC()</span><span class="sxs-lookup"><span data-stu-id="d033e-583">public Int64 hDC()</span></span>                                                                                      |                                                                                                   |
| <span data-ttu-id="d033e-584">public boolean lockDestinationProperties(\[boolean warn\])</span><span class="sxs-lookup"><span data-stu-id="d033e-584">public boolean lockDestinationProperties(\[boolean warn\])</span></span>                                              |                                                                                                   |
| <span data-ttu-id="d033e-585">public str mailCc(\[str MailCc\])</span><span class="sxs-lookup"><span data-stu-id="d033e-585">public str mailCc(\[str MailCc\])</span></span>                                                                       |                                                                                                   |
| <span data-ttu-id="d033e-586">public str mailSubject(\[str MailSubject\])</span><span class="sxs-lookup"><span data-stu-id="d033e-586">public str mailSubject(\[str MailSubject\])</span></span>                                                             |                                                                                                   |
| <span data-ttu-id="d033e-587">public str mailTo(\[str MailTo\])</span><span class="sxs-lookup"><span data-stu-id="d033e-587">public str mailTo(\[str MailTo\])</span></span>                                                                       |                                                                                                   |
| <span data-ttu-id="d033e-588">public int numberOfCopyDescriptions(int number)</span><span class="sxs-lookup"><span data-stu-id="d033e-588">public int numberOfCopyDescriptions(int number)</span></span>                                                         |                                                                                                   |
| <span data-ttu-id="d033e-589">public boolean outputToClient(\[boolean toClient\])</span><span class="sxs-lookup"><span data-stu-id="d033e-589">public boolean outputToClient(\[boolean toClient\])</span></span>                                                     |                                                                                                   |
| <span data-ttu-id="d033e-590">public boolean outputToPrnFile(\[boolean writePrnFile\])</span><span class="sxs-lookup"><span data-stu-id="d033e-590">public boolean outputToPrnFile(\[boolean writePrnFile\])</span></span>                                                |                                                                                                   |
| <span data-ttu-id="d033e-591">public container packNamesAndPrinterData()</span><span class="sxs-lookup"><span data-stu-id="d033e-591">public container packNamesAndPrinterData()</span></span>                                                              |                                                                                                   |
| <span data-ttu-id="d033e-592">public container packPageSettings()</span><span class="sxs-lookup"><span data-stu-id="d033e-592">public container packPageSettings()</span></span>                                                                     | <span data-ttu-id="d033e-593">ページの書式設定時に選択されているデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="d033e-593">Stores the data that is selected during page formatting in a container.</span></span>                           |
| <span data-ttu-id="d033e-594">public container packPrinterSettings()</span><span class="sxs-lookup"><span data-stu-id="d033e-594">public container packPrinterSettings()</span></span>                                                                  |                                                                                                   |
| <span data-ttu-id="d033e-595">public container packPrintJobSettings()</span><span class="sxs-lookup"><span data-stu-id="d033e-595">public container packPrintJobSettings()</span></span>                                                                 |                                                                                                   |
| <span data-ttu-id="d033e-596">public container packSubtotalSettings()</span><span class="sxs-lookup"><span data-stu-id="d033e-596">public container packSubtotalSettings()</span></span>                                                                 |                                                                                                   |
| <span data-ttu-id="d033e-597">public int pageCopy2Tray(int pageNumber, \[int copyNumber\])</span><span class="sxs-lookup"><span data-stu-id="d033e-597">public int pageCopy2Tray(int pageNumber, \[int copyNumber\])</span></span>                                            |                                                                                                   |
| <span data-ttu-id="d033e-598">public boolean pageFormatting()</span><span class="sxs-lookup"><span data-stu-id="d033e-598">public boolean pageFormatting()</span></span>                                                                         |                                                                                                   |
| <span data-ttu-id="d033e-599">public PrinterOrientation paperOrientation(\[PrinterOrientation orientation\])</span><span class="sxs-lookup"><span data-stu-id="d033e-599">public PrinterOrientation paperOrientation(\[PrinterOrientation orientation\])</span></span>                          |                                                                                                   |
| <span data-ttu-id="d033e-600">public int paperTray(\[int tray\])</span><span class="sxs-lookup"><span data-stu-id="d033e-600">public int paperTray(\[int tray\])</span></span>                                                                      |                                                                                                   |
| <span data-ttu-id="d033e-601">public int paperTrayRaw(\[int tray\])</span><span class="sxs-lookup"><span data-stu-id="d033e-601">public int paperTrayRaw(\[int tray\])</span></span>                                                                   |                                                                                                   |
| <span data-ttu-id="d033e-602">public int performanceTest(\[int loops\])</span><span class="sxs-lookup"><span data-stu-id="d033e-602">public int performanceTest(\[int loops\])</span></span>                                                               |                                                                                                   |
| <span data-ttu-id="d033e-603">public PrintFormat preferredFileFormat(\[PrintFormat format\])</span><span class="sxs-lookup"><span data-stu-id="d033e-603">public PrintFormat preferredFileFormat(\[PrintFormat format\])</span></span>                                          |                                                                                                   |
| <span data-ttu-id="d033e-604">public PrintFormat preferredMailFormat(\[PrintFormat format\])</span><span class="sxs-lookup"><span data-stu-id="d033e-604">public PrintFormat preferredMailFormat(\[PrintFormat format\])</span></span>                                          |                                                                                                   |
| <span data-ttu-id="d033e-605">public PrinterOrientation preferredOrientation(\[PrinterOrientation orientation\])</span><span class="sxs-lookup"><span data-stu-id="d033e-605">public PrinterOrientation preferredOrientation(\[PrinterOrientation orientation\])</span></span>                      |                                                                                                   |
| <span data-ttu-id="d033e-606">public PrintMedium preferredTarget(\[PrintMedium target\])</span><span class="sxs-lookup"><span data-stu-id="d033e-606">public PrintMedium preferredTarget(\[PrintMedium target\])</span></span>                                              |                                                                                                   |
| <span data-ttu-id="d033e-607">public int printerAttributes()</span><span class="sxs-lookup"><span data-stu-id="d033e-607">public int printerAttributes()</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="d033e-608">public int printerAveragePPM()</span><span class="sxs-lookup"><span data-stu-id="d033e-608">public int printerAveragePPM()</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="d033e-609">public str printerComment()</span><span class="sxs-lookup"><span data-stu-id="d033e-609">public str printerComment()</span></span>                                                                             |                                                                                                   |
| <span data-ttu-id="d033e-610">public str printerDatatype()</span><span class="sxs-lookup"><span data-stu-id="d033e-610">public str printerDatatype()</span></span>                                                                            |                                                                                                   |
| <span data-ttu-id="d033e-611">public int printerDefaultPriority()</span><span class="sxs-lookup"><span data-stu-id="d033e-611">public int printerDefaultPriority()</span></span>                                                                     |                                                                                                   |
| <span data-ttu-id="d033e-612">public str printerDriverName()</span><span class="sxs-lookup"><span data-stu-id="d033e-612">public str printerDriverName()</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="d033e-613">public str printerLocation()</span><span class="sxs-lookup"><span data-stu-id="d033e-613">public str printerLocation()</span></span>                                                                            |                                                                                                   |
| <span data-ttu-id="d033e-614">public int printerPageHeight()</span><span class="sxs-lookup"><span data-stu-id="d033e-614">public int printerPageHeight()</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="d033e-615">public int printerPageWidth()</span><span class="sxs-lookup"><span data-stu-id="d033e-615">public int printerPageWidth()</span></span>                                                                           |                                                                                                   |
| <span data-ttu-id="d033e-616">public int printerPaper()</span><span class="sxs-lookup"><span data-stu-id="d033e-616">public int printerPaper()</span></span>                                                                               |                                                                                                   |
| <span data-ttu-id="d033e-617">public str printerParameters()</span><span class="sxs-lookup"><span data-stu-id="d033e-617">public str printerParameters()</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="d033e-618">public str printerPortName()</span><span class="sxs-lookup"><span data-stu-id="d033e-618">public str printerPortName()</span></span>                                                                            |                                                                                                   |
| <span data-ttu-id="d033e-619">public str printerPrinterName()</span><span class="sxs-lookup"><span data-stu-id="d033e-619">public str printerPrinterName()</span></span>                                                                         |                                                                                                   |
| <span data-ttu-id="d033e-620">public str printerPrintProcessor()</span><span class="sxs-lookup"><span data-stu-id="d033e-620">public str printerPrintProcessor()</span></span>                                                                      |                                                                                                   |
| <span data-ttu-id="d033e-621">public int printerPriority()</span><span class="sxs-lookup"><span data-stu-id="d033e-621">public int printerPriority()</span></span>                                                                            |                                                                                                   |
| <span data-ttu-id="d033e-622">public int printerQueuedJobs()</span><span class="sxs-lookup"><span data-stu-id="d033e-622">public int printerQueuedJobs()</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="d033e-623">public ClassRunMode printerRunOn()</span><span class="sxs-lookup"><span data-stu-id="d033e-623">public ClassRunMode printerRunOn()</span></span>                                                                      |                                                                                                   |
| <span data-ttu-id="d033e-624">public str printerSepFile()</span><span class="sxs-lookup"><span data-stu-id="d033e-624">public str printerSepFile()</span></span>                                                                             |                                                                                                   |
| <span data-ttu-id="d033e-625">public str printerServerName()</span><span class="sxs-lookup"><span data-stu-id="d033e-625">public str printerServerName()</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="d033e-626">public boolean printerSettings(str formName, \[xArgs args\], \[ReportRun reportRun\], \[int showWhat\])</span><span class="sxs-lookup"><span data-stu-id="d033e-626">public boolean printerSettings(str formName, \[xArgs args\], \[ReportRun reportRun\], \[int showWhat\])</span></span> |                                                                                                   |
| <span data-ttu-id="d033e-627">public str printerShareName()</span><span class="sxs-lookup"><span data-stu-id="d033e-627">public str printerShareName()</span></span>                                                                           |                                                                                                   |
| <span data-ttu-id="d033e-628">public TimeOfDay printerStartTime()</span><span class="sxs-lookup"><span data-stu-id="d033e-628">public TimeOfDay printerStartTime()</span></span>                                                                     |                                                                                                   |
| <span data-ttu-id="d033e-629">public int printerStatus()</span><span class="sxs-lookup"><span data-stu-id="d033e-629">public int printerStatus()</span></span>                                                                              |                                                                                                   |
| <span data-ttu-id="d033e-630">public TimeOfDay printerUntilTime()</span><span class="sxs-lookup"><span data-stu-id="d033e-630">public TimeOfDay printerUntilTime()</span></span>                                                                     |                                                                                                   |
| <span data-ttu-id="d033e-631">public ReportRun reportRun()</span><span class="sxs-lookup"><span data-stu-id="d033e-631">public ReportRun reportRun()</span></span>                                                                            |                                                                                                   |
| <span data-ttu-id="d033e-632">public str requestedDeviceName()</span><span class="sxs-lookup"><span data-stu-id="d033e-632">public str requestedDeviceName()</span></span>                                                                        |                                                                                                   |
| <span data-ttu-id="d033e-633">public ClassRunMode requestedRunOn()</span><span class="sxs-lookup"><span data-stu-id="d033e-633">public ClassRunMode requestedRunOn()</span></span>                                                                    |                                                                                                   |
| <span data-ttu-id="d033e-634">public boolean runClient()</span><span class="sxs-lookup"><span data-stu-id="d033e-634">public boolean runClient()</span></span>                                                                              |                                                                                                   |
| <span data-ttu-id="d033e-635">public boolean runServer()</span><span class="sxs-lookup"><span data-stu-id="d033e-635">public boolean runServer()</span></span>                                                                              |                                                                                                   |
| <span data-ttu-id="d033e-636">public int sectionsPerPage(\[int sectionsPerPage\])</span><span class="sxs-lookup"><span data-stu-id="d033e-636">public int sectionsPerPage(\[int sectionsPerPage\])</span></span>                                                     |                                                                                                   |
| <span data-ttu-id="d033e-637">public PrintMedium setTarget(PrintMedium target)</span><span class="sxs-lookup"><span data-stu-id="d033e-637">public PrintMedium setTarget(PrintMedium target)</span></span>                                                        | <span data-ttu-id="d033e-638">印刷メディアを設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-638">Sets the print medium.</span></span>                                                                            |
| <span data-ttu-id="d033e-639">public boolean singleLargePage(\[boolean singleLargePage\])</span><span class="sxs-lookup"><span data-stu-id="d033e-639">public boolean singleLargePage(\[boolean singleLargePage\])</span></span>                                             |                                                                                                   |
| <span data-ttu-id="d033e-640">public boolean skipBitmapsInRTF(\[boolean skipBitmaps\])</span><span class="sxs-lookup"><span data-stu-id="d033e-640">public boolean skipBitmapsInRTF(\[boolean skipBitmaps\])</span></span>                                                | <span data-ttu-id="d033e-641">.rtf ファイルにレポートを印刷するときにビットマップを含めるかどうかをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="d033e-641">Controls whether bitmaps are included when reports are printed to an .rtf file.</span></span>                   |
| <span data-ttu-id="d033e-642">public boolean storeInPrintArchive(\[boolean store\])</span><span class="sxs-lookup"><span data-stu-id="d033e-642">public boolean storeInPrintArchive(\[boolean store\])</span></span>                                                   |                                                                                                   |
| <span data-ttu-id="d033e-643">public boolean suppressScalingMessage(\[boolean suppress\])</span><span class="sxs-lookup"><span data-stu-id="d033e-643">public boolean suppressScalingMessage(\[boolean suppress\])</span></span>                                             |                                                                                                   |
| <span data-ttu-id="d033e-644">public int to(\[int toPage\])</span><span class="sxs-lookup"><span data-stu-id="d033e-644">public int to(\[int toPage\])</span></span>                                                                           |                                                                                                   |
| <span data-ttu-id="d033e-645">public str toString()</span><span class="sxs-lookup"><span data-stu-id="d033e-645">public str toString()</span></span>                                                                                   | <span data-ttu-id="d033e-646">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-646">Returns a string that represents the current object.</span></span>                                              |
| <span data-ttu-id="d033e-647">public boolean unpackPageSettings(container settings)</span><span class="sxs-lookup"><span data-stu-id="d033e-647">public boolean unpackPageSettings(container settings)</span></span>                                                   | <span data-ttu-id="d033e-648">用紙サイズと向きなど、ページ設定を設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-648">Sets the page settings, such as paper size and orientation.</span></span>                                       |
| <span data-ttu-id="d033e-649">public boolean unpackPrinterSettings(container settings)</span><span class="sxs-lookup"><span data-stu-id="d033e-649">public boolean unpackPrinterSettings(container settings)</span></span>                                                |                                                                                                   |
| <span data-ttu-id="d033e-650">public boolean unpackPrintJobSettings(container settings)</span><span class="sxs-lookup"><span data-stu-id="d033e-650">public boolean unpackPrintJobSettings(container settings)</span></span>                                               |                                                                                                   |
| <span data-ttu-id="d033e-651">public boolean unpackSubtotalSettings(container settings)</span><span class="sxs-lookup"><span data-stu-id="d033e-651">public boolean unpackSubtotalSettings(container settings)</span></span>                                               |                                                                                                   |
| <span data-ttu-id="d033e-652">public int unprintableBottom()</span><span class="sxs-lookup"><span data-stu-id="d033e-652">public int unprintableBottom()</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="d033e-653">public int unprintableLeft()</span><span class="sxs-lookup"><span data-stu-id="d033e-653">public int unprintableLeft()</span></span>                                                                            |                                                                                                   |
| <span data-ttu-id="d033e-654">public int unprintableRight()</span><span class="sxs-lookup"><span data-stu-id="d033e-654">public int unprintableRight()</span></span>                                                                           |                                                                                                   |
| <span data-ttu-id="d033e-655">public int unprintableTop()</span><span class="sxs-lookup"><span data-stu-id="d033e-655">public int unprintableTop()</span></span>                                                                             | <span data-ttu-id="d033e-656">用紙の最上部から用紙の印刷可能な範囲までの距離を示します。</span><span class="sxs-lookup"><span data-stu-id="d033e-656">Indicates the distance from the top of the paper to the printable area of the paper.</span></span>              |
| <span data-ttu-id="d033e-657">public ReportOutputUserType viewerType(\[ReportOutputUserType type\])</span><span class="sxs-lookup"><span data-stu-id="d033e-657">public ReportOutputUserType viewerType(\[ReportOutputUserType type\])</span></span>                                   |                                                                                                   |
| <span data-ttu-id="d033e-658">public int virtualPageHeight(\[int height\])</span><span class="sxs-lookup"><span data-stu-id="d033e-658">public int virtualPageHeight(\[int height\])</span></span>                                                            |                                                                                                   |
| <span data-ttu-id="d033e-659">public boolean warnIfFileExists(\[boolean warn\])</span><span class="sxs-lookup"><span data-stu-id="d033e-659">public boolean warnIfFileExists(\[boolean warn\])</span></span>                                                       |                                                                                                   |
| <span data-ttu-id="d033e-660">public void enableBody(\[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="d033e-660">public void enableBody(\[TableId tableId\])</span></span>                                                             |                                                                                                   |
| <span data-ttu-id="d033e-661">public void new(\[container Settings\], \[boolean infoOnly\])</span><span class="sxs-lookup"><span data-stu-id="d033e-661">public void new(\[container Settings\], \[boolean infoOnly\])</span></span>                                           | <span data-ttu-id="d033e-662">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-662">Initializes a new instance of the Object class.</span></span>                                                   |
| <span data-ttu-id="d033e-663">public void addTrayPageCopy(int tray, int pageNumber, \[int copyNumber\])</span><span class="sxs-lookup"><span data-stu-id="d033e-663">public void addTrayPageCopy(int tray, int pageNumber, \[int copyNumber\])</span></span>                               |                                                                                                   |
| <span data-ttu-id="d033e-664">public void disableBody(\[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="d033e-664">public void disableBody(\[TableId tableId\])</span></span>                                                            |                                                                                                   |
| <span data-ttu-id="d033e-665">public void clearTrayPageCopy()</span><span class="sxs-lookup"><span data-stu-id="d033e-665">public void clearTrayPageCopy()</span></span>                                                                         |                                                                                                   |
| <span data-ttu-id="d033e-666">public void rulerInch()</span><span class="sxs-lookup"><span data-stu-id="d033e-666">public void rulerInch()</span></span>                                                                                 |                                                                                                   |
| <span data-ttu-id="d033e-667">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="d033e-667">public void finalize()</span></span>                                                                                  |                                                                                                   |
| <span data-ttu-id="d033e-668">public void rulerOff()</span><span class="sxs-lookup"><span data-stu-id="d033e-668">public void rulerOff()</span></span>                                                                                  |                                                                                                   |
| <span data-ttu-id="d033e-669">public void rulerMetric()</span><span class="sxs-lookup"><span data-stu-id="d033e-669">public void rulerMetric()</span></span>                                                                               |                                                                                                   |

### <a name="method-allpages"></a><span data-ttu-id="d033e-670">メソッド allPages</span><span class="sxs-lookup"><span data-stu-id="d033e-670">Method allPages</span></span>

<span data-ttu-id="d033e-671">sysPrintForm を実行するときに、すべてまたはページのオプション ボタンを選択するかどうかをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="d033e-671">Controls whether the All or Pages option button should be selected when you run the sysPrintForm.</span></span>

    public boolean allPages([boolean all])

#### <a name="parameters"></a><span data-ttu-id="d033e-672">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-672">Parameters</span></span>

<span data-ttu-id="d033e-673">すべて</span><span class="sxs-lookup"><span data-stu-id="d033e-673">all</span></span>  
<span data-ttu-id="d033e-674">true の場合、すべてのオプション ボタンが選択されるブール値; それ以外の場合は、ページ オプション ボタンが選択されます。</span><span class="sxs-lookup"><span data-stu-id="d033e-674">A boolean value that, if true, the All option button is selected; otherwise, the Pages option button is selected.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d033e-675">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-675">Return Value</span></span>

<span data-ttu-id="d033e-676">すべてのオプション ボタンを選択する必要がある場合は true。それ以外の場合は false で、ページのオプション ボタンが選択されます。</span><span class="sxs-lookup"><span data-stu-id="d033e-676">true if the All radio button should be selected; otherwise, false, and the Pages option button is selected.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-677">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-677">Remarks</span></span>

<span data-ttu-id="d033e-678">このメソッドは、sysPrintForm によって内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d033e-678">The method is for internal use by sysPrintForm.</span></span>

#### <a name="examples"></a><span data-ttu-id="d033e-679">例</span><span class="sxs-lookup"><span data-stu-id="d033e-679">Examples</span></span>

<span data-ttu-id="d033e-680">次の例では、2 〜 4 のページを印刷し、[すべてのオプション] ボタンではなく [ページのオプション] ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="d033e-680">The following example prints pages 2 to 4 and selects the Pages option button instead of the All option button.</span></span>

    static void PrintingToPDF(Args _args) 
    { 
        Args                args; 
        ReportRun           rr; 
        str reportName = 'Cust'; 
        int i; 
        int numReports = 10; 
        args = new Args(reportName); 
        rr = new ReportRun(args,''); 
        rr.setTarget(Printmedium::File); 
        rr.printJobSettings().format(PrintFormat::RTF); 
        rr.printJobSettings().fileName("C:\\tmp\\Cust_ReportRange2.rtf"); 
        // Select the Pages option button rather than the All option button. 
        rr.printJobSettings().allPages(false); 
        rr.printJobSettings().from(2); 
        rr.printJobSettings().to(4); 
        rr.query().interactive(false); 
        rr.report().interactive(false); 
        rr.run(); 
    }

### <a name="method-appendtotextfile"></a><span data-ttu-id="d033e-681">メソッド appendToTextFile</span><span class="sxs-lookup"><span data-stu-id="d033e-681">Method appendToTextFile</span></span>

    public boolean appendToTextFile([boolean append])

#### <a name="parameters"></a><span data-ttu-id="d033e-682">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-682">Parameters</span></span>

<span data-ttu-id="d033e-683">append</span><span class="sxs-lookup"><span data-stu-id="d033e-683">append</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-684">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-684">Return Value</span></span>

### <a name="method-banding"></a><span data-ttu-id="d033e-685">メソッド banding</span><span class="sxs-lookup"><span data-stu-id="d033e-685">Method banding</span></span>

    public boolean banding()

#### <a name="return-value"></a><span data-ttu-id="d033e-686">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-686">Return Value</span></span>

### <a name="method-clientprintjobsettings"></a><span data-ttu-id="d033e-687">メソッド clientPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="d033e-687">Method clientPrintJobSettings</span></span>

    public PrintJobSettings clientPrintJobSettings()

#### <a name="return-value"></a><span data-ttu-id="d033e-688">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-688">Return Value</span></span>

### <a name="method-collate"></a><span data-ttu-id="d033e-689">メソッド collate</span><span class="sxs-lookup"><span data-stu-id="d033e-689">Method collate</span></span>

    public boolean collate([boolean collate])

#### <a name="parameters"></a><span data-ttu-id="d033e-690">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-690">Parameters</span></span>

<span data-ttu-id="d033e-691">collate</span><span class="sxs-lookup"><span data-stu-id="d033e-691">collate</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-692">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-692">Return Value</span></span>

### <a name="method-copies"></a><span data-ttu-id="d033e-693">メソッド copies</span><span class="sxs-lookup"><span data-stu-id="d033e-693">Method copies</span></span>

    public int copies([int numberOfCopies])

#### <a name="parameters"></a><span data-ttu-id="d033e-694">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-694">Parameters</span></span>

<span data-ttu-id="d033e-695">numberOfCopies</span><span class="sxs-lookup"><span data-stu-id="d033e-695">numberOfCopies</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-696">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-696">Return Value</span></span>

### <a name="method-copydescription"></a><span data-ttu-id="d033e-697">メソッド copyDescription</span><span class="sxs-lookup"><span data-stu-id="d033e-697">Method copyDescription</span></span>

    public str copyDescription(int number, [str description])

#### <a name="parameters"></a><span data-ttu-id="d033e-698">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-698">Parameters</span></span>

<span data-ttu-id="d033e-699">数値</span><span class="sxs-lookup"><span data-stu-id="d033e-699">number</span></span>  

<!-- -->

<span data-ttu-id="d033e-700">description</span><span class="sxs-lookup"><span data-stu-id="d033e-700">description</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-701">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-701">Return Value</span></span>

### <a name="method-devicename"></a><span data-ttu-id="d033e-702">メソッド deviceName</span><span class="sxs-lookup"><span data-stu-id="d033e-702">Method deviceName</span></span>

<span data-ttu-id="d033e-703">プリンターを選択するか、選択されているプリンター デバイス名を取得します。</span><span class="sxs-lookup"><span data-stu-id="d033e-703">Selects a printer or retrieves the deviceName of the selected printer.</span></span>

    public str deviceName([str device], [ClassRunMode runOn])

#### <a name="parameters"></a><span data-ttu-id="d033e-704">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-704">Parameters</span></span>

<span data-ttu-id="d033e-705">デバイス</span><span class="sxs-lookup"><span data-stu-id="d033e-705">device</span></span>  

<!-- -->

<span data-ttu-id="d033e-706">runOn</span><span class="sxs-lookup"><span data-stu-id="d033e-706">runOn</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-707">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-707">Return Value</span></span>

<span data-ttu-id="d033e-708">選択したプリンターの deviceName。</span><span class="sxs-lookup"><span data-stu-id="d033e-708">The deviceName of the selected printer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-709">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-709">Remarks</span></span>

<span data-ttu-id="d033e-710">選択されるプリンターの deviceName は、getPrinter メソッドを使用して検出できます。</span><span class="sxs-lookup"><span data-stu-id="d033e-710">The deviceName of a printer to be selected could be found by using the getPrinter method.</span></span>

#### <a name="examples"></a><span data-ttu-id="d033e-711">例</span><span class="sxs-lookup"><span data-stu-id="d033e-711">Examples</span></span>

<span data-ttu-id="d033e-712">このジョブは、利用可能なプリンターと印刷できない領域を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="d033e-712">This job lists the available printers and their nonprintable area.</span></span>

    static void aaaKJ(args a) 
    { 
        printJobSettings pjs; 
        str printer; 
        int i; 
        pjs = new printJobSettings(); 
        for (i=1; i<=pjs.GetNumberOfPrinters(); i++) 
        { 
            printer = pjs.GetPrinter(i); 
            pjs.DeviceName(printer); 
            print "printer No. ",i, " has name ",  printer; 
            print "   left:  ", pjs.UnprintableLeft(),   "/100 mm"; 
            print "   right: ", pjs.UnprintableRight(),  "/100 mm"; 
            print "   top:   ", pjs.UnprintableTop(),    "/100 mm"; 
            print "   bottom:", pjs.UnprintableBottom(), "/100 mm"; 
        } 
        pause; 
    }

### <a name="method-donotoverwrite"></a><span data-ttu-id="d033e-713">メソッド doNotOverwrite</span><span class="sxs-lookup"><span data-stu-id="d033e-713">Method doNotOverwrite</span></span>

    public boolean doNotOverwrite([boolean warn])

#### <a name="parameters"></a><span data-ttu-id="d033e-714">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-714">Parameters</span></span>

<span data-ttu-id="d033e-715">警告</span><span class="sxs-lookup"><span data-stu-id="d033e-715">warn</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-716">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-716">Return Value</span></span>

### <a name="method-enablecopies"></a><span data-ttu-id="d033e-717">メソッド enableCopies</span><span class="sxs-lookup"><span data-stu-id="d033e-717">Method enableCopies</span></span>

    public boolean enableCopies([boolean enable])

#### <a name="parameters"></a><span data-ttu-id="d033e-718">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-718">Parameters</span></span>

<span data-ttu-id="d033e-719">enable</span><span class="sxs-lookup"><span data-stu-id="d033e-719">enable</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-720">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-720">Return Value</span></span>

### <a name="method-enabledevice"></a><span data-ttu-id="d033e-721">メソッド enableDevice</span><span class="sxs-lookup"><span data-stu-id="d033e-721">Method enableDevice</span></span>

    public boolean enableDevice([boolean enable])

#### <a name="parameters"></a><span data-ttu-id="d033e-722">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-722">Parameters</span></span>

<span data-ttu-id="d033e-723">enable</span><span class="sxs-lookup"><span data-stu-id="d033e-723">enable</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-724">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-724">Return Value</span></span>

### <a name="method-enablepages"></a><span data-ttu-id="d033e-725">メソッド enablePages</span><span class="sxs-lookup"><span data-stu-id="d033e-725">Method enablePages</span></span>

    public boolean enablePages([boolean enable])

#### <a name="parameters"></a><span data-ttu-id="d033e-726">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-726">Parameters</span></span>

<span data-ttu-id="d033e-727">enable</span><span class="sxs-lookup"><span data-stu-id="d033e-727">enable</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-728">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-728">Return Value</span></span>

### <a name="method-enableproperties"></a><span data-ttu-id="d033e-729">メソッド enableProperties</span><span class="sxs-lookup"><span data-stu-id="d033e-729">Method enableProperties</span></span>

    public boolean enableProperties([boolean enable])

#### <a name="parameters"></a><span data-ttu-id="d033e-730">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-730">Parameters</span></span>

<span data-ttu-id="d033e-731">enable</span><span class="sxs-lookup"><span data-stu-id="d033e-731">enable</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-732">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-732">Return Value</span></span>

### <a name="method-enablestoreinprintarchive"></a><span data-ttu-id="d033e-733">メソッド enableStoreInPrintArchive</span><span class="sxs-lookup"><span data-stu-id="d033e-733">Method enableStoreInPrintArchive</span></span>

    public boolean enableStoreInPrintArchive([boolean enable])

#### <a name="parameters"></a><span data-ttu-id="d033e-734">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-734">Parameters</span></span>

<span data-ttu-id="d033e-735">enable</span><span class="sxs-lookup"><span data-stu-id="d033e-735">enable</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-736">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-736">Return Value</span></span>

### <a name="method-enabletarget"></a><span data-ttu-id="d033e-737">メソッド enableTarget</span><span class="sxs-lookup"><span data-stu-id="d033e-737">Method enableTarget</span></span>

    public boolean enableTarget([boolean enable])

#### <a name="parameters"></a><span data-ttu-id="d033e-738">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-738">Parameters</span></span>

<span data-ttu-id="d033e-739">enable</span><span class="sxs-lookup"><span data-stu-id="d033e-739">enable</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-740">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-740">Return Value</span></span>

### <a name="method-facename2number"></a><span data-ttu-id="d033e-741">メソッド facename2number</span><span class="sxs-lookup"><span data-stu-id="d033e-741">Method facename2number</span></span>

    public int facename2number([str facename])

#### <a name="parameters"></a><span data-ttu-id="d033e-742">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-742">Parameters</span></span>

<span data-ttu-id="d033e-743">facename</span><span class="sxs-lookup"><span data-stu-id="d033e-743">facename</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-744">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-744">Return Value</span></span>

### <a name="method-filename"></a><span data-ttu-id="d033e-745">メソッド fileName</span><span class="sxs-lookup"><span data-stu-id="d033e-745">Method fileName</span></span>

    public str fileName([str FileName])

#### <a name="parameters"></a><span data-ttu-id="d033e-746">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-746">Parameters</span></span>

<span data-ttu-id="d033e-747">FileName</span><span class="sxs-lookup"><span data-stu-id="d033e-747">FileName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-748">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-748">Return Value</span></span>

### <a name="method-fittopage"></a><span data-ttu-id="d033e-749">メソッド fitToPage</span><span class="sxs-lookup"><span data-stu-id="d033e-749">Method fitToPage</span></span>

    public boolean fitToPage([boolean fit])

#### <a name="parameters"></a><span data-ttu-id="d033e-750">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-750">Parameters</span></span>

<span data-ttu-id="d033e-751">fit</span><span class="sxs-lookup"><span data-stu-id="d033e-751">fit</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-752">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-752">Return Value</span></span>

### <a name="method-format"></a><span data-ttu-id="d033e-753">メソッド format</span><span class="sxs-lookup"><span data-stu-id="d033e-753">Method format</span></span>

    public PrintFormat format([PrintFormat format])

#### <a name="parameters"></a><span data-ttu-id="d033e-754">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-754">Parameters</span></span>

<span data-ttu-id="d033e-755">形式</span><span class="sxs-lookup"><span data-stu-id="d033e-755">format</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-756">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-756">Return Value</span></span>

### <a name="method-from"></a><span data-ttu-id="d033e-757">メソッド from</span><span class="sxs-lookup"><span data-stu-id="d033e-757">Method from</span></span>

    public int from([int fromPage])

#### <a name="parameters"></a><span data-ttu-id="d033e-758">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-758">Parameters</span></span>

<span data-ttu-id="d033e-759">fromPage</span><span class="sxs-lookup"><span data-stu-id="d033e-759">fromPage</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-760">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-760">Return Value</span></span>

### <a name="method-getfacename"></a><span data-ttu-id="d033e-761">メソッド getFacename</span><span class="sxs-lookup"><span data-stu-id="d033e-761">Method getFacename</span></span>

    public str getFacename(int number)

#### <a name="parameters"></a><span data-ttu-id="d033e-762">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-762">Parameters</span></span>

<span data-ttu-id="d033e-763">数値</span><span class="sxs-lookup"><span data-stu-id="d033e-763">number</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-764">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-764">Return Value</span></span>

### <a name="method-getfacenameinfo"></a><span data-ttu-id="d033e-765">メソッド getFacenameInfo</span><span class="sxs-lookup"><span data-stu-id="d033e-765">Method getFacenameInfo</span></span>

    public str getFacenameInfo(int number)

#### <a name="parameters"></a><span data-ttu-id="d033e-766">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-766">Parameters</span></span>

<span data-ttu-id="d033e-767">数値</span><span class="sxs-lookup"><span data-stu-id="d033e-767">number</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-768">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-768">Return Value</span></span>

### <a name="method-getfontinfo"></a><span data-ttu-id="d033e-769">メソッド getFontInfo</span><span class="sxs-lookup"><span data-stu-id="d033e-769">Method getFontInfo</span></span>

    public Struct getFontInfo(str fontName)

#### <a name="parameters"></a><span data-ttu-id="d033e-770">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-770">Parameters</span></span>

<span data-ttu-id="d033e-771">fontName</span><span class="sxs-lookup"><span data-stu-id="d033e-771">fontName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-772">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-772">Return Value</span></span>

### <a name="method-getglyphwidthsarray"></a><span data-ttu-id="d033e-773">メソッド getGlyphWidthsArray</span><span class="sxs-lookup"><span data-stu-id="d033e-773">Method getGlyphWidthsArray</span></span>

    public Array getGlyphWidthsArray(str fontName, int firstChar, int lastChar)

#### <a name="parameters"></a><span data-ttu-id="d033e-774">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-774">Parameters</span></span>

<span data-ttu-id="d033e-775">fontName</span><span class="sxs-lookup"><span data-stu-id="d033e-775">fontName</span></span>  

<!-- -->

<span data-ttu-id="d033e-776">firstChar</span><span class="sxs-lookup"><span data-stu-id="d033e-776">firstChar</span></span>  

<!-- -->

<span data-ttu-id="d033e-777">lastChar</span><span class="sxs-lookup"><span data-stu-id="d033e-777">lastChar</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-778">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-778">Return Value</span></span>

### <a name="method-getnumberofclientprinters"></a><span data-ttu-id="d033e-779">メソッド getNumberOfClientPrinters</span><span class="sxs-lookup"><span data-stu-id="d033e-779">Method getNumberOfClientPrinters</span></span>

    public int getNumberOfClientPrinters()

#### <a name="return-value"></a><span data-ttu-id="d033e-780">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-780">Return Value</span></span>

### <a name="method-getnumberoffacenames"></a><span data-ttu-id="d033e-781">メソッド getNumberOfFacenames</span><span class="sxs-lookup"><span data-stu-id="d033e-781">Method getNumberOfFacenames</span></span>

    public int getNumberOfFacenames()

#### <a name="return-value"></a><span data-ttu-id="d033e-782">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-782">Return Value</span></span>

### <a name="method-getnumberofprinters"></a><span data-ttu-id="d033e-783">メソッド getNumberOfPrinters</span><span class="sxs-lookup"><span data-stu-id="d033e-783">Method getNumberOfPrinters</span></span>

<span data-ttu-id="d033e-784">コンピューターに設定されているプリンターの数を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-784">Returns the number of printers that are set up on the computer.</span></span>

    public int getNumberOfPrinters()

#### <a name="return-value"></a><span data-ttu-id="d033e-785">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-785">Return Value</span></span>

<span data-ttu-id="d033e-786">コンピューターに設定されているプリンターの数。</span><span class="sxs-lookup"><span data-stu-id="d033e-786">The number of printers that are set up on the computer.</span></span>

### <a name="method-getnumberofserverprinters"></a><span data-ttu-id="d033e-787">メソッド getNumberOfServerPrinters</span><span class="sxs-lookup"><span data-stu-id="d033e-787">Method getNumberOfServerPrinters</span></span>

    public int getNumberOfServerPrinters()

#### <a name="return-value"></a><span data-ttu-id="d033e-788">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-788">Return Value</span></span>

### <a name="method-getnumberoftrays"></a><span data-ttu-id="d033e-789">メソッド getNumberOfTrays</span><span class="sxs-lookup"><span data-stu-id="d033e-789">Method getNumberOfTrays</span></span>

    public int getNumberOfTrays()

#### <a name="return-value"></a><span data-ttu-id="d033e-790">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-790">Return Value</span></span>

### <a name="method-getprinter"></a><span data-ttu-id="d033e-791">メソッド getPrinter</span><span class="sxs-lookup"><span data-stu-id="d033e-791">Method getPrinter</span></span>

<span data-ttu-id="d033e-792">プリンターの deviceName を取得します。</span><span class="sxs-lookup"><span data-stu-id="d033e-792">Gets the deviceName of a printer.</span></span>

    public str getPrinter(int number)

#### <a name="parameters"></a><span data-ttu-id="d033e-793">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-793">Parameters</span></span>

<span data-ttu-id="d033e-794">数値</span><span class="sxs-lookup"><span data-stu-id="d033e-794">number</span></span>  
<span data-ttu-id="d033e-795">1 から使用可能なプリンターの数までの値。</span><span class="sxs-lookup"><span data-stu-id="d033e-795">A value between 1 and the number of available printers.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d033e-796">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-796">Return Value</span></span>

<span data-ttu-id="d033e-797">指定されたプリンター番号の deviceName。</span><span class="sxs-lookup"><span data-stu-id="d033e-797">The deviceName of the given printer number.</span></span>

#### <a name="examples"></a><span data-ttu-id="d033e-798">例</span><span class="sxs-lookup"><span data-stu-id="d033e-798">Examples</span></span>

    printJobSettings pjs; 
    int i; 
    pjs = new printJobSettings(); 
    i = 1; 
    while (i<=pjs.GetNumberOfPrinters()) 
    { 
        print "Printer No. ", i, " is ", pjs.GetPrinter(i); 
        i++; 
    }

### <a name="method-getrunon"></a><span data-ttu-id="d033e-799">メソッド getRunOn</span><span class="sxs-lookup"><span data-stu-id="d033e-799">Method getRunOn</span></span>

    public ClassRunMode getRunOn(int number)

#### <a name="parameters"></a><span data-ttu-id="d033e-800">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-800">Parameters</span></span>

<span data-ttu-id="d033e-801">数値</span><span class="sxs-lookup"><span data-stu-id="d033e-801">number</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-802">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-802">Return Value</span></span>

### <a name="method-gettarget"></a><span data-ttu-id="d033e-803">メソッド getTarget</span><span class="sxs-lookup"><span data-stu-id="d033e-803">Method getTarget</span></span>

    public PrintMedium getTarget()

#### <a name="return-value"></a><span data-ttu-id="d033e-804">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-804">Return Value</span></span>

### <a name="method-gettray"></a><span data-ttu-id="d033e-805">メソッド getTray</span><span class="sxs-lookup"><span data-stu-id="d033e-805">Method getTray</span></span>

    public int getTray(int number)

#### <a name="parameters"></a><span data-ttu-id="d033e-806">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-806">Parameters</span></span>

<span data-ttu-id="d033e-807">数値</span><span class="sxs-lookup"><span data-stu-id="d033e-807">number</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-808">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-808">Return Value</span></span>

### <a name="method-gettrayname"></a><span data-ttu-id="d033e-809">メソッド getTrayName</span><span class="sxs-lookup"><span data-stu-id="d033e-809">Method getTrayName</span></span>

    public str getTrayName(int number)

#### <a name="parameters"></a><span data-ttu-id="d033e-810">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-810">Parameters</span></span>

<span data-ttu-id="d033e-811">数値</span><span class="sxs-lookup"><span data-stu-id="d033e-811">number</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-812">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-812">Return Value</span></span>

### <a name="method-hdc"></a><span data-ttu-id="d033e-813">メソッド hDC</span><span class="sxs-lookup"><span data-stu-id="d033e-813">Method hDC</span></span>

    public Int64 hDC()

#### <a name="return-value"></a><span data-ttu-id="d033e-814">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-814">Return Value</span></span>

### <a name="method-lockdestinationproperties"></a><span data-ttu-id="d033e-815">メソッド lockDestinationProperties</span><span class="sxs-lookup"><span data-stu-id="d033e-815">Method lockDestinationProperties</span></span>

    public boolean lockDestinationProperties([boolean warn])

#### <a name="parameters"></a><span data-ttu-id="d033e-816">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-816">Parameters</span></span>

<span data-ttu-id="d033e-817">警告</span><span class="sxs-lookup"><span data-stu-id="d033e-817">warn</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-818">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-818">Return Value</span></span>

### <a name="method-mailcc"></a><span data-ttu-id="d033e-819">メソッド mailCc</span><span class="sxs-lookup"><span data-stu-id="d033e-819">Method mailCc</span></span>

    public str mailCc([str MailCc])

#### <a name="parameters"></a><span data-ttu-id="d033e-820">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-820">Parameters</span></span>

<span data-ttu-id="d033e-821">MailCc</span><span class="sxs-lookup"><span data-stu-id="d033e-821">MailCc</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-822">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-822">Return Value</span></span>

### <a name="method-mailsubject"></a><span data-ttu-id="d033e-823">メソッド mailSubject</span><span class="sxs-lookup"><span data-stu-id="d033e-823">Method mailSubject</span></span>

    public str mailSubject([str MailSubject])

#### <a name="parameters"></a><span data-ttu-id="d033e-824">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-824">Parameters</span></span>

<span data-ttu-id="d033e-825">MailSubject</span><span class="sxs-lookup"><span data-stu-id="d033e-825">MailSubject</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-826">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-826">Return Value</span></span>

### <a name="method-mailto"></a><span data-ttu-id="d033e-827">メソッド mailTo</span><span class="sxs-lookup"><span data-stu-id="d033e-827">Method mailTo</span></span>

    public str mailTo([str MailTo])

#### <a name="parameters"></a><span data-ttu-id="d033e-828">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-828">Parameters</span></span>

<span data-ttu-id="d033e-829">MailTo</span><span class="sxs-lookup"><span data-stu-id="d033e-829">MailTo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-830">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-830">Return Value</span></span>

### <a name="method-numberofcopydescriptions"></a><span data-ttu-id="d033e-831">メソッド numberOfCopyDescriptions</span><span class="sxs-lookup"><span data-stu-id="d033e-831">Method numberOfCopyDescriptions</span></span>

    public int numberOfCopyDescriptions(int number)

#### <a name="parameters"></a><span data-ttu-id="d033e-832">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-832">Parameters</span></span>

<span data-ttu-id="d033e-833">数値</span><span class="sxs-lookup"><span data-stu-id="d033e-833">number</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-834">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-834">Return Value</span></span>

### <a name="method-outputtoclient"></a><span data-ttu-id="d033e-835">メソッド outputToClient</span><span class="sxs-lookup"><span data-stu-id="d033e-835">Method outputToClient</span></span>

    public boolean outputToClient([boolean toClient])

#### <a name="parameters"></a><span data-ttu-id="d033e-836">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-836">Parameters</span></span>

<span data-ttu-id="d033e-837">toClient</span><span class="sxs-lookup"><span data-stu-id="d033e-837">toClient</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-838">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-838">Return Value</span></span>

### <a name="method-outputtoprnfile"></a><span data-ttu-id="d033e-839">メソッド outputToPrnFile</span><span class="sxs-lookup"><span data-stu-id="d033e-839">Method outputToPrnFile</span></span>

    public boolean outputToPrnFile([boolean writePrnFile])

#### <a name="parameters"></a><span data-ttu-id="d033e-840">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-840">Parameters</span></span>

<span data-ttu-id="d033e-841">writePrnFile</span><span class="sxs-lookup"><span data-stu-id="d033e-841">writePrnFile</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-842">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-842">Return Value</span></span>

### <a name="method-packnamesandprinterdata"></a><span data-ttu-id="d033e-843">メソッド packNamesAndPrinterData</span><span class="sxs-lookup"><span data-stu-id="d033e-843">Method packNamesAndPrinterData</span></span>

    public container packNamesAndPrinterData()

#### <a name="return-value"></a><span data-ttu-id="d033e-844">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-844">Return Value</span></span>

### <a name="method-packpagesettings"></a><span data-ttu-id="d033e-845">メソッド packPageSettings</span><span class="sxs-lookup"><span data-stu-id="d033e-845">Method packPageSettings</span></span>

<span data-ttu-id="d033e-846">ページの書式設定時に選択されているデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="d033e-846">Stores the data that is selected during page formatting in a container.</span></span>

    public container packPageSettings()

#### <a name="return-value"></a><span data-ttu-id="d033e-847">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-847">Return Value</span></span>

<span data-ttu-id="d033e-848">ページの書式設定時に選択されているデータを保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="d033e-848">A container that holds data that is selected during page formatting.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-849">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-849">Remarks</span></span>

<span data-ttu-id="d033e-850">返されたコンテナーは、unpackPageSettings メソッドへの入力として使用できます。</span><span class="sxs-lookup"><span data-stu-id="d033e-850">The returned container can be used as input to the unpackPageSettings method.</span></span>

### <a name="method-packprintersettings"></a><span data-ttu-id="d033e-851">メソッド packPrinterSettings</span><span class="sxs-lookup"><span data-stu-id="d033e-851">Method packPrinterSettings</span></span>

    public container packPrinterSettings()

#### <a name="return-value"></a><span data-ttu-id="d033e-852">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-852">Return Value</span></span>

### <a name="method-packprintjobsettings"></a><span data-ttu-id="d033e-853">メソッド packPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="d033e-853">Method packPrintJobSettings</span></span>

    public container packPrintJobSettings()

#### <a name="return-value"></a><span data-ttu-id="d033e-854">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-854">Return Value</span></span>

### <a name="method-packsubtotalsettings"></a><span data-ttu-id="d033e-855">メソッド packSubtotalSettings</span><span class="sxs-lookup"><span data-stu-id="d033e-855">Method packSubtotalSettings</span></span>

    public container packSubtotalSettings()

#### <a name="return-value"></a><span data-ttu-id="d033e-856">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-856">Return Value</span></span>

### <a name="method-pagecopy2tray"></a><span data-ttu-id="d033e-857">メソッド pageCopy2Tray</span><span class="sxs-lookup"><span data-stu-id="d033e-857">Method pageCopy2Tray</span></span>

    public int pageCopy2Tray(int pageNumber, [int copyNumber])

#### <a name="parameters"></a><span data-ttu-id="d033e-858">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-858">Parameters</span></span>

<span data-ttu-id="d033e-859">pageNumber</span><span class="sxs-lookup"><span data-stu-id="d033e-859">pageNumber</span></span>  

<!-- -->

<span data-ttu-id="d033e-860">copyNumber</span><span class="sxs-lookup"><span data-stu-id="d033e-860">copyNumber</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-861">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-861">Return Value</span></span>

### <a name="method-pageformatting"></a><span data-ttu-id="d033e-862">メソッド pageFormatting</span><span class="sxs-lookup"><span data-stu-id="d033e-862">Method pageFormatting</span></span>

    public boolean pageFormatting()

#### <a name="return-value"></a><span data-ttu-id="d033e-863">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-863">Return Value</span></span>

### <a name="method-paperorientation"></a><span data-ttu-id="d033e-864">メソッド paperOrientation</span><span class="sxs-lookup"><span data-stu-id="d033e-864">Method paperOrientation</span></span>

    public PrinterOrientation paperOrientation([PrinterOrientation orientation])

#### <a name="parameters"></a><span data-ttu-id="d033e-865">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-865">Parameters</span></span>

<span data-ttu-id="d033e-866">orientation</span><span class="sxs-lookup"><span data-stu-id="d033e-866">orientation</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-867">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-867">Return Value</span></span>

### <a name="method-papertray"></a><span data-ttu-id="d033e-868">メソッド paperTray</span><span class="sxs-lookup"><span data-stu-id="d033e-868">Method paperTray</span></span>

    public int paperTray([int tray])

#### <a name="parameters"></a><span data-ttu-id="d033e-869">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-869">Parameters</span></span>

<span data-ttu-id="d033e-870">トレイ</span><span class="sxs-lookup"><span data-stu-id="d033e-870">tray</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-871">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-871">Return Value</span></span>

### <a name="method-papertrayraw"></a><span data-ttu-id="d033e-872">メソッド paperTrayRaw</span><span class="sxs-lookup"><span data-stu-id="d033e-872">Method paperTrayRaw</span></span>

    public int paperTrayRaw([int tray])

#### <a name="parameters"></a><span data-ttu-id="d033e-873">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-873">Parameters</span></span>

<span data-ttu-id="d033e-874">トレイ</span><span class="sxs-lookup"><span data-stu-id="d033e-874">tray</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-875">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-875">Return Value</span></span>

### <a name="method-performancetest"></a><span data-ttu-id="d033e-876">メソッド performanceTest</span><span class="sxs-lookup"><span data-stu-id="d033e-876">Method performanceTest</span></span>

    public int performanceTest([int loops])

#### <a name="parameters"></a><span data-ttu-id="d033e-877">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-877">Parameters</span></span>

<span data-ttu-id="d033e-878">loops</span><span class="sxs-lookup"><span data-stu-id="d033e-878">loops</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-879">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-879">Return Value</span></span>

### <a name="method-preferredfileformat"></a><span data-ttu-id="d033e-880">メソッド preferredFileFormat</span><span class="sxs-lookup"><span data-stu-id="d033e-880">Method preferredFileFormat</span></span>

    public PrintFormat preferredFileFormat([PrintFormat format])

#### <a name="parameters"></a><span data-ttu-id="d033e-881">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-881">Parameters</span></span>

<span data-ttu-id="d033e-882">形式</span><span class="sxs-lookup"><span data-stu-id="d033e-882">format</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-883">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-883">Return Value</span></span>

### <a name="method-preferredmailformat"></a><span data-ttu-id="d033e-884">メソッド preferredMailFormat</span><span class="sxs-lookup"><span data-stu-id="d033e-884">Method preferredMailFormat</span></span>

    public PrintFormat preferredMailFormat([PrintFormat format])

#### <a name="parameters"></a><span data-ttu-id="d033e-885">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-885">Parameters</span></span>

<span data-ttu-id="d033e-886">形式</span><span class="sxs-lookup"><span data-stu-id="d033e-886">format</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-887">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-887">Return Value</span></span>

### <a name="method-preferredorientation"></a><span data-ttu-id="d033e-888">メソッド preferredOrientation</span><span class="sxs-lookup"><span data-stu-id="d033e-888">Method preferredOrientation</span></span>

    public PrinterOrientation preferredOrientation([PrinterOrientation orientation])

#### <a name="parameters"></a><span data-ttu-id="d033e-889">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-889">Parameters</span></span>

<span data-ttu-id="d033e-890">orientation</span><span class="sxs-lookup"><span data-stu-id="d033e-890">orientation</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-891">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-891">Return Value</span></span>

### <a name="method-preferredtarget"></a><span data-ttu-id="d033e-892">メソッド preferredTarget</span><span class="sxs-lookup"><span data-stu-id="d033e-892">Method preferredTarget</span></span>

    public PrintMedium preferredTarget([PrintMedium target])

#### <a name="parameters"></a><span data-ttu-id="d033e-893">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-893">Parameters</span></span>

<span data-ttu-id="d033e-894">target</span><span class="sxs-lookup"><span data-stu-id="d033e-894">target</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-895">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-895">Return Value</span></span>

### <a name="method-printerattributes"></a><span data-ttu-id="d033e-896">メソッド printerAttributes</span><span class="sxs-lookup"><span data-stu-id="d033e-896">Method printerAttributes</span></span>

    public int printerAttributes()

#### <a name="return-value"></a><span data-ttu-id="d033e-897">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-897">Return Value</span></span>

### <a name="method-printeraverageppm"></a><span data-ttu-id="d033e-898">メソッド printerAveragePPM</span><span class="sxs-lookup"><span data-stu-id="d033e-898">Method printerAveragePPM</span></span>

    public int printerAveragePPM()

#### <a name="return-value"></a><span data-ttu-id="d033e-899">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-899">Return Value</span></span>

### <a name="method-printercomment"></a><span data-ttu-id="d033e-900">メソッド printerComment</span><span class="sxs-lookup"><span data-stu-id="d033e-900">Method printerComment</span></span>

    public str printerComment()

#### <a name="return-value"></a><span data-ttu-id="d033e-901">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-901">Return Value</span></span>

### <a name="method-printerdatatype"></a><span data-ttu-id="d033e-902">メソッド printerDatatype</span><span class="sxs-lookup"><span data-stu-id="d033e-902">Method printerDatatype</span></span>

    public str printerDatatype()

#### <a name="return-value"></a><span data-ttu-id="d033e-903">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-903">Return Value</span></span>

### <a name="method-printerdefaultpriority"></a><span data-ttu-id="d033e-904">メソッド printerDefaultPriority</span><span class="sxs-lookup"><span data-stu-id="d033e-904">Method printerDefaultPriority</span></span>

    public int printerDefaultPriority()

#### <a name="return-value"></a><span data-ttu-id="d033e-905">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-905">Return Value</span></span>

### <a name="method-printerdrivername"></a><span data-ttu-id="d033e-906">メソッド printerDriverName</span><span class="sxs-lookup"><span data-stu-id="d033e-906">Method printerDriverName</span></span>

    public str printerDriverName()

#### <a name="return-value"></a><span data-ttu-id="d033e-907">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-907">Return Value</span></span>

### <a name="method-printerlocation"></a><span data-ttu-id="d033e-908">メソッド printerLocation</span><span class="sxs-lookup"><span data-stu-id="d033e-908">Method printerLocation</span></span>

    public str printerLocation()

#### <a name="return-value"></a><span data-ttu-id="d033e-909">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-909">Return Value</span></span>

### <a name="method-printerpageheight"></a><span data-ttu-id="d033e-910">メソッド printerPageHeight</span><span class="sxs-lookup"><span data-stu-id="d033e-910">Method printerPageHeight</span></span>

    public int printerPageHeight()

#### <a name="return-value"></a><span data-ttu-id="d033e-911">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-911">Return Value</span></span>

### <a name="method-printerpagewidth"></a><span data-ttu-id="d033e-912">メソッド printerPageWidth</span><span class="sxs-lookup"><span data-stu-id="d033e-912">Method printerPageWidth</span></span>

    public int printerPageWidth()

#### <a name="return-value"></a><span data-ttu-id="d033e-913">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-913">Return Value</span></span>

### <a name="method-printerpaper"></a><span data-ttu-id="d033e-914">メソッド printerPaper</span><span class="sxs-lookup"><span data-stu-id="d033e-914">Method printerPaper</span></span>

    public int printerPaper()

#### <a name="return-value"></a><span data-ttu-id="d033e-915">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-915">Return Value</span></span>

### <a name="method-printerparameters"></a><span data-ttu-id="d033e-916">メソッド printerParameters</span><span class="sxs-lookup"><span data-stu-id="d033e-916">Method printerParameters</span></span>

    public str printerParameters()

#### <a name="return-value"></a><span data-ttu-id="d033e-917">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-917">Return Value</span></span>

### <a name="method-printerportname"></a><span data-ttu-id="d033e-918">メソッド printerPortName</span><span class="sxs-lookup"><span data-stu-id="d033e-918">Method printerPortName</span></span>

    public str printerPortName()

#### <a name="return-value"></a><span data-ttu-id="d033e-919">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-919">Return Value</span></span>

### <a name="method-printerprintername"></a><span data-ttu-id="d033e-920">メソッド printerPrinterName</span><span class="sxs-lookup"><span data-stu-id="d033e-920">Method printerPrinterName</span></span>

    public str printerPrinterName()

#### <a name="return-value"></a><span data-ttu-id="d033e-921">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-921">Return Value</span></span>

### <a name="method-printerprintprocessor"></a><span data-ttu-id="d033e-922">メソッド printerPrintProcessor</span><span class="sxs-lookup"><span data-stu-id="d033e-922">Method printerPrintProcessor</span></span>

    public str printerPrintProcessor()

#### <a name="return-value"></a><span data-ttu-id="d033e-923">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-923">Return Value</span></span>

### <a name="method-printerpriority"></a><span data-ttu-id="d033e-924">メソッド printerPriority</span><span class="sxs-lookup"><span data-stu-id="d033e-924">Method printerPriority</span></span>

    public int printerPriority()

#### <a name="return-value"></a><span data-ttu-id="d033e-925">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-925">Return Value</span></span>

### <a name="method-printerqueuedjobs"></a><span data-ttu-id="d033e-926">メソッド printerQueuedJobs</span><span class="sxs-lookup"><span data-stu-id="d033e-926">Method printerQueuedJobs</span></span>

    public int printerQueuedJobs()

#### <a name="return-value"></a><span data-ttu-id="d033e-927">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-927">Return Value</span></span>

### <a name="method-printerrunon"></a><span data-ttu-id="d033e-928">メソッド printerRunOn</span><span class="sxs-lookup"><span data-stu-id="d033e-928">Method printerRunOn</span></span>

    public ClassRunMode printerRunOn()

#### <a name="return-value"></a><span data-ttu-id="d033e-929">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-929">Return Value</span></span>

### <a name="method-printersepfile"></a><span data-ttu-id="d033e-930">メソッド printerSepFile</span><span class="sxs-lookup"><span data-stu-id="d033e-930">Method printerSepFile</span></span>

    public str printerSepFile()

#### <a name="return-value"></a><span data-ttu-id="d033e-931">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-931">Return Value</span></span>

### <a name="method-printerservername"></a><span data-ttu-id="d033e-932">メソッド printerServerName</span><span class="sxs-lookup"><span data-stu-id="d033e-932">Method printerServerName</span></span>

    public str printerServerName()

#### <a name="return-value"></a><span data-ttu-id="d033e-933">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-933">Return Value</span></span>

### <a name="method-printersettings"></a><span data-ttu-id="d033e-934">メソッド printerSettings</span><span class="sxs-lookup"><span data-stu-id="d033e-934">Method printerSettings</span></span>

    public boolean printerSettings(str formName, [xArgs args], [ReportRun reportRun], [int showWhat])

#### <a name="parameters"></a><span data-ttu-id="d033e-935">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-935">Parameters</span></span>

<span data-ttu-id="d033e-936">formName</span><span class="sxs-lookup"><span data-stu-id="d033e-936">formName</span></span>  

<!-- -->

<span data-ttu-id="d033e-937">args</span><span class="sxs-lookup"><span data-stu-id="d033e-937">args</span></span>  

<!-- -->

<span data-ttu-id="d033e-938">reportRun</span><span class="sxs-lookup"><span data-stu-id="d033e-938">reportRun</span></span>  

<!-- -->

<span data-ttu-id="d033e-939">showWhat</span><span class="sxs-lookup"><span data-stu-id="d033e-939">showWhat</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-940">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-940">Return Value</span></span>

### <a name="method-printersharename"></a><span data-ttu-id="d033e-941">メソッド printerShareName</span><span class="sxs-lookup"><span data-stu-id="d033e-941">Method printerShareName</span></span>

    public str printerShareName()

#### <a name="return-value"></a><span data-ttu-id="d033e-942">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-942">Return Value</span></span>

### <a name="method-printerstarttime"></a><span data-ttu-id="d033e-943">メソッド printerStartTime</span><span class="sxs-lookup"><span data-stu-id="d033e-943">Method printerStartTime</span></span>

    public TimeOfDay printerStartTime()

#### <a name="return-value"></a><span data-ttu-id="d033e-944">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-944">Return Value</span></span>

### <a name="method-printerstatus"></a><span data-ttu-id="d033e-945">メソッド printerStatus</span><span class="sxs-lookup"><span data-stu-id="d033e-945">Method printerStatus</span></span>

    public int printerStatus()

#### <a name="return-value"></a><span data-ttu-id="d033e-946">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-946">Return Value</span></span>

### <a name="method-printeruntiltime"></a><span data-ttu-id="d033e-947">メソッド printerUntilTime</span><span class="sxs-lookup"><span data-stu-id="d033e-947">Method printerUntilTime</span></span>

    public TimeOfDay printerUntilTime()

#### <a name="return-value"></a><span data-ttu-id="d033e-948">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-948">Return Value</span></span>

### <a name="method-reportrun"></a><span data-ttu-id="d033e-949">メソッド reportRun</span><span class="sxs-lookup"><span data-stu-id="d033e-949">Method reportRun</span></span>

    public ReportRun reportRun()

#### <a name="return-value"></a><span data-ttu-id="d033e-950">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-950">Return Value</span></span>

### <a name="method-requesteddevicename"></a><span data-ttu-id="d033e-951">メソッド requestedDeviceName</span><span class="sxs-lookup"><span data-stu-id="d033e-951">Method requestedDeviceName</span></span>

    public str requestedDeviceName()

#### <a name="return-value"></a><span data-ttu-id="d033e-952">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-952">Return Value</span></span>

### <a name="method-requestedrunon"></a><span data-ttu-id="d033e-953">メソッド requestedRunOn</span><span class="sxs-lookup"><span data-stu-id="d033e-953">Method requestedRunOn</span></span>

    public ClassRunMode requestedRunOn()

#### <a name="return-value"></a><span data-ttu-id="d033e-954">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-954">Return Value</span></span>

### <a name="method-runclient"></a><span data-ttu-id="d033e-955">メソッド runClient</span><span class="sxs-lookup"><span data-stu-id="d033e-955">Method runClient</span></span>

    public boolean runClient()

#### <a name="return-value"></a><span data-ttu-id="d033e-956">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-956">Return Value</span></span>

### <a name="method-runserver"></a><span data-ttu-id="d033e-957">メソッド runServer</span><span class="sxs-lookup"><span data-stu-id="d033e-957">Method runServer</span></span>

    public boolean runServer()

#### <a name="return-value"></a><span data-ttu-id="d033e-958">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-958">Return Value</span></span>

### <a name="method-sectionsperpage"></a><span data-ttu-id="d033e-959">メソッド sectionsPerPage</span><span class="sxs-lookup"><span data-stu-id="d033e-959">Method sectionsPerPage</span></span>

    public int sectionsPerPage([int sectionsPerPage])

#### <a name="parameters"></a><span data-ttu-id="d033e-960">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-960">Parameters</span></span>

<span data-ttu-id="d033e-961">sectionsPerPage</span><span class="sxs-lookup"><span data-stu-id="d033e-961">sectionsPerPage</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-962">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-962">Return Value</span></span>

### <a name="method-settarget"></a><span data-ttu-id="d033e-963">メソッド setTarget</span><span class="sxs-lookup"><span data-stu-id="d033e-963">Method setTarget</span></span>

<span data-ttu-id="d033e-964">印刷メディアを設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-964">Sets the print medium.</span></span>

    public PrintMedium setTarget(PrintMedium target)

#### <a name="parameters"></a><span data-ttu-id="d033e-965">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-965">Parameters</span></span>

<span data-ttu-id="d033e-966">target</span><span class="sxs-lookup"><span data-stu-id="d033e-966">target</span></span>  
<span data-ttu-id="d033e-967">印刷メディア。</span><span class="sxs-lookup"><span data-stu-id="d033e-967">The print medium.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d033e-968">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-968">Return Value</span></span>

<span data-ttu-id="d033e-969">印刷メディア。</span><span class="sxs-lookup"><span data-stu-id="d033e-969">The print medium.</span></span>

### <a name="method-singlelargepage"></a><span data-ttu-id="d033e-970">メソッド singleLargePage</span><span class="sxs-lookup"><span data-stu-id="d033e-970">Method singleLargePage</span></span>

    public boolean singleLargePage([boolean singleLargePage])

#### <a name="parameters"></a><span data-ttu-id="d033e-971">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-971">Parameters</span></span>

<span data-ttu-id="d033e-972">singleLargePage</span><span class="sxs-lookup"><span data-stu-id="d033e-972">singleLargePage</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-973">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-973">Return Value</span></span>

### <a name="method-skipbitmapsinrtf"></a><span data-ttu-id="d033e-974">メソッド skipBitmapsInRTF</span><span class="sxs-lookup"><span data-stu-id="d033e-974">Method skipBitmapsInRTF</span></span>

<span data-ttu-id="d033e-975">.rtf ファイルにレポートを印刷するときにビットマップを含めるかどうかをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="d033e-975">Controls whether bitmaps are included when reports are printed to an .rtf file.</span></span>

    public boolean skipBitmapsInRTF([boolean skipBitmaps])

#### <a name="parameters"></a><span data-ttu-id="d033e-976">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-976">Parameters</span></span>

<span data-ttu-id="d033e-977">skipBitmaps</span><span class="sxs-lookup"><span data-stu-id="d033e-977">skipBitmaps</span></span>  
<span data-ttu-id="d033e-978">ビットマップが含まれるかどうかを判断するブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="d033e-978">A boolean flag that determines whether bitmaps are included; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d033e-979">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-979">Return Value</span></span>

<span data-ttu-id="d033e-980">ビットマップが含まれる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d033e-980">true if the bitmaps are included; otherwise, false.</span></span>

### <a name="method-storeinprintarchive"></a><span data-ttu-id="d033e-981">メソッド storeInPrintArchive</span><span class="sxs-lookup"><span data-stu-id="d033e-981">Method storeInPrintArchive</span></span>

    public boolean storeInPrintArchive([boolean store])

#### <a name="parameters"></a><span data-ttu-id="d033e-982">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-982">Parameters</span></span>

<span data-ttu-id="d033e-983">店舗</span><span class="sxs-lookup"><span data-stu-id="d033e-983">store</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-984">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-984">Return Value</span></span>

### <a name="method-suppressscalingmessage"></a><span data-ttu-id="d033e-985">メソッド suppressScalingMessage</span><span class="sxs-lookup"><span data-stu-id="d033e-985">Method suppressScalingMessage</span></span>

    public boolean suppressScalingMessage([boolean suppress])

#### <a name="parameters"></a><span data-ttu-id="d033e-986">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-986">Parameters</span></span>

<span data-ttu-id="d033e-987">suppress</span><span class="sxs-lookup"><span data-stu-id="d033e-987">suppress</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-988">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-988">Return Value</span></span>

### <a name="method-to"></a><span data-ttu-id="d033e-989">メソッド to</span><span class="sxs-lookup"><span data-stu-id="d033e-989">Method to</span></span>

    public int to([int toPage])

#### <a name="parameters"></a><span data-ttu-id="d033e-990">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-990">Parameters</span></span>

<span data-ttu-id="d033e-991">toPage</span><span class="sxs-lookup"><span data-stu-id="d033e-991">toPage</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-992">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-992">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="d033e-993">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="d033e-993">Method toString</span></span>

<span data-ttu-id="d033e-994">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-994">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="d033e-995">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-995">Return Value</span></span>

<span data-ttu-id="d033e-996">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d033e-996">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-997">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-997">Remarks</span></span>

<span data-ttu-id="d033e-998">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-998">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="d033e-999">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d033e-999">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="d033e-1000">たとえば、クラスのインスタンスは、インスタンスまたは静的などの、メソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1000">For example, an instance of the class returns the method name and type of the method, such as instance or static.</span></span>

### <a name="method-unpackpagesettings"></a><span data-ttu-id="d033e-1001">メソッド unpackPageSettings</span><span class="sxs-lookup"><span data-stu-id="d033e-1001">Method unpackPageSettings</span></span>

<span data-ttu-id="d033e-1002">用紙サイズと向きなど、ページ設定を設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1002">Sets the page settings, such as paper size and orientation.</span></span>

    public boolean unpackPageSettings(container settings)

#### <a name="parameters"></a><span data-ttu-id="d033e-1003">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1003">Parameters</span></span>

<span data-ttu-id="d033e-1004">設定</span><span class="sxs-lookup"><span data-stu-id="d033e-1004">settings</span></span>  
<span data-ttu-id="d033e-1005">packPageSettings メソッドを呼び出して取得されるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="d033e-1005">A container that is obtained by calling the packPageSettings method.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d033e-1006">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1006">Return Value</span></span>

<span data-ttu-id="d033e-1007">pageSettings が正常に変更された場合は true。pageSettings が既定値に設定された場合は false。</span><span class="sxs-lookup"><span data-stu-id="d033e-1007">true if the pageSettings were successfully changed; false if the pageSettings were set to the default values.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-1008">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1008">Remarks</span></span>

<span data-ttu-id="d033e-1009">reportDesign クラスと report クラスには、同じ名前のメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="d033e-1009">The classes reportDesign and report have a method with the same name.</span></span>

### <a name="method-unpackprintersettings"></a><span data-ttu-id="d033e-1010">メソッド unpackPrinterSettings</span><span class="sxs-lookup"><span data-stu-id="d033e-1010">Method unpackPrinterSettings</span></span>

    public boolean unpackPrinterSettings(container settings)

#### <a name="parameters"></a><span data-ttu-id="d033e-1011">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1011">Parameters</span></span>

<span data-ttu-id="d033e-1012">設定</span><span class="sxs-lookup"><span data-stu-id="d033e-1012">settings</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1013">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1013">Return Value</span></span>

### <a name="method-unpackprintjobsettings"></a><span data-ttu-id="d033e-1014">メソッド unpackPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="d033e-1014">Method unpackPrintJobSettings</span></span>

    public boolean unpackPrintJobSettings(container settings)

#### <a name="parameters"></a><span data-ttu-id="d033e-1015">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1015">Parameters</span></span>

<span data-ttu-id="d033e-1016">設定</span><span class="sxs-lookup"><span data-stu-id="d033e-1016">settings</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1017">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1017">Return Value</span></span>

### <a name="method-unpacksubtotalsettings"></a><span data-ttu-id="d033e-1018">メソッド unpackSubtotalSettings</span><span class="sxs-lookup"><span data-stu-id="d033e-1018">Method unpackSubtotalSettings</span></span>

    public boolean unpackSubtotalSettings(container settings)

#### <a name="parameters"></a><span data-ttu-id="d033e-1019">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1019">Parameters</span></span>

<span data-ttu-id="d033e-1020">設定</span><span class="sxs-lookup"><span data-stu-id="d033e-1020">settings</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1021">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1021">Return Value</span></span>

### <a name="method-unprintablebottom"></a><span data-ttu-id="d033e-1022">メソッド unprintableBottom</span><span class="sxs-lookup"><span data-stu-id="d033e-1022">Method unprintableBottom</span></span>

    public int unprintableBottom()

#### <a name="return-value"></a><span data-ttu-id="d033e-1023">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1023">Return Value</span></span>

### <a name="method-unprintableleft"></a><span data-ttu-id="d033e-1024">メソッド unprintableLeft</span><span class="sxs-lookup"><span data-stu-id="d033e-1024">Method unprintableLeft</span></span>

    public int unprintableLeft()

#### <a name="return-value"></a><span data-ttu-id="d033e-1025">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1025">Return Value</span></span>

### <a name="method-unprintableright"></a><span data-ttu-id="d033e-1026">メソッド unprintableRight</span><span class="sxs-lookup"><span data-stu-id="d033e-1026">Method unprintableRight</span></span>

    public int unprintableRight()

#### <a name="return-value"></a><span data-ttu-id="d033e-1027">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1027">Return Value</span></span>

### <a name="method-unprintabletop"></a><span data-ttu-id="d033e-1028">メソッド unprintableTop</span><span class="sxs-lookup"><span data-stu-id="d033e-1028">Method unprintableTop</span></span>

<span data-ttu-id="d033e-1029">用紙の最上部から用紙の印刷可能な範囲までの距離を示します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1029">Indicates the distance from the top of the paper to the printable area of the paper.</span></span>

    public int unprintableTop()

#### <a name="return-value"></a><span data-ttu-id="d033e-1030">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1030">Return Value</span></span>

<span data-ttu-id="d033e-1031">印刷できない領域のサイズ。単位は 100 分の 1 ミリメートルです。</span><span class="sxs-lookup"><span data-stu-id="d033e-1031">The size of nonprintable area, measured in hundredths of a millimeter.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-1032">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1032">Remarks</span></span>

<span data-ttu-id="d033e-1033">レポートでは、reportDesign の topMargin を unprintableTop よりも小さくしてはなりません。</span><span class="sxs-lookup"><span data-stu-id="d033e-1033">In reports, the topMargin of a reportDesign must not be less than unprintableTop.</span></span>

#### <a name="examples"></a><span data-ttu-id="d033e-1034">例</span><span class="sxs-lookup"><span data-stu-id="d033e-1034">Examples</span></span>

    static void printerInfo(args a) 
    { 
        printJobSettings pjs; 
        str printer; 
        int i; 
        pjs = new printJobSettings(); 
        for (i=1; i<=pjs.GetNumberOfPrinters(); i++) 
        { 
            printer = pjs.GetPrinter(i); 
            pjs.DeviceName(printer); 
            print "printer No. ",i, " has name ",  printer; 
            print "   left:   ", pjs.UnprintableLeft(),   "/100 mm"; 
            print "   right:  ", pjs.UnprintableRight(),  "/100 mm"; 
            print "   totalWidth: ", pjs.UnprintableLeft() +  
                pjs.PrinterPageWidth() + pjs.UnprintableRight(); 
            print "   top:    ", pjs.UnprintableTop(),    "/100 mm"; 
            print "   bottom: ", pjs.UnprintableBottom(), "/100 mm"; 
            print "   totalHeight: ", pjs.UnprintableTop() +  
                pjs.PrinterPageHeight() + pjs.UnprintableBottom(); 
        } 
        pause; 
    }

### <a name="method-viewertype"></a><span data-ttu-id="d033e-1035">メソッド viewerType</span><span class="sxs-lookup"><span data-stu-id="d033e-1035">Method viewerType</span></span>

    public ReportOutputUserType viewerType([ReportOutputUserType type])

#### <a name="parameters"></a><span data-ttu-id="d033e-1036">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1036">Parameters</span></span>

<span data-ttu-id="d033e-1037">タイプ</span><span class="sxs-lookup"><span data-stu-id="d033e-1037">type</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1038">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1038">Return Value</span></span>

### <a name="method-virtualpageheight"></a><span data-ttu-id="d033e-1039">メソッド virtualPageHeight</span><span class="sxs-lookup"><span data-stu-id="d033e-1039">Method virtualPageHeight</span></span>

    public int virtualPageHeight([int height])

#### <a name="parameters"></a><span data-ttu-id="d033e-1040">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1040">Parameters</span></span>

<span data-ttu-id="d033e-1041">height</span><span class="sxs-lookup"><span data-stu-id="d033e-1041">height</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1042">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1042">Return Value</span></span>

### <a name="method-warniffileexists"></a><span data-ttu-id="d033e-1043">メソッド warnIfFileExists</span><span class="sxs-lookup"><span data-stu-id="d033e-1043">Method warnIfFileExists</span></span>

    public boolean warnIfFileExists([boolean warn])

#### <a name="parameters"></a><span data-ttu-id="d033e-1044">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1044">Parameters</span></span>

<span data-ttu-id="d033e-1045">警告</span><span class="sxs-lookup"><span data-stu-id="d033e-1045">warn</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1046">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1046">Return Value</span></span>

### <a name="method-enablebody"></a><span data-ttu-id="d033e-1047">メソッド enableBody</span><span class="sxs-lookup"><span data-stu-id="d033e-1047">Method enableBody</span></span>

    public void enableBody([TableId tableId])

#### <a name="parameters"></a><span data-ttu-id="d033e-1048">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1048">Parameters</span></span>

<span data-ttu-id="d033e-1049">tableId</span><span class="sxs-lookup"><span data-stu-id="d033e-1049">tableId</span></span>  

### <a name="method-new"></a><span data-ttu-id="d033e-1050">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d033e-1050">Method new</span></span>

<span data-ttu-id="d033e-1051">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1051">Initializes a new instance of the Object class.</span></span>

    public void new([container Settings], [boolean infoOnly])

#### <a name="parameters"></a><span data-ttu-id="d033e-1052">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1052">Parameters</span></span>

<span data-ttu-id="d033e-1053">設定</span><span class="sxs-lookup"><span data-stu-id="d033e-1053">Settings</span></span>  

<!-- -->

<span data-ttu-id="d033e-1054">infoOnly</span><span class="sxs-lookup"><span data-stu-id="d033e-1054">infoOnly</span></span>  

### <a name="method-addtraypagecopy"></a><span data-ttu-id="d033e-1055">メソッド addTrayPageCopy</span><span class="sxs-lookup"><span data-stu-id="d033e-1055">Method addTrayPageCopy</span></span>

    public void addTrayPageCopy(int tray, int pageNumber, [int copyNumber])

#### <a name="parameters"></a><span data-ttu-id="d033e-1056">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1056">Parameters</span></span>

<span data-ttu-id="d033e-1057">トレイ</span><span class="sxs-lookup"><span data-stu-id="d033e-1057">tray</span></span>  

<!-- -->

<span data-ttu-id="d033e-1058">pageNumber</span><span class="sxs-lookup"><span data-stu-id="d033e-1058">pageNumber</span></span>  

<!-- -->

<span data-ttu-id="d033e-1059">copyNumber</span><span class="sxs-lookup"><span data-stu-id="d033e-1059">copyNumber</span></span>  

### <a name="method-disablebody"></a><span data-ttu-id="d033e-1060">メソッド disableBody</span><span class="sxs-lookup"><span data-stu-id="d033e-1060">Method disableBody</span></span>

    public void disableBody([TableId tableId])

#### <a name="parameters"></a><span data-ttu-id="d033e-1061">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1061">Parameters</span></span>

<span data-ttu-id="d033e-1062">tableId</span><span class="sxs-lookup"><span data-stu-id="d033e-1062">tableId</span></span>  

### <a name="method-cleartraypagecopy"></a><span data-ttu-id="d033e-1063">メソッド clearTrayPageCopy</span><span class="sxs-lookup"><span data-stu-id="d033e-1063">Method clearTrayPageCopy</span></span>

    public void clearTrayPageCopy()

### <a name="method-rulerinch"></a><span data-ttu-id="d033e-1064">メソッド rulerInch</span><span class="sxs-lookup"><span data-stu-id="d033e-1064">Method rulerInch</span></span>

    public void rulerInch()

### <a name="method-finalize"></a><span data-ttu-id="d033e-1065">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="d033e-1065">Method finalize</span></span>

    public void finalize()

### <a name="method-ruleroff"></a><span data-ttu-id="d033e-1066">メソッド rulerOff</span><span class="sxs-lookup"><span data-stu-id="d033e-1066">Method rulerOff</span></span>

    public void rulerOff()

### <a name="method-rulermetric"></a><span data-ttu-id="d033e-1067">メソッド rulerMetric</span><span class="sxs-lookup"><span data-stu-id="d033e-1067">Method rulerMetric</span></span>

    public void rulerMetric()

## <a name="class-profiler"></a><span data-ttu-id="d033e-1068">クラス プロファイラー</span><span class="sxs-lookup"><span data-stu-id="d033e-1068">Class profiler</span></span>
    class profiler extends Object

### <a name="remarks"></a><span data-ttu-id="d033e-1069">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1069">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d033e-1070">例</span><span class="sxs-lookup"><span data-stu-id="d033e-1070">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d033e-1071">メソッド</span><span class="sxs-lookup"><span data-stu-id="d033e-1071">Methods</span></span>

| <span data-ttu-id="d033e-1072">方法</span><span class="sxs-lookup"><span data-stu-id="d033e-1072">Method</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="d033e-1073">説明</span><span class="sxs-lookup"><span data-stu-id="d033e-1073">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d033e-1074">public int collected()</span><span class="sxs-lookup"><span data-stu-id="d033e-1074">public int collected()</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |                                                      |
| <span data-ttu-id="d033e-1075">public int flushInterval(\[int interval\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1075">public int flushInterval(\[int interval\])</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                      |                                                      |
| <span data-ttu-id="d033e-1076">public AnyType profileOff()</span><span class="sxs-lookup"><span data-stu-id="d033e-1076">public AnyType profileOff()</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |                                                      |
| <span data-ttu-id="d033e-1077">public AnyType profileOn(str runId, \[int traceDepth\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1077">public AnyType profileOn(str runId, \[int traceDepth\])</span></span>                                                                                                                                                                                                                                                                                                                                                                                                         |                                                      |
| <span data-ttu-id="d033e-1078">public str tempPath()</span><span class="sxs-lookup"><span data-stu-id="d033e-1078">public str tempPath()</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |                                                      |
| <span data-ttu-id="d033e-1079">public str toString()</span><span class="sxs-lookup"><span data-stu-id="d033e-1079">public str toString()</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="d033e-1080">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1080">Returns a string that represents the current object.</span></span> |
| <span data-ttu-id="d033e-1081">::public static AnyType profilerAlreadyOn()</span><span class="sxs-lookup"><span data-stu-id="d033e-1081">::public static AnyType profilerAlreadyOn()</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |                                                      |
| <span data-ttu-id="d033e-1082">public void flush()</span><span class="sxs-lookup"><span data-stu-id="d033e-1082">public void flush()</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                      |
| <span data-ttu-id="d033e-1083">public void new()</span><span class="sxs-lookup"><span data-stu-id="d033e-1083">public void new()</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="d033e-1084">profiler クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1084">Initializes a new instance of the profiler class.</span></span>    |
| <span data-ttu-id="d033e-1085">public void flushData(int lineNumber, str path, int microSecs, int sequenceNumber, int parentSequenceNumber, int selectCalls, int selectBytes, int selectRows, int sqlWaitTime, int aosWaitTime, int sqlInserts, int sqlUpdates, int sqlDeletes, int aosInCalls, int aosOutCalls, int aosInBytes, int aosOutBytes, \[int sqlInsertBytes\], \[int sqlInsertRows\], \[int sqlUpdateBytes\], \[int sqlUpdateRows\], \[int sqlDeleteBytes\], \[int sqlDeleteRows\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1085">public void flushData(int lineNumber, str path, int microSecs, int sequenceNumber, int parentSequenceNumber, int selectCalls, int selectBytes, int selectRows, int sqlWaitTime, int aosWaitTime, int sqlInserts, int sqlUpdates, int sqlDeletes, int aosInCalls, int aosOutCalls, int aosInBytes, int aosOutBytes, \[int sqlInsertBytes\], \[int sqlInsertRows\], \[int sqlUpdateBytes\], \[int sqlUpdateRows\], \[int sqlDeleteBytes\], \[int sqlDeleteRows\])</span></span> |                                                      |

### <a name="method-collected"></a><span data-ttu-id="d033e-1086">メソッド collected</span><span class="sxs-lookup"><span data-stu-id="d033e-1086">Method collected</span></span>

    public int collected()

#### <a name="return-value"></a><span data-ttu-id="d033e-1087">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1087">Return Value</span></span>

### <a name="method-flushinterval"></a><span data-ttu-id="d033e-1088">メソッド flushInterval</span><span class="sxs-lookup"><span data-stu-id="d033e-1088">Method flushInterval</span></span>

    public int flushInterval([int interval])

#### <a name="parameters"></a><span data-ttu-id="d033e-1089">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1089">Parameters</span></span>

<span data-ttu-id="d033e-1090">interval</span><span class="sxs-lookup"><span data-stu-id="d033e-1090">interval</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1091">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1091">Return Value</span></span>

### <a name="method-profileoff"></a><span data-ttu-id="d033e-1092">メソッド profileOff</span><span class="sxs-lookup"><span data-stu-id="d033e-1092">Method profileOff</span></span>

    public AnyType profileOff()

#### <a name="return-value"></a><span data-ttu-id="d033e-1093">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1093">Return Value</span></span>

### <a name="method-profileon"></a><span data-ttu-id="d033e-1094">メソッド profileOn</span><span class="sxs-lookup"><span data-stu-id="d033e-1094">Method profileOn</span></span>

    public AnyType profileOn(str runId, [int traceDepth])

#### <a name="parameters"></a><span data-ttu-id="d033e-1095">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1095">Parameters</span></span>

<span data-ttu-id="d033e-1096">runId</span><span class="sxs-lookup"><span data-stu-id="d033e-1096">runId</span></span>  

<!-- -->

<span data-ttu-id="d033e-1097">traceDepth</span><span class="sxs-lookup"><span data-stu-id="d033e-1097">traceDepth</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1098">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1098">Return Value</span></span>

### <a name="method-temppath"></a><span data-ttu-id="d033e-1099">メソッド tempPath</span><span class="sxs-lookup"><span data-stu-id="d033e-1099">Method tempPath</span></span>

    public str tempPath()

#### <a name="return-value"></a><span data-ttu-id="d033e-1100">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1100">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="d033e-1101">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="d033e-1101">Method toString</span></span>

<span data-ttu-id="d033e-1102">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1102">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="d033e-1103">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1103">Return Value</span></span>

<span data-ttu-id="d033e-1104">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d033e-1104">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-1105">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1105">Remarks</span></span>

<span data-ttu-id="d033e-1106">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1106">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="d033e-1107">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1107">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="d033e-1108">たとえば、クラスのインスタンスは、インスタンスまたは静的などの、メソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1108">For example, an instance of the class returns the method name and type of the method, such as instance or static.</span></span>

### <a name="method-profileralreadyon"></a><span data-ttu-id="d033e-1109">メソッド profilerAlreadyOn</span><span class="sxs-lookup"><span data-stu-id="d033e-1109">Method profilerAlreadyOn</span></span>

    public static AnyType profilerAlreadyOn()

#### <a name="return-value"></a><span data-ttu-id="d033e-1110">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1110">Return Value</span></span>

### <a name="method-flush"></a><span data-ttu-id="d033e-1111">メソッド flush</span><span class="sxs-lookup"><span data-stu-id="d033e-1111">Method flush</span></span>

    public void flush()

### <a name="method-new"></a><span data-ttu-id="d033e-1112">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d033e-1112">Method new</span></span>

<span data-ttu-id="d033e-1113">profiler クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1113">Initializes a new instance of the profiler class.</span></span>

    public void new()

### <a name="method-flushdata"></a><span data-ttu-id="d033e-1114">メソッド flushData</span><span class="sxs-lookup"><span data-stu-id="d033e-1114">Method flushData</span></span>

    public void flushData(int lineNumber, str path, int microSecs, int sequenceNumber, int parentSequenceNumber, int selectCalls, int selectBytes, int selectRows, int sqlWaitTime, int aosWaitTime, int sqlInserts, int sqlUpdates, int sqlDeletes, int aosInCalls, int aosOutCalls, int aosInBytes, int aosOutBytes, [int sqlInsertBytes], [int sqlInsertRows], [int sqlUpdateBytes], [int sqlUpdateRows], [int sqlDeleteBytes], [int sqlDeleteRows])

#### <a name="parameters"></a><span data-ttu-id="d033e-1115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1115">Parameters</span></span>

<span data-ttu-id="d033e-1116">lineNumber</span><span class="sxs-lookup"><span data-stu-id="d033e-1116">lineNumber</span></span>  

<!-- -->

<span data-ttu-id="d033e-1117">path</span><span class="sxs-lookup"><span data-stu-id="d033e-1117">path</span></span>  

<!-- -->

<span data-ttu-id="d033e-1118">microSecs</span><span class="sxs-lookup"><span data-stu-id="d033e-1118">microSecs</span></span>  

<!-- -->

<span data-ttu-id="d033e-1119">sequenceNumber</span><span class="sxs-lookup"><span data-stu-id="d033e-1119">sequenceNumber</span></span>  

<!-- -->

<span data-ttu-id="d033e-1120">parentSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="d033e-1120">parentSequenceNumber</span></span>  

<!-- -->

<span data-ttu-id="d033e-1121">selectCalls</span><span class="sxs-lookup"><span data-stu-id="d033e-1121">selectCalls</span></span>  

<!-- -->

<span data-ttu-id="d033e-1122">selectBytes</span><span class="sxs-lookup"><span data-stu-id="d033e-1122">selectBytes</span></span>  

<!-- -->

<span data-ttu-id="d033e-1123">selectRows</span><span class="sxs-lookup"><span data-stu-id="d033e-1123">selectRows</span></span>  

<!-- -->

<span data-ttu-id="d033e-1124">sqlWaitTime</span><span class="sxs-lookup"><span data-stu-id="d033e-1124">sqlWaitTime</span></span>  

<!-- -->

<span data-ttu-id="d033e-1125">aosWaitTime</span><span class="sxs-lookup"><span data-stu-id="d033e-1125">aosWaitTime</span></span>  

<!-- -->

<span data-ttu-id="d033e-1126">sqlInserts</span><span class="sxs-lookup"><span data-stu-id="d033e-1126">sqlInserts</span></span>  

<!-- -->

<span data-ttu-id="d033e-1127">sqlUpdates</span><span class="sxs-lookup"><span data-stu-id="d033e-1127">sqlUpdates</span></span>  

<!-- -->

<span data-ttu-id="d033e-1128">sqlDeletes</span><span class="sxs-lookup"><span data-stu-id="d033e-1128">sqlDeletes</span></span>  

<!-- -->

<span data-ttu-id="d033e-1129">aosInCalls</span><span class="sxs-lookup"><span data-stu-id="d033e-1129">aosInCalls</span></span>  

<!-- -->

<span data-ttu-id="d033e-1130">aosOutCalls</span><span class="sxs-lookup"><span data-stu-id="d033e-1130">aosOutCalls</span></span>  

<!-- -->

<span data-ttu-id="d033e-1131">aosInBytes</span><span class="sxs-lookup"><span data-stu-id="d033e-1131">aosInBytes</span></span>  

<!-- -->

<span data-ttu-id="d033e-1132">aosOutBytes</span><span class="sxs-lookup"><span data-stu-id="d033e-1132">aosOutBytes</span></span>  

<!-- -->

<span data-ttu-id="d033e-1133">sqlInsertBytes</span><span class="sxs-lookup"><span data-stu-id="d033e-1133">sqlInsertBytes</span></span>  

<!-- -->

<span data-ttu-id="d033e-1134">sqlInsertRows</span><span class="sxs-lookup"><span data-stu-id="d033e-1134">sqlInsertRows</span></span>  

<!-- -->

<span data-ttu-id="d033e-1135">sqlUpdateBytes</span><span class="sxs-lookup"><span data-stu-id="d033e-1135">sqlUpdateBytes</span></span>  

<!-- -->

<span data-ttu-id="d033e-1136">sqlUpdateRows</span><span class="sxs-lookup"><span data-stu-id="d033e-1136">sqlUpdateRows</span></span>  

<!-- -->

<span data-ttu-id="d033e-1137">sqlDeleteBytes</span><span class="sxs-lookup"><span data-stu-id="d033e-1137">sqlDeleteBytes</span></span>  

<!-- -->

<span data-ttu-id="d033e-1138">sqlDeleteRows</span><span class="sxs-lookup"><span data-stu-id="d033e-1138">sqlDeleteRows</span></span>  

## <a name="class-progresswindow"></a><span data-ttu-id="d033e-1139">クラス ProgressWindow</span><span class="sxs-lookup"><span data-stu-id="d033e-1139">Class ProgressWindow</span></span>
    class ProgressWindow extends Object

### <a name="remarks"></a><span data-ttu-id="d033e-1140">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1140">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d033e-1141">例</span><span class="sxs-lookup"><span data-stu-id="d033e-1141">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d033e-1142">メソッド</span><span class="sxs-lookup"><span data-stu-id="d033e-1142">Methods</span></span>

| <span data-ttu-id="d033e-1143">方法</span><span class="sxs-lookup"><span data-stu-id="d033e-1143">Method</span></span>                                                      | <span data-ttu-id="d033e-1144">説明</span><span class="sxs-lookup"><span data-stu-id="d033e-1144">Description</span></span>                                             |
|-------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d033e-1145">public int addProgressControl(\[int progressControlCount\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1145">public int addProgressControl(\[int progressControlCount\])</span></span> |                                                         |
| <span data-ttu-id="d033e-1146">public void ProgressBarVisible(int index, int visible)</span><span class="sxs-lookup"><span data-stu-id="d033e-1146">public void ProgressBarVisible(int index, int visible)</span></span>      |                                                         |
| <span data-ttu-id="d033e-1147">public void ProgressValue(int index, int progressValue)</span><span class="sxs-lookup"><span data-stu-id="d033e-1147">public void ProgressValue(int index, int progressValue)</span></span>     |                                                         |
| <span data-ttu-id="d033e-1148">public void ControlMinMax(int index, int min, int max)</span><span class="sxs-lookup"><span data-stu-id="d033e-1148">public void ControlMinMax(int index, int min, int max)</span></span>      |                                                         |
| <span data-ttu-id="d033e-1149">public void ProgressTextVisible(int index, int visible)</span><span class="sxs-lookup"><span data-stu-id="d033e-1149">public void ProgressTextVisible(int index, int visible)</span></span>     |                                                         |
| <span data-ttu-id="d033e-1150">public void Animation(str animation)</span><span class="sxs-lookup"><span data-stu-id="d033e-1150">public void Animation(str animation)</span></span>                        |                                                         |
| <span data-ttu-id="d033e-1151">public void ControlText(int index, str text)</span><span class="sxs-lookup"><span data-stu-id="d033e-1151">public void ControlText(int index, str text)</span></span>                |                                                         |
| <span data-ttu-id="d033e-1152">public void FormCaption(str text)</span><span class="sxs-lookup"><span data-stu-id="d033e-1152">public void FormCaption(str text)</span></span>                           |                                                         |
| <span data-ttu-id="d033e-1153">public void ControlTime(str text)</span><span class="sxs-lookup"><span data-stu-id="d033e-1153">public void ControlTime(str text)</span></span>                           |                                                         |
| <span data-ttu-id="d033e-1154">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="d033e-1154">public void finalize()</span></span>                                      |                                                         |
| <span data-ttu-id="d033e-1155">public void new()</span><span class="sxs-lookup"><span data-stu-id="d033e-1155">public void new()</span></span>                                           | <span data-ttu-id="d033e-1156">ProgressWindow クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1156">Initializes a new instance of the ProgressWindow class.</span></span> |

### <a name="method-addprogresscontrol"></a><span data-ttu-id="d033e-1157">メソッド addProgressControl</span><span class="sxs-lookup"><span data-stu-id="d033e-1157">Method addProgressControl</span></span>

    public int addProgressControl([int progressControlCount])

#### <a name="parameters"></a><span data-ttu-id="d033e-1158">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1158">Parameters</span></span>

<span data-ttu-id="d033e-1159">progressControlCount</span><span class="sxs-lookup"><span data-stu-id="d033e-1159">progressControlCount</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1160">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1160">Return Value</span></span>

### <a name="method-progressbarvisible"></a><span data-ttu-id="d033e-1161">メソッド ProgressBarVisible</span><span class="sxs-lookup"><span data-stu-id="d033e-1161">Method ProgressBarVisible</span></span>

    public void ProgressBarVisible(int index, int visible)

#### <a name="parameters"></a><span data-ttu-id="d033e-1162">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1162">Parameters</span></span>

<span data-ttu-id="d033e-1163">指数</span><span class="sxs-lookup"><span data-stu-id="d033e-1163">index</span></span>  

<!-- -->

<span data-ttu-id="d033e-1164">表示</span><span class="sxs-lookup"><span data-stu-id="d033e-1164">visible</span></span>  

### <a name="method-progressvalue"></a><span data-ttu-id="d033e-1165">メソッド ProgressValue</span><span class="sxs-lookup"><span data-stu-id="d033e-1165">Method ProgressValue</span></span>

    public void ProgressValue(int index, int progressValue)

#### <a name="parameters"></a><span data-ttu-id="d033e-1166">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1166">Parameters</span></span>

<span data-ttu-id="d033e-1167">指数</span><span class="sxs-lookup"><span data-stu-id="d033e-1167">index</span></span>  

<!-- -->

<span data-ttu-id="d033e-1168">progressValue</span><span class="sxs-lookup"><span data-stu-id="d033e-1168">progressValue</span></span>  

### <a name="method-controlminmax"></a><span data-ttu-id="d033e-1169">メソッド ControlMinMax</span><span class="sxs-lookup"><span data-stu-id="d033e-1169">Method ControlMinMax</span></span>

    public void ControlMinMax(int index, int min, int max)

#### <a name="parameters"></a><span data-ttu-id="d033e-1170">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1170">Parameters</span></span>

<span data-ttu-id="d033e-1171">指数</span><span class="sxs-lookup"><span data-stu-id="d033e-1171">index</span></span>  

<!-- -->

<span data-ttu-id="d033e-1172">最小</span><span class="sxs-lookup"><span data-stu-id="d033e-1172">min</span></span>  

<!-- -->

<span data-ttu-id="d033e-1173">最大</span><span class="sxs-lookup"><span data-stu-id="d033e-1173">max</span></span>  

### <a name="method-progresstextvisible"></a><span data-ttu-id="d033e-1174">メソッド ProgressTextVisible</span><span class="sxs-lookup"><span data-stu-id="d033e-1174">Method ProgressTextVisible</span></span>

    public void ProgressTextVisible(int index, int visible)

#### <a name="parameters"></a><span data-ttu-id="d033e-1175">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1175">Parameters</span></span>

<span data-ttu-id="d033e-1176">指数</span><span class="sxs-lookup"><span data-stu-id="d033e-1176">index</span></span>  

<!-- -->

<span data-ttu-id="d033e-1177">表示</span><span class="sxs-lookup"><span data-stu-id="d033e-1177">visible</span></span>  

### <a name="method-animation"></a><span data-ttu-id="d033e-1178">メソッド アニメーション</span><span class="sxs-lookup"><span data-stu-id="d033e-1178">Method Animation</span></span>

    public void Animation(str animation)

#### <a name="parameters"></a><span data-ttu-id="d033e-1179">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1179">Parameters</span></span>

<span data-ttu-id="d033e-1180">animation</span><span class="sxs-lookup"><span data-stu-id="d033e-1180">animation</span></span>  

### <a name="method-controltext"></a><span data-ttu-id="d033e-1181">メソッド ControlText</span><span class="sxs-lookup"><span data-stu-id="d033e-1181">Method ControlText</span></span>

    public void ControlText(int index, str text)

#### <a name="parameters"></a><span data-ttu-id="d033e-1182">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1182">Parameters</span></span>

<span data-ttu-id="d033e-1183">指数</span><span class="sxs-lookup"><span data-stu-id="d033e-1183">index</span></span>  

<!-- -->

<span data-ttu-id="d033e-1184">テキスト</span><span class="sxs-lookup"><span data-stu-id="d033e-1184">text</span></span>  

### <a name="method-formcaption"></a><span data-ttu-id="d033e-1185">メソッド FormCaption</span><span class="sxs-lookup"><span data-stu-id="d033e-1185">Method FormCaption</span></span>

    public void FormCaption(str text)

#### <a name="parameters"></a><span data-ttu-id="d033e-1186">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1186">Parameters</span></span>

<span data-ttu-id="d033e-1187">テキスト</span><span class="sxs-lookup"><span data-stu-id="d033e-1187">text</span></span>  

### <a name="method-controltime"></a><span data-ttu-id="d033e-1188">メソッド ControlTime</span><span class="sxs-lookup"><span data-stu-id="d033e-1188">Method ControlTime</span></span>

    public void ControlTime(str text)

#### <a name="parameters"></a><span data-ttu-id="d033e-1189">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1189">Parameters</span></span>

<span data-ttu-id="d033e-1190">テキスト</span><span class="sxs-lookup"><span data-stu-id="d033e-1190">text</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="d033e-1191">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="d033e-1191">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="d033e-1192">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d033e-1192">Method new</span></span>

<span data-ttu-id="d033e-1193">ProgressWindow クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1193">Initializes a new instance of the ProgressWindow class.</span></span>

    public void new()

## <a name="class-projectgroupnode"></a><span data-ttu-id="d033e-1194">クラス ProjectGroupNode</span><span class="sxs-lookup"><span data-stu-id="d033e-1194">Class ProjectGroupNode</span></span>
    class ProjectGroupNode extends TreeNode

<span data-ttu-id="d033e-1195">ProjectGroupNode クラスは、プロジェクト内のグループ ノードを表します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1195">The ProjectGroupNode class represents a group node within a project.</span></span>

### <a name="remarks"></a><span data-ttu-id="d033e-1196">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1196">Remarks</span></span>

<span data-ttu-id="d033e-1197">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1197">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="d033e-1198">この API を呼び出す前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1198">Make sure that the user has access to the development security key (SysDevelopment) before you call this API.</span></span>

### <a name="examples"></a><span data-ttu-id="d033e-1199">例</span><span class="sxs-lookup"><span data-stu-id="d033e-1199">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d033e-1200">メソッド</span><span class="sxs-lookup"><span data-stu-id="d033e-1200">Methods</span></span>

| <span data-ttu-id="d033e-1201">方法</span><span class="sxs-lookup"><span data-stu-id="d033e-1201">Method</span></span>                                                                                       | <span data-ttu-id="d033e-1202">説明</span><span class="sxs-lookup"><span data-stu-id="d033e-1202">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d033e-1203">public TreeNode findGroupMember(str name, UtilElementType type, \[boolean searchSubgroups\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1203">public TreeNode findGroupMember(str name, UtilElementType type, \[boolean searchSubgroups\])</span></span> | <span data-ttu-id="d033e-1204">特定の要素の projectGroup を検索します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1204">Searches the projectGroup for a specific element.</span></span> <span data-ttu-id="d033e-1205">特定のグループまたはプロジェクト全体を検索するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1205">It can be used to search a specific group or the whole project.</span></span>                             |
| <span data-ttu-id="d033e-1206">public str groupMask(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1206">public str groupMask(\[str value\])</span></span>                                                          |                                                                                                                                               |
| <span data-ttu-id="d033e-1207">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1207">public str name(\[str value\])</span></span>                                                               | <span data-ttu-id="d033e-1208">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1208">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="d033e-1209">public boolean preventEditProperties(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1209">public boolean preventEditProperties(\[boolean value\])</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="d033e-1210">public GroupNodeType projectGroupType(\[GroupNodeType value\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1210">public GroupNodeType projectGroupType(\[GroupNodeType value\])</span></span>                               |                                                                                                                                               |
| <span data-ttu-id="d033e-1211">public void addUtilNode(UtilElementType type, str name)</span><span class="sxs-lookup"><span data-stu-id="d033e-1211">public void addUtilNode(UtilElementType type, str name)</span></span>                                      | <span data-ttu-id="d033e-1212">projectGroup にノードを追加します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1212">Adds a node to the projectGroup.</span></span>                                                                                                              |
| <span data-ttu-id="d033e-1213">public void addNode(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="d033e-1213">public void addNode(TreeNode node)</span></span>                                                           | <span data-ttu-id="d033e-1214">ProjectGroup に既存のノードを追加します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1214">Adds an existing node to the projectGroup.</span></span>                                                                                                    |

### <a name="method-findgroupmember"></a><span data-ttu-id="d033e-1215">メソッド findGroupMember</span><span class="sxs-lookup"><span data-stu-id="d033e-1215">Method findGroupMember</span></span>

<span data-ttu-id="d033e-1216">特定の要素の projectGroup を検索します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1216">Searches the projectGroup for a specific element.</span></span> <span data-ttu-id="d033e-1217">特定のグループまたはプロジェクト全体を検索するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1217">It can be used to search a specific group or the whole project.</span></span>

    public TreeNode findGroupMember(str name, UtilElementType type, [boolean searchSubgroups])

#### <a name="parameters"></a><span data-ttu-id="d033e-1218">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1218">Parameters</span></span>

<span data-ttu-id="d033e-1219">名前</span><span class="sxs-lookup"><span data-stu-id="d033e-1219">name</span></span>  
<span data-ttu-id="d033e-1220">検索が再帰的 (サブプロジェクトを検索するか) どうかを決定するブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="d033e-1220">A boolean flag that determines whether the search should be recursive (whether to search subprojects); optional.</span></span>

<!-- -->

<span data-ttu-id="d033e-1221">タイプ</span><span class="sxs-lookup"><span data-stu-id="d033e-1221">type</span></span>  
<span data-ttu-id="d033e-1222">検索が再帰的 (サブプロジェクトを検索するか) どうかを決定するブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="d033e-1222">A boolean flag that determines whether the search should be recursive (whether to search subprojects); optional.</span></span>

<!-- -->

<span data-ttu-id="d033e-1223">searchSubgroups</span><span class="sxs-lookup"><span data-stu-id="d033e-1223">searchSubgroups</span></span>  
<span data-ttu-id="d033e-1224">検索が再帰的 (サブプロジェクトを検索するか) どうかを決定するブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="d033e-1224">A boolean flag that determines whether the search should be recursive (whether to search subprojects); optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d033e-1225">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1225">Return Value</span></span>

<span data-ttu-id="d033e-1226">オブジェクトが見つからない場合は、条件を満たす最初のオブジェクト、または nullNothingnullptrunita null 参照 (Visual Basic にはなし) を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1226">The first object that fits the criteria; returns nullNothingnullptrunita null reference (Nothing in Visual Basic) if no object is found.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-1227">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1227">Remarks</span></span>

<span data-ttu-id="d033e-1228">このメソッドは ProjectNode にもあります。</span><span class="sxs-lookup"><span data-stu-id="d033e-1228">This method is also found on ProjectNode.</span></span>

### <a name="method-groupmask"></a><span data-ttu-id="d033e-1229">メソッド groupMask</span><span class="sxs-lookup"><span data-stu-id="d033e-1229">Method groupMask</span></span>

    public str groupMask([str value])

#### <a name="parameters"></a><span data-ttu-id="d033e-1230">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1230">Parameters</span></span>

<span data-ttu-id="d033e-1231">値</span><span class="sxs-lookup"><span data-stu-id="d033e-1231">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1232">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1232">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="d033e-1233">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d033e-1233">Method name</span></span>

<span data-ttu-id="d033e-1234">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1234">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="d033e-1235">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1235">Parameters</span></span>

<span data-ttu-id="d033e-1236">値</span><span class="sxs-lookup"><span data-stu-id="d033e-1236">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1237">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1237">Return Value</span></span>

<span data-ttu-id="d033e-1238">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="d033e-1238">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-1239">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1239">Remarks</span></span>

<span data-ttu-id="d033e-1240">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d033e-1240">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="d033e-1241">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1241">Begins with a letter.</span></span>
-   <span data-ttu-id="d033e-1242">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="d033e-1242">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="d033e-1243">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1243">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="d033e-1244">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="d033e-1244">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="d033e-1245">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="d033e-1245">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-preventeditproperties"></a><span data-ttu-id="d033e-1246">メソッド preventEditProperties</span><span class="sxs-lookup"><span data-stu-id="d033e-1246">Method preventEditProperties</span></span>

    public boolean preventEditProperties([boolean value])

#### <a name="parameters"></a><span data-ttu-id="d033e-1247">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1247">Parameters</span></span>

<span data-ttu-id="d033e-1248">値</span><span class="sxs-lookup"><span data-stu-id="d033e-1248">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1249">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1249">Return Value</span></span>

### <a name="method-projectgrouptype"></a><span data-ttu-id="d033e-1250">メソッド projectGroupType</span><span class="sxs-lookup"><span data-stu-id="d033e-1250">Method projectGroupType</span></span>

    public GroupNodeType projectGroupType([GroupNodeType value])

#### <a name="parameters"></a><span data-ttu-id="d033e-1251">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1251">Parameters</span></span>

<span data-ttu-id="d033e-1252">値</span><span class="sxs-lookup"><span data-stu-id="d033e-1252">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1253">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1253">Return Value</span></span>

### <a name="method-addutilnode"></a><span data-ttu-id="d033e-1254">メソッド addUtilNode</span><span class="sxs-lookup"><span data-stu-id="d033e-1254">Method addUtilNode</span></span>

<span data-ttu-id="d033e-1255">projectGroup にノードを追加します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1255">Adds a node to the projectGroup.</span></span>

    public void addUtilNode(UtilElementType type, str name)

#### <a name="parameters"></a><span data-ttu-id="d033e-1256">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1256">Parameters</span></span>

<span data-ttu-id="d033e-1257">タイプ</span><span class="sxs-lookup"><span data-stu-id="d033e-1257">type</span></span>  
<span data-ttu-id="d033e-1258">ノードの名前。</span><span class="sxs-lookup"><span data-stu-id="d033e-1258">The name of the node.</span></span>

<!-- -->

<span data-ttu-id="d033e-1259">名前</span><span class="sxs-lookup"><span data-stu-id="d033e-1259">name</span></span>  
<span data-ttu-id="d033e-1260">ノードの名前。</span><span class="sxs-lookup"><span data-stu-id="d033e-1260">The name of the node.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-1261">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1261">Remarks</span></span>

<span data-ttu-id="d033e-1262">このメソッドは、ProjectNode クラスにもあります。</span><span class="sxs-lookup"><span data-stu-id="d033e-1262">This method also is found on the ProjectNode class.</span></span>

### <a name="method-addnode"></a><span data-ttu-id="d033e-1263">メソッド addNode</span><span class="sxs-lookup"><span data-stu-id="d033e-1263">Method addNode</span></span>

<span data-ttu-id="d033e-1264">ProjectGroup に既存のノードを追加します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1264">Adds an existing node to the projectGroup.</span></span>

    public void addNode(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="d033e-1265">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1265">Parameters</span></span>

<span data-ttu-id="d033e-1266">node</span><span class="sxs-lookup"><span data-stu-id="d033e-1266">node</span></span>  
<span data-ttu-id="d033e-1267">追加するノード。</span><span class="sxs-lookup"><span data-stu-id="d033e-1267">The node to add.</span></span>

## <a name="class-projectlistnode"></a><span data-ttu-id="d033e-1268">クラス ProjectListNode</span><span class="sxs-lookup"><span data-stu-id="d033e-1268">Class ProjectListNode</span></span>
    class ProjectListNode extends TreeNode

<span data-ttu-id="d033e-1269">ProjectListNode クラスは、プロジェクトの概要ウィンドウ内のプロジェクトのプライベートと共有のリストに対応します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1269">The ProjectListNode class corresponds to the Private and Shared lists of projects in the project overview window.</span></span> <span data-ttu-id="d033e-1270">X++ コードから新しいプロジェクトを追加するのにには、ProjectListNode.addProject メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1270">Use the ProjectListNode.addProject method to add a new project from X++ code.</span></span>

### <a name="remarks"></a><span data-ttu-id="d033e-1271">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1271">Remarks</span></span>

<span data-ttu-id="d033e-1272">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1272">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="d033e-1273">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1273">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

### <a name="examples"></a><span data-ttu-id="d033e-1274">例</span><span class="sxs-lookup"><span data-stu-id="d033e-1274">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d033e-1275">メソッド</span><span class="sxs-lookup"><span data-stu-id="d033e-1275">Methods</span></span>

| <span data-ttu-id="d033e-1276">方法</span><span class="sxs-lookup"><span data-stu-id="d033e-1276">Method</span></span>                                                               | <span data-ttu-id="d033e-1277">説明</span><span class="sxs-lookup"><span data-stu-id="d033e-1277">Description</span></span>                     |
|----------------------------------------------------------------------|---------------------------------|
| <span data-ttu-id="d033e-1278">public ProjectNode addProject(str projectName, \[str projectClass\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1278">public ProjectNode addProject(str projectName, \[str projectClass\])</span></span> | <span data-ttu-id="d033e-1279">リストに新しいプロジェクトを追加します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1279">Adds a new project to the list.</span></span> |

### <a name="method-addproject"></a><span data-ttu-id="d033e-1280">メソッド addProject</span><span class="sxs-lookup"><span data-stu-id="d033e-1280">Method addProject</span></span>

<span data-ttu-id="d033e-1281">リストに新しいプロジェクトを追加します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1281">Adds a new project to the list.</span></span>

    public ProjectNode addProject(str projectName, [str projectClass])

#### <a name="parameters"></a><span data-ttu-id="d033e-1282">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1282">Parameters</span></span>

<span data-ttu-id="d033e-1283">projectName</span><span class="sxs-lookup"><span data-stu-id="d033e-1283">projectName</span></span>  
<span data-ttu-id="d033e-1284">projecttype の名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d033e-1284">The name of the projecttype; optional.</span></span> <span data-ttu-id="d033e-1285">これは、プロジェクトに関連付けられたクラスの名前でなければなりません (setProjectClass メソッドを参照)。</span><span class="sxs-lookup"><span data-stu-id="d033e-1285">This should be the name of a class associated with the project (see the setProjectClass method).</span></span> <span data-ttu-id="d033e-1286">値が指定されていない場合は、標準のプロジェクトがプロジェクトになります。</span><span class="sxs-lookup"><span data-stu-id="d033e-1286">If no value is supplied, the project becomes a standard project.</span></span>

<!-- -->

<span data-ttu-id="d033e-1287">projectClass</span><span class="sxs-lookup"><span data-stu-id="d033e-1287">projectClass</span></span>  
<span data-ttu-id="d033e-1288">projecttype の名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d033e-1288">The name of the projecttype; optional.</span></span> <span data-ttu-id="d033e-1289">これは、プロジェクトに関連付けられたクラスの名前でなければなりません (setProjectClass メソッドを参照)。</span><span class="sxs-lookup"><span data-stu-id="d033e-1289">This should be the name of a class associated with the project (see the setProjectClass method).</span></span> <span data-ttu-id="d033e-1290">値が指定されていない場合は、標準のプロジェクトがプロジェクトになります。</span><span class="sxs-lookup"><span data-stu-id="d033e-1290">If no value is supplied, the project becomes a standard project.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d033e-1291">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1291">Return Value</span></span>

<span data-ttu-id="d033e-1292">新たに追加された projectNode。</span><span class="sxs-lookup"><span data-stu-id="d033e-1292">The newly added projectNode.</span></span>

## <a name="class-projectnode"></a><span data-ttu-id="d033e-1293">クラス ProjectNode</span><span class="sxs-lookup"><span data-stu-id="d033e-1293">Class ProjectNode</span></span>
    class ProjectNode extends TreeNode

<span data-ttu-id="d033e-1294">ProjectNode クラスは、AOT プロジェクトの動作を制御します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1294">The ProjectNode class controls the behavior of an AOT project.</span></span>

### <a name="remarks"></a><span data-ttu-id="d033e-1295">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1295">Remarks</span></span>

<span data-ttu-id="d033e-1296">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1296">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="d033e-1297">このクラスから拡張して、新しいユーザー定義の AOT プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1297">Create a new, user-defined AOT project by extending from this class.</span></span> <span data-ttu-id="d033e-1298">このクラスのメソッドを上書きすることによって、プロジェクトの動作を制御します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1298">Control the behavior of the project by overriding the methods of this class.</span></span> <span data-ttu-id="d033e-1299">Web プロジェクトとヘルプ プロジェクトの両方を作成するには、ProjectNode クラスを拡張するクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1299">Create both Web projects and Help projects by creating classes that extend the ProjectNode class.</span></span>

### <a name="examples"></a><span data-ttu-id="d033e-1300">例</span><span class="sxs-lookup"><span data-stu-id="d033e-1300">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d033e-1301">メソッド</span><span class="sxs-lookup"><span data-stu-id="d033e-1301">Methods</span></span>

| <span data-ttu-id="d033e-1302">方法</span><span class="sxs-lookup"><span data-stu-id="d033e-1302">Method</span></span>                                                                                       | <span data-ttu-id="d033e-1303">説明</span><span class="sxs-lookup"><span data-stu-id="d033e-1303">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d033e-1304">public str addContextMenuItems()</span><span class="sxs-lookup"><span data-stu-id="d033e-1304">public str addContextMenuItems()</span></span>                                                             | <span data-ttu-id="d033e-1305">プロジェクト ノードのショートカット メニューに品目のリストを追加します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1305">Adds a list of items to the shortcut menu of the project node.</span></span>                                                                                |
| <span data-ttu-id="d033e-1306">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1306">public str changedBy(\[str value\])</span></span>                                                          | <span data-ttu-id="d033e-1307">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1307">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="d033e-1308">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1308">public Date changedDate(\[Date value\])</span></span>                                                      | <span data-ttu-id="d033e-1309">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1309">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="d033e-1310">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1310">public str changedTime(\[str value\])</span></span>                                                        | <span data-ttu-id="d033e-1311">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1311">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="d033e-1312">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1312">public str createdBy(\[str value\])</span></span>                                                          | <span data-ttu-id="d033e-1313">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1313">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="d033e-1314">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1314">public Date creationDate(\[Date value\])</span></span>                                                     | <span data-ttu-id="d033e-1315">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1315">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="d033e-1316">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1316">public str creationTime(\[str value\])</span></span>                                                       |                                                                                                                                               |
| <span data-ttu-id="d033e-1317">public str export(str buffer)</span><span class="sxs-lookup"><span data-stu-id="d033e-1317">public str export(str buffer)</span></span>                                                                |                                                                                                                                               |
| <span data-ttu-id="d033e-1318">public TreeNode findGroupMember(str name, UtilElementType type, \[boolean searchSubgroups\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1318">public TreeNode findGroupMember(str name, UtilElementType type, \[boolean searchSubgroups\])</span></span> | <span data-ttu-id="d033e-1319">特定の要素のプロジェクトまたはグループを検索します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1319">Searches the project or group for a specific element.</span></span>                                                                                         |
| <span data-ttu-id="d033e-1320">public str getProjectClassName()</span><span class="sxs-lookup"><span data-stu-id="d033e-1320">public str getProjectClassName()</span></span>                                                             | <span data-ttu-id="d033e-1321">プロジェクトの classid に対応するクラスの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1321">Returns the name of the class corresponding to the classid of the project.</span></span>                                                                    |
| <span data-ttu-id="d033e-1322">public ProjectNode getRunNode()</span><span class="sxs-lookup"><span data-stu-id="d033e-1322">public ProjectNode getRunNode()</span></span>                                                              | <span data-ttu-id="d033e-1323">プロジェクト ウィンドウを開いて、プロジェクトの概要ウィンドウで見つかった特定の projectNode のためにそのウィンドウのルート projectNode を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1323">Opens the project window and returns the root projectNode of that window, for a particular projectNode found in the project overview window.</span></span>  |
| <span data-ttu-id="d033e-1324">public str import(str buffer)</span><span class="sxs-lookup"><span data-stu-id="d033e-1324">public str import(str buffer)</span></span>                                                                |                                                                                                                                               |
| <span data-ttu-id="d033e-1325">public boolean isRunNode()</span><span class="sxs-lookup"><span data-stu-id="d033e-1325">public boolean isRunNode()</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="d033e-1326">public ProjectNode loadForInspection()</span><span class="sxs-lookup"><span data-stu-id="d033e-1326">public ProjectNode loadForInspection()</span></span>                                                       | <span data-ttu-id="d033e-1327">プロジェクトの概要ウィンドウにある projectNode の読み込まれたバージョンを返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1327">Returns a loaded version of a projectNode found in the project overview window.</span></span>                                                               |
| <span data-ttu-id="d033e-1328">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1328">public str name(\[str value\])</span></span>                                                               | <span data-ttu-id="d033e-1329">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1329">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="d033e-1330">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1330">public Guid origin(\[Guid value\])</span></span>                                                           |                                                                                                                                               |
| <span data-ttu-id="d033e-1331">public boolean removeFromProject(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="d033e-1331">public boolean removeFromProject(TreeNode node)</span></span>                                              |                                                                                                                                               |
| <span data-ttu-id="d033e-1332">public str tooltipText(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="d033e-1332">public str tooltipText(TreeNode node)</span></span>                                                        |                                                                                                                                               |
| <span data-ttu-id="d033e-1333">::public static str projectType()</span><span class="sxs-lookup"><span data-stu-id="d033e-1333">::public static str projectType()</span></span>                                                            |                                                                                                                                               |
| <span data-ttu-id="d033e-1334">public void lockUpdate()</span><span class="sxs-lookup"><span data-stu-id="d033e-1334">public void lockUpdate()</span></span>                                                                     | <span data-ttu-id="d033e-1335">一連のアクションを実行中に、視覚的な更新を禁止します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1335">Prevents visual updates while a series of actions is being performed.</span></span>                                                                         |
| <span data-ttu-id="d033e-1336">public void addSpecialOverlayIcon(str path, int resId, \[int xOffset\], \[int yOffset\])</span><span class="sxs-lookup"><span data-stu-id="d033e-1336">public void addSpecialOverlayIcon(str path, int resId, \[int xOffset\], \[int yOffset\])</span></span>     |                                                                                                                                               |
| <span data-ttu-id="d033e-1337">public void created(str name)</span><span class="sxs-lookup"><span data-stu-id="d033e-1337">public void created(str name)</span></span>                                                                | <span data-ttu-id="d033e-1338">プロジェクトの新しいインスタンスが作成された際、プロジェクトでカスタム アクションを実行を有効にします。</span><span class="sxs-lookup"><span data-stu-id="d033e-1338">Enables the ability to perform custom actions on a project when a new instance of the project is created.</span></span>                                     |
| <span data-ttu-id="d033e-1339">public void setSpecialIcon(int type, str name, int resId)</span><span class="sxs-lookup"><span data-stu-id="d033e-1339">public void setSpecialIcon(int type, str name, int resId)</span></span>                                    | <span data-ttu-id="d033e-1340">プロジェクト内の特定のノードに別のアイコンを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1340">Assigns a different icon to a specific node in the project.</span></span>                                                                                   |
| <span data-ttu-id="d033e-1341">public void loadProject(str buffer)</span><span class="sxs-lookup"><span data-stu-id="d033e-1341">public void loadProject(str buffer)</span></span>                                                          | <span data-ttu-id="d033e-1342">プロジェクトが読み込まれた際、プロジェクト定義にカスタムデータの格納と取得を有効にします。</span><span class="sxs-lookup"><span data-stu-id="d033e-1342">Enables storing and retrieving custom data in the project definition when a project is loaded.</span></span>                                                |
| <span data-ttu-id="d033e-1343">public void saveProject(str buffer)</span><span class="sxs-lookup"><span data-stu-id="d033e-1343">public void saveProject(str buffer)</span></span>                                                          | <span data-ttu-id="d033e-1344">アプリケーション オブジェクト データベースでは、プロジェクトと共にカスタム データの保存を有効にします。</span><span class="sxs-lookup"><span data-stu-id="d033e-1344">Enables saving custom data together with the project in the application object database.</span></span>                                                      |
| <span data-ttu-id="d033e-1345">public void unlockUpdate()</span><span class="sxs-lookup"><span data-stu-id="d033e-1345">public void unlockUpdate()</span></span>                                                                   | <span data-ttu-id="d033e-1346">lockUpdate で一連のアクションを開始した後にビジュアル更新プログラムを有効にします。</span><span class="sxs-lookup"><span data-stu-id="d033e-1346">Enables a visual update after a series of actions started with lockUpdate.</span></span>                                                                    |
| <span data-ttu-id="d033e-1347">public void handleContextMenuItem(int id)</span><span class="sxs-lookup"><span data-stu-id="d033e-1347">public void handleContextMenuItem(int id)</span></span>                                                    | <span data-ttu-id="d033e-1348">ユーザーが対応するメソッド addContextMenuItems で定義されているショートカット メニューの項目を選択するのを処理します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1348">Handles a user selecting an item on the shortcut menu that has been defined by the corresponding method addContextMenuItems.</span></span>                  |
| <span data-ttu-id="d033e-1349">public void addNode(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="d033e-1349">public void addNode(TreeNode node)</span></span>                                                           | <span data-ttu-id="d033e-1350">プロジェクトに既存のノードを追加します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1350">Adds an existing node to the project.</span></span>                                                                                                         |
| <span data-ttu-id="d033e-1351">public void addUtilNode(UtilElementType type, str name)</span><span class="sxs-lookup"><span data-stu-id="d033e-1351">public void addUtilNode(UtilElementType type, str name)</span></span>                                      | <span data-ttu-id="d033e-1352">プロジェクトにノードを追加します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1352">Adds a node to the project.</span></span>                                                                                                                   |
| <span data-ttu-id="d033e-1353">public void clear()</span><span class="sxs-lookup"><span data-stu-id="d033e-1353">public void clear()</span></span>                                                                          | <span data-ttu-id="d033e-1354">プロジェクトの内容を削除します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1354">Removes the contents of a project.</span></span>                                                                                                            |
| <span data-ttu-id="d033e-1355">public void setProjectClass(int classid)</span><span class="sxs-lookup"><span data-stu-id="d033e-1355">public void setProjectClass(int classid)</span></span>                                                     | <span data-ttu-id="d033e-1356">クラスをプロジェクトに割り当てますが、クラスに定義されているタイプをプロジェクトに与えます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1356">Assigns a class to the project, which gives the project the type that the class defines.</span></span>                                                      |
| <span data-ttu-id="d033e-1357">public void removeSpecialOverlayIcons(str path)</span><span class="sxs-lookup"><span data-stu-id="d033e-1357">public void removeSpecialOverlayIcons(str path)</span></span>                                              |                                                                                                                                               |
| <span data-ttu-id="d033e-1358">public void new()</span><span class="sxs-lookup"><span data-stu-id="d033e-1358">public void new()</span></span>                                                                            | <span data-ttu-id="d033e-1359">ProjectNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1359">Initializes a new instance of the ProjectNode class.</span></span>                                                                                          |

### <a name="method-addcontextmenuitems"></a><span data-ttu-id="d033e-1360">メソッド addContextMenuItems</span><span class="sxs-lookup"><span data-stu-id="d033e-1360">Method addContextMenuItems</span></span>

<span data-ttu-id="d033e-1361">プロジェクト ノードのショートカット メニューに品目のリストを追加します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1361">Adds a list of items to the shortcut menu of the project node.</span></span>

    public str addContextMenuItems()

#### <a name="return-value"></a><span data-ttu-id="d033e-1362">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1362">Return Value</span></span>

<span data-ttu-id="d033e-1363">追加するメニュー項目のコンマ区切りリスト。</span><span class="sxs-lookup"><span data-stu-id="d033e-1363">A comma-separated list of the menu items to be added.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-1364">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1364">Remarks</span></span>

<span data-ttu-id="d033e-1365">プロジェクト ノードのショートカット メニューに品目のリストを追加するには、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="d033e-1365">Override this method to add a list of items to the shortcut menu of the project node.</span></span> <span data-ttu-id="d033e-1366">追加されたメニュー項目の 1 つがユーザーによって選択されると、handleContextMenuItem メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1366">When one of the added menu items is selected by a user, the handleContextMenuItem method is called.</span></span> <span data-ttu-id="d033e-1367">適切なアクションを実行するには、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="d033e-1367">Override this method to perform the appropriate action.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="d033e-1368">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="d033e-1368">Method changedBy</span></span>

<span data-ttu-id="d033e-1369">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1369">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="d033e-1370">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1370">Parameters</span></span>

<span data-ttu-id="d033e-1371">値</span><span class="sxs-lookup"><span data-stu-id="d033e-1371">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1372">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1372">Return Value</span></span>

<span data-ttu-id="d033e-1373">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="d033e-1373">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="d033e-1374">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="d033e-1374">Method changedDate</span></span>

<span data-ttu-id="d033e-1375">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1375">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="d033e-1376">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1376">Parameters</span></span>

<span data-ttu-id="d033e-1377">値</span><span class="sxs-lookup"><span data-stu-id="d033e-1377">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1378">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1378">Return Value</span></span>

<span data-ttu-id="d033e-1379">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="d033e-1379">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="d033e-1380">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="d033e-1380">Method changedTime</span></span>

<span data-ttu-id="d033e-1381">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1381">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="d033e-1382">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1382">Parameters</span></span>

<span data-ttu-id="d033e-1383">値</span><span class="sxs-lookup"><span data-stu-id="d033e-1383">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1384">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1384">Return Value</span></span>

<span data-ttu-id="d033e-1385">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="d033e-1385">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="d033e-1386">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="d033e-1386">Method createdBy</span></span>

<span data-ttu-id="d033e-1387">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1387">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="d033e-1388">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1388">Parameters</span></span>

<span data-ttu-id="d033e-1389">値</span><span class="sxs-lookup"><span data-stu-id="d033e-1389">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1390">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1390">Return Value</span></span>

<span data-ttu-id="d033e-1391">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="d033e-1391">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="d033e-1392">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="d033e-1392">Method creationDate</span></span>

<span data-ttu-id="d033e-1393">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1393">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="d033e-1394">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1394">Parameters</span></span>

<span data-ttu-id="d033e-1395">値</span><span class="sxs-lookup"><span data-stu-id="d033e-1395">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1396">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1396">Return Value</span></span>

<span data-ttu-id="d033e-1397">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="d033e-1397">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="d033e-1398">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="d033e-1398">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="d033e-1399">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1399">Parameters</span></span>

<span data-ttu-id="d033e-1400">値</span><span class="sxs-lookup"><span data-stu-id="d033e-1400">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1401">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1401">Return Value</span></span>

### <a name="method-export"></a><span data-ttu-id="d033e-1402">メソッド export</span><span class="sxs-lookup"><span data-stu-id="d033e-1402">Method export</span></span>

    public str export(str buffer)

#### <a name="parameters"></a><span data-ttu-id="d033e-1403">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1403">Parameters</span></span>

<span data-ttu-id="d033e-1404">バッファ</span><span class="sxs-lookup"><span data-stu-id="d033e-1404">buffer</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1405">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1405">Return Value</span></span>

### <a name="method-findgroupmember"></a><span data-ttu-id="d033e-1406">メソッド findGroupMember</span><span class="sxs-lookup"><span data-stu-id="d033e-1406">Method findGroupMember</span></span>

<span data-ttu-id="d033e-1407">特定の要素のプロジェクトまたはグループを検索します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1407">Searches the project or group for a specific element.</span></span>

    public TreeNode findGroupMember(str name, UtilElementType type, [boolean searchSubgroups])

#### <a name="parameters"></a><span data-ttu-id="d033e-1408">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1408">Parameters</span></span>

<span data-ttu-id="d033e-1409">名前</span><span class="sxs-lookup"><span data-stu-id="d033e-1409">name</span></span>  
<span data-ttu-id="d033e-1410">検索を再帰的に行うかどうかを決定するブール値フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="d033e-1410">A Boolean flag to determine whether the search should be recursive; optional.</span></span>

<!-- -->

<span data-ttu-id="d033e-1411">タイプ</span><span class="sxs-lookup"><span data-stu-id="d033e-1411">type</span></span>  
<span data-ttu-id="d033e-1412">検索を再帰的に行うかどうかを決定するブール値フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="d033e-1412">A Boolean flag to determine whether the search should be recursive; optional.</span></span>

<!-- -->

<span data-ttu-id="d033e-1413">searchSubgroups</span><span class="sxs-lookup"><span data-stu-id="d033e-1413">searchSubgroups</span></span>  
<span data-ttu-id="d033e-1414">検索を再帰的に行うかどうかを決定するブール値フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="d033e-1414">A Boolean flag to determine whether the search should be recursive; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d033e-1415">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1415">Return Value</span></span>

<span data-ttu-id="d033e-1416">オブジェクトが見つからない場合は、条件を満たす最初のオブジェクト、または nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="d033e-1416">The first object that fits the criteria, or nullNothingnullptrunita null reference (Nothing in Visual Basic) if no object is found.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-1417">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1417">Remarks</span></span>

<span data-ttu-id="d033e-1418">このメソッドは ProjectGroupNode にもあります。</span><span class="sxs-lookup"><span data-stu-id="d033e-1418">This method is also found on ProjectGroupNode.</span></span>

### <a name="method-getprojectclassname"></a><span data-ttu-id="d033e-1419">メソッド getProjectClassName</span><span class="sxs-lookup"><span data-stu-id="d033e-1419">Method getProjectClassName</span></span>

<span data-ttu-id="d033e-1420">プロジェクトの classid に対応するクラスの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1420">Returns the name of the class corresponding to the classid of the project.</span></span>

    public str getProjectClassName()

#### <a name="return-value"></a><span data-ttu-id="d033e-1421">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1421">Return Value</span></span>

<span data-ttu-id="d033e-1422">プロジェクトの classid に対応するクラスの名前。</span><span class="sxs-lookup"><span data-stu-id="d033e-1422">The name of the class corresponding to the classid of the project.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-1423">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1423">Remarks</span></span>

<span data-ttu-id="d033e-1424">setClassId メソッドは、クラス ID をプロジェクトに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1424">The setClassId method assigns a classid to the project.</span></span>

### <a name="method-getrunnode"></a><span data-ttu-id="d033e-1425">メソッド getRunNode</span><span class="sxs-lookup"><span data-stu-id="d033e-1425">Method getRunNode</span></span>

<span data-ttu-id="d033e-1426">プロジェクト ウィンドウを開いて、プロジェクトの概要ウィンドウで見つかった特定の projectNode のためにそのウィンドウのルート projectNode を返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1426">Opens the project window and returns the root projectNode of that window, for a particular projectNode found in the project overview window.</span></span>

    public ProjectNode getRunNode()

#### <a name="return-value"></a><span data-ttu-id="d033e-1427">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1427">Return Value</span></span>

<span data-ttu-id="d033e-1428">実行中の projectNode。</span><span class="sxs-lookup"><span data-stu-id="d033e-1428">The running projectNode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-1429">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1429">Remarks</span></span>

<span data-ttu-id="d033e-1430">[プロジェクト] ウィンドウを開くことがなく実行中の projectNode を取得するには、ProjectNode.loadForInspection メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1430">To obtain a running projectNode without opening the project window, use the ProjectNode.loadForInspection Method.</span></span>

### <a name="method-import"></a><span data-ttu-id="d033e-1431">メソッド import</span><span class="sxs-lookup"><span data-stu-id="d033e-1431">Method import</span></span>

    public str import(str buffer)

#### <a name="parameters"></a><span data-ttu-id="d033e-1432">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1432">Parameters</span></span>

<span data-ttu-id="d033e-1433">バッファ</span><span class="sxs-lookup"><span data-stu-id="d033e-1433">buffer</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1434">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1434">Return Value</span></span>

### <a name="method-isrunnode"></a><span data-ttu-id="d033e-1435">メソッド isRunNode</span><span class="sxs-lookup"><span data-stu-id="d033e-1435">Method isRunNode</span></span>

    public boolean isRunNode()

#### <a name="return-value"></a><span data-ttu-id="d033e-1436">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1436">Return Value</span></span>

### <a name="method-loadforinspection"></a><span data-ttu-id="d033e-1437">メソッド loadForInspection</span><span class="sxs-lookup"><span data-stu-id="d033e-1437">Method loadForInspection</span></span>

<span data-ttu-id="d033e-1438">プロジェクトの概要ウィンドウにある projectNode の読み込まれたバージョンを返します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1438">Returns a loaded version of a projectNode found in the project overview window.</span></span>

    public ProjectNode loadForInspection()

#### <a name="return-value"></a><span data-ttu-id="d033e-1439">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1439">Return Value</span></span>

<span data-ttu-id="d033e-1440">読み込まれた projectNode。</span><span class="sxs-lookup"><span data-stu-id="d033e-1440">The loaded projectNode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-1441">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1441">Remarks</span></span>

<span data-ttu-id="d033e-1442">[プロジェクト] ウィンドウを開いたときに projectNode を読み込むには、getRunNode メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1442">To get a loaded projectNode while also opening the project window, use the method getRunNode.</span></span>

### <a name="method-name"></a><span data-ttu-id="d033e-1443">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d033e-1443">Method name</span></span>

<span data-ttu-id="d033e-1444">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1444">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="d033e-1445">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1445">Parameters</span></span>

<span data-ttu-id="d033e-1446">値</span><span class="sxs-lookup"><span data-stu-id="d033e-1446">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1447">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1447">Return Value</span></span>

<span data-ttu-id="d033e-1448">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="d033e-1448">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-1449">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1449">Remarks</span></span>

<span data-ttu-id="d033e-1450">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d033e-1450">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="d033e-1451">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1451">Begins with a letter.</span></span>
-   <span data-ttu-id="d033e-1452">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="d033e-1452">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="d033e-1453">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1453">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="d033e-1454">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="d033e-1454">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="d033e-1455">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="d033e-1455">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-origin"></a><span data-ttu-id="d033e-1456">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="d033e-1456">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="d033e-1457">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1457">Parameters</span></span>

<span data-ttu-id="d033e-1458">値</span><span class="sxs-lookup"><span data-stu-id="d033e-1458">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1459">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1459">Return Value</span></span>

### <a name="method-removefromproject"></a><span data-ttu-id="d033e-1460">メソッド removeFromProject</span><span class="sxs-lookup"><span data-stu-id="d033e-1460">Method removeFromProject</span></span>

    public boolean removeFromProject(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="d033e-1461">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1461">Parameters</span></span>

<span data-ttu-id="d033e-1462">node</span><span class="sxs-lookup"><span data-stu-id="d033e-1462">node</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1463">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1463">Return Value</span></span>

### <a name="method-tooltiptext"></a><span data-ttu-id="d033e-1464">メソッド tooltipText</span><span class="sxs-lookup"><span data-stu-id="d033e-1464">Method tooltipText</span></span>

    public str tooltipText(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="d033e-1465">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1465">Parameters</span></span>

<span data-ttu-id="d033e-1466">node</span><span class="sxs-lookup"><span data-stu-id="d033e-1466">node</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1467">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1467">Return Value</span></span>

### <a name="method-projecttype"></a><span data-ttu-id="d033e-1468">メソッド projectType</span><span class="sxs-lookup"><span data-stu-id="d033e-1468">Method projectType</span></span>

    public static str projectType()

#### <a name="return-value"></a><span data-ttu-id="d033e-1469">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1469">Return Value</span></span>

### <a name="method-lockupdate"></a><span data-ttu-id="d033e-1470">メソッド lockUpdate</span><span class="sxs-lookup"><span data-stu-id="d033e-1470">Method lockUpdate</span></span>

<span data-ttu-id="d033e-1471">一連のアクションを実行中に、視覚的な更新を禁止します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1471">Prevents visual updates while a series of actions is being performed.</span></span>

    public void lockUpdate()

#### <a name="remarks"></a><span data-ttu-id="d033e-1472">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1472">Remarks</span></span>

<span data-ttu-id="d033e-1473">一連のアクションの後にビジュアル アップデートを実行するには、unlockUpdate を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1473">To perform visual updates after the series of actions, call unlockUpdate.</span></span>

### <a name="method-addspecialoverlayicon"></a><span data-ttu-id="d033e-1474">メソッド addSpecialOverlayIcon</span><span class="sxs-lookup"><span data-stu-id="d033e-1474">Method addSpecialOverlayIcon</span></span>

    public void addSpecialOverlayIcon(str path, int resId, [int xOffset], [int yOffset])

#### <a name="parameters"></a><span data-ttu-id="d033e-1475">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1475">Parameters</span></span>

<span data-ttu-id="d033e-1476">path</span><span class="sxs-lookup"><span data-stu-id="d033e-1476">path</span></span>  

<!-- -->

<span data-ttu-id="d033e-1477">resId</span><span class="sxs-lookup"><span data-stu-id="d033e-1477">resId</span></span>  

<!-- -->

<span data-ttu-id="d033e-1478">xOffset</span><span class="sxs-lookup"><span data-stu-id="d033e-1478">xOffset</span></span>  

<!-- -->

<span data-ttu-id="d033e-1479">yOffset</span><span class="sxs-lookup"><span data-stu-id="d033e-1479">yOffset</span></span>  

### <a name="method-created"></a><span data-ttu-id="d033e-1480">メソッド created</span><span class="sxs-lookup"><span data-stu-id="d033e-1480">Method created</span></span>

<span data-ttu-id="d033e-1481">プロジェクトの新しいインスタンスが作成された際、プロジェクトでカスタム アクションを実行を有効にします。</span><span class="sxs-lookup"><span data-stu-id="d033e-1481">Enables the ability to perform custom actions on a project when a new instance of the project is created.</span></span>

    public void created(str name)

#### <a name="parameters"></a><span data-ttu-id="d033e-1482">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1482">Parameters</span></span>

<span data-ttu-id="d033e-1483">名前</span><span class="sxs-lookup"><span data-stu-id="d033e-1483">name</span></span>  
<span data-ttu-id="d033e-1484">プロジェクト インスタンスの名前。</span><span class="sxs-lookup"><span data-stu-id="d033e-1484">The name of the project instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-1485">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1485">Remarks</span></span>

<span data-ttu-id="d033e-1486">このメソッドは、プロジェクトの新しいインスタンスが作成されるときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1486">This method is called when a new instance of the project is created.</span></span> <span data-ttu-id="d033e-1487">プロジェクトでカスタム アクションを実行するには、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="d033e-1487">Override this method to perform custom actions on your project.</span></span>

### <a name="method-setspecialicon"></a><span data-ttu-id="d033e-1488">メソッド setSpecialIcon</span><span class="sxs-lookup"><span data-stu-id="d033e-1488">Method setSpecialIcon</span></span>

<span data-ttu-id="d033e-1489">プロジェクト内の特定のノードに別のアイコンを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1489">Assigns a different icon to a specific node in the project.</span></span>

    public void setSpecialIcon(int type, str name, int resId)

#### <a name="parameters"></a><span data-ttu-id="d033e-1490">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1490">Parameters</span></span>

<span data-ttu-id="d033e-1491">タイプ</span><span class="sxs-lookup"><span data-stu-id="d033e-1491">type</span></span>  
<span data-ttu-id="d033e-1492">指定されたノードに使用する必要があるアイコンの ID。</span><span class="sxs-lookup"><span data-stu-id="d033e-1492">The ID of the icon that must be used for the specified node.</span></span>

<!-- -->

<span data-ttu-id="d033e-1493">名前</span><span class="sxs-lookup"><span data-stu-id="d033e-1493">name</span></span>  
<span data-ttu-id="d033e-1494">指定されたノードに使用する必要があるアイコンの ID。</span><span class="sxs-lookup"><span data-stu-id="d033e-1494">The ID of the icon that must be used for the specified node.</span></span>

<!-- -->

<span data-ttu-id="d033e-1495">resId</span><span class="sxs-lookup"><span data-stu-id="d033e-1495">resId</span></span>  
<span data-ttu-id="d033e-1496">指定されたノードに使用する必要があるアイコンの ID。</span><span class="sxs-lookup"><span data-stu-id="d033e-1496">The ID of the icon that must be used for the specified node.</span></span>

### <a name="method-loadproject"></a><span data-ttu-id="d033e-1497">メソッド loadProject</span><span class="sxs-lookup"><span data-stu-id="d033e-1497">Method loadProject</span></span>

<span data-ttu-id="d033e-1498">プロジェクトが読み込まれた際、プロジェクト定義にカスタムデータの格納と取得を有効にします。</span><span class="sxs-lookup"><span data-stu-id="d033e-1498">Enables storing and retrieving custom data in the project definition when a project is loaded.</span></span>

    public void loadProject(str buffer)

#### <a name="parameters"></a><span data-ttu-id="d033e-1499">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1499">Parameters</span></span>

<span data-ttu-id="d033e-1500">バッファ</span><span class="sxs-lookup"><span data-stu-id="d033e-1500">buffer</span></span>  
<span data-ttu-id="d033e-1501">saveProject によってプロジェクトに保存されたカスタム データを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d033e-1501">A string that contains the custom data that was saved in the project by saveProject.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-1502">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1502">Remarks</span></span>

<span data-ttu-id="d033e-1503">このメソッドは、プロジェクトが読み込まれたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1503">This method is called when a project is loaded.</span></span> <span data-ttu-id="d033e-1504">saveProject および loadProject を上書きすることにより、ユーザーはカスタム データをプロジェクト定義に保存して取得できます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1504">By overriding saveProject and loadProject, a user can store and retrieve custom data in the project definition.</span></span> <span data-ttu-id="d033e-1505">読み込みを続行するには、プロジェクトの super() を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d033e-1505">You must call super() for the project to continue loading.</span></span>

### <a name="method-saveproject"></a><span data-ttu-id="d033e-1506">メソッド saveProject</span><span class="sxs-lookup"><span data-stu-id="d033e-1506">Method saveProject</span></span>

<span data-ttu-id="d033e-1507">アプリケーション オブジェクト データベースでは、プロジェクトと共にカスタム データの保存を有効にします。</span><span class="sxs-lookup"><span data-stu-id="d033e-1507">Enables saving custom data together with the project in the application object database.</span></span>

    public void saveProject(str buffer)

#### <a name="parameters"></a><span data-ttu-id="d033e-1508">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1508">Parameters</span></span>

<span data-ttu-id="d033e-1509">バッファ</span><span class="sxs-lookup"><span data-stu-id="d033e-1509">buffer</span></span>  
<span data-ttu-id="d033e-1510">データをパッキングするために使用する必要がある文字列バッファ。</span><span class="sxs-lookup"><span data-stu-id="d033e-1510">A string buffer that must be used for packing the data.</span></span> <span data-ttu-id="d033e-1511">その後、バッファ はsuper() に渡されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d033e-1511">The buffer must then be passed on to super().</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-1512">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1512">Remarks</span></span>

<span data-ttu-id="d033e-1513">このメソッドを上書きすることにより、アプリケーション オブジェクト データベースでは、プロジェクトと共にカスタム データを保存できます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1513">By overriding this method, you can save custom data together with the project in the application object database.</span></span> <span data-ttu-id="d033e-1514">データは「&lt;APPDATA&gt; ... &lt;/APPDATA&gt;」の形式で XML 文字列として形成することをお勧めします。このデータは loadProject メソッドをオーバーライドして取得できます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1514">It is recommended that the data be formed as an XML string in the following form: "&lt;APPDATA&gt; ... &lt;/APPDATA&gt;" The data can be retrieved by overriding the loadProject method.</span></span>

### <a name="method-unlockupdate"></a><span data-ttu-id="d033e-1515">メソッド unlockUpdate</span><span class="sxs-lookup"><span data-stu-id="d033e-1515">Method unlockUpdate</span></span>

<span data-ttu-id="d033e-1516">lockUpdate で一連のアクションを開始した後にビジュアル更新プログラムを有効にします。</span><span class="sxs-lookup"><span data-stu-id="d033e-1516">Enables a visual update after a series of actions started with lockUpdate.</span></span>

    public void unlockUpdate()

### <a name="method-handlecontextmenuitem"></a><span data-ttu-id="d033e-1517">メソッド handleContextMenuItem</span><span class="sxs-lookup"><span data-stu-id="d033e-1517">Method handleContextMenuItem</span></span>

<span data-ttu-id="d033e-1518">ユーザーが対応するメソッド addContextMenuItems で定義されているショートカット メニューの項目を選択するのを処理します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1518">Handles a user selecting an item on the shortcut menu that has been defined by the corresponding method addContextMenuItems.</span></span>

    public void handleContextMenuItem(int id)

#### <a name="parameters"></a><span data-ttu-id="d033e-1519">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1519">Parameters</span></span>

<span data-ttu-id="d033e-1520">id</span><span class="sxs-lookup"><span data-stu-id="d033e-1520">id</span></span>  
<span data-ttu-id="d033e-1521">メニュー項目の ID。</span><span class="sxs-lookup"><span data-stu-id="d033e-1521">The ID of the menu items.</span></span> <span data-ttu-id="d033e-1522">これは、addContextMenuItems メソッドによって設定されたリスト内の 0 から始まる数値です。</span><span class="sxs-lookup"><span data-stu-id="d033e-1522">This is the zero-based number in the list set by the addContextMenuItems method.</span></span> <span data-ttu-id="d033e-1523">accContextMenuItems が文字列である "item1,item2" を返し、ユーザーがショートカット メニューの品目である "item2" を選択した場合、この方法では値 1 を使用します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1523">If accContextMenuItems returns the string "item1,item2" and the user selects the item "item2" in the shortcut menu, this method uses the value 1.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-1524">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1524">Remarks</span></span>

<span data-ttu-id="d033e-1525">このメソッドは、ユーザーが対応するメソッド addContextMenuItems で定義されているショートカット メニューの項目を選択するときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1525">This method is called when a user selects an item on the shortcut menu that has been defined by the corresponding method addContextMenuItems.</span></span>

### <a name="method-addnode"></a><span data-ttu-id="d033e-1526">メソッド addNode</span><span class="sxs-lookup"><span data-stu-id="d033e-1526">Method addNode</span></span>

<span data-ttu-id="d033e-1527">プロジェクトに既存のノードを追加します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1527">Adds an existing node to the project.</span></span>

    public void addNode(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="d033e-1528">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1528">Parameters</span></span>

<span data-ttu-id="d033e-1529">node</span><span class="sxs-lookup"><span data-stu-id="d033e-1529">node</span></span>  
<span data-ttu-id="d033e-1530">追加するノード。</span><span class="sxs-lookup"><span data-stu-id="d033e-1530">The node to add.</span></span>

### <a name="method-addutilnode"></a><span data-ttu-id="d033e-1531">メソッド addUtilNode</span><span class="sxs-lookup"><span data-stu-id="d033e-1531">Method addUtilNode</span></span>

<span data-ttu-id="d033e-1532">プロジェクトにノードを追加します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1532">Adds a node to the project.</span></span>

    public void addUtilNode(UtilElementType type, str name)

#### <a name="parameters"></a><span data-ttu-id="d033e-1533">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1533">Parameters</span></span>

<span data-ttu-id="d033e-1534">タイプ</span><span class="sxs-lookup"><span data-stu-id="d033e-1534">type</span></span>  
<span data-ttu-id="d033e-1535">ノードの名前。</span><span class="sxs-lookup"><span data-stu-id="d033e-1535">The name of the node.</span></span>

<!-- -->

<span data-ttu-id="d033e-1536">名前</span><span class="sxs-lookup"><span data-stu-id="d033e-1536">name</span></span>  
<span data-ttu-id="d033e-1537">ノードの名前。</span><span class="sxs-lookup"><span data-stu-id="d033e-1537">The name of the node.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-1538">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1538">Remarks</span></span>

<span data-ttu-id="d033e-1539">この関数は ProjectGroupNode にもあります。</span><span class="sxs-lookup"><span data-stu-id="d033e-1539">This function is also found on ProjectGroupNode.</span></span>

### <a name="method-clear"></a><span data-ttu-id="d033e-1540">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="d033e-1540">Method clear</span></span>

<span data-ttu-id="d033e-1541">プロジェクトの内容を削除します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1541">Removes the contents of a project.</span></span>

    public void clear()

#### <a name="remarks"></a><span data-ttu-id="d033e-1542">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1542">Remarks</span></span>

<span data-ttu-id="d033e-1543">このメソッドは、アプリケーション オブジェクト ツリー (AOT) からプロジェクトの内容を削除しません。プロジェクト自体からのみです。</span><span class="sxs-lookup"><span data-stu-id="d033e-1543">This method does not remove the project contents from the Application Object Tree (AOT)—only from the project itself.</span></span> <span data-ttu-id="d033e-1544">このメソッドはプロジェクトの内容を削除しますが、プロジェクト フォルダーは削除しません。</span><span class="sxs-lookup"><span data-stu-id="d033e-1544">This method removes the project contents but does not remove the project folder.</span></span> <span data-ttu-id="d033e-1545">1 回のメソッド呼び出しでプロジェクトとその内容を削除するには、AOTdelete メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1545">To delete a project and its contents in one method call, use the AOTdelete method.</span></span> <span data-ttu-id="d033e-1546">オブジェクトを AOT から削除するには、AOTdelete メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1546">To delete objects from the AOT, use the AOTdelete method.</span></span>

#### <a name="examples"></a><span data-ttu-id="d033e-1547">例</span><span class="sxs-lookup"><span data-stu-id="d033e-1547">Examples</span></span>

<span data-ttu-id="d033e-1548">次の例では、Project1 プロジェクト内のプライベート フォルダー内のオブジェクトをすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1548">The following example removes any objects in the Project1 project in the Private folder.</span></span>

    static void clearProjectObjects(Args _args) 
        { 
            ProjectNode privatePn; 
            ProjectNode pn; 
            // Navigate to the Private projects folder. 
            privatePn = infolog.projectRootNode().AOTfindChild("Private"); 
            // Get a reference to the project. 
            pn = privatePn.AOTfindChild("Project1"); 
            // Clear the project. 
            pn.clear(); 
        }

### <a name="method-setprojectclass"></a><span data-ttu-id="d033e-1549">メソッド setProjectClass</span><span class="sxs-lookup"><span data-stu-id="d033e-1549">Method setProjectClass</span></span>

<span data-ttu-id="d033e-1550">クラスをプロジェクトに割り当てますが、クラスに定義されているタイプをプロジェクトに与えます。</span><span class="sxs-lookup"><span data-stu-id="d033e-1550">Assigns a class to the project, which gives the project the type that the class defines.</span></span>

    public void setProjectClass(int classid)

#### <a name="parameters"></a><span data-ttu-id="d033e-1551">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1551">Parameters</span></span>

<span data-ttu-id="d033e-1552">classid</span><span class="sxs-lookup"><span data-stu-id="d033e-1552">classid</span></span>  
<span data-ttu-id="d033e-1553">プロジェクトに割り当てるクラスの ID。</span><span class="sxs-lookup"><span data-stu-id="d033e-1553">The ID of the class to assign to the project.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d033e-1554">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1554">Remarks</span></span>

<span data-ttu-id="d033e-1555">指定されたクラスは、projectNode クラスを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d033e-1555">The specified class must extend the projectNode class.</span></span>

### <a name="method-removespecialoverlayicons"></a><span data-ttu-id="d033e-1556">メソッド removeSpecialOverlayIcons</span><span class="sxs-lookup"><span data-stu-id="d033e-1556">Method removeSpecialOverlayIcons</span></span>

    public void removeSpecialOverlayIcons(str path)

#### <a name="parameters"></a><span data-ttu-id="d033e-1557">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1557">Parameters</span></span>

<span data-ttu-id="d033e-1558">path</span><span class="sxs-lookup"><span data-stu-id="d033e-1558">path</span></span>  

### <a name="method-new"></a><span data-ttu-id="d033e-1559">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d033e-1559">Method new</span></span>

<span data-ttu-id="d033e-1560">ProjectNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d033e-1560">Initializes a new instance of the ProjectNode class.</span></span>

    public void new()

## <a name="class-propertieswindow"></a><span data-ttu-id="d033e-1561">クラス PropertiesWindow</span><span class="sxs-lookup"><span data-stu-id="d033e-1561">Class PropertiesWindow</span></span>
    class PropertiesWindow extends Object

### <a name="remarks"></a><span data-ttu-id="d033e-1562">備考</span><span class="sxs-lookup"><span data-stu-id="d033e-1562">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d033e-1563">例</span><span class="sxs-lookup"><span data-stu-id="d033e-1563">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d033e-1564">メソッド</span><span class="sxs-lookup"><span data-stu-id="d033e-1564">Methods</span></span>

| <span data-ttu-id="d033e-1565">方法</span><span class="sxs-lookup"><span data-stu-id="d033e-1565">Method</span></span>                                                   | <span data-ttu-id="d033e-1566">説明</span><span class="sxs-lookup"><span data-stu-id="d033e-1566">Description</span></span> |
|----------------------------------------------------------|-------------|
| <span data-ttu-id="d033e-1567">public int Activate(PropWindowDisplayState displaystate)</span><span class="sxs-lookup"><span data-stu-id="d033e-1567">public int Activate(PropWindowDisplayState displaystate)</span></span> |             |
| <span data-ttu-id="d033e-1568">public boolean DockFrame(PropWindowDockState dockstate)</span><span class="sxs-lookup"><span data-stu-id="d033e-1568">public boolean DockFrame(PropWindowDockState dockstate)</span></span>  |             |
| <span data-ttu-id="d033e-1569">public str GetSelectedPropertyName()</span><span class="sxs-lookup"><span data-stu-id="d033e-1569">public str GetSelectedPropertyName()</span></span>                     |             |
| <span data-ttu-id="d033e-1570">public boolean IsVisible()</span><span class="sxs-lookup"><span data-stu-id="d033e-1570">public boolean IsVisible()</span></span>                               |             |
| <span data-ttu-id="d033e-1571">public boolean SelectPropertyByName(str propname)</span><span class="sxs-lookup"><span data-stu-id="d033e-1571">public boolean SelectPropertyByName(str propname)</span></span>        |             |
| <span data-ttu-id="d033e-1572">public boolean SelectTab(PropWindowSelectTab selecttab)</span><span class="sxs-lookup"><span data-stu-id="d033e-1572">public boolean SelectTab(PropWindowSelectTab selecttab)</span></span>  |             |

### <a name="method-activate"></a><span data-ttu-id="d033e-1573">メソッド Activate</span><span class="sxs-lookup"><span data-stu-id="d033e-1573">Method Activate</span></span>

    public int Activate(PropWindowDisplayState displaystate)

#### <a name="parameters"></a><span data-ttu-id="d033e-1574">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1574">Parameters</span></span>

<span data-ttu-id="d033e-1575">displaystate</span><span class="sxs-lookup"><span data-stu-id="d033e-1575">displaystate</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1576">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1576">Return Value</span></span>

### <a name="method-dockframe"></a><span data-ttu-id="d033e-1577">メソッド DockFrame</span><span class="sxs-lookup"><span data-stu-id="d033e-1577">Method DockFrame</span></span>

    public boolean DockFrame(PropWindowDockState dockstate)

#### <a name="parameters"></a><span data-ttu-id="d033e-1578">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1578">Parameters</span></span>

<span data-ttu-id="d033e-1579">dockstate</span><span class="sxs-lookup"><span data-stu-id="d033e-1579">dockstate</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1580">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1580">Return Value</span></span>

### <a name="method-getselectedpropertyname"></a><span data-ttu-id="d033e-1581">メソッド GetSelectedPropertyName</span><span class="sxs-lookup"><span data-stu-id="d033e-1581">Method GetSelectedPropertyName</span></span>

    public str GetSelectedPropertyName()

#### <a name="return-value"></a><span data-ttu-id="d033e-1582">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1582">Return Value</span></span>

### <a name="method-isvisible"></a><span data-ttu-id="d033e-1583">メソッド IsVisible</span><span class="sxs-lookup"><span data-stu-id="d033e-1583">Method IsVisible</span></span>

    public boolean IsVisible()

#### <a name="return-value"></a><span data-ttu-id="d033e-1584">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1584">Return Value</span></span>

### <a name="method-selectpropertybyname"></a><span data-ttu-id="d033e-1585">メソッド SelectPropertyByName</span><span class="sxs-lookup"><span data-stu-id="d033e-1585">Method SelectPropertyByName</span></span>

    public boolean SelectPropertyByName(str propname)

#### <a name="parameters"></a><span data-ttu-id="d033e-1586">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1586">Parameters</span></span>

<span data-ttu-id="d033e-1587">propname</span><span class="sxs-lookup"><span data-stu-id="d033e-1587">propname</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1588">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1588">Return Value</span></span>

### <a name="method-selecttab"></a><span data-ttu-id="d033e-1589">メソッド SelectTab</span><span class="sxs-lookup"><span data-stu-id="d033e-1589">Method SelectTab</span></span>

    public boolean SelectTab(PropWindowSelectTab selecttab)

#### <a name="parameters"></a><span data-ttu-id="d033e-1590">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d033e-1590">Parameters</span></span>

<span data-ttu-id="d033e-1591">selecttab</span><span class="sxs-lookup"><span data-stu-id="d033e-1591">selecttab</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d033e-1592">戻り値</span><span class="sxs-lookup"><span data-stu-id="d033e-1592">Return Value</span></span>



