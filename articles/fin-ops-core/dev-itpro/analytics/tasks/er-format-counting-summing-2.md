---
title: ER 棚卸および集計を行うための形式のコンフィギュレーション (第 2 部 - 計算のコンフィギュレーション)
description: 次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d785b321037645837dbcbaf28c8ede9b8e97b79
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550605"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a>ER 棚卸および集計を行うための形式のコンフィギュレーション (第 2 部 - 計算のコンフィギュレーション)

[!include [task guide banner](../../includes/task-guide-banner.md)]

次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。 これらの手順はどのタイプの企業でも実施できます。

これらの手順を完了するには、まず「計算と集計を行うER設定フォーマット（パート1：フォーマットの作成）」の手順を完了する必要があります。

この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a>フォーマット設定を作成し、計算と集計の情報を加えます。
1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。
2. [コンフィギュレーションをレポートする] をクリックします。
3. ツリーで、「Intrastat model」を展開します。
4. ツリーで、「イントラスタットmodel\Intrastat (DE)を選択します。
    * イントラスタット レポートの最後に集計詳細を含む明細行を追加して、Microsoft 提供のフォーマットをカスタマイズする必要があります。 そのためには、変更を行うMicrosoftのインスタンスからイントラスタット コンフィギュレーションのインスタンスを取得する必要があります。  
