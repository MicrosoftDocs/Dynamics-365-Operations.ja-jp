---
title: インスタンスのコピー
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009628"
---
# <a name="copy-an-instance"></a><span data-ttu-id="f81f4-102">インスタンスのコピー</span><span class="sxs-lookup"><span data-stu-id="f81f4-102">Copy an instance</span></span>

<span data-ttu-id="f81f4-103">Microsoft Dynamics Lifecycle Services (LCS) を使用して、Microsoft Dynamics 365 Human Resources データベース をサンドボックス環境にコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="f81f4-103">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="f81f4-104">別のサンドボックス環境を使用する場合は、その環境から対象のサンドボックス環境にデータベースをコピーすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f81f4-104">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="f81f4-105">インスタンスをコピーするには、次の項目をご確認ください:</span><span class="sxs-lookup"><span data-stu-id="f81f4-105">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="f81f4-106">上書きを行う Human Resources インスタンスは、サンドボックス環境である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f81f4-106">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="f81f4-107">コピー元とコピー先の環境は同じリージョンにある必要があります。</span><span class="sxs-lookup"><span data-stu-id="f81f4-107">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="f81f4-108">異なるリージョン間でのコピーはできません。</span><span class="sxs-lookup"><span data-stu-id="f81f4-108">You can't copy across regions.</span></span>

