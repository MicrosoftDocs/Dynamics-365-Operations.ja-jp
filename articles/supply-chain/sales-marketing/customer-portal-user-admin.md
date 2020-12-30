---
title: 顧客ポータルのユーザーの作成と管理
description: このトピックでは、顧客ポータルのユーザー アカウントを作成し、アクセス権限の設定方法について説明します。
author: dasani-madipalli
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e2001d5c0b17ecadf4cb42529d9beb4b3b81805a
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528296"
---
# <a name="create-and-manage-customer-portal-users"></a><span data-ttu-id="950e4-103">顧客ポータルのユーザーの作成と管理</span><span class="sxs-lookup"><span data-stu-id="950e4-103">Create and manage Customer portal users</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="950e4-104">既定の実装では、ユーザーは顧客ポータルを使用して作成された Web サイトを自分で登録することはできません。</span><span class="sxs-lookup"><span data-stu-id="950e4-104">In the out-of-box implementation, there is no way for users to self-register for websites that are created by using the Customer portal.</span></span> <span data-ttu-id="950e4-105">Web サイトにログインして使用するには、ユーザーが管理者で招待されている必要があります。マイクロソフトでは、ユーザーが登録を行う権限を意図的にブロックしています。</span><span class="sxs-lookup"><span data-stu-id="950e4-105">To sign in and use a website, users must be invited by the admin. Microsoft has intentionally blocked the ability of users to self-register.</span></span>

<span data-ttu-id="950e4-106">ユーザーが Web サイトを使用できるようにするには、そのユーザーに対して担当者レコードを作成しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="950e4-106">Before a user can use a website, a contact record must be created for that user.</span></span> <span data-ttu-id="950e4-107">このレコードは、ユーザーが属する顧客アカウントとエンティティを示します。</span><span class="sxs-lookup"><span data-stu-id="950e4-107">This record indicates which customer account and legal entity the user belongs to.</span></span> <span data-ttu-id="950e4-108">この情報は、ユーザーが販売注文の作成と表示できることを保証するために不可欠です。</span><span class="sxs-lookup"><span data-stu-id="950e4-108">This information is essential for ensuring that the user can create and view sales orders.</span></span>

<span data-ttu-id="950e4-109">担当者レコードは、ユーザーが登録した際に自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="950e4-109">When users self-register, contact records are automatically created for them.</span></span> <span data-ttu-id="950e4-110">そのため、ユーザーが正しい顧客アカウントとエンティティを選択しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="950e4-110">Therefore, you can't ensure that a user selects the correct customer account and legal entity.</span></span> <span data-ttu-id="950e4-111">一方で、招待形式の処理では、招待の送信前に、管理者が正しい顧客アカウントとエンティティを担当者レコードに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="950e4-111">On the other hand, the invitation process lets an admin assign the correct customer account and legal entity to the contact record before an invitation is sent.</span></span> <span data-ttu-id="950e4-112">ユーザーが自分で登録できるようなソリューションのカスタマイズを検討している場合は、想定される結果を必ず考慮してください。</span><span class="sxs-lookup"><span data-stu-id="950e4-112">If you're thinking about customizing the solution so that users can self-register, be sure to consider the possible consequences.</span></span>

## <a name="video"></a><span data-ttu-id="950e4-113">ビデオ</span><span class="sxs-lookup"><span data-stu-id="950e4-113">Video</span></span>
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ADkI]

