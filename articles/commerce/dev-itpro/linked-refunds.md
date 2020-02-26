---
title: リンクされた払戻 - 以前に承認および確認済みのトランザクションの払戻
description: このトピックでは、リンクされた払戻を有効にして使用する方法を説明します。
author: josaw1
manager: AnnBe
ms.date: 7/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-03-28
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: eb3d2d9cf6aaa6e8aacf6e0ffaff2d67eae9709d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004567"
---
# <a name="linked-refunds--refunds-of-previously-approved-and-confirmed-transactions"></a>リンクされた払戻 – 以前に承認および確認済みのトランザクションの払戻

[!include [banner](../../includes/banner.md)]

返品は小売企業にとって重要な業務です。 販売に対する返品を受け入れて顧客への支払いを払い戻す機能により、小売企業は顧客のニーズに対応して問題を解決できます。

このトピックでは、リンクされた払戻を構成および使用する方法に関する情報を提供します。 リンクされた払戻は、以前に承認および確認されたトランザクションの払戻です。 払戻は、トランザクションの全額払戻、または部分払戻のいずれかで、元の承認の全額を超えることはできません。 リンクされた払戻の機能は、Microsoft Dynamics 365 Retail バージョン 10.0.1 で利用できます。

Microsoft Dynamics 365 Retail バージョン 10.0 以前では、小売企業はカードへの払い戻しを処理できますが、レジ担当者はこれらの払戻を手動で指定する必要があります。 レジ担当者は顧客がその支払い方法を提供した場合にのみ、元の支払い方法への払戻を処理できます。 したがって、新しいカードの詳細を提供することにより、顧客は返品プロセスを使用してあるカードから別のカードに残高を移動できるため、不正なカード残高の移動を行うことができます。

リンクされた払戻を使用することで、元のトランザクション中に承認されたカードのみに払戻が処理されるようにして、小売業者はリスクを大幅に軽減できます。 承認されていないカード残高の転送を防止するために、システムは確認され承認されたカード トークンを使用して払戻を処理するようレジ担当者に促すことができます。 払戻に元の支払い方法を使用することで小売企業はカード認証コストを削減できます。

## <a name="prerequisites"></a>必要条件
[支払方法の設定](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/payment-methods) 

[オムニ チャネル支払の設定](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/omni-channel-payments)

### <a name="additional-setup"></a>追加の設定

標準の Adyen コネクタ実装を使用していない顧客は、クレジットカードのトークン化をサポートするコネクタを設定する必要があります。 このトピックで説明されるすべてのシナリオは、コマースで提供される標準の支払ソフトウェア開発キット (SDK) を使用して実装できます。 [Dynamics 365 Payment Connector for Adyen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3) では、こちらで説明されるすべてのシナリオの直ぐに使える実装を提供します。

## <a name="turn-on-the-linked-refunds-functionality"></a>リンクされた払戻の機能を有効にする

リンクされた払戻機能は、Microsoft Dynamics 365 Retail 8.1.3 以降で利用可能なオムニチャネル支払い機能と連携します。

リンクされた払戻機能を有効にするには **Retail とコマース \> バックオフィスの設定 \> パラメーター \> コマース共有パラメーター**に移動します。 **オムニ チャネル支払い** タブで **オムニ チャネル支払いを使用する** オプションを **はい** に設定します。

![オムニチャネル支払いの構成](media/LinkedRefundsOmniChannel.jpg)

オムニチャネル支払い機能をオンにすると、配送料とその他の料金を計算して料金を販売時点管理 (POS) 販売に追加するビジネス プロセス フローを変更します。 したがって、この機能を有効にする前に従業員のテストとトレーニングが必要です。

オムニチャネル支払い機能が有効の場合、1 つのチャネル (たとえば、コールセンターや Modern POS (MPOS)) で使用されるカード支払いトークンは、小売企業に設定されたすべてのチャネルで使用可能になります。 POS アプリケーションの場合は、リンクされた払戻機能も有効になります。 コールセンター、MPOS、E コマース アプリケーションの場合、顧客は支払い用のカード番号を手動で入力することもできます。

### <a name="supported-flows"></a>サポートされているフロー

レジ担当者は、返品のためにカードが提示されない場合も元のトランザクションで使用されたカードへの払戻を処理できます。

- クレジットカードやデビットカードを使用する現金払いトランザクションのリンクされた払戻
- クレジットカードやデビットカードを使用する顧客注文のリンクされた払戻
 
### <a name="unsupported-flows"></a>サポートされないフロー

- ギフト カードを使用するトランザクションのリンクされた払戻
- ロイヤルティ カードを使用するトランザクションのリンクされた払戻
- 交換注文のリンクされた払戻
- 同じトランザクションでの複数の返品注文
- レシートや顧客アカウントの詳細なしでの返品

## <a name="use-case-examples"></a>ユース ケース例

このセクションでは、顧客注文やレシートが提示される返品のコンテキストで、リンクされた払戻と支払い承認の構成と使用の理解に役立つユース ケースの例を示します。 これらの例は **オムニ チャネル支払** パラメーターが有効なときのアプリケーションの動作を示します。

### <a name="customer-accountbased-or-receipt-based-return-that-has-a-single-card-authorization"></a>単一のカード認証を持つ顧客アカウント ベースまたはレシート ベースの返品

顧客は単一のクレジット カードを使用して購入したアイテムを返品します。 顧客はレシートを提出し、返品が許可された期間内で返品が行われます。 レジ担当者がレシートをスキャンすると、返品するアイテムが処理されます。 レジ担当者が支払い方法のボタンを選択して支払いの払戻を処理すると、既存のクレジットカード認証が表示されます。

![単一のカード認証](media/LinkedRefundsSingleAuthorization.jpg)

レジ係がクレジットカード認証を選択すると、支払いの払戻が処理され **トランザクションの終了** 画面が表示されます。 レシートの印刷が構成されている場合、レジ担当者はレシートを印刷するように求められます。

### <a name="customer-accountbased-or-receipt-based-return-that-has-multiple-card-authorizations"></a>複数のカード認証を持つ顧客アカウント ベースまたはレシート ベースの返品

顧客は複数のクレジット カードを使用して購入したアイテムを返品します。 レジ担当者がレシートをスキャンすると、返品するアイテムが処理されます。 レジ担当者が支払い方法のボタンを選択して支払いの払戻を処理すると、既存のクレジットカード認証がすべて表示されます。

![複数のカード認証](media/LinkedRefundsMultipleAuthorization.jpg)

レジ担当者がクレジットカード認証を選択すると、支払いの払戻が処理されます。 さらに返金する必要がある場合、現在のトランザクション画面に残額が表示されます。 レジ担当者がこの金額の支払いの払戻を処理すると、残りのクレジットカードの承認が表示されます。 このプロセスは払戻が必要な残額がなくなるまで続きます。

全額払戻が成功したら、レジ担当者はトランザクションを完了して構成済としてレシートを印刷できます。

## <a name="related-topics"></a>関連トピック

- [支払に関するよく寄せられる質問](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
- [Adyen 向け Dynamics 365 Payment Connector](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3)
