---
title: リリースされた製品を削除できません
description: リリースされた製品およびそのすべてのバリアントは、リリースされた製品に関連するトランザクションが存在しない場合にのみ削除できます。
author: SmithaNataraj
ms.date: 06/11/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f03d45a36401314a4b02ff354fabb474568c48b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476908"
---
# <a name="you-cant-delete-a-released-product"></a>リリースされた製品を削除できません

## <a name="symptoms"></a>現象

リリースされた製品およびそのすべてのバリアントは、リリースされた製品に関連するトランザクションが存在しない場合にのみ削除できます。

## <a name="resolution"></a>解決策

リリースされた製品または製品マスターを削除するには、次の手順に従います。

1. 品目の未処理トランザクションをすべて閉じます。
1. 在庫を 0 (ゼロ) に減らします。
1. 在庫計算を実行します。
1. 削除する製品マスターのすべての製品バリアントを削除します。
