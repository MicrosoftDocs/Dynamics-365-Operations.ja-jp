---
title: ER テンプレートのバックアップストレージ
description: このトピックでは、テンプレートの復旧に電子申告 (ER) バックアップストレージを使用する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-13
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2e399290153c2c63ac1c02f0f9cdb956ff5031e5
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321669"
---
# <a name="backup-storage-of-er-templates"></a><span data-ttu-id="89232-103">ER テンプレートのバックアップストレージ</span><span class="sxs-lookup"><span data-stu-id="89232-103">Backup storage of ER templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89232-104">[電子申告 (ER) の概要](general-electronic-reporting.md) を使用して、ビジネス ユーザーはさまざまな国/地域の法的要件に従って発信ドキュメントの形式を構成できます。</span><span class="sxs-lookup"><span data-stu-id="89232-104">The [Electronic reporting (ER) overview](general-electronic-reporting.md) lets business users configure formats for outbound documents according to the legal requirements of various countries and regions.</span></span> <span data-ttu-id="89232-105">構成された ER 形式では、定義済みのテンプレートを使用して Microsoft Excel、workbooks、Microsoft Word ドキュメント、PDF ドキュメントなど、さまざまな形式で送信ドキュメントを生成できます。</span><span class="sxs-lookup"><span data-stu-id="89232-105">Configured ER formats can use predefined templates to generate outbound documents in various formats, such as Microsoft Excel workbooks, Microsoft Word documents, or PDF documents.</span></span> <span data-ttu-id="89232-106">テンプレートには、生成されたドキュメントに対して構成されたデータフローに必要なデータが入力されます。</span><span class="sxs-lookup"><span data-stu-id="89232-106">The templates are filled with data that the configured dataflow for generated documents requires.</span></span>

<span data-ttu-id="89232-107">ER ソリューションの一部として、構成された各形式を公開できます。</span><span class="sxs-lookup"><span data-stu-id="89232-107">Each configured format can be published as part of an ER solution.</span></span> <span data-ttu-id="89232-108">各 ER ソリューションは、Finance and Operations の 1 つのインスタンスからエクスポートして、別のインスタンスにインポートできます。</span><span class="sxs-lookup"><span data-stu-id="89232-108">Each ER solution can be exported from one instance of Finance and Operations and imported into another instance.</span></span>

<span data-ttu-id="89232-109">ER フレームワークでは、[ドキュメント管理の構成](../../fin-ops/organization-administration/configure-document-management.md) を使用して、現在の Finance and Operations インスタンスに必要なテンプレートを保持します。</span><span class="sxs-lookup"><span data-stu-id="89232-109">The ER framework uses the [Configure document management](../../fin-ops/organization-administration/configure-document-management.md) to keep the required templates for the current Finance and Operations instance.</span></span> <span data-ttu-id="89232-110">ER フレームワークの設定に応じて、Microsoft Azure Blob ストレージまたは Microsoft SharePoint フォルダをテンプレートの物理的なプライマリ ストレージの場所として選択できます。</span><span class="sxs-lookup"><span data-stu-id="89232-110">Depending on the settings of the ER framework, Microsoft Azure Blob storage or a Microsoft SharePoint folder can be selected as the physical primary storage location for templates.</span></span> <span data-ttu-id="89232-111">(詳細については、[電子申告 (ER) フレームワークの構成](electronic-reporting-er-configure-parameters.md) を参照してください。) DocuValue テーブルには、各テンプレートの個々のレコードが保持されます。</span><span class="sxs-lookup"><span data-stu-id="89232-111">(For more information, see [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md).) The DocuValue table holds an individual record for each template.</span></span> <span data-ttu-id="89232-112">各レコードの **AccessInformation** フィールドには、構成されている保管場所にあるテンプレートファイルのパスが格納されます。</span><span class="sxs-lookup"><span data-stu-id="89232-112">In each record, the **AccessInformation** field stores the path of a template file that is located in the configured storage location.</span></span>

