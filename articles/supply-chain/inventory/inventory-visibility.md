---
title: Inventory Visibility アドインの概要
description: この記事では、在庫の可視化とその機能について説明します。
author: yufeihuang
ms.date: 03/18/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 274f9b368a6074725d1938de5f2172d2810a5985
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066643"
---
# <a name="inventory-visibility-add-in-overview"></a>在庫可視化アドインの概要

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

## <a name="feature-highlights"></a>機能の特徴

### <a name="get-a-global-view-of-real-time-inventory"></a>リアルタイム在庫のグローバル表示の取得

Inventory Visibility により、すべてのチャネル、場所、倉庫で、常に最新の在庫数量にアクセスすることができます。 在庫レコードを取得する必要がある場合、日々の運用業務をサポートするために使用すると非常に効果的です。 現物手持在庫、販売数量、および購入数量は、すべてすぐに使用できます。 必要に合じて他の現物在庫メジャー (返品済、検査済、転記済データなど) を構成して、その詳細をリアル タイムで取得することもできます。 Inventory Visibility により、何百万もの在庫変更の転記を効率的に処理できます。 このデータは、データが転記される間隔に応じて、サービス内の最新の在庫数量を即座に、1 秒または 1 分あたりに集計および反映できます。 詳細については、[Inventory Visibility のパブリック API](inventory-visibility-api.md) を参照してください。

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>すべての注文チャネルで過剰販売を回避するための仮引当

*仮引当* を使用すると、注文または需要を満たすために特定の数量を割り当てるか、フラグを設定できます。 仮引当は現物在庫には影響しませんが、*引当可能* 在庫数量から差し引かれ、今後の注文履行のために更新された数量を提供します。 この機能は、Systems of Record エンタープライズ リソース プランニング (ERP) システムの外部にある 1 つ以上のチャネルまたはデータ ソースから販売リクエストや注文がビジネスに入る場合に役立ちます。

Inventory Visibility サービスで仮引当を使用しない場合は、注文が ERP システムに同期されて処理されるまで待機して、現物在庫数量の更新を取得する必要があります。 通常、このプロセスには膨大な待ち時間があります。 ただし、販売チャネルで販売リクエストまたは注文が生成されるたびに仮引当は即座に有効になります。 そのため、オムニチャネル注文が最終的に ERP システムに到達したときに相互に干渉しないようにすることで、過剰販売の状況を回避できます。 仮引当では、確約したすべての注文を確実に履行することもできます。 したがって、顧客の期待に応え、顧客のロイヤリティを維持することができます。 詳細については、[在庫の視覚化引当](inventory-visibility-reservations.md) を参照してください。

### <a name="immediate-response-of-atp-dates-confirmation"></a>ATP 日付確認の即時応答

企業が次の目標を達成するのに役立つため、近い将来の予測在庫 (供給、需要、および予測される手持の詳細を含む) の可視化が重要です。

- 在庫レベルを最小化して、在庫管理コストを削減します。
- 社内での注文処理を容易にし、販売担当者が発注された製品の在庫状況に基づいて、出荷日と配送日を計算できるようにします。
- 次の入荷予定日を提示することで、顧客が在庫切れの品目をいつ入手できるようになるかについての透明性を提供します。

ATP 機能は、日々の注文フルフィルメント プロセスに簡単に導入できます。 最も重要なのは、他の Inventory Visibility の提供と同様に、ATP 機能が *グローバルでリアルタイム* であることです。 したがって、すべてのビジネス チャネルとデータ ソースをカバーする完全な在庫状況クエリを含む複数の ATP 計算式を設定できます。 詳細については、[Inventory Visibility の手持変更スケジュールと納期回答可能在庫](inventory-visibility-available-to-promise.md) を参照してください。

### <a name="compatibility-with-warehouse-management-processes-wms-items"></a>倉庫管理プロセス (WMS) 品目との互換性

Microsoft は、すぐに使用できる倉庫管理プロセス (WMS) との統合を提供することを目指しており、WMS の顧客も在庫可視化サービスの利点を享受できます。 2022 ウェーブ 1 リリース (3 月のパブリック プレビュー) により、在庫サービスは WMS 品目の手持クエリと ATP をサポートします。 仮引当と配賦機能は、WMS の顧客に対して次のサイクルでサポートされます。 詳細については、[WMS 品目に対応した Inventory Visibility](inventory-visibility-whs-support.md) を参照してください。

## <a name="licensing"></a>ライセンス

Inventory Visibility サービスは次のバージョンで使用できます:

- **Microsoft Dynamics 365 Supply Chain Management 向け Inventory Visibility Add-in** – 有効な Supply Chain Management ライセンスを持つ企業の場合、追加のライセンス コストなしで Inventory Visibility を利用できます。 今日からお試しいただけます。 インストールの詳細については、[Inventory Visibility のインストールと設定](inventory-visibility-setup.md) を参照してください。
- **IOM のコンポーネントとしての Inventory Visibility サービス** – このバージョンは、Supply Chain Management を ERP システムとして使用していない Intelligent Order Management (IOM) の顧客または企業向けです。 ライセンスは IOM バンドルに含まれています。 詳細については、[Intelligent Order Management の概要](/dynamics365/intelligent-order-management/overview) を参照してください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
