---
title: 拡張性 FAQ
description: このトピックでは、拡張機能に関してよくある質問に対する回答を示します。
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: 28568d7a959d3b29e7ea179c018c7e2fb9bd7e7e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368733"
---
# <a name="extensibility-faq"></a><span data-ttu-id="7c07c-103">拡張性 FAQ</span><span class="sxs-lookup"><span data-stu-id="7c07c-103">Extensibility FAQ</span></span>

[!include [banner](../includes/banner.md)]

## <a name="will-source-code-be-available-after-the-hard-seal"></a><span data-ttu-id="7c07c-104">ハード シールの後にソース コードを使用できますか。</span><span class="sxs-lookup"><span data-stu-id="7c07c-104">Will source code be available after the hard seal?</span></span>

<span data-ttu-id="7c07c-105">はい、ソース コードはハード シールの後に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7c07c-105">Yes, source code will be available after the hard seal.</span></span> <span data-ttu-id="7c07c-106">効果的な実装とデバッグのために必須とされます。</span><span class="sxs-lookup"><span data-stu-id="7c07c-106">It's required for effective implementation and debugging.</span></span>

## <a name="how-do-i-contact-microsoft-if-i-have-an-extensibility-request"></a><span data-ttu-id="7c07c-107">拡張機能の要求がある場合、Microsoft に連絡するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="7c07c-107">How do I contact Microsoft if I have an extensibility request?</span></span>

<span data-ttu-id="7c07c-108">Lifecycle Services (LCS) サイトには特別な拡張性要求書式があります。</span><span class="sxs-lookup"><span data-stu-id="7c07c-108">There is a special extensibility request form on the Lifecycle Services (LCS) site.</span></span> 

## <a name="where-can-i-ask-questions-about-extensibility-patterns"></a><span data-ttu-id="7c07c-109">拡張性のパターンについてはどこで質問できますか</span><span class="sxs-lookup"><span data-stu-id="7c07c-109">Where can I ask questions about extensibility patterns?</span></span>

<span data-ttu-id="7c07c-110">Yammer で Operations Extensibility グループに対するアクセスを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="7c07c-110">You can gain access to the Operations Extensibility group in Yammer.</span></span> <span data-ttu-id="7c07c-111">Operations Extensibility は、パートナー契約の大部分を占める有効なグループです。</span><span class="sxs-lookup"><span data-stu-id="7c07c-111">Operations Extensibility is an active group that has a significant amount of partner engagement.</span></span> <span data-ttu-id="7c07c-112">機密保持契約に署名することにより、接続サイト経由でアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="7c07c-112">You get access via the Connect site by signing an NDA.</span></span>

## <a name="where-can-i-find-documentation-about-extensibility-patterns"></a><span data-ttu-id="7c07c-113">拡張性のパターンについてのドキュメントはどこにありますか ?</span><span class="sxs-lookup"><span data-stu-id="7c07c-113">Where can I find documentation about extensibility patterns?</span></span>

<span data-ttu-id="7c07c-114">拡張性パターンについてのドキュメントは、[拡張性 ホーム ページ](extensibility-home-page.md)で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="7c07c-114">Documentation about extensibility patterns is available on the [Extensibility home page](extensibility-home-page.md).</span></span>

## <a name="where-can-i-get-information-about-extensibility-training"></a><span data-ttu-id="7c07c-115">拡張性のトレーニングに関する情報を取得する場所は?</span><span class="sxs-lookup"><span data-stu-id="7c07c-115">Where can I get information about extensibility training?</span></span>

<span data-ttu-id="7c07c-116">トレーニング セッションを複数の方法で公表します。</span><span class="sxs-lookup"><span data-stu-id="7c07c-116">We will announce training sessions in multiple ways.</span></span> <span data-ttu-id="7c07c-117">AppSource パートナーは一部のセッションについて直接招待を受ける可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7c07c-117">AppSource partners might receive direct invitations for some sessions.</span></span> <span data-ttu-id="7c07c-118">Operations Extensibility Yammer グループおよびその他のフォーラムのワーク ショップも公表します。</span><span class="sxs-lookup"><span data-stu-id="7c07c-118">We will also announce workshops in the Operations Extensibility Yammer group and other forums.</span></span>  

