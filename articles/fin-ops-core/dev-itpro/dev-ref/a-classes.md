---
title: A クラス
description: 文字 A で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 47561
ms.assetid: 03d9d906-d683-47b4-8488-795173db2125
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfe183ba6bff03189d1d5ef4465a43059a24be2f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191618"
---
# <a name="a-classes"></a><span data-ttu-id="ae9cf-103">A クラス</span><span class="sxs-lookup"><span data-stu-id="ae9cf-103">A classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae9cf-104">文字 A で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-104">System API classes that start with the letter A.</span></span>

<a name="class-absolutefieldbinding"></a><span data-ttu-id="ae9cf-105">クラス AbsoluteFieldBinding</span><span class="sxs-lookup"><span data-stu-id="ae9cf-105">Class AbsoluteFieldBinding</span></span>
--------------------------

    class AbsoluteFieldBinding extends FieldBinding

### <a name="remarks"></a><span data-ttu-id="ae9cf-106">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-106">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="ae9cf-107">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-107">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="ae9cf-108">方法</span><span class="sxs-lookup"><span data-stu-id="ae9cf-108">Methods</span></span>

| <span data-ttu-id="ae9cf-109">方法</span><span class="sxs-lookup"><span data-stu-id="ae9cf-109">Method</span></span>                                                                            | <span data-ttu-id="ae9cf-110">説明</span><span class="sxs-lookup"><span data-stu-id="ae9cf-110">Description</span></span>                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="ae9cf-111">::public static AbsoluteFieldBinding construct(str fieldName, str tableName)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-111">::public static AbsoluteFieldBinding construct(str fieldName, str tableName)</span></span>      |                                                               |
| <span data-ttu-id="ae9cf-112">::public static AbsoluteFieldBinding create(container packedAbsoluteFieldBinding)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-112">::public static AbsoluteFieldBinding create(container packedAbsoluteFieldBinding)</span></span> |                                                               |
| <span data-ttu-id="ae9cf-113">private void new()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-113">private void new()</span></span>                                                                | <span data-ttu-id="ae9cf-114">AbsoluteFieldBinding クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-114">Initializes a new instance of the AbsoluteFieldBinding class.</span></span> |

### <a name="method-construct"></a><span data-ttu-id="ae9cf-115">メソッド construct</span><span class="sxs-lookup"><span data-stu-id="ae9cf-115">Method construct</span></span>

    public static AbsoluteFieldBinding construct(str fieldName, str tableName)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-116">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-116">Parameters</span></span>

<span data-ttu-id="ae9cf-117">fieldName</span><span class="sxs-lookup"><span data-stu-id="ae9cf-117">fieldName</span></span>  

<!-- -->

<span data-ttu-id="ae9cf-118">tableName</span><span class="sxs-lookup"><span data-stu-id="ae9cf-118">tableName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="ae9cf-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-119">Return Value</span></span>

### <a name="method-create"></a><span data-ttu-id="ae9cf-120">メソッド create</span><span class="sxs-lookup"><span data-stu-id="ae9cf-120">Method create</span></span>

    public static AbsoluteFieldBinding create(container packedAbsoluteFieldBinding)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-121">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-121">Parameters</span></span>

<span data-ttu-id="ae9cf-122">packedAbsoluteFieldBinding</span><span class="sxs-lookup"><span data-stu-id="ae9cf-122">packedAbsoluteFieldBinding</span></span>  

#### <a name="return-value"></a><span data-ttu-id="ae9cf-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-123">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="ae9cf-124">メソッド new</span><span class="sxs-lookup"><span data-stu-id="ae9cf-124">Method new</span></span>

<span data-ttu-id="ae9cf-125">AbsoluteFieldBinding クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-125">Initializes a new instance of the AbsoluteFieldBinding class.</span></span>

    private void new()

## <a name="class-adobject"></a><span data-ttu-id="ae9cf-126">クラス AdObject</span><span class="sxs-lookup"><span data-stu-id="ae9cf-126">Class AdObject</span></span>
    class AdObject extends Object

### <a name="remarks"></a><span data-ttu-id="ae9cf-127">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-127">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="ae9cf-128">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-128">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="ae9cf-129">メソッド</span><span class="sxs-lookup"><span data-stu-id="ae9cf-129">Methods</span></span>

| <span data-ttu-id="ae9cf-130">方法</span><span class="sxs-lookup"><span data-stu-id="ae9cf-130">Method</span></span>                             | <span data-ttu-id="ae9cf-131">説明</span><span class="sxs-lookup"><span data-stu-id="ae9cf-131">Description</span></span>                                     |
|------------------------------------|-------------------------------------------------|
| <span data-ttu-id="ae9cf-132">public boolean found()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-132">public boolean found()</span></span>             |                                                 |
| <span data-ttu-id="ae9cf-133">public str getValue(str attribute)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-133">public str getValue(str attribute)</span></span> |                                                 |
| <span data-ttu-id="ae9cf-134">public void new(str osUserName)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-134">public void new(str osUserName)</span></span>    | <span data-ttu-id="ae9cf-135">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-135">Initializes a new instance of the Object class.</span></span> |

### <a name="method-found"></a><span data-ttu-id="ae9cf-136">メソッド found</span><span class="sxs-lookup"><span data-stu-id="ae9cf-136">Method found</span></span>

    public boolean found()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-137">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-137">Return Value</span></span>

### <a name="method-getvalue"></a><span data-ttu-id="ae9cf-138">メソッド getValue</span><span class="sxs-lookup"><span data-stu-id="ae9cf-138">Method getValue</span></span>

    public str getValue(str attribute)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-139">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-139">Parameters</span></span>

<span data-ttu-id="ae9cf-140">属性</span><span class="sxs-lookup"><span data-stu-id="ae9cf-140">attribute</span></span>  

#### <a name="return-value"></a><span data-ttu-id="ae9cf-141">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-141">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="ae9cf-142">メソッド new</span><span class="sxs-lookup"><span data-stu-id="ae9cf-142">Method new</span></span>

<span data-ttu-id="ae9cf-143">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-143">Initializes a new instance of the Object class.</span></span>

    public void new(str osUserName)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-144">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-144">Parameters</span></span>

<span data-ttu-id="ae9cf-145">osUserName</span><span class="sxs-lookup"><span data-stu-id="ae9cf-145">osUserName</span></span>  

## <a name="class-allowencryptionkeyretrievalpermission"></a><span data-ttu-id="ae9cf-146">クラス AllowEncryptionKeyRetrievalPermission</span><span class="sxs-lookup"><span data-stu-id="ae9cf-146">Class AllowEncryptionKeyRetrievalPermission</span></span>
    class AllowEncryptionKeyRetrievalPermission extends CodeAccessPermission

### <a name="remarks"></a><span data-ttu-id="ae9cf-147">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-147">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="ae9cf-148">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-148">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="ae9cf-149">メソッド</span><span class="sxs-lookup"><span data-stu-id="ae9cf-149">Methods</span></span>

| <span data-ttu-id="ae9cf-150">方法</span><span class="sxs-lookup"><span data-stu-id="ae9cf-150">Method</span></span>                                                 | <span data-ttu-id="ae9cf-151">説明</span><span class="sxs-lookup"><span data-stu-id="ae9cf-151">Description</span></span>                                                                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae9cf-152">public CodeAccessPermission copy()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-152">public CodeAccessPermission copy()</span></span>                     | <span data-ttu-id="ae9cf-153">アクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-153">Creates and returns a copy of a permission class object.</span></span>                                                                  |
| <span data-ttu-id="ae9cf-154">public boolean isSubsetOf(CodeAccessPermission target)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-154">public boolean isSubsetOf(CodeAccessPermission target)</span></span> | <span data-ttu-id="ae9cf-155">現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-155">Determines whether a current permission is a subset of the specified permission when it is overridden by a derived class.</span></span> |
| <span data-ttu-id="ae9cf-156">public void new()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-156">public void new()</span></span>                                      | <span data-ttu-id="ae9cf-157">AllowEncryptionKeyRetrievalPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-157">Initializes a new instance of the AllowEncryptionKeyRetrievalPermission class.</span></span>                                            |

### <a name="method-copy"></a><span data-ttu-id="ae9cf-158">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="ae9cf-158">Method copy</span></span>

<span data-ttu-id="ae9cf-159">アクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-159">Creates and returns a copy of a permission class object.</span></span>

    public CodeAccessPermission copy()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-160">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-160">Return Value</span></span>

<span data-ttu-id="ae9cf-161">現在の派生クラスオブジェクトのコピーです。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-161">A copy of the derived class object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-162">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-162">Remarks</span></span>

<span data-ttu-id="ae9cf-163">API のセキュリティをさらに強化するプロセスの一部として、このメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-163">You can override this method as part of the process of making an API more secure.</span></span> <span data-ttu-id="ae9cf-164">詳細については、「サーバー層で実行する API の保護」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-164">For more information, see ‘Securing an API that Executes on the Server Tier.’</span></span>

### <a name="method-issubsetof"></a><span data-ttu-id="ae9cf-165">メソッド isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="ae9cf-165">Method isSubsetOf</span></span>

<span data-ttu-id="ae9cf-166">現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-166">Determines whether a current permission is a subset of the specified permission when it is overridden by a derived class.</span></span>

    public boolean isSubsetOf(CodeAccessPermission target)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-167">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-167">Parameters</span></span>

<span data-ttu-id="ae9cf-168">target</span><span class="sxs-lookup"><span data-stu-id="ae9cf-168">target</span></span>  
<span data-ttu-id="ae9cf-169">CodeAccessPermission クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-169">A CodeAccessPermission class object.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ae9cf-170">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-170">Return Value</span></span>

<span data-ttu-id="ae9cf-171">現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-171">true if a current permission is a subset of a specified permission; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-172">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-172">Remarks</span></span>

<span data-ttu-id="ae9cf-173">API のセキュリティをさらに強化するプロセスの一部として、メソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-173">You can override the method as part of the process of making an API more secure.</span></span> <span data-ttu-id="ae9cf-174">詳細については、「サーバー層で実行する API の保護」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-174">For more information, see ‘Securing an API that Executes on the Server Tier.’</span></span>

### <a name="method-new"></a><span data-ttu-id="ae9cf-175">メソッド new</span><span class="sxs-lookup"><span data-stu-id="ae9cf-175">Method new</span></span>

<span data-ttu-id="ae9cf-176">AllowEncryptionKeyRetrievalPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-176">Initializes a new instance of the AllowEncryptionKeyRetrievalPermission class.</span></span>

    public void new()

## <a name="class-aosloadgen"></a><span data-ttu-id="ae9cf-177">クラス AOSLoadGen</span><span class="sxs-lookup"><span data-stu-id="ae9cf-177">Class AOSLoadGen</span></span>
    class AOSLoadGen extends Object

### <a name="remarks"></a><span data-ttu-id="ae9cf-178">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-178">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="ae9cf-179">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-179">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="ae9cf-180">メソッド</span><span class="sxs-lookup"><span data-stu-id="ae9cf-180">Methods</span></span>

| <span data-ttu-id="ae9cf-181">方法</span><span class="sxs-lookup"><span data-stu-id="ae9cf-181">Method</span></span>                                                     | <span data-ttu-id="ae9cf-182">説明</span><span class="sxs-lookup"><span data-stu-id="ae9cf-182">Description</span></span>                                  |
|------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="ae9cf-183">public boolean spawnClass(ClassId classId, str parm)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-183">public boolean spawnClass(ClassId classId, str parm)</span></span>       |                                              |
| <span data-ttu-id="ae9cf-184">public boolean spawnJob(UtilElementName jobName, str parm)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-184">public boolean spawnJob(UtilElementName jobName, str parm)</span></span> |                                              |
| <span data-ttu-id="ae9cf-185">public void new(\[UserId user\], \[ClassId infoClass\])</span><span class="sxs-lookup"><span data-stu-id="ae9cf-185">public void new(\[UserId user\], \[ClassId infoClass\])</span></span>    | <span data-ttu-id="ae9cf-186">AOSLoadGen クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-186">Creates an instance of the AOSLoadGen class.</span></span> |

### <a name="method-spawnclass"></a><span data-ttu-id="ae9cf-187">メソッド spawnClass</span><span class="sxs-lookup"><span data-stu-id="ae9cf-187">Method spawnClass</span></span>

    public boolean spawnClass(ClassId classId, str parm)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-188">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-188">Parameters</span></span>

<span data-ttu-id="ae9cf-189">classId</span><span class="sxs-lookup"><span data-stu-id="ae9cf-189">classId</span></span>  

<!-- -->

<span data-ttu-id="ae9cf-190">parm</span><span class="sxs-lookup"><span data-stu-id="ae9cf-190">parm</span></span>  

#### <a name="return-value"></a><span data-ttu-id="ae9cf-191">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-191">Return Value</span></span>

### <a name="method-spawnjob"></a><span data-ttu-id="ae9cf-192">メソッド spawnJob</span><span class="sxs-lookup"><span data-stu-id="ae9cf-192">Method spawnJob</span></span>

    public boolean spawnJob(UtilElementName jobName, str parm)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-193">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-193">Parameters</span></span>

