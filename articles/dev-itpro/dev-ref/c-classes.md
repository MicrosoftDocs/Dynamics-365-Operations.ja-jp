---
title: C クラス
description: 文字 C で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 11/06/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 50962
ms.assetid: 53eb660c-9a11-4f59-9870-a24502588ebf
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65d92f10f3456d44a38978d8902aa1dbd0a3c8d6
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595470"
---
# <a name="c-classes"></a><span data-ttu-id="20ffe-103">C クラス</span><span class="sxs-lookup"><span data-stu-id="20ffe-103">C classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20ffe-104">文字 C で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="20ffe-104">System API classes that start with the letter C.</span></span>

<a name="class-classnode"></a><span data-ttu-id="20ffe-105">クラス ClassNode</span><span class="sxs-lookup"><span data-stu-id="20ffe-105">Class ClassNode</span></span>
---------------

    class ClassNode extends TreeNode

<span data-ttu-id="20ffe-106">ClassNode クラスは、Finance and Operations のアプリケーション オブジェクト ツリー (AOT) 内のクラスを表す TreeNode クラスの特殊な形式です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-106">The ClassNode class is a specialization of the TreeNode class that represents a class in the Finance and Operations Application Object Tree (AOT).</span></span>

### <a name="remarks"></a><span data-ttu-id="20ffe-107">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-107">Remarks</span></span>

<span data-ttu-id="20ffe-108">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-108">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="20ffe-109">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-109">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-110">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-110">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="20ffe-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-111">Methods</span></span>

| <span data-ttu-id="20ffe-112">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-112">Method</span></span>                                            | <span data-ttu-id="20ffe-113">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-113">Description</span></span>                                                                                                                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ffe-114">public TreeNode AOToverrideMethod(str methodName)</span><span class="sxs-lookup"><span data-stu-id="20ffe-114">public TreeNode AOToverrideMethod(str methodName)</span></span> |                                                                                                                                               |
| <span data-ttu-id="20ffe-115">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-115">public str changedBy(\[str value\])</span></span>               | <span data-ttu-id="20ffe-116">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-116">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="20ffe-117">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-117">public Date changedDate(\[Date value\])</span></span>           | <span data-ttu-id="20ffe-118">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-118">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="20ffe-119">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-119">public str changedTime(\[str value\])</span></span>             | <span data-ttu-id="20ffe-120">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-120">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="20ffe-121">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-121">public str createdBy(\[str value\])</span></span>               | <span data-ttu-id="20ffe-122">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-122">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="20ffe-123">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-123">public Date creationDate(\[Date value\])</span></span>          | <span data-ttu-id="20ffe-124">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-124">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="20ffe-125">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-125">public str creationTime(\[str value\])</span></span>            |                                                                                                                                               |
| <span data-ttu-id="20ffe-126">public str extends(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-126">public str extends(\[str value\])</span></span>                 |                                                                                                                                               |
| <span data-ttu-id="20ffe-127">public int iD(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-127">public int iD(\[int value\])</span></span>                      |                                                                                                                                               |
| <span data-ttu-id="20ffe-128">public boolean isDetached()</span><span class="sxs-lookup"><span data-stu-id="20ffe-128">public boolean isDetached()</span></span>                       |                                                                                                                                               |
| <span data-ttu-id="20ffe-129">public int legacyId(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-129">public int legacyId(\[int value\])</span></span>                |                                                                                                                                               |
| <span data-ttu-id="20ffe-130">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-130">public str name(\[str value\])</span></span>                    | <span data-ttu-id="20ffe-131">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-131">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="20ffe-132">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-132">public Guid origin(\[Guid value\])</span></span>                |                                                                                                                                               |
| <span data-ttu-id="20ffe-133">public int runOn(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-133">public int runOn(\[int value\])</span></span>                   |                                                                                                                                               |
| <span data-ttu-id="20ffe-134">public void AOTedit(\[int Line\], \[int Column\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-134">public void AOTedit(\[int Line\], \[int Column\])</span></span> | <span data-ttu-id="20ffe-135">クラスを開き、エディターで変更することもできるようにします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-135">Opens the class so that it can be modified in the editor.</span></span>                                                                                     |

### <a name="method-aotoverridemethod"></a><span data-ttu-id="20ffe-136">メソッド AOToverrideMethod</span><span class="sxs-lookup"><span data-stu-id="20ffe-136">Method AOToverrideMethod</span></span>

    public TreeNode AOToverrideMethod(str methodName)

#### <a name="parameters"></a><span data-ttu-id="20ffe-137">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-137">Parameters</span></span>

<span data-ttu-id="20ffe-138">methodName</span><span class="sxs-lookup"><span data-stu-id="20ffe-138">methodName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-139">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-139">Return Value</span></span>

### <a name="method-changedby"></a><span data-ttu-id="20ffe-140">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="20ffe-140">Method changedBy</span></span>

<span data-ttu-id="20ffe-141">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-141">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-142">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-142">Parameters</span></span>

<span data-ttu-id="20ffe-143">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-143">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-144">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-144">Return Value</span></span>

<span data-ttu-id="20ffe-145">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="20ffe-145">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="20ffe-146">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="20ffe-146">Method changedDate</span></span>

<span data-ttu-id="20ffe-147">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-147">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-148">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-148">Parameters</span></span>

<span data-ttu-id="20ffe-149">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-149">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-150">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-150">Return Value</span></span>

<span data-ttu-id="20ffe-151">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="20ffe-151">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="20ffe-152">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="20ffe-152">Method changedTime</span></span>

<span data-ttu-id="20ffe-153">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-153">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-154">Parameters</span></span>

<span data-ttu-id="20ffe-155">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-155">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-156">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-156">Return Value</span></span>

<span data-ttu-id="20ffe-157">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="20ffe-157">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="20ffe-158">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="20ffe-158">Method createdBy</span></span>

<span data-ttu-id="20ffe-159">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-159">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-160">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-160">Parameters</span></span>

<span data-ttu-id="20ffe-161">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-161">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-162">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-162">Return Value</span></span>

<span data-ttu-id="20ffe-163">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="20ffe-163">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="20ffe-164">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="20ffe-164">Method creationDate</span></span>

<span data-ttu-id="20ffe-165">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-165">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-166">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-166">Parameters</span></span>

<span data-ttu-id="20ffe-167">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-167">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-168">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-168">Return Value</span></span>

<span data-ttu-id="20ffe-169">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="20ffe-169">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="20ffe-170">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="20ffe-170">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-171">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-171">Parameters</span></span>

<span data-ttu-id="20ffe-172">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-172">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-173">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-173">Return Value</span></span>

### <a name="method-extends"></a><span data-ttu-id="20ffe-174">メソッド extends</span><span class="sxs-lookup"><span data-stu-id="20ffe-174">Method extends</span></span>

    public str extends([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-175">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-175">Parameters</span></span>

<span data-ttu-id="20ffe-176">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-176">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-177">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-177">Return Value</span></span>

### <a name="method-id"></a><span data-ttu-id="20ffe-178">メソッド iD</span><span class="sxs-lookup"><span data-stu-id="20ffe-178">Method iD</span></span>

    public int iD([int value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-179">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-179">Parameters</span></span>

<span data-ttu-id="20ffe-180">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-180">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-181">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-181">Return Value</span></span>

### <a name="method-isdetached"></a><span data-ttu-id="20ffe-182">メソッド isDetached</span><span class="sxs-lookup"><span data-stu-id="20ffe-182">Method isDetached</span></span>

    public boolean isDetached()

#### <a name="return-value"></a><span data-ttu-id="20ffe-183">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-183">Return Value</span></span>

### <a name="method-legacyid"></a><span data-ttu-id="20ffe-184">メソッド legacyId</span><span class="sxs-lookup"><span data-stu-id="20ffe-184">Method legacyId</span></span>

    public int legacyId([int value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-185">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-185">Parameters</span></span>

<span data-ttu-id="20ffe-186">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-186">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-187">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-187">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="20ffe-188">メソッド名</span><span class="sxs-lookup"><span data-stu-id="20ffe-188">Method name</span></span>

<span data-ttu-id="20ffe-189">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-189">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-190">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-190">Parameters</span></span>

<span data-ttu-id="20ffe-191">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-191">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-192">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-192">Return Value</span></span>

<span data-ttu-id="20ffe-193">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="20ffe-193">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-194">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-194">Remarks</span></span>

<span data-ttu-id="20ffe-195">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-195">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="20ffe-196">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-196">Begins with a letter.</span></span>
-   <span data-ttu-id="20ffe-197">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-197">Does not exceed 250 characters.</span></span>
-   <span data-ttu-id="20ffe-198">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-198">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="20ffe-199">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-199">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="20ffe-200">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-200">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, classes, and so on.</span></span>

### <a name="method-origin"></a><span data-ttu-id="20ffe-201">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="20ffe-201">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-202">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-202">Parameters</span></span>

<span data-ttu-id="20ffe-203">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-203">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-204">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-204">Return Value</span></span>

### <a name="method-runon"></a><span data-ttu-id="20ffe-205">メソッド runOn</span><span class="sxs-lookup"><span data-stu-id="20ffe-205">Method runOn</span></span>

    public int runOn([int value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-206">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-206">Parameters</span></span>

<span data-ttu-id="20ffe-207">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-207">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-208">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-208">Return Value</span></span>

### <a name="method-aotedit"></a><span data-ttu-id="20ffe-209">メソッド AOTedit</span><span class="sxs-lookup"><span data-stu-id="20ffe-209">Method AOTedit</span></span>

<span data-ttu-id="20ffe-210">クラスを開き、エディターで変更することもできるようにします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-210">Opens the class so that it can be modified in the editor.</span></span>

    public void AOTedit([int Line], [int Column])

#### <a name="parameters"></a><span data-ttu-id="20ffe-211">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-211">Parameters</span></span>

<span data-ttu-id="20ffe-212">明細行</span><span class="sxs-lookup"><span data-stu-id="20ffe-212">Line</span></span>  
<span data-ttu-id="20ffe-213">無視される値、オプション。</span><span class="sxs-lookup"><span data-stu-id="20ffe-213">A value that is ignored; optional.</span></span>

<!-- -->

<span data-ttu-id="20ffe-214">円柱</span><span class="sxs-lookup"><span data-stu-id="20ffe-214">Column</span></span>  
<span data-ttu-id="20ffe-215">無視される値、オプション。</span><span class="sxs-lookup"><span data-stu-id="20ffe-215">A value that is ignored; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-216">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-216">Remarks</span></span>

<span data-ttu-id="20ffe-217">すべてのメソッドはエディターに読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-217">All methods are loaded into the editor.</span></span> <span data-ttu-id="20ffe-218">引数は、下位互換性のためにのみ署名に含まれているため、無視されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-218">The arguments are included in the signature for backward compatibility only; they are ignored.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-219">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-219">Examples</span></span>

    static void example() 
    { 
        ClassNode classNode; 

        classNode = infolog.findNode('\Classes\SysClassWizard'); 
        classNode.AOTedit(); 
    }

## <a name="class-clientprintjobsettings"></a><span data-ttu-id="20ffe-220">クラス ClientPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="20ffe-220">Class ClientPrintJobSettings</span></span>
    class ClientPrintJobSettings extends PrintJobSettings

### <a name="remarks"></a><span data-ttu-id="20ffe-221">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-221">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-222">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-222">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="20ffe-223">メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-223">Methods</span></span>

| <span data-ttu-id="20ffe-224">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-224">Method</span></span>                                                                                                                  | <span data-ttu-id="20ffe-225">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-225">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="20ffe-226">public container getFontDimension(container container)</span><span class="sxs-lookup"><span data-stu-id="20ffe-226">public container getFontDimension(container container)</span></span>                                                                  |                                                 |
| <span data-ttu-id="20ffe-227">public container getInfoStrings()</span><span class="sxs-lookup"><span data-stu-id="20ffe-227">public container getInfoStrings()</span></span>                                                                                       |                                                 |
| <span data-ttu-id="20ffe-228">public int getNextLineOffset(container container)</span><span class="sxs-lookup"><span data-stu-id="20ffe-228">public int getNextLineOffset(container container)</span></span>                                                                       |                                                 |
| <span data-ttu-id="20ffe-229">public container getPageInfo()</span><span class="sxs-lookup"><span data-stu-id="20ffe-229">public container getPageInfo()</span></span>                                                                                          |                                                 |
| <span data-ttu-id="20ffe-230">public container getPrinterNames()</span><span class="sxs-lookup"><span data-stu-id="20ffe-230">public container getPrinterNames()</span></span>                                                                                      |                                                 |
| <span data-ttu-id="20ffe-231">public int getTextWidth(str text, str fontName, int charSet, int fontHeight, int style, int weight)</span><span class="sxs-lookup"><span data-stu-id="20ffe-231">public int getTextWidth(str text, str fontName, int charSet, int fontHeight, int style, int weight)</span></span>                     |                                                 |
| <span data-ttu-id="20ffe-232">public container getTextWidthExt(container container)</span><span class="sxs-lookup"><span data-stu-id="20ffe-232">public container getTextWidthExt(container container)</span></span>                                                                   |                                                 |
| <span data-ttu-id="20ffe-233">public container getWordWrapInfo(str text, int width, str fontName, int charSet, int fontHeight, int style, int weight)</span><span class="sxs-lookup"><span data-stu-id="20ffe-233">public container getWordWrapInfo(str text, int width, str fontName, int charSet, int fontHeight, int style, int weight)</span></span> |                                                 |
| <span data-ttu-id="20ffe-234">public container getWordWrapInfoExt(container container)</span><span class="sxs-lookup"><span data-stu-id="20ffe-234">public container getWordWrapInfoExt(container container)</span></span>                                                                |                                                 |
| <span data-ttu-id="20ffe-235">public container printerSettingsExt(str formName, \[xArgs args\], \[ReportRun reportRun\], \[int showWhat\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-235">public container printerSettingsExt(str formName, \[xArgs args\], \[ReportRun reportRun\], \[int showWhat\])</span></span>            |                                                 |
| <span data-ttu-id="20ffe-236">public container setOrientationGetPageInfo(PrinterOrientation orientation)</span><span class="sxs-lookup"><span data-stu-id="20ffe-236">public container setOrientationGetPageInfo(PrinterOrientation orientation)</span></span>                                              |                                                 |
| <span data-ttu-id="20ffe-237">public void new(\[container Settings\], \[boolean infoOnly\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-237">public void new(\[container Settings\], \[boolean infoOnly\])</span></span>                                                           | <span data-ttu-id="20ffe-238">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-238">Initializes a new instance of the Object class.</span></span> |

### <a name="method-getfontdimension"></a><span data-ttu-id="20ffe-239">メソッド getFontDimension</span><span class="sxs-lookup"><span data-stu-id="20ffe-239">Method getFontDimension</span></span>

    public container getFontDimension(container container)

#### <a name="parameters"></a><span data-ttu-id="20ffe-240">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-240">Parameters</span></span>

<span data-ttu-id="20ffe-241">コンテナー</span><span class="sxs-lookup"><span data-stu-id="20ffe-241">container</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-242">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-242">Return Value</span></span>

### <a name="method-getinfostrings"></a><span data-ttu-id="20ffe-243">メソッド getInfoStrings</span><span class="sxs-lookup"><span data-stu-id="20ffe-243">Method getInfoStrings</span></span>

    public container getInfoStrings()

#### <a name="return-value"></a><span data-ttu-id="20ffe-244">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-244">Return Value</span></span>

### <a name="method-getnextlineoffset"></a><span data-ttu-id="20ffe-245">メソッド getNextLineOffset</span><span class="sxs-lookup"><span data-stu-id="20ffe-245">Method getNextLineOffset</span></span>

    public int getNextLineOffset(container container)

#### <a name="parameters"></a><span data-ttu-id="20ffe-246">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-246">Parameters</span></span>

<span data-ttu-id="20ffe-247">コンテナー</span><span class="sxs-lookup"><span data-stu-id="20ffe-247">container</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-248">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-248">Return Value</span></span>

### <a name="method-getpageinfo"></a><span data-ttu-id="20ffe-249">メソッド getPageInfo</span><span class="sxs-lookup"><span data-stu-id="20ffe-249">Method getPageInfo</span></span>

    public container getPageInfo()

#### <a name="return-value"></a><span data-ttu-id="20ffe-250">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-250">Return Value</span></span>

### <a name="method-getprinternames"></a><span data-ttu-id="20ffe-251">メソッド getPrinterNames</span><span class="sxs-lookup"><span data-stu-id="20ffe-251">Method getPrinterNames</span></span>

    public container getPrinterNames()

#### <a name="return-value"></a><span data-ttu-id="20ffe-252">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-252">Return Value</span></span>

### <a name="method-gettextwidth"></a><span data-ttu-id="20ffe-253">メソッド getTextWidth</span><span class="sxs-lookup"><span data-stu-id="20ffe-253">Method getTextWidth</span></span>

    public int getTextWidth(str text, str fontName, int charSet, int fontHeight, int style, int weight)

#### <a name="parameters"></a><span data-ttu-id="20ffe-254">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-254">Parameters</span></span>

<span data-ttu-id="20ffe-255">テキスト</span><span class="sxs-lookup"><span data-stu-id="20ffe-255">text</span></span>  

<!-- -->

<span data-ttu-id="20ffe-256">fontName</span><span class="sxs-lookup"><span data-stu-id="20ffe-256">fontName</span></span>  

<!-- -->

<span data-ttu-id="20ffe-257">charSet</span><span class="sxs-lookup"><span data-stu-id="20ffe-257">charSet</span></span>  

<!-- -->

<span data-ttu-id="20ffe-258">fontHeight</span><span class="sxs-lookup"><span data-stu-id="20ffe-258">fontHeight</span></span>  

<!-- -->

<span data-ttu-id="20ffe-259">style</span><span class="sxs-lookup"><span data-stu-id="20ffe-259">style</span></span>  

<!-- -->

<span data-ttu-id="20ffe-260">重量</span><span class="sxs-lookup"><span data-stu-id="20ffe-260">weight</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-261">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-261">Return Value</span></span>

### <a name="method-gettextwidthext"></a><span data-ttu-id="20ffe-262">メソッド getTextWidthExt</span><span class="sxs-lookup"><span data-stu-id="20ffe-262">Method getTextWidthExt</span></span>

    public container getTextWidthExt(container container)

#### <a name="parameters"></a><span data-ttu-id="20ffe-263">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-263">Parameters</span></span>

<span data-ttu-id="20ffe-264">コンテナー</span><span class="sxs-lookup"><span data-stu-id="20ffe-264">container</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-265">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-265">Return Value</span></span>

### <a name="method-getwordwrapinfo"></a><span data-ttu-id="20ffe-266">メソッド getWordWrapInfo</span><span class="sxs-lookup"><span data-stu-id="20ffe-266">Method getWordWrapInfo</span></span>

    public container getWordWrapInfo(str text, int width, str fontName, int charSet, int fontHeight, int style, int weight)

#### <a name="parameters"></a><span data-ttu-id="20ffe-267">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-267">Parameters</span></span>

<span data-ttu-id="20ffe-268">テキスト</span><span class="sxs-lookup"><span data-stu-id="20ffe-268">text</span></span>  

<!-- -->

<span data-ttu-id="20ffe-269">width</span><span class="sxs-lookup"><span data-stu-id="20ffe-269">width</span></span>  

<!-- -->

<span data-ttu-id="20ffe-270">fontName</span><span class="sxs-lookup"><span data-stu-id="20ffe-270">fontName</span></span>  

<!-- -->

<span data-ttu-id="20ffe-271">charSet</span><span class="sxs-lookup"><span data-stu-id="20ffe-271">charSet</span></span>  

<!-- -->

<span data-ttu-id="20ffe-272">fontHeight</span><span class="sxs-lookup"><span data-stu-id="20ffe-272">fontHeight</span></span>  

<!-- -->

<span data-ttu-id="20ffe-273">style</span><span class="sxs-lookup"><span data-stu-id="20ffe-273">style</span></span>  

<!-- -->

<span data-ttu-id="20ffe-274">重量</span><span class="sxs-lookup"><span data-stu-id="20ffe-274">weight</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-275">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-275">Return Value</span></span>

### <a name="method-getwordwrapinfoext"></a><span data-ttu-id="20ffe-276">メソッド getWordWrapInfoExt</span><span class="sxs-lookup"><span data-stu-id="20ffe-276">Method getWordWrapInfoExt</span></span>

    public container getWordWrapInfoExt(container container)

#### <a name="parameters"></a><span data-ttu-id="20ffe-277">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-277">Parameters</span></span>

<span data-ttu-id="20ffe-278">コンテナー</span><span class="sxs-lookup"><span data-stu-id="20ffe-278">container</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-279">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-279">Return Value</span></span>

### <a name="method-printersettingsext"></a><span data-ttu-id="20ffe-280">メソッド printerSettingsExt</span><span class="sxs-lookup"><span data-stu-id="20ffe-280">Method printerSettingsExt</span></span>

    public container printerSettingsExt(str formName, [xArgs args], [ReportRun reportRun], [int showWhat])

#### <a name="parameters"></a><span data-ttu-id="20ffe-281">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-281">Parameters</span></span>

<span data-ttu-id="20ffe-282">formName</span><span class="sxs-lookup"><span data-stu-id="20ffe-282">formName</span></span>  

<!-- -->

<span data-ttu-id="20ffe-283">args</span><span class="sxs-lookup"><span data-stu-id="20ffe-283">args</span></span>  

<!-- -->

<span data-ttu-id="20ffe-284">reportRun</span><span class="sxs-lookup"><span data-stu-id="20ffe-284">reportRun</span></span>  

<!-- -->

<span data-ttu-id="20ffe-285">showWhat</span><span class="sxs-lookup"><span data-stu-id="20ffe-285">showWhat</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-286">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-286">Return Value</span></span>

### <a name="method-setorientationgetpageinfo"></a><span data-ttu-id="20ffe-287">メソッド setOrientationGetPageInfo</span><span class="sxs-lookup"><span data-stu-id="20ffe-287">Method setOrientationGetPageInfo</span></span>

    public container setOrientationGetPageInfo(PrinterOrientation orientation)

#### <a name="parameters"></a><span data-ttu-id="20ffe-288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-288">Parameters</span></span>

<span data-ttu-id="20ffe-289">orientation</span><span class="sxs-lookup"><span data-stu-id="20ffe-289">orientation</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-290">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-290">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="20ffe-291">メソッド new</span><span class="sxs-lookup"><span data-stu-id="20ffe-291">Method new</span></span>

<span data-ttu-id="20ffe-292">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-292">Initializes a new instance of the Object class.</span></span>

    public void new([container Settings], [boolean infoOnly])

#### <a name="parameters"></a><span data-ttu-id="20ffe-293">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-293">Parameters</span></span>

<span data-ttu-id="20ffe-294">設定</span><span class="sxs-lookup"><span data-stu-id="20ffe-294">Settings</span></span>  

<!-- -->

<span data-ttu-id="20ffe-295">infoOnly</span><span class="sxs-lookup"><span data-stu-id="20ffe-295">infoOnly</span></span>  

## <a name="class-clrinterop"></a><span data-ttu-id="20ffe-296">クラス CLRInterop</span><span class="sxs-lookup"><span data-stu-id="20ffe-296">Class CLRInterop</span></span>
    class CLRInterop extends Object

<span data-ttu-id="20ffe-297">ClrInterop クラスは、タイプ マーシャ リングおよび例外処理の機能を提供するユーティリティ クラスです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-297">The ClrInterop class is a utility class that provides functionality for type marshaling and exception handling.</span></span> <span data-ttu-id="20ffe-298">すべてのメソッドは静的であるため、クラスのインスタンス化をする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-298">Because all the methods are static, no instantiation of the class is required.</span></span>

### <a name="remarks"></a><span data-ttu-id="20ffe-299">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-299">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-300">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-300">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="20ffe-301">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-301">Methods</span></span>

| <span data-ttu-id="20ffe-302">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-302">Method</span></span>                                                                               | <span data-ttu-id="20ffe-303">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-303">Description</span></span>                                                                                                                              |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ffe-304">::public static AnyType getAnyTypeForObject(CLRObject clrObject)</span><span class="sxs-lookup"><span data-stu-id="20ffe-304">::public static AnyType getAnyTypeForObject(CLRObject clrObject)</span></span>                     | <span data-ttu-id="20ffe-305">共通言語ランタイム (CLR) オブジェクトを X++ anytype データ型の値に変換します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-305">Converts a common language runtime (CLR) object to a value of the X++ anytype data type.</span></span>                                                 |
| <span data-ttu-id="20ffe-306">::public static CLRObject getLastException()</span><span class="sxs-lookup"><span data-stu-id="20ffe-306">::public static CLRObject getLastException()</span></span>                                         | <span data-ttu-id="20ffe-307">最新の CLR 例外を取得します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-307">Retrieves the most recent CLR exception.</span></span>                                                                                                 |
| <span data-ttu-id="20ffe-308">::public static CLRObject getObjectForAnyType(AnyType anyType)</span><span class="sxs-lookup"><span data-stu-id="20ffe-308">::public static CLRObject getObjectForAnyType(AnyType anyType)</span></span>                       | <span data-ttu-id="20ffe-309">X++ anytype データ型の値を CLRObject データ型の値に変換します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-309">Converts a value of the X++ anytype data type to a value of the CLRObject data type.</span></span>                                                     |
| <span data-ttu-id="20ffe-310">::public static CLRObject getType(str clrTypeName)</span><span class="sxs-lookup"><span data-stu-id="20ffe-310">::public static CLRObject getType(str clrTypeName)</span></span>                                   |                                                                                                                                          |
| <span data-ttu-id="20ffe-311">::public static boolean isNull(CLRObject clrObject)</span><span class="sxs-lookup"><span data-stu-id="20ffe-311">::public static boolean isNull(CLRObject clrObject)</span></span>                                  | <span data-ttu-id="20ffe-312">指定された CLRObject インスタンスが nullNothingnullptrunita null 参照 (Visual Basic では Nothing) にセットされているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-312">Confirms whether the specified CLRObject instance is set to nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>            |
| <span data-ttu-id="20ffe-313">::public static CLRObject Null(str clrTypeName)</span><span class="sxs-lookup"><span data-stu-id="20ffe-313">::public static CLRObject Null(str clrTypeName)</span></span>                                      | <span data-ttu-id="20ffe-314">nullNothingnullptrunita null 参照 (Visual Basic では Nothing) の値を持つ CLR データ型を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-314">Returns a CLR data type that has a value of nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>                            |
| <span data-ttu-id="20ffe-315">::public static CLRObject parseClrEnum(str clrEnumTypeName, str enumValues)</span><span class="sxs-lookup"><span data-stu-id="20ffe-315">::public static CLRObject parseClrEnum(str clrEnumTypeName, str enumValues)</span></span>          | <span data-ttu-id="20ffe-316">1 つ以上の列挙定数の名前または数値の文字列で表したものを、等価の CLRObject インスタンスに変換します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-316">Converts the string representation of the name or numeric value of one or more enumerated constants to an equivalent CLRObject instance.</span></span> |
| <span data-ttu-id="20ffe-317">::public static CLRObject staticInvoke(str className, str methodName, VarArg params)</span><span class="sxs-lookup"><span data-stu-id="20ffe-317">::public static CLRObject staticInvoke(str className, str methodName, VarArg params)</span></span> | <span data-ttu-id="20ffe-318">CLR データ型の静的メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-318">Calls a static method on a CLR data type.</span></span>                                                                                                |
| <span data-ttu-id="20ffe-319">::public static void loadAssembly(str clrAssemblyName)</span><span class="sxs-lookup"><span data-stu-id="20ffe-319">::public static void loadAssembly(str clrAssemblyName)</span></span>                               |                                                                                                                                          |
| <span data-ttu-id="20ffe-320">public void new()</span><span class="sxs-lookup"><span data-stu-id="20ffe-320">public void new()</span></span>                                                                    | <span data-ttu-id="20ffe-321">CLRInterop クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-321">Initializes a new instance of the CLRInterop class.</span></span>                                                                                      |

### <a name="method-getanytypeforobject"></a><span data-ttu-id="20ffe-322">メソッド getAnyTypeForObject</span><span class="sxs-lookup"><span data-stu-id="20ffe-322">Method getAnyTypeForObject</span></span>

<span data-ttu-id="20ffe-323">共通言語ランタイム (CLR) オブジェクトを X++ anytype データ型の値に変換します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-323">Converts a common language runtime (CLR) object to a value of the X++ anytype data type.</span></span>

    public static AnyType getAnyTypeForObject(CLRObject clrObject)

#### <a name="parameters"></a><span data-ttu-id="20ffe-324">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-324">Parameters</span></span>

<span data-ttu-id="20ffe-325">clrObject</span><span class="sxs-lookup"><span data-stu-id="20ffe-325">clrObject</span></span>  
<span data-ttu-id="20ffe-326">X++ データ型に変換する CLR オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="20ffe-326">The CLR object to convert to an X++ data type.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-327">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-327">Return Value</span></span>

<span data-ttu-id="20ffe-328">\_オブジェクトの引数値を持つ X++ anytype データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-328">An X++ anytype date type that has the value of the \_object argument.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-329">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-329">Remarks</span></span>

<span data-ttu-id="20ffe-330">攻撃者が getAnyTypeForObject メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-330">If an attacker can control input to the getAnyTypeForObject method, a security risk exists.</span></span> <span data-ttu-id="20ffe-331">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-331">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="20ffe-332">サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-332">Calls to this method on the server require permission.</span></span> <span data-ttu-id="20ffe-333">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-333">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span> <span data-ttu-id="20ffe-334">引数 X++ のデータ型に変換することができない場合、Exception::ClrError タイプの例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-334">If the argument cannot be converted to an X++ data type, an exception of the Exception::ClrError type is thrown.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-335">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-335">Examples</span></span>

<span data-ttu-id="20ffe-336">次の例では、CLR 文字列の値を X++ str データ型に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-336">The following example sets the value of a CLR string to an X++ str data type.</span></span>

    { 
        CLRObject clrObj; 
        InteropPermission perm; 
        System.String   clrStr = "Calculate total"; 
        str             s; 

        perm = new InteropPermission(InteropKind::ClrInterop); 
        if (perm == null) 
        { 
            return; 
        } 
        perm.assert(); 

        s = ClrInterop::getAnyTypeForObject(clrStr); 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-getlastexception"></a><span data-ttu-id="20ffe-337">メソッド getLastException</span><span class="sxs-lookup"><span data-stu-id="20ffe-337">Method getLastException</span></span>

<span data-ttu-id="20ffe-338">最新の CLR 例外を取得します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-338">Retrieves the most recent CLR exception.</span></span>

    public static CLRObject getLastException()

#### <a name="return-value"></a><span data-ttu-id="20ffe-339">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-339">Return Value</span></span>

<span data-ttu-id="20ffe-340">Exception::ClrError 型の最新の例外。それ以外の場合は、nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-340">The most recent exception of the Exception::ClrError type; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-341">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-341">Remarks</span></span>

<span data-ttu-id="20ffe-342">攻撃者が getLastException メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-342">If an attacker can control input to the getLastException method, a security risk exists.</span></span> <span data-ttu-id="20ffe-343">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-343">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="20ffe-344">サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-344">Calls to this method on the server require permission.</span></span> <span data-ttu-id="20ffe-345">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-345">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-346">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-346">Examples</span></span>

<span data-ttu-id="20ffe-347">次の例では、無効な形式の日付を渡します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-347">The following example tries to pass in a date that has an invalid format.</span></span> <span data-ttu-id="20ffe-348">スローされた CLR 例外は、X++ 例外に変換された後、情報ログに出力されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-348">The CLR exception that is thrown is converted to an X++ exception and then printed to the Infolog.</span></span> <span data-ttu-id="20ffe-349">入れ子になった例外は情報ログにも出力されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-349">Any nested exceptions are also printed to the Infolog.</span></span>

    static void Job2(Args _args) 
    { 
        CLRObject clrObj; 
        InteropPermission perm; 

        try 
        { 
            System.DateTime::Parse( "-1/-1/-1"); 
        } 
        catch( Exception::CLRError ) 
        { 
            perm = new InteropPermission(InteropKind::ClrInterop); 
            if (perm == null) 
            { 
                return; 
            } 
            perm.assert(); 

            e = ClrInterop::getLastException(); 

            CodeAccessPermission::revertAssert(); 

            while( e ) 
            { 
                info( e.get_Message() ); 
                e = e.get_InnerException(); 
            } 
        } 

    }

### <a name="method-getobjectforanytype"></a><span data-ttu-id="20ffe-350">メソッド getObjectForAnyType</span><span class="sxs-lookup"><span data-stu-id="20ffe-350">Method getObjectForAnyType</span></span>

<span data-ttu-id="20ffe-351">X++ anytype データ型の値を CLRObject データ型の値に変換します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-351">Converts a value of the X++ anytype data type to a value of the CLRObject data type.</span></span>

    public static CLRObject getObjectForAnyType(AnyType anyType)

#### <a name="parameters"></a><span data-ttu-id="20ffe-352">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-352">Parameters</span></span>

<span data-ttu-id="20ffe-353">anyType</span><span class="sxs-lookup"><span data-stu-id="20ffe-353">anyType</span></span>  
<span data-ttu-id="20ffe-354">CLRObject データ型の値に変換する X++ 値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-354">The X++ value to convert to a value of the CLRObject data type.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-355">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-355">Return Value</span></span>

<span data-ttu-id="20ffe-356">値 \_anytype 引数を持つ CLR オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="20ffe-356">The CLR object that has the value of the \_anytype argument.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-357">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-357">Remarks</span></span>

<span data-ttu-id="20ffe-358">攻撃者が getObjectForAnyType メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-358">If an attacker can control input to the getObjectForAnyType method, a security risk exists.</span></span> <span data-ttu-id="20ffe-359">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-359">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="20ffe-360">サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-360">Calls to this method on the server require permission.</span></span> <span data-ttu-id="20ffe-361">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-361">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span> <span data-ttu-id="20ffe-362">引数を CLRObject 型に変換することができない場合、Exception::CLRError 型の例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-362">If the argument cannot be converted to the CLRObject type, an exception of the Exception::CLRError type is thrown.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-363">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-363">Examples</span></span>

<span data-ttu-id="20ffe-364">次の例では、文字列値を CLR 文字列オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-364">The following example converts a string value to a CLR string object.</span></span>

    static void Job3(Args _args) 
    { 
        CLRObject clrObj; 
        InteropPermission perm; 
        System.String s; 

        perm = new InteropPermission(InteropKind::ClrInterop); 
        if (perm == null) 
        { 
            return; 
        } 
        perm.assert(); 

        s = CLRInterop::getObjectForAnyType("Calculate total"); 

        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-gettype"></a><span data-ttu-id="20ffe-365">メソッド getType</span><span class="sxs-lookup"><span data-stu-id="20ffe-365">Method getType</span></span>

    public static CLRObject getType(str clrTypeName)

#### <a name="parameters"></a><span data-ttu-id="20ffe-366">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-366">Parameters</span></span>

<span data-ttu-id="20ffe-367">clrTypeName</span><span class="sxs-lookup"><span data-stu-id="20ffe-367">clrTypeName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-368">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-368">Return Value</span></span>

### <a name="method-isnull"></a><span data-ttu-id="20ffe-369">メソッド isNull</span><span class="sxs-lookup"><span data-stu-id="20ffe-369">Method isNull</span></span>

<span data-ttu-id="20ffe-370">指定された CLRObject インスタンスが nullNothingnullptrunita null 参照 (Visual Basic では Nothing) にセットされているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-370">Confirms whether the specified CLRObject instance is set to nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

    public static boolean isNull(CLRObject clrObject)

#### <a name="parameters"></a><span data-ttu-id="20ffe-371">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-371">Parameters</span></span>

<span data-ttu-id="20ffe-372">clrObject</span><span class="sxs-lookup"><span data-stu-id="20ffe-372">clrObject</span></span>  
<span data-ttu-id="20ffe-373">評価する CLRObject インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-373">The CLRObject instance to evaluate.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-374">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-374">Return Value</span></span>

<span data-ttu-id="20ffe-375">指定された CLRObject インスタンスが nullNothingnullptrunita null 参照 (Visual Basic では Nothing) にセットされた場合または初期化されていない場合は true。</span><span class="sxs-lookup"><span data-stu-id="20ffe-375">true if the specified CLRObject instance is set to nullNothingnullptrunita null reference (Nothing in Visual Basic) or has not been initialized.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-376">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-376">Remarks</span></span>

<span data-ttu-id="20ffe-377">CLR データ型が nullNothingnullptrunita null 参照 (Visual Basic では Nothing) であるかどうかを評価する条件ステートメントでは、X++ nullNothingnullptrunita null 参照 (Visual Basic では Nothing) の代わりに isNull メソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-377">The isNull method should be used instead of the X++ nullNothingnullptrunita null reference (Nothing in Visual Basic) in conditional statements that evaluate whether a CLR data type is nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-378">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-378">Examples</span></span>

<span data-ttu-id="20ffe-379">次の例では、CLR 文字列データ型を nullNothingnullptrunita null 参照 (Visual Basic では Nothing) に設定し、タイプ値を CLR オブジェクトに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-379">The following example sets the CLR string data type to nullNothingnullptrunita null reference (Nothing in Visual Basic) and assigns the type value to the CLR object.</span></span> <span data-ttu-id="20ffe-380">isNull メソッドを呼び出し、情報ログに結果を出力します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-380">It then calls the isNull method and prints the result in the Infolog.</span></span>

    static void Job5(Args _args) 
    { 
        System.String nullStr; 

        nullStr = CLRInterop::Null("System.String"); 

        print CLRInterop::isNull(nullStr); 
    }

### <a name="method-null"></a><span data-ttu-id="20ffe-381">メソッド Null</span><span class="sxs-lookup"><span data-stu-id="20ffe-381">Method Null</span></span>

<span data-ttu-id="20ffe-382">nullNothingnullptrunita null 参照 (Visual Basic では Nothing) の値を持つ CLR データ型を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-382">Returns a CLR data type that has a value of nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

    public static CLRObject Null(str clrTypeName)

#### <a name="parameters"></a><span data-ttu-id="20ffe-383">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-383">Parameters</span></span>

<span data-ttu-id="20ffe-384">clrTypeName</span><span class="sxs-lookup"><span data-stu-id="20ffe-384">clrTypeName</span></span>  
<span data-ttu-id="20ffe-385">nullNothingnullptrunita null参照 (Visual Basic では Nothing) に設定する必要がある CLR データ型。</span><span class="sxs-lookup"><span data-stu-id="20ffe-385">The CLR data type to set to nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-386">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-386">Return Value</span></span>

<span data-ttu-id="20ffe-387">指定された CLR データ型の CLRObject インスタンス。</span><span class="sxs-lookup"><span data-stu-id="20ffe-387">A CLRObject instance of the specified CLR data type.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-388">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-388">Remarks</span></span>

<span data-ttu-id="20ffe-389">X++ で CLR データ型を NullNothingnullptrunita null 参照 (Visual Basic では Nothing) に直接設定する場合は、カーネル参照を nullNothingnullptrunita null 参照 (Visual Basic では Nothing) にのみ設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-389">If you directly set CLR data types to nullNothingnullptrunita null reference (Nothing in Visual Basic) in X++, you only set the kernel reference to nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span> <span data-ttu-id="20ffe-390">これにより、CLR データ型として型を使用することができなくなります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-390">This will make it impossible to use the type as a CLR data type.</span></span> <span data-ttu-id="20ffe-391">CLRInterop:null("yourType") に CLR データ型を割り当てると、静的メソッド呼び出しのパラメーターとして、実行時にタイプを解析できます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-391">If you assign the CLR data type to CLRInterop:null("yourType"),, the type can be parsed at run time as a parameter of a static method invocation.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-392">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-392">Examples</span></span>

<span data-ttu-id="20ffe-393">次の例では、CLR 文字列型を nullNothingnullptrunita null 参照 (Visual Basic では Nothing) に設定し、タイプ値を CLR オブジェクトに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-393">The following example sets the CLR string type to nullNothingnullptrunita null reference (Nothing in Visual Basic) and assigns the type value to a CLR object.</span></span>

    static void Job5(Args _args) 
    { 
        System.String nullStr; 

        nullStr = CLRInterop::Null("System.String"); 

        print CLRInterop::isInitialized(nullStr); 
        print CLRInterop::isNull(nullStr); 
    }

### <a name="method-parseclrenum"></a><span data-ttu-id="20ffe-394">メソッド parseClrEnum</span><span class="sxs-lookup"><span data-stu-id="20ffe-394">Method parseClrEnum</span></span>

<span data-ttu-id="20ffe-395">1 つ以上の列挙定数の名前または数値の文字列で表したものを、等価の CLRObject インスタンスに変換します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-395">Converts the string representation of the name or numeric value of one or more enumerated constants to an equivalent CLRObject instance.</span></span>

    public static CLRObject parseClrEnum(str clrEnumTypeName, str enumValues)

#### <a name="parameters"></a><span data-ttu-id="20ffe-396">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-396">Parameters</span></span>

<span data-ttu-id="20ffe-397">clrEnumTypeName</span><span class="sxs-lookup"><span data-stu-id="20ffe-397">clrEnumTypeName</span></span>  
<span data-ttu-id="20ffe-398">変換する名前または値を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="20ffe-398">A string that contains the name or value to convert.</span></span>

<!-- -->

<span data-ttu-id="20ffe-399">enumValues</span><span class="sxs-lookup"><span data-stu-id="20ffe-399">enumValues</span></span>  
<span data-ttu-id="20ffe-400">変換する名前または値を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="20ffe-400">A string that contains the name or value to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-401">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-401">Return Value</span></span>

<span data-ttu-id="20ffe-402">指定した CLR 列挙値を含む CLRObject インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-402">The CLRObject instance that contains the specified CLR enumerator values.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-403">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-403">Remarks</span></span>

<span data-ttu-id="20ffe-404">\_enumValues パラメーターには、値、名前付き定数、またはコンマ (,) で区切られた名前付き定数の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-404">The \_enumValues parameter contains a value, a named constant, or a list of named constants that are delimited by commas (,).</span></span> <span data-ttu-id="20ffe-405">1 つ以上の空白スペースは、\_enumValues の各値、名前、またはコンマの前か後に置くことができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-405">One or more blanks spaces can precede or follow each value, name, or comma in \_enumValues.</span></span> <span data-ttu-id="20ffe-406">\_enumValues が一覧の場合、戻り値は、ビット単位の OR 演算と組み合わされた指定された名前の値です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-406">If \_enumValues is a list, the return value is the value of the specified names combined with a bitwise OR operation.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-407">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-407">Examples</span></span>

<span data-ttu-id="20ffe-408">次の例では、列挙子の値を月曜日の文字列値に変換し、Infolog の値を出力します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-408">The following example converts the enumerator value to the string value of Monday and prints the value in the Infolog.</span></span>

    static void Job6(Args _args) 
    { 
        System.DayOfWeek    dayOfWeek; 
        System.Type         dayOfWeekType; 

        dayOfWeek = CLRInterop::parseClrEnum( "System.DayOfWeek", "Monday"); 

        dayOfWeekType = dayOfWeek.GetType(); 

        info( dayOfWeek.ToString() ); 
    }

### <a name="method-staticinvoke"></a><span data-ttu-id="20ffe-409">メソッド staticInvoke</span><span class="sxs-lookup"><span data-stu-id="20ffe-409">Method staticInvoke</span></span>

<span data-ttu-id="20ffe-410">CLR データ型の静的メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-410">Calls a static method on a CLR data type.</span></span>

    public static CLRObject staticInvoke(str className, str methodName, VarArg params)

#### <a name="parameters"></a><span data-ttu-id="20ffe-411">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-411">Parameters</span></span>

<span data-ttu-id="20ffe-412">className</span><span class="sxs-lookup"><span data-stu-id="20ffe-412">className</span></span>  
<span data-ttu-id="20ffe-413">\_methodName パラメーターで指定されるメソッドの引数 (引数がある場合)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-413">The arguments, if there are any, to the method that is specified in the \_methodName parameter.</span></span>

<!-- -->

<span data-ttu-id="20ffe-414">methodName</span><span class="sxs-lookup"><span data-stu-id="20ffe-414">methodName</span></span>  
<span data-ttu-id="20ffe-415">\_methodName パラメーターで指定されるメソッドの引数 (引数がある場合)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-415">The arguments, if there are any, to the method that is specified in the \_methodName parameter.</span></span>

<!-- -->

<span data-ttu-id="20ffe-416">params</span><span class="sxs-lookup"><span data-stu-id="20ffe-416">params</span></span>  
<span data-ttu-id="20ffe-417">\_methodName パラメーターで指定されるメソッドの引数 (引数がある場合)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-417">The arguments, if there are any, to the method that is specified in the \_methodName parameter.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-418">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-418">Return Value</span></span>

<span data-ttu-id="20ffe-419">静的 CLR メソッドによって返される値を含む CLRObject。それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-419">The CLRObject that contains the value that is returned by the static CLR method; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-420">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-420">Remarks</span></span>

<span data-ttu-id="20ffe-421">攻撃者が staticInvoke メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-421">If an attacker can control input to the staticInvoke method, a security risk exists.</span></span> <span data-ttu-id="20ffe-422">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-422">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="20ffe-423">サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-423">Calls to this method on the server require permission.</span></span> <span data-ttu-id="20ffe-424">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-424">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span> <span data-ttu-id="20ffe-425">get\_Now メソッドを呼び出すときにエラーが発生した場合は、Exception::ClrError 例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-425">If an error occurs when you call the get\_Now method, the Exception::ClrError exception is thrown.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-426">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-426">Examples</span></span>

<span data-ttu-id="20ffe-427">次の例では、System.DateTime CLR クラスの get\_Now メソッドを呼び出し、結果を Infolog に出力します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-427">The following example calls the get\_Now method on the System.DateTime CLR class and prints the results in the Infolog.</span></span>

    static void Job7(Args _args) 
    { 
        CLRObject clrObj; 
        InteropPermission perm; 
        System.DateTime dateTime; 

        perm = new InteropPermission(InteropKind::ClrInterop); 
        if (perm == null) 
        { 
            return; 
        } 
        perm.assert(); 

        dateTime = CLRInterop::staticInvoke( 
                       "System.DateTime", 
                       "get_Now" ); 
        info(dateTime.ToString()); 
        CodeAccessPermission::revertAssert(); 

        pause; 

        // This is the same code using CLR syntax. 
        // dateTime = System.DateTime::get_Now(); 
        // info(dateTime.ToString()); 
    }

### <a name="method-loadassembly"></a><span data-ttu-id="20ffe-428">メソッド loadAssembly</span><span class="sxs-lookup"><span data-stu-id="20ffe-428">Method loadAssembly</span></span>

    public static void loadAssembly(str clrAssemblyName)

#### <a name="parameters"></a><span data-ttu-id="20ffe-429">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-429">Parameters</span></span>

<span data-ttu-id="20ffe-430">clrAssemblyName</span><span class="sxs-lookup"><span data-stu-id="20ffe-430">clrAssemblyName</span></span>  

### <a name="method-new"></a><span data-ttu-id="20ffe-431">メソッド new</span><span class="sxs-lookup"><span data-stu-id="20ffe-431">Method new</span></span>

<span data-ttu-id="20ffe-432">CLRInterop クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-432">Initializes a new instance of the CLRInterop class.</span></span>

    public void new()

#### <a name="remarks"></a><span data-ttu-id="20ffe-433">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-433">Remarks</span></span>

<span data-ttu-id="20ffe-434">CLRInterop クラスのすべてのメンバーは静的です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-434">All members of the CLRInterop class are static.</span></span> <span data-ttu-id="20ffe-435">このクラスをインスタンス化する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-435">There is no requirement to instantiate this class.</span></span> <span data-ttu-id="20ffe-436">攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-436">If an attacker can control input to the new method, a security risk exists.</span></span> <span data-ttu-id="20ffe-437">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-437">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="20ffe-438">サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-438">Calls to this method on the server require permission from the InteropPermission class.</span></span>

## <a name="class-clrobject"></a><span data-ttu-id="20ffe-439">クラス CLRObject</span><span class="sxs-lookup"><span data-stu-id="20ffe-439">Class CLRObject</span></span>
    class CLRObject extends Object

<span data-ttu-id="20ffe-440">CLRObject クラスは、共通言語ランタイム (CLR) オブジェクトのインスタンスへの参照を保持し、X++ からの呼び出しを対応するラップされたマネージド インスタンスにディスパッチします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-440">The CLRObject class holds a reference to an instance of a common language runtime (CLR) object and dispatches calls from X++ to the corresponding wrapped managed instance.</span></span>

### <a name="remarks"></a><span data-ttu-id="20ffe-441">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-441">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-442">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-442">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="20ffe-443">メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-443">Methods</span></span>

| <span data-ttu-id="20ffe-444">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-444">Method</span></span>                                            | <span data-ttu-id="20ffe-445">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-445">Description</span></span>                                   |
|---------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="20ffe-446">private CLRObject dispatch(VarArg )</span><span class="sxs-lookup"><span data-stu-id="20ffe-446">private CLRObject dispatch(VarArg )</span></span>               | <span data-ttu-id="20ffe-447">予約済み: メソッドを明示的に呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-447">Reserved: Do not explicitly call this method.</span></span> |
| <span data-ttu-id="20ffe-448">public void new(str className, \[VarArg params\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-448">public void new(str className, \[VarArg params\])</span></span> | <span data-ttu-id="20ffe-449">CLRObject クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-449">Creates an instance of the CLRObject class.</span></span>   |

### <a name="method-dispatch"></a><span data-ttu-id="20ffe-450">メソッド dispatch</span><span class="sxs-lookup"><span data-stu-id="20ffe-450">Method dispatch</span></span>

<span data-ttu-id="20ffe-451">予約済み: メソッドを明示的に呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-451">Reserved: Do not explicitly call this method.</span></span>

    private CLRObject dispatch(VarArg )

#### <a name="parameters"></a><span data-ttu-id="20ffe-452">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-452">Parameters</span></span>



#### <a name="return-value"></a><span data-ttu-id="20ffe-453">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-453">Return Value</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-454">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-454">Remarks</span></span>

<span data-ttu-id="20ffe-455">攻撃者が出荷メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-455">If an attacker can control input to the dispatch method, a security risk exists.</span></span> <span data-ttu-id="20ffe-456">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-456">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="20ffe-457">サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-457">Calls to this method on the server require permission from the InteropPermission class.</span></span>

### <a name="method-new"></a><span data-ttu-id="20ffe-458">メソッド new</span><span class="sxs-lookup"><span data-stu-id="20ffe-458">Method new</span></span>

<span data-ttu-id="20ffe-459">CLRObject クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-459">Creates an instance of the CLRObject class.</span></span>

    public void new(str className, [VarArg params])

#### <a name="parameters"></a><span data-ttu-id="20ffe-460">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-460">Parameters</span></span>

<span data-ttu-id="20ffe-461">className</span><span class="sxs-lookup"><span data-stu-id="20ffe-461">className</span></span>  
<span data-ttu-id="20ffe-462">インスタンスを作成する CLR クラスのコンストラクターの引数。</span><span class="sxs-lookup"><span data-stu-id="20ffe-462">The arguments for the constructor of the CLR class to instantiate.</span></span>

<!-- -->

<span data-ttu-id="20ffe-463">params</span><span class="sxs-lookup"><span data-stu-id="20ffe-463">params</span></span>  
<span data-ttu-id="20ffe-464">インスタンスを作成する CLR クラスのコンストラクターの引数。</span><span class="sxs-lookup"><span data-stu-id="20ffe-464">The arguments for the constructor of the CLR class to instantiate.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-465">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-465">Remarks</span></span>

<span data-ttu-id="20ffe-466">CLRObject クラスのインスタンスは、CLR メソッドの呼び出しから返される値をラップするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-466">Instances of the CLRObject class are used to wrap values that are returned from calls to CLR methods.</span></span> <span data-ttu-id="20ffe-467">攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-467">If an attacker can control input to the new method, a security risk exists.</span></span> <span data-ttu-id="20ffe-468">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-468">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="20ffe-469">サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-469">Calls to this method on the server require permission from the InteropPermission class.</span></span> <span data-ttu-id="20ffe-470">ユーザーが新しいメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-470">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls the new method.</span></span> <span data-ttu-id="20ffe-471">新しい ClrObject オブジェクトをインスタンス化できない場合、例外: 例外内部はスローします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-471">If a new ClrObject object cannot be instantiated, the Exception:Internal exception is thrown.</span></span> <span data-ttu-id="20ffe-472">元の CLR 例外を取得するには、CLRInterop::getLastException メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-472">To obtain the original CLR exception, call the CLRInterop::getLastException method.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-473">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-473">Examples</span></span>

<span data-ttu-id="20ffe-474">この例では、新しい System.Int32 CLR オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-474">This example creates a new System.Int32 CLR object.</span></span>

    void ClrObjectExample() 
    { 
        CLRObject clrObj; 
        InteropPermission perm; 
        anytype retVal; 

        perm = new InteropPermission(InteropKind::ClrInterop); 
        if (perm == null) 
        { 
            return; 
        } 

        perm.assert(); 

        clrObj = new CLRObject("System.Int32"); 

        CodeAccessPermission::revertAssert(); 
    }

## <a name="class-codeaccesspermission"></a><span data-ttu-id="20ffe-475">クラス CodeAccessPermission</span><span class="sxs-lookup"><span data-stu-id="20ffe-475">Class CodeAccessPermission</span></span>
    class CodeAccessPermission extends Object

<span data-ttu-id="20ffe-476">CodeAccessPermission クラスは、コード アクセス許可の基になる構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-476">The CodeAccessPermission class defines the underlying structure of code access permissions.</span></span>

### <a name="remarks"></a><span data-ttu-id="20ffe-477">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-477">Remarks</span></span>

<span data-ttu-id="20ffe-478">次のクラスは、CodeAccessPermission クラスを拡張します: ExecutePermission、FileIOPermission、InteropPermission、RunAsPermission、SkipAOSValidationPermission、SqlDataDictionaryPermission、SqlStatementExecutePermission、および SysDatabaseLogPermission。</span><span class="sxs-lookup"><span data-stu-id="20ffe-478">The following classes extend the CodeAccessPermission class: ExecutePermission, FileIOPermission, InteropPermission, RunAsPermission, SkipAOSValidationPermission, SqlDataDictionaryPermission, SqlStatementExecutePermission, and SysDatabaseLogPermission.</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-479">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-479">Examples</span></span>

<span data-ttu-id="20ffe-480">次のコード例は、CodeAccessPermission クラスから派生したクラスを示しています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-480">The following code example shows a class that is derived from the CodeAccessPermission class.</span></span>

    final class SysTestCodeAccessPermission extends CodeAccessPermission 
    { 
        str data; 
    }

<span data-ttu-id="20ffe-481">このコード例は、API を保護するプロセスのステップを示しています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-481">This code example illustrates a step in the process of protecting an API.</span></span>

### <a name="methods"></a><span data-ttu-id="20ffe-482">メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-482">Methods</span></span>

| <span data-ttu-id="20ffe-483">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-483">Method</span></span>                                                 | <span data-ttu-id="20ffe-484">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-484">Description</span></span>                                                                                                                                       |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ffe-485">public CodeAccessPermission copy()</span><span class="sxs-lookup"><span data-stu-id="20ffe-485">public CodeAccessPermission copy()</span></span>                     | <span data-ttu-id="20ffe-486">アクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-486">Creates and returns a copy of a permission class object.</span></span>                                                                                          |
| <span data-ttu-id="20ffe-487">public boolean isSubsetOf(CodeAccessPermission target)</span><span class="sxs-lookup"><span data-stu-id="20ffe-487">public boolean isSubsetOf(CodeAccessPermission target)</span></span> | <span data-ttu-id="20ffe-488">現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-488">Determines whether a current permission is a subset of the specified permission when it is overridden by a derived class.</span></span>                         |
| <span data-ttu-id="20ffe-489">public void new()</span><span class="sxs-lookup"><span data-stu-id="20ffe-489">public void new()</span></span>                                      | <span data-ttu-id="20ffe-490">CodeAccessPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-490">Initializes a new instance of the CodeAccessPermission class.</span></span>                                                                                     |
| <span data-ttu-id="20ffe-491">public void assert()</span><span class="sxs-lookup"><span data-stu-id="20ffe-491">public void assert()</span></span>                                   | <span data-ttu-id="20ffe-492">呼び出しコードがアクセス許可によって保護されている API を呼び出すことができることを宣言します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-492">Declares that the calling code can invoke an API that is protected by a permission.</span></span>                                                               |
| <span data-ttu-id="20ffe-493">public void demand()</span><span class="sxs-lookup"><span data-stu-id="20ffe-493">public void demand()</span></span>                                   | <span data-ttu-id="20ffe-494">コール スタックをチェックして、API を呼び出すために必要なアクセス許可が呼び出しコードに与えられているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-494">Checks the call stack to determine whether the permission that is required to invoke an API has been granted to the calling code.</span></span>                 |
| <span data-ttu-id="20ffe-495">::public static void revertAssert()</span><span class="sxs-lookup"><span data-stu-id="20ffe-495">::public static void revertAssert()</span></span>                    | <span data-ttu-id="20ffe-496">CodeAccessPermission.assert および CodeAccessPermission::assertMultiple メソッドへの以前の呼び出しを削除し、無効にします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-496">Causes a previous call to the CodeAccessPermission.assert and CodeAccessPermission::assertMultiple methods to be removed and no longer in effect.</span></span> |
| <span data-ttu-id="20ffe-497">::public static void assertMultiple(Set permissionSet)</span><span class="sxs-lookup"><span data-stu-id="20ffe-497">::public static void assertMultiple(Set permissionSet)</span></span> | <span data-ttu-id="20ffe-498">呼び出しコードが指定されたコレクションでのアクセス許可によって保護されている API を呼び出すことができることを宣言します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-498">Declares that the calling code can invoke an API that is protected by any of the permissions in a specified collection.</span></span>                           |

### <a name="method-copy"></a><span data-ttu-id="20ffe-499">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="20ffe-499">Method copy</span></span>

<span data-ttu-id="20ffe-500">アクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-500">Creates and returns a copy of a permission class object.</span></span>

    public CodeAccessPermission copy()

#### <a name="return-value"></a><span data-ttu-id="20ffe-501">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-501">Return Value</span></span>

<span data-ttu-id="20ffe-502">現在の派生クラスオブジェクトのコピーです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-502">A copy of the derived class object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-503">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-503">Remarks</span></span>

<span data-ttu-id="20ffe-504">API のセキュリティをさらに強化するプロセスの一部として、このメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-504">You can override this method as part of the process of making an API more secure.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-505">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-505">Examples</span></span>

<span data-ttu-id="20ffe-506">次のコード例は、copy メソッドを上書きして、CodeAccessPermission クラスから派生したクラスのコピーを作成して返す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-506">The following code example shows how to override the copy method to create and return a copy of a class that is derived from the CodeAccessPermission class.</span></span>

    public CodeAccessPermission copy() 
    { 
        return new SysTestCodeAccessPermission(_data); 
    }

### <a name="method-issubsetof"></a><span data-ttu-id="20ffe-507">メソッド isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="20ffe-507">Method isSubsetOf</span></span>

<span data-ttu-id="20ffe-508">現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-508">Determines whether a current permission is a subset of the specified permission when it is overridden by a derived class.</span></span>

    public boolean isSubsetOf(CodeAccessPermission target)

#### <a name="parameters"></a><span data-ttu-id="20ffe-509">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-509">Parameters</span></span>

<span data-ttu-id="20ffe-510">target</span><span class="sxs-lookup"><span data-stu-id="20ffe-510">target</span></span>  
<span data-ttu-id="20ffe-511">CodeAccessPermission クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="20ffe-511">A CodeAccessPermission class object.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-512">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-512">Return Value</span></span>

<span data-ttu-id="20ffe-513">現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="20ffe-513">true if a current permission is a subset of a specified permission; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-514">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-514">Remarks</span></span>

<span data-ttu-id="20ffe-515">API のセキュリティをさらに強化するプロセスの一部として、メソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-515">You can override the method as part of the process of making an API more secure.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-516">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-516">Examples</span></span>

<span data-ttu-id="20ffe-517">次の例は、isSubsetOf メソッドを上書きして、現在のオブジェクトに格納されているアクセス権が \_target にあるかどうかを判断する方法を示しています。.</span><span class="sxs-lookup"><span data-stu-id="20ffe-517">The following example shows how to override the isSubsetOf method to determine whether permissions that are stored in the current object are located in \_target.</span></span>

    public boolean isSubsetOf(CodeAccessPermission _target) 
    { 
        SysTestCodeAccessPermission sysTarget = _target; 
        return this.handle() == _target.handle(); 
    }

### <a name="method-new"></a><span data-ttu-id="20ffe-518">メソッド new</span><span class="sxs-lookup"><span data-stu-id="20ffe-518">Method new</span></span>

<span data-ttu-id="20ffe-519">CodeAccessPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-519">Initializes a new instance of the CodeAccessPermission class.</span></span>

    public void new()

### <a name="method-assert"></a><span data-ttu-id="20ffe-520">メソッド assert</span><span class="sxs-lookup"><span data-stu-id="20ffe-520">Method assert</span></span>

<span data-ttu-id="20ffe-521">呼び出しコードがアクセス許可によって保護されている API を呼び出すことができることを宣言します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-521">Declares that the calling code can invoke an API that is protected by a permission.</span></span>

    public void assert()

#### <a name="remarks"></a><span data-ttu-id="20ffe-522">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-522">Remarks</span></span>

<span data-ttu-id="20ffe-523">API を起動する前に、保護された API の派生クラスで assert メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-523">You must call the assert method in the derived class for a protected API before you invoke the API.</span></span> <span data-ttu-id="20ffe-524">アクセス許可によって保護されている API の詳細については、「セキュリティで保護された API」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-524">For more information about APIs that are protected by permissions, see Secured APIs.</span></span> <span data-ttu-id="20ffe-525">保護された API が実行される前に、対応する CodeAccessPermission::demand メソッドが呼び出される、通常はサーバー層である、同じ層で assert メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-525">You must call the assert method on the same tier, usually the server tier, that the corresponding CodeAccessPermission::demand method is called on before the protected API is executed.</span></span> <span data-ttu-id="20ffe-526">次のいずれかでサーバー層のメソッドを呼び出します:</span><span class="sxs-lookup"><span data-stu-id="20ffe-526">Call a method on the server tier from one of the following:</span></span>

-   <span data-ttu-id="20ffe-527">サーバー静的メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-527">A server static method</span></span>
-   <span data-ttu-id="20ffe-528">RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-528">A class instance method that is set to run on the server by using the RunOn class property</span></span>

<span data-ttu-id="20ffe-529">Finance and Operations は、同じ呼び出しコードで、Assert メソッドに対する複数の連続する呼び出しをサポートしません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-529">Finance and Operations does not support multiple, successive calls to the assert method in the same calling code.</span></span> <span data-ttu-id="20ffe-530">assert メソッドへの各呼び出し間で CodeAccessPermission::revertAssert メソッドを呼び出すか、または CodeAccessPermission::assertMultiple メソッドを呼び出すかのいずれかを行います。</span><span class="sxs-lookup"><span data-stu-id="20ffe-530">Either call the CodeAccessPermission::revertAssert method between each call to the assert method, or call the CodeAccessPermission::assertMultiple method.</span></span> <span data-ttu-id="20ffe-531">assertmethod を複数にわたり連続して呼び出すと、コードを実行するときに Infolog によってエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-531">If you make multiple, successive calls to the assertmethod, the Infolog displays an error when you execute the code.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-532">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-532">Examples</span></span>

<span data-ttu-id="20ffe-533">次のコード例は、アクセス許可で保護されている AsciiIo クラスが呼び出される前に assert メソッドを呼び出す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-533">The following code example shows a call to the assert method before the AsciiIo Class class that is protected by a permission is invoked.</span></span> <span data-ttu-id="20ffe-534">assert メソッドは、CodeAccessPermission クラスから派生した FileIOPermission クラスのメンバーです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-534">The assert method is a member of the FileIOPermission class that is derived from the CodeAccessPermission class.</span></span>

    server static void main(Args args) 
    { 
        FileIoPermission _perm; 
        AsciiIo a; 


        _perm = new FileIoPermission("c:\File.txt",'r'); 
        _perm.assert(); 

        // Invoke the protected API. 
        a = new AsciiIo("c:\File.txt",'r'); 
    }

### <a name="method-demand"></a><span data-ttu-id="20ffe-535">メソッド demand</span><span class="sxs-lookup"><span data-stu-id="20ffe-535">Method demand</span></span>

<span data-ttu-id="20ffe-536">コール スタックをチェックして、API を呼び出すために必要なアクセス許可が呼び出しコードに与えられているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-536">Checks the call stack to determine whether the permission that is required to invoke an API has been granted to the calling code.</span></span>

    public void demand()

#### <a name="examples"></a><span data-ttu-id="20ffe-537">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-537">Examples</span></span>

<span data-ttu-id="20ffe-538">次のコード例は、API 機能を実行する前に、API を呼び出すコードに data 変数で指定されたリソースへのアクセス許可が与えられているかどうかを判断するための、demand メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-538">The following code example shows a call to the demand method before the API functionality is executed, to determine whether permission to access the resource that is specified by the data variable has been granted to code that is calling the API.</span></span>

    public static void main(str data) 
    { 
        SysTestCodeAccessPermission p = new SysTestCodeAccessPermission(data); 
        p.demand(); 

        //Add functionality 
    }

<span data-ttu-id="20ffe-539">このコード例は、API を保護するプロセスのステップを示しています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-539">This code example illustrates a step in the process of protecting an API.</span></span>

### <a name="method-revertassert"></a><span data-ttu-id="20ffe-540">メソッド revertAssert</span><span class="sxs-lookup"><span data-stu-id="20ffe-540">Method revertAssert</span></span>

<span data-ttu-id="20ffe-541">CodeAccessPermission.assert および CodeAccessPermission::assertMultiple メソッドへの以前の呼び出しを削除し、無効にします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-541">Causes a previous call to the CodeAccessPermission.assert and CodeAccessPermission::assertMultiple methods to be removed and no longer in effect.</span></span>

    public static void revertAssert()

#### <a name="remarks"></a><span data-ttu-id="20ffe-542">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-542">Remarks</span></span>

<span data-ttu-id="20ffe-543">同じ呼び出しコードで assert メソッドに複数の呼び出しをするときは、それぞれの呼び出しの間に revertAssert メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-543">When you have multiple calls to the assert method in the same calling code, you must call the revertAssert method between each call.</span></span> <span data-ttu-id="20ffe-544">それ以外の場合、情報ログには、コードを実行するときにエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-544">Otherwise, the Infolog displays an error when you execute the code.</span></span> <span data-ttu-id="20ffe-545">assert メソッドを1回だけ呼び出すとき、または CodeAccessPermission::assertMultiple メソッドを呼び出すときは、保護された API の起動後にも revertAssert メソッドを呼び出して、アサートの範囲を制限することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-545">When you call the assert method only one time, or when you call the CodeAccessPermission::assertMultiple method, we recommend that you still call the revertAssert method after you invoke the protected API to limit the scope of the assert.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-546">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-546">Examples</span></span>

<span data-ttu-id="20ffe-547">次のコード例は、ユーザーが CodeAccessPermission.assert メソッドとアクセス許可で保護されている AsciiIo クラスの呼び出しを呼び出した後の、 CodeAccessPermission::revertAssert メソッドへの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-547">The following code example shows a call to the CodeAccessPermission::revertAssert method after the user calls the CodeAccessPermission.assert method and the AsciiIo class that is protected by a permission.</span></span>

    server static void main(Args args) 
    { 
        FileIoPermission _perm; 
        AsciiIo a; 


        _perm = new FileIoPermission("c:\File.txt",'r'); 
        _perm.assert(); 

        //invoke protected API 
        a = new AsciiIo("c:\File.txt",'r'); 

        // Optionally call revertAssert() to limit scope of assert. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-assertmultiple"></a><span data-ttu-id="20ffe-548">メソッド assertMultiple</span><span class="sxs-lookup"><span data-stu-id="20ffe-548">Method assertMultiple</span></span>

<span data-ttu-id="20ffe-549">呼び出しコードが指定されたコレクションでのアクセス許可によって保護されている API を呼び出すことができることを宣言します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-549">Declares that the calling code can invoke an API that is protected by any of the permissions in a specified collection.</span></span>

    public static void assertMultiple(Set permissionSet)

#### <a name="parameters"></a><span data-ttu-id="20ffe-550">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-550">Parameters</span></span>

<span data-ttu-id="20ffe-551">permissionSet</span><span class="sxs-lookup"><span data-stu-id="20ffe-551">permissionSet</span></span>  
<span data-ttu-id="20ffe-552">アクセス許可のコレクションを含むセット クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="20ffe-552">A Set class object that contains a collection of permissions.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-553">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-553">Remarks</span></span>

<span data-ttu-id="20ffe-554">同じ呼び出しコードで CodeAccessPermission.assert および CodeAccessPermission::revertAssert メソッドに対する複数の連続する呼び出しをする代わりに、assertMultple メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-554">You call the assertMultple method instead of making multiple, successive calls to the CodeAccessPermission.assert and CodeAccessPermission::revertAssert methods in the same calling code.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-555">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-555">Examples</span></span>

<span data-ttu-id="20ffe-556">次のコード例は、CodeAccessPermission::assertMultple メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-556">The following code example calls the CodeAccessPermission::assertMultple method.</span></span> <span data-ttu-id="20ffe-557">このコード例は WinAPIServer::createFile メソッドを呼び出します。このメソッド、CodeAccessPermission::assertMultple メソッドへの事前の呼び出しがない場合は失敗します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-557">Then the code example calls the WinAPIServer::createFile method, which would fail without the previous call to the CodeAccessPermission::assertMultple method.</span></span> <span data-ttu-id="20ffe-558">このコード例は、作成する新しいクラスに追加できる静的メソッドです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-558">The code example is a static method that you can add to a new class that you create.</span></span> <span data-ttu-id="20ffe-559">MyClass::RunOnServerPermissionTest のようなコード行を使用して、X++ ジョブから静的メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-559">You can call this static method from an X++ job by using one line of code that resembles MyClass::RunOnServerPermissionTest.</span></span> <span data-ttu-id="20ffe-560">コードの例では、WinAPIServer クラスに、セキュリティで保護されたメソッドがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-560">In the code example, the WinAPIServer class has several secure methods.</span></span> <span data-ttu-id="20ffe-561">WinAPIServer クラスは、クライアント層ではなく、サーバー層で実行されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-561">The WinAPIServer class runs on the server tier, not on the client tier.</span></span> <span data-ttu-id="20ffe-562">したがって、コード例のメソッドはサーバー層でも実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-562">Therefore the code example method must also run on the server tier.</span></span> <span data-ttu-id="20ffe-563">それ以外の場合、クライアント層で実行されたすべてのアクセス許可アサートは、サーバー層で実行されるメソッドにより無視されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-563">Otherwise, any permission asserts that are made on the client tier are ignored by methods that run on the server tier.</span></span> <span data-ttu-id="20ffe-564">このため、サーバー キーワードはコード例のメソッド宣言に含まれています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-564">This is why the server keyword is included in the method declaration of the code example.</span></span> <span data-ttu-id="20ffe-565">メソッドのサーバー キーワードは、クラスで指定された RunOn プロパティ値よりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-565">The server keyword on the method takes precedence over the RunOn property value that is specified on the class.</span></span>

    server
        static public void RunOnServerPermissionTest()
    {
        Set permissionSet;
        str fileName = @"C:\TestFile75a.txt";
        boolean boolFileDeleted;

        permissionSet =  new Set(Types::Class);
        permissionSet.add(new FileIoPermission(fileName,'rw'));

        CodeAccessPermission::assertMultiple(permissionSet);
        //--- Permissions are set, now perform file operations.

        WinAPIServer::createFile(fileName);
        boolFileDeleted = WinAPI::deleteFile(fileName);

        if (boolFileDeleted)
        {
            info("The file was deleted. Good.");
        }
        else
        {
            error("The file was not deleted. Error.");
        }
    }

## <a name="class-com"></a><span data-ttu-id="20ffe-566">クラス COM</span><span class="sxs-lookup"><span data-stu-id="20ffe-566">Class COM</span></span>
    class COM

<span data-ttu-id="20ffe-567">COM クラスは、コンポーネント オブジェクト モデル (COM) オブジェクトを作成するためにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-567">The COM class is used to create Component Object Model (COM) objects.</span></span>

### <a name="remarks"></a><span data-ttu-id="20ffe-568">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-568">Remarks</span></span>

<span data-ttu-id="20ffe-569">COM クラスは、分散コンポーネント オブジェクト モデル (DCOM) もサポートしています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-569">The COM class also supports Distributed Component Object Model (DCOM).</span></span> <span data-ttu-id="20ffe-570">DCOM は、DCOM をサポートするオブジェクトをリモート コンピュータで実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-570">DCOM enables objects that support DCOM to run on remote computers.</span></span> <span data-ttu-id="20ffe-571">COM クラスを使用して COM オブジェクトがインスタンス化されると、そのメソッドおよびプロパティに、COMDispFunction クラスかまたは COM クラスの 拡張構文を使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-571">When a COM object has been instantiated by using the COM class, its methods and properties can be accessed by using either the COMDispFunction class or the extended syntax for the COM class.</span></span> <span data-ttu-id="20ffe-572">拡張構文を使用すると、Lookup リストに表示されていなくても 、メソッドとプロパティを COM オブジェクトで直接呼び出すことができます (例: com.comMethod("Hello World");)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-572">The extended syntax enables methods and properties to be directly called on the COM object, even though they don't appear in the Lookup list (for example, com.comMethod("Hello World");).</span></span> <span data-ttu-id="20ffe-573">拡張構文は、任意の数の引数を取るメソッドとプロパティへの呼び出しをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-573">The extended syntax supports calls to methods and properties that take any number of arguments.</span></span> <span data-ttu-id="20ffe-574">一部の COM オブジェクトは、省略可能な引数の概念をサポートします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-574">Some COM objects support the concept of optional arguments.</span></span> <span data-ttu-id="20ffe-575">オプションのバリアント引数のみ省略できます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-575">Only optional variant arguments can be omitted.</span></span> <span data-ttu-id="20ffe-576">オプションの引数を省略すると、COM オブジェクトは、既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-576">If optional arguments are omitted, the COM object uses its default values.</span></span> <span data-ttu-id="20ffe-577">COM オブジェクトの引数を省略し、強制的に既定値を使用するには、次の例に示すように、COMArgument::NoValue 列挙型を指定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-577">To omit an argument for the COM object and force it to use its default value, specify the COMArgument::NoValue enumeration, as shown in the following example.</span></span>

    com.comMethod(COMArgument::NoValue, "Hello Another World");



<span data-ttu-id="20ffe-578">COM オブジェクトから省略する引数が引数リストの最後に表示される場合は、コードから省略します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-578">If the arguments to omit from the COM object appear at the end of the argument list, omit them from the code.</span></span> <span data-ttu-id="20ffe-579">COM クラスの引数型と戻り値型の拡張構文では、次の型がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-579">The following types are supported for the extended syntax for the COM class argument type and return type:</span></span>

-   <span data-ttu-id="20ffe-580">array</span><span class="sxs-lookup"><span data-stu-id="20ffe-580">array</span></span>
-   <span data-ttu-id="20ffe-581">COM</span><span class="sxs-lookup"><span data-stu-id="20ffe-581">COM</span></span>
-   <span data-ttu-id="20ffe-582">COMVariant</span><span class="sxs-lookup"><span data-stu-id="20ffe-582">COMVariant</span></span>
-   <span data-ttu-id="20ffe-583">日付</span><span class="sxs-lookup"><span data-stu-id="20ffe-583">date</span></span>
-   <span data-ttu-id="20ffe-584">列挙型</span><span class="sxs-lookup"><span data-stu-id="20ffe-584">enum</span></span>
-   <span data-ttu-id="20ffe-585">int</span><span class="sxs-lookup"><span data-stu-id="20ffe-585">int</span></span>
-   <span data-ttu-id="20ffe-586">real</span><span class="sxs-lookup"><span data-stu-id="20ffe-586">real</span></span>
-   <span data-ttu-id="20ffe-587">str</span><span class="sxs-lookup"><span data-stu-id="20ffe-587">str</span></span>

<span data-ttu-id="20ffe-588">COM オブジェクトが日付を返し、拡張構文が使用されている場合は、COM メソッドの戻り値を COM Variant クラス変数に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-588">If a COM object returns a date, and if the extended syntax is used, the return value of the COM method should be assigned to a COMVariant class variable.</span></span> <span data-ttu-id="20ffe-589">そして、日付と時刻のプロパティを使用して、COMVariant クラスから実際の日時 (形式) を抽出することができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-589">The actual date and time (format) can then be extracted from the COMVariant class by using the date and time properties.</span></span> <span data-ttu-id="20ffe-590">日付の戻り値に COMVariant クラスではなく日付変数が割り当てられている場合、日付の時間の部分は失われます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-590">If the date return value is assigned to a date variable instead of a COMVariant class, the time component of the date is lost.</span></span> <span data-ttu-id="20ffe-591">拡張構文を使用するときは、オブジェクトに対して COM クラス メソッド (ルックアップ リストに表示されるメソッド) をまだ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-591">When the extended syntax is used, you can still call the COM class methods (the methods that appear in the Lookup list) on the objects.</span></span> <span data-ttu-id="20ffe-592">COM クラス メソッドは、実際の COM オブジェクトでのメソッドよりも優先順位が高くなります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-592">The COM class methods have a higher priority than the methods on the actual COM object.</span></span> <span data-ttu-id="20ffe-593">COM オブジェクトのメソッドが COM クラスのメソッドと同じ名前 (たとえば、attach) である場合、そのメソッドを COM オブジェクトで呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-593">If a method on the COM object has the same name as a method on the COM class (for example, attach), you cannot call that method on the COM object.</span></span> <span data-ttu-id="20ffe-594">Finance and Operations で、COM クラスで同じ名前を持つメソッドを呼び出すのではなく、COM オブジェクトのメソッドを呼び出せるようにするには、重複するメソッド名の先頭にアンダースコアを付けます (たとえば、com.\_detach();)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-594">To enable Finance and Operations to call the method on the COM object instead of the method that has the same name on the COM class, prefix the duplicate method name with an underscore (for example, com.\_detach();).</span></span> <span data-ttu-id="20ffe-595">COM クラスの拡張構文は、コンパイル時ではなく実行時に評価され、パフォーマンスがわずかに低下します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-595">The extended syntax for the COM class is evaluated at run time, not compile time, which causes a slight decrease in performance.</span></span> <span data-ttu-id="20ffe-596">パフォーマンスの高いコードが必要な場合は、COMDispFunction クラスを使用することを検討します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-596">If high-performance code is required, consider using the COMDispFunction class.</span></span> <span data-ttu-id="20ffe-597">このクラスは、COM クラスの拡張構文よりもパフォーマンスが向上しています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-597">This class offers performance improvements over the extended syntax for the COM class.</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-598">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-598">Examples</span></span>

<span data-ttu-id="20ffe-599">この例では、Scripting.FileSystemObject COM オブジェクトから GetFileName メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-599">This example calls the GetFileName method from the Scripting.FileSystemObject COM object.</span></span>

    void COMExample() 
    { 
        COM               com; 
        str               result; 
        InteropPermission perm; 
        ; 

        // Set code access permission to help protect the use of the 
        // COM object. 
        perm = new InteropPermission(InteropKind::ComInterop); 
        if (perm == null) 
        { 
            return; 
        } 
        // Permission scope starts here. 
        perm.assert(); 

        com = new COM("Scripting.FileSystemObject"); 
        if (com != null) 
        { 
            result = com.GetFileName(@"c:\boot.ini"); 
        } 

        // Close code access permission scope. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="methods"></a><span data-ttu-id="20ffe-600">メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-600">Methods</span></span>

| <span data-ttu-id="20ffe-601">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-601">Method</span></span>                                                                                                      | <span data-ttu-id="20ffe-602">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-602">Description</span></span>                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ffe-603">public AnyType dispatch(VarArg )</span><span class="sxs-lookup"><span data-stu-id="20ffe-603">public AnyType dispatch(VarArg )</span></span>                                                                            | <span data-ttu-id="20ffe-604">予約済み。</span><span class="sxs-lookup"><span data-stu-id="20ffe-604">Reserved.</span></span> <span data-ttu-id="20ffe-605">メソッドを明示的に呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-605">Do not explicitly call this method.</span></span>                                                                                                |
| <span data-ttu-id="20ffe-606">public str documentationName()</span><span class="sxs-lookup"><span data-stu-id="20ffe-606">public str documentationName()</span></span>                                                                              | <span data-ttu-id="20ffe-607">COM クラスのインスタンスに関連付けられている COM オブジェクトの名前を表すテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-607">Returns the textual name of the COM object that is associated with the instance of the COM class.</span></span>                                            |
| <span data-ttu-id="20ffe-608">public COMError error()</span><span class="sxs-lookup"><span data-stu-id="20ffe-608">public COMError error()</span></span>                                                                                     | <span data-ttu-id="20ffe-609">COM クラスのインスタンスに関連付けられている COMError オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-609">Returns a COMError object that is associated with the instance of the COM class.</span></span>                                                             |
| <span data-ttu-id="20ffe-610">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="20ffe-610">public ComInterface interface()</span></span>                                                                             | <span data-ttu-id="20ffe-611">COM オブジェクトに関連付けられているインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-611">Returns the interface that is associated with the COM object.</span></span>                                                                                |
| <span data-ttu-id="20ffe-612">public int lcid(\[int lcid\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-612">public int lcid(\[int lcid\])</span></span>                                                                               |                                                                                                                                              |
| <span data-ttu-id="20ffe-613">public str toString()</span><span class="sxs-lookup"><span data-stu-id="20ffe-613">public str toString()</span></span>                                                                                       | <span data-ttu-id="20ffe-614">COM クラスのインスタンスを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-614">Returns a string that represents the instance of the COM class.</span></span>                                                                              |
| <span data-ttu-id="20ffe-615">::public static COM createFromInterface(ComInterface interface)</span><span class="sxs-lookup"><span data-stu-id="20ffe-615">::public static COM createFromInterface(ComInterface interface)</span></span>                                             | <span data-ttu-id="20ffe-616">指定された COM インターフェイスを使用して COM クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-616">Creates an instance of the COM class by using the specified COM interface.</span></span>                                                                   |
| <span data-ttu-id="20ffe-617">::public static COM createFromObject(COM object)</span><span class="sxs-lookup"><span data-stu-id="20ffe-617">::public static COM createFromObject(COM object)</span></span>                                                            | <span data-ttu-id="20ffe-618">指定された COM オブジェクトを使用して COM クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-618">Creates an instance of the COM class by using the specified COM object.</span></span>                                                                      |
| <span data-ttu-id="20ffe-619">::public static COM createFromVariant(COMVariant variant)</span><span class="sxs-lookup"><span data-stu-id="20ffe-619">::public static COM createFromVariant(COMVariant variant)</span></span>                                                   | <span data-ttu-id="20ffe-620">COMVariant クラスの指定されたインスタンスを使用して、COM クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-620">Creates an instance of the COM class by using the specified instance of the COMVariant class.</span></span>                                                |
| <span data-ttu-id="20ffe-621">::public static COM getObject(str className)</span><span class="sxs-lookup"><span data-stu-id="20ffe-621">::public static COM getObject(str className)</span></span>                                                                | <span data-ttu-id="20ffe-622">実行している COM オブジェクトのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-622">Returns an instance of a COM object that is running.</span></span>                                                                                         |
| <span data-ttu-id="20ffe-623">::public static COM getObjectEx(str fileName)</span><span class="sxs-lookup"><span data-stu-id="20ffe-623">::public static COM getObjectEx(str fileName)</span></span>                                                               | <span data-ttu-id="20ffe-624">ファイル名で指定されている COM オブジェクトのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-624">Returns an instance of a COM object that is specified by its file name.</span></span>                                                                      |
| <span data-ttu-id="20ffe-625">::public static AnyType unsupported(int action, \[AnyType param1\], \[AnyType param2\], \[AnyType param3\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-625">::public static AnyType unsupported(int action, \[AnyType param1\], \[AnyType param2\], \[AnyType param3\])</span></span> | <span data-ttu-id="20ffe-626">予約済み。</span><span class="sxs-lookup"><span data-stu-id="20ffe-626">Reserved.</span></span>                                                                                                                                    |
| <span data-ttu-id="20ffe-627">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="20ffe-627">public void finalize()</span></span>                                                                                      | <span data-ttu-id="20ffe-628">COM クラスのインスタンスに関連付けられているリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-628">Frees resources that are associated with the instance of the COM class.</span></span>                                                                      |
| <span data-ttu-id="20ffe-629">public void new(\[str className\], \[str computerName\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-629">public void new(\[str className\], \[str computerName\])</span></span>                                                    | <span data-ttu-id="20ffe-630">COM クラスに接続できる COM クラスのインスタンスを作成し、オプションで、指定されたコンピュータ上で COM オブジェクトをインスタンス化することができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-630">Creates an instance of the COM class that can be attached to the COM class and optionally instantiates a COM object on a specified computer.</span></span> |
| <span data-ttu-id="20ffe-631">public void attach(ComInterface interface)</span><span class="sxs-lookup"><span data-stu-id="20ffe-631">public void attach(ComInterface interface)</span></span>                                                                  | <span data-ttu-id="20ffe-632">COM クラスのインスタンスを COM インターフェイスに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-632">Attaches an instance of the COM class to a COM interface.</span></span>                                                                                    |
| <span data-ttu-id="20ffe-633">public void detach()</span><span class="sxs-lookup"><span data-stu-id="20ffe-633">public void detach()</span></span>                                                                                        | <span data-ttu-id="20ffe-634">関連付けられているクラスから COM オブジェクトを解除します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-634">Detaches a COM object from the class that it was associated with.</span></span>                                                                            |

### <a name="method-dispatch"></a><span data-ttu-id="20ffe-635">メソッド dispatch</span><span class="sxs-lookup"><span data-stu-id="20ffe-635">Method dispatch</span></span>

<span data-ttu-id="20ffe-636">予約済み。</span><span class="sxs-lookup"><span data-stu-id="20ffe-636">Reserved.</span></span> <span data-ttu-id="20ffe-637">メソッドを明示的に呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-637">Do not explicitly call this method.</span></span>

    public AnyType dispatch(VarArg )

#### <a name="parameters"></a><span data-ttu-id="20ffe-638">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-638">Parameters</span></span>



#### <a name="return-value"></a><span data-ttu-id="20ffe-639">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-639">Return Value</span></span>

### <a name="method-documentationname"></a><span data-ttu-id="20ffe-640">メソッド documentationName</span><span class="sxs-lookup"><span data-stu-id="20ffe-640">Method documentationName</span></span>

<span data-ttu-id="20ffe-641">COM クラスのインスタンスに関連付けられている COM オブジェクトの名前を表すテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-641">Returns the textual name of the COM object that is associated with the instance of the COM class.</span></span>

    public str documentationName()

#### <a name="return-value"></a><span data-ttu-id="20ffe-642">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-642">Return Value</span></span>

<span data-ttu-id="20ffe-643">COM クラスのインスタンスに関連付けられている COM オブジェクトのテキスト名。COM オブジェクトのドキュメント名がない場合は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-643">The textual name of the COM object that is associated with the instance of the COM class; an empty string if there is no documentation name for the COM object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-644">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-644">Remarks</span></span>

<span data-ttu-id="20ffe-645">クラスのテキスト名は、そのクラスを記述するためにクラスによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-645">The textual name of a class is used by the class to describe itself.</span></span> <span data-ttu-id="20ffe-646">テキスト名は、クラスをインスタンス化するために使用されるクラス名とは異なります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-646">The textual name differs from the class name that is used to instantiate the class.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-647">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-647">Examples</span></span>

<span data-ttu-id="20ffe-648">次の例は、COM オブジェクトのドキュメント名を取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-648">The following example shows how to retrieve the documentation name for a COM object.</span></span>

    str docName; 
    ; 
    // The obj that was previously instantiated. 
    docName = obj.documentationName(); 
    info(strfmt("documentationName: %1", docName));

### <a name="method-error"></a><span data-ttu-id="20ffe-649">メソッド error</span><span class="sxs-lookup"><span data-stu-id="20ffe-649">Method error</span></span>

<span data-ttu-id="20ffe-650">COM クラスのインスタンスに関連付けられている COMError オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-650">Returns a COMError object that is associated with the instance of the COM class.</span></span>

    public COMError error()

#### <a name="return-value"></a><span data-ttu-id="20ffe-651">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-651">Return Value</span></span>

<span data-ttu-id="20ffe-652">COM クラスのインスタンスに関連付けられているエラーを表す COMError 値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-652">A COMError value that represents the error that is associated with the instance of the COM class.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-653">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-653">Examples</span></span>

<span data-ttu-id="20ffe-654">次の例は、COM クラスのインスタンスに関連付けられているエラー オブジェクトを取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-654">The following example shows how to retrieve the error object that is associated with an instance of the COM class.</span></span>

    COMError err; 

    // The obj variable was previously instantiated. 
    err = obj.error(); 

    // Output the error number. 
    info(strfmt("Error: %1", err.number()))

### <a name="method-interface"></a><span data-ttu-id="20ffe-655">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="20ffe-655">Method interface</span></span>

<span data-ttu-id="20ffe-656">COM オブジェクトに関連付けられているインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-656">Returns the interface that is associated with the COM object.</span></span>

    public ComInterface interface()

#### <a name="return-value"></a><span data-ttu-id="20ffe-657">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-657">Return Value</span></span>

<span data-ttu-id="20ffe-658">COM オブジェクトに関連付けられているインターフェイス。インターフェイスが COM オブジェクトに関連付けられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-658">The interface that is associated with the COM object; 0 (zero) if no interface is associated with the COM object.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-659">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-659">Examples</span></span>

<span data-ttu-id="20ffe-660">次の例は、COM オブジェクトに関連付けられているインターフェイスを取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-660">The following example shows how to retrieve the interface that is associated with a COM object.</span></span>

    // The obj variable was previously instantiated. 
    info(strfmt("Interface: %1", obj.interface()));

### <a name="method-lcid"></a><span data-ttu-id="20ffe-661">メソッド lcid</span><span class="sxs-lookup"><span data-stu-id="20ffe-661">Method lcid</span></span>

    public int lcid([int lcid])

#### <a name="parameters"></a><span data-ttu-id="20ffe-662">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-662">Parameters</span></span>

<span data-ttu-id="20ffe-663">lcid</span><span class="sxs-lookup"><span data-stu-id="20ffe-663">lcid</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-664">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-664">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="20ffe-665">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="20ffe-665">Method toString</span></span>

<span data-ttu-id="20ffe-666">COM クラスのインスタンスを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-666">Returns a string that represents the instance of the COM class.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="20ffe-667">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-667">Return Value</span></span>

<span data-ttu-id="20ffe-668">COM クラスのインスタンスの説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="20ffe-668">A string that contains a description of the instance of the COM class.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-669">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-669">Examples</span></span>

<span data-ttu-id="20ffe-670">次の例は、toString メソッドの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-670">The following example shows how to use the toString method.</span></span>

    print objCOM.toString();

### <a name="method-createfrominterface"></a><span data-ttu-id="20ffe-671">メソッド createFromInterface</span><span class="sxs-lookup"><span data-stu-id="20ffe-671">Method createFromInterface</span></span>

<span data-ttu-id="20ffe-672">指定された COM インターフェイスを使用して COM クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-672">Creates an instance of the COM class by using the specified COM interface.</span></span>

    public static COM createFromInterface(ComInterface interface)

#### <a name="parameters"></a><span data-ttu-id="20ffe-673">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-673">Parameters</span></span>

<span data-ttu-id="20ffe-674">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="20ffe-674">interface</span></span>  
<span data-ttu-id="20ffe-675">COM クラスの新しいインスタンスを作成するために使用するインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="20ffe-675">The interface to use to create the new instance of the COM class.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-676">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-676">Return Value</span></span>

<span data-ttu-id="20ffe-677">インターフェイス パラメーターで指定される COM インターフェイスの COM クラスのインスタンス。COM クラスのインスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-677">An instance of the COM class for the COM interface that is specified by the interface parameter; nullNothingnullptrunita null reference (Nothing in Visual Basic) if the instance of the COM class could not be created.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-678">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-678">Remarks</span></span>

<span data-ttu-id="20ffe-679">アンマネージ コードに関連したセキュリティ リスクを軽減するには、このメソッドに渡されるオブジェクトを検証し、COM オブジェクトに使用されるすべての DLL がアクセス制御リストによって保護されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-679">To help reduce security risks that are associated with unmanaged code, make sure that you validate the objects that are passed to this method, and that all DLLs used for your COM objects are protected by access control lists.</span></span>

### <a name="method-createfromobject"></a><span data-ttu-id="20ffe-680">メソッド createFromObject</span><span class="sxs-lookup"><span data-stu-id="20ffe-680">Method createFromObject</span></span>

<span data-ttu-id="20ffe-681">指定された COM オブジェクトを使用して COM クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-681">Creates an instance of the COM class by using the specified COM object.</span></span>

    public static COM createFromObject(COM object)

#### <a name="parameters"></a><span data-ttu-id="20ffe-682">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-682">Parameters</span></span>

<span data-ttu-id="20ffe-683">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="20ffe-683">object</span></span>  
<span data-ttu-id="20ffe-684">COM クラスの新しいインスタンスを作成するために使用する COM クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="20ffe-684">The instance of the COM class to use to create the new instance of the COM class.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-685">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-685">Return Value</span></span>

<span data-ttu-id="20ffe-686">オブジェクト パラメーターで指定される COM オブジェクトの COM クラスのインスタンス。COM クラスのインスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-686">An instance of the COM class for the COM object that is specified by the object parameter; nullNothingnullptrunita null reference (Nothing in Visual Basic) if the instance of the COM class could not be created.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-687">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-687">Remarks</span></span>

<span data-ttu-id="20ffe-688">アンマネージ コードに関連したセキュリティ リスクを軽減するには、このメソッドに渡されるオブジェクトを検証し、COM オブジェクトに使用されるすべての DLL がアクセス制御リストによって保護されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-688">To help reduce security risks that are associated with unmanaged code, make sure that you validate the objects that are passed to this method, and that all DLLs used for your COM objects are protected by access control lists.</span></span>

### <a name="method-createfromvariant"></a><span data-ttu-id="20ffe-689">メソッド createFromVariant</span><span class="sxs-lookup"><span data-stu-id="20ffe-689">Method createFromVariant</span></span>

<span data-ttu-id="20ffe-690">COMVariant クラスの指定されたインスタンスを使用して、COM クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-690">Creates an instance of the COM class by using the specified instance of the COMVariant class.</span></span>

    public static COM createFromVariant(COMVariant variant)

#### <a name="parameters"></a><span data-ttu-id="20ffe-691">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-691">Parameters</span></span>

<span data-ttu-id="20ffe-692">バリアント</span><span class="sxs-lookup"><span data-stu-id="20ffe-692">variant</span></span>  
<span data-ttu-id="20ffe-693">COM クラスの新しいインスタンスを作成するために使用する COMVariant クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="20ffe-693">The instance of the COMVariant class to use to create the new instance of the COM class.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-694">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-694">Return Value</span></span>

<span data-ttu-id="20ffe-695">バリアント パラメーターで指定される COM オブジェクトの COM クラスのインスタンス。COM クラスのインスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-695">An instance of the COM class for the COM object that is specified by the variant parameter; nullNothingnullptrunita null reference (Nothing in Visual Basic) if the instance of the COM class could not be created.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-696">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-696">Remarks</span></span>

<span data-ttu-id="20ffe-697">アンマネージ コードに関連したセキュリティ リスクを軽減するには、このメソッドに渡されるオブジェクトを検証し、COM オブジェクトに使用されるすべての DLL がアクセス制御リストによって保護されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-697">To help reduce security risks that are associated with unmanaged code, make sure that you validate the objects that are passed to this method, and that all DLLs used for your COM objects are protected by access control lists.</span></span>

### <a name="method-getobject"></a><span data-ttu-id="20ffe-698">メソッド getObject</span><span class="sxs-lookup"><span data-stu-id="20ffe-698">Method getObject</span></span>

<span data-ttu-id="20ffe-699">実行している COM オブジェクトのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-699">Returns an instance of a COM object that is running.</span></span>

    public static COM getObject(str className)

#### <a name="parameters"></a><span data-ttu-id="20ffe-700">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-700">Parameters</span></span>

<span data-ttu-id="20ffe-701">className</span><span class="sxs-lookup"><span data-stu-id="20ffe-701">className</span></span>  
<span data-ttu-id="20ffe-702">COM クラスのインスタンスを作成するために使用される COM オブジェクトの ProgID 値またはクラス名。</span><span class="sxs-lookup"><span data-stu-id="20ffe-702">The ProgID value or class name of the COM object that is used to create the instance of the COM class.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-703">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-703">Return Value</span></span>

<span data-ttu-id="20ffe-704">className パラメーターで指定されるクラスの COM クラスのインスタンス。インスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-704">An instance of the COM class for the class that is specified by the className parameter; nullNothingnullptrunita null reference (Nothing in Visual Basic) if the instance could not be created.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-705">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-705">Remarks</span></span>

<span data-ttu-id="20ffe-706">指定した COM オブジェクトの複数インスタンスが実行している場合は、getObject メソッドによってどのインスタンスが返されるかを保証できません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-706">If multiple instances of the specified COM object are running, we cannot guarantee which instance will be returned by the getObject method.</span></span> <span data-ttu-id="20ffe-707">一部の COM オブジェクトは、このメソッドの呼び出しを可能にする拡張機能をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-707">Some COM objects do not support the extended features that enable calls to this method.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-708">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-708">Examples</span></span>

<span data-ttu-id="20ffe-709">次の例は、実行中の COM オブジェクトのインスタンスを取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-709">The following example shows how to retrieve an instance of a running COM object.</span></span>

    COM objExcel, objWorkBook, objWorkBooks; 
    InteropPermission perm; 

    // Set code access permission to help protect the use of COM.new. 
    perm = new InteropPermission(InteropKind::ComInterop); 
    perm.assert(); 

    objExcel = COM::getObject("Excel.Application"); 

    if (!objExcel) 
    { 
        // Unable to connect to a running instance of Microsoft Excel. 
        // Try starting it. 
        objExcel = new COM("Excel.Application"); 
        if (!objExcel) 
        { 
            Info ("Unable to find or create an instance of Excel"); 
            return;  // Or other error action. 
        }  
    } 
    // Close code access permission scope. 
    CodeAccessPermission::revertAssert(); 

    objExcel.visible(true); 
    objWorkBooks = objExcel.workbooks(); 
    if (objWorkBooks) 
    { 
        objWorkBook = objWorkBooks.open("d:\mydata\book1.xls"); 
    }

### <a name="method-getobjectex"></a><span data-ttu-id="20ffe-710">メソッド getObjectEx</span><span class="sxs-lookup"><span data-stu-id="20ffe-710">Method getObjectEx</span></span>

<span data-ttu-id="20ffe-711">ファイル名で指定されている COM オブジェクトのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-711">Returns an instance of a COM object that is specified by its file name.</span></span>

    public static COM getObjectEx(str fileName)

#### <a name="parameters"></a><span data-ttu-id="20ffe-712">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-712">Parameters</span></span>

<span data-ttu-id="20ffe-713">fileName</span><span class="sxs-lookup"><span data-stu-id="20ffe-713">fileName</span></span>  
<span data-ttu-id="20ffe-714">COM クラスのインスタンスを作成するために使用される COM オブジェクトの機能を提供するファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="20ffe-714">The name of the file that provides the functionality for the COM object that is used to create the instance of the COM class.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-715">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-715">Return Value</span></span>

<span data-ttu-id="20ffe-716">filename パラメーターで指定される COM クラスのインスタンス。インスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-716">An instance of the COM class that is specified by the filename parameter; nullNothingnullptrunita null reference (Nothing in Visual Basic) if the instance could not be created.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-717">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-717">Remarks</span></span>

<span data-ttu-id="20ffe-718">アンマネージ コードに関連したセキュリティ リスクを軽減するには、このメソッドに渡されるオブジェクトを検証し、COM オブジェクトに使用されるすべての DLL がアクセス制御リストによって保護されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-718">To help reduce security risks that are associated with unmanaged code, make sure that you validate the objects that are passed to this method, and that all DLLs used for your COM objects are protected by access control lists.</span></span>

### <a name="method-unsupported"></a><span data-ttu-id="20ffe-719">メソッド unsupported</span><span class="sxs-lookup"><span data-stu-id="20ffe-719">Method unsupported</span></span>

<span data-ttu-id="20ffe-720">予約済み。</span><span class="sxs-lookup"><span data-stu-id="20ffe-720">Reserved.</span></span>

    public static AnyType unsupported(int action, [AnyType param1], [AnyType param2], [AnyType param3])

#### <a name="parameters"></a><span data-ttu-id="20ffe-721">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-721">Parameters</span></span>

<span data-ttu-id="20ffe-722">アクション</span><span class="sxs-lookup"><span data-stu-id="20ffe-722">action</span></span>  

<!-- -->

<span data-ttu-id="20ffe-723">param1</span><span class="sxs-lookup"><span data-stu-id="20ffe-723">param1</span></span>  

<!-- -->

<span data-ttu-id="20ffe-724">param2</span><span class="sxs-lookup"><span data-stu-id="20ffe-724">param2</span></span>  

<!-- -->

<span data-ttu-id="20ffe-725">param3</span><span class="sxs-lookup"><span data-stu-id="20ffe-725">param3</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-726">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-726">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="20ffe-727">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="20ffe-727">Method finalize</span></span>

<span data-ttu-id="20ffe-728">COM クラスのインスタンスに関連付けられているリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-728">Frees resources that are associated with the instance of the COM class.</span></span>

    public void finalize()

#### <a name="examples"></a><span data-ttu-id="20ffe-729">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-729">Examples</span></span>

<span data-ttu-id="20ffe-730">次の例では、finalize メソッドの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-730">The following example how to use the finalize method.</span></span>

    objCOM.finalize();

### <a name="method-new"></a><span data-ttu-id="20ffe-731">メソッド new</span><span class="sxs-lookup"><span data-stu-id="20ffe-731">Method new</span></span>

<span data-ttu-id="20ffe-732">COM クラスに接続できる COM クラスのインスタンスを作成し、オプションで、指定されたコンピュータ上で COM オブジェクトをインスタンス化することができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-732">Creates an instance of the COM class that can be attached to the COM class and optionally instantiates a COM object on a specified computer.</span></span>

    public void new([str className], [str computerName])

#### <a name="parameters"></a><span data-ttu-id="20ffe-733">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-733">Parameters</span></span>

<span data-ttu-id="20ffe-734">className</span><span class="sxs-lookup"><span data-stu-id="20ffe-734">className</span></span>  
<span data-ttu-id="20ffe-735">COM オブジェクトをインスタンス化するリモート コンピューターの名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-735">The name of the remote computer on which to instantiate the COM object; optional.</span></span> <span data-ttu-id="20ffe-736">このパラメータを省略すると、COM オブジェクトはローカル コンピューターでインスタンス化されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-736">If this parameter is omitted, the COM object is instantiated on the local computer.</span></span> <span data-ttu-id="20ffe-737">コンピューター名が指定されている場合は、ローカル コンピューターとリモート コンピューターの両方に DCOM システムのコンポーネントをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-737">If the computer name is specified, the DCOM system component must be installed on both the local computer and the remote computer.</span></span> <span data-ttu-id="20ffe-738">特定の COM オブジェクトは DCOM をサポートする必要があり、ローカル コンピューターとリモート コンピューターの両方で正しく構成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-738">The specific COM object must support DCOM, and it must be correctly configured on both the local computer and the remote computer.</span></span> <span data-ttu-id="20ffe-739">システム コンポーネントは、Microsoft Windows 98、Windows NT、およびそれ以降のバージョンの標準コンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-739">The system component is a standard component of Microsoft Windows 98, Windows NT, and later versions.</span></span> <span data-ttu-id="20ffe-740">Windows 95 では、DCOM システム コンポーネントをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-740">In Windows 95, the DCOM system component must be installed.</span></span>

<!-- -->

<span data-ttu-id="20ffe-741">computerName</span><span class="sxs-lookup"><span data-stu-id="20ffe-741">computerName</span></span>  
<span data-ttu-id="20ffe-742">COM オブジェクトをインスタンス化するリモート コンピューターの名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-742">The name of the remote computer on which to instantiate the COM object; optional.</span></span> <span data-ttu-id="20ffe-743">このパラメータを省略すると、COM オブジェクトはローカル コンピューターでインスタンス化されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-743">If this parameter is omitted, the COM object is instantiated on the local computer.</span></span> <span data-ttu-id="20ffe-744">コンピューター名が指定されている場合は、ローカル コンピューターとリモート コンピューターの両方に DCOM システムのコンポーネントをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-744">If the computer name is specified, the DCOM system component must be installed on both the local computer and the remote computer.</span></span> <span data-ttu-id="20ffe-745">特定の COM オブジェクトは DCOM をサポートする必要があり、ローカル コンピューターとリモート コンピューターの両方で正しく構成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-745">The specific COM object must support DCOM, and it must be correctly configured on both the local computer and the remote computer.</span></span> <span data-ttu-id="20ffe-746">システム コンポーネントは、Microsoft Windows 98、Windows NT、およびそれ以降のバージョンの標準コンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-746">The system component is a standard component of Microsoft Windows 98, Windows NT, and later versions.</span></span> <span data-ttu-id="20ffe-747">Windows 95 では、DCOM システム コンポーネントをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-747">In Windows 95, the DCOM system component must be installed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-748">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-748">Remarks</span></span>

<span data-ttu-id="20ffe-749">COM オブジェクトのクラス名は、そのプログラム識別子 (ProgID) またはそのクラス識別子 (CLSID) です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-749">The class name of a COM object is either its programmatic identifier (ProgID) or its class identifier (CLSID):</span></span>

-   <span data-ttu-id="20ffe-750">ProgID の形式: program.component.version</span><span class="sxs-lookup"><span data-stu-id="20ffe-750">ProgIDs have the following format: program.component.version</span></span>
-   <span data-ttu-id="20ffe-751">ClSID は 128 ビット値であり、その形式は {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-751">CLSIDs are 128-bit values and have the following format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span>

<span data-ttu-id="20ffe-752">攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-752">If an attacker can control input to the new method, a security risk exists.</span></span> <span data-ttu-id="20ffe-753">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-753">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="20ffe-754">サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-754">Calls to this method on the server require permission from the InteropPermission class.</span></span> <span data-ttu-id="20ffe-755">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-755">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-756">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-756">Examples</span></span>

<span data-ttu-id="20ffe-757">この例では、Scripting.FileSystemObject COM オブジェクトから GetFileName メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-757">This example calls the GetFileName method from the Scripting.FileSystemObject COM object.</span></span>

    void COMExample() 
    { 
        COM               com; 
        str               result; 
        InteropPermission perm; 

        // Set the code access permission to help protect the use of the 
        // COM object. 
        perm = new InteropPermission(InteropKind::ComInterop); 
        if (perm == null) 
        { 
            return; 
        } 
        // Permission scope starts here. 
        perm.assert(); 

        com = new COM("Scripting.FileSystemObject"); 
        if (com != null) 
        { 
            result = com.GetFileName(@"c:\boot.ini"); 
        } 

        // Close the code access permission scope. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-attach"></a><span data-ttu-id="20ffe-758">メソッド attach</span><span class="sxs-lookup"><span data-stu-id="20ffe-758">Method attach</span></span>

<span data-ttu-id="20ffe-759">COM クラスのインスタンスを COM インターフェイスに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-759">Attaches an instance of the COM class to a COM interface.</span></span>

    public void attach(ComInterface interface)

#### <a name="parameters"></a><span data-ttu-id="20ffe-760">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-760">Parameters</span></span>

<span data-ttu-id="20ffe-761">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="20ffe-761">interface</span></span>  
<span data-ttu-id="20ffe-762">COM クラスのインスタンスに関連付けるインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="20ffe-762">The interface to attach to the instance of the COM class.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-763">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-763">Remarks</span></span>

<span data-ttu-id="20ffe-764">このメソッドは、一部の COM オブジェクトは他の COM オブジェクトによってのみインスタンス化されるが、COM クラスによって直接インスタンス化することができないため、用意されています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-764">This method is provided because some COM objects can be instantiated only by other COM objects and cannot be instantiated directly by the COM class.</span></span>

### <a name="method-detach"></a><span data-ttu-id="20ffe-765">メソッド detach</span><span class="sxs-lookup"><span data-stu-id="20ffe-765">Method detach</span></span>

<span data-ttu-id="20ffe-766">関連付けられているクラスから COM オブジェクトを解除します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-766">Detaches a COM object from the class that it was associated with.</span></span>

    public void detach()

#### <a name="remarks"></a><span data-ttu-id="20ffe-767">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-767">Remarks</span></span>

<span data-ttu-id="20ffe-768">たとえば、このメソッドは、接続または新しいメソッドの呼び出しから COM オブジェクトを切り離すために呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-768">For example, this method can be called to detach a COM object from a call to the attach or new method.</span></span>

## <a name="class-comdispfunction"></a><span data-ttu-id="20ffe-769">クラス COMDispFunction</span><span class="sxs-lookup"><span data-stu-id="20ffe-769">Class COMDispFunction</span></span>
    class COMDispFunction extends Object

### <a name="remarks"></a><span data-ttu-id="20ffe-770">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-770">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-771">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-771">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="20ffe-772">メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-772">Methods</span></span>

| <span data-ttu-id="20ffe-773">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-773">Method</span></span>                                                                   | <span data-ttu-id="20ffe-774">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-774">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ffe-775">public int call(VarArg )</span><span class="sxs-lookup"><span data-stu-id="20ffe-775">public int call(VarArg )</span></span>                                                 |                                                                                                      |
| <span data-ttu-id="20ffe-776">public AnyType callContainerOfParms(container parms)</span><span class="sxs-lookup"><span data-stu-id="20ffe-776">public AnyType callContainerOfParms(container parms)</span></span>                     |                                                                                                      |
| <span data-ttu-id="20ffe-777">public str toString()</span><span class="sxs-lookup"><span data-stu-id="20ffe-777">public str toString()</span></span>                                                    | <span data-ttu-id="20ffe-778">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-778">Returns a string that represents the current object.</span></span>                                                 |
| <span data-ttu-id="20ffe-779">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="20ffe-779">public void finalize()</span></span>                                                   |                                                                                                      |
| <span data-ttu-id="20ffe-780">public void new(COM comObject, str functionName, COMDispContext context)</span><span class="sxs-lookup"><span data-stu-id="20ffe-780">public void new(COM comObject, str functionName, COMDispContext context)</span></span> | <span data-ttu-id="20ffe-781">オートメーション オブジェクトの機能にアクセスするために使用される COMDispFunction オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-781">Creates a COMDispFunction object, which is used to access the functionality in an Automation object.</span></span> |

### <a name="method-call"></a><span data-ttu-id="20ffe-782">メソッド call</span><span class="sxs-lookup"><span data-stu-id="20ffe-782">Method call</span></span>

    public int call(VarArg )

#### <a name="parameters"></a><span data-ttu-id="20ffe-783">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-783">Parameters</span></span>



#### <a name="return-value"></a><span data-ttu-id="20ffe-784">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-784">Return Value</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-785">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-785">Remarks</span></span>

<span data-ttu-id="20ffe-786">攻撃者が呼び出しメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-786">If an attacker can control input to the call method, a security risk exists.</span></span> <span data-ttu-id="20ffe-787">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-787">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="20ffe-788">サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-788">Calls to this method on the server require permission from the InteropPermission class.</span></span> <span data-ttu-id="20ffe-789">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-789">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

### <a name="method-callcontainerofparms"></a><span data-ttu-id="20ffe-790">メソッド callContainerOfParms</span><span class="sxs-lookup"><span data-stu-id="20ffe-790">Method callContainerOfParms</span></span>

    public AnyType callContainerOfParms(container parms)

#### <a name="parameters"></a><span data-ttu-id="20ffe-791">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-791">Parameters</span></span>

<span data-ttu-id="20ffe-792">parms</span><span class="sxs-lookup"><span data-stu-id="20ffe-792">parms</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-793">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-793">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="20ffe-794">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="20ffe-794">Method toString</span></span>

<span data-ttu-id="20ffe-795">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-795">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="20ffe-796">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-796">Return Value</span></span>

<span data-ttu-id="20ffe-797">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="20ffe-797">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-798">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-798">Remarks</span></span>

<span data-ttu-id="20ffe-799">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-799">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="20ffe-800">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-800">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="20ffe-801">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-801">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

### <a name="method-finalize"></a><span data-ttu-id="20ffe-802">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="20ffe-802">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="20ffe-803">メソッド new</span><span class="sxs-lookup"><span data-stu-id="20ffe-803">Method new</span></span>

<span data-ttu-id="20ffe-804">オートメーション オブジェクトの機能にアクセスするために使用される COMDispFunction オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-804">Creates a COMDispFunction object, which is used to access the functionality in an Automation object.</span></span>

    public void new(COM comObject, str functionName, COMDispContext context)

#### <a name="parameters"></a><span data-ttu-id="20ffe-805">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-805">Parameters</span></span>

<span data-ttu-id="20ffe-806">comObject</span><span class="sxs-lookup"><span data-stu-id="20ffe-806">comObject</span></span>  
<span data-ttu-id="20ffe-807">アクセスする機能のコンテキスト。</span><span class="sxs-lookup"><span data-stu-id="20ffe-807">The context of the functionality to access.</span></span> <span data-ttu-id="20ffe-808">次の値が使用されます: COMDispContext::METHOD、COMDispContext::PROPERTYGET、COMDispContext::PROPERTYPUT、および COMDispContext::PROPERTYPUTREF</span><span class="sxs-lookup"><span data-stu-id="20ffe-808">The following values are used: COMDispContext::METHOD, COMDispContext::PROPERTYGET, COMDispContext::PROPERTYPUT, and COMDispContext::PROPERTYPUTREF</span></span>

<!-- -->

<span data-ttu-id="20ffe-809">functionName</span><span class="sxs-lookup"><span data-stu-id="20ffe-809">functionName</span></span>  
<span data-ttu-id="20ffe-810">アクセスする機能のコンテキスト。</span><span class="sxs-lookup"><span data-stu-id="20ffe-810">The context of the functionality to access.</span></span> <span data-ttu-id="20ffe-811">次の値が使用されます: COMDispContext::METHOD、COMDispContext::PROPERTYGET、COMDispContext::PROPERTYPUT、および COMDispContext::PROPERTYPUTREF</span><span class="sxs-lookup"><span data-stu-id="20ffe-811">The following values are used: COMDispContext::METHOD, COMDispContext::PROPERTYGET, COMDispContext::PROPERTYPUT, and COMDispContext::PROPERTYPUTREF</span></span>

<!-- -->

<span data-ttu-id="20ffe-812">context</span><span class="sxs-lookup"><span data-stu-id="20ffe-812">context</span></span>  
<span data-ttu-id="20ffe-813">アクセスする機能のコンテキスト。</span><span class="sxs-lookup"><span data-stu-id="20ffe-813">The context of the functionality to access.</span></span> <span data-ttu-id="20ffe-814">次の値が使用されます: COMDispContext::METHOD、COMDispContext::PROPERTYGET、COMDispContext::PROPERTYPUT、および COMDispContext::PROPERTYPUTREF</span><span class="sxs-lookup"><span data-stu-id="20ffe-814">The following values are used: COMDispContext::METHOD, COMDispContext::PROPERTYGET, COMDispContext::PROPERTYPUT, and COMDispContext::PROPERTYPUTREF</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-815">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-815">Remarks</span></span>

<span data-ttu-id="20ffe-816">COM オブジェクトは、同じ名前を使用する最大 4 つの機能を指定できるので、アクセスする COM オブジェクトで機能の正しいコンテキストを指定することが重要です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-816">It is important that you specify the correct context of the functionality in the COM object that you want to access, because a COM object can supply up to four functions that use the same name.</span></span> <span data-ttu-id="20ffe-817">使用可能な名前の衝突のため、コンテキストはメソッドまたはプロパティを区別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-817">Because of the possible name clashing, the context is used to distinguish the method or properties.</span></span> <span data-ttu-id="20ffe-818">正しいコンテキストを指定するには、アクセスする COM オブジェクトのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-818">To specify the correct context, see the documentation for the COM object that you want to access.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-819">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-819">Examples</span></span>



    { 
        InteropPermission perm; 
        COM com; 
        COMDispFunction funcShow; 
        COMDispFunction getValue; 
        COMDispFunction putValue; 
        ; 

        perm = new InteropPermission(InteropKind::ComInterop); 
        perm.assert(); 
        com = new COM("MyCOM.Object"); 
        funcShow = 
            new COMDispFunction(com, "show",  COMDispContext::METHOD); 
        getValue = 
            new COMDispFunction(com, "value", COMDispContext::PROPERTYGET); 
        putValue = 
            new COMDispFunction(com, "value", COMDispContext::PROPERTYPUT); 
    }

## <a name="class-comerror"></a><span data-ttu-id="20ffe-820">クラス COMError</span><span class="sxs-lookup"><span data-stu-id="20ffe-820">Class COMError</span></span>
    class COMError extends Object

<span data-ttu-id="20ffe-821">COMError クラスは、COM メソッド呼び出し時に発生するすべての COM エラーをラップします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-821">The COMError class wraps any COM errors that occur during a COM method call.</span></span>

### <a name="remarks"></a><span data-ttu-id="20ffe-822">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-822">Remarks</span></span>

<span data-ttu-id="20ffe-823">COM メソッド呼び出し中にエラーが発生すると、エラー コードとエラーの説明が COMError オブジェクトに格納されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-823">When an error occurs during a COM method call, the error code and the error description are stored in the COMError object.</span></span> <span data-ttu-id="20ffe-824">COM クラスに関連付けられている COMError オブジェクトは、COM.error メソッドを使用して COM クラスから取得されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-824">The COMError object that is associated with a COM class is retrieved from the COM class by using the COM.error method.</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-825">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-825">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="20ffe-826">メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-826">Methods</span></span>

| <span data-ttu-id="20ffe-827">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-827">Method</span></span>                   | <span data-ttu-id="20ffe-828">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-828">Description</span></span>                                                                                                               |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ffe-829">public str description()</span><span class="sxs-lookup"><span data-stu-id="20ffe-829">public str description()</span></span> | <span data-ttu-id="20ffe-830">COM オブジェクトが呼び出されたときに発生したエラーの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-830">Returns a description of the error that occurred when the COM object was called.</span></span>                                          |
| <span data-ttu-id="20ffe-831">public int helpContext()</span><span class="sxs-lookup"><span data-stu-id="20ffe-831">public int helpContext()</span></span> | <span data-ttu-id="20ffe-832">COM オブジェクトが呼び出されたときに発生したエラーのヘルプ コンテキスト ID を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-832">Returns the Help context ID for the error that occurred when the COM object was called.</span></span>                                   |
| <span data-ttu-id="20ffe-833">public str helpFile()</span><span class="sxs-lookup"><span data-stu-id="20ffe-833">public str helpFile()</span></span>    | <span data-ttu-id="20ffe-834">COM オブジェクトが呼び出されたときに発生したエラーに関する情報が含まれるヘルプ ファイルの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-834">Returns the name of the Help file that contains information about the error that occurred when the COM object was called.</span></span> |
| <span data-ttu-id="20ffe-835">public int number()</span><span class="sxs-lookup"><span data-stu-id="20ffe-835">public int number()</span></span>      | <span data-ttu-id="20ffe-836">COM オブジェクトが呼び出されたときに発生したエラーのエラー コードを返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-836">Returns the error code of the error that occurred when the COM object was called.</span></span>                                         |
| <span data-ttu-id="20ffe-837">public str source()</span><span class="sxs-lookup"><span data-stu-id="20ffe-837">public str source()</span></span>      | <span data-ttu-id="20ffe-838">COM オブジェクトが呼び出されたときに発生したエラーを引き起こしたコンポーネントの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-838">Returns the name of the component that caused the error that occurred when the COM object was called.</span></span>                     |
| <span data-ttu-id="20ffe-839">public str toString()</span><span class="sxs-lookup"><span data-stu-id="20ffe-839">public str toString()</span></span>    | <span data-ttu-id="20ffe-840">クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-840">Returns a string that contains the class handle and name, and sometimes additional information.</span></span>                           |
| <span data-ttu-id="20ffe-841">public void clear()</span><span class="sxs-lookup"><span data-stu-id="20ffe-841">public void clear()</span></span>      | <span data-ttu-id="20ffe-842">COMError オブジェクトのプロパティをクリアします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-842">Clears the properties of the COMError object.</span></span>                                                                             |
| <span data-ttu-id="20ffe-843">public void new()</span><span class="sxs-lookup"><span data-stu-id="20ffe-843">public void new()</span></span>        | <span data-ttu-id="20ffe-844">COMError クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-844">Initializes an instance of the COMError class.</span></span>                                                                            |
| <span data-ttu-id="20ffe-845">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="20ffe-845">public void finalize()</span></span>   |                                                                                                                           |

### <a name="method-description"></a><span data-ttu-id="20ffe-846">メソッドの説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-846">Method description</span></span>

<span data-ttu-id="20ffe-847">COM オブジェクトが呼び出されたときに発生したエラーの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-847">Returns a description of the error that occurred when the COM object was called.</span></span>

    public str description()

#### <a name="return-value"></a><span data-ttu-id="20ffe-848">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-848">Return Value</span></span>

<span data-ttu-id="20ffe-849">エラーの説明です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-849">The error description.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-850">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-850">Remarks</span></span>

<span data-ttu-id="20ffe-851">COM オブジェクトがテキストのエラー メッセージの手渡しをサポートしていない場合は、説明が空白になることがあります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-851">The description might be empty if the COM object does not support handing out textual error messages.</span></span> <span data-ttu-id="20ffe-852">説明のプロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-852">The description property is read-only.</span></span>

### <a name="method-helpcontext"></a><span data-ttu-id="20ffe-853">メソッド helpContext</span><span class="sxs-lookup"><span data-stu-id="20ffe-853">Method helpContext</span></span>

<span data-ttu-id="20ffe-854">COM オブジェクトが呼び出されたときに発生したエラーのヘルプ コンテキスト ID を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-854">Returns the Help context ID for the error that occurred when the COM object was called.</span></span>

    public int helpContext()

#### <a name="return-value"></a><span data-ttu-id="20ffe-855">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-855">Return Value</span></span>

<span data-ttu-id="20ffe-856">ヘルプ コンテキスト ID。</span><span class="sxs-lookup"><span data-stu-id="20ffe-856">The Help context ID.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-857">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-857">Remarks</span></span>

<span data-ttu-id="20ffe-858">ヘルプ コンテキスト ID は、COM オブジェクトがエラーのヘルプをサポートしていない場合、0 (ゼロ) にすることができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-858">The Help context ID might be 0 (zero) if the COM object does not support Help for its errors.</span></span> <span data-ttu-id="20ffe-859">helpContext プロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-859">The helpContext property is read-only.</span></span>

### <a name="method-helpfile"></a><span data-ttu-id="20ffe-860">メソッド helpFile</span><span class="sxs-lookup"><span data-stu-id="20ffe-860">Method helpFile</span></span>

<span data-ttu-id="20ffe-861">COM オブジェクトが呼び出されたときに発生したエラーに関する情報が含まれるヘルプ ファイルの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-861">Returns the name of the Help file that contains information about the error that occurred when the COM object was called.</span></span>

    public str helpFile()

#### <a name="return-value"></a><span data-ttu-id="20ffe-862">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-862">Return Value</span></span>

<span data-ttu-id="20ffe-863">ヘルプ ファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="20ffe-863">The name of the Help file.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-864">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-864">Remarks</span></span>

<span data-ttu-id="20ffe-865">ヘルプ ファイルは、COM オブジェクトがエラーのヘルプをサポートしていない場合、空にすることができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-865">The Help file might be empty if the COM object does not support Help for its errors.</span></span> <span data-ttu-id="20ffe-866">helpFile プロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-866">The helpFile property is read-only.</span></span>

### <a name="method-number"></a><span data-ttu-id="20ffe-867">メソッド number</span><span class="sxs-lookup"><span data-stu-id="20ffe-867">Method number</span></span>

<span data-ttu-id="20ffe-868">COM オブジェクトが呼び出されたときに発生したエラーのエラー コードを返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-868">Returns the error code of the error that occurred when the COM object was called.</span></span>

    public int number()

#### <a name="return-value"></a><span data-ttu-id="20ffe-869">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-869">Return Value</span></span>

<span data-ttu-id="20ffe-870">エラーコード。COM オブジェクトが呼び出されたときにエラーが発生しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-870">The error code; 0 (zero) if no error occurred when the COM object was called.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-871">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-871">Remarks</span></span>

<span data-ttu-id="20ffe-872">数プロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-872">The number property is read-only.</span></span>

### <a name="method-source"></a><span data-ttu-id="20ffe-873">メソッド source</span><span class="sxs-lookup"><span data-stu-id="20ffe-873">Method source</span></span>

<span data-ttu-id="20ffe-874">COM オブジェクトが呼び出されたときに発生したエラーを引き起こしたコンポーネントの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-874">Returns the name of the component that caused the error that occurred when the COM object was called.</span></span>

    public str source()

#### <a name="return-value"></a><span data-ttu-id="20ffe-875">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-875">Return Value</span></span>

<span data-ttu-id="20ffe-876">エラーのソース。</span><span class="sxs-lookup"><span data-stu-id="20ffe-876">The source of the error.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-877">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-877">Remarks</span></span>

<span data-ttu-id="20ffe-878">COM オブジェクトがエラーのソースの手渡しをサポートしていない場合は、ソースが空白になることがあります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-878">The source might be empty if the COM object does not support handing out the source of the error.</span></span> <span data-ttu-id="20ffe-879">ソースのプロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-879">The source property is read-only.</span></span>

### <a name="method-tostring"></a><span data-ttu-id="20ffe-880">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="20ffe-880">Method toString</span></span>

<span data-ttu-id="20ffe-881">クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-881">Returns a string that contains the class handle and name, and sometimes additional information.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="20ffe-882">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-882">Return Value</span></span>

<span data-ttu-id="20ffe-883">クラスのテキストの説明。</span><span class="sxs-lookup"><span data-stu-id="20ffe-883">A textual description of the class.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-884">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-884">Remarks</span></span>

<span data-ttu-id="20ffe-885">ほとんどのクラスでは、返される文字列には、クラス ハンドルと名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-885">For most classes, the string that is returned contains the class handle and name.</span></span> <span data-ttu-id="20ffe-886">ただし、一部のクラスでは、文字列に追加情報が追加されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-886">However, for some classes, additional information is included in the string.</span></span>

### <a name="method-clear"></a><span data-ttu-id="20ffe-887">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="20ffe-887">Method clear</span></span>

<span data-ttu-id="20ffe-888">COMError オブジェクトのプロパティをクリアします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-888">Clears the properties of the COMError object.</span></span>

    public void clear()

#### <a name="remarks"></a><span data-ttu-id="20ffe-889">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-889">Remarks</span></span>

<span data-ttu-id="20ffe-890">通常、COMError オブジェクトのプロパティは読み取り専用ですが、このメソッドを使用して解除できます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-890">The properties of the COMError object are usually read-only, but they can be cleared by using this method.</span></span>

### <a name="method-new"></a><span data-ttu-id="20ffe-891">メソッド new</span><span class="sxs-lookup"><span data-stu-id="20ffe-891">Method new</span></span>

<span data-ttu-id="20ffe-892">COMError クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-892">Initializes an instance of the COMError class.</span></span>

    public void new()

### <a name="method-finalize"></a><span data-ttu-id="20ffe-893">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="20ffe-893">Method finalize</span></span>

    public void finalize()

## <a name="class-commaio"></a><span data-ttu-id="20ffe-894">クラス CommaIo</span><span class="sxs-lookup"><span data-stu-id="20ffe-894">Class CommaIo</span></span>
    class CommaIo extends Io

<span data-ttu-id="20ffe-895">CommaIo クラスには、コンマ区切りファイルの読み取りと書き込みを行う機能があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-895">The CommaIo class provides functionality for reading and writing comma-separated files.</span></span>

### <a name="remarks"></a><span data-ttu-id="20ffe-896">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-896">Remarks</span></span>

<span data-ttu-id="20ffe-897">このクラスは、CommaTextIo クラスに置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="20ffe-897">This class has been replaced by the CommaTextIo class.</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-898">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-898">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="20ffe-899">メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-899">Methods</span></span>

| <span data-ttu-id="20ffe-900">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-900">Method</span></span>                                       | <span data-ttu-id="20ffe-901">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-901">Description</span></span>                                                                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ffe-902">public int filePosition()</span><span class="sxs-lookup"><span data-stu-id="20ffe-902">public int filePosition()</span></span>                    |                                                                                                                              |
| <span data-ttu-id="20ffe-903">public str inFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-903">public str inFieldDelimiter(\[str value\])</span></span>   | <span data-ttu-id="20ffe-904">\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-904">Determines the delimiter used to separate fields in records accessed by the \*Io classes.</span></span>                                    |
| <span data-ttu-id="20ffe-905">public str inRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-905">public str inRecordDelimiter(\[str value\])</span></span>  | <span data-ttu-id="20ffe-906">完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-906">Determines to the \*Io classes what character or characters to search for to determine whether a full record has been read.</span></span>  |
| <span data-ttu-id="20ffe-907">public int inRecordLength(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-907">public int inRecordLength(\[int value\])</span></span>     | <span data-ttu-id="20ffe-908">ファイル内の各レコードを読み取る文字数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-908">Gets or sets the number of characters to read for each record in a file.</span></span>                                                     |
| <span data-ttu-id="20ffe-909">public str outFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-909">public str outFieldDelimiter(\[str value\])</span></span>  | <span data-ttu-id="20ffe-910">レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-910">Gets or sets the sequence of characters that are written to a file that is used to separate the fields of a record.</span></span>          |
| <span data-ttu-id="20ffe-911">public str outRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-911">public str outRecordDelimiter(\[str value\])</span></span> | <span data-ttu-id="20ffe-912">出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-912">Gets or sets the sequence of characters that is written to the output files, which separate the records in the output files.</span></span> |
| <span data-ttu-id="20ffe-913">public container read()</span><span class="sxs-lookup"><span data-stu-id="20ffe-913">public container read()</span></span>                      | <span data-ttu-id="20ffe-914">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-914">Reads the next full record from the Io object.</span></span>                                                                               |
| <span data-ttu-id="20ffe-915">public IO\_Status status()</span><span class="sxs-lookup"><span data-stu-id="20ffe-915">public IO\_Status status()</span></span>                   | <span data-ttu-id="20ffe-916">Io オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-916">Retrieves the status of the last operation that was performed on the Io object.</span></span>                                              |
| <span data-ttu-id="20ffe-917">public boolean write(VarArg values)</span><span class="sxs-lookup"><span data-stu-id="20ffe-917">public boolean write(VarArg values)</span></span>          | <span data-ttu-id="20ffe-918">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-918">Writes values of a simple type.</span></span>                                                                                              |
| <span data-ttu-id="20ffe-919">public boolean writeExp(container data)</span><span class="sxs-lookup"><span data-stu-id="20ffe-919">public boolean writeExp(container data)</span></span>      | <span data-ttu-id="20ffe-920">コンテナのコンテンツをファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-920">Writes the content of a container to a file.</span></span>                                                                                 |
| <span data-ttu-id="20ffe-921">public void new(str filename, str mode)</span><span class="sxs-lookup"><span data-stu-id="20ffe-921">public void new(str filename, str mode)</span></span>      | <span data-ttu-id="20ffe-922">CommaIo クラスの新しいオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-922">Creates a new object of the CommaIo class.</span></span>                                                                                   |
| <span data-ttu-id="20ffe-923">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="20ffe-923">public void finalize()</span></span>                       | <span data-ttu-id="20ffe-924">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-924">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>                                                  |

### <a name="method-fileposition"></a><span data-ttu-id="20ffe-925">メソッド filePosition</span><span class="sxs-lookup"><span data-stu-id="20ffe-925">Method filePosition</span></span>

    public int filePosition()

#### <a name="return-value"></a><span data-ttu-id="20ffe-926">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-926">Return Value</span></span>

### <a name="method-infielddelimiter"></a><span data-ttu-id="20ffe-927">メソッド inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="20ffe-927">Method inFieldDelimiter</span></span>

<span data-ttu-id="20ffe-928">\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-928">Determines the delimiter used to separate fields in records accessed by the \*Io classes.</span></span>

    public str inFieldDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-929">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-929">Parameters</span></span>

<span data-ttu-id="20ffe-930">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-930">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-931">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-931">Return Value</span></span>

<span data-ttu-id="20ffe-932">\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字。</span><span class="sxs-lookup"><span data-stu-id="20ffe-932">The delimiter used to separate fields in records accessed by the \*Io classes.</span></span>

### <a name="method-inrecorddelimiter"></a><span data-ttu-id="20ffe-933">メソッド inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="20ffe-933">Method inRecordDelimiter</span></span>

<span data-ttu-id="20ffe-934">完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-934">Determines to the \*Io classes what character or characters to search for to determine whether a full record has been read.</span></span>

    public str inRecordDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-935">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-935">Parameters</span></span>

<span data-ttu-id="20ffe-936">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-936">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-937">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-937">Return Value</span></span>

<span data-ttu-id="20ffe-938">完全なレコードが読み込まれたかどうかを示す文字。</span><span class="sxs-lookup"><span data-stu-id="20ffe-938">The character or characters that indicate whether a full record has been read.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-939">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-939">Remarks</span></span>

<span data-ttu-id="20ffe-940">標準的なテキストについては、区切り記号は改行文字です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-940">For standard text, the delimiter is a newline character.</span></span>

### <a name="method-inrecordlength"></a><span data-ttu-id="20ffe-941">メソッド inRecordLength</span><span class="sxs-lookup"><span data-stu-id="20ffe-941">Method inRecordLength</span></span>

<span data-ttu-id="20ffe-942">ファイル内の各レコードを読み取る文字数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-942">Gets or sets the number of characters to read for each record in a file.</span></span>

    public int inRecordLength([int value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-943">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-943">Parameters</span></span>

<span data-ttu-id="20ffe-944">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-944">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-945">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-945">Return Value</span></span>

<span data-ttu-id="20ffe-946">ファイル内の各レコードを読み取る文字数。</span><span class="sxs-lookup"><span data-stu-id="20ffe-946">The number of characters to read for each record in the file.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-947">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-947">Remarks</span></span>

<span data-ttu-id="20ffe-948">固定長形式になっているファイルについては、inRecordLength プロパティを使用して、各レコードに対して指定された文字数以上が読み取られていないことを保証します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-948">For files that have a fixed-length format, use the inRecordLength property to guarantee that no more than the specified number of characters are read for each record.</span></span> <span data-ttu-id="20ffe-949">レコード フォーマットが指定された inRecordDelimiter プロパティ値で上書きされた場合、つまり、固定長が読み込まれる前に inRecordDelimiter 値が満たされている場合)、レコードは受け入れられ、追加のデータは読み込まれません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-949">If the record format is overruled by a specified inRecordDelimiter property value , that is the inRecordDelimiter value is met before the fixed length is read, the record is accepted, and no additional data is read.</span></span> <span data-ttu-id="20ffe-950">固定数の文字を確実に読み取るには、inRecordDelimiter プロパティ値を空の文字列に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-950">To ensure that a fixed number of characters are read, set the inRecordDelimiter property value to an empty string.</span></span> <span data-ttu-id="20ffe-951">inRecordDelimiter プロパティ値が見つからない場合、inRecordDelimiter プロパティ値は読み取れる最大文字数になります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-951">When no inRecordDelimiter property value is found, the inRecordDelimiter property value is the maximum limit of characters to read.</span></span> <span data-ttu-id="20ffe-952">レコードの長さチェックを無効にするには、inRecordDelimiter プロパティ値をゼロに設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-952">Set the inRecordDelimiter property value to zero to disable the record length check.</span></span>

### <a name="method-outfielddelimiter"></a><span data-ttu-id="20ffe-953">メソッド outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="20ffe-953">Method outFieldDelimiter</span></span>

<span data-ttu-id="20ffe-954">レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-954">Gets or sets the sequence of characters that are written to a file that is used to separate the fields of a record.</span></span>

    public str outFieldDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-955">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-955">Parameters</span></span>

<span data-ttu-id="20ffe-956">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-956">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-957">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-957">Return Value</span></span>

<span data-ttu-id="20ffe-958">レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンス。</span><span class="sxs-lookup"><span data-stu-id="20ffe-958">The sequence of characters that are written to a file that is used to separate the fields of a record.</span></span>

### <a name="method-outrecorddelimiter"></a><span data-ttu-id="20ffe-959">メソッド outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="20ffe-959">Method outRecordDelimiter</span></span>

<span data-ttu-id="20ffe-960">出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-960">Gets or sets the sequence of characters that is written to the output files, which separate the records in the output files.</span></span>

    public str outRecordDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-961">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-961">Parameters</span></span>

<span data-ttu-id="20ffe-962">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-962">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-963">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-963">Return Value</span></span>

<span data-ttu-id="20ffe-964">出力ファイルに書き込まれる文字のシーケンス。</span><span class="sxs-lookup"><span data-stu-id="20ffe-964">The sequence of characters that is written to the output files.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-965">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-965">Remarks</span></span>

<span data-ttu-id="20ffe-966">標準的なテキスト ファイルについては、区切り記号は改行文字です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-966">For standard text files, the delimiter is a newline character.</span></span>

### <a name="method-read"></a><span data-ttu-id="20ffe-967">メソッド read</span><span class="sxs-lookup"><span data-stu-id="20ffe-967">Method read</span></span>

<span data-ttu-id="20ffe-968">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-968">Reads the next full record from the Io object.</span></span>

    public container read()

#### <a name="return-value"></a><span data-ttu-id="20ffe-969">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-969">Return Value</span></span>

<span data-ttu-id="20ffe-970">Io オブジェクトからの次の完全なレコード。</span><span class="sxs-lookup"><span data-stu-id="20ffe-970">The next full record from the Io object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-971">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-971">Remarks</span></span>

<span data-ttu-id="20ffe-972">次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength プロパティによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-972">The definition of the next full record is controlled by the inFieldDelimiter, inRecordDelimiter, and inRecordLength properties.</span></span> <span data-ttu-id="20ffe-973">レコードはコンテナーとして返されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-973">The record is returned as a container.</span></span> <span data-ttu-id="20ffe-974">コンテナー内の各エントリは、レコードの 1 つのフィールドと同じです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-974">Each entry in the container equals one field in the record.</span></span> <span data-ttu-id="20ffe-975">それぞれの特殊な Io クラスでは、inFieldDelimiter、inRecordDelimiter、および inRecordLength のプロパティのデフォルト設定を使用し、最も一般的な形式の入出力を有効にします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-975">Each specialized Io class has default settings for the inFieldDelimiter, inRecordDelimiter, and inRecordLength properties to enable input and output in the most common formats.</span></span> <span data-ttu-id="20ffe-976">ただし、目的の形式をサポートするために、これらの設定の調整が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-976">However, you might have to adjust these settings to support the desired format.</span></span>

### <a name="method-status"></a><span data-ttu-id="20ffe-977">メソッド status</span><span class="sxs-lookup"><span data-stu-id="20ffe-977">Method status</span></span>

<span data-ttu-id="20ffe-978">Io オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-978">Retrieves the status of the last operation that was performed on the Io object.</span></span>

    public IO_Status status()

#### <a name="return-value"></a><span data-ttu-id="20ffe-979">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-979">Return Value</span></span>

<span data-ttu-id="20ffe-980">最後の操作の状態。システム列挙形式。</span><span class="sxs-lookup"><span data-stu-id="20ffe-980">The status of the last operation, in the form of a system enumeration.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-981">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-981">Remarks</span></span>

<span data-ttu-id="20ffe-982">戻り値は、IO\_ステータス システムの列挙によって表されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-982">The return value is represented by the IO\_Status system enumeration.</span></span> <span data-ttu-id="20ffe-983">可能性のある IO\_Status 値の範囲はクラスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-983">The range of possible IO\_Status values varies among Io classes.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-984">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-984">Examples</span></span>

<span data-ttu-id="20ffe-985">この例は、状態メソッドを使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-985">This example shows how to use the status method.</span></span> <span data-ttu-id="20ffe-986">ただし、この例は、クラス、フォーム、またはその他のオブジェクトのコンテキストで実行される必要があるため、ジョブはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-986">However, this example will not compile in a job, because it must be run in the context of a class, form, or other object.</span></span>

    { 
        // Create an Io object and perform some operations. 
        if (myIo.status() == IO_Status::OK) 
        { 
            // Go ahead - the last operation was successful. 
        } 
    }

### <a name="method-write"></a><span data-ttu-id="20ffe-987">メソッド write</span><span class="sxs-lookup"><span data-stu-id="20ffe-987">Method write</span></span>

<span data-ttu-id="20ffe-988">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-988">Writes values of a simple type.</span></span>

    public boolean write(VarArg values)

#### <a name="parameters"></a><span data-ttu-id="20ffe-989">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-989">Parameters</span></span>

<span data-ttu-id="20ffe-990">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-990">values</span></span>  
<span data-ttu-id="20ffe-991">1 つ以上の値の、各単純型は、フィールドの区切り記号で区切られています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-991">One or more values, each of a simple type, separated by a field delimiter.</span></span> <span data-ttu-id="20ffe-992">単純型は、文字列、整数、実数、列挙型、日付です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-992">The simple types are string, integer, real, enum, and date.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-993">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-993">Return Value</span></span>

<span data-ttu-id="20ffe-994">書き込み操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="20ffe-994">true if the write operation succeeds; otherwise, false.</span></span> <span data-ttu-id="20ffe-995">工程が失敗すると、ステータスをチェックし障害について確認できます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-995">If the operation fails, you can check the status to learn the cause of the failure.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-996">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-996">Remarks</span></span>

<span data-ttu-id="20ffe-997">このメソッドは、可変数の引数を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-997">The method accepts a variable number of arguments.</span></span> <span data-ttu-id="20ffe-998">指定された各値は、フィールドとして出力レコードに配置されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-998">Each value that is specified is put into the output record as a field.</span></span> <span data-ttu-id="20ffe-999">最初の引数は最初のフィールドになり、2 番目の引数は 2 番目のフィールドなどになります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-999">The first argument becomes the first field, the second argument becomes the second field, and so on.</span></span> <span data-ttu-id="20ffe-1000">フィールドは、outFieldDelimiter メソッドで指定されるフィールド区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1000">Fields are separated by the field delimiter that is specified in the outFieldDelimiter method.</span></span> <span data-ttu-id="20ffe-1001">レコードは、outRecordDelimiter メソッドを使用して指定される区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1001">Records are separated by the delimiter that is specified by using the outRecordDelimiter method.</span></span> <span data-ttu-id="20ffe-1002">完全なコンテナーを書き込むには、writeExp メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1002">To write complete containers, use the writeExp method.</span></span>

### <a name="method-writeexp"></a><span data-ttu-id="20ffe-1003">メソッド writeExp</span><span class="sxs-lookup"><span data-stu-id="20ffe-1003">Method writeExp</span></span>

<span data-ttu-id="20ffe-1004">コンテナのコンテンツをファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1004">Writes the content of a container to a file.</span></span>

    public boolean writeExp(container data)

#### <a name="parameters"></a><span data-ttu-id="20ffe-1005">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1005">Parameters</span></span>

<span data-ttu-id="20ffe-1006">データ</span><span class="sxs-lookup"><span data-stu-id="20ffe-1006">data</span></span>  
<span data-ttu-id="20ffe-1007">レコードのデータを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1007">The container that holds data for the record.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1008">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1008">Return Value</span></span>

<span data-ttu-id="20ffe-1009">操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1009">true if the operation succeeds; otherwise, false.</span></span> <span data-ttu-id="20ffe-1010">工程が失敗すると、ステータスをチェックし障害について確認できます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1010">If the operation fails, you can check the status to learn the cause of the failure.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1011">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1011">Remarks</span></span>

<span data-ttu-id="20ffe-1012">コンテナー内のエントリはフィールドとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1012">The entries in the container are treated as fields.</span></span> <span data-ttu-id="20ffe-1013">コンテナー自体は、完全なレコードとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1013">The container itself is treated as a full record.</span></span> <span data-ttu-id="20ffe-1014">フィールドは、outFieldDelimiter メソッドを使用して指定される区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1014">Fields are separated by the delimiter that is specified by using the outFieldDelimiter method.</span></span> <span data-ttu-id="20ffe-1015">レコードは、outRecordDelimiter メソッドを使用して指定される区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1015">Records are separated by the delimiter that is specified by using the outRecordDelimiter method.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1016">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1016">Examples</span></span>

<span data-ttu-id="20ffe-1017">この例では、CommaIO オブジェクトを使用してサンプル ファイルから読み取ります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1017">This example uses a CommaIO object to read from the example file.</span></span>

    { 
        container c; 
        CommaIo myfile; 
        FileIoPermission perm; 

        #define.ExampleFile(@"c:\myfile.txt") 
        #define.ExampleOpenMode("w") 

        // Set code access permission to help protect the use 
        // of CommaIO.new 
        perm = new FileIoPermission(#ExampleFile, #ExampleOpenMode); 
        perm.assert(); 

        myfile = new CommaIo(#ExampleFile, #ExampleOpenMode); 

        // Assign the entries in the container according to record layout. 
        c = [1,"MyText",1.324,"Last field"]; 
        // Write this record according to file format  
        // (record/field delimiters). 
        myfile.writeExp(c); 

        // Close the code access permission. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-new"></a><span data-ttu-id="20ffe-1018">メソッド new</span><span class="sxs-lookup"><span data-stu-id="20ffe-1018">Method new</span></span>

<span data-ttu-id="20ffe-1019">CommaIo クラスの新しいオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1019">Creates a new object of the CommaIo class.</span></span>

    public void new(str filename, str mode)

#### <a name="parameters"></a><span data-ttu-id="20ffe-1020">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1020">Parameters</span></span>

<span data-ttu-id="20ffe-1021">filename</span><span class="sxs-lookup"><span data-stu-id="20ffe-1021">filename</span></span>  
<span data-ttu-id="20ffe-1022">ファイルを開く必要があるモード。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1022">The mode that the file should be opened in.</span></span> <span data-ttu-id="20ffe-1023">次のようにモードを指定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1023">Specify the mode as follows:</span></span>

<!-- -->

<span data-ttu-id="20ffe-1024">モード</span><span class="sxs-lookup"><span data-stu-id="20ffe-1024">mode</span></span>  
<span data-ttu-id="20ffe-1025">ファイルを開く必要があるモード。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1025">The mode that the file should be opened in.</span></span> <span data-ttu-id="20ffe-1026">次のようにモードを指定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1026">Specify the mode as follows:</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1027">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1027">Remarks</span></span>

<span data-ttu-id="20ffe-1028">ランタイム エラーは、現在のモードに対応していないメソッドを使用してファイルにアクセスした場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1028">A run-time error occurs if the file is accessed by using a method that does not correspond to the current mode.</span></span> <span data-ttu-id="20ffe-1029">たとえば、ユーザーが読み取りモードで開いているファイルへの書き込みしようとすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1029">For example, an error occurs if a user tries to write to a file that is opened in read mode.</span></span> <span data-ttu-id="20ffe-1030">攻撃者がこのメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1030">If an attacker can control input to this method, a security risk exists.</span></span> <span data-ttu-id="20ffe-1031">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1031">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="20ffe-1032">サーバー上でこのメソッドを呼び出すには、FileIOPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1032">Calls to this method on the server require permission from the FileIOPermission class.</span></span> <span data-ttu-id="20ffe-1033">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1033">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1034">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1034">Examples</span></span>

<span data-ttu-id="20ffe-1035">次の例では、CommaIO オブジェクトを使用して ExampleFile ファイルから読み取ります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1035">The following example uses a CommaIO object to read from the ExampleFile file.</span></span>

    { 
        CommaIo         io; 
        container       con; 
        FileIoPermission perm; 

        #define.ExampleFile(@"c:\test.txt") 
        #define.ExampleOpenMode("r") 

        perm = new FileIoPermission(#ExampleFile, #ExampleOpenMode); 
        if (perm == null) 
        { 
            return; 
        } 
        // Grants permission to execute the CommaIo.new method. 
        // CommaIo.new runs under code access security. 
        perm.assert(); 

        io = new CommaIo(#ExampleFile, #ExampleOpenMode); 
        if (io != null) 
        { 
            con = io.read(); 
        } 

        // Close the code access permission scope. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-finalize"></a><span data-ttu-id="20ffe-1036">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="20ffe-1036">Method finalize</span></span>

<span data-ttu-id="20ffe-1037">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1037">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>

    public void finalize()

#### <a name="remarks"></a><span data-ttu-id="20ffe-1038">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1038">Remarks</span></span>

<span data-ttu-id="20ffe-1039">このメソッドは通常は直接呼び出されません。代わりに、オブジェクトはスコープを離れることによって確定されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1039">This method is not usually called directly; instead, the object is finalized by leaving the scope.</span></span> <span data-ttu-id="20ffe-1040">記述された出力はオブジェクトが終了するまで無効です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1040">The written output is not valid until the object is finalized.</span></span>

## <a name="class-commatextio"></a><span data-ttu-id="20ffe-1041">クラス CommaTextIo</span><span class="sxs-lookup"><span data-stu-id="20ffe-1041">Class CommaTextIo</span></span>
    class CommaTextIo extends Io

### <a name="remarks"></a><span data-ttu-id="20ffe-1042">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1042">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-1043">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1043">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="20ffe-1044">メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-1044">Methods</span></span>

| <span data-ttu-id="20ffe-1045">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-1045">Method</span></span>                                                    | <span data-ttu-id="20ffe-1046">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-1046">Description</span></span>                                                                                                                  |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ffe-1047">public int filePosition()</span><span class="sxs-lookup"><span data-stu-id="20ffe-1047">public int filePosition()</span></span>                                 |                                                                                                                              |
| <span data-ttu-id="20ffe-1048">public str inFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1048">public str inFieldDelimiter(\[str value\])</span></span>                | <span data-ttu-id="20ffe-1049">\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1049">Determines the delimiter used to separate fields in records accessed by the \*Io classes.</span></span>                                    |
| <span data-ttu-id="20ffe-1050">public str inRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1050">public str inRecordDelimiter(\[str value\])</span></span>               | <span data-ttu-id="20ffe-1051">完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1051">Determines to the \*Io classes what character or characters to search for to determine whether a full record has been read.</span></span>  |
| <span data-ttu-id="20ffe-1052">public int inRecordLength(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1052">public int inRecordLength(\[int value\])</span></span>                  | <span data-ttu-id="20ffe-1053">ファイル内の各レコードを読み取る文字数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1053">Gets or sets the number of characters to read for each record in a file.</span></span>                                                     |
| <span data-ttu-id="20ffe-1054">public str outFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1054">public str outFieldDelimiter(\[str value\])</span></span>               | <span data-ttu-id="20ffe-1055">レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1055">Gets or sets the sequence of characters that are written to a file that is used to separate the fields of a record.</span></span>          |
| <span data-ttu-id="20ffe-1056">public str outRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1056">public str outRecordDelimiter(\[str value\])</span></span>              | <span data-ttu-id="20ffe-1057">出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1057">Gets or sets the sequence of characters that is written to the output files, which separate the records in the output files.</span></span> |
| <span data-ttu-id="20ffe-1058">public container read()</span><span class="sxs-lookup"><span data-stu-id="20ffe-1058">public container read()</span></span>                                   | <span data-ttu-id="20ffe-1059">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1059">Reads the next full record from the Io object.</span></span>                                                                               |
| <span data-ttu-id="20ffe-1060">public IO\_Status status()</span><span class="sxs-lookup"><span data-stu-id="20ffe-1060">public IO\_Status status()</span></span>                                | <span data-ttu-id="20ffe-1061">Io オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1061">Retrieves the status of the last operation that was performed on the Io object.</span></span>                                              |
| <span data-ttu-id="20ffe-1062">public boolean write(VarArg values)</span><span class="sxs-lookup"><span data-stu-id="20ffe-1062">public boolean write(VarArg values)</span></span>                       | <span data-ttu-id="20ffe-1063">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1063">Writes values of a simple type.</span></span>                                                                                              |
| <span data-ttu-id="20ffe-1064">public boolean writeExp(container data)</span><span class="sxs-lookup"><span data-stu-id="20ffe-1064">public boolean writeExp(container data)</span></span>                   | <span data-ttu-id="20ffe-1065">コンテナのコンテンツをファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1065">Writes the content of a container to a file.</span></span>                                                                                 |
| <span data-ttu-id="20ffe-1066">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="20ffe-1066">public void finalize()</span></span>                                    | <span data-ttu-id="20ffe-1067">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1067">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>                                                  |
| <span data-ttu-id="20ffe-1068">public void new(str filename, str mode, \[int codepage\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1068">public void new(str filename, str mode, \[int codepage\])</span></span> | <span data-ttu-id="20ffe-1069">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1069">Initializes a new instance of the Object class.</span></span>                                                                              |

### <a name="method-fileposition"></a><span data-ttu-id="20ffe-1070">メソッド filePosition</span><span class="sxs-lookup"><span data-stu-id="20ffe-1070">Method filePosition</span></span>

    public int filePosition()

#### <a name="return-value"></a><span data-ttu-id="20ffe-1071">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1071">Return Value</span></span>

### <a name="method-infielddelimiter"></a><span data-ttu-id="20ffe-1072">メソッド inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="20ffe-1072">Method inFieldDelimiter</span></span>

<span data-ttu-id="20ffe-1073">\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1073">Determines the delimiter used to separate fields in records accessed by the \*Io classes.</span></span>

    public str inFieldDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1074">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1074">Parameters</span></span>

<span data-ttu-id="20ffe-1075">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1075">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-1076">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1076">Return Value</span></span>

<span data-ttu-id="20ffe-1077">\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1077">The delimiter used to separate fields in records accessed by the \*Io classes.</span></span>

### <a name="method-inrecorddelimiter"></a><span data-ttu-id="20ffe-1078">メソッド inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="20ffe-1078">Method inRecordDelimiter</span></span>

<span data-ttu-id="20ffe-1079">完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1079">Determines to the \*Io classes what character or characters to search for to determine whether a full record has been read.</span></span>

    public str inRecordDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1080">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1080">Parameters</span></span>

<span data-ttu-id="20ffe-1081">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1081">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-1082">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1082">Return Value</span></span>

<span data-ttu-id="20ffe-1083">完全なレコードが読み込まれたかどうかを示す文字。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1083">The character or characters that indicate whether a full record has been read.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1084">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1084">Remarks</span></span>

<span data-ttu-id="20ffe-1085">標準的なテキストについては、区切り記号は改行文字です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1085">For standard text, the delimiter is a newline character.</span></span>

### <a name="method-inrecordlength"></a><span data-ttu-id="20ffe-1086">メソッド inRecordLength</span><span class="sxs-lookup"><span data-stu-id="20ffe-1086">Method inRecordLength</span></span>

<span data-ttu-id="20ffe-1087">ファイル内の各レコードを読み取る文字数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1087">Gets or sets the number of characters to read for each record in a file.</span></span>

    public int inRecordLength([int value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1088">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1088">Parameters</span></span>

<span data-ttu-id="20ffe-1089">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1089">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-1090">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1090">Return Value</span></span>

<span data-ttu-id="20ffe-1091">ファイル内の各レコードを読み取る文字数。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1091">The number of characters to read for each record in the file.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1092">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1092">Remarks</span></span>

<span data-ttu-id="20ffe-1093">固定長形式になっているファイルについては、inRecordLength プロパティを使用して、各レコードに対して指定された文字数以上が読み取られていないことを保証します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1093">For files that have a fixed-length format, use the inRecordLength property to guarantee that no more than the specified number of characters are read for each record.</span></span> <span data-ttu-id="20ffe-1094">レコード フォーマットが指定された inRecordDelimiter プロパティ値で上書きされた場合、つまり、固定長が読み込まれる前に inRecordDelimiter 値が満たされている場合)、レコードは受け入れられ、追加のデータは読み込まれません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1094">If the record format is overruled by a specified inRecordDelimiter property value , that is the inRecordDelimiter value is met before the fixed length is read, the record is accepted, and no additional data is read.</span></span> <span data-ttu-id="20ffe-1095">固定数の文字を確実に読み取るには、inRecordDelimiter プロパティ値を空の文字列に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1095">To guarantee that a fixed number of characters are read, set the inRecordDelimiter property value to an empty string.</span></span> <span data-ttu-id="20ffe-1096">inRecordDelimiter プロパティ値が見つからない場合、inRecordDelimiter プロパティ値は読み取れる最大文字数になります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1096">When no inRecordDelimiter property value is found, the inRecordDelimiter property value is the maximum limit of characters to read.</span></span> <span data-ttu-id="20ffe-1097">レコードの長さチェックを無効にするには、inRecordDelimiter プロパティ値をゼロに設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1097">Set the inRecordDelimiter property value to zero to disable the record length check.</span></span>

### <a name="method-outfielddelimiter"></a><span data-ttu-id="20ffe-1098">メソッド outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="20ffe-1098">Method outFieldDelimiter</span></span>

<span data-ttu-id="20ffe-1099">レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1099">Gets or sets the sequence of characters that are written to a file that is used to separate the fields of a record.</span></span>

    public str outFieldDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1100">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1100">Parameters</span></span>

<span data-ttu-id="20ffe-1101">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1101">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-1102">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1102">Return Value</span></span>

<span data-ttu-id="20ffe-1103">レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンス。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1103">The sequence of characters that are written to a file that is used to separate the fields of a record.</span></span>

### <a name="method-outrecorddelimiter"></a><span data-ttu-id="20ffe-1104">メソッド outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="20ffe-1104">Method outRecordDelimiter</span></span>

<span data-ttu-id="20ffe-1105">出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1105">Gets or sets the sequence of characters that is written to the output files, which separate the records in the output files.</span></span>

    public str outRecordDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1106">Parameters</span></span>

<span data-ttu-id="20ffe-1107">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1107">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-1108">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1108">Return Value</span></span>

<span data-ttu-id="20ffe-1109">出力ファイルに書き込まれる文字のシーケンス。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1109">The sequence of characters that is written to the output files.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1110">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1110">Remarks</span></span>

<span data-ttu-id="20ffe-1111">標準的なテキスト ファイルについては、区切り記号は改行文字です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1111">For standard text files, the delimiter is a newline character.</span></span>

### <a name="method-read"></a><span data-ttu-id="20ffe-1112">メソッド read</span><span class="sxs-lookup"><span data-stu-id="20ffe-1112">Method read</span></span>

<span data-ttu-id="20ffe-1113">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1113">Reads the next full record from the Io object.</span></span>

    public container read()

#### <a name="return-value"></a><span data-ttu-id="20ffe-1114">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1114">Return Value</span></span>

<span data-ttu-id="20ffe-1115">入出力オブジェクトから次の完全なレコードを保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1115">A container that holds the next full record from the Io object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1116">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1116">Remarks</span></span>

<span data-ttu-id="20ffe-1117">次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength メソッド プロパティによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1117">The definition of the next full record is controlled by the inFieldDelimiter, inRecordDelimiter, and inRecordLength method properties.</span></span> <span data-ttu-id="20ffe-1118">レコードはコンテナーとして返されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1118">The record is returned as a container.</span></span> <span data-ttu-id="20ffe-1119">コンテナー内の各エントリは、レコードの 1 つのフィールドと同じです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1119">Each entry in the container equals one field in the record.</span></span> <span data-ttu-id="20ffe-1120">それぞれの特殊な Io クラスには、inFieldDelimiter、inRecordDelimiter、および inRecordLength のプロパティのデフォルト設定があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1120">Each specialized Io class has default settings for the inFieldDelimiter, inRecordDelimiter, and inRecordLength properties.</span></span> <span data-ttu-id="20ffe-1121">これらの既定の設定では、最も一般的な形式の入力と出力が可能です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1121">These default settings enable input and output in the most common formats.</span></span> <span data-ttu-id="20ffe-1122">ただし、目的の形式をサポートするために、これらの設定の調整が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1122">However, you might have to adjust these settings to support the desired format.</span></span>

### <a name="method-status"></a><span data-ttu-id="20ffe-1123">メソッド status</span><span class="sxs-lookup"><span data-stu-id="20ffe-1123">Method status</span></span>

<span data-ttu-id="20ffe-1124">Io オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1124">Retrieves the status of the last operation that was performed on the Io object.</span></span>

    public IO_Status status()

#### <a name="return-value"></a><span data-ttu-id="20ffe-1125">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1125">Return Value</span></span>

<span data-ttu-id="20ffe-1126">IO\_Status システム列挙値としての最後の操作の状態。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1126">The status of the last operation, as an IO\_Status system enumeration value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1127">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1127">Remarks</span></span>

<span data-ttu-id="20ffe-1128">返される IO\_Status の値の範囲は、Io クラスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1128">The range of IO\_Status values that can be returned varies, depending on the Io class.</span></span>

### <a name="method-write"></a><span data-ttu-id="20ffe-1129">メソッド write</span><span class="sxs-lookup"><span data-stu-id="20ffe-1129">Method write</span></span>

<span data-ttu-id="20ffe-1130">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1130">Writes values of a simple type.</span></span>

    public boolean write(VarArg values)

#### <a name="parameters"></a><span data-ttu-id="20ffe-1131">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1131">Parameters</span></span>

<span data-ttu-id="20ffe-1132">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1132">values</span></span>  
<span data-ttu-id="20ffe-1133">単純型の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1133">A value of a simple type.</span></span> <span data-ttu-id="20ffe-1134">単純型は、文字列、整数、実数、列挙型、日付です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1134">The simple types are string, integer, real, enum, and date.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1135">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1135">Return Value</span></span>

<span data-ttu-id="20ffe-1136">書き込み操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1136">true if the write operation is successful; otherwise, false.</span></span> <span data-ttu-id="20ffe-1137">書き込み操作が失敗すると、ステータス メソッドを使用して、原因について確認できます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1137">If the write operation fails, you can use the status method to determine the cause.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1138">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1138">Remarks</span></span>

<span data-ttu-id="20ffe-1139">このメソッドは、可変数の引数を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1139">The method accepts a variable number of arguments.</span></span> <span data-ttu-id="20ffe-1140">指定された各値は、フィールドとして出力レコードに配置されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1140">Each value that is specified is put into the output record as a field.</span></span> <span data-ttu-id="20ffe-1141">最初の引数は最初のフィールドであり、2 番目の引数は 2 番目のフィールドなどになります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1141">The first argument is the first field, the second argument is the second field, and so on.</span></span> <span data-ttu-id="20ffe-1142">フィールドは、outFieldDelimiter メソッドで指定される区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1142">Fields are separated by the delimiter that is specified in the outFieldDelimiter method.</span></span> <span data-ttu-id="20ffe-1143">レコードは、outRecordDelimiter メソッドで指定される区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1143">Records are separated by the delimiter that is specified in the outRecordDelimiter method.</span></span> <span data-ttu-id="20ffe-1144">完全なコンテナーを書き込むには、writeExp メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1144">To write complete containers, use the writeExp method.</span></span>

### <a name="method-writeexp"></a><span data-ttu-id="20ffe-1145">メソッド writeExp</span><span class="sxs-lookup"><span data-stu-id="20ffe-1145">Method writeExp</span></span>

<span data-ttu-id="20ffe-1146">コンテナのコンテンツをファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1146">Writes the content of a container to a file.</span></span>

    public boolean writeExp(container data)

#### <a name="parameters"></a><span data-ttu-id="20ffe-1147">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1147">Parameters</span></span>

<span data-ttu-id="20ffe-1148">データ</span><span class="sxs-lookup"><span data-stu-id="20ffe-1148">data</span></span>  
<span data-ttu-id="20ffe-1149">レコードのデータを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1149">The container that holds data for the record.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1150">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1150">Return Value</span></span>

<span data-ttu-id="20ffe-1151">操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1151">true if the operation is successful; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1152">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1152">Remarks</span></span>

<span data-ttu-id="20ffe-1153">このメソッドが false を返す場合、ステータス メソッドで原因を確認します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1153">If this method returns false, check the status method for the cause.</span></span> <span data-ttu-id="20ffe-1154">コンテナー内のエントリはフィールドとして扱われ、コンテナーは完全なレコードとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1154">The entries in the container are treated as fields, and the container is treated as a full record.</span></span> <span data-ttu-id="20ffe-1155">フィールド区切り記号は、outFieldDelimiter メソッドで定義されています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1155">The field separator is defined in the outFieldDelimiter method.</span></span> <span data-ttu-id="20ffe-1156">レコード区切りは outRecordDelimiter メソッドで定義されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1156">The record separator is defined in the outRecordDelimiter method.</span></span>

### <a name="method-finalize"></a><span data-ttu-id="20ffe-1157">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="20ffe-1157">Method finalize</span></span>

<span data-ttu-id="20ffe-1158">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1158">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>

    public void finalize()

#### <a name="remarks"></a><span data-ttu-id="20ffe-1159">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1159">Remarks</span></span>

<span data-ttu-id="20ffe-1160">このメソッドは、通常は直接呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1160">This method is not usually called directly.</span></span> <span data-ttu-id="20ffe-1161">代わりに、オブジェクトは通常、スコープを離れることによって確定されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1161">Instead, the object is usually finalized by leaving the scope.</span></span> <span data-ttu-id="20ffe-1162">記述された出力はオブジェクトが終了するまで無効です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1162">Written output is not valid until the object is finalized.</span></span>

### <a name="method-new"></a><span data-ttu-id="20ffe-1163">メソッド new</span><span class="sxs-lookup"><span data-stu-id="20ffe-1163">Method new</span></span>

<span data-ttu-id="20ffe-1164">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1164">Initializes a new instance of the Object class.</span></span>

    public void new(str filename, str mode, [int codepage])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1165">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1165">Parameters</span></span>

<span data-ttu-id="20ffe-1166">filename</span><span class="sxs-lookup"><span data-stu-id="20ffe-1166">filename</span></span>  

<!-- -->

<span data-ttu-id="20ffe-1167">モード</span><span class="sxs-lookup"><span data-stu-id="20ffe-1167">mode</span></span>  

<!-- -->

<span data-ttu-id="20ffe-1168">codepage</span><span class="sxs-lookup"><span data-stu-id="20ffe-1168">codepage</span></span>  

#### <a name="remarks"></a><span data-ttu-id="20ffe-1169">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1169">Remarks</span></span>

<span data-ttu-id="20ffe-1170">攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1170">If an attacker can control input to the new method, a security risk exists.</span></span> <span data-ttu-id="20ffe-1171">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1171">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="20ffe-1172">サーバー上でこのメソッドを呼び出すには、FileIOPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1172">Calls to this method on the server require permission from the FileIOPermission class.</span></span> <span data-ttu-id="20ffe-1173">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1173">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

## <a name="class-compileoutputinfos"></a><span data-ttu-id="20ffe-1174">クラス CompileOutputInfos</span><span class="sxs-lookup"><span data-stu-id="20ffe-1174">Class CompileOutputInfos</span></span>
    class CompileOutputInfos extends Object

### <a name="remarks"></a><span data-ttu-id="20ffe-1175">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1175">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-1176">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1176">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="20ffe-1177">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-1177">Methods</span></span>

| <span data-ttu-id="20ffe-1178">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-1178">Method</span></span>                               | <span data-ttu-id="20ffe-1179">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-1179">Description</span></span> |
|--------------------------------------|-------------|
| <span data-ttu-id="20ffe-1180">::public static void NotifyChanges()</span><span class="sxs-lookup"><span data-stu-id="20ffe-1180">::public static void NotifyChanges()</span></span> |             |

### <a name="method-notifychanges"></a><span data-ttu-id="20ffe-1181">メソッド NotifyChanges</span><span class="sxs-lookup"><span data-stu-id="20ffe-1181">Method NotifyChanges</span></span>

    public static void NotifyChanges()

## <a name="class-comvariant"></a><span data-ttu-id="20ffe-1182">クラス COMVariant</span><span class="sxs-lookup"><span data-stu-id="20ffe-1182">Class COMVariant</span></span>
    class COMVariant extends Object

<span data-ttu-id="20ffe-1183">COMVariant クラスは、さまざまな種類のデータを格納できる一般的なクラスとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1183">The COMVariant class is used as a generic class that can store different types of data.</span></span> <span data-ttu-id="20ffe-1184">このクラスは、COM (コンポーネント オブジェクト モデル) 自動オブジェクトのメソッドまたはプロパティに引数を渡すために使用され、COM および COMDispFunction クラスとともに使用されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1184">The class is used to pass arguments to the methods or properties of a COM (Component Object Model) Automation object and is used with the COM and COMDispFunction classes.</span></span>

### <a name="remarks"></a><span data-ttu-id="20ffe-1185">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1185">Remarks</span></span>

<span data-ttu-id="20ffe-1186">COMVariant オブジェクトのデータ型は次によって設定できます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1186">The data type of the COMVariant object can be set by:</span></span>

-   <span data-ttu-id="20ffe-1187">新しいメソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-1187">The new method</span></span>
-   <span data-ttu-id="20ffe-1188">variantType メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-1188">The variantType method</span></span>
-   <span data-ttu-id="20ffe-1189">createFrom…</span><span class="sxs-lookup"><span data-stu-id="20ffe-1189">The createFrom…</span></span> <span data-ttu-id="20ffe-1190">メソッド。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1190">methods.</span></span> <span data-ttu-id="20ffe-1191">たとえば、createFromBoolean メソッドは、VT\_BOOL (= ブール値) のタイプの COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1191">For example, the createFromBoolean method creates a COMVariant object of type VT\_BOOL (= Boolean).</span></span>
-   <span data-ttu-id="20ffe-1192">プロパティ メソッド。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1192">The property methods.</span></span> <span data-ttu-id="20ffe-1193">たとえば、boolean プロパティを使用して新しい値を設定すると、オブジェクトは VT\_BOOL (= Boolean) のタイプではなく、このタイプに変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1193">For example, if you set a new value by using the boolean property, and the object is not of type VT\_BOOL (= Boolean), it will be changed to this type.</span></span>

<span data-ttu-id="20ffe-1194">データ型の値は、いずれかのプロパティ メソッドによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1194">The value of the data type is set by one of the property methods.</span></span> <span data-ttu-id="20ffe-1195">たとえば、タイプ VT\_BOOL の COMVariant オブジェクトの値は、boolean メソッドにより設定されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1195">For example, the value of a COMVariant object of type VT\_BOOL is set by the boolean method.</span></span> <span data-ttu-id="20ffe-1196">その値を設定する可能なデータ型とメソッドは、「備考」セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1196">The possible data types and the methods that set their values are listed in the Remarks section.</span></span> <span data-ttu-id="20ffe-1197">COMVariant クラスがサポートするデータ型は、X++ データ型ではなく、COMオートメーション標準によって定義されたデータ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1197">The data types that the COMVariant class supports are not X++ data types, but data types defined by the COM Automation standard.</span></span> <span data-ttu-id="20ffe-1198">COMVariant クラスは、Win32 SDK にある VARIANT 構造に基づいています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1198">The COMVariant class is based on the VARIANT structure found in the Win32 SDK.</span></span> <span data-ttu-id="20ffe-1199">詳細については、Win32 SDK ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1199">For more information see the Win32 SDK documentation.</span></span> <span data-ttu-id="20ffe-1200">COMVariant クラスのプロパティ メソッドは、次のように COMVariantType 値にマップされます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1200">The property methods of the COMVariant class map to the COMVariantType values in the following way:</span></span>

|             |               |                                                                                           |
|-------------|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ffe-1201">ブール値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1201">boolean</span></span>     | <span data-ttu-id="20ffe-1202">VT\_BOOL</span><span class="sxs-lookup"><span data-stu-id="20ffe-1202">VT\_BOOL</span></span>      |                                                                                           |
| <span data-ttu-id="20ffe-1203">bStr</span><span class="sxs-lookup"><span data-stu-id="20ffe-1203">bStr</span></span>        | <span data-ttu-id="20ffe-1204">VT\_BSTR</span><span class="sxs-lookup"><span data-stu-id="20ffe-1204">VT\_BSTR</span></span>      | <span data-ttu-id="20ffe-1205">文字列データ型</span><span class="sxs-lookup"><span data-stu-id="20ffe-1205">String data type</span></span>                                                                          |
| <span data-ttu-id="20ffe-1206">byte</span><span class="sxs-lookup"><span data-stu-id="20ffe-1206">byte</span></span>        | <span data-ttu-id="20ffe-1207">VT\_UI1</span><span class="sxs-lookup"><span data-stu-id="20ffe-1207">VT\_UI1</span></span>       |                                                                                           |
| <span data-ttu-id="20ffe-1208">char</span><span class="sxs-lookup"><span data-stu-id="20ffe-1208">char</span></span>        | <span data-ttu-id="20ffe-1209">VT\_I1</span><span class="sxs-lookup"><span data-stu-id="20ffe-1209">VT\_I1</span></span>        |                                                                                           |
| <span data-ttu-id="20ffe-1210">通貨</span><span class="sxs-lookup"><span data-stu-id="20ffe-1210">currency</span></span>    | <span data-ttu-id="20ffe-1211">VT\_CY</span><span class="sxs-lookup"><span data-stu-id="20ffe-1211">VT\_CY</span></span>        |                                                                                           |
| <span data-ttu-id="20ffe-1212">日付、時刻</span><span class="sxs-lookup"><span data-stu-id="20ffe-1212">date, time</span></span>  | <span data-ttu-id="20ffe-1213">VT\_DATE</span><span class="sxs-lookup"><span data-stu-id="20ffe-1213">VT\_DATE</span></span>      | <span data-ttu-id="20ffe-1214">日付/時刻データ型。両方のプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1214">Date/time data type; both properties must be set.</span></span>                                         |
| <span data-ttu-id="20ffe-1215">decimal</span><span class="sxs-lookup"><span data-stu-id="20ffe-1215">decimal</span></span>     | <span data-ttu-id="20ffe-1216">VT\_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="20ffe-1216">VT\_DECIMAL</span></span>   |                                                                                           |
| <span data-ttu-id="20ffe-1217">double</span><span class="sxs-lookup"><span data-stu-id="20ffe-1217">double</span></span>      | <span data-ttu-id="20ffe-1218">VT\_R8</span><span class="sxs-lookup"><span data-stu-id="20ffe-1218">VT\_R8</span></span>        |                                                                                           |
| <span data-ttu-id="20ffe-1219">float</span><span class="sxs-lookup"><span data-stu-id="20ffe-1219">float</span></span>       | <span data-ttu-id="20ffe-1220">VT\_R4</span><span class="sxs-lookup"><span data-stu-id="20ffe-1220">VT\_R4</span></span>        |                                                                                           |
| <span data-ttu-id="20ffe-1221">iDispatch</span><span class="sxs-lookup"><span data-stu-id="20ffe-1221">iDispatch</span></span>   | <span data-ttu-id="20ffe-1222">VT\_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="20ffe-1222">VT\_DISPATCH</span></span>  |                                                                                           |
| <span data-ttu-id="20ffe-1223">int, long</span><span class="sxs-lookup"><span data-stu-id="20ffe-1223">int, long</span></span>   | <span data-ttu-id="20ffe-1224">VT\_I4</span><span class="sxs-lookup"><span data-stu-id="20ffe-1224">VT\_I4</span></span>        | <span data-ttu-id="20ffe-1225">VT\_I4 は、int データ型と Long データ型の両方で使用されます</span><span class="sxs-lookup"><span data-stu-id="20ffe-1225">VT\_I4 is used for both the int and the long data types</span></span>                                   |
| <span data-ttu-id="20ffe-1226">iUnknown</span><span class="sxs-lookup"><span data-stu-id="20ffe-1226">iUnknown</span></span>    | <span data-ttu-id="20ffe-1227">VT\_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="20ffe-1227">VT\_UNKNOWN</span></span>   |                                                                                           |
| <span data-ttu-id="20ffe-1228">sCode</span><span class="sxs-lookup"><span data-stu-id="20ffe-1228">sCode</span></span>       | <span data-ttu-id="20ffe-1229">VT\_ERROR</span><span class="sxs-lookup"><span data-stu-id="20ffe-1229">VT\_ERROR</span></span>     | <span data-ttu-id="20ffe-1230">scode データ型は、Win32 HRESULT データ型と同等の COM データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1230">The scode data type is a COM data type that is equivalent to the Win32 HRESULT data type.</span></span> |
| <span data-ttu-id="20ffe-1231">short</span><span class="sxs-lookup"><span data-stu-id="20ffe-1231">short</span></span>       | <span data-ttu-id="20ffe-1232">VT\_I2</span><span class="sxs-lookup"><span data-stu-id="20ffe-1232">VT\_I2</span></span>        |                                                                                           |
| <span data-ttu-id="20ffe-1233">uInt、uLong</span><span class="sxs-lookup"><span data-stu-id="20ffe-1233">uInt, uLong</span></span> | <span data-ttu-id="20ffe-1234">VT\_UI4</span><span class="sxs-lookup"><span data-stu-id="20ffe-1234">VT\_UI4</span></span>       | <span data-ttu-id="20ffe-1235">VT\_UI4 は、uInt データ型と uLong データ型の両方で使用されます</span><span class="sxs-lookup"><span data-stu-id="20ffe-1235">VT\_UI4 is used for both the uInt and the uLong data types</span></span>                                |
| <span data-ttu-id="20ffe-1236">uShort</span><span class="sxs-lookup"><span data-stu-id="20ffe-1236">uShort</span></span>      | <span data-ttu-id="20ffe-1237">VT\_UI2</span><span class="sxs-lookup"><span data-stu-id="20ffe-1237">VT\_UI2</span></span>       |                                                                                           |
| <span data-ttu-id="20ffe-1238">バリアント</span><span class="sxs-lookup"><span data-stu-id="20ffe-1238">variant</span></span>     | <span data-ttu-id="20ffe-1239">VT\_VARIANT</span><span class="sxs-lookup"><span data-stu-id="20ffe-1239">VT\_VARIANT</span></span>   |                                                                                           |
| <span data-ttu-id="20ffe-1240">safeArray</span><span class="sxs-lookup"><span data-stu-id="20ffe-1240">safeArray</span></span>   | <span data-ttu-id="20ffe-1241">VT\_SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="20ffe-1241">VT\_SAFEARRAY</span></span> | <span data-ttu-id="20ffe-1242">配列データ タイプ</span><span class="sxs-lookup"><span data-stu-id="20ffe-1242">Array data type</span></span>                                                                           |

### <a name="examples"></a><span data-ttu-id="20ffe-1243">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1243">Examples</span></span>

<span data-ttu-id="20ffe-1244">次の例では、COMVariant パラメーターとして渡された 2 つの浮動小数点数を乗算する multiply というメソッドを公開する COM オブジェクトをインスタンス化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1244">The following example instantiates a COM object that exposes a method called multiply which multiplies two floating point numbers passed in as COMVariant parameters.</span></span>

    { 
        COM com; 
        COMVariant varArg1 = new COMVariant(); 
        COMVariant varArg2 = new COMVariant(); 
        COMVariant varRet; 
        real ret; 
        InteropPermission perm; 

        // Set code access permission to help protect the use  
        // of the COM object. 
        perm = new InteropPermission(InteropKind::ComInterop); 
        if (perm == null) 
        { 
            return; 
        } 

        // Permission scope starts here 
        perm.assert(); 

            com = new COM("MyCOM.Object"); 

        // Specify arguments for the 'multiply' method 
        varArg1.float(123); 
        varArg2.float(456); 
        varRet = com.multiply(varArg1, varArg2); 

        ret = varRet.double(); 
        // 'ret' is now 56088 (123*456) 

        // Close the code access permission scope. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="methods"></a><span data-ttu-id="20ffe-1245">メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-1245">Methods</span></span>

| <span data-ttu-id="20ffe-1246">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-1246">Method</span></span>                                                                                                    | <span data-ttu-id="20ffe-1247">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-1247">Description</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ffe-1248">public boolean boolean(\[boolean newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1248">public boolean boolean(\[boolean newValue\])</span></span>                                                              | <span data-ttu-id="20ffe-1249">VT\_BOOL データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1249">Gets or sets the value of a COMVariant object of the VT\_BOOL data type.</span></span>                                                                                                    |
| <span data-ttu-id="20ffe-1250">public str bStr(\[str newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1250">public str bStr(\[str newValue\])</span></span>                                                                         | <span data-ttu-id="20ffe-1251">VT\_BSTR データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1251">Gets or sets the value of a COMVariant object of the VT\_BSTR data type.</span></span>                                                                                                    |
| <span data-ttu-id="20ffe-1252">public int byte(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1252">public int byte(\[int newValue\])</span></span>                                                                         | <span data-ttu-id="20ffe-1253">VT\_UI1 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1253">Gets or sets the value of a COMVariant object of the VT\_UI1 data type.</span></span>                                                                                                     |
| <span data-ttu-id="20ffe-1254">public int char(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1254">public int char(\[int newValue\])</span></span>                                                                         | <span data-ttu-id="20ffe-1255">VT\_I1 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1255">Gets or sets the value of a COMVariant object of the VT\_I1 data type.</span></span>                                                                                                      |
| <span data-ttu-id="20ffe-1256">public container container(\[container newValue\], \[COMVariantType newType\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1256">public container container(\[container newValue\], \[COMVariantType newType\])</span></span>                            | <span data-ttu-id="20ffe-1257">コンテナ データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1257">Gets or sets the value of a COMVariant object of the container data type.</span></span>                                                                                                   |
| <span data-ttu-id="20ffe-1258">public Real currency(\[Real newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1258">public Real currency(\[Real newValue\])</span></span>                                                                   | <span data-ttu-id="20ffe-1259">VT\_CY データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1259">Gets or sets the value of a COMVariant object of the VT\_CY data type.</span></span>                                                                                                      |
| <span data-ttu-id="20ffe-1260">public Date date(\[Date newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1260">public Date date(\[Date newValue\])</span></span>                                                                       | <span data-ttu-id="20ffe-1261">VT\_DATE データ タイプの COMVariant オブジェクトの値の日付部分を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1261">Gets or sets the date part of the value of a COMVariant object of the VT\_DATE data type.</span></span>                                                                                   |
| <span data-ttu-id="20ffe-1262">public Real decimal(\[Real newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1262">public Real decimal(\[Real newValue\])</span></span>                                                                    | <span data-ttu-id="20ffe-1263">VT\_DECIMAL データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1263">Gets or sets the value of a COMVariant object of the VT\_DECIMAL data type.</span></span>                                                                                                 |
| <span data-ttu-id="20ffe-1264">public Real double(\[Real newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1264">public Real double(\[Real newValue\])</span></span>                                                                     | <span data-ttu-id="20ffe-1265">VT\_R8 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1265">Gets or sets the value of a COMVariant object of the VT\_R8 data type.</span></span>                                                                                                      |
| <span data-ttu-id="20ffe-1266">public Real float(\[Real newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1266">public Real float(\[Real newValue\])</span></span>                                                                      | <span data-ttu-id="20ffe-1267">VT\_R4 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1267">Gets or sets the value of a COMVariant object of the VT\_R4 data type.</span></span>                                                                                                      |
| <span data-ttu-id="20ffe-1268">public ComInterface iDispatch(\[ComInterface newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1268">public ComInterface iDispatch(\[ComInterface newValue\])</span></span>                                                  | <span data-ttu-id="20ffe-1269">VT\_DISPATCH データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1269">Gets or sets the value of a COMVariant object of the VT\_DISPATCH data type.</span></span>                                                                                                |
| <span data-ttu-id="20ffe-1270">public int int(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1270">public int int(\[int newValue\])</span></span>                                                                          | <span data-ttu-id="20ffe-1271">VT\_I4 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1271">Gets or sets the value of a COMVariant object of the VT\_I4 data type.</span></span>                                                                                                      |
| <span data-ttu-id="20ffe-1272">public ComInterface iUnknown(\[ComInterface newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1272">public ComInterface iUnknown(\[ComInterface newValue\])</span></span>                                                   | <span data-ttu-id="20ffe-1273">VT\_UNKNOWN (IUnknown) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1273">Gets or sets the value of a COMVariant object of the VT\_UNKNOWN (IUnknown) data type.</span></span>                                                                                      |
| <span data-ttu-id="20ffe-1274">public int long(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1274">public int long(\[int newValue\])</span></span>                                                                         | <span data-ttu-id="20ffe-1275">VT\_I4 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1275">Gets or sets the value of a COMVariant object of the VT\_I4 data type.</span></span>                                                                                                      |
| <span data-ttu-id="20ffe-1276">public Int64 longLong(\[Int64 newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1276">public Int64 longLong(\[Int64 newValue\])</span></span>                                                                 | <span data-ttu-id="20ffe-1277">VT\_I8 (longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1277">Gets or sets the value of a COMVariant object of the VT\_I8 (longlong) data type.</span></span>                                                                                           |
| <span data-ttu-id="20ffe-1278">public Array safeArray(\[Array newValue\], \[COMVariantType newType\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1278">public Array safeArray(\[Array newValue\], \[COMVariantType newType\])</span></span>                                    | <span data-ttu-id="20ffe-1279">VT\_SAFEARRAY データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1279">Gets or sets the value of a COMVariant object of the VT\_SAFEARRAY data type.</span></span>                                                                                               |
| <span data-ttu-id="20ffe-1280">public int sCode(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1280">public int sCode(\[int newValue\])</span></span>                                                                        | <span data-ttu-id="20ffe-1281">VT\_ERROR データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1281">Gets or sets the value of a COMVariant object of the VT\_ERROR data type.</span></span>                                                                                                   |
| <span data-ttu-id="20ffe-1282">public int short(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1282">public int short(\[int newValue\])</span></span>                                                                        | <span data-ttu-id="20ffe-1283">VT\_I2 (短い) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1283">Gets or sets the value of a COMVariant object of the VT\_I2 (short) data type.</span></span>                                                                                              |
| <span data-ttu-id="20ffe-1284">public int time(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1284">public int time(\[int newValue\])</span></span>                                                                         | <span data-ttu-id="20ffe-1285">VT\_DATE データ タイプの COMVariant オブジェクトの値の時刻部分を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1285">Gets or sets the time part of the value of a COMVariant object of the VT\_DATE data type.</span></span>                                                                                   |
| <span data-ttu-id="20ffe-1286">public str toString()</span><span class="sxs-lookup"><span data-stu-id="20ffe-1286">public str toString()</span></span>                                                                                     | <span data-ttu-id="20ffe-1287">COMVariant オブジェクトの文字列形式を作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1287">Creates a string representation of a COMVariant object.</span></span> <span data-ttu-id="20ffe-1288">この文字列形式には、オブジェクトの値と型が含まれます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1288">This string representation includes the value and type of the object.</span></span>                                               |
| <span data-ttu-id="20ffe-1289">public int uInt(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1289">public int uInt(\[int newValue\])</span></span>                                                                         | <span data-ttu-id="20ffe-1290">VT\_UI4 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1290">Gets or sets the value of a COMVariant object of the VT\_UI4 data type.</span></span>                                                                                                     |
| <span data-ttu-id="20ffe-1291">public int uLong(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1291">public int uLong(\[int newValue\])</span></span>                                                                        | <span data-ttu-id="20ffe-1292">VT\_UI4 (未署名の longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1292">Gets or sets the value of a COMVariant object of the VT\_UI4 (unsigned long) data type.</span></span>                                                                                     |
| <span data-ttu-id="20ffe-1293">public Int64 uLongLong(\[Int64 newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1293">public Int64 uLongLong(\[Int64 newValue\])</span></span>                                                                | <span data-ttu-id="20ffe-1294">VT\_UI8 (未署名の longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1294">Gets or sets the value of a COMVariant object of the VT\_UI8 (unsigned longlong) data type.</span></span>                                                                                 |
| <span data-ttu-id="20ffe-1295">public int uShort(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1295">public int uShort(\[int newValue\])</span></span>                                                                       | <span data-ttu-id="20ffe-1296">VT\_UI2 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1296">Gets or sets the value of a COMVariant object of the VT\_UI2 data type.</span></span>                                                                                                     |
| <span data-ttu-id="20ffe-1297">public COMVariant variant(\[COMVariant newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1297">public COMVariant variant(\[COMVariant newValue\])</span></span>                                                        | <span data-ttu-id="20ffe-1298">VT\_VARIANT (バリアント) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1298">Gets or sets the value of a COMVariant object of the VT\_VARIANT (variant) data type.</span></span>                                                                                       |
| <span data-ttu-id="20ffe-1299">public COMVariantInOut variantInOutFlag(\[COMVariantInOut newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1299">public COMVariantInOut variantInOutFlag(\[COMVariantInOut newValue\])</span></span>                                     | <span data-ttu-id="20ffe-1300">COMVariant オブジェクトに対する InOutFlag 設定を設定する返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1300">Sets or returns the InOutFlag setting for a COMVariant object.</span></span>                                                                                                              |
| <span data-ttu-id="20ffe-1301">public COMVariantType variantType(\[COMVariantType newValue\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1301">public COMVariantType variantType(\[COMVariantType newValue\])</span></span>                                            | <span data-ttu-id="20ffe-1302">COMVariant オブジェクトにそのバリアント データ型を照会するか、データ型を変更します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1302">Queries a COMVariant object for its variant data type or changes the data type.</span></span>                                                                                             |
| <span data-ttu-id="20ffe-1303">::public static COMVariant createDateFromYMD(int year, int month, int day, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1303">::public static COMVariant createDateFromYMD(int year, int month, int day, \[COMVariantInOut inOutFlag\])</span></span> | <span data-ttu-id="20ffe-1304">新しい COMVariant オブジェクトを作成し、1 回の操作で日付値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1304">Creates a new COMVariant object and initializes it with a date value in one operation.</span></span>                                                                                      |
| <span data-ttu-id="20ffe-1305">::public static COMVariant createFromArray(Array value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1305">::public static COMVariant createFromArray(Array value, \[COMVariantInOut inOutFlag\])</span></span>                    | <span data-ttu-id="20ffe-1306">新しい COMVariant オブジェクトを作成し、1 回の操作で配列で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1306">Creates a new COMVariant object and initializes it with an array in one operation.</span></span>                                                                                          |
| <span data-ttu-id="20ffe-1307">::public static COMVariant createFromBoolean(boolean value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1307">::public static COMVariant createFromBoolean(boolean value, \[COMVariantInOut inOutFlag\])</span></span>                | <span data-ttu-id="20ffe-1308">新しい COMVariant オブジェクトを作成し、1 回の操作でブール値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1308">Creates a new COMVariant object and initializes it with a Boolean value in one operation.</span></span>                                                                                   |
| <span data-ttu-id="20ffe-1309">::public static COMVariant createFromCOM(COM value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1309">::public static COMVariant createFromCOM(COM value, \[COMVariantInOut inOutFlag\])</span></span>                        | <span data-ttu-id="20ffe-1310">新しい COMVariant オブジェクトを作成し、1 回の操作で COM クラスで初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1310">Creates a new COMVariant object and initializes it with a COM class in one operation.</span></span>                                                                                       |
| <span data-ttu-id="20ffe-1311">::public static COMVariant createFromDate(Date value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1311">::public static COMVariant createFromDate(Date value, \[COMVariantInOut inOutFlag\])</span></span>                      | <span data-ttu-id="20ffe-1312">新しい COMVariant オブジェクトを作成し、1 回の操作で日付値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1312">Creates a new COMVariant object and initializes it with a date value in one operation.</span></span>                                                                                      |
| <span data-ttu-id="20ffe-1313">::public static COMVariant createFromDateAndTime(Date date, int time, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1313">::public static COMVariant createFromDateAndTime(Date date, int time, \[COMVariantInOut inOutFlag\])</span></span>      | <span data-ttu-id="20ffe-1314">新しい COMVariant オブジェクトを作成し、1 回の操作で日時で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1314">Creates a new COMVariant object and initializes it with a date and time in one operation.</span></span>                                                                                   |
| <span data-ttu-id="20ffe-1315">::public static COMVariant createFromInt(int value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1315">::public static COMVariant createFromInt(int value, \[COMVariantInOut inOutFlag\])</span></span>                        | <span data-ttu-id="20ffe-1316">新しい COMVariant オブジェクトを作成し、1 回の操作で整数値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1316">Creates a new COMVariant object and initializes it with an integer value in one operation.</span></span>                                                                                  |
| <span data-ttu-id="20ffe-1317">::public static COMVariant createFromInt64(Int64 value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1317">::public static COMVariant createFromInt64(Int64 value, \[COMVariantInOut inOutFlag\])</span></span>                    | <span data-ttu-id="20ffe-1318">新しい COMVariant オブジェクトを作成し、1 回の操作でint64 値 (longLong や uLongLong) で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1318">Creates a new COMVariant object and initializes it with an int64 value (longLong or uLongLong) in one operation.</span></span>                                                            |
| <span data-ttu-id="20ffe-1319">::public static COMVariant createFromReal(Real value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1319">::public static COMVariant createFromReal(Real value, \[COMVariantInOut inOutFlag\])</span></span>                      | <span data-ttu-id="20ffe-1320">新しい COMVariant オブジェクトを作成し、1 回の操作で実際の値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1320">Creates a new COMVariant object and initializes it with a real value in one operation.</span></span>                                                                                      |
| <span data-ttu-id="20ffe-1321">::public static COMVariant createFromStr(str value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1321">::public static COMVariant createFromStr(str value, \[COMVariantInOut inOutFlag\])</span></span>                        | <span data-ttu-id="20ffe-1322">新しい COMVariant オブジェクトを作成し、1 回の操作で文字列で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1322">Creates a new COMVariant object and initializes it with a string in one operation.</span></span>                                                                                          |
| <span data-ttu-id="20ffe-1323">::public static COMVariant createFromTime(int value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1323">::public static COMVariant createFromTime(int value, \[COMVariantInOut inOutFlag\])</span></span>                       | <span data-ttu-id="20ffe-1324">新しい COMVariant オブジェクトを作成し、1 回の操作で時刻値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1324">Creates a new COMVariant object and initializes it with a time value in one operation.</span></span>                                                                                      |
| <span data-ttu-id="20ffe-1325">::public static COMVariant createFromUtcDateTime(DateTime value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1325">::public static COMVariant createFromUtcDateTime(DateTime value, \[COMVariantInOut inOutFlag\])</span></span>           |                                                                                                                                                                             |
| <span data-ttu-id="20ffe-1326">::public static COMVariant createNoValue()</span><span class="sxs-lookup"><span data-stu-id="20ffe-1326">::public static COMVariant createNoValue()</span></span>                                                                | <span data-ttu-id="20ffe-1327">値を持たない VT\_エラー バリアント タイプの COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1327">Creates a COMVariant object of the VT\_ERROR variant type with no value.</span></span>                                                                                                    |
| <span data-ttu-id="20ffe-1328">public void new(\[COMVariantInOut inOutFlag\], \[COMVariantType type\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-1328">public void new(\[COMVariantInOut inOutFlag\], \[COMVariantType type\])</span></span>                                   | <span data-ttu-id="20ffe-1329">COM オートメーション オブジェクトのメソッドまたはプロパティに引数を渡すために使用できる COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1329">Creates a COMVariant object that can be used to pass arguments to the methods or properties of a COM Automation object.</span></span>                                                     |
| <span data-ttu-id="20ffe-1330">public void noValue()</span><span class="sxs-lookup"><span data-stu-id="20ffe-1330">public void noValue()</span></span>                                                                                     | <span data-ttu-id="20ffe-1331">既存の COMVariant オブジェクトの内容を削除し、COMDispFunction.call メソッドまたは COM クラスで使用されている場合は、未指定の引数として機能させることができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1331">Deletes the contents of an existing COMVariant object and enables it to act as an unspecified argument when it is used in the COMDispFunction.call method or the COM class.</span></span> |
| <span data-ttu-id="20ffe-1332">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="20ffe-1332">public void finalize()</span></span>                                                                                    | <span data-ttu-id="20ffe-1333">実装されていません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1333">Not implemented.</span></span> <span data-ttu-id="20ffe-1334">明示的にオブジェクトを破棄する必要がある場合は、このメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1334">You can override this method if you need to explicitly destruct an object.</span></span>                                                                                 |

### <a name="method-boolean"></a><span data-ttu-id="20ffe-1335">メソッド boolean</span><span class="sxs-lookup"><span data-stu-id="20ffe-1335">Method boolean</span></span>

<span data-ttu-id="20ffe-1336">VT\_BOOL データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1336">Gets or sets the value of a COMVariant object of the VT\_BOOL data type.</span></span>

    public boolean boolean([boolean newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1337">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1337">Parameters</span></span>

<span data-ttu-id="20ffe-1338">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1338">newValue</span></span>  
<span data-ttu-id="20ffe-1339">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1339">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1340">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1340">Return Value</span></span>

<span data-ttu-id="20ffe-1341">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1341">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1342">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1342">Remarks</span></span>

<span data-ttu-id="20ffe-1343">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1343">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1344">データ型が COMVariantType::VT\_BOOL に設定されている場合、その COMVariant オブジェクトはブール型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1344">A COMVariant object has a Boolean type if its data type is set to COMVariantType::VT\_BOOL.</span></span> <span data-ttu-id="20ffe-1345">COM ブール値のデータ型は、"VARIANT\_BOOL" とも呼ばれることがあります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1345">The COM Boolean data type may also be referred to as "VARIANT\_BOOL".</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1346">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1346">Examples</span></span>

<span data-ttu-id="20ffe-1347">次の例では、VT\_BOOL 型の新しい COMVariant オブジェクトを作成し、値を true に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1347">The following example creates a new COMVariant object of type VT\_BOOL and sets the value to true.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_BOOL); 

        // Set value of the object 
        var.boolean(true); 
    }

### <a name="method-bstr"></a><span data-ttu-id="20ffe-1348">メソッド bStr</span><span class="sxs-lookup"><span data-stu-id="20ffe-1348">Method bStr</span></span>

<span data-ttu-id="20ffe-1349">VT\_BSTR データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1349">Gets or sets the value of a COMVariant object of the VT\_BSTR data type.</span></span>

    public str bStr([str newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1350">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1350">Parameters</span></span>

<span data-ttu-id="20ffe-1351">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1351">newValue</span></span>  
<span data-ttu-id="20ffe-1352">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1352">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1353">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1353">Return Value</span></span>

<span data-ttu-id="20ffe-1354">現在の文字列の価値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1354">The current string value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1355">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1355">Remarks</span></span>

<span data-ttu-id="20ffe-1356">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1356">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1357">データ型が COMVariantType::VT\_BSTR に設定されている場合、その COMVariant オブジェクトは文字列データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1357">A COMVariant object has a string data type if its data type is set to COMVariantType::VT\_BSTR.</span></span> <span data-ttu-id="20ffe-1358">BStr データ型は、文字列の処理に使用される COM データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1358">The BStr data type is a COM data type that is used for handling strings.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1359">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1359">Examples</span></span>

<span data-ttu-id="20ffe-1360">次の例では、VT\_BSTR 型の新しい COMVariant オブジェクトを作成し、値を "Hello World" に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1360">The following example creates a new COMVariant object of type VT\_BSTR, and sets the value to "Hello World."</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_BSTR); 

        // Set string value of the object 
        var.bStr("Hello World"); 
    }

### <a name="method-byte"></a><span data-ttu-id="20ffe-1361">メソッド byte</span><span class="sxs-lookup"><span data-stu-id="20ffe-1361">Method byte</span></span>

<span data-ttu-id="20ffe-1362">VT\_UI1 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1362">Gets or sets the value of a COMVariant object of the VT\_UI1 data type.</span></span>

    public int byte([int newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1363">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1363">Parameters</span></span>

<span data-ttu-id="20ffe-1364">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1364">newValue</span></span>  
<span data-ttu-id="20ffe-1365">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1365">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1366">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1366">Return Value</span></span>

<span data-ttu-id="20ffe-1367">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1367">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1368">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1368">Remarks</span></span>

<span data-ttu-id="20ffe-1369">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1369">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1370">データ型が COMVariantType::VT\_UI1 に設定されている場合、その COMVariant オブジェクトは byte データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1370">A COMVariant object has a byte data type if its data type is set to COMVariantType::VT\_UI1.</span></span> <span data-ttu-id="20ffe-1371">また、「符号なし文字型」を使用して COM バイト データ型を参照することができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1371">You can also use "unsigned char" to refer to the COM byte data type.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1372">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1372">Examples</span></span>

<span data-ttu-id="20ffe-1373">次の例では、VT\_UI1 型の新しい COMVariant オブジェクトを作成し、値を 123 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1373">The following example creates a new COMVariant object of the VT\_UI1 type and sets the value to 123.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_UI1); 

        // Set value of the object 
        var.byte(123); 
    }

### <a name="method-char"></a><span data-ttu-id="20ffe-1374">メソッド char</span><span class="sxs-lookup"><span data-stu-id="20ffe-1374">Method char</span></span>

<span data-ttu-id="20ffe-1375">VT\_I1 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1375">Gets or sets the value of a COMVariant object of the VT\_I1 data type.</span></span>

    public int char([int newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1376">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1376">Parameters</span></span>

<span data-ttu-id="20ffe-1377">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1377">newValue</span></span>  
<span data-ttu-id="20ffe-1378">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1378">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1379">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1379">Return Value</span></span>

<span data-ttu-id="20ffe-1380">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1380">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1381">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1381">Remarks</span></span>

<span data-ttu-id="20ffe-1382">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1382">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1383">データ型が COMVariantType::VT\_I1 に設定されている場合、その COMVariant オブジェクトは char データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1383">A COMVariant object has a char data type if its data type is set to COMVariantType::VT\_I1.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1384">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1384">Examples</span></span>

<span data-ttu-id="20ffe-1385">次の例では、VT\_I1 型の 新しい COMVariant オブジェクトを作成し、値を 65 の、A の数値に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1385">The following example creates a new COMVariant object of type VT\_I1 and sets the value to the numeric value of A, which is 65.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_I1); 

        // Set value of the object 
        var.char(Char2Num("A", 1)); 
    }

### <a name="method-container"></a><span data-ttu-id="20ffe-1386">メソッド container</span><span class="sxs-lookup"><span data-stu-id="20ffe-1386">Method container</span></span>

<span data-ttu-id="20ffe-1387">コンテナ データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1387">Gets or sets the value of a COMVariant object of the container data type.</span></span>

    public container container([container newValue], [COMVariantType newType])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1388">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1388">Parameters</span></span>

<span data-ttu-id="20ffe-1389">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1389">newValue</span></span>  
<span data-ttu-id="20ffe-1390">新しいコンテナーのタイプ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1390">The type of the new container; optional.</span></span> <span data-ttu-id="20ffe-1391">既定では、コンテナーが整数を格納します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1391">The default is for the container to store integers.</span></span>

<!-- -->

<span data-ttu-id="20ffe-1392">newType</span><span class="sxs-lookup"><span data-stu-id="20ffe-1392">newType</span></span>  
<span data-ttu-id="20ffe-1393">新しいコンテナーのタイプ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1393">The type of the new container; optional.</span></span> <span data-ttu-id="20ffe-1394">既定では、コンテナーが整数を格納します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1394">The default is for the container to store integers.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1395">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1395">Return Value</span></span>

<span data-ttu-id="20ffe-1396">現在のコンテナー。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1396">The current container.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1397">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1397">Remarks</span></span>

<span data-ttu-id="20ffe-1398">newType パラメーターの使用可能な値は、COMVariantType システム列挙によって提供される値のサブセットです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1398">The possible values for the newType parameter are a subset of the values that are supplied by the COMVariantType system enum:</span></span>

-   <span data-ttu-id="20ffe-1399">VT\_I2</span><span class="sxs-lookup"><span data-stu-id="20ffe-1399">VT\_I2</span></span>
-   <span data-ttu-id="20ffe-1400">VT\_I4</span><span class="sxs-lookup"><span data-stu-id="20ffe-1400">VT\_I4</span></span>
-   <span data-ttu-id="20ffe-1401">VT\_R4</span><span class="sxs-lookup"><span data-stu-id="20ffe-1401">VT\_R4</span></span>
-   <span data-ttu-id="20ffe-1402">VT\_R8</span><span class="sxs-lookup"><span data-stu-id="20ffe-1402">VT\_R8</span></span>
-   <span data-ttu-id="20ffe-1403">VT\_CY</span><span class="sxs-lookup"><span data-stu-id="20ffe-1403">VT\_CY</span></span>
-   <span data-ttu-id="20ffe-1404">VT\_DATE</span><span class="sxs-lookup"><span data-stu-id="20ffe-1404">VT\_DATE</span></span>
-   <span data-ttu-id="20ffe-1405">VT\_BSTR</span><span class="sxs-lookup"><span data-stu-id="20ffe-1405">VT\_BSTR</span></span>
-   <span data-ttu-id="20ffe-1406">VT\_ERROR</span><span class="sxs-lookup"><span data-stu-id="20ffe-1406">VT\_ERROR</span></span>
-   <span data-ttu-id="20ffe-1407">VT\_BOOL</span><span class="sxs-lookup"><span data-stu-id="20ffe-1407">VT\_BOOL</span></span>
-   <span data-ttu-id="20ffe-1408">VT\_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="20ffe-1408">VT\_DECIMAL</span></span>
-   <span data-ttu-id="20ffe-1409">VT\_I1</span><span class="sxs-lookup"><span data-stu-id="20ffe-1409">VT\_I1</span></span>
-   <span data-ttu-id="20ffe-1410">VT\_UI1</span><span class="sxs-lookup"><span data-stu-id="20ffe-1410">VT\_UI1</span></span>
-   <span data-ttu-id="20ffe-1411">VT\_UI2</span><span class="sxs-lookup"><span data-stu-id="20ffe-1411">VT\_UI2</span></span>
-   <span data-ttu-id="20ffe-1412">VT\_UI4</span><span class="sxs-lookup"><span data-stu-id="20ffe-1412">VT\_UI4</span></span>
-   <span data-ttu-id="20ffe-1413">VT\_I8</span><span class="sxs-lookup"><span data-stu-id="20ffe-1413">VT\_I8</span></span>
-   <span data-ttu-id="20ffe-1414">VT\_UI8</span><span class="sxs-lookup"><span data-stu-id="20ffe-1414">VT\_UI8</span></span>
-   <span data-ttu-id="20ffe-1415">VT\_INT</span><span class="sxs-lookup"><span data-stu-id="20ffe-1415">VT\_INT</span></span>
-   <span data-ttu-id="20ffe-1416">VT\_UINT</span><span class="sxs-lookup"><span data-stu-id="20ffe-1416">VT\_UINT</span></span>

<span data-ttu-id="20ffe-1417">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1417">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1418">コンテナーが COMVariant オブジェクトに保存されると、コンテナーのバイナリ表現がバイナリ配列に保存されます (COMVariant.safeArray メソッドを参照してください)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1418">When a container is stored in a COMVariant object, the binary representation of the container is stored in a binary array (see the COMVariant.safeArray method).</span></span> <span data-ttu-id="20ffe-1419">コンテナーのプロパティは、データベース COM オブジェクトにデータを格納し、後でデータを処理する COM オブジェクトを使用せずに Finance and Operations にデータを読み戻す必要がある場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1419">The container property is useful when you need to store data in a database COM object and then later read the data back into Finance and Operations without the COM object processing the data.</span></span> <span data-ttu-id="20ffe-1420">コンテナーのプロパティは、COMVariant クラスの高度なプロパティです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1420">The container property is an advanced property of the COMVariant class.</span></span> <span data-ttu-id="20ffe-1421">COMVariant オブジェクト内で、コンテナーが格納されるバイナリ配列の内容は、どの COM オブジェクトによっても変更されないようにしなければならないため、注意して使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1421">It should be used with caution because the content of the binary array that the container is stored in, inside the COMVariant object, must not be changed by any COM object.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1422">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1422">Examples</span></span>

<span data-ttu-id="20ffe-1423">次の例では、コンテナー 型の新しい COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1423">The following example creates a new COMVariant object of type container.</span></span> <span data-ttu-id="20ffe-1424">コンテナー内のデータは、データベース COM オブジェクトに渡され、データベース COM オブジェクトによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1424">The data in the container is passed to, and used by, a database COM object.</span></span> <span data-ttu-id="20ffe-1425">注記: 次のセクションのコードには仮想 COM オブジェクト (「MyDatabaseCOM.Object」) が含まれており、Finance and Operations の外部でオブジェクトが作成されていない限り、Finance and Operations では実行されません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1425">Note The code in the following section contains a hypothetical COM object MyDatabaseCOM.Object" and will therefore not run in Finance and Operations, unless such an object is created outside Finance and Operations.</span></span>

    { 
        COM com; 
        COMVariant var = new COMVariant(); 
        container con; 
        InteropPermission perm; 

        // Set code access permission to help protect use of COM object 
        perm = new InteropPermission(InteropKind::ComInterop); 
        if (perm == null) 
        { 
            return; 
        } 

        // Permission scope starts here 
        perm.assert(); 

        // Put some data in the container 
        con = conins(con, 1, "Element 1"); 
        con = conins(con, 2, "Element 2"); 
        // Set value of the object and ensure the data 
        // is stored in a binary array of bytes 
        var.container(con, COMVariantType::VT_UI1); 

        // Create a database object to store the data in 
        com = new COM("MyDatabaseCOM.Object"); 
        com.writeData(var); 
        // ... 

        // Close code access permission 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-currency"></a><span data-ttu-id="20ffe-1426">メソッド currency</span><span class="sxs-lookup"><span data-stu-id="20ffe-1426">Method currency</span></span>

<span data-ttu-id="20ffe-1427">VT\_CY データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1427">Gets or sets the value of a COMVariant object of the VT\_CY data type.</span></span>

    public Real currency([Real newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1428">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1428">Parameters</span></span>

<span data-ttu-id="20ffe-1429">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1429">newValue</span></span>  
<span data-ttu-id="20ffe-1430">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1430">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1431">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1431">Return Value</span></span>

<span data-ttu-id="20ffe-1432">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1432">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1433">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1433">Remarks</span></span>

<span data-ttu-id="20ffe-1434">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1434">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1435">データ型が COMVariantType::VT\_CY に設定されている場合、その COMVariant オブジェクトは通貨データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1435">A COMVariant object has a currency data type if its data type is set to COMVariantType::VT\_CY.</span></span> <span data-ttu-id="20ffe-1436">通貨データ型は、通貨値に最適化された COM データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1436">The currency data type is a COM data type that is optimized for currency values.</span></span> <span data-ttu-id="20ffe-1437">小数点以下 4 桁のある実数です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1437">It is a real number with four decimal places.</span></span> <span data-ttu-id="20ffe-1438">場合によっては、COM 通貨データ型を参照するために "CY" も使用されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1438">Sometimes "CY" is also used to refer to the COM currency data type.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1439">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1439">Examples</span></span>

<span data-ttu-id="20ffe-1440">次の例では、VT\_CY 型の新しい COMVariant オブジェクトを作成し、値を 123.4567 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1440">The following example creates a new COMVariant object of type VT\_CY and sets the value to 123.4567.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_CY); 

        // Set value of the object 
        var.currency(123.4567); 
    }

### <a name="method-date"></a><span data-ttu-id="20ffe-1441">メソッド date</span><span class="sxs-lookup"><span data-stu-id="20ffe-1441">Method date</span></span>

<span data-ttu-id="20ffe-1442">VT\_DATE データ タイプの COMVariant オブジェクトの値の日付部分を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1442">Gets or sets the date part of the value of a COMVariant object of the VT\_DATE data type.</span></span>

    public Date date([Date newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1443">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1443">Parameters</span></span>

<span data-ttu-id="20ffe-1444">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1444">newValue</span></span>  
<span data-ttu-id="20ffe-1445">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1445">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1446">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1446">Return Value</span></span>

<span data-ttu-id="20ffe-1447">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1447">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1448">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1448">Remarks</span></span>

<span data-ttu-id="20ffe-1449">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1449">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1450">データ型が COMVariantType::VT\_DATE に設定されている場合、その COMVariant オブジェクトは日時データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1450">A COMVariant object has a date and time data type if its data type is set to COMVariantType::VT\_DATE.</span></span> <span data-ttu-id="20ffe-1451">オブジェクトの値を設定するとき、日付に加えて、値の時刻の部分を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1451">When you set the value of the object, you must set the time part of the value in addition to the date.</span></span> <span data-ttu-id="20ffe-1452">値の時間部分を設定するには、time プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1452">To set the time part of the value, use the time property.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1453">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1453">Examples</span></span>

<span data-ttu-id="20ffe-1454">次の例では、VT\_DATE 型の COMVariant オブジェクトを作成し、値の日付部分を 1998 年 12 月 24 日に設定し、時刻の部分を 13.24 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1454">The following example creates a COMVariant object of type VT\_DATE and sets the date part of the value to 24 December 1998, and the time part of the value to 13.24.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_DATE); 

        // Set value of the object 
        var.date(Str2Date("12.24.1998", 213)); 
        var.time(Str2Time("13:24:00")); 
    }

### <a name="method-decimal"></a><span data-ttu-id="20ffe-1455">メソッド decimal</span><span class="sxs-lookup"><span data-stu-id="20ffe-1455">Method decimal</span></span>

<span data-ttu-id="20ffe-1456">VT\_DECIMAL データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1456">Gets or sets the value of a COMVariant object of the VT\_DECIMAL data type.</span></span>

    public Real decimal([Real newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1457">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1457">Parameters</span></span>

<span data-ttu-id="20ffe-1458">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1458">newValue</span></span>  
<span data-ttu-id="20ffe-1459">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1459">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1460">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1460">Return Value</span></span>

<span data-ttu-id="20ffe-1461">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1461">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1462">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1462">Remarks</span></span>

<span data-ttu-id="20ffe-1463">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1463">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1464">データ型が COMVariantType::VT\_DECIMAL に設定されている場合、その COMVariant オブジェクトは 10 進型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1464">A COMVariant object has a decimal type if its data type is set to COMVariantType::VT\_DECIMAL.</span></span> <span data-ttu-id="20ffe-1465">10進データ型は、数値のサイズとスケールを提供する COM データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1465">The decimal data type is a COM data type that provides size and scale for a number.</span></span> <span data-ttu-id="20ffe-1466">X++ には 10 進データ型と並行するものはありません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1466">There is no parallel to the decimal data type in X++.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1467">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1467">Examples</span></span>

<span data-ttu-id="20ffe-1468">次の例では、VT\_DECIMAL 型の新しい COMVariant オブジェクトを作成し、値を 123.456 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1468">The following example creates a new COMVariant object of type VT\_DECIMAL and sets the value to 123.456.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_DECIMAL); 

        // Set value of the object 
        var.decimal(123.456); 
    }

### <a name="method-double"></a><span data-ttu-id="20ffe-1469">メソッド double</span><span class="sxs-lookup"><span data-stu-id="20ffe-1469">Method double</span></span>

<span data-ttu-id="20ffe-1470">VT\_R8 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1470">Gets or sets the value of a COMVariant object of the VT\_R8 data type.</span></span>

    public Real double([Real newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1471">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1471">Parameters</span></span>

<span data-ttu-id="20ffe-1472">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1472">newValue</span></span>  
<span data-ttu-id="20ffe-1473">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1473">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1474">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1474">Return Value</span></span>

<span data-ttu-id="20ffe-1475">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1475">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1476">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1476">Remarks</span></span>

<span data-ttu-id="20ffe-1477">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1477">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1478">データ型が COMVariantType::VT\_R8 に設定されている場合、その COMVariant オブジェクトは double データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1478">A COMVariant object has a double data type if its data type is set to COMVariantType::VT\_R8.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1479">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1479">Examples</span></span>

<span data-ttu-id="20ffe-1480">次の例では、VT\_R8 型の新しい COMVariant オブジェクトを作成し、値を 123.456 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1480">The following example creates a new COMVariant object of type VT\_R8 and sets the value to 123.456.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_R8); 

        // Set value of the object 
        var.double(123.456); 
    }

### <a name="method-float"></a><span data-ttu-id="20ffe-1481">メソッド float</span><span class="sxs-lookup"><span data-stu-id="20ffe-1481">Method float</span></span>

<span data-ttu-id="20ffe-1482">VT\_R4 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1482">Gets or sets the value of a COMVariant object of the VT\_R4 data type.</span></span>

    public Real float([Real newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1483">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1483">Parameters</span></span>

<span data-ttu-id="20ffe-1484">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1484">newValue</span></span>  
<span data-ttu-id="20ffe-1485">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1485">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1486">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1486">Return Value</span></span>

<span data-ttu-id="20ffe-1487">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1487">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1488">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1488">Remarks</span></span>

<span data-ttu-id="20ffe-1489">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1489">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1490">データ型が COMVariantType::VT\_R4 に設定されている場合、COMVariant オブジェクトは float 型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1490">A COMVariant object has a float type if its data type is set to COMVariantType::VT\_R4.</span></span> <span data-ttu-id="20ffe-1491">場合によっては、COM 浮動小数点データ型を参照するために "single" も使用されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1491">Sometimes "single" is also used to refer to the COM float data type.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1492">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1492">Examples</span></span>

<span data-ttu-id="20ffe-1493">次の例では、VT\_R4 型の新しい COMVariant オブジェクトを作成し、値を 123.456 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1493">The following example creates a new COMVariant object of type VT\_R4 and sets the value to 123.456.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_R4); 

        // Set value of the object 
        var.float(123.456); 
    }

### <a name="method-idispatch"></a><span data-ttu-id="20ffe-1494">メソッド iDispatch</span><span class="sxs-lookup"><span data-stu-id="20ffe-1494">Method iDispatch</span></span>

<span data-ttu-id="20ffe-1495">VT\_DISPATCH データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1495">Gets or sets the value of a COMVariant object of the VT\_DISPATCH data type.</span></span>

    public ComInterface iDispatch([ComInterface newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1496">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1496">Parameters</span></span>

<span data-ttu-id="20ffe-1497">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1497">newValue</span></span>  
<span data-ttu-id="20ffe-1498">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1498">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1499">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1499">Return Value</span></span>

<span data-ttu-id="20ffe-1500">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1500">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1501">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1501">Remarks</span></span>

<span data-ttu-id="20ffe-1502">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1502">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1503">データ型が COMVariantType::VT\_DISPATCH に設定されている場合、その COMVariant オブジェクトは IDispatch データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1503">A COMVariant object has an IDispatch data type if its data type is set to COMVariantType::VT\_DISPATCH.</span></span> <span data-ttu-id="20ffe-1504">IDispatch データ型は、COM IDispatch インターフェイスへのハンドルを提供する COM データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1504">The IDispatch data type is a COM data type that provides a handle to a COM IDispatch interface.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1505">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1505">Examples</span></span>

<span data-ttu-id="20ffe-1506">次の例では、VT\_DISPATCH 型の新しい COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1506">The following example creates a new COMVariant object of type VT\_DISPATCH.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_DISPATCH); 
        COMInterface comInterface; 

        // Here, the comInterface variable must be assigned 
        // a COM IDispatch interface 
        //… 

        // Set value of the object 
        var.iDispatch(comInterface); 
    }

### <a name="method-int"></a><span data-ttu-id="20ffe-1507">メソッド int</span><span class="sxs-lookup"><span data-stu-id="20ffe-1507">Method int</span></span>

<span data-ttu-id="20ffe-1508">VT\_I4 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1508">Gets or sets the value of a COMVariant object of the VT\_I4 data type.</span></span>

    public int int([int newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1509">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1509">Parameters</span></span>

<span data-ttu-id="20ffe-1510">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1510">newValue</span></span>  
<span data-ttu-id="20ffe-1511">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1511">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1512">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1512">Return Value</span></span>

<span data-ttu-id="20ffe-1513">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1513">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1514">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1514">Remarks</span></span>

<span data-ttu-id="20ffe-1515">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1515">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1516">COMVariantType::VT\_I4 データ型は long バリアント型にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1516">The COMVariantType::VT\_I4 data type is also used for the long variant type.</span></span> <span data-ttu-id="20ffe-1517">COMVariant.long メソッドは、このメソッドと同じです。2 つのメソッドは、完全性のために存在します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1517">The COMVariant.long method is identical to this method; the two methods exist for completeness.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1518">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1518">Examples</span></span>

<span data-ttu-id="20ffe-1519">次の例では、VT\_I4 型の COMVariant オブジェクトを作成し、値を 123456 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1519">The following example creates a COMVariant object of type VT\_I4 and sets the value to 123456.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_I4); 

        // Set value of the object 
        var.int(123456); 
    }

### <a name="method-iunknown"></a><span data-ttu-id="20ffe-1520">メソッド iUnknown</span><span class="sxs-lookup"><span data-stu-id="20ffe-1520">Method iUnknown</span></span>

<span data-ttu-id="20ffe-1521">VT\_UNKNOWN (IUnknown) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1521">Gets or sets the value of a COMVariant object of the VT\_UNKNOWN (IUnknown) data type.</span></span>

    public ComInterface iUnknown([ComInterface newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1522">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1522">Parameters</span></span>

<span data-ttu-id="20ffe-1523">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1523">newValue</span></span>  
<span data-ttu-id="20ffe-1524">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1524">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1525">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1525">Return Value</span></span>

<span data-ttu-id="20ffe-1526">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1526">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1527">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1527">Remarks</span></span>

<span data-ttu-id="20ffe-1528">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、データ型の値に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1528">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type value.</span></span> <span data-ttu-id="20ffe-1529">データ型が COMVariantType::VT\_UNKNOWN に設定されている場合、COMVariant オブジェクトは IUnknown データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1529">A COMVariant object has an IUnknown data type if its data type is set to COMVariantType::VT\_UNKNOWN.</span></span> <span data-ttu-id="20ffe-1530">IUnknown データ型は、COM IUnknown インターフェイスへのハンドルを提供する COM データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1530">The IUnknown data type is a COM data type that provides a handle to a COM IUnknown interface.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1531">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1531">Examples</span></span>

<span data-ttu-id="20ffe-1532">次の例では、VT\_UNKNOWN 型の新しい COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1532">The following example creates a new COMVariant object of type VT\_UNKNOWN.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_UNKNOWN); 
        COMInterface comInterface; 

        // comInterface variable is assigned 
        // a COM IUnknown interface 
        // ... 

        // Set value of the object 
        var.iUnknown(comInterface); 
    }

### <a name="method-long"></a><span data-ttu-id="20ffe-1533">メソッド long</span><span class="sxs-lookup"><span data-stu-id="20ffe-1533">Method long</span></span>

<span data-ttu-id="20ffe-1534">VT\_I4 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1534">Gets or sets the value of a COMVariant object of the VT\_I4 data type.</span></span>

    public int long([int newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1535">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1535">Parameters</span></span>

<span data-ttu-id="20ffe-1536">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1536">newValue</span></span>  
<span data-ttu-id="20ffe-1537">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1537">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1538">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1538">Return Value</span></span>

<span data-ttu-id="20ffe-1539">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1539">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1540">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1540">Remarks</span></span>

<span data-ttu-id="20ffe-1541">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1541">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1542">COMVariantType::VT\_I4 データ型は int バリアント型にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1542">The COMVariantType::VT\_I4 data type is also used for the int variant type.</span></span> <span data-ttu-id="20ffe-1543">COMVariant.int メソッドは、このメソッドと同じです。2 つのメソッドは、完全性のために存在します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1543">The COMVariant.int method is identical to this method; the two methods exist for completeness.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1544">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1544">Examples</span></span>

<span data-ttu-id="20ffe-1545">次の例では、VT\_I4 型の COMVariant オブジェクトを作成し、値を 123456 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1545">The following example creates a COMVariant object of type VT\_I4 and sets the value to 123456.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_I4); 

        // Set value of the object 
        var.long(123456); 
    }

### <a name="method-longlong"></a><span data-ttu-id="20ffe-1546">メソッド longLong</span><span class="sxs-lookup"><span data-stu-id="20ffe-1546">Method longLong</span></span>

<span data-ttu-id="20ffe-1547">VT\_I8 (longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1547">Gets or sets the value of a COMVariant object of the VT\_I8 (longlong) data type.</span></span>

    public Int64 longLong([Int64 newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1548">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1548">Parameters</span></span>

<span data-ttu-id="20ffe-1549">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1549">newValue</span></span>  
<span data-ttu-id="20ffe-1550">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1550">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1551">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1551">Return Value</span></span>

<span data-ttu-id="20ffe-1552">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1552">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1553">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1553">Remarks</span></span>

<span data-ttu-id="20ffe-1554">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1554">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the value’s data type.</span></span> <span data-ttu-id="20ffe-1555">データ型が COMVariantType::VT\_I8 に設定されている場合、その COMVariant オブジェクトは longlong バリアント型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1555">A COMVariant object has a longlong variant type if its data type is set to COMVariantType::VT\_I8.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1556">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1556">Examples</span></span>

<span data-ttu-id="20ffe-1557">次の例では、VT\_I8 型の新しい COMVariant オブジェクトを作成し、値を 2,305,843,009,213,693,952 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1557">The following example creates a new COMVariant object of type VT\_I8 and sets the value to 2,305,843,009,213,693,952.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_BOOL); 

        // Set value of the object 
        var.longLong(2305843009213693952); 
    }

### <a name="method-safearray"></a><span data-ttu-id="20ffe-1558">メソッド safeArray</span><span class="sxs-lookup"><span data-stu-id="20ffe-1558">Method safeArray</span></span>

<span data-ttu-id="20ffe-1559">VT\_SAFEARRAY データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1559">Gets or sets the value of a COMVariant object of the VT\_SAFEARRAY data type.</span></span>

    public Array safeArray([Array newValue], [COMVariantType newType])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1560">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1560">Parameters</span></span>

<span data-ttu-id="20ffe-1561">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1561">newValue</span></span>  
<span data-ttu-id="20ffe-1562">新しい配列のタイプ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1562">The type of the new array; optional.</span></span>

<!-- -->

<span data-ttu-id="20ffe-1563">newType</span><span class="sxs-lookup"><span data-stu-id="20ffe-1563">newType</span></span>  
<span data-ttu-id="20ffe-1564">新しい配列のタイプ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1564">The type of the new array; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1565">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1565">Return Value</span></span>

<span data-ttu-id="20ffe-1566">現在の配列。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1566">The current array.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1567">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1567">Remarks</span></span>

<span data-ttu-id="20ffe-1568">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1568">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1569">データ型が COMVariantType::VT\_SAFEARRAY に設定されている場合、その COMVariant オブジェクトは配列ブール型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1569">A COMVariant object has an array Boolean type if its data type is set to COMVariantType::VT\_SAFEARRAY.</span></span> <span data-ttu-id="20ffe-1570">セーフ配列は、COM の配列に相当します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1570">A safe array is COM's equivalent to an array.</span></span> <span data-ttu-id="20ffe-1571">現在、1 次元セーフ配列のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1571">Currently only one-dimensional safe arrays are supported.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1572">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1572">Examples</span></span>

<span data-ttu-id="20ffe-1573">次の例では、VT\_SAFEARRAY 型の新しい COMVariant オブジェクトを作成し、short 配列で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1573">The following example creates a new COMVariant object of type VT\_SAFEARRAY and initializes it with an array of shorts.</span></span>

    { 
        int i, result; 
        COM com; 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_SAFEARRAY); 
        Array arr = new Array(Types::INTEGER); 

        // Insert 10 values in the array 
        for (i = 1; i <= 10; i++) 
        { 
            arr.value(i, i); 
        } 

        // Set value of the object and ensure the integer values 
        // are treated as short data types 
        var.safeArray(arr, COMVariantType::VT_I2); 
    }

### <a name="method-scode"></a><span data-ttu-id="20ffe-1574">メソッド sCode</span><span class="sxs-lookup"><span data-stu-id="20ffe-1574">Method sCode</span></span>

<span data-ttu-id="20ffe-1575">VT\_ERROR データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1575">Gets or sets the value of a COMVariant object of the VT\_ERROR data type.</span></span>

    public int sCode([int newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1576">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1576">Parameters</span></span>

<span data-ttu-id="20ffe-1577">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1577">newValue</span></span>  
<span data-ttu-id="20ffe-1578">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1578">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1579">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1579">Return Value</span></span>

<span data-ttu-id="20ffe-1580">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1580">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1581">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1581">Remarks</span></span>

<span data-ttu-id="20ffe-1582">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1582">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1583">データ型が COMVariantType::VT\_ERROR に設定されている場合、その COMVariant オブジェクトは scode データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1583">A COMVariant object has an scode data type if its data type is set to COMVariantType::VT\_ERROR.</span></span> <span data-ttu-id="20ffe-1584">scode データ型は、COM 関数の戻り値として最もよく使用される Win32 HRESULT データ型と同等の COM データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1584">The scode data type is a COM data type that is equivalent to the Win32 HRESULT data type, which is most used as return values for COM functions.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1585">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1585">Examples</span></span>

<span data-ttu-id="20ffe-1586">次の例では、VT\_ERROR 型の新しい COMVariant オブジェクトを作成し、値を 0x80001004 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1586">The following example creates a new COMVariant object of type VT\_ERROR and sets the value to 0x80001004.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_ERROR); 

        // Set value of the object 
        var.sCode(0x80001004); 
    }

### <a name="method-short"></a><span data-ttu-id="20ffe-1587">メソッド short</span><span class="sxs-lookup"><span data-stu-id="20ffe-1587">Method short</span></span>

<span data-ttu-id="20ffe-1588">VT\_I2 (短い) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1588">Gets or sets the value of a COMVariant object of the VT\_I2 (short) data type.</span></span>

    public int short([int newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1589">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1589">Parameters</span></span>

<span data-ttu-id="20ffe-1590">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1590">newValue</span></span>  
<span data-ttu-id="20ffe-1591">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1591">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1592">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1592">Return Value</span></span>

<span data-ttu-id="20ffe-1593">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1593">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1594">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1594">Remarks</span></span>

<span data-ttu-id="20ffe-1595">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1595">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1596">データ型が COMVariantType::VT\_I2 に設定されている場合、その COMVariant オブジェクトは short データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1596">A COMVariant object has a short data type if its data type is set to COMVariantType::VT\_I2.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1597">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1597">Examples</span></span>

<span data-ttu-id="20ffe-1598">次の例では、VT\_I2 型の新しい COMVariant オブジェクトを作成し、値を 123 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1598">The following example creates a new COMVariant object of the VT\_I2 type and sets the value to 123.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_I2); 

        // Set value of the object 
        var.short(123); 
    }

### <a name="method-time"></a><span data-ttu-id="20ffe-1599">メソッド time</span><span class="sxs-lookup"><span data-stu-id="20ffe-1599">Method time</span></span>

<span data-ttu-id="20ffe-1600">VT\_DATE データ タイプの COMVariant オブジェクトの値の時刻部分を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1600">Gets or sets the time part of the value of a COMVariant object of the VT\_DATE data type.</span></span>

    public int time([int newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1601">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1601">Parameters</span></span>

<span data-ttu-id="20ffe-1602">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1602">newValue</span></span>  
<span data-ttu-id="20ffe-1603">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1603">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1604">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1604">Return Value</span></span>

<span data-ttu-id="20ffe-1605">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1605">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1606">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1606">Remarks</span></span>

<span data-ttu-id="20ffe-1607">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1607">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1608">データ型が COMVariantType::VT\_DATE に設定されている場合、その COMVariant オブジェクトは日時データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1608">A COMVariant object has a date and time data type if its data type is set to COMVariantType::VT\_DATE.</span></span> <span data-ttu-id="20ffe-1609">オブジェクトの値を設定するとき、時刻に加えて、値の日付の部分を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1609">When you set the value of the object, you must set the date part of the value in addition to the time.</span></span> <span data-ttu-id="20ffe-1610">値の日付部分を設定するには、date プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1610">To set the date part of the value, use the date property.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1611">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1611">Examples</span></span>

<span data-ttu-id="20ffe-1612">次の例では、VT\_DATE 型の COMVariant オブジェクトを作成し、値の日付部分を 1998 年 12 月 24 日に設定し、時刻の部分を 13.24 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1612">The following example creates a COMVariant object of type VT\_DATE and sets the date part of the value to 24 December 1998, and the time part of the value to 13.24.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_DATE); 

        // Set value of the object 
        var.date(Str2Date("12.24.1998", 213)); 
        var.time(Str2Time("13:24:00")); 
    }

### <a name="method-tostring"></a><span data-ttu-id="20ffe-1613">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="20ffe-1613">Method toString</span></span>

<span data-ttu-id="20ffe-1614">COMVariant オブジェクトの文字列形式を作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1614">Creates a string representation of a COMVariant object.</span></span> <span data-ttu-id="20ffe-1615">この文字列形式には、オブジェクトの値と型が含まれます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1615">This string representation includes the value and type of the object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="20ffe-1616">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1616">Return Value</span></span>

<span data-ttu-id="20ffe-1617">COMVariant オブジェクトの文字列表現。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1617">The string representation of the COMVariant object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1618">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1618">Remarks</span></span>

<span data-ttu-id="20ffe-1619">このメソッドから返される実際の文字列は、COMVariant オブジェクトのバリアント データ型によって異なります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1619">The actual string returned from this method depends on the variant data type of the COMVariant object.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1620">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1620">Examples</span></span>

<span data-ttu-id="20ffe-1621">次の例では、COMVariant オブジェクトを作成し、現在の日付を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1621">The following example creates a COMVariant object and assigns the current date to it.</span></span> <span data-ttu-id="20ffe-1622">情報ログにオブジェクトの説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1622">It then prints a description of the object to the Infolog.</span></span>

    COMVariant theDay; 

    theDay = COMVariant::createFromDate(today()); 
    info(theDay.toString());

### <a name="method-uint"></a><span data-ttu-id="20ffe-1623">メソッド uInt</span><span class="sxs-lookup"><span data-stu-id="20ffe-1623">Method uInt</span></span>

<span data-ttu-id="20ffe-1624">VT\_UI4 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1624">Gets or sets the value of a COMVariant object of the VT\_UI4 data type.</span></span>

    public int uInt([int newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1625">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1625">Parameters</span></span>

<span data-ttu-id="20ffe-1626">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1626">newValue</span></span>  
<span data-ttu-id="20ffe-1627">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1627">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1628">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1628">Return Value</span></span>

<span data-ttu-id="20ffe-1629">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1629">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1630">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1630">Remarks</span></span>

<span data-ttu-id="20ffe-1631">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1631">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1632">COMVariantType::VT\_UI4 データ型は uLong データ型にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1632">The COMVariantType::VT\_UI4 data type is also used for the uLong data type.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1633">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1633">Examples</span></span>

<span data-ttu-id="20ffe-1634">次の例では、VT\_UI4 型の新しい COMVariant オブジェクトを作成し、値を 123456 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1634">The following example creates a new COMVariant object of the VT\_UI4 type and sets the value to 123456.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_UI4); 

        // Set value of the object 
        var.uInt(123456); 
    }

### <a name="method-ulong"></a><span data-ttu-id="20ffe-1635">メソッド uLong</span><span class="sxs-lookup"><span data-stu-id="20ffe-1635">Method uLong</span></span>

<span data-ttu-id="20ffe-1636">VT\_UI4 (未署名の longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1636">Gets or sets the value of a COMVariant object of the VT\_UI4 (unsigned long) data type.</span></span>

    public int uLong([int newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1637">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1637">Parameters</span></span>

<span data-ttu-id="20ffe-1638">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1638">newValue</span></span>  
<span data-ttu-id="20ffe-1639">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1639">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1640">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1640">Return Value</span></span>

<span data-ttu-id="20ffe-1641">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1641">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1642">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1642">Remarks</span></span>

<span data-ttu-id="20ffe-1643">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1643">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1644">COMVariantType::VT\_UI4 データ型は uInt データ型にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1644">The COMVariantType::VT\_UI4 data type is also used for the uInt data type.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1645">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1645">Examples</span></span>

<span data-ttu-id="20ffe-1646">次の例では、VT\_UI4 型の新しい COMVariant オブジェクトを作成し、値を 123456 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1646">The following example creates a new COMVariant object of type VT\_UI4 and sets the value to 123456.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_UI4); 

        // set value of the object 
        var.uLong(123456); 
    }

### <a name="method-ulonglong"></a><span data-ttu-id="20ffe-1647">メソッド uLongLong</span><span class="sxs-lookup"><span data-stu-id="20ffe-1647">Method uLongLong</span></span>

<span data-ttu-id="20ffe-1648">VT\_UI8 (未署名の longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1648">Gets or sets the value of a COMVariant object of the VT\_UI8 (unsigned longlong) data type.</span></span>

    public Int64 uLongLong([Int64 newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1649">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1649">Parameters</span></span>

<span data-ttu-id="20ffe-1650">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1650">newValue</span></span>  
<span data-ttu-id="20ffe-1651">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1651">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1652">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1652">Return Value</span></span>

<span data-ttu-id="20ffe-1653">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1653">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1654">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1654">Remarks</span></span>

<span data-ttu-id="20ffe-1655">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1655">If you pass in a value that has a different data type than the object, the object’s data type will be changed to match the value’s data type.</span></span> <span data-ttu-id="20ffe-1656">データ型が COMVariantType::VT\_I8 に設定されている場合、その COMVariant オブジェクトは unsigned longlong バリアント型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1656">A COMVariant object has an unsigned longlong variant type if its data type is set to COMVariantType::VT\_I8.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1657">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1657">Examples</span></span>

<span data-ttu-id="20ffe-1658">次の例では、VT\_I8 型の新しい COMVariant オブジェクトを作成し、値を 9,223,372,036,854,775,808 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1658">The following example creates a new COMVariant object of type VT\_I8 and sets the value to 9,223,372,036,854,775,808.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_BOOL); 

        // Set value of the object 
        var.longLong(9223372036854775808); 
    }

### <a name="method-ushort"></a><span data-ttu-id="20ffe-1659">メソッド uShort</span><span class="sxs-lookup"><span data-stu-id="20ffe-1659">Method uShort</span></span>

<span data-ttu-id="20ffe-1660">VT\_UI2 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1660">Gets or sets the value of a COMVariant object of the VT\_UI2 data type.</span></span>

    public int uShort([int newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1661">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1661">Parameters</span></span>

<span data-ttu-id="20ffe-1662">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1662">newValue</span></span>  
<span data-ttu-id="20ffe-1663">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1663">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1664">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1664">Return Value</span></span>

<span data-ttu-id="20ffe-1665">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1665">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1666">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1666">Remarks</span></span>

<span data-ttu-id="20ffe-1667">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1667">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1668">データ型が COMVariantType::VT\_UI2 に設定されている場合、その COMVariant オブジェクトは unsigned short データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1668">A COMVariant object has an unsigned short data type if its data type is set to COMVariantType::VT\_UI2.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1669">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1669">Examples</span></span>

<span data-ttu-id="20ffe-1670">次の例では、VT\_UI2 型の新しい COMVariant オブジェクトを作成し、値を 12345 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1670">The following example creates a new COMVariant object of type VT\_UI2 and sets the value to 12345.</span></span>

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_UI2); 

        // Set value of the object 
        var.uShort(12345); 
    }

### <a name="method-variant"></a><span data-ttu-id="20ffe-1671">メソッド variant</span><span class="sxs-lookup"><span data-stu-id="20ffe-1671">Method variant</span></span>

<span data-ttu-id="20ffe-1672">VT\_VARIANT (バリアント) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1672">Gets or sets the value of a COMVariant object of the VT\_VARIANT (variant) data type.</span></span>

    public COMVariant variant([COMVariant newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1673">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1673">Parameters</span></span>

<span data-ttu-id="20ffe-1674">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1674">newValue</span></span>  
<span data-ttu-id="20ffe-1675">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1675">The new value; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1676">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1676">Return Value</span></span>

<span data-ttu-id="20ffe-1677">現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1677">The current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1678">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1678">Remarks</span></span>

<span data-ttu-id="20ffe-1679">variant プロパティは、ある COMVariant オブジェクトを別の COMVariant オブジェクトにネストするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1679">The variant property is used to nest one COMVariant object in another COMVariant object.</span></span> <span data-ttu-id="20ffe-1680">親オブジェクトを COMDispFunction.call への呼び出しまたは COM クラスへの呼び出しの引数として使用する場合、呼び出されたメソッドは自動的に入れ子になったオブジェクトのデータを抽出します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1680">When using the parent object as the argument in a call to COMDispFunction.call or in a call to the COM class, the called method will automatically extract the data of the nested object.</span></span> <span data-ttu-id="20ffe-1681">このネスト機能は、COM オブジェクトのメソッドが複数のデータ型で動作できる場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1681">This nesting facility is useful when a method on a COM object can work with multiple data types.</span></span> <span data-ttu-id="20ffe-1682">バリアントの入れ子は 1 つのレベルのみ許可されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1682">Only one level of variant nesting is allowed.</span></span> <span data-ttu-id="20ffe-1683">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1683">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="20ffe-1684">データ型が COMVariantType::VT\_VARIANT に設定されている場合、その COMVariant オブジェクトはバリアント型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1684">A COMVariant object has a variant type if its data type is set to COMVariantType::VT\_VARIANT.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1685">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1685">Examples</span></span>

<span data-ttu-id="20ffe-1686">次の例では、VT\_I4 (long) 型の COMVariant オブジェクトと VT\_VARIANT 型の COMVariant オブジェクトを作成します.</span><span class="sxs-lookup"><span data-stu-id="20ffe-1686">The following example creates a COMVariant object of type VT\_I4 (long), and a COMVariant object of type VT\_VARIANT.</span></span> <span data-ttu-id="20ffe-1687">VT\_VARIANT タイプのオブジェクトには、VT\_I4 タイプのオブジェクトの値が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1687">The object of type VT\_VARIANT is assigned the value of the object of type VT\_I4.</span></span> <span data-ttu-id="20ffe-1688">以下のコードには仮想 COM オブジェクト (「MyCOM.Object」) が含まれており、Finance and Operations の外部でオブジェクトが作成されていない限り、Finance and Operations では実行されません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1688">The code below contains a hypothetical COM object ("MyCOM.Object"), and will therefore not run in Finance and Operations, unless such an object is created outside Finance and Operations.</span></span>

    { 
        COM com; 
        COMDispFunction funcShow; 

        COMVariant var1 = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_I4); 

        COMVariant var2 = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_VARIANT); 

        InteropPermission perm1; 
        InteropPermission perm2; 

        // Set code access permission to help protect use of COM object 
        perm1 = new InteropPermission(InteropKind::ComInterop); 
        perm1.assert(); 

        com = new COM("MyCOM.Object"); 

        // Close code access permission for COM 
        CodeAccessPermission::revertAssert(); 

        // Set value of 'var1' 
        var1.Long(123456); 
        // Set value of 'var2' to 'var1' 
        var2.Variant(var1); 

        // Set code access permission to protect use of 
        // COMDispFunction object 
        perm2 = new InteropPermission(InteropKind::ComInterop); 
        perm2.assert(); 

        funcShow = new COMDispFunction( 
            com,  
            "Show",  
            COMDispContext::METHOD); 

        // Call funcShow with a long 
        funcShow.Call(var2); 
        // Change value of 'var1' 
         var1.BStr("Hello World"); 
        // Call funcShow with a string 
        funcShow.Call(var2); 

        // Close code access permission for COMDispFunction 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-variantinoutflag"></a><span data-ttu-id="20ffe-1689">メソッド variantInOutFlag</span><span class="sxs-lookup"><span data-stu-id="20ffe-1689">Method variantInOutFlag</span></span>

<span data-ttu-id="20ffe-1690">COMVariant オブジェクトに対する InOutFlag 設定を設定する返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1690">Sets or returns the InOutFlag setting for a COMVariant object.</span></span>

    public COMVariantInOut variantInOutFlag([COMVariantInOut newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1691">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1691">Parameters</span></span>

<span data-ttu-id="20ffe-1692">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1692">newValue</span></span>  
<span data-ttu-id="20ffe-1693">新しい InOutFlag 設定 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1693">The new InOutFlag setting; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1694">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1694">Return Value</span></span>

<span data-ttu-id="20ffe-1695">現在の InOutFlag 設定。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1695">The current InOutFlag setting.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1696">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1696">Remarks</span></span>

<span data-ttu-id="20ffe-1697">次に、newValue パラメーターで使用可能な値のリストを示します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1697">The following is a list of possible values for the newValue parameter.</span></span>

-   <span data-ttu-id="20ffe-1698">COMVariantInOut::IN</span><span class="sxs-lookup"><span data-stu-id="20ffe-1698">COMVariantInOut::IN</span></span>
-   <span data-ttu-id="20ffe-1699">COMVariantInOut::IN\_OUT</span><span class="sxs-lookup"><span data-stu-id="20ffe-1699">COMVariantInOut::IN\_OUT</span></span>
-   <span data-ttu-id="20ffe-1700">COMVariantInOut::OUT</span><span class="sxs-lookup"><span data-stu-id="20ffe-1700">COMVariantInOut::OUT</span></span>
-   <span data-ttu-id="20ffe-1701">COMVariantInOut::OUT\_RETVAL.</span><span class="sxs-lookup"><span data-stu-id="20ffe-1701">COMVariantInOut::OUT\_RETVAL.</span></span>

<span data-ttu-id="20ffe-1702">InOutFlag 設定は、オブジェクトが COMDispFunction.call メソッドで引数として使用されたときに、オブジェクトに格納されているデータがどのように扱われるかを記述します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1702">The InOutFlag setting describes how the data that is stored in the object is treated when the object is used as an argument in the COMDispFunction.call method.</span></span> <span data-ttu-id="20ffe-1703">InOutFlag 設定の使用可能な値は、Win32 SDK に記述されている COM オートメーション オブジェクトの値に対応します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1703">The possible values of the InOutFlag setting correspond to the values for COM Automation objects described in the Win32 SDK.</span></span> <span data-ttu-id="20ffe-1704">COMVariant オブジェクトに格納されたデータは、InOutFlag 設定が変更されても影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1704">The data stored in the COMVariant object is unaffected when the InOutFlag setting is changed.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1705">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1705">Examples</span></span>

<span data-ttu-id="20ffe-1706">次の例では、InOutFlag 設定が IN に設定されている COMVariant オブジェクトを作成し、variantInOutFlag メソッドを使用して設定を OUT に変更します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1706">The following example creates a COMVariant object that has the InOutFlag setting set to IN, and then uses the variantInOutFlag method to change the setting to OUT.</span></span>

    { 
        COMVariant var = new COMVariant(COMVariantInOut::IN); 

        // Change the 'var' object to be used as an out argument 
        var.variantInOutFlag(COMVariantInOut::OUT); 
    }

### <a name="method-varianttype"></a><span data-ttu-id="20ffe-1707">メソッド variantType</span><span class="sxs-lookup"><span data-stu-id="20ffe-1707">Method variantType</span></span>

<span data-ttu-id="20ffe-1708">COMVariant オブジェクトにそのバリアント データ型を照会するか、データ型を変更します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1708">Queries a COMVariant object for its variant data type or changes the data type.</span></span>

    public COMVariantType variantType([COMVariantType newValue])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1709">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1709">Parameters</span></span>

<span data-ttu-id="20ffe-1710">newValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1710">newValue</span></span>  
<span data-ttu-id="20ffe-1711">新しいバリアント データ型 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1711">The new variant data type; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1712">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1712">Return Value</span></span>

<span data-ttu-id="20ffe-1713">現在のバリアント データ型。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1713">The current variant data type.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1714">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1714">Remarks</span></span>

<span data-ttu-id="20ffe-1715">newValue パラメーターの使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1715">The possible values for the newValue parameter are:</span></span>

-   <span data-ttu-id="20ffe-1716">COMVariantType::VT\_I2</span><span class="sxs-lookup"><span data-stu-id="20ffe-1716">COMVariantType::VT\_I2</span></span>
-   <span data-ttu-id="20ffe-1717">COMVariantType::VT\_I4</span><span class="sxs-lookup"><span data-stu-id="20ffe-1717">COMVariantType::VT\_I4</span></span>
-   <span data-ttu-id="20ffe-1718">COMVariantType::VT\_R4</span><span class="sxs-lookup"><span data-stu-id="20ffe-1718">COMVariantType::VT\_R4</span></span>
-   <span data-ttu-id="20ffe-1719">COMVariantType::VT\_R8</span><span class="sxs-lookup"><span data-stu-id="20ffe-1719">COMVariantType::VT\_R8</span></span>
-   <span data-ttu-id="20ffe-1720">COMVariantType::VT\_CY</span><span class="sxs-lookup"><span data-stu-id="20ffe-1720">COMVariantType::VT\_CY</span></span>
-   <span data-ttu-id="20ffe-1721">COMVariantType::VT\_DATE</span><span class="sxs-lookup"><span data-stu-id="20ffe-1721">COMVariantType::VT\_DATE</span></span>
-   <span data-ttu-id="20ffe-1722">COMVariantType::VT\_BSTR</span><span class="sxs-lookup"><span data-stu-id="20ffe-1722">COMVariantType::VT\_BSTR</span></span>
-   <span data-ttu-id="20ffe-1723">COMVariantType::VT\_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="20ffe-1723">COMVariantType::VT\_DISPATCH</span></span>
-   <span data-ttu-id="20ffe-1724">COMVariantType::VT\_ERROR</span><span class="sxs-lookup"><span data-stu-id="20ffe-1724">COMVariantType::VT\_ERROR</span></span>
-   <span data-ttu-id="20ffe-1725">COMVariantType::VT\_BOOL</span><span class="sxs-lookup"><span data-stu-id="20ffe-1725">COMVariantType::VT\_BOOL</span></span>
-   <span data-ttu-id="20ffe-1726">COMVariantType::VT\_VARIANT</span><span class="sxs-lookup"><span data-stu-id="20ffe-1726">COMVariantType::VT\_VARIANT</span></span>
-   <span data-ttu-id="20ffe-1727">COMVariantType::VT\_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="20ffe-1727">COMVariantType::VT\_UNKNOWN</span></span>
-   <span data-ttu-id="20ffe-1728">COMVariantType::VT\_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="20ffe-1728">COMVariantType::VT\_DECIMAL</span></span>
-   <span data-ttu-id="20ffe-1729">COMVariantType::VT\_I1</span><span class="sxs-lookup"><span data-stu-id="20ffe-1729">COMVariantType::VT\_I1</span></span>
-   <span data-ttu-id="20ffe-1730">COMVariantType::VT\_UI1</span><span class="sxs-lookup"><span data-stu-id="20ffe-1730">COMVariantType::VT\_UI1</span></span>
-   <span data-ttu-id="20ffe-1731">COMVariantType::VT\_UI2</span><span class="sxs-lookup"><span data-stu-id="20ffe-1731">COMVariantType::VT\_UI2</span></span>
-   <span data-ttu-id="20ffe-1732">COMVariantType::VT\_UI4</span><span class="sxs-lookup"><span data-stu-id="20ffe-1732">COMVariantType::VT\_UI4</span></span>

<span data-ttu-id="20ffe-1733">バリアント データ型は、オブジェクトが COMDispFunction.call メソッドの呼び出しまたは COM クラスの呼び出しで引数として使用されたときに、オブジェクトに格納されているデータがどのように扱われるかを記述します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1733">The variant data type describes how the data that is stored in the object is treated when the object is used as an argument in a call to the COMDispFunction.call method or a call to the COM class.</span></span> <span data-ttu-id="20ffe-1734">データ型を変更すると、オブジェクトに保持されているデータは削除されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1734">If you change the data type, the data that is held in the object is deleted.</span></span> <span data-ttu-id="20ffe-1735">使用可能なバリアント データ型については、\[COMVariant.new\] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1735">See the \[COMVariant.new\] for information about the available variant data types.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1736">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1736">Examples</span></span>

<span data-ttu-id="20ffe-1737">次の例では、新しい COMVariant オブジェクトを作成し、それを long (VT\_I4) データ型に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1737">The following example creates a new COMVariant object and sets it to be of long (VT\_I4) data type.</span></span> <span data-ttu-id="20ffe-1738">その後、variantType メソッドを使用して、データ型を VT\_DATE (日付) に変更します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1738">The variantType method is then used to change the data type to VT\_DATE (date).</span></span> <span data-ttu-id="20ffe-1739">オブジェクトが保持するデータは破棄されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1739">The data that is held by the object is discarded.</span></span>

    { 
        COMVariant var = new COMVariant(); 

        // Set the 'var' object to be a long 
        var.long(123); 

        // Change var so that it can store a date 
        var.variantType(COMVariantType::VT_DATE); 
    }

### <a name="method-createdatefromymd"></a><span data-ttu-id="20ffe-1740">メソッド createDateFromYMD</span><span class="sxs-lookup"><span data-stu-id="20ffe-1740">Method createDateFromYMD</span></span>

<span data-ttu-id="20ffe-1741">新しい COMVariant オブジェクトを作成し、1 回の操作で日付値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1741">Creates a new COMVariant object and initializes it with a date value in one operation.</span></span>

    public static COMVariant createDateFromYMD(int year, int month, int day, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1742">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1742">Parameters</span></span>

<span data-ttu-id="20ffe-1743">年</span><span class="sxs-lookup"><span data-stu-id="20ffe-1743">year</span></span>  
<span data-ttu-id="20ffe-1744">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1744">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1745">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1745">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1746">有効値: COMVariantInOut::OUT\_RETVAL</span><span class="sxs-lookup"><span data-stu-id="20ffe-1746">Possible values are: COMVariantInOut::OUT\_RETVAL</span></span>

<!-- -->

<span data-ttu-id="20ffe-1747">月</span><span class="sxs-lookup"><span data-stu-id="20ffe-1747">month</span></span>  
<span data-ttu-id="20ffe-1748">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1748">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1749">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1749">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1750">有効値: COMVariantInOut::OUT\_RETVAL</span><span class="sxs-lookup"><span data-stu-id="20ffe-1750">Possible values are: COMVariantInOut::OUT\_RETVAL</span></span>

<!-- -->

<span data-ttu-id="20ffe-1751">日</span><span class="sxs-lookup"><span data-stu-id="20ffe-1751">day</span></span>  
<span data-ttu-id="20ffe-1752">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1752">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1753">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1753">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1754">有効値: COMVariantInOut::OUT\_RETVAL</span><span class="sxs-lookup"><span data-stu-id="20ffe-1754">Possible values are: COMVariantInOut::OUT\_RETVAL</span></span>

<!-- -->

<span data-ttu-id="20ffe-1755">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="20ffe-1755">inOutFlag</span></span>  
<span data-ttu-id="20ffe-1756">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1756">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1757">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1757">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1758">有効値: COMVariantInOut::OUT\_RETVAL</span><span class="sxs-lookup"><span data-stu-id="20ffe-1758">Possible values are: COMVariantInOut::OUT\_RETVAL</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1759">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1759">Return Value</span></span>

<span data-ttu-id="20ffe-1760">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1760">The new COMVariant object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1761">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1761">Remarks</span></span>

<span data-ttu-id="20ffe-1762">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_DATE (日時) を持っています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1762">The COMVariant object that is created by this method has the data type VT\_DATE (date/time).</span></span> <span data-ttu-id="20ffe-1763">このメソッドを使用すると、Finance and Operationsdate データ型 (0111901〜31122154) の範囲外の日付を使用できます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1763">This method allows you to use dates that are outside the range for the Finance and Operationsdate data type (0111901 to 31122154).</span></span> <span data-ttu-id="20ffe-1764">日付範囲内の日付で、COMVariant.createFromDate メソッドを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1764">For dates within the date range, you can use the COMVariant.createFromDate method.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1765">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1765">Examples</span></span>

<span data-ttu-id="20ffe-1766">次の例では、COMVariant オブジェクトを作成し、4015 年 1 月 1 日の日付で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1766">The following example creates a COMVariant object and initializes it with the date 01 January 4015.</span></span>

    COMVariant myDate; 

    myDate = COMVariant::createDateFromYMD(4015,1,1);

### <a name="method-createfromarray"></a><span data-ttu-id="20ffe-1767">メソッド createFromArray</span><span class="sxs-lookup"><span data-stu-id="20ffe-1767">Method createFromArray</span></span>

<span data-ttu-id="20ffe-1768">新しい COMVariant オブジェクトを作成し、1 回の操作で配列で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1768">Creates a new COMVariant object and initializes it with an array in one operation.</span></span>

    public static COMVariant createFromArray(Array value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1769">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1769">Parameters</span></span>

<span data-ttu-id="20ffe-1770">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1770">value</span></span>  
<span data-ttu-id="20ffe-1771">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1771">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1772">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1772">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1773">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1773">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="20ffe-1774">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="20ffe-1774">inOutFlag</span></span>  
<span data-ttu-id="20ffe-1775">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1775">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1776">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1776">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1777">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1777">Possible values are:</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1778">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1778">Return Value</span></span>

<span data-ttu-id="20ffe-1779">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1779">The new COMVariant object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1780">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1780">Remarks</span></span>

<span data-ttu-id="20ffe-1781">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_SAFEARRAY (配列) を持っています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1781">The COMVariant object that is created by this method has the data type VT\_SAFEARRAY (array).</span></span> <span data-ttu-id="20ffe-1782">variantType メソッドの使用により、または safeArray プロパティ メソッドを使用して配列値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_SAFEARRAY に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1782">You can change the data type of an existing COMVariant object to VT\_SAFEARRAY by using the variantType method or by passing in an array value by using the safeArray property method.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1783">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1783">Examples</span></span>

<span data-ttu-id="20ffe-1784">次の例では、新しい COMVariant オブジェクトを作成し、整数の配列で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1784">The following example creates a new COMVariant object and initializes it with an array of integers.</span></span>

    { 
        int i; 
        COMVariant var; 
        Array arr = new Array(Types::INTEGER); 

        for (i = 1; i <= 10; i++) 
            // Insert 10 values in the array 
            arr.value(i, i); 

        // Create and initialize a COMVariant object  
        var = COMVariant::createFromArray(arr); 
    }

### <a name="method-createfromboolean"></a><span data-ttu-id="20ffe-1785">メソッド createFromBoolean</span><span class="sxs-lookup"><span data-stu-id="20ffe-1785">Method createFromBoolean</span></span>

<span data-ttu-id="20ffe-1786">新しい COMVariant オブジェクトを作成し、1 回の操作でブール値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1786">Creates a new COMVariant object and initializes it with a Boolean value in one operation.</span></span>

    public static COMVariant createFromBoolean(boolean value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1787">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1787">Parameters</span></span>

<span data-ttu-id="20ffe-1788">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1788">value</span></span>  
<span data-ttu-id="20ffe-1789">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1789">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1790">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1790">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1791">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1791">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="20ffe-1792">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="20ffe-1792">inOutFlag</span></span>  
<span data-ttu-id="20ffe-1793">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1793">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1794">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1794">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1795">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1795">Possible values are:</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1796">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1796">Return Value</span></span>

<span data-ttu-id="20ffe-1797">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1797">The new COMVariant object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1798">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1798">Remarks</span></span>

<span data-ttu-id="20ffe-1799">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_BOOL (ブール値) を持っています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1799">The COMVariant object that is created by this method has the data type VT\_BOOL (Boolean).</span></span> <span data-ttu-id="20ffe-1800">variantType メソッドの使用により、または boolean プロパティ メソッドを使用してブール値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_BOOL に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1800">You can change the data type of an existing COMVariant object to VT\_BOOL by using the variantType method or by passing in a Boolean value by using the boolean property method.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1801">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1801">Examples</span></span>

<span data-ttu-id="20ffe-1802">次の例では、VT\_BOOL バリアント データ型 (ブール値) の COMVariant オブジェクトを作成し、その値を true に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1802">The following example creates a COMVariant object of the VT\_BOOL variant data type (Boolean), and sets the value to true.</span></span>

    { 
        COMVariant var; 

        var = COMVariant::createFromBoolean(TRUE); 
    }

### <a name="method-createfromcom"></a><span data-ttu-id="20ffe-1803">メソッド createFromCOM</span><span class="sxs-lookup"><span data-stu-id="20ffe-1803">Method createFromCOM</span></span>

<span data-ttu-id="20ffe-1804">新しい COMVariant オブジェクトを作成し、1 回の操作で COM クラスで初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1804">Creates a new COMVariant object and initializes it with a COM class in one operation.</span></span>

    public static COMVariant createFromCOM(COM value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1805">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1805">Parameters</span></span>

<span data-ttu-id="20ffe-1806">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1806">value</span></span>  
<span data-ttu-id="20ffe-1807">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1807">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1808">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1808">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1809">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1809">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="20ffe-1810">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="20ffe-1810">inOutFlag</span></span>  
<span data-ttu-id="20ffe-1811">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1811">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1812">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1812">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1813">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1813">Possible values are:</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1814">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1814">Return Value</span></span>

<span data-ttu-id="20ffe-1815">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1815">The new COMVariant object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1816">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1816">Remarks</span></span>

<span data-ttu-id="20ffe-1817">inOutFlag パラメーターの使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1817">Possible values of the inOutFlag parameter are as follows:</span></span>

-   <span data-ttu-id="20ffe-1818">COMVariantInOut::IN</span><span class="sxs-lookup"><span data-stu-id="20ffe-1818">COMVariantInOut::IN</span></span>
-   <span data-ttu-id="20ffe-1819">COMVariantInOut::IN\_OUT</span><span class="sxs-lookup"><span data-stu-id="20ffe-1819">COMVariantInOut::IN\_OUT</span></span>
-   <span data-ttu-id="20ffe-1820">COMVariantInOut::OUT</span><span class="sxs-lookup"><span data-stu-id="20ffe-1820">COMVariantInOut::OUT</span></span>
-   <span data-ttu-id="20ffe-1821">COMVariantInOut::OUT\_RETVAL</span><span class="sxs-lookup"><span data-stu-id="20ffe-1821">COMVariantInOut::OUT\_RETVAL</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1822">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1822">Examples</span></span>

<span data-ttu-id="20ffe-1823">次の例では、新しい COMVariant オブジェクトを作成し、COM オブジェクトで初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1823">The following example creates a new COMVariant object and initializes it with a COM object.</span></span>

    { 
        COMVariant var; 
        COM com = new COM("MyCOM.Object"); 

        var = COMVariant::createFromCOM(com); 
    }

### <a name="method-createfromdate"></a><span data-ttu-id="20ffe-1824">メソッド createFromDate</span><span class="sxs-lookup"><span data-stu-id="20ffe-1824">Method createFromDate</span></span>

<span data-ttu-id="20ffe-1825">新しい COMVariant オブジェクトを作成し、1 回の操作で日付値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1825">Creates a new COMVariant object and initializes it with a date value in one operation.</span></span>

    public static COMVariant createFromDate(Date value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1826">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1826">Parameters</span></span>

<span data-ttu-id="20ffe-1827">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1827">value</span></span>  
<span data-ttu-id="20ffe-1828">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1828">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1829">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1829">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1830">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1830">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="20ffe-1831">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="20ffe-1831">inOutFlag</span></span>  
<span data-ttu-id="20ffe-1832">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1832">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1833">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1833">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1834">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1834">Possible values are:</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1835">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1835">Return Value</span></span>

<span data-ttu-id="20ffe-1836">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1836">The new COMVariant object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1837">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1837">Remarks</span></span>

<span data-ttu-id="20ffe-1838">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_DATE (日時) を持っています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1838">The COMVariant object that is created by this method has the data type VT\_DATE (date/time).</span></span> <span data-ttu-id="20ffe-1839">variantType メソッドの使用により、または date プロパティ メソッドを使用して時刻値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_DATE に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1839">You can change the data type of an existing COMVariant object to VT\_DATE by using the variantType method or by passing in a time value by using the date property method.</span></span> <span data-ttu-id="20ffe-1840">Axapta の日付タイプ (0111901〜31122154) の範囲外の日付を使用する場合は、COMVariant.createDateFromYMD メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1840">If you want to use a date that is outside the range for the Axapta date type (0111901 to 31122154), use the COMVariant.createDateFromYMD method.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1841">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1841">Examples</span></span>

<span data-ttu-id="20ffe-1842">次の例では、COMVariant オブジェクトを作成し、現在の日付で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1842">The following example creates a COMVariant object and initializes it with the current date.</span></span>

    COMVariant theDay; 

    theDay = COMVariant::createFromDate(today()); 
    info(theDay.toString());

### <a name="method-createfromdateandtime"></a><span data-ttu-id="20ffe-1843">メソッド createFromDateAndTime</span><span class="sxs-lookup"><span data-stu-id="20ffe-1843">Method createFromDateAndTime</span></span>

<span data-ttu-id="20ffe-1844">新しい COMVariant オブジェクトを作成し、1 回の操作で日時で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1844">Creates a new COMVariant object and initializes it with a date and time in one operation.</span></span>

    public static COMVariant createFromDateAndTime(Date date, int time, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1845">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1845">Parameters</span></span>

<span data-ttu-id="20ffe-1846">日付</span><span class="sxs-lookup"><span data-stu-id="20ffe-1846">date</span></span>  
<span data-ttu-id="20ffe-1847">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1847">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1848">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1848">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1849">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1849">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="20ffe-1850">タイム</span><span class="sxs-lookup"><span data-stu-id="20ffe-1850">time</span></span>  
<span data-ttu-id="20ffe-1851">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1851">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1852">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1852">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1853">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1853">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="20ffe-1854">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="20ffe-1854">inOutFlag</span></span>  
<span data-ttu-id="20ffe-1855">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1855">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1856">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1856">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1857">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1857">Possible values are:</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1858">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1858">Return Value</span></span>

<span data-ttu-id="20ffe-1859">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1859">The new COMVariant object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1860">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1860">Remarks</span></span>

<span data-ttu-id="20ffe-1861">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_DATE (日時) を持っています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1861">The COMVariant object that is created by this method has the data type VT\_DATE (date/time).</span></span> <span data-ttu-id="20ffe-1862">variantType メソッドを使用することにより、既存の COMVariant オブジェクトを VT\_DATE に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1862">You can change the data type of an existing COMVariant object to VT\_DATE by using the variantType method.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1863">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1863">Examples</span></span>

<span data-ttu-id="20ffe-1864">次の例では、COMVariant オブジェクトを作成し、現在の日付と深夜 0 時から 10 秒の間隔の時刻を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1864">The following example creates a COMVariant object and assigns it the current date, and a time of 10 seconds past midnight.</span></span>

    date theDay; 
    COMVariant theDayAndTime; 

    theDay = today(); 
    theDayAndTime = COMVariant::createFromDateAndTime(theDay, 10); 
    info(theDayAndTime.toString());

### <a name="method-createfromint"></a><span data-ttu-id="20ffe-1865">メソッド createFromInt</span><span class="sxs-lookup"><span data-stu-id="20ffe-1865">Method createFromInt</span></span>

<span data-ttu-id="20ffe-1866">新しい COMVariant オブジェクトを作成し、1 回の操作で整数値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1866">Creates a new COMVariant object and initializes it with an integer value in one operation.</span></span>

    public static COMVariant createFromInt(int value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1867">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1867">Parameters</span></span>

<span data-ttu-id="20ffe-1868">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1868">value</span></span>  
<span data-ttu-id="20ffe-1869">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1869">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1870">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1870">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1871">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1871">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="20ffe-1872">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="20ffe-1872">inOutFlag</span></span>  
<span data-ttu-id="20ffe-1873">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1873">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1874">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1874">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1875">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1875">Possible values are:</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1876">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1876">Return Value</span></span>

<span data-ttu-id="20ffe-1877">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1877">The new COMVariant object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1878">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1878">Remarks</span></span>

<span data-ttu-id="20ffe-1879">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_I4 (整数) を持っています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1879">The COMVariant object that is created by this method has the data type VT\_I4 (integer).</span></span> <span data-ttu-id="20ffe-1880">variantType メソッドの使用により、または int プロパティ メソッドを使用して整数値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_I4 に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1880">You can change the data type of an existing COMVariant object to VT\_I4 by using the variantType method or by passing in an integer value by using the int property method.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1881">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1881">Examples</span></span>

<span data-ttu-id="20ffe-1882">次の例では、VT\_I4 バリアント データ型 (整数) の COMVariant オブジェクトを作成し、値を 123 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1882">The following example creates a COMVariant object of the VT\_I4 variant data type (integer), and sets the value to 123.</span></span>

    { 
        COMVariant var; 

        var = COMVariant::createFromInt(123); 
    }

### <a name="method-createfromint64"></a><span data-ttu-id="20ffe-1883">メソッド createFromInt64</span><span class="sxs-lookup"><span data-stu-id="20ffe-1883">Method createFromInt64</span></span>

<span data-ttu-id="20ffe-1884">新しい COMVariant オブジェクトを作成し、1 回の操作でint64 値 (longLong や uLongLong) で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1884">Creates a new COMVariant object and initializes it with an int64 value (longLong or uLongLong) in one operation.</span></span>

    public static COMVariant createFromInt64(Int64 value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1885">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1885">Parameters</span></span>

<span data-ttu-id="20ffe-1886">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1886">value</span></span>  
<span data-ttu-id="20ffe-1887">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1887">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1888">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1888">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1889">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1889">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="20ffe-1890">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="20ffe-1890">inOutFlag</span></span>  
<span data-ttu-id="20ffe-1891">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1891">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1892">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1892">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1893">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1893">Possible values are:</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1894">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1894">Return Value</span></span>

<span data-ttu-id="20ffe-1895">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1895">The new COMVariant object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1896">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1896">Remarks</span></span>

<span data-ttu-id="20ffe-1897">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_I8 (int64) を持っています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1897">The COMVariant object that is created by this method has the data type VT\_I8 (int64).</span></span> <span data-ttu-id="20ffe-1898">variantType メソッドの使用により、または longLong や uLongLong プロパティ メソッドを使用して int64 値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_I8 に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1898">You can change the data type of an existing COMVariant object to VT\_I8 by using the variantType method or by passing in an int64 value by using the longLong or uLongLong property method.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1899">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1899">Examples</span></span>

<span data-ttu-id="20ffe-1900">次の例では、VT\_I8 バリアント データ型 (整数) の COMVariant オブジェクトを作成し、値を 123456 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1900">The following example creates a COMVariant object of the VT\_I8 variant data type (integer), and sets the value to 123456.</span></span>

    { 
        COMVariant var; 

        var = COMVariant::createFromInt64(123456); 
    }

### <a name="method-createfromreal"></a><span data-ttu-id="20ffe-1901">メソッド createFromReal</span><span class="sxs-lookup"><span data-stu-id="20ffe-1901">Method createFromReal</span></span>

<span data-ttu-id="20ffe-1902">新しい COMVariant オブジェクトを作成し、1 回の操作で実際の値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1902">Creates a new COMVariant object and initializes it with a real value in one operation.</span></span>

    public static COMVariant createFromReal(Real value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1903">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1903">Parameters</span></span>

<span data-ttu-id="20ffe-1904">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1904">value</span></span>  
<span data-ttu-id="20ffe-1905">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1905">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1906">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1906">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1907">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1907">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="20ffe-1908">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="20ffe-1908">inOutFlag</span></span>  
<span data-ttu-id="20ffe-1909">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1909">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1910">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1910">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1911">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1911">Possible values are:</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1912">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1912">Return Value</span></span>

<span data-ttu-id="20ffe-1913">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1913">The new COMVariant object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1914">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1914">Remarks</span></span>

<span data-ttu-id="20ffe-1915">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_R8 (実数) を持っています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1915">The COMVariant object that is created by this method has the data type VT\_R8 (real).</span></span> <span data-ttu-id="20ffe-1916">variantType メソッドの使用により、または double プロパティ メソッドを使用してブール値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_R8 に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1916">You can change the data type of an existing COMVariant object to VT\_R8 by using the variantType method or by passing in a Boolean value by using the double property method.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1917">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1917">Examples</span></span>

<span data-ttu-id="20ffe-1918">次の例では、VT\_R8 バリアント データ型 (実数) の COMVariant オブジェクトを作成し、値を 123.456 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1918">The following example creates a COMVariant object of the VT\_R8 variant data type (real) and sets the value to 123.456.</span></span>

    { 
        COMVariant var; 

        var = COMVariant::createFromReal(123.456); 
    }

### <a name="method-createfromstr"></a><span data-ttu-id="20ffe-1919">メソッド createFromStr</span><span class="sxs-lookup"><span data-stu-id="20ffe-1919">Method createFromStr</span></span>

<span data-ttu-id="20ffe-1920">新しい COMVariant オブジェクトを作成し、1 回の操作で文字列で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1920">Creates a new COMVariant object and initializes it with a string in one operation.</span></span>

    public static COMVariant createFromStr(str value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1921">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1921">Parameters</span></span>

<span data-ttu-id="20ffe-1922">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1922">value</span></span>  
<span data-ttu-id="20ffe-1923">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1923">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1924">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1924">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1925">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1925">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="20ffe-1926">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="20ffe-1926">inOutFlag</span></span>  
<span data-ttu-id="20ffe-1927">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1927">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1928">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1928">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1929">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1929">Possible values are:</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1930">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1930">Return Value</span></span>

<span data-ttu-id="20ffe-1931">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1931">The new COMVariant object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1932">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1932">Remarks</span></span>

<span data-ttu-id="20ffe-1933">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_BSTR (文字列) を持っています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1933">The COMVariant object that is created by this method has the data type VT\_BSTR (string).</span></span> <span data-ttu-id="20ffe-1934">variantType メソッドの使用により、または bStr プロパティ メソッドを使用して文字列値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_BSTR に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1934">You can change the data type of an existing COMVariant object to VT\_BSTR by using the variantType method or by passing in a string value by using the bStr property method.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1935">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1935">Examples</span></span>

<span data-ttu-id="20ffe-1936">次の例では、VT\_BSTR バリアント データ型の COMVariant オブジェクトを作成し、値を "Hello World" に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1936">The following example creates a COMVariant object of the VT\_BSTR variant data type and sets the value to "Hello World."</span></span>

    { 
        COMVariant var; 

        var = COMVariant::createFromStr("Hello World"); 
    }

### <a name="method-createfromtime"></a><span data-ttu-id="20ffe-1937">メソッド createFromTime</span><span class="sxs-lookup"><span data-stu-id="20ffe-1937">Method createFromTime</span></span>

<span data-ttu-id="20ffe-1938">新しい COMVariant オブジェクトを作成し、1 回の操作で時刻値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1938">Creates a new COMVariant object and initializes it with a time value in one operation.</span></span>

    public static COMVariant createFromTime(int value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1939">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1939">Parameters</span></span>

<span data-ttu-id="20ffe-1940">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1940">value</span></span>  
<span data-ttu-id="20ffe-1941">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1941">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1942">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1942">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1943">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1943">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="20ffe-1944">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="20ffe-1944">inOutFlag</span></span>  
<span data-ttu-id="20ffe-1945">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1945">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="20ffe-1946">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1946">This parameter is optional.</span></span> <span data-ttu-id="20ffe-1947">有効値:</span><span class="sxs-lookup"><span data-stu-id="20ffe-1947">Possible values are:</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-1948">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1948">Return Value</span></span>

<span data-ttu-id="20ffe-1949">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1949">The new COMVariant object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1950">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1950">Remarks</span></span>

<span data-ttu-id="20ffe-1951">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_DATE (日時) を持っています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1951">The COMVariant object that is created by this method has the data type VT\_DATE (date/time).</span></span> <span data-ttu-id="20ffe-1952">variantType メソッドの使用により、または time プロパティ メソッドを使用して時刻値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_DATE に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1952">You can change the data type of an existing COMVariant object to VT\_DATE by using the variantType method or by passing in a time value by using the time property method.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1953">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1953">Examples</span></span>

<span data-ttu-id="20ffe-1954">次の例では、COMVariant オブジェクトを作成し、時刻の部分を深夜 0 時から 10 秒の間隔に設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1954">The following example will create a COMVariant object and set the time part to 10 seconds past midnight.</span></span>

    COMVariant theTime; 

    theTime = COMVariant::createFromTime(10); 
    info(theTime.toString());

### <a name="method-createfromutcdatetime"></a><span data-ttu-id="20ffe-1955">メソッド createFromUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="20ffe-1955">Method createFromUtcDateTime</span></span>

    public static COMVariant createFromUtcDateTime(DateTime value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1956">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1956">Parameters</span></span>

<span data-ttu-id="20ffe-1957">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1957">value</span></span>  

<!-- -->

<span data-ttu-id="20ffe-1958">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="20ffe-1958">inOutFlag</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-1959">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1959">Return Value</span></span>

### <a name="method-createnovalue"></a><span data-ttu-id="20ffe-1960">メソッド createNoValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1960">Method createNoValue</span></span>

<span data-ttu-id="20ffe-1961">値を持たない VT\_エラー バリアント タイプの COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1961">Creates a COMVariant object of the VT\_ERROR variant type with no value.</span></span>

    public static COMVariant createNoValue()

#### <a name="return-value"></a><span data-ttu-id="20ffe-1962">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-1962">Return Value</span></span>

<span data-ttu-id="20ffe-1963">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1963">The new COMVariant object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1964">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1964">Remarks</span></span>

<span data-ttu-id="20ffe-1965">オプションの COM パラメーターには、値を持たない COMVariant オブジェクトを使用できます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1965">A COMVariant object with no value can be used for COM parameters which are optional.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1966">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1966">Examples</span></span>

<span data-ttu-id="20ffe-1967">次の例では、空の COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1967">The following example creates an empty COMVariant object.</span></span>

    COMVariant noValue; 

    noValue = COMVariant::createNoValue(); 
    info(noValue.toString());

### <a name="method-new"></a><span data-ttu-id="20ffe-1968">メソッド new</span><span class="sxs-lookup"><span data-stu-id="20ffe-1968">Method new</span></span>

<span data-ttu-id="20ffe-1969">COM オートメーション オブジェクトのメソッドまたはプロパティに引数を渡すために使用できる COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1969">Creates a COMVariant object that can be used to pass arguments to the methods or properties of a COM Automation object.</span></span>

    public void new([COMVariantInOut inOutFlag], [COMVariantType type])

#### <a name="parameters"></a><span data-ttu-id="20ffe-1970">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-1970">Parameters</span></span>

<span data-ttu-id="20ffe-1971">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="20ffe-1971">inOutFlag</span></span>  
<span data-ttu-id="20ffe-1972">格納するデータのタイプ、オプション。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1972">A type of data to store; optional.</span></span> <span data-ttu-id="20ffe-1973">これらは、COMVariantType システム列挙型によって提供される可能性のある値です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1973">These are the possible values that are supplied by the COMVariantType system enum:</span></span>

<!-- -->

<span data-ttu-id="20ffe-1974">タイプ</span><span class="sxs-lookup"><span data-stu-id="20ffe-1974">type</span></span>  
<span data-ttu-id="20ffe-1975">格納するデータのタイプ、オプション。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1975">A type of data to store; optional.</span></span> <span data-ttu-id="20ffe-1976">これらは、COMVariantType システム列挙型によって提供される可能性のある値です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1976">These are the possible values that are supplied by the COMVariantType system enum:</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-1977">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1977">Remarks</span></span>

<span data-ttu-id="20ffe-1978">型パラメーターが省略されると、COMVariant オブジェクトのプロパティのいずれかによって必要とされるまで、内部メモリは割り当てられません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1978">If the type parameter is omitted, no internal memory will be allocated until it is needed by one of the property methods of the COMVariant object.</span></span> <span data-ttu-id="20ffe-1979">プロパティ メソッドの一覧については、\[COMVariant クラス\] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1979">For a list of the property methods, see \[COMVariant Class\].</span></span> <span data-ttu-id="20ffe-1980">異なるタイプの新しい値を指定することにより (いずれかのプロパティ メソッドを使用して)、バリアント データ型を設定後に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1980">You can change the variant data type after it has been set by passing in a new value of a different type (by using one of the property methods).</span></span> <span data-ttu-id="20ffe-1981">COMVariantType 列挙によって定義されるデータ型は、Win32 SDK によって定義されるバリアントデータ型と同じです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1981">The data types that are defined by the COMVariantType enum are equivalent to the variant data types that are defined by the Win32 SDK.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1982">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1982">Examples</span></span>

<span data-ttu-id="20ffe-1983">次の例では、3 つの COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1983">The following example creates three COMVariant objects:</span></span>

-   <span data-ttu-id="20ffe-1984">varIn は COM メソッドにデータを渡すためのものです。内部には文字列および短整数が格納されています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1984">varIn is for passing data to a COM method; it has a string stored in it and then a short (integer).</span></span>
-   <span data-ttu-id="20ffe-1985">varOut は VT\_I4 (long) タイプのデータを受け取るためのものです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1985">varOut is to receive data of type VT\_I4 (long).</span></span>
-   <span data-ttu-id="20ffe-1986">varOutRetval はデータをパスまたは受け取ることができます。そのデータ タイプは COMDispFunction.call メソッドでセットすることができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1986">varOutRetval can pass in or receive data; its data type can be set by the COMDispFunction.call method.</span></span>

<!-- -->

    { 
        COMVariant varIn  = new COMVariant(); 
        COMVariant varOut = new COMVariant( 
            COMVariantInOut::OUT,  
            COMVariantType::VT_I4); 
        COMVariant varOutRetval = new COMVariant( 
            COMVariantInOut::OUT_RETVAL); ; 

        // Store a text string in the varIn object 
        varIn.bStr("Hello World"); 

        // Change varIn to a short. 
        // Text string stored in varIn is automatically released 
        varIn.short(123);  
    }

### <a name="method-novalue"></a><span data-ttu-id="20ffe-1987">メソッド noValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-1987">Method noValue</span></span>

<span data-ttu-id="20ffe-1988">既存の COMVariant オブジェクトの内容を削除し、COMDispFunction.call メソッドまたは COM クラスで使用されている場合は、未指定の引数として機能させることができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1988">Deletes the contents of an existing COMVariant object and enables it to act as an unspecified argument when it is used in the COMDispFunction.call method or the COM class.</span></span>

    public void noValue()

#### <a name="remarks"></a><span data-ttu-id="20ffe-1989">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-1989">Remarks</span></span>

<span data-ttu-id="20ffe-1990">値を持たないバリアントは、null にできるパラメーターが COM メソッドにあるときに使用できます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1990">A no-value variant can be used when a COM method has parameters that can be null.</span></span> <span data-ttu-id="20ffe-1991">引数が指定されていない COM オブジェクトと、独自の既定値を使用する必要がある COM オブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1991">It indicates to the COM object that the argument has not been specified and that it must use its own default value.</span></span> <span data-ttu-id="20ffe-1992">COM オブジェクトに対するメソッドを呼び出すときは、COMArgument::NoValue 列挙型を使用して、未指定の引数を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1992">When you are calling methods on a COM object, the unspecified argument can also be specified by using the COMArgument::NoValue enum.</span></span> <span data-ttu-id="20ffe-1993">COMDispFunction クラスを通じて呼び出すときに、この列挙型は使用できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1993">Note that this enum cannot be used when calling through the COMDispFunction class.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-1994">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-1994">Examples</span></span>

<span data-ttu-id="20ffe-1995">次の例は、3 番目の引数 unspecified を使用して COM.multiply メソッドを呼び出す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1995">The following example shows how to call the COM.multiply method with the third argument unspecified.</span></span> <span data-ttu-id="20ffe-1996">以下のコードには仮想 COM オブジェクト (「MyCOM.Object」) が含まれており、Finance and Operations の外部でオブジェクトが作成されていない限り、Finance and Operations では実行されません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1996">The code below contains a hypothetical COM object ("MyCOM.Object"), and will therefore not run in Finance and Operations, unless such an object is created outside Finance and Operations.</span></span>

    { 
        COM        com; 
        COMVariant varArg1 = new COMVariant(); 
        COMVariant varArg2 = new COMVariant(); 
        COMVariant varArg3 = new COMVariant(); 
        COMVariant varRet  = new COMVariant(COMVariantInOut::OUT_RETVAL); 
        real       ret; 
        InteropPermission perm; 

        // Set code access permission to help protect use of COM object 
        perm = new InteropPermission(InteropKind::ComInterop); 
        if (perm == null) 
        { 
            return; 
        } 

        // Permission scope starts here 
        perm.assert(); 

        com = new COM("MyCOM.Object"); 

        // Specify arguments for the multiply method 
        varArg1.float(123); 
        varArg2.float(456); 
        varArg3.noValue(); 
        varRet = com.multiply(varArg1, varArg2, varArg3); 
        // …or… 
        varRet = com.multiply(varArg1, varArg2, COMArgument::NoValue); 
         ret = varRet.double(); 
        // ret is now 56088 (123*456) 

        // Close code access permission 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-finalize"></a><span data-ttu-id="20ffe-1997">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="20ffe-1997">Method finalize</span></span>

<span data-ttu-id="20ffe-1998">実装されていません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1998">Not implemented.</span></span> <span data-ttu-id="20ffe-1999">明示的にオブジェクトを破棄する必要がある場合は、このメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-1999">You can override this method if you need to explicitly destruct an object.</span></span>

    public void finalize()

#### <a name="remarks"></a><span data-ttu-id="20ffe-2000">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2000">Remarks</span></span>

<span data-ttu-id="20ffe-2001">メソッドのすべてのステートメントを実行する確定メソッドを呼び出す必要があります。メソッドを確定する暗黙的な呼び出しはありません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2001">You must call finalize methods to execute any statements in them; there are no implicit calls to finalize methods.</span></span>

## <a name="class-configurationkeyset"></a><span data-ttu-id="20ffe-2002">クラス ConfigurationKeySet</span><span class="sxs-lookup"><span data-stu-id="20ffe-2002">Class ConfigurationKeySet</span></span>
    class ConfigurationKeySet extends Object

<span data-ttu-id="20ffe-2003">ConfigurationKeySet クラスでは、コンフィギュレーション キーのツリーを操作できます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2003">The ConfigurationKeySet class enables working with a tree of configuration keys.</span></span>

### <a name="remarks"></a><span data-ttu-id="20ffe-2004">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2004">Remarks</span></span>

<span data-ttu-id="20ffe-2005">新しい ConfigurationKeySet が作成されるとき、コンフィギュレーション キーのツリーが作成されます。この場合、すべてのキーは既定では「有効」に設定されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2005">When a new ConfigurationKeySet is created, a tree of configuration keys is created, where all keys are set by default to "enabled".</span></span> <span data-ttu-id="20ffe-2006">cnt メソッドは、すべての設定キーをループしてカウントするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2006">The cnt method is used to loop through all configuration keys and count them.</span></span> <span data-ttu-id="20ffe-2007">cntID メソッドは、設定キーの ID を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2007">The cntID method is used to retrieve the IDs of the configuration keys.</span></span> <span data-ttu-id="20ffe-2008">コンフィギュレーション キーが削除され、キー ID が ID1、ID2、ID5 などである場合、このメソッドはそれらの ID と比較してコンフィギュレーション キーの数を区別します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2008">In situations in which a configuration key has been deleted and the key IDs are ID1, ID2, ID5, and so on, this method will distinguish the number of configuration keys compared to their IDs.</span></span> <span data-ttu-id="20ffe-2009">新しい ConfigurationKeySet が作成されるとき、すべてのコンフィギュレーション キーが有効になります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2009">When a new ConfigurationKeySet is created, all configuration keys are enabled.</span></span> <span data-ttu-id="20ffe-2010">システムは loadSystemSetup メソッドを呼び出し、構成タイプが格納されている SysConfig テーブルをスキャンします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2010">The system will then call the loadSystemSetup method, which scans the SysConfig table where the configuration types are stored.</span></span> <span data-ttu-id="20ffe-2011">コンフィギュレーション キーの設定をループし、有効になっているものを識別します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2011">It loops through the configuration key setup and identifies what is enabled.</span></span> <span data-ttu-id="20ffe-2012">次に、有効なメソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2012">Next, the enabled method is called.</span></span> <span data-ttu-id="20ffe-2013">構成キーが無効になるたびに、すべてのサブ構成キーも自動的に無効になります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2013">Every time a configuration key is disabled, all sub-configuration keys are also automatically disabled.</span></span> <span data-ttu-id="20ffe-2014">トップ ノードが有効でサブノードの 1 つが無効になっている場合、カーネルはトップ ノードが無効になったときに必ずどのコンフィギュレーション キー サブ ノードが以前に無効にされたかを記録します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2014">In a situation in which a top node is enabled and one of the sub-nodes is disabled, the kernel will remember which configuration key sub-nodes were previously disabled whenever a top node is disabled.</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-2015">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-2015">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="20ffe-2016">メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-2016">Methods</span></span>

| <span data-ttu-id="20ffe-2017">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-2017">Method</span></span>                                                                            | <span data-ttu-id="20ffe-2018">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-2018">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ffe-2019">public int cnt()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2019">public int cnt()</span></span>                                                                  | <span data-ttu-id="20ffe-2020">Finance and Operations アプリケーション オブジェクト ツリー (AOT) で定義されているコンフィギュレーション キーの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2020">Retrieves the number of configuration keys that are defined in the Finance and Operations Application Object Tree (AOT).</span></span> |
| <span data-ttu-id="20ffe-2021">public ConfigurationKeyId cnt2Id(int cnt)</span><span class="sxs-lookup"><span data-stu-id="20ffe-2021">public ConfigurationKeyId cnt2Id(int cnt)</span></span>                                         | <span data-ttu-id="20ffe-2022">*n* 番目のコンフィギュレーション キーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2022">Retrieves the ID of the *n*th configuration key.</span></span>                                                                        |
| <span data-ttu-id="20ffe-2023">public boolean enabled(ConfigurationKeyId configurationKeyId, \[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2023">public boolean enabled(ConfigurationKeyId configurationKeyId, \[boolean enable\])</span></span> | <span data-ttu-id="20ffe-2024">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2024">Determines whether to enable or disable the object.</span></span>                                                                     |
| <span data-ttu-id="20ffe-2025">public container pack()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2025">public container pack()</span></span>                                                           | <span data-ttu-id="20ffe-2026">ConfigurationKeySet クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2026">Serializes the current instance of the ConfigurationKeySet class.</span></span>                                                       |
| <span data-ttu-id="20ffe-2027">public boolean touchedByUser(ConfigurationKeyId configurationKeyId)</span><span class="sxs-lookup"><span data-stu-id="20ffe-2027">public boolean touchedByUser(ConfigurationKeyId configurationKeyId)</span></span>               |                                                                                                                         |
| <span data-ttu-id="20ffe-2028">public void new(\[container container\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2028">public void new(\[container container\])</span></span>                                          | <span data-ttu-id="20ffe-2029">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2029">Initializes a new instance of the Object class.</span></span>                                                                         |
| <span data-ttu-id="20ffe-2030">public void loadSystemSetup()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2030">public void loadSystemSetup()</span></span>                                                     |                                                                                                                         |

### <a name="method-cnt"></a><span data-ttu-id="20ffe-2031">メソッド cnt</span><span class="sxs-lookup"><span data-stu-id="20ffe-2031">Method cnt</span></span>

<span data-ttu-id="20ffe-2032">Finance and Operations アプリケーション オブジェクト ツリー (AOT) で定義されているコンフィギュレーション キーの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2032">Retrieves the number of configuration keys that are defined in the Finance and Operations Application Object Tree (AOT).</span></span>

    public int cnt()

#### <a name="return-value"></a><span data-ttu-id="20ffe-2033">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2033">Return Value</span></span>

<span data-ttu-id="20ffe-2034">AOT で定義されているコンフィギュレーション キーの数。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2034">The number of configuration keys that are defined in the AOT.</span></span>

### <a name="method-cnt2id"></a><span data-ttu-id="20ffe-2035">メソッド cnt2Id</span><span class="sxs-lookup"><span data-stu-id="20ffe-2035">Method cnt2Id</span></span>

<span data-ttu-id="20ffe-2036">*n* 番目のコンフィギュレーション キーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2036">Retrieves the ID of the *n*th configuration key.</span></span>

    public ConfigurationKeyId cnt2Id(int cnt)

#### <a name="parameters"></a><span data-ttu-id="20ffe-2037">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2037">Parameters</span></span>

<span data-ttu-id="20ffe-2038">cnt</span><span class="sxs-lookup"><span data-stu-id="20ffe-2038">cnt</span></span>  
<span data-ttu-id="20ffe-2039">コンフィギュレーション キーのインデックス。1 とコンフィギュレーション キーの間でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2039">The index of the configuration key, which must be between 1 and the number of configuration keys.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-2040">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2040">Return Value</span></span>

<span data-ttu-id="20ffe-2041">指定されたコンフィギュレーション キーの ID。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2041">The ID of the specified configuration key.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-2042">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2042">Remarks</span></span>

<span data-ttu-id="20ffe-2043">構成キーの数を調べるには、cnt メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2043">To find the number of configuration keys, use the cnt method.</span></span> <span data-ttu-id="20ffe-2044">一般に、すべての ID が使用されているわけではないため、インデックスおよび ID は異なります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2044">In general, the index and ID will differ, because not all the IDs are used.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-2045">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-2045">Examples</span></span>

    ConfigurationKeySet configKeySet = new ConfigurationKeySet(); 
    DictConfigurationKey dictConfigurationKey; 
    int i; 

    configKeySet.loadSystemSetup(); 
    for (i=1; i<= configKeySet.cnt(); i++) 
    { 
        setPrefix('Disabled configurationkeys'); 
        if (!configKeySet.enabled( configKeySet.cnt2Id(i) )) 
        { 
            dictConfigurationKey =  
                new DictConfigurationKey(configKeySet.cnt2id(i)); 
            info (dictConfigurationKey.name()); 
        } 
    }

### <a name="method-enabled"></a><span data-ttu-id="20ffe-2046">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="20ffe-2046">Method enabled</span></span>

<span data-ttu-id="20ffe-2047">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2047">Determines whether to enable or disable the object.</span></span>

    public boolean enabled(ConfigurationKeyId configurationKeyId, [boolean enable])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2048">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2048">Parameters</span></span>

<span data-ttu-id="20ffe-2049">configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="20ffe-2049">configurationKeyId</span></span>  
<span data-ttu-id="20ffe-2050">構成キーの状態を設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2050">The value to which to set the state of the configuration key; optional.</span></span>

<!-- -->

<span data-ttu-id="20ffe-2051">enable</span><span class="sxs-lookup"><span data-stu-id="20ffe-2051">enable</span></span>  
<span data-ttu-id="20ffe-2052">構成キーの状態を設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2052">The value to which to set the state of the configuration key; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-2053">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2053">Return Value</span></span>

<span data-ttu-id="20ffe-2054">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2054">true if the object is enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-2055">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2055">Remarks</span></span>

<span data-ttu-id="20ffe-2056">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2056">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="20ffe-2057">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2057">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="20ffe-2058">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2058">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-2059">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-2059">Examples</span></span>

<span data-ttu-id="20ffe-2060">この例では、ConfigurationKeySet.enabled メソッドの使用方法を示します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2060">This example demonstrates the use of the ConfigurationKeySet.enabled method.</span></span>

    static void testConfigKey(Args _args) 
    { 
        ConfigurationKeySet configKey = new ConfigurationKeySet(); 

        configKey.loadSystemSetup(); 

        // Set the enable value to false. 
        configKey.enabled(configurationkeynum(RouteApprove), false); 
        SysDictConfigurationKey::save(configKey.pack()); 
        SysSecurity::reload(true); 
        print isConfigurationkeyEnabled(configurationkeynum(RouteApprove)); 

        // Set the enable value to true. 
        configKey.enabled(configurationkeynum(RouteApprove), true); 
        //Save the configuration key setup. 
        SysDictConfigurationKey::save(configKey.pack()); 
        SysSecurity::reload(true); 

        print isConfigurationkeyEnabled(configurationkeynum(RouteApprove)); 

        pause; 
    }

### <a name="method-pack"></a><span data-ttu-id="20ffe-2061">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="20ffe-2061">Method pack</span></span>

<span data-ttu-id="20ffe-2062">ConfigurationKeySet クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2062">Serializes the current instance of the ConfigurationKeySet class.</span></span>

    public container pack()

#### <a name="return-value"></a><span data-ttu-id="20ffe-2063">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2063">Return Value</span></span>

<span data-ttu-id="20ffe-2064">ConfigurationKeySet クラスの現在のインスタンスを含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2064">A container that contains the current instance of the ConfigurationKeySet class.</span></span>

### <a name="method-touchedbyuser"></a><span data-ttu-id="20ffe-2065">メソッド touchedByUser</span><span class="sxs-lookup"><span data-stu-id="20ffe-2065">Method touchedByUser</span></span>

    public boolean touchedByUser(ConfigurationKeyId configurationKeyId)

#### <a name="parameters"></a><span data-ttu-id="20ffe-2066">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2066">Parameters</span></span>

<span data-ttu-id="20ffe-2067">configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="20ffe-2067">configurationKeyId</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2068">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2068">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="20ffe-2069">メソッド new</span><span class="sxs-lookup"><span data-stu-id="20ffe-2069">Method new</span></span>

<span data-ttu-id="20ffe-2070">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2070">Initializes a new instance of the Object class.</span></span>

    public void new([container container])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2071">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2071">Parameters</span></span>

<span data-ttu-id="20ffe-2072">コンテナー</span><span class="sxs-lookup"><span data-stu-id="20ffe-2072">container</span></span>  

### <a name="method-loadsystemsetup"></a><span data-ttu-id="20ffe-2073">メソッド loadSystemSetup</span><span class="sxs-lookup"><span data-stu-id="20ffe-2073">Method loadSystemSetup</span></span>

    public void loadSystemSetup()

## <a name="class-connection"></a><span data-ttu-id="20ffe-2074">クラス接続</span><span class="sxs-lookup"><span data-stu-id="20ffe-2074">Class Connection</span></span>
    class Connection extends Object

<span data-ttu-id="20ffe-2075">接続クラスは、SQL ステートメントを実行して結果を返す現在のデータベース セッションを確立します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2075">The Connection class establishes a current database session that you can use to execute SQL statements and return results.</span></span>

### <a name="remarks"></a><span data-ttu-id="20ffe-2076">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2076">Remarks</span></span>

<span data-ttu-id="20ffe-2077">次のクラスは Connection クラスを拡張しています。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2077">The following classes extend the Connection class:</span></span>

-   <span data-ttu-id="20ffe-2078">OdbcConnection</span><span class="sxs-lookup"><span data-stu-id="20ffe-2078">OdbcConnection</span></span>
-   <span data-ttu-id="20ffe-2079">OciConnection</span><span class="sxs-lookup"><span data-stu-id="20ffe-2079">OciConnection</span></span>
-   <span data-ttu-id="20ffe-2080">UserConnection</span><span class="sxs-lookup"><span data-stu-id="20ffe-2080">UserConnection</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-2081">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-2081">Examples</span></span>

<span data-ttu-id="20ffe-2082">次の例では、createStatement メソッドはステートメント オブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2082">In the following example, the createStatement method initializes the Statement object.</span></span> <span data-ttu-id="20ffe-2083">Statement.executeQuery メソッドは、SQL ステートメントを実行し、ResultSet オブジェクトに取得したデータを格納します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2083">The Statement.executeQuery method executes an SQL statement and then stores the retrieved data in the ResultSet object.</span></span>

    server static void main(Args args) 
    { 
        Connection con = new Connection(); 
        Statement stmt = con.createStatement(); 
        ResultSet r; 
        str sql; 
        SqlStatementExecutePermission perm; 

        sql = strfmt('SELECT VALUE FROM SQLSYSTEMVARIABLES'); 

        // Set code access permission to help protect the use of 
        // Statement.executeUpdate. 
        perm = new SqlStatementExecutePermission(sql); 
        perm.assert(); 

        try 
        { 
            r = stmt.executeQuery(sql); 
            while (r.next()) 
            { 
                print r.getString(1); 
                pause; 
            } 
        } 
        catch (exception::Error) 
        { 
            print "An error occurred in the query."; 
            pause; 
        } 
        // Code access permission scope ends here. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="methods"></a><span data-ttu-id="20ffe-2084">メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-2084">Methods</span></span>

| <span data-ttu-id="20ffe-2085">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-2085">Method</span></span>                                                                                                           | <span data-ttu-id="20ffe-2086">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-2086">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ffe-2087">public Statement createStatement(\[ResultSetType resultSetType\], \[ResultSetConcurrency resultSetConcurrency\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2087">public Statement createStatement(\[ResultSetType resultSetType\], \[ResultSetConcurrency resultSetConcurrency\])</span></span> | <span data-ttu-id="20ffe-2088">SQL ステートメントの実行に使用されるステートメント オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2088">Creates a Statement object that is used to execute an SQL statement.</span></span>                                                                                                                    |
| <span data-ttu-id="20ffe-2089">public int odbcGetInfoInt(int InfoId)</span><span class="sxs-lookup"><span data-stu-id="20ffe-2089">public int odbcGetInfoInt(int InfoId)</span></span>                                                                            | <span data-ttu-id="20ffe-2090">ODBC ドライバに関する情報と接続に関連付けられているデータのソースを取得する SQLGetInfo Open Database Connectivity (ODBC) 関数へのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2090">Provides an interface to the SQLGetInfo Open Database Connectivity (ODBC) function to retrieve information about the ODBC driver and data source that are associated with a connection.</span></span> |
| <span data-ttu-id="20ffe-2091">public int odbcGetInfoLong(int InfoId)</span><span class="sxs-lookup"><span data-stu-id="20ffe-2091">public int odbcGetInfoLong(int InfoId)</span></span>                                                                           | <span data-ttu-id="20ffe-2092">ODBC ドライバに関する情報と接続に関連付けられているデータのソースを取得する SQLGetInfo ODBC 関数へのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2092">Provides an interface to the SQLGetInfo ODBC function to retrieve information about the ODBC driver and data source that are associated with a connection.</span></span>                              |
| <span data-ttu-id="20ffe-2093">public str odbcGetInfoStr(int InfoId)</span><span class="sxs-lookup"><span data-stu-id="20ffe-2093">public str odbcGetInfoStr(int InfoId)</span></span>                                                                            | <span data-ttu-id="20ffe-2094">ODBC ドライバに関する情報と接続に関連付けられているデータのソースを文字列形式で取得する SQLGetInfo ODBC 関数へのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2094">Provides an interface to the SQLGetInfo ODBC function to retrieve information, in string format, about the ODBC driver and data source that are associated with a connection.</span></span>           |
| <span data-ttu-id="20ffe-2095">public str toString()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2095">public str toString()</span></span>                                                                                            | <span data-ttu-id="20ffe-2096">接続オブジェクトを文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2096">Converts the Connection object to a string.</span></span>                                                                                                                                             |
| <span data-ttu-id="20ffe-2097">public int ttsLevel()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2097">public int ttsLevel()</span></span>                                                                                            | <span data-ttu-id="20ffe-2098">トランザクションを開始するために使用する ttsbegin メソッドの最後の呼び出しの数を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2098">Returns the number for the last call to the ttsbegin method that is used to begin a transaction.</span></span>                                                                                        |
| <span data-ttu-id="20ffe-2099">public boolean isInTransactionScope()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2099">public boolean isInTransactionScope()</span></span>                                                                            |                                                                                                                                                                                         |
| <span data-ttu-id="20ffe-2100">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2100">public void finalize()</span></span>                                                                                           |                                                                                                                                                                                         |
| <span data-ttu-id="20ffe-2101">public void transactionScopeAbort()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2101">public void transactionScopeAbort()</span></span>                                                                              |                                                                                                                                                                                         |
| <span data-ttu-id="20ffe-2102">public void ttsNotifyCommit()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2102">public void ttsNotifyCommit()</span></span>                                                                                    | <span data-ttu-id="20ffe-2103">ttscommit メソッドが呼び出されると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2103">Is called when the ttscommit method is called.</span></span>                                                                                                                                          |
| <span data-ttu-id="20ffe-2104">public void transactionScopeBegin()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2104">public void transactionScopeBegin()</span></span>                                                                              |                                                                                                                                                                                         |
| <span data-ttu-id="20ffe-2105">public void transactionScopeCommit()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2105">public void transactionScopeCommit()</span></span>                                                                             |                                                                                                                                                                                         |
| <span data-ttu-id="20ffe-2106">public void ttsNotifyBegin()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2106">public void ttsNotifyBegin()</span></span>                                                                                     |                                                                                                                                                                                         |
| <span data-ttu-id="20ffe-2107">public void ttsbegin()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2107">public void ttsbegin()</span></span>                                                                                           | <span data-ttu-id="20ffe-2108">トランザクションを開始します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2108">Begins a transaction.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="20ffe-2109">public void ttsabort()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2109">public void ttsabort()</span></span>                                                                                           | <span data-ttu-id="20ffe-2110">トランザクションに関連する変更を破棄し、データベースを元の状態にロールバックします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2110">Discards changes that are associated with a transaction and rolls the database back to the original state.</span></span>                                                                              |
| <span data-ttu-id="20ffe-2111">public void new()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2111">public void new()</span></span>                                                                                                | <span data-ttu-id="20ffe-2112">Connection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2112">Initializes a new instance of the Connection class.</span></span>                                                                                                                                     |
| <span data-ttu-id="20ffe-2113">public void ttsNotifyAbort()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2113">public void ttsNotifyAbort()</span></span>                                                                                     | <span data-ttu-id="20ffe-2114">例外がスローされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2114">Is called when an exception is thrown.</span></span>                                                                                                                                                  |
| <span data-ttu-id="20ffe-2115">public void ttscommit()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2115">public void ttscommit()</span></span>                                                                                          | <span data-ttu-id="20ffe-2116">トランザクションに関連付けられている変更をデータベースにコミットします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2116">Commits the changes that are associated with a transaction to the database.</span></span>                                                                                                             |

### <a name="method-createstatement"></a><span data-ttu-id="20ffe-2117">メソッド createStatement</span><span class="sxs-lookup"><span data-stu-id="20ffe-2117">Method createStatement</span></span>

<span data-ttu-id="20ffe-2118">SQL ステートメントの実行に使用されるステートメント オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2118">Creates a Statement object that is used to execute an SQL statement.</span></span>

    public Statement createStatement([ResultSetType resultSetType], [ResultSetConcurrency resultSetConcurrency])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2119">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2119">Parameters</span></span>

<span data-ttu-id="20ffe-2120">resultSetType</span><span class="sxs-lookup"><span data-stu-id="20ffe-2120">resultSetType</span></span>  
<span data-ttu-id="20ffe-2121">既定で読み取り専用を指定する ResultSetConcurrency 列挙。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2121">A ResultSetConcurrency enumeration that specifies ReadOnly by default.</span></span>

<!-- -->

<span data-ttu-id="20ffe-2122">resultSetConcurrency</span><span class="sxs-lookup"><span data-stu-id="20ffe-2122">resultSetConcurrency</span></span>  
<span data-ttu-id="20ffe-2123">既定で読み取り専用を指定する ResultSetConcurrency 列挙。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2123">A ResultSetConcurrency enumeration that specifies ReadOnly by default.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-2124">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2124">Return Value</span></span>

<span data-ttu-id="20ffe-2125">新しいステートメント オブジェクトであるデータ型の値です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2125">A data type value that is a new Statement object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-2126">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2126">Remarks</span></span>

<span data-ttu-id="20ffe-2127">createStatement メソッドを使用して SQL ステートメントを作成し、ユーザーがステートメントへの入力を制御できるようにすると、SQL インジェクション脅威の危険性があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2127">There is risk of an SQL injection threat when you use the createStatement method to create an SQL statement and then allow a user to control input to the statement.</span></span> <span data-ttu-id="20ffe-2128">詳細については [SQL インジェクション](https://go.microsoft.com/fwlink/?LinkId=114986) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2128">For information, see [SQL Injection](https://go.microsoft.com/fwlink/?LinkId=114986).</span></span> <span data-ttu-id="20ffe-2129">AOT、ビュー、および X++ Select ステートメントでは、SQL ステートメントを実行するための安全な代替手段として、クエリ要素を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2129">You can use Query Elements in the AOT, views, and X++ Select statements as safer alternatives to executing SQL statements.</span></span>

### <a name="method-odbcgetinfoint"></a><span data-ttu-id="20ffe-2130">メソッド odbcGetInfoInt</span><span class="sxs-lookup"><span data-stu-id="20ffe-2130">Method odbcGetInfoInt</span></span>

<span data-ttu-id="20ffe-2131">ODBC ドライバに関する情報と接続に関連付けられているデータのソースを取得する SQLGetInfo Open Database Connectivity (ODBC) 関数へのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2131">Provides an interface to the SQLGetInfo Open Database Connectivity (ODBC) function to retrieve information about the ODBC driver and data source that are associated with a connection.</span></span>

    public int odbcGetInfoInt(int InfoId)

#### <a name="parameters"></a><span data-ttu-id="20ffe-2132">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2132">Parameters</span></span>

<span data-ttu-id="20ffe-2133">InfoId</span><span class="sxs-lookup"><span data-stu-id="20ffe-2133">InfoId</span></span>  
<span data-ttu-id="20ffe-2134">ODBC 標準に従って要求された情報の ID を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2134">An integer that specifies an ID for the requested information according to the ODBC standard.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-2135">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2135">Return Value</span></span>

<span data-ttu-id="20ffe-2136">取得される情報の整数値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2136">An integer value for the information that is retrieved.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-2137">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-2137">Examples</span></span>

<span data-ttu-id="20ffe-2138">次の例では、odbcGetInfoInt メソッドは列名の最大の長さの整数値を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2138">In the following example, the odbcGetInfoInt method returns an integer value for the maximum length of the column name.</span></span>

    void getConnection() 
    { 
        Connection con; 
        Statement stmt; 
        int info; 

        #define.SQL_MAX_COLUMN_NAME_LEN(30) 
        con = new Connection(); 

        try 
        { 
            info = con.odbcGetInfoInt(#SQL_MAX_COLUMN_NAME_LEN); 

            print info; 
            pause; 
         } 

        catch(exception::Error) 
        { 
            print "An error occurred."; 

        } 

    }

### <a name="method-odbcgetinfolong"></a><span data-ttu-id="20ffe-2139">メソッド odbcGetInfoLong</span><span class="sxs-lookup"><span data-stu-id="20ffe-2139">Method odbcGetInfoLong</span></span>

<span data-ttu-id="20ffe-2140">ODBC ドライバに関する情報と接続に関連付けられているデータのソースを取得する SQLGetInfo ODBC 関数へのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2140">Provides an interface to the SQLGetInfo ODBC function to retrieve information about the ODBC driver and data source that are associated with a connection.</span></span>

    public int odbcGetInfoLong(int InfoId)

#### <a name="parameters"></a><span data-ttu-id="20ffe-2141">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2141">Parameters</span></span>

<span data-ttu-id="20ffe-2142">InfoId</span><span class="sxs-lookup"><span data-stu-id="20ffe-2142">InfoId</span></span>  
<span data-ttu-id="20ffe-2143">ODBC 標準による要求された情報の ID を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2143">An Integer data type that specifies an ID for the requested information, according to the ODBC standard.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-2144">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2144">Return Value</span></span>

<span data-ttu-id="20ffe-2145">取得される情報の整数データ型値です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2145">An Integer data type value for the information that is retrieved.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-2146">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2146">Remarks</span></span>

<span data-ttu-id="20ffe-2147">このメソッドは 32 ビット整数を取得し、整数として返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2147">This method retrieves a 32-bit integer and returns it as an integer.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-2148">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-2148">Examples</span></span>

<span data-ttu-id="20ffe-2149">次の例では、odbcGetInfoLong メソッドは行の最大サイズの整数を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2149">In the following example, the odbcGetInfoLong method returns an integer for the maximum row size.</span></span>

    void getConnection() 
    { 
        Connection con; 
        Statement stmt; 
        int info; 

        #define.SQL_MAX_ROW_SIZE(104) 
        con = new Connection(); 

        try 
        { 
            info = con.odbcGetInfoLong(#SQL_MAX_ROW_SIZE); 

            print info; 
            pause; 
         } 

        catch(exception::Error) 
        { 
            print "An error occurred."; 

        } 

    }

### <a name="method-odbcgetinfostr"></a><span data-ttu-id="20ffe-2150">メソッド odbcGetInfoStr</span><span class="sxs-lookup"><span data-stu-id="20ffe-2150">Method odbcGetInfoStr</span></span>

<span data-ttu-id="20ffe-2151">ODBC ドライバに関する情報と接続に関連付けられているデータのソースを文字列形式で取得する SQLGetInfo ODBC 関数へのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2151">Provides an interface to the SQLGetInfo ODBC function to retrieve information, in string format, about the ODBC driver and data source that are associated with a connection.</span></span>

    public str odbcGetInfoStr(int InfoId)

#### <a name="parameters"></a><span data-ttu-id="20ffe-2152">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2152">Parameters</span></span>

<span data-ttu-id="20ffe-2153">InfoId</span><span class="sxs-lookup"><span data-stu-id="20ffe-2153">InfoId</span></span>  
<span data-ttu-id="20ffe-2154">ODBC 標準による要求された情報の ID を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2154">An Integer data type that specifies an ID for the requested information, according to the ODBC standard.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20ffe-2155">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2155">Return Value</span></span>

<span data-ttu-id="20ffe-2156">取得される情報の文字列データ型値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2156">A String data type value for the information that is retrieved.</span></span>

#### <a name="examples"></a><span data-ttu-id="20ffe-2157">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-2157">Examples</span></span>

<span data-ttu-id="20ffe-2158">次の例では、odbcGetInfoStr メソッドはデータベース管理システムの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2158">In the following example, the odbcGetInfoStr method returns the name of the database management system.</span></span>

    void getConnection() 
    { 
        Connection con; 
        str info; 

        #define.SQL_DBMS_NAME(17) 
        con = new Connection(); 

        try 
        { 
            info = con.odbcGetInfoStr(#SQL_DBMS_NAME); 

            print info; 
            pause; 
         } 

        catch(exception::Error) 
        { 
            print "An error occurred."; 
        } 
    }

### <a name="method-tostring"></a><span data-ttu-id="20ffe-2159">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="20ffe-2159">Method toString</span></span>

<span data-ttu-id="20ffe-2160">接続オブジェクトを文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2160">Converts the Connection object to a string.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="20ffe-2161">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2161">Return Value</span></span>

<span data-ttu-id="20ffe-2162">接続オブジェクトの文字列値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2162">A string value for the Connection object.</span></span>

### <a name="method-ttslevel"></a><span data-ttu-id="20ffe-2163">メソッド ttsLevel</span><span class="sxs-lookup"><span data-stu-id="20ffe-2163">Method ttsLevel</span></span>

<span data-ttu-id="20ffe-2164">トランザクションを開始するために使用する ttsbegin メソッドの最後の呼び出しの数を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2164">Returns the number for the last call to the ttsbegin method that is used to begin a transaction.</span></span>

    public int ttsLevel()

#### <a name="return-value"></a><span data-ttu-id="20ffe-2165">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2165">Return Value</span></span>

<span data-ttu-id="20ffe-2166">ttsbegin メソッドに最後の呼び出しの番号を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2166">An integer value that indicates the number for the last call to the ttsbegin method.</span></span> <span data-ttu-id="20ffe-2167">たとえば、ttsLevel メソッドが ttsbegin メソッドへの 3 回目の呼び出し後に呼び出されると、戻り値は 3 になります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2167">For example, if the ttsLevel method is called after the third call to the ttsbegin method, the return value is 3.</span></span>

### <a name="method-isintransactionscope"></a><span data-ttu-id="20ffe-2168">メソッド isInTransactionScope</span><span class="sxs-lookup"><span data-stu-id="20ffe-2168">Method isInTransactionScope</span></span>

    public boolean isInTransactionScope()

#### <a name="return-value"></a><span data-ttu-id="20ffe-2169">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2169">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="20ffe-2170">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="20ffe-2170">Method finalize</span></span>

    public void finalize()

### <a name="method-transactionscopeabort"></a><span data-ttu-id="20ffe-2171">メソッド transactionScopeAbort</span><span class="sxs-lookup"><span data-stu-id="20ffe-2171">Method transactionScopeAbort</span></span>

    public void transactionScopeAbort()

### <a name="method-ttsnotifycommit"></a><span data-ttu-id="20ffe-2172">メソッド ttsNotifyCommit</span><span class="sxs-lookup"><span data-stu-id="20ffe-2172">Method ttsNotifyCommit</span></span>

<span data-ttu-id="20ffe-2173">ttscommit メソッドが呼び出されると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2173">Is called when the ttscommit method is called.</span></span>

    public void ttsNotifyCommit()

### <a name="method-transactionscopebegin"></a><span data-ttu-id="20ffe-2174">メソッド transactionScopeBegin</span><span class="sxs-lookup"><span data-stu-id="20ffe-2174">Method transactionScopeBegin</span></span>

    public void transactionScopeBegin()

### <a name="method-transactionscopecommit"></a><span data-ttu-id="20ffe-2175">メソッド transactionScopeCommit</span><span class="sxs-lookup"><span data-stu-id="20ffe-2175">Method transactionScopeCommit</span></span>

    public void transactionScopeCommit()

### <a name="method-ttsnotifybegin"></a><span data-ttu-id="20ffe-2176">メソッド ttsNotifyBegin</span><span class="sxs-lookup"><span data-stu-id="20ffe-2176">Method ttsNotifyBegin</span></span>

    public void ttsNotifyBegin()

### <a name="method-ttsbegin"></a><span data-ttu-id="20ffe-2177">メソッド ttsbegin</span><span class="sxs-lookup"><span data-stu-id="20ffe-2177">Method ttsbegin</span></span>

<span data-ttu-id="20ffe-2178">トランザクションを開始します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2178">Begins a transaction.</span></span>

    public void ttsbegin()

### <a name="method-ttsabort"></a><span data-ttu-id="20ffe-2179">メソッド ttsabort</span><span class="sxs-lookup"><span data-stu-id="20ffe-2179">Method ttsabort</span></span>

<span data-ttu-id="20ffe-2180">トランザクションに関連する変更を破棄し、データベースを元の状態にロールバックします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2180">Discards changes that are associated with a transaction and rolls the database back to the original state.</span></span>

    public void ttsabort()

### <a name="method-new"></a><span data-ttu-id="20ffe-2181">メソッド new</span><span class="sxs-lookup"><span data-stu-id="20ffe-2181">Method new</span></span>

<span data-ttu-id="20ffe-2182">Connection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2182">Initializes a new instance of the Connection class.</span></span>

    public void new()

### <a name="method-ttsnotifyabort"></a><span data-ttu-id="20ffe-2183">メソッド ttsNotifyAbort</span><span class="sxs-lookup"><span data-stu-id="20ffe-2183">Method ttsNotifyAbort</span></span>

<span data-ttu-id="20ffe-2184">例外がスローされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2184">Is called when an exception is thrown.</span></span>

    public void ttsNotifyAbort()

### <a name="method-ttscommit"></a><span data-ttu-id="20ffe-2185">メソッド ttscommit</span><span class="sxs-lookup"><span data-stu-id="20ffe-2185">Method ttscommit</span></span>

<span data-ttu-id="20ffe-2186">トランザクションに関連付けられている変更をデータベースにコミットします。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2186">Commits the changes that are associated with a transaction to the database.</span></span>

    public void ttscommit()

## <a name="class-containerclass"></a><span data-ttu-id="20ffe-2187">クラス ContainerClass</span><span class="sxs-lookup"><span data-stu-id="20ffe-2187">Class ContainerClass</span></span>
    class ContainerClass extends Object

### <a name="remarks"></a><span data-ttu-id="20ffe-2188">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2188">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-2189">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-2189">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="20ffe-2190">メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-2190">Methods</span></span>

| <span data-ttu-id="20ffe-2191">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-2191">Method</span></span>                                                              | <span data-ttu-id="20ffe-2192">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-2192">Description</span></span>                                          |
|---------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="20ffe-2193">public int length()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2193">public int length()</span></span>                                                 |                                                      |
| <span data-ttu-id="20ffe-2194">public container toBlob()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2194">public container toBlob()</span></span>                                           |                                                      |
| <span data-ttu-id="20ffe-2195">public str toString()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2195">public str toString()</span></span>                                               | <span data-ttu-id="20ffe-2196">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2196">Returns a string that represents the current object.</span></span> |
| <span data-ttu-id="20ffe-2197">public container value()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2197">public container value()</span></span>                                            |                                                      |
| <span data-ttu-id="20ffe-2198">::public static container blob2Container(container blob\_container)</span><span class="sxs-lookup"><span data-stu-id="20ffe-2198">::public static container blob2Container(container blob\_container)</span></span> |                                                      |
| <span data-ttu-id="20ffe-2199">::public static int containerLength(container container)</span><span class="sxs-lookup"><span data-stu-id="20ffe-2199">::public static int containerLength(container container)</span></span>            |                                                      |
| <span data-ttu-id="20ffe-2200">public void new(container container)</span><span class="sxs-lookup"><span data-stu-id="20ffe-2200">public void new(container container)</span></span>                                | <span data-ttu-id="20ffe-2201">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2201">Initializes a new instance of the Object class.</span></span>      |

### <a name="method-length"></a><span data-ttu-id="20ffe-2202">メソッド length</span><span class="sxs-lookup"><span data-stu-id="20ffe-2202">Method length</span></span>

    public int length()

#### <a name="return-value"></a><span data-ttu-id="20ffe-2203">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2203">Return Value</span></span>

### <a name="method-toblob"></a><span data-ttu-id="20ffe-2204">メソッド toBlob</span><span class="sxs-lookup"><span data-stu-id="20ffe-2204">Method toBlob</span></span>

    public container toBlob()

#### <a name="return-value"></a><span data-ttu-id="20ffe-2205">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2205">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="20ffe-2206">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="20ffe-2206">Method toString</span></span>

<span data-ttu-id="20ffe-2207">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2207">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="20ffe-2208">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2208">Return Value</span></span>

<span data-ttu-id="20ffe-2209">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2209">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-2210">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2210">Remarks</span></span>

<span data-ttu-id="20ffe-2211">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2211">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="20ffe-2212">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2212">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="20ffe-2213">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2213">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="20ffe-2214">メソッド value</span><span class="sxs-lookup"><span data-stu-id="20ffe-2214">Method value</span></span>

    public container value()

#### <a name="return-value"></a><span data-ttu-id="20ffe-2215">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2215">Return Value</span></span>

### <a name="method-blob2container"></a><span data-ttu-id="20ffe-2216">メソッド blob2Container</span><span class="sxs-lookup"><span data-stu-id="20ffe-2216">Method blob2Container</span></span>

    public static container blob2Container(container blob_container)

#### <a name="parameters"></a><span data-ttu-id="20ffe-2217">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2217">Parameters</span></span>

<span data-ttu-id="20ffe-2218">blob\_container</span><span class="sxs-lookup"><span data-stu-id="20ffe-2218">blob\_container</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2219">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2219">Return Value</span></span>

### <a name="method-containerlength"></a><span data-ttu-id="20ffe-2220">メソッド containerLength</span><span class="sxs-lookup"><span data-stu-id="20ffe-2220">Method containerLength</span></span>

    public static int containerLength(container container)

#### <a name="parameters"></a><span data-ttu-id="20ffe-2221">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2221">Parameters</span></span>

<span data-ttu-id="20ffe-2222">コンテナー</span><span class="sxs-lookup"><span data-stu-id="20ffe-2222">container</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2223">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2223">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="20ffe-2224">メソッド new</span><span class="sxs-lookup"><span data-stu-id="20ffe-2224">Method new</span></span>

<span data-ttu-id="20ffe-2225">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2225">Initializes a new instance of the Object class.</span></span>

    public void new(container container)

#### <a name="parameters"></a><span data-ttu-id="20ffe-2226">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2226">Parameters</span></span>

<span data-ttu-id="20ffe-2227">コンテナー</span><span class="sxs-lookup"><span data-stu-id="20ffe-2227">container</span></span>  

## <a name="class-controlfiltervalue"></a><span data-ttu-id="20ffe-2228">クラス ControlFilterValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-2228">Class ControlFilterValue</span></span>
    class ControlFilterValue extends FilterValue

### <a name="remarks"></a><span data-ttu-id="20ffe-2229">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2229">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-2230">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-2230">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="20ffe-2231">メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-2231">Methods</span></span>

| <span data-ttu-id="20ffe-2232">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-2232">Method</span></span>                                                | <span data-ttu-id="20ffe-2233">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-2233">Description</span></span>                                     |
|-------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="20ffe-2234">public FormControl control()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2234">public FormControl control()</span></span>                          |                                                 |
| <span data-ttu-id="20ffe-2235">public void new(FormControl control, str filterValue)</span><span class="sxs-lookup"><span data-stu-id="20ffe-2235">public void new(FormControl control, str filterValue)</span></span> | <span data-ttu-id="20ffe-2236">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2236">Initializes a new instance of the Object class.</span></span> |

### <a name="method-control"></a><span data-ttu-id="20ffe-2237">メソッド control</span><span class="sxs-lookup"><span data-stu-id="20ffe-2237">Method control</span></span>

    public FormControl control()

#### <a name="return-value"></a><span data-ttu-id="20ffe-2238">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2238">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="20ffe-2239">メソッド new</span><span class="sxs-lookup"><span data-stu-id="20ffe-2239">Method new</span></span>

<span data-ttu-id="20ffe-2240">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2240">Initializes a new instance of the Object class.</span></span>

    public void new(FormControl control, str filterValue)

#### <a name="parameters"></a><span data-ttu-id="20ffe-2241">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2241">Parameters</span></span>

<span data-ttu-id="20ffe-2242">control</span><span class="sxs-lookup"><span data-stu-id="20ffe-2242">control</span></span>  

<!-- -->

<span data-ttu-id="20ffe-2243">filterValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-2243">filterValue</span></span>  

## <a name="class-controlnode"></a><span data-ttu-id="20ffe-2244">クラス ControlNode</span><span class="sxs-lookup"><span data-stu-id="20ffe-2244">Class ControlNode</span></span>
    class ControlNode extends TreeNode

<span data-ttu-id="20ffe-2245">ControlNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2245">The ControlNode class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="20ffe-2246">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2246">Remarks</span></span>

<span data-ttu-id="20ffe-2247">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2247">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-2248">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-2248">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="20ffe-2249">メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-2249">Methods</span></span>

| <span data-ttu-id="20ffe-2250">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-2250">Method</span></span>                                         | <span data-ttu-id="20ffe-2251">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-2251">Description</span></span>                                       |
|------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="20ffe-2252">public void new(str name, \[TreeNode parent\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2252">public void new(str name, \[TreeNode parent\])</span></span> | <span data-ttu-id="20ffe-2253">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2253">Initializes a new instance of the TreeNode class.</span></span> |

### <a name="method-new"></a><span data-ttu-id="20ffe-2254">メソッド new</span><span class="sxs-lookup"><span data-stu-id="20ffe-2254">Method new</span></span>

<span data-ttu-id="20ffe-2255">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2255">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str name, [TreeNode parent])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2256">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2256">Parameters</span></span>

<span data-ttu-id="20ffe-2257">名前</span><span class="sxs-lookup"><span data-stu-id="20ffe-2257">name</span></span>  

<!-- -->

<span data-ttu-id="20ffe-2258">parent</span><span class="sxs-lookup"><span data-stu-id="20ffe-2258">parent</span></span>  

## <a name="class-cryptoapi"></a><span data-ttu-id="20ffe-2259">クラス CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="20ffe-2259">Class CryptoAPI</span></span>
    class CryptoAPI extends Object

### <a name="remarks"></a><span data-ttu-id="20ffe-2260">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2260">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-2261">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-2261">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="20ffe-2262">メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-2262">Methods</span></span>

| <span data-ttu-id="20ffe-2263">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-2263">Method</span></span>                                   | <span data-ttu-id="20ffe-2264">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-2264">Description</span></span>                                     |
|------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="20ffe-2265">public container decrypt(container blob)</span><span class="sxs-lookup"><span data-stu-id="20ffe-2265">public container decrypt(container blob)</span></span> |                                                 |
| <span data-ttu-id="20ffe-2266">public container encrypt(container blob)</span><span class="sxs-lookup"><span data-stu-id="20ffe-2266">public container encrypt(container blob)</span></span> |                                                 |
| <span data-ttu-id="20ffe-2267">public container getKey()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2267">public container getKey()</span></span>                |                                                 |
| <span data-ttu-id="20ffe-2268">public Int64 salt()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2268">public Int64 salt()</span></span>                      |                                                 |
| <span data-ttu-id="20ffe-2269">public void new(Int64 salt)</span><span class="sxs-lookup"><span data-stu-id="20ffe-2269">public void new(Int64 salt)</span></span>              | <span data-ttu-id="20ffe-2270">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2270">Initializes a new instance of the Object class.</span></span> |
| <span data-ttu-id="20ffe-2271">::public static void resetKey()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2271">::public static void resetKey()</span></span>          |                                                 |

### <a name="method-decrypt"></a><span data-ttu-id="20ffe-2272">メソッド decrypt</span><span class="sxs-lookup"><span data-stu-id="20ffe-2272">Method decrypt</span></span>

    public container decrypt(container blob)

#### <a name="parameters"></a><span data-ttu-id="20ffe-2273">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2273">Parameters</span></span>

<span data-ttu-id="20ffe-2274">blob</span><span class="sxs-lookup"><span data-stu-id="20ffe-2274">blob</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2275">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2275">Return Value</span></span>

### <a name="method-encrypt"></a><span data-ttu-id="20ffe-2276">メソッド encrypt</span><span class="sxs-lookup"><span data-stu-id="20ffe-2276">Method encrypt</span></span>

    public container encrypt(container blob)

#### <a name="parameters"></a><span data-ttu-id="20ffe-2277">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2277">Parameters</span></span>

<span data-ttu-id="20ffe-2278">blob</span><span class="sxs-lookup"><span data-stu-id="20ffe-2278">blob</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2279">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2279">Return Value</span></span>

### <a name="method-getkey"></a><span data-ttu-id="20ffe-2280">メソッド getKey</span><span class="sxs-lookup"><span data-stu-id="20ffe-2280">Method getKey</span></span>

    public container getKey()

#### <a name="return-value"></a><span data-ttu-id="20ffe-2281">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2281">Return Value</span></span>

### <a name="method-salt"></a><span data-ttu-id="20ffe-2282">メソッド salt</span><span class="sxs-lookup"><span data-stu-id="20ffe-2282">Method salt</span></span>

    public Int64 salt()

#### <a name="return-value"></a><span data-ttu-id="20ffe-2283">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2283">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="20ffe-2284">メソッド new</span><span class="sxs-lookup"><span data-stu-id="20ffe-2284">Method new</span></span>

<span data-ttu-id="20ffe-2285">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2285">Initializes a new instance of the Object class.</span></span>

    public void new(Int64 salt)

#### <a name="parameters"></a><span data-ttu-id="20ffe-2286">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2286">Parameters</span></span>

<span data-ttu-id="20ffe-2287">salt</span><span class="sxs-lookup"><span data-stu-id="20ffe-2287">salt</span></span>  

### <a name="method-resetkey"></a><span data-ttu-id="20ffe-2288">メソッド resetKey</span><span class="sxs-lookup"><span data-stu-id="20ffe-2288">Method resetKey</span></span>

    public static void resetKey()

## <a name="class-cue"></a><span data-ttu-id="20ffe-2289">クラス キュー</span><span class="sxs-lookup"><span data-stu-id="20ffe-2289">Class Cue</span></span>
    class Cue extends TreeNode

### <a name="remarks"></a><span data-ttu-id="20ffe-2290">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2290">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-2291">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-2291">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="20ffe-2292">メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-2292">Methods</span></span>

| <span data-ttu-id="20ffe-2293">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-2293">Method</span></span>                                         | <span data-ttu-id="20ffe-2294">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-2294">Description</span></span>                                                                                                                               |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ffe-2295">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2295">public str changedBy(\[str value\])</span></span>            | <span data-ttu-id="20ffe-2296">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2296">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="20ffe-2297">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2297">public Date changedDate(\[Date value\])</span></span>        | <span data-ttu-id="20ffe-2298">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2298">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="20ffe-2299">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2299">public str changedTime(\[str value\])</span></span>          | <span data-ttu-id="20ffe-2300">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2300">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="20ffe-2301">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2301">public str createdBy(\[str value\])</span></span>            | <span data-ttu-id="20ffe-2302">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2302">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="20ffe-2303">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2303">public Date creationDate(\[Date value\])</span></span>       | <span data-ttu-id="20ffe-2304">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2304">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="20ffe-2305">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2305">public str creationTime(\[str value\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="20ffe-2306">public int cueMax(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2306">public int cueMax(\[int value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="20ffe-2307">public str dataField(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2307">public str dataField(\[str value\])</span></span>            |                                                                                                                                           |
| <span data-ttu-id="20ffe-2308">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2308">public str label(\[str value\])</span></span>                | <span data-ttu-id="20ffe-2309">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2309">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="20ffe-2310">public str LabelId()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2310">public str LabelId()</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="20ffe-2311">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2311">public str menuItemName(\[str value\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="20ffe-2312">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2312">public str name(\[str value\])</span></span>                 | <span data-ttu-id="20ffe-2313">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2313">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="20ffe-2314">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2314">public Guid origin(\[Guid value\])</span></span>             |                                                                                                                                           |
| <span data-ttu-id="20ffe-2315">public str previewPartReference(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2315">public str previewPartReference(\[str value\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="20ffe-2316">public boolean showAlert(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2316">public boolean showAlert(\[boolean value\])</span></span>    |                                                                                                                                           |
| <span data-ttu-id="20ffe-2317">public int showAlertValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2317">public int showAlertValue(\[int value\])</span></span>       |                                                                                                                                           |
| <span data-ttu-id="20ffe-2318">public int showAlertWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2318">public int showAlertWhen(\[int value\])</span></span>        |                                                                                                                                           |
| <span data-ttu-id="20ffe-2319">public boolean showSum(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2319">public boolean showSum(\[boolean value\])</span></span>      |                                                                                                                                           |
| <span data-ttu-id="20ffe-2320">public str table(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2320">public str table(\[str value\])</span></span>                | <span data-ttu-id="20ffe-2321">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2321">Gets or sets the table ID associated with the object.</span></span>                                                                                     |
| <span data-ttu-id="20ffe-2322">public void new(str cueName)</span><span class="sxs-lookup"><span data-stu-id="20ffe-2322">public void new(str cueName)</span></span>                   | <span data-ttu-id="20ffe-2323">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2323">Initializes a new instance of the TreeNode class.</span></span>                                                                                         |

### <a name="method-changedby"></a><span data-ttu-id="20ffe-2324">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="20ffe-2324">Method changedBy</span></span>

<span data-ttu-id="20ffe-2325">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2325">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2326">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2326">Parameters</span></span>

<span data-ttu-id="20ffe-2327">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2327">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2328">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2328">Return Value</span></span>

<span data-ttu-id="20ffe-2329">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2329">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="20ffe-2330">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="20ffe-2330">Method changedDate</span></span>

<span data-ttu-id="20ffe-2331">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2331">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2332">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2332">Parameters</span></span>

<span data-ttu-id="20ffe-2333">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2333">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2334">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2334">Return Value</span></span>

<span data-ttu-id="20ffe-2335">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2335">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="20ffe-2336">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="20ffe-2336">Method changedTime</span></span>

<span data-ttu-id="20ffe-2337">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2337">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2338">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2338">Parameters</span></span>

<span data-ttu-id="20ffe-2339">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2339">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2340">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2340">Return Value</span></span>

<span data-ttu-id="20ffe-2341">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2341">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="20ffe-2342">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="20ffe-2342">Method createdBy</span></span>

<span data-ttu-id="20ffe-2343">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2343">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2344">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2344">Parameters</span></span>

<span data-ttu-id="20ffe-2345">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2345">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2346">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2346">Return Value</span></span>

<span data-ttu-id="20ffe-2347">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2347">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="20ffe-2348">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="20ffe-2348">Method creationDate</span></span>

<span data-ttu-id="20ffe-2349">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2349">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2350">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2350">Parameters</span></span>

<span data-ttu-id="20ffe-2351">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2351">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2352">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2352">Return Value</span></span>

<span data-ttu-id="20ffe-2353">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2353">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="20ffe-2354">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="20ffe-2354">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2355">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2355">Parameters</span></span>

<span data-ttu-id="20ffe-2356">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2356">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2357">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2357">Return Value</span></span>

### <a name="method-cuemax"></a><span data-ttu-id="20ffe-2358">メソッド cueMax</span><span class="sxs-lookup"><span data-stu-id="20ffe-2358">Method cueMax</span></span>

    public int cueMax([int value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2359">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2359">Parameters</span></span>

<span data-ttu-id="20ffe-2360">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2360">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2361">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2361">Return Value</span></span>

### <a name="method-datafield"></a><span data-ttu-id="20ffe-2362">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="20ffe-2362">Method dataField</span></span>

    public str dataField([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2363">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2363">Parameters</span></span>

<span data-ttu-id="20ffe-2364">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2364">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2365">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2365">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="20ffe-2366">メソッド label</span><span class="sxs-lookup"><span data-stu-id="20ffe-2366">Method label</span></span>

<span data-ttu-id="20ffe-2367">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2367">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2368">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2368">Parameters</span></span>

<span data-ttu-id="20ffe-2369">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2369">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2370">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2370">Return Value</span></span>

<span data-ttu-id="20ffe-2371">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2371">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-2372">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2372">Remarks</span></span>

<span data-ttu-id="20ffe-2373">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2373">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="20ffe-2374">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2374">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-labelid"></a><span data-ttu-id="20ffe-2375">メソッド LabelId</span><span class="sxs-lookup"><span data-stu-id="20ffe-2375">Method LabelId</span></span>

    public str LabelId()

#### <a name="return-value"></a><span data-ttu-id="20ffe-2376">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2376">Return Value</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="20ffe-2377">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="20ffe-2377">Method menuItemName</span></span>

    public str menuItemName([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2378">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2378">Parameters</span></span>

<span data-ttu-id="20ffe-2379">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2379">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2380">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2380">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="20ffe-2381">メソッド名</span><span class="sxs-lookup"><span data-stu-id="20ffe-2381">Method name</span></span>

<span data-ttu-id="20ffe-2382">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2382">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2383">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2383">Parameters</span></span>

<span data-ttu-id="20ffe-2384">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2384">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2385">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2385">Return Value</span></span>

<span data-ttu-id="20ffe-2386">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2386">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-2387">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2387">Remarks</span></span>

<span data-ttu-id="20ffe-2388">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2388">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="20ffe-2389">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2389">Begins with a letter.</span></span>
-   <span data-ttu-id="20ffe-2390">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2390">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="20ffe-2391">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2391">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="20ffe-2392">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2392">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="20ffe-2393">テーブルは、拡張データ型、基本列挙型、およびクラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2393">Tables cannot have the same name as other public objects, such as extended data types, base enumeration types, and classes.</span></span>

### <a name="method-origin"></a><span data-ttu-id="20ffe-2394">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="20ffe-2394">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2395">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2395">Parameters</span></span>

<span data-ttu-id="20ffe-2396">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2396">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2397">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2397">Return Value</span></span>

### <a name="method-previewpartreference"></a><span data-ttu-id="20ffe-2398">メソッド previewPartReference</span><span class="sxs-lookup"><span data-stu-id="20ffe-2398">Method previewPartReference</span></span>

    public str previewPartReference([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2399">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2399">Parameters</span></span>

<span data-ttu-id="20ffe-2400">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2400">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2401">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2401">Return Value</span></span>

### <a name="method-showalert"></a><span data-ttu-id="20ffe-2402">メソッド showAlert</span><span class="sxs-lookup"><span data-stu-id="20ffe-2402">Method showAlert</span></span>

    public boolean showAlert([boolean value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2403">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2403">Parameters</span></span>

<span data-ttu-id="20ffe-2404">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2404">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2405">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2405">Return Value</span></span>

### <a name="method-showalertvalue"></a><span data-ttu-id="20ffe-2406">メソッド showAlertValue</span><span class="sxs-lookup"><span data-stu-id="20ffe-2406">Method showAlertValue</span></span>

    public int showAlertValue([int value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2407">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2407">Parameters</span></span>

<span data-ttu-id="20ffe-2408">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2408">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2409">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2409">Return Value</span></span>

### <a name="method-showalertwhen"></a><span data-ttu-id="20ffe-2410">メソッド showAlertWhen</span><span class="sxs-lookup"><span data-stu-id="20ffe-2410">Method showAlertWhen</span></span>

    public int showAlertWhen([int value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2411">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2411">Parameters</span></span>

<span data-ttu-id="20ffe-2412">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2412">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2413">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2413">Return Value</span></span>

### <a name="method-showsum"></a><span data-ttu-id="20ffe-2414">メソッド showSum</span><span class="sxs-lookup"><span data-stu-id="20ffe-2414">Method showSum</span></span>

    public boolean showSum([boolean value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2415">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2415">Parameters</span></span>

<span data-ttu-id="20ffe-2416">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2416">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2417">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2417">Return Value</span></span>

### <a name="method-table"></a><span data-ttu-id="20ffe-2418">メソッド table</span><span class="sxs-lookup"><span data-stu-id="20ffe-2418">Method table</span></span>

<span data-ttu-id="20ffe-2419">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2419">Gets or sets the table ID associated with the object.</span></span>

    public str table([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2420">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2420">Parameters</span></span>

<span data-ttu-id="20ffe-2421">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2421">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2422">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2422">Return Value</span></span>

<span data-ttu-id="20ffe-2423">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2423">The current value of the table ID associated with the object.</span></span>

### <a name="method-new"></a><span data-ttu-id="20ffe-2424">メソッド new</span><span class="sxs-lookup"><span data-stu-id="20ffe-2424">Method new</span></span>

<span data-ttu-id="20ffe-2425">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2425">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str cueName)

#### <a name="parameters"></a><span data-ttu-id="20ffe-2426">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2426">Parameters</span></span>

<span data-ttu-id="20ffe-2427">cueName</span><span class="sxs-lookup"><span data-stu-id="20ffe-2427">cueName</span></span>  

## <a name="class-cuegroup"></a><span data-ttu-id="20ffe-2428">クラス CueGroup</span><span class="sxs-lookup"><span data-stu-id="20ffe-2428">Class CueGroup</span></span>
    class CueGroup extends TreeNode

### <a name="remarks"></a><span data-ttu-id="20ffe-2429">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2429">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-2430">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-2430">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="20ffe-2431">メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-2431">Methods</span></span>

| <span data-ttu-id="20ffe-2432">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-2432">Method</span></span>                                   | <span data-ttu-id="20ffe-2433">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-2433">Description</span></span>                                                                                                                                   |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ffe-2434">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2434">public str changedBy(\[str value\])</span></span>      | <span data-ttu-id="20ffe-2435">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2435">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="20ffe-2436">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2436">public Date changedDate(\[Date value\])</span></span>  | <span data-ttu-id="20ffe-2437">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2437">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="20ffe-2438">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2438">public str changedTime(\[str value\])</span></span>    | <span data-ttu-id="20ffe-2439">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2439">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="20ffe-2440">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2440">public str createdBy(\[str value\])</span></span>      | <span data-ttu-id="20ffe-2441">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2441">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="20ffe-2442">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2442">public Date creationDate(\[Date value\])</span></span> | <span data-ttu-id="20ffe-2443">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2443">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="20ffe-2444">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2444">public str creationTime(\[str value\])</span></span>   |                                                                                                                                               |
| <span data-ttu-id="20ffe-2445">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2445">public str label(\[str value\])</span></span>          | <span data-ttu-id="20ffe-2446">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2446">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="20ffe-2447">public str LabelId()</span><span class="sxs-lookup"><span data-stu-id="20ffe-2447">public str LabelId()</span></span>                     |                                                                                                                                               |
| <span data-ttu-id="20ffe-2448">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2448">public str name(\[str value\])</span></span>           | <span data-ttu-id="20ffe-2449">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2449">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="20ffe-2450">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2450">public Guid origin(\[Guid value\])</span></span>       |                                                                                                                                               |
| <span data-ttu-id="20ffe-2451">public void new(str cueGroupName)</span><span class="sxs-lookup"><span data-stu-id="20ffe-2451">public void new(str cueGroupName)</span></span>        | <span data-ttu-id="20ffe-2452">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2452">Initializes a new instance of the TreeNode class.</span></span>                                                                                             |

### <a name="method-changedby"></a><span data-ttu-id="20ffe-2453">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="20ffe-2453">Method changedBy</span></span>

<span data-ttu-id="20ffe-2454">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2454">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2455">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2455">Parameters</span></span>

<span data-ttu-id="20ffe-2456">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2456">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2457">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2457">Return Value</span></span>

<span data-ttu-id="20ffe-2458">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2458">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="20ffe-2459">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="20ffe-2459">Method changedDate</span></span>

<span data-ttu-id="20ffe-2460">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2460">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2461">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2461">Parameters</span></span>

<span data-ttu-id="20ffe-2462">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2462">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2463">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2463">Return Value</span></span>

<span data-ttu-id="20ffe-2464">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2464">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="20ffe-2465">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="20ffe-2465">Method changedTime</span></span>

<span data-ttu-id="20ffe-2466">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2466">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2467">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2467">Parameters</span></span>

<span data-ttu-id="20ffe-2468">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2468">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2469">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2469">Return Value</span></span>

<span data-ttu-id="20ffe-2470">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2470">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="20ffe-2471">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="20ffe-2471">Method createdBy</span></span>

<span data-ttu-id="20ffe-2472">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2472">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2473">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2473">Parameters</span></span>

<span data-ttu-id="20ffe-2474">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2474">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2475">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2475">Return Value</span></span>

<span data-ttu-id="20ffe-2476">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2476">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="20ffe-2477">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="20ffe-2477">Method creationDate</span></span>

<span data-ttu-id="20ffe-2478">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2478">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2479">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2479">Parameters</span></span>

<span data-ttu-id="20ffe-2480">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2480">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2481">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2481">Return Value</span></span>

<span data-ttu-id="20ffe-2482">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2482">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="20ffe-2483">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="20ffe-2483">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2484">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2484">Parameters</span></span>

<span data-ttu-id="20ffe-2485">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2485">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2486">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2486">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="20ffe-2487">メソッド label</span><span class="sxs-lookup"><span data-stu-id="20ffe-2487">Method label</span></span>

<span data-ttu-id="20ffe-2488">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2488">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2489">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2489">Parameters</span></span>

<span data-ttu-id="20ffe-2490">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2490">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2491">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2491">Return Value</span></span>

<span data-ttu-id="20ffe-2492">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2492">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-2493">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2493">Remarks</span></span>

<span data-ttu-id="20ffe-2494">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2494">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="20ffe-2495">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2495">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-labelid"></a><span data-ttu-id="20ffe-2496">メソッド LabelId</span><span class="sxs-lookup"><span data-stu-id="20ffe-2496">Method LabelId</span></span>

    public str LabelId()

#### <a name="return-value"></a><span data-ttu-id="20ffe-2497">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2497">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="20ffe-2498">メソッド名</span><span class="sxs-lookup"><span data-stu-id="20ffe-2498">Method name</span></span>

<span data-ttu-id="20ffe-2499">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2499">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2500">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2500">Parameters</span></span>

<span data-ttu-id="20ffe-2501">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2501">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2502">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2502">Return Value</span></span>

<span data-ttu-id="20ffe-2503">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2503">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-2504">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2504">Remarks</span></span>

<span data-ttu-id="20ffe-2505">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2505">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="20ffe-2506">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2506">Begins with a letter.</span></span>
-   <span data-ttu-id="20ffe-2507">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2507">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="20ffe-2508">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2508">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="20ffe-2509">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2509">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="20ffe-2510">テーブルは、拡張データ型、基本列挙型、およびクラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2510">Tables cannot have the same name as other public objects, such as extended data types, base enumeration types, and classes.</span></span>

### <a name="method-origin"></a><span data-ttu-id="20ffe-2511">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="20ffe-2511">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2512">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2512">Parameters</span></span>

<span data-ttu-id="20ffe-2513">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2513">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2514">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2514">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="20ffe-2515">メソッド new</span><span class="sxs-lookup"><span data-stu-id="20ffe-2515">Method new</span></span>

<span data-ttu-id="20ffe-2516">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2516">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str cueGroupName)

#### <a name="parameters"></a><span data-ttu-id="20ffe-2517">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2517">Parameters</span></span>

<span data-ttu-id="20ffe-2518">cueGroupName</span><span class="sxs-lookup"><span data-stu-id="20ffe-2518">cueGroupName</span></span>  

## <a name="class-cuereference"></a><span data-ttu-id="20ffe-2519">クラス CueReference</span><span class="sxs-lookup"><span data-stu-id="20ffe-2519">Class CueReference</span></span>
    class CueReference extends TreeNode

### <a name="remarks"></a><span data-ttu-id="20ffe-2520">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2520">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="20ffe-2521">例</span><span class="sxs-lookup"><span data-stu-id="20ffe-2521">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="20ffe-2522">メソッド</span><span class="sxs-lookup"><span data-stu-id="20ffe-2522">Methods</span></span>

| <span data-ttu-id="20ffe-2523">方法</span><span class="sxs-lookup"><span data-stu-id="20ffe-2523">Method</span></span>                                | <span data-ttu-id="20ffe-2524">説明</span><span class="sxs-lookup"><span data-stu-id="20ffe-2524">Description</span></span>                                                                                                                       |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ffe-2525">public str cue(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2525">public str cue(\[str value\])</span></span>         |                                                                                                                                   |
| <span data-ttu-id="20ffe-2526">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20ffe-2526">public str name(\[str value\])</span></span>        | <span data-ttu-id="20ffe-2527">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2527">Gets or sets the name used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="20ffe-2528">public void new(str cueReferenceName)</span><span class="sxs-lookup"><span data-stu-id="20ffe-2528">public void new(str cueReferenceName)</span></span> | <span data-ttu-id="20ffe-2529">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2529">Initializes a new instance of the TreeNode class.</span></span>                                                                                 |

### <a name="method-cue"></a><span data-ttu-id="20ffe-2530">メソッド cue</span><span class="sxs-lookup"><span data-stu-id="20ffe-2530">Method cue</span></span>

    public str cue([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2531">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2531">Parameters</span></span>

<span data-ttu-id="20ffe-2532">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2532">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2533">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2533">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="20ffe-2534">メソッド名</span><span class="sxs-lookup"><span data-stu-id="20ffe-2534">Method name</span></span>

<span data-ttu-id="20ffe-2535">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2535">Gets or sets the name used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="20ffe-2536">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2536">Parameters</span></span>

<span data-ttu-id="20ffe-2537">値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2537">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="20ffe-2538">戻り値</span><span class="sxs-lookup"><span data-stu-id="20ffe-2538">Return Value</span></span>

<span data-ttu-id="20ffe-2539">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2539">The name used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="20ffe-2540">備考</span><span class="sxs-lookup"><span data-stu-id="20ffe-2540">Remarks</span></span>

<span data-ttu-id="20ffe-2541">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2541">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="20ffe-2542">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2542">Begins with a letter.</span></span>
-   <span data-ttu-id="20ffe-2543">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2543">Does not exceed 250 characters.</span></span>
-   <span data-ttu-id="20ffe-2544">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2544">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="20ffe-2545">句読点やスペースを含めないでください。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2545">Does not include punctuation or spaces.</span></span>
-   <span data-ttu-id="20ffe-2546">テーブルは、拡張データ型、基本列挙型、クラス、他のパブリックオブジェクトなど、他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2546">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, classes, and other public objects.</span></span>

### <a name="method-new"></a><span data-ttu-id="20ffe-2547">メソッド new</span><span class="sxs-lookup"><span data-stu-id="20ffe-2547">Method new</span></span>

<span data-ttu-id="20ffe-2548">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2548">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str cueReferenceName)

#### <a name="parameters"></a><span data-ttu-id="20ffe-2549">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20ffe-2549">Parameters</span></span>

<span data-ttu-id="20ffe-2550">cueReferenceName</span><span class="sxs-lookup"><span data-stu-id="20ffe-2550">cueReferenceName</span></span>  
<span data-ttu-id="20ffe-2551">このフォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="20ffe-2551">The name to use to identify this form, report, table, query, or other application object.</span></span>





