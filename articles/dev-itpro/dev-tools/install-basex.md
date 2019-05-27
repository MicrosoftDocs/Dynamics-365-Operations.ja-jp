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
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: anniels
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Platform update 25
ms.openlocfilehash: 35755f94383f124e503c4416149a7afa4eed4411
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536978"
---
# <a name="install-basex-for-application-checker"></a><span data-ttu-id="2540e-103">アプリケーション チェッカーに対する BaseX のインストール</span><span class="sxs-lookup"><span data-stu-id="2540e-103">Install BaseX for Application Checker</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="2540e-104">AppChecker を使用するには、BaseX をインストールする必要があります。X++ コンパイラを生成するクエリ抽象構文ツリーを保存して問い合わせる必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="2540e-104">Application Checker depends on an installation of BaseX to store and query abstract syntax trees that the X++ compiler generates.</span></span> <span data-ttu-id="2540e-105">このトピックでは、開発環境で BaseX をインストールして設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2540e-105">This topic explains how to install and set up BaseX in a developer environment.</span></span>

<span data-ttu-id="2540e-106">このトピックのセクションは、記載されている順序で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2540e-106">The sections of this topic should be completed in the order that they appear in.</span></span>

<span data-ttu-id="2540e-107">開発環境で作業しており、管理者特権がない場合、タブを使用して、管理者以外のユーザーに対する指示に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="2540e-107">If you're working in a developer environment and don't have admin privileges, use the tabs to switch to the instructions for non-admin users.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2540e-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="2540e-108">Prerequisites</span></span>

<span data-ttu-id="2540e-109">BaseX は、Java ベースの XML ドキュメント データベースです。</span><span class="sxs-lookup"><span data-stu-id="2540e-109">BaseX is a Java-based XML document database.</span></span> <span data-ttu-id="2540e-110">8 またはそれ以降のバージョンの Java ランタイム環境 (JRE) が必要です。</span><span class="sxs-lookup"><span data-stu-id="2540e-110">It requires a Java Runtime Environment (JRE) of version 8 or later.</span></span> <span data-ttu-id="2540e-111">BaseX をインストールする前に、JRE がインストールされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2540e-111">Before you install BaseX, verify that a JRE is installed.</span></span>

# <a name="admin-install-javatabadmin"></a>[<span data-ttu-id="2540e-112">管理者: Java をインストール</span><span class="sxs-lookup"><span data-stu-id="2540e-112">Admin: Install Java</span></span>](#tab/admin)

