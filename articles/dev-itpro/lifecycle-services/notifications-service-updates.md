---
title: Lifecycle Services (LCS) でサービス更新プログラムに関する通知を受け取る
description: このトピックでは環境へのサービス更新プログラムについて通知を受けるさまざまな方法について説明します。
author: manalidongre
manager: AnnBe
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: ccaa596f9edeba5f653f674886d85229969f4ea5
ms.sourcegitcommit: f5c2cfac0411c880994376ead6691ab52f2fd12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "1720224"
---
# <a name="get-notified-about-service-updates-through-lifecycle-services-lcs"></a><span data-ttu-id="93a9b-103">Lifecycle Services (LCS) でサービス更新プログラムに関する通知を受け取る</span><span class="sxs-lookup"><span data-stu-id="93a9b-103">Get notified about service updates through Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93a9b-104">このトピックでは Microsoft からのサービス更新プログラムについて最新の状態に保つ方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="93a9b-104">This topic explains how you can stay up to date about service updates from Microsoft.</span></span>

<span data-ttu-id="93a9b-105">Microsoft はサービス更新プログラムを使用して、構成されたサンドボックスおよび実稼働環境を最新のリリース バージョンに更新します。</span><span class="sxs-lookup"><span data-stu-id="93a9b-105">Microsoft uses service updates to update your configured sandbox and production environments to the latest released version.</span></span> <span data-ttu-id="93a9b-106">Microsoft はお客様の環境に対する今後の更新プログラムについて、電子メールおよび Microsoft Dynamics Lifecycle Services (LCS) の通知でお知らせします。</span><span class="sxs-lookup"><span data-stu-id="93a9b-106">Microsoft notifies you about upcoming updates to your environments via email and through notifications in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="93a9b-107">受け取る通知の種類を次に示します:</span><span class="sxs-lookup"><span data-stu-id="93a9b-107">Here are the different types of notifications that you will receive:</span></span>

- <span data-ttu-id="93a9b-108">**更新が利用可能になった際の通知:** 新しいリリースが一般公開されると、ご利用の実装しているプロジェクトのアクションセンターに Microsoft からの通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="93a9b-108">**Notification when an update is made available:** When a new release is made generally available, Microsoft surfaces a notification in your implementation projects' action center.</span></span> <span data-ttu-id="93a9b-109">Microsoft による自動更新がされる前に環境に更新を適用する場合は、その更新をプロジェクトのアセットライブラリに保存することができます。</span><span class="sxs-lookup"><span data-stu-id="93a9b-109">You can then save that update in your projects' asset library, if you want to apply the update to your environments before Microsoft does an automatic update.</span></span> <span data-ttu-id="93a9b-110">Microsoftが自動更新を行うと、プロジェクトのアセットライブラリに更新のコピーが保存されます。</span><span class="sxs-lookup"><span data-stu-id="93a9b-110">When Microsoft does an automatic update, it also saves a copy of the update in your projects' asset library.</span></span> 
- <span data-ttu-id="93a9b-111">**更新の 5 日前に送信される通知:** Microsoft はお客様の環境を更新する 5 日前にユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="93a9b-111">**Notification that is sent five days before the update:** Microsoft notifies you five days before it updates your environment.</span></span> <span data-ttu-id="93a9b-112">更新頻度を構成した後で、更新が発生する 5 日前に次回の更新プログラムに関する通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="93a9b-112">After you've configured your update cadence, you will receive notifications about upcoming updates five days before they occur.</span></span> <span data-ttu-id="93a9b-113">これらの通知は 3 つのフォームを取ります:</span><span class="sxs-lookup"><span data-stu-id="93a9b-113">These notifications take three forms:</span></span>

    - <span data-ttu-id="93a9b-114">**電子メール通知:** プロジェクト所有者、環境管理者、および追加で環境の関係者としてリストされているユーザーに、次回の更新について電子メールで通知されます。</span><span class="sxs-lookup"><span data-stu-id="93a9b-114">**Email notification:** Project owners, environment managers, and users who are listed as additional stakeholders for an environment are notified by email about the upcoming update.</span></span>
    - <span data-ttu-id="93a9b-115">**環境の詳細ページの通知バー:** LCS の環境の詳細ページに表示される通知は、次回の更新についてお客様に知らせます。</span><span class="sxs-lookup"><span data-stu-id="93a9b-115">**Notification bar on the environment details page:** A notification that appears on the environment details page in LCS informs the customer about the upcoming update.</span></span>
    - <span data-ttu-id="93a9b-116">**更新を反映した今後の更新:** LCS の環境の詳細ページで **管理 &gt; 次回の更新** を選択し、今後の更新プログラムに関する詳細を含むダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="93a9b-116">**Upcoming update reflects the update:** On the environment details page in LCS, select **Maintain &gt; Upcoming Update** to open a dialog box that contains details about the upcoming update.</span></span>

