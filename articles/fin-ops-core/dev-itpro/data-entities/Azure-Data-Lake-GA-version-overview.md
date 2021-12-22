---
title: Azure Data Lake へのエクスポートの概要
description: このトピックでは、Finance and Operations 環境を Data Lake に接続してデータで非表示にされているインサイトのロック解除をする方法について説明します。
author: MilindaV2
ms.date: 11/20/2021
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2021-11-30
ms.openlocfilehash: 047a4fa39ae4c105b5789fe695c86d42c6cb8d58
ms.sourcegitcommit: ac23a0a1f0cc16409aab629fba97dac281cdfafb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2021
ms.locfileid: "7867628"
---
# <a name="export-to-azure-data-lake-overview"></a>Azure Data Lake へのエクスポートの概要

[!include [banner](../includes/banner.md)]

## <a name="what-is-export-to-azure-data-lake"></a>Azure Data Lake へのエクスポートとは?

Azure Data Lake へのエクスポートにより、Finance and Operations 環境を Data Lake に接続してデータで非表示にされているインサイトのロックを解除することができます。

Azure Data Lake へのエクスポート アドインを有効にするとき、Finance and Operations 環境を指定した Data Lake に接続します。 承認されたユーザーは、Finance and Operations 環境からその Data Lake にデータをコピーできます。 Power BI および Azure Synapse などのツールにより、Data Lake のデータに対して分析、ビジネス インテリジェンス、および機械学習のシナリオが有効になります。

Finance and Operations アプリのデータを選択すると、システムは Data Lake 内のデータの初期コピーを作成します。 その初期コピーを作成した後、変更されたデータを継続的に挿入、更新、および削除することにより、システムは Data Lake 内のデータを最新に保ちます。 サービスをエクスポートしたり管理したりする必要はなく、Finance and Operations ワークロードに負担になることはありません。

Data Lake に保存されるデータは、Common Data Model 形式を使用するフォルダー構造で整理されています。 Common Data Model 形式は、機械可読の JavaScript Object Notation (JSON) 形式で追加のメタデータを提供しま、下流のツールはデータのセマンティクスを決定することができます。 追加のメタデータには、テーブル構造、説明、およびデータ型が含まれます。

Azure Data Lake へのエクスポートは、Microsoft が完全に管理する、スケーラブルで可用性の高いサービスです。 組み込みのディザスター リカバリーが含まれます。 サポートされる機能の一部を次に示します。

- 最大 200 テーブル選択できます。 データに対するすべての変更は、Data Lake 内で継続的に更新されます。 これらの変更には、挿入、更新、および削除の操作が含まれます。
- テーブルまたはエンティティを使用してデータを選択できます。 エンティティを使用する場合、基本テーブルはサービスにより選択されます。
- 標準エンティティとカスタム エンティティおよびテーブルの両方を選択できます。
- Transact-SQL (T-SQL) と Synapse SQL Serverless を使用して、Data Lake のデータを操作することができます。 [CDMUtilSolution](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CDMUtilSolution) という名前の一連の既製のソリューション テンプレートを使用すると、Data Lake のデータを簡単に Synapse ワークスペースに統合することができます。

ストレージ アカウントは、Finance and Operations 環境と同じ Azure リージョンにある必要があります。

次のセクションでは、使用可能なプレビュー機能について説明します。

> [!NOTE]
> プレビュー機能は完成していません。 ただし、顧客が早期アクセスを使用してフィードバックを提供できるよう、プレビュー ベースで使用可能です。 プレビュー機能は、機能が限定または制限されていて、運用上の用途を目的としていないことがあり、選択された地理的な地域でのみ使用できることがあります。
>
> プレビュー機能を有効にすることにより、[追加使用条件](../../fin-ops/get-started/public-preview-terms.md)に同意します。

## <a name="enable-near-real-time-data-changes-preview"></a>ほぼリアルタイムのデータ変更を有効にする (プレビュー)

このプレビュー機能を選択した場合、データは Data Lake でほぼリアルタイムで挿入、更新、および削除されます。 データが Finance and Operations 環境内で変更されると、数分以内に Data Lake 内のデータが更新されます。

この機能を使用すると、選択できるテーブルの数は 350 に増加します。

