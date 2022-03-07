---
title: 価格と割引の拡張性
description: このトピックでは、価格設定機能を展開する方法を説明します。
author: smithanataraj
ms.date: 12/21/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2017-12-10
ms.dyn365.ops.version: Platform update 11
ms.openlocfilehash: d951168c4b369592157e9a1308c38f372b10adff
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783018"
---
# <a name="price-and-discount-extensibility"></a>価格と割引の拡張性

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3 以降では、価格設定の領域が拡張します。 価格と割引のいくつかの一般的なカスタマイズは次のとおりです。
- 新しい価格タイプの検索メカニズムに加えて、新しい価格グループ タイプと対応する価格タイプ (**PriceType** と **PriceGroupType** の列挙値) を追加します。
- 追加のパラメーターを **PriceDisc** クラスに渡すことを含め、価格と割引の検索を変更します。 

## <a name="pricetype-and-pricegrouptype-enums"></a>PriceType および PriceGroupType 列挙
通常、新しいタイプの価格割引検索を追加すると、**PriceType** と **PriceGroupType** の 2 つの列挙型へ新しい列挙型値が追加されて開始します。 拡張機能をサポートするために、**PriceType** と **PriceGroupType** の列挙型の値は、クラス階層 **PriceGroupTypeTradeAgreementMapping** と **PriceTypeTradeAgreementMapping** にそれぞれカプセル化されました。 これらは、新しい **PriceType** および **PriceGroupType** 拡張列挙値に対して拡張できます。

**Customer**、**Vendor**、および **InventTable** テーブルの価格タイプに対応するフィールドのマッピングは、**PriceTypeTradeAgreementMapping** で定義されています。 

次の図は、実装を強調表示しています。 メソッドはサブクラスを 1 つだけ示すことに注意してください。 実装は、各サブクラスにする必要があります。 

![PriceGroupTypeTradeAgreementMapping.](media/PricingFall20171.png)

## <a name="pricedisc-class"></a>PriceDisc クラス

**PriceDisc** クラスは、価格と割引の検索エンジンです。 このクラスは、**PriceDiscParameters** オブジェクトを、価格および割引検索で使用されるパラメーターを渡すメンバとして使用します。 これにより、特定のソリューションの追加の検索パラメーターを渡すことができます。 特定の **PriceGroupType** 検索のパラメータのみ、**PriceDisc** クラスの対応する find メソッドを使用して渡されます。 

**PriceDiscParameters** クラスのインスタンス化をラップし、変更する機能は、AppSuite 全体で実行されたすべての価格と割引の検索呼び出しで有効になっています。

次の図では、どのように **PriceDisc** クラスを拡張して、既存の検索を変更したり、拡張された **PriceType** 列挙値に対応する新しい検索メソッドを追加したりできるかを確認できます。

![PriceDiscClass.](media/PricingFall20172.png)

## <a name="add-a-new-price-search"></a>新しい価格検索の追加

このシナリオでは、**PriceGroupType** 列挙を新しい値 **PriceGroupTypeISVExtension**、および 2 つの対応する **PriceType** 列挙値である **ISVPurchPriceType** と **ISVSalesPriceType** で拡張しました。 

![WalkThrough1.](media/PricingFall20173.png)

次の図は、**PriceType** 値および **PriceGroupType** 値に対して新しい価格検索を追加する方法を示しています

![WalkThrough2.](media/PricingFall20174.png)

以下に例を示します。

- 新しく作成された **PriceGroupType** 値については、属性 **ISVPriceGroupType** で修飾された **PriceGroupTypeTradeAgreementMappingISVPriceGroupType** クラスは、価格グループ タイプの動作を定義します。
- 新しく作成された **PriceType** 値については、**PriceTypeTradeAgreementMappingISVPurchPriceType** および **PriceTypeTradeAgreementMappingISVSalesPriceType** クラスは、購買および販売に対応します。
- **PriceDiscParameters** クラスを拡張して価格割引検索の汎用パラメータを追加します。
- **PriceDisc** クラスを拡張して新しい価格タイプの新しい価格割引検索メソッドを作成します。
- **PriceDiscParameters** には、価格と割引の検索に関連するすべてのクラスからアクセスでき、これらは要件に基づいて拡張できます。 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]