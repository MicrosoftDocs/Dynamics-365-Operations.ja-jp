---
title: 顧客の基本設定データをチャネル データベースに追加
description: このチュートリアルでは、RetailCustPreferences テーブルを小売チャネルのコマース ランタイム (CRT) に追加する方法と、新しいテーブルのデータをチャネル データベースに移動するサブジョブを作成する方法を示します。
author: kfend
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 18081
ms.assetid: 3c13fe1d-2078-4539-b865-e266b6f56e60
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 71556dde632b06f51534b528000be037022fc693
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004606"
---
# <a name="add-customer-preference-data-to-channel-databases"></a>顧客の基本設定データをチャネル データベースに追加

[!include [banner](../includes/banner.md)]

> [!NOTE]
> このトピックは、Dynamics 365 for Finance and Operations バージョン 7.1 およびそれ以前のバージョンに適用されます。 バージョン 7.2 およびそれ以上の場合は、この実装はサポートされていません。 これらのバージョンでは、オーバーレイせずに拡張モデルに従います。

このチュートリアルでは、RetailCustPreferences テーブルを小売チャネルのコマース ランタイム (CRT) に追加する方法と、新しいテーブルのデータをチャネル データベースに移動するサブジョブを作成する方法を示します。

<a name="add-the-retailcustpreferences-table-in-the-data-distribution-to-the-crt-for-the-retail-channel"></a>小売チャネルの CRT へのデータ配布での RetailCustPreferences テーブルの追加
----------------------------------------------------------------------------------------------

チャネル スキーマは、チャネル データベースに送信されるデータの XML 記述です。

1.  **小売** &gt; **本社の設定** &gt; **小売用スケジューラ** &gt; **小売チャネル スキーマ**の順にクリックします。
2.  チャネルに対応するスキーマ名を選択します。 その後、**チャネル テーブル** をクリックします。
3.  **新規**をクリックし、**テーブル名**フィールドに、新しいテーブルの名前として **ax.RetailCustPreference** を入力します。
4.  **チャネル テーブル フィールド**タブで、**新規**をクリックし、フィールド名 **ACCOUNTNUM**、**EMAILOPTIN**、および **RECID** を入力します。
5.  **チャネル テーブル** ページを閉じます。

## <a name="create-a-subjob"></a>サブジョブの作成
次に、チャネル データベースに新しいテーブルのデータを移動するために、CustTable ジョブのサブジョブを作成します。

1. Retail Headquarters で **小売** &gt; **本社の設定** &gt; **小売用スケジューラ** &gt; **スケジューラ サブジョブ** とクリックして、そして **新規** をクリックします。
2. **サブジョブ番号**および**説明**フィールドに **RetailCustPreference** を入力します。
3. **小売チャネル スキーマ** フィールドで、**Dynamics 365 Retail** を選択します。
4. **チャネル テーブル名**フィールドで、**ax.RetailCustPreference** を選択します。
5. **テーブル名**フィールドで、**RetailCustPreference** を選択します。
6. **チャネル フィールド マッピング**タブで、**フィールドの照合**をクリックします。 **開始** フィールドと **終了** フィールドの列に入力されます。 **上記の手順で UI を使用する代わりに、代替方法として、コードで実行することもできます。**
   1.  Microsoft Visual Studio を起動してから、アプリケーション オブジェクト ツリー (AOT) で **RetailCDXSeedData\_AX7** クラスを見つけます。
   2.  次のメソッドを追加します。

           private void C_RetailCustPreference()
           {
               jobIDContainer = ['1010'];
               subjobID = 'RetailCustPreference';
               axTableName = tableStr(RetailCustPreference);
               axFieldNames = [
               fieldStr(RetailCustPreference, AccountNum),
               fieldStr(RetailCustPreference, EmailOptIn),
               fieldStr(RetailCustPreference, RecId)
               ];
           }

   3.  クラスをコンパイルします。
   4.  インターネット インフォメーション サービス (IIS) をリセットします。
   5.  クライアントに切り替えます。
   6.  **小売** &gt; **本社の設定** &gt; **小売用スケジューラ** &gt; **小売用スケジューラの初期化**の順にクリックします。 必要なスケジューラ サブジョブ定義が生成され、サブジョブがスケジューラ ジョブに追加されます。

7. **小売** &gt; **本社の設定** &gt; **小売用スケジューラ** &gt; **小売チャネル スキーマ**の順にクリックします。
8. **小売チャンネル スキーマ** ページの、左側のナビゲーション ウィンドウで、**Dynamics 365 Retail** をクリックします。
9. **小売データの配布**タブで、**エクスポート**をクリックします。
10. 使用しているブラウザーに応じて、次のいずれかのステップを実行します。
    -   Google Chrome を使用している場合は、XML ファイルをダウンロードするように求められる必要があります。 ファイルをパスに保存します。
    -   Internet Explorer を使用している場合は、web ページが開きます。 ページ内を右クリックし、**ソースの表示** をクリックします。 次に、ページ ソースのコンテンツをファイル パスに保存します。

11. Notepad++ などテキスト エディターで、保存した XML ファイルを開き、これらの手順に従います。
    1.  次の行を検索します: **&lt;Table name=“RetailCustTable”&gt;**。 29 行目前後と 744 行目前後に 2 つのインスタンスがあります。
    2.  両方の **&lt;Table name=“RetailCustTable”&gt;** コード ブロックの最後の行の後に次のコードを追加します。 コードを **&lt;/Table&gt;** タグの後に追加します。

            <Table name="RetailCustPreference">
                <LinkGroup>
                    <Link type="FieldMatch" fieldName="accountNum" parentFieldName="AccountNum" />
                </LinkGroup>
            </Table>

12. ファイルの編集が終了した後、クライアントおよび **Retail チャンネル スキーマ** ページ‎に戻ります。 左のナビゲーション ウィンドウで、**Dynamics 365 Retail** をクリックします。
13. **小売データの配布**タブで、**インポート**をクリックします。
14. 表示されるダイアログ ボックスで、**参照**をクリックし、編集した XML ファイルを選択してから、**OK** をクリックしてファイルをインポートします。
15. **小売チャネル スキーマ** ページを閉じます。
16. **小売** &gt; **本社の設定** &gt; **小売用スケジューラ** &gt; **スケジューラ ジョブ**の順にクリックします。
17. **スケジューラ ジョブ**ページで、**1010** をクリックし、「顧客」ジョブを選択します。
18. **サブジョブ**タブで、**新規**をクリックし、**RetailCustPreference** をサブジョブ番号として入力します。 **保存** をクリックします。
19. <strong>小売チャネル スキーマ</strong> ページで、スキーマ名として **Dynamics 365 Retail** を選択してから、**クエリの生成** をクリックします。
