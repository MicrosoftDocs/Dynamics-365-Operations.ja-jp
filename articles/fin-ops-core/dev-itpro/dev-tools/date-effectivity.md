---
title: 日付の有効期間
description: このトピックでは、データ エンティティとデータ ソースの開始日時に関する情報を提供し、エンティティの開始日時を作成する方法を示します。 また、日付の有効性が読み取りおよび書き込みアクティビティに適用される方法についても説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 24861
ms.assetid: 63e43066-76c7-400b-be7d-d14785e7985d
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08a670e1a43a37cd56844e593c1e2be1ff68619b
ms.sourcegitcommit: 9f90b194c0fc751d866d3d24d57ecf1b3c5053a1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2020
ms.locfileid: "3033016"
---
# <a name="date-effectivity"></a>日付の有効期間

[!include [banner](../includes/banner.md)]

このトピックでは、データ エンティティとデータ ソースの開始日時に関する情報を提供し、エンティティの開始日時を作成する方法を示します。 また、日付の有効性が読み取りおよび書き込みアクティビティに適用される方法についても説明します。

データ エンティティを含む日付有効機能のデザイン パターンはさまざまです。 パターンは、次の 2 つの主要なカテゴリに分類されます。

-   **有効日エンティティ** - エンティティには少なくとも 1 つの有効日データ ソースがあり、エンティティ自体も日付が有効です。
-   **有効日の対象外のエンティティ** – エンティティ自体は、有効日ではありませんが、有効日データ ソースが含まれています。

次のセクションでは、プロパティの小さなリストとエンティティの日付を有効にする操作と有効日データ ソースを制御するメソッドについて説明します。

## <a name="date-effective-entities"></a>有効日のエンティティ
次のテーブルは、データ エンティティの日付を有効にする操作を制御するプロパティを示しています。

| エンティティのプロパティ名 | プロパティのノード                                    | 先頭値       | 説明                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------|---------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ValidTimeStateEnabled       | デザイナーのデータ エンティティ ノード                        | はい (またはいいえ) | 値 **Yes** は、エンティティの日付を有効にします。 エンティティには、**ValidFrom** および **ValidTo** フィールドが必要です。 これらのフィールドは、有効日データ ソースの **ValidFrom** フィールドおよび **ValidTo** フィールドにマップされます。 値 **No** は、エンティティのデータ ソースである日付有効テーブルの日付有効性の強制を無効に*しません*。 |
| ValidTimeStateKey           | データ エンティティ ノードの下では、**キー**&gt;**EntityKey** | はい (またはいいえ) | 値 **Yes** は、この特定のエンティティの日付有効値を実施するために必要なキーを識別します。                                                                                                                                                                                                                                        |

## <a name="read-activities"></a>読み取りアクティビティ
日付の有効期限がデータ エンティティ レベルで設定されると、エンティティからの読み取りはテーブルからの読み取りと動作が同じです。 エンティティには、システムが読み込み中に日付フィルターを適用する **ValidFrom** および **ValidTo** フィールドがあります。

### <a name="query-modes-and-the-validtimestate-keyword-of-x-sql-select"></a>クエリ モードと X++ SQL 選択の validtimestate キーワード

日付有効なエンティティは、X++ **validtimestate** キーワードの使用方法が異なる次の 3 つの*クエリモード*をサポートします。

-   **既定のモード** - 現在のレコードは、`select * from FMVehicleRateEntity; // X++ SQL.` を使用して返されます。
-   **AsOfDate モード** - 指定された日付に有効なレコードは `select validtimestate(d1) * from FMVehicleRateEntity;` を使用して返されます。
-   **AsOfDateRange モード** - 指定された日付範囲に有効なレコードは `select validtimestate(d1,d2) * from FMVehicleRateEntity;` を使用して返されます。

**重要:** それら自体は有効日ではないデータ エンティティでも、有効日のデータ ソースがある場合には、既定のクエリ モードのみ使用できます。 この概念については、この記事の後半で説明します。

### <a name="applying-a-date-filter-at-the-data-source-level"></a>データ ソース レベルで日付フィルターを適用する

