---
title: ジョブ カード デバイスからライセンス プレートにより制御されている場所への完了レポート
description: このトピックでは、場所がライセンス プレートによって制御される場合に、在庫への製造オーダーの完成品を完了させるプロセスについて説明します。
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: 63073035941cd2ef343c65364536fe76a9b71430
ms.sourcegitcommit: af36eb17b36092a3101bbfc96486b25036676558
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/06/2020
ms.locfileid: "2935125"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="0c664-103">ジョブ カード デバイスからライセンス プレートにより制御されている場所への完了レポート</span><span class="sxs-lookup"><span data-stu-id="0c664-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="0c664-104">完了レポートを呼び出したプロセスが在庫への製造オーダーの完成品を完了させます。</span><span class="sxs-lookup"><span data-stu-id="0c664-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="0c664-105">完成品が高度な倉庫管理プロセスに対して有効化されている場合、生産出荷の場所と呼ばれる場所に製品が完了したことが報告されます。</span><span class="sxs-lookup"><span data-stu-id="0c664-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="0c664-106">生産出荷の場所の設定の詳細については、[生産出荷の場所](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0c664-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="0c664-107">生産出荷の場所がライセンス プレートで管理されている場合は、完了報告時にライセンス プレートを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c664-107">If the production output location is license plate controlled, then a license plate must be provided when reporting as finished.</span></span> <span data-ttu-id="0c664-108">**ライセンス プレート** フィールドは、**ジョブ カード デバイス** ページの**進捗状況のレポート**の確認に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0c664-108">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="0c664-109">このフィールドは、製造オーダーの最後の工程を報告し、製造オーダーの品目が倉庫管理プロセスに対して有効になっている場合に、**進捗状況レポート**確認にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="0c664-109">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order and the item for the production order is enabled for the warehouse management processes.</span></span> 

<span data-ttu-id="0c664-110">ライセンス プレートを指定するには 2 つのオプションがあります</span><span class="sxs-lookup"><span data-stu-id="0c664-110">There are two options for providing the license plate</span></span>
- <span data-ttu-id="0c664-111">ユーザーは、ライセンス プレート フィールドで既存のライセンス プレートを選択しています。</span><span class="sxs-lookup"><span data-stu-id="0c664-111">The user is selecting an existing license plate in the license plate field.</span></span>
- <span data-ttu-id="0c664-112">ライセンス プレートは、番号順序から自動生成され、ライセンス プレート フィールドに既定値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="0c664-112">The license plate is automatically generated from a number sequence and defaulted to the license plate field.</span></span>

<span data-ttu-id="0c664-113">ライセンス プレートを自動生成するためのオプションをコンフィギュレーションするには、**デバイスのジョブ カードのコンフィギュレーション** ページの、**ライセンス プレートの作成**オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="0c664-113">The option to have the license plate generated automatically is configured by selecting the option **Generate license plate** on the **Configure job card for devices** page.</span></span>
