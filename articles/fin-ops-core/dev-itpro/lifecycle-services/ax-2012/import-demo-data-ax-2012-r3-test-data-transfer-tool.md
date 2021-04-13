---
title: テスト データ転送ツールを使用した AX 2012 R3 のデモ データのインポート
description: このチュートリアルでは、テスト データ転送ツール (ベータ) を使用して Microsoft Dynamics AX 2012 R3 のデモ データをインポートします。
author: kfend
ms.date: 01/02/2020
ms.topic: article
ms.prod: dynamics-ax-2012
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 13401
ms.assetid: c16c9fb5-b1c1-4f22-a955-ff7325621a22
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: f77e1e570419e50933d42aee5539c7d9addd656c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745283"
---
# <a name="import-demo-data-for-ax-2012-r3-by-using-the-test-data-transfer-tool"></a><span data-ttu-id="9b95c-103">テスト データ転送ツールを使用した AX 2012 R3 のデモ データのインポート</span><span class="sxs-lookup"><span data-stu-id="9b95c-103">Import demo data for AX 2012 R3 by using the Test Data Transfer Tool</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9b95c-104">このチュートリアルでは、テスト データ転送ツール (ベータ) を使用して Microsoft Dynamics AX 2012 R3 のデモ データをインポートします。</span><span class="sxs-lookup"><span data-stu-id="9b95c-104">In this walkthrough, you will use the Test Data Transfer Tool (beta) to import the demo data for Microsoft Dynamics AX 2012 R3.</span></span>

<span data-ttu-id="9b95c-105">AX 2012 R3 のビジネス データベースが格納されているデータベース サーバーでローカルに作業することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9b95c-105">We strongly recommend that you work locally on the database server where the business database for AX 2012 R3 is stored.</span></span> <span data-ttu-id="9b95c-106">これは、より高速で、インポート中のネットワーク通信の問題を回避します。</span><span class="sxs-lookup"><span data-stu-id="9b95c-106">This is both faster, and avoids any network communication issues during import.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9b95c-107">前提条件</span><span class="sxs-lookup"><span data-stu-id="9b95c-107">Prerequisites</span></span>
<span data-ttu-id="9b95c-108">**注意:** テスト データ転送ツール (ベータ) は、開発、テスト、またはデモ環境でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="9b95c-108">**Caution:** The Test Data Transfer Tool (beta) is only supported for use in a development, test, or demo environment.</span></span> <span data-ttu-id="9b95c-109">実稼働環境では、この手順を実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="9b95c-109">Do not perform this procedure in a production environment.</span></span>