日付実効フィルタリングが、データ エンティティの外部、データ ソース レベルで必要とされるシナリオがあります。 たとえば、顧客エンティティ (CustTableTestEntity) にはデータ ソースとして CustTable および LogisticsPostalAddress が含まれています。LogisticsPostalAddress は日付の有効なテーブルであり、CustTable は通常のテーブルです。 顧客エンティティの目的は、顧客とそのアクティブなプライマリ アドレスのリスト (プライマリ アドレスがある場合) を含めることです。 したがって、顧客エンティティ自体は日付有効ではありませんが、データ ソースの 1 つに日付フィルターが必要です。 この場合、エンティティは **ValidTimeStateEnabled** にマークされません。 代わりに、**日付フィルターの適用**プロパティがデータ ソースに追加されます。 **日付フィルターの適用**の値が**はい**に設定されている場合、日付フィルターがそのデータ ソースに自動的に適用されます。 次のテーブルでは、データ エンティティの有効日データ ソースの有効日動作を制御するプロパティについて説明します。

| データ ソースのプロパティ名 | プロパティのノード                             | 先頭値       | 説明                                                                                                                                                                                                                                                                                                    |
|----------------------------------|--------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 日付フィルターの適用                | エンティティの特定のデータ ソースのノード | はい (またはいいえ) | *読み取り*で、このプロパティは、エンティティ データ ソースで日付フィルターが適用されるかどうかを制御します。 この場合、データ ソースを **ValidTimeStateEnabled** にマークする必要があります。 このプロパティ値は、エンティティ自体が日付有効であるかどうかにかかわらず有効です。 *書き込み*で、このプロパティは影響を与えません。 |

この記事では、これらの日付が有効なプロパティの使用方法とそれらの相互作用について説明します。

### <a name="state-matrixes-for-reads"></a>読み取り用の状態マトリックス

このセクションは、データ エンティティからの読み取りのみに関係します。 以下の一対の参照マトリックスは、データ エンティティとそのデータ ソースとの間に存在できる日付有効状態の組み合わせについて説明します。 各テーブルには、4 つのクラスが含まれ、各ケースでは、2 つの異なるターゲットについて説明します。 理解しておく必要がある主要なポイントを次に示します。

-   エンティティから指定された読み取りで、クエリ モードはエンティティと有効日データ ソースの両方で同じです。
-   エンティティの日付が有効ではない場合、クエリ モードは既定のモードに限定されます。 したがって、日付が有効なデータ ソースは現在の日付のみにアクセスされます。
-   有効日データ ソースで、**日付フィルターの適用**プロパティを**いいえ**に設定すると、過去、現在、未来のすべてのデータをデータソースに戻すことができます。
-   OData で、日付の有効なフィルターはデータ エンティティには適用されません。 ただし、データ ソースのフィルターはすべてのコード パスに適用されます。

A. エンティティは有効日で*ある*、なぜならば ValidTimeStateEnabled = はい

**データ ソース*は*日付が有効**

**データ ソース*は*日付が有効ではない**

**日付フィルターの適用 = はい**

-   **エンティティ** 日付フィルターが適用されます。 すべてのクエリ モードがサポートされています。
-   **データ ソース:** フィルターが適用されます。 クエリ モードはサポートされていますが、モードはエンティティのコードと同じです。

有効日の対象外のデータ ソースは影響しません。

**日付フィルターの適用 = いいえ**

-   **エンティティ** 日付フィルターが適用されます。 すべてのクエリ モードがサポートされています。
-   **データ ソース:** 日付フィルターは適用されません。

有効日の対象外のデータ ソースは影響しません。



B. エンティティは有効日では*ない*、なぜならば ValidTimeStateEnabled = いいえ

**データ ソース*は*日付が有効**

**データ ソース*は*日付が有効ではない**

**日付フィルターの適用 = はい**

-   **エンティティ** 日付フィルターが適用されません。
-   **データ ソース:** 日付フィルターが適用されます。 既定のクエリ モードのみサポートされ、X++ **validtimestate** キーワードは省略されます。

有効日の対象外のデータ ソースは影響しません。

**日付フィルターの適用 = いいえ**

-   **エンティティ** 日付フィルターが適用されません。
-   **データ ソース:** 日付フィルターは適用されません。

有効日の対象外のデータ ソースは影響しません。

