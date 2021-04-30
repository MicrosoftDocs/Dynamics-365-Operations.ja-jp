---
title: インスタンスのコピー
description: Microsoft Dynamics Lifecycle Services (LCS) を使用して、Microsoft Dynamics 365 Human Resources データベース をサンドボックス環境にコピーすることができます。
author: andreabichsel
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44df05083cd3c91e5dcbdb3062665c2145d92a7e
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889815"
---
# <a name="copy-an-instance"></a><span data-ttu-id="ba06a-103">インスタンスのコピー</span><span class="sxs-lookup"><span data-stu-id="ba06a-103">Copy an instance</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ba06a-104">Microsoft Dynamics Lifecycle Services (LCS) を使用して、Microsoft Dynamics 365 Human Resources データベース をサンドボックス環境にコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="ba06a-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="ba06a-105">別のサンドボックス環境を使用する場合は、その環境から対象のサンドボックス環境にデータベースをコピーすることもできます。</span><span class="sxs-lookup"><span data-stu-id="ba06a-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="ba06a-106">インスタンスをコピーする際には、次のヒントを念頭に置いてください :</span><span class="sxs-lookup"><span data-stu-id="ba06a-106">To copy an instance, keep the following tips in mind:</span></span>

- <span data-ttu-id="ba06a-107">上書きを行う Human Resources インスタンスは、サンドボックス環境である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba06a-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="ba06a-108">コピー元とコピー先の環境は同じリージョン内にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba06a-108">The environments you're copying from and to must be in the same region.</span></span> <span data-ttu-id="ba06a-109">異なるリージョン間でのコピーはできません。</span><span class="sxs-lookup"><span data-stu-id="ba06a-109">You can't copy across regions.</span></span>

- <span data-ttu-id="ba06a-110">対象の環境の管理者である必要があります。そうすることでコピー後のインスタンスにサイン インすることができます。</span><span class="sxs-lookup"><span data-stu-id="ba06a-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="ba06a-111">Human Resources データベースをコピーする際は、 Microsoft Power Apps 環境に含まれる要素 (アプリやデータ) のコピーをしないでください。</span><span class="sxs-lookup"><span data-stu-id="ba06a-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft Power Apps environment.</span></span> <span data-ttu-id="ba06a-112">Power Apps 環境の各要素のコピー方法については、 [環境をコピーする](/power-platform/admin/copy-environment) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba06a-112">For information about how to copy elements in a Power Apps environment, see [Copy an environment](/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="ba06a-113">上書きを行う Power Apps 環境 は、サンドボックス環境である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba06a-113">The Power Apps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="ba06a-114">Power Apps の運用環境をサンドボックス環境に変更するには、グローバル テナントの管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba06a-114">You must be a global tenant admin to change a Power Apps production environment to a sandbox environment.</span></span> <span data-ttu-id="ba06a-115">Power Apps 環境の変更に関する詳細については、 [インスタンスを切り替える](/dynamics365/admin/switch-instance) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba06a-115">For more information about changing a Power Apps environment, see [Switch an instance](/dynamics365/admin/switch-instance).</span></span>

