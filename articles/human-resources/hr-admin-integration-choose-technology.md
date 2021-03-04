---
title: データ統合テクノロジの選択
description: この記事では、Human Resources で管理されるデータの統合について説明します。 ニーズに最適なテクノロジを判断する際に役立つさまざまな統合テクノロジについて説明します。
author: andreabichsel
manager: AnnBe
ms.date: 02/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9e6eeac66cff24d193e30aa942039707fc0aed52
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528344"
---
# <a name="choose-a-data-integration-technology"></a>データ統合テクノロジの選択

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

この記事では、Dynamics 365 Human Resources で管理されているデータを統合するための情報を提供します。 ニーズに最適なテクノロジを判断する際に役立つさまざまな統合テクノロジについて説明します。

## <a name="data-integration-background"></a>データ統合の背景

業務データは、会社を比類ないものにする重要な資産です。 業務データは非常に重要です。 業務全体で収集されたデータ間の関係を使用して、組織全体の業務プロセスやビジネス インテリジェンスを向上させることができます。 どのようなシステムからの業務データにも、簡単、安全、安定したアクセスを提供するよう努めています。

これまで、複数のシステム間のデータの統合は困難でした。
Microsoft はデータ統合を容易にするための措置を講じており、その目標に向けた大きな一歩は [Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro) によって実現されます。

Human Resources では、Common Data Service が Human Resources データの推奨パブリック インターフェイスになります。 時間の経過とともに、Human Resources によって管理されるもっとも重要なすべてのデータが Common Data Service で公開される予定です。 ほとんどの統合アプリケーションにとって最適な技術として、Common Data Service をお勧めします。

Common Data Service には、アプリケーションが必要とするすべてのデータが含まれているわけではありません。 プロジェクト タイムラインには、別のテクノロジが必要になる場合もあります。 Common Data Service が統合のニーズを満たしていない場合は、必ずお知らせください。

## <a name="integration-technologies"></a>統合の技術

以下のセクションでは、Human Resources で使用するために用意されているさまざまなデータ統合テクノロジについて説明します。

### <a name="common-data-service-entities"></a>Common Data Service エンティティ

Common Data Service は、Human Resources の推奨のパブリック データ インターフェイスです。 [Dynamics 365 Customer Engagement](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement) ソリューションで使用される Dynamics 365 XRM プラットフォームから生まれました。

Common Data Serviceは、データ エンティティ用のプラットフォームと API を提供します。 Human Resources を展開すると、Common Data Service インスタンスに接続されます。 Human Resources データのエンティティは、その Common Data Service インスタンスに展開されます。 エンティティとそのデータは、Common Data Service インスタンスに接続できるすべてのアプリケーションで使用できます。 Human Resources では、Common Data Service エンティティとの間でデータを同期します。

統合アプリで必要なデータ エンティティが Common Data Service にある場合は、[Common Data Service とそれがサポートする API](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer) を完全に使用できます。 サポートされる API の 1 つに [Dynamics 365 Web API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api) があります。この API は、Common Data Service データにアクセスするための OData 実装を提供します。

Common Data Service エンティティおよび関連付けられている API は、Web アプリケーション、Web サービス/API から、また OData フィードに接続するその他のアプリケーションから、Human Resources データにアクセスするための最良のオプションです。

> [!NOTE]
> Common Data Service を Human Resources の優先データ インターフェイスにするという決定は比較的最近のことなので、統合に必要な Human Resources データ エンティティが Common Data Service でまだ使用できない場合があります。
</br>
> Common Data Service で利用できる Human Resources エンティティの一覧については、[Human Resources および Common Data Service](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities) を参照してください。
> </br>
> 統合に必要な Human Resources エンティティがまだ使用できない場合は、データ エンティティが利用できるまで待つか、または以下に示すその他の統合テクノロジのいずれかを使用する必要があります。
> </br>
> 既定では、Common Data Service の統合は、提供されたデモ データを含まない新しい環境ではオフになっています。 デモ データが含まれる新しい環境ではオンになっており、環境はデータの準備時にデータとの同期を開始します。 データと同期する準備が整ったら、統合をオンにすることができます。

