---
title: Dynamics 365 for Talent の新機能および変更された機能 (2019 年 2 月 14 日)
description: このトピックでは、Microsoft Dynamics 365 for Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1db7d032eade3f996e0554e64d6ea0704a347ed8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518436"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-14-2019"></a><span data-ttu-id="8a3ec-103">Dynamics 365 for Talent の新機能および変更された機能 (2019 年 2 月 14 日)</span><span class="sxs-lookup"><span data-stu-id="8a3ec-103">What's new or changed in Dynamics 365 for Talent (February 14, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8a3ec-104">このトピックでは、 Talent の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="8a3ec-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="8a3ec-105">Attract の変更</span><span class="sxs-lookup"><span data-stu-id="8a3ec-105">Changes in Attract</span></span>
<span data-ttu-id="8a3ec-106">このリリースには、マイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8a3ec-106">There are minor bug fixes included with this release.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="8a3ec-107">オンボードの変更</span><span class="sxs-lookup"><span data-stu-id="8a3ec-107">Changes in Onboarding</span></span>
<span data-ttu-id="8a3ec-108">このリリースには、マイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8a3ec-108">There are minor bug fixes included with this release.</span></span>
 
## <a name="changes-in-core-hr"></a><span data-ttu-id="8a3ec-109">Core HR の変更</span><span class="sxs-lookup"><span data-stu-id="8a3ec-109">Changes in Core HR</span></span> 
<span data-ttu-id="8a3ec-110">**ビルド 8.1.2146**</span><span class="sxs-lookup"><span data-stu-id="8a3ec-110">**Build 8.1.2146**</span></span>

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a><span data-ttu-id="8a3ec-111">従業員の固定報酬のエンティティは、すべてのレコードをエクスポートしない</span><span class="sxs-lookup"><span data-stu-id="8a3ec-111">Employee fixed compensation entity doesn't export all records</span></span>
<span data-ttu-id="8a3ec-112">この変更により、**従業員の固定報酬**エンティティですべてのレコードをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="8a3ec-112">With this change, the **Employee fixed compensation** entity will now export all records.</span></span> <span data-ttu-id="8a3ec-113">既存の従業員の固定報酬レコードを作成および更新するためにエンティティを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="8a3ec-113">The entity can be used to create and update existing fixed compensation records for employees.</span></span> 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a><span data-ttu-id="8a3ec-114">雇用終了日が従業員の優先タイム ゾーンの設定を遵守しない</span><span class="sxs-lookup"><span data-stu-id="8a3ec-114">Employment end date doesn't honor employee preferred time zone settings</span></span>
<span data-ttu-id="8a3ec-115">会社での雇用を作成または終了するときに、雇用終了日がユーザーの優先タイムゾーンを遵守するようになりました。</span><span class="sxs-lookup"><span data-stu-id="8a3ec-115">Employment end dates are now honoring the user-preferred time zone when creating or ending employment with a company.</span></span>
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a><span data-ttu-id="8a3ec-116">Analytics で英国の住所が東部スイスの住所として表示される</span><span class="sxs-lookup"><span data-stu-id="8a3ec-116">UK addresses display in Analytics as Eastern Switzerland addresses</span></span>
<span data-ttu-id="8a3ec-117">今回のリリースで、**人事管理**「場所別の人数」レポートでの住所の不整合を修正する変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="8a3ec-117">In this release, a change has been made to correct misalignment in addresses in the **Personnel Management** "Headcount by location" report.</span></span>
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a><span data-ttu-id="8a3ec-118">職位の終了時に、作業者の職位の割り当てレコードに退職コードが設定されない</span><span class="sxs-lookup"><span data-stu-id="8a3ec-118">Termination code is not populated on the worker position assignment record when ending the position</span></span>
<span data-ttu-id="8a3ec-119">従業員の職位の割り当ての終了時に、「退職理由」コードを既定として設定する変更が加えられました。</span><span class="sxs-lookup"><span data-stu-id="8a3ec-119">A change has been made to default the "Termination reason" code when ending the employees position assignment.</span></span>

### <a name="new-entity-created-for-job-compensation-levels"></a><span data-ttu-id="8a3ec-120">ジョブの報酬レベルに対して作成された新しいエンティティ</span><span class="sxs-lookup"><span data-stu-id="8a3ec-120">New entity created for job compensation levels</span></span>
<span data-ttu-id="8a3ec-121">新しいデータ管理フレームワーク (DMF) エンティティが作成されました。</span><span class="sxs-lookup"><span data-stu-id="8a3ec-121">A new data management framework (DMF) entity was created.</span></span> <span data-ttu-id="8a3ec-122">エンティティは、報酬レベル、市場価値、およびシステムで定義されている各ジョブの調査情報の作成と更新を提供します。</span><span class="sxs-lookup"><span data-stu-id="8a3ec-122">The entity provides for creation and updates to compensation levels, market values, and survey information for each job defined in the system.</span></span>
