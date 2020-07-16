---
title: ReportSectionGroup クラス
description: このトピックでは、ReportSectionGroup クラスについて説明します。
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
ms.openlocfilehash: e19e72ab3ef5b66b2001a2f5c052232b591f9e74
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502829"
---
# <a name="class-reportsectiongroup"></a><span data-ttu-id="aa0bb-103">クラス ReportSectionGroup</span><span class="sxs-lookup"><span data-stu-id="aa0bb-103">Class ReportSectionGroup</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportSectionGroup extends TreeNode
```

<span data-ttu-id="aa0bb-104">ReportSectionGroup クラスは、レポート セクションのコレクションを定義します。</span><span class="sxs-lookup"><span data-stu-id="aa0bb-104">The ReportSectionGroup class defines a collection of report sections.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa0bb-105">備考</span><span class="sxs-lookup"><span data-stu-id="aa0bb-105">Remarks</span></span>

<span data-ttu-id="aa0bb-106">レポート セクション グループは、ヘッダー セクション、本文セクション、フッター セクションを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="aa0bb-106">A report section group can contain header sections, body sections, and footer sections.</span></span> <span data-ttu-id="aa0bb-107">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="aa0bb-107">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="aa0bb-108">この API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa0bb-108">You must have access to the development security key (SysDevelopment) before you call this API.</span></span>

## <a name="examples"></a><span data-ttu-id="aa0bb-109">例</span><span class="sxs-lookup"><span data-stu-id="aa0bb-109">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="aa0bb-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="aa0bb-110">Methods</span></span>

| <span data-ttu-id="aa0bb-111">方法</span><span class="sxs-lookup"><span data-stu-id="aa0bb-111">Method</span></span>                                                       | <span data-ttu-id="aa0bb-112">説明</span><span class="sxs-lookup"><span data-stu-id="aa0bb-112">Description</span></span>                                                                                                               |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0bb-113">public ReportSection addSection(ReportBlockType sectionType)</span><span class="sxs-lookup"><span data-stu-id="aa0bb-113">public ReportSection addSection(ReportBlockType sectionType)</span></span> |                                                                                                                           |
| <span data-ttu-id="aa0bb-114">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="aa0bb-114">public FieldId dataField(\[FieldId value\])</span></span>                  |                                                                                                                           |
| <span data-ttu-id="aa0bb-115">public int delete()</span><span class="sxs-lookup"><span data-stu-id="aa0bb-115">public int delete()</span></span>                                          |                                                                                                                           |
| <span data-ttu-id="aa0bb-116">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="aa0bb-116">public str name(\[str value\])</span></span>                               | <span data-ttu-id="aa0bb-117">フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="aa0bb-117">Gets or sets the name that is used in code to identify a form, report, table, query, or another MSDAX application object.</span></span> |
| <span data-ttu-id="aa0bb-118">public ReportSection section(ReportBlockType sectionType)</span><span class="sxs-lookup"><span data-stu-id="aa0bb-118">public ReportSection section(ReportBlockType sectionType)</span></span>    |                                                                                                                           |
| <span data-ttu-id="aa0bb-119">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="aa0bb-119">public TableId table(\[TableId value\])</span></span>                      | <span data-ttu-id="aa0bb-120">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="aa0bb-120">Gets or sets the table ID associated with the object.</span></span>                                                                     |

## <a name="method-addsection"></a><span data-ttu-id="aa0bb-121">メソッド addSection</span><span class="sxs-lookup"><span data-stu-id="aa0bb-121">Method addSection</span></span>

```xpp
public ReportSection addSection(ReportBlockType sectionType)
```

### <a name="parameters---addsection"></a><span data-ttu-id="aa0bb-122">パラメーター - addSection</span><span class="sxs-lookup"><span data-stu-id="aa0bb-122">Parameters - addSection</span></span>

<span data-ttu-id="aa0bb-123">sectionType</span><span class="sxs-lookup"><span data-stu-id="aa0bb-123">sectionType</span></span>  

### <a name="return-value---addsection"></a><span data-ttu-id="aa0bb-124">戻り値 - addSection</span><span class="sxs-lookup"><span data-stu-id="aa0bb-124">Return Value - addSection</span></span>

## <a name="method-datafield"></a><span data-ttu-id="aa0bb-125">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="aa0bb-125">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="aa0bb-126">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="aa0bb-126">Parameters - dataField</span></span>

<span data-ttu-id="aa0bb-127">値</span><span class="sxs-lookup"><span data-stu-id="aa0bb-127">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="aa0bb-128">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="aa0bb-128">Return Value - dataField</span></span>

## <a name="method-delete"></a><span data-ttu-id="aa0bb-129">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="aa0bb-129">Method delete</span></span>

```xpp
public int delete()
```

### <a name="return-value---delete"></a><span data-ttu-id="aa0bb-130">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="aa0bb-130">Return Value - delete</span></span>

## <a name="method-name"></a><span data-ttu-id="aa0bb-131">メソッド名</span><span class="sxs-lookup"><span data-stu-id="aa0bb-131">Method name</span></span>

<span data-ttu-id="aa0bb-132">フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="aa0bb-132">Gets or sets the name that is used in code to identify a form, report, table, query, or another MSDAX application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="aa0bb-133">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="aa0bb-133">Parameters - name</span></span>

<span data-ttu-id="aa0bb-134">値</span><span class="sxs-lookup"><span data-stu-id="aa0bb-134">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="aa0bb-135">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="aa0bb-135">Return Value - name</span></span>

<span data-ttu-id="aa0bb-136">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="aa0bb-136">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="aa0bb-137">備考 - name</span><span class="sxs-lookup"><span data-stu-id="aa0bb-137">Remarks - name</span></span>

<span data-ttu-id="aa0bb-138">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa0bb-138">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="aa0bb-139">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="aa0bb-139">Begins with a letter.</span></span>
-   <span data-ttu-id="aa0bb-140">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="aa0bb-140">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="aa0bb-141">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="aa0bb-141">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="aa0bb-142">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="aa0bb-142">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="aa0bb-143">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="aa0bb-143">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-section"></a><span data-ttu-id="aa0bb-144">メソッド section</span><span class="sxs-lookup"><span data-stu-id="aa0bb-144">Method section</span></span>

```xpp
public ReportSection section(ReportBlockType sectionType)
```

### <a name="parameters---section"></a><span data-ttu-id="aa0bb-145">パラメーター - section</span><span class="sxs-lookup"><span data-stu-id="aa0bb-145">Parameters - section</span></span>

<span data-ttu-id="aa0bb-146">sectionType</span><span class="sxs-lookup"><span data-stu-id="aa0bb-146">sectionType</span></span>  

### <a name="return-value---section"></a><span data-ttu-id="aa0bb-147">戻り値 - section</span><span class="sxs-lookup"><span data-stu-id="aa0bb-147">Return Value - section</span></span>

## <a name="method-table"></a><span data-ttu-id="aa0bb-148">メソッド table</span><span class="sxs-lookup"><span data-stu-id="aa0bb-148">Method table</span></span>

<span data-ttu-id="aa0bb-149">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="aa0bb-149">Gets or sets the table ID associated with the object.</span></span>

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a><span data-ttu-id="aa0bb-150">パラメーター - table</span><span class="sxs-lookup"><span data-stu-id="aa0bb-150">Parameters - table</span></span>

<span data-ttu-id="aa0bb-151">値</span><span class="sxs-lookup"><span data-stu-id="aa0bb-151">value</span></span>  

### <a name="return-value---table"></a><span data-ttu-id="aa0bb-152">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="aa0bb-152">Return Value - table</span></span>

<span data-ttu-id="aa0bb-153">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="aa0bb-153">The current value of the table ID associated with the object.</span></span>

