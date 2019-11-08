---
title: ジョブ カード デバイスからライセンス プレートにより制御されている場所への完了レポート
description: このトピックでは、場所がライセンス プレートによって制御される場合に、在庫への製造オーダーの完成品を完了させるプロセスについて説明します。
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: cb809e596fd6bf3030bcee460838798435512b95
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572132"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="1684d-103">ジョブ カード デバイスからライセンス プレートにより制御されている場所への完了レポート</span><span class="sxs-lookup"><span data-stu-id="1684d-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="1684d-104">完了レポートを呼び出したプロセスが在庫への製造オーダーの完成品を完了させます。</span><span class="sxs-lookup"><span data-stu-id="1684d-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="1684d-105">完成品が高度な倉庫管理プロセスに対して有効化されている場合、生産出荷の場所と呼ばれる場所に製品が完了したことが報告されます。</span><span class="sxs-lookup"><span data-stu-id="1684d-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="1684d-106">生産出荷の場所の設定の詳細については、[生産出荷の場所](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1684d-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="1684d-107">このタスクを完了するには、既存のライセンス プレート番号を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1684d-107">You must select an existing license plate number to complete this task.</span></span> <span data-ttu-id="1684d-108">生産出荷の場所をライセンス プレート別に追跡するように設定している場合、生産出荷の場所を完了として報告する時に、ライセンス プレート番号を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="1684d-108">If the production output location is set up to be tracked by license plate, then a license plate number must be included when reporting the production output location as finished.</span></span> <span data-ttu-id="1684d-109">**ライセンス プレート** フィールドは、**ジョブ カード デバイス** ページの**進捗状況のレポート**の確認に表示されます。</span><span class="sxs-lookup"><span data-stu-id="1684d-109">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="1684d-110">このフィールドは、製造オーダーの最後の工程を報告する時、**進捗状況のレポート**の確認にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="1684d-110">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order.</span></span> <span data-ttu-id="1684d-111">このフィールドは、製造オーダーの品目が倉庫管理プロセスに対して有効化されている場合にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="1684d-111">The field is only shown if the item for the production order is enabled for the warehouse management processes.</span></span> 
