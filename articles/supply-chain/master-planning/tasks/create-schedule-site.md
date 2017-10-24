--- 
title: "サイトのスケジュールの作成"
description: "この手順は、サイトでまだ開始されていない製造オーダーをスケジュールする方法を示します。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 775428bf84a752c03c492e764fa9ed576ab64fb8
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-schedule-for-a-site"></a>サイトのスケジュールの作成

[!include[task guide banner](../../includes/task-guide-banner.md)]

この手順は、サイトでまだ開始されていない製造オーダーをスケジュールする方法を示します。  この手順を完了するのにデモ データの会社 USMF が使用されています。


## <a name="identify-production-orders-that-are-not-started"></a>開始されていない製造オーダーを識別します
1. [生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。
2. クイック フィルターを使用して、レコードを見つけます。 たとえば、「1」という値で [サイト] フィールドをフィルター処理します。
    * 1 では USMF 内のサイトを表します。 USMF を使用していない場合は、自分の会社からサイトを選択します。  
3. [ステータス列フィルター] を開きます。
4. [次の値と完全に一致する] フィルター演算子を使用して、[ステータス] フィールドに値 [スケジュール済] でフィルターを適用します。

## <a name="create-a-schedule"></a>スケジュールの作成
1. 一覧で、すべての行のマークを設定または解除します。
2. [アクション ペイン] で、[スケジュール] をクリックします。
3. [ジョブのスケジュール] をクリックします。
4. [スケジューリング指示] フィールドで、[出荷日からバックワード] をクリックします。
5. [有限能力] フィールドで [いいえ] を選択します。
6. [有限原材料] フィールドで [いいえ] を選択します。
7. [OK] をクリックします。
    * しばらく時間がかかる場合があります  

## <a name="view-the-result-of-scheduled-production-orders"></a>スケジュールされた製造オーダーの結果を表示します
1. 一覧で、選択された行をマークします。
    * どの行でもマークできます。  
2. アクション ウィンドウで、[製造オーダー] をクリックします。
3. [すべてのジョブ] をクリックします。
    * このページで、ジョブのリストを表示できます。 [スケジューリング] タブで、ジョブの開始日と終了日を表示できます。  
4. [材料] をクリックします。
    * このページで、製造オーダー工程用の材料消費見積、および現在利用可能な在庫を確認できます。  


