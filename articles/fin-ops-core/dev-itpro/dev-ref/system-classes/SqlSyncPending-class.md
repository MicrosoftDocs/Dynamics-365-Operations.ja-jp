---
title: SqlSyncPending クラス
description: このトピックでは、SqlSyncPending クラスについて説明します。
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
ms.openlocfilehash: 7e19820aaf415e27f1c6da0440df3691e237b624
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502798"
---
# <a name="class-sqlsyncpending"></a><span data-ttu-id="d51a2-103">クラス SqlSyncPending</span><span class="sxs-lookup"><span data-stu-id="d51a2-103">Class SqlSyncPending</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SqlSyncPending extends Object
```

## <a name="remarks"></a><span data-ttu-id="d51a2-104">備考</span><span class="sxs-lookup"><span data-stu-id="d51a2-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="d51a2-105">例</span><span class="sxs-lookup"><span data-stu-id="d51a2-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="d51a2-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="d51a2-106">Methods</span></span>

| <span data-ttu-id="d51a2-107">方法</span><span class="sxs-lookup"><span data-stu-id="d51a2-107">Method</span></span>                                               | <span data-ttu-id="d51a2-108">説明</span><span class="sxs-lookup"><span data-stu-id="d51a2-108">Description</span></span>                                             |
|------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d51a2-109">public ConfigurationKeyId configurationKeyTouched()</span><span class="sxs-lookup"><span data-stu-id="d51a2-109">public ConfigurationKeyId configurationKeyTouched()</span></span>  |                                                         |
| <span data-ttu-id="d51a2-110">public boolean databaseTouched(\[boolean newValue\])</span><span class="sxs-lookup"><span data-stu-id="d51a2-110">public boolean databaseTouched(\[boolean newValue\])</span></span> |                                                         |
| <span data-ttu-id="d51a2-111">public ExtendedTypeId extendedDataTypeTouched()</span><span class="sxs-lookup"><span data-stu-id="d51a2-111">public ExtendedTypeId extendedDataTypeTouched()</span></span>      |                                                         |
| <span data-ttu-id="d51a2-112">public TableId indexesTouched()</span><span class="sxs-lookup"><span data-stu-id="d51a2-112">public TableId indexesTouched()</span></span>                      |                                                         |
| <span data-ttu-id="d51a2-113">public TableId relationTouched()</span><span class="sxs-lookup"><span data-stu-id="d51a2-113">public TableId relationTouched()</span></span>                     |                                                         |
| <span data-ttu-id="d51a2-114">public TableId tableDeleted()</span><span class="sxs-lookup"><span data-stu-id="d51a2-114">public TableId tableDeleted()</span></span>                        |                                                         |
| <span data-ttu-id="d51a2-115">public TableId tableTouched()</span><span class="sxs-lookup"><span data-stu-id="d51a2-115">public TableId tableTouched()</span></span>                        |                                                         |
| <span data-ttu-id="d51a2-116">public void new()</span><span class="sxs-lookup"><span data-stu-id="d51a2-116">public void new()</span></span>                                    | <span data-ttu-id="d51a2-117">SqlSyncPending クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d51a2-117">Initializes a new instance of the SqlSyncPending class.</span></span> |

## <a name="method-configurationkeytouched"></a><span data-ttu-id="d51a2-118">メソッド configurationKeyTouched</span><span class="sxs-lookup"><span data-stu-id="d51a2-118">Method configurationKeyTouched</span></span>

```xpp
public ConfigurationKeyId configurationKeyTouched()
```

### <a name="return-value---configurationkeytouched"></a><span data-ttu-id="d51a2-119">戻り値 - configurationKeyTouched</span><span class="sxs-lookup"><span data-stu-id="d51a2-119">Return Value - configurationKeyTouched</span></span>

## <a name="method-databasetouched"></a><span data-ttu-id="d51a2-120">メソッド databaseTouched</span><span class="sxs-lookup"><span data-stu-id="d51a2-120">Method databaseTouched</span></span>

```xpp
public boolean databaseTouched([boolean newValue])
```

### <a name="parameters---databasetouched"></a><span data-ttu-id="d51a2-121">パラメーター - databaseTouched</span><span class="sxs-lookup"><span data-stu-id="d51a2-121">Parameters - databaseTouched</span></span>

<span data-ttu-id="d51a2-122">newValue</span><span class="sxs-lookup"><span data-stu-id="d51a2-122">newValue</span></span>  

### <a name="return-value---databasetouched"></a><span data-ttu-id="d51a2-123">戻り値 - databaseTouched</span><span class="sxs-lookup"><span data-stu-id="d51a2-123">Return Value - databaseTouched</span></span>

## <a name="method-extendeddatatypetouched"></a><span data-ttu-id="d51a2-124">メソッド extendedDataTypeTouched</span><span class="sxs-lookup"><span data-stu-id="d51a2-124">Method extendedDataTypeTouched</span></span>

```xpp
public ExtendedTypeId extendedDataTypeTouched()
```

### <a name="return-value---extendeddatatypetouched"></a><span data-ttu-id="d51a2-125">戻り値 - extendedDataTypeTouched</span><span class="sxs-lookup"><span data-stu-id="d51a2-125">Return Value - extendedDataTypeTouched</span></span>

## <a name="method-indexestouched"></a><span data-ttu-id="d51a2-126">メソッド indexesTouched</span><span class="sxs-lookup"><span data-stu-id="d51a2-126">Method indexesTouched</span></span>

```xpp
public TableId indexesTouched()
```

### <a name="return-value---indexestouched"></a><span data-ttu-id="d51a2-127">戻り値 - indexesTouched</span><span class="sxs-lookup"><span data-stu-id="d51a2-127">Return Value - indexesTouched</span></span>

## <a name="method-relationtouched"></a><span data-ttu-id="d51a2-128">メソッド relationTouched</span><span class="sxs-lookup"><span data-stu-id="d51a2-128">Method relationTouched</span></span>

```xpp
public TableId relationTouched()
```

### <a name="return-value---relationtouched"></a><span data-ttu-id="d51a2-129">戻り値 - relationTouched</span><span class="sxs-lookup"><span data-stu-id="d51a2-129">Return Value - relationTouched</span></span>

## <a name="method-tabledeleted"></a><span data-ttu-id="d51a2-130">メソッド tableDeleted</span><span class="sxs-lookup"><span data-stu-id="d51a2-130">Method tableDeleted</span></span>

```xpp
public TableId tableDeleted()
```

### <a name="return-value---tabledeleted"></a><span data-ttu-id="d51a2-131">戻り値 - tableDeleted</span><span class="sxs-lookup"><span data-stu-id="d51a2-131">Return Value - tableDeleted</span></span>

## <a name="method-tabletouched"></a><span data-ttu-id="d51a2-132">メソッド tableTouched</span><span class="sxs-lookup"><span data-stu-id="d51a2-132">Method tableTouched</span></span>

```xpp
public TableId tableTouched()
```

### <a name="return-value---tabletouched"></a><span data-ttu-id="d51a2-133">戻り値 - tableTouched</span><span class="sxs-lookup"><span data-stu-id="d51a2-133">Return Value - tableTouched</span></span>

## <a name="method-new"></a><span data-ttu-id="d51a2-134">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d51a2-134">Method new</span></span>

<span data-ttu-id="d51a2-135">SqlSyncPending クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d51a2-135">Initializes a new instance of the SqlSyncPending class.</span></span>

```xpp
public void new()
```