## <a name="what-is-the-goal-of-sealing-the-application"></a><span data-ttu-id="7c07c-119">アプリケーションの封印の目的は何ですか ?</span><span class="sxs-lookup"><span data-stu-id="7c07c-119">What is the goal of sealing the application?</span></span>

<span data-ttu-id="7c07c-120">アプリケーションは、エコシステムでのアップグレード コスト削減への第一歩としてシールされているため、顧客は、常に最新のリリースを利用できます。</span><span class="sxs-lookup"><span data-stu-id="7c07c-120">The application is being sealed as a step toward reducing upgrade costs in the ecosystem, so that customers can stay current on new releases.</span></span> <span data-ttu-id="7c07c-121">顧客は、Microsoft およびパートナーの新しい革新を利用することができます。</span><span class="sxs-lookup"><span data-stu-id="7c07c-121">Customers can take advantage of new innovations that come from Microsoft and partners.</span></span>

<span data-ttu-id="7c07c-122">拡張パッケージを使用すると、設計時のパフォーマンスが向上し、ビルドの自動化が迅速になり、単体テストが可能になります。</span><span class="sxs-lookup"><span data-stu-id="7c07c-122">Extension packages enable better performance at design time, faster build automation, and unit testing.</span></span> <span data-ttu-id="7c07c-123">また、独立したソフトウェア ベンダー (ISV) や顧客から、さまざまなシステム間でより効率的にモデルを配布したりインストールできるようになります。</span><span class="sxs-lookup"><span data-stu-id="7c07c-123">They also provide more efficient distribution and installation of models from independent software vendors (ISVs) and customers across different systems.</span></span>

## <a name="what-is-microsoft-working-on-to-support-this-move"></a><span data-ttu-id="7c07c-124">この動きをサポートするために Microsoft は何に取り組んでいますか ?</span><span class="sxs-lookup"><span data-stu-id="7c07c-124">What is Microsoft working on to support this move?</span></span>

<span data-ttu-id="7c07c-125">製品チームは、製品の拡張性を向上させるためにいくつかの分野に取り組んでいます。</span><span class="sxs-lookup"><span data-stu-id="7c07c-125">There are several areas where the product team is working to improve the extensibility of the product.</span></span> <span data-ttu-id="7c07c-126">この作業には、広範な影響を与えるプラットフォームの変更から、追加フック ポイントを提供するリファクタリングされたアプリケーション コードまでさまざまなものがあります。</span><span class="sxs-lookup"><span data-stu-id="7c07c-126">This work ranges from platform changes that have broad impact to refactored application code that provides additional hook points.</span></span> <span data-ttu-id="7c07c-127">詳細については、Operations Extensibility Yammer グループおよび製品のリリース ノートを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7c07c-127">For details, see the Operations Extensibility Yammer group and the product release notes.</span></span>

## <a name="after-the-application-is-sealed-what-should-customers-do-in-a-critical-situation-if-they-must-make-a-quick-change"></a><span data-ttu-id="7c07c-128">アプリケーションをシールした後、すばやく変更する必要がある場合、顧客は、重要な状態で何をすべきでしょうか?</span><span class="sxs-lookup"><span data-stu-id="7c07c-128">After the application is sealed, what should customers do in a critical situation if they must make a quick change?</span></span>

<span data-ttu-id="7c07c-129">このシナリオは、致命的なバグ修正が必要なシナリオと非常によく似ており、同じプロセスを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c07c-129">This scenario is very similar to a scenario where a critical bug fix is required, and the same process should be followed.</span></span> <span data-ttu-id="7c07c-130">必要な最初の手順として、サポートのためのケースを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c07c-130">As a required first step, you must create a case for support.</span></span>

## <a name="can-i-overlayer-an-isv-solution-after-the-hard-seal-of-the-application-code"></a><span data-ttu-id="7c07c-131">アプリケーション コードのハード シールの後に ISV ソリューションをオーバーレイすることはできますか。</span><span class="sxs-lookup"><span data-stu-id="7c07c-131">Can I overlayer an ISV solution after the hard seal of the application code?</span></span>

