--- 
title: "製品モデルのルートの管理"
description: "この手順を実行するには、既存の製品コンフィギュレーション モデルが必要です。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 0e793466e021671501570aed06959d684d5e9c15
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---
# <a name="maintain-route-for-a-product-model"></a>製品モデルのルートの管理

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


