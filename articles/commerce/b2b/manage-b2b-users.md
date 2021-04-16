---
title: B2B eコマース Web サイトでのビジネス パートナー ユーザーの管理
description: このトピックでは、管理者が企業間 (B2B) の e コマース Web サイトに関するビジネス パートナー ユーザーを追加、編集、削除する方法について説明します。
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7c1bd8d9cb494cef78fa7c14f6c391821d48749a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799856"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a><span data-ttu-id="071dc-103">B2B eコマース Web サイトでのビジネス パートナー ユーザーの管理</span><span class="sxs-lookup"><span data-stu-id="071dc-103">Manage business partner users on B2B e-commerce websites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="071dc-104">このトピックでは、管理者が企業間 (B2B) の e コマース Web サイトに関するビジネス パートナー ユーザーを追加、編集、削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="071dc-104">This topic describes how administrators can add, edit, and delete business partner users on business-to-business (B2B) e-commerce websites.</span></span>

<span data-ttu-id="071dc-105">B2B e コマースの Web サイトでは、組織が取引相手となるために登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="071dc-105">B2B e-commerce websites require that organizations register to become business partners.</span></span> <span data-ttu-id="071dc-106">組織が B2B e コマースの Web サイトに登録の詳細を送信すると、資格審査プロセスを経由します。</span><span class="sxs-lookup"><span data-stu-id="071dc-106">After an organization submits registration details to a B2B e-commerce website, it goes through a qualification process.</span></span> <span data-ttu-id="071dc-107">組織が審査つ通貨した場合は、ビジネスパートナーとしてオンボードされます。</span><span class="sxs-lookup"><span data-stu-id="071dc-107">If the organization is successfully qualified, it's onboarded as a business partner.</span></span>

<span data-ttu-id="071dc-108">組織がビジネス パートナーとしてオンボードされた後、ビジネスパートナーへの要求を開始した組織ユーザーは、管理者ユーザーとして識別され、B2B e コマース Web サイトの承認された追加のユーザーに権限を与える特権が付与されます。</span><span class="sxs-lookup"><span data-stu-id="071dc-108">After an organization is onboarded as a business partner, the organization user who initiated the request to become a business partner is identified as the administrator user and is granted privileges to onboard additional authorized users of the B2B e-commerce website.</span></span> <span data-ttu-id="071dc-109">これらの認可されたユーザーは、ビジネスパートナーの代理として注文を出すことができます。</span><span class="sxs-lookup"><span data-stu-id="071dc-109">These authorized users can then place orders on behalf of the business partner.</span></span>

## <a name="turn-on-the-b2b-e-commerce-capabilities-feature-in-commerce-headquarters"></a><span data-ttu-id="071dc-110">Commerce 本部で B2B の e コマース機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="071dc-110">Turn on the B2B e-commerce capabilities feature in Commerce headquarters</span></span>

<span data-ttu-id="071dc-111">Commerce 本部の B2B e コマース機能により、組織はビジネスパートナーをオンボードし、管理者ユーザーを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="071dc-111">The B2B e-commerce capabilities feature in Commerce headquarters enables organizations to onboard business partners and define administrator users.</span></span> <span data-ttu-id="071dc-112">また、この機能を使用すると、管理者はビジネス パートナーのユーザーとチームを作成および管理し、特定のロールを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="071dc-112">This feature also enables administrators to create and manage business partner users and teams, and to assign specific roles to them.</span></span> <span data-ttu-id="071dc-113">最終的に、ビジネス パートナー ユーザーは注文テンプレートを作成し、既存の注文を使用して製品を再注文することができます。</span><span class="sxs-lookup"><span data-stu-id="071dc-113">Finally, it enables business partner users to create order templates and use existing orders to reorder products.</span></span>

<span data-ttu-id="071dc-114">Commerce 本部の B2B e コマース機能をオンにするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="071dc-114">To turn on the B2B e-commerce capabilities feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="071dc-115">**ワークスペース \> 機能管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="071dc-115">Go to **Workspaces \> Feature Management**.</span></span>
1. <span data-ttu-id="071dc-116">**すべて** タブの、**モジュール** フィールドで **小売およびコマース** という語句でフィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="071dc-116">On the **All** tab, filter on the **Module** field by using the term **Retail and commerce**.</span></span>
1. <span data-ttu-id="071dc-117">**B2B e コマース機能の使用を有効化** という機能を選択し、**今すぐ有効化を** 選択します。</span><span class="sxs-lookup"><span data-stu-id="071dc-117">Find and select the feature that is named **Enable the use of B2B eCommerce capabilities**, and then select **Enable now**.</span></span>