<span data-ttu-id="ae9cf-194">jobName</span><span class="sxs-lookup"><span data-stu-id="ae9cf-194">jobName</span></span>  

<!-- -->

<span data-ttu-id="ae9cf-195">parm</span><span class="sxs-lookup"><span data-stu-id="ae9cf-195">parm</span></span>  

#### <a name="return-value"></a><span data-ttu-id="ae9cf-196">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-196">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="ae9cf-197">メソッド new</span><span class="sxs-lookup"><span data-stu-id="ae9cf-197">Method new</span></span>

<span data-ttu-id="ae9cf-198">AOSLoadGen クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-198">Creates an instance of the AOSLoadGen class.</span></span>

    public void new([UserId user], [ClassId infoClass])

#### <a name="parameters"></a><span data-ttu-id="ae9cf-199">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-199">Parameters</span></span>

<span data-ttu-id="ae9cf-200">ユーザー</span><span class="sxs-lookup"><span data-stu-id="ae9cf-200">user</span></span>  
<span data-ttu-id="ae9cf-201">AOSLoadGen クラスのインスタンスを作成するために使用される情報クラス。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-201">The information class that is used to create the instance of the AOSLoadGen class.</span></span> <span data-ttu-id="ae9cf-202">既定値は情報です。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-202">The default value is info.</span></span>

<!-- -->

<span data-ttu-id="ae9cf-203">infoClass</span><span class="sxs-lookup"><span data-stu-id="ae9cf-203">infoClass</span></span>  
<span data-ttu-id="ae9cf-204">AOSLoadGen クラスのインスタンスを作成するために使用される情報クラス。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-204">The information class that is used to create the instance of the AOSLoadGen class.</span></span> <span data-ttu-id="ae9cf-205">既定値は情報です。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-205">The default value is info.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-206">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-206">Remarks</span></span>

<span data-ttu-id="ae9cf-207">新しいメソッドへの入力を制御することは、セキュリティ上のリスクとなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-207">Control of the input to the new method could be a security risk.</span></span> <span data-ttu-id="ae9cf-208">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-208">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="ae9cf-209">サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-209">Calls to this method on the server require permission from the ExecutePermission class.</span></span> <span data-ttu-id="ae9cf-210">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-210">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

## <a name="class-aossessioninfo"></a><span data-ttu-id="ae9cf-211">クラス AOSSessionInfo</span><span class="sxs-lookup"><span data-stu-id="ae9cf-211">Class AOSSessionInfo</span></span>
    class AOSSessionInfo extends Object

<span data-ttu-id="ae9cf-212">AOSSessionInfo クラスは、Application Object Server (AOS) のセッションに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-212">The AOSSessionInfo class is used to provide information about a session for the Application Object Server (AOS).</span></span>

### <a name="remarks"></a><span data-ttu-id="ae9cf-213">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-213">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="ae9cf-214">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-214">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="ae9cf-215">メソッド</span><span class="sxs-lookup"><span data-stu-id="ae9cf-215">Methods</span></span>

| <span data-ttu-id="ae9cf-216">方法</span><span class="sxs-lookup"><span data-stu-id="ae9cf-216">Method</span></span>                             | <span data-ttu-id="ae9cf-217">説明</span><span class="sxs-lookup"><span data-stu-id="ae9cf-217">Description</span></span>                                                               |
|------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="ae9cf-218">public AOSClientMode clientMode()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-218">public AOSClientMode clientMode()</span></span>  | <span data-ttu-id="ae9cf-219">AOS セッションのクライアント モードを返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-219">Returns the client mode for the AOS session.</span></span>                              |
| <span data-ttu-id="ae9cf-220">public int cpuTime()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-220">public int cpuTime()</span></span>               | <span data-ttu-id="ae9cf-221">CPU が AOS セッションに使用するミリ秒数を返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-221">Returns the number of milliseconds that the CPU uses for the AOS session.</span></span> |
| <span data-ttu-id="ae9cf-222">public int idleTicks()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-222">public int idleTicks()</span></span>             | <span data-ttu-id="ae9cf-223">AOS との最後の通信以降のミリ秒数を返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-223">Returns the number of milliseconds since the last communication with AOS.</span></span> |
| <span data-ttu-id="ae9cf-224">public int sessionId()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-224">public int sessionId()</span></span>             | <span data-ttu-id="ae9cf-225">AOS セッションの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-225">Returns the ID of the AOS session.</span></span>                                        |
| <span data-ttu-id="ae9cf-226">public void new(\[int sessionId\])</span><span class="sxs-lookup"><span data-stu-id="ae9cf-226">public void new(\[int sessionId\])</span></span> | <span data-ttu-id="ae9cf-227">AOSSessionInfo クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-227">Creates an instance of the AOSSessionInfo class.</span></span>                          |

### <a name="method-clientmode"></a><span data-ttu-id="ae9cf-228">メソッド clientMode</span><span class="sxs-lookup"><span data-stu-id="ae9cf-228">Method clientMode</span></span>

<span data-ttu-id="ae9cf-229">AOS セッションのクライアント モードを返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-229">Returns the client mode for the AOS session.</span></span>

    public AOSClientMode clientMode()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-230">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-230">Return Value</span></span>

<span data-ttu-id="ae9cf-231">AOS セッションのクライアント モード。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-231">The client mode for the AOS session.</span></span>

### <a name="method-cputime"></a><span data-ttu-id="ae9cf-232">メソッド cpuTime</span><span class="sxs-lookup"><span data-stu-id="ae9cf-232">Method cpuTime</span></span>

<span data-ttu-id="ae9cf-233">CPU が AOS セッションに使用するミリ秒数を返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-233">Returns the number of milliseconds that the CPU uses for the AOS session.</span></span>

    public int cpuTime()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-234">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-234">Return Value</span></span>

<span data-ttu-id="ae9cf-235">CPU が AOS セッションに使用するミリ秒数。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-235">The number of milliseconds that the CPU uses for the AOS session.</span></span>

### <a name="method-idleticks"></a><span data-ttu-id="ae9cf-236">メソッド idleTicks</span><span class="sxs-lookup"><span data-stu-id="ae9cf-236">Method idleTicks</span></span>

<span data-ttu-id="ae9cf-237">AOS との最後の通信以降のミリ秒数を返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-237">Returns the number of milliseconds since the last communication with AOS.</span></span>

    public int idleTicks()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-238">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-238">Return Value</span></span>

<span data-ttu-id="ae9cf-239">AOS との最後の通信以降のミリ秒数。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-239">The number of milliseconds since the last communication with AOS.</span></span>

### <a name="method-sessionid"></a><span data-ttu-id="ae9cf-240">メソッド sessionId</span><span class="sxs-lookup"><span data-stu-id="ae9cf-240">Method sessionId</span></span>

<span data-ttu-id="ae9cf-241">AOS セッションの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-241">Returns the ID of the AOS session.</span></span>

    public int sessionId()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-242">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-242">Return Value</span></span>

<span data-ttu-id="ae9cf-243">AOS セッションの ID。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-243">The ID of the AOS session.</span></span>

### <a name="method-new"></a><span data-ttu-id="ae9cf-244">メソッド new</span><span class="sxs-lookup"><span data-stu-id="ae9cf-244">Method new</span></span>

<span data-ttu-id="ae9cf-245">AOSSessionInfo クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-245">Creates an instance of the AOSSessionInfo class.</span></span>

    public void new([int sessionId])

#### <a name="parameters"></a><span data-ttu-id="ae9cf-246">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-246">Parameters</span></span>

<span data-ttu-id="ae9cf-247">sessionId</span><span class="sxs-lookup"><span data-stu-id="ae9cf-247">sessionId</span></span>  
<span data-ttu-id="ae9cf-248">AOSSessionInfo クラスのインスタンスを作成するために使用されるセッション ID。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-248">The session ID that is used to create the instance of the AOSSessionInfo class.</span></span> <span data-ttu-id="ae9cf-249">セッション ID が指定されていない場合、現在のセッションが使用されます; 省略。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-249">If a session ID is not specified, the current session is used; optional.</span></span>

## <a name="class-aottablefieldlist"></a><span data-ttu-id="ae9cf-250">クラス AOTTableFieldList</span><span class="sxs-lookup"><span data-stu-id="ae9cf-250">Class AOTTableFieldList</span></span>
    class AOTTableFieldList extends TreeNode

<span data-ttu-id="ae9cf-251">AOTTableFieldList クラスは、テーブルのフィールド ノードを表し、フィールドをテーブルに追加するためにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-251">The AOTTableFieldList class represents the Fields node of a table and is also used to add fields to a table.</span></span>

### <a name="remarks"></a><span data-ttu-id="ae9cf-252">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-252">Remarks</span></span>

<span data-ttu-id="ae9cf-253">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-253">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="ae9cf-254">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-254">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span> <span data-ttu-id="ae9cf-255">開発者は、他の方法を使用してノードに関する一般的な情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-255">The developer can obtain general information on the node by using other methods.</span></span>

### <a name="examples"></a><span data-ttu-id="ae9cf-256">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-256">Examples</span></span>

