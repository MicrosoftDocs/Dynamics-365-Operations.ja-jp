---
title: 拡張機能を介したカスタム Commerce Data Exchange 同期の有効化
description: このトピックでは、コマース 初期化クラスを拡張して、カスタムの Commerce Data Exchange (CDX) 同期をサポートする方法について説明します。
author: mugunthanm
ms.date: 12/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-09-15
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.openlocfilehash: a8696dd4934ed6f495c5add98b5b8070c56427ea
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791223"
---
# <a name="enable-custom-commerce-data-exchange-synchronization-via-extension"></a>拡張機能を介したカスタム Commerce Data Exchange 同期の有効化

[!include [banner](../../includes/banner.md)]

このトピックでは、コマース 初期化クラスを拡張して、カスタムの Commerce Data Exchange (CDX) 同期をサポートする方法について説明します。 この拡張機能では、Microsoft Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 8 または Microsoft Dynamics 365 Retail プラットフォーム更新プログラム 8 で追加された新しい拡張ポイントを使用します。

CDX は、コマース バックオフィス (HQ) と、オンライン ストアまたは従来型の店舗などのチャネルの間でデータを転送するシステムです。 HQ とチャネル データベース間のデータ転送は、スケジューラ ジョブによって制御されます。 各スケジューラ ジョブには、スケジューラ サブジョブの一覧が含まれています。 スケジューラ サブジョブには、ソース テーブルと出力先テーブルの名前と、それらのテーブルの転送フィールド マッピングが含まれています。 HQ とチャネル データベース間のデータ同期をコンフィグレーションするには、2 つの方法があります。

+ CDX のコンフィギュレーション ユーザー インターフェイス (UI) を使用して、すべてのカスタム ジョブとサブジョブをコンフィギュレーションします。
+ プッシュおよびプルの両方のカスタム ジョブとサブジョブをサポートするために用意されている拡張ポイントを使用して、コマース初期化クラスを拡張します。

コマース初期化クラスを使用する利点は、さまざまな環境 (開発、テスト、および実稼働) でカスタム ジョブを構成する必要がないことです。 代わりに、**Retail と Commerce > バックオフィスの設定 > コマース スケジューラ > コマース スケジューラの初期化** から **コマース スケジューラの初期化** ダイアログ ボックスを使用して、CDX 初期化を実行できます。 データの同期のためのカスタム ジョブに関する情報は CDX で自動的に作成されます。

HQ とチャネル データベース間のデータ転送には、さまざまなシナリオがあります。

+ ダウンロード ジョブを使用して新しい HQ テーブルから新しいチャンネル データベース テーブルにデータを送信します。
+ プッシュ ジョブを使用して新しい HQ テーブルに新しいチャンネル データベース テーブルからのデータを取り込みます。

## <a name="send-data-from-a-new-hq-table-to-a-new-channel-database-table-by-using-a-download-job"></a>ダウンロード ジョブを使用して新しい HQ テーブルから新しいチャンネル データベース テーブルにデータを送信

データをプッシュまたはプルする前に、XML リソース ファイルのさまざまなメタデータ定義を理解する必要があります。 リソース ファイルには、データのプッシュやプルを実行する環境で初期化されるカスタム ジョブ情報が含まれています。 コンフィギュレーションする必要があるリソース ファイルの一覧を次に示します。

+ **ChannelDBSchema** - チャンネル データベースで作成した拡張スキーマです。
+ **TargetTableSchema** – カスタム テーブルを追加するチャンネル データベースで作成した拡張スキーマ。
+ **AxTableName** - テーブル名。
+ **IsUpload** – ジョブがプッシュ ジョブかプル ジョブかを判断するフラグ。 (つまり、フラグは、HQ からチャンネル データベースにデータを送信するか、チャンネル データベースから HQ にデータをプルするかを示します)。 既定値は **false** で、HQ からチャネル データベースにデータを送信していることを示します。
+ **ScheduledByJob** – このリソース ファイルには、1 つ以上のサブジョブが含まれています。
+ **サブジョブ** – 各テーブルは、サブジョブとして追加され、各サブジョブは 1 つまたは複数のスケジューラ ジョブによってスケジュールされています。
+ **TargetTable** – チャンネル データベース テーブルの名前です。 このテーブルは、プッシュ ジョブまたはプル ジョブのデータの送り先となるターゲット テーブルです。 値が指定されていない場合、ターゲット テーブルの名前とソース テーブルの名前が同じになります。

