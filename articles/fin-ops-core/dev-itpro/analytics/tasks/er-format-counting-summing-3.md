---
title: ER 棚卸および集計を行うための形式のコンフィギュレーション (第 3 部 - 出力を作成するための計算の使用)
description: この記事では、既に生成されたテキスト出力のデータに基づいて棚卸および集計を行うために電子レポート形式を構成する方法について説明します。 (第 3 部)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
ms.openlocfilehash: 818c48f8c9ac874a36c741e59061d79fb34995ce
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290637"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a>ER 棚卸および集計を行うための形式のコンフィギュレーション (第 3 部 - 出力を作成するための計算の使用)

[!include [banner](../../includes/banner.md)]

次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。 これらの手順はどのタイプの企業でも実施できます。

これらの手順を完了するには、まず 「計算と集計を行うER設定フォーマット（パート2：計算の環境設定）」に記載の手順を完了する必要があります。

この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。


## <a name="configure-this-report-to-use-counting-and-summing-info"></a>計算と集計の情報を使用するには、このレポートを設定します。
1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。
2. [コンフィギュレーションをレポートする] をクリックします。
3. ツリーで、「Intrastat model」を展開します。
4. ツリーで、「Intrastat model\Intrastat (DE)」を選択します。
5. ツリーで、「Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'」を選択します。
6. [デザイナー] をクリックします。
7. [マッピング] タブをクリックします。
8. [ルートの追加] をクリックして、ドロップ ダイアログを開きます。
    * 新規データソースを加えて、記憶されたブロックのリストを取得します。  
9. ツリーで、[Functions\Calculated field] を選択します。
10. [名称] フィールドに、「$BlocksList」を入力します。
    * $BlocksList  
11. [式の編集] をクリックします。
12. ツリーで、「Data collection functions\COLLECTEDLIST」を選択します。
13. [機能の追加] をクリックします。
14. [データ ソースの追加] をクリックします。
15. [式] フィールドに、「COLLECTEDLIST('$BlockName', '」を入力します。
    * COLLECTEDLIST('$BlockName',  
16. [式] フィールドに、「COLLECTEDLIST('$BlockName', "*")」を入力します。
    * COLLECTEDLIST('$BlockName', "*")  
17. [保存] をクリックします。
    * パターン 「*」 は、すべてのブロックがこの記録のリストに含まれることを意味します。  
18. ページを閉じます。
19. [OK] をクリックします。
20. [フォーマット] タブをクリックします。
21. ツリーで、「Intrastat\Data」を選択します。
22. [追加] をクリックしてドロップ ダイアログを開きます。
23. ツリーで、「Text\Sequence」を選択します。
24. [名称] フィールドに、「Totals by blocks」を入力します。
    * ブロック別の合計  
25. [特殊文字] フィールドでは、「New line - Windows (CR LF)」を選択します。
26. [OK] をクリックします。
27. ツリーで、「Intrastat\Data\Totals by blocks」を選択します。
28. [追加] をクリックしてドロップ ダイアログを開きます。
29. ツリーで、[Text\String] を選択します。
30. [名称] フィールドで、「ブロックコード」と入力します。
    * ブロック コード  
31. [OK] をクリックします。
32. [ストリングの追加] をクリックします。
33. [名称] フィールドに、「Lines counting」と入力します。
    * 計算の明細行  
34. [OK] をクリックします。
35. [ストリングの追加] をクリックします。
36. [名前] フィールドに、「Total amount」を入力します。
    * 合計時間  
37. [OK] をクリックします。
38. [マッピング] タブをクリックします。
39. ツリーで、「$BlocksList」を選択します。
40. [バインド] をクリックします。
    * 記憶された各ブロックの集計行を作成します。  
41. [フォーマット] タブをクリックします。
42. ツリーで、「Intrastat\Data\Totals by blocks\Block code」を選択します。
43. [マッピング] タブをクリックします。
44. [式の編集] をクリックします。
45. [式] フィールドに、「"Block id: " & 」を入力します。
    * "ブロック id: " &  
46. ツリーで、「$BlocksList」を展開します。
47. ツリーで、「$BlocksList\Value」を選択します
48. [データ ソースの追加] をクリックします。
49. [保存] をクリックします。
50. ページを閉じます。
51. [フォーマット] タブをクリックします。
52. ツリーで、「Intrastat\Data\Totals by blocks\Lines counting」を選択します。
53. [マッピング] タブをクリックします。
54. [式の編集] をクリックします。
    * このレポートに表示される各ブロックの行数の出荷を作成します。  
55. [式] フィールドで、「"このブロックの行数： " & 」を入力します。
    * "このブロックの行数: " &  
56. [式] フィールドで、「"このブロックの行数： " & TEXT(」を入力します。
    * "このブロックの行数: " & TEXT(  
57. ツリーで、「Data collection functions\COUNTIFS」を選択します。
58. [機能の追加] をクリックします。
59. [データ ソースの追加] をクリックします。
60. [式] フィールドで、「"このブロックの行数: " & TEXT(COUNTIFS('$BlockName', 」を入力します。
    * "このブロックの行数: " & TEXT(COUNTIFS('$BlockName',  
61. ツリーで、「$BlocksList」を展開します。
62. ツリーで、「$BlocksList\Value」を選択します
63. [データ ソースの追加] をクリックします。
64. [式] フィールドで、「"このブロックの行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, 」を入力します。
    * "このブロックの行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,  
65. ツリーで、「$RecName」を選択します。
66. [データ ソースの追加] をクリックします。
67. [式] フィールドで、「"このブロックの行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))」を入力します。
    * "このブロックの行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
68. [保存] をクリックします。
69. ページを閉じます。
70. [フォーマット] タブをクリックします。
71. ツリーで、「Intrastat\Data\Totals by blocks\Total amount」を選択します。
72. [マッピング] タブをクリックします。
73. [式の編集] をクリックします。
    * このレポートで指定された各ブロックの合計請求金額となる出荷を作成します。  
74. [式] フィールドで、「"合計請求金額: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))」を入力します。
    * "合計請求金額: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
75. [保存] をクリックします。
76. ページを閉じます。
77. [保存] をクリックします。
78. ページを閉じます。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
