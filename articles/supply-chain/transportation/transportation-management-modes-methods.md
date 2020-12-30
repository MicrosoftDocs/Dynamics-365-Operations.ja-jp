---
title: 輸送管理モードと方法
description: このトピックでは、運輸管理のモードと方法を設定する方法について説明します。
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: ceb3930cdb7764f846e88edfff6906b902a7f5fa
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/29/2020
ms.locfileid: "4432428"
---
# <a name="transportation-management-modes-and-methods"></a><span data-ttu-id="41963-103">輸送管理モードと方法</span><span class="sxs-lookup"><span data-stu-id="41963-103">Transportation management modes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41963-104">輸送管理は、積荷未満 (LTL)、トラック積荷 (TL)、または小包などの、配送業者が積荷の配達に使用する輸送のタイプを表します。</span><span class="sxs-lookup"><span data-stu-id="41963-104">The transportation management  mode represents the type of transport that the carrier uses for freight deliveries, such as less than load (LTL), truckload (TL), or parcel.</span></span> <span data-ttu-id="41963-105">輸送方法は、空輸、陸上輸送、船便、鉄道輸送などの、配送業者が積荷の配達に使用する配送形態を表します。</span><span class="sxs-lookup"><span data-stu-id="41963-105">The transportation method represents the form of transport that the carrier uses for freight deliveries, such as air, ground, ocean, or rail.</span></span>

<span data-ttu-id="41963-106">モードと輸送方法は、いくつかの場面で使用されます。</span><span class="sxs-lookup"><span data-stu-id="41963-106">Modes and transportation methods are used in several contexts.</span></span> <span data-ttu-id="41963-107">工順計画ではモードのみが使用されますが、出荷配送業者と配送業者サービスを設定する際には、モードと配送方法の両方が使用されます。</span><span class="sxs-lookup"><span data-stu-id="41963-107">Only modes are used in route plans, while both modes and transportation methods are used when setting up shipping carriers and carrier services.</span></span> <span data-ttu-id="41963-108">モードと輸送方法では、明示的な関係や階層が存在しません。</span><span class="sxs-lookup"><span data-stu-id="41963-108">No explicit relationship or hierarchy exists between modes and transportation methods.</span></span>

## <a name="create-a-mode"></a><span data-ttu-id="41963-109">モードの作成</span><span class="sxs-lookup"><span data-stu-id="41963-109">Create a mode</span></span>

<span data-ttu-id="41963-110">モードを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="41963-110">To create a mode, follow these steps:</span></span>

1. <span data-ttu-id="41963-111">**輸送管理 \> 設定 \> 配送業者 \> 方式** に移動します。</span><span class="sxs-lookup"><span data-stu-id="41963-111">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="41963-112">**新規作成** を選択して、新しいモードを作成します。</span><span class="sxs-lookup"><span data-stu-id="41963-112">Select **New** to create a new mode.</span></span>
1. <span data-ttu-id="41963-113">モードのための固有 ID および説明のついた名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="41963-113">Enter a unique ID and a descriptive name for the mode.</span></span>
1. <span data-ttu-id="41963-114">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="41963-114">Close the page.</span></span>

## <a name="create-a-transportation-method"></a><span data-ttu-id="41963-115">輸送方法の作成</span><span class="sxs-lookup"><span data-stu-id="41963-115">Create a transportation method</span></span>

<span data-ttu-id="41963-116">輸送方法を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="41963-116">To create a transportation method, follow these steps:</span></span>

1. <span data-ttu-id="41963-117">**輸送管理 \> 設定 \> 配送業者 \> 輸送方法** に移動します。</span><span class="sxs-lookup"><span data-stu-id="41963-117">Go to **Transportation management \> Setup \> Carriers \> Transportation methods**.</span></span>
1. <span data-ttu-id="41963-118">**新規** を選択して新しい配送方法を作成します。</span><span class="sxs-lookup"><span data-stu-id="41963-118">Select **New** to create a new transportation method.</span></span>
1. <span data-ttu-id="41963-119">配送方法のための固有 ID および説明のついた名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="41963-119">Enter a unique ID and descriptive name for the transportation method.</span></span>
1. <span data-ttu-id="41963-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="41963-120">Close the page.</span></span>