新しい HQ テーブルと新しいチャンネル データベース テーブルを作成した場合は、2 つのテーブル間でデータをプッシュするためのこれらの手順に従います。

1. カスタム プロジェクトを作成し、アプリケーション オブジェクト ツリー (AOT) を使用してカスタム テーブルを追加します。
2. すべてのカスタム ジョブ情報を追加する新しいリソース ファイルを作成します。 リソース ファイルのテンプレートを次に示します。

```csharp
    <RetailCdxSeedData ChannelDBMajorVersion="7" ChannelDBSchema="ext" Name="AX7">
        <Jobs>
        </jobs>
        <Subjobs>
            <Subjob Id="" TargetTableSchema="" TargetTableName="">
        </Subjobs>
     </RetailCdxSeedData>
```

> [!NOTE]
> **DataAreaId** の列名は、フィールド マッピングには明示的に含まれません。 これは、 Commerce Data Exchange (CDX) によって自動的に生成されます。 追加された場合、小売用スケジューラの初期化中にエラーが発生します。

3. AOT を使用して新しい XML リソースを作成します。 リソースの XML ファイルで、次の例に示すように新しいテーブルと新しいジョブの詳細を指定します。

    > [!NOTE]
    > 新規テーブルを既存のジョブの一部として追加するか、または新しいジョブを作成してからこのテーブルを追加するかのいずれかを実行できます。 この場合、ジョブ ID が **7000** で、カスタムのテーブルに **ContosoRetailSeatingArrangementData** と名前が付けられている場合、新しいジョブを作成しています。
    >
    > ```xml
    > <RetailCdxSeedData ChannelDBMajorVersion="7" ChannelDBSchema="ext" Name="AX7">
    >    <Jobs>
    >        <Job DescriptionLabelId="REX4520710" Description="Custom job" Id="7000"/>
    >    </Jobs>
    >    <Subjobs>
    >        <Subjob Id="ContosoRetailSeatingArrangementData" TargetTableSchema="ext" AxTableName="ContosoRetailSeatingArrangementData">
    >            <ScheduledByJobs>
    >                <ScheduledByJob>7000</ScheduledByJob>
    >            </ScheduledByJobs>
    >            <AxFields>
    >                <Field Name="seatNumber"/>
    >                <Field Name="capacity"/>
    >                <Field Name="channelRecId"/>
    >                <Field Name="RecId"/>
    >             </AxFields>
    >        </Subjob>
    >    </Subjobs>
    > </RetailCdxSeedData>
    > ```

    既定では、ターゲット テーブルの名前がここでは指定されていません。 システムでは、チャネル側のターゲット テーブルの名前がコマース側のソース テーブルの名前 (**AXTableName**) と同じであることが前提です。 ただし、チャンネル側のターゲット テーブルの名前は、時にソース テーブルの名前とは異なる場合があります。 この場合、**&lt;サブジョブ&gt;** ノードで **&lt;TargetTableName&gt;** 属性を使用してチャネル側でターゲット テーブルの名前を設定できます。

    同様に、マッピング セクションでは、コマース側にあるフィールドの名前だけが指定されています (**AxFields**)。 既定では、同じフィールド名がチャネル側でも使用されていると想定します。 ただし、対応するチャンネル テーブルのフィールド名は、時にコマース側にあるフィールド名とは異なる場合があります。 この場合、マッピングで **&lt;フィールド&gt;** ノードの **ToName** 属性を使用してチャネル側でフィールドの名前を設定できます。

4. プロジェクトを右クリックし、**追加** &gt; **新しい項目** を選択します。
5. **新しい項目の追加** ダイアログ ボックスで、**リソース** を選択し、リソース ファイルに **RetailCDXSeedDataAX7_Custom** と名前を付けてから、**追加** を選択します。

    ![新しい品目の追加](media/cdx-ext-1.png)

