---
title: "サービス管理"
description: "サービス契約とサービスの定期売買を締結し、サービス注文および顧客の照会を処理し、顧客へのサービスの配送を管理および分析するには、サービス管理を使用します。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 02cdf4615e2071f2b7de2e86b6f9e6637c6e5d8d
ms.openlocfilehash: 236ab21b2d1c5a4e82270e5381d163e97437cb7f
ms.contentlocale: ja-jp
ms.lasthandoff: 05/09/2018

---


# <a name="service-management"></a>サービス管理 

[!include [banner](../includes/banner.md)]


サービス契約とサービスの定期売買を締結し、サービス注文および顧客の照会を処理し、顧客へのサービスの配送を管理および分析するには、**サービス管理**を使用します。 サービス契約を使用して、標準的なサービス訪問で使用されるリソースを定義できます。 また、サービス契約を使用して、それらのリソースに関する顧客への請求方法を表示できます。 サービス契約には、標準応答時間を指定し、実際の時間を記録するツールを提供する、サービス レベル契約も含まれています。

サービス注文を作成して、サービス技術者の顧客サイトへの予定された訪問および予定外の訪問に関する情報を管理できます。 サービス注文には次のような情報が含まれます。

1.  サービス技術者が実行する作業時間

2.  修復またはサービスのタイプ

3.  修復する品目 (現象および診断に関する詳細を含む)

4.  サービスまたは修復に関連する経費および手数料

顧客は、エンタープライズ ポータルを使用してインターネット経由でサービス要求を送信できます。 これらの要求を受信し、処理し、発信できます。 サービス注文を作成した後、サービス ステージを使用して進捗を監視し、各ステージで有効になるアクションを制御するルールを指定することができます。 サービス注文が完了すると、注文でサインオフして完了したことを確認してから、注文を転記して請求書プロセスを開始できます。

サービス注文利益幅および定期売買トランザクションを監視したり、作業の説明および作業受入を印刷したりするには、レポート ツールを使用します。

## <a name="business-processes"></a>業務プロセス

次の図は、**サービス管理**の高レベルの業務プロセスを示し、Microsoft Dynamics 365 for Finance and Operations 内の他のモジュールとサービス プロセス統合場所を表示します。

[![サービス管理の業務プロセス図](./media/sm_home_page.gif)](./media/sm_home_page.gif)

## <a name="service-management-at-a-glance"></a>サービス管理の図

<table>
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>重要なタスク</p></th>
<th><p>基本フォーム</p></th>
<th><p>一般的なレポート</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>サービス契約の履行</a></p></td>
<td><p><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">サービス契約 (フォーム)</a></p></td>
<td><p><strong>サービス注文利益幅</strong></p></td>
</tr>
<tr class="even">
<td><p>顧客の照会の処理</a></p></td>
<td><p><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">サービス注文 (フォーム)</a></p></td>
<td><p><strong>作業の説明</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">派遣表 (フォーム)</a></p></td>
<td><p><strong>トランザクション - 定期売買</strong></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p></p></td>
<td><p><strong>定期売買手数料トランザクション</strong></p></td>
</tr>
</tbody>
</table>


## <a name="integration-of-service-management"></a>サービス管理の統合

サービス管理は、Microsoft Dynamics 365 for Finance and Operations 内で以下のモジュールと統合されます。

  - [販売とマーケティング](../sales-marketing/overview-sales-marketing.md)

  - [人事管理](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


