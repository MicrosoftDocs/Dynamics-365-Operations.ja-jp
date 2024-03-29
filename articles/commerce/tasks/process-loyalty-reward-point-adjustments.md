---
title: ロイヤルティ報酬ポイント調整の処理
description: この手順では、ロイヤルティ カード情報を検索し、ロイヤルティ報酬ポイントを調整する方法を示します。
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: RetailLoyaltyCards, RetailLoyaltyCardRewardPointTrans, RetailLoyaltyCardRewardPointAdjustment, RetailAffiliationLookup
ms.openlocfilehash: 814b1a357ef19aed0782bf57096731b86d5e4448
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285662"
---
# <a name="process-loyalty-reward-point-adjustments"></a>ロイヤルティ報酬ポイント調整の処理

[!include [banner](../includes/banner.md)]

この手順では、ロイヤルティ カード情報を検索し、ロイヤルティ報酬ポイントを調整する方法を示します。 このタスクの作成に使用するデモ データの会社は USRT です。 このタスクはコマース工程マネージャー ロールまたは顧客サービス マネージャ ロールを対象としています。

1. [ロイヤルティ カード] に移動
2. 一覧で、目的のレコードを見つけ、選択します。
3. 一覧で、選択された行のリンクをクリックします。
4. [カード トランザクション] をクリックします。
    * このページでは、選択したロイヤルティ カードのすべてのロイヤルティ トランザクションを確認できます。  
5. ページを閉じます。
6. [カードの調整] をクリックします。
7. [新規] をクリックします。
8. [報酬ポイント] フィールドで、値を入力または選択します。
9. [金額または数量] フィールドに数値を入力します。
    * 正の金額または負の金額を使用して、ロイヤルティ カードにポイントを追加、または削除できます。  
10. [ロイヤルティ プログラム] フィールドで、値を入力または選択します。
11. [コメント] フィールドで、値を入力します。
12. [調整の転記] をクリックします。
13. [はい] をクリックします。
14. ページを閉じます。
    * 通常、 [報酬のポイントの集計] タブの報酬ポイント調整の結果を表示するには、この時点でページを更新します。しかし、タスク ガイドとしてこれを実行している場合、更新するとタスク ガイドが終了してしまうので、今すぐ更新しないでください。  
15. [カード トランザクション] をクリックします。
16. ページを閉じます。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
