---
title: 経費精算書での個人経費
description: このトピックでは、作業者の個人経費を Microsoft Dynamics 365 Finance で処理するための 2 つの方法を説明します。
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178652"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="552f5-103">経費精算書での個人経費</span><span class="sxs-lookup"><span data-stu-id="552f5-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="552f5-104">出張中に、作業者は、会社のクレジット カードで個人経費を支払う場合があります。</span><span class="sxs-lookup"><span data-stu-id="552f5-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="552f5-105">個人経費を取扱うプロセスを定義していない場合は、作業員が経費明細精算書を提出すると、経費精算書承認プロセスが混乱する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="552f5-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="552f5-106">作業者の個人経費を処理する 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="552f5-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="552f5-107">**従業員による支払** – 組織は、会社のクレジット カードの請求に表示される個人経費を支払いません。</span><span class="sxs-lookup"><span data-stu-id="552f5-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="552f5-108">代わりに、会社のクレジット カードに請求された会社経費と共に個人経費を表示するレポートを作成します。</span><span class="sxs-lookup"><span data-stu-id="552f5-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="552f5-109">**会社による支払** – 組織は、法人のクレジット カードの請求を全額支払った後に、個人経費を作業者の勘定の借方に転記します。</span><span class="sxs-lookup"><span data-stu-id="552f5-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="552f5-110">**経費管理パラメーター**ページで組織が使用する方法を選択できます。</span><span class="sxs-lookup"><span data-stu-id="552f5-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>