---
title: テスト データ転送ツール (ベータ) のインストール
description: このトピックでは、Microsoft Dynamics AX 2012 のテスト データ転送ツールをインストールする方法について説明します。
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 17551
ms.assetid: 1681290d-93f0-489d-9746-7793b2ffe690
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 16ae6a0f5fded1702a1131592511b36ff568b86e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183247"
---
# <a name="install-the-test-data-transfer-tool-beta"></a><span data-ttu-id="d8364-103">テスト データ転送ツール (ベータ) のインストール</span><span class="sxs-lookup"><span data-stu-id="d8364-103">Install the Test Data Transfer Tool (beta)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8364-104">このトピックでは、Microsoft Dynamics AX 2012 のテスト データ転送ツール (ベータ) をインストールする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d8364-104">This topic describes how to install the Microsoft Dynamics AX 2012 Test Data Transfer Tool (beta).</span></span> <span data-ttu-id="d8364-105">上級者のみ、このツールを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8364-105">Only advanced users should use this tool.</span></span> 

<span data-ttu-id="d8364-106">Microsoft SQL Server の使用経験がある開発者またはデータベース管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8364-106">You must be a database administrator or a developer who has experience using Microsoft SQL Server.</span></span> <span data-ttu-id="d8364-107">また、処理している Microsoft Dynamics AX 2012 データベースに直接読み取り/書き込みを行って、データベースをホストしているコンピューター上で直接アプリケーションを実行するためのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="d8364-107">You must also have permission to read from or write directly to the Microsoft Dynamics AX 2012 database that you are working with, and to execute applications directly on the computer that is hosting the database.</span></span> <span data-ttu-id="d8364-108">開始する前に、環境には次のコンポーネントが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8364-108">Before you begin, your environment must include the following components:</span></span>

-   <span data-ttu-id="d8364-109">ビジネス用に構成されている Microsoft Dynamics AX 2012 データベース。</span><span class="sxs-lookup"><span data-stu-id="d8364-109">An Microsoft Dynamics AX 2012 database that has been configured for your business.</span></span>
-   <span data-ttu-id="d8364-110">SQL Server 一括コピー ツール (bcp) がコマンド プロンプト パスにあるように、SQL Server クライアント ツールは、ローカル コンピューターと、データの転送先のデータベース サーバーにインストールされます。</span><span class="sxs-lookup"><span data-stu-id="d8364-110">The SQL Server client tools installed on the local computer, and on the database server that you are transferring data to, so that the SQL Server bulk copy tool (bcp) is in the command-prompt path.</span></span>

<span data-ttu-id="d8364-111">エクスポート中に、ツールが各テーブルに対して 3 つのファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="d8364-111">During export, the tool creates three files for each table.</span></span> <span data-ttu-id="d8364-112">エクスポートされるすべてのテーブルに対して十分なハード ディスク領域があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d8364-112">Make sure that there is enough hard disk space for all the tables that are exported.</span></span>

## <a name="install-the-test-data-transfer-tool-beta"></a><span data-ttu-id="d8364-113">テスト データ転送ツール (ベータ) のインストール</span><span class="sxs-lookup"><span data-stu-id="d8364-113">Install the Test Data Transfer Tool (beta)</span></span>
1.  <span data-ttu-id="d8364-114">「[Microsoft Dynamics Lifecycle Services](http://go.microsoft.com/fwlink/?LinkId=228148)」のダウンロード可能なツール セクションからツールを取得し、ローカル フォルダーに展開します。</span><span class="sxs-lookup"><span data-stu-id="d8364-114">Get the tool from the Downloadable tools section of [Microsoft Dynamics Lifecycle Services](http://go.microsoft.com/fwlink/?LinkId=228148), and extract it to a local folder.</span></span>
2.  <span data-ttu-id="d8364-115">**AX2012TestDataTransferTool.msi** を右クリックして**管理者として実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d8364-115">Right-click **AX2012TestDataTransferTool.msi**, and then click **Run as administrator**.</span></span>
3.  <span data-ttu-id="d8364-116">**設定** **ウィザード**で、ライセンス条項に同意してからツールのバイナリおよびファイルをインストールする場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8364-116">In the **Setup** **Wizard**, accept the license terms, and then select the location in which to install the binaries and files for the tool.</span></span> <span data-ttu-id="d8364-117">既定では、ツールは %Program Files%/Microsoft Dynamics AX 2012 のテスト データ転送ツール (ベータ) にインストールされています。</span><span class="sxs-lookup"><span data-stu-id="d8364-117">By default, the tool is installed to %Program Files%/Microsoft Dynamics AX 2012 Test Data Transfer Tool (Beta).</span></span>



<a name="additional-resources"></a><span data-ttu-id="d8364-118">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d8364-118">Additional resources</span></span>
--------

[<span data-ttu-id="d8364-119">Microsoft Dynamics AX 2012 用のテスト データ転送ツール (ベータ)</span><span class="sxs-lookup"><span data-stu-id="d8364-119">Test Data Transfer Tool (beta) for Microsoft Dynamics AX 2012</span></span>](test-data-transfer-tool-beta-2012.md)

[<span data-ttu-id="d8364-120">Microsoft Dynamics AX 用のテスト データ転送ツール (ベータ) の実行</span><span class="sxs-lookup"><span data-stu-id="d8364-120">Run the Test Data Transfer Tool (beta) for Microsoft Dynamics AX</span></span>](run-test-data-transfer-tool-beta.md)


