---
title: "メンテナンス モード"
description: "この記事では、Microsoft Dynamics 365 for Finance and Operations のメンテナンス モードについて説明します。 メンテナンス モードは、システム機能に影響を与える可能性のあるシステム変更を、システム管理者が安全に実行できる新しいシステム全体に適用される設定です。"
author: manalidongre
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysConfiguration
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 70292
ms.assetid: c11a35e8-40bb-4005-adf3-cfd998a418fc
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5b997b1e5ccf9bc43f4290812c66d736285eb7ce
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="maintenance-mode"></a><span data-ttu-id="2c34e-104">メンテナンス モード</span><span class="sxs-lookup"><span data-stu-id="2c34e-104">Maintenance mode</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c34e-105">この記事では、Microsoft Dynamics 365 for Finance and Operations のメンテナンス モードについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2c34e-105">This article provides information about maintenance mode in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="2c34e-106">メンテナンス モードは、システム機能に影響を与える可能性のあるシステム変更を、システム管理者が安全に実行できる新しいシステム全体に適用される設定です。</span><span class="sxs-lookup"><span data-stu-id="2c34e-106">Maintenance mode is a new system-wide setting that lets system administrators safely make system changes that might affect system functionality.</span></span>

<span data-ttu-id="2c34e-107">Microsoft Dynamics 365 for Finance and Operations には、メンテナンス モードという名前の新しいシステム全体に適用される設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2c34e-107">Microsoft Dynamics 365 for Finance and Operations includes a new system-wide setting that is named maintenance mode.</span></span> <span data-ttu-id="2c34e-108">メンテナンス モードを有効にすると、システム機能に影響を与える可能性のあるシステム変更を、システム管理者が安全に実行する方法が提供されます。</span><span class="sxs-lookup"><span data-stu-id="2c34e-108">When maintenance mode is turned on, it provides a safe way for system administrators to make system changes that might affect system functionality.</span></span> <span data-ttu-id="2c34e-109">たとえば、コンフィギュレーション キーは、有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="2c34e-109">For example, configuration keys can be enabled or disabled.</span></span> <span data-ttu-id="2c34e-110">メンテナンス モードがオンのとき、システム管理者および **メンテナンス モード ユーザー** ロールを持つユーザーのみがシステムにサインインすることができます。</span><span class="sxs-lookup"><span data-stu-id="2c34e-110">While maintenance mode is on, only system administrators and users who have the **Maintenance mode user** role can sign in to the system.</span></span> <span data-ttu-id="2c34e-111">既定では、メンテナンス モードがオフになっています。</span><span class="sxs-lookup"><span data-stu-id="2c34e-111">By default, maintenance mode is turned off.</span></span>

## <a name="turning-maintenance-mode-on-and-off"></a><span data-ttu-id="2c34e-112">メンテナンス モードのオン/オフを切り替え</span><span class="sxs-lookup"><span data-stu-id="2c34e-112">Turning maintenance mode on and off</span></span>
<span data-ttu-id="2c34e-113">メンテナンス モードがオフのとき、**ライセンス コンフィギュレーション** ページを編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="2c34e-113">When maintenance mode is off, you can't edit the **License configuration** page.</span></span>
<span data-ttu-id="2c34e-114">次のコマンドを実行して、メンテナンス モードをローカルでオンにすることができます。</span><span class="sxs-lookup"><span data-stu-id="2c34e-114">You can turn on maintenance mode locally by running the following command.</span></span> 

<span data-ttu-id="2c34e-115">**注記:** 一部の仮想マシン (VM) では、Deployment.Setup.exe ツールの正確な場所が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="2c34e-115">**Note:** On some virtual machines (VMs), the exact location of the Deployment.Setup.exe tool might differ.</span></span> <span data-ttu-id="2c34e-116">AosServiceWebRootbin を確認してください。</span><span class="sxs-lookup"><span data-stu-id="2c34e-116">Check AosServiceWebRootbin.</span></span>

    J:\AosService\PackagesLocalDirectory\Bin\Microsoft.Dynamics.AX.Deployment.Setup.exe --metadatadir J:\AosService\PackagesLocalDirectory --bindir J:\AosService\PackagesLocalDirectory\Bin --sqlserver . --sqldatabase axdb --sqluser axdbadmin --sqlpwd ********* --setupmode maintenancemode --isinmaintenancemode true