5. [コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。
6. [新規] フィールドで、「名称から取得: Intrastat (DE), Microsoft」を選択します。
7. [名称] フィールドに、「計算 & 集計を含Intrastat (DE)」と入力します。
8. [コンフィギュレーションの作成] をクリックします。

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a>出荷詳細に基づく計算と集計を行うには、このレポートを設定します。
1. [デザイナー] をクリックします。
2. [出荷情報] フィールドで、[はい] を選択します。
    * このフラグは、イントラスタット ファイル生成に必要な出力情報を収集するプロセスを実行時にアクティブ化します。  
    * イントラスタットのさまざまな指示について計算をする必要があるため、このフォーマットのコンフィグレーションのデータソースリストに専用モデルリストを追加します。  
3. [マッピング] タブをクリックします。
4. [ルートの追加] をクリックして、ドロップ ダイアログを開きます。
5. ツリーで、「Data model\Enumeration」を選択します。
6. [名称] フィールドに、「指示」を入力します。
7. [モデル リスト] フィールドで、値を入力または選択します。
    * 値の「指示」を選択します。  
8. [OK] をクリックします。
9. [ルートの追加] をクリックして、ドロップ ダイアログを開きます。
10. ツリーで、[Functions\Calculated field] を選択します。
11. [名称] フィールドに、[$BlockName] を入力します。
12. [式の編集] をクリックします。
13. [式] フィールドに、[ブロック] を入力します。
14. [保存] をクリックします。
15. ページを閉じます。
16. [OK] をクリックします。
17. [ルートの追加] をクリックして、ドロップ ダイアログを開きます。
18. ツリーで、[Functions\Calculated field] を選択します。
19. [名称] フィールドに、[$RecName] を入力します。
20. [式の編集] をクリックします。
21. [式] フィールドに、[記録] を入力します。
22. [保存] をクリックします。
23. ページを閉じます。
24. [OK] をクリックします。
25. [ルートの追加] をクリックして、ドロップ ダイアログを開きます。
26. ツリーで、[Functions\Calculated field] を選択します。
27. [名称] フィールドに、[$InvName] を入力します。
28. [式の編集] をクリックします。
29. [式] フィールドに、[InvoicedAmountEUR] を入力します。
30. [保存] をクリックします。
31. ページを閉じます。
32. [OK] をクリックします。
33. ツリーで、「Intrastat\Data」を選択します。
34. 「収集したデータ キー名」のフィールドの編集のボタンをクリックします。
35. [データ ソースの追加] をクリックします。
    * $BlockName  
36. [保存] をクリックします。
37. ページを閉じます。
38. 「収集したデータ キー値」のフィールドの編集のボタンをクリックします。
39. [式] フィールドに、「IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")」を入力します。
    * IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")  
40. [保存] をクリックします。
41. ページを閉じます。
    * このシーケンスの明細行をカウントします。 結果は、別途さまざまな方向の名称「ブロック」で使用されます。 値「インポートは」、着荷のイントラスタット トランザクションに使用されます。 値「エクスポートは」、発送のイントラスタット トランザクションに使用されます。 これが仮想のExcelワークシートの有効であるとみなします。 各トランザクションについて、最初の列「ブロック」は「インポート」と「エクスポート」が入ります。  
42. ツリーで、「Intrastat\Data: Sequence」を展開します。
43. ツリーで、「Intrastat\Data: Sequence\Arrivals?」を選択します。
44. 「収集したデータ キー名」のフィールドの編集のボタンをクリックします。
    * このシーケンスの明細行をカウントします。 結果は、名称「記録」を使用して記憶されます。  
45. ツリーで、「$RecName」を選択します。
46. [データ ソースの追加] をクリックします。
47. [保存] をクリックします。
48. ページを閉じます。
49. 「収集したデータ キー値」のフィールドの編集のボタンをクリックします。
50. [式] フィールドで、「Intrastat.CommodityRecord.CommodityCode」を入力します。
51. [保存] をクリックします。
52. ページを閉じます。
    * このシーケンスの明細行をカウントします。 結果は、別途さまざまな商品コードについて名称「記録」で使用されます。 これが仮想のExcelワークシートの有効であるとみなします。 各トランザクションについて、最初の列「ブロック」は「インポート」と「エクスポート」が入り、2番目のブロック「記録」は商品コード値が入ります。  
53. ツリーで、「Intrastat\Data: Sequence\Dispatches?」を選択します。
54. 「収集したデータ キー名」のフィールドの編集のボタンをクリックします。
55. ツリーで、「$RecName」を選択します。
56. [データ ソースの追加] をクリックします。
57. [保存] をクリックします。
58. ページを閉じます。
59. 「収集したデータ キー値」のフィールドの編集のボタンをクリックします。
60. [式] フィールドで、「Intrastat.CommodityRecord.CommodityCode」を入力します。
61. [保存] をクリックします。
62. ページを閉じます。
63. ツリーで、「Intrastat\Data: Sequence\Dispatches: Sequence?」を展開します。
64. ツリーで、「Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord」を展開します。
65. [フォーマット] タブをクリックします。
66. ツリーで、「Intrastat\Data\Dispatches\Record\Invoice amount EUR」を選択します。
67. [マッピング] タブをクリックします。
68. 「収集したデータ キー名」のフィールドの編集のボタンをクリックします。
69. ツリーで、「$InvName」を選択します。
70. [データ ソースの追加] をクリックします。
71. [保存] をクリックします。
72. ページを閉じます。
    * このシーケンスの明細行について、請求額を集計します。 結果は、別途さまざまなイントラスタットの指示と商品コードについて名称「記録」で使用されます。 これが仮想のExcelスプレッドシートであるとみなします。 各トランザクションについて、最初の列「ブロック」は「インポート」と「エクスポート」が入ります。 2番目のブロック「記録」は商品コードの値が入り、3番目の列「InvoicedAmountEUR値」は請求金額が入ります。  
73. ツリーで、「Intrastat\Data\Arrivals?」を展開します。
74. ツリーで、「Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord」を展開します。
75. [フォーマット] タブをクリックします。
76. ツリーで、「Intrastat\Data\Dispatches\Record\Invoice amount EUR」を選択します。
77. [マッピング] タブをクリックします。
78. 「収集したデータ キー名」のフィールドの編集のボタンをクリックします。
79. ツリーで、「$InvName」を選択します。
80. [データ ソースの追加] をクリックします。
81. [保存] をクリックします。
82. ページを閉じます。
83. [保存] をクリックします。
84. ページを閉じます。

