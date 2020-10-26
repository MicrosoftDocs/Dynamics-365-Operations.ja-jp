---
title: Lifecycle Services (LCS) で、コード アップグレード サービスを構成する
description: このトピックでは、Lifecycle Services (LCS) の<strong>コード アップグレード</strong> タイルを構成して、ソリューションを最新バージョンの Finance and Operations アプリに移行する方法について説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 265594
ms.assetid: 964b5a15-9b9c-434c-a4c2-e14406ebfaeb
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: baf81832aa1476fb476a8c9d8d8d4ae413fbebb9
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986914"
---
# <a name="configure-the-code-upgrade-service-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) で、コード アップグレード サービスを構成する

[!include [banner](../includes/banner.md)]

このトピックでは、Lifecycle Services (LCS) の<strong>コード アップグレード</strong> タイルを構成して、ソリューションを最新バージョンの Dynamics 365 Finance and Operations アプリに移行する方法について説明します。

<a name="overview"></a>概要
--------


コードのアップグレード ツールは、Azure DevOps プロジェクトに接続し、Trunk\\Main ブランチを検索し、Releases\\\<version number\> という名前の新しいブランチに分岐してから、コードのアップグレードを実行します。 このプロセスが完了した後、開発環境を、Releases\\\<version number\> の下の新しいブランチに同期させ、競合を解決できます。 アップグレード後のコードをコンパイルしてテストしたとき、新しいブランチを Visual Studio のソース管理エクスプ ローラーを使用して Trunk\\Main にマージすると、プロセスが完了します。


Dynamics 365 for Finance and Operations バージョン 8.0 およびそれ以降では、Microsoft モデルをオーバーレイしてカスタマイズすることはできません。 アップグレードする前に、カスタマイズを拡張機能にリファクターする計画が必要です。 詳細については [拡張機能のホーム ページ](../extensibility/extensibility-home-page.md) および [モデルの制限を緩和して、オーバレイを拡張機能にリファクタリングする](../extensibility/refactoring-over-layering.md) を参照してください。

## <a name="process"></a>処理
### <a name="create-the-trunkmain-folder-structure"></a>トランク\\メイン フォルダー構造を作成する

ソース コードを識別するコード アップグレード サービスについては、Azure DevOps プロジェクトには Team Foundation バージョン管理 (TFVC) コード リポジトリが含まれている必要があります。 さらに、コード リポジトリ フォルダー構造は、次の厳密なパターンに準拠している必要があります。 

 - コードおよびメタデータ: /<DevOps project name>/Trunk/Main/Metadata
 - Visual Studio プロジェクトおよびソリューション ファイル: /<DevOps project name>/Trunk/Main/Projects
 
 新しいフォルダーは、Azure DevOps Web インターフェイスの **リポジトリ** で直接作成できます。
 
 
> [!NOTE]
> - フォルダー名は大文字と小文字を区別していて、つまり、メインおよびメインでない、またはコードのアップグレード サービスはフォルダーを認識しません。
> - Azure DevOps プロジェクトは、既定で Git バージョン管理を使用します。 TFVC リポジトリを追加する必要があります。
>     1. プロジェクト設定へ移動し、リポジトリに移動します。
>     2. [新しいリポジトリ] を選択します。
>     3. [種類] フィールドで [TFVC] を選択し、[作成] をクリックします。


### <a name="create-a-personal-access-token"></a>個人用アクセス トークンを作成する

Azure DevOps プロジェクトに接続するために、LCS は個人用アクセス トークンを使用して認証されます。 Azure DevOps で個人用アクセス トークンを作成するには、以下の手順に従います。 LCS プロジェクトを Azure DevOps プロジェクトへ接続できるように構成する場合、このセクションを省略できます。

1. visualstudio.com にログインし、Azure DevOps プロジェクトを見つけます。
2. 右上隅で、名前をポイントするとメニューが表示され、**セキュリティ**を選択します。
3. **追加**をクリックして、新しい個人用アクセス トークンを作成し、名前を付けて、トークンが使用できる期間を入力します。 **トークンの作成**をクリックします。 

   [![コード アップグレードのトークンの作成](./media/codeupgrademaketoken.png)](./media/codeupgrademaketoken.png)

4. トークンをクリップボードにコピーします。 このステップが完了したら、トークンの詳細情報を見つけることはできません。したがって、このページから移動する前に、かならずトークンをコピーしてください。

### <a name="configure-your-lifecycle-services-project-to-connect-to-azure-devops"></a>Lifecycle Services プロジェクトをコンフィギュレーションして Azure DevOps に接続する

