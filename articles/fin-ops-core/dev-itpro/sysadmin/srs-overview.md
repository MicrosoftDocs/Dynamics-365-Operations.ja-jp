---
title: 会社間データ共有の概要
description: この記事では、会社間でのデータ共有の概要について説明します。 これは、展開において、参照およびグループ データを会社間で共有するためのメカニズムです。
author: RamaKrishnamoorthy
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: ramasri
ms.search.validFrom: 2022-01-27
ms.dyn365.ops.version: Platform update 1
ms.custom: 89071
ms.assetid: 0bbe7453-624f-4551-a1d0-842484067311
ms.search.form: SysDataSharingConfiguration
ms.openlocfilehash: 46db32e4104963a89dbdf9b7b1cdde29e7346663
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702083"
---
# <a name="cross-company-data-sharing-overview"></a>会社間データ共有の概要

[!include [banner](../includes/banner.md)]

会社間データ共有の概念により、財務と運用の展開内で、会社固有のマスター、参照、および設定データを会社間で共有できます。 

2 つのデータ共有概念を使用できます。 
+ 重複レコード共有 (DRS) は、ポリシー内の任意の会社のレコードの作成、更新、または削除が、ポリシー内のすべての会社間でコピー/複製されるという概念です。 ポリシーで共有するように選択されている場合は、フィールドの更新も複製されます。 DRS は、利用可能になった最初の共有タイプでした。 
+ マスター会社共有は、単一レコード共有 (SRS) とも呼ばれ、マスター会社に属する単一の物理レコードが子会社間で仮想的に共有される概念です。 ポリシー内の任意の会社で作成、更新、または削除すると、すべての会社で使用される単一のレコードが更新されます。 マスター会社共有は現在プレビューにあります。


## <a name="why-should-you-consider-cross-company-data-sharing"></a>なぜ会社間データ共有を検討する必要があるのですか?
配置環境において複数の会社間で一貫したデータが必要な場合は、会社間データ共有を検討する必要があります。 配置環境には数百社以上の会社が存在する可能性があり、ビジネスでは、これらの会社はいつでも重要なデータについて確実な単一バージョンに依存することができます。

会社間データ共有の業務シナリオの例を次に示します。
+   すべての顧客は常にサービスを利用でき、すべての会社間で同じ条件を持っている必要があります。
+   支払条件と配送条件は、地域ごとにすべての会社間で常に調整する必要があります。 
+   現金および銀行管理パラメーターのコンフィギュレーションは、すべての会社で一貫した処理を確保するために揃える必要があります。

ロールとセキュリティ コンフィギュレーションを使用すると、選択した会社で選択したユーザーにのみアクセス許可を提供することで、共有テーブルを集中管理できます。

## <a name="data-sharing-policies"></a>データ共有ポリシー
データ共有は、データ共有ポリシーのコンフィギュレーションに基づいています。 ポリシーでは、データ共有の次の側面を制御できます。
+   データ共有概念。
+   共有されるテーブル。
+   共有されるフィールド。
+   共有に参加している会社。

![単一レコード共有の例。](media/SRS-image1.png)

同じ会社とテーブルは、1 つの有効なポリシーにのみ含めることができます。 同じテーブルを複数のポリシーで共有することもできます。 これは、DRS のレコードまたは会社の制限に達した場合、または国/地域ごとに異なる方法で共有する必要があるテーブルのポリシーを作成する場合に必要になる可能性があります。


## <a name="when-to-consider-duplicate-record-versus-master-company-sharing-preview"></a>重複レコードとマスター会社の共有 (プレビュー) をいつ検討するべきですか?
重複レコードの共有にはいくつかの利点があり、可能な限り常にこのオプションを選択する必要があります。 一度マスター会社の共有を有効にすると、その後範囲を縮小したり共有を停止したりすることができないため、慎重に考慮してください。

マスター会社の共有は、共有する必要がある場合にのみ考慮する必要があります。
- 同じポリシーで 300 社を超える会社
    - ポリシーでは、テーブルのトランザクション数は 200 万レコードを超えます。 
    - 制限は、会社ごとのレコード数 x ポリシー内の会社数として計算されます。
    -   テーブルは、マスター会社の共有でサポートされています。

