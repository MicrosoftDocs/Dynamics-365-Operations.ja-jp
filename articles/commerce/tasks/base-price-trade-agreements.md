---
title: 基準価格と売買契約
description: この手順では、チャンネル固有の販売価格の売買契約の作成方法を説明します。
author: josaw1
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 282cbe0cb115d6204137613f4754068b8a9a321400d24808eb67266a83d7bcc6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730734"
---
# <a name="base-price-and-trade-agreements"></a>基準価格と売買契約

[!include [banner](../includes/banner.md)]

この手順では、チャンネル固有の販売価格の売買契約の作成方法を説明します。 この手順では、デモ データの会社 USRT を使用します。

1. **ナビゲーション ウィンドウ** で、**モジュール > Retail と Commerce > 価格と割引の管理 > 価格グループ > すべての価格グループ** の順に移動します。 価格グループは、売買契約を特定のチャネルに割り当てる方法です。 価格グループを使用して、チャンネル固有の価格設定が可能なチャンネルに売買契約を割り当てます。  
2. **新規** をクリックします。
3. **価格グループ** フィールドに値を入力します。
4. **名前** フィールドに値を入力します。
5. **保存** をクリックします。
6. ページを閉じます。
7. **ナビゲーション ウィンドウ** で、**モジュール > Retail と Commerce > チャネル > 店舗 > すべての店舗** に移動します。
8. 一覧で「ニューヨーク」を選択します。
9. アクション ウィンドウで、**店舗** をクリックします。
10. **価格グループ** をクリックします。
11. **新規** をクリックします。
12. **価格グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
13. 一覧で、目的のレコードを見つけ、選択します。
14. **保存** をクリックします。
15. ページを閉じます。
16. ページを閉じます。
17. **ナビゲーション ウィンドウ** で、**モジュール > Retail と Commerce > 製品とカテゴリ > カテゴリ別リリース済製品** の順に移動します。
18. 一覧で、選択された行のリンクをクリックします。
19. **編集** をクリックします。
20. **販売** クイック タブを展開します。
21. **価格** フィールドに数値を入力します。 この価格は、適用できる売買契約がない場合に使用されます。  
22. **保存** をクリックします。
23. **アクション ウィンドウ** で、**販売** をクリックします。
24. **売買契約** をクリックします。
25. **新規** をクリックします。
26. **名前** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
27. 一覧で、**Commerce** を選択します。 デモ データで、**Commerce** 仕訳帳名の既定のリレーションは **価格 (販売)** です。 これは、作成されたすべての新しい明細行が、販売価格の売買契約の既定値であることを意味します。  
28. **アクション ウィンドウ** で、**明細行** をクリックします。
29. **関係者コード タイプ** フィールドで、'グループ' を選択します。
30. **勘定の選択** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
31. 一覧で、目的のレコードを見つけ、選択します。 これによって、チャンネルから価格グループ、売買契約へのリンクが完了します。  
32. **商品関係** フィールドに値を入力します。
33. **通貨金額** フィールドに数値を入力します。
34. **詳細** クイック タブで、**次を検索** チェックボックスをオンまたはオフにします。 **次を検索** が 'はい' に設定されている場合、価格決定エンジンは販売価格の低い適用できる売買契約を検索し続けます。 **次を検索** が 'いいえ' に設定されている場合、価格エンジンは検索を中止し、その売買契約を使用します。  
35. **転記** をクリックします。
36. **OK** をクリックします。
37. ページを閉じます。
38. **アクション ウィンドウ** で販売をクリックします。
39. **販売価格** をクリックします。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]