<span data-ttu-id="2540e-113">[Javaダウンロード ページ](https://aka.ms/getjava)からJava JRE **64ビット**をダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="2540e-113">Download and install Java JRE **64-bit** from the [Java download page](https://aka.ms/getjava).</span></span>

# <a name="non-admin-set-up-javatabnon-admin"></a>[<span data-ttu-id="2540e-114">管理者以外: Java をセットアップ</span><span class="sxs-lookup"><span data-stu-id="2540e-114">Non-admin: Set up Java</span></span>](#tab/non-admin)

<span data-ttu-id="2540e-115">[Javaダウンロード ページ](https://www.oracle.com/technetwork/java/javase/downloads/index.html)から Java **Server JRE** をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="2540e-115">Download Java **Server JRE** from the [Java download page](https://www.oracle.com/technetwork/java/javase/downloads/index.html).</span></span>

<span data-ttu-id="2540e-116">Java サーバー JRE は、.tar.gz 圧縮アーカイブとしてダウンロードされます。[7zip](https://www.7-zip.org/download.html) などのツールを使用して展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2540e-116">Java Server JRE is downloaded as a .tar.gz compressed archive that you must extract by using a tool such as [7zip](https://www.7-zip.org/download.html).</span></span> <span data-ttu-id="2540e-117">インストールする必要はなく、[SourceForge](https://sourceforge.net/projects/sevenzip/files/7-Zip/9.20/7za920.zip/download) から 7zip をダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="2540e-117">You can download 7zip, without having to install it, from [SourceForge](https://sourceforge.net/projects/sevenzip/files/7-Zip/9.20/7za920.zip/download).</span></span>

<span data-ttu-id="2540e-118">アーカイブから Java サーバー JRE バイナリを抽出するには、次の Windows PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="2540e-118">To extract Java Server JRE binaries from the archive, run the following Windows PowerShell commands.</span></span>

> [!NOTE]
> <span data-ttu-id="2540e-119">ダウンロードしたサーバー JRE アーカイブのバージョンが反映されるように、これらのコマンドを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2540e-119">You must modify these commands so that they reflect the version of the Server JRE archive that you downloaded.</span></span> <span data-ttu-id="2540e-120">ここに示すコマンドでは、7za.exe とアーカイブの両方が現在の作業ディレクトリあります。</span><span class="sxs-lookup"><span data-stu-id="2540e-120">In the commands that are shown here, both 7za.exe and the archive are in the current working directory.</span></span>

```powershell
.\7za.exe x .\server-jre-8u202-windows-x64.tar.gz # decompresses to current working directory
.\7za.exe x .\server-jre-8u202-windows-x64.tar # extracts jdk1.8.0_202 to current working directory
```

<span data-ttu-id="2540e-121">Java を展開したら、次のWindows PowerShellスクリプトを実行して、Java bin フォルダーを **PATH** 環境変数に追加します。</span><span class="sxs-lookup"><span data-stu-id="2540e-121">After you extract Java, modify and run the following Windows PowerShell script to add the Java bin folder to your **PATH** environment variable.</span></span>

```powershell
[Environment]::SetEnvironmentVariable(
    "Path",
    # replace <path_to_jdk> below with the absolute path from the extracted jdk above
    [Environment]::GetEnvironmentVariable("Path", [EnvironmentVariableTarget]::User) + ";<path_to_jdk>\bin\",
    [EnvironmentVariableTarget]::User)
```

---

## <a name="download-basex"></a><span data-ttu-id="2540e-122">BaseX をダウンロード</span><span class="sxs-lookup"><span data-stu-id="2540e-122">Download BaseX</span></span>

<span data-ttu-id="2540e-123">BaseX をダウンロードするには、[BaseX Web サイト](http://basex.org/download/)に移動し、最新版をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="2540e-123">To download BaseX, go to the [BaseX website](http://basex.org/download/), and download the latest version.</span></span>

# <a name="admin-download-basextabadmin"></a>[<span data-ttu-id="2540e-124">管理者: BaseX をダウンロード</span><span class="sxs-lookup"><span data-stu-id="2540e-124">Admin: Download BaseX</span></span>](#tab/admin)

<span data-ttu-id="2540e-125">ダウンロード ページから、Microsoft Windows インストーラーをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="2540e-125">Download the Microsoft Windows installer from the download page.</span></span>

# <a name="non-admin-download-basextabnon-admin"></a>[<span data-ttu-id="2540e-126">管理者以外: BaseX をダウンロード</span><span class="sxs-lookup"><span data-stu-id="2540e-126">Non-admin: Download BaseX</span></span>](#tab/non-admin)

<span data-ttu-id="2540e-127">ダウンロード ページから、zip パッケージをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="2540e-127">Download the zip package from the download page.</span></span>

---

<span data-ttu-id="2540e-128">現時点では、最新バージョンは、9.1.2です。</span><span class="sxs-lookup"><span data-stu-id="2540e-128">Currently, the latest version is 9.1.2.</span></span>

## <a name="install-basex"></a><span data-ttu-id="2540e-129">BaseXをインストール</span><span class="sxs-lookup"><span data-stu-id="2540e-129">Install BaseX</span></span>

# <a name="admin-install-basextabadmin"></a>[<span data-ttu-id="2540e-130">管理者: BaseX をインストール</span><span class="sxs-lookup"><span data-stu-id="2540e-130">Admin: Install BaseX</span></span>](#tab/admin)

<span data-ttu-id="2540e-131">モジュールをコンパイルする開発者のコンピューターで実行可能ファイルを実行します。</span><span class="sxs-lookup"><span data-stu-id="2540e-131">Run the executable file on the developer machine where you will compile your module.</span></span> <span data-ttu-id="2540e-132">各ステップで、既定の設定を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="2540e-132">For each step, accept the default settings.</span></span>

# <a name="non-admin-set-up-basextabnon-admin"></a>[<span data-ttu-id="2540e-133">管理者以外: BaseX をセットアップ</span><span class="sxs-lookup"><span data-stu-id="2540e-133">Non-admin: Set up BaseX</span></span>](#tab/non-admin)

<span data-ttu-id="2540e-134">以前にダウンロードした BaseX zip パッケージを抽出します。</span><span class="sxs-lookup"><span data-stu-id="2540e-134">Extract the BaseX zip package that you previously downloaded.</span></span>

---

> [!TIP]
> <span data-ttu-id="2540e-135">インストール ドライブにモデルの十分な領域がない場合、BaseX データのフォルダーを後で変更できます。</span><span class="sxs-lookup"><span data-stu-id="2540e-135">If the installation drive doesn't have enough space for your model, you can change the folder for BaseX data later.</span></span> <span data-ttu-id="2540e-136">詳細については、[BaseX コンフィギュレーション](http://docs.basex.org/wiki/Configuration#Database_Directory)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2540e-136">For more information, see [BaseX configuration](http://docs.basex.org/wiki/Configuration#Database_Directory).</span></span>

<span data-ttu-id="2540e-137">BaseX をインストールしたら、次のWindows PowerShellスクリプトを実行して、BaseX bin フォルダーを **PATH** 環境変数に追加します。</span><span class="sxs-lookup"><span data-stu-id="2540e-137">After you install BaseX, modify and run the following Windows PowerShell script to add the BaseX bin folder to your **PATH** environment variable.</span></span>

```powershell
[Environment]::SetEnvironmentVariable(
    "Path",
    # replace <path_to_basex> below with the absolute path from the extracted basex zip package above
    [Environment]::GetEnvironmentVariable("Path", [EnvironmentVariableTarget]::User) + ";<path_to_basex>\bin\",
    [EnvironmentVariableTarget]::User)
```

> [!IMPORTANT]
> <span data-ttu-id="2540e-138">**PATH** 環境変数を設定するときに Microsoft Visual Studio が開いていた場合、再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2540e-138">If Microsoft Visual Studio was open while you set the **PATH** environment variable, you must restart it.</span></span>

## <a name="configure-basex-to-handle-your-model"></a><span data-ttu-id="2540e-139">モデルを処理するために BaseXをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="2540e-139">Configure BaseX to handle your model</span></span>

<span data-ttu-id="2540e-140">モデルのサイズによっては、BaseXは大量のメモリを使用します。</span><span class="sxs-lookup"><span data-stu-id="2540e-140">Depending on the size of your model, BaseX can use a lot of memory.</span></span>

<span data-ttu-id="2540e-141">既定では、BaseXは約1200メガバイト (MB) のランダム アクセス メモリ (RAM) を最大で使用するようにコンフィギュレーションされます。</span><span class="sxs-lookup"><span data-stu-id="2540e-141">By default, BaseX is configured to use a maximum of about 1200 megabytes (MB) of random-access memory (RAM).</span></span> <span data-ttu-id="2540e-142">大規模なモデルを使用する場合は、次の手順に従ってこの限度を増やすことを検討してください。</span><span class="sxs-lookup"><span data-stu-id="2540e-142">If you have a large model, you should consider increasing this limit by following these steps.</span></span>

1. <span data-ttu-id="2540e-143">編集のために **\<BaseX インストール パス\>\\bin\\basex.bat** にあるバッチ スクリプトを開きます。</span><span class="sxs-lookup"><span data-stu-id="2540e-143">Open the batch script at **\<BaseX Install Path\>\\bin\\basex.bat** for editing.</span></span>
2. <span data-ttu-id="2540e-144">**set BASEX\_JVM=-Xmx1200m %BASEX\_JVM%** を含む行を見つけ、**-Xmx** の後の値を大きくします。</span><span class="sxs-lookup"><span data-stu-id="2540e-144">Find the line that contains **set BASEX\_JVM=-Xmx1200m %BASEX\_JVM%**, and increase the value after **-Xmx**.</span></span> <span data-ttu-id="2540e-145">たとえば、値を **10g** に変更し、BaseX が最大 10 GB の RAM を追加できるようにします。</span><span class="sxs-lookup"><span data-stu-id="2540e-145">For example, change the value to **10g** to let BaseX use up to 10 GB of RAM.</span></span>

    <span data-ttu-id="2540e-146">詳細については、[非標準オプション](https://docs.oracle.com/javase/8/docs/technotes/tools/windows/java.html#BABHDABI)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2540e-146">For more information, see [Non-Standard Options](https://docs.oracle.com/javase/8/docs/technotes/tools/windows/java.html#BABHDABI).</span></span> <span data-ttu-id="2540e-147">Java ドキュメントのこのセクションでは、Java仮想マシン (VM) の制限値を大きくする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2540e-147">This section of the Java documentation explains how to increase the limits of the Java virtual machine (VM).</span></span>

    <span data-ttu-id="2540e-148">スクリプトの残りの部分はそのままにします。</span><span class="sxs-lookup"><span data-stu-id="2540e-148">Leave the rest of the script unchanged.</span></span>

> [!NOTE]
> <span data-ttu-id="2540e-149">Application Checker は保存とクエリに単独で実行可能ファイルを使用するため、BaseXサーバーを起動する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2540e-149">You don't have to start the BaseX server, because Application Checker will use the standalone executable file for storage and queries.</span></span>
