---
title: 顧客の口座引落の委任状の作成
description: このタスク ガイドでは、口座引落の委任状を作成し、それを請求書に使用する方法を示します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 86d29782f616219b5d84e3567910cb28c60b65ae
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140309"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>顧客の口座引落の委任状の作成

[!include [banner](../../includes/banner.md)]

このタスク ガイドでは、口座引落の委任状を作成し、それを請求書に使用する方法を示します。


## <a name="create-a-bank-account"></a>銀行口座の作成
1. **ナビゲーション ウィンドウ**で、**モジュール > 売掛金勘定 > 顧客 > すべての顧客**の順に移動します。
2. 一覧で、レコードを選択します。 たとえば、「US-001」を選択します。
3. アクション ウィンドウで、**顧客**をクリックします。
4. **銀行口座**をクリックします。
5. **新規** をクリックします。
6. **銀行口座**フィールドに、値を入力します。
7. **名前**フィールドに値を入力します。
8. **IBAN** フィールドに値を入力します。
9. **通貨**フィールドに値を入力します。
10. **保存**をクリックします。
11. ページを閉じます。
12. **ナビゲーション ウィンドウ**で、**モジュール > 現金および銀行管理 > 銀行口座 > 銀行口座**の順に移動します。
13. 一覧で、目的のレコードを見つけ、選択します。
14. 一覧で、選択された行のリンクをクリックします。
15. **編集** をクリックします。
16. **追加 ID** クイック タブを展開します。
17. **口座引落 ID** フィールドに値を入力します。
18. **IBAN** フィールドに値を入力します。
19. ページを閉じます。
20. ページを閉じます。

## <a name="define-the-electronic-payment-method"></a>電子的支払方法の定義
1. **ナビゲーション ウィンドウ**で、**モジュール > 売掛金勘定 > 支払設定 > 支払方法**の順に移動します。
2. **新規** をクリックします。
3. **支払方法**フィールドに値を入力します。
4. **説明**フィールドで、値を入力します。
5. **支払タイプ** フィールドで、'電子支払' を入力します。 口座引落委任状の支払タイプは、電子支払でなければなりません。
6. **委任状の要求**フィールドで、はいを選択します。
7. ページを閉じます。

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>口座引落の委任状を顧客に追加します。
1. **ナビゲーション ウィンドウ**で、**モジュール > 売掛金勘定 > 顧客 > すべての顧客**の順に移動します。
2. 一覧で、レコードを選択します。 たとえば、「US-001」を選択します。
3. **編集** をクリックします。
4. **支払の既定値**クイック タブを展開します。
5. **支払方法**フィールドで値を入力または選択します。
6. **支払の既定値**クイック タブを展開します。
7. **口座引落委任状**クイック タブを展開します。
8. **追加**をクリックします。
9. **銀行口座**フィールドで、値を入力または選択します。
10. **債権者の銀行口座**フィールドで、値を入力または選択します。
11. **支払頻度**フィールドで、この委任状用に処理を予定している支払回数を入力します。
12. **OK**をクリックします。
13. **印刷** をクリックします。
14. **委任状レポート**をクリックします。
15. ページを閉じます。
16. **編集** をクリックします。
17. **署名日**フィールドに日付を入力します。
18. **はい** をクリックします。
19. 委任状に署名した場所を入力します。
20. **OK**をクリックします。
21. ページを閉じます。

## <a name="create-a-free-text-invoice-with-mandate"></a>委任状と自由書式の請求書の作成
1. **ナビゲーション ウィンドウ**で、**モジュール > 売掛金勘定 > 請求書 > すべての自由書式の請求書**の順に移動します。
2. **新規** をクリックします。
3. 委任状を追加した顧客を選択します。
4. **口座引落の委任状 ID** フィールドで、値を入力または選択します。

