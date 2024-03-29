---
title: Inventory Visibility Add-in をインストールする
description: この記事では、Microsoft Dynamics 365 Supply Chain Management Inventory Visibility アドインのインストールの方法を説明します。
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: c08568b14d7f5c79a1d3609107a88f905498ce2b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762784"
---
# <a name="install-and-set-up-inventory-visibility"></a>Inventory Visibility のインストールと設定

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Supply Chain Management Inventory Visibility アドインのインストールの方法を説明します。

[Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/v2) を使用して、Inventory Visibility アドインをインストールする必要があります。 Lifecycle Services は、財務と運用アプリのアプリケーション ライフサイクルを管理するのをサポートする定期的に更新されるサービスと環境を提供するコラボレーション ポータルです。 詳細については、 [Lifecycle Services のリソース](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md) を参照してください。

> [!TIP]
> Inventory Visibility アドイン ユーザー グループに参加することをお勧めします。このグループでは、役立つガイドを見つけて最新の更新プログラムを取得し、Inventory Visibility の使用に関するご質問を投稿することができます。 参加するには、[inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) の Inventory Visibility 製品チームに電子メールを送信して、それに Supply Chain Management 環境 ID を記載してください。

## <a name="inventory-visibility-prerequisites"></a>Inventory Visibility の前提条件

Inventory Visibility をインストールする前に、以下のタスクを完了する必要があります。

- 少なくとも 1 つの環境が展開されている Lifecycle Services 実装プロジェクトを取得します。
- アドインを設定するための前提条件が完了していることを確認します。 これらの前提条件の詳細については、[アドインの概要](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)を参照してください。 Inventory Visibility にデュアル書き込みリンクは必要ありません。

> [!NOTE]
> 現在サポートされている国と地域には、カナダ (CCA、ECA)、米国 (WUS、EUS)、欧州連合 (NEU、WEU)、英国 (SUK、 WUK)、オーストラリア (EAU、SEAU)、日本 (EJP、WJP)、ブラジル (SBR、SCUS) があります。

これらの前提条件について質問がある場合は、Inventory Visibility 製品チーム ([inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com)) にお問い合せください。

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Inventory Visibility Add-in をインストールする

アドインをインストールする前に、アプリケーションを登録し、Azure サブスクリプションの下の Azure Active Directory (Azure AD) にクライアント シークレットを追加します。 手順については、[アプリケーションの登録](/azure/active-directory/develop/quickstart-register-app)および[クライアント シークレットの追加](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)を参照してください。 **アプリケーション (クライアント) ID**、**クライアント シークレット**、**テナント ID** の値は後で必要になるので、必ずメモしておいてください。

> [!IMPORTANT]
> 複数の Lifecycle Services 環境を使用する場合は、環境ごとに異なる Azure AD アプリケーションを作成します。 同じアプリケーション ID とテナント ID を使用して異なる環境の Inventory Visibility アドインをインストールした場合、古い環境ではトークンの問題が発生します。 その結果、最後にインストールされたものだけが有効になります。

アプリケーションを登録し、クライアント シークレットを Azure AD に追加した後、次の手順に従って Inventory Visibility アドインをインストールします。

