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
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 51691
ms.assetid: 92bfbb9c-4f45-464a-8ccb-71fb227780fe
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 73658479ac9fdb72de0fc9f2cd82c0f081975af7
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537003"
---
# <a name="u-classes"></a><span data-ttu-id="04114-103">U クラス</span><span class="sxs-lookup"><span data-stu-id="04114-103">U classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04114-104">文字 U で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="04114-104">System API classes that start with the letter U.</span></span>

<a name="class-unitofwork"></a><span data-ttu-id="04114-105">クラス UnitofWork</span><span class="sxs-lookup"><span data-stu-id="04114-105">Class UnitofWork</span></span>
----------------

    class UnitofWork extends Object

### <a name="remarks"></a><span data-ttu-id="04114-106">備考</span><span class="sxs-lookup"><span data-stu-id="04114-106">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="04114-107">例</span><span class="sxs-lookup"><span data-stu-id="04114-107">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="04114-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="04114-108">Methods</span></span>

| <span data-ttu-id="04114-109">方法</span><span class="sxs-lookup"><span data-stu-id="04114-109">Method</span></span>                                                       | <span data-ttu-id="04114-110">説明</span><span class="sxs-lookup"><span data-stu-id="04114-110">Description</span></span>                                         |
|--------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="04114-111">public boolean getByKey(Common record)</span><span class="sxs-lookup"><span data-stu-id="04114-111">public boolean getByKey(Common record)</span></span>                       |                                                     |
| <span data-ttu-id="04114-112">public void updateonSaveChanges(Common record)</span><span class="sxs-lookup"><span data-stu-id="04114-112">public void updateonSaveChanges(Common record)</span></span>               |                                                     |
| <span data-ttu-id="04114-113">public void saveChanges(\[UserConnection user\_connection\])</span><span class="sxs-lookup"><span data-stu-id="04114-113">public void saveChanges(\[UserConnection user\_connection\])</span></span> |                                                     |
| <span data-ttu-id="04114-114">public void deleteonSaveChanges(Common record)</span><span class="sxs-lookup"><span data-stu-id="04114-114">public void deleteonSaveChanges(Common record)</span></span>               |                                                     |
| <span data-ttu-id="04114-115">public void insertonSaveChanges(Common record)</span><span class="sxs-lookup"><span data-stu-id="04114-115">public void insertonSaveChanges(Common record)</span></span>               |                                                     |
| <span data-ttu-id="04114-116">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="04114-116">public void finalize()</span></span>                                       |                                                     |
| <span data-ttu-id="04114-117">public void new()</span><span class="sxs-lookup"><span data-stu-id="04114-117">public void new()</span></span>                                            | <span data-ttu-id="04114-118">UnitofWork クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="04114-118">Initializes a new instance of the UnitofWork class.</span></span> |
| <span data-ttu-id="04114-119">public void clear()</span><span class="sxs-lookup"><span data-stu-id="04114-119">public void clear()</span></span>                                          |                                                     |

### <a name="method-getbykey"></a><span data-ttu-id="04114-120">メソッド getByKey</span><span class="sxs-lookup"><span data-stu-id="04114-120">Method getByKey</span></span>

    public boolean getByKey(Common record)

#### <a name="parameters"></a><span data-ttu-id="04114-121">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04114-121">Parameters</span></span>

<span data-ttu-id="04114-122">記録</span><span class="sxs-lookup"><span data-stu-id="04114-122">record</span></span>  

#### <a name="return-value"></a><span data-ttu-id="04114-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="04114-123">Return Value</span></span>

### <a name="method-updateonsavechanges"></a><span data-ttu-id="04114-124">メソッド updateonSaveChanges</span><span class="sxs-lookup"><span data-stu-id="04114-124">Method updateonSaveChanges</span></span>

    public void updateonSaveChanges(Common record)

#### <a name="parameters"></a><span data-ttu-id="04114-125">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04114-125">Parameters</span></span>

<span data-ttu-id="04114-126">記録</span><span class="sxs-lookup"><span data-stu-id="04114-126">record</span></span>  

### <a name="method-savechanges"></a><span data-ttu-id="04114-127">メソッド saveChanges</span><span class="sxs-lookup"><span data-stu-id="04114-127">Method saveChanges</span></span>

    public void saveChanges([UserConnection user_connection])

#### <a name="parameters"></a><span data-ttu-id="04114-128">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04114-128">Parameters</span></span>

<span data-ttu-id="04114-129">user\_connection</span><span class="sxs-lookup"><span data-stu-id="04114-129">user\_connection</span></span>  

