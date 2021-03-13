---
title: 原価会計分析の Power BI コンテンツのセキュリティ設定
description: このトピックでは、Microsoft Power BI で行レベルのセキュリティに原価会計のアクセス レベルのセキュリティを反映する方法を説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d54ced21de112288c2f98c0bc895ca0d49c217e3
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093358"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="45083-103">原価会計分析の Power BI コンテンツのセキュリティ設定</span><span class="sxs-lookup"><span data-stu-id="45083-103">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45083-104">このトピックでは、Microsoft Power BI で行レベルのセキュリティに原価会計のアクセス レベルのセキュリティを反映する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="45083-104">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="45083-105">この機能により、ユーザーがアクセス権を持つ Power BI データのみが表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="45083-105">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

## <a name="overview"></a><span data-ttu-id="45083-106">概要</span><span class="sxs-lookup"><span data-stu-id="45083-106">Overview</span></span>

<span data-ttu-id="45083-107">**原価会計分析** Microsoft Power BI コンテンツは、Power BI 行レベルのセキュリティを使用してユーザーのアクセスを制限します。</span><span class="sxs-lookup"><span data-stu-id="45083-107">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="45083-108">セキュリティは、原価会計パラメーターで設定されたアクセス レベルの組織階層に基づきます。</span><span class="sxs-lookup"><span data-stu-id="45083-108">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="45083-109">**原価会計分析** Power BI コンテンツに関する詳細については、「[原価会計分析 Power BI コンテンツ](cost-accounting-analysis-content-pack.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="45083-109">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="45083-110">セットアップ</span><span class="sxs-lookup"><span data-stu-id="45083-110">Setup</span></span>
<span data-ttu-id="45083-111">Power BI にアクセス レベルのセキュリティを反映するには、Power BI コンテンツの所有者は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="45083-111">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="45083-112">**原価会計分析** Power BI コンテンツを公開するユーザーが自動的に所有者になります。</span><span class="sxs-lookup"><span data-stu-id="45083-112">The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="45083-113">所有者のみが Power BI のセキュリティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="45083-113">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="45083-114">また、所有者が PowerBI.com で他のユーザーを追加するまで、所有者以外は **原価会計分析** Power BI コンテンツ内のデータを参照することはできません。</span><span class="sxs-lookup"><span data-stu-id="45083-114">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1. <span data-ttu-id="45083-115">Power BI に定義ファイルを公開します。</span><span class="sxs-lookup"><span data-stu-id="45083-115">Publish the definition file to Power BI.</span></span>
2. <span data-ttu-id="45083-116">PowerBI.com にサインインします。</span><span class="sxs-lookup"><span data-stu-id="45083-116">Sign in to PowerBI.com.</span></span>
3. <span data-ttu-id="45083-117">**原価会計分析** Power BI コンテンツのデータセットを検索します。</span><span class="sxs-lookup"><span data-stu-id="45083-117">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4. <span data-ttu-id="45083-118">セキュリティ ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="45083-118">Open the security page.</span></span>

    ![セキュリティ ページを開く](./media/CA-picture-1.png)

5. <span data-ttu-id="45083-120">**原価オブジェクト コントローラー** ロールが既に作成されています。</span><span class="sxs-lookup"><span data-stu-id="45083-120">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="45083-121">原価会計のアクセス レベル組織階層の一部であるほかのメンバを追加します。</span><span class="sxs-lookup"><span data-stu-id="45083-121">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span>

    ![メンバーの追加](./media/CA-picture-2.png)

<span data-ttu-id="45083-123">**原価オブジェクト コントローラー** ロールに追加されているユーザーには、原価会計のアクセス レベル組織階層の定義に従って、許可されたデータのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="45083-123">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="45083-124">行レベル セキュリティは、Power BI から埋め込まれたタイルとレポートに適用されます。</span><span class="sxs-lookup"><span data-stu-id="45083-124">Row-level security applies to tiles and reports that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="45083-125">セキュリティの更新</span><span class="sxs-lookup"><span data-stu-id="45083-125">Updating security</span></span>
<span data-ttu-id="45083-126">原価会計のアクセス レベルのセキュリティに更新が行われ、それらの更新を Power BI に反映したい場合、**原価会計分析** Power BI コンテンツのエンティティ格納を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45083-126">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="45083-127">エンティティ格納の更新を完了後、PowerBI.com のコンポーネントを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45083-127">After you complete the entity store update you must update the artifacts on PowerBI.com.</span></span> <span data-ttu-id="45083-128">エンティティ格納の更新方法の詳細については、[エンティティ格納と Power BI の統合](power-bi-integration-entity-store.md#update-entity-store) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="45083-128">For more information about how to do an entity store update, see [Power BI integration with Entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="45083-129">**原価会計分析** Power BI コンテンツの所有者は、新しいユーザーに組織階層へのアクセスが許可された場合にもエンティティ格納の更新を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="45083-129">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="45083-130">また、所有者はその新たなユーザーを PowerBI.com の **原価オブジェクト コントローラー** ロールに追加して、行レベルのセキュリティが適用されるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="45083-130">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="45083-131">セキュリティの無効化</span><span class="sxs-lookup"><span data-stu-id="45083-131">Disabling security</span></span>
<span data-ttu-id="45083-132">ここでは、組織がデータ アクセスを制限すると想定します。</span><span class="sxs-lookup"><span data-stu-id="45083-132">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="45083-133">何らかの理由で、原価会計を実行する際にセキュリティ パラメーターが無効になっている場合は、所有者は代わりにユーザーを Power BI の **原価経理担当** ロールに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45083-133">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="45083-134">セキュリティを有効状態から無効状態に変更する場合は、**原価オブジェクト コントローラー** ロールからユーザーを削除することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="45083-134">If you change security from an enabled state to a disabled state, it's a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="45083-135">セキュリティを再び有効にする場合は、その逆を行ないます。</span><span class="sxs-lookup"><span data-stu-id="45083-135">And vice versa if you re-enable security.</span></span> <span data-ttu-id="45083-136">ユーザーは両方のロールに属することができます。</span><span class="sxs-lookup"><span data-stu-id="45083-136">Users can belong to both roles.</span></span> <span data-ttu-id="45083-137">結合アクセスとは両方のロールの結合のことです。</span><span class="sxs-lookup"><span data-stu-id="45083-137">Joint access is the union of both roles.</span></span> <span data-ttu-id="45083-138">**原価会計分析** Power BI コンテンツの場合、結合アクセスを持つユーザーには無制限のデータ アクセス権があります。</span><span class="sxs-lookup"><span data-stu-id="45083-138">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="45083-139">目標がアクセス権を制限することである場合は、ユーザーを **原価オブジェクト コントローラー** ロールのみに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="45083-139">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="45083-140">これらの行レベルのセキュリティの更新はすぐに反映されます。</span><span class="sxs-lookup"><span data-stu-id="45083-140">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="45083-141">影響を受けるユーザーは自分のブラウザを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45083-141">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="45083-142">追加リソース</span><span class="sxs-lookup"><span data-stu-id="45083-142">Additional resources</span></span>
<span data-ttu-id="45083-143">Power BI の行レベルのセキュリティの詳細については、「[Power BI のモデルでのセキュリティ管理](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="45083-143">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>