## <a name="create-a-number-sequence-and-add-it-to-commerce-shared-parameters"></a><span data-ttu-id="071dc-118">番号順序を作成して Commerce の共有パラメータに追加する</span><span class="sxs-lookup"><span data-stu-id="071dc-118">Create a number sequence and add it to Commerce shared parameters</span></span>

<span data-ttu-id="071dc-119">番号順序は、ID が必要なマスター データ レコードおよびトランザクション レコードに対して読みやすい固有の ID を生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="071dc-119">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="071dc-120">番号シーケンスの詳細については、[番号シーケンスの概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="071dc-120">For more information about number sequences, see [Number sequences overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview).</span></span>

<span data-ttu-id="071dc-121">番号順序を作成し、これを Commerce 本部の [Commerce] 共有パラメータに追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="071dc-121">To create a number sequence and add it to Commerce shared parameters in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="071dc-122">**小売りとコマース \> 本部の設定 \> 番号順序 \> 番号順序** に移動して、番号順序を作成します。</span><span class="sxs-lookup"><span data-stu-id="071dc-122">Go to **Retail and Commerce \> Headquarters setup \> Number sequences \> Number sequences**, and create a number sequence.</span></span>
1. <span data-ttu-id="071dc-123">**小売りとコマース \> 本部の設定 \> パラメーター \> Commerce の共有パラメーター** に移動し、**顧客階層 ID** 参照に新しい番号順序を追加します。</span><span class="sxs-lookup"><span data-stu-id="071dc-123">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce shared parameters**, and add the new number sequence to the **Customer hierarchy ID** reference.</span></span>

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a><span data-ttu-id="071dc-124">新しいビジネス パートナーで使用する管理者ユーザーの設定</span><span class="sxs-lookup"><span data-stu-id="071dc-124">Set up the administrator user for a new business partner</span></span>

<span data-ttu-id="071dc-125">潜在的なビジネスパートナーは、サイト上のリンクを介してオンボーディング リクエストを送信することで、B2B e コマース Web サイトへのオンボーディング プロセスを開始することができます。</span><span class="sxs-lookup"><span data-stu-id="071dc-125">Potential business partners can initiate the onboarding process to a B2B e-commerce website by submitting an onboarding request via a link on the site.</span></span> <span data-ttu-id="071dc-126">潜在的なビジネス パートナーのユーザーがリンクを選択した後、オンボーディングとサインアップに必要な詳細を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="071dc-126">After a potential business partner user selects the link, they can provide the details that are required for onboarding and sign-up.</span></span> <span data-ttu-id="071dc-127">要求が送信されると、送信確認ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="071dc-127">After the request is submitted, a submission confirmation page appears.</span></span> <span data-ttu-id="071dc-128">申請が承認された場合、変更の要求を開始した申請者 (つまり、変更を開始したユーザー) がビジネス パートナーの管理者ユーザーになります。</span><span class="sxs-lookup"><span data-stu-id="071dc-128">If the submission is approved, the requestor (that is, the user who initiated the onboarding request) becomes the business partner administrator user.</span></span>

<span data-ttu-id="071dc-129">Commerce 本部でビジネス パートナーの管理者ユーザーを承認・設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="071dc-129">To approve and set up a business partner administrator user in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="071dc-130">**小売りとコマース IT \> 配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="071dc-130">Go to **Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="071dc-131">**P-0001** ジョブを実行して、すべてのビジネス パートナーが要求を Commerce 本部に取り込みます。</span><span class="sxs-lookup"><span data-stu-id="071dc-131">Run the **P-0001** job to pull all business partner onboarding requests into Commerce headquarters.</span></span>
1. <span data-ttu-id="071dc-132">**P-0001** ジョブが正常に実行された後、**小売りとコマース IT \> 顧客** に移動し、**同期モード ジョブから顧客とビジネスパートナーを同期する** ジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="071dc-132">After the **P-0001** job has successfully run, go to **Retail and Commerce IT \> Customer**, and run the **Synchronize customers and business partners from async mode** job.</span></span> <span data-ttu-id="071dc-133">このジョブが正常に実行された後、オンボードの要求は、Commerce 本部の見込顧客レコードとして作成されます。</span><span class="sxs-lookup"><span data-stu-id="071dc-133">After this job has successfully run, the onboarding requests are created as prospects records in Commerce headquarters.</span></span> <span data-ttu-id="071dc-134">これらのレコードの **タイプ ID** フィールドは、**B2B 見込顧客** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="071dc-134">The **Type ID** field of these records is set to **B2B prospect**.</span></span>
1. <span data-ttu-id="071dc-135">**顧客 \> すべての見込顧客** に移動し、見込顧客ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="071dc-135">Go to **Customers \> All prospects**, and open the prospects page.</span></span>
1. <span data-ttu-id="071dc-136">新しい取引先の見込顧客レコードを選択して、見込顧客の詳細ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="071dc-136">Select the prospect record for the new business partner to open the prospect details page.</span></span>
1. <span data-ttu-id="071dc-137">**全般** タブ で、**変換 \> 承認/否認** を選択し、オンボード要求を承認または否認します。</span><span class="sxs-lookup"><span data-stu-id="071dc-137">On the **General** tab, select **Convert \> Approve/Reject** to approve or reject the onboarding request.</span></span> <span data-ttu-id="071dc-138">確認メッセージが表示されたら、処理の続行を確認し、要求を承認します。</span><span class="sxs-lookup"><span data-stu-id="071dc-138">When a confirmation message appears, confirm that you want to continue with the process, and approve the request.</span></span> <span data-ttu-id="071dc-139">申請者のメールアドレスにメールが送信され、組織がビジネスパートナーとして承認されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="071dc-139">An email is then sent to the requestor's email address to confirm that their organization has been approved as a business partner.</span></span>

    <span data-ttu-id="071dc-140">要求を承認すると、見込顧客レコードの **状態** フィールドが **承認済** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="071dc-140">After you approve the request, the **Status** field of the prospect record is set to **Approved**.</span></span> <span data-ttu-id="071dc-141">さらに、システムに 2 つの新しい顧客レコードが作成されます。**組織のタイプ** : 取引先組織の顧客レコード、**担当者タイプ** : 申請者の顧客レコード。</span><span class="sxs-lookup"><span data-stu-id="071dc-141">Additionally, two new customer records are created in the system: a **Type Organization** customer record for the business partner organization and a **Type Person** customer record for the requestor.</span></span> <span data-ttu-id="071dc-142">また、取引先の顧客階層レコードも作成されます。</span><span class="sxs-lookup"><span data-stu-id="071dc-142">A customer hierarchy record for the business partner is also created.</span></span> <!--(Please refer to the Org modeling of B2B customer section in this document for more information)-->

1. <span data-ttu-id="071dc-143">**小売およびコマース IT \> 配送スケジュール** に移動し、**1010** (**顧客**) ジョブを実行し、新規作際された顧客と顧客の階層レコードをチャネル データベースに プッシュします。</span><span class="sxs-lookup"><span data-stu-id="071dc-143">Go to **Retail and Commerce IT \> Distribution schedule**, and run the **1010** (**Customers**) job to push the newly created customer and customer hierarchy records to the channel database.</span></span>

<span data-ttu-id="071dc-144">リクエストが承認され、顧客と顧客階層レコードがチャネルデータベースに同期されると、申請者は、リクエストを送信した際に提供されたメールアドレスを使用して、B2B e コマース Web サイトにサインインすることができます。</span><span class="sxs-lookup"><span data-stu-id="071dc-144">After the request is approved, and the customer and customer hierarchy records are synced to the channel database, the requestor can sign in to the B2B e-commerce website by using the email address that they provided when they submitted the request.</span></span> <span data-ttu-id="071dc-145">ユーザーは、登録フローを使用してアカウントのパスワードを定義できます。</span><span class="sxs-lookup"><span data-stu-id="071dc-145">Users can use the sign-up flow to define the password for their account.</span></span>

## <a name="onboard-additional-business-partner-users"></a><span data-ttu-id="071dc-146">追加の取引先ユーザーをオンボードする</span><span class="sxs-lookup"><span data-stu-id="071dc-146">Onboard additional business partner users</span></span>

<span data-ttu-id="071dc-147">取引先の管理者ユーザーは、必要に応じて、B2B eコマースの Web サイトに取引先ユーザーを追加で提供することができます。</span><span class="sxs-lookup"><span data-stu-id="071dc-147">The business partner administrator user can onboard additional business partner users to the B2B e-commerce website as required.</span></span>

<span data-ttu-id="071dc-148">追加のビジネス パートナー ユーザーを B2B e コマース Webサイトに変更するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="071dc-148">To onboard additional business partner users to a B2B e-commerce website, follow these steps.</span></span>

1. <span data-ttu-id="071dc-149">B2B e コマースの Web サイトに管理者としてログインします。</span><span class="sxs-lookup"><span data-stu-id="071dc-149">Sign in to the B2B e-commerce website as an administrator.</span></span>
1. <span data-ttu-id="071dc-150">**自分のアカウント \> 組織のユーザー \> 詳細の表示** に移動し、**ユーザーの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="071dc-150">Go to **My Account \> Organization users \> View details**, and select **Add a user**.</span></span>
1. <span data-ttu-id="071dc-151">必要な情報を入力し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="071dc-151">Enter the required information, and then select **Save**.</span></span> <span data-ttu-id="071dc-152">新規ユーザーの状態を **保留中** に設定します。</span><span class="sxs-lookup"><span data-stu-id="071dc-152">The status of the new user is set to **Pending**.</span></span>

    <span data-ttu-id="071dc-153">**P-0001** および **非同期モードから顧客と取引先を同期する** ジョブの実行後は、Commerce 本部に新規ユーザーの **担当者タイプ** 顧客レコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="071dc-153">After the **P-0001** and **Synchronize customers and business partners from async mode** jobs are run, a **Type Person** customer record for the new user is created in Commerce headquarters.</span></span> <span data-ttu-id="071dc-154">この顧客レコードは、関連する取引先の顧客階層レコードにも関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="071dc-154">This customer record is also associated with the relevant business partner's customer hierarchy record.</span></span> <span data-ttu-id="071dc-155">さらに、新規ユーザーのメールアドレスにメールが送信され、取引先組織のユーザーとして追加され、B2B e Web サイトにサインインできるようになったことが通知されます。</span><span class="sxs-lookup"><span data-stu-id="071dc-155">Additionally, an email is sent to the new user's email address to notify them that they have been added as a user of the business partner organization and can now sign in to the B2B e-commerce website.</span></span>

1. <span data-ttu-id="071dc-156">**1010** (**顧客**) ジョブを実行して 、新しい取引先ユーザーをチャンネル データベースに同期します。</span><span class="sxs-lookup"><span data-stu-id="071dc-156">Run the **1010** (**Customers**) job to sync the new business partner user to the channel database.</span></span>

<span data-ttu-id="071dc-157">顧客レコードが同期された後、B2B e コマース Web サイトのユーザーの状態が **有効** に設定され、新しいユーザーはメール アドレスを使用して B2B e コマース Web サイトにログインできます。</span><span class="sxs-lookup"><span data-stu-id="071dc-157">After the customer record is synced, the status of the user on the B2B e-commerce website is set to **Active**, and the new user can sign in to the B2B e-commerce website by using their email address.</span></span> <span data-ttu-id="071dc-158">ユーザーは、登録フローを使用してアカウントのパスワードを定義できます。</span><span class="sxs-lookup"><span data-stu-id="071dc-158">Users can use the sign-up flow to define the password for their account.</span></span>

## <a name="edit-business-partner-user-details"></a><span data-ttu-id="071dc-159">取引先のユーザー詳細情報を編集する</span><span class="sxs-lookup"><span data-stu-id="071dc-159">Edit business partner user details</span></span>

<span data-ttu-id="071dc-160">取引先ユーザーの詳細を編集するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="071dc-160">To edit the details of business partner users, follow these steps.</span></span>

1. <span data-ttu-id="071dc-161">B2B e コマースの Web サイトに管理者としてログインします。</span><span class="sxs-lookup"><span data-stu-id="071dc-161">Sign in to the B2B e-commerce website as an administrator.</span></span>
1. <span data-ttu-id="071dc-162">**自分のアカウント \> 組織ユーザー \> 詳細の表示** に移動し、**編集** ボタン (鉛筆アイコン) を選択して必要な変更を行い、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="071dc-162">Go to **My Account \> Organization users \> View details**, select the **Edit** button (pencil symbol), make the required changes, and then select **Save**.</span></span> <span data-ttu-id="071dc-163">この変更が反映されるのは、**P-0001**、**非同期モードから顧客と取引先を同期する**、**1010** (**顧客**) ジョブが実行された後にのみです。</span><span class="sxs-lookup"><span data-stu-id="071dc-163">The changes take effect only after the **P-0001**, **Synchronize customers and business partners from async mode**, and **1010** (**Customers**) jobs have been run.</span></span>

## <a name="remove-a-business-partner-user"></a><span data-ttu-id="071dc-164">取引先ユーザーの削除</span><span class="sxs-lookup"><span data-stu-id="071dc-164">Remove a business partner user</span></span>

<span data-ttu-id="071dc-165">必要に応じて、管理者は、B2B e コマース Web サイトにアクセスできるユーザーのリストから、ビジネスパートナー組織の既存のユーザーを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="071dc-165">As required, an administrator can remove existing users of a business partner organization from the list of users who can access the B2B e-commerce website.</span></span>

<span data-ttu-id="071dc-166">取引先ユーザーを削除するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="071dc-166">To remove a business partner user, follow these steps.</span></span>

1. <span data-ttu-id="071dc-167">B2B e コマースの Web サイトに管理者としてログインします。</span><span class="sxs-lookup"><span data-stu-id="071dc-167">Sign in to the B2B e-commerce website as an administrator.</span></span>
1. <span data-ttu-id="071dc-168">**自分のアカウント \> 組織のユーザー \> 詳細の表示** に移動し、**削除** ボタン ("X" マーク) を選択します。</span><span class="sxs-lookup"><span data-stu-id="071dc-168">Go to **My Account \> Organization users \> View details**, and select the **Remove** button ("X" symbol).</span></span> <span data-ttu-id="071dc-169">確認メッセージが表示されたら、ユーザーを削除してください。</span><span class="sxs-lookup"><span data-stu-id="071dc-169">When a confirmation message appears, confirm that you want to remove the user.</span></span> <span data-ttu-id="071dc-170">この変更が反映されるのは、**P-0001**、**非同期モードから顧客と取引先を同期する**、**1010** (**顧客**) ジョブが実行された後にのみです。</span><span class="sxs-lookup"><span data-stu-id="071dc-170">The change takes effect only after the **P-0001**, **Synchronize customers and business partners from async mode**, and **1010** (**Customers**) jobs have been run.</span></span>

> [!NOTE]
> <span data-ttu-id="071dc-171">B2B eコマース Web サイトにアクセスできるユーザーの一覧からユーザーを削除すると、対応する顧客レコードが取引先の顧客階層レコードから削除されます。</span><span class="sxs-lookup"><span data-stu-id="071dc-171">When you remove a user from the list of users who can access the B2B e-commerce website, the corresponding customer record is removed from the business partner's customer hierarchy record.</span></span> <span data-ttu-id="071dc-172">ただし、顧客レコード自体は Commerce 本部からは削除されません。</span><span class="sxs-lookup"><span data-stu-id="071dc-172">However, the customer record itself isn't deleted from Commerce headquarters.</span></span>

## <a name="onboard-business-partner-and-users-in-commerce-headquarters"></a><span data-ttu-id="071dc-173">Commerce 本部で取引先とユーザーを変更する</span><span class="sxs-lookup"><span data-stu-id="071dc-173">Onboard business partner and users in Commerce headquarters</span></span>

<span data-ttu-id="071dc-174">管理者は、取引相手やユーザーを Commerce 本部で直接変更することができます。</span><span class="sxs-lookup"><span data-stu-id="071dc-174">Administrators can onboard business partners and users directly in Commerce headquarters.</span></span>

<span data-ttu-id="071dc-175">Commerce 本部の取引先とユーザーをオンボードするには、以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="071dc-175">To onboard business partners and users in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="071dc-176">取引先で使用する **組織のタイプ** タイプの顧客レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="071dc-176">Create a **Type Organization** customer record for the business partner organization.</span></span>
1. <span data-ttu-id="071dc-177">取引先で使用する **担当者タイプ** の顧客レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="071dc-177">Create **Type Person** customer records for business partner users.</span></span> <span data-ttu-id="071dc-178">すべての顧客に対して基本メール アドレスが指定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="071dc-178">Make sure that a primary email address is specified for every customer.</span></span>
1. <span data-ttu-id="071dc-179">取引先組織の管理者ユーザーとして指定刷る必要のある **担当者タイプ** の顧客レコードについては、 **小売り** クイックタブで、**B2B 管理者** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="071dc-179">For each **Type Person** customer record that must be designated as an administrator user of the business partner organization, on the **Retail** FastTab, set the **B2B administrator** option to **Yes**.</span></span>
1. <span data-ttu-id="071dc-180">顧客の階層 ID を作成します。</span><span class="sxs-lookup"><span data-stu-id="071dc-180">Create a customer hierarchy ID.</span></span> <span data-ttu-id="071dc-181">**名前** フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="071dc-181">In the **Name** field, enter a name.</span></span>
1. <span data-ttu-id="071dc-182">**組織** フィールドで、取引先組織の顧客を入力します。</span><span class="sxs-lookup"><span data-stu-id="071dc-182">In the **Organization** field, enter the business partner organization customer.</span></span>
1. <span data-ttu-id="071dc-183">**追加** を選択し、**名前** フィールドで顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="071dc-183">Select **Add**, and then select a customer in the **Name** field.</span></span>
1. <span data-ttu-id="071dc-184">このプロセスを繰り返し、階層に顧客を追加していきます。</span><span class="sxs-lookup"><span data-stu-id="071dc-184">Repeat this process to add additional customers to the hierarchy.</span></span>

## <a name="additional-information"></a><span data-ttu-id="071dc-185">追加情報</span><span class="sxs-lookup"><span data-stu-id="071dc-185">Additional information</span></span>

- <span data-ttu-id="071dc-186">このトピックで説明されているジョブはすべて、バッチ形式でスケジュール上で実行するように構成することができます。</span><span class="sxs-lookup"><span data-stu-id="071dc-186">All the jobs that are mentioned in this topic can be configured to run on a schedule in a batch format.</span></span> <span data-ttu-id="071dc-187">取引先が必要に応じてバッチジョブを構成することが意図されています。</span><span class="sxs-lookup"><span data-stu-id="071dc-187">The expectation is that business partners will configure batch jobs as required.</span></span>
- <span data-ttu-id="071dc-188">現在、管理者ユーザーとして指定できるユーザー/顧客レコードは1つのみであり、そのロールは Commerce 本部でのみ変更できます。</span><span class="sxs-lookup"><span data-stu-id="071dc-188">Currently, only one user/customer record can be designated as an administrator user, and that role can be changed only in Commerce headquarters.</span></span> <span data-ttu-id="071dc-189">取引先が複数の管理者を指定したり、B2B の e コマース Web サイトから管理者を変更したりできるような、セルフサービス機能には対応していません。</span><span class="sxs-lookup"><span data-stu-id="071dc-189">There is no support for self-service capabilities that let business partners to designate multiple administrators or change administrators from B2B e-commerce websites.</span></span>
<!--- The modules and labels of the different fields referenced in the screenshots for e-commerce are only for illustration purposes. Customers have complete control on the placement of the B2B related modules and the labels.-->
- <span data-ttu-id="071dc-190">ユーザーに対して支出制限を定義することができますが、注文入力プロセス中に支出制限を実施する機能はまだ実装されていません。</span><span class="sxs-lookup"><span data-stu-id="071dc-190">Although spending limits can be defined for users, enforcement of spending limits during the order entry process hasn't yet been implemented.</span></span>
- <span data-ttu-id="071dc-191">B2B e コマース Web サイトでのユーザーエクスペリエンスのビジネス ロジックと検証は、Commerce 本部でユーザーにマッピングされた顧客レコードの構成に基づいています。</span><span class="sxs-lookup"><span data-stu-id="071dc-191">All business logic and validation for a user's experience on a B2B e-commerce website are based on the configuration of the customer record that is mapped to the user in Commerce headquarters.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="071dc-192">追加リソース</span><span class="sxs-lookup"><span data-stu-id="071dc-192">Additional resources</span></span>

[<span data-ttu-id="071dc-193">B2B eコマース サイトの設定</span><span class="sxs-lookup"><span data-stu-id="071dc-193">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="071dc-194">B2B 組織の組織モデリング階層の作成</span><span class="sxs-lookup"><span data-stu-id="071dc-194">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="071dc-195">B2B eコマース サイト用の顧客アカウントの支払方法の構成</span><span class="sxs-lookup"><span data-stu-id="071dc-195">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)

[<span data-ttu-id="071dc-196">B2B eコマース サイトの製品数量制限の設定</span><span class="sxs-lookup"><span data-stu-id="071dc-196">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)

[<span data-ttu-id="071dc-197">番号順序の概要</span><span class="sxs-lookup"><span data-stu-id="071dc-197">Number sequences overview</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]