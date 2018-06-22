---
title: "U クラス"
description: "文字 U で始まるシステム API クラス。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 51691
ms.assetid: 92bfbb9c-4f45-464a-8ccb-71fb227780fe
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fc1419958ec115271fbc1532d9d556ecaf835d2c
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="u-classes"></a><span data-ttu-id="14b96-103">U クラス</span><span class="sxs-lookup"><span data-stu-id="14b96-103">U Classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14b96-104">文字 U で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="14b96-104">System API classes that start with the letter U.</span></span>

<a name="class-unitofwork"></a><span data-ttu-id="14b96-105">クラス UnitofWork</span><span class="sxs-lookup"><span data-stu-id="14b96-105">Class UnitofWork</span></span>
----------------

    class UnitofWork extends Object

### <a name="remarks"></a><span data-ttu-id="14b96-106">備考</span><span class="sxs-lookup"><span data-stu-id="14b96-106">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="14b96-107">例</span><span class="sxs-lookup"><span data-stu-id="14b96-107">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="14b96-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="14b96-108">Methods</span></span>

| <span data-ttu-id="14b96-109">方法</span><span class="sxs-lookup"><span data-stu-id="14b96-109">Method</span></span>                                                       | <span data-ttu-id="14b96-110">説明</span><span class="sxs-lookup"><span data-stu-id="14b96-110">Description</span></span>                                         |
|--------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="14b96-111">public boolean getByKey(Common record)</span><span class="sxs-lookup"><span data-stu-id="14b96-111">public boolean getByKey(Common record)</span></span>                       |                                                     |
| <span data-ttu-id="14b96-112">public void updateonSaveChanges(Common record)</span><span class="sxs-lookup"><span data-stu-id="14b96-112">public void updateonSaveChanges(Common record)</span></span>               |                                                     |
| <span data-ttu-id="14b96-113">public void saveChanges(\[UserConnection user\_connection\])</span><span class="sxs-lookup"><span data-stu-id="14b96-113">public void saveChanges(\[UserConnection user\_connection\])</span></span> |                                                     |
| <span data-ttu-id="14b96-114">public void deleteonSaveChanges(Common record)</span><span class="sxs-lookup"><span data-stu-id="14b96-114">public void deleteonSaveChanges(Common record)</span></span>               |                                                     |
| <span data-ttu-id="14b96-115">public void insertonSaveChanges(Common record)</span><span class="sxs-lookup"><span data-stu-id="14b96-115">public void insertonSaveChanges(Common record)</span></span>               |                                                     |
| <span data-ttu-id="14b96-116">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="14b96-116">public void finalize()</span></span>                                       |                                                     |
| <span data-ttu-id="14b96-117">public void new()</span><span class="sxs-lookup"><span data-stu-id="14b96-117">public void new()</span></span>                                            | <span data-ttu-id="14b96-118">UnitofWork クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="14b96-118">Initializes a new instance of the UnitofWork class.</span></span> |
| <span data-ttu-id="14b96-119">public void clear()</span><span class="sxs-lookup"><span data-stu-id="14b96-119">public void clear()</span></span>                                          |                                                     |

### <a name="method-getbykey"></a><span data-ttu-id="14b96-120">メソッド getByKey</span><span class="sxs-lookup"><span data-stu-id="14b96-120">Method getByKey</span></span>

    public boolean getByKey(Common record)

#### <a name="parameters"></a><span data-ttu-id="14b96-121">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14b96-121">Parameters</span></span>

<span data-ttu-id="14b96-122">記録</span><span class="sxs-lookup"><span data-stu-id="14b96-122">record</span></span>  

#### <a name="return-value"></a><span data-ttu-id="14b96-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="14b96-123">Return Value</span></span>

### <a name="method-updateonsavechanges"></a><span data-ttu-id="14b96-124">メソッド updateonSaveChanges</span><span class="sxs-lookup"><span data-stu-id="14b96-124">Method updateonSaveChanges</span></span>

    public void updateonSaveChanges(Common record)

