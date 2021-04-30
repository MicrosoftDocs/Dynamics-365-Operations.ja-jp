---
title: 資産リースの支払いスケジュールをバッチで確認する
description: このトピックでは、複数の支払スケジュールをバッチで確認する方法について説明します。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymConfirmationDetails
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: eaff604b92c412cd35c5c2aeadb2d9ed8dc77706
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881255"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a><span data-ttu-id="7a69d-103">資産リースの支払いスケジュールをバッチで確認する</span><span class="sxs-lookup"><span data-stu-id="7a69d-103">Confirm Asset leasing payment schedules in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a69d-104">このトピックでは、複数の支払スケジュールをバッチで確認する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7a69d-104">This topic explains how to confirm multiple payment schedules in a batch.</span></span> <span data-ttu-id="7a69d-105">支払スケジュールを、リース期間や確認バッチプロセスで確認します。</span><span class="sxs-lookup"><span data-stu-id="7a69d-105">Payment schedules are confirmed either on a lease-to-lease basis or through the confirmation batch process.</span></span> <span data-ttu-id="7a69d-106">仕訳入力は、確認済の支払スケジュールが設定されたリースのみを転記できます。</span><span class="sxs-lookup"><span data-stu-id="7a69d-106">A journal entry can be posted only against a lease that has a confirmed payment schedule.</span></span> <span data-ttu-id="7a69d-107">支払スケジュールの確認は、そのリースの財務情報の最終承認として機能します。</span><span class="sxs-lookup"><span data-stu-id="7a69d-107">Confirmation of the payment schedule serves as a final approval of the financial information for the lease.</span></span> <span data-ttu-id="7a69d-108">支払リース料やリース期間など、リースに関する財務情報の将来的な変更はすべてリースの調整に該当し、その方法で処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a69d-108">All future changes to the financial information for the lease, such as payments and the lease term, constitute a lease adjustment and should be processed in that way.</span></span>

<span data-ttu-id="7a69d-109">複数の支払スケジュールを確認するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7a69d-109">To confirm multiple payment schedules, follow these steps.</span></span>

1. <span data-ttu-id="7a69d-110">**資産リース \> 定期 \> 確認バッチ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7a69d-110">Go to **Asset leasing \> Periodic \> Confirmation batch**.</span></span>
2. <span data-ttu-id="7a69d-111">**確認バッチ** ページで、**確認バッチ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a69d-111">On the **Confirmation batch** page, select **Confirmation batch**.</span></span>
3. <span data-ttu-id="7a69d-112">表示されるダイアログ ボックスで、確認する帳簿をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="7a69d-112">In the dialog box that appears, filter for the books that you want to confirm.</span></span>

    - <span data-ttu-id="7a69d-113">特定のリース グループに含まれるすべての帳簿を確認するには、**リース グループ** フィールドでグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="7a69d-113">To confirm all the books in a specific lease group, select the group in the **Lease group** field.</span></span>
    - <span data-ttu-id="7a69d-114">特定の帳簿を確認するには、**帳簿 ID** フィールドで帳簿を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a69d-114">To confirm specific books, select the books in the **Book ID** field.</span></span>
    - <span data-ttu-id="7a69d-115">すべての帳簿を確認するには、**すべての帳簿** パラメーターをオンにします。</span><span class="sxs-lookup"><span data-stu-id="7a69d-115">To confirm all books, turn on the **For all books** parameter.</span></span>

<span data-ttu-id="7a69d-116">新しく確認した帳簿の情報は、**確認済の帳簿** ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="7a69d-116">Information for the newly confirmed books is shown on the **Confirmed books** page.</span></span> <span data-ttu-id="7a69d-117">支払スケジュールを確認した後、リースに対して当初認識の仕訳入力を転記できます。</span><span class="sxs-lookup"><span data-stu-id="7a69d-117">After the payment schedules are confirmed, the initial recognition journal entries can be posted against the leases.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
