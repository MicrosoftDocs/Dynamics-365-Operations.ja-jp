--- 
title: "消費税レポートの生成 (日本)"
description: "この手順では、日本の消費税申告の生成について説明します。"
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8beb86f670ebc99212e6ba658f7d0aba041c8f38
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="generate-consumption-tax-report-japan"></a>消費税レポートの生成 (日本)

[!include[task guide banner](../../includes/task-guide-banner.md)]

この手順では、日本の消費税申告の生成について説明します。



この手順は、デモ データ会社 JPMF を使用して作成されました。





1. [税] > [申告] > [売上税] > [消費税申告書] の順に移動します。
2. [開始日] フィールドに日付を入力します。
    * 例: 2012/1/1  
3. [終了日] フィールドで、日付を入力します。
    * 例: 2012/12/31  
4. [決済期間] フィールドに値を入力します。
5. [申告のタイプ] フィールドで、オプションを選択します。
6. [計算方法] フィールドで、オプションを選択します。
7. [修正] フィールドで、 [はい] を選択します。
    * 以前にレポートを生成し、もう一度生成する場合は、既存のレコードの修正を更新するように選択する必要があります。  
8. [OK] をクリックします。
9. [編集] をクリックします。
10. [項目 6] フィールドに番号を入力します。
    * データはトランザクションから取得され、集計されます。 調整のために編集可能なフィールドを更新できます。  
11. [保存] をクリックします。
12. [金額の更新] をクリックします。
    * これにより、金額を再計算します。  
13. [確定] をクリックします。
14. [はい] をクリックします。
15. [消費税申告] をクリックします。
16. [税額の計算] タブをクリックします。
17. [編集] をクリックします。
18. [項目 10] フィールドに番号を入力します。
19. [保存] をクリックします。
20. [金額の更新] をクリックします。
21. [追加情報] タブをクリックします。
    * [追加情報] タブでは、情報を、コンフィギュレーションされたとおりに印刷します。  
    * 例: [割賦基準の適用] スライダーを「はい」に変更して、最終レポート上に印刷します。  
22. [確定] をクリックします。
23. [はい] をクリックします。
24. [アクション] ペインで [消費税申告] をクリックします。
    * [レポートを印刷] をクリックして、最終レポートを生成します。  


