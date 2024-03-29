---
title: ER 書式設定のコンフィギュレーションの作成 (2016 年 11 月)
description: この記事では、電子申告 (ER) 用の形式構成を作成する方法について説明します。
author: kfend
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
ms.openlocfilehash: 3c705add64a46c4cce5127f16fae45edba1bc001
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290727"
---
# <a name="er-create-a-format-configuration-november-2016"></a>ER 書式設定のコンフィギュレーションの作成 (2016 年 11 月)

[!include [banner](../../includes/banner.md)]

この記事では、システム管理者または電子申告開発者の役割のユーザーが、電子申告 (ER)の形式構成作成方法について説明します。 このコンフィギュレーションの書式設定では、支払を処理するために使用される電子ドキュメントの書式を定義します。 この例では、サンプル会社 Litware、Inc. のフォーマット構成を作成します。この手順を完了するには、まず「選択したデータソースへのモデルのマッピング」に記載の手順のを完了する必要があります。


## <a name="create-a-new-format-configuration"></a>新しいコンフィギュレーションの書式設定の作成
1. **組織管理 > ワークスペース > 電子申告** の順に移動します。
2. **コンフィギュレーションをレポートする** をクリックします。
3. ツリーで、**支払 (単純化モデル)** を選択します。
4. **コンフィギュレーションの作成** をクリックして、ドロップ ダイアログを開きます。

 > [!NOTE]
 > **コンフィギュレーションの作成** が表示されない場合は、**電子申告のパラメーター** ページでデザイン モードを有効にする必要があります。 
 
5. **新規** フィールドで、**PaymentModel データ モデルに基づいた書式** と入力します。
6. **名前** フィールドに、**BACS (英国企業)** と入力します。
7. **説明** フィールドに、**BACS 仕入先支払形式 (英国企業)** と入力します。
    * 有効なコンフィギュレーション プロバイダーは自動的にここに入力されます。 このプロバイダーはこのコンフィギュレーションを管理できます。 他のプロバイダーはこのコンフィギュレーションを使用できますが、管理できません。  
    * 電子ドキュメントの特定の形式を定義できます。 実行時に形式を選択する場合は、このフィールドを空白のままにします。  
8. **データ モデル定義** フィールドで、値を入力または選択します。
9. **コンフィギュレーションの作成** をクリックします。 新しいコンフィギュレーションが作成されました。 ドラフト バージョンは、電子ドキュメントを管理するためのデザイン形式の保存に使用できます。  

