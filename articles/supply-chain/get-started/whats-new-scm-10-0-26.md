---
title: Dynamics 365 Supply Chain Management 10.0.26 (2022 年 5 月) の新機能および変更された機能
description: この記事では、Microsoft Dynamics 365 Supply Chain Management 10.0.26 の新機能または変更された機能について説明します。
author: kamaybac
ms.date: 03/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: db8799aba8095c8144d878c96590e8d90276726b
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428203"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10026-may-2022"></a>Dynamics 365 Supply Chain Management 10.0.26 (2022 年 5 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Supply Chain Management バージョン 10.0.26 の新機能または変更された機能について一覧表示します。 このバージョンには 10.0.1192 のビルド番号が含まれており、次のように使用できます。

- **リリースのプレビュー:** 2022 年 3 月
- **リリースの一般提供 (自己更新):** 2022 年 4 月
- **リリースの一般提供 (自動更新):** 2022 年 5 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 この記事が最初に公開された後に、ビルドに加えた機能を含めるために、この記事を更新することがあります。

| 機能領域 | フィーチャー | 詳細 |  に  によって有効化 |
|---|---|---|---|
| 在庫および物流 | [高度な倉庫管理品目をサポートする在庫可視性の手持在庫に対するクエリ](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-visibility-support-advanced-warehouse-management) | [WMS 品目に対応した在庫可視化](../inventory/inventory-visibility-whs-support.md) | 機能管理:<br>*在庫可視化で在庫品目を有効化* |
| 在庫および物流 | [在庫の可視化アドインの納期回答可能在庫](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/available-to-promise-inventory-visibility-add-in) | [Inventory Visibility の手持変更スケジュールと納期回答可能在庫](../inventory/inventory-visibility-available-to-promise.md) | サービス コンフィギュレーションによって有効 |
| 製造 | [生産現場の実行インターフェイスの CW 品目](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/catch-weight-items-production-floor-execution-interface) | [生産現場の実行インターフェイスを作業者が使用する方法](../production-control/production-floor-execution-use.md) | 機能管理:<br>*生産現場の実行インターフェイスからの CW 品目に関するレポート* |
| 製造 | 生産現場の実行インターフェース上の [自分の職務] タブ | [生産現場の実行インターフェイスを作業者が使用する方法](../production-control/production-floor-execution-use.md) | 機能管理:<br>*生産現場の実行インターフェース上の [自分の職務] タブ* |

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能拡張は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) には記載されません。 ただし、これらの拡張機能が既存のカスタマイズや基本設定と競合しないように、各機能は (特に断りのない限り) 既定でオフになっています。

これらの機能をオンまたはオフにする場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) で実行する必要があります。

