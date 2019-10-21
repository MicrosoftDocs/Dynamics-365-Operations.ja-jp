---
title: 継続的なビルドとテストの自動化をサポートする環境を配置して使用する
description: このトピックでは、継続的なビルドとテストの自動化をサポートする開発者トポロジを配置する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 02/22/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 13171
ms.assetid: ''
ms.search.region: Global
ms.author: shailesn
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5182bc14a07a0972602d2ff55a1f39934acf73a6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191812"
---
# <a name="deploy-and-use-an-environment-that-supports-continuous-build-and-test-automation"></a>継続的なビルドとテストの自動化をサポートする環境を配置して使用する

[!include [banner](../includes/banner.md)]

このトピックでは継続的なビルドとテストの自動化をサポートする環境を配置して使用する方法を説明します。

## <a name="prerequisites"></a>必要条件

仮想マシン (VM) のクラウド配置には Microsoft Azure DevOps サブスクリプションが必要です。

## <a name="workflow"></a>ワークフロー

Microsoft Dynamics Lifecycle Services (LCS) で Azure DevOps サブスクリプションを構成した後、LCS を使用して開発者 VM やビルド / テスト VM を配置できます。 LCS は開発 VM を構成し、それは Azure DevOps プロジェクトにマップされます。 LCS は、ビルド VM も構成します。ビルド VM は、自動的に Azure DevOps プロジェクトにマップされ、Azure DevOps プロジェクトのモジュールを構成するビルド エージェント / コントローラーを持ち、妥当性確認のための外部エンドポイントを持つ自動化テストを実行します。 次の図は通常のワークフローを示します。

![LCS、Azure DevOps、および VM の関係](./media/deploy-build-test.png)

このワークフローには、Azure の開発者 VM とビルド / テスト VM の LCS 配置が含まれています。

+ LCS は Azure で開発およびビルド / テスト環境を作成します。 ビルド / テスト環境を作成するためには、LCS は Azure DevOps プロジェクトのソース コードがどこにあるか特定できる必要があります。
+ 開発者は開発者 VM のソース コードで作業し、その作業は Azure DevOps プロジェクトに同期されます。
+ ビルドプロセスによって、コードがAzure DevOpsからビルド / テスト VM に同期され、配置可能なパッケージが作成され、サンドボックスおよび実稼動環境に適用できるようになります。 ソース コードは、開発 VM からビルド / テスト VM への直接フローを持ちません。 これらは Azure DevOps を通して同期されます。

カスタム テスト コードの記述またはビルド インフラストラクチャと統合するための自動テスト コードを生成する方法の詳細は、[テストと検証](testing-validation.md) を参照してください。

## <a name="set-up-azure-devops"></a>Azure DevOps の設定

### <a name="choose-a-plan"></a>計画を選択

