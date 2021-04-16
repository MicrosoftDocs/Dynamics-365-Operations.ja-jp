---
title: 電子申告 (ER) における会社間データ ソース
description: このトピックでは、電子申告 (ER) で会社間のデータ ソースを使用する方法について説明します。
author: NickSelin
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, ERFormatMappingLegalEntityFilterTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 7528a84bae388dd8b159405043570b647d6e2cb4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753747"
---
# <a name="cross-company-data-sources-in-electronic-reporting-er"></a>電子申告 (ER) における会社間データ ソース

[!include[banner](../includes/banner.md)]

さまざまな形式で送信ドキュメントを生成するため、電子申告 (ER) 形式をデザインできます。 ドキュメントを生成する際、ER 形式は、対応する ER モデル マッピングでコンフィギュレーションされたデータ ソースを呼び出します。 レコード取得用にアプリケーション テーブルへのアクセスをコンフィギュレーションするため、**テーブル レコード** タイプの ER データ ソースを使用できます。 アクセスするテーブルが共有テーブル (つまり、会社 ID なしでデータが保存されているテーブル) である場合、このデータ ソースは、すべてのレコードを返します。 アクセスするテーブルが会社固有のテーブル (つまり、会社ごとのデータが保存されるテーブル) である場合、このデータ ソースは現在の会社 (つまり、ER 形式が実行されている会社コンテキスト) に対して保存されたレコードのみを返します。

モデル マッピングでの **テーブル レコード** タイプのデータ ソースは、会社間データ ソースとしてマークされます。 したがって、アプリケーション テーブルで会社間データにアクセスするため、**テーブル レコード** タイプの ER データ ソースを使用できます。

会社間としてデータ ソースをマークする場合、次の動作が発生します。

- CompanyInfo を除く任意の共有テーブルを参照するデータ ソースについては、データ ソースは参照テーブル内に存在するすべてのレコードを返します。 
- CompanyInfo テーブルを参照するデータ ソースについては、CompanyInfo が共有テーブルであっても、データ ソースは定義されるスコープから会社の ID を含むレコードを返します。
- 任意の会社固有テーブルについては、データ ソースは定義されるスコープから会社の ID を含む参照テーブルのレコードを返します。

システム クエリ ダイアログ ボックスで、会社間としてマークされる任意のデータ ソースで **クエリの要求** オプションが有効とされる場合、**会社範囲** タブで 1 つ以上の会社を含むよう手動で選択できます。

> [!IMPORTANT]
> 他のフィルターと同様に、ER 形式の実行時にクエリの最後の使用値として会社フィルターが保持されます。 データ ソースの会社間の値を変更すると、フィルターは自動的に変更されません。 別のデータ ソースに対して会社間の異なる値を使用するには、対応するユーザー固有の選択項目を削除します。

会社間としてマークされているデータ ソースごとに、ER 式で **FILTER** および **WHERE** 関数を使用してレコードを選択できます。 **dataAreaID** フィールドは会社 ID としても使用できます。 現在、**dataAreaID** フィールドは **FILTER** 関数が使用される際の次の条件のタイプに制限されます。

- 単一の **dataAreaID** フィールドの比較を持つ条件のみがサポートされます。
- レコードの一覧項目に依存しない式を持つ比較のみが使用できます。

したがって、次の式は有効です。

```ER Expression
FILTER (MyTable, MyTable.dataAreaID = $StringUserInputParameter)
While shown below expressions will not pass the validation:
FILTER (MyTable, MyTable.dataAreaID = MyTable2RecordsList.MyField)
FILTER (MyTable, 
    OR(
        MyTable.dataAreaID = $StringUserInputParameter1,
        MyTable.dataAreaID = $StringUserInputParameter2
    )
)
```

既定では、現在のアプリケーションのすべての会社がスコープに含まれます。 ただし、それは制限できます。 単一の ER 形式の会社間のデータ アクセスのスコープを制限するには、形式に特定の組織階層を割り当てます。 ER 形式用に階層が定義されると、形式が会社間データ ソースを呼び出す場合でも、割り当てられた階層に表示される法人のレコードのみが返されます。 既に存在しない階層への参照が ER 形式に対して定義されると、既定のスコープが適用され、形式は会社間のデータ ソースを呼び出します。 この場合、すべてのアプリケーション会社のレコードが返されます。

**ドラフトを使用** オプションが単一の ER 形式組織階層への割り当てに対して有効となっている場合、この階層のドラフト バージョンからの法人は、会社間のデータ ソースのスコープを識別するために使用されることに注意してください。 ドラフト バージョンが存在しない場合、この組織階層の最後に発行されたバージョンからの法人がこれに対して使用されます。

**ドラフトを使用** オプションが単一の ER 形式組織階層への割り当てに対して有効となっていない場合、この階層の最後に発行されたバージョンからの法人は、会社間のデータ ソースのスコープを識別するために使用されることに注意してください。 組織階層の日付の有効性は、ER フレームワークでまだサポートされていません。

階層は、ER ワークスペースからまたは **O組織管理 \> 電子申告 \> 形式の法人フィルター** メニュー項目を使用してアクセスできる特定のページでの形式に割り当てられます。 ページにアクセスするには、**形式の法人フィルターを管理** 権限 (ERMaintainFormatMappingLegalEntityFilters) がユーザーに付与される必要があります。 ユーザーが手動でシステム クエリ ダイアログ ボックスで指定できる制限に加えて、形式に対する階層ベース法人のスコープ制限が適用されます。 これらの制限の交差部分は、形式の実行時に使用されます。

この機能の詳細については、7.5.4.3 IT サービス/ソリューション コンポーネントの取得/開発 (10677) 業務プロセスの一部であるタスクガイド、**会社間モードで会社固有テーブルの ER アクセス レコード** を再生し、[Microsoft ダウンロード センター](https://go.microsoft.com/fwlink/?linkid=874684) からダウンロードできます。 このタスク ガイドでは、会社間モードでアプリケーション テーブルにアクセスする ER モデル マッピングおよび ER 形式のコンフィギュレーションのプロセスについて説明します。

タスクガイドを完成させるには、次のファイルをダウンロードしてください。

- [ER モデル コンフィギュレーション - CrossCompanyDataAccessModel.xml](https://go.microsoft.com/fwlink/?linkid=874111)
- [ER 形式コンフィギュレーション - CrossCompanyDataAccessFormat.xml](https://go.microsoft.com/fwlink/?linkid=874111)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]