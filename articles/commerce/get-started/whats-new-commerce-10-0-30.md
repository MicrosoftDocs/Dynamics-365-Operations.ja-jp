---
title: Dynamics 365 Commerce 10.0.30 のプレビュー (2022 年 11 月)
description: この記事では、Microsoft Dynamics 365 Commerce 10.0.30 の新機能および変更された機能について説明します。
author: josaw1
ms.date: 08/31/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-09-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 0149c9671e8baeb26965b4f136ed91d09e2d039b
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405563"
---
# <a name="preview-of-dynamics-365-commerce-10030-november-2022"></a>Dynamics 365 Commerce 10.0.30 のプレビュー (2022 年 11 月)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Commerce プレビュー バージョン 10.0.30 の新機能または変更された機能について一覧表示します。 このバージョンのビルド番号は 10.0.1362 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 9 月
- **リリースの一般提供 (手動更新):** 2022 年 10 月
- **リリースの一般提供 (自動更新):** 2022 年 11 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 この記事が最初に公開された後に、ビルドに追加された機能を含めるために、この記事を更新することがあります。

| 機能領域 | フィーチャー | 詳細 |  に  によって有効化 |
|---------|------------------|----------------|--------------| 
| カスタマー サポート   | Power Virtual Agents ボットを使用した eコマース サイトのチャット | この機能を使用すると、e コマース サイトのユーザーが、サポート要求に対して Power Virtual Agents チャットボットを使用することができます。 | 管理者/作成者によってエンド ユーザー向けに有効化 |
| インサイト  |  自分 Application Insights アカウントに対する販売時点 (POS) 運用情報イベントを配信 します。 | [Application Insights のログへのアクセス](../dev-itpro/retail-component-events-diagnostics-troubleshooting.md#enable-diagnostic-events-in-application-insights)   |  IT Pro/開発者のオプトイン   |
|  支払  | PayPal 注文では、29 日間の認証期間を超える期間をサポートしています。 | PayPal の最大認証期間は 29 日で、この後に新しい認証 ID と注文 ID を生成する必要があります。 別の方法として、PayPal では、PayPal 注文が一般的な注文として参照できるオプションが用意されています。このオプションを使用すると、29 日目に新しい認証 ID と注文 ID を生成する代わりに、同じ注文 ID に対して複数の認証とキャプチャを行うことができます。 | Commerce Headquarters で PayPal 支払コネクタを構成する場合は、**OrderIntent** フィールドが追加され、2 つの値を使用できます。<p><p>- **承認** - この構成が既定で使用されます (フィールドが空白の場合、**Authorize** が既定の動作になります)。 **OrderIntent** を **Authorize** に構成することは、**NO_INSTRUCTION** の PayPal **processing_instruction** の値に関連します。 この値を使用すると、注文は PayPal で承認され、承認を変更することはできません。<p>- **Save** - **OrderIntent** の値が **Save** に設定されている場合、これは **ORDER_SAVED_EXPLICITLY** の PayPal **processing_instruction** の値に関連します。 この値が使用された場合、注文参照は PayPal サービスに保存されます。  |
| POS サインイン  | [POS サインインのセルフサービス診断機能の有効化](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-self-serve-diagnosis-capabilities-pos-sign-in)  |  この機能により、POS および Commerce Headquarters のセルフサービス診断機能を使用する際、店舗の従業員やマネージャーが POS サインインの問題の原因のルートをすぐに特定および修正できます。<p><p>- POS サインイン画面に表示される失敗メッセージが改善され、POS を使用する従業員が問題を解決するために必要なアクションを実行できるようなルート情報が提供されました。<p>- **テスト ログオン** 関数 は Commerce Headquarters の **ワーカー** ページで使用できるので、POS デバイスを設定する店舗マネージャーは、POS サインインをシミュレートできます。 サインインに失敗した場合、この機能はアクション可能なトラブルシューティング ガイドを提供します。これにより、マネージャーは関連する構成を確認し、問題を修正し、修正を検証できます。  | 既定で有効 |


## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Dynamics 365 Finance 10.0.30 には、プラットフォーム更新プログラムが含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.30 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

バージョン 10.0.30 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468) を参照してください。 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 2 プラン](/dynamics365-release-plan/2022wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Dynamics 365 Commerce で削除または廃止された機能](removed-deprecated-features-commerce.md)の記事では、Commerce で削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Commerce の削除済みまたは非推奨の機能](removed-deprecated-features-commerce.md)の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