<span data-ttu-id="89232-113">Finance and Operations インスタンスを管理する場合、現在のインスタンスを別の場所に移行する必要性が発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="89232-113">When you manage your Finance and Operations instances, you might decide to migrate the current instance to another location.</span></span> <span data-ttu-id="89232-114">たとえば、本番インスタンスを新しいサンドボックス環境に移行するかもしれません。</span><span class="sxs-lookup"><span data-stu-id="89232-114">For example, you might migrate your production instance to a new sandbox environment.</span></span> <span data-ttu-id="89232-115">テンプレートを Blob ストレージに保存するように ER フレームワークを構成した場合、新しいサンドボックス環境の DocuValue テーブルは、本番環境の Blob ストレージのインスタンスを参照します。</span><span class="sxs-lookup"><span data-stu-id="89232-115">If you configured the ER framework to store templates in Blob storage, the DocuValue table in the new sandbox environment refers to the instance of Blob storage in the production environment.</span></span> <span data-ttu-id="89232-116">ただし、移行プロセスでは、Blob ストレージ内のアーティファクトの移行をサポートしていないため、このインスタンスにサンドボックス環境からアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="89232-116">However, this instance can't be accessed from the sandbox environment, because the migration process doesn't support the migration of artifacts in Blob storage.</span></span> <span data-ttu-id="89232-117">したがって、テンプレートを使用して ER 形式を実行してビジネスドキュメントを生成すると、例外が発生し、テンプレートが欠落していることについて通知されます。</span><span class="sxs-lookup"><span data-stu-id="89232-117">Therefore, if you try to run an ER format that uses a template to generate business documents, an exception occurs, and you're notified about the missing template.</span></span> <span data-ttu-id="89232-118">また、ER クリーンアップ ツールを使用して、テンプレートを含む ER 形式の構成を削除してから再インポートする方法も紹介しています。</span><span class="sxs-lookup"><span data-stu-id="89232-118">You're also guided to use the ER cleanup tool to delete and then re-import the ER format configuration that contains the template.</span></span> <span data-ttu-id="89232-119">ER 形式の構成が複数存在する場合があるため、このプロセスには時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="89232-119">Because you might have several ER format configurations, this process can be time consuming.</span></span>

<span data-ttu-id="89232-120">ER テンプレート機能のバックアップ ストレージを使用すると、テンプレートを使用して、常にビジネス ドキュメントを生成するためのテンプレートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="89232-120">The Backup storage of ER templates feature can help you make your templates so that they are always available to generate business documents.</span></span>

> [!NOTE]
> <span data-ttu-id="89232-121">この機能は、ER テンプレートの物理的な保管場所として Blob ストレージが選択されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="89232-121">This feature can be used only when Blob storage has been selected as the physical storage location for ER templates.</span></span>

## <a name="automated-recovery-and-notification"></a><span data-ttu-id="89232-122">自動回復と通知</span><span class="sxs-lookup"><span data-stu-id="89232-122">Automated recovery and notification</span></span>

<span data-ttu-id="89232-123">この機能では、次のイベントが発生すると、現在の環境の新しい ER 形式の構成のすべてのテンプレートが、テンプレートのバックアップ保存場所 (ERDocuDatabaseStorage データベース テーブル) に自動的に保存されます。</span><span class="sxs-lookup"><span data-stu-id="89232-123">For this feature, every template of a new ER format configuration in the current environment is automatically saved to the backup storage location for templates (the ERDocuDatabaseStorage database table) when the following events occur:</span></span>

- <span data-ttu-id="89232-124">テンプレートを含む新しい ER 形式構成をインポートします。</span><span class="sxs-lookup"><span data-stu-id="89232-124">You import a new ER format configuration that contains a template.</span></span>
- <span data-ttu-id="89232-125">テンプレートを含む ER 形式構成の下書きバージョンを完了します。</span><span class="sxs-lookup"><span data-stu-id="89232-125">You complete the draft version of an ER format configuration that contains a template.</span></span>

<span data-ttu-id="89232-126">テンプレートのバックアップ コピーは、アプリケーション データベースの一部として Finance and Operations の新しいインスタンスに移行されます。</span><span class="sxs-lookup"><span data-stu-id="89232-126">Backup copies of templates are migrated to a new instance of Finance and Operations as part of the application database.</span></span>

<span data-ttu-id="89232-127">たとえば、支払通知やコントロール レポートを生成する場合など、発信ドキュメントの生成に ER 形式のテンプレートが必要だが、基本の保管場所に必要なテンプレートが見つからない場合は、次のイベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="89232-127">If a template of an ER format is required for generation of outbound documents, to process vendor payments including generation of payment advice and control reports, for example, but the required template isn't found in the primary storage location, the following events occur:</span></span>

