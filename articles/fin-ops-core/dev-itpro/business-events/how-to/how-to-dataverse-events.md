---
title: Dataverse のイベントをサブスクライブする
description: この記事では、財務と運用アプリのビジネス イベントおよび Microsoft Dataverse データ イベントをサブスクライブして管理する方法について説明します。
author: jaredha
ms.date: 11/08/2021
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-11-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8493ae6b556a87be341db61dda0539f3f7a441f8
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111520"
---
# <a name="subscribe-to-events-in-dataverse"></a>Dataverse のイベントをサブスクライブする

[!include[banner](../../includes/banner.md)]

> [!IMPORTANT]
> 財務と運用アプリのビジネス イベントと Microsoft Dataverse のデータ イベントに登録する前に、Microsoft Power Platform 統合を有効にする必用があります。 財務と運用アプリ環境の Microsoft Power Platform 統合を有効にする方法の詳細については、[Power Platform 統合の有効化](../../power-platform/enable-power-platform-integration.md) を参照してください。

Dataverse のイベントでプラグインとソフトウェア開発キット (SDK) のステップを登録することにより、財務と運用アプリのビジネス イベントと Dataverse のデータ イベントをサブスクライブすることができます。 この記事では、Visual Studio の Power Platform Tools の拡張機能を使用して、財務と運用アプリ イベントのプラグインを登録する方法について説明します。 サブスクリプションは、財務と運用アプリのビジネス イベント カタログ内の他のサブスクリプションと共に表示されます。 エンドポイントは、財務と運用アプリのビジネス イベント カタログの他のエンドポイントと同じように動作します。

## <a name="set-up-your-development-environment"></a>開発環境を設定する

### <a name="install-the-power-platform-tools-extension"></a>Power Platform Tools の拡張機能をインストールする

Visual Studio 用 Power Platform Tools は、Dataverse プラグインのコード テンプレートを提供する拡張機能です。これには、テーブル、ビジネス イベント、および仮想エンティティ データ イベントを表示する Dataverse エクスプローラーが含まれます。 エクスプローラにより、Visual Studio からプラグインを直接登録することができます。 その後、プラグインの C# のコードをソリューションから直接 Dataverse に配置することができます。

Power Platform Tools の拡張機能をインストールする方法については、[Power Platform Tools をインストールする](/powerapps/developer/data-platform/tools/devtools-install)を参照してください 。

### <a name="create-a-project"></a>プロジェクトの作成

Power Platform Tools の拡張機能をインストールした後、新しいプロジェクトを作成します。

1. Visual Studio 2019 以降を開きます。
2. **開始する** ダイアログ ボックスで、**新しいプロジェクトを作成する** を選択します。
3. **新しいプロジェクトを作成する** ダイアログ ボックスで、**Power Platform ソリューション テンプレート** を検索して選択し、**次へ** を選択します。

    ![新しいプロジェクトを作成するダイアログ ボックスで Power Platform ソリューション テンプレートを選択しています。](../media/businessevents_SelectSolutionTemplate.png)

4. **新しいプロジェクトをコンフィギュレーションする** ダイアログ ボックスでプロジェクト名を入力し、ソリューション ファイルを保存する場所を選択して、**作成** を選択します。
5. **Microsoft Power Platform ソリューションをコンフィギュレーションする** ダイアログ ボックスの **1. コンフィギュレーションするソリューション タイプ** の下で、**Dataverse から開始する** を選択します。
6. **Power Platform Tools** ダイアログ ボックスの **2. Dataverse に接続する** の下で、次の手順に従います。

    1. **配置のタイプ** フィールド グループで、**Office 365** のオプションを選択します。
    2. **使用可能な組織のリストを表示する** チェック ボックスを選択します。
    3. **ログイン** を選択し、資格情報を入力して、財務と運用アプリ環境にリンクされている Dataverse 環境にサイン インします。
    4. 組織のリスト内で、作業する Microsoft Power Platform 環境を選択します。 その後、**ログイン** を選択します。
    5. **次へ** を選択します。

    ![Power Platform Tools ダイアログ ボックスで Dataverse に接続します。](../media/businessevents_PowerPlatformToolsConnectToDataverse.png)

