---
title: "展開のトレースを使用する"
description: "この記事は、注文の展開結果の背後にある原因を参照して追跡する方法について説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: dc4328bfd04b338decc237b2300eab59c072ab21
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="use-tracing-for-explosion"></a>展開のトレースを使用する

[!include[banner](../includes/banner.md)]


この記事は、注文の展開結果の背後にある原因を参照して追跡する方法について説明します。

追跡を有効にすることで、特定の注文の展開結果に関与する要因を表示できます。 次の例は、追跡情報の使用方法です。

-   サプライ チェーンおよび在庫引当を最適化する、計画オーダーのアクション間の関係を表示します。
-   既に承認された注文との関係を表示します。 自動的に確定する派生要求を絞り込み、より正確にオーダーの優先順位付けをします。
-   計画のパラメーターが最適であるかどうか、プランの結果をシミュレーションします。
-   注文の生産日付、量、および優先順位などの情報を決定した方法を確認します。

選択した注文の将来およびアクションに関する詳細を表示できます。 [**展開**] ページにある上部ウィンドウの [**説明**] タブで追跡情報を使用できます。 追跡はオーダーを展開するときに発生します。 オーダーの追跡を開始するには、[**更新**] をクリックし、[**トレースの有効化**] チェック ボックスをオンにします。 特定の情報のログを検索するには [**テキストの検索**] フィールドを使用できます。 検索結果はツリーで強調表示されます。

<a name="see-also"></a>参照
--------

[マスタ プラン](master-plans.md)