- <span data-ttu-id="f81f4-109">対象の環境の管理者である必要があります。そうすることでコピー後のインスタンスにサイン インすることができます。</span><span class="sxs-lookup"><span data-stu-id="f81f4-109">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="f81f4-110">Human Resources データベースをコピーする際は、 Microsoft PowerApps 環境に含まれる要素 (アプリやデータ) のコピーをしないでください。</span><span class="sxs-lookup"><span data-stu-id="f81f4-110">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="f81f4-111">PowerApps 環境の各要素のコピー方法については、 [環境をコピーする](https://docs.microsoft.com/power-platform/admin/copy-environment) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f81f4-111">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="f81f4-112">上書きを行う PowerApps 環境 は、サンドボックス環境である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f81f4-112">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="f81f4-113">PowerApps の運用環境をサンドボックス環境に変更するには、グローバル テナントの管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f81f4-113">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="f81f4-114">PowerApps 環境の変更に関する詳細については、 [インスタンスを切り替える](https://docs.microsoft.com/dynamics365/admin/switch-instance) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f81f4-114">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="f81f4-115">Human Resources データベースのコピーによる影響</span><span class="sxs-lookup"><span data-stu-id="f81f4-115">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="f81f4-116">Human Resources データベースのコピーをする際に、次のイベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="f81f4-116">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="f81f4-117">コピーの過程で、対象とする環境の既存のデータベースが削除されます。</span><span class="sxs-lookup"><span data-stu-id="f81f4-117">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="f81f4-118">コピーの完了後は、既存のデータベースを復元することはできません。</span><span class="sxs-lookup"><span data-stu-id="f81f4-118">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="f81f4-119">対象とする環境は、コピーが完了するまで使用することができません。</span><span class="sxs-lookup"><span data-stu-id="f81f4-119">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="f81f4-120">Microsoft Azure Blob storage 内のドキュメントは環境間でのコピーがされません。</span><span class="sxs-lookup"><span data-stu-id="f81f4-120">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="f81f4-121">そのため、この ストレージ に属するドキュメントやテンプレートはコピーされず、コピー元の環境に残留します。</span><span class="sxs-lookup"><span data-stu-id="f81f4-121">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="f81f4-122">管理者ユーザー、およびその他の内部サービス ユーザー アカウントを除くすべてのユーザーは使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="f81f4-122">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="f81f4-123">そのため、管理者ユーザーは他のユーザーがシステムに復帰する前にデータの削除や難読化することができます。</span><span class="sxs-lookup"><span data-stu-id="f81f4-123">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="f81f4-124">管理者ユーザーは、特定のサービスまたは URL に統合エンドポイントを再接続するなど、必要な構成の変更を加える必要があります。</span><span class="sxs-lookup"><span data-stu-id="f81f4-124">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="f81f4-125">Human Resources データベースのコピー</span><span class="sxs-lookup"><span data-stu-id="f81f4-125">Copy the Human Resources database</span></span>

<span data-ttu-id="f81f4-126">このタスクを完了するには、最初にインスタンスをコピーして、続いて Microsoft Power Platform 管理センターを PowerApps 環境へとコピーします。</span><span class="sxs-lookup"><span data-stu-id="f81f4-126">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="f81f4-127">インスタンスのコピーを行うと、対象となるインスタンスのデータベースが削除されます。</span><span class="sxs-lookup"><span data-stu-id="f81f4-127">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="f81f4-128">対象のインスタンスをこの処理中に使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="f81f4-128">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="f81f4-129">LCS にサインインし、コピーをするインスタンスを含む LCS プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="f81f4-129">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="f81f4-130">LCS プロジェクトでは、**人事管理アプリの管理**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f81f4-130">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="f81f4-131">コピーをするインスタンスを選択して、**コピー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f81f4-131">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="f81f4-132">**インスタンスをコピーする** のタスク ウィンドウで、上書きするインスタンスを選択し、続いて **コピー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f81f4-132">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="f81f4-133">**コピーのステータス** フィールドの値が **完了** となるまで待機してください。</span><span class="sxs-lookup"><span data-stu-id="f81f4-133">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="f81f4-134">上書きするインスタンスを選択します</span><span class="sxs-lookup"><span data-stu-id="f81f4-134">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="f81f4-135">**Power Platform** を選択し、 Microsoft Power Platform 管理センターにサインインします。</span><span class="sxs-lookup"><span data-stu-id="f81f4-135">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="f81f4-136">Power Platformを選択します</span><span class="sxs-lookup"><span data-stu-id="f81f4-136">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="f81f4-137">コピーをするPowerApps 環境 を選択して、 **コピー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f81f4-137">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="f81f4-138">コピー処理の完了後、対象のインスタンスにサインインし、 Common Data Service 統合を有効化します。</span><span class="sxs-lookup"><span data-stu-id="f81f4-138">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="f81f4-139">詳細情報と解説については、 [Common Data Service の統合を構成する](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f81f4-139">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="f81f4-140">データの属性と状態</span><span class="sxs-lookup"><span data-stu-id="f81f4-140">Data elements and statuses</span></span>

<span data-ttu-id="f81f4-141">次のデータ要素は、Human Resources インスタンスのコピーを行う際にコピーされません。</span><span class="sxs-lookup"><span data-stu-id="f81f4-141">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="f81f4-142">**LogisticsElectronicAddress** テーブルの電子メールアドレス</span><span class="sxs-lookup"><span data-stu-id="f81f4-142">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="f81f4-143">**BatchJobHistory**、 **BatchHistory**、 **BatchConstraintHistory** テーブル内のバッチジョブ履歴</span><span class="sxs-lookup"><span data-stu-id="f81f4-143">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="f81f4-144">**SysEmailSMTPPassword** テーブル内の Simple Mail Transfer Protocol (シンプル メール トランスファー プロトコル、SMTP) のパスワード</span><span class="sxs-lookup"><span data-stu-id="f81f4-144">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="f81f4-145">**SysEmailParameters** テーブル内の SMTP リレーサーバー</span><span class="sxs-lookup"><span data-stu-id="f81f4-145">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="f81f4-146">**PrintMgmtSettings** と **PrintMgmtDocInstance** テーブル内 の 印刷管理設定</span><span class="sxs-lookup"><span data-stu-id="f81f4-146">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="f81f4-147">**SysServerConfig**、 **SysServerSessions**、 **SysCorpNetPrinters**、 **SysClientSessions**、 **BatchServerConfig**、 **BatchServerGroup** テーブル内の環境固有のレコード</span><span class="sxs-lookup"><span data-stu-id="f81f4-147">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="f81f4-148">DocuValue テーブル内のドキュメント添付ファイル。</span><span class="sxs-lookup"><span data-stu-id="f81f4-148">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="f81f4-149">コピー元の環境で上書きされた Microsoft Office のテンプレートを含む要素</span><span class="sxs-lookup"><span data-stu-id="f81f4-149">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="f81f4-150">**PersonnelIntegrationConfiguration** テーブル内の接続文字列</span><span class="sxs-lookup"><span data-stu-id="f81f4-150">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="f81f4-151">これらの要素は、環境固有のものであるためコピーされません。</span><span class="sxs-lookup"><span data-stu-id="f81f4-151">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="f81f4-152">**BatchServerConfig** と **SysCorpNetPrinters** のレコードを含む例。</span><span class="sxs-lookup"><span data-stu-id="f81f4-152">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="f81f4-153">その他の要素は、サポート チケットのデータ量が多くなる懸念があるためコピーされません。</span><span class="sxs-lookup"><span data-stu-id="f81f4-153">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="f81f4-154">たとえば、SMTP がユーザーの受け入れテスト (サンドボックス) 環境で有効化されていると重複する電子メールが送信されてしまう、バッチジョブが有効化されていると無効な統合メッセージが送信されてしまう、管理者が更新後のクリーンアップ処理を実行する前にユーザーが有効化されてしまうなどの可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f81f4-154">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="f81f4-155">加えて、インスタンスのコピー時には、次の状態変更がされます:</span><span class="sxs-lookup"><span data-stu-id="f81f4-155">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="f81f4-156">管理者以外の全ユーザーが **無効化** されます。</span><span class="sxs-lookup"><span data-stu-id="f81f4-156">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="f81f4-157">一部のシステムジョブを除いた、すべてのバッチジョブが **保留** となります。</span><span class="sxs-lookup"><span data-stu-id="f81f4-157">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="f81f4-158">環境管理者</span><span class="sxs-lookup"><span data-stu-id="f81f4-158">Environment admin</span></span>

<span data-ttu-id="f81f4-159">対象となるサンドボックス環境の、管理者を含む全ユーザーが、コピー元のユーザーに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="f81f4-159">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="f81f4-160">インスタンスのコピーの実行者は、自分にコピー先の環境で管理者の権限があることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f81f4-160">Before you copy an instance, be sure that you're an Administrator in the target environment.</span></span> <span data-ttu-id="f81f4-161">管理者の権限がない場合は、コピーの完了後に対象のサンドボックス環境にサインインすることができません。</span><span class="sxs-lookup"><span data-stu-id="f81f4-161">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="f81f4-162">コピー先のサンドボックス環境内の全ての非管理者ユーザーは無効化され、サンドボックス環境へと不必要なログインができません。</span><span class="sxs-lookup"><span data-stu-id="f81f4-162">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="f81f4-163">システム管理者は、必要に応じてユーザーを有効化することができます。</span><span class="sxs-lookup"><span data-stu-id="f81f4-163">Administrators can reenable users if needed.</span></span>
