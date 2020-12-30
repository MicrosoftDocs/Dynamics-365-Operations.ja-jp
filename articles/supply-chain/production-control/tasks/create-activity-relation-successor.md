---
title: 活動リレーションの作成 - 後続処理
description: リーン生産フローの活動フローは活動関係を通して文書化されています。
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91e1535ab6b53ad60394967d0377606a0cd27d01
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431688"
---
# <a name="create-activity-relation---successor"></a>活動リレーションの作成 - 後続処理

[!include [banner](../../includes/banner.md)]

リーン生産フローの活動フローは活動関係を通して文書化されています。 このレコードは、活動関係を作成する方法を示します。

前提条件:

- ドラフト モードの生産フローとバージョン。 

- 生産フローで交互に実行される 2 つの活動が作成されましたが、関連付けられていません。


## <a name="find-the-production-flow-version"></a>生産フロー バージョンの検索 
1. [生産管理] > [設定] > [リーン生産フロー] > [生産フロー] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. 一覧で、選択された行のリンクをクリックします。
4. 一覧で、選択された行をマークします。
5. 一覧で、ドラフト バージョンを選択します。
    * 活動関係は、生産フローのドラフトか、有効なバージョンの両方に追加できます。  

## <a name="open-the-activity-overview"></a>活動の概要を開く
1. [活動] をクリックします。
    * このフォームは、作業している生産フローのバージョンに割り当てられている生産フローのすべての活動を示すことに注意してください。  

## <a name="add-a-successor"></a>後続処理の追加
1. [後続処理の追加] をクリックします。
2. [活動] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. 一覧で、目的のレコードを見つけ、選択します。
4. 一覧で、選択された行のリンクをクリックします。
5. [制約] チェック ボックスをオンにします。
6. [制約値] フィールドで、値を入力します。
    * 制約時間とは、先行処理の終了予定時刻 (期日の日時) と後続処理の開始予定時刻の間にスケジュールされる時間です。  
7. [単位] フィールドで、値を入力します。
8. [サイクル時間の比率] フィールドで、数値を入力します。
    * 両方の活動が同じタクトで実行される場合、サイクル時間率は 1 にしてください。 先行処理が後続処理の 2 倍のスピードで実行される場合、サイクル時間率は 2 にしてください。   サイクル時間率は生産フロー活動の個々のサイクル時間の計算に使用されます。  
9. [OK] をクリックします。
10. ページを閉じます。
11. [グリッド パネル] タブをクリックします。
12. ページを閉じます。
13. ページを更新します。

