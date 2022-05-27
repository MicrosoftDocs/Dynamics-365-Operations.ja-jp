---
title: Dynamics 365 Supply Chain Management 10.0.23 (2022 年 1 月) の新機能と変更された機能
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management 10.0.23 の新機能または変更された機能について説明します。
author: kamaybac
ms.date: 10/15/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 86e33296fd8631082e47bf6814d8e5e716d9fa1b
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691473"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10023-january-2022"></a>Dynamics 365 Supply Chain Management 10.0.23 (2022 年 1 月) の新機能と変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management バージョン 10.0.23 の新機能または変更された機能について一覧表示します。 このバージョンには 10.0.1037 のビルド番号が含まれており、次のように使用できます。

- **リリースのプレビュー:** 2021 年 10 月
- **リリースの一般提供 (セルフ更新)**: 2021 年 12 月
- **リリースの一般提供 (自動更新):** 2022 年 1 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 *機能* 列には、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) へのリンクがあり、各機能の公式リリース日を確認できます。 *詳細情報* 列には、詳細情報や関連ドキュメントへのリンクが表示されます。 機能を有効にする方法を確認するには、*有効化* 列を参照してください。 機能管理の使用方法の詳細については [機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。 このトピックが最初に公開された後に、ビルドに加えた機能を含めるために、このトピックを更新することがあります。

| 機能領域 | フィーチャー | 詳細 |  に  によって有効化 |
|---|---|---|---|
| グローバル アドレス帳 | 住所の設定で国/地域ごとに既定の都道府県を定義する | グローバル アドレス帳の住所設定で国/地域ごとに既定の都道府県を定義できるようになりました。 既定の都道府県が設定されている場合は、その国/地域に新しい郡または市のレコードが作成される際、それが都道府県フィールドに入力された規定値になります。 また、[アドレス設定](../../fin-ops-core/fin-ops/organization-administration/global-address-book-address-setup.md?toc=/dynamics365/supply-chain/toc.json) も参照してください。 | 既定で有効になっています。 |
| 在庫&nbsp;および&nbsp;物流 | [Warehouse Management モバイル アプリのタスクの一時停止](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/park-tasks-warehouse-management-mobile-app) | [モバイル デバイス メニュー項目のステップの迂回を構成する](../warehousing/warehouse-app-detours.md) | 機能管理 (*Warehouse Management アプリの迂回*) |
| 在庫&nbsp;および&nbsp;物流 | [倉庫アプリのプロモーション フィールド](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [モバイル デバイスの手順に昇格したフィールドを構成する](../warehousing/warehouse-app-promoted-fields.md)| 機能管理 (*Warehouse Management アプリの昇格したフィールド*) |
| 製造 | [製造実行システム統合](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-systems-integration) | [サード パーティ製造システムとの統合](../production-control/mes-integration.md) | 機能管理 (*製造実行システム統合*) |
| 製造 | [生産現場の実行インターフェースの連産品と副産物に関するレポート](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | [生産現場の実行インターフェイスを作業者が使用する方法](../production-control/production-floor-execution-use.md) | 機能管理 (*生産フロア実行インターフェイスからの連産品と副産物を報告する*) |
| 計画 | [優先順位に基づく計画の計画最適化サポート](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-priority-based-planning) | [優先順位に基づく計画](../master-planning/planning-optimization/priority-based-planning.md) | 機能管理 (*計画最適化に対して優先順位によって推進される MRP のサポート*) |

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次のテーブルは、このリリースに含まれる機能拡張の一覧を示します。 これらの機能拡張は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) には記載されません。 ただし、これらの拡張機能が既存のカスタマイズや基本設定と競合しないように、各機能は (特に断りのない限り) 既定でオフになっています。

これらの機能のいずれかをオンまたはオフにする場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) で次のテーブルの *機能管理の機能名* 列に示されている名前を使用してリストする必要があります。

| モジュール | 機能管理の機能名 | 詳細 |
|---|---|---|
| 資産管理 | 作業指示書仕訳の経費の相手勘定 | この機能は、作業指示書の仕訳帳に一覧表示されている各経費に対して相手勘定を指定することができます。 通常は、仕入勘定を各経費に関連付けしますが、他の勘定タイプもサポートされています。 これは、**作業指示書の仕訳帳** ページの **経費** クイック タブに新しい 2 列 (**相手勘定のタイプ** と **相手勘定**) を追加します。|
| 原価管理 | 標準原価丸め再評価に関連する伝票を作成する | <p>在庫財務転記 (販売注文請求書や在庫トランザクションなど) を作成すると、この機能によって、関連する標準原価の丸め再評価用の別の伝票が作成され、それを関連する伝票として財務転記伝票に関連付けられます。</p><p>この機能がない場合は、同じ伝票転記の標準原価丸め再評価が記録されます。 再評価ではセッションまたはシステムの日付が使用されるのに対し、財務転記では転記日付が使用されるため、その動作により日付情報が競合する場合があります。</p> |
| 在庫および倉庫管理 | \[ロシア\] 受注の会計伝票の訂正フラグに従って、Storno 資産在庫トランザクションを転記する | この機能は、ロシアの貸方票定性機能に影響します。 これはロシア 受注の会計伝票の訂正フラグに応じて、逆資産在庫取引を計上します。 この機能を有効にした場合、在庫トランザクションの財務伝票の **訂正** フラグと在庫トランザクションで **Storno** フラグの間の不一致はこれ以上ありません。 |
| 在庫および倉庫管理 | (ロシア) 在庫残高回転率レポートの計算をバッチで実行する | Supply Chain Management の ロシアのローカライズの場合、*在庫残高回転率* レポートをバッチで実行して保存したり、以前生成したレポートを表示できます。 |
| 在庫および倉庫管理 | (ロシア) 在庫管理で国または地域固有のプライマリ フォームでローカル言語への翻訳を使用する | Supply Chain Management のロシア語ローカライズでは、この機能を使用して、次のロシア固有の在庫のプリントアウトで、製品/品目名および測定単位にロシア語の翻訳を使用できます:棚卸リスト (INV-3)、棚卸リスト (INV-5)、棚卸リスト (INV-6)。 |
| マスター プラン | 需要予測向け Azure Machine Learning Service | この機能により、Azure Machine Learning Service は履歴データに基づいて需要予測を生成できます。 詳細については、[需要予測の設定](../master-planning/demand-forecasting-setup.md) を参照してください。 |
| 調達 | 発注書更新履歴をクリーンアップする | この機能を使用すると、発注書の更新に関連する一時的な履歴レコードをクリーンアップできます。 **すべての発注書** ページのアクション ウィンドウに、**購買更新履歴のクリーンアップ** と呼ばれる 新しいボタンが追加されます。 この機能は、既定で有効になっています。 |
| 生産管理 | (プレビュー) 自動転記されたピッキング リストの倉庫対応材料の自動ピッキング | この機能を使用して、自動転記、派生/一括引き落とし済みピッキング リスト仕訳帳の、在庫分析コードの自動ピッキングと解決ができます |
| 生産管理 | 予定消費日と対する原材料の有効期限の検証 | この機能により、生産中に使用される原材料のバッチを引当する際に、バッチの有効期限が検証される方法が変更されます。 この機能を有効にすると、バッチ有効期限は、生産 BOM 明細行またはバッチ オーダーのフォーミュラ明細行で設定された予定消費日 (原材料の日付) に対して検証されます。 この機能を無効にすると、バッチ有効期限が、製造オーダーまたはバッチ オーダーの予定出荷日と対して検証されます (以前の日付)。 |
| 販売とマーケティング | 経過日数に基づいて販売更新履歴をクリーンアップする | この機能を使用すると、**販売更新履歴クリーンアップ** 定期処理タスクの実行時に保持するレコードの最大期間を設定できます。 古いレコードは削除されます。 これは、タスクが実行される日付を基準として常に年数が計算されるので、タスクを定期的に実行するために設定する場合に役立ちます。 この機能を使用しない場合、保持できる最も古いレコードに対する特定の日付だけを設定できます。 詳細については、[販売履歴データのクリーンアップをスケジュールする](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) を参照してください。 |
| 販売とマーケティング | "上位 100" の顧客レポートのパフォーマンスを向上する | この機能により、カスタム クエリを許可するのではなく、常にすべての顧客 (その用途) にわたってレポートを実行することで、**上位 100 人** の顧客レポートのパフォーマンスが向上します。 この機能を有効にすると、すべての **含めるレコード** 設定が **上位 100** レポート ダイアログで無効になります。 |
| 倉庫管理 | 出荷注文の倉庫へのリリースのスケール ユニットのサポート | この機能が有効な場合、出荷注文は、注文を履行するスケール ユニットにハブから直接リリースできます。 |

## <a name="new-and-updated-documentation-resources"></a>新しいドキュメント リソースおよび更新されたドキュメント リソース

次のヘルプ トピックが最近追加されたか大幅に更新されました。 これらのトピックは、前のセクションに示したように、このリリースで追加された新しい機能に関連するとは限りません。 ただし、これらの機能は既存の機能をさらに活用するために役立つ場合があります。

| 機能領域 | 新規または更新されたトピック |
|---|---|
| エンジニアリング変更管理 | エンジニアリング属性継承の機能については、[エンジニアリング属性とエンジニアリング属性の検索](../engineering-change-management/engineering-attributes-and-search.md) で説明されています。 |
| マスター プラン | [需要予測](../master-planning/planning-optimization/demand-forecast.md) および [予測の減少キーを使用したマスタ プラン](../master-planning/reduction-keys.md) では、減少キーの操作方法に関する情報が提供されます。 |
| マスター プラン | [品目の安全在庫フルフィルメント](../master-planning/safety-stock-replenishment.md) では、最小/最大キーの使用に関する詳細が表示するようになりました。 |
| マスター プラン | [在庫予測](../master-planning/inventory-forecast.md) では、予測の割り当てに関する詳細を表示するようになりました。 |
| マスター プラン | [供給スケジュール](../master-planning/supply-schedule.md) |
| 倉庫管理 | [グローバル モバイル デバイス パラメーター](../warehousing/mobile-device-parameters.md) |
| 倉庫管理 | [アンカー設定](../warehousing/anchoring.md) |
| 販売とマーケティング | これで、[会社間取引の設定](../sales-marketing/intercompany-trade-set-up.md) および関連トピックから、会社間取引の詳細が説明されるようになりました。 |
| 販売とマーケティング | [販売履歴クリーンアップ パフォーマンスの改善](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| 在庫管理 | 在庫の可視性のドキュメントは、[在庫の可視性アドインの概要](../inventory/inventory-visibility.md) および関連トピックから、展開および更新されています。 |
| 倉庫管理 | [モバイル デバイスのユーザー アカウント](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Microsoft Dynamics 365 Supply Chain Management 10.0.23 には、Platform updates が含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.23 のプラットフォーム更新プログラム (2021 年 11 月)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-23.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

10.0.23 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=627874&dbType=3&qc=9b7e01944eb8b43f9c3aac4be26811c27be205847d6d2a240424f34f7e722910) を参照してください。

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 および業界のクラウド: 2021年リリース ウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365 および業界のクラウド: 2021年リリース ウェーブ 2 プラン](/dynamics365-release-plan/2021wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-supply-chain-management-features"></a>削除済みおよび非推奨の Supply Chain Management 機能

[Dynamics 365 Supply Chain Management の削除済みおよび非推奨の機能](removed-deprecated-features-scm-updates.md)トピックは、Supply Chain Management で削除または非推奨となる予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Supply Chain Management の削除済みまたは非推奨の機能](removed-deprecated-features-scm-updates.md)のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
