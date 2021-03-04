---
title: Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operations バージョン 8.0 の新機能または変更された機能について説明します。 このバージョンは 2018 年 4 月にリリースされました。
author: tonyafehr
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: b265d51c-52d1-45c5-b578-64c5242c592a
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-09-30
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 2b5b79776b122a2c4e38825468823d96bf7b52c8
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797183"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-version-80-april-2018"></a>Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月) の新機能または変更された機能について説明します。 このバージョンは 2018 年 4 月にリリースされ、ビルド番号は 8.0.30 と 8.0.35 です。

ビジネス アプリケーションの最新の更新プログラムや、独自のアプリケーションと拡張機能をプラットフォームにビルドするための新しい機能を見つけるには、[Dynamics 365 2018 年春リリース計画](https://docs.microsoft.com/business-applications-release-notes/April18/release-overview)をダウンロードしてください。 リリース ノートでは、Dynamics 365 for Finance and Operations の新規または変更のいずれかの機能に関する詳細を提供します。

### <a name="introducing-dynamics-365-for-finance-and-operations"></a>Dynamics 365 for Finance and Operations の導入

ユーザーおよび開発者は、「Microsoft Dynamics 365 for Finance and Operations」という更新済の製品名を確認できます。 バージョン 8.0 では Dynamics 365 製品がさらに簡素化され、顧客とエコシステムの選択がさらに簡単になります。 今後 Microsoft は、個別エディション (Business Edition および Enterprise Edition) を提供しなくなるため、この Dynamics 365 アプリケーションの製品名は Microsoft Dynamics 365 for Finance and Operations になります。

## <a name="business-productivity"></a>業務の生産性

### <a name="alerts"></a>警告

クライアント ベースの警告機能により、請求書が支払われたときや顧客が住所を変更したときなど、ビジネス イベントに基づいて警告ルールを定義できます。 警告およびその作成方法の詳細については、[警告の概要](alerts-overview.md) を参照してください。

### <a name="optimization-advisor"></a>最適化アドバイザー

テレメトリを使用して、お客様のビジネス プロセスを分析し、最適化の可能性を探し、アプリケーション データを使用してその可能性を定量化し、ソリューションを推奨します。

### <a name="project-timesheet-mobile"></a>プロジェクト タイムシート モバイル

従業員は、プロジェクト タイムシートを作成して送信できます。 保存したお気に入りの使用機能と、以前のタイムシートからのコピー機能により、迅速で正確な時間の入力が容易になります。

### <a name="edit-default-project-fulfillment-hours"></a>既定のプロジェクトのフルフィルメント時間を編集

プロジェクト リソース管理者は、プロジェクトの予約調達のためのプロセスの一部として、既定の時間を編集できます。

### <a name="reserve-project-resources-past-the-task-end-date"></a>タスクの終了日が過ぎてからプロジェクト リソースを予約

プロジェクト リソースの管理者は、タスクの現在の計画終了日を過ぎたタスクでリソースをフルフィルメントすることができます。

### <a name="person-search-report"></a>個人検索レポート

Finance and Operations 内で担当者および個人データを検索することができます。

### <a name="data-sharing-for-customer-and-vendor-tables"></a>顧客および仕入先のテーブルのデータ共有

データは、顧客テーブルと仕入先テーブル、および複数の法人の多くの関連テーブルで共有することができます。

### <a name="one-voucher-deprecation"></a>1 つの伝票の廃止

財務仕訳帳 (一般仕訳帳、固定資産仕訳帳、仕入先支払仕訳帳など) の既存の機能を使用して、1 つの伝票のコンテキストで複数の補助元帳トランザクションを入力できます。 この機能を「1 つの伝票」と呼びます。 1 つの伝票機能により、決済、税計算、補助元帳の一般会計への調整、財務報告などの間に問題が発生します。 これらの問題のため、1 つの伝票機能は廃止されます。 ただし、この機能に依存する機能的なギャップがあるため、機能が一度に無効になることはありません。 代わりに、次のスケジュールを使用します。

- **18 年春リリース** – 機能は、一般会計パラメーターによって既定で、オフになります。 ただし、組織が単一伝票文書に記載されているビジネス シナリオ ギャップの範囲内にシナリオがある場合、機能をオンにできます。

    - 顧客が 1 つの伝票を必要としないビジネス シナリオがある場合、機能をオンにしないでください。 この機能が使用される場合、単一伝票文書に記載されている領域の「不具合」は修正されません。
    - 機能的なギャップのいずれかに必要な機能でない限り、 Microsoft Dynamics 365 Finance and Operations への統合に 1 つの伝票を使用しないでください。

- **18 年秋およびそれ以降のリリース** – 機能的なギャップが埋まります。 機能的なギャップが埋められた後、1 つの伝票の機能が完全にオフになります。

この機能の使用と廃止に関する詳細については、[1 つの伝票ドキュメント](https://docs.microsoft.com/dynamics365/unified-operations/financials/general-ledger/one-voucher)を参照してください。

## <a name="extensibility-and-customization"></a>拡張性およびカスタマイズ

### <a name="customizations-through-extensions-only"></a>拡張機能のみによるカスタマイズ

1 つのリリースから次へのカスタマイズの移行が、オーバーレイから拡張機能の使用に移動したことにより簡素化されています。

### <a name="extensibility-requests"></a>拡張機能の要求

お客様は、必要なシナリオのために製品に拡張サポートを追加するよう Microsoft に依頼することができます。 今回のリリースでは、この機能は Lifecycle Services (LCS) に移動されています。

### <a name="embedding-microsoft-power-apps-in-workspaces-and-forms"></a>ワークスペースおよびフォームに Microsoft Power Apps を埋め込む

Microsoft Power Apps を使用して、外部ソースからのデータを Finance and Operations のデータに埋め込みます。 Finance and Operations ページで PowerApp を埋め込む方法の詳細については、[PowerApps の埋め込み](embed-power-apps.md) を参照してください。

### <a name="custom-fields"></a>カスタム フィールド

組織は、コードなしの機能拡張経験を使用し、カスタム フィールドを追加してビジネス要件に合わせて自社アプリケーションをカスタマイズできます。 カスタム フィールドを作成および管理する方法の詳細については、[カスタム フィールドの作成と操作](user-defined-fields.md)を参照してください。

## <a name="integration"></a>統合 

### <a name="integration-with-dataverse"></a>Dataverse との統合

Dynamics 365 for Finance and Operations では、Finance and Operations と Dynamics 365 for Field Service の間、および Finance and Operations と Dynamics 365 for Project Service Automation の間のクロス アプリケーションの業務プロセスを有効にしました。 これらのシナリオは、拡張可能なデータ インテグレーター テンプレートと Dataverse を使用して構成され、クロス アプリケーション シナリオを実現します。

### <a name="integration-with-dynamics-365-for-field-service"></a>Dynamics 365 for Field Service との統合

データ インテグレーターを活用して、Field Service アクティビティが Finance and Operations の外で行われるシナリオをサポートするためのデータ統合を提供します。

### <a name="integration-with-dynamics-365-for-project-service-automation"></a>Dynamics 365 for Project Service Automation との統合

データ インテグレーターを活用することで、プロジェクトおよびリソース管理アクティビティが Finance and Operations の外で行われ、プロジェクト会計アクティビティが Finance and Operations で行われるシナリオをサポートします。

## <a name="improved-support-experiences"></a>サポート エクスペリエンスの強化

### <a name="telemetry-based-kb-recommendation"></a>テレメトリに基づく KB の推奨事項

実稼働環境からのテレメトリは、テナントに適用されるアプリケーション修正プログラムを識別するために使用できます。

### <a name="kb-recommendations-when-entering-a-support-case"></a>サポート案件を入力する際の KB の推奨事項

LCS では、テレメトリ駆動の KB の推奨事項を提供します。

### <a name="report-production-outage"></a>稼働停止のレポート

実稼動環境のサービスが低下または使用不可能になった場合、Microsoft サポートに問題をエスカレートを迅速かつ有効なチャンネルを提供します。

## <a name="supply-chain-management"></a>サプライ チェーン マネジメント

### <a name="vendor-collaboration--rfq-process"></a>仕入先コラボレーション - RFQ プロセス

機能強化により、誰が入札したかを容易に把握できます (仕入先または調達部門)。 詳細については、「[見積依頼 (RFQ)](../../../supply-chain/procurement/request-quotations.md)」を参照してください。

### <a name="partial-shipment-of-a-load-split-load"></a>積荷の部分的出荷 (分割積荷)

1 つの積荷または複数の積荷を完全に、または部分的に読み込めるように許可します。

### <a name="immediate-replenishment-of-locations"></a>場所の即時補充

補充テンプレートのある場所ディレクティブの明細行の配賦に失敗した場合、ウェーブ実行中に使用されます。 即時補充の詳細については、[即時補充](../../../supply-chain/warehousing/immediate-replenishment.md) を参照してください。

### <a name="reason-codes-added-to-warehouse-counting-and-adjustment"></a>倉庫の棚卸と調整に追加された理由コード

棚卸を実行するとき、および調整を行うときに理由コードを追加できます。 理由コードの詳細については、[在庫棚卸の理由コード](../../../supply-chain/warehousing/reason-codes-for-counting-journals.md) を参照してください。

### <a name="batch-balancing-enabled-for-advanced-warehousing-processes"></a>高度な倉庫管理プロセスが有効になっているバッチ バランシング

倉庫管理プロセスに対して設定されている製品にバッチ バランシング プロセスを利用できるようになりました (以前のリリースでは、倉庫管理プロセスに対して設定されていない製品にのみバッチ バランシング プロセスが有効になっていました)。 この機能拡張により、バッチ バランシング プロセスが完了した後に、ユーザーがピッキングに原料をリリースすることが可能になります。 バッチ バランシングの詳細については、「[バッチ バランシング](../../../supply-chain/production-control/batch-balancing.md)」を参照してください。

### <a name="analytical-workspaces-with-embedded-power-bi-for-cost-management"></a>原価管理のための Power BI が埋め込まれた分析ワークスペースです。

原価管理のための新しい分析ワークスペースは、原価管理およびコスト分析のワークスペースに埋め込まれます。 コンテンツ パックには、期首残高、期末残高、正味調達および正味使用量などの措置が含まれています。 在庫回転率、手持在庫日数、在庫の精度などの一連の計算メジャーも含まれています。 **原価管理** Power BI コンテンツは、**原価管理** および **コスト分析** ワークスペースで表示されます。 詳細については、[原価管理 Power BI コンテンツ](../../dev-itpro/analytics/cost-management-content-pack.md) を参照してください。

## <a name="globalization"></a>グローバリゼーション

### <a name="india-localization--project-and-upgrade"></a>インド ローカライズ – プロジェクトとアップグレード

ユーザーはプロジェクト管理および会計モジュールでインドの商品及びサービス税 (GST) を管理でき、AX 2012 の顧客は Dynamics 365 for Finance and Operations にアップグレードできます。

### <a name="enhanced-configurability"></a>拡張されたコンフィギュレーションの可能性

新機能にはインポートとテスト シナリオが含まれており、コーディングなしでコンフィギュレーションが可能になるより広範なサポートも含まれます。

## <a name="servicing-performance-and-deployment"></a>保守、パフォーマンス、展開

### <a name="improved-delivery-of-platform-and-financial-reporting-updates"></a>プラットフォームおよび財務レポート更新のデリバリーの強化

プラットフォームおよび財務レポートの更新は、オプションの更新プログラムではなく、Microsoft によって管理される継続的な更新になります。 この変更は、サービスの信頼性と可用性を向上させるとともに、最新の改善と修正を顧客に確実に提供することを目的としています。  プラットフォームと財務レポートの更新には、下位互換性があります。 詳細については、[Finance and Operations クラウド プラットフォームの毎月の更新に関するよく寄せられる質問](../../../dev-itpro/sysadmin/faq-platform-monthly-updates.md) を参照してください。

### <a name="upgrade-automation"></a>自動アップグレード

アップグレードの自動化により、非運用環境で LCS を使用して、顧客に対しメジャー バージョンのアップグレードをセルフ サービス操作として提供します。

### <a name="service-hardening"></a>サービスの強化

主要な業務プロセスの監視と警告を追加し、最も使用頻度の高いフォームのフォーム負荷パフォーマンスを改善します。

### <a name="lifecycle-services-sandbox-self-service-automation-and-rdp-lockdown"></a>Lifecycle Services サンドボックス セルフサービス自動化および RDP ロックダウン

サンドボックス セルフサービスの自動化では、リモート デスクトップを介したサンドボックス環境へのアクセスがなくても、データの移動、デバッグ工程、監視、および診断がサポートされています。 サンドボックス環境のリモート デスクトップ機能は使用されなくなります。 つまり、顧客は VM にアクセスするためにリモート デスクトップを使用する必要がなくなり、信頼性とセキュリティが向上します。

## <a name="compliance"></a>コンプライアンス

### <a name="general-data-protection-regulation-gdpr"></a>一般データ保護規則 (GDPR)

投資は、欧州のプライバシーに関する法律の要件に対応します。 準拠に役立つリソースを検索するには [Trust Center](https://www.microsoft.com/trustcenter/compliance/accessibility) を参照してください。

### <a name="accessibility-enhancements"></a>アクセシビリティの拡張機能

業界をリードするアクセシビリティ標準については [Trust Center](https://www.microsoft.com/trustcenter/compliance/accessibility) を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]