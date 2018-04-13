--- 
title: "資産除去債務見積の調整 (日本)"
description: "日本では、資産除去責務 (ARO) の最初の見積を調整できます。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/10/2016
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
ms.openlocfilehash: 23944f55a4bb4b318fa10edbaa956998380fd5c6
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="adjust-an-asset-retirement-obligation-estimate-japan"></a>資産除去債務見積の調整 (日本)

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

日本では、資産除去責務 (ARO) の最初の見積を調整できます。 



この手順を使用して、ARO 金額を調整する方法を説明します。



この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



このタスクは デモ データ会社 JPMF を使用して作成されました。


## <a name="adjust-the-aro-estimate"></a>ARO 見積の調整
1. [固定資産] > [資産除去責務] > [固定資産] に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. [アクション] ウィンドウで、[固定資産] をクリックします。
4. [資産除去責務] をクリックします。
5. [切り上げ] をクリックしてドロップ ダイアログを開きます。
    * [切り捨て] をクリックしてマイナス調整することもできます。  
6. [トランザクション日付] フィールドで、調整金額を転記する日付を入力します。
7. [切り上げ] フィールドに調整金額を入力します。
8. [OK] をクリックします。

## <a name="post-the-adjustment"></a>調整の転記
1. [固定資産] > [資産除去責務] > [固定資産仕訳帳] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
4. [保存] をクリックします。
5. [明細行] をクリックします。
6. [提案] をクリックします。
7. [除去費用の資産計上] をクリックします。
8. [終了日] フィールドで、日付を入力します。
9. [フィルター] をクリックします。
10. [基準] フィールドに値を入力します。
11. [OK] をクリックします。
12. [OK] をクリックします。
    * 調整が提案されていることを確認します。 提案された金額は現在の値に割引されます。  
13. [転記] をクリックします。