1. LCS プロジェクトで、**プロジェクト設定**タイルに移動し、**Visual Studio Team Services** を選択してから、**Visual Studio Team Services の設定**ボタンを選択します。 この構成は多くの LCS ツールで必要になります。すでに Azure DevOps プロジェクトに接続するように LCS を設定している場合は、このセクションをスキップできます。 


   [![LCS VSTS の設定](./media/lcs_vsts_setup.png)](./media/lcs_vsts_setup.png)

2. Azure DevOps アカウントのルート URL および以前に作成したアクセス トークンを入力し、**続行**をクリックします。

   [![LCS トークン](./media/lcstoken.png)](./media/lcstoken.png)

3. 接続する Azure DevOps アカウント内のプロジェクトを選択し、**続行** を選択します。 
   
   [![LCS がプロジェクトを選択](./media/lcs_selectproject.png)](./media/lcs_selectproject.png)

4. **確認および保存**ページで、**保存**をクリックします。

### <a name="create-an-ax7version-file"></a>ax7.version ファイルを作成します

> [!NOTE]
> AX 2012 から移行する場合は、この手順を省略できます。

LCS のコードのアップグレード タイルは、移行元のバージョンを自動的に検出します。ソース管理のメイン フォルダの ax7.version ファイルを参照してください。 以下に示すように、Visual Studio または Azure DevOps Web ポータルを通じて、このファイルを手動で作成する必要があります。 Dynamics AX 2012 R3 またはそれ以前のバージョンからコードを移行する場合、このファイルは必要ありません。 ここに入力するバージョン番号は、アプリケーションのバージョン (プラットフォームのバージョンではない) である必要があります。 このファイルに無効なバージョン番号を入力するとしてのコード アップグレードの実行に失敗する可能性があるため、ここには必ず正しいバージョン番号を入力してください。

[![ax7 バージョン ファイル](./media/ax7_versionfile.png)](./media/ax7_versionfile.png) 

どのアプリケーション バージョンを持っているか識別する方法の詳細については、[Microsoft Dynamics AX ビルド番号の概要](https://blogs.msdn.microsoft.com/axsupport/2012/03/29/overview-of-microsoft-dynamics-ax-build-numbers/)を参照してください。

### <a name="execute-the-code-upgrade-tile"></a>コード アップグレード タイルを実行

1. LCS プロジェクトで、**コードのアップグレード** タイルを選択します。 

   [![コード アップグレード タイル](./media/codeupgradetile.png)](./media/codeupgradetile.png)

2. 画面の左下隅で、**追加**をクリックしてから名前と説明を入力します。 アップグレード元のバージョンとして Microsoft Dynamics AX 7 を選択し、**作成**をクリックします。
   -   Dynamics AX 2012 R3 からコードをアップグレードする場合は、アップグレード元のバージョンを選択します。 圧縮バージョンの Dynamics AX 2012 R3 モデル ストア ファイルをアップロードするように要求されます。
   -   **見積のみ**チェック ボックスがオンになっている場合、ツールはレポートのみを生成し、チェックインや Azure DevOps の新しいコード分岐の作成を行いません。 実際のアップグレードをコミットする前に、アップグレードに必要な作業の潜在的なサイズを評価する場合、このオプションを使用する必要があります。

   [![新規コード ブランチ](./media/codeupgrade_new.png)](./media/codeupgrade_new.png)

3. 右下にある**コードの分析**をクリックします。 コードのアップグレード プロセスが開始されます。 これは、大規模なソリューションが完了するまでに通常 40 分かかります。 完了したら、LCS の **コードのアップグレード** タイルに戻り、結果を表示します。
4. コードのアップグレード サービスは、新しいブランチを作成し、アップグレードされたコードを Azure DevOps プロジェクトにチェックインします。 アップグレード プロセスが完了した後、コードは**リリース**フォルダ下の新しいブランチに存在します。 分岐名の後には、アップグレードの日時が付いています。 

   [![コード アップグレード ブランチ](./media/codeupgradebranch-300x192.png)](./media/codeupgradebranch.png)


### <a name="merge-releases-back-into-trunkmain"></a>リリースを Trunk\\Main にマージ

Releases\\\<version number\> のアップグレードされたコードが正常にコンパイルされ、コード移行とテストを完了したら、このブランチを Trunk\\Main にマージする準備が整います。 これを行うには、Visual Studio の開発環境で、ソース管理エクスプローラー ウィンドウを開き、**Releases**\\\<version number\> のブランチを右クリックし、コンテキスト メニューで**分岐とマージ**に進み、サブ メニューで**マージ**を選択します。

[![リリース ブランチのマージ](./media/MergeReleasesBranch.PNG)](./media/MergeReleasesBranch.PNG)

[ソース管理マージ ウィザード](https://www.visualstudio.com/docs/tfvc/merge-folders-files#sourcecontrolwizard) が開かれ、Releases\\\<version number\> ブランチを Trunk\\Main にマージする手順が示されます。 