1. [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) にサインインします。
1. ホーム ページで、環境が展開されているプロジェクトを選択します。
1. プロジェクト ページで、アドインをインストールする環境を選択します。
1. 環境ページの **Power Platform 統合** セクションで、**環境アドイン** セクションが表示されるまで下にスクロール ダウンします。 この場所に Dataverse 環境名が表示されます。 Dataverse 環境名が Inventory Visibility に使用する名前であることを確認します。

    > [!NOTE]
    > 現在、Lifecycle Services を使用して作成された Dataverse の環境のみがサポートされています。 Dataverse の環境がその他の方法 (PowerApps 管理センターを使用するなど) で作成され、それが Supply Chain Management 環境にリンクされている場合、Inventory Visibility アドインをインストールする前に、まずマッピングの問題を修正する必要があります。
    >
    > Lifecycle Services を Power Platform 統合に設定していない場合は、二重書き込み環境を Dataverse インスタンスにリンクしている可能性があります。 このリンクの不一致は予期しない動作の原因になる可能性があります。 ビジネスイベント、仮想テーブル、アドインで同じ接続を使用できるように、Lifecycle Services 環境の詳細をデュアルライトで接続しているものと一致させることをお勧めします。マッピングの問題を解決する方法については、[リンクの不一致](../../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#linking-mismatch) を参照してください。 マッピングの問題が解決されると、Inventory Visibility のインストールに進むことができます。

1. **環境アドイン** セクションで、**新しいアドインのインストール** を選択します。

    ![Lifecycle Services の環境ページ](media/inventory-visibility-environment.png "Lifecycle Services の環境ページ")

1. **新しいアドインのインストール** リンクを選択します。 使用可能なアドインの一覧が表示されます。
1. 一覧で **Inventory Visibility** を選択します。
1. 次のフィールドを環境に合わせて設定します。

    - **AAD アプリケーション ID (クライアント) ID** – 先ほど作成してメモした Azure AD アプリケーション ID を入力します。
    - **AAD テナント ID** – 先ほどメモしたテナント IDを入力します。

    ![アドインの設定ページ](media/inventory-visibility-setup.png "アドインの設定ページ")

1. **使用条件** チェック ボックスを選択して、使用条件に同意します。
1. **インストール** を選択します。 アドインの状態は、**インストール中** として表示されます。 インストールが完了したら、ページを更新します。 状態は **インストール済** に変更されます。
1. Dataverse で、左ナビゲーションの **アプリ** セクションを選択し、**Inventory Visibility** Power Apps が正常にインストールされていることを確認します。 **アプリ** セクションが存在しない場合は、Inventory Visibility 製品チーム ([inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com)) にお問い合わせください。

> [!NOTE]
> Lifecycle Services に Inventory Visibility をインストールするアクセス許可がないことを警告された場合は、管理者に連絡してアクセス許可を変更する必要があります。
>
> Lifecycle Services ページからインストールするのに 1 時間以上かかる場合、Dataverse 環境にソリューションをインストールするためのアクセス許可がユーザー アカウントにない可能性があります。 問題を解決するには、次の手順に従います。
>
> 1. Lifecycle Services ページで、Inventory Visibility アドインのインストール プロセスをキャンセルします。
> 1. [Microsoft 365 管理センター](https://admin.microsoft.com) にサインインし、アドインのインストールに使用するユーザー アカウントに "Dynamics 365 Unified Operations 計画" ライセンスが割り当てられているかを確認します。 必要に応じてライセンスを割り当てます。
> 1. 関連するユーザー アカウントを使用して [Power Platform 管理センター](https://admin.powerplatform.microsoft.com) にログインします。 次のステップに従って、Inventory Visibility アドインをインストールします。
>     1. アドインをインストールする環境を選択します。
>     1. **Dynamics 365 アプリ** を選択します。
>     1. **アプリをインストールする** を選択します。
>     1. **Inventory Visibility** を選択する
>
> 1. インストールが完了したら、Lifecycle Services ページに戻ってもう一度やり直し、**Inventory Visibility** アドインを再インストールします。

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Supply Chain Management における Inventory Visibility の設定

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Inventory Visibility 統合パッケージの配置

Supply Chain Management バージョン 10.0.17 以前を実行している場合、[inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) で Inventory Visibility のオンボード サポート チームに連絡してパッケージ ファイルを取得してください。 その後、Lifecycle Services にパッケージを配置します。

> [!NOTE]
> 配置中にバージョンの不一致エラーが発生した場合は、X++ プロジェクトを手動で開発環境にインポートする必要があります。 その後、配置可能パッケージを開発環境に作成し、それを運用環境に配置します。
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
    - *Inventory Visibility 統合* – 必須です。
    - *引当相殺と Inventory Visibility の統合* – 推奨されますが、オプションです。 バージョン 10.0.22 またはそれ以降が必要です。 詳細については、[Inventory Visibility 引当](inventory-visibility-reservations.md) を参照してください。

1. **在庫管理 \> 設定 \> Inventory Visibility 統合パラメーター** の順に移動します。
1. **一般** タブを開き、次の設定を行います。
    - **Inventory Visibility エンドポイント** – Inventory Visibility を実行している環境の URLを入力します。 詳細については、[サービス エンドポイントの検索](inventory-visibility-configuration.md#get-service-endpoint) を参照してください。
    - **1つの要求の最大レコード数** – 1 つの要求に含める レコードの最大数を設定します。 1000 以下の正の整数を入力する必要があります。 既定値は 512 です。 Microsoft サポートからアドバイスを受けた場合や、変更が必要だと確信した場合を除き、デフォルト値のままにしておくことを強くお勧めします。

1. オプションの *引当相殺と Inventory Visibility の統合* 機能を有効にしている場合は、**引当相殺** タブを開き、次の設定を行います。
    - **引当相殺を有効にする** – *はい* に設定し、この機能を有効にします。
    - **引当相殺モディファイア** – Inventory Visibility に対して行われた引当を相殺する在庫トランザクション状態を選択します。 この設定は、相殺をトリガーする注文処理ステージを決定します。 ステージは、注文の在庫トランザクション状態によって追跡されます。 次のいずれかのオプションを選択します。
        - *受注中* – *トランザクション中* の状態では、注文が作成されると相殺要求を送信します。 相殺数量は作成された注文の数量になります。
        - *引当* – *引当注文済トランザクション* 状態では、注文が引当、ピッキング、梱包明細の転記、または請求を行った際に相殺要求を送信します。 要求は前述のプロセスが発生したときの最初のステップに対して、1 度だけトリガーされます。 相殺数量は注文明細行の在庫トランザクション状態が *受注中* から *引当済注文* (またはそれ以降の状態) に変更された数量となります。

1. **在庫管理 \> 定期処理 \> Inventory Visibility 統合** の順に移動し、ジョブを有効します。 Supply Chain Management からのすべての在庫変更イベントが Inventory Visibility に転記されるようになります。

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Inventory Visibility アドインをアンインストールする

Inventory Visibility アドオンをアンインストールするには、次の手順に従います。

1. Supply Chain Management にサインインします。
1. **在庫管理 \> 定期処理 \> Inventory Visibility の統合** の順に移動し、ジョブを無効化します。
1. Lifecycle Services に移動して、アドインをアンインストールする環境のページを開きます ([Inventory Visibility アドインのインストール](#install-add-in) も参照してください)。
1. **アンインストール** を選択します。
1. アンインストール プロセスは現在、Inventory Visibility アドインを終了させ、Lifecycle Services からアドインの登録を解除し、Inventory Visibility アドイン データ キャッシュに保存されている一時的なデータが削除されます。 ただし、Dataverse サブスクリプションに同期されている基本在庫データは依然ここに保管されます。 このデータを削除するには、この手順の残りを完了させます。
1. [Power Apps](https://make.powerapps.com) を開きます。
1. ナビゲーション バーで **環境** を選択します。
1. Lifecycle Services 環境と連携している Dataverse 環境を選択します。
1. **ソリューション** に移動し、次の順序で次のソリューションを削除します。
    1. Dynamics 365 Inventory Visibility – アンカー
    1. Dynamics 365 Inventory Visibility – プラグイン
    1. Dynamics 365 Inventory Visibility – アプリケーション
    1. Dynamics 365 Inventory Visibility – コントロール
    1. Dynamics 365 Inventory Visibility – ベース 

    これらのソリューションを削除すると、テーブルに保存されているデータも削除されます。

> [!NOTE]
> Inventory Visibility アドインをアンインストールした後に Supply Chain Management データベースを復元し、アドインを再インストールする場合は、アドインを再インストールする前に、Dataverse サブスクリプションに保存されている古い Inventory Visibility データを (前の手順の説明に従って) 削除してください。 これによって、データの不整合の問題が発生する可能性がなされます。

## <a name="clean-inventory-visibility-data-from-dataverse-before-restoring-the-supply-chain-management-database"></a><a name="restore-environment-database"></a>Supply Chain Management データベースを復元する前の Dataverse からの Inventory Visibility のクリーンアップ

在庫品目一覧を使用していて、Supply Chain Management のデータベースを復元するには、復元したデータベースに、Dataverse への Inventory Visibility で以前に同期されたデータと一致しなくなったデータが含まれている場合があります。 このデータの不整合によって、システム エラーや他の問題が発生する可能性があります。 したがって、Supply Chain Management の データベースを Dataverse から復元する前に、すべての Inventory Visibility データを常にクリーンアップすることが重要です。

Supply Chain Management のデータベースを復元する必要がある場合は、次の手順に従います。

1. [Inventory Visibility アドインのアンインストール](#uninstall-add-in) に説明がある通り、Inventory Visibility アドインをアンインストールして、Dataverse でのすべての関連データを削除します
1. Supply Chain Management のデータベースを、たとえば [データベースの時点管理 (PITR)](../../fin-ops-core/dev-itpro/database/database-point-in-time-restore.md) または [実稼働データベースのサンドボックス環境へのポイントインタイム復元](../../fin-ops-core/dev-itpro/database/database-pitr-prod-sandbox.md) で説明されているように復元します。
1. それでも使いたい場合は、[Inventory Visibility アドインのインストール](#install-add-in) と [Inventory Visibility 統合の設定](#setup-inventory-visibility-integration) にある通り Inventory Visibility アドインを設定します


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
