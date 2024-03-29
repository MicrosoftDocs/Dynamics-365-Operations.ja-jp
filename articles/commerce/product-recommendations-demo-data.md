---
title: 推奨事項とデモ データの作成
description: この記事には、事前設定されたカスタマイズ可能なデモ データを使用して、レベル 1 シングル ボックス環境でのオムニチャネル製品の推奨事項を活用する方法についてのガイダンスが含まれます。
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7e3df414b3c16c28b6f5ca04f765d91c1312ada4
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459971"
---
# <a name="create-recommendations-with-demo-data"></a>推奨事項とデモ データの作成

[!include [banner](includes/banner.md)]

この記事には、事前設定されたカスタマイズ可能なデモ データを使用して、レベル 1 シングル ボックス環境でのオムニチャネル製品の推奨事項を活用する方法についてのガイダンスが含まれます。

オムニ チャネルの製品推奨事項は、編集上精選された、またはプログラムで生成された製品一覧を提供します。 これらの一覧は、ビジネスのニーズに応じて、いくつかのシナリオで使用できます。 製品推奨事項一覧の詳細については、[製品推奨事項の概要](product-recommendations.md) を参照してください。

レベル 2 およびそれ以上の Dynamics 365 環境では、製品推奨事項は顧客データに基づいて自動的に計算されます。 製品推奨事項のデモ データを使用しても、環境で既にプロビジョニングされている製品推奨ソリューション、およびその使用に関連するコストが無効になることはありません。

レベル 1 環境では、製品推奨事項は、.csv ファイルに格納された静的デモ データのみに基づいています。

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>環境内の製品推奨事項デモ データの有効化
製品推奨事項デモ日付を有効にするには、それぞれの環境に Dynamics 365 Commerce プレビュー デモ拡張機能を配置する必要があります。 これを行うと、製品推奨事項デモ データが自動的に有効になります。

## <a name="default-demo-data"></a>既定のデモ データ
各 OneBox タイプの環境には、コンマで区切られた 'reco_demo_data.csv' ファイルに格納されたプリロード済の一連の製品推奨事項のデモ データが含まれ、Commerce Scale Unit 上にあります。

データは、次の列に沿って構成されています。

| 列名         | 必須          | 説明                                                                                                                                 | 有効値                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| レコリスト            | :ヘビー_チェック_マーク: | デモ データ ポイントが生成する、特定の製品推奨事項リスト タイプ。                                                    | <ul><li>レコベストセリング</li><li>レコニュー</li><li>レコトレンディング</li><li>レコカート</li><li>レコピーポーオールソーバイ</li><li>RecoPicks</li><li>RecoSlarlarVisual</li><li>RecoSlarlarTextual</li></ul> |
| オペレーティングユニットナンバー | :ヘビー_チェック_マーク: | 製品推奨事項が提示される特定の作業単位番号。                                        |                                                                              |
| カテゴリ            |                    |    特定のリストが返されるカテゴリ。 カテゴリが指定されていない場合、リストはナビゲーション階層の上部にのみ表示されます。    |                                                                              |
| SeedItemId          |                    |    シードを必要とするリスト (RecoPeopleAlsoBuy および RecoCart) については、それらのリストの製品には追加の製品が表示されます。            |                                                                              |
| CustomerId          |                    |    顧客識別子 (RecoPicks) を必要とするリスト。  既定値 ' 0 ' はすべての顧客に適用されます。          |                                                                              |
| ItemIds             | :ヘビー_チェック_マーク: | 「;」で区切られ、結果として返される 1 つ以上の製品。                                                                  |                                                                              |

## <a name="customize-demo-data"></a>デモ データのカスタマイズ
本社でコンフィギュレーションされた製品およびカテゴリ情報を使用して、既定のデモ データを編集できます。 .csv を更新すると、顧客に返される製品推奨事項は変更をすぐに反映します。

拡張機能には、'RecoMockDataset.csv' と呼ばれるデータファイルが含まれています。これによりモックの推奨結果の出力に使用するデータセットを制御できます。 ファイル名は、**ext.Recommendations.DemoFilePath** 設定を使用して、拡張コンフィギュレーションによって制御できます。 これにより、コンフィギュレーション時に簡単に切り替えることができる複数のデータセットを利用できるようになります。


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

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

[製品推奨事項に関するよく寄せられる質問](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
