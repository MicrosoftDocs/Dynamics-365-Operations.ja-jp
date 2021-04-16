---
title: 支払いモジュール
description: このトピックでは、支払いモジュールについて取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。
author: anupamar-ms
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 09c7504eda0d389738b9d13b73f33472dc8f5fe3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804482"
---
# <a name="payment-module"></a>支払モジュール

[!include [banner](includes/banner.md)]

このトピックでは、支払いモジュールについて取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。

支払モジュールにより、顧客はクレジット カードやデビット カードを使用して注文の支払を行うことができます。 このモジュールの支払い統合は、 Dynamics 365 Payment Connector によって提供されます。 支払いコネクタを設定および構成方法についての詳細は、[Adyen 用の Dynamics 365 Payment Connector ](dev-itpro/adyen-connector.md) を参照してください。  

Commerce リリース 10.0.14 の時点で、支払モジュールは PayPal 向け Dynamics 365 Payment Connector とも統合されており、顧客は PayPal を使用して注文の支払いを行うことができます。 PayPal 向け Dynamics 365 Payment Connector の設定および構成方法についての詳細は、[PayPal 向け Dynamics 365 Payment Connector](paypal.md) を参照してください。 

## <a name="dynamics-365-payment-connector-for-adyen"></a>Adyen 向け Dynamics 365 Payment Connector 

支払モジュールは、HTML インライン フレーム (iframe) でAdyen 経由で提供される支払情報をホストします。 支払モジュールは、Commerce Scale Unit とやり取りして、Adyen 支払情報を取得します。 Commerce Scale Unit のやり取りの一部として、支払モジュールでは、入力した請求先住所情報を iFrame で Adyen 経由で処理するか、別のモジュールとして処理するかを指定できます。 Fabrikam テーマでは、請求先住所が別のモジュールとして有効化されます。 この方法を使用すると、住所の行を出荷先住所の行と類似したものに表示することができるので、書式設定上の柔軟性が高まります。

支払モジュールでは、顧客は支払情報を保存することもできます。 支払情報と請求先住所は、Adyen 支払コネクタを介して保存および管理されます。

支払モジュールは、ロイヤルティ ポイントまたはギフトカードで既にカバーされていない注文費用を対象とします。 注文の合計がロイヤルティ ポイントまたはギフトカード クレジットによって完全に覆われている場合は、支払モジュールが非表示になり、顧客は注文をそのままにすることができます。

Adyen 支払いコネクタは強力な顧客認証 (SCA) もサポートします。 欧州連合 (EU) 改訂決済サービス指令 (PSD2) の一部では、オンラインで買い物をする人は電子決済方法で決済する場合、自分たちのオンライン ショッピング体験以外で認証を受けることを義務付けています。 チェックアウト フローでは、顧客は銀行サイトにリダイレクトされ、認証後に Commerce のチェックアウト フローにリダイレクトされます。 このリダイレクトでは、顧客がチェックアウト フロー中に入力した情報 (たとえば、出荷先住所、配送オプション、ギフトカード情報、ロイヤルティ情報など) が維持されます。 Adyen 支払コネクタ機能を有効にする前に、Commerce 本社の SCA 用に支払コネクタをコンフィギュレーションする必要があります。 詳細については、[Adyen を使用した強力な顧客認証](adyen_redirect.md) を参照してください。 この機能は、Commerce リリース 10.0.12 で有効になりました。

> [!NOTE]
> Adyen 支払コネクタの場合、サイトの許可リストに Adyen URL を追加した場合にのみ、支払モジュールの iframe モジュールはレンダリングできます。 この手順を完了するには、**\*.adyen.com** をサイトのコンテンツ セキュリティ ポリシーの **child-src**、**connect-src**、**img-src**、**script-src**、**style-src** の各ディレクティブに追加します。 詳細については、[コンテンツ セキュリティ ポリシーの管理](manage-csp.md) を参照してください。 

次の図は、チェックアウト ページのギフト カード、ロイヤルティ ポイント、Adyen 支払モジュールの例を示しています。

![チェックアウト ページのギフト カード、ロイヤルティ ポイント、Adyen 支払モジュールの例](./media/ecommerce-payments.PNG)

## <a name="dynamics-365-payment-connector-for-paypal"></a>PayPal 向け Dynamics 365 Payment Connector

Commerce リリース 10.0.14 の時点で、支払モジュールは PayPal 向け Dynamics 365 Payment Connector とも統合されています。 この支払コネクタを設定および構成方法についての詳細は、[PayPal 向け Dynamics 365 Payment Connector ](paypal.md) を参照してください。
 
チェックアウト ページでは、Adyen と PayPal の両方のコネクタをコンフィギュレーションすることができます。 支払モジュールは、どのコネクタを使用する必要があるかを識別するための追加プロパティを持つように拡張されています。 詳細については、次の表の **サポートされている支払/入金タイプ** および **基本支払い** モジュールのプロパティを参照してください。
  
PayPal 支払コネクタを使用するように支払モジュールがコンフィギュレーションされている場合、チェックアウト ページに PayPal ボタンが表示されます。 顧客から呼び出された場合、支払モジュールは PayPal 情報を含む iFrame をレンダリングします。 顧客はログインして、この iFrame に PayPal 情報を提供することで、トランザクションを完了できます。 顧客が PayPal での支払いを選択した場合、注文の残りの残高は PayPal 経由で請求されます。

PayPal 支払コネクタは、すべての請求書関連情報が、その iFrame 内の PayPal によって処理されるため、請求先住所のモジュールを必要としません。 ただし、送付先住所と配送オプションの各モジュールが必要です。

