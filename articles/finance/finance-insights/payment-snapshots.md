---
title: スナップショットの概要 (プレビュー)
description: このトピックでは、スナップショット機能を使用して、分析のためのキャッシュフロー予測を保存したり、後で実績と比較したりできます。 キャッシュフロー予測を生成する場合は、その予測を "スナップショット" として保存できます。 その後、そのスナップショットを使用して、予測に含まれていた勘定を編集したり、スナップショットの予測を実績と比較することができます。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f0d0bdde8b69148c72b8c645e040f0e596ecba92
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645628"
---
# <a name="snapshots-overview-preview"></a>スナップショットの概要 (プレビュー)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

スナップショットを使用すると、組織は、その時点でのキャッシュ ポジションと現金予測に関する情報を編集および保存できます。 財務実績とスナップショットを比較し、差異をチェックして、その情報を使用して、キャッシュフロー予測を時間の経過とともに向上させることができます。 具体的には、スナップショットは次の方法で使用できます。

- キャッシュ ポジションと現金予測を長期にわたって追跡します。
- データをフィルターして、そのスナップショットが作成された法人のサブセットを表示します。
- システムによって生成されたキャッシュ ポジションと現金予測を編集します。
- キャッシュフローを表示する場合に、楽観的、悲観、および最も可能性の高いビューを検討するために what-if 分析を行います。
- 財務実績を、スナップショットに保存されている予測と比較します。

スナップショットを作成するには、 **キャッシュ フロー予測** ワークスペースの **キャッシュ ポジション** タブまたは **現金予測** タブのいずれかで **新規スナップショット** を選択します。  スナップショットが作成された後、そのスナップショット内のインフローとアウトフローを編集して保存することができます。 保存されているすべてのスナップショットは、 **スナップショット** タブで使用でき、スナップショットを開くには、その名前を選択します。

スナップショットのキャッシュ インフローとアウトフローは、いつでも編集できます。 インフロー金額またはアウトフロー金額を編集すると、更新された金額は、元の残高を作成した流動資産勘定と比例配分するようになります。 スナップショットの編集を終えたら、**保存** を選び変更を保存します。

複数のスナップショットを比較するには、**スナップショットの比較** を選択します。 一度に 2 つのスナップショットを比較できます。 比較する 2 つのスナップショットを選択し、**OK** を選択します。 **スナップショットの比較** ページには、選択したスナップショットの比較が表示されます。 このページの上部セクションのグラフは、2 つのスナップショット間の重複する期間におけるキャッシュ インフロー、キャッシュ アウトフロー、および銀行残高を比較したものです。 下部のグリッドには、各流動性金額について、2 つの予測の詳細な比較が示されます。 グリッドの **差異** 列には、期間内の残高の差が表示されます。

財務実績結果を、スナップショットとして保存された予測と比較するには、**実績と比較** を選択します。 **スナップショットの比較** ページには、実際の金額と予測の比較が表示されます。 このページの上部セクションのグラフは、2 つのスナップショット間の重複する期間におけるキャッシュ インフロー、キャッシュ アウトフロー、および銀行残高を比較したものです。 下部のグリッドには、期間あたりの実際の残高と各流動性金額に対する予測残高の詳細な比較が示されます。 グリッドの **差異** 列には、期間内の実際の残高から予測残高との間の差が表示されます。

#### <a name="privacy-notice"></a>プライバシー通知
プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよび少ないセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル アグリーメント (SLA) には含まれておらず、(3) 個人データや、その他の法律上またはコンプライアンス要件の対象となるデータの処理に使用されず、(4) サポートが制限されます。