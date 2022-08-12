---
title: 税計算コンフィギュレーションのマスタ データルックアップの有効化
description: この記事では、税計算マスター データ検索機能を有効にするための設定方法について説明します。
author: kai-cloud
ms.date: 07/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3642bb88d5b0570014513b64eef5fdab6d1ee9d3
ms.sourcegitcommit: 5b721f6fc1ba4350b5bd0eae457f71d80246db42
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/20/2022
ms.locfileid: "9181127"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>税計算コンフィギュレーションのマスタ データルックアップの有効化 

[!include [banner](../includes/banner.md)]

この記事では、税計算マスター データ検索機能を有効にするための設定方法について説明します。 ドロップダウン リストで、**法人**、**仕入先アカウント**、**品目コード**、**配送条件** などのフィールドに対する税計算コンフィギュレーションの値を選択できます。 これらの値は、Microsoft Dataverse データ ソースを使用して接続されている Microsoft Dynamics 365 Finance 環境から取得されます。

> [!NOTE] 
> 税計算マスター データ検索機能はオプションの機能です。 Regulatory Configuration Service (RCS) の **税サービス Dataverse のデータソースのサポート** 機能を無効にする場合は、次の手順を省略できます。 ただし、この場合、ドロップダウン リストは税計算コンフィギュレーションでは使用できません。

税計算の機能バージョン構成のドロップダウン リストを有効にするには、次の手順を実行します。