さらに、Data Lake 内の変更されたデータを使用して、下流のデータ ウェアハウスを更新することができます。 変更データ フォルダーを使用して、データに行われた変更を簡単に特定し、ほぼリアルタイムでデータ パイプラインを作成することができます。

ほぼリアルタイムの変更フィードの詳細については、[Azure Data Lake の変更データ](azure-data-lake-change-feeds.md)を参照してください。


## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="what-is-azure-data-lake-and-what-benefits-do-data-lakes-offer"></a>Azure Data Lake とはなんですか? Azure Data Lake にはどのようなメリットがありますか。

Azure Data Lake は、Azure クラウドのテクノロジで、分析のために「ビッグ データ」の保存と操作を行い、機械学習と AI に適用することができます。 このトピックで、「Data Lake」 という場合、Azure Data Lake Storage Gen2 に基づく記憶域テクノロジーのことを指します。

Data Lakes が提供するクラウドストレージは、リレーショナルデータベースが提供するものよりも安価です。 そのため、大量のデータをクラウドに格納できます。 このデータには、従来、業務システムとデータ ウェアハウス、およびデバイスとセンサーのデータに格納されている、デバイスからの信号などの業務データが含まれます。 さらに、Data Lakeは、大量のデータの報告、照会、変換を実現する広範なツールとプログラミング言語に対応しています。

### <a name="how-much-does-this-service-cost"></a>このサービスの費用はどのくらいか?

独自のサブスクリプションの Data Lake をプロビジョニングする必要があります。 Azure Data Lake へのエクスポート サービスは、データを独自の Data Lake にコピーします。 Power BI、Spark、および Microsoft や他のソースからの多くのツールを使用して、Data Lake のデータをクエリできます。

Azure Data Lake へのエクスポートは、Dynamics 365 サービスへのサブスクリプションに含まれるアドオン サービスです。

自身のサブスクリプションには Data Lake Storage Gen2 が含まれているため、Data Lake にデータを読み書きする際に発生するデータ ストレージや入出力 (I/O) のコストを負担する必要があります。 また、Finance and Operations アプリが Data Lake にデータを書き込んだり、データを更新することにより、I/O コストが発生する場合もあります。 領域内の I/O コストを削減するために、Finance and Operations アプリでは Finance and Operations 環境と同じ国や地理的リージョンに Data Lake をプロビジョニングする必要があります。

FastTrack ソリューション テンプレートは、Finance and Operations アプリの業務量に基づいて、ストレージのコストを見積もるツールを提供します。 詳細については、[CostCalculator](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CostCalculator) を参照してください。

### <a name="i-am-currently-using-a-byod-service-why-should-i-transition-to-data-lake"></a>現在、BYOD サービスを使用しています。 Data Lake へ移行する必要があるのはなぜですか?

顧客は、Finance and Operations アプリからデータを抽出するのに[自分のデータベースの持ち込み (BYOD)](../analytics/export-entities-to-your-own-database.md) を使用し、レポートや分析にそのデータを活用することができます。 BYOD では、 Finance and Operations アプリからエクスポートされたデータを保存する際に、Azure SQL データベースのプロビジョニングとメンテナンスが必要となります。

運用レポート シナリオでは、BYOD でエクスポートされたデータ (つまり SQL データベース) はレポートを作成するために使用されます。

より複雑なデータ ウェアハウス シナリオでは、BYOD は、Finance and Operations データの *スナップショット* が保持されるステージング領域として使用されます。 BYOD ステージング領域からデータ ウェアハウスにデータをコピーする下流のデータ パイプラインがある場合があります。

これらのタイプのシナリオに対して現在、BYOD を使用している場合、Data Lake へのエクスポート機能に移行できます。 この場合、次のような恩恵が得られることがあります。