#### <a name="parameters"></a><span data-ttu-id="14b96-125">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14b96-125">Parameters</span></span>

<span data-ttu-id="14b96-126">記録</span><span class="sxs-lookup"><span data-stu-id="14b96-126">record</span></span>  

### <a name="method-savechanges"></a><span data-ttu-id="14b96-127">メソッド saveChanges</span><span class="sxs-lookup"><span data-stu-id="14b96-127">Method saveChanges</span></span>

    public void saveChanges([UserConnection user_connection])

#### <a name="parameters"></a><span data-ttu-id="14b96-128">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14b96-128">Parameters</span></span>

<span data-ttu-id="14b96-129">user\_connection</span><span class="sxs-lookup"><span data-stu-id="14b96-129">user\_connection</span></span>  

### <a name="method-deleteonsavechanges"></a><span data-ttu-id="14b96-130">メソッド deleteonSaveChanges</span><span class="sxs-lookup"><span data-stu-id="14b96-130">Method deleteonSaveChanges</span></span>

    public void deleteonSaveChanges(Common record)

#### <a name="parameters"></a><span data-ttu-id="14b96-131">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14b96-131">Parameters</span></span>

<span data-ttu-id="14b96-132">記録</span><span class="sxs-lookup"><span data-stu-id="14b96-132">record</span></span>  

### <a name="method-insertonsavechanges"></a><span data-ttu-id="14b96-133">メソッド insertonSaveChanges</span><span class="sxs-lookup"><span data-stu-id="14b96-133">Method insertonSaveChanges</span></span>

    public void insertonSaveChanges(Common record)

#### <a name="parameters"></a><span data-ttu-id="14b96-134">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14b96-134">Parameters</span></span>

<span data-ttu-id="14b96-135">記録</span><span class="sxs-lookup"><span data-stu-id="14b96-135">record</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="14b96-136">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="14b96-136">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="14b96-137">メソッド new</span><span class="sxs-lookup"><span data-stu-id="14b96-137">Method new</span></span>

<span data-ttu-id="14b96-138">UnitofWork クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="14b96-138">Initializes a new instance of the UnitofWork class.</span></span>

    public void new()

### <a name="method-clear"></a><span data-ttu-id="14b96-139">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="14b96-139">Method clear</span></span>

    public void clear()

## <a name="class-userconnection"></a><span data-ttu-id="14b96-140">クラス UserConnection</span><span class="sxs-lookup"><span data-stu-id="14b96-140">Class UserConnection</span></span>
    class UserConnection extends Connection

<span data-ttu-id="14b96-141">UserConnection クラスは、主要な接続と同じログオン プロパティに基づいて、SQL データベースへの補助接続を表します。</span><span class="sxs-lookup"><span data-stu-id="14b96-141">The UserConnection class represents an auxiliary connection to the SQL database, based on the same logon properties as the main connection.</span></span>

### <a name="remarks"></a><span data-ttu-id="14b96-142">備考</span><span class="sxs-lookup"><span data-stu-id="14b96-142">Remarks</span></span>

<span data-ttu-id="14b96-143">SQL ステートメントが実行され、結果が UserConnection クラスのコンテキストで返されます。</span><span class="sxs-lookup"><span data-stu-id="14b96-143">SQL statements are executed, and results are returned in the context of a UserConnection class.</span></span> <span data-ttu-id="14b96-144">UserConnection クラスを使用して、別個のトランザクション スコープを取得できます。</span><span class="sxs-lookup"><span data-stu-id="14b96-144">The UserConnection class can be used to obtain a separate transaction scope.</span></span>