6. **リソース ファイルの選択** ダイアログ ボックスで、手順 2 で作成したリソース ファイルを検索し、**開く** を選択します。
7. **registerCDXSeedDataExtension** イベントを処理するために使用する新しいクラスを追加します。 **RetailCDXSeedDataBase** クラスを検索し、デザイナーで開きます。 **registerCDXSeedDataExtension** デリゲートを右クリックし、**イベント ハンドラーをコピー** を選択します。
8. 作成したイベント ハンドラー クラスに移動して、次のイベント ハンドラー コードを貼り付けます。

    ```csharp
    if (originalCDXSeedDataResource == resourceStr(RetailCDXSeedDataAX7))
    {
        resources.addEnd(resourceStr(RetailCDXSeedDataAX7_Custom));
    }
    ```

    > [!NOTE]
    > システムの CDX シード データに対して 2 つの定義があるため、生成する CDX シード データが拡張の対象のバージョンである場合にのみ、拡張 CDX データが追加されるように指定する必要があります。 **if** 条件が削除されている場合、拡張 CDX シード データが N-1 CDX シード データの上にも適用され、意図しない結果が生じる可能性があります。 ベスト プラクティスとして、X++ の CDX/Retail スケジューラ同期フレームワーク クラスのその他のカスタマイズを回避することをお勧めします。 追加の処理が実行される場合、これによりデータ フローが影響を受けることがあります。 提案されるパターンは、別のクラスおよびバッチ ジョブによりアップロードされたデータを処理させることです。
    >
    > 後で言及されるさまざまなシナリオの個別のリソース ファイルを作成する必要はありません。 1 つのファイルにすべてのカスタム ジョブ情報を含め、拡張機能クラスからそのファイルを登録することができます。
    >
    > 初期化クラスが実行される場合、このクラスはこのハンドラーを実装する拡張機能を検索します。 拡張子が見つかった場合、ランタイムはリソース ファイルに含まれるカスタム情報も初期化します。

9. **Retail と Commerce > バックオフィスの設定 > コマース スケジューラ >コマース スケジューラの初期化** に移動します。
10. **コマース スケジューラの初期化** ダイアログの **OK** ボタンをクリックして CDX の初期化を実行します。

## <a name="pull-data-from-a-new-channel-database-table-to-a-new-hq-table-by-using-a-push-job"></a>プッシュ ジョブを使用して新しいチャンネル データベース テーブルから HQ テーブルにデータをプルする

新しいチャネル テーブルから HQ にデータをプルするには、次の 2 つの方法があります。

+ ここに示すように、新しいリソース ファイルを作成し、新しいリソースを 2 行目のイベント ハンドラーに追加します。

    ```csharp
    if (originalCDXSeedDataResource == resourceStr(RetailCDXSeedDataAX7))
    {
        resources.addEnd(resourceStr(RetailCDXSeedDataAX7\_Custom));
        resources.addEnd(resourceStr(RetailCDXSeedDataAX7\_Custom1));
    }
    ```

+ 新しい行を追加しなくて済むように、新しい情報を含む既存のリソース ファイルを更新します。 アップロードするには、次の例に示すように、リソース ファイルの **IsUpload** 属性を **true** に設定し、カスタム プルジョブに関する情報を追加します。

    ```xml
    <Subjob Id="ContosoRetailSeatReservationTrans" TargetTableSchema="ext" IsUpload="true"
    ReplicationCounterFieldName="ReplicationCounterFromOrigin" AxTableName="ContosoRetailSeatReservationTrans">
        <ScheduledByJobs>
            <ScheduledByJob>P-1000</ScheduledByJob>
        </ScheduledByJobs>
        <AxFields>
            <Field Name="transactionId"/>
            <Field Name="storeId"/>
            <Field Name="terminalId"/>
            <Field Name="contactPhoneNo"/>
            <Field Name="numberOfCustomers"/>
            <Field Name="customerName"/>
            <Field Name="reservationDate"/>
            <Field Name="reservationTime"/>
            <Field Name="replicationCounterFromOrigin"/>
        </AxFields>
    </Subjob>
    ```

    > [!NOTE]
    > 拡張テーブルを作成している場合にデータを HQ に同期するには、テーブルの主キーおよびクラスター化されたインデックスが拡張テーブルの HQ テーブルと同じである必要があります。そうでない場合 CDX 同期は失敗します。 拡張テーブルから HQ にデータをプルする必要がある場合は、拡張テーブルに REPLICATIONCOUNTERFROMORIGIN ID 列 ([REPLICATIONCOUNTERFROMORIGIN] [int] IDENTITY(1,1) NOT NULL,) が含まれている必要があります。
    
    > この新規テーブルを既存のプル ジョブ (P-0001) の一部として追加するか、または新しいプル ジョブを作成するかのいずれかを実行できます。

