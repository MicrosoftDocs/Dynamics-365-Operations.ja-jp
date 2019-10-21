---
title: データ エンティティの列と仮想フィールドを計算する
description: この記事では、計算されたフィールドと仮想フィールドに関する情報を提供します。これは、データ エンティティが持つことができる 2 つのタイプのマッピングされていないフィールドです。
author: Sunil-Garg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 17891
ms.assetid: 88d230af-7d3d-49b3-bf19-69ecf81ed751
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1307987f98900e27a35e92b8fa16988a77c262db
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183432"
---
# <a name="computed-columns-and-virtual-fields-in-data-entities"></a>データ エンティティの列と仮想フィールドを計算する

[!include [banner](../includes/banner.md)]

この記事では、計算されたフィールドと仮想フィールドに関する情報を提供します。これは、データ エンティティが持つことができる 2 つのタイプのマッピングされていないフィールドです。 この記事には、マップされていないフィールドのプロパティに関する情報と、それらの作成、使用、テストの方法を示す例が含まれています。

サンプルコードは、ユーザーが所有しているソリューションの一部であるエンティティの作成または変更を行う用途で使用します。  既存のエンティティを拡張するには、若干の変更を加える必要があります。

## <a name="overview"></a>概要

データ エンティティは、データ ソースのフィールドに直接マップされているフィールド以外に*マップされていない*フィールドを追加で持つことができます。 マップされていないフィールドの値を生成するメカニズムは次のとおりです。

- カスタム X++ コード
- Microsoft SQL Server で実行される SQL

マップされていない2種類のフィールドは、計算と仮想です。 マップされていないフィールドは常に読み取り操作をサポートしますが、機能仕様では、書き込み操作をサポートするための開発作業は必要とされない場合があります。

### <a name="computed-field"></a>計算フィールド

- 値は、SQL ビューの計算列によって生成されます。
- 読み取り中に、データは SQL によって計算され、ビューから直接フェッチされます。
- 書き込みについては、カスタム X++ コードは入力値を解析し、データ エンティティの通常のフィールドに解析された値を書き込む必要があります。 値はエンティティのデータ ソースの通常のフィールドに格納されます。
- 計算フィールドは主に読み取りに使用されます。
- 可能であれば、計算された列は SQL Server レベルで計算されている一方、仮想フィールドは、X++ の行ごとに計算された行であるため、可能な限り仮想フィールドではなく計算された列を使用することをお勧めします。

### <a name="virtual-field"></a>仮想フィールド

- 保持されないフィールドです。
- カスタム X++ コードによって制御されます。
- 読み取り/書き込みは、カスタム X++ コードを通じて発生します。
- 仮想フィールドは 通常X++ コードを使用して計算される入力値に使用され、計算された列に置き換わることはできません。

### <a name="properties-of-unmapped-fields"></a>マップされていないフィールドのプロパティ

<table>
<thead>
<tr>
<th>カテゴリ</th>
<th>氏名</th>
<th>種類</th>
<th>既定値</th>
<th>動作</th>
</tr>
</thead>
<tbody>
<tr>
<td>データ</td>
<td>IsComputedField</td>
<td>NoYes</td>
<td>有</td>
<td><ul>
<li><strong>はい:</strong> - フィールドは、SQL ビューの計算済み列として同期されます。 列の SQL 定義文字列を計算するために X++ メソッドが必要です。 仮想列の定義は静的であり、エンティティが同期されているときに使用されます。 その後は、 X++ メソッドは、実行時に呼び出されません。</li>
<li><strong>いいえ</strong> - フィールドは、入庫および出荷の値がカスタム コードによって完全に制御される真の仮想フィールドです。</li>
</ul></td>
</tr>
<tr>
<td>データ</td>
<td>ComputedFieldMethod</td>
<td>文字列</td>
<td></td>
<td>フィールド定義を生成する SQL 式を構築するための X++ の静的 <strong>DataEntity</strong> メソッド。 プロパティ <strong>IsComputedField</strong> が <strong>いいえ</strong> に設定されている場合、このプロパティは無効で無関係です。 このメソッドは、プロパティ <strong>IsComputedField</strong> が <strong>はい</strong> に設定されている場合に必要です。</td>
</tr>
<tr>
<td>データ</td>
<td>ExtendedDataType</td>
<td>文字列</td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-create-a-computed-field"></a>例: 計算フィールドを作成
この例では、**FMCustomerEntity** エンティティに計算フィールドを追加します。 読み取りについては、このフィールドは、顧客の名前と住所を適切な形式に結合します。 書き込みについては、X++ コードは複合値を個別の名前および住所の値に解析し、それからコードが通常の名前や住所フィールドを更新します。

