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
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e17093ac1334b023f6d7a3fde55d44d24b148590
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144147"
---
# <a name="propose-and-post-the-impairment-amount-by-using-fixed-asset-journal"></a>固定資産仕訳帳を使用した減損損失の提案と転記

[!include [banner](../../includes/banner.md)]

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

