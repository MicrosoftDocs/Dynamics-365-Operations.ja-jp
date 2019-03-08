---
title: 電子署名
description: この記事では、電子署名の概要と Microsoft Dynamics 365 for Finance and Operations での使用方法を説明します。
author: maertenm
manager: AnnBe
ms.date: 08/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 676510ef503d51d914ba762e7ac15e2c4811c6ba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "325667"
---
# <a name="electronic-signatures"></a><span data-ttu-id="abecb-103">電子署名</span><span class="sxs-lookup"><span data-stu-id="abecb-103">Electronic signatures</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="abecb-104">この記事では、電子署名の概要と Microsoft Dynamics 365 for Finance and Operations での使用方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="abecb-104">This article provides an overview of electronic signatures and describes how they can be used in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="what-is-an-electronic-signature"></a><span data-ttu-id="abecb-105">電子署名とは</span><span class="sxs-lookup"><span data-stu-id="abecb-105">What is an electronic signature?</span></span>

<span data-ttu-id="abecb-106">電子署名は、コンピューティング プロセスの開始者または承認者を確認するための ID です。</span><span class="sxs-lookup"><span data-stu-id="abecb-106">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="abecb-107">一部の業界では、電子署名は手書きの署名と同じだけの法的拘束力があります。</span><span class="sxs-lookup"><span data-stu-id="abecb-107">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span>

<span data-ttu-id="abecb-108">製薬、飲食料品、航空防衛などの規制対象業界では、規制準拠要件として電子署名が義務付けられています。</span><span class="sxs-lookup"><span data-stu-id="abecb-108">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span> <span data-ttu-id="abecb-109">また、米国の食品医薬品局 (FDA) の規制である CFR 第 21 章第 11 部に準拠するためにも必要です。</span><span class="sxs-lookup"><span data-stu-id="abecb-109">They are also required for compliance with regulations in 21 CFR Part 11 that was issued by the Food and Drug Administration (FDA) in the United States.</span></span>

> [!NOTE]
> <span data-ttu-id="abecb-110">電子署名自体は、デジタル署名と同一ではありません。</span><span class="sxs-lookup"><span data-stu-id="abecb-110">An electronic signature by itself isn't the same as a digital signature.</span></span> <span data-ttu-id="abecb-111">電子署名は単純に手書きの署名の代わりであり、一方、デジタル署名には追加のセキュリティ対策が用意されています。</span><span class="sxs-lookup"><span data-stu-id="abecb-111">An electronic signature is just a substitute for a handwritten signature, whereas a digital signature provides additional security measures.</span></span> <span data-ttu-id="abecb-112">デジタル署名は、他のユーザーまたはプロセスによってデータが改ざんされていないことを確認するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="abecb-112">A digital signature can help identify whether another user or process has tampered with the data.</span></span> <span data-ttu-id="abecb-113">また、デジタル署名は検証することができ、データに署名するために使用された証明書の所有者が、この検証に異議を唱えることはできません。</span><span class="sxs-lookup"><span data-stu-id="abecb-113">A digital signature can also be verified, and this verification can't be refuted by the owner of the certificate that was used to sign the data.</span></span> <span data-ttu-id="abecb-114">以下に説明するように、Microsoft Dynamics 365 for Finance and Operations の電子署名には組み込みのデジタル署名機能があります。</span><span class="sxs-lookup"><span data-stu-id="abecb-114">As described below, electronic signatures in Microsoft Dynamics 365 for Finance and Operations have built-in digital signature functionality.</span></span>

## <a name="electronic-signatures-in-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="abecb-115">Dynamics 365 for Finance and Operations の電子署名</span><span class="sxs-lookup"><span data-stu-id="abecb-115">Electronic signatures in Dynamics 365 for Finance and Operations</span></span>

<span data-ttu-id="abecb-116">Finance and Operations では、重要なビジネス プロセスに電子署名を使用できます。</span><span class="sxs-lookup"><span data-stu-id="abecb-116">In Finance and Operations, you can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="abecb-117">組み込みの電子署名機能を持つプロセスもあります。</span><span class="sxs-lookup"><span data-stu-id="abecb-117">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="abecb-118">任意のデータベース テーブルおよびフィールド用にカスタム署名要求を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="abecb-118">You can also create custom signature requirements for any database table and field.</span></span>

