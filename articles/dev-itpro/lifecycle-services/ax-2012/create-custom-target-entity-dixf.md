---
title: "データのインポート/エクスポート フレームワークのカスタム ターゲット エンティティを作成する"
description: "このトピックでは、カスタム エンティティを作成して、Microsoft Dynamics AX のデータ インポート/エクスポート フレームワークを使用して、定義済みのエンティティに適合しないデータをインポート、エクスポート、または移行できるようにする方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 18181
ms.assetid: 60c79bd4-1090-4e79-9a8c-2117d963647a
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b5d732e986c654656700791ddad044a8d7e37ad5
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="create-custom-target-entities-for-the-data-importexport-framework"></a>データのインポート/エクスポート フレームワークのカスタム ターゲット エンティティを作成する

[!include [banner](../../includes/banner.md)]

このトピックでは、カスタム エンティティを作成して、Microsoft Dynamics AX のデータ インポート/エクスポート フレームワークを使用して、定義済みのエンティティに適合しないデータをインポート、エクスポート、または移行できるようにする方法について説明します。

カスタム エンティティには、ステージング テーブル、プロジェクト、クエリ、クラス、および関数が必要です。 **データ インポート/エクスポート用のカスタム エンティティの作成ウィザード** を使用してこれらの要素を作成、または手動で作成することができます。

## <a name="prerequisites"></a>前提条件
開始する前に、作成しているエンティティに Microsoft Dynamics AX 内の、どのテーブルがマップされているかを把握しておく必要があります。 このテーブルは、エクスポートするデータのソースか、またはインポートするデータのターゲットのいずれかです。 新しいテーブルを作成する必要がある場合、「[テーブルの作成方法](create-tables.md)」の指示に従います。

## <a name="create-a-custom-entity-by-using-the-create-a-custom-entity-for-data-importexport-wizard"></a>データのインポート/エクスポート ウィザードでカスタム エンティティを作成ウィザードを使用してカスタム エンティティを作成する
**データのインポート/エクスポート ウィザードでカスタム エンティティを作成ウィザード**では、カスタム エンティティをすばやく作成できます。

1.  **データのインポート/エクスポート フレームワーク** &gt; **共通** &gt; **データのインポート/エクスポート用のカスタム エンティティの作成**の順に移動します。
2.  移行対象のエンティティに関連するテーブルを選択し、**次へ** をクリックします。
   **注意**: ウィザードは、他のテーブルのデータ構造を継承しないテーブルにのみ関連付けられているカスタム エンティティを作成するために使用できます。
