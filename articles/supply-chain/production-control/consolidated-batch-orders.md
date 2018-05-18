---
title: "連結バッチ オーダー (複数)"
description: "この記事は、連結バッチ注文の概念について説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d6ee4ea9c8af06c493d906887f5ed6f7874e703e
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="consolidated-batch-orders"></a>連結バッチ オーダー (複数)

[!include [banner](../includes/banner.md)]

この記事は、連結バッチ注文の概念について説明します。

生産されたバルク品目は親品目とみなされますが、梱包済み品目は子品目とみなされます。 バルク品目と梱包済み品目の関係は、バルク品変換に示されます。 このバルク品変換はバルク品目自体に定義されます。  

梱包済み品目は、単一サイズのコンテナーに梱包することも、1 つの単位と見なされる複数サイズのコンテナーに梱包することもできます。 バルク品目の注文を連結することで関連するすべてのバッチ オーダーを 1 つのビューで表示できるため、未完了の作業を特定するのに役立ちます。  

連結バッチ オーダーは次の注文の組み合わせを含めることができます。

-   1 つのバルク オーダーと複数の梱包オーダー
-   複数のバルク オーダーと複数の梱包オーダー
-   複数のバルク オーダーと 1 つの梱包オーダー
-   梱包オーダーのみ





