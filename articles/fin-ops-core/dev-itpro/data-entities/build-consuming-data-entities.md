---
title: データ エンティティのビルドおよび使用
description: このチュートリアルでは、エンティティを構築する方法と、統合シナリオで一部のアウト・オブ・バンド (OOB) エンティティを使用する方法を示します。
author: Sunil-Garg
manager: AnnBe
ms.date: 03/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 77523
ms.assetid: 1de997fb-d5c4-4668-9759-0758d141a3eb
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2642832d12801ab4e10ffc6d68f3817f4b184384
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172294"
---
# <a name="build-and-consume-data-entities"></a>データ エンティティのビルドおよび使用

[!include [banner](../includes/banner.md)]

このチュートリアルでは、エンティティを構築する方法と、統合シナリオで一部のアウト・オブ・バンド (OOB) エンティティを使用する方法を示します。 データのインポートとエクスポート、統合、および OData サービスなどのさまざまな統合シナリオで、これらのデータ エンティティが使用される方法もプレビューされます。

最初のエンティティを構築する準備が整ったら、次の作業を行う必要があります。
- 独自のパッケージとモデルを作成します。 詳細については、[モデルとパッケージ](../dev-tools/models.md) を参照してください。
- 新しいプロジェクトを作成し、作成したばかりのプロジェクトにモデル プロパティを設定します。

## <a name="prerequisites"></a>必要条件
このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングする必要があります。

このチュートリアルでは、baseUrl はインスタンスのベース URL を指します。

