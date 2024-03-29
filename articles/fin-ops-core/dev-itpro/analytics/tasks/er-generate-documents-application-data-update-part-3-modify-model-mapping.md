---
title: アプリケーション データを含むドキュメントを生成するためのモデルおよびマッピングの変更
description: この記事では、電子ドキュメントを生成し、アプリケーション データを更新するためのレポート作成構成を設計する方法について説明します。 (パート 2 - ドキュメントの生成)。
author: kfend
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8e94a78b9ee9821b65430b2fed179fd9f15617c1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290517"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a>アプリケーション データを含むドキュメントを生成するためのモデルおよびマッピングの変更

[!include [banner](../../includes/banner.md)]

この手順のステップを完了するには、まず 「ER アプリケーション データ更新と共にドキュメントを生成する (パート 2：ドキュメントの生成)」 に記載の手順を完了する必要があります。 

この手順のステップでは、電子ドキュメントを生成してアプリケーション データを更新するために電子申告 (ER) コンフィギュレーションを設計する方法について説明します。 この手順では、ER コンフィギュレーションを変更し、その使用を開始して、電子ドキュメントを生成しアプリケーション データを更新します。 この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられているユーザー用に作成されています。 これらのステップは、DEMF データ セットを使用して完了することができます。


## <a name="modify-data-model"></a>データ モデルの変更
1. [組織管理] > [電子申告] > [コンフィギュレーション] に移動します。
2. ツリーで、「イントラスタット (モデル)」を選択します。
    * データ モデルを使用する方法を拡張します。 データ モデルは、イントラスタット レポートを生成するデータ ソースとして使用するだけでなく、イントラスタット レポート プロセスに関する詳細を収集するためにも使用します。 その詳細は、アプリケーション データの更新に使用されます。   
3. [デザイナー] をクリックします。
4. [新規] をクリックすると、ドロップ ダイアログが開きます。
5. [新しいノード] フィールドに、「モデル ルート」を入力します。
6. [名前] フィールドに、「アプリケーション データの更新用」と入力します。
    * アプリケーション データの更新用  
7. [追加] をクリックします。
8. ツリーで、「アプリケーション データの更新用」を選択します。
    * この新しいルート項目は、イントラスタット レポート (データ ソースとして使用) からアプリケーション テーブル (更新先) にデータを移動するためのデータ フローを指定するために追加されます。 送信文書に投稿されるデータを取得したり、アプリケーション データを更新するために使用される文書からデータを取得するには、異なるルート項目を使用する必要があることに注意してください。   
9. [新規] をクリックすると、ドロップ ダイアログが開きます。
10. [名前] フィールドに、「アーカイブ ヘッダー」と入力します。
    * アーカイブ ヘッダー  
11. [品目タイプ] フィールドで、「レコード リスト」を選択します。
12. [追加] をクリックします。
    * 生成されるそれぞれのイントラスタット レポートにレコードを作成するので、そのための新しい品目を作成する必要があります。  
13. [新規] をクリックすると、ドロップ ダイアログが開きます。
14. [名称] フィールドで、「ファイル名」を入力します。
    * ファイル名  
15. [品目タイプ] フィールドで、「String」を選択します。
16. [追加] をクリックします。
17. [新規] をクリックすると、ドロップ ダイアログが開きます。
18. [名前] フィールドに、「行数」と入力します。
    * ライン数  
19. [項目タイプ] フィールドで、「整数」を選択します。
20. [追加] をクリックします。
    * 現在のレポート プロセス中にレポートされたイントラスタット トランザクションの数を表すために、この品目を追加します。  
21. [新規] をクリックすると、ドロップ ダイアログが開きます。
22. [名前] フィールドに、「アーカイブ明細行」と入力します。
    * アーカイブ明細行  
23. [品目タイプ] フィールドで、「レコード リスト」を選択します。
24. [追加] をクリックします。
    * 現在のレポート プロセス中にレポートされたイントラスタット トランザクションのリストを表すために、この品目を追加します。  
25. [新規] をクリックすると、ドロップ ダイアログが開きます。
26. [名前] フィールドに、「$Amount」と入力します。
    * 量  
27. [品目タイプ] フィールドで、「実数」を選択します。
28. [追加] をクリックします。
29. [新規] をクリックすると、ドロップ ダイアログが開きます。
30. [名前] フィールドに、「商品 rec id」と入力します。
    * 商品 rec id  
31. [項目タイプ] フィールドで、「Int64」を選択します。
32. [追加] をクリックします。
33. [新規] をクリックすると、ドロップ ダイアログが開きます。
34. [名前] フィールドに、「品目番号」と入力します。
    * 品目番号  
35. [品目タイプ] フィールドで、「String」を選択します。
36. [追加] をクリックします。
37. [保存] をクリックします。
38. ページを閉じます。

## <a name="modify-model-mapping"></a>モデル マッピングの変更
1. ツリーで、「イントラスタット (モデル)」を展開します。
2. ツリーで、「イントラスタット (モデル)\イントラスタット (マッピング)」を選択します。
    * 既存のモデルマッピングを変更して、アプリケーションデータの更新への使用を開始し、イントラスタット レポートの詳細をアーカイブします。  
3. [デザイナー] をクリックします。
4. [新規] をクリックします。
5. [名前] フィールドに、「アーカイブの更新」と入力します。
    * アーカイブの更新  
