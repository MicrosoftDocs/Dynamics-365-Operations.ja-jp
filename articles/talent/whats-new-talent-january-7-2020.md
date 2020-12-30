---
title: Dynamics 365 Talent (2020 年 1 月 7 日) の新機能および変更された機能
description: この記事では、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
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
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461764"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a><span data-ttu-id="a840c-103">Dynamics 365 Talent (2020 年 1 月 7 日) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="a840c-103">What's new or changed in Dynamics 365 Talent (January 7, 2020)</span></span>

<span data-ttu-id="a840c-104">この記事では、Dynamics 365 Talent の新機能および変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="a840c-104">This article describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="a840c-105">Attract の変更</span><span class="sxs-lookup"><span data-stu-id="a840c-105">Changes in Attract</span></span>

<span data-ttu-id="a840c-106">今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a840c-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="a840c-107">Onboard の変更</span><span class="sxs-lookup"><span data-stu-id="a840c-107">Changes in Onboard</span></span>

<span data-ttu-id="a840c-108">今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a840c-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="a840c-109">Core HR の変更</span><span class="sxs-lookup"><span data-stu-id="a840c-109">Changes in Core HR</span></span>

<span data-ttu-id="a840c-110">このセクションに記載された変更は、ビルド番号 8.1.2697 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="a840c-110">Changes described in this section apply to build number 8.1.2697.</span></span> <span data-ttu-id="a840c-111">ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="a840c-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a><span data-ttu-id="a840c-112">雇用レコードがない作業者を削除できない - (386157)</span><span class="sxs-lookup"><span data-stu-id="a840c-112">Can't delete workers that don't have employment records - (386157)</span></span>

<span data-ttu-id="a840c-113">この変更により、**雇用なし作業者** フォームに削除オプションが追加されます。</span><span class="sxs-lookup"><span data-stu-id="a840c-113">This change adds a delete option in the **Workers without employment** form.</span></span> <span data-ttu-id="a840c-114">作業者の将来雇用、現職、または過去の職歴が存在しない場合は、作業者がこのフォームで表示されます。</span><span class="sxs-lookup"><span data-stu-id="a840c-114">Workers appear in this form when no future, active, or historical employments exist for the worker.</span></span> <span data-ttu-id="a840c-115">このリリースでは、システム管理者に対してのみ削除が有効になります。</span><span class="sxs-lookup"><span data-stu-id="a840c-115">In this release, delete is only enabled for System Administrators.</span></span> <span data-ttu-id="a840c-116">ただし、来週のリリースでは、HR アシスタント ロールのすべてのユーザーが雇用なし従業員を削除できるよう、セキュリティが更新されます。</span><span class="sxs-lookup"><span data-stu-id="a840c-116">However, in next week's release, security will be updated to allow all users with the HR assistant role to remove employees without employments.</span></span> <span data-ttu-id="a840c-117">これらの変更は、次の手順に従って手動で行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="a840c-117">You can also make these changes manually by following the following steps.</span></span>

1. <span data-ttu-id="a840c-118">**セキュリティのコンフィギュレーション** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a840c-118">Go to **Security configuration**.</span></span>
2. <span data-ttu-id="a840c-119">**権限** タブで、**権限** リストを **作業者の管理** にフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="a840c-119">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>
3. <span data-ttu-id="a840c-120">**参照** 列で、**メニュー項目の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a840c-120">In the **References** column, select **Display menu items**.</span></span>
4. <span data-ttu-id="a840c-121">**メニュー項目の表示** 列で、**HcmWOrkersWithoutEmployment** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a840c-121">In **Display menu items**, select **HcmWOrkersWithoutEmployment**.</span></span>
5. <span data-ttu-id="a840c-122">**削除** のアクセス許可を付与するよう設定します。</span><span class="sxs-lookup"><span data-stu-id="a840c-122">Set the **Delete** permission to Grant.</span></span>
6. <span data-ttu-id="a840c-123">**未公開のオブジェクト** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="a840c-123">Select the **Unpublished objects** tab.</span></span>
7. <span data-ttu-id="a840c-124">**すべて公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a840c-124">Select **Publish all**.</span></span>