### <a name="method-deleteonsavechanges"></a><span data-ttu-id="04114-130">メソッド deleteonSaveChanges</span><span class="sxs-lookup"><span data-stu-id="04114-130">Method deleteonSaveChanges</span></span>

    public void deleteonSaveChanges(Common record)

#### <a name="parameters"></a><span data-ttu-id="04114-131">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04114-131">Parameters</span></span>

<span data-ttu-id="04114-132">記録</span><span class="sxs-lookup"><span data-stu-id="04114-132">record</span></span>  

### <a name="method-insertonsavechanges"></a><span data-ttu-id="04114-133">メソッド insertonSaveChanges</span><span class="sxs-lookup"><span data-stu-id="04114-133">Method insertonSaveChanges</span></span>

    public void insertonSaveChanges(Common record)

#### <a name="parameters"></a><span data-ttu-id="04114-134">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04114-134">Parameters</span></span>

<span data-ttu-id="04114-135">記録</span><span class="sxs-lookup"><span data-stu-id="04114-135">record</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="04114-136">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="04114-136">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="04114-137">メソッド new</span><span class="sxs-lookup"><span data-stu-id="04114-137">Method new</span></span>

<span data-ttu-id="04114-138">UnitofWork クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="04114-138">Initializes a new instance of the UnitofWork class.</span></span>

    public void new()

### <a name="method-clear"></a><span data-ttu-id="04114-139">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="04114-139">Method clear</span></span>

    public void clear()

## <a name="class-userconnection"></a><span data-ttu-id="04114-140">クラス UserConnection</span><span class="sxs-lookup"><span data-stu-id="04114-140">Class UserConnection</span></span>
    class UserConnection extends Connection

<span data-ttu-id="04114-141">UserConnection クラスは、主要な接続と同じログオン プロパティに基づいて、SQL データベースへの補助接続を表します。</span><span class="sxs-lookup"><span data-stu-id="04114-141">The UserConnection class represents an auxiliary connection to the SQL database, based on the same logon properties as the main connection.</span></span>

### <a name="remarks"></a><span data-ttu-id="04114-142">備考</span><span class="sxs-lookup"><span data-stu-id="04114-142">Remarks</span></span>

<span data-ttu-id="04114-143">SQL ステートメントが実行され、結果が UserConnection クラスのコンテキストで返されます。</span><span class="sxs-lookup"><span data-stu-id="04114-143">SQL statements are executed, and results are returned in the context of a UserConnection class.</span></span> <span data-ttu-id="04114-144">UserConnection クラスを使用して、別個のトランザクション スコープを取得できます。</span><span class="sxs-lookup"><span data-stu-id="04114-144">The UserConnection class can be used to obtain a separate transaction scope.</span></span>

<span data-ttu-id="04114-145">注記: ユーザー接続リークを防ぐため、finally ブロックで Userconnection.finalize() を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="04114-145">Note: Userconnection.finalize() needs to be called in the finally block to prevent user connection leak.</span></span>  <span data-ttu-id="04114-146">オープン ユーザー接続の数がサーバー上で制限されており、制限に達すると、それ以上接続を開くことができなくなり、ビジネス ロジックのエラーになる可能性があります</span><span class="sxs-lookup"><span data-stu-id="04114-146">Number of open user connections is limited on the server, when it reaches the limit, no more connections can be opened, which can leads to business logic failures</span></span>

### <a name="examples"></a><span data-ttu-id="04114-147">例</span><span class="sxs-lookup"><span data-stu-id="04114-147">Examples</span></span>

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

### <a name="methods"></a><span data-ttu-id="04114-148">方法</span><span class="sxs-lookup"><span data-stu-id="04114-148">Methods</span></span>

| <span data-ttu-id="04114-149">方法</span><span class="sxs-lookup"><span data-stu-id="04114-149">Method</span></span>                                                | <span data-ttu-id="04114-150">説明</span><span class="sxs-lookup"><span data-stu-id="04114-150">Description</span></span>                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="04114-151">public void new(\[boolean generateNewTransactionID\])</span><span class="sxs-lookup"><span data-stu-id="04114-151">public void new(\[boolean generateNewTransactionID\])</span></span> | <span data-ttu-id="04114-152">Connection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="04114-152">Initializes a new instance of the Connection class.</span></span> |

### <a name="method-new"></a><span data-ttu-id="04114-153">メソッド new</span><span class="sxs-lookup"><span data-stu-id="04114-153">Method new</span></span>