<span data-ttu-id="950e4-114">[顧客を招待して、顧客ポータルへの登録と利用を促進する](https://youtu.be/drGUYHX9QIQ)  ビデオ (上記) は、YouTube で利用可能な [Finance and Operations のプレイリスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)に含まれています。</span><span class="sxs-lookup"><span data-stu-id="950e4-114">The [Invite customers to register and use your customer portal](https://youtu.be/drGUYHX9QIQ) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="prerequisite-setup"></a><span data-ttu-id="950e4-115">前提条件の設定</span><span class="sxs-lookup"><span data-stu-id="950e4-115">Prerequisite setup</span></span>

<span data-ttu-id="950e4-116">Power Apps ポータルの担当者は、Common Data Service の **担当者** エンティティにレコードとして保存されます。</span><span class="sxs-lookup"><span data-stu-id="950e4-116">Contacts in Power Apps portals are stored as records in the **Contacts** entity in Common Data Service.</span></span> <span data-ttu-id="950e4-117">デュアル書き込みでは、これらのレコードが必要に応じて Microsoft Dynamics 365 Supply Chain Management に同期されます。</span><span class="sxs-lookup"><span data-stu-id="950e4-117">Dual-write then syncs these records to Microsoft Dynamics 365 Supply Chain Management as required.</span></span>

<span data-ttu-id="950e4-118">![顧客ポータルの担当者で使用するシステム ダイアグラム](media/customer-portal-contacts.png "顧客ポータルの担当者で使用するシステム ダイアグラム")</span><span class="sxs-lookup"><span data-stu-id="950e4-118">![System diagram for Customer portal contacts](media/customer-portal-contacts.png "System diagram for Customer portal contacts")</span></span>

<span data-ttu-id="950e4-119">新たな顧客の招待をする前に、**担当者** エンティティのマッピングがデュアル書き込みで有効化されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="950e4-119">Before you start to invite new customers, make sure that you've enabled the **Contact** entity mapping in dual-write.</span></span>

## <a name="the-invitation-process"></a><span data-ttu-id="950e4-120">招待の処理</span><span class="sxs-lookup"><span data-stu-id="950e4-120">The invitation process</span></span>

<span data-ttu-id="950e4-121">顧客ポータルに既に存在する担当者を招待するには、Power Apps ポータル ドキュメントにおける [ポータルへの担当者への招待](https://docs.microsoft.com/powerapps/maker/portals/configure/invite-contacts) に記載の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="950e4-121">To invite an existing contact to the Customer portal, follow the steps in [Invite contacts to your portals](https://docs.microsoft.com/powerapps/maker/portals/configure/invite-contacts) in the Power Apps portals documentation.</span></span>

<span data-ttu-id="950e4-122">顧客を顧客ポータルに招待する前に、顧客の [担当者レコード ](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) が有効なものであり、次のように設定されていることを確認してください :</span><span class="sxs-lookup"><span data-stu-id="950e4-122">Before you invite a customer to join the Customer portal, make sure that the customer's [contact record](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) is available and set up in the following way:</span></span>

1. <span data-ttu-id="950e4-123">**会社** フィールドを、Supply Chain Management にて顧客を所属させる法人に設定します。</span><span class="sxs-lookup"><span data-stu-id="950e4-123">Set the **Company** field to the legal entity that you want the customer to belong to in Supply Chain Management.</span></span>
2. <span data-ttu-id="950e4-124">**顧客番号** フィールドを、Supply Chain Management にて顧客に設定する顧客アカウントの番号に設定します。</span><span class="sxs-lookup"><span data-stu-id="950e4-124">Set the **Account Number** field to the customer account number that you want the user to have in Supply Chain Management.</span></span>

<span data-ttu-id="950e4-125">担当者の作成後は、Supply Chain Management でその担当者を表示できるようになります。</span><span class="sxs-lookup"><span data-stu-id="950e4-125">After a contact is created, you should be able to see it in Supply Chain Management.</span></span>

<span data-ttu-id="950e4-126">詳細については、Power Apps ポータル ドキュメントの [ポータルで使用する担当者の構成](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="950e4-126">For more information, see [Configure a contact for use on a portal](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) in the Power Apps portals documentation.</span></span>

## <a name="out-of-box-web-roles-and-entity-permissions"></a><span data-ttu-id="950e4-127">既成の Web ロールとエンティティのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="950e4-127">Out-of-box web roles and entity permissions</span></span>

<span data-ttu-id="950e4-128">Power Apps ポータルのユーザー ロールは 、[Web ロール](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles)と[エンティティのアクセス許可](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions)によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="950e4-128">User roles in Power Apps portals are defined by [web roles](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) and [entity permissions](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions).</span></span> <span data-ttu-id="950e4-129">既定では、顧客ポータルには少数のロールのみが定義されています。</span><span class="sxs-lookup"><span data-stu-id="950e4-129">A few roles are defined for the Customer portal out of the box.</span></span> <span data-ttu-id="950e4-130">新たなロールの作成、既存のロールの変更または削除が可能です。</span><span class="sxs-lookup"><span data-stu-id="950e4-130">You can create new roles, and you can modify or remove existing roles.</span></span>

### <a name="out-of-box-web-roles"></a><span data-ttu-id="950e4-131">既成の Web ロール</span><span class="sxs-lookup"><span data-stu-id="950e4-131">Out-of-box web roles</span></span>

<span data-ttu-id="950e4-132">このセクションでは、顧客ポータルと共に提供される既成の Web ロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="950e4-132">This section describes the web roles that are delivered with the Customer portal.</span></span>

<span data-ttu-id="950e4-133">既成のユーザー ロールの変更方法の詳細については、 Power Apps ポータル ドキュメントに記載の [ポータルで使用する Web ロールの作成](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) と [ポータルのエンティティ権限を使用してレコードに基づくセキュリティを追加する](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="950e4-133">For more information about how to modify the out-of-box user roles, see [Create web roles for portals](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) and [Add record-based security by using entity permissions for portals](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions) in the Power Apps portals documentation.</span></span>

#### <a name="administrator"></a><span data-ttu-id="950e4-134">管理者</span><span class="sxs-lookup"><span data-stu-id="950e4-134">Administrator</span></span>

<span data-ttu-id="950e4-135">管理者は、Web サイトの監視と管理をします。</span><span class="sxs-lookup"><span data-stu-id="950e4-135">The administrator oversees and maintains the website.</span></span> <span data-ttu-id="950e4-136">このユーザーは、顧客ポータルの準備と設定を行います。</span><span class="sxs-lookup"><span data-stu-id="950e4-136">This person will provision and set up the Customer portal.</span></span> <span data-ttu-id="950e4-137">管理者は、ポータルを IT とセキュリティの観点から維持し、すべてが円滑に実行されるように管理します。</span><span class="sxs-lookup"><span data-stu-id="950e4-137">The administrator maintains the IT and security aspects of the portal, and makes sure that everything runs smoothly.</span></span> <span data-ttu-id="950e4-138">管理者は、新たな機能を追加したり、新たな役割を作成することによって、ポータルのカスタマイズや変更をすることもできます。</span><span class="sxs-lookup"><span data-stu-id="950e4-138">The administrator might also customize and/or change the portal by adding new functionalities, creating new roles, and more.</span></span>

#### <a name="customer-representative"></a><span data-ttu-id="950e4-139">顧客担当者</span><span class="sxs-lookup"><span data-stu-id="950e4-139">Customer representative</span></span>

<span data-ttu-id="950e4-140">顧客の担当者は顧客の会社に勤務し、会社が発注する注文を管理します。</span><span class="sxs-lookup"><span data-stu-id="950e4-140">A customer representative works for a customer company and is responsible for managing the orders that the company places.</span></span> <span data-ttu-id="950e4-141">顧客の担当者は、会社が発注したすべての注文、およびそれら発注をしたユーザーを表示できます。</span><span class="sxs-lookup"><span data-stu-id="950e4-141">The customer representative can see all the orders that have been placed for the company and the users who placed them.</span></span> <span data-ttu-id="950e4-142">さらに、顧客担当者は、アカウント全体の情報を見ることができ、どの担当者がそのアカウントに代わって注文することができるかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="950e4-142">Additionally, the customer representative can see information about the overall account and which contacts can place orders on behalf of that account.</span></span>

#### <a name="authorized-users"></a><span data-ttu-id="950e4-143">承認されたユーザー</span><span class="sxs-lookup"><span data-stu-id="950e4-143">Authorized users</span></span>

<span data-ttu-id="950e4-144">承認されたユーザーは、発注処理や、発注した注文の状態を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="950e4-144">Authorized users can place orders and view the status of the orders that they have placed.</span></span> <span data-ttu-id="950e4-145">社内の他のユーザーは、注文の状態を表示できません。</span><span class="sxs-lookup"><span data-stu-id="950e4-145">However, they can't view the status of orders that other users in their company have placed.</span></span>

#### <a name="unauthorized-users"></a><span data-ttu-id="950e4-146">承認されていないユーザー</span><span class="sxs-lookup"><span data-stu-id="950e4-146">Unauthorized users</span></span>

<span data-ttu-id="950e4-147">承認されていないユーザーはデータを表示できません。</span><span class="sxs-lookup"><span data-stu-id="950e4-147">Unauthorized users can't view any data.</span></span> <span data-ttu-id="950e4-148">これらのユーザーは、契約条件などの公開された情報だけでなく、顧客ポータルを実行している会社に関する詳細情報を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="950e4-148">They can see only public information, such as terms and conditions, and details about the company that is running the Customer portal.</span></span>

#### <a name="example"></a><span data-ttu-id="950e4-149">例</span><span class="sxs-lookup"><span data-stu-id="950e4-149">Example</span></span>

<span data-ttu-id="950e4-150">次の表に、各 Web ロールのユーザーがシステム内で参照できる販売注文を示します。</span><span class="sxs-lookup"><span data-stu-id="950e4-150">The following table shows which sales orders the users in each web role can see in the system.</span></span>

| <span data-ttu-id="950e4-151">販売注文</span><span class="sxs-lookup"><span data-stu-id="950e4-151">Sales order</span></span> | <span data-ttu-id="950e4-152">管理者</span><span class="sxs-lookup"><span data-stu-id="950e4-152">Administrator</span></span> | <span data-ttu-id="950e4-153">顧客 &nbsp;X の顧客代表者</span><span class="sxs-lookup"><span data-stu-id="950e4-153">Customer representative for customer&nbsp;X</span></span> | <span data-ttu-id="950e4-154">承認されたユーザー : ジェーン</span><span class="sxs-lookup"><span data-stu-id="950e4-154">Authorized user: Jane</span></span> | <span data-ttu-id="950e4-155">承認されたユーザー : サム</span><span class="sxs-lookup"><span data-stu-id="950e4-155">Authorized user: Sam</span></span> | <span data-ttu-id="950e4-156">承認されていないユーザー : メイ</span><span class="sxs-lookup"><span data-stu-id="950e4-156">Unauthorized user: May</span></span> |
|---|---|---|---|---|---|
| <span data-ttu-id="950e4-157">顧客 &nbsp; X 発注者 : &nbsp; Jane</span><span class="sxs-lookup"><span data-stu-id="950e4-157">Customer&nbsp;X Orderer:&nbsp;Jane</span></span> | <span data-ttu-id="950e4-158">有</span><span class="sxs-lookup"><span data-stu-id="950e4-158">Yes</span></span> | <span data-ttu-id="950e4-159">有</span><span class="sxs-lookup"><span data-stu-id="950e4-159">Yes</span></span> | <span data-ttu-id="950e4-160">有</span><span class="sxs-lookup"><span data-stu-id="950e4-160">Yes</span></span> | <span data-ttu-id="950e4-161">無</span><span class="sxs-lookup"><span data-stu-id="950e4-161">No</span></span> | <span data-ttu-id="950e4-162">無</span><span class="sxs-lookup"><span data-stu-id="950e4-162">No</span></span> |
| <span data-ttu-id="950e4-163">顧客 &nbsp; X 発注者 : &nbsp; サム</span><span class="sxs-lookup"><span data-stu-id="950e4-163">Customer&nbsp;X Orderer:&nbsp;Sam</span></span> | <span data-ttu-id="950e4-164">有</span><span class="sxs-lookup"><span data-stu-id="950e4-164">Yes</span></span> | <span data-ttu-id="950e4-165">有</span><span class="sxs-lookup"><span data-stu-id="950e4-165">Yes</span></span> | <span data-ttu-id="950e4-166">無</span><span class="sxs-lookup"><span data-stu-id="950e4-166">No</span></span> | <span data-ttu-id="950e4-167">有</span><span class="sxs-lookup"><span data-stu-id="950e4-167">Yes</span></span> | <span data-ttu-id="950e4-168">無</span><span class="sxs-lookup"><span data-stu-id="950e4-168">No</span></span> |
| <span data-ttu-id="950e4-169">顧客 &nbsp; Y 発注者 : &nbsp; メイ</span><span class="sxs-lookup"><span data-stu-id="950e4-169">Customer&nbsp;Y Orderer:&nbsp;May</span></span> | <span data-ttu-id="950e4-170">有</span><span class="sxs-lookup"><span data-stu-id="950e4-170">Yes</span></span> | <span data-ttu-id="950e4-171">無</span><span class="sxs-lookup"><span data-stu-id="950e4-171">No</span></span> | <span data-ttu-id="950e4-172">無</span><span class="sxs-lookup"><span data-stu-id="950e4-172">No</span></span> | <span data-ttu-id="950e4-173">無</span><span class="sxs-lookup"><span data-stu-id="950e4-173">No</span></span> | <span data-ttu-id="950e4-174">無</span><span class="sxs-lookup"><span data-stu-id="950e4-174">No</span></span> |

> [!NOTE]
> <span data-ttu-id="950e4-175">サムとジェーンのどちらも顧客 X に勤務する担当者ですが、自分が発注した注文のみを表示でき、その他注文は表示されません。</span><span class="sxs-lookup"><span data-stu-id="950e4-175">Even though both Sam and Jane are contacts who work for customer X, they can see only the orders that they themselves have placed and nothing else.</span></span> <span data-ttu-id="950e4-176">メイは、システム内に注文があっても、承認されていないユーザーであるため、顧客ポータルで当該注文を表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="950e4-176">Although May has an order in the system, she can't see that order in the Customer portal, because she is an unauthorized user.</span></span> <span data-ttu-id="950e4-177">(さらに、メイは顧客のポータル以外のチャネルを使用して発注している必要があります)</span><span class="sxs-lookup"><span data-stu-id="950e4-177">(Additionally, she must have placed the order through some channel other than the Customer portal.)</span></span>
