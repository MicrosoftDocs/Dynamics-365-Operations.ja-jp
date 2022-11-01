---
title: モジュールのエラー参照コードのチェックアウト
description: この記事では、Microsoft Dynamics 365 Commerce でユーザー が表示するエラー メッセージで表示されるチェック アウト モジュールのエラー参照コードについて説明します 。
author: BrianShook
ms.date: 10/20/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: cd8269a71e56f23dbe3782ec3ffc69ec3ea6b151
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709666"
---
# <a name="checkout-module-error-reference-codes"></a>モジュールのエラー参照コードのチェックアウト

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Commerce でユーザー が表示するエラー メッセージで表示されるチェック アウト モジュールのエラー コードについて説明します 。

Dynamics 365 Commerce では、オンライン顧客に表示されるオンライン チャンネルのチェック アウト エラーに含まれる標準化されたエラー参照が導入されています。 Commerce Version 10.0.31 以降では、チェック アウト モジュールのエラー メッセージにエラー コードが含まれるので、オンライン顧客に対して不必要な情報は表示されません。 このエラー コードは、この記事で詳細が表示されるエラーを参照します。

発生したエラーに応じて、この記事の表に次の詳細が含まれています。

- エラーの原因となる状況の説明、または追加の詳細
- 環境または支払コネクタ構成で考慮する情報
- 追加支援が必要な場合にサポート ケースで参照できる情報

## <a name="checkout-module-error-reference-codes"></a>モジュールのエラー参照コードのチェックアウト

顧客によって提供またはオンライン店舗で経験したエラー コード参照に関する詳細を取得するには、次の表を使用します。

| エラー コード | Dynamics に関連付けられたエラー コード | エラーの説明 |
| ---------- | ------------------------------ | ----------------- |
| CCR001     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardTypeMissingOrNotSupported | 支払が承認できませんでした。 **TokenizedPaymentCard** にカード タイプ ID がないか、提供されたカードタイプ ID がサポートされていません。 |
| CCR002     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePayment | 却下されました。 支払が承認できませんでした。 |
| CCR003     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardAdditionalContextRequired | 支払が承認できませんでした。 顧客から必要とされる追加情報。 |
| CCR004     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToRetrieveCardPaymentAcceptResult | 問題が発生しました。 カード支払による支払の結果を得ることができませんでした。 やり直すか、システム管理者に問い合わせてください |
| CCR005     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentRequiresMerchantProperties | マーチャント支払プロパティが見つからないため、支払を行うことができません。 システム管理者にお問い合わせください。 |
| CCR006     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidPaymentRequest | 操作の支払/入金サービスを取得できません。 選択した支払/入金タイプに対する支払方法の設定を確認します。 |
| CCR007     | Microsoft\_Dynamics\_Commerce\_Runtime\_MultipleCustomerAccountPaymentsNotAllowed | 顧客口座支払は既に適用されており、トランザクションごとに 1 つの支払だけ許可されます。 |
| CCR008     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountLimitSignDifferentFromAromA Due | 顧客勘定の限度額が支払金額と異なる。 別の支払方法を使用するか、カスタマ サポートに問い合わせてください。 |
| CCR009     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsTotalAmountForCarryOutAndReturnItems | 顧客勘定の支払が、一覧表示された品目に対する合計期日を超えている。 後でやり直すか、カスタマ サポートに問い合わせてください。 |
| CCR010     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentUsingUnauthorizedAccount | 顧客口座支払では、支払/入金明細行に自身の口座または対応する請求先/元 ID がある必要があります。 |
| CCR011     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsCustomerAccountFloorLimit | 現在、顧客口座支払を処理できません。フロア制限を超えています。 |
| CCR012     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentForCustomerWithoutAllowOnAccount | この顧客はアカウント上の支払が許可されていません。 |
| CCR013     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToCancelPayment | 問題が発生しました。 支払がキャンセルできませんでした。 やり直してください |
| CCR014     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToReadCardTokenInfo | 支払の処理中にエラーが発生しました。 後でやり直してください。 |
| CCR015     | Microsoft\_Dynamics\_Commerce\_Runtime\_NotEnoughRewardPoints | ロイヤルティ支払額が、このトランザクションで使用したロイヤルティ カードに許可されている金額を超えています。 |
| CCR016     | Microsoft\_Dynamics\_Commerce\_Runtime\_RefundAmountMoreThanAllowed | ロイヤルティ払戻額が、このトランザクションで使用したロイヤルティ カードに許可されている額を超えました。 |
| CCR017     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidLoyaltyCardNumber | ロイヤルティ カード番号が見つかりませんでした。 ロイヤルティ カード番号を有効化するか、別のカード番号を入力して、もう一度実行してください。 |
| CCR018     | Microsoft\_Dynamics\_Commerce\_Runtime\_BlockedLoyaltyCard | このロイヤリティー カード番号は利用できません。 異なるカード番号を入力してから、再試行してください。 |
| CCR019     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoTenderLoyaltyCard | このロイヤルティ カードは、このトランザクションのロイヤルティ ポイントの引換には使用できません。 |
| CCR020     | Microsoft\_Dynamics\_Commerce\_Runtime\_GiftCardCurrencyMismatch | ギフト カード番号にエラーが発生しました。 異なるギフト カードを使用するか、カスタマ サポートに問い合わせてください。 |
| CCR021     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAmountExceedsGiftBalance | ギフト カード残高を超える金額です。 異なる額を入力してから、再試行してください。 |
| CCR022     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoMoreThanOneLoyaltyTender | トランザクションに複数のロイヤルティ支払明細行を含めることはできません。 |
| CCR023     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAlreadyVoided | 支払情報に情報が見つからないか、間違っています。 支払情報を確認してからやり直してください。 |
| CCR024     | Microsoft\_Dynamics\_Commerce\_Runtime\_FraudRisk | このオーダーは現時点では処理できません。 後でやり直してください。 |
| CCR025     | チェックアウト API のフロントエンド タイムアウト | フロントエンド操作はタイム アウトされました。オーダーが Dynamics 365 Commerce headquarters で処理されたどうか確認します。 |
| CCR026     | 変更された元の承認済金額 | このオーダー金額は、支払ゲートウェイで処理された元の認証金額から変更されています。 これは、クーポン、プロモーション、または販売の期限が期限を過ぎた場合があります。 |
| CCR027     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidCartVersion | 支払の処理中にエラーが発生しました。 カート API に提供された参照は予想とは異なる参照です (チェックアウトプロセス中に不整合が生じる可能性があります)。 |
| CCR028     | Microsoft\_Dynamics\_Commerce\_Runtime\_MissingRequiredCartTenderLines | 試行された支払方法でエラーが発生しました。 アカウント設定を確認するか、別の支払方法でもう一度やり直す場合は、サポートに問い合わせください。 |

## <a name="additional-resources"></a>追加リソース

[支払に関するよく寄せられる質問](dev-itpro/payments-retail.md)

[チェックアウト モジュール](add-checkout-module.md)

[支払モジュール](payment-module.md)
