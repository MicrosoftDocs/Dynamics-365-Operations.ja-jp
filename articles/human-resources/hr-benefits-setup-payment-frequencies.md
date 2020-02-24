---
title: 支払頻度の設定
description: ''
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
ms.openlocfilehash: e5fe0a16c4abbb9241fcdac88fd56e92bf04788c
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009733"
---
# <a name="set-up-payment-frequencies"></a>支払頻度の設定

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resources は、支払頻度を使用して年間給付金給与を計算し、従業員が各支払期間に支払う給付金割増金額を決定し、支払いがプロバイダーに行われる頻度を定義します。

給付金支払頻度は、換算率を使用して毎月、半月毎、隔週毎、毎週、および毎日の支払頻度を給付金支払期間に変換します。 これにより、会社は給付金プラン内の支払頻度の間で相互依存関係を定義できます。

換算率フィールドでは、支払頻度から標準支払期間への換算率を識別し、システムが支払頻度間の計算を行えるようにします。 換算率の金額は、従業員が各支払頻度に支払う必要がある給付金割増金額を決定するためにも使用されます。

1. **給付金管理**ワーク スペースの**設定**で、**支払頻度**を選択します。

2. **新規** を選択します。

3. 次のフィールドの値を指定します。

   | フィールド | 説明 |
   | --- | --- |
   | 支払頻度 | 支払頻度の一意名。 |
   | 説明 | 支払頻度の説明。 |
   | 期間 | 給付金プロバイダーおよび従業員の支払頻度に最も一致する適切な期間。 期間リストは、標準支払期間で作成されます。 |
   | 支払い期間数 | 支払期間数は給付金プロバイダーまたは従業員に支払われる頻度を表します。 この金額は、従業員の年間給付金給与金額を計算するために使用されます。 |
   | 年次の変換係数 | 支払頻度の年間変換率。 たとえば、月次支払頻度の年間の変換率は次のようになります: </br></br>(12 か月の支払 / 1 年) = 12 |
   | 半年ごとの変換係数 | 半年毎の支払頻度の変換率。 たとえば、月次支払頻度の半年毎の変換率は次のようになります: </br></br>(12 か月の支払 / 年 2 回) = 6 |
   | 四半期ごとの変換係数 | 四半期の支払頻度の変換率。 たとえば、月次支払頻度の四半期ごとの変換率は次のようになります: </br></br>(12 か月の支払 / 四半期の 4 期分) = 3 |
   | 月次の変換係数 | 支払頻度の毎月の変換率。 たとえば、月次支払頻度の毎月の変換率は次のようになります: </br></br>(12 か月の支払 / 12 か月) = 1 |
   | 半月ごとの変換係数 | 半月毎の支払頻度の変換率。 たとえば、月次支払頻度の半月毎の変換率は次のようになります: </br></br>(12 か月の支払 / 24 (月 2 回)) = .5 | 
   | 隔週の変換係数 | 支払頻度の年間変換率。 たとえば、月次支払頻度の年間の変換率は次のようになります: </br></br>(12 か月の支払 / 26 週間) = 0.461538 |
   | 週次の変換係数 | 支払頻度の年間変換率。 たとえば、月次支払頻度の年間の変換率は次のようになります: </br></br>(12 か月の支払 / 52 週間) = 0.230769 |
   | 日次の変換係数 | 支払頻度の年間変換率。 たとえば、月次支払頻度の年間の変換率は次のようになります: </br></br>(12 か月の支払 / 365 日) = 0.032877 |

4. **保存** を選択します。 