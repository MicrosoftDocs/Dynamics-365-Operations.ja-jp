---
title: サービス注文の理由コード
description: サービス注文のステージの更新時にサービス注文の状態を分かりやすくするための理由コードを使用します。
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9548d3a29c787b49713499519e1a02b5d218ac1c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836185"
---
# <a name="reason-codes-for-service-orders"></a><span data-ttu-id="3bb1e-103">サービス注文の理由コード</span><span class="sxs-lookup"><span data-stu-id="3bb1e-103">Reason codes for service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3bb1e-104">サービス注文のステージの更新時にサービス注文の状態を分かりやすくするための理由コードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="3bb1e-104">You can use reason codes to help explain the status of a service order when the stage of a service order is updated.</span></span> <span data-ttu-id="3bb1e-105">たとえば、サービス注文をキャンセルした場合、キャンセルの理由コードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="3bb1e-105">For example, if you cancel a service order, you can select a reason code for the cancellation.</span></span>

<span data-ttu-id="3bb1e-106">サービス注文の進捗を追跡するために使用されている理由コードの情報を表示するには、サービス注文の処理状況レポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="3bb1e-106">To view information about reason codes that are used to track the progress of service orders, run the Service order progress report.</span></span> <span data-ttu-id="3bb1e-107">このレポートには、ステージにかかわりなくすべてのサービス注文と、サービス注文のステージの更新時に指定された理由コードが一覧表示されています。</span><span class="sxs-lookup"><span data-stu-id="3bb1e-107">This report lists all service orders, regardless of their stage, and the reason codes that are specified when a service order stage is updated.</span></span>

## <a name="turn-reason-codes-on-or-off"></a><span data-ttu-id="3bb1e-108">理由コードのオン/オフの切り替え</span><span class="sxs-lookup"><span data-stu-id="3bb1e-108">Turn reason codes on or off</span></span>

<span data-ttu-id="3bb1e-109">理由コードはオプションです。</span><span class="sxs-lookup"><span data-stu-id="3bb1e-109">Reason codes are optional.</span></span> <span data-ttu-id="3bb1e-110">特定のサービス ステージにサービス注文を更新するときに理由コードを要求するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="3bb1e-110">You can decide whether to require a reason code when you update a service order to a specific service stage.</span></span>

1.  <span data-ttu-id="3bb1e-111">**サービス管理** \> **設定** \> **サービス注文** \> **サービス ステージ** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="3bb1e-111">Click **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="3bb1e-112">**サービス ステージ** フォームで、サービス ステージを選択し、そのサービスのステージの **理由** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="3bb1e-112">In the **Service stages** form, select a service stage, and then select the **Reason** check box for the service stage.</span></span>

3.  <span data-ttu-id="3bb1e-113">フォームを閉じて、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="3bb1e-113">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="3bb1e-114">参照</span><span class="sxs-lookup"><span data-stu-id="3bb1e-114">See also</span></span>

[<span data-ttu-id="3bb1e-115">サービス注文ステージを設定します</span><span class="sxs-lookup"><span data-stu-id="3bb1e-115">Set up service order stages</span></span>](set-up-service-order-stages.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]