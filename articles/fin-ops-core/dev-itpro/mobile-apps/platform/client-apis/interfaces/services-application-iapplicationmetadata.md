---
title: ApplicationMetadata タイプ
description: アプリケーションの宣言メタデータを表します
author: robinarh
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c4750ad0556048c0add255a914ac5eebe0de57f3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685425"
---
# <a name="applicationmetadata-type"></a><span data-ttu-id="c0e3a-103">ApplicationMetadata タイプ</span><span class="sxs-lookup"><span data-stu-id="c0e3a-103">ApplicationMetadata type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="c0e3a-104">アプリケーションの宣言メタデータを表します</span><span class="sxs-lookup"><span data-stu-id="c0e3a-104">Represents the declarative metadata of an application</span></span>

### <a name="hierarchy"></a><span data-ttu-id="c0e3a-105">階層</span><span class="sxs-lookup"><span data-stu-id="c0e3a-105">Hierarchy</span></span>

<span data-ttu-id="c0e3a-106">ApplicationMetadata</span><span class="sxs-lookup"><span data-stu-id="c0e3a-106">ApplicationMetadata</span></span> <br>

## <a name="index"></a><span data-ttu-id="c0e3a-107">指数</span><span class="sxs-lookup"><span data-stu-id="c0e3a-107">Index</span></span>

### <a name="properties"></a><span data-ttu-id="c0e3a-108">プロパティ</span><span class="sxs-lookup"><span data-stu-id="c0e3a-108">Properties</span></span>

* [<span data-ttu-id="c0e3a-109">ColorName</span><span class="sxs-lookup"><span data-stu-id="c0e3a-109">ColorName</span></span>](services-application-iapplicationmetadata.md#colorname)
* [<span data-ttu-id="c0e3a-110">Configs</span><span class="sxs-lookup"><span data-stu-id="c0e3a-110">Configs</span></span>](services-application-iapplicationmetadata.md#configs)
* [<span data-ttu-id="c0e3a-111">説明</span><span class="sxs-lookup"><span data-stu-id="c0e3a-111">Description</span></span>](services-application-iapplicationmetadata.md#description)
* [<span data-ttu-id="c0e3a-112">IconName</span><span class="sxs-lookup"><span data-stu-id="c0e3a-112">IconName</span></span>](services-application-iapplicationmetadata.md#iconname)
* [<span data-ttu-id="c0e3a-113">ID</span><span class="sxs-lookup"><span data-stu-id="c0e3a-113">Id</span></span>](services-application-iapplicationmetadata.md#id)
* [<span data-ttu-id="c0e3a-114">タイトル</span><span class="sxs-lookup"><span data-stu-id="c0e3a-114">Title</span></span>](services-application-iapplicationmetadata.md#title)

## <a name="properties"></a><span data-ttu-id="c0e3a-115">プロパティ</span><span class="sxs-lookup"><span data-stu-id="c0e3a-115">Properties</span></span>

### <a name="colorname"></a><span data-ttu-id="c0e3a-116">ColorName</span><span class="sxs-lookup"><span data-stu-id="c0e3a-116">ColorName</span></span>

<span data-ttu-id="c0e3a-117">ColorName: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="c0e3a-117">ColorName: string (optional)</span></span> 

<span data-ttu-id="c0e3a-118">アプリケーションのテーマ色。</span><span class="sxs-lookup"><span data-stu-id="c0e3a-118">The theme color of the application</span></span>


### <a name="configs"></a><span data-ttu-id="c0e3a-119">Configs</span><span class="sxs-lookup"><span data-stu-id="c0e3a-119">Configs</span></span>

<span data-ttu-id="c0e3a-120">Configs: [名前: 文字列]: 任意 (オプション)</span><span class="sxs-lookup"><span data-stu-id="c0e3a-120">Configs: [name: string]: any (optional)</span></span> 

<span data-ttu-id="c0e3a-121">アプリケーションは作成者またはリソース プロバイダーにより指定された名前付き構成のセットを持つことができます</span><span class="sxs-lookup"><span data-stu-id="c0e3a-121">An application can have a set of named config supplied by the author or the resource provider</span></span>


### <a name="description"></a><span data-ttu-id="c0e3a-122">説明</span><span class="sxs-lookup"><span data-stu-id="c0e3a-122">Description</span></span>

<span data-ttu-id="c0e3a-123">説明:文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="c0e3a-123">Description: string (optional)</span></span> 

<span data-ttu-id="c0e3a-124">アプリケーションの説明</span><span class="sxs-lookup"><span data-stu-id="c0e3a-124">The description of the application</span></span>


### <a name="iconname"></a><span data-ttu-id="c0e3a-125">IconName</span><span class="sxs-lookup"><span data-stu-id="c0e3a-125">IconName</span></span>

<span data-ttu-id="c0e3a-126">IconName: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="c0e3a-126">IconName: string (optional)</span></span> 

<span data-ttu-id="c0e3a-127">アプリケーションの代表的なアイコン</span><span class="sxs-lookup"><span data-stu-id="c0e3a-127">The representative icon of the application</span></span>


### <a name="id"></a><span data-ttu-id="c0e3a-128">ID</span><span class="sxs-lookup"><span data-stu-id="c0e3a-128">Id</span></span>

<span data-ttu-id="c0e3a-129">Id: 文字列</span><span class="sxs-lookup"><span data-stu-id="c0e3a-129">Id: string</span></span>

<span data-ttu-id="c0e3a-130">アプリケーションの一意の識別子</span><span class="sxs-lookup"><span data-stu-id="c0e3a-130">The unique identifier of the application</span></span>


### <a name="title"></a><span data-ttu-id="c0e3a-131">肩書き</span><span class="sxs-lookup"><span data-stu-id="c0e3a-131">Title</span></span>

<span data-ttu-id="c0e3a-132">タイトル: 文字列</span><span class="sxs-lookup"><span data-stu-id="c0e3a-132">Title: string</span></span>

<span data-ttu-id="c0e3a-133">アプリケーションのタイトル。</span><span class="sxs-lookup"><span data-stu-id="c0e3a-133">The title of the application</span></span>