<span data-ttu-id="abecb-119">電子署名には組み込みのデジタル署名機能があります。</span><span class="sxs-lookup"><span data-stu-id="abecb-119">Electronic signatures have built-in digital signature functionality.</span></span> <span data-ttu-id="abecb-120">ドキュメントに署名する各ユーザーは、有効な暗号証明書を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="abecb-120">Every user who signs documents must obtain a valid cryptographic certificate.</span></span> <span data-ttu-id="abecb-121">ドキュメントに署名するときに、その証明書に関連付けられたプライベート キーが検証されます。</span><span class="sxs-lookup"><span data-stu-id="abecb-121">When a document is signed, the private key that is associated with that certificate is validated.</span></span> <span data-ttu-id="abecb-122">Finance and Operations は、監査証跡を提供するために電子署名の情報をログに記録します。</span><span class="sxs-lookup"><span data-stu-id="abecb-122">Finance and Operations records electronic signature information in a log to provide an audit trail.</span></span> <span data-ttu-id="abecb-123">電子署名を設定するには、「[電子署名の設定 (タスク ガイド)](tasks/set-up-electronic-signatures.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="abecb-123">To set up electronic signatures, see [Set up electronic signatures (Task guide)](tasks/set-up-electronic-signatures.md).</span></span>

## <a name="users-who-require-access-to-electronic-signatures"></a><span data-ttu-id="abecb-124">電子署名へのアクセスを必要とするユーザー</span><span class="sxs-lookup"><span data-stu-id="abecb-124">Users who require access to electronic signatures</span></span>

<span data-ttu-id="abecb-125">通常、3 種類のユーザーが、電子署名に対するセキュリティ アクセス権を必要としています。こららのユーザーとは、電子署名の管理者、署名者、電子署名の監査担当者です。</span><span class="sxs-lookup"><span data-stu-id="abecb-125">Three kinds of users typically require security access to electronic signatures: electronic signature administrators, signers, and electronic signature auditors.</span></span>

### <a name="electronic-signature-administrator"></a><span data-ttu-id="abecb-126">電子署名の管理者</span><span class="sxs-lookup"><span data-stu-id="abecb-126">Electronic signature administrator</span></span>

<span data-ttu-id="abecb-127">電子署名の管理者は、署名要求、一般パラメータ、および承認者を設定し、署名を検証できないときに警告を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="abecb-127">The electronic signature administrator sets up signature requirements, general parameters, and approvers, and receives alerts when signatures can't be verified.</span></span> <span data-ttu-id="abecb-128">既定では、**情報技術マネージャー** セキュリティ ロールに属するユーザーが、電子署名を管理するためのアクセス許可を所有しています。</span><span class="sxs-lookup"><span data-stu-id="abecb-128">By default, a user who belongs to the **Information technology manager** security role has permission to administer electronic signatures.</span></span>

### <a name="signer"></a><span data-ttu-id="abecb-129">署名者</span><span class="sxs-lookup"><span data-stu-id="abecb-129">Signer</span></span>

<span data-ttu-id="abecb-130">署名者は、署名が要求されているドキュメントおよびプロセスに電子署名を行います。</span><span class="sxs-lookup"><span data-stu-id="abecb-130">A signer provides electronic signatures for documents and processes that require signatures.</span></span> <span data-ttu-id="abecb-131">既定では、**システム ユーザー** セキュリティ ロールに属するユーザーは、ドキュメントに電子署名を行うためのアクセス許可を所有しています。</span><span class="sxs-lookup"><span data-stu-id="abecb-131">By default, a user who belongs to the **System user** security role has permission to sign documents electronically.</span></span>

> [!NOTE]
> <span data-ttu-id="abecb-132">署名者は、署名対象のドキュメントまたはプロセスの関連データにアクセスするために、追加のアクセス許可を必要とする場合があります。</span><span class="sxs-lookup"><span data-stu-id="abecb-132">The signer might require additional permissions before access is granted to data that is related to the document or process that is being signed.</span></span> <span data-ttu-id="abecb-133">データに変更を加え、変更に署名する必要があるユーザーは、データ変更のためのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="abecb-133">A user who changes data and must then sign for those changes must have permission to change the data.</span></span> <span data-ttu-id="abecb-134">別のユーザーの代わりに署名するユーザーは、データへのアクセスが必要ない場合があります。</span><span class="sxs-lookup"><span data-stu-id="abecb-134">A user who signs on behalf of another user might not require access to the data.</span></span> <span data-ttu-id="abecb-135">このタイプのユーザーの例は、従業員の変更に署名する監修者です。</span><span class="sxs-lookup"><span data-stu-id="abecb-135">An example of this kind of user is a supervisor who signs for an employee's changes.</span></span>

### <a name="electronic-signature-auditor"></a><span data-ttu-id="abecb-136">電子署名の監査担当者</span><span class="sxs-lookup"><span data-stu-id="abecb-136">Electronic signature auditor</span></span>

<span data-ttu-id="abecb-137">電子署名の監査担当者は、データベース ログおよびデータベース ログから表示できる署名の確認ログを確認します。</span><span class="sxs-lookup"><span data-stu-id="abecb-137">The electronic signature auditor reviews the database log and the signature review log that is available from the database log.</span></span> <span data-ttu-id="abecb-138">既定では、**情報技術マネージャー** セキュリティ ロールに属するユーザーが、電子署名を監査するためのアクセス許可を所有しています。</span><span class="sxs-lookup"><span data-stu-id="abecb-138">By default, a user who belongs to the **Information technology manager** security role has permission to audit electronic signatures.</span></span>

<span data-ttu-id="abecb-139">**情報技術マネージャー**以外のロールを使用する場合は、そのロールが次の権限に割り当てられていることを確認します:</span><span class="sxs-lookup"><span data-stu-id="abecb-139">If you use a role other than **Information technology manager**, make sure that the role is assigned the following privileges:</span></span>

- <span data-ttu-id="abecb-140">電子署名の失敗を表示</span><span class="sxs-lookup"><span data-stu-id="abecb-140">View electronic signature failures</span></span>
- <span data-ttu-id="abecb-141">データベース ログの表示</span><span class="sxs-lookup"><span data-stu-id="abecb-141">View database log</span></span>

## <a name="signing-documents-electronically"></a><span data-ttu-id="abecb-142">ドキュメントに電子的に署名する</span><span class="sxs-lookup"><span data-stu-id="abecb-142">Signing documents electronically</span></span>

### <a name="get-a-certificate"></a><span data-ttu-id="abecb-143">証明書の取得</span><span class="sxs-lookup"><span data-stu-id="abecb-143">Get a certificate</span></span>

<span data-ttu-id="abecb-144">Finance and Operations でドキュメントに電子署名を行うには、各署名者が証明書を事前に要求しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="abecb-144">Before you sign documents electronically in Finance and Operations, you must request a certificate.</span></span>

> [!NOTE]
> <span data-ttu-id="abecb-145">Finance and Operations は Microsoft SQL Server の機能を使用して証明書を作成し、電子署名を有効にします。</span><span class="sxs-lookup"><span data-stu-id="abecb-145">Finance and Operations uses Microsoft SQL Server features to create certificates and enable electronic signing.</span></span> <span data-ttu-id="abecb-146">追加の証明書または公開キー インフラストラクチャ (PKI) は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="abecb-146">No additional certificate or public key infrastructure (PKI) is required.</span></span>

<span data-ttu-id="abecb-147">証明書を要求すると、Finance and Operations データベースに公開キーとプライベート キーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="abecb-147">When you request a certificate, a public key and a private key are created for you in the Finance and Operations database.</span></span> <span data-ttu-id="abecb-148">プライベート キーは、ユーザーだけが知っているパスワードを使用して暗号化されます。</span><span class="sxs-lookup"><span data-stu-id="abecb-148">The private key is encrypted by using a password that is known only to you.</span></span> <span data-ttu-id="abecb-149">ドキュメントに電子署名を行う場合、パスワードを入力したときに ID が検証されます。</span><span class="sxs-lookup"><span data-stu-id="abecb-149">When you sign a document electronically, your identity is verified when you enter the password.</span></span>

<span data-ttu-id="abecb-150">証明書を要求するには、**オプション**ページの**アカウント**タブで**証明書の取得**をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="abecb-150">To request a certificate, on the **Options** page, on the **Accounts** tab, click **Get certificate**.</span></span>

<span data-ttu-id="abecb-151">署名に使用するパスワードを入力して確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="abecb-151">You must enter and confirm the password that you will use for signing.</span></span> <span data-ttu-id="abecb-152">パスワードは、プライベート キーを保護し、証明書の使用を承認するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="abecb-152">The password is used to protect your private key and authorize the use of your certificate.</span></span> <span data-ttu-id="abecb-153">このパスワードはデータベースに保存されず、Finance and Operations 管理者を含めて他のだれも使用できません。</span><span class="sxs-lookup"><span data-stu-id="abecb-153">This password isn't stored in the database, and it isn't available to anyone else, not even to the Finance and Operations administrator.</span></span>

<span data-ttu-id="abecb-154">証明書に関連付けられたパスワードを忘れた場合は、その証明書をリセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="abecb-154">If you forget the password that is connected with your certificate, that certificate must be reset.</span></span> <span data-ttu-id="abecb-155">証明書をリセットしても、リセット前の証明書を使用して署名したドキュメントに影響はありません。</span><span class="sxs-lookup"><span data-stu-id="abecb-155">If you reset the certificate, you don't affect documents that you signed by using the previous certificate.</span></span> <span data-ttu-id="abecb-156">証明書をリセットするには、**オプション**ページで**証明書のリセット**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="abecb-156">To reset the certificate, on the **Options** page, click **Reset certificate**.</span></span>

### <a name="sign-a-document-electronically"></a><span data-ttu-id="abecb-157">ドキュメントへの電子的な署名</span><span class="sxs-lookup"><span data-stu-id="abecb-157">Sign a document electronically</span></span>

<span data-ttu-id="abecb-158">電子署名が要求される変更を行うと、**ドキュメントに署名**ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="abecb-158">The **Sign document** page is displayed when you make a change that requires an electronic signature.</span></span>

1. <span data-ttu-id="abecb-159">**ドキュメントに署名**ページで**ドキュメント**タブをクリックし、ドキュメントに対する変更を確認します。</span><span class="sxs-lookup"><span data-stu-id="abecb-159">On the **Sign document** page, click the **Document** tab to review the changes to the document.</span></span>
2. <span data-ttu-id="abecb-160">**署名**タブで理由コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="abecb-160">On the **Signature** tab, select a reason code.</span></span>
3. <span data-ttu-id="abecb-161">コメントが必要な場合は、コメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="abecb-161">Enter a comment, if a comment is required.</span></span>
4. <span data-ttu-id="abecb-162">**署名者**フィールドにユーザー ID が表示されない場合は、一覧から選択します。</span><span class="sxs-lookup"><span data-stu-id="abecb-162">If your user ID doesn't appear in the **Signer** field, select it in the list.</span></span>
5. <span data-ttu-id="abecb-163">自分の場所が必要な場合は、その情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="abecb-163">Enter your location, if this information is required.</span></span>
6. <span data-ttu-id="abecb-164">**OK** をクリックします</span><span class="sxs-lookup"><span data-stu-id="abecb-164">Click **OK**.</span></span>

### <a name="sign-for-another-users-changes"></a><span data-ttu-id="abecb-165">別のユーザーによる変更への署名</span><span class="sxs-lookup"><span data-stu-id="abecb-165">Sign for another user's changes</span></span>

<span data-ttu-id="abecb-166">場合によっては、あるユーザーが行った変更に別のユーザーが署名するような場合があります。</span><span class="sxs-lookup"><span data-stu-id="abecb-166">Occasionally, you might want a user to sign for another user's changes.</span></span> <span data-ttu-id="abecb-167">たとえば、従業員が部品表 (BOM) に対して行った変更に監修者が署名することが求められる場合があります。</span><span class="sxs-lookup"><span data-stu-id="abecb-167">For example, a supervisor might be required to sign for changes that an employee makes to a bill of materials (BOM).</span></span> <span data-ttu-id="abecb-168">Finance and Operations ユーザーを別のユーザーに対して署名者として指定するには、この手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="abecb-168">Use this procedure to designate a Finance and Operations user as a signer for another user.</span></span>

> [!NOTE]
> <span data-ttu-id="abecb-169">別のユーザーの変更に署名する場合、変更を行ったユーザーのワークステーションで署名を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="abecb-169">When one user signs for another user's change, the signature must be provided at the workstation of the user who made the change.</span></span> <span data-ttu-id="abecb-170">署名が行われるまで、変更を行ったユーザーは変更を保存できません。</span><span class="sxs-lookup"><span data-stu-id="abecb-170">The user can't save the change until the signature has been provided.</span></span>

<span data-ttu-id="abecb-171">承認者を指定するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="abecb-171">To designate approvers, follow these steps.</span></span>

1. <span data-ttu-id="abecb-172">**オプション**ページの**アカウント**タブで**指定の承認者**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="abecb-172">On the **Options** page, on the **Accounts** tab, click **Designate approver**.</span></span>
2. <span data-ttu-id="abecb-173">**承認ユーザー ID** フィールドで、別のユーザーの変更に署名する必要があるユーザーの ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="abecb-173">In the **Approver user ID** field, select the ID of the user who must sign for another user's changes.</span></span>
3. <span data-ttu-id="abecb-174">**ユーザー ID に対する署名**フィールドで、変更に署名してもらう必要があるユーザーの ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="abecb-174">In the **Sign for user ID** field, select the ID of the user whose changes must be signed for.</span></span>
