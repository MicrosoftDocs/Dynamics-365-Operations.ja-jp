---
title: Adyen 向け Dynamics 365 Payment Connector に関するよく寄せられる質問
description: このトピックでは、Adyen 向けの Microsoft Dynamics 365 Payment Connector に関するよく寄せられる質問への回答を提供します。
author: rassadi
ms.date: 09/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: v-chgri
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 63aa76116a30431e836cbe836679310969bff542
ms.sourcegitcommit: 49f29aaa553eb105ddd5d9b42529f15b8e64007e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2021
ms.locfileid: "7592474"
---
# <a name="dynamics-365-payment-connector-for-adyen-faq"></a>Adyen 向け Dynamics 365 Payment Connector に関するよく寄せられる質問

[!include [banner](../includes/banner.md)]

このトピックでは、Adyen 向けの Microsoft Dynamics 365 Payment Connector に関するよく寄せられる質問への回答を提供します。 Adyen 向け Dynamics 365 Payment Connector の概要については [Adyen 向け Dynamics 365 Payment Connector の概要](adyen-connector.md)を参照してください。 

### <a name="can-i-share-a-payment-terminal-with-multiple-hardware-stations"></a>複数のハードウェア ステーションを使用して支払端末を共有することはできますか。

一連番号 支払端末は、単一のハードウェア ステーションまたは販売時点管理 (POS) 端末でのみ使用できます。 複数のハードウェア ステーションを単一の支払端末に接続しようとすると、ロックの問題が発生します。 支払端末を複数の POS デバイスで共有する必要がある場合は、支払端末を管理するために、IIS ハードウェア ステーションを配置する必要があります。 

### <a name="can-i-reuse-my-existing-payment-terminal-with-the-adyen-connector"></a>Adyen コネクタで既存の支払端末を再使用することはできますか。

一連番号 Adyen 支払端末は Adyen ソフトウェアと共に投入されます。 そのため、Adyen を使用して構成されていない既存の支払端末は、Adyen 向け Dynamics 365 Payment Connector で再使用することはできません。

### <a name="do-i-need-a-static-ip-address-for-the-adyen-payment-terminal"></a>Adyen 支払端末に対して静的 IP アドレスは必要ですか。

はい。 Modern POS では、Adyen 支払端末と通信するための既知の IP アドレスが必要です。 Adyen 支払端末の IP アドレスはクライアントで変更することができますが、IP アドレスの変更を続けると顕著なオーバーヘッドが生じ、業務の中断の原因となります。

### <a name="can-i-use-my-merchant-bank"></a>自分の商業銀行を使用することはできますか。

はい。 Adyen は任意の商社銀行で作業することができます。

### <a name="when-i-configure-card-type-bin-range-mapping-in-commerce-for-the-adyen-connector-how-many-digits-can-i-use"></a>Adyen コネクター用に Commerce でカード タイプの BIN 範囲マッピングを構成する場合、使用できる桁数はどのくらいですか?

Adyen は、カードの最初の 6 桁を照合のために返します。 Adyen 向け Dynamics 365 Payment Connector を使用する場合、カード タイプの BIN 範囲のマッピングの最大値は 6 桁です。

### <a name="how-do-commerce-transaction-events-align-with-adyen-payment-status-codes"></a>Commerce トランザクション イベントは Adyen 支払ステータス コードとどのように対応しますか?

次の表に、Adyen ポータルの「支払」セクションに示されている Dynamics 365 Commerce の一般的な支払イベントとそれに対応する支払ステータス コードを示します。

#### <a name="pos-terminal"></a>POS 端末

| Commerce イベント | Adyen 支払ステータス コード |
|---|---|
| 進行中の初期トランザクション | **AuthorisedPending** |
| 正常なトランザクション | **承認済** |
| 進行中の正常なトランザクション | **SentForSettle** |
| 完了した正常なトランザクション | **決済済** |
| 無効 | **キャンセル済** (承認済の状態のみ) または **払戻済** (資金が取り込みされている場合) |
| キャンセル | キャンセル済みの品目は、Adyen ポータルに表示することは求められません。 |
| リンクされた払戻 | **SentForRefund** または **払戻済** |
| リンクされていない払戻し | 元の支払明細行が最終状態に残ります (たとえば、**承認済**)。 新しい行には、使用されている支払方法の **RefundPending** が表示されます。 |
| 支払方法としての外部ギフト カード | **SettledExternally** |
| 外部ギフト カードの資金追加 | **RefundPending** |

#### <a name="call-center-and-online-channels"></a>コール センターおよびオンライン チャネル

| コマース イベント | Adyen 支払ステータス コード |
|---|---|
| 正常なトランザクション | **承認済** |
| 認証 | **決済済** |
| 無効 | **キャンセル済** (承認済の状態のみ) または **払戻済** (資金が取り込みされている場合) |
| キャンセル | キャンセル済みの品目は、Adyen ポータルに表示することは求められません。 |
| リンクされた払戻 | **SentForRefund** または **払戻済** (*コール センターのみ*) |
| リンクされていない払戻 | 元の支払明細行が最終状態に残ります (たとえば、**承認済**)。 新しい行には、使用されている支払方法の **RefundPending** が表示されます。 (*コール センターのみ*) |
| 支払方法としての外部ギフト カード | **SettledExternally** |
| 外部ギフト カードの資金追加 | **RefundPending** |

Adyen が決済済の状態で支払の発生元のサービスを処理している場合でも、コール センターおよびオンライン店舗では支払が成功したと見なされます。

Adyen 支払ステータス コードの完全な一覧については、[支払のライフサイクル](https://docs.adyen.com/account/payments-lifecycle) を参照してください。

## <a name="next-steps"></a>次のステップ

Adyen 向け Dynamics 365 Payment Connector に関する一般的な問題のトラブルシューティングについては [Adyen 向け Dynamics 365 Payment Connector のトラブルシューティング](adyen-connector-troubleshoot.md)を参照してください。 

## <a name="additional-resources"></a>追加リソース

[Adyen 向け Dynamics 365 Payment Connector の概要](adyen-connector.md)

[Adyen 向け Dynamics 365 Payment Connector の設定](adyen-connector-setup.md)

[Adyen 向け Dynamics 365 Payment Connector のトラブルシューティング](adyen-connector-troubleshoot.md)

[支払に関するよく寄せられる質問](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
