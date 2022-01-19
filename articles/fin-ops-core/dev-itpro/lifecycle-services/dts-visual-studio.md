---
title: Dynamics 365 Translation Service Visual Studio 拡張機能 (プライベート プレビュー)
description: このトピックでは、Visual Studio 用の Microsoft Dynamics 365 Translation Service (DTS) 拡張機能を Visual Studio ワークフローに統合する方法について説明します。
author: abmotgi
ms.date: 12/13/2021
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ROBOTS: NOINDEX, NOFOLLOW
ms.search.region: Global
ms.author: abmotgi
ms.search.validFrom: 2021-12-13
ms.openlocfilehash: abd3b927500de7ed1527b9750245258040764d67
ms.sourcegitcommit: a5861c2fef4071e130208ad20e26cb3a42a45cf1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/17/2021
ms.locfileid: "7928541"
---
# <a name="dynamics-365-translation-service-visual-studio-extension-private-preview"></a>Dynamics 365 Translation Service Visual Studio 拡張機能 (プライベート プレビュー)

[!include[banner](../includes/banner.md)]
[!include[preview banner](../includes/preview-banner.md)]

Visual Studio 用の Microsoft Dynamics 365 Translation Service (DTS) 拡張機能を使用すると、開発者は Visual Studio 統合開発環境 (IDE) から直接 DTS でアクションを実行できます。 たとえば、ユーザー インターフェイス (UI) ファイルを翻訳し、翻訳を再生成できます。 サポートされている機能の詳細については、[Dynamics 365 Translation Service の概要](translation-service-overview.md)を参照してください。

DTS Visual Studio 拡張機能を使用するには、Microsoft Dynamics Lifecycle Services (LCS) へのアクセス許可が必要です。 また、この拡張機能は、主に Visual Studio の Finance and Operations アプリの開発ワークフローをサポートすることを目的としています。 詳細については、[Finance and Operations アプリの開発と管理](/dynamics365/fin-ops-core/dev-itpro/)を参照してください。

> [!NOTE]
> DTS Visual Studio の拡張機能は、プライベート プレビューとしてのみ使用できます。 DTS は現在米国でのみ展開されているため、データは地域の境界外で処理および保管されることがあります。

## <a name="installing-the-extension"></a>拡張機能をインストールする

