---
title: Dynamics AX 2012 環境でテーブルを圧縮する
description: このトピックでは、Microsoft Dynamics AX 2012 環境でテーブルを圧縮する方法について説明します。
author: ttreen
ms.date: 05/23/2022
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: ttreen
ms.search.validFrom: ''
ms.search.form: 2022-04-08
ms.openlocfilehash: 78dac5b34461998dff886b2613a7a1e18ec36ac7
ms.sourcegitcommit: 771465b63c9d919f043316a54b8e2b9b2e0605cc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/24/2022
ms.locfileid: "8794525"
---
# <a name="compress-tables-in-microsoft-dynamics-ax-2012-environments"></a>Microsoft Dynamics AX 2012 環境でテーブルを圧縮する

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics AX 2012 環境でテーブルを圧縮する方法について説明します。

## <a name="background"></a>背景

セルフ サービス環境で Dynamics 365 にアップグレードすると、大規模なデータベースを持つ Dynamics AX 2012 環境では、次の例のようなエラーが生成される場合があります。

> 管理対象のテーブル ワーカーの同期で例外が検出されましたが、ContinueOnError が true のため続行されています。 次のテーブルでテーブル同期が失敗しました: TaxTrans。 例外: System.InvalidOperationException: データベースの実行に失敗しました: エラスティック プールが記憶域の上限に達しています。 エラスティック プールの記憶域の使用量が (4194304) MBs を超えることはできません。  
明細書は終了しました。

このタイプのエラーを回避する 1 つの方法は、アップグレード前にテーブル データとインデックス データを圧縮し、Dynamics AX 2012 ソース データベースのサイズを小さくすることです。

Dynamics 365 では、ページ データまたは行データ圧縮を使用して、テーブルとインデックスを圧縮できます。

ほとんどの Dynamics AX 2012 の顧客は圧縮を既定にしませんが、後から有効にできます。 圧縮が有効にされた場合、Dynamics 365 に複製されたデータも圧縮されます。 この圧縮は、アップグレードを完了するために十分なデータベースの容量を解放するはずです。

## <a name="prerequisites"></a>必要条件

テーブルを圧縮する前に、次の前提条件が満たされている必要があります。

> [!NOTE]
> テーブルの圧縮ステータスを複製するには、2022 年 3 月 30 日以降のバージョンの AX 2012 Database Upgrade Toolkit for Dynamics 365 を使用する必要があります。 それ以前のリリースでは、圧縮フラグはサポートされていません。

### <a name="identify-tables-for-compression"></a>圧縮するテーブルを識別する

圧縮するテーブルを識別するには、次の手順に従います。

1. SQL Management Studio を開き、Dynamics AX 2012 データベースをホストするサーバーに接続します。
1. オブジェクト エクスプローラで、使用している Dynamics AX 2012 データベースを選択したまま (または右クリックし)、**レポート \> 標準レポート \> トップ テーブルによるディスク用途** を選択して **トップ テーブルによるディスク用途** を実行します。
1. レポートの結果を確認して、どのテーブルがストレージを一番多く使用しているかを特定します。 これらのテーブルを圧縮することで、アップグレードするために十分な容量を解放できるはずです。

### <a name="configure-dynamics-ax-2012-for-the-upgrade"></a>アップグレード用の Dynamics AX 2012 を構成する

アップグレード用に Dynamics AX 2012 を構成するには、次の手順を実行します。

1. Dynamics AX 2012 開発ワークスペースから、**SysSqlSetup** フォームを検索して開きます。 このフォームを開くのに数分間かかる場合があります。
1. **テーブル** ドロップダウン リストで、圧縮するテーブル (**RetailTtransactionSalesTrans** など) のいずれかを検索して選択します。
1. **圧縮を有効化** チェック ボックスをオンにし、**ページ** または **行** を選択して、**保存** を選択します。
1. **選択したテーブルのすべてのインデックス** を選択し、**圧縮を有効化** チェック ボックスをオンにし、**ページ** または **行** を選択して、**保存** を選択します。
1. 圧縮するテーブルごとに手順 2 から 4 を繰り返します。

