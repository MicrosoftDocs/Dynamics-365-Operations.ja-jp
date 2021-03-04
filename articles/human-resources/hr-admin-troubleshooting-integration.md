---
title: Finance FAQ との統合
description: この記事では、人事管理および Finance 統合でどのデータが同期されるのかについて説明します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6a94c1269cd81ecdcbdff018ec4a8f90be36f0f3
ms.sourcegitcommit: 6aa8d6aa8276611967fb6fab44715950de49f6af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2020
ms.locfileid: "4589066"
---
# <a name="integration-with-finance-faq"></a>Finance FAQ との統合

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Human Resources が Dynamics 365 Finance に統合される際にどのデータが同期されるかに関連した一般的な質問に回答します。

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a>Power Apps で Dynamics 365 Talent アプリケーションを編集することはできますか。

No. Talent アプリケーション ユーザーを編集すると、Human Resources と Common Data Service の統合に失敗する可能性があります。 次のテーブルでは、Talent アプリケーション ユーザーに対する既定の設定を表示しています。

| 姓名 | アプリケーション ID | Azure AD オブジェクト ID | アプリケーション ID URI |
| --- | --- | --- | --- |
| Dynamics 365 for Talent | f9be0c49-aa22-4ec6-911a-c5da515226ff | 27fd8129-4b3c-43f7-b1bf-47495d3a049b | f9be0c49-aa22-4ec6-911a-c5da515226ff |

