--- 
title: "詳細ルール構造の作成と割り当て"
description: "このタスク ガイドでは、詳細ルール構造の作成と勘定構造への割り当てについて説明します。"
author: aprilolson
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 18ad27eb673745d09569f6a49c8bc66132550f35
ms.openlocfilehash: 8bce8cabe3570cf9e32419e478204e9b59a0cc78
ms.contentlocale: ja-jp
ms.lasthandoff: 10/27/2017

---
# <a name="create-and-assign-advanced-rule-structures"></a>詳細ルール構造の作成と割り当て

[!include [task guide banner](../../includes/task-guide-banner.md)]

このタスク ガイドでは、詳細ルール構造の作成と勘定構造への割り当てについて説明します。 このガイドでは、USMF デモ会社を使用します。


## <a name="create-an-advanced-rule-structure"></a>詳細なルール構造の作成
1. [総勘定元帳] > [勘定科目表] > [構造] > [詳細ルール構造] の順に移動します。
2. [新規] をクリックすると、ドロップ ダイアログが開きます。
3. [詳細ルール構造] フィールドにルール構造を説明する名前を入力します。
4. [説明] フィールドに構造を説明する値を入力します。
5. [OK] をクリックします。
6. [区分の追加] をクリックします。
7. 区分リストで、財務分析コードを選択します。
    * たとえば [店舗] です。  
8. [区分の追加] をクリックします。
9. 一覧で、詳細ルール構造を表示するリンクをクリックします。
10. [有効化] をクリックします。
11. [有効化] をクリックします。

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a>詳細ルール構造の勘定構造への適用
1. フォームを閉じます。
2. ページを閉じます。
3. [総勘定元帳] > [勘定科目表] > [構造] > [勘定構造のコンフィギュレーション] に移動します。
4. 一覧で、詳細ルールを適用する勘定構造を検索し選択します。
5. 勘定構造の名前をクリックして開きます。
6. [編集] をクリックします。
    * [詳細ルール] をクリックすると、勘定構造を [ドラフト モード] に設定するよう要求されます。  
7. [詳細ルール] をクリックします。
8. [新規] をクリックすると、ドロップ ダイアログが開きます。
9. [詳細ルール] フィールドに値を入力します。
10. [名前] フィールドに値を入力します。
11. [作成] をクリックします。
12. [新しい基準の追加] をクリックします。
13. [適用箇所] フィールドで、主勘定または財務分析コードを選択します。
14. [演算子] フィールドで、「is between」や「includes」などのオプションを選択します。
15. [値] フィールドに値を入力します。
16. [終了日] フィールドに値を入力します。
17. [追加] をクリックしてドロップ ダイアログを開きます。
18. 一覧で、入力した基準と一致した場合に使用する詳細ルール構造を検索します。
19. [追加] をクリックします。
20. ページを閉じます。
21. [有効化] をクリックします。
22. [有効化] をクリックします。


