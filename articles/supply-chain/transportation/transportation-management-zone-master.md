---
title: 輸送管理ゾーン マスター
description: このトピックでは、輸送管理を使用して地理的な場所をゾーンに分割する方法について説明します。
author: Henrikan
manager: ''
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSZoneMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-01-09
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2112e7131281cd485b580fd71536981c1ba4aefd
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/29/2020
ms.locfileid: "4432430"
---
# <a name="transportation-management-zone-master"></a><span data-ttu-id="8d98f-103">輸送管理ゾーン マスター</span><span class="sxs-lookup"><span data-stu-id="8d98f-103">Transportation management zone master</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d98f-104">輸送管理を使用すると、地理的な場所をゾーンに分割できます。</span><span class="sxs-lookup"><span data-stu-id="8d98f-104">Transport management lets you divide geographic locations into zones.</span></span> <span data-ttu-id="8d98f-105">場所をゾーンに分割すると、次のことができます。</span><span class="sxs-lookup"><span data-stu-id="8d98f-105">Dividing locations into zones can help to:</span></span>

- <span data-ttu-id="8d98f-106">**輸送価格の合理化**: 特に輸送場所が散在している場合など、個々の場所に基づく価格設定よりも、ゾーンごとの価格設定の方が容易になります。</span><span class="sxs-lookup"><span data-stu-id="8d98f-106">**Simplify transportation pricing** – Zone-wise pricing can be simpler than individual location-based pricing, especially when transportation locations are scattered.</span></span>
- <span data-ttu-id="8d98f-107">**積荷計画を最適化する**: ゾーンごとに積荷を統合します。</span><span class="sxs-lookup"><span data-stu-id="8d98f-107">**Optimize load planning** – By consolidating loads by zones.</span></span>
- <span data-ttu-id="8d98f-108">**工順計画を最適化する**: 特定の工順計画を特定のゾーンに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8d98f-108">**Optimize route planning** – By assigning specific route plans to specific zones.</span></span>

<span data-ttu-id="8d98f-109">ゾーンは、各ゾーンを修飾するメタデータ フィールドの値 (国、郵便番号の範囲、または配送業者のサービス) に基づいて定義します。</span><span class="sxs-lookup"><span data-stu-id="8d98f-109">You define zones based on the metadata field values (such as country, zip code range, or carrier service) that qualify each zone.</span></span> <span data-ttu-id="8d98f-110">輸送価格設定でゾーンの概念を採用していない場合は、ゾーン定義は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="8d98f-110">Zone definitions aren't required if your transportation pricing doesn't employ a zone concept.</span></span>
