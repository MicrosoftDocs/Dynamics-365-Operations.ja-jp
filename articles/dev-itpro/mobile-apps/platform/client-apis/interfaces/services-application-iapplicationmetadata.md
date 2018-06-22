---
title: ApplicationMetadata
description: "アプリケーションの宣言メタデータを表します"
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: 
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: bc18e9033792441bd11cfdf0c7c968c0edebbf1a
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="applicationmetadata-type"></a><span data-ttu-id="81a02-103">ApplicationMetadata タイプ</span><span class="sxs-lookup"><span data-stu-id="81a02-103">ApplicationMetadata Type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="81a02-104">アプリケーションの宣言メタデータを表します</span><span class="sxs-lookup"><span data-stu-id="81a02-104">Represents the declarative metadata of an application</span></span>

### <a name="hierarchy"></a><span data-ttu-id="81a02-105">階層</span><span class="sxs-lookup"><span data-stu-id="81a02-105">Hierarchy</span></span>

<span data-ttu-id="81a02-106">ApplicationMetadata</span><span class="sxs-lookup"><span data-stu-id="81a02-106">ApplicationMetadata</span></span> <br>

## <a name="index"></a><span data-ttu-id="81a02-107">指数</span><span class="sxs-lookup"><span data-stu-id="81a02-107">Index</span></span>

### <a name="properties"></a><span data-ttu-id="81a02-108">プロパティ</span><span class="sxs-lookup"><span data-stu-id="81a02-108">Properties</span></span>

* [<span data-ttu-id="81a02-109">ColorName</span><span class="sxs-lookup"><span data-stu-id="81a02-109">ColorName</span></span>](services-application-iapplicationmetadata.md#colorname)
* [<span data-ttu-id="81a02-110">Configs</span><span class="sxs-lookup"><span data-stu-id="81a02-110">Configs</span></span>](services-application-iapplicationmetadata.md#configs)
* [<span data-ttu-id="81a02-111">説明</span><span class="sxs-lookup"><span data-stu-id="81a02-111">Description</span></span>](services-application-iapplicationmetadata.md#description)
* [<span data-ttu-id="81a02-112">IconName</span><span class="sxs-lookup"><span data-stu-id="81a02-112">IconName</span></span>](services-application-iapplicationmetadata.md#iconname)
* [<span data-ttu-id="81a02-113">ID</span><span class="sxs-lookup"><span data-stu-id="81a02-113">Id</span></span>](services-application-iapplicationmetadata.md#id)
* [<span data-ttu-id="81a02-114">タイトル</span><span class="sxs-lookup"><span data-stu-id="81a02-114">Title</span></span>](services-application-iapplicationmetadata.md#title)

## <a name="properties"></a><span data-ttu-id="81a02-115">プロパティ</span><span class="sxs-lookup"><span data-stu-id="81a02-115">Properties</span></span>

### <a name="colorname"></a><span data-ttu-id="81a02-116">ColorName</span><span class="sxs-lookup"><span data-stu-id="81a02-116">ColorName</span></span>

<span data-ttu-id="81a02-117">ColorName: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="81a02-117">ColorName: string (optional)</span></span> 

<span data-ttu-id="81a02-118">アプリケーションのテーマ色。</span><span class="sxs-lookup"><span data-stu-id="81a02-118">The theme color of the application</span></span>


### <a name="configs"></a><span data-ttu-id="81a02-119">Configs</span><span class="sxs-lookup"><span data-stu-id="81a02-119">Configs</span></span>

<span data-ttu-id="81a02-120">Configs: [名前: 文字列]: 任意 (オプション)</span><span class="sxs-lookup"><span data-stu-id="81a02-120">Configs: [name: string]: any (optional)</span></span> 

<span data-ttu-id="81a02-121">アプリケーションは作成者またはリソース プロバイダーにより指定された名前付き構成のセットを持つことができます</span><span class="sxs-lookup"><span data-stu-id="81a02-121">An application can have a set of named config supplied by the author or the resource provider</span></span>


### <a name="description"></a><span data-ttu-id="81a02-122">説明</span><span class="sxs-lookup"><span data-stu-id="81a02-122">Description</span></span>

<span data-ttu-id="81a02-123">説明:文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="81a02-123">Description: string (optional)</span></span> 

<span data-ttu-id="81a02-124">アプリケーションの説明</span><span class="sxs-lookup"><span data-stu-id="81a02-124">The description of the application</span></span>


### <a name="iconname"></a><span data-ttu-id="81a02-125">IconName</span><span class="sxs-lookup"><span data-stu-id="81a02-125">IconName</span></span>

<span data-ttu-id="81a02-126">IconName: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="81a02-126">IconName: string (optional)</span></span> 

<span data-ttu-id="81a02-127">アプリケーションの代表的なアイコン</span><span class="sxs-lookup"><span data-stu-id="81a02-127">The representative icon of the application</span></span>


### <a name="id"></a><span data-ttu-id="81a02-128">ID</span><span class="sxs-lookup"><span data-stu-id="81a02-128">Id</span></span>

<span data-ttu-id="81a02-129">Id: 文字列</span><span class="sxs-lookup"><span data-stu-id="81a02-129">Id: string</span></span>

<span data-ttu-id="81a02-130">アプリケーションの一意の識別子</span><span class="sxs-lookup"><span data-stu-id="81a02-130">The unique identifier of the application</span></span>


### <a name="title"></a><span data-ttu-id="81a02-131">肩書き</span><span class="sxs-lookup"><span data-stu-id="81a02-131">Title</span></span>

<span data-ttu-id="81a02-132">タイトル: 文字列</span><span class="sxs-lookup"><span data-stu-id="81a02-132">Title: string</span></span>

<span data-ttu-id="81a02-133">アプリケーションのタイトル。</span><span class="sxs-lookup"><span data-stu-id="81a02-133">The title of the application</span></span>



