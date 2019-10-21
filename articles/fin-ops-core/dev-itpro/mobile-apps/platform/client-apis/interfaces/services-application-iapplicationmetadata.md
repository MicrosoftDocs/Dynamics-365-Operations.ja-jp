---
title: ApplicationMetadata タイプ
description: アプリケーションの宣言メタデータを表します
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: ''
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9b005b477895d75a6b9a6e92afe4694386bd45b2
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183146"
---
# <a name="applicationmetadata-type"></a><span data-ttu-id="e15fa-103">ApplicationMetadata タイプ</span><span class="sxs-lookup"><span data-stu-id="e15fa-103">ApplicationMetadata type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="e15fa-104">アプリケーションの宣言メタデータを表します</span><span class="sxs-lookup"><span data-stu-id="e15fa-104">Represents the declarative metadata of an application</span></span>

### <a name="hierarchy"></a><span data-ttu-id="e15fa-105">階層</span><span class="sxs-lookup"><span data-stu-id="e15fa-105">Hierarchy</span></span>

<span data-ttu-id="e15fa-106">ApplicationMetadata</span><span class="sxs-lookup"><span data-stu-id="e15fa-106">ApplicationMetadata</span></span> <br>

## <a name="index"></a><span data-ttu-id="e15fa-107">指数</span><span class="sxs-lookup"><span data-stu-id="e15fa-107">Index</span></span>

### <a name="properties"></a><span data-ttu-id="e15fa-108">プロパティ</span><span class="sxs-lookup"><span data-stu-id="e15fa-108">Properties</span></span>

* [<span data-ttu-id="e15fa-109">ColorName</span><span class="sxs-lookup"><span data-stu-id="e15fa-109">ColorName</span></span>](services-application-iapplicationmetadata.md#colorname)
* [<span data-ttu-id="e15fa-110">Configs</span><span class="sxs-lookup"><span data-stu-id="e15fa-110">Configs</span></span>](services-application-iapplicationmetadata.md#configs)
* [<span data-ttu-id="e15fa-111">説明</span><span class="sxs-lookup"><span data-stu-id="e15fa-111">Description</span></span>](services-application-iapplicationmetadata.md#description)
* [<span data-ttu-id="e15fa-112">IconName</span><span class="sxs-lookup"><span data-stu-id="e15fa-112">IconName</span></span>](services-application-iapplicationmetadata.md#iconname)
* [<span data-ttu-id="e15fa-113">ID</span><span class="sxs-lookup"><span data-stu-id="e15fa-113">Id</span></span>](services-application-iapplicationmetadata.md#id)
* [<span data-ttu-id="e15fa-114">タイトル</span><span class="sxs-lookup"><span data-stu-id="e15fa-114">Title</span></span>](services-application-iapplicationmetadata.md#title)

## <a name="properties"></a><span data-ttu-id="e15fa-115">プロパティ</span><span class="sxs-lookup"><span data-stu-id="e15fa-115">Properties</span></span>

### <a name="colorname"></a><span data-ttu-id="e15fa-116">ColorName</span><span class="sxs-lookup"><span data-stu-id="e15fa-116">ColorName</span></span>

<span data-ttu-id="e15fa-117">ColorName: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="e15fa-117">ColorName: string (optional)</span></span> 

<span data-ttu-id="e15fa-118">アプリケーションのテーマ色。</span><span class="sxs-lookup"><span data-stu-id="e15fa-118">The theme color of the application</span></span>


### <a name="configs"></a><span data-ttu-id="e15fa-119">Configs</span><span class="sxs-lookup"><span data-stu-id="e15fa-119">Configs</span></span>

<span data-ttu-id="e15fa-120">Configs: [名前: 文字列]: 任意 (オプション)</span><span class="sxs-lookup"><span data-stu-id="e15fa-120">Configs: [name: string]: any (optional)</span></span> 

<span data-ttu-id="e15fa-121">アプリケーションは作成者またはリソース プロバイダーにより指定された名前付き構成のセットを持つことができます</span><span class="sxs-lookup"><span data-stu-id="e15fa-121">An application can have a set of named config supplied by the author or the resource provider</span></span>


### <a name="description"></a><span data-ttu-id="e15fa-122">説明</span><span class="sxs-lookup"><span data-stu-id="e15fa-122">Description</span></span>

<span data-ttu-id="e15fa-123">説明:文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="e15fa-123">Description: string (optional)</span></span> 

<span data-ttu-id="e15fa-124">アプリケーションの説明</span><span class="sxs-lookup"><span data-stu-id="e15fa-124">The description of the application</span></span>


### <a name="iconname"></a><span data-ttu-id="e15fa-125">IconName</span><span class="sxs-lookup"><span data-stu-id="e15fa-125">IconName</span></span>

<span data-ttu-id="e15fa-126">IconName: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="e15fa-126">IconName: string (optional)</span></span> 

<span data-ttu-id="e15fa-127">アプリケーションの代表的なアイコン</span><span class="sxs-lookup"><span data-stu-id="e15fa-127">The representative icon of the application</span></span>


### <a name="id"></a><span data-ttu-id="e15fa-128">ID</span><span class="sxs-lookup"><span data-stu-id="e15fa-128">Id</span></span>

<span data-ttu-id="e15fa-129">Id: 文字列</span><span class="sxs-lookup"><span data-stu-id="e15fa-129">Id: string</span></span>

<span data-ttu-id="e15fa-130">アプリケーションの一意の識別子</span><span class="sxs-lookup"><span data-stu-id="e15fa-130">The unique identifier of the application</span></span>


### <a name="title"></a><span data-ttu-id="e15fa-131">肩書き</span><span class="sxs-lookup"><span data-stu-id="e15fa-131">Title</span></span>

<span data-ttu-id="e15fa-132">タイトル: 文字列</span><span class="sxs-lookup"><span data-stu-id="e15fa-132">Title: string</span></span>

<span data-ttu-id="e15fa-133">アプリケーションのタイトル。</span><span class="sxs-lookup"><span data-stu-id="e15fa-133">The title of the application</span></span>


