---
title: "X++ セッション ランタイム関数"
description: "このトピックでは、セッション ランタイム関数について説明します。"
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
ms.custom: 31421
ms.assetid: a83ec18b-cc9e-40e3-ab06-87ff1c972a6a
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 69fa9878a2a1729e67423374054f26de6ebe2c17
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="x-session-runtime-functions"></a><span data-ttu-id="f9ca4-103">X++ セッション ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="f9ca4-103">X++ session runtime functions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9ca4-104">このトピックでは、セッション ランタイム関数について説明します。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-104">This topic describes the session run-time functions.</span></span>

<a name="curext"></a><span data-ttu-id="f9ca4-105">curExt</span><span class="sxs-lookup"><span data-stu-id="f9ca4-105">curExt</span></span>
------

<span data-ttu-id="f9ca4-106">現在の会社に使用できる拡張を取得します。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-106">Retrieves the extension that is used for the current company.</span></span>

    str curExt()

### <a name="return-value"></a><span data-ttu-id="f9ca4-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="f9ca4-107">Return value</span></span>

<span data-ttu-id="f9ca4-108">現在の会社の内線電話番号。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-108">The extension for the current company.</span></span>

### <a name="remarks"></a><span data-ttu-id="f9ca4-109">備考</span><span class="sxs-lookup"><span data-stu-id="f9ca4-109">Remarks</span></span>

<span data-ttu-id="f9ca4-110">サーバー層への呼び出しを回避するには、このメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-110">Use this method to avoid a call to the server tier.</span></span> <span data-ttu-id="f9ca4-111">代わりに、サーバー層を呼び出す**アプリケーション** クラスの **company** メソッドを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-111">The alternative is the **company** method of the **Application** class, which does call the server tier.</span></span>

### <a name="example"></a><span data-ttu-id="f9ca4-112">例</span><span class="sxs-lookup"><span data-stu-id="f9ca4-112">Example</span></span>

    static void curExtExample(Args _arg)
    {
            str s;
            // Sets s to the extension of the current company.
            s = curExt();
            print "Current extension is " + s;
    }

## <a name="curuserid"></a><span data-ttu-id="f9ca4-113">curUserId</span><span class="sxs-lookup"><span data-stu-id="f9ca4-113">curUserId</span></span>
<span data-ttu-id="f9ca4-114">現在のユーザーを表す数値以外の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-114">Retrieves the nonnumeric ID that represents the current user.</span></span>

    str curUserId()

### <a name="return-value"></a><span data-ttu-id="f9ca4-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="f9ca4-115">Return value</span></span>

<span data-ttu-id="f9ca4-116">現在のユーザーを表す数値以外の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-116">The nonnumeric ID that represents the current user.</span></span>

### <a name="example"></a><span data-ttu-id="f9ca4-117">例</span><span class="sxs-lookup"><span data-stu-id="f9ca4-117">Example</span></span>

    static void curUserIdExample(Args _arg)
    {
            str s;
            s = curUserId();
            print "Current user ID is " + s;
    }

## <a name="funcname"></a><span data-ttu-id="f9ca4-118">funcName</span><span class="sxs-lookup"><span data-stu-id="f9ca4-118">funcName</span></span>
<span data-ttu-id="f9ca4-119">現在の関数コンテキストを含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-119">Retrieves a string that contains the current function context.</span></span>

    str funcName()

### <a name="return-value"></a><span data-ttu-id="f9ca4-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="f9ca4-120">Return value</span></span>

<span data-ttu-id="f9ca4-121">このメソッドを実行しているメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-121">The name of the method that is executing this method.</span></span>

### <a name="remarks"></a><span data-ttu-id="f9ca4-122">備考</span><span class="sxs-lookup"><span data-stu-id="f9ca4-122">Remarks</span></span>

<span data-ttu-id="f9ca4-123">実行がテーブルまたはクラス メンバー内に現在ある場合は、メソッドの名前に、そのテーブルまたはクラスの名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-123">If execution is currently within the member of a table or class, the name of the method is prefixed with the name of that table or class.</span></span>

### <a name="example"></a><span data-ttu-id="f9ca4-124">例</span><span class="sxs-lookup"><span data-stu-id="f9ca4-124">Example</span></span>

    static void funcNameExample(Args _arg)
    {
            print "Current function context is " + funcName();
    }

