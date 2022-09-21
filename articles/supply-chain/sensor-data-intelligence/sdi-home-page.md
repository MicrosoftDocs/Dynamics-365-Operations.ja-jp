---
title: Sensor Data Intelligence のホーム ページ
description: この記事では、Sensor Data Intelligence の概要を示します。 組織はこの機能を使用して、生産フロアの機械や設備からの IoT (Internet of Things) 信号に基づいて、Microsoft Dynamics 365 Supply Chain Management のプロセスを活用できます。
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2e4cd8d4d4ffcd10d02fbf26615f12cdd6ccca9e
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428371"
---
# <a name="sensor-data-intelligence-home-page"></a>Sensor Data Intelligence のホーム ページ

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management 向け Sensor Data Intelligence は、組織が Supply Chain Management で、製造フロアのマシンや機器からの Internet of Things (IoT) 信号に基づいて業務プロセスを推進するのを可能にします。 これは、以前に Supply Chain Management で使用できる、名前を変更した更新されたバージョンの *IoT インテリジェンス* 機能です。

Sensor Data Intelligence を使用すると、次のタスクを実行できます。

- マシンや機器から詳細を収集して、Supply Chain Management でメンテナンス資産カウンターを更新して、予防メンテナンスを推進します。
- Microsoft Dynamics Lifecycle Services (LCS) のコンポーネントを手動でインストール および構成する代わりに、単純なウィザードを使用してソリューションを設定します。
- 独自のサブスクリプションにコンポーネントを配置することにより、Azure コンポーネントを柔軟に管理できます。
- このソリューションを、Azure コンポーネントで実行するビジネス ロジックとして構成、スケール、拡張します。 これで、これらのコンポーネントは独自のサブスクリプションで管理されます。 したがって、必要に応じてカスタマイズして、固有の業務ニーズを満たすことができます。

## <a name="business-scenarios"></a>業務シナリオ

Sensor Data Intelligence は、いくつかのタイプの機能を有効にするための機能です。これらの機能は、システムの特定の *シナリオ* によって表されます。 各シナリオは、次の表に示す、システムに特別な構成オプションセットを提供します。

| シナリオ | Description |
|---|---|
| [資産ダウンタイム](sdi-scenario-asset-downtime.md) | データ を使用して機械のダウンタイムを追跡し、マシン資産の効率を正確に追跡します。 |
| [資産メンテナンス](sdi-scenario-asset-maintenance.md) | マシン資産の重要な制御点の読み取り値を読み取りプログラムに基づいてメンテナンス計画を改善し、管理費を最小限にし、資産の寿命を拡張します。 |
| [マシンの状態](sdi-scenario-equipment-downtime.md) | マシンの動作を変更し、遅延を緩和するためのオプションを提供するために、動作を開始する読み取りを使用してプランナーに通知することで、効率を保証します。 |
| [製品の品質](sdi-scenario-product-quality.md) | 水分、温度、カスタム定義の品質測定基準など、各製品バッチの実際のプロパティを比較することで、製品バッチの品質を保証します。 誤差が発生した場合は、システムによってユーザーに通知されます。 |
| [生産の遅延](sdi-scenario-production-delays.md) | 実際のサイクル時間と計画されたサイクル時間を比較し、生産の変更予定時刻を監修者に通知するには、大計な読み取り値を使用します。 その後、必要に応じて監修者が介入し、最大の運用効率を確保できます。 |

## <a name="architecture"></a>アーキテクチャ

次のアーキテクチャ図は、ソリューションとそのコンポーネントの概要を示しています。

![Sensor Data Intelligence のアーキテクチャ図。](media/sdi-architecture.png "Sensor Data Intelligence のアーキテクチャ図")
