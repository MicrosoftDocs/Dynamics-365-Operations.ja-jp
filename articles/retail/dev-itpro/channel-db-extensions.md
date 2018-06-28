---
title: "チャネル データベース (DB) 拡張機能"
description: "このトピックでは、チャネル データベースを拡張する方法について説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 12/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-09-15
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: c1958f8ffabba121dc0992dd70fae16021365705
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="channel-database-db-extensions"></a>チャネル データベース (DB) 拡張機能

[!include [banner](../../includes/banner.md)]

チャネル データベース (チャネル DB) は、オンライン ストアまたはブリックアンドモルタル ストアなどの 1 つまたは複数の小売チャネルからのトランザクションおよびマスターデータを保持します。 マスター データは、Commerce Data Exchange (CDX) を使用して小売用バックオフィス (Retail HQ) からチャネル データベースに適用されます。 チャネル データベースに格納されたトランザクション データは、CDX を使用して本社に引き戻されます。

このトピックでは、さまざまなシナリオのチャネル データベースを拡張する方法について説明します。 ここで説明したステップは、Dynamics 365 for Retail、Dynamics 365 for Finance and Operations にのみ適用されます。

拡張機能のさまざまなシナリオを説明する前に、チャネル DB 拡張機能の最新の機能拡張を理解することが重要です。 

アップグレード時のカスタマイズの処理の方法にいくつかの改善を加えました。 以下の環境構成のいずれかを使用することをお勧めします。
- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (2017 年 7 月) アプリケーション更新プログラム 5
- Microsoft Dynamics 365 for Retail 7.2 アプリケーション更新プログラム 5 はすぐに入手できるようになります。
- Microsoft Dynamics 365 for Retail 7.3 には、アプリケーション更新プログラム 5 が含まれます。
- アプリケーション更新プログラム 5 を含む Microsoft Dynamics 365 for Finance and Operations 7.3。

## <a name="ext-schema"></a>Ext スキーマ

Dynamics 365 for Retail および Dynamics 365 Finance and Operations では、**ext スキーマ**と呼ばれる新しいスキーマを導入して拡張機能をサポートしました。 以前のバージョンでは、チャネル DB に拡張機能を追加する場合、CRT または AX スキーマに追加していました。 Dynamics 365 for Retail および Dynamics 365 for Finance and Operations バージョンでは、CRT、AX、または DBO スキーマを変更することはできません。 すべての変更は **ext スキーマ**で行う必要があります。 CRT または AX スキーマで変更する場合は、Lifecycle Service での配置は失敗します。 CRT、AX、および DBO スキーマを変更する権限を持たないエラー レポート。 

## <a name="best-practices-for-channel-db-extensions"></a>チャネル DB 拡張機能のためのベスト プラクティス

- CRT、AX、または DBO スキーマ内では何も変更しないでください。 すべての拡張シナリオで **ext スキーマ**を使用します。
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

配置プロセスは、データベースのコンポーネントに変更があるかどうかを判断します。 CRT、AX、または DBO スキーマ オブジェクトを変更しようとした場合、または SQL で直接シナリオに対してそれらにアクセスすると、展開は失敗します。


