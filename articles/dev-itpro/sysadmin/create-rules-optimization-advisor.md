---
title: 最適化アドバイザーのためのルールを作成します
description: このトピックでは、最適化アドバイザーのための新しいルールを追加する方法について説明します。
author: roxanadiaconu
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 27066cd860d78743d5ae7c851876eb62fe019245
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851424"
---
# <a name="create-rules-for-optimization-advisor"></a><span data-ttu-id="cab1d-103">最適化アドバイザーのためのルールを作成します</span><span class="sxs-lookup"><span data-stu-id="cab1d-103">Create rules for Optimization advisor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cab1d-104">このトピックでは、**最適化アドバイザー**のための新しいルールを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cab1d-104">This topic explains how to create new rules for **Optimization advisor**.</span></span> <span data-ttu-id="cab1d-105">例えば、見積依頼 (RFQ) のケースに空のタイトルがあるかどうかを識別する新しいルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-105">For example, you can create a new rule that identifies which Request for Quotations (RFQ) cases have an empty title.</span></span> <span data-ttu-id="cab1d-106">ケースのタイトルを使用して、識別および検索を容易にします。</span><span class="sxs-lookup"><span data-stu-id="cab1d-106">Using titles on cases makes them easily identifiable and searchable.</span></span> <span data-ttu-id="cab1d-107">非常に単純ですが、この例では最適化ルールで何が達成できるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="cab1d-107">While quite simple, this example shows what can be achieved with optimization rules.</span></span> 

<span data-ttu-id="cab1d-108">*ルール*はアプリケーション データのチェックです。</span><span class="sxs-lookup"><span data-stu-id="cab1d-108">A *rule* is a check on application data.</span></span> <span data-ttu-id="cab1d-109">ルールの評価条件が満たされた場合、プロセスを最適化したり、データを改善する案件が作成されます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-109">If the condition that the rule evaluates is met, opportunities to optimize processes or improve data are created.</span></span> <span data-ttu-id="cab1d-110">営業案件を対象にすることができ、必要に応じてアクションの影響を測定することができます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-110">The opportunities can be acted upon and, optionally, the impact of the actions can be measured.</span></span> 

<span data-ttu-id="cab1d-111">**最適化アドバイザー**の新しいルールを作成するために、**SelfHealingRule** 抽象クラスを拡張する新しいクラスの追加、**IDiagnosticsRule** インターフェイスの実装、および **DiagnosticRule** 属性によって修飾がされます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-111">To create a new rule for the **Optimization advisor**, add a new class that extends the **SelfHealingRule** abstract class, implements the **IDiagnosticsRule** interface, and is decorated by the **DiagnosticRule** attribute.</span></span> <span data-ttu-id="cab1d-112">クラスは **DiagnosticsRuleSubscription** 属性で修飾されるメソッドも必要です。</span><span class="sxs-lookup"><span data-stu-id="cab1d-112">The class must also have a method decorated with the **DiagnosticsRuleSubscription** attribute.</span></span> <span data-ttu-id="cab1d-113">慣例として、これは **opportunityTitle** メソッドで実行されます。これについては後で説明します。</span><span class="sxs-lookup"><span data-stu-id="cab1d-113">By convention, that is done on the **opportunityTitle** method, which will be discussed later.</span></span> <span data-ttu-id="cab1d-114">この新しいクラスは **SelfHealingRules** に依存関係を持つカスタム モデルに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-114">This new class can be added to a custom model with a dependency on the **SelfHealingRules** model.</span></span> <span data-ttu-id="cab1d-115">実装されている **RFQTitleSelfHealingRule** と呼ばれるルールを以下の例に示します。</span><span class="sxs-lookup"><span data-stu-id="cab1d-115">In the following example, the rule being implemented is called **RFQTitleSelfHealingRule**.</span></span>

