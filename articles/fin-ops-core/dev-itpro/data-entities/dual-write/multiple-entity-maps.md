---
title: 複数のエンティティ マップの管理
description: この記事では、複数のエンティティ マップを選択し、依存エンティティ マップの一覧を表示し、エンティティ マップとそれに関連するすべてのエンティティを有効にし、さらに既存のデータをコピーする方法について説明します。
author: sabinn-msft
manager: AnnBe
ms.date: 08/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Developer
ms.reviewer: v-douklo
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7ba2adbeeb5deb4abbbe77174691eb8aa22a773
ms.sourcegitcommit: d62e52484dfd9913a75a4561766d5e22fe2f3e8b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2020
ms.locfileid: "3689524"
---
# <a name="manage-multiple-entity-maps"></a>複数のエンティティ マップの管理

[!include [banner](../../includes/banner.md)]


この記事では、複数のエンティティ マップを選択し、依存エンティティ マップの一覧を表示し、エンティティ マップとそれに関連するすべてのエンティティを有効にし、さらに既存のデータをコピーする方法について説明します。

日常業務の一部として、エンティティ マップを一括処理する必要がある場合があります。 たとえば、一連のエンティティ マップを同時に有効化または一時停止することができます。 これを 1 つ行う代わりに、煩雑で時間がかかりますが、二重書き込みリスト ページで複数のエンティティ マップを同時に有効化、一時停止、再開、または停止することができます。

![複数のエンティティ マップを選択](media/select-multiple-entity-maps.png)
 
複数のエンティティ マップを有効にすると共に、**関連エンティティ マップの表示**を選択することによって、すべての依存エンティティ マップの一覧を表示することもできます。

![関連するエンティティ マップの表示](media/show-related-entity-map.png)
 
選択したエンティティ マップとそれに関連するすべてのエンティティを有効にするには、**実行**を選択します。 選択したエンティティマップまたはその依存に対応する既存のデータをコピーする場合は、**初期同期**に対応するチェック ボックスをオンにします。 または、チェック ボックスをオフにして、1 つ以上の関連エンティティの選択を解除します。 エンティティ マップをドラッグ アンド ドロップして、同期されるマップの順序を変更することもできます。
