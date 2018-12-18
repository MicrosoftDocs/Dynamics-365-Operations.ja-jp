---
title: "組織と組織階層"
description: "組織とは、業務プロセスを実行や目標の達成を協力して行う人々の集まりです。 組織階層とは、業務を構成する組織の関係を表すものです。"
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: OMHierarchyManager, OMOperatingUnit,
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17291
ms.assetid: 76b7ca45-93d4-45cc-b191-66ee63afa1fd
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 72834769e393382ac511ad3af21544efddb049d3
ms.contentlocale: ja-jp
ms.lasthandoff: 12/18/2018

---

# <a name="organizations-and-organizational-hierarchies"></a><span data-ttu-id="d2f40-104">組織と組織階層</span><span class="sxs-lookup"><span data-stu-id="d2f40-104">Organizations and organizational hierarchies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2f40-105">組織とは、業務プロセスを実行や目標の達成を協力して行う人々の集まりです。</span><span class="sxs-lookup"><span data-stu-id="d2f40-105">An organization is a group of people who are working together to carry out a business process or achieve a goal.</span></span> <span data-ttu-id="d2f40-106">組織階層とは、業務を構成する組織の関係を表すものです。</span><span class="sxs-lookup"><span data-stu-id="d2f40-106">Organizational hierarchies represent the relationships between the organizations that make up your business.</span></span>

## <a name="organizations"></a><span data-ttu-id="d2f40-107">組織</span><span class="sxs-lookup"><span data-stu-id="d2f40-107">Organizations</span></span>

<span data-ttu-id="d2f40-108">Microsoft Dynamics 365 for Finance and Operations では、法人、作業単位、およびチームという内部組織のタイプを定義できます。</span><span class="sxs-lookup"><span data-stu-id="d2f40-108">In Microsoft Dynamics 365 for Finance and Operations, you can define the following types of internal organizations: legal entities, operating units, and teams.</span></span>

<span data-ttu-id="d2f40-109">すべての内部組織は [**関係者**] エンティティ タイプです。</span><span class="sxs-lookup"><span data-stu-id="d2f40-109">All internal organizations are types of the **Party** entity.</span></span> <span data-ttu-id="d2f40-110">したがって、これらの組織は、住所と連絡先情報を保存するためにアドレス帳機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="d2f40-110">Therefore, these organizations use the address book to store address and contact information.</span></span> <span data-ttu-id="d2f40-111">当時者は、個人または組織のいずれかであり、1 つ以上のアドレス帳に含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d2f40-111">A party, which can be either a person or an organization, can belong to one or more address books.</span></span>

### <a name="legal-entities"></a><span data-ttu-id="d2f40-112">法人</span><span class="sxs-lookup"><span data-stu-id="d2f40-112">Legal entities</span></span>

<span data-ttu-id="d2f40-113">法人とは、登記または法的手続きを済ませた法律上の構造を持つ組織です。</span><span class="sxs-lookup"><span data-stu-id="d2f40-113">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="d2f40-114">法人には、法的契約の締結が認められており、業績を報告する収支報告書の作成が義務付けられています。</span><span class="sxs-lookup"><span data-stu-id="d2f40-114">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="d2f40-115">会社とは、法人の 1 つのタイプです。</span><span class="sxs-lookup"><span data-stu-id="d2f40-115">A company is a type of legal entity.</span></span> <span data-ttu-id="d2f40-116">Microsoft Dynamics 365 for Finance and Operations の今回のリリースでは、会社はユーザーが作成できる唯一の法人であり、個々の法人は会社 ID と関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="d2f40-116">In this release of Microsoft Dynamics 365 for Finance and Operations, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="d2f40-117">この関連付けは、プログラム内の一部の機能エリアで法人 ID (データモデルでは DataAreaId) が使用されているために設けられています。</span><span class="sxs-lookup"><span data-stu-id="d2f40-117">This association exists because some functional areas in the program use a company ID, or DataAreaId, in their data models.</span></span> <span data-ttu-id="d2f40-118">これらの機能エリアでは、データのセキュリティ区分として法人が使用されています。</span><span class="sxs-lookup"><span data-stu-id="d2f40-118">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="d2f40-119">ユーザーは、現在ログオン中の会社のデータにのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d2f40-119">Users can access data only for the company that they are currently logged on to.</span></span>

### <a name="operating-units"></a><span data-ttu-id="d2f40-120">作業単位</span><span class="sxs-lookup"><span data-stu-id="d2f40-120">Operating units</span></span>

