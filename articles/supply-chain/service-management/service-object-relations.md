---
title: サービス対象の関係
description: サービス対象とサービス合意またはサービス注文の間に、サービス対象の関係を作成できます。
author: ShylaThompson
manager: tfehr
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 913b3c30bf972de7cc3dde73280e4f2f2be38507
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974338"
---
# <a name="service-object-relations"></a>サービス対象の関係 

[!include [banner](../includes/banner.md)]

サービス対象とサービス合意またはサービス注文の間に、サービス対象の関係を作成できます。 関係を作成すると、サービス対象がサービス合意またはサービス注文に関連付けられます。

リレーションが作成された後、サービス合意またはサービス注文の任意の明細行にサービス対象を関連付けることができます。

## <a name="template-boms"></a>テンプレート BOM

サービス対象の関係にはテンプレート BOM を指定することもできます。 テンプレート BOM は、サービスの実行対象に対する部品表です。 サービス訪問時にサービス対象の部品を交換する場合は、[サービス対象] フォームを使用して、この変更をサービス BOM に登録できます。

## <a name="example"></a>例

顧客サイトで 2 台のエレベーターを点検するサービス合意を作成します。
このサービス合意の ID は SAL-001 です。

このエレベーターは、[サービス対象] フォームで EL-S/1000 および EL-L/1000 という対象として設定されています。

このサービス対象 (EL-S/1000 および EL-L/1000) をサービス合意に関連付けます。

サービス対象の部品を交換した場合に、その対象の BOM に変更を登録する必要があります。そこで、次の表のように、サービス BOM をサービス対象の関係に関連付けます。

| サービス対象 | リレーション - サービス契約 | サービス BOM   |
|----------------|------------------------------|---------------|
| EL-S/1000      | ID SAL-001                   | BOM-EL-S/1000 |
| EL-L/1000      | ID SAL-001                   | BOM-EL-L/1000 |

この合意にはサービス対象の関係が存在するため、上記の対象に対して次の表のようにサービス合意項目を作成できます。

| トランザクション タイプ | カテゴリ           | サービス対象 |
|------------------|--------------------|----------------|
| 時間             | 検査         | EL-S/1000      |
| 時間             | ギアボックスのクリーニング  | EL-S/1000      |
| 品目             | クリーニング用具 | EL-S/1000      |
| 時間             | 検査         | EL-L/1000      |
| 時間             | ギアボックスのクリーニング   | EL-L/1000      |
| 品目             | クリーニング用具 | EL-L/1000      |

サービス訪問時にエレベーター EL-S/1000 のギアボックスを交換する必要が生じました。 この対象の部品を交換するには、現在のサービス合意に対して設定したサービス対象の関係を使用して、BOM デザイナにアクセスします。

サービス対象の関係を使用した BOM デザイナへのアクセス

1. サービス契約
2. サービス契約をダブルクリックするか、[サービス契約] をクリックしてサービス契約を作成します。
3. [設定] タブをクリックします。
4. テンプレート BOM をサービス合意に関連付けるには、[サービス対象] をクリックします。
5. [サービス対象] フォームでは、テンプレート BOM を変更する [デザイナー] フォームを開いて [デザイナー] をクリックします。

## <a name="automatically-created-service-orders"></a>自動的に作成されるサービス注文

サービス合意に対してサービス注文を自動的に作成すると、合意におけるサービス対象の関係が、サービス注文にも作成されます。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]