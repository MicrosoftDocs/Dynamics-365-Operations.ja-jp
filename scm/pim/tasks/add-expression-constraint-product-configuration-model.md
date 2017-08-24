--- 
title: "製品コンフィギュレーション モデルへ式の制約の追加"
description: "この手順は、製品コンフィギュレーション モデルに新しい式の制約を追加する方法を表示します。"
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: b8286eba5c799789ebba9a501a5a0b06ccdaabb1
ms.contentlocale: ja-jp
ms.lasthandoff: 07/28/2017

---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>製品コンフィギュレーション モデルへ式の制約の追加

[!include[task guide banner](../../includes/task-guide-banner.md)]

この手順は、製品コンフィギュレーション モデルに新しい式の制約を追加する方法を表示します。 ユーザーが金属の前グリルを選択した場合は、コーナーの保護をスピーカーに適用する必要があることを義務付ける方法を表示します。 その手順は、デモ会社 USMF で [ハイエンド スピーカー] コンポーネントを使用します。


## <a name="create-an-expression-constraint"></a>式の制約の作成
1. [製品バリアント モデルの定義] をクリックします。
2. [製品コンフィギュレーション モデル] をクリックします。
3. 一覧で、目的のレコードを見つけ、選択します。
    * この例では、ハイエンド スピーカー モデルを使用します。  
4. 一覧で、選択された行のリンクをクリックします。
5. [制約] セクションを展開します。
6. [追加] をクリックします。
7. [作成] をクリックします。
8. [名前] フィールドに値を入力します。

## <a name="enter-expression"></a>式の入力
1. [式の編集] をクリックします。
    * この段階で、タスク記録のユーザー インターフェイスのロックを解除する場合、制約式の構築のため、[IntelliSense] と記号のリストを使用できます。  
2. [ConstraintBody] フィールドで、「Implies[FrontGrill=="Metal", CornerProtection]」と入力します。
    * この式ロジックの状態 : [前グリル] が金属の場合、角の保護オプションを選択する必要があります。  
3. [検証] をクリックします。
    * 検証機能は、制約式に対して実行され、構文エラーを確認します。  
4. [閉じる] をクリックします。
5. [OK] をクリックします。


