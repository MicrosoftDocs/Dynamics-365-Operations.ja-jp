---
title: "Power BI レポートをワークスペースにピン留めする"
description: "Microsoft Dynamics 365 for Finance and Operations は、データ検索に Power BI を使用します。 このトピックでは、Finance and Operations のワークスペースにページ全体の Power BI レポートを配置して、ユーザーにインタラクティブなデータ探索エクスペリンスを提供する方法について説明します。"
author: MilindaV2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 265844
ms.assetid: a0011a12-a1eb-46bd-8d28-e532fec14e09
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: a4dc28f7f4c6fb2683dddac80144f5ab447e5a33
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="pin-power-bi-reports-to-workspaces"></a>Power BI レポートをワークスペースにピン留めする

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations は、データ検索に Power BI を使用します。 このトピックでは、Finance and Operations のワークスペースにページ全体の Power BI レポートを配置して、ユーザーにインタラクティブなデータ探索エクスペリンスを提供する方法について説明します。

このトピックは、Microsoft Power BI タイルをワークスペースにピン留めする機能に精通しているものと仮定します。 詳細については、「[Power BI 統合](power-bi-integration.md)」を参照してください。 ユーザーがワークスペースを作成している開発者であり、ユーザーに Power BI をワークスペースにピン留め並べしてもらうには、Power BI コントロールを埋め込みます。

## <a name="pin-power-bi-reports-to-workspaces"></a>Power BI レポートをワークスペースにピン留めする
Microsoft Dynamics AX プラットフォーム更新プログラム 1 (2016 年 5 月) では、Power BI レポートをワークスペースにピン留めする機能が導入されました。 Power BI レポートは、**リンク** セクションが含まれる任意のワークスペースに追加できます。 つまり、製品に含まれた最初から用意されているワークスペースのほとんどにレポートを追加できます。 Power BI のレポートとタイルを有効にするには、Power BI が Microsoft Dynamics 365 for Finance and Operations と連携するように構成する必要があります。 この 1 回限りの操作は、Dynamics 365 for Finance and Operations 環境の管理者が完了する必要があります。 手順については、「[ワークスペースの Power BI 統合のコンフィギュレーション](configure-power-bi-integration.md)」を参照してください。 Dynamics 365 for Finance and Operations と連携するように Power BI をコンフィギュレーションした後、クライアントの**元帳予算および予測**ワークスペースを開きます。 ワークスペースで、**オプション** タブをクリックします。このタブには (Power BI) タイル カタログと (Power BI) レポート カタログを開くボタンが含まれています。 **レポート カタログを開く**をクリックします。 レポートの一覧を示すダイアログ ボックスが表示されます。 レポートのリストは、Power BI アカウントにあるレポートから取得されます。 ブラウザーで PowerBI.com を開くと、Power BI ダッシュボード全体で同じレポートのリストが使用されていることがわかります。 次の図のように、一部のレポートを選択し、**OK** をクリックして続行します。 [![レポート カタログ ダイアログ ボックス](./media/ledger-budgets-workspace-list-of-reports-chosen-1024x570.jpg)](./media/ledger-budgets-workspace-list-of-reports-chosen.jpg)次に、ワークスペースの**リンク**セクションの下部までスクロールします。 Power BI レポートの新しいセクションが、リンクに追加されたことに注意します。 [![リンク セクションにある Power BI レポート セクション](./media/ledger-budgets-workspace-reports-in-links-section-1024x572.jpg)](./media/ledger-budgets-workspace-reports-in-links-section.jpg)

## <a name="full-page-power-bi-reports-in-the-client"></a>クライアントでの全ページ Power BI レポート
Power BI reports は the Dynamics 365 for Finance and Operations クライアントで開いて実行することができます。 この機能は、Microsoft SQL Server Reporting Services (SSRS) レポートを実行するための機能に似ています。 Power BI レポートを実行するには、**リンク** セクションで、Power BI レポートのいずれかのリンクをクリックします。 この例では、**Retail 分析サンプル**リンクをクリックします。 Power BI レポートは、次の図に示すように、ページ全体のビューを使用してクライアントで開かれます。 このレポートはインタラクティブです。 レポート領域をクリックすると、残りのビジュアルは選択内容に反応します。 [![小売分析のサンプル レポート](./media/retail-analysis-report-full-page-no-filters-1024x573.jpg)](./media/retail-analysis-report-full-page-no-filters.jpg)フィルター ウィンドウを使用して、レポート上のデータをフィルターできます。 次の図は、フィルターが適用された後のレポートを示しています。 [![フィルター処理した小売分析のサンプル レポート](./media/retail-analysis-report-full-page-filtered-view-1-1024x571.jpg)](./media/retail-analysis-report-full-page-filtered-view-1.jpg) PowerBI.com でこのレポートを開いて変更することもできます。 異なる名前を持つ別のコピーとして修正済みのレポートを保存し、新しいレポートをワークスペースにピン留めすることもできます。

## <a name="power-bi-in-user-created-workspaces"></a>ユーザーが作成したワークスペースの Power BI
これまで、「開発者が作成した」ワークスペースに Power BI タイルおよびレポートを追加する方法を説明してきました。 開発者が作成したワークスペースは、Microsoftによって作成されたワークスペース (つまり、製品に組み込まれている)、独立系ソフトウェア ベンダー (ISV) またはパートナー、または社内開発者によって作成されたワークスペースです。 ただし、Microsoft Dynamics AX プラットフォーム更新プログラム 1 (2016 年 5 月) で、ユーザーはクライアントの個人用設定機能を使用して新しいワークスペースを作成できます。 新しいワークスペースを作成するには、ホームページ (またはダッシュボード) でワークスペースのタイルを右クリックし、**ワークスペースを追加** をクリックします。 新しいワークスペースが作成されます。 新しいワークスペースは、**マイ ワークスペース 1**、**マイ ワークスペース 2** などという名前が付けられます。 後から名前は変更することができます。 作成したワークスペースをクリックします。 先に説明したのと同じオプションを使用して、Power BI タイルおよびレポートを追加することができるようになりました。 次の図は、例を示します。 [![ユーザーが作成したワークスペースの Power BI レポート](./media/my-workspace-with-tiles-and-reports-1024x584.jpg)](./media/my-workspace-with-tiles-and-reports.jpg)




