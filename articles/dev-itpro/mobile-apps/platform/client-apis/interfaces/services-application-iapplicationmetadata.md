---
title: "ApplicationMetadata タイプ"
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
ms.sourcegitcommit: ed6cabcc8c76fba3d4414cd4b564b720c54169e0
ms.openlocfilehash: 3d38b632298ccb4457c6a741f3d42777f2aa8306
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="applicationmetadata-type"></a><span data-ttu-id="5df07-103">ApplicationMetadata タイプ</span><span class="sxs-lookup"><span data-stu-id="5df07-103">ApplicationMetadata type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="5df07-104">アプリケーションの宣言メタデータを表します</span><span class="sxs-lookup"><span data-stu-id="5df07-104">Represents the declarative metadata of an application</span></span>

### <a name="hierarchy"></a><span data-ttu-id="5df07-105">階層</span><span class="sxs-lookup"><span data-stu-id="5df07-105">Hierarchy</span></span>

<span data-ttu-id="5df07-106">ApplicationMetadata</span><span class="sxs-lookup"><span data-stu-id="5df07-106">ApplicationMetadata</span></span> <br>

## <a name="index"></a><span data-ttu-id="5df07-107">指数</span><span class="sxs-lookup"><span data-stu-id="5df07-107">Index</span></span>

### <a name="properties"></a><span data-ttu-id="5df07-108">プロパティ</span><span class="sxs-lookup"><span data-stu-id="5df07-108">Properties</span></span>

* [<span data-ttu-id="5df07-109">ColorName</span><span class="sxs-lookup"><span data-stu-id="5df07-109">ColorName</span></span>](services-application-iapplicationmetadata.md#colorname)
* [<span data-ttu-id="5df07-110">Configs</span><span class="sxs-lookup"><span data-stu-id="5df07-110">Configs</span></span>](services-application-iapplicationmetadata.md#configs)
* [<span data-ttu-id="5df07-111">説明</span><span class="sxs-lookup"><span data-stu-id="5df07-111">Description</span></span>](services-application-iapplicationmetadata.md#description)
* [<span data-ttu-id="5df07-112">IconName</span><span class="sxs-lookup"><span data-stu-id="5df07-112">IconName</span></span>](services-application-iapplicationmetadata.md#iconname)
* [<span data-ttu-id="5df07-113">ID</span><span class="sxs-lookup"><span data-stu-id="5df07-113">Id</span></span>](services-application-iapplicationmetadata.md#id)
* [<span data-ttu-id="5df07-114">タイトル</span><span class="sxs-lookup"><span data-stu-id="5df07-114">Title</span></span>](services-application-iapplicationmetadata.md#title)

## <a name="properties"></a><span data-ttu-id="5df07-115">プロパティ</span><span class="sxs-lookup"><span data-stu-id="5df07-115">Properties</span></span>

### <a name="colorname"></a><span data-ttu-id="5df07-116">ColorName</span><span class="sxs-lookup"><span data-stu-id="5df07-116">ColorName</span></span>

<span data-ttu-id="5df07-117">ColorName: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="5df07-117">ColorName: string (optional)</span></span> 

<span data-ttu-id="5df07-118">アプリケーションのテーマ色。</span><span class="sxs-lookup"><span data-stu-id="5df07-118">The theme color of the application</span></span>


### <a name="configs"></a><span data-ttu-id="5df07-119">Configs</span><span class="sxs-lookup"><span data-stu-id="5df07-119">Configs</span></span>

<span data-ttu-id="5df07-120">Configs: [名前: 文字列]: 任意 (オプション)</span><span class="sxs-lookup"><span data-stu-id="5df07-120">Configs: [name: string]: any (optional)</span></span> 

<span data-ttu-id="5df07-121">アプリケーションは作成者またはリソース プロバイダーにより指定された名前付き構成のセットを持つことができます</span><span class="sxs-lookup"><span data-stu-id="5df07-121">An application can have a set of named config supplied by the author or the resource provider</span></span>


### <a name="description"></a><span data-ttu-id="5df07-122">説明</span><span class="sxs-lookup"><span data-stu-id="5df07-122">Description</span></span>

<span data-ttu-id="5df07-123">説明:文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="5df07-123">Description: string (optional)</span></span> 

<span data-ttu-id="5df07-124">アプリケーションの説明</span><span class="sxs-lookup"><span data-stu-id="5df07-124">The description of the application</span></span>


### <a name="iconname"></a><span data-ttu-id="5df07-125">IconName</span><span class="sxs-lookup"><span data-stu-id="5df07-125">IconName</span></span>

<span data-ttu-id="5df07-126">IconName: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="5df07-126">IconName: string (optional)</span></span> 

<span data-ttu-id="5df07-127">アプリケーションの代表的なアイコン</span><span class="sxs-lookup"><span data-stu-id="5df07-127">The representative icon of the application</span></span>


### <a name="id"></a><span data-ttu-id="5df07-128">ID</span><span class="sxs-lookup"><span data-stu-id="5df07-128">Id</span></span>

<span data-ttu-id="5df07-129">Id: 文字列</span><span class="sxs-lookup"><span data-stu-id="5df07-129">Id: string</span></span>

<span data-ttu-id="5df07-130">アプリケーションの一意の識別子</span><span class="sxs-lookup"><span data-stu-id="5df07-130">The unique identifier of the application</span></span>


### <a name="title"></a><span data-ttu-id="5df07-131">肩書き</span><span class="sxs-lookup"><span data-stu-id="5df07-131">Title</span></span>

<span data-ttu-id="5df07-132">タイトル: 文字列</span><span class="sxs-lookup"><span data-stu-id="5df07-132">Title: string</span></span>

<span data-ttu-id="5df07-133">アプリケーションのタイトル。</span><span class="sxs-lookup"><span data-stu-id="5df07-133">The title of the application</span></span>