3.  **コード生成パラメーターの選択**ページで、次の手順に従います。
    1.  ステージング テーブル、クエリ、クラスの名前がウィザードに表示されます。 これらの名前を受け入れるか、それらを変更することができます。
    2.  エンティティから表示メニュー項目を選択します。 新しい表示メニュー項目を作成する必要がある場合、「[メニューとメニュー項目の作成方法](https://msdn.microsoft.com/library/5277205c-edb9-498e-b927-406237806217(AX.60).aspx)」の指示に従います。
    3.  テーブルで外部キーのデータを生成するためにメソッドとクエリのどちらを使用するかを選択します。 選択に応じて、**生成**メソッドがクラスに追加されるか、外部キーのソース テーブルがエンティティのクエリに追加されます。
    4.  エンティティに 2 つのテーブルと関連しているデータが格納されているデータ ソースを使用する場合は、複合エンティティを選択します。 次に、**RowID** フィールドがステージング テーブル内に作成されます。 このフィールドは、関連するデータの行を互いにマップするために使用されます。
    5.  エンティティに必要な値の設定が終了したら、**次** をクリックします。

4.  **ターゲット テーブル内のフィールド**ページで、ターゲット テーブルのフィールドを選択します。 **次へ** をクリックします。
5.  **ウィザード完了**ページで、**完了**をクリックします。 データのインポート/エクスポート フレームワークは、Microsoft Dynamics AX アプリケーション オブジェクト ツリー (AOT) を開き、現在のレイヤーでユーザー定義のエンティティのプロジェクトを作成します。
6.  選択したテーブルで拡張データ型 (EDT) が使用されている場合、EDT の外部キー関係を新しいステージング テーブルに追加するかどうかを 2 回尋ねられます。 毎回**はい**をクリックして、ForeignKey のリレーションシップを作成します。
7.  新しいターゲット エンティティとしては、カスタム エンティティを追加します。 エンティティによっては、いくつかの手動のステップが必要な場合があります。 ターゲット エンティティを作成する方法の詳細については、[データのインポート/エクスポート フレームワークを使用する移行データ (DIXF、DMF)](migrate-data-dixf.md) を参照してください。

## <a name="manually-create-a-custom-entity"></a>カスタム エンティティの手動での作成
このセクションでは、カスタム エンティティを手動で作成する方法について説明します。

### <a name="create-a-staging-table-for-the-entity"></a>エンティティのステージング テーブルを作成する

1.  Microsoft Dynamics AX の AOT でエンティティのステージング テーブルを作成します。
2.  次の情報を使用して、ステージング テーブルのテーブル プロパティを設定します。

    | プロパティ名               | 先頭値   |
    |-----------------------------|---------|
    | **SaveDataPerCompany**      | 無      |
    | **SupportInheritance**      | 無      |
    | **TableType**               | 通常 |
    | **ConfigurationKey**        | DMF     |
    | **ValidTimeStateFieldType** | None    |

3.  次のプロパティを持つフィールドを作成します。

    | フィールド名          | 拡張データ型     | 列挙              |
    |---------------------|------------------------|-------------------|
    | **DefinitionGroup** | DMFDefinitionGroupName |                   |
    | **IsSelected**      | DMFIsSelected          | NoYes             |
    | **TransferStatus**  |                        | DMFTransferStatus |
    | **ExecutionId**     | DMFExecutionId         |                   |

4.  次のプロパティを持つフィールド グループを作成します。

    | フィールド グループ名                                                         | ラベル                                                                         | フィールド                                                                                        |
    |--------------------------------------------------------------------------|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
    | **ExclusionList**                                                        | **除外リスト**                                                            | **DefinitionGroup**                                                                          |
    | ** **                                                                    | ** **                                                                         | **IsSelected**                                                                               |
    | ** **                                                                    | ** **                                                                         | **TransferStatus**                                                                           |
    | ** **                                                                    | ** **                                                                         | **ExecutionId**                                                                              |
    | **有効**                                                              | **有効**                                                                   | オプション: 既定でテンプレートに追加するステージング テーブルからのフィールド。 |
    | &lt;&lt;FunctionName\_Sequence&gt;&gt;例 – GeneratePostalAddress\_2 | &lt;&lt; 機能の説明 &gt;&gt;住所を生成する機能。 | 指定されたメソッドのソースであるステージング テーブルのフィールド。              |
    |                                                                          |                                                                               | **CountryRegionId**                                                                          |
    | ** **                                                                    | ** **                                                                         | **都道府県**                                                                                    |
    | ** **                                                                    | ** **                                                                         | **市町村**                                                                                     |
    | ** **                                                                    |                                                                               | ..                                                                                           |

5.  テーブルのプライマリ インデックスを作成します。

    | インデックス名                              | プロパティ                             | フィールド                                                 |
    |-----------------------------------------|----------------------------------------|--------------------------------------------------------|
    | &lt;&lt;任意の名前&gt;&gt;. 例 – Idx | AllowDuplicates – いいえ  | **DefinitionGroup**                                    |
    |   | AlternateKey - はい | **DefinitionGroup**                                    |
    |                                         |                                        | **ExecutionId**                                        |
    |                                         |                                        | **一意性を定義するステージング テーブルのフィールド** |
    |                                         |                                        | ..                                                     |

6.  ステージング テーブルとターゲット テーブル間の関係を指定します。 この関係は、特定のステージング レコードを関連するターゲット エンティティに自動的にリンクするために使用されます。 関係のノードを使用して関係を定義することはできない場合は、エンティティのクラスに addStagingLink() メソッドを使用しそれを定義する必要があります。

    | インデックス名                                    | 関係プロパティ                  | 関係フィールド                |
    |-----------------------------------------------|--------------------------------------|--------------------------------|
    | &lt;&lt;ターゲット テーブル&gt;&gt;. 例 - ターゲット | テーブル - &lt;&lt;ターゲット テーブル&gt;&gt; | Staging.Field1 = Target.Field1 |
    |                                               |                                      | ..                             |
    |                                               |                                      | ..                             |

### <a name="create-a-project"></a>プロジェクトの作成

Microsoft Dynamics AX の AOT で、プロジェクトを作成します。

### <a name="create-a-class-for-the-entity"></a>エンティティのクラスを作成します

1.  Microsoft Dynamics AX の AOT でエンティティのクラスを作成します。
2.  クラス宣言では、次のプロパティを含めます。

    -   “\[DMFAttribute(true)\]” を指定します。
    -   “DMFClassName extends DMFEntityBase” を指定します。
    -   名前が**エンティティ**のステージング テーブルのオブジェクトを宣言します。
    -   ターゲット エンティティのメイン テーブルのオブジェクトを**ターゲット**という名前で宣言します。

    次の例は、**DMFCustomerEntityClass** クラスの宣言方法を示しています。

        [DMFAttribute(true)]
        class DMFCustomerEntityClass extends DMFEntityBase
        {

        DMFCustomerEntity entity;

        CustTable target;

        }

3.  **新規**メソッドの作成は次のようにします。

    -   メソッドはステージング テーブルをパラメーターとして使用する必要があります。
    -   値のエンティティは、パラメーターから初期化する必要があります。

    次の例は、**DMFCustomerEntity** の **new** メソッドを示しています。

        Public void new(DMFCustomerEntity _entity)
        {
        entity = _entity;
        }

4.  **コンストラクター** メソッドの作成は次のようにします。

    -   メソッドはステージング テーブルをパラメーターとして使用する必要があります。
    -   このメソッドは、パラメーターを使用して現在のクラスのオブジェクトを作成して返す必要があります。

    次の例は、**DMFCustomerEntity** の **construct** メソッドを示しています。

        public static DMFCustomerEntityClass construct (DMFCustomerEntity _entity)
        {
        DMFCustomerEntityClass entityClass = new DMFCustomerEntityClass(_entity);
        return entityClass;
        }

5.  **setTargetBuffer** メソッドの作成は次のようにします。

    -   ターゲット エンティティは、複数のデータ ソースを持つことができます。 1 つのデータ ソースは、エンティティを表すメイン テーブルです。 **setTargetBuffer** メソッドで、**\_dataSourceName** パラメーターはターゲット エンティティ クエリに存在するデータ ソースを表します。
    -   データ ソースによっては、データ ソースのテーブルのローカル インスタンスを初期化する必要があります。 ローカル インスタンスは、データ移行に必要な機能で使用できます。 ターゲットは、ターゲット エンティティを表すメイン テーブルによって初期化される必要があります。

    次の例は、**setTargetBuffer** メソッドを示しています。

        public void setTargetBuffer(Common _common, Name _dataSourceName = ' ')
        {
        switch (_common.TableId)
        {
        Case tableNum(CustTable) :
        Target = _common;
        Break;
        }
        }

6.  クラスの **RunOn** プロパティの値を **CalledFrom** に設定します。

### <a name="write-functions-to-import-and-export-data"></a>データをインポートおよびエクスポートする関数を記述

次の 2 つの方法で、ステージングからターゲット エンティティにデータをマッピングすることができます。
-   ステージング エンティティのフィールドを直接ターゲット エンティティのフィールドに割り当てます。 この場合、ステージング フィールドとターゲット フィールドのデータ型は同じである必要があります。
-   X++ 関数を記述してフィールド値をステージングからターゲットに変換します。

定義したデータのインポートおよびエクスポート関数は、次の操作を実行する必要があります。
-   **入力/ソース** – ステージング レコード全体は、ローカル変数としてクラスで使用できます。 したがって、このクラスにパラメーターを渡す必要はありません。
-   **出力/ターゲット** – 関数が実行された後、ターゲット エンティティのゼロまたは複数のフィールドが設定されます。 関数の戻り値の型は、ターゲットに設定する必要がある 0 以上の値を保持できるコンテナーです。

特定の関数によって返される値のシーケンスは、**getReturnFields** メソッドで定義する必要があります。
#### <a name="create-a-getreturnfields-method"></a>getReturnFields メソッドの作成

**getReturnFields** メソッドは、データ移行に使用される関数の既定の出力またはターゲット フィールドを指定するために使用されます。 メソッドのパラメーターの一部は次のとおりです。
-   \_エンティティ – エンティティの名前。
-   \_名前 – 機能の名前。

**戻る**: この方法では次の情報を戻す必要があります。
-   コンテナー
-   メソッドを実行する必要のあるターゲット エンティティ クエリ内のデータ ソースの名前
-   関数によって初期化されるターゲット エンティティ クエリ内のデータ ソース フィールドの名前

#### <a name="create-an-addstaginglink-method"></a>AddStagingLink メソッドを作成する

**addStagingLink** メソッドは、ステージング テーブルの関係プロパティを使用してこの関係を定義できないときに、ステージング テーブルとターゲット テーブル間の関係を定義するために使用されます。 ターゲット クエリとステージング レコードは、このメソッドで使用できます。 したがって、コードを使用してターゲットとステージングの間の範囲を追加できます。 次の例は、**DMFEmployeeEntityClass** クラスの **addStagingLink** メソッドを示しています。
public Query addStagingLink(Query query, TableId _entityTableId, Common _staging) { QueryBuildDataSource qbd; qbd = query.dataSourceTable(tableNum(HcmWorker)); qbd.addRange(fieldNum(HcmWorker,PersonnelNumber)).value(_staging.(fieldNum(DMFEmployeeEntity,PersonnelNumber))); return query; } 

#### <a name="create-a-query-to-populate-the-target-entity"></a>ターゲット エンティティを設定するためのクエリを作成する

エンティティを表すテーブルは、ターゲット エンティティ クエリに追加する必要があります。 手動プロジェクトのクエリを追加する必要があります。

### <a name="create-an-enum-field-in-the-target-entity"></a>ターゲットエンティティに列挙フィールドを作成する

ターゲット エンティティの列挙フィールドは、ステージング テーブルの文字列フィールドで表されます。 列挙型ラベル文字列を保持する適切な長さの文字列型の新しい EDT を作成する必要があります。 ターゲットエンティティの列挙型フィールドとステージング テーブルの文字列フィールドの間の変換は、データ インポート/エクスポート フレームワークによって自動的に処理されます。

### <a name="handle-the-refrecid-field"></a>RefRecId フィールドを処理します

ステージング テーブルには、通常、ナチュラル キー (文字列) があります。 ターゲット テーブルに他のテーブルの Recid が含まれている場合、RecId ナチュラル キーに変換する必要があります。 この場合、2 つのオプションがあります。
-   照会テーブルをターゲット エンティティ クエリに追加することができるように、データ ソースを追加します。
-   機能を作成します。

#### <a name="add-a-data-source"></a>データ ソースの追加

照会テーブルをターゲット エンティティ クエリに追加することができるように、データ ソースを追加することができます。 たとえば、ターゲットの **VendTable** テーブルには **VendExceptionGroup** が含まれています。それは **VendExceptionGroup** テーブルから取得される RecId です。 この場合、ステージング テーブルに **VendExceptionGroup** を含める必要があります。 **VendExceptionGroup** テーブルは、**VendTable** データ ソースの下でターゲット エンティティ クエリにも追加する必要があります。 **VendTable** と **VendExecptionGroup** の間の関係は手動で指定する必要があります。 リレーションシップは **VendTable** の **RefRecId** と **VendExceptionGroup** の [RecId] の間にしてください。 ステージング フィールド **DMFVendorEntity.VendExecptionGroup** は、**DMFVendorTargetEntity. DS:VendExceptionGroup.VendExceptionGroup** のターゲット フィールド クエリにマップする必要があります。 多くのシナリオでは、ターゲット クエリのフィールドの名前がステージング フィールドと同じである場合、マッピングは自動的に実行されます。 ターゲット フィールドをステージング フィールドに手動でマッピングすることもできます。

#### <a name="create-a-function"></a>機能の作成

エンティティ クラスで関数を作成することができます。 ステージング テーブルの RefRecId フィールドの関連フィールドは、ステージング テーブルのナチュラル キーである必要があります。 文字列を RecId に変換するには、エンティティ クラスでメソッドを作成します。 たとえば、CustTable テーブルには、CompanyNAFCode テーブルの RecId である CompanyNAFCode フィールドが含まれます。 この場合、文字列 (DMFCustomerEntity.CompanyIdNAF) を RecId (CompanyNAFCode.RecID) に変換するために DMFCustomerEntityClass に関数を作成することができます。 関数を作成するときは、ステージング テーブルのフィールド グループを作成する必要があり、エンティティ クラスの **getReturnFields** メソッドで、ターゲット上に戻りフィールドを指定する必要があります。






