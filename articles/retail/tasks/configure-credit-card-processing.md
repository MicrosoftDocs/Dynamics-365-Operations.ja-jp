--- 
title: "クレジット カード処理のコンフィギュレーション"
description: "この手順は、支払プロバイダの一覧を表示し、売掛金勘定の支払口座を構成する方法を説明しています。"
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c8e7bfbf6b51aca9cf8a7f800ac7db22c0330d00
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="configure-credit-card-processing"></a>クレジット カード処理のコンフィギュレーション

[!include[task guide banner](../includes/task-guide-banner.md)]

この手順は、支払プロバイダの一覧を表示し、売掛金勘定の支払口座を構成する方法を説明しています。 この手順では、デモ データの会社 USRT を使用し、管理者および IT プロフェッショナルを対象としています。


## <a name="view-a-list-of-payment-providers"></a>支払プロバイダーの一覧を表示します。
1. [売掛金勘定] > [支払設定] > [支払サービス] に移動します。
2. [使用可能プロバイダーの表示] をクリックします。

## <a name="configure-payment-account"></a>支払アカウントの構成
1. [新規] をクリックします。
2. [支払サービス] フィールドに値を入力します。
3. [支払コネクタ] フィールドで、オプションを選択します。
4. [支払サービス アカウント] セクションの展開を切り替えます。
5. [環境] フィールドに「PROD」を入力します。
6. [クレジット カード タイプ] をクリックします。
7. [支払仕訳帳] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
8. 一覧で、選択された行のリンクをクリックします。
9. [追加] をクリックします。
10. [通貨] フィールドに値を入力します。
11. 一覧で、目的のレコードを見つけ、選択します。
12. [支払仕訳帳] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
13. 一覧で、選択された行のリンクをクリックします。
14. [追加] をクリックします。
15. [通貨] フィールドに値を入力します。
16. 一覧で、目的のレコードを見つけ、選択します。
    * 必要なカード タイプの数だけこれらの手順を繰り返すことができます。  
17. [支払仕訳帳] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
18. 一覧で、選択された行のリンクをクリックします。
19. [追加] をクリックします。
20. [通貨] フィールドに値を入力します。
21. [保存] をクリックします。
22. ページを閉じます。
23. [検証] をクリックします。
24. [新しいクレジット カードの既定のプロセッサ] チェックボックスをオンにします。
25. [保存] をクリックします。


