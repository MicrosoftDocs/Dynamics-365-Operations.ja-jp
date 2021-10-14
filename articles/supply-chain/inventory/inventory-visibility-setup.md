---
title: Inventory Visibility Add-in をインストールする
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
ms.openlocfilehash: d6f58eab38d1aee97a5d39704255bf06a168b36c
ms.sourcegitcommit: 79d19924ed736c9210fa9ae4e0d4c41c53c27eb5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2021
ms.locfileid: "7581868"
---
# <a name="install-and-set-up-inventory-visibility"></a>在庫視覚化のインストールと設定

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management の在庫視覚化アドインのインストールの方法を説明します。

Microsoft Dynamics Lifecycle Services (LCS) を使用して、在庫可視化アドインをインストールする必要があります。 LCS は、財務および操作アプリのアプリケーション ライフサイクルを管理するのをサポートする定期的に更新されるサービスと環境を提供するコラボレーション ポータルです。

詳細については、 [Lifecycle Services のリソース](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md) を参照してください。

## <a name="inventory-visibility-prerequisites"></a>在庫視覚化の前提条件

在庫可視化をインストールする前に、以下のタスクを完了する必要があります。

- 少なくとも 1 つの環境が展開されている LCS 実装プロジェクトを取得します。
- アドインを設定するための前提条件が完了していることを確認します。 これらの前提条件の詳細については、[アドインの概要](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)を参照してください。 在庫の視覚化にデュアル書き込みリンクは必要ありません。

> [!NOTE]
> 現在サポートされている国と地域には、カナダ (CCA、ECA)、米国 (WUS、EUS)、欧州連合 (NEU、WEU)、英国 (SUK、 WUK)、オーストラリア (EAU、SEAU)、日本 (EJP、WJP)、ブラジル (SBR、SCUS) があります。

これらの前提条件について質問がある場合は、在庫可視化製品チーム ([inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com)) にお問い合せください。

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Inventory Visibility Add-in をインストールする

アドインをインストールする前に、アプリケーションを登録し、Azure 定期購読の下の Azure Active Directory (Azure AD) にクライアント シークレットを追加します。 手順については、[アプリケーションの登録](/azure/active-directory/develop/quickstart-register-app)および[クライアント シークレットの追加](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)を参照してください。 **アプリケーション (クライアント) ID**、**クライアント シークレット**、および **テナント ID** の値は後で必要になるので、必ずメモしておいてください。

アプリケーションを登録し、クライアント シークレットを Azure AD に追加した後、次の手順に従って在庫視覚化アドインをインストールします。

