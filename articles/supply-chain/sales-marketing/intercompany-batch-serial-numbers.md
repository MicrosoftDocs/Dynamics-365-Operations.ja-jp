---
title: 会社間バッチ番号とシリアル番号
description: この記事では、会社間注文にバッチ番号とシリアル番号を登録する際の処理について説明します
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 5c743c8eee8d27a2c2357523a11236eb247ec5be
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851510"
---
# <a name="intercompany-batch-and-serial-numbers"></a>会社間バッチ番号とシリアル番号

[!include [banner](../../includes/banner.md)]

シリアル番号またはバッチ番号を使用して品目を追跡している会社は、ピッキング済品目のシリアル番号やバッチ番号も追跡する必要があります。 会社間機能では、シリアル番号やバッチ番号のプッシュ/プルを自動化しています。 会社間販売注文書で品目のバッチ番号やシリアル番号を登録する場合、これらの番号を会社間発注書および元の販売注文書に自動的にプッシュするプログラムを設定できます。 **会社間取引** のページで、関連するパラメータを設定します。

- **販売注文ポリシー** ページの **バッチ番号** フィールドを選択すると、会社間販売注文書の梱包明細を転記するときに、会社間発注書明細行の在庫トランザクションにバッチ番号が同期されます。
- **シリアル番号** フィールドを選択すると、会社間販売注文書の梱包明細を転記するときに、会社間発注書明細行の在庫トランザクションにシリアル番号が同期されます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
