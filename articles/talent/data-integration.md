---
title: Dynamics 365 Talent のデータ統合ガイド
description: このトピックでは、Dynamics 365 Talent で管理されているデータを統合するための各種オプションに関するガイドを提供します。
author: andreabichsel
manager: AnnBe
ms.date: 02/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: IT Pro
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: Talent January 2019 update
ms.openlocfilehash: c830685495e0ee30bc2e15f4ff1c4f4728258833
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251028"
---
# <a name="data-integration-guidance-for-dynamics-365-talent"></a>Dynamics 365 Talent のデータ統合ガイド

[!include[banner](../includes/banner.md)]


## <a name="overview"></a>概要
Dynamics 365 Talent は、さまざまな業務プロセスで役に立つ業務データを管理します。 このトピックでは、Talent で管理されるデータを統合するためのさまざまなオプションについてのガイドを提供し、インテグレーターが自分たちのニーズにどの技術が最も適しているかに関して十分な情報に基づいて判断ができるように、さまざまな統合テクノロジの特性について説明します。

## <a name="data-integration-vision"></a>データ統合のビジョン
Microsoft は、業務データを、会社を比類ないものにする重要な資産と見ています。 業務データは非常に重要です。 業務の 1 つの部分で収集および管理されているデータは、業務の別の部分で収集されたデータに関係し、これらの関係を使用して、組織全体の業務プロセスとビジネス インテリジェンスを向上させることができます。 どのシステムがデータを「所有する」かに関係なく、業務データへの容易で、セキュリティで保護され、安定したアクセスを提供することが、Talent によるデータ統合のビジョンの基本原則です。

これまで、複数のシステム間のデータの統合は困難でした。
Microsoft はデータ統合を容易にするための措置を講じており、その目標に向けた大きな一歩は [Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro) によって実現されます。
今後は、Talent では、Common Data Service が Talent データの推奨のパブリック インターフェイスになります。 時間の経過とともに、Talent によって管理されるもっとも重要なすべてのデータが Common Data Service で公開されると思っています。 ほとんどの統合アプリケーションにとって最適な技術として、Common Data Service をお勧めします。 アプリケーションが必要とするすべてのデータが現在 Common Data Service に必ずしも存在していないことを、またプロジェクトのスケジュールにより代替のテクノロジが要求されることを認識していますが、Common Data Service が統合のニーズを満たさないときはお知らせください。

## <a name="integration-technologies"></a>統合の技術
以下のセクションでは、Talent: Core HR で使用するために用意されているさまざまなデータ統合技術について説明します。

### <a name="common-data-service-entities"></a>Common Data Service エンティティ
Common Data Service は、Talent の推奨のパブリック データ インターフェイスです。 Common Data Service は、Dynamics 365 "XRM" から生まれた完成度の高いプラットフォームの上に構築されており、このプラットフォームの上に [Dynamics 365 Customer Engagement](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement) ソリューションが構築されています。

Common Data Service は、データ エンティティのためのプラットフォームと、これらのエンティティにアクセスするための API を提供します。 Talent が組織に配置されると、Talent は Common Data Service インスタンスに接続され、Talent データを維持するエンティティが Common Data Service インスタンスに配置され、これにより、Common Data Service インスタンスに接続できるすべてのアプリケーションがエンティティとそれらのデータを使用できるようになります。 使用する Talent アプリに基づいて、Talent は、Common Data Service エンティティに対してデータの操作を直接実行する (Attract と Onboard の場合) か、または Common Data Service エンティティとの間でデータを同期します (これは、Core HR の場合)。

統合アプリが必要とするデータを公開するデータ エンティティが Common Data Service に存在すると、[Common Data Service とサポートされる API](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer) を十分に活用することができます。
サポートされる API の 1 つに [Dynamics 365 Web API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api) があります。この API は、Common Data Service データにアクセスするための OData 実装を提供します。

Common Data Service エンティティおよび関連付けられている API は、Web アプリケーション、Web サービス/API から、また OData フィードに接続するその他のアプリケーションから、Talent データにアクセスするための最良のオプションです。

> [!NOTE]
> Common Data Service を Talent: Core HR の優先データインターフェイスにする決定が比較的新しい場合、統合に必要な Core HR データ エンティティを Common Data Service<sup>1</sup> で使用できない場合があります。 統合に必要な Core HR エンティティをまだ使用できない場合は、データ エンティティが利用できるまで待つか、または以下に示すその他の統合テクノロジのいずれかを使用する必要があります。