<span data-ttu-id="d2f40-121">作業単位とは、事業における経済資源と運営プロセスの管理を振り分ける際に使用する組織です。</span><span class="sxs-lookup"><span data-stu-id="d2f40-121">An operating unit is an organization that is used to divide the control of economic resources and operational processes in a business.</span></span> <span data-ttu-id="d2f40-122">作業単位のメンバは、希少なリソースの有効活用、プロセスの改善、および業績に対する責任を担っています。</span><span class="sxs-lookup"><span data-stu-id="d2f40-122">People in an operating unit have a duty to maximize the use of scarce resources, improve processes, and account for their performance.</span></span>

<span data-ttu-id="d2f40-123">Microsoft Dynamics 365 for Finance and Operations では、作業単位には、コスト センター、事業単位、バリュー ストリーム、部門、小売チャネルなどのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="d2f40-123">In Microsoft Dynamics 365 for Finance and Operations, the types of operating units include cost centers, business units, value streams, departments, and retail channels.</span></span> <span data-ttu-id="d2f40-124">次の表に、作業単位の各タイプに関する詳細情報を示します。</span><span class="sxs-lookup"><span data-stu-id="d2f40-124">The following table provides more information about each type of operating unit.</span></span>

| <span data-ttu-id="d2f40-125">作業単位のタイプ</span><span class="sxs-lookup"><span data-stu-id="d2f40-125">Operating unit type</span></span> | <span data-ttu-id="d2f40-126">説明</span><span class="sxs-lookup"><span data-stu-id="d2f40-126">Description</span></span> | <span data-ttu-id="d2f40-127">目的</span><span class="sxs-lookup"><span data-stu-id="d2f40-127">Purpose</span></span> |
|---------------------|-------------|---------|
| <span data-ttu-id="d2f40-128">原価部門</span><span class="sxs-lookup"><span data-stu-id="d2f40-128">Cost center</span></span>         | <span data-ttu-id="d2f40-129">予算経費と実績経費の責任をその管理者が負う作業単位。</span><span class="sxs-lookup"><span data-stu-id="d2f40-129">An operating unit in which managers are accountable for budgeted and actual expenditures.</span></span> | <span data-ttu-id="d2f40-130">法人間にまたがる業務プロセスの管理と運用管理に使用します。</span><span class="sxs-lookup"><span data-stu-id="d2f40-130">Used for the management and operational control of business processes that span legal entities.</span></span> |
| <span data-ttu-id="d2f40-131">事業単位</span><span class="sxs-lookup"><span data-stu-id="d2f40-131">Business unit</span></span>       | <span data-ttu-id="d2f40-132">戦略的なビジネス目標達成のために作成された半自治の事業単位。</span><span class="sxs-lookup"><span data-stu-id="d2f40-132">A semi-autonomous operating unit that is created to meet strategic business objectives.</span></span> | <span data-ttu-id="d2f40-133">法人とは別に、組織が係わる業界または製品ラインに基づいた財務報告に使用します。</span><span class="sxs-lookup"><span data-stu-id="d2f40-133">Used for financial reporting that is based on industries or product lines that the organization serves independently of legal entities.</span></span> |
| <span data-ttu-id="d2f40-134">バリュー ストリーム</span><span class="sxs-lookup"><span data-stu-id="d2f40-134">Value stream</span></span>        | <span data-ttu-id="d2f40-135">一つ以上の生産フローを制御する作業単位。</span><span class="sxs-lookup"><span data-stu-id="d2f40-135">An operating unit that controls one or more production flows.</span></span> | <span data-ttu-id="d2f40-136">消費者に製品やサービスを提供するために必要な活動およびフローを管理するリーン生産に一般的に使用します。</span><span class="sxs-lookup"><span data-stu-id="d2f40-136">Commonly used in lean manufacturing to control the activities and flows that are required to supply a product or service to consumers.</span></span> |
| <span data-ttu-id="d2f40-137">部門</span><span class="sxs-lookup"><span data-stu-id="d2f40-137">Department</span></span>          | <span data-ttu-id="d2f40-138">販売や会計など、特定のタスクを実行する組織のカテゴリまたは機能パーツを表す作業単位。</span><span class="sxs-lookup"><span data-stu-id="d2f40-138">An operating unit that represents a category or functional part of an organization that performs a specific task, such as sales or accounting.</span></span> | <span data-ttu-id="d2f40-139">機能分野の報告に使用します。</span><span class="sxs-lookup"><span data-stu-id="d2f40-139">Used to report on functional areas.</span></span> <span data-ttu-id="d2f40-140">部門は損益の職責を担っており、複数のコスト センターで構成される場合があります。</span><span class="sxs-lookup"><span data-stu-id="d2f40-140">A department may have profit and loss responsibility, and may consist of a group of cost centers.</span></span> |
| <span data-ttu-id="d2f40-141">小売チャンネル</span><span class="sxs-lookup"><span data-stu-id="d2f40-141">Retail channel</span></span>      | <span data-ttu-id="d2f40-142">従来型の店舗、オンライン ストア、またはオンライン マーケットプレースを表す作業単位。</span><span class="sxs-lookup"><span data-stu-id="d2f40-142">An operating unit that represents a brick and mortar store, an online store or an online marketplace.</span></span> | <span data-ttu-id="d2f40-143">法人内または法人全体の 1 つ以上の店舗の管理と運用管理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d2f40-143">Used for the management and operational control of one or more stores within or across legal entities.</span></span> |

