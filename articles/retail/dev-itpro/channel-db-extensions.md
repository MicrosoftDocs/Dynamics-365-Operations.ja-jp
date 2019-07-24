---
title: チャネル データベース 拡張機能
description: このトピックでは、チャネル データベースを拡張する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-09-15
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.openlocfilehash: f26f18c782541470ce50407d25636f570a6443d4
ms.sourcegitcommit: 4ae431bae554776df880a3992e21103aee7b64f0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/20/2019
ms.locfileid: "1694403"
---
# <a name="channel-database-extensions"></a>チャネル データベース 拡張機能

[!include [banner](../../includes/banner.md)]

チャネル データベース (チャネル DB) は、オンライン ストアまたはブリックアンドモルタル ストアなどの 1 つまたは複数の小売チャネルからのトランザクションおよびマスターデータを保持します。 Commerce Data Exchange (CDX) を使用して、Retail Headquarters マスター データは (Retail HQ) からチャネル データベースにプッシュされます。 チャネル データベースに格納されたトランザクション データは、CDX を使用して本社に引き戻されます。

このトピックでは、さまざまなシナリオのチャネル データベースを拡張する方法について説明します。 以下の手順は、Dynamics 365 for Retail、Dynamics 365 for Finance and Operations にのみ適用します。

拡張機能のさまざまなシナリオを説明する前に、チャネル DB 拡張機能の最新の機能拡張を理解することが重要です。 

アップグレード時の拡張機能の処理の方法にいくつかの改善を加えました。 以下の環境構成のいずれかを使用することをお勧めします。
- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月) およびアプリケーション更新プログラム 5
- Microsoft Dynamics 365 for Retail 7.2 およびアプリケーション更新プログラム 5 (まもなく利用できます)
- Microsoft Dynamics 365 for Retail 7.3 (アプリケーション更新プログラム 5 を含みます)
- Microsoft Dynamics 365 for Finance and Operations 7.3 (アプリケーション更新プログラム 5 を含みます)

## <a name="ext-schema"></a>Ext スキーマ

Dynamics 365 for Retail および Dynamics 365 Finance and Operations では、**ext スキーマ**と呼ばれる新しいスキーマを導入して拡張機能をサポートしました。 以前のバージョンでは、チャネル DB に拡張機能を追加する場合、CRT または AX スキーマに追加していました。 小売および Finance and Operations の両方のスキーマを変更CRT、AX、または DBO スキーマを変更することはできません。 すべての変更は **ext スキーマ**で行う必要があります。 CRT または AX スキーマの何かを変更すると、Lifecycle Services (LCS) での展開に失敗します。 CRT、AX、および DBO スキーマを変更する権限がありませんというエラーが報告されます。

> [!NOTE]
> いずれかのチャネル DB フィールドの長さを伸ばす場合は、LCS で拡張機能の要求を作成し、EDT の伸長または小数点以下の精度を高める必要があります。 Dynamics 365 Finance and Operations は、変更をチャネル DB に自動的にプッシュしません。また、拡張子には、チャネル DB - CRT、AXまたは DBO スキーマでなにかを変更または修正するための許可が付与されません。 CRT または AX スキーマの何かを変更すると、LCS での展開が失敗します。 

## <a name="best-practices-for-channel-db-extensions"></a>チャネル DB 拡張機能のためのベスト プラクティス

- CRT、AX、または DBO スキーマのいずれも変更しないでください。 すべての拡張シナリオで **ext スキーマ**を使用します。
- **ext schema** 内で、CRT、AX、または DBO オブジェクトにアクセスしないでください。 任意のチャネル データベース コンポーネントにアクセスするには、商取引ランタイム データ サービスを使用する必要があります。

### <a name="dont-do-this"></a>このようにしない
以下はユーザーがしてはいけないことの例です。 代わりに、主キーの値を取得するために CRT データ サービスを使用してから、拡張テーブルに挿入するために主キーの値を使用する必要があります。

```sql
MERGE INTO [ax].RETAILCUSTPREFERENCE   --DONT access ax schema object
USING (SELECT DISTINCT
tp.PARENTRECID, tp.PROPERTYVALUE as [EMAILOPTIN], ct.ACCOUNTNUM, ct.DATAAREAID
FROM @TVP_EXTENSIONPROPERTIESTABLETYPE tp
JOIN [ax].CUSTTABLE ct on ct.RECID = tp.PARENTRECID  --DONT access ax schema object
WHERE tp.PARENTRECID <> 0 and tp.PROPERTYNAME = 'EMAILOPTIN') AS SOURCE
ON [ax].RETAILCUSTPREFERENCE.RECID = SOURCE.PARENTRECID   
and [ax].RETAILCUSTPREFERENCE.DATAAREAID = SOURCE.DATAAREAID --DONT access ax schema object
and [ax].RETAILCUSTPREFERENCE.ACCOUNTNUM = SOURCE.ACCOUNTNUM
WHEN MATCHED THEN
UPDATE SET [EMAILOPTIN] = source.[EMAILOPTIN]
WHEN NOT MATCHED THEN
INSERT
(
    RECID
    ,DATAAREAID
    ,EMAILOPTIN
    ,ACCOUNTNUM
)
VALUES
(
    SOURCE.PARENTRECID
    ,SOURCE.DATAAREAID
    ,SOURCE.EMAILOPTIN
    ,SOURCE.ACCOUNTNUM
);
SELECT @i_Error = @@ERROR;
IF @i_Error <> 0
    BEGIN
    SET @i_ReturnCode = @i_Error;
    GOTO exit_label;
END;
```


