---
title: PageState 列挙
description: ページを配置できるさまざまな高レベルの状態を表します。
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
ms.openlocfilehash: 6cc7fdef9ae4deb094d845c039c7011cd4066b06
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183148"
---
# <a name="pagestate-enumeration"></a><span data-ttu-id="0ca2a-103">PageState 列挙</span><span class="sxs-lookup"><span data-stu-id="0ca2a-103">PageState enumeration</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="0ca2a-104">ページを配置できるさまざまな高レベルの状態を表します。</span><span class="sxs-lookup"><span data-stu-id="0ca2a-104">Represents the various high-level states the a page can be in.</span></span>

## <a name="index"></a><span data-ttu-id="0ca2a-105">指数</span><span class="sxs-lookup"><span data-stu-id="0ca2a-105">Index</span></span>

### <a name="enumeration-members"></a><span data-ttu-id="0ca2a-106">列挙型メンバー</span><span class="sxs-lookup"><span data-stu-id="0ca2a-106">Enumeration members</span></span>

* [<span data-ttu-id="0ca2a-107">エラー</span><span class="sxs-lookup"><span data-stu-id="0ca2a-107">error</span></span>](view-model-ipage-pagestate.md#error)
* [<span data-ttu-id="0ca2a-108">読み込み済み</span><span class="sxs-lookup"><span data-stu-id="0ca2a-108">loaded</span></span>](view-model-ipage-pagestate.md#loaded)
* [<span data-ttu-id="0ca2a-109">読み込み中</span><span class="sxs-lookup"><span data-stu-id="0ca2a-109">loading</span></span>](view-model-ipage-pagestate.md#loading)
* [<span data-ttu-id="0ca2a-110">オフライン</span><span class="sxs-lookup"><span data-stu-id="0ca2a-110">offline</span></span>](view-model-ipage-pagestate.md#offline)
* [<span data-ttu-id="0ca2a-111">更新中</span><span class="sxs-lookup"><span data-stu-id="0ca2a-111">refreshing</span></span>](view-model-ipage-pagestate.md#refreshing)

## <a name="enumeration-members"></a><span data-ttu-id="0ca2a-112">列挙型メンバー</span><span class="sxs-lookup"><span data-stu-id="0ca2a-112">Enumeration members</span></span>

### <a name="error"></a><span data-ttu-id="0ca2a-113">エラー</span><span class="sxs-lookup"><span data-stu-id="0ca2a-113">error</span></span>

<span data-ttu-id="0ca2a-114">エラー: 10 ページは現在、エラー状態にありますが、更新することでこの状態から抜け出すことができます。</span><span class="sxs-lookup"><span data-stu-id="0ca2a-114">error: 10 The page is currently in the error state, but can be refreshed in an attempt to get out of this state.</span></span>


### <a name="loaded"></a><span data-ttu-id="0ca2a-115">loaded</span><span class="sxs-lookup"><span data-stu-id="0ca2a-115">loaded</span></span>

<span data-ttu-id="0ca2a-116">loaded: 3 ページが完全に読み込まれ、更新可能であり、可能ならば送信できます。</span><span class="sxs-lookup"><span data-stu-id="0ca2a-116">loaded: 3 The page is fully loaded and can be refreshed and, if possible, submitted.</span></span>


### <a name="loading"></a><span data-ttu-id="0ca2a-117">loading</span><span class="sxs-lookup"><span data-stu-id="0ca2a-117">loading</span></span>

<span data-ttu-id="0ca2a-118">loading: 2 ページが現在読み込まれています。</span><span class="sxs-lookup"><span data-stu-id="0ca2a-118">loading: 2 The page is currently being loaded.</span></span>


### <a name="offline"></a><span data-ttu-id="0ca2a-119">オフライン</span><span class="sxs-lookup"><span data-stu-id="0ca2a-119">offline</span></span>

<span data-ttu-id="0ca2a-120">offline: 1 ページはオフライン モードで読み込まれたので更新できません。</span><span class="sxs-lookup"><span data-stu-id="0ca2a-120">offline: 1 The page was loaded in the offline mode, thus not refreshable.</span></span>


### <a name="refreshing"></a><span data-ttu-id="0ca2a-121">更新中</span><span class="sxs-lookup"><span data-stu-id="0ca2a-121">refreshing</span></span>

<span data-ttu-id="0ca2a-122">更新中: 4 ページは現在データを更新中です。</span><span class="sxs-lookup"><span data-stu-id="0ca2a-122">refreshing: 4 The page is currently refreshing its data.</span></span>