1. [LCS](https://lcs.dynamics.com/Logon/Index) にサインインします。
1. ホーム ページで、環境が展開されているプロジェクトを選択します。
1. プロジェクト ページで、アドインをインストールする環境を選択します。
1. 環境ページの **Power Platform 統合** セクションで、**環境アドイン** セクションが表示されるまで下にスクロール ダウンします。 この場所に Dataverse 環境名が表示されます。 Dataverse 環境名が在庫可視化に使用する名前であることを確認します。

    > [!NOTE]
    > 現在、LCSを使用して作成された Dataverse の環境のみがサポートされています。 Dataverse 環境が何らかの別の方法 (例えば、Power Apps 管理センターを使用して) で作成され、Supply Chain Management 環境にリンクされている場合は、まず在庫可視化製品チーム ([inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com)) にお問い合わせいただき、マッピングの問題を解決する必要があります。 その後、在庫可視化をインストールできます。

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
1. Dataverse で、左ナビゲーションの **アプリ** セクションを選択し、**在庫可視化** Power Apps が正常にインストールされていることを確認します。 **アプリ** セクションが存在しない場合は、在庫可視化製品チーム ([inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com)) にお問い合わせください。

> [!IMPORTANT]
> 複数の LCS 環境を使用する場合は、環境ごとに異なる Azure AD アプリケーションを作成します。 同じアプリケーション ID とテナント ID を使用して異なる環境の在庫視覚化アドインをインストールした場合、古い環境ではトークンの問題が発生します。 最後にインストールされたものだけが有効になります。

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>在庫可視化アドインをアンインストールする

在庫可視化アドインをアンインストールするには、LCS ページで **アンインストール** を選択します。 アンインストール プロセスは、在庫可視化アドインを終了させ、LCS からアドインの登録を解除し、在庫可視化アドイン データ キャッシュに保存されている一時的なデータが削除されます。 ただし、Dataverse 定期購読に保存されている基本在庫データは削除されません。

Dataverse 定期購読に保存されている在庫データをアンインストールするには、[Power Apps](https://make.powerapps.com) を開き、ナビゲーション バーの **環境** を選択し、LCS 環境と連携している Dataverse 環境を選択します。 次に、**ソリューション** に移動し、次の 5 つのソリューションをこの順序で削除します:

1. Dynamics 365 ソリューションが含む在庫品目一覧アプリケーションのアンカー ソリューション。
1. Dynamics 365 FNO SCM Inventory Visibility アプリケーション ソリューション
1. 在庫サービス コンフィギュレーション
1. 在庫品目一覧スタンドアロン
1. Dynamics 365 FNO SCM Inventory Visibility の基準ソリューション

これらのソリューションを削除すると、テーブルに保存されているデータも削除されます。

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Supply Chain Management における在庫視覚化の設定

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

アドインをインストールしたら、次の手順に従って Supply Chain Management システムを動作させる準備をします。

1. Supply Chain Management で、**[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** ワークスペースを開き、以下の機能を有効にします。
    - *在庫視覚化統合* – 必須です。
    - *引当相殺と在庫視覚化の統合* – 推奨されますが、オプションです。 バージョン 10.0.22 またはそれ以降が必要です。 詳細については、[在庫の視覚化引当](inventory-visibility-reservations.md) を参照してください。

1. **在庫管理 \> 設定 \> 在庫視覚化統合パラメーター** の順に移動します。
1. **一般** タブを開き、次の設定を行います。
    - **在庫視覚化エンドポイント** – 在庫視覚化を実行している環境の URLを入力します。 詳細については、[サービス エンドポイントの検索](inventory-visibility-configuration.md#get-service-endpoint) を参照してください。
    - **1つの要求の最大レコード数** – 1 つの要求に含める レコードの最大数を設定します。 1000 以下の正の整数を入力する必要があります。 既定値は 512 です。 Microsoft サポートからアドバイスを受けた場合や、変更が必要だと確信した場合を除き、デフォルト値のままにしておくことを強くお勧めします。

1. オプションの *引当相殺と在庫視覚化の統合* 機能を有効にしている場合は、**引当相殺** タブを開き、次の設定を行います。
    - **引当相殺を有効にする** – *はい* に設定し、この機能を有効にします。
    - **引当相殺モディファイア** – 在庫視覚化に対して行われた引当を相殺する在庫トランザクション状態を選択します。 この設定は、相殺をトリガーする注文処理ステージを決定します。 ステージは、注文の在庫トランザクション状態によって追跡されます。 次のいずれかを選択します : 
        - *受注中* – *トランザクション中* の状態では、注文が作成されると相殺要求を送信します。 相殺数量は作成された注文の数量になります。
        - *引当* – *引当注文済トランザクション* 状態では、注文が引当、ピッキング、梱包明細の転記、または請求を行った際に相殺要求を送信します。 要求は前述のプロセスが発生したときの最初のステップに対して、1 度だけトリガーされます。 相殺数量は注文明細行の在庫トランザクション状態が *受注中* から *引当済注文* (またはそれ以降の状態) に変更された数量となります。

1. **在庫管理 \> 定期処理 \> 在庫の視覚化統合** の順に移動し、ジョブを有効します。 Supply Chain Management からのすべての在庫変更イベントが在庫の視覚化に転記されるようになります。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
