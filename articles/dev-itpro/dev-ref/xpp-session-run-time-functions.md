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
ms.sourcegitcommit: 46315f12e1d26c29f9df7c6809bfd444f4dc5ad5
ms.openlocfilehash: a3cf485e8ab08145ae09125df8afde2e3c487cd7
ms.contentlocale: ja-jp
ms.lasthandoff: 10/09/2018

---

# <a name="x-session-runtime-functions"></a><span data-ttu-id="6b297-103">X++ セッション ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="6b297-103">X++ session runtime functions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b297-104">このトピックでは、セッション ランタイム関数について説明します。</span><span class="sxs-lookup"><span data-stu-id="6b297-104">This topic describes the session run-time functions.</span></span>

<a name="curext"></a><span data-ttu-id="6b297-105">curExt</span><span class="sxs-lookup"><span data-stu-id="6b297-105">curExt</span></span>
------

<span data-ttu-id="6b297-106">現在の会社に使用できる拡張を取得します。</span><span class="sxs-lookup"><span data-stu-id="6b297-106">Retrieves the extension that is used for the current company.</span></span>

    str curExt()

### <a name="return-value"></a><span data-ttu-id="6b297-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="6b297-107">Return value</span></span>

<span data-ttu-id="6b297-108">現在の会社の内線電話番号。</span><span class="sxs-lookup"><span data-stu-id="6b297-108">The extension for the current company.</span></span>

### <a name="example"></a><span data-ttu-id="6b297-109">例</span><span class="sxs-lookup"><span data-stu-id="6b297-109">Example</span></span>

    static void curExtExample(Args _arg)
    {
            str s;
            // Sets s to the extension of the current company.
            s = curExt();
            print "Current extension is " + s;
    }

## <a name="curuserid"></a><span data-ttu-id="6b297-110">curUserId</span><span class="sxs-lookup"><span data-stu-id="6b297-110">curUserId</span></span>
<span data-ttu-id="6b297-111">現在のユーザーを表す数値以外の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6b297-111">Retrieves the nonnumeric ID that represents the current user.</span></span>

    str curUserId()

### <a name="return-value"></a><span data-ttu-id="6b297-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="6b297-112">Return value</span></span>

<span data-ttu-id="6b297-113">現在のユーザーを表す数値以外の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6b297-113">The nonnumeric ID that represents the current user.</span></span>

### <a name="example"></a><span data-ttu-id="6b297-114">例</span><span class="sxs-lookup"><span data-stu-id="6b297-114">Example</span></span>

    static void curUserIdExample(Args _arg)
    {
            str s;
            s = curUserId();
            print "Current user ID is " + s;
    }

## <a name="funcname"></a><span data-ttu-id="6b297-115">funcName</span><span class="sxs-lookup"><span data-stu-id="6b297-115">funcName</span></span>
<span data-ttu-id="6b297-116">現在の関数コンテキストを含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="6b297-116">Retrieves a string that contains the current function context.</span></span>

    str funcName()

### <a name="return-value"></a><span data-ttu-id="6b297-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="6b297-117">Return value</span></span>

<span data-ttu-id="6b297-118">このメソッドを実行しているメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="6b297-118">The name of the method that is executing this method.</span></span>

### <a name="remarks"></a><span data-ttu-id="6b297-119">備考</span><span class="sxs-lookup"><span data-stu-id="6b297-119">Remarks</span></span>

<span data-ttu-id="6b297-120">実行がテーブルまたはクラス メンバー内に現在ある場合は、メソッドの名前に、そのテーブルまたはクラスの名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="6b297-120">If execution is currently within the member of a table or class, the name of the method is prefixed with the name of that table or class.</span></span>

### <a name="example"></a><span data-ttu-id="6b297-121">例</span><span class="sxs-lookup"><span data-stu-id="6b297-121">Example</span></span>

    static void funcNameExample(Args _arg)
    {
            print "Current function context is " + funcName();
    }

## <a name="getcurrentpartition"></a><span data-ttu-id="6b297-122">getCurrentPartition</span><span class="sxs-lookup"><span data-stu-id="6b297-122">getCurrentPartition</span></span>
<span data-ttu-id="6b297-123">現在のパーティションの短い名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="6b297-123">Retrieves the short name of the current partition.</span></span>

    str getCurrentPartition()