1. [Microsoft Power Platform 統合を有効にして Dataverse 環境を開きます。](#enable)
2. [財務と運用の仮想エンティティをインストールします。](#install)
3. [Azure Active Directory (Azure AD) アプリケーションを登録します。](#register)
4. [財務と運用アプリでアプリのアクセス許可を付与します。](#grant)
5. [仮想エンティティ データ ソースを構成します。](#configure)
6. [Dataverse 仮想エンティティを有効化します。](#virtual)
7. [税計算用に接続されているアプリケーションを設定します。](#set-up)
8. [Dataverse モデル マッピング コンフィギュレーションをインポートし、設定します。](#import)

## <a name="enable-microsoft-power-platform-integration-and-open-the-dataverse-environment"></a><a name='enable'></a> Microsoft Power Platform 統合を有効にして、Dataverse 環境を開く

財務と運用アプリおよび Microsoft Power Platform の統合は Microsoft Dynamics Lifecycle Services (LCS) で新しい財務と運用アプリ環境を作成する時に有効化できます。 詳細については、[Microsoft Power Platform 統合 - アドインの概要](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)を参照してください。 完了すると、Microsoft Power Platform 環境の名前が **Power Platform 統合** セクションに表示されます。

1. LCS の財務と運用環境にある、**Power Platform 統合** セクションで、リンクされた環境の **環境名** の値を検索してメモします。

    [![環境名の値です。](./media/tcs-dataverse-master-data-lookup-1.png)](./media/tcs-dataverse-master-data-lookup-1.png)

2. [Power Platform 管理センター](https://admin.powerplatform.microsoft.com/environments) の **環境** タブで、メモした **環境名** の値に一致する環境を選択します。
3. **詳細** ページで、Dataverse 環境の **環境 URL** の値を検索できます。 [手順 7. 税計算用に接続されているアプリケーションを設定する](#set-up) で必要であるため、この値をメモします。
4. **環境 URL** の値を選択して、ブラウザーの Dataverse 環境を開けることを確認します。

    [![Dataverse 環境ページ。](./media/tcs-dataverse-master-data-lookup-2.png)](./media/tcs-dataverse-master-data-lookup-2.png)

    > [!NOTE]
    > ブラウザーで Dataverse 環境を常時開いておきます。 これは、[手順 5. 仮想エンティティ データ ソースを構成する](#configure) で必要になります。

詳細については、[Microsoft Power Platform の統合を有効にする](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md)を参照してください。

## <a name="install-finance-and-operations-virtual-entities"></a><a name='install'></a> 財務と運用の仮想エンティティをインストールする

財務と運用の仮想エンティティの Dataverse ソリューションは、Microsoft AppSource 仮想エンティティ ソリューションからインストールする必要があります。

1. AppSource で, [財務と運用の仮想エンティティ](https://appsource.microsoft.com/product/dynamics-365/mscrm.finance_and_operations_virtual_entity) を検索します。
2. **今すぐ取得** を選択します。
3. **環境の選択** フィールドに、以前にメモした **環境名** の値を入力します。
4. チェックボックス、次に **インストール** を選択します。

インストールが完了すると、**リソース** \> **Dynamics 365 アプリ** の下の、[Power Platform 管理センター](https://admin.powerplatform.microsoft.com/) で、**財務と運用の仮想エンティティ** を見つけることができます。

詳細については、[財務と運用の仮想エンティティのソリューションの取得](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution) を参照してください。

## <a name="register-an-azure-ad-application"></a><a name='register'></a> Azure AD アプリケーションを登録する

Dataverse によって呼び出しが行えるので、Azure AD アプリケーションを財務と運用アプリと同じテナントに登録する必要があります。

1. [Azure ポータル](https://portal.azure.com) で、**Azure Active Directory \> アプリの登録** に移動します。
2. **新しいアプリケーションの登録** を選択し、以下の情報を入力します。

    - **名前** – 一意の名前を入力します。
    - **アカウント タイプ** - **任意の Azure AD ディレクトリ** を入力します (単一テナントまたはマルチテナント)。
    - **リダイレクト URI** – このフィールドは空白のままにします。

3. **登録** を選択します。
4. 後の手順で必要となるため、**アプリケーション (クライアント) ID** の値をメモしておきます。

    [![Azure AD アプリケーション (クライアント) ID の値。](./media/tcs-dataverse-master-data-lookup-3.png)](./media/tcs-dataverse-master-data-lookup-3.png)

5. アプリケーションの対称キーを作成します。
6. 新しく作成されたアプリケーションで **証明書およびシークレット** を選択します。
7. **新しいクライアント シークレット** を選択します。
8. 説明を入力し、有効期限を選択して、**保存** を選択します。 キーが作成され、表示されます。 その値を後で使用するためにコピーします。

詳細については、[Azure AD アプリケーションの登録](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#register-the-app-in-the-azure-portal) を参照してください。

## <a name="grant-app-permissions-in-finance-and-operations-apps"></a><a name='grant'></a> 財務と運用アプリでアプリのアクセス許可を付与する

Dataverse は、財務と運用アプリを呼び出すために作成した Azure AD アプリケーションを使用します。 したがって、アプリケーションは財務と運用アプリによって信頼され、適切な権限を持つユーザー アカウントに関連付けられている必要があります。 仮想エンティティ機能への権限 **のみ** を持つ特殊サービス ユーザーは、財務と運用アプリで作成される必要があります。 このサービス ユーザーには、その他の権限が設定されている必要はありません。 この手順を完了した後、作成した Azure AD アプリケーションのシークレットを持つアプリケーションによって、この財務と運用アプリ環境を呼び出して仮想エンティティ機能にアクセスできるようになります。

1. ご利用の環境で、**システム管理** \> **ユーザー** \> **ユーザー** へと移動します。
2. **新規** を選択して新しいユーザーを追加し、次のフィールド情報を入力します。

    - **ユーザー ID** - **dataverseintegration** または別の値を入力します。
    - **ユーザー名** - **Dataverse 統合** または別の値を入力します。
    - **プロバイダー** - このフィールドを **NonAAD** に設定します。
    - **ユーザー ID** - **dataverseintegration** または別の値を入力します。 (この値は、有効な電子メール アカウントである必要はありません。)

3. そのユーザーに **CDS 仮想エンティティ アプリケーション** のセキュリティ ロールを割り当てます。
4. **システム ユーザー** を含む他のすべてのロールを削除します。
5. **システム管理** \> **設定** \> **Azure Active Directory アプリケーション** の順に移動して、Dataverse を登録します。 
6. 行を追加し、**クライアント ID** フィールドに、以前にメモした **アプリケーション (クライアント) ID** の値を入力します。
7. **名前** フィールドに、名前を入力します。 たとえば、**Dataverse 統合** と入力します。
8. **ユーザー ID** フィールドで、以前に作成したユーザー ID を入力します。

詳細については、[財務と運用アプリでアプリのアクセス許可を付与する](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#grant-app-permissions-in-finance-and-operations-apps) を参照してください。

## <a name="configure-the-virtual-entity-data-source"></a><a name='configure'></a>仮想エンティティ データ ソースの構成

接続先の財務と運用アプリ インスタンスに Dataverse を提供する必要があります。

1. Dataverse 環境は[手順 1. Microsoft Power Platform 統合を有効にして Dataverse 環境を開く](#enable) からブラウザーで引き続き環境が開いている必要があります。 右側の設定ボタン (ギヤ記号) を選択してから、**詳細設定** を選択します。

    [![Dataverse 環境の詳細設定を開きます。](./media/tcs-dataverse-master-data-lookup-4.png)](./media/tcs-dataverse-master-data-lookup-4.png)

2. **設定** ドロップダウン メニューで、**管理** を選択します。

    [![管理。](./media/tcs-dataverse-master-data-lookup-5.png)](./media/tcs-dataverse-master-data-lookup-5.png)

3. **仮想エンティティ データ ソース** を選択します。

    [![仮想エンティティ データ ソース。](./media/tcs-dataverse-master-data-lookup-6.png)](./media/tcs-dataverse-master-data-lookup-6.png)

4. **財務と運用** という名前のデータ ソースを選択します。

    [![財務と運用データ ソース。](./media/tcs-dataverse-master-data-lookup-7.png)](./media/tcs-dataverse-master-data-lookup-7.png)

5. 前の手順から次の情報を入力します。

    - **ターゲット URL** - 財務と運用アプリにアクセスできる URL を入力します。
    - **OAuth URL** - `https://login.windows.net/` を入力します。
    - **テナント ID** - テナントを指定します。 Contosoこの値は、会社の電子メールのドメイン名です (contoso.com など)。
    - **AAD アプリケーション ID** - 以前に作成した **アプリケーション (クライアント) ID** を入力します。
    - **AAD アプリケーション シークレット** - 以前に生成されたシークレットを入力します。
    - **AAD リソース** - **00000015-0000-0000-c000-000000000000** を入力します。 この値は、財務と運用アプリを表す Azure AD アプリケーションです。 常にこの同じ値を使用する必要があります。

6. 変更を保存します。
7. ページを閉じて **管理** ページに戻り、[手順 6. Dataverse 仮想エンティティを有効にする](#virtual) を開始します。

    [![編集のためにエンティティを閉じます。](./media/tcs-dataverse-master-data-lookup-8.png)](./media/tcs-dataverse-master-data-lookup-8.png)

詳細については、[仮想エンティティ データ ソースの構成](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#configure-the-virtual-entity-data-source) を参照してください。

## <a name="enable-dataverse-virtual-entities"></a><a name='virtual'></a> Dataverse 仮想エンティティを有効化する

税務計算コンフィギュレーションで消費される前に、財務と運用アプリからの仮想エンティティの可視性を **はい** に設定する必要があります。

> [!NOTE]
> [手順 8. 税計算用に接続されているアプリケーションを設定する](#import) をワン クリックして税計算関連の仮想エンティティを有効にすると、この手順をスキップすることができます。 ただし、財務と運用アプリおよび Dataverse 間の接続が正しく接続されていることを示すために、少なくとも 1 つの仮想エンティティを手動で有効にすることをお勧めします。

1. Dataverse 環境の、**管理** ページで、右上隅にあるフィルター ボタン (じょうごのアイコン) を選択します。

    [![フィルター ボタン。](./media/tcs-dataverse-master-data-lookup-9.png)](./media/tcs-dataverse-master-data-lookup-9.png)

2. **高度な検索** ウィンドウの **検索** フィールドで、**利用可能な財務と運用エンティティ** を選択します。
3. 次のルールを追加します: **名前** - **次の値を含む** - **CompanyInfoEntity**。 次に **結果** を選択します。

    [![高度な検索ウィンドウ。](./media/tcs-dataverse-master-data-lookup-10.png)](./media/tcs-dataverse-master-data-lookup-10.png)

4. 検索結果で **CompanyInfoEntity** を選択し、**表示** チェックボックスをオンにして、**保存** を選択します。

    [![エンティティの可視性の設定。](./media/tcs-dataverse-master-data-lookup-11.png)](./media/tcs-dataverse-master-data-lookup-11.png)

5. 税計算コンフィギュレーションで参照される次のエンティティに対して、上記の手順を繰り返します。

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeadingEntity
    - VendVendorV2Entity
    - InventOperationalSiteV2Entity
    - TaxExemptCodeEntity
    - InventWarehouseEntity

    > [!NOTE]
    > Dataverse から取得でき、税計算コンフィギュレーションのドロップダウン リストで使用できるのは、エンティティの最初の 5,000 レコードのみです。

詳細については、[Microsoft Dataverse 仮想エンティティの有効化](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md) を参照してください。

## <a name="set-up-the-connected-application-for-tax-calculation"></a><a name='set-up'></a> 税計算用に接続されているアプリケーションを設定する

1. RCS で、**機能管理** ワークスペースを開き、次の機能を有効にします。

    - 電子報告 Dataverse データ ソース サポート
    - 税サービス Dataverse のデータソースのサポート
    - グローバリゼーション機能

2. **電子申告**、次に **関連リンク** セクションに移動し、**接続されているアプリケーション** を選択します。

    [![接続されているアプリケーション。](./media/tcs-dataverse-master-data-lookup-12.png)](./media/tcs-dataverse-master-data-lookup-12.png)

3. **新規** を選択してレコードを追加し、次の情報を入力します。

    - **名前** – 名前を入力します。
    - **タイプ** - **Dataverse** を選択します。
    - **アプリケーション** - [手順 1. Microsoft Power Platform 統合を有効化し Dataverse 環境を開く](#enable) でメモした Dataverse 環境の **環境 URL** 値を入力します。
    - **テナント** - テナントを入力します。
    - **カスタム URL** - Dataverse URL を入力し、**/api/data/v9.1** を追加します。

4. **接続の確認** を選択し、表示されるダイアログ ボックスで、**選択したリモート アプリケーションに接続するには、ここをクリックする** を選択します。

    [![接続を確認します。](./media/tcs-dataverse-master-data-lookup-13.png)](./media/tcs-dataverse-master-data-lookup-13.png)
5. 「成功!」を受け取ることを確認する 接続が正常に確立されたことを示すメッセージです。

    [![成功メッセージ。](./media/tcs-dataverse-master-data-lookup-14.png)](./media/tcs-dataverse-master-data-lookup-14.png)

## <a name="import-and-set-up-the-dataverse-model-mapping-configuration"></a><a name='import'></a> Dataverse モデル マッピング コンフィギュレーションをインポートし、設定する

Microsoft は、財務と運用アプリから税計算へのエンティティの既定のモデル マッピング コンフィギュレーションを提供します。

1. RCS で **電子申告** に移動します。
2. **コンフィギュレーション プロバイダー** セクションで、**Microsoft** プロバイダーのタイルの **リポジトリ** をクリックします。

    [![リポジトリ。](./media/tcs-dataverse-master-data-lookup-15.png)](./media/tcs-dataverse-master-data-lookup-15.png)

3. **グローバル コンフィギュレーション リポジトリ** を選択し、次に **開く** を選択します。
4. **税金データ モデル**\>**税計算データ モデル** の下で、**Dataverse モデル マッピング** コンフィギュレーションを選択します。
5. **バージョン** クィックタブで、財務と運用アプリのバージョンに一致するバージョンを選択し、**インポート** を選択します。

    [![Dataverse モデル マッピング コンフィギュレーションのインポート。](./media/tcs-dataverse-master-data-lookup-16.png)](./media/tcs-dataverse-master-data-lookup-16.png)

    > [!IMPORTANT]
    > **Dataverse モデル マッピング** コンフィギュレーションは、その最大のインポート バージョンでのみ有効です。 したがって、実装する予定の税計算コンフィギュレーションのバージョンより高い **Dataverse モデル マッピング** コンフィギュレーションのバージョンをインポートすることはできません。 たとえば、税計算コンフィギュレーションのバージョン 40.50.225 を実装する予定の場合、**Dataverse モデル マッピング** コンフィギュレーションのバージョン 40.50.13 のみをインポートする必要があります。 バージョン 40.54.14 をインポートすべきではありません。 そうしない場合、コンフィギュレーションにデータ モデルの不一致が生じる可能性があります。

6. **電子申告** に戻り、**税コンフィギュレーション** タイルを選択します。
7. インポートした **Dataverse モデル マッピング** コンフィギュレーションを選択し、次に **編集** を選択します。
8. **モデル マッピングの既定値** オプションを **はい** に設定します。
9. **接続されたアプリケーション** フィールドで、[手順 7. 税計算用に接続されているアプリケーションを設定する](#set-up) で設定した接続されているアプリケーションを選択します。
10. **仮想テーブルの表示の設定** オプションを **はい** に設定し、税計算関連のすべての仮想エンティティを表示します。

これでマスター データ検索機能の設定が完了しました。 Dynamics 365 Finance からの **法人**、**仕入先**、**品目コード**、**配送条件** などのフィールドのドロップダウン リストは、**税計算機能バージョン** 設定で有効になります。

[![法人エンティティ ドロップダウン リスト。](./media/tcs-dataverse-master-data-lookup-17.png)](./media/tcs-dataverse-master-data-lookup-17.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
