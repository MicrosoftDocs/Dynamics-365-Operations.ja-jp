---
title: PropertiesWindow クラス
description: このトピックでは、PropertiesWindow クラスについて説明します。
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
ms.openlocfilehash: 3ad165eade677843ca000b3bc4dcf85bc80036c2
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502868"
---
# <a name="class-propertieswindow"></a><span data-ttu-id="7d5c0-103">クラス PropertiesWindow</span><span class="sxs-lookup"><span data-stu-id="7d5c0-103">Class PropertiesWindow</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class PropertiesWindow extends Object
```

## <a name="remarks"></a><span data-ttu-id="7d5c0-104">備考</span><span class="sxs-lookup"><span data-stu-id="7d5c0-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="7d5c0-105">例</span><span class="sxs-lookup"><span data-stu-id="7d5c0-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="7d5c0-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="7d5c0-106">Methods</span></span>

| <span data-ttu-id="7d5c0-107">方法</span><span class="sxs-lookup"><span data-stu-id="7d5c0-107">Method</span></span>                                                   | <span data-ttu-id="7d5c0-108">説明</span><span class="sxs-lookup"><span data-stu-id="7d5c0-108">Description</span></span> |
|----------------------------------------------------------|-------------|
| <span data-ttu-id="7d5c0-109">public int Activate(PropWindowDisplayState displaystate)</span><span class="sxs-lookup"><span data-stu-id="7d5c0-109">public int Activate(PropWindowDisplayState displaystate)</span></span> |             |
| <span data-ttu-id="7d5c0-110">public boolean DockFrame(PropWindowDockState dockstate)</span><span class="sxs-lookup"><span data-stu-id="7d5c0-110">public boolean DockFrame(PropWindowDockState dockstate)</span></span>  |             |
| <span data-ttu-id="7d5c0-111">public str GetSelectedPropertyName()</span><span class="sxs-lookup"><span data-stu-id="7d5c0-111">public str GetSelectedPropertyName()</span></span>                     |             |
| <span data-ttu-id="7d5c0-112">public boolean IsVisible()</span><span class="sxs-lookup"><span data-stu-id="7d5c0-112">public boolean IsVisible()</span></span>                               |             |
| <span data-ttu-id="7d5c0-113">public boolean SelectPropertyByName(str propname)</span><span class="sxs-lookup"><span data-stu-id="7d5c0-113">public boolean SelectPropertyByName(str propname)</span></span>        |             |
| <span data-ttu-id="7d5c0-114">public boolean SelectTab(PropWindowSelectTab selecttab)</span><span class="sxs-lookup"><span data-stu-id="7d5c0-114">public boolean SelectTab(PropWindowSelectTab selecttab)</span></span>  |             |

## <a name="method-activate"></a><span data-ttu-id="7d5c0-115">メソッド Activate</span><span class="sxs-lookup"><span data-stu-id="7d5c0-115">Method Activate</span></span>

```xpp
public int Activate(PropWindowDisplayState displaystate)
```

### <a name="parameters---activate"></a><span data-ttu-id="7d5c0-116">パラメーター - Activate</span><span class="sxs-lookup"><span data-stu-id="7d5c0-116">Parameters - Activate</span></span>

<span data-ttu-id="7d5c0-117">displaystate</span><span class="sxs-lookup"><span data-stu-id="7d5c0-117">displaystate</span></span>  

### <a name="return-value---activate"></a><span data-ttu-id="7d5c0-118">戻り値 - Activate</span><span class="sxs-lookup"><span data-stu-id="7d5c0-118">Return Value - Activate</span></span>

## <a name="method-dockframe"></a><span data-ttu-id="7d5c0-119">メソッド DockFrame</span><span class="sxs-lookup"><span data-stu-id="7d5c0-119">Method DockFrame</span></span>

```xpp
public boolean DockFrame(PropWindowDockState dockstate)
```

### <a name="parameters---dockframe"></a><span data-ttu-id="7d5c0-120">パラメーター - DockFrame</span><span class="sxs-lookup"><span data-stu-id="7d5c0-120">Parameters - DockFrame</span></span>

<span data-ttu-id="7d5c0-121">dockstate</span><span class="sxs-lookup"><span data-stu-id="7d5c0-121">dockstate</span></span>  

### <a name="return-value---dockframe"></a><span data-ttu-id="7d5c0-122">戻り値 - DockFrame</span><span class="sxs-lookup"><span data-stu-id="7d5c0-122">Return Value - DockFrame</span></span>

## <a name="method-getselectedpropertyname"></a><span data-ttu-id="7d5c0-123">メソッド GetSelectedPropertyName</span><span class="sxs-lookup"><span data-stu-id="7d5c0-123">Method GetSelectedPropertyName</span></span>

```xpp
public str GetSelectedPropertyName()
```

### <a name="return-value---getselectedpropertyname"></a><span data-ttu-id="7d5c0-124">戻り値 - GetSelectedPropertyName</span><span class="sxs-lookup"><span data-stu-id="7d5c0-124">Return Value - GetSelectedPropertyName</span></span>

## <a name="method-isvisible"></a><span data-ttu-id="7d5c0-125">メソッド IsVisible</span><span class="sxs-lookup"><span data-stu-id="7d5c0-125">Method IsVisible</span></span>

```xpp
public boolean IsVisible()
```

### <a name="return-value---isvisible"></a><span data-ttu-id="7d5c0-126">戻り値 - IsVisible</span><span class="sxs-lookup"><span data-stu-id="7d5c0-126">Return Value - IsVisible</span></span>

## <a name="method-selectpropertybyname"></a><span data-ttu-id="7d5c0-127">メソッド SelectPropertyByName</span><span class="sxs-lookup"><span data-stu-id="7d5c0-127">Method SelectPropertyByName</span></span>

```xpp
public boolean SelectPropertyByName(str propname)
```

### <a name="parameters---selectpropertybyname"></a><span data-ttu-id="7d5c0-128">パラメーター - SelectPropertyByName</span><span class="sxs-lookup"><span data-stu-id="7d5c0-128">Parameters - SelectPropertyByName</span></span>

<span data-ttu-id="7d5c0-129">propname</span><span class="sxs-lookup"><span data-stu-id="7d5c0-129">propname</span></span>  

### <a name="return-value---selectpropertybyname"></a><span data-ttu-id="7d5c0-130">戻り値 - SelectPropertyByName</span><span class="sxs-lookup"><span data-stu-id="7d5c0-130">Return Value - SelectPropertyByName</span></span>

## <a name="method-selecttab"></a><span data-ttu-id="7d5c0-131">メソッド SelectTab</span><span class="sxs-lookup"><span data-stu-id="7d5c0-131">Method SelectTab</span></span>

```xpp
public boolean SelectTab(PropWindowSelectTab selecttab)
```

### <a name="parameters---selecttab"></a><span data-ttu-id="7d5c0-132">パラメーター - SelectTab</span><span class="sxs-lookup"><span data-stu-id="7d5c0-132">Parameters - SelectTab</span></span>

<span data-ttu-id="7d5c0-133">selecttab</span><span class="sxs-lookup"><span data-stu-id="7d5c0-133">selecttab</span></span>  

### <a name="return-value---selecttab"></a><span data-ttu-id="7d5c0-134">戻り値 - SelectTab</span><span class="sxs-lookup"><span data-stu-id="7d5c0-134">Return Value - SelectTab</span></span>