<span data-ttu-id="04114-154">Connection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="04114-154">Initializes a new instance of the Connection class.</span></span>

    public void new([boolean generateNewTransactionID])

#### <a name="parameters"></a><span data-ttu-id="04114-155">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04114-155">Parameters</span></span>

<span data-ttu-id="04114-156">generateNewTransactionID</span><span class="sxs-lookup"><span data-stu-id="04114-156">generateNewTransactionID</span></span>  

## <a name="class-usermenulist"></a><span data-ttu-id="04114-157">クラス UserMenuList</span><span class="sxs-lookup"><span data-stu-id="04114-157">Class UserMenuList</span></span>
    class UserMenuList extends TreeNode

<span data-ttu-id="04114-158">UserMenuList クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="04114-158">The UserMenuList class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="04114-159">備考</span><span class="sxs-lookup"><span data-stu-id="04114-159">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="04114-160">例</span><span class="sxs-lookup"><span data-stu-id="04114-160">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="04114-161">メソッド</span><span class="sxs-lookup"><span data-stu-id="04114-161">Methods</span></span>

| <span data-ttu-id="04114-162">方法</span><span class="sxs-lookup"><span data-stu-id="04114-162">Method</span></span>                               | <span data-ttu-id="04114-163">説明</span><span class="sxs-lookup"><span data-stu-id="04114-163">Description</span></span> |
|--------------------------------------|-------------|
| <span data-ttu-id="04114-164">public void createMenu(\[str name\])</span><span class="sxs-lookup"><span data-stu-id="04114-164">public void createMenu(\[str name\])</span></span> |             |

### <a name="method-createmenu"></a><span data-ttu-id="04114-165">メソッド createMenu</span><span class="sxs-lookup"><span data-stu-id="04114-165">Method createMenu</span></span>

    public void createMenu([str name])

#### <a name="parameters"></a><span data-ttu-id="04114-166">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04114-166">Parameters</span></span>

<span data-ttu-id="04114-167">名前</span><span class="sxs-lookup"><span data-stu-id="04114-167">name</span></span>  

## <a name="class-usersetup"></a><span data-ttu-id="04114-168">クラス UserSetup</span><span class="sxs-lookup"><span data-stu-id="04114-168">Class UserSetup</span></span>
    class UserSetup extends TreeNode

<span data-ttu-id="04114-169">UserSetup クラスは、ユーザー パラメーターを設定するためのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="04114-169">The UserSetup class provides an interface for setting user parameters.</span></span>

### <a name="remarks"></a><span data-ttu-id="04114-170">備考</span><span class="sxs-lookup"><span data-stu-id="04114-170">Remarks</span></span>

<span data-ttu-id="04114-171">このクラスは、主に SysUserSetup フォームで使用されます。</span><span class="sxs-lookup"><span data-stu-id="04114-171">This class is used mainly in the SysUserSetup form.</span></span> <span data-ttu-id="04114-172">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="04114-172">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="04114-173">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="04114-173">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="04114-174">例</span><span class="sxs-lookup"><span data-stu-id="04114-174">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="04114-175">メソッド</span><span class="sxs-lookup"><span data-stu-id="04114-175">Methods</span></span>

