---
title: Dynamics 365 for Talent から Dynamics 365 for Finance and Operations への統合に関する FAQ
description: このトピックでは、Talent および Finance and Operations の統合でどのデータが同期されるのかについて説明します。
author: andreabichsel
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 438c2b5689e450b9aae9c55168993f2ee84be4d5
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518511"
---
# <a name="dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations-integration-faq"></a>Dynamics 365 for Talent から Dynamics 365 for Finance and Operations への統合に関する FAQ

[!include [banner](includes/banner.md)]

このトピックでは、Dynamics 365 for Talent が Dynamics 365 for Finance and Operations に統合される際にどのデータが同期されるかに関連した一般的な質問に回答します。

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>すべてのデータが同期された、または一部のデータ エンティティだけが同期されましたか。

Core Human Resources (HR) で、データのサブセットが同期されます。 すべてのエンティティの一覧については、「[Dynamics 365 for Talent から Dynamics 365 for Finance and Operations への統合](talent-financeandoperations-integration.md)」を参照してください。

Attract および Onboard に関しては、すべてのデータが Common Data Service にネイティブです。

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>テンプレートを使用せずに新しいマップを作成できますか。

テンプレートは、開始点です。 独自のテンプレートを作成できますが、テンプレートは統合プロジェクトを作成する際に常に必要です。 データ統合 (DI)、テンプレート、およびプロジェクトの詳細については、「[Common Data Service へデータを統合](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)」を参照してください。

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance-and-operations"></a>Talent および Finance and Operations 間で転送する財務分析コードをマップできますか。

財務分析コードは、現在 Common Data Service にはなく、結果として既定のテンプレートの一部ではありません。 このエンティティは計画されていますが、現在利用可能なリリース タイムラインはありません。

Finance and Operations で存在しますが、Talent では存在しないデータに関しては、Talent の**リンクの構成**を使用して 2 つのシステムを相互にリンクします。 Talent および Finance and Operations 間のリンクを構成する方法の詳細については、「[Dynamics 365 for Talent Core HR (2018 年 10月 31日) の新機能および変更された機能](whats-new-talent-october-31.md)」を参照してください。

