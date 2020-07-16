---
title: MemberFunction クラス
description: このトピックでは、MemberFunction クラスについて説明します。
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
ms.openlocfilehash: 0c838cd651a9bf80f4d2e8a9019ba132e986e078
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502574"
---
# <a name="class-memberfunction"></a><span data-ttu-id="c623b-103">クラス MemberFunction</span><span class="sxs-lookup"><span data-stu-id="c623b-103">Class MemberFunction</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class MemberFunction extends TreeNode
```

<span data-ttu-id="c623b-104">MemberFunction クラスは、フォーム、レポート、クラスなどのアプリケーション オブジェクト ツリー (AOT) で指定されたノードに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="c623b-104">The MemberFunction class provides information about a specified node in the Application Object Tree (AOT), such as a form, report, or class.</span></span>

## <a name="remarks"></a><span data-ttu-id="c623b-105">備考</span><span class="sxs-lookup"><span data-stu-id="c623b-105">Remarks</span></span>

<span data-ttu-id="c623b-106">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="c623b-106">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="c623b-107">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c623b-107">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span> <span data-ttu-id="c623b-108">::findNode メソッドを使用すると MemberFunction クラスのインスタンスにノードを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="c623b-108">You can use the ::findNode method to assign a node to an instance of the MemberFunction class.</span></span>

## <a name="examples"></a><span data-ttu-id="c623b-109">例</span><span class="sxs-lookup"><span data-stu-id="c623b-109">Examples</span></span>

<span data-ttu-id="c623b-110">次の例では、TreeNode::findNode メソッドを使用して、AddressSelectForm.callerDataSource メソッドのノードを MemberFunction クラスのインスタンスに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c623b-110">The following example uses the TreeNode::findNode method to assign the node for the AddressSelectForm.callerDataSource method to an instance of the MemberFunction class.</span></span> <span data-ttu-id="c623b-111">MemberFunction.AOTgetSource メソッドは、メソッドのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="c623b-111">The MemberFunction.AOTgetSource Method method returns the method source code.</span></span>

```xpp
void getMemberFunction() 
{ 
    MemberFunction memberFunction; 
    str name; 
    boolean isStatic; 
    str source; 
    try 
    { 
        memberFunction = TreeNode::findNode( 
           '\\Classes\\AddressSelectForm\\callerDataSource'); 
        if(!memberFunction) 
        { 
            throw exception::Error; 
        } 
        source = memberFunction.AOTgetSource(); 
        print source; 
        pause; 
    } 
    catch (exception::Error) 
    { 
        print "The specified node does not exist."; 
        pause; 
        } 
    } 
}
```

## <a name="methods"></a><span data-ttu-id="c623b-112">メソッド</span><span class="sxs-lookup"><span data-stu-id="c623b-112">Methods</span></span>

| <span data-ttu-id="c623b-113">方法</span><span class="sxs-lookup"><span data-stu-id="c623b-113">Method</span></span>                                                     | <span data-ttu-id="c623b-114">説明</span><span class="sxs-lookup"><span data-stu-id="c623b-114">Description</span></span>                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c623b-115">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="c623b-115">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="c623b-116">クラスやメソッドなど、AOT 内で指定したノードのソース コードを提供します。</span><span class="sxs-lookup"><span data-stu-id="c623b-116">Provides the source code for a specified node in the AOT, such as a class or method.</span></span>                                                    |
| <span data-ttu-id="c623b-117">public boolean canAddEventHandler()</span><span class="sxs-lookup"><span data-stu-id="c623b-117">public boolean canAddEventHandler()</span></span>                        |                                                                                                                                         |
| <span data-ttu-id="c623b-118">public boolean isEvent()</span><span class="sxs-lookup"><span data-stu-id="c623b-118">public boolean isEvent()</span></span>                                   |                                                                                                                                         |
| <span data-ttu-id="c623b-119">public boolean isStatic()</span><span class="sxs-lookup"><span data-stu-id="c623b-119">public boolean isStatic()</span></span>                                  | <span data-ttu-id="c623b-120">メソッドが静的かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="c623b-120">Indicates whether a method is static.</span></span>                                                                                                   |
| <span data-ttu-id="c623b-121">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c623b-121">public str name(\[str value\])</span></span>                             | <span data-ttu-id="c623b-122">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c623b-122">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="c623b-123">public void AOTedit(\[int Line\], \[int Column\])</span><span class="sxs-lookup"><span data-stu-id="c623b-123">public void AOTedit(\[int Line\], \[int Column\])</span></span>          | <span data-ttu-id="c623b-124">AOT で指定したノードの適切なエディタを開きます。</span><span class="sxs-lookup"><span data-stu-id="c623b-124">Opens the appropriate editor for a specified node in the AOT.</span></span>                                                                           |
| <span data-ttu-id="c623b-125">public void new()</span><span class="sxs-lookup"><span data-stu-id="c623b-125">public void new()</span></span>                                          | <span data-ttu-id="c623b-126">MemberFunction クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c623b-126">Initializes a new instance of the MemberFunction class.</span></span>                                                                                 |
| <span data-ttu-id="c623b-127">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="c623b-127">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="c623b-128">クラスやメソッドなど、AOT 内で指定したノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="c623b-128">Sets the source code for a specified node in the AOT, such as a class or method.</span></span>                                                        |

## <a name="method-aotgetsource"></a><span data-ttu-id="c623b-129">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="c623b-129">Method AOTgetSource</span></span>

<span data-ttu-id="c623b-130">クラスやメソッドなど、AOT 内で指定したノードのソース コードを提供します。</span><span class="sxs-lookup"><span data-stu-id="c623b-130">Provides the source code for a specified node in the AOT, such as a class or method.</span></span>

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a><span data-ttu-id="c623b-131">戻り値 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="c623b-131">Return Value - AOTgetSource</span></span>

<span data-ttu-id="c623b-132">ソース コードの文字列値、ノードにソース コードが含まれていない場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="c623b-132">A string value for the source code; nullNothingnullptrunita null reference (Nothing in Visual Basic) if the node does not contain source code.</span></span>

## <a name="method-canaddeventhandler"></a><span data-ttu-id="c623b-133">メソッド canAddEventHandler</span><span class="sxs-lookup"><span data-stu-id="c623b-133">Method canAddEventHandler</span></span>

```xpp
public boolean canAddEventHandler()
```

### <a name="return-value---canaddeventhandler"></a><span data-ttu-id="c623b-134">戻り値 - canAddEventHandler</span><span class="sxs-lookup"><span data-stu-id="c623b-134">Return Value - canAddEventHandler</span></span>

## <a name="method-isevent"></a><span data-ttu-id="c623b-135">メソッド isEvent</span><span class="sxs-lookup"><span data-stu-id="c623b-135">Method isEvent</span></span>

```xpp
public boolean isEvent()
```

### <a name="return-value---isevent"></a><span data-ttu-id="c623b-136">戻り値 - isEvent</span><span class="sxs-lookup"><span data-stu-id="c623b-136">Return Value - isEvent</span></span>

## <a name="method-isstatic"></a><span data-ttu-id="c623b-137">メソッド isStatic</span><span class="sxs-lookup"><span data-stu-id="c623b-137">Method isStatic</span></span>

<span data-ttu-id="c623b-138">メソッドが静的かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="c623b-138">Indicates whether a method is static.</span></span>

```xpp
public boolean isStatic()
```

### <a name="return-value---isstatic"></a><span data-ttu-id="c623b-139">戻り値 - isStatic</span><span class="sxs-lookup"><span data-stu-id="c623b-139">Return Value - isStatic</span></span>

<span data-ttu-id="c623b-140">メソッドが静的である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="c623b-140">true if the method is static; otherwise, false.</span></span>

### <a name="remarks---isstatic"></a><span data-ttu-id="c623b-141">備考 - isStatic</span><span class="sxs-lookup"><span data-stu-id="c623b-141">Remarks - isStatic</span></span>

<span data-ttu-id="c623b-142">このメソッドは、AOT の指定されたノード (フォーム、レポート、クラスなど) に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="c623b-142">This method is associated with a specified node in the AOT, such as a form, report, or class.</span></span> <span data-ttu-id="c623b-143">このメソッドは、主に MemberFunction::AOTsetSource メソッドと組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="c623b-143">This method is used primarily in conjunction with the MemberFunction::AOTsetSource method.</span></span>

## <a name="method-name"></a><span data-ttu-id="c623b-144">メソッド名</span><span class="sxs-lookup"><span data-stu-id="c623b-144">Method name</span></span>

<span data-ttu-id="c623b-145">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c623b-145">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="c623b-146">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="c623b-146">Parameters - name</span></span>

<span data-ttu-id="c623b-147">値</span><span class="sxs-lookup"><span data-stu-id="c623b-147">value</span></span>  
<span data-ttu-id="c623b-148">ノードを指定する文字列、オプション。</span><span class="sxs-lookup"><span data-stu-id="c623b-148">A string that specifies a node; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="c623b-149">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="c623b-149">Return Value - name</span></span>

<span data-ttu-id="c623b-150">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="c623b-150">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="c623b-151">備考 - name</span><span class="sxs-lookup"><span data-stu-id="c623b-151">Remarks - name</span></span>

<span data-ttu-id="c623b-152">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c623b-152">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="c623b-153">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="c623b-153">It starts with a letter.</span></span>
-   <span data-ttu-id="c623b-154">250 文字を超えていません。</span><span class="sxs-lookup"><span data-stu-id="c623b-154">It doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="c623b-155">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="c623b-155">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="c623b-156">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="c623b-156">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="c623b-157">テーブルは、拡張データ型、基本列挙型、およびクラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="c623b-157">Tables cannot have the same name as other public objects, such as extended data types, base enums, and classes.</span></span>

## <a name="method-aotedit"></a><span data-ttu-id="c623b-158">メソッド AOTedit</span><span class="sxs-lookup"><span data-stu-id="c623b-158">Method AOTedit</span></span>

<span data-ttu-id="c623b-159">AOT で指定したノードの適切なエディタを開きます。</span><span class="sxs-lookup"><span data-stu-id="c623b-159">Opens the appropriate editor for a specified node in the AOT.</span></span>

```xpp
public void AOTedit([int Line], [int Column])
```

### <a name="parameters---aotedit"></a><span data-ttu-id="c623b-160">パラメーター - AOTedit</span><span class="sxs-lookup"><span data-stu-id="c623b-160">Parameters - AOTedit</span></span>

<span data-ttu-id="c623b-161">折れ線</span><span class="sxs-lookup"><span data-stu-id="c623b-161">Line</span></span>  
<span data-ttu-id="c623b-162">カーソルの列の位置を指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="c623b-162">An integer that specifies the column position for the cursor; optional.</span></span>

<!-- -->

<span data-ttu-id="c623b-163">円柱</span><span class="sxs-lookup"><span data-stu-id="c623b-163">Column</span></span>  
<span data-ttu-id="c623b-164">カーソルの列の位置を指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="c623b-164">An integer that specifies the column position for the cursor; optional.</span></span>

## <a name="method-new"></a><span data-ttu-id="c623b-165">メソッド new</span><span class="sxs-lookup"><span data-stu-id="c623b-165">Method new</span></span>

<span data-ttu-id="c623b-166">MemberFunction クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c623b-166">Initializes a new instance of the MemberFunction class.</span></span>

```xpp
public void new()
```

## <a name="method-aotsetsource"></a><span data-ttu-id="c623b-167">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="c623b-167">Method AOTsetSource</span></span>

<span data-ttu-id="c623b-168">クラスやメソッドなど、AOT 内で指定したノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="c623b-168">Sets the source code for a specified node in the AOT, such as a class or method.</span></span>

```xpp
public void AOTsetSource(str source, [boolean isStatic])
```

### <a name="parameters---aotsetsource"></a><span data-ttu-id="c623b-169">パラメーター - AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="c623b-169">Parameters - AOTsetSource</span></span>

<span data-ttu-id="c623b-170">ソース</span><span class="sxs-lookup"><span data-stu-id="c623b-170">source</span></span>  
<span data-ttu-id="c623b-171">ブール値: 静的メソッドの場合は true、インスタンス メソッドの場合は false; オプション。</span><span class="sxs-lookup"><span data-stu-id="c623b-171">A Boolean value: true for a static method or false for an instance method; optional.</span></span>

<!-- -->

<span data-ttu-id="c623b-172">isStatic</span><span class="sxs-lookup"><span data-stu-id="c623b-172">isStatic</span></span>  
<span data-ttu-id="c623b-173">ブール値: 静的メソッドの場合は true、インスタンス メソッドの場合は false; オプション。</span><span class="sxs-lookup"><span data-stu-id="c623b-173">A Boolean value: true for a static method or false for an instance method; optional.</span></span>