```
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

<span data-ttu-id="cab1d-116">**SelfHealingRule** 抽象クラスは、派生クラスで実装される必要がある抽象メソッドを持っています。</span><span class="sxs-lookup"><span data-stu-id="cab1d-116">The **SelfHealingRule** abstract class has abstract methods that must be implemented in inheriting classes.</span></span> <span data-ttu-id="cab1d-117">コアは**評価**方法です。ルールによって識別される案件の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="cab1d-117">The core is the **evaluate** method, which returns a list of the opportunities identified by the rule.</span></span> <span data-ttu-id="cab1d-118">営業案件は法人ごと、またはシステム全体に適用できます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-118">Opportunities can be per legal entity or can apply to the whole system.</span></span>

```
protected List evaluate() 
{ 
    List results = new List(Types::Record); 
    
    DataArea dataArea; 

    while select id from dataArea 
        where !dataArea.isVirtual 
    { 
        changecompany(dataArea.id) 
        { 
            container result = this.findRFQCasesWithEmptyTitle(); 

            if (conLen(result) > 0) 
            { 
                SelfHealingOpportunity opportunity = this.getOpportunityForCompany(dataArea.Id); 
                opportunity.EvaluationState = SelfHealingEvaluationState::Evaluated; 
                opportunity.Data = result; 
                opportunity.OpportunityDate = DateTimeUtil::utcNow(); 
                
                results.addEnd(opportunity); 
            } 
        } 
    } 
    
    return results; 
} 
```

<span data-ttu-id="cab1d-119">上記のメソッドは会社にループ、および **findRFQCasesWithEmptyTitle** メソッドで空のタイトルの RFQ ケースを選択します。</span><span class="sxs-lookup"><span data-stu-id="cab1d-119">The method shown above loops over companies and selects RFQ cases with empty titles in the **findRFQCasesWithEmptyTitle** method.</span></span> <span data-ttu-id="cab1d-120">このようなケースが 1 つでも見つかった場合、**getOpportunityForCompany** メソッドで会社固有の営業案件が作成されます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-120">If at least one such case is found, then a company-specific opportunity is created with the **getOpportunityForCompany** method.</span></span> <span data-ttu-id="cab1d-121">**SelfHealingOpportunity** テーブルの **データ** フィールドはタイプ **コンテナー**です。そのため、このルールに固有のロジックに適切なデータを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-121">Notice that the field **Data** in the **SelfHealingOpportunity** table is of type **Container**, and can therefore contain any data relevant to the logic specific to this rule.</span></span> <span data-ttu-id="cab1d-122">現在のタイムスタンプを持つ **OpportunityDate** 設定は営業案件の最新の評価の時間を登録します。</span><span class="sxs-lookup"><span data-stu-id="cab1d-122">Setting **OpportunityDate** with the current timestamp registers the time of the latest evaluation of the opportunity.</span></span>  

<span data-ttu-id="cab1d-123">営業案件は会社間でも可能です。</span><span class="sxs-lookup"><span data-stu-id="cab1d-123">Opportunities can also be cross-company.</span></span> <span data-ttu-id="cab1d-124">この場合、会社にループすることは必要ではなく、営業案件は **getOpportunityAcrossCompanies** メソッドで作成される必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab1d-124">In this case, the loop over companies is not necessary and the opportunity must be created with the **getOpportunityAcrossCompanies** method.</span></span> 

<span data-ttu-id="cab1d-125">次のコードは **findRFQCasesWithEmptyTitle** メソッドを示しており、空のタイトルがある RFQ ケースの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="cab1d-125">The following code shows the **findRFQCasesWithEmptyTitle** method, which returns the IDs of the RFQ cases that have empty titles.</span></span>

```
private container findRFQCasesWithEmptyTitle() 
{ 
    container result; 

    PurchRFQCaseTable rfqCase; 
    while select RFQCaseId from rfqCase 
        where rfqCase.Name == '' 
    { 
        result += rfqCase.RFQCaseId; 
    } 
    
    return result; 
} 
```

<span data-ttu-id="cab1d-126">実装される必要のあるさらに 2 つのメソッドは、**opportunityTitle** および **opportunityDetails** です。</span><span class="sxs-lookup"><span data-stu-id="cab1d-126">Two more methods that must be implemented are **opportunityTitle** and **opportunityDetails**.</span></span> <span data-ttu-id="cab1d-127">前者は営業案件の簡単なタイトルを返し、後者は営業案件の詳細な説明を返します。これはデータを含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-127">The former returns a short title for the opportunity, the latter returns a detailed description of the opportunity, which can also include data.</span></span>

<span data-ttu-id="cab1d-128">**opportunityTitle** によって返されるタイトルは、**Optimization advisor** ワークスペースの **Optimization opportunity** 列の下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-128">The title returned by **opportunityTitle** appears under the **Optimization opportunity** column in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="cab1d-129">作業ウィンドウのヘッダーとして、営業案件についての詳細情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-129">It also appears as the header of the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="cab1d-130">慣例として、**DiagnosticRuleSubscription** 属性でこのメソッドは修飾されます。このメソッドは次の引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="cab1d-130">By convention, this method is decorated with the **DiagnosticRuleSubscription** attribute, which takes the following arguments:</span></span> 

* <span data-ttu-id="cab1d-131">**診断エリア** – **DiagnosticArea::SCM** のような、ルールが属するアプリケーションのどの領域かを説明する **DiagnosticArea** タイプの列挙型。</span><span class="sxs-lookup"><span data-stu-id="cab1d-131">**Diagnostic area** – An enum of type **DiagnosticArea** that describes what area of the application the rule belongs to, such as **DiagnosticArea::SCM**.</span></span> 

* <span data-ttu-id="cab1d-132">**ルール名** – ルール名の文字列。</span><span class="sxs-lookup"><span data-stu-id="cab1d-132">**Rule name** – A string with the rule name.</span></span> <span data-ttu-id="cab1d-133">これは、**診断検証ルール** フォーム (**DiagnosticsValidationRuleMaintain**) 内の **ルール名** コラムの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-133">This will appear under the **Rule name** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

* <span data-ttu-id="cab1d-134">**実行頻度** – **DiagnosticRunFrequency::Daily** のような、どのくらいの頻度でルールが実行されるかを説明する **DiagnosticRunFrequency** タイプの列挙型。</span><span class="sxs-lookup"><span data-stu-id="cab1d-134">**Run frequency** – An enum of type **DiagnosticRunFrequency** that describes how often the rule should be run, such as **DiagnosticRunFrequency::Daily**.</span></span> 

* <span data-ttu-id="cab1d-135">**ルールの説明** – ルールの詳細な説明の文字列。</span><span class="sxs-lookup"><span data-stu-id="cab1d-135">**Rule description** – A string with a more detailed description of the rule.</span></span> <span data-ttu-id="cab1d-136">これは、**診断検証ルール** フォーム (**DiagnosticsValidationRuleMaintain**) 内の **ルールの説明** コラムの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-136">This will appear under the **Rule description** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

> [!NOTE]
> <span data-ttu-id="cab1d-137">**DiagnosticRuleSubscription** 属性はルールが機能するために必要です。</span><span class="sxs-lookup"><span data-stu-id="cab1d-137">The **DiagnosticRuleSubscription** attribute is required for the rule to work.</span></span> <span data-ttu-id="cab1d-138">通常、**opportunityTitle** で使用されますが、クラスの任意のメソッドで修飾できます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-138">Typically, it is used on **opportunityTitle**, but it can decorate any method of the class.</span></span>

<span data-ttu-id="cab1d-139">実装例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="cab1d-139">The following is an example implementation.</span></span> <span data-ttu-id="cab1d-140">未加工の文字列は単純化のために使用されていますが、正しい実装にはラベルが必要です。</span><span class="sxs-lookup"><span data-stu-id="cab1d-140">Raw strings are used for simplicity, but a correct implementation requires labels.</span></span> 

```
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

