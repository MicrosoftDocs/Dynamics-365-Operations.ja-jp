---
title: RunAsPermission クラス
description: このトピックでは、RunAsPermission クラスについて説明します。
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
ms.openlocfilehash: 1272adb7eafda535d1b60fc54cdcb673703d58c7
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502821"
---
# <a name="class-runaspermission"></a><span data-ttu-id="e0572-103">クラス RunAsPermission</span><span class="sxs-lookup"><span data-stu-id="e0572-103">Class RunAsPermission</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class RunAsPermission extends CodeAccessPermission
```

<span data-ttu-id="e0572-104">RunAsPermssion クラスは、別のユーザーのセキュリティ コンテキストでコードの実行を制御します。</span><span class="sxs-lookup"><span data-stu-id="e0572-104">The RunAsPermssion class controls the execution of code in the security context of another user.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0572-105">備考</span><span class="sxs-lookup"><span data-stu-id="e0572-105">Remarks</span></span>

<span data-ttu-id="e0572-106">保護された API が実行される前に、対応する CodeAccessPermission.demand メソッドが呼び出される、通常はサーバー層である、同じ層で assert メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0572-106">You must call the assert method on the same tier, usually the server tier, that the corresponding CodeAccessPermission.demand method is called on before the protected API is executed.</span></span> <span data-ttu-id="e0572-107">次のいずれかでサーバー層のメソッドを呼び出します。RunAsPermission クラスは、runAs 関数のアクセス許可をチェックするように設計されています。</span><span class="sxs-lookup"><span data-stu-id="e0572-107">Call a method on the server tier from one of the following: The RunAsPermission class is designed to check permissions for the runAs function.</span></span> <span data-ttu-id="e0572-108">アクセス許可によって保護されたすべての API のリストについては、「セキュリティで保護された API」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0572-108">For a list of all APIs protected by permissions, see Secured APIs.</span></span>

-   <span data-ttu-id="e0572-109">サーバー静的メソッド �または�</span><span class="sxs-lookup"><span data-stu-id="e0572-109">A server static method �or�</span></span>
-   <span data-ttu-id="e0572-110">RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド</span><span class="sxs-lookup"><span data-stu-id="e0572-110">A class instance method that is set to run on the server by using the RunOn class property</span></span>

## <a name="examples"></a><span data-ttu-id="e0572-111">例</span><span class="sxs-lookup"><span data-stu-id="e0572-111">Examples</span></span>

<span data-ttu-id="e0572-112">次のコード例は、RunAsPermission クラスの新しいインスタンスを示しています。</span><span class="sxs-lookup"><span data-stu-id="e0572-112">The following code example shows a new instance of the RunAsPermission class.</span></span> <span data-ttu-id="e0572-113">assert メソッドが呼び出され、コードが runAs 関数を呼び出して、別のユーザーのセキュリティ コンテキストで EventJobDueDate.:runDueDateEventsForUser メソッドを実行できることが宣言されます。</span><span class="sxs-lookup"><span data-stu-id="e0572-113">The assert method is called to declare that the code can then call the runAs function to run the EventJobDueDate.:runDueDateEventsForUser method in the security context of another user.</span></span>

```xpp
server static void main(Args args) 
{ 
    RunAsPermission _perm; 
    UserId          _runAsUser; 
    SysUserInfo     _userInfo; 
    _userInfo = SysUserInfo::find(); 
    _runAsUser = _userInfo.Id; 
    _perm = new RunAsPermission(_runAsUser); 
    _perm.assert(); 
    // Invoke the protected API. 
    RunAs(_runAsUser, classnum(EventJobDueDate), "runDueDateEventsForUser"); 
    // Optionally, call revertAssert() to limit the scope of assert. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="methods"></a><span data-ttu-id="e0572-114">メソッド</span><span class="sxs-lookup"><span data-stu-id="e0572-114">Methods</span></span>

| <span data-ttu-id="e0572-115">方法</span><span class="sxs-lookup"><span data-stu-id="e0572-115">Method</span></span>                                                 | <span data-ttu-id="e0572-116">説明</span><span class="sxs-lookup"><span data-stu-id="e0572-116">Description</span></span>                                                                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0572-117">public CodeAccessPermission copy()</span><span class="sxs-lookup"><span data-stu-id="e0572-117">public CodeAccessPermission copy()</span></span>                     | <span data-ttu-id="e0572-118">アクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="e0572-118">Creates and returns a copy of a permission class object.</span></span>                                                            |
| <span data-ttu-id="e0572-119">public boolean isSubsetOf(CodeAccessPermission target)</span><span class="sxs-lookup"><span data-stu-id="e0572-119">public boolean isSubsetOf(CodeAccessPermission target)</span></span> | <span data-ttu-id="e0572-120">派生クラスによって上書きされたときに、現在のアクセス許可が指定されたアクセス許可のサブセットであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="e0572-120">Determines whether a current permission is a subset of the specified permission when overridden by a derived class.</span></span> |
| <span data-ttu-id="e0572-121">public void new(UserId userId)</span><span class="sxs-lookup"><span data-stu-id="e0572-121">public void new(UserId userId)</span></span>                         | <span data-ttu-id="e0572-122">CodeAccessPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e0572-122">Initializes a new instance of the CodeAccessPermission class.</span></span>                                                       |

## <a name="method-copy"></a><span data-ttu-id="e0572-123">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="e0572-123">Method copy</span></span>

<span data-ttu-id="e0572-124">アクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="e0572-124">Creates and returns a copy of a permission class object.</span></span>

```xpp
public CodeAccessPermission copy()
```

### <a name="return-value---copy"></a><span data-ttu-id="e0572-125">戻り値 - copy</span><span class="sxs-lookup"><span data-stu-id="e0572-125">Return Value - copy</span></span>

<span data-ttu-id="e0572-126">現在の派生クラスオブジェクトのコピーです。</span><span class="sxs-lookup"><span data-stu-id="e0572-126">A copy of the derived class object.</span></span>

### <a name="remarks---copy"></a><span data-ttu-id="e0572-127">備考 - copy</span><span class="sxs-lookup"><span data-stu-id="e0572-127">Remarks - copy</span></span>

<span data-ttu-id="e0572-128">API のセキュリティをさらに強化するプロセスの一部として、このメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="e0572-128">You can override this method as part of the process of making an API more secure.</span></span>

## <a name="method-issubsetof"></a><span data-ttu-id="e0572-129">メソッド isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="e0572-129">Method isSubsetOf</span></span>

<span data-ttu-id="e0572-130">派生クラスによって上書きされたときに、現在のアクセス許可が指定されたアクセス許可のサブセットであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="e0572-130">Determines whether a current permission is a subset of the specified permission when overridden by a derived class.</span></span>

```xpp
public boolean isSubsetOf(CodeAccessPermission target)
```

### <a name="parameters---issubsetof"></a><span data-ttu-id="e0572-131">パラメーター - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="e0572-131">Parameters - isSubsetOf</span></span>

<span data-ttu-id="e0572-132">target</span><span class="sxs-lookup"><span data-stu-id="e0572-132">target</span></span>  
<span data-ttu-id="e0572-133">CodeAccessPermission クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="e0572-133">A CodeAccessPermission class object.</span></span>

### <a name="return-value---issubsetof"></a><span data-ttu-id="e0572-134">戻り値 - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="e0572-134">Return Value - isSubsetOf</span></span>

<span data-ttu-id="e0572-135">現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="e0572-135">true if a current permission is a subset of a specified permission; otherwise, false.</span></span>

### <a name="remarks---issubsetof"></a><span data-ttu-id="e0572-136">備考 - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="e0572-136">Remarks - isSubsetOf</span></span>

<span data-ttu-id="e0572-137">API のセキュリティをさらに強化するプロセスの一部として、メソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="e0572-137">You can override the method as part of the process of making an API more secure.</span></span>

## <a name="method-new"></a><span data-ttu-id="e0572-138">メソッド new</span><span class="sxs-lookup"><span data-stu-id="e0572-138">Method new</span></span>

<span data-ttu-id="e0572-139">CodeAccessPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e0572-139">Initializes a new instance of the CodeAccessPermission class.</span></span>

```xpp
public void new(UserId userId)
```

### <a name="parameters---new"></a><span data-ttu-id="e0572-140">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="e0572-140">Parameters - new</span></span>

<span data-ttu-id="e0572-141">userId</span><span class="sxs-lookup"><span data-stu-id="e0572-141">userId</span></span>  
<span data-ttu-id="e0572-142">ユーザーを指定する userId システム データ型。</span><span class="sxs-lookup"><span data-stu-id="e0572-142">A userId system data type that specifies a user.</span></span>

### <a name="examples---new"></a><span data-ttu-id="e0572-143">例 - new</span><span class="sxs-lookup"><span data-stu-id="e0572-143">Examples - new</span></span>

<span data-ttu-id="e0572-144">次の例は、RunAsPermission クラスの新しいインスタンスを示しています。</span><span class="sxs-lookup"><span data-stu-id="e0572-144">The following example shows a new instance of the RunAsPermission class.</span></span> <span data-ttu-id="e0572-145">SysUserInfo テーブルは、userId パラメーターの初期化に使用されます。</span><span class="sxs-lookup"><span data-stu-id="e0572-145">The SysUserInfo table is used to initialize the userId parameter.</span></span>

```xpp
server static void main(Args args) 
{ 
    RunAsPermission _perm; 
    UserId          _userId; 
    SysUserInfo     _userInfo; 
    _userInfo = SysUserInfo::find(); 
    _userId = _userInfo.Id; 
    _perm = new RunAsPermission(_userId); 
```

```xpp
}
```

### <a name="remarks---new"></a><span data-ttu-id="e0572-146">備考 - new</span><span class="sxs-lookup"><span data-stu-id="e0572-146">Remarks - new</span></span>

<span data-ttu-id="e0572-147">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e0572-147">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="e0572-148">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="e0572-148">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="e0572-149">モード。</span><span class="sxs-lookup"><span data-stu-id="e0572-149">Mode.</span></span>            | <span data-ttu-id="e0572-150">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="e0572-150">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0572-151">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="e0572-151">-1 Exact.</span></span>        | <span data-ttu-id="e0572-152">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e0572-152">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="e0572-153">0 自動。</span><span class="sxs-lookup"><span data-stu-id="e0572-153">0 Auto.</span></span>          | <span data-ttu-id="e0572-154">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="e0572-154">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="e0572-155">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="e0572-155">1 Column height.</span></span> | <span data-ttu-id="e0572-156">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="e0572-156">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="e0572-157">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="e0572-157">The height and height calculation mode can be set separately.</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="e0572-158">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="e0572-158">Method rightMargin</span></span>

```xpp
public void rightMargin(Real value, Units unit)
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="e0572-159">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="e0572-159">Parameters - rightMargin</span></span>

<span data-ttu-id="e0572-160">値</span><span class="sxs-lookup"><span data-stu-id="e0572-160">value</span></span>  

<!-- -->

<span data-ttu-id="e0572-161">単位</span><span class="sxs-lookup"><span data-stu-id="e0572-161">unit</span></span>  

## <a name="method-left"></a><span data-ttu-id="e0572-162">メソッド left</span><span class="sxs-lookup"><span data-stu-id="e0572-162">Method left</span></span>

```xpp
public void left(Real value, Units unit)
```

### <a name="parameters---left"></a><span data-ttu-id="e0572-163">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="e0572-163">Parameters - left</span></span>

<span data-ttu-id="e0572-164">値</span><span class="sxs-lookup"><span data-stu-id="e0572-164">value</span></span>  

<!-- -->

<span data-ttu-id="e0572-165">単位</span><span class="sxs-lookup"><span data-stu-id="e0572-165">unit</span></span>  

## <a name="method-width"></a><span data-ttu-id="e0572-166">メソッド width</span><span class="sxs-lookup"><span data-stu-id="e0572-166">Method width</span></span>

<span data-ttu-id="e0572-167">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e0572-167">Gets or sets the width of the control.</span></span>

```xpp
public void width(Real value, Units unit)
```

### <a name="parameters---width"></a><span data-ttu-id="e0572-168">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="e0572-168">Parameters - width</span></span>

<span data-ttu-id="e0572-169">値</span><span class="sxs-lookup"><span data-stu-id="e0572-169">value</span></span>  

<!-- -->

<span data-ttu-id="e0572-170">単位</span><span class="sxs-lookup"><span data-stu-id="e0572-170">unit</span></span>  

### <a name="remarks---width"></a><span data-ttu-id="e0572-171">備考 - width</span><span class="sxs-lookup"><span data-stu-id="e0572-171">Remarks - width</span></span>

<span data-ttu-id="e0572-172">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e0572-172">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="e0572-173">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="e0572-173">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="e0572-174">モード。</span><span class="sxs-lookup"><span data-stu-id="e0572-174">Mode.</span></span>           | <span data-ttu-id="e0572-175">幅計算。</span><span class="sxs-lookup"><span data-stu-id="e0572-175">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0572-176">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="e0572-176">-1 Exact.</span></span>       | <span data-ttu-id="e0572-177">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="e0572-177">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="e0572-178">0 自動。</span><span class="sxs-lookup"><span data-stu-id="e0572-178">0 Auto.</span></span>         | <span data-ttu-id="e0572-179">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="e0572-179">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="e0572-180">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="e0572-180">1 Column width.</span></span> | <span data-ttu-id="e0572-181">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="e0572-181">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="e0572-182">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="e0572-182">The width and width calculation mode can be set separately.</span></span>

## <a name="method-extrasumwidth"></a><span data-ttu-id="e0572-183">メソッド extraSumWidth</span><span class="sxs-lookup"><span data-stu-id="e0572-183">Method extraSumWidth</span></span>

```xpp
public void extraSumWidth(Real value, Units unit)
```

### <a name="parameters---extrasumwidth"></a><span data-ttu-id="e0572-184">パラメーター - extraSumWidth</span><span class="sxs-lookup"><span data-stu-id="e0572-184">Parameters - extraSumWidth</span></span>

<span data-ttu-id="e0572-185">値</span><span class="sxs-lookup"><span data-stu-id="e0572-185">value</span></span>  

<!-- -->

<span data-ttu-id="e0572-186">単位</span><span class="sxs-lookup"><span data-stu-id="e0572-186">unit</span></span>  

## <a name="method-topmargin"></a><span data-ttu-id="e0572-187">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="e0572-187">Method topMargin</span></span>

```xpp
public void topMargin(Real value, Units unit)
```

### <a name="parameters---topmargin"></a><span data-ttu-id="e0572-188">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="e0572-188">Parameters - topMargin</span></span>

<span data-ttu-id="e0572-189">値</span><span class="sxs-lookup"><span data-stu-id="e0572-189">value</span></span>  

<!-- -->

<span data-ttu-id="e0572-190">単位</span><span class="sxs-lookup"><span data-stu-id="e0572-190">unit</span></span>  

## <a name="method-leftmargin"></a><span data-ttu-id="e0572-191">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="e0572-191">Method leftMargin</span></span>

```xpp
public void leftMargin(Real value, Units unit)
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="e0572-192">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="e0572-192">Parameters - leftMargin</span></span>

<span data-ttu-id="e0572-193">値</span><span class="sxs-lookup"><span data-stu-id="e0572-193">value</span></span>  

<!-- -->

<span data-ttu-id="e0572-194">単位</span><span class="sxs-lookup"><span data-stu-id="e0572-194">unit</span></span>  

## <a name="method-labelwidth"></a><span data-ttu-id="e0572-195">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="e0572-195">Method labelWidth</span></span>

```xpp
public void labelWidth(Real value, Units unit)
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="e0572-196">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="e0572-196">Parameters - labelWidth</span></span>

<span data-ttu-id="e0572-197">値</span><span class="sxs-lookup"><span data-stu-id="e0572-197">value</span></span>  

<!-- -->

<span data-ttu-id="e0572-198">単位</span><span class="sxs-lookup"><span data-stu-id="e0572-198">unit</span></span>  

## <a name="method-top"></a><span data-ttu-id="e0572-199">メソッド top</span><span class="sxs-lookup"><span data-stu-id="e0572-199">Method top</span></span>

```xpp
public void top(Real value, Units unit)
```

### <a name="parameters---top"></a><span data-ttu-id="e0572-200">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="e0572-200">Parameters - top</span></span>

<span data-ttu-id="e0572-201">値</span><span class="sxs-lookup"><span data-stu-id="e0572-201">value</span></span>  

<!-- -->

<span data-ttu-id="e0572-202">単位</span><span class="sxs-lookup"><span data-stu-id="e0572-202">unit</span></span>  

## <a name="method-bottommargin"></a><span data-ttu-id="e0572-203">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="e0572-203">Method bottomMargin</span></span>

```xpp
public void bottomMargin(Real value, Units unit)
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="e0572-204">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="e0572-204">Parameters - bottomMargin</span></span>

<span data-ttu-id="e0572-205">値</span><span class="sxs-lookup"><span data-stu-id="e0572-205">value</span></span>  

<!-- -->

<span data-ttu-id="e0572-206">単位</span><span class="sxs-lookup"><span data-stu-id="e0572-206">unit</span></span>  

