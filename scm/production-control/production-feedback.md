---
title: "生産フィードバック"
description: "この記事は、作業者に生産ジョブに関するフィードバックを与える生産フィードバックに関する情報を提供します。 この記事には、生産フィードバックを更新するさまざまな方法に関する情報が含まれます。"
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 19 - 15
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c1192695351fe1eab4beb471e5b8d4eb7a384c70
ms.lasthandoff: 03/29/2017


---

# <a name="production-feedback"></a>生産フィードバック

この記事は、作業者に生産ジョブに関するフィードバックを与える生産フィードバックに関する情報を提供します。 この記事には、生産フィードバックを更新するさまざまな方法に関する情報が含まれます。

生産フィードバックは、作業者に、生産ジョブに関するフィードバックを提供します。 製造オーダーの時間や材料消費、工程の数量および状態、ジョブや工程の失敗原因になったエラーを記録しています。 生産フィードバックは、製造オーダーに関連付けられた仕訳帳で更新できます。 **生産ジョブ カード**と**生産工順カード**の仕訳帳を使用して、ジョブや工程ごとの時間と数量を報告することができます。 最後のジョブまたは工程に関するレポートで、完成品の数量を完了として報告できます。 生産フィードバックは、**ジョブ カード ターミナル** ページと**ジョブ カードのデバイス** ページで更新できます。 これらのページは、生産フィードバックが作業現場で更新されるように、**生産管理**モジュールの製造実行メカニズムの一部です。 ** ジョブ カード ターミナル** ページには、コンフィギュレーション可能なユーザー インターフェイスがあり、選択した作業領域について、リリースされたジョブの一覧を優先付けされた順序で表示できます。 また、ジョブのバンドル、チーム作業などの詳細オプションを提供します。 **ジョブ カードのデバイス** ページには、タッチに最適化されたユーザー インターフェイスがあります。 両方のページの生産フィードバックは、生産仕訳帳から更新されます。


