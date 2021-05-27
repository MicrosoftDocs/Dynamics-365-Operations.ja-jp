---
title: 場所プロファイルではマイナス在庫は許可されませんが、マイナス手持ち在庫は許可されます
description: 場所プロファイルの [マイナス在庫を許可] オプションは [いいえ] に設定されていますが、マイナス手持ち在庫は許容されたままになります。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026675"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a><span data-ttu-id="f5092-103">場所プロファイルではマイナス在庫は許可されませんが、マイナス手持ち在庫は許可されます</span><span class="sxs-lookup"><span data-stu-id="f5092-103">Location profile disallows negative inventory, but negative on-hand inventory is permitted</span></span>

<span data-ttu-id="f5092-104">KB 番号: 4613622</span><span class="sxs-lookup"><span data-stu-id="f5092-104">KB number: 4613622</span></span>

## <a name="symptoms"></a><span data-ttu-id="f5092-105">現象</span><span class="sxs-lookup"><span data-stu-id="f5092-105">Symptoms</span></span>

<span data-ttu-id="f5092-106">場所プロファイルの **マイナス在庫を許可** オプションは *いいえ* に設定されていますが、マイナス手持ち在庫は許容されたままになります。</span><span class="sxs-lookup"><span data-stu-id="f5092-106">The **Allow negative inventory** option for the location profile is set to *No*, but the system still allows negative on-hand inventory.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="f5092-107">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="f5092-107">Example scenario</span></span>

<span data-ttu-id="f5092-108">政府が規制したトランザクションの場合、システムはマイナス在庫を帳損に記録できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5092-108">For government-regulated transactions, the system must be able to record negative inventory to book losses.</span></span> <span data-ttu-id="f5092-109">品目は、マイナスの在庫を指定した場所 (変更可能な場所など) にのみ表示可能にする。</span><span class="sxs-lookup"><span data-stu-id="f5092-109">You want an item to be able to show negative inventory, but only in designated locations, such as tanks.</span></span> <span data-ttu-id="f5092-110">ただし、品目モデル グループでマイナス在庫が許可されている場合、場所がマイナス在庫を許可するよう設定されているかどうかは関係ありません。</span><span class="sxs-lookup"><span data-stu-id="f5092-110">However, if the item model group allows negative inventory, you find that it doesn't matter whether the location is set to allow negative inventory.</span></span> <span data-ttu-id="f5092-111">マイナス在庫を許可しないよう品目が設定されている場合、場所プロファイルの設定方法は関係ありません。</span><span class="sxs-lookup"><span data-stu-id="f5092-111">If the item is set up so that negative inventory isn't allowed, it doesn't matter how the location profile is set up.</span></span>

## <a name="resolution"></a><span data-ttu-id="f5092-112">解像度</span><span class="sxs-lookup"><span data-stu-id="f5092-112">Resolution</span></span>

<span data-ttu-id="f5092-113">場所プロファイルの **マイナス在庫を許可** 設定は、ピッキングなどの倉庫プロセスにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f5092-113">The **Allow negative inventory** setting from the location profile applies only to warehouse processes, such as picking.</span></span> <span data-ttu-id="f5092-114">ただし、マイナス在庫を許可するよう設定された品目モデル グループは、在庫管理モジュールおよび倉庫管理モジュールのすべてのプロセスに影響します。場所プロファイルは、この設定を上書きしません。</span><span class="sxs-lookup"><span data-stu-id="f5092-114">However, item model groups that are set to allow negative inventory affect all processes from the Inventory management and Warehouse management modules, and the location profile won't override the setting.</span></span>

<span data-ttu-id="f5092-115">倉庫でマイナス在庫を保管できるかどうかを制御できます。</span><span class="sxs-lookup"><span data-stu-id="f5092-115">You can control whether a warehouse is allowed to carry negative inventory.</span></span> <span data-ttu-id="f5092-116">品目モデル グループがマイナス在庫を許可しないよう設定し、マイナス在庫を許可するには関連倉庫のみを設定します。</span><span class="sxs-lookup"><span data-stu-id="f5092-116">Set your item model groups to disallow negative physical inventory, and set only the relevant warehouse to allow negative inventory.</span></span>
