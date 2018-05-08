--- 
title: "電子申告 (ER) 用の形式コンフィギュレーションを作成する"
description: "次の手順では、システム管理者または電子申告開発者の役割のユーザーが、電子申告 (ER) にコンフィギュレーションの書式設定を作成する方法を説明します。"
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 04817d1f1851e43679995641e8b0ff99edaa83ad
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a>電子申告 (ER) 用の形式コンフィギュレーションを作成する

[!include [task guide banner](../../includes/task-guide-banner.md)]

次の手順では、システム管理者または電子申告開発者の役割のユーザーが、電子申告 (ER) にコンフィギュレーションの書式設定を作成する方法を説明します。 このコンフィギュレーションの書式設定では、支払を処理するために使用される電子ドキュメントの書式を定義します。 この例では、サンプル会社 Litware、Inc. の形式コンフィギュレーションを作成します。これらの手順を完了するには、先に「選択したデータソースへのモデルのマッピング」の手順の各ステップを完了する必要があります。


## <a name="create-a-new-format-configuration"></a>新しいコンフィギュレーションの書式設定の作成
1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。
2. [コンフィギュレーションをレポートする] をクリックします。
3. ツリーで、「支払 (単純化モデル)」を選択します。
4. [コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。
5. [新規] フィールドで、「PaymentModel データ モデルに基づいた書式」と入力します。
6. [名前] フィールドに、「BACS (英国企業)」と入力します。
    * BACS (英国企業)  
7. [説明] フィールドに、「BACS の仕入先支払形式 (英国企業) 」と入力します。
    * BACS の仕入先支払形式 (英国企業)  
    * 有効なコンフィギュレーション プロバイダーは自動的にここに入力されます。 このプロバイダーはこのコンフィギュレーションを管理できます。 他のプロバイダーはこのコンフィギュレーションを使用できますが、管理できません。  
    * 電子ドキュメントの特定の形式を定義できます。 実行時に形式を選択する場合は、このフィールドを空白のままにします。  
8. [データモデル定義] フィールドで、値を入力または選択します。
9. [コンフィギュレーションの作成] をクリックします。
    * 新しいコンフィギュレーションが作成されました。 ドラフト バージョンは、電子ドキュメントを管理するためのデザイン形式の保存に使用できます。  

## <a name="design-format-of-electronic-document"></a>電子ドキュメントのデザイン形式
1. [デザイナー] をクリックします。
2. [ルートの追加] をクリックして、ドロップ ダイアログを開きます。
3. ツリーで、[Common\File] を選択します。
4. [名前] フィールドに、「Xml」と入力します。
    * Xml  
5. [エンコード] フィールドに、「UTF-8」と入力します。
    * UTF-8  
6. [OK] をクリックします。
7. [追加] をクリックしてドロップ ダイアログを開きます。
8. ツリーで、[XML\Element] を選択します。
9. [名前] フィールドに、「メッセージ」と入力します。
    * メッセージ  
10. [OK] をクリックします。
11. ツリーで、「Xml\Message」を選択します。
12. [エレメントの追加] をクリックします。
13. [名前] フィールドに、「ProcessingDate」と入力します。
    * ProcessingDate  
14. [OK] をクリックします。
15. [エレメントの追加] をクリックします。
16. [名前] フィールドに、「MessageId」と入力します。
    * MessageId  
17. [OK] をクリックします。
18. [エレメントの追加] をクリックします。
19. [名前] フィールドに、「支払」と入力します。
    * 支払利息  
20. [OK] をクリックします。
21. ツリーで、「Xml\Message\Payments」を選択します。
22. [エレメントの追加] をクリックします。
23. [名前] フィールドに、「Item」と入力します。
    * 項目  
24. [OK] をクリックします。
25. ツリーで、「Xml\Message\Payments\Item」を選択します。
26. [追加] をクリックしてドロップ ダイアログを開きます。
27. ツリーで、[XML\Attribute] を選択します。
28. [名前] フィールドに、「Id」と入力します。
    * ID  
29. [OK] をクリックします。
30. [追加] をクリックしてドロップ ダイアログを開きます。
31. ツリーで、[XML\Element] を選択します。
32. [名前] フィールドに、「Vendor」と入力します。
    * ベンダー  
33. [OK] をクリックします。
34. ツリーで、「Xml\Message\Payments\Item\Vendor」を選択します。
35. [エレメントの追加] をクリックします。
36. [名前] フィールドに、「名前」と入力します。
    * 氏名  
37. [OK] をクリックします。
38. [エレメントの追加] をクリックします。
39. [名前] フィールドに、「Bank」と入力します。
    * 銀行  
40. [OK] をクリックします。
41. ツリーで、「Xml\Message\Payments\Item\Vendor\Bank」を選択します。
42. [エレメントの追加] をクリックします。
43. [名前] フィールドに、「RoutingNumber」と入力します。
    * RoutingNumber  
44. [OK] をクリックします。
45. [エレメントの追加] をクリックします。
46. [名前] フィールドに、「AccountNumber」と入力します。
    * AccountNumber  
47. [OK] をクリックします。
48. ツリーで、「Xml\Message\Payments\Item\Vendor」を選択します。
49. [コピー] をクリックします。
50. ツリーで、「Xml\Message\Payments\Item」を選択します。
51. [ペースト] をクリックします。
52. [名前] フィールドに、「Payer」と入力します。
    * 指定します  
53. ツリーで、「Xml\Message\Payments\Item」を選択します。
54. [エレメントの追加] をクリックします。
55. [名前] フィールドで、「通貨」と入力します。
    * 通貨  
56. [OK] をクリックします。
57. [エレメントの追加] をクリックします。
58. [名前] フィールドに、「説明」と入力します。
    * 説明  
59. [OK] をクリックします。
60. [エレメントの追加] をクリックします。
61. [名前] フィールドに、「TransDate」と入力します。
    * TransDate  
62. [OK] をクリックします。
63. [エレメントの追加] をクリックします。
64. [名前] フィールドに、「$Amount」と入力します。
    * 量  
65. [OK] をクリックします。

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>データ モデルの要素にマッピングする形式のコンポーネントを準備します。
1. ツリーで、「Xml\Message\ProcessingDate」を選択します。
2. [追加] をクリックしてドロップ ダイアログを開きます。
3. ツリーで、「Text\DateTime」を選択します。
4. [形式] フィールドで、「yyyy-MM-dd」と入力します。
    * yyyy-MM-dd  
5. [OK] をクリックします。
6. ツリーで、「Xml\Message\Payments\Item\TransDate」を選択します。
7. [日時を追加] をクリックします。
8. [形式] フィールドで、「yyyy-MM-dd」と入力します。
    * yyyy-MM-dd  
9. [DateTime 型] フィールドで、「日付」を選択します。
10. [OK] をクリックします。
11. ツリーで、「Xml\Message\MessageId」を選択します。
12. [追加] をクリックしてドロップ ダイアログを開きます。
13. ツリーで、[Text\String] を選択します。
14. [OK] をクリックします。
15. ツリーで、「Xml\Message\Payments\Item\Vendor\Name」を選択します。
16. [ストリングの追加」をクリックします。
17. [OK] をクリックします。
18. ツリーで、「Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber」を選択します。
19. [ストリングの追加」をクリックします。
20. [OK] をクリックします。
21. ツリーで、「Xml\Message\Payments\Item\Vendor\Bank\AccountNumber」を選択します。
22. [ストリングの追加」をクリックします。
23. [OK] をクリックします。
24. ツリーで、「Xml\Message\Payments\Item\Payer\Name」を選択します。
25. [ストリングの追加」をクリックします。
26. [OK] をクリックします。
27. ツリーで、「Xml\Message\Payments\Item\Payer\Bank\RoutingNumber」を選択します。
28. [ストリングの追加」をクリックします。
29. [OK] をクリックします。
30. ツリーで、「Xml\Message\Payments\Item\Payer\Bank\AccountNumber」を選択します。
31. [ストリングの追加」をクリックします。
32. [OK] をクリックします。
33. ツリーで、「Xml\Message\Payments\Item\Currency」を選択します。
34. [ストリングの追加」をクリックします。
35. [OK] をクリックします。
36. ツリーで、「Xml\Message\Payments\Item\Description」を選択します。
37. [ストリングの追加」をクリックします。
38. [OK] をクリックします。
39. ツリーで、「Xml\Message\Payments\Item\Amount」を選択します。
40. [ストリングの追加」をクリックします。
41. [OK] をクリックします。
42. [保存] をクリックします。
43. ページを閉じます。


