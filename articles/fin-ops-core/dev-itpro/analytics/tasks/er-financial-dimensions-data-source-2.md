---
title: ER 財務分析コードをデータ ソースとして使用する (第 2 部 - モデル マッピング)
description: このトピックでは、財務分析コードを ER レポートのデータ ソースとして使用するために、電子申告 (ER) モデルを構成する方法について説明します。 (第 2 部)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 02c730d08c411e736a7f8b9e7bad3d6a18cb8e6a
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093240"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a>ER 財務分析コードをデータ ソースとして使用する (第 2 部 - モデル マッピング)

[!include [banner](../../includes/banner.md)]

次の手順では、システム管理者に指定されたユーザーまたは電子レポート開発者のロールが、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。 これらの手順はどのタイプの企業でも実施できます。

これらの手順を実施するには、まず 「ER 財務分析コードをデータソースとして使用する （パート1：デザインデータ モデル）」に記載の手順を実施する必要があります。


## <a name="add-required-data-sources-to-model-mapping"></a>必要なデータ ソースをモデルマッピングに加える
1. [組織管理] > [電子申告] > [コンフィギュレーション] に移動します。
2. [ツリー] フィールドで、「財務分析コード・サンプル モデル」を選択します。
3. [デザイナー] をクリックします。
4. [モデルからデータ ソースへのマップ] をクリックします。
5. [新規] をクリックします。
6. [定義] フィールドで、「エントリ」を選択します。
7. [名称] フィールドで、「分析コードデータ・マッピング」と入力します。
8. [説明] フィールドで、「分析コードデータ・マッピング」と入力します。
9. [保存] をクリックします。
10. [デザイナー] をクリックします。
11. ツリーで、'Dynamics 365 for Operations\Table を選択します。
12. [ルートの追加] をクリックします。
13. [名前] フィールドに、「Company」と入力します。
14. [テーブル] フィールドに「CompanyInfo」と入力します。
15. [OK] をクリックします。
16. [ツリー] フィールドで、「財務分析コード・サンプル モデル」を選択します。
17. [ルートの追加] をクリックします。
    * このデータ ソースでは、データソースとしてそのモデルを使用するレポートについて財務分析コードをどのように定義するのか示します。  
18. [名前] フィールドに値を入力します。
19. 「分析コードのフィールドを要求する」で [はい] を選択します。
    * ユーザー ダイアログ フォームの実行時に分析コードを選択できるよう、「はい」を選択します。 「いいえ」を選択しますと、現インスタンスのすべての財務分析コードが既定値で使用されることになります。  
20. 「財務分析コードの選択」のフィールドで、「法人」を選択します。
    * ルックアップ フィールドの現インスタンスについて「分析コードを希望」を選択するには、「すべて」を選択します。  ルックアップ フィールドの会社について「分析コード」を選択するには、「法人」を選択します。  分析コードを選択して、ユーザーが単一の分析コードセットを使用して分析コードを選択できるようにします。  
21. 「主勘定のフィールドを要求する」で、[はい] を選択します。
    * 「主勘定を要求する」 を 「はい」 に設定することで、分析コードリストの一部として主勘定を選択できるようになります。   「いいえ」 に設定すると、主勘定は分析コードのリストに含まれなくなり、 「主勘定を必須にする」 オプションが有効になります。 「主勘定を必須にする」 オプションが 「はい」 に設定されると、ユーザーの選択にかかわらず主勘定が分析コードのリストに含まれます。  
22. [OK] をクリックします。
![ER モデル マッピング デザイナーのページ](../media/er-financial-dimensions-guides-model-mapping1.png)
23. ツリーで、'Dynamics 365 for Operations\Table records'を選択します。
24. [ルートの追加] をクリックします。
25. [名称] フィールドで、「LedgerJournal」と入力します。
26. [クエリの要求] フィールドで、[はい] を選択します。
27. [表] フィールドで、「LedgerJournalTable」と入力します。
28. [OK] をクリックします。
![ER モデル マッピング デザイナーのページ](../media/er-financial-dimensions-guides-model-mapping2.png)

