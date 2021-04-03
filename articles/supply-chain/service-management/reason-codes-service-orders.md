---
title: サービス注文の理由コード
description: サービス注文のステージの更新時にサービス注文の状態を分かりやすくするための理由コードを使用します。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: b059ad5b2ea9cd577624355cf17925cfb9b4867b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258521"
---
# <a name="reason-codes-for-service-orders"></a><span data-ttu-id="91384-103">サービス注文の理由コード</span><span class="sxs-lookup"><span data-stu-id="91384-103">Reason codes for service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="91384-104">サービス注文のステージの更新時にサービス注文の状態を分かりやすくするための理由コードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="91384-104">You can use reason codes to help explain the status of a service order when the stage of a service order is updated.</span></span> <span data-ttu-id="91384-105">たとえば、サービス注文をキャンセルした場合、キャンセルの理由コードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="91384-105">For example, if you cancel a service order, you can select a reason code for the cancellation.</span></span>

<span data-ttu-id="91384-106">サービス注文の進捗を追跡するために使用されている理由コードの情報を表示するには、サービス注文の処理状況レポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="91384-106">To view information about reason codes that are used to track the progress of service orders, run the Service order progress report.</span></span> <span data-ttu-id="91384-107">このレポートには、ステージにかかわりなくすべてのサービス注文と、サービス注文のステージの更新時に指定された理由コードが一覧表示されています。</span><span class="sxs-lookup"><span data-stu-id="91384-107">This report lists all service orders, regardless of their stage, and the reason codes that are specified when a service order stage is updated.</span></span>

## <a name="turn-reason-codes-on-or-off"></a><span data-ttu-id="91384-108">理由コードのオン/オフの切り替え</span><span class="sxs-lookup"><span data-stu-id="91384-108">Turn reason codes on or off</span></span>

<span data-ttu-id="91384-109">理由コードはオプションです。</span><span class="sxs-lookup"><span data-stu-id="91384-109">Reason codes are optional.</span></span> <span data-ttu-id="91384-110">特定のサービス ステージにサービス注文を更新するときに理由コードを要求するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="91384-110">You can decide whether to require a reason code when you update a service order to a specific service stage.</span></span>

1.  <span data-ttu-id="91384-111">**サービス管理** \> **設定** \> **サービス注文** \> **サービス ステージ** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="91384-111">Click **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="91384-112">**サービス ステージ** フォームで、サービス ステージを選択し、そのサービスのステージの **理由** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="91384-112">In the **Service stages** form, select a service stage, and then select the **Reason** check box for the service stage.</span></span>

3.  <span data-ttu-id="91384-113">フォームを閉じて、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="91384-113">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="91384-114">参照</span><span class="sxs-lookup"><span data-stu-id="91384-114">See also</span></span>

[<span data-ttu-id="91384-115">サービス注文ステージを設定します</span><span class="sxs-lookup"><span data-stu-id="91384-115">Set up service order stages</span></span>](set-up-service-order-stages.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]