1. Microsoft Visual Studio で、プロジェクトを右クリックし、既存の **FMCustomerEntity** を追加します。
2. ソリューション エクスプローラーで、**FMCustomerEntity** ノードを右クリックしてから**開く**をクリックします。
3. **FMCustomerEntity** のデザイナービューで、 **Fields** ノードを右クリックし、 **New** &gt; **String Unmapped Field** とクリックします。

    [![新しくマップされていない文字列フィールドを作成](./media/computedcolumnsandvirtualfields11.png)](./media/computedcolumnsandvirtualfields11.png)

4. 新しいフィールドの名前を **NameAndAddress** に変更します。
5. 次のスクリーンショットに示すように、マッピングされていない **NameAndAddress** フィールドのプロパティを更新します。

    [![NameAndAddress のマップされていないフィールドのプロパティの更新](./media/computedcolumnsandvirtualfields21.png)](./media/computedcolumnsandvirtualfields21.png)

6. **FMCustomerEntity** &gt; **メソッド**に移動します。 **メソッド** ノードを右クリックし、**新規** をクリックします。 メソッド名が、マップされていない計算されたフィールドの **DataEntityView方法** のプロパティ値と一致していることを、確認します。
7. 次の X++ コードをメソッドに貼り付けます。 このメソッドは、結合されて書式設定された **NameAndAddress** 値を返します。

    > [!NOTE]
    > **サーバー**キーワードが必要です。

    ```
    private static server str formatNameAndAddress()   // X++
    {
        DataEntityName      dataEntityName= tablestr(FMCustomerEntity);
        List                fieldList = new List(types::String);
        ////Format name and address to look like following
        ////John Smith, 123 Main St, Redmond, WA 98052
        fieldList.addEnd(SysComputedColumn::returnField(DataEntityName, identifierstr(FMCustomer), fieldstr(FMCustomer, FirstName)));
        fieldList.addEnd(SysComputedColumn::returnLiteral(" "));
        fieldList.addEnd(SysComputedColumn::returnField(DataEntityName, identifierstr(FMCustomer), fieldstr(FMCustomer, LastName)));
        fieldList.addEnd(SysComputedColumn::returnLiteral("; "));
        fieldList.addEnd(SysComputedColumn::returnField(DataEntityName, identifierstr(FMAddressTable), fieldstr(FMAddressTable, AddressLine1)));
        fieldList.addEnd(SysComputedColumn::returnLiteral(", "));
        fieldList.addEnd(SysComputedColumn::returnField(DataEntityName, identifierstr(FMAddressTable), fieldstr(FMAddressTable, City)));
        fieldList.addEnd(SysComputedColumn::returnLiteral(", "));
        fieldList.addEnd(SysComputedColumn::returnField(DataEntityName, identifierstr(FMAddressTable), fieldstr(FMAddressTable, State)));
        fieldList.addEnd(SysComputedColumn::returnLiteral(", "));
        fieldList.addEnd(SysComputedColumn::cast(
            SysComputedColumn::returnField(DataEntityName, identifierstr(FMAddressTable), fieldstr(FMAddressTable, ZipCode)), "NVARCHAR"));
        return SysComputedColumn::addList(fieldList);
    }

    T-SQL for the computed column.

    ( Cast (( ( T1.firstname ) + ( N' ' ) + ( T1.lastname ) + ( N'; ' ) +
        ( T5.addressline1 )
        + ( N', ' ) + ( T5.city ) + ( N', ' ) + ( T5.state ) + (
        N', '
        ) +
        ( Cast(T5.zipcode AS NVARCHAR) ) ) AS NVARCHAR(100))
    )
    AS
    NAMEANDADDRESS
    ```

    > [!TIP]
    > 計算列のためにデータ エンティティの同期にエラーが発生した場合、X++ で使用する前に、Microsoft SQL Server Management Studio (SSMS) で SQL 定義を用意することは簡単です。

8. プロジェクトをリビルドします。
9. データベースを同期させます。 この手順を忘れないでください。 **Dynamics 365 &gt; データベースの同期 &gt; 同期**に移動することによりこれを実行することができます。