![Talent アプリケーション ユーザーに対する既定の設定](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>すべてのデータが同期された、または一部のデータ エンティティだけが同期されましたか。

データのサブセットが同期されます。 すべてのエンティティの一覧については、[ Dynamics 365 Finance との統合](hr-admin-integration-finance.md) 参照してください。

## <a name="why-dont-i-see-any-data-synced-to-common-data-service"></a>Common Data Service に同期されたデータを表示できないのはなぜですか?

既定では、Common Data Service の統合は、提供されているデモ データが含まれていない新しい環境ではオフになっています。 既定では、デモ データが含まれている新しい環境ではオンになっており、環境の準備時にデータの同期が開始されます。 データと同期する準備が整ったら、統合をオンにすることができます。 詳細については、[Common Data Service 統合のコンフィギュレーション](hr-admin-integration-common-data-service.md) を参照してください。

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>テンプレートを使用せずに新しいマップを作成できますか。

テンプレートは、開始点です。 独自のテンプレートを作成できますが、テンプレートは統合プロジェクトを作成する際に常に必要です。 データ統合 (DI)、テンプレート、およびプロジェクトの詳細については、「[Common Data Service へデータを統合](https://docs.microsoft.com/powerapps/administrator/data-integrator)」を参照してください。

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a>人事管理および Finance 間で転送する財務分析コードをマップできますか?

財務分析コードは、現在 Common Data Service にはなく、結果として既定のテンプレートの一部ではありません。 このエンティティは計画されていますが、現在利用可能なリリース タイムラインはありません。

Finance and Operations で存在しますが、人事管理では存在しないデータに関しては、人事管理 **リンクの構成** を使用して 2 つのシステムを相互にリンクします。

![財務分析コードのマップ](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a>場合によっては、従業員をインポートする場合 Finance の無効な作業者に入ってしまいます。 なぜですか。

従業員が人事管理に有効な雇用詳細レコードがない場合、このエラーが発生する可能性があります。 この問題を解決するには、**人事管理 \> 従業員 \> 雇用履歴 \> 日付マネージャー** に移動し、有効な雇用詳細レコードがあることを確認します。

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>フィールドのサブセットのみをマップする選択をする場合、非マップ フィールドに対して加えた変更は同期をトリガーしますか。

データ同期は、実行スケジュールに従います。 このフィールドが統合マッピングの一部であるかどうかにかかわらず、レコードの任意のフィールドが変更されると、統合はレコードを選択します。

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>有効な作業者のみの変更を送信し、終了したレコードを送信しないためにはどうしますか。

「高度なクエリ」を使用して、ソースデータを送信先に渡す前に、フィルター処理して再作成できます。

![有効な作業者の高度なクエリ](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a>特定のエンティティの Finance に送信するフィールドを指定できますか。

フィールドは、統合タスクから追加または削除できます。 Common Data Service エンティティに存在するすべてのデータ フィールドが、人事管理から入力されるわけではありません。
追加のデータは、Power Apps 経由で入力されます。

![統合タスクへ (から) フィールドを追加または削除します](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>バッチ ジョブとしての統合を設定しましたが、人事管理は宛先システムへの接続を失いました。 宛先システムに同じ一連の変更をどのように送信しますか。

例外処理の特別なセットアップは必要ではありません。 データ統合は自動的にソースと宛先で発生したエラーを検出して報告し、手動での再試行を許可します。 ただし、手動でのデータ修正は許可しません。 データの更新が必要な場合、ソースまたは宛先のいずれかで発生します。

## <a name="can-i-set-up-bi-directional-integration"></a>双方向の統合を設定できますか。

いいえ、統合は現在一方向 (Finance and Operations への人事管理) です。 ただし、人事管理から Finance にデータを送信可能な既定のテンプレートがあります。

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>自分の統合の一部として、レコードの削除を許可できますか。

いいえ、データ統合は、データ転送の削除したレコードをキャプチャしません。 データ作成と更新 (UPSERT) のみが現在含まれます。

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>エラーの実行を再実行できますか。 その場合は、送信されるのは完全なファイルまたは変更のみですか。

データ統合の最初の実行は、常に完全な実行です。 その後の実行は、変更追跡に基づいています。 エラー実行が実行されると、実行のスコープのレコードを抽出し、Common Data Service から最新の変更を送信します。

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>プロジェクトを保存すると、エラーが発生します:「プロジェクトにはマッピング エラーがあります。」 何をしたらいいですか ?

統合キーの設定を確認し、設定に必要などんな変更も加えてから、プロジェクトでエンティティを更新します。

既定のテンプレートを使用すると、統合キーは自動的にインポートされます。 この問題は、新しいタスクが既存のテンプレートに追加されたときに発生する可能性があります。

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>作業者の雇用がある法人の N 番号がある場合、それぞれに対するマップを作成する必要がありますか。

はい、Finance の各法人に対して、データ統合の統合プロジェクトを分ける必要があります。

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Microsoft により提供された既定のテンプレートの一部ではないデータを転送する必要があります。 これを実行できますか ?

はい、フィールドは既存のテンプレートから追加または削除できます。 テンプレートを変更して、他の Common Data Service のエンティティからの追加データを含めます。 エンティティは、テンプレートに含まれる Common Data Service である必要があります。 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>新しい Finance および人事管理環境を作成しましたが、「データ値が、整合性制約に違反しています」というエラーが発生しました。 なぜですか。

このエラーが発生する理由には以下が含まれます。

- データ転送がなかったため、転送ソース (Common Data Service) で重複レコードの抽出となりました。

- データ転送には、Finance and Operations で必要とされるフィールドの Null 値があります。 Common Data Service にあり、Finance and Operations の要件を満たすデータを確認します。

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>実行エラーがあり従業員 ID が同期しなかった場合、失敗した従業員レコードがある履歴ジョブをどのように見つけますか。

データ統合は、Finance で複数のプロジェクトを作成します。 データ統合タスクと Finance プロジェクトとの関係は、1 対 1 です。

データ統合実行履歴からの時間を追跡し、Finance でインデックス -1 プロジェクトを検索します。 データ統合でタスク番号が 9 の場合、Finance のインデックスは 8 です。

1. データ統合からタスク インデックスをキャプチャします (この例では「9」)。

    ![データ統合からタスク インデックスをキャプチャします。](media/CaptureTaskIndex.png)

2. プロジェクトの実行時間を追跡します。

    ![プロジェクトの実行時間の追跡](media/CaptureTimeOfExecution.png)

3. Finance では、インデックス - 1 を識別します。 この例では、接尾語「8」でインデックス「0」プロジェクトの実行時間を持つプロジェクトは、ステップ 2 の実行時間と一致します。

    ![インデックスの識別](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a>人事管理と Finance を統合した後、財務の人事管理データは表示されません。 何をしたらいいですか ?

Finance への統合には 2 つのステップがあります。 まず、人事管理データが更新済で、Common Data Service で利用可能であることを確認します。 これはほぼリアルタイムの同期であり、データ エンティティ内のデータを参照して Power Apps で検証できます。

![Common Data Service 内のデータ](media/DataInCDS.png)

Common Data Service で予定どおりにデータが表示されない場合は、エンティティが統合でサポートされていることを確認します。 Common Data Service に追加データを含めるには、Microsoft 側で変更が必要です。

エンティティがサポートされデータが Common Data Service で使用できる場合は、データ統合でマッピングが正しいことを確認します。 インテグレーター マッピングが正常に見える場合、データ管理ジョブが正常に実行されたことを確認します。 バッチ ジョブの実行中にエラーが発生する可能性があります。 データ管理の詳細については、「[データ管理](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)」を参照してください。

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a>Finance にインポートした後、従業員の住所が正しくありません。 何をする必要がありますか。

**場所 ID** の番号順序は、人事管理および Finance の両方で同じパターンを使用します。 Common Data Service から Finance and Operations にデータを統合する場合、アドレスの衝突がないように、番号順序は両側で一意である必要があります。

人事管理の実装中に、番号順序が人事管理および Finance and Operations で同じではないことを確認します。 データが両方のシステムで維持される可能性がある場合は、すべての番号順序が同一でないことを検証します。

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>接続設定を作成する際に、接続ドロップダウン リストで接続が確認できません。 何をしたらいいですか ?

接続を作成するときは、Dynamics 365 Finance および Common Data Service を選択していることを確認してください。

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>雇用を同期する際、エラーが発生します。「CompanyInfo_FK が存在しません」または「フィールド '雇用終了日' の値 '12/31/2154 11:59:59 pm' が、関連するテーブル '雇用' で見つかりません。」何をする必要がありますか。

正しい法人にマッピングしていることを確認します。 法人の同期は既定のテンプレートの一部ではないため、人事管理や Common Data Service に存在する各法人が Finance にも存在することが予想されます。
また、関連付けられている接続設定に対して正しい法人を選択していることを確認してください。

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a>プロジェクトの設定後、Finance のフィールド マッピングは空のようです。 何をする必要がありますか。

**データ管理 \> フレームワーク パラメーター \> エンティティ設定 \> エンティティ リストの更新** に移動して、Finance のデータ エンティティを更新します。 これは数分で完了し、それらのマッピングを表示できます。 新しいプロジェクトが作成されたときに、この問題が発生します。

![フィールド マッピングがありません](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>追加リソース

- データ統合 (DI): 

  - [データを Common Data Service に統合](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [データ統合エラーの管理とトラブルシューティング](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [Power Apps、Microsoft Power Automate、および Common Data Service でシステムにより生成されたログの DSR 要求への応答](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- データ管理:

  - [データ管理](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]