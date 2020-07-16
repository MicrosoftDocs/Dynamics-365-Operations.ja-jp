---
title: DataSourceRuntimeMetadataChangedEvtArgs クラス
description: このトピックでは、DataSourceRuntimeMetadataChangedEvtArgs クラスについて説明します。
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
ms.openlocfilehash: e26a3b799530d73eb6b958a56116c4fe3efa6a1e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502731"
---
# <a name="class-datasourceruntimemetadatachangedevtargs"></a><span data-ttu-id="8c855-103">クラス DataSourceRuntimeMetadataChangedEvtArgs</span><span class="sxs-lookup"><span data-stu-id="8c855-103">Class DataSourceRuntimeMetadataChangedEvtArgs</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DataSourceRuntimeMetadataChangedEvtArgs extends ManagedEventArgs
```

## <a name="remarks"></a><span data-ttu-id="8c855-104">備考</span><span class="sxs-lookup"><span data-stu-id="8c855-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="8c855-105">例</span><span class="sxs-lookup"><span data-stu-id="8c855-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="8c855-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="8c855-106">Methods</span></span>

| <span data-ttu-id="8c855-107">方法</span><span class="sxs-lookup"><span data-stu-id="8c855-107">Method</span></span>                                                                                                                                    | <span data-ttu-id="8c855-108">説明</span><span class="sxs-lookup"><span data-stu-id="8c855-108">Description</span></span>                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8c855-109">public str changedDataSourceName()</span><span class="sxs-lookup"><span data-stu-id="8c855-109">public str changedDataSourceName()</span></span>                                                                                                        |                                                           |
| <span data-ttu-id="8c855-110">public FieldId changedFieldId()</span><span class="sxs-lookup"><span data-stu-id="8c855-110">public FieldId changedFieldId()</span></span>                                                                                                           |                                                           |
| <span data-ttu-id="8c855-111">public DataSourceMetadataChangeType changeType()</span><span class="sxs-lookup"><span data-stu-id="8c855-111">public DataSourceMetadataChangeType changeType()</span></span>                                                                                          |                                                           |
| <span data-ttu-id="8c855-112">public str referencedDataSourceName()</span><span class="sxs-lookup"><span data-stu-id="8c855-112">public str referencedDataSourceName()</span></span>                                                                                                     |                                                           |
| <span data-ttu-id="8c855-113">public void new(str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType)</span><span class="sxs-lookup"><span data-stu-id="8c855-113">public void new(str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType)</span></span> | <span data-ttu-id="8c855-114">ManagedEventArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="8c855-114">Initializes a new instance of the ManagedEventArgs class.</span></span> |
| <span data-ttu-id="8c855-115">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="8c855-115">public void finalize()</span></span>                                                                                                                    |                                                           |

## <a name="method-changeddatasourcename"></a><span data-ttu-id="8c855-116">メソッド changedDataSourceName</span><span class="sxs-lookup"><span data-stu-id="8c855-116">Method changedDataSourceName</span></span>

```xpp
public str changedDataSourceName()
```

### <a name="return-value---changeddatasourcename"></a><span data-ttu-id="8c855-117">戻り値 - changedDataSourceName</span><span class="sxs-lookup"><span data-stu-id="8c855-117">Return Value - changedDataSourceName</span></span>

## <a name="method-changedfieldid"></a><span data-ttu-id="8c855-118">メソッド changedFieldId</span><span class="sxs-lookup"><span data-stu-id="8c855-118">Method changedFieldId</span></span>

```xpp
public FieldId changedFieldId()
```

### <a name="return-value---changedfieldid"></a><span data-ttu-id="8c855-119">戻り値 - changedFieldId</span><span class="sxs-lookup"><span data-stu-id="8c855-119">Return Value - changedFieldId</span></span>

## <a name="method-changetype"></a><span data-ttu-id="8c855-120">メソッド changeType</span><span class="sxs-lookup"><span data-stu-id="8c855-120">Method changeType</span></span>

```xpp
public DataSourceMetadataChangeType changeType()
```

### <a name="return-value---changetype"></a><span data-ttu-id="8c855-121">戻り値 - changeType</span><span class="sxs-lookup"><span data-stu-id="8c855-121">Return Value - changeType</span></span>

## <a name="method-referenceddatasourcename"></a><span data-ttu-id="8c855-122">メソッド referencedDataSourceName</span><span class="sxs-lookup"><span data-stu-id="8c855-122">Method referencedDataSourceName</span></span>

```xpp
public str referencedDataSourceName()
```

### <a name="return-value---referenceddatasourcename"></a><span data-ttu-id="8c855-123">戻り値 - referencedDataSourceName</span><span class="sxs-lookup"><span data-stu-id="8c855-123">Return Value - referencedDataSourceName</span></span>

## <a name="method-new"></a><span data-ttu-id="8c855-124">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8c855-124">Method new</span></span>

<span data-ttu-id="8c855-125">ManagedEventArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="8c855-125">Initializes a new instance of the ManagedEventArgs class.</span></span>

```xpp
public void new(str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType)
```

### <a name="parameters---new"></a><span data-ttu-id="8c855-126">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="8c855-126">Parameters - new</span></span>

<span data-ttu-id="8c855-127">changedDatasourceName</span><span class="sxs-lookup"><span data-stu-id="8c855-127">changedDatasourceName</span></span>  

<!-- -->

<span data-ttu-id="8c855-128">referencedDatasourceName</span><span class="sxs-lookup"><span data-stu-id="8c855-128">referencedDatasourceName</span></span>  

<!-- -->

<span data-ttu-id="8c855-129">changedFieldId</span><span class="sxs-lookup"><span data-stu-id="8c855-129">changedFieldId</span></span>  

<!-- -->

<span data-ttu-id="8c855-130">changeType</span><span class="sxs-lookup"><span data-stu-id="8c855-130">changeType</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="8c855-131">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="8c855-131">Method finalize</span></span>

```xpp
public void finalize()
```