## <a name="map-data-model-elements-to-added-data-sources"></a>データ モデル・エレメントを追加したデータソースにマッピングする
1. ツリーで、「Journal」を展開します。
2. ツリーで、「Journal\Transaction」を展開します。
3. ツリーで、「Journal\Transaction\Dimensions data」を展開します。
4. ツリーで、Dimensions setting」を展開します。
5. ツリーで、「LedgerJournal」を展開します。
6. ツリーで、「LedgerJournal\<Relations」を展開します。
7. ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans」を展開します。
8. ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Voucher」を選択します。
9. ツリーで、「Journal\Transaction\Voucher」を選択します。
10. [バインド] をクリックします。
11. ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)」を選択します。
    * たとえば、LedgerDimensionに設定されている財務分析コードについては、相当するデータソースの品目が使用できます（LedgerDimension.分析コード）。 このデータ ソースの品目は、レコードのリストとして設定された分析コードの財務分析コードを示します。  
12. つりーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)」を展開します。
13. ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions」を展開します。
14. ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value」を展開します。
15. ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition」を展開します。
16. ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name」を選択します。
17. ツリーで、「Journal\Transaction\Dimensions data\Name」を選択します。
18. [バインド] をクリックします。
19. ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description」を選択します。
20. ツリーで、「Journal\Transaction\Dimensions data\Description」を選択します。
21. [バインド] をクリックします。
22. ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code」を選択します。
23. ツリーで、「Journal\Transaction\Dimensions data\Code」を選択します。
24. [バインド] をクリックします。
25. ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions」を選択します。
26. ツリーで、「Journal\Transaction\Dimensions data」を選択します。
27. [バインド] をクリックします。
![ER モデル マッピング デザイナーのページ](../media/er-financial-dimensions-guides-model-mapping3.png)
28. ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)」を選択します。
29. ツリーで、「Journal\Transaction\Debit」を選択します。
30. [バインド] をクリックします。
31. ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)」を選択します。
32. ツリーで、「Journal\Transaction\Date」を選択します。
33. [バインド] をクリックします。
34. ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)」を選択します。
35. ツリーで、「Journal\Transaction\Currency」を選択します。
36. [バインド] をクリックします。
37. ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)」を選択します。
38. ツリーで、「Journal\Transaction\Credit」を選択します。
39. [バインド] をクリックします。
40. ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans」を選択します。
41. ツリーで、「Journal\Transaction」を選択します。
42. [バインド] をクリックします。
43. ツリーで、[LedgerJournal\Journal batch number(JournalNum)] を選択します。
44. ツリーで、「Journal\Batch」を選択します。
45. [バインド] をクリックします。
46. ツリーで、「LedgerJournal」を選択します。
47. ツリーで、「Journal」を選択します。
48. [バインド] をクリックします。
49. ツリーで、「Dimensions」を展開します。
50. ツリーで、「Dimensions\Main account and dimensions」を展開します。
51. ツリーで、「Dimensions\Main account and dimensions\Definition」を展開します。
52. ツリーで、「Dimensions\Main account and dimensions\Definition\Name」を選択します。
53. ツリーで、「Dimensions setting\Code」を選択します。
54. [バインド] をクリックします。
55. ツリーで、「Dimensions\Main account and dimensions\Definition\Report column name」を選択します。
56. ツリーで、「Dimensions setting\Name」を選択します。
57. [バインド] をクリックします。
58. ツリーで、「Dimensions\Main account and dimensions」を選択します。
59. ツリーで、「Dimensions setting」を選択します。
60. [バインド] をクリックします。
61. ツリーで、「Company」を選択します。
62. [編集] をクリックします。
63. expressionAsStringTextのフィールドで、Company.'find()'.'name()を入力します。
    * 会社.'検索()'.'名称()'  
64. [保存] をクリックします。
![ER モデル マッピング デザイナーのページ](../media/er-financial-dimensions-guides-model-mapping4.png)
65. ページを閉じます。
66. [保存] をクリックします。
67. ページを閉じます。

## <a name="complete-this-draft-models-version"></a>このドラフト モデルのバージョンを実行します。
1. ページを閉じます。
2. ページを閉じます。
3. [状態の変更] をクリックします。
4. [完了] をクリックします。
5. [OK] をクリックします。
![ER モデル マッピング デザイナーのページ](../media/er-financial-dimensions-guides-model-mapping5.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]