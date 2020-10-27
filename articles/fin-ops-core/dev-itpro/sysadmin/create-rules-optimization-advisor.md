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
ms.author: sericks
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 8c4f5eff01ab20ce9de2a30b27b163df8cf83e02
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985222"
---
# <a name="create-rules-for-optimization-advisor"></a>最適化アドバイザーのためのルールを作成します

[!include [banner](../includes/banner.md)]

このトピックでは、**最適化アドバイザー**のための新しいルールを作成する方法について説明します。 例えば、見積依頼 (RFQ) のケースに空のタイトルがあるかどうかを識別する新しいルールを作成できます。 ケースのタイトルを使用して、識別および検索を容易にします。 非常に単純ですが、この例では最適化ルールで何が達成できるかを示しています。 

*ルール*はアプリケーション データのチェックです。 ルールの評価条件が満たされた場合、プロセスを最適化したり、データを改善する案件が作成されます。 営業案件を対象にすることができ、必要に応じてアクションの影響を測定することができます。 

**最適化アドバイザー**の新しいルールを作成するために、**SelfHealingRule** 抽象クラスを拡張する新しいクラスの追加、**IDiagnosticsRule** インターフェイスの実装、および **DiagnosticRule** 属性によって修飾がされます。 クラスは **DiagnosticsRuleSubscription** 属性で修飾されるメソッドも必要です。 慣例として、これは **opportunityTitle** メソッドで実行されます。これについては後で説明します。 この新しいクラスは **SelfHealingRules** に依存関係を持つカスタム モデルに追加することができます。 実装されている **RFQTitleSelfHealingRule** と呼ばれるルールを以下の例に示します。

```xpp
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

**SelfHealingRule** 抽象クラスは、派生クラスで実装される必要がある抽象メソッドを持っています。 コアは**評価**方法です。ルールによって識別される案件の一覧を返します。 営業案件は法人ごと、またはシステム全体に適用できます。

```xpp
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

上記のメソッドは会社にループ、および **findRFQCasesWithEmptyTitle** メソッドで空のタイトルの RFQ ケースを選択します。 このようなケースが 1 つでも見つかった場合、**getOpportunityForCompany** メソッドで会社固有の営業案件が作成されます。 **SelfHealingOpportunity** テーブルの **データ** フィールドはタイプ **コンテナー**です。そのため、このルールに固有のロジックに適切なデータを含めることができます。 現在のタイムスタンプを持つ **OpportunityDate** 設定は営業案件の最新の評価の時間を登録します。  

営業案件は会社間でも可能です。 この場合、会社にループすることは必要ではなく、営業案件は **getOpportunityAcrossCompanies** メソッドで作成される必要があります。 

次のコードは **findRFQCasesWithEmptyTitle** メソッドを示しており、空のタイトルがある RFQ ケースの ID を返します。

```xpp
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

実装される必要のあるさらに 2 つのメソッドは、**opportunityTitle** および **opportunityDetails** です。 前者は営業案件の簡単なタイトルを返し、後者は営業案件の詳細な説明を返します。これはデータを含めることもできます。

**opportunityTitle** によって返されるタイトルは、**Optimization advisor** ワークスペースの **Optimization opportunity** 列の下に表示されます。 作業ウィンドウのヘッダーとして、営業案件についての詳細情報が表示されます。 慣例として、**DiagnosticRuleSubscription** 属性でこのメソッドは修飾されます。このメソッドは次の引数を使用します。 

* **診断エリア** – **DiagnosticArea::SCM** のような、ルールが属するアプリケーションのどの領域かを説明する **DiagnosticArea** タイプの列挙型。 

* **ルール名** – ルール名の文字列。 これは、**診断検証ルール** フォーム (**DiagnosticsValidationRuleMaintain**) 内の **ルール名** コラムの下に表示されます。 

* **実行頻度** – **DiagnosticRunFrequency::Daily** のような、どのくらいの頻度でルールが実行されるかを説明する **DiagnosticRunFrequency** タイプの列挙型。 

* **ルールの説明** – ルールの詳細な説明の文字列。 これは、**診断検証ルール** フォーム (**DiagnosticsValidationRuleMaintain**) 内の **ルールの説明** コラムの下に表示されます。 

> [!NOTE]
> **DiagnosticRuleSubscription** 属性はルールが機能するために必要です。 通常、**opportunityTitle** で使用されますが、クラスの任意のメソッドで修飾できます。

実装例を次に示します。 未加工の文字列は単純化のために使用されていますが、正しい実装にはラベルが必要です。 

```xpp
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

**opportunityDetails** によって返された説明が作業ウィンドウに表示され、営業案件に関する詳細を示します。 これは **SelfHealingOpportunity** 引数を取ります。これは営業案件についての詳細を提供するために使用される **データ** フィールドです。 例では、メソッドは空のタイトルを持つ RFQ ケースの ID を返します。 

```xpp
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

実装する残りの 2 つの抽象メソッドは **provideHealingAction** および **securityMenuItem** です。 

**provideHealingAction** は修復アクションを指定すると true を返します。それ以外の場合は false を返します。 true が返された場合、**performAction** メソッドを実装する必要があるか、またはエラーがスローされます。 **performAction** メソッドは **SelfHealingOpportunity** 引数を取ります。この引数では、データをアクションに使用できます。 例では、手動で修正するために、アクションが **PurchRFQCaseTableListPage** を開きます。 

```xpp
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

ルールの詳細によっては、営業案件データを使用して自動アクションを行うことが可能な場合もあります。 この例では、システムが RFQ ケースのタイトルを自動的に生成します。 

**securityMenuItem** は、アクション メニュー項目にアクセスできるユーザーのみがルールを表示できるように、アクション メニュー項目の名前を返します。 セキュリティは、特定のルールや営業案件に許可されたユーザーのみがアクセスできることを求める場合があります。 この例では、**PurchRFQCaseTitleAction** へのアクセス権を持つユーザーのみが営業案件を見ることができます。 このアクション メニュー項目は、この例で作成され、**PurchRFQCaseTableMaintain** セキュリティ権限のエントリ ポイントとして追加されたことに注目してください。 

> [!NOTE]
> メニュー項目は、セキュリティが正常に機能するためのアクション メニュー項目である必要があります。 **メニュー項目の表示** などのその他のメニュー項目タイプは、正しく動作しません。

```xpp
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

ルールがコンパイルされたら、次のジョブを実行してユーザー インターフェイス (UI) に表示させます。

```xpp
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

ルールは **診断検証ルール** フォームで表示され、**システム管理** > **定期処理のタスク** > **診断検証ルールの管理** からも使用できます。 それを評価するために、**システム管理** > **定期処理のタスク** > **診断検証ルールのスケジュール** に移動し、**毎日** のようなルールの頻度を選択します。 **OK** をクリックします。 **システム管理** > **最適化アドバイザー** に移動し、営業案件を表示します。 

次の例は、すべての必要なメソッドと属性を含むルールのスケルトンを持つコード スニペットです。 これにより、新しいルールの作成を開始することができます。この例で使用するラベルおよびアクション メニュー項目は、デモ目的でのみ使用されます。

```xpp
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

詳細については、短い YouTube ビデオを確認してください: [Dynamics 365 for Finance and Operations の最適化アドバイザー](https://www.youtube.com/watch?v=MRsAzgFCUSQ)