## <a name="getcurrentpartition"></a><span data-ttu-id="f9ca4-125">getCurrentPartition</span><span class="sxs-lookup"><span data-stu-id="f9ca4-125">getCurrentPartition</span></span>
<span data-ttu-id="f9ca4-126">現在のパーティションの短い名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-126">Retrieves the short name of the current partition.</span></span>

    str getCurrentPartition()

### <a name="return-value"></a><span data-ttu-id="f9ca4-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="f9ca4-127">Return value</span></span>

<span data-ttu-id="f9ca4-128">現在のパーティションの短い名前。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-128">The short name of the current partition.</span></span>

### <a name="remarks"></a><span data-ttu-id="f9ca4-129">備考</span><span class="sxs-lookup"><span data-stu-id="f9ca4-129">Remarks</span></span>

<span data-ttu-id="f9ca4-130">返されるデータ パーティション名の最大の長さは 8 文字です。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-130">The maximum length of the data partition name that is returned is eight characters.</span></span>

### <a name="example"></a><span data-ttu-id="f9ca4-131">例</span><span class="sxs-lookup"><span data-stu-id="f9ca4-131">Example</span></span>

<span data-ttu-id="f9ca4-132">次のコード例は、X++ 言語の **getCurrentPartition** 関数、および関連する関数またはメソッドへの呼び出しおよび出力を示しています。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-132">The following code example shows calls to, and output from, the **getCurrentPartition** function of the X++ language, and related functions or methods.</span></span>

    static public void Main(Args _args)  // X++ method.
    {
            int64 iPartition;
            str sPartition;
            SelectableDataArea oSelectableDataArea;  // System ExDT.
            iPartition = getCurrentPartitionRecId();
            sPartition = getcurrentpartition();
            oSelectableDataArea = Global::getCompany( tableNum(BankAccountTable) );
            Global::info( strFmt(
                    "getCurrentPartitionRecId =%1 , getCurrentPartition =%2 , getCompany =%3",
                    iPartition, sPartition, oSelectableDataArea) );
    }
    /**** Pasted from Infolog window:
    Message_@SYS14327 (03:42:38 pm)
    getCurrentPartitionRecId =5637144576 , getCurrentPartition =initial , getCompany =ceu
    ****/

## <a name="getcurrentpartitionrecid"></a><span data-ttu-id="f9ca4-133">getCurrentPartitionRecId</span><span class="sxs-lookup"><span data-stu-id="f9ca4-133">getCurrentPartitionRecId</span></span>
<span data-ttu-id="f9ca4-134">現在のパーティションの **RecId** フィールドを取得します。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-134">Retrieves the **RecId** field of the current partition.</span></span>

    int64 getCurrentPartitionRecId()

### <a name="return-value"></a><span data-ttu-id="f9ca4-135">戻り値</span><span class="sxs-lookup"><span data-stu-id="f9ca4-135">Return value</span></span>

<span data-ttu-id="f9ca4-136">現在のデータ パーティションの **RecId** フィールド。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-136">The **RecId** field of the current data partition.</span></span>

### <a name="remarks"></a><span data-ttu-id="f9ca4-137">備考</span><span class="sxs-lookup"><span data-stu-id="f9ca4-137">Remarks</span></span>

