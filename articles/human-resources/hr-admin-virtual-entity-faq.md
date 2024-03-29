---
title: Human Resources 仮想テーブルに関するよく寄せられる質問
description: この記事では、Human Resources 仮想エンティティに関してよく寄せられる質問への回答を提供します。
author: jaredha
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 4a205cc1979a0a1bc38c7908947232fcf563d8d4
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066124"
---
# <a name="human-resources-virtual-tables-faq"></a>Human Resources 仮想テーブルに関するよく寄せられる質問


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、よく寄せられる Dynamics 365 Human Resources の仮想テーブルに関していくつかの質問に対する回答を提供します。

> [!NOTE]
> Dataverse (旧 Common Data Service) および用語更新の詳細については、[Microsoft Dataverse とは何ですか?](/powerapps/maker/data-platform/data-platform-intro)を参照してください

### <a name="can-a-solution-from-an-independent-software-vendor-isv-take-a-dependency-on-virtual-tables-what-does-the-application-lifecycle-management-alm-look-like"></a>独立系ソフトウェアベンダー (ISV) のソリューションは、仮想テーブルに依存できますか? アプリケーション ライフサイクル管理 (ALM) はどのような外観になりますか。

はい。 仮想テーブルはすべて Dynamics 365 HR Virtual Entities ソリューションで生成され、API によって管理されます。 ソリューションの項目は、テーブルの表示または非表示に応じて変更されます。 ただし、ソリューションは引き続き依存できる管理ソリューションです。 各テーブルのスキーマおよび契約が維持されます。 標準 ALM フローでは、ISV ソリューションの **既存の追加** オプションを使用して、このソリューションから仮想テーブルに対する標準参照を取得するだけです。 ソリューションの依存関係の欠落が、ソリューションのインポート時にチェックされます。 インポート時に、特定の仮想テーブルがまだ存在しない場合は、仮想テーブルが自動的に表示されます。

### <a name="which-tables-from-human-resources-do-users-see-in-the-catalog-in-dataverse"></a>Dataverse のカタログでユーザーに表示される Human Resources のテーブルは何ですか?

一般に、ユーザーには、**IsPublic** が **はい** に設定されているすべてのテーブルが表示されます。 これらのテーブルは、Open Data Protocol (OData) で現在表示されているテーブルと同じです。

### <a name="do-all-microsoft-power-platform-users-have-to-be-users-in-human-resources"></a>すべての Microsoft Power Platform ユーザーが Human Resources のユーザーである必要がありますか?

仮想テーブルを介して Human Resources データにアクセスしようとする Microsoft Power Platform のユーザーはすべて、Human Resources でユーザーとして存在している必要があります。 したがって、*すべて* のユーザーが Human Resources のユーザーである必要はありません。 仮想テーブルを介して Human Resources データにアクセスするユーザーのみが Human Resources のユーザーである必要があります。

### <a name="where-do-i-find-the-catalog-table"></a>カタログ テーブルはどこにありますか?

テーブル カタログは、Human Resources アプリケーションの **Dataverse 統合** ページの **仮想テーブル** タブに表示されます。 使用可能なすべてのテーブルが、設定およびコンフィギュレーションの完了後に一覧表示されます。 詳細については、[Dataverse 仮想テーブルのコンフィギュレーション](hr-admin-integration-common-data-service-virtual-entities.md)を参照してください。

### <a name="is-there-a-way-to-specify-a-company-when-i-perform-data-operations-on-a-virtual-table"></a>仮想テーブルに対してデータ操作を実行するときに会社を指定する方法はありますか?

はい。 Human Resources には会社が暗黙のうちに含まれていますが、Dataverse では会社でストライプされたテーブルごとに明示的な列になっています。 **会社コード** 列 (値は 4 文字の文字列)、または **会社** 列 (cdm\_Company へのルックアップ) のいずれかを使用できます。 どちらの方法でも同じ情報が得られます。

Dataverse Web API を介してテーブルにアクセスする場合、その会社は **データ領域 ID** プロパティ (mshr\_dataareaid) で識別されます。 このプロパティを持つ各会社固有のテーブルには、cdm\_Company テーブルへのナビゲーション プロパティがあります。

### <a name="can-i-change-the-prefix-for-the-virtual-tables"></a>仮想テーブルの接頭語を変更することはできますか?

No. すべての Human Resources 仮想テーブルは、Dynamics 365 HR Virtual Entities ソリューションで生成され、"mshr\_" の接頭語が付く必要があります。 この接頭語は変更しないでください。 接頭語を変更する必要があると考えられる場合は、そのシナリオを Microsoft と共有する必要があります。

