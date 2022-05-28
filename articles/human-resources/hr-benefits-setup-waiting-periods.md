---
title: 待機期間のコンフィギュレーション
description: Microsoft Dynamics 365 Human Resources では、待機日は、給付金プランに使用するマイルストーンを確立します。
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 770fed04f951ff45b5c0c423c96bee855d87adf7
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8696071"
---
# <a name="configure-waiting-periods"></a>待機期間のコンフィギュレーション


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources では、待機日は、給付金プランに使用するマイルストーンを確立します。 たとえば、雇用日から 3 か月、各月の最初、または 6 か月です。   

1. **給付金管理** ワーク スペースの **設定** で、**待機期間** を選択します。

2. **新規** を選択します。

3. 次のフィールドの値を指定します。

   | フィールド | 説明 |
   | --- | --- |
   | **待機コード** | 待機期間の一意の識別子。 |
   | **説明** | 待機期間の説明。 |
   | **待機方法** | 値のドロップダウン リストから適切な待機メソッドを選択します。 オプションには、**作成日**、**今月**、**現在の四半期**、**今年**、および **現在の週** があります。 |
   | **月数** | 待機日を計算するために待機メソッドに追加する月数を入力します。 |
   | **日** | 待機日を計算するために待機メソッドに追加する日数を入力します。 |
   | **待機日数** | 待機日の計算に使用する待機日を選択します。 |

4. **保存** を選択します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
