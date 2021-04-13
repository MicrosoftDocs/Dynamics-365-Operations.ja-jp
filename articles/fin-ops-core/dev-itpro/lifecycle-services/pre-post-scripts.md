---
title: ローカル エージェントの配置前スクリプトおよび配置後スクリプト
description: このトピックでは、ローカル エージェントの配置前スクリプトおよび配置後スクリプトに関する情報を提供します。
author: faix
ms.date: 08/07/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: 2929e2ade38888ae56ffef6a6b34de324f2e2abf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743945"
---
# <a name="local-agent-pre-deployment-and-post-deployment-scripts"></a><span data-ttu-id="9b2f2-103">ローカル エージェントの配置前スクリプトおよび配置後スクリプト</span><span class="sxs-lookup"><span data-stu-id="9b2f2-103">Local agent pre-deployment and post-deployment scripts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b2f2-104">ローカル エージェント 2.3.0 は、配置前スクリプトおよび配置後スクリプトの実行をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-104">Local agent 2.3.0 supports the execution of pre-deployment and post-deployment scripts.</span></span> <span data-ttu-id="9b2f2-105">したがって、環境配置の前後に実行される Microsoft Windows PowerShell スクリプトを設定できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-105">Therefore, customers can now set up Microsoft Windows PowerShell scripts that are run before and after the environment is deployed.</span></span> <span data-ttu-id="9b2f2-106">この機能は、配置と再配置に適用されるほか、サービス操作にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-106">This feature applies to deployments and redeployments, and also to servicing operations.</span></span>

<span data-ttu-id="9b2f2-107">この機能を使用できるようにするには、エージェント ファイル共有にスクリプト フォルダーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-107">To make this feature available, you must create a Scripts folder in the agent file share.</span></span> <span data-ttu-id="9b2f2-108">配置前スクリプトを実行するには、スクリプト フォルダーに **PreDeployment.ps1** ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-108">To run a pre-deployment script, create a **PreDeployment.ps1** file in the Scripts folder.</span></span> <span data-ttu-id="9b2f2-109">配置後スクリプトを実行するには、**PostDeployment.ps1** ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-109">To run a post-deployment script, create a **PostDeployment.ps1** file.</span></span> <span data-ttu-id="9b2f2-110">次の例は、フォルダー構造を示しています。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-110">The following examples show the folder structure:</span></span>

- <span data-ttu-id="9b2f2-111">\\\\\\fileserver\\agent\\scripts\\PreDeployment.ps1</span><span class="sxs-lookup"><span data-stu-id="9b2f2-111">\\\\\\fileserver\\agent\\scripts\\PreDeployment.ps1</span></span>
- <span data-ttu-id="9b2f2-112">\\\\\\fileserver\\agent\\scripts\\PostDeployment.ps1</span><span class="sxs-lookup"><span data-stu-id="9b2f2-112">\\\\\\fileserver\\agent\\scripts\\PostDeployment.ps1</span></span>

<span data-ttu-id="9b2f2-113">これらのファイルが存在しない場合、配置は通常どおりに続行されます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-113">If these files don't exist, the deployment continues as usual.</span></span> <span data-ttu-id="9b2f2-114">次の例は、新しい配置フローを示しています。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-114">The following examples show the new deployment flow.</span></span>

<span data-ttu-id="9b2f2-115">**配置または再配置**:</span><span class="sxs-lookup"><span data-stu-id="9b2f2-115">**Deployment or redeployment:**</span></span>

1. <span data-ttu-id="9b2f2-116">異常なモジュールを取得します。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-116">Get unhealthy modules.</span></span> <span data-ttu-id="9b2f2-117">このステップでは、既存のサービスの健全性を取得して、問題を見つけます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-117">In this step, the health of existing services is obtained to find which are unhealthy.</span></span> <span data-ttu-id="9b2f2-118">このステップは再配置シナリオにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-118">This step applies only to redeployment scenarios.</span></span>
2. <span data-ttu-id="9b2f2-119">モジュールをクリーンアップします。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-119">Clean up modules.</span></span> <span data-ttu-id="9b2f2-120">このステップでは、サービスが取り除かれ、**wp** フォルダの内容が削除されます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-120">In this step, the services are removed and the contents of the **wp** folder are deleted.</span></span> <span data-ttu-id="9b2f2-121">このステップは再配置シナリオにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-121">This step applies only to redeployment scenarios.</span></span>
3. <span data-ttu-id="9b2f2-122">ダウンロード コンポーネントをリンクします。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-122">Link download artifacts.</span></span> <span data-ttu-id="9b2f2-123">このステップでは、Microsoft Dynamics Lifecycle Services (LCS) からのコンポーネントのダウンロード、抽出、処理が行われます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-123">In this step, download, extraction, and processing of artifacts from Microsoft Dynamics Lifecycle Services (LCS) takes place.</span></span>
4. <span data-ttu-id="9b2f2-124">配置前スクリプト。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-124">Pre-deployment script.</span></span> <span data-ttu-id="9b2f2-125">このステップでは **PreDeployment.ps1** スクリプト (存在する場合) が実行されます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-125">In this step the **PreDeployment.ps1** script is executed (if it exists).</span></span>
5. <span data-ttu-id="9b2f2-126">モジュールを設定します。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-126">Set up modules.</span></span> <span data-ttu-id="9b2f2-127">このステップでは、新しいサービスが配置されます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-127">In this step, the new services are deployed.</span></span>
6. <span data-ttu-id="9b2f2-128">配置後スクリプト。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-128">Post-Deployment script.</span></span> <span data-ttu-id="9b2f2-129">このステップでは **PostDeployment.ps1** スクリプト (存在する場合) が実行されます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-129">In this step the **PostDeployment.ps1** script is executed (if it exists).</span></span>

