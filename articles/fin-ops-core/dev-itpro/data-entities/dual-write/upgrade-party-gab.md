---
title: 当事者およびグローバル アドレス帳モデルへのアップグレード
description: このトピックでは、二重書き込みデータを当事者およびグローバル アドレス帳モデルにアップグレードする方法について説明します。
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 579a7d19ee7196d3242c78bd9915df24ec479c31
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060488"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>当事者およびグローバル アドレス帳モデルへのアップグレード

[!include [banner](../../includes/banner.md)]



[Microsoft Azure Data Factory のテンプレート](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema)を使用すると、デュアルライトの既存データをパーティとグローバル アドレス帳モデル (**取引先企業**、**取引先担当者**、**ベンダー** テーブルのデータ、郵便、電子アドレス) にアップグレードすることができます。

データファクトリーのテンプレートには以下の 3 種類が用意されています。 財務と運用アプリおよび Customer Engagement アプリの両方からのデータを照合するのに役立ちます。

- **[パーティ テンプレート](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json) (データをデュアルライト パーティ GAB schema/arm_template.json にアップグレードします)** – このテンプレートは、**取引先企業**、**取引先担当者**、**ベンダー** データに関連付けられている **パーティ** および **取引先担当者** データのアップグレードに役立ちます。
- **[パーティの送付先住所](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json) (データをデュアルライト パーティ schema/Upgrade to Party Postal Address - GAB/arm_template.json にアップグレードします)** – このテンプレートは、**取引先企業**、**取引先担当者t**、**ベンダー** データに関連付けられている送付先住所のアップグレードに役立ちます。
- **[パーティの電子住所](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json) (データをデュアルライト パーティ schema/Upgrade to Party Postal Address - GAB/arm_template.json にアップグレードし、パーティの電子住所 GAB/arm_template.json にアップグレードします)** – このテンプレートは、**取引先企業**、**取引先担当者**、**ベンダー** データに関連付けられている電子住所のアップグレードに役立ちます。

プロセスの最後に、以下のカンマ区切りの値 (.csv) ファイルが生成されます。

| ファイル名 | 使用方法 |
|---|---|
| FONewParty.csv | このファイルは、財務と運用アプリ内で新しい **関係者** レコードの作成に使用します。 |
| ImportFONewPostalAddressLocation.csv | このファイルは、財務と運用アプリ内で新しい **配送先住所のロケーション** レコードの作成に使用します。 |
| ImportFONewPartyPostalAddress.csv | このファイルは、財務と運用アプリ内で新しい **関係者の住所** レコードの作成に使用します。 |
| ImportFONewPostalAddress.csv | このファイルは、財務と運用アプリ内で新しい **住所** レコードの作成に使用します。 |
| ImportFONewElectronicAddress.csv | このファイルは、財務と運用アプリ内で新しい **電子アドレス** レコードの作成に使用します。 |

このトピックでは、Data Factory のテンプレートを使用し、データをアップグレードする方法について説明します。 カスタマイズを実行しない場合は、このテンプレートをそのまま使用できます。 ただし、**取引先企業**、**連絡先**、**ベンダー** データをカスタマイズする場合は、このトピックで説明するようにテンプレートを変更する必要があります。

> [!IMPORTANT]
> 関係者の住所と関係者の電子アドレスのテンプレートを実行するための特別な指示があります。 最初にパーティのテンプレートを起動し、次にパーティの配送先住所のテンプレートを起動し、次にパーティの電子住所のテンプレートを起動する必要があります。 各テンプレートは、個別のデータ ファクトリでインポートするように設計されています。

## <a name="prerequisites"></a>必要条件

パーティのグローバルアドレス帳モデルにアップグレードするには、以下の前提条件が必要です:

