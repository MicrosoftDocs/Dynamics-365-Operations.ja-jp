---
title: "仕入先コラボレーション ユーザーの管理"
description: "このトピックでは、新しい仕入先コラボレーション ユーザーのプロビジョニングの要求方法、および新しい仕入先コラボレーションの連絡先を追加する方法について説明します。"
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 0c4f8cf32e93f4330bc73f8e0bd350545482c19d
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---

# <a name="manage-vendor-collaboration-users"></a><span data-ttu-id="ecbc0-103">仕入先コラボレーション ユーザーの管理</span><span class="sxs-lookup"><span data-stu-id="ecbc0-103">Manage vendor collaboration users</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ecbc0-104">このトピックでは、新しい仕入先コラボレーション ユーザーのプロビジョニングの要求方法、および新しい仕入先コラボレーションの連絡先を追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-104">This topic describes how you can request the provisioning of new vendor collaboration users, and how to add new vendor collaboration contacts.</span></span> 

<span data-ttu-id="ecbc0-105">Microsoft Dynamics 365 for Finance and Operations の仕入先コラボレーション インタフェースは、発注書、請求書、委託販売在庫関する情報を外部仕入先に公開します。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-105">The vendor collaboration interface in Microsoft Dynamics 365 for Finance and Operations exposes information about purchase orders, invoices, and consignment stock to external vendors.</span></span> <span data-ttu-id="ecbc0-106">**仕入先管理者 (外部)** セキュリティ ロールまたは同様の権限を持つ外部仕入先として作業する場合は、新しい仕入先コラボレーションの連絡先を作成して、新しいユーザーがプロビジョニングされるように要求できます。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-106">You can create new vendor collaboration contacts and request that new users are provisioned if you're working as an external vendor with the **Vendor admin (external)** security role, or similar permissions.</span></span> <span data-ttu-id="ecbc0-107">調達担当者として作業する場合、これらのタスクを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-107">You can also perform these tasks if you're working as a procurement professional.</span></span> <span data-ttu-id="ecbc0-108">このトピックでは、このロールは Finance and Operations のインスタンスを所有する会社内で作業している調達担当者を指します。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-108">In this topic, this role refers to a procurement professional who is working within the company that owns the instance of Finance and Operations.</span></span> <span data-ttu-id="ecbc0-109">外部仕入先である場合の、仕入先コラボレーションの使用方法の詳細については、「[顧客に対する仕入先](vendor-collaboration-work-customers-dynamics-365-operations.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-109">For more information about how to use vendor collaboration if you're an external vendor, see [Vendor with customers](vendor-collaboration-work-customers-dynamics-365-operations.md).</span></span>  