次のスクリーン ショットは、**日付フィルターの適用** プロパティを **はい** に設定したものです。 したがって、**Address** データ ソースの読み取りに日付フィルターが適用されます。 

[![日付フィルターの適用 = はい](./media/date1.png)](./media/date1.png)

## <a name="write-activities"></a>活動の記述
このセクションでは、有効日エンティティとその有効日データ ソースの動作を設定するオプションについて説明します。 有効日テーブルの概念を確認し、それを有効日エンティティと対比させることから開始します。 **有効日テーブル:** データが有効日テーブルに挿入または更新されると、プロセスは、**xRecord.validTimeStateUpdateMode** メソッドをテーブルバッファーで呼び出すことができます。 このメソッドは、**ValidTimeStateUpdate** 列挙型の要素を受け入れます。 使用可能な要素値を次に示します。

-   CreateNewTimePeriod
-   訂正
-   EffectiveBased

**有効日エンティティ:** 対照的に、データが有効日データ エンティティに挿入または更新されると、**validTimeStateUpdateMode** メソッドはエンティティ レベルで使用されません。 書き込みについては、データ エンティティは、テーブル レベルに有効日プロセスを残します。 エンティティ データ ソース上で **有効時間状態の更新** プロパティを使用すると、データ エンティティの各データ ソースのために **validTimeStateUpdateMode** メソッドを使用することを指定することができます。

## <a name="creating-a-date-effective-entity"></a>日付有効なエンティティを作成しています
このセクションでは、有効日のあるエンティティを作成する方法を示します。

#### <a name="create-a-new-project"></a>新しいプロジェクトの作成

1.  **ファイル** &gt; **新規** &gt; **プロジェクト**とクリックし、新しいプロジェクトを作成します。
2.  ソリューション エクスプローラーで、プロジェクトを右クリックしてから**プロパティ**をクリックします。 プロジェクトの **プロパティ ページ** ダイアログ ボックスが開きます。
3.  **ビルドでのデータベースの同期**プロパティの値を **True** に変更し、**OK** をクリックします。 このプロパティはプロジェクトごとに 1 回のみ設定する必要があります。 

    [![ビルド上にデータベースを同期 =True](./media/date3.png)](./media/date3.png)

#### <a name="add-a-new-data-entity-to-your-project"></a>プロジェクトへの新しいデータ エンティティの追加

**FMVehicleRateEntity** という名前の新しいエンティティを作成し、プロジェクトに追加します。

1.  左ウィンドウで **Microsoft Dynamics 365 アーティファクト**を選択してから、メイン ウィンドウの左側にある**データ エンティティ**をクリックします。
2.  **追加** をクリックします。 **データ エンティティ ビュー** ウィザードが起動します。
3.  次のスクリーン ショットに表示される作成するデータ エンティティのプロパティ値を指定します。 最も重要なフィールドは、**FMVehicleRate** を選択する **プライマリ データ ソース** です。 

    [![プライマリ データ ソース =FMVehicleRate](./media/date5.png)](./media/date5.png) **次へ**をクリックします。

4.  プライマリ データ ソース、**FMVehicleRate** からエンティティにフィールドを追加します。
5.  すべてのフィールドを選択し、**完了** をクリックします。 

    [![新たに追加されたフィールドをすべて選択する](./media/date6.png)](./media/date6.png) 
    
    項目がソリューション エクスプローラーのプロジェクトに追加されます。 
    
    [![ソリューション エクスプローラー内のプロジェクト](./media/date7.png)](./media/date7.png)

#### <a name="build-your-project"></a>プロジェクトの構築

1.  **ビルド** &gt; **ソリューションのビルド**とクリックし、プロジェクトを構築します。
2.  ビルドにエラーが含まれていないことを確認します。 プロセスのこの段階では、警告を容認する必要があります。

#### <a name="validate-the-property-values"></a>プロパティ値の検証

-   ソリューション エクスプローラーで、**FMVehicleRateEntity** ノードを選択し、**FMVehicleRateEntity** エンティティのプロパティを**プロパティ** ウィンドウの値と比較して確認します。 

    [![プロパティ ウィンドウの値](./media/date8.png)](./media/date8.png)

#### <a name="make-your-entity-date-effective"></a>エンティティの日付を有効にする