> [!TIP]
> 次の SQL クエリを使用して、圧縮を設定したテーブルを特定できます。
>
> ```SQL
> select t2.name as TABLENAME, t1.*
> from sqlstorage t1
> join sqldictionary t2 on t1.TABLEID = t2.TABLEID and t2.FIELDID = 0 
> ```

## <a name="compress-the-tables"></a>テーブルを圧縮する

テーブルを圧縮するには 2 つのオプションがあります。

- **[オプション 1: SysSqlAdmin フォーム](#option-1-compress-the-tables-from-the-syssqladmin-form)** からテーブルを圧縮する – **SysSqlAdmin** フォームの 1 つの制限は、テーブルの圧縮が選択的でないということです。 つまり、処理するテーブルは選択できません。 圧縮は常に、圧縮を設定したすべてのテーブルに対して処理されます。 ただし、インデックスの圧縮は選択的 *です*。 このプロセスを制御したいなら、特にライブ データベースの場合は、オプション 2 が適しているかもしれません。
- **[オプション 2: SQL スクリプトを実行する](#option-2-run-a-sql-script)** – このオプションはより細かいもので、さらなる制御が可能です。

### <a name="option-1-compress-the-tables-from-the-syssqladmin-form"></a>オプション 1: SysSqlAdmin フォームからテーブルを圧縮する

**SysSqlAdmin** フォームからテーブルを圧縮するには、次の手順に従います。

1. Dynamics AX アプリケーション オブジェクト ツリー (AOT) で、**SysSqlAdmin** フォームを検索して開きます。
1. ドロップダウン メニューで、**テーブル アクション \> 圧縮の適用** を選択します。
1. 以前に有効にした各テーブルを検索して選択し、ドロップダウン メニューで **インデックス アクション \> インデックスの再作成** を選択します。
1. 次の SQL スクリプトを実行して、圧縮が有効にされたことを確認します。

    ```SQL
    -- Tables with Compression
    SELECT T2.name AS TableName, 
        T1.partition_number AS Partition,
        T1.data_compression_desc AS CompressionType
    FROM sys.partitions AS T1
    INNER JOIN sys.tables AS T2 ON T2.object_id = T1.object_id
    WHERE T1.index_id in (0,1)
    AND T1.data_compression_desc != 'NONE'
    ORDER BY T2.name

    -- Indexes with Compression
    SELECT T2.name AS TableName, 
        T3.name AS IndexName,
        T1.partition_number AS Partition,
        T1.data_compression_desc AS Compression
    FROM sys.partitions AS T1
    INNER JOIN sys.tables AS T2 ON T2.object_id = T1.object_id
    INNER JOIN sys.indexes AS T3 ON T3.object_id = T1.object_id AND T3.index_id = T1.index_id
    WHERE T1.index_id > 1
    AND T1.data_compression_desc != 'NONE'
    ORDER BY T2.name, T3.name 
    ```

### <a name="option-2-run-a-sql-script"></a>オプション 2: SQL スクリプトを実行する

このオプションでは、Dynamics AX 2012 データベースに対して次の SQL スクリプトを実行する必要があります。 まずテーブルの一覧 (スクリプトでコメントされている) を編集し、圧縮するテーブルを含むようにします。 既定では、スクリプトはテーブルのインデックスも圧縮します。 ただし、(スクリプトにコメントされているとおり) その機能は無効にできます。

```SQL
--
-- This source code or script is freeware and is provided on an "as is" basis without warranties of any kind, 
-- whether express or implied, including without limitation warranties that the code is free of defect, 
-- fit for a particular purpose or non-infringing. The entire risk as to the quality and performance of 
-- the code is with the end user.
--

-- This script uses PAGE compression, if you wish to use ROW compression you will need to edit the script

-- Edit the list below to include the tables you want to compress
DECLARE @tablestocompress NVARCHAR(MAX) = 'TABLE1, TABLE2, TABLE3, TABLE4, TABLE4, TABLE6'

-- If you want to disable the index compression, set the following to 0 
DECLARE @compressIndexes BIT = 1;

-- Script Code Block - Start
DECLARE @tablename NVARCHAR(256), @indexName NVARCHAR(256)
DECLARE @dataCompression TINYINT;
DECLARE @sql NVARCHAR(MAX);
DECLARE @xml XML
DECLARE @errors BIT

set @tablestocompress = REPLACE(@tablestocompress,' ', '')
set @xml = (SELECT CAST('<cr>'+REPLACE(@tablestocompress, ',', '</cr><cr>')+'</cr>' AS XML) AS STRING) 
set @errors = 0

-- Check tables in list exist
DECLARE tableCursor CURSOR FOR 
    select t.value('.','varchar(max)') as TABLESTOCOMPRESS from @xml.nodes('//cr') as a(t);
OPEN tableCursor;
FETCH NEXT FROM tableCursor INTO @tablename;
WHILE @@FETCH_STATUS = 0
    BEGIN
        IF NOT EXISTS (SELECT name from sys.tables where name = @tablename and schema_id = (select schema_id from sys.schemas where name = 'DBO')) 
        BEGIN
            IF (@errors) = 0
            BEGIN
                PRINT 'Some tables entered do not exist, please check the list you edited and the tables below...';
            END
            SET @errors = 1;
            PRINT @tablename + ' table does not exist';
        END
        FETCH NEXT FROM tableCursor INTO @tablename;
    END
CLOSE tableCursor;
DEALLOCATE tableCursor;

IF (@errors) = 0
BEGIN
    -- All Tables In List were Present
    -- Start Compression
    DECLARE tableCursor CURSOR FOR 
        select t.value('.','varchar(max)') as TABLESTOCOMPRESS from @xml.nodes('//cr') as a(t);
    OPEN tableCursor;
    FETCH NEXT FROM tableCursor INTO @tablename;
    WHILE @@FETCH_STATUS = 0
        BEGIN
            IF EXISTS (SELECT T1.data_compression_desc FROM sys.partitions AS T1 
                INNER JOIN sys.tables AS T2 ON T2.object_id = T1.object_id
                WHERE T1.index_id in (0,1) --0 HEAP, 1 CLUSTERED
                AND T2.object_id = OBJECT_ID(@tablename)
                AND T1.data_compression != 2) --PAGE
            BEGIN
                -- Table is not is not compressed
                PRINT 'Compressing table ' + @tablename + ' with DATA_COMPRESSION = PAGE'
                set @SQL = 'ALTER TABLE DBO.' + @tablename + ' REBUILD PARTITION = ALL WITH (DATA_COMPRESSION = PAGE);'
                EXEC (@SQL);
            END
            ELSE
            BEGIN
                -- Table is already compressed
                PRINT 'PAGE compression already set on table ' + @tablename + ', skipping...'
            END

            IF (@compressIndexes) = 1
            BEGIN
                -- Compress Indexes if not already compressed
                DECLARE indexCursor CURSOR FOR 
                    SELECT T3.name, T1.data_compression 
                    FROM sys.partitions AS T1
                    INNER JOIN sys.tables AS T2 ON T2.object_id = T1.object_id
                    INNER JOIN sys.indexes AS T3 ON T3.object_id = T1.object_id AND T3.index_id = T1.index_id
                    WHERE T1.index_id > 1
                    AND T2.schema_id = (select schema_id from sys.schemas where name = 'DBO')
                    AND T2.name = @tablename;
                OPEN indexCursor;
                FETCH NEXT FROM indexCursor INTO @indexName, @dataCompression;
                WHILE @@FETCH_STATUS = 0
                BEGIN
                    IF (@dataCompression) != 2
                    BEGIN
                        PRINT 'Compressing table index ' + @tableName + '.' + @indexName + ' with DATA_COMPRESSION = PAGE'
                        set @SQL = 'ALTER INDEX ' + @indexName + ' ON DBO.' + @tablename + ' REBUILD PARTITION = ALL WITH (DATA_COMPRESSION = PAGE);'
                        EXEC (@SQL);
                    END
                    ELSE
                    BEGIN
                        PRINT 'PAGE compression already set on table index ' + @tableName + '.' + @indexName;
                    END
                    FETCH NEXT FROM indexCursor INTO @indexName, @dataCompression;
                END
                CLOSE indexCursor;
                DEALLOCATE indexCursor;
            END

            FETCH NEXT FROM tableCursor INTO @tablename;
        END
    CLOSE tableCursor;
    DEALLOCATE tableCursor;
END
-- Script Code Block - End
```
