---
title: Dynamics 365 Talent - Core HR (2018 年 9 月 24 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent - Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 09/21/2018
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
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e0c1a3bf7613db4887e0943a70ad6262a70997f0
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898969"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-24-2018"></a><span data-ttu-id="2c228-103">Dynamics 365 Talent - Core HR (2018 年 9 月 24 日) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="2c228-103">What's new or changed in Dynamics 365 Talent - Core HR (September 24, 2018)</span></span>

<span data-ttu-id="2c228-104">**ビルド 8.1.1015.0**</span><span class="sxs-lookup"><span data-stu-id="2c228-104">**Build 8.1.1015.0**</span></span>

<span data-ttu-id="2c228-105">このトピックでは、Core HR の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="2c228-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="currency-added-to-benefits"></a><span data-ttu-id="2c228-106">給付金に追加された通貨</span><span class="sxs-lookup"><span data-stu-id="2c228-106">Currency added to Benefits</span></span>

<span data-ttu-id="2c228-107">給付金の通貨を含めるため、福利厚生計画が更新されました。</span><span class="sxs-lookup"><span data-stu-id="2c228-107">Benefit plans have been updated to include the currency of the benefit.</span></span> <span data-ttu-id="2c228-108">この新しいフィールドも作業者が登録されている給付金に使用できます。</span><span class="sxs-lookup"><span data-stu-id="2c228-108">This new field is also available on worker enrolled benefits.</span></span> <span data-ttu-id="2c228-109">この新しいフィールドは、給付金の管理および給付金のセキュリティ権限の一覧表示の一部です。</span><span class="sxs-lookup"><span data-stu-id="2c228-109">This new field is part of the Maintain benefits and View a list of benefits security privilege.</span></span>

## <a name="update-proration-process--leave-and-absence"></a><span data-ttu-id="2c228-110">比例配分処理の更新 – 休暇と欠勤</span><span class="sxs-lookup"><span data-stu-id="2c228-110">Update proration process – Leave and Absence</span></span>

<span data-ttu-id="2c228-111">組織は、従業員の入社日および退社日に基づいて、休暇を別々に付与します。</span><span class="sxs-lookup"><span data-stu-id="2c228-111">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="2c228-112">組織を退職する従業員については、退職日に報奨を終了する必要がある場合もあれば、見越計上処理を停止する勤務最終日に依存する場合もあります。</span><span class="sxs-lookup"><span data-stu-id="2c228-112">For employees leaving the organization, some may need to end the award on the termination date, while others rely on the last day worked to stop the accrual process.</span></span> <span data-ttu-id="2c228-113">これらの変更は、退職処理中のどの時期に登録を終了するかを選択する機能を組織に提供します。</span><span class="sxs-lookup"><span data-stu-id="2c228-113">These changes provide organizations the ability to choose when to end enrollment during the termination process.</span></span> <span data-ttu-id="2c228-114">これらの新しいオプションは、作業者の退職およびマネージャー セルフ サービスの作業者の退職の特権の一部です。</span><span class="sxs-lookup"><span data-stu-id="2c228-114">These new options are part of the privileges for Terminate a worker and Terminate a worker from manager self service.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="2c228-115">その他の変更</span><span class="sxs-lookup"><span data-stu-id="2c228-115">Other changes</span></span>

<span data-ttu-id="2c228-116">このリリースには、いくつかの追加のバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2c228-116">This release includes several additional bug fixes.</span></span>

## <a name="known-issue"></a><span data-ttu-id="2c228-117">既知の問題</span><span class="sxs-lookup"><span data-stu-id="2c228-117">Known Issue</span></span>

-   <span data-ttu-id="2c228-118">**問題:** 作業者に新しい添付ファイルを追加する場合、**新規**および**編集**ボタンは灰色表示です。**回避策:** 添付ファイル ページを開く前に、**作業者**ページの情報ボックスが閉じていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2c228-118">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the fact boxes on the **Worker** page are closed.</span></span> <span data-ttu-id="2c228-119">**作業者**ページが読み込まれるとき情報ボックスが閉じている場合、添付ファイルボタンが有効になります。</span><span class="sxs-lookup"><span data-stu-id="2c228-119">If the fact boxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="2c228-120">(この問題は次のプラットフォーム更新プログラムで修正されます。)</span><span class="sxs-lookup"><span data-stu-id="2c228-120">(This issue will be fixed in the next platform update.)</span></span>
