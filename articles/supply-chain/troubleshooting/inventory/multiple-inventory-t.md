---
title: 現物更新が無効な場合に使用するバッチ番号の複数の在庫トランザクション
description: バッチ番号グループの [現物更新] オプションが [いいえ] に設定されている品目の発注書行を調整すると、複数の在庫トランザクションが作成されます。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026691"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a>現物更新が無効な場合に使用するバッチ番号の複数の在庫トランザクション

KB 番号: 4613390

## <a name="symptoms"></a>現象

バッチ番号グループの **現物更新** オプションが *いいえ* に設定されている品目の発注書行を調整すると、複数の在庫トランザクションが作成されます。

バッチ番号グループの **現物更新** オプションが *いいえ* に設定されている品目を作成すると、購買注文明細数量を変更して発注書ページを保存すると、新しいバッチ番号が自動的に作成されます。

## <a name="resolution"></a>解像度

バッチ番号グループの **現物更新** 設定は次のように処理されます。

- このオプションが *はい* に設定されている場合は、現物更新の後 (品目の出荷時や受け取り時など) にのみ新しいバッチ番号が作成されます。
- このオプションが *いいえ* に設定されている場合は、該当する更新が行われる度に (発注書に新しい数量が追加される場合など)、新しいバッチ番号が作成されます。
