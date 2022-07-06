---
title: MPOS (シールド) と CPOS 拡張機能のデバッグ
description: この記事では、モダン販売時点管理 (シールド) と Cloud POS 拡張機能のデバッグ方法について説明します。
author: mugunthanm
ms.date: 05/05/2022
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: d0d3005df25dcb8043545e9a7ba1a400440bae2e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870568"
---
# <a name="debug-mpos-sealed-and-cpos-extensions"></a>MPOS (シールド) と CPOS 拡張機能のデバッグ

[!include [banner](../../includes/banner.md)]

この記事では、**シールド** の Modern 販売時点管理 (MPOS) と Cloud POS 拡張機能のデバッグ方法について説明します。 Retail ソフトウェア開発キット (SDK) バージョン 10.0.18 以降に適用されます。 

 > [!NOTE]
 > Store Commerce アプリのデバッグについては、[Visual Studio Code を使用し Store Commerce 拡張機能のデバッグ](../sc-debug.md) を参照してください

## <a name="debug-sealed-modern-pos-by-using-visual-studio-2017"></a>Visual Studio 2017 を使用したシールド Modern POS のデバッグ

次の手順に従って拡張機能をデバッグします。

1. シールドされた MPOS インストーラーを使用して、開発マシンでシールドされた Modern POS をインストールします。 **Modern POS (SEALED)** インストーラは、https://lcs.dynamics.com/V2/SharedAssetLibrary > Retail セルフ サービス パッケージ セクションからダウンロードが可能です。
2. **Modern POS (SEALED)** インストーラのインストール後に、デスクトップ ショートカット アイコンは POS Universal Windows Platform (UWP) アプリをインストールまたは更新するために作成されます。 デスクトップ上で **Retail Modern POS のインストールまたは更新** アイコンをダブル クリックし、UWP アプリをインストールします。 この前に必要なバックエンド コンポーネントを配置し、UWP アプリをインストールします。
3. Microsoft Visual Studio で、MPOS 拡張機能パッケージ プロジェクト (JavaScript プロジェクト ファイル \[.jsproj file\]) を構築します。
4. MPOS 拡張機能パッケージを配置します。 ソリューション エクスプローラーで、MPOS .jsproj ファイルを選択したまま (または右クリック) にして、**配置** を選択します。
5. デバッガーが関連付けられるように POS を開きます。

    1. **デバッグ** メニューで、**その他のデバッグ ターゲット &gt; インストールされたアプリ パッケージをデバッグする**。
    2. **Commerce Modern POS** を検索して選択します。
    3. **開始** を選択すると、アプリケーションが開きます。

## <a name="run-and-debug-cloud-pos"></a>Cloud POS の実行およびデバッグ

### <a name="configure-the-cloud-pos-extension-development-environment"></a><a name="configure-cloud-pos"></a>Cloud POS 拡張機能の開発環境のコンフィギュレーション

拡張機能パッケージがマシン上で初めて開発されたとき、またはリンクが削除された場合は、次の手順を実行します。 Cloud POS (CPOS) **拡張機能** ディレクトリに、拡張機能パッケージ ルート ディレクトリへのディレクトリ シンボル リンクを作成します。

1. CPOS がマシンに配置されていることを確認します。 配置されていない場合は、Commerce Scale Unit (自己ホスト) インストーラーを使用して配置します。
2. インターネット インフォメーション サービス (IIS) を開きます。 **Windows ロゴ キーと R キー** を同時に押して、**実行** ダイアログ ボックスに **inetmgr** と入力し、**OK** を選択します。
3. **サイト** を展開し、**RetailCloudPos** を選択したまま (または右クリック) にして、**エクスプローラー** を選択します。
4. **ファイル** を選択し、**管理者として Windows PowerShell を開く** を選択します。
5. **Windows PowerShell** ウィンドウで次のコマンドを実行し、Windows コマンド プロンプトを開きます。

    ```powershell
    cmd .
    ```

6. 次のコマンド を実行して、現在のディレクトリを **拡張機能** のルート ディレクトリに変更します。

   ```powershell
   cd Extensions
   ```

7. 次のコマンドを実行して、拡張機能パッケージの名前を持つセッション変数を作成します。

    ```powershell
    set ExtensionPackageName=Contoso.Pos.Developer.Samples
    ```

    > [!NOTE]
    > **Contoso.Pos.Developer.Samples** を POS 拡張機能パッケージの名前に置き換えます。 拡張機能パッケージ名は、POS 拡張機能パッケージを構成する Commerce Runtime  CRT トリガー拡張機能の **ExtensionPackageDefinition** で指定された名前と一致する必要があります。

8. 次のコマンドを実行して、POS 拡張機能パッケージ プロジェクト ディレクトリへの絶対パスを持つセッション変数を作成します。

    ```powershell
    set AbsolutePathToExtensionPackageProject=%FullPathToPOSExtensionProjectRootDirectory%
    ```

    > [!NOTE]
    > **%FullPathToPOSExtensionProjectRootDirectory%** を POS 拡張機能パッケージ プロジェクトへの絶対パスに置き換えます。 次に例を示します。
    >
    > ```powershell
    > set AbsolutePathToExtensionPackageProject=K:\RetailCloudPos\WebRoot\Extensions\ Contoso.Pos.Developer.Samples
    > ```

9. 次のコマンドを実行して、**拡張機能** ディレクトリから拡張機能パッケージ プロジェクトのルート ディレクトリへのリンクを作成します。

    ```powershell
    mklink /D %ExtensionPackageName% %AbsolutePathToExtensionPackageProject%
    ```

10. 拡張機能パッケージのリンク フォルダーが CPOS 拡張機能パッケージ ディレクトリに作成されているかどうかを確認します。

## <a name="debug-cpos-by-using-the-microsoft-edge-developer-tools"></a>Microsoft Edge 開発者ツールを使用した CPOS のデバッグ

1. この記事で前述されている [Cloud POS 拡張機能の開発環境のコンフィギュレーション](#configure-cloud-pos) セクションの手順に従います。
2. CPOS 拡張機能プロジェクトを構築します。
3. Microsoft Edge で、CPOS Web サイトを開きます。
4. **F12** キーを選択して、Microsoft Edge 開発者ツールを開きます。
5. CPOS 拡張機能パッケージのルート ディレクトリを指すワークスペースを設定します。 この手順を初めて実行する場合は、ワークスペースを設定する必要があります。
6. **JavaScript ソース マッピング** が有効であることを確認します。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