次の図は、チェックアウト ページにある 2 つの支払モジュール (Adyen コネクタと PayPal 支払コネクタで構成された支払方法の例) を示しています。
![チェックアウト ページのAdyen 支払モジュールと PayPal モジュールの例](./media/ecommerce-paypal.png)

次の図は、PayPal ボタンを使用して起動された PayPal iFrame の例を示しています。 
![チェックアウト ページの Paypal iFrame の例](./media/ecommerce-paypal-iframe.png)

## <a name="payment-module-properties"></a>支払モジュールのプロパティ

| プロパティ名 | 値 | 説明 |
|---------------|--------|-------------|
| ヘッダー | ヘッダー テキスト | 支払いモジュールのオプション ヘッダー。 |
| iframe の高さ | ピクセル | ピクセル単位での iframe の高さ。 高さは必要に応じて調整できます。 |
| 請求先住所の表示 | **True** または **False** | このプロパティが **True** に設定されている場合、請求先住所は、支払モジュール iframe 内の Adyen で処理されます。 この値が **False** に設定されている場合は、請求先住所が Adyen によって処理されないため、Commerce ユーザーは、チェックアウト ページで請求先住所を表示するようにモジュールをコンフィギュレーションする必要があります。 PayPal の支払コネクタの場合、このフィールドは、PayPal で請求先住所が完全に処理されているので、影響を与えません。 |
| 支払スタイルの上書き | カスケード スタイル シート (CSS) コード | 支払モジュールは iframe でホストされるため、スタイル機能が制限されます。 このプロパティを使用すると、何らかのスタイルを実現できます。 サイト スタイルをオーバーライドするには、CSS コードをこのプロパティの値として貼り付ける必要があります。 サイト ビルダー CSS が上書きし、スタイルはこのモジュールには適用されません。 |
|サポートされている支払/入金タイプ| 文字列| 複数の支払コネクタがコンフィギュレーションされている場合は、サポートされている支払/入金タイプ文字列を Commerce 本社支払コネクタ コンフィギュレーションで定義されているとおりに提供する必要があります (この画像を参照)。 空白の場合、既定では Adyen 支払コネクタになります。 Commerce リリース 10.0.14 に追加されました。|
|基本支払|  **True** または **False** | **True** の場合、すべてのエラー メッセージは、チェックアウト ページの基本支払コネクタから生成されます。 Adyen と PayPal の両方の支払コネクタがコンフィギュレーションされている場合は、Commerce リリース 10.0.14 で追加された Adyen を **True** に設定します。|

次の図は、Commerce 本社の支払コネクタのコンフィギュレーションで "PayPal" に設定されている、**サポートされている支払/入金タイプ** の値の例を示しています。
![Commerce 本社でサポートされている支払/入金タイプの例](./media/ecommerce-paymenttendertypes.png)

## <a name="billing-address"></a>請求先住所

請求先住所モジュールは、Adyen 支払コネクタ請求先明細行がサイトの他の部分の外観と十分に一致しない場合に、チェックアウト ページで使用できます。 

支払モジュールが Adyen 支払コネクタに統合されているときに、チェックアウト ページで請求先住所モジュールを使用するには、**請求先住所の表示** プロパティを **False** に設定します。これは、請求先住所モジュールを既定の Adyen 請求先住所の代わりに使用できるようにするためです。 この場合、サイトの作成者は、チェックアウト ページに請求先住所モジュールを含める必要があります。 Adyen 支払コネクタを使用すると、配送先住所を請求先住所として使用して、サイト ユーザーの手順の数を最小限にすることもできます。

支払モジュールと同様に、**サポートされている支払/入金タイプ** のプロパティは、Commerce リリース 10.0.14 の請求先住所モジュールに追加されています。 このプロパティの値は、支払モジュールに指定されている値と同じである必要があります。この値は、一緒に動作することを保証するために使用されます。 Adyen 支払コネクタの場合、支払モジュールと請求先住所モジュールの両方でこの値を空白のままにしておく必要があります (既定の状態)。 PayPal コネクタの場合、専用の請求先住所モジュールは必要ありません。 その他のタイプの支払コネクタの場合は、その文字列を Commerce 本社でコンフィギュレーションされているものとして指定する必要があります。

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>チェックアウト ページに支払い モジュールを追加して、必要なプロパティを設定する

支払い モジュールは、チェックアウト モジュールにのみ追加できます。 チェックアウト ページをコンフィギュレーションする方法の詳細については、[チェックアウト モジュール](add-checkout-module.md) を参照してください。

Adyen と PayPal の両方の支払コネクタが必要な場合は、両方のモジュールを支払セクションに追加します。 **サポートされている支払/入金タイプ** プロパティ値が PayPal 向けにコンフィギュレーションされていることを確認し、Adyen 向けは空のままにします。 また、**基本支払** プロパティを Adyen 向けに **True** に設定します。

## <a name="additional-resources"></a>追加リソース

[カート モジュール](add-cart-module.md)

[カート アイコン モジュール](cart-icon-module.md)

[チェックアウト モジュール](add-checkout-module.md)

[出荷先住所モジュール](ship-address-module.md)

[配送オプション モジュール](delivery-options-module.md)

[集荷情報モジュール](pickup-info-module.md)

[注文詳細のモジュール](order-confirmation-module.md)

[ギフト カード モジュール](add-giftcard.md)

[Adyen 向け Dynamics 365 Payment Connector](dev-itpro/adyen-connector.md)

[PayPal 向け Dynamics 365 Payment Connector](paypal.md)

[Adyen を使用した強力な顧客認証 (SCA)](adyen_redirect.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]