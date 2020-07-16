---
title: FileIOPermission クラス
description: このトピックでは、FileIOPermission クラスについて説明します。
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
ms.openlocfilehash: 4fea939d775183fc3948bbe4cbc9ef4487006f17
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502979"
---
# <a name="class-fileiopermission"></a><span data-ttu-id="ee4b2-103">クラス FileIOPermission</span><span class="sxs-lookup"><span data-stu-id="ee4b2-103">Class FileIOPermission</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FileIOPermission extends CodeAccessPermission
```

<span data-ttu-id="ee4b2-104">FileIOPermission クラスは、ファイルおよびフォルダーへのアクセス機能を制御します。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-104">The FileIOPermission class controls the ability to access files and folders.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee4b2-105">備考</span><span class="sxs-lookup"><span data-stu-id="ee4b2-105">Remarks</span></span>

<span data-ttu-id="ee4b2-106">FileIoPermission クラスは、特定の API のアクセス許可をチェックするように設計されています。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-106">The FileIoPermission class is designed to check permissions for specific APIs.</span></span> <span data-ttu-id="ee4b2-107">アクセス許可によって保護されているすべての API のリストについては、「セキュリティで保護された API」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-107">For a list of all APIs that are protected by permissions, see Secured APIs.</span></span> <span data-ttu-id="ee4b2-108">保護された API を実行する前に、対応する CodeAccessPermission:: demand メソッドが呼び出されている同じ層 (通常はサーバー層) で assert メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-108">Before the protected API is run, you must call the assert method on the same tier, usually the server tier, that the corresponding CodeAccessPermission::demand method is called on.</span></span> <span data-ttu-id="ee4b2-109">次のいずれかでサーバー層のメソッドを呼び出します:</span><span class="sxs-lookup"><span data-stu-id="ee4b2-109">Call a method on the server tier from one of the following:</span></span>

-   <span data-ttu-id="ee4b2-110">サーバー静的メソッド</span><span class="sxs-lookup"><span data-stu-id="ee4b2-110">A server static method</span></span>
-   <span data-ttu-id="ee4b2-111">RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド</span><span class="sxs-lookup"><span data-stu-id="ee4b2-111">A class instance method that is set to run on the server by using the RunOn class property</span></span>

## <a name="examples"></a><span data-ttu-id="ee4b2-112">例</span><span class="sxs-lookup"><span data-stu-id="ee4b2-112">Examples</span></span>

<span data-ttu-id="ee4b2-113">次のコード例は、File.txt ファイルの読み取りアクセス許可を指定する FileIoPermission クラスの新しいインスタンスを示しています。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-113">The following code example shows a new instance of the FileIoPermission class that specifies read access for the File.txt file.</span></span> <span data-ttu-id="ee4b2-114">assert メソッドが呼び出され、コードが AsciiIo.new メソッドを呼び出すことができることが宣言されます。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-114">The assert method is called to declare that the code can then call the AsciiIo.new method.</span></span>

```xpp
server static void main(Args args) 
{ 
    FileIoPermission _perm; 
    AsciiIo a; 
    _perm = new FileIoPermission("c:\\File.txt",'r'); 
    _perm.assert(); 
    // Invoke the protected API. 
    a = new AsciiIo("c:\\File.txt",'r'); 
}
```

## <a name="methods"></a><span data-ttu-id="ee4b2-115">メソッド</span><span class="sxs-lookup"><span data-stu-id="ee4b2-115">Methods</span></span>

| <span data-ttu-id="ee4b2-116">方法</span><span class="sxs-lookup"><span data-stu-id="ee4b2-116">Method</span></span>                                                 | <span data-ttu-id="ee4b2-117">説明</span><span class="sxs-lookup"><span data-stu-id="ee4b2-117">Description</span></span>                                                                      |
|--------------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ee4b2-118">public CodeAccessPermission copy()</span><span class="sxs-lookup"><span data-stu-id="ee4b2-118">public CodeAccessPermission copy()</span></span>                     | <span data-ttu-id="ee4b2-119">現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-119">Creates and returns a copy of the current permission class object.</span></span>               |
| <span data-ttu-id="ee4b2-120">public boolean isSubsetOf(CodeAccessPermission target)</span><span class="sxs-lookup"><span data-stu-id="ee4b2-120">public boolean isSubsetOf(CodeAccessPermission target)</span></span> | <span data-ttu-id="ee4b2-121">現在のアクセス許可が指定されたアクセス許可のサブセットかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-121">Determines whether the current permission is a subset of a specified permission.</span></span> |
| <span data-ttu-id="ee4b2-122">public void new(str filename, str mode)</span><span class="sxs-lookup"><span data-stu-id="ee4b2-122">public void new(str filename, str mode)</span></span>                | <span data-ttu-id="ee4b2-123">CodeAccessPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-123">Initializes a new instance of the CodeAccessPermission class.</span></span>                    |

## <a name="method-copy"></a><span data-ttu-id="ee4b2-124">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="ee4b2-124">Method copy</span></span>

<span data-ttu-id="ee4b2-125">現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-125">Creates and returns a copy of the current permission class object.</span></span>

```xpp
public CodeAccessPermission copy()
```

### <a name="return-value---copy"></a><span data-ttu-id="ee4b2-126">戻り値 - copy</span><span class="sxs-lookup"><span data-stu-id="ee4b2-126">Return Value - copy</span></span>

<span data-ttu-id="ee4b2-127">現在のアクセス許可オブジェクトのコピーです。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-127">A copy of the current permission object.</span></span>

### <a name="remarks---copy"></a><span data-ttu-id="ee4b2-128">備考 - copy</span><span class="sxs-lookup"><span data-stu-id="ee4b2-128">Remarks - copy</span></span>

<span data-ttu-id="ee4b2-129">CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-129">You override this method when you derive a class from the CodeAccessPermission class.</span></span> <span data-ttu-id="ee4b2-130">詳細については、「コピー」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-130">For more information, see copy.</span></span>

## <a name="method-issubsetof"></a><span data-ttu-id="ee4b2-131">メソッド isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="ee4b2-131">Method isSubsetOf</span></span>

<span data-ttu-id="ee4b2-132">現在のアクセス許可が指定されたアクセス許可のサブセットかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-132">Determines whether the current permission is a subset of a specified permission.</span></span>

```xpp
public boolean isSubsetOf(CodeAccessPermission target)
```

### <a name="parameters---issubsetof"></a><span data-ttu-id="ee4b2-133">パラメーター - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="ee4b2-133">Parameters - isSubsetOf</span></span>

<span data-ttu-id="ee4b2-134">target</span><span class="sxs-lookup"><span data-stu-id="ee4b2-134">target</span></span>  
<span data-ttu-id="ee4b2-135">CodeAccessPermission クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-135">A CodeAccessPermission class object.</span></span>

### <a name="return-value---issubsetof"></a><span data-ttu-id="ee4b2-136">戻り値 - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="ee4b2-136">Return Value - isSubsetOf</span></span>

<span data-ttu-id="ee4b2-137">現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-137">true if the current permission is a subset of the specified permission; otherwise, false.</span></span>

### <a name="remarks---issubsetof"></a><span data-ttu-id="ee4b2-138">備考 - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="ee4b2-138">Remarks - isSubsetOf</span></span>

<span data-ttu-id="ee4b2-139">CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-139">You override this method when you derive a class from the CodeAccessPermission class.</span></span> <span data-ttu-id="ee4b2-140">詳細については、「M: CodeAccessPermission.isSubsetOf」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-140">For more information, see M: CodeAccessPermission.isSubsetOf.</span></span>

## <a name="method-new"></a><span data-ttu-id="ee4b2-141">メソッド new</span><span class="sxs-lookup"><span data-stu-id="ee4b2-141">Method new</span></span>

<span data-ttu-id="ee4b2-142">CodeAccessPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-142">Initializes a new instance of the CodeAccessPermission class.</span></span>

```xpp
public void new(str filename, str mode)
```

### <a name="parameters---new"></a><span data-ttu-id="ee4b2-143">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="ee4b2-143">Parameters - new</span></span>

<span data-ttu-id="ee4b2-144">filename</span><span class="sxs-lookup"><span data-stu-id="ee4b2-144">filename</span></span>  
<span data-ttu-id="ee4b2-145">アクセスのタイプを指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-145">A String data type that specifies the type of access.</span></span>

<!-- -->

<span data-ttu-id="ee4b2-146">モード</span><span class="sxs-lookup"><span data-stu-id="ee4b2-146">mode</span></span>  
<span data-ttu-id="ee4b2-147">アクセスのタイプを指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-147">A String data type that specifies the type of access.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="ee4b2-148">備考 - new</span><span class="sxs-lookup"><span data-stu-id="ee4b2-148">Remarks - new</span></span>

<span data-ttu-id="ee4b2-149">次のテーブルに、\_mode パラメーターの使用可能な値を示します。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-149">The following table lists the possible values for the \_mode parameter.</span></span>

|     |                |
|-----|----------------|
| <span data-ttu-id="ee4b2-150">R</span><span class="sxs-lookup"><span data-stu-id="ee4b2-150">R</span></span>   | <span data-ttu-id="ee4b2-151">既読</span><span class="sxs-lookup"><span data-stu-id="ee4b2-151">Read</span></span>           |
| <span data-ttu-id="ee4b2-152">W</span><span class="sxs-lookup"><span data-stu-id="ee4b2-152">W</span></span>   | <span data-ttu-id="ee4b2-153">書き込み</span><span class="sxs-lookup"><span data-stu-id="ee4b2-153">Write</span></span>          |
| <span data-ttu-id="ee4b2-154">RW</span><span class="sxs-lookup"><span data-stu-id="ee4b2-154">RW</span></span>  | <span data-ttu-id="ee4b2-155">読み取りと書き込み</span><span class="sxs-lookup"><span data-stu-id="ee4b2-155">Read and write</span></span> |

### <a name="examples---new"></a><span data-ttu-id="ee4b2-156">例 - new</span><span class="sxs-lookup"><span data-stu-id="ee4b2-156">Examples - new</span></span>

<span data-ttu-id="ee4b2-157">次のコード例は、File.txt ファイルの読み取りアクセス許可を指定する FileIoPermission クラスの新しいインスタンスを示しています。</span><span class="sxs-lookup"><span data-stu-id="ee4b2-157">The following code example shows a new instance of the FileIoPermission class that specifies read access for the File.txt file.</span></span>

```xpp
server static void main(Args args) 
{ 
    FileIoPermission _perm; 
    _perm = new FileIoPermission("c:\\File.txt",'r'); 
}
```

