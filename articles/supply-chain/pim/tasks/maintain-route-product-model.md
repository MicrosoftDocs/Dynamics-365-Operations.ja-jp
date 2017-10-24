--- 
title: "製品モデルのルートの管理"
description: "この手順を実行するには、既存の製品コンフィギュレーション モデルが必要です。"
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2f3df2bd6018d07d65950398e38821cad475752e
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="maintain-a-route-for-a-product-model"></a>製品モデルのルートの管理

[!include[task guide banner](../../includes/task-guide-banner.md)]

この手順を実行するには、既存の製品コンフィギュレーション モデルが必要です。 この手順は、このプロセスを説明するために、デモ会社 USMF の [ハイエンド スピーカー] モデルを使用します。


## <a name="add-a-route-operation"></a>工順工程の追加
1. [製品バリアント モデルの定義] をクリックします。
2. [製品コンフィギュレーション モデル] をクリックします。
3. 一覧で、目的のレコードを見つけ、選択します。
    * この練習の [ハイエンド スピーカー] モデルを選択します。  
4. 一覧で、選択された行のリンクをクリックします。
5. [工順工程] セクションを展開します。
6. [追加] をクリックします。
7. [名前] フィールドに値を入力します。
8. [説明] フィールドに値を入力します。
9. [保存] をクリックします。

## <a name="enter-route-operation-details"></a>工順工程の詳細の入力
1. [工順工程の詳細] をクリックします。
2. [操作] フィールドで、値を入力または選択します。
3. [工程 一連番号 フィールドで番号を入力します。
    * 工程番号が工順を決定します。  
    * 工順工程の各プロパティは、静的値を取得するか、または属性にマップすることができます。 属性へのマッピングは、コンフィギュレーションの一部として設定された値になります。  
4. [工順グループ] フィールドで、値を入力または選択します。
    * 工順グループは、原価計算、消費、設定の重要な動作を決定します。  
5. [設定] タブをクリックします。
6. [時間] タブをクリックします。
7. 処理数量 フィールドで、数値を入力します。
    * 一つの工程間で処理される数量を決定します。  
8. [時間変換係数] フィールドで、数値を入力します。
    * 時間の比率を入力します。  
9. [設定] チェック ボックスを選択します。
10. [実行時間] フィールドで、数値を入力します。
    * 指定した数量に対する処理時間を決定します。  
11. [リソース要件] タブをクリックします。
12. [追加] をクリックします。
13. 一覧で、選択された行をマークします。
14. [要件のタイプ] フィールドでオプションを選択します。
    * 保有している特定のリソースまたは機能を指定するかどうかを決定します。  
15. [要件] フィールドで、値を入力または選択します。
16. [OK] をクリックします。


