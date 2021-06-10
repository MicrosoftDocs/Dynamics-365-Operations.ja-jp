---
title: 審査頻度の生成方法
description: このトピックでは、Dynamics 365 Human Resources における審査頻度の生成方法のオプション セットについて説明します。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae5ad3e556f40cedd385d8aadded9ef76447a98b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054095"
---
# <a name="screening-frequency-generate-from"></a><span data-ttu-id="bfa70-103">審査頻度の生成方法</span><span class="sxs-lookup"><span data-stu-id="bfa70-103">Screening frequency generate from</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bfa70-104">このトピックでは、Dynamics 365 Human Resources における審査頻度の生成方法のオプション セットについて説明します。</span><span class="sxs-lookup"><span data-stu-id="bfa70-104">This topic describes the Screening frequency generate from option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="bfa70-105">物理名 : mshr_hcmfrequencygeneratefrom</span><span class="sxs-lookup"><span data-stu-id="bfa70-105">Physical name: mshr_hcmfrequencygeneratefrom</span></span>

<span data-ttu-id="bfa70-106">このリストでは、次に必要な審査の計算開始日を決定するため値のオプションセットを提供します。</span><span class="sxs-lookup"><span data-stu-id="bfa70-106">This enumeration provides the option set of values for determining the start date of the calculation for the next required screening.</span></span>

| <span data-ttu-id="bfa70-107">先頭値</span><span class="sxs-lookup"><span data-stu-id="bfa70-107">Value</span></span> | <span data-ttu-id="bfa70-108">ラベル</span><span class="sxs-lookup"><span data-stu-id="bfa70-108">Label</span></span> | <span data-ttu-id="bfa70-109">説明</span><span class="sxs-lookup"><span data-stu-id="bfa70-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="bfa70-110">200000000 未選択</span><span class="sxs-lookup"><span data-stu-id="bfa70-110">200000000 Not selected</span></span> | <span data-ttu-id="bfa70-111">値が選択されていません。</span><span class="sxs-lookup"><span data-stu-id="bfa70-111">No value has been selected.</span></span> |
| <span data-ttu-id="bfa70-112">200000001 完了日</span><span class="sxs-lookup"><span data-stu-id="bfa70-112">200000001 Date completed</span></span> | <span data-ttu-id="bfa70-113">最終審査の完了日からの計算となります。</span><span class="sxs-lookup"><span data-stu-id="bfa70-113">Calculation is done from the last screening date completed.</span></span> |
| <span data-ttu-id="bfa70-114">200000002 必要な日付</span><span class="sxs-lookup"><span data-stu-id="bfa70-114">200000002 Date required</span></span> | <span data-ttu-id="bfa70-115">要求された審査の最終日から計算します。</span><span class="sxs-lookup"><span data-stu-id="bfa70-115">Calculation is done from the last screening date required.</span></span> |

## <a name="see-also"></a><span data-ttu-id="bfa70-116">参照</span><span class="sxs-lookup"><span data-stu-id="bfa70-116">See also</span></span>

[<span data-ttu-id="bfa70-117">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="bfa70-117">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="bfa70-118">採用する採用候補者に対するクエリの例</span><span class="sxs-lookup"><span data-stu-id="bfa70-118">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]