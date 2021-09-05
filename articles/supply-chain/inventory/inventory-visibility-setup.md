---
title: 在庫視覚化を設定する
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management の在庫視覚化アドインのインストールの方法を説明します。
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 8573fe01abb1c6092012baf85e8b7df40b74a31f
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343587"
---
# <a name="set-up-inventory-visibility"></a>在庫視覚化を設定する

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management の在庫視覚化アドインのインストールの方法を説明します。

Microsoft Dynamics Lifecycle Services (LCS) を使用して、在庫可視化アドインをインストールする必要があります。 LCS は、財務および操作アプリのアプリケーション ライフサイクルを管理するのをサポートする定期的に更新されるサービスと環境を提供するコラボレーション ポータルです。

詳細については、 [Lifecycle Services のリソース](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md) を参照してください。

## <a name="inventory-visibility-prerequisites"></a>在庫視覚化の前提条件

在庫可視化をインストールする前に、以下のタスクを完了する必要があります。

- 少なくとも 1 つの環境が展開されている LCS 実装プロジェクトを取得します。
- アドインを設定するための前提条件が完了していることを確認します。 これらの前提条件の詳細については、[アドインの概要](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)を参照してください。 在庫の視覚化にデュアル書き込みリンクは必要ありません。
- 以下の必要なファイルを入手するため、[inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) の在庫視覚化製品チームにお問い合わせください。

    - `InventoryServiceApplication.PackageDeployer.zip`
    - `Inventory Visibility Integration.zip` (実行している Supply Chain Management がバージョン 10.0.18 より以前のバージョンの場合)

> [!NOTE]
> 現在サポートされている国と地域には、カナダ (CCA、ECA)、米国 (WUS、EUS)、欧州連合 (NEU、WEU)、英国 (SUK、 WUK)、オーストラリア (EAU、SEAU) があります。

これらの前提条件についてご不明な点がありましたら、在庫可視化製品チームにお問い合わせください。

## <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>Dataverse を設定する

Dataverse を在庫可視化で使用できるよう設定するため、Package Deployer ツールを使用して、在庫可視化パッケージを展開します。 次のサブセクションでは、これらの各タスクの完了方法について説明します。

> [!NOTE]
> 現在、LCSを使用して作成された Dataverse の環境のみがサポートされています。 Dataverse 環境が何らかの別の方法で作成されている場合 (たとえば、Power Apps 管理者センターを使用している場合)、および Supply Chain Management 環境にリンクされている場合は、まず在庫可視化製品チームに問い合わせ、マッピングの問題を解決する必要があります。 その後、在庫可視化をインストールできます。

### <a name="migrate-from-an-old-version-of-the-dataverse-solution"></a>Dataverse ソリューションの古いバージョンから移行する

在庫可視化 Dataverse ソリューションの古いバージョンをインストールしてある場合は、次の手順に従ってバージョン を更新してください。 2 つのケースがあります。

