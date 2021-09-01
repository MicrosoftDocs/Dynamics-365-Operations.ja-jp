---
title: 二重書き込み FAQ
description: このトピックでは、二重書き込みについてよく寄せられる質問に回答します。
author: robinarh
ms.date: 07/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 21311
ms.assetid: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-07-21
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d313597a1e421a635990f0413a32237ffd25156341bca240ec400687b77f884b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726225"
---
# <a name="dual-write-faq"></a>二重書き込み FAQ

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、二重書き込みに関してよく寄せられる質問を取り上げ、必要な情報をすぐ得られるように簡単な回答を示します。

## <a name="dual-write-setup"></a>二重書き込みの設定

### <a name="do-you-plan-to-enable-dual-write-to-use-dataverse-as-a-hub-between-multiple-finance-and-operations-environments-if-dataverse-is-used-as-a-hub-data-can-be-synced-between-two-or-more-finance-and-operations-environments"></a>Dataverse を、複数の Finance and Operations 環境間でハブとして使用できるように二重書き込みを有効にする予定はありますか? Dataverse をハブとして使用すれば、2 つ以上の Finance and Operations 環境間でデータを同期することができます。

行の扱いに関する現在のプランでは、二重書き込みを単一の Finance and Operations 環境および単一の Dataverse 環境との間の 1 対 1 (1:1) のマッピングに制限しています。

### <a name="can-i-control-the-sequencing-of-maps-in-dual-write-as-i-can-in-data-integrator"></a>データ インテグレーターのように、二重書き込みでマッピングの順序をコントロールすることはできますか?

二重書き込みはトランザクション ベースです。 たとえば、Finance and Operations アプリの変更より、Dataverse で複数のマップの同期が実行される場合、既定では、それらの変更はデータベースで更新される順序で行われます。 このパターンは、最初の同期のコンテキストでは、より有意義なものです。 システムによって、関連するテーブル マップが指定された順序で提供されますが、環境に適したものにするよう、一覧の順序を変更することができます。

### <a name="do-application-users-require-any-special-permissions-to-enable-or-configure-dual-write"></a>アプリケーション ユーザーは、二重書き込みを有効にしたり構成したりするために特別なアクセス許可を必要としていますか?

