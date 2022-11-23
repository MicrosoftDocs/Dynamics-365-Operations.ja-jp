---
title: Inventory Visibility アドインの概要
description: この記事では、Inventory Visibility とその機能について説明します。
author: yufeihuang
ms.date: 11/04/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dd790bcaada0c1a05e46b4edacaa31fc4e15be92
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762810"
---
# <a name="inventory-visibility-add-in-overview"></a>Inventory Visibility アドインの概要

[!include [banner](../includes/banner.md)]

Inventory Visibility Add-in (*Inventory Visibility サービス* とも呼ばれる) は、すべてのデータ ソースとチャネルでリアルタイムの手持在庫変更の転記と可視性の追跡を可能にする、独立した高度にスケーラブルなマイクロサービスを提供します。 次のリストを含む (ただし、限定はされない) 機能を使用して、グローバル在庫を管理できるプラットフォームを提供します:

- Supply Chain Management またはサード パーティー ロジスティクス データ ソース (注文管理システム、サード パーティ エンタープライズ リソース プランニング \[ERP\] システム、販売時点管理 \[POS\] システム、倉庫管理システムなど) を Inventory Visibility サービスに接続することで、すべてのデータ ソース、倉庫、および場所で最新の在庫ステータス (手持、注文済、購買済、輸送中、返品済、検査済など) を一元的に追跡します。
- 手持在庫の有無や不足を照会し、Inventory Visibility サービスを直接呼び出すことによって即時応答を取得します。
- 特に需要が異なるチャネルから来ている場合は、Inventory Visibility サービスでリアルタイムの仮引当を行うことで、過剰販売を回避します。
- 現在または次の入荷予定日を正確に提供することで、確約された注文と顧客の期待をより適切に管理し、オムニチャネルの納期回答可能在庫 (ATP) 機能で予想される注文の履行日を計算できるようにします。

## <a name="extensibility"></a>拡張性

データの入力および出力が Microsoft アプリケーションに限定されないので、Inventory Visibility サービスは高度な拡張性があります。 外部システムは、RESTful アプリケーション プログラミング インターフェイス (API) を使用してサービスにアクセスできます。 Supply Chain Management データ ソースおよび分析コードに対して用意されている既成のマッピングを使用する他に、構成アプリを使用して追加のデータ ソース、在庫ステータス メジャー (Inventory Visibility サービスでは *物理的測定* と呼ばれる)、および在庫分析コードを設定することで、Inventory Visibility を複数のサード パーティ システムと統合できます。 これにより、柔軟にクエリを実行し、複数のデータ ソースおよび定義済の在庫分析コードを変更できます。

また、Inventory Visibility は Microsoft Dataverse に基づいて構築されているため、そのデータを使用して Power Apps を作成および統合できます。 Power BI を使用して、業務要件に合うカスタマイズされたダッシュボードを作成することもできます。

## <a name="scalability"></a>スケーラビリティ

Inventory Visibility サービスは、データ量に応じて拡張または縮小できます。 スケーラビリティ エクスペリエンスは、ほとんどシームレスであり、トランザクション データ量の自動検出と評価に基づいて Microsoft プラットフォーム チームによって実行されます。

次の図では、Inventory Visibility アーキテクチャを表示します。

[<img src="media/inventory-visibility-architecture.png" alt="Inventory Visibility architecture." title="Inventory Visibility アーキテクチャ" width="720" />](media/inventory-visibility-architecture.png)

## <a name="feature-highlights"></a>機能の特徴

### <a name="get-a-global-view-of-real-time-inventory"></a>リアルタイム在庫のグローバル表示の取得

Inventory Visibility により、すべてのチャネル、場所、倉庫で、常に最新の在庫数量にアクセスすることができます。 在庫レコードを取得する必要がある場合、日々の運用業務をサポートするために使用すると非常に効果的です。 現物手持在庫、販売数量、および購入数量は、すべてすぐに使用できます。 必要に合じて他の現物在庫メジャー (返品済、検査済、転記済データなど) を構成して、その詳細をリアル タイムで取得することもできます。 Inventory Visibility により、何百万もの在庫変更の転記を効率的に処理できます。 このデータは、データが転記される間隔に応じて、サービス内の最新の在庫数量を即座に、1 秒または 1 分あたりに集計および反映できます。 詳細については、[Inventory Visibility のパブリック API](inventory-visibility-api.md) を参照してください。

### <a name="central-inventory-adjustment"></a>セントラル在庫調整

Inventory Visibility により、外部システムは API を呼び出して在庫変更を転記できます。 変更内容は、即座に Inventory Visibility に反映されます。 したがって、手持在庫は即座に差し引かれます。

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>すべての注文チャネルで過剰販売を回避するための仮引当

*仮引当* を使用すると、注文または需要を満たすために特定の数量を割り当てるか、フラグを設定できます。 仮引当は現物在庫には影響しませんが、*引当可能* 在庫数量から差し引かれ、今後の注文履行のために更新された数量を提供します。 この機能は、Systems of Record エンタープライズ リソース プランニング (ERP) システムの外部にある 1 つ以上のチャネルまたはデータ ソースから販売リクエストや注文がビジネスに入る場合に役立ちます。

Inventory Visibility サービスで仮引当を使用しない場合は、注文が ERP システムに同期されて処理されるまで待機して、現物在庫数量の更新を取得する必要があります。 通常、このプロセスには膨大な待ち時間があります。 ただし、販売チャネルで販売リクエストまたは注文が生成されるたびに仮引当は即座に有効になります。 そのため、オムニチャネル注文が最終的に ERP システムに到達したときに相互に干渉しないようにすることで、過剰販売の状況を回避できます。 仮引当では、確約したすべての注文を確実に履行することもできます。 したがって、顧客の期待に応え、顧客のロイヤリティを維持することができます。 詳細については、[Inventory Visibility 引当](inventory-visibility-reservations.md) を参照してください。