## <a name="other-scenarios"></a>その他のシナリオ

残りのプッシュとプル シナリオでは、サンプル リソース ファイルの情報のみが記載されます。それは前のセクションの説明にあるように、初期化が同じであるためです。

### <a name="push-existing-headquarters-tables-to-channel-database-that-are-not-part-of-cdx-configurations"></a>CDX コンフィギュレーションに含まれていないチャネル データベースに既存の Headquarters テーブルをプッシュする

この場合、拡張機能では、コア テーブルと同じ名前を持つ新しいサブ ジョブを作成し、それと同じテーブルをチャネル データベースの ext スキーマに作成して、マップする必要があります。 CDX は同じテーブルに対する複数のサブ ジョブをサポートしていないので、サブ ジョブ名はコア テーブル名と一致させておき、将来の競合を回避する必要があります。 将来的には、Headquarters テーブルが、コア テーブルと同じサブ ジョブ名で、アウト・オブ・バンド (OOB) 製品による CDX プッシュ/プル配信に追加される可能性があります。 CDX フレームワークは、重複するサブ ジョブ名がある場合は、自動的にマージされます。

### <a name="push-existing-columns-that-arent-mapped-as-part-of-any-subjobs"></a>任意のサブジョブの一部としてマップされていない既存の列をプッシュ

次の例で示すように、マッピングされていない既存の列を、新しい拡張列またはチャンル データベース内の既存の列のいずれかにプッシュすることができます。

```xml
<Subjob Id="RetailChannelTable" TargetTableSchema="ext">
    <AxFields>
        <Field Name="Payment"/>
        <!-- Existing column which was not pushed to channel db-->
        <Field Name="PaymMode"/>
        <!-- Existing column which was not pushed to channel db-->
        <Field Name="ContosoRetailWallPostMessage"/>
        <!-- New column from the extended table -->
    </AxFields>
</Subjob>
```

テーブルに **RecId** ではない主キーがある場合、次の例に示されるように、チャンネル側の拡張子テーブルに 非 **RecId** 主キーも含まれる必要があります。

```xml
    <Subjob Id="RetailCustTable" TargetTableSchema="ext">
        <AxFields>
            <Field Name="ReturnTaxGroup_W"/>
            <!-- Existing column which was not pushed to channel db-->
            <Field Name="SSNNumber"/>
            <!-- New column from the extended table-->
        </AxFields>
    </Subjob>
</Subjobs>
```

### <a name="pull-new-columns-to-an-existing-table"></a>新しい列を既存のテーブルにプルする

新しい列を追加して既存のテーブルの一部を取得する場合は、次のコードを使用します。

```xml
<Subjob Id="RetailTransactionTable" TargetTableName="CONTOSORETAILTRANSACTIONTABLE" TargetTableSchema="ext"  OverrideTarget="false">
    <AxFields>
        <Field Name="ContosoRetailSeatNumber"/>
        <Field Name="ContosoRetailServerStaffId"/>
    </AxFields>
</Subjob>
```

### <a name="move-an-existing-subjob-to-another-subjob"></a>別のサブジョブへの既存のサブジョブの移動

既存のサブジョブを別のジョブに移動するには、リソース ファイルの **ScheduledByJob** 属性を変更することができます。この属性はイベント ハンドラの一部として実行されます。

```xml
<Subjob Id="DirPartyTable">
    <ScheduledByJobs>
        <ScheduledByJob>1000</ScheduledByJob>
        <!--add existing subjob to another job-->
    </ScheduledByJobs>
```

## <a name="cdx-sample---pull-new-columns-to-an-existing-table"></a>CDX サンプル - 新しい列を既存のテーブルにプルする

Microsoft Dynamics 365 Retail アプリケーション更新プログラム 5 では、**RetailSDK\Documents\SampleExtensionsInstructions\ExtensionTables** に新しいサンプルが追加され、そこにすべてのサンプル SQL スクリプト、さまざまな CDX 拡張機能シナリオの ax プロジェクト ファイルがありますが、さまざまな CDX 拡張機能シナリオの参照として使用してください。

