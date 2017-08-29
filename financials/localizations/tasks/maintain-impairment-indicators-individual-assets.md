--- 
title: "個別資産の減損インジケーターの管理 (日本)"
description: "このタスクを使用して、個別資産の減損インジケーターの管理方法を把握します。"
author: ShylaThompson
manager: AnnBe
ms.date: 09/22/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 1cb5d92aab7a85d93af365f318008ff9d468b431
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="maintain-impairment-indicators-on-individual-assets-japan"></a>個別資産の減損インジケーターの管理 (日本)

[!include[task guide banner](../../includes/task-guide-banner.md)]

このタスクを使用して、個別資産の減損インジケーターの管理方法を把握します。



この手順を実行する前に、「減損会計の共通パラメーターの設定」タスクを実行します。 



この手順では、JPMF デモ会社のデータを使用します。


## <a name="update-impairment-indicator-on-a-single-fixed-asset"></a>単一の固定資産の減損インジケーターを更新
1. [固定資産] > [固定資産] > [固定資産] に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
    * 例: TOOLM-000006  
3. [帳簿] をクリックします。
4. [機能] をクリックします。
5. [減損インジケーターの更新] をクリックします。
6. [新規] をクリックします。
7. [日付の変更] フィールドに、日付を入力します。
    * 例: 2013-04-01  
8. [説明] フィールドに値を入力します。
9. [割引前キャッシュ フロー] フィールドに数値を入力します。
    * この例では、フィールドに「3900000」を入力します。  
10. [回収可能金額] フィールドに、数値を入力します。
    * この例では、フィールドに「3350226」を入力します。  
11. [保存] をクリックします。

## <a name="update-impairment-indicator-on-the-impairment-management-form"></a>減損管理フォームの減損のインジケーターを更新
1. 次の順に移動します: [固定資産] > > .. > [減損管理]。
2. [クエリ] をクリックします。
3. 固定資産グループの行の、[基準] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. [OK] をクリックします。
5. 一覧で、目的のレコードを見つけ、選択します。
    * TOOLM-000007  
6. 一覧で、目的のレコードを見つけ、選択します。
    * TOOLM-000008  
7. [減損インジケーターの更新] をクリックします。
8. 一覧で、選択された行をマークします。
    * 固定資産番号「TOOLM-000007」を持つレコードを選択します。  
9. [日付の変更] フィールドに、日付を入力します。
    * 日付を定義 = 2013-04-01  
10. [説明] フィールドに値を入力します。
11. [割引前キャッシュ フロー] フィールドに数値を入力します。
    * 2500000.00 を入力します。  
12. [回収可能金額] フィールドに、数値を入力します。
    * 入力 = 2000000.00。  
13. 一覧で、目的のレコードを見つけ、選択します。
    * 固定資産番号「TOOLM-000008」を持つ行を選択します。  
14. [日付の変更] フィールドに、日付を入力します。
15. [説明] フィールドに値を入力します。
16. [割引前キャッシュ フロー] フィールドに数値を入力します。
    * 2000000.00 を入力します。  
17. [回収可能金額] フィールドに、数値を入力します。
    * 1500000.00 を入力します。  
18. [インジケーターの更新] をクリックします。


