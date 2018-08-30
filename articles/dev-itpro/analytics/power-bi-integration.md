---
title: "Power BI 統合によって利用できる機能とサービス"
description: "このトピックでは、Microsoft Power BI に含まれる機能およびサービスを使用して、データからのインサイトにアクセス、参照、取得する方法を説明します。"
author: TJVass
manager: AnnBe
ms.date: 02/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: PowerBIConfiguration
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 31001
ms.assetid: bf6eff60-4a30-4338-a55f-1f2a97d3debe
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: c30cb7ac34d01dddf1b7bab79076c53c0f5b2b37
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="features-and-services-available-through-power-bi-integration"></a>Power BI 統合によって利用できる機能とサービス

[!include [banner](../includes/banner.md)]

Microsoft Power BI は、データを分析して情報を共有できる一連のビジネス分析ツールです。 Power BI ツールを使用することにより、データを検証し豊富なレポートおよびダッシュボードをすばやく作成できます。 ユーザーおよび同僚は任意のデバイス上で対話的にレポートを使用することができます。 Microsoft Dynamics 365 for Finance and Operations は、データ検索に Power BI を使用します。

## <a name="data-exploration-through-power-bi"></a>Power BI を使用しデータを検索
Finance and Operations にはさまざまなタイプのレポートがあります。

![データ検索](./media/data-exploration.png)

Chart コントロールは、ビジュアルを必要とする埋め込みエクスペリエンスをビルドするために使用されます。

Microsoft SQL Server Reporting Services (SSRS) は、多くの場合に印刷が必要となるピクセル パーフェクトに書式設定されたレポートのために設計されたエンジンです。 請求書や発注書などの文書スタイル レポートには SSRS を使用しています。 SSRS 統合への投資は、ドキュメントの生成および印刷のシナリオに焦点を当てています。

すべてのドキュメント以外のレポートまたは印刷する必要がないレポートに関しては、Power BI を採用します。
 
