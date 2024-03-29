---
title: コール センターの連続プログラムの設定
description: この記事では、コール センターの連続プログラムの設定方法について説明します。
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 39c3e6d740bff2af27a2fba2ac4c406c01b43a87218fdc1dcfe094c147cd3de3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716153"
---
# <a name="set-up-continuity-programs-for-call-centers"></a>コール センターの連続プログラムの設定

[!include [banner](includes/banner.md)]

この記事では、コール センターの連続プログラムの設定方法について説明します。

繰返し注文プログラムとも呼ばれる連続プログラムでは、事前定義スケジュールに応じて、顧客は通常の製品出荷を受け取ります。 月例図書推薦会の場合のように、各出荷に異なる製品を含めたり、同じ製品を繰り返し送信することもできます。 連続プログラムを設定するには、次の作業を行う必要があります。

1. **コール センター パラメーター** ページで連続パラメーターを設定します。
2. 支払スケジュール、出荷のタイミング、先行請求であるか、などの詳細を指定する連続プログラムを作成します。 また、連続プログラムに含まれる製品の一覧を追加する必要があります。 各製品は 1 で始まる、連続して割り当てられるイベント ID 番号を受け取ります。 イベント ID により、製品が送信される順序が決まります。

    - 顧客が各出荷で別の製品を受け取る場合、製品はイベント ID に応じて、現在のイベントから順番に送信されます。
    - 顧客が各出荷で同じ製品を受け取る場合、一覧には 1 つのイベント ID を持つ 1 つのイベントのみが含まれます。 同じイベントが繰り返し発生します。 各イベントが繰り返される回数を指定できます。

3. 手順 2 で作成した連続プログラムを表す親製品を作成します。 販売注文にこの製品を追加すると、**連続性** ページが開きます。 その後、このページを使用して実際の連続注文を作成できます。 親製品は、顧客が各出荷で受け取る個々の製品を指定しません。

上記で説明されている連続プログラムを設定すると、顧客の連続注文を作成できます。 次の追加のメンテナンス作業を行う必要があります。

- **現在の連続イベント期間の更新** – 現在のイベント期間をシステムに知らせるバッチ ジョブを設定します。
- **連続の子注文の作成** – 親の連続注文から子注文を作成します。
- **連続支払の処理** – 連続販売注文に関連付けられた支払の請求と通知を処理します。
- **連続行数の拡張** (必要な場合) – 連続イベントを繰り返す回数を拡張します。 これにより出荷の繰り返しは、コール センター パラメーターの **連続繰り返しのしきい値** フィールドで設定されている制限を超えて拡張することができます。
- **連続更新の実行** (必要な場合) – 連続プログラムと親連続販売注文の間の差を同期します。
- **連続の親明細行と注文を閉じる** – 連続注文を閉じます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]