<sup>1</sup>Common Data Service で利用できる Core HR エンティティの一覧については、[Core HR および Common Data Service](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities) を参照してください。 Attract と Onboard については、すべてのエンティティが Common Data Service で利用可能です。

### <a name="dmfdixf-entities"></a>DMF/DIXF エンティティ
Finance and Operations applications と同じプラットフォーム上にもともと構築されている Core HR は、データ インポート エクスポート フレームワークまたは DIXF と呼ばれることもある、[データ管理フレームワーク (DMF)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json) と、Talent との間のデータのインポートまたはエクスポートのために使用できる一連のデータ エンティティを提供します。 Common Data Service エンティティは Talent の優先データ統合インターフェイスであり、DMF エンティティは次のような環境で有用です。

- Common Data Service エンティティをまだ利用できない。

- 統合に、高性能なバルク データ インポート/エクスポート機能が必要である。

現時点で、DMF エンティティは、Talent (Core HR) データに対してもっとも完全なデータ カバレージを提供します。

DMF はリアルタイム統合 (ユーザー インターフェイスでの即時のユーザーからのフィードバックが必要な場合など) には適切ではありません。その理由は、パッケージ操作はスケジュールされたバッチ ジョブであり、バッチ サービスで実行のためのジョブをピックアップするまでに最低 1 ～ 2 分の待ち時間が発生することがよくあり、そのほかに、インポート/エクスポート操作を完了するための時間が必要なためです。

DMF は、高スループット (夜間にスケジュールされている数千のレコードのインポート/エクスポートなど) が必要なときに最適なオプションになることがあります。

> [!NOTE]
> DMF は、Attract および Onboard には使用できません。

### <a name="dmf-package-rest-api"></a>DMF パッケージ REST API

DMF には、データ パッケージの操作のために [REST API](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api) が用意されています。 この API を使用して、プログラムで DMF と対話することで、次のような操作が可能になります。

- データ パッケージのインポート

- データ パッケージのエクスポート

- インポート/エクスポート操作のステータスの確認

DMF パッケージ REST API は Talent: Core HR で完全にサポートされています。

### <a name="azure-sql-db-byod"></a>Azure SQL DB (BYOD)

DMF はさらに、Talent でのユーザー独自の Microsoft Azure SQL データベースへのデータのエクスポートを可能にする、強力な機能 ([自分のデータベースの持ち込み](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database)、またはBYOD とも呼ばれます) を提供します。 これにより、データがユーザー所有の SQL データベースに存在する場合は、SQL データ ストアに接続できるアプリケーションやミドルウェアを利用できるので、驚異的な柔軟性が得られます。

BYOD は、通常、読み取り専用のソリューションと考えられています。 必要なデータを操作して Azure SQL データベース (データ マッシュ アップなど) に格納することができますが、Azure SQL データベースに格納されたデータは Talent: Core HR に逆同期されません。

BYOD は、[Azure Data Factory](https://docs.microsoft.com/azure/data-factory/) パイプラインのデータ ソースとして、ソリューション、データ統合、データ マッシュ アップを報告するために適しています。

> [!NOTE]
> BYOD は、Attract および Onboard には使用できません。

### <a name="odata-enabled-entities"></a>OData 対応エンティティ
ほとんどの DMF エンティティは、Talent データ サービス (OData) を使用したアクセスにも有効です。 [Finance and Operations OData サービス](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata) に対して用意されているドキュメントは、通常、Talent: Core HR にも適用されますが、ユーザー独自の OData を公開したエンティティの作成に関するドキュメントは適用されません。

Common Data Service および Common Data Service によって ([Dynamics 365 Web API](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8)) を通じて) 用意されている OData 実装は Talent データ サービスよりも優先されますが、現在のところ、Talent データ サービスは、Talent データに対してより完全なエンティティ カバレージを提供します。

### <a name="excel-add-in"></a>Excel アドイン

[Excel アドイン](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) は、内部にある OData 対応エンティティを利用します。 このアドインは、エンドユーザーが使い慣れた Excel UI を使用して Talent データを取得および変更するために便利な方法を説明します。

Excel アドインは、ビジネス ドメインの専門家による一時的なデータのインポート/エクスポートに適しています。 プログラムによる自動化を必要とする繰り返して発生するデータ統合の場合は、別の統合テクノロジがより適切です。

