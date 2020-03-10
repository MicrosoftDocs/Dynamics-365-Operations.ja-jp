---
title: 拡張機能を介したカスタム Commerce Data Exchange 同期の有効化
description: このトピックでは、コマース 初期化クラスを拡張して、カスタムの Commerce Data Exchange (CDX) 同期をサポートする方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 09/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-09-15
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.openlocfilehash: b465bce8482095104b22d9e88478c35ae9f3bc18
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070467"
---
# <a name="enable-custom-commerce-data-exchange-synchronization-via-extension"></a><span data-ttu-id="b5124-103">拡張機能を介したカスタム Commerce Data Exchange 同期の有効化</span><span class="sxs-lookup"><span data-stu-id="b5124-103">Enable custom Commerce Data Exchange synchronization via extension</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5124-104">このトピックでは、コマース 初期化クラスを拡張して、カスタムの Commerce Data Exchange (CDX) 同期をサポートする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b5124-104">This topic explains how you can extend the Commerce initialization class to support custom Commerce Data Exchange (CDX) synchronization.</span></span> <span data-ttu-id="b5124-105">この拡張機能では、Microsoft Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 8 または Microsoft Dynamics 365 Retail プラットフォーム更新プログラム 8 で追加された新しい拡張ポイントを使用します。</span><span class="sxs-lookup"><span data-stu-id="b5124-105">For this extension, you use the new extension points that were added in Microsoft Dynamics 365 for Finance and Operations platform update 8 or Microsoft Dynamics 365 Retail platform update 8.</span></span>

<span data-ttu-id="b5124-106">CDX は、コマース バックオフィス (HQ) と、オンライン ストアまたは従来型の店舗などのチャネルの間でデータを転送するシステムです。</span><span class="sxs-lookup"><span data-stu-id="b5124-106">CDX is a system that transfers data between Commerce Headquarters (HQ) and channels, such as online stores or brick-and-mortar stores.</span></span> <span data-ttu-id="b5124-107">HQ とチャネル データベース間のデータ転送は、スケジューラ ジョブによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="b5124-107">The data transfer between HQ and the channel database is controlled by scheduler jobs.</span></span> <span data-ttu-id="b5124-108">各スケジューラ ジョブには、スケジューラ サブジョブの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b5124-108">Each scheduler job contains a list of scheduler subjobs.</span></span> <span data-ttu-id="b5124-109">スケジューラ サブジョブには、ソース テーブルと出力先テーブルの名前と、それらのテーブルの転送フィールド マッピングが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b5124-109">The scheduler subjobs contain the names of the source tables and destination tables, and the transfer field mapping of those tables.</span></span> <span data-ttu-id="b5124-110">HQ とチャネル データベース間のデータ同期をコンフィグレーションするには、2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="b5124-110">There are two ways to configure the data synchronization between HQ and the channel database:</span></span>

+ <span data-ttu-id="b5124-111">CDX のコンフィギュレーション ユーザー インターフェイス (UI) を使用して、すべてのカスタム ジョブとサブジョブをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="b5124-111">Configure all the custom jobs and subjobs by using the configuration user interface (UI) for CDX.</span></span>
+ <span data-ttu-id="b5124-112">プッシュおよびプルの両方のカスタム ジョブとサブジョブをサポートするために用意されている拡張ポイントを使用して、コマース初期化クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="b5124-112">Extend the Commerce initialization class by using the extension points that are provided to support custom jobs and subjobs for both push and pull.</span></span>

<span data-ttu-id="b5124-113">コマース初期化クラスを使用する利点は、さまざまな環境 (開発、テスト、および実稼働) でカスタム ジョブを構成する必要がないことです。</span><span class="sxs-lookup"><span data-stu-id="b5124-113">The advantage of using the Commerce initialization class is that you don't have to configure the custom jobs in different environments (dev, test, and production).</span></span> <span data-ttu-id="b5124-114">代わりに、**Retail と Commerce > バックオフィスの設定 > コマース スケジューラ > コマース スケジューラの初期化**から**コマース スケジューラの初期化**ダイアログ ボックスを使用して、CDX 初期化を実行できます。</span><span class="sxs-lookup"><span data-stu-id="b5124-114">Instead, you can run the CDX initialization by using the **Initialize commerce scheduler** dialog box from **Retail and Commerce > Headquarters setup > Commerce scheduler > Initialize commerce scheduler**.</span></span> <span data-ttu-id="b5124-115">データの同期のためのカスタム ジョブに関する情報は CDX で自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="b5124-115">Information about the custom job for the data synchronization is then automatically created in CDX.</span></span>

<span data-ttu-id="b5124-116">HQ とチャネル データベース間のデータ転送には、さまざまなシナリオがあります。</span><span class="sxs-lookup"><span data-stu-id="b5124-116">There are various scenarios for data transfer between HQ and the channel database:</span></span>

+ <span data-ttu-id="b5124-117">ダウンロード ジョブを使用して新しい HQ テーブルから新しいチャンネル データベース テーブルにデータを送信します。</span><span class="sxs-lookup"><span data-stu-id="b5124-117">Send data from a new HQ table to a new channel database table by using a download job.</span></span>
+ <span data-ttu-id="b5124-118">プッシュ ジョブを使用して新しい HQ テーブルに新しいチャンネル データベース テーブルからのデータを取り込みます。</span><span class="sxs-lookup"><span data-stu-id="b5124-118">Pull data from a new channel database table to a new HQ table by using a push job.</span></span>

## <a name="send-data-from-a-new-hq-table-to-a-new-channel-database-table-by-using-a-download-job"></a><span data-ttu-id="b5124-119">ダウンロード ジョブを使用して新しい HQ テーブルから新しいチャンネル データベース テーブルにデータを送信</span><span class="sxs-lookup"><span data-stu-id="b5124-119">Send data from a new HQ table to a new channel database table by using a download job</span></span>

<span data-ttu-id="b5124-120">データをプッシュまたはプルする前に、XML リソース ファイルのさまざまなメタデータ定義を理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5124-120">Before you push or pull data, you must understand various metadata definitions in the XML resource file.</span></span> <span data-ttu-id="b5124-121">リソース ファイルには、データのプッシュやプルを実行する環境で初期化されるカスタム ジョブ情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b5124-121">The resource file contains the custom job information that will be initialized in your environment to push and pull data.</span></span> <span data-ttu-id="b5124-122">コンフィギュレーションする必要があるリソース ファイルの一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b5124-122">Here is a list of the resource files that you must configure:</span></span>

+ <span data-ttu-id="b5124-123">**ChannelDBSchema** - チャンネル データベースで作成した拡張スキーマです。</span><span class="sxs-lookup"><span data-stu-id="b5124-123">**ChannelDBSchema** – The extension schema that you created in the channel database.</span></span>
+ <span data-ttu-id="b5124-124">**TargetTableSchema** – カスタム テーブルを追加するチャンネル データベースで作成した拡張スキーマ。</span><span class="sxs-lookup"><span data-stu-id="b5124-124">**TargetTableSchema** – The extension schema that you created in the channel database to add your custom tables.</span></span>
+ <span data-ttu-id="b5124-125">**AxTableName** - テーブル名。</span><span class="sxs-lookup"><span data-stu-id="b5124-125">**AxTableName** – The table name.</span></span>
+ <span data-ttu-id="b5124-126">**IsUpload** – ジョブがプッシュ ジョブかプル ジョブかを判断するフラグ。</span><span class="sxs-lookup"><span data-stu-id="b5124-126">**IsUpload** – A flag that determines whether the job is a push job or a pull job.</span></span> <span data-ttu-id="b5124-127">(つまり、フラグは、HQ からチャンネル データベースにデータを送信するか、チャンネル データベースから HQ にデータをプルするかを示します)。</span><span class="sxs-lookup"><span data-stu-id="b5124-127">(In other words, the flag indicates whether you want to send data from HQ to the channel database or pull data from the channel database to HQ).</span></span> <span data-ttu-id="b5124-128">既定値は **false** で、HQ からチャネル データベースにデータを送信していることを示します。</span><span class="sxs-lookup"><span data-stu-id="b5124-128">The default value is **false**, which indicates that you're sending data from HQ to the channel database.</span></span>
+ <span data-ttu-id="b5124-129">**ScheduledByJob** – このリソース ファイルには、1 つ以上のサブジョブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b5124-129">**ScheduledByJob** – This resource file contains one or more subjobs.</span></span>
+ <span data-ttu-id="b5124-130">**サブジョブ** – 各テーブルは、サブジョブとして追加され、各サブジョブは 1 つまたは複数のスケジューラ ジョブによってスケジュールされています。</span><span class="sxs-lookup"><span data-stu-id="b5124-130">**Subjob** – Each table is added as a subjob, and each subjob is scheduled by one or more scheduler jobs.</span></span>
+ <span data-ttu-id="b5124-131">**TargetTable** – チャンネル データベース テーブルの名前です。</span><span class="sxs-lookup"><span data-stu-id="b5124-131">**TargetTable** – The name of the channel database table.</span></span> <span data-ttu-id="b5124-132">このテーブルは、プッシュ ジョブまたはプル ジョブのデータの送り先となるターゲット テーブルです。</span><span class="sxs-lookup"><span data-stu-id="b5124-132">This table is the target table that the push job or pull job must send data to.</span></span> <span data-ttu-id="b5124-133">値が指定されていない場合、ターゲット テーブルの名前とソース テーブルの名前が同じになります。</span><span class="sxs-lookup"><span data-stu-id="b5124-133">If a value isn't specified, the system assumes that name of the target table and the name of the source table are the same.</span></span>