### <a name="dmfdixf-entities"></a>DMF/DIXF エンティティ

Finance and Operations アプリケーションと同じプラットフォームで主に構築された Human Resources は、[データ管理フレームワーク (DMF)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)　を提供します。 DMF は、データ インポート エクスポート フレームワーク (DIXF) とも呼ばれます。 Human Resources には、Human Resources データのインポートとエクスポートに使用できる一連のデータ エンティティが用意されています。 Common Data Service エンティティは Human Resources の優先データ統合インターフェイスですが、DMF エンティティは次のような環境でも有用です:

- Common Data Service エンティティをまだ利用できない。

- 統合に、高性能なバルク データ インポート/エクスポート機能が必要である。

現時点で、DMF エンティティは、Human Resources データに対してもっとも完全なデータ カバレージを提供します。

DMFは、ユーザー インターフェイスでユーザー フィードバックがすぐに必要な場合など、リアルタイム統合には適していません。 パッケージ操作はスケジュールされたバッチ ジョブであり、多くの場合、バッチ サービスが実行のためにジョブを取得するまでに 1 - 2 分以上の待機時間があり、さらにインポート/エクスポート操作を完了するために必要な時間があります。

DMF は、高スループット (夜間にスケジュールされている数千のレコードのインポート/エクスポートなど) が必要なときに最適なオプションになることがあります。

> [!NOTE]
> DMF は、Attract および Onboard には使用できません。

### <a name="dmf-package-rest-api"></a>DMF パッケージ REST API

DMF には、データ パッケージの操作のために [REST API](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api) が用意されています。 この API を使用して、プログラムで DMF と対話することで、次のような操作が可能になります。

- データ パッケージのインポート

- データ パッケージのエクスポート

- インポート/エクスポート操作のステータスの確認

DMF パッケージ REST API は Human Resources: Core HR で完全にサポートされています。

### <a name="azure-sql-db-byod"></a>Azure SQL DB (BYOD)

DMF はさらに、Human Resources がユーザー独自の Microsoft Azure SQL データベースにデータをエクスポートできる強力な機能 ([自分のデータベースの持ち込み](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database)、または BYOD と呼ばれる) を提供します。 この機能は、非常に高い柔軟性を提供します。 データがユーザー独自の SQL データベースに存在する場合は、SQL データ ストアに接続できるアプリケーションやミドルウェアを利用できます。

BYOD は、主に読み取り専用ソリューションです。 必要なデータを操作して Azure SQL データベース (データ マッシュ アップなど) に格納することができますが、Azure SQL データベースに格納されたデータは Human Resources に同期されません。

BYOD は、[Azure Data Factory](https://docs.microsoft.com/azure/data-factory/) パイプラインのデータ ソースとして、ソリューション、データ統合、データ マッシュ アップを報告するために適しています。

> [!NOTE]
> BYOD は、Attract および Onboard には使用できません。

### <a name="odata-enabled-entities"></a>OData 対応エンティティ

ほとんどの DMF エンティティは、Human Resources データ サービス (OData) を使用したアクセスにも有効です。 [Finance and Operations OData サービス](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata) に提供されるドキュメントは、独自の OData 公開エンティティを作成する場合を除き、Human Resources に適用されます。

Common Data Service および Common Data Service によって ([Dynamics 365 Web API](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8)) を通じて) 用意されている OData 実装は、Human Resources データ サービスよりも優先されますが、現在のところ、Human Resources データ サービスは、Human Resources データに対してより完全なエンティティ カバレージを提供します。

### <a name="excel-add-in"></a>Excel アドイン

[Excel アドイン](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) は、内部にある OData 対応エンティティを利用します。 このアドインは、エンド ユーザーが使い慣れた Excel UI を使用して Human Resources データを取得および変更するために便利な方法を説明します。

Excel アドインは、ビジネス ドメインの専門家による一時的なデータのインポート/エクスポートに適しています。 プログラムによる自動化を必要とする繰り返して発生するデータ統合の場合は、別の統合テクノロジがより適切です。

