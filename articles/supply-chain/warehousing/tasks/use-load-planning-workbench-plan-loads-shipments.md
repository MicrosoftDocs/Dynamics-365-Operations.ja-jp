--- 
title: "積荷計画ワークベンチを使用した積荷および出荷の計画"
description: "この手順では、販売注文の積荷を作成するための積荷計画ワークベンチの使用方法を示します。"
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f840a4c15305af5f55451ae7f1cec2da25e685a4
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>積荷計画ワークベンチを使用した積荷および出荷の計画

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

この手順では、販売注文の積荷を作成するための積荷計画ワークベンチの使用方法を示します。 前提条件として、まず販売注文を作成します。 この手順は、配送コーディネーターの日常の作業一部です。 この手順の作成に使用するデモ データの会社は USMF です。


## <a name="create-a-sales-order"></a>販売注文の作成
1. [売掛金勘定] > [注文] > [すべての販売注文] の順に移動します。
2. [新規] をクリックします。
3. [顧客口座] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 勘定 US-004 を選択します。
5. [OK] をクリックします。
6. [品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
7. 品目 A0001 を選択します。
    * A0001 は輸送管理に対して有効になっています。  
8. 一覧で、選択された行のリンクをクリックします。
9. [数量] フィールドに数値を入力します。
10. [倉庫] フィールドに、「24」と入力します。
    * この例では、倉庫 24 を選択します。 この倉庫は、輸送管理および高度な倉庫管理で有効になっています。  
11. [保存] をクリックします。
12. ページを閉じます。

## <a name="create-a-new-load"></a>新しい積荷の作成
1. [配送管理] > [計画] > [積荷計画ワークベンチ] の順に移動します。
2. [販売明細行] タブをクリックします。
    * 次に、作成した販売注文の積荷を構築します。 積荷は、発注書、移動オーダー、および販売注文からの供給と需要に基づいて作成することができます。  
3. アクション ウィンドウで、[供給と需要] をクリックします。
4. [新しい積荷へ] をクリックします。
5. [読み込みテンプレート ID] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
    * 積荷のテンプレートには、積荷全体の重量および容積の最大測定値を定義します。 たとえば、積荷テンプレートは、コンテナーまたはトラックのサイズを表す場合があります。  
6. 一覧で、選択された行のリンクをクリックします。
7. [OK] をクリックします。

## <a name="rate-and-route-the-load"></a>積荷のレートと工順
1. [評価とルート指定] をクリックします。
2. [工順ワークベンチの評価] をクリックします。
3. [レート ショップ] をクリックします。
4. 一覧で、目的のレコードを見つけ、選択します。
5. [割り当て] をクリックします。
6. ページを閉じます。
7. ページを閉じます。