### <a name="dont-do-this"></a>このようにしない
- 拡張テーブルまたは新しいテーブルを作成する場合、すべてを ext スキーマで行う必要があります。
- ビュー、手順、関数、またはデータベースのコンポーネントを変更しないでください。
- 拡張子からのビュー、定義されたタイプ、関数および手順を含むデータベースのコンポーネントにアクセスしたり、呼び出したりしないでください。
- データベースのアーティファクトにアクセスするには、CRT データ サービスを使用します。 たとえば、一部のカスタム フィールドを検索する、または仕訳帳のビューにカスタム列を表示する製品検索ビューを拡張するとします。 SQL 内では、ビューまたは手順、機能を変更しないでください。 代わりに、CRT データ サービスを使用して、投稿トリガーをオーバーライドまたは使用することによって拡張機能を実行し、拡張プロシージャを呼び出します。

```sql
CREATE VIEW [ext].[CONTOSORETAILSTOREHOURSVIEW] AS
(
    SELECT
    sdht.DAY,
    sdht.OPENTIME,
    sdht.CLOSINGTIME,
    sdht.RECID,
    rst.STORENUMBER
    FROM [ext].[CONTOSORETAILSTOREHOURSTABLE\] sdht
    INNER JOIN [ax].RETAILSTORETABLE rst ON rst.RECID = sdht.RETAILSTORETABLE  --DONT access ax schema object
)
```

## <a name="adding-extensions"></a>拡張機能の追加
1. すべての拡張機能テーブルは **UserRole** および **DeployExtensibilityRole** にアクセス許可を付与する必要があります。

    ```sql
    GRANT EXECUTE ON [ext].[EXTTABLENAME] TO [DeployExtensibilityRole];
        GO
        GRANT EXECUTE ON [ext].[EXTTABLENAME] TO [UsersRole];
        GO
    ```

2. テーブルが HQ から受信するデータを送信する場合、**DataSyncUsersRole** アクセス許可を付与します。

    ```sql
    GRANT SELECT, INSERT, UPDATE, DELETE ON OBJECT::[ext].[EXTTABLENAME] TO [DataSyncUsersRole]
    GO
    ```

3. 拡張テーブルを作成し、HQ にデータを同期させる場合は、拡張テーブルに親テーブルの主な列を含めます。
4. たとえば、**ContosoRetailTransactionTable** など、常にテーブルに接頭語を付けると、他のパートナー/ISV カスタマイズとの競合を回避できます。

## <a name="attributes"></a>属性

顧客、顧客の注文、現金売りトランザクション、およびコール センター注文の属性をサポートするために、HQ の属性フレームワークを拡張しました。

### <a name="customer-attributes"></a>顧客属性
新しい顧客属性フレームワークでは、構成を使用して、POS または HQ 内の顧客追加/編集画面または顧客詳細画面に新しいフィールドを追加することができます。 小売パラメーターで顧客属性グループを構成した後、POS や HQ はコードの変更やカスタマイズを行わずに新しい属性を自動的に表示します。 画面レイアウト設計者は、取引画面 (**顧客** パネル) に顧客属性を表示するようにも設定されます。

### <a name="order-attributes"></a>注文属性
属性フレームワークは、現金売りトランザクション、顧客の注文、およびコール センター注文の属性をサポートするように拡張されました。 HQ または CRT で値を直接編集して設定することができます。 これらすべてはデータベースを変更せずにコンフィギュレーションを介して実行することができます。 (基本的な CRUD 操作は必要ではなく、主要なビジネス ロジックの属性値をカスタマイズすることができます。) 以前は、これを行うには、HQ とチャンネル DB に新しいテーブルを作成し、CRT を変更する必要がありました。 現在は、すべての属性の作成をコンフィギュレーションを通じて実行できるようになりました。 

## <a name="adding-a-new-table"></a>新しいテーブルの追加

