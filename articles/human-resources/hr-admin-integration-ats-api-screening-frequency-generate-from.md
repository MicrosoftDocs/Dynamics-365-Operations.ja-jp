---
title: 審査頻度の生成方法
description: このトピックでは、Dynamics 365 Human Resources における審査頻度の生成方法のオプション セットについて説明します。
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f291e28584dadc465092d99a1354fda793ff7560
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126149"
---
# <a name="screening-frequency-generate-from"></a><span data-ttu-id="a5319-103">審査頻度の生成方法</span><span class="sxs-lookup"><span data-stu-id="a5319-103">Screening frequency generate from</span></span>

<span data-ttu-id="a5319-104">このトピックでは、Dynamics 365 Human Resources における審査頻度の生成方法のオプション セットについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a5319-104">This topic describes the Screening frequency generate from option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="a5319-105">物理名 : mshr_hcmfrequencygeneratefrom</span><span class="sxs-lookup"><span data-stu-id="a5319-105">Physical name: mshr_hcmfrequencygeneratefrom</span></span>

<span data-ttu-id="a5319-106">このリストでは、次に必要な審査の計算開始日を決定するため値のオプションセットを提供します。</span><span class="sxs-lookup"><span data-stu-id="a5319-106">This enumeration provides the option set of values for determining the start date of the calculation for the next required screening.</span></span>

| <span data-ttu-id="a5319-107">先頭値</span><span class="sxs-lookup"><span data-stu-id="a5319-107">Value</span></span> | <span data-ttu-id="a5319-108">ラベル</span><span class="sxs-lookup"><span data-stu-id="a5319-108">Label</span></span> | <span data-ttu-id="a5319-109">説明</span><span class="sxs-lookup"><span data-stu-id="a5319-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a5319-110">200000000 未選択</span><span class="sxs-lookup"><span data-stu-id="a5319-110">200000000 Not selected</span></span> | <span data-ttu-id="a5319-111">値が選択されていません。</span><span class="sxs-lookup"><span data-stu-id="a5319-111">No value has been selected.</span></span> |
| <span data-ttu-id="a5319-112">200000001 完了日</span><span class="sxs-lookup"><span data-stu-id="a5319-112">200000001 Date completed</span></span> | <span data-ttu-id="a5319-113">最終審査の完了日からの計算となります。</span><span class="sxs-lookup"><span data-stu-id="a5319-113">Calculation is done from the last screening date completed.</span></span> |
| <span data-ttu-id="a5319-114">200000002 必要な日付</span><span class="sxs-lookup"><span data-stu-id="a5319-114">200000002 Date required</span></span> | <span data-ttu-id="a5319-115">要求された審査の最終日から計算します。</span><span class="sxs-lookup"><span data-stu-id="a5319-115">Calculation is done from the last screening date required.</span></span> |

## <a name="see-also"></a><span data-ttu-id="a5319-116">参照</span><span class="sxs-lookup"><span data-stu-id="a5319-116">See also</span></span>

[<span data-ttu-id="a5319-117">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="a5319-117">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="a5319-118">採用する採用候補者に対するクエリの例</span><span class="sxs-lookup"><span data-stu-id="a5319-118">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
