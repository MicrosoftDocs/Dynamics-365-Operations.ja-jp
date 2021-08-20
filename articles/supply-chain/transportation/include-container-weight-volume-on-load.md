---
title: 積荷のコンテナーの重量と容積を含める
description: このトピックでは、積荷のコンテナーの重量と容積を含めるための機能を設定および適用する方法について説明します。
author: Henrikan
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52b42bd0b97564a493a50331d1424ca8084b389b29518f012f443d9cf722efe7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763918"
---
# <a name="include-container-weight-and-volume-on-load"></a>積荷のコンテナーの重量と容積を含める

[!include [banner](../includes/banner.md)]

積荷のコンテナーの重量と容積を含める機能は、積載するコンテナーと品目の合計重量および容積を明確に表示します。

積荷には単一または複数の出荷が含まれており、これらの出荷には単一つの販売注文または複数の販売注文に属する特徴的品目が含まれます。 品目は、コンテナーに内部格納され、コンテナーは積荷に積載されます。 コンテナーの外部にある品目も、積荷の一部となります。 これらの条件に基づき、システムはコンテナーと品目両方の重量および容積を考慮して、積荷の重量および容積を計算します。

計算された値が詳細でない場合は、積荷の重量および容積の実際の値を入力することで調整できます。 重量および容積の値は、輸送管理プロセスで使用されます。 たとえば、値は工順ワークベンチの評価に使用されます。それは積荷のレートとルートを定義するのに役立ち、輸送業者および配送担当者のチェックインにも使用されます。

## <a name="where-it-applies"></a>該当する場所

積荷のコンテナーの重量と容積を含める機能は、工順ワークベンチの評価、輸送業者、および配送担当者のチェックインなどの、輸送管理プロセスに適用されます。

## <a name="how-it-is-set-up"></a>設定方法

考慮する必要がある積荷のコンテナーの数は、コンテナーの重量および容積、さらに使用されるコンテナーの割合に基づいて計算されます。

-   コンテナーの重量と容積を設定するには、**倉庫管理** \> **設定** \> **コンテナー** \> **コンテナー タイプ** の順にクリックします。

-   コンテナー使用率の割合を設定するには、**倉庫管理** \> **設定** \> **コンテナー** \> **コンテナー グループ** の順にクリックし、**コンテナー使用率の割合** フィールドに値を入力します。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]