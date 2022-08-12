---
title: 需要主導型材料所要量計画 (DDMRP) の概要
description: この記事では、供給と需要のデカップリングに基づく計画方法である需要主導型材料所要量計画 (DDMRP) に関する情報を提供します。
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: d894b83afe822e013c0c4375e5cfe5e7e8ac8d1d
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186755"
---
# <a name="demand-driven-material-requirements-planning-ddmrp-overview"></a>需要主導型材料所要量計画 (DDMRP) の概要

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

製品の製造に必要な材料とコンポーネントを計算するシステムとして、企業は長年にわたり材料所要量計画 (MRP) を使用してきました。 しかし、現在、サプライ チェーンは変化しています。 部品は、海外からの調達が多くなっているため、リード タイムが長くなっています。 このため、多くの企業では在庫の量が分からず、在庫切れや過剰在庫になったという報告があります。 また、市場の変動 (時には予測が不正確) が大きく、顧客は短いリード タイムで製品を要求しています。 そのため、世界中でサプライ チェーンが不足しています。 さらに、MRP ツールを使用すると、プランナーが実行するアクションを何千も与えてしまうことがよくあります。 したがって、何を重視すべきかを知るのは困難です。 多くの場合、こうした問題に対する解決策は、需要主導型材料所要量計画 (DDMRP) に切り替えることです。

DDMRP は、供給と需要のデカップリングに基づく計画方法です。 このデカップリングは、デカップリング ポイントの項目を設定することで実現されます。 それらの項目については、正しい在庫量を確保するために、バッファーが維持されています。 供給と需要のデカップリングは、変動が連鎖的に伝わらないため、"ブルウィップ効果" を防ぐのに役立ちます。 (*ブルウィップ効果* とは、小売レベルでの需要の小さな変動が、卸売業者、ディストリビューター、製造元、および原材料の仕入先レベルで、需要の変動が徐々に大きくなる可能性があることを指します。) 各バッファーは、部品の平均的な使用量をカバーすることを目的としており、需要のスパイクに対応するよう調整することも可能です。

DDMRP は、顧客の許容時間が累計リード タイムよりも短い可変環境において、価値ある計画方法であることが証明されています。

## <a name="the-five-components-of-ddmrp"></a>DDMRP の 5 つのコンポーネント

DDMRP には 5 つの連続したコンポーネントがあります (ステップ)。 最初の 3 つのコンポーネントは、基本的に需要主導型材料所要量計画モデルの初期設定および発展性のある構成を定義します。 最後の 2 つのコンポーネントは、手法の日常的な運用を定義します。

1. **[戦略的在庫配置](ddmrp-inventory-positioning.md)** – サプライ チェーン ネットワークのデカップリング ポイントを特定します。 デカップリング ポイントとは、監視および補充する在庫バッファーを配置するサプライ チェーンの特定のポイントです。
2. **[バッファー プロファイルとレベル](ddmrp-buffer-profile-and-levels.md)** – 各デカップリング ポイントについて、バッファー サイズ (最小数量、最大数量、再発注ポイント) および再発注数量を識別します。
3. **[動的バッファー調整](ddmrp-buffer-profile-and-levels.md#dynamic-adjustments)** – 変化する運用パラメーターまたは将来のイベントに基づいてバッファー レベルを調整します。
4. **[需要主導型計画](ddmrp-planning.md)** – 必要に応じて供給注文を生成します。 これらの供給注文には、製造オーダー、発注書、在庫移動オーダーが含まれます
5. **[高度な協調性と可視性のある実行](ddmrp-visual-and-collaborative-execution.md)** – 可視化を利用して供給注文を実行します。

DDMRP は通常、複数レベルの部品表 (BOM) を持つメーカーで使用されます。 ただし、流通や小売ネットワークにも適用可能です。

## <a name="ddmrp-in-dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management の DDMRP

DDMRP は Microsoft Dynamics 365 Supply Chain Management に含まれており、追加のライセンス料金は必要ありません。 Supply Chain Management では、既存の **マスター プラン** モジュールに DDMRP 機能が追加されました。 ただし、計画最適化アドインを使用することが条件となります。 

DDMRP は Supply Chain Management の既存の計画設定と統合され、これらの設定と一緒に使用することで、ビジネスに適した計画構成を行うことができます。 期間、最小/最大、要件などとは全く異なる、新しい補充コードによって制御されます。 これは新しいモジュールでもなければ、既存の計画機能を置き換えるものでもありません。 ただし、使用できる機能は増えています。