7. **3. ソリューションを選択する** の下で、イベントのサブスクリプションを作成する Microsoft Power Platform ソリューションを選択します。 まだソリューションを作成していない場合、[ソリューションを作成する](/powerapps/maker/data-platform/create-solution)の手順に従い、Power Apps 作成者ポータルで作成することができます。

    ![Power Platform Tools ダイアログ ボックスでソリューションを選択しています。](../media/businessevents_PowerPlatformToolsSelectSolution.png)

8. **完了** を選択します。
9. **Visual Studio テンプレートの選択 Microsoft Power Platform** ダイアログ ボックスの **1. テンプレートのアイテムを選択する** の下で、**新しいテンプレートを追加する** を選択します。

    ![Visual Studio テンプレートの選択 Microsoft Power Platform ダイアログ ボックスで新しいテンプレートを選択して追加します。](../media/businessevents_PowerPlatformToolsSelectItemsForTemplate.png)

10. **新しいアイテムを作成する** ダイアログ ボックスの **2. 選択したテンプレート プロジェクト** の下で、**プラグイン プロジェクトを追加する** チェック ボックスを選択し、**次へ** を選択します。
11. **3. プロジェクト名を割り当てる** の下にある **プラグイン** フィールドに、プラグイン プロジェクトの名前を入力します。 名前は Visual Studio プロジェクトの名前になります。 既定では、アセンブリの名前にも使用されます。

    ![新しいアイテムを作成するダイアログ ボックスでプラグインのプロジェクトを追加しています。](../media/businessevents_PowerPlatformToolsCreateNewItems.png)

12. **完了** を選択します。

Power Platform Tools の拡張機能を使用してプロジェクトを作成する方法の詳細については、[クイックスタート: Power Platform Tools プロジェクトを作成する](/powerapps/developer/data-platform/tools/devtools-create-project)を参照してください。

### <a name="sign-the-assemblies"></a>アセンブリに署名する

Dataverse アセンブリは署名されている必要があります。 ソリューションで自己署名のキーを設定するか、使用可能な場合は別のキーを指定します。 自己署名のキーを作成するには、次の手順に従います。

1. Visual Studio のソリューション エクスプローラーで、プロジェクト名を選択して保留にし (または右クリック)、**プロパティ** を選択します。
2. **署名** タブで、**アセンブリに署名する** チェック ボックスを選択します。
3. **厳密な名前のキー ファイルを選択する** フィールドで、**新規** を選択します。
4. キーの名前とパスワードを入力し、**OK** を選択します。

## <a name="subscribe-to-a-finance-and-operations-apps-event"></a>財務と運用アプリ イベントをサブスクライブする

開発環境の設定が完了したら、コードの記述を開始できます。 プラグインがサブスクライブされている財務と運用アプリのビジネス イベントまたはデータ イベントが発生するときに、Dataverse でビジネス ロジックを実行する C# クラス ライブラリを作成することができます。

### <a name="register-a-new-step"></a>新しい手順を登録する

1. Visual Studio の **表示** メニューで、**Power Platform エクスプローラー** を選択します。

    Power Platform エクスプローラーに、開発環境の設定中に選択した Dataverse 環境から取得されたコンポーネントのリストが表示されます。 これらのコンポーネントには、テーブル、選択肢、およびイベント カタログが含まれます。