+ [Azure のサブスクリプション](https://portal.azure.com/)に登録している必要があります。
+ [このテンプレート](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema)へのアクセス許可が必要です。
+ 既存の二重書き込み顧客である必要があります。

## <a name="prepare-for-the-upgrade"></a>アップグレードの準備

アップグレードには以下の準備が必要です:

+ **完全同期:** Finance and Operations 環境と Customer Engagement 環境の両方で、**取引先企業 (顧客)**、**取引先担当者**、**ベンダー** の各テーブルが完全に同期された状態になります。
+ **統合キー**: Customer Engagement アプリの **取引先企業 (顧客)**、**連絡先**、および **仕入先** テーブルは、既成の統合キーを使用しています。 統合キーをカスタマイズした場合は、テンプレートをカスタマイズする必要があります。
+ **パーティ番号:** すべてのアップグレードされる **取引先企業 (顧客)**、**取引先担当者**、**ベンダー** レコードにはパーティ番号があります。 パーティ番号がないレコードは無視されます。 これらのレコードをアップグレードする場合は、アップグレード処理を開始する前に、それらのレコードにパーティ番号を追加します。
+ **システム停止:** アップグレードの際には、Finance and Operations 環境と Customer Engagement 環境の両方をオフラインにする必要があります。
+ **スナップショット**: 財務と運用アプリと Customer Engagement アプリ両方のスナップショットを作成します。 その後、必要に応じてスナップショットを使って以前の状態を復元することができます。

## <a name="deployment"></a>展開

1. テンプレートを [Dynamics-365-FastTrack-Implementation-Assets](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) からダウンロードします。
2. [Azure ポータル](https://portal.azure.com/)にサインインします。
3. [リソース グループ](/azure/azure-resource-manager/management/manage-resource-groups-portal)を作成します。
4. 作成したリソース グループに[ストレージ アカウント](/azure/storage/common/storage-account-create?tabs=azure-portal)を作成します。
5. 作成したリソース グループに[Data Factory ](/azure/data-factory/quickstart-create-data-factory-portal)を作成します。
6. Data Factory を開き、**作成者 & モニター** タイルを選択します。
7. **管理** タブで、**ARM テンプレート** を選択します。
8. **ARM テンプレートをインポートする** を選択して、**パーティ** テンプレートをインポートします。
9. テンプレートをデータ ファクトリーにインポートします。 **プロジェクトの詳細** および **インスタンスの詳細** に対して次の値を入力します。

    | フィールド | 値 |
    |---|---|
    | サブスクリプション | Azure サブスクリプション |
    | リソース グループ | ストレージ アカウントが作成されたのと同じリソースを提供します。 |
    | リージョン | リージョン ID |
    | ファクトリー名 | ファクトリー名 |
    | FO リンクされた Service_service プリンシパル キー | アプリケーションのキー |
    | Azure Blob Storage_connection 文字列 | Azure Blob Storage 接続文字列 |
    | Dynamics CRM リンクされた Service_password | ユーザー名に指定したユーザーアカウントのパスワードです |
    | FO リンクされた Service_properties_type Properties_url | `https://sampledynamics.sandbox-operationsdynamics.com/data` |
    | FO リンクされた Service_properties_type Properties_tenant | アプリケーションが所属するテナントに関する情報 (ドメイン名またはテナント ID) です |
    | FO リンクされた Service_properties_type Properties_aad リソース ID | `https://sampledynamics.sandboxoperationsdynamics.com` |
    | FO リンクされた Service_properties_type Properties_service プリンシパル ID | アプリケーションのクライアント ID です |
    | Dynamics CRM リンクされた Service_properties_type Properties_username | Dynamics 365 サービスに接続するために使用するユーザー名です |

    詳細については、次のトピックを参照してください。

    - [各環境の Resource Manager テンプレートの手動促進](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [リンクされたサービス プロパティ](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Azure Data Factory を使用したデータのコピー](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. 配置後に、データ ファクトリのデータセット、データ フロー、およびリンクされたサービスを検証します。

    ![データセット、データ フロー、およびリンクされたサービス。](media/data-factory-validate.png)

11. **管理** に移動します。 **接続** で、**リンクされたサービス** を選択します。 **DynamicsCrmLinkedService** を選択します。 **リンクされたサービスの編集 (Dynamics CRM)** ダイアログ ボックスに、次の値を入力します。

    | フィールド | 値 |
    |---|---|
    | Name | DynamicsCrmLinkedService |
    | 説明 | エンティティ データをフェッチする CRM インスタンスに接続するリンクされたサービス |
    | 統合ランタイム経由の接続 | AutoResolvelntegrationRuntime |
    | 配置のタイプ | オンライン |
    | サービス URI | `https://<organization-name>.crm[x].dynamics.com` |
    | 認証タイプ | Office365 |
    | ユーザー名 | |
    | パスワードまたは Azure Key Vault | パスワード |
    | パスワード | |

## <a name="prepare-to-run-the-data-factory-templates"></a>Data Factory のテンプレートの実行を準備する

ここでは、パーティの配送先住所およびパーティの電子住所の Data Factory のテンプレートを実行する前に必要な設定について説明します。

### <a name="setup-to-run-the-party-postal-address-template"></a>パーティの配送先住所テンプレートを実行する設定

1. Customer Engagement アプリにサインインして、**設定** \> **パーソナライズ設定** にアクセスします。 **全般** タブで、 システム管理者アカウントのタイムゾーン構成を行います。 財務と運用アプリから住所の有効期限を更新するには、タイムゾーンが協定世界時 (UTC) である必要があります。

    ![システム管理者アカウントのタイムゾーン設定。](media/ADF-1.png)

2. Data Factory の **管理** タブにある **グローバルパラメーター** で、次のグローバルパラメーターを作成します。

    | 番号 | Name | 種類 | 値 |
    |---|---|---|---|
    | 1 | PostalAddressIdPrefix | 文字列 | このパラメーターは、新規に作成された配送先住所の宛先に、接頭辞としてシリアル番号を付加します。 財務と運用アプリや Customer Engagement アプリの住所と競合しない文字列を入力してください。 たとえば、**ADF-PAD-** を使用します。 |

    ![管理タブで作成した PostalAddressIdPrefix グローバル パラメータです。](media/ADF-2.png)

3. 完了したら、**すべて発行する** を選択します。

    ![すべてのボタンを公開します。](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>パーティの電子住所テンプレートを実行する設定

1. Data Factory の **管理** タブにある **グローバルパラメーター** で、次のグローバルパラメーターを作成します。

    | 番号 | Name | 種類 | 値 |
    |---|---|---|---|
    | 1 | IsFOSource | ブール | このパラメーターは、競合が発生した場合に、どのプライマリ システムのアドレスを置き換えるかを決定します。 この値が **true** の場合、財務と運用アプリのプライマリ アドレスは、Customer Engagement アプリのプライマリ アドレスに置き換えられます。 この値が **false** の場合、Customer Engagement アプリのプライマリ アドレスは、財務と運用アプリのプライマリ アドレスに置き換えられます。 |
    | 2 | ElectronicAddressIdPrefix | 文字列 | このパラメーターは、新規に作成された電子住所の宛先に、接頭辞としてシリアル番号を付加します。 財務と運用アプリや Customer Engagement アプリの電子アドレスと競合しない文字列を入力してください。 たとえば、**ADF-EAD-** を使用します。 |

    ![管理タブで作成したグローバル パラメーター IsFOSource と ElectronicAddressIdPrefix です。](media/ADF-4.png)

2. 完了したら、**すべて発行する** を選択します。

## <a name="run-the-templates"></a>テンプレートの実行

1. 財務と運用アプリを使用する、次の **取引先企業**、**取引先担当者**、および **仕入先** の二重書き込みマップを停止します。

    + 顧客 V3 (アカウント)
    + 顧客 V3 (連絡先)
    + CDS 連絡先 V2 (連絡先)
    + CDS 連絡先 V2 (連絡先)
    + 仕入先 V2 (msdyn_vendors)

2. Dataverse の **msdy_dualwriteruntimeconfig** テーブルからマッピングが削除されていることを確認してください。
3. AppSource から [二重書き込み当事者およびグローバル アドレス帳ソリューション](https://aka.ms/dual-write-gab)をインストールします 。
4. 次のテーブルにデータが含まれている場合は、財務と運用アプリで **初期同期** を実行します:

    + あいさつ文
    + 個人の特徴タイプ
    + 結句
    + 連絡担当者の肩書き
    + 意思決定ロール
    + ロイヤルティ レベル

5. Customer Engagement アプリで、次のプラグイン ステップを無効にします:

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

    + Customeraddress

        + 作成

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: customeraddress の作成

        + 更新

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: customeraddress の更新

        + 削除

            + Microsoft.Dynamics.GABExtended.Plugins.DeleteCustomerAddress: customeraddress の削除

    + msdyn_partypostaladdress

        + 作成

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress の作成
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdress の作成

        + 更新

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress の更新
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdress の更新

    + msdyn_postaladdress

        + 作成

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: msdyn_postaladdress の作成
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: msdyn_postaladdress の作成
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdress の作成

        + 更新

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: msdyn_postaladdress の更新
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdress の更新

    + msdyn_partyelectronicaddress

        + 作成

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress の作成

        + 更新

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress の更新

        + 削除

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: msdyn_partyelectronicaddress の削除

6. Customer Engagement アプリで、次のワークフローを無効にします:

    + 取引先企業テーブルでの仕入先の作成
    + 取引先企業テーブルでの仕入先の作成
    + 連絡先テーブルでの個人タイプの仕入先の作成
    + 仕入先テーブルでの個人タイプの仕入先の作成
    + 取引先企業テーブルでの仕入先の更新
    + 仕入先テーブルでの仕入先の更新
    + 取引先担当者テーブルでの個人タイプの仕入先の更新
    + 仕入先テーブルでの個人タイプの仕入先の更新

7. Data Factory で、次のイラストに示すように **今すぐトリガーする** を選択してテンプレートを実行します。 このプロセスは、データ量にもよりますが、完了までに数時間かかる場合があります。

    ![テンプレートを実行します。](media/data-factory-trigger.png)

    > [!NOTE]
    > **取引先企業**、**連絡先**、**ベンダー** をカスタマイズする場合は、テンプレートを変更する必要があります。

8. 新しい **関係者** レコードを財務と運用アプリにインポートします。

    1. Azure Blob Storage から **FONewParty.csv** ファイルをダウンロードします。 このパスは、 **partybootstrapping/output/FONewParty.csv** です。
    2. **FONewParty.csv** ファイルを Excel ファイルに変換し、Excel ファイルを財務と運用アプリにインポートします。 または、CSV のインポートが機能する場合は、.csv ファイルを直接インポートできます。 この手順は、データ量にもよりますが、完了までに数時間かかる場合があります。 詳細については、[データのインポート ジョブとエクスポート ジョブの概要](../data-import-export-job.md)を参照してください。

    ![新しい Dataverse レコードをインポートします。](media/data-factory-import-party.png)

9. Data Factory では、パーティの配送先住所とパーティの電子住所のテンプレートを続けて実行します。

    + パーティの配送先住所テンプレートは、Customer Engagement アプリ内のすべての配送先住所レコードをアップサートし、対応する **取引先企業**、**取引先担当者**、**ベンダー** レコードと関連づけます。 3 種類の .csv が生成されます: ImportFONewPostalAddressLocation.csv、ImportFONewPartyPostalAddress.csv、ImportFONewPostalAddress.csv 。
    + パーティの電子先住所テンプレートは、Customer Engagement アプリ内のすべての電子住所レコードをアップサートし、対応する **取引先企業**、**取引先担当者**、**ベンダー** レコードと関連づけます。 1 種類の .csv が生成されます: ImportFONewElectronicAddress.csv 。

    ![パーティの配送先住所とパーティの電子先住所のテンプレートを実行します。](media/ADF-7.png)

10. このデータを使用して財務と運用アプリを更新するには、.csv ファイルを Excel ブックに変換し、[財務と運用アプリにインポート](/data-entities/data-import-export-job) します。 または、CSV のインポートが機能する場合は、.csv ファイルを直接インポートできます。 この手順は、データ量にもよりますが、完了までに数時間かかる場合があります。

    ![正常にインポートされました。](media/ADF-8.png)

11. Customer Engagement アプリで、次のプラグイン ステップを有効にします:

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

    + msdyn_partypostaladdress

        + 作成

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress の作成
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdress の作成

        + 更新

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress の更新
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdress の更新

    + msdyn_postaladdress

        + 作成

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: msdyn_postaladdress の作成
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: msdyn_postaladdress の作成
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdress の作成

        + 更新

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: msdyn_postaladdress の更新
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdress の更新
 
    + msdyn_partyelectronicaddress

        + 作成

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress の作成

        + 更新

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress の更新

        + 削除

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: msdyn_partyelectronicaddress の削除

12. Customer Engagement アプリで、前述の手順で次のワークフローを無効化した場合は、有効にします:

    + 取引先企業テーブルでの仕入先の作成
    + 取引先企業テーブルでの仕入先の作成
    + 連絡先テーブルでの個人タイプの仕入先の作成
    + 仕入先テーブルでの個人タイプの仕入先の作成
    + 取引先企業テーブルでの仕入先の更新
    + 仕入先テーブルでの仕入先の更新
    + 取引先担当者テーブルでの個人タイプの仕入先の更新
    + 仕入先テーブルでの個人タイプの仕入先の更新

13. [パーティおよびグローバル アドレス帳](party-gab.md)の指示に従って **パーティ** 関連のマップを実行します。

## <a name="explanation-of-the-data-factory-templates"></a>Data Factory テンプレートの説明

ここでは、Data Factory の各テンプレートの手順を説明します。

### <a name="steps-in-the-party-template"></a>パーティ テンプレートの手順

1. 手順 1～6 では、デュアルライトが可能な企業を特定し、その企業のためのフィルター句を構築します。
2. 手順 7-1 から 7-9 では、財務と運用アプリと Customer Engagement アプリの両方からデータを取得し、そのデータをアップグレード用にステージングします。
3. 手順 8 から 9 では、財務と運用アプリと Customer Engagement アプリの間で、**取引先企業**、**取引先担当者**、**仕入先** レコードの関係者番号を比較します。 パーティ番号がないレコードはスキップされます。
4. 手順 10 では、Customer Engagement アプリと財務と運用アプリで作成する必要がある関係者レコード用の 2 つの .csv ファイルを生成します。

    - **FOCDSParty.csv** – このファイルには、企業がデュアルライトを有効にしているかどうかにかかわらず、両システムのすべてのパーティ レコードが含まれています。
    - **FONewParty.csv** – このファイルには、Dataverse が認識しているパーティ レコードのサブセット (例えば、**見込顧客** タイプのアカウント) が含まれています。

5. 手順 11 では、Customer Engagement アプリにパーティを作成します。
6. 手順 12 では、Customer Engagementアプリからパーティ のグローバルに一意な識別子 (GUID)を取得し、後続の手順で **取引先企業**、**取引先担当者**、 **ベンダー** のレコードに関連づけられるようにステージングします。
7. 手順 13 では、**取引先企業**、**取引先担当者**、**ベンダー** の各レコードをパーティの GUID と関連付けます。
8. 手順 14-1 から 14-3 では、Customer Engagement アプリの **取引先企業**、**取引先担当者**、**ベンダー** のレコードをパーティの GUID で更新します。
9. 手順 15-1 から 手順 15-3 では、**取引先企業**, **取引先担当者**、**ベンダー** のレコードに対する **パーティーの連絡先** レコードを用意します。
10. 手順 16-1 から 手順 16-7 では、敬称や個人の文字種などの参照データを取得し、**パーティーの連絡先** レコードに関連付けることができます。
11. 手順 17 では、**取引先企業**, **取引先担当者**、**ベンダー** のレコードに対する **パーティーの連絡先** レコードをマージします。
12. 手順 18 では、**パーティーの連絡先** レコードを Customer Engagement アプリにインポートします。

### <a name="steps-in-the-party-postal-address-template"></a>パーティの配送先住所テンプレートの手順

1. 手順 1-1 から 1-10 では、財務と運用アプリと Customer Engagement アプリの両方からデータを取得し、そのデータをアップグレード用にステージングします。
2. 手順 2 では、財務と運用アプリの住所データを、住所と関係者住所を結合して非正規化します。
3. 手順 3 では、Customer Engagement アプリから取引先企業、取引先担当者、ベンダーのアドレスデータを重複排除してマージします。
4. 手順 4 では、財務と運用アプリで使用する .csv ファイルを作成し、取引先企業、取引先担当者、仕入先の住所に基づいた新しい住所データを作成します。
5. 手順 5-1 では、財務と運用アプリと Customer Engagement アプリの両方に基づいて、Customer Engagement アプリで使用する .csv ファイルを作成し、すべての住所データを作成します。
6. 手順 5-2では、.csvファイルを手動インポートで使用する Finance and Operations インポートのフォーマットに変換します。

    - ImportFONewPostalAddressLocation.csv
    - ImportFONewPartyPostalAddress.csv
    - ImportFONewPostalAddress.csv

7. 手順 6 では、配送先住所のコレクション データを Customer Engagement アプリにインポートします。
8. 手順 7 では、パーティーの配送先住所のコレクション データを Customer Engagement アプリから取得します。
9. 手順 8 では、顧客の住所データを作成し、配送先住所のコレクション ID を関連付けます。
10. 手順 9-1 ～ 9-2 では、パーティーおよび配送先住所の収集 ID と配送先住所とパーティーの配送先住所を関連付けます。
11. 手順 10-1 ～ 10-3 では、顧客の住所、配送先住所、パーティの配送先住所を Customer Engagement アプリにインポートします。

### <a name="steps-in-the-party-electronic-address-template"></a>パーティの電子住所テンプレートの手順

1. 手順 1-1 から 1-5 では、財務と運用アプリと Customer Engagement アプリの両方からデータを取得し、そのデータをアップグレード用にステージングします。
2. 手順 2 では、Customer Engagement アプリ内の電子住所を、取引先企業、取引先担当者、ベンダーの各エンティティから統合します。
3. 手順 3 では、Customer Engagement アプリと財務と運用アプリのプライマリ電子アドレス データをマージします。
4. 手順 4 では .csv ファイルを作成します。

    - 取引先企業、取引先担当者、仕入先の住所を基に、財務と運用アプリで使用する電子アドレス データを新規作成します。
    - 財務と運用アプリの電子アドレス、取引先企業、取引先担当者、仕入先の住所をもとに、Customer Engagement アプリの電子アドレス データを新規作成します。

5. 手順 5-1 では、電子住所を Customer Engagement アプリにインポートします。
6. 手順 5-2 では、Customer Engagement アプリの取引先企業、取引先担当者のプライマリ住所の更新に使用する .csv ファイルを作成します。
7. 手順 6-1 ～ 6-2 では、取引先企業、取引先担当者のプライマリ住所を Customer Engagement アプリにインポートします。

## <a name="troubleshooting"></a>トラブルシューティング

1. 処理に失敗した場合は、データ ファクトリを再実行してください。 失敗した活動からスタートします。
2. データファクトリーで生成されたファイルは、データの検証に使用することができます。
3. データ ファクトリは、.csv ファイルをベースに動作します。 そのため、任意のフィールド値にカンマが含まれていると、結果に影響が出る場合があります。 フィールドの値からすべてのカンマを取り除く必要があります。
4. **監視** タブでは、すべての手順と処理済みデータに関する情報が提供されます。 特定の手順を選択してデバッグします。

    ![監視タブ。](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>テンプレートの詳細を確認する

テンプレートに関する詳細については、[Azure Data Factory テンプレートの readme コメント](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) で確認できます。
