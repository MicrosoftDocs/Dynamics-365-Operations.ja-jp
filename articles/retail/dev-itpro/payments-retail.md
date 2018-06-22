---
title: "支払の FAQ"
description: "このトピックでは、Dynamics 365 for Operations for Retail で使用できる支払オプションについて説明します。"
author: athinesh99
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 65801
ms.assetid: 99079d81-fde2-4432-8cee-82bbcc3bd57e
ms.search.region: Global
ms.author: athinesh
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: b05d769fab80ad4b31125f4f51c4a1372b557a4a
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---
# <a name="payments-faq"></a>支払の FAQ

[!include [banner](../../includes/banner.md)]

## <a name="what-payment-scenarios-are-supported"></a>どのような支払シナリオがサポートされますか ?
- マーチャント口座を設定します。
- コール センター注文を処理します。
- オフライン注文を処理します。
- 受諾ページを使用して、POS 現金払い取引を処理します。
- 受諾ページを使用して、POS 現金払い返品を処理します。
- 受諾ページを使用して、POS 現金払い返品を処理します。
- 受諾ページを使用して POS 顧客注文を処理します。
- Microsoft Dynamics AX 2012 Retail ハードウェア ステーションを使用して、POS 現金払いトランザクションを処理します。
- ハードウェア ステーションを使用して、POS 現金払い返品を処理します。
- ハードウェア ステーションを使用して POS 顧客注文を処理します。

        
## <a name="which-payment-providers-are-supported-and-in-what-regions"></a>どの支払プロバイダーがどの地域でサポートされていますか。
- Verifoneは、カードが存在する取引 (デバイスを使用してを実行) 、およびカードが存在しない取引 (電子商取引やコールセンター取引など) のために米国でサポートされています。
- カードが次の国に存在しない場合、トランザクションでは Mastercard がサポートされています: オーストラリア、カナダ、デンマーク、フランス、ドイツ、アイスランド、アイルランド、メキシコ、オランダ、ニュージーランド、南アフリカ、英国、および米国。


## <a name="what-is-a-payment-connector-and-in-what-cases-do-i-need-to-deploy-and-implement-a-payment-connector"></a>支払コネクタとは何ですか、またどのような場合に支払コネクタの配置と実装が必要ですか ?
支払コネクタは、カードが存在しないトランザクションとカードが存在するトランザクションの支払いをアプリケーションが処理できるようにする、設定可能なソフトウェア コンポーネントです。

Verifone および MasterCard などの Microsoft によって指定されたコネクタを使用するか、ISV パートナーがカスタム コネクタを構築することができます。 コネクタは通常、顧客の業務でのニーズを満たすために構築されます。 新しいタイプの支払いタイプ (リンク払い戻しなど) が必要なシナリオがある場合、カスタム コネクタが作成されることがあります。 特定の地域でビジネスを行っている顧客は、最初から用意されているコネクタがこれらの地域をサポートしていない場合、新しいコネクタが必要になることがあります。
          
## <a name="are-other-payment-connector-providers-supported"></a>その他の支払コネクタ プロバイダーはサポートされていますか。
はい、ただしカスタマイズを使用してそれらを接続する必要があります。

## <a name="what-is-the-service-level-agreement-sla-for-out-of-box-payment-connectors-like-verifone-and-mastercard"></a>Verifone および Mastercard などの標準の支払いコネクタのサービス レベル アグリーメント (SLA) とは何ですか ?
Verifone や Mastercard などの標準コネクタの SLA は、支払コネクタ プロバイダー自体によって所有されます。 その SLA については、Verifone または Mastercard サポートにお問い合わせください。
        
## <a name="if-a-supported-payment-provider-issues-an-update-will-microsoft-automatically-update-the-payment-connector-or-do-i-need-to-work-with-the-payment-provider-to-get-the-updated-payment-connector"></a>サポートされている支払プロバイダーが更新プログラムを発行した場合は、Microsoft は自動的に支払コネクタを更新してくれますか? または更新された支払コネクタを取得するために支払プロバイダーと連携する必要がありますか。
支払いコネクターの更新プログラムが支払コネクター プロバイダーによって発行された場合、支払いコネクターの更新バージョンは Dynamics 365 for Retail の次の予定リリースに含まれます。 ただし、顧客は早期に取得するため、支払コネクタ プロバイダと直接作業することもできます。

        
関連トピック: 
- [Dynamics AX 2012 ホワイト ペーパー用の支払コネクタと支払デバイスの実装](http://download.microsoft.com/download/4/D/7/4D7C6B05-0C23-4C6C-BA13-AB62ED08AA61/The%20Guide%20to%20Implementing%20Payment%20Connector%20and%20Payment%20Device.docx)
- [支払コネクタの配置](deploy-payment-connector.md)
- [支払コネクタ用の Windows インストーラーの作成](create-windows-installer-payment-connector.md)
- [Verifone 支払コネクタ](https://dynamics.verifone.com/repo/)
- [MasterCard 支払コネクタ](https://www.simplify.com/microsoft/) 

