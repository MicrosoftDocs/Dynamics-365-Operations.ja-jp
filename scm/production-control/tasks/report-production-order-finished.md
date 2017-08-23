--- 
title: "製造オーダーの完了レポート"
description: "この手順では、製造オーダーを完了として報告する方法を示します。"
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ff651be006b4bbe205aa9937bd7927e37a83a558
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="report-a-production-order-as-finished"></a>製造オーダーの完了レポート

[!include[task guide banner](../../includes/task-guide-banner.md)]

この手順では、製造オーダーを完了として報告する方法を示します。 この手順の作成に使用するデモ データの会社は USMF です。 これは、製造オーダーのライフ サイクルを説明する 7 個の手順の 6 番目です。


## <a name="report-a-production-order-as-finished"></a>製造オーダーの完了レポート
1. [生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。
    * [開始済] 状態を持つ製造オーダーを選択します。  
2. アクション ウィンドウで、[製造オーダー] をクリックします。
3. [完了レポート] をクリックします。
    * このページでは、完了を報告する完成品の数量を確認できます。  
4. [一般] タブをクリックします。
5. [良品数量] を「18」に設定します。
6. [不良数量] を「2」に設定します。
7. [エラーの原因] フィールドで、[材料] を選択します。
8. [終了ジョブ] チェック ボックスをオンまたはオフにします。
9. [適用エラー] チェック ボックスをオンまたはオフにします。
10. [OK] をクリックします。

## <a name="verify-the-report-as-finished-journal"></a>完了レポート仕訳帳の確認
1. アクション ウィンドウで、[表示] をクリックします。
2. [完了報告済] をクリックします。
3. 一覧で、選択された行をマークします。
4. 一覧で、選択された行のリンクをクリックします。
    * 完了レポート仕訳帳が転記されます。 仕訳帳に調整を加える場合は、新しい仕訳帳を作成し、この仕訳帳に手動で変更を加えることができます。  


