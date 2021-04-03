---
title: 生成されるドキュメントに対するカスタム ストレージの場所を指定する
description: このトピックでは、電子申告 (ER) 形式で生成されたドキュメントの保存先のリストを拡張する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 146e7fb5fefbecabc99c2978b52eb0e782da0322
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562217"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a>生成されるドキュメントに対するカスタム ストレージの場所を指定する

[!include[banner](../includes/banner.md)]

電子申告 (ER) フレームワークのアプリケーション プログラミング インターフェイス (API) により、電子申告 (ER) 形式が生成するドキュメントの保存先のリストを拡張することができます。 このトピックでは、ER の送信先を作成するタスクを既定の送信先ファクトリに委任し、独自の送信先ロジックを持つカスタム クラスを実装することにより、生成されるドキュメントのカスタムストレージの場所を追加する方法について説明します。

## <a name="prerequisites"></a>必要条件

継続的ビルドをサポートするトポロジを配置します。 詳細については、[継続的ビルドとテストの自動化をサポートするトポロジの配置](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation)を参照してください。 次のいずれかのロールに対応するこのトポロジにアクセスできる必要があります:

- 電子申告開発者
- 電子申告機能コンサルタント
- システム管理者

また、このトポロジの開発環境にもアクセスできる必要があります。

このトピックのすべてのタスクは、**USMF** 会社で完了することができます。

## <a name="import-the-fixed-asset-roll-forward-er-format"></a>固定資産ロール フォワード ER 形式のインポート

カスタム ストレージの場所を追加する予定のドキュメントを生成するには、**固定資産ロール フォワード** ER 形式の構成を現在のトポロジに [インポート](er-download-configurations-global-repo.md) します。

![レポジトリ ページの構成](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a>固定資産ロール フォワード レポートの実行

1. **固定資産** \> **照会およびレポート** \> **トランザクション レポート** \> **固定資産ロールフォワード** に移動します。
2. **開始日** フィールドに **1/1/2017** (2017 年 1 月 1 日) を入力します。
3. **終了日** フィールドに **1/31/2017** (2017 年 1 月 31 日) を入力します。
4. **通貨フィールド** で、**会計通貨** を選択します。
5. **形式マッピング** フィールドで、**固定資産ロール フォワード** を選択します。
6. **OK** を選択します。

![固定資産ロール フォワード レポートのランタイム ダイアロボックス](./media/er-custom-storage-generated-files-runtime-dialog.png)

Microsoft Excel で、生成されてダウンロード可能な送信ドキュメントを確認します。 この動作は、[送信先](electronic-reporting-destinations.md) が設定されておらず、対話モードで実行されている ER フォーマットの [既定の動作](electronic-reporting-destinations.md#default-behavior) です。

## <a name="review-the-source-code"></a>ソース コードの確認

`AssetRollForwardService` クラスの `generateReportByGER()` メソッドのコードを確認します。 `Run()` メソッドを使用して ER フレームワークを呼び出し、**固定資産ロール フォワード** レポートを生成することに注意してください。

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

## <a name="modify-the-source-code"></a>ソース コードの修正

1. Visual Studio プロジェクトで、新しいクラス (この例では `AssetRollForwardDestination`) を追加し、生成される **固定資産ロール フォワード** レポート用のカスタム送信先を実装するコードを記述します。

    - `new()` メソッドは、元の ER 送信先オブジェクトと、生成されたレポートを保存するカスタムの場所を指定するアプリケーション ロジック駆動パラメーターを取得するように設計されています。 この例では、カスタムの場所は、Application Object Server (AOS) サービスを実行するサーバーのローカル ファイル システムのフォルダー名です。
    - `saveFile()` メソッドは、生成されたドキュメントを、AOS サービスを実行するサーバーのローカル ファイル システムのフォルダーに保存するように設計されています。

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

2. Visual Studio プロジェクトで、新しいクラス (この例では `AssetRollForwardDestinationFactory`) を追加し、コードを記述して、送信先の作成を既定の送信先ファクトリに委任するカスタム送信先ファクトリを設定し、ファイル送信先を独自の送信先でラップします。

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

3. 既存の `AssetRollForwardService` クラスを変更し、レポート ランナーのカスタム送信先ファクトリを設定するコードを記述します。 カスタムの送信先ファクトリが構築されるときに、ターゲット フォルダーを指定するアプリケーション駆動型のパラメーターが渡されることに注意してください。 これにより、そのターゲット フォルダーは、生成されたファイルを保存するために使用されます。

    > [!NOTE] 
    > AOS サービスを実行するサーバーのローカル ファイル システムに、指定したフォルダー (この例では **c:\\0**) が存在することを確認してください。 それ以外の場合は、[DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) 例外が実行時にスローされます。

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

4. プロジェクトのリビルドします。

## <a name="re-run-the-fixed-asset-roll-forward-report"></a>固定資産ロール フォワード レポートの再実行

1. **固定資産** \> **照会およびレポート** \> **トランザクション レポート** \> **固定資産ロールフォワード** に移動します。
2. **開始日** フィールドに **1/1/2017** を入力します。
3. **終了日** フィールドに **1/31/2017** を入力します。
4. **通貨フィールド** で、**会計通貨** を選択します。
5. **形式マッピング** フィールドで、**固定資産ロール フォワード** を選択します。
6. **OK** を選択します。
7. ローカルの **C:\\0** フォルダーを参照して、生成ファイルを見つけます。

> [!NOTE]
> この例では、`AssetRollForwardDestination` オブジェクトで `originDestination` オブジェクトが使用されていないため、ER 形式の [送信先](electronic-reporting-destinations.md) の構成は実行時に無視されます。

## <a name="additional-resources"></a>追加リソース

- [電子申告 (ER) の送信先](electronic-reporting-destinations.md)
- [拡張機能のホーム ページ](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]