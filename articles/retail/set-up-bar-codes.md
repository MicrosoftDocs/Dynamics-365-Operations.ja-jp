---
title: "バーコードの設定"
description: "この記事では、Microsoft Dynamics 365 for Retail でのバーコードの使用方法について説明します。"
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fdc56bf468babd4b0b0652d9791114af676c8470
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-bar-codes"></a>バーコードの設定

[!include[banner](includes/banner.md)]


この記事では、Microsoft Dynamics 365 for Retail でのバーコードの使用方法について説明します。

バーコードを使用して、製品の購買および販売、製品バリアントの追跡、および顧客と従業員の設定を行うことができます。 また、バーコードを使用して、クーポン、ギフト カード、およびクレジット メモを発行して裏書きすることもできます。 標準バーコード、カスタム バーコード、社内バーコードを使用するように、小売製品を設定できます。 製品では、複数のバーコードを使用できます。 たとえば、製品をさまざまな製造業者から仕入れる場合、あるいは製品にサイズ、スタイル、または色に基づいたバリアントがある場合、製品で複数のバーコードを使用できます。 バーコードには、製品の重量や価格を含めることができます。 バーコード マスクは、バーコードの作成に使用されるテンプレートです。 **注記:** バリアントの組み合わせごとに固有のバーコードを割り当てる場合、レジスターで品目のバーコードをスキャンしたときに、製品のどのバリアントが販売されたかを判断できます。 また、バリアント別に販売に関する統計を収集および表示することもできます。 サイズ、色、およびスタイルの各グループに固有の番号を割り当てて、バーコードで識別できます。 Dynamics 365 for Retail はバーコード マスクを使用して、バリアントの組み合わせごとに自動的にバーコードを生成します。 多くのサイズ、色、およびスタイルがある場合は、バリアント コードが追加されるたびに組み合わせが飛躍的に増加するため、この方法を使用すると便利です。 この機能を使用しない場合、製品バリアントを表す組み合わせごとに手動でバーコードを割り当てる必要があります。 バーコードは手動または自動で作成できます。 バーコードを作成するには、表示されている順序で次のタスクを行います。

1.  [バーコード マスク文字の設定](set-up-bar-code-masks.md)。
2.  [バーコード マスクの設定](set-up-bar-code-masks.md)。
3.  バーコードの設定をコンフィギュレーションします。
4.  製品のバーコードを作成します。


<a name="see-also"></a>参照
--------

[バーコード マスクの設定](set-up-bar-code-masks.md)