| モジュール | 機能管理の機能名 | 詳細 |
|---|---|---|
| 調達 | 受領書および仕入先請求書に対して在庫製品の登録数量と非在庫製品の残余を転記する | この機能により、仕入先請求書や発注書に対する入庫しない製品 (サービスなど) の数量の転記方法が変更されます。 この機能は、入庫および仕入先請求書を転記する場合の *登録された数量および非在庫製品* オプションの動作を、販売梱包明細の数量を転記するときに既に指定されている *登録された数量とサービス* 数量オプションの動作に合わせて変更することにより修正します。<br><br>*登録済数量およびサービス数量* オプションを使用して製品入庫または仕入先請求書を転記すると、システムは、在庫製品の登録数量を転記し、在庫されていない製品の残りの数量 (サービスとサービス以外の両方を含む) を転記します。 この機能がない場合は、在庫製品の登録数量 (在庫品目として設定されたサービスを含む) は転記されますが、在庫のないサービス製品の注文済数量が常に転記されます (さらに、*サービス* タイプではない在庫のない製品は無視されます)。 |
| 調達 | 会社間販売および発注書明細行の追跡用分析コードを同期化する | この機能により、シリアル番号とバッチ番号の追跡分析コードを、会社間販売注文書明細行と会社間購買注文明細行間で同期するかどうかを制御できます。 また、顧客および仕入先の **会社間** 設定ページの **発注書ポリシー** タブと **販売注文ポリシー** タブに新しい設定が追加されます。 また、関連する多くの関連設定や関連する設定の名前が更新されます。<br><br>倉庫管理プロセス (WMS) を使用している場合は、この機能ではバッチとシリアル番号が対象宛先予約階層の場所より上にある場合にのみ、同期されることに注意してください。 |
| 製品情報管理 | 製品属性値のクリーンアップ | この機能により、**製品属性値のクリーンアップ** という定期的なタスクが追加され、製品カテゴリを介して製品に関連付けられなくなった製品属性値レコードがクリーンアップされます。 |
| 在庫および倉庫管理 | (ロシア) WMS 対応品目を含む発注書に対して GTD を発行する際に不一致を回避する | この機能はロシアのローカライズ専用です。 この機能は、倉庫管理プロセス (WMS) が有効になっている品目を含む輸入発注書に対してロシア関税申告番号 (GTD) を発行するときに発生する不一致を回避します。 GTD 発行プロセスでは、カスタム仕訳帳に含まれる請求書に関連する在庫トランザクションの一部の在庫分析コード値を変更します。その結果、発注書の作業レコードと購買の在庫トランザクション間に不一致が生じます。 この機能が有効な場合、GTD 発行プロセスではそのような不一致を解消する調整作業を生成します。 |
| 倉庫管理 | GS1 バーコードの拡張パーサー | この機能により、GS1 記号データ用拡張パーサーの使用を有効にします。 新しいパーサーは、GS1 記号を解析するための GS1 一般仕様アルゴリズムを実装し、データの正確性を確認するためのより強力な検証機能を備えています。 詳細については、[GS1 バーコード スキャニング](../warehousing/gs1-barcodes.md) をご覧ください。 |
| 倉庫管理 | 倉庫管理アプリケーション - 空白の GTD | この機能はロシアのローカライズ専用です。 このオプションを使用すると、Warehouse Management モバイル アプリを使用する作業者は、必要に応じて [ロシア関税申告番号] 番号 (GTD) を空白のままにできます。 GTD 追跡用分析コードで空白の値を許可設定している場合、手持ち在庫がある場合に在庫操作の GTD の在庫操作に空白の値を使用できるようになります。 |

## <a name="new-and-updated-documentation-resources"></a>新しいドキュメント リソースおよび更新されたドキュメント リソース

次のヘルプ記事を最近追加、または大幅に更新しました。 これらの記事は、前のセクションに示したように、このリリースで追加された新しい機能に関連するとは限りません。 ただし、これらの機能は既存の機能をさらに活用するために役立つ場合があります。

| 機能領域 | 新規または更新された記事 |
|---|---|
| 原価管理 | 更新された例と図が、次の各記事に追加されました。<ul><li>[現物価格とマーキングを使用した FIFO](../cost-management/fifo-physical-value-marking.md)</li><li>[現物価格とマーキングを使用した LIFO](../cost-management/lifo-physical-value-marking.md)</li><li>[現物価格とマーキングを使用した LIFO 日付](../cost-management/lifo-date-physical-value-marking.md)</li><li>[移動平均原価価格](../cost-management/running-average-cost-price.md)</li><li>[現物価格とマーキングを使用した加重平均](../cost-management/weighted-average-physical-value-marking.md)</li></ul> |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Microsoft Dynamics 365 Supply Chain Management 10.0.26 には、Platform updates が含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.26 のプラットフォーム更新プログラム (2022 年 5 月)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-26.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

10.0.26 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864) を参照してください。

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 1 プラン](/dynamics365-release-plan/2022wave1/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-supply-chain-management-features"></a>削除済みおよび非推奨の Supply Chain Management 機能

[Dynamics 365 Supply Chain Management の削除済みおよび非推奨の機能](removed-deprecated-features-scm-updates.md)の記事は、Supply Chain Management で削除または非推奨となる予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Supply Chain Management の削除済みまたは非推奨の機能](removed-deprecated-features-scm-updates.md)の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