<span data-ttu-id="7c07c-132">ISV もモデルを封印することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7c07c-132">We recommend that ISVs also seal their models.</span></span> <span data-ttu-id="7c07c-133">このステップは、アップグレード コストを削減するというより広い目標を達成するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="7c07c-133">This step helps achieve the broader goal of reducing upgrade costs.</span></span> 

## <a name="will-i-be-able-to-overlayer-an-on-premises-solution"></a><span data-ttu-id="7c07c-134">オンプレミス ソリューションをオーバーレイすることはできますか。</span><span class="sxs-lookup"><span data-stu-id="7c07c-134">Will I be able to overlayer an on-premises solution?</span></span>

<span data-ttu-id="7c07c-135">オンプレミス ソリューションは、クラウド ソリューションとして同じパターンに従います。</span><span class="sxs-lookup"><span data-stu-id="7c07c-135">On-premises solutions will follow the same patterns as cloud solutions.</span></span> <span data-ttu-id="7c07c-136">したがって、Microsoft コードのオーバーレイはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="7c07c-136">Therefore, no overlayering of Microsoft code will be supported.</span></span>
    
## <a name="how-often-will-microsoft-provide-external-updates-so-that-partners-can-see-what-extensibility-enhancements-have-been-made"></a><span data-ttu-id="7c07c-137">どのくらいの頻度で Microsoft は外部更新を提供することで、パートナーがどの拡張性の強化が実行されたかを確認できますか。</span><span class="sxs-lookup"><span data-stu-id="7c07c-137">How often will Microsoft provide external updates so that partners can see what extensibility enhancements have been made?</span></span>

<span data-ttu-id="7c07c-138">Microsoft Dynamics 365 for Finance and Operations リリース 8.0 の後、プラットフォームおよびアプリケーションの月ごとの更新プログラムを提供する計画です。</span><span class="sxs-lookup"><span data-stu-id="7c07c-138">We plan to provide monthly updates of platform and application after Microsoft Dynamics 365 for Finance and Operations release 8.0.</span></span>

## <a name="why-wasnt-my-extensibility-request-accepted"></a><span data-ttu-id="7c07c-139">拡張性要求が承認されなかった理由を教えてください。</span><span class="sxs-lookup"><span data-stu-id="7c07c-139">Why wasn't my extensibility request accepted?</span></span>

