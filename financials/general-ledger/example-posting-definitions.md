---
title: "転記の定義"
description: "この記事では、発注書の債務および予算割り当てに対する転記の定義の使用方法を示す例を示します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 06d789d83b623e76c67a6ec4c9fc1fea673d3294
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="posting-definition-examples"></a>転記の定義の例

[!include[banner](../includes/banner.md)]


この記事では、発注書の債務および予算割り当てに対する転記の定義の使用方法を示す例を示します。

このトピックの読み取る前に、転記の定義とトランザクションの転記の定義をよく理解しておく必要があります。 詳細については、「[転記の定義](posting-definitions.md)」を参照してください。 次の例は、**転記の定義**ページで設定できます。 各例には、次のセクションが含まれています:

-   転記の定義 – 照合基準
-   転記の定義 – 生成されたエントリ
-   勘定、分析コード値、および金額を含むトランザクション
-   転記の定義から生成された元帳エントリ

転記の定義と、トランザクションの勘定と分析コード値について**照合基準**ページで、勘定と分析コード値の間に一致があった場合、転記の定義の**生成されたエントリ** ペインに基づいて、元帳エントリが生成されます。 
> [!NOTE]
> 転記の定義を特定のトランザクション タイプに関連付けるには、**トランザクションの転記の定義**ページを使用します。 転記の定義をトランザクション タイプに関連付け、**一般会計パラメーター** ページで [**転記の定義の使用**] を選択した後、選択されたトランザクション タイプのすべてのトランザクションでは、転記の定義を使用する必要があります。

## <a name="example-purchase-order-encumbrances"></a>例: 発注書の債務
**総勘定元帳パラメーター** ページの**債務プロセスの有効化**を選択して債務処理を有効にした場合、転記の定義を使用して、引当対象の勘定の総勘定元帳に債務を記録する必要があります。 ほとんどの場合、すべての経費勘定は、貸借対照表で引当が行われます。 

債務の転記の定義は、**転記の定義**ページの**購買**モジュールに対して設定されます。 その後、**トランザクションの転記の定義**ページの**購買**の領域で、**発注書**のトランザクション タイプを選択して、転記の定義を発注書に関連付けることができます。 

発注書の債務のすべての伝票トランザクションは、伝票の一意の分析コードで精算する (借方と貸方が等しくなる必要がある) 必要があります。

### <a name="posting-definition--match-criteria"></a>転記の定義 – 照合基準

| 勘定構造       | 照合勘定番号 | 優先順位 |
|-------------------------|----------------------|----------|
| 勘定構造 - P&L | \*                   | 1        |

* **照合勘定番号**フィールドの空白の値は、定義された勘定構造のすべての照合勘定が一致するルールの一部になります。

### <a name="posting-definition--generated-entries"></a>転記の定義 – 生成されたエントリ

| 勘定構造 | 生成された勘定番号                    | 生成された借方/貸方 |
|-------------------|---------------------------------------------|------------------------|
| 残高           | 300143 - -(債務口座)             | 同じ                   |
| 残高           | 300144 - -(債務口座の引当) | バランスをとる              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>勘定、分析コード値、および金額を含むトランザクション

勘定および分析コード値は、購買注文明細行に対して入力する勘定配布から来ているか、または仕入先、品目、カテゴリ、および分析コードのテンプレートの既定の設定に基づいて自動的に生成される分析コードと勘定から来ています。

| 口座 + 分析コード           | デビット  | クレジット | コメント |
|--------------------------------|--------|--------|---------|
| 606400-OU\_1-OU\_3566-トレーニング | 250.00 |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>転記の定義から生成された元帳エントリ

生成された元帳エントリは債務を記録するために作成されます。

| 口座 + 分析コード           | デビット  | クレジット | コメント |
|--------------------------------|--------|--------|---------|
| 300143-OU\_1-OU\_3566-トレーニング | 250.00 |        |         |
| 300144-OU\_1-OU\_3566-トレーニング |        | 250.00 |         |

この例では、勘定構造 - P&L の一部であるいずれかの口座が転記の定義の基準に一致します。 したがって、606500-OU\_1-OU\_3566-トレーニングが評価されると、生成されたエントリは転記の定義の**生成されたエントリ** ペインで定義された勘定に対して作成されます。

## <a name="example-budget-appropriations"></a>例: 予算割り当て
**総勘定元帳パラメーター** ページの **予算割り当ての有効化**を選択して予算割り当てを有効にすると、一般会計への予算登録のエントリを記録するためには、転記の定義を使用する必要があります。 予算管理コンフィギュレーションが有効な場合、一般会計に対して、割り当て、変更、転送、プロジェクト、固定資産、および供給と需要予測のエントリの記録をサポートするために、転記の定義とトランザクションの転記の定義を使用できます。 

**元の予算**の予算タイプがあり、有効な割り当てがある予算登録エントリの転記の定義を設定するには、**転記の定義**ページで**予算**モジュールを選択します。 その後、**トランザクションの転記の定義**ページの**予算**領域で、予算コードを使用して、転記の定義を**元の予算**の予算タイプを持つ予算登録エントリに関連付けることができます。 

予算割り当ておよび転記の定義が有効な場合、予算登録のエントリは予算管理のために、一般会計に記録されます。

### <a name="posting-definition--match-criteria"></a>転記の定義 – 照合基準

| 勘定構造       | 照合勘定番号 | 優先順位 |
|-------------------------|----------------------|----------|
| 勘定構造 - P&L | \*                   | 1        |

* **照合勘定番号**フィールドの空白の値は、定義された勘定構造のすべての照合勘定が一致するルールの一部になります。

### <a name="posting-definition--generated-entries"></a>転記の定義 – 生成されたエントリ

| 勘定構造 | 生成された勘定番号              | 生成された借方/貸方 |
|-------------------|---------------------------------------|------------------------|
| 勘定構造 | 300145 - -(見積られた収益口座) | 同じ                   |
| 勘定構造 | 300146 - -(割り当て口座)     | バランスをとる              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>勘定、分析コード値、および金額を含むトランザクション

**予算登録エントリ** ページで、予算勘定項目の勘定、分析コード値、金額を入力します。

| 口座 + 分析コード           | デビット | クレジット | コメント |
|--------------------------------|-------|--------|---------|
| 606400-OU\_1-OU\_3566-トレーニング |       | 250.00 |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>転記の定義から生成された元帳エントリ

生成された元帳エントリは各分析コードの元の予算を記録するために作成されます。

| 口座 + 分析コード           | デビット  | クレジット | コメント |
|--------------------------------|--------|--------|---------|
| 300145-OU\_1-OU\_3566-トレーニング |        | 250.00 |         |
| 300146-OU\_1-OU\_3566-トレーニング | 250.00 |        |         |

この例では、勘定構造 - P&L の一部であるいずれかの口座が転記の定義の基準に一致します。 したがって、606400-OU\_1-OU\_3566-トレーニングが評価されると、生成された元帳エントリが作成されます。





