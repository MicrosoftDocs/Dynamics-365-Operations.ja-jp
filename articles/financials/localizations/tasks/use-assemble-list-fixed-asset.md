--- 
title: "固定資産の組み立て一覧の使用 (日本)"
description: "日本では、在庫品目を固定資産に移転できます。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4b9755b0320ad9a709aa56d77fa2133e33ecdbb0
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="use-assemble-list-for-fixed-assets-japan"></a>固定資産の組み立て一覧の使用 (日本)

[!include [task guide banner](../../includes/task-guide-banner.md)]

日本では、在庫品目を固定資産に移転できます。 



このタスクでは、組み立てリストを使用して在庫品目を使用すると同時に、固定資産を作成するプロセスを説明します。



このタスクは デモ データ会社 JPMF を使用して作成されました。


## <a name="assign-component-in-an-assembly-list"></a>組み立て一覧のコンポーネントの割り当て
1. [固定資産] > [固定資産] > [固定資産] に移動します。
2. 一覧で、選択された行をマークします。
    * 組み立てリストを割り当てる固定資産を選択します。  
3. [アクション] ウィンドウで、[固定資産] をクリックします。
4. [コンポーネント] をクリックします。
5. [追加] をクリックします。
6. [品目番号] フィールドに値を入力します。
    * たとえば、「D0001」を入力します。  
7. [保存] をクリックします。

## <a name="use-the-assembly-list-to-post-a-fixed-asset-write-up-transaction"></a>組み立て一覧を使用した固定資産評価増トランザクションの転記
1. 次の順に移動します: [固定資産] > > [固定資産仕訳帳]。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
4. [明細行] をクリックします。
5. [日付] フィールドに日付を入力します。
6. [トランザクション タイプ] フィールドで [評価増調整] を選択します。
7. [勘定] フィールドで、任意の値を指定します。
    * 組み立てリストに割り当てた固定資産番号を選択します。  
8. [借方] フィールドに数値を入力します。
    * 在庫品目の原価を入力します。  
9. [転記] をクリックします。


