---
title: Finance and Operations 仮想エンティティに関するよくあるご質問
description: このトピックでは、Finance and Operations 仮想エンティティに関してよく寄せられる質問の一覧を示します。
author: Sunil-Garg
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-05-31
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: a3fc5746f538ea6a74fb16e7d659902c02369bb9
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063045"
---
# <a name="finance-and-operations-virtual-entities-faq"></a>Finance and Operations 仮想エンティティに関するよくあるご質問

[!include[banner](../includes/banner.md)]



> [!IMPORTANT]
> この機能を使用するには、財務と運用アプリのバージョン 10.0.12 が必要ですが、Dataverse にはサービス更新 189 が必要です。 Dataverse のリリース情報は、[最新バージョンの利用可能性](/business-applications-release-notes/dynamics/released-versions/dynamics-365ce#all-version-availability)ページに発行されています。

このトピックは、Finance and Operations 仮想エンティティに関してよく寄せられる質問を集めたものです。 

### <a name="do-tier-1-finance-and-operations-environments-or-demo-topologies-work"></a>Tier 1 Finance and Operations 環境、またはトポロジのデモは機能しますか?

はい、レベル 1、DEVTEST、およびデモの各トポロジが機能します。

### <a name="what-version-of-finance-and-operations-do-i-need"></a>どのバージョンの Finance and Operations が必要ですか?

必要な最小バージョンは 10.0.12 です。

### <a name="can-a-solution-from-an-independent-software-vendor-isv-take-a-dependency-on-virtual-entities-what-does-the-application-lifecycle-management-alm-look-like"></a>独立系ソフトウェアベンダー (ISV) のソリューションは、仮想エンティティへの依存を受けることができますか。 アプリケーション ライフサイクル管理 (ALM) はどのような外観になりますか。

はい。 仮想エンティティはすべて MicrosoftOperationsERPVE ソリューションで生成され、API 管理されます。言い換えると、ソリューションの項目は、エンティティの表示/非表示を切り替えたときに変更されますが、ソリューションは依存できるマネージド ソリューションのままになります。 標準 ALM フローでは、ISV ソリューションの **既存の追加** オプションを使用して、このソリューションから仮想エンティティに対する標準参照を取得するだけです。 ソリューションの依存関係が見つからない場合は、ソリューションがインポートされたときやインポート時に、その仮想エンティティが存在しない場合は自動的に表示されます。

### <a name="which-entities-from-finance-and-operations-do-users-see-in-the-catalog-in-dataverse"></a>Dataverse のカタログでユーザーには Finance and Operations のどのエンティティが表示されるのでしょうか?

一般に、ユーザーには、**IsPublic** が **はい** に設定されているすべてのエンティティが表示されます。 これらのエンティティは、Open Data Protocol (OData) で現在表示されているものと同じです。

### <a name="do-all-microsoft-power-platform-users-have-to-be-users-in-finance-and-operations"></a>すべての Microsoft Power Platform ユーザーが Finance and Operations のユーザーである必要がありますか?

Microsoft Power Platform の **対話型ユーザー** が、仮想エンティティを通じて Finance and Operations データにアクセスしようとする場合、Finance and Operations のユーザーとしても存在する必要があります。 したがって、*すべて* のユーザーが Finance and Operations のユーザーであるとは限りません。 仮想エンティティを介して Finance and Operations データにアクセスするユーザーのみが Finance and Operations のユーザーである必要があります。

**S2S アプリケーション ユーザー** は、仮想エンティティへの呼び出しにも使用できます。 この種類の統合を行う場合は、**システム管理 > 設定 > Azure Active Directory アプリケーションの構成** でアプリケーション ユーザーを設定する必要があります。 これにより、アプリケーションは仮想エンティティを使用して Finance and Operations と統合できます。

### <a name="where-do-i-find-the-catalog-entity"></a>カタログ エンティティはどこにありますか。

**高度な検索** ウィンドウでは、エンティティの名前は **使用可能な Finance and Operations エンティティ** になります。

### <a name="is-there-a-way-to-specify-a-company-when-i-perform-data-operations-on-a-virtual-entity"></a>仮想エンティティに対してデータ操作を実行するときに会社を指定する方法はありますか。

はい。 Finance and Operations には暗黙的に会社が含まれていますが、Dataverse では会社でストライプされたエンティティごとに明示的なフィールドになっています。 **会社コード** フィールド (値は 4 文字の文字列) または **会社** フィールド (cdm\_Company へのルックアップ) のいずれかを使用できます。 どちらの方法でも同じ情報が得られます。

### <a name="can-i-change-the-prefix-for-the-virtual-entities"></a>仮想エンティティの接頭辞を変更することはできますか。

いいえ。 すべての Finance and Operations 仮想エンティティは、MicrosoftOperationsERPVE ソリューションで生成する必要があり、すべて "mserp\_" プレフィックスが付いている必要があります。 この接頭語は変更しないでください。 接頭語を変更する必要があると考えられる場合は、そのシナリオを Microsoft と共有する必要があります。

### <a name="how-can-i-filter-data-in-an-app-that-is-created-by-using-power-apps-based-on-the-current-user-or-any-other-dynamic-criteria-such-as-today-10"></a>Power Apps を使用して作成されたアプリのデータについては、現在のユーザーまたはその他の動的な基準 (10 日前など) に基づいてフィルター処理を行うことができます。

エンティティの RetrieveMultiple メッセージに対して前工程プラグインを作成し、その中のクエリに対する基準を変更することができます。 または、結果を返す前に結果をフィルター処理するために、操作後のプラグインを作成することもできます。

### <a name="can-i-pin-a-model-driven-app-into-finance-and-operations"></a>モデル駆動型のアプリを Finance and Operations にピン留めできますか?

いいえ、現時点ではモデル駆動アプリを Finance and Operations にピン留めすることはできません。

### <a name="how-can-i-show-in-the-same-grid-data-from-multiple-virtual-entities-that-are-joined-to-a-physical-entity-record-in-dataverse"></a>Dataverse の物理エンティティ レコードに結合されている複数の仮想エンティティからのデータを、同じグリッドで表示する方法はありますか。

このアプローチは、現在 Dataverse でサポートされていません。

### <a name="how-do-i-add-subcomponents-in-the-new-power-apps-experience"></a>新しい Power Apps エクスペリエンスでサブコンポーネントを追加するにはどうすればよいですか。

前の Power Apps ユーザー インターフェイス (UI) と同様に、**既存の追加** 操作をやり直す必要があります。 ソリューションを選択した後、顧客グループが既にエンティティとして追加されている場合は、次の手順に従います。

1. **既存の追加** \> **エンティティ** を選択します。
2. 顧客グループ エンティティを選択し、**次へ** を選択します。
3. **コンポーネント** で、**コンポーネントの選択** を選択します。
4. 必要なフィールド、リレーションシップ、およびフォームを選択し、**追加** をクリックします。

### <a name="if-i-want-a-default-value-to-be-entered-in-a-field-during-pre-create-will-an-initvalue-on-the-data-entity-work"></a>事前作成時にフィールドに既定値を入力する必要がある場合は、データ エンティティの initValue は機能しますか。

はい。 呼び出しの順序を次に示します。

1. Dataverse が作成または更新メッセージを送信します。
2. Finance and Operations エンティティおよびバッキング テーブルの既存のすべてのロジックが呼び出されます。 このロジックには、値を変更する可能性がある既定値のエントリが含まれています。
3. Dataverse は、既定値が入力されたフィールドを含む、データの最新のコピーを取得するための別の取得 (1 つ) メッセージを送信します。

### <a name="can-i-debug-finance-and-operations-when-we-do-a-create-read-update-and-delete-crud-operation-from-dataverse-if-so-which-process-do-i-have-to-attach"></a>Dataverse から作成、読み取り、更新、削除 (CRUD) 操作を行うときに、Finance and Operations をデバッグできますか? できる場合、どのプロセスにアタッチする必要がありますか。

はい、Finance and Operations でデバッグするには、管理者として Visual Studio を起動します。通常、財務と運用アプリは、w3wp.exe でプロセスとして実行されます。 ただし、管理者として Visual Studio を開くと、IISExpress.exe が自動的に開かれ、Finance and Operations がそこにホストされます。 IISExpress.exe (管理者として Visual Studio が実行されていない場合は w3wp.exe) にアタッチできます。 仮想エンティティ コードにブレークポイントを設定するには、**CDSVirtualEntityAdapter** および **CDSVirtualEntityController** クラスを検索します。 アダプター クラスは、最初に呼び出されるクラスであり、シリアル化と逆シリアル化のみを行います。 次に、実際のクエリを実行するためにコントローラー クラスに委任します。 したがって、通常はコントローラー クラスが最も簡単なブレークポイントの配置です。

### <a name="does-the-form-business-logic-in-finance-and-operations-get-called-through-virtual-entities"></a>Finance and Operations のフォーム ビジネス ロジックは、仮想エンティティを介して呼び出されますか?

フォームに存在する Finance and Operations ビジネス ロジックは、仮想エンティティを介して呼び出されることはありません。 代わりに、同じエンティティへの OData アクセスを行う場合と同じ動作を期待する必要があります。 予想されるのは、OData に公開されているエンティティ (つまり、**IsPublic** が **Yes** に設定されているエンティティ) が適切に保護され、データが破損しないようにすることです。 この保護がないエンティティがある場合は、この状況はエンティティのバグを表します。 OData と仮想エンティティ間でエンティティの動作に違いがある場合は、仮想エンティティ機能のバグを示しています。

### <a name="if-i-develop-a-new-finance-and-operations-entity-and-want-to-see-it-in-dataverse-do-i-have-to-select-refresh-entity-list-in-finance-and-operations-do-i-have-to-do-anything-in-dataverse"></a>新しい Finance and Operations エンティティを作成し、それを Dataverse に表示する場合、Finance and Operations でエンティティ リストの更新を選択する必要はありますか? Dataverse で何かを行う必要はありますか。

理論的には、エンティティの一覧を更新する必要はありません。 通常は、Application Object Server (AOS) の実行場所に応じて、インターネット インフォメーション サービス (IIS) をリセットするか、IIS Express を再起動するだけでかまいません。 エンティティの一覧は、プロセスごとのキャッシュである SysGlobalObjectCache にキャッシュされるということになります。 このキャッシュにリストが正確であると示されていない場合は、リストが再構築されます。 リビルド プロセスには約 5 秒かかります。 したがって、AOS プロセス (w3wp.exe または iisexpress.exe) を再起動すると、リストは次に Dataverse から照会されるときに正確になります。 また、リコンパイルは SysGlobalObjectCache キャッシュをフラッシュする *必要があります* が、そうでない場合もあります。 この場合、AOS を再起動すると、それがフラッシュされます。

### <a name="is-there-guidance-on-when-to-use-a-virtual-entity-and-when-to-use-dual-write"></a>いつ仮想エンティティを使用するか、いつ二重書き込みを使用するかについてのガイダンスはありますか?

仮想エンティティおよび、二重書き込みをいつ使用するかに関しては[財務と運用アプリとサード パーティー サービスの統合](../data-entities/integration-overview.md)で説明されています。

### <a name="when-adding-records-using-virtual-entities-is-there-any-way-to-use-number-sequences"></a>仮想エンティティを使用してレコードを追加する場合、番号順序を使用する方法はありますか?
はい、Finance and Operations エンティティで番号順序が自動生成される場合は、仮想エンティティからも同じように機能します。

### <a name="why-does-search-view-not-work-in-power-apps"></a>Power Apps で「検索ビュー」が機能しないのはなぜですか?
エンティティの簡易検索ビューにフィールドが追加されていない場合、検索ボックスは使用できません。 回避策として、エンティティのフィールドを 1 つ以上、簡易検索ビューに追加することができます。

### <a name="the-virtual-entity-performance-is-slow-when-a-virtual-entity-has-relationships-to-other-entities-is-there-guidance-on-how-to-avoid-these-issues"></a>仮想エンティティに他のエンティティとのリレーションシップがある場合、仮想エンティティのパフォーマンスが低下します。 これらの問題を回避する方法のガイダンスはありますか?
仮想エンティティに他のエンティティとのリレーションシップがある場合に、仮想エンティティのパフォーマンスが低下する理由はいくつかあります。 新しいパターンが特定されると、このセクションが更新されます。 現在、次のパターンが知られています。このパターンは、ガイダンスとして使用できます。

仮想エンティティに他のエンティティとのリレーションシップがある場合は、フィールドの選択リストに関連エンティティの外部キー値が含まれる場合、仮想エンティティ フレームワークは、関連するエンティティをクエリする必要があります。 既定では、エンティティに対するクエリは、呼び出し元が特定のフィールド セットを要求しない限り、すべてのフィールドを返します。 ベスト プラクティスは、絞り込み選択リストを指定します。 これは、パフォーマンスの低下を防ぐのに役立ちます。

この問題の例については、[仮想テーブル クエリの Dataverse 最適化](../../../human-resources/hr-developer-optimize-virtual-table-queries.md) で説明します。

### <a name="can-i-configure-virtual-entities-to-connect-other-power-platform-environments-to-the-finance-and-operations-environment-even-if-the-power-platform-integration-is-enabled"></a>Power Platform 統合が有効になっている場合でも、他の Power Platform 環境を Finance and Operations 環境に接続するように仮想エンティティを構成できますか?

[ビジネス イベントとデータ イベントの同期 Dataverse](../business-events/business-events-flow.md) など、Microsoft Power Platform 統合の一部の機能は、財務と運用アプリと Microsoft Power Platform 統合を介してリンクされた Power Platform 環境の間でのみ機能しますが、複数の Power Platform 環境および Finance and Operations 環境の間で仮想エンティティを手動で構成することは引き続き可能です。 

Microsoft Power Platform 統合が有効になっている場合、Finance and Operations 環境は、単一の Power Platform 環境にリンクされます。 これは、統合の 1 対 1 の環境関係になります。 これを有効にすると、2 つの環境間で仮想エンティティが自動的に構成されます。 つまり、[Dataverse 仮想エンティティの構成](admin-reference.md)ドキュメントで定義されている手動の仮想エンティティ構成は必要ないことを意味します。 2 つの環境間で Microsoft Power Platform 統合を有効にする前に手動の仮想エンティティ構成が行われた場合、統合を有効にすると手動構成は無視され、自動構成を使用して 2 つの環境が接続されます。

自動仮想エンティティ構成は、Microsoft Power Platform 統合を通じて Finance and Operations 環境にリンクされた Power Platform 環境に使用されますが、追加の Power Platform 環境で仮想エンティティを手動で構成して、複数の Power Platform 環境で Finance and Operations 環境の仮想エンティティを有効にすることができます。

### <a name="can-i-use-dataverse-virtual-entities-as-a-data-source-with-the-data-integrator"></a>Dataverse 仮想エンティティを、データ統合のデータ ソースとして使用できますか?

いいえ。 仮想エンティティは、[データ統合](/power-platform/admin/data-integrator.md)とのデータ統合のソースとしてはサポートされていません。 技術的な制限により、データ インテグレーターはソース データのデルタを取得して、データを移行先環境にプッシュすることができません。

### <a name="im-getting-an-error-that-paging-is-not-supported-how-do-i-work-around-this"></a>ページングがサポートされていないというエラーが表示されます。 回避するにはどうすればよいですか。

仮想エンティティに対してクエリを実行すると、「一時テーブルを使用するクエリではページングはサポートされていません」というメッセージが表示される場合があります。 これは仕様です。 クエリに一時テーブルが含まれる場合、エラーが返されます。 このエラーが返された場合は、クエリに含まれる一時テーブルを特定し、それを除外するようにクエリを変更する必要があります。
無効になっているコンフィギュレーション キーによって、このエラーが発生する場合があります。 Dynamics 365 ERP 仮想エンティティ ソリューションで提供される既定の仮想エンティティには、すべての構成が有効になっている場合、一時テーブルは含まれません。 ただし、エンティティのバッキング テーブルに対してコンフィギュレーション キーが有効になっていない場合は、物理テーブルが一時テーブルに置き換えられるので、スキーマ変更に対してシステムを再コンパイルする必要はありません。 これにより、仮想エンティティ クエリに一時テーブルが含まれます。 これらのシナリオでは、関連付けられているコンフィギュレーション キーを有効にしてエラーを解決します。

コンフィギュレーション キーがデータ エンティティに与える影響の詳細については、[コンフィギュレーション キーおよびデータ エンティティ](../data-entities/config-key-entities.md)を参照してください。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
