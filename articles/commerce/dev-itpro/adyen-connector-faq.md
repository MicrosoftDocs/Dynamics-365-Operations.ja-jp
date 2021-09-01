---
title: Adyen 向け Dynamics 365 Payment Connector に関するよく寄せられる質問
description: このトピックでは、Adyen 向けの Microsoft Dynamics 365 Payment Connector に関するよく寄せられる質問への回答を提供します。
author: rassadi
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: e881545e76fcfb207fa1b3d88ac2a793b2b6fbb24dc0da57240f138bc3dd8dc4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730969"
---
# <a name="dynamics-365-payment-connector-for-adyen-faq"></a>Adyen 向け Dynamics 365 Payment Connector に関するよく寄せられる質問

[!include [banner](../includes/banner.md)]

このトピックでは、Adyen 向けの Microsoft Dynamics 365 Payment Connector に関するよく寄せられる質問への回答を提供します。 Adyen 向け Dynamics 365 Payment Connector の概要については [Adyen 向け Dynamics 365 Payment Connector の概要](adyen-connector.md)を参照してください。 

### <a name="can-i-share-a-payment-terminal-with-multiple-hardware-stations"></a>複数のハードウェア ステーションを使用して支払端末を共有することはできますか。

一連番号 支払端末は、単一のハードウェア ステーションまたは POS 端末でのみ使用できます。 複数のハードウェア ステーションを単一の支払端末に接続しようとすると、ロックの問題が発生します。 支払端末を複数の POS デバイスで共有する必要がある場合は、支払端末を管理するために、IIS ハードウェア ステーションを配置する必要があります。 

### <a name="can-i-reuse-my-existing-payment-terminal-with-the-adyen-connector"></a>Adyen コネクタで既存の支払端末を再使用することはできますか。

一連番号 Adyen 支払端末は Adyen ソフトウェアと共に投入されます。 そのため、Adyen を使用して構成されていない既存の支払端末は、Adyen 向け Dynamics 365 Payment Connector で再使用することはできません。

### <a name="do-i-need-a-static-ip-address-for-the-adyen-payment-terminal"></a>Adyen 支払端末に対して静的 IP アドレスは必要ですか。

はい。 Modern POS では、Adyen 支払端末と通信するための既知の IP アドレスが必要です。 Adyen 支払端末の IP アドレスはクライアントで変更することができますが、IP アドレスの変更を続けると顕著なオーバーヘッドが生じ、業務の中断の原因となります。

### <a name="can-i-use-my-merchant-bank"></a>自分の商業銀行を使用することはできますか。

はい。 Adyen は任意の商社銀行で作業することができます。

## <a name="next-steps"></a>次のステップ

Adyen 向け Dynamics 365 Payment Connector に関する一般的な問題のトラブルシューティングについては [Adyen 向け Dynamics 365 Payment Connector のトラブルシューティング](adyen-connector-troubleshoot.md)を参照してください。 

## <a name="additional-resources"></a>追加リソース

[Adyen 向け Dynamics 365 Payment Connector の概要](adyen-connector.md)

[Adyen 向け Dynamics 365 Payment Connector の設定](adyen-connector-setup.md)

[Adyen 向け Dynamics 365 Payment Connector のトラブルシューティング](adyen-connector-troubleshoot.md)

[支払に関するよく寄せられる質問](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
