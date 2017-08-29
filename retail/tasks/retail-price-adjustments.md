--- 
title: "小売価格調整の管理"
description: "この手順では、小売価格調整の作成を説明します。"
author: josaw1
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: ab13aced30f90c4d7c8b96f30340fff6e3eee927
ms.contentlocale: ja-jp
ms.lasthandoff: 07/28/2017

---
# <a name="retail-price-adjustments"></a>小売価格調整の管理

[!include[task guide banner](../includes/task-guide-banner.md)]

この手順では、小売価格調整の作成を説明します。 小売の価格調整では、品目の販売価格を直接設定できます。また、基準販売価格、あるいは売買契約の販売価格を変更できます。 この手順では、デモ データの会社 USRT を使用します。

1. [価格設定および割引の管理] をクリックします。
2. [価格調整] タブをクリックします。
3. [新規] をクリックします。
    * ここで、小売割引、小売価格調整、売買契約仕訳帳、およびカテゴリの価格決定ルールを含む、よく使用する価格および割引ルールを作成できます。  
4. [価格調整] をクリックします。
5. [名前] フィールドに値を入力します。
6. [明細行] セクションを展開します。
7. [追加] をクリックします。
    * この例の場合、[製品] フィールドに「81126」と入力します。    次に、[割引率] フィールドに「10.0」を入力します。  
    * 割引率のタイプの価格調整では、基準販売価格または売買契約の販売価格を削減します。  
8. [追加] をクリックします。
    * この例の場合、[製品] フィールドに「81125」と入力します。    その後、[割引方法] フィールドで [現金割引金額] を選択します。    最後に、[現金割引金額] フィールドに「5.0」を入力します。  
    * [現金割引金額] 割引タイプは、基準価格または売買契約の価格から差し引かれる金額です。  
9. [価格グループ] をクリックします。
    * [価格グループ] フィールドで [RP-Houston] を選択します。  
    * これにより、ヒューストン店舗に価格調整が関連付けられます。  
10. [保存] をクリックします。
11. ページを閉じます。
12. [ステータス] フィールドで [有効] を選択します。
13. [保存] をクリックします。
14. ページを閉じます。
15. ページを更新します。


