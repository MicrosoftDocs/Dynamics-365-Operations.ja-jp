---
title: 初期同期に関する考慮事項
description: このトピックでは、制約、既知の問題、およびデュアル書き込みの初期同期に関するガイダンスについて説明します。
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: ramasri
ms.search.validFrom: 2020-10-12
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3377514fe9e5b67dbec191bd404fb479f0a7759d
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062300"
---
# <a name="considerations-for-initial-synchronization"></a>初期同期に関する考慮事項

[!include [banner](../../includes/banner.md)]



テーブルで二重書き込みを開始する前に、最初の同期を実行して、財務と運用アプリと Customer Engagement アプリの両面で既存のデータを処理することができます。 2 つの環境間でデータを同期する必要がない場合は、初期同期を省略できます。

初期同期では、既存のデータを 1 つのアプリから別のアプリに双方向でコピーできます。また、実行する際には、いくつかの考慮事項があります。 たとえば、Go-Live 前にデータ移行が必要な場合があります。 この場合、データはデータ移行によって一方の側に読み込まれ、初期同期によってもう一方の側に同期されます。

初期同期には、次の方法を使用することをお勧めします。

+ **[単一スレッド テーブル](#single-threaded-entities):** まずデータを財務と運用アプリに移行し、次に初期同期をトリガーしてデータを Dataverse に移動します。 Microsoft が実行したラボ テストによると、このシーケンスは、Dataverse から財務と運用アプリへの同期よりもパフォーマンスが高いです。
+ **複数スレッド テーブル**: まずデータを Dataverse に移行し、次に初期同期をトリガーしてデータを財務と運用アプリに移動します。

## <a name="constraints"></a>制約

### <a name="data-migration-slow-down-with-enabled-dual-write"></a>二重書き込みの有効化によるデータ移行速度の低下

最初にデュアル書き込みでマップを有効にしてからデータのインポートを開始すると、移行のパフォーマンスが低下します。 データの移行が完了するまでは、実行中のマップをデュアル書き込みで有効にしないことをお勧めします。

### <a name="limit-of-500000-rows-per-run"></a>実行ごとに 500,000 の行制限

初期同期によって許可される行の最大数は、1 回の実行ごとに 500,000 です。 各リーガル テーブルが個別に実行するため、各リーガル テーブルに 500,000 の行制限が適用されます。 詳細については、[Dataverse へデータを統合](/power-platform/admin/data-integrator) を参照してください。 特に、「パフォーマンスを最適化し、アプリケーションに過負荷をかけないために、現在プロジェクトの実行数を 500K 行に制限しています」という通知に注意してください。

初期同期時に、1 回の実行に 500,000 行以上の行が存在する場合は、データを財務と運用アプリと Dataverse に個別に移行し、初期同期をスキップすることをお勧めします。

### <a name="twenty-four-hour-limit"></a>24 時間制限

Dataverse から財務と運用アプリへの初期同期を実行している場合、24 時間以内にインポートの結果を財務と運用アプリから受け取る必要があります。 そうしない場合、タイムアウトが発生します。 したがって、大量のデータを同期していて、1 回の実行に 24 時間以上かかる場合、タイムアウトが原因で初期同期が失敗する可能性があります。たとえば、**顧客/アカウント** テーブルの Dataverse から財務と運用アプリへの初期同期には、70,000 行が含まれます。 したがって、実行には 24 時間以上の時間がかかる場合があります。

データ量が 70,000 行を超える場合は、[単一スレッド テーブル](#single-threaded-entities)に対して Dataverse から財務と運用アプリへの初期同期を実行しないでください。 これらのテーブルは、インポート時にマルチスレッドをサポートしていないので、ボリュームが 70,000 行を超えると、タイムアウトが発生する可能性があります。 この場合、データを財務と運用アプリと Dataverse に別々に移行し、初期同期をスキップする必要があります。

### <a name="limit-of-40-legal-entities-while-the-environments-are-being-linked"></a>環境がリンクされている場合の 40 の法人制限

現在、環境がリンクされている場合には法人は 40 までという制限があります。 40 を超える法人が環境間でリンクされているマップを有効にしようとすると、次のエラー メッセージが表示されます。

```console
Dual-write failure - Plugin registration failed: [(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-XXXXX. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea- XXXXX)], One or more errors occurred.
```

### <a name="initial-synchronization-isnt-currently-supported-for-table-maps-that-have-10-or-more-lookups"></a>現在、初期同期は 10 以上のルックアップを含むテーブル マップではサポートされていません

この制限は、ルックアップが 10 以上あるテーブル マップの Dataverse からの初期同期にのみ適用されます。 10 以上のルックアップを含むテーブル マップに対して初期同期を実行すると、次のエラー メッセージが表示される場合があります。

```console
5 Attempts to get data from https://XXXX.azure-apim.net/apim... Failed
```

回避策として、初期同期を次の手順に分けることができます。

1. 二重書き込みテーブル マップから必須ではないルックアップ列をいくつか削除し、ルックアップの数を 10 にします。 
2. ルックアップ列が削除されたら、マップを保存し、初期同期を行います。 
3. 最初の手順の初期同期が正常に完了したら、残りのルックアップ列を追加し、最初の手順で同期されたルックアップ列を削除します。 ルックアップ列の数が 10 であることを再度確認します。 マップを保存し、初期同期を実行します。これらの手順を繰り返して、すべてのルックアップ列が同期されていることを確認します。 
4. すべてのルックアップ列をマップに戻し、マップを保存して、初期同期をスキップしてマップを実行します。これにより、マップでライブ同期モードが有効になります。

### <a name="five-minute-limit-for-finance-and-operations-data-export"></a>Finance and Operations のデータ エクスポートに対する 5 分の制限

財務と運用アプリから Dataverse への初期同期を実行し、Finance and Operations のデータのエクスポートに 5 分以上かかる場合、初期同期がタイムアウトすることがあります。タイムアウトは、データ テーブルに `postLoad` メソッドの仮想列がある場合、またはエクスポート クエリが最適化されていない (たとえば、インデックスが存在しない) 場合に発生する可能性があります。

このタイプの同期は、Platform update 37 (PU37) 以降でサポートされます。 したがって、財務と運用アプリを PU37 またはそれ以降のバージョンに更新する必要があります。

### <a name="security-role-for-write-access"></a>書き込みアクセス用のセキュリティ ロール

二重書き込みを使用する Customer Engagement 組織のすべてのユーザーは、**二重書き込みランタイム ユーザー** ロールに追加する必要があります。 このロールがない場合、ユーザーは、Customer Engagement 組織のテーブルに行を作成することはできません。

### <a name="company-and-currency-exchange-tables-required-security-role"></a>会社および通貨為替テーブルに必要なセキュリティ ロール

会社と通貨為替テーブルは本質的にグローバルであり、すべての二重書き込みユーザーにはこれら 2 つのテーブルへの読み取りアクセスが必要です。 アクセスを提供するため、すべての二重書き込みユーザーを、**二重書き込みアプリ ユーザー** セキュリティ ロールに追加する必要があります。 ユーザーにこのセキュリティ ロールが割り当てられていない場合、会社と通貨の値を含むテーブルを読み取ることができません。

### <a name="error-handling-capabilities"></a>エラー処理機能

#### <a name="initial-synchronization-is-always-a-full-push"></a>初期同期は常にフル プッシュ

個別の行の同期が失敗した場合は、その個別の行だけを再同期することはできません。 初期同期では、常にデータ セット全体がプッシュされます。 この動作は、*フル プッシュ* と呼ばれます。 初期同期が部分的にしか成功しなかった場合、初期同期に失敗した行だけでなく、すべての行に対して 2 回目の同期が実行されます。

#### <a name="only-the-top-five-errors-can-be-viewed"></a>上位 5 つのエラーのみ表示可能

初期同期のエラー ログに記録された上位 5 つのエラーのみを表示できます。

## <a name="known-issues"></a>既知の問題

既知の問題の詳細については、[初期同期中の問題のトラブルシューティング](dual-write-troubleshooting-initial-sync.md)を参照してください。

## <a name="guidance-matrix"></a>ガイダンス マトリックス

<table>
<thead>
<tr>
<th>財務と運用アプリ インスタンス</th>
<th>Dataverse インスタンス</th>
<th>初期同期を実行するデータの有無</th>
<th>説明</th>
<th>テーブルの最大ボリューム</th>
<th>単一スレッドまたはマルチスレッド</th>
<th>アプローチ</th>
</tr>
</thead>
<tbody>
<tr>
<td>新規</td>
<td>新規</td>
<td>番号</td>
<td>財務と運用アプリ インスタンスと新しい Customer Engagement アプリ インスタンス。どちらのアプリにも初期データがない場合</td>
<td>適用できません</td>
<td>任意</td>
<td>
<ul>
<li>二重書き込みを有効にし、初期同期をスキップします。</li>
</ul>
</td>
</tr>
<tr>
<td rowspan='3'>新規</td>
<td rowspan='3'>新規</td>
<td rowspan='3'>あり</td>
<td rowspan='3'>財務と運用アプリ インスタンスと新しい Customer Engagement アプリ インスタンス。どちらかのアプリに移行されたデータがある場合</td>
<td>&lt;500,000</td>
<td><a href='#single-threaded-entities'>単一スレッド</a></td>
<td>
<ol>
<li>財務と運用アプリへのデータ移行</li>
<li>初期同期を実行します。</li>
</ol>
</td>
</tr>
<tr>
<td>&lt;500,000</td>
<td>マルチスレッド</td>
<td>
<ol>
<li>Dataverse にデータを移行します。</li>
<li>初期同期を実行します。</li>
</ol>
</td>
</tr>
<tr>
<td>&gt;500,000</td>
<td>任意</td>
<td>
<ol>
<li>初期同期の範囲外で、各アプリにデータを移行します。</li>
<li>二重書き込みを有効にし、初期同期をスキップします。</li>
</ol>
</td>
</tr>
<tr>
<td rowspan='4'>新規</td>
<td rowspan='4'>既存</td>
<td rowspan='4'>あり</td>
<td rowspan='4'>新しい財務と運用アプリ インスタンスと既存の Customer Engagement アプリ インスタンス</td>
<td>&lt;70,000</td>
<td><a href='#single-threaded-entities'>単一スレッド</a></td>
<td>
<ol>
<li>財務と運用アプリで新しい会社を作成します。</li>
<li>会社コードのブートストラップ Dataverse。</li
><li>初期同期を実行します。</li>
</ol>
</td>
</tr>
<tr>
<td>&gt;70,000</td>
<td><a href='#single-threaded-entities'>単一スレッド</a></td>
<td>
<ol>
<li>財務と運用アプリで新しい会社を作成します。</li>
<li>会社コードのブートストラップ Dataverse。</li>
<li>初期同期の範囲外で、各アプリにデータを移行します。</li>
<li>二重書き込みを有効にし、初期同期をスキップします。</li>
</ol>
</td>
</tr>
<tr>
<td>&lt;500,000</td>
<td>マルチスレッド</td>
<td>
<ol>
<li>財務と運用アプリで新しい会社を作成します。</li>
<li>会社コードのブートストラップ Dataverse。</li>
<li>初期同期を実行します。</li>
</ol>
</td>
</tr>
<tr>
<td>&gt;500,000</td>
<td>任意</td>
<td>
<ol>
<li>財務と運用アプリで新しい会社を作成します。</li>
<li>会社コードのブートストラップ Dataverse。</li>
<li>初期同期の範囲外で、各アプリにデータを移行します。</li>
<li>二重書き込みを有効にし、初期同期をスキップします。</li>
</ol>
</td>
</tr>
<tr>
<td rowspan='2'>既存</td>
<td rowspan='2'>新規</td>
<td rowspan='2'>あり</td>
<td rowspan='2'>既存の財務と運用アプリ インスタンスと新しい Customer Engagement アプリ インスタンス</td>
<td>&lt;500,000</td>
<td>任意</td>
<td>
<ul>
<li>初期同期を実行します。</li>
</ul>
</td>
</tr>
<tr>
<td>&gt;500,000</td>
<td>任意</td>
<td>
<ol>
<li>各アプリにデータを移行します。</li>
<li>二重書き込みを有効にし、初期同期をスキップします。</li>
</ol>
</td>
</tr>
<tr>
<td rowspan='4'>既存</td>
<td rowspan='4'>既存</td>
<td rowspan='4'>あり</td>
<td rowspan='4'>既存の財務と運用アプリ インスタンスと既存の Customer Engagement アプリ インスタンス</td>
<td>&lt;70,000</td>
<td><a href='#single-threaded-entities'>単一スレッド</a></td>
<td>
<ol>
<li>会社コードのブートストラップ Dataverse。</li>
<li>初期同期を実行します。</li>
</ol>
</td>
</tr>
<tr>
<td>&gt;70,000</td>
<td><a href='#single-threaded-entities'>単一スレッド</a></td>
<td>
<ol>
<li>会社コードのブートストラップ Dataverse。</li>
<li>初期同期の範囲外で、各アプリにデータを移行します。</li>
<li>二重書き込みを有効にし、初期同期をスキップします。</li>
</ol>
</td>
</tr>
<tr>
<td>&lt;500,000</td>
<td>マルチスレッド</td>
<td>
<ol>
<li>会社コードのブートストラップ Dataverse。</li>
<li>初期同期を実行します。</li>
</ol>
</td>
</tr>
<tr>
<td>&gt;500,000</td>
<td>任意</td>
<td>
<ol>
<li>会社コードのブートストラップ Dataverse。</li>
<li>初期同期の範囲外で、各アプリにデータを移行します。</li>
<li>二重書き込みを有効にし、初期同期をスキップします。</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="single-threaded-tables"></a><a id="single-threaded-entities"></a>単一スレッド テーブル

- 消費税コード (msdyn\_taxcodes)
- 顧客 V3 (アカウント)
- 仕入先 V2 (msdyn\_vendors)
- 倉庫 (msdyn\_warehouses)
- 製品カテゴリ (msdyn\_productcategories)
- 雇用 (cdm\_employments)
- 職位作業者割り当て (cdm\_positionworkerassignmentmaps)
- 倉庫の場所 (msdyn\_inventorylocations)
- 配送モード (msdyn\_shipvias)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