### <a name="examples"></a><span data-ttu-id="14b96-145">例</span><span class="sxs-lookup"><span data-stu-id="14b96-145">Examples</span></span>

    static void example()  
    { 
        UserConnection Con; 
        Statement Stmt; 
        Str sql; 
        ResultSet R; 
        SqlStatementExecutePermission perm; 
        Con = new UserConnection(); 
        sql = 'SELECT VALUE FROM SQLSYSTEMVARIABLES'; 
        Stmt = Con.createStatement(); 
        perm = new SqlStatementExecutePermission(sql); 
        // Check for permission to use the statement. 
        perm.assert(); 
        R = Stmt.executeQuery(sql); 
        while ( R.next() ) 
        { 
            print R.getString(1); 
        } 
    }

### <a name="methods"></a><span data-ttu-id="14b96-146">メソッド</span><span class="sxs-lookup"><span data-stu-id="14b96-146">Methods</span></span>

| <span data-ttu-id="14b96-147">方法</span><span class="sxs-lookup"><span data-stu-id="14b96-147">Method</span></span>                                                | <span data-ttu-id="14b96-148">説明</span><span class="sxs-lookup"><span data-stu-id="14b96-148">Description</span></span>                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="14b96-149">public void new(\[boolean generateNewTransactionID\])</span><span class="sxs-lookup"><span data-stu-id="14b96-149">public void new(\[boolean generateNewTransactionID\])</span></span> | <span data-ttu-id="14b96-150">Connection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="14b96-150">Initializes a new instance of the Connection class.</span></span> |

### <a name="method-new"></a><span data-ttu-id="14b96-151">メソッド new</span><span class="sxs-lookup"><span data-stu-id="14b96-151">Method new</span></span>

<span data-ttu-id="14b96-152">Connection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="14b96-152">Initializes a new instance of the Connection class.</span></span>

    public void new([boolean generateNewTransactionID])

#### <a name="parameters"></a><span data-ttu-id="14b96-153">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14b96-153">Parameters</span></span>

<span data-ttu-id="14b96-154">generateNewTransactionID</span><span class="sxs-lookup"><span data-stu-id="14b96-154">generateNewTransactionID</span></span>  

## <a name="class-usermenulist"></a><span data-ttu-id="14b96-155">クラス UserMenuList</span><span class="sxs-lookup"><span data-stu-id="14b96-155">Class UserMenuList</span></span>
    class UserMenuList extends TreeNode

<span data-ttu-id="14b96-156">UserMenuList クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="14b96-156">The UserMenuList class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="14b96-157">備考</span><span class="sxs-lookup"><span data-stu-id="14b96-157">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="14b96-158">例</span><span class="sxs-lookup"><span data-stu-id="14b96-158">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="14b96-159">メソッド</span><span class="sxs-lookup"><span data-stu-id="14b96-159">Methods</span></span>

| <span data-ttu-id="14b96-160">方法</span><span class="sxs-lookup"><span data-stu-id="14b96-160">Method</span></span>                               | <span data-ttu-id="14b96-161">説明</span><span class="sxs-lookup"><span data-stu-id="14b96-161">Description</span></span> |
|--------------------------------------|-------------|
| <span data-ttu-id="14b96-162">public void createMenu(\[str name\])</span><span class="sxs-lookup"><span data-stu-id="14b96-162">public void createMenu(\[str name\])</span></span> |             |

### <a name="method-createmenu"></a><span data-ttu-id="14b96-163">メソッド createMenu</span><span class="sxs-lookup"><span data-stu-id="14b96-163">Method createMenu</span></span>

    public void createMenu([str name])

#### <a name="parameters"></a><span data-ttu-id="14b96-164">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14b96-164">Parameters</span></span>

<span data-ttu-id="14b96-165">名前</span><span class="sxs-lookup"><span data-stu-id="14b96-165">name</span></span>  

## <a name="class-usersetup"></a><span data-ttu-id="14b96-166">クラス UserSetup</span><span class="sxs-lookup"><span data-stu-id="14b96-166">Class UserSetup</span></span>
    class UserSetup extends TreeNode

