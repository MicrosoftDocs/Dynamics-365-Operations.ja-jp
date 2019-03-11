---
title: ER モデル マッピングの定義およびそのデータ ソースの選択
description: 次の手順では、システム管理者または電子申告開発者ロールのユーザーがどのように電子申告データ モデルのデータ ソースを選択できるか説明します。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5f2f2c699514d723f42f5d1fb25724f46dfc4f4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "348874"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a>ER モデル マッピングの定義およびそのデータ ソースの選択

[!include [task guide banner](../../includes/task-guide-banner.md)]

次の手順では、システム管理者または電子申告開発者ロールのユーザーがどのように電子申告 (ER) データ モデルのデータ ソースを選択できるか説明します。 データ ソースは、設計時には選択したデータ モデルの個々のコンポーネントにバインドされ、実行時には業務データがそのデータ モデルに設定されます。 この例では、サンプル会社 Litware、Inc. に対して作成された既存のデータ モデルのデータ ソースを選択します。これらの手順を完了するには、最初に「新しいデータ モデルの作成」手順でステップを完了する必要があります。


## <a name="open-the-electronic-reporting-configurations-tree"></a>電子申告コンフィギュレーション ツリーを開きます
1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。
2. [コンフィギュレーションをレポートする] をクリックします。

## <a name="insert-a-new-model-mapping"></a>新しいモデル マッピングの挿入
1. ツリーで、「支払 (単純化モデル)」を選択します。
2. [デザイナー] をクリックします。
3. [モデルからデータ ソースへのマップ] をクリックします。
4. [新規] をクリックします。
    * これにより、データ ソースにデータ モデルをマップする新しいレコードが作成されます。 この例では、目的の支払タイプ「口座振替」のために、データ ソースにデータ モデルをマップします。     特定のデータ モデルに複数のマッピングを設計することができます。 たとえば、口座引落や口座振替などの異なる支払タイプのマッピングを作成できます。 この例では、口座振替のマッピングを作成します。  
5. [名前] フィールドで、「CT マッピング」と入力します。
    * CT マッピング  
6. [説明] フィールドに、「支払モデル マッピング CT」と入力します。
    * 支払モデル マッピング CT  
7. [定義] フィールドに、「CustomerCreditTransferInitiation」を入力します。
    * CustomerCreditTransferInitiation  
8. [定義の変更] を解決します。
9. [保存] をクリックします。

## <a name="define-required-data-sources-for-the-current-model-mapping"></a>現在のモデル マッピングに必要なデータ ソースの定義
1. [デザイナー] をクリックします。
2. ツリーで、'Dynamics 365 for Operations\Table records'を選択します。
3. [ルートの追加] をクリックします。
    * 支払トランザクションにアクセスするために、このデータ ソースを入力します。  
4. [名前] フィールドで、「Transactions」と入力します。
    * トランザクション  
5. [ラベル] フィールドに「Transactions」と入力します。
    * トランザクション  
6. [ヘルプ] フィールドに、「Ledger journal lines」と入力します。
    * 仕訳元帳明細行  
7. [クエリの要求] フィールドで、[はい] を選択します。
    * [はい] を選択します。  
8. [テーブル] フィールドで、「LedgerJournalTrans」と入力します。
    * LedgerJournalTrans  
9. [OK] をクリックします。
    * 現在のデータ モデルのデータ ソースとして、LedgerJournalTrans テーブルを選択します。  
10. ツリーで、[Functions\Calculated field] を選択します。
11. [追加] をクリックします。
    * [追加] をクリックして、新しい計算済フィールドを追加します。  
12. [名前] フィールドに、「$EndToEndID」と入力します。
    * $EndToEndID  
13. [式の編集] をクリックします。
14. ツリーで、[String\CONCATENATE] を選択します。
15. [機能の追加] をクリックします。
16. ツリーで、[Transactions] を展開します。
17. ツリーで、[Transactions\Voucher] を選択します。
18. [データ ソースの追加] をクリックします。
19. [フォーミュラ] フィールドに、「CONCATENATE(Transactions.Voucher, "-",」を入力します。
    * フォーミュラの最後に、「, “-“,」を入力します。  
20. ツリーで、[String\TEXT] を選択します。
21. [機能の追加] をクリックします。
22. ツリーで、[Transactions\Record-ID(RecId)] を選択します。
23. [データ ソースの追加] をクリックします。
24. [フォーミュラ] フィールドに、「CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))」を入力します。
    * フォーミュラの最後に、「))」を入力します。  