- <span data-ttu-id="ba06a-116">サンドボックス環境にインスタンスをコピーしてサンドボックス環境を Dataverse と統合する場合は、ユーザー設定フィールドを Dataverse テーブルに再適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba06a-116">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span> <span data-ttu-id="ba06a-117">[カスタムフィールドを Dataverse に適用する](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="ba06a-117">See [Apply custom fields to Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="ba06a-118">Human Resources データベースのコピーによる影響</span><span class="sxs-lookup"><span data-stu-id="ba06a-118">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="ba06a-119">Human Resources データベースのコピーをする際に、次のイベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="ba06a-119">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="ba06a-120">コピーの過程で、対象とする環境の既存のデータベースが削除されます。</span><span class="sxs-lookup"><span data-stu-id="ba06a-120">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="ba06a-121">コピーの完了後は、既存のデータベースを復元することはできません。</span><span class="sxs-lookup"><span data-stu-id="ba06a-121">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="ba06a-122">対象とする環境は、コピーが完了するまで使用することができません。</span><span class="sxs-lookup"><span data-stu-id="ba06a-122">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="ba06a-123">Microsoft Azure Blob storage 内のドキュメントは環境間でのコピーがされません。</span><span class="sxs-lookup"><span data-stu-id="ba06a-123">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="ba06a-124">そのため、この ストレージ に属するドキュメントやテンプレートはコピーされず、コピー元の環境に残ります。</span><span class="sxs-lookup"><span data-stu-id="ba06a-124">As a result, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="ba06a-125">管理者ユーザー、およびその他の内部サービス ユーザー アカウントを除くすべてのユーザーは使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="ba06a-125">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="ba06a-126">管理者ユーザーは他のユーザーがシステムに復帰する前にデータの削除や難読化することができます。</span><span class="sxs-lookup"><span data-stu-id="ba06a-126">The Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="ba06a-127">管理者ユーザーは、特定のサービスまたは URL に統合エンドポイントを再接続するなど、必要な構成の変更を加える必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba06a-127">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="ba06a-128">Human Resources データベースのコピー</span><span class="sxs-lookup"><span data-stu-id="ba06a-128">Copy the Human Resources database</span></span>

<span data-ttu-id="ba06a-129">このタスクを完了するには、最初にインスタンスをコピーして、続いて Microsoft Power Platform 管理センターを Power Apps 環境へとコピーします。</span><span class="sxs-lookup"><span data-stu-id="ba06a-129">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your Power Apps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="ba06a-130">インスタンスのコピーを行うと、対象となるインスタンスのデータベースが削除されます。</span><span class="sxs-lookup"><span data-stu-id="ba06a-130">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="ba06a-131">対象のインスタンスをこの処理中に使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="ba06a-131">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="ba06a-132">LCS にサインインし、コピーをするインスタンスを含む LCS プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="ba06a-132">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="ba06a-133">LCS プロジェクトでは、**人事管理アプリの管理** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="ba06a-133">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="ba06a-134">コピーをするインスタンスを選択して、**コピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ba06a-134">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="ba06a-135">**インスタンスをコピーする** のタスク ウィンドウで、上書きするインスタンスを選択し、続いて **コピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ba06a-135">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="ba06a-136">**コピーのステータス** フィールドの値が **完了** となるまで待機してください。</span><span class="sxs-lookup"><span data-stu-id="ba06a-136">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="ba06a-137">上書きするインスタンスを選択します</span><span class="sxs-lookup"><span data-stu-id="ba06a-137">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="ba06a-138">**Power Platform** を選択し、 Microsoft Power Platform 管理センターにサインインします。</span><span class="sxs-lookup"><span data-stu-id="ba06a-138">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="ba06a-139">Power Platformを選択します</span><span class="sxs-lookup"><span data-stu-id="ba06a-139">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="ba06a-140">コピーをするPower Apps 環境 を選択して、 **コピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ba06a-140">Select the Power Apps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="ba06a-141">コピー処理の完了後、対象のインスタンスにサインインし、 Dataverse 統合を有効化します。</span><span class="sxs-lookup"><span data-stu-id="ba06a-141">When the copy process is completed, sign in to the target instance, and enable Dataverse integration.</span></span> <span data-ttu-id="ba06a-142">詳細情報と解説については、 [Dataverse の統合を構成する](./hr-admin-integration-common-data-service.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba06a-142">For more information and instructions, see [Configure Dataverse integration](./hr-admin-integration-common-data-service.md).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="ba06a-143">データの属性と状態</span><span class="sxs-lookup"><span data-stu-id="ba06a-143">Data elements and statuses</span></span>