- <span data-ttu-id="93a9b-117">**更新の 1 時間前に送信される通知:** ダウンタイム時間枠の開始 1 時間前に Microsoft Dynamics 365 for Finance and Operations のユーザーは通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="93a9b-117">**Notification that is sent one hour before the update:** One hour before the start of the downtime window, users in Microsoft Dynamics 365 for Finance and Operations receive a notification.</span></span> <span data-ttu-id="93a9b-118">この通知は、環境が更新で停止されるためユーザーに作業を保存するよう求めます。</span><span class="sxs-lookup"><span data-stu-id="93a9b-118">This notification asks users to save their work, because the environment will be taken down for an update.</span></span>
- <span data-ttu-id="93a9b-119">**更新が完了したときに送信される通知:** Microsoft が構成された環境の更新を完了すると、更新の結果について電子メールで通知されます。</span><span class="sxs-lookup"><span data-stu-id="93a9b-119">**Notification that is sent when the update is completed:** After Microsoft has finished updating your configured environment, it notifies you by email about the outcome of the update.</span></span> <span data-ttu-id="93a9b-120">更新が正常に適用されたかに関わらず、この電子メールは常に送信されます。</span><span class="sxs-lookup"><span data-stu-id="93a9b-120">This email is always sent, regardless of whether the update was successfully applied.</span></span> <span data-ttu-id="93a9b-121">プロジェクト所有者、環境管理者、および環境の追加の関係者としてリストされているユーザーに送信されます。</span><span class="sxs-lookup"><span data-stu-id="93a9b-121">It's sent to project owners, environment managers, and users who are listed as the additional stakeholders for the environment.</span></span> <span data-ttu-id="93a9b-122">Microsoft が何らかの理由で更新プログラムを開始できない場合、電子メールは更新プログラムが開始されなかった理由の説明を含みます。</span><span class="sxs-lookup"><span data-stu-id="93a9b-122">If Microsoft can't start the update for some reason, the email includes a reason to explain why the update wasn't started.</span></span>

<span data-ttu-id="93a9b-123">通知を受け取った後で、何らかの理由により更新を続行できない場合は、一時停止することができます。</span><span class="sxs-lookup"><span data-stu-id="93a9b-123">After you receive a notification, if you can't proceed with the update for some reason, you can pause it.</span></span> <span data-ttu-id="93a9b-124">構成されたサンドボックス環境および実稼働環境への更新を一時停止する方法の詳細は、[Lifecycle Services (LCS) によるサービスの更新の一時停止](pause-service-updates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93a9b-124">For more information about how to pause updates to configured sandbox and production environments, see [Pause service updates through Lifecycle Services (LCS)](pause-service-updates.md).</span></span>

<span data-ttu-id="93a9b-125">1 つのバージョンおよび Microsoft が管理するサービスの更新の詳細は、[1 つのバージョンのサービス更新に関するよく寄せられる質問](../../fin-and-ops/get-started/one-version.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93a9b-125">For more information about One Version and Microsoft-managed service updates, see [One Version service updates FAQ](../../fin-and-ops/get-started/one-version.md).</span></span>