- **データが既に存在するため、エクスポートの必要がありません。** Data Lake 統合は、Finance and Operations アプリで変更される場合に行われる、Data Lake への継続的なデータのエクスポートをエクスポートを管理します。 BYOD の場合のように、データ エクスポートの監視と管理を行う必要はありません。
- **データ ストレージのコストが削減されます。** データは、BYOD が要求する SQL データベース内にではなく、Data Lake に格納されます。 したがって、顧客は Azure SQL データベースよりも安価なストレージ メディアを使用してデータを保存できます。
- **既存の下流/消費パイプラインを維持することができます。** 最初のタイプのシナリオにおいて、多くのレポート ツールは、T-SQL を使用してデータを読み取ることができるため、SQL データベースで動作します。 Azure Synapse Analytics を使用して、SQL Server のエンドポイントを作成できます。 Synapse には、T-SQL 言語を使用して Data Lake のクエリを可能にする SQL のオンデマンド機能が含まれています。 2 つ目のタイプのシナリオでは、T-SQL エンドポイントを使用することができますが、データ統合パイプラインで、Data Lake でファイルを使用できることがあります。 どちらの方法でも、主なコストを発生させることなく BYOD から移行できます。

### <a name="how-often-is-data-in-the-data-lake-updated"></a>Data Lake のデータはどのくらいの頻度で更新されますか?

データを選択すると、Azure Data Lake へのエクスポート サービスは、Data Lake 内のデータの初期コピーを作成します。 複数のテーブルを選択する場合、システムは一度に 10 個のテーブルを取得して初期コピーを作成します。 データのサイズやテーブル内のレコード数によっては、このプロセスに数分または数時間かかる場合があります。 エクスポートの進行状況が画面に表示されます。

初期コピーが作成された後、Finance and Operations アプリで変更が行われると、システムによってデータが継続的に更新されます。 レコードの挿入、更新、または削除を行う場合、Data Lake 内のデータ レコードは、それに応じて挿入、更新、または削除されます。

オプションのほぼリアルタイムの変更機能 (現在プレビュー中) を使用すると、Finance and Operations 環境の変更から数分以内に Data Lake 内のデータは更新されます。 それ以外の場合は、Finance and Operations 環境内の変更から数時間以内に Data Lake 内のデータは更新されます。

Finance and Operations 環境にある **Data Lake へのエクスポート** のページは、Data Lake 内のデータが最後に更新された時のタイプ スタンプを表示します。 システムは、Data Lake 内のデータが更新された時刻を識別するのに役立つデータ フィールドも追加します。 ダウンストリーム プロセスでは、タイム スタンプを使用して、Data Lake 内で変化するデータを検出して処理できます。

### <a name="why-dont-i-see-the-export-to-data-lake-feature-in-my-environment"></a>環境で Data Lake へのエクスポート機能が表示されないのはなぜですか?

Data Lake へのエクスポート機能は、以下の地域でのみ使用できます: **米国**、**カナダ**、**英国**、**ヨーロッパ**、**東南アジア**、**インド**、**東アジア**、**オーストラリア**、および **日本** リージョン。 Finance and Operations 環境がそれらの地域にある場合は、Microsoft Dynamics Lifecycle Services (LCS) を使用して、環境でこの機能を有効にできます。 機能は最終的により多くの地域で使用可能になります。

Data Lake へのエクスポート機能は、Tier 1 (開発者) 環境では使用できません。 この機能を有効にするには、クラウド ベースの Tier 2 またはそれ以上のサンドボックス環境が必要です。

Tier 1 (開発者) 環境では、[GitHub ツール](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Analytics/AzureDataFactoryARMTemplates/SQLToADLSFullExport/ReadmeV2.md) を使用して機能の実装のプロトタイプを作成または計画できます。 このツールを使用すると、機能がエクスポートしたのと同じ形式で、階層 1 またはサンドボックス環境のデータをストレージ アカウントにエクスポートすることができます。

### <a name="how-can-i-stay-in-touch-about-upcoming-features"></a>今後の機能に関してどのように連絡を取り合えますか?

数か月後に、Microsoft はより多くの地域で Data Lake へのエクスポート機能を有効にします。 また、他の機能についても積極的に取り組んでいます。 製品チームや他の顧客やパートナーに連絡して質問を行いますか? 製品チームに直接フィードバックを提供しますか? その場合、[プレビュー Yammer グループ](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=32768909312&view=all)に参加することもできます。 毎週の「営業時間」のオンライン ミーティングに参加し、Yammerオンライン フォーラムを使用して連絡を取り合い、質問することができます。
