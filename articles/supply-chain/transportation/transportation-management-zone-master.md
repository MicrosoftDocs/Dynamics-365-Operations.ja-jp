---
title: 輸送管理ゾーン マスター
description: このトピックでは、輸送管理を使用して地理的な場所をゾーンに分割する方法について説明します。
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSZoneMaster
audience: Application User
ms.reviewer: kamaybac
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-01-09
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 7347add052ec4a9540417a5aeea64ab623026954
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880741"
---
# <a name="transportation-management-zone-master"></a><span data-ttu-id="491b6-103">輸送管理ゾーン マスター</span><span class="sxs-lookup"><span data-stu-id="491b6-103">Transportation management zone master</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="491b6-104">輸送管理を使用すると、地理的な場所をゾーンに分割できます。</span><span class="sxs-lookup"><span data-stu-id="491b6-104">Transport management lets you divide geographic locations into zones.</span></span> <span data-ttu-id="491b6-105">場所をゾーンに分割すると、次のことができます。</span><span class="sxs-lookup"><span data-stu-id="491b6-105">Dividing locations into zones can help to:</span></span>

- <span data-ttu-id="491b6-106">**輸送価格の合理化**: 特に輸送場所が散在している場合など、個々の場所に基づく価格設定よりも、ゾーンごとの価格設定の方が容易になります。</span><span class="sxs-lookup"><span data-stu-id="491b6-106">**Simplify transportation pricing** – Zone-wise pricing can be simpler than individual location-based pricing, especially when transportation locations are scattered.</span></span>
- <span data-ttu-id="491b6-107">**積荷計画を最適化する**: ゾーンごとに積荷を統合します。</span><span class="sxs-lookup"><span data-stu-id="491b6-107">**Optimize load planning** – By consolidating loads by zones.</span></span>
- <span data-ttu-id="491b6-108">**工順計画を最適化する**: 特定の工順計画を特定のゾーンに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="491b6-108">**Optimize route planning** – By assigning specific route plans to specific zones.</span></span>

<span data-ttu-id="491b6-109">ゾーンは、各ゾーンを修飾するメタデータ フィールドの値 (国、郵便番号の範囲、または配送業者のサービス) に基づいて定義します。</span><span class="sxs-lookup"><span data-stu-id="491b6-109">You define zones based on the metadata field values (such as country, zip code range, or carrier service) that qualify each zone.</span></span> <span data-ttu-id="491b6-110">輸送価格設定でゾーンの概念を採用していない場合は、ゾーン定義は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="491b6-110">Zone definitions aren't required if your transportation pricing doesn't employ a zone concept.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