<span data-ttu-id="7c07c-140">一部の拡張性は、重大な変更を要求します。</span><span class="sxs-lookup"><span data-stu-id="7c07c-140">Some extensibility requests break changes.</span></span> <span data-ttu-id="7c07c-141">重大な可能性のあるよくある要求の一部を、その考えられる回避策と共に以下に掲載します。</span><span class="sxs-lookup"><span data-stu-id="7c07c-141">Some of the more common potentially breaking requests are listed here along with potential workarounds.</span></span> <span data-ttu-id="7c07c-142">さらに、[拡張の作成](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/extensibility/add-enum-value)を読んで既存のプラットフォーム拡張機能については理解し、[拡張性要求を記録するためのヒント](https://blogs.msdn.microsoft.com/mfp/2018/09/15/tips-for-logging-extensibility-requests/)を読んで、機能が最新リリースに存在しない場合に適切な要求を作成する方法を確認してください。</span><span class="sxs-lookup"><span data-stu-id="7c07c-142">In addition, read [Creating extensions](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/extensibility/add-enum-value) to understand the existing platform extension capabilities and [Tips for logging extensibility requests](https://blogs.msdn.microsoft.com/mfp/2018/09/15/tips-for-logging-extensibility-requests/) to learn more about how to create solid requests if a capability doesn't exist in the latest release.</span></span>

### <a name="why-cant-edtstringsize-be-made-extensible"></a><span data-ttu-id="7c07c-143">EDT.StringSize を拡張可能にできないのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="7c07c-143">Why can't EDT.StringSize be made extensible?</span></span>

- <span data-ttu-id="7c07c-144">要求: 拡張を通じて EDT.StringSize を変更可能にする。</span><span class="sxs-lookup"><span data-stu-id="7c07c-144">Request: Make EDT.StringSize changeable via extension.</span></span>
- <span data-ttu-id="7c07c-145">問題: テーブル文字列フィールド (FieldX) のタイプが "親 EDT" であり、タイプが EDT2 (EDT2 は "親 EDT" から派生) の別のテーブルのフィールド (FieldY) に関連付けられている (テーブル関係を通じて) いる場合。</span><span class="sxs-lookup"><span data-stu-id="7c07c-145">Problem: When a table string field (FieldX) is of type “parent EDT" and is associated (through table relations) with another table’s field (FieldY) of type EDT2 (EDT2 is derived from “parent EDT”).</span></span> <span data-ttu-id="7c07c-146">EDT2.StringSize の増加を許可することで FieldY が大きい文字列を持つ可能性がある場合、FieldX は新しい文字列サイズを処理できません。</span><span class="sxs-lookup"><span data-stu-id="7c07c-146">If FieldY could have a larger string by allowing EDT2.StringSize to increase, FieldX would not be able to handle the new string size.</span></span> 
- <span data-ttu-id="7c07c-147">回避策: 新しい EDT を作成し、テーブル フィールド FieldY にそれを使用します。</span><span class="sxs-lookup"><span data-stu-id="7c07c-147">Workaround: Create a new EDT and use that for the table field FieldY.</span></span>

### <a name="why-cant-a-unique-table-index-be-made-extensible"></a><span data-ttu-id="7c07c-148">固有のテーブル インデックスを拡張可能にできないのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="7c07c-148">Why can't a unique table index be made extensible?</span></span>

- <span data-ttu-id="7c07c-149">要求: 拡張を通じて固有のテーブル インデックスを拡張可能にする。たとえば、余分なフィールドの追加を許可するによってなど。</span><span class="sxs-lookup"><span data-stu-id="7c07c-149">Request: Make unique table indexes changeable via extension, for example by allowing an extra field to be added.</span></span>
- <span data-ttu-id="7c07c-150">問題: 固有のテーブル インデックスが変更され、すべてのデータが新しいインデックスに準拠していない場合、重大な変更となります。</span><span class="sxs-lookup"><span data-stu-id="7c07c-150">Problem: If a unique table index changes and any data does not conform to the new index, then it would be a breaking change.</span></span> <span data-ttu-id="7c07c-151">また、重複レコードを取得できるようになったため、クエリに影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="7c07c-151">Also, any query would affect it since it can now retrieve a non-unique record.</span></span> <span data-ttu-id="7c07c-152">たとえば、Person テーブルにキー "Name" があり、name="Chris" が適切な担当者を選択したが、BirthDate がキーに追加された場合、"Chris" に複数のレコードが返される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7c07c-152">For example, if a Person table had a key of "Name" and select person where name="Chris" works, but if BirthDate was added to the key, now there could be multiple records returned for "Chris".</span></span>
- <span data-ttu-id="7c07c-153">回避策: validateWrite または validateInsert メソッドに "soft" 制約を追加します。</span><span class="sxs-lookup"><span data-stu-id="7c07c-153">Workaround: Add "soft" constraints in the validateWrite or validateInsert methods.</span></span>

### <a name="why-cant-countryregioncode-be-made-extensible-it-already-is"></a><span data-ttu-id="7c07c-154">CountryRegionCode を拡張可能にできないのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="7c07c-154">Why can't CountryRegionCode be made extensible?</span></span> <span data-ttu-id="7c07c-155">(*既にこのようになっています*)</span><span class="sxs-lookup"><span data-stu-id="7c07c-155">(*it already is*)</span></span>
- <span data-ttu-id="7c07c-156">要求: 拡張を通じて CountryRegionCode を変更可能にする。</span><span class="sxs-lookup"><span data-stu-id="7c07c-156">Request: Make CountryRegionCode changeable via extension.</span></span>
- <span data-ttu-id="7c07c-157">問題: プラットフォーム更新 14 以降、CountryRegionCode への変更は、CountryRegionCode プロパティに値が既にある場合にサポートされます。</span><span class="sxs-lookup"><span data-stu-id="7c07c-157">Problem: Starting with Platform update 14, changes to CountryRegionCode are supported if the CountryRegionCode property already has a value.</span></span> <span data-ttu-id="7c07c-158">変更の制限が厳しくなり (要素は一部の国/地域でのみ利用可能になりました)、重大な変更となる可能性があるため、空の CountryRegionCode プロパティを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="7c07c-158">Empty CountryRegionCode properties cannot be changed because that change is more restrictive (the element would now only be available for certain countries/regions) and therefore would be a breaking change.</span></span>
- <span data-ttu-id="7c07c-159">回避策: 要素が既に国/地域に固有の場合、既存の CountryRegionCode 拡張機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="7c07c-159">Workaround: Use the existing CountryRegionCode extension capability when the element is already country/region specific.</span></span>

### <a name="why-cant-the-table-field-properties-allowedit-alloweditoncreate-mandatory-or-ignoreedtrelation-be-made-extensible"></a><span data-ttu-id="7c07c-160">テーブル フィールド プロパティ AllowEdit、AllowEditOnCreate、Mandatory、または IgnoreEDTRelation を拡張可能にできないのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="7c07c-160">Why can't the Table Field properties AllowEdit, AllowEditOnCreate, Mandatory, or IgnoreEDTRelation be made extensible?</span></span>
- <span data-ttu-id="7c07c-161">リクエスト: テーブル フィールド プロパティ AllowEdit、AllowEditOnCreate、Mandatory、IgnoreEDTRelation を拡張機能経由で変更可能にします。</span><span class="sxs-lookup"><span data-stu-id="7c07c-161">Request: Make Table Field properties AllowEdit, AllowEditOnCreate, Mandatory, and/or IgnoreEDTRelation changeable via extension.</span></span>
- <span data-ttu-id="7c07c-162">問題: テーブル フィールドで "編集を許可"、"作成時の編集を許可"、"必須"、"IgnoreEDTRelation" プロパティを変更できると、重大な変更が生じます。</span><span class="sxs-lookup"><span data-stu-id="7c07c-162">Problem: The ability to change the "Allow Edit", "Allow Edit On Create", "Mandatory", and "IgnoreEDTRelation" properties on Table Fields would result in breaking changes.</span></span> <span data-ttu-id="7c07c-163">編集を許可するフィールドを変更すると、フィールドの目的が変更されます。</span><span class="sxs-lookup"><span data-stu-id="7c07c-163">Changing a field to allow editing changes the intent of the field.</span></span> <span data-ttu-id="7c07c-164">フィールドの編集を許可しないと、既存の動作が遮断されることがあります。</span><span class="sxs-lookup"><span data-stu-id="7c07c-164">Not allowing a field to be edited can break existing behavior.</span></span> <span data-ttu-id="7c07c-165">関係を変更すると、その関係の当初の目的が中断され、重大な変更となります。</span><span class="sxs-lookup"><span data-stu-id="7c07c-165">Changing a relation breaks the original intent of that relation, which is a breaking change.</span></span> <span data-ttu-id="7c07c-166">フィールドを必須にすると、既存の動作が中断される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7c07c-166">Making a field mandatory can result in breaking existing behavior.</span></span>
- <span data-ttu-id="7c07c-167">対応策: 拡張機能経由で新しいテーブル フィールドを追加し、必要に応じてそれを制御します。</span><span class="sxs-lookup"><span data-stu-id="7c07c-167">Workaround: Add new Table Fields via extension and control those as needed.</span></span>

### <a name="why-cant-security-privileges-be-made-extensible"></a><span data-ttu-id="7c07c-168">セキュリティ権限を拡張可能にできないのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="7c07c-168">Why can't Security Privileges be made extensible?</span></span>
- <span data-ttu-id="7c07c-169">要求: 拡張を通じてセキュリティ権限を変更可能にする。</span><span class="sxs-lookup"><span data-stu-id="7c07c-169">Request: Make Security Privilege changeable via extension.</span></span>
- <span data-ttu-id="7c07c-170">問題: セキュリティ権限を変更できると、変更が分割される可能性があります。これはセキュリティ メタデータの最下位レベルであるためです。</span><span class="sxs-lookup"><span data-stu-id="7c07c-170">Problem: The ability to change the Security Privilege would result in breaking changes because this are the lowest level of security metadata.</span></span>
- <span data-ttu-id="7c07c-171">対応策: 必要な場合は、新しいセキュリティ権限を作成し、それを使用します。</span><span class="sxs-lookup"><span data-stu-id="7c07c-171">Workaround: Create a new Security Privilege if needed and use that.</span></span>
