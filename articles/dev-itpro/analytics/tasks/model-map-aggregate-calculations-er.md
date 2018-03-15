--- 
title: "データベース レベル (ER) でモデル マッピングの configurationforaggregate 計算を使用する"
description: "この手順は、新しい電子申告 (ER) モデル マッピング コンフィギュレーションをデザインして、効率的な集計計算の組み込み ER 機能を使用する方法に関する情報を提供します。"
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: 3c3558d9e25dcfd56f3306e69884528d01324cbd
ms.contentlocale: ja-jp
ms.lasthandoff: 02/07/2018

---
# <a name="use-a-model-mapping-configuration-for-aggregate-calculations-at-the-database-leveler"></a>データベース レベル (ER) で集約計算に対するモデル マッピング コンフィギュレーションを使用する 

[!include[task guide banner](../../includes/task-guide-banner.md)]

この手順は、新しい電子申告 (ER) モデル マッピング コンフィギュレーションをデザインして、効率的な集計計算の組み込み ER 機能を使用する方法に関する情報を提供します。 この手順では、サンプル会社 Litware、Inc. のコンフィギュレーションを作成します。 

この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられているユーザー用に作成されています。 これらのステップは、任意のデータ セットを使用して完了することができます。

 これらの手順を完了するには、手順にあるステップを最初に実行する必要があります。[ER はデータベース レベルでそれらを実行することで、集約計算の効率が向上を図ります (第1部: コンフィギュレーションの準備)]

1. [組織管理] > [電子申告] > [コンフィギュレーション] に移動します。
2. ツリーで、「Intrastat model」を展開します。
3. ツリーで、「イントラスタット モデル\イントラスタットのサンプル マッピング」を選択します。
4. [デザイナー] をクリックします。
5. [デザイナー] をクリックします。
6. ツリーで、[Dynamics 365 for Operations\Table records] を選択します。
7. [ルートの追加] をクリックします。
    * グループ化するレコードを表す新しいデータ ソースを追加  
8. [名前] フィールドで、「Transactions」と入力します。
    * トランザクション  
9. [テーブル] フィールドで、「Intrastat」と入力します。
    * イントラスタット  
10. [OK] をクリックします。
11. ツリーで、「Functions\Group by」を選択します。
    * このデータ ソースのタイプは、レコードをグループ化して必要な集約を計算する実行時、新しいデータ ソースの案内に使用されます。  
12. [ルートの追加] をクリックします。
13. 名前 フィールドで、「TransactionsGroups」と入力します。
    * TransactionsGroups  
14. [次の基準でグループを編集] をクリックします。
15. ツリーで、[Transactions] を選択します。
    * グループ化したいレコードを表す「レコード リスト」タイプの追加されたデータ ソースを選択します。  
16. [フィールドの追加先] をクリックします。
17. [グループ化の対象] をクリックします。
18. ツリーで、[Transactions] を展開します。
19. ツリーで、「Transactions\Direction」を選択します。
20. [フィールドの追加先] をクリックします。
21. [グループ化されたフィールド] をクリックします。
    * グループ化レベルを指定するフィールドを選択します。 この選択に基づいて、データ ソースは実行時に、イントラスタットのテーブルで満たされる方向コードがあるように、トランザクションの多くのグループとして返されます。  
22. ツリーで、「Transactions\Invoice amount(AmountMST)」を選択します。
    * 集約計算のソースを指定するには、そのフィールドを選択します。  
23. [フィールドの追加先] をクリックします。
24. [集計] フィールドをクリックします。
25. 一覧で、選択された行をマークします。
26. [方法] フィールドで、「Sum」を選択します。
    * 集約タイプを選択します。  
27. [名前] フィールドで、「SumOfAmountMST」と入力します。
    * コンフィギュレーション済のデータ ソース内にあるこの集約の名前を指定します。  
28. [保存] をクリックします。
    * [実行場所] フィールドが SQL のデータ ベースで、実行時にこのグループ化が実行されることを示すことに注意してください。  
29. ページを閉じます。
30. [OK] をクリックします。
31. ツリーで、「Totals」を展開します。
32. ツリーで、「TransactionsGroups」を展開します。
33. ツリーで、「TransactionsGroups\aggregated」を展開します。
34. ツリーで、「TransactionsGroups\aggregated\SumOfAmountMST」を選択します。
35. ツリーで、「Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')」を選択します。
36. [バインド] をクリックします。
    * この設定に基づいて、このデータ ソースはトランザクションの各グループに対して [AmountMST] フィールドの値の合計を計算します。 この集約計算は、TransactionsGroups.aggregated.TotalAmount 品目として使用可能になります。  
37. ツリーで、「TransactionsGroups」を展開します。
38. ツリーで、「TransactionsGroups」を選択します。
39. [編集] をクリックします。
40. [次の基準でグループを編集] をクリックします。
41. ツリーで、[Transactions] を展開します。
42. ツリーで、「Transactions\Invoice amount(AmountMST)」を選択します。
43. [フィールドの追加先] をクリックします。
44. [集計] フィールドをクリックします。
45. 一覧で、選択された行をマークします。
46. [方法] フィールドで、「Max」を選択します。
47. [名前] フィールドで、「MaxOfAmountMST」と入力します。
48. [保存] をクリックします。
    * 現時点では、SQL のデータベース レベルがいくつかの制限で GROUPBY データ ソースの実行を変換することができます。 翻訳は、「レコードの一覧」タイプのデータ ソースまたは FILTER 関数を式として実行するデータ ソースのどちらでも行うことができます。 また、一つの集約のみがグループ化レコードの単一フィールドのためにコンフィギュレーションされている場合も実行できます。  
    * たとえ一つ以上の集約は AmountMST フィールドにコンフィギュレーションされたとしても、これはまだ [実行場所] フィールドが SQLデータベースの実行時にこのグループ化が実行されることを示しています。 これは、一つだけの集計がデータ モデルの品目にバインドされて、このデータ ソースから実行時にデータの取得に使用されるためです。  
49. ページを閉じます。
50. [OK] をクリックします。
51. ツリーで、「TransactionsGroups」を展開します。
52. ツリーで、「TransactionsGroups\aggregated」を展開します。
53. ツリーで、「TransactionsGroups\aggregated\MaxOfAmountMST」を選択します。
54. ツリーで、「Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')」を選択します。
55. [バインド] をクリックします。
56. ツリーで、「TransactionsGroups」を展開します。
57. ツリーで、「TransactionsGroups」を選択します。
58. [編集] をクリックします。
59. [次の基準でグループを編集] をクリックします。
    * [実行場所] フィールドは、同じフィールドの両方の集約がデータ モデルの品目にバインドされているため、このグループ化がメモリーで実行時に実行されることを示します。   
60. 一覧で、すべての行のマークを設定または解除します。
61. [削除] をクリックします。
62. [はい] をクリックします。
63. [削除] をクリックします。
64. [はい] をクリックします。
65. [フィールドの追加先] をクリックします。
66. [グループ化の対象] をクリックします。
67. ツリーで、「Commodity record(Intrastat)」を展開します。
68. [保存] をクリックします。
    * [実行場所] フィールドは、たとえ集約定義が無く、「テーブル レコード」タイプの選択されたデータ ソースが同じ「イントラスタット」テーブルを参照しても、このグループ化はメモリーの実行時に実行されることを示します。 これは、そのデータ ソースがまだ SQL データベース レベルに翻訳できないいくつかの計算済フィールドを含むからです。  


