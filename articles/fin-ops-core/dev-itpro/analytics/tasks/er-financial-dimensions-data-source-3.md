---
title: ER 財務分析コードをデータ ソースとして使用する (第 3 部 - レポートのデザイン)
description: 次の手順では、システム管理者に指定されたユーザーまたは電子レポート開発者のロールが、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a12f88f1e8b5e451bc8a5c5486d820da61bf3ad0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684790"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a>ER 財務分析コードをデータ ソースとして使用する (第 3 部 - レポートのデザイン)

[!include [banner](../../includes/banner.md)]

次の手順では、システム管理者に指定されたユーザーまたは電子レポート開発者のロールが、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。 これらの手順はどのタイプの企業でも実施できます。

この手順を実施するには、まず 「ER 財務分析コードをデータ ソースとして使用する（パート2：モデル マッピング）」に記載の手順を実施する必要があります。


## <a name="design-a-report-to-present-financial-dimensions"></a>財務分析コードを示すレポートを作成する
1. [組織管理] > [電子申告] > [コンフィギュレーション] に移動します。
2. [ツリー] フィールドで、「財務分析コード・サンプル モデル」を選択します。
3. [コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。
4. [新規] フィールドで、「財務分析コード・サンプルモデルに基づくフォーマット」を入力します。
    * 新しいレポートのデータ ソースとして事前に作成されたモデルを使用します。  
5. [名称] フィールドで、「Ledger journal report」を入力します。
6. [データモデル定義] フィールドで、「エントリ」を選択します。
7. [コンフィギュレーションの作成] をクリックします。
8. [デザイナー] をクリックします。
9. [ルートの追加] をクリックして、ドロップ ダイアログを開きます。
10. ツリーで、[XML\Element] を選択します。
11. [名称] のフィールドに、「Root」を入力します。
12. [OK] をクリックします。
13. [追加] をクリックしてドロップ ダイアログを開きます。
14. ツリーで、[XML\Attribute] を選択します。
15. [名前] フィールドに、「Company」と入力します。
16. [OK] をクリックします。
17. [追加] をクリックしてドロップ ダイアログを開きます。
18. ツリーで、[XML\Element] を選択します。
19. [名称] フィールドに、「仕訳」と入力します。
20. [OK] をクリックします。
21. ツリーで、「Root: XML Element\Journal: XML Element」を選択します。
22. [追加] をクリックしてドロップ ダイアログを開きます。
23. ツリーで、[XML\Attribute] を選択します。
24. [名称] フィールドに、「バッチ」と入力します。
25. [OK] をクリックします。
26. [追加] をクリックしてドロップ ダイアログを開きます。
27. ツリーで、[XML\Element] を選択します。
28. [名称] フィールドで、「トランザクション」と入力します。
29. [OK] をクリックします。
30. ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element」を選択します。
31. [追加] をクリックしてドロップ ダイアログを開きます。
32. ツリーで、[XML\Attribute] を選択します。
33. [名称] フィールドで、「伝票」と入力します。
34. [OK] をクリックします。
35. [属性を加える] をクリックします。
36. [名称] フィールドで、「日付」と入力します。
37. [OK] をクリックします。
38. [属性を加える] をクリックします。
39. [名前] フィールドで、「通貨」と入力します。
40. [OK] をクリックします。
41. [属性を加える] をクリックします。
42. [名称] フィールドに、「Dt」と入力します。
43. [OK] をクリックします。
44. [属性を加える] をクリックします。
45. [名称] フィールドに、「Ct」と入力します。
46. [OK] をクリックします。
47. [追加] をクリックしてドロップ ダイアログを開きます。
48. ツリーで、[XML\Element] を選択します。
49. [名称] フィールドに、「分析コード」を入力します。
50. [OK] をクリックします。
51. ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'」を選択します。
52. [追加] をクリックしてドロップ ダイアログを開きます。
53. ツリーで、[XML\Attribute] を選択します。
54. [名称] フィールドに、「コード」と入力します。
55. [OK] をクリックします。
56. [属性を加える] をクリックします。
57. [名称] フィールドに値を入力します。
58. [OK] をクリックします。
59. [属性を加える] をクリックします。
60. [名称] フィールドに説明を入力します。
61. [OK] をクリックします。
![ER Operations デザイナーのページ](../media/er-financial-dimensions-guides-format1.png)

## <a name="map-report-elements-to-data-sources"></a>レポートエレメントをデータソースにマッピングする
1. [マッピング] タブをクリックします。
2. ツリーで、「model: Data model Financial dimensions sample model」を展開します。
3. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list」を展開します。
4. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list」を展開します。
5. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list」を展開します。
6. ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute」を選択します。
7. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String」を展開します。
8. [バインド] をクリックします。
9. ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute」を選択します。
10. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record listt\Code: String」を選択します。
11. [バインド] をクリックします。
12. ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute」を選択します。
13. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String」を選択します。
14. [バインド] をクリックします。
15. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list」を展開します。
16. ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'」を選択します。
17. [バインド] をクリックします。
18. ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'」を選択します。
19. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real」を選択します。
20. [バインド] をクリックします。
21. ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'」を選択します。
22. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real」を選択します。
23. [バインド] をクリックします。
24. ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'」を選択します。
25. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String」を選択します。
26. [バインド] をクリックします。
27. ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'」を選択します。
28. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date」を選択します。
29. [バインド] をクリックします。
30. ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'」を選択します。
31. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String」を選択します。
32. [バインド] をクリックします。
33. ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element」を選択します。
34. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list」を選択します。
35. [バインド] をクリックします。
36. ツリーで、「Root: XML Element\Journal: XML Element\Batch: XML Attribute」を選択します。
37. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Batch: String」を選択します。
38. [バインド] をクリックします。
39. ツリーで、「Root: XML Element\Journal: XML Element」を選択します。
40. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list」を選択します。
41. [バインド] をクリックします。
42. ツリーで、「Root: XML Element\Company: XML Attribute」を選択します。
43. ツリーで、「model: Data model Financial dimensions sample model\Company: String」を選択します。
44. [バインド] をクリックします。
45. [保存] をクリックします。
46. ページを閉じます。
![ER Operations デザイナーのページ](../media/er-financial-dimensions-guides-format2.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]