---
title: Dynamics 365 Supply Chain Management 10.0.28 のプレビュー (2022 年 8 月)
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management 10.0.28 の新機能または変更された機能について説明します。
author: kamaybac
ms.date: 05/27/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 306ff9be80c7a7a947b9132e3c9b4b9ec799b265
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813124"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10028-august-2022"></a>Dynamics 365 Supply Chain Management 10.0.28 のプレビュー (2022 年 8 月)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management プレビュー バージョン 10.0.28 の新機能または変更された機能について一覧表示します。 このバージョンのビルド番号は 10.0.1264 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 5 月
- **リリースの一般提供 (手動更新):** 2022 年 7 月
- **リリースの一般提供 (自動更新):** 2022 年 7 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 このトピックが最初に公開された後に、ビルドに追加された機能を含めるために、このトピックを更新することがあります。

| 機能領域 | フィーチャー | 詳細 |  に  によって有効化 |
|---|---|---|---|
| 在庫および物流 | [サード パーティ配送業者の陸揚原価統合エンティティ](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/landed-cost-integration-third-party-freight-forwarders) | [陸揚原価エンティティの概要](../landed-cost/landed-cost-entities-overview.md) | 既定で有効 |
| 計画 | [有効期限の最適化サポートの計画](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-shelf-life) | 間もなく公開 <!-- KFM: Vendor is preparing this. Expected May 20. --> | 既定で有効 |

<!-- KFM: Confirm status of this feature:
| Planning | [Demand Driven Material Requirements Planning (DDMRP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/demand-driven-material-requirements-planning-ddmrp) | Coming soon | Feature management:<br>*(Preview) DDMRP for Planning Optimization* | -->

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能拡張は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) には記載されません。 ただし、これらの拡張機能が既存のカスタマイズや基本設定と競合しないように、各機能は (特に断りのない限り) 既定でオフになっています。

これらの機能をオンまたはオフにする場合、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)で実行する必要があります。

| モジュール | 機能管理の機能名 | 詳細 |
|---|---|---|
| 在庫および倉庫管理 | 会社間手持在庫で、0 以外の手持在庫数量のみを表示可能にする | この機能を使用すると、手持ち数量が 0 の品目を会社間の手持ち在庫リストに含めるかどうかを選択できます。 このオプションを制御するには、**会社間手持在庫リストに 0 の手持在庫数量の品目を表示しない** 設定を使用します。この機能は、**在庫および倉庫管理パラメーター** ページに追加されます。 |
| 在庫および倉庫管理 | (インド) 移動価格ルールにより、[元倉庫コード] が [すべて] に設定されている場合は場所を無視する | <p>この機能は、インドのローカライズにのみ適用されます。 在庫移動時に品目の移動価格をより直感的に設定することができます。</p><p>移動価格を設定するには、移動価格ルールを使用して各品目を設定します。 この設定方法の 1 つは、**元倉庫コード** フィールドが *すべて* に設定されているルール明細行を含めることです。 この設定は、品目をピッキングする倉庫に関係なく、明細行で定義された移動価格を適用します。 この機能を有効にすると、**元倉庫コード** フィールドが *すべて* に設定されている移動価格ルールは **場所** の設定を無視します。 そのため、移動オーダーで指定される場所に関係なくルールが適用されます。 場所が保管分析コード階層の倉庫の下にあるため、これはおそらく予期される動作です。</p><p>この機能を使用しない場合、このタイプ のルールが適用されるのは、移動オーダーの場所がルールに設定されている場所と完全に一致する場合に限ります。 (ルールに空の場所が設定されている場合、場所に空の値を持つ移動オーダーにのみルールが適用されます。)</p> |
| 在庫および倉庫管理 | 手持在庫レポート データのクリーンアップ | この機能を使用すると、*手持在庫レポート ストレージ* レポートのデータを作成するために使用するデータをクリーンアップできます。 |
| 生産管理 | サービス契約およびサービス注文明細行へのプロジェクト活動の割り当て | この機能で、**プロジェクト活動** という名前のフィールドをサービス契約およびサービス注文明細行に追加できるので、それらのプロジェクト活動を設定できます。 この機能は、プロジェクト活動の設定が必要なサービス管理プロジェクト仕訳帳を転記する際に、ブロック エラーを防ぐのに役立ちます。  |
| 倉庫管理 | 管理者または同様の信頼できるユーザーのための移動明細行手動ピッキング サービス | この機能を使用すると、移動明細行に関連付けられた在庫トランザクションを手動で選択できます。 これらの明細行には、既に倉庫にリリースされている明細行が含まれます。 管理者は、システムが破損した状態などの例外的な場合にのみこのピッキングを行うようにしてください。 |

## <a name="new-and-updated-documentation-resources"></a>新しいドキュメント リソースおよび更新されたドキュメント リソース

次のヘルプ トピックを最近追加、または大幅に更新しました。 これらのトピックは、前のセクションに示したように、このリリースで追加された新しい機能に関連するとは限りません。 ただし、これらの機能は既存の機能をさらに活用するために役立つ場合があります。

| 機能領域 | 新規または更新されたトピック |
|---|---|
| 原価管理 | [固定入庫価格](../cost-management/fixed-receipt-price.md) |
| 原価管理 | [在庫原価計算のよく寄せられる質問](../cost-management/inventory-costing-faq.md) |
| 原価管理 | [掛売勘定の会計原則に転記](../cost-management/post-to-charge-account-accounting-principle.md) |
| 在庫管理 | [在庫トランザクションの詳細](../inventory/inventory-transactions-details.md) |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Microsoft Dynamics 365 Supply Chain Management 10.0.28 には、Platform updates が含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.28 のプラットフォーム更新プログラム (2022 年 6 月)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md) を参照してください。<!-- KFM Confirm link -->

### <a name="bug-fixes"></a>バグ修正

10.0.28 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438) を参照してください。

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 1 プラン](/dynamics365-release-plan/2022wave1/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-supply-chain-management-features"></a>削除済みおよび非推奨の Supply Chain Management 機能

[Dynamics 365 Supply Chain Management の削除済みおよび非推奨の機能](removed-deprecated-features-scm-updates.md)トピックは、Supply Chain Management で削除または非推奨となる予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Supply Chain Management の削除済みまたは非推奨の機能](removed-deprecated-features-scm-updates.md)のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
