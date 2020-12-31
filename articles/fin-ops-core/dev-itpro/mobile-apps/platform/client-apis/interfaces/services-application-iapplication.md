---
title: アプリケーション タイプ
description: アプリケーションの実行時のインスタンスを表します。
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
ms.openlocfilehash: 1066ae3b0689169cfb2836cecfb145e99f83174a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685427"
---
# <a name="application-type"></a><span data-ttu-id="93c76-103">アプリケーション タイプ</span><span class="sxs-lookup"><span data-stu-id="93c76-103">Application type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="93c76-104">アプリケーションの実行時のインスタンスを表します。</span><span class="sxs-lookup"><span data-stu-id="93c76-104">Represents a runtime instance of an application.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="93c76-105">階層</span><span class="sxs-lookup"><span data-stu-id="93c76-105">Hierarchy</span></span>

<span data-ttu-id="93c76-106">申請</span><span class="sxs-lookup"><span data-stu-id="93c76-106">Application</span></span> <br>

## <a name="index"></a><span data-ttu-id="93c76-107">指数</span><span class="sxs-lookup"><span data-stu-id="93c76-107">Index</span></span>

### <a name="properties"></a><span data-ttu-id="93c76-108">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93c76-108">Properties</span></span>

* [<span data-ttu-id="93c76-109">minVersion</span><span class="sxs-lookup"><span data-stu-id="93c76-109">minVersion</span></span>](services-application-iapplication.md#minversion)

### <a name="methods"></a><span data-ttu-id="93c76-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="93c76-110">Methods</span></span>

* [<span data-ttu-id="93c76-111">appInit</span><span class="sxs-lookup"><span data-stu-id="93c76-111">appInit</span></span>](services-application-iapplication.md#appinit)

## <a name="properties"></a><span data-ttu-id="93c76-112">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93c76-112">Properties</span></span>

### <a name="minversion"></a><span data-ttu-id="93c76-113">minVersion</span><span class="sxs-lookup"><span data-stu-id="93c76-113">minVersion</span></span>

<span data-ttu-id="93c76-114">minVersion: string (省略可)</span><span class="sxs-lookup"><span data-stu-id="93c76-114">minVersion: string (optional)</span></span> 

<span data-ttu-id="93c76-115">このコンポーネントで必要な最小プラットフォーム バージョンを示すオプション マーカーです。</span><span class="sxs-lookup"><span data-stu-id="93c76-115">An optional marker to indicate the minimum platform version required by this component.</span></span> <span data-ttu-id="93c76-116">これが指定され、プラットフォームの以前のバージョンへのコンポーネントの読み込みが試行されるとき、対応するワークスペースは読み込まれず、ユーザーはプラットフォームの新しいバージョンのインストールを指示されます。</span><span class="sxs-lookup"><span data-stu-id="93c76-116">When this is specified and the component is attempted to be loaded in an older version of the platform, the corresponding workspace is not loaded and user is directed to install a newer version of the platform.</span></span>


## <a name="methods"></a><span data-ttu-id="93c76-117">メソッド</span><span class="sxs-lookup"><span data-stu-id="93c76-117">Methods</span></span>

### <a name="appinit"></a><span data-ttu-id="93c76-118">appInit</span><span class="sxs-lookup"><span data-stu-id="93c76-118">appInit</span></span>


<span data-ttu-id="93c76-119">appInit(metadata: [ApplicationMetadata](services-application-iapplicationmetadata.md)): any</span><span class="sxs-lookup"><span data-stu-id="93c76-119">appInit(metadata: [ApplicationMetadata](services-application-iapplicationmetadata.md)): any</span></span>

<span data-ttu-id="93c76-120">このメソッドは、アプリケーションが実行される時点で呼び出され、アプリケーション メタデータのインスタンスが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="93c76-120">This method is invoked at the point the application is about to run, with the instance of the application metadata loaded.</span></span>
<span data-ttu-id="93c76-121">渡されたメタデータは、このメソッドが戻る前に動作を変更するために変更できます。</span><span class="sxs-lookup"><span data-stu-id="93c76-121">The metadata passed in can be still modified to change behaviors before this method returns.</span></span>


#### <a name="parameters"></a><span data-ttu-id="93c76-122">パラメーター</span><span class="sxs-lookup"><span data-stu-id="93c76-122">Parameters</span></span>

| <span data-ttu-id="93c76-123">氏名</span><span class="sxs-lookup"><span data-stu-id="93c76-123">Name</span></span> | <span data-ttu-id="93c76-124">種類</span><span class="sxs-lookup"><span data-stu-id="93c76-124">Type</span></span> | <span data-ttu-id="93c76-125">説明</span><span class="sxs-lookup"><span data-stu-id="93c76-125">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="93c76-126">metadata</span><span class="sxs-lookup"><span data-stu-id="93c76-126">metadata</span></span>|[<span data-ttu-id="93c76-127">ApplicationMetadata</span><span class="sxs-lookup"><span data-stu-id="93c76-127">ApplicationMetadata</span></span>](services-application-iapplicationmetadata.md)||

#### <a name="returns-any"></a><span data-ttu-id="93c76-128">any を返します</span><span class="sxs-lookup"><span data-stu-id="93c76-128">Returns any</span></span>