### <a name="immediate-response-of-atp-quantity-and-dates"></a>ATP 数量と日数の即時応答

企業が次の目標を達成するのに役立つため、近い将来の予測在庫 (供給、需要、および予測される手持の詳細を含む) の可視化が重要です。

- 在庫レベルを最小化して、在庫管理コストを削減します。
- 社内での注文処理を容易にし、販売担当者が発注された製品の在庫状況に基づいて、出荷日と配送日を計算できるようにします。
- 次の入荷予定日を提示することで、顧客が在庫切れの品目をいつ入手できるようになるかについての透明性を提供します。

ATP 機能は、日々の注文フルフィルメント プロセスに簡単に導入できます。 最も重要なのは、他の Inventory Visibility の提供と同様に、ATP 機能が *グローバルでリアルタイム* であることです。 したがって、すべてのビジネス チャネルとデータ ソースをカバーする完全な在庫状況クエリを含む複数の ATP 計算式を設定できます。 詳細については、[Inventory Visibility の手持変更スケジュールと納期回答可能在庫](inventory-visibility-available-to-promise.md) を参照してください。

### <a name="preallocate-your-stock-to-important-channels-or-customers-with-inventory-allocation"></a>在庫配賦を使用した重要なチャネルまたは顧客への在庫の事前割り当て

Inventory Visibility 配賦機能を使用すると、重要なチャネル、顧客グループ、または場所の貴重な在庫を保護し、リングフェンスすることができます。 在庫を割り当て後、在庫消費が割り当てられたプールに制限され、プール内に残っている数量はほぼリアルタイムで差し引かれ、まだ消費可能な数量を反映します。 詳細については、[Inventory Visibility の在庫配賦](inventory-visibility-allocation.md) を参照してください。

### <a name="compatibility-with-wms-items"></a>WMS 品目との互換性

Microsoft は、すぐに使用できる倉庫管理プロセス (WMS) との統合を提供することを目指しており、WMS の顧客も Inventory Visibility サービスの利点を享受できます。 2022 ウェーブ 1 リリース (3 月のパブリック プレビュー) により、在庫サービスは WMS 品目の手持クエリと ATP をサポートします。 仮引当と配賦機能は、WMS の顧客に対して次のサイクルでサポートされます。 詳細については、[WMS 品目に対応した Inventory Visibility](inventory-visibility-whs-support.md) を参照してください。

次の図は、既存の機能の高レベルの概要、およびこれらの機能をデータ フローに配置する方法を示しています。

[<img src="media/inventory-visibility-feature-overview.png" alt="Inventory Visibility feature overview." title="Inventory Visibility 機能の概要" width="720" />](media/inventory-visibility-feature-overview.png)

## <a name="licensing"></a>ライセンス

Inventory Visibility サービスは次のバージョンで使用できます:

- **Microsoft Dynamics 365 Supply Chain Management 向け Inventory Visibility アドイン** – 有効な Supply Chain Management ライセンスを持つ企業の場合、追加コストなしで Inventory Visibility を利用できます。 Inventory Visibility は Microsoft Power Platform に基づくため、Microsoft Power Platform ストレージ容量と API の制限の対象となります。 Supply Chain Management ライセンスには、既定のストレージと API の容量が含まれている必要があります。 より多くのストレージと API の容量が必要な場合は、プロフェッショナル ライセンスを購入できます。 既定の API 割り当てとプロフェッショナル ライセンスの詳細については、[要求の制限と割り当て](/power-platform/admin/api-request-limits-allocations) と [Microsoft Power Platform ライセンスの概要](/power-platform/admin/pricing-billing-skus) を参照してください。 既定のストレージと API 割り当てで、今日から Inventory Visibility アドインを試すことができます。 インストールの詳細については、[Inventory Visibility のインストールと設定](inventory-visibility-setup.md) を参照してください。 想定される API とストレージの使用状況が標準の割り当てを超えている場合は、販売担当者に連絡して、例外としてプラットフォーム チームに連絡するよう依頼できます。
- **IOM のコンポーネントとしての Inventory Visibility サービス** – このバージョンは、Supply Chain Management を ERP システムとして使用していない Intelligent Order Management (IOM) の顧客または企業向けです。 ライセンスは、Intelligent Order Management バンドルに含まれます。 詳細については、[Intelligent Order Management の概要](/dynamics365/intelligent-order-management/overview) を参照してください。

## <a name="inventory-visibility-terminology"></a>Inventory Visibility 用語

Inventory Visibility アドインを使用する場合は、次の概念と用語を理解することが重要です:

- **データ ソース** – データ ソースは、データの元となるシステムを表します。
- **分析コード** – 分析コードは、製品の特性を特定します。 保管分析コード (サイトや倉庫など) や製品分析コード (色、サイズ、スタイルなど) です。
- **現物メジャー** – 現物メジャーは、さまざまな在庫ステータス (手持在庫、購買済、注文中、販売済など) を測定する数量です。
- **計算メジャー** – 計算メジャーは、一連の現物メジャーから計算される定量的な尺度です。 たとえば、*引当可能合計数* 計算メジャーは、*手持在庫* + *購買済* – *注文中* – *売却済* として計算されます。
- **パーティション** – パーティションは Inventory Visibility で受け取ったデータを配分する方法に関する階層を定義します。 現在、既定のパーティションはサイトと場所です。
- **インデックス階層** – インデックス階層により、在庫のクエリ方法、およびより詳細な結果の取得方法をさらに定義します。

これらの用語と概念の詳細については、[Inventory Visibility の構成](inventory-visibility-configuration.md) を参照してください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
