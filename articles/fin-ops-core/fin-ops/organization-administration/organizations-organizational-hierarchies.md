---
title: 組織と組織階層の概要
description: 組織階層とは、業務を構成する組織の関係を表すものです。
author: sericks007
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMOperatingUnit,
audience: Application User
ms.reviewer: sericks
ms.custom: 17291
ms.assetid: 76b7ca45-93d4-45cc-b191-66ee63afa1fd
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efd34b01ab414b2282fd08d8d9329ae7f9a801ce
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747638"
---
# <a name="organizations-and-organizational-hierarchies-overview"></a><span data-ttu-id="7d245-103">組織と組織階層の概要</span><span class="sxs-lookup"><span data-stu-id="7d245-103">Organizations and organizational hierarchies overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d245-104">組織とは、業務プロセスを実行や目標の達成を協力して行う人々の集まりです。</span><span class="sxs-lookup"><span data-stu-id="7d245-104">An organization is a group of people who are working together to carry out a business process or achieve a goal.</span></span> <span data-ttu-id="7d245-105">組織階層とは、業務を構成する組織の関係を表すものです。</span><span class="sxs-lookup"><span data-stu-id="7d245-105">Organizational hierarchies represent the relationships between the organizations that make up your business.</span></span>

## <a name="organizations"></a><span data-ttu-id="7d245-106">組織</span><span class="sxs-lookup"><span data-stu-id="7d245-106">Organizations</span></span>

<span data-ttu-id="7d245-107">法人、作業単位、およびチームという内部組織のタイプを定義できます。</span><span class="sxs-lookup"><span data-stu-id="7d245-107">You can define the following types of internal organizations: legal entities, operating units, and teams.</span></span>

<span data-ttu-id="7d245-108">すべての内部組織は **関係者** エンティティ タイプです。</span><span class="sxs-lookup"><span data-stu-id="7d245-108">All internal organizations are types of the **Party** entity.</span></span> <span data-ttu-id="7d245-109">したがって、これらの組織は、住所と連絡先情報を保存するためにアドレス帳機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="7d245-109">Therefore, these organizations use the address book to store address and contact information.</span></span> <span data-ttu-id="7d245-110">当時者は、個人または組織のいずれかであり、1 つ以上のアドレス帳に含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7d245-110">A party, which can be either a person or an organization, can belong to one or more address books.</span></span>

### <a name="legal-entities"></a><span data-ttu-id="7d245-111">法人</span><span class="sxs-lookup"><span data-stu-id="7d245-111">Legal entities</span></span>

<span data-ttu-id="7d245-112">法人とは、登記または法的手続きを済ませた法律上の構造を持つ組織です。</span><span class="sxs-lookup"><span data-stu-id="7d245-112">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="7d245-113">法人には、法的契約の締結が認められており、業績を報告する収支報告書の作成が義務付けられています。</span><span class="sxs-lookup"><span data-stu-id="7d245-113">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="7d245-114">会社とは、法人の 1 つのタイプです。</span><span class="sxs-lookup"><span data-stu-id="7d245-114">A company is a type of legal entity.</span></span> <span data-ttu-id="7d245-115">現在、会社はユーザーが作成できる唯一の法人であり、個々の法人は会社 ID と関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="7d245-115">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="7d245-116">この関連付けは、プログラム内の一部の機能エリアで法人 ID (データモデルでは DataAreaId) が使用されているために設けられています。</span><span class="sxs-lookup"><span data-stu-id="7d245-116">This association exists because some functional areas in the program use a company ID, or DataAreaId, in their data models.</span></span> <span data-ttu-id="7d245-117">これらの機能エリアでは、データのセキュリティ区分として法人が使用されています。</span><span class="sxs-lookup"><span data-stu-id="7d245-117">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="7d245-118">ユーザーは、現在ログオン中の会社のデータにのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="7d245-118">Users can access data only for the company that they are currently logged on to.</span></span>

### <a name="operating-units"></a><span data-ttu-id="7d245-119">作業単位</span><span class="sxs-lookup"><span data-stu-id="7d245-119">Operating units</span></span>

<span data-ttu-id="7d245-120">作業単位とは、事業における経済資源と運営プロセスの管理を振り分ける際に使用する組織です。</span><span class="sxs-lookup"><span data-stu-id="7d245-120">An operating unit is an organization that is used to divide the control of economic resources and operational processes in a business.</span></span> <span data-ttu-id="7d245-121">作業単位のメンバは、希少なリソースの有効活用、プロセスの改善、および業績に対する責任を担っています。</span><span class="sxs-lookup"><span data-stu-id="7d245-121">People in an operating unit have a duty to maximize the use of scarce resources, improve processes, and account for their performance.</span></span>

