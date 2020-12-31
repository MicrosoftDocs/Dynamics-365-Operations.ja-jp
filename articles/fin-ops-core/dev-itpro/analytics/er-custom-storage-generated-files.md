---
title: 生成されるドキュメントに対するカスタム ストレージの場所を指定する
description: このトピックでは、電子申告 (ER) 形式で生成されたドキュメントの保存先のリストを拡張する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 362ac7f10cc61e26be89dfbae0e84745d42588a3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680761"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a><span data-ttu-id="0b174-103">生成されるドキュメントに対するカスタム ストレージの場所を指定する</span><span class="sxs-lookup"><span data-stu-id="0b174-103">Specify custom storage locations for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0b174-104">電子申告 (ER) フレームワークのアプリケーション プログラミング インターフェイス (API) により、電子申告 (ER) 形式が生成するドキュメントの保存先のリストを拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="0b174-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="0b174-105">このトピックでは、ER の送信先を作成するタスクを既定の送信先ファクトリに委任し、独自の送信先ロジックを持つカスタム クラスを実装することにより、生成されるドキュメントのカスタムストレージの場所を追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0b174-105">This topic explains how to add a custom storage location for generated documents by delegating the task of creating ER destinations to the default destination factory and then implementing a custom class that has its own destination logic.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0b174-106">必要条件</span><span class="sxs-lookup"><span data-stu-id="0b174-106">Prerequisites</span></span>

