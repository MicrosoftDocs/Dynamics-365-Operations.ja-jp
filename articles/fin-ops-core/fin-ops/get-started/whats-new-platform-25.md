---
title: Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 25 (2019 年 4 月) の新機能および変更点
description: このトピックでは、Dynamics 365 for Finance and Operation プラットフォーム更新プログラム 25 (2019 年 4 月) の新機能または変更された機能について説明します。
author: tonyafehr
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: Platform 25
ms.openlocfilehash: 5cfa47c07677ebf124dbb979a04b6a79115ce7e6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749179"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-platform-update-25-april-2019"></a>Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 25 (2019 年 4 月) の新機能および変更点

[!include [banner](../includes/banner.md)]


このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 25 の新機能または変更された機能について説明します。 このバージョンのビルド番号は 7.0.5222 です。 プラットフォーム更新プログラム 25 の詳細については [追加リソース](whats-new-platform-25.md#additional-resources) を参照してください。

## <a name="extensibility-enhancements"></a>拡張性の強化
プラットフォーム更新プログラム 25 に含まれる [プラットフォーム拡張機能の 2 番目の波](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-finance-operations/platform-extensibility2) は、2019 年 4 月リリース ノートにドキュメントされています。 そこには 14 の機能強化が詳述されており、強調する点の 1 つは InternalUseOnlyAttribute メソッドのコマンド チェーンが、警告だけで許可されることです。

## <a name="powerbicom-report-pinning"></a>PowerBI.com レポートの固定
アプリケーションに組み込まれている標準の分析レポートを PowerBI.com でホストされているカスタム ソリューションに置き換える組み込みツールを使用することにより、パワー ユーザー向け Web クライアントで利用可能なカスタマイズ オプションの柔軟性の向上を利用できます。 最新のプラットフォーム更新プログラムにより、パワー ユーザーはアプリケーション ワークスペースの標準レポートを PowerBI.com でホストされたレポートに置き換えることができます。 これらの更新プログラムはすぐにワークスペースの他のユーザーが利用できるようになり、標準ソリューションを置き換えます。 追加オプションには、元々アプリケーションとともにリリースされた分析レポートに戻す機能が含まれています。

## <a name="entity-store-in-azure-data-lake-public-preview"></a>Azure Data Lake のエンティティ格納 (パブリック プレビュー)
エンティティストアは、Power BI でレポートするための簡略化したトランザクション データを含む運用データ ウェアハウスです。 これで Azure Data Lake Storage Gen2 にあるエンティティ格納をステージできます。 データを操作するのに、他の Azure やサードパーティ製ツールに加え PowerBI.com を使用できます。 この機能が有効になると、エンティティ格納データは、Microsoft サブスクリプションでリレーショナル エンティティ格納データベースに入力されません。 代わりに、独自のサブスクリプションの Azure Data Lake ストレージ  Azure Data Lake Storage Gen2 アカウントに入力されます。 PowerBI.com およびその他の Azure ツールのすべての機能をエンティティ格納で使用できます。

この機能を有効にするには [Business Data Lake のエンティティ格納](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-finance-operations/erp-data-entity-store-byod-business-data-lake) を参照してください。

## <a name="trickle-feed-support-for-entity-store-in-azure-data-lake-public-preview"></a>Azure Data Lake でのエンティティ格納のトリクル フィードのサポート (パブリック プレビュー)
エンティティ格納が Azure Data Lake にステージされている場合は、トリクル フィードの更新プログラムを有効にするオプションがあります。 トリクル フィード オプションが有効の場合、トランザクション データは Dynamics 365 for Finance and Operations でコミットされるとすぐに独自の Azure Data Lake で更新されます。 このオプションを使用して、PowerBI.com や他のツールを使用したトランザクション データでリアルタイム レポートを可能にします。

## <a name="edit-analytical-workspace"></a>分析ワークスペースの編集
開発者に頼らずに必要なレポートを作成する権限をユーザーに与えることができます。 最新のプラットフォーム アップデートを使用して、組み込みアプリケーション ソリューションに対して中断を伴わずに機能拡張を行うことができます。 パワー ユーザーは、クライアントから離れたり開発者ツールを使用することなく、既成の分析ワークスペースを変更できます。 特定のセキュリティ権限を持つユーザーは、レポート ビジュアルを追加または変更したり既存のレポートに新しいページを追加できます。 これらの変更はレポートを表示するすべてのユーザーに適用されます。

## <a name="system-printer-management"></a>システム プリンターの管理
組み込みのシステム管理ツールを使用して、法人間でネットワーク プリンタを簡単に管理できます。 ひとつのビューを使用して、デバイスのプロパティを変更したりネットワーク プリンタを削除したりできます。 これらのツールは Dynamics 365 for Finance and Operations  アプリケーション内で利用可能なネットワーク プリンタ デバイスを設定するタスクを劇的に単純化します。

## <a name="client-alert-email-support"></a>クライアント警告電子メールのサポート
統合された変更追跡ツールで業務データを常に把握します。 最新のプラットフォーム更新では、イベントによってトリガーされたときに、内部および外部の取引先担当者の事前定義グループに電子メール通知を自動的に送信するアラート ルールを作成できます。 Finance and Operations により、データのフィルタ処理されたビューを監視するためのカスタム アラート ルールを定義できます。 詳細については [電子メールによるクライアント警告通知](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/alert-email-notifications) を参照してください。

## <a name="client-alert-sub-table-field-tracking"></a>クライアント警告サブ テーブル フィールドの追跡
最新のプラットフォーム更新リリースには、子テーブルから供給されたフィールドに対する更新を監視する警告ルールを作成する機能が含まれます。 以前、オプションはルート データ ソースから提供されるフィールドに限定されていました。 現在は子テーブルのものも含め、ユーザーに表示されるすべてのフィールドに対して警告ルールを定義できます。

## <a name="azure-blob-storage-as-an-endpoint-for-business-events-private-preview"></a>ビジネス イベントのエンド ポイントとしての Azure Blob Storage (プライベート プレビュー)
Azure Blob Storage はビジネス イベントのエンド ポイントとして構成することができます。 これによりサポートされている既存の Azure エンドポイントの種類のセットが追加され、統合シナリオの選択肢が広がります。

ビジネス イベントについての詳細は [ビジネス イベントの概要](../../dev-itpro/business-events/home-page.md) を参照してください。 

> [!Note]
> ビジネス イベント機能はプライベート プレビューとして使用できます。 その機能が一般に利用可能になる時期については[リリース計画](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-finance-operations/planned-features)を参照してください。 

## <a name="batch-jobs-single-scheduler"></a>バッチ ジョブの単一スケジューラ
バッチ フレームワークでは、バッチ スケジューリング機能を最適化するための改善が行われています。 一度に有効になるバッチスケジューラは１つだけであり、これによってバッチテーブルの競合が減少し、スループットが向上する場合があります。 これはプラットフォーム更新プログラム 25 では既定で有効です。

## <a name="batch-jobs-enhanced-forms"></a>バッチ ジョブ拡張フォーム
**バッチ ジョブ** フォームは生産性の向上し、ユーザー エクスペリエンスを高めるために拡張されています。 ユーザーは拡張形式とレガシ形式を切り替えることができます。 詳細については、[拡張バッチ フォーム](../../dev-itpro/sysadmin/enhanced-forms.md)を参照してください。
さらに、保存されているビューに対するサポートが追加され、将来のプラットフォーム更新プログラムでリリースされる予定です。 保存されているビューについては [リリース計画](https://docs.microsoft.com/business-applications-release-notes/april19/dynamics365-finance-operations/saved-views)を参照してください。

## <a name="batch-jobs-alerts-and-notifications"></a>バッチ ジョブの警告および通知
アクション センターでバッチ ジョブの通知を確認できます。 これらの通知はバッチ イベントについて欠かさず知らせます。 バッチ ジョブが終了したとき、エラーで終了したとき、またはキャンセルされたときに警告ルールを有効化できます。 警告を電子メールで送信するか、アクション センターにポップアップ通知として表示するかどうかを選択できます。 詳細については、[警告の設定](../../dev-itpro/sysadmin/alerts.md) 参照してください。

## <a name="additional-resources"></a>追加リソース

### <a name="platform-update-25-bug-fixes"></a>プラットフォーム アップデート 25 のバグ修正プログラム
プラットフォーム更新 25 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、この [KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=299594&dbType=3&qc=cd4a0699eeae081b2b715d75b33ba6024dce2576563a84015bf60ed3509420a5)を参照してください。

### <a name="dynamics-365-april-19-release-notes"></a>Dynamics 365 2019 年 4 月 リリース ノート
当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2019 年 4 月リリース ノートをご覧ください](https://docs.microsoft.com/business-applications-release-notes/April19/index)。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能
[Finance and Operations の削除または廃止された機能](../../dev-itpro/migration-upgrade/deprecated-features.md) トピックでは、Dynamics 365 for Finance and Operations の削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Finance and Operations の削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]