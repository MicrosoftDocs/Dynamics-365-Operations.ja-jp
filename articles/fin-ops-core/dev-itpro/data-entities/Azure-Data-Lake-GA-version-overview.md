---
title: Azure Data Lake へのエクスポートの概要
description: この記事では、財務と運用環境を Data Lake に接続してデータで非表示にされているインサイトのロック解除をする方法について説明します。
author: MilindaV2
ms.date: 06/14/2022
ms.topic: overview
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2021-11-30
ms.openlocfilehash: d4c6afe0ace84512fb46f2eaeef96a91fbe6ae7e
ms.sourcegitcommit: f5b156f2e5ca99ad05b3d6e4a5d118631fd3064e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2022
ms.locfileid: "9012488"
---
# <a name="export-to-azure-data-lake-overview"></a>Azure Data Lake へのエクスポートの概要

[!include [banner](../includes/banner.md)]

## <a name="what-is-export-to-azure-data-lake"></a>Azure Data Lake へのエクスポートとは?

Azure Data Lake へのエクスポートにより、財務と運用環境を Data Lake に接続してデータで非表示にされているインサイトのロックを解除することができます。

Azure Data Lake へのエクスポート アドインを有効にするとき、財務と運用環境を指定した Data Lake に接続します。 承認されたユーザーは、財務と運用環境からその Data Lake にデータをコピーできます。 Power BI および Azure Synapse などのツールにより、Data Lake のデータに対して分析、ビジネス インテリジェンス、および機械学習のシナリオが有効になります。

財務と運用アプリのデータを選択すると、システムは Data Lake 内のデータの初期コピーを作成します。 その初期コピーを作成した後、変更されたデータを継続的に挿入、更新、および削除することにより、システムは Data Lake 内のデータを最新に保ちます。 サービスをエクスポートしたり管理したりする必要はなく、財務と運用ワークロードに負担になることはありません。

