---
title: インスタンスのコピー
description: Microsoft Dynamics Lifecycle Services (LCS) を使用して、Microsoft Dynamics 365 Human Resources データベース をサンドボックス環境にコピーすることができます。
author: andreabichsel
manager: tfehr
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e38abf3537d88bb147fbf0030999953025e5820f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466907"
---
# <a name="copy-an-instance"></a>インスタンスのコピー

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics Lifecycle Services (LCS) を使用して、Microsoft Dynamics 365 Human Resources データベース をサンドボックス環境にコピーすることができます。 別のサンドボックス環境を使用する場合は、その環境から対象のサンドボックス環境にデータベースをコピーすることもできます。

インスタンスをコピーする際には、次のヒントを念頭に置いてください :

- 上書きを行う Human Resources インスタンスは、サンドボックス環境である必要があります。

- コピー元とコピー先の環境は同じリージョン内にある必要があります。 異なるリージョン間でのコピーはできません。

- 対象の環境の管理者である必要があります。そうすることでコピー後のインスタンスにサイン インすることができます。

- Human Resources データベースをコピーする際は、 Microsoft Power Apps 環境に含まれる要素 (アプリやデータ) のコピーをしないでください。 Power Apps 環境の各要素のコピー方法については、 [環境をコピーする](https://docs.microsoft.com/power-platform/admin/copy-environment) を参照してください。 上書きを行う Power Apps 環境 は、サンドボックス環境である必要があります。 Power Apps の運用環境をサンドボックス環境に変更するには、グローバル テナントの管理者である必要があります。 Power Apps 環境の変更に関する詳細については、 [インスタンスを切り替える](https://docs.microsoft.com/dynamics365/admin/switch-instance) を参照してください。

- サンドボックス環境にインスタンスをコピーしてサンドボックス環境を Dataverse と統合する場合は、ユーザー設定フィールドを Dataverse テーブルに再適用する必要があります。 [カスタムフィールドを Dataverse に適用する](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service)を参照してください 。

## <a name="effects-of-copying-a-human-resources-database"></a>Human Resources データベースのコピーによる影響

Human Resources データベースのコピーをする際に、次のイベントが発生します。

- コピーの過程で、対象とする環境の既存のデータベースが削除されます。 コピーの完了後は、既存のデータベースを復元することはできません。

- 対象とする環境は、コピーが完了するまで使用することができません。

- Microsoft Azure Blob storage 内のドキュメントは環境間でのコピーがされません。 そのため、この ストレージ に属するドキュメントやテンプレートはコピーされず、コピー元の環境に残ります。

- 管理者ユーザー、およびその他の内部サービス ユーザー アカウントを除くすべてのユーザーは使用できなくなります。 管理者ユーザーは他のユーザーがシステムに復帰する前にデータの削除や難読化することができます。

- 管理者ユーザーは、特定のサービスまたは URL に統合エンドポイントを再接続するなど、必要な構成の変更を加える必要があります。

## <a name="copy-the-human-resources-database"></a>Human Resources データベースのコピー

このタスクを完了するには、最初にインスタンスをコピーして、続いて Microsoft Power Platform 管理センターを Power Apps 環境へとコピーします。

> [!WARNING]
> インスタンスのコピーを行うと、対象となるインスタンスのデータベースが削除されます。 対象のインスタンスをこの処理中に使用することはできません。

1. LCS にサインインし、コピーをするインスタンスを含む LCS プロジェクトを選択します。

2. LCS プロジェクトでは、**人事管理アプリの管理** タイルを選択します。

3. コピーをするインスタンスを選択して、**コピー** を選択します。

4. **インスタンスをコピーする** のタスク ウィンドウで、上書きするインスタンスを選択し、続いて **コピー** を選択します。 **コピーのステータス** フィールドの値が **完了** となるまで待機してください。

   ![[上書きするインスタンスを選択します](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. **Power Platform** を選択し、 Microsoft Power Platform 管理センターにサインインします。

   ![[Power Platformを選択します](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. コピーをするPower Apps 環境 を選択して、 **コピー** を選択します。

7. コピー処理の完了後、対象のインスタンスにサインインし、 Dataverse 統合を有効化します。 詳細情報と解説については、 [Dataverse の統合を構成する](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration) を参照してください。

## <a name="data-elements-and-statuses"></a>データの属性と状態

次のデータ要素は、Human Resources インスタンスのコピーを行う際にコピーされません。

- **LogisticsElectronicAddress** テーブルの電子メールアドレス

- **BatchJobHistory**、 **BatchHistory**、 **BatchConstraintHistory** テーブル内のバッチジョブ履歴

- **SysEmailSMTPPassword** テーブル内の Simple Mail Transfer Protocol (シンプル メール トランスファー プロトコル、SMTP) のパスワード

- **SysEmailParameters** テーブル内の SMTP リレーサーバー

- **PrintMgmtSettings** と **PrintMgmtDocInstance** テーブル内 の 印刷管理設定

- **SysServerConfig**、 **SysServerSessions**、 **SysCorpNetPrinters**、 **SysClientSessions**、 **BatchServerConfig**、 **BatchServerGroup** テーブル内の環境固有のレコード

- DocuValue テーブル内のドキュメント添付ファイル。 コピー元の環境で上書きされた Microsoft Office のテンプレートを含む要素

- **PersonnelIntegrationConfiguration** テーブル内の接続文字列

これらの要素は、環境固有のものであるためコピーされません。 **BatchServerConfig** と **SysCorpNetPrinters** のレコードを含む例。 その他の要素は、サポート チケットのデータ量が多くなる懸念があるためコピーされません。 例:

- 重複した電子メールは、SMTP がユーザー受け入れテスト (サンドボックス) 環境で有効になっている場合に送信される可能性があります。

- バッチジョブが有効な場合、無効な統合メッセージが送信される可能性があります。

- 管理者が更新後のクリーンアップ アクションを実行する前に、ユーザーが有効化される場合があります。

また、インスタンスのコピー時には、次の状態変更がされます :

- 管理者以外の全ユーザーが **無効化** されます。

- 一部のシステムジョブを除いた、すべてのバッチジョブが **保留** となります。

## <a name="environment-admin"></a>環境管理者

対象となるサンドボックス環境の、管理者を含む全ユーザーが、コピー元のユーザーに置き換えられます。 インスタンスのコピーの実行者は、自分にソース環境で管理者の権限があることを確認してください。 管理者の権限がない場合は、コピーの完了後に対象のサンドボックス環境にサイン インすることができません。

コピー先のサンドボックス環境内の全ての非管理者ユーザーは無効化され、サンドボックス環境へと不必要なログインができません。 システム管理者は、必要に応じてユーザーを有効化することができます。

## <a name="apply-custom-fields-to-dataverse"></a>カスタム フィールドを Dataverse に適用する

サンドボックス環境にインスタンスをコピーしてサンドボックス環境を Dataverse と統合する場合は、ユーザー設定フィールドを Dataverse テーブルに再適用する必要があります。

Dataverse テーブルに表示されるユーザー設定フィールドごとに、次の手順を実行します :

1. カスタム設定フィールドに移動して、**編集** を選択し ます。

2. ユーザー設定フィールドが有効になっている各 "cdm_* エンティティ" の **有効** フィールドをオフにします。

3. **変更を適用する** を選択します。

4. 再度 **編集** を選択します。

5. ユーザー設定フィールドが有効になっている各 "cdm_* エンティティ" の **有効** フィールドをオンにします。

6. 再度 **変更を適用する** を選択します。

選択解除、変更の適用、再選択、変更の再適用を行うプロセスでは、カスタム フィールドを含むように Dataverse でスキーマを更新するように促されます。

カスタム フィールドについての詳細については、[カスタム フィールドの作成と操作](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields) を参照してください。

## <a name="see-also"></a>参照

[Human Resources のプロビジョニング](hr-admin-setup-provision.md)</br>
[インスタンスの削除](hr-admin-setup-remove-instance.md)</br>
[更新プロセス](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]