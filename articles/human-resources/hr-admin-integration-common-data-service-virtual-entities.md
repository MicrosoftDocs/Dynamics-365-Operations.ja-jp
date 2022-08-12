---
title: Dataverse の仮想テーブルのコンフィギュレーション
description: この記事では、Dynamics 365 Human Resources の既存の仮想テーブルを構成、生成、更新し、生成された利用可能なテーブルを分析する方法を示します。
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 45155dba5063981eb3aeeed4dda1d79a57b7c8af
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067101"
---
# <a name="configure-dataverse-virtual-tables"></a>Dataverse の仮想テーブルのコンフィギュレーション


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Dynamics 365 Human Resources は Microsoft Dataverse の仮想データ ソースです。 このサービスでは、Dataverse および Microsoft Power Platform からの作成、読み取り、更新、および削除 (CRUD) の完全な操作が提供されます。 仮想テーブルのデータは Dataverse には格納されませんが、アプリケーション データベースに保存されます。

Dataverse から Human Resources エンティティに対して CRUD 操作を有効にするには、エンティティを Dataverse の仮想テーブルとして使用できるようにする必要があります。 これにより、Human Resources のデータで Dataverse と Microsoft Power Platform から CRUD 操作を実行できます。 また、この操作では、Human Resources のビジネス ロジックの完全な検証をサポートしているため、エンティティにデータを書き込むときにデータの整合性を確保できます。

> [!NOTE]
> Human Resources エンティティは Dataverse テーブルに対応します。 Dataverse (旧 Common Data Service) および用語更新の詳細については、[Microsoft Dataverse とは何ですか?](/powerapps/maker/data-platform/data-platform-intro)を参照してください

## <a name="available-virtual-tables-for-human-resources"></a>Human Resources で使用可能な仮想テーブル

Human Resources のすべての Open Data Protocol (OData) テーブルは、Dataverse の仮想エンティティとして使用できます。 また、Power Platform で使用することもできます。 データを Dataverse にコピーまたは同期することなく、完全な CRUD 機能を備えた Human Resources からデータを使ってアプリとエクスペリエンスを直接ビルドできるようになりました。 Power Apps ポータルは、Human Resources の業務プロセスのコラボレーション シナリオを可能にする外部向けの Web サイトをビルドするために使用できます。

