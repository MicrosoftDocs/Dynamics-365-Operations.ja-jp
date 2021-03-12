---
title: Human Resources 仮想テーブルに関するよく寄せられる質問
description: このトピックでは、Human Resources 仮想エンティティに関してよく寄せられる質問の一覧を示します。
author: jaredha
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 7026e0888f935657463f5c7b05bfbfc0dc127315
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111208"
---
# <a name="human-resources-virtual-tables-faq"></a>Human Resources 仮想テーブルに関するよく寄せられる質問

このトピックでは、Dynamics 365 Human Resources の仮想テーブルに関してよく寄せられる質問のコレクションを示します。 

> [!NOTE]
> Dataverse (旧 Common Data Service) および用語更新の詳細については、[Microsoft Dataverse とは何ですか?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)を参照してください

### <a name="can-a-solution-from-an-independent-software-vendor-isv-take-a-dependency-on-virtual-tables-what-does-the-application-lifecycle-management-alm-look-like"></a>独立系ソフトウェアベンダー (ISV) のソリューションは、仮想テーブルに依存できますか? アプリケーション ライフサイクル管理 (ALM) はどのような外観になりますか。

はい。 仮想テーブルはすべて Dynamics 365 HR 仮想エンティティ ソリューションで生成され、API によって管理されます。 ソリューションの項目は、テーブルの表示または非表示に応じて変更されます。 ただし、ソリューションは引き続き依存できる管理ソリューションです。 各テーブルのスキーマおよび契約が維持されます。 標準 ALM フローでは、ISV ソリューションの **既存の追加** オプションを使用して、このソリューションから仮想テーブルに対する標準参照を取得するだけです。 ソリューションの依存関係の欠落が、ソリューションのインポート時にチェックされます。 インポート時に、特定の仮想テーブルがまだ存在しない場合は、仮想テーブルが自動的に表示されます。

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

No. すべての Human Resources 仮想テーブルは、Dynamics 365 HR 仮想エンティティ ソリューションで生成され、"mshr\_" の接頭語が付く必要があります。 この接頭語は変更しないでください。 接頭語を変更する必要があると考えられる場合は、そのシナリオを Microsoft と共有する必要があります。

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]