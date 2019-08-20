---
title: G クラス
description: 文字 G で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 52381
ms.assetid: 6d4b3577-f254-4702-9878-ec3863c033fa
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30525a5e2d44a57c31e57796565e8e4401d68ffe
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833682"
---
# <a name="g-classes"></a><span data-ttu-id="c32e2-103">G クラス</span><span class="sxs-lookup"><span data-stu-id="c32e2-103">G classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c32e2-104">文字 G で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="c32e2-104">System API classes that start with the letter G.</span></span>

<a name="class-gac"></a><span data-ttu-id="c32e2-105">クラス Gac</span><span class="sxs-lookup"><span data-stu-id="c32e2-105">Class Gac</span></span>
---------

    class Gac extends Object

<span data-ttu-id="c32e2-106">Gac クラスを使用すると、グローバル アセンブリ キャッシュ (GAC) のアセンブリを列挙できます。</span><span class="sxs-lookup"><span data-stu-id="c32e2-106">The Gac class lets you enumerate the assemblies of the global assembly cache (GAC).</span></span>

### <a name="remarks"></a><span data-ttu-id="c32e2-107">備考</span><span class="sxs-lookup"><span data-stu-id="c32e2-107">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="c32e2-108">例</span><span class="sxs-lookup"><span data-stu-id="c32e2-108">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="c32e2-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="c32e2-109">Methods</span></span>

| <span data-ttu-id="c32e2-110">方法</span><span class="sxs-lookup"><span data-stu-id="c32e2-110">Method</span></span>                                 | <span data-ttu-id="c32e2-111">説明</span><span class="sxs-lookup"><span data-stu-id="c32e2-111">Description</span></span>                                                   |
|----------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c32e2-112">public container enumerateAssemblies()</span><span class="sxs-lookup"><span data-stu-id="c32e2-112">public container enumerateAssemblies()</span></span> | <span data-ttu-id="c32e2-113">グローバル アセンブリ キャッシュ (GAC) のアセンブリを列挙します。</span><span class="sxs-lookup"><span data-stu-id="c32e2-113">Enumerates the assemblies of the global assembly cache (GAC).</span></span> |
| <span data-ttu-id="c32e2-114">public void new()</span><span class="sxs-lookup"><span data-stu-id="c32e2-114">public void new()</span></span>                      | <span data-ttu-id="c32e2-115">Gac クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c32e2-115">Initializes a new instance of the Gac class.</span></span>                  |

### <a name="method-enumerateassemblies"></a><span data-ttu-id="c32e2-116">メソッド enumerateAssemblies</span><span class="sxs-lookup"><span data-stu-id="c32e2-116">Method enumerateAssemblies</span></span>

<span data-ttu-id="c32e2-117">グローバル アセンブリ キャッシュ (GAC) のアセンブリを列挙します。</span><span class="sxs-lookup"><span data-stu-id="c32e2-117">Enumerates the assemblies of the global assembly cache (GAC).</span></span>

    public container enumerateAssemblies()

#### <a name="return-value"></a><span data-ttu-id="c32e2-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="c32e2-118">Return Value</span></span>

<span data-ttu-id="c32e2-119">GAC のアセンブリを表すコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="c32e2-119">A container that represents the assemblies of the GAC.</span></span>

### <a name="method-new"></a><span data-ttu-id="c32e2-120">メソッド new</span><span class="sxs-lookup"><span data-stu-id="c32e2-120">Method new</span></span>

<span data-ttu-id="c32e2-121">Gac クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c32e2-121">Initializes a new instance of the Gac class.</span></span>

    public void new()



