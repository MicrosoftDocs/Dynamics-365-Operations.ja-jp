---
title: 輸送管理ステータス
description: このトピックでは、輸送ステータスを作成し、そのステータスを配送業者のステータスにマップする方法について説明します。
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9d3ed4b73f909b50e97c971a37c548c8c4a9e620
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006469"
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
