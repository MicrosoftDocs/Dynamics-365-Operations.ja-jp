---
title: Dataverse の企業概念
description: このトピックでは、Finance and Operations と Dataverse 間の企業データの統合について説明します。
author: RamaKrishnamoorthy
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1c3af66c0b8daa120c6ba19bd910f7531ffada0e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751413"
---
# <a name="company-concept-in-dataverse"></a><span data-ttu-id="a202f-103">Dataverse の企業概念</span><span class="sxs-lookup"><span data-stu-id="a202f-103">Company concept in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="a202f-104">Finance and Operations では、*企業* の概念は、法的コンストラクトとビジネス コンストラクトの両方です。</span><span class="sxs-lookup"><span data-stu-id="a202f-104">In Finance and Operations, the concept of a *company* is both a legal construct and a business construct.</span></span> <span data-ttu-id="a202f-105">また、データのセキュリティと可視性の境界でもあります。</span><span class="sxs-lookup"><span data-stu-id="a202f-105">It's also a security and visibility boundary for data.</span></span> <span data-ttu-id="a202f-106">ユーザーは常に単一の会社のコンテキストで作業し、データのほとんどは会社によってストライプされます。</span><span class="sxs-lookup"><span data-stu-id="a202f-106">Users always work in the context of a single company, and most of the data is striped by company.</span></span>

<span data-ttu-id="a202f-107">Dataverse は、同等の概念を持っていません。</span><span class="sxs-lookup"><span data-stu-id="a202f-107">Dataverse doesn't have an equivalent concept.</span></span> <span data-ttu-id="a202f-108">最も近い概念は、主にユーザー データのセキュリティと可視性の境界である *事業単位* です。</span><span class="sxs-lookup"><span data-stu-id="a202f-108">The closest concept is *business unit*, which is primarily a security and visibility boundary for user data.</span></span> <span data-ttu-id="a202f-109">この概念は、企業概念と同じ法的またはビジネス上の意味を持ちません。</span><span class="sxs-lookup"><span data-stu-id="a202f-109">This concept doesn't have the same legal or business implications as the company concept.</span></span>

<span data-ttu-id="a202f-110">事業単位と企業は同等の概念ではないため、Dataverse 統合を目的として 1 対 1 (1:1) のマッピングを強制することはできません。</span><span class="sxs-lookup"><span data-stu-id="a202f-110">Because business unit and company aren't equivalent concepts, it isn't possible to force a one-to-one (1:1) mapping between them for the purpose of Dataverse integration.</span></span> <span data-ttu-id="a202f-111">ただし、ユーザーは既定でアプリケーションと Dataverse で同じ行を表示する必要があるため、Microsoft では cdm\_Company という Dataverse に新たなテーブルを導入しています。</span><span class="sxs-lookup"><span data-stu-id="a202f-111">However, because users must, by default, be able to see the same rows in the application and Dataverse, Microsoft has introduced a new table in Dataverse that is named cdm\_Company.</span></span> <span data-ttu-id="a202f-112">このテーブルは、アプリケーションの企業テーブルと同等です。</span><span class="sxs-lookup"><span data-stu-id="a202f-112">This table is equivalent to the Company table in the application.</span></span> <span data-ttu-id="a202f-113">行の可視性はアプリケーションと Dataverse 間で同等に、すぐに使用できることを保証するために、Dataverse のデータで次の設定をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a202f-113">To help guarantee that visibility of rows is equivalent between the application and Dataverse out of the box, we recommend the following setup for data in Dataverse:</span></span>

+ <span data-ttu-id="a202f-114">デュアル書き込みが有効になっている Finance and Operations の企業の行ごとに、関連付けられた cdm\_Company の行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="a202f-114">For each Finance and Operations Company row that is enabled for dual-write, an associated cdm\_Company row is created.</span></span>
+ <span data-ttu-id="a202f-115">cdm\_Company の行が作成され、デュアル書き込みが有効になると、同じ名前の既定の事業単位が作成されます。</span><span class="sxs-lookup"><span data-stu-id="a202f-115">When a cdm\_Company row is created and enabled for dual-write, a default business unit is created that has the same name.</span></span> <span data-ttu-id="a202f-116">既定のチームは、その事業単位に対して自動的に作成されますが、事業単位は使用されません。</span><span class="sxs-lookup"><span data-stu-id="a202f-116">Although a default team is automatically created for that business unit, the business unit isn't used.</span></span>
+ <span data-ttu-id="a202f-117">同じ名前を持つ別の所有者チームが、作成されます。</span><span class="sxs-lookup"><span data-stu-id="a202f-117">A separate owner team is created that has the same name.</span></span> <span data-ttu-id="a202f-118">また、事業単位にも関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="a202f-118">It's also associated with the business unit.</span></span>
+ <span data-ttu-id="a202f-119">既定では、作成されて、Dataverse にデュアル書き込みされた行の所有者は、関連付けられた事業部にリンクされている 「DW 所有者」 チームに設定されます。</span><span class="sxs-lookup"><span data-stu-id="a202f-119">By default, the owner of any row that is created and dual-written to Dataverse is set to the "DW Owner" team that is linked to the associated business unit.</span></span>

