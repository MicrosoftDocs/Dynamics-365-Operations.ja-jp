---
title: 警告の設定
description: ここでは Microsoft Dynamics 365 for Finance and Operationsでバッチ ジョブの警告を設定する方法について説明します。
author: hasaid
manager: AnnBe
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 62333
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: Platform update 25
ms.openlocfilehash: d45d27b11beb70630df1cd1d17939468e734c908
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537177"
---
# <a name="set-up-alerts"></a><span data-ttu-id="28a29-103">警告の設定</span><span class="sxs-lookup"><span data-stu-id="28a29-103">Set up alerts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28a29-104">Microsoft Dynamics 365 for Finance and Operations の重大なイベントの通知システムは、警告によって形成されます。</span><span class="sxs-lookup"><span data-stu-id="28a29-104">Alerts form a notification system for critical events in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="28a29-105">警告を使用することで、作業日に追跡したいイベントに関する情報を常に受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="28a29-105">You can use alerts to stay informed about events that you want to track during the workday.</span></span> <span data-ttu-id="28a29-106">警告ルールの組み合わせを設定できます。そうすることでバッチ ジョブの終了時にエラーが発生した場合、またはキャンセルされた場合に警告を表示させることができます。</span><span class="sxs-lookup"><span data-stu-id="28a29-106">You can set up a set of alert rules so that you're alerted when a batch job ends, ends in error, or is canceled.</span></span> <span data-ttu-id="28a29-107">警告を電子メールで送信するか、アクション センターに通知として表示するかどうかを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="28a29-107">You can select whether the alerts are emailed to you or appear as notifications in the Action center.</span></span> <span data-ttu-id="28a29-108">警告はバッチ ジョブおよびユーザーごとに設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="28a29-108">Alerts can be set up per batch job and per user.</span></span>

## <a name="set-up-alerts-for-batch-enhanced-forms"></a><span data-ttu-id="28a29-109">バッチ ジョブの警告の設定</span><span class="sxs-lookup"><span data-stu-id="28a29-109">Set up alerts for batch enhanced forms</span></span>

<span data-ttu-id="28a29-110">この手順では、バッチ化されたフォームに表示される警告を設定します。</span><span class="sxs-lookup"><span data-stu-id="28a29-110">Follow these steps to set up alerts for batch enhanced forms.</span></span>

1. <span data-ttu-id="28a29-111">**システム管理** \> **照会** \> **バッチ ジョブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="28a29-111">Go to **System administration** \> **Inquiries** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="28a29-112">一覧から バッチ ジョブ を選択し、次に アクション ウィンドウ で **警告** を選択します。</span><span class="sxs-lookup"><span data-stu-id="28a29-112">Select a batch job in the list, and then, on the Action Pane, select **Alerts**.</span></span>
3. <span data-ttu-id="28a29-113">**バッチ ジョブの警告** ダイアログ ボックスでは、警告の内容を設定し、 **OK** します。</span><span class="sxs-lookup"><span data-stu-id="28a29-113">In the **Batch job alerts** dialog box, configure the alerts, and then select **OK**.</span></span>

    ![警告の設定](./media/Batch-alert-configure.png) 

4. <span data-ttu-id="28a29-115">警告の通知については [アクション センター] を確認してください。</span><span class="sxs-lookup"><span data-stu-id="28a29-115">Check the Action center for alert notifications.</span></span>

    ![警告の通知](./media/Batch-alert-notification.png)

# <a name="set-up-alerts-for-batch-legacy-forms"></a><span data-ttu-id="28a29-117">旧方式によるバッチ ジョブ 警告の設定</span><span class="sxs-lookup"><span data-stu-id="28a29-117">Set up alerts for batch legacy forms</span></span>

<span data-ttu-id="28a29-118">この手順では、従来のバッチ化されたフォームに表示される警告を設定します。</span><span class="sxs-lookup"><span data-stu-id="28a29-118">Follow these steps to set up alerts for batch legacy forms.</span></span>

1. <span data-ttu-id="28a29-119">**システム管理** \> **照会** \> **バッチ ジョブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="28a29-119">Go to **System administration** \> **Inquiries** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="28a29-120">一覧から バッチ ジョブ を選択し、次に アクション ウィンドウ 内の **バッチジョブ** タブ で **警告** を選択します。</span><span class="sxs-lookup"><span data-stu-id="28a29-120">Select a batch job in the list, and then, on the Action Pane, on the **Batch job** tab, select **Alerts**.</span></span>

    ![旧方式の警告](./media/Batch-alert-legacy.png) 

3. <span data-ttu-id="28a29-122">**バッチ ジョブの警告** ダイアログ ボックスでは、警告の内容を設定し、 **OK** します。</span><span class="sxs-lookup"><span data-stu-id="28a29-122">In the **Batch job alerts** dialog box, configure the alerts, and then select **OK**.</span></span>

> [!NOTE] 
> <span data-ttu-id="28a29-123">電子メールで通知を受信するには、 **バッチ ジョブの警告** ダイアログ ボックスで、 **電子メール** のオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="28a29-123">To receive email notifications, in the **Batch job alerts** dialog box, set the **Email** option to **Yes**.</span></span>
