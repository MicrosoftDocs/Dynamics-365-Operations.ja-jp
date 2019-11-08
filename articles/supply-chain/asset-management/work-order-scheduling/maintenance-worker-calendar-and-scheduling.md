---
title: メンテナンス作業者のカレンダーとスケジューリング
description: このトピックでは、資産管理のスケジューリングに関連するメンテナンス作業者のカレンダーについて説明します。
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: aa2d50a976af7ee7dde5335f94336b995fdc2d11
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652060"
---
# <a name="maintenance-worker-calendar-and-scheduling"></a><span data-ttu-id="c40bb-103">メンテナンス作業者のカレンダーとスケジューリング</span><span class="sxs-lookup"><span data-stu-id="c40bb-103">Maintenance worker calendar and scheduling</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c40bb-104">作業指示書をスケジュールする場合、メンテナンス作業者、ツール、および資産に対してスケジュールを作成します。</span><span class="sxs-lookup"><span data-stu-id="c40bb-104">When you schedule work orders, you create a schedule for maintenance workers, tools, and assets.</span></span> <span data-ttu-id="c40bb-105">メンテナンス作業者のスケジュールするには、各メンテナンス作業者に対してカレンダーを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c40bb-105">In order to schedule maintenance workers, a calendar must be set up for each maintenance worker.</span></span> <span data-ttu-id="c40bb-106">メンテナンス作業者はリソースに関連付けられ、作業時間カレンダーはリソースに対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="c40bb-106">Maintenance workers are related to a resource, and working time calendars are set up for resources.</span></span> <span data-ttu-id="c40bb-107">リソースおよびカレンダーは、**資産管理** > **設定** > **作業者** > **作業者**で設定することができ、[メンテナンス作業者と作業者グループ](../setup-for-objects/workers-and-worker-groups.md) で説明されています。</span><span class="sxs-lookup"><span data-stu-id="c40bb-107">You set up the resource and calendar in **Asset management** > **Setup** > **Workers** > **Workers**, which is described in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

<span data-ttu-id="c40bb-108">次のスクリーンショットは、「生産」の作業時間カレンダーを使用するリソースに関連付けられているメンテナンス作業者の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c40bb-108">The screenshot below shows an example of a maintenance worker who is related to a resource that uses the working time calendar "Production".</span></span>

![図 1](media/01-work-order-scheduling.png)

<span data-ttu-id="c40bb-110">ツールと資産のカレンダー設定は、作業指示書のスケジューリングに関連付けられている必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c40bb-110">Calendar setup for tools and assets is not needed in relation to work order scheduling.</span></span> <span data-ttu-id="c40bb-111">メンテナンスに対してツールと資産が 24 時間利用可能であることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="c40bb-111">The assumption is that tools and assets are available 24 hours a day for maintenance.</span></span>

