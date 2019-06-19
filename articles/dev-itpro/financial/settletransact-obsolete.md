---
title: CustTrans::settleTransaction を使用したトランザクションの決済
description: このトピックでは、新しいCustTrans::settleTransactionメソッドについて説明を行い、CustTrans::settleTransact には実装されていない新機能について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 25631
ms.assetid: 0090efe3-3fd8-4988-83df-745d25b063d3
ms.search.region: Global
ms.author: markskun
ms.search.validFrom: 2019-06-01
ms.dyn365.ops.version: AX 10.0.4
ms.openlocfilehash: 1368d58d3d0dcaeefe4531ce40a49c499d5eeac9
ms.sourcegitcommit: c576b81dc3c93c09fb08fb0ba0c19f417360c5ab
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/05/2019
ms.locfileid: "1620474"
---
# <a name="settle-transactions-by-using-custtranssettletransaction"></a>CustTrans::settleTransaction を使用したトランザクションの決済

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="custtranssettletransact-is-obsolete"></a>CustTrans::settleTransact が過去のものに

CustTransテーブルの **settleTransact** メソッドが刷新されます。

```X++
public static boolean settleTransact(
CustTable _custTable,
    LedgerVoucher _ledgerVoucher = null,
    boolean _balancePostingProfile = true,
    SettleDatePrinc _saveDatePrinciple = SettleDatePrinc::DateOfPayment,
    TransDate _saveDate = dateNull()
    ,DimSettlementType_RU _dimSettlementType = DimSettlementType_RU::None
    ,CustTrans _parentCustTrans = null)
```

### <a name="why-is-it-marked-as-obsolete"></a>なぜ刷新される必要があるのか。

同じ顧客に対して複数の決済が同時に行われると、データベースのブロックが発生します。 データベースのブロックはパフォーマンスの低下につながります。

### <a name="what-does-the-method-do"></a>このメソッドによってできること

**settleTransact** メソッドでは、特定の顧客に対する一連の請求書と支払の決済を行います。 決済処理では、SpecTrans テーブルの **SpecCompany**、 **SpecTableId**、 **SpecRecId** 列を使用して一連の請求書を識別します。 同時に、これらの列によって決済コンテキストが定義されます。

**settleTransact** メソッドの **\_custTable** パラメータが、決済コンテキストをCustTable **DataAreaId**, **TableId**, **RecId** の値として定義します。 次の例は、2つのコンテキストを示しています。

| SpecCompany | SpecTableId | SpecRecId | 取引 |
|---|---|---|---|
| USMF | 7589 | 22565451428 | 1 |
| USMF | 7589 | 22565451428 | 2 |

## <a name="replacement-method"></a>メソッドの更新

CustTrans テーブル **settleTransaction** メソッドが メソッドの更新を行います。

```X++
public static boolean settleTransaction(
    SpecTransExecutionContext _specTransExecutionContext,
    CustTransSettleTransactionParameters _parameters)
```

### <a name="how-blocking-will-be-avoided"></a>ブロックがどのように回避されるか

それぞれの顧客の決済に固有の決済コンテキストが付与されます。 決済にはそれぞれ固有のコンテキストが割り当てられるため、どのトランザクションもブロックを引き起こすことがなくなります。  次の例は、2つのコンテキストを示しています。 各コンテキストには一意の **SpecRecId** 値を持っています。

| SpecCompany | SpecTableId | SpecRecId | 取引 |
|---|---|---|---|
| USMF | 7599 | 68719604825 | 1 |
| USMF | 7599 | 68719604826 | 2 |
    
### <a name="replacement-method-parameters"></a>メソッドのパラメーターを更新する

**SpecTransExecutionContext** クラスは、一意となる決済の実行コンテキストを定義します。 これは2つの部分で構成されています。 一つ目の部分は、決済の顧客または仕入先を定義します。 2つ目の部分では、決済のソースを定義します。

+ **newFromSource** メソッドには、顧客、仕入先、およびソースが必要となります。 顧客、仕入先、ソースは常に顧客となります。

    ```X++
    public static SpecTransExecutionContext newFromSource(
        CustVendTable _custVendTable, 
        Common _source = _custVendTable)
    ```

+ **parmSpecContext** メソッドは、生成された決済コンテキストを公開します。

    ```X++
    public Common parmSpecContext()
    ```

**CustTransSettleTransactionParamters** には、他のメソッドパラメータが含まれています。 これに含まれるコンストラクターメソッドは、既定値を使用してクラスの初期化を行います。 その一例として **LedgerVoucher** が挙げられます。

### <a name="how-to-use-the-settletransaction-method"></a>settleTransaction メソッドの使用方法

決済は2つの部分で行われます。 はじめに、決済処理に向けて請求書と支払を選び出します。 次に、決済処理を行います。

#### <a name="obsolete-code-example"></a>古いコードの例

```X++
//Mark for settlement
SpecTransManager specTransManager = SpecTransManager::construct(custTable);

specTransManager.insert(…) //Invoice(s)
specTransManager.insert(…) //Payment(s)

//Settle
CustTrans::settleTransact(recipientCustVendTable);
```

#### <a name="new-code-example"></a>新しいコードの例

```X++
//Mark for settlement
SpecTransExecutionContext specTransExecutionContext = SpecTransExecutionContext::newFromSource(custTable);
specTransManager = SpecTransManager::construct(specTransExecutionContext.parmSpecContext());

specTransManager.insert(…) //Invoice(s)
specTransManager.insert(…) //Payment(s)

//Settle
CustTrans::settleTransaction(
    specTransExecutionContext,
    CustTransSettleTransactionParameters::construct());
```

### <a name="testing"></a>テスト

この機能はフライトを使用します。 このテストを行うには、非稼働環境にてフライトを有効にする必要があります。 非稼動環境でフライトをオンにする方法については、 [データ管理でフライトされる機能とフライトされた機能の有効化](../data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features).を参照してください。

フライトの名称は **EnableCustTransSettleTransaction**です。
