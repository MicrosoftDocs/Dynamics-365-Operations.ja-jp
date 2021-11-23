---
title: 受信したドキュメントのカスタム ER ソースを実装する
description: このトピックでは、電子申告 (ER) ソースのリストを拡張して、データ インポート用の受信ドキュメントにアクセスする方法について説明します。
author: NickSelin
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERFormatDestinationTable, ERParameters
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-10-01
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 537633473a21af04c55f566f17b316317d02fd7b
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647776"
---
# <a name="implement-a-custom-er-source-of-inbound-documents"></a>受信したドキュメントのカスタム ER ソースを実装する

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

[電子申告 (ER)](general-electronic-reporting.md) フレームワークを使用して受信ドキュメントからデータをインポートするには、インポートをサポートする ER [形式](general-electronic-reporting.md#FormatComponentInbound) を構成し、その形式をデータ ソースとして使用する **宛先** タイプのモデル マッピングを実行します。 データをインポートするには、インポートするドキュメントに移動し、SharePoint フォルダーを、無人モードでインポート可能な受信ドキュメントの標準 ER ソースとして使用します。 このプロセスの詳細については、[SharePoint からのデータ インポートを構成する](er-configure-data-import-sharepoint.md) を参照してください。

ER フレームワークのアプリケーション・プログラミング・インターフェース (API) では、ER フォーマットでデータ インポート用に [解析](/er-parse-incoming-documents.md) される受信ドキュメントにアクセスするための ER ソースのリストを [拡張](er-apis-app10-0-23.md#er-api-extend-file-source) できるようになりました。 したがって、ER の構成を使用して、カスタム ソースに保存されているドキュメントからデータのインポートを実行できます。

このトピックには、受信ドキュメントのカスタム ER ソースを実装して、使用を開始するために完了する必要のある主要なタスクの概要が含まれています。 これらのタスクを完了するには、[SharePoint からのデータ インポートの構成](er-configure-data-import-sharepoint.md)で説明されている仕入先トランザクションのインポートと同じ例を使用します。 これらのタスクのステップは、Microsoft Dynamics 365 Finance の **USMF** 会社で完了することができます。

## <a name="prerequisites"></a>必要条件

### <a name="deploy-a-topology"></a>トポロジをデプロイする

継続的ビルドをサポートするトポロジを配置する必要があります。 詳細については、[継続的ビルドとテストの自動化をサポートするトポロジの配置](../perf-test/continuous-build-test-automation.md)を参照してください。 次のいずれかのロールに対応するこのトポロジにアクセスできる必要があります:

- 電子申告開発者
- 電子申告機能コンサルタント
- システム管理者

また、このトポロジの開発環境にもアクセスできる必要があります。

### <a name="configure-the-er-framework"></a> ER フレームワークを構成する

[ER フレームワークの構成](er-quick-start2-customize-report.md#ConfigureFramework)に記載の手順に従って、 ER パラメーターの最小限のセットを構成します。 ER フレームワークを使用してカスタム ソースから受信ドキュメントをインポートする前に、この設定を完了してください。

### <a name="import-an-er-format-configuration"></a>ER 形式の構成をインポートする

追加のタスクは、[SharePoint からのデータ インポートをコンフィジュレ―ションする](er-configure-data-import-sharepoint.md)で説明されている ER の構成を使用します。 このトピックのタスク ガイドをまだ再生していない場合は、次のファイルをダウンロードしてください。

| コンテンツの説明 | ファイル |
|---------------------|------|
| ER データ モデル構成 | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |
| ER フォーマット構成 | [1099format-import-from-excel.xml](https://download.microsoft.com/download/b/3/8/b38faf0a-fbaf-4e9e-84c2-dedae7464880/1099format-import-from-excel.xml) |
| インポート用のサンプル データを含む .XLSX 形式の受信ファイル | [1099import data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx) |

[XML ファイルから読み込む](er-defer-sequence-element.md#import-the-sample-er-configurations) ER オプションを使用して、ダウンロードした ER コンフィギュレーションを次の順序で Finance インスタンスにインポートします。

1. ER データ モデル構成
2. ER フォーマット構成

![構成ページでインポートされた ER の構成のリスト。](media/er-custom-file-source-configurations.png)

> [!IMPORTANT]
> 作成またはインポートする ER フォーマットには、次のフォーマット エレメントのうち少なくとも 1 つを含める必要があります。
>
> - Common\\File
> - Excel\\File

## <a name="extend-the-source-code"></a>ソース コードの拡張

1. Visual Studio プロジェクトに新しいクラスを追加します。 この例では、`ContosoInboundFile` を使用します。
2. `ERIImportFile` パブリック インターフェイスを使用し、カスタム受信ファイルを説明するコードを書き込みます。 受信ファイルを処理する ER フレームワークの要件に準拠するために、次の情報を指定する必要があります。

    - 実行時にカスタム ソースを一意に識別するためのキー (この例では `sourceSettingsKey` 変数) およびこのキーを取得し、設定する方法。 多くのソースが存在する可能性があるため、このキーは重要です。
    - [*日時*](er-formula-supported-data-types-primitive.md#datetime)値で、受信ファイルの作成と変更の日付と時間 (この例では `createdDateTime` と `modifiedDateTime` 変数)、およびこれらの日付を取得、設定する方法を指定します。 この値は、カスタム ソースで認識される受信ドキュメントの並べ替えやフィルター処理の実行時に使用されます。
    - カスタム ソースから受信ファイルを読み込む方法 (この例では `Load()` メソッド)。
    - カスタム ストレージに取り込んだファイルを削除する方法 (この例では `Delete()` メソッド)。
    - 受信ファイルに関する追加情報を公開する方法で (この例では `parmAdditionalInfo()` メソッド)、この情報を保存し、要求に応じて抽出することができます。

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using SL = Microsoft.Dynamics365.LocalizationFramework.XppSupportLayer;
    using System.IO;

    /// <summary>
    /// Import file
    /// </summary>
    public class ContosoInboundFile implements ERIImportFile
    {
        private str folderPath;
        private System.IO.Stream fileContent;
        private str additionalInfo;
        private str fileId;
        private str name;
        private SL.utcdatetime createdDateTime;
        private SL.utcdatetime modifiedDateTime;
        private str sourceSettingsKey;

        protected void new(
            str _fileId,
            str _name,
            utcdatetime _dateTime,
            str _folderPath,
            Stream _fileContent
            )
        {
            fileId = _fileId;
            name = _name;
            createdDateTime = ERLFConvert::fromUtcdatetime(_dateTime);
            modifiedDateTime =  ERLFConvert::fromUtcdatetime(_dateTime);
            folderPath = _folderPath;
            fileContent = _fileContent;
            this.set_SourceSettingsKey(ContosoInboundFileSourceSettings::SettingsKey);

        }

        [Hookable(false)]
        public str get_SourceSettingsKey()
        {
            return sourceSettingsKey;
        }

        [Hookable(false)]
        public void set_SourceSettingsKey(str _sourceSettingsKey = sourceSettingsKey)
        {
            sourceSettingsKey = _sourceSettingsKey;
        }

        [Hookable(false)]
        public str parmAdditionalInfo(str _additionalInfo = additionalInfo)
        {
            additionalInfo = _additionalInfo;
            return additionalInfo;
        }

        /// <summary>
        /// Construct new object.
        /// </summary>
        /// <param name = "_fileId">File id.</param>
        /// <param name = "_name">Name.</param>
        /// <param name = "_dateTime">Date time.</param>
        /// <param name = "_folderPath">Folder path.</param>
        /// <param name = "_fileContent">File content as stream.</param>
        /// <returns>Import file.</returns>
        public static ContosoInboundFile construct(str _fileId,
            str _name,
            utcdatetime _dateTime,
            str _folderPath,
            Stream _fileContent
            )
        {
            return new ContosoInboundFile(_fileId, _name, _dateTime, _folderPath, _fileContent);
        }

        [Hookable(false)]
        public void set_FileId(str _fileId = fileId)
        {
            fileId = _fileId;
        }

        [Hookable(false)]
        public void set_Name(str _name = name)
        {
            name = _name;
        }

        [Hookable(false)]
        public str get_Name()
        {
            return name;
        }

        [Hookable(false)]
        public SL.utcdatetime get_CreatedDateTime()
        {
            return createdDateTime;
        }

        [Hookable(false)]
        public void set_CreatedDateTime(SL.utcdatetime _createdDateTime = createdDateTime)
        {
            createdDateTime = _createdDateTime;
        }

        [Hookable(false)]
        public void set_ModifiedDateTime(SL.utcdatetime _modifiedDateTime = modifiedDateTime)
        {
            modifiedDateTime = _modifiedDateTime;
        }

        /// <summary>
        /// Loads the file from the source.
        /// </summary>
        /// <returns>A file operation result.</returns>
        public ERFileLoadResult Load()
        {
            return ERFileLoadResult::Success(fileContent);
        }

        public ERFileDeleteResult Delete()
        {
            if (System.IO.File::Exists(Path::Combine(folderPath, name)))
            {
                System.IO.File::Delete(Path::Combine(folderPath, name));
                return ERFileDeleteResult::Success();
            }
            return ERFileDeleteResult::Fail();
        }

        [Hookable(false)]
        public str GetFileId()
        {
            return fileId;
        }

        [Hookable(false)]
        public SL.utcdatetime GetModifiedDateTime()
        {
            return modifiedDateTime;
        }

    }
    ```

3. Visual Studio プロジェクトに新しいクラスを追加します。 この例では、`ContosoInboundFileSource` を使用します。
4. `ERIFileSource` パブリック インターフェイスを使用し、受信ファイルのカスタム ソースを説明するコードを書き込みます。 受信ファイルを処理する ER フレームワークの要件に準拠するために、次の情報を指定する必要があります。

    - ファイル マスク (この例では `fileMask` 変数) によって、ユーザーはファイル名のパターンを指定して、ファイル名と拡張子に基づいてカスタム ソースの特定のファイルだけをフィルター処理することができます。
    - カスタム ソースから受信ファイルを読み込む方法 (この例では `GetFiles()` メソッド)。 このメソッドは、受信ファイルを指定するための `ContosoInboundFile()` メソッドを指しています。

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using System.IO;

    /// <summary>
    /// File source as a folder
    /// </summary>
    public class ContosoInboundFileSource implements ERIFileSource
    {
        private str folderPath;
        private str fileMask;

        /// <summary>
        /// Creates a new instance of <C>ERFileSourceFolder</C>.
        /// </summary>
        /// <param name = "_folderPath">A folder path.</param>
        /// <param name = "_fileMask">A file mask to filter; optional.</param>
        protected void new(str _folderPath, str _fileMask)
        {
            folderPath = _folderPath;
            fileMask = _fileMask;
        }

        /// <summary>
        /// Construct new instance of <c>ERFileSourceFolder</c>.
        /// </summary>
        /// <param name = "_folderPath">A folder path.</param>
        /// <param name = "_fileMask">A file mask to filter; optional.</param>
        /// <returns>New instance of class.</returns>
        internal static ContosoInboundFileSource construct(str _folderPath, str _fileMask)
        {
            return new ContosoInboundFileSource(_folderPath, _fileMask);
        }

        public str parmFolderPath(str _value = folderPath)
        {
            folderPath = _value;
            return folderPath;
        }

        [Hookable(false)]
        public ERIFiles GetFiles()
        {
            if (fileMask == '')
            {
                fileMask = '*.*';
            }
            var ret = new ERFiles();
            var directoryInfo = new System.IO.DirectoryInfo(folderPath);
            var files = directoryInfo.GetFiles(fileMask);
            var i = files.GetEnumerator();

            while (i.MoveNext())
            {
                System.IO.FileInfo fileInfo = i.get_Current();
                if (fileInfo)
                {
                    using (StreamReader sr = fileInfo.OpenText())
                    {
                        var localStream = new System.IO.MemoryStream();

                        System.IO.Stream base = sr.BaseStream;
                        base.CopyTo(localStream);
                        if (localStream.CanSeek)
                        {
                            localStream.Seek(0, System.IO.SeekOrigin::Begin);
                        }
                        ERIFile file = ContosoInboundFile::construct(fileInfo.Name, fileInfo.Name, DateTimeUtil::getSystemDateTime(), folderPath, localStream);
                        ret.Add(file);

                    }
                }
            }
            return ret;
        }

    }
    ```

    > [!NOTE]
    > `GetFiles()` メソッドが呼び出され、ファイル オブジェクトが構築される際に、ファイル名は構成されたカスタム ソース内の固有のファイル識別子として使用されます。 受信ファイルの保存にローカル ファイル システム ソースのフォルダー以外を使用する場合は、別の方法を実装し受信ファイルを一意に識別することができます。

5. Visual Studio プロジェクトに新しいクラスを追加します。 この例では、`ContosoERFileDestinationFolder` を使用します。
6. `ERIFileDestination` パブリック インターフェイスを使用し、受信ファイルのカスタム ソースをフォルダーとして説明するコードを書き込みます。 [生成されるドキュメントに対するカスタム送信先を実装する](er-custom-file-destination.md#extend-the-source-code)の "ソース コードの拡張" の手順 1 にあるコード サンプルを再利用できます。 次の例では、クラスは、受信ドキュメントをローカル ファイル システムのフォルダー内のファイルとして検索するように設計されています。

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// File destination as a folder
    /// </summary>
    public class ContosoERFileDestinationFolder implements ERIFileDestination
    {
        private str folderPath;
        private boolean overwrite;

        public str parmFolderPath(str _value = folderPath)
        {
            folderPath = _value;
            return folderPath;
        }

        public boolean parmOverwrite(boolean _value = overwrite)
        {
            overwrite = _value;
            return overwrite;
        }

        [Hookable(false)]
        public System.IO.Stream saveFile(System.IO.Stream _stream, str _filePath)
        {
            this.sendFileToFolder(_stream, _filePath);
            return _stream;
        }

        [Hookable(false)]
        public System.IO.Stream newFileStream(str _filePath)
        {
            return new System.IO.MemoryStream();
        }

        private str getFileName(str _fileName)
        {
            if (overwrite)
            {
                return _fileName;
            }
            System.DateTime now = DateTimeUtil::utcNow();
            return strFmt('%1_%2%3', System.IO.Path::GetFileNameWithoutExtension(_fileName), now.ToString('yyyy-M-d_HH_mm_ss'), System.IO.Path::GetExtension(_fileName));
        }

        private void sendFileToFolder(System.IO.Stream _stream, str _filePath)
        {
            using(var fileStream = System.IO.File::Create(_filePath))
            {
                if( _stream.CanSeek)
                {
                    _stream.Seek(0, System.IO.SeekOrigin::Begin);
                }
                _stream.CopyTo(fileStream);
            }
        }

        /// <summary>
        /// Finalizes files processing.
        /// </summary>
        [Hookable(false)]
        public void finalize()
        {
        }

    }
    ```

7. Visual Studio プロジェクトに新しいクラスを追加します。 この例の場合、`ContosoInboundFileSourceSettings` を使用します。
8. `ERIImportFileSourceSettings` パブリック インターフェースを使用して、カスタム ソースの作成方法、そのパラメーターをストレージ用にパックする方法、およびユーザー インターフェイス (UI) に表示するためにパラメーターをアンパックする方法を指定するコードを書き込みます。 受信ファイルを処理する ER フレームワークの要件に準拠するために、次の情報を指定する必要があります。

    - 実行時にカスタム ソースの設定を一意に識別するキー (`SettingsKey` この例ではテキスト定数)。 このタイプのキーの一意性を保証するために、クラス名を使用することをお勧めします。
    - デザイン時に適切な UI ダイアログ ボックスにカスタム ソースを表示するためのカスタム ソースの名前 (この例では `Folder` テキスト定数)。
    - カスタム ソースがランタイムに使用できるように、デザイン時に有効になっているかどうかを示すパラメーター (この例では `isEnabled` 変数)。
    - これらのパラメータはすべて、アプリケーション データベース内の単一のバイナリ オブジェクトの一部として保存されなければならないため、デザイン時にこの目的のためにパックされ、実行時に要求されたときにアンパックされる必要があります。 このプロセスをサポートするために、適切なメソッドを実装する必要があります。
    - インポート済ファイルに適用される必要な後処理のロジックを実装するために使用される `fileImported()` メソッドに注意してください。 このメソッドの引数は、インポートしたファイル自体および実行されたインポートに関する情報を表します。 状態マネージャーが含まれています。 この状態マネージャには、インポートしたファイルが削除されたのか、別の場所に移動されたのかに関する情報を収集するロガーが含まれています。 この例では、コードは正常にインポートされたファイルをローカル ファイル システムの別のフォルダ (**C:\\InboundFiles\\アーカイブ**) に移動し、元のファイル名を維持しています。

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using System.IO;

    /// <summary>
    /// Folder file source settings
    /// </summary>
    public class ContosoInboundFileSourceSettings implements SysPackable, ERIImportFileSourceSettings
    {
        internal const str SettingsKey = classStr(ContosoInboundFileSourceSettings);
        public const int CurrentVersion = 1;

        private boolean isEnabled;
        private str folderPath;

        [Hookable(false)]
        public str parmFolderPath(str _value = folderPath)
        {
            folderPath = _value;
            return folderPath;
        }

        [Hookable(false)]
        public boolean parmIsEnabled(boolean _value = isEnabled)
        {
            isEnabled = _value;
            return isEnabled;
        }

        [Hookable(false)]
        public void setEnabled(boolean _value)
        {
            isEnabled = _value;
        }

        [Hookable(false)]
        public boolean isEnabled()
        {
            return isEnabled;
        }

        [Hookable(false)]
        public str getName()
        {
            /// Name of settings of a custom source. 
            /// This name will be presented in the dialog box that is offered at runtime for user to adjust configured settings.
            return 'Folder';
        }

        [Hookable(false)]
        public boolean validate()
        {
            return true;
        }

        [Hookable(false)]
        public str getKey()
        {
            return SettingsKey;
        }

        [Hookable(false)]
        public container pack()
        {
            return [CurrentVersion, isEnabled, folderPath];
        }

        [Hookable(false)]
        public boolean unpack(container packedClass)
        {
            int version = RunBase::getVersion(packedClass);
            switch (version)
            {
                case CurrentVersion:
                    [version, isEnabled, folderPath] = packedClass;
                    return true;
                default:
                    return false;
            }
        }

        /// <summary>
        /// Creates a file source for current settings.
        /// </summary>
        /// <param name = "_fileMask">File mask.</param>
        /// <returns>A new instance of a file source.</returns>
        public ERIFileSource createFileSource(str _fileMask)
        {
            return ContosoInboundFileSource::construct(folderPath, _fileMask);
        }

        /// <summary>
        /// Creates a file destination for current settings.
        /// </summary>
        /// <param name = "_destination">A destination folder to move the file.</param>
        /// <returns>A new instance of a file destination.</returns>
        private ERIFileDestination createPostProcessingDestination(ERFormatFileDestinationAfterImport _destination)
        {
            ContosoERFileDestinationFolder ret = new ContosoERFileDestinationFolder();
            var path = folderPath;
            switch (_destination)
            {
                case ERFormatFileDestinationAfterImport::None :
                    break;
                default:
                    path = System.IO.Path::Combine(path, enum2Str(_destination));
                    break;
            }
            ret.parmFolderPath(path);
            return ret;
        }

        public void fileImported(ERFileImportedArgs _args)
        {
            if (_args.IsImportOperationSuccessful())
            {
                /// copy an outbound file to the alternative location
                var destination = this.createPostProcessingDestination( _args.IsImportOperationSuccessful() ? ERFormatFileDestinationAfterImport::Archive : ERFormatFileDestinationAfterImport::None);
                ERIImportFile file = _args.getFile();
                destination.saveFile(_args.getFileStream(), @'C:\InboundFiles\Archive\'+file.Name);

                /// do logging
                ttsbegin;
                _args.getState().markAsMoved();
                _args.getState().getLogger().logMoved(!_args.IsImportOperationSuccessful(), 'Custom error message', 'Custom description');
                ttscommit;

                /// delete file
                ttsbegin;
                _args.getFile().Delete();
                _args.getState().markAsDeleted();
                ttscommit;
            }      
        }

        /// <summary>
        /// Create new instance of <c>ERImportFormatSourceFolderSettings</c> from packed presentation.
        /// </summary>
        /// <param name = "_packedClass">A container with packed presentation.</param>
        /// <returns>New instance.</returns>
        internal static ContosoInboundFileSourceSettings create(container _packedClass)
        {
            var settings = new ContosoInboundFileSourceSettings();
            settings.unpack(_packedClass);
            return settings;
        }

        /// <summary>
        /// Event.
        /// </summary>
        /// <param name="_record">Record.</param>
        /// <param name="_file">File.</param>
        ///
        /// This code and code below presents the sample how you can memorize additional info about an imported file
        /// in the extended field of the ERImportFormatFileSourceStateTable table.
        /// 
        [SubscribesTo(tableStr(ERImportFormatFileSourceStateTable), delegateStr(ERImportFormatFileSourceStateTable, objectInitialized))]
        public static void ERImportFormatFileSourceStateTable_objectInitialized(ERImportFormatFileSourceStateTable _record, ERIImportFile _file)
        {
            anytype file =_file;
            var folderFile = file as ContosoInboundFile;
            if (folderFile != null)
            {
    ///            folderFile.parmAdditionalInfo(_record.additionalInfo);
            }
        }

        /// <summary>
        /// Event.
        /// </summary>
        /// <param name="_record">Record.</param>
        /// <param name="_file">File</param>
        [SubscribesTo(tableStr(ERImportFormatFileSourceStateTable), delegateStr(ERImportFormatFileSourceStateTable, tableRecordInitialized))]
        public static void ERImportFormatFileSourceStateTable_tableRecordInitialized(ERImportFormatFileSourceStateTable _record, ERIImportFile _file)
        {
            anytype file =_file;
            var folderFile = file as ContosoInboundFile;
            if (folderFile != null)
            {
    ///            _record.AdditionalInfo = folderFile.parmAdditionalInfo();
            }
        }

    }
    ```

9. Visual Studio プロジェクトで、`ERImportFormatSourceSettings` フォームの新しい拡張機能を追加します。 この例では、`ERImportFormatSourceSettings.ContosoCustomFileSource` を使用します。
10. 受信ファイルのカスタム ソースのカスタム UI を実装するコードを書き込みます。 次の図は、この UI が Visual Studio デザイナーでどのように表示されるかを示しています。

    ![Visual Studio デザイナーのカスタム UI。](media/er-custom-file-source-form-extension.png)

11. Visual Studio プロジェクトに新しいクラスを追加します。 この例の場合、`ContosoImportFormatSourceSettingsEventHandlers` を使用します。
12. カスタム ソースの拡張形式設定のためのイベント ハンドラー コードを書き込みます。 この手順は、パブリック `ERIImportFileSourceSettingsStorage` インターフェイス を実装する必要があります。

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// Handler for <c>ERImportFormatSourceSettings</c> form
    /// </summary>
    public class ContosoImportFormatSourceSettingsEventHandlers
    {
        /// <summary>
        /// Post init method event handler.
        /// </summary>
        /// <param name = "args">Args.</param>
        [PostHandlerFor(formStr(ERImportFormatSourceSettings), formMethodStr(ERImportFormatSourceSettings, init))]
        public static void ERImportFormatSourceSettings_Post_init(XppPrePostArgs args)
        {
            FormRun formRun = args.getThis();
            ERIImportFileSourceSettingsStorage settingsStorage = args.getThis();
            var settings = ContosoImportFormatSourceSettingsEventHandlers::getSaveInFolderSettings(settingsStorage);

            FormStringControl folderPathControl = formRun.design().controlName(formControlStr(ERImportFormatSourceSettings, ContosoFolder_FolderPath));
            folderPathControl.text(settings.parmFolderPath());

            FormCheckBoxControl enabledControl = formRun.design().controlName(formControlStr(ERImportFormatSourceSettings, ContosoFolderEnable));
            enabledControl.checked(settings.isEnabled());

        }

        /// <summary>
        /// CloseOk method event handler.
        /// </summary>
        /// <param name = "args">Args.</param>
        [PreHandlerFor(formStr(ERImportFormatSourceSettings), formMethodStr(ERImportFormatSourceSettings, closeOk))]
        public static void ERFormatDestinationSettings_Pre_closeOk(XppPrePostArgs args)
        {
            FormRun formRun = args.getThis();
            ERIImportFileSourceSettingsStorage settingsStorage = args.getThis();
            var settings = ContosoImportFormatSourceSettingsEventHandlers::getSaveInFolderSettings(settingsStorage);

            FormStringControl folderPathControl = formRun.design().controlName(formControlStr(ERImportFormatSourceSettings, ContosoFolder_FolderPath));
            settings.parmFolderPath(folderPathControl.text());

            FormCheckBoxControl enabledControl = formRun.design().controlName(formControlStr(ERImportFormatSourceSettings, ContosoFolderEnable));
            settings.setEnabled(enabledControl.checked());
            
        }

        private static ContosoInboundFileSourceSettings getSaveInFolderSettings(ERIImportFileSourceSettingsStorage _settingsStorage)
        {
            ContosoInboundFileSourceSettings ret = _settingsStorage.getSettingsByKey(ContosoInboundFileSourceSettings::SettingsKey);
            if (ret == null)
            {
                ret = new ContosoInboundFileSourceSettings();
                _settingsStorage.addSettings(ret);
            }
            return ret;
        }

    }
    ```

13. Visual Studio プロジェクトを再構築します。

## <a name="configure-er-sources-for-the-imported-er-format"></a>インポートした ER 形式の ER ソースを構成する

1. インポートした ER 形式の前述したいずれかのコンポーネント (一般\\ファイルまたは Excel\\ファイル) のために受信ファイルのカスタム ソースを構成します。

    1. **組織管理** \> **電子申告** \> **電子申告ソース** に移動します。
    2. **電子申告ソース** ページで、**新規** タブを選択します。
    3. **形式** フィールドで、インポートした ER 形式を選択します。
    4. **ファイル ソース** クイックタブで、**新規** を選択し、次の手順に従います:

        1. **名前** フィールドに、カスタム ソースの名前として **ローカル フォルダーから** と入力します。
        2. **ファイル名マスク** フィールドに、**_.xlsx_* マスクを入力すると、カスタム ソースで拡張機能が .xlsx のファイルのみをフィルター処理することができます。
        3. **ファイルをインポート前に並べ替える** フィールドで **変更した日付/時間で並べ替える** を選択します。

    4. 入力したソース レコードについて、**設定** オプションを選択し、次の手順に従います。

        1. 表示される **ソース設定** ダイアログ ボックスの **Contoso カスタマー ファイル ソース** タブで、**有効** オプションを **はい** に設定します。
        2. **パス** フィールドに **C:\\InboundFiles\\ソース** を入力し、受信ファイルを含むローカル フォルダーを指定します。
        3. **OK** を選択してから、**保存** を選択します。

    ![ソース設定ダイアログ ボックスで、受信ファイルのカスタム ソースを構成する。](media/er-custom-file-source-setting-folder.png)

2. インポートしたファイル **1099import-data.xlsx** を、アプリケーション オブジェクト サーバー (AOS) の最初のインスタンスを実行しているサーバーのファイル システム **C:\\InboundFiles\\ソース** のフォルダーにコピーします。
3. 最初の AOS インスタンスを実行するサーバーのファイル システムに、**C:\\InboundFiles\\アーカイブ** フォルダーされていることを確認してください。
4. **電子申告ソース** ページで、**ソースのファイル状態** を選択し、次の手順に従って現在の ER 形式用に構成されたカスタム ファイル ソースのコンテンツを確認します。

    1. **ソースのファイルの状態** ページの、**ファイル ソース** リストで **ローカル フォルダーから** を選択します。
    2. **ファイル** タブで **更新** を選択して、カスタム ソースからインポートする準備が出来ている **1099import-data.xlsx** ファイルを表示します。

    ![ソースのファイルの状態ページで、カスタム ファイル ソースのファイルの状態を確認します。](media/er-custom-file-source-files-state.png)

## <a name="run-the-er-mapping-that-you-imported"></a>インポートした ER マッピングを実行する

1. カスタム ソースにある受信ファイルから仕入先トランザクションをインポートするには、次の手順に従って、インポートした ER モデル マッピングを実行します。

    1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
    2. **構成** ツリーで、**1099 支払いモデル** を選択します。
    3. **コンポーネントの構成** クイックタブで、**モデル マッピング** コンポーネントの名前を選択して、選択した ER モデル構成のモデル マッピングのリストを開きます。
    5. **実行** を選択し、選択したモデル マッピングを実行します。 ER 形式のファイル ソースを構成したので、必要に応じて **ファイル ソース** オプションの設定を変更できます。 このオプション設定を維持すると、.xslx ファイルは設定されたカスタム ソースからインポートされます (この例では、**C:\\InboundFiles\\ソース** ローカル フォルダーの **1099import-data.xlsx** ファイル)。
    6. **V-00001** などの伝票 ID を入力し、**OK** を選択します。

    ![ER モデル マッピングを実行して、カスタム ソースにある .xlsx ファイルからデータをインポートします。](./media/er-custom-file-source-run-model-mapping.png)

2. ローカル **C:\\InboundFiles\\アーカイブ** フォルダーを参照し、ソース コードで定義されている後処理ロジックに基づいて、**C:\\InboundFiles\\ソース** ローカル フォルダーから移動されたインポート済みの **1099import-data.xlsx** ファイルを検索します。
3. 次の手順に従って、構成済み受信ファイルのカスタム ソースの現在の状態を確認します。

    1. **組織管理** \> **電子申告** \> **電子申告ソース** に移動します。
    2. **電子申告ソース** ページで、**ソースのファイル状態** を選択して、現在の ER 形式の構成済みカスタム ファイル ソースのコンテンツを確認します。
    3. **ソースのファイルの状態** ページの、**ファイル ソース** リストで **ローカル フォルダーから** を選択します。
    4. **ファイル** タブで **最新の情報に更新** を選択して、以前にインポートされ **C:\\InboundFiles\\ソース** フォルダーから **C:\\InboundFiles\\アーカイブ** フォルダーに移動した **1099import-data.xlsx** ファイルを表示します。

    ![ファイルのインポート後、ソースのファイルの状態ページで、カスタム ファイル ソースのファイルの状態を確認します。](media/er-custom-file-source-files-state2.png)

## <a name="additional-resources"></a>追加リソース

[SharePoint からのデータ インポートの構成](er-configure-data-import-sharepoint.md)

[Application update 10.0.23 での電子申告フレームワーク API の変更](er-apis-app10-0-23.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