<span data-ttu-id="7d245-122">作業単位のタイプには、コスト センター、事業単位、バリュー ストリーム、部門、コマース チャネルなどがあります。</span><span class="sxs-lookup"><span data-stu-id="7d245-122">The types of operating units include cost centers, business units, value streams, departments, and commerce channels.</span></span> <span data-ttu-id="7d245-123">次の表に、作業単位の各タイプに関する詳細情報を示します。</span><span class="sxs-lookup"><span data-stu-id="7d245-123">The following table provides more information about each type of operating unit.</span></span>

| <span data-ttu-id="7d245-124">作業単位のタイプ</span><span class="sxs-lookup"><span data-stu-id="7d245-124">Operating unit type</span></span> | <span data-ttu-id="7d245-125">説明</span><span class="sxs-lookup"><span data-stu-id="7d245-125">Description</span></span> | <span data-ttu-id="7d245-126">目的</span><span class="sxs-lookup"><span data-stu-id="7d245-126">Purpose</span></span> |
|---------------------|-------------|---------|
| <span data-ttu-id="7d245-127">原価部門</span><span class="sxs-lookup"><span data-stu-id="7d245-127">Cost center</span></span>         | <span data-ttu-id="7d245-128">予算経費と実績経費の責任をその管理者が負う作業単位。</span><span class="sxs-lookup"><span data-stu-id="7d245-128">An operating unit in which managers are accountable for budgeted and actual expenditures.</span></span> | <span data-ttu-id="7d245-129">法人間にまたがる業務プロセスの管理と運用管理に使用します。</span><span class="sxs-lookup"><span data-stu-id="7d245-129">Used for the management and operational control of business processes that span legal entities.</span></span> |
| <span data-ttu-id="7d245-130">事業単位</span><span class="sxs-lookup"><span data-stu-id="7d245-130">Business unit</span></span>       | <span data-ttu-id="7d245-131">戦略的なビジネス目標達成のために作成された半自治の事業単位。</span><span class="sxs-lookup"><span data-stu-id="7d245-131">A semi-autonomous operating unit that is created to meet strategic business objectives.</span></span> | <span data-ttu-id="7d245-132">法人とは別に、組織が係わる業界または製品ラインに基づいた財務報告に使用します。</span><span class="sxs-lookup"><span data-stu-id="7d245-132">Used for financial reporting that is based on industries or product lines that the organization serves independently of legal entities.</span></span> |
| <span data-ttu-id="7d245-133">バリュー ストリーム</span><span class="sxs-lookup"><span data-stu-id="7d245-133">Value stream</span></span>        | <span data-ttu-id="7d245-134">一つ以上の生産フローを制御する作業単位。</span><span class="sxs-lookup"><span data-stu-id="7d245-134">An operating unit that controls one or more production flows.</span></span> | <span data-ttu-id="7d245-135">消費者に製品やサービスを提供するために必要な活動およびフローを管理するリーン生産に一般的に使用します。</span><span class="sxs-lookup"><span data-stu-id="7d245-135">Commonly used in lean manufacturing to control the activities and flows that are required to supply a product or service to consumers.</span></span> |
| <span data-ttu-id="7d245-136">部門</span><span class="sxs-lookup"><span data-stu-id="7d245-136">Department</span></span>          | <span data-ttu-id="7d245-137">販売や会計など、特定のタスクを実行する組織のカテゴリまたは機能パーツを表す作業単位。</span><span class="sxs-lookup"><span data-stu-id="7d245-137">An operating unit that represents a category or functional part of an organization that performs a specific task, such as sales or accounting.</span></span> | <span data-ttu-id="7d245-138">機能分野の報告に使用します。</span><span class="sxs-lookup"><span data-stu-id="7d245-138">Used to report on functional areas.</span></span> <span data-ttu-id="7d245-139">部門は損益の職責を担っており、複数のコスト センターで構成される場合があります。</span><span class="sxs-lookup"><span data-stu-id="7d245-139">A department may have profit and loss responsibility, and may consist of a group of cost centers.</span></span> |
| <span data-ttu-id="7d245-140">Commerce チャネル</span><span class="sxs-lookup"><span data-stu-id="7d245-140">Commerce channel</span></span>      | <span data-ttu-id="7d245-141">従来型の店舗、オンライン ストア、またはオンライン マーケットプレースを表す作業単位。</span><span class="sxs-lookup"><span data-stu-id="7d245-141">An operating unit that represents a brick and mortar store, an online store or an online marketplace.</span></span> | <span data-ttu-id="7d245-142">法人内または法人全体の 1 つ以上の店舗の管理と運用管理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7d245-142">Used for the management and operational control of one or more stores within or across legal entities.</span></span> |