### <a name="return-value"></a><span data-ttu-id="6b297-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="6b297-124">Return value</span></span>

<span data-ttu-id="6b297-125">現在のパーティションの短い名前。</span><span class="sxs-lookup"><span data-stu-id="6b297-125">The short name of the current partition.</span></span>

### <a name="remarks"></a><span data-ttu-id="6b297-126">備考</span><span class="sxs-lookup"><span data-stu-id="6b297-126">Remarks</span></span>

<span data-ttu-id="6b297-127">返されるデータ パーティション名の最大の長さは 8 文字です。</span><span class="sxs-lookup"><span data-stu-id="6b297-127">The maximum length of the data partition name that is returned is eight characters.</span></span>

### <a name="example"></a><span data-ttu-id="6b297-128">例</span><span class="sxs-lookup"><span data-stu-id="6b297-128">Example</span></span>

<span data-ttu-id="6b297-129">次のコード例は、X++ 言語の **getCurrentPartition** 関数、および関連する関数またはメソッドへの呼び出しおよび出力を示しています。</span><span class="sxs-lookup"><span data-stu-id="6b297-129">The following code example shows calls to, and output from, the **getCurrentPartition** function of the X++ language, and related functions or methods.</span></span>

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

## <a name="getcurrentpartitionrecid"></a><span data-ttu-id="6b297-130">getCurrentPartitionRecId</span><span class="sxs-lookup"><span data-stu-id="6b297-130">getCurrentPartitionRecId</span></span>
<span data-ttu-id="6b297-131">現在のパーティションの **RecId** フィールドを取得します。</span><span class="sxs-lookup"><span data-stu-id="6b297-131">Retrieves the **RecId** field of the current partition.</span></span>

    int64 getCurrentPartitionRecId()

### <a name="return-value"></a><span data-ttu-id="6b297-132">戻り値</span><span class="sxs-lookup"><span data-stu-id="6b297-132">Return value</span></span>

<span data-ttu-id="6b297-133">現在のデータ パーティションの **RecId** フィールド。</span><span class="sxs-lookup"><span data-stu-id="6b297-133">The **RecId** field of the current data partition.</span></span>

### <a name="remarks"></a><span data-ttu-id="6b297-134">備考</span><span class="sxs-lookup"><span data-stu-id="6b297-134">Remarks</span></span>

