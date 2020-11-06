---
title: Common Data Service 仮想エンティティの構成
description: このトピックでは、Dynamics 365 Human Resources の仮想エンティティを構成する方法について説明します。 既存の仮想エンティティを生成および更新し、生成されたエンティティと使用可能なエンティティを分析します。
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0d6f79ea569a7a9b0d25e73e8666bf9ba19095d0
ms.sourcegitcommit: a8665c47696028d371cdc4671db1fd8fcf9e1088
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/21/2020
ms.locfileid: "4058157"
---
# <a name="configure-common-data-service-virtual-entities"></a>Common Data Service 仮想エンティティの構成

[!include [banner](includes/preview-feature.md)]

Dynamics 365 Human Resources は Common Data Service の仮想データ ソースです。 このサービスでは、Common Data Service および Microsoft Power Platform からの作成、読み取り、更新、および削除 (CRUD) の完全な操作が提供されます。 仮想エンティティのデータは Common Data Service には保存されませんが、アプリケーション データベースに保存されます。 

Common Data Service から Human Resources エンティティに対して CRUD 操作を有効にするには、エンティティを Common Data Service の仮想エンティティとして使用できるようにする必要があります。 これにより、Human Resources のデータで Common Data Service と Microsoft Power Platform から CRUD 操作を実行できます。 また、この操作では、Human Resources のビジネス ロジックの完全な検証をサポートしているため、エンティティにデータを書き込むときにデータの整合性を確保できます。

## <a name="available-virtual-entities-for-human-resources"></a>Human Resources で使用可能な仮想エンティティ

Human Resources のすべての Open Data Protocol (OData) エンティティは、Common Data Service の仮想エンティティとして使用できます。 また、Power Platform で使用することもできます。 データを Common Data Service にコピーまたは同期することなく、完全な CRUD 機能を備えた Human Resources からデータを使ってアプリとエクスペリエンスを直接ビルドできるようになりました。 Power Apps ポータルは、Human Resources の業務プロセスのコラボレーション シナリオを可能にする外部向けの Web サイトをビルドするために使用できます。

