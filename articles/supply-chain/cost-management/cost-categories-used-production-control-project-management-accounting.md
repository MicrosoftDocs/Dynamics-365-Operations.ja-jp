---
title: 生産管理、およびプロジェクト管理会計で使用される原価カテゴリ
description: 生産作業によっては、プロジェクト時間の見積と報告に適用できます。 この記事は、生産とプロジェクトのために、これらの種類の生産作業に定義する必要のある原価カテゴリに関する情報を提供します。
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCategory
audience: Application User
ms.reviewer: kamaybac
ms.custom: 78253
ms.assetid: cfdd58a0-8afa-4a6f-a208-a76e2c162429
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 540d020820222b024f838f8156aaef823605e950
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228710"
---
# <a name="cost-categories-used-in-production-control-and-project-management-accounting"></a><span data-ttu-id="dd62c-104">生産管理、およびプロジェクト管理会計で使用される原価カテゴリ</span><span class="sxs-lookup"><span data-stu-id="dd62c-104">Cost categories used in Production control and Project management accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd62c-105">生産作業によっては、プロジェクト時間の見積と報告に適用できます。</span><span class="sxs-lookup"><span data-stu-id="dd62c-105">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="dd62c-106">この記事は、生産とプロジェクトのために、これらの種類の生産作業に定義する必要のある原価カテゴリに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="dd62c-106">This article provides information about the cost categories that you must define for these types of production work for production and project purposes.</span></span>

<span data-ttu-id="dd62c-107">生産作業によっては、プロジェクト時間の見積と報告に適用できます。</span><span class="sxs-lookup"><span data-stu-id="dd62c-107">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="dd62c-108">この場合、生産とプロジェクトのために原価カテゴリが必要です。</span><span class="sxs-lookup"><span data-stu-id="dd62c-108">In this case, a cost category is required for production and project purposes.</span></span> <span data-ttu-id="dd62c-109">原価カテゴリを生産とプロジェクトで使用する場合は、プロジェクト関連の追加情報を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd62c-109">When a cost category is used in production and projects, additional project-related information must be defined.</span></span> <span data-ttu-id="dd62c-110">たとえば、プロジェクトに関連付けられた時間原価は、生産に関連付けられた時間原価と異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="dd62c-110">For example, the hourly costs that are associated with projects can differ from the hourly costs that are associated with production.</span></span> <span data-ttu-id="dd62c-111">生産管理とプロジェクト管理会計で使用される原価カテゴリを定義するには、**原価カテゴリ** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="dd62c-111">You can use the **Cost categories** page to define a cost category that is used in Production control and Project management accounting.</span></span> 

<span data-ttu-id="dd62c-112">**メモ:** 原価計算には **プロジェクト カテゴリ** ページが含まれますが、このページはこのトピックで説明する機能とは関係ありません。</span><span class="sxs-lookup"><span data-stu-id="dd62c-112">**Note:** Cost accounting has a **Project categories** page, but this page has no relationship to the functionality that is described in this topic.</span></span> <span data-ttu-id="dd62c-113">プロジェクトで原価カテゴリを使用する場合、**原価カテゴリ** ページには追加のプロジェクト関連情報を表示する追加のタブがあります。</span><span class="sxs-lookup"><span data-stu-id="dd62c-113">When you use a cost category in projects, the **Cost categories** page has additional tabs that show additional project-related information.</span></span> <span data-ttu-id="dd62c-114">この情報には、カテゴリ グループ、明細行プロパティ、および原価カテゴリに割り当てられている勘定科目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="dd62c-114">This information includes the category group, a line property, and ledger accounts that are assigned to the cost category.</span></span>

-   <span data-ttu-id="dd62c-115">原価カテゴリは、**時間** のトランザクション タイプをサポートするカテゴリ グループに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd62c-115">The cost category must be assigned to a category group that supports a transaction type of **Hours**.</span></span>
-   <span data-ttu-id="dd62c-116">明細行プロパティは、報告される時間をプロジェクトの課金対象にする方法についての既定情報を示します。</span><span class="sxs-lookup"><span data-stu-id="dd62c-116">The line property indicates default information about how reported time can be charged to a project.</span></span>
-   <span data-ttu-id="dd62c-117">通常、原価および販売に関連する勘定科目は、原価カテゴリに割り当てられるカテゴリ グループに対して定義されます。</span><span class="sxs-lookup"><span data-stu-id="dd62c-117">Typically, the ledger accounts that are related to costs and sales are defined for the category group that is assigned to the cost category.</span></span> <span data-ttu-id="dd62c-118">ただし、特定の勘定を個別の原価カテゴリに対して定義できます。</span><span class="sxs-lookup"><span data-stu-id="dd62c-118">However, specific accounts can be defined for an individual cost category.</span></span>

<span data-ttu-id="dd62c-119">**原価カテゴリ** ページの新しいボタンを使用すると、選択した原価カテゴリに関するプロジェクト関連情報にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="dd62c-119">Additional buttons on the **Cost categories** page let you access project-related information about a selected cost category.</span></span> <span data-ttu-id="dd62c-120">たとえば、プロジェクト関連のトランザクションの表示、従業員やプロジェクトの定義、時間単位の原価と販売価格の定義、レポートの表示を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="dd62c-120">For example, you can view project-related transactions, define employees or projects, define hourly costs and sales prices, and view reports.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]