---
title: ジャストインタイム データベース アクセスの有効化
description: このトピックでは、ジャストインタイム (JIT) 方式でデータベース アクセスを有効にするために必要な手順を示します。
author: laneswenka
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: 7d5465ebca2cdda260ac68020db7839d6a76a2b4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753050"
---
# <a name="enable-just-in-time-database-access"></a><span data-ttu-id="52648-103">ジャストインタイム データベース アクセスの有効化</span><span class="sxs-lookup"><span data-stu-id="52648-103">Enable just-in-time database access</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52648-104">このトピックでは、ジャストインタイム (JIT) 方式を使用してデータベース アクセスを有効にするために必要な手順を示します。</span><span class="sxs-lookup"><span data-stu-id="52648-104">This topic provides the steps necessary to enable database access using a just-in-time (JIT) fashion.</span></span> <span data-ttu-id="52648-105">さまざまなトラブルシューティング作業、予定外のクエリの実行、またはデータ アップグレードの問題解決に、データベースへのアクセスが必要な場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="52648-105">This is useful if access to the database is required for various troubleshooting efforts, running unplanned queries, or data upgrade problem solving.</span></span> <span data-ttu-id="52648-106">このプロセスは、セルフサービスおよび Microsoft が管理するサンドボックス承認テスト環境の両方に対して使用できます。</span><span class="sxs-lookup"><span data-stu-id="52648-106">This process is available for both self-service as well as Microsoft-managed sandbox acceptance test environments.</span></span> <span data-ttu-id="52648-107">使用可能な環境のタイプの詳細については、[配置の概要](../deployment/cloud-deployment-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52648-107">For more information about the available environment types, see [Deployment overview](../deployment/cloud-deployment-overview.md).</span></span>

## <a name="microsoft-managed-environments-without-rdp-access"></a><span data-ttu-id="52648-108">RDP へのアクセスがない Microsoft が管理する環境</span><span class="sxs-lookup"><span data-stu-id="52648-108">Microsoft-managed environments without RDP access</span></span>

<span data-ttu-id="52648-109">サンドボックスへのリモート デスクトップ プロトコル (RDP) アクセスがない場合は、ご利用の IP アドレスを Lifecycle Services (LCS) からセルフサービス方式で許可リストに追加できます。</span><span class="sxs-lookup"><span data-stu-id="52648-109">If you no longer have Remote Desktop Protocol (RDP) access to your sandbox, you can add your IP address to the allow-list in a self-service manner from Lifecycle Services (LCS).</span></span> <span data-ttu-id="52648-110">環境から RDP が削除されると、環境の詳細ページのマシン資格情報セクションが削除されます。</span><span class="sxs-lookup"><span data-stu-id="52648-110">When RDP is removed from an environment, the machine credentials section of the environment details page is removed.</span></span>  <span data-ttu-id="52648-111">この場合、次のスクリーンショットに示すように、データベース アカウント セクションのみが残ります。</span><span class="sxs-lookup"><span data-stu-id="52648-111">This leaves just the database accounts section, as shown in the following screenshot.</span></span> 
<span data-ttu-id="52648-112">![データベース アカウント セクション](media/sql-jit1.png)</span><span class="sxs-lookup"><span data-stu-id="52648-112">![Database accounts section](media/sql-jit1.png)</span></span>

<span data-ttu-id="52648-113">サンドボックス環境の環境の詳細ページを開いて、**管理** > **アクセスの有効化** を選択してから、ダイアログ ボックスでソース環境の IP アドレスを追加します。</span><span class="sxs-lookup"><span data-stu-id="52648-113">From the environment details page for your sandbox environment, select **Maintain** > **Enable access**, and then in the dialog box, add the IP address of your source environment.</span></span> <span data-ttu-id="52648-114">このエントリは期限切れになり、入力した IP アドレスの横に有効期限が表示されます。</span><span class="sxs-lookup"><span data-stu-id="52648-114">This entry will expire, with the expire date shown alongside the IP address you entered.</span></span> <span data-ttu-id="52648-115">また、データベースの更新やデータベースのインポートなど、データベースの移動操作によってデータベースが置き換えられた後にも失われます。</span><span class="sxs-lookup"><span data-stu-id="52648-115">It also will be lost after the database is replaced by a database movement operation, such as database refresh or database import.</span></span>

