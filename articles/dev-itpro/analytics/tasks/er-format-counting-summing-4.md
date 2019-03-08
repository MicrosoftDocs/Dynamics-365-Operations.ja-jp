---
title: ER 棚卸および集計を行うための形式のコンフィギュレーション (第 4 部 - 形式の実行)
description: 次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 17989b7fa2baf14472ec19a041cb5ce7e5c0380d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "336201"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4-run-format"></a>ER 棚卸および集計を行うための形式のコンフィギュレーション (パート 4: 形式の実行)

[!include [task guide banner](../../includes/task-guide-banner.md)]

次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。 これらのステップは DEMF 会社で実行できます。

これらの手順を完了するには、まず「計算と集計を行うER設定フォーマット（パート3：出荷のための計算）」の手順を完了する必要があります。

この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a>イントラスタット レポートの生成にあたり、この設定をテストします。
1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。
2. [コンフィギュレーションをレポートする] をクリックします。
3. ツリーで、「Intrastat model」を展開します。
4. ツリーで、「Intrastat model\Intrastat (DE)」を選択します。
5. ツリーで、「Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'」を選択します。
6. アクション ウィンドウで、[設定] をクリックします。
7. [ユーザー パラメーター] をクリックします。
8. [設定の実行] フィールドで、[はい] を選択します。
9. [OK] をクリックします。
10. [編集] をクリックします。
11. [ドラフトの実行] フィールドで、[はい] を選択します。
12. [保存] をクリックします。
13. [税] > [設定] > [対外貿易] > [対外貿易パラメーター] の順に移動します。
14. [電子申告] セクションを展開します。
15. [計算 & 集計を含むイントラスタット (DE)] の設定を選択します。
16. [計算 & 集計を含むイントラスタット (DE)] の設定を選択します。
17. [保存] をクリックします。
18. ページを閉じます。
19. [税] > [申告] > [対外貿易] > [イントラスタット] の順に移動します。
20. [出力] をクリックします。
21. [レポート] をクリックします。
    * イントラスタット レポートの生成処理を実行します。  
22. [開始日] フィールドで、日付を「2000-01-01」に設定します。
    * トランザクションのフォームで既存のレポートを含むレポート期間の開始日と終了日を定義します。  
23. [終了日] フィールドで、日付を「2022-12-31」に設定します。
    * トランザクションのフォームで既存のレポートを含むレポート期間の開始日と終了日を定義します。  
24. [指示] フィールドで、「着荷」を選択します。
25. [ファイルの生成] フィールドで、[はい] を選択します。
26. [OK] をクリックします。
    * 最終的な集計明細行を含む作成済みの出荷を確認します。  
27. [新規] をクリックします。
28. 一覧で、選択された行をマークします。
29. [指示] フィールドで、「発送」を選択します。
30. [品目番号] フィールドで、値を入力または選択します。
31. [商品] フィールドで値を入力または選択します。
32. 受領を「10」に設定します。
33. 請求金額を「10000」に設定します。
34. 統計金額を「10000」に設定します。
35. [出力] をクリックします。
36. [レポート] をクリックします。
37. [指示] フィールドで、「発送」を選択します。
38. [OK] をクリックします。
    * 最終的な集計明細行を含む作成済みの出荷を確認します。 最初の実行時と比較すると変更されていることに注意してください。  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a>デバッグモードでこの設定を実行し、収集した計算 & 集計データを確認します。
1. [組織管理] > [電子申告] > [コンフィギュレーション] に移動します。
2. ツリーで、「Intrastat model」を展開します。
3. ツリーで、「Intrastat model\Intrastat (DE)」を選択します。
4. ツリーで、「Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'」を選択します。
5. アクション ウィンドウで、[設定] をクリックします。
6. [ユーザー パラメーター] をクリックします。
7. [デバッグモードの実行] フィールドで、[はい] を選択します。
8. [OK] をクリックします。
9. ページを閉じます。
10. [税] > [申告] > [対外貿易] > [イントラスタット] の順に移動します。
11. [出力] をクリックします。
12. [レポート] をクリックします。
13. [OK] をクリックします。
14. ページを閉じます。
15. [組織管理] > [電子申告] > [コンフィギュレーション] に移動します。
16. ツリーで、「Intrastat model」を展開します。
17. ツリーで、「Intrastat model\Intrastat (DE)」を選択します。
18. ツリーで、「Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'」を選択します。
19. [デバッグ ログ] をクリックします。
    * 選択した設定の実行に際して、デバッグのログ記録が作成されていることに注意してください。  
20. [添付] をクリックします。
21. [開く] をクリックします。
    * 選択した設定の実行中に収集された計算と集計の情報を含む作成済みのXMLファイルを確認します。  