6. [方向] フィールドで、「宛先」を選択します。
7. [保存] をクリックします。
    * この新しいマッピングは、データ モデルからアプリケーション テーブル (更新先) にデータ (イントラスタット レポートの詳細) を移動するためのデータ フローを指定します。 レポート プロセスで使用するアプリケーションからデータを取得し、アプリケーション データ更新のためにデータ モデルのデータを使用するには、異なるモデルのルート項目を使用する必要があることに注意してください。   
8. [デザイナー] をクリックします。
9. ツリーで、「データ モデル\データ モデル」を選択します。
    * 必要なデータ ソースを追加します。 これは、アーカイブする必要のあるレポートされたイントラスタット トランザクションの詳細を含むデータ モデルです。  
10. [ルートの追加] をクリックします。
11. [名前] フィールドに、「モデル」と入力します。
    * モデル  
12. [定義] フィールドで、「アプリケーション データの更新」 という値を入力または選択します。
    * アプリケーション データの更新用  
13. [OK] をクリックします。
14. ツリーで、[model] を展開します。
15. ツリーで、[Functions\Calculated field] を選択します。
16. ツリーで、「モデル\アーカイブ ヘッダー」を選択します。
17. [追加] をクリックします。
    * アーカイブ用にレポート済イントラスタット トランザクションを列挙するため、適切なデータ ソースを追加する必要があります。  
18. [名前] フィールドに、「列挙された明細行」と入力します。
    * 列挙された明細行  
19. [式の編集] をクリックします。
20. ツリーで、「リスト\ENUMERATE」を選択します。
21. [機能の追加] をクリックします。
22. ツリーで、「model」を展開します。
23. ツリーで、「モデル\アーカイブ ヘッダー」を展開します。
24. ツリーで、「モデル\アーカイブ ヘッダー\アーカイブ明細行」を選択します。
25. [データ ソースの追加] をクリックします。
26. [フォーミュラ] フィールドに、「ENUMERATE(model.'Archive header'.'Archive lines')」と入力します。
    * ENUMERATE(model.'Archive header'.'Archive lines')  
27. [保存] をクリックします。
28. ページを閉じます。
29. [OK] をクリックします。
30. [宛先の追加] をクリックします。
    * レポート済のイントラスタット トランザクションの詳細をアーカイブするために更新を必要とする必要な出力先として、アプリケーション テーブルを追加します。  
31. [名前] フィールドに、「アーカイブ」と入力します。
    * アーカイブ  
32. [テーブル名] フィールドで、「IntrastatArchiveGeneral」と入力します。
    * IntrastatArchiveGeneral  
    * レコードアクション 「挿入」 を保持することで、イントラスタット レポートプロセスの詳細アーカイブ中にレコードを追加することができます。  
33. [レコード情報ログ] フィールドで [はい] を選択します。
    * [はい] を選択して、アプリケーション データ更新の問題に関する情報を取得します。  
34. [レコード アクションの検証のスキップ] フィールドで [はい] を選択します。
    * [はい] を選択すると、空の [イントラスタット アーカイブ ID] フィールドに関する検証エラーを抑制することができます。 これは、[対外貿易パラメーター] フォームのこのテーブルにコンフィギュレーションされている順序番号設定に基づいて、レコードの追加後に行われます。  
35. [OK] をクリックします。
    * 追加されたデータ ソースの要素 (選択されたルート項目に基づいてフィルタ処理されたモデル) を、追加された出力先の要素とバインドします。  
36. ツリーで、「アーカイブ」を展開します。
37. ツリーで、「アーカイブ\<リレーション」を展開します。
38. ツリーで、「アーカイブ\<リレーション\IntrastatArchiveDetail」を展開します。
39. ツリーで、「アーカイブ\<リレーション\IntrastatArchiveDetail\Amount(AmountMST)」を選択します。
40. ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行」を展開します。
41. ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行\値」を展開します。
42. ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行\値\金額」を選択します。
43. [バインド] をクリックします。
44. ツリーで、「アーカイブ\<リレーション\IntrastatArchiveDetail\商品 (IntrastatCommodity)」を選択します。
45. ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行\値\商品 rec id」を選択します。
46. [バインド] をクリックします。
47. ツリーで、「アーカイブ\<リレーション\IntrastatArchiveDetail\品目番号 (ItemId)」を選択します。
48. ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行\値\品目番号」を選択します。
49. [バインド] をクリックします。
50. ツリーで、「アーカイブ\<リレーション\IntrastatArchiveDetail\行番号 (LineNumber)」を選択します。
51. ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行\番号」を選択します。
52. [バインド] をクリックします。
53. ツリーで、「アーカイブ\<リレーション\IntrastatArchiveDetail」を選択します。
54. ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行」を選択します。
55. [バインド] をクリックします。
56. ツリーで、「アーカイブ\ファイル名 (FileName)」を選択します。
57. ツリーで、「モデル\アーカイブ ヘッダー\ファイル名」を選択します。
58. [バインド] をクリックします。
59. ツリーで、「アーカイブ\行数 (NumberOfLines)」を選択します。
60. ツリーで、「モデル\アーカイブ ヘッダー\行数」を選択します。
61. [バインド] をクリックします。
62. ツリーで、「アーカイブ」を選択します。
63. ツリーで、「モデル\アーカイブ ヘッダー」を選択します。
64. [バインド] をクリックします。
65. [保存] をクリックします。
66. ページを閉じます。
67. ページを閉じます。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
