---
title: サービス テンプレート
description: サービス合意をテンプレートとして定義し、後でテンプレート行を別のサービス合意やサービス注文にコピーできます。
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ade35eee21585aed2f542f4c977788aa3fe8804b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256138"
---
# <a name="service-templates"></a>サービス テンプレート

[!include [banner](../includes/banner.md)]

サービス合意をテンプレートとして定義し、後でテンプレート行を別のサービス合意やサービス注文にコピーできます。

## <a name="example"></a>例

サービスの提供先の顧客は、5 つの異なる場所で同一の業務用エレベータを使用しています。

この顧客向けの 5 つのサービス合意を、各サイトに 1 つずつ設定するとします。
設定作業の繰り返しを省き、サービス合意の設定情報が同一になるようにするために、サービス合意を 1 つ作成して、各エレベータのサービス作業のテンプレートとして指定します。

これにより、テンプレート行を 5 つの新しいサービス合意にコピーし、その行を使用してサービス合意を設定できるようになります。

## <a name="create-a-template"></a>テンプレートの作成

サービス テンプレートを作成する際には、サービス合意を作成してから、必要な行をサービス合意に作成して、サービス合意をサービス テンプレート グループに関連付けます。

> [!NOTE]
> サービス合意は、サービス注文が関連付けられていない場合にのみ、テンプレートとして定義できます。 また、テンプレートとして定義したサービス合意からサービス注文を生成することはできません。

## <a name="copy-template-lines"></a>テンプレートの行のコピー

サービス テンプレート行は、別のサービス合意またはサービス注文にコピーすることができます。

テンプレート行をサービス注文またはサービス合意にコピーすると、各テンプレート グループを展開可能なツリー ビューにテンプレート グループが表示されます。 これにより、各テンプレートとテンプレート行を確認することができます。

テンプレートの用途を表す名前でテンプレートをグループ化すると、コピーするサービス テンプレート行を簡単に特定できるようになります。

## <a name="related-topics"></a>関連トピック

[サービス テンプレート行のコピー](copy-service-template-lines.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]