## <a name="design-the-format-of-an-electronic-document"></a>電子ドキュメントの形式のデザイン
1. **デザイナー** をクリックします。
2. **ルートの追加** をクリックして、ドロップ ダイアログを開きます。
3. ツリーで、**Common\File** を選択します。
4. **名前** フィールドに、**Xml** と入力します。
5. **エンコード** フィールドに、**UTF-8** と入力します。
6. **OK** をクリックします。
7. **追加** をクリックします。
8. ツリーで、**XML\Element** を選択します。
9. **名前** フィールドに、**メッセージ** と入力します。
10. **OK** をクリックします。
11. ツリーで、**Xml\Message** を選択します。
12. **要素の追加** をクリックします。
13. **名前** フィールドに、**ProcessingDate** と入力します。
14. **OK** をクリックします。
15. **要素の追加** をクリックします。
16. 名前フィールドに、**MessageId** と入力します。
17. **OK** をクリックします。
18. **要素の追加** をクリックします。
19. **名前** フィールドに、**支払** と入力します。
20. **OK** をクリックします。
21. ツリーで、**Xml\Message\Payments** を選択します。
22. **要素の追加** をクリックします。
23. **名前** フィールドに、**品目** と入力します。
24. **OK** をクリックします。
25. ツリーで、**Xml\Message\Payments\Item** を選択します。
26. **追加** をクリックします。
27. ツリーで、**XML\Attribute** を選択します。
28. 名前フィールドに、**Id** と入力します。
29. **OK** をクリックします。
30. **追加** をクリックします。
31. ツリーで、**XML\Element** を選択します。
32. 名前フィールドに、**仕入先** と入力します。
33. **OK** をクリックします。
34. ツリーで、**Xml\Message\Payments\Item\Vendor** を選択します。
35. **要素の追加** をクリックします。
36. 名前フィールドに、**名前** と入力します。
37. **OK** をクリックします。
38. **要素の追加** をクリックします。
39. **名前** フィールドに、**銀行** と入力します。
40. **OK** をクリックします。
41. ツリーで、**Xml\Message\Payments\Item\Vendor\Bank** を選択します。
42. **要素の追加** をクリックします。
43. **名前** フィールドに、**RoutingNumber** と入力します。
44. **OK** をクリックします。
45. **要素の追加** をクリックします。
46. **名前** フィールドに、**AccountNumber** と入力します。
47. **OK** をクリックします。
48. ツリーで、**Xml\Message\Payments\Item\Vendor** を選択します。
49. **コピー** をクリックします。
50. ツリーで、**Xml\Message\Payments\Item** を選択します。
51. **ペースト** をクリックします。
52. **名前** フィールドに、**支払人** と入力します。
53. ツリーで、**Xml\Message\Payments\Item** を選択します。
54. **要素の追加** をクリックします。
55. **名前** フィールドに、**通貨** と入力します。
56. **OK** をクリックします。
57. **要素の追加** をクリックします。
58. **名前** フィールドに、**説明** と入力します。
59. **OK** をクリックします。
60. **要素の追加** をクリックします。
61. 名前フィールドに、**TransDate** と入力します。
62. **OK** をクリックします。
63. **要素の追加** をクリックします。
64. 名前フィールドに、**Amount** と入力します。
65. **OK** をクリックします。

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>データ モデルの要素にマッピングする形式のコンポーネントを準備します。
1. ツリーで、**Xml\Message\ProcessingDate** を選択します。
2. **追加** をクリックしてドロップ ダイアログを開きます。
3. ツリーで、**Text\DateTime** を選択します。
4. **形式** フィールドに、**yyyy-MM-dd** と入力します。
5. **OK** をクリックします。
6. ツリーで、**Xml\Message\Payments\Item\TransDate** を選択します。
7. **日時を追加** をクリックします。
8. **形式** フィールドに、**yyyy-MM-dd** と入力します。
9. **DateTime** 型フィールドで、**日付** を選択します。
10. **OK** をクリックします。
11. ツリーで、**Xml\Message\MessageId** を選択します。
12. **追加** をクリックしてドロップ ダイアログを開きます。
13. ツリーで、**Text\String** を選択します。
14. **OK** をクリックします。
15. ツリーで、**Xml\Message\Payments\Item\Vendor\Name** を選択します。
16. **文字列の追加** をクリックします。
17. **OK** をクリックします。
18. ツリーで、**Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber** を選択します。
19. **文字列の追加** をクリックします。
20. **OK** をクリックします。
21. ツリーで、**Xml\Message\Payments\Item\Vendor\Bank\AccountNumber** を選択します。
22. **文字列の追加** をクリックします。
23. **OK** をクリックします。
24. ツリーで、**Xml\Message\Payments\Item\Payer\Name** を選択します。
25. **文字列の追加** をクリックします。
26. **OK** をクリックします。
27. ツリーで、**Xml\Message\Payments\Item\Payer\Bank\RoutingNumber** を選択します。
28. **文字列の追加** をクリックします。
29. **OK** をクリックします。
30. ツリーで、**Xml\Message\Payments\Item\Payer\Bank\AccountNumber** を選択します。
31. **文字列の追加** をクリックします。
32. **OK** をクリックします。
33. ツリーで、**Xml\Message\Payments\Item\Currency** を選択します。
34. **文字列の追加** をクリックします。
35. **OK** をクリックします。
36. ツリーで、**Xml\Message\Payments\Item\Description** を選択します。
37. **文字列の追加** をクリックします。
38. **OK** をクリックします。
39. ツリーで、**Xml\Message\Payments\Item\Amount** を選択します。
40. **文字列の追加** をクリックします。
41. **OK** をクリックします。
42. **保存** をクリックします。
43. ページを閉じます。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
