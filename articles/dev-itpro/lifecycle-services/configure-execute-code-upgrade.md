---
title: "Lifecycle Services (LCS) で、コード アップグレード サービスを構成する"
description: "このトピックでは、Lifecycle Services (LCS) の <strong>コード アップグレード</strong> タイルを構成して、ソリューションを最新バージョンの Finance and Operations に移行する方法について説明します。"
author: tariqbell
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 265594
ms.assetid: 964b5a15-9b9c-434c-a4c2-e14406ebfaeb
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: fcef08f348ec6bf0ff903c6f3a255763ba7b5808
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="configure-the-code-upgrade-service-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) で、コード アップグレード サービスを構成する

[!include [banner](../includes/banner.md)]

このトピックでは、Lifecycle Services (LCS) の <strong>コード アップグレード</strong> タイルを構成して、ソリューションを最新バージョンの Dynamics 365 for Finance and Operations に移行する方法について説明します。

<a name="overview"></a>概要
--------

コードのアップグレード ツールは、Visual Studio Team Services (VSTS) に接続し、トランク\\メインブランチを検索し、リリース\\\<バージョン番号\>という名前の新しいブランチに分岐してから、コードのアップグレードを実行します。 このプロセスが完了した後、Finance and Operations 開発環境を、リリース \\\<バージョン番号\> 下の新しいブランチに同期させ、競合を解決できます。 アップグレード後のコードをコンパイルしてテストしたとき、新しいブランチを Visual Studio のソース管理エクスプ ローラーを使用して Trunk\\Main にマージすると、プロセスが完了します。

Dynamics 365 for Finance and Operations 8.0 およびこれ以降のバージョンでは、Microsoft モデルのオーバーレイ経由でのカスタマイズは許可されていません。 アップグレードする前に、カスタマイズを拡張機能にリファクターする計画が必要です。 詳細については、[拡張機能のホームページ](../extensibility/extensibility-home-page.md)および [8.0 環境でオーバーレイをリファクタリングする](../extensibility/refactoring-over-layering.md)を参照してください。

## <a name="process"></a>プロセス
### <a name="create-the-trunkmain-folder-structure"></a>トランク\\メイン フォルダー構造を作成する

ソース コードを識別するコード アップグレード サービスについては、フォルダ構造は以下の厳密なパターンに準拠している必要があります。 正しい構造は次のとおりです。 

 - コード自体用: ..\\\<VSTS プロジェクト名 >\\トランク\\メイン\\メタデータ
 - Visual Studio プロジェクト用: ..\\\<VSTS プロジェクト名 >\\トランク\\メイン\\プロジェクト
 
 VSTS で新しいフォルダーを作成するには、ローカルでフォルダーを作成し、VSTS にチェックインします。
 
 > [!NOTE]
 > フォルダー名は大文字と小文字を区別していて、つまり、メインおよびメインでない、またはコードのアップグレード サービスはフォルダーを認識しません。 


### <a name="to-create-a-personal-access-token"></a>個人用アクセス トークンを作成するには

VSTS プロジェクトに接続するために、LCS は個人用アクセス トークンを使用して認証されます。 VSTS で個人用アクセス トークンを作成するには、次の手順に従います。 LCS プロジェクトを VSTS プロジェクトへ接続できるように構成する場合、このセクションを省略できます。

1. visualstudio.com にログインし、VSTS プロジェクトを見つけます。
2. 右上隅で、名前をポイントするとメニューが表示され、**セキュリティ**を選択します。
3. **追加**をクリックして、新しい個人用アクセス トークンを作成し、名前を付けて、トークンが使用できる期間を入力します。 **トークンの作成**をクリックします。 

   [![コード アップグレードのトークンの作成](./media/codeupgrademaketoken.png)](./media/codeupgrademaketoken.png)

4. トークンをクリップボードにコピーします。 このステップが完了したら、トークンの詳細情報を見つけることはできません。したがって、このページから移動する前に、かならずトークンをコピーしてください。

### <a name="configure-your-lifecycle-services-project-to-connect-to-vsts"></a>Lifecycle Services プロジェクトをコンフィギュレーションして VSTS に接続する

1. LCS プロジェクトで、**プロジェクト設定**タイルに移動し、**Visual Studio Team Services** を選択してから、**Visual Studio Team Services の設定**ボタンを選択します。 この構成は多くの LCS ツールで必要になります。すでに VSTS プロジェクトに接続するように LCS を設定している場合は、このセクションをスキップできます。 

   [![LCS VSTS の設定](./media/lcs_vsts_setup.png)](./media/lcs_vsts_setup.png)

