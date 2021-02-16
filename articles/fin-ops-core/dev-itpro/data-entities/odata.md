---
title: データ プロトコル (OData) を開く
description: このトピックでは、Open Data Protocol (OData) に関する情報を提供し、OData V4 を使用して更新可能なビューを公開する方法について説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 06/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 24841
ms.assetid: 7137b0a0-1473-4134-b769-ede5e07fd6f5
ms.search.region: Global
ms.search.industry: ''
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ebf3ff4296307aec323daba9f3db9e7871780c1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688059"
---
# <a name="open-data-protocol-odata"></a>データ プロトコル (OData) を開く

[!include [banner](../includes/banner.md)]

このトピックでは、Open Data Protocol (OData) に関する情報を提供し、OData V4 を使用して更新可能なビューを公開する方法について説明します。

## <a name="what-is-odata"></a>OData とは
OData は、データを作成および消費するための標準プロトコルです。 OData の目的は、作成、読み取り、更新、削除 (CRUD) 操作のための Representational State Transfer (REST) に基づくプロトコルを提供することです。 OData は、さまざまなプログラムからの情報にアクセスするために、HTTP および JavaScript Object Notation (JSON) などの Web テクノロジーを適用します。 OData には次のメリットがあります。

- これにより、開発者は RESTful Web サービスを使用してデータを操作できます。
- これにより、見つけやすい方法でデータを共有する簡単で一貫した方法が提供されます。
- 製品を越えた広範な統合を有効にします。
- HTTP プロトコル スタックを使用して統合を有効にします。

OData の詳細については、次の Web ページを参照してください。

| トピック                                                               | Webpage                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------|
| OData 標準                                                     | <https://www.odata.org/documentation/>                   |
| OData: Web、クラウド、モバイル デバイスなどのデータ アクセス | <https://docs.microsoft.com/aspnet/web-api/overview/odata-support-in-aspnet-web-api/>    |

パブリック OData サービス エンドポイントにより、幅広いクライアントにわたって、一貫した方法でデータにアクセスできるようになります。 公開されているすべてのエンティティの一覧を表示するには、OData サービスのルート URLを開きます。 システムのサービス ルートの URL の形式は **\[お客様の組織のルート URL\]/data** です。

> [!NOTE]
> 拡張機能を介して追加された OData アクションは、現在サポートされていません。

## <a name="addressing"></a>アドレス指定
次のテーブルでは、フリート管理サンプルのリソースと対応する URL を示しています。


| リソース            | URL                                                                     | 説明                                                    |
|---------------------|-------------------------------------------------------------------------|----------------------------------------------------------------|
| サービス エンドポイント    | \[組織のルート URL\]/data/                                  | OData エンティティのルート サービス エンドポイント                   |
| エンティティ コレクション   | \[組織のルート URL\]/data/Customers                         | すべての顧客のコレクション                                |
| エンティティ              | \[組織のルート URL\]/data/Customers("\[キー\]")              | エンティティのコレクションから 1 つのエンティティ                     |
| ナビゲーション プロパティ | \[組織のルート URL\]/data/Customers("\[キー\]")/Reservations | 顧客からその顧客の引当までのナビゲーション |
| プロパティ            | \[組織のルート URL\]/data/Customers("\[キー\]")/FirstName    | 顧客の名                                      |

## <a name="odata-services"></a>OData サービス
OData REST エンドポイントを提供します。 このエンドポイントは、アプリケーション オブジェクト ツリー (AOT) の **IsPublic** としてマークされているすべてのデータ エンティティを公開します。 ユーザーがデータを挿入およびシステムから取得するために使用できる完全な CRUD (作成、取得、更新、および削除) 機能をサポートしています。 この機能の詳細なラボは、LCS の方法論に基づいています。

> [!NOTE]
> OData を使用してデータ エンティティを操作する場合、OData 呼び出しを正常に実行するには、エンティティ キーのすべてのフィールドを指定する必要があります。

OData サービスを使用するためのコード例については、[Microsoft Dynamics AX 統合 GitHub リポジトリ](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/ODataConsoleApplication)を参照してください。

### <a name="supported-features-from-the-odata-specification"></a>OData 仕様からサポートされている機能