<span data-ttu-id="a202f-120">次の図では、Dataverse のデータ設定の例を示します。</span><span class="sxs-lookup"><span data-stu-id="a202f-120">The following illustration shows an example of this data setup in Dataverse.</span></span>

![Dataverse のデータ設定](media/dual-write-company-1.png)

<span data-ttu-id="a202f-122">この構成により、USMF 社に関連する行は、Dataverse の USMF 事業単位にリンクされているチームが所有します。</span><span class="sxs-lookup"><span data-stu-id="a202f-122">Because of this configuration, any row that is related to the USMF company will be owned by a team that is linked to the USMF business unit in Dataverse.</span></span> <span data-ttu-id="a202f-123">したがって、事業単位レベルの可視性に設定されたセキュリティ ロールを通じて、その事業単位にアクセスできるユーザーは、これらの行を表示できるようになります。</span><span class="sxs-lookup"><span data-stu-id="a202f-123">Therefore, any user who has access to that business unit through a security role that is set to business unit–level visibility can now see those rows.</span></span> <span data-ttu-id="a202f-124">次の例は、チームを使用してこれら行への正しいアクセスを提供する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a202f-124">The following example shows how teams can be used to provide the correct access to those rows.</span></span>

+ <span data-ttu-id="a202f-125">「営業マネージャー」のロールは、「USMF セールス」チームのメンバーに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="a202f-125">The "Sales Manager" role is assigned to members of the "USMF Sales" team.</span></span>
+ <span data-ttu-id="a202f-126">「営業マネージャー」のロールを持つユーザーは、自分が所属する同じ事業単位のメンバーである任意の取引先企業の行にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a202f-126">Users who have the "Sales Manager" role can access any account rows that are members of the same business unit that they are members of.</span></span>
+ <span data-ttu-id="a202f-127">「USMF セールス」チームは、前述の USMF 事業単位にリンクされています。</span><span class="sxs-lookup"><span data-stu-id="a202f-127">The "USMF Sales" team is linked to the USMF business unit that was mentioned earlier.</span></span>
+ <span data-ttu-id="a202f-128">したがって、「USMF セールス」チームのメンバーは、Finance and Operations の USMF 会社テーブルから来た「USMF DW」ユーザーが所有するアカウントを確認できます。</span><span class="sxs-lookup"><span data-stu-id="a202f-128">Therefore, members of the "USMF Sales" team can see any account that is owned by the "USMF DW" user, which would have come from the USMF Company table in Finance and Operations.</span></span>

![チームの使用方法](media/dual-write-company-2.png)

<span data-ttu-id="a202f-130">前の図に示すように、事業単位、企業、およびチーム間の 1:1 マッピングは、出発点に過ぎません。</span><span class="sxs-lookup"><span data-stu-id="a202f-130">As the preceding illustration shows, this 1:1 mapping between business unit, company, and team is just a starting point.</span></span> <span data-ttu-id="a202f-131">この例では、新しい「ヨーロッパ」の事業単位が DEMF と ESMF の両方の Dataverse にて手動で作成されます。</span><span class="sxs-lookup"><span data-stu-id="a202f-131">In this example, a new "Europe" business unit is manually created in Dataverse as the parent for both DEMF and ESMF.</span></span> <span data-ttu-id="a202f-132">この新しいルートの事業単位は、デュアル書き込みとは無関係です。</span><span class="sxs-lookup"><span data-stu-id="a202f-132">This new root business unit is unrelated to dual-write.</span></span> <span data-ttu-id="a202f-133">ただし、関連するセキュリティー ロールの **親 / 子 BU** にデータの可視性を設定することにより、DEMF および ESMF の両方のアカウント データに対する「EUR 営業」チームのメンバーにアクセスできるよう使用できます。</span><span class="sxs-lookup"><span data-stu-id="a202f-133">However, it can be used to give members of the "EUR Sales" team access to account data in both DEMF and ESMF by setting the data visibility to **Parent/Child BU** in the associated security role.</span></span>

