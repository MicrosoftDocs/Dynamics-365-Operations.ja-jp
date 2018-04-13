--- 
title: "連産品の材料計画の作成"
description: "生産計画担当者は、フォーミュラ連産品である品目の材料要求を計画します。"
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: c8805ca02525ae001fbd5e10ad9405fe60c7473e
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-material-plan-for-co-products"></a>連産品の材料計画の作成

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

生産計画担当者は、フォーミュラ連産品である品目の材料要求を計画します。 この手順の作成に使用するデモ データの会社は USP2 です。


## <a name="create-requirement-for-a-co-product"></a>連産品要求の作成
1. [既定のダッシュボード] に移動します。
2. [販売注文の処理と照会] をクリックします。
3. [新規] をクリックします。
4. [販売注文] をクリックします。
5. [顧客口座] フィールドに値を入力します。
    * 例: US-001  
6. [OK] をクリックします。
7. [品目番号] フィールドに値を入力します。
    * 例: P6003  
8. [数量] フィールドに数値を入力します。
    * 例: 50000  
9. [保存] をクリックします。

## <a name="create-a-material-plan-for-co-products"></a>連産品の材料計画の作成
1. [マスター プラン] をクリックします。
2. [計画] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. 一覧で、選択された行のリンクをクリックします。
    * 例: MasterPlan  
4. [実行] をクリックします。
5. [対象に含めるレコード] セクションを展開または折りたたみます。
6. [フィルター] をクリックします。
7. リストで、フィールド = 品目番号の行を選択します。
8. [基準] フィールドに値を入力します。
    * 例: P6003  
9. [OK] をクリックします。
10. [OK] をクリックします。
11. [計画オーダー] をクリックします。
12. クイック フィルターを使用して、レコードを見つけます。 たとえば、「P6000」という値を含む [品目番号] フィールドをフィルター処理します。
    * 販売注文を作成した品目の連産品としてのフォーミュラ品目でフィルター抽出します。  
13. 一覧で、選択された行をマークします。
    * フィルターによって返された行を選択します。  
14. 一覧で、選択された行のリンクをクリックします。
15. [ペギング] セクションを展開または折りたたみます。
16. 一覧で、選択された行のリンクをクリックします。
    * 計画オーダーは、連産品の販売注文にペギングされます。  
17. ページを閉じます。


