---
title: "原価管理ホーム ページ"
description: "原価管理では、原材料、半完成品、完成品、および進行中の作業資産の評価および会計処理ができます。"
author: AndersGirke
manager: AnnBe
ms.date: 02/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cab2f165a70e5ce8f09f0391282e055e51afb225
ms.openlocfilehash: b1513e5a7cb3a19fd3743a5aac8efd211aa02ce8
ms.contentlocale: ja-jp
ms.lasthandoff: 02/21/2018

---

# <a name="cost-management-home-page"></a>原価管理ホーム ページ

[!include[banner](../includes/banner.md)]

[原価管理 (ビデオ)](https://www.youtube.com/watch?v=vXzlC-mOBcg&feature=youtu.be) では、原材料、半完成品、完成品、および進行中の作業資産の評価および会計処理が使用できます。 これは定義、管理、および [在庫会計](cost-object.md) と [製造の会計](bom-calculations.md)のレポートのプロセスです。

次の領域で、原価ポリシーを定義できます。 
-  [あらかじめ設定された原価](costing-versions.md)
-  [在庫会計](cost-object.md)
-  [製造の会計](bom-calculations.md)
-  [間接原価の会計](costing-sheets.md)
-  [元帳統合](production-order-cost-analysis.md)

たとえば、在庫会計の [品目モデル グループ](../inventory/reserve-inventory-quantities.md) で商品に適用する [FIFO](fifo-physical-value-marking.md)、[加重平均](weighted-average-physical-value-marking.md)、[標準原価](prerequisites-standard-costs.md)、または [移動平均](moving-average.md) など、在庫評価方法を定義できます。

**原価管理** および **コスト分析** ワークスペースから、在庫会計および製造の会計にアクセスできます。 これらのワークスペースは、現在のステータス、主要業績評価指標 (KPI)、および誤差検出の包括的な概要を提供します。 

製造の会計では、製造オーダーおよびバッチ オーダーで [作業オーダー原価計算](production-order-cost-analysis.md)、さらにリーン生産で [一括引き落とし原価計算](backflush-costing.md) の処理ができます。

[原価管理 Power BI コンテンツ](../../dev-itpro/analytics/cost-management-content-pack.md) では、在庫および仕掛品 (WIP) 在庫の管理上の情報、および時間経過に伴ってカテゴリごとに原価がどのように流れているかを示します。 この情報は、財務諸表の詳細な補足情報として使用できます。

### <a name="additional-resources"></a>その他のリソース

#### <a name="whats-new-and-in-development"></a>新機能および開発中の機能

リリースされた新機能と開発中の新機能については、[Microsoft Dynamics 365 ロードマップ](https://roadmap.dynamics.com/)を参照してください。 

#### <a name="white-paper"></a>ホワイト ペーパー
[原価計算表を使用した BOM 計算](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/white-papers/365operationsbomcalsheet) では、材料と製造を含む原価計算表を設定する方法と、その設定が BOM 計算の結果に及ぼす影響について説明しています。 トピックをより良く説明するため、さまざまな設定およびコンフィギュレーションの影響を示す、具体的なシナリオとデータを提供します。 このドキュメントはコンフィギュレーションするための十分な詳細を提供していないため、ユーザーがこれらすべてのシナリオに従うことはできないと思います。 しかし、基本的な知識がある場合は、下の一覧に表示される順に従ってタスク ガイドを再生してみてください。 BOM 計算の分析をするには、このドキュメントを読み取って得た知識を活用してください。 

-  [完成品の作成](tasks/create-finished-product-2016-02.md)
-  [半完成品の作成](tasks/create-semi-finished-product-2016-02.md)
-  [原材料の作成](tasks/create-raw-materials-2016-02.md)
-  [BOM の作成](tasks/create-boms-2016-02.md)
-  [工順の作成](tasks/create-routes-2016-02.md)
-  [単一レベル構造を使用した BOM の計算](tasks/calculate-bom-single-level-structure-2016-02.md)
-  [複数レベル構造を使用した BOM の計算](tasks/calculate-bom-multilevel-structure-2016-02.md)


#### <a name="blogs"></a>ブログ
[Dynamics AX Manufacturing R&D Team Blog (Dynamics AX 製造研究開発チーム ブログ)](https://blogs.msdn.microsoft.com/axmfg) および [Supply Chain Management in Dynamics AX R&D Team Blog (Dynamics AX のサプライ チェーン マネジメント研究開発チーム ブログ)](https://blogs.msdn.microsoft.com/dynamicsaxscm) で、原価管理に関する意見、ニュース、その他の情報を見つけることができます。 これらの投稿の一部は原価管理の以前のバージョンに関して書かれていますが、現在のバージョンでも同じ概念を適用でき、手順も類似しています。

#### <a name="task-guides"></a>タスク ガイド
Finance and Operations には、タスク ガイドとして使用できる追加のヘルプが用意されています。 タスク ガイドにアクセスするには、ページの [ヘルプ] ボタンをクリックします。


