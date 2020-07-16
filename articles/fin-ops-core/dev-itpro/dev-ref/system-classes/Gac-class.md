---
title: Gac クラス
description: このトピックでは、Gac クラスについて説明します。
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
ms.openlocfilehash: 4bbc2e2d2275299da98d37a47a05282c9247d7c3
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502612"
---
# <a name="class-gac"></a><span data-ttu-id="fa313-103">クラス Gac</span><span class="sxs-lookup"><span data-stu-id="fa313-103">Class Gac</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class Gac extends Object
```

<span data-ttu-id="fa313-104">Gac クラスを使用すると、グローバル アセンブリ キャッシュ (GAC) のアセンブリを列挙できます。</span><span class="sxs-lookup"><span data-stu-id="fa313-104">The Gac class lets you enumerate the assemblies of the global assembly cache (GAC).</span></span>

## <a name="remarks"></a><span data-ttu-id="fa313-105">備考</span><span class="sxs-lookup"><span data-stu-id="fa313-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="fa313-106">例</span><span class="sxs-lookup"><span data-stu-id="fa313-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="fa313-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="fa313-107">Methods</span></span>

| <span data-ttu-id="fa313-108">方法</span><span class="sxs-lookup"><span data-stu-id="fa313-108">Method</span></span>                                 | <span data-ttu-id="fa313-109">説明</span><span class="sxs-lookup"><span data-stu-id="fa313-109">Description</span></span>                                                   |
|----------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="fa313-110">public container enumerateAssemblies()</span><span class="sxs-lookup"><span data-stu-id="fa313-110">public container enumerateAssemblies()</span></span> | <span data-ttu-id="fa313-111">グローバル アセンブリ キャッシュ (GAC) のアセンブリを列挙します。</span><span class="sxs-lookup"><span data-stu-id="fa313-111">Enumerates the assemblies of the global assembly cache (GAC).</span></span> |
| <span data-ttu-id="fa313-112">public void new()</span><span class="sxs-lookup"><span data-stu-id="fa313-112">public void new()</span></span>                      | <span data-ttu-id="fa313-113">Gac クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="fa313-113">Initializes a new instance of the Gac class.</span></span>                  |

## <a name="method-enumerateassemblies"></a><span data-ttu-id="fa313-114">メソッド enumerateAssemblies</span><span class="sxs-lookup"><span data-stu-id="fa313-114">Method enumerateAssemblies</span></span>

<span data-ttu-id="fa313-115">グローバル アセンブリ キャッシュ (GAC) のアセンブリを列挙します。</span><span class="sxs-lookup"><span data-stu-id="fa313-115">Enumerates the assemblies of the global assembly cache (GAC).</span></span>

```xpp
public container enumerateAssemblies()
```

### <a name="return-value---enumerateassemblies"></a><span data-ttu-id="fa313-116">戻り値 - enumerateAssemblies</span><span class="sxs-lookup"><span data-stu-id="fa313-116">Return Value - enumerateAssemblies</span></span>

<span data-ttu-id="fa313-117">GAC のアセンブリを表すコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="fa313-117">A container that represents the assemblies of the GAC.</span></span>

## <a name="method-new"></a><span data-ttu-id="fa313-118">メソッド new</span><span class="sxs-lookup"><span data-stu-id="fa313-118">Method new</span></span>

<span data-ttu-id="fa313-119">Gac クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="fa313-119">Initializes a new instance of the Gac class.</span></span>

```xpp
public void new()
```


