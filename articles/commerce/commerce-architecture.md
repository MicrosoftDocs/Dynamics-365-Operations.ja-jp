---
title: Dynamics 365 Commerce アーキテクチャの概要
description: この記事では、Microsoft Dynamics 365 Commerce エコシステム内すべてのコンポーネントの概要を示します。これには、Dynamics 365 製品スイートへの統合ポイントなどが含まれます。
author: samjarawan
ms.date: 09/15/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.11
ms.assetid: ''
ms.search.industry: Retail
ms.search.form: RetailITWorkspace
ms.openlocfilehash: 14ef158d157487f03a2c623157ae4b5ddeb0502c
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740426"
---
# <a name="dynamics-365-commerce-architecture-overview"></a>Dynamics 365 Commerce アーキテクチャの概要

[!include [banner](includes/banner.md)]



この記事では、Microsoft Dynamics 365 Commerce エコシステム内すべてのコンポーネントの概要を示します。これには、Dynamics 365 製品スイートへの統合ポイントなどが含まれます。 

次の図は、Dynamics 365 Commerce コンポーネントの概要を示します。

![Dynamics 365 Commerce コンポーネントの概要](./media/Commerce_Architecture_Component_Overview.png)

## <a name="architecture-benefits"></a>アーキテクチャのメリット

### <a name="omni-enabled-headless-commerce-engine"></a>全方向性が有効なヘッドレス コマース エンジン

Commerce Scale Unit は、ヘッドレス コマース エンジンをホストします。 すべての商取引ビジネス ロジックの中心統合ポイントとなり、物理ストアとデジタル ストアを横断した完全な指向性チャネル ソリューションを提供します。 Commerce Scale Unit は、ポータブルなアーキテクチャを使用して構築されており、クラウド、エッジ、ハイブリッドのトポロジにわたって柔軟なホスティング オプションを実現します。 

ヘッドレス コマース エンジンは、店舗内および e コマースのチャネルを含め、すべてのネイティブ Dynamics 365 Commerce チャネルの能力を強化します。 また、サードパーティ製チャネル ソリューションの単一の統合ポイントとして機能します。 そのため、これらのソリューションでは、マイクロソフトや独立系ソフトウェア ベンダー（ISV）が提供する Dynamics 365 Commerce ビジネス ロジックや他のコマース関連サービスとの統合をすることができます。

### <a name="interconnected-business-processes"></a>相互接続された業務プロセス

Dynamics 365 Commerce、Dynamics 365 Supply Chain Management、Dynamics 365 Finance のような様々な Dynamics 365 業務アプリケーションの間で共有されているプラットフォームは、ユーザーがすぐに恩恵を受けることができる相互に接続された一連の業務プロセスを提供しています。 これらのアプリケーションのバックオフィス機能はすべて、同じウェブ エクスペリエンスとデータストア上に構築されています。 そのため、組織内の様々な機能にまたがる業務プロセスのシームレスフローが発生しますが、アプリケーションやサービス間のカスタム統合は必要ありません。 ヘッドレス コマース エンジンとバックオフィスの統合により、バックオフィスとコマース チャネルで相互に接続された業務プロセスの適用範囲がさらに広がります。

### <a name="unified-data"></a>統合されたデータ

