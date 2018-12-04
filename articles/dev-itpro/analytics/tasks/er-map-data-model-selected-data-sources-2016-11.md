--- 
title: "ER データ モデルを選択したデータ ソースにマップする"
description: "次のステップでは、「システム管理者」または「電子申告開発者」ロールのユーザーが、選択した Dynamics 365 for Finance and Operations, Enterprise Edition データ ソースに電子申告 (ER) データ モデルをマップする方法を説明します。"
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 249bf3f3806ed43eccf39086bdf9697a3e879c27
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---
# <a name="er-map-data-model-to-selected-data-sources"></a>ER データ モデルを選択したデータ ソースにマップする

[!include [task guide banner](../../includes/task-guide-banner.md)]

次のステップでは、「システム管理者」または「電子申告開発者」ロールのユーザーが、選択した Dynamics 365 for Finance and Operations, Enterprise Edition データ ソースに電子申告 (ER) データ モデルをマップする方法を説明します。 このマッピング モデルは、電子支払ドキュメントを管理するために使用するコンフィギュレーションの書式設定で、データ ソースとして後で使用されます。 この例では、サンプル会社 Litware、Inc. のデータ モデルをデータ ソースにマップします。 これらの手順を完了するには、最初に「モデル マッピングのためのデータ ソースの選択」の手順でステップを完了する必要があります。


## <a name="open-er-configurations-tree"></a>ER コンフィギュレーション ツリーを開く
1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。
2. [コンフィギュレーション] をクリックします。

## <a name="select-created-model-mapping"></a>作成したモデル マッピングの選択
1. ツリーで、「支払 (単純化モデル)」を選択します。
    * モデル コンフィギュレーション「支払 (単純化モデル)」が事前に作成されていることを確認します。 そうでない場合は、今すぐ停止し、タスク ガイド「選択したドメインのデータ モデルに対する新しいコンフィギュレーションの作成」の完了後に戻ります。  
2. [モデル デザイナー] をクリックします。
3. [モデルからデータ ソースへのマップ] をクリックします。
4. 「CT mapping」のレコードを選択します。
    * CT マッピング  