環境で有効になっている仮想テーブルの一覧を表示し、**Dynamics 365 HR 仮想テーブル** ソリューションで [Power Apps](https://make.powerapps.com) のテーブルの操作を開始できます。

![Power Apps の Dynamics 365 HR 仮想テーブル。](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a>仮想テーブルとネイティブ テーブルの対比

Human Resources の仮想テーブルは、Human Resources 向けに作成されたネイティブの Dataverse テーブルとは異なります。 

Human Resources のネイティブ テーブルは、Dataverse の HCM Common ソリューションで個別に生成・管理されます。 ナチュラル テーブルでは、データが Dataverse に保存され、Human Resources アプリケーション データベースとの同期が必要になります。

> [!NOTE]
> Human Resources の Dataverse ナチュラル テーブルの一覧については、[Dataverse テーブル](./hr-developer-entities.md)を参照してください 。

## <a name="setup"></a>段取り

環境で仮想テーブルを有効にするには、次の設定手順に従います。

### <a name="enable-virtual-tables-in-human-resources"></a>Human Resources の仮想テーブルを有効にする

まず、**機能管理** ワークスペースで仮想テーブルを有効にする必要があります。

1. 人事管理では、**システム管理** を選択します。

2. **機能管理** タイルを選択します。

3. **Dataverse における HR の仮想テーブルのサポート** を選択し、**有効化** を選択します。

有効化および無効化機能に関する情報は、[機能の管理](hr-admin-manage-features.md) を参照してください。

### <a name="register-the-app-in-microsoft-azure"></a>アプリを Microsoft Azure に登録する

Microsoft ID プラットフォームがアプリとユーザーに対して認証および承認サービスを提供できるように、Azure portal で Human Resources インスタンスを登録する必要があります。 Azure でのアプリの登録に関する詳細については、「[クイックスタート: Microsoft ID プラットフォームでアプリケーションを登録する](/azure/active-directory/develop/quickstart-register-app)」を参照してください。

1. [Microsoft Azure ポータル](https://portal.azure.com)を開きます。

2. Azure サービスの一覧で、**アプリの登録** を選択します。

3. **新規登録** を選択します。

4. **名前** フィールドに、アプリの内容を示す名前を入力します。 たとえば、**Dynamics 365 Human Resources 仮想テーブル** です。

5. **リダイレクト URI** フィールドに、Human Resources のインスタンスの名前空間 URL を入力します。

6. **登録** を選択します。

7. 登録が完了すると、Azure portal には、**アプリケーション (クライアント) ID** を含むアプリ登録の **概要** ウィンドウが表示されます。 この時点で **アプリケーション (クライアント) ID** をメモします。 この情報は、[仮想テーブル データ ソースを構成する](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source)際に入力します。

8. 左側のナビゲーション ウィンドウで、**証明書とシークレット** を選択します。

9. ページの **クライアント シークレット** セクションで、**新しいクライアント シークレット** を選択します。

10. 説明を入力し、期間を選択して、**追加** を選択します。

11. テーブルの **値** プロパティからシークレットの値を記録します。 この情報は、[仮想テーブル データ ソースを構成する](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source)際に入力します。

    > [!IMPORTANT]
    > この時点でシークレットの値をメモしておく必要があります。 このページから移動すると、シークレットは再度表示されません。

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a>Dynamics 365 HR 仮想テーブル アプリのインストール

Power Apps 環境に Dynamics 365 HR Virtual テーブルアプリをインストールして、仮想テーブルのソリューション パッケージを Dataverse にデプロイします。

1. Human Resources で、**Microsoft Dataverse の統合** ページを開きます。

2. **仮想テーブル** タブを選択します。

3. **テーブル アプリのインストール** を選択します。

### <a name="configure-the-virtual-table-data-source"></a>仮想テーブル データ ソースの構成

次の手順では、Power Apps 環境で仮想テーブルのデータ ソースを構成します。

1. [Power Platform 管理センター](https://admin.powerplatform.microsoft.com)を開きます。

2. **環境** の一覧で、Human Resources のインスタンスに関連付けられている Power Apps 環境を選択します。

3. ページの **詳細** セクションで、**環境 URL** を選択します。

4. **ソリューションの正常性ハブ** で、アプリケーション ページの右上にある **高度な検索** アイコンを選択します。

5. **高度な検索** ページの **検索対象** ドロップダウン リストで、**財務と運用の仮想データ ソースの構成** を選択します。

   > [!NOTE]
   > 前の設定手順から仮想テーブル アプリをインストールするには、数分かかる場合があります。 **財務と運用の仮想データ ソースの構成** がリストにない場合は、1 分ほど待ってからリストを更新してください。

6. **結果** を選択します。

7. **Microsoft HR データ ソース** のレコードを選択します。

8. データ ソースの構成に必要な情報を入力します。

   - **ターゲット URL**: Human Resources の名前空間の URL。 ターゲット URL の形式は次のとおりです。
     
     https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/

     例:
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     >URL の末尾に "**/**" 文字を挿入し、エラーを回避します。

     >[!NOTE]
     >ターゲット URL は、仮想テーブルがデータに対してポイントする Human Resources 環境を決定します。 運用環境のコピーを作成してサンドボックス環境を作成する場合は、この値を新しいサンドボックス環境の名前空間 URL に更新します。 これにより、仮想テーブルは、運用環境をポイントし続けずに、サンドボックス環境と接続できます。

   - **テナント ID**: Azure Active Directory (Azure AD) テナント ID。

   - **AAD アプリケーション ID**: Microsoft Azure ポータルに登録されているアプリケーションに対して作成されたアプリケーション (クライアント) ID。 この情報は、[アプリを Microsoft Azure に登録する](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)のステップで先に取得しました。

   - **AAD アプリケーション シークレット**: Microsoft Azure ポータルに登録されているアプリケーションに対して作成されたクライアント シークレット。 この情報は、[アプリを Microsoft Azure に登録する](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)のステップで先に取得しました。

   ![Microsoft HR データ ソース。](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. **保存して閉じる** を選択します。

### <a name="grant-app-permissions-in-human-resources"></a>Human Resources でアプリのアクセス許可を付与する

Human Resources でアクセス許可を付与するのは、次の 2 つの Azure AD アプリケーションです。

- Microsoft Azure ポータルでテナント用に作成されたアプリ
- Power Apps 環境にインストールされた Dynamics 365 HR 仮想テーブル アプリ 

1. Human Resources で、**Azure Active Directory アプリケーション** ページを開きます。

2. **新規** を選択して、新しい申請レコードを作成します。

    - **クライアント ID** フィールドに、Microsoft Azure ポータルに登録したアプリのクライアント ID を入力します。
    - **名前** フィールドに、Microsoft Azure ポータルに登録したアプリの名前を入力します。
    - **ユーザー ID** フィールドで、管理者アクセス許可を持つユーザーのユーザー ID をHuman Resources と Power Apps 環境から選択します。

3. **新規** を選択して、2 つ目の申請レコードを作成します。

    - **クライアント ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **名前**: Dynamics 365 HR 仮想テーブル
    - **ユーザー ID** フィールドで、管理者アクセス許可を持つユーザーのユーザー ID をHuman Resources と Power Apps 環境から選択します。

## <a name="generate-virtual-tables"></a>仮想テーブルの生成

設定が完了したら、Dataverse インスタンスで生成して有効にする仮想テーブルを選択できます。

1. Human Resources で、**Microsoft Dataverse の統合** ページを開きます。

2. **仮想テーブル** タブを選択します。

> [!NOTE]
> 必要なすべての設定が完了すると、**仮想テーブルの有効化** トグルが自動的に **はい** に設定されます。 トグルが **いいえ** に設定されている場合は 、このドキュメントの前のセクションの手順を確認して、すべての前提条件の設定が完了していることを確認してください。

3. Dataverse で生成するテーブルを選択します。

4. **生成/更新** を選択します。

![Dataverse の統合。](./media/hr-admin-integration-dataverse-integration.png)

## <a name="check-table-generation-status"></a>テーブルの生成状態の確認

仮想テーブルは、非同期のバックグラウンド プロセスによって Dataverse で生成されます。 アクション センターのプロセス表示を更新します。 エラー ログを含むプロセスの詳細については、**プロセスの自動化** ページに表示されます。

1. Human Resources で、**プロセスの自動化** ページを開きます。

2. **バックグラウンド プロセス** タブを選択し ます。

3. **仮想テーブルポーリング非同期操作のバックグラウンド プロセス** を選択します。

4. **最新の結果を表示する** を選択します。

スライドアウト ペインには、プロセスの最新の実行結果が表示されます。 Dataverse から返されたエラーを含む、プロセスのログを表示することができます。

## <a name="see-also"></a>参照

[Dataverse とは](/powerapps/maker/common-data-service/data-platform-intro)<br>
[Dataverse のテーブル](/powerapps/maker/common-data-service/entity-overview)<br>
[テーブルの関連付けの概要](/powerapps/maker/common-data-service/relationships-overview)<br>
[外部データ ソースのデータを含む仮想テーブルの作成と編集](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Power Apps ポータルについて](/powerapps/maker/portals/overview)<br>
[Power Apps でのアプリの作成の概要](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