過去には、_セルフ サービス レポート_および_アドホック レポート_といった用語で Power BI について言及していました。 ここで、_data exploration_ という用語を使用します。 この用語の変更は、パラダイムの微妙な変化を反映しています。 セルフ サービス レポートは、ユーザーが自分で作成したレポートです。 (または、パワー ユーザーがレポートを作成して他のユーザーと共有しました。 その後、これらのユーザーは、要件に応じてレポートを調整し続けました。多くの場合、グラフの形状を変更したり、新しい列を追加したり、グループを変更したり、新しいデータ ビューを作成したりしなければなりませんでした。 結果を報告書として考えるかもしれませんが、ユーザーはデータを調べ、列の周りをピボットし、グラフの形を変えたりして、ただ理解しようとしているだけです。 過去のテクノロジでは、ユーザーは大量のデータを対話的に参照できません。 したがって、ユーザーは「レポート」、または同じデータの多くのビューを作成する必要がありました。

Power BI では、Microsoft SQL Server のメモリ内データベース テクノロジーにより、レポートはインタラクティブなデータ探索の開始点にすぎません。 Power BI レポートのグラフは、ユーザーにクリックを促し、ビジュアルの形状を対話的に変更し、データを簡単にフィルタリングすることができます。 簡単に既存のレポートを調整したり、独自のデータ ビューを作成したりできます。 レポートを共有して、チームがデータ上でコラボレーションできます。

したがって、Power BI コンポーネントを参照するには _report_ という用語を使用することもできますが、より大きなシナリオを検討する必要があります。 ユーザーはデータを探索しています! Power BI は、データの調査と視覚化の要件に対応する必要があるときに選択できるツールです。

Finance and Operations で概念をレポートする詳細ディスカッションについては、[情報へのアクセスとレポート](information-access-reporting.md) を参照してください。

## <a name="ready-made-power-bi-content"></a>既存の Power BI コンテンツ
既製の Power BI レポートをすぐに使用することができます。 2 種類の Power BI コンテンツを利用できます。

- Microsoft Dynamics Lifecycle Service (LCS) で使用可能な Power BI コンテンツ
- PowerBI.com マーケットプレースで配布される Power BI コンテンツ パック

バージョンによっては、両方のタイプのコンテンツのいずれかを使用できます。

### <a name="power-bi-content-that-is-available-in-lcs"></a>LCS で使用できる Power BI コンテンツ
LCS は、Finance and Operations の環境を管理できるサービスです。 LCS は Microsoft によって運用されています。 Power BI レポートは、エンティティ格納を使用して開発され、実装資産として LCS で配分されます。 LCS では、Microsoft が開発するコンテンツだけでなく、独立系ソフトウェア ベンダー (ISV) とパートナーが開発するコンテンツも確認できます。

エンティティ格納に基づく Power BI コンテンツを引き続きリリースします。 詳細については、[Roadmap](https://roadmap.dynamics.com) を参照してください。

### <a name="power-bi-content-packs-that-are-distributed-in-the-powerbicom-marketplace"></a>PowerBI.com マーケットプレースで配布される Power BI コンテンツ パック
PowerBI.com マーケットプレースには Power BI コンテンツ パックがいくつかあります。 これらのコンテンツ パックは通知があるまで引き続きサポートされますが、コンテンツ パックの将来の投資はエンティティ格納に基づき、またコンテンツは LCS 経由でリリースされます。

コンテンツの詳細については、[Power BI コンテンツ](power-bi-home-page.md) を参照してください。

## <a name="extending-creating-and-distributing-power-bi-reports"></a>Power BI レポートの拡張、作成、配布
最初のステップとして、既製の Power BI コンテンツを使用する必要があります。 既製のレポートを変更したり、PowerBI.com に組み込まれている機能を使用して、それらを拡張することができます。 既製のレポートを変更するだけでなく、Power BI desktop などの Power BI オーサリング ツールを使用して拡張することができます。 新しいレポートを作成することもできます。 いくつかの方法を使用して、新しい Power BI レポートを作成することができます。

### <a name="creating-high-volume-near-real-time-operational-power-bi-reports-by-using-entity-store"></a>エンティティ格納を使用して大量の、ほぼリアルタイムな「運用 Power BI レポート」を作成しています
エンティティ格納は、Power BI 統合用に組み込まれている運用データ ストアです。 エンティティ ストアを使用するほぼリアルタイムの大量の Power BI レポートを作成するには、ビジネス アナリストまたは開発者は Power BI レポートのオーサリングツールである Power BI デスクトップを使用できます。 開発者が作成するその他のコンポーネントと同様に、これらのレポートは LCS 経由でユーザーに配布する必要があります。

エンティティ格納を使用して作成されるレポートは、DirectQuery テクノロジを利用します。 この技術により、大量のデータに対するレポートを作成できます。 DirectQuery テクノロジを使用して作成されるレポートは、PowerBI.com サービスにデータをキャッシュしません。 代わりに、データは常に Finance and Operations に保存されます。

エンティティ格納と Power BI 統合の概要については、[エンティティ格納と Power BI の統合の概要](power-bi-integration-entity-store.md) を参照してください。 

Microsoft Dynamics AX 2012 をアップグレードする場合は、エンティティ店舗を使用する集計測定にキューブをアップグレードすることができます。 エンティティ格納を使用して、Power BI レポートを作成することができます。 詳細については、[アップグレードした Dynamics AX 2012 R3 販売キューブをエンティティの店舗へ移行する](../migration-upgrade/migrate-upgraded-cube-entity-store.md) を参照してください。

### <a name="creating-power-bi-reports-by-using-excel"></a>Excel を使用して Power BI レポートを作成しています
Power BI desktop オーサリング ツールの使用に加えて、Excel に採用されている「Power ツール」を使用して視覚エフェクトを作成できます。 組織には、既に Excel を毎日使用している多くのユーザーが存在する可能性があります。 クイック「1 回限り」レポートでは、Excel はこれらのユーザーに対して最適なオプションである可能性があります。

Excel を使用できるシナリオはいくつかあります。

- Dynamics 365 のページから Excel にデータをエクスポートします。 Excel 内に組み込まれた Power View アドインを使用して、データを視覚化することができます。 Excel ブックは、スタンドアロンのビジュアル化として使用できます。 さらに、PowerBI.com サービスにレポートをインポートすることができます。
-   別のワークシートのデータ (または OData エンドポイントからインポートされたデータ) と外部データとを結合するには、Excel の Power Query 拡張機能を使用します。 Power View を使用すると、結果データを視覚化できます。
- 大量のデータを Excel に取り込むには、Excel の PowerPivot 拡張機能を使用します。

アドホックな「1 回限り」のレポートには、Excel のエクスポート機能を使用することを検討してください。 レポートをユーザー グループと共有する場合、エンティティの店舗を使用してそれらを作成することを検討する必要があります。

## <a name="sharing-and-using-reports-in-powerbicom"></a>PowerBI.com でレポートを共有して使用
PowerBI.com は、Microsoft が提供するサービスです。 これにより、ダッシュボードおよびレポートを作成することができ、ユーザーのグループと共同作業することもできます。 レポートを作成する方法に関係なくに、PowerBI.com サービスにアップロードすることで、ユーザーとレポートを共有できます。 (このプロセスは_公開_とも呼ばれます。)

レポートをアップロードした後、ユーザーは Web 上で (自宅またはオフィスでインターネットに接続されている場合) またはデバイス上のアプリを使用して表示、調整、検索することができます。

Power BI の概念の詳細については、[Power BI ドキュメント](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-how-should-i-share-my-dashboard/) を参照してください。

## <a name="pinning-power-bi-content-to-the-finance-and-operations-client"></a>Finance and Operations クライアントに Power BI コンテンツを固定
PowerBI.com は、組織または業務単位のレポートおよびダッシュ ボード ソリューションとして独自に使用できます。 ただし、ユーザーは自分の PowerBI.com アカウントから Finance and Operations のワークスペースにタイルおよびレポートをピン留めすることもできます。 Dynamics 365 の Power BI コンテンツは、事業運営に関連するコンテキスト インサイトを提供します。

PowerBI.com ダッシュボード内の PowerBI.com: タイル、およびレポートから、2 つのタイプのオブジェクトをピン留めすることができます。

Power BI コンテンツを固定する前に、Dynamics 365 環境で Power BI をコンフィギュレーションする必要があります。

### <a name="one-time-configuration-of-powerbicom-integration"></a>PowerBI.com 統合の一時コンフィギュレーション
タイルまたはレポートを固定する前に、管理者は Finance and Operations 環境で PowerBI.com との統合を構成する必要があります。 この構成は、環境ごとに 1 回だけ実行する必要があります。 手順については、「[ワークスペースの Power BI 統合のコンフィギュレーション](configure-power-bi-integration.md)」を参照してください。

### <a name="pinning-powerbicom-tiles"></a>PowerBI.com タイルを固定
Dynamics 365 クライアントに固定されている Power BI タイルは、わかりやすいビジュアルの概要を提供します。 ユーザーは、対話型分析 PowerBI.com を開くこともできます。 詳細については、「[ワークスペースの Power BI 統合のコンフィギュレーション](configure-power-bi-integration.md)」を参照してください。

### <a name="pinning-powerbicom-reports-to-workspaces"></a>PowerBI.com レポートをワークスペースにピン留めする
パワー ユーザー、ビジネス アナリスト、または開発者は、 Power BI デスクトップを使用してエンティティ格納を使用するレポートを作成できます。 これらのレポートは豊富で対話型であるだけではなく、ユーザーは他のユーザーに依存することがなく変更することができます。

PowerBI.com 内のレポートは強力かつ独自での対話型ではありますが、ワークスペースに固定することもできます。 ユーザーは自身で、レポートをワークスペースにピン留めできます。 ワークスペースにレポートをピン留めする方法の詳細については、[Power BI レポートをワークスペースにピン留めする](pin-power-bi-reports.md) を参照してください。