- <span data-ttu-id="89232-128">バックアップの保存場所でテンプレートが使用できる場合は、自動的にバックアップの保存場所から取得され、主な保管場所に復元され、現在の実行に使用されます。</span><span class="sxs-lookup"><span data-stu-id="89232-128">If the template is available in the backup storage location, it is automatically taken from the backup storage location, restored to the primary storage location, and used for the current execution.</span></span>
- <span data-ttu-id="89232-129">**電子申告開発者**または**システム管理者**のロールに割り当てられているすべてのユーザーには、アクション センターによって不足しているテンプレートの問題が通知されます。</span><span class="sxs-lookup"><span data-stu-id="89232-129">Every user who is assigned to the **Electronic reporting developer** or **System administrator** role is notified about the missing template issue through the Action center.</span></span> <span data-ttu-id="89232-130">表示されるメッセージは、**破損したテンプレートをバッチで復元する手順を自動的に実行する**パラメーターの値によって異なります。</span><span class="sxs-lookup"><span data-stu-id="89232-130">The message that appears depends on the value of the **Automatically run the procedure of restoring the broken templates in batch** parameter:</span></span>

    - <span data-ttu-id="89232-131">このパラメーターが **Off** に設定されている場合、メッセージはバッチ処理を開始して、他の ER 形式の構成テンプレートの類似した問題を自動的に修正することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="89232-131">If this parameter is set to **Off**, the message recommends that you start the batch process to automatically fix similar issues for other ER format configuration templates.</span></span> <span data-ttu-id="89232-132">このメッセージには、バッチ処理を開始するために使用できるリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="89232-132">The message includes a link that you can use to start the batch process.</span></span>
    - <span data-ttu-id="89232-133">このパラメーターを **On** に設定すると、不足しているテンプレートの問題が検出されたことと、新しいバッチ処理、**破損したテンプレートの内部データベースバックアップからの復元**が自動的にスケジュールされたことを知らせるメッセージが通知されます。</span><span class="sxs-lookup"><span data-stu-id="89232-133">If this parameter is set to **On**, the message notifies you that a missing templates issue has been discovered, and that a new batch process, **Restore broken templates from internal database backup**, has been automatically scheduled.</span></span> <span data-ttu-id="89232-134">このバッチ処理によって、他のテンプレートの同様の問題が自動的に修正されます。</span><span class="sxs-lookup"><span data-stu-id="89232-134">This batch process will automatically fix similar issues for other templates.</span></span>

<span data-ttu-id="89232-135">**破損したテンプレートをバッチで復元する手順を自動的に実行する**パラメーターを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="89232-135">To set up the he **Automatically run the procedure of restoring the broken templates in batch** parameter, complete the following steps:</span></span>

1. <span data-ttu-id="89232-136">Finance and Operations で、 **組織管理  \> 電子申告 \> 構成ページ** を開きます。</span><span class="sxs-lookup"><span data-stu-id="89232-136">In Finance and Operations, open the **Organization administration \> Electronic reporting \> Configurations page**.</span></span>
2. <span data-ttu-id="89232-137">**構成**ページ、アクション ウィンドウ、**構成**タブ、**詳細設定**グループで、**ユーザー パラメーター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="89232-137">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="89232-138">**ユーザー パラメーター** ダイアログ ボックスで、**破損したテンプレートをバッチで復元する手順を自動的に実行する**パラメーターに必要な値を設定します。</span><span class="sxs-lookup"><span data-stu-id="89232-138">In the **User parameters** dialog box, set the required value for the **Automatically run the procedure of restoring the broken templates in batch** parameter.</span></span>

> [!NOTE]
> <span data-ttu-id="89232-139">このパラメーターは、アプリケーションユーザーとして定義され、会社に固有のログに記録されます。</span><span class="sxs-lookup"><span data-stu-id="89232-139">This parameter is defined as application user and logged company specific.</span></span>

![ER コンフィギュレーション ページ](./media/GER-BackupTemplates-1.png)

<span data-ttu-id="89232-141">次の図は、**破損したテンプレートをバッチで復元する手順を自動的に実行する**パラメーターが **On** に設定されている場合に表示されるメッセージの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="89232-141">The following illustration shows an example of the message that appears when the **Automatically run the procedure of restoring the broken templates in batch** parameter is set to **On**.</span></span>

![仕入先支払仕訳帳明細ページ](./media/GER-BackupTemplates-2.png)

<span data-ttu-id="89232-143">次の図は、**バッチ ジョブ** ページの**破損したテンプレートの内部データベース バックアップからの復元**バッチ処理を示しています。</span><span class="sxs-lookup"><span data-stu-id="89232-143">The following illustration shows the **Restore broken templates from internal database backup** batch process on the **Batch job** page.</span></span>

![バッチ ジョブのページ](./media/GER-BackupTemplates-3.png)