### <a name="teams"></a><span data-ttu-id="7d245-143">チーム</span><span class="sxs-lookup"><span data-stu-id="7d245-143">Teams</span></span>

<span data-ttu-id="7d245-144">メンバが共通の責任、関心、または目標を持つ組織。</span><span class="sxs-lookup"><span data-stu-id="7d245-144">A team is an organization in which the members share a common responsibility, interest, or objective.</span></span> <span data-ttu-id="7d245-145">チームは組織階層では使用できません。</span><span class="sxs-lookup"><span data-stu-id="7d245-145">Teams cannot be used in organizational hierarchies.</span></span>

## <a name="organizational-hierarchies"></a><span data-ttu-id="7d245-146">組織階層</span><span class="sxs-lookup"><span data-stu-id="7d245-146">Organizational hierarchies</span></span>

<span data-ttu-id="7d245-147">業務について、さまざまな観点から表示と報告を行う組織階層を設定します。</span><span class="sxs-lookup"><span data-stu-id="7d245-147">Set up organizational hierarchies to view and report on your business from different perspectives.</span></span> <span data-ttu-id="7d245-148">たとえば、税金、法律、または法令についての報告に使用するの法人の階層を設定できます。</span><span class="sxs-lookup"><span data-stu-id="7d245-148">For example, you can set up a hierarchy of legal entities for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="7d245-149">法的に必須でなくても内部統制に使用する財務情報を報告する階層を、作業単位に基づいて設定します。</span><span class="sxs-lookup"><span data-stu-id="7d245-149">Set up a hierarchy that is based on operating units to report financial information that is not legally required, but that is used for internal control.</span></span> <span data-ttu-id="7d245-150">たとえば、購買ポリシー、ルール、および業務プロセスを管理する購買階層を作成できます。</span><span class="sxs-lookup"><span data-stu-id="7d245-150">For example, you can create a purchasing hierarchy to control purchasing policies, rules, and business processes.</span></span>

<span data-ttu-id="7d245-151">各階層は目的で割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="7d245-151">Each hierarchy is assigned a purpose.</span></span> <span data-ttu-id="7d245-152">階層の目的により、階層に含めることができる組織のタイプが決まります。</span><span class="sxs-lookup"><span data-stu-id="7d245-152">The purpose of a hierarchy determines the types of organizations that can be included in the hierarchy.</span></span> <span data-ttu-id="7d245-153">この目的により、どのアプリケーションのシナリオで階層を使用できるかが決まります。</span><span class="sxs-lookup"><span data-stu-id="7d245-153">The purpose also determines which application scenarios a hierarchy can be used in.</span></span>

<span data-ttu-id="7d245-154">各階層の組織では、パラメータ、ポリシー、およびトランザクションを共有できます。</span><span class="sxs-lookup"><span data-stu-id="7d245-154">Organizations in a hierarchy can share parameters, policies, and transactions.</span></span> <span data-ttu-id="7d245-155">親組織のパラメータは、各組織で継承または上書きできます。</span><span class="sxs-lookup"><span data-stu-id="7d245-155">An organization can inherit or override the parameters of its parent organization.</span></span> <span data-ttu-id="7d245-156">ただし、製品やアドレス帳などの共有マスタ データは組織全体に適用され、個々の組織では上書きすることはできません。</span><span class="sxs-lookup"><span data-stu-id="7d245-156">However, shared master data, such as products and address books, applies to the whole organization and cannot be overridden for individual organizations.</span></span> <span data-ttu-id="7d245-157">組織と階層の作成は慎重に計画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d245-157">Creating organizations and hierarchies requires careful planning.</span></span> <span data-ttu-id="7d245-158">詳細については、[組織階層の計画](plan-organizational-hierarchy.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7d245-158">For more information, see [Plan your organizational hierarchy](plan-organizational-hierarchy.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]