Finance and Operations 環境に対して 2 つ の Azure Active Directory (Azure AD) アプリケーションが設定され、Dataverse 環境で 2 つのアプリケーション ユーザーが設定されている必要があります。 これらのアプリケーション ユーザーには、適切なアプリケーション ID を含める必要があります。 正常に接続されるようにするため、アプリケーションに、セキュリティ ロールを使用して関連するテーブル アクセス許可を付与する必要があります。 詳細については、[要件を確認してアクセスを許可する](requirements-and-prerequisites.md#verify-requirements-and-grant-access) を参照してください。

### <a name="do-end-users-require-any-special-permissions-to-enable-or-configure-dual-write"></a>エンド ユーザーは、二重書き込みを有効にしたり構成したりするために特別なアクセス許可を必要としていますか?

二重書き込みマッピングの構成を行っているエンド ユーザーは、Dataverse および Finance and Operations の両方の環境でシステム管理者セキュリティ ロールが割り当てられている必要があります。

すべてのユーザーおよび環境が単一テナントに属し、ユーザーが必要なセキュリティおよびライセンスの割り当てを所有している限り、複数のユーザーが二重書き込みマッピングにアクセスできます。

### <a name="i-have-multiple-legal-entities-some-of-my-maps-are-legal-tablespecific-or-valid-for-only-some-of-the-legal-entities-what-is-the-best-way-to-address-this-requirement-can-i-apply-a-filter-such-as-company--usmf-to-address-it"></a>複数の法人を担当しています。 扱っているマップの中には、リーガル テーブルに特化しているもの、または一部の法人に対してのみ有効というものがあります。 この要件に対応する最善の方法は何でしょうか? Company = USMF などのフィルタを適用して対応することはできますか?

Dataverse 環境がリンクされているなら、リーガル テーブル マッピングを行うことができます。 特定の法人にテーブル マップをマップすることはできません。

### <a name="if-dual-write-solutions-are-installed-in-dataverse-can-i-uninstall-them"></a>Dataverse に二重書き込みソリューションがインストールされている場合、アンインストールすることはできますか?

二重書き込みソリューションは、アンインストール可能なマネージド ソリューションです。 ただし、マネージド ソリューションをアンインストールすると、ソリューション内のすべてのコンポーネントが削除されます。 コンポーネントに格納されているデータも削除されます。 詳細については、[管理ソリューションの保守](/powerapps/developer/common-data-service/maintain-managed-solutions) を参照してください。

### <a name="i-have-data-in-both-a-customer-engagement-app-and-a-finance-and-operations-app-and-i-bootstrap-my-existing-data-in-the-customer-engagement-app-if-my-data-isnt-currently-aligned-can-i-specify-a-master-source-for-the-initialization-run-so-that-all-differences-are-applied-to-the-target"></a>Customer Engagement アプリと Finance and Operations アプリの両方にデータを保持しており、Customer Engagement アプリで既存のデータをブートストラップしています。 現在データが配置されていない場合は、初期化実行でマスタ ソースを指定して、すべての差異がターゲットに適用されるようにすることができますか?

ブートストラップが完了したら、差異を適用してマスタを選択するように、初期同期の設定を構成することができます。 ブートストラップの詳細については、[社内データを含むブートストラップに関するよく寄せられる質問](bootstrap-company-data.md) を参照してください。 初期同期の詳細については、[テーブル マップの二重書き込みの有効化](enable-entity-map.md) を参照してください。

## <a name="dual-write-administration-and-management"></a>二重書き込みの管理

### <a name="what-is-the-purpose-of-the-integration-key-and-is-it-mandatory"></a>統合キーの目的は何ですか。これは必須ですか?

統合キーは、行を一意に識別するナチュラル キーです。 統合キーは、Dataverse テーブルに対してのみ必要です。 二重書き込みで統合キーを手動作成できます。 テーブルに対して代替キーが既に提供されている場合は、テーブルの代替キーから自動的に統合キーを作成することもできます。 統合キーは、代替キーと同じ目的で使用されます。これにより、データを外部システムと統合するための効率的かつ正確な方法が提供されます。 統合キーは、Dataverse の行を一意に識別するグローバル一意識別子 (GUID) が外部システムに格納されていない場合に必須です。

二重書き込みでは、統合キーを使用して、固有の組み合わせを表す 1 つ以上のテーブル列の値を使用して、行を一意に識別します。 たとえば、統合キーを使用して勘定行を識別するには、勘定番号列を使用できます。 別の方法として、勘定番号列を、変更すべきではない値を持つ他の列と共に使用することもできます。 詳細については、[Power Apps ポータルを使用した代替キーの定義](/powerapps/maker/common-data-service/define-alternate-keys-portal) を参照してください。

キーが Finance and Operations 環境と Dataverse 環境との間で一致していることは重要です。 そうでない場合、初期同期フェーズで問題が発生する可能性があります。

### <a name="how-do-i-move-table-maps-between-environments-is-version-control-supported-for-table-maps"></a>環境間でテーブル マップを移動するにはどうすればよいですか? テーブル マップではバージョン管理がサポートされていますか?

マップをエクスポートして、別の環境にインポートすることができます。 Azure DevOps を使用してプロセスを自動化することができます。 マッピングはソリューションに対応しているコンポーネントなので、二重書き込みマッピングに対してバージョン管理を行うことができます。 詳細については、[テーブル マップを更新し、ソリューションとして他の環境にエクスポートする](app-lifecycle-management.md#update-table-maps) を参照してください。

### <a name="where-can-i-find-examples-and-patterns-for-filtering-dual-write-maps"></a>二重書き込みマップをフィルタリングするための例とパターンはどこにありますか?

基本的なフィルタ処理の例については、[データのフィルター処理](customizing-mappings.md#filter-your-data) を参照してください。

Dataverse での詳細な例については、[結果のフィルター](/powerapps/developer/common-data-service/webapi/query-data-web-api#filter-results) を参照してください。 二重書き込みソースフィルターでは、ネストしたルックアップはサポートされません。 テーブル列に対して直接、[標準のフィルタ演算子](/powerapps/developer/common-data-service/webapi/query-data-web-api#standard-filter-operators)のみがサポートされています。

Finance and Operations のフィルターの詳細については、[クエリ範囲での式の使用](/dynamicsax-2012/developer/using-expressions-in-query-ranges)、および[高度なフィルター処理とクエリ構文](../../../fin-ops/get-started/advanced-filtering-query-options.md) を参照してください。

### <a name="dual-write-live-synchronization-introduces-tight-coupling-across-applications-what-happens-if-one-side-fails-will-the-other-side-fail-too"></a>二重書き込みライブ同期では、アプリケーション間に緊密な結合が導入されます。 1 つの側に障害が発生した場合はどうなりますか? 他方の側でも障害が発生するでしょうか?

統合がライブ同期モードの場合、いずれかのアプリケーションで同期が失敗すると、他のアプリケーションも失敗し、ユーザーにエラーが表示されます。 統合が一時停止すると、変更がステージングされます。 その後、ターゲット システムが起動して実行されるときに、これらが書き込まれます。 統合を自動的に一時停止する方法の詳細については、[警告の通知](errors-and-alerts.md#alert-notifications) を参照してください

### <a name="when-live-synchronization-is-paused-and-then-resumed-does-it-follow-the-sequence-of-changes-for-example-if-the-name-column-in-the-finance-and-operations-app-is-changed-from-namea-to-nameb-to-namec-is-customer-engagement-data-changed-from-namea-to-nameb-to-namec-or-is-it-changed-directly-from-namea-to-namec"></a>ライブ同期が一時停止後に再開された場合、変更の順序に従いますか? たとえば、Finance and Operations アプリの名前列が NameA から NameB、次いで NameC に変更された場合、Customer Engagement のデータは NameA から NameB、次いで NameC に変更されますか? それとも、NameA から NameC に直接変更されますか?

統合は、変更の順序を完全に反映します。 この例では、Customer Engagement アプリのデータは、**NameA** から **NameB** に、次いで、**NameC** に変更されます。

### <a name="how-do-i-handle-a-finance-and-operations-database-transfer-from-prod-to-stage-what-is-the-effect-on-dual-write-after-the-transfer-the-systems-are-no-longer-in-sync-is-the-synchronization-done-automatically"></a>PROD から STAGE への Finance and Operations データベースの転送をどのように処理したらよいですか? 二重書き込みはどんな影響がありますか? 転送後、システムの同期は解除されますが、同期は自動的に行われますか?

リンクされた各環境ペア (Finance and Operations アプリ環境と Dataverse 環境) は、単一の単位として処理され、それに応じて更新される必要があります。 たとえば、実稼働環境からサンドボックスを更新する場合、Finance and Operations アプリのサンドボックス環境と Dataverse のサンドボックス環境の両方を、それに対応する実稼働環境から更新する必要があります。 二重書き込みがターゲット環境で既に使用されている場合は、それらの環境のリンクを解除する必要があります。 ターゲット環境でデータを更新した後、次のテーブルをクリーンアップする必要があります。

+ Finance and Operations アプリ テーブル: **DualWriteProjectConfiguration**、**DualWriteProjectFieldConfiguration**、および **BusinessEventsDefinition**。 
+ Dataverse テーブル: **DualwriteRuntimeConfiguration**。 

環境を再びリンクし、手動でマップを再有効化する必要があります。

### <a name="i-need-real-time-integration-and-i-want-to-move-some-tables-or-scenarios-from-data-integrator-to-dual-write-how-do-i-migrate-and-what-are-the-implications-of-changing-my-integration-pattern"></a>リアルタイム統合が必要なので、一部のテーブルまたはシナリオをデータ インテグレーターから二重書き込みに移動したいと考えています。 移行の方法と、統合パターンを変更した場合の影響について教えてください。

Prospect to Cash を二重書き込みに移行する方法の詳細については、[データ インテグレーターから二重書き込みへのデータの移行](https://www.yammer.com/dynamicsaxfeedbackprograms/#/files/433337729024) を参照してください。 一般に、移行中に変更される可能性があるものを 3 つ挙げておきます。

+ データ インテグレーターから二重書き込みへのマップの手動移行
+ 高度なクエリ機能がないため、テーブルを変更
+ 会社のストライピングなどの新しい概念に適合するためのデータ移行

### <a name="on-finance-and-operations-data-tables-can-i-develop-unbounded-columns-that-flow-to-dataverse-by-using-dual-write"></a>Finance and Operations データ テーブルでは、二重書き込みを使用して Dataverse にフローするバインドされない列を開発することはできますか?

はい。 [計算列と仮想列](../data-entity-computed-columns-virtual-fields.md)の両方を使用できます。 ただし、読み取りと書き込みに必要な追加のX++ ロジックを使用して、パフォーマンスのオーバーヘッドを監視する必要があります。 同じトランザクション内でのラウンド トリップは許可されません。 したがって、X++ を使用して追加の値を変換または計算するために仮想列を使用することは避け、それが同じトランザクション内の Dataverse に戻ることを予期してください。

### <a name="when-i-use-the-dataverse-offline-app-what-happens-if-i-cant-sync-the-data-after-reconnection-does-this-situation-cause-an-inconsistent-state-between-the-dataverse-environment-and-the-finance-and-operations-environment"></a>Dataverse オフライン アプリを使用して、再接続後にデータを同期できない場合はどうなりますか? この状況により、Dataverse 環境と Finance and Operations 環境との間で状態が矛盾することになりますか?

[電話用 Dynamics 365 アプリ](/dynamics365/mobile-app/install-dynamics-365-for-phones-and-tablets)、または [Field Service Mobile アプリ](/dynamics365/field-service/field-service-mobile-overview) をオフライン モードで使用すると、Dataverse データをオフラインで操作できます。 両方のアプリで、データはオフラインで保存され、お客様の裁量で、サーバーとの同期を行うことができます。 オフライン データとサーバーの同期中にエラーが発生し、他の環境が失敗しているために更新ができない場合、データ同期は失敗し、Dataverse は更新されません。 統合が一時停止したときに、同期を再度実行して、サーバーに更新データを保存することができます。 これらの変更はステージングされ、マッピングが再度実行されるときに Finance and Operations 環境に同期されます。 詳細については、[Power Apps Mobile でモデル駆動型アプリおよびキャンバス アプリを実行する](/powerapps/mobile/run-powerapps-on-mobile)を参照してください。

## <a name="mapping-concepts-between-apps"></a>アプリ間の概念のマッピング

### <a name="how-are-number-sequences-handled-for-example-the-customer-account-number-is-automatically-generated-in-finance-and-operations-apps-but-its-added-manually-in-customer-engagement-apps"></a>番号順序はどのように処理されますか? たとえば、顧客アカウント番号は Finance and Operations アプリで自動的に生成されますが、Customer Engagement アプリでは手動で追加されています。

Finance and Operations アプリと Customer Engagement アプリの番号順序は関連付けられていません。 複数のマスター テーブルが含まれるシナリオでは、別々の番号順序の形式を設計するか、各アプリケーションの範囲を定める必要があります。 次にいくつか例を挙げます。

+ Finance and Operationsアプリでは、**F0001、F0002、F0003** を使用します。 Customer Engagement アプリでは、**C0001、C0002、C0003** を使用します。
+ Finance and Operations アプリでは、**US0001 から US4999 まで** を使用します。 Customer Engagement アプリでは、**US5000 から US9999 まで** を使用します。

テーブルが単一のシステムで作成された場合は、ソース アプリに対してのみ番号順序を設定します。 詳細については、[自動付番列](/powerapps/maker/common-data-service/autonumber-columns)を参照してください。

### <a name="can-i-map-a-company-specific-table-in-a-customer-engagement-app-with-a-global-table-in-a-finance-and-operations-app-or-a-global-table-in-a-customer-engagement-app-with-a-company-specific-table-in-a-finance-and-operations-app"></a>Customer Engagement アプリの会社固有のテーブルを Finance and Operations アプリのグローバル テーブルに、または Customer Engagement アプリのグローバル テーブルを Finance and Operations アプリの会社固有のテーブルにマップすることはできますか?

二重書き込みでは、会社間のテーブル、または会社固有のテーブルのみ、両側からのマッピングがサポートされます。

### <a name="how-do-i-make-a-company-specific-table-in-dataverse"></a>どのように Dataverse の会社固有のテーブルを作成しますか?

Dataverse の会社固有のカスタム テーブルを作成するには、カスタム テーブルと標準の会社テーブルとの間に多対一 (N:1) の関係を追加します。 また、テーブル キーの一部として会社の外部キーを含める必要があります。 詳細については、[Dataverse の企業概念](company-data.md) を参照してください。

テーブル マップの二重書き込みを有効にするには、Dataverse で代替キーを定義する必要があります。 Dataverse の代替キーの値は、Finance and Operations アプリで定義されているキーと一致する必要があります。 詳細については、[テーブルをリンクするための基準](enable-entity-map.md#criteria-for-linking) を参照してください。

### <a name="is-there-a-document-about-best-practices-for-table-usage-should-i-use-customers-v2-customers-v3-or-customer-details-what-is-the-difference-between-these-tables-and-what-is-the-use-case-for-each"></a>テーブルの使用方法に関するベスト プラクティスについてのドキュメントがありますか? 顧客 V2、顧客 V3、または顧客の詳細を使用する必要がありますか? これらのテーブルの違いは何ですか、またそれぞれのユース ケースはどのようなものですか?

可能であれば、顧客や仕入先の統合などの一般的なシナリオをカバーしている[標準のシナリオ](./customer-mapping.md)を使用してください。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]