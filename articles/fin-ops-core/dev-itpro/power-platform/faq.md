---
title: Finance and Operations 仮想エンティティに関するよく寄せられる質問
description: このトピックでは、Finance and Operations 仮想エンティティに関してよく寄せられる質問の一覧を示します。
author: Sunil-Garg
manager: AnnBe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-05-31
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 1912757eba69a8dd798d52f947d688423ad7cb6a
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744447"
---
# <a name="finance-and-operations-virtual-entities-faq"></a>Finance and Operations 仮想エンティティに関するよく寄せられる質問

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!IMPORTANT]
> この機能を使用するには、Finance and Operations アプリのバージョン 10.0.12 が必要ですが、Dataverse にはサービス更新 189 が必要です。 Dataverse のリリース情報は、[最新バージョンの利用可能性](https://docs.microsoft.com/business-applications-release-notes/dynamics/released-versions/dynamics-365ce#all-version-availability)ページに発行されています。

このトピックでは、Finance and Operations 仮想エンティティに関してよく寄せられる質問のコレクションを示します。 

### <a name="do-tier-1-finance-and-operations-environments-or-demo-topologies-work"></a>レベル 1 Finance and Operations 環境またはデモ トポロジは機能しますか。

はい、レベル 1、DEVTEST、およびデモの各トポロジが機能します。

### <a name="what-version-of-finance-and-operations-do-i-need"></a>必要な Finance and Operations のバージョンを教えてください。

必要な最小バージョンは 10.0.12 です。

### <a name="can-a-solution-from-an-independent-software-vendor-isv-take-a-dependency-on-virtual-entities-what-does-the-application-lifecycle-management-alm-look-like"></a>独立系ソフトウェアベンダー (ISV) のソリューションは、仮想エンティティへの依存を受けることができますか。 アプリケーション ライフサイクル管理 (ALM) はどのような外観になりますか。

はい。 仮想エンティティはすべて MicrosoftOperationsERPVE ソリューションで生成され、API 管理されます。言い換えると、ソリューションの項目は、エンティティの表示/非表示を切り替えたときに変更されますが、ソリューションは依存できるマネージド ソリューションのままになります。 標準 ALM フローでは、ISV ソリューションの **既存の追加** オプションを使用して、このソリューションから仮想エンティティに対する標準参照を取得するだけです。 ソリューションの依存関係が見つからない場合は、ソリューションがインポートされたときやインポート時に、その仮想エンティティが存在しない場合は自動的に表示されます。

### <a name="which-entities-from-finance-and-operations-do-users-see-in-the-catalog-in-dataverse"></a>Dataverse のカタログでユーザーに表示される Finance and Operations のエンティティは何ですか。

一般に、ユーザーには、**IsPublic** が **はい** に設定されているすべてのエンティティが表示されます。 これらのエンティティは、Open Data Protocol (OData) で現在表示されているものと同じです。

### <a name="do-all-microsoft-power-platform-users-have-to-be-users-in-finance-and-operations"></a>すべての Microsoft Power Platform ユーザーが Finance and Operations のユーザーである必要がありますか。

仮想エンティティを介して Finance and Operations データにアクセスしようとする Microsoft Power Platform のユーザーはすべて、Finance and Operations でユーザーとして存在している必要があります。 したがって、*すべて* のユーザーが Finance and Operations のユーザーであるとは限りません。 仮想エンティティを介して Finance and Operations データにアクセスするユーザーのみが Finance and Operations のユーザーである必要があります。

### <a name="where-do-i-find-the-catalog-entity"></a>カタログ エンティティはどこにありますか。

**高度な検索** ウィンドウでは、エンティティは **使用可能な Finance and Operations エンティティ** という名前になります。

### <a name="is-there-a-way-to-specify-a-company-when-i-perform-data-operations-on-a-virtual-entity"></a>仮想エンティティに対してデータ操作を実行するときに会社を指定する方法はありますか。

はい。 Finance and Operations には、会社が暗黙のうちに含まれていますが、Dataverse では会社でストライプされたエンティティごとに明示的なフィールドになっています。 **会社コード** フィールド (値は 4 文字の文字列) または **会社** フィールド (cdm\_Company へのルックアップ) のいずれかを使用できます。 どちらの方法でも同じ情報が得られます。

### <a name="can-i-change-the-prefix-for-the-virtual-entities"></a>仮想エンティティの接頭辞を変更することはできますか。

No. すべての Finance and Operations 仮想エンティティは、MicrosoftOperationsERPVE ソリューションで生成する必要があり、すべて "mserp\_" プレフィックスが付いている必要があります。 この接頭語は変更しないでください。 接頭語を変更する必要があると考えられる場合は、そのシナリオを Microsoft と共有する必要があります。

### <a name="how-can-i-filter-data-in-an-app-that-is-created-by-using-power-apps-based-on-the-current-user-or-any-other-dynamic-criteria-such-as-today-10"></a>Power Apps を使用して作成されたアプリのデータについては、現在のユーザーまたはその他の動的な基準 (10 日前など) に基づいてフィルター処理を行うことができます。

エンティティの RetrieveMultiple メッセージに対して前工程プラグインを作成し、その中のクエリに対する基準を変更することができます。 または、結果を返す前に結果をフィルター処理するために、操作後のプラグインを作成することもできます。

### <a name="can-i-pin-a-model-driven-app-into-finance-and-operations"></a>モデル駆動型アプリを Finance and Operations にピン留めできますか。

いいえ、現時点では、モデル駆動アプリを Finance and Operations にピン留めすることはできません。

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

### <a name="can-i-debug-finance-and-operations-when-we-do-a-create-read-update-and-delete-crud-operation-from-dataverse-if-so-which-process-do-i-have-to-attach"></a>Dataverse から作成、読み取り、更新、および削除 (CRUD) 操作を行うとき、Finance and Operations をデバッグできますか。 できる場合、どのプロセスにアタッチする必要がありますか。

はい、Finance and Operations でデバッグするには、管理者として Visual Studio を起動します。通常、Finance and Operations アプリは、w3wp.exe でプロセスとして実行されます。 ただし、管理者として Visual Studio を開くと、IISExpress が自動的に開かれ、Finance and Operations がそこにホストされます。 IISExpress.exe (管理者として Visual Studio が実行されていない場合は w3wp.exe) にアタッチできます。 仮想エンティティ コードにブレークポイントを設定するには、**CDSVirtualEntityAdapter** および **CDSVirtualEntityController** クラスを検索します。 アダプター クラスは、最初に呼び出されるクラスであり、シリアル化と逆シリアル化のみを行います。 次に、実際のクエリを実行するためにコントローラー クラスに委任します。 したがって、通常はコントローラー クラスが最も簡単なブレークポイントの配置です。

### <a name="does-the-form-business-logic-in-finance-and-operations-get-called-through-virtual-entities"></a>Finance and Operations のフォーム ビジネス ロジックは、仮想エンティティを介して呼び出されますか。

フォームに存在する Finance and Operations ビジネス ロジックは、仮想エンティティを介して起動されることはありません。 代わりに、同じエンティティへの OData アクセスを行う場合と同じ動作を期待する必要があります。 予想されるのは、OData に公開されているエンティティ (つまり、**IsPublic** が **Yes** に設定されているエンティティ) が適切に保護され、データが破損しないようにすることです。 この保護がないエンティティがある場合は、この状況はエンティティのバグを表します。 OData と仮想エンティティ間でエンティティの動作に違いがある場合は、仮想エンティティ機能のバグを示しています。

### <a name="if-i-develop-a-new-finance-and-operations-entity-and-want-to-see-it-in-dataverse-do-i-have-to-select-refresh-entity-list-in-finance-and-operations-do-i-have-to-do-anything-in-dataverse"></a>新しい Finance and Operations エンティティを作成し、それを Dataverse に表示する場合 、Finance and Operationsで [エンティティの更新] リストを選択する必要はありますか。 Dataverse で何かを行う必要はありますか。

理論的には、エンティティの一覧を更新する必要はありません。 通常は、Application Object Server (AOS) の実行場所に応じて、インターネット インフォメーション サービス (IIS) をリセットするか、IIS Express を再起動するだけでかまいません。 エンティティの一覧は、プロセスごとのキャッシュである SysGlobalObjectCache にキャッシュされるということになります。 このキャッシュにリストが正確であると示されていない場合は、リストが再構築されます。 リビルド プロセスには約 5 秒かかります。 したがって、AOS プロセス (w3wp.exe または iisexpress.exe) を再起動すると、リストは次に Dataverse から照会されるときに正確になります。 また、リコンパイルは SysGlobalObjectCache キャッシュをフラッシュする *必要があります* が、そうでない場合もあります。 この場合、AOS を再起動すると、それがフラッシュされます。

### <a name="do-you-have-guidance-on-when-to-use-a-virtual-entity-and-when-to-use-dual-write"></a>いつ仮想エンティティを使用するか、いつ二重書き込みを使用するかについてのガイダンスはありますか?

二重書き込みは、データが Dataverse にネイティブに存在する必要があるいくつかの主要なデータエンティティに対してのみ提供されます。 これらのデータ エンティティは、仮想エンティティとしては使用できません。

### <a name="when-adding-records-using-virtual-entities-is-there-any-way-to-use-number-sequences"></a>仮想エンティティを使用してレコードを追加する場合、番号順序を使用する方法はありますか?
はい、Finance and Operations エンティティで番号順序が自動生成される場合は、仮想エンティティからも同じように機能します。

### <a name="why-does-search-view-not-work-in-power-apps"></a>Power Apps で「検索ビュー」が機能しないのはなぜですか?
エンティティの簡易検索ビューにフィールドが追加されていない場合、検索ボックスは使用できません。 回避策として、エンティティのフィールドを 1 つ以上、簡易検索ビューに追加することができます。




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]