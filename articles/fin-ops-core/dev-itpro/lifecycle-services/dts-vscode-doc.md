---
title: Dynamics 365 Translation Service Visual Studio Code 拡張機能 (パブリック プレビュー)
description: この記事では、Visual Studio Code 用の Microsoft Dynamics 365 Translation Service (DTS) 拡張機能を Visual Studio Code ワークフローに統合する方法について説明します。
author: joshsantana
ms.date: 04/18/2022
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: joshsantana
ms.search.validFrom: 2022-05-02
ms.openlocfilehash: 00d3efb3983aed2af175fd3eafb0775c3235332c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270699"
---
# <a name="dynamics-365-translation-service-visual-studio-code-extension-public-preview"></a>Dynamics 365 Translation Service Visual Studio Code 拡張機能 (パブリック プレビュー)

[!include[banner](../includes/banner.md)]
[!include[preview banner](../includes/preview-banner.md)]

Visual Studio Code (VS Code) 用 Microsoft Dynamics 365 Translation Service (DTS) 拡張機能では、ユーザーが VS Code 編集者から DTS と対話できます。 この拡張機能は、AL で拡張機能を開発する Dynamics 365 Business Central ユーザーに対して作成されました。 新しい DTS 変換要求を作成、送信、および取得するためのユーザー インターフェイス (UI) を提供します。

開始する前に、AL の開発についてよく理解する必要があります。 また、Business Central 開発環境で翻訳ファイルを使用する方法も説明します。 詳細については、次のトピックを参照してください。

- [AL で拡張機能の開発](/dynamics365/business-central/dev-itpro/developer/devenv-dev-overview)
- [翻訳ファイルに関する作業](/dynamics365/business-central/dev-itpro/developer/devenv-work-with-translation-files)

## <a name="install-vs-code-and-the-dts-extension"></a>VS Code および DTS 拡張機能のインストール

まだ実行していない場合は、[VS Code](https://code.visualstudio.com/) をインストールしてください。

次に、Visual Studio Marketplace から VS Code 用に DTS 拡張機能をインストールします。 拡張機能をインストールする方法については、[拡張機能 Marketplace](https://code.visualstudio.com/docs/editor/extension-marketplace) を参照してください。

## <a name="access-the-dts-extension"></a>DTS 拡張機能にアクセスする

AL ワークスペースに作業している場合、拡張機能は有効になります。 次の図に示すように、拡張機能にアクセスするには、VS Cude ウィンドウ側の活動バーの DTS アイコンを選択します。

![VS Code の活動バーの DTS アイコン。](media/dtsvsc-icon.png)

DTS ビューが開いています。 このファイルは、リソース ファイル エクスプローラと翻訳要求コンフィギュレーション ビューで構成されます。

![DTS ビュー。](media/dtsvsc-dtsview.png)

リソース ファイルがまだない場合は、[翻訳ファイルで実行](/dynamics365/business-central/dev-itpro/developer/devenv-work-with-translation-files) を参照して生成方法について確認してください。 XML ローカライズ交換ファイル形式 (XLIFF) を生成した後、リソース ファイル エクスプローラに表示されます。

## <a name="resource-file-explorer"></a>リソース ファイル エクスプローラー

リソース ファイル エクスプローラは、プロジェクトのリソースの移動に使用できるツリー ビューを提供します。

次の図は、1 つのワークスペースで複数の AL プロジェクト フォルダーを操作する例を示しています。 特定のソース XLIFF の翻訳ファイルを表示するには、ソース ノードを選択して展開します。 翻訳ジョブ後に、ツリー ビューが自動的に更新されない場合は、**更新** ボタンを使用することも可能です。

![リソース ファイル エクスプローラー。](media/dtsvsc-resourceexplorer.png)

## <a name="configure-translation-requests"></a>翻訳タスクを構成する

次の手順に従って、翻訳要求を構成します。

1. 翻訳要求コンフィギュレーション ビューで、コンフィギュレーションする AL プロジェクトを選択します。 1 つのワークスペースで複数の AL プロジェクト フォルダーを使用する場合を除き、使用可能なプロジェクトは 1 つのみです。
2. **ターゲット言語** リストで、ターゲット言語を選択します。
3. リサイクルする XLIFF ファイルがある場合は、**ファイルの選択** ボタンを使いファイルを追加できます。
4. すべてのデータを欧州連合 (EU) で処理する場合は、**欧州連合内の要求処理** チェックボックススを選択します。
5. **保存** を選択します。

![翻訳要求コンフィギュレーション ビュー。](media/dtsvsc-reqconfig.png)

## <a name="submit-translation-requests"></a>翻訳要求を送信

新しい翻訳要求を送信する前に、翻訳要求用のコンフィギュレーションが保存済みである必要があります。 新しい保存操作で上書きされない限り、そのコンフィギュレーションは将来のすべての要求に使用されます。

新しい要求を送信するには、リソース ファイル エクスプローラで省略記号ボタン (**...**) を選び、メニューで **翻訳要求の送信** を選択します。

![翻訳要求コマンドを送信。](media/dtsvsc-submit.png) 

要求の処理が開始される際、通知が表示され完了すると、別の通知が表示されます。

![要求のステータスに関する通知。](media/dtsvsc-processing.png)

各翻訳ファイルは、ソース翻訳ファイルが格納されているフォルダーに書き込まれます。

## <a name="authentication"></a>認証

プログラムにログインしていないと、認証を求めるメッセージが表示されます。 プロンプトで認証コードをメモし、**URL を開く** を選択します。

![認証プロンプト。](media/dtsvsc-auth.png)

新しい Web ブラウザー ウィンドウを開く必要があります。 新しいブラウザー ウィンドウを開いていない場合は、開いた後、アドレス バーにプロンプトから URL を入力します。 ブラウザー ウィンドウで、認証コードを入力します。 サインイン ページにリダイレクトされます。 資格情報を使用してサインインします。

## <a name="pending-requests"></a>保留中の要求

すべての翻訳要求をダウンロードする前に、VS Code セッションを終了すると、完了した要求をダウンロードできる通知が表示されます。

![DTS 要求の通知を保留中。](media/dtsvsc-pending.png)