1.  ソリューション エクスプローラーで、**FMVehicleRateEntity** ノードを右クリックしてから**開く**をクリックします。 エンティティのデザイナーが中央のウィンドウに開きます。 

    [![FMVehicleRateEntity エンティティのデザイナー](./media/date9.png)](./media/date9.png)

2.  **時間状態が有効であるかどうかを検証する**プロパティの値を**はい**に変更します。 

    [![時間状態が有効であるかどうかを検証する = はい](./media/date10.png)](./media/date10.png)

#### <a name="configure-the-valid-time-state-update-property-for-the-date-effective-data-source"></a>有効日データソースの有効時間状態の更新プロパティのコンフィギュレーション

-   **FMVehicleRate** データ ソースを選択し、**有効時間状態の更新** プロパティを **CreateNewTimePeriod** に設定します。 

    [![有効時間状態の更新 = CreateNewTimePeriod](./media/date11.png)](./media/date11.png)

#### <a name="test-your-project"></a>プロジェクトをテスト

-   プロジェクトを再度構築し、次の X++ コードを実行してプロジェクトをテストします。

```xml
/// <summary>
    /// Runs the class with the specified arguments.
    /// </summary>
    /// <param name = "_args">The specified arguments.</param>
    public static void main(Args _args)
    {
        FMVehicleRateEntity FMVehicleRateEntity;
        FMCarClass          vehicle;
        FMVehicleModel      model;
        FMVehicleRate       vehicleRateTable;
        TransDate           d1=1\1\1999,d2=31\12\2014;

        ttsbegin;

        select count(RecId) from FMVehicleRateEntity;
        info(strfmt("Entity - Valid today before insert %1",FMVehicleRateEntity.RecId));

        select count(RecId) from vehicleRateTable;
        info(strfmt("Table - Valid today before insert %1",vehicleRateTable.RecId));

        select firstonly model;

        vehicle.VehicleModel = model.RecId;
        vehicle.VehicleId = "TestV1001";
        vehicle.insert();

            if (vehicle)
            {
                FMVehicleRateEntity.clear();
                FMVehicleRateEntity.FMVehicle_VehicleId = vehicle.VehicleId;
                FMVehicleRateEntity.ValidFrom = d1;
                FMVehicleRateEntity.ValidTo = d2;
                FMVehicleRateEntity.RatePerDay = 100;
                FMVehicleRateEntity.RatePerWeek = 600;
                FMVehicleRateEntity.insert();

                // Should increase by one as compared to before insert numbers
                select count(RecId) from FMVehicleRateEntity;
                info(strfmt("Entity - Valid today after insert %1",FMVehicleRateEntity.RecId));

                // Should increase by one as compared to before insert numbers
                select count(RecId) from vehicleRateTable;
                info(strfmt("Table - Valid today after insert %1",vehicleRateTable.RecId));

                // New record should show in count
                select validtimestate(d1) count(RecId) from FMVehicleRateEntity;
                info(strfmt("Entity - Valid 1999 %1",FMVehicleRateEntity.RecId));

                // New record should show in count
                select validtimestate(d1) count(RecId) from vehicleRateTable;
                info(strfmt("Table - Valid 1999 %1",vehicleRateTable.RecId));

                // update newly created record
                // This should split record into two - 2009 to Today, today to 2014
                // Split happens because of mode in saveEntityDatasource
                select forupdate validtimestate(d1,d2) FMVehicleRateEntity 
                     where FMVehicleRateEntity.FMVehicle_VehicleId == vehicle.VehicleId &&
                           FMVehicleRateEntity.ValidFrom == d1 &&
                           FMVehicleRateEntity.ValidTo == d2;
                FMVehicleRateEntity.RatePerDay = 200;
                FMVehicleRateEntity.update();

                // validate the split
                while select validtimestate(d1,d2) FMVehicleRateEntity
                     where FMVehicleRateEntity.FMVehicle_VehicleId == vehicle.VehicleId
                {
                    info(strfmt("Entity - %1 to %2 , RatePerDay-%3, RatePerWeek-%4",
                            FMVehicleRateEntity.ValidFrom,
                            FMVehicleRateEntity.ValidTo,
                            FMVehicleRateEntity.RatePerDay,
                            FMVehicleRateEntity.RatePerWeek));
                }
                ttsabort;
            }
        }

```



