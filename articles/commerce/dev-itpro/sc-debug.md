---
title: Visual Studio Code を使用した Store Commerce 拡張機能のデバッグ
description: この記事では、Visual Studio Code を使用して Microsoft Dynamics 365 Commerce Store Commerce 拡張機能をデバッグする方法について説明します。
author: mugunthanm
ms.date: 04/21/2022
ms.topic: article
audience: Developer
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 03-30-2022
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 85b29d24fec1abbe995902d1127616c429f4634e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908670"
---
# <a name="debug-store-commerce-extensions-using-visual-studio-code"></a>Visual Studio Code を使用した Store Commerce 拡張機能のデバッグ

[!include [banner](../includes/banner.md)]

この記事では、Visual Studio Code を使用して Microsoft Dynamics 365 Commerce Store Commerce 拡張機能をデバッグする方法について説明します。

> [!NOTE]
> Visual Studio Code を使用して、64 ビット .NET Framework アプリのみをデバッグできます。 Store Commerce でオフラインの Commerce Runtime (CRT)/ハードウェア ステーション (HWS) コードをデバッグするには、Visual Studio 2019 以降を使用する必要があります。
>
> 1. Store Commerce アプリを開きます。
> 1. Visual Studio で、CRT または HWS コードを開きます。
> 1. メニューで、**デバッグ \> プロセスに添付する** を選択してから、**Microsoft.Dynamics.Commerce.StoreCommerce.exe** を選択します。

Visual Studio Code を使用して Store Commerce 拡張機能をデバッグするには、以下の手順を実行します。

1. [Visual Studio Code](https://code.visualstudio.com/) をインストールします。
1. Visual Studio Code を開き、Visual Studio Marketplace から [VS コードの Microsoft Edge ツール](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) をインストールします。
1. 拡張機能を展開する前に、[Store Commerce アプリ](store-commerce.md#device-installation)をインストールします。 インストール プロセス中に、次の例に示すように **--enablewebviewdevtools** パラメーターを渡すことでデバッグ オプションを有効にします。

    ```PowerShell
    .\StoreCommerce.Installer.exe install --enablewebviewdevtools
    ```

1. [InStore GitHub リポジトリ (repo)](https://github.com/microsoft/Dynamics365Commerce.InStore) から Store Commerce 拡張機能サンプル コードをダウンロードするか、独自の拡張機能コードを使用します。

    > [!NOTE]
    > 管理者モードでは Visual Studio Code を実行しないでください。

1. Visual Studio 開発者コマンド プロンプトを開き、**コード** を入力して Visual Studio Code を開きます。
1. Visual Studio Code で、**ファイル \> フォルダーを開く** を選択してから、拡張機能コード ルート フォルダーを開きます。
1. Visual Studio Code で、ソリューション ディレクトリのルート フォルダーを選択したまま (または右クリック) にして、**.vscode** という名前の新しいフォルダーを作成します。
1. **.vscode** フォルダー内で、**launch.json** という新しいファイルを作成します。
1. **launch.commerc** ファイルで、次のコンフィギュレーションを追加して Store Commerce 拡張機能を構築およびデバッグします:

    - **Store Commerce のデバッグ** – このコンフィギュレーションにより、Store Commerce アプリが開き、デバッグ用に拡張コードが関連付けられます。
    - **Store Commerce の構築とデバッグ** - このコンフィギュレーションにより拡張コードが構築され、拡張機能が展開され、Store Commerce アプリが開き、デバッグ用に拡張コードが関連付けられます。
    - **Store Commerce へのデバッガーの関連付け** - このコンフィギュレーションにより、デバッグ用に Store Commerce アプリへの拡張コードが関連付けられますが、Store Commerce アプリは開きません。

1. 次のコンフィギュレーション コードをコピーし、**aunch.json** ファイルに貼り付けてから、ファイルを保存します。

    ```json
    {
        "version": "0.2.0",
        "configurations": [
            {
                "type": "pwa-msedge",
                "request": "launch",
                "port": 9222,
                "name": "Debug Store Commerce",
                "useWebView": true,
                "runtimeExecutable": "${env:ProgramFiles}/Microsoft Dynamics 365/10.0/Store Commerce/Microsoft/contentFiles/Microsoft.Dynamics.Commerce.StoreCommerce.exe",
                "userDataDir": "${env:LocalAppData}/Microsoft Dynamics 365/10.0/Data/Store Commerce/Pos",
                "url": "file:///${env:ProgramFiles}/Microsoft Dynamics 365/10.0/Store Commerce/Microsoft/contentFiles/Pos/Pos.html"
            },
            {
                "type": "pwa-msedge",
                "request": "launch",
                "port": 9222,
                "name": "Build and Debug Store Commerce",
                "useWebView": true,
                "runtimeExecutable": "${env:ProgramFiles}/Microsoft Dynamics 365/10.0/Store Commerce/Microsoft/contentFiles/Microsoft.Dynamics.Commerce.StoreCommerce.exe",
                "userDataDir": "${env:LocalAppData}/Microsoft Dynamics 365/10.0/Data/Store Commerce/Pos",
                "url": "file:///${env:ProgramFiles}/Microsoft Dynamics 365/10.0/Store Commerce/Microsoft/contentFiles/Pos/Pos.html",
                "preLaunchTask": "${defaultBuildTask}"
            },
            {
                "name": "Attach debugger to Store Commerce",
                "type": "pwa-msedge",
                "port": 9222,
                "request": "attach",
                "useWebView": true,
                "runtimeExecutable": "${env:ProgramFiles}/Microsoft Dynamics 365/10.0/Store Commerce/Microsoft/contentFiles/Microsoft.Dynamics.Commerce.StoreCommerce.exe"
            }
        ]
    }
    ```

1. **.vscode** フォルダー内で、**tasks.json** という新しいファイルを作成します。 このファイルを使用して、Store Commerce アプリを構築しインストールするためのコンフィギュレーションを作成します。
1. 次のコンフィギュレーション コードをコピーして、**tasks.json** ファイルに貼り付けます。

    ```json
    {
        "version": "2.0.0",
        "tasks": [
            {
                "label": "Build & Install Store Commerce Extension",
                "type": "shell",
                "command": "msbuild",
                "args": [
                    "/p:Configuration=debug",
                    "/p:InstallStoreCommerceExtensionsAfterBuild=true",
                    "/t:build",
                    "/m",
                    "/consoleloggerparameters:NoSummary",
                    "${workspaceFolder}"
                ],
                "group": {
                    "kind": "build",
                    "isDefault": true
                },
            }
        ]
    }
    ```

1. Visual Studio Code で、**デバッグ** を選択し、シナリオの適切なオプションを選択してから、拡張子コードにブレークポイントを設定してデバッグを開始します。

## <a name="troubleshoot-debug-issues"></a>デバッグ問題のトラブルシューティング

### <a name="msbuild-error"></a>msbuild エラー

以下のようなエラーメッセージが表示される場合があります: "msbuild : 'msbuild" という用語は、コマンドレット、関数、スクリプト ファイル、または操作可能なプログラムの名前として認識されません。" この場合、Visual Studio Code を閉じます。 次に、Visual Studio 開発者コマンド プロンプトを開き、ソリューション ディレクトリに移動し、**コード** を入力して Visual Studio Code を再度開き、正しい msbuild バージョンを設定します。

### <a name="json-file-comment-extension"></a>JSON ファイル コメント拡張子

.json ファイル コメントに関連するエラー メッセージが表示された場合は、.json ファイルを閉じてから、再度 **デバッグ** コマンドを実行します。 または、.json ファイルのコメントをすべて削除してください。