<span data-ttu-id="a202f-134">最後に、デュアル書き込みによって、どの所有者チームに行の割り当てが決定されるかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a202f-134">A final topic to discuss is how dual-write determines which owner team it should assign rows to.</span></span> <span data-ttu-id="a202f-135">この動作は、cdm\_Company 行の **既定の所有チーム** 列で制御します。</span><span class="sxs-lookup"><span data-stu-id="a202f-135">This behavior is controlled by the **Default owning team** column on the cdm\_Company row.</span></span> <span data-ttu-id="a202f-136">cdm\_Company 行がデュアル書き込みに有効となっている場合、プラグインは関連付けられた事業単位と所有者チームを自動的に作成し (存在しない場合)、**既定の所有チーム** 列を設定します。</span><span class="sxs-lookup"><span data-stu-id="a202f-136">When a cdm\_Company row is enabled for dual-write, a plug-in automatically creates the associated business unit and owner team (if it doesn't already exist), and sets the **Default owning team** column.</span></span> <span data-ttu-id="a202f-137">管理者は、この列を別の値に変更できます。</span><span class="sxs-lookup"><span data-stu-id="a202f-137">The admin can change this column to a different value.</span></span> <span data-ttu-id="a202f-138">ただし、テーブルがデュアル書き込みを有効にしている限り、管理者は列をクリアできません。</span><span class="sxs-lookup"><span data-stu-id="a202f-138">However, the admin can't clear the column as long as the table is enabled for dual-write.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="a202f-139">![既定の所有チーム列](media/dual-write-default-owning-team.jpg)</span><span class="sxs-lookup"><span data-stu-id="a202f-139">![Default owning team column](media/dual-write-default-owning-team.jpg)</span></span>

## <a name="company-striping-and-bootstrapping"></a><span data-ttu-id="a202f-140">企業のストライピングとブートストラップ</span><span class="sxs-lookup"><span data-stu-id="a202f-140">Company striping and bootstrapping</span></span>

<span data-ttu-id="a202f-141">Dataverse 統合は、企業の識別子を使用してデータをストライプすることにより、企業パリティをもたらします。</span><span class="sxs-lookup"><span data-stu-id="a202f-141">Dataverse integration brings company parity by using a company identifier to stripe data.</span></span> <span data-ttu-id="a202f-142">次の図に示すように、すべての企業の固有のテーブルは、cdm\_Company テーブルと多対1 (N:1) の関係を持つよう拡張されます。</span><span class="sxs-lookup"><span data-stu-id="a202f-142">As the following illustration shows, all company-specific tables are extended so that they have a many-to-one (N:1) relationship with the cdm\_Company table.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="a202f-143">![企業の固有テーブルと cdm_Company テーブル間の N:1 関係](media/dual-write-bootstrapping.png)</span><span class="sxs-lookup"><span data-stu-id="a202f-143">![N:1 relationship between a company-specific table and the cdm_Company table](media/dual-write-bootstrapping.png)</span></span>

+ <span data-ttu-id="a202f-144">行の場合、企業が追加、保存された後で、値が読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="a202f-144">For rows, after a company is added and saved, the value becomes read-only.</span></span> <span data-ttu-id="a202f-145">したがって、ユーザーは正しい企業を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a202f-145">Therefore, users should make sure that they select the correct company.</span></span>
+ <span data-ttu-id="a202f-146">企業データを持つ行のみが、アプリケーションと Dataverse 間のデュアル書き込みの対象となります。</span><span class="sxs-lookup"><span data-stu-id="a202f-146">Only rows that have company data are eligible for dual-write between the application and Dataverse.</span></span>
+ <span data-ttu-id="a202f-147">既存の Dataverse データによって、管理者主導のブートストラップ エクスペリエンスがまもなく利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="a202f-147">For existing Dataverse data, an admin-led bootstrapping experience will soon be available.</span></span>


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a><span data-ttu-id="a202f-148">Customer Engagement アプリに会社名を自動入力する</span><span class="sxs-lookup"><span data-stu-id="a202f-148">Autopopulate company name in customer engagement apps</span></span>

