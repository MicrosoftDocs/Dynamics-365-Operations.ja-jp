---
title: NavigationArgs タイプ
description: NavigationArgs タイプ
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: ''
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: b1e38920b7a3d529eebfd5b5039591aaaf88a79d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547343"
---
# <a name="navigationargs-type"></a><span data-ttu-id="25ed0-103">NavigationArgs タイプ</span><span class="sxs-lookup"><span data-stu-id="25ed0-103">NavigationArgs type</span></span>

[!include [banner](../../../../includes/banner.md)]

### <a name="hierarchy"></a><span data-ttu-id="25ed0-104">階層</span><span class="sxs-lookup"><span data-stu-id="25ed0-104">Hierarchy</span></span>

[<span data-ttu-id="25ed0-105">PageTarget</span><span class="sxs-lookup"><span data-stu-id="25ed0-105">PageTarget</span></span>](view-model-ipage-ipagetarget.md) <br><span data-ttu-id="25ed0-106">&nbsp;&nbsp;&nbsp;└─ NavigationArgs</span><span class="sxs-lookup"><span data-stu-id="25ed0-106">&nbsp;&nbsp;&nbsp;└─ NavigationArgs</span></span> <br>

## <a name="index"></a><span data-ttu-id="25ed0-107">指数</span><span class="sxs-lookup"><span data-stu-id="25ed0-107">Index</span></span>

### <a name="properties"></a><span data-ttu-id="25ed0-108">プロパティ</span><span class="sxs-lookup"><span data-stu-id="25ed0-108">Properties</span></span>

* [<span data-ttu-id="25ed0-109">ラベル</span><span class="sxs-lookup"><span data-stu-id="25ed0-109">label</span></span>](view-model-ipage-inavigationargs.md#label)
* [<span data-ttu-id="25ed0-110">オプション</span><span class="sxs-lookup"><span data-stu-id="25ed0-110">options</span></span>](view-model-ipage-inavigationargs.md#options)
* [<span data-ttu-id="25ed0-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="25ed0-111">params</span></span>](view-model-ipage-inavigationargs.md#params)
* [<span data-ttu-id="25ed0-112">置換</span><span class="sxs-lookup"><span data-stu-id="25ed0-112">replace</span></span>](view-model-ipage-inavigationargs.md#replace)
* [<span data-ttu-id="25ed0-113">to</span><span class="sxs-lookup"><span data-stu-id="25ed0-113">to</span></span>](view-model-ipage-inavigationargs.md#to)
* [<span data-ttu-id="25ed0-114">url</span><span class="sxs-lookup"><span data-stu-id="25ed0-114">url</span></span>](view-model-ipage-inavigationargs.md#url)

## <a name="properties"></a><span data-ttu-id="25ed0-115">プロパティ</span><span class="sxs-lookup"><span data-stu-id="25ed0-115">Properties</span></span>

### <a name="label"></a><span data-ttu-id="25ed0-116">ラベル</span><span class="sxs-lookup"><span data-stu-id="25ed0-116">label</span></span>

<span data-ttu-id="25ed0-117">label: string (省略可)</span><span class="sxs-lookup"><span data-stu-id="25ed0-117">label: string (optional)</span></span> 




### <a name="options"></a><span data-ttu-id="25ed0-118">オプション</span><span class="sxs-lookup"><span data-stu-id="25ed0-118">options</span></span>

<span data-ttu-id="25ed0-119">options: any (省略可)</span><span class="sxs-lookup"><span data-stu-id="25ed0-119">options: any (optional)</span></span> 




### <a name="params"></a><span data-ttu-id="25ed0-120">params</span><span class="sxs-lookup"><span data-stu-id="25ed0-120">params</span></span>

<span data-ttu-id="25ed0-121">params: [PageOptions](view-model-ipage-ipageoptions.md) (省略可)</span><span class="sxs-lookup"><span data-stu-id="25ed0-121">params: [PageOptions](view-model-ipage-ipageoptions.md) (optional)</span></span> 



> <span data-ttu-id="25ed0-122">[PageTarget](view-model-ipage-ipagetarget.md).[params](view-model-ipage-ipagetarget.md#params) から継承</span><span class="sxs-lookup"><span data-stu-id="25ed0-122">Inherited from [PageTarget](view-model-ipage-ipagetarget.md).[params](view-model-ipage-ipagetarget.md#params)</span></span>


### <a name="replace"></a><span data-ttu-id="25ed0-123">置換</span><span class="sxs-lookup"><span data-stu-id="25ed0-123">replace</span></span>

<span data-ttu-id="25ed0-124">replace: boolean (省略可)</span><span class="sxs-lookup"><span data-stu-id="25ed0-124">replace: boolean (optional)</span></span> 

<span data-ttu-id="25ed0-125">true と設定されている場合は、ナビゲーション履歴スタックから現在のビューの起動ナビゲーションを削除します。</span><span class="sxs-lookup"><span data-stu-id="25ed0-125">If set to true, removes current view firing navigation from navigation history stack.</span></span>


### <a name="to"></a><span data-ttu-id="25ed0-126">終了</span><span class="sxs-lookup"><span data-stu-id="25ed0-126">to</span></span>

<span data-ttu-id="25ed0-127">to: string (省略可)</span><span class="sxs-lookup"><span data-stu-id="25ed0-127">to: string (optional)</span></span> 



> <span data-ttu-id="25ed0-128">[PageTarget](view-model-ipage-ipagetarget.md).[to](view-model-ipage-ipagetarget.md#to) から継承</span><span class="sxs-lookup"><span data-stu-id="25ed0-128">Inherited from [PageTarget](view-model-ipage-ipagetarget.md).[to](view-model-ipage-ipagetarget.md#to)</span></span>


### <a name="url"></a><span data-ttu-id="25ed0-129">URL</span><span class="sxs-lookup"><span data-stu-id="25ed0-129">url</span></span>

<span data-ttu-id="25ed0-130">url: string (省略可)</span><span class="sxs-lookup"><span data-stu-id="25ed0-130">url: string (optional)</span></span> 

<span data-ttu-id="25ed0-131">指定した場合、このリンクは直接開かれます。</span><span class="sxs-lookup"><span data-stu-id="25ed0-131">If provided, this link is directly opened.</span></span>


