---
title: POS 拡張機能のデバッグ
description: このトピックでは、POS 拡張機能のデバッグ方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 0f114824b36cd1400432ee2958403af9bfafe3fc
ms.sourcegitcommit: fd15b02fc9caa1c05e56abdc276a7f4b23b0d8f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/29/2021
ms.locfileid: "5960154"
---
# <a name="debugging-pos-extensions"></a>POS 拡張機能のデバッグ

[!include [banner](../../includes/banner.md)]

このトピックでは、POS 拡張機能のデバッグ方法について説明します。 これは、Retail SDK バージョン 10.0.18 以降に適用されます。

## <a name="debugging-modern-pos-using-visual-studio-2017"></a>Visual Studio 2017 を使用した Modern POS のデバッグ

次の手順に従って拡張機能をデバッグします。

1. シールドされた MPOS インストーラーを使用して、開発マシンでシールドされた Modern POS をインストールします。
2. デスクトップ上のショートカットをクリックして UWP アプリをインストールします。
3. Visual Studio で、Modern POS 拡張機能パッケージ プロジェクト (**jsproj**) を構築します。
4. Visual Studio で、Modern POS 拡張機能パッケージを展開します。 ソリューション エクスプローラーで ModernPOS JavaScript プロジェクト ファイルを右クリックしてから、**展開** を選択します。
5. 次の手順に従って、デバッガーが関連付けられた POS を起動します。

    1. **デバッグ** メニューで、**その他のデバッグ ターゲット &gt; インストールされたアプリをデバッグする**。
    2. **Commerce Modern POS** を検索して選択します。
    3. **開始** をクリックしてアプリケーションを起動します。

## <a name="running-and-debugging-cloud-pos"></a>Cloud POS の実行およびデバッグ

### <a name="configuring-the-cloud-pos-extension-development-environment"></a><a name="configure-cloud-pos"></a> Cloud POS 拡張機能の開発環境の構成

拡張機能パッケージがマシン上で初めて開発されたとき、またはリンクが削除された場合は、次の手順を実行します。 Cloud POS 拡張機能ディレクトリに、拡張機能パッケージ ルート ディレクトリへのディレクトリ シンボル リンクを作成します。

1. Cloud POS がマシンに配置されている必要があります。 インストールされていない場合は、CSU 自己ホスト型インストーラーを使用して Cloud POS を配置します。
2. IIS を開きます。 **実行** メニュー (**Windows キー + R**) を開き、**inetmgr** と入力します。 **OK** を選択します。
3. **サイト &gt; RetailCloudPos を選択** を展開し、右クリックして **エクスプローラ** を選択します。
4. **ファイル** を選択し、**管理者として Windows PowerShell を開く** を選択します。
5. コマンド `cmd .` を実行して、PowerShell ウィンドウでウィンドウ コマンド プロンプトを開きます。
6. コマンド `cd Extensions` を実行して、現在のディレクトリを拡張機能のルート ディレクトリに変更します。
7. コマンド `set ExtensionPackageName=Contoso.Pos.Developer.Samples` を実行して、拡張機能パッケージの名前でセッション変数を作成

    > [!NOTE]
    > 上記のコマンドの **Contoso.Pos.Developer.Samples** を POS 拡張機能パッケージの名前に置き換えます。 拡張機能パッケージ名は、POS 拡張機能パッケージを構成する Commerce Runtime トリガー拡張機能の **ExtensionPackageDefinition** で指定された名前と一致する必要があります。

8. コマンド `set AbsolutePathToExtensionPackageProject=%FullPathToPOSExtensionProjectRootDirectory%` を実行して、POS 拡張機能パッケージ プロジェクト ディレクトリへの絶対パスを使用してセッション変数を作成

    > [!NOTE]
    > **%FullPathToPOSExtensionProjectRootDirectory%** を POS 拡張機能パッケージ プロジェクトへの絶対パスに置き換えます。

    例: 

    ```powershell
    set AbsolutePathToExtensionPackageProject=K:\RetailCloudPos\WebRoot\Extensions\ Contoso.Pos.Developer.Samples
    ```

9. 次のコマンドを実行して、拡張機能ディレクトリから拡張機能パッケージ プロジェクトのルート ディレクトリへのリンクを作成します。

    ```powershell
     mklink /D %ExtensionPackageName% %AbsolutePathToExtensionPackageProject%
    ```

10. 拡張機能パッケージのリンク フォルダーが Cloud POS 拡張機能パッケージ ディレクトリに作成されているかどうかを確認します。次の画像のようになります。

## <a name="debugging-cloud-pos-using-edge-developer-tools"></a>Edge 開発者ツールを使用した Cloud POS のデバッグ

1. [Cloud POS 拡張機能の開発環境の構成](#configure-cloud-pos) の手順を完了しました。
2. Cloud POS 拡張機能プロジェクトを構築します。
3. Edge の Cloud POS Web サイトに移動します。
4. F12 キーを押し、Edge 開発者ツールを起動します。
5. Cloud POS 拡張機能パッケージのルート ディレクトリを指すワークスペースを設定します。 ワークスペースを設定するのは最初だけです。
6. **JavaScript ソース マッピング** が有効であることを確認します。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