- クラウド環境では、ベース URL は Microsoft Dynamics Lifecycle Services (LCS) から取得されます。
- [ローカル仮想マシン (VM)](../dev-tools/access-instances.md#vm-that-is-running-on-premises) の、基準 URL は `https://usnconeboxax1aos.cloud.onebox.dynamics.com` です。
- FMLab サンプル コードを C: にダウンロードします。 詳細については、[FMLab サンプル コード](https://github.com/Microsoft/FMLab) を参照してください。

## <a name="key-concepts"></a>重要な概念
- Microsoft Visual Studio のデータ エンティティの開発
- データ管理および OData サービスのデータ エンティティを有効化
- 統合シナリオでデータ エンティティを消費する

## <a name="business-problem"></a>ビジネスの問題
フリート管理は、FMCustomer table テーブルに顧客データを、FMAddressTable テーブルにアドレス データを格納します。 顧客情報にアクセスまたは更新するには、複数のテーブルにアクセスする必要があります。 代わりに、機能的に顧客情報を表し、統合ソリューションを構築するために使用できるビジネス オブジェクトを作成することができます。

## <a name="building-the-fmlabcustomer-entity"></a>FMLabCustomer エンティティの作成
このセクションでは、フリート管理モデルで FMLabCustomer のデータ エンティティを作成する必要があります。 このエンティティは、インポート/エクスポートおよび統合サービスを通じてマスター データを管理するために使用されます。 プライマリ データ ソースが FMCustomer で、セカンダリ データ ソースが FMAddressTable です。

### <a name="data-entity"></a>データ エンティティ

FMLabCustomerEntity

#### <a name="data-entity-fields"></a>データ エンティティ フィールド

| 氏名          | マッピング                     |
|---------------|-----------------------------|
| CellPhone     | FMCustomer.CellPhone        |
| DriverLicense | FMCustomer.DriverLicense    |
| 電子メール         | FMCustomer.Email            |
| 名     | FMCustomer.FirstName        |
| 姓      | FMCustomer.LastName         |
| CustomerGroup | FMCustomer.CustGroup        |
| AddressLine1  | FMAddressTable.AddressLine1 |
| AddressLine2  | FMAddressTable.AddressLine2 |
| 市町村          | FMAddressTable.City         |
| 行政単位 (区画)         | FMAddressTable.State        |
| ZipCode       | FMAddressTable.ZipCode      |
| 国       | FMAddressTable.Country      |

#### <a name="corresponding-staging-table"></a>対応するステージング テーブル

ステージング テーブルは、ファイルの解析と変換時に中間ストレージを提供するため、インポート/エクスポートのシナリオで使用されます。 これらのテーブルは、コネクター統合シナリオでも使用されます。 多くの場合、ステージング テーブルはエンティティに対して 1 対 1 でマップされます。 **FMLabCustomerEntity** エンティティに対応するステージング テーブルの名前は FMLabCustomerStaging です。

### <a name="create-a-new-project"></a>新しいプロジェクトの作成

1. Visual Studio で、**ファイル** &gt; **新規** &gt; **プロジェクト**をクリックして、**Finance and Operations プロジェクト**を選択します。
2. プロジェクトを右クリックして **プロパティ** をクリックし、プロジェクトがフリート管理モデルであることを確認します。 設定されていない場合、**モデル** プロパティを**フリート管理**に設定します。

### <a name="add-a-new-data-entity-to-your-project"></a>プロジェクトへの新しいデータ エンティティの追加

1. **FMLabCustomerEntity** という名前の新しいエンティティを作成します。 プロジェクトを右クリックし、**追加** &gt; **新しい項目** をクリックします。 **新しい項目の追加** ダイアログ ボックスが開きます。
2. **データ エンティティ** を選択し、**名前** プロパティを **FMLabCustomerEntity** に設定します。
3. **追加** をクリックします。
4. **データ エンティティ** ウィザードで、作成しているデータ エンティティのプロパティを指定します。 次のスクリーン ショットに表示される値を使用します。

    > [!NOTE]
    > エンティティの名前に '\_' や数字 (0...9) を使用することはできません。 これらの文字を使用すると、後でマッピング エラーが発生することがあります。

    [![データ エンティティ ウィザード](./media/data-entity-wizard.png)](./media/data-entity-wizard.png)

5. **次へ** をクリックします。 各プロパティ機能の詳細については、 [データ エンティティ の概要](data-entities.md) 内の「エンティティのカテゴリ」および「エンティティの作成」を参照してください。
6. 次のスクリーン ショットに示すように、データ ソースから新しいエンティティにフィールドを追加します。 主要なデータ ソース、**FMCustomer** からフィールドを追加することができます。 このエンティティについては、テストを効率化するため**画像**および **LicenseImage** コンテナー タイプのチェック ボックスをオフにします。
7. データ エンティティのフィールドの名前を、パブリック データ コントラクト標準を反映するように変更するか、**ラベルをフィールド名に変換** をクリックして既存のラベルから名前を生成します。
8. **DriverLicense** フィールドの行で、**必須**チェック ボックスを選択します。 このフィールドはエンティティのナチュラル キーとして使用されます。

    [![データ エンティティ ウィザード 2](./media/data-entity-wizard-2.png)](./media/data-entity-wizard-2.png)

9. **データ ソース** フィールドで、**PrimaryAddress** を選択します。 **AddressID** の自動拡張または代理外部キー交換のため、**PrimaryAddress** データ ソースが自動的に追加されることに注意します。

    [![手順およびフィールドの追加](./media/steps-and-add-fields.png)](./media/steps-and-add-fields.png)

10. エンティティの一部にする **PrimaryAddress** データ ソースからフィールドを選択します。 また、次のフィールドの名前を変更して、適切な公開データ契約の名前付けを反映します。

    - PrimaryAddress \_AddressLine1 &gt; AddressLine1
    - PrimaryAddress \_AddressLine2 &gt; AddressLine2
    - PrimaryAddress \_City &gt; City
    - PrimaryAddress \_State &gt; State
    - PrimaryAddress \_ZipCode &gt; ZipCode
    - PrimaryAddress \_Country &gt; Country

    ![データ エンティティ ウィザード](./media/data-entity-wizard-3.png)

11. **完了** をクリックします。 データ エンティティの品目およびステージング テーブルは、プロジェクトに追加されます。

    [![ソリューション エクスプローラー](./media/solution-explorer.png)](./media/solution-explorer.png)

### <a name="build-your-project"></a>プロジェクトの構築

1. ソリューション エクスプローラーで、プロジェクトを右クリックしてから**プロパティ**をクリックします。
2. **ビルドでのデータベースの同期**プロパティの値を **True** に変更し、**OK** をクリックします。 このプロパティは、プロジェクトごとに 1 回のみ設定する必要があります。

    > [!NOTE]
    > エンティティが Microsoft SQL Server のビューとして作成され、ステージング テーブルが追加されます。 したがって、エンティティを作成するときにデータベースを同期する必要があります。

    ![プロパティ ページ](./media/property-pages.png)

3. Visual Studio ツールバーで、**構築** &gt; **ソリューションの構築** の順にクリックしてプロジェクトを構築します。
4. ビルドにエラーが含まれていないことを確認します。 この時点でチュートリアルは警告が許可されています。

### <a name="visually-validate-and-customize-an-entity"></a>目視による検証とエンティティのカスタマイズ

1. ソリューション エクスプローラーで、**FMLabCustomerEntity** ノードを右クリックしてから**開く**をクリックします。 エンティティのデザイナーが中央のウィンドウに開きます。
2. **FMLabCustomerEntity** エンティティのプロパティを検証します。 ソリューション エクスプ ローラーでエンティティを選択し、**プロパティ** ウィンドウの値と次のスクリーンショットを比較します。
3. **ラベル** プロパティを **フリート ラボ顧客** に設定します。

    [![FMLabCustomerEntity - プロパティ](./media/fmlabcustomerentity-properties.png)](./media/fmlabcustomerentity-properties.png)

4. 左ウィンドウで、**データ ソース** &gt; **FMCustomer** &gt; **データ ソース** &gt; **FMAddressTable** をクリックします。
5. **読み取り専用**プロパティを**いいえ**に変更します。 これは、既知の問題です。 最終的に、この値は結合のタイプに基づき、自動的に**はい**または**いいえ**に設定されます。 合成シナリオの場合、値は **Yes**、アソシエーションの場合、値は **No** にしてください (代理外部キー拡張)。 このプロパティを使用すると、データ ソースを読み取り/書き込みをすることができます。

    [![FMLabCustomerEntity - プロパティ 2](./media/fmlabcustomerentity-properties2.png)](./media/fmlabcustomerentity-properties2.png)

6. **FMLabCustomerEntity** デザイナーで、**キー** &gt; **EntityKey** とクリックしてから**フィールド** ノードを展開します。 フィールドの一覧が次のスクリーン ショットと一致していることを確認します。

    [![FMLabCustomerEntity](./media/fmlabcustomerentity.png)](./media/fmlabcustomerentity.png)

7. インポート/エクスポートに使用するステージング テーブルを視覚的に検証するには、デザイナーの **FMLabCustomerStaging** テーブルを開き、**FMLabCustomerStaging** ノードを選択します。

    [![fMLabCustomerStaging - プロパティ](./media/fmlabcustomerstaging-properties.png)](./media/fmlabcustomerstaging-properties.png)

8. **FMLabCustomerStaging** &gt; **フィールド**とクリックします。 次のスクリーン ショットでは、ステージング テーブルの標準フィールドが選択されています。 すべてのエンティティ ステージング テーブルにはこれらの標準的なフィールドがあります。 スクリーンショットには、このデー タエンティティに属するデータ フィールドも表示されます。

    [![FMLabCustomerStaging](./media/fmlabcustomerstaging.png)](./media/fmlabcustomerstaging.png)

9. ソリューション エクスプローラーで、プロジェクトを右クリックしてから、**再構築**を選択して、プロジェクトを再構築して同期します。

## <a name="testing-data-entities"></a>データ エンティティのテスト
エンティティは、データのインポート/エキスポートまたは統合を通じ、X++ のさまざまなメソッドを使用してテストできます。 このセクションでは、エンティティを検証するためのシナリオについて調べます。

### <a name="test-the-entity-by-using-x-code"></a>X++ コードを使用してエンティティをテスト

データ エンティティとの対話の最も一般的な方法の 1 つは、単体テストまたは実行可能なジョブを使用してエンティティが構築されたことを検証することによって、x++ を使用する方法です。 この例では、実行可能なジョブを使用します。

1. ソリューション エクスプローラーで、**追加** &gt; **新しい項目** &gt; **実行可能なクラス**をクリックして、実行可能なクラスをプロジェクトに追加します。
2. 次のコードをコピーしてクラスに貼り付け、データ エンティティをテストします。

    ```xpp
    public static void main(Args _args)
    {
        FMLabCustomerEntity customer;
        str license = "License";
        Random r = new Random();
        int rand = r.nextInt();
        license = license + int2str(rand);

        //Create a new record in FM lab customer entity
        customer.clear();
        customer.FirstName = "Bob";
        customer.LastName = "Smith";
        customer.DriverLicense = license;
        customer.insert();

        info(strfmt("Tried to insert customer '%1 %2' with license %3", 
            customer.FirstName, customer.LastName, customer.DriverLicense));

        //Display newly created record
        select forupdate customer where customer.DriverLicense==license;
        info(strfmt("Found newly created customer '%1 %2' with license %3", 
            customer.FirstName, customer.LastName, customer.DriverLicense));

        //Now delete the record from the entity
        customer.delete();
        select customer where customer.DriverLicense==license ;
        info(strfmt("Deleted customer does not exist: license- %1", customer.DriverLicense));
    }
    ```

3. スタートアップ オブジェクトとして設定するためデバッガーでコードを実行します。
4. エンティティを検証するには、デバッガー ウィンドウまたは Web サイトの通知で Infolog を調べます。 3 つの成功メッセージが記録されていることが確認されます。 実行されたアクションも表示されます。

## <a name="importing-data-by-using-entities"></a>エンティティを使用したデータのインポート
**データ管理を有効**プロパティを持つデータ エンティティは、さまざまなファイル形式のデータをインポートおよびエクスポートするために使用できます。 このセクションでは、**FMLabCustomer** エンティティについて CSV ファイル形式でデータをインポートします。

### <a name="file-import"></a>ファイル インポート

データ エンティティを作成した後は、インポート/エクスポートを検証することができます。

1. インポートすることができる CSV ファイルのサンプルを作成します。 次のテキストをコピーし、**FM Lab Customer Import.csv** として保存します。

    ```Console
    CELLPHONE,DRIVERSLICENSE,EMAIL,FIRSTNAME,LASTNAME,CUSTOMERGROUP,ADDRESSLINE1,ADDRESSLINE2,CITY,STATE,ZIPCODE,COUNTRY(999) 555-0100,S615-3939-2349,chris.spencer@adatum.com,Chris,Spencer,adv\_mem\_1,444 Main Street,,Orlando,FL,77899,US(188) 555-0101,S615-3939-2350,Ichiro.lannin@blueyonderairlines.com,Ichiro,Lannin,non\_mem\_1,12 Long Street,,New York City,NY,99087,US(777) 555-0102,S615-3939-2351,josh.smith@fourthcoffee.com,Josh,Smith,adv\_mem\_1,9606 122th Avenue,,Sydney,TX,99874,US(456) 555-0103,S615-3939-2352,Vince@fabrikam.us,Vince,Ahmed,non\_mem\_1,123 Microsoft Way,Unit 87,Seattle,WA,90001,US(345) 555-0104,S615-3939-2353,tony.parker@lucernepublishing.com,Tony,Parker,non\_mem\_1,12012 11th PLNE,Apt 160,San Francisco,CA,75645,US(312) 555-0105,S615-3939-2354,Julia@fineartschool.net,Julia,Natarajan,exec\_mem\_1,449 Long Street,Apt 160,Bruxelles,ID,34213,US
    ```

2. **ユーザー ダッシュ ボード** &gt; **データ管理**をクリックします。
3. **データ管理**ワークスペースで、**インポート** タイルをクリックします。
4. **インポート** ページで、次のスクリーン ショットに表示されるインポートの詳細を入力します。

    ![新しいレコードのインポート](./media/import-new-record.png)

5. **エンティティ ファイルのアップロード** フィールドの隣にある **データのアップロード** ボタンをクリックし、作成した CSV ファイルを選択します。
6. ファイルがアップロードされると、エンティティが中間セクションに追加された事が表示されます。 また、マッピングが無効であることを示すエラーが表示されます。 いくつかのフィールドは、ソース ファイルとターゲット エンティティの間で正しくマップされていません。
7. エンティティ リストで**マップの表示**をクリックします。
8. **AddressLine1** および **AddressLine2** は、ターゲット フィールドにマップされていないソース内の 2 つのフィールドです。 ビジュアル マッパー、または詳細表示で、これらのフィールドを次のようにマップして**保存**をクリックします。

    - AddressLine1 – Address1
    - AddressLine2 – Address2

    [![ソースをステージングにマップ](./media/map-source-to-staging.png)](./media/map-source-to-staging.png)

9. ブラウザーの **戻る** ボタンをクリックして、**インポート ジョブ** ページに戻ります。 エンティティ リストのチェック マークは、エンティティがインポートの準備ができていることを示します。

    [![新規レコード 2 のインポート](./media/import-new-record-2.png)](./media/import-new-record-2.png)

10. **今すぐインポート** をクリックします。 インポートが完了したら、ジョブ ステータス ページが開きます。

## <a name="consuming-entities-by-using-odata"></a>OData を使用してエンティティを消費する
このセクションでは、OData のエンティティを公開して使用する方法を説明します。 開始する前に、クライアントからフリート デモ データが読み込まれたことを確認します。\[baseURL\]/?f=FMSetup

### <a name="review-the-fleetrental-entity-and-add-a-navigation-property-for-odata"></a>FleetRental エンティティを確認し、OData のナビゲーション プロパティを追加

既存の **FleetRental** エンティティをレビューしてから、1 つのデータ エンティティと別のデータ エンティティ間のリレーションシップを作成します。 この関係は、OData エンティティのナビゲーション プロパティとして使用されます。

1. ソリューション エクスプローラーで、**FMEntityLab** プロジェクトの中であることを確認します。
2. アプリケーション エクスプローラーで、**FMRentalEntity** を検索して右クリックしてから、**プロジェクトに追加**を選択します。
3. アプリケーション エクスプローラーで、**FMCustomerEntity** を検索して右クリックしてから、**プロジェクトに追加**を選択します。
4. ソリューション エクスプローラーで、**FMRentalEntity** を右クリックしてから、**開く**を選択します。
5. ビュー デザイナーで、ルート ノード **FMRentalEntity** を選択し、次のプロパティを確認します。

    | プロパティ               | 先頭値        | 説明 |
    |------------------------|--------------|-------------|
    | IsPublic               | 有          | このプロパティを **はい** に設定すると、OData アプリケーション プログラミング インターフェイス (API) を使用して、エンティティを表示できます。 |
    | パブリック エンティティ名     | FleetRental  | **EntityType** の OData API で使用される名前。 |
    | パブリック コレクション名 | FleetRentals | OData コレクション エンティティに使用される名前。 |

6. ビュー デザイナーで、**関係**ノードを展開します。
7. **顧客関係** を選択し、**削除** をクリックします。
8. **関係** を右クリックし、**新規** &gt; **関係** を選択します。
9. **関係 1** を選択し、次のプロパティを設定します。

    | プロパティ                        | 先頭値            |
    |---------------------------------|------------------|
    | 基数                     | ZeroMore         |
    | 氏名                            | CustomerRelation |
    | 関連するデータ エンティティ             | FMCustomerEntity |
    | 関連データ エンティティ カーディナリティ | ExactlyOne       |
    | 関連するデータ エンティティ ロール        | CustomerRole     |
    | 関係のタイプ               | 関連      |
    | 役割                            | レンタル           |

10. ビュー デザイナーで、**CustomerRelation** ノードを右クリックしてから、**新規** &gt; **標準**を選択します。
11. **CustomerRelation** で新しいノードを右クリックし、**プロパティ** を選択します。
12. 次のプロパティを設定します。

    | プロパティ      | 先頭値                                                                         |
    |---------------|-------------------------------------------------------------------------------|
    | フィールド         | **CustomerDriverLicense** これは、**FMRentalEntity** の外部キーフィールドです。 |
    | 関連フィールド | **DriverLicense** これは、**FMCustomerEntity** の固有のキーです。              |

    次のスクリーンショットは、Visual Studio での関係を示しています。

    [![FMRentalEntity - ソリューション エクスプローラー](./media/fmrentalentity-solution-explorer.png)](./media/fmrentalentity-solution-explorer.png)

13. **ビルド**メニューで、**ソリューションのビルド**をクリックして変更を保存し、プロジェクトをビルドします。 **出力** ウィンドウでビルドの進行状況を表示できます。
14. OData エンドポイントをこの変更と併せて更新するには、**iisreset** コマンドを実行する必要があります。 管理者として**コマンド プロンプト** ウィンドウを開き、**iisreset** と入力します。

これで、**FMRentalEntity** と **FMCustomerEntity** 間に、ナビゲーション プロパティの作成を完了しました。

### <a name="use-standard-odata-syntax-to-retrieve-data"></a>標準の OData 構文を使用してデータを取得する

このセクションでは、標準の OData 構文の一部を使用し、フリート管理モデルで公開されている OData エンティティを操作して照会します。 最初に、以下の手順に従って、JSON 形式のデータを表示する Internet Explorer を有効にします。

1. すべての Internet Explorer ウィンドウを閉じます。
2. C:\\FMLab に移動し、json-ie.reg ファイルを選択してダブルクリックします。
3. **レジストリ エディター** ダイアログ ボックスで、**はい**をクリックします。
4. **OK**をクリックします。

Internet Explorer  を使用して一部の OData URI を表示できるようになりました。

1. Internet Explorer を起動し、アドレス バーに次の URL \[baseURL\]/data/$metadata を入力します。OData エンティティに関連付けられているすべてのメタデータが表示されます。

    > [!NOTE]
    > 最初にアクセスする場合、メタデータの表示に数分かかることがあります。 XML で、OData エンティティに関連付けられているすべてのプロパティおよびナビゲーション プロパティを表示できます。

2. ブラウザーで **FleetRental** を検索します。 次のスクリーン ショットは、**FleetRental** エンティティのメタデータと、新しいリレーションシップ **NavigationProperty** を示しています。

    [![FleetRental メタデータ](./media/fleetrental-metadata.png)](./media/fleetrental-metadata.png)

3. フリート管理アプリケーションのすべての顧客を JSON 形式で表示するには、ブラウザーのアドレス バーに \[baseURL\]/data/FleetCustomer の URL を入力します。

    > [!NOTE]
    > エンティティ名は大文字と小文字が区別されます。

4. 顧客のすべてのプロパティを取得しない場合は、選択したプロパティのみを取得できます。 たとえば、**FirstName** および **LastName** のみを取得するには、次の URL を入力します: \[baseURL\]/data/FleetCustomers?$filter=FirstName.LastName
5. また、フィルターを適用することもできます。 たとえば、**FirstName**=**Phil** であるすべての顧客をフィルター処理するには、次の URL を入力します: \[baseUrl\]/data/FleetCustomers?$filter=FirstName%20eq%20'Phil'

    > [!NOTE]
    > これらの URL はコピーおよび貼り付けする場合、機能しません。 アドレス バーに手動で入力する必要があります。

6. 顧客のすべての詳細とともにすべての**レンタル**レコードを取得するには、URL "\[baseURL\]/data/FleetRentals?$expand=CustomerRole" を入力します。次の例は、**レンタル**レコードと、リンクされた顧客の詳細を JSON 形式で示しています。

    ```Text
    "@odata.context":"https://testax32aos.cloud.test.dynamics.com/en/data/$metadata#FleetRentals","value":
    {  
        { 
            "@odata.etag":"W/"JzEsNTYzNzE0NDU3NjsxLDU2MzcxNDQ1NzY7MTc4NjA2OTg1Niw1NjM3MTQ0NjA1Jw=="",
            "Comments":"","StartMileage":0,"VehicleRatePerDay":40,"CustomerDriverLicense":
            "S468-3184-6541","VehicleRateTotal":280,"VehicleId":"Litware_LitwareFour_1",
            "RentalId":"000001",
            "StartFuelLevel":"Full","StartDate":"2010-04-09T00:00:00Z","CustomerLastName":"Spencer",
            "EndMileage":0,"VehicleVIN":"2J4FY19P0NJ710529",
            "RecId":5637144576,"EndDate":"2010-04-16T00:00:00Z",
            "VehicleRatePerWeek":270,"CustomerFirstName":"Phil","State":3,
            "EndFuelLevel":"","CustomerRole":

            {"@odata.etag":"W/"JzEsNTYzNzE0NDU3NjsxLDU2MzcxNDQ1NzYn"",
            "CellPhone":"(999) 555-0100",
            "DriverLicense":"S468-3184-6541","AddressLine2":"",
            "State":"FL","Country":"US","FirstName":"Phil",
            "Email":"phil.spencer@adatum.com","CustomerGroup":
            "adv_mem_1","AddressLine1":"167 BBN Way","City":"Orlando",
            "ZipCode":77899,"RecId":5637144576,"LastName":"Spencer"
        }  
    }
    ```

### <a name="add-an-action-to-odata-entity"></a>OData エンティティへのアクションの追加

アクションは、動作をデータ モデルに挿入する方法を提供します。 Dynamics 'AX 7' では、データ エンティティにメソッドを追加して特定の属性を持つメソッドを修飾することで、アクションを追加します。 このセクションでは、アクションを追加するための手順を見てみましょう。

1. ソリューション エクスプローラーで、**FMRentalEntity** を右クリックしてから、**コードの表示**を選択します。
2. 次のコード明細行をコピーし、**コード**ウィンドウに貼り付けます。

    ```xpp
    public class FMRentalEntity extends common
    {
        [SysODataActionAttribute("ReturnRental", true)]
        public str ReturnRental()
        {
            //do something
            return "Rental was successfully returned. Thanks for your business";
        }
    }
    ```

3. **ビルド**メニューで、**ソリューションの再構築**をクリックして変更を保存し、プロジェクトをビルドします。 **出力** ウィンドウでビルドの進行状況を表示できます。
4. OData エンドポイントをこの変更と併せて更新するには、**iisreset** コマンドを実行する必要があります。 管理者として**コマンド プロンプト** ウィンドウを開き、**iisreset** と入力します。

    追加したアクションは、次のセクションに示すように、コードで呼び出すことができます。

### <a name="consume-the-odata-api-from-an-external-console-application"></a>外部コンソール アプリケーションから OData API を消費する

このセクションでは、コンソール アプリケーションを使用して、フリート管理アプリケーションで公開されている OData エンドポイントを使用します。 コンソール アプリケーションは、最初に、新規顧客を作成し、その顧客の新しい予約を作成します。 このチュートリアルでは、標準の .NET Windows Communication Foundation (WCF) データ サービス ライブラリと共に OData を使用して、Dynamics AX と統合することがいかに簡単であるかを示します。

1. Visual Studio の新しいインスタンスを開始します。
2. **ファイル**メニューで、**開く** &gt; **プロジェクト/ソリューション**をクリックします。
3. **プロジェクトを開く**ダイアログ ボックスで、**C:\\FMLab\\Odata4ConsoleApplication** を参照してから **Odata4ConsoleApplication.csproj** を選択します。
4. **開く** をクリックします。 **Odata4ConsoleApplication** プロジェクトがソリューション エクスプローラーに表示されます。
5. ソリューション エクスプローラーで、**OdataProxyGenerator.tt** をダブルクリックします。
6. コード エディターで、次の文字列を組織の URL に置き換えます。

    ```xpp
    <baseURL> public const string MetadataDocumentUri = "<baseURL>/data/"
    ```

7. OdataProxyGenerator.tt ファイルを保存します。
8. **読み取り専用ファイルの保存**ダイアログ ボックスで、**上書き**をクリックします。 OData メタデータ エンドポイントのプロキシ クラスが生成されます。 この操作には数分かかる場合があります。
9. ソリューション エクスプローラーで、**Program.cs** をダブルクリックします。
10. **dynamicsBaseUri** 変数の値を組織の URL に置き換えます。
11. URL に最後の終了スラッシュ (/) があることを確認してから、**保存** をクリックします。
12. **読み取り専用ファイルの保存**ダイアログ ボックスで、**上書き**をクリックします。
13. F5 キーを押してアプリケーションを実行し、出力コンソール ウィンドウで指示に従います。 アプリケーションによって、Dynamics AX の資格情報を入力するよう求められる場合があります。 アプリケーションが実行された後、新しい顧客と対応する引当が作成されます。
14. **レンタル**ページで新しい予約が表示されることを確認するには、これらの手順に従います。

    1. Internet Explorer を起動して、アドレス バーに URL \[baseURL\]/?mi=FMRental を入力します。**FMRental**  ページにレンタルの一覧が表示されます。

        [![レンタル リスト](./media/rental-list.png)](./media/rental-list.png)

    2. リストの下部にある**次へ**をクリックして、次のページを表示します。 このページで、追加された新しい顧客の予約が作成されたことを確認できます。

        [![顧客引当](./media/customer-reservation.png)](./media/customer-reservation.png)

これで、OData エンドポイントを使用して フリート管理モデルと対話する外部クライアントを見たウォークスルーは完了です。

## <a name="casing-rules-in-data-entities"></a>データ エンティティでのケーシング規則

### <a name="xml-format"></a>XML 形式
エクスポート中、エンティティ名とフィールド名は大文字でエクスポートされます。 変換を適用する必要がある場合、変換ではすべての参照で大文字を使用する必要があります。

インポート中、データ管理は大文字、小文字どちらの入力ファイルも受け入れます。 ただし、ファイル内の特定の属性/要素に同じ形式を使用するように注意する必要があります。 変換を適用するときは、変換が着信ファイル内のすべての参照で同じケーシング規則を使用していることを確認してください。

### <a name="excel-format"></a>Excel 形式
エクスポート中、列名は大文字でエクスポートされます。 インポートでは大文字と小文字が区別されません。

### <a name="csv-format"></a>CSV 形式
エクスポート中、列名は大文字でエクスポートされます。 インポートでは大文字と小文字が区別されません。

## <a name="tips-and-tricks"></a>ヒントや秘訣

### <a name="max-join-limits"></a>最大結合の制限
エンティティの開発中に、エンティティの全体的な構造が最大統合制限である 26 を超えないようにします。 これが既定の制限です。 統合制限を増やすことは、意図しない結果をもたらす可能性があるためお勧めしません。 この制限を超えると、エンティティはレコードの処理に失敗する可能性が高く、次の SQL エラーが発生します。 このエラーを回避するために、エンティティの列の合計数を管理することもお勧めします。

```Console
Cannot create a row of size xxx which is greater than the allowable maximum row size of 8060
```
### <a name="exporting-container-fields"></a>コンテナー フィールドのエクスポート
エンティティにコンテナー フィールドがあり、これらのフィールドをエクスポートする必要がある場合、エンティティは **getFieldsToBeConvertedToFile** を実装して、各コンテナー フィールドがデータ値を個別のファイルにエクスポートできるようにする必要があります。 これにより、コンテナー フィールドをエクスポート可能にすると同時に、エンティティ エクスポート ファイル (コンテナー フィールドのないコア エンティティ データ) が読み取り不能になるのを防ぎます。 **getFieldsToBeConvertedToFile** が実装されていない場合、これらのフィールドはエクスポートされませんが、残りのエンティティ データは通常どおりエクスポートされます。

## <a name="additional-resources"></a>追加リソース

[データ移行のエンティティの開発](develop-entity-for-data-migration.md)
