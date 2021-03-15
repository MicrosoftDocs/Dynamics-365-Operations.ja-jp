---
title: AI-ML ベースの製品推奨事項結果の調整
description: このトピックでは、人為的知能の機械学習 (AI-ML) に基づいて製品勧告の結果を調整する方法について説明します。
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: aab1b22b844ad14a94e1143f49b69f525d93f5b0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985914"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a>AI-ML ベースの製品推奨事項結果の調整


[!include [banner](includes/banner.md)]

このトピックでは、人為的知能の機械学習 (AI-ML) に基づいて製品推奨事項の結果を調整する方法について説明します。 

製品の推奨設定を有効にすると、既定の設定が有効になります。これらのパラメーターは、多くのニーズに対して機能する場合があります。 結果が製品の販売活動に適合しているかどうかを、評価するための計画を立てることをお勧めします。 再テストの前に、必要に応じてパラメーターを変更する前に、数日間結果を評価することをお勧めします。 

## <a name="understanding-recommendation-list-parameters"></a>推奨リスト パラメーターの理解

パラメーターを変更する前に、それらが以下の結果にどのように影響するかについて説明します。

### <a name="trending-product-list"></a>「トレンド」製品リスト

「トレンド」製品リストには、変更可能なパラメーターが 2 つあります。

![「トレンド」リストの既定パラメーターの例](./media/exampletrendingparameters.png)

1. **過去 X 日間の新製品を含める** - 現在の日付を使用して製品候補を選択できるようになるまで、指定した日数以内に追加された製品を表示します。 写真の既定値では、古いものから 180 日以内の製品はトレンド製品リストで使用されることが示されています。
1. **過去 X 日間の販売を含める** - 現在の日付を使用して製品を注文できるようになるまで、指定した日数以内に発生した販売取引を表示します。 この既定値では、過去 30 日以内の製品に対して行われたすべての購買が、トレンド製品リストでの製品の配置を決定するために使れることが提案されます。 

### <a name="best-selling-product-list"></a>「ベスト セラー」製品リスト

ビジネスに応じて、「ベスト セラー」リストは、トランザクション データを使用して製品を注文する場合でも、トレンドとは異なる結果をもたらします。 ベスト セラーは、品揃えの日付に基づいて中断しないのでまだ非常に人気があり、古い製品はトレンド リストから削除されている場合もあります。 

「ベスト セラー」製品リストには、変更可能なパラメーターが 1 つあります。

![ベスト セラー リストの既定パラメーターの例](./media/examplebestsellingparameters.PNG)

1. **過去 X 日間の販売を含める** - 現在の日付を使用して製品を注文できるようになるまで、指定した日数以内に発生した販売取引を表示します。 この既定値では、過去 30 日以内の製品に対して行われたすべての購買が、ベスト セラー製品リストでの製品の配置を決定するために使れることが提案されます。 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>推奨リストからの製品を手動で追加または削除

### <a name="for-new-trending-or-best-selling-lists"></a>「新規」、「トレンド」、または「ベスト セラー」リスト用

1.  **Retail と Commerce** > **製品推奨事項** > **推奨パラメーター** に移動します。
1.  共有パラメーターのリストで、**推奨リスト** を選択します。
1.  リストの追加または製品をリストから削除を選択します。
1.  テーブルに製品を追加するには、**行の追加** を選択します。 
1.  製品列で、**名前** または **製品番号** で製品を検索します。

    ![新しい製品リストでの製品の検索例](./media/examplenewlistconfiguration1.png)

1.  行タイプ列で、次の 2 つのオプションのいずれかを選択します。
    -   **含める**: 製品をリストの先頭に強制的に追加
    -   **除外** - リストに表示される製品を削除
    
    ![新しい製品リストに製品を含めるまたは除外する例](./media/examplenewlistconfiguration2.png)

1.  **表示順序** を変更して、**含める** とマークされた製品がリストに表示される順序を変更します。
    - 2 つの製品が同じ **表示順序** の値を持つ場合、これら 2 つの結果の最終的な順序は、バック オフィスとは異なる場合があります。
1.  テーブルから製品を削除するには: 削除する行を選び、**削除** を選択します。


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>「人気製品」「よく一緒に購入される」リスト用

「よく一緒に購入される」または「人気製品」リストのコンテキストでは、機械学習を使用してコンシューマー向け購入パターンを分析し、固有のシード製品に対して共通に購入した関連製品を推奨することができます。 
 
*シード製品* とは、結果を生成する製品です。 推奨リストを手動で調整するコンテキストでは、この製品の結果を追加または削除します。 

シード製品の結果を手動で追加または削除するには、次の手順に従います。
1.  **シード製品** を選択します。 
1.  **製品** 列の下で、**名前** または **製品番号** で製品を検索します。
![よく一緒に購入したリストで製品検索の例](./media/exampleFBTlistconfiguration1.png)
1. **行タイプ** 列で、次の 2 つのオプションのいずれかを選択します。
    - **含める**: 製品をリストの先頭に強制的に追加
    - **除外** - リストに表示される製品を削除     
![よく一緒に購入したリストの製品を含める、または除外する例](./media/exampleFBTlistconfiguration2.png)
1.  テーブルから製品を削除するには: 削除する行を選び、削除を選択します。


## <a name="additional-resources"></a>追加リソース

[製品推奨事項の概要](product-recommendations.md)

[Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する](enable-adls-environment.md)

[製品推奨事項の有効化](enable-product-recommendations.md)

[カスタマイズされた推奨事項の有効化](personalized-recommendations.md)

[カスタマイズされた推奨事項のオプト アウト](personalization-gdpr.md)

["類似したルックを買う" 推奨を有効にする](shop-similar-looks.md)

[POS での製品推奨事項の追加](product.md)

[トランザクション画面への推奨事項の追加](add-recommendations-control-pos-screen.md)

[収集された推奨事項の手動作成](create-editorial-recommendation-lists.md)

[推奨事項とデモ データの作成](product-recommendations-demo-data.md)

[製品推奨事項に関するよく寄せられる質問](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]