<span data-ttu-id="cab1d-141">**opportunityDetails** によって返された説明が作業ウィンドウに表示され、営業案件に関する詳細を示します。</span><span class="sxs-lookup"><span data-stu-id="cab1d-141">The description returned by **opportunityDetails** appears on the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="cab1d-142">これは **SelfHealingOpportunity** 引数を取ります。これは営業案件についての詳細を提供するために使用される **データ** フィールドです。</span><span class="sxs-lookup"><span data-stu-id="cab1d-142">This takes the **SelfHealingOpportunity** argument, which is **Data** field that can be used to provide more details about the opportunity.</span></span> <span data-ttu-id="cab1d-143">例では、メソッドは空のタイトルを持つ RFQ ケースの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="cab1d-143">In the example, the method returns the IDs of the RFQ cases with an empty title.</span></span> 

```
public str opportunityDetails(SelfHealingOpportunity _opportunity) 
{ 
    str details = ''; 
    container opportunityData = _opportunity.Data; 
    int affectedRFQCasesCount = conLen(opportunityData); 

    if (affectedRFQCasesCount != 0) 
    { 
        details = 'The following Request for Quotation cases have an empty title:\n'; 
        for (int i = 1; i <= affectedRFQCasesCount ; i++) 
        { 
            PurchRFQCaseId rfqCaseId = conPeek(opportunityData, i); 
            details += rfqCaseId + '\n'; 
        } 
    } 

    return details; 
}
```

