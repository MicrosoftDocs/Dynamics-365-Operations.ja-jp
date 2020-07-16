---
title: OleCommand クラス
description: このトピックでは、OleCommand クラスについて説明します。
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
ms.openlocfilehash: 3b840512bd497132a1022658f45a72c0d61356ca
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502561"
---
# <a name="class-olecommand"></a><span data-ttu-id="f8389-103">クラス OleCommand</span><span class="sxs-lookup"><span data-stu-id="f8389-103">Class OleCommand</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class OleCommand extends Object
```

## <a name="remarks"></a><span data-ttu-id="f8389-104">備考</span><span class="sxs-lookup"><span data-stu-id="f8389-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="f8389-105">例</span><span class="sxs-lookup"><span data-stu-id="f8389-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="f8389-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="f8389-106">Methods</span></span>

| <span data-ttu-id="f8389-107">方法</span><span class="sxs-lookup"><span data-stu-id="f8389-107">Method</span></span>                                                                              | <span data-ttu-id="f8389-108">説明</span><span class="sxs-lookup"><span data-stu-id="f8389-108">Description</span></span>                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="f8389-109">public COMVariant exec(str cmdGroup, int cmdId, int cmdExecOption, COMVariant parm)</span><span class="sxs-lookup"><span data-stu-id="f8389-109">public COMVariant exec(str cmdGroup, int cmdId, int cmdExecOption, COMVariant parm)</span></span> |                                                 |
| <span data-ttu-id="f8389-110">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="f8389-110">public void finalize()</span></span>                                                              |                                                 |
| <span data-ttu-id="f8389-111">public void new(ComInterface comObject)</span><span class="sxs-lookup"><span data-stu-id="f8389-111">public void new(ComInterface comObject)</span></span>                                             | <span data-ttu-id="f8389-112">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f8389-112">Initializes a new instance of the Object class.</span></span> |

## <a name="method-exec"></a><span data-ttu-id="f8389-113">メソッド exec</span><span class="sxs-lookup"><span data-stu-id="f8389-113">Method exec</span></span>

```xpp
public COMVariant exec(str cmdGroup, int cmdId, int cmdExecOption, COMVariant parm)
```

### <a name="parameters---exec"></a><span data-ttu-id="f8389-114">パラメーター - exec</span><span class="sxs-lookup"><span data-stu-id="f8389-114">Parameters - exec</span></span>

<span data-ttu-id="f8389-115">cmdGroup</span><span class="sxs-lookup"><span data-stu-id="f8389-115">cmdGroup</span></span>  

<!-- -->

<span data-ttu-id="f8389-116">cmdId</span><span class="sxs-lookup"><span data-stu-id="f8389-116">cmdId</span></span>  

<!-- -->

<span data-ttu-id="f8389-117">cmdExecOption</span><span class="sxs-lookup"><span data-stu-id="f8389-117">cmdExecOption</span></span>  

<!-- -->

<span data-ttu-id="f8389-118">parm</span><span class="sxs-lookup"><span data-stu-id="f8389-118">parm</span></span>  

### <a name="return-value---exec"></a><span data-ttu-id="f8389-119">戻り値 - exec</span><span class="sxs-lookup"><span data-stu-id="f8389-119">Return Value - exec</span></span>

## <a name="method-finalize"></a><span data-ttu-id="f8389-120">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="f8389-120">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-new"></a><span data-ttu-id="f8389-121">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f8389-121">Method new</span></span>

<span data-ttu-id="f8389-122">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f8389-122">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(ComInterface comObject)
```

### <a name="parameters---new"></a><span data-ttu-id="f8389-123">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="f8389-123">Parameters - new</span></span>

<span data-ttu-id="f8389-124">comObject</span><span class="sxs-lookup"><span data-stu-id="f8389-124">comObject</span></span>  