### <a name="how-can-i-filter-data-in-a-power-apps-app-based-on-the-current-user-or-any-other-dynamic-criteria-such-as-today-10"></a>Power Apps アプリのデータについては、現在のユーザーまたはその他の動的な基準 (10 日前など) に基づいてフィルター処理を行うことができますか?

テーブルの RetrieveMultiple メッセージに対して前工程プラグインを作成し、その中のクエリに対する基準を変更することができます。 または、結果を返す前に結果をフィルター処理するために、操作後のプラグインを作成することもできます。

### <a name="how-can-i-show-in-the-same-grid-data-from-multiple-virtual-tables-that-are-joined-to-a-physical-table-record-in-dataverse"></a>Dataverse の物理テーブル レコードに結合されている複数の仮想テーブルからのデータを、同じグリッドで表示する方法はありますか?

このアプローチは、現在 Dataverse でサポートされていません。

### <a name="if-i-want-a-default-value-to-be-entered-in-a-field-during-pre-create-will-an-initvalue-on-the-data-table-work"></a>事前作成時にフィールドに既定値を入力する必要がある場合は、データ テーブルの initValue は機能しますか?

はい。 呼び出しの順序を次に示します。

1. Dataverse が作成または更新メッセージを送信します。
2. Human Resources エンティティおよびバッキング テーブルの既存のすべてのロジックが呼び出されます。 このロジックには、値を変更する可能性がある既定値のエントリが含まれています。
3. Dataverse は、既定値が入力された列を含む、データの最新のコピーを取得するための別の取得 (単一) メッセージを送信します。

### <a name="does-the-form-business-logic-in-human-resources-get-called-through-virtual-tables"></a>Human Resources のフォーム ビジネス ロジックは、仮想テーブルを介して呼び出されますか?

フォームに存在する Human Resources ビジネス ロジックは、仮想テーブルを介して起動されることはありません。 代わりに、同じテーブルへの OData アクセスを行う場合と同じ動作が予想されます。 OData (つまり、**IsPublic** が **はい** に設定されているテーブル) に公開されているテーブルは、適切に保護され、データが破損しないように確認することが必要です。 この保護がないテーブルがある場合、この状況はテーブルのバグを表します。 OData と仮想テーブル間でテーブルの動作に違いがある場合、仮想テーブル機能のバグを示しています。

### <a name="when-adding-records-using-virtual-tables-is-there-any-way-to-use-number-sequences"></a>仮想テーブルを使用してレコードを追加する場合、番号順序を使用する方法はありますか?

はい、Human Resources テーブルで番号順序が自動生成される場合は、仮想テーブルからも同じように機能します。

### <a name="why-doesnt-search-view-work-in-power-apps"></a>Power Apps で「検索ビュー」が機能しないのはなぜですか?

テーブルの簡易検索ビューに列が追加されていない場合、検索ボックスは使用できません。 回避策として、テーブルの列を 1 つ以上、簡易検索ビューに追加することができます。

### <a name="are-custom-fields-supported-on-virtual-tables"></a>カスタム フィールドは仮想テーブルでサポートされていますか?