<span data-ttu-id="b5124-134">新しい HQ テーブルと新しいチャンネル データベース テーブルを作成した場合は、2 つのテーブル間でデータをプッシュするためのこれらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b5124-134">If you created a new HQ table and a new channel database table, follow these steps to push the data between the two tables.</span></span>

1. <span data-ttu-id="b5124-135">カスタム プロジェクトを作成し、アプリケーション オブジェクト ツリー (AOT) を使用してカスタム テーブルを追加します。</span><span class="sxs-lookup"><span data-stu-id="b5124-135">Create a custom project and use the Application Object Tree (AOT) to add a custom table.</span></span>
2. <span data-ttu-id="b5124-136">すべてのカスタム ジョブ情報を追加する新しいリソース ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="b5124-136">Create a new resource file to add all custom job information.</span></span> <span data-ttu-id="b5124-137">リソース ファイルのテンプレートを次に示します。</span><span class="sxs-lookup"><span data-stu-id="b5124-137">Here is the template for the resource file.</span></span>

    ```csharp
    <RetailCdxSeedData ChannelDBMajorVersion="7" ChannelDBSchema="ext" Name="AX7">
        <Jobs>
        </jobs>
        <Subjobs>
            <Subjob Id="" TargetTableSchema="" TargetTableName="">
        </Subjobs>
     </RetailCdxSeedData>
    ```

3. <span data-ttu-id="b5124-138">AOT を使用して新しい XML リソースを作成します。</span><span class="sxs-lookup"><span data-stu-id="b5124-138">Use the AOT to create a new XML resource.</span></span> <span data-ttu-id="b5124-139">リソースの XML ファイルで、次の例に示すように新しいテーブルと新しいジョブの詳細を指定します。</span><span class="sxs-lookup"><span data-stu-id="b5124-139">In the XML file for the resource, specify the new table and new job details, as shown in the following example.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b5124-140">新規テーブルを既存のジョブの一部として追加するか、または新しいジョブを作成してからこのテーブルを追加するかのいずれかを実行できます。</span><span class="sxs-lookup"><span data-stu-id="b5124-140">You can either add the new table as part of the existing job, or create a new job and add this table.</span></span> <span data-ttu-id="b5124-141">この場合、ジョブ ID が **7000** で、カスタムのテーブルに **ContosoRetailSeatingArrangementData** と名前が付けられている場合、新しいジョブを作成しています。</span><span class="sxs-lookup"><span data-stu-id="b5124-141">In this case, we are creating a new job, where the job ID is **7000** and the custom table is named **ContosoRetailSeatingArrangementData**.</span></span>
    >
    > ```xml
    > <RetailCdxSeedData ChannelDBMajorVersion="7" ChannelDBSchema="ext" Name="AX7">
    >    <Jobs>
    >        <Job DescriptionLabelId="REX4520710" Description="Custom job" Id="7000"/>
    >    </Jobs>
    >    <Subjobs>
    >        <Subjob Id="ContosoRetailSeatingArrangementData" TargetTableSchema="ext" AxTableName="ContosoRetailSeatingArrangementData">
    >            <ScheduledByJobs>
    >                <ScheduledByJob>7000</ScheduledByJob>
    >            </ScheduledByJobs>
    >            <AxFields>
    >                <Field Name="seatNumber"/>
    >                <Field Name="capacity"/>
    >                <Field Name="channelRecId"/>
    >                <Field Name="RecId"/>
    >             </AxFields>
    >        </Subjob>
    >    </Subjobs>
    > </RetailCdxSeedData>
    > ```

    <span data-ttu-id="b5124-142">既定では、ターゲット テーブルの名前がここでは指定されていません。</span><span class="sxs-lookup"><span data-stu-id="b5124-142">By default, the name of the target table isn't specified here.</span></span> <span data-ttu-id="b5124-143">システムでは、チャネル側のターゲット テーブルの名前がコマース側のソース テーブルの名前 (**AXTableName**) と同じであることが前提です。</span><span class="sxs-lookup"><span data-stu-id="b5124-143">The system assumes the name of the target table on the channel side is the same as the name of the source table on the Commerce side (**AXTableName**).</span></span> <span data-ttu-id="b5124-144">ただし、チャンネル側のターゲット テーブルの名前は、時にソース テーブルの名前とは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b5124-144">However, the name of the target table on the channel side might sometimes differ from the name of the source table.</span></span> <span data-ttu-id="b5124-145">この場合、**&lt;サブジョブ&gt;** ノードで **&lt;TargetTableName&gt;** 属性を使用してチャネル側でターゲット テーブルの名前を設定できます。</span><span class="sxs-lookup"><span data-stu-id="b5124-145">In this case, in the **&lt;Subjob&gt;** node, you can use the **&lt;TargetTableName&gt;** attribute to set the name of the target table on the channel side.</span></span>

    <span data-ttu-id="b5124-146">同様に、マッピング セクションでは、コマース側にあるフィールドの名前だけが指定されています (**AxFields**)。</span><span class="sxs-lookup"><span data-stu-id="b5124-146">Similarly, in the mapping section, only the names of fields on the Commerce side are specified (**AxFields**).</span></span> <span data-ttu-id="b5124-147">既定では、同じフィールド名がチャネル側でも使用されていると想定します。</span><span class="sxs-lookup"><span data-stu-id="b5124-147">By default, it's assumed that the same field name is also used on the channel side.</span></span> <span data-ttu-id="b5124-148">ただし、対応するチャンネル テーブルのフィールド名は、時にコマース側にあるフィールド名とは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b5124-148">However, the field name on the corresponding channel table might sometimes differ from the field name on the Commerce side.</span></span> <span data-ttu-id="b5124-149">この場合、マッピングで **&lt;フィールド&gt;** ノードの **ToName** 属性を使用してチャネル側でフィールドの名前を設定できます。</span><span class="sxs-lookup"><span data-stu-id="b5124-149">In this case, in the mapping, you can use the **ToName** attribute of the **&lt;Field&gt;** node to set the name of the field on the channel side.</span></span>

4. <span data-ttu-id="b5124-150">プロジェクトを右クリックし、**追加** &gt; **新しい項目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-150">Right-click the project, and then select **Add** &gt; **New Item**.</span></span>
5. <span data-ttu-id="b5124-151">**新しい項目の追加**ダイアログ ボックスで、**リソース**を選択し、リソース ファイルに **RetailCDXSeedDataAX7_Custom** と名前を付けてから、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-151">In the **Add New item** dialog box, select **Resources**, name the resource file **RetailCDXSeedDataAX7_Custom**, and then select **Add**.</span></span>

    ![新しい品目の追加](media/cdx-ext-1.png)

