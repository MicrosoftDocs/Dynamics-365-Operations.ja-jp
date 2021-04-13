---
title: 支払 SDK でのチップのサポート
description: このトピックでは、支払ソフトウェア開発キット (SDK) での支払ターミナルのチップのサポートについて説明します。
author: rubendel
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 4fd670f8b4dd3c5aca1c3df20b823bc65bfc82e2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792917"
---
# <a name="support-for-tipping-in-the-payments-sdk"></a>支払 SDK でのチップのサポート

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce の支払ソフトウェア開発キット (SDK) が、支払ターミナルを介して入力されるチップ金額をサポートする方法について説明します。 この機能の目的は、承認の応答にチップ金額のフィールドを個別に含めることによって、支払 SDK にファーストクラスのサポートを追加することです。

この機能は、販売時点管理 (POS) でのチップまたはチップ レポートのサポートは追加されません。 完全なチップ機能を実装するには、POS 拡張機能が必要です。

## <a name="key-terms"></a>重要な用語

| 相談 | 説明 |
|---|---|
| ヒント | チップは、チップとも呼ばれ、簡易サービス業界やホスピタリティ業界では一般的です。 これにより、サービスを提供する店舗またはレストランの従業員に対して直接支払を行うことができます。 |
| ヘッダーレベルの請求金額 | 購入に適用できる料金ですが、特定の品目には適用されません。 |

## <a name="overview-of-the-tipping-feature"></a>チップ機能の概要

チップは、一部のロケールおよび業界では一般的です。 たとえば、簡易サービスとホスピタリティ業界では、チップは現在、米国のほぼすべての場所で行われています。 多くの企業にとって、支払ターミナルを介したチップをサポートする機能は、従業員を引き付けるのに役立つ重要な要素になりつつあります。 この機能は、支払 SDK に個別の **TipAmount** フィールドが追加され、支払ターミナルで選択されたチップ金額を承認の応答の一部として POS に送り返すことができます。

この機能は、支払 SDK のレベルでのチップのサポートを追加しますが、チップ機能の他の重要な側面のサポートは含まれていません。 たとえば、この機能は、シフト終了時のチップ支払いのレポート、チップをプールする機能、または給与のチップをレポートする機能をサポートしていません。 完全なチップ サポートを有効にするには、拡張機能を介してこれらの機能を実装する必要があります。

このトピックで説明されている支払ターミナル統合と SDK 参照を作成する方法の詳細については、[支払ターミナルの支払統合全体の作成](end-to-end-payment-extension.md) を参照してください。

### <a name="prerequisites"></a>必要条件

| 前提条件 | 説明 |
|---|---|
| デバイスのチップ サポート | 顧客は、支払ターミナルでチップ金額を選択できる必要があります。 |
| **isTippingEnabled** サポート | 支払いコネクタは、支払いの初期化のために **isTippingEnabled** 変数をサポートする必要があります。 |
| **TipAmount** フィールド | チップ金額は、承認応答の **TipAmount** フィールドの支払いコネクタから返される必要があります。 |
| 拡張による POS チップのサポート | 支払いコネクタから返されるチップ金額は、ヘッダーレベルの料金として販売に追加する必要があります。 チップのレポートおよび管理は、そのままでは提供されません。 |

### <a name="tipping-support-by-payment-processors"></a>支払プロセッサによるチップのサポート

この機能は、新しい **isTippingEnabled** 変数を **AuthorizePaymentTerminalDeviceRequest** リクエストに追加します。 POS から支払いが要求されると、この変数は、承認要求がチップを追加する資格があるかどうかを示します。 このリクエストを受信した支払コネクタは、接続された支払サービスまたはターミナルからチップ適格承認をリクエストできます。

**isTippingEnabled** 変数が **True** に設定されている場合、顧客が支払ターミナルでチップ金額を選択すると、その金額は支払コネクタから返される **AuthorizePaymentCardPaymentResponse** 応答の **TipAmount** フィールドに返されます。 チップ金額は、承認応答の **ApprovedAmount** フィールドにも含まれています。

### <a name="tipping-support-for-the-adyen-connector"></a>Adyen コネクタのチップ サポート

Adyen コネクタにはチップ サポートが含まれています。 承認応答がコネクターに渡されるときに **isTippingEnabled** 変数を **True** に設定するには、カスタマイズが必要です。 **isTippingEnabled** 変数が **True** に設定されている場合、顧客がデバイスでチップ金額を選択すると、その金額が承認応答の **TipAmount** フィールドに返されます。

顧客が Adyen ターミナルでチップの金額を選択するように求められる前に、ターミナルはチップ用に構成されている必要があります。 この構成は、Adyen 顧客領域を介して行われます。 チップを有効にするには、Adyen ポータルの **販売時点管理** タブを選択します。 チップは、ターミナルまたはフリート全体の **ターミナル設定** オプションを介して有効にできます。 個々のターミナルの設定とフリート全体のターミナル設定の両方で、**支払機能** タブでチップが有効になっています。Adyen デバイスでチップを有効にした後、デバイスの設定を更新する必要があります。 この更新が完了するまで、変更は有効になりません。

### <a name="suggested-implementation"></a>推奨される実装

支払いコネクタから承認応答が返された後、ヘッダーレベルの料金を使用してチップ金額をトランザクションに追加することをお勧めします。 この機能をサポートするには、**PaymentTerminalAuthorizePaymentRequestHandler** ハンドラーの拡張機能を作成する必要があります。 その拡張機能には、承認応答で **TipAmount** 値が返された場合に、取引にヘッダーレベルの料金を追加するロジックを含める必要があります。

## <a name="additional-resources"></a>追加リソース

- [Adyen コネクタの概要](adyen-connector.md?tabs=10-0-14.md)
- [支払端末のエンド・ツー・エンド支払統合を作成する](end-to-end-payment-extension.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]