---
title: "ODBC データ ソースからのデータのインポート"
description: "Microsoft Dynamics AX 2012 のデータのインポート/エクスポート フレームワークを使用すると、ODBC データ ソースからのデータを Microsoft Dynamics AX 2012 にインポートすることができます。"
author: kfend
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 18821
ms.assetid: 3eb200bd-666e-424c-8bd0-9528da4ba880
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: fa3d38e4880d450a775c5e18321fd2e51299db0c
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="import-data-from-odbc-data-sources"></a>ODBC データ ソースからのデータのインポート

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics AX 2012 のデータのインポート/エクスポート フレームワークを使用すると、ODBC データ ソースからのデータを Microsoft Dynamics AX 2012 にインポートすることができます。 

このチュートリアルでは、次の作業について説明します。

-   SQL Server ソース データを作成する
-   ソース データのフォーマットを形式する
-   処理グループの定義
-   ソースからステージングにデータを処理
-   ステージングのデータの検証
-   ステージングからターゲットにデータを処理
-   ターゲットのデータの検証

## <a name="prerequisites"></a>前提条件
このチュートリアルを完了するには、次のものが必要です。

-   Microsoft Dynamics AX 2012、Microsoft Dynamics AX 2012 R2、または Microsoft Dynamics AX 2012 R3。
-   データのインポート/エクスポート フレームワーク

## <a name="create-a-sql-server-data-source"></a>SQL Server ソース データを作成する
1.  Microsoft SQL Server Management Studio を開きます。
2.  次のクエリを実行し、データベースの作成 (DMFLEgacyDB)、テーブルの作成 (VendorEntity)、テーブルへのデータ入力を行います。

         USE [master] GO /****** Database [DMFLegacyDB] ******/ CREATE DATABASE [DMFLegacyDB]GOUSE [DMFLegacyDB]
        GO
         /****** Table [dbo].[VendorEntity] ******/
         CREATE TABLE [dbo].[VendorEntity]
        (
         [ACCOUNTNUM][nvarchar](20)default(N'') NOT NULL,
         [FIRSTNAME][nvarchar](25)default(N'') NOT NULL,
         [MIDDLENAME][nvarchar](25)default(N'') NOT NULL,
         [LASTNAME][nvarchar](25)default(N'') NOT NULL,
         [LANGUAGEID][nvarchar](7)NOT NULL,
         [VENDGROUP][nvarchar](20)NULL,
         [CURRENCY][nvarchar](10)NULL,
         [PartyType][nvarchar](10)NULL
         ) 
        ON [PRIMARY]
        GO
        INSERT [dbo].[VendorEntity] ([ACCOUNTNUM], [FIRSTNAME], [MIDDLENAME], [LANGUAGEID], [LASTNAME], [VENDGROUP], [CURRENCY], [PartyType])
         VALUES (N'V001', N'001 first', N'001 middle', N'en-us', N'001 last', N'10', N'USD', N'Person')
        INSERT [dbo].[VendorEntity] ([ACCOUNTNUM], [FIRSTNAME], [MIDDLENAME], [LANGUAGEID], [LASTNAME], [VENDGROUP], [CURRENCY], [PartyType])
         VALUES (N'V002', N'002 first', N'002 middle', N'en-us', N'002 last', N'20', N'USD', N'Person')

