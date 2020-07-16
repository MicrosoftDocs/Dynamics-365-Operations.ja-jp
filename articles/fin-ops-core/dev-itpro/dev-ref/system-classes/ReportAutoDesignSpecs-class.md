---
title: ReportAutoDesignSpecs クラス
description: このトピックでは、ReportAutoDesignSpecs クラスについて説明します。
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
ms.openlocfilehash: 59471ab8b56da13773ed6bf83ca9535ab9795193
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502847"
---
# <a name="class-reportautodesignspecs"></a><span data-ttu-id="2d179-103">クラス ReportAutoDesignSpecs</span><span class="sxs-lookup"><span data-stu-id="2d179-103">Class ReportAutoDesignSpecs</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportAutoDesignSpecs extends TreeNode
```

<span data-ttu-id="2d179-104">ReportAutoDesignSpecs クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="2d179-104">The ReportAutoDesignSpecs class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d179-105">備考</span><span class="sxs-lookup"><span data-stu-id="2d179-105">Remarks</span></span>

<span data-ttu-id="2d179-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2d179-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="2d179-107">例</span><span class="sxs-lookup"><span data-stu-id="2d179-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="2d179-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="2d179-108">Methods</span></span>

| <span data-ttu-id="2d179-109">方法</span><span class="sxs-lookup"><span data-stu-id="2d179-109">Method</span></span>                                                                            | <span data-ttu-id="2d179-110">説明</span><span class="sxs-lookup"><span data-stu-id="2d179-110">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="2d179-111">public ReportSection addProgrammableSection(int number)</span><span class="sxs-lookup"><span data-stu-id="2d179-111">public ReportSection addProgrammableSection(int number)</span></span>                           |                                                                    |
| <span data-ttu-id="2d179-112">public ReportSection addSection(ReportBlockType sectionType, \[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="2d179-112">public ReportSection addSection(ReportBlockType sectionType, \[TableId tableId\])</span></span> |                                                                    |
| <span data-ttu-id="2d179-113">public boolean autoHeader(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2d179-113">public boolean autoHeader(\[boolean value\])</span></span>                                      |                                                                    |
| <span data-ttu-id="2d179-114">public str footerText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2d179-114">public str footerText(\[str value\])</span></span>                                              |                                                                    |
| <span data-ttu-id="2d179-115">public boolean grandHeader(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2d179-115">public boolean grandHeader(\[boolean value\])</span></span>                                     |                                                                    |
| <span data-ttu-id="2d179-116">public boolean grandTotal(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2d179-116">public boolean grandTotal(\[boolean value\])</span></span>                                      | <span data-ttu-id="2d179-117">FooterText プロパティ値が表示されるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2d179-117">Determines whether the FooterText property value can be displayed.</span></span> |
| <span data-ttu-id="2d179-118">public str headerText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2d179-118">public str headerText(\[str value\])</span></span>                                              |                                                                    |
| <span data-ttu-id="2d179-119">public boolean view()</span><span class="sxs-lookup"><span data-stu-id="2d179-119">public boolean view()</span></span>                                                             |                                                                    |

## <a name="method-addprogrammablesection"></a><span data-ttu-id="2d179-120">メソッド addProgrammableSection</span><span class="sxs-lookup"><span data-stu-id="2d179-120">Method addProgrammableSection</span></span>

```xpp
public ReportSection addProgrammableSection(int number)
```

### <a name="parameters---addprogrammablesection"></a><span data-ttu-id="2d179-121">パラメーター - addProgrammableSection</span><span class="sxs-lookup"><span data-stu-id="2d179-121">Parameters - addProgrammableSection</span></span>

<span data-ttu-id="2d179-122">番号</span><span class="sxs-lookup"><span data-stu-id="2d179-122">number</span></span>  

### <a name="return-value---addprogrammablesection"></a><span data-ttu-id="2d179-123">戻り値 - addProgrammableSection</span><span class="sxs-lookup"><span data-stu-id="2d179-123">Return Value - addProgrammableSection</span></span>

## <a name="method-addsection"></a><span data-ttu-id="2d179-124">メソッド addSection</span><span class="sxs-lookup"><span data-stu-id="2d179-124">Method addSection</span></span>

```xpp
public ReportSection addSection(ReportBlockType sectionType, [TableId tableId])
```

### <a name="parameters---addsection"></a><span data-ttu-id="2d179-125">パラメーター - addSection</span><span class="sxs-lookup"><span data-stu-id="2d179-125">Parameters - addSection</span></span>

<span data-ttu-id="2d179-126">sectionType</span><span class="sxs-lookup"><span data-stu-id="2d179-126">sectionType</span></span>  

<!-- -->

<span data-ttu-id="2d179-127">tableId</span><span class="sxs-lookup"><span data-stu-id="2d179-127">tableId</span></span>  

### <a name="return-value---addsection"></a><span data-ttu-id="2d179-128">戻り値 - addSection</span><span class="sxs-lookup"><span data-stu-id="2d179-128">Return Value - addSection</span></span>

## <a name="method-autoheader"></a><span data-ttu-id="2d179-129">メソッド autoHeader</span><span class="sxs-lookup"><span data-stu-id="2d179-129">Method autoHeader</span></span>

```xpp
public boolean autoHeader([boolean value])
```

### <a name="parameters---autoheader"></a><span data-ttu-id="2d179-130">パラメーター - autoHeader</span><span class="sxs-lookup"><span data-stu-id="2d179-130">Parameters - autoHeader</span></span>

<span data-ttu-id="2d179-131">値</span><span class="sxs-lookup"><span data-stu-id="2d179-131">value</span></span>  

### <a name="return-value---autoheader"></a><span data-ttu-id="2d179-132">戻り値 - autoHeader</span><span class="sxs-lookup"><span data-stu-id="2d179-132">Return Value - autoHeader</span></span>

## <a name="method-footertext"></a><span data-ttu-id="2d179-133">メソッド footerText</span><span class="sxs-lookup"><span data-stu-id="2d179-133">Method footerText</span></span>

```xpp
public str footerText([str value])
```

### <a name="parameters---footertext"></a><span data-ttu-id="2d179-134">パラメーター - footerText</span><span class="sxs-lookup"><span data-stu-id="2d179-134">Parameters - footerText</span></span>

<span data-ttu-id="2d179-135">値</span><span class="sxs-lookup"><span data-stu-id="2d179-135">value</span></span>  

### <a name="return-value---footertext"></a><span data-ttu-id="2d179-136">戻り値 - footerText</span><span class="sxs-lookup"><span data-stu-id="2d179-136">Return Value - footerText</span></span>

## <a name="method-grandheader"></a><span data-ttu-id="2d179-137">メソッド grandHeader</span><span class="sxs-lookup"><span data-stu-id="2d179-137">Method grandHeader</span></span>

```xpp
public boolean grandHeader([boolean value])
```

### <a name="parameters---grandheader"></a><span data-ttu-id="2d179-138">パラメーター - grandHeader</span><span class="sxs-lookup"><span data-stu-id="2d179-138">Parameters - grandHeader</span></span>

<span data-ttu-id="2d179-139">値</span><span class="sxs-lookup"><span data-stu-id="2d179-139">value</span></span>  

### <a name="return-value---grandheader"></a><span data-ttu-id="2d179-140">戻り値 - grandHeader</span><span class="sxs-lookup"><span data-stu-id="2d179-140">Return Value - grandHeader</span></span>

## <a name="method-grandtotal"></a><span data-ttu-id="2d179-141">メソッド grandTotal</span><span class="sxs-lookup"><span data-stu-id="2d179-141">Method grandTotal</span></span>

<span data-ttu-id="2d179-142">FooterText プロパティ値が表示されるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2d179-142">Determines whether the FooterText property value can be displayed.</span></span>

```xpp
public boolean grandTotal([boolean value])
```

### <a name="parameters---grandtotal"></a><span data-ttu-id="2d179-143">パラメーター - grandTotal</span><span class="sxs-lookup"><span data-stu-id="2d179-143">Parameters - grandTotal</span></span>

<span data-ttu-id="2d179-144">値</span><span class="sxs-lookup"><span data-stu-id="2d179-144">value</span></span>  

### <a name="return-value---grandtotal"></a><span data-ttu-id="2d179-145">戻り値 - grandTotal</span><span class="sxs-lookup"><span data-stu-id="2d179-145">Return Value - grandTotal</span></span>

<span data-ttu-id="2d179-146">FooterText プロパティ値が表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2d179-146">true if the FooterText property value is displayed; otherwise, false.</span></span>

### <a name="remarks---grandtotal"></a><span data-ttu-id="2d179-147">備考 - grandTotal</span><span class="sxs-lookup"><span data-stu-id="2d179-147">Remarks - grandTotal</span></span>

<span data-ttu-id="2d179-148">grandTotal プロパティは、レポートに複数のデータ ソースがテストされていない場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="2d179-148">The grandTotal property is available only when a report has untested, multiple data sources.</span></span>

## <a name="method-headertext"></a><span data-ttu-id="2d179-149">メソッド headerText</span><span class="sxs-lookup"><span data-stu-id="2d179-149">Method headerText</span></span>

```xpp
public str headerText([str value])
```

### <a name="parameters---headertext"></a><span data-ttu-id="2d179-150">パラメーター - headerText</span><span class="sxs-lookup"><span data-stu-id="2d179-150">Parameters - headerText</span></span>

<span data-ttu-id="2d179-151">値</span><span class="sxs-lookup"><span data-stu-id="2d179-151">value</span></span>  

### <a name="return-value---headertext"></a><span data-ttu-id="2d179-152">戻り値 - headerText</span><span class="sxs-lookup"><span data-stu-id="2d179-152">Return Value - headerText</span></span>

## <a name="method-view"></a><span data-ttu-id="2d179-153">メソッド view</span><span class="sxs-lookup"><span data-stu-id="2d179-153">Method view</span></span>

```xpp
public boolean view()
```

### <a name="return-value---view"></a><span data-ttu-id="2d179-154">戻り値 - view</span><span class="sxs-lookup"><span data-stu-id="2d179-154">Return Value - view</span></span>

