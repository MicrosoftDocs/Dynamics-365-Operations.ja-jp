---
title: 計画の最適化の概要
description: このトピックでは、計画の最適化機能の概要を示します。
author: ChristianRytt
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 110045d4c7e4f32c29b73096dd4df3a09b5434ac
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431744"
---
# <a name="planning-optimization-overview"></a>計画の最適化の概要

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management の計画の最適化アドインを使用すると、マスター プランの計算を、Dynamics 365 Supply Chain Management および関連する SQL データベース以外で行うことができます。 計画の最適化機能に関連する利点として、マスター プランの実行時にパフォーマンスが向上し、SQL データベースへの影響が最小限に抑えられます。 迅速なプランニングを営業時間中に実行できるため、プランナーは要求またはパラメータの変更にすぐに対応できます。

計画の最適化を使用するには、計画の最適化アドインを Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトからインストールし、Supply Chain Management の計画の最適化機能を有効にする必要があります。 詳細については、[計画の最適化を開始する](get-started.md) を参照してください。

次の図は、営業時間内に計画の最適化を実行する利点を示しています。

![営業時間内に計画の最適化を実行する利点](media/PlanningOptimization1.png)

## <a name="improved-performance"></a>パフォーマンスの向上

長時間実行されるマスター プランに関連するシナリオでは、計画の最適化を使用できます。 非常に大量のデータを含む非常に高速な計算に特化して設計されています。 ハイパースケーラブルなマルチテナント サービスとして構築されているため、複数のインスタンスは同時に連携して計画を計算することができます。 さらに、計画サービスはマスター プランの負荷をシステムから除去し、サーバーの負荷を最小限に抑えるデータ ストリームと連携して機能します。

計画の最適化は、次の目標を達成するのに役立ちます。

- 短い実行時間で計画のパフォーマンスを向上させること。
- マスター プランの実行中に他のプロセスへの影響を軽減すること。
- より頻繁に計画を実行すること。 (日常の実行は制限されません。)
- 将来のビジネス成長によって計画のシステムが過負荷にならないこと。

## <a name="architecture-and-data-flow"></a>アーキテクチャとデータ フロー

LCS から計画の最適化アドインをインストールすると、計画の最適化サービスへの安全な接続が確立されます。 このサービスは、関連する Supply Chain Management インスタンスと同じデータ センターの国または地域にあります。 計画の最適化が設定されたら、マスター プランの実行時に、マスター データおよびトランザクション データが Supply Chain Management から計画の最適化サービスに送信されます。

計画の最適化アドインをアンインストールすると、計画の最適化サービスに関連するすべてのデータが削除されます。

### <a name="high-level-data-flow-for-regeneration-runs"></a>再生成実行のための高レベル データ フロー

1. Supply Chain Management クライアントは、計画の最適化から計画の実行を要求するためのシグナルを送信します。
2. 計画の最適化は、統合コネクタを介して必要なデータを要求します。
3. SQL データベースはコネクタを介して、設定、マスター、およびトランザクションのデータについて要求された情報を、計画の最適化に送信します。 コネクタは、Supply Chain Management と計画の最適化サービス間で情報を変換します。
4. 計画の最適化サービスでは、計画に関連するデータがメモリに保持され、必要な計算が行われます。
5. 計画の結果は、コネクタを介して Supply Chain Management データベースに送信されます。 この結果には、計画オーダーやペギング情報などの情報が含まれます。 計画の最適化では、計画の実行が完了したことを示すシグナルが、Supply Chain Management に送信されます。 また、関連するメッセージおよび警告を送信することもできます。

次の図はデータ フローを示します。

![再生成実行のためのデータ フロー](media/PlanningOptimization2.png)

## <a name="related-resources"></a>関連するリソース

[計画の最適化を開始する](get-started.md)

[計画の最適化フィット分析](planning-optimization-fit-analysis.md)

[計画の履歴と計画ログの表示](plan-history-logs.md)

[プランへのフィルターの適用](plan-filters.md)

[計画ジョブのキャンセル](cancel-planning-job.md)