次のセクションでは、拡張テーブルを使用してトランザクション テーブルをカスタマイズする手順とベスト プラクティスについて説明します。 他のセクションでは、CDX をカスタマイズしてチャネル側のカスタマイズされた (拡張子) テーブルをコマースにアップロードする方法を示します。 また、カスタマイズのテスト方法を説明するセクションも含めました。

### <a name="setup-steps"></a>設定手順

変更していない Retail ソフトウェア開発キット (SDK) にこれらの変更を実装することをお勧めします。 または、SDK を Microsoft Azure DevOps などのソース管理下で配置することにより、どのステップでも変更を簡単に元に戻すことができます。 まず、SDK にある \*.axpp パッケージをインポートします。 次に、チャンネル データベースで、SQL 更新スクリプトを実行します。

1. カスタマイズ コードを含むコマース側にパッケージをインポートします。

    1. ExtensionTablesAndCDXCustomization.axpp ファイルをRetailSDK\Documents\SampleExtensionsInstructions\ExtensionTables フォルダーからコピーし、拡張プロジェクト フォルダーに貼り付けます。
    2. Microsoft Visual Studio を起動します。
    3. **Dynamics 365** > **インポート プロジェクト** を選択します。
    4. **プロジェクトのインポート** ダイアログ ボックスで、手順 1 でコピーした .axpp ファイルのパスを指定します。
    5. 必要に応じて、**現在のソリューション** または **新しいソリューション** を選択します。
    6. **OK** を選択してパッケージのインポートを開始します。

        インポートが完了した後、ソリューション エクスプローラーにファイルがあります。

    7. ソリューションをビルドします。
    8. プロジェクトを右クリックし、**データベースの同期** を選択します。

2. SQL 更新スクリプトを実行します。

   1. Retail SDK フォルダーから **ContosoRetailExtensionTablesUpdate.sql** ファイルをコピーします。 同様の仕方で他のサンプル ファイルを実行することができます。
   2. Microsoft SQL Server ブラウザーでスクリプトを開いて、チャネル データベースに対してスクリプトを実行します。

      このステップでは、トランザクション テーブルをカスタマイズするために必要な拡張テーブルを作成します。 スクリプトはその他のサンプル シナリオに使用されるその他のテーブルも作成することに注意してください。

### <a name="extend-the-data-in-the-sample"></a>サンプルでデータを拡張する

コマース側のテーブル拡張は、サンプルですでに作成されています。 手動で作成するには、次の手順を実行します。

1. Visual Studio を起動します。
2. メニューで、**表示** > **アプリケーション エクスプローラー** を選択します。
3. **データ モデル** > **テーブル** > **RetailTransactionTable** を選択し、**RetailTransactionTable** を右クリックして **拡張機能を作成** を選択します。

    ベスト プラクティスは、デフォルトの名前を次のように変更する必要があります **RetailTransactionTable.ContosoRetailExtension**。 常に一意の接頭語を追加します。 このサンプルでは、**ContosoRetail** が一意の接頭語として使用されます。 一意の接頭語を使用することにより、複数の独立系ソフトウェア ベンダー (ISV) によってテーブルが拡張されている場合、名前の競合を防ぐことができます。

4. 新しい **RetailTransactionTable.ContosoRetailExtension** テーブルで、2 つの新しいフィールドを作成します。

    **タイプ = 文字列、名前 =ContosoRetailServerStaffId**: **拡張データ型** プロパティを **RetailStaffId** に設定します。
    **タイプ = 整数、名前 =ContosoRetailSeatNumber**: **拡張データ型** プロパティを **ContosoRetailSeatNumber** に設定します。

5. 変更を保存し、プロジェクトをビルドします。
6. プロジェクトを右クリックし、**データベースの同期** を選択します。

    > [!NOTE]
    > ベスト プラクティスとして、今後の名前の競合を回避するために新しい列名に固有の接頭語が追加されます。 別の ISV が同じ名前を持つ列を作成する場合、または Microsoft が同じ名前を持つ列を使用する更新プログラムをリリースする場合、名前付けの競合が発生する可能性があります。 拡張テーブルでは異なる AOT 資産に作成されますが、新しい列は SQL の元のテーブルに追加されます。

