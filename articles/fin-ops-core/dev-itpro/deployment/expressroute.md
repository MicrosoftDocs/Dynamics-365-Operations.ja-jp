---
title: Azure ExpressRoute および財務と運用アプリ
description: 顧客は、Microsoft Azure ExpressRoute を使用して、オンプレミス インフラストラクチャに接続できます。
author: PeterRFriis
ms.date: 09/20/2019
ms.topic: article
ms.prod: dynamics-365
ms.service: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: 260954
ms.assetid: 5dccb418-b489-4777-aa5e-2a0b03b4f2b0
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8aa28c1018f1d47ce11180a2598bba82d199e918
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103134"
---
# <a name="azure-expressroute-and-finance-and-operations-apps"></a>Azure ExpressRoute および財務と運用アプリ

[!include [banner](../includes/banner.md)]

顧客は、財務と運用アプリで Microsoft Azure ExpressRoute を使用して、オンプレミスのインフラストラクチャに接続することができます。 この記事では、ExpressRoute を使い始めるのに必要な情報を提供します。

Microsoft Azure ExpressRoute で、Azure データ センターとオンプレミスの場所の間に、専用で、すぐに使用できる、信頼性の高い、低待機時間の接続を作成できます。 ExpressRoute 回線は顧客のオンプレミス ネットワークと接続プロバイダーを通じた Microsoft クラウド サービスでの論理接続です。 ExpressRoute は、財務と運用アプリとは別に構成されます。 実装に ExpressRoute 回路を使用するには、ネットワーク サービス プロバイダーに直接問い合わせる必要があります。 ExpressRoute が構成された後、財務と運用アプリに接続することに加えて、顧客は Microsoft 365 などのアプリや、仮想マシンへの接続および仮想ネットワークに配置されたクラウド サービスなどの、サポートされている Azure サービスに接続できます。 サポートされているその他のサービスの詳細については、[ExpressRoute FAQ](/azure/expressroute/expressroute-faqs) を参照してください。 ExpressRoute 回線を購入する前に、次の情報を理解する必要があります。

- 財務と運用アプリが配置されているデータ センター。
- 接続元となるリージョン。

この情報は、ExpressRoute の標準または割増給与提供が必要かどうかを判別するために必要です。

## <a name="resources-for-getting-started"></a>概要リソース

- [ExpressRoute サービス ページ](https://azure.microsoft.com/services/expressroute/)
- [ExpressRoute 技術の概要](/azure/expressroute/expressroute-introduction)
- [ExpressRoute パートナーおよびピアリング場所](/azure/expressroute/expressroute-locations)
- [ExpressRoute の価格決定](https://azure.microsoft.com/pricing/details/expressroute/)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

