---
title: Lifecycle Services (LCS) 内での構成マネージャー
description: Microsoft Dynamics Lifecycle Services の構成マネージャー (ベータ) 機能を使用すると、Microsoft Dynamics AX 2012 R3 の 1 つのインスタンスから他のインスタンスに構成をコピーすることができます。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012, Operations
ms.custom: 62753
ms.assetid: fab3f6cf-03db-47c7-90fb-f8bc03dacf49
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 8af724108aabb477625df02a618a981858978f94
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369380"
---
# <a name="configuration-manager-in-lifecycle-services-lcs"></a><span data-ttu-id="816b7-103">Lifecycle Services (LCS) 内での構成マネージャー</span><span class="sxs-lookup"><span data-stu-id="816b7-103">Configuration manager in Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="816b7-104">構成マネージャーを使用すると、以下の条件を満たす Dynamics AX 2012 R3 環境間で相互にコピーを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="816b7-104">You can use the Configuration manager to copy from and to Dynamics AX 2012 R3 environments that meet the following criteria:</span></span>
-   <span data-ttu-id="816b7-105">Lifecycle Services プロジェクトの一部として管理</span><span class="sxs-lookup"><span data-stu-id="816b7-105">Managed as part of a Lifecycle Services project</span></span>
-   <span data-ttu-id="816b7-106">システム診断の実行</span><span class="sxs-lookup"><span data-stu-id="816b7-106">Running System diagnostics</span></span>
-   <span data-ttu-id="816b7-107">データのインポート/エクスポート フレームワークの実行中</span><span class="sxs-lookup"><span data-stu-id="816b7-107">Running the Data Import/Export Framework</span></span>

| <span data-ttu-id="816b7-108">**重要**</span><span class="sxs-lookup"><span data-stu-id="816b7-108">**Important**</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="816b7-109">この機能は、運用上の用途ではサポートされて**いません**。 </span><span class="sxs-lookup"><span data-stu-id="816b7-109">This feature is **not** supported for production use.</span></span> <span data-ttu-id="816b7-110">構成マネージャー (ベータ) は、環境内のデータのインポート/エクスポート フレームワークからのエンティティに依存します。</span><span class="sxs-lookup"><span data-stu-id="816b7-110">Configuration manager (beta) relies on entities from the Data Import/Export Framework in your environment.</span></span> <span data-ttu-id="816b7-111">これらのエンティティには現在 AX 2012 R3 のすべての機能が含まれていないため、一部の構成データは環境間でコピーされません。</span><span class="sxs-lookup"><span data-stu-id="816b7-111">Because these entities do not currently include all the functionality in AX 2012 R3, some configuration data is not copied between environments.</span></span> |

<span data-ttu-id="816b7-112">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="816b7-112">For more information, see:</span></span>
-   [<span data-ttu-id="816b7-113">構成マネージャーの設定 (Lifecycle Services、LCS)</span><span class="sxs-lookup"><span data-stu-id="816b7-113">Set up Configuration manager (Lifecycle Services, LCS)</span></span>](set-up-configuration-manager-lcs.md)
-   [<span data-ttu-id="816b7-114">コンフィギュレーションのコピー (Lifecycle Services、LCS)</span><span class="sxs-lookup"><span data-stu-id="816b7-114">Copy a configuration (Lifecycle Services, LCS)</span></span>](copy-configuration-lcs.md)