2. **イベント カタログ** ノードの下に、**財務と運用** を展開します。

    **財務と運用** ノードの下に、選択した Microsoft Power Platform 環境の **Dynamics 365 ERP 仮想エンティティ** ソリューションで使用可能なカタログの一覧が表示されます。 各カタログの下で、環境内のカテゴリに対して生成された仮想エンティティのリスト、および各仮想エンティティについて使用可能なデータ イベント (**作成後**、**更新後**、および **削除後**) が表示されます。 

    (**財務と運用** ノードの下にカタログが表示されない場合、ソリューションに必要な仮想エンティティを生成して有効にする必要があるかもしれません。 Dataverse 環境で仮想エンティティを生成する方法の詳細については、[Microsoft Dataverse 仮想エンティティを有効にする](../../power-platform/enable-virtual-entities.md)を参照してください。 (必要な仮想エンティティを有効にした後、Power Platform エクスプローラーで **更新** を選択すると、リストが更新されてエンティティが表示されます。)

    各カタログの **グローバル** ノードの下で、カテゴリに対して有効にされているすべての財務と運用アプリのビジネス イベントが表示されます。

3. ビジネス ロジックをトリガーする必要のある仮想エンティティの下でデータ イベントを選択して保留 (または右クリック) し、**プラグインを追加する** を選択します。

    ![Power Platform エクスプローラーで作業者エンティティの OnExternalCreated イベントにプラグインを追加しています。](../media/businessevents_RegisterWorkerPlugin.png)

4. **新しい手順を登録する** ダイアログ ボックスで、次の手順に従います。

    1. **クラス名** フィールドで、値を作成するクラスの名前に変更します。
    2. **実行のイベント パイプライン ステージ** の下にあるドロップダウン リストで **PostOperation** を選択します。
    3. **実行モード** で、**非同期** オプションを選択します。
    4. **新しい手順を登録する** を選択します。

    > [!NOTE]
    > 現在、**PreValidation** および **PreOperation** 実行ステージと **同期** 実行モードは、仮想エンティティに対してはサポートされていません。

    ![新しい手順を登録するダイアログ ボックスで、新しいプラグインの手順を登録します。](../media/businessevents_PowerPlatformToolsRegisterNewStep.png)

新しい手順を登録するとき、プラグインの基本コードを含む新しいクラスが生成されます。 新しいクラスの **ExecuteCdsPlugin** メソッド内において、**TODO** で示される場所にカスタム ビジネス ロジックを記述することができます。 その後、ソリューションをビルドし、プラグインを環境に配置することができます。

## <a name="deploy-the-plug-in"></a>プラグインを配置する

プラグインを Microsoft Power Platform ソリューションに配置できるようになりました。

- Visual Studio のソリューション エクスプローラーで、プロジェクトを保留 (または右クリック) し、**配置** を選択します。

配置が正常に行われたことを確認するために、Power Apps 作成者ポータルでプラグインのアセンブリを表示することができます。 プラグインを配置した Microsoft Power Platform ソリューションに移動し、左側のナビゲーションで **プラグイン アセンブリ** を選択します。 登録済のプラグインの手順を表示するには、ナビゲーションで **プラグインの手順** を選択します。

![Power Apps 作成者ポータルのプラグイン アセンブリ。](../media/businessevents_PowerPlatformToolsPluginAssemblies.png)

財務と運用アプリの **ビジネス イベント** ページの **エンドポイント** タブで新しいエンドポイントが正しく表示されていること、および新しいイベントが **有効なイベント** タブに表示されていることを確認することもできます。

![ビジネス イベント ページの有効なイベント タブにある Dataverse イベント。](../../media/businessevents_PowerPlatformToolsFinOpsEvents.png)

## <a name="troubleshooting"></a>トラブルシューティング

配置に失敗した場合、詳細ログを有効にして問題のトラブルシューティングをすることができます。

1. Visual Studio の **ツール** メニューで、**オプション** を選択します。
2. **オプション** ダイアログ ボックスの **Power Platform Tools** ノードの下にある **一般** を選択します。
3. **詳細なログ データを表示する** および **(診断) Dataverse の詳細な通信ログ** を選択します。
4.  **OK** を選択します。

