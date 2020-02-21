---
title: Dynamics 365 Fraud Protection の Dynamics 365 Commerce との統合
description: このトピックでは、Microsoft Dynamics 365 Fraud Protection と Dynamics 365 Commerce との間で使用可能な標準統合について説明します。
author: rubendel
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: ''
ms.search.scope: Operations, Retail, Commerce
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 79965de3a3bf6107f646ec1ea9f6873f12e5458b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004612"
---
# <a name="dynamics-365-fraud-protection-integration-with-dynamics-365-commerce"></a>Dynamics 365 Fraud Protection の Dynamics 365 Commerce との統合

[!include [banner](../includes/banner.md)]


このトピックでは、Microsoft Dynamics 365 Commerce と Dynamics 365 Fraud Protection との間で使用可能な標準統合について説明します。

## <a name="key-terms"></a>重要な用語

| 相談 | 説明 |
|---|---|
| 購入保護 | マーチャントが決定したリスクレベルに基づいて、購入に対して不正の分析をおこないう Fraud Protection モジュール。 |
| 店舗 | 商取引に提供する標準の電子商取引店舗。 |

## <a name="overview"></a>概要

Fraud Protection は、小売業者が不正活動を防ぎ、知られていない可能性がある不正の場所を特定するのを助ける Fraud Protection ソリューションを提供するサービスです。 このトピックでは、Fraud Protection と Commerce との間で使用可能な標準統合について説明します。 これは、今後のリリースで 2 つのサービスの間で新しい統合がリリースされると、更新されます。 Commerce との標準統合ではまだサポートされていないモジュールに関する情報など、Fraud Protection に関する詳しい情報は、[Fraud Protection ランディング ページ](https://dynamics.microsoft.com/ai/fraud-protection/) をご覧ください。 また、Dynamics 365 の営業担当者から [コールバックを要請](https://dynamics.microsoft.com/get-started/?appname=fraudprotection) し、Fraud Protection が利益性を大幅に増加し、運営経費を削減し、顧客エクスペリエンスを向上させる方法について話をすることもできます。

## <a name="purchase-protection-in-commerce"></a>Commerce の購入保護

### <a name="purchase-protection-overview"></a>購入保護の概要

Fraud Protection から最初に使用可能な一般的なオファリングは、マーチャントを組織の Fraud Protection ダッシュボード へとサインインさせ、オンライン購入に当たっての不正ルールを定義させる購入保護モジュールです。 Fraud Protection でマーチャントが構成する設定に基づいて、電子商取引トランザクションは支払認証に送られる前に Fraud Protection を使って検証することができます。

注文が Fraud Protection 購入保護モジュールに送信される場合、Fraud Protection は購入を分析し、マーチャントが定義した不正ルールと人工知能 (AI) によって駆動されるインサイト、そしてにコンソーシアムベースの不正分析に基づいてリスク評価を提供します。 不正スコアがマーチャントのリスク トレランスの次元を超過して返された場合は、Fraud Protection は店舗に注文を拒否するように指示を出します。 注文が拒否されない場合は、Fraud Protection は店舗が注文のフルフィルメント処理の次のステップを決定するために使用できる不正スコアを返します。 このようなステップには、注文の手動レビューのために注文を保留にしたり、注文した顧客のフォローアップなどが含まれることがあります。

### <a name="supported-capabilities-in-the-purchase-protection-integration"></a>購入保護統合でサポートされている機能

#### <a name="purchase-events"></a>発注イベント

現在、Commerce はパブリック プレビューにあります。 ただし、一般的で入手可能になった場合には、この購入保護統合は Fraud Protection リスク評価の受信とストア店舗での注文の中止をサポートします。

こちらが購入イベントのフローです。

1. 店舗の顧客が、商品を買い物かごに追加してチェックアウトへと進みます。
2. 顧客が配送先と支払の詳細を入力します。
3. 前提条件が完了した後、顧客が **注文する** を選択します。
4. 購入保護評価のために、注文の詳細が Fraud Protection に送信されます。
5. Fraud Protection で定義されたマーチャント ルールがこのオーダーを拒否すべきと判断した場合は、応答が店舗に送信され、注文は中止されます。

Fraud Protection 購入保護が注文の中止をおこなった場合は、ユーザーは次のメッセージを受信します : 「このオーダーは現時点では処理できません 後でもう一度お試しください。」

![参照となる店舗から拒否された注文の例](../media/Payments/SampleDFPReject.png)

あるいは、マーチャント ルールがこの注文は承認されるべきと判断した場合は、不正スコアと Fraud Protection で判定された理由コードを含む回答が店舗へ送信されます。 初期統合では、Fraud Protection 評価はどちらにしても使われておらず、承認と拒否の両セクションの回答は保存されません。

拒否された注文は、支払プロセスの承認には送信されず、バック オフィスの注文作成プロセスには進みません。

#### <a name="bank-events"></a>銀行イベント

オンライン注文が Fraud Protection 評価に基づいて許可された場合は、次のステップは、その注文が支払承認が該当する場合は、支払いの承認になります。 支払プロセッサがこの注文を承認したら、Fraud Protection は承認結果を通知されます。 この結果を Fraud Protection に送信することで、高度な AI は生来の承認結果を予測するためにさらに学習することができ、それによって将来の Fraud Protection 評価の質を著しく向上させます。

#### <a name="purchase-status-events"></a>注文ステータスイベント

注文ステータスは銀行イベントと類似しています。 注文が Commerce の銀行オフィスで作成された後、信号が Fraud Protection に発信され、注文が正常に作成されたことを示します。 銀行イベントと購入ステータスは両方とも情報を提供するイベントです。 従って、Fraud Protection からの回答はありません。

### <a name="availability"></a>在庫状態

Dynamics 365 Retail バージョン 10.0.8 では、Retail には Fraud Protection 統合のバック オフィス設定が含まれます。 ただし、標準のフル統合には Commerce に含まれている店舗が必要ですが、Commerce は現在パブリック プレビューをしています。 Commerce が一般に利用可能となりましたら、既存の Retail の顧客はそちらに更新できるようになります。 詳細については、[Dynamics 365 Commerce のランディング ページ](https://dynamics.microsoft.com/commerce/overview/) を参照してください。

#### <a name="setup"></a>セットアップ

標準の購入保護統合には、Fraud Protection 環境が必要です。 Fraud Protection を設定するには、 Dynamics 365 の営業担当者からの [コールバックを要求してください](https://dynamics.microsoft.com/get-started/?appname=fraudprotection)。

マーチャントの Fraud Protection 環境が利用可能になると、購入保護設定が構成され、Commerce バック オフィスで設定を続行できます。

##### <a name="key-vault-setup"></a>Key Vault の設定

統合設定では、Commerce が Fraud Protection と通信して、購入保護の結果を得る際にシークレットを使用することが求められます。 このシークレットは  Azure Key Vault クライアントの使用によって保存されなければなりません。 位置情報検出を設定する方法の詳細については [位置情報検出の設定](https://support.microsoft.com/help/4040305/setting-up-azure-key-vault-client) を参照してください。

Key Vault に保管されている Fraud Protection 証明書は、Commerce のバック オフィスにある Key Vault パラメーターによって参照される場合のみ参照されることができます。 Key Vault パラメーターを設定するには、Commerce で、**Retail と Commerce** \> **本社の設定** \> **パラメーター** \> **Key Vault パラメーター** の順に移動します。

次に、Fraud Protection シークレットを補完するために使用される Key Vault URL を選択して、**追加** を選択します。 その後、購入保護評価のために注文を送る際、Commerce を承認するために使用される、Key Vault シークレットの名前、説明、パスを指定します。

##### <a name="retail-parameters-setup"></a>Retail のパラメーター設定

1. **Retail と Commerce** \> **本社の設定** \> **パラメーター** \> **Retail パラメーター** の順に移動します。
2. **Dynamics Fraud Protection** タブで、**Dynamics Fraud Protection 統合を有効にする** オプションを **はい** に設定します。
3. **構成** ファストタブで、Azure Active Directory (Azure AD) クライアント ID を追加し、その後、前に構成した Key Vault シークレットの名前を選択します。

    規定では、**評価の種類** フィールドは **評価** に設定します。 この場合は、Fraud Protection は不正の注文を従順にチェックしますが、積極的に注文の拒否はしません。 従って、マーチャントは Fraud Protection のリスク評価を自分たちの不正ツールと比較をし、承諾レートで Fraud Protection の影響を理解することができます。

    または、**評価の種類** フィールドは **保護** に設定できます。 この場合、Fraud Protection は「拒否」評価を返答し、承認に送信またはバック オフィスで作成される前に、不正な注文は中止されます。

4. **Dynamics Fraud Protection エンドポイント URL** フィールドは設定する必要があります。 この URL は Fraud Protection から提供され、ユーザー受け入れテスト (UAT) と運用環境に渡り異なります。

![Retail パラメーターでの Fraud Protection 設定](../media/Payments/DFPSetupParams.png)

> [!NOTE]
> Key Vault 設定と Fraud Protection 設定は会社固有です。 Fraud Protection を運用環境に対して有効にするには、ユーザーインターフェイス (UI) を通して Azure AD クライアント ID は入力しません。 その代わり、[サービス要求](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team) を作成および提出する必要があります。 要求のタイトルには、この要求が運用版 Commerce または Retail のための Fraud Protection 購入保護を構成するためであることを明確に示します。

## <a name="privacy-notice"></a>プライバシー通知

この機能を有効にする場合、データの一部はその他の Microsoft オンライン サービスと共有されます。 このデータには、支払い、クレジット、返却、トランザクション状況や個人データについての情報が含まれます。 Fraud Protection の購入保護評価は、Retail または Commerce のオンラインサービスによって並べ替えはされません。

Microsoft にとってお客様のプライバシーは重要です。 詳細については、[Microsoft のプライバシーに関する声明](https://go.microsoft.com/fwlink/?LinkId=521839) をお読みください。

## <a name="related-articles"></a>関連記事

- [支払に関するよく寄せられる質問](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
- [Dynamics 365 支払データの使用](https://docs.microsoft.com/dynamics365/retail/payment-connector-data-fields)
