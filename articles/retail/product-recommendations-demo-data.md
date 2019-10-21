---
title: オムニ チャネル製品推奨事項のデモ データ
description: このドキュメントでは、事前設定されたカスタマイズ可能なデモ データを使用して、レベル 1 シングルボックス環境でのオムニ チャネル製品の推奨事項を活用する方法についてのガイダンスを提供します。
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 81af4c1bb7828c9b346a3ef514d8657e853dcefb
ms.sourcegitcommit: c526cfd1f823df1ff33ded95e599a72f0a15cc5a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2226139"
---
# <a name="omni-channel-product-recommendations-demo-data"></a>オムニ チャネル製品推奨事項のデモ データ

このドキュメントでは、事前設定されたカスタマイズ可能なデモ データを使用して、レベル 1 シングルボックス環境でのオムニ チャネル製品の推奨事項を活用する方法についてのガイダンスを提供します。

オムニ チャンネルの製品推奨事項は、編集上精選された、またはプログラムで生成された一連の製品一覧を提供します。 これらの一覧は、ビジネスのニーズに応じて、いくつかのシナリオで使用できます。 製品推奨事項一覧の詳細については、[製品推奨事項の概要](product-recommendaitons-overview.md)を参照してください。

レベル 2 およびそれ以上の Dynamics 環境では、製品推奨事項は顧客データに基づいて自動的に計算されます。
製品推奨事項のデモ データを使用しても、環境で既にプロビジョニングされている製品推奨ソリューション、およびその使用に関連するコストが無効になることはありません。

レベル 1 環境では、製品推奨事項は、csv ファイルに格納された静的デモ データのみに基づいています。

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>環境内の製品推奨事項デモ データの有効化

顧客はそれぞれの環境に **Dynamics 365 Commerce プレビュー デモ拡張機能**を配置する必要があります。これにより、製品推奨事項のデモ データが自動的に有効になります。

## <a name="default-demo-data"></a>既定のデモ データ
各 Onebox タイプの環境には、コンマで区切られた **' reco_demo_data '** ファイルに格納されたプリロード済の一連の製品推奨事項のデモ データが含まれ、Retail Server 上のこのドキュメントと同じフォルダーにあります。

このデータは、次の列に沿って構成されています。

| 列名         | 必須          | 説明                                                                                                                                 | 有効値                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| レコリスト            | :ヘビー_チェック_マーク: | デモ データ ポイントが生成する特定の製品推奨事項リスト タイプ。                                                    | <ul><li>レコベストセリング</li><li>レコニュー</li><li>レコトレンディング</li><li>レコカート</li><li>レコピーポーオールソーバイ</li></ul> |
| オペレーティングユニットナンバー | :ヘビー_チェック_マーク: | 製品推奨事項が提示される特定の作業単位番号。                                        |                                                                              |
| カテゴリ            |                    |    特定のリストが返されるカテゴリ。 カテゴリが指定されていない場合は、リストはナビゲーション階層の上部にのみ表示されます。    |                                                                              |
| SeedItemId          |                    |    シードを必要とするリスト (レコピーポーオールソーバイおよびレコカート) については、それらのリストの製品には追加の製品が表示されます。            |                                                                              |
| ItemIds             | :ヘビー_チェック_マーク: | **‘;’** で区切られ、結果として返される 1 つ以上の製品。                                                                  |                                                                              |


## <a name="customize-demo-data"></a>デモ データのカスタマイズ
顧客は、本社でコンフィギュレーションされた製品およびカテゴリ情報を使用して、既定のデモ データを編集できます。 CSV が更新されると、顧客に返される製品推奨事項に、その変更がすぐに反映されます。

拡張機能には、レコモックデータセット .csv と呼ばれるデータファイルが含まれています。これにより、顧客は、モックの推奨結果の出力に使用するデータセットを制御できます。 ファイル名は、**ext.Recommendations.DemoFilePath** 設定を使用して、拡張コンフィギュレーションによって制御できます。 これにより、コンフィギュレーション時に簡単に切り替えることができる複数のデータセットを顧客が利用できるようになります。

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a>追加リソース

[製品推奨事項の概要](product-recommendations-overview.md)

[環境計画](environment-planning.md)