### <a name="extend-the-database-on-the-channel-side"></a>チャンネル側にあるデータベースを拡張

Retail SDK フォルダーから SQL Server **ContosoRetailExtensionTablesUpdate.sql** スクリプトを開いて実行します。 複数の品目が作成され、コンフィギュレーションされています。

+ 外部キーとカスタム (拡張子) フィールドを含む **[ext].ContosoRetailTransactionTable** テーブルが作成されます。 テーブルに追加した拡張列に加えて、チャネル側の拡張テーブルにはチャネル側にある元のテーブルと同じ主キー列が必要です。 したがって、[ext].RetailTransactionTable_ContosoRetailExtension には、[ax].RetailTransactionTable で使用される 4 つの主キー列があります。 ベスト プラクティスは、チャンネル側の拡張子テーブルに主キー列を追加するときに、列の名前を元のテーブルの主キー列の名前と同じにしておきます。

+ CDX は、チャネル拡張テーブルからカスタム列をアップロードしてコマースに戻すように構成されています。 RetailCDXSeedDataAX7 リソースには、コマースからチャネル データベースへのテーブル マッピングの情報が含まれています。 CDX はこの情報を使用して、必要なデータ転送スケジューラのジョブとサブジョブを作成します。 データ転送に新しい拡張テーブルまたは列を含めるには、CDX データ転送のカスタマイズを指定するリソース ファイルを提供する必要があります。 ベスト プラクティスは、競合を防ぐため次のような名前付け規則を使用します。 **RetailCDXSeedDataAX7_ContosoRetailExtension**。 (ここでは、**ContosoRetail** は、固有の拡張機能です。)

Retail SDK のサンプル CDX リソース ファイルには、追加のカスタマイズが含まれています。 ただし、RetailTransactionTable 拡張子の例の場合、次のコードのセクションはチャンネル側から HQ にデータをプルするために必要な唯一のセクションです。

```csharp
<RetailCdxSeedData Name="AX7" ChannelDBSchema="ext" ChannelDBMajorVersion="7">
    <Subjobs>
        <!--Adding additional columns to (existing) RetailTransactionTable and wants to pull it back to HQ.For upload subjobs, set the OverrideTarget property to  "false", as ilustrated below. This will tell CDX to use the table defined by TargetTableName and TargetTableSchema as extension table on this subjob.-->
        <Subjob Id="RetailTransactionTable" TargetTableName ="CONTOSORETAILTRANSACTIONTABLE" TargetTableSchema="ext" OverrideTarget="false">
            <!--Notice that there is no mention of the <ScheduledByJobs></ScheduledByJobs> because the subjob is already part of an upload job. -->
            <AxFields>
                <!--If you notice the existing columns are not listed here in the <Field> tag, it's because the existing fields are already mapped in the main RetailCdxSeedData resource file, we only add the delta here. -->
                <Field Name="ContosoRetailSeatNumber" />
                <Field Name="ContosoRetailServerStaffId" />
            </AxFields>
        </Subjob>
    </Subjobs>
</RetailCdxSeedData>
```

**このリソース ファイルで使用されるフィールドの説明:**

**ChannelDBSchema ='ext'** - リソースがチャンネル データベース内の拡張スキーマから読み取るように、このフィールドが含まれています。

**サブジョブ ID ="RetailTransactionTable"** – SubJob ID がそのテーブルの元のサブジョブ ID と同じであることを確認する必要があります。 そうすると、拡張性フレームワークはユーザーが既存のサブジョブをカスタマイズすることを判断することができます。 新しいサブジョブ di を使用すると、同じテーブルに対してサブジョブの重複エラーが発生します。

**TargetTableName = "CONTOSORETAILTRANSACTIONTABLE"** - チャンネル拡張子のテーブル名。

**TargetTableSchema="拡張"** - チャンネル拡張子スキーマ。 現在のところ、拡張子スキーマ名は外部としてのみサポートします。

**OverrideTarget ="false"** - アップロード サブジョブ (チャンネルから本社にデータを取り込むもの) の場合、OverrideTarget が false に設定されていると、TargetTableName で定義されたテーブルが拡張テーブルであり、サブジョブで既に定義されているプライマリ テーブルに沿ってデータがアップロードされることが CDX に通知されます。