最初のステップは組織に [Azure DevOps プランを選ぶ](https://www.visualstudio.com/products/visual-studio-team-services-feature-matrix-vs) ことです。

> [!NOTE]
> TFVC はサポートされている唯一のソース管理リポジトリです。 Git はサポートされていません。

### <a name="set-up-azure-devops"></a>Azure DevOps の設定

Azure DevOps をセットアップするには、次の手順に従います。

1. [個人用アクセス トークンの作成](../lifecycle-services/synchronize-bpm-vsts.md#lcs-project-settings-set-up-azure-devops). トークンはすべての LCS バックグラウンド アクションに使用されます。 これらのアクションにはアップグレードと配置が含まれます。 ユーザーが LCS からアクションを起動すると、LCS はこれらのユーザーが Azure DevOps に追加されることを期待しています。 ユーザーは彼らのために Azure DevOps への LCS アクセスを認可する必要があります。
1. [LCS の構成](../lifecycle-services/synchronize-bpm-vsts.md#lcs-project-settings-set-up-azure-devops)。

LCS の Azure DevOps へのアクセスを承認するまで、アクション センターに次のメッセージが表示されます。

![LCS エラーでの VSTS 設定](./media/vsts-setup-in-lcs_may27.jpg)

### <a name="suspend-current-builds"></a>現在のビルドの中断

既にビルド定義を持つ既存の Azure DevOps プロジェクトにビルド環境を展開している場合、ビルドをキューに入れるアクティブなトリガーがないことを確認してください。 また、ビルド プールに対して、スケジュールされたりキューに格納されたビルドがないことを確認してください。

## <a name="deploy-developer-and-buildtest-environments-from-lcs"></a>LCS 開発およびビルド / テスト環境の展開
LCS では、開発およびビルド / テスト環境を展開するオプションが提供されます。 このオプションでは、Azure DevOps プロジェクトに接続されたクラウド内に、開発者を配置して VM をビルドすることができます。

### <a name="azure-devops-credential-setup-and-linking-to-lcs-project"></a>Azure DevOps 資格情報の設定と LCS プロジェクトへのリンク
まだ完了していない場合は、ビルド環境を配置する前に、最初にLCS プロジェクトを設定してから Azure DevOps プロジェクトに接続してください。

1. [https://lcs.dynamics.com/](https://lcs.dynamics.com/)で LCS ポータルにログインして、Azure DevOps および LCS プロジェクトに接続します。
2. 作業しているプロジェクトを選択します。
3. **プロジェクト設定**タイルをクリックします。
4. **Azure DevOps** を選択し、モジュール プロジェクトのソース コードが保管されている Azure DevOps URL を入力します。
5. Azure DevOps リンクを指定して、承認し、**既定のプロジェクトを選択** をクリックします。
   > [!NOTE]
   > 現在のところ、VSTF をソース コントロールとしてサポートしていますが、Git をサポートしていません。 

[![VSTS](./media/vsts-1024x792.jpg)](./media/vsts.jpg)

### <a name="check-in-migrated-or-new-module-code-into-azure-devops"></a>Azure DevOps に移行または新しいモジュールコードをチェックイン

コードの移行プロセスまたは開発活動の一環として、モデル ソース ファイルと関連するテスト モデル ソース ファイルを Azure DevOps にチェックインすることをお勧めします。 LCS 移行サービスを使用してコードを移行した場合、自動的に行われます。 Azure DevOps にコードをチェックインせずに直接チェックインする場合は、Azure DevOps フォルダ構造の特定のガイドラインに従う必要があります。 これは、適切なビルド定義の設定に役立ちます。 すべてのモジュールをルート フォルダー**メタデータ**に追加する必要があります。 各モジュールにはフォルダーが 2 つ必要です。 1 つのフォルダーには、すべてのモデルが含まれています。 他のフォルダーには、そのモジュールの記述子 XML が含まれている必要があります。 

![VSTS フォルダー構造](media/build-trunk-main-metadata.png)

### <a name="deploy-a-build-environment"></a>ビルド環境の展開

「[開発環境の展開およびアクセス](../dev-tools/access-instances.md)」のトピックでは、開発環境の展開方法が説明されています。 同様のフローを使用して、ビルド環境を配置します。 展開またはコンフィギュレーション ウィザードを実行する際に、**トポロジを選択してください**というメッセージが表示されたら、**ビルドおよびテスト**トポロジを選択するのではなく **DevTest** を選択します。

展開ウィザードの一部として、ビルド エージェント名およびビルド エージェント プールを構成できます。

**詳細設定** をクリックし、**Azure DevOps** を選択します
   1.  ビルド エージェント名: Azure DevOps ビルド エージェントのフレンドリ名
   2.  ビルド エージェント プール: ビルド マシンの配置に使用するビルド エージェント プール名を指定します。 Azure DevOps に少なくとも 1 つのエージェント プールが含まれていることを確認します。 既定では、既定のプールがあります。 既定のプールを削除した場合は、ビルド配置は失敗します。
   3.  分岐名: ビルド VM の既定のソース コード同期場所になる Azure DevOps ソース コード ブランチを指定します。 既定の分岐は、「メイン」です。

   ![設定](media/settings.jpg)

## <a name="test-integration-with-the-build"></a>ビルドとのテスト統合
テストと検証のためのビルド プロセスの一部としてテストを統合するには、2 つの方法があります。

-   単位とコンポーネントのレベル テストに基づく SysTest フレームワーク。
-   自動化されたテストの実行の XML を記録するタスク レコーダーから、コードを生成します。

これら 2 つの方法の詳細については、[テストと検証](testing-validation.md) を参照してください。テストおよび検証の戦略についてはこの記事を確認してください。

## <a name="use-the-build-vm-environment"></a>ビルド VM 環境の使用
LCS を通じて開発者トポロジにビルド VM が配置されると、それは事前に構成され、ビルドを開始する準備ができます。 Visual Studio IDE または Azure DevOps インターフェイスから、いつでも既定の構成を変更することができます。 ビルド VM では、簡単なビルドのセットアップのために、モジュール ソース コードがビルド コンピューターに同期されます。 ビルド マシンは、ビルド エージェント、ビルド コントローラー、ビルド プロセス テンプレート、ビルド定義のデフォルト設定で自動構成されています。 ビルドに成功したら、ビルド定義と統合されているテストが実行されます。

### <a name="review-a-pre-configured-customizable-build-environment"></a>定義済みのカスタマイズ可能なビルド環境を確認

ビルド VM には、TFS 2015 の一部としてリリースされた vNext ビルド エージェントが含まれています。 ビルド VM を配置するときは、既定では Azure DevOps プロジェクトと接続して同期するようにビルド エージェントが構成されます。 ビルド VM 構成の一部として、以下に示すようにデフォルトのビルド定義も作成および構成されます。 

[![Build1](./media/build1-1024x488.jpg)](./media/build1.jpg) 

既定のビルド定義には、以下で説明するように、特定の操作を実行する複数のタスクが含まれています。

1.  ビルドに渡す事前定義済の変数パラメータをコンフィギュレーションします。 ビルド実行ごとにクリーンなデータベースを設定するには、**DatabaseBackupToRestore**変数のデータベース バックアップ ファイルの名前を指定します。 パッケージ フォルダーは、すべてのビルド時にクリーン パッケージ フォルダーのコピーで復元されます。

    [![build2](./media/build2-1024x678.jpg)](./media/build2.jpg)

2.  以下のように、「トランク/メイン」ブランチにあるすべてのモジュールを検出して構築するためにソリューションをビルドします。

    [![Build3](./media/build3-1024x456.jpg)](./media/build3.jpg)

3.  「レポートの展開」タスクを使用して、レポートを生成し、ビルド VM に展開します。
4.  「データベース同期」タスクを使用して、データベースをビルド VM 上のローカル SQL に同期させます。
5.  ビルドが成功した後、サンドボックス/ステージング環境を更新するために使用できる配置可能なパッケージを作成します。

    [![Build4](./media/build4-1024x462.jpg)](./media/build4.jpg)

6.  「ビルド コンポーネントのコピーと発行」は、配置可能パッケージを Azure DevOps コンポーネントの場所にアップロードします。

    [![build5](./media/build5-1024x439.jpg)](./media/build5.jpg)

7.  テストの実行については、3 つの既定のタスク「テスト設定」、「テストの実行」、および「テストの終了」があります。

    [![build7](./media/build7-1024x457.jpg)](./media/build7.jpg)

8.  既定のビルドでは毎日午後 5 時に開始される予定です。 チームの必要性に従って、各チェックインでトリガーを「継続」に変更することができます。

    [![build8](./media/build8-1024x491.jpg)](./media/build8.jpg)

既定の構成に変更を加えて、そのビルド VM がビルドをトリガーできるようにすることができます。

## <a name="start-a-build-and-verify-the-build-and-test-execution-results"></a>ビルドを開始し、ビルドとテストの実行結果を確認します。
既定のビルド構成を確認した後、Visual Studio IDE または Azure DevOps Web インターフェイスからビルドを手動でトリガーできます。

1.  ブラウザーを開き、Azure DevOps URL に接続します。
2.  資格情報を使用してをログインします。
3.  ホーム ページの**最近のプロジェクトとソリューション**で、プロジェクトを選択します。
4.  上部リンク オプションから、**ビルド**を選択します。
5.  左側のパネルで、既定のビルド定義インスタンスを選択します。
6.  右クリックし、**キュー ビルド** を選択して Azure DevOps ソース管理に既にチェックインしているモジュールおよびテスト モジュールのビルドをトリガーします。

[![image045](./media/image045.png)](./media/image045.png) 

次の例に示すように、ビルドの成功または失敗が表示されます。 すべてのビルドを表示します。 

[![build9](./media/build9-1024x443.jpg)](./media/build9.jpg) 

特定の完了したビルドとビューの成功/失敗の詳細を選択します。 

[![build10](./media/build10-1024x446.jpg)](./media/build10.jpg) テストリンクをクリックして、テスト実行の失敗を視覚化します。 

[![build11](./media/build11-1024x455.jpg)](./media/build11.jpg)
