---
title: 製品推奨事項に関するよく寄せられる質問
description: この記事では、製品推奨事項またはその結果に関連する問題のトラブルシューティングに使用できる、プロセスおよびツールに関する情報を提供します。
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 77a5532ab1ae3b630bb335aa7cff6dc747184994
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900450"
---
# <a name="product-recommendations-faq"></a>製品推奨事項に関するよく寄せられる質問


[!include [banner](includes/banner.md)]

この記事では、[製品推奨事項](product-recommendations.md) またはその結果に関連する問題のトラブルシューティングに使用できる、プロセスおよびツールに関する情報を提供します。

## <a name="best-practices"></a>ベスト プラクティス
製品マスターとバリアントの概念を活用することは非常に重要です。 親製品マスターに対するバリアントの正確なグループ化は、リスト アルゴリズムとサービスがより良いモデルを作成するのに役立ちます。 さらにこのサービスは、密接に関係するすべてのバリアントをリストに含める代わりに、製品のインスタンスを 1 つだけ提供します。 密接に関係するすべてのバリアントがリストに追加されると、エラーまたは重複する結果が発生する可能性があります。

## <a name="why-are-products-missing-from-my-recommendation-lists"></a>製品が推奨リストに見つからないのはなぜですか。

通常、製品推奨リストに品目が含まれていない場合は、製品コンフィギュレーションに問題がある可能性があります。 たとえば、製品の開始日または終了日が正しくない場合や、分析コードの構成に誤りがある場合、または製品が正しいチャンネル品揃えに含まれていない場合などが考えられます。

人為的知能の機械学習 (AI-ML) に基づく推奨リストに品目が含まれていない場合、その品目は推奨リストの基準に適合していないか、推奨リストを表示するための十分な購入トランザクションがない可能性があります。

次の手順を確認することをお勧めします。
1. **製品推奨事項が本社で有効になっていることを確認します。** このサービスを有効にする方法の詳細については、[製品推奨事項の有効化](enable-product-recommendations.md)を参照してください。
1. **主要製品のプロパティが設定されていることを確認してください。** たとえば、製品の品揃えは **含める** ように設定する必要があります。
1. **新たに類別された製品については、製品が新しい一覧に表示されるまでに最大で 3 時間かかる場合があります。**
1. **製品がトレンド、ベストセラー、人気製品、またはよく一緒に購入されるものに表示されない場合、その製品に対して十分なトランザクションがない可能性があります。** この場合、さらにトランザクションが発生するのを待つか、既定の推奨リスト パラメーターを更新するか、手動操作で推奨製品リストの結果を変更します。 推奨パラメーターの詳細については、[AI-ML ベースの製品推奨事項の結果の管理](modify-product-recommendation-results.md)を参照してください。
1. **製品がリストの推奨基準を満たしていることを確認してください。** 製品推奨パラメーターの詳細については、[AI-ML ベースの製品推奨事項の結果の管理](modify-product-recommendation-results.md)を参照してください。

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a>低い推奨結果が返されないようにするにはどうすればよいでしょうか。

推奨リストは、結果を生成するために大量のトランザクションを必要とします。 したがって、ユーザーが完全なトランザクション履歴データを提供することが重要になってきます。

さらに、トランザクションがないか、トランザクションがほとんどない製品には、通常 **人気製品** または **よく一緒に購入される製品** のような結果も含まれません。また **トレンド** や **ベストセラー** の推奨リストにも表示されません。 この状況は、非常に新しい製品、または購入数が少ない古い製品でよく発生します。 人気のある新しい製品は、この問題を容易に解決できます。

次の手順を実行することをお勧めします。
1. **製品がそのリストの推奨基準を満たしていることを確認してください。** 製品推奨パラメーターの詳細については、AI-ML ベースの製品推奨事項の結果の変更を参照してください。
1. **製品が新しい場合は、製品のトランザクションがさらに増えるまで、推奨リストを変更することを検討してください。** 推奨リスト結果の変更方法の詳細については、[AI-ML ベースの製品推奨事項の結果の管理](modify-product-recommendation-results.md)を参照してください。


- **製品がそのリストの推奨基準を満たしていることを確認してください。** 製品推奨パラメーターの詳細については、[AI-ML ベースの製品推奨事項の結果の管理](modify-product-recommendation-results.md)を参照してください。
- **製品が新しい場合は、製品のトランザクションがさらに増えるまで、推奨リストを変更することを検討してください**。 推奨リスト結果の変更方法の詳細については、[AI-ML ベースの製品推奨事項の結果の管理](modify-product-recommendation-results.md)を参照してください。

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a>製品を削除しても、店舗でそれを閲覧することはできますか。

業務上の必要性に応じて、アルゴリズムによって生成されたリストを調整できます。 ただし、製品が推奨リストから削除された場合、その製品は店舗内で引き続き検出可能になります。 製品推奨事項の結果の変更方法の詳細については、[AI-ML ベースの製品推奨事項の結果の管理](modify-product-recommendation-results.md)を参照してください。

店舗での品目の検出をブロックする必要がある場合は、**品目分類** の値を **除外** に変更する必要があります。

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a>E コマース ページにリストを追加する方法はありますか。

製品推奨事項ページを E コマース Web サイトに追加する方法の詳細については、[製品推奨リストをページに追加する](./product-recommendations.md)を参照してください。

## <a name="how-do-i-enable-recommendations-on-pos"></a>POS で推奨事項を有効にするにはどうすればよいですか。

製品の推奨事項を有効にした後、制御 POS 画面に推奨事項パネルを追加する必要があります。 詳細については、[POS デバイスのトランザクション画面に推奨事項コントロールを追加](add-recommendations-control-pos-screen.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[製品推奨事項の概要](product-recommendations.md)

[Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する](enable-adls-environment.md)

[製品推奨事項の有効化](enable-product-recommendations.md)

[カスタマイズされた推奨事項の有効化](personalized-recommendations.md)

[カスタマイズされた推奨事項のオプト アウト](personalization-gdpr.md)

["類似したルックを買う" 推奨を有効にする](shop-similar-looks.md)

[POS での製品推奨事項の追加](product.md)

[トランザクション画面への推奨事項の追加](add-recommendations-control-pos-screen.md)

[AI-ML 推奨事項結果の調整](modify-product-recommendation-results.md)

[収集された推奨事項の手動作成](create-editorial-recommendation-lists.md)

[推奨事項とデモ データの作成](product-recommendations-demo-data.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]