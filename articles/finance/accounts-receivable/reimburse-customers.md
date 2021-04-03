---
title: 顧客への払戻し
description: この記事では、顧客グループの払い戻しトランザクションを作成する方法を説明します。 顧客に貸方残高がある場合、顧客に残高金額を払い戻すことができます。
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca087b5a39432eec6b2711cc4c4decf23932b611
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251124"
---
# <a name="reimburse-customers"></a>顧客への払戻し

[!include [banner](../includes/banner.md)]

この記事では、顧客グループの払い戻しトランザクションを作成する方法を説明します。 顧客に貸方残高がある場合、顧客に残高金額を払い戻すことができます。 

次の表に、開始する前に準備が整っている必要のある前提条件を示します。

| 前提条件                                                            | 説明 |
|-------------------------------------------------------------------------|-------------|
| 法人の最低払い戻し金額を指定します。          | **売掛金勘定パラメータ** ページで、**一般** エリアの **最低払い戻し金額** フィールドに、顧客の超過支払の場合に払い戻すことができる最低金額を入力します。 |
| オプション: 払い戻しを受けることができる各顧客に仕入先勘定を追加します。 | **顧客** のページの **その他の詳細** クイック タブの **仕入先** フィールドで、顧客の仕入先勘定を選択します。 |

払い戻しトランザクションを作成するとき、仕入先請求書が貸方残高金額に対して作成されます。 払い戻し処理により、顧客口座の貸付残高が削除され、顧客に対応する仕入先の差引請求額が作成されます。

1. 売掛金勘定で、**払い戻し** プロセス (**売掛金勘定 \>定期処理タスク \> 払い戻し**) を実行します。
2. 元帳分析コードに関係なくすべてのトランザクションをグループ化するには、**顧客の集計** オプションを **はい** に設定します。 類似した元帳分析コードが設定されているトランザクションのみをグループ化するには、オプションを **いいえ** に設定します。
3. **未処理の借方トランザクションのある顧客を含める** を選択して、未決済の借方金額のある顧客を選択します。
4. 特定の顧客勘定を払い戻すには、**含めるレコード** クイックタブで、**フィルター** を選択してからクエリで顧客勘定を指定します。

    貸方金額が顧客の仕入先勘定に転送され、通常の支払として処理されます。 顧客が仕入先勘定を持たない場合、その顧客の一時仕入先勘定が自動的に作成されます。

5. 作成された払い戻しトランザクションを表示するには、**払い戻し** レポート (**売掛金勘定 \> 照会およびレポート \> 払い戻しレポート**) を使用します。
6. 買掛金勘定で、払い戻しプロセスの結果として作成された仕入先請求書に対する支払を作成します。 仕入先への支払方法の詳細については、[仕入先への支払に関する概要](../accounts-payable/Vendor-payments-workspace.md) を参照してください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]