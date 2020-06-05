---
title: 会社間経費
description: 組織内の 1 つの法人で雇用されている作業者は、同じ組織の別の法人の作業を実行する場合があります。 この場合、会社間経費機能を使用して、作業が実行された法人に作業者の経費を割り当てることができます。
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390887"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="c1aad-104">会社間経費</span><span class="sxs-lookup"><span data-stu-id="c1aad-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1aad-105">組織内の 1 つの法人で雇用されている作業者は、同じ組織の別の法人の作業を実行する場合があります。</span><span class="sxs-lookup"><span data-stu-id="c1aad-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="c1aad-106">この場合、会社間経費機能を使用して、作業が実行された法人に作業者の経費を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="c1aad-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="c1aad-107">作業者を雇用する法人は、貸出側の法人と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="c1aad-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="c1aad-108">従業員が経費を支払う法人は、借入側法人と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="c1aad-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="c1aad-109">作業者が別の法人に対して実行される作業の経費を作成および送信する前に、貸出側法人で、**経費管理パラメーター** ページで **会社間経費明細行を許可** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c1aad-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="c1aad-110">会社間の経費の税金計上</span><span class="sxs-lookup"><span data-stu-id="c1aad-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1aad-111">経費精算書の借入先の法人に関連付けられている税グループを使用する場合は、総勘定元帳の売上税を設定する際にそれを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1aad-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="c1aad-112">総勘定元帳パラメータ ( **会社間税転記を行う法人)** が**ソース**に設定され、**売上税課税ルール** が **いいえ** に設定されている場合は、借入法人の税の組み合わせが使用されます。</span><span class="sxs-lookup"><span data-stu-id="c1aad-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="c1aad-113">同じパラメータが **宛先**に設定されている場合は 、借入法人の税の組み合わせが使用されます。</span><span class="sxs-lookup"><span data-stu-id="c1aad-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="c1aad-114">米国の法人で、パラメータが **ソース** に設定されている場合は、新しい **元帳転記グループ** ページでも **売上税収入** フィールドを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1aad-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="c1aad-115">会計エンジンでは、このフィールドの情報を税務関連の勘定項目に使用します。</span><span class="sxs-lookup"><span data-stu-id="c1aad-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="c1aad-116">この動作は、プロジェクトの有無に関わらず、経費明細行では一貫しています。</span><span class="sxs-lookup"><span data-stu-id="c1aad-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