<span data-ttu-id="f9ca4-138">**getCurrentPartitionRecId** 関数に依存するコード例を参照するには、[[パーティションのフィルターを直接 Transact-SQL に含める方法](http://msdn.microsoft.com/library/5ce90a42-e862-464e-90bc-1eb16a8afd1a(AX.60).aspx)] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-138">To see a code example that relies on the **getCurrentPartitionRecId** function, see [How to: Include a Filter for Partition in Direct Transact-SQL](http://msdn.microsoft.com/library/5ce90a42-e862-464e-90bc-1eb16a8afd1a(AX.60).aspx).</span></span>

### <a name="example"></a><span data-ttu-id="f9ca4-139">例</span><span class="sxs-lookup"><span data-stu-id="f9ca4-139">Example</span></span>

<span data-ttu-id="f9ca4-140">次のコード例は、X++ 言語の **getCurrentPartitionRecId** 関数、および関連する関数またはメソッドへの呼び出しおよび出力を示しています。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-140">The following code example shows calls to, and output from, the **getCurrentPartitionRecId** function of the X++ language, and related functions or methods.</span></span>

    static public void Main(Args _args)  // X++ method.
    {
            int64 iPartition;
            str sPartition;
            SelectableDataArea oSelectableDataArea;  // System ExDT.
            iPartition = getCurrentPartitionRecId();
            sPartition = getcurrentpartition();
            oSelectableDataArea = Global::getCompany( tableNum(BankAccountTable) );
            Global::info( strFmt(
                    "getCurrentPartitionRecId =%1 , getCurrentPartition =%2 , getCompany =%3",
                    iPartition, sPartition, oSelectableDataArea) );
    }
    /**** Pasted from Infolog window:
    Message_@SYS14327 (03:42:38 pm)
    getCurrentPartitionRecId =5637144576 , getCurrentPartition =initial , getCompany =ceu
    ****/

## <a name="getprefix"></a><span data-ttu-id="f9ca4-141">getPrefix</span><span class="sxs-lookup"><span data-stu-id="f9ca4-141">getPrefix</span></span>
<span data-ttu-id="f9ca4-142">**setPrefix** 関数が連続して呼び出された後、現在の実行接頭辞を取得します。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-142">Retrieves the current execution prefix after successive calls to the **setPrefix** function.</span></span>

    str getPrefix()

### <a name="return-value"></a><span data-ttu-id="f9ca4-143">戻り値</span><span class="sxs-lookup"><span data-stu-id="f9ca4-143">Return value</span></span>

<span data-ttu-id="f9ca4-144">現在の実行接頭語。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-144">The current execution prefix.</span></span>

### <a name="remarks"></a><span data-ttu-id="f9ca4-145">備考</span><span class="sxs-lookup"><span data-stu-id="f9ca4-145">Remarks</span></span>

<span data-ttu-id="f9ca4-146">接頭語メカニズムを使用すると、アプリケーションが実行したトランザクションについての正確なエラー メッセージの書き込みがより簡単になります。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-146">The prefix mechanism makes it more straightforward to write precise error messages about the transactions that an application performs.</span></span> <span data-ttu-id="f9ca4-147">情報ログでは階層表示が作成されるため、各エラーの原因を特定するのが容易になります。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-147">Because a hierarchical display is created in the Infolog, it can be easier to determine where each error came from.</span></span>

### <a name="example"></a><span data-ttu-id="f9ca4-148">例</span><span class="sxs-lookup"><span data-stu-id="f9ca4-148">Example</span></span>

    static void getPrefixExample(Args _arg)
    {
            setPrefix("Prefix");
            setPrefix("Another prefix");
            print getPrefix();
    }

## <a name="sessionid"></a><span data-ttu-id="f9ca4-149">sessionId</span><span class="sxs-lookup"><span data-stu-id="f9ca4-149">sessionId</span></span>
<span data-ttu-id="f9ca4-150">現在のセッションのセッション番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-150">Retrieves the session number of the current session.</span></span>

    int sessionId()

### <a name="return-value"></a><span data-ttu-id="f9ca4-151">戻り値</span><span class="sxs-lookup"><span data-stu-id="f9ca4-151">Return value</span></span>

<span data-ttu-id="f9ca4-152">現在のセッションの数値 ID。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-152">The numeric ID of the current session.</span></span>

### <a name="remarks"></a><span data-ttu-id="f9ca4-153">備考</span><span class="sxs-lookup"><span data-stu-id="f9ca4-153">Remarks</span></span>

<span data-ttu-id="f9ca4-154">セッション番号は、クライアントの起動時に割り当てられ、Application Object Server (AOS) に接続します。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-154">A session number is assigned when the client is started and connects to Application Object Server (AOS).</span></span> <span data-ttu-id="f9ca4-155">クライアントの存続中にこの関数を呼び出すたびに、同じ整数値が戻されます。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-155">Every call of this function during the life of the client returns the same integer value.</span></span> <span data-ttu-id="f9ca4-156">返された値は、**SessionID** 拡張データ型と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-156">The returned value is compatible with the **SessionID** extended data type.</span></span> <span data-ttu-id="f9ca4-157">**contains** メソッドは、個々のユーザー セッションに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-157">The **contains** methods return information about individual user sessions.</span></span>

### <a name="example"></a><span data-ttu-id="f9ca4-158">例</span><span class="sxs-lookup"><span data-stu-id="f9ca4-158">Example</span></span>

    static void sessionIdExample(Args _arg)
    {
            int session;
            session = sessionId();
            print "This session ID is number " + int2Str(session);
    }

## <a name="prmisdefault"></a><span data-ttu-id="f9ca4-159">prmIsDefault</span><span class="sxs-lookup"><span data-stu-id="f9ca4-159">prmIsDefault</span></span>
<span data-ttu-id="f9ca4-160">現在のメソッドの指定されたパラメータに既定値があるかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-160">Determines whether the specified parameter for the current method has the default value.</span></span>

    int prmIsDefault(anytype argument)

### <a name="parameters"></a><span data-ttu-id="f9ca4-161">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f9ca4-161">Parameters</span></span>

| <span data-ttu-id="f9ca4-162">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f9ca4-162">Parameter</span></span> | <span data-ttu-id="f9ca4-163">説明</span><span class="sxs-lookup"><span data-stu-id="f9ca4-163">Description</span></span>            |
|-----------|------------------------|
| <span data-ttu-id="f9ca4-164">引数</span><span class="sxs-lookup"><span data-stu-id="f9ca4-164">Argument</span></span>  | <span data-ttu-id="f9ca4-165">テストするパラメータ。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-165">The parameter to test.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f9ca4-166">戻り値</span><span class="sxs-lookup"><span data-stu-id="f9ca4-166">Return value</span></span>

<span data-ttu-id="f9ca4-167">パラメータの既定値が使用された場合 **1**、それ以外の場合は、**0** (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-167">**1** if the default value for the parameter was used; otherwise, **0** (zero).</span></span>

### <a name="example"></a><span data-ttu-id="f9ca4-168">例</span><span class="sxs-lookup"><span data-stu-id="f9ca4-168">Example</span></span>

    static void prmIsDefaultExample(Args _arg)
    {
            void fn(boolean b = true, int j = 42)
            {
                    if (prmIsDefault(b) == 1)
                    {
                            print "First parameter is using the default value.";
                    }
                    else
                    {
                            print "First parameter is not using the default value.";
                    }
            }
            fn();
            fn(false);
    }

## <a name="runas"></a><span data-ttu-id="f9ca4-169">runAs</span><span class="sxs-lookup"><span data-stu-id="f9ca4-169">runAs</span></span>
<span data-ttu-id="f9ca4-170">別のユーザーのセキュリティ コンテキストで、X++ メソッドを実行する呼び出し元を有効にします。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-170">Enables the caller to run an X++ method in the security context of another user.</span></span> <span data-ttu-id="f9ca4-171">この関数は、バッチ処理で最もよく使用されます。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-171">This function is most often used with batch processing.</span></span>

    container runAs(
            str userId,
            int classId,
            str staticMethodName
            [,
            container params,
            str company,
            str language,
            str partition
            ])

### <a name="parameters"></a><span data-ttu-id="f9ca4-172">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f9ca4-172">Parameters</span></span>

| <span data-ttu-id="f9ca4-173">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f9ca4-173">Parameter</span></span>        | <span data-ttu-id="f9ca4-174">説明</span><span class="sxs-lookup"><span data-stu-id="f9ca4-174">Description</span></span>                                                                                       |
|------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9ca4-175">userId</span><span class="sxs-lookup"><span data-stu-id="f9ca4-175">userId</span></span>           | <span data-ttu-id="f9ca4-176">偽装するユーザー。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-176">The user to impersonate.</span></span>                                                                          |
| <span data-ttu-id="f9ca4-177">classId</span><span class="sxs-lookup"><span data-stu-id="f9ca4-177">classId</span></span>          | <span data-ttu-id="f9ca4-178">偽装セッションで呼び出すクラス。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-178">The class to invoke in the impersonated session.</span></span>                                                  |
| <span data-ttu-id="f9ca4-179">staticMethodName</span><span class="sxs-lookup"><span data-stu-id="f9ca4-179">staticMethodName</span></span> | <span data-ttu-id="f9ca4-180">新しいユーザー コンテキストで呼び出すクラス メソッド。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-180">The class method to invoke in the new user context.</span></span>                                               |
| <span data-ttu-id="f9ca4-181">params</span><span class="sxs-lookup"><span data-stu-id="f9ca4-181">params</span></span>           | <span data-ttu-id="f9ca4-182">メソッドに渡すパラメーター (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-182">The parameters to pass to the method; optional.</span></span>                                                   |
| <span data-ttu-id="f9ca4-183">会社</span><span class="sxs-lookup"><span data-stu-id="f9ca4-183">company</span></span>          | <span data-ttu-id="f9ca4-184">偽装セッション用に選択された会社 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-184">The company that is selected for the impersonated session; optional.</span></span>                              |
| <span data-ttu-id="f9ca4-185">言語</span><span class="sxs-lookup"><span data-stu-id="f9ca4-185">language</span></span>         | <span data-ttu-id="f9ca4-186">偽装セッション用に選択された言語 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-186">The language that is selected for the impersonated session; optional.</span></span>                             |
| <span data-ttu-id="f9ca4-187">パーティション</span><span class="sxs-lookup"><span data-stu-id="f9ca4-187">partition</span></span>        | <span data-ttu-id="f9ca4-188">**getCurrentPartition** 関数によって返されるタイプのパーティション キー。省略可能です。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-188">The partition key of the type that is returned by the **getCurrentPartition** function; optional.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f9ca4-189">戻り値</span><span class="sxs-lookup"><span data-stu-id="f9ca4-189">Return value</span></span>

<span data-ttu-id="f9ca4-190">任意の値が返された場合に、**runAs** 関数によって呼び出されるメソッドの戻り値または値を保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-190">A container that holds the return value or values of the method that is called by the **runAs** function, if any values were returned.</span></span>

### <a name="remarks"></a><span data-ttu-id="f9ca4-191">備考</span><span class="sxs-lookup"><span data-stu-id="f9ca4-191">Remarks</span></span>

<span data-ttu-id="f9ca4-192">この関数を使用すると、別のユーザーとしてコードを実行できます。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-192">This function makes it possible to run code as another user.</span></span> <span data-ttu-id="f9ca4-193">この機能はセキュリティ上の脅威です。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-193">This capability presents a security threat.</span></span> <span data-ttu-id="f9ca4-194">したがって、この関数は、[コード アクセス セキュリティ](http://msdn.microsoft.com/library/09299e91-5b73-4cf5-a17e-f1f39b6bae76(AX.60).aspx)で実行されます。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-194">Therefore, this function runs under [Code Access Security](http://msdn.microsoft.com/library/09299e91-5b73-4cf5-a17e-f1f39b6bae76(AX.60).aspx).</span></span> <span data-ttu-id="f9ca4-195">サーバー上でこの関数を呼び出すには、**RunAsPermission** クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-195">Calls to this function on the server require permission from the **RunAsPermission** class.</span></span> <span data-ttu-id="f9ca4-196">このアプリケーション プログラミング インターフェイス (API) を使用するたびに、脅威なモデル化とする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-196">Each use of this application programming interface (API) should be threat-modeled.</span></span> <span data-ttu-id="f9ca4-197">セキュリティの脆弱性が見つかった場合は、この API への入力を検証します。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-197">If a security vulnerability is discovered, validate input to this API.</span></span> <span data-ttu-id="f9ca4-198">デバッガーは、**runAs** 関数を使用して呼び出されるメソッドにあるブレークポイントを無視することがあります。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-198">The debugger might ignore breakpoints that are located in a method that is called by using the **runAs** function.</span></span> <span data-ttu-id="f9ca4-199">**runAs** 関数として実行される X++ コードは Microsoft .NET Framework の共通中間言語 (CIL) として実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-199">X++ code that is executed by the **runAs** function must run as Microsoft .NET Framework Common Intermediate Language (CIL).</span></span> <span data-ttu-id="f9ca4-200">CIL が対象となる静的メソッドに対して生成されていない場合、メソッドが見つからないことを示すエラーメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-200">If CIL hasn't been generated for the target static method, an error message indicates that the method isn't found.</span></span> <span data-ttu-id="f9ca4-201">**PartitionKey** システムの型は、*partition* パラメーターの正確な型です。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-201">The **PartitionKey** system type is the exact type of the *partition* parameter.</span></span> <span data-ttu-id="f9ca4-202">**PartitionKey** は最大長が 8 文字の文字列です。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-202">**PartitionKey** is a string that has a maximum length of eight characters.</span></span>

### <a name="example"></a><span data-ttu-id="f9ca4-203">例</span><span class="sxs-lookup"><span data-stu-id="f9ca4-203">Example</span></span>

<span data-ttu-id="f9ca4-204">次の例では、**EventJobDueDate** クラスの **runDueDateEventsForUser** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-204">The following example calls the **runDueDateEventsForUser** method in the **EventJobDueDate** class.</span></span> <span data-ttu-id="f9ca4-205">このコードは、ユーザーのセキュリティ コンテキストで実行されます。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-205">The code runs in the security context of a user.</span></span> <span data-ttu-id="f9ca4-206">新しいクラスのメソッドに適用することによって、このコードを実行します。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-206">Run this code by applying it to a method in a new class.</span></span>

    server static public void Main(Args _args)
    {
            RunAsPermission perm;
            UserId runAsUser;
            SysUserInfo userInfo;
            userInfo = SysUserInfo::find();
            runAsUser = userInfo.Id;
            perm = new RunAsPermission(runAsUser);
            perm.assert();
            runAs(runAsUser, classnum(EventJobDueDate), "runDueDateEventsForUser");
            CodeAccessPermission::revertAssert();
    }

## <a name="setprefix"></a><span data-ttu-id="f9ca4-207">setPrefix</span><span class="sxs-lookup"><span data-stu-id="f9ca4-207">setPrefix</span></span>
<span data-ttu-id="f9ca4-208">現在の実行スコープの接頭語を設定します。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-208">Sets the prefix for the current execution scope.</span></span>

    int setPrefix(str _prefix)

### <a name="parameters"></a><span data-ttu-id="f9ca4-209">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f9ca4-209">Parameters</span></span>

| <span data-ttu-id="f9ca4-210">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f9ca4-210">Parameter</span></span> | <span data-ttu-id="f9ca4-211">説明</span><span class="sxs-lookup"><span data-stu-id="f9ca4-211">Description</span></span>                                 |
|-----------|---------------------------------------------|
| <span data-ttu-id="f9ca4-212">\_接頭語</span><span class="sxs-lookup"><span data-stu-id="f9ca4-212">\_prefix</span></span>  | <span data-ttu-id="f9ca4-213">現在の実行スコープの接頭語。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-213">The prefix for the current execution scope.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f9ca4-214">戻り値</span><span class="sxs-lookup"><span data-stu-id="f9ca4-214">Return value</span></span>

<span data-ttu-id="f9ca4-215">**0** 接頭語が正常に設定された場合。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-215">**0** if the prefix was set successfully.</span></span>

### <a name="remarks"></a><span data-ttu-id="f9ca4-216">備考</span><span class="sxs-lookup"><span data-stu-id="f9ca4-216">Remarks</span></span>

<span data-ttu-id="f9ca4-217">**getPrefix** 関数を使用すると、実行の完全な接頭辞を取得できます。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-217">The complete prefix for the execution can be fetched by using the **getPrefix** function.</span></span> <span data-ttu-id="f9ca4-218">スコープが残っているときは、接頭語が前のレベルに自動的にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-218">When the scope is left, the prefix is automatically reset to the previous level.</span></span> <span data-ttu-id="f9ca4-219">接頭語メカニズムを使用すると、アプリケーションが実行したトランザクションについての正確なエラー メッセージの書き込みがより簡単になります。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-219">The prefix mechanism makes it more straightforward to write precise error messages about the transactions that an application performs.</span></span> <span data-ttu-id="f9ca4-220">たとえば、**AA** メソッドは **BB** メソッドを呼び出し、各メソッドは **setPrefix** 機能を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-220">For example, the **AA** method calls the **BB** method, and each method calls the **setPrefix** function.</span></span> <span data-ttu-id="f9ca4-221">**BB** メソッドが情報ログに書き込んだメッセージは、階層内で入れ子になって表示されます。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-221">Messages that the **BB** method writes to the Infolog appear nested in a hierarchy.</span></span> <span data-ttu-id="f9ca4-222">**BB** メソッドが終了し、コントロールが **AA** メソッドに戻ると、**BB** メソッドによって設定された接頭語は後続のメッセージには関連付けられません。</span><span class="sxs-lookup"><span data-stu-id="f9ca4-222">When the **BB** method ends, and control returns to the **AA** method, the prefix that was set by the **BB** method isn't attached to subsequent messages.</span></span>

### <a name="example"></a><span data-ttu-id="f9ca4-223">例</span><span class="sxs-lookup"><span data-stu-id="f9ca4-223">Example</span></span>

    static void setPrefixExample(Args _arg)
    {
            int i;
            i = setPrefix("Prefix");
            print i;
    }