<span data-ttu-id="0b174-107">継続的ビルドをサポートするトポロジを配置します。</span><span class="sxs-lookup"><span data-stu-id="0b174-107">Deploy a topology that supports continuous build.</span></span> <span data-ttu-id="0b174-108">詳細については、[継続的ビルドとテストの自動化をサポートするトポロジの配置](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b174-108">For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span></span> <span data-ttu-id="0b174-109">次のいずれかのロールに対応するこのトポロジにアクセスできる必要があります:</span><span class="sxs-lookup"><span data-stu-id="0b174-109">You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="0b174-110">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="0b174-110">Electronic reporting developer</span></span>
- <span data-ttu-id="0b174-111">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="0b174-111">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="0b174-112">システム管理者</span><span class="sxs-lookup"><span data-stu-id="0b174-112">System administrator</span></span>

<span data-ttu-id="0b174-113">また、このトポロジの開発環境にもアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b174-113">You must also have access to the development environment for this topology.</span></span>

<span data-ttu-id="0b174-114">このトピックのすべてのタスクは、**USMF** 会社で完了することができます。</span><span class="sxs-lookup"><span data-stu-id="0b174-114">All the tasks in this topic can be completed in the **USMF** company.</span></span>

## <a name="import-the-fixed-asset-roll-forward-er-format"></a><span data-ttu-id="0b174-115">固定資産ロール フォワード ER 形式のインポート</span><span class="sxs-lookup"><span data-stu-id="0b174-115">Import the Fixed asset roll forward ER format</span></span>

<span data-ttu-id="0b174-116">カスタム ストレージの場所を追加する予定のドキュメントを生成するには、**固定資産ロール フォワード** ER 形式の構成を現在のトポロジに [インポート](er-download-configurations-global-repo.md) します。</span><span class="sxs-lookup"><span data-stu-id="0b174-116">To generate the documents that you plan to add a custom storage location for, [import](er-download-configurations-global-repo.md) the **Fixed asset roll forward** ER format configuration into the current topology.</span></span>

![レポジトリ ページの構成](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="0b174-118">固定資産ロール フォワード レポートの実行</span><span class="sxs-lookup"><span data-stu-id="0b174-118">Run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="0b174-119">**固定資産** \> **照会およびレポート** \> **トランザクション レポート** \> **固定資産ロールフォワード** に移動します。</span><span class="sxs-lookup"><span data-stu-id="0b174-119">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="0b174-120">**開始日** フィールドに **1/1/2017** (2017 年 1 月 1 日) を入力します。</span><span class="sxs-lookup"><span data-stu-id="0b174-120">In the **From date** field, enter **1/1/2017** (January 1, 2017).</span></span>
3. <span data-ttu-id="0b174-121">**終了日** フィールドに **1/31/2017** (2017 年 1 月 31 日) を入力します。</span><span class="sxs-lookup"><span data-stu-id="0b174-121">In the **To date** field, enter **1/31/2017** (January 31, 2017).</span></span>
4. <span data-ttu-id="0b174-122">**通貨フィールド** で、**会計通貨** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b174-122">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="0b174-123">**形式マッピング** フィールドで、**固定資産ロール フォワード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b174-123">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="0b174-124">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b174-124">Select **OK**.</span></span>

![固定資産ロール フォワード レポートのランタイム ダイアロボックス](./media/er-custom-storage-generated-files-runtime-dialog.png)

<span data-ttu-id="0b174-126">Microsoft Excel で、生成されてダウンロード可能な送信ドキュメントを確認します。</span><span class="sxs-lookup"><span data-stu-id="0b174-126">In Microsoft Excel, review the outbound document that is generated and available for download.</span></span> <span data-ttu-id="0b174-127">この動作は、[送信先](electronic-reporting-destinations.md) が設定されておらず、対話モードで実行されている ER フォーマットの [既定の動作](electronic-reporting-destinations.md#default-behavior) です。</span><span class="sxs-lookup"><span data-stu-id="0b174-127">This behavior is the [default behavior](electronic-reporting-destinations.md#default-behavior) for an ER format that no [destinations](electronic-reporting-destinations.md) are configured for, and that is running in interactive mode.</span></span>

## <a name="review-the-source-code"></a><span data-ttu-id="0b174-128">ソース コードの確認</span><span class="sxs-lookup"><span data-stu-id="0b174-128">Review the source code</span></span>

<span data-ttu-id="0b174-129">`AssetRollForwardService` クラスの `generateReportByGER()` メソッドのコードを確認します。</span><span class="sxs-lookup"><span data-stu-id="0b174-129">Review the code of the `generateReportByGER()` method of the `AssetRollForwardService` class.</span></span> <span data-ttu-id="0b174-130">`Run()` メソッドを使用して ER フレームワークを呼び出し、**固定資産ロール フォワード** レポートを生成することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0b174-130">Notice that the `Run()` method is used to call the ER framework and generate the **Fixed asset roll forward** report.</span></span>

```xpp
class AssetRollForwardService extends SysOperationServiceBase
{
    public const str ERFormatModelName = 'Fixed assets';
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'AssetRollForward';

    /// <summary>
    /// Generates report by general electronic reporting
    /// </summary>
    /// <param name = "_contract">The Asset Period Statement contract</param>
    public void generateReportByGER(AssetRollForwardContract _contract)
    {
        ERFormatMappingId   formatMappingId;
        AssetRollForwardDP  dataProvider;
        AssetRollForwardTmp assetRollForwardTmp;
        Query               query;

        query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
        dataProvider = AssetRollForwardDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

        if (assetRollForwardTmp)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                // Call ER to generate the report.
                ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName)
                    .withParameter(parameters)
                    .withFileDestination(_contract.getFileDestination())
                    .run();
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

## <a name="modify-the-source-code"></a><span data-ttu-id="0b174-131">ソース コードの修正</span><span class="sxs-lookup"><span data-stu-id="0b174-131">Modify the source code</span></span>

1. <span data-ttu-id="0b174-132">Visual Studio プロジェクトで、新しいクラス (この例では `AssetRollForwardDestination`) を追加し、生成される **固定資産ロール フォワード** レポート用のカスタム送信先を実装するコードを記述します。</span><span class="sxs-lookup"><span data-stu-id="0b174-132">In your Visual Studio project, add a new class (`AssetRollForwardDestination` in this example), and write code to implement your custom destination for **Fixed asset roll forward** reports that are generated.</span></span>

    - <span data-ttu-id="0b174-133">`new()` メソッドは、元の ER 送信先オブジェクトと、生成されたレポートを保存するカスタムの場所を指定するアプリケーション ロジック駆動パラメーターを取得するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="0b174-133">The `new()` method is designed to get the original ER destination object and the application logic–driven parameter that specifies the custom location where generated reports should be stored.</span></span> <span data-ttu-id="0b174-134">この例では、カスタムの場所は、Application Object Server (AOS) サービスを実行するサーバーのローカル ファイル システムのフォルダー名です。</span><span class="sxs-lookup"><span data-stu-id="0b174-134">In this example, the custom location is the name of a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    - <span data-ttu-id="0b174-135">`saveFile()` メソッドは、生成されたドキュメントを、AOS サービスを実行するサーバーのローカル ファイル システムのフォルダーに保存するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="0b174-135">The `saveFile()` method is designed to save a generated document to a folder of the local file system of the server that runs the AOS service.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// Destination class for <c>AssetRollForwardDestinationFactory</c> that stores a generated report.
    /// </summary>
    public class AssetRollForwardDestination implements ERIFileDestination
    {
        private ERIFileDestination originDestination;
        private str TargetFolder;

        /// <summary>
        /// Creates a stream for new file.
        /// </summary>
        /// <param name = "_fileName">Name of a new file.</param>
        /// <returns>Stream for new file.</returns>
        public System.IO.Stream newFileStream(System.String _fileName)
        {
            return originDestination.newFileStream(_fileName);
        }

        /// <summary>
        /// Saves file in destination.
        /// </summary>
        /// <param name = "_stream">A stream to save.</param>
        /// <param name = "_fileName">A file name.</param>
        /// <returns>Saved stream.</returns>
        public System.IO.Stream saveFile(System.IO.Stream _stream, System.String _fileName)
        {
            _stream.Seek(0, System.IO.SeekOrigin::Begin);
            using (var localStream = System.IO.File::OpenWrite(TargetFolder + _fileName))
            {
                _stream.CopyTo(localStream);
            }
            return _stream;
        }

        /// <summary>
        /// Constructs destination for fixed asset roll forward report.
        /// </summary>
        /// <param name = "_originDestination">The original destination.</param>
        /// <param name = "_TargetFoder">The folder to store a report that's being created.</param>
        /// <returns>The fixed asset roll forward destination.</returns>
        public static AssetRollForwardDestination construct(ERIFileDestination _originDestination, str _TargetFoder)
        {
            return new AssetRollForwardDestination(_originDestination, _TargetFoder);
        }

        protected void new(ERIFileDestination _originDestination, str _TargetFoder)
        {
            originDestination = _originDestination;
            TargetFolder = _TargetFoder;
        }
    }
    ```

2. <span data-ttu-id="0b174-136">Visual Studio プロジェクトで、新しいクラス (この例では `AssetRollForwardDestinationFactory`) を追加し、コードを記述して、送信先の作成を既定の送信先ファクトリに委任するカスタム送信先ファクトリを設定し、ファイル送信先を独自の送信先でラップします。</span><span class="sxs-lookup"><span data-stu-id="0b174-136">In your Visual Studio project, add a new class (`AssetRollForwardDestinationFactory` in this example), and write code to set up a custom destination factory that delegates the creation of a destination to the default destination factory, and to wrap a file destination with your own destination.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using Microsoft.Dynamics365.LocalizationFramework.Format.FileGeneration;

    /// <summary>
    /// Destination factory for using <c>AssetRollForwardDestinationFactory</c>.
    /// </summary>
    public class AssetRollForwardDestinationFactory implements ERIFileDestinationFactory, ERIFileDestinationFactoryPostProcessor
    {
        private ERIFileDestinationFactory originDestinationFactory;
        private str TargetFolder;

        /// <summary>
        /// Creates file destination for print management.
        /// </summary>
        /// <param name = "_fileDestination">A default file destination.</param>
        /// <param name = "_identification">An identification strategy.</param>
        /// <param name = "_rootContext">A root context.</param>
        /// <param name = "_root">A root element.</param>
        /// <returns>A file destination.</returns>
        public ERIDataDrivenFileDestination createPrintMgmtDestination(
            ERIFileDestination _fileDestination,
            ERIObjectIdentificationStrategy _identification,
            ERTextFormatDataContext _rootContext,
            ERTextFormatIFileComponent _root)
        {
            ERIDataDrivenFileDestination dataDrivenDestination = originDestinationFactory.createPrintMgmtDestination(
                _fileDestination,
                _identification,
                _rootContext,
                _root);

            IFileDestinationHost fileDestinationHost = dataDrivenDestination as IFileDestinationHost;
            if (fileDestinationHost)
            {
                fileDestinationHost.FileDestination = AssetRollForwardDestination::construct(
                    fileDestinationHost.get_FileDestination(),
                    TargetFolder);
            }

            return dataDrivenDestination;
        }

        /// <summary>
        /// Constructs the fixed asset roll forward destination factory.
        /// </summary>
        /// <param name = "_originDestinationFactory">The original destination.</param>
        /// <param name = "_TargetFolder">The string containing a folder name that corresponds to the report, that's being created.</param>
        /// <returns>The destination factory for the fixed asset roll forward report.</returns>
        public static AssetRollForwardDestinationFactory construct(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            AssetRollForwardDestinationFactory destinationFactory = new AssetRollForwardDestinationFactory(_originDestinationFactory, _TargetFolder);

            ERIFileDestinationFactoryPostProcessorsHost factoryPostProcessing = ERCast::asObject(destinationFactory.originDestinationFactory) as ERIFileDestinationFactoryPostProcessorsHost;

            if (factoryPostProcessing)
            {
                factoryPostProcessing.addDestinationPostProcessor(destinationFactory);
            }
            return destinationFactory;
        }

        public ERIFileDestination processDestinationAfterCreation(ERIFileDestination _sourceDestination)
        {
            return AssetRollForwardDestination::construct(_sourceDestination, TargetFolder);
        }

        protected void new(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            originDestinationFactory = _originDestinationFactory;
            TargetFolder = _TargetFolder;
        }
    }
    ```

3. <span data-ttu-id="0b174-137">既存の `AssetRollForwardService` クラスを変更し、レポート ランナーのカスタム送信先ファクトリを設定するコードを記述します。</span><span class="sxs-lookup"><span data-stu-id="0b174-137">Modify the existing `AssetRollForwardService` class, and write code to set up a custom destination factory for the report runner.</span></span> <span data-ttu-id="0b174-138">カスタムの送信先ファクトリが構築されるときに、ターゲット フォルダーを指定するアプリケーション駆動型のパラメーターが渡されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0b174-138">Notice that when a custom destination factory is constructed, the application-driven parameter that specifies a target folder is passed.</span></span> <span data-ttu-id="0b174-139">これにより、そのターゲット フォルダーは、生成されたファイルを保存するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0b174-139">In this way, that target folder is used to store generated files.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="0b174-140">AOS サービスを実行するサーバーのローカル ファイル システムに、指定したフォルダー (この例では **c:\\0**) が存在することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="0b174-140">Make sure that the specified folder (**c:\\0** in this example) is present in the local file system of the server that runs the AOS service.</span></span> <span data-ttu-id="0b174-141">それ以外の場合は、[DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) 例外が実行時にスローされます。</span><span class="sxs-lookup"><span data-stu-id="0b174-141">Otherwise, a [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) exception will be thrown at runtime.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    /// <summary>
    /// The electronic reporting service class for fixed asset roll forward report
    /// </summary>
    class AssetRollForwardService extends SysOperationServiceBase
    {
        public const str ERFormatModelName = 'Fixed assets';
        public const str ERModelDataSourceName = 'model';
        public const str DefaultExportedFileName = 'AssetRollForward';

        /// <summary>
        /// Generates report by general electronic reporting
        /// </summary>
        /// <param name = "_contract">The Asset Period Statement contract</param>
        public void generateReportByGER(AssetRollForwardContract _contract)
        {
            ERFormatMappingId   formatMappingId;
            AssetRollForwardDP  dataProvider;
            AssetRollForwardTmp assetRollForwardTmp;
            Query               query;

            query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
            dataProvider = AssetRollForwardDP::construct();
            formatMappingId = _contract.parmFormatMapping();
            assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

            if (assetRollForwardTmp)
            {
                try
                {
                    ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                        .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                        .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                    // Call ER to generate the report.
                    ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());

                    ERIFileDestinationFactoryHost factoryHost = ERCast::asObject(formatMappingRun) as ERIFileDestinationFactoryHost;
                    if (factoryHost)
                    {
                        ERIFileDestinationFactory fileDestinationFactory = factoryHost.getFileDestinationFactory();
                        factoryHost.setFileDestinationFactory(AssetRollForwardDestinationFactory::construct(fileDestinationFactory, @'c:\0\'));
                        formatMappingRun.run();
                    }
                }
                catch
                {
                    // An error occurred while exporting data.
                    error("@SYP4861341");
                }
            }
            else
            {
                // There is no data available.
                info("@SYS300117");
            }
        }
    }
    ```

4. <span data-ttu-id="0b174-142">プロジェクトのリビルドします。</span><span class="sxs-lookup"><span data-stu-id="0b174-142">Rebuild your project.</span></span>

## <a name="re-run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="0b174-143">固定資産ロール フォワード レポートの再実行</span><span class="sxs-lookup"><span data-stu-id="0b174-143">Re-run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="0b174-144">**固定資産** \> **照会およびレポート** \> **トランザクション レポート** \> **固定資産ロールフォワード** に移動します。</span><span class="sxs-lookup"><span data-stu-id="0b174-144">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="0b174-145">**開始日** フィールドに **1/1/2017** を入力します。</span><span class="sxs-lookup"><span data-stu-id="0b174-145">In the **From date** field, enter **1/1/2017**.</span></span>
3. <span data-ttu-id="0b174-146">**終了日** フィールドに **1/31/2017** を入力します。</span><span class="sxs-lookup"><span data-stu-id="0b174-146">In the **To date** field, enter **1/31/2017**.</span></span>
4. <span data-ttu-id="0b174-147">**通貨フィールド** で、**会計通貨** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b174-147">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="0b174-148">**形式マッピング** フィールドで、**固定資産ロール フォワード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b174-148">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="0b174-149">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b174-149">Select **OK**.</span></span>
7. <span data-ttu-id="0b174-150">ローカルの **C:\\0** フォルダーを参照して、生成ファイルを見つけます。</span><span class="sxs-lookup"><span data-stu-id="0b174-150">Browse the local **C:\\0** folder to find the generated file.</span></span>

> [!NOTE]
> <span data-ttu-id="0b174-151">この例では、`AssetRollForwardDestination` オブジェクトで `originDestination` オブジェクトが使用されていないため、ER 形式の [送信先](electronic-reporting-destinations.md) の構成は実行時に無視されます。</span><span class="sxs-lookup"><span data-stu-id="0b174-151">Because the `originDestination` object isn't used in the `AssetRollForwardDestination` object in this example, the configurations for the ER format [destinations](electronic-reporting-destinations.md) will be ignored at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b174-152">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0b174-152">Additional resources</span></span>

- [<span data-ttu-id="0b174-153">電子申告 (ER) の送信先</span><span class="sxs-lookup"><span data-stu-id="0b174-153">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="0b174-154">拡張機能のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="0b174-154">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)
