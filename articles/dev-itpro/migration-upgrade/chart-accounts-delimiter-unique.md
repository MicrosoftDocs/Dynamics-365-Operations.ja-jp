---
title: 勘定科目表の区切り記号を一意にする
description: Dynamics 365 for Finance and Operations では、勘定科目表と分析コード値の同じ区切り記号を所有できません。 アップグレード後に区切り記号値を変更する必要があります。
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559531"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a><span data-ttu-id="985a7-104">勘定科目表の区切り記号を一意にする</span><span class="sxs-lookup"><span data-stu-id="985a7-104">Make the chart of accounts delimiter unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="985a7-105">Microsoft Dynamics AX 2012 では、勘定科目表および分析コード値に対して、同じ区切り記号を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="985a7-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="985a7-106">Dynamics 365 for Finance and Operations では、勘定科目表と分析コード値の同じ区切り記号を所有できません。</span><span class="sxs-lookup"><span data-stu-id="985a7-106">In Dynamics 365 for Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="985a7-107">重複する区切り記号がある場合、アップグレード後に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="985a7-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="985a7-108">この機能は次で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="985a7-108">This feature is available in:</span></span>
- <span data-ttu-id="985a7-109">Dynamics 365 for Finance and Operations バージョン 8.0</span><span class="sxs-lookup"><span data-stu-id="985a7-109">Dynamics 365 for Finance and Operations version 8.0</span></span>
- <span data-ttu-id="985a7-110">Dynamics 365 for Finance and Operations バージョン 7.1、KB 4094701 は、分析コード値が勘定科目表の区切り記号を含んでいる場合、財務分析コードを入力することができません</span><span class="sxs-lookup"><span data-stu-id="985a7-110">Dynamics 365 for Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="985a7-111">Dynamics 365 for Finance and Operations バージョン 7.2、KB 4092967 は、下位プロジェクトの形式が分析コードの区切り記号を含んでいる場合、は下位プロジェクトを分析コードとして選択することができません</span><span class="sxs-lookup"><span data-stu-id="985a7-111">Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="985a7-112">区切り記号の更新</span><span class="sxs-lookup"><span data-stu-id="985a7-112">Update delimiter</span></span>
<span data-ttu-id="985a7-113">勘定科目表との競合が発生している場合、勘定科目表の区切り記号およびプロジェクト/下位プロジェクト ID の形式は変更できません。</span><span class="sxs-lookup"><span data-stu-id="985a7-113">If there is a conflict with the Chart of Accounts, the Chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="985a7-114">その他の分析コードの区切り記号を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="985a7-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="985a7-115">**一般会計パラメーター** > **勘定科目表および分析コード** > **区切り記号を変更**で Finance and Operations をアップグレード後、勘定科目表の区切り記号を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="985a7-115">You can change the chart of accounts delimiter after upgrade to Finance and Operations in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="985a7-116">競合が、プロジェクト/下位プロジェクト ID の形式にのみ発生している場合、**プロジェクト管理および会計パラメーター** > **一般** > **下位プロジェクト形式を変更する**の値を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="985a7-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="985a7-117">更新された区切り記号が環境で必要かどうかを判断する方法</span><span class="sxs-lookup"><span data-stu-id="985a7-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="985a7-118">アップグレードされた環境の区切り記号が競合している場合、セグメント化エントリ コントロールまたは分析コード エントリ コントロールに値を入力する際に動作が不安定になることがあります</span><span class="sxs-lookup"><span data-stu-id="985a7-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="985a7-119">つまり、勘定と分析コードの組み合わせを入力するときは、ルックアップまたはポップ アップ メニューを常に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="985a7-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>
