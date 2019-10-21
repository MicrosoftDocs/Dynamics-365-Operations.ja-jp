---
title: アプリケーション チェッカーに対する BaseX のインストール
description: このトピックでは、開発環境で BaseX をインストールして設定する方法について説明します。
author: AndreasHassing
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: anniels
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Platform update 25
ms.openlocfilehash: 6799df7484cff3c804c0c63c918d2c4fe2846541
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191683"
---
# <a name="install-basex-for-application-checker"></a>アプリケーション チェッカーに対する BaseX のインストール

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

AppChecker を使用するには、BaseX をインストールする必要があります。X++ コンパイラを生成するクエリ抽象構文ツリーを保存して問い合わせる必要があるためです。 このトピックでは、開発環境で BaseX をインストールして設定する方法について説明します。

このトピックのセクションは、記載されている順序で実行する必要があります。

開発環境で作業しており、管理者特権がない場合、タブを使用して、管理者以外のユーザーに対する指示に切り替えます。

## <a name="prerequisites"></a>必要条件

BaseX は、Java ベースの XML ドキュメント データベースです。 8 またはそれ以降のバージョンの Java ランタイム環境 (JRE) が必要です。 BaseX をインストールする前に、JRE がインストールされていることを確認します。

# <a name="admin-install-javatabadmin"></a>[管理者: Java をインストール](#tab/admin)

[Javaダウンロード ページ](https://aka.ms/getjava)からJava JRE **64ビット**をダウンロードしてインストールします。

# <a name="non-admin-set-up-javatabnon-admin"></a>[管理者以外: Java をセットアップ](#tab/non-admin)

[Javaダウンロード ページ](https://www.oracle.com/technetwork/java/javase/downloads/index.html)から Java **Server JRE** をダウンロードします。

Java サーバー JRE は、.tar.gz 圧縮アーカイブとしてダウンロードされます。[7zip](https://www.7-zip.org/download.html) などのツールを使用して展開する必要があります。 インストールする必要はなく、[SourceForge](https://sourceforge.net/projects/sevenzip/files/7-Zip/9.20/7za920.zip/download) から 7zip をダウンロードできます。

アーカイブから Java サーバー JRE バイナリを抽出するには、次の Windows PowerShell コマンドを実行します。

> [!NOTE]
> ダウンロードしたサーバー JRE アーカイブのバージョンが反映されるように、これらのコマンドを変更する必要があります。 ここに示すコマンドでは、7za.exe とアーカイブの両方が現在の作業ディレクトリあります。

```powershell
.\7za.exe x .\server-jre-8u202-windows-x64.tar.gz # decompresses to current working directory
.\7za.exe x .\server-jre-8u202-windows-x64.tar # extracts jdk1.8.0_202 to current working directory
```

Java を展開したら、次のWindows PowerShellスクリプトを実行して、Java bin フォルダーを **PATH** 環境変数に追加します。

```powershell
[Environment]::SetEnvironmentVariable(
    "Path",
    # replace <path_to_jdk> below with the absolute path from the extracted jdk above
    [Environment]::GetEnvironmentVariable("Path", [EnvironmentVariableTarget]::User) + ";<path_to_jdk>\bin\",
    [EnvironmentVariableTarget]::User)
```

---

## <a name="download-basex"></a>BaseX をダウンロード

BaseX をダウンロードするには、[BaseX Web サイト](http://basex.org/download/)に移動し、最新版をダウンロードします。

# <a name="admin-download-basextabadmin"></a>[管理者: BaseX をダウンロード](#tab/admin)

ダウンロード ページから、Microsoft Windows インストーラーをダウンロードします。

# <a name="non-admin-download-basextabnon-admin"></a>[管理者以外: BaseX をダウンロード](#tab/non-admin)

ダウンロード ページから、zip パッケージをダウンロードします。

---

現時点では、最新バージョンは、9.1.2です。

## <a name="install-basex"></a>BaseXをインストール

# <a name="admin-install-basextabadmin"></a>[管理者: BaseX をインストール](#tab/admin)

モジュールをコンパイルする開発者のコンピューターで実行可能ファイルを実行します。 各ステップで、既定の設定を受け入れます。

# <a name="non-admin-set-up-basextabnon-admin"></a>[管理者以外: BaseX をセットアップ](#tab/non-admin)

以前にダウンロードした BaseX zip パッケージを抽出します。

---

> [!TIP]
> インストール ドライブにモデルの十分な領域がない場合、BaseX データのフォルダーを後で変更できます。 詳細については、[BaseX コンフィギュレーション](http://docs.basex.org/wiki/Configuration#Database_Directory)を参照してください。

BaseX をインストールしたら、次のWindows PowerShellスクリプトを実行して、BaseX bin フォルダーを **PATH** 環境変数に追加します。

```powershell
[Environment]::SetEnvironmentVariable(
    "Path",
    # replace <path_to_basex> below with the absolute path from the extracted basex zip package above
    [Environment]::GetEnvironmentVariable("Path", [EnvironmentVariableTarget]::User) + ";<path_to_basex>\bin\",
    [EnvironmentVariableTarget]::User)
```

> [!IMPORTANT]
> **PATH** 環境変数を設定するときに Microsoft Visual Studio が開いていた場合、再起動する必要があります。

## <a name="configure-basex-to-handle-your-model"></a>モデルを処理するために BaseXをコンフィギュレーションする

モデルのサイズによっては、BaseXは大量のメモリを使用します。

既定では、BaseXは約1200メガバイト (MB) のランダム アクセス メモリ (RAM) を最大で使用するようにコンフィギュレーションされます。 大規模なモデルを使用する場合は、次の手順に従ってこの限度を増やすことを検討してください。

1. 編集のために **\<BaseX インストール パス\>\\bin\\basex.bat** にあるバッチ スクリプトを開きます。
2. **set BASEX\_JVM=-Xmx1200m %BASEX\_JVM%** を含む行を見つけ、**-Xmx** の後の値を大きくします。 たとえば、値を **10g** に変更し、BaseX が最大 10 GB の RAM を追加できるようにします。

    詳細については、[非標準オプション](https://docs.oracle.com/javase/8/docs/technotes/tools/windows/java.html#BABHDABI)を参照してください。 Java ドキュメントのこのセクションでは、Java仮想マシン (VM) の制限値を大きくする方法について説明します。

    スクリプトの残りの部分はそのままにします。

> [!NOTE]
> Application Checker は保存とクエリに単独で実行可能ファイルを使用するため、BaseXサーバーを起動する必要はありません。
