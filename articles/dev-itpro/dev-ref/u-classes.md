---
title: U クラス
description: 文字 U で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 01/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 51691
ms.assetid: 92bfbb9c-4f45-464a-8ccb-71fb227780fe
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d2d1f5bdf10c538b3d398bc2ac22d23498da1f5
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833648"
---
# <a name="u-classes"></a><span data-ttu-id="e9d6c-103">U クラス</span><span class="sxs-lookup"><span data-stu-id="e9d6c-103">U classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9d6c-104">文字 U で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-104">System API classes that start with the letter U.</span></span>

<a name="class-unitofwork"></a><span data-ttu-id="e9d6c-105">クラス UnitofWork</span><span class="sxs-lookup"><span data-stu-id="e9d6c-105">Class UnitofWork</span></span>
----------------

    class UnitofWork extends Object

### <a name="remarks"></a><span data-ttu-id="e9d6c-106">備考</span><span class="sxs-lookup"><span data-stu-id="e9d6c-106">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="e9d6c-107">例</span><span class="sxs-lookup"><span data-stu-id="e9d6c-107">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="e9d6c-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="e9d6c-108">Methods</span></span>

| <span data-ttu-id="e9d6c-109">方法</span><span class="sxs-lookup"><span data-stu-id="e9d6c-109">Method</span></span>                                                       | <span data-ttu-id="e9d6c-110">説明</span><span class="sxs-lookup"><span data-stu-id="e9d6c-110">Description</span></span>                                         |
|--------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="e9d6c-111">public boolean getByKey(Common record)</span><span class="sxs-lookup"><span data-stu-id="e9d6c-111">public boolean getByKey(Common record)</span></span>                       |                                                     |
| <span data-ttu-id="e9d6c-112">public void updateonSaveChanges(Common record)</span><span class="sxs-lookup"><span data-stu-id="e9d6c-112">public void updateonSaveChanges(Common record)</span></span>               |                                                     |
| <span data-ttu-id="e9d6c-113">public void saveChanges(\[UserConnection user\_connection\])</span><span class="sxs-lookup"><span data-stu-id="e9d6c-113">public void saveChanges(\[UserConnection user\_connection\])</span></span> |                                                     |
| <span data-ttu-id="e9d6c-114">public void deleteonSaveChanges(Common record)</span><span class="sxs-lookup"><span data-stu-id="e9d6c-114">public void deleteonSaveChanges(Common record)</span></span>               |                                                     |
| <span data-ttu-id="e9d6c-115">public void insertonSaveChanges(Common record)</span><span class="sxs-lookup"><span data-stu-id="e9d6c-115">public void insertonSaveChanges(Common record)</span></span>               |                                                     |
| <span data-ttu-id="e9d6c-116">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="e9d6c-116">public void finalize()</span></span>                                       |                                                     |
| <span data-ttu-id="e9d6c-117">public void new()</span><span class="sxs-lookup"><span data-stu-id="e9d6c-117">public void new()</span></span>                                            | <span data-ttu-id="e9d6c-118">UnitofWork クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-118">Initializes a new instance of the UnitofWork class.</span></span> |
| <span data-ttu-id="e9d6c-119">public void clear()</span><span class="sxs-lookup"><span data-stu-id="e9d6c-119">public void clear()</span></span>                                          |                                                     |

### <a name="method-getbykey"></a><span data-ttu-id="e9d6c-120">メソッド getByKey</span><span class="sxs-lookup"><span data-stu-id="e9d6c-120">Method getByKey</span></span>

    public boolean getByKey(Common record)

#### <a name="parameters"></a><span data-ttu-id="e9d6c-121">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9d6c-121">Parameters</span></span>

<span data-ttu-id="e9d6c-122">記録</span><span class="sxs-lookup"><span data-stu-id="e9d6c-122">record</span></span>  

#### <a name="return-value"></a><span data-ttu-id="e9d6c-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="e9d6c-123">Return Value</span></span>

