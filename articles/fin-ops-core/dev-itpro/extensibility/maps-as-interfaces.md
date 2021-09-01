---
title: インターフェイスとして使用されるテーブル マップの拡張
description: このトピックでは、インターフェイスとして使用されるテーブル マップを拡張する方法について説明します。
author: MichaelFruergaardPontoppidan
ms.date: 12/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 11
ms.openlocfilehash: 54ddf4e5a345d3e1bfba65b1c79732e48f2ef7a359484c68164efe6fb2aaf26c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729730"
---
# <a name="extend-table-maps-that-are-used-as-interfaces"></a>インターフェイスとして使用されるテーブル マップの拡張

[!include [banner](../includes/banner.md)]

**SalesPurchLine** および **SalesPurchTable** テーブル マップは、さまざまな製品機能により使用される一般的なフィールドおよびメソッドのセットを公開します。 フィールドのマッピングとメソッドの実装は、クラス階層にリファクタリングされています。 変更の一部は以下のとおりです。
- テーブル マップのメソッドは、クラス階層に移動されました。
- フィールドは、クラス階層で parm メソッドを通して公開されます。
- テーブル マップは引き続き存在し、テーブル マップへのマッピングも引き続き実装されていますが、テーブル マップのフィールドは廃止され、フィールド マッピングは削除されています。
- テーブル マップ上のメソッドは廃止されました。

## <a name="salespurchtableinterface-hierarchy"></a>SalesPurchTableInterface 階層

新しい **SalesPurchTableInterface** クラスは、**SalesPurchTable** テーブル マップのリファクタリングによって導入された ApplicationSuite 機能の抽象基本クラスです。 このクラスにはフィールドとメソッドの抽象メソッドが含まれています。これらはインターフェイスを実装する各テーブルに存在している必要があります。 これにより、メソッドに既定のロジックを含めることができ、すべての実装においてよく用いられます。 **SalesPurchTable** テーブル マップを実装する各テーブルは、**SalesPurchTableInterface** クラスの階層の派生クラスとして表す必要があります。 各派生クラスは、**SalesPurchTableInterfaceFactory** 属性クラスで修飾される必要があります。 属性を使用して派生クラスをテーブルに関連付けます。これで、**SalesPurchTable** レコードに応じて、適切なタイプのクラスのインスタンスを作成できるようになります。

![MapsAsInterfaces.](media/MapsAsInterfaces1.png)

テーブル マップ メソッドが廃止されたにもかかわらず、対応するメソッドはまだ実装テーブルに存在します。 これらのメソッドのロジックは、テーブル マップのメソッドへの呼び出しを階層の基本クラスの対応するメソッドにデリゲートすることからリファクタリングされています。

## <a name="extension-scenario"></a>拡張子シナリオ

この例では、ISVModule2 モデルによってインターフェイス クラス階層と **SalesPurchTable** テーブル マップを実装しているテーブルを拡張させる場合、次の手順を実行する必要があります。
1. **SalesPurchTable** テーブル マップを実装する必要なテーブルに、テーブル拡張機能を使用してフィールドとメソッドを追加します。
2. 新規のインターフェイス クラス階層を作成し、新しいフィールドを parm メソッドやその他の追加メソッドとして公開します。 クラス階層構造の基本クラスは、具体的であり、抽象的ではない必要があります。
3. 拡張された各テーブルの派生クラスを作成します。
    1. 各派生クラスを **SalesPurchTableInterfaceFactory** 属性クラスで修飾し、クラスを正しいテーブルに関連付けます。
    2. 新しいクラス階層の基本クラスに静的ファクトリ メソッドを作成します。 ファクトリ メソッドは、**SalesPurchTableInterfaceFactory** 属性を利用する適切な派生クラスをインスタンス化する必要があります。 派生クラスが見つからない場合は、基本クラスのインスタンスを戻す必要があります。
4. **SalesPurchTableInterface** クラスの拡張クラスを作成します。 このクラスは、**SalesPurchTableInterface** クラスを、新しいクラス階層のファクトリ メソッドを呼び出して新しいクラス階層からインスタンスを作成するメソッドで補強します。
    
上記のクラスと拡張機能は、次の図に示されています。

![MapsAsInterfacesWalkThrough.](media/MapsAsInterfaces2.png)

この図には、**SalesPurchTable** を実装する **ISV1Header** テーブルを含み、独自の **SalesPurchTableInterface** 派生クラスを含む ISVModule1 モデルが含まれています。 このモデルは ISVModule2 から独立しているため、ISVModule2 のロジックが、**ISV2SalesPurchTableInterface** クラス階層からインスタンスを作成すると、**SalesPurchTable** レコードが **ISV1Header** タイプの場合に基本クラスのインスタンスが返されます。 基本クラスのメソッドが、未知のテーブルに対して適切な結果を返す場合、同じインストール内で 2 つの ISV モデルが共存します。

## <a name="code-example"></a>コードの例

次のコード例は、テーブル マップを拡張する方法を示しています。

```xpp
[ExtensionOf(classStr(SalesPurchTableInterface))]
final public class ISV2SalesPurchTableInterface_Extension
{
    private ISV2SalesPurchTableInterface ISV2SalesPurchTableInterface;

    public ISV2SalesPurchTableInterface ISV2SalesPurchTableInterface()
    {
        if (!ISV2SalesPurchTableInterface)
        {
            ISV2SalesPurchTableInterface = ISV2SalesPurchTableInterface::createInstance(this);
        }

        return ISV2SalesPurchTableInterface;
    }

}

public class ISV2SalesPurchTableInterface
{

    SalesPurchTableInterface salesPurchTableInterface;

    private void initializeSalesPurchTableInterface(SalesPurchTableInterface _salesPurchTableInterface)
    {
        salesPurchTableInterface = _salesPurchTableInterface;
    }

    public SalesPurchTable parmSalesPurchTable()
    {
        return salesPurchTableInterface.parmSalesPurchTable();
    }

    protected void new()
    {
    }

    public static ISV2SalesPurchTableInterface createInstance(SalesPurchTableInterface _salesPurchTableInterface)
    {
        SalesPurchTableInterfaceFactoryAttribute attr = 
        new SalesPurchTableInterfaceFactoryAttribute(
            tableId2Name(_salesPurchTableInterface.parmSalesPurchTable().tableId));
        
        ISV2SalesPurchTableInterface instance = 
        SysExtensionAppClassFactory::getClassFromSysAttribute(classStr(ISV2SalesPurchTableInterface), attr) 
        as ISV2SalesPurchTableInterface;

        instance.initializeSalesPurchTableInterface(_salesPurchTableInterface);

        return instance;
    }

    public AccountingGroupId parmAccountingGroupId()
    {
        return '';
    }

}
[SalesPurchTableInterfaceFactoryAttribute(tableStr(SalesTable))]
public class ISV2SalesTableSalesPurchTable extends ISV2SalesPurchTableInterface
{
    private SalesTable parmSalesTable()
    {
        return this.parmSalesPurchTable();
    }

    public AccountingGroupId parmAccountingGroupId()
    {
        return this.parmSalesTable().AccountingGroupId;
    }

}

[SalesPurchTableInterfaceFactoryAttribute(tableStr(PurchTable))]
public class ISV2PurchTableSalesPurchTable extends ISV2SalesPurchTableInterface
{

    private PurchTable parmPurchTable()
    {
        return this.parmSalesPurchTable();
    }

    public AccountingGroupId parmAccountingGroupId()
    {
        return this.parmPurchTable().AccountingGroupId;
    }

}
```



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]