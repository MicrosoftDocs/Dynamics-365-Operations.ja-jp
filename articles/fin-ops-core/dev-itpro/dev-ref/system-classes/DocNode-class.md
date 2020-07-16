---
title: DocNode クラス
description: このトピックでは、DocNode クラスについて説明します。
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
ms.openlocfilehash: a663a384aab5c07a24dbfa66b70a2c80e47f1e66
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502672"
---
# <a name="class-docnode"></a><span data-ttu-id="9a8a3-103">クラス DocNode</span><span class="sxs-lookup"><span data-stu-id="9a8a3-103">Class DocNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DocNode extends TreeNode
```

<span data-ttu-id="9a8a3-104">DocNode クラスは、ドキュメント ノードの情報や機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-104">The DocNode class provides the information and functions for a documentation node.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a8a3-105">備考</span><span class="sxs-lookup"><span data-stu-id="9a8a3-105">Remarks</span></span>

<span data-ttu-id="9a8a3-106">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-106">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="9a8a3-107">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-107">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="9a8a3-108">例</span><span class="sxs-lookup"><span data-stu-id="9a8a3-108">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="9a8a3-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="9a8a3-109">Methods</span></span>

| <span data-ttu-id="9a8a3-110">方法</span><span class="sxs-lookup"><span data-stu-id="9a8a3-110">Method</span></span>                                                                                                                                                                                            | <span data-ttu-id="9a8a3-111">説明</span><span class="sxs-lookup"><span data-stu-id="9a8a3-111">Description</span></span>                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a8a3-112">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="9a8a3-112">public str AOTgetSource()</span></span>                                                                                                                                                                         | <span data-ttu-id="9a8a3-113">ノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-113">Returns the source code for the node.</span></span>                                                                                                   |
| <span data-ttu-id="9a8a3-114">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9a8a3-114">public str changedBy(\[str value\])</span></span>                                                                                                                                                               | <span data-ttu-id="9a8a3-115">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-115">Gets or sets the name of the user who last changed the application object.</span></span>                                                              |
| <span data-ttu-id="9a8a3-116">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="9a8a3-116">public Date changedDate(\[Date value\])</span></span>                                                                                                                                                           | <span data-ttu-id="9a8a3-117">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-117">Gets or sets the date that an application object was last changed.</span></span>                                                                      |
| <span data-ttu-id="9a8a3-118">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9a8a3-118">public str changedTime(\[str value\])</span></span>                                                                                                                                                             | <span data-ttu-id="9a8a3-119">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-119">Gets or sets the time that an application object was last changed.</span></span>                                                                      |
| <span data-ttu-id="9a8a3-120">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="9a8a3-120">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                                                                                                          | <span data-ttu-id="9a8a3-121">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-121">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="9a8a3-122">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9a8a3-122">public str createdBy(\[str value\])</span></span>                                                                                                                                                               | <span data-ttu-id="9a8a3-123">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-123">Gets or sets the name of the user who created the application object.</span></span>                                                                   |
| <span data-ttu-id="9a8a3-124">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="9a8a3-124">public Date creationDate(\[Date value\])</span></span>                                                                                                                                                          | <span data-ttu-id="9a8a3-125">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-125">Gets or sets the date that an application object was created.</span></span>                                                                           |
| <span data-ttu-id="9a8a3-126">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9a8a3-126">public str creationTime(\[str value\])</span></span>                                                                                                                                                            |                                                                                                                                         |
| <span data-ttu-id="9a8a3-127">public str description(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9a8a3-127">public str description(\[str value\])</span></span>                                                                                                                                                             | <span data-ttu-id="9a8a3-128">ドキュメント ノードの説明を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-128">Sets or returns the description of the documentation node.</span></span>                                                                              |
| <span data-ttu-id="9a8a3-129">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9a8a3-129">public str name(\[str value\])</span></span>                                                                                                                                                                    | <span data-ttu-id="9a8a3-130">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-130">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="9a8a3-131">public int neededAccessLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="9a8a3-131">public int neededAccessLevel(\[int value\])</span></span>                                                                                                                                                       | <span data-ttu-id="9a8a3-132">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-132">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>                                                                 |
| <span data-ttu-id="9a8a3-133">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="9a8a3-133">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                                                                                                         | <span data-ttu-id="9a8a3-134">ドキュメント ノードのセキュリティ キーを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-134">Sets or returns the security key for the documentation node.</span></span>                                                                            |
| <span data-ttu-id="9a8a3-135">public str title(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9a8a3-135">public str title(\[str value\])</span></span>                                                                                                                                                                   | <span data-ttu-id="9a8a3-136">ドキュメント ノードのタイトルを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-136">Sets or returns the title of the documentation node.</span></span>                                                                                    |
| <span data-ttu-id="9a8a3-137">::public static DocNode findAOTElementDocNode(ApplCodeDocType HelpType, str Name, \[str ParentName\], \[int Mode\])</span><span class="sxs-lookup"><span data-stu-id="9a8a3-137">::public static DocNode findAOTElementDocNode(ApplCodeDocType HelpType, str Name, \[str ParentName\], \[int Mode\])</span></span>                                                                               | <span data-ttu-id="9a8a3-138">アプリケーション オブジェクト ツリー (AOT) で要素ドキュメント ノードの検索を実行します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-138">Performs a search for an element documentation node in the Application Object Tree (AOT).</span></span>                         |
| <span data-ttu-id="9a8a3-139">::public static DocNode findApplicationDocNode(ApplHelpType HelpType, str Name, \[str ParentName\], \[int Mode\])</span><span class="sxs-lookup"><span data-stu-id="9a8a3-139">::public static DocNode findApplicationDocNode(ApplHelpType HelpType, str Name, \[str ParentName\], \[int Mode\])</span></span>                                                                                 | <span data-ttu-id="9a8a3-140">アプリケーション要素ドキュメント ノードの検索を実行します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-140">Performs a search for an application element documentation node.</span></span>                                                                        |
| <span data-ttu-id="9a8a3-141">::public static DocNode findKernelDocNode(KernelHelpType HelpType, str Name, \[str ParentName\], \[int Mode\])</span><span class="sxs-lookup"><span data-stu-id="9a8a3-141">::public static DocNode findKernelDocNode(KernelHelpType HelpType, str Name, \[str ParentName\], \[int Mode\])</span></span>                                                                                    | <span data-ttu-id="9a8a3-142">カーネル要素ドキュメント ノードの検索を実行します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-142">Performs a search for a kernel element documentation node.</span></span>                                                                              |
| <span data-ttu-id="9a8a3-143">::public static DocNode getNodeDetached(UtilFileType helpType, int UtilType, str Name, \[int ParentId\], \[int Type\], \[UtilEntryLevel Utillevel\], \[boolean Forcelevel\], \[boolean OldUtil\])</span><span class="sxs-lookup"><span data-stu-id="9a8a3-143">::public static DocNode getNodeDetached(UtilFileType helpType, int UtilType, str Name, \[int ParentId\], \[int Type\], \[UtilEntryLevel Utillevel\], \[boolean Forcelevel\], \[boolean OldUtil\])</span></span> | <span data-ttu-id="9a8a3-144">指定したドキュメントのノードを返します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-144">Returns the specified documentation node.</span></span>                                                                                               |
| <span data-ttu-id="9a8a3-145">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="9a8a3-145">public void AOTsetSource(str source, \[boolean isStatic\])</span></span>                                                                                                                                        | <span data-ttu-id="9a8a3-146">ノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-146">Sets the source code for the node.</span></span>                                                                                                      |
| <span data-ttu-id="9a8a3-147">public void AOTedit(\[int Line\], \[int Column\])</span><span class="sxs-lookup"><span data-stu-id="9a8a3-147">public void AOTedit(\[int Line\], \[int Column\])</span></span>                                                                                                                                                 | <span data-ttu-id="9a8a3-148">このノードの適切なエディタを開きます。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-148">Opens the appropriate editor for this node.</span></span>                                                                                             |

## <a name="method-aotgetsource"></a><span data-ttu-id="9a8a3-149">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="9a8a3-149">Method AOTgetSource</span></span>

<span data-ttu-id="9a8a3-150">ノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-150">Returns the source code for the node.</span></span>

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a><span data-ttu-id="9a8a3-151">戻り値 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="9a8a3-151">Return Value - AOTgetSource</span></span>

<span data-ttu-id="9a8a3-152">文字列としてのノードのソースコード。ノードのソース コードがない場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-152">The source code for the node as a string; null, Nothing, nullptr, unit, a null reference (Nothing in Visual Basic) if there is no source code for the node.</span></span>

## <a name="method-changedby"></a><span data-ttu-id="9a8a3-153">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="9a8a3-153">Method changedBy</span></span>

<span data-ttu-id="9a8a3-154">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-154">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="9a8a3-155">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="9a8a3-155">Parameters - changedBy</span></span>

<span data-ttu-id="9a8a3-156">値</span><span class="sxs-lookup"><span data-stu-id="9a8a3-156">value</span></span>  
<span data-ttu-id="9a8a3-157">ドキュメント ノードを変更したユーザーとして割り当てられている値。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-157">The value that is being assigned as the user who changed the documentation node.</span></span>

### <a name="return-value---changedby"></a><span data-ttu-id="9a8a3-158">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="9a8a3-158">Return Value - changedBy</span></span>

<span data-ttu-id="9a8a3-159">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-159">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="9a8a3-160">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="9a8a3-160">Method changedDate</span></span>

<span data-ttu-id="9a8a3-161">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-161">Gets or sets the date that an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="9a8a3-162">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="9a8a3-162">Parameters - changedDate</span></span>

<span data-ttu-id="9a8a3-163">値</span><span class="sxs-lookup"><span data-stu-id="9a8a3-163">value</span></span>  
<span data-ttu-id="9a8a3-164">ドキュメント ノードの変更日として割り当てられている値。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-164">The value that is being assigned as the change date for the documentation node.</span></span>

### <a name="return-value---changeddate"></a><span data-ttu-id="9a8a3-165">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="9a8a3-165">Return Value - changedDate</span></span>

<span data-ttu-id="9a8a3-166">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-166">The date that an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="9a8a3-167">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="9a8a3-167">Method changedTime</span></span>

<span data-ttu-id="9a8a3-168">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-168">Gets or sets the time that an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="9a8a3-169">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="9a8a3-169">Parameters - changedTime</span></span>

<span data-ttu-id="9a8a3-170">値</span><span class="sxs-lookup"><span data-stu-id="9a8a3-170">value</span></span>  
<span data-ttu-id="9a8a3-171">ドキュメント ノードの変更時刻として割り当てられている値。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-171">The value that is being assigned as the change time for the documentation node.</span></span>

### <a name="return-value---changedtime"></a><span data-ttu-id="9a8a3-172">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="9a8a3-172">Return Value - changedTime</span></span>

<span data-ttu-id="9a8a3-173">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-173">The time that an application object was last changed.</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="9a8a3-174">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="9a8a3-174">Method configurationKey</span></span>

<span data-ttu-id="9a8a3-175">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-175">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="9a8a3-176">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="9a8a3-176">Parameters - configurationKey</span></span>

<span data-ttu-id="9a8a3-177">値</span><span class="sxs-lookup"><span data-stu-id="9a8a3-177">value</span></span>  
<span data-ttu-id="9a8a3-178">構成キー ID に割り当てられている値。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-178">The value that is being assigned for the configuration key ID.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="9a8a3-179">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="9a8a3-179">Return Value - configurationKey</span></span>

<span data-ttu-id="9a8a3-180">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-180">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="9a8a3-181">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="9a8a3-181">Remarks - configurationKey</span></span>

<span data-ttu-id="9a8a3-182">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-182">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="9a8a3-183">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-183">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="9a8a3-184">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="9a8a3-184">Method createdBy</span></span>

<span data-ttu-id="9a8a3-185">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-185">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="9a8a3-186">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="9a8a3-186">Parameters - createdBy</span></span>

<span data-ttu-id="9a8a3-187">値</span><span class="sxs-lookup"><span data-stu-id="9a8a3-187">value</span></span>  
<span data-ttu-id="9a8a3-188">ドキュメント ノードを作成したユーザーとして割り当てられている値。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-188">The value that is being assigned as the user who created the documentation node.</span></span>

### <a name="return-value---createdby"></a><span data-ttu-id="9a8a3-189">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="9a8a3-189">Return Value - createdBy</span></span>

<span data-ttu-id="9a8a3-190">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-190">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="9a8a3-191">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="9a8a3-191">Method creationDate</span></span>

<span data-ttu-id="9a8a3-192">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-192">Gets or sets the date that an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="9a8a3-193">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="9a8a3-193">Parameters - creationDate</span></span>

<span data-ttu-id="9a8a3-194">値</span><span class="sxs-lookup"><span data-stu-id="9a8a3-194">value</span></span>  
<span data-ttu-id="9a8a3-195">ドキュメント ノードの作成日として割り当てられている値。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-195">The value that is being assigned as the creation date for the documentation node.</span></span>

### <a name="return-value---creationdate"></a><span data-ttu-id="9a8a3-196">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="9a8a3-196">Return Value - creationDate</span></span>

<span data-ttu-id="9a8a3-197">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-197">The date that an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="9a8a3-198">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="9a8a3-198">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="9a8a3-199">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="9a8a3-199">Parameters - creationTime</span></span>

<span data-ttu-id="9a8a3-200">値</span><span class="sxs-lookup"><span data-stu-id="9a8a3-200">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="9a8a3-201">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="9a8a3-201">Return Value - creationTime</span></span>

## <a name="method-description"></a><span data-ttu-id="9a8a3-202">メソッドの説明</span><span class="sxs-lookup"><span data-stu-id="9a8a3-202">Method description</span></span>

<span data-ttu-id="9a8a3-203">ドキュメント ノードの説明を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-203">Sets or returns the description of the documentation node.</span></span>

```xpp
public str description([str value])
```

### <a name="parameters---description"></a><span data-ttu-id="9a8a3-204">パラメーター - description</span><span class="sxs-lookup"><span data-stu-id="9a8a3-204">Parameters - description</span></span>

<span data-ttu-id="9a8a3-205">値</span><span class="sxs-lookup"><span data-stu-id="9a8a3-205">value</span></span>  
<span data-ttu-id="9a8a3-206">ドキュメント ノードの説明として割り当てられている値。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-206">The value that is being assigned as the description of the documentation node.</span></span>

### <a name="return-value---description"></a><span data-ttu-id="9a8a3-207">戻り値 - description</span><span class="sxs-lookup"><span data-stu-id="9a8a3-207">Return Value - description</span></span>

<span data-ttu-id="9a8a3-208">ドキュメント ノードの説明の入力</span><span class="sxs-lookup"><span data-stu-id="9a8a3-208">The description of the documentation node.</span></span>

## <a name="method-name"></a><span data-ttu-id="9a8a3-209">メソッド名</span><span class="sxs-lookup"><span data-stu-id="9a8a3-209">Method name</span></span>

<span data-ttu-id="9a8a3-210">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-210">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="9a8a3-211">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="9a8a3-211">Parameters - name</span></span>

<span data-ttu-id="9a8a3-212">値</span><span class="sxs-lookup"><span data-stu-id="9a8a3-212">value</span></span>  
<span data-ttu-id="9a8a3-213">ドキュメント ノードに割り当てられている名前。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-213">The name that is being assigned to the documentation node.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="9a8a3-214">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="9a8a3-214">Return Value - name</span></span>

<span data-ttu-id="9a8a3-215">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-215">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="9a8a3-216">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="9a8a3-216">Remarks - name</span></span>

<span data-ttu-id="9a8a3-217">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-217">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="9a8a3-218">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-218">It must begin with a letter.</span></span>
-   <span data-ttu-id="9a8a3-219">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-219">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="9a8a3-220">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-220">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="9a8a3-221">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-221">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="9a8a3-222">テーブルは、拡張データ型、基本列挙型、およびクラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-222">Tables cannot have the same name as other public objects, such as extended data types, base enums, and classes.</span></span>

## <a name="method-neededaccesslevel"></a><span data-ttu-id="9a8a3-223">メソッド neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="9a8a3-223">Method neededAccessLevel</span></span>

<span data-ttu-id="9a8a3-224">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-224">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>

```xpp
public int neededAccessLevel([int value])
```

### <a name="parameters---neededaccesslevel"></a><span data-ttu-id="9a8a3-225">パラメーター - neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="9a8a3-225">Parameters - neededAccessLevel</span></span>

<span data-ttu-id="9a8a3-226">値</span><span class="sxs-lookup"><span data-stu-id="9a8a3-226">value</span></span>  

### <a name="return-value---neededaccesslevel"></a><span data-ttu-id="9a8a3-227">戻り値 - neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="9a8a3-227">Return Value - neededAccessLevel</span></span>

<span data-ttu-id="9a8a3-228">neededAccessLevel プロパティの現在の値。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-228">The current value of the neededAccessLevel property.</span></span>

### <a name="remarks---neededaccesslevel"></a><span data-ttu-id="9a8a3-229">備考 - neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="9a8a3-229">Remarks - neededAccessLevel</span></span>

<span data-ttu-id="9a8a3-230">AccessType システム列挙値の使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-230">The possible values for the AccessType system enumuration value are as follows:</span></span>

-   <span data-ttu-id="9a8a3-231">AccessType::NoAccess。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-231">AccessType::NoAccess.</span></span>
-   <span data-ttu-id="9a8a3-232">AccessType::View。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-232">AccessType::View.</span></span>
-   <span data-ttu-id="9a8a3-233">AccessType::Edit。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-233">AccessType::Edit.</span></span>
-   <span data-ttu-id="9a8a3-234">AccessType::Add。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-234">AccessType::Add.</span></span>
-   <span data-ttu-id="9a8a3-235">AccessType::Delete。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-235">AccessType::Delete.</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="9a8a3-236">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="9a8a3-236">Method securityKey</span></span>

<span data-ttu-id="9a8a3-237">ドキュメント ノードのセキュリティ キーを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-237">Sets or returns the security key for the documentation node.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="9a8a3-238">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="9a8a3-238">Parameters - securityKey</span></span>

<span data-ttu-id="9a8a3-239">値</span><span class="sxs-lookup"><span data-stu-id="9a8a3-239">value</span></span>  
<span data-ttu-id="9a8a3-240">セキュリティ キー ID に割り当てられている値。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-240">The value that is being assigned for the security key ID.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="9a8a3-241">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="9a8a3-241">Return Value - securityKey</span></span>

<span data-ttu-id="9a8a3-242">ドキュメント ノードのセキュリティ キー ID。ドキュメント ノードにセキュリティ キーが関連付けられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-242">The security key ID for the documentation node; 0 (zero) if no security key is associated with the documentation node.</span></span>

## <a name="method-title"></a><span data-ttu-id="9a8a3-243">メソッド title</span><span class="sxs-lookup"><span data-stu-id="9a8a3-243">Method title</span></span>

<span data-ttu-id="9a8a3-244">ドキュメント ノードのタイトルを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-244">Sets or returns the title of the documentation node.</span></span>

```xpp
public str title([str value])
```

### <a name="parameters---title"></a><span data-ttu-id="9a8a3-245">パラメーター - title</span><span class="sxs-lookup"><span data-stu-id="9a8a3-245">Parameters - title</span></span>

<span data-ttu-id="9a8a3-246">値</span><span class="sxs-lookup"><span data-stu-id="9a8a3-246">value</span></span>  
<span data-ttu-id="9a8a3-247">ドキュメント ノードに割り当てられているタイトル。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-247">The title that is being assigned to the documentation node.</span></span>

### <a name="return-value---title"></a><span data-ttu-id="9a8a3-248">戻り値 - title</span><span class="sxs-lookup"><span data-stu-id="9a8a3-248">Return Value - title</span></span>

<span data-ttu-id="9a8a3-249">ドキュメント ノードのタイトル。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-249">The title of the documentation node.</span></span>

## <a name="method-findaotelementdocnode"></a><span data-ttu-id="9a8a3-250">メソッド findAOTElementDocNode</span><span class="sxs-lookup"><span data-stu-id="9a8a3-250">Method findAOTElementDocNode</span></span>

<span data-ttu-id="9a8a3-251">アプリケーション オブジェクト ツリー (AOT) で要素ドキュメント ノードの検索を実行します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-251">Performs a search for an element documentation node in the Application Object Tree (AOT).</span></span>

```xpp
public static DocNode findAOTElementDocNode(ApplCodeDocType HelpType, str Name, [str ParentName], [int Mode])
```

### <a name="parameters---findaotelementdocnode"></a><span data-ttu-id="9a8a3-252">パラメーター - findAOTElementDocNode</span><span class="sxs-lookup"><span data-stu-id="9a8a3-252">Parameters - findAOTElementDocNode</span></span>

<span data-ttu-id="9a8a3-253">HelpType</span><span class="sxs-lookup"><span data-stu-id="9a8a3-253">HelpType</span></span>  
<span data-ttu-id="9a8a3-254">検索に使用するモード (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-254">The mode to use for the search; optional.</span></span>

<!-- -->

<span data-ttu-id="9a8a3-255">氏名</span><span class="sxs-lookup"><span data-stu-id="9a8a3-255">Name</span></span>  
<span data-ttu-id="9a8a3-256">検索に使用するモード (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-256">The mode to use for the search; optional.</span></span>

<!-- -->

<span data-ttu-id="9a8a3-257">ParentName</span><span class="sxs-lookup"><span data-stu-id="9a8a3-257">ParentName</span></span>  
<span data-ttu-id="9a8a3-258">検索に使用するモード (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-258">The mode to use for the search; optional.</span></span>

<!-- -->

<span data-ttu-id="9a8a3-259">モード</span><span class="sxs-lookup"><span data-stu-id="9a8a3-259">Mode</span></span>  
<span data-ttu-id="9a8a3-260">検索に使用するモード (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-260">The mode to use for the search; optional.</span></span>

### <a name="return-value---findaotelementdocnode"></a><span data-ttu-id="9a8a3-261">戻り値 - findAOTElementDocNode</span><span class="sxs-lookup"><span data-stu-id="9a8a3-261">Return Value - findAOTElementDocNode</span></span>

<span data-ttu-id="9a8a3-262">検出されたノード。それ以外の場合は、null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-262">The node that is found; otherwise, null, Nothing, nullptr, unit, a null reference (Nothing in Visual Basic).</span></span>

## <a name="method-findapplicationdocnode"></a><span data-ttu-id="9a8a3-263">メソッド findApplicationDocNode</span><span class="sxs-lookup"><span data-stu-id="9a8a3-263">Method findApplicationDocNode</span></span>

<span data-ttu-id="9a8a3-264">アプリケーション要素ドキュメント ノードの検索を実行します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-264">Performs a search for an application element documentation node.</span></span>

```xpp
public static DocNode findApplicationDocNode(ApplHelpType HelpType, str Name, [str ParentName], [int Mode])
```

### <a name="parameters---findapplicationdocnode"></a><span data-ttu-id="9a8a3-265">パラメーター - findApplicationDocNode</span><span class="sxs-lookup"><span data-stu-id="9a8a3-265">Parameters - findApplicationDocNode</span></span>

<span data-ttu-id="9a8a3-266">HelpType</span><span class="sxs-lookup"><span data-stu-id="9a8a3-266">HelpType</span></span>  
<span data-ttu-id="9a8a3-267">検索に使用するモード (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-267">The mode to use for the search; optional.</span></span>

<!-- -->

<span data-ttu-id="9a8a3-268">氏名</span><span class="sxs-lookup"><span data-stu-id="9a8a3-268">Name</span></span>  
<span data-ttu-id="9a8a3-269">検索に使用するモード (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-269">The mode to use for the search; optional.</span></span>

<!-- -->

<span data-ttu-id="9a8a3-270">ParentName</span><span class="sxs-lookup"><span data-stu-id="9a8a3-270">ParentName</span></span>  
<span data-ttu-id="9a8a3-271">検索に使用するモード (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-271">The mode to use for the search; optional.</span></span>

<!-- -->

<span data-ttu-id="9a8a3-272">モード</span><span class="sxs-lookup"><span data-stu-id="9a8a3-272">Mode</span></span>  
<span data-ttu-id="9a8a3-273">検索に使用するモード (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-273">The mode to use for the search; optional.</span></span>

### <a name="return-value---findapplicationdocnode"></a><span data-ttu-id="9a8a3-274">戻り値 - findApplicationDocNode</span><span class="sxs-lookup"><span data-stu-id="9a8a3-274">Return Value - findApplicationDocNode</span></span>

<span data-ttu-id="9a8a3-275">検出されたノード。ノードが検出されなかった場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-275">The node that is found; null, Nothing, nullptr, unit, a null reference (Nothing in Visual Basic) if the node was not found.</span></span>

## <a name="method-findkerneldocnode"></a><span data-ttu-id="9a8a3-276">メソッド findKernelDocNode</span><span class="sxs-lookup"><span data-stu-id="9a8a3-276">Method findKernelDocNode</span></span>

<span data-ttu-id="9a8a3-277">カーネル要素ドキュメント ノードの検索を実行します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-277">Performs a search for a kernel element documentation node.</span></span>

```xpp
public static DocNode findKernelDocNode(KernelHelpType HelpType, str Name, [str ParentName], [int Mode])
```

### <a name="parameters---findkerneldocnode"></a><span data-ttu-id="9a8a3-278">パラメーター - findKernelDocNode</span><span class="sxs-lookup"><span data-stu-id="9a8a3-278">Parameters - findKernelDocNode</span></span>

<span data-ttu-id="9a8a3-279">HelpType</span><span class="sxs-lookup"><span data-stu-id="9a8a3-279">HelpType</span></span>  
<span data-ttu-id="9a8a3-280">検索に使用するモード (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-280">The mode to use for the search; optional.</span></span>

<!-- -->

<span data-ttu-id="9a8a3-281">氏名</span><span class="sxs-lookup"><span data-stu-id="9a8a3-281">Name</span></span>  
<span data-ttu-id="9a8a3-282">検索に使用するモード (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-282">The mode to use for the search; optional.</span></span>

<!-- -->

<span data-ttu-id="9a8a3-283">ParentName</span><span class="sxs-lookup"><span data-stu-id="9a8a3-283">ParentName</span></span>  
<span data-ttu-id="9a8a3-284">検索に使用するモード (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-284">The mode to use for the search; optional.</span></span>

<!-- -->

<span data-ttu-id="9a8a3-285">モード</span><span class="sxs-lookup"><span data-stu-id="9a8a3-285">Mode</span></span>  
<span data-ttu-id="9a8a3-286">検索に使用するモード (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-286">The mode to use for the search; optional.</span></span>

### <a name="return-value---findkerneldocnode"></a><span data-ttu-id="9a8a3-287">戻り値 - findKernelDocNode</span><span class="sxs-lookup"><span data-stu-id="9a8a3-287">Return Value - findKernelDocNode</span></span>

<span data-ttu-id="9a8a3-288">検出されたノード。それ以外の場合は、null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-288">The node that is found; otherwise, null, Nothing, nullptr, unit, a null reference (Nothing in Visual Basic).</span></span>

## <a name="method-getnodedetached"></a><span data-ttu-id="9a8a3-289">メソッド getNodeDetached</span><span class="sxs-lookup"><span data-stu-id="9a8a3-289">Method getNodeDetached</span></span>

<span data-ttu-id="9a8a3-290">指定したドキュメントのノードを返します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-290">Returns the specified documentation node.</span></span>

```xpp
public static DocNode getNodeDetached(UtilFileType helpType, int UtilType, str Name, [int ParentId], [int Type], [UtilEntryLevel Utillevel], [boolean Forcelevel], [boolean OldUtil])
```

### <a name="parameters---getnodedetached"></a><span data-ttu-id="9a8a3-291">パラメーター - getNodeDetached</span><span class="sxs-lookup"><span data-stu-id="9a8a3-291">Parameters - getNodeDetached</span></span>

<span data-ttu-id="9a8a3-292">helpType</span><span class="sxs-lookup"><span data-stu-id="9a8a3-292">helpType</span></span>  
<span data-ttu-id="9a8a3-293">引当済。省略可能です。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-293">Reserved; optional.</span></span>

<!-- -->

<span data-ttu-id="9a8a3-294">UtilType</span><span class="sxs-lookup"><span data-stu-id="9a8a3-294">UtilType</span></span>  
<span data-ttu-id="9a8a3-295">引当済。省略可能です。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-295">Reserved; optional.</span></span>

<!-- -->

<span data-ttu-id="9a8a3-296">氏名</span><span class="sxs-lookup"><span data-stu-id="9a8a3-296">Name</span></span>  
<span data-ttu-id="9a8a3-297">引当済。省略可能です。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-297">Reserved; optional.</span></span>

<!-- -->

<span data-ttu-id="9a8a3-298">ParentId</span><span class="sxs-lookup"><span data-stu-id="9a8a3-298">ParentId</span></span>  
<span data-ttu-id="9a8a3-299">引当済。省略可能です。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-299">Reserved; optional.</span></span>

<!-- -->

<span data-ttu-id="9a8a3-300">種類</span><span class="sxs-lookup"><span data-stu-id="9a8a3-300">Type</span></span>  
<span data-ttu-id="9a8a3-301">引当済。省略可能です。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-301">Reserved; optional.</span></span>

<!-- -->

<span data-ttu-id="9a8a3-302">Utillevel</span><span class="sxs-lookup"><span data-stu-id="9a8a3-302">Utillevel</span></span>  
<span data-ttu-id="9a8a3-303">引当済。省略可能です。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-303">Reserved; optional.</span></span>

<!-- -->

<span data-ttu-id="9a8a3-304">Forcelevel</span><span class="sxs-lookup"><span data-stu-id="9a8a3-304">Forcelevel</span></span>  
<span data-ttu-id="9a8a3-305">引当済。省略可能です。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-305">Reserved; optional.</span></span>

<!-- -->

<span data-ttu-id="9a8a3-306">OldUtil</span><span class="sxs-lookup"><span data-stu-id="9a8a3-306">OldUtil</span></span>  
<span data-ttu-id="9a8a3-307">引当済。省略可能です。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-307">Reserved; optional.</span></span>

### <a name="return-value---getnodedetached"></a><span data-ttu-id="9a8a3-308">戻り値 - getNodeDetached</span><span class="sxs-lookup"><span data-stu-id="9a8a3-308">Return Value - getNodeDetached</span></span>

<span data-ttu-id="9a8a3-309">指定したドキュメントのノードです。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-309">The specified documentation node.</span></span>

## <a name="method-aotsetsource"></a><span data-ttu-id="9a8a3-310">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="9a8a3-310">Method AOTsetSource</span></span>

<span data-ttu-id="9a8a3-311">ノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-311">Sets the source code for the node.</span></span>

```xpp
public void AOTsetSource(str source, [boolean isStatic])
```

### <a name="parameters---aotsetsource"></a><span data-ttu-id="9a8a3-312">パラメーター - AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="9a8a3-312">Parameters - AOTsetSource</span></span>

<span data-ttu-id="9a8a3-313">ソース</span><span class="sxs-lookup"><span data-stu-id="9a8a3-313">source</span></span>  
<span data-ttu-id="9a8a3-314">メソッドが静的かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-314">A Boolean value that indicates whether the method is static.</span></span>

<!-- -->

<span data-ttu-id="9a8a3-315">isStatic</span><span class="sxs-lookup"><span data-stu-id="9a8a3-315">isStatic</span></span>  
<span data-ttu-id="9a8a3-316">メソッドが静的かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-316">A Boolean value that indicates whether the method is static.</span></span>

## <a name="method-aotedit"></a><span data-ttu-id="9a8a3-317">メソッド AOTedit</span><span class="sxs-lookup"><span data-stu-id="9a8a3-317">Method AOTedit</span></span>

<span data-ttu-id="9a8a3-318">このノードの適切なエディタを開きます。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-318">Opens the appropriate editor for this node.</span></span>

```xpp
public void AOTedit([int Line], [int Column])
```

### <a name="parameters---aotedit"></a><span data-ttu-id="9a8a3-319">パラメーター - AOTedit</span><span class="sxs-lookup"><span data-stu-id="9a8a3-319">Parameters - AOTedit</span></span>

<span data-ttu-id="9a8a3-320">折れ線</span><span class="sxs-lookup"><span data-stu-id="9a8a3-320">Line</span></span>  
<span data-ttu-id="9a8a3-321">カーソル位置の列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-321">The column of the cursor position; optional.</span></span>

<!-- -->

<span data-ttu-id="9a8a3-322">円柱</span><span class="sxs-lookup"><span data-stu-id="9a8a3-322">Column</span></span>  
<span data-ttu-id="9a8a3-323">カーソル位置の列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-323">The column of the cursor position; optional.</span></span>

### <a name="remarks---aotedit"></a><span data-ttu-id="9a8a3-324">備考 - AOTedit</span><span class="sxs-lookup"><span data-stu-id="9a8a3-324">Remarks - AOTedit</span></span>

<span data-ttu-id="9a8a3-325">ノードがメソッドである場合は、コード エディタが開きます。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-325">If the node is a method, the code editor opens.</span></span> <span data-ttu-id="9a8a3-326">ノードがドキュメンテーションの対象である場合は、ヘルプ エディタが開きます。</span><span class="sxs-lookup"><span data-stu-id="9a8a3-326">If the node is a documentation object, the Help editor opens.</span></span>