このシナリオでは、新しいテーブルを作成し、チャネル DB に追加する方法について説明します。 すべての拡張コードは **ext スキーマ**へアクセスすることができます。

1. SQL Server Management Studio デザイナーを使用するか、SQL スクリプトを使用して、**ext スキーマ**のチャネル データベースに新しいテーブルを作成します。 以下は、SQL スクリプトの例です。

    ```sql
    -- Create the extension table to store the custom fields.
    IF (SELECT OBJECT_ID('[ext].[CONTOSORETAILSTOREHOURSTABLE]')) IS NULL
    BEGIN
    CREATE TABLE [ext].[CONTOSORETAILSTOREHOURSTABLE](
    [RECID] [bigint] NOT NULL,
    [DAY] [int] NOT NULL DEFAULT ((0)),
    [OPENTIME] [int] NOT NULL DEFAULT ((0)),
    [CLOSINGTIME] [int] NOT NULL DEFAULT ((0)),
    [RETAILSTORETABLE] [bigint] NOT NULL DEFAULT ((0)),
    CONSTRAINT [I_CONTOSORETAILSTOREHOURSTABLE_RECID] PRIMARY KEY CLUSTERED
    (
        [RECID] ASC
    ) WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
    ) ON [PRIMARY]
    ALTER TABLE [ext].[CONTOSORETAILSTOREHOURSTABLE] WITH CHECK ADD CHECK (([RECID]<>(0)))
    END
    GO
    GRANT SELECT, INSERT, UPDATE, DELETE ON OBJECT::[ext].[CONTOSORETAILSTOREHOURSTABLE] TO [DataSyncUsersRole]
    GO

## Extending an existing table

If you are extending existing table, then you must either use attributes if supported for that entity or create and extended table (new table) with same primary key as the parent table. The following script extends a table.

```sql
CREATE TABLE [ext].[RETAILTRANSACTIONTABLE](
[TRANSACTIONID] [nvarchar](44) NOT NULL, -- FK to [crt].RETAILTRANSACTIONTABLE
[ISB2BSALES] [int] NOT NULL DEFAULT (0),
[EXTERNALID] [nvarchar](20) NOT NULL DEFAULT (''),
CONSTRAINT [EXT_RETAILTRANSACTIONTABLE_PK] PRIMARY KEY CLUSTERED
(
    [TRANSACTIONID]
) WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
     ) ON [PRIMARY]