<span data-ttu-id="ba06a-144">次のデータ要素は、Human Resources インスタンスのコピーを行う際にコピーされません。</span><span class="sxs-lookup"><span data-stu-id="ba06a-144">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="ba06a-145">**LogisticsElectronicAddress** テーブルの電子メールアドレス</span><span class="sxs-lookup"><span data-stu-id="ba06a-145">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="ba06a-146">**BatchJobHistory**、 **BatchHistory**、 **BatchConstraintHistory** テーブル内のバッチジョブ履歴</span><span class="sxs-lookup"><span data-stu-id="ba06a-146">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="ba06a-147">**SysEmailSMTPPassword** テーブル内の Simple Mail Transfer Protocol (シンプル メール トランスファー プロトコル、SMTP) のパスワード</span><span class="sxs-lookup"><span data-stu-id="ba06a-147">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="ba06a-148">**SysEmailParameters** テーブル内の SMTP リレーサーバー</span><span class="sxs-lookup"><span data-stu-id="ba06a-148">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="ba06a-149">**PrintMgmtSettings** と **PrintMgmtDocInstance** テーブル内 の 印刷管理設定</span><span class="sxs-lookup"><span data-stu-id="ba06a-149">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="ba06a-150">**SysServerConfig**、 **SysServerSessions**、 **SysCorpNetPrinters**、 **SysClientSessions**、 **BatchServerConfig**、 **BatchServerGroup** テーブル内の環境固有のレコード</span><span class="sxs-lookup"><span data-stu-id="ba06a-150">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="ba06a-151">DocuValue テーブル内のドキュメント添付ファイル。</span><span class="sxs-lookup"><span data-stu-id="ba06a-151">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="ba06a-152">コピー元の環境で上書きされた Microsoft Office のテンプレートを含む要素</span><span class="sxs-lookup"><span data-stu-id="ba06a-152">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="ba06a-153">**PersonnelIntegrationConfiguration** テーブル内の接続文字列</span><span class="sxs-lookup"><span data-stu-id="ba06a-153">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="ba06a-154">これらの要素は、環境固有のものであるためコピーされません。</span><span class="sxs-lookup"><span data-stu-id="ba06a-154">Some of these elements aren't copied because they're environment-specific.</span></span> <span data-ttu-id="ba06a-155">**BatchServerConfig** と **SysCorpNetPrinters** のレコードを含む例。</span><span class="sxs-lookup"><span data-stu-id="ba06a-155">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="ba06a-156">その他の要素は、サポート チケットのデータ量が多くなる懸念があるためコピーされません。</span><span class="sxs-lookup"><span data-stu-id="ba06a-156">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="ba06a-157">例:</span><span class="sxs-lookup"><span data-stu-id="ba06a-157">For example:</span></span>

- <span data-ttu-id="ba06a-158">重複した電子メールは、SMTP がユーザー受け入れテスト (サンドボックス) 環境で有効になっている場合に送信される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ba06a-158">Duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment.</span></span>

- <span data-ttu-id="ba06a-159">バッチジョブが有効な場合、無効な統合メッセージが送信される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ba06a-159">Invalid integration messages might be sent because batch jobs are still enabled.</span></span>

- <span data-ttu-id="ba06a-160">管理者が更新後のクリーンアップ アクションを実行する前に、ユーザーが有効化される場合があります。</span><span class="sxs-lookup"><span data-stu-id="ba06a-160">Users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="ba06a-161">また、インスタンスのコピー時には、次の状態変更がされます :</span><span class="sxs-lookup"><span data-stu-id="ba06a-161">Also, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="ba06a-162">管理者以外の全ユーザーが **無効化** されます。</span><span class="sxs-lookup"><span data-stu-id="ba06a-162">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="ba06a-163">一部のシステムジョブを除いた、すべてのバッチジョブが **保留** となります。</span><span class="sxs-lookup"><span data-stu-id="ba06a-163">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="ba06a-164">環境管理者</span><span class="sxs-lookup"><span data-stu-id="ba06a-164">Environment admin</span></span>