### <a name="data-integrator"></a>データ インテグレーター

[データ インテグレーター サービス](https://docs.microsoft.com/powerapps/administrator/data-integrator) を使用して、Common Data Service との間でデータを統合できます。 データ インテグレーターを使用すると、多くの場合、アプリケーション開発者が特定の統合に合せて調整した定義済みのテンプレートに基づく統合プロジェクトを定義することができます。 統合プロジェクトを定期的なスケジュールで自動的に実行するようにスケジュールしたり、手動で実行したりできます。

データ インテグレータ プロジェクトは、Common Data Service バッチ統合に適しています。 これらは、Dynamics 365 ファミリのアプリケーション間の統合に最適です。 たとえば、Microsoft は、Human Resources からのデータを Dynamics 365 Finance に統合するためのデータ インテグレーター テンプレートを提供します。 テンプレートの詳細については、[Dynamics 365 Human Resources から Dynamics 365 Finance への統合](hr-admin-integration-finance.md) を参照してください。

### <a name="power-query"></a>Power Query

データ インテグレーターは、[高度なクエリ機能](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering) を通じて [Power Query](https://docs.microsoft.com/power-query/power-query-what-is-power-query) をサポートしています。 Power Query は、豊富な M 数式言語を含む、強力で柔軟なデータ フィルター処理と変換を提供します。 Power Query は、Power BI レポートを作成したことがあれば、親しみやすいでしょう。

## <a name="deciding-on-an-integration-technology"></a>統合テクノロジの決定

非常に多くのさまざまな統合テクノロジが使用可能な場合、使用する統合方法を決定することに困惑することがあります。 Common Data Service のデータ カバレージが完全になるに伴って、ほとんどの場合、Common Data Service が優先データ インターフェイスとなり、その決定は簡単になります。 しかし、それまでは、Common Data Service がユーザーのニーズを満たさないことがあります。 次のテーブルは、統合テクノロジ オプションの主要な特性のいくつかをまとめたものです。

| テクノロジ/ツール/API    | 定期統合                   | 同期/非同期                    | API によるプログラム アクセス        | 適切なデータ量                                   | データ カバレージ                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Common Data Service エンティティ           | データ インテグレーターまたはミドルウェアを使用します | 同期、非同期、バッチ (データ インテグレーターを使用) | Dynamics 365 Web API (OData) を使用 | ユース ケースによって異なります (対話型の使用に対してページングをサポート) | 改善<sup>2</sup>                       |
| DMF エンティティ           | ミドルウェアを使用してスケジュール        | 非同期、バッチ                                | DMF パッケージ REST API を使用         | 高 (数十万のレコード)                    | 高                                |
| DMF パッケージ REST API   | ミドルウェアを使用してスケジュール        | 非同期、バッチ                                | はい                                       | 高 (数十万のレコード)                    | API はすべての DMF エンティティをサポートします       |
| BYOD                   | 管理者による Human Resources でのスケジュール        | 非同期、バッチ                                | いいえ<sup>3</sup>                                    | 高 (数十万のレコード)                    | すべての DMF エンティティをサポートします           |
| OData 対応エンティティ | ミドルウェアを使用                    | 同期                                        | Human Resources データ サービス (OData) を通じて  | ユース ケースによって異なります (対話型の使用に対してページングをサポート) | 高                                |
| Excel アドイン           | 無                                       | 同期                                        | 無                                        | 中間 (数十万のレコード)                      | すべての OData 対応エンティティをサポートします |
| データ インテグレーター        | データ インテグレーターでスケジュール        | 非同期、バッチ                                | いいえ                                        | ユース ケースによって異なります                                       | すべての Common Data Service エンティティをサポートします           |

<sup>2</sup>Microsoft は、Common Data Service エンティティのデータ カバレッジの拡大に多額の投資を行っています。 カバレッジが利用可能な場合は、Common Data Service の使用をお勧めします。 現時点では、Common Data Service データ カバレージは、DMF および OData 対応エンティティと比較して低いです。

<sup>3</sup>SQL データベースにプログラムを使用してアクセスできます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]