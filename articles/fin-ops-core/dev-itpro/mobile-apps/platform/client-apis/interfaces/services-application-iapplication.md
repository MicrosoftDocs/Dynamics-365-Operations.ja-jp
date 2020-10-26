---
title: アプリケーション タイプ
description: アプリケーションの実行時のインスタンスを表します。
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
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: b6f75076a6e263542542d05df72eb367c245f8a7
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983965"
---
# <a name="application-type"></a><span data-ttu-id="99be7-103">アプリケーション タイプ</span><span class="sxs-lookup"><span data-stu-id="99be7-103">Application type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="99be7-104">アプリケーションの実行時のインスタンスを表します。</span><span class="sxs-lookup"><span data-stu-id="99be7-104">Represents a runtime instance of an application.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="99be7-105">階層</span><span class="sxs-lookup"><span data-stu-id="99be7-105">Hierarchy</span></span>

<span data-ttu-id="99be7-106">申請</span><span class="sxs-lookup"><span data-stu-id="99be7-106">Application</span></span> <br>

## <a name="index"></a><span data-ttu-id="99be7-107">指数</span><span class="sxs-lookup"><span data-stu-id="99be7-107">Index</span></span>

### <a name="properties"></a><span data-ttu-id="99be7-108">プロパティ</span><span class="sxs-lookup"><span data-stu-id="99be7-108">Properties</span></span>

* [<span data-ttu-id="99be7-109">minVersion</span><span class="sxs-lookup"><span data-stu-id="99be7-109">minVersion</span></span>](services-application-iapplication.md#minversion)

### <a name="methods"></a><span data-ttu-id="99be7-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="99be7-110">Methods</span></span>

* [<span data-ttu-id="99be7-111">appInit</span><span class="sxs-lookup"><span data-stu-id="99be7-111">appInit</span></span>](services-application-iapplication.md#appinit)

## <a name="properties"></a><span data-ttu-id="99be7-112">プロパティ</span><span class="sxs-lookup"><span data-stu-id="99be7-112">Properties</span></span>

### <a name="minversion"></a><span data-ttu-id="99be7-113">minVersion</span><span class="sxs-lookup"><span data-stu-id="99be7-113">minVersion</span></span>

<span data-ttu-id="99be7-114">minVersion: string (省略可)</span><span class="sxs-lookup"><span data-stu-id="99be7-114">minVersion: string (optional)</span></span> 

<span data-ttu-id="99be7-115">このコンポーネントで必要な最小プラットフォーム バージョンを示すオプション マーカーです。</span><span class="sxs-lookup"><span data-stu-id="99be7-115">An optional marker to indicate the minimum platform version required by this component.</span></span> <span data-ttu-id="99be7-116">これが指定され、プラットフォームの以前のバージョンへのコンポーネントの読み込みが試行されるとき、対応するワークスペースは読み込まれず、ユーザーはプラットフォームの新しいバージョンのインストールを指示されます。</span><span class="sxs-lookup"><span data-stu-id="99be7-116">When this is specified and the component is attempted to be loaded in an older version of the platform, the corresponding workspace is not loaded and user is directed to install a newer version of the platform.</span></span>


## <a name="methods"></a><span data-ttu-id="99be7-117">メソッド</span><span class="sxs-lookup"><span data-stu-id="99be7-117">Methods</span></span>

### <a name="appinit"></a><span data-ttu-id="99be7-118">appInit</span><span class="sxs-lookup"><span data-stu-id="99be7-118">appInit</span></span>


<span data-ttu-id="99be7-119">appInit(metadata: [ApplicationMetadata](services-application-iapplicationmetadata.md)): any</span><span class="sxs-lookup"><span data-stu-id="99be7-119">appInit(metadata: [ApplicationMetadata](services-application-iapplicationmetadata.md)): any</span></span>

<span data-ttu-id="99be7-120">このメソッドは、アプリケーションが実行される時点で呼び出され、アプリケーション メタデータのインスタンスが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="99be7-120">This method is invoked at the point the application is about to run, with the instance of the application metadata loaded.</span></span>
<span data-ttu-id="99be7-121">渡されたメタデータは、このメソッドが戻る前に動作を変更するために変更できます。</span><span class="sxs-lookup"><span data-stu-id="99be7-121">The metadata passed in can be still modified to change behaviors before this method returns.</span></span>


#### <a name="parameters"></a><span data-ttu-id="99be7-122">パラメーター</span><span class="sxs-lookup"><span data-stu-id="99be7-122">Parameters</span></span>

| <span data-ttu-id="99be7-123">氏名</span><span class="sxs-lookup"><span data-stu-id="99be7-123">Name</span></span> | <span data-ttu-id="99be7-124">種類</span><span class="sxs-lookup"><span data-stu-id="99be7-124">Type</span></span> | <span data-ttu-id="99be7-125">説明</span><span class="sxs-lookup"><span data-stu-id="99be7-125">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="99be7-126">metadata</span><span class="sxs-lookup"><span data-stu-id="99be7-126">metadata</span></span>|[<span data-ttu-id="99be7-127">ApplicationMetadata</span><span class="sxs-lookup"><span data-stu-id="99be7-127">ApplicationMetadata</span></span>](services-application-iapplicationmetadata.md)||

#### <a name="returns-any"></a><span data-ttu-id="99be7-128">any を返します</span><span class="sxs-lookup"><span data-stu-id="99be7-128">Returns any</span></span>

