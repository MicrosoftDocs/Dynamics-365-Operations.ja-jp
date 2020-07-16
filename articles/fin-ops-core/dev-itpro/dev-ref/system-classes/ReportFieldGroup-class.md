---
title: ReportFieldGroup クラス
description: このトピックでは、ReportFieldGroup クラスについて説明します。
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
ms.openlocfilehash: fc6cb020861ff94f9f599570f4e8531ecff87812
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502840"
---
# <a name="class-reportfieldgroup"></a><span data-ttu-id="996ff-103">クラス ReportFieldGroup</span><span class="sxs-lookup"><span data-stu-id="996ff-103">Class ReportFieldGroup</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportFieldGroup extends TreeNode
```

<span data-ttu-id="996ff-104">ReportFieldGroup クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="996ff-104">The ReportFieldGroup class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="996ff-105">備考</span><span class="sxs-lookup"><span data-stu-id="996ff-105">Remarks</span></span>

<span data-ttu-id="996ff-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="996ff-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="996ff-107">例</span><span class="sxs-lookup"><span data-stu-id="996ff-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="996ff-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="996ff-108">Methods</span></span>

| <span data-ttu-id="996ff-109">方法</span><span class="sxs-lookup"><span data-stu-id="996ff-109">Method</span></span>                                        | <span data-ttu-id="996ff-110">説明</span><span class="sxs-lookup"><span data-stu-id="996ff-110">Description</span></span>                                                   |
|-----------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="996ff-111">public int autoFieldGroupOrder(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="996ff-111">public int autoFieldGroupOrder(\[int value\])</span></span> |                                                               |
| <span data-ttu-id="996ff-112">public str dataGroup(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="996ff-112">public str dataGroup(\[str value\])</span></span>           |                                                               |
| <span data-ttu-id="996ff-113">public int fieldCount()</span><span class="sxs-lookup"><span data-stu-id="996ff-113">public int fieldCount()</span></span>                       |                                                               |
| <span data-ttu-id="996ff-114">public ReportControl fieldNumber(int number)</span><span class="sxs-lookup"><span data-stu-id="996ff-114">public ReportControl fieldNumber(int number)</span></span>  |                                                               |
| <span data-ttu-id="996ff-115">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="996ff-115">public TableId table(\[TableId value\])</span></span>       | <span data-ttu-id="996ff-116">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="996ff-116">Gets or sets the table ID that is associated with the object.</span></span> |

## <a name="method-autofieldgrouporder"></a><span data-ttu-id="996ff-117">メソッド autoFieldGroupOrder</span><span class="sxs-lookup"><span data-stu-id="996ff-117">Method autoFieldGroupOrder</span></span>

```xpp
public int autoFieldGroupOrder([int value])
```

### <a name="parameters---autofieldgrouporder"></a><span data-ttu-id="996ff-118">パラメーター - autoFieldGroupOrder</span><span class="sxs-lookup"><span data-stu-id="996ff-118">Parameters - autoFieldGroupOrder</span></span>

<span data-ttu-id="996ff-119">値</span><span class="sxs-lookup"><span data-stu-id="996ff-119">value</span></span>  

### <a name="return-value---autofieldgrouporder"></a><span data-ttu-id="996ff-120">戻り値 - autoFieldGroupOrder</span><span class="sxs-lookup"><span data-stu-id="996ff-120">Return Value - autoFieldGroupOrder</span></span>

## <a name="method-datagroup"></a><span data-ttu-id="996ff-121">メソッド dataGroup</span><span class="sxs-lookup"><span data-stu-id="996ff-121">Method dataGroup</span></span>

```xpp
public str dataGroup([str value])
```

### <a name="parameters---datagroup"></a><span data-ttu-id="996ff-122">パラメーター - dataGroup</span><span class="sxs-lookup"><span data-stu-id="996ff-122">Parameters - dataGroup</span></span>

<span data-ttu-id="996ff-123">値</span><span class="sxs-lookup"><span data-stu-id="996ff-123">value</span></span>  

### <a name="return-value---datagroup"></a><span data-ttu-id="996ff-124">戻り値 - dataGroup</span><span class="sxs-lookup"><span data-stu-id="996ff-124">Return Value - dataGroup</span></span>

## <a name="method-fieldcount"></a><span data-ttu-id="996ff-125">メソッド fieldCount</span><span class="sxs-lookup"><span data-stu-id="996ff-125">Method fieldCount</span></span>

```xpp
public int fieldCount()
```

### <a name="return-value---fieldcount"></a><span data-ttu-id="996ff-126">戻り値 - fieldCount</span><span class="sxs-lookup"><span data-stu-id="996ff-126">Return Value - fieldCount</span></span>

## <a name="method-fieldnumber"></a><span data-ttu-id="996ff-127">メソッド fieldNumber</span><span class="sxs-lookup"><span data-stu-id="996ff-127">Method fieldNumber</span></span>

```xpp
public ReportControl fieldNumber(int number)
```

### <a name="parameters---fieldnumber"></a><span data-ttu-id="996ff-128">パラメーター - fieldNumber</span><span class="sxs-lookup"><span data-stu-id="996ff-128">Parameters - fieldNumber</span></span>

<span data-ttu-id="996ff-129">番号</span><span class="sxs-lookup"><span data-stu-id="996ff-129">number</span></span>  

### <a name="return-value---fieldnumber"></a><span data-ttu-id="996ff-130">戻り値 - fieldNumber</span><span class="sxs-lookup"><span data-stu-id="996ff-130">Return Value - fieldNumber</span></span>

## <a name="method-table"></a><span data-ttu-id="996ff-131">メソッド table</span><span class="sxs-lookup"><span data-stu-id="996ff-131">Method table</span></span>

<span data-ttu-id="996ff-132">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="996ff-132">Gets or sets the table ID that is associated with the object.</span></span>

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a><span data-ttu-id="996ff-133">パラメーター - table</span><span class="sxs-lookup"><span data-stu-id="996ff-133">Parameters - table</span></span>

<span data-ttu-id="996ff-134">値</span><span class="sxs-lookup"><span data-stu-id="996ff-134">value</span></span>  

### <a name="return-value---table"></a><span data-ttu-id="996ff-135">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="996ff-135">Return Value - table</span></span>

<span data-ttu-id="996ff-136">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="996ff-136">The current value of the table ID that is associated with the object.</span></span>

