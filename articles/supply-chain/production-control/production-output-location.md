---
title: 生産出荷場所
description: この記事では、生産出荷場所を識別するために使用される階層について説明します。
author: johanhoffmann
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5bfabae39d3bcb8f7fdd71ac5c93fcdbaeb9d946
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893297"
---
# <a name="production-output-location"></a>生産出荷場所

[!include [banner](../includes/banner.md)]

この記事では、生産出荷場所を識別するために使用される階層について説明します。

生産出荷場所は、完成品が生産された後に最初に保管される場所です。 通常、この場所は完成品を生産する生産工程の近くにあります。 生産出荷場所は、出荷エリア、保管場所、下流生産プロセスの生産入庫場所などに移動する前に、品目の中間保管として使用されます。 

既定の生産出荷場所は、完成品が製造オーダーまたはバッチ オーダーで報告されたときに設定されます。 次の階層を使用して、この出荷場所を識別します。

1. 製造オーダーまたはバッチの注文ヘッダーで定義されている出荷場所を使用します。
2. そこに場所が見つからない場合は、本番ルートで定義されている最後の操作により使用されているリソースで定義されている出荷場所を使用します。
3. そこに場所が見つからない場合は、本番ルートで定義されている最後の操作のリソースにより使用されているリソース グループで定義されている出荷場所を使用します。
4. そこに場所が見つからない場合は、製造オーダーに定義されている倉庫で定義されている出荷場所を使用します。

既定の生産出荷場所は、高度な倉庫プロセスを使用して設定されている製品にのみ設定されます。 このタイプの品目が完了報告されると、**商品の保存を完了** または **連産品および副産物の保存** タイプの倉庫作業が作成されます。 このタイプの作業は、ピッキング場所として生産出荷場所を使用します。 プット アウェイの場所は、場所ディレクティブによって決定されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]