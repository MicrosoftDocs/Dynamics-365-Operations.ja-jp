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
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 52381
ms.assetid: 6d4b3577-f254-4702-9878-ec3863c033fa
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68bb58cea4ef68c09668f36270290180b528b83e
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537034"
---
# <a name="g-classes"></a><span data-ttu-id="12645-103">G クラス</span><span class="sxs-lookup"><span data-stu-id="12645-103">G classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12645-104">文字 G で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="12645-104">System API classes that start with the letter G.</span></span>

<a name="class-gac"></a><span data-ttu-id="12645-105">クラス Gac</span><span class="sxs-lookup"><span data-stu-id="12645-105">Class Gac</span></span>
---------

    class Gac extends Object

<span data-ttu-id="12645-106">Gac クラスを使用すると、グローバル アセンブリ キャッシュ (GAC) のアセンブリを列挙できます。</span><span class="sxs-lookup"><span data-stu-id="12645-106">The Gac class lets you enumerate the assemblies of the global assembly cache (GAC).</span></span>

### <a name="remarks"></a><span data-ttu-id="12645-107">備考</span><span class="sxs-lookup"><span data-stu-id="12645-107">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="12645-108">例</span><span class="sxs-lookup"><span data-stu-id="12645-108">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="12645-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="12645-109">Methods</span></span>

| <span data-ttu-id="12645-110">方法</span><span class="sxs-lookup"><span data-stu-id="12645-110">Method</span></span>                                 | <span data-ttu-id="12645-111">説明</span><span class="sxs-lookup"><span data-stu-id="12645-111">Description</span></span>                                                   |
|----------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="12645-112">public container enumerateAssemblies()</span><span class="sxs-lookup"><span data-stu-id="12645-112">public container enumerateAssemblies()</span></span> | <span data-ttu-id="12645-113">グローバル アセンブリ キャッシュ (GAC) のアセンブリを列挙します。</span><span class="sxs-lookup"><span data-stu-id="12645-113">Enumerates the assemblies of the global assembly cache (GAC).</span></span> |
| <span data-ttu-id="12645-114">public void new()</span><span class="sxs-lookup"><span data-stu-id="12645-114">public void new()</span></span>                      | <span data-ttu-id="12645-115">Gac クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="12645-115">Initializes a new instance of the Gac class.</span></span>                  |

### <a name="method-enumerateassemblies"></a><span data-ttu-id="12645-116">メソッド enumerateAssemblies</span><span class="sxs-lookup"><span data-stu-id="12645-116">Method enumerateAssemblies</span></span>

<span data-ttu-id="12645-117">グローバル アセンブリ キャッシュ (GAC) のアセンブリを列挙します。</span><span class="sxs-lookup"><span data-stu-id="12645-117">Enumerates the assemblies of the global assembly cache (GAC).</span></span>

    public container enumerateAssemblies()

#### <a name="return-value"></a><span data-ttu-id="12645-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="12645-118">Return Value</span></span>

<span data-ttu-id="12645-119">GAC のアセンブリを表すコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="12645-119">A container that represents the assemblies of the GAC.</span></span>

### <a name="method-new"></a><span data-ttu-id="12645-120">メソッド new</span><span class="sxs-lookup"><span data-stu-id="12645-120">Method new</span></span>

<span data-ttu-id="12645-121">Gac クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="12645-121">Initializes a new instance of the Gac class.</span></span>

    public void new()



