---
title: 製造オーダーの完了済としての報告
description: 完了レポートは生産ステージです。 この段階では、完成品は製造オーダーから在庫へ報告され、移動されます。
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87e5d4f46a2ae34a2bc114a92ed4e037875dde43
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431896"
---
# <a name="report-production-orders-as-finished"></a>製造オーダーの完了済としての報告

[!include [banner](../includes/banner.md)]

完了レポートは生産ステージです。 この段階では、完成品は製造オーダーから在庫へ報告され、移動されます。

製造オーダーで完成品の完了数が完了として報告があると、在庫の手持在庫として更新されます。 元の計画オーダー数量の一部の数量を完了報告できます。 数量の完了を報告するときに、関連するエラーとともにエラー数量を報告することもできます。 製造オーダーが [完了報告済] ステージに達すると、これ以上の数量は製造オーダーで報告されません。
次の特性は、**完了レポート** プロセスと関連付けられます。
-   原材料の消費と、報告済数量 (バック フラッシュ) に比例する時間を設定できます。
-   プット アウェイ作業は倉庫プロセスに有効になる品目に対して生成できます。
-   完成品の予定または標準原価の値は、勘定科目に報告されるように設定できます。
-   品質指示は品質関連の設定に基づいて、報告された数量に対して作成できます。

数量が出荷場所に報告されます。 倉庫の作業は、出荷場所からプット アウェイ作業の場所のディレクティブによって定義される最終目的地に数量を移動するために生成されます。

-   品質指示は、品質関連が設定されている場合に、製造オーダーの完了報告時に作成できます。

## <a name="set-a-production-order-to-reporting-as-finished"></a>完了レポートする製造オーダーの設定
標準の製造オーダー更新機能を使用するか、工順およびジョブ カード仕訳帳か、仕訳帳の **完了レポート** を使用して、製造オーダーのステータスを **完了レポート** に設定できます。 製造オーダーの最後のジョブを報告するときに、ジョブ カード ターミナル、ジョブ カード デバイスのページを使用してステージを **完了レポート** に更新できます。 最後に、ハンドヘルド デバイスの倉庫のソリューションのプロセスとして **完了レポート** オプションを有効にできます。  



