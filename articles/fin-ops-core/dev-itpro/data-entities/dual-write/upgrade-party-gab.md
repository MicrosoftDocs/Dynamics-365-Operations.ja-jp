---
title: 当事者およびグローバル アドレス帳モデルへのアップグレード
description: このトピックでは、二重書き込みデータを当事者およびグローバル アドレス帳モデルにアップグレードする方法について説明します。
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 673c3a68e2eccdabdfc2df281389537297ec3524bee5e744e910c50d38b8d298
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720691"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>当事者およびグローバル アドレス帳モデルへのアップグレード

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[Microsoft Azure Data Factory テンプレート](https://aka.ms/dual-write-gab-adf) を使用すると、既存の **取引先企業**、**連絡先**、および **仕入先** テーブル データを当事者およびグローバル アドレス帳モデルに二重書き込みでアップグレードできます。 テンプレートでは、Finance and Operations アプリおよび Customer Engagement アプリケーションの両方からのデータを調整します。 このプロセスの終了時に、**当事者** レコードの **当事者** および **連絡先** が作成され、Customer Engagement アプリケーションの **取引先企業**、**連絡先**、および **仕入先** レコードに関連付けされます。 .csv ファイル (`FONewParty.csv`) が生成され、Finance and Operations アプリ内に新しい **当事者** レコードが作成されます。 このトピックでは、Data Factory テンプレートを使用し、データをアップグレードする方法について説明します。

カスタマイズを実行しない場合は、テンプレートを現状のままで使用できます。 **取引先企業**、**連絡先**、および **仕入先** をカスタマイズする場合は、次の手順に従ってテンプレートを変更する必要があります。

> [!NOTE]
> テンプレートは、**当事者** データのみをアップグレードします。 将来のリリースでは、郵便番号および電子住所が含まれる予定です。

## <a name="prerequisites"></a>必要条件

当事者およびグローバル アドレス帳モデルにアップグレードするには、次の前提条件を満たしている必要があります:

+ [Azure サブスクリプション](https://portal.azure.com/)
+ [テンプレートへのアクセス](https://aka.ms/dual-write-gab-adf)
+ 既存の二重書き込み顧客である必要があります。

## <a name="prepare-for-the-upgrade"></a>アップグレードの準備
アップグレードの準備には、次の活動が必要です:

+ **完全同期**: 両方の環境は、**取引先企業 (顧客)**、**連絡先**、および **仕入先** に対して完全に同期された状態です。
+ **統合キー**: Customer Engagement アプリの **取引先企業 (顧客)**、**連絡先**、および **仕入先** テーブルは、すぐに出荷される統合キーを使用しています。 統合キーをカスタマイズした場合は、テンプレートをカスタマイズする必要があります。
+ **当事者番号**: すべてのアップグレードされる **取引先企業 (顧客)**、**連絡先**、および **仕入先** レコードには **当事者** 番号があります。 **当事者** 番号のないレコードは無視されます。 これらのレコードをアップグレードする場合は、アップグレード プロセスを開始する前にレコードに **当事者** 番号を追加します。
+ **システム停止**: アップグレード プロセス中は、Finance and Operations および Customer Engagement 環境の両方をオフラインにする必要があります。
+ **スナップショット**: Finance and Operations および Customer Engagement アプリ両方のスナップショットを作成します。 必要に応じて、スナップショットを使用して以前の状態を復元します。

## <a name="deployment"></a>配置

1. テンプレートを [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf) からダウンロードします。

2. [Microsoft Azure](https://portal.azure.com/) にログインします。

3. [リソース グループ](/azure/azure-resource-manager/management/manage-resource-groups-portal)を作成します。

4. 作成したリソース グループに[ストレージ アカウント](/azure/storage/common/storage-account-create?tabs=azure-portal)を作成します。

5. 作成した上記のリソース グループに[データ ファクトリー](/azure/data-factory/quickstart-create-data-factory-portal)を作成します。

6. データ ファクトリーを開き、**作成者 & モニター** タイルを選択します。

7. **管理** タブで、**ARM テンプレート** を選択します。

8. **ARM テンプレートをインポートする** を選択して、**当事者** テンプレートをインポートします。

9. テンプレートをデータ ファクトリーにインポートします。 **プロジェクトの詳細** および **インスタンスの詳細** に対して次の値を入力します。

    フィールド | 先頭値
    ---|---
    サブスクリプション | Azure サブスクリプション
    リソース グループ | ストレージ アカウントを作成されるのと同じリソースを提供します。
    リージョン | リージョンを指定します。
    ファクトリー名 | ファクトリー名を指定します。
    FO リンクされた Service_service プリンシパル キー | アプリケーション キーを指定します。
    Azure Blob Storage_connection 文字列 | Azure Blob Storage の接続文字列。
    Dynamics CRM リンクされた Service_password | ユーザー名として指定したユーザー アカウントのパスワード。
    FO リンクされた Service_properties_type Properties_url  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    FO リンクされた Service_properties_type Properties_tenant | アプリケーションが存在するテナント情報 (ドメイン名またはテナント ID) を指定します。
    FO リンクされた Service_properties_type Properties_aad リソース ID | `https://sampledynamics.sandboxoperationsdynamics.com`
    FO リンクされた Service_properties_type Properties_service プリンシパル ID | アプリケーションのクライアント ID を指定します。
    Dynamics CRM リンクされた Service_properties_type Properties_username | Dynamics 365 に接続する username。

    詳細については、次のトピックを参照してください: 
    
    - [各環境の Resource Manager テンプレートの手動促進](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [リンクされたサービス プロパティ](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Azure Data Factory を使用したデータのコピー](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. 配置後に、データ ファクトリのデータセット、データ フロー、およびリンクされたサービスを検証します。

   ![データセット、データ フロー、およびリンクされたサービス。](media/data-factory-validate.png)

11. **管理** に移動します。 **接続** で、**リンクされたサービス** を選択します。 **DynamicsCrmLinkedService** を選択します。 **リンクされたサービスの編集 (Dynamics CRM)** フォームに、次の値を入力します。

    フィールド | 先頭値
    ---|---
    氏名 | DynamicsCrmLinkedService
    説明 | エンティティ データをフェッチする CRM インスタンスに接続するリンクされたサービス
    統合ランタイム経由の接続 | AutoResolvelntegrationRuntime
    配置のタイプ | オンライン
    サービス URI | `https://<organization-name>.crm[x].dynamics.com`
    認証タイプ | Office365
    ユーザー名 |
    パスワードまたは Azure Key Vault | パスワード
    パスワード |

## <a name="run-the-template"></a>テンプレートの実行

1. Finance and Operations アプリを使用して、次の **取引先企業**、**連絡先**、および **仕入先** の二重書き込みマップを停止します。

    + 顧客 V3 (アカウント)
    + 顧客 V3 (連絡先)
    + CDS 連絡先 V2 (連絡先)
    + CDS 連絡先 V2 (連絡先)
    + 仕入先 V2 (msdyn_vendors)

2. Dataverse で `msdy_dualwriteruntimeconfig` テーブルからマップが削除されたのを確認します。

3. AppSource から [二重書き込み当事者およびグローバル アドレス帳ソリューション](https://aka.ms/dual-write-gab)をインストールします 。

4. Finance and Operations アプリで、次のテーブルにデータが含まれている場合は、そのテーブルの **初期同期** を実行します。

    + あいさつ文
    + 個人の特徴タイプ
    + 結句
    + 連絡担当者の肩書き
    + 意思決定ロール
    + ロイヤルティ レベル

5. Customer Engagement アプリで、次のプラグイン ステップを無効にします。

    + 取引先企業の更新
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: 取引先企業の更新
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: 取引先企業の更新
    + 連絡先の更新
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: 連絡先の更新
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: 連絡先の更新
    + msdyn_party の更新
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party の更新
    + msdyn_vendor の更新
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor の更新

6. Customer Engagement アプリで、次のワークフローを無効にします:

    + 取引先企業テーブルでの仕入先の作成
    + 取引先企業テーブルでの仕入先の作成
    + 連絡先テーブルでの個人タイプの仕入先の作成
    + 仕入先テーブルでの個人タイプの仕入先の作成
    + 取引先企業テーブルでの仕入先の更新
    + 仕入先テーブルでの仕入先の更新
    + 取引先担当者テーブルでの個人タイプの仕入先の更新
    + 仕入先テーブルでの個人タイプの仕入先の更新

7. データ ファクトリーで、次の図に示すように **今すぐトリガーする** を選択してテンプレートを実行します。 このプロセスは、データ量に基づいて完了に数時間かかる場合があります。

    ![トリガーの実行。](media/data-factory-trigger.png)

    > [!NOTE]
    > **取引先企業**、**連絡先**、および **仕入先** をカスタマイズする場合は、テンプレートを変更する必要があります。

8. Finance and Operations アプリで新しい **当事者** レコードをインポートします。

    + Azure Blob Storage から `FONewParty.csv` ファイルをダウンロードします。 パスは `partybootstrapping/output/FONewParty.csv` です。
    + `FONewParty.csv` ファイルを Excel ファイルに変換し、Excel ファイルを Finance and Operations アプリにインポートします。 csv インポートが機能する場合は、csv ファイルを直接インポートできます。 データ量によっては、インポートの実行に数時間かかる場合があります。 詳細については、[データのインポート ジョブとエクスポート ジョブの概要](../data-import-export-job.md)を参照してください。

    ![Datavers 当事者レコードのインポート。](media/data-factory-import-party.png)

9. Customer Engagement アプリで、次のプラグイン ステップを有効にします:

    + 取引先企業の更新
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: 取引先企業の更新
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: 取引先企業の更新
    + 連絡先の更新
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: 連絡先の更新
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: 連絡先の更新
    + msdyn_party の更新
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party の更新
    + msdyn_vendor の更新
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor の更新

10. Customer Engagement アプリで、前の手順で次のワークフローを無効化した場合は、有効にします:

    + 取引先企業テーブルでの仕入先の作成
    + 取引先企業テーブルでの仕入先の作成
    + 連絡先テーブルでの個人タイプの仕入先の作成
    + 仕入先テーブルでの個人タイプの仕入先の作成
    + 取引先企業テーブルでの仕入先の更新
    + 仕入先テーブルでの仕入先の更新
    + 取引先担当者テーブルでの個人タイプの仕入先の更新
    + 仕入先テーブルでの個人タイプの仕入先の更新

11. [当事者およびグローバル アドレス帳](party-gab.md)の指示に従って **当事者** 関連のマップを実行します。

## <a name="troubleshooting"></a>トラブルシューティング

1. プロセスが失敗した場合は、失敗した活動から始めてデータ ファクトリを再実行します。
2. 一部のファイルは、データ検証の目的で使用できるデータ ファクトリによって生成されます。
3. データ ファクトリは、コンマ区切りされた csv ファイルに基づいて実行されます。 コンマを含むフィールド値がある場合は、結果に影響が出る場合があります。 コンマを削除する必要があります。
4. **監視** タブでは、すべてのステップおよび処理済みデータに関する情報が提供されます。 特定の手順を選択してデバッグします。

    ![監視タブ。](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>テンプレートの詳細を確認する

テンプレートに関する追加情報は、[Azure Data Factory テンプレートの readme のコメント](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) で確認できます。
