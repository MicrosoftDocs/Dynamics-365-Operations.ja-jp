---
title: 販売注文明細行の作成時に同じ売買契約が選択される
description: 特定の日付に対して複数の売買契約が定義される場合、販売注文明細行の作成時には、最低価格の売買契約が常に選択されます。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a586a399fb349965b972191bec1271651bec5fcb
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476881"
---
# <a name="if-two-trade-agreements-exist-for-overlapping-dates-the-same-one-is-always-selected"></a>重複する日付に対して 2 つの売買契約が存在する場合、常に同じ売買契約が選択される

## <a name="symptoms"></a>現象

2 つの売買契約が同じ期間または重複する期間に対して定義されている場合は、それらの品目を含む販売注文明細行を作成するたびに同じ売買契約が選択されるように見えます。

## <a name="resolution"></a>解決策

特定の日付に対して複数の売買契約がある場合は、最低価格の売買契約が常に選択されます。 詳細については、[Microsoft Dynamics AX 2012 の売買契約](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90) のホワイトペーパーをダウンロードしてください。
