---
title: 支払いモジュール
description: このトピックでは、支払いモジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: f4f6baa3c4a42a2994cab772c98d373996e2648b
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661213"
---
# <a name="payment-module"></a>支払いモジュール

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

このトピックでは、支払いモジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。

## <a name="overview"></a>概要

支払モジュールにより、顧客はクレジット カードやデビット カードを使用して注文の支払を行うことができます。 このモジュールの支払い統合は、 Dynamics 365 Payment Connector によって提供されます。 支払いコネクタを設定および構成方法についての詳細は、[Adyen 用の Dynamics 365 Payment Connector ](dev-itpro/adyen-connector.md) を参照してください。

支払モジュールは、HTML インライン フレーム (iframe) でAdyen 経由で提供される支払情報をホストします。 支払モジュールは、Commerce Scale Unit とやり取りして、Adyen 支払情報を取得します。 Commerce Scale Unit のやり取りの一部として、支払モジュールでは、入力した請求先住所情報を iframe で処理するか、別のモジュールとして処理するかを指定できます。 Fabrikam テーマでは、請求先住所が別のモジュールに表示されます。 この方法を使用すると、住所の行を出荷先住所の行と類似したものに表示することができるので、書式設定上の柔軟性が高まります。

支払モジュールでは、顧客は支払情報を保存することもできます。 支払情報と請求先住所は、Adyen 支払コネクタを介して保存および管理されます。

支払モジュールは、ロイヤルティ ポイントまたはギフトカードで既にカバーされていない注文費用を対象とします。 注文の合計がロイヤルティ ポイントまたはギフトカード クレジットによって完全に覆われている場合は、支払モジュールが非表示になり、顧客は注文をそのままにすることができます。

Adyen 支払いコネクタは強力な顧客認証 (SCA) もサポートします。 欧州連合 (EU) 決済サービス指令 2.0 (PSD 2.0) の一部では、オンラインで買い物をする人は電子決済方法で決済する場合、自分たちのオンライン ショッピング体験以外で認証を受けることを義務付けています。 チェックアウト フローでは、顧客は銀行のサイトにリダイレクトされます。 その後、認証後に Commerce のチェックアウト フローにリダイレクトされます。 このリダイレクトでは、顧客がチェックアウト フローに入力した情報 (たとえば、出荷先住所、配送オプション、ギフトカード情報、ロイヤルティ情報など) が維持されます。 この機能を有効にするには、Commerce 本社の SCA 用に支払コネクタをコンフィギュレーションする必要があります。 詳細については、[Adyen を使用した強力な顧客認証](adyen_redirect.md) を参照してください。

次の図は、チェックアウト ページのギフト カード、ロイヤルティ ポイント、支払モジュールの例を示しています。

![チェックアウト ページのギフト カード、ロイヤルティ ポイント、支払モジュールの例](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a>支払モジュールのプロパティ

| プロパティ名 | 値 | 説明 |
|---------------|--------|-------------|
| ヘッダー | ヘッダー テキスト | 支払いモジュールのオプション ヘッダー。 |
| iframe の高さ | ピクセル | ピクセル単位での iframe の高さ。 高さは必要に応じて調整できます。 |
| 請求先住所の表示 | **True** または **False** | このプロパティが **True** に設定されている場合、請求先住所は、支払モジュール iframe 内の Adyen で処理されます。 この値が **False** に設定されている場合は、請求先住所が Adyen によって処理されないため、Commerce ユーザーは、チェックアウト ページで請求先住所を表示するようにモジュールをコンフィギュレーションする必要があります。 |
| 支払スタイルの上書き | カスケード スタイル シート (CSS) コード | 支払モジュールは iframe でホストされるため、スタイル機能が制限されます。 このプロパティを使用すると、何らかのスタイルを実現できます。 サイト スタイルをオーバーライドするには、CSS コードをこのプロパティの値として貼り付ける必要があります。 サイト ビルダー CSS が上書きし、スタイルはこのモジュールには適用されません。 |

## <a name="billing-address"></a>請求先住所

支払モジュールを使用すると、顧客は支払情報の請求先住所を指定できます。 また、請求先住所として配送先住所を使用することもできます。この場合、チェックアウト フローをより簡単かつ迅速にすることができます。 **請求先住所の表示** プロパティが、**False** に設定されている場合は、支払モジュールをチェックアウト ページでコンフィギュレーションする必要があります。

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>チェックアウト ページに支払い モジュールを追加して、必要なプロパティを設定する

支払い モジュールは、チェックアウト モジュールにのみ追加できます。 チェックアウト ページをコンフィギュレーションする方法の詳細については、[チェックアウト モジュール](add-checkout-module.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[買い物カゴ モジュール](add-cart-module.md)

[買い物カゴ アイコン モジュール](cart-icon-module.md)

[チェックアウト モジュール](add-checkout-module.md)

[配送先住所モジュール](ship-address-module.md)

[配送オプション モジュール](delivery-options-module.md)

[注文詳細のモジュール](order-confirmation-module.md)

[ギフト カード モジュール](add-giftcard.md)

[Adyen 向け Dynamics 365 Payment Connector](dev-itpro/adyen-connector.md)

[Adyen を使用した強力な顧客認証 (SCA)](adyen_redirect.md)