<span data-ttu-id="89232-145">完了した**破損したテンプレートの内部データベース バックアップからの復元**バッチ処理の実行ログには、バックアップの保存場所からプライマリ ストレージの場所に復元されたテンプレートに関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="89232-145">The execution log of the completed **Restore broken templates from internal database backup** batch process includes information about the templates that have been restored from the backup storage location to the primary storage location.</span></span>

![バッチ ジョブ履歴ページ](./media/GER-BackupTemplates-4.png)

<span data-ttu-id="89232-147">既定では、ER 形式の構成に存在するテンプレートのバックアップ コピーを自動的に作成するプロセスが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="89232-147">By default, the process of automatically creating backup copies of templates that reside in ER format configurations is turned on.</span></span> <span data-ttu-id="89232-148">テンプレートのバックアップ コピーを停止するには、**電子申告のパラメーター** ページの**添付**タブで、**テンプレートのバックアップ コピーの作成を停止する**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="89232-148">To stop making backup copies of templates, set the **Stop making backup copies of template** option to **Yes** on the **Attachments** tab of the **Electronic reporting parameters** page.</span></span> <span data-ttu-id="89232-149">**電子申告**ワークスペースから、このページを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="89232-149">You can open this page from the **Electronic reporting** workspace.</span></span>

<span data-ttu-id="89232-150">**テンプレートのバックアップ コピーの作成を停止する**オプションを**はい**に設定したが、以前にテンプレートで作成したバックアップ コピーを保持しないように設定する場合は、**電子申告のパラメーター** ページで**バックアップ ストレージのクリーンアップ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="89232-150">If you set the **Stop making backup copies of templates** option to **Yes** and don't want to keep the backup copies that were previously made of templates, select **Clean up backup storage** on the **Electronic reporting parameters** page.</span></span>

<span data-ttu-id="89232-151">環境を Finance and Operations  バージョン 10.0.5 (2019 年 10 月) にアップグレードして、実行可能な ER 形式の構成を含む新しい環境に移行する場合は、移行をする前に **電子申告のパラメーター** ページで **バックアップ ストレージに入力する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89232-151">If you upgraded your environment to Finance and Operations version 10.0.5 (October 2019) and want to migrate to a new environment that includes ER format configurations that can be run, select **Fill in backup storage** on the **Electronic reporting parameters** page before the migration occurs.</span></span> <span data-ttu-id="89232-152">このボタンをクリックすると、使用可能なすべてのテンプレートのバックアップ コピーを作成するプロセスが開始され、テンプレートの ER バックアップ保存場所に保存できるようになります。</span><span class="sxs-lookup"><span data-stu-id="89232-152">This button starts the process of making backup copies of all available templates, so that they can be stored in the ER backup storage location for templates.</span></span>

![電子申告のパラメーター ページ](./media/GER-BackupTemplates-5.png)

## <a name="manual-recovery"></a><span data-ttu-id="89232-154">手動による回復</span><span class="sxs-lookup"><span data-stu-id="89232-154">Manual recovery</span></span>

<span data-ttu-id="89232-155">**組織管理** \> **電子レポート** \> **破損したテンプレートの復元** に移動し、バックアップ ストレージの場所からプライマリ ストレージの場所に ER のテンプレートを復元するプロセスを手動で開始します。</span><span class="sxs-lookup"><span data-stu-id="89232-155">Go to **Organization administration** \> **Electronic reporting** \> **Restore broken templates** to manually initiate the process of restoring ER templates from the backup storage location to the primary storage location.</span></span> <span data-ttu-id="89232-156">このプロセスを開始する前に、**破損したテンプレートの復元** ページで同プロセスを対話的に実行するか、バッチプロセスをスケジュールするかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="89232-156">Before you start this process, on the **Restore broken templates** page you can specify whether it will be performed interactively, or the batch process will be scheduled for this.</span></span>

## <a name="supported-deployments"></a><span data-ttu-id="89232-157">サポートされている配置</span><span class="sxs-lookup"><span data-stu-id="89232-157">Supported deployments</span></span>

<span data-ttu-id="89232-158">Finance and Operations バージョン 10.0.5 では、ER テンプレートのバックアップ保存機能はクラウド配置でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="89232-158">In Finance and Operations version 10.0.5, the Backup storage of ER templates feature is available only in cloud deployments.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="89232-159">追加リソース</span><span class="sxs-lookup"><span data-stu-id="89232-159">Additional resources</span></span>

[<span data-ttu-id="89232-160">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="89232-160">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="89232-161">電子申告 (ER) フレームワークの構成</span><span class="sxs-lookup"><span data-stu-id="89232-161">Configure the Electronic reporting (ER) framework</span></span>](electronic-reporting-er-configure-parameters.md)
