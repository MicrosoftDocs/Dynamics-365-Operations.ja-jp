---
title: 機能の管理
description: このトピックでは、管理者が Microsoft Dynamics 365 Talent のプレビュー機能を有効にできる方法について説明し、プレビューで現在有効な機能を一覧表示します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.1.0, Talent
ms.openlocfilehash: d818e9e04ce88e5ab285ef8176334809447fb477
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006432"
---
# <a name="manage-features"></a><span data-ttu-id="60cad-103">機能の管理</span><span class="sxs-lookup"><span data-stu-id="60cad-103">Manage features</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="60cad-104">Microsoft Dynamics 365 Human Resources の人事管理サービス (HCM) 機能の継続的なロールアウトの一環として、お客様にできるだけ早く新しい機能を体験していただきたいと思います。</span><span class="sxs-lookup"><span data-stu-id="60cad-104">As part of our continuous rollout of human capital management (HCM) capabilities for Microsoft Dynamics 365 Human Resources, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="60cad-105">管理者はそれぞれの環境でプレビュー機能を表示し使用することができます。</span><span class="sxs-lookup"><span data-stu-id="60cad-105">Administrators can see and use preview features in their environments.</span></span> <span data-ttu-id="60cad-106">これらの機能は、一般的な使用可能性の準備がほぼ整い、および徹底したテストを経ています。</span><span class="sxs-lookup"><span data-stu-id="60cad-106">These features are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="60cad-107">一般提供にリリースする前に、顧客フィードバックおよび検証の最終ラウンドを探しています。</span><span class="sxs-lookup"><span data-stu-id="60cad-107">We're just looking for a final round of customer feedback and validation before we release them for general availability.</span></span>

