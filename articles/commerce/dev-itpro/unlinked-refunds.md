---
title: Adyen 用 Dynamics 365 Commerce Payment Connector でリンクされていない払戻を処理する
description: この記事では、Adyen 用 Microsoft Dynamics 365 Payment Connector を使用する場合に、リンクされていない払戻しがいかに機能するかについて説明します。
author: BrianShook
ms.date: 10/07/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 2b2bee7ad45bbff82c8b7de2741925fde29d8583
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284314"
---
# <a name="process-unlinked-refunds-with-the-dynamics-365-commerce-payment-connector-for-adyen"></a>Adyen 用 Dynamics 365 Commerce Payment Connector でリンクされていない払戻を処理する

[!include [banner](../includes/banner.md)]

この記事では、[Adyen 用 Microsoft Dynamics 365 Payment Connector](adyen-connector.md) を使用する場合に、リンクされていない払戻しがいかに機能するかについて説明します。 また、これは販売時点管理 (POS) やコールセンターでの新しい支払方法に対する払戻しを処理する能力もレビューします。

Adyen 用 Dynamics 365 Payment Connector では、元のトランザクションで使用された支払方法とは異なる支払方法を使用して払戻しを処理することができます。 リンクされた払戻しを使用して、[リンクされた払戻し](linked-refunds.md) を使って、提供された元の支払方法に対する払戻しを処理することをお勧めしますが、場合によっては別の方法での払戻しが必要になります。 たとえば、元の支払に使用されたカードの期限が切れたり失われたり、ユーザーによってキャンセルされた場合があります。

## <a name="prerequisites"></a>必要条件

Adyen 用 Dynamics 365 Payment Connector がリンクされていない払戻しを処理する前に、次の前提条件を満たす必要があります。

- [支払い方法](../payment-methods.md) を設定する。
- [オムニチャネル支払い](../omni-channel-payments.md) を設定する。

## <a name="additional-configuration"></a>追加設定

Adyen 用 Dynamics 365 Payment Connector では、次のセクションで説明されるすべてのサポートされている払戻しのシナリオにすぐに使える実装を提供します。 Adyen 用 Dynamics 365 Payment Connector の標準の実装を使用していない顧客は、クレジットカードのトークン化をサポートするコネクタを設定する必要があります。

## <a name="supported-refund-scenarios"></a>サポートされている払戻しシナリオ

Dynamics 365 Commerce では、以前に承認および確認されたトランザクションの払戻しをサポートしています。 払戻しは、トランザクションの全額払戻または一部払戻しで構成されます。 元の支払許可の金額を超えた払戻しはできません。 リンクされていない払戻しは、POS とコール センターでのみサポートされます。

## <a name="enable-unlinked-refunds-functionality"></a>リンクされていない払戻し機能を有効にする

Commerce 本社で、リンクされていない払戻し機能を有効にするには、次の手順を実行します。

1. **Retail とコマース \> 本社の設定 \> パラメーター \> コマース共有パラメーター** の順に移動します。
1. **オムニ チャネル支払い** タブで **オムニ チャネル支払いを使用する** オプションを **はい** に設定します。

### <a name="supported-payment-method-variants"></a>サポートされている支払方法のバリアント

次の支払い方法のバリアントでは、標準でリンクされていない払戻しがサポートされています。

- カード
- ウォレット

リンクされていない払戻しはすべての支払い方法でサポートされているわけではありません。 次の表は、一般的な支払い方法の一覧で、リンクされた払戻しとリンクされていない払戻しに対する各方法のサポート機能を示しています。

| 支払方法        | リンクされた払戻 | リンクされていない払戻し |
|-----------------------|:-------------:|:---------------:|
| amexcommercial        | あり           | あり             |
| amexconsumer          | あり           | あり             |
| amexcorporate         | あり           | あり             |
| amexdebit             | あり           | あり             |
| amexprepaid           | あり           | あり             |
| amexprepaidreloadable | あり           | あり             |
| amexsmallbusiness     | あり           | あり             |
| discover              | あり           | あり             |
| maestro               | あり           | あり             |
| maestrouk             | あり           | あり             |
| mc                    | あり           | あり             |
| mcalphabankbonus      | あり           | あり             |
| mcprepaidanonymous    | あり           | あり             |
| visa                  | あり           | あり             |
| visaalphabankbonus    | あり           | あり             |
| visacheckout          | あり           | あり             |
| visadankort           | あり           | あり             |
| Visahipotecario       | あり           | あり             |
| visasaraivacard       | あり           | あり             |
| vpay                  | あり           | あり             |
| givex                 | **なし**        | あり             |
| svs                   | **なし**        | あり             |
| cup                   | あり           | あり             |
| diners                | あり           | あり             |
| interac               | **なし**        | あり             |
| jcb                   | あり           | あり             |
| jcb_applepay          | あり           | あり             |
| unionpay              | あり           | あり             |

### <a name="process-an-unlinked-refund-in-pos"></a>POS でのリンクされていない払戻しの処理

顧客は、返品が許可されている期間中に商品を POS レジ係に返品し、有効なレシートを受け取ります。 返品の処理中に、**支払の返品** ダイアログ ボックスに **支払い方法** のオプションが含まれています。 その後、レジ係は、サポートされている払戻し方法 (カードとウォレット) の中から支払い方法を選択できます。

### <a name="process-an-unlinked-refund-in-call-center"></a>コールセンターでのリンクされていない払戻しの処理

リンクされていない払戻しがコール センターの注文に対して処理される場合、コール センターの従業員は元の方法とは異なる支払い方法を選択します。 次に、管理者に個人の ID 番号 (PIN) の上書きを求めるメッセージが表示されます。 PIN は、さまざまな支払い方法で払戻しを処理する前に必要です。

#### <a name="set-up-an-administrator-override-pin-for-call-center"></a>コール センターの管理者上書き PIN の設定

Commerce 本社でコール センターの管理者上書き PIN を設定するには、次の手順に従います。

1. **小売およびコマース \> チャネル設定 \> コールセンター設定** の順に移動するか、"上書きの許可" を選択します。
1. リンクされていない払戻し処理のアクセス許可を許可するロールを選択します。
1. **払戻し** クイック タブで、**別の支払いを許可** オプションを **はい** に設定します。

## <a name="additional-resources"></a>追加リソース

[Adyen 向け Dynamics 365 Payment Connector](adyen-connector.md)

[以前に承認および確認済みのトランザクションのリンクされた払戻](linked-refunds.md)
