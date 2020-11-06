---
title: 例外処理の倉庫作業をキャンセルする
description: このトピックでは、倉庫の監督がブロックされた作業を処理できるようにする、キャンセル作業機能について説明します。
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: daa8f0d19de75e6c126fe7a5fe312bca24c89bdc
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016243"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a><span data-ttu-id="84ac0-103">例外処理の倉庫作業をキャンセルする</span><span class="sxs-lookup"><span data-stu-id="84ac0-103">Cancel warehouse work for exception handling</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84ac0-104">Microsoft Dynamics 365 Supply Chain Management のキャンセル作業機能を使用して、管理者ユーザーは、現在進行中の特定の倉庫作業をキャンセルできますが、それがシステムによってブロックされたり、例外的な状況では完了できなかったりします。</span><span class="sxs-lookup"><span data-stu-id="84ac0-104">The Cancel work functionality in Microsoft Dynamics 365 Supply Chain Management lets the admin user cancel specific warehouse work that is currently in progress, but that is blocked by the system or can't be completed because of exceptional circumstances.</span></span> <span data-ttu-id="84ac0-105">この機能は、矛盾したデータを修復する SQL 修正スクリプトに対する魅力的で安全な代替手段です。</span><span class="sxs-lookup"><span data-stu-id="84ac0-105">This functionality is an attractive and secure alternative to SQL corrective scripts that fix inconsistent data.</span></span> <span data-ttu-id="84ac0-106">ただし、これらのスクリプトは通常 IT プロフェッショナルから要求されますが、会社の管理者権限を持つユーザーはこのキャンセル作業機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="84ac0-106">However, whereas these scripts are typically requested from IT professionals, the Cancel work functionality can be used by users in the company who have admin rights.</span></span>

<span data-ttu-id="84ac0-107">**倉庫管理** \> **定期処理のタスク** \> **クリーンアップ \> キャンセル作業** で、キャンセル作業機能にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="84ac0-107">You can access the Cancel work functionality at **Warehouse management** \> **Periodic tasks** \> **Clean up \> Cancel work**.</span></span> <span data-ttu-id="84ac0-108">**キャンセル作業** ダイアログ ボックスで、キャンセルする作業の作業 ID を指定し、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84ac0-108">In the **Cancel work** dialog box, specify the work ID of the work to cancel, and then select **OK**.</span></span>

## <a name="warehouse-work-that-can-be-canceled"></a><span data-ttu-id="84ac0-109">キャンセルできる倉庫作業</span><span class="sxs-lookup"><span data-stu-id="84ac0-109">Warehouse work that can be canceled</span></span>

<span data-ttu-id="84ac0-110">倉庫ピッキング工程中に、作業者は保管場所からユーザーの場所にピッキングされた数量を登録したが、プット工程を登録できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="84ac0-110">During warehouse picking operations, a worker might encounter situations where they have registered quantities as picked from a storage location to their user location, but then they can't register the put operation.</span></span> <span data-ttu-id="84ac0-111">一貫性のない倉庫データは、作業がブロックされる理由になりますが、常にそうとは限りません。</span><span class="sxs-lookup"><span data-stu-id="84ac0-111">Inconsistent warehouse data is often, but not always, the reason why work is blocked.</span></span>

<span data-ttu-id="84ac0-112">作業ヘッダーの **キャンセル** ボタンを使用してアクセスできる通常のキャンセル機能とは異なり、キャンセル作業機能では、最後に完了した作業明細行が **プット** タイプの作業明細行である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="84ac0-112">Unlike the regular Cancel functionality that can be accessed by using the **Cancel** button on the work header, the Cancel work functionality doesn't require that the last completed work line be a work line of the **put** type.</span></span> <span data-ttu-id="84ac0-113">つまり、キャンセル作業機能では、作業明細行の品目の数量がユーザーの場所にある場合でも、取消ロジックを実行できます。</span><span class="sxs-lookup"><span data-stu-id="84ac0-113">In other words, for the Cancel work functionality, cancellation logic can be run even if the item quantity on a work line is in a user location.</span></span>

> [!NOTE]
> <span data-ttu-id="84ac0-114">業務上の理由からキャンセルする必要がある作業の場合、倉庫ユーザーは作業ページで通常のキャンセル機能を引き続き使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84ac0-114">For work that must be canceled for operational reasons, warehouse users must continue to use the regular Cancel functionality on the work page.</span></span>

<span data-ttu-id="84ac0-115">**販売** 、 **移動の出庫** 、 **原材料ピッキング** 、または **補充** タイプの作業のみ、キャンセル作業機能を使用してキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="84ac0-115">Only work of the **Sales** , **Transfer issue** , **Raw material picking** , or **Replenishment** type can be canceled by using the Cancel work functionality.</span></span> <span data-ttu-id="84ac0-116">取消ロジックは、凍結された原材料ピッキング作業または通常のキャンセル機能を使用してキャンセルされる作業に対して実行されることはありません (前の注記を参照)。</span><span class="sxs-lookup"><span data-stu-id="84ac0-116">Cancellation logic won't be run for frozen raw material picking work or work that can be canceled by using the regular Cancel functionality (see the preceding note).</span></span>

<span data-ttu-id="84ac0-117">作業をブロック解除するには、システムは残りの作業明細行をキャンセルし、ユーザーが指定した作業 ID に関連付けられている倉庫データを修正します。</span><span class="sxs-lookup"><span data-stu-id="84ac0-117">To unblock the work, the system cancels any remaining work lines and fixes the warehouse data that is associated with the work ID that the user specified.</span></span> <span data-ttu-id="84ac0-118">その後、影響を受ける品目数量を含む、通常の倉庫処理工程を再開できます。</span><span class="sxs-lookup"><span data-stu-id="84ac0-118">Any regular warehouse-handling operations that involve the affected item quantity can then resume.</span></span>

<span data-ttu-id="84ac0-119">作業がキャンセルされた後に影響を受ける品目を特定の場所に配置するには、ユーザーはモバイル デバイスで在庫移動または数量調整操作を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84ac0-119">To put the affected item in a specific location after the work is canceled, the user must use an inventory movement or quantity adjustment operation on a mobile device.</span></span>