<span data-ttu-id="ae9cf-257">次の例では、列挙型のフィールドを TutorialJournalName テーブルに追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-257">The following example adds a field of the enum type to the TutorialJournalName table.</span></span>

    { 
        AOTTableFieldList tfl = infolog.findNode( 
            '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 

         if (!tfl.AOTFindChild('NewEnum')) 
         { 
             tfl.addEnum('NewEnum');  // Adds the field NewEnum. 
         } 
    }

### <a name="methods"></a><span data-ttu-id="ae9cf-258">メソッド</span><span class="sxs-lookup"><span data-stu-id="ae9cf-258">Methods</span></span>

| <span data-ttu-id="ae9cf-259">方法</span><span class="sxs-lookup"><span data-stu-id="ae9cf-259">Method</span></span>                             | <span data-ttu-id="ae9cf-260">説明</span><span class="sxs-lookup"><span data-stu-id="ae9cf-260">Description</span></span>                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ae9cf-261">public void addInteger(str name)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-261">public void addInteger(str name)</span></span>   | <span data-ttu-id="ae9cf-262">現在のテーブルのフィールドのリストに整数型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-262">Adds a new field of the integer type to the list of fields for the current table.</span></span>   |
| <span data-ttu-id="ae9cf-263">public void addGuid(str name)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-263">public void addGuid(str name)</span></span>      |                                                                                     |
| <span data-ttu-id="ae9cf-264">public void addContainer(str name)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-264">public void addContainer(str name)</span></span> | <span data-ttu-id="ae9cf-265">現在のテーブルのフィールドのリストにコンテナー型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-265">Adds a new field of the container type to the list of fields for the current table.</span></span> |
| <span data-ttu-id="ae9cf-266">public void addInt64(str name)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-266">public void addInt64(str name)</span></span>     |                                                                                     |
| <span data-ttu-id="ae9cf-267">public void addDateTime(str name)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-267">public void addDateTime(str name)</span></span>  |                                                                                     |
| <span data-ttu-id="ae9cf-268">public void addDate(str name)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-268">public void addDate(str name)</span></span>      | <span data-ttu-id="ae9cf-269">現在のテーブルのフィールドのリストに日付型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-269">Adds a new field of the date type to the list of fields for the current table.</span></span>      |
| <span data-ttu-id="ae9cf-270">public void addString(str name)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-270">public void addString(str name)</span></span>    | <span data-ttu-id="ae9cf-271">現在のテーブルのフィールドのリストに文字列型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-271">Adds a new field of the string type to the list of fields for the current table.</span></span>    |
| <span data-ttu-id="ae9cf-272">public void addReal(str name)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-272">public void addReal(str name)</span></span>      | <span data-ttu-id="ae9cf-273">現在のテーブルのフィールドのリストに実数型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-273">Adds a new field of the real type to the list of fields for the current table.</span></span>      |
| <span data-ttu-id="ae9cf-274">public void addTime(str name)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-274">public void addTime(str name)</span></span>      | <span data-ttu-id="ae9cf-275">現在のテーブルのフィールドのリストに時刻タイプの新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-275">Adds a new field of the time type to the list of fields for the current table.</span></span>      |
| <span data-ttu-id="ae9cf-276">public void addEnum(str name)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-276">public void addEnum(str name)</span></span>      | <span data-ttu-id="ae9cf-277">現在のテーブルのフィールドのリストに列挙型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-277">Adds a new field of the enum type to the list of fields for the current table.</span></span>      |

### <a name="method-addinteger"></a><span data-ttu-id="ae9cf-278">メソッド addInteger</span><span class="sxs-lookup"><span data-stu-id="ae9cf-278">Method addInteger</span></span>

<span data-ttu-id="ae9cf-279">現在のテーブルのフィールドのリストに整数型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-279">Adds a new field of the integer type to the list of fields for the current table.</span></span>

    public void addInteger(str name)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-280">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-280">Parameters</span></span>

<span data-ttu-id="ae9cf-281">名前</span><span class="sxs-lookup"><span data-stu-id="ae9cf-281">name</span></span>  
<span data-ttu-id="ae9cf-282">追加するフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-282">The name of the field to add.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-283">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-283">Remarks</span></span>

<span data-ttu-id="ae9cf-284">指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-284">If the supplied name coincides with an existing field in the field list, an integer is appended to the name of the new field to make the field name unique.</span></span> <span data-ttu-id="ae9cf-285">開発者は名前が予約語ではないことを確認する必要があります。予約語が指定されている場合、メソッドはエラーをスローしません。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-285">The developer must make sure that the name is not a reserved word; the method will not throw an error if a reserved word is specified.</span></span> <span data-ttu-id="ae9cf-286">AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-286">You can use the AOTfindChild method to determine whether a field name is already being used.</span></span>

#### <a name="examples"></a><span data-ttu-id="ae9cf-287">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-287">Examples</span></span>

<span data-ttu-id="ae9cf-288">次のコード例は、整数型である、NewInteger フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-288">The following code example adds the NewInteger field, which is of the integer type, to the list of fields for the TutorialJournalName table.</span></span>

    AOTTableFieldList tfl = infolog.findNode( 
        '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
    if (!tfl.AOTFindChild('NewInteger')) 
    { 
        tfl.addInteger('NewInteger'); 
    }

### <a name="method-addguid"></a><span data-ttu-id="ae9cf-289">メソッド addGuid</span><span class="sxs-lookup"><span data-stu-id="ae9cf-289">Method addGuid</span></span>

    public void addGuid(str name)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-290">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-290">Parameters</span></span>

<span data-ttu-id="ae9cf-291">名前</span><span class="sxs-lookup"><span data-stu-id="ae9cf-291">name</span></span>  

### <a name="method-addcontainer"></a><span data-ttu-id="ae9cf-292">メソッド addContainer</span><span class="sxs-lookup"><span data-stu-id="ae9cf-292">Method addContainer</span></span>

<span data-ttu-id="ae9cf-293">現在のテーブルのフィールドのリストにコンテナー型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-293">Adds a new field of the container type to the list of fields for the current table.</span></span>

    public void addContainer(str name)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-294">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-294">Parameters</span></span>

<span data-ttu-id="ae9cf-295">名前</span><span class="sxs-lookup"><span data-stu-id="ae9cf-295">name</span></span>  
<span data-ttu-id="ae9cf-296">追加するフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-296">The name of the field to add.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-297">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-297">Remarks</span></span>

<span data-ttu-id="ae9cf-298">指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-298">If the supplied name coincides with an existing field in the field list, an integer is appended to the name of the new field to make the field name unique.</span></span> <span data-ttu-id="ae9cf-299">開発者は名前が予約語ではないことを確認する必要があります。予約語が指定されている場合、メソッドはエラーをスローしません。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-299">The developer must make sure that the name is not a reserved word; the method will not throw an error if a reserved word is specified.</span></span> <span data-ttu-id="ae9cf-300">AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-300">You can use the AOTfindChild method to determine whether a field name is already being used.</span></span>

#### <a name="examples"></a><span data-ttu-id="ae9cf-301">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-301">Examples</span></span>

<span data-ttu-id="ae9cf-302">次のコード例は、NewContainer フィールドと NewContainer1 フィールド (両方ともコンテナー タイプ) を TutorialJournalName テーブルのフィールドのリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-302">The following code example adds the NewContainer and NewContainer1 fields, which are both of the container type, to the list of fields of the TutorialJournalName table.</span></span>

    AOTTableFieldList tfl = infolog.findNode( 
        '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 

    // Add a NewContainer field. 
    tfl.addContainer('NewContainer'); 

    // Add a NewContainer1 field. 
    tfl.addContainer('NewContainer');

### <a name="method-addint64"></a><span data-ttu-id="ae9cf-303">メソッド addInt64</span><span class="sxs-lookup"><span data-stu-id="ae9cf-303">Method addInt64</span></span>

    public void addInt64(str name)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-304">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-304">Parameters</span></span>

<span data-ttu-id="ae9cf-305">名前</span><span class="sxs-lookup"><span data-stu-id="ae9cf-305">name</span></span>  

### <a name="method-adddatetime"></a><span data-ttu-id="ae9cf-306">メソッド addDateTime</span><span class="sxs-lookup"><span data-stu-id="ae9cf-306">Method addDateTime</span></span>

    public void addDateTime(str name)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-307">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-307">Parameters</span></span>

<span data-ttu-id="ae9cf-308">名前</span><span class="sxs-lookup"><span data-stu-id="ae9cf-308">name</span></span>  

### <a name="method-adddate"></a><span data-ttu-id="ae9cf-309">メソッド addDate</span><span class="sxs-lookup"><span data-stu-id="ae9cf-309">Method addDate</span></span>

<span data-ttu-id="ae9cf-310">現在のテーブルのフィールドのリストに日付型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-310">Adds a new field of the date type to the list of fields for the current table.</span></span>

    public void addDate(str name)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-311">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-311">Parameters</span></span>

<span data-ttu-id="ae9cf-312">名前</span><span class="sxs-lookup"><span data-stu-id="ae9cf-312">name</span></span>  
<span data-ttu-id="ae9cf-313">追加するフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-313">The name of the field to add.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-314">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-314">Remarks</span></span>

<span data-ttu-id="ae9cf-315">指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-315">If the supplied name coincides with an existing field in the field list, an integer is appended to the name of the new field to make the field name unique.</span></span> <span data-ttu-id="ae9cf-316">開発者は名前が予約語ではないことを確認する必要があります。予約語が指定されている場合、メソッドはエラーをスローしません。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-316">The developer must make sure that the name is not a reserved word; the method will not throw an error if a reserved word is specified.</span></span> <span data-ttu-id="ae9cf-317">AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-317">You can use the AOTfindChild method to determine whether a field name is already being used.</span></span>

#### <a name="examples"></a><span data-ttu-id="ae9cf-318">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-318">Examples</span></span>

<span data-ttu-id="ae9cf-319">次のコード例は、日付タイプである、NewDate フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-319">The following code example adds the NewDate field, which is of the date type, to the list of fields for the TutorialJournalName table.</span></span>

    AOTTableFieldList tfl = infolog.findNode( 
        '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
    if (!tfl.AOTFindChild('NewDate')) 
    { 
        tfl.addDate('NewDate'); 
    }

### <a name="method-addstring"></a><span data-ttu-id="ae9cf-320">メソッド addString</span><span class="sxs-lookup"><span data-stu-id="ae9cf-320">Method addString</span></span>

<span data-ttu-id="ae9cf-321">現在のテーブルのフィールドのリストに文字列型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-321">Adds a new field of the string type to the list of fields for the current table.</span></span>

    public void addString(str name)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-322">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-322">Parameters</span></span>

<span data-ttu-id="ae9cf-323">名前</span><span class="sxs-lookup"><span data-stu-id="ae9cf-323">name</span></span>  
<span data-ttu-id="ae9cf-324">追加するフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-324">The name of the field to add.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-325">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-325">Remarks</span></span>

<span data-ttu-id="ae9cf-326">指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-326">If the supplied name coincides with an existing field in the field list, an integer is appended to the name of the new field to make the field name unique.</span></span> <span data-ttu-id="ae9cf-327">名前が予約語ではないことを確認するのは開発者次第です。予約語が指定されている場合、メソッドはエラーをスローしません。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-327">It is up to the developer to make sure that the name is not a reserved word; the method will not throw an error if a reserved word is specified.</span></span> <span data-ttu-id="ae9cf-328">AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-328">You can use the AOTfindChild method to determine whether a field name is already being used.</span></span>

#### <a name="examples"></a><span data-ttu-id="ae9cf-329">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-329">Examples</span></span>

<span data-ttu-id="ae9cf-330">次の例では、文字列型の NewString フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-330">The following example adds the NewString field, which is of the string type, to the list of fields for the TutorialJournalName table.</span></span>

    { 
        AOTTableFieldList tfl = infolog.findNode( 
            '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
        if (!tfl.AOTFindChild('NewString')) 
        { 
            tfl.addString('NewString'); 
        } 
    }

### <a name="method-addreal"></a><span data-ttu-id="ae9cf-331">メソッド addReal</span><span class="sxs-lookup"><span data-stu-id="ae9cf-331">Method addReal</span></span>

<span data-ttu-id="ae9cf-332">現在のテーブルのフィールドのリストに実数型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-332">Adds a new field of the real type to the list of fields for the current table.</span></span>

    public void addReal(str name)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-333">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-333">Parameters</span></span>

<span data-ttu-id="ae9cf-334">名前</span><span class="sxs-lookup"><span data-stu-id="ae9cf-334">name</span></span>  
<span data-ttu-id="ae9cf-335">追加するフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-335">The name of the field to add.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-336">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-336">Remarks</span></span>

<span data-ttu-id="ae9cf-337">指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-337">If the supplied name coincides with an existing field in the field list, an integer is appended to the name of the new field to make the field name unique.</span></span> <span data-ttu-id="ae9cf-338">名前が予約語ではないことを確認するのは開発者次第です。予約語が指定されている場合、メソッドはエラーをスローしません。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-338">It is up to the developer to make sure that the name is not a reserved word; the method will not throw an error if a reserved word is specified.</span></span> <span data-ttu-id="ae9cf-339">AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-339">You can use the AOTfindChild method to determine whether a field name is already being used.</span></span>

#### <a name="examples"></a><span data-ttu-id="ae9cf-340">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-340">Examples</span></span>

<span data-ttu-id="ae9cf-341">次の例では、実際の型の NewReal フィールドと NewReal1 フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-341">The following example adds the NewReal and NewReal1 fields, which is of the real type, to the list of fields for the TutorialJournalName table.</span></span>

    AOTTableFieldList tfl = infolog.findNode( 
        '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
    // Add the field NewReal. 
    tfl.addReal('NewReal'); 
    // Add the field NewReal1. 
    tfl.addReal('NewReal');

### <a name="method-addtime"></a><span data-ttu-id="ae9cf-342">メソッド addTime</span><span class="sxs-lookup"><span data-stu-id="ae9cf-342">Method addTime</span></span>

<span data-ttu-id="ae9cf-343">現在のテーブルのフィールドのリストに時刻タイプの新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-343">Adds a new field of the time type to the list of fields for the current table.</span></span>

    public void addTime(str name)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-344">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-344">Parameters</span></span>

<span data-ttu-id="ae9cf-345">名前</span><span class="sxs-lookup"><span data-stu-id="ae9cf-345">name</span></span>  
<span data-ttu-id="ae9cf-346">追加するフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-346">The name of the field to add.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-347">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-347">Remarks</span></span>

<span data-ttu-id="ae9cf-348">指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-348">If the supplied name coincides with an existing field in the field list, an integer is appended to the name of the new field to make the field name unique.</span></span> <span data-ttu-id="ae9cf-349">開発者は名前が予約語ではないことを確認する必要があります。予約語が指定されている場合、メソッドはエラーをスローしません。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-349">The developer must make sure that the name is not a reserved word; the method will not throw an error if a reserved word is specified.</span></span> <span data-ttu-id="ae9cf-350">AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-350">You can use the AOTfindChild method to determine whether a field name is already being used.</span></span>

#### <a name="examples"></a><span data-ttu-id="ae9cf-351">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-351">Examples</span></span>

<span data-ttu-id="ae9cf-352">次のコード例は、時間タイプである、NewTime フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-352">The following code example adds the NewTime field, which is of the time type, to the list of fields of the TutorialJournalName table.</span></span>

    AOTTableFieldList tfl = infolog.findNode( 
        '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
    if (!tfl.AOTFindChild('NewTime')) 
    { 
        tfl.addTime('NewTime'); 
    }

### <a name="method-addenum"></a><span data-ttu-id="ae9cf-353">メソッド addEnum</span><span class="sxs-lookup"><span data-stu-id="ae9cf-353">Method addEnum</span></span>

<span data-ttu-id="ae9cf-354">現在のテーブルのフィールドのリストに列挙型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-354">Adds a new field of the enum type to the list of fields for the current table.</span></span>

    public void addEnum(str name)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-355">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-355">Parameters</span></span>

<span data-ttu-id="ae9cf-356">名前</span><span class="sxs-lookup"><span data-stu-id="ae9cf-356">name</span></span>  
<span data-ttu-id="ae9cf-357">追加するフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-357">The name of the field to add.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-358">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-358">Remarks</span></span>

<span data-ttu-id="ae9cf-359">指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-359">If the supplied name coincides with an existing field in the field list, an integer is appended to the name of the new field to make the field name unique.</span></span> <span data-ttu-id="ae9cf-360">名前が予約語ではないことを確認するのは開発者次第です。予約語が指定されている場合、メソッドはエラーをスローしません。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-360">It is up to the developer to make sure that the name is not a reserved word; the method will not throw an error if a reserved word is specified.</span></span> <span data-ttu-id="ae9cf-361">AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-361">You can use the AOTfindChild method to determine whether a field name is already being used.</span></span>

#### <a name="examples"></a><span data-ttu-id="ae9cf-362">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-362">Examples</span></span>

<span data-ttu-id="ae9cf-363">次の例では、列挙型の NewEnum フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-363">The following example adds the NewEnum field, which is of the enum type, to the list of fields of the TutorialJournalName table.</span></span>

    AOTTableFieldList tfl = infolog.findNode( 
        '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
    if (!tfl.AOTFindChild('NewEnum')) 
    { 
        tfl.addEnum('NewEnum');  // adds the field NewEnum 
    }

## <a name="class-applicationobjecttreewindow"></a><span data-ttu-id="ae9cf-364">クラス ApplicationObjectTreeWindow</span><span class="sxs-lookup"><span data-stu-id="ae9cf-364">Class ApplicationObjectTreeWindow</span></span>
    class ApplicationObjectTreeWindow extends Object

### <a name="remarks"></a><span data-ttu-id="ae9cf-365">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-365">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="ae9cf-366">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-366">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="ae9cf-367">メソッド</span><span class="sxs-lookup"><span data-stu-id="ae9cf-367">Methods</span></span>

| <span data-ttu-id="ae9cf-368">方法</span><span class="sxs-lookup"><span data-stu-id="ae9cf-368">Method</span></span>                                  | <span data-ttu-id="ae9cf-369">説明</span><span class="sxs-lookup"><span data-stu-id="ae9cf-369">Description</span></span>                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="ae9cf-370">public str getSelectedNodeModelName()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-370">public str getSelectedNodeModelName()</span></span>   |                                                                      |
| <span data-ttu-id="ae9cf-371">public Set getSelectedNodes()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-371">public Set getSelectedNodes()</span></span>           |                                                                      |
| <span data-ttu-id="ae9cf-372">public Set getSelectedNodesPaths()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-372">public Set getSelectedNodesPaths()</span></span>      |                                                                      |
| <span data-ttu-id="ae9cf-373">public boolean isSelectedNodeExpanded()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-373">public boolean isSelectedNodeExpanded()</span></span> |                                                                      |
| <span data-ttu-id="ae9cf-374">private void new()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-374">private void new()</span></span>                      | <span data-ttu-id="ae9cf-375">ApplicationObjectTreeWindow クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-375">Initializes a new instance of the ApplicationObjectTreeWindow class.</span></span> |

### <a name="method-getselectednodemodelname"></a><span data-ttu-id="ae9cf-376">メソッド getSelectedNodeModelName</span><span class="sxs-lookup"><span data-stu-id="ae9cf-376">Method getSelectedNodeModelName</span></span>

    public str getSelectedNodeModelName()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-377">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-377">Return Value</span></span>

### <a name="method-getselectednodes"></a><span data-ttu-id="ae9cf-378">メソッド getSelectedNodes</span><span class="sxs-lookup"><span data-stu-id="ae9cf-378">Method getSelectedNodes</span></span>

    public Set getSelectedNodes()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-379">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-379">Return Value</span></span>

### <a name="method-getselectednodespaths"></a><span data-ttu-id="ae9cf-380">メソッド getSelectedNodesPaths</span><span class="sxs-lookup"><span data-stu-id="ae9cf-380">Method getSelectedNodesPaths</span></span>

    public Set getSelectedNodesPaths()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-381">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-381">Return Value</span></span>

### <a name="method-isselectednodeexpanded"></a><span data-ttu-id="ae9cf-382">メソッド isSelectedNodeExpanded</span><span class="sxs-lookup"><span data-stu-id="ae9cf-382">Method isSelectedNodeExpanded</span></span>

    public boolean isSelectedNodeExpanded()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-383">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-383">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="ae9cf-384">メソッド new</span><span class="sxs-lookup"><span data-stu-id="ae9cf-384">Method new</span></span>

<span data-ttu-id="ae9cf-385">ApplicationObjectTreeWindow クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-385">Initializes a new instance of the ApplicationObjectTreeWindow class.</span></span>

    private void new()

## <a name="class-array"></a><span data-ttu-id="ae9cf-386">クラス配列</span><span class="sxs-lookup"><span data-stu-id="ae9cf-386">Class Array</span></span>
    class Array extends Object

### <a name="remarks"></a><span data-ttu-id="ae9cf-387">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-387">Remarks</span></span>

<span data-ttu-id="ae9cf-388">配列では、オブジェクトやレコードなど単一タイプの値を保持できます (X++ 言語に組み込まれている配列のデータ タイプとは異なります) 。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-388">Arrays can hold values of any single type, such as objects and records (contrary to the array data type that is built into the X++ language).</span></span> <span data-ttu-id="ae9cf-389">このタイプのオブジェクトは、関数やメソッドに転送することができます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-389">Objects of this type can be transferred to functions and methods.</span></span> <span data-ttu-id="ae9cf-390">値は、順番に格納されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-390">The values are stored sequentially.</span></span> <span data-ttu-id="ae9cf-391">配列は、必要に応じて展開されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-391">The arrays expand as required.</span></span> <span data-ttu-id="ae9cf-392">したがって、配列の特定の分析コードは提供されません。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-392">Therefore, no specific dimension of the array is supplied.</span></span>

### <a name="examples"></a><span data-ttu-id="ae9cf-393">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-393">Examples</span></span>

<span data-ttu-id="ae9cf-394">次の例では、クラスの配列を作成し、3 つのクエリ オブジェクトを配列に追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-394">The following example creates an array of classes and adds three query objects to the array.</span></span>

    { 
        Array oarray = new Array (Types::Class); 

        oarray.value(1, new query()); 
        oarray.value(2, new query()); 
        oarray.value(4, new query());  
        print oarray.toString(); 
        print oarray.definitionString(); 
        pause; 
    }

### <a name="methods"></a><span data-ttu-id="ae9cf-395">メソッド</span><span class="sxs-lookup"><span data-stu-id="ae9cf-395">Methods</span></span>

| <span data-ttu-id="ae9cf-396">方法</span><span class="sxs-lookup"><span data-stu-id="ae9cf-396">Method</span></span>                                              | <span data-ttu-id="ae9cf-397">説明</span><span class="sxs-lookup"><span data-stu-id="ae9cf-397">Description</span></span>                                                                                         |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae9cf-398">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-398">public str definitionString()</span></span>                       | <span data-ttu-id="ae9cf-399">配列の定義を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-399">Returns a string that contains the definition of the array.</span></span>                                         |
| <span data-ttu-id="ae9cf-400">public boolean exists(int index)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-400">public boolean exists(int index)</span></span>                    | <span data-ttu-id="ae9cf-401">特定の配列要素が有効かどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-401">Determines whether a particular array element is valid.</span></span>                                             |
| <span data-ttu-id="ae9cf-402">public int lastIndex()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-402">public int lastIndex()</span></span>                              | <span data-ttu-id="ae9cf-403">配列に値を格納するために使用する最上位のインデックスを取得します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-403">Retrieves the highest index that is used to store a value in the array.</span></span>                             |
| <span data-ttu-id="ae9cf-404">public container pack()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-404">public container pack()</span></span>                             | <span data-ttu-id="ae9cf-405">Array クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-405">Serializes the current instance of the Array class.</span></span>                                                 |
| <span data-ttu-id="ae9cf-406">public str toString()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-406">public str toString()</span></span>                               | <span data-ttu-id="ae9cf-407">配列の内容を説明する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-407">Returns a string that describes the contents of the array.</span></span>                                          |
| <span data-ttu-id="ae9cf-408">public Types typeId()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-408">public Types typeId()</span></span>                               | <span data-ttu-id="ae9cf-409">配列の値のデータ型を返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-409">Returns the data type of the values in the array.</span></span>                                                   |
| <span data-ttu-id="ae9cf-410">public AnyType value(int index, \[AnyType arg\])</span><span class="sxs-lookup"><span data-stu-id="ae9cf-410">public AnyType value(int index, \[AnyType arg\])</span></span>    | <span data-ttu-id="ae9cf-411">指定したインデックスに格納される配列要素の値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-411">Gets or sets the value of the array element that is stored at the specified index.</span></span>                  |
| <span data-ttu-id="ae9cf-412">public str xml(\[int indent\])</span><span class="sxs-lookup"><span data-stu-id="ae9cf-412">public str xml(\[int indent\])</span></span>                      | <span data-ttu-id="ae9cf-413">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-413">Returns an XML string that represents the current object.</span></span>                                           |
| <span data-ttu-id="ae9cf-414">::public static Array create(container container)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-414">::public static Array create(container container)</span></span>   | <span data-ttu-id="ae9cf-415">以前の Array.pack メソッドの呼び出しで取得されるコンテナーから配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-415">Creates an array from the container that is obtained from a previous call to the Array.pack method.</span></span> |
| <span data-ttu-id="ae9cf-416">::public static Array createFromXML(Object xmlnode)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-416">::public static Array createFromXML(Object xmlnode)</span></span> |                                                                                                     |
| <span data-ttu-id="ae9cf-417">public void new(Types Type)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-417">public void new(Types Type)</span></span>                         | <span data-ttu-id="ae9cf-418">各要素が指定されたタイプを持つ配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-418">Creates an array in which each element has the specified type.</span></span>                                      |

### <a name="method-definitionstring"></a><span data-ttu-id="ae9cf-419">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="ae9cf-419">Method definitionString</span></span>

<span data-ttu-id="ae9cf-420">配列の定義を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-420">Returns a string that contains the definition of the array.</span></span>

    public str definitionString()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-421">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-421">Return Value</span></span>

<span data-ttu-id="ae9cf-422">配列の定義を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-422">A string that contains the definition of the array.</span></span>

#### <a name="examples"></a><span data-ttu-id="ae9cf-423">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-423">Examples</span></span>

<span data-ttu-id="ae9cf-424">次の例では、クラスの配列を作成し、3 つのクエリ オブジェクトを配列に追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-424">The following example creates an array of classes and then adds three query objects to the array.</span></span> <span data-ttu-id="ae9cf-425">definitionString メソッドを使用して、配列の定義を出力します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-425">It uses the definitionString method to print a definition of the array.</span></span>

    { 
        Array oarray = new Array (Types::Class); 

        oarray.value(1, new query()); 
        oarray.value(2, new query()); 
        oarray.value(4, new query());  
        print oarray.definitionString(); 
        pause; 
    }

### <a name="method-exists"></a><span data-ttu-id="ae9cf-426">メソッド exists</span><span class="sxs-lookup"><span data-stu-id="ae9cf-426">Method exists</span></span>

<span data-ttu-id="ae9cf-427">特定の配列要素が有効かどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-427">Determines whether a particular array element is valid.</span></span>

    public boolean exists(int index)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-428">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-428">Parameters</span></span>

<span data-ttu-id="ae9cf-429">指数</span><span class="sxs-lookup"><span data-stu-id="ae9cf-429">index</span></span>  
<span data-ttu-id="ae9cf-430">テスト対象の配列要素。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-430">The array element to test.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ae9cf-431">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-431">Return Value</span></span>

<span data-ttu-id="ae9cf-432">インデックスにより指定される配列要素が有効な場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-432">true if the array element that is pointed to by the index is valid; otherwise, false.</span></span>

#### <a name="examples"></a><span data-ttu-id="ae9cf-433">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-433">Examples</span></span>

<span data-ttu-id="ae9cf-434">次の例では、exists メソッドを使用して、配列内のさまざまな要素が有効かどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-434">The following example uses the exists method to test whether various elements in an array are valid.</span></span>

    { 
        array a = new array(types::Integer); 

        a.value(1, 23); 

        print a.value(1); 
        pause; 
        if (a.exists(7)) // No, only element 1 is initialized 
        { 
            print a.value(7); 

        } 
        else  
        { 
            print "Value does not exist"; 
        } 
        pause; 

        //Array positions 2 to 9 padded with default values 
        a.value(10, 55); 

        if (a.exists(7)) // Yes, elements 1..10 now initialized 
        { 
            print a.value(7); 
        } 
        else  
        { 
            print "Value does not exist"; 
        } 
        pause; 
    }

### <a name="method-lastindex"></a><span data-ttu-id="ae9cf-435">メソッド lastIndex</span><span class="sxs-lookup"><span data-stu-id="ae9cf-435">Method lastIndex</span></span>

<span data-ttu-id="ae9cf-436">配列に値を格納するために使用する最上位のインデックスを取得します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-436">Retrieves the highest index that is used to store a value in the array.</span></span>

    public int lastIndex()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-437">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-437">Return Value</span></span>

<span data-ttu-id="ae9cf-438">値を格納するために使用する最上位のインデックスを表す整数。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-438">An integer that represents the highest index that is used to store a value.</span></span>

#### <a name="examples"></a><span data-ttu-id="ae9cf-439">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-439">Examples</span></span>

<span data-ttu-id="ae9cf-440">次の例では、lastIndex メソッドを使用して配列の最後の要素を見つけ、この要素の後に新しい値を追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-440">The following example uses the lastIndex method to find the last element in the array and then add a new value after this element.</span></span>

    { 
        Array myArray = new Array(Types::Integer); 
        int newValue; 

        // Other code - values are added to myArray 
        // and a value is assigned to newValue 

        myArray.value(myArray.lastIndex()+1, newValue); 
    }

### <a name="method-pack"></a><span data-ttu-id="ae9cf-441">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="ae9cf-441">Method pack</span></span>

<span data-ttu-id="ae9cf-442">Array クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-442">Serializes the current instance of the Array class.</span></span>

    public container pack()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-443">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-443">Return Value</span></span>

<span data-ttu-id="ae9cf-444">Array クラスの現在のインスタンスを含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-444">A container that contains the current instance of the Array class.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-445">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-445">Remarks</span></span>

<span data-ttu-id="ae9cf-446">このメソッドで作成されたコンテナーには、配列の最初の要素の前に 3 つの要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-446">The container created by this method contains three elements before the first element from the array:</span></span>

-   <span data-ttu-id="ae9cf-447">コンテナのバージョン番号。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-447">A version number for the container.</span></span>
-   <span data-ttu-id="ae9cf-448">配列要素のデータ型を識別する整数。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-448">An integer that identifies the data type of the array elements.</span></span>
-   <span data-ttu-id="ae9cf-449">この配列の要素の数。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-449">The number of elements in the array.</span></span>

<span data-ttu-id="ae9cf-450">配列の値がオブジェクトになっている場合は、各オブジェクトに対して pack メソッドが呼び出され、サブコンテナーを取得します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-450">If the values of the array are objects, the pack method is called on each object to yield a subcontainer.</span></span>

#### <a name="examples"></a><span data-ttu-id="ae9cf-451">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-451">Examples</span></span>

<span data-ttu-id="ae9cf-452">次の例では、整数の配列を作成し、それにいくつかの値を追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-452">The following example creates an array of integers and adds some values to it.</span></span> <span data-ttu-id="ae9cf-453">pack メソッドを使用して配列をコンテナーにパックし、コンテナーを使用して新しい配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-453">The pack method is used to pack the array into a container, and the container is then used to create a new array.</span></span>

    { 
        int i; 
        container packedArray; 
        // Create an integer array 
        Array ia = new Array (Types::Integer); 
        Array iacopy; 

        // Write some elements in it 
        for (i = 1; i< 10; i++) 
        { 
            ia.value(i, i*2); 
        } 

        // Pack the array 
        packedArray = ia.pack(); 

        // Unpack the array  
        iacopy = Array::create(packedArray); 

        // Check the values 
        for (i = 1; i< 10; i++) 
        { 
            if (iacopy.value(i) != 2*i) 
            { 
                print "Error!"; 
            } 
        } 
        pause; 
    }

### <a name="method-tostring"></a><span data-ttu-id="ae9cf-454">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="ae9cf-454">Method toString</span></span>

<span data-ttu-id="ae9cf-455">配列の内容を説明する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-455">Returns a string that describes the contents of the array.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-456">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-456">Return Value</span></span>

<span data-ttu-id="ae9cf-457">配列の内容を説明する文字列。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-457">A string that describes the contents of the array.</span></span>

#### <a name="examples"></a><span data-ttu-id="ae9cf-458">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-458">Examples</span></span>

<span data-ttu-id="ae9cf-459">次の例では、整数の配列を作成し、それにいくつかの値を追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-459">The following example creates an array of integers and adds some values to it.</span></span> <span data-ttu-id="ae9cf-460">toString メソッドは、配列が保持する値を出力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-460">The toString method is used to print the values that the array holds.</span></span>

    { 
        Array     myArray; 

        Set set1 = new Set(Types::Integer); 
        Set set2 = new Set(Types::Integer); 
        int i; 


        myArray = new Array(Types::Integer); 

        // Add some values to the array. 
        for (i = 1; i< 10; i++) 
        { 
            myArray.value(i, i*2); 
        } 

        // Print out the values in the array. 
        print myArray.toString(); 
        pause; 
    }

### <a name="method-typeid"></a><span data-ttu-id="ae9cf-461">メソッド typeId</span><span class="sxs-lookup"><span data-stu-id="ae9cf-461">Method typeId</span></span>

<span data-ttu-id="ae9cf-462">配列の値のデータ型を返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-462">Returns the data type of the values in the array.</span></span>

    public Types typeId()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-463">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-463">Return Value</span></span>

<span data-ttu-id="ae9cf-464">配列の要素のデータ型。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-464">The data type of the elements in the array.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-465">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-465">Remarks</span></span>

<span data-ttu-id="ae9cf-466">タイプは配列の寿命を通して同じままです。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-466">The type remains the same throughout the life of the array.</span></span> <span data-ttu-id="ae9cf-467">タイプは、配列の作成時に指定されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-467">The type is specified when the array is created.</span></span>

#### <a name="examples"></a><span data-ttu-id="ae9cf-468">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-468">Examples</span></span>

<span data-ttu-id="ae9cf-469">次の例では、特定の配列要素が存在するかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-469">The following example tests whether a particular array element exists.</span></span> <span data-ttu-id="ae9cf-470">存在しない場合、配列に追加する必要がある新しい値のタイプを指定するために typeId メソッドが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-470">If it does not exist, the typeId method is used to specify the type of the new value that should be added to the array.</span></span>

    public anytype getArrayValue(Array a, int _index) 
    { 
        if (! a.exists(_index)) 
        { 
            a.value(_index,nullValueFromType(a.typeId())); 
        } 

        return a.value(_index); 
    }

### <a name="method-value"></a><span data-ttu-id="ae9cf-471">メソッド value</span><span class="sxs-lookup"><span data-stu-id="ae9cf-471">Method value</span></span>

<span data-ttu-id="ae9cf-472">指定したインデックスに格納される配列要素の値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-472">Gets or sets the value of the array element that is stored at the specified index.</span></span>

    public AnyType value(int index, [AnyType arg])

#### <a name="parameters"></a><span data-ttu-id="ae9cf-473">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-473">Parameters</span></span>

<span data-ttu-id="ae9cf-474">指数</span><span class="sxs-lookup"><span data-stu-id="ae9cf-474">index</span></span>  
<span data-ttu-id="ae9cf-475">指定されたオフセットで配列要素に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-475">The value to assign to the array element at the specified offset; optional.</span></span>

<!-- -->

<span data-ttu-id="ae9cf-476">arg</span><span class="sxs-lookup"><span data-stu-id="ae9cf-476">arg</span></span>  
<span data-ttu-id="ae9cf-477">指定されたオフセットで配列要素に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-477">The value to assign to the array element at the specified offset; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ae9cf-478">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-478">Return Value</span></span>

<span data-ttu-id="ae9cf-479">指定したオフセットに格納されている値。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-479">The value that is stored at the specified offset.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-480">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-480">Remarks</span></span>

<span data-ttu-id="ae9cf-481">戻り値のタイプは、配列のタイプと同じです。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-481">The return type is the same as the type of the array.</span></span> <span data-ttu-id="ae9cf-482">値を持つ最後のインデックスを超えるインデックスで値を読み取ろうとすると、例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-482">If an attempt is made to read a value at an index that is beyond the last index that has a value, an exception is thrown.</span></span> <span data-ttu-id="ae9cf-483">値が実在しない位置に書き込まれる場合、前の要素とその実在しない位置との間にあるすべての位置に既定値が入力され、配列が展開されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-483">If a value is written to a nonexistent location, all locations between the previous element and the nonexistent location are filled with default values, and the array is expanded.</span></span>

#### <a name="examples"></a><span data-ttu-id="ae9cf-484">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-484">Examples</span></span>

<span data-ttu-id="ae9cf-485">次の例では、整数の配列を作成し、value メソッドを使用して値を配列に追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-485">The following example creates an array of integers and then uses the value method to add some values to the array.</span></span> <span data-ttu-id="ae9cf-486">値のメソッドを使用して配列内で格納されている値を取得し、それらをテストします。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-486">It then uses the value method to get the values that are stored in the array and test them.</span></span>

    { 
         int i; 
        // Create an integer array 
        Array ia = new Array (Types::Integer); 

        // Write some elements in it 
        for (i = 1; i< 10; i++) 
        { 
            ia.value(i, i*2); 
        } 

        // Check the values 
        for (i = 1; i< 10; i++) 
        { 
            if (ia.value(i) != 2*i) 
            { 
                print "Error!"; 
            } 
        } 
        pause; 
    }

### <a name="method-xml"></a><span data-ttu-id="ae9cf-487">メソッド xml</span><span class="sxs-lookup"><span data-stu-id="ae9cf-487">Method xml</span></span>

<span data-ttu-id="ae9cf-488">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-488">Returns an XML string that represents the current object.</span></span>

    public str xml([int indent])

#### <a name="parameters"></a><span data-ttu-id="ae9cf-489">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-489">Parameters</span></span>

<span data-ttu-id="ae9cf-490">インデント</span><span class="sxs-lookup"><span data-stu-id="ae9cf-490">indent</span></span>  
<span data-ttu-id="ae9cf-491">返された XML 文字列のインデントの量 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-491">The amount of indentation of the returned XML string; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ae9cf-492">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-492">Return Value</span></span>

<span data-ttu-id="ae9cf-493">現在のオブジェクトを表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-493">An XML string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-494">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-494">Remarks</span></span>

<span data-ttu-id="ae9cf-495">このメソッドをオーバーライドして、特定の型に対して意味のある値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-495">This method can be overridden to return values that are meaningful for a particular type.</span></span>

### <a name="method-create"></a><span data-ttu-id="ae9cf-496">メソッド create</span><span class="sxs-lookup"><span data-stu-id="ae9cf-496">Method create</span></span>

<span data-ttu-id="ae9cf-497">以前の Array.pack メソッドの呼び出しで取得されるコンテナーから配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-497">Creates an array from the container that is obtained from a previous call to the Array.pack method.</span></span>

    public static Array create(container container)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-498">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-498">Parameters</span></span>

<span data-ttu-id="ae9cf-499">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ae9cf-499">container</span></span>  
<span data-ttu-id="ae9cf-500">Array.pack メソッドを使用して作成されるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-500">A container that is created by using the Array.pack method.</span></span> <span data-ttu-id="ae9cf-501">コンテナーを展開して配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-501">The container is unpacked to create an array.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ae9cf-502">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-502">Return Value</span></span>

<span data-ttu-id="ae9cf-503">指定したコンテナーの内容を保持する配列です。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-503">An array that holds the contents of the specified container.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-504">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-504">Remarks</span></span>

<span data-ttu-id="ae9cf-505">配列の値がオブジェクトの場合、オブジェクトにはコンテナーからその内部状態を再設定するために呼び出される Array.unpack メソッドが必要です。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-505">If the values in the array are objects, the objects must have an Array.unpack method that is called to reestablish their internal state from a container.</span></span>

#### <a name="examples"></a><span data-ttu-id="ae9cf-506">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-506">Examples</span></span>

<span data-ttu-id="ae9cf-507">次の例では、配列を作成し、2 つのセットを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-507">The following example creates an array and adds two sets to it.</span></span> <span data-ttu-id="ae9cf-508">配列がパックされ、それを使用して、新しい配列が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-508">The array is packed and then used to create a new array.</span></span>

    { 
        Array     myArray; 
        Array     newArray; 
        container packedArray; 

        Set set1 = new Set(Types::Integer); 
        Set set2 = new Set(Types::Integer); 
        int i; 
        int j; 

        myArray = new Array(Types::Class); 

        // Add some values to the set1 and set2 
        for (i = 0; i < 10; i++) 
        { 
            set1.add(i); 
            j = i+3; 
            set2.add(j); 
        } 

        // Add set1 and set2 to myArray 
        myArray.value(1, set1); 
        myArray.value(2, set2); 

        // Pack the myArray into a container 
        packedArray = myArray.pack(); 

        // Create a new array from the container 
        if(packedArray != connull()) 
        { 
            newArray = Array::create(packedArray); 
        } 

        // Test that newArray has same contents as myArray 
        print newArray.definitionString(); 
        print newArray.toString(); 
        pause; 
    }

### <a name="method-createfromxml"></a><span data-ttu-id="ae9cf-509">メソッド createFromXML</span><span class="sxs-lookup"><span data-stu-id="ae9cf-509">Method createFromXML</span></span>

    public static Array createFromXML(Object xmlnode)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-510">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-510">Parameters</span></span>

<span data-ttu-id="ae9cf-511">xmlnode</span><span class="sxs-lookup"><span data-stu-id="ae9cf-511">xmlnode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="ae9cf-512">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-512">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="ae9cf-513">メソッド new</span><span class="sxs-lookup"><span data-stu-id="ae9cf-513">Method new</span></span>

<span data-ttu-id="ae9cf-514">各要素が指定されたタイプを持つ配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-514">Creates an array in which each element has the specified type.</span></span>

    public void new(Types Type)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-515">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-515">Parameters</span></span>

<span data-ttu-id="ae9cf-516">種類</span><span class="sxs-lookup"><span data-stu-id="ae9cf-516">Type</span></span>  
<span data-ttu-id="ae9cf-517">配列要素のデータ型。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-517">The data type of the array elements.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-518">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-518">Remarks</span></span>

<span data-ttu-id="ae9cf-519">可能な値は、Types システム列挙に使用可能な値です。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-519">The possible values are those that are available for the Types system enumeration:</span></span>

-   <span data-ttu-id="ae9cf-520">AnyType</span><span class="sxs-lookup"><span data-stu-id="ae9cf-520">AnyType</span></span>
-   <span data-ttu-id="ae9cf-521">BLOB</span><span class="sxs-lookup"><span data-stu-id="ae9cf-521">BLOB</span></span>
-   <span data-ttu-id="ae9cf-522">クラス</span><span class="sxs-lookup"><span data-stu-id="ae9cf-522">Class</span></span>
-   <span data-ttu-id="ae9cf-523">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ae9cf-523">Container</span></span>
-   <span data-ttu-id="ae9cf-524">日</span><span class="sxs-lookup"><span data-stu-id="ae9cf-524">Date</span></span>
-   <span data-ttu-id="ae9cf-525">日時</span><span class="sxs-lookup"><span data-stu-id="ae9cf-525">DateTime</span></span>
-   <span data-ttu-id="ae9cf-526">列挙</span><span class="sxs-lookup"><span data-stu-id="ae9cf-526">Enum</span></span>
-   <span data-ttu-id="ae9cf-527">Guid</span><span class="sxs-lookup"><span data-stu-id="ae9cf-527">Guid</span></span>
-   <span data-ttu-id="ae9cf-528">Int64</span><span class="sxs-lookup"><span data-stu-id="ae9cf-528">Int64</span></span>
-   <span data-ttu-id="ae9cf-529">整数</span><span class="sxs-lookup"><span data-stu-id="ae9cf-529">Integer</span></span>

#### <a name="examples"></a><span data-ttu-id="ae9cf-530">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-530">Examples</span></span>

<span data-ttu-id="ae9cf-531">次の例では、整数の配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-531">The following example creates an array of integers.</span></span>

    Array intArray = new Array(Types::Integer);

## <a name="class-asciiio"></a><span data-ttu-id="ae9cf-532">クラス AsciiIo</span><span class="sxs-lookup"><span data-stu-id="ae9cf-532">Class AsciiIo</span></span>
    class AsciiIo extends CommaIo

<span data-ttu-id="ae9cf-533">AsciiIo クラスには、ASCII ファイルの読み取りと書き込みを行う機能があります。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-533">The AsciiIo class provides functionality for reading and writing ASCII files.</span></span>

### <a name="remarks"></a><span data-ttu-id="ae9cf-534">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-534">Remarks</span></span>

<span data-ttu-id="ae9cf-535">TextIo クラスには、さまざまなコード ページを使用するファイルの読み取りと書き込みを行う機能があります。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-535">The TextIo class provides functionality for reading and writing files that use various code pages.</span></span> <span data-ttu-id="ae9cf-536">AsciiIO クラスは、ANSI コード ページ (ACP) 文字のみサポートします。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-536">The AsciiIO class supports only ANSI code page (ACP) characters.</span></span> <span data-ttu-id="ae9cf-537">AsciiIO クラスを使用する既存のコードは、ファイルに ACP 以外の文字が含まれている場合や、.xpo ファイルなどの Finance and Operations アプリケーションでのみ使用されるファイルの場合に TextIO クラスを使用するように変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-537">Existing code that uses the AsciiIO class must be converted to use the TextIO class if the file contains non-ACP characters, or if it is a file that is used only in a Finance and Operations application, such as an .xpo file.</span></span>

### <a name="examples"></a><span data-ttu-id="ae9cf-538">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-538">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="ae9cf-539">メソッド</span><span class="sxs-lookup"><span data-stu-id="ae9cf-539">Methods</span></span>

| <span data-ttu-id="ae9cf-540">方法</span><span class="sxs-lookup"><span data-stu-id="ae9cf-540">Method</span></span>                                       | <span data-ttu-id="ae9cf-541">説明</span><span class="sxs-lookup"><span data-stu-id="ae9cf-541">Description</span></span>                                                                                                                      |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae9cf-542">public str inFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ae9cf-542">public str inFieldDelimiter(\[str value\])</span></span>   | <span data-ttu-id="ae9cf-543">AsciiIO オブジェクトによって表される入力ファイルのフィールド区切り記号として使用される文字を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-543">Sets or retrieves the character that is used as the field delimiter of an input file that is represented by an AsciiIO object.</span></span>   |
| <span data-ttu-id="ae9cf-544">public str inRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ae9cf-544">public str inRecordDelimiter(\[str value\])</span></span>  | <span data-ttu-id="ae9cf-545">AsciiIO オブジェクトによって表される入力ファイルのレコード区切り記号として使用される文字を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-545">Sets or retrieves the character that is used as the record delimiter of an input file that is represented by an AsciiIO object.</span></span>  |
| <span data-ttu-id="ae9cf-546">public int inRecordLength(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ae9cf-546">public int inRecordLength(\[int value\])</span></span>     | <span data-ttu-id="ae9cf-547">入力ファイルのレコードの長さを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-547">Sets or retrieves the record length for an input file.</span></span>                                                                           |
| <span data-ttu-id="ae9cf-548">public str outFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ae9cf-548">public str outFieldDelimiter(\[str value\])</span></span>  | <span data-ttu-id="ae9cf-549">AsciiIO オブジェクトによって表される出力ファイルのフィールド区切り記号として使用される文字を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-549">Sets or retrieves the character that is used as the field delimiter of an output file that is represented by an AsciiIO object.</span></span>  |
| <span data-ttu-id="ae9cf-550">public str outRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ae9cf-550">public str outRecordDelimiter(\[str value\])</span></span> | <span data-ttu-id="ae9cf-551">AsciiIO オブジェクトによって表される出力ファイルのレコード区切り記号として使用される文字を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-551">Sets or retrieves the character that is used as the record delimiter of an output file that is represented by an AsciiIO object.</span></span> |
| <span data-ttu-id="ae9cf-552">public container read()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-552">public container read()</span></span>                      | <span data-ttu-id="ae9cf-553">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-553">Reads the next full record from the Io object.</span></span>                                                                                   |
| <span data-ttu-id="ae9cf-554">public IO\_Status status()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-554">public IO\_Status status()</span></span>                   | <span data-ttu-id="ae9cf-555">ファイルでの最後の操作のステータスを返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-555">Returns the status of the last operation on the file.</span></span>                                                                            |
| <span data-ttu-id="ae9cf-556">public boolean write(VarArg values)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-556">public boolean write(VarArg values)</span></span>          | <span data-ttu-id="ae9cf-557">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-557">Writes values of a simple type.</span></span>                                                                                                  |
| <span data-ttu-id="ae9cf-558">public boolean writeChar(int int)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-558">public boolean writeChar(int int)</span></span>            |                                                                                                                                  |
| <span data-ttu-id="ae9cf-559">public boolean writeExp(container data)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-559">public boolean writeExp(container data)</span></span>      | <span data-ttu-id="ae9cf-560">コンテナのコンテンツをファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-560">Writes the content of a container to a file.</span></span>                                                                                     |
| <span data-ttu-id="ae9cf-561">public boolean writeRaw(str data)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-561">public boolean writeRaw(str data)</span></span>            |                                                                                                                                  |
| <span data-ttu-id="ae9cf-562">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-562">public void finalize()</span></span>                       | <span data-ttu-id="ae9cf-563">ファイルを閉じ、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-563">Closes the file and then flushes the file buffers to disk.</span></span>                                                                       |
| <span data-ttu-id="ae9cf-564">public void new(str filename, str mode)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-564">public void new(str filename, str mode)</span></span>      | <span data-ttu-id="ae9cf-565">AsciiIo クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-565">Creates an instance of the AsciiIo class.</span></span>                                                                                        |

### <a name="method-infielddelimiter"></a><span data-ttu-id="ae9cf-566">メソッド inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="ae9cf-566">Method inFieldDelimiter</span></span>

<span data-ttu-id="ae9cf-567">AsciiIO オブジェクトによって表される入力ファイルのフィールド区切り記号として使用される文字を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-567">Sets or retrieves the character that is used as the field delimiter of an input file that is represented by an AsciiIO object.</span></span>

    public str inFieldDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="ae9cf-568">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-568">Parameters</span></span>

<span data-ttu-id="ae9cf-569">値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-569">value</span></span>  
<span data-ttu-id="ae9cf-570">フィールドの区切り記号として割り当てられる文字。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-570">The character to assign as the field delimiter.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ae9cf-571">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-571">Return Value</span></span>

<span data-ttu-id="ae9cf-572">フィールドの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-572">The character that is used as the field delimiter.</span></span>

### <a name="method-inrecorddelimiter"></a><span data-ttu-id="ae9cf-573">メソッド inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="ae9cf-573">Method inRecordDelimiter</span></span>

<span data-ttu-id="ae9cf-574">AsciiIO オブジェクトによって表される入力ファイルのレコード区切り記号として使用される文字を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-574">Sets or retrieves the character that is used as the record delimiter of an input file that is represented by an AsciiIO object.</span></span>

    public str inRecordDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="ae9cf-575">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-575">Parameters</span></span>

<span data-ttu-id="ae9cf-576">値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-576">value</span></span>  
<span data-ttu-id="ae9cf-577">レコードの区切り記号として割り当てられる文字。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-577">The character to assign as the record delimiter.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ae9cf-578">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-578">Return Value</span></span>

<span data-ttu-id="ae9cf-579">レコードの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-579">The character that is used as the record delimiter.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-580">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-580">Remarks</span></span>

<span data-ttu-id="ae9cf-581">標準的なテキストについては、区切り記号は改行文字です。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-581">For standard text, the delimiter is a newline character.</span></span>

### <a name="method-inrecordlength"></a><span data-ttu-id="ae9cf-582">メソッド inRecordLength</span><span class="sxs-lookup"><span data-stu-id="ae9cf-582">Method inRecordLength</span></span>

<span data-ttu-id="ae9cf-583">入力ファイルのレコードの長さを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-583">Sets or retrieves the record length for an input file.</span></span>

    public int inRecordLength([int value])

#### <a name="parameters"></a><span data-ttu-id="ae9cf-584">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-584">Parameters</span></span>

<span data-ttu-id="ae9cf-585">値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-585">value</span></span>  
<span data-ttu-id="ae9cf-586">入力ファイルのレコード長として割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-586">The value to assign as the record length for the input file.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ae9cf-587">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-587">Return Value</span></span>

<span data-ttu-id="ae9cf-588">入力ファイルのレコードの長さ。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-588">The record length for the input file.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-589">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-589">Remarks</span></span>

<span data-ttu-id="ae9cf-590">固定長形式になっているファイルについては、inRecordLength プロパティを使用して、各レコードに対して指定された文字数以上が読み取られていないことを保証します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-590">For files that have a fixed-length format, use the inRecordLength property to guarantee that no more than the specified number of characters is read for each record.</span></span> <span data-ttu-id="ae9cf-591">レコード フォーマットが指定された inRecordDelimiter プロパティ値で上書きされた場合 (つまり、固定長が読み込まれる前に inRecordDelimiter 値が満たされている場合)、レコードは受け入れられ、それ以上のデータは読み込まれません。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-591">If the record format is overruled by a specified inRecordDelimiter property value (in other words, if the inRecordDelimiter value is met before the fixed length is read), the record is accepted, and no more data is read.</span></span> <span data-ttu-id="ae9cf-592">固定数の文字を確実に読み取るには、inRecordDelimiter プロパティ値を空の文字列に設定します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-592">To make sure that a fixed number of characters is read, set the inRecordDelimiter property value to an empty string.</span></span> <span data-ttu-id="ae9cf-593">inRecordDelimiter プロパティ値が見つからない場合、inRecordDelimiter プロパティ値は読み取れる最大文字数になります。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-593">When no inRecordDelimiter property value is found, the inRecordDelimiter property value is the maximum limit of characters to read.</span></span> <span data-ttu-id="ae9cf-594">レコードの長さのチェックを無効にするには、inRecordDelimiter プロパティ値を 0 (ゼロ) に設定します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-594">Set the inRecordDelimiter property value to 0 (zero) to disable the check of the record length.</span></span>

### <a name="method-outfielddelimiter"></a><span data-ttu-id="ae9cf-595">メソッド outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="ae9cf-595">Method outFieldDelimiter</span></span>

<span data-ttu-id="ae9cf-596">AsciiIO オブジェクトによって表される出力ファイルのフィールド区切り記号として使用される文字を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-596">Sets or retrieves the character that is used as the field delimiter of an output file that is represented by an AsciiIO object.</span></span>

    public str outFieldDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="ae9cf-597">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-597">Parameters</span></span>

<span data-ttu-id="ae9cf-598">値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-598">value</span></span>  
<span data-ttu-id="ae9cf-599">フィールドの区切り記号として割り当てられる文字。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-599">The character to assign as the field delimiter.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ae9cf-600">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-600">Return Value</span></span>

<span data-ttu-id="ae9cf-601">フィールドの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-601">The character that is used as the field delimiter.</span></span>

### <a name="method-outrecorddelimiter"></a><span data-ttu-id="ae9cf-602">メソッド outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="ae9cf-602">Method outRecordDelimiter</span></span>

<span data-ttu-id="ae9cf-603">AsciiIO オブジェクトによって表される出力ファイルのレコード区切り記号として使用される文字を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-603">Sets or retrieves the character that is used as the record delimiter of an output file that is represented by an AsciiIO object.</span></span>

    public str outRecordDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="ae9cf-604">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-604">Parameters</span></span>

<span data-ttu-id="ae9cf-605">値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-605">value</span></span>  
<span data-ttu-id="ae9cf-606">レコードの区切り記号として割り当てられる文字。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-606">The character to assign as the record delimiter.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ae9cf-607">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-607">Return Value</span></span>

<span data-ttu-id="ae9cf-608">レコードの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-608">The character that is used as the record delimiter.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-609">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-609">Remarks</span></span>

<span data-ttu-id="ae9cf-610">標準的なテキスト ファイルについては、区切り記号は改行文字です。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-610">For standard text files, the delimiter is a newline character.</span></span>

### <a name="method-read"></a><span data-ttu-id="ae9cf-611">メソッド read</span><span class="sxs-lookup"><span data-stu-id="ae9cf-611">Method read</span></span>

<span data-ttu-id="ae9cf-612">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-612">Reads the next full record from the Io object.</span></span>

    public container read()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-613">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-613">Return Value</span></span>

<span data-ttu-id="ae9cf-614">Io オブジェクトからの次の完全なレコード。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-614">The next full record from the Io object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-615">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-615">Remarks</span></span>

<span data-ttu-id="ae9cf-616">次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-616">The definition of the next full record is controlled by the following properties: inFieldDelimiter, inRecordDelimiter, and inRecordLength.</span></span> <span data-ttu-id="ae9cf-617">レコードはコンテナーとして返されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-617">The record is returned as a container.</span></span> <span data-ttu-id="ae9cf-618">コンテナー内の各エントリは、レコードの 1 つのフィールドを表します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-618">Each entry in the container represents one field in the record.</span></span> <span data-ttu-id="ae9cf-619">それぞれの特殊な Io クラスには、inFieldDelimiter、inRecordDelimiter、および inRecordLength のデフォルト設定があります。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-619">Each of the specialized Io classes has default settings for inFieldDelimiter, inRecordDelimiter, and inRecordLength.</span></span> <span data-ttu-id="ae9cf-620">これらの設定では、最も一般的な形式の入力と出力が可能です。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-620">These settings allow for input and output of the most common formats.</span></span> <span data-ttu-id="ae9cf-621">ただし、目的の形式をサポートするために、これらの設定の調整が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-621">However, you might have to adjust these settings to support the desired format.</span></span>

### <a name="method-status"></a><span data-ttu-id="ae9cf-622">メソッド status</span><span class="sxs-lookup"><span data-stu-id="ae9cf-622">Method status</span></span>

<span data-ttu-id="ae9cf-623">ファイルでの最後の操作のステータスを返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-623">Returns the status of the last operation on the file.</span></span>

    public IO_Status status()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-624">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-624">Return Value</span></span>

<span data-ttu-id="ae9cf-625">最後のファイル操作の状態。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-625">The status of the last file operation.</span></span>

### <a name="method-write"></a><span data-ttu-id="ae9cf-626">メソッド write</span><span class="sxs-lookup"><span data-stu-id="ae9cf-626">Method write</span></span>

<span data-ttu-id="ae9cf-627">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-627">Writes values of a simple type.</span></span>

    public boolean write(VarArg values)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-628">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-628">Parameters</span></span>

<span data-ttu-id="ae9cf-629">値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-629">values</span></span>  
<span data-ttu-id="ae9cf-630">1 つ以上の値の、各単純型は、フィールドの区切り記号で区切られています。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-630">One or more values, each of a simple type, separated by a field delimiter.</span></span> <span data-ttu-id="ae9cf-631">単純型は、文字列、整数、実数、列挙型、日付です。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-631">The simple types are string, integer, real, enum, and date.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ae9cf-632">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-632">Return Value</span></span>

<span data-ttu-id="ae9cf-633">書き込み操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-633">true if the write operation succeeds; otherwise, false.</span></span> <span data-ttu-id="ae9cf-634">書き込み操作が失敗すると、ステータスをチェックし、原因について確認できます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-634">If the write operation fails, you can check the status to learn the cause.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-635">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-635">Remarks</span></span>

<span data-ttu-id="ae9cf-636">このメソッドは、可変数の引数を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-636">The method accepts a variable number of arguments.</span></span> <span data-ttu-id="ae9cf-637">指定された各値は、フィールドとして出力レコードに配置されます: 最初のフィールドとしての最初の引数、2 番目のフィールドとしての 2 番目の引数など。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-637">Each value that is specified is put into the output record as a field: the first argument as the first field, the second argument as the second field, and so on.</span></span> <span data-ttu-id="ae9cf-638">フィールドは、outFieldDelimiter メソッドで指定される区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-638">Fields are separated by the delimiter that is specified in the outFieldDelimiter method.</span></span> <span data-ttu-id="ae9cf-639">レコードは、outRecordDelimiter メソッドで指定される区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-639">Records are separated by the delimiter that is specified in the outRecordDelimiter method.</span></span> <span data-ttu-id="ae9cf-640">完全なコンテナーを書き込むには、writeExp メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-640">To write complete containers, use the writeExp method.</span></span>

### <a name="method-writechar"></a><span data-ttu-id="ae9cf-641">メソッド writeChar</span><span class="sxs-lookup"><span data-stu-id="ae9cf-641">Method writeChar</span></span>

    public boolean writeChar(int int)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-642">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-642">Parameters</span></span>

<span data-ttu-id="ae9cf-643">int</span><span class="sxs-lookup"><span data-stu-id="ae9cf-643">int</span></span>  

#### <a name="return-value"></a><span data-ttu-id="ae9cf-644">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-644">Return Value</span></span>

### <a name="method-writeexp"></a><span data-ttu-id="ae9cf-645">メソッド writeExp</span><span class="sxs-lookup"><span data-stu-id="ae9cf-645">Method writeExp</span></span>

<span data-ttu-id="ae9cf-646">コンテナのコンテンツをファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-646">Writes the content of a container to a file.</span></span>

    public boolean writeExp(container data)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-647">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-647">Parameters</span></span>

<span data-ttu-id="ae9cf-648">データ</span><span class="sxs-lookup"><span data-stu-id="ae9cf-648">data</span></span>  
<span data-ttu-id="ae9cf-649">レコードのデータを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-649">The container that holds data for the record.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ae9cf-650">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-650">Return Value</span></span>

<span data-ttu-id="ae9cf-651">操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-651">true if the operation succeeds; otherwise, false.</span></span> <span data-ttu-id="ae9cf-652">工程が失敗すると、ステータスをチェックし原因について確認します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-652">If the operation fails, check the status to learn the cause.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-653">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-653">Remarks</span></span>

<span data-ttu-id="ae9cf-654">コンテナー内のエントリはフィールドとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-654">The entries in the container are treated as fields.</span></span> <span data-ttu-id="ae9cf-655">コンテナーは、完全なレコードとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-655">The container is treated as a full record.</span></span> <span data-ttu-id="ae9cf-656">フィールドは、outFieldDelimiter メソッドで指定される区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-656">Fields are separated by the delimiter that is specified in the outFieldDelimiter method.</span></span> <span data-ttu-id="ae9cf-657">レコードは、outRecordDelimiter メソッドで指定される区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-657">Records are separated by the delimiter that is specified in the outRecordDelimiter method.</span></span>

### <a name="method-writeraw"></a><span data-ttu-id="ae9cf-658">メソッド writeRaw</span><span class="sxs-lookup"><span data-stu-id="ae9cf-658">Method writeRaw</span></span>

    public boolean writeRaw(str data)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-659">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-659">Parameters</span></span>

<span data-ttu-id="ae9cf-660">データ</span><span class="sxs-lookup"><span data-stu-id="ae9cf-660">data</span></span>  

#### <a name="return-value"></a><span data-ttu-id="ae9cf-661">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-661">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="ae9cf-662">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="ae9cf-662">Method finalize</span></span>

<span data-ttu-id="ae9cf-663">ファイルを閉じ、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-663">Closes the file and then flushes the file buffers to disk.</span></span>

    public void finalize()

#### <a name="remarks"></a><span data-ttu-id="ae9cf-664">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-664">Remarks</span></span>

<span data-ttu-id="ae9cf-665">AsciiIo オブジェクトは通常そのスコープの終了後に確定されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-665">An AsciiIo object is usually finalized after its scope has ended.</span></span> <span data-ttu-id="ae9cf-666">このメソッドは、通常は直接呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-666">This method is not usually called directly.</span></span> <span data-ttu-id="ae9cf-667">AsciiIo オブジェクトが確定済みになるまで、ファイルに書き込まれる出力は無効です。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-667">Output that is written to the file is not valid until the AsciiIo object is finalized.</span></span>

### <a name="method-new"></a><span data-ttu-id="ae9cf-668">メソッド new</span><span class="sxs-lookup"><span data-stu-id="ae9cf-668">Method new</span></span>

<span data-ttu-id="ae9cf-669">AsciiIo クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-669">Creates an instance of the AsciiIo class.</span></span>

    public void new(str filename, str mode)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-670">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-670">Parameters</span></span>

<span data-ttu-id="ae9cf-671">filename</span><span class="sxs-lookup"><span data-stu-id="ae9cf-671">filename</span></span>  
<span data-ttu-id="ae9cf-672">AsciiIo クラスのこのインスタンスを作成するために使用するモード。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-672">The mode to use to create this instance of the AsciiIo class.</span></span>

<!-- -->

<span data-ttu-id="ae9cf-673">モード</span><span class="sxs-lookup"><span data-stu-id="ae9cf-673">mode</span></span>  
<span data-ttu-id="ae9cf-674">AsciiIo クラスのこのインスタンスを作成するために使用するモード。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-674">The mode to use to create this instance of the AsciiIo class.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae9cf-675">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-675">Remarks</span></span>

<span data-ttu-id="ae9cf-676">攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-676">If an attacker can control input to the new method, a security risk exists.</span></span> <span data-ttu-id="ae9cf-677">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-677">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="ae9cf-678">サーバー上でこのメソッドを呼び出すには、FileIOPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-678">Calls to this method on the server require permission from the FileIOPermission class.</span></span> <span data-ttu-id="ae9cf-679">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-679">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

#### <a name="examples"></a><span data-ttu-id="ae9cf-680">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-680">Examples</span></span>

<span data-ttu-id="ae9cf-681">次の例では、AsciiIo クラスを使用してテキスト ファイルから読み込みます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-681">The following example uses the AsciiIo class to read from a text file.</span></span>

    void AsciiIoExample() 
    { 
        AsciiIo asciiIo; 
        container con; 
        FileIoPermission perm; 

        #define.ExampleFile(@"c:\test.txt") 
        #define.ExampleOpenMode("r") 

        // The AsciiIo.new method runs under code access permission. 
        perm = new FileIoPermission(#ExampleFile, #ExampleOpenMode); 
        if (perm == null) 
        { 
            return; 
        } 

        // Code access permission scope starts here. 
         perm.assert(); 

         asciiIo = new AsciiIo(#ExampleFile, #ExampleOpenMode); 
        if (asciiIo != null) 
        { 
              con = asciiIo.read(); 
        } 
        // Closes the code access permission scope. 
        CodeAccessPermission::revertAssert(); 
    }

## <a name="class-assemblydeploymanager"></a><span data-ttu-id="ae9cf-682">クラス AssemblyDeployManager</span><span class="sxs-lookup"><span data-stu-id="ae9cf-682">Class AssemblyDeployManager</span></span>
    class AssemblyDeployManager extends Object

<span data-ttu-id="ae9cf-683">AssemblyDeployManager クラスを使用すると、.NET 呼び出し時に X++ ランタイムによって使用できる AOS VSAssemblies フォルダーに、AOT Visual Studio プロジェクトに格納されているアセンブリを展開することができます。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-683">The AssemblyDeployManager class lets you deploy the assemblies that are stored in the AOT Visual Studio Projects to the AOS VSAssemblies folder that can be used by the X++ runtime during .NET calls.</span></span>

### <a name="remarks"></a><span data-ttu-id="ae9cf-684">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-684">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="ae9cf-685">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-685">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="ae9cf-686">方法</span><span class="sxs-lookup"><span data-stu-id="ae9cf-686">Methods</span></span>

| <span data-ttu-id="ae9cf-687">方法</span><span class="sxs-lookup"><span data-stu-id="ae9cf-687">Method</span></span>                                                        | <span data-ttu-id="ae9cf-688">説明</span><span class="sxs-lookup"><span data-stu-id="ae9cf-688">Description</span></span>                                                                                             |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae9cf-689">::public static boolean isHotswappingEnabled()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-689">::public static boolean isHotswappingEnabled()</span></span>                | <span data-ttu-id="ae9cf-690">ホット スワップが有効かどうかを示すブール値を返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-690">Returns a Boolean value that indicates whether hot swapping is enabled.</span></span>                                 |
| <span data-ttu-id="ae9cf-691">::public static void deployAssemblyFromPath(str assemblyPath)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-691">::public static void deployAssemblyFromPath(str assemblyPath)</span></span> |                                                                                                         |
| <span data-ttu-id="ae9cf-692">::public static void removeAssemblyFromPath(str assemblyPath)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-692">::public static void removeAssemblyFromPath(str assemblyPath)</span></span> | <span data-ttu-id="ae9cf-693">サーバーへの配置用にマークされた特定のアセンブリを VSAssemblies フォルダーから削除します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-693">Removes one specific assembly that is marked for deployment to the server from the VSAssemblies folder.</span></span> |
| <span data-ttu-id="ae9cf-694">::public static void deployAssemblies()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-694">::public static void deployAssemblies()</span></span>                       | <span data-ttu-id="ae9cf-695">サーバーへの配置用にマークされた特定のアセンブリを VSAssemblies フォルダーに展開します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-695">Deploys one specific assembly that is marked for deployment to server to the VSAssemblies folder.</span></span>       |

### <a name="method-ishotswappingenabled"></a><span data-ttu-id="ae9cf-696">メソッド isHotswappingEnabled</span><span class="sxs-lookup"><span data-stu-id="ae9cf-696">Method isHotswappingEnabled</span></span>

<span data-ttu-id="ae9cf-697">ホット スワップが有効かどうかを示すブール値を返します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-697">Returns a Boolean value that indicates whether hot swapping is enabled.</span></span>

    public static boolean isHotswappingEnabled()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-698">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-698">Return Value</span></span>

<span data-ttu-id="ae9cf-699">ホット スワップが有効かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-699">A Boolean value that indicates whether hot swapping is enabled.</span></span>

### <a name="method-deployassemblyfrompath"></a><span data-ttu-id="ae9cf-700">メソッド deployAssemblyFromPath</span><span class="sxs-lookup"><span data-stu-id="ae9cf-700">Method deployAssemblyFromPath</span></span>

    public static void deployAssemblyFromPath(str assemblyPath)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-701">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-701">Parameters</span></span>

<span data-ttu-id="ae9cf-702">assemblyPath</span><span class="sxs-lookup"><span data-stu-id="ae9cf-702">assemblyPath</span></span>  

### <a name="method-removeassemblyfrompath"></a><span data-ttu-id="ae9cf-703">メソッド removeAssemblyFromPath</span><span class="sxs-lookup"><span data-stu-id="ae9cf-703">Method removeAssemblyFromPath</span></span>

<span data-ttu-id="ae9cf-704">サーバーへの配置用にマークされた特定のアセンブリを VSAssemblies フォルダーから削除します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-704">Removes one specific assembly that is marked for deployment to the server from the VSAssemblies folder.</span></span>

    public static void removeAssemblyFromPath(str assemblyPath)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-705">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-705">Parameters</span></span>

<span data-ttu-id="ae9cf-706">assemblyPath</span><span class="sxs-lookup"><span data-stu-id="ae9cf-706">assemblyPath</span></span>  
<span data-ttu-id="ae9cf-707">アセンブリが格納されている Visual Studio プロジェクト パス。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-707">The Visual Studio Project path where the assembly is stored.</span></span>

### <a name="method-deployassemblies"></a><span data-ttu-id="ae9cf-708">メソッド deployAssemblies</span><span class="sxs-lookup"><span data-stu-id="ae9cf-708">Method deployAssemblies</span></span>

<span data-ttu-id="ae9cf-709">サーバーへの配置用にマークされた特定のアセンブリを VSAssemblies フォルダーに展開します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-709">Deploys one specific assembly that is marked for deployment to server to the VSAssemblies folder.</span></span>

    public static void deployAssemblies()

## <a name="class-asynctaskresult"></a><span data-ttu-id="ae9cf-710">クラス AsyncTaskResult</span><span class="sxs-lookup"><span data-stu-id="ae9cf-710">Class AsyncTaskResult</span></span>
    class AsyncTaskResult extends Object

### <a name="remarks"></a><span data-ttu-id="ae9cf-711">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-711">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="ae9cf-712">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-712">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="ae9cf-713">メソッド</span><span class="sxs-lookup"><span data-stu-id="ae9cf-713">Methods</span></span>

| <span data-ttu-id="ae9cf-714">方法</span><span class="sxs-lookup"><span data-stu-id="ae9cf-714">Method</span></span>                                                                               | <span data-ttu-id="ae9cf-715">説明</span><span class="sxs-lookup"><span data-stu-id="ae9cf-715">Description</span></span> |
|--------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="ae9cf-716">public container getResult()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-716">public container getResult()</span></span>                                                         |             |
| <span data-ttu-id="ae9cf-717">public System.Exception getException()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-717">public System.Exception getException()</span></span>                                               |             |
| <span data-ttu-id="ae9cf-718">public container getInfologData()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-718">public container getInfologData()</span></span>                                                    |             |
| <span data-ttu-id="ae9cf-719">public container getAsyncState()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-719">public container getAsyncState()</span></span>                                                     |             |
| <span data-ttu-id="ae9cf-720">::public static AsyncTaskResult getAsyncTaskResult(System.Threading.Tasks.Task task)</span><span class="sxs-lookup"><span data-stu-id="ae9cf-720">::public static AsyncTaskResult getAsyncTaskResult(System.Threading.Tasks.Task task)</span></span> |             |

### <a name="method-getresult"></a><span data-ttu-id="ae9cf-721">メソッド getResult</span><span class="sxs-lookup"><span data-stu-id="ae9cf-721">Method getResult</span></span>

    public container getResult()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-722">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-722">Return Value</span></span>

### <a name="method-getexception"></a><span data-ttu-id="ae9cf-723">メソッド getException</span><span class="sxs-lookup"><span data-stu-id="ae9cf-723">Method getException</span></span>

    public System.Exception getException()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-724">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-724">Return Value</span></span>

### <a name="method-getinfologdata"></a><span data-ttu-id="ae9cf-725">メソッド getInfologData</span><span class="sxs-lookup"><span data-stu-id="ae9cf-725">Method getInfologData</span></span>

    public container getInfologData()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-726">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-726">Return Value</span></span>

### <a name="method-getasyncstate"></a><span data-ttu-id="ae9cf-727">メソッド getAsyncState</span><span class="sxs-lookup"><span data-stu-id="ae9cf-727">Method getAsyncState</span></span>

    public container getAsyncState()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-728">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-728">Return Value</span></span>

### <a name="method-getasynctaskresult"></a><span data-ttu-id="ae9cf-729">メソッド getAsyncTaskResult</span><span class="sxs-lookup"><span data-stu-id="ae9cf-729">Method getAsyncTaskResult</span></span>

    public static AsyncTaskResult getAsyncTaskResult(System.Threading.Tasks.Task task)

#### <a name="parameters"></a><span data-ttu-id="ae9cf-730">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae9cf-730">Parameters</span></span>

<span data-ttu-id="ae9cf-731">タスク</span><span class="sxs-lookup"><span data-stu-id="ae9cf-731">task</span></span>  

#### <a name="return-value"></a><span data-ttu-id="ae9cf-732">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-732">Return Value</span></span>

## <a name="class-axaptacomconnectormonitor"></a><span data-ttu-id="ae9cf-733">クラス AxaptaCOMConnectorMonitor</span><span class="sxs-lookup"><span data-stu-id="ae9cf-733">Class AxaptaCOMConnectorMonitor</span></span>
    class AxaptaCOMConnectorMonitor extends Object

<span data-ttu-id="ae9cf-734">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-734">Microsoft internal use only.</span></span>

### <a name="remarks"></a><span data-ttu-id="ae9cf-735">備考</span><span class="sxs-lookup"><span data-stu-id="ae9cf-735">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="ae9cf-736">例</span><span class="sxs-lookup"><span data-stu-id="ae9cf-736">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="ae9cf-737">メソッド</span><span class="sxs-lookup"><span data-stu-id="ae9cf-737">Methods</span></span>

| <span data-ttu-id="ae9cf-738">方法</span><span class="sxs-lookup"><span data-stu-id="ae9cf-738">Method</span></span>                                     | <span data-ttu-id="ae9cf-739">説明</span><span class="sxs-lookup"><span data-stu-id="ae9cf-739">Description</span></span>                                                        |
|--------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ae9cf-740">public int getBufferCount()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-740">public int getBufferCount()</span></span>                |                                                                    |
| <span data-ttu-id="ae9cf-741">public str getCOMRegistration()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-741">public str getCOMRegistration()</span></span>            |                                                                    |
| <span data-ttu-id="ae9cf-742">public int getContainerCount()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-742">public int getContainerCount()</span></span>             |                                                                    |
| <span data-ttu-id="ae9cf-743">public int getLoggedOnAxaptaObjectCount()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-743">public int getLoggedOnAxaptaObjectCount()</span></span>  |                                                                    |
| <span data-ttu-id="ae9cf-744">public int getObjectCount()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-744">public int getObjectCount()</span></span>                |                                                                    |
| <span data-ttu-id="ae9cf-745">public int getRecordCount()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-745">public int getRecordCount()</span></span>                |                                                                    |
| <span data-ttu-id="ae9cf-746">public int getReferenceCount()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-746">public int getReferenceCount()</span></span>             |                                                                    |
| <span data-ttu-id="ae9cf-747">public boolean isAxaptaCOMConnector()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-747">public boolean isAxaptaCOMConnector()</span></span>      |                                                                    |
| <span data-ttu-id="ae9cf-748">public boolean isAxaptaInternetConnector()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-748">public boolean isAxaptaInternetConnector()</span></span> |                                                                    |
| <span data-ttu-id="ae9cf-749">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-749">public void finalize()</span></span>                     | <span data-ttu-id="ae9cf-750">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-750">Microsoftinternal use only.</span></span>                                        |
| <span data-ttu-id="ae9cf-751">public void new()</span><span class="sxs-lookup"><span data-stu-id="ae9cf-751">public void new()</span></span>                          | <span data-ttu-id="ae9cf-752">AxaptaCOMConnectorMonitor クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-752">Initializes a new instance of the AxaptaCOMConnectorMonitor class.</span></span> |

### <a name="method-getbuffercount"></a><span data-ttu-id="ae9cf-753">メソッド getBufferCount</span><span class="sxs-lookup"><span data-stu-id="ae9cf-753">Method getBufferCount</span></span>

    public int getBufferCount()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-754">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-754">Return Value</span></span>

### <a name="method-getcomregistration"></a><span data-ttu-id="ae9cf-755">メソッド getCOMRegistration</span><span class="sxs-lookup"><span data-stu-id="ae9cf-755">Method getCOMRegistration</span></span>

    public str getCOMRegistration()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-756">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-756">Return Value</span></span>

### <a name="method-getcontainercount"></a><span data-ttu-id="ae9cf-757">メソッド getContainerCount</span><span class="sxs-lookup"><span data-stu-id="ae9cf-757">Method getContainerCount</span></span>

    public int getContainerCount()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-758">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-758">Return Value</span></span>

### <a name="method-getloggedonaxaptaobjectcount"></a><span data-ttu-id="ae9cf-759">メソッド getLoggedOnAxaptaObjectCount</span><span class="sxs-lookup"><span data-stu-id="ae9cf-759">Method getLoggedOnAxaptaObjectCount</span></span>

    public int getLoggedOnAxaptaObjectCount()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-760">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-760">Return Value</span></span>

### <a name="method-getobjectcount"></a><span data-ttu-id="ae9cf-761">メソッド getObjectCount</span><span class="sxs-lookup"><span data-stu-id="ae9cf-761">Method getObjectCount</span></span>

    public int getObjectCount()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-762">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-762">Return Value</span></span>

### <a name="method-getrecordcount"></a><span data-ttu-id="ae9cf-763">メソッド getRecordCount</span><span class="sxs-lookup"><span data-stu-id="ae9cf-763">Method getRecordCount</span></span>

    public int getRecordCount()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-764">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-764">Return Value</span></span>

### <a name="method-getreferencecount"></a><span data-ttu-id="ae9cf-765">メソッド getReferenceCount</span><span class="sxs-lookup"><span data-stu-id="ae9cf-765">Method getReferenceCount</span></span>

    public int getReferenceCount()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-766">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-766">Return Value</span></span>

### <a name="method-isaxaptacomconnector"></a><span data-ttu-id="ae9cf-767">メソッド isAxaptaCOMConnector</span><span class="sxs-lookup"><span data-stu-id="ae9cf-767">Method isAxaptaCOMConnector</span></span>

    public boolean isAxaptaCOMConnector()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-768">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-768">Return Value</span></span>

### <a name="method-isaxaptainternetconnector"></a><span data-ttu-id="ae9cf-769">メソッド isAxaptaInternetConnector</span><span class="sxs-lookup"><span data-stu-id="ae9cf-769">Method isAxaptaInternetConnector</span></span>

    public boolean isAxaptaInternetConnector()

#### <a name="return-value"></a><span data-ttu-id="ae9cf-770">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae9cf-770">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="ae9cf-771">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="ae9cf-771">Method finalize</span></span>

<span data-ttu-id="ae9cf-772">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-772">Microsoftinternal use only.</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="ae9cf-773">メソッド new</span><span class="sxs-lookup"><span data-stu-id="ae9cf-773">Method new</span></span>

<span data-ttu-id="ae9cf-774">AxaptaCOMConnectorMonitor クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ae9cf-774">Initializes a new instance of the AxaptaCOMConnectorMonitor class.</span></span>

    public void new()