2. VSTS アカウントのルート URL および以前に作成したアクセス トークンを入力し、**続行**をクリックします。

   [![LCS トークン](./media/lcstoken.png)](./media/lcstoken.png)

3. 接続する VSTS アカウント内のプロジェクトを選択し、**続行** を選択します。 
   [![LCS がプロジェクトを選択](./media/lcs_selectproject.png)](./media/lcs_selectproject.png)

4. **確認および保存**ページで、**保存**をクリックします。

### <a name="create-an-ax7version-file"></a>ax7.version ファイルを作成します

LCS のコードのアップグレード タイルは、移行元の Finance and Operations のバージョンを自動的に検出します。ソース管理のメイン フォルダの ax7.version ファイルを参照してください。 以下に示すように、Visual Studio または VSTS ポータルを通じて、このファイルを手動で作成する必要があります。 Dynamics AX 2012 R3 またはそれ以前のバージョンからコードを移行した場合、このファイルは必要ありません。 ここに入力するバージョン番号は、アプリケーションのバージョン (プラットフォームのバージョンではない) である必要があります。 このファイルに無効なバージョン番号を入力するとしてのコード アップグレードの実行に失敗する可能性があるため、ここには必ず正しいバージョン番号を入力してください。

[![ax7 バージョン ファイル](./media/ax7_versionfile.png)](./media/ax7_versionfile.png) 

どのアプリケーション バージョンを持っているか識別する方法の詳細については、[Microsoft Dynamics AX ビルド番号の概要](https://blogs.msdn.microsoft.com/axsupport/2012/03/29/overview-of-microsoft-dynamics-ax-build-numbers/) を参照してください。

### <a name="execute-the-code-upgrade-tile"></a>コード アップグレード タイルを実行

1. LCS プロジェクトで、**コードのアップグレード** タイルを選択します。 

   [![コード アップグレード タイル](./media/codeupgradetile.png)](./media/codeupgradetile.png)

2. 画面の左下隅で、**追加**をクリックしてから名前と説明を入力します。 アップグレード元のバージョンとして Microsoft Dynamics AX 7 を選択し、**作成** をクリックします。
   -   Dynamics AX 2012 R3 からコードをアップグレードする場合、アップグレード元のバージョンを選択します。 圧縮バージョンの Dynamics AX 2012 R3 モデル ストア ファイルをアップロードするように要求されます。
   -   **見積のみ**チェック ボックスがオンになっている場合、ツールはレポートのみを生成し、チェックインや VSTS の新しいコード分岐の作成を行いません。 実際のアップグレードをコミットする前に、アップグレードに必要な作業の潜在的なサイズを評価する場合、このオプションを使用する必要があります。

   [![新規コード ブランチ](./media/codeupgrade_new.png)](./media/codeupgrade_new.png)

3. 右下にある**コードの分析**をクリックします。 コードのアップグレード プロセスが開始されます。 これは、大規模なソリューションが完了するまでに通常 40 分かかります。 完了したら、LCS の **コードのアップグレード** タイルに戻り、結果を表示します。
4. コードのアップグレード サービスは、新しいブランチを作成し、アップグレードされたコードを VSTS プロジェクトにチェックインします。 アップグレード プロセスが完了した後、コードは**リリース**フォルダ下の新しいブランチに存在します。 分岐名の後には、アップグレードの日時が付いています。 

   [![コード アップグレード ブランチ](./media/codeupgradebranch-300x192.png)](./media/codeupgradebranch.png)


### <a name="merge-releases-back-into-trunkmain"></a>リリースを Trunk\\Main にマージ

リリース\\\<バージョン番号\>のアップグレードされたコードが正常にコンパイルされ、テストに合格したら、このブランチをトランク\\メインにマージする準備が整いました。 これを行うには、Visual Studio の開発環境で、[ソース管理エクスプローラー] ウィンドウを開き、**リリース\\\<バージョン番号\>** 分岐を右クリックし、コンテキスト メニューで **分岐とマージ** に進み、サブ メニューで **マージ** を選択します。

[![リリース ブランチのマージ](./media/MergeReleasesBranch.PNG)](./media/MergeReleasesBranch.PNG)

これにより、[[ソース管理マージ ウィザード](https://www.visualstudio.com/en-us/docs/tfvc/merge-folders-files#sourcecontrolwizard)] が開きます。これは、リリース\\\<のバージョン番号\>のブランチをトランク\\メインにマージする手順を案内します。 

