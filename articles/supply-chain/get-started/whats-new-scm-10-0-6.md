---
title: Dynamics 365 Supply Chain Management 10.0.6 (2019 年 11 月) の新機能および変更された機能
description: この記事では、Dynamics 365 Supply Chain Management 10.0.6 の新機能および変更された機能について説明します。
author: kamaybac
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 8c97e4e5544c49d2e6a13b34061abfbf50e2932a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844441"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a>Dynamics 365 Supply Chain Management 10.0.6 (2019 年 11 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Supply Chain Management 10.0.6 の新機能または変更された機能について説明します。 このバージョンのビルド番号は 10.0.234 です。 一般提供開始日は 11 月ですが、新機能は 10 月の初期リリースで使用できます。 バージョン 10.0.6 の詳細については [追加リソース](whats-new-scm-10-0-6.md#additional-resources) を参照してください。

## <a name="product-configuration-models-v2-data-entity"></a>製品コンフィギュレーション モデル V2 データ エンティティ

「製品コンフィギュレーション モデル」 データ エンティティの 2 番目のバージョンがリリースされます (「製品コンフィギュレーション モデル V2」 と呼ばれます)。 既定のテンプレート 「418- 製品コンフィギュレーション モデル」も、インポート/エクスポート フレームワーク テンプレートで新しい「製品コンフィギュレーション モデル V2」 データ エンティティを使用するようにする必要があります。 テンプレートは自動更新されないので、既定で手動でテンプレートを読み込む必要があります。 V2 エンティティは、1 つの行をインラインの代わりに添付ファイルの個別のファイルとしてエクスポートし、V1 エンティティのサイズ制限を解決します。 
 
この変更を行うにはどうしますか。
-    V1 エンティティは使用されなくなったため、V1 から V2 への移行を開始する必要があります。 「418- 製品コンフィギュレーション モデル」 テンプレートを使用している場合、「既定のテンプレートの読み込み」ボタンをクリックし、テンプレート 「418- 製品コンフィギュレーション モデル」を再読み込みできます
-    既存のシステムとの互換性を維持する必要がある場合は、統合を新しいテンプレートに移行するまで、とりあえず既存のテンプレートおよび (非推奨) V1 エンティティを引き続き使用できます。 

## <a name="feature-management-enhancements"></a>機能管理の拡張
機能管理を使用すると、既定ですべての新機能を有効にできます。それには機能を有効にするための確認と、まだ有効になっていないすべての機能を有効にすることが必要です。 


## <a name="purchase-agreement-responsible-party"></a>購買契約責任者
購買契約分類フォームと結果の購買契約で、基本および二次の責任者を定義する機能が用意されました。  これにより、ユーザーは契約の監督者にアクセスできるようになります。

## <a name="rfq-link-on-the-purchase-order-line"></a>発注書明細行の RFQ リンク
発注書明細行から元の RFQ 明細行に参照リンクを追加できます。これにより、サポートする見積依頼ドキュメントをユーザーに簡単に提供できます。

## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正
10.0.6 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7) を参照してください。

### <a name="platform-update-30"></a>プラットフォーム update 30
Microsoft Dynamics 365 Supply Chain Management 10.0.6 には、プラットフォーム更新プログラム 30 が含まれています。 プラットフォーム更新プロフラム 30 についての詳細は、[プラットフォーム更新プログラム 30 の新機能と変更](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md) をご覧ください。

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: 2019 リリースのウェーブ 2 プラン
当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2019 リリース ウェーブ 2 プラン](/dynamics365-release-plan/2019wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-supply-chain-management-features"></a>削除済みおよび非推奨の Supply Chain Management 機能

[Dynamics 365 Supply Chain Management の削除済みおよび非推奨の機能](removed-deprecated-features-scm-updates.md)の記事は、Supply Chain Management で削除または非推奨となる予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Supply Chain Management の削除済みまたは非推奨の機能](removed-deprecated-features-scm-updates.md)の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]