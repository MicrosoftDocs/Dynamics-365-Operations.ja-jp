---
title: ProjectGroupNode クラス
description: このトピックでは、ProjectGroupNode クラスについて説明します。
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
ms.openlocfilehash: 3edba6caab410d9687bbbea89ea59d0453539fc3
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502873"
---
# <a name="class-projectgroupnode"></a><span data-ttu-id="753ea-103">クラス ProjectGroupNode</span><span class="sxs-lookup"><span data-stu-id="753ea-103">Class ProjectGroupNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ProjectGroupNode extends TreeNode
```

<span data-ttu-id="753ea-104">ProjectGroupNode クラスは、プロジェクト内のグループ ノードを表します。</span><span class="sxs-lookup"><span data-stu-id="753ea-104">The ProjectGroupNode class represents a group node within a project.</span></span>

## <a name="remarks"></a><span data-ttu-id="753ea-105">備考</span><span class="sxs-lookup"><span data-stu-id="753ea-105">Remarks</span></span>

<span data-ttu-id="753ea-106">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="753ea-106">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="753ea-107">この API を呼び出す前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="753ea-107">Make sure that the user has access to the development security key (SysDevelopment) before you call this API.</span></span>

## <a name="examples"></a><span data-ttu-id="753ea-108">例</span><span class="sxs-lookup"><span data-stu-id="753ea-108">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="753ea-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="753ea-109">Methods</span></span>

| <span data-ttu-id="753ea-110">方法</span><span class="sxs-lookup"><span data-stu-id="753ea-110">Method</span></span>                                                                                       | <span data-ttu-id="753ea-111">説明</span><span class="sxs-lookup"><span data-stu-id="753ea-111">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="753ea-112">public TreeNode findGroupMember(str name, UtilElementType type, \[boolean searchSubgroups\])</span><span class="sxs-lookup"><span data-stu-id="753ea-112">public TreeNode findGroupMember(str name, UtilElementType type, \[boolean searchSubgroups\])</span></span> | <span data-ttu-id="753ea-113">特定の要素の projectGroup を検索します。</span><span class="sxs-lookup"><span data-stu-id="753ea-113">Searches the projectGroup for a specific element.</span></span> <span data-ttu-id="753ea-114">特定のグループまたはプロジェクト全体を検索するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="753ea-114">It can be used to search a specific group or the whole project.</span></span>                             |
| <span data-ttu-id="753ea-115">public str groupMask(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="753ea-115">public str groupMask(\[str value\])</span></span>                                                          |                                                                                                                                               |
| <span data-ttu-id="753ea-116">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="753ea-116">public str name(\[str value\])</span></span>                                                               | <span data-ttu-id="753ea-117">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="753ea-117">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="753ea-118">public boolean preventEditProperties(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="753ea-118">public boolean preventEditProperties(\[boolean value\])</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="753ea-119">public GroupNodeType projectGroupType(\[GroupNodeType value\])</span><span class="sxs-lookup"><span data-stu-id="753ea-119">public GroupNodeType projectGroupType(\[GroupNodeType value\])</span></span>                               |                                                                                                                                               |
| <span data-ttu-id="753ea-120">public void addUtilNode(UtilElementType type, str name)</span><span class="sxs-lookup"><span data-stu-id="753ea-120">public void addUtilNode(UtilElementType type, str name)</span></span>                                      | <span data-ttu-id="753ea-121">projectGroup にノードを追加します。</span><span class="sxs-lookup"><span data-stu-id="753ea-121">Adds a node to the projectGroup.</span></span>                                                                                                              |
| <span data-ttu-id="753ea-122">public void addNode(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="753ea-122">public void addNode(TreeNode node)</span></span>                                                           | <span data-ttu-id="753ea-123">ProjectGroup に既存のノードを追加します。</span><span class="sxs-lookup"><span data-stu-id="753ea-123">Adds an existing node to the projectGroup.</span></span>                                                                                                    |

## <a name="method-findgroupmember"></a><span data-ttu-id="753ea-124">メソッド findGroupMember</span><span class="sxs-lookup"><span data-stu-id="753ea-124">Method findGroupMember</span></span>

<span data-ttu-id="753ea-125">特定の要素の projectGroup を検索します。</span><span class="sxs-lookup"><span data-stu-id="753ea-125">Searches the projectGroup for a specific element.</span></span> <span data-ttu-id="753ea-126">特定のグループまたはプロジェクト全体を検索するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="753ea-126">It can be used to search a specific group or the whole project.</span></span>

```xpp
public TreeNode findGroupMember(str name, UtilElementType type, [boolean searchSubgroups])
```

### <a name="parameters---findgroupmember"></a><span data-ttu-id="753ea-127">パラメーター - findGroupMember</span><span class="sxs-lookup"><span data-stu-id="753ea-127">Parameters - findGroupMember</span></span>

<span data-ttu-id="753ea-128">名前</span><span class="sxs-lookup"><span data-stu-id="753ea-128">name</span></span>  
<span data-ttu-id="753ea-129">検索が再帰的 (サブプロジェクトを検索するか) どうかを決定するブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="753ea-129">A boolean flag that determines whether the search should be recursive (whether to search subprojects); optional.</span></span>

<!-- -->

<span data-ttu-id="753ea-130">タイプ</span><span class="sxs-lookup"><span data-stu-id="753ea-130">type</span></span>  
<span data-ttu-id="753ea-131">検索が再帰的 (サブプロジェクトを検索するか) どうかを決定するブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="753ea-131">A boolean flag that determines whether the search should be recursive (whether to search subprojects); optional.</span></span>

<!-- -->

<span data-ttu-id="753ea-132">searchSubgroups</span><span class="sxs-lookup"><span data-stu-id="753ea-132">searchSubgroups</span></span>  
<span data-ttu-id="753ea-133">検索が再帰的 (サブプロジェクトを検索するか) どうかを決定するブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="753ea-133">A boolean flag that determines whether the search should be recursive (whether to search subprojects); optional.</span></span>

### <a name="return-value---findgroupmember"></a><span data-ttu-id="753ea-134">戻り値 - findGroupMember</span><span class="sxs-lookup"><span data-stu-id="753ea-134">Return Value - findGroupMember</span></span>

<span data-ttu-id="753ea-135">オブジェクトが見つからない場合は、条件を満たす最初のオブジェクト、または nullNothingnullptrunita null 参照 (Visual Basic にはなし) を返します。</span><span class="sxs-lookup"><span data-stu-id="753ea-135">The first object that fits the criteria; returns nullNothingnullptrunita null reference (Nothing in Visual Basic) if no object is found.</span></span>

### <a name="remarks---findgroupmember"></a><span data-ttu-id="753ea-136">備考 - findGroupMember</span><span class="sxs-lookup"><span data-stu-id="753ea-136">Remarks - findGroupMember</span></span>

<span data-ttu-id="753ea-137">このメソッドは ProjectNode にもあります。</span><span class="sxs-lookup"><span data-stu-id="753ea-137">This method is also found on ProjectNode.</span></span>

## <a name="method-groupmask"></a><span data-ttu-id="753ea-138">メソッド groupMask</span><span class="sxs-lookup"><span data-stu-id="753ea-138">Method groupMask</span></span>

```xpp
public str groupMask([str value])
```

### <a name="parameters---groupmask"></a><span data-ttu-id="753ea-139">パラメーター - groupMask</span><span class="sxs-lookup"><span data-stu-id="753ea-139">Parameters - groupMask</span></span>

<span data-ttu-id="753ea-140">値</span><span class="sxs-lookup"><span data-stu-id="753ea-140">value</span></span>  

### <a name="return-value---groupmask"></a><span data-ttu-id="753ea-141">戻り値 - groupMask</span><span class="sxs-lookup"><span data-stu-id="753ea-141">Return Value - groupMask</span></span>

## <a name="method-name"></a><span data-ttu-id="753ea-142">メソッド名</span><span class="sxs-lookup"><span data-stu-id="753ea-142">Method name</span></span>

<span data-ttu-id="753ea-143">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="753ea-143">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="753ea-144">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="753ea-144">Parameters - name</span></span>

<span data-ttu-id="753ea-145">値</span><span class="sxs-lookup"><span data-stu-id="753ea-145">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="753ea-146">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="753ea-146">Return Value - name</span></span>

<span data-ttu-id="753ea-147">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="753ea-147">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="753ea-148">備考 - name</span><span class="sxs-lookup"><span data-stu-id="753ea-148">Remarks - name</span></span>

<span data-ttu-id="753ea-149">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="753ea-149">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="753ea-150">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="753ea-150">Begins with a letter.</span></span>
-   <span data-ttu-id="753ea-151">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="753ea-151">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="753ea-152">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="753ea-152">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="753ea-153">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="753ea-153">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="753ea-154">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="753ea-154">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-preventeditproperties"></a><span data-ttu-id="753ea-155">メソッド preventEditProperties</span><span class="sxs-lookup"><span data-stu-id="753ea-155">Method preventEditProperties</span></span>

```xpp
public boolean preventEditProperties([boolean value])
```

### <a name="parameters---preventeditproperties"></a><span data-ttu-id="753ea-156">パラメーター - preventEditProperties</span><span class="sxs-lookup"><span data-stu-id="753ea-156">Parameters - preventEditProperties</span></span>

<span data-ttu-id="753ea-157">値</span><span class="sxs-lookup"><span data-stu-id="753ea-157">value</span></span>  

### <a name="return-value---preventeditproperties"></a><span data-ttu-id="753ea-158">戻り値 - preventEditProperties</span><span class="sxs-lookup"><span data-stu-id="753ea-158">Return Value - preventEditProperties</span></span>

## <a name="method-projectgrouptype"></a><span data-ttu-id="753ea-159">メソッド projectGroupType</span><span class="sxs-lookup"><span data-stu-id="753ea-159">Method projectGroupType</span></span>

```xpp
public GroupNodeType projectGroupType([GroupNodeType value])
```

### <a name="parameters---projectgrouptype"></a><span data-ttu-id="753ea-160">パラメーター - projectGroupType</span><span class="sxs-lookup"><span data-stu-id="753ea-160">Parameters - projectGroupType</span></span>

<span data-ttu-id="753ea-161">値</span><span class="sxs-lookup"><span data-stu-id="753ea-161">value</span></span>  

### <a name="return-value---projectgrouptype"></a><span data-ttu-id="753ea-162">戻り値 - projectGroupType</span><span class="sxs-lookup"><span data-stu-id="753ea-162">Return Value - projectGroupType</span></span>

## <a name="method-addutilnode"></a><span data-ttu-id="753ea-163">メソッド addUtilNode</span><span class="sxs-lookup"><span data-stu-id="753ea-163">Method addUtilNode</span></span>

<span data-ttu-id="753ea-164">projectGroup にノードを追加します。</span><span class="sxs-lookup"><span data-stu-id="753ea-164">Adds a node to the projectGroup.</span></span>

```xpp
public void addUtilNode(UtilElementType type, str name)
```

### <a name="parameters---addutilnode"></a><span data-ttu-id="753ea-165">パラメーター - addUtilNode</span><span class="sxs-lookup"><span data-stu-id="753ea-165">Parameters - addUtilNode</span></span>

<span data-ttu-id="753ea-166">タイプ</span><span class="sxs-lookup"><span data-stu-id="753ea-166">type</span></span>  
<span data-ttu-id="753ea-167">ノードの名前。</span><span class="sxs-lookup"><span data-stu-id="753ea-167">The name of the node.</span></span>

<!-- -->

<span data-ttu-id="753ea-168">名前</span><span class="sxs-lookup"><span data-stu-id="753ea-168">name</span></span>  
<span data-ttu-id="753ea-169">ノードの名前。</span><span class="sxs-lookup"><span data-stu-id="753ea-169">The name of the node.</span></span>

### <a name="remarks---addutilnode"></a><span data-ttu-id="753ea-170">備考 - addUtilNode</span><span class="sxs-lookup"><span data-stu-id="753ea-170">Remarks - addUtilNode</span></span>

<span data-ttu-id="753ea-171">このメソッドは、ProjectNode クラスにもあります。</span><span class="sxs-lookup"><span data-stu-id="753ea-171">This method also is found on the ProjectNode class.</span></span>

## <a name="method-addnode"></a><span data-ttu-id="753ea-172">メソッド addNode</span><span class="sxs-lookup"><span data-stu-id="753ea-172">Method addNode</span></span>

<span data-ttu-id="753ea-173">ProjectGroup に既存のノードを追加します。</span><span class="sxs-lookup"><span data-stu-id="753ea-173">Adds an existing node to the projectGroup.</span></span>

```xpp
public void addNode(TreeNode node)
```

### <a name="parameters---addnode"></a><span data-ttu-id="753ea-174">パラメーター - addNode</span><span class="sxs-lookup"><span data-stu-id="753ea-174">Parameters - addNode</span></span>

<span data-ttu-id="753ea-175">node</span><span class="sxs-lookup"><span data-stu-id="753ea-175">node</span></span>  
<span data-ttu-id="753ea-176">追加するノード。</span><span class="sxs-lookup"><span data-stu-id="753ea-176">The node to add.</span></span>

