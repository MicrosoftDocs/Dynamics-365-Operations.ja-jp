---
title: 製造差異の一般的な発生源
description: この記事は、製造差異のタイプごとの一般的な発生源について説明します。
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostTrans, ProdCalcVarianceTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f36e482595cad49d1149873f8bcdd6a05a3287d5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229282"
---
# <a name="common-sources-of-production-variances"></a>製造差異の一般的な発生源

[!include [banner](../includes/banner.md)]

この記事は、製造差異のタイプごとの一般的な発生源について説明します。 

**ロット サイズ** の差異の一般的な発生源を次に示します。

-   製造オーダーの商品数量が、標準原価計算で使用される計算数量と異なる。 この数量は、固定費を償却するための基準を提供します。
-   製造オーダー内の固定費の金額が、標準原価計算で使用される固定費と異なる。 製造オーダー内の固定費は、さまざまな理由で異なる可能性があります。 たとえば、固定費には次の要因が反映されている場合があります。
    -   生産部品表 (BOM) または工順の手動による変更
    -   製造オーダーを作成時に異なる BOM バージョンまたは工順バージョンの選択
    -   品目に割り当てられる BOM バージョンまたは工順バージョンの計画技術変更

**生産価格** の差異の一般的な発生源を次に示します。

-   報告された工順工程の消費に対する原価カテゴリ (および原価カテゴリ価格) が、標準原価計算で使用される原価カテゴリと異なる。
-   原価カテゴリ価格の有効原価が、標準原価計算で使用される原価カテゴリ価格と異なる。

**生産数量** の差異の一般的な発生源を次に示します。

-   材料コンポーネントの過剰出庫または過少出庫。
-   工順工程の過剰レポート時間または過少レポート時間。
-   注文数量に比例した親品目の適正数量からの過剰入庫または過少入庫。 ただし、製造オーダー用の注文数量に基づいて、コンポーネントの発行と工程報告は完了しています。

**生産代替** の差異の一般的な発生源を次に示します。

-   生産 BOM に含まれていない材料コンポーネントの出庫。
-   生産 BOM にコンポーネントを手動追加し、そのコンポーネントを消費済としてレポート。
-   品目を生産 BOM に手動追加せずに、消費済としてレポート。
-   工程を生産工順に手動追加し、その工程を消費済としてレポート。
-   製造オーダーの作成時に別の BOM バージョンを選択。その BOM バージョンは、標準原価計算で使用されるものと異なっている。
-   製造オーダーの作成時に別の工順バージョンを選択。その工順バージョンは、標準原価計算で使用されるものと異なっている。






[!INCLUDE[footer-include](../../includes/footer-banner.md)]