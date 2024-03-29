---
title: 輸送管理ステータス
description: この記事では、輸送ステータスを作成し、そのステータスを配送業者のステータスにマップする方法について説明します。
author: Weijiesa
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9b20570a87a9f8969ca6dcf898176fd40f88eeca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897375"
---
# <a name="transportation-management-statuses"></a>輸送管理ステータス

[!include [banner](../includes/banner.md)]

出荷配送業者から提供されるコードを解釈するために、輸送状態のマスター コードを設定します。 これにより、出荷配送業者と統合してステータスを提供することができます。 輸送マスター ステータス コードに与える輸送状態によって、積荷、出荷、またはコンテナーの状態を容易に追跡できます。 積荷、出荷、またはコンテナーの特定の輸送ステータスは、データ統合を通じてのみ更新できます。ユーザー インターフェイスから手動で更新することはできません。

## <a name="create-a-transportation-status"></a>輸送状態の作成

輸送ステータスを作成するには、次の手順に従います。

1. **輸送管理 \> 設定 \> 輸送ステータス マスター** に移動します。
1. **新規** を選択して、輸送状態マスターを作成します。
1. **輸送状態マスター** フィールドに、輸送状態に対応した固有 ID を入力します。
1. **輸送タイプ** フィールドで、輸送のタイプとして *出荷配送業者* または *ハブ* のいずれかを選択します。
1. 名前と輸送状態を入力します。
1. ページを閉じます。

## <a name="map-a-transportation-status-to-a-carrier-status"></a>配送業者ステータスへの配送ステータスのマップ

配送ステータスを配送業者ステータスにマップするには、次の手順に従います。

1. **輸送管理 \> 設定 \> 配送業者 \> 配送業者輸送ステータス** に移動します。
1. **新規** を選択して、出荷配送業者から提供されるコードを輸送状態のマスター コードにマップします。
1. 出荷配送業者と配送業者サービスの固有 ID を選択します。
1. 選択した出荷配送業者のコードにマップする輸送状態コードを選択します。
1. 出荷配送業者が使用する外部コードを入力します。
1. ページを閉じます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]