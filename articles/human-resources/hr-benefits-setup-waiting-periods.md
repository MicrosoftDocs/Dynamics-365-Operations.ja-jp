---
title: 待機期間のコンフィギュレーション
description: Microsoft Dynamics 365 Human Resources では、待機日は、給付金プランに使用するマイルストーンを確立します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 58d96469fc953c1bbabe8e29bf9df7a8fb4a0589
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092516"
---
# <a name="configure-waiting-periods"></a>待機期間のコンフィギュレーション

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resources では、待機日は、給付金プランに使用するマイルストーンを確立します。 たとえば、雇用日から 3 か月、各月の最初、または 6 か月です。   

1. **給付金管理**ワーク スペースの**設定**で、**待機期間**を選択します。

2. **新規** を選択します。

3. 次のフィールドの値を指定します。

   | フィールド | 説明 |
   | --- | --- |
   | 待機コード | 待機期間の一意の識別子。 |
   | 説明 | 待機期間の説明。 |
   | 待機方法 | 値のドロップ ダウン リストから適切な待機メソッドを選択します。 オプションには、正味、当月、現在の四半期、今年度、および現在の週があります。 |
   | 月数 | 待機日を計算するために待機メソッドに追加する月数を入力します。 |
   | Days | 待機日を計算するために待機メソッドに追加する日数を入力します。 |
   | 待機日数 | 待機日の計算に使用する待機日を選択します。 |

4. **保存** を選択します。
