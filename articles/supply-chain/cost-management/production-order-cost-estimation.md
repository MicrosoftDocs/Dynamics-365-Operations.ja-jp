---
title: 原価見積を行う製造オーダー。
description: この記事は、生産原価見積に関する情報を提供します。 生産原価見積では、計画製造オーダー数量で品目を製造する場合の予測される材料消費および能力消費の原価が示されます。
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac658b49109a3fb3f987cf30bfa0b62bbff3d1c2
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672265"
---
# <a name="production-order-cost-estimation"></a>原価見積を行う製造オーダー。

[!include [banner](../includes/banner.md)]

この記事は、生産原価見積に関する情報を提供します。 生産原価見積では、計画製造オーダー数量で品目を製造する場合の予測される材料消費および能力消費の原価が示されます。 

製造オーダーを作成したあと、生産原価を見積もる必要があります。 その目的は、品目消費と工順消費を生産プロセスに対して見積もることです。これらの見積によって、以降のスケジューリングや生産プロセスの基盤を築くことができます。

## <a name="production-cost-estimation"></a>製造原価見積
生産原価の見積は、次の情報に基づいています。

-   製造オーダーの数量
-   製造部品表 (BOM) のコンポーネント
-   製造工順の工順工程
-   コンポーネントと工程に適用される間接原価
-   計算日付においての現在有効な原価データ

製造 BOM にファントム品目がある場合、ファントムのコンポーネントと工順工程が計算に反映されます。 見積タスクを使用すると、見積原価を再計算して更新情報を反映させることができます。 たとえば、更新情報には、製造オーダーの数量、製造 BOM のコンポーネント、生産工順における工順工程、これらのコンポーネントと工程に適用される間接費、または再計算日の時点での実績原価データの変更などがあります。 見積原価の計算では、原価に利幅を追加するアプローチに基づいて、製造品目の販売価格も提案されます。 オプションで、製造オーダーにリンクされた別の製造オーダーを反映した参照オーダーに見積原価計算を適用できます。

## <a name="view-the-estimated-costs"></a>見積原価の表示
見積を実行した後、**価格計算** ページで結果を表示できます。 見積では、次の値が計算されます。

-   **生産原価**– 生産原価は、見積のトップラインです。 製造オーダーを実行するすべての原価と、生産の販売価格合計が示されます。 見積のすべての原価明細行の合計になります。
-   **工順またはリソース コスト** – 工順またはリソース コストとは、生産工程の原価です。 ここには、段取り時間、実行時間、間接費などの要素の原価が含まれます。
-   **原材料の原価** – 原材料の原価は、品目の製造に必要な部品表 (BOM) コンポーネントの原価と価格です。 これらの原価は事前に作成され、システムに入力されています。

## <a name="other-uses-of-cost-estimation"></a>原価見積のその他の用途
原価見積では、次の情報も提供されます。

-   有効な価格見積書
-   注文の収益性の見積
-   原材料消費の見積
-   前の生産からの原価情報の比較
-   予算と予測情報
-   特定の原価を管理するために必要な生産サイズの見積






[!INCLUDE[footer-include](../../includes/footer-banner.md)]