| <span data-ttu-id="04114-176">方法</span><span class="sxs-lookup"><span data-stu-id="04114-176">Method</span></span>                                  | <span data-ttu-id="04114-177">説明</span><span class="sxs-lookup"><span data-stu-id="04114-177">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="04114-178">public boolean xRef(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="04114-178">public boolean xRef(\[boolean enable\])</span></span> |             |
| <span data-ttu-id="04114-179">public void setUserSetup(Common cursor)</span><span class="sxs-lookup"><span data-stu-id="04114-179">public void setUserSetup(Common cursor)</span></span> |             |
| <span data-ttu-id="04114-180">public void setDefaults(Common cursor)</span><span class="sxs-lookup"><span data-stu-id="04114-180">public void setDefaults(Common cursor)</span></span>  |             |

### <a name="method-xref"></a><span data-ttu-id="04114-181">メソッド xRef</span><span class="sxs-lookup"><span data-stu-id="04114-181">Method xRef</span></span>

    public boolean xRef([boolean enable])

#### <a name="parameters"></a><span data-ttu-id="04114-182">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04114-182">Parameters</span></span>

<span data-ttu-id="04114-183">enable</span><span class="sxs-lookup"><span data-stu-id="04114-183">enable</span></span>  

#### <a name="return-value"></a><span data-ttu-id="04114-184">戻り値</span><span class="sxs-lookup"><span data-stu-id="04114-184">Return Value</span></span>

### <a name="method-setusersetup"></a><span data-ttu-id="04114-185">メソッド setUserSetup</span><span class="sxs-lookup"><span data-stu-id="04114-185">Method setUserSetup</span></span>

    public void setUserSetup(Common cursor)

#### <a name="parameters"></a><span data-ttu-id="04114-186">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04114-186">Parameters</span></span>

<span data-ttu-id="04114-187">cursor</span><span class="sxs-lookup"><span data-stu-id="04114-187">cursor</span></span>  

### <a name="method-setdefaults"></a><span data-ttu-id="04114-188">メソッド setDefaults</span><span class="sxs-lookup"><span data-stu-id="04114-188">Method setDefaults</span></span>

    public void setDefaults(Common cursor)

#### <a name="parameters"></a><span data-ttu-id="04114-189">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04114-189">Parameters</span></span>

<span data-ttu-id="04114-190">cursor</span><span class="sxs-lookup"><span data-stu-id="04114-190">cursor</span></span>  

## <a name="class-utilfile"></a><span data-ttu-id="04114-191">クラス UtilFile</span><span class="sxs-lookup"><span data-stu-id="04114-191">Class UtilFile</span></span>
    class UtilFile extends Object

### <a name="remarks"></a><span data-ttu-id="04114-192">備考</span><span class="sxs-lookup"><span data-stu-id="04114-192">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="04114-193">例</span><span class="sxs-lookup"><span data-stu-id="04114-193">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="04114-194">メソッド</span><span class="sxs-lookup"><span data-stu-id="04114-194">Methods</span></span>

| <span data-ttu-id="04114-195">方法</span><span class="sxs-lookup"><span data-stu-id="04114-195">Method</span></span>                                                      | <span data-ttu-id="04114-196">説明</span><span class="sxs-lookup"><span data-stu-id="04114-196">Description</span></span>                                                      |
|-------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="04114-197">public boolean aodFileExist(UtilEntryLevel layer)</span><span class="sxs-lookup"><span data-stu-id="04114-197">public boolean aodFileExist(UtilEntryLevel layer)</span></span>           |                                                                  |
| <span data-ttu-id="04114-198">public int importAODFile(UtilEntryLevel layer, int modelId)</span><span class="sxs-lookup"><span data-stu-id="04114-198">public int importAODFile(UtilEntryLevel layer, int modelId)</span></span> |                                                                  |
| <span data-ttu-id="04114-199">public str layers()</span><span class="sxs-lookup"><span data-stu-id="04114-199">public str layers()</span></span>                                         |                                                                  |
| <span data-ttu-id="04114-200">public boolean needReindex()</span><span class="sxs-lookup"><span data-stu-id="04114-200">public boolean needReindex()</span></span>                                |                                                                  |
| <span data-ttu-id="04114-201">public void check(str layer, str action)</span><span class="sxs-lookup"><span data-stu-id="04114-201">public void check(str layer, str action)</span></span>                    |                                                                  |
| <span data-ttu-id="04114-202">public void new(str fileType)</span><span class="sxs-lookup"><span data-stu-id="04114-202">public void new(str fileType)</span></span>                               | <span data-ttu-id="04114-203">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="04114-203">Initializes a new instance of the Object class.</span></span>                  |
| <span data-ttu-id="04114-204">public void reindex()</span><span class="sxs-lookup"><span data-stu-id="04114-204">public void reindex()</span></span>                                       | <span data-ttu-id="04114-205">X++ コードとメタデータの作成、読み取り、更新、および削除ができます。</span><span class="sxs-lookup"><span data-stu-id="04114-205">Lets you create, read, update, and delete X++ code and metadata.</span></span> |
| <span data-ttu-id="04114-206">public void flushCache()</span><span class="sxs-lookup"><span data-stu-id="04114-206">public void flushCache()</span></span>                                    |                                                                  |

### <a name="method-aodfileexist"></a><span data-ttu-id="04114-207">メソッド aodFileExist</span><span class="sxs-lookup"><span data-stu-id="04114-207">Method aodFileExist</span></span>

    public boolean aodFileExist(UtilEntryLevel layer)

#### <a name="parameters"></a><span data-ttu-id="04114-208">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04114-208">Parameters</span></span>

<span data-ttu-id="04114-209"> レイヤー</span><span class="sxs-lookup"><span data-stu-id="04114-209">layer</span></span>  

#### <a name="return-value"></a><span data-ttu-id="04114-210">戻り値</span><span class="sxs-lookup"><span data-stu-id="04114-210">Return Value</span></span>

### <a name="method-importaodfile"></a><span data-ttu-id="04114-211">メソッド importAODFile</span><span class="sxs-lookup"><span data-stu-id="04114-211">Method importAODFile</span></span>

    public int importAODFile(UtilEntryLevel layer, int modelId)

#### <a name="parameters"></a><span data-ttu-id="04114-212">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04114-212">Parameters</span></span>

<span data-ttu-id="04114-213"> レイヤー</span><span class="sxs-lookup"><span data-stu-id="04114-213">layer</span></span>  

<!-- -->

<span data-ttu-id="04114-214">modelId</span><span class="sxs-lookup"><span data-stu-id="04114-214">modelId</span></span>  

#### <a name="return-value"></a><span data-ttu-id="04114-215">戻り値</span><span class="sxs-lookup"><span data-stu-id="04114-215">Return Value</span></span>

### <a name="method-layers"></a><span data-ttu-id="04114-216">メソッド layers</span><span class="sxs-lookup"><span data-stu-id="04114-216">Method layers</span></span>

    public str layers()

#### <a name="return-value"></a><span data-ttu-id="04114-217">戻り値</span><span class="sxs-lookup"><span data-stu-id="04114-217">Return Value</span></span>

### <a name="method-needreindex"></a><span data-ttu-id="04114-218">メソッド needReindex</span><span class="sxs-lookup"><span data-stu-id="04114-218">Method needReindex</span></span>

    public boolean needReindex()

#### <a name="return-value"></a><span data-ttu-id="04114-219">戻り値</span><span class="sxs-lookup"><span data-stu-id="04114-219">Return Value</span></span>

### <a name="method-check"></a><span data-ttu-id="04114-220">メソッド check</span><span class="sxs-lookup"><span data-stu-id="04114-220">Method check</span></span>

    public void check(str layer, str action)

#### <a name="parameters"></a><span data-ttu-id="04114-221">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04114-221">Parameters</span></span>

<span data-ttu-id="04114-222"> レイヤー</span><span class="sxs-lookup"><span data-stu-id="04114-222">layer</span></span>  

<!-- -->

<span data-ttu-id="04114-223">アクション</span><span class="sxs-lookup"><span data-stu-id="04114-223">action</span></span>  

### <a name="method-new"></a><span data-ttu-id="04114-224">メソッド new</span><span class="sxs-lookup"><span data-stu-id="04114-224">Method new</span></span>

<span data-ttu-id="04114-225">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="04114-225">Initializes a new instance of the Object class.</span></span>

    public void new(str fileType)

#### <a name="parameters"></a><span data-ttu-id="04114-226">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04114-226">Parameters</span></span>

<span data-ttu-id="04114-227">fileType</span><span class="sxs-lookup"><span data-stu-id="04114-227">fileType</span></span>  

### <a name="method-reindex"></a><span data-ttu-id="04114-228">メソッド reindex</span><span class="sxs-lookup"><span data-stu-id="04114-228">Method reindex</span></span>

<span data-ttu-id="04114-229">X++ コードとメタデータの作成、読み取り、更新、および削除ができます。</span><span class="sxs-lookup"><span data-stu-id="04114-229">Lets you create, read, update, and delete X++ code and metadata.</span></span>

    public void reindex()

#### <a name="remarks"></a><span data-ttu-id="04114-230">備考</span><span class="sxs-lookup"><span data-stu-id="04114-230">Remarks</span></span>

<span data-ttu-id="04114-231">この API を呼び出す前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="04114-231">Make sure that the user has access to the development security key (SysDevelopment) before you call this API.</span></span>

#### <a name="examples"></a><span data-ttu-id="04114-232">例</span><span class="sxs-lookup"><span data-stu-id="04114-232">Examples</span></span>

<span data-ttu-id="04114-233">次の例では、UtilFile.reindex メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="04114-233">The following example calls the UtilFile.reindex method.</span></span> <span data-ttu-id="04114-234">変更を実行する前に、ユーザーが必要なセキュリティ キーを持っているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="04114-234">It checks whether the user has the required security key before you perform a modification.</span></span>

    server static public void Main(Args _args) 
    { 
        UtilFile u; 
        u = new UtilFile("util"); 
        if (u) 
        { 
            u.reindex(); 
        } 
    }

### <a name="method-flushcache"></a><span data-ttu-id="04114-235">メソッド flushCache</span><span class="sxs-lookup"><span data-stu-id="04114-235">Method flushCache</span></span>

    public void flushCache()