DTS Visual Studio 拡張機能をダウンロードする前に、プライベート プレビューへのアクセスを要求する必要があります。 アクセスが許可されたら、[Visual Studio Marketplace](https://marketplace.visualstudio.com/) から Visual Studio の拡張機能をダウンロードできます。

拡張機能をダウンロードして、Visual Studio の開発環境にインストールします。 拡張機能をインストールすると、**ツール** メニューに DTS から追加された新しいコマンドが含まれます。

## <a name="using-the-extension"></a>拡張機能を使用する

### <a name="sign-in-to-dts"></a>DTS にサインインする

DTS Visual Studio 拡張機能の使用を開始する前に、LCS で認証する必要があります。 サインアウト状態のときに翻訳または再生成コマンドを実行すると、自動的にサインインするよう求められます。

### <a name="access-the-dts-commands"></a>DTS コマンドにアクセスする

DTS コマンドには次の 2 つの方法でアクセスできます。

- メイン ツールバーの **ツール** を選択し、メニューの DTS コマンドを選択します。 4 つの DTS コマンドを使用できます: **DTS による翻訳**、**DTS による再生成**、**翻訳要求のダウンロード**、および **DTS からログアウト**。

    ![Visual Studio IDE のツール メニュー。](media/dts-vs-tools-menu.PNG)

- ソリューション内のファイルを選択したまま (または右クリックして)、ショートカット メニューから DTS コマンドを選択します。

## <a name="features"></a>機能

### <a name="translation-workflow"></a>翻訳ワークフロー

リソース ファイルを翻訳する前に、ソース言語とターゲット言語の両方のリソース ファイルを用意しておく必要があります。 ソース言語のリソース ファイルが既にある場合は、ソース リソース ノードを選択したまま (または右クリックして)**新しい言語の追加** を選択することで、ターゲット言語のファイルを作成できます。

![新しい言語のコマンドを追加します。](media/dts-vs-new-language.PNG)

**ラベル ファイル** ウィザードが表示されます。 目的の言語用に新しいラベル ファイルを作成するには、このウィザードを完了します。 ラベル ファイル ウィザードの使用方法については、[ラベル ファイルの作成方法](/dynamicsax-2012/developer/how-to-create-a-label-file)を参照してください。

![ラベル ファイル ウィザード。](media/dts-vs-label-wizard.PNG)

新しい翻訳要求を作成する準備が整いました。 **ツール** メニューから、**DTS による翻訳** を選択します。 または、ソリューション エクスプローラーでリソース ファイルを選択したまま (または右クリック)、**DTS による翻訳** を選択します。 新しい翻訳要求を構成できるダイアログ ボックスが表示されます。

次の表で、**DTS による翻訳** ダイアログ ボックスのフィールドについて説明します。

| フィールド              | 必須 | Description |
|--------------------|----------|-------------|
| 要求名       | あり | 要求名を入力します。 |
| 製品            | あり | 製品タイプを選択します。 |
| Project            | あり | リソース ファイルを含むプロジェクトを選択します。 |
| ソース言語    | あり | ソース ファイルの言語を選択します。 |
| ソース ファイル       | あり | 翻訳用のリソース ファイルを 1 つ以上選択します。 このフィールドには、選択したプロジェクトで参照されているすべてのリソース ファイルが一覧表示されます。 |
| ターゲット言語    | あり | <p>ソース ファイルを翻訳する言語を選択します。</p><p><strong>注記:</strong> リソース ファイルが既に存在するターゲット言語にのみ翻訳できます。 太字で示されている言語名は、Microsoft Dynamics 製品の一般提供 (GA) 言語です。 したがって、機械翻訳 (MT) モデルをこれらの言語で使用でき、MT モデルは Microsoft Dynamics の用語でトレーニングされます。 GA 言語以外の場合、MT モデルは一般的なドメイン トレーニングを使用します。</p> |
| 翻訳メモリ | いいえ | 特定のターゲット言語の翻訳メモリ ファイルを追加します。 (この値は、リサイクル用の翻訳メモリを含む ZIP ファイルです。) |
| カスタム MT を作成しますか?  | いいえ | アップロード済みの翻訳メモリを使用してカスタム MT モデルを作成するかどうかを選択します。 |

![DTS ダイアログ ボックスを使用して翻訳します。](media/dts-vs-translate.png)

翻訳要求の構成が完了したら、**送信** を選択して DTS に送信します。 その後、**出力** ウィンドウに要求のステータスが表示されます。 要求が完了すると、出力ファイル (翻訳メモリ ファイルおよび翻訳されたリソース ファイル) がダウンロードされます。 これらの出力ファイルは、モジュールの適切な言語サブフォルダに格納されます。

![DTS 拡張機能の出力ウィンドウ。](media/dts-vs-outputwindow.PNG)

出力ファイルがダウンロードされる前に Visual Studio が閉じられている場合は、**ツール** メニューの **翻訳要求の結果をダウンロード** を選択して手動でダウンロードできます。

### <a name="regeneration-workflow"></a>ワークフローを再生成する

DTS の翻訳を確認し、編集することをお勧めします。 XML ローカライズ交換ファイル形式 (XLIFF) ファイルは、対応する翻訳済リソース ファイルと同じディレクトリに格納されます。 XLIFF ファイルを編集する方法の詳細については、[翻訳メモリ ファイル](use-translation-service-tm.md)を参照してください。

XLIFF での翻訳ファイルのレビューと編集が完了したら、翻訳されたネイティブ形式ファイルを再生成できます。 **ツール** メニューから、**DTS による再生成** を選択します。 または、ソリューション エクスプローラーでリソース ファイルを選択したまま (または右クリック) にして、**DTS による再生成** を選択します。 再生成要求を構成できるダイアログ ボックスが表示されます。

次の表で、**DTS による再生成** ダイアログ ボックスのフィールドについて説明します。

| 入力             | 必須 | Description |
|-------------------|----------|-------------|
| Project           | あり | 修正された翻訳メモリに関連付けられているプロジェクトを選択します。 |
| 翻訳ファイル | あり | <p>修正された翻訳メモリ ファイルを 1 つ以上選択します。 リスト内のファイルは自動的に識別され、それらは以前の DTS 翻訳要求の結果です。</p><p>選択した修正済みの各翻訳メモリ ファイル (.xlf ファイル) は、対応するターゲットのネイティブ ファイルを再生成するために使用されます。 たとえば、**ExampleLabel.es.label.txt.xlf** は、**ExampleLabel.es.label.txt** を再生成します。</p> |

![DTS ダイアログ ボックスを使用して再生成します。](media/dts-vs-regenerate.PNG)

再生成要求の構成が完了したら、**送信** を選択して DTS に送信します。 **出力** ウィンドウに要求のステータスが表示されます。 要求が完了すると、出力ファイル (翻訳メモリ ファイルおよびターゲットの翻訳されたファイル) がダウンロードされます。
