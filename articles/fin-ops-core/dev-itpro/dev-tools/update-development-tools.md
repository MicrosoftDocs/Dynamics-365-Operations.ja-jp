---
title: Visual Studio 開発ツールの更新
description: このトピックでは、開発ツールを更新する方法について説明します。
author: RobinARH
ms.date: 07/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 33571
ms.assetid: bd24d864-6915-4d17-9ebb-d1619b7d4311
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41186165b2d4e19ad41d3130a4fb94e98b106c00
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753006"
---
# <a name="update-the-visual-studio-development-tools"></a>Visual Studio 開発ツールの更新

[!include [banner](../includes/banner.md)]

このトピックでは、開発ツールを更新する方法について説明します。

このチュートリアルを使用して、Visual Studio 開発ツールを新しいバージョンに更新します。 既存の Visual Studio 開発ツールをアンインストールして、新しい拡張機能をインストールする方法を説明します。 新しい拡張機能は、インストール可能な VSIX ファイルの形式です。 このファイルは、Dynamics Lifecycle Services (LCS) のサイトで使用可能なバイナリ修正プログラムの一部です。 VSIX ファイルは、バイナリ修正プログラム パッケージの **DevToolsService\\Scripts** フォルダーにあります。 

> [!NOTE]
> Finance and Operations プラットフォームをプラットフォーム更新プログラム 4 以降にアップグレードする場合は、この記事の手順に従う必要はありません。 プラットフォームのアップグレード プロセスの一部である自動のステップです。

## <a name="uninstall-the-existing-visual-studio-extension"></a>既存の Visual Studio 拡張機能をアンインストールする
開発ツールの新しいバージョンをインストールするには、最初に既存のバージョンをアンインストールする必要があります。 インストールされている開発ツールのバージョンを確認します。 インストールしていない場合は、このセクションを省略できます。

### <a name="verify-your-current-version-of-the-visual-studio-extension"></a>Visual Studio 拡張機能の現在のバージョンを確認します。

1.  Visual Studio で **ヘルプ &gt; Microsoft Visual Studio について** ダイアログを開いて、**Finance and Operations 開発者ツール** を表示します。
2.  選択して **OK** をクリックします。

### <a name="uninstall-the-extension"></a>拡張機能をアンインストールする

1.  Visual Studio の **ツール&gt;拡張子と更新** ダイアログを開きます。
2.  **Finance and Operations Visual Studio ツール** を選択し、**削除** をクリックします。
3.  拡張機能がアンインストールされると、Visual Studio を終了します。

## <a name="install-a-new-version-of-the-extension"></a>拡張機能の新しいバージョンのインストール
1.  Visual Studio が実行されていないことを確認します。
2.  新しいバージョンの VSIX ファイルをダブルクリック (または右クリックと **未処理**) します。
3.  インストールの指示に従ってください。
4.  インストールが完了したら、Visual Studio を起動して、アプリケーションの開発を開始できます。






[!INCLUDE[footer-include](../../../includes/footer-banner.md)]