<span data-ttu-id="52648-116">LCS のアカウントおよび有効にした IP アドレスを使用して、データベースに接続する SQL Server Management Studio (SSMS) のようなツールを使用することができるようになります。</span><span class="sxs-lookup"><span data-stu-id="52648-116">You can now use tools like SQL Server Management Studio (SSMS) to connect to the database, using the accounts from LCS and the IP address that you enabled.</span></span> <span data-ttu-id="52648-117">LCS はサーバーとデータベースを次の形式で表示することに注意してください: **serverName\databaseName**。</span><span class="sxs-lookup"><span data-stu-id="52648-117">Note that LCS shows the server and database in the following format: **serverName\databaseName**.</span></span>  <span data-ttu-id="52648-118">SSMS で接続するには、Azure パブリック クラウドの場合、**serverName.database.windows.net** などのドメイン名の接尾語を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52648-118">To connect in SSMS, you will need to append the domain name suffix, such as **serverName.database.windows.net** if you are in Azure public cloud.</span></span> <span data-ttu-id="52648-119">SSMS 接続ウィンドウの **オプション** タブでは、正常に接続するために **データベース** フィールドの databaseName 値も明示的に入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52648-119">On the **Options** tab in the SSMS connection window, you will also need to explicitly enter the databaseName value in the **Database** field to successfully connect.</span></span>

## <a name="self-service-environments"></a><span data-ttu-id="52648-120">セルフサービス環境</span><span class="sxs-lookup"><span data-stu-id="52648-120">Self-service environments</span></span>

<span data-ttu-id="52648-121">セルフサービス環境のタイプには、リモート デスクトップ プロトコル (RDP) アクセスまたは静的データベース アカウントはありませんでした。</span><span class="sxs-lookup"><span data-stu-id="52648-121">The self-service environment type has never had Remote Desktop Protocol (RDP) access or static database accounts.</span></span> <span data-ttu-id="52648-122">ただし、この場合もデータベースにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="52648-122">However, it is still possible to access the database.</span></span>

<span data-ttu-id="52648-123">サンドボックス環境の環境の詳細ページを開いて、**管理** > **アクセスの有効化** を選択してから、ダイアログ ボックスでソース環境の IP アドレスを追加します。</span><span class="sxs-lookup"><span data-stu-id="52648-123">From the environment details page for your sandbox environment, select **Maintain** > **Enable access**, and then in the dialog box, add the IP address of your source environment.</span></span> <span data-ttu-id="52648-124">エントリの有効期限は設定されていませんが、データベースの更新やデータベースのインポートなど、データベースの移動操作によってデータベースが置き換えられた後に失われます。</span><span class="sxs-lookup"><span data-stu-id="52648-124">This entry will not expire, however it will be lost after the database is replaced by a database movement operation, such as database refresh or database import.</span></span>

<span data-ttu-id="52648-125">また、**データベース アカウント** セクションで必要なアクセスのタイプを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52648-125">You also need to enter which type of access you require in the **Database Accounts** section.</span></span> <span data-ttu-id="52648-126">使用可能なオプションには、読み取りまたは読み取り-書き込みのアクセスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="52648-126">The available options include read or read-write access.</span></span> <span data-ttu-id="52648-127">簡単な理由の説明を入力し、**アクセスの要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52648-127">Enter a short reason description and then select **Request access**.</span></span>
<span data-ttu-id="52648-128">![アクセスの要求オプション](media/sql-jit2.png)</span><span class="sxs-lookup"><span data-stu-id="52648-128">![Request access option](media/sql-jit2.png)</span></span>

<span data-ttu-id="52648-129">ページが更新されると、有効期限の時間とともにデータベース アカウントが表示されます。</span><span class="sxs-lookup"><span data-stu-id="52648-129">When the page is refreshed, the database account will be shown with its expiry time.</span></span>
<span data-ttu-id="52648-130">![有効期限の時間とともに表示されるデータベース アカウント](media/sql-jit3.png)</span><span class="sxs-lookup"><span data-stu-id="52648-130">![Database account shown with the expiry time](media/sql-jit3.png)</span></span>

<span data-ttu-id="52648-131">LCS のアカウントおよび有効にした IP アドレスを使用して、データベースに接続する SQL Server Management Studio (SSMS) のようなツールを使用することができるようになります。</span><span class="sxs-lookup"><span data-stu-id="52648-131">You can now use tools like SQL Server Management Studio (SSMS) to connect to the database, using the accounts from LCS and the IP address you enabled.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]