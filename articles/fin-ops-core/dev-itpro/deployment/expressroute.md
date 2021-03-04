---
title: Azure ExpressRoute と Finance and Operations アプリ
description: 顧客は、Microsoft Azure ExpressRoute を使用して、オンプレミス インフラストラクチャに接続できます。
author: PeterRFriis
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: 260954
ms.assetid: 5dccb418-b489-4777-aa5e-2a0b03b4f2b0
ms.search.region: Global
ms.author: perahlff
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: da0af411f7770d523026a454c71930dbac974f9b
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127664"
---
# <a name="azure-expressroute-and-finance-and-operations-apps"></a>Azure ExpressRoute と Finance and Operations アプリ

[!include [banner](../includes/banner.md)]

顧客は、 Finance and Operations アプリで Microsoft Azure ExpressRoute を使用して、オンプレミス インフラストラクチャに接続することができます。 このトピックでは、ExpressRoute を使い始めるのに必要な情報を提供します。

Microsoft Azure ExpressRoute で、Azure データ センターとオンプレミスの場所の間に、専用で、すぐに使用できる、信頼性の高い、低待機時間の接続を作成できます。 ExpressRoute 回線は顧客のオンプレミス ネットワークと接続プロバイダーを通じた Microsoft クラウド サービスでの論理接続です。 ExpressRoute は、 Finance and Operations とは別に構成されています。 実装に ExpressRoute 回路を使用するには、ネットワーク サービス プロバイダーに直接問い合わせる必要があります。 ExpressRoute が構成された後、Finance and Operations アプリに接続することに加えて、顧客は Microsoft 365 などのアプリや、仮想マシンへの接続や仮想ネットワークに配置されたクラウド サービスなどの対応している Azure サービスに接続できます。 サポートされているその他のサービスの詳細については、[ExpressRoute FAQ](/azure/expressroute/expressroute-faqs) を参照してください。 ExpressRoute 回線を購入する前に、次の情報を理解する必要があります。

- Finance and Operations アプリが配置されているデータ センター。
- 接続元となるリージョン。

この情報は、ExpressRoute の標準または割増給与提供が必要かどうかを判別するために必要です。

## <a name="resources-for-getting-started"></a>概要リソース

- [ExpressRoute サービス ページ](https://azure.microsoft.com/services/expressroute/)
- [ExpressRoute 技術の概要](https://azure.microsoft.com/documentation/articles/expressroute-introduction/)
- [ExpressRoute パートナーおよびピアリング場所](https://azure.microsoft.com/documentation/articles/expressroute-locations/)
- [ExpressRoute の価格決定](https://azure.microsoft.com/pricing/details/expressroute/)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]