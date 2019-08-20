---
title: 増加償却の提案と転記
description: 日本の場合、確認済加速償却ドキュメントのデータに基づいて加速償却を提案することができます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset, AssetAcceleratedDepDocument_JP
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05f3a6175332125a8f9f60dafae41c945fe0b7e1
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848763"
---
# <a name="propose-and-post-accelerated-depreciation"></a>増加償却の提案と転記

[!include [task guide banner](../../includes/task-guide-banner.md)]

日本の場合、確認済加速償却ドキュメントのデータに基づいて加速償却を提案することができます。 注記: 加速償却の提案は通常の減価償却を提案しません。 この手順では、通常の減価償却の転記後に完了する必要があります。



この手順は確認済加速減価償却ドキュメントに基づく加速償却の提案および転記について説明します。 



この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



この手順は、デモ データ会社 JPMF を使用して作成されました。

1. [固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
4. [保存] をクリックします。
5. [明細行] をクリックします。
6. [提案] をクリックします。
7. [加速償却提案] をクリックします。
8. [終了日] フィールドで、日付を入力します。
    * 既定では、すべての確認済加速償却を提案するよう基準がコンフィギュレーションされています。 ある特定のドキュメントの提案など、その他のニーズがある場合は変更できます。  
9. [OK] をクリックします。
    * 加速償却が提案されたことを確認します。  
    * 注記: 通常の減価償却は取り扱わないため、提案および転記にはユーザーによる操作が必要です。  
10. [転記] をクリックします。
11. ページを閉じます。
12. [固定資産] > [定期処理タスク] > [加速償却] > [加速償却ドキュメント] の順に移動します。
    * 転記済ドキュメントのステータスが更新されていることを確認します。  

