---
title: "顧客への払戻し"
description: "この記事では、顧客グループの払い戻しトランザクションを作成する方法を説明します。 顧客に貸方残高がある場合、顧客に残高金額を払い戻すことができます。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: Shiva.Pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c3201166eb7054205647a54ed80f98968fcfda6e
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017

---

# <a name="reimburse-customers"></a>顧客への払戻し

[!include[banner](../includes/banner.md)]


この記事では、顧客グループの払い戻しトランザクションを作成する方法を説明します。 顧客に貸方残高がある場合、顧客に残高金額を払い戻すことができます。 

次の表に、開始する前に準備が整っている必要のある前提条件を示します。

| 前提条件                                                            | 説明                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 法人の最低払い戻し金額を指定します。          | [**売掛金勘定パラメータ**] ページで、[**一般**] エリアの [**最低払い戻し金額**] フィールドに、顧客の超過支払の場合に払い戻すことができる最低金額を入力します。 |
| オプション: 払い戻しを受けることができる各顧客に仕入先勘定を追加します。 | [**顧客**] のページの [**その他の詳細**] クイック タブの [**仕入先**] フィールドで、顧客の仕入先勘定を選択します。                                           |

払い戻しトランザクションを作成するとき、仕入先請求書が貸方残高金額に対して作成されます。 払い戻し処理により、顧客口座の貸付残高が削除され、顧客に対応する仕入先の差引請求額が作成されます。

1.  売掛金勘定では、**払い戻し**プロセスを実行します。
2.  次の手順のいずれかを実行します。
    -   特定の顧客勘定を払い戻すには、[**選択**] をクリックし、クエリで顧客勘定を指定します。
    -   すべての顧客勘定を払い戻すには、[**OK**] をクリックします。

    貸方金額が顧客の仕入先勘定に転送され、通常の支払として処理されます。 顧客が仕入先勘定を持たない場合、その顧客の一時仕入先勘定が自動的に作成されます。
3.  作成された払い戻しトランザクションを表示するには、[**払い戻し**] ページを使用します。
4.  買掛金勘定で、払い戻しプロセスの結果として作成された仕入先請求書に対する支払を作成します。