6. <span data-ttu-id="b5124-153">**リソース ファイルの選択**ダイアログ ボックスで、手順 2 で作成したリソース ファイルを検索し、**開く**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-153">In the **Select a Resource file** dialog box, find the resource file that you created in step 2, and then select **Open**.</span></span>
7. <span data-ttu-id="b5124-154">**registerCDXSeedDataExtension** イベントを処理するために使用する新しいクラスを追加します。</span><span class="sxs-lookup"><span data-stu-id="b5124-154">Add a new class that should be used to handle the **registerCDXSeedDataExtension** event.</span></span> <span data-ttu-id="b5124-155">**RetailCDXSeedDataBase** クラスを検索し、デザイナーで開きます。</span><span class="sxs-lookup"><span data-stu-id="b5124-155">Search for the **RetailCDXSeedDataBase** class, and then open it in the designer.</span></span> <span data-ttu-id="b5124-156">**registerCDXSeedDataExtension** デリゲートを右クリックし、**イベント ハンドラーをコピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-156">Right-click the **registerCDXSeedDataExtension** delegate, and then select **Copy event handler**.</span></span>
8. <span data-ttu-id="b5124-157">作成したイベント ハンドラー クラスに移動して、次のイベント ハンドラー コードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="b5124-157">Go to the event handler class that you created and paste the following event handler code into it.</span></span>

    ```csharp
    if (originalCDXSeedDataResource == resourceStr(RetailCDXSeedDataAX7))
    {
        resources.addEnd(resourceStr(RetailCDXSeedDataAX7_Custom));
    }
    ```

    > [!NOTE]
    > <span data-ttu-id="b5124-158">システムの CDX シード データに対して 2 つの定義があるため、生成する CDX シード データが拡張の対象のバージョンである場合にのみ、拡張 CDX データが追加されるように指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5124-158">Because there are two definitions for CDX seed data in the system, you must specify that your extension CDX seed data should be added only if the CDX seed data that is being generated is the version that you're trying to extend.</span></span> <span data-ttu-id="b5124-159">**if** 条件が削除されている場合、拡張 CDX シード データが N-1 CDX シード データの上にも適用され、意図しない結果が生じる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b5124-159">If the **if** condition is removed, your extension CDX seed data could also be applied on top of the N-1 CDX seed data and cause unintended results.</span></span> <span data-ttu-id="b5124-160">ベスト プラクティスとして、X++ の CDX/Retail スケジューラ同期フレームワーク クラスのその他のカスタマイズを回避することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b5124-160">As a best practice, try to avoid any other customization on CDX/Retail scheduler sync framework class in X++.</span></span> <span data-ttu-id="b5124-161">追加の処理が実行される場合、これによりデータ フローが影響を受けることがあります。</span><span class="sxs-lookup"><span data-stu-id="b5124-161">This could impact the flow of data when extra processing is performed.</span></span> <span data-ttu-id="b5124-162">提案されるパターンは、別のクラスおよびバッチ ジョブによりアップロードされたデータを処理させることです。</span><span class="sxs-lookup"><span data-stu-id="b5124-162">The suggested pattern is to have a separate class and batch job to process the uploaded data.</span></span>
    >
    > <span data-ttu-id="b5124-163">後で言及されるさまざまなシナリオの個別のリソース ファイルを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b5124-163">You don't have to create separate resource files for the various scenarios that are mentioned later.</span></span> <span data-ttu-id="b5124-164">1 つのファイルにすべてのカスタム ジョブ情報を含め、拡張機能クラスからそのファイルを登録することができます。</span><span class="sxs-lookup"><span data-stu-id="b5124-164">You can have one file that contains all the custom job information and register that file from the extension class.</span></span>
    >
    > <span data-ttu-id="b5124-165">初期化クラスが実行される場合、このクラスはこのハンドラーを実装する拡張機能を検索します。</span><span class="sxs-lookup"><span data-stu-id="b5124-165">When the initialization class runs, it looks for any extension that implements this handler.</span></span> <span data-ttu-id="b5124-166">拡張子が見つかった場合、ランタイムはリソース ファイルに含まれるカスタム情報も初期化します。</span><span class="sxs-lookup"><span data-stu-id="b5124-166">If an extension is found, the runtime will also initialize the custom information that is found in the resource file.</span></span>

9. <span data-ttu-id="b5124-167">**Retail と Commerce > バックオフィスの設定 > コマース スケジューラ >コマース スケジューラの初期化**に移動します。</span><span class="sxs-lookup"><span data-stu-id="b5124-167">Go to **Retail and Commerce > Headquarters setup > Commerce scheduler >Initialize commerce scheduler**.</span></span>
10. <span data-ttu-id="b5124-168">**コマース スケジューラの初期化**ダイアログの **OK** ボタンをクリックして CDX の初期化を実行します。</span><span class="sxs-lookup"><span data-stu-id="b5124-168">Run the CDX initialization by clicking the **OK** button on **Initialize commerce scheduler** dialog.</span></span>

## <a name="pull-data-from-a-new-channel-database-table-to-a-new-hq-table-by-using-a-push-job"></a><span data-ttu-id="b5124-169">プッシュ ジョブを使用して新しいチャンネル データベース テーブルから HQ テーブルにデータをプルする</span><span class="sxs-lookup"><span data-stu-id="b5124-169">Pull data from a new channel database table to a new HQ table by using a push job</span></span>

<span data-ttu-id="b5124-170">新しいチャネル テーブルから HQ にデータをプルするには、次の 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="b5124-170">To pull data from a new channel table to HQ, you have two options:</span></span>

+ <span data-ttu-id="b5124-171">ここに示すように、新しいリソース ファイルを作成し、新しいリソースを 2 行目のイベント ハンドラーに追加します。</span><span class="sxs-lookup"><span data-stu-id="b5124-171">Create a new resource file and add the new resource to the event handler as a second line, as shown here.</span></span>

    ```csharp
    if (originalCDXSeedDataResource == resourceStr(RetailCDXSeedDataAX7))
    {
        resources.addEnd(resourceStr(RetailCDXSeedDataAX7\_Custom));
        resources.addEnd(resourceStr(RetailCDXSeedDataAX7\_Custom1));
    }
    ```

+ <span data-ttu-id="b5124-172">新しい行を追加しなくて済むように、新しい情報を含む既存のリソース ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="b5124-172">Update the existing resource file with the new information, so that you don't have to add a new line.</span></span> <span data-ttu-id="b5124-173">アップロードするには、次の例に示すように、リソース ファイルの **IsUpload** 属性を **true** に設定し、カスタム プルジョブに関する情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="b5124-173">To upload you set the **IsUpload** attribute to **true** in the resource file and add information about your custom pull job, as shown in the following example.</span></span>

    ```xml
    <Subjob Id="ContosoRetailSeatReservationTrans" TargetTableSchema="ext" IsUpload="true"
    ReplicationCounterFieldName="ReplicationCounterFromOrigin" AxTableName="ContosoRetailSeatReservationTrans">
        <ScheduledByJobs>
            <ScheduledByJob>P-1000</ScheduledByJob>
        </ScheduledByJobs>
        <AxFields>
            <Field Name="transactionId"/>
            <Field Name="storeId"/>
            <Field Name="terminalId"/>
            <Field Name="contactPhoneNo"/>
            <Field Name="numberOfCustomers"/>
            <Field Name="customerName"/>
            <Field Name="reservationDate"/>
            <Field Name="reservationTime"/>
            <Field Name="replicationCounterFromOrigin"/>
        </AxFields>
    </Subjob>
    ```
  > [!NOTE]
  > <span data-ttu-id="b5124-174">この新規テーブルを既存のプル ジョブ (P-1000) の一部として追加するか、または新しいプル ジョブを作成するかのいずれかを実行できます。</span><span class="sxs-lookup"><span data-stu-id="b5124-174">You can either add this new table as part of the existing pull job (P-1000) or create a new pull job.</span></span>