## <a name="download-the-demo-data-and-test-data-transfer-tool-beta"></a><span data-ttu-id="9b95c-110">デモ データおよび Test Data Transfer Tool (beta) をダウンロード</span><span class="sxs-lookup"><span data-stu-id="9b95c-110">Download the demo data and Test Data Transfer Tool (beta)</span></span>
1.  <span data-ttu-id="9b95c-111">AX 2012 R3 デモ データを、「[PartnerSource](https://go.microsoft.com/fwlink/?LinkId=403073)」のリリース ページからダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="9b95c-111">Download the AX 2012 R3 demo data from the Release Page on [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=403073).</span></span>
2.  <span data-ttu-id="9b95c-112">デモ データをパッケージから、使用している環境用の AX 2012 R3 ビジネス データベースをホストするデータベース サーバーに抽出します。</span><span class="sxs-lookup"><span data-stu-id="9b95c-112">Extract the demo data from the package to the database server that hosts the AX 2012 R3 business database for your environment.</span></span>
3.  <span data-ttu-id="9b95c-113">Test Data Transfer Tool (beta) ツール インストーラーを「[Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com)」の Downloadable ツール セクションからダウンロードし、使用環境に合わせて AX 2012 R3 ビジネス データべースをホストするデータベース サーバーにインストールします。</span><span class="sxs-lookup"><span data-stu-id="9b95c-113">Download the Test Data Transfer Tool (beta) tool installer from the Downloadable tools section of [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com), and install it on the database server that hosts the AX 2012 R3 business database for your environment.</span></span>
4.  <span data-ttu-id="9b95c-114">データをインポートするための適切なアクセス許可があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9b95c-114">Verify that you have appropriate permissions to import data.</span></span> <span data-ttu-id="9b95c-115">デモ データが保存されている場所への読み取りアクセスが必要です。SQL Server Management Studio では、**選択** ステートメントおよび **一括挿入** ステートメントを実行するためのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="9b95c-115">You must have read access to the location where the demo data is stored, and in SQL Server Management Studio, permission to execute **SELECT** statements and **BULK INSERT** statements.</span></span> <span data-ttu-id="9b95c-116">詳細については、 [テスト データ転送ツール (ベータ) のインストール](install-test-data-transfer-tool-beta.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b95c-116">For more information, see [Install the Test Data Transfer Tool (beta)](install-test-data-transfer-tool-beta.md).</span></span>

## <a name="run-the-test-data-transfer-tool-beta"></a><span data-ttu-id="9b95c-117">テスト データ転送ツール (ベータ) の実行</span><span class="sxs-lookup"><span data-stu-id="9b95c-117">Run the Test Data Transfer Tool (beta)</span></span>
1.  <span data-ttu-id="9b95c-118">**コントロール パネル** &gt; **サービス** に移動し、環境に関連付けられている AOS インスタンスを停止します。</span><span class="sxs-lookup"><span data-stu-id="9b95c-118">Go to **Control Panel** &gt; **Services**, and stop the AOS instance associated with your environment.</span></span>
2.  <span data-ttu-id="9b95c-119">Windows エクスプ ローラーを使用して、**テスト データ転送ツール (beta)** を参照します。</span><span class="sxs-lookup"><span data-stu-id="9b95c-119">Using Windows Explorer, browse to the **Test Data Transfer Tool (beta)**.</span></span>
3.  <span data-ttu-id="9b95c-120">Windows エクスプローラーの **ファイル** メニューで、**管理者としてコマンド プロンプトを開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9b95c-120">On the **File** menu in Windows Explorer, click **Open command prompt as administrator**.</span></span>
4.  <span data-ttu-id="9b95c-121">コマンド プロンプト で、次のコマンドを入力してデモデータをインポートします: **dp.exe import** \location\_of\_demo\_data \Name\_of\_AX\_business\_database \ServernameInstanceName.</span><span class="sxs-lookup"><span data-stu-id="9b95c-121">At the command prompt, enter the following command to import the demo data: **dp.exe import** \location\_of\_demo\_data \Name\_of\_AX\_business\_database \ServernameInstanceName.</span></span> 

    <span data-ttu-id="9b95c-122">ローカル コンピューター上でテスト データ転送ツール (beta) を実行していると仮定します。</span><span class="sxs-lookup"><span data-stu-id="9b95c-122">We assume that you are running the Test Data Transfer Tool (beta) on the local computer.</span></span> <span data-ttu-id="9b95c-123">ローカル コンピューターに名前付きインスタンスがある場合は、localhostInstanceName または **.** という構文を使用できます。</span><span class="sxs-lookup"><span data-stu-id="9b95c-123">If you have a named instance on the local computer, you can use the syntax localhostInstanceName or **.**</span></span> <span data-ttu-id="9b95c-124">InstanceName.</span><span class="sxs-lookup"><span data-stu-id="9b95c-124">InstanceName.</span></span> <span data-ttu-id="9b95c-125">次の例では、データが E ドライブの demodata フォルダーにあり、ビジネス データベースには MicrosoftDynamicsAX: **dp.exe import e:demodata MicrosoftDynamicsAX** と名前が付けられています。</span><span class="sxs-lookup"><span data-stu-id="9b95c-125">In the following example, the data is on the E drive, in the demodata folder, and the business database is named MicrosoftDynamicsAX: **dp.exe import e:demodata MicrosoftDynamicsAX**</span></span> 

    > [!NOTE]
    > <span data-ttu-id="9b95c-126">デモ データのインポートに 30 分以上がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="9b95c-126">It may take over 30 minutes to import the demo data.</span></span> <span data-ttu-id="9b95c-127">インポート中に問題が発生した場合は、ログ ファイル **DPLog.xml** を開くことができ、テスト データ転送ツール (ベータ) を実行したフォルダに作成されます。</span><span class="sxs-lookup"><span data-stu-id="9b95c-127">If you encounter any issues during the import, you can open the log file **DPLog.xml**, which will be created in the folder where you ran the Test Data Transfer Tool (beta).</span></span>
5.  <span data-ttu-id="9b95c-128">**コントロール パネル** &gt; **サービス** に移動し、環境に関連付けられている AOS インスタンスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="9b95c-128">Go to **Control Panel** &gt; **Services**, and restart the AOS instance associated with your environment.</span></span>


<a name="additional-resources"></a><span data-ttu-id="9b95c-129">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9b95c-129">Additional resources</span></span>
--------

[<span data-ttu-id="9b95c-130">テスト データ転送ツール (ベータ)</span><span class="sxs-lookup"><span data-stu-id="9b95c-130">Test Data Transfer Tool (beta)</span></span>](test-data-transfer-tool-beta-2012.md)

[<span data-ttu-id="9b95c-131">テスト データ転送ツール (ベータ) のインストール</span><span class="sxs-lookup"><span data-stu-id="9b95c-131">Install the Test Data Transfer Tool (beta)</span></span>](install-test-data-transfer-tool-beta.md)

[<span data-ttu-id="9b95c-132">テスト データ転送ツール (ベータ) の実行</span><span class="sxs-lookup"><span data-stu-id="9b95c-132">Run the Test Data Transfer Tool (beta)</span></span>](run-test-data-transfer-tool-beta.md)





[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]