<span data-ttu-id="9b2f2-130">**サービス:**</span><span class="sxs-lookup"><span data-stu-id="9b2f2-130">**Servicing:**</span></span>

1. <span data-ttu-id="9b2f2-131">サービスの準備を行います。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-131">Prepare for servicing.</span></span> <span data-ttu-id="9b2f2-132">このステップでは、LCS でパッケージを準備し、環境にダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-132">In this step, the package is prepared in LCS and gets downloaded to the environment.</span></span>
2. <span data-ttu-id="9b2f2-133">モジュールをクリーンアップします。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-133">Clean up modules.</span></span> <span data-ttu-id="9b2f2-134">このステップでは、サービスが取り除かれ、**wp** フォルダの内容が削除されます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-134">In this step, the services are removed and the contents of the **wp** folder are deleted.</span></span>
3. <span data-ttu-id="9b2f2-135">ダウンロード コンポーネントをリンクします。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-135">Link download artifacts.</span></span> <span data-ttu-id="9b2f2-136">このステップでは、LCS から以前にダウンロードしたコンポーネントの抽出および処理が行われます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-136">In this step, extraction and processing of previously downloaded artifacts from LCS takes place.</span></span>
4. <span data-ttu-id="9b2f2-137">配置前スクリプト。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-137">Pre-deployment script.</span></span> <span data-ttu-id="9b2f2-138">このステップでは **PreDeployment.ps1** スクリプト (存在する場合) が実行されます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-138">In this step the **PreDeployment.ps1** script is executed (if it exists).</span></span>
5. <span data-ttu-id="9b2f2-139">モジュールを設定します。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-139">Set up modules.</span></span> <span data-ttu-id="9b2f2-140">このステップでは、新しいサービスが配置されます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-140">In this step, the new services are deployed.</span></span>
6. <span data-ttu-id="9b2f2-141">配置後スクリプト。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-141">Post-Deployment script.</span></span> <span data-ttu-id="9b2f2-142">このステップでは **PostDeployment.ps1** スクリプト (存在する場合) が実行されます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-142">In this step the **PostDeployment.ps1** script is executed (if it exists).</span></span>

> [!NOTE]
> <span data-ttu-id="9b2f2-143">配置前スクリプトと配置後スクリプトには、任意のものを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-143">The pre-deployment and post-deployment scripts can contain anything.</span></span> <span data-ttu-id="9b2f2-144">スクリプトによって実行されるコードは、顧客の責任を負うものです。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-144">The code that the scripts run is solely the customer's responsibility.</span></span> <span data-ttu-id="9b2f2-145">ローカル エージェントはスクリプトを起動するだけです。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-145">The local agent just invokes the scripts.</span></span>

## <a name="customizations"></a><span data-ttu-id="9b2f2-146">カスタマイズ</span><span class="sxs-lookup"><span data-stu-id="9b2f2-146">Customizations</span></span>

<span data-ttu-id="9b2f2-147">スクリプト実行の既定のタイムアウトは 30 分です。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-147">The default time-out for script execution is 30 minutes.</span></span> <span data-ttu-id="9b2f2-148">この値を変更するには、localagent-config.json ファイルを変更し、その変更したファイルを使用してローカル エージェントを再インストールします。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-148">To change this value, modify the localagent-config.json file, and then reinstall the local agent by using the modified file.</span></span> <span data-ttu-id="9b2f2-149">次の属性は、タイムアウト値を定義するもので、ここで示すように設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-149">The following attribute defines time-out value and must be set as shown here.</span></span> <span data-ttu-id="9b2f2-150">(ここに示すコードは、ファイル内の **LocalAgent** コンポーネントに含まれています。)</span><span class="sxs-lookup"><span data-stu-id="9b2f2-150">(The code that is shown here is part of the **LocalAgent** component in the file.)</span></span>

```json
"powershellScriptRunner": {
    "timeoutMinutes": {
        "value": "30"
        }
    }
```

## <a name="logging"></a><span data-ttu-id="9b2f2-151">ログ記録</span><span class="sxs-lookup"><span data-stu-id="9b2f2-151">Logging</span></span>

<span data-ttu-id="9b2f2-152">スクリプトからの出力およびエラー メッセージは、.log ファイルや .err ファイルとして、スクリプト フォルダーのログ フォルダーに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-152">The outputs and error messages from the scripts are written, as .log and .err files, into the Logs folder in the Scripts folder.</span></span> <span data-ttu-id="9b2f2-153">スクリプトがタイムアウトした場合は、エラー メッセージのみがログに記録されます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-153">If a script times out, only an error message is logged.</span></span> <span data-ttu-id="9b2f2-154">このエラー メッセージには、タイムアウトのメッセージが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-154">This error message has a time-out message.</span></span> <span data-ttu-id="9b2f2-155">この場合、他の出力は記録されません。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-155">No other outputs are logged in this situation.</span></span>

<span data-ttu-id="9b2f2-156">スクリプトの実行は、Event Tracing for Windows (ETW) イベントとしてもログに記録されます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-156">Execution of the scripts is also logged as Event Tracing for Windows (ETW) events.</span></span> <span data-ttu-id="9b2f2-157">これらのイベントはイベント ビューアーで表示できます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-157">You can view these events in Event Viewer.</span></span> <span data-ttu-id="9b2f2-158">スクリプトでエラーが発生すると、エラー イベントがログに記録されますが、配置は通常どおり続行されます。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-158">If a script produces any errors, an error event is logged, but deployment continues as usual.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]