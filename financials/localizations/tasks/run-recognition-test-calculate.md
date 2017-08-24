--- 
title: "認識テストの実行と個別資産の減損損失の計算 (日本)"
description: "このタスクは、認識テストの実行方法および個々の資産の減損金額の計算方法について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 61ca53aa8585193b95eea80e63650ecd75e3a39f
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="run-the-recognition-test-and-calculate-the-impairment-amount-on-individual-assets-japan"></a>認識テストの実行と個別資産の減損損失の計算 (日本)

[!include[task guide banner](../../includes/task-guide-banner.md)]

このタスクは、認識テストの実行方法および個々の資産の減損金額の計算方法について説明します。



このタスクを完了するには、個々の資産の減損インジケーターを管理しておく必要があります。



このタスクは デモ データ会社 JPMF を使用して作成されました。


## <a name="impairment-recognition-test"></a>減損認識テスト
1. [固定資産] > [定期処理タスク] > [個別資産の減損] > [減損認識テスト] の順に移動します。
2. [クエリ] をクリックします。
3. 一覧で、目的のレコードを見つけ、選択します。
    * この例では、[固定資産グループ] 行を選択します。  
4. [基準] フィールドに値を入力します。
    * 例: TOOL-M  
5. [OK] をクリックします。
    * 減損インジケーターを構成済の、3つの固定資産が表示されることを確認します。  
    * TOOLM-000006 に減損損失調整はありませんが、TOOLM-000007 および TOOLM-000008 の減損損失調整はそれぞれ -1,750,000.00 と -2,250,000.00 です。  
6. [減損の保存] をクリックして、ドロップ ダイアログを開きます。
7. [説明] フィールドに値を入力します。
8. [日付] フィールドに日付を入力します。
9. [OK] をクリックします。
    * 減損固定資産の確認フォームが表示されます。  
    * [減損テスト ID] は有効です。     後に [提案と転記] で使用するため、[減損テスト ID] を忘れないでください。   


