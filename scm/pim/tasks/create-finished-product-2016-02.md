--- 
title: "完成品の作成 (2016 年 2 月のみ)"
description: "このタスクでは、完成品の作成に重点を置きます。"
author: BibiSp
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: a31a18ee075c865d5ad99f7cf4ca2eac7c6281c9
ms.contentlocale: ja-jp
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-finished-product-february-2016-only"></a>完成品の作成 (2016 年 2 月のみ)

[!include[task guide banner](../../includes/task-guide-banner.md)]

このタスクでは、完成品の作成に重点を置きます。 これは、BOM 計算シリーズの最初のタスクです。 このタスクの作成に使用するデモ データの会社は USMF です。

1. [製品情報管理] > [製品] > [リリースされた製品] の順に移動します。
2. [新規] をクリックします。
3. [製品番号] フィールドに値を入力します。
    * デモの場合、「BOM_1」を入力します。  
4. [品目モデル グループ] フィールドで、値を入力または選択します。
    * [STD] を選択します。 STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。  
5. [品目グループ] フィールドで、値を入力または選択します。
    * たとえば、「AUDIO」を選択します。 これは原価計算には影響しません。  
6. [保管分析コード グループ] フィールドで、値を入力または選択します。
    * 「SiteWH」を選択します。 サイトと倉庫のみがデモに使用されます。  
7. [追跡用分析コード グループ] フィールドで、値を入力または選択します。
    * 追跡用分析コードはこの例には使用されません。「なし」を選択してください。  
8. [OK] をクリックします。
9. [アクション] ウィンドウで [在庫の管理] をクリックします。
10. [既定の注文設定] をクリックします。
11. [既定の注文タイプ] フィールドで、「生産」を選択します。
    * これは生成される完成品であるので、「生産」を選択します。  
12. [購買サイト] フィールドで、値を入力または選択します。
    * デモの場合は、「サイト 1」を選択します。  
13. [在庫サイト] フィールドで、値を入力または選択します。
    * この例では、「サイト 1」を選択します。  
14. [販売サイト] フィールドで、値を入力または選択します。
    * この例では、「サイト 1」を選択します。  
15. ページを閉じます。


