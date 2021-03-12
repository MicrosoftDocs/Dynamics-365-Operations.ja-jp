---
title: 販売注文のリーン ペギング
description: この手順で、品目がかんばんで生産される販売明細行からペギング ツリーを検証することに集中します。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457e7128bed2232a3e092b31136f768940482741
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994182"
---
# <a name="lean-pegging-from-sales-orders"></a>販売注文のリーン ペギング

[!include [banner](../../includes/banner.md)]

この手順で、品目がかんばんで生産される販売明細行からペギング ツリーを検証することに集中します。 ペギング ツリーを検証すると、すべてのかんばん作業が計画済になります。 これにより、すぐに生産を始められるようにする必要のある注文受付者の注文のシナリオに役立ちます。 この手順の作成に使用するデモ データの会社は USMF です。 この手順は、リーン会社で働いている上級の受付者を対象としています。


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a>かんばんの統制品目の販売注文の作成
1. [すべての販売注文] に移動します。
2. [新規] をクリックします。
3. [顧客口座] フィールドで値を入力または選択します。
    * US-001 を使用します。  
4. [OK] をクリックします。
5. [品目番号] フィールドに、'L0001' を入力します。
6. 数量を '30' に設定します。
    * イベントかんばんルールをトリガーするためには数量が 24 以上であることが重要です。  

## <a name="open-a-pegging-tree"></a>ペギング ツリーを開く 
1. [製品と供給] をクリックします。
2. [ペギング ツリーの表示] をクリックします。
    * ペギング ツリーが販売注文明細行に必要なペギングのすべてのレベルを示すことを確認します。 この場合、かんばんの 2 つのレベルとすべての必須コンポーネントがあります。  

## <a name="plan-the-pegging-tree"></a>ペギング ツリーの計画
1. ツリーで、「Sales line 000832\Kanban 000558」を選択します。
2. [かんばん作業] セクションを展開します。
    * かんばん作業のジョブ ステータスが [未計画] になっていることを確認します。  
3. [ペギング ツリー全体の計画] をクリックします。
    * これがペギング ツリーですべてのかんばん作業を計画し、[ジョブ ステータス] を「未計画」から「計画済」に変更します。  
4. ページを更新します。
    * かんばん作業の状態が「未計画」から「計画済」に変更されていることを確認します。  
5. ツリーで、「Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559」を選択します。
    * すべてのペギング ツリーが [計画済] であるため、2 番目のかんばんジョブも計画済になります。 かんばん作業の状態が [未計画] から [計画済] に変更されていることを確認します。  

