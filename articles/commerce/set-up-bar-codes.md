---
title: バーコードの設定
description: この記事は、Dynamics 365 Commerce でのバーコードの使用方法について説明します。
author: josaw1
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.industry: Retail
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
ms.openlocfilehash: 5771ada4a9bba92fb32155ae425f08d6429b46e6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271799"
---
# <a name="set-up-bar-codes"></a>バーコードの設定

[!include [banner](includes/banner.md)]

この記事は、Dynamics 365 Commerce でのバーコードの使用方法について説明します。

バーコードを使用して、製品の購買および販売、製品バリアントの追跡、および顧客と従業員の設定を行うことができます。 また、バーコードを使用して、クーポン、ギフト カード、およびクレジット メモを発行して裏書きすることもできます。 標準バーコード、カスタム バーコード、社内バーコードを使用するように、製品を設定できます。 製品では、複数のバーコードを使用できます。 たとえば、製品をさまざまな製造業者から仕入れる場合、あるいは製品にサイズ、スタイル、または色に基づいたバリアントがある場合、製品で複数のバーコードを使用できます。 バーコードには、製品の重量や価格を含めることができます。 バーコード マスクは、バーコードの作成に使用されるテンプレートです。

> [!NOTE]
> バリアントの組み合わせごとに固有のバーコードを割り当てる場合、レジスターで品目のバーコードをスキャンしたときに、製品のどのバリアントが販売されたかを判断できます。 また、バリアント別に販売に関する統計を収集および表示することもできます。 サイズ、色、およびスタイルの各グループに固有の番号を割り当てて、バーコードで識別できます。 コマースはバーコード マスクを使用して、バリアントの組み合わせごとに自動的にバーコードを生成します。 多くのサイズ、色、およびスタイルがある場合は、バリアント コードが追加されるたびに組み合わせが飛躍的に増加するため、この方法を使用すると便利です。 この機能を使用しない場合、製品バリアントを表す組み合わせごとに手動でバーコードを割り当てる必要があります。

バーコードは手動または自動で作成できます。 バーコードを作成するには、表示されている順序で次のタスクを行います。

1. [バーコード マスク文字の設定](set-up-bar-code-masks.md)。
2. [バーコード マスクの設定](set-up-bar-code-masks.md)。
3. バーコードの設定をコンフィギュレーションします。
4. [製品のバーコードを作成します](../supply-chain/pim/tasks/create-bar-code-product.md)。

## <a name="additional-resources"></a>その他のリソース

[バーコード マスクの設定](set-up-bar-code-masks.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
