---
title: 定期的な与信管理タスク
description: このトピックでは、顧客の与信限度額を管理するために必要なプロセスの一部である定期処理タスクについて説明します。
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: df3b0b239fe542eab80fa92057248328d3f5188f
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015298"
---
# <a name="periodic-credit-management-tasks"></a><span data-ttu-id="e917b-103">定期的な与信管理タスク</span><span class="sxs-lookup"><span data-stu-id="e917b-103">Periodic credit management tasks</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e917b-104">このトピックでは、顧客の与信限度額を管理するために必要なプロセスの一部である定期処理タスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e917b-104">This topic describes the periodic tasks that are a necessary part of the process of managing credit limits for customers.</span></span>

## <a name="update-risk-scores"></a><span data-ttu-id="e917b-105">リスク スコアの更新</span><span class="sxs-lookup"><span data-stu-id="e917b-105">Update risk scores</span></span>

<span data-ttu-id="e917b-106">企業の進化や状況の変化に応じて、特定の顧客に対する与信リスクも変更する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e917b-106">As businesses evolve and circumstances change, the credit risks for a given customer can also change.</span></span> <span data-ttu-id="e917b-107">顧客に対して適切な与信限度額を維持するには、各リスク スコアの基準を定期的に確認し、各顧客のスコアを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e917b-107">To help maintain appropriate credit limits for your customers, you must periodically review the criteria for each risk score and update the scores for each customer.</span></span> <span data-ttu-id="e917b-108">**リスク スコアの更新**ページを使用して、次のスコアを更新することができます (**与信および回収\>定期処理タスク\>与信管理\>リスク スコアの更新**)。</span><span class="sxs-lookup"><span data-stu-id="e917b-108">You can update the following scores by using the **Update risk scores** page (**Credit and collections \> Periodic tasks \> Credit management \> Update risk scores**).</span></span> <span data-ttu-id="e917b-109">すべてのユーザー定義計算も処理されます。</span><span class="sxs-lookup"><span data-stu-id="e917b-109">All user-defined calculations are also processed.</span></span>

- <span data-ttu-id="e917b-110">**平均支払日数** - このスコアは、顧客が請求書の支払に要する平均日数です。</span><span class="sxs-lookup"><span data-stu-id="e917b-110">**Average payment days** – This score is the average number of days that a customer takes to pay invoices.</span></span>
- <span data-ttu-id="e917b-111">**初回購入** - このスコアは、顧客が組織の顧客であった年数を示します。</span><span class="sxs-lookup"><span data-stu-id="e917b-111">**Customer since** – This score is the number of years that a customer has been a customer of your organization.</span></span>
- <span data-ttu-id="e917b-112">**業務年数** - このスコアは、顧客が業務を行った年数です。</span><span class="sxs-lookup"><span data-stu-id="e917b-112">**In business since** – This score is the number of years that a customer has been in business.</span></span> <span data-ttu-id="e917b-113">**顧客**ページの**業務開始**フィールドの値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="e917b-113">It uses the value of the **Business start** field on the **Customers** page.</span></span>
- <span data-ttu-id="e917b-114">**売掛債権回転日数** - このスコアは、売掛金勘定残高、売上収益、および過去 12 か月間の日数に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="e917b-114">**Days sales outstanding** – This score is based on the accounts receivable balance, sales revenue, and number of days for the previous 12-month period.</span></span>
- <span data-ttu-id="e917b-115">**平均残高** - このスコアは、過去の 12 か月間の売掛金勘定残高に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="e917b-115">**Average balance** – This score is based on the accounts receivable balance for the previous 12-month period.</span></span>
- <span data-ttu-id="e917b-116">**与信管理グループ**、**アカウント ステータス**、および**国** - これらのスコアは、顧客からの情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="e917b-116">**Credit management group**, **Account status**, and **Country** – These scores use information from the customer.</span></span>

## <a name="update-customer-balance-statistics"></a><span data-ttu-id="e917b-117">顧客残高統計の更新</span><span class="sxs-lookup"><span data-stu-id="e917b-117">Update customer balance statistics</span></span>

<span data-ttu-id="e917b-118">**顧客残高統計**の更新プロセスを実行すると、**残高統計の照会**ページに表示される残高統計の計算を更新できます。</span><span class="sxs-lookup"><span data-stu-id="e917b-118">You can run the **Update customer balance statistics** process to update the calculation of balance statistics that is shown on the **Balance statistics inquiry** page.</span></span> <span data-ttu-id="e917b-119">この情報は、リスクのスコアと、**顧客**ページの与信統計情報ボックスに表示される値を計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e917b-119">This information is used to calculate risk scores and the values that are shown in the credit statistics FactBoxes on the **Customer** page.</span></span>

<span data-ttu-id="e917b-120">プロセスを実行すると、単一の顧客の顧客残高統計が更新されます。</span><span class="sxs-lookup"><span data-stu-id="e917b-120">When you run the process, it updates customer balance statistics for a single customer.</span></span> <span data-ttu-id="e917b-121">複数の顧客に対してプロセスを実行するバッチ ジョブを設定するには、**残高統計の計算**ページ (**与信管理\>定期処理のタスク\>残高統計の計算**) を使用します。</span><span class="sxs-lookup"><span data-stu-id="e917b-121">To set up a batch job to run the process for multiple customers, you can use the **Calculate balance statistics** page (**Credit management \> Periodic tasks \> Calculate balance statistics**).</span></span>