Data Lake に保存されたデータは、[Common Data Model](https://powerplatform.microsoft.com/common-data-model/) を使用してまとめられています。 Common Data Model によって、Data Lake のデータの価値が強化されます。 例については、機械可読の JavaScript Object Notation (JSON) 形式で追加のメタデータが提供されますので、下流ツールはデータのセマンティクスを決定することができます。 追加のメタデータには、テーブル構造、説明、およびデータ型が含まれます。

Azure Data Lake へのエクスポートは、Microsoft が完全に管理する、スケーラブルで可用性の高いサービスです。 組み込みのディザスター リカバリーが含まれます。 サポートされる機能の一部を次に示します。

- 最大 350 テーブル選択できます。 データに対するすべての変更は、Data Lake 内で継続的に更新されます。 これらの変更には、挿入、更新、および削除の操作が含まれます。
- テーブルまたはエンティティを使用してデータを選択できます。 エンティティを使用する場合、基本テーブルはサービスにより選択されます。
- 標準エンティティとカスタム エンティティおよびテーブルの両方を選択できます。
- Microsoft Azure Synapse Analytics または他の多くのサード パーティ ツールを使用して、Data Lake でデータを処理することができます。

ストレージ アカウントは、財務と運用環境と同じ Azure リージョンにある必要があります。

サービスのインストール時に、ほぼリアルタイムのデータ変更やビジネス イベントを有効にするよう選択することもできます。

## <a name="enable-near-real-time-data-changes"></a>ほぼリアルタイムのデータ変更の有効化 
この機能を選択した場合、データは Data Lake でほぼリアルタイムで挿入、更新、および削除されます。 データが財務と運用環境内で変更されると、数分以内に Data Lake 内のデータが更新されます。

さらに、Data Lake 内の変更されたデータを使用して、下流のデータ ウェアハウスを更新することができます。 変更データ フォルダーを使用して、データに行われた変更を簡単に特定し、ほぼリアルタイムでデータ パイプラインを作成することができます。

ほぼリアルタイムの変更フィードの詳細については、[Azure Data Lake の変更データ](azure-data-lake-change-feeds.md)を参照してください。

## <a name="business-events"></a>ビジネス イベント 
この機能を有効にすると、Data Lake の何か重要な問題が発生した場合に警告を発することができます。 たとえば、レイクでデータが初期化されると警告を受け取る可能性があります。 データの最初のコピーが完了すると、システムによってビジネス イベントが生成されます。 [ビジネス イベント](/powerapps/developer/data-platform/business-events) は、Dynamics 365 と Dataverse のフレームワークであり、簡単にインテリジェント アクションと自動化を作成できます。 たとえば、Power Platform に統合されているツールである [Power Automate](https://powerautomate.microsoft.com/) を使用して、自動化されたワークフローを構築し、ダウンストリームのデータ パイプラインを自動的にトリガするなどのアクションを実行できます。

エクスポートから Data Lake サービスによって生成されたビジネス イベントの詳細については、[エクスポートから Azure Data Lake サービスによって生成されたビジネス イベント](Azure-Data-Lake-Generates-Biz-events.md) を参照してください。

次のセクションでは、使用可能なプレビュー機能について説明します。

> [!NOTE]
> プレビュー機能は完成していません。 顧客が早期アクセスを使用してフィードバックを提供できるよう、プレビュー ベースで使用可能になりました。 プレビュー機能は、機能が限定または制限されていて、運用上の用途を目的としていないことがあり、選択された地理的な地域でのみ使用できることがあります。
>
> プレビュー機能を有効にすることにより、[追加使用条件](../../fin-ops/get-started/public-preview-terms.md)に同意します。

## <a name="enhanced-metadata-preview"></a>拡張メタデータ (プレビュー)

データに加え、Data Lake には、データの名前、データ型、およびサイズを記述したメタデータが含まれています。 レイクでは、データ ファイルに加え、データ ファイルに対応するフォルダー レベルでメタデータ ファイルが表示されます。 Data Lake 機能にエクスポートをインストールし、データ レイクに追加するデータを選択すると、システムはデータに加えてメタデータ ファイルを書き込みます。 Data Lake へのエクスポートをインストールする際 **拡張メタデータ (プレビュー)** オプションを選択する場合、システムによって更に多くのメタデータが追加されます。 メタデータと拡張メタデータ (プレビュー) 機能については、[Azure Data Lake のデータと格納メタデータ](Azure-Data-Lake-Enhanced-Metadata.md) を参照してください。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="what-is-azure-data-lake-and-what-benefits-do-data-lakes-offer"></a>Azure Data Lake とはなんですか? Azure Data Lake にはどのようなメリットがありますか。

Azure Data Lake は、Azure クラウドのテクノロジで、分析のために「ビッグ データ」の保存と操作を行い、機械学習と AI に適用することができます。 この記事で、「Data Lake」 という場合、Azure Data Lake Storage Gen2 に基づく記憶域テクノロジーのことを指します。

Data Lakes が提供するクラウドストレージは、リレーショナルデータベースが提供するものよりも安価です。 そのため、大量のデータをクラウドに格納できます。 このデータには、従来、業務システムとデータ ウェアハウス、およびデバイスとセンサーのデータに格納されている、デバイスからの信号などの業務データが含まれます。 さらに、Data Lakeは、大量のデータの報告、照会、変換を実現する広範なツールとプログラミング言語に対応しています。

### <a name="how-much-does-this-service-cost"></a>このサービスの費用はどのくらいか?

独自のサブスクリプションの Data Lake をプロビジョニングする必要があります。 Azure Data Lake へのエクスポート サービスは、データを独自の Data Lake にコピーします。 Power BI、Spark、および Microsoft や他のソースからの多くのツールを使用して、Data Lake のデータをクエリできます。

Azure Data Lake へのエクスポートは、Dynamics 365 サービスへのサブスクリプションに含まれるアドオン サービスです。

自身のサブスクリプションには Data Lake Storage Gen2 が含まれているため、Data Lake にデータを読み書きする際に発生するデータ ストレージや入出力 (I/O) のコストを負担する必要があります。 また、財務と運用アプリが Data Lake にデータを書き込んだり、データを更新することにより、I/O コストが発生する場合もあります。 領域内の I/O コストを削減するために、財務と運用アプリでは財務と運用環境と同じ国や地理的リージョンに Data Lake をプロビジョニングする必要があります。

FastTrack ソリューション テンプレートは、財務と運用アプリの業務量に基づいて、ストレージのコストを見積もるツールを提供します。 詳細については、[FastTrack for Dynamics 365- CostCalculator](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CostCalculator) を参照してください。

### <a name="i-am-currently-using-a-byod-service-why-should-i-transition-to-data-lake"></a>現在、BYOD サービスを使用しています。 Data Lake へ移行する必要があるのはなぜですか?

顧客は、財務と運用アプリからデータを抽出するのに[自分のデータベースの持ち込み (BYOD)](../analytics/export-entities-to-your-own-database.md) を使用し、レポートや分析にそのデータを活用することができます。 BYOD では、財務と運用アプリからエクスポートされたデータを保存する際に、Azure SQL データベースのプロビジョニングとメンテナンスが必要となります。

運用レポート シナリオでは、BYOD でエクスポートされたデータ (つまり SQL データベース) はレポートを作成するために使用されます。

より複雑なデータ ウェアハウス シナリオでは、BYOD は、財務と運用データの *スナップショット* が保持されるステージング領域として使用されます。 BYOD ステージング領域からデータ ウェアハウスにデータをコピーする下流のデータ パイプラインがある場合があります。

これらのタイプのシナリオに対して現在、BYOD を使用している場合、Data Lake へのエクスポート機能に移行できます。 この場合、次のような恩恵が得られることがあります。

- **データが既に存在するため、エクスポートの必要がありません。** Data Lake 統合は、財務と運用アプリで変更された Data Lake への継続的なデータのエクスポートを管理します。 BYOD の場合のように、データ エクスポートの監視と管理を行う必要はありません。
- **データ ストレージのコストが削減されます。** データは、BYOD が要求する SQL データベース内にではなく、Data Lake に格納されます。 したがって、顧客は Azure SQL データベースよりも安価なストレージ メディアを使用してデータを保存できます。
- **既存の下流/消費パイプラインを維持することができます。** [Azure Synapse Analytics サーバーレス SQL プール](/azure/synapse-analytics/sql/on-demand-workspace-overview) を使用して、レイク内のデータに対して T-SQL ビュー定義を作成し、BYOD からデータを読み取るのと同じ方法でデータを読み取ることができます。 データ統合パイプラインを再指定して、主なコストを発生させることなく、Data Lake でデータを使用することができる場合があります。 

BYOD ソリューションは、財務と運用アプリから Azure SQL データベースにエンティティ データの形状をエクスポートします。 **Data Lake へのエクスポート** 機能により、エンティティの形状またはテーブルを使用してデータを選択できます。 Data Lake にエクスポートされたデータを使用すると、 [FastTrack for Dynamics 365- CDMUtilSolution](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CDMUtilSolution) を使用して、Azure Synapse Analytics サーバーレス SQL プール内のエンティティの形状を再作成できます。  

### <a name="how-is-the-data-stored-in-the-lake"></a>データはどのように Data Lake に格納されますか?
Data Lake 内のデータは、システムによって管理されるフォルダー構造に CSV ファイルとして格納されます。 フォルダー構造は、財務と運用アプリのデータ構成に基づいています。 例については、**財務**、**サプライ チェーン**、**コマース** などの名前を持つフォルダーが表示され、これらのフォルダー内に、**売掛金勘定**、または **買掛金勘定** などの名前を持つサブフォルダーが表示されます。 下位階層には、各テーブルの実際のデータを含むフォルダーが表示されます。 テーブルレベルのフォルダー内には、複数の CSV ファイルと、データの形式を説明するメタデータ ファイルが表示されます。 

財務と運用アプリのデータが更新される際に、テーブル フォルダーの CSV ファイル内の対応するデータ行が更新されます。 財務と運用アプリのテーブルに新しい行を追加するか、既存の行を削除すると、対応する CSV ファイルから新しい行が追加または削除されます。 

例については、財務と運用アプリでデータ構造が変更された場合、テーブルに新しいフィールドを追加すると、その変更を反映するように、Data Lake 内のメタデータ ファイルが更新されます。 データ構造の変更を破壊的に行う場合は、システムがテーブル フォルダー全体 (すべての CSV ファイル) を再設定する場合もあります。 例については、財務と運用アプリのテーブルからフィールドが削除される場合、まれに破壊的なシナリオでは、テーブル フォルダー全体が再設定されます。 新しいフィールドを追加した場合、すべてのデータ ファイルは再設定されません。 変更された行を含むデータ ファイルだけが、新しいフィールドを含むように更新されます。 多くの消費元のツールは、新しく追加されたデータ フィールド (*スキーマ ドリフト* と呼ばれる機能) を使用できるので、システムはフォルダー全体を再設定できません。  

### <a name="how-can-i-consume-data-in-the-lake"></a>Data Lake のデータをどのように消費できますか?
Microsoft およびサード パーティの各種のツールを使用して、Data Lake のデータを管理することができます。 ほとんどのツールでは、CSV ファイルとして Data Lake 内に保存されているデータを消費できます。  

Azure Synapse Analytics サーバーレス SQL プールを使用すると、Transact-SQL 言語 (T-SQL) を使用して、同じ言語のデータを消費することができます。 T-SQL 言語は、多くのツールによって広くサポートされています。 データベースからデータを消費する場合と同様に、Synapse ワークスペースを Data Lake のデータ上で定義し、T-SQL、Spark または Syapse Pipelines を使用することができます。 レイクのデータに Synapse ワークスペースを作成するには、[FastTrack Solutions for Dynamics 365 - CDMUtilSolution](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CDMUtilSolution) を使用します。

既製のソリューション テンプレートを使用して、Data Lake から SQL Server データ ウェアハウスまたは別の接続先にデータをコピーすることもできます。 詳細については、[FastTrack Solutions for Dynamics 365 - SynapseToSQL_ADF](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/SynapseToSQL_ADF) を参照してください。

### <a name="how-often-is-data-in-the-data-lake-updated"></a>Data Lake のデータはどのくらいの頻度で更新されますか?

データを選択すると、Azure Data Lake へのエクスポート サービスは、Data Lake 内のデータの初期コピーを作成します。 複数のテーブルを選択する場合、システムは一度に 10 個のテーブルを取得して初期コピーを作成します。 データのサイズやテーブル内のレコード数によっては、このプロセスに数分または数時間かかる場合があります。 エクスポートの進行状況が画面に表示されます。

初期コピーが作成された後、財務と運用アプリで変更が行われると、システムによってデータが継続的に更新されます。 レコードの挿入、更新、または削除を行う場合、Data Lake 内のデータ レコードは、それに応じて挿入、更新、または削除されます。

オプションのほぼリアルタイムの変更機能を使用すると、財務と運用環境の変更から数分以内に Data Lake 内のデータは更新されます。 それ以外の場合は、財務と運用環境内の変更から数時間以内に Data Lake 内のデータは更新されます。

財務と運用環境にある **Data Lake へのエクスポート** のページは、Data Lake 内のデータが最後に更新された時のタイム スタンプを表示します。 システムは、Data Lake 内のデータが更新された時刻を識別するのに役立つデータ フィールドも追加します。 ダウンストリーム プロセスでは、タイム スタンプを使用して、Data Lake 内で変化するデータを検出して処理できます。

### <a name="why-dont-i-see-the-export-to-data-lake-feature-in-my-environment"></a>環境で Data Lake へのエクスポート機能が表示されないのはなぜですか?

Data Lake へのエクスポート機能は、米国、カナダ、英国、ヨーロッパ、スイス、東南アジア、インド、東アジア、オーストラリア、ラテン アメリカ、および日本の地域で使用できます。 財務と運用環境がそれらの地域にある場合は、Microsoft Dynamics Lifecycle Services (LCS) を使用して、環境でこの機能を有効にできます。 機能は最終的により多くの地域で使用可能になります。

Data Lake へのエクスポート機能は、Tier 1 (開発者) 環境では使用できません。 この機能を有効にするには、クラウド ベースの Tier 2 またはそれ以上のサンドボックス環境が必要です。

レベル 1 (開発者) 環境では、[FastTrack for Dynamics 365- GitHub ツール](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Analytics/AzureDataFactoryARMTemplates/SQLToADLSFullExport/ReadmeV2.md) を使用してプロトタイプを使用、または機能の実装を計画できます。 このツールを使用すると、機能がエクスポートしたのと同じ形式で、階層 1 またはサンドボックス環境のデータをストレージ アカウントにエクスポートすることができます。

### <a name="how-can-i-stay-in-touch-about-upcoming-features"></a>今後の機能に関してどのように連絡を取り合えますか?

数か月後に、Microsoft はより多くの地域で Data Lake へのエクスポート機能を有効にします。 また、他の機能についても積極的に取り組んでいます。 製品チームや他の顧客やパートナーに連絡して質問を行いますか? 製品チームに直接フィードバックを提供しますか? その場合、[プレビュー Yammer グループ](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=32768909312&view=all)に参加することもできます。 毎週の「営業時間」のオンライン ミーティングに参加し、Yammerオンライン フォーラムを使用して連絡を取り合い、質問することができます。