<span data-ttu-id="14b96-167">UserSetup クラスは、ユーザー パラメーターを設定するためのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="14b96-167">The UserSetup class provides an interface for setting user parameters.</span></span>

### <a name="remarks"></a><span data-ttu-id="14b96-168">備考</span><span class="sxs-lookup"><span data-stu-id="14b96-168">Remarks</span></span>

<span data-ttu-id="14b96-169">このクラスは、主に SysUserSetup フォームで使用されます。</span><span class="sxs-lookup"><span data-stu-id="14b96-169">This class is used mainly in the SysUserSetup form.</span></span> <span data-ttu-id="14b96-170">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="14b96-170">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="14b96-171">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="14b96-171">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="14b96-172">例</span><span class="sxs-lookup"><span data-stu-id="14b96-172">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="14b96-173">メソッド</span><span class="sxs-lookup"><span data-stu-id="14b96-173">Methods</span></span>

| <span data-ttu-id="14b96-174">方法</span><span class="sxs-lookup"><span data-stu-id="14b96-174">Method</span></span>                                  | <span data-ttu-id="14b96-175">説明</span><span class="sxs-lookup"><span data-stu-id="14b96-175">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="14b96-176">public boolean xRef(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="14b96-176">public boolean xRef(\[boolean enable\])</span></span> |             |
| <span data-ttu-id="14b96-177">public void setUserSetup(Common cursor)</span><span class="sxs-lookup"><span data-stu-id="14b96-177">public void setUserSetup(Common cursor)</span></span> |             |
| <span data-ttu-id="14b96-178">public void setDefaults(Common cursor)</span><span class="sxs-lookup"><span data-stu-id="14b96-178">public void setDefaults(Common cursor)</span></span>  |             |

### <a name="method-xref"></a><span data-ttu-id="14b96-179">メソッド xRef</span><span class="sxs-lookup"><span data-stu-id="14b96-179">Method xRef</span></span>

    public boolean xRef([boolean enable])

#### <a name="parameters"></a><span data-ttu-id="14b96-180">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14b96-180">Parameters</span></span>

<span data-ttu-id="14b96-181">enable</span><span class="sxs-lookup"><span data-stu-id="14b96-181">enable</span></span>  

#### <a name="return-value"></a><span data-ttu-id="14b96-182">戻り値</span><span class="sxs-lookup"><span data-stu-id="14b96-182">Return Value</span></span>

### <a name="method-setusersetup"></a><span data-ttu-id="14b96-183">メソッド setUserSetup</span><span class="sxs-lookup"><span data-stu-id="14b96-183">Method setUserSetup</span></span>

    public void setUserSetup(Common cursor)

#### <a name="parameters"></a><span data-ttu-id="14b96-184">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14b96-184">Parameters</span></span>

<span data-ttu-id="14b96-185">cursor</span><span class="sxs-lookup"><span data-stu-id="14b96-185">cursor</span></span>  

### <a name="method-setdefaults"></a><span data-ttu-id="14b96-186">メソッド setDefaults</span><span class="sxs-lookup"><span data-stu-id="14b96-186">Method setDefaults</span></span>

    public void setDefaults(Common cursor)

#### <a name="parameters"></a><span data-ttu-id="14b96-187">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14b96-187">Parameters</span></span>

<span data-ttu-id="14b96-188">cursor</span><span class="sxs-lookup"><span data-stu-id="14b96-188">cursor</span></span>  

## <a name="class-utilfile"></a><span data-ttu-id="14b96-189">クラス UtilFile</span><span class="sxs-lookup"><span data-stu-id="14b96-189">Class UtilFile</span></span>
    class UtilFile extends Object

### <a name="remarks"></a><span data-ttu-id="14b96-190">備考</span><span class="sxs-lookup"><span data-stu-id="14b96-190">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="14b96-191">例</span><span class="sxs-lookup"><span data-stu-id="14b96-191">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="14b96-192">メソッド</span><span class="sxs-lookup"><span data-stu-id="14b96-192">Methods</span></span>

| <span data-ttu-id="14b96-193">方法</span><span class="sxs-lookup"><span data-stu-id="14b96-193">Method</span></span>                                                      | <span data-ttu-id="14b96-194">説明</span><span class="sxs-lookup"><span data-stu-id="14b96-194">Description</span></span>                                                      |
|-------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="14b96-195">public boolean aodFileExist(UtilEntryLevel layer)</span><span class="sxs-lookup"><span data-stu-id="14b96-195">public boolean aodFileExist(UtilEntryLevel layer)</span></span>           |                                                                  |
| <span data-ttu-id="14b96-196">public int importAODFile(UtilEntryLevel layer, int modelId)</span><span class="sxs-lookup"><span data-stu-id="14b96-196">public int importAODFile(UtilEntryLevel layer, int modelId)</span></span> |                                                                  |
| <span data-ttu-id="14b96-197">public str layers()</span><span class="sxs-lookup"><span data-stu-id="14b96-197">public str layers()</span></span>                                         |                                                                  |
| <span data-ttu-id="14b96-198">public boolean needReindex()</span><span class="sxs-lookup"><span data-stu-id="14b96-198">public boolean needReindex()</span></span>                                |                                                                  |
| <span data-ttu-id="14b96-199">public void check(str layer, str action)</span><span class="sxs-lookup"><span data-stu-id="14b96-199">public void check(str layer, str action)</span></span>                    |                                                                  |
| <span data-ttu-id="14b96-200">public void new(str fileType)</span><span class="sxs-lookup"><span data-stu-id="14b96-200">public void new(str fileType)</span></span>                               | <span data-ttu-id="14b96-201">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="14b96-201">Initializes a new instance of the Object class.</span></span>                  |
| <span data-ttu-id="14b96-202">public void reindex()</span><span class="sxs-lookup"><span data-stu-id="14b96-202">public void reindex()</span></span>                                       | <span data-ttu-id="14b96-203">X++ コードとメタデータの作成、読み取り、更新、および削除ができます。</span><span class="sxs-lookup"><span data-stu-id="14b96-203">Lets you create, read, update, and delete X++ code and metadata.</span></span> |
| <span data-ttu-id="14b96-204">public void flushCache()</span><span class="sxs-lookup"><span data-stu-id="14b96-204">public void flushCache()</span></span>                                    |                                                                  |

### <a name="method-aodfileexist"></a><span data-ttu-id="14b96-205">メソッド aodFileExist</span><span class="sxs-lookup"><span data-stu-id="14b96-205">Method aodFileExist</span></span>

    public boolean aodFileExist(UtilEntryLevel layer)

#### <a name="parameters"></a><span data-ttu-id="14b96-206">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14b96-206">Parameters</span></span>

<span data-ttu-id="14b96-207"> レイヤー</span><span class="sxs-lookup"><span data-stu-id="14b96-207">layer</span></span>  

#### <a name="return-value"></a><span data-ttu-id="14b96-208">戻り値</span><span class="sxs-lookup"><span data-stu-id="14b96-208">Return Value</span></span>

### <a name="method-importaodfile"></a><span data-ttu-id="14b96-209">メソッド importAODFile</span><span class="sxs-lookup"><span data-stu-id="14b96-209">Method importAODFile</span></span>

    public int importAODFile(UtilEntryLevel layer, int modelId)

#### <a name="parameters"></a><span data-ttu-id="14b96-210">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14b96-210">Parameters</span></span>

<span data-ttu-id="14b96-211"> レイヤー</span><span class="sxs-lookup"><span data-stu-id="14b96-211">layer</span></span>  

<!-- -->

<span data-ttu-id="14b96-212">modelId</span><span class="sxs-lookup"><span data-stu-id="14b96-212">modelId</span></span>  

#### <a name="return-value"></a><span data-ttu-id="14b96-213">戻り値</span><span class="sxs-lookup"><span data-stu-id="14b96-213">Return Value</span></span>

### <a name="method-layers"></a><span data-ttu-id="14b96-214">メソッド layers</span><span class="sxs-lookup"><span data-stu-id="14b96-214">Method layers</span></span>

    public str layers()

#### <a name="return-value"></a><span data-ttu-id="14b96-215">戻り値</span><span class="sxs-lookup"><span data-stu-id="14b96-215">Return Value</span></span>

### <a name="method-needreindex"></a><span data-ttu-id="14b96-216">メソッド needReindex</span><span class="sxs-lookup"><span data-stu-id="14b96-216">Method needReindex</span></span>

    public boolean needReindex()

#### <a name="return-value"></a><span data-ttu-id="14b96-217">戻り値</span><span class="sxs-lookup"><span data-stu-id="14b96-217">Return Value</span></span>

### <a name="method-check"></a><span data-ttu-id="14b96-218">メソッド check</span><span class="sxs-lookup"><span data-stu-id="14b96-218">Method check</span></span>

    public void check(str layer, str action)

#### <a name="parameters"></a><span data-ttu-id="14b96-219">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14b96-219">Parameters</span></span>

<span data-ttu-id="14b96-220"> レイヤー</span><span class="sxs-lookup"><span data-stu-id="14b96-220">layer</span></span>  

<!-- -->

<span data-ttu-id="14b96-221">アクション</span><span class="sxs-lookup"><span data-stu-id="14b96-221">action</span></span>  

### <a name="method-new"></a><span data-ttu-id="14b96-222">メソッド new</span><span class="sxs-lookup"><span data-stu-id="14b96-222">Method new</span></span>

<span data-ttu-id="14b96-223">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="14b96-223">Initializes a new instance of the Object class.</span></span>

    public void new(str fileType)

#### <a name="parameters"></a><span data-ttu-id="14b96-224">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14b96-224">Parameters</span></span>

<span data-ttu-id="14b96-225">fileType</span><span class="sxs-lookup"><span data-stu-id="14b96-225">fileType</span></span>  

### <a name="method-reindex"></a><span data-ttu-id="14b96-226">メソッド reindex</span><span class="sxs-lookup"><span data-stu-id="14b96-226">Method reindex</span></span>

<span data-ttu-id="14b96-227">X++ コードとメタデータの作成、読み取り、更新、および削除ができます。</span><span class="sxs-lookup"><span data-stu-id="14b96-227">Lets you create, read, update, and delete X++ code and metadata.</span></span>

    public void reindex()

#### <a name="remarks"></a><span data-ttu-id="14b96-228">備考</span><span class="sxs-lookup"><span data-stu-id="14b96-228">Remarks</span></span>

<span data-ttu-id="14b96-229">この API を呼び出す前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="14b96-229">Make sure that the user has access to the development security key (SysDevelopment) before you call this API.</span></span>

#### <a name="examples"></a><span data-ttu-id="14b96-230">例</span><span class="sxs-lookup"><span data-stu-id="14b96-230">Examples</span></span>

<span data-ttu-id="14b96-231">次の例では、UtilFile.reindex メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="14b96-231">The following example calls the UtilFile.reindex method.</span></span> <span data-ttu-id="14b96-232">変更を実行する前に、ユーザーが必要なセキュリティ キーを持っているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="14b96-232">It checks whether the user has the required security key before you perform a modification.</span></span>

    server static public void Main(Args _args) 
    { 
        UtilFile u; 
        u = new UtilFile("util"); 
        if (u) 
        { 
            u.reindex(); 
        } 
    }

### <a name="method-flushcache"></a><span data-ttu-id="14b96-233">メソッド flushCache</span><span class="sxs-lookup"><span data-stu-id="14b96-233">Method flushCache</span></span>

    public void flushCache()