<span data-ttu-id="2c34e-117">次のテーブルに、このコマンドで使用されるパラメーターを示します。</span><span class="sxs-lookup"><span data-stu-id="2c34e-117">The following table describes the parameters that are used in this command.</span></span>

| <span data-ttu-id="2c34e-118">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="2c34e-118">Parameter name</span></span>              | <span data-ttu-id="2c34e-119">説明</span><span class="sxs-lookup"><span data-stu-id="2c34e-119">Description</span></span>                                                                                                       |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c34e-120">--setupmode maintenancemode</span><span class="sxs-lookup"><span data-stu-id="2c34e-120">--setupmode maintenancemode</span></span> | <span data-ttu-id="2c34e-121">システムをメンテナンス モードにするかメンテナンス モードを解除するかをセットアップ ツールに通知するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="2c34e-121">Use this parameter to inform the setup tool that the system will be put into or taken out of maintenance mode.</span></span>    |
| <span data-ttu-id="2c34e-122">--metadatadir</span><span class="sxs-lookup"><span data-stu-id="2c34e-122">--metadatadir</span></span>               | <span data-ttu-id="2c34e-123">メタデータ ディレクトリ を指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="2c34e-123">Use this parameter to specify the metadata directory.</span></span> <span data-ttu-id="2c34e-124">既定のパッケージ ディレクトリを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c34e-124">You should use the default packages directory.</span></span>              |
| <span data-ttu-id="2c34e-125">--bindir</span><span class="sxs-lookup"><span data-stu-id="2c34e-125">--bindir</span></span>                    | <span data-ttu-id="2c34e-126">バイナリ ディレクトリ を指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="2c34e-126">Use this parameter to specify the binaries directory.</span></span> <span data-ttu-id="2c34e-127">既定のパッケージ ディレクトリを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c34e-127">You should use the default packages directory.</span></span>              |
| <span data-ttu-id="2c34e-128">--sqlserver</span><span class="sxs-lookup"><span data-stu-id="2c34e-128">--sqlserver</span></span>                 | <span data-ttu-id="2c34e-129">Microsoft SQL Server を指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="2c34e-129">Use this parameter to specify the Microsoft SQL Server.</span></span> <span data-ttu-id="2c34e-130">1 ボックス環境では、ピリオド (**.**) を使用します。</span><span class="sxs-lookup"><span data-stu-id="2c34e-130">For one-box environments, use a period (**.**).</span></span>           |
| <span data-ttu-id="2c34e-131">--sqluser</span><span class="sxs-lookup"><span data-stu-id="2c34e-131">--sqluser</span></span>                   | <span data-ttu-id="2c34e-132">SQL Server のユーザーを指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="2c34e-132">Use this parameter to specify the SQL Server user.</span></span> <span data-ttu-id="2c34e-133">**AOSUser** を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c34e-133">You should use **AOSUser**.</span></span>                                    |
| <span data-ttu-id="2c34e-134">--sqlpwd</span><span class="sxs-lookup"><span data-stu-id="2c34e-134">--sqlpwd</span></span>                    | <span data-ttu-id="2c34e-135">SQL Server のパスワードを指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="2c34e-135">Use this parameter to specify the SQL Server password.</span></span>                                                            |
| <span data-ttu-id="2c34e-136">--isinmaintenancemode</span><span class="sxs-lookup"><span data-stu-id="2c34e-136">--isinmaintenancemode</span></span>       | <span data-ttu-id="2c34e-137">構成モードを有効または無効にするには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="2c34e-137">Use this parameter to turn configuration mode on or off.</span></span> <span data-ttu-id="2c34e-138">オンにするには **true** とし、オフにするには **false** にします。</span><span class="sxs-lookup"><span data-stu-id="2c34e-138">Use **true** to turn it on and **false** to turn it off.</span></span> |

