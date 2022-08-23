---
title: 固定資産仕訳帳を使用した減損損失の提案と転記
description: この手順を用いて、固定資産仕訳帳を使用して減損金額を提示および転記する方法を把握します。
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
ms.openlocfilehash: 9fad44ce14ad8ad5aebec9894783c47b8044a96d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270541"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
