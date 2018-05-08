--- 
title: "制約付き計画の生成"
description: "この手順では、材料制約と能力制約の両方を考慮した計画の作成方法を示します。"
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 59c6a4a2b239b3fd6b6ddc8f06bfd007f0191f0a
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="generate-a-constrained-plan"></a>制約付き計画の生成

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、材料制約と能力制約の両方を考慮した計画の作成方法を示します。 計画により、材料が利用可能でないうちに生産が開始しないように、またリソースが予約超過にならないようにします。 

この手順の作成に使用するデモ データの会社は USMF です。 この手順は、生産の計画者を対象としています。


## <a name="set-up-a-constrained-plan"></a>制約付き計画の設定
1. [マスター プラン] をクリックします。
2. [マスター プラン] をクリックします。
3. 一覧で、目的のレコードを見つけ、選択します。
    * 例: StaticPlan  
4. [有限能力] フィールドで [はい] を選択します。
5. [有限能力タイム フェンス] フィールドに「30」と入力します。
6. [タイム フェンス (日)] セクションを展開します。
7. [能力] フィールドで [はい] を選択します。
8. [能力スケジューリング タイム フェンス (日)] フィールドに、数値を入力します。
    * 例: 60  
9. [計算済遅延] フィールドで、[はい] を選択します。
10. [遅延の計算タイム フェンス (日)] フィールドに、数値を入力します。
    * 例: 60  
11. [計算済遅延] セクションを展開します。
12. [計算済遅延を要求日に追加] フィールドで「はい」を選択します。
13. [計算済遅延を要求日に追加] フィールドで「はい」を選択します。
14. [計算済遅延を要求日に追加] フィールドで「はい」を選択します。
15. ページを閉じます。

## <a name="create-a-constrained-plan"></a>制約付き計画の作成
1. [実行] をクリックします。
2. [マスター プラン] フィールドで、値を入力または選択します。
    * 制約を設定した計画を選択します。  
3. [OK] をクリックします。
    * しばらく時間がかかる場合があります  
4. [計画オーダー] をクリックします。


