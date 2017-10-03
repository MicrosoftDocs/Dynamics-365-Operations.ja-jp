--- 
title: "買掛金勘定からの資産の作成および取得"
description: "このタスク ガイドでは、購買プロセスで固定資産を作成し、取得する方法を説明します。"
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f814d20bc16bb3334ae4bc449cc0d45843487023
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>買掛金勘定からの資産の作成および取得

[!include[task guide banner](../../includes/task-guide-banner.md)]

このタスク ガイドでは、購買プロセスで固定資産を作成し、取得する方法を説明します。  ここでは、経理担当者、買掛金勘定係、デモ会社 USMF を使用します。


## <a name="set-fixed-assets-parameters"></a>固定資産パラメーターの設定
1. [固定資産] > [設定] > [固定資産パラメーター] の順に移動します。
2. [発注書] セクションを展開または折りたたみます。
3. [購買からの資産の取得を許可する] チェック ボックスをオンにします。
4. [製品受領書または請求書の転記時に資産を作成する] チェック ボックスをオンにします。

## <a name="create-a-new-vendor-invoice"></a>新しい仕入先請求書の作成
1. [買掛金勘定] > [ワークスペース] > [仕入先請求書入力] に移動します。
2. [新しい仕入先請求書] をクリックします。
3. [請求元仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、選択された行のリンクをクリックします。
5. [数] フィールドに値を入力します。
6. [転記日付] フィールドに日付を入力します。
7. [明細行の追加] をクリックします。
8. [品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
    * 在庫のない品目または調達カテゴリが、固定資産の取得に使用できます。  
9. 一覧で、選択された行のリンクをクリックします。
10. [数量] フィールドに数値を入力します。
    * 数量に関係なく、1 つの請求明細行が作成する固定資産は 1 つのみです。  請求書の数量フィールドの値は、固定資産の数量に転送されます。  
11. [単価] フィールドに数値を入力します。
12. [明細行の詳細] セクションを展開または折りたたみます。
13. [固定資産] タブをクリックします。
14. [新しい固定資産の作成] チェック ボックスをオンにします。
15. [固定資産グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
16. 新しい固定資産を作成するときに使用する固定資産グループを一覧で選択します。
17. 一覧で、選択された行のリンクをクリックします。
18. [転記] をクリックします。
    * 固定資産は、請求書の転記時に作成および取得されます。  