### <a name="teams"></a><span data-ttu-id="d2f40-144">チーム</span><span class="sxs-lookup"><span data-stu-id="d2f40-144">Teams</span></span>

<span data-ttu-id="d2f40-145">メンバが共通の責任、関心、または目標を持つ組織。</span><span class="sxs-lookup"><span data-stu-id="d2f40-145">A team is an organization in which the members share a common responsibility, interest, or objective.</span></span> <span data-ttu-id="d2f40-146">チームは組織階層では使用できません。</span><span class="sxs-lookup"><span data-stu-id="d2f40-146">Teams cannot be used in organizational hierarchies.</span></span>

## <a name="organizational-hierarchies"></a><span data-ttu-id="d2f40-147">組織階層</span><span class="sxs-lookup"><span data-stu-id="d2f40-147">Organizational hierarchies</span></span>

<span data-ttu-id="d2f40-148">業務について、さまざまな観点から表示と報告を行う組織階層を設定します。</span><span class="sxs-lookup"><span data-stu-id="d2f40-148">Set up organizational hierarchies to view and report on your business from different perspectives.</span></span> <span data-ttu-id="d2f40-149">たとえば、税金、法律、または法令についての報告に使用するの法人の階層を設定できます。</span><span class="sxs-lookup"><span data-stu-id="d2f40-149">For example, you can set up a hierarchy of legal entities for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="d2f40-150">法的に必須でなくても内部統制に使用する財務情報を報告する階層を、作業単位に基づいて設定します。</span><span class="sxs-lookup"><span data-stu-id="d2f40-150">Set up a hierarchy that is based on operating units to report financial information that is not legally required, but that is used for internal control.</span></span> <span data-ttu-id="d2f40-151">たとえば、購買ポリシー、ルール、および業務プロセスを管理する購買階層を作成できます。</span><span class="sxs-lookup"><span data-stu-id="d2f40-151">For example, you can create a purchasing hierarchy to control purchasing policies, rules, and business processes.</span></span>

<span data-ttu-id="d2f40-152">Microsoft Dynamics 365 for Finance and Operations では各階層の目的が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="d2f40-152">Each hierarchy is assigned a purpose in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="d2f40-153">階層の目的により、階層に含めることができる組織のタイプが決まります。</span><span class="sxs-lookup"><span data-stu-id="d2f40-153">The purpose of a hierarchy determines the types of organizations that can be included in the hierarchy.</span></span> <span data-ttu-id="d2f40-154">この目的により、どのアプリケーションのシナリオで階層を使用できるかが決まります。</span><span class="sxs-lookup"><span data-stu-id="d2f40-154">The purpose also determines which application scenarios a hierarchy can be used in.</span></span>

<span data-ttu-id="d2f40-155">各階層の組織では、パラメータ、ポリシー、およびトランザクションを共有できます。</span><span class="sxs-lookup"><span data-stu-id="d2f40-155">Organizations in a hierarchy can share parameters, policies, and transactions.</span></span> <span data-ttu-id="d2f40-156">親組織のパラメータは、各組織で継承または上書きできます。</span><span class="sxs-lookup"><span data-stu-id="d2f40-156">An organization can inherit or override the parameters of its parent organization.</span></span> <span data-ttu-id="d2f40-157">ただし、製品やアドレス帳などの共有マスタ データは組織全体に適用され、個々の組織では上書きすることはできません。</span><span class="sxs-lookup"><span data-stu-id="d2f40-157">However, shared master data, such as products and address books, applies to the whole organization and cannot be overridden for individual organizations.</span></span> <span data-ttu-id="d2f40-158">組織と階層の作成は慎重に計画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2f40-158">Creating organizations and hierarchies requires careful planning.</span></span> <span data-ttu-id="d2f40-159">詳細については、「[組織階層の計画](plan-organizational-hierarchy.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2f40-159">For more information, see [Plan the organizational hierarchy](plan-organizational-hierarchy.md).</span></span>