<span data-ttu-id="2c34e-139">Microsoft Dynamics 365 for Finance and Operations の Application Object Server (AOS)のインスタンスを再起動すると、システムはメンテナンス モードになります。</span><span class="sxs-lookup"><span data-stu-id="2c34e-139">After the instance of Microsoft Dynamics 365 for Finance and Operations Application Object Server (AOS) is restarted, the system will be in maintenance mode.</span></span> <span data-ttu-id="2c34e-140">次のスクリーン ショットに示すように、構成キーを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="2c34e-140">You can then enable configuration keys, as shown in the following screen shot.</span></span> 

<span data-ttu-id="2c34e-141">[![license-configuration-page-when-not-in-maintenance-mode](./media/license-configuration-page-when-not-in-maintenance-mode.png)](./media/license-configuration-page-when-not-in-maintenance-mode.png)</span><span class="sxs-lookup"><span data-stu-id="2c34e-141">[![license-configuration-page-when-not-in-maintenance-mode](./media/license-configuration-page-when-not-in-maintenance-mode.png)](./media/license-configuration-page-when-not-in-maintenance-mode.png)</span></span> 

<span data-ttu-id="2c34e-142">システムがメンテナンス モードになっているときに、システム管理者または**メンテナンス モード ユーザー** ロールを持つユーザーではない人が、Finance and Operations にアクセスしようとすると、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2c34e-142">If you try to access Finance and Operations while the system is in maintenance mode, but you aren't a system administrator or a user who has the **Maintenance mode user** role, you receive an error message.</span></span> 

<span data-ttu-id="2c34e-143">次のコマンドを実行して、メンテナンス モードをオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="2c34e-143">You can turn off maintenance mode by running the following command.</span></span>

    J:\AosService\PackagesLocalDirectory\Bin\Microsoft.Dynamics.AX.Deployment.Setup.exe --metadatadir J:\AosService\PackagesLocalDirectory --bindir J:\AosService\PackagesLocalDirectory\Bin --sqlserver . --sqldatabase axdb --sqluser axdbadmin --sqlpwd ********* --setupmode maintenancemode --isinmaintenancemode false

## <a name="maintenance-mode-in-production-environments"></a><span data-ttu-id="2c34e-144">実稼動環境でのメンテナンス モード</span><span class="sxs-lookup"><span data-stu-id="2c34e-144">Maintenance mode in production environments</span></span>
<span data-ttu-id="2c34e-145">実稼動環境でメンテナンス モードを有効にするには、**サービス要求** ページで LCS の **その他の要求** フォームを使用して、Dynamics サービス エンジニアリング (DSE) チームに要求を送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c34e-145">To turn on maintenance mode in a production environment, you must submit a request to the Dynamics Service Engineering (DSE) team by using the **Other request** form in LCS on the **Service requests** page.</span></span> <span data-ttu-id="2c34e-146">LCS を通しての要求の送信の詳細については、[Dynamics サービス エンジニア リング チームへの要求の送信](../lifecycle-services/submit-request-dynamics-service-engineering-team.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2c34e-146">For more information about submitting a request through LCS, see , see [Submit a request to the Dynamics Service Engineering team](../lifecycle-services/submit-request-dynamics-service-engineering-team.md).</span></span> 

<span data-ttu-id="2c34e-147">Dynamics サービス エンジニアリング チームは、システムをメンテナンス モードにし、お客様と連携してコンフィギュレーションの更新を完了します。</span><span class="sxs-lookup"><span data-stu-id="2c34e-147">The Dynamics Service Engineering team will move your system into maintenance mode and work with you to complete the configuration updates.</span></span> <span data-ttu-id="2c34e-148">更新が完了したという確認をチームが受け取った後、メンテナンス モードからシステムが削除されます。</span><span class="sxs-lookup"><span data-stu-id="2c34e-148">After the team receives a confirmation from you that the updates are complete, they will remove your system from maintenance mode.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="2c34e-149">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="2c34e-149">Troubleshooting</span></span>
<span data-ttu-id="2c34e-150">イベント ビューアーにエラーが検出できます。</span><span class="sxs-lookup"><span data-stu-id="2c34e-150">Errors can be found in Event viewer.</span></span>




