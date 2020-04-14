---
title: 請求仕訳帳の仕入先請求書の記録
description: このタスク ガイドでは、発注書に関連付けられていない仕入先請求書を記録する方法について説明します。
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5277081d9f7adcc43c30d30208d13c7e39d76118
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140378"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>請求仕訳帳の仕入先請求書の記録

[!include [banner](../../includes/banner.md)]

このタスク ガイドでは、発注書に関連付けられていない仕入先請求書を記録する方法について説明します。 このタイプの請求書の例には、消耗品やサービスの経費があります。  このレコードでは、USMF デモ会社を使用します。

1. **ナビゲーション ウィンドウ > モジュール > 買掛金勘定 > ワークスペース > 仕入先請求書入力**の順に移動します。
2. **アクション ペイン**で、**新しい請求仕訳帳**をクリックします。
3. **新規** をクリックします。
4. **名前**フィールドで、仕訳帳名を入力するか、ドロップ ダウン ボタンをクリックしてルックアップを開きます。
5. **説明**フィールドで、値を入力します。
6. **アクション ウィンドウ**で、**明細行**をクリックします。 **日付**フィールドで、総勘定元帳を更新する転記日付を入力します。  
7. **勘定**フィールドで、**仕入先**を指定します。
8. **請求書**フィールドに、請求書番号を入力します。
9. **説明**フィールドで、値を入力します。
10. **貸方**フィールドに、数値を入力します。
11. **相手勘定**フィールドで、勘定番号を入力するか、ドロップ ダウン ボタンをクリックしてルックアップを開きます。
    * **消費税グループ**は、仕入先勘定の既定値になります。  
    * **品目消費税グループ**は、**相手勘定**フィールドで指定された主勘定の既定値になります。  
    * **期日**は支払条件に基づいて計算されます。  
    * **現金割引**は仕入先口座から既定値が取得されます。  
12. **転記** をクリックします。
13. ページを閉じます。

