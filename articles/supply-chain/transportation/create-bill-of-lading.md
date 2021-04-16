---
title: 船荷証券の作成
description: このトピックでは、倉庫管理のプロセスを使用して、船荷証券の作成方法を説明します。
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a14d971475c71e6a02957acfa0c6e6494c4638fc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807635"
---
# <a name="create-a-bill-of-lading"></a><span data-ttu-id="dfed4-103">船荷証券の作成</span><span class="sxs-lookup"><span data-stu-id="dfed4-103">Create a bill of lading</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dfed4-104">このトピックでは、倉庫管理のプロセスを使用して、船荷証券の作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="dfed4-104">This topic describes how to create a bill of lading when using warehouse management processes.</span></span>  

<span data-ttu-id="dfed4-105">船荷証券は、配送業者と品目を出荷する会社間の法律文書です。</span><span class="sxs-lookup"><span data-stu-id="dfed4-105">A bill of lading is a legal document between the company that ships the items and the carrier.</span></span> <span data-ttu-id="dfed4-106">この文書は出荷済品目に添えられ、品目が宛先に配送されると出荷明細行として使用されます。</span><span class="sxs-lookup"><span data-stu-id="dfed4-106">The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination.</span></span> <span data-ttu-id="dfed4-107">倉庫管理を使用する場合は、船荷証券を生成する 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="dfed4-107">If you're using warehouse management, there are two ways to generate a bill of lading:</span></span>

  -   <span data-ttu-id="dfed4-108">**船荷証券** ページを使用してレポートを手動で作成します。</span><span class="sxs-lookup"><span data-stu-id="dfed4-108">Create the report manually, using the **Bill of lading** page.</span></span>
  -   <span data-ttu-id="dfed4-109">**積荷計画ワークベンチ** からレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="dfed4-109">Generate the report from the **Load planning workbench**.</span></span>

<span data-ttu-id="dfed4-110">**積荷計画ワークベンチ** から船荷証券を生成する場合は、積荷ステータスを **出荷済** にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dfed4-110">If you generate the bill of lading from the **Load planning workbench**, the load status must be **Shipped.**</span></span> <span data-ttu-id="dfed4-111">積荷に複数の出荷がある場合、船荷証券は各出荷ごとに生成されます。</span><span class="sxs-lookup"><span data-stu-id="dfed4-111">If there's more than one shipment in the load, a bill of lading is created for each shipment.</span></span> <span data-ttu-id="dfed4-112">船荷証券の作成後、**船荷証券** ページで変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="dfed4-112">After a bill of lading has been created you can make changes to it on the **Bill of lading** page.</span></span>

## <a name="master-bill-of-lading"></a><span data-ttu-id="dfed4-113">主船荷証券</span><span class="sxs-lookup"><span data-stu-id="dfed4-113">Master bill of lading</span></span>
<span data-ttu-id="dfed4-114">1 つの積荷に複数の出荷がある場合、主船荷証券を生成します。</span><span class="sxs-lookup"><span data-stu-id="dfed4-114">If there's more than one shipment in the load, you can generate a master bill of lading.</span></span> <span data-ttu-id="dfed4-115">これは船荷証券と同じレイアウトおよび情報がありますが、すべての出荷の集計されたコンテンツが含まれます。</span><span class="sxs-lookup"><span data-stu-id="dfed4-115">This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments.</span></span> <span data-ttu-id="dfed4-116">**輸送管理パラメーター** ページの **1 つの積荷に複数の出荷がある場合は主船荷証券を作成** オプションで **あり** を設定した場合、複数の出荷があるときに **積荷計画ワークベンチ** から主船荷証券を作成すると、主船荷証券が自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="dfed4-116">If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench**, and there's more than one shipment.</span></span> <span data-ttu-id="dfed4-117">**関連情報** &gt; **船荷証券** の順にクリックして船荷証券のリストを取得できます。</span><span class="sxs-lookup"><span data-stu-id="dfed4-117">You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**.</span></span> <span data-ttu-id="dfed4-118">船荷証券を手動で作成する場合は、**船荷証券** ページで主船荷証券を作成できます。</span><span class="sxs-lookup"><span data-stu-id="dfed4-118">If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]