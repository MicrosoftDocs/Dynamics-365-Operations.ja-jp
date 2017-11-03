---
title: "組織管理ホーム ページ"
description: "このトピックでは、組織での Microsoft Dynamics 365 for Finance and Operations, Enterprise edition の使用に役立つリソースを示します。"
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f1cff2388b02ff6dfd52a39b7f3ea90f10807096
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="organization-administration-home-page"></a><span data-ttu-id="33ba9-103">組織管理ホーム ページ</span><span class="sxs-lookup"><span data-stu-id="33ba9-103">Organization administration home page</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="33ba9-104">このトピックでは、Power Users および Administrators が Microsoft Dynamics 365 for Finance and Operations, Enterprise edition をコンフィギュレーションするのに役立つコンテンツを示します。</span><span class="sxs-lookup"><span data-stu-id="33ba9-104">This topic points to content that will help power users and administrators configure Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="33ba9-105">このコンテンツは、組織と業務を円滑かつ効率的に操作するようシステムをコンフィギュレーションするのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="33ba9-105">This content will help them configure the system to work smoothly and effectively for your organization and business.</span></span>

<span data-ttu-id="33ba9-106">ここに表示されるコンテンツの多くは、[**組織管理**] モジュールでの機能に適用されます。</span><span class="sxs-lookup"><span data-stu-id="33ba9-106">Much of the content listed here applies to features in the **Organizational administration** module.</span></span> <span data-ttu-id="33ba9-107">ただし、レコード テンプレートを作成および使用するなどの、組織をより効率的に実行するのに役立つ任意のモジュールで実行できる、いくつかのタスクがあります。</span><span class="sxs-lookup"><span data-stu-id="33ba9-107">However, there are a couple of tasks, such as creating and using a record template, that can be performed in any module to help your organization run more efficiently.</span></span> 

<a name="number-sequences"></a><span data-ttu-id="33ba9-108">番号順序</span><span class="sxs-lookup"><span data-stu-id="33ba9-108">Number sequences</span></span>
----------------
<span data-ttu-id="33ba9-109">番号順序は、ID が必要なマスター データ レコードおよびトランザクション レコードに対して読みやすい固有の ID を生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="33ba9-109">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="33ba9-110">ID が必要なマスタ データ レコードまたはトランザクション レコードは、*参照*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="33ba9-110">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span> <span data-ttu-id="33ba9-111">参照先に新しいレコードを作成するには、事前に番号順序を設定して参照先に関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="33ba9-111">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span>