## <a name="bind-created-data-sources-to-data-model-elements"></a>データ モデルの要素のために作成したデータ ソースのバインド
1. [デザイナー] をクリックします。
2. ツリーで、[処理日時 (ProcessingDateTime)] を選択します。
3. ツリーで、[Processing date(ProcessingDateTime)] を選択します。
4. [バインド] をクリックします。
5. ツリーで、[Payment message identification(MessageIdentification)] を選択します。
6. ツリーで、[Transactions] を展開します。
7. ツリーで、[Transactions\Journal batch number(JournalNum)] を選択します。
8. [バインド] をクリックします。
9. ツリーで、[Payments] を選択します。
10. ツリーで、[Transactions] を選択します。
11. [バインド] をクリックします。
12. ツリーで、[Payments= Transactions] を展開します。
13. ツリーで、[Payments= Transactions\Creditor] を展開します。
14. ツリーで、[Payments= Transactions\Creditor\Account] を展開します。
15. ツリーで、[Payments= Transactions\Creditor\Account\Currency code(Currency)] を選択します。
16. ツリーで、[Transactions\vendBankAccountInTransactionCompany()] を展開します。
17. ツリーで、[Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)] を選択します。
18. [バインド] をクリックします。
19. ツリーで、[Payments= Transactions\Creditor\Account\IBAN code(IBAN)] を選択します。
20. ツリーで、[Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)] を展開します。
21. [バインド] をクリックします。
22. ツリーで、[Payments= Transactions\Creditor\Account\Number] を選択します。
23. ツリーで、[Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)] を展開します。
24. [バインド] をクリックします。
25. ツリーで、[Payments= Transactions\Creditor\Agent] を展開します。
26. ツリーで、[Payments= Transactions\Creditor\Agent\Name] を選択します。
27. ツリーで、[Transactions\vendBankAccountInTransactionCompany()\Name] を展開します。
28. [バインド] をクリックします。
29. ツリーで、[Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)] を選択します。
30. ツリーで、[Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)] を展開します。
31. [バインド] をクリックします。
32. ツリーで、[Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)] を選択します。
33. ツリーで、[Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)] を選択します。
34. [バインド] をクリックします。
35. ツリーで、[Payments= Transactions\Creditor\Name] を選択します。
36. ツリーで、[Transactions\findVendTable()] を展開します。
37. ツリーで、[Transactions\findVendTable()\name()] を選択します。
38. [バインド] をクリックします。
39. ツリーで、[Payments= Transactions\Currency code(Currency)] を選択します。
40. ツリーで、[Transactions\>Relations] を展開します。
41. ツリーで、[Transactions\>Relations\Currency table(Currency)] を展開します。
42. ツリーで、[Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)] を選択します。
43. [バインド] をクリックします。
44. ツリーで、[Payments= Transactions\Debtor] を展開します。
45. ツリーで、[Payments= Transactions\Debtor\Account] を展開します。
46. ツリーで、[Payments= Transactions\Debtor\Account\Currency code(Currency)] を選択します。
47. ツリーで、[Bank Account(BankAccount)] を選択します。
48. ツリーで、[Bank Account(BankAccount)] を展開します。
49. ツリーで、[Bank Account(BankAccount)\Currency(CurrencyCode)] を選択します。
50. [バインド] をクリックします。
51. ツリーで、[Bank Account(BankAccount)\IBAN] を選択します。
52. ツリーで、[Payments= Transactions\Debtor\Account\IBAN code(IBAN)] を選択します。
53. [バインド] をクリックします。
54. ツリーで、[Payments= Transactions\Debtor\Account\Number] を選択します。
55. ツリーで、[Bank Account(BankAccount)\Bank account number(AccountNum)] を選択します。
56. [バインド] をクリックします。
57. ツリーで、[Payments= Transactions\Debtor\Agent] を展開します。
58. ツリーで、[Payments= Transactions\Debtor\Agent\Name] を選択します。
59. ツリーで、[Bank Account(BankAccount)\Name] を選択します。
60. [バインド] をクリックします。
61. ツリーで、[Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)] を選択します。
62. ツリーで、[Bank Account(BankAccount)\Routing number(RegistrationNum)] を選択します。
63. [バインド] をクリックします。
64. ツリーで、[Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)] を選択します。
65. ツリーで、[Bank Account(BankAccount)\SWIFT code(SWIFTNo)] を選択します。
66. [バインド] をクリックします。
67. ツリーで、[Payments= Transactions\Debtor\Name] を選択します。
68. ツリーで、[Company information(Company)] を選択します。
69. ツリーで、[Company information(Company)] を展開します。
70. ツリーで、[Company information(Company)\Name] を選択します。
71. [バインド] をクリックします。
72. ツリーで、[Payments= Transactions\Description] を選択します。
73. ツリーで、[Transactions\Description(Txt)] を選択します。
74. [バインド] をクリックします。
75. ツリーで、[Payments= Transactions\End to end identification code(End2EndID)] を選択します。
76. ツリーで、[Transactions\$EndToEndID] を選択します。
77. [バインド] をクリックします。
78. ツリーで、[Payments= Transactions\Instructed amount(InstructedAmount)] を選択します。
79. ツリーで、[Transactions\$Amount] を選択します。
80. [バインド] をクリックします。
81. ツリーで、[Payments= Transactions\Transaction date(TransactionDate)] を選択します。
82. ツリーで、[Transactions\Date(TransDate)] を選択します。
83. [バインド] をクリックします。

## <a name="validate-created-mapping"></a>作成したマップの検証
1. [検証] をクリックします。
    * 新しいマッピングを検証し、すべてのバインディングが要件を満たしていることを確認します。  
2. [エラー リスト] セクションを展開または折りたたむには、矢印をクリックします。
3. [保存] をクリックします。
4. ページを閉じます。
5. ページを閉じます。
6. ページを閉じます。

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a>モデル コンフィギュレーションの現在のバージョンのステータスの変更
1. [状態の変更] をクリックします。
    * 支払形式の設計に使用できるように、指定のモデルのコンフィギュレーションの状態を [ドラフト] から [完了] に変更します。  
2. [完了] をクリックします。
    * [完了] を選択します。  
3. [説明] フィールドに値を入力します。
    * 例えば、「バージョン 1」。  
4. [OK] をクリックします。
5. 現在のコンフィギュレーションの完了したバージョンを選択します。
    * 作成したコンフィギュレーションが完了したバージョン 1 として保存されることに注意してください。  