はい。カスタム フィールドは仮想テーブルでサポートされています。 最初に、仮想テーブルに関連付けられているデータ エンティティにカスタム フィールドを追加する必要があります。 [データ エンティティのカスタム フィールドの公開](../fin-ops-core/fin-ops/get-started/user-defined-fields.md#exposing-custom-fields-on-data-entities)で説明されている手順に従って、カスタム フィールドをデータ エンティティに追加できます。 データ エンティティにカスタム フィールドを追加した後、仮想テーブルを生成または更新することで、関連付けられている仮想テーブルにカスタム フィールドを追加できます。 仮想テーブルの生成および更新方法の詳細については、[仮想テーブルの生成](hr-admin-integration-common-data-service-virtual-entities.md#generate-virtual-tables)を参照してください。

仮想テーブルに対して依存関係を作成した場合は、仮想テーブルからカスタム フィールドを追加したり削除したりすることはできません。 たとえば、仮想テーブルを使用する Power App を作成した場合、依存関係がある間は仮想テーブルを削除、変更、または更新することはできません。 Dynamics 365 HR Virtual Entities マネージド ソリューションの一部である仮想テーブルを更新するには、最初に、マネージド ソリューションの一部ではない依存コンポーネントを削除する必要があります。 依存コンポーネントを確認および削除する方法の詳細については、[依存関係の削除](/power-platform/alm/removing-dependencies)を参照してください。

### <a name="what-do-i-do-if-i-get-an-error-that-the-dynamics-365-for-talent-user-wasnt-found"></a>Dynamics 365 for Talent ユーザーが見つからないというエラーが発生した場合、どうしたらよいですか?

**Microsoft Dataverse 統合** ページで仮想テーブルを設定すると、アクション センターに次のようなエラー メッセージが表示される場合があります。

`User Dynamics365 for Talent was not found in finance and operations. Please ensure this user exists.`

このメッセージは、仮想テーブル用に設定されたアプリに対して、Human Resources アプリケーションでアクセス許可が付与されていないことを示しています。 これを解決するには、[Human Resourcesでアプリのアクセス許可を付与する](hr-admin-integration-common-data-service-virtual-entities.md#grant-app-permissions-in-human-resources) 手順を実行します。

### <a name="what-do-i-do-if-the-finance-and-operations-virtual-data-source-configurations-option-isnt-available-in-my-microsoft-dataverse-environment"></a>財務と運用の仮想データ ソースの構成オプションを Microsoft Dataverse 環境で使用できない場合はどうしたらよいですか?

仮想テーブルの設定時に Dynamics 365 HR 仮想テーブル アプリをインストールする必要があります。このアプリにより、**財務と運営の仮想データ ソースの構成** オプションが追加されます。 **Microsoft Dataverse 統合** ページでのアプリのインストールの詳細については、[Dataverse 仮想テーブルの構成](hr-admin-integration-common-data-service-virtual-entities.md#install-the-dynamics-365-hr-virtual-table-app) を参照してください。

**Microsoft Dataverse 統合** ページの **仮想テーブル アプリのインストール** アクションが正常に完了しなかった場合は、Power Platform 管理センターでアクションを実行できます。

1. [Power Platform 管理センター](https://admin.powerplatform.microsoft.com)を開きます。

2. **環境** の一覧で、Human Resources のインスタンスに関連付けられている Power Apps 環境を選択します。

3. ページの **リソース** セクションで、**Dynamics 365 アプリ** を選択します。

4. **アプリのインストール** アクションを選択します。

5. **Dynamics 365 HR 仮想テーブル** を選択し、**次へ** を選択します。

6. サービス使用条件に同意することを確認してマークします。

7. **インストール** を選択します。

インストールには数分かかります。 完了すると **財務と運用の仮想データ ソースの構成** エンティティがこの環境で生成されます。

![Power Platform 管理センターから Dynamics 365 HR 仮想テーブル アプリをインストールします。](media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="can-i-generate-virtual-tables-for-hr-from-my-power-apps-environment"></a>HR の仮想テーブルを自分の Power Apps 環境から生成できますか?

はい。 [Dataverse 仮想テーブルのコンフィギュレーション](hr-admin-integration-common-data-service-virtual-entities.md)に示されている仮想テーブルの前提条件の設定手順を完了した後、Power Apps 環境から直接仮想テーブルを生成できます。 ドキュメントの[仮想テーブルの生成](hr-admin-integration-common-data-service-virtual-entities.md#generate-virtual-tables)セクションで説明されている Human Resources アプリから仮想テーブルを生成するプロセスではなく、このプロセスに従うことができます。

1. [Power Platform 管理センター](https://admin.powerplatform.microsoft.com)を開きます。

2. **環境** の一覧で、Human Resources のインスタンスに関連付けられている Power Apps 環境を選択します。

3. ページの **詳細** セクションで、**環境 URL** を選択します。

4. ソリューションの正常性ハブで、ページ右上のアイコン グループにある **高度な検索** (じょうご) アイコンを選択します。

5. **検索** リストで、**使用可能な HR エンティティ** を選択します。

6. フィルター オプションを使用して、有効にするエンティティを検索します。

7. リストからエンティティを選択します。

8. エンティティ ページで、**生成済み** のプロパティを **はい** に変更します。

9. エンティティ ページを保存して閉じます。

> [!NOTE]  
> **複数のレコードの変更** ページを使用すると、複数の仮想テーブルを一度に生成できます。 ページで複数のレコードを選択し、リボンで **編集** アクションを選択します。 これにより、選択したすべてのレコードについて、**生成済み** のプロパティを変更できます。

[!INCLUDE[footer-include](../includes/footer-banner.md)]