## <a name="other-scenarios"></a><span data-ttu-id="b5124-175">その他のシナリオ</span><span class="sxs-lookup"><span data-stu-id="b5124-175">Other scenarios</span></span>
<span data-ttu-id="b5124-176">残りのプッシュとプル シナリオでは、サンプル リソース ファイルの情報のみが記載されます。それは前のセクションの説明にあるように、初期化が同じであるためです。</span><span class="sxs-lookup"><span data-stu-id="b5124-176">For the remaining push and pull scenarios, only the information for the sample resource file is described, because initialization is the same as we described in the previous sections.</span></span>

### <a name="push-existing-columns-that-arent-mapped-as-part-of-any-subjobs"></a><span data-ttu-id="b5124-177">任意のサブジョブの一部としてマップされていない既存の列をプッシュ</span><span class="sxs-lookup"><span data-stu-id="b5124-177">Push existing columns that aren't mapped as part of any subjobs</span></span>

<span data-ttu-id="b5124-178">次の例で示すように、マッピングされていない既存の列を、新しい拡張列またはチャンル データベース内の既存の列のいずれかにプッシュすることができます。</span><span class="sxs-lookup"><span data-stu-id="b5124-178">You can push the existing unmapped column to either new extension columns or existing columns in the channel database, as shown in the following example.</span></span> 

```xml
<Subjob Id="RetailChannelTable" TargetTableSchema="ext">
    <AxFields>
        <Field Name="Payment"/>
        <!-- Existing column which was not pushed to channel db-->
        <Field Name="PaymMode"/>
        <!-- Existing column which was not pushed to channel db-->
        <Field Name="ContosoRetailWallPostMessage"/>
        <!-- New column from the extended table -->
    </AxFields>
</Subjob>
```

<span data-ttu-id="b5124-179">テーブルに **RecId** ではない主キーがある場合、次の例に示されるように、チャンネル側の拡張子テーブルに 非 **RecId** 主キーも含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5124-179">If the table has a primary key that isn't **RecId**, your extension table on the channel side should also contain the non-**RecId** primary keys, as shown in the following example.</span></span>

```xml
    <Subjob Id="RetailCustTable" TargetTableSchema="ext">
        <AxFields>
            <Field Name="ReturnTaxGroup_W"/>
            <!-- Existing column which was not pushed to channel db-->
            <Field Name="SSNNumber"/>
            <!-- New column from the extended table-->
        </AxFields>
    </Subjob>
</Subjobs>
```

### <a name="pull-new-columns-to-an-existing-table"></a><span data-ttu-id="b5124-180">新しい列を既存のテーブルにプルする</span><span class="sxs-lookup"><span data-stu-id="b5124-180">Pull new columns to an existing table</span></span>

<span data-ttu-id="b5124-181">新しい列を追加して既存のテーブルの一部を取得する場合は、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="b5124-181">If you add new columns and want to pull in part of the existing table, use the following code.</span></span>

```xml
<Subjob Id="RetailTransactionTable" TargetTableName="CONTOSORETAILTRANSACTIONTABLE" TargetTableSchema="ext"  OverrideTarget="false">
    <AxFields>
        <Field Name="ContosoRetailSeatNumber"/>
        <Field Name="ContosoRetailServerStaffId"/>
    </AxFields>
</Subjob>
```

### <a name="move-an-existing-subjob-to-another-subjob"></a><span data-ttu-id="b5124-182">別のサブジョブへの既存のサブジョブの移動</span><span class="sxs-lookup"><span data-stu-id="b5124-182">Move an existing subjob to another subjob</span></span>

<span data-ttu-id="b5124-183">既存のサブジョブを別のジョブに移動するには、リソース ファイルの **ScheduledByJob** 属性を変更することができます。この属性はイベント ハンドラの一部として実行されます。</span><span class="sxs-lookup"><span data-stu-id="b5124-183">To move an existing subjob to another job, you can change the **ScheduledByJob** attribute in the resource file and it is run as part of the event handler.</span></span>

```xml
<Subjob Id="DirPartyTable">
    <ScheduledByJobs>
        <ScheduledByJob>1000</ScheduledByJob>
        <!--add existing subjob to another job-->
    </ScheduledByJobs>
```

## <a name="cdx-sample---pull-new-columns-to-an-existing-table"></a><span data-ttu-id="b5124-184">CDX サンプル - 新しい列を既存のテーブルにプルする</span><span class="sxs-lookup"><span data-stu-id="b5124-184">CDX sample - Pull new columns to an existing table</span></span>
<span data-ttu-id="b5124-185">Microsoft Dynamics 365 Retail アプリ更新プログラム 5 では、RetailSDK\Documents\SampleExtensionsInstructions\ExtensionTables に新しいサンプルが追加され、そこにすべてのサンプル SQL スクリプト、さまざまな CDX 拡張機能シナリオの ax プロジェクト ファイルがありますが、さまざまな CDX 拡張機能シナリオの参照として使用してください。</span><span class="sxs-lookup"><span data-stu-id="b5124-185">In Microsoft Dynamics 365 Retail App update 5, we added a new sample in RetailSDK\Documents\SampleExtensionsInstructions\ExtensionTables, it has all the sample SQL scripts, ax project files for different CDX extension scenarios, please use it as a reference for different CDX extension scenarios.</span></span>

<span data-ttu-id="b5124-186">次のセクションでは、拡張テーブルを使用してトランザクション テーブルをカスタマイズする手順とベスト プラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b5124-186">In the next sections, we discuss the steps and best practices for customizing transactional tables by using extension tables.</span></span> <span data-ttu-id="b5124-187">他のセクションでは、CDX をカスタマイズしてチャネル側のカスタマイズされた (拡張子) テーブルをコマースにアップロードする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b5124-187">Another section shows how to customize CDX to upload the customized (extension) tables on the channel side back to Commerce.</span></span> <span data-ttu-id="b5124-188">また、カスタマイズのテスト方法を説明するセクションも含めました。</span><span class="sxs-lookup"><span data-stu-id="b5124-188">We have also included a section that describes how to test the customization.</span></span>

### <a name="setup-steps"></a><span data-ttu-id="b5124-189">設定手順</span><span class="sxs-lookup"><span data-stu-id="b5124-189">Setup steps</span></span>

<span data-ttu-id="b5124-190">変更していない Retail ソフトウェア開発キット (SDK) にこれらの変更を実装することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b5124-190">We recommend that you implement these changes on an untouched Retail software development kit (SDK).</span></span> <span data-ttu-id="b5124-191">または、SDK を Microsoft Azure DevOps などのソース管理下で配置することにより、どのステップでも変更を簡単に元に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="b5124-191">Alternatively, you can put the SDK under source control, such as Microsoft Azure DevOps, so that you can easily revert your changes at any step.</span></span> <span data-ttu-id="b5124-192">まず、SDK にある \*.axpp パッケージをインポートします。</span><span class="sxs-lookup"><span data-stu-id="b5124-192">To begin, you import the \*.axpp package that is located in the SDK.</span></span> <span data-ttu-id="b5124-193">次に、チャンネル データベースで、SQL 更新スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="b5124-193">You then run the SQL update script on your channel database.</span></span>

1. <span data-ttu-id="b5124-194">カスタマイズ コードを含むコマース側にパッケージをインポートします。</span><span class="sxs-lookup"><span data-stu-id="b5124-194">Import the package on the Commerce side that contains the customization code:</span></span>

    1. <span data-ttu-id="b5124-195">ExtensionTablesAndCDXCustomization.axpp ファイルをRetailSDK\Documents\SampleExtensionsInstructions\ExtensionTables フォルダーからコピーし、拡張プロジェクト フォルダーに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="b5124-195">Copy the ExtensionTablesAndCDXCustomization.axpp file from the RetailSDK\Documents\SampleExtensionsInstructions\ExtensionTables   folder and paste in your extension project folder.</span></span>
    2. <span data-ttu-id="b5124-196">Microsoft Visual Studio を起動します。</span><span class="sxs-lookup"><span data-stu-id="b5124-196">Start Microsoft Visual Studio.</span></span>
    3. <span data-ttu-id="b5124-197">**Dynamics 365** > **インポート プロジェクト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-197">Select **Dynamics 365** > **Import project**.</span></span>
    4. <span data-ttu-id="b5124-198">**プロジェクトのインポート** ダイアログ ボックスで、手順 1 でコピーした .axpp ファイルのパスを指定します。</span><span class="sxs-lookup"><span data-stu-id="b5124-198">In the **Import project** dialog box, specify the path of the .axpp file you copied in step 1.</span></span>
    5. <span data-ttu-id="b5124-199">必要に応じて、**現在のソリューション** または **新しいソリューション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-199">Select either **Current solution** or **New solution**, according to your preference.</span></span>
    6. <span data-ttu-id="b5124-200">**OK** を選択してパッケージのインポートを開始します。</span><span class="sxs-lookup"><span data-stu-id="b5124-200">Select **OK** to begin to import the package.</span></span>

        <span data-ttu-id="b5124-201">インポートが完了した後、ソリューション エクスプローラーにファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="b5124-201">After the import is completed, you have the files in Solution Explorer.</span></span>

    7. <span data-ttu-id="b5124-202">ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="b5124-202">Build the solution.</span></span>
    8. <span data-ttu-id="b5124-203">プロジェクトを右クリックし、**データベースの同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-203">Right-click the project, and then select **Synchronize database**.</span></span>