<span data-ttu-id="a202f-149">Customer Engagement アプリで会社名を自動入力するには、いくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="a202f-149">There are several ways to auto-populate the company name in customer engagement apps.</span></span>

+ <span data-ttu-id="a202f-150">システム管理者は、**詳細設定 > システム > セキュリティ > ユーザー** に移動することによって、既定の会社を設定できます。</span><span class="sxs-lookup"><span data-stu-id="a202f-150">If you are a system administrator, you can set the default company by navigating to **Advanced Settings > System > Security > Users**.</span></span> <span data-ttu-id="a202f-151">**ユーザー** フォームを開き、**組織情報** セクションで **会社をフォーム上の既定** 値に設定します。</span><span class="sxs-lookup"><span data-stu-id="a202f-151">Open the **User** form, and in the **Organization Information** section, set the **Company to default on Forms** value.</span></span>

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="組織情報セクションで既定の会社を設定します。":::

+ <span data-ttu-id="a202f-153">**事業単位** レベルの **SystemUser** テーブルに対する **書き込み** アクセス権がある場合は、**会社** ドロップダウン メニューから会社を選択することにより、任意のフォームで既定の会社を変更できます。</span><span class="sxs-lookup"><span data-stu-id="a202f-153">If you have **Write** access to the **SystemUser** table for the **Business Unit** level, then you can change the default company on any form by selecting a company from the **Company** drop-down menu.</span></span>

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="新しいアカウントで会社名を変更します。":::

+ <span data-ttu-id="a202f-155">複数の会社のデータへの **書き込み** アクセス権がある場合は、別の会社に属する行を選択して既定の会社を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="a202f-155">If you have **Write** access to data in more than one company, then you can change the default company by choosing a row that belongs to different company.</span></span>

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="行を選択すると、既定の会社が変更されます。":::

+ <span data-ttu-id="a202f-157">システム コンフィギュレーターまたは管理者で、会社データをカスタム フォームに自動入力する場合、[フォーム イベント](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a202f-157">If you are a system configurator or administrator, and you want to auto-populate company data on a custom form, then you can use [form events](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span></span> <span data-ttu-id="a202f-158">JavaScript リファレンスを **msdyn_/DefaultCompany.js** に追加し、次のイベントを使用します。</span><span class="sxs-lookup"><span data-stu-id="a202f-158">Add a JavaScript reference to **msdyn_/DefaultCompany.js** and use the following events.</span></span> <span data-ttu-id="a202f-159">**アカウント** フォームなど、すぐに利用できるフォームを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="a202f-159">You can use any out-of-the-box form, for example, the **Account** form.</span></span>

    + <span data-ttu-id="a202f-160">フォームの **OnLoad** イベント: **defaultCompany** 列を設定します。</span><span class="sxs-lookup"><span data-stu-id="a202f-160">**OnLoad** event for the form: Set the **defaultCompany** column.</span></span>
    + <span data-ttu-id="a202f-161">**会社** 列の **OnChange** イベント: **updateDefaultCompany** 列を設定します。</span><span class="sxs-lookup"><span data-stu-id="a202f-161">**OnChange** event for the **Company** column: Set the **updateDefaultCompany** column.</span></span>

## <a name="apply-filtering-based-on-the-company-context"></a><span data-ttu-id="a202f-162">会社コンテキストに基づくフィルター処理の適用</span><span class="sxs-lookup"><span data-stu-id="a202f-162">Apply filtering based on the company context</span></span>

<span data-ttu-id="a202f-163">カスタム フォーム、または標準フォームに追加されたカスタム ルックアップ列の会社コンテキストに基づいてフィルター処理を適用するには、フォームを開き、**関連レコードのフィルター処理** セクションを使用して、会社フィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="a202f-163">To apply filtering based on the company context on your custom forms or on custom lookup columns added to the standard forms, open the form and use the **Related Records Filtering** section to apply the company filter.</span></span> <span data-ttu-id="a202f-164">この設定は、指定された行の基礎となる会社に基づくフィルター処理が必要となる各ルックアップ列に対して行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a202f-164">You must set this for each lookup column that requires filtering based on the underlying company on a given row.</span></span> <span data-ttu-id="a202f-165">次の図に **アカウント** の設定を示します。</span><span class="sxs-lookup"><span data-stu-id="a202f-165">The setting is shown for **Account** in the following illustration.</span></span>

:::image type="content" source="media/apply-company-context.png" alt-text="会社コンテキストの適用":::



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]