OverrideTarget が "true" に設定されている場合、TargetTableName で定義されたテーブルはサブジョブのプライマリ テーブルをオーバーライドします (プル ジョブでは既定値フィールドが省略され、拡張フィールドのみが考慮されます)。 たとえば、このサンプルでは、この値を true に設定する場合は、これは ax.RetailTransactionTable からデータをアップロードするのではなく、CDX は ext.CONTOSORETAILTRANSACTIONTABLE からのデータのみをアップロードすることを意味します。

指定されたサブジョブがシンクとして使用する **AxTableName** 値をフレームワークが既に判断できるので、**AxTableName** 属性は指定されません。 RetailCDXSeedDataAX7 リソースをカスタマイズする場合は、相違点を指定するだけで済みます。 フレームワークが推定できるすべてのデータは、拡張機能により追加する必要はありません。 同様に、<AXFields></AXFields? セクションでは、カスタム フィールドまたは新しいフィールドのみ指定されているのがわかります。拡張フレームワークにより、指定されたサブジョブ ID からの残りのフィールドのリストが決まるためです。

+ CDX カスタマイズ リソースを持つ CDX モジュールが更新されます。 RetailCDXSeedDataAX7_ContosoRetailExtensionで指定されているカスタマイズを適用するには、registerCDXSeedDataExtension デリゲートを購読する必要があります。 このイベントをサブスクライブすることで、CDX シード データの初期化が実行されるときにカスタマイズが適用されることを保証できます。

#### <a name="subscribe-to-the-registercdxseeddataextension-delegate"></a>registerCDXSeedDataExtension デリゲートにサブスクライブ

1. **表示** > **アプリケーション エクスプローラー** を選択します。
2. **RetailCDXSeedDataBase** クラスを検索します。
3. クラスを右クリックし、**デザイナーで開く** を選択します。
4. デザイナーのデリゲートおよびメソッドの一覧で、**registerCDXSeedDataExtension** デリゲートを選択します。
5. 右クリックし、**イベント ハンドラーのコピー** を選択します。 実装する必要があるメソッド シグネチャがコピーされるため、CDX は CDX シード データのカスタマイズされたリソースを取得します。
6. 新しいクラスを作成し、**ContosoRetailCDXSeedDataAX7EventHandler** などの名前を付けます。 任意の名前を指定することができます。 ただし、ベスト プラクティスとしては、接頭語をクラス名の前に付けてください。
7. 手順 5 でコピーしたコードを貼り付けます。

    ```csharp
    class ContosoRetailCDXSeedDataAX7EventHandler
    {
        /// <summary>
        /// Registers the extension CDX seed data resource to be used during CDX seed data generation.
        /// </summary>
        /// <param name="result">The result object which is used to return the resource name.</param>
        [SubscribesTo(classStr(RetailCDXSeedDataBase), delegateStr(RetailCDXSeedDataBase, registerCDXSeedDataExtension))]
        public static void RetailCDXSeedDataBase_registerCDXSeedDataExtension(str originalCDXSeedDataResource, List resources)
        {
        }
    }
    ```

8. CDX 機能拡張フレームワークは、コマースの初期化を選択するとこのメソッドを呼び出します。 CDX 拡張モジュールが CDX カスタマイズを使用するようにするためには、上記のメソッドに次のコードを貼り付けます。

    ```csharp
    if (originalCDXSeedDataResource == resourceStr(RetailCDXSeedDataAX7))
    {
        resources.addEnd(resourceStr(RetailCDXSeedDataAX7_ContosoRetailExtension));
    }
    ```

    カスタム リソースをリストに追加する前に、処理中の originalCDXSeedDataResource リソースが RetailCDXSeedDataAX7 であることを確認する必要があります。 そうしないと、予期しない結果が生じる場合があります。

9. カスタマイズした構成で CDX モジュールを初期化または再初期化するには、次の手順を実行します。

   1. **Retail と Commerce** > **バックオフィスの設定** > **コマース スケジューラ** > **スケジューラ ジョブ** > **コマース スケジューラの初期化** に移動します。
   2. 表示されるダイアログ ボックスで、**既存のコンフィギュレーションの削除** を選択します。
   3. **OK** を選択して、初期化を開始します。

      初期化が完了したとき、CDX スケジューラ ジョブ、サブジョブの定義、および配布スケジュールは、元の RetailCDXSeedDataAX7 リソースとカスタマイズされた RetailCDXSeedDataAX7_ContosoRetailExtension リソースを使用して更新されます。

