---
title: 輸送管理ステータス
description: このトピックでは、輸送ステータスを作成し、そのステータスを配送業者のステータスにマップする方法について説明します。
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
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 3f7d471771ec2b4703d878fbf395cd90902b6669
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/29/2020
ms.locfileid: "4432426"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="8e82d-103">輸送管理ステータス</span><span class="sxs-lookup"><span data-stu-id="8e82d-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e82d-104">出荷配送業者から提供されるコードを解釈するために、輸送状態のマスター コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="8e82d-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="8e82d-105">これにより、出荷配送業者と統合してステータスを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="8e82d-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="8e82d-106">輸送マスター ステータス コードに与える輸送状態によって、積荷、出荷、またはコンテナーの状態を容易に追跡できます。</span><span class="sxs-lookup"><span data-stu-id="8e82d-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="8e82d-107">積荷、出荷、またはコンテナーの特定の輸送ステータスは、データ統合を通じてのみ更新できます。ユーザー インターフェイスから手動で更新することはできません。</span><span class="sxs-lookup"><span data-stu-id="8e82d-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="8e82d-108">輸送状態の作成</span><span class="sxs-lookup"><span data-stu-id="8e82d-108">Create a transportation status</span></span>

<span data-ttu-id="8e82d-109">輸送ステータスを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8e82d-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="8e82d-110">**輸送管理 \> 設定 \> 輸送ステータス マスター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8e82d-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="8e82d-111">**新規** を選択して、輸送状態マスターを作成します。</span><span class="sxs-lookup"><span data-stu-id="8e82d-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="8e82d-112">**輸送状態マスター** フィールドに、輸送状態に対応した固有 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="8e82d-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="8e82d-113">**輸送タイプ** フィールドで、輸送のタイプとして *出荷配送業者* または *ハブ* のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="8e82d-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="8e82d-114">名前と輸送状態を入力します。</span><span class="sxs-lookup"><span data-stu-id="8e82d-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="8e82d-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8e82d-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="8e82d-116">配送業者ステータスへの配送ステータスのマップ</span><span class="sxs-lookup"><span data-stu-id="8e82d-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="8e82d-117">配送ステータスを配送業者ステータスにマップするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8e82d-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="8e82d-118">**輸送管理 \> 設定 \> 配送業者 \> 配送業者輸送ステータス** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8e82d-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="8e82d-119">**新規** を選択して、出荷配送業者から提供されるコードを輸送状態のマスター コードにマップします。</span><span class="sxs-lookup"><span data-stu-id="8e82d-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="8e82d-120">出荷配送業者と配送業者サービスの固有 ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e82d-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="8e82d-121">選択した出荷配送業者のコードにマップする輸送状態コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="8e82d-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="8e82d-122">出荷配送業者が使用する外部コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="8e82d-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="8e82d-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8e82d-123">Close the page.</span></span>
