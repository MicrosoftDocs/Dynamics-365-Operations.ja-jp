---
title: チャネルの概要
description: この記事では、Microsoft Dynamics 365 Commerce のチャネルの概要を表示します。
author: samjarawan
ms.date: 01/27/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: af5089f0065610873360b2e2883928a43600caa9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884640"
---
# <a name="channels-overview"></a>チャネルの概要


[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce のチャネルの概要を表示します。 ここでは、各チャネルを設定する前と後の、実施する必要のあるタスクについて説明します。

## <a name="types-of-channels"></a>チャネルのタイプ

Dynamics 365 Commerce は、小売、コール センター、およびオンライン チャネルという 3 つのチャネル タイプがサポートされています。

### <a name="retail-channels"></a>小売チャネル

小売チャネルは、従来型の店舗を表します。 各店舗は、独自の販売時点管理 (POS)、収入/経費勘定、およびスタッフを持つことができます。 

### <a name="call-center-channels"></a>コール センター チャネル

コール センター チャネルは、コール センターの注文と顧客管理を表します。

### <a name="online-channels"></a>オンライン チャネル

オンライン チャネルは、オンライン電子商取引店舗を表します。 オンライン チャネルを作成した後、Microsoft Dynamics 365 Commerce サイト ビルダー ツールまたはその他のサードパーティの電子商取引ソリューションを使用してサイトを作成する必要があります。

## <a name="channel-setup-basics"></a>チャネル設定の基本

チャネルの設定は、Commerce ツールで実行されます。 各チャネルごとに、独自の支払方法、価格グループ、製品階層、品揃え、および一連の製品を設定できます。 チャネルを作成したら、そのチャネルで配送および販売する製品を割り当てます。 チャネル タイプごとに、コンフィギュレーションする必要がある固有の機能セットがあります。 たとえば、小売チャネルには従業員、レジスター、および顧客が割り当てられている必要があります。 新しいチャネルを作成したら、それを組織階層に割り当てる必要があります。

## <a name="channel-setup-prerequisites"></a>チャネル設定の前提条件

チャネルを設定する前に、チャネル タイプに基づいていくつかの前提条件タスクを完了しておく必要があります。 詳細については、[チャネル設定の前提条件](channels-prerequisites.md) を参照してください。

## <a name="set-up-a-channel"></a>チャネルの設定

前提条件のタスクを完了した後、セットアップ手順の詳細については、次のリンクを使用してください。

- [小売チャネルの設定](channel-setup-retail.md)
- [コール センターのチャネルの設定](channel-setup-callcenter.md)
- [オンライン チャネルの設定](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a>追加リソース

[チャネル設定の前提条件](channels-prerequisites.md)

[小売チャネルの設定](channel-setup-retail.md)
    
[オンライン チャネルの設定](channel-setup-online.md)

[コール センターのチャネルの設定](channel-setup-callcenter.md)

[組織階層の設定](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]