<span data-ttu-id="ba06a-165">対象となるサンドボックス環境の、管理者を含む全ユーザーが、コピー元のユーザーに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="ba06a-165">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="ba06a-166">インスタンスのコピーの実行者は、自分にソース環境で管理者の権限があることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ba06a-166">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="ba06a-167">管理者の権限がない場合は、コピーの完了後に対象のサンドボックス環境にサイン インすることができません。</span><span class="sxs-lookup"><span data-stu-id="ba06a-167">If you aren't, you can't sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="ba06a-168">コピー先のサンドボックス環境内の全ての非管理者ユーザーは無効化され、サンドボックス環境へと不必要なログインができません。</span><span class="sxs-lookup"><span data-stu-id="ba06a-168">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="ba06a-169">システム管理者は、必要に応じてユーザーを有効化することができます。</span><span class="sxs-lookup"><span data-stu-id="ba06a-169">Administrators can reenable users if needed.</span></span>

## <a name="apply-custom-fields-to-dataverse"></a><span data-ttu-id="ba06a-170">カスタム フィールドを Dataverse に適用する</span><span class="sxs-lookup"><span data-stu-id="ba06a-170">Apply custom fields to Dataverse</span></span>

<span data-ttu-id="ba06a-171">サンドボックス環境にインスタンスをコピーしてサンドボックス環境を Dataverse と統合する場合は、ユーザー設定フィールドを Dataverse テーブルに再適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba06a-171">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span>

<span data-ttu-id="ba06a-172">Dataverse テーブルに表示されるユーザー設定フィールドごとに、次の手順を実行します :</span><span class="sxs-lookup"><span data-stu-id="ba06a-172">For each custom field that's exposed on Dataverse tables, do the following steps:</span></span>

1. <span data-ttu-id="ba06a-173">カスタム設定フィールドに移動して、**編集** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="ba06a-173">Go to the custom field and select **Edit**.</span></span>

2. <span data-ttu-id="ba06a-174">ユーザー設定フィールドが有効になっている各 "cdm_\* エンティティ" の **有効** フィールドをオフにします。</span><span class="sxs-lookup"><span data-stu-id="ba06a-174">Unselect the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

3. <span data-ttu-id="ba06a-175">**変更を適用する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ba06a-175">Select **Apply Changes**.</span></span>

4. <span data-ttu-id="ba06a-176">再度 **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ba06a-176">Select **Edit** again.</span></span>

5. <span data-ttu-id="ba06a-177">ユーザー設定フィールドが有効になっている各 "cdm_\* エンティティ" の **有効** フィールドをオンにします。</span><span class="sxs-lookup"><span data-stu-id="ba06a-177">Select the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

6. <span data-ttu-id="ba06a-178">再度 **変更を適用する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ba06a-178">Select **Apply Changes** again.</span></span>

<span data-ttu-id="ba06a-179">選択解除、変更の適用、再選択、変更の再適用を行うプロセスでは、カスタム フィールドを含むように Dataverse でスキーマを更新するように促されます。</span><span class="sxs-lookup"><span data-stu-id="ba06a-179">The process of unselecting, applying changes, reselecting, and reapplying changes prompts the schema to update in Dataverse to include the custom fields.</span></span>

<span data-ttu-id="ba06a-180">カスタム フィールドについての詳細については、[カスタム フィールドの作成と操作](../fin-ops-core/fin-ops/get-started/user-defined-fields.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba06a-180">For more information about custom fields, see [Create and work with custom fields](../fin-ops-core/fin-ops/get-started/user-defined-fields.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ba06a-181">参照</span><span class="sxs-lookup"><span data-stu-id="ba06a-181">See also</span></span>

[<span data-ttu-id="ba06a-182">Human Resources のプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="ba06a-182">Provision Human Resources</span></span>](hr-admin-setup-provision.md)</br>
[<span data-ttu-id="ba06a-183">インスタンスの削除</span><span class="sxs-lookup"><span data-stu-id="ba06a-183">Remove an instance</span></span>](hr-admin-setup-remove-instance.md)</br>
[<span data-ttu-id="ba06a-184">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="ba06a-184">Update process</span></span>](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]