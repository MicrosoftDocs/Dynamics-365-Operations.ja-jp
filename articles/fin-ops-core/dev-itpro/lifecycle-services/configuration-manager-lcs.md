---
title: Lifecycle Services の設定の概要
description: Microsoft Dynamics Lifecycle Services の構成マネージャー (ベータ) 機能を使用すると、Microsoft Dynamics AX 2012 R3 の 1 つのインスタンスから他のインスタンスに構成をコピーすることができます。
author: RobinARH
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012, Operations
ms.custom: 62753
ms.assetid: fab3f6cf-03db-47c7-90fb-f8bc03dacf49
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 8b21ff7e1dd7c5e0742066926305cd2c38297d0d
ms.sourcegitcommit: 759325234a763e14071348a6f5399999a92f8264
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2020
ms.locfileid: "2983715"
---
# <a name="configuration-in-lifecycle-services-overview"></a><span data-ttu-id="b73e3-103">Lifecycle Services の設定の概要</span><span class="sxs-lookup"><span data-stu-id="b73e3-103">Configuration in Lifecycle Services overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b73e3-104">構成マネージャーを使用すると、以下の条件を満たす Dynamics AX 2012 R3 環境間で相互にコピーを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="b73e3-104">You can use the Configuration manager to copy from and to Dynamics AX 2012 R3 environments that meet the following criteria:</span></span>
-   <span data-ttu-id="b73e3-105">Lifecycle Services プロジェクトの一部として管理</span><span class="sxs-lookup"><span data-stu-id="b73e3-105">Managed as part of a Lifecycle Services project</span></span>
-   <span data-ttu-id="b73e3-106">システム診断の実行</span><span class="sxs-lookup"><span data-stu-id="b73e3-106">Running System diagnostics</span></span>
-   <span data-ttu-id="b73e3-107">データのインポート/エクスポート フレームワークの実行中</span><span class="sxs-lookup"><span data-stu-id="b73e3-107">Running the Data Import/Export Framework</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b73e3-108">この機能は、運用上の用途ではサポートされて**いません**。 </span><span class="sxs-lookup"><span data-stu-id="b73e3-108">This feature is **not** supported for production use.</span></span> <span data-ttu-id="b73e3-109">構成マネージャー (ベータ) は、環境内のデータのインポート/エクスポート フレームワークからのエンティティに依存します。</span><span class="sxs-lookup"><span data-stu-id="b73e3-109">Configuration manager (beta) relies on entities from the Data Import/Export Framework in your environment.</span></span> <span data-ttu-id="b73e3-110">これらのエンティティには現在 AX 2012 R3 のすべての機能が含まれていないため、一部の構成データは環境間でコピーされません。</span><span class="sxs-lookup"><span data-stu-id="b73e3-110">Because these entities do not currently include all the functionality in AX 2012 R3, some configuration data is not copied between environments.</span></span>

<span data-ttu-id="b73e3-111">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b73e3-111">For more information, see:</span></span>
-   [<span data-ttu-id="b73e3-112">構成マネージャーの設定</span><span class="sxs-lookup"><span data-stu-id="b73e3-112">Set up Configuration manager</span></span>](set-up-configuration-manager-lcs.md)
-   [<span data-ttu-id="b73e3-113">構成マネージャーを使用して構成をコピーする</span><span class="sxs-lookup"><span data-stu-id="b73e3-113">Copy configurations by using Configuration manager</span></span>](copy-configuration-lcs.md)