- **ケース 1:** Dataverse を手動で設定する場合は、`Inventory Visibility Dataverse Solution_1_0_0_2_managed.zip` ソリューションをインポートし、次の手順に従います。

    1. 次の 3 つのファイルをダウンロードしてください。

        - `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip`
        - `InventoryServiceBase_managed.cab`
        - `InventoryServiceApplication.PackageDeployer.zip`

    1. 次の手順に従って、`Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip` および `InventoryServiceBase_managed.cab` を Dataverse に手動でインポートします。

        1. Dataverse 環境の URLを開きます。
        1. **ソリューション** ページを開きます。
        1. **インポート** を選択します。

    1. package deployer ツールを使用して `InventoryServiceApplication.PackageDeployer.zip` パッケージを展開します。 手順については、このトピックで後述する [package deployer ツールを使用してパッケージを展開する](#deploy-package)セクションを参照してください。

- **ケース 2 :** package deployer ツールを使用して Dataverse を設定する場合、古い `.*PackageDeployer.zip` パッケージをインストールする前に、`InventoryServiceApplication.PackageDeployer.zip` をダウンロードして更新を行ってください。 手順については、[package deployer ツールを使用してパッケージを展開する](#deploy-package)セクションを参照してください。

### <a name="use-the-package-deployer-tool-to-deploy-the-package"></a><a name="deploy-package"></a>package deployer ツールを使用してパッケージを展開する

1. [NuGet からツールをダウンロードする](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget)に従って、開発者ツールをインストールします。
1. 次の手順に従って、チーム グループからダウンロードした `InventoryServiceApplication.PackageDeployer.zip` ファイルのブロックを解除します。

    1. ファイルを選択したまま (または右クリック) にしてから、**プロパティ** を選択します。
    1. **プロパティ** ダイアログ ボックスの **一般** タブで、**セキュリティ** セクションを検索し、**ブロック解除** を選択して変更を適用します。 **セキュリティ** セクションが **一般** タブにない場合、ファイルはブロックされません。 この場合は、次のステップに進みます。

    ![ダウンロードしたファイルのブロック解除](media/unblock-file.png "ダウンロードしたファイルのブロック解除")

1. `InventoryServiceApplication.PackageDeployer.zip` を解凍し、次の品目を探します。

    - `InventoryServiceApplication` フォルダー
    - `[Content_Types].xml` ファイル
    - `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll` ファイル

1. これらの各品目を `.\Tools\PackageDeployment` ディレクトリにコピーします。 (このディレクトリは、開発者ツールのインストール時に作成されました。)
1. `.\Tools\PackageDeployment\PackageDeployer.exe` を実行し、画面の指示に従ってソリューションをインポートします。

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Inventory Visibility Add-in をインストールする

アドインをインストールする前に、アプリケーションを登録し、Azure 定期購読の下の Azure Active Directory (Azure AD) にクライアント シークレットを追加します。 手順については、[アプリケーションの登録](/azure/active-directory/develop/quickstart-register-app)および[クライアント シークレットの追加](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)を参照してください。 **アプリケーション (クライアント) ID**、**クライアント シークレット**、および **テナント ID** の値は後で必要になるので、必ずメモしておいてください。

アプリケーションを登録し、クライアント シークレットを Azure AD に追加した後、次の手順に従って在庫視覚化アドインをインストールします。

1. [LCS](https://lcs.dynamics.com/Logon/Index) にサインインします。
1. ホーム ページで、環境が展開されているプロジェクトを選択します。
1. プロジェクト ページで、アドインをインストールする環境を選択します。
1. 環境ページの **Power Platform 統合** セクションで、**環境アドイン** セクションが表示されるまで下にスクロール ダウンします。 この場所に Dataverse 環境名が表示されます。
1. **環境アドイン** セクションで、**新しいアドインのインストール** を選択します。

    ![LCS の環境ページ](media/inventory-visibility-environment.png "LCS の環境ページ")

1. **新しいアドインのインストール** リンクを選択します。 使用可能なアドインの一覧が表示されます。
1. 一覧で **在庫視覚化** を選択します。
1. 次のフィールドを環境に合わせて設定します。

    - **AAD アプリケーション ID (クライアント) ID** – 先ほど作成してメモした Azure AD アプリケーション ID を入力します。
    - **AAD テナント ID** – 先ほどメモしたテナント IDを入力します。

    ![アドインの設定ページ](media/inventory-visibility-setup.png "アドインの設定ページ")

1. **使用条件** チェック ボックスを選択して、使用条件に同意します。
1. **インストール** を選択します。 アドインの状態は、**インストール中** として表示されます。 インストールが完了したら、ページを更新します。 状態は **インストール済** に変更されます。

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>在庫可視化アドインをアンインストールする

在庫可視化アドインをアンインストールするには、LCS ページで **アンインストール** を選択します。 アンインストール プロセスは、在庫可視化アドインを終了させ、LCS からアドインの登録を解除し、在庫可視化アドイン データ キャッシュに保存されている一時的なデータが削除されます。 ただし、Dataverse 定期購読に保存されている基本在庫データは削除されません。

Dataverse 定期購読に保存されている在庫データをアンインストールするには、[Power Apps](https://make.powerapps.com) を開き、ナビゲーション バーの **環境** を選択し、LCS 環境と連携している Dataverse 環境を選択します。 次に、**ソリューション** に移動 し、次の 5 つのソリューションを削除します。

- Dynamics 365 ソリューションが含む在庫品目一覧アプリケーションのアンカー ソリューション。
- Dynamics 365 FNO SCM Inventory Visibility アプリケーション ソリューション
- 在庫サービス コンフィギュレーション
- 在庫品目一覧スタンドアロン
- Dynamics 365 FNO SCM Inventory Visibility の基準ソリューション

これらのソリューションを削除すると、テーブルに保存されているデータも削除されます。

## <a name="set-up-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Supply Chain Management を設定する

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>在庫の視覚化統合パッケージの配置

Supply Chain Management バージョン 10.0.17 以前を実行している場合、[inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) で在庫の視覚化のオンボード サポート チームに連絡してパッケージ ファイルを取得してください。 その後、LCS にパッケージを配置します。

> [!NOTE]
> 配置中にバージョンの不一致エラーが発生した場合は、X++ プロジェクトを手動で開発環境にインポートする必要があります。 その後、配置可能パッケージを開発環境に作成し、それを実稼働環境に配置します。
>
> このコードは Supply Chain Management バージョン 10.0.18 に含まれています。 そのバージョン以降を実行する場合、配置は必須ではありません。

Supply Chain Management 環境で次の機能が有効になっていることを確認してください。 (既定では、有効になっています。)

| 機能の説明 | コード バージョン | トグル クラス |
|---|---|---|
| InventSum テーブルで在庫分析コードの使用の有効化または無効化      | 10.0.11 | InventUseDimOfInventSumToggle      |
| InventSumDelta テーブルで在庫分析コードの使用の有効化または無効化 | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Inventory Visibility 統合の設定

1. Supply Chain Management で、**[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** ワークスペースを開き、在庫の可視性の *在庫の視覚化統合* 機能を有効にします。
1. **在庫管理 \> 設定 \>在庫の視覚化統合パラメーター** の順に移動し、実行している在庫の視覚化で環境の URL を入力します。 詳細については、[サービス エンドポイントの検索](inventory-visibility-power-platform.md#get-service-endpoint) を参照してください。
1. **在庫管理 \> 定期処理 \> 在庫の視覚化統合** の順に移動し、ジョブを有効します。 Supply Chain Management からのすべての在庫変更イベントが在庫の視覚化に転記されるようになります。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