#### <a name="validate-the-customization"></a>カスタマイズの検証

1. カスタマイズが正しく動作することを確認します。

    1. 初期化が完了した後、**Retail と Commerce** > **バックオフィスの設定** > **コマース スケジューラ** に移動し、**スケジューラ サブジョブ** リンクを選択します。
    2. サブジョブ テーブルで、**RetailTransactionTable** サブジョブ ID を検索します。
    3. 詳細領域の **チャネル フィールド マッピング** セクションで、新しいカスタム (拡張) 列がマッピングに表示されていることを確認します。

2. CDX ジョブのアップロード、およびチャネル側の元のテーブルと拡張テーブルからのプルをテストします (元のテーブルと拡張可能なテーブルを組み合わせたビューが、CDX フレームワークによって生成されます)。

    1. Retail Modern POS (MPOS) でいくつかのトランザクションを作成します。
    2. 拡張テーブルは Commerce Runtime (CRT) および MPOS では使用されないため、拡張テーブルに手動でデータを挿入する必要があります。 必要な値を変更した後、次のスクリプトを実行します。

        ```sql
        INSERT INTO [ext].[CONTOSORETAILTRANSACTIONTABLE] (
        [CONTOSORETAILSEATNUMBER],
        [CONTOSORETAILSERVERSTAFFID],
        [TRANSACTIONID],
        [STORE],
        [CHANNEL],
        [TERMINAL],
        [DATAAREAID])
        VALUES (
        1, /*normally this needs to be an existing seat number from ContosoRetailSeatingData table, but for this test add any number*/
        '000160' /*add any staff ID here*/,
        'HOUSTON-HOUSTON-11-101',/\*add the transaction id you just created */
        'HOUSTON', /*add the store used to create the transaction */
        5637144592, /*add the channel RecId of the store used to create the transaction*/
        'HOUSTON-11', /*add the terminalId used to create the transaction*/
        'USRT' /*add the dataareaId used by the store*/)
        GO
        ```

        他のトランザクションにもこの手順を繰り返します。 MPOS で作成したトランザクションの一部 [ext].[CONTOSORETAILTRANSACTIONTABLE] に対応するデータを追加しないでください。 この方法で、拡張テーブルに対応するデータがない場合でも、[ax].RetailTransactionTable からデータを取得してアップロードすることを確認できます。

    3. **Dynamics 365** > **Retail と Commerce** > **Retail とコマース IT** に移動し, **配送スケジュール** を選択します。
    4. 配送スケジュールの一覧で、**P-0001** を選択します。 この配布スケジュールには、カスタマイズした RetailTransactionTable のサブジョブが含まれています。
    5. アクション ウィンドウで、**実行** を選択します。 確認メッセージが表示されたら、**はい** を選択します。
    6. アクション ウィンドウで、**履歴** を選択し **履歴** ページを開き、アップロードされたセッションが正常に完了したことを確認できます。
    7. **履歴** ページで、新しいアップロード セッション レコードがあることを確認します。 レコードのステータスが **申請済** に設定され、さらに **影響を受けた行** 値は **0** (ゼロ) でないことを確認してください。

3. アップロード セッションが正常に適用されたら、**Retail と Commerce** > **照会やレポート** > **店舗のトランザクション** に移動し、アップロードした新しいトランザクションを検索します。 トランザクション、シート番号、およびサーバー スタッフ ID の各カスタム列に期待された値が入っていることを確認します。

    また、チャネル側の [ext].ContosoRetailTransactionTable 拡張テーブルに対応するレコードを持たないトランザクションもアップロードされていることを確認します。 これらのトランザクションにシート番号とサーバー スタッフ ID の既定値が含まれていることを確認します。 シート番号は **0** (ゼロ) に設定し、サーバー スタッフ ID は **000160** に設定する必要があります。

#### <a name="mpos-offline-transaction-sync"></a>MPOS オフライン トランザクションの同期

 MPOS をオフライン モードに切り替えて、トランザクションを実行します。 オンラインに切り替えて、データがオフライン データベースからチャネル データベースに、次いでバックオフィスに正しく同期されていることを確認します。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]