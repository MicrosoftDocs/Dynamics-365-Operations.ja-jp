---
title: 作業者のコンフィギュレーション
description: この手順では、POS の販売手数料が適用される販売員としての作業者を環境設定する方法を示します。
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
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
ms.openlocfilehash: 8bbd3899da8e289dcf82fabc0fd21370655f38e0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276050"
---
# <a name="configure-a-worker"></a>作業者のコンフィギュレーション

[!include [banner](../includes/banner.md)]

この手順では、POS の販売手数料が適用される販売員としての作業者を環境設定する方法を示します。 この手順では、デモ データの会社 USRT を使用します。


## <a name="create-a-commission-sales-group-for-the-worker"></a>作業者向け委託販売グループを作成する
1. [販売とマーケティング] > [コミッション] > [販売グループ] の順に移動します。
    * 作業者は複数の販売グループに割り当てることができます。 POSで、店舗のアドレス帳記載の作業者を含む販売グループを選択できます。  
2. [新規] をクリックします。
3. [グループ] フィールドに値を入力します。
4. [名前] フィールドに値を入力します。
5. [保存] をクリックします。
6. アクション ウィンドウで、[一般] をクリックします。
7. [販売担当者] をクリックします。
    * 販売グループには複数の作業者を含めることができます。 手数料は、その分配方法に基づき作業者間で分配することができます。  
8. [名前] フィールドで値を入力または選択します。
9. [手数料分配] フィールドに数値を入力します。
10. [保存] をクリックします。
11. ページを閉じます。
12. ページを閉じます。

## <a name="assign-the-workers-default-sales-group"></a>作業者を既定の販売グループに割り当てる
1. Retail とコマース > 従業員 > 作業者の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. 一覧で、選択された行のリンクをクリックします。
4. コマース タブをクリックします。
    * 作業者は、既定の販売グループに割り当てることができます。 既定の販売グループは、店舗の機能プロファイルでオプションが有効になっていればPOSの販売明細行に自動的に追加されます。  
5. [編集] をクリックします。
6. [既定のグループ] フィールドで、値を入力または選択します。
7. [保存] をクリックします。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