-   [<span data-ttu-id="33ba9-112">番号順序の概要</span><span class="sxs-lookup"><span data-stu-id="33ba9-112">Number sequence overview</span></span>](number-sequence-overview.md)
-   <span data-ttu-id="33ba9-113">[ウィザードを使用した番号順序の設定](tasks/set-up-number-sequences-wizard.md) (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="33ba9-113">[Set up number sequences by using a wizard](tasks/set-up-number-sequences-wizard.md) (Task guide)</span></span>
-   <span data-ttu-id="33ba9-114">[番号順序を個別に設定する](tasks/set-up-number-sequences-individual-basis.md) (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="33ba9-114">[Set up number sequences on an individual basis](tasks/set-up-number-sequences-individual-basis.md) (Task guide)</span></span>

## <a name="organizations"></a><span data-ttu-id="33ba9-115">組織</span><span class="sxs-lookup"><span data-stu-id="33ba9-115">Organizations</span></span>
<span data-ttu-id="33ba9-116">組織とは、業務プロセスを実行や目標の達成を協力して行う人々の集まりです。</span><span class="sxs-lookup"><span data-stu-id="33ba9-116">An organization is a group of people who are working together to carry out a business process or achieve a goal.</span></span> <span data-ttu-id="33ba9-117">組織階層とは、業務を構成する組織の関係を表すものです。</span><span class="sxs-lookup"><span data-stu-id="33ba9-117">Organizational hierarchies represent the relationships between the organizations that make up your business.</span></span>

<span data-ttu-id="33ba9-118">Finance and Operations で組織と組織階層を設定する前に、組織をシミュレーションする方法を確認してください。</span><span class="sxs-lookup"><span data-stu-id="33ba9-118">Before you set up organizations and organization hierarchies in Finance and Operations, make sure that you plan how your business will be modeled.</span></span> <span data-ttu-id="33ba9-119">組織モデルは、Finance and Operations の実装と業務プロセスに重要な影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="33ba9-119">The organization model has a significant effect on the implementation of Finance and Operations and on business processes.</span></span>

-   [<span data-ttu-id="33ba9-120">組織と組織階層</span><span class="sxs-lookup"><span data-stu-id="33ba9-120">Organizations and organizational hierarchies</span></span>](organizations-organizational-hierarchies.md)
-   [<span data-ttu-id="33ba9-121">組織階層の計画</span><span class="sxs-lookup"><span data-stu-id="33ba9-121">Plan your organizational hierarchy</span></span>](plan-organizational-hierarchy.md)
-   <span data-ttu-id="33ba9-122">[組織階層の作成](tasks/create-organization-hierarchy.md) (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="33ba9-122">[Create an organization hierarchy](tasks/create-organization-hierarchy.md) (Task guide)</span></span>
-   <span data-ttu-id="33ba9-123">[法人の作成](tasks/create-legal-entity.md) (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="33ba9-123">[Create a legal entity](tasks/create-legal-entity.md) (Task guide)</span></span>
-   <span data-ttu-id="33ba9-124">[作業単位の作成](tasks/create-operating-unit.md) (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="33ba9-124">[Create an operating unit](tasks/create-operating-unit.md) (Task guide)</span></span>

## <a name="address-books"></a><span data-ttu-id="33ba9-125">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="33ba9-125">Address books</span></span>
<span data-ttu-id="33ba9-126">グローバル アドレス帳は、連携する会社のすべての内部および外部担当者と組織が格納されている必要があるマスター データに対する中央リポジトリです。</span><span class="sxs-lookup"><span data-stu-id="33ba9-126">The global address book is a centralized repository for master data that must be stored for all internal and external persons and organizations that the company interacts with.</span></span> <span data-ttu-id="33ba9-127">関係者レコードに関連付けられているデータには、関係者の名前、住所、および連絡先情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="33ba9-127">The data that is associated with party records includes the party's name, address, and contact information.</span></span> 

<span data-ttu-id="33ba9-128">グローバル アドレス帳を作成すると、必要に応じて組織の各会社別または事業品目別のアドレス帳など追加のアドレス帳を作成できます。</span><span class="sxs-lookup"><span data-stu-id="33ba9-128">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> 

-   [<span data-ttu-id="33ba9-129">グローバル アドレス帳</span><span class="sxs-lookup"><span data-stu-id="33ba9-129">Global address book</span></span>](overview-global-address-book.md)
-   [<span data-ttu-id="33ba9-130">グローバル アドレス帳および追加のアドレス帳の構成方法を計画する</span><span class="sxs-lookup"><span data-stu-id="33ba9-130">Plan how to configure the global address book and additional address books</span></span>](plan-configuration-global-address-book-additional-address-books.md)
- [<span data-ttu-id="33ba9-131">グローバル アドレス帳を構成する</span><span class="sxs-lookup"><span data-stu-id="33ba9-131">Configure the global address book</span></span>](tasks/configure-global-address-book.md)
-   [<span data-ttu-id="33ba9-132">アドレス帳のよくある質問</span><span class="sxs-lookup"><span data-stu-id="33ba9-132">Address books FAQ</span></span>](qa-address-books.md)


## <a name="workflow"></a><span data-ttu-id="33ba9-133">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="33ba9-133">Workflow</span></span>
<span data-ttu-id="33ba9-134">ワークフローは、Finance and Operations のインストール時にインストールされるシステムで、個々のワークフローまたはビジネス プロセスを作成するのに使用できます。</span><span class="sxs-lookup"><span data-stu-id="33ba9-134">Workflow is a system that is installed with Finance and Operations that you can use to create individual workflows, or business processes.</span></span> <span data-ttu-id="33ba9-135">ワークフローを作成する場合、タスクを完了し、決定を下し、ドキュメントを承認するユーザーを示すことによって、システムにおけるドキュメントの流れ (移動) を指定します。</span><span class="sxs-lookup"><span data-stu-id="33ba9-135">When you create a workflow, you specify how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> 

-   [<span data-ttu-id="33ba9-136">ワークフローの概要</span><span class="sxs-lookup"><span data-stu-id="33ba9-136">Workflow overview</span></span>](overview-workflow-system.md)
-   [<span data-ttu-id="33ba9-137">ワークフロー要素</span><span class="sxs-lookup"><span data-stu-id="33ba9-137">Workflow elements</span></span>](workflow-elements.md)
-   [<span data-ttu-id="33ba9-138">ワークフロー アクション</span><span class="sxs-lookup"><span data-stu-id="33ba9-138">Workflow actions</span></span>](workflow-actions.md)
-   [<span data-ttu-id="33ba9-139">ワークフローの作成</span><span class="sxs-lookup"><span data-stu-id="33ba9-139">Create a workflow</span></span>](create-workflow.md)

## <a name="electronic-signatures"></a><span data-ttu-id="33ba9-140">電子署名</span><span class="sxs-lookup"><span data-stu-id="33ba9-140">Electronic signatures</span></span>
<span data-ttu-id="33ba9-141">電子署名は、コンピューティング プロセスの開始者または承認者を確認するための ID です。</span><span class="sxs-lookup"><span data-stu-id="33ba9-141">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="33ba9-142">一部の業界では、電子署名は手書きの署名と同じだけの法的拘束力があります。</span><span class="sxs-lookup"><span data-stu-id="33ba9-142">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span> <span data-ttu-id="33ba9-143">製薬、飲食料品、航空防衛などの規制対象業界では、規制準拠要件として電子署名が義務付けられています。</span><span class="sxs-lookup"><span data-stu-id="33ba9-143">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span>

<span data-ttu-id="33ba9-144">Finance and Operations では、重要なビジネス プロセスに電子署名を使用できます。</span><span class="sxs-lookup"><span data-stu-id="33ba9-144">In Finance and Operations, you can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="33ba9-145">組み込みの電子署名機能を持つプロセスもあります。</span><span class="sxs-lookup"><span data-stu-id="33ba9-145">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="33ba9-146">任意のデータベース テーブルおよびフィールド用にカスタム署名要求を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="33ba9-146">You can also create custom signature requirements for any database table and field.</span></span>

-   [<span data-ttu-id="33ba9-147">電子署名の概要</span><span class="sxs-lookup"><span data-stu-id="33ba9-147">Electronic signature overview</span></span>](electronic-signature-overview.md)
-   <span data-ttu-id="33ba9-148">[電子署名の設定](tasks/set-up-electronic-signatures.md) (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="33ba9-148">[Set up electronic signatures](tasks/set-up-electronic-signatures.md) (Task guide)</span></span>

## <a name="case-management"></a><span data-ttu-id="33ba9-149">ケース管理</span><span class="sxs-lookup"><span data-stu-id="33ba9-149">Case management</span></span>
<span data-ttu-id="33ba9-150">ケースの計画、追跡、および分析を行うことで、同様の問題に使用できる効率的な解決策を作成できます。</span><span class="sxs-lookup"><span data-stu-id="33ba9-150">By planning, tracking, and analyzing cases, you can develop efficient resolutions that can be used for similar issues.</span></span> <span data-ttu-id="33ba9-151">たとえば、顧客サービス担当者または一般人事担当者がケースを作成することで、より効率的なケースを対処したり解決するのに役立つ情報をナレッジ記事で検索できるようになります。</span><span class="sxs-lookup"><span data-stu-id="33ba9-151">For example, when customer service representatives or Human Resources generalists create cases, they can find information in knowledge articles to help them work with or resolve a case more efficiently.</span></span> 

-   [<span data-ttu-id="33ba9-152">ケース管理の概要</span><span class="sxs-lookup"><span data-stu-id="33ba9-152">Case management overview</span></span>](cases.md)
-   [<span data-ttu-id="33ba9-153">ケース セキュリティ、プロセス、およびカテゴリのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="33ba9-153">Configure case security, processes, and categories</span></span>](plan-case-management.md)

## <a name="record-templates"></a><span data-ttu-id="33ba9-154">レコード テンプレート</span><span class="sxs-lookup"><span data-stu-id="33ba9-154">Record templates</span></span>
<span data-ttu-id="33ba9-155">レコード テンプレートでは、レコードをもっと迅速に作成することができます。</span><span class="sxs-lookup"><span data-stu-id="33ba9-155">Record templates can help you to create records more quickly.</span></span> <span data-ttu-id="33ba9-156">よく使用されるフィールド値を新しいレコードごとに明示的に入力する必要をなくなるようにする、レコード テンプレートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="33ba9-156">You can create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> 

-   [<span data-ttu-id="33ba9-157">レコード テンプレート</span><span class="sxs-lookup"><span data-stu-id="33ba9-157">Record templates</span></span>](record-templates.md)
- <span data-ttu-id="33ba9-158">[データ入力を容易にするレコード テンプレートの作成](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="33ba9-158">[Create a record template to facilitate data entry](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Task guide)</span></span>
- <span data-ttu-id="33ba9-159">[レコード テンプレートを使用した新しいレコードの作成](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="33ba9-159">[Use a record template to create a new record](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Task guide)</span></span>

## <a name="general-organization-administration"></a><span data-ttu-id="33ba9-160">一般的な組織管理</span><span class="sxs-lookup"><span data-stu-id="33ba9-160">General organization administration</span></span>
-   <span data-ttu-id="33ba9-161">[バナーまたはロゴの変更](../get-started/tasks/change-banner-or-logo.md) (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="33ba9-161">[Change the banner or logo](../get-started/tasks/change-banner-or-logo.md) (Task guide)</span></span>
- [<span data-ttu-id="33ba9-162">ドキュメント管理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="33ba9-162">Configure document management</span></span>](configure-document-management.md)
- [<span data-ttu-id="33ba9-163">電子メールのコンフィギュレーションと送信</span><span class="sxs-lookup"><span data-stu-id="33ba9-163">Configure and send email</span></span>](configure-email.md)
-   [<span data-ttu-id="33ba9-164">日時データとタイム ゾーン</span><span class="sxs-lookup"><span data-stu-id="33ba9-164">Date/time data and time zones</span></span>](date-time-zones.md)








