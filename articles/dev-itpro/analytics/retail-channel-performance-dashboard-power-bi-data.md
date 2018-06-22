---
title: "販売チャネル パフォーマンス Power BI コンテンツ"
description: "このトピックでは、Dynamics AX 7.0 リリースの Retail チャネル パフォーマンス Power BI コンテンツに関する情報を提供します。 このコンテンツ パックを使用すると、チャネル パフォーマンス アナリティクスを迅速にビルドして、販売実績に基づいて傾向を予測し、洞察を得ることができます。"
author: ashishmsft
manager: AnnBe
ms.date: 02/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 105483
ms.assetid: cb5aff3b-5b29-44f7-9c6f-6b055c043996
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 8218df7b0c64a2b83a64b1884f2b3f2600768be6
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="retail-channel-performance-power-bi-content"></a>販売チャネル パフォーマンス Power BI コンテンツ

[!include [banner](../includes/banner.md)]

> [!Note]
> このコンテンツ パックは [Power BI コンテンツ パックを PowerBI.com に公開する](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features#power-bi-content-packs-published-to-powerbicom)で記載されたものとして非推奨になっています。

このトピックでは、Dynamics AX の Retail チャネル パフォーマンス Power BI コンテンツに関する情報を提供します。 このコンテンツ パックを使用すると、チャネル パフォーマンス アナリティクスを迅速にビルドして、販売実績に基づいて傾向を予測し、洞察を得ることができます。

Retail チャンネル パフォーマンス コンテンツ パックを使用すると、チャネル パフォーマンスの分析機能をすばやく作成することができます。 コンテンツ パックは、販売実績に焦点を当てて傾向を予測し、洞察を明らかにするチャネル マネージャー専用に設計されています。 そのコンポーネントは、Dynamics AX データベースで Retail と Commerce のデータから直接を取得し、従業員、カテゴリ、製品、ターミナル、チャネルなどによって地理的に世界中の組織全体の販売実績に関するドリルダウン レポートを提供します。 Power BI は、小売およびコマース データを調査して分析するための良い出発点となる、レポートとダッシュボードに自動的に作成します。 この記事には、次の情報が含まれています。

-   Power BI の Retail チャネル パフォーマンス コンテンツ パックを Dynamics AX データ ソースに接続する方法について説明します。
-   小売チャネルの実績に関する詳細情報を提供するレポートの一覧を表示します。
-   コンテンツ パックの既存のレポートを変更して自分で作成する方法について説明します。
-   Power BI でのエクスペリエンス全体を有効にする実際のデータ モデルのほんの一部を取得します。

## <a name="connect-the-retail-channel-performance-content-pack-in-power-bi-to-a-dynamics-ax-data-source"></a>Power BI の小売チャネル パフォーマンス コンテンツ パックを Dynamics AX データ ソースに接続する
1.  https://www.powerbi.com に移動し、**サインイン**をクリックします。 アカウントがない場合は、サインアップし、新しい Power BI を無料でプレビューできます。
2.  サインインするには、Power BI アカウントを持つ Microsoft Office 365 アカウントを入力します。
3.  ワークスペースが表示されたら、左のナビゲーション ウィンドウの下部にある**データの取得**をクリックします。
4.  **サービス** セクションで、**取得**をクリックします。
5.  スクロールするか検索して **Microsoft Dynamics AX Retail チャネル パフォーマンス** を見つけ、**今すぐ入手** をクリックします。
6.  次の形式に Dynamics AX の URL を入力します `https://<tenant>.cloudax.dynamics.com` (たとえば、`https://YourAOSTenant.cloudax.dynamics.com`)。 次に、**Next** をクリックして Dynamics AX データ ストレージからこの Power BI ダッシュボードにデータをプルします。
7.  認証方法として **oAuth2** を選択し、**署名する** をクリックします。
8.  サインインするには、Dynamics AX 環境にアクセスするアクセス許可を持つ Office 365 のアカウントを入力します。
9.  データが Dynamics AX から Power BI に正常に引き込まれた後、左のナビゲーション ウィンドウで**小売チャネルの実績ダッシュボード**をクリックして、Power BI の個人の**小売チャネルの実績**を表示することができます。 [![小売チャンネル パフォーマンス ダッシュボード](./media/rcmpbidashboard-1024x679.png)](./media/rcmpbidashboard.png)
10. 自然言語を使用することにより、Power BI 内の Q&A フィーチャーを活用して Dynamics AX の営業データをクエリすることができます。 [![Power BI にある Q&A 機能](./media/qnapbiretailchannelperformance.png)](./media/qnapbiretailchannelperformance.png)

## <a name="view-a-list-of-reports"></a>レポートの一覧の表示
ダッシュボードの固定されたタイルのいずれかをクリックすると、小売チャネルの実績に関する情報を提供する次の一覧に移動できます。

-   地理的な販売配布
-   カテゴリ販売実績
-   支払/入金タイプまたは支払方法ごとの売上集計
-   従業員の月次パフォーマンス
-   店舗の月次パフォーマンス
-   特定の店舗での特定のカテゴリにおける製品の販売実績

たとえば、地理的な販売流通のより深い分析を実行する場合があります。 

[![地理的販売配送レポート](./media/slicendicegeographicalsalesdata-1024x715.png)](./media/slicendicegeographicalsalesdata.png)

## <a name="modify-an-existing-report-in-the-content-pack-to-make-it-self-authored"></a>コンテンツ パックの既存のレポートを変更して自分で作成する
コンテンツ パックの既存のレポートを変更して自己作成できるようにする簡単な例を次に示します。 この例では、**カテゴリおよび製品のパフォーマンス**という名前の既存のレポートを、そのレポートの**カテゴリ レベル 1** を**月 / 年ごとの合計金額**グラフに追加することで変更します。

1.  ウィンドウの下部にある **CategoryProductPerformance** タブをクリックし、**カテゴリ、および製品のパフォーマンス** レポートを開きます。次に、**レポートの編集**をクリックします。 [![レポートの編集](./media/editreport-1024x580.png)](./media/editreport.png)
2.  **月/年ごとの合計金額** というグラフを選択します。 その後、ウィンドウの右側の **Fields** ウィンドウで、**既定小売品目カテゴリ階層** ノードを展開します。 [![月/年グラフによる合計金額の既定小売品目カテゴリ階層ノード](./media/editreportstep2-1024x624.png)](./media/editreportstep2.png)
3.  この階層のカテゴリ レベルの一覧で**カテゴリ レベル 1** を選択します。 **月/年とカテゴリ レベル 1 グラフごとの合計金額** に変更するためにこの属性を選択したグラフの名前。このグラフでは、各カテゴリの売上シェアを毎月表示します。 [![月 / 年とカテゴリレベル 1 グラフごとの合計金額](./media/editreportstep3-1024x625.png)](./media/editreportstep3.png)
4.  最後に、視覚化自体を変更するようにしてください。 **月/年とカテゴリ レベル 1 ごとの合計金額** グラフを選択し、**ビジュアル化** ウィンドウで **面グラフ** または **積み上げ面グラフ** をクリックして結果を確認します。 [![月/年およびカテゴリレベル 1 のグラフによる合計金額の視覚化の変更](./media/editreportstep4-1024x630.png)](./media/editreportstep4.png)

## <a name="get-a-glimpse-of-the-actual-data-model"></a>実際のデータ モデルのほんの一部を取得します
Dynamics AX データ エンティティおよび集約データ エンティティのコンテンツ パックに含まれているデータ モデルを使用すると、さまざまな分析コードを使用してさまざまな測定間でスライスおよびダイスすることができます。 [![データ モデル](./media/datamodeltomakeslicingndicingpossibleinrcm-1024x600.png)](./media/datamodeltomakeslicingndicingpossibleinrcm.png)

<a name="additional-resources"></a>その他のリソース
--------

[Power BI 統合](power-bi-integration.md)

[ワークスペースの Power BI 統合のコンフィギュレーション](configure-power-bi-integration.md)