<span data-ttu-id="cab1d-144">実装する残りの 2 つの抽象メソッドは **provideHealingAction** および **securityMenuItem** です。</span><span class="sxs-lookup"><span data-stu-id="cab1d-144">The two remaining abstract methods to implement are **provideHealingAction** and **securityMenuItem**.</span></span> 

<span data-ttu-id="cab1d-145">**provideHealingAction** は修復アクションを指定すると true を返します。それ以外の場合は false を返します。</span><span class="sxs-lookup"><span data-stu-id="cab1d-145">**provideHealingAction** returns true if a healing action is provided, otherwise, it returns false.</span></span> <span data-ttu-id="cab1d-146">true が返された場合、**performAction** メソッドを実装する必要があるか、またはエラーがスローされます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-146">If true is returned, the method **performAction** must be implemented, or an error will be thrown.</span></span> <span data-ttu-id="cab1d-147">**performAction** メソッドは **SelfHealingOpportunity** 引数を取ります。この引数では、データをアクションに使用できます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-147">The **performAction** method takes a **SelfHealingOpportunity** argument, in which the data can be used for the action.</span></span> <span data-ttu-id="cab1d-148">例では、手動で修正するために、アクションが **PurchRFQCaseTableListPage** を開きます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-148">In the example, the action opens the **PurchRFQCaseTableListPage**, for manual correction.</span></span> 

```
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

<span data-ttu-id="cab1d-149">ルールの詳細によっては、営業案件データを使用して自動アクションを行うことが可能な場合もあります。</span><span class="sxs-lookup"><span data-stu-id="cab1d-149">Depending on the specifics of the rule, it might be possible to take an automatic action using the opportunity data.</span></span> <span data-ttu-id="cab1d-150">この例では、システムが RFQ ケースのタイトルを自動的に生成します。</span><span class="sxs-lookup"><span data-stu-id="cab1d-150">In this example, the system could generate titles for RFQ cases automatically.</span></span> 

<span data-ttu-id="cab1d-151">**securityMenuItem** は、アクション メニュー項目にアクセスできるユーザーのみがルールを表示できるように、アクション メニュー項目の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="cab1d-151">**securityMenuItem** returns the name of an action menu item such that the rule is only visible to users who can access the action menu item.</span></span> <span data-ttu-id="cab1d-152">セキュリティは、特定のルールや営業案件に許可されたユーザーのみがアクセスできることを求める場合があります。</span><span class="sxs-lookup"><span data-stu-id="cab1d-152">Security might require that specific rules and opportunities are accessible only to authorized users.</span></span> <span data-ttu-id="cab1d-153">この例では、**PurchRFQCaseTitleAction** へのアクセス権を持つユーザーのみが営業案件を見ることができます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-153">In the example, only users with access to **PurchRFQCaseTitleAction** can view the opportunity.</span></span> <span data-ttu-id="cab1d-154">このアクション メニュー項目は、この例で作成され、**PurchRFQCaseTableMaintain** セキュリティ権限のエントリ ポイントとして追加されたことに注目してください。</span><span class="sxs-lookup"><span data-stu-id="cab1d-154">Notice that this action menu item was created for this example, and was added as an entry point for the **PurchRFQCaseTableMaintain** security privilege.</span></span> 

> [!NOTE]
> <span data-ttu-id="cab1d-155">メニュー項目は、セキュリティが正常に機能するためのアクション メニュー項目である必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab1d-155">The menu item must be an action menu item for security to work correctly.</span></span> <span data-ttu-id="cab1d-156">**メニュー項目の表示** などのその他のメニュー項目タイプは、正しく動作しません。</span><span class="sxs-lookup"><span data-stu-id="cab1d-156">Other menu item types, such as **Display menu items** will not work correctly.</span></span>

```
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

