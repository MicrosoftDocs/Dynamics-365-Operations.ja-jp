---
title: ジョブの詳細 API
description: このトピックでは、Dynamics 365 Human Resources におけるジョブの詳細エンティティに対するクエリの詳細および例を示します。
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 562b9f505311b6cfe505a76fc5c0a384eb641936
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054767"
---
# <a name="job-detail-api"></a><span data-ttu-id="a2e09-103">ジョブの詳細 API</span><span class="sxs-lookup"><span data-stu-id="a2e09-103">Job detail API</span></span>

<span data-ttu-id="a2e09-104">このトピックでは、Dynamics 365 Human Resources におけるジョブの詳細エンティティに対するクエリの詳細および例を示します。</span><span class="sxs-lookup"><span data-stu-id="a2e09-104">This topic provides details and an example query for the Job detail entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="a2e09-105">プロパティ</span><span class="sxs-lookup"><span data-stu-id="a2e09-105">Properties</span></span>

| <span data-ttu-id="a2e09-106">プロパティ</span><span class="sxs-lookup"><span data-stu-id="a2e09-106">Property</span></span><br><span data-ttu-id="a2e09-107">**現物名**</span><span class="sxs-lookup"><span data-stu-id="a2e09-107">**Physical name**</span></span><br><span data-ttu-id="a2e09-108">**_種類_**</span><span class="sxs-lookup"><span data-stu-id="a2e09-108">**_Type_**</span></span> | <span data-ttu-id="a2e09-109">使用</span><span class="sxs-lookup"><span data-stu-id="a2e09-109">Use</span></span> | <span data-ttu-id="a2e09-110">説明</span><span class="sxs-lookup"><span data-stu-id="a2e09-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a2e09-111">**ジョブ ID**</span><span class="sxs-lookup"><span data-stu-id="a2e09-111">**Job ID**</span></span><br><span data-ttu-id="a2e09-112">mshr_jobid</span><span class="sxs-lookup"><span data-stu-id="a2e09-112">mshr_jobid</span></span><br><span data-ttu-id="a2e09-113">*文字列*</span><span class="sxs-lookup"><span data-stu-id="a2e09-113">*String*</span></span> | <span data-ttu-id="a2e09-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a2e09-114">Read-only</span></span><br><span data-ttu-id="a2e09-115">必須</span><span class="sxs-lookup"><span data-stu-id="a2e09-115">Required</span></span> | <span data-ttu-id="a2e09-116">ジョブの固有 ID。</span><span class="sxs-lookup"><span data-stu-id="a2e09-116">Unique ID for a job.</span></span> |
| <span data-ttu-id="a2e09-117">**市場価格の低しきい値**</span><span class="sxs-lookup"><span data-stu-id="a2e09-117">**Market price low threshold**</span></span><br><span data-ttu-id="a2e09-118">mshr_marketpricelowthreshold</span><span class="sxs-lookup"><span data-stu-id="a2e09-118">mshr_marketpricelowthreshold</span></span><br><span data-ttu-id="a2e09-119">*実数*</span><span class="sxs-lookup"><span data-stu-id="a2e09-119">*Decimal*</span></span> | | <span data-ttu-id="a2e09-120">職位を一意に識別するためのシステム生成の GUID 値。</span><span class="sxs-lookup"><span data-stu-id="a2e09-120">A system-generated GUID value to uniquely identify the position.</span></span>  |