### <a name="data-integrator"></a>データ インテグレーター
Common Data Service 管理者経験により、Common Data Service との間のデータ統合に使用可能な[データ インテグレーター サービス](https://docs.microsoft.com/powerapps/administrator/data-integrator)が提供されます。 データ インテグレーターを使用して統合プロジェクトを定義することができます (多くの場合、アプリケーション開発者が特定の統合に合せて調整した定義済みのテンプレートに基づく)。 統合プロジェクトは、定期的なスケジュールで自動的に実行するようにスケジュールするか、または手動で実行することができます。

データ インテグレーター プロジェクトは Common Data Service バッチ統合に適しており、アプリケーションの Dynamics 365 ファミリ間の統合のために素晴らしい選択をします。 たとえば、Microsoft は、Core HR からのデータを Dynamics 365 Finance に統合するために使用できる、追加設定のないデータ インテグレーター テンプレートを提供します。 詳細については、[Dynamics 365 Talent から Dynamics 365 Finance への統合](talent-financeandoperations-integration.md) を参照してください。

### <a name="power-query"></a>Power Query

データ インテグレーターは、[Power Query](https://docs.microsoft.com/power-query/power-query-what-is-power-query) もサポートしています (その [高度なクエリ機能](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering) を通じて)。
Power Query は、リッチな M formula language を含む、強力で柔軟なデータのフィルタリングと変換を提供し、Power BI レポートの作成に経験のあるユーザーには親しみやすいと思われます。

## <a name="deciding-on-an-integration-technology"></a>統合テクノロジの決定
非常に多くのさまざまな統合テクノロジが使用可能な場合、使用する統合方法を決定することに困惑することがあります。 時間とともに、特に Common Data Service でのデータ カバレージが完全になるに伴って、ほとんどの場合、Common Data Service が優先データ インターフェイスとなり、その決定は簡単になります。 しかし、それまでは、Common Data Service がユーザーのニーズを満たさないことがあります。 次の表は、さまざまな統合テクノロジのオプションのいくつかの主要な特性を要約するのに役立ちます。

| テクノロジ/ツール/API    | 定期統合                   | 同期/非同期                    | API によるプログラム アクセス        | 適切なデータ量                                   | データ カバレージ                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Common Data Service エンティティ           | データ インテグレーターまたはミドルウェアを使用します | 同期、非同期、バッチ (データ インテグレーターを使用) | Dynamics 365 Web API (OData) を使用 | ユース ケースによって異なります (対話型の使用に対してページングをサポート) | 改善<sup>2</sup>                       |
| DMF エンティティ           | ミドルウェアを使用してスケジュール        | 非同期、バッチ                                | DMF パッケージ REST API を使用         | 高 (数十万のレコード)                    | 高                                |
| DMF パッケージ REST API   | ミドルウェアを使用してスケジュール        | 非同期、バッチ                                | 有                                       | 高 (数十万のレコード)                    | API はすべての DMF エンティティをサポートします       |
| BYOD                   | 管理者による Talent でのスケジュール        | 非同期、バッチ                                | いいえ<sup>3</sup>                                    | 高 (数十万のレコード)                    | すべての DMF エンティティをサポートします           |
| OData 対応エンティティ | ミドルウェアを使用                    | 同期                                        | Talent データ サービス (OData) を通じて  | ユース ケースによって異なります (対話型の使用に対してページングをサポート) | 高                                |
| Excel アドイン           | 無                                       | 同期                                        | 無                                        | 中間 (数十万のレコード)                      | すべての OData 対応エンティティをサポートします |
| データ インテグレーター        | データ インテグレーターでスケジュール        | 非同期、バッチ                                | いいえ                                        | ユース ケースによって異なります                                       | すべての Common Data Service エンティティをサポートします           |

<sup>2</sup>Microsoft は、Common Data Service エンティティのデータ カバレージの増加に重点を置いて投資しており、カバレージが得られるとき、Common Data Service を優先データ インターフェイスとして推奨します。 現時点では、Common Data Service データ カバレージは、DMF および OData 対応エンティティと比較すると低いです。

<sup>3</sup>SQL データベースにプログラムを使用してアクセスできます。

## <a name="summary"></a>集計
業務データは重要な資産ですが、特定の目的 (レポート、データ マッシュ アップ、またはカスタム アプリケーションなど) にデータを使用することが困難な場合、その価値は大幅に減少する可能性があります。 Dynamics 365 Talent は、Talent アプリケーションのユーザー インターフェイス (UI) の外部にあるデータを操作するための複数のテクノロジを提供して、そのデータへの統合アプリケーション アクセスを可能にします。 このトピックでは、使用可能な統合テクノロジとその主要な特性の一部について説明しました。
この情報は、統合プロジェクトに活用する方法に対してより良い決定するのに役立ちます。