<span data-ttu-id="ecbc0-110">調達担当者である場合は、仕入先コラボレーションの使用方法の詳細について、「[外部仕入先との仕入先コラボレーション](vendor-collaboration-work-external-vendors.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-110">For more information about how to use vendor collaboration if you're a procurement professional, see [Vendor collaboration to with external vendors](vendor-collaboration-work-external-vendors.md).</span></span>

## <a name="add-new-vendor-collaboration-contacts"></a><span data-ttu-id="ecbc0-111">新しい仕入先コラボレーションの連絡先の追加</span><span class="sxs-lookup"><span data-stu-id="ecbc0-111">Add new vendor collaboration contacts</span></span>
<span data-ttu-id="ecbc0-112"> 仕入先コラボレーションにアクセスしようとする場合、仕入先コラボレーションの連絡先として最初に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-112">If you want someone to have access to vendor collaboration they first have to be added as a vendor collaboration contact.</span></span> <span data-ttu-id="ecbc0-113">仕入先コラボレーションを使用しない会社の従業員の連絡先を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-113">You may also want to add contacts for employees in your company who won't use vendor collaboration.</span></span> <span data-ttu-id="ecbc0-114">たとえば、他のタイプの調達情報の連絡先時点であることが可能です。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-114">For example, they could be the point of contact for other kinds of procurement information.</span></span> <span data-ttu-id="ecbc0-115">新しい連絡先は、[**仕入先コラボレーション**] &gt; [**連絡先**] メニューからアクセスできる [**すべての連絡先**] ページに追加されます。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-115">New contacts are added on the **All contacts** page, which is accessed from the **Vendor collaboration** &gt; **Contacts** menu.</span></span> <span data-ttu-id="ecbc0-116">新しい連絡先の追加: </span><span class="sxs-lookup"><span data-stu-id="ecbc0-116">To add a new contact:</span></span>

1.  <span data-ttu-id="ecbc0-117">[**新規**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-117">Click **New.**</span></span>
2.  <span data-ttu-id="ecbc0-118">連絡担当者の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-118">Enter the contact person details.</span></span>
3.  <span data-ttu-id="ecbc0-119">会社でどの法人を代表しているのか、連携する会社で作業するどの法人かを選択します。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-119">Choose which legal entity they're representing in your company, and which legal entity they'll work with in the company that they'll collaborate with.</span></span> <span data-ttu-id="ecbc0-120">この操作は、[**自社の法人**/**顧客会社の法人**] ペアを選択することによって行います。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-120">You do this by selecting a **Legal entity in my company**/**Legal entity in customer company** pair.</span></span>
4.  <span data-ttu-id="ecbc0-121">[**作成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-121">Click **Create.**</span></span>

<span data-ttu-id="ecbc0-122">連絡先を削除するには、作成したものだけを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-122">If you want to delete a contact, it's only possible to delete the ones that you've created.</span></span>

## <a name="vendor-collaboration-user-requests"></a><span data-ttu-id="ecbc0-123">仕入先コラボレーションのユーザー要求</span><span class="sxs-lookup"><span data-stu-id="ecbc0-123">Vendor collaboration user requests</span></span>
<span data-ttu-id="ecbc0-124">仕入先コラボレーションのユーザーの要求は、調達担当者、または外部仕入先によって上げることができます。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-124">Vendor collaboration user requests can be raised by a procurement professional, or by an external vendor administrator.</span></span>

-   <span data-ttu-id="ecbc0-125">外部仕入先の場合は、[**仕入先コラボレーション**] モジュール内の [**すべての連絡先**] ページから要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-125">If you're an external vendor, you submit requests from the **All contacts** page within the **Vendor collaboration** module.</span></span>
-   <span data-ttu-id="ecbc0-126">調達担当者である場合、[**連絡先の表示**] ページから要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-126">If you're a procurement professional, you submit requests from the **View contacts** page.</span></span> <span data-ttu-id="ecbc0-127">これを行うには、仕入先レコードの、アクション ペインの [**設定**] セクションで、[**連絡先**] &gt; [**連絡先の表示**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-127">To do this, on the vendor record, in the **Setup** section in the Action pane, select **Contacts** &gt; **View contacts**.</span></span>

<span data-ttu-id="ecbc0-128">ユーザーのプロビジョニング、ユーザーの無効化、またはセキュリティ ロールの変更を要求をできます。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-128">You can make a request to provision a user, to inactivate a user, or to modify security roles.</span></span> <span data-ttu-id="ecbc0-129">外部仕入先の管理者の場合は、ユーザーが要求する仕入先アカウントの連絡担当者として登録する必要があり、仕入先アカウントの仕入先コラボレーション インターフェイスにアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-129">If you're an external vendor administrator, you must be registered as a contact person for the vendor accounts that you want to make user requests for, and you must have access to the vendor collaboration interface for those vendor accounts.</span></span>  

<span data-ttu-id="ecbc0-130">リクエストが送信されると、[**仕入先コラボレーション**] モジュールの**仕入先コラボレーション ユーザー要求**リストと [**調達**] モジュール (外部ユーザーは調達モジュールにアクセスできません) の**仕入先コラボレーションのユーザー要求**リストが追加されます。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-130">When a request is submitted it is added to the **Vendor collaboration user requests** list in the **Vendor collaboration** module, and to the **Vendor collaboration user request** list in the **Procurement and sourcing** module (the Procurement and sourcing module is not accessible to external users).</span></span>

### <a name="provision-a-user"></a><span data-ttu-id="ecbc0-131">ユーザーのプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="ecbc0-131">Provision a user</span></span>

<span data-ttu-id="ecbc0-132">新しいユーザーがプロビジョニングを要求する前に、そのユーザーは、1 つ以上の仕入先勘定として設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-132">Before you can request that a new user is provisioned, that person must be set up as a contact for one or more vendor accounts.</span></span> <span data-ttu-id="ecbc0-133">新しい仕入先コラボレーションのユーザー要求の作成:</span><span class="sxs-lookup"><span data-stu-id="ecbc0-133">To create a request for a new vendor collaboration user:</span></span>

1. <span data-ttu-id="ecbc0-134">[**すべての連絡先**] ページで、[**ベンダー ユーザーのプロビジョニング**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-134">On the **All contacts** page, click **Provision vendor user**.</span></span>
2. <span data-ttu-id="ecbc0-135">ユーザーの電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-135">Enter an email address for the user.</span></span> <span data-ttu-id="ecbc0-136">このアドレスは、Finance and Operations にログオンするユーザーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-136">This address will be used by the user to log onto Finance and Operations.</span></span> <span data-ttu-id="ecbc0-137">電子メール アドレスが Microsoft Azure でテナントとして登録されているドメインに属する場合、プロビジョニング プロセスが正常に完了するためには、電子メール アドレスが既存の Azure Active Directory (AAD) のアカウントである必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-137">If the email address belongs to a domain registered as a tenant with Microsoft Azure, then the email address has to be an existing Azure Active Directory (AAD) account in order for the provisioning process to complete successfully.</span></span> <span data-ttu-id="ecbc0-138">電子メール アドレスが Microsoft Azure で登録されているドメインに属さなない場合は、プロビジョニング プロセスの一部として ADD アカウントが作成され、新しいユーザーは招待メールを受信します。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-138">If the email address does not belong to a domain registered with Microsoft Azure, an ADD account will be created as part of the provisioning process and the new user will receive an invitation mail.</span></span> <span data-ttu-id="ecbc0-139">@hotmail.com、@gmail.com、@comcast.net などのドメインを含む消費者向け電子メール アドレスは、Finance and Operations ユーザーを登録するために使用できません。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-139">Consumer email addresses with domains such as @hotmail.com, @gmail.com, or @comcast.net cannot be used to register a Finance and Operations user.</span></span>
3. <span data-ttu-id="ecbc0-140">[**仕入先コラボレーションへのアクセスの許可**] オプションで、ユーザーがアクセスを必要とするすべての法人で [**はい**] を設定します。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-140">Set the **Vendor collaboration access allowed** option to **Yes** for all the legal entities that the user needs access to.</span></span>
4. <span data-ttu-id="ecbc0-141">[**ユーザー ロールの割り当て**] セクションで、新しいユーザーが持つ必要のあるセキュリティ ロールの [**割り当て**] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-141">In the **Assign user roles** section, select the **Assign** check box for the security roles that the new user should have.</span></span>
5. <span data-ttu-id="ecbc0-142">[**送信**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-142">Click **Submit**.</span></span>

<span data-ttu-id="ecbc0-143">仕入先ユーザーが送信を要求する場合、[**仕入先コラボレーションへのアクセスの許可**] フィールドは、選択された仕入先アカウントのために [**はい**] に設定され、ユーザー要求のワークフローは開始されます。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-143">When the vendor user request is submitted, the **Vendor collaboration access allowed** field is set to **Yes** for the selected vendor account and a user request workflow is started.</span></span> <span data-ttu-id="ecbc0-144">ワークフローの一部として、新しいユーザーは Finance and Operations で作成し、セキュリティ ロールが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-144">As part of the workflow, a new user is created in Finance and Operations, and security roles are assigned.</span></span> <span data-ttu-id="ecbc0-145">また、Azure B2B サービスは、Azure ポータルでインタラクションを開始することを有効化し、Finance and Operations ユーザー アカウントで関連する新しいもしくは既存の AAD アカウントを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-145">In addition, an Azure B2B service is activated which initiates interaction with Azure portal and associates a new or existing AAD account with the Finance and Operations user account.</span></span> <span data-ttu-id="ecbc0-146">詳細については、[Azure AD B2B コラボレーションとは何ですか。](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-146">For more information, see [What is Azure AD B2B collaboration?](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b).</span></span>

### <a name="inactivate-a-user"></a><span data-ttu-id="ecbc0-147">ユーザーの無効化</span><span class="sxs-lookup"><span data-stu-id="ecbc0-147">Inactivate a user</span></span>

<span data-ttu-id="ecbc0-148">ユーザーの仕入先コラボレーションへのアクセス許可を削除する 2 つの方法があります:</span><span class="sxs-lookup"><span data-stu-id="ecbc0-148">There are two ways to remove access to vendor collaboration for a user:</span></span>

-   <span data-ttu-id="ecbc0-149">仕入先の [**連絡先**] ページで、連絡先のために [**仕入先コラボレーションへのアクセス許可**] オプションを [**いいえ**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-149">On the **Contacts** page for the vendor, set the **Vendor collaboration access allowed** option to **No** for the contact.</span></span> <span data-ttu-id="ecbc0-150">これは、個人が連絡先である個別の法人ごとに行うことができます。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-150">This can be done individually per legal entity that the person is a contact for.</span></span> <span data-ttu-id="ecbc0-151">このオプションは、調達担当者のみが使用できます。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-151">This option can only be used by procurement professionals.</span></span>
-   <span data-ttu-id="ecbc0-152">**仕入先ユーザーの無効化**リクエストを送信して、ユーザー アカウント全体を無効化します。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-152">Inactivate the entire user account, by submitting an **Inactivate vendor user** request.</span></span>

<span data-ttu-id="ecbc0-153">ユーザーを無効にする要求:</span><span class="sxs-lookup"><span data-stu-id="ecbc0-153">To request that a user is inactivated:</span></span>

1.  <span data-ttu-id="ecbc0-154">[**すべての連絡先**] ページで、[**無効化** **仕入先ユーザー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-154">On the **All contacts** page, click **Inactivate** **vendor user**.</span></span>
2.  <span data-ttu-id="ecbc0-155">[**業務の妥当性**] フィールドにコメントを記述します。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-155">Write a comment in the **Business justification** field.</span></span>
3.  <span data-ttu-id="ecbc0-156">[**送信**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-156">Click **Submit**.</span></span>

### <a name="modify-security-roles"></a><span data-ttu-id="ecbc0-157">セキュリティ ロールを変更</span><span class="sxs-lookup"><span data-stu-id="ecbc0-157">Modify security roles</span></span>

<span data-ttu-id="ecbc0-158">セキュリティ ロールのリストが編集できること以外は、[**仕入先ユーザー ロールの管理**] ページは、[**仕入先ユーザーのプロビジョニング**] ページと同じです。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-158">The **Maintain vendor user roles** page is the same as the **Provision vendor user** page except that the list of security roles can be edited.</span></span>  

<span data-ttu-id="ecbc0-159">ユーザーのためのセキュリティ ロールの変更要求:</span><span class="sxs-lookup"><span data-stu-id="ecbc0-159">To request that the security roles are modified for a user:</span></span>

1.  <span data-ttu-id="ecbc0-160">[**すべての連絡先**] ページで、[**管理** **仕入先ユーザー ロール**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-160">On the **All contacts** page, click **Maintain** **vendor user roles**.</span></span>
2.  <span data-ttu-id="ecbc0-161">[**業務の妥当性**] フィールドにコメントを記述します。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-161">Write a comment in the **Business justification** field.</span></span>
3.  <span data-ttu-id="ecbc0-162">[**ユーザー ロールの管理**] セクションで割り当てるセキュリティ ロールを選択、または削除するものをクリアします。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-162">In the **Maintain user roles** section, select the security roles that you want to assign, or clear the ones that you want to remove.</span></span>
4.  <span data-ttu-id="ecbc0-163">[**送信**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ecbc0-163">Click **Submit**.</span></span>





