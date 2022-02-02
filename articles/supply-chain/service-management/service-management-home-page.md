---
title: サービス管理の概要
description: サービス契約とサービスの定期売買を締結し、サービス注文および顧客の照会を処理し、顧客へのサービスの配送を管理および分析するには、サービス管理を使用します。
author: kamaybac
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b9b8444c635fe08a224314d1b76de5ac8d9defbc
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983025"
---
# <a name="service-management-overview"></a>サービス管理の概要

[!include [banner](../includes/banner.md)]


サービス契約とサービスの定期売買を締結し、サービス注文および顧客の照会を処理し、顧客へのサービスの配送を管理および分析するには、**サービス管理** を使用します。 サービス契約を使用して、標準的なサービス訪問で使用されるリソースを定義できます。 また、サービス契約を使用して、それらのリソースに関する顧客への請求方法を表示できます。 サービス契約には、標準応答時間を指定し、実際の時間を記録するツールを提供する、サービス レベル契約も含まれています。

サービス注文を作成して、サービス技術者の顧客サイトへの予定された訪問および予定外の訪問に関する情報を管理できます。 サービス注文には次のような情報が含まれます。

1.  サービス技術者が実行する作業時間

2.  修復またはサービスのタイプ

3.  修復する品目 (現象および診断に関する詳細を含む)

4.  サービスまたは修復に関連する経費および手数料

サービス要求を受信し、処理し、発信できます。 サービス注文を作成した後、サービス ステージを使用して進捗を監視し、各ステージで有効になるアクションを制御するルールを指定することができます。 サービス注文が完了すると、注文でサインオフして完了したことを確認してから、注文を転記して請求書プロセスを開始できます。

サービス注文利益幅および定期売買トランザクションを監視したり、作業の説明および作業受入を印刷したりするには、レポート ツールを使用します。

## <a name="business-processes"></a>業務プロセス

次の図は、**サービス管理** の上位レベルの業務プロセスを示し、サービス プロセスが他のモジュールと統合する場所を示します。

[![サービス管理の業務プロセス図。](./media/sm_home_page.gif)](./media/sm_home_page.gif)

## <a name="service-management-at-a-glance"></a>サービス管理の図

|重要なタスク           | 基本ページ                         |一般的なレポート              |
|--------------------------|---------------------------------------|-----------------------------|
|サービス契約の履行|サービス契約                     |サービス注文利益幅         |
|顧客の照会の処理 |サービス注文                         |作業の説明             |
|                          |派遣表                         |トランザクション - 定期売買   |
|                          |                                       |定期売買手数料トランザクション|


## <a name="integration-of-service-management"></a>サービス管理の統合

サービス管理は次のモジュールと統合できます。

  - [販売とマーケティングの概要](../sales-marketing/overview-sales-marketing.md)
  - [人事管理](/dynamics365/unified-operations/talent/index)

  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]