|  注意事項  | レコード共有の重複 | マスター会社の共有 |
|----|-----|-----|
| ポリシーを有効化/更新した後に、テーブル、フィールド、または会社を削除できますか? | 有効   | 無効   |
| ポリシーを無効にできますか? |  有効  |  無効  |
| ポリシーを有効にした後に、テーブル、フィールド、または会社を追加できますか? | 有効   | 有効  |
| 必須の外部キー関係を共有対象から除外/選択解除できますか? | 無効   | 無効   |
| 必須ではない外部キー フィールドの共有を手動で管理できますか? | 有効   | 無効   |
| 共有対象として選択されていないフィールドは、各会社で引き続き維持できますか? | 有効   | 無効   |
| ポリシー内の最大会社数 |  300  | 無制限   |
| テーブルおよびポリシーごとの最大レコード数 | 200 万    |  無制限  |
| 一意のインデックスのないテーブルを共有できますか? |  無効  |  有効  |
| どのようなテーブル データ共有タイプがサポートされていますか? | 複写   | 重複および単一   |
| 共有を有効にする前に、会社はテーブルに既存のレコードを含めることができますか? | 有効   | マスター会社のみ   |
| ポリシーを有効化または更新した後で、コピー データを選択し、共有に関する問題を検証する必要がありますか? |  有効  |  無効  |
| 正式にサポートされているテーブルの一覧 |  [サポートされているテーブル](/dynamics365/fin-ops-core/dev-itpro/sysadmin/drs-srs-tables)  | [サポートされているテーブル](/dynamics365/fin-ops-core/dev-itpro/sysadmin/drs-srs-tables#tables-supported-for-master-company-data-sharing)   |
| Microsoft が提供するポリシー テンプレートは利用できますか?  |  有効  |  無効  |

異なるポリシーを使用することにより、同じ会社のセットに対して重複レコード共有とマスター会社の共有を組み合わせることができます。 重複レコード ポリシーで該当するすべてのテーブルとオプションの外部キーフィールドを常に選択し、マスター会社の共有ポリシーを有効にする前にポリシーを有効にすることが重要です。 

たとえば、次のことを共有できます。 
 - 重複レコード共有を使用した顧客グループと支払条件テーブル 
 - マスター会社の共有を使用した顧客テーブル。 これは、顧客レコード数が制限を超える場合と、ポリシーに対して会社数が 300 を超えない場合に使用できます。

## <a name="specific-considerations-for-successful-data-sharing"></a>データ共有を成功させるための考慮事項
### <a name="automatically-added-tables-based-on-selected-foreign-key-fields"></a>選択した外部キー フィールドに基づいて自動的に追加されるテーブル 
外部キー フィールドは、自動または手動で選択します。 参照テーブルが追加されていない場合は、ポリシーを有効化または更新すると、参照されるテーブルが自動的に追加されます。 

次の画像に示す例では、支払条件テーブルを手動で追加しない限り、PaymTermId 外部キー フィールドが顧客グループ テーブルで共有用に選択されているため、自動的に追加されます。 

![単一レコード共有。](media/SRS-image2.png)

> [!NOTE]
> 子の外部キー リレーションシップの 1 つのレベルのみが自動的に追加されます。 

ポリシーが有効化または更新された場合に自動的に追加されるテーブルは、ポリシーが無効になる前は、会社間データ共有の構成フォームに表示されません。 ベスト プラクティスは、ポリシーを有効化または更新する前に、選択した外部キー フィールドに基づいてテーブルを手動で追加することです。 これにより、共有するテーブルとフィールドへの理解を深めることができます。 このようにして、テーブルのフィールドを選択する DRS ポリシーのオプションも提供され、他のテーブルを追加する可能性のあるオプションの外部キー フィールドが含まれます。 

### <a name="countryregion-specific-considerations-for-successful-data-sharing"></a>データ共有を成功させるための国/地域固有の考慮事項
国/地域固有のフィールドやロジックを含むテーブルについては、慎重に検討する必要があります。 コンフィギュレーションの競合を回避するために、特定のテーブルに対して国/地域ごとに共有ポリシーを使用する必要がある場合があります。 国/地域固有のフィールドは、その国/地域の会社に対してのみ実行可能/編集可能ですが、これらのフィールドの更新によって他の国の地域の会社との競合が発生する場合があります。 

### <a name="additional-considerations"></a>その他の考慮事項
+   複合テーブルは、同じポリシーで共有する必要があります。 そうでない場合は、これを保護するために、有効化および更新中にテーブルを追加するようユーザーに通知するメッセージが表示されます。  
+   番号シーケンスを使用するテーブルの場合、番号順序タイプは、それらのエンティティの共有ポリシーにおいて、すべての会社で同じである必要があります。
    +   有効化および更新の際に番号順序を調整することもできます。 

## <a name="limitations"></a>制限
+   財務分析コードを参照する外部キー フィールド (たとえば、元帳または既定の分析コード) は、共有することはできません。 分析コードには、背景の分析コード データに対する緩い外部キー参照が保持されます。これは、会社固有のデータと非会社固有のデータの両方を参照できます。 各分析コード値に適用される適切なアクションを決定することは本質的に複雑であり、現在の実装からの変更が必要です。これは、パフォーマンスに大幅な影響を与える可能性があります。
+   共有は、二重書き込みと共に使用することはできません。
+   共有レコードの削除は、まだ完全にサポートされていないので、使用しないでください。 共有レコードを削除すると、トランザクションの参照 (ルックアップ/参照フィールド) が空白になります。 現在、固有レコード キーの名前を変更する名前変更アクションについても同様です。

## <a name="duplicate-record-sharing"></a>レコード共有の重複 
DRS の共有ロジックは、レコードの固有キー (顧客のアカウントや支払条件の名前など) に基づいています。 したがって、DRS ポリシーの一部となるには、テーブルに一意のインデックスが必要です。 ポリシーを有効化または更新した後で、初期同期を処理するために会社間でデータをコピーすることをお勧めします。 ボリュームが大きくなる可能性があるので、このアクションは営業時間外に実行することをお勧めします。

ポリシーにテーブルを追加する場合、既定では必須の外部キー フィールドのみが選択されます。 オプションの外部キーを手動で選択して追加する必要があります。

### <a name="conflict-resolution"></a>競合の解決
検証ルールは、共有ポリシーが有効化または更新された場合に実行されます。 会社間の不整合を表示および解決するには、"共有の問題を検索" を常に使用することをお勧めします。 不整合は、固有のレコード キーに基づいて会社間で属性値が異なる場合に発生します。 たとえば、同じ支払条件名などです。 たとえば、説明や支払方法の違いなどがあります。 データ共有の問題では、ポリシー内の他のすべての会社に対して使用する会社の値を、フィールドごとまたは完全なレコードのいずれかで選択できます。  

### <a name="customer-and-vendor-master-data-sharing-feature"></a>顧客および仕入先のマスター データ共有機能
顧客および仕入先のマスタ データ共有により、複数の会社間で顧客および仕入先のデータを共有することができます。 機能管理の顧客および仕入先マスター データ共有機能を使用して有効にできます。 上記のように、レコードおよび会社の最大数の制限を考慮することが重要です。 当事者の概念の一部であるテーブルでは、共有を有効にする前に追加の準備が必要になる場合があります。 同じ固有のレコード キーに対して会社間で関係者のリレーションシップが異なる場合は、すべて解決する必要があります。 たとえば、顧客 ID 番号 1000 は、会社間で異なる関係者 ID に関連付けられる場合があります。 この場合、顧客が名前変更機能を使用して個別の顧客として維持する場合は、関係者のリレーションシップを調整する必要があります。 詳細については、[当事者とグローバル アドレス帳](../data-entities/dual-write/party-gab.md)を参照してください。

### <a name="stop-or-reduce-sharing-scope"></a>共有範囲の停止または削減 
ポリシーを更新する前に、1 つ以上の会社の共有を削除することで共有を停止できます。 この方法は、共有からフィールドの選択を解除する場合に使用できます。 テーブルの共有を停止するには、ポリシーを無効にし、テーブルを削除する必要があります。 ポリシー全体を削除する場合も同様です。 これらすべてのシナリオで、除外したスコープの同期は停止しますが、既存のレコードは残ります。 テーブルまたは会社のレコード数が上限を超えた場合、共有は有効化または更新時に自動的に停止します。  

## <a name="master-company-sharing-preview"></a>マスター会社の共有 (プレビュー) 
マスター会社の共有を有効にする場合は、機能管理モジュールのマスター会社データ共有機能を使用します。 この機能は、管理モードで有効にする必要があります。

> [!NOTE]
> 共有範囲を停止または縮小することはできないので、運用環境で同じコンフィギュレーションを有効にする前に、マスター会社のデータ共有ポリシーを十分にテストおよび検証してください。 現在プレビュー モード中なので、生産用の Microsoft サポートではサポートされていません。 

マスター会社の共有ポリシーにテーブルが追加された場合、既定ですべての可能なフィールドが選択されます。 これには、マスター会社の共有でサポートされているすべてのテーブルのすべての外部キー フィールドが含まれます。 マスター会社のポリシーを無効にすることはできません。したがって、既定の外部キー フィールドに基づいて自動的に追加されるすべてのテーブルを手動で追加することが特に重要になります。 これは、有効になるテーブルとフィールドの共有範囲をよく理解するための唯一の方法です。 自動的に追加されたテーブルは、会社間データ共有の構成フォームには表示されません。 たとえば、仕入先テーブルが DRS を使用して既に共有されていない限り、外部キー リレーションに基づいて顧客テーブルが追加された場合に仕入先テーブルが追加されます。

外部キー リレーションに基づいてテーブルが自動的に追加されるのを回避する必要がある場合は、DRS ポリシー構成を回避策モードとして使用できます。 回避策は、マスター会社と運用していない会社をこのポリシーに追加して、テーブルの DRS ポリシーを作成して有効化することです。 外部キー テーブルを共有していない場合は、外部キー フィールドに対する値がないことも意味します。  

### <a name="limitations"></a>制限
次の制限があります。
+   子会社テーブルの変更追跡はサポートされていません。 たとえば、これは、データ管理では完全なエクスポートを使用する必要があることを意味します。
+   共有は、小売チャンネル データベースと組み合わせて使用することはできません。
+   共有はカーネル ロジックに基づいています。 これは、子会社の SQL に実際のレコードが存在しないことを意味します。