2. <span data-ttu-id="b5124-204">SQL 更新スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="b5124-204">Run the SQL update script:</span></span>

   1. <span data-ttu-id="b5124-205">Retail SDK フォルダーから **ContosoRetailExtensionTablesUpdate.sql** ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="b5124-205">Copy the **ContosoRetailExtensionTablesUpdate.sql** file from the Retail SDK folder.</span></span> <span data-ttu-id="b5124-206">同様の仕方で他のサンプル ファイルを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="b5124-206">You can run the other sample files in a similar manner.</span></span>
   2. <span data-ttu-id="b5124-207">Microsoft SQL Server ブラウザーでスクリプトを開いて、チャネル データベースに対してスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="b5124-207">Open the script in Microsoft SQL Server Browser, and run the script against your channel database.</span></span>

      <span data-ttu-id="b5124-208">このステップでは、トランザクション テーブルをカスタマイズするために必要な拡張テーブルとビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="b5124-208">This step creates the extension tables and views that are required in order to customize the transactional tables.</span></span> <span data-ttu-id="b5124-209">スクリプトはその他のサンプル シナリオに使用されるその他のテーブルも作成することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b5124-209">Note that the script also creates other tables that are used for other sample scenarios.</span></span>

### <a name="extend-the-data-in-the-sample"></a><span data-ttu-id="b5124-210">サンプルでデータを拡張する</span><span class="sxs-lookup"><span data-stu-id="b5124-210">Extend the data in the sample</span></span>

<span data-ttu-id="b5124-211">コマース側のテーブル拡張は、サンプルですでに作成されています。</span><span class="sxs-lookup"><span data-stu-id="b5124-211">The table extension on the Commerce side is already created in the sample.</span></span> <span data-ttu-id="b5124-212">手動で作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b5124-212">To create it manually, follow these steps.</span></span>

1. <span data-ttu-id="b5124-213">Visual Studio を起動します。</span><span class="sxs-lookup"><span data-stu-id="b5124-213">Start Visual Studio.</span></span>
2. <span data-ttu-id="b5124-214">メニューで、**表示** > **アプリケーション エクスプローラー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-214">On the menu, select **View** > **Application Explorer**.</span></span>
3. <span data-ttu-id="b5124-215">**データ モデル** > **テーブル** > **RetailTransactionTable** を選択し、**RetailTransactionTable** を右クリックして **拡張機能を作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-215">Select **Data Model** > **Tables** > **RetailTransactionTable**, right-click **RetailTransactionTable**, and then select **Create extension**.</span></span>

    <span data-ttu-id="b5124-216">ベスト プラクティスは、デフォルトの名前を次のように変更する必要があります **RetailTransactionTable.ContosoRetailExtension**。</span><span class="sxs-lookup"><span data-stu-id="b5124-216">As a best practice, you should change the default name to something like **RetailTransactionTable.ContosoRetailExtension**.</span></span> <span data-ttu-id="b5124-217">常に一意の接頭語を追加します。</span><span class="sxs-lookup"><span data-stu-id="b5124-217">Always add your unique prefix.</span></span> <span data-ttu-id="b5124-218">このサンプルでは、**ContosoRetail** が一意の接頭語として使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5124-218">In this sample, **ContosoRetail** is used as a unique prefix.</span></span> <span data-ttu-id="b5124-219">一意の接頭語を使用することにより、複数の独立系ソフトウェア ベンダー (ISV) によってテーブルが拡張されている場合、名前の競合を防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="b5124-219">By using a unique prefix, you help prevent naming conflicts if a table is extended by multiple independent software vendors (ISVs).</span></span>

4. <span data-ttu-id="b5124-220">新しい **RetailTransactionTable.ContosoRetailExtension** テーブルで、2 つの新しいフィールドを作成します。</span><span class="sxs-lookup"><span data-stu-id="b5124-220">In the new **RetailTransactionTable.ContosoRetailExtension** table, create two new fields:</span></span>

    <span data-ttu-id="b5124-221">**タイプ = 文字列、名前 =ContosoRetailServerStaffId**: **拡張データ型**プロパティを **RetailStaffId** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b5124-221">**Type=string, name=ContosoRetailServerStaffId**: Set the **Extended data type** property to **RetailStaffId**.</span></span>
    <span data-ttu-id="b5124-222">**タイプ = 整数、名前 =ContosoRetailSeatNumber**: **拡張データ型**プロパティを **ContosoRetailSeatNumber** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b5124-222">**Type=int, name=ContosoRetailSeatNumber**: Set the **Extended data type** property to **ContosoRetailSeatNumber**.</span></span>

5. <span data-ttu-id="b5124-223">変更を保存し、プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="b5124-223">Save the changes, and build your project.</span></span>
6. <span data-ttu-id="b5124-224">プロジェクトを右クリックし、**データベースの同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-224">Right-click your project, and then select **Synchronize the database**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b5124-225">ベスト プラクティスとして、今後の名前の競合を回避するために新しい列名に固有の接頭語が追加されます。</span><span class="sxs-lookup"><span data-stu-id="b5124-225">As a best practice, the unique prefix is added to the new column names to help prevent future naming conflicts.</span></span> <span data-ttu-id="b5124-226">別の ISV が同じ名前を持つ列を作成する場合、または Microsoft が同じ名前を持つ列を使用する更新プログラムをリリースする場合、名前付けの競合が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b5124-226">A naming conflict can occur if another ISV creates a column that has the same name, or if Microsoft releases an update that uses a column that has the same name.</span></span> <span data-ttu-id="b5124-227">拡張テーブルでは異なる AOT 資産に作成されますが、新しい列は SQL の元のテーブルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="b5124-227">Even though the extension table is created in a different AOT asset, the new columns are added to the original table in SQL.</span></span>

### <a name="extend-the-database-on-the-channel-side"></a><span data-ttu-id="b5124-228">チャンネル側にあるデータベースを拡張</span><span class="sxs-lookup"><span data-stu-id="b5124-228">Extend the database on the channel side</span></span>

<span data-ttu-id="b5124-229">Retail SDK フォルダーから SQL Server **ContosoRetailExtensionTablesUpdate.sql** スクリプトを開いて実行します。</span><span class="sxs-lookup"><span data-stu-id="b5124-229">From the Retail SDK folder, open and run the SQL Server **ContosoRetailExtensionTablesUpdate.sql** script.</span></span> <span data-ttu-id="b5124-230">複数の品目が作成され、コンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="b5124-230">Several items are created and configured:</span></span>

