---
title: 顧客の損金処理仕訳帳の作成
description: このタスク ガイドでは、損金処理のパラメータを設定し、[コレクション] ページ、[未処理の顧客請求書] ページおよび [顧客ページ] からトランザクションを損金処理する方法を表示します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd97f91f1ba53b56150b556fffdfed10a0c8911a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140240"
---
# <a name="create-a-write-off-journal-for-a-customer"></a>顧客の損金処理仕訳帳の作成

[!include [banner](../../includes/banner.md)]

このタスク ガイドでは、損金処理のパラメータを設定し、[コレクション] ページ、[未処理の顧客請求書] ページおよび [顧客ページ] からトランザクションを損金処理する方法を表示します。 このタスクでは、USMF というデモ会社を使用します。


## <a name="set-up-the-write-off-parameters"></a>損金処理パラメーターの設定
1. **ナビゲーション ウィンドウ > モジュール > クレジットおよびコレクション > 設定 > 売掛金勘定パラメーター**の順に移動します。
2. **回収**タブをクリックします。
3. **損金処理**セクションを展開または折りたたみます。
    - **損金処理仕訳**とは、作成する損金処理トランザクションを保持する一般仕訳帳のことです。  
    - 各損金処理に理由コードを添付できます。 損金処理時にこの既定値を上書きできます。  
    - 損金処理の元のトランザクションから売上税を分割する場合は、**売上税を分離する**をはいに設定します。  
4. ページを閉じます。
5. **貸方転記および取立 > 設定 > 顧客転記プロファイル**の順に移動します。 損金処理勘定は、一般仕訳帳で経費勘定として、または準備金の調整として使用されます。
6. ページを閉じます。

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>[指定の期間に達している残高] ページから顧客残高を損金処理します。
1. **与信および回収 > 回収 > 指定の期間に達している残高**の順に移動します。
2. 損金処理する顧客の行をマークします。 たとえば、Birch 会社の明細行をマークします。
3. **アクション ウィンドウ**で、**回収**をクリックします。
4. **損金処理**をクリックします。
5. **OK**をクリックします。
6. ページを閉じます。
7. **ナビゲーション ウィンドウ > モジュール > 総勘定元帳 > 仕訳入力 > 一般仕訳帳**の順に移動します。
8. 損金処理を含む仕訳帳の仕訳帳バッチ番号を選択します。 1 つの明細行は、顧客残高を取り消すために作成されます。 1 つ以上の明細行は、損金処理勘定に損金処理を転記するために作成されます。  
9. ページを閉じます。
10. ページを閉じます。

## <a name="write-off-transactions-from-the-collections-form"></a>回収フォームのトランザクションを損金処理します。
1. **与信および回収 > 回収 > 指定の期間に達している残高**の順に移動します。
2. 損金処理するトランザクションがある顧客の名前を選択します。 たとえば、「Cave Wholesales (US-004)」を選択します。
3. 最初のトランザクションの行をマークします。
4. 2 番目のトランザクションの行をマークします。
5. **損金処理**をクリックします。
6. **理由コメント** フィールドに '貸倒損失' を入力します。
7. **OK**をクリックします。
8. ページを閉じます。
9. ページを閉じます。
10. **総勘定元帳 > 仕訳入力 > 一般仕訳帳**の順に移動します。
11. 損金処理を含む仕訳帳の仕訳帳バッチ番号を選択します。 1 つの明細行は、顧客残高を取り消すために作成されます。 1 つ以上の明細行は、損金処理勘定に損金処理を転記するために作成されます。  
12. ページを閉じます。
13. ページを閉じます。

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>[未処理の顧客請求書] ページの請求書の損金処理
1. **ナビゲーション ウィンドウ > モジュール > 売掛金勘定 > 請求書 > 未処理の顧客請求書**の順に移動します。
2. 請求の明細行をマークします。 たとえば、「CIV-000667」の明細行をマークします。
3. **アクション ウィンドウ**で、**請求書**をクリックします。
4. **損金処理**をクリックします。
5. **OK**をクリックします。
6. ページを閉じます。

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>[顧客] ページの顧客残高の損金処理
1. **売掛金勘定 > 顧客 > すべての顧客**の順に移動します。
2. 顧客 ID を選択します。 たとえば、「US-001 (Contoso Retail San Diego)」を選択します。
3. **アクション ウィンドウ**で、**回収**をクリックします。
4. **損金処理**をクリックします。
5. **OK**をクリックします。
6. ページを閉じます。

