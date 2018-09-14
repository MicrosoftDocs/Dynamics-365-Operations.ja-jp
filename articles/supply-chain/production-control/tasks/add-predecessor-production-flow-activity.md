--- 
title: "生産フロー活動への先行処理の追加"
description: "生産フロー バージョンでは、すべての活動は順番に配列する必要があります。"
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d19fb20e8cc941daeaa506e4bf1cb0c7031cf2ee
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>生産フロー活動への先行処理の追加

[!include [task guide banner](../../includes/task-guide-banner.md)]

生産フロー バージョンでは、すべての活動は順番に配列する必要があります。 活動には、複数の先行または後続の処理を含めることができます。 

この手順は、活動に先行処理を関連付ける方法を示します。 

この作業を行うには、接続できる2つ以上の活動を有するドラフト バージョンがある生産フローが必要です。 

詳細については、 「生産フローおよびリーン生産」というホワイト ペーパーを参照します。


## <a name="find-the-production-flow-and-version"></a>生産フロー バージョンを検索する
1. [生産管理] > [設定] > [リーン生産フロー] > [生産フロー] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. 一覧で、選択された行のリンクをクリックします。
4. 一覧で、目的のレコードを見つけ、選択します。
5. [活動] をクリックします。

## <a name="select-an-activity-and-add-a-predecessor"></a>[活動] を選択して、[先行処理] を追加する
1. 一覧で、目的のレコードを見つけ、選択します。
2. [先行処理の追加] をクリックします。
3. [活動] フィールドで値を入力または選択します。
4. [サイクル時間の比率] フィールドで、数値を入力します。
    * 活動関係の既定のサイクル時間率は 1 です。 これは、活動またはタクト タイムの両方が同じペースで実行されると仮定します。 先行処理がより速いペース (下部タクト タイム) で実行中の場合、比率は1以下にします。先行がそれよりも遅いペース (より大きい)で実行中の場合、サイクル時間率は1以上になります。  
5. [OK] をクリックします。