+ <span data-ttu-id="b5124-231">外部キーとカスタム (拡張子) フィールドを含む **[ext].ContosoRetailTransactionTable** テーブルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="b5124-231">The **[ext].ContosoRetailTransactionTable** table that has the foreign key and custom (extension) fields is created.</span></span> <span data-ttu-id="b5124-232">テーブルに追加した拡張列に加えて、チャネル側の拡張テーブルにはチャネル側にある元のテーブルと同じ主キー列が必要です。</span><span class="sxs-lookup"><span data-stu-id="b5124-232">In addition to the extension columns that we added in the tables, the extension table on the channel side must have the same primary key columns as the original table on the channel side.</span></span> <span data-ttu-id="b5124-233">したがって、[ext].RetailTransactionTable_ContosoRetailExtension には、[ax].RetailTransactionTable で使用される 4 つの主キー列があります。</span><span class="sxs-lookup"><span data-stu-id="b5124-233">Therefore, [ext].RetailTransactionTable_ContosoRetailExtension has the four primary key columns that are used in [ax].RetailTransactionTable.</span></span> <span data-ttu-id="b5124-234">ベスト プラクティスは、チャンネル側の拡張子テーブルに主キー列を追加するときに、列の名前を元のテーブルの主キー列の名前と同じにしておきます。</span><span class="sxs-lookup"><span data-stu-id="b5124-234">As a best practice, when you add the primary key columns to the extension table on the channel side, keep the names of the columns the same as the names of the primary key column on the original table.</span></span> 

+ <span data-ttu-id="b5124-235">CDX は、チャネル拡張テーブルからカスタム列をアップロードしてコマースに戻すように構成されています。</span><span class="sxs-lookup"><span data-stu-id="b5124-235">CDX is configured to upload and pull the custom columns from the channel extension table back to Commerce.</span></span> <span data-ttu-id="b5124-236">RetailCDXSeedDataAX7 リソースには、コマースからチャネル データベースへのテーブル マッピングの情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b5124-236">The RetailCDXSeedDataAX7 resource contains the information for the table mapping from Commerce to the channel database.</span></span> <span data-ttu-id="b5124-237">CDX はこの情報を使用して、必要なデータ転送スケジューラのジョブとサブジョブを作成します。</span><span class="sxs-lookup"><span data-stu-id="b5124-237">CDX uses this information to create the required data transfer scheduler jobs and subjobs.</span></span> <span data-ttu-id="b5124-238">データ転送に新しい拡張テーブルまたは列を含めるには、CDX データ転送のカスタマイズを指定するリソース ファイルを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5124-238">To include your new extension tables or columns in the data transfer, you must provide a resource file that specifies the customization for the CDX data transfer.</span></span> <span data-ttu-id="b5124-239">ベスト プラクティスは、競合を防ぐため次のような名前付け規則を使用します。 **RetailCDXSeedDataAX7_ContosoRetailExtension**。</span><span class="sxs-lookup"><span data-stu-id="b5124-239">As a best practice, use the following naming convention to prevent conflicts: **RetailCDXSeedDataAX7_ContosoRetailExtension**.</span></span> <span data-ttu-id="b5124-240">(ここでは、**ContosoRetail** は、固有の拡張機能です。)</span><span class="sxs-lookup"><span data-stu-id="b5124-240">(Here, **ContosoRetail** is your unique extension.)</span></span>

<span data-ttu-id="b5124-241">Retail SDK のサンプル CDX リソース ファイルには、追加のカスタマイズが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b5124-241">The sample CDX resource file in the Retail SDK contains additional customizations.</span></span> <span data-ttu-id="b5124-242">ただし、RetailTransactionTable 拡張子の例の場合、次のコードのセクションはチャンネル側から HQ にデータをプルするために必要な唯一のセクションです。</span><span class="sxs-lookup"><span data-stu-id="b5124-242">However, for our example of RetailTransactionTable extension, the section in the following code is the only section that is required to pull data from the channel side back to HQ.</span></span>

```csharp
<RetailCdxSeedData Name="AX7" ChannelDBSchema="ext" ChannelDBMajorVersion="7">
    <Subjobs>
        <!--Adding additional columns to (existing) RetailTransactionTable and wants to pull it back to HQ.For upload subjobs, set the OverrideTarget property to  "false", as ilustrated below. This will tell CDX to use the table defined by TargetTableName and TargetTableSchema as extension table on this subjob.-->
        <Subjob Id="RetailTransactionTable" TargetTableName ="CONTOSORETAILTRANSACTIONTABLE" TargetTableSchema="ext" OverrideTarget="false">
            <!--Notice that there is no mention of the <ScheduledByJobs></ScheduledByJobs> because the subjob is already part of an upload job. -->
            <AxFields>
                <!--If you notice the existing columns are not listed here in the <Field> tag, it's because the existing fields are already mapped in the main RetailCdxSeedData resource file, we only add the delta here. -->
                <Field Name="ContosoRetailSeatNumber" />
                <Field Name="ContosoRetailServerStaffId" />
            </AxFields>
        </Subjob>
    </Subjobs>
</RetailCdxSeedData>
```

<span data-ttu-id="b5124-243">**このリソース ファイルで使用されるフィールドの説明:**</span><span class="sxs-lookup"><span data-stu-id="b5124-243">**Description  of the fields used in this resource file:**</span></span>

<span data-ttu-id="b5124-244">**ChannelDBSchema ='ext'** - リソースがチャンネル データベース内の拡張スキーマから読み取るように、このフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b5124-244">**ChannelDBSchema='ext'** – This field is included so that the resource reads from the extension schema in the channel database.</span></span>

<span data-ttu-id="b5124-245">**サブジョブ ID ="RetailTransactionTable"** – SubJob ID がそのテーブルの元のサブジョブ ID と同じであることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5124-245">**Subjob Id="RetailTransactionTable"** – You must make sure that the SubJob ID is the same as the orginal subjob id for that table.</span></span> <span data-ttu-id="b5124-246">そうすると、拡張性フレームワークはユーザーが既存のサブジョブをカスタマイズすることを判断することができます。</span><span class="sxs-lookup"><span data-stu-id="b5124-246">so that the extensibility framework can determine that you're customizing the existing subjob.</span></span> <span data-ttu-id="b5124-247">新しいサブジョブ di を使用すると、同じテーブルに対してサブジョブの重複エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="b5124-247">If you use new subjob di, system will throw duplicate subjob error for the same table.</span></span>

<span data-ttu-id="b5124-248">**TargetTableName = "CONTOSORETAILTRANSACTIONTABLE"** - チャンネル拡張子のテーブル名。</span><span class="sxs-lookup"><span data-stu-id="b5124-248">**TargetTableName ="CONTOSORETAILTRANSACTIONTABLE"** - Your channel extension table name.</span></span>

<span data-ttu-id="b5124-249">**TargetTableSchema="拡張"** - チャンネル拡張子スキーマ。</span><span class="sxs-lookup"><span data-stu-id="b5124-249">**TargetTableSchema="ext"** - Your channel extension schema.</span></span> <span data-ttu-id="b5124-250">現在のところ、拡張子スキーマ名は外部としてのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="b5124-250">Currently we support the extension schema name only as ext.</span></span>

<span data-ttu-id="b5124-251">**OverrideTarget ="false"** - アップロード サブジョブ (チャンネルから本社にデータを取り込むもの) の場合、OverrideTarget が false に設定されていると、TargetTableName で定義されたテーブルが拡張テーブルであり、サブジョブで既に定義されているプライマリ テーブルに沿ってデータがアップロードされることが CDX に通知されます。</span><span class="sxs-lookup"><span data-stu-id="b5124-251">**OverrideTarget="false"** - For upload subjobs (the ones that bring data from the channel to the headquarters), OverrideTarget when set to "false" will tell CDX that the table defined by TargetTableName is an extension table and data will be uploaded along with the primary table already defined in the subjob.</span></span>

<span data-ttu-id="b5124-252">OverrideTarget が "true" に設定されている場合、TargetTableName で定義されたテーブルはサブジョブのプライマリ テーブルをオーバーライドします (プル ジョブでは既定値フィールドが省略され、拡張フィールドのみが考慮されます)。</span><span class="sxs-lookup"><span data-stu-id="b5124-252">If OverrideTarget is set to "true" the table defined by TargetTableName will override the primary table for the subjob (default value fields will be omitted during the pull job and only the extension fields will be considered).</span></span> <span data-ttu-id="b5124-253">たとえば、このサンプルでは、この値を true に設定する場合は、これは ax.RetailTransactionTable からデータをアップロードするのではなく、CDX は ext.CONTOSORETAILTRANSACTIONTABLE からのデータのみをアップロードすることを意味します。</span><span class="sxs-lookup"><span data-stu-id="b5124-253">For instance, in this sample, if you set this value to true, this would mean that instead of uploading the data from ax.RetailTransactionTable, CDX would only upload the data from ext.CONTOSORETAILTRANSACTIONTABLE.</span></span>