## <a name="create-an-odbc-data-source-to-connect-to-the-sql-server-database"></a>SQL Server データベースを作成して、ODBC データ ソース に接続する
1.  Microsoft Dynamics AX を実行しているコンピューターで、**管理ツール** &gt; **データ ソース (ODBC)** を開きます。
2.  SQL Server のユーザー DSN を作成し、名前を **DMFLegacyDB DSN** にして、データベースの作成に使用した SQL Server のインスタンスを選択します。
3.  **次へ**をクリックし、適切な値を選択して SQL Server インスタンスに接続します。 一般に、データのインポート/エクスポート フレームワーク サービスを実行しているアカウントと接続することをお勧めします。 詳細については、[データ ソースの管理](http://msdn.microsoft.com/en-us/library/windows/desktop/ms712362(v=vs.85).aspx) を参照してください。
4.  **次へ**をクリックし、既定のデータベースの **DMFLegacyDB** を選択し、**完了**をクリックします。

## <a name="define-the-format-of-your-source-data"></a>ソース データのフォーマットを形式する
1.  **データのインポート/エクスポート フレームワーク** &gt; **設定** &gt; **ソース データ形式**を開きます。
2.  **新規**をクリックし、名前と説明を入力します。次に、**タイプ** フィールドの **ODBC** を選択します。
3.  **一般**タブの、**DSN** タイプで、**ユーザー DSN** を選択し、**DSN 場所**の場合は、**クライアント**を選択し、**DMFLegacyDB-DSN** を選択します。 接続文字列が入力されます。
4.  **検証**をクリックして、ログオンしているアカウントが ODBC 接続にアクセスできることを確認します。

## <a name="define-a-processing-group"></a>処理グループの定義
1.  **データのインポート/エクスポート フレームワーク** &gt; **共通** &gt; **処理グループ**で、**新規**をクリックして新しい処理グループを作成します。
2.  グループの名前と説明を設定します。
3.  処理グループに含めるエンティティを選択するには、**エンティティ**をクリックします。
4.  **処理グループのエンティティの選択**フォームで、**新規**をクリックしてから、**エンティティ**に対して**仕入先**を選択します。
5.  **エンティティ**をクリックします。 **処理グループのエンティティの選択** ダイアログ ボックスが開きます。
6.  **クエリ** ボックスに次のクエリを入力します。

        select * from VendorEntity

7.  **ソース マッピングの生成**をクリックします。 オプション: マッピングを必要に応じて変更します。
8.  **検証**をクリックします。
9.  **ソース ファイルのプレビュー**をクリックし、**処理グループのエンティティの選択**フォームを閉じます。

## <a name="process-data-from-source-to-staging"></a>ソースからステージングにデータを処理
1.  **処理グループ** フォームで、作成した仕入先グループを選択して**ステージング データの取得**をクリックします。 **ステージング データ ジョブに対するジョブ ID の作成** ダイアログ ボックスが開きます。
2.  既定では、ジョブの ID が生成されます。 必要に応じて、IDを変更して説明を追加することができます。 **OK** をクリックします。
3.  **ステージング データ実行** フォームが開きます。
4.  **ソースからステージングにデータを取得**フォームで、**OK** をクリックしてすぐに実行します。 ソース データはステージング テーブルにコピーされます。

## <a name="validate-the-data-in-staging"></a>ステージングのデータの検証
1.  **データのインポート/エクスポート フレームワーク** &gt; **共通** &gt; **処理グループ**で、**実行履歴**をクリックして実行したジョブを選択します。
2.  **ステージング データの表示**をクリックします。
3.  ODBC ソースと一致することを検証するステージング データを確認します。
4.  **すべて検証**をクリックして、関連するすべての参照データが正しくシステムに存在することを確認します。

## <a name="process-data-from-staging-to-target"></a>ステージングからターゲットにデータを処理
1.  **データのインポート/エクスポート フレームワーク** &gt; **共通** &gt; **処理グループ**で、操作する処理グループを選択します。
2.  **データをターゲットにコピー**をクリックします。 **実行するジョブ ID を選択** ダイアログ ボックスが開きます。
3.  ジョブを選択し、**OK** をクリックします。 **ターゲット データ実行** ダイアログ ボックスが開きます。
4.  **実行**をクリックし、**OK** をクリックします。 データはターゲット エンティティにコピーされます。

## <a name="validate-the-data-in-target"></a>ターゲットのデータの検証
ODBC ソースからの顧客仕入先データが次のいずれかの方法で表示されることを確認します。

-   ステージング データの表示:
    1.  **データのインポート/エクスポート フレームワーク** &gt; **共通** &gt; **処理グループ**、**実行履歴**、**ステージング データの表示**とクリックしてから実行したジョブを選択します。
    2.  ODBC ソースと一致することを検証するステージング データを確認します。
    3.  **すべて検証**をクリックして、関連するすべての参照データが正しくシステムに存在することを確認します。
-   ODBC ソースからの顧客データが **買掛金勘定** &gt; **共通** &gt; **仕入先** &gt; **すべての仕入先** フォームに表示されるようになったことを確認します。