<span data-ttu-id="60cad-108">このトピックでは、プレビュー機能を有効にできる方法について説明し、プレビューで現在使用可能な機能を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="60cad-108">This topic describes how you can enable preview features, and it lists the features that are currently available for preview.</span></span> <span data-ttu-id="60cad-109">このリストは、一般提供にリリースされる機能およびプレビューにリリースされる新しい機能として更新されます。</span><span class="sxs-lookup"><span data-stu-id="60cad-109">This list will be updated as features are released to general availability and as new features are released to preview.</span></span> <span data-ttu-id="60cad-110">プレビューに新しい機能がリリースされるときに、通知は表示されません。</span><span class="sxs-lookup"><span data-stu-id="60cad-110">No notification is given when new features are released to preview.</span></span> <span data-ttu-id="60cad-111">ユーザーは、機能を確認し始めます。</span><span class="sxs-lookup"><span data-stu-id="60cad-111">Users will just start to see the features.</span></span> <span data-ttu-id="60cad-112">Talent の新機能に関する詳細は、[Dynamics 365 Talent の新機能と変更](./whats-new.md) および [Dynamics 365 と Power Platform Release Notes](https://docs.microsoft.com/business-applications-release-notes) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="60cad-112">For more information about new features in Talent, see [What's new or changed in Dynamics 365 Talent](./whats-new.md) and [Dynamics 365 and Power Platform Release Notes](https://docs.microsoft.com/business-applications-release-notes).</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="60cad-113">プレビュー機能の有効化または無効化</span><span class="sxs-lookup"><span data-stu-id="60cad-113">Enable or disable preview features</span></span>

<span data-ttu-id="60cad-114">プレビュー機能にアクセスするには、まず、環境でプレビュー機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="60cad-114">To access preview features, you must first enable them in your environment.</span></span> <span data-ttu-id="60cad-115">プレビュー機能の有効化または無効化は、環境に特有のものです。</span><span class="sxs-lookup"><span data-stu-id="60cad-115">Enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="60cad-116">**プレビュー機能**設定をオンにして、その環境内の組織にいるすべてのユーザーに対してプレビュー機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="60cad-116">When you turn on the **Preview Features** setting, you enable preview features for all users in your organization who are in that environment.</span></span> <span data-ttu-id="60cad-117">設定をオフにして、プレビュー機能を無効にし、ユーザーがアクセスできないようにします。</span><span class="sxs-lookup"><span data-stu-id="60cad-117">When you turn off the setting, you disable preview features and make them inaccessible to your users.</span></span> <span data-ttu-id="60cad-118">プレビュー機能は、Talent でサポートが制限されます。</span><span class="sxs-lookup"><span data-stu-id="60cad-118">Preview features have limited support in Talent.</span></span> <span data-ttu-id="60cad-119">プライバシーとセキュリティ対策の使用は少なく、Talent サービス レベル契約 (SLA) には含まれません。</span><span class="sxs-lookup"><span data-stu-id="60cad-119">They might use fewer privacy and security measures, and they aren't included in the Talent service level agreement (SLA).</span></span> <span data-ttu-id="60cad-120">個人のデータ (つまり、ユーザーを識別する任意の情報)、または法律上または規制順守要件の対象となるその他のデータを処理するプレビュー機能を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="60cad-120">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

### <a name="attract"></a><span data-ttu-id="60cad-121">Attract</span><span class="sxs-lookup"><span data-stu-id="60cad-121">Attract</span></span>

1. <span data-ttu-id="60cad-122">Microsoft Dynamics 365 Talent: Attract にサインインします。</span><span class="sxs-lookup"><span data-stu-id="60cad-122">Sign in to Microsoft Dynamics 365 Talent: Attract.</span></span>
2. <span data-ttu-id="60cad-123">右上隅の**設定**メニュー (ギヤ記号) で、**管理センター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="60cad-123">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span>
3. <span data-ttu-id="60cad-124">**機能管理**タブで**プレビュー機能**の横のオプションを選択すると、青色に変わり**オン**になります。</span><span class="sxs-lookup"><span data-stu-id="60cad-124">On the **Feature management** tab, select the option next to **Preview features** so that it turns blue and says **On**.</span></span>

    ![Attract のプレビュー機能の有効化](./media/attract-enable-preview-features.png)

4. <span data-ttu-id="60cad-126">個々のプレビュー機能の選択を選択または解除します。</span><span class="sxs-lookup"><span data-stu-id="60cad-126">Select or cancel the selection of individual preview features.</span></span> <span data-ttu-id="60cad-127">何もしない場合は、使用可能なプレビュー機能がすべて有効になります。</span><span class="sxs-lookup"><span data-stu-id="60cad-127">If you do nothing, all available preview features are enabled.</span></span>
5. <span data-ttu-id="60cad-128">新しい機能の表示を開始するブラウザーを更新します。</span><span class="sxs-lookup"><span data-stu-id="60cad-128">Refresh your browser to start to see the new features.</span></span> <span data-ttu-id="60cad-129">既にサイン インしているすべてのユーザーは、次にサイン インするときに機能を表示し、または機能をすぐに表示するためにそのブラウザーを更新することができます。</span><span class="sxs-lookup"><span data-stu-id="60cad-129">Any users who are already signed in will see the features the next time they sign in, or they can refresh their browser to see the features immediately.</span></span>

> [!NOTE]
> <span data-ttu-id="60cad-130">一部のプレビュー機能には、追加のコンフィギュレーションが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="60cad-130">Some preview features might require additional configuration.</span></span> <span data-ttu-id="60cad-131">プレビュー機能の横にあるリンクを使用して、設定を完了します。</span><span class="sxs-lookup"><span data-stu-id="60cad-131">Follow the links next to the preview feature to complete the setup for it.</span></span>

## <a name="feedback"></a><span data-ttu-id="60cad-132">フィードバック</span><span class="sxs-lookup"><span data-stu-id="60cad-132">Feedback</span></span>

<span data-ttu-id="60cad-133">これらのプレビュー機能の使用経験に関するご意見をお聞かせください。</span><span class="sxs-lookup"><span data-stu-id="60cad-133">We want to hear from you about your experience with any of these preview features.</span></span> <span data-ttu-id="60cad-134">その他の機能を使用する際に、以下のサイトにて、フィードバックを定期的に転記することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="60cad-134">We encourage you to regularly post your feedback on the following sites as you use these or any other features:</span></span>

- <span data-ttu-id="60cad-135">[コミュニティ](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – このサイトは、ユーザーが使用ケースを説明したり、質問したり、およびコミュニティ ヘルプを得られる優れたリソースです。</span><span class="sxs-lookup"><span data-stu-id="60cad-135">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="60cad-136">製品に必要な機能、または既存の機能に対して行われるべき変更についてお知らせください。</span><span class="sxs-lookup"><span data-stu-id="60cad-136">Let us know about features that you want to see in the product, or let us know about any changes you think we should make to existing features.</span></span> <span data-ttu-id="60cad-137">以下のサイトにて、製品アイデアを提案してください。</span><span class="sxs-lookup"><span data-stu-id="60cad-137">Suggest product ideas on the following sites:</span></span>

    - [<span data-ttu-id="60cad-138">Attract アイデア</span><span class="sxs-lookup"><span data-stu-id="60cad-138">Attract ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [<span data-ttu-id="60cad-139">Onboard アイデア</span><span class="sxs-lookup"><span data-stu-id="60cad-139">Onboard ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

<span data-ttu-id="60cad-140">フィードバックまたは製品のレビュー申請には個人データ (ユーザーを識別できる任意の情報) を含めないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="60cad-140">Make sure that you don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="60cad-141">収集した情報はさらに分析されることがありますが、該当するプライバシーに関する法律の下で要求に回答するためには使用されません。</span><span class="sxs-lookup"><span data-stu-id="60cad-141">Collected information might be analyzed further and isn't used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="60cad-142">これらのプログラムで個別に収集された個人データは、[Microsoft のプライバシーに関する声明](https://privacy.microsoft.com/privacystatement) の対象となります。</span><span class="sxs-lookup"><span data-stu-id="60cad-142">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span>

> [!TIP]
> <span data-ttu-id="60cad-143">リリースに際して新しいプレビュー機能に関して最新の状態を保つため、このトピックをブックマークし、頻繁に確認してください。</span><span class="sxs-lookup"><span data-stu-id="60cad-143">Bookmark this topic, and check back often to stay up to date about new preview features as we release them.</span></span>

## <a name="see-also"></a><span data-ttu-id="60cad-144">参照</span><span class="sxs-lookup"><span data-stu-id="60cad-144">See also</span></span>

- [<span data-ttu-id="60cad-145">Talent アプリの試みまたは購入</span><span class="sxs-lookup"><span data-stu-id="60cad-145">Try or buy Talent apps</span></span>](https://dynamics.microsoft.com/talent/overview/)
- [<span data-ttu-id="60cad-146">Dynamics 365 Talent の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="60cad-146">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="60cad-147">リリース計画</span><span class="sxs-lookup"><span data-stu-id="60cad-147">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="60cad-148">Microsoft Dynamics 365 Talent に関するサポートの利用</span><span class="sxs-lookup"><span data-stu-id="60cad-148">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
