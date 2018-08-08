---
title: "船荷証券の作成"
description: "このトピックでは、倉庫管理のプロセスを使用して、船荷証券の作成方法を説明します。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 8d5caed5553ad1c7aec5db83591024129aab1264
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---

# <a name="create-a-bill-of-lading"></a><span data-ttu-id="9979f-103">船荷証券の作成</span><span class="sxs-lookup"><span data-stu-id="9979f-103">Create a bill of lading</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9979f-104">このトピックでは、倉庫管理のプロセスを使用して、船荷証券の作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="9979f-104">This topic describes how to create a bill of lading when using warehouse management processes.</span></span>  

<span data-ttu-id="9979f-105">船荷証券は、配送業者と品目を出荷する会社間の法律文書です。</span><span class="sxs-lookup"><span data-stu-id="9979f-105">A bill of lading is a legal document between the company that ships the items and the carrier.</span></span> <span data-ttu-id="9979f-106">この文書は出荷済品目に添えられ、品目が宛先に配送されると出荷明細行として使用されます。</span><span class="sxs-lookup"><span data-stu-id="9979f-106">The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination.</span></span> <span data-ttu-id="9979f-107">倉庫管理を使用する場合は、船荷証券を生成する 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="9979f-107">If you're using warehouse management, there are two ways to generate a bill of lading:</span></span>

  -   <span data-ttu-id="9979f-108">[船荷証券] ページを使用してレポートを手動で作成します。</span><span class="sxs-lookup"><span data-stu-id="9979f-108">Create the report manually, using the **Bill of lading** page.</span></span>
  -   <span data-ttu-id="9979f-109">[積荷計画ワークベンチ] からレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="9979f-109">Generate the report from the **Load planning workbench**.</span></span>

<span data-ttu-id="9979f-110">[積荷計画ワークベンチ] から船荷証券を生成する場合は、積荷ステータスを [出荷済] にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9979f-110">If you generate the bill of lading from the **Load planning workbench**, the load status must be **Shipped.**</span></span> <span data-ttu-id="9979f-111">積荷に複数の出荷がある場合、船荷証券は各出荷ごとに生成されます。</span><span class="sxs-lookup"><span data-stu-id="9979f-111">If there's more than one shipment in the load, a bill of lading is created for each shipment.</span></span> <span data-ttu-id="9979f-112">船荷証券の作成後、[船荷証券] ページで変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="9979f-112">After a bill of lading has been created you can make changes to it on the **Bill of lading** page.</span></span>

## <a name="master-bill-of-lading"></a><span data-ttu-id="9979f-113">主船荷証券</span><span class="sxs-lookup"><span data-stu-id="9979f-113">Master bill of lading</span></span>
<span data-ttu-id="9979f-114">1 つの積荷に複数の出荷がある場合、主船荷証券を生成します。</span><span class="sxs-lookup"><span data-stu-id="9979f-114">If there's more than one shipment in the load, you can generate a master bill of lading.</span></span> <span data-ttu-id="9979f-115">これは船荷証券と同じレイアウトおよび情報がありますが、すべての出荷の集計されたコンテンツが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9979f-115">This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments.</span></span> <span data-ttu-id="9979f-116">[輸送管理パラメーター] ページの [1 つの積荷に複数の出荷がある場合は主船荷証券を作成] オプションで [あり] を設定した場合、複数の出荷があるときに [積荷計画ワークベンチ] から主船荷証券を作成すると、主船荷証券が自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="9979f-116">If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench**, and there's more than one shipment.</span></span> <span data-ttu-id="9979f-117">[関連情報] &gt; [船荷証券] の順にクリックして船荷証券のリストを取得できます。</span><span class="sxs-lookup"><span data-stu-id="9979f-117">You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**.</span></span> <span data-ttu-id="9979f-118">船荷証券を手動で作成する場合は、[船荷証券] ページで主船荷証券を作成できます。</span><span class="sxs-lookup"><span data-stu-id="9979f-118">If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.</span></span>




