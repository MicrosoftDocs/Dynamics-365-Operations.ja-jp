---
title: 予算計画データの配賦
description: このトピックは、Microsoft Dynamics 365 Finance で利用できる配賦方法と、その使用方法ついて説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 03/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ceddeda5760d961568d58e7e4805955ea972c586
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445314"
---
# <a name="budget-planning-data-allocation"></a>予算計画データの配賦

[!include [banner](../includes/banner.md)]

このトピックは、Microsoft Dynamics 365 Finance で利用できる配賦方法と、その使用方法ついて説明します。  

予想金額を正確に描くさまざまな方法で予算計画のデータを配分できます。

## <a name="allocation-methods"></a>配賦方法
3 つの配賦方法 (複数の期間に割り当て、分析コードへの配賦、および元帳配賦ルールの使用) で、同じ予算計画明細行に基づく予算計画明細行を作成できます。 3 つの他の方法 (集計、配分、および予算計画からのコピー) で、他の予算計画での予算計画明細行を作成できます。 すべての 6 つの配賦方法では、ターゲット シナリオを指定します。 ターゲット シナリオは、ソース シナリオと同じ場合も異なる場合もあります。 また、新しい明細行を予算計画に追加するか、予算計画の現在の明細行を置き換えるか指定できます。

> [!NOTE] 
> 集約には、親計画で以前に実行された配布またはその他の変更に使用されたシナリオとは異なる一意のシナリオを使用する必要があります。  

[![配賦方法を複数の期間に割り当てる](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**複数の期間に割り当て** – 期間割り当てカテゴリを使用して、ソース予算計画シナリオの予算計画明細行を、ターゲット シナリオの期間全域に配賦します。 当初起票額は、期間割り当てカテゴリで定義された割合と日付に基づいて、ターゲット シナリオの複数の明細行に割り当てられます。         

[![分析コード配賦方法への配賦](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**分析コードへの配賦** – 選択した予算配賦条件で定義された割合および財務分析コードに基づいて、ソース予算計画シナリオからターゲット シナリオの 1 つ以上の明細行に予算計画明細行を配賦します。           

![集計チャート](./media/aggregatechart-300x230.png)
**集計** – 関連付けられた (子) 予算計画のソース予算計画シナリオから、親予算計画のターゲット シナリオに予算計画明細行を集計します。 この方法で、上位レベルで統合されるように組織の下位レベルで準備した予算金額が有効になります。          

[![配分チャート](./media/distributechart-300x230.png)](./media/distributechart.png)
**配分** – 関連付けられた計画の組織単位の財務分析コードに基づいて、親予算計画のソース予算計画シナリオから、関連付けられた (子) 予算計画のターゲット シナリオに予算計画明細行を配分します。 この方法で、さらなるローカライズ レビューのために分配されるよう組織の上位レベルで準備した予算金額が有効になります。           

[![元帳配賦ルール](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**元帳配賦ルールの使用** – 選択された元帳配賦ルールに基づいて、ソース予算計画シナリオからターゲット シナリオに予算計画明細行を分配します。 

[![予算計画からのコピー](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**予算計画からのコピー** – 配分配賦の方法のように、関連する予算計画の明細行に基づいて、ターゲットに予算計画明細行を作成します。 ただし、この方法の場合、ソース予算計画は親である必要はありませんが、予算計画階層の上位になる可能性があります。 この配賦方法は、結合された金額をさらに上位レベルで予算とする場合に役立ち、詳細な確認と調整を行うには組織の下位レベルに転送させると、上位レベルの承認を受けられます。          

## <a name="using-allocation-methods-in-a-budget-plan"></a>予算計画の配賦方法を使用
予算計画ページで配賦を実行するには、配賦する明細行を選択し、**予算の配賦** をクリックします。

[![予算配賦ボタン](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png) 

次に、配賦方法を選択します。 残りのフィールドが選択した方法に基づいて設定されます。 これらのフィールドでは、予算計画データのソースとターゲット、および目標金額が作成される際に指定した係数をソースに掛けられる、バルク調整を簡単にするためのオプションが含まれます。 **計画への追加** オプションも設定できます。 **いいえ** を選択して既存の予算計画明細行を置き換えるか、**はい** を選択して既存の予算計画明細行をそのままにし、配賦済金額の新しい明細行を追加します。

## <a name="automating-allocations-during-a-workflow"></a>ワークフロー中の配賦の自動化
1 つの強力な機能を使用して、予算計画のワークフローの一部として配賦を自動的に実行できます。 予算計画はそのワークフローで進行するため、指定した予算計画ステージで自動化タスクで配賦を開始できます。 

自動配賦を設定するには、最初に **予算計画のコンフィギュレーション** ページで配賦スケジュールを作成する必要があります。 配賦スケジュールでは、自動配賦を実行する際に使用される配賦方法、およびさまざまな配賦オプションの値を定義します (説明は前のセクションを参照してください)。 

次に、**予算計画のコンフィギュレーション** ページでステージ配賦を作成します。 ステージ配賦は、予算計画のワークフローおよびステージに配賦スケジュールを割り当てます。 

最後に、目的のワークフロー ステージで予算計画ステージ配賦の自動化タスクを追加します。 次の例では、2 つの予算計画ステージ配賦 (赤に示されています) がワークフローに挿入されます。

[![予算計画ステージ配賦](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]