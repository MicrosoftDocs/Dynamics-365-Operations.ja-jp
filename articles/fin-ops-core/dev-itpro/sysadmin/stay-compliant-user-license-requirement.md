---
title: ユーザー ライセンス要件への準拠の維持
description: このトピックでは、Finance and Operations アプリのユーザー ライセンス要件を遵守する方法に関する情報を提供します。
author: peakerbl
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: chaubold
ms.search.validFrom: 2018-05-30
ms.dyn365.ops.version: AX 7.0
ms.openlocfilehash: 81fb88cf2225d9ec74f16b6726b96de16847518e
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907927"
---
# <a name="stay-compliant-with-user-licensing-requirements"></a><span data-ttu-id="4981e-103">ユーザー ライセンス要件への準拠の維持</span><span class="sxs-lookup"><span data-stu-id="4981e-103">Stay compliant with user licensing requirements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4981e-104">このトピックでは、顧客が Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Commerce などの Finance and Operations アプリに対するユーザー ライセンス要件を遵守する方法に関する概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="4981e-104">This topic provides an overview of how customers can stay compliant with the user licensing requirements for Finance and Operations apps, such as Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4981e-105">ユーザーのライセンス要件は、それらのユーザーに割り当てられているセキュリティ ロールによって決まります。</span><span class="sxs-lookup"><span data-stu-id="4981e-105">The licensing requirements for users are determined by the security roles that are assigned to those users.</span></span> <span data-ttu-id="4981e-106">セキュリティ ロールは、次の階層に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="4981e-106">Security roles are built based on a hierarchy of:</span></span>

- <span data-ttu-id="4981e-107">サブ ロール</span><span class="sxs-lookup"><span data-stu-id="4981e-107">Sub-roles</span></span>
- <span data-ttu-id="4981e-108">職務</span><span class="sxs-lookup"><span data-stu-id="4981e-108">Duties</span></span>
- <span data-ttu-id="4981e-109">権限</span><span class="sxs-lookup"><span data-stu-id="4981e-109">Privileges</span></span>
- <span data-ttu-id="4981e-110">直接参照された、セキュリティ保護可能なオブジェクト</span><span class="sxs-lookup"><span data-stu-id="4981e-110">Directly referenced securable objects</span></span> 

