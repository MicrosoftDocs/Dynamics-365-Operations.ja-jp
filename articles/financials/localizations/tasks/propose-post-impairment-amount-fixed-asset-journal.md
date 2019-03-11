---
title: 固定資産仕訳帳を使用した減損損失の提案と転記
description: この手順を用いて、固定資産仕訳帳を使用して減損金額を提示および転記する方法を把握します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b7353519782e62d57d66d9ba36a2f6a2b33a7c9c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "371038"
---
# <a name="propose-and-post-the-impairment-amount-by-using-fixed-asset-journal"></a>固定資産仕訳帳を使用した減損損失の提案と転記

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順を用いて、固定資産仕訳帳を使用して減損金額を提示および転記する方法を把握します。



このタスクを実行する前に、減損テスト結果がすでに作成されている必要があります。



この手順は、デモ データ会社 JPMF を使用して作成されました。

1. [固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、目的のレコードを見つけ、選択します。
5. [明細行] をクリックします。
6. [提案] をクリックします。
7. [減損提案] をクリックします。
8. [減損テスト ID] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
9. 一覧で、選択された行のリンクをクリックします。
    * この例では、「JPMF-000004」を選択します。  
10. [OK] をクリックします。
    * 減損テストの 2 つの固定資産は、次の情報と共に提案されます: 固定資産番号、貸方の減損金額、および減損テストの日付として日付。  
11. [転記] をクリックします。

