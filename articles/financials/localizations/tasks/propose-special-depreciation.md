--- 
title: "特別償却の提案"
description: "日本では、特定の条件下で特別償却が許可されます。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d8929755858ce3a531a367ea18869cdc3761382b
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---
# <a name="propose-special-depreciation"></a>特別償却の提案

[!include [task guide banner](../../includes/task-guide-banner.md)]

日本では、特定の条件下で特別償却が許可されます。 引当メソッドの場合、このタスクには 2 つのステップがあります。準備金の転記と準備金配賦の転記です。 ディレクト オフ メソッドの場合、必要なステップは 1 つです。これは準備金の転記と同じ手順です。 



この手順では、引当メソッドによる特別償却の提案方法を説明します。

この手順を実行する前に固定資産が取得済であることを確認します。 また、[固定資産コンフィギュレーション キー] が選択されていることを確認します。



この手順では、JPMF デモ会社のデータを使用します。


## <a name="post-reserve"></a>準備金の転記
1. [固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
4. [保存] をクリックします。
5. [明細行] をクリックします。
6. [提案] をクリックします。
7. [特別償却提案] クリックします。
8. [終了日] フィールドで、日付を入力します。
9. [フィルター] をクリックします。
10. [基準] フィールドに値を入力します。
11. [OK] をクリックします。
12. [OK] をクリックします。
13. [転記] をクリックします。

## <a name="post-reserve-allocation"></a>準備金配賦の転記
1. [固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
4. [保存] をクリックします。
5. [明細行] をクリックします。
6. [提案] をクリックします。
7. [特別償却提案] クリックします。
8. [終了日] フィールドで、日付を入力します。
    * [準備金配賦開始日] は、[取崩開始] によって異なります。  
9. [フィルター] をクリックします。
10. [基準] フィールドに値を入力します。
11. [OK] をクリックします。
12. [OK] をクリックします。
13. [転記] をクリックします。


