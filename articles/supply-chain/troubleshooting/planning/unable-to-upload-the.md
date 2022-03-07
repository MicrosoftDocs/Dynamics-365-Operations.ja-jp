---
title: 需要予測レコードをインポートする際に予測単位原価を更新できない
description: データ エンティティを使用して需要予測レコードをインポートする場合、既存のレコードの原価価格はインポートされたデータに一致するようには更新されません。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026681"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>需要予測レコードをインポートする際に予測単位原価を更新できない

KB 番号: 4614109

## <a name="symptoms"></a>現象

データ エンティティを使用して需要予測レコードをインポートする場合、既存のレコードの **予測単価** の値はインポートされたデータに一致するようには更新されません。

## <a name="cause"></a>原因

**予測単位原価** は読み取り専用フィールドです。 この値は製品の単位原価に基づいており、インポートによって直接設定することはできません。

## <a name="resolution"></a>解像度

このフィールドは読み取り専用であるため、値をインポートできません。 この値は、既存のビジネス ロジックに従って計算されます。
