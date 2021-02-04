---
title: 負債、資産、および経費トランザクションの表示
description: このトピックでは、リース資産のトランザクションを表示する方法について説明します。 これらのトランザクションには、リース負債トランザクションと、転記された履行費用トランザクションが含まれます。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7008891d194dc990d13a9f56db155c6990aae0c0
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445400"
---
# <a name="view-liability-asset-and-expense-transactions"></a>負債、資産、および経費トランザクションの表示

[!include [banner](../includes/banner.md)]

このトピックでは、リース資産のトランザクションを表示する方法について説明します。 これらのトランザクションには、リース負債トランザクションと、転記された履行費用トランザクションが含まれます。 負債および使用権資産のキャリー額は、いくつかのレポートで使用されます。 また、調整値を計算するためにも使用されます。

## <a name="liability-transactions"></a>負債トランザクション

リース負債トランザクションを表示するには、**リースの概要** ページでリースを選択し、**帳簿** を選択して、リース レコードに関連付けられているブックを開きます。 最初の認識、請求書、または利子仕訳帳が転記された後、**負債トランザクション** を選択します。

**負債トランザクション** ページには、リース負債を増減させるトランザクションが表示されます。 このページの負の金額は、標準アプリケーションの貸方トランザクションを表します。 未収利息は負の値として表示され、リース負債の合計額が増加します。 リース調整は、リース帳簿の性質と影響に応じて、正または負の値として表示されます。 選択したリースのリース負債の現在の正味残高がページの左下に表示されます。

## <a name="asset-transactions"></a>資産トランザクション

リース資産トランザクションを表示するには、**リースの概要** ページでリースを選択し、**帳簿** を選択して、リース レコードに関連付けられているリース帳簿を開きます。 **資産トランザクション** を選択します。

**資産トランザクション** ページには、リース資産と累計減価償却勘定の増加または減少のトランザクションが表示されます。 借方は正の値として表示され、**負債トランザクション** ページのように貸方が負の値として表示されます。 転記された初期認識と、減価償却累計額の次の金額が、ページの左下に資産残高として表示されます。 

## <a name="expenses-transactions"></a>経費トランザクション

リース経費トランザクションを表示するには、**リースの概要** ページでリースを選択し、**帳簿** を選択して、リース レコードに関連付けられているリース帳簿を開きます。 次に、**経費トランザクション** を選択します。

**経費トランザクション** ページには、リースに対して転記されたすべての経費 (支払利息、減価償却費、履行費用など) が表示されます。