<span data-ttu-id="cab1d-157">ルールがコンパイルされたら、次のジョブを実行してユーザー インターフェイス (UI) に表示させます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-157">After the rule has compiled, execute the following job to have it display in the user interface (UI).</span></span>

```
class ScanNewRulesJob 
{         
    public static void main(Args _args) 
    {         
        SysExtensionCache::clearAllScopes(); 
        var controller = new DiagnosticsRuleController(); 
        controller.runOperation(); 
    } 
} 
```

<span data-ttu-id="cab1d-158">ルールは **診断検証ルール** フォームで表示され、**システム管理** > **定期処理のタスク** > **診断検証ルールの管理** からも使用できます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-158">The rule will display in the **Diagnostics validation rule** form, available from **System administration** > **Periodic tasks** > **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="cab1d-159">それを評価するために、**システム管理** > **定期処理のタスク** > **診断検証ルールのスケジュール** に移動し、**毎日** のようなルールの頻度を選択します。</span><span class="sxs-lookup"><span data-stu-id="cab1d-159">To have it evaluated, go to **System administration** > **Periodic tasks** > **Schedule diagnostics validation rule**, select the frequency of the rule, such as **Daily**.</span></span> <span data-ttu-id="cab1d-160">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cab1d-160">Click **OK**.</span></span> <span data-ttu-id="cab1d-161">**システム管理** > **最適化アドバイザー** に移動し、営業案件を表示します。</span><span class="sxs-lookup"><span data-stu-id="cab1d-161">Go to **System administration** > **Optimization advisor** to view the new opportunity.</span></span> 

<span data-ttu-id="cab1d-162">次の例は、すべての必要なメソッドと属性を含むルールのスケルトンを持つコード スニペットです。</span><span class="sxs-lookup"><span data-stu-id="cab1d-162">The following example is a code snippet with the skeleton of a rule including all the required methods and attributes.</span></span> <span data-ttu-id="cab1d-163">これにより、新しいルールの作成を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-163">It helps you get started with writing new rules.</span></span><span data-ttu-id="cab1d-164">この例で使用するラベルおよびアクション メニュー項目は、デモ目的でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="cab1d-164"> The labels and action menu items that are used in the example are only used for demonstration purpose.</span></span>

```
[DiagnosticsRuleAttribute]
public final class SkeletonSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule
{
    [DiagnosticsRuleSubscription(DiagnosticsArea::SCM,
                                 "@SkeletonRuleLabels:SkeletonRuleTitle", // Label with the title of the rule
                                 DiagnosticsRunFrequency::Monthly,
                                 "@SkeletonRuleLabels:SkeletonRuleDescription")] // Label with a description of the rule
    public str opportunityTitle()
    {
        // Return a label with the title of the opportunity
        return "@SkeletonRuleLabels:SkeletonOpportunityTitle";
    }

    public str opportunityDetails(SelfHealingOpportunity _opportunity)
    {
        str details = "";

        // Use _opportunity.data to provide details on the opportunity

        return details;
    }

    protected List evaluate()
    {
        List results = new List(Types::Record);

        // Write here the core logic of the rule

        // When creating an opportunity, use:
        //     * this.getOpportunityForCompany() for company specific opportunities
        //     * this.getOpportunityAcrossCompanies() for cross-company opportunities

        return results;
    }

    public boolean providesHealingAction()
    {
        return true;
    }

    protected void performAction(SelfHealingOpportunity _opportunity)
    {
        // Place here the code that performs the healing action

        // To open a form, use the following:
        // new MenuFunction(menuItemDisplayStr(SkeletonRuleDisplayMenuItem), MenuItemType::Display).run();
    }

    public MenuName securityMenuItem()
    {
        return menuItemActionStr(SkeletonRuleActionMenuItem);
    }

}
```

<span data-ttu-id="cab1d-165">詳細については、短い YouTube ビデオを確認してください: [Dynamics 365 for Finance and Operations の最適化アドバイザー](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span><span class="sxs-lookup"><span data-stu-id="cab1d-165">For more information, watch the short YouTube video: [Optimization advisor in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span></span>
