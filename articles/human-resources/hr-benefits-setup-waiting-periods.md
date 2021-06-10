---
title: 待機期間のコンフィギュレーション
description: Microsoft Dynamics 365 Human Resources では、待機日は、給付金プランに使用するマイルストーンを確立します。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4973a2a3b2fcedcf2301c80b362cfb22c912bc49
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058491"
---
# <a name="configure-waiting-periods"></a>待機期間のコンフィギュレーション

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources では、待機日は、給付金プランに使用するマイルストーンを確立します。 たとえば、雇用日から 3 か月、各月の最初、または 6 か月です。   

1. **給付金管理** ワーク スペースの **設定** で、**待機期間** を選択します。

2. **新規** を選択します。

3. 次のフィールドの値を指定します。

   | フィールド | 説明 |
   | --- | --- |
   | **待機コード** | 待機期間の一意の識別子。 |
   | **説明** | 待機期間の説明。 |
   | **待機方法** | 値のドロップダウン リストから適切な待機メソッドを選択します。 オプションには、正味、当月、現在の四半期、今年度、および現在の週があります。 |
   | **月数** | 待機日を計算するために待機メソッドに追加する月数を入力します。 |
   | **日** | 待機日を計算するために待機メソッドに追加する日数を入力します。 |
   | **待機日数** | 待機日の計算に使用する待機日を選択します。 |

4. **保存** を選択します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]