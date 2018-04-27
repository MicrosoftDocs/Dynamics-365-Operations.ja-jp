--- 
title: "電子申告 (ER) のデータ モデル要素に作成済みの形式のコンポーネントをマッピングする"
description: "次の手順では、システム管理者ロールまたは電子申告開発者ロールのいずれかのユーザーが、支払いビジネス ドメインの電子ドキュメント書式を定義する電子レポート (ER) のコンポーネントにデータ モデルをマッピングする様子を示します。"
author: NickSelin
manager: AnnBe
ms.date: 02/27/2017
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
ms.openlocfilehash: 1c81a1268a56164e0d4465359a0f9ec425ee7c31
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="map-components-of-the-created-format-to-data-model-elements-for-electronic-reporting-er"></a>電子申告 (ER) のデータ モデル要素に作成済みの形式のコンポーネントをマッピングする

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

次の手順では、システム管理者ロールまたは電子申告開発者ロールのいずれかのユーザーが、支払いビジネス ドメインの電子ドキュメント書式を定義する電子レポート (ER) のコンポーネントにデータ モデルをマッピングする様子を示します。 この書式は、支払を処理するための電子ドキュメントを生成するために後で使用します。 この例では、サンプル会社 'Litware、Inc.' のコンフィギュレーションの書式設定を作成します。 ER コンフィギュレーションはすべての会社用に共有されるため、これらのステップはどの会社でも実行できます。 これらの手順を完了するには、最初に「コンフィギュレーションの書式設定の作成」タスク ガイドのステップを完了する必要があります。


## <a name="select-a-format-configuration"></a>書式コンフィギュレーションの選択
1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。
2. [コンフィギュレーションをレポートする] をクリックします。
3. ツリーで、「支払 (単純化モデル)」を展開します。
4. ツリーで、「支払 (単純化モデル)」 \BACS (英国の企業) を選択します。
5. [デザイナー] をクリックします。

## <a name="map-format-components-to-data-model-elements"></a>データ モデルの要素への形式のコンポーネントのマッピング
1. [展開] / [折りたたみ] をクリックします。
2. [マッピング] タブをクリックします。
3. ツリーで、「model」を展開します。
4. ツリーで、[Xml\Message\ProcessingDate\DateTime] を選択します。
5. ツリーで、[model\ProcessingDateTime] を選択します。
6. [バインド] をクリックします。
7. ツリーで、[Xml\Message\MessageId\String] を選択します。
8. ツリーで、[model\MessageIdentification] を選択します。
9. [バインド] をクリックします。
10. ツリーで、「model\Payments」を展開します。
11. ツリーで、[Xml\Message\Payments\Item\Amount\String] を選択します。
12. ツリーで、[model\Payments\InstructedAmount] を選択します。
13. [バインド] をクリックします。
14. ツリーで、[Xml\Message\Payments\Item\TransDate\DateTime] を選択します。
15. ツリーで、[model\Payments\TransactionDate] を選択します。
16. [バインド] をクリックします。
17. ツリーで、[Xml\Message\Payments\Item\Description\String] を選択します。
18. ツリーで、[model\Payments\Description] を選択します。
19. [バインド] をクリックします。
20. ツリーで、[Xml\Message\Payments\Item\Currency\String] を選択します。
21. ツリーで、「model\Payments\Currency」を選択します。
22. [バインド] をクリックします。
23. ツリーで、[Xml\Message\Payments\Item\Id] を選択します。
24. ツリーで、[model\Payments\End2EndID] を選択します。
25. [バインド] をクリックします。
26. ツリーで、[model\Payments\Creditor] を展開します。
27. ツリーで、[model\Payments\Creditor\Account] を展開します。
28. ツリーで、[model\Payments\Creditor\Agent] を展開します。
29. ツリーで、「Xml\Message\Payments\Item\Vendor\Name\String」を選択します。
30. ツリーで、[model\Payments\Creditor\Name] を選択します。
31. [バインド] をクリックします。
32. ツリーで、[Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String] を選択します。
33. ツリーで、[model\Payments\Creditor\Agent\RoutingNumber] を選択します。
34. [バインド] をクリックします。
35. ツリーで、[Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String] を選択します。
36. ツリーで、[model\Payments\Creditor\Account\Number] を選択します。
37. [バインド] をクリックします。
38. ツリーで、[Xml\Message\Payments\Item\Payer\Name\String] を選択します。
39. ツリーで、[model\Payments\Debtor] を展開します。
40. ツリーで、[model\Payments\Debtor\Account] を展開します。
41. ツリーで、[model\Payments\Debtor\Agent] を展開します。
42. ツリーで、[model\Payments\Debtor\Name] を選択します。
43. [バインド] をクリックします。
44. ツリーで、[Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String] を選択します。
45. ツリーで、[model\Payments\Debtor\Agent\RoutingNumber] を選択します。
46. [バインド] をクリックします。
47. ツリーで、[Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String] を選択します。
48. ツリーで、[model\Payments\Debtor\Account\Number] を選択します。
49. [バインド] をクリックします。
50. ツリーで、「Xml\Message\Payments\Item」を選択します。
51. ツリーで、[model\Payments] を選択します。
52. [バインド] をクリックします。
53. [保存] をクリックします。

## <a name="validate-format-mapping"></a>書式マッピングの検証
1. [検証] をクリックします。
    * 新しいマッピングを検証し、すべてのバインディングが要件を満たしていることを確認します。  
2. ページを閉じます。

## <a name="change-status-of-the-current-version-of-format-configuration"></a>コンフィギュレーションの書式設定の現在のバージョンのステータスの変更
    * 次の手順では、支払ドキュメント生成に使用するために、ドラフトから完了に書式コンフィギュレーションのステータスを変更します。  
1. [状態の変更] をクリックします。
2. [完了] をクリックします。
3. [説明] フィールドに値を入力します。
    * 例えば、「バージョン 1」。  
4. [OK] をクリックします。
5. 現在のコンフィギュレーションの完了したバージョンを選択します。
    * コンフィギュレーションの設定が完了したバージョン 1.1 として保存されることに注意してください。これはデータ モデルのバージョン 1 に基づく書式のバージョン 1 です。  

## <a name="define-effective-date-for-completed-version-of-format"></a>形式の完了したバージョンの有効期間の定義
    * 各書式のバージョンは、特定の日付をから使用開始するように設定できます。 複数の書式のバージョンを特定の日付に有効にする場合は、最新書式 (バージョン番号に基づく) を使用できるように選択します。 セッション日付値は、適切なバージョンの選択に使用されます。  

## <a name="restrict-access-to-created-format-from-companies"></a>会社から作成した形式へのアクセスの制限
1. [ISO 国/地域コード] セクションを展開します。
    * 各書式へのアクセスは、書式が適用される特定の国/地域の ID によって制限することができます。 特定の書式の国/地域のリストが空の場合、この書式は任意の会社で使用することができます。 一部の ISO 国/地域コードがその国/地域のリストに挿入された場合、この書式は基本住所がその国/地域にある場合にのみ会社で使用することができます。  