<span data-ttu-id="4981e-111">詳細については、[ロールベース セキュリティ](./role-based-security.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4981e-111">For more information, see [Role-based security](./role-based-security.md).</span></span>

<span data-ttu-id="4981e-112">ユーザーのライセンス要件は、組織またはテナント レベルで決定されます。</span><span class="sxs-lookup"><span data-stu-id="4981e-112">The licensing requirements for users are determined at the organization or tenant level.</span></span> <span data-ttu-id="4981e-113">このトピックでは、単一の環境の要件に重点を置いて説明します。</span><span class="sxs-lookup"><span data-stu-id="4981e-113">This topic is focused on the requirements for a single environment.</span></span> <span data-ttu-id="4981e-114">複数の環境がある場合は、すべての要件に対して要件を分析する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4981e-114">If you have multiple environments, the requirements must be analyzed across all of them.</span></span>

<span data-ttu-id="4981e-115">ライセンス要件は、セキュリティで保護されたすべてのオブジェクトに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="4981e-115">A licensing requirement is assigned to every securable object.</span></span> <span data-ttu-id="4981e-116">ライセンス要件の例としては、**なし**、**チームメンバー**、**アクティビティ**、**操作** があります。</span><span class="sxs-lookup"><span data-stu-id="4981e-116">Examples of licensing requirements include **None**, **Team members**, **Activity**, and **Operations**.</span></span> <span data-ttu-id="4981e-117">**操作** ライセンス要件は、ユーザーのフル ライセンスが必要であることを示しています。</span><span class="sxs-lookup"><span data-stu-id="4981e-117">The **Operations** licensing requirement indicates that a full user license is required.</span></span> <span data-ttu-id="4981e-118">一部の特権は、特定のユーザーのフル ライセンスに固有であり、ユーザーのフル ライセンスをそのユーザーに割り当てるのに *ベース* または *Attach* ライセンスが必要です。</span><span class="sxs-lookup"><span data-stu-id="4981e-118">Some privileges are unique to a specific full user license and require a *base* or *attach* license for the full user license be assigned to the user.</span></span> <span data-ttu-id="4981e-119">詳細については、このトピックの後半の [ユーザー ライセンスの見積もりレポート](#user-license-estimator-report) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4981e-119">For more information, see the [User license estimator report](#user-license-estimator-report) section later in this topic.</span></span>

<span data-ttu-id="4981e-120">このトピックの残りの部分では、実際のライセンスが予定されたライセンス要件を満たしていることを確認するために使用できる、さまざまなツールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4981e-120">The rest of this topic describes the various tools that you can use to ensure that the actual licensing complies with the expected licensing requirements.</span></span>

## <a name="roles-for-selected-user-factbox-on-the-users-page"></a><span data-ttu-id="4981e-121">ユーザー ページで選択したユーザー情報ボックスのロール</span><span class="sxs-lookup"><span data-stu-id="4981e-121">Roles for selected user FactBox on the Users page</span></span>

<span data-ttu-id="4981e-122">**ユーザー** ページ (**システム管理者 \>ユーザー**) で、ユーザーに役割を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="4981e-122">You assign roles to users on the **Users** page (**System administration \> Users**).</span></span> <span data-ttu-id="4981e-123">**選択したユーザーのロール** 情報ボックスで各ロールのライセンス要件を表示できます。</span><span class="sxs-lookup"><span data-stu-id="4981e-123">You can view license requirements for each role in the **Roles for selected user** FactBox.</span></span>

![ユーザー ページで選択したユーザー情報ボックスのロール](media/UsersRoles.png)

<span data-ttu-id="4981e-125">ライセンスの最大要件によって、ユーザーの実際のライセンス要件が決まります。</span><span class="sxs-lookup"><span data-stu-id="4981e-125">The maximum license requirement determines the actual licensing requirement for a user.</span></span> <span data-ttu-id="4981e-126">ライセンス要件が **操作** として識別された場合は、[ユーザー ライセンスの見積もり](#user-license-estimator-report) レポートを使用して、ユーザーのフル ライセンス要件を決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4981e-126">If any license requirement is identified as **Operations**, you must use the [User license estimator](#user-license-estimator-report) report to determine the full user licensing requirements.</span></span>

> [!NOTE]
> <span data-ttu-id="4981e-127">バージョン 10.0.15 のプラットフォーム更新を開始して、必要なライセン スタイプが、Commerce、Finance、および Supply Chain Management などのアプリケーション固有のライセンス タイプが含まれるように拡張されています。</span><span class="sxs-lookup"><span data-stu-id="4981e-127">Starting with platform update for version 10.0.15, the required license types are extended to include application specific license types such as Commerce, Finance, and Supply Chain Management.</span></span> <span data-ttu-id="4981e-128">この拡張機能を使用すると、ロールをユーザーに割り当てるとき、および選択したユーザーの情報ボックスに対してロールを使用するときに、実際のライセンス要件を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="4981e-128">This extension makes it possible to view the actual license requirements when you assign roles to users and when using the Roles for the selected user FactBox.</span></span> <span data-ttu-id="4981e-129">必要なライセン スタイプに対して複数の値を表示できます。</span><span class="sxs-lookup"><span data-stu-id="4981e-129">More than one value can be displayed for the required license type.</span></span> 

## <a name="view-permissions-page"></a><span data-ttu-id="4981e-130">アクセス許可の表示ページ</span><span class="sxs-lookup"><span data-stu-id="4981e-130">View permissions page</span></span>

<span data-ttu-id="4981e-131">**セキュリティの構成** ページ (**システム管理者 \>セキュリティ \> セキュリティの構成**) でのセキュリティ構成中に、セキュリティ オブジェクト、役割、職務、またはアクセス許可を選択し、**アクセス許可の表示** を選択することにより、現在含まれているすべてのアクセス許可、およびライセンス要件を表示できます。</span><span class="sxs-lookup"><span data-stu-id="4981e-131">During security configuration on the **Configure security** page (**System administration \> Security \> Configure security**), you can select any security object, a role, duty, or permissions, and then select **View permissions** to view all permissions that are currently included and their licensing requirements.</span></span> <span data-ttu-id="4981e-132">**アクセス許可の表示** ページのヘッダーに、必要なライセンス レベルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4981e-132">The header of the **View permissions** page shows the required license level.</span></span>

![アクセス許可の表示ページ](media/ViewPermissons.png)

> [!NOTE]
> <span data-ttu-id="4981e-134">バージョン 10.0.15 のプラットフォーム更新を開始して、必要なライセン スタイプが、Commerce、Finance、および Supply Chain Management などのアプリケーション固有のライセンス タイプが含まれるように拡張されています。</span><span class="sxs-lookup"><span data-stu-id="4981e-134">Starting with platform update for version 10.0.15, the required license types are extended to include application specific license types such as Commerce, Finance, and Supply Chain Management.</span></span> <span data-ttu-id="4981e-135">この拡張機能を使用すると、実際のライセンス要件を決定する特定のセキュリティ オブジェクトを識別しながら、セキュリティを構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="4981e-135">This extension makes it possible to identify the specific security objects that determine the actual license requirements while also configuring security.</span></span> <span data-ttu-id="4981e-136">必要なライセン スタイプに対して複数の値を表示できます。</span><span class="sxs-lookup"><span data-stu-id="4981e-136">More than one value can be displayed for the required license type.</span></span> 

## <a name="user-license-counts-report"></a><span data-ttu-id="4981e-137">ユーザー ライセンス数レポート</span><span class="sxs-lookup"><span data-stu-id="4981e-137">User license counts report</span></span>

<span data-ttu-id="4981e-138">**ユーザー ライセンス カウント** レポート (**システム管理 \> 照会 \> ライセンス**) を使用して、ライセンス タイプごとに必要なライセンスの数 (**チームメンバ**、**アクティビティ**、**操作** など) を取得します。</span><span class="sxs-lookup"><span data-stu-id="4981e-138">The **User license counts** report (**System administration \> Inquiries \> License**) is used to get a count of required licenses per license type (for example, **Team members**, **Activity**, and **Operations**).</span></span>

![ユーザー ライセンス数レポート](media/UserLicenseCountsReport.png)

<span data-ttu-id="4981e-140">また、各ユーザーの詳細と、割り当てられた役割ごとのライセンス要件についても説明します。</span><span class="sxs-lookup"><span data-stu-id="4981e-140">The report also provides details about each user and the licensing requirements for each assigned role.</span></span> <span data-ttu-id="4981e-141">ユーザーは最も高いライセンスの種類の元一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="4981e-141">Users are listed under the highest license type.</span></span> <span data-ttu-id="4981e-142">ライセンス要件が **操作** として識別された場合は、[ユーザー ライセンスの見積もり](#user-license-estimator-report) レポートを使用して、特定のユーザーのフル ライセンス要件を決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4981e-142">If the license requirement is identified as **Operations**, you must use the [User license estimator](#user-license-estimator-report) report to determine the specific full user licensing requirements.</span></span>

<span data-ttu-id="4981e-143">**ユーザー数履歴** レポートには、日ごとの合計数が表示されますが、詳細は含まれません。</span><span class="sxs-lookup"><span data-stu-id="4981e-143">The **User counts history** report shows total counts per date, but without any details.</span></span>

> [!NOTE]
> <span data-ttu-id="4981e-144">このレポートは、**指定されたユーザー ライセンス数のレポート処理** バッチ ジョブに依存します。</span><span class="sxs-lookup"><span data-stu-id="4981e-144">This report depends on the **Named user license count reports processing** batch job.</span></span> <span data-ttu-id="4981e-145">バッチが前回実行された時を確認するには、**バッチ ジョブの履歴** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="4981e-145">To determine when the batch was last run, use the **Batch job history** page.</span></span>

## <a name="user-license-estimator-report"></a><span data-ttu-id="4981e-146">ユーザー ライセンス見積もりレポート</span><span class="sxs-lookup"><span data-stu-id="4981e-146">User license estimator report</span></span>

<span data-ttu-id="4981e-147">前述のツールによって、ユーザーが **操作** タイプのライセンスを必要としていることが確認された場合は、**ユーザーライセンスの見積もり** レポート (**システム管理 \>照会 \>ライセンス レポート**) を使用して、それらのユーザーの特定のライセンス要件の数を取得できます。</span><span class="sxs-lookup"><span data-stu-id="4981e-147">If the previously mentioned tools have identified that any users require a license of the **Operations** type, you can use the **User license estimator** report (**System administration \> Inquiries \> License reports**) to get a count of specific licensing requirements for those users.</span></span> <span data-ttu-id="4981e-148">このレポートには、これらのユーザーのみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4981e-148">The report includes only those users.</span></span>

<span data-ttu-id="4981e-149">特定のユーザーのフル ライセンスを必要とする特権がユーザーに割り当てられていない場合は、そのユーザーが表示されますが、特定の完全なユーザー ライセンスはマークされません。</span><span class="sxs-lookup"><span data-stu-id="4981e-149">If no privileges that require a specific full user license have been assigned to a user, that user is shown, but no specific full user licenses are marked.</span></span> <span data-ttu-id="4981e-150">このユーザーは、割り当てられているすべてのユーザー ライセンスに準拠します。</span><span class="sxs-lookup"><span data-stu-id="4981e-150">That user will be compliant with any full user license that is assigned.</span></span> <span data-ttu-id="4981e-151">次の図の例では、**データベース管理管理者** ロールがユーザーに割り当てられており、その **操作** タイプのライセンスを必要とする他のロールが割り当てられていません 。</span><span class="sxs-lookup"><span data-stu-id="4981e-151">In the example in the following illustration, the **Database management administrator** role is assigned to a user, and no other roles that require a license of the **Operations** type are assigned.</span></span>

![ユーザー ライセンス見積もりレポート](media/LicenseGuide.png)

<span data-ttu-id="4981e-153">このユーザーは、ライセンス ガイドに基づいて、すべてのユーザー ライセンスに準拠しています。</span><span class="sxs-lookup"><span data-stu-id="4981e-153">Based on the licensing guide, this user is compliant with any full user license.</span></span>

<span data-ttu-id="4981e-154">管理者権限は、Finance、Supply Chain Management、Commerce の各アプリに適用されます。</span><span class="sxs-lookup"><span data-stu-id="4981e-154">Admin rights apply across the Finance, Supply Chain Management, and Commerce apps.</span></span> <span data-ttu-id="4981e-155">たとえば、Finance ライセンスがある場合は、Finance、Supply Chain Management、Commerce の管理者権限を持ちます。</span><span class="sxs-lookup"><span data-stu-id="4981e-155">For example, if you have a Finance license, you have the admin rights for Finance, Supply Chain Management, and Commerce.</span></span>

<span data-ttu-id="4981e-156">この原則は、含まれる特権に基づいて、Microsoft やカスタマイズによって提供されるいくつかのロールに適用される場合があります。</span><span class="sxs-lookup"><span data-stu-id="4981e-156">This principle might apply to several roles that are provided by Microsoft and customizations, based on the included privileges.</span></span> <span data-ttu-id="4981e-157">これらのユーザーに対して特定のライセンスが示されていない場合、**ユーザー ライセンスの見積もり** レポート上で示されます。</span><span class="sxs-lookup"><span data-stu-id="4981e-157">No specific license is indicated for these users on the **User license estimator** report.</span></span>

![ユーザーのフル ライセンスが必要なユーザー](media/UserLicenseEstimatorClaire.png)

<span data-ttu-id="4981e-159">または、特定のユーザーのフル ライセンスが必要な特権がユーザーに割り当てられている場合は、そのユーザーに割り当てられているライセンスを参照するときに、そのライセンスが示されます。</span><span class="sxs-lookup"><span data-stu-id="4981e-159">Alternatively, if privileges that require a specific full user license have been assigned to a user, that license is indicated when you look at the licenses that are assigned to the user.</span></span> <span data-ttu-id="4981e-160">次の図の例では、ユーザーがSupply Chain Management の *ベース* ライセンスを持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4981e-160">In the example in the following illustration, the user must have a *base* license for Supply Chain Management.</span></span>

![特定のユーザー フル ライセンスが必要なユーザー](media/UserLicenseEstimatorAlica.png)

<span data-ttu-id="4981e-162">ユーザーに 1 つ以上のユーザー フル ライセンスを要する特権が割り当てられている場合、そのユーザーに割り当てられているライセンスを参照するときに、それらのライセンスが示されます。</span><span class="sxs-lookup"><span data-stu-id="4981e-162">If privileges that require more than one specific full user license have been assigned to a user, those licenses are indicated when you look at the licenses that are assigned to the user.</span></span> <span data-ttu-id="4981e-163">この場合、ユーザーは、そのライセンスの 1 つの *ベース* ライセンスと、その他のユーザーのフル ライセンスに必要な *Attach* ライセンスを持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4981e-163">In this case, the user must have a *base* license for one of the licenses and an *attach* license for all other full user licenses that are required.</span></span> <span data-ttu-id="4981e-164">次の図の例では、ユーザーは、Finance の *ベース* ライセンスと Supply Chain Management の *Attach* ライセンス、または Supply Chain Management の *ベース* ライセンスと Finance の *Attach* ライセンスのいずれかを所有している必要があります。</span><span class="sxs-lookup"><span data-stu-id="4981e-164">In the example in the following illustration, the user must have either a *base* license for Finance and an *attach* license for Supply Chain Management, or a *base* license for Supply Chain Management and an *attach* license for Finance.</span></span>

![1 つ以上の特定のユーザー フル ライセンスが必要なユーザー](media/UserLicenseEstimatorCassie.png)

<span data-ttu-id="4981e-166">特定のユーザー フル ライセンス数あたりの合計は、*ベース* ライセンスと *Attach* のライセンスに分割されていません。</span><span class="sxs-lookup"><span data-stu-id="4981e-166">The totals per specific full user license counts aren't divided into *base* licenses and *attach* licenses.</span></span>

> [!NOTE]
> <span data-ttu-id="4981e-167">バージョン 10.0.13 のプラットフォーム更新プログラムのリリース以降に、特定のユーザー フル ライセンスとカスタム特権の評価の合計数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4981e-167">The total count per specific full user license and evaluation of custom privileges are included starting in the release of the platform update for version 10.0.13.</span></span> <span data-ttu-id="4981e-168">このレポートでは、*ベース* ライセンス要件と *Attach* ライセンス要件を区別することはできません。</span><span class="sxs-lookup"><span data-stu-id="4981e-168">The report can't separate the *base* and *attach* license requirements.</span></span> <span data-ttu-id="4981e-169">したがって、ユーザーのフル ライセンス要件の合計のみが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="4981e-169">Therefore, it lists only the total full user licenses requirements.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4981e-170">追加リソース</span><span class="sxs-lookup"><span data-stu-id="4981e-170">Additional resources</span></span>

<span data-ttu-id="4981e-171">Finance and Operations アプリの購入方法とライセンスの詳細については、[Microsoft Dynamics 365 ライセンス ガイド](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4981e-171">For information about how to buy and license Finance and Operations apps, see [Microsoft Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).</span></span>

<span data-ttu-id="4981e-172">Microsoft 365 管理センターでユーザーにライセンスを割り当てる方法については、[ユーザーへのライセンスの割り当て](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4981e-172">For information about how to assign licenses to users in the Microsoft 365 admin center, see [Assign licenses to users](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide).</span></span>

<span data-ttu-id="4981e-173">同じテナントに複数の実装プロジェクトが存在する場合は、追加のユーザー ライセンスが必要です。</span><span class="sxs-lookup"><span data-stu-id="4981e-173">Additional user licenses are required when multiple implementation projects exist for the same tenant.</span></span> <span data-ttu-id="4981e-174">詳細については、[1 つの Azure AD テナントでの複数の LCS プロジェクトと運用環境](../../fin-ops/get-started/implement-multiple-projects-aad-tenant.md#licensing-requirements) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4981e-174">For more information, see [Multiple LCS projects and production environments on one Azure AD tenant](../../fin-ops/get-started/implement-multiple-projects-aad-tenant.md#licensing-requirements).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]