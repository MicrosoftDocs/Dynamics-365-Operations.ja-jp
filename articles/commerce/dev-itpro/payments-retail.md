---
title: 支払いに関するよくあるご質問
description: この記事では、Dynamics 365 Commerce で使用できる支払いオプションについて説明します。
author: josaw1
ms.date: 10/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Version 1611
ms.custom: 65801
ms.assetid: 99079d81-fde2-4432-8cee-82bbcc3bd57e
ms.openlocfilehash: aa56c6856cbd6bf5559005b4767c622e0514176c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268428"
---
# <a name="payments-faq"></a>支払いに関するよくあるご質問

[!include [banner](../../includes/banner.md)]

## <a name="what-payment-scenarios-are-supported"></a>どのような支払シナリオがサポートされますか ?

- マーチャント口座を設定します。
- コール センター注文を処理します。
- オフライン注文を処理します。
- 受諾ページを使用して、POS 現金払い取引を処理します。
- 受諾ページを使用して、POS 現金払い返品を処理します。
- 受諾ページを使用して、POS 現金払い返品を処理します。
- 受諾ページを使用して POS 顧客注文を処理します。
- Microsoft Dynamics Commerce Retail ハードウェア ステーションを使用して、POS 現金払いトランザクションを処理します。
- ハードウェア ステーションを使用して、POS 現金払い返品を処理します。
- ハードウェア ステーションを使用して POS 顧客注文を処理します。
- オンラインで購入し、店舗で受け取ります。
- コール センターで購入し、店舗で受け取ります。

## <a name="which-payment-providers-are-supported-and-in-what-regions"></a>どの支払プロバイダーがどの地域でサポートされていますか。

- Adyenはカードが存在する、またはカードが存在しない商取引に対応しています。 対応している地域の一覧については、 [Adyen 向け Dynamics 365 Payment Connector の概要ページ](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3) を参照してください。
- PayPal はオンライン購買でサポートされます。 対応している地域の一覧については、[PayPal 向け Dynamics 365 Payment Connector の概要ページ](../paypal.md) を参照してください。
- **TestConnector** は、ユーザー受け入れテスト (UAT) または運用 (prod) ではサポートされていません。 **TestConnector** は、サンドボックスおよび開発のみで使用することができ、サンプル専用です。 
- Mastercard Simplify は新しい顧客に対しては対応していません。

## <a name="what-is-a-payment-connector-and-in-what-cases-do-i-need-to-deploy-and-implement-a-payment-connector"></a>支払コネクタとは何ですか、またどのような場合に支払コネクタの配置と実装が必要ですか ?

支払コネクタは、カードが存在しないトランザクションとカードが存在するトランザクションの支払いをアプリケーションが処理できるようにする、設定可能なソフトウェア コンポーネントです。

Adyen などの Microsoft によって指定されたコネクタを使用するか、または ISV パートナーがカスタム コネクタを開発することができます。 コネクタは通常、顧客の業務でのニーズを満たすために構築されます。 新しいタイプの支払いタイプ (リンク払い戻しなど) が必要なシナリオがある場合、カスタム コネクタが作成されることがあります。 特定の地域でビジネスを行っている顧客は、最初から用意されているコネクタがこれらの地域をサポートしていない場合、新しいコネクタが必要になることがあります。

## <a name="are-other-payment-connector-providers-supported"></a>その他の支払コネクタ プロバイダーはサポートされていますか。

はい、ただしカスタマイズを使用してそれらを接続する必要があります。

## <a name="what-is-the-service-level-agreement-sla-for-out-of-box-payment-connectors-like-adyen"></a>Adyen などの革新的な支払いコネクタ の サービス レベル アグリーメント (SLA) はどうなっているか ?

Adyen コネクタに関して、設定に関する問題の場合は Adyenコネクタの [概要ページ](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3) を参照してください。 コネクタに関するその他の設定、または機能の問題については、Microsoftへのサポートリクエストを作成してください。 問題がデバイス本体、またはAdyenの処理サービスに起因する場合は、support-dynamics365@adyen.com Adyenのサポートに連絡してください。

## <a name="if-a-supported-payment-provider-issues-an-update-will-microsoft-automatically-update-the-payment-connector-or-do-i-need-to-work-with-the-payment-provider-to-get-the-updated-payment-connector"></a>サポートされている支払プロバイダーが更新プログラムを発行した場合は、Microsoft は自動的に支払コネクタを更新してくれますか? または更新された支払コネクタを取得するために支払プロバイダーと連携する必要がありますか。

支払いコネクターの更新プログラムが支払コネクター プロバイダーによって発行された場合、支払いコネクターの更新バージョンは Dynamics 365 Commerce の次の予定リリースに含まれます。 ただし、顧客は早期に取得するため、支払コネクタ プロバイダと直接作業することもできます。

## <a name="does-dynamics-365-commerce-support-cash-out-or-cash-back-operations-during-the-checkout-process-in-point-of-sale-pos"></a>Dynamics 365 Commerce は販売時点管理 (POS) のチェックアウト プロセス中に「キャッシュ アウト」操作または「キャッシュ バック」操作をサポートしますか?

いいえ、トランザクションの間、POS ではキャッシュ バック操作またはキャッシュ アウト操作はサポートされません。 ただし、拡張機能によるカスタマイズは、ギフトカードの「キャッシュ アウト」操作と同様のキャッシュ リターンおよび支払い操作を使用して達成できます。 

## <a name="related-articles"></a>関連記事

- [支払端末のエンド・ツー・エンド支払統合を作成する](end-to-end-payment-extension.md)
- [支払コネクタの配置](deploy-payment-connector.md)
- [支払コネクタ用の Windows インストーラーの作成](create-windows-installer-payment-connector.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
