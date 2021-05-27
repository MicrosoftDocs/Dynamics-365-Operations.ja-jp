---
title: ジョブの詳細 API
description: このトピックでは、Dynamics 365 Human Resources におけるジョブの詳細エンティティに対するクエリの詳細および例を示します。
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c92b0636fbd68c6ee7eded90a8cb5bcd0cda7ca3
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018365"
---
# <a name="job-detail-api"></a><span data-ttu-id="3ac3e-103">ジョブの詳細 API</span><span class="sxs-lookup"><span data-stu-id="3ac3e-103">Job detail API</span></span>

<span data-ttu-id="3ac3e-104">このトピックでは、Dynamics 365 Human Resources におけるジョブの詳細エンティティに対するクエリの詳細および例を示します。</span><span class="sxs-lookup"><span data-stu-id="3ac3e-104">This topic provides details and an example query for the Job detail entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="3ac3e-105">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3ac3e-105">Properties</span></span>

| <span data-ttu-id="3ac3e-106">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3ac3e-106">Property</span></span><br><span data-ttu-id="3ac3e-107">**現物名**</span><span class="sxs-lookup"><span data-stu-id="3ac3e-107">**Physical name**</span></span><br><span data-ttu-id="3ac3e-108">**_種類_**</span><span class="sxs-lookup"><span data-stu-id="3ac3e-108">**_Type_**</span></span> | <span data-ttu-id="3ac3e-109">使用</span><span class="sxs-lookup"><span data-stu-id="3ac3e-109">Use</span></span> | <span data-ttu-id="3ac3e-110">説明</span><span class="sxs-lookup"><span data-stu-id="3ac3e-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3ac3e-111">**ジョブ ID**</span><span class="sxs-lookup"><span data-stu-id="3ac3e-111">**Job ID**</span></span><br><span data-ttu-id="3ac3e-112">mshr_jobid</span><span class="sxs-lookup"><span data-stu-id="3ac3e-112">mshr_jobid</span></span><br><span data-ttu-id="3ac3e-113">*文字列*</span><span class="sxs-lookup"><span data-stu-id="3ac3e-113">*String*</span></span> | <span data-ttu-id="3ac3e-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3ac3e-114">Read-only</span></span><br><span data-ttu-id="3ac3e-115">必須</span><span class="sxs-lookup"><span data-stu-id="3ac3e-115">Required</span></span> | <span data-ttu-id="3ac3e-116">ジョブの固有 ID。</span><span class="sxs-lookup"><span data-stu-id="3ac3e-116">Unique ID for a job.</span></span> |
| <span data-ttu-id="3ac3e-117">**市場価格の低しきい値**</span><span class="sxs-lookup"><span data-stu-id="3ac3e-117">**Market price low threshold**</span></span><br><span data-ttu-id="3ac3e-118">mshr_marketpricelowthreshold</span><span class="sxs-lookup"><span data-stu-id="3ac3e-118">mshr_marketpricelowthreshold</span></span><br><span data-ttu-id="3ac3e-119">*実数*</span><span class="sxs-lookup"><span data-stu-id="3ac3e-119">*Decimal*</span></span> | | <span data-ttu-id="3ac3e-120">職位を一意に識別するためのシステム生成の GUID 値。</span><span class="sxs-lookup"><span data-stu-id="3ac3e-120">A system-generated GUID value to uniquely identify the position.</span></span>  |