<span data-ttu-id="b5124-254">指定されたサブジョブがシンクとして使用する **AxTableName** 値をフレームワークが既に判断できるので、**AxTableName** 属性は指定されません。</span><span class="sxs-lookup"><span data-stu-id="b5124-254">The **AxTableName** attribute isn't specified, because the framework can already determine the **AxTableName** value that the specified subjob uses as a sink.</span></span> <span data-ttu-id="b5124-255">RetailCDXSeedDataAX7 リソースをカスタマイズする場合は、相違点を指定するだけで済みます。</span><span class="sxs-lookup"><span data-stu-id="b5124-255">You only have to specify the differences when you customize the RetailCDXSeedDataAX7 resource.</span></span> <span data-ttu-id="b5124-256">フレームワークが推定できるすべてのデータは、拡張機能により追加する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b5124-256">Any data that the framework can infer doesn't have to be added by extensions.</span></span> <span data-ttu-id="b5124-257">同様に、<AXFields></AXFields? セクションでは、カスタム フィールドまたは新しいフィールドのみ指定されているのがわかります。拡張フレームワークにより、指定されたサブジョブ ID からの残りのフィールドのリストが決まるためです。</span><span class="sxs-lookup"><span data-stu-id="b5124-257">Similarly, in the <AXFields></AXFields? section, you can see that we specified only the custom or new fields, because the extensibility framework can determine the list of remaining fields from the specified subjob ID.</span></span>

+ <span data-ttu-id="b5124-258">CDX カスタマイズ リソースを持つ CDX モジュールが更新されます。</span><span class="sxs-lookup"><span data-stu-id="b5124-258">The CDX module that has the CDX customization resource is updated.</span></span> <span data-ttu-id="b5124-259">RetailCDXSeedDataAX7_ContosoRetailExtensionで指定されているカスタマイズを適用するには、registerCDXSeedDataExtension デリゲートを購読する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5124-259">To apply the customization that is specified in RetailCDXSeedDataAX7_ContosoRetailExtension, you must subscribe to the registerCDXSeedDataExtension delegate.</span></span> <span data-ttu-id="b5124-260">このイベントをサブスクライブすることで、CDX シード データの初期化が実行されるときにカスタマイズが適用されることを保証できます。</span><span class="sxs-lookup"><span data-stu-id="b5124-260">By subscribing to this event, you help guarantee that the customization is applied when initialization of the CDX seed data is run.</span></span>

#### <a name="subscribe-to-the-registercdxseeddataextension-delegate"></a><span data-ttu-id="b5124-261">registerCDXSeedDataExtension デリゲートにサブスクライブ</span><span class="sxs-lookup"><span data-stu-id="b5124-261">Subscribe to the registerCDXSeedDataExtension delegate</span></span>

1. <span data-ttu-id="b5124-262">**表示** > **アプリケーション エクスプローラー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-262">Select **View** > **Application Explorer**.</span></span>
2. <span data-ttu-id="b5124-263">**RetailCDXSeedDataBase** クラスを検索します。</span><span class="sxs-lookup"><span data-stu-id="b5124-263">Search for the **RetailCDXSeedDataBase** class.</span></span>
3. <span data-ttu-id="b5124-264">クラスを右クリックし、**デザイナーで開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-264">Right-click the class, and then select **Open in designer**.</span></span>
4. <span data-ttu-id="b5124-265">デザイナーのデリゲートおよびメソッドの一覧で、**registerCDXSeedDataExtension** デリゲートを選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-265">In the designer, in the list of delegates and methods, select the **registerCDXSeedDataExtension** delegate.</span></span>
5. <span data-ttu-id="b5124-266">右クリックし、**イベント ハンドラーのコピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-266">Right-click, and then select **Copy event handler**.</span></span> <span data-ttu-id="b5124-267">実装する必要があるメソッド シグネチャがコピーされるため、CDX は CDX シード データのカスタマイズされたリソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="b5124-267">The method signature that you must implement is copied, so that CDX picks up the customized resource for CDX seed data.</span></span>
6. <span data-ttu-id="b5124-268">新しいクラスを作成し、**ContosoRetailCDXSeedDataAX7EventHandler** などの名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="b5124-268">Create a new class, and give it a name, such as **ContosoRetailCDXSeedDataAX7EventHandler**.</span></span> <span data-ttu-id="b5124-269">任意の名前を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="b5124-269">You can specify any name.</span></span> <span data-ttu-id="b5124-270">ただし、ベスト プラクティスとしては、接頭語をクラス名の前に付けてください。</span><span class="sxs-lookup"><span data-stu-id="b5124-270">However, as a best practice, be sure to prefix the class name with your prefix.</span></span>
7. <span data-ttu-id="b5124-271">手順 5 でコピーしたコードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="b5124-271">Paste the code that you copied in step 5.</span></span>

    ```csharp
    class ContosoRetailCDXSeedDataAX7EventHandler
    {
        /// <summary>
        /// Registers the extension CDX seed data resource to be used during CDX seed data generation.
        /// </summary>
        /// <param name="result">The result object which is used to return the resource name.</param>
        [SubscribesTo(classStr(RetailCDXSeedDataBase), delegateStr(RetailCDXSeedDataBase, registerCDXSeedDataExtension))]
        public static void RetailCDXSeedDataBase_registerCDXSeedDataExtension(str originalCDXSeedDataResource, List resources)
        {
        }
    }
    ```

8. <span data-ttu-id="b5124-272">CDX 機能拡張フレームワークは、コマースの初期化を選択するとこのメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b5124-272">The CDX extensibility framework calls this method when you select the Commerce initialization.</span></span> <span data-ttu-id="b5124-273">CDX 拡張モジュールが CDX カスタマイズを使用するようにするためには、上記のメソッドに次のコードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="b5124-273">To help guarantee that the CDX extensibility module uses the CDX customization, paste the following code into the preceding method.</span></span>
    
    ```csharp
    if (originalCDXSeedDataResource == resourceStr(RetailCDXSeedDataAX7))
    {
        resources.addEnd(resourceStr(RetailCDXSeedDataAX7_ContosoRetailExtension));
    }
    ```
    
    <span data-ttu-id="b5124-274">カスタム リソースをリストに追加する前に、処理中の originalCDXSeedDataResource リソースが RetailCDXSeedDataAX7 であることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5124-274">Before you add your custom resource to the list, you must verify that the originalCDXSeedDataResource resource that is being processed is RetailCDXSeedDataAX7.</span></span> <span data-ttu-id="b5124-275">そうしないと、予期しない結果が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b5124-275">Otherwise, you might cause unintended results.</span></span>

9. <span data-ttu-id="b5124-276">カスタマイズした構成で CDX モジュールを初期化または再初期化するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b5124-276">To initialize or reinitialize the CDX module with the customized configuration, follow these steps:</span></span>

   1. <span data-ttu-id="b5124-277">**Retail と Commerce** > **バックオフィスの設定** > **コマース スケジューラ** > **スケジューラ ジョブ** > **コマース スケジューラの初期化**に移動します。</span><span class="sxs-lookup"><span data-stu-id="b5124-277">Go to **Retail and Commerce** > **Headquarters setup** > **Commerce scheduler** > **Scheduler jobs** > **Initialize commerce scheduler**.</span></span>
   2. <span data-ttu-id="b5124-278">表示されるダイアログ ボックスで、**既存のコンフィギュレーションの削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-278">In the dialog box that appears, select **Delete existing configuration**.</span></span>
   3. <span data-ttu-id="b5124-279">**OK** を選択して、初期化を開始します。</span><span class="sxs-lookup"><span data-stu-id="b5124-279">Select **OK** to start the initialization.</span></span>

      <span data-ttu-id="b5124-280">初期化が完了したとき、CDX スケジューラ ジョブ、サブジョブの定義、および配布スケジュールは、元の RetailCDXSeedDataAX7 リソースとカスタマイズされた RetailCDXSeedDataAX7_ContosoRetailExtension リソースを使用して更新されます。</span><span class="sxs-lookup"><span data-stu-id="b5124-280">When the initialization is completed, the CDX scheduler jobs, subjob definitions, and distribution schedules are updated by using the original RetailCDXSeedDataAX7 resource and the customized RetailCDXSeedDataAX7_ContosoRetailExtension resource.</span></span>

