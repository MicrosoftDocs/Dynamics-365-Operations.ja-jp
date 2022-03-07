---
title: 分割後の逓減残高による減価償却
description: このトピックでは、定率法を使用して資産を分割した後に減価償却を計算する方法 (固定資産で使用) について説明します。
author: moaamer
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8e59ff1ef2b06a7203c1023bade7f06019479f3929dfbd582860f102c46b49f0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737704"
---
# <a name="reduce-balance-depreciation-after-a-split"></a>分割後の逓減残高による減価償却

[!include [banner](../includes/banner.md)]

このトピックでは、定率法を使用して資産を他の資産に分割した後に減価償却を計算する方法 (固定資産で使用) について説明します。 資産帳簿で構成されている減価償却年度は会計年度です。 詳細については、[逓減残高による減価償却](reduce-balance-depreciation.md) および [固定資産の分割](tasks/split-fixed-asset.md) を参照してください。

資産の取得時よりも後の会計年度期間中に固定資産を分割した場合、逓減残高による減価償却は、前年度の資産正味簿価額 (NBV) を含みます。 また、資産を分割するトランザクションから生成された取得および減価償却調整トランザクションも含まれます。 この現象は、資産が 1 会計年度に取得され、将来の会計年度に分割されたことを想定しています。 分割後に元の資産に対して減価償却が必要な金額は、資産が分割される前の資産 NBV と、分割に対して転記された取得および減価償却調整トランザクションが反映されます。

たとえば、次の条件は、

- 会計年度期間は 6 月 30 日から 7 月 1 日まで有効です。
- 逓減残高の割合は 18% で、資産は USD 10,000 の取得価格で 2019 年 6 月に取得されます。
- 最初の会計年度の減価償却は USD18,000、月々の減価償却は USD150、そして資産は 2019 年 11 月まで USD738.75 の金額で償却されます。
- 2019 年 11 月 には、資産の 80% が別の固定資産に分割されます。

[![分割後の逓減残高による減価償却。](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)

元の資産に対して減価償却する金額は USD1,822.25 です。 この金額は、分割トランザクションが転記される前の (USD9,111.25) NBV、分割トランザクション (-USD8,000) の転記中に生成される取得原価調整、分割トランザクション中 (USD711) に生成される減価償却調整と等しくなります。 したがって、2 年目の減価償却は (1,822.25 × 18 パーセント) ÷ 12 = USD27.33です。

初年度の新しい固定資産に対して減価償却する金額は (8,000 × 18 パーセント) ÷ 12 = USD120 です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]