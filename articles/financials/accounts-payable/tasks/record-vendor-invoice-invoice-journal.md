--- 
title: "請求仕訳帳の仕入先請求書の記録"
description: "このタスク ガイドでは、発注書に関連付けられていない仕入先請求書を記録する方法について説明します。"
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 42f93e6d8fcf62babc3e3244bc1fe76d1efd9d13
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>請求仕訳帳の仕入先請求書の記録

[!include [task guide banner](../../includes/task-guide-banner.md)]

このタスク ガイドでは、発注書に関連付けられていない仕入先請求書を記録する方法について説明します。 このタイプの請求書の例には、消耗品やサービスの経費があります。  このレコードでは、USMF デモ会社を使用します。

1. [買掛金勘定] > [ワークスペース] > [仕入先請求書入力] に移動します。
2. [新しい請求仕訳帳] をクリックします。
3. [新規] をクリックします。
4. [名前] フィールドで、仕訳帳名を入力するか、ドロップ ダウン ボタンをクリックしてルックアップを開きます。
5. [説明] フィールドに値を入力します。
6. [明細行] をクリックします。
    * [日付] フィールドで、総勘定元帳を更新する転記日付を入力します。  
7. [勘定] フィールドで、仕入先を指定します。
8. [請求書] フィールドに請求書番号を入力します。
9. [説明] フィールドで値を入力します。
10. [貸方] フィールドに数値を入力します。
11. [相手勘定] フィールドで、勘定番号を入力するか、ドロップ ダウン ボタンをクリックしてルックアップを開きます。
    * 売上税グループは、仕入先から既定値が取得されます。  
    * [品目売上税グループ] は、[相手勘定] フィールドで指定された主勘定から既定値が取得されます。  
    * [期日] は、支払条件に基づいて計算されます。  
    * [現金割引] は、仕入先から既定値が取得されます。  
12. [転記] をクリックします。
13. ページを閉じます。