## <a name="example-create-a-virtual-field"></a>例: 仮想フィールドを作成
この例では、**FMCustomerEntity** エンティティに仮想フィールドを追加します。 このフィールドには、姓と名の組み合わせとしてフルネームが表示されます。 X++ コードは複合値を生成します。

1. **FMCustomerEntity** エンティティのデザイナーで、**フィールド**ノードを右クリックしてから、**新規 &gt; マップされていない文字列フィールド**をクリックします。
2. マップされていないフィールドのプロパティ ウィンドウで、**名前**プロパティを **FullName** に設定します。
3. **計算フィールドかどうか** プロパティ **いいえ** に設定します。 **DataEntityView メソッド**が空のままであることを確認します。

    [![マップされていないフィールドのプロパティの設定](./media/computedcolumnsandvirtualfields31.png)](./media/computedcolumnsandvirtualfields31.png)

4. **FMCustomerEntity** デザイナーで、**メソッド**ノードを右クリックしてから、**オーバーライド &gt; postLoad** とクリックします。 このメソッドの X++ コードは、仮想フィールドの値を生成します。
5. 次の X++ コードを **postLoad** オーバーライドに貼り付けます。 **postLoad** メソッドが **void** を返すことに注意します。

    ```
    public void postLoad()
    {
        super();
        //Populate virtual field once entity has been loaded from database
        //Format full name - "Doe, John"
        this.FullName = this.LastName + ", " + this.FirstName;
    }
    ```

6. プロジェクトをコンパイルします。

## <a name="example-use-a-virtual-field-to-receive-and-parse-an-inbound-field"></a>例: 受信フィールドを受信および解析する仮想フィールドを使用
外部システムが、システムに送信する 1 つのフィールドに姓と名を組み合わせた複合値として人物の名前を送信する場合を考えてみましょう。 ただし、システムは姓と名を個別に格納します。 このシナリオでは、作成した **FullName** 仮想フィールド使用することができます。 この例で、主要な追加は **mapEntityToDataSource** メソッドのオーバーライドです。 **更新**が呼び出されると、各データ ソースごとに **mapEntityToDataSource** メソッドが呼び出されます。

1. **FMCustomerEntity** のデザイナーで、**メソッド**ノードを右クリックしてから、**オーバーライド &gt; mapEntityToDataSource** とクリックします。
2. 次の X++ コードを **mapEntityToDataSource** メソッドに貼り付けます。

    ```
    public void mapEntityToDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)
    {
        super(entityCtx, dataSourceCtx);
        //Check if desired data source context is available
        if (dataSourceCtx.name() == "FMCustomer")
        {
            FMCustomer dsCustomer = dataSourceCtx.getBuffer();
            //Find position of "," to parse full name format "Doe, John"
            int commaPosition = strfind(this.FullName, ",",0,strlen(this.FullName));
            //Update FirstName and LastName in the data source buffer to update
            dsCustomer.LastName = substr(this.FullName,0,commaPosition-1);
            dsCustomer.FirstName = substr(this.FullName, commaPosition+1, strlen(this.FullName));
        }
    }
    ```

## <a name="test-the-computed-and-virtual-fields"></a>計算フィールドと仮想フィールドのテスト
次の **main** メソッドは、計算フィールドと仮想フィールドをテストします。 両方のフィールドは読み取りアクションでテストされ、仮想フィールドは更新アクションでテストされます。

1. この例では、**フリート管理 (移行済)** というデータ セットがあることを確認します。 データ セットはブラウザーのダッシュボードから利用できます。 右上隅にあるメニュー アイコンをクリックし、**アプリのリンク** メニューをクリックしてスクロールし、**フリート管理 (移行)** という名前のデータセットを見つけます
2. 次の X++ コードをプロジェクトのスタートアップ オブジェクトに貼り付けます。 プロジェクトを実行します。

    ```
    public static void main(Args _args)   // X++
    {
        FMCustomerEntity customer;
        //Using transactions to avoid committing updates to database
        ttsbegin;
        //SELECT single customer entity record from the database
        select customer
            where customer.Email == "phil.spencer@adatum.com";
        //Read full name (Virtual Field)
        info(customer.FullName);
        //Read formatted NameAndAddress(computed Field)
        info(customer.NameAndAddress);
        //UPDATE full name (virtual field)
        customer.FullName = "Doe, John";
        customer.update();
        //Reselect data from database to get updated information
        select customer
            where customer.Email == "phil.spencer@adatum.com";
        //Read full name (virtual field)
        info(customer.FullName);
        ttsabort;
    }
    ```
