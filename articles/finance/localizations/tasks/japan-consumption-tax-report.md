---
title: 日本消費税レポートの生成
description: この手順では、日本の消費税申告の生成について説明します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsumptionTaxCalcTrans_JP, LedgerConsumptionTaxReportTrans_JP
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bbfce615531315a65bb2a4992ba1e8c64eed90139ce781e6e211829367bac453
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740857"
---
# <a name="generate-japan-consumption-tax-report"></a>日本消費税レポートの生成

[!include [banner](../../includes/banner.md)]

この手順では、日本の消費税申告の生成について説明します。 この手順は、デモ データ会社 JPMF を使用して作成されました。

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

> [!NOTE]
> 2019 年 10 月 1 日から提出される消費税申告書を計算するには、**機能管理** ワークスペースの **消費税申告書** 機能を有効にする必要があります。 詳細については [機能管理の概要](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]