#### <a name="test-the-customization"></a><span data-ttu-id="b5124-281">カスタマイズのテスト</span><span class="sxs-lookup"><span data-stu-id="b5124-281">Test the customization</span></span>

1. <span data-ttu-id="b5124-282">カスタマイズが正しく動作することを確認します。</span><span class="sxs-lookup"><span data-stu-id="b5124-282">Verify that your customization works correctly:</span></span>

    1. <span data-ttu-id="b5124-283">初期化が完了した後、**Retail と Commerce** > **バックオフィスの設定** > **コマース スケジューラ**に移動し、**スケジューラ サブジョブ** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-283">After the initialization is completed, go to **Retail and Commerce** > **Headquarters setup** > **Commerce scheduler**, and then select the **Scheduler subjobs** link.</span></span>
    2. <span data-ttu-id="b5124-284">サブジョブ テーブルで、**RetailTransactionTable** サブジョブ ID を検索します。</span><span class="sxs-lookup"><span data-stu-id="b5124-284">On the subjobs table, search for the **RetailTransactionTable** subjob ID.</span></span>
    3. <span data-ttu-id="b5124-285">**設定**クイック タブで、**チャネル テーブル名**フィールドが **[ext].RetailTransactionTableView** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b5124-285">On the **Set up** FastTab, verify that the **Channel table name** field is set to **[ext].RetailTransactionTableView**.</span></span>
    4. <span data-ttu-id="b5124-286">詳細セクションの**チャネル フィールド マッピング** セクションで、新しいカスタム (拡張) 列がマッピングに表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b5124-286">In the details section, in the **Channel field mapping** section, verify that the new custom (extension) columns are listed in the mapping.</span></span>

2. <span data-ttu-id="b5124-287">CDX ジョブがアップロードし、統合されたビューを使用してチャンネル側にある元のテーブルと拡張テーブルから取得するテスト:</span><span class="sxs-lookup"><span data-stu-id="b5124-287">Test that the CDX job will upload and pull from the original and extension tables on the channel side by using their unified view:</span></span>

    1. <span data-ttu-id="b5124-288">Retail Modern POS (MPOS) でいくつかのトランザクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="b5124-288">Create some transactions in Retail Modern POS (MPOS).</span></span>
    2. <span data-ttu-id="b5124-289">拡張テーブルは Commerce Runtime (CRT) および MPOS では使用されないため、拡張テーブルに手動でデータを挿入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5124-289">Because the extension table isn't used in the Commerce Runtime (CRT) and MPOS, you must manually insert data into the extension table.</span></span> <span data-ttu-id="b5124-290">必要な値を変更した後、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="b5124-290">Run the following script after you change the required values.</span></span>

        ```sql
        INSERT INTO [ext].[CONTOSORETAILTRANSACTIONTABLE] (
        [CONTOSORETAILSEATNUMBER],
        [CONTOSORETAILSERVERSTAFFID],
        [TRANSACTIONID],
        [STORE],
        [CHANNEL],
        [TERMINAL],
        [DATAAREAID])
        VALUES (
        1, /*normally this needs to be an existing seat number from ContosoRetailSeatingData table, but for this test add any number*/
        '000160' /*add any staff ID here*/,
        'HOUSTON-HOUSTON-11-101',/\*add the transaction id you just created */
        'HOUSTON', /*add the store used to create the transaction */
        5637144592, /*add the channel RecId of the store used to create the transaction*/
        'HOUSTON-11', /*add the terminalId used to create the transaction*/
        'USRT' /*add the dataareaId used by the store*/)
        GO
        ```

        <span data-ttu-id="b5124-291">他のトランザクションにもこの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="b5124-291">Repeat this step for the other transactions.</span></span> <span data-ttu-id="b5124-292">MPOS で作成したトランザクションの一部 [ext].[CONTOSORETAILTRANSACTIONTABLE] に対応するデータを追加しないでください。</span><span class="sxs-lookup"><span data-stu-id="b5124-292">Don't add corresponding data in [ext].[CONTOSORETAILTRANSACTIONTABLE] for some of the transactions that you created in MPOS.</span></span> <span data-ttu-id="b5124-293">この方法で、拡張テーブルに対応するデータがない場合でも、[ax].RetailTransactionTable からデータを取得してアップロードすることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="b5124-293">In this way, you can verify that the data from [ax].RetailTransactionTable is pulled and uploaded even if there is no corresponding data in the extension table.</span></span>

    3. <span data-ttu-id="b5124-294">**Dynamics 365** > **Retail と Commerce** > **Retail とコマース IT** に移動し, **配送スケジュール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-294">Go to **Dynamics 365** > **Retail and Commerce** > **Retail and Commerce IT**, and then select **Distribution schedule**.</span></span>
    4. <span data-ttu-id="b5124-295">配送スケジュールの一覧で、**P-0001** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-295">In the list of distribution schedules, select **P-0001**.</span></span> <span data-ttu-id="b5124-296">この配布スケジュールには、カスタマイズした RetailTransactionTable のサブジョブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b5124-296">This distribution schedule contains the RetailTransactionTable subjob that you customized.</span></span>
    5. <span data-ttu-id="b5124-297">アクション ウィンドウで、**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-297">On the Action Pane, select **Run**.</span></span> <span data-ttu-id="b5124-298">確認メッセージが表示されたら、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5124-298">When the confirmation message appears, select **Yes**.</span></span>
    6. <span data-ttu-id="b5124-299">アクション ウィンドウで、**履歴**を選択し**履歴**ページを開き、アップロードされたセッションが正常に完了したことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="b5124-299">On the Action Pane, select **History** to open the **History** page, where you can verify that the uploaded session was completed successfully.</span></span>
    7. <span data-ttu-id="b5124-300">**履歴**ページで、新しいアップロード セッション レコードがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b5124-300">On the **History** page, verify that there is a new upload session record.</span></span> <span data-ttu-id="b5124-301">レコードのステータスが**申請済**に設定され、さらに**影響を受けた行**値は**0** (ゼロ) でないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b5124-301">Also verify that the status of the record is set to **Applied**, and that the **Rows Affected** value isn't **0** (zero).</span></span>

3. <span data-ttu-id="b5124-302">アップロード セッションが正常に適用されたら、**Retail と Commerce** > **照会やレポート** > **店舗のトランザクション**に移動し、アップロードした新しいトランザクションを検索します。</span><span class="sxs-lookup"><span data-stu-id="b5124-302">If the upload session is applied successfully, go to **Retail and Commerce** > **Inquiries and reports** > **Store transactions**, and search for the new transactions that you just uploaded.</span></span> <span data-ttu-id="b5124-303">トランザクション、シート番号、およびサーバー スタッフ ID の各カスタム列に期待された値が入っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b5124-303">Verify that the transactions, seat number, and server staff ID custom columns have the expected values.</span></span>

    <span data-ttu-id="b5124-304">また、チャネル側の [ext].ContosoRetailTransactionTable 拡張テーブルに対応するレコードを持たないトランザクションもアップロードされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b5124-304">Additionally, verify that the transactions that don't have a corresponding record in the [ext].ContosoRetailTransactionTable extension table on the channel side are also uploaded.</span></span> <span data-ttu-id="b5124-305">これらのトランザクションにシート番号とサーバー スタッフ ID の既定値が含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b5124-305">Verify that these transactions have default values for the seat number and server staff ID.</span></span> <span data-ttu-id="b5124-306">シート番号は **0** (ゼロ) に設定し、サーバー スタッフ ID は **000160** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5124-306">The seat number should be set to **0** (zero), and the server staff ID should be set to **000160**.</span></span>
