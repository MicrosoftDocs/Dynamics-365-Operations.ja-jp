---
title: Dynamics 365 Commerce 10.0.27 (2022 年 7 月) の新機能または変更された機能
description: この記事では、Dynamics 365 Commerce 10.0.27 の新機能および変更された機能について説明します。
author: josaw1
ms.date: 04/29/2022
ms.topic: article
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-04-30
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: cd8b38dad9311f2af36335f3e2c20402b09ab2c6
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069610"
---
# <a name="whats-new-or-changed-in-dynamics-365-commerce-10027-july-2022"></a>Dynamics 365 Commerce 10.0.27 (2022 年 7 月) の新機能または変更された機能

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Commerce 10.0.27 の新機能または変更された機能を示します。 このバージョンのビルド番号は 10.0.1227 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 4 月
- **リリースの一般提供 (手動更新):** 2022 年 6 月
- **リリースの一般提供 (自動更新):** 2022 年 7 月


## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 この記事が最初に公開された後に、ビルドに加えた機能を含めるために、この記事を更新することがあります。

| 機能領域   | フィーチャー                                                  | 詳細                                          |   に  によって有効化             |
|----------------|----------------------------------------------------------|-----------------------------------------------------------|-------------------------|
|B2B   | 顧客固有のカタログの有効化    |   この機能によって、 顧客が Commerce 企業間 (B2B) サイトのコマース製品カタログを作成する方法について説明します。 カタログを作成すると、顧客は製品が提供されるオンライン ストアを識別し、含める製品を追加し、また販売促進詳細を追加して提供製品を強化することができます。 顧客は B2B のオンライン ストアに複数のカタログを作成できます。</br></br>詳細については、[B2B サイトのコマース カタログの作成](../catalogs-b2b-sites.md)を参照してください。   | 機能管理<p>*小売チャネルで複数カタログの使用を有効にする*   |
|eコマース    |   Azure Active Directory B2C (Azure AD B2C) を使用したWeb API 認証から e コマースへの転送 | この機能により、顧客は外部サービスから有効な Azure AD B2C トークンを e コマース サイトに渡すことができます。 別のアプリケーションまたはサービスから Azure AD B2C テナントに対して認証されたユーザーを e コマース サイトに送信して、認証済みユーザーとして引き続き参照することができます。 | 開発者のオプトイン |
| グローバリゼーション  |  メキシコ向け電子請求書がグローバル CFDI バージョン 4.0 に対応 |   メキシコの電子請求機能 (Comprobante Fiscal Digital por Internet - CFDI) は、グローバル CFDI 形式のバージョン 4.0 に対する規制に準拠するために拡張されています。 この機能により、主要な変更点を含め、レイアウトに対して必要な変更が追加されます。<p><p>- 小売固有の新しい要素「InformacionGlobal」。 <p>- 特定期間に最終顧客に発行されたすべてのレシートを集計します。 <p>詳細については、[メキシコのグローバル CFDI 電子請求書](/finance/localizations/latam-mex-global-cfdi-3-3) を参照してください。     | 電子請求書パラメーターの CFDI バージョン。 詳細については、[電子請求書 (CFDI)](/finance/localizations/latam-mex-CFDI-electronic-invoices) を参照してください。 |
| グローバリゼーション  | POS での会計登録プロセスの詳細の表示             |      この機能を使用すると、Commerce POS の **設定** ページで、会計統合の状態、監査イベントのキュー、接続パラメーター、その他の関連情報を確認できます。<p><p>詳細情報については、[コマース チャネルの会計統合の設定](../localizations/setting-up-fiscal-integration-for-retail-channel.md)を参照してください             |   機能管理<p>*会計統合技術プロファイルの上書き*             |
| グローバリゼーション  |    フランス向け NF525 認証更新           |    この更新プログラムには、フランスの NF525 資格要件に従って新しい機能が含まれています。<p><p>- POS 監査イベント ログに品目の無効化監査イベントを登録し、デジタル署名します。<p>- Commerce HQ から XML ファイルに終了したシフトの Z レポートをエクスポートします。<p>新しい *(フランス) POS で追加監査イベントを有効にする* 機能で、Commerce Runtime (CRT) および Commerce POS の対応する拡張機能を明示的に有効にすることなく、フランスのすべての監査イベントの登録およびデジタル署名を可能にできます。<p>詳細については、 [フランスのキャッシュ レジスター機能。](../localizations/emea-fra-cash-registers.md) を参照してください。          | 機能管理<p>*(フランス) POS で追加監査イベントを有効にする*<p>*(フランス) Z レポートのファイルへのエクスポートを有効にする*|     
| 支払  |  Adyen 向け Dynamics 365 Payment Connector で Google Pay を有効にする | e コマースの顧客は、エクスプレス チェックアウト モジュールで構成されたカートとチェックアウトのページで Google Pay を使用できます。 | 開発者のオプトイン   |
|売上税   | [価格に売上税が含まれる場合の eコマースの税内訳の表示/非表示](/dynamics365-release-plan/2022wave1/commerce/dynamics365-commerce/show-or-hide-tax-breakdown-e-commerce-when-prices-include-sales-tax)  |  Commerce は税内訳情報を、カートの注文集計、チェックアウト、注文確認、および注文の詳細ページで表示します。 Commerce バージョン 10.0.2 では、Commerce サイト ビルダーに、注文集計の税内訳情報を非表示にできるオプションが用意されています。 詳細については、[税内訳情報を注文集計で非表示にする](../hide-taxes-breakup.md) を参照してください。   |  サイト ビルダー  |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Dynamics 365 Commerce 10.0.27 には、プラットフォーム更新プログラムが含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.27 のプラットフォーム更新プログラム (2022 年 7 月)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-27.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正 
この更新プログラムに含まれるバグ修正については、Lifecycle Services (LCS) にサインインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271) を参照してください。

Commerce 固有の重大な変更を加える場合は、[Dynamics 365 Commerce オンライン SDK に関するよく寄せられる質問](../e-commerce-extensibility/sdk-faq.md) を参照してください。

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 1 プラン](/dynamics365-release-plan/2022wave1/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Dynamics 365 Commerce で削除または廃止された機能](removed-deprecated-features-commerce.md)の記事では、Commerce で削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Commerce の削除済みまたは非推奨の機能](removed-deprecated-features-commerce.md)の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