<span data-ttu-id="6b297-135">**getCurrentPartitionRecId** 関数に依存するコード例を参照するには、[[パーティションのフィルターを直接 Transact-SQL に含める方法](http://msdn.microsoft.com/library/5ce90a42-e862-464e-90bc-1eb16a8afd1a(AX.60).aspx)] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b297-135">To see a code example that relies on the **getCurrentPartitionRecId** function, see [How to: Include a Filter for Partition in Direct Transact-SQL](http://msdn.microsoft.com/library/5ce90a42-e862-464e-90bc-1eb16a8afd1a(AX.60).aspx).</span></span>

### <a name="example"></a><span data-ttu-id="6b297-136">例</span><span class="sxs-lookup"><span data-stu-id="6b297-136">Example</span></span>

<span data-ttu-id="6b297-137">次のコード例は、X++ 言語の **getCurrentPartitionRecId** 関数、および関連する関数またはメソッドへの呼び出しおよび出力を示しています。</span><span class="sxs-lookup"><span data-stu-id="6b297-137">The following code example shows calls to, and output from, the **getCurrentPartitionRecId** function of the X++ language, and related functions or methods.</span></span>

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

## <a name="getprefix"></a><span data-ttu-id="6b297-138">getPrefix</span><span class="sxs-lookup"><span data-stu-id="6b297-138">getPrefix</span></span>
<span data-ttu-id="6b297-139">**setPrefix** 関数が連続して呼び出された後、現在の実行接頭辞を取得します。</span><span class="sxs-lookup"><span data-stu-id="6b297-139">Retrieves the current execution prefix after successive calls to the **setPrefix** function.</span></span>

    str getPrefix()

### <a name="return-value"></a><span data-ttu-id="6b297-140">戻り値</span><span class="sxs-lookup"><span data-stu-id="6b297-140">Return value</span></span>

<span data-ttu-id="6b297-141">現在の実行接頭語。</span><span class="sxs-lookup"><span data-stu-id="6b297-141">The current execution prefix.</span></span>

### <a name="remarks"></a><span data-ttu-id="6b297-142">備考</span><span class="sxs-lookup"><span data-stu-id="6b297-142">Remarks</span></span>

<span data-ttu-id="6b297-143">接頭語メカニズムを使用すると、アプリケーションが実行したトランザクションについての正確なエラー メッセージの書き込みがより簡単になります。</span><span class="sxs-lookup"><span data-stu-id="6b297-143">The prefix mechanism makes it more straightforward to write precise error messages about the transactions that an application performs.</span></span> <span data-ttu-id="6b297-144">情報ログでは階層表示が作成されるため、各エラーの原因を特定するのが容易になります。</span><span class="sxs-lookup"><span data-stu-id="6b297-144">Because a hierarchical display is created in the Infolog, it can be easier to determine where each error came from.</span></span>

### <a name="example"></a><span data-ttu-id="6b297-145">例</span><span class="sxs-lookup"><span data-stu-id="6b297-145">Example</span></span>

    static void getPrefixExample(Args _arg)
    {
            setPrefix("Prefix");
            setPrefix("Another prefix");
            print getPrefix();
    }

## <a name="sessionid"></a><span data-ttu-id="6b297-146">sessionId</span><span class="sxs-lookup"><span data-stu-id="6b297-146">sessionId</span></span>
<span data-ttu-id="6b297-147">現在のセッションのセッション番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="6b297-147">Retrieves the session number of the current session.</span></span>

    int sessionId()

### <a name="return-value"></a><span data-ttu-id="6b297-148">戻り値</span><span class="sxs-lookup"><span data-stu-id="6b297-148">Return value</span></span>

<span data-ttu-id="6b297-149">現在のセッションの数値 ID。</span><span class="sxs-lookup"><span data-stu-id="6b297-149">The numeric ID of the current session.</span></span>

### <a name="remarks"></a><span data-ttu-id="6b297-150">備考</span><span class="sxs-lookup"><span data-stu-id="6b297-150">Remarks</span></span>

<span data-ttu-id="6b297-151">セッション番号は、クライアントの起動時に割り当てられ、Application Object Server (AOS) に接続します。</span><span class="sxs-lookup"><span data-stu-id="6b297-151">A session number is assigned when the client is started and connects to Application Object Server (AOS).</span></span> <span data-ttu-id="6b297-152">クライアントの存続中にこの関数を呼び出すたびに、同じ整数値が戻されます。</span><span class="sxs-lookup"><span data-stu-id="6b297-152">Every call of this function during the life of the client returns the same integer value.</span></span> <span data-ttu-id="6b297-153">返された値は、**SessionID** 拡張データ型と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="6b297-153">The returned value is compatible with the **SessionID** extended data type.</span></span> <span data-ttu-id="6b297-154">**contains** メソッドは、個々のユーザー セッションに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="6b297-154">The **contains** methods return information about individual user sessions.</span></span>

### <a name="example"></a><span data-ttu-id="6b297-155">例</span><span class="sxs-lookup"><span data-stu-id="6b297-155">Example</span></span>

    static void sessionIdExample(Args _arg)
    {
            int session;
            session = sessionId();
            print "This session ID is number " + int2Str(session);
    }

## <a name="prmisdefault"></a><span data-ttu-id="6b297-156">prmIsDefault</span><span class="sxs-lookup"><span data-stu-id="6b297-156">prmIsDefault</span></span>
<span data-ttu-id="6b297-157">現在のメソッドの指定されたパラメータに既定値があるかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="6b297-157">Determines whether the specified parameter for the current method has the default value.</span></span>

    int prmIsDefault(anytype argument)

### <a name="parameters"></a><span data-ttu-id="6b297-158">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6b297-158">Parameters</span></span>

| <span data-ttu-id="6b297-159">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6b297-159">Parameter</span></span> | <span data-ttu-id="6b297-160">説明</span><span class="sxs-lookup"><span data-stu-id="6b297-160">Description</span></span>            |
|-----------|------------------------|
| <span data-ttu-id="6b297-161">引数</span><span class="sxs-lookup"><span data-stu-id="6b297-161">Argument</span></span>  | <span data-ttu-id="6b297-162">テストするパラメータ。</span><span class="sxs-lookup"><span data-stu-id="6b297-162">The parameter to test.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6b297-163">戻り値</span><span class="sxs-lookup"><span data-stu-id="6b297-163">Return value</span></span>

<span data-ttu-id="6b297-164">パラメータの既定値が使用された場合 **1**、それ以外の場合は、**0** (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="6b297-164">**1** if the default value for the parameter was used; otherwise, **0** (zero).</span></span>

### <a name="example"></a><span data-ttu-id="6b297-165">例</span><span class="sxs-lookup"><span data-stu-id="6b297-165">Example</span></span>

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

## <a name="runas"></a><span data-ttu-id="6b297-166">runAs</span><span class="sxs-lookup"><span data-stu-id="6b297-166">runAs</span></span>
<span data-ttu-id="6b297-167">別のユーザーのセキュリティ コンテキストで、X++ メソッドを実行する呼び出し元を有効にします。</span><span class="sxs-lookup"><span data-stu-id="6b297-167">Enables the caller to run an X++ method in the security context of another user.</span></span> <span data-ttu-id="6b297-168">この関数は、バッチ処理で最もよく使用されます。</span><span class="sxs-lookup"><span data-stu-id="6b297-168">This function is most often used with batch processing.</span></span>

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

### <a name="parameters"></a><span data-ttu-id="6b297-169">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6b297-169">Parameters</span></span>

| <span data-ttu-id="6b297-170">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6b297-170">Parameter</span></span>        | <span data-ttu-id="6b297-171">説明</span><span class="sxs-lookup"><span data-stu-id="6b297-171">Description</span></span>                                                                                       |
|------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b297-172">userId</span><span class="sxs-lookup"><span data-stu-id="6b297-172">userId</span></span>           | <span data-ttu-id="6b297-173">偽装するユーザー。</span><span class="sxs-lookup"><span data-stu-id="6b297-173">The user to impersonate.</span></span>                                                                          |
| <span data-ttu-id="6b297-174">classId</span><span class="sxs-lookup"><span data-stu-id="6b297-174">classId</span></span>          | <span data-ttu-id="6b297-175">偽装セッションで呼び出すクラス。</span><span class="sxs-lookup"><span data-stu-id="6b297-175">The class to invoke in the impersonated session.</span></span>                                                  |
| <span data-ttu-id="6b297-176">staticMethodName</span><span class="sxs-lookup"><span data-stu-id="6b297-176">staticMethodName</span></span> | <span data-ttu-id="6b297-177">新しいユーザー コンテキストで呼び出すクラス メソッド。</span><span class="sxs-lookup"><span data-stu-id="6b297-177">The class method to invoke in the new user context.</span></span>                                               |
| <span data-ttu-id="6b297-178">params</span><span class="sxs-lookup"><span data-stu-id="6b297-178">params</span></span>           | <span data-ttu-id="6b297-179">メソッドに渡すパラメーター (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="6b297-179">The parameters to pass to the method; optional.</span></span>                                                   |
| <span data-ttu-id="6b297-180">会社</span><span class="sxs-lookup"><span data-stu-id="6b297-180">company</span></span>          | <span data-ttu-id="6b297-181">偽装セッション用に選択された会社 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6b297-181">The company that is selected for the impersonated session; optional.</span></span>                              |
| <span data-ttu-id="6b297-182">言語</span><span class="sxs-lookup"><span data-stu-id="6b297-182">language</span></span>         | <span data-ttu-id="6b297-183">偽装セッション用に選択された言語 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6b297-183">The language that is selected for the impersonated session; optional.</span></span>                             |
| <span data-ttu-id="6b297-184">パーティション</span><span class="sxs-lookup"><span data-stu-id="6b297-184">partition</span></span>        | <span data-ttu-id="6b297-185">**getCurrentPartition** 関数によって返されるタイプのパーティション キー。省略可能です。</span><span class="sxs-lookup"><span data-stu-id="6b297-185">The partition key of the type that is returned by the **getCurrentPartition** function; optional.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6b297-186">戻り値</span><span class="sxs-lookup"><span data-stu-id="6b297-186">Return value</span></span>

<span data-ttu-id="6b297-187">任意の値が返された場合に、**runAs** 関数によって呼び出されるメソッドの戻り値または値を保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="6b297-187">A container that holds the return value or values of the method that is called by the **runAs** function, if any values were returned.</span></span>

### <a name="remarks"></a><span data-ttu-id="6b297-188">備考</span><span class="sxs-lookup"><span data-stu-id="6b297-188">Remarks</span></span>

<span data-ttu-id="6b297-189">この関数を使用すると、別のユーザーとしてコードを実行できます。</span><span class="sxs-lookup"><span data-stu-id="6b297-189">This function makes it possible to run code as another user.</span></span> <span data-ttu-id="6b297-190">この機能はセキュリティ上の脅威です。</span><span class="sxs-lookup"><span data-stu-id="6b297-190">This capability presents a security threat.</span></span> <span data-ttu-id="6b297-191">したがって、この関数は、[コード アクセス セキュリティ](http://msdn.microsoft.com/library/09299e91-5b73-4cf5-a17e-f1f39b6bae76(AX.60).aspx)で実行されます。</span><span class="sxs-lookup"><span data-stu-id="6b297-191">Therefore, this function runs under [Code Access Security](http://msdn.microsoft.com/library/09299e91-5b73-4cf5-a17e-f1f39b6bae76(AX.60).aspx).</span></span> <span data-ttu-id="6b297-192">サーバー上でこの関数を呼び出すには、**RunAsPermission** クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="6b297-192">Calls to this function on the server require permission from the **RunAsPermission** class.</span></span> <span data-ttu-id="6b297-193">このアプリケーション プログラミング インターフェイス (API) を使用するたびに、脅威なモデル化とする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b297-193">Each use of this application programming interface (API) should be threat-modeled.</span></span> <span data-ttu-id="6b297-194">セキュリティの脆弱性が見つかった場合は、この API への入力を検証します。</span><span class="sxs-lookup"><span data-stu-id="6b297-194">If a security vulnerability is discovered, validate input to this API.</span></span> <span data-ttu-id="6b297-195">デバッガーは、**runAs** 関数を使用して呼び出されるメソッドにあるブレークポイントを無視することがあります。</span><span class="sxs-lookup"><span data-stu-id="6b297-195">The debugger might ignore breakpoints that are located in a method that is called by using the **runAs** function.</span></span> <span data-ttu-id="6b297-196">**runAs** 関数として実行される X++ コードは Microsoft .NET Framework の共通中間言語 (CIL) として実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b297-196">X++ code that is executed by the **runAs** function must run as Microsoft .NET Framework Common Intermediate Language (CIL).</span></span> <span data-ttu-id="6b297-197">CIL が対象となる静的メソッドに対して生成されていない場合、メソッドが見つからないことを示すエラーメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6b297-197">If CIL hasn't been generated for the target static method, an error message indicates that the method isn't found.</span></span> <span data-ttu-id="6b297-198">**PartitionKey** システムの型は、*partition* パラメーターの正確な型です。</span><span class="sxs-lookup"><span data-stu-id="6b297-198">The **PartitionKey** system type is the exact type of the *partition* parameter.</span></span> <span data-ttu-id="6b297-199">**PartitionKey** は最大長が 8 文字の文字列です。</span><span class="sxs-lookup"><span data-stu-id="6b297-199">**PartitionKey** is a string that has a maximum length of eight characters.</span></span>

### <a name="example"></a><span data-ttu-id="6b297-200">例</span><span class="sxs-lookup"><span data-stu-id="6b297-200">Example</span></span>

<span data-ttu-id="6b297-201">次の例では、**EventJobDueDate** クラスの **runDueDateEventsForUser** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6b297-201">The following example calls the **runDueDateEventsForUser** method in the **EventJobDueDate** class.</span></span> <span data-ttu-id="6b297-202">このコードは、ユーザーのセキュリティ コンテキストで実行されます。</span><span class="sxs-lookup"><span data-stu-id="6b297-202">The code runs in the security context of a user.</span></span> <span data-ttu-id="6b297-203">新しいクラスのメソッドに適用することによって、このコードを実行します。</span><span class="sxs-lookup"><span data-stu-id="6b297-203">Run this code by applying it to a method in a new class.</span></span>

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

## <a name="setprefix"></a><span data-ttu-id="6b297-204">setPrefix</span><span class="sxs-lookup"><span data-stu-id="6b297-204">setPrefix</span></span>
<span data-ttu-id="6b297-205">現在の実行スコープの接頭語を設定します。</span><span class="sxs-lookup"><span data-stu-id="6b297-205">Sets the prefix for the current execution scope.</span></span>

    int setPrefix(str _prefix)

### <a name="parameters"></a><span data-ttu-id="6b297-206">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6b297-206">Parameters</span></span>

| <span data-ttu-id="6b297-207">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6b297-207">Parameter</span></span> | <span data-ttu-id="6b297-208">説明</span><span class="sxs-lookup"><span data-stu-id="6b297-208">Description</span></span>                                 |
|-----------|---------------------------------------------|
| <span data-ttu-id="6b297-209">\_接頭語</span><span class="sxs-lookup"><span data-stu-id="6b297-209">\_prefix</span></span>  | <span data-ttu-id="6b297-210">現在の実行スコープの接頭語。</span><span class="sxs-lookup"><span data-stu-id="6b297-210">The prefix for the current execution scope.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6b297-211">戻り値</span><span class="sxs-lookup"><span data-stu-id="6b297-211">Return value</span></span>

<span data-ttu-id="6b297-212">**0** 接頭語が正常に設定された場合。</span><span class="sxs-lookup"><span data-stu-id="6b297-212">**0** if the prefix was set successfully.</span></span>

### <a name="remarks"></a><span data-ttu-id="6b297-213">備考</span><span class="sxs-lookup"><span data-stu-id="6b297-213">Remarks</span></span>

<span data-ttu-id="6b297-214">**getPrefix** 関数を使用すると、実行の完全な接頭辞を取得できます。</span><span class="sxs-lookup"><span data-stu-id="6b297-214">The complete prefix for the execution can be fetched by using the **getPrefix** function.</span></span> <span data-ttu-id="6b297-215">スコープが残っているときは、接頭語が前のレベルに自動的にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="6b297-215">When the scope is left, the prefix is automatically reset to the previous level.</span></span> <span data-ttu-id="6b297-216">接頭語メカニズムを使用すると、アプリケーションが実行したトランザクションについての正確なエラー メッセージの書き込みがより簡単になります。</span><span class="sxs-lookup"><span data-stu-id="6b297-216">The prefix mechanism makes it more straightforward to write precise error messages about the transactions that an application performs.</span></span> <span data-ttu-id="6b297-217">たとえば、**AA** メソッドは **BB** メソッドを呼び出し、各メソッドは **setPrefix** 機能を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6b297-217">For example, the **AA** method calls the **BB** method, and each method calls the **setPrefix** function.</span></span> <span data-ttu-id="6b297-218">**BB** メソッドが情報ログに書き込んだメッセージは、階層内で入れ子になって表示されます。</span><span class="sxs-lookup"><span data-stu-id="6b297-218">Messages that the **BB** method writes to the Infolog appear nested in a hierarchy.</span></span> <span data-ttu-id="6b297-219">**BB** メソッドが終了し、コントロールが **AA** メソッドに戻ると、**BB** メソッドによって設定された接頭語は後続のメッセージには関連付けられません。</span><span class="sxs-lookup"><span data-stu-id="6b297-219">When the **BB** method ends, and control returns to the **AA** method, the prefix that was set by the **BB** method isn't attached to subsequent messages.</span></span>

### <a name="example"></a><span data-ttu-id="6b297-220">例</span><span class="sxs-lookup"><span data-stu-id="6b297-220">Example</span></span>

    static void setPrefixExample(Args _arg)
    {
            int i;
            i = setPrefix("Prefix");
            print i;
    }




