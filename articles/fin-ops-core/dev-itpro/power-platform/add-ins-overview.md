---
title: アドインの概要
description: この記事では、財務と運用アプリの機能を拡張するために使用できるアドインに関する情報を提供します。
author: ankugo
ms.date: 02/11/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: ankugo
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: fa231890ccfd88899ed8ff253cd16a8921ca319e
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740808"
---
# <a name="add-ins-overview"></a>アドインの概要

[!include[banner](../includes/banner.md)]

アドインを使用すると、財務と運用アプリの機能を拡張できます。 すべてのアドインは、Microsoft Dynamics Lifecycle Services (LCS) のサンドボックスおよび運用環境の環境詳細ページを介してインストールされ、管理されます。 アーキテクチャおよび機能のロック解除方法については、[財務と運用アプリとの Microsoft Power Platform 統合](overview.md) を参照してください。

## <a name="what-add-ins-are-available"></a>どのアドインで使用できますか?

新しいアドインは、定期的に利用できます。 ここでは、現在使用できるアドインについて説明し、各詳細へのリンクを提供します。

### <a name="planning-optimization"></a>計画の最適化

Microsoft Dynamics 365 Supply Chain Management の計画の最適化アドインを使用すると、マスター プランの計算を、Dynamics 365 Supply Chain Management および関連する SQL データベース以外で行うことができます。 計画の最適化機能に関連する利点として、マスター プランの実行時にパフォーマンスが向上し、SQL データベースへの影響が最小限に抑えられます。 簡単な計画の実行は、営業時間内でも可能です。 したがって、プランナーは、需要またはパラメータの変更に直ちに対応できます。 詳細については、[マスター プランのシステム アーキテクチャ](../../../supply-chain/master-planning/master-planning-architecture.md) を参照してください

### <a name="inventory-visibility"></a>在庫品目一覧

Inventory Visibility Add-in は、リアルタイムで手持在庫を追跡を可能とする、独立し拡張性の高いマイクロサービスです。 そのため、在庫の可視性をグローバルに表示できます。 詳細については、[Inventory Visibility Add-in](../../../supply-chain/inventory/inventory-visibility.md) を参照してください。

### <a name="export-to-azure-data-lake"></a>Azure Data Lake へのエクスポート

Azure Data Lake へのエクスポート機能は、財務と運用アプリ データを Azure Data Lake へエクスポートし、データを最新の状態に維持するマイクロサービスに基づいています。 詳細については、[Azure Data Lake へのエキスポートの構成](../data-entities/configure-export-data-lake.md) を参照してください。

### <a name="iot-intelligence"></a>IoT インテリジェンス

IoT インテリジェンスは、Supply Chain Management のアドインです。 また、モノのインターネット (Internet of Things: IoT) の信号を Supply Chain Management のデータと統合し、実用的な分析情報を生み出します。 詳細については、[IoT インテリジェンスのホーム ページ](../../../supply-chain/iot/iot-intelligence-home-page.md) を参照してください。

### <a name="finance-insights"></a>Finance Insights

Finance Insights には構成可能なソリューションが用意されており、会社のキャッシュ フローを的確に予測したり、未払の債権に対する支払をいつ受け取るかを予測したり、予算作成プロセスを高速化するための予算案を生成できます。 これらの機能では、インテリジェントな機械学習テンプレートを使用して、ビューローからの消費者レポート情報などのサード パーティからのデータを含む提供されたデータを使用してモデルを構築します。 これらのインテリジェントな機能は、意思決定に役立ち、現在および予想されるビジネス上の課題に効果的に対応するための行動を支援します。 詳細については、[Finance insights ホーム ページ](../../../finance/finance-insights/finance-insights-home-page.md) を参照してください。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