### <a name="method-updateonsavechanges"></a><span data-ttu-id="e9d6c-124">メソッド updateonSaveChanges</span><span class="sxs-lookup"><span data-stu-id="e9d6c-124">Method updateonSaveChanges</span></span>

    public void updateonSaveChanges(Common record)

#### <a name="parameters"></a><span data-ttu-id="e9d6c-125">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9d6c-125">Parameters</span></span>

<span data-ttu-id="e9d6c-126">記録</span><span class="sxs-lookup"><span data-stu-id="e9d6c-126">record</span></span>  

### <a name="method-savechanges"></a><span data-ttu-id="e9d6c-127">メソッド saveChanges</span><span class="sxs-lookup"><span data-stu-id="e9d6c-127">Method saveChanges</span></span>

    public void saveChanges([UserConnection user_connection])

#### <a name="parameters"></a><span data-ttu-id="e9d6c-128">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9d6c-128">Parameters</span></span>

<span data-ttu-id="e9d6c-129">user\_connection</span><span class="sxs-lookup"><span data-stu-id="e9d6c-129">user\_connection</span></span>  

### <a name="method-deleteonsavechanges"></a><span data-ttu-id="e9d6c-130">メソッド deleteonSaveChanges</span><span class="sxs-lookup"><span data-stu-id="e9d6c-130">Method deleteonSaveChanges</span></span>

    public void deleteonSaveChanges(Common record)

#### <a name="parameters"></a><span data-ttu-id="e9d6c-131">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9d6c-131">Parameters</span></span>

<span data-ttu-id="e9d6c-132">記録</span><span class="sxs-lookup"><span data-stu-id="e9d6c-132">record</span></span>  

### <a name="method-insertonsavechanges"></a><span data-ttu-id="e9d6c-133">メソッド insertonSaveChanges</span><span class="sxs-lookup"><span data-stu-id="e9d6c-133">Method insertonSaveChanges</span></span>

    public void insertonSaveChanges(Common record)

#### <a name="parameters"></a><span data-ttu-id="e9d6c-134">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9d6c-134">Parameters</span></span>

<span data-ttu-id="e9d6c-135">記録</span><span class="sxs-lookup"><span data-stu-id="e9d6c-135">record</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="e9d6c-136">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="e9d6c-136">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="e9d6c-137">メソッド new</span><span class="sxs-lookup"><span data-stu-id="e9d6c-137">Method new</span></span>

<span data-ttu-id="e9d6c-138">UnitofWork クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-138">Initializes a new instance of the UnitofWork class.</span></span>

    public void new()

### <a name="method-clear"></a><span data-ttu-id="e9d6c-139">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="e9d6c-139">Method clear</span></span>

    public void clear()

## <a name="class-userconnection"></a><span data-ttu-id="e9d6c-140">クラス UserConnection</span><span class="sxs-lookup"><span data-stu-id="e9d6c-140">Class UserConnection</span></span>
    class UserConnection extends Connection

<span data-ttu-id="e9d6c-141">UserConnection クラスは、主要な接続と同じログオン プロパティに基づいて、SQL データベースへの補助接続を表します。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-141">The UserConnection class represents an auxiliary connection to the SQL database, based on the same logon properties as the main connection.</span></span>

### <a name="remarks"></a><span data-ttu-id="e9d6c-142">備考</span><span class="sxs-lookup"><span data-stu-id="e9d6c-142">Remarks</span></span>

<span data-ttu-id="e9d6c-143">SQL ステートメントが実行され、結果が UserConnection クラスのコンテキストで返されます。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-143">SQL statements are executed, and results are returned in the context of a UserConnection class.</span></span> <span data-ttu-id="e9d6c-144">UserConnection クラスを使用して、別個のトランザクション スコープを取得できます。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-144">The UserConnection class can be used to obtain a separate transaction scope.</span></span>