Dynamics 365 Commerce は、[Microsoft Dataverse](https://powerplatform.microsoft.com/dataverse/) および [Azure Data Lake Storage](/azure/storage/blobs/data-lake-storage-introduction) と標準で統合された、統合データ ソリューションを提供します。 Dynamics 365 Sales や Dynamics 365 Marketing などの Dynamics 365 アプリ間の統合やデータ共有は、Microsoft Dataverse を介してサポートされています。 Azure Data Lake Storage のトランザクショ データは、さまざまな統合を使用して分析や分析情報のシナリオを強化するために使用されます。

### <a name="powered-by-ai-and-analytics"></a>AI と Analytics を搭載

Data Lake Storage には、アクセス可能で、永続性があり、最新かつ統一された組織データを利用できるため、組織全体が Analytics、人工知能（AI）、機械学習（ML）を上から適用できる 「単一の真実のソース」 を手に入れることができます。 このようにして、組織は分析情報を導き出し、すべてのチャネルで業務プロセスを最適化し、自動化するために使用できる主要なパフォーマンス指標（KPI）を取得することができます。

#### <a name="business-and-transactional-analytical-reports-in-pos-and-commerce-headquarters"></a>POS および Commerce headquarters のビジネスとトランザクションの分析レポート

Commerce で事前にパッケージ化された一連のビジネスとトランザクションの分析レポートは、Store Commerce 販売時点管理 (POS) システムおよび Commerce headquarters に high-charts と SSRS ベースのレポートを組み込むことで、小売業者に Commerce エコシステムのすべてのポイントにおいて Intelligent Insights を提供します。 コマース分析ソリューションは、すぐに利用できるビジネスとトランザクションのレポートの包括的なセットを提供し、小売業者がすべてのチャネルで分析情報を活用できるようになります。

POS の highcharts ベースのレポートはリアルタイムであり、店舗の関係者がトランザクションの完了時にチャネルのトランザクションおよびその他の POS 活動を分析できるようになります。 これは、Commerce headquarters のすぐに使用できるレポートとは対照的で、小売業者はデータが同期されると、すべてのチャネルでトランザクション活動に関する分析レポートを表示できます。 Commerce headquarters レポートは、販売実績に焦点を当ててトレンドを予測し、分析情報を明らかにするチャネル マネージャーために特別に設計されており、組織全体の販売実績に関するレポートを従業員、カテゴリ、製品、ターミナル、チャネルなど、グローバルな地域で掘り下げることができます。

## <a name="component-overview"></a>コンポーネントの概要

### <a name="user-experiences"></a>ユーザー エクスペリエンス

#### <a name="dynamics-365"></a>Dynamics 365

Dynamics 365は、中規模から大規模なビジネス向けの包括的で柔軟性のあるエンタープライズ リソース プランニング (ERP) ソリューションを提供するアプリケーションを集めたものです。 これにより、多数のパートナーを通じて顧客固有の要件に合った拡張可能なフレームワークとエコシステムが提供されます。 Dynamics 365 アプリケーションには、対象となる業務セグメントの機能を用意しています。 また、互いの強みを活かし、Microsoft の他のサービスや提供機能を活用して、顧客の複雑なビジネスの運営を支援するソリューションを提供しています。

#### <a name="pos"></a>POS

POS では、新たなチャンネルのオムニチャンネル ソルーションを提供することにより、小売業者の操作が簡略化されます。 これらのチャンネルは、現金売りトランザクション、現金/シフト管理、顧客契約、支援販売、クライアントリング、エンドレス アイル、注文処理/フルフィルメント、在庫管理、レポートなどの様々なコマース ビジネスを実行します。

#### <a name="modern-pos"></a>Modern POS

モダン POSは、レジ担当者、販売員、在庫担当者、店長など、すべての店舗内の第一線で働く人が使用する、クロス プラットフォーム（Windows、iOS、Android）、マルチフ ォーム ファクタ（デスクトップ、タブレット、電話）のソリューションです。 オフライン機能を持つアプリとして配置できます。 また、クラウドに配置して、Web ブラウザーを使用してアクセスすることもできます。 アプリケーションはロールに基づいており、本社から完全な構成を行うことができます。 また、カスタマイズ性も高く、リテール ソフトウェア開発キット（SDK）を使用することで、サードパーティのサービスに拡張または統合することができます。

モダン POSには、標準的な「キャッシュ アンド キャリー」のトランザクション処理に加えて、アシスト販売、クライエンテリング、エンドレス アイル、注文処理/フルフィルメント、在庫管理、キャッシュ/シフト管理、レポート作成機能が搭載されています。 詳細については、[モダンPOS (MPOS) アーキテクチャ](./dev-itpro/retail-modern-pos-architecture.md) と [モダン POS (MPOS) とクラウド POSを選択する](./mpos-or-cpos.md) を参照してください。

#### <a name="e-commerce-storefront"></a>E コマース ウェブストア

e コマース ウェブストアは、顧客向けの web サイト レンダリング システムです。 React.js フレームワークをベースに構築されており、サーバー サイドとクライアント サイドのレンダリングを組み合わせて使用し、1 つ以上のオンライン チャンネルに対して応答性の高い web エクスペリエンスを提供します。 ウェブストアには標準で使用できる機能のセットが豊富に用意されていますが、この機能は高度なカスタマイズが可能で、オンライン ビジネス向けの効率的でスケーラブルなソリューションを提供します。 詳細については、[オンライン ストアの概要](./online-store-overview.md) を参照してください。

#### <a name="site-builder"></a>サイト ビルダー

サイト ビルダーは、コンテンツ管理および店舗内の Web サイト レンダリング システムに web ベースのオーサリング インタフェースとして使用されます。 e コマースのエクスペリエンスに関するマーケティング コンテンツの管理と作成を、日常的なワークフロー タスクとして実行するサイト管理者とコンテンツ制作者のために、サイト ビルダーのビジュアル ページ ビルダーは、目的に適したコンテンツ (WYSIWYG) エディターを提供します。 サイト ビルダーでは、特定の製品に対してより多くのマーケティング詳細を提供し、顧客に対する買い物の利便性を高めることができます。 さらに、サイト ビルダーには、アクセシビリティ レポート、URL管理、サイトマップ生成、画像の焦点管理などの機能が統合されています。 詳細については、[オンライン ストアの概要](./online-store-overview.md) を参照してください。

#### <a name="external-services-and-apps"></a>外部サービスとアプリ

Commerce Scale Unit を介して公開されるヘッドレス コマース エンジンにより、パートナーや顧客は、標準で実装されている e コマースや POS（Point of Sale）コンポーネントで使用されているのと同じチャネル サイドの機能やビジネス ロジックをすべて利用することができます。 そのため、同じデータと業務プロセス機能を連携させることで、標準で実装されているチャネル コンポーネントや、パートナーが提供する/顧客が開発したサービスやアプリケーションを横断して、シームレスなオムニチャネル機能を実現します。 また、Commerce Scale Unit を通じて利用可能な、標準または ISVが開発したすべてのサラウンド サービスへのアクセスを提供します。

### <a name="back-office"></a>バック オフィス

#### <a name="dynamics-365-commerce-headquarters"></a>Dynamics 365 Commerce 本部

この Dynamics 365 Commerce アプリケーションは、コマース 本部 コンポーネントと呼ばれることが多く、業務に必要な製品、従業員、業務プロセス、およびその他の機能の構成を可能とするバックオフィス機能を提供します。 また、コールセンターの作業者がコマース関連のワークフローを支援するために使用するアプリケーションでもあります。

#### <a name="dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management

[Dynamics 365 Supply Chain Management](https://dynamics.microsoft.com/supply-chain-management/overview/)は、生産から在庫、倉庫、輸送、流通に至るまで、サプライチェーンのライフサイクル全体を通して製品を管理する機能を提供しています。 詳細については、 [Supply Chain Management に関するヘルプ リソース](../supply-chain/index.md) を参照してください。

#### <a name="dynamics-365-finance"></a>Dynamics 365 Finance

[Dynamics 365 Finance](https://dynamics.microsoft.com/finance/overview/) には、グローバルな財務を自動的に管理する機能が用意されています。 Dynamics 365 Commerce アプリケーションを利用している顧客に対し、Dynamics 365 Finance は、店舗や e コマースの財務諸表を他の業務と並行して管理する統合されたエクスペリエンスを提供しています。 詳細については、[Dynamics 365 Finance のヘルプ リソース](../finance/index.md)を参照してください。

#### <a name="dynamics-365-human-resources"></a>Dynamics 365 Human Resources

[Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/)では、企業が従業員のリソースを総合的に把握し、統一された方法で管理することができます。 採用プロセスから人材の計画や社員の時間管理まで、統合された経験を提供します。 詳細については、[Dynamics 365 Human Resources のヘルプ リソース](./index.md) を参照してください。

### <a name="commerce-scale-unit"></a>コマース スケール ユニット

小売業は分散型組織であり、業務の概略をハブ＆スポークモデルで表現することができます。 Dynamics 365 Commerce はこのモデルに対応しています。本部の機能（ハブ）と、多数の分散型チャネル コンポーネント（スポーク）を持ち、店舗内や近くのMicrosoftが管理している Azure データセンターに展開して自己管理することができます。 スポークは、物理的な分離 (スケールの関数) と 1 つの更新の原子単位を表すため、スケール単位と呼ばれています。

クラウドやエッジ コンピューティングのシナリオを容易にするために、Commerce Scale Unit は、Microsoft が管理する SaaS (Software as a Service) コンポーネント (クラウドの Commerce Scale Unit) と、ローカルで配置できる自己管理型コンポーネント (自己ホスト) のどちらでも利用できます。 単一の環境には、Commerce Scale Unit (クラウドと自己ホスト) を混在させることができます。 そのため、ネットワークの冗長性を導入して接続性を向上させることで、店舗ごとに運用上の間接費への投資を調整することができます。 詳細については、[店舗内トポロジーの選択](./dev-itpro/retail-in-store-topology.md) を参照してください。

#### <a name="commerce-scale-units-cloud"></a>Commerce Scale Unit (クラウド)

それぞれの環境には、複数の Commerce Scale Unit を関連付けることができます。 それぞれの Commerce Scale Unit は、独立してサービスを提供、更新することができ、各スケールユニットは、1 つまたは複数の法人にまたがる 1 つまたは複数のチャネルにサービスを提供することができます。 各 Commerce Scale Unit は、対応するすべての Azure の地域に配置できます。また、複数の Commerce Scale Unit を同じ地域に配置することもできます。 各 Commerce Scale Unit は独立しているため、チャンネルの集合に対して更新を段階的にロールアウトできます。

#### <a name="commerce-scale-units-self-hosted"></a>Commerce Scale Unit (自己ホスト)

Commerce Scale Unit をエッジ コンピューティングにすることにより、インターネットの接続性が悪い場合た不安定になる場合にも対応できます。 このアプローチは多くの小売業者にとって、店舗に物理的な足跡を残すことを意味します。 Commerce Scale Unit (自己ホスト) を使用することで、小売業者は、Azure クラウド上で実行されるのと同じ業務ロジックと機能を店舗に取り込むことができます。 このような場合、店舗内接続の方が信頼性は高くなりますが、これらコンポーネントの自己管理には、監視と更新の点で追加の間接費が必要になります。 詳細については、[店舗内トポロジーの選択](./dev-itpro/retail-in-store-topology.md) を参照してください。

### <a name="e-commerce-platform"></a>E コマースのプラットフォーム

#### <a name="content-management-system"></a>コンテンツ管理システム

完全な機能を備えたコンテンツ管理システム（CMS）は、 e コマース プラットフォームに直接統合されています。 豊富なインデックス機能に加え、、CMSには、ヘッドレス コマース エンジンによって管理される製品情報を補うマーケティング資料が用意されています。 これには、ローカライズ機能や、リリースを通じて複数項目を公開する機能が含まれています。 システムは、Azure Active Directory (Azure AD) と Azure Cosmos DB を含むスケーラブルで弾力性のある Azure インフラストラクチャの上に構築されています。

#### <a name="digital-asset-management"></a>デジタル資産管理

コマース デジタル資産管理は、コンテンツ管理ストアを拡張し、ウェブストアで提供される画像、動画、ファイルのダウンロードを追跡します。 画像のリサイズ サービスは、ダウンロードした画像をさまざまなデバイスやコンテキストに合わせて最適化します。 このようにして、画質を管理しながらパフォーマンスも向上させることができます。 また、デジタル資産管理も Azure Media Services と統合されており、ビデオストリームの効率的な再生を実現します。

#### <a name="web-storefront"></a>ウェブストア

CMS では、自身のページを一連のモジュールとして格納しています。 ウェブストアの Web サーバーは、これらモジュールをレンダリングされた HTML ページにまとめます。 ウェブストアは、レンダリング プラットフォーム、コマース データ プロキシ、機能拡張層で構成されています。 これらのコンポーネントは、Web ベースのコマース体験を実現するモジュールのセットである、Dynamics 365 Commerce モジュール ライブラリによって補完されるベースを形成しています。 初期モジュール ライブラリは、各業務固有の要件に合わせて変更することができます。 または、パートナーが開発した拡張機能やモジュールで補完することも可能です。

### <a name="commerce-surround-services"></a>コマースに関連するサービス

#### <a name="dynamics-365-fraud-protection"></a>Dynamics 365 Fraud Protection

[Dynamics 365 Fraud Protection](/dynamics365/fraud-protection/overview)は、Commerce Scale Unit を介して管理、処理される e コマースのチェックアウト フローに統合されます。 本サービスへの接続は、Commerce Scale Unit で自動的にプロビジョニングされ、Dynamics 365 Fraud Protection に登録した顧客はコマース本部で統合の有効化と設定を行うことができます。 このサービスは、サービスの有効性を評価する 「評価」 モードと、構成された業務ルールを使用して不正なトランザクションを検出する 「保護」 モードのいずれかで実行することができます。 詳細については、 [Dynamics 365 Commerce を使用した Dynamics 365 Fraud Protection の統合](./dev-itpro/dfp.md) を参照してください。

#### <a name="dynamics-365-customer-insights"></a>Dynamics 365 Customer Insights

[Dynamics 365 Customer Insights](/ai/customer-insights/overview) は、さまざまなトランザクション、行動、観察の各ソースのデータを接続して、360 度の顧客ビューを作成し、分析情報を生成することで、顧客に対する理解を深めることができます。 Dynamics 365 Commerce を使用することで、小売業者は Dynamics 365 Customer Insights との統合を容易に有効化し、POS で生成された分析情報を表示することができます。 これらの分析情報には、顧客離れ率や次に取るべき最良の策が含まれており、販売担当者が顧客と効果的な会話に行い、顧客にパーソナライズされたショッピング体験を提供するのに役立つため、価値のあるものとなっています。 詳細については、 [Dynamics 365 Commerce を使用した Dynamics 365 Customer Insights の統合](./clienteling-overview.md#integration-with-dynamics-365-customer-insights) を参照してください。

#### <a name="azure-cognitive-search"></a>Azure Cognitive Search

[Azure Cognitive Search](/azure/search/search-what-is-azure-search) は Commerce に統合されており、Commerce Scale Unit (CSU) を使用するすべての Commerce チャネルで一貫した製品検出と検索のエクスペリエンスを提供します。 統合された Azure Cognitive Search を使用すると、顧客はカテゴリの参照、検索、フィルター処理によって、製品をすばやく見つけるけることができます。 製品発見機能の向上は、小売業者が顧客の維持率と転換率を高めるのに役立ちます。 また、Azure Cognitive Search は、eコマースのトラフィックに必要なスケーラビリティとパフォーマンスも提供します。 詳細については [クラウドを利用した検索の概要](./cloud-powered-search-overview.md) の記事を参照してください。

#### <a name="product-recommendations"></a>製品推奨事項

Dynamics 365 Commerce は、e コマース サイトや POS デバイス上で商品のおすすめ表示に使用することができます。 これらのおすすめ商品は、顧客が興味を持ちそうな商品であり、オンラインや実店舗での他の顧客の購入動向に基づいています。

製品の推奨により、顧客は購入したい製品を簡単かつ迅速に見つけることができます。また、クロスセルとアップセルを使用して、顧客が購入する予定のなかった製品を追加で見つけることができます。 製品の検出のために推奨機能を使用した場合、より多くの変換の機会を創出し、販売収益を増加させ、顧客満足度と定着率を高めるのに役立ちます。 詳細については、[製品推奨事項の概要](./product-recommendations.md) を参照してください。


#### <a name="ratings-and-reviews"></a>評価とレビュー

コマースの評価およびレビュー ソリューションでは、オンライン ストアの顧客が E コマース ストアで商品のレビューや評価を入力することができます。 小売業者は、eコマース サイト全体で平均化された評価とレビュー情報を表示することができます。 Azure Cognitive Services は、40 にわたる言語での冒涜的な言葉の自動修正を提供しており、人間の承認が不要なため、修正コストが削減されます。 また、システムは、顧客の懸念事項、フィードバック、および要求の取り下げに応答し、ユーザーからのデータ要求処理を行うために使用できるモデレーター ツールも提供します。 詳細については、[評価とレビューの概要](./ratings-reviews-overview.md) を参照してください。

### <a name="unified-data-components"></a>統合されたデータコンポーネント

#### <a name="azure-data-lake-storage"></a>Azure Data Lake Storage

自身の Azure Data Lake Storage アカウントを持っている顧客は、バックオフィス業務の構造化されたビジネスデータや、E コマース のクリック ストリームデータを活用することができます。 このデータは、製品の推奨、顧客の分析情報、コマース分析などのインテリジェンス サービスに戻され、顧客中心の業務プロセスやユーザー エクスペリエンスを強化します。 これらの業務プロセスとユーザー エクスペリエンスは、 Dynamics 365 Commerce 本部、POS、E コマースのウェブサイトに再び組み込むことができます。 詳細については、[エンティティストアを Data Lake として利用する](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md) を参照してください。

#### <a name="dataverse"></a>Dataverse

Dataverse は、すべての業務アプリケーションのデータを統合する統合データ ストアです。 Dynamics 365 Sales、Dynamics 365 Customer Service、 Dynamics 365 Commerce などの Dynamics 365 アプリケーションは Dataverse を使って業務データを保存しています。 そのため、Dataverse は業務横断的なアプリケーション シナリオを可能にし、Power Apps や Power Automate を介して新たなシナリオを強化することができます。 詳細については、[Microsoft Dataverse とは?](/powerapps/maker/common-data-service/data-platform-intro) を参照してください。

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce 認証フロー](arch-auth-flow.md)

[Azure Data Lake Storage](/azure/storage/blobs/data-lake-storage-introduction)

[Microsoft Dataverse](https://powerplatform.microsoft.com/dataverse/)

[Modern POS (MPOS) アーキテクチャ](./dev-itpro/retail-modern-pos-architecture.md)

[Dynamics 365 Supply Chain Management](https://dynamics.microsoft.com/supply-chain-management/overview/)

[Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/)

[Dynamics 365 Finance](https://dynamics.microsoft.com/finance/overview/)

[Dynamics 365 Fraud Protection](/dynamics365/fraud-protection/overview)

[Dynamics 365 Commerce と Dynamics 365 Fraud Protection の統合](./dev-itpro/dfp.md)

[Dynamics 365 Customer Insights](/dynamics365/ai/customer-insights/overview)

[Azure Cognitive Search](/azure/search/search-what-is-azure-search)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
