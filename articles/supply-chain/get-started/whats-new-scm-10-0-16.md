---
title: Dynamics 365 Supply Chain Management 10.0.16 のプレビュー (2021 年 2 月)
description: このトピックでは、Dynamics 365 Supply Chain Management 10.0.16 の新機能または変更された機能について説明します。
author: kamaybac
manager: annbe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-11-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 963979c9d24c275f77347ec5d682f318db18f915
ms.sourcegitcommit: be4b9d557511bbb43e71a93f2c3b23b5f1a4669d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "4626805"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10016-february-2021"></a>Dynamics 365 Supply Chain Management 10.0.16 のプレビュー (2021 年 2 月)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

このトピックでは、バージョン 10.0.16 の Microsoft Dynamics 365 Supply Chain Management プレビューの新機能または変更された機能について一覧表示します。 このバージョンには 10.0.689 のビルド番号が含まれており、次のように使用できます。

- **リリースのプレビュー:** 2020 年 11 月
- **リリースの一般提供 (手動更新):** 2021 年 1 月
- **リリースの一般提供 (自動更新):** 2021 年 2 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

このリリースでは次の機能が含まれています。 一覧表示された機能の一部はプレビューのままですが、他の機能はすでに一般提供されている可能性があります。 [リリース計画](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/planned-features) へのリンクに従って、各機能の公式リリース日を確認してください。

- [カスタマイズ可能な作業現場の実行インターフェイス](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/customizable-shop-floor-execution-interface)<br> - 詳細については、[生産現場の実行インターフェースを実行するデバイスを設定する](../production-control/production-floor-execution-setup.md)を参照してください。
- [Dynamics 365 Supply Chain Management の在庫の視覚化アドイン](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/inventory-visibility-add-in-dynamics-365-supply-chain-management-preview)<br> - 詳細については、[在庫の視覚化アドイン](../inventory/inventory-visibility.md)を参照してください。
- [元伝票明細行のライセンス プレートの検証](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/validate-license-plates-source-document-lines)<br> - 詳細については、[倉庫のコンフィギュレーションの概要](../warehousing/warehouse-configuration.md)を参照してください。
- [倉庫管理の出庫ワークロードのビジュアル化](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management--workload-visualization)<br> - 詳細については、[出庫ワークロードの視覚化](../warehousing/outbound-workload-visualization.md)を参照してください。

これらの機能のほとんどは、使用する前に[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して有効にする必要があります。

## <a name="new-and-updated-documentation-resources"></a>新しいドキュメント リソースおよび更新されたドキュメント リソース

次のヘルプ トピックが最近追加されたか大幅に更新されました。 前のセクションに示したように、このリリースで追加された新しい機能に関連するとは限りませんが、既存の機能をさらに活用するために役立つ場合があります。

- [制約ベースの製品コンフィギュレーションの属性ベースの販売価格](../pim/attribute-based-product-configurator.md)
- [雑費の自動配賦](../procurement/automatic-charges-allocation.md)
- [危険物の概要](../pim/hazmat-overview.md) (および関連トピック)
- [マスター プランの計画最適化への移行](../master-planning/new-master-planning-engine.md)
- [cXML 拡張機能の購入](../procurement/purchasing-cxml-enhancements.md)
- [コスト管理のトラブルシューティング](../cost-management/troubleshoot-costmanagement.md)
- [入庫倉庫操作のトラブルシューティング](../warehousing/troubleshoot-warehouse-inbound.md)
- [積荷構築と出荷のトラブルシューティング](../warehousing/troubleshoot-warehouse-loads-shipments.md)
- [マスター プランのトラブルシューティング](../master-planning/troubleshoot-masterplanning.md)
- [出庫倉庫操作のトラブルシューティング](../warehousing/troubleshoot-warehouse-outbound.md)
- [部分的なリリースと部分的な出荷に関するトラブルシューティング](../warehousing/troubleshoot-warehouse-partial-release-shipment.md)
- [製品コンフィギュレーターのトラブルシューティング](../pim/troubleshooting-productconfigurator.md)
- [製品情報のトラブルシューティング](../pim/troubleshooting-productinformation.md)
- [調達ワークフローのトラブルシューティング](../procurement/troubleshoot-procurementworkflows.md)
- [発注書のトラブルシューティング](../procurement/troubleshoot-purchaseorders.md)
- [価格、割引、契約、リベートのトラブルシューティング](../procurement/troubleshooting-pricediscountagreements.md)
- [製品受領書と請求書のトラブルシューティング](../procurement/troubleshooting-productreceiptinvoicing.md)
- [個別製造のトラブルシューティング](../production-control/troubleshoot-discretemanufacturing.md)
- [ピッキングと梱包のトラブルシューティング](../warehousing/troubleshoot-warehouse-picking-packing.md)
- [プロセス製造のトラブルシューティング](../production-control/troubleshoot-processmanufacturing.md)
- [倉庫管理での引当のトラブルシューティング](../warehousing/troubleshoot-warehouse-reservations.md)
- [販売注文のトラブルシューティング](../sales-marketing/troubleshooting-sales.md)
- [販売見積のトラブルシューティング](../sales-marketing/troubleshooting-salesquotation.md)
- [高度な倉庫管理へのアップグレードおよび移行のトラブルシューティング](../warehousing/troubleshoot-warehouse-upgrade-migration.md)
- [在庫アプリの接続の問題のトラブルシューティング](../warehousing/troubleshoot-warehouse-app-connection.md)
- [倉庫コンフィギュレーションのトラブルシューティング](../warehousing/troubleshoot-warehouse-configuration.md)
- [倉庫の補充のトラブルシューティング](../warehousing/troubleshoot-warehouse-replenishment.md)
- [倉庫の設定のトラブルシューティング](../warehousing/troubleshoot-warehouse-setup.md)
- [倉庫作業のトラブルシューティング](../warehousing/troubleshoot-warehouse-work.md)
- [プットアウェイ クラスター](../warehousing/putaway-clusters.md)
- [補充戦略](../warehousing/replenishment-strategies.md)
- [作業の分割](../warehousing/work-split.md)
- [場所ディレクティブの作業](../warehousing/create-location-directive.md)

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations アプリのプラットフォーム更新プログラム

Microsoft Dynamics 365 Supply Chain Management 10.0.16 には、Platform updates が含まれています。 詳細については、[Finance and Operations アプリのバージョン 10.0.16 (2020 年 10 月) のプラットフォーム アップデート](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-16.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

10.0.16 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=528995&dbType=3&qc=267a545fabd24e111868bedc16716f5713a785ed096cdb6209526f41631e41db)を参照してください

### <a name="dynamics-365-2020-release-wave-2-plan"></a>Dynamics 365: 2020 リリースのウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2020 リリース ウェーブ 2 プラン](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/index) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-supply-chain-management-features"></a>削除済みおよび非推奨の Supply Chain Management 機能

[Dynamics 365 Supply Chain Management の削除済みおよび非推奨の機能](removed-deprecated-features-scm-updates.md)トピックは、Supply Chain Management で削除または非推奨となる予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Supply Chain Management の削除済みまたは非推奨の機能](removed-deprecated-features-scm-updates.md)のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。