環境で有効になっている仮想エンティティの一覧を表示し、 **Dynamics 365 HR 仮想エンティティ** ソリューションで [Power Apps](https://make.powerapps.com) のエンティティの操作を開始できます。

![Power Apps の Dynamics 365 HR 仮想エンティティ](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a>仮想エンティティとナチュラル エンティティの比較

Human Resources の仮想エンティティは、Human Resources 向けに作成された Common Data Service のナチュラル エンティティとは異なります。 Human Resources のナチュラル エンティティは、Common Data Service の HCM Common ソリューションで個別に生成および管理されます。 ナチュラル エンティティでは、データが Common Data Service に保存され、Human Resources アプリケーション データベースとの同期が必要になります。

> [!NOTE]
> Human Resources の Common Data Service ナチュラル エンティティの一覧については、「[Common Data Service エンティティ](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities)」を参照してください 。

## <a name="setup"></a>段取り

環境で仮想エンティティを有効にするには、次の設定手順に従います。 

### <a name="register-the-app-in-microsoft-azure"></a>アプリを Microsoft Azure に登録する

最初に、Microsoft ID プラットフォームがアプリとユーザーに対して認証および承認サービスを提供できるように、Azure portal でアプリを登録する必要があります。 Azure でのアプリの登録に関する詳細については、「[クイックスタート: Microsoft ID プラットフォームでアプリケーションを登録する](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)」を参照してください。

1. [Microsoft Azure ポータル](https://portal.azure.com)を開きます。

2. Azure サービスの一覧で、 **アプリの登録** を選択します。

3. **新規登録** を選択します。

4. **名前** フィールドに、アプリの内容を示す名前を入力します。 たとえば、 **Dynamics 365 Human Resources 仮想エンティティ** 。

5. **リダイレクト URI** フィールドに、Human Resources のインスタンスの名前空間 URL を入力します。

6. **登録** を選択します。

7. 登録が完了すると、Azure portal には、 **アプリケーション (クライアント) ID** を含むアプリ登録の **概要** ウィンドウが表示されます。 この時点で **アプリケーション (クライアント) ID** をメモします。 この情報は、[仮想エンティティ データ ソースを構成する](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source)ときに入力します。

8. 左側のナビゲーション ウィンドウで、 **証明書とシークレット** を選択します。

9. ページの **クライアント シークレット** セクションで、 **新しいクライアント シークレット** を選択します。

10. 説明を入力し、期間を選択して、 **追加** を選択します。

11. シークレットの値を記録します。 この情報は、[仮想エンティティ データ ソースを構成する](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source)ときに入力します。

    > [!IMPORTANT]
    > この時点でシークレットの値をメモしておく必要があります。 このページから移動すると、シークレットは再度表示されません。

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a>Dynamics 365 HR Virtual Entity のインストール

Power Apps 環境に Dynamics 365 HR Virtual Entity アプリをインストールして、仮想エンティティ ソリューション パッケージを Common Data Service にデプロイします。

1. [Power Platform 管理センター](https://admin.powerplatform.microsoft.com)を開きます。

2. **環境** の一覧で、Human Resources のインスタンスに関連付けられている Power Apps 環境を選択します。

3. ページの **リソース** セクションで、 **Dynamics 365 アプリ** を選択します。

4. **アプリのインストール** アクションを選択します。

5. **Dynamics 365 HR Virtual Entity** を選択し、 **次へ** を選択します。

6. サービス使用条件に同意することを確認してマークします。

7. **インストール** を選択します。

インストールには数分かかります。 完了したら、次の手順に進みます。

![Power Platform 管理センターから Dynamics 365 HR Virtual Entity アプリをインストールします](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a>仮想エンティティ データ ソースの構成 

次の手順では、Power Apps 環境で仮想エンティティ データ ソースを構成します。 

1. [Power Platform 管理センター](https://admin.powerplatform.microsoft.com)を開きます。

2. **環境** の一覧で、Human Resources のインスタンスに関連付けられている Power Apps 環境を選択します。

3. ページの **詳細** セクションで、 **環境 URL** を選択します。

4. **ソリューションの正常性ハブ** で、アプリケーション ページの右上にある **高度な検索** アイコンを選択します。

5. **高度な検索** ページの **検索対象** ドロップダウン リストで、 **Finance and Operations 仮想データ ソースの構成** を選択します。

6. **結果** を選択します。

7. **Microsoft HR データ ソース** のレコードを選択します。

8. データ ソースの構成に必要な情報を入力します。

   - **ターゲット URL** : Human Resources の名前空間の URL。
   - **テナント ID** : Azure Active Directory (Azure AD) テナント ID。
   - **AAD アプリケーション ID** : Microsoft Azure ポータルに登録されているアプリケーションに対して作成されたアプリケーション (クライアント) ID。 この情報は、[アプリを Microsoft Azure に登録する](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)のステップで先に取得しました。
   - **AAD アプリケーション シークレット** : Microsoft Azure ポータルに登録されているアプリケーションに対して作成されたクライアント シークレット。 この情報は、[アプリを Microsoft Azure に登録する](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)のステップで先に取得しました。

9. **保存して閉じる** を選択します。

   ![Microsoft HR データ ソース](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a>Human Resources でアプリのアクセス許可を付与する

Human Resources でアクセス許可を付与するのは、次の 2 つの Azure AD アプリケーションです。

- Microsoft Azure ポータルでテナント用に作成されたアプリ
- Power Apps 環境にインストールされた Dynamics 365 HR Virtual Entity アプリ 

1. Human Resources で、 **Azure Active Directory アプリケーション** ページを開きます。

2. **新規** を選択して、新しい申請レコードを作成します。

    - **クライアント ID** フィールドに、Microsoft Azure ポータルに登録したアプリのクライアント ID を入力します。
    - **名前** フィールドに、Microsoft Azure ポータルに登録したアプリの名前を入力します。
    - **ユーザー ID** フィールドで、管理者アクセス許可を持つユーザーのユーザー ID をHuman Resources と Power Apps 環境から選択します。

3. **新規** を選択して、2 つ目の申請レコードを作成します。

    - **クライアント ID** : f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **名前** : Dynamics 365 HR Virtual Entity
    - **ユーザー ID** フィールドで、管理者アクセス許可を持つユーザーのユーザー ID をHuman Resources と Power Apps 環境から選択します。

## <a name="generate-virtual-entities"></a>仮想エンティティの生成

セットアップが完了したら、Common Data Service インスタンスで生成して有効にする仮想エンティティを選択できます。

1. Human Resources で、 **Common Data Service (CDS) の統合** ページを開きます。

2. **仮想エンティティ** タブを選択します。

> [!NOTE]
> 必要なすべての設定が完了すると、 **仮想エンティティの有効化** トグルが自動的に **はい** に設定されます。 トグルが **いいえ** に設定されている場合は 、このドキュメントの前のセクションの手順を確認して、すべての前提条件の設定が完了していることを確認してください。

3. Common Data Service で生成するエンティティを選択します。

4. **生成/更新** を選択します。

![Common Data Service の統合](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a>エンティティの生成状態の確認

仮想エンティティは、非同期のバックグラウンド プロセスによって Common Data Service で生成されます。 アクション センターのプロセス表示を更新します。 エラー ログを含むプロセスの詳細については、 **プロセスの自動化** ページに表示されます。

1. Human Resources で、 **プロセスの自動化** ページを開きます。

2. **バックグラウンド プロセス** タブを選択し ます。

3. **仮想エンティティポーリング非同期操作のバックグラウンド プロセス** を選択します。

4. **最新の結果を表示する** を選択します。

スライドアウト ペインには、プロセスの最新の実行結果が表示されます。 Common Data Service から返されたエラーを含む、プロセスのログを表示することができます。

## <a name="see-also"></a>参照

[Common Data Service とは](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[エンティティ概要](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[エンティティの関連付けの概要](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[外部データ ソースのデータを含む仮想エンティティの作成と編集](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Power Apps ポータルについて](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[Power Apps でのアプリの作成の概要](https://docs.microsoft.com/powerapps/maker/)