![](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-and-operations-why"></a>場合によっては、従業員をインポートする場合 Finance and Operations の無効な作業者に入ってしまいます。 なぜですか。

従業員が Talent に有効な雇用詳細レコードがない場合、このエラーが発生する可能性があります。 この問題を解決するには、**人事管理 \> 従業員 \> 雇用履歴 \> 日付マネージャー**に移動し、有効な雇用詳細レコードがあることを確認します。

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>フィールドのサブセットのみをマップする選択をする場合、非マップ フィールドに対して加えた変更は同期をトリガーしますか。

データ同期は、実行スケジュールに従います。 このフィールドが統合マッピングの一部であるかどうかにかかわらず、レコードの任意のフィールドが変更されると、統合はレコードを選択します。

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>有効な作業者のみの変更を送信し、終了したレコードを送信しないためにはどうしますか。

「高度なクエリ」を使用して、ソースデータを送信先に渡す前に、フィルター処理して再作成できます。

![](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-and-operations-for-a-specific-entity"></a>特定のエンティティの Finance and Operations に送信するフィールドを指定できますか。

フィールドは、統合タスクから追加または削除できます。 Common Data Service エンティティに存在するすべてのデータ フィールドが、Core HR から入力されるわけではありません。
追加のデータは、PowerApps 経由で入力されます。

![](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>バッチ ジョブとしての統合を設定しましたが、Talent は宛先システムへの接続を失いました。 宛先システムに同じ一連の変更をどのように送信しますか。

例外処理の特別なセットアップは必要ではありません。 データ統合は自動的にソースと宛先で発生したエラーを検出して報告し、手動での再試行を許可します。 ただし、手動でのデータ修正は許可しません。 データの更新が必要な場合、ソースまたは宛先のいずれかで発生します。

## <a name="can-i-set-up-bi-directional-integration"></a>双方向の統合を設定できますか。

いいえ、統合は現在一方向です (Talent から Finance and Operations)。 ただし、Talent から Finance and Operations にデータを送信可能な既定のテンプレートがあります。

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>自分の統合の一部として、レコードの削除を許可できますか。

いいえ、データ統合は、データ転送の削除したレコードをキャプチャしません。 データ作成と更新 (UPSERT) のみが現在含まれます。

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>エラーの実行を再実行できますか。 その場合は、送信されるのは完全なファイルまたは変更のみですか。

データ統合の最初の実行は、常に完全な実行です。 その後の実行は、変更追跡に基づいています。 エラー実行が実行されると、実行のスコープのレコードを抽出し、Common Data Service から最新の変更を送信します。

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>プロジェクトを保存すると、エラーが発生します:「プロジェクトにはマッピング エラーがあります。」 何をしたらいいですか ?

統合キーの設定を確認し、設定に必要などんな変更も加えてから、プロジェクトでエンティティを更新します。

既定のテンプレートを使用すると、統合キーは自動的にインポートされます。 この問題は、新しいタスクが既存のテンプレートに追加されたときに発生する可能性があります。

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>作業者の雇用がある法人の N 番号がある場合、それぞれに対するマップを作成する必要がありますか。

はい、Finance and Operations の各法人に対して、データ統合の統合プロジェクトを分ける必要があります。

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Microsoft により提供された既定のテンプレートの一部ではないデータを転送する必要があります。 これを実行できますか ?

はい、フィールドは既存のテンプレートから追加または削除できます。 テンプレートを変更して、他の Common Data Service のエンティティからの追加データを含めます。 エンティティは、テンプレートに含まれる Common Data Service である必要があります。 

## <a name="i-just-created-new-finance-and-operations-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>新しい Finance and Operations、および Talent 環境を作成しましたが、エラーが発生しました。「データ値が、整合性制約に違反しています。」 なぜですか。

このエラーが発生する理由には以下が含まれます。

- データ転送がなかったため、転送ソース (Common Data Service) で重複レコードの抽出となりました。

- データ転送には、Finance and Operations で必要とされるフィールドの null 値があります。 Common Data Service にあり、Finance and Operations の要件を満たすデータを確認します。

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>実行エラーがあり従業員 ID が同期しなかった場合、失敗した従業員レコードがある履歴ジョブをどのように見つけますか。

データ統合は、Finance and Operations で複数のプロジェクトを作成します。 データ統合タスクと Finance and Operations プロジェクトとの関係は、1 対 1 です。

データ統合実行履歴からの時間を追跡し、Finance and Operations でインデックス -1 プロジェクトを検索します。 データ統合でタスク番号が 9 の場合、Finance and Operations のインデックスは 8 です。

1. データ統合からタスク インデックスをキャプチャします (この例では「9」)。

![データ統合からタスク インデックスをキャプチャします。](media/CaptureTaskIndex.png)

2. プロジェクトの実行時間を追跡します。

![プロジェクトの実行時間の追跡](media/CaptureTimeOfExecution.png)

3. Finance and Operations で、インデックス - 1 を識別します。 この例では、接尾語「8」でインデックス「0」プロジェクトの実行時間を持つプロジェクトは、ステップ 2 の実行時間と一致します。

![インデックスの識別](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-and-operations-i-dont-see-my-talent-data-in-finance-and-operations-what-do-i-do"></a>Talent および Finance and Operations を統合した後、Finance and Operations で Talent データが表示されません。 何をしたらいいですか ?

Finance and Operations への統合には 2 つのステップがあります。 まず、Talent データが更新済で、Common Data Service で利用可能であることを確認します。 これはほぼリアルタイムの同期であり、データ エンティティ内のデータを参照して PowerApps で検証できます。

![Common Data Service 内のデータ](media/DataInCDS.png)

Common Data Service で予定どおりにデータが表示されない場合は、エンティティが統合でサポートされていることを確認します。 Common Data Service に追加データを含めるには、Microsoft 側で変更が必要です。

エンティティがサポートされデータが Common Data Service で使用できる場合は、データ統合でマッピングが正しいことを確認します。 インテグレーター マッピングが正常に見える場合、データ管理ジョブが正常に実行されたことを確認します。 バッチ ジョブの実行中にエラーが発生する可能性があります。 データ管理の詳細については、「[データ管理](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)」を参照してください。

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-and-operations-what-should-i-do"></a>Finance and Operations にインポートした後、従業員の住所が正しくありません。 何をする必要がありますか。

**場所 ID** の番号順序は、Talent および Finance and Operations の両方で同じパターンを使用します。 Common Data Service から Finance and Operations にデータを統合する場合、アドレスの衝突がないように、番号順序は両側で一意である必要があります。

Talent の実装中に、番号順序が Talent および Finance and Operations で同じではないことを確認します。 データが両方のシステムで維持される可能性がある場合は、すべての番号順序が同一でないことを検証します。

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>接続設定を作成する際に、接続ドロップダウン リストで接続が確認できません。 何をしたらいいですか ?

接続を作成するときは、Dynamics 365 for Finance and Operations (現在のプレビュー) および Common Data Service を選択していることを確認してください。

## <a name="when-syncing-employments-i-get-the-errors-companyinfofk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>雇用を同期する際、エラーが発生します。「CompanyInfo_FK が存在しません」または「フィールド '雇用終了日' の値 '12/31/2154 11:59:59 pm' が、関連するテーブル '雇用' で見つかりません。」何をする必要がありますか。

正しい法人にマッピングしていることを確認します。 法人の同期は既定のテンプレートの一部ではないため、Talent や Common Data Service に存在する各法人が Finance and Operations にも存在することが予想されます。
また、関連付けられている接続設定に対して正しい法人を選択していることを確認してください。

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-and-operations-appears-to-be-empty-what-should-i-do"></a>プロジェクトの設定後、Finance and Operations のフィールド マッピングは空のようです。 何をする必要がありますか。

**データ管理 \> フレームワーク パラメーター \> エンティティ設定 \> エンティティ リストの更新**に移動して、Finance and Operations のデータ エンティティを更新します。 これは数分で完了し、それらのマッピングを表示できます。 新しいプロジェクトが作成されたときに、この問題が発生します。

![フィールド マッピングがありません](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>追加リソース

- データ統合 (DI): 

  - [データを Common Data Service に統合](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)

  - [データ統合エラーの管理とトラブルシューティング](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator-error-management)

  - [PowerApps、Microsoft Flow、および Common Data Service でシステムにより生成されたログの DSR 要求への応答](https://docs.microsoft.com/en-us/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- データ管理:

  - [データ管理](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