[OData 仕様](https://docs.oasis-open.org/odata/odata/v4.0/odata-v4.0-part1-protocol.html) に従って、OData サービスで使用可能な上位レベルの機能は次のとおりです.

- CRUD サポートは、転記、パッチ、挿入、および削除の HTTP 動詞サポートにより処理されます。
- 利用可能なクエリ オプションは

    - $filter
    - $count
    - $orderby
    - $skip
    - $top
    - $expand (第 1 レベルの展開のみがサポートされます)
    - $select

- OData サービスでは、最大ページ サイズが 10,000 のサービス ドリブン ページングをサポートします。

詳細については、以下を参照してください: [エンティティにバインドされている OData アクション](https://docs.oasis-open.org/odata/odata/v4.0/errata02/os/complete/part1-protocol/odata-v4.0-errata02-os-part1-protocol-complete.html#_Toc406398355)

#### <a name="filter-details"></a>フィルター詳細

$filter には組み込みの演算子があります。

- 等しい (eq)
- 等しくない (ne)
- より大きい (gt)
- 等しい 、またはより大きい (ge)
- より小さい (lt)
- 等しい 、またはより小さい (le)
- かつ
- 又は
- ない
- 加算 (add)
- 減算 (sub)
- 乗算 (mul)
- 除算 (div)
- 小数点除算 (divby)
- 剰余 (mod)
- 優先順位のグループ化 ({ })

また、**Contains** オプションを $filter 要求とともに使用することができます。 これは、ワイルドカード文字として実装されています。 例: `http://host/service/EntitySet?$filter=StringField eq '\*retail\*'`

「持つ」 と 「含む」 の演算子には対応していません。

詳細については、「[OData 演算子](https://docs.oasis-open.org/odata/odata/v4.0/errata02/os/complete/part2-url-conventions/odata-v4.0-errata02-os-part2-url-conventions-complete.html#_Toc406398096)」を参照してください。

#### <a name="batch-requests"></a>バッチ要求
OData サービスでは、バッチ要求がサポートされています。 詳細については、「[OData バッチ要求](https://docs.oasis-open.org/odata/odata/v4.0/errata02/os/complete/part1-protocol/odata-v4.0-errata02-os-part1-protocol-complete.html#_Toc406398359)」を参照してください。

#### <a name="metadata-annotations"></a>メタデータの注釈

/data/$ メタデータは、注釈を提供します。 EnumType は、$metadata でサポートされます。

![EnumType メタデータ](./media/metadata.png)

### <a name="cross-company-behavior"></a>会社間動作

既定では、OData はユーザーの既定の会社に属しているデータのみを返します。 ユーザーの既定の会社以外のデータを表示するには、**?cross-company=true** クエリ オプションを指定します。 このオプションは、ユーザーがアクセスできるすべての会社のデータを返します。

**例:** `http://[baseURI\]/data/FleetCustomers?cross-company=true`

既定の会社ではない特定の会社ごとにフィルター処理するには、次の構文を使用します。

`http://[baseURI\]/data/FleetCustomers?$filter=dataAreaId eq 'usrt'&cross-company=true`

### <a name="validate-methods"></a>メソッドの検証

次のテーブルは、OData スタックが対応するデータ エンティティで暗黙的に呼び出す検証方法を示します。

<table>
<thead>
<tr>
<th>OData</th>
<th>メソッド (呼び出される順序で一覧表示されます)</th>
</tr>
</thead>
<tbody>
<tr>
<td>新規</td>
<td><ol>
<li><strong>クリア ()</strong></li>
<li><strong>Initvalue()</strong></li>
<li><strong>PropertyInfo.SetValue()</strong> 要求の指定されたすべてのフィールド</li>
<li><strong>Validatefield()</strong></li>
<li><strong>Defaultrow</strong></li>
<li><strong>Validatewrite()</strong></li>
<li><strong>書き込み ()</strong></li>
</ol></td>
</tr>
<tr>
<td>更新</td>
<td><ol>
<li><strong>Forupdate()</strong></li>
<li><strong>再表示 ()</strong></li>
<li><strong>クリア ()</strong></li>
<li><strong>Initvalue()</strong></li>
<li><strong>PropertyInfo.SetValue()</strong> 要求の指定されたすべてのフィールド</li>
<li><strong>Validatefield()</strong></li>
<li><strong>Defaultrow()</strong></li>
<li><strong>Validatewrite()</strong></li>
<li><strong>書き込み ()</strong></li>
</ol></td>
</tr>
<tr>
<td>消去</td>
<td><ol>
<li><strong>Forupdate()</strong></li>
<li><strong>再表示 ()</strong></li>
<li><strong>checkRestrictedDeleteActions()</strong></li>
<li><strong>Validatedelete()</strong></li>
<li><strong>削除 ()</strong></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="exposing-odata-entities"></a>OData エンティティを公開
OData エンティティは、更新可能なビューの概念に基づいています。 更新可能なビューの **IsPublic** プロパティが **TRUE** 設定されているとき、そのビューは最上位レベルの OData エンティティとして公開されます。

## <a name="setting-navigation-properties-between-odata-entities"></a>OData エンティティ間のナビゲーション プロパティの設定
OData エンティティ間のリンクは、ナビゲーション プロパティによって記述されます。 ナビゲーション プロパティでは、アソシエーションの一方から他方までのナビゲーションについて説明します。

#### <a name="adding-actions-on-odata-entities"></a>OData エンティティでのアクションの追加
アクションで動作をデータ モデルに挿入できます。 アクションを追加するには、更新可能なビューにメソッドを追加し、そのメソッドを特定の属性で修飾します。 次に例を示します。

```xpp
[SysODataActionAttribute("CalcMaintenanceDuration", true)]
public int CalculateMaintenanceDuration()
{
    //do something
    return 0;
}
```

この例では、**SysODataActionAttribute** クラスがアクションとして公開されている **CalculateMaintenanceDuration** メソッドを修飾します。 属性の最初の引数は公開されているアクションの名前で、2 番目の引数はこのアクションが常に利用可能かどうかを示します。 アクションとして公開されているメソッドは、任意のプリミティブ型または別のパブリックの更新可能なビューを返すことができます。 このメソッドが公開されると、OData $ メタデータに表示されます。 次に例を示します。

```xml
<Action Name="CalcMaintenanceDuration" IsBound="true">
    <Parameter Name="ViewMaintenance" Type="Microsoft.Dynamics.AX.Resources.ViewMaintenance"/>
    <ReturnType Type="Edm.String" />
</Action>
```

次の OData アクションの例では、パラメーターで取り、リストを返します。

```xpp
[SysODataActionAttribute("GetColors", true),
    SysODataCollectionAttribute("return", Types::Record, "CarColor")]
public List GetColorsByAvailability(boolean onlyAvailableVehicles)
{
    List returnList = new List(Types::Record);
    // do something
    return returnList;
}
```

この例では、OData は **SysODataCollectionAttribute** クラスによって X++ から強く定型化されたコレクションを公開できます。 このクラスは次の 3 つのパラメーターを取ります。

- リストを示すパラメーターの名前 (メソッドの戻り値として **return** を返します)。
- この一覧のメンバーの X++ タイプ
- コレクションに含まれている OData リソースのパブリック名

これらのアクションが公開された後、サービス ルートの URL から呼び出すことができます。

ソース コード内の **SysODataActionAttribute** 属性を検索することにより、データ エンティティ上で定義されたアクションを見つけることができます。

## <a name="querying-or-browsing-an-odata-endpoint"></a>OData エンドポイントの照会や参照
OData は、データベースに対して豊富なクエリを作成できる SQL に似た言語を有効にして、結果に希望するデータ項目のみが含まれるようにします。 クエリを作成するには、リソース パスに条件を追加します。 たとえば、ブラウザで次のクエリ オプションを加えることによって、**顧客** エンティティ コレクションのクエリを行うことができます。

| URL                                                                        | 説明 |
|----------------------------------------------------------------------------|-------------|
| \[組織のルート URL\]/data/Customers                            | すべての顧客の一覧を表示します。 |
| \[組織のルート URL\]/data/Customers?$top=3                     | 最初の 3 つのレコードを一覧表示します。 |
| \[組織のルート URL\]/data/Customers?$select=FirstName,LastName | すべての顧客の一覧を表示しますが、姓名のプロパティだけを表示します。 |
| \[組織のルート URL\]/data/Customers?$format=json               | JavaScript クライアントとやり取りするために使用できる JSON 形式ですべての顧客の一覧を表示します。 |

OData プロトコルは、エンティティで多くの似たフィルター処理とクエリ オプションをサポートします。 クエリ オプションの完全なセットについては、[Windows Communication Foundation](https://msdn.microsoft.com/library/ff478141.aspx) を参照してください。

## <a name="using-enums"></a>列挙型の使用
列挙型は、名前空間 **Microsoft.Dynamics.DataEntities** の下にあります。 OData クエリに列挙型を含めるには、次の構文を使用します。

`Microsoft.Dynamics.DataEntities.Gender'Unknown'`

`Microsoft.Dynamics.DataEntities.NoYes'Yes'`

上記の列挙型の値を使用したクエリの例を次に示します。

`https://environment.cloud.onebox.dynamics.com/data/CustomersV3?\$filter=PersonGender eq Microsoft.Dynamics.DataEntities.Gender'Unknown'`

`https://environment.cloud.onebox.dynamics.com/data/Currencies?\$filter=ReferenceCurrencyForTriangulation eq Microsoft.Dynamics.DataEntities.NoYes'No'`

列挙型に対応している演算子は **eq** と **ne** です。

## <a name="authentication"></a>認証
OData は、サーバーと同じ認証スタック上に配置されます。 認証の詳細については、 [サービス エンドポイントの概要](services-home-page.md) を参照してください。

## <a name="tips-and-tricks"></a>ヒントや秘訣

### <a name="run-multiple-requests-in-a-single-transaction"></a>1 つのトランザクションで複数の要求を実行
OData バッチ フレームワークは、*変更セット* を使用します。 各変更セットには、単一アトミック ユニットとして扱われるべき要求のリストが含まれています。 つまり、すべての要求が正常に実行されるか、要求が失敗した場合はすべての要求が正常に実行されません。 次の例は、単一の変更セット内に要求のリストを持つバッチ要求を送信する方法を示しています。

**SaveChanges()** の **SaveChangesOptions.BatchWithSingleChangeset** オプションを使用すると、単一の変更セットにすべての要求がバンドルされていることを保証できます。

```xpp
public static void CreateProductColors(Resources context)
{
    var productColorsCollection = new DataServiceCollection<ProductColor>(context);

    var color1 = new ProductColor();
    productColorsCollection.Add(color);
    color1.ColorId = "New Color1"; // set any other properties needed

    var color2 = new ProductColor();
    productColorsCollection.Add(color1);
    color2.ColorId = "New Color2"; // set any other properties needed

    context.SaveChanges(SaveChangesOptions.BatchWithSingleChangeset);
}
```

### <a name="prevent-unset-records-from-being-posted-when-you-use-an-odata-client"></a>OData クライアントを使用する場合に設定されていないレコードが転記されることを防止する
例 1 に示すように、OData クライアントを使用して新しいレコードを作成するときは、設定されていないプロパティが要求の本体に含まれ、既定値がそれらのプロパティに割り当てられます。 この動作を回避し、明示的に設定されたプロパティのみをポストするには、例 2 に示すように、**SaveChanges()** の **SaveChangesOptions.PostOnlySetProperties** オプションを使用します。

**例 1**

```xpp
public static void CreateVendor(Resources context)
{
    var vendorCollection = new DataServiceCollection<Vendor>(context);
    var vendor = new Vendor();
    vendorCollection.Add(vendor);
    // set properties
    context.SaveChanges();
}
```

**例 2**

```xpp
public static void CreateVendor(Resources context)
{
    var vendorCollection = new DataServiceCollection<Vendor>(context);
    var vendor = new Vendor();
    vendorCollection.Add(vendor);
    // set properties

    // Save specifying PostOnlySetProperties flag
    context.SaveChanges(SaveChangesOptions.PostOnlySetProperties);
}
```

### <a name="handling-duplicate-names-between-enums-and-entities-in-metadata"></a>メタデータ内の列挙とエンティティ間の重複する名前の処理
列挙とエンティティが同じ名前を共有する場合があります。 この名前の重複により、OData クライアント コードの生成エラーが発生します。 このエラーから回復するには、削除しなければならない重複する名前のインスタンスを識別するために [GitHub のヘルパー コード](https://github.com/Microsoft/Dynamics-AX-Integration/blob/master/ServiceSamples/ODataConsoleApplication/MetadataDocumentValidator.cs) を使用できます。 生成されたメタデータ ドキュメントは、クライアント側で OData ロジック のより詳細な処理をするために使用することができます。

### <a name="array-fields"></a>配列フィールド
OData はエンティティで配列フィールドをサポートしていません。 OData で使用されるエンティティを設計するときにこれを考慮する必要があります。

### <a name="after-restarting-aos-the-first-odata-call-may-take-a-long-time-to-process"></a>AOS を再起動した後、最初の OData 呼び出しの処理に時間がかかることがあります
メタデータがキャッシュされていないために、再起動された AOS によって処理される最初の OData 呼び出しは処理に時間がかかる場合があります。 この待ち時間は、AOS 起動時に OData をウォーム アップすることで回避できます。 詳細については、[AOS 起動時に OData メタデータ キャッシュを作成する](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/odata-warmup) を参照してください。