25. [保存] をクリックします。
    * 作成したフォーミュラでエラーが検出されていないことを確認します。 フォーミュラ エディタ コントロールの下にある [エラー] タブを参照してください。  
26. ページを閉じます。
27. [OK] をクリックします。
    * このデータ ソースに計算済フィールドを追加します。  
28. [追加] をクリックします。
    * [追加] をクリックして、新しい計算済フィールドを追加します。  
29. [名前] フィールドに、「$Amount」と入力します。
    * $金額  
30. [式の編集] をクリックします。
31. ツリーで、[Transactions] を展開します。
32. ツリーで、[Transactions\Debit(AmountCurDebit)] を選択します。
33. [データ ソースの追加] をクリックします。
34. [フォーミュラ] フィールドに、「Transactions.AmountCurDebit - 」を入力します。
    * フォーミュラの最後に、「-」を入力します。  
35. ツリーで、[Transactions\Credit(AmountCurCredit)] を選択します。
36. [データ ソースの追加] をクリックします。
37. [保存] をクリックします。
38. ページを閉じます。
39. [OK] をクリックします。
    * これにより、現在のデータ モデルの選択したデータ ソースに [$Amount] 計算済フィールドが追加されます。  
40. ツリーで、[Transactions\$Amount] を選択します。
41. ツリーで、[Transactions] を展開します。
42. ツリーで、[Transactions\$Amount] を展開するかまた折りたたみます。
43. ツリーで、「Transactions」を展開または折りたたみます。
44. ツリーで、'Dynamics 365 for Operations\Table records'を選択します。
45. [ルートの追加] をクリックします。
    * このデータ ソースを入力して、会社の銀行口座情報にアクセスします。  
46. [名前] フィールドに、「BankAccount」と入力します。
    * BankAccount  
47. [ラベル] フィールドに「Bank Account」と入力します。
    * 銀行口座  
48. [ヘルプ] フィールドに「Bank Account」と入力します。
    * 銀行口座  
49. [クエリの要求] フィールドで、[はい] を選択します。
    * [はい] を選択します。  
50. [テーブル] フィールドに「BankAccountTable」と入力します。
    * BankAccountTable  
51. [OK] をクリックします。
    * 現在のデータ モデルのデータ ソースとして、BankAccountTable テーブルを選択します。  
52. [ルートの追加] をクリックします。
    * このデータ ソースを入力して、会社の必要条件にアクセスします。  
53. [名前] フィールドに、「Company」と入力します。
    * 法人  
54. [ラベル] フィールドに値を入力します。
    * 会社情報  
55. [ヘルプ] フィールドに、「Company information」と入力します。
    * 会社情報  
56. [クエリの要求] フィールドで、[はい] を選択します。
    * [はい] を選択します。  
57. [テーブル] フィールドに「CompanyInfo」と入力します。
    * CompanyInfo  
58. [OK] をクリックします。
    * 現在のデータ モデルのデータ ソースとして、CompanyInfo テーブルを選択します。  
59. ツリーで、[Functions\Calculated field] を選択します。
60. [ルートの追加] をクリックします。
    * 新しいデータ ソースとして計算済フィールドを挿入します。  
61. [名前] フィールドに、「ProcessingDateTime」と入力します。
    * ProcessingDateTime  
62. [ラベル] フィールドに、「処理日時」と入力します。
    * 処理日時  
63. [式の編集] をクリックします。
64. ツリーで、「Date/time\SESSIONNOW」を選択します。
65. [機能の追加] をクリックします。
66. [保存] をクリックします。
67. ページを閉じます。
68. [OK] をクリックします。
    * 現在のデータ モデルのデータ ソースとして、[ProcessingDateTime] 計算済フィールドを追加します。  
69. [保存] をクリックします。
70. ページを閉じます。
71. ページを閉じます。
72. ページを閉じます。

