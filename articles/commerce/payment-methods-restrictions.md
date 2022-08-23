---
title: レシートのない返品の支払方法の制限
description: この記事では、返品がレシートなしで行われた場合に、特定の支払タイプがどのように返金を制限するかについて説明します。
author: josaw1
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.industry: Retail
ms.search.form: RetailTenderTypeTable
ms.openlocfilehash: 9b14d7d8f6a2d9209ad6a12cd53bce4a9b50178d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281399"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>レシートのない返品の支払方法の制限


[!include [banner](includes/banner.md)]

小売業者が受け入れる各支払タイプは、システムの設定時にコンフィギュレーションする必要があります。 この記事では、返品がレシートなしで行われた場合に、特定の支払タイプがどのように返金を制限するかについて説明します。

## <a name="set-up-payment-methods"></a>支払方法の設定

支払方法を設定するには、次の作業を行う必要があります。
1. 組織全体で受け入れる支払方法を作成します。
2. 組織全体のカード タイプとカード番号の作成。 クレジット カードまたはデビット カードを受け入れる場合、カードの支払方法を 1 つ作成し、組織全体のカード タイプとカード番号を作成する必要があります。
3. 店舗の支払方法を設定します。 支払方法を各店舗に関連付けて、各支払方法の店舗固有の設定を入力します。
4. 店舗のカード支払方法の設定。 店舗で受け入れるカード支払方法について、カードの設定を行います。

![店舗の設定。](media/NoReceiptReturns1.png "小売店舗の設定") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>レシートのない返品の支払方法の制限

各店舗の支払方法について、**店舗管理** ページの **レシートなしの返品** で、**レシートなしの払戻の制限** を **はい** に設定します。 

切替の既定値が **いいえ** である場合は、その支払方法は払戻が許可されていることを保証します。 

**レシートなしの払戻の制限** が **はい** に設定されている場合、選択された支払方法は払戻に使用できません。 

![店舗支払方法。](media/NoReceiptReturns3.png "小売店舗の支払方法") 

> [!NOTE]
> レジ担当者が、レシートなしでの払戻が制限されている支払方法を選択すると、許容されている支払方法を確認するメッセージが表示されます。

![許容可能な支払方法。](media/NoReceiptReturns4.png "許容可能な支払方法") 

トランザクションにレシートありの返品とレシートなしの返品の両方がある場合、トランザクションはレシートありの返品ワークフローになるため、制限条件は適用されません。 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
