---
title: 製造オーダーの開始
description: この手順では、作業現場での製造オーダーの開始方法を説明します。
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f83091a9f3e96a9176860bd16fa5969507488a25
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547471"
---
# <a name="start-a-production-order"></a>製造オーダーの開始

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、作業現場での製造オーダーの開始方法を説明します。 時間および材料の消費は、このプロセスでレポートされます。 この手順の作成に使用するデモ データの会社は USMF です。 これは、製造オーダーのライフ サイクルを説明する 7 個の手順の 5 番目です。


## <a name="start-a-production-order"></a>製造オーダーの開始
1. [生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。
    * ステータスが [リリース済] の製造オーダーを選択します。  
2. アクション ウィンドウで、[製造オーダー] をクリックします。
3. [開始] をクリックします。
    * このページで、製造オーダーの開始を確認できます。  
4. [一般] タブをクリックします。
5. [開始行程 一連番号 フィールドで、「10」を入力します。
6. [自動工順消費] フィールドで、「常に」を選択します。
7. [工順カード転記] チェック ボックスをクリックします。
8. [自動 BOM 消費] フィールドで、「常に」を選択します。
9. [ピッキング リスト転記] チェックボックスをクリックします。
10. [ピッキング リストの印刷] チェックボックスをクリックします。
11. [OK] をクリックします。
    * これは、製造オーダーに使用される材料を示す印刷されたピッキング リストです。  
12. ページを閉じます。

## <a name="validate-the-picking-list"></a>ピッキング リストの検証
1. アクション ウィンドウで、[表示] をクリックします。
2. [ピッキング リスト] をクリックします。
3. 一覧で、目的のレコードを見つけ、選択します。
4. 一覧で、選択された行のリンクをクリックします。
5. [編集] をクリックします。
6. [消費] フィールドに数値を入力します。
7. [転記] をクリックします。
8. [OK] をクリックします。
    * ピッキング リスト仕訳帳には、製造オーダーによって消費される材料が転記されます。 見積数量と実際の消費量に差がある場合は、仕訳帳を転記する前に調整することができます。  
9. [グリッド パネル] タブをクリックします。
10. ページを閉じます。

## <a name="verify-the-route-card-journal"></a>工順カード仕訳帳の確認
1. アクション ウィンドウで、[表示] をクリックします。
2. [工順カード] をクリックします。
3. 一覧で、目的のレコードを見つけ、選択します。
4. 一覧で、選択された行のリンクをクリックします。
5. [編集] をクリックします。
6. [時間] フィールドに数値を入力します。
7. [転記] をクリックします。
8. [OK] をクリックします。
    * [工順カード仕訳帳] では、個々の工程にかかった時間が記録されます。 良品および不良品の数量をレポートできます。  