<span data-ttu-id="e9d6c-145">注記: ユーザー接続リークを防ぐため、finally ブロックで Userconnection.finalize() を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-145">Note: Userconnection.finalize() needs to be called in the finally block to prevent user connection leak.</span></span>  <span data-ttu-id="e9d6c-146">オープン ユーザー接続の数がサーバー上で制限されており、制限に達すると、それ以上接続を開くことができなくなり、ビジネス ロジックのエラーになる可能性があります</span><span class="sxs-lookup"><span data-stu-id="e9d6c-146">Number of open user connections is limited on the server, when it reaches the limit, no more connections can be opened, which can leads to business logic failures</span></span>

### <a name="examples"></a><span data-ttu-id="e9d6c-147">例</span><span class="sxs-lookup"><span data-stu-id="e9d6c-147">Examples</span></span>

    static void example()  
    { 
        UserConnection Con;
        try
        {
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
        finally
        {
            con.finalize();
        }
     }

### <a name="methods"></a><span data-ttu-id="e9d6c-148">方法</span><span class="sxs-lookup"><span data-stu-id="e9d6c-148">Methods</span></span>

| <span data-ttu-id="e9d6c-149">方法</span><span class="sxs-lookup"><span data-stu-id="e9d6c-149">Method</span></span>                                                | <span data-ttu-id="e9d6c-150">説明</span><span class="sxs-lookup"><span data-stu-id="e9d6c-150">Description</span></span>                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="e9d6c-151">public void new(\[boolean generateNewTransactionID\])</span><span class="sxs-lookup"><span data-stu-id="e9d6c-151">public void new(\[boolean generateNewTransactionID\])</span></span> | <span data-ttu-id="e9d6c-152">Connection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-152">Initializes a new instance of the Connection class.</span></span> |

### <a name="method-new"></a><span data-ttu-id="e9d6c-153">メソッド new</span><span class="sxs-lookup"><span data-stu-id="e9d6c-153">Method new</span></span>

<span data-ttu-id="e9d6c-154">Connection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-154">Initializes a new instance of the Connection class.</span></span>

    public void new([boolean generateNewTransactionID])

#### <a name="parameters"></a><span data-ttu-id="e9d6c-155">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9d6c-155">Parameters</span></span>

<span data-ttu-id="e9d6c-156">generateNewTransactionID</span><span class="sxs-lookup"><span data-stu-id="e9d6c-156">generateNewTransactionID</span></span>  

## <a name="class-usermenulist"></a><span data-ttu-id="e9d6c-157">クラス UserMenuList</span><span class="sxs-lookup"><span data-stu-id="e9d6c-157">Class UserMenuList</span></span>
    class UserMenuList extends TreeNode

<span data-ttu-id="e9d6c-158">UserMenuList クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-158">The UserMenuList class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="e9d6c-159">備考</span><span class="sxs-lookup"><span data-stu-id="e9d6c-159">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="e9d6c-160">例</span><span class="sxs-lookup"><span data-stu-id="e9d6c-160">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="e9d6c-161">メソッド</span><span class="sxs-lookup"><span data-stu-id="e9d6c-161">Methods</span></span>

| <span data-ttu-id="e9d6c-162">方法</span><span class="sxs-lookup"><span data-stu-id="e9d6c-162">Method</span></span>                               | <span data-ttu-id="e9d6c-163">説明</span><span class="sxs-lookup"><span data-stu-id="e9d6c-163">Description</span></span> |
|--------------------------------------|-------------|
| <span data-ttu-id="e9d6c-164">public void createMenu(\[str name\])</span><span class="sxs-lookup"><span data-stu-id="e9d6c-164">public void createMenu(\[str name\])</span></span> |             |

### <a name="method-createmenu"></a><span data-ttu-id="e9d6c-165">メソッド createMenu</span><span class="sxs-lookup"><span data-stu-id="e9d6c-165">Method createMenu</span></span>

    public void createMenu([str name])

#### <a name="parameters"></a><span data-ttu-id="e9d6c-166">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9d6c-166">Parameters</span></span>

<span data-ttu-id="e9d6c-167">名前</span><span class="sxs-lookup"><span data-stu-id="e9d6c-167">name</span></span>  

## <a name="class-usersetup"></a><span data-ttu-id="e9d6c-168">クラス UserSetup</span><span class="sxs-lookup"><span data-stu-id="e9d6c-168">Class UserSetup</span></span>
    class UserSetup extends TreeNode

<span data-ttu-id="e9d6c-169">UserSetup クラスは、ユーザー パラメーターを設定するためのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-169">The UserSetup class provides an interface for setting user parameters.</span></span>

### <a name="remarks"></a><span data-ttu-id="e9d6c-170">備考</span><span class="sxs-lookup"><span data-stu-id="e9d6c-170">Remarks</span></span>

<span data-ttu-id="e9d6c-171">このクラスは、主に SysUserSetup フォームで使用されます。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-171">This class is used mainly in the SysUserSetup form.</span></span> <span data-ttu-id="e9d6c-172">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-172">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="e9d6c-173">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-173">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="e9d6c-174">例</span><span class="sxs-lookup"><span data-stu-id="e9d6c-174">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="e9d6c-175">メソッド</span><span class="sxs-lookup"><span data-stu-id="e9d6c-175">Methods</span></span>

| <span data-ttu-id="e9d6c-176">方法</span><span class="sxs-lookup"><span data-stu-id="e9d6c-176">Method</span></span>                                  | <span data-ttu-id="e9d6c-177">説明</span><span class="sxs-lookup"><span data-stu-id="e9d6c-177">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="e9d6c-178">public boolean xRef(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="e9d6c-178">public boolean xRef(\[boolean enable\])</span></span> |             |
| <span data-ttu-id="e9d6c-179">public void setUserSetup(Common cursor)</span><span class="sxs-lookup"><span data-stu-id="e9d6c-179">public void setUserSetup(Common cursor)</span></span> |             |
| <span data-ttu-id="e9d6c-180">public void setDefaults(Common cursor)</span><span class="sxs-lookup"><span data-stu-id="e9d6c-180">public void setDefaults(Common cursor)</span></span>  |             |

### <a name="method-xref"></a><span data-ttu-id="e9d6c-181">メソッド xRef</span><span class="sxs-lookup"><span data-stu-id="e9d6c-181">Method xRef</span></span>

    public boolean xRef([boolean enable])

#### <a name="parameters"></a><span data-ttu-id="e9d6c-182">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9d6c-182">Parameters</span></span>

<span data-ttu-id="e9d6c-183">enable</span><span class="sxs-lookup"><span data-stu-id="e9d6c-183">enable</span></span>  

#### <a name="return-value"></a><span data-ttu-id="e9d6c-184">戻り値</span><span class="sxs-lookup"><span data-stu-id="e9d6c-184">Return Value</span></span>

### <a name="method-setusersetup"></a><span data-ttu-id="e9d6c-185">メソッド setUserSetup</span><span class="sxs-lookup"><span data-stu-id="e9d6c-185">Method setUserSetup</span></span>

    public void setUserSetup(Common cursor)

#### <a name="parameters"></a><span data-ttu-id="e9d6c-186">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9d6c-186">Parameters</span></span>

<span data-ttu-id="e9d6c-187">cursor</span><span class="sxs-lookup"><span data-stu-id="e9d6c-187">cursor</span></span>  

### <a name="method-setdefaults"></a><span data-ttu-id="e9d6c-188">メソッド setDefaults</span><span class="sxs-lookup"><span data-stu-id="e9d6c-188">Method setDefaults</span></span>

    public void setDefaults(Common cursor)

#### <a name="parameters"></a><span data-ttu-id="e9d6c-189">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9d6c-189">Parameters</span></span>

<span data-ttu-id="e9d6c-190">cursor</span><span class="sxs-lookup"><span data-stu-id="e9d6c-190">cursor</span></span>  

## <a name="class-utilfile"></a><span data-ttu-id="e9d6c-191">クラス UtilFile</span><span class="sxs-lookup"><span data-stu-id="e9d6c-191">Class UtilFile</span></span>
    class UtilFile extends Object

### <a name="remarks"></a><span data-ttu-id="e9d6c-192">備考</span><span class="sxs-lookup"><span data-stu-id="e9d6c-192">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="e9d6c-193">例</span><span class="sxs-lookup"><span data-stu-id="e9d6c-193">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="e9d6c-194">メソッド</span><span class="sxs-lookup"><span data-stu-id="e9d6c-194">Methods</span></span>

| <span data-ttu-id="e9d6c-195">方法</span><span class="sxs-lookup"><span data-stu-id="e9d6c-195">Method</span></span>                                                      | <span data-ttu-id="e9d6c-196">説明</span><span class="sxs-lookup"><span data-stu-id="e9d6c-196">Description</span></span>                                                      |
|-------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="e9d6c-197">public boolean aodFileExist(UtilEntryLevel layer)</span><span class="sxs-lookup"><span data-stu-id="e9d6c-197">public boolean aodFileExist(UtilEntryLevel layer)</span></span>           |                                                                  |
| <span data-ttu-id="e9d6c-198">public int importAODFile(UtilEntryLevel layer, int modelId)</span><span class="sxs-lookup"><span data-stu-id="e9d6c-198">public int importAODFile(UtilEntryLevel layer, int modelId)</span></span> |                                                                  |
| <span data-ttu-id="e9d6c-199">public str layers()</span><span class="sxs-lookup"><span data-stu-id="e9d6c-199">public str layers()</span></span>                                         |                                                                  |
| <span data-ttu-id="e9d6c-200">public boolean needReindex()</span><span class="sxs-lookup"><span data-stu-id="e9d6c-200">public boolean needReindex()</span></span>                                |                                                                  |
| <span data-ttu-id="e9d6c-201">public void check(str layer, str action)</span><span class="sxs-lookup"><span data-stu-id="e9d6c-201">public void check(str layer, str action)</span></span>                    |                                                                  |
| <span data-ttu-id="e9d6c-202">public void new(str fileType)</span><span class="sxs-lookup"><span data-stu-id="e9d6c-202">public void new(str fileType)</span></span>                               | <span data-ttu-id="e9d6c-203">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-203">Initializes a new instance of the Object class.</span></span>                  |
| <span data-ttu-id="e9d6c-204">public void reindex()</span><span class="sxs-lookup"><span data-stu-id="e9d6c-204">public void reindex()</span></span>                                       | <span data-ttu-id="e9d6c-205">X++ コードとメタデータの作成、読み取り、更新、および削除ができます。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-205">Lets you create, read, update, and delete X++ code and metadata.</span></span> |
| <span data-ttu-id="e9d6c-206">public void flushCache()</span><span class="sxs-lookup"><span data-stu-id="e9d6c-206">public void flushCache()</span></span>                                    |                                                                  |

### <a name="method-aodfileexist"></a><span data-ttu-id="e9d6c-207">メソッド aodFileExist</span><span class="sxs-lookup"><span data-stu-id="e9d6c-207">Method aodFileExist</span></span>

    public boolean aodFileExist(UtilEntryLevel layer)

#### <a name="parameters"></a><span data-ttu-id="e9d6c-208">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9d6c-208">Parameters</span></span>

<span data-ttu-id="e9d6c-209"> レイヤー</span><span class="sxs-lookup"><span data-stu-id="e9d6c-209">layer</span></span>  

#### <a name="return-value"></a><span data-ttu-id="e9d6c-210">戻り値</span><span class="sxs-lookup"><span data-stu-id="e9d6c-210">Return Value</span></span>

### <a name="method-importaodfile"></a><span data-ttu-id="e9d6c-211">メソッド importAODFile</span><span class="sxs-lookup"><span data-stu-id="e9d6c-211">Method importAODFile</span></span>

    public int importAODFile(UtilEntryLevel layer, int modelId)

#### <a name="parameters"></a><span data-ttu-id="e9d6c-212">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9d6c-212">Parameters</span></span>

<span data-ttu-id="e9d6c-213"> レイヤー</span><span class="sxs-lookup"><span data-stu-id="e9d6c-213">layer</span></span>  

<!-- -->

<span data-ttu-id="e9d6c-214">modelId</span><span class="sxs-lookup"><span data-stu-id="e9d6c-214">modelId</span></span>  

#### <a name="return-value"></a><span data-ttu-id="e9d6c-215">戻り値</span><span class="sxs-lookup"><span data-stu-id="e9d6c-215">Return Value</span></span>

### <a name="method-layers"></a><span data-ttu-id="e9d6c-216">メソッド layers</span><span class="sxs-lookup"><span data-stu-id="e9d6c-216">Method layers</span></span>

    public str layers()

#### <a name="return-value"></a><span data-ttu-id="e9d6c-217">戻り値</span><span class="sxs-lookup"><span data-stu-id="e9d6c-217">Return Value</span></span>

### <a name="method-needreindex"></a><span data-ttu-id="e9d6c-218">メソッド needReindex</span><span class="sxs-lookup"><span data-stu-id="e9d6c-218">Method needReindex</span></span>

    public boolean needReindex()

#### <a name="return-value"></a><span data-ttu-id="e9d6c-219">戻り値</span><span class="sxs-lookup"><span data-stu-id="e9d6c-219">Return Value</span></span>

### <a name="method-check"></a><span data-ttu-id="e9d6c-220">メソッド check</span><span class="sxs-lookup"><span data-stu-id="e9d6c-220">Method check</span></span>

    public void check(str layer, str action)

#### <a name="parameters"></a><span data-ttu-id="e9d6c-221">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9d6c-221">Parameters</span></span>

<span data-ttu-id="e9d6c-222"> レイヤー</span><span class="sxs-lookup"><span data-stu-id="e9d6c-222">layer</span></span>  

<!-- -->

<span data-ttu-id="e9d6c-223">アクション</span><span class="sxs-lookup"><span data-stu-id="e9d6c-223">action</span></span>  

### <a name="method-new"></a><span data-ttu-id="e9d6c-224">メソッド new</span><span class="sxs-lookup"><span data-stu-id="e9d6c-224">Method new</span></span>

<span data-ttu-id="e9d6c-225">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-225">Initializes a new instance of the Object class.</span></span>

    public void new(str fileType)

#### <a name="parameters"></a><span data-ttu-id="e9d6c-226">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9d6c-226">Parameters</span></span>

<span data-ttu-id="e9d6c-227">fileType</span><span class="sxs-lookup"><span data-stu-id="e9d6c-227">fileType</span></span>  

### <a name="method-reindex"></a><span data-ttu-id="e9d6c-228">メソッド reindex</span><span class="sxs-lookup"><span data-stu-id="e9d6c-228">Method reindex</span></span>

<span data-ttu-id="e9d6c-229">X++ コードとメタデータの作成、読み取り、更新、および削除ができます。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-229">Lets you create, read, update, and delete X++ code and metadata.</span></span>

    public void reindex()

#### <a name="remarks"></a><span data-ttu-id="e9d6c-230">備考</span><span class="sxs-lookup"><span data-stu-id="e9d6c-230">Remarks</span></span>

<span data-ttu-id="e9d6c-231">この API を呼び出す前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-231">Make sure that the user has access to the development security key (SysDevelopment) before you call this API.</span></span>

#### <a name="examples"></a><span data-ttu-id="e9d6c-232">例</span><span class="sxs-lookup"><span data-stu-id="e9d6c-232">Examples</span></span>

<span data-ttu-id="e9d6c-233">次の例では、UtilFile.reindex メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-233">The following example calls the UtilFile.reindex method.</span></span> <span data-ttu-id="e9d6c-234">変更を実行する前に、ユーザーが必要なセキュリティ キーを持っているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="e9d6c-234">It checks whether the user has the required security key before you perform a modification.</span></span>

    server static public void Main(Args _args) 
    { 
        UtilFile u; 
        u = new UtilFile("util"); 
        if (u) 
        { 
            u.reindex(); 
        } 
    }

### <a name="method-flushcache"></a><span data-ttu-id="e9d6c-235">メソッド flushCache</span><span class="sxs-lookup"><span data-stu-id="e9d6c-235">Method flushCache</span></span>

    public void flushCache()



