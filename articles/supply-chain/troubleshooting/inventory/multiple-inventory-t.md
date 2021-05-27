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
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a><span data-ttu-id="ed034-103">現物更新が無効な場合に使用するバッチ番号の複数の在庫トランザクション</span><span class="sxs-lookup"><span data-stu-id="ed034-103">Multiple inventory transactions for batch numbers when On physical update is disabled</span></span>

<span data-ttu-id="ed034-104">KB 番号: 4613390</span><span class="sxs-lookup"><span data-stu-id="ed034-104">KB number: 4613390</span></span>

## <a name="symptoms"></a><span data-ttu-id="ed034-105">現象</span><span class="sxs-lookup"><span data-stu-id="ed034-105">Symptoms</span></span>

<span data-ttu-id="ed034-106">バッチ番号グループの **現物更新** オプションが *いいえ* に設定されている品目の発注書行を調整すると、複数の在庫トランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="ed034-106">Multiple inventory transactions are created after you adjust a purchase order line for items where the **On physical update** option of the batch number group is set to *No*.</span></span>

<span data-ttu-id="ed034-107">バッチ番号グループの **現物更新** オプションが *いいえ* に設定されている品目を作成すると、購買注文明細数量を変更して発注書ページを保存すると、新しいバッチ番号が自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="ed034-107">When you create an item where the **On physical update** option of the batch number group is set to *No*, the system automatically creates a new batch number if you modify a purchase line quantity and save the purchase order page.</span></span>

## <a name="resolution"></a><span data-ttu-id="ed034-108">解像度</span><span class="sxs-lookup"><span data-stu-id="ed034-108">Resolution</span></span>

<span data-ttu-id="ed034-109">バッチ番号グループの **現物更新** 設定は次のように処理されます。</span><span class="sxs-lookup"><span data-stu-id="ed034-109">The **On physical update** setting for batch number groups works in the following way:</span></span>

- <span data-ttu-id="ed034-110">このオプションが *はい* に設定されている場合は、現物更新の後 (品目の出荷時や受け取り時など) にのみ新しいバッチ番号が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ed034-110">When the option is set to *Yes*, new batch numbers are created only after a physical update (for example, when items are shipped or received).</span></span>
- <span data-ttu-id="ed034-111">このオプションが *いいえ* に設定されている場合は、該当する更新が行われる度に (発注書に新しい数量が追加される場合など)、新しいバッチ番号が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ed034-111">When the option is set to *No*, a new batch number is created every time that an applicable update occurs (for example, when a new quantity is added to a purchase order).</span></span>
