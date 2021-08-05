---
title: 管理者以外のユーザーが Regression suite automation tool (RSAT) を使用するように構成する
description: このトピックでは、RSAT バージョン 2.2 およびそれ以降のユーザーに特権リソースを付与する方法について説明します。
author: FrankDahl
ms.date: 03/09/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2021-03-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ec977c0db9529a504a85d96efb0c099b25413dd
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346472"
---
# <a name="configure-non-administrator-users-to-use-rsat"></a>管理者以外のユーザーが RSAT を使用するように構成する

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Regression suite automation tool (RSAT) は、実行しているコンピューターの特権リソースを使用します。 RSAT のテストを実行するには、ユーザーはコンピューターの管理者である必要があります。 このトピックでは、RSAT バージョン 2.2 および **それ以降** を使用している場合、これらの特権リソースを付与する方法について説明します。 管理者以外のユーザーは、コンピューターの管理者になることなく、RSAT テストを実行することができます。

これらの指示は、管理者以外のユーザーが RSAT をインストールできるようにするものではありません。 この指示は、インストール後に RSAT の使用を有効にするだけです。 この状況には、Selenium フレームワークがインストールされているか、またはブラウザーのバージョンを更新した後に新しいブラウザーのドライバー インストールを使用している RSAT を初めて使用するときにが含まれます。 これらのインストール手順には、RSAT を管理者権限で実行していることが必要です。

複数のユーザーが共有する仮想マシン (VM) に RSAT がインストールされている場合、複数のユーザーが同時に RSAT を実行すると、ユーザーがブロックされることがあります。 たとえば、ユーザーがテスト ケースを実行中のリソースを保留にし、他のユーザーへのアクセスがブロックされることがあります。 これらの指示は、動作を変更しません。

## <a name="enable-non-administrator-rsat-use"></a>管理者以外の RSAT の使用を有効にする

管理者以外の RSAT の使用を有効にするには、2 つの PowerShell スクリプトと新しいショートカット ファイルが必要です。 これらのファイルは、**管理者以外を有効にする** という名前のサブフォルダーにある RSAT インストール フォルダーにあります。

1. Windows PowerShell を管理者として開きます。
2. フォルダーを RSAT インストール フォルダーの **管理者以外を有効にする** に変更します。 インストール フォルダーは、コンピューターで実行しているローカライズされた Windows にしたがって、**C:\Program Files (x86)\Regression Suite Automation Tool\Enable non admin** のように名前が付けられます。

    ![PowerShell のファイルの一覧。](media/config-file-list.png)

3. **管理者以外を有効にする** フォルダーに、これらのファイルが表示されます。

    + Enable-non-admin-mode.ps1
    + Enable-non-admin-user.ps1
    + Regression Suite Automation Tool (Non admin).lnk

4. 最初のファイル **Enable-non-admin-mode.ps1** は、コンピューターに対して管理者以外のモードを有効にする PowerShell スクリプトです。 このファイルを各コンピューターで 1 回実行します。

    これらの必須パラメーターを使用して、**管理者以外を有効にする** フォルダーからスクリプト **Enable-non-admin-mode.ps1** を直接実行します。

    + **action**: (文字列) 管理者以外のモードを有効または無効にするオプション。 有効な値は、**有効** または **無効** です。
    + **thumbprint**: (文字列) 証明書の拇印。 この値は、一般設定の RSAT で指定したのと同じ値である必要があります。

    次に例を示します。

    ```powershell
    .\Enable-non-admin-mode.ps1 "enable" "23055S5DXXXXXXXXXXXXXXXXXXXXXX"
    ```

    ヘルプを入手するには、このコマンドを実行します。

    ```powershell
    help .\Enable-non-admin-mode.ps1 -full
    ```

    > [!IMPORTANT]
    > **管理者以外を有効にする** フォルダーからこの PowerShell スクリプトを削除したり、コピーしないでください。 このフォルダーからのみ実行してください。

5. 2 つ目のファイル **Enable-non-admin-user.ps1** は、ユーザーに対して管理者以外のモードを有効にする PowerShell スクリプトです。 コンピューターで RSAT を使用する各ユーザーに対してこのスクリプトを実行します。

    これらの必須パラメーターを使用して、**管理者以外を有効にする** フォルダーからスクリプト **Enable-non-admin-user.ps1** を直接実行します。

    + **action**: (文字列) 管理者以外のモードを有効または無効にするオプション。 有効な値は、**有効** または **無効** です。
    + **thumbprint**: (文字列) 証明書の拇印。 この値は、一般設定の RSAT で指定したのと同じ値である必要があります。
    + **user**: (文字列) `domain\userName` 形式のローカル ユーザー名。

    次に例を示します。

    ```powershell
    .\Enable-non-admin-user.ps1 "enable" "TESTDOMAIN\testuser" "23055S5DXXXXXXXXXXXXXXXXXXXXXX"
    ```

    ヘルプを入手するには、このコマンドを実行します。

    ```powershell
    help .\Enable-non-admin-user.ps1 -full
    ```

    > [!IMPORTANT]
    > **管理者以外を有効にする** フォルダーからこの PowerShell スクリプトを削除したり、コピーしないでください。 このフォルダーからのみ実行してください。

6. PowerShell を閉じます。

7. ショートカット ファイル **Regression Suite Automation Tool (Non admin).lnk** をユーザーのデスクトップにコピーします。 (古いショートカットは、一部のユーザーは実行を許可されていない Visual Basic スクリプトを呼び出します。 新しいショートカットは、実行可能ファイルを直接呼び出します。)

    > [!IMPORTANT]
    > 古いショートカットは、コンピューターのすべてのユーザーが使用できる共有ファイルなので、削除しないでください。 ファイルを削除すると、すべてのユーザーに表示されなくなります。 すべてのユーザーに対して管理者以外のユーザーとしての実行が有効にされる場合、古いショートカットを削除しても問題ありません。 ただし、ショートカットは、新しいバージョンの RSAT がインストールされるたびに再び表示されます。

8. RSAT を最初に開始するとき、Selenium フレームワークとブラウザーのバージョンに一致するドライバーをダウンロードし、インストールする必要があります。 管理者ではないユーザーは、これらのコンポーネントのダウンロードとインストールができない場合があります。 この場合、RSAT は失敗し、例外が生成されることがあります。 コンポーネントをダウンロードし、インストールするには、管理者権限で RSAT を実行し、インストールを完了してください。 管理者権限で実行するには、新しいショートカット **Regression Suite Automation Tool (Non admin)** を右クリックし、**管理者として実行** を選択します。 インストールが完了した後、RSAT を閉じ、もう一度ユーザーに RSAT を実行させます。

9. 新しいショートカット **Regression Suite Automation Tool (Non admin)** を使用して RSAT を開始します。

## <a name="disable-non-administrator-rsat-use"></a>管理者以外の RSAT の使用を無効にする

管理者を使用して実行するようにコンピューターを元に戻す必要がある場合は、**action** パラメーターを **無効** にして、PowerShell スクリプト **Enable-non-admin-mode.ps1** を実行してください。

```powershell
.\Enable-non-admin-mode.ps1 "disable"
```

## <a name="future-versions-of-rsat"></a>RSAT の今後のバージョン

現在、この管理者以外のモードで RSAT を実行しているユーザーからのフィードバックを収集しています。 今後、インストール プロセスを変更し、管理者以外のユーザーを有効にする手順を自動的に含める可能性があります。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
