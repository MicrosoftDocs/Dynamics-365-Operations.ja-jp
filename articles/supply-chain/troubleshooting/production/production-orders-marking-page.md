---
title: マーキング ページに製造オーダーが表示されない
description: マーキング ページには、一部の製造オーダーが表示されません。 このトピックでは、マーキングに使用できない 3 つの製品コンフィギュレーションについて説明します。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 87507e91d3feb2557e7ba771b8e34ff7ca105749
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476822"
---
# <a name="production-orders-arent-shown-on-the-marking-page"></a>マーキング ページに製造オーダーが表示されない

## <a name="symptoms"></a>現象

個別製造で作業しているとき、一部の製造オーダーが **マーキング** ページに表示されません。

## <a name="resolution"></a>解決策

次の構成を持つ製品をマーキングに使用することはできません。 したがって、これらは **マーキング** ページに表示されません。

- 製品は、*CW* タイプの製品として定義されます。
- これらは、高度な倉庫プロセスに対して有効になっています。
- これらは、*標準原価* 原則によって制御されるように構成されています。