GO
GRANT INSERT ON [ext].[RETAILTRANSACTIONTABLE] TO [DataSyncUsersRole];
GO
GRANT DELETE ON [ext].[RETAILTRANSACTIONTABLE] TO [DataSyncUsersRole];
GO
GRANT UPDATE ON [ext\].[RETAILTRANSACTIONTABLE] TO [DataSyncUsersRole];
GO
GRANT SELECT ON [ext].[RETAILTRANSACTIONTABLE] TO [DataSyncUsersRole];
GO
```

## <a name="adding-new-views-stored-procedure-functions-and-defined-types"></a>新しいビュー、ストアド プロシージャ、関数、定義済タイプの追加

すべての新しいストアド プロシージャ、ビューまたは機能は **ext スキーマ**に作成する必要があります。 手順、ビューまたは機能から、データベース コンポーネントをアクセスするまたは呼びだすことはやめてください。

## <a name="deployment-checks"></a>配置のチェック

配置プロセスは、データベースのコンポーネントに変更があるかどうかを判断します。 CRT、AX、または DBO スキーマ オブジェクトを変更しようとした場合、またはどのシナリオの場合でも SQL でそれらに直接アクセスすると、展開は失敗します。

## <a name="extension-scripts-and-deployment"></a>拡張スクリプトおよび展開

チャンネル データベース拡張は、1 つまたは複数の T-SQL スクリプト ファイルを作成し、[展開可能なパッケージ](./retail-sdk/retail-sdk-packaging.md)に含めることで用意されます。 このプロセスについては、[Retail SDK](./retail-sdk/retail-sdk-overview.md) ドキュメントで説明します。

拡張スクリプト ファイルは、[T-SQL](https://docs.microsoft.com/en-us/sql/t-sql/language-reference) を使用して記述され、[Azure SQL データベース](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-features)と互換性があります。
スクリプト ファイルの末尾は *.sql* ファイル拡張子にする必要があります。その他のファイルは無視されます。または、パッケージングまたは配置障害を引き起こす可能性があります。 Retail Store Scale Unit または Modern POS の一部としてオフラインでチャネル データベース拡張機能を展開する場合、スクリプトは、それらのコンポーネントに対して使用される SQL Express または SQL Server のバージョンの両方またはいずれかと互換性があることも必要です。

配置とインストール中、拡張子スクリプトは、スクリプト ファイル名に基づいたアルファベット順で実行されます。
各スクリプトは、完了するまで実行され、拡張スクリプトの完了を追跡するため、メタデータ レコードはチャンネル データベースの CRT.RETAILUPGRADEHISTORY テーブルに追加されます。
そのメタデータ レコードが存在する場合、その後の展開で同じチャネル データベースに対してスクリプトが再度実行されることはありません。
スクリプトが実行中に失敗し、正常に完了しない場合、そのメタデータは保存されず、以降の配置でスクリプトが再実行されます。

展開やインストールが製品の更新と組み合わされている場合、拡張スクリプトは製品の更新後に実行されます。

正常に行われるチャネル データベース拡張を作成するには、次のガイドラインに従う必要があります。

### <a name="use-a-naming-convention-that-ensures-stable-order-when-sorted-alphabetically"></a>アルファベット順に並べ替えられたときに、安定した順序が確保される名前付け規則を使用します。

拡張スクリプトは、ファイル名に基づくアルファベット順に実行されるので、並べ替えたときに正しい実行順序が使用される名前付け規則を確立する必要があります。

1 つの例は、次のパターンを持つファイルの名前付けです: "<ISO 8601 date>_<descriptio>.sql"。ここで **<ISO 8601 date>** は ISO 8601 形式の日付で、**<description>** はスクリプトの目的を識別するための説明のテキストです。
たとえば、*"20180501_CustomerDetails.sql"* と *"20181102_CustomerDetailsIndex.sql"* などです。
前者は、「顧客の詳細」機能に関連する 2018 年 5 月 1 日に作成された拡張スクリプトを表しており、後者は、2018 年 11 月 2 日に作成された以前の機能に関連するインデックスに関連付けられている拡張スクリプトです。

別の単純な方法は、"0001_CustomerDetails.sql" や "0002_CustomerDetailsIndex.sql" などの差分数値接頭語を使用する方法です。

1 つのスクリプトが正常に実行される別のスクリプトに依存している場合、アルファベット順のファイル名が必要な実行順序と一致していることを確認する方法で命名する必要があります。

### <a name="do-not-alter-extension-scripts-that-have-been-published"></a>発行された拡張スクリプトを変更しないでください。

展開可能なパッケージまたはチャンル データベース拡張スクリプトを含むインストーラー拡張をリリースした場合、それらのスクリプトを変更しないでください。 拡張スクリプトは、チャネル データベース インスタンスあたり 1 回だけ実行されます。
既にスクリプトを発行しており、それらのスクリプトがチャネル データベースに対して実行済の場合、既に実行されたスクリプトへの変更はデータベースには適用されません。

代わりに、新しいスクリプト ファイル内の変更を提供します。 依存関係の後に実行されるように、上記の名前付け規則を検討してください。

### <a name="do-not-remove-old-extension-scripts-that-have-been-published"></a>発行された以前の拡張スクリプトを削除しないでください。

展開可能なパッケージまたはインストーラー拡張機能は、データベースの拡張機能の累積的な更新を表す必要があります。 拡張機能パッケージまたはインストーラーの以前のバージョンには依存関係はありません。 ユーザーは、パッケージまたは拡張機能の以前のバージョンに依存しなくても拡張機能パッケージやインストーラーを適用できる必要があります。

拡張スクリプトが展開可能なパッケージまたはインストーラー拡張の一部として公開されている場合、パッケージまたはインストーラーの以降の更新から削除しないでください。 災害復旧、アップグレード、スケール アウト シナリオに対応するため、チャンル データベースの新しいインスタンスを同じバージョンの最後に配置された拡張機能パッケージに持ち込むために拡張パッケージを使用できます。

### <a name="extension-scripts-must-be-idempotent-and-reentrant"></a>拡張スクリプトは、非べき等および再入力である必要がある

拡張スクリプトはチャネル データベースあたり 1 回だけ実行されますが、スクリプトはオーサリング エラーまたはタイムアウトやトランザクション デッドロックなどの一時的な SQL エラーが原因で実行されない場合があります。 拡張スクリプトは、それらの障害シナリオに対応するため、非べき等および再入力である必要があります。
拡張スクリプトがエラーが原因で失敗した場合、再実行できます。 スクリプトを再実行しても、データベースに悪影響を及ぼしません。

### <a name="do-not-assume-that-the-channel-database-data-is-perennial"></a>チャネル データベース データが永続すると仮定しない

チャネル データベースは、Retail サーバーで実行される操作の記憶域サポートを提供するトランザクション データベースです。 長期間保存する必要があるチャネル データベースに格納されるすべてのデータは、[Commerce Data Exchange](./cdx-extensibility.md) を通じて本社にアップロードする必要があります。 本社にアップロードされたデータには、[Commerce Data Exchange リアルタイム サービス](./extend-commerce-data-exchange.md)によりアクセスすることができます。
