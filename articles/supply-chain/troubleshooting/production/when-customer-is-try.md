---
title: 新しいロット ID を選択するとバッチ番号がクリアされる
description: ピッキング リスト仕訳帳の行を確認するときに、[ロット ID] フィールドで新しい値を選択すると、[バッチ番号] フィールドの値がクリアされます。
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026662"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a><span data-ttu-id="c97d7-103">新しいロット ID を選択するとバッチ番号がクリアされる</span><span class="sxs-lookup"><span data-stu-id="c97d7-103">Batch number is cleared when a new lot ID is selected</span></span>

<span data-ttu-id="c97d7-104">KB 番号: 4613107</span><span class="sxs-lookup"><span data-stu-id="c97d7-104">KB number: 4613107</span></span>

## <a name="symptoms"></a><span data-ttu-id="c97d7-105">現象</span><span class="sxs-lookup"><span data-stu-id="c97d7-105">Symptoms</span></span>

<span data-ttu-id="c97d7-106">ピッキング リスト仕訳帳の行を確認するときに、**ロット ID** フィールドで新しい値を選択すると、**バッチ番号** フィールドの値がクリアされます。</span><span class="sxs-lookup"><span data-stu-id="c97d7-106">When you're reviewing a picking list journal line, the value in the **Batch number** field is cleared if you select a new value in the **Lot ID** field.</span></span>

## <a name="resolution"></a><span data-ttu-id="c97d7-107">解像度</span><span class="sxs-lookup"><span data-stu-id="c97d7-107">Resolution</span></span>

<span data-ttu-id="c97d7-108">システムはデザイン通り動作しています。</span><span class="sxs-lookup"><span data-stu-id="c97d7-108">The system is behaving as designed.</span></span> <span data-ttu-id="c97d7-109">ロット ID を変更する場合は、品目コンテキストを変更します。</span><span class="sxs-lookup"><span data-stu-id="c97d7-109">If you change the lot ID, you change the item context.</span></span> <span data-ttu-id="c97d7-110">したがって、バッチ番号がリセットされます。</span><span class="sxs-lookup"><span data-stu-id="c97d7-110">Therefore, the batch number is reset.</span></span>

<span data-ttu-id="c97d7-111">バッチ番号をロット ID に関連付ける場合は、最初にロット ID を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c97d7-111">To associate the batch number with a lot ID, you must set the lot ID first.</span></span>
