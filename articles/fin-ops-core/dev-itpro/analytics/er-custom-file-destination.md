---
title: 生成されるドキュメントに対するカスタム送信先の実装
description: この記事では、電子申告 (ER) 形式で生成されたドキュメントを格納する ER 送信先リストを拡張する方法について説明します。
author: NickSelin
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERFormatDestinationTable, ERParameters
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: da3e09c15c336301ec3b17b313afc9e96bf4cd1a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864763"
---
# <a name="implement-a-custom-destination-for-generated-documents"></a>生成されるドキュメントに対するカスタム 送信先の実装

[!include[banner](../includes/banner.md)]

[電子申告 (ER)](general-electronic-reporting.md) フレームワークのアプリケーション プログラミング インターフェイス (API) により、ER 形式で生成されるドキュメントを格納する ER 送信先のリストを[拡張](er-apis-app10-0-19.md#er-api-extend-destination) できます。 この記事には、カスタマイズされた ER 送信先を実装するために完了する必要のある主要なタスクに関する概要が含まれます。

## <a name="prerequisites"></a>必要条件

継続的ビルドをサポートするトポロジを配置する必要があります。 詳細については、[継続的ビルドとテストの自動化をサポートするトポロジの配置](../perf-test/continuous-build-test-automation.md)を参照してください。 次のいずれかのロールに対応するこのトポロジにアクセスできる必要があります:

- 電子申告開発者
- 電子申告機能コンサルタント
- システム管理者

また、このトポロジの開発環境にもアクセスできる必要があります。

## <a name="create-or-import-an-er-format-configuration"></a>ER フォーマット構成の作成またはインポート

現在のトポロジでは、[新しい ER フォーマットを作成](tasks/er-format-configuration-2016-11.md) して、カスタマイズされた ER 送信先を使用して格納したいドキュメントを生成します。 または、[既存の ER フォーマットをこのトポロジにインポート](general-electronic-reporting-manage-configuration-lifecycle.md) できます。

![形式デザイナー ページで ER 形式の構造を確認する。](media/er-custom-file-destination-format-structure.png)

> [!IMPORTANT]
> 作成またはインポートする ER フォーマットには、次のフォーマット エレメントのうち少なくとも 1 つを含める必要があります。
>
> - Common\\File
> - Common\\File attachment
> - Common\\Folder
> - Excel\\File 
> - PDF\\Merger
> - PDF\\File

## <a name="extend-the-source-code"></a>ソース コードの拡張

1. Microsoft Visual Studio プロジェクトに新しいクラス (この例では `ERFileDestinationFolder`) を追加し、`ERIFileDestination` パブリック インターフェイスを使用してカスタム送信先を実装するコードを記述します。 次の例では、クラスは、生成されたドキュメントをローカル ファイル システムのフォルダーにファイルとして格納するように設計されています。

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    public class ERFileDestinationFolder implements ERIFileDestination
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
            this.sendFileToFolder(_stream, System.IO.Path::GetFileName(_filePath));
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

        private void sendFileToFolder(System.IO.Stream _stream, str _fileName)
        {
            var resultPath = System.IO.Path::Combine(this.folderPath, this.getFileName(_fileName));
            using(var fileStream = System.IO.File::Create(resultPath))
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

2. Visual Studio プロジェクト (この例では `ERFormatDestinationSaveInFolderSettings`) に新しいクラスを追加し、`ERIFormatFileDestinationSettings` パブリック インターフェイスを使用して、カスタム送信先の作成方法、パラメーターをストレージ用にパックする方法、およびパラメーターをユーザー インターフェイス (UI) に表示するためにアンパックする方法を指定するコードを記述します。

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    public class ERFormatDestinationSaveInFolderSettings implements ERIFormatFileDestinationSettings
    {
        internal const str SettingsKey = classStr(ERFormatDestinationSaveInFolderSettings);
        public const int CurrentVersion = 1;

        private boolean isEnabled;
        private boolean overwrite;
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
        public boolean parmOverwrite(boolean _value = overwrite)
        {
            overwrite = _value;
            return overwrite;
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
            return 'Save in folder';
        }

        [Hookable(false)]
        public void validate()
        {
        }

        [Hookable(false)]
        public ERIFileDestination createDestination(ERDestinationExecutionContext _destinationContext, boolean _isGrouped)
        {
            ERFileDestinationFolder ret = new ERFileDestinationFolder();
            ret.parmFolderPath(this.parmFolderPath());
            ret.parmOverwrite(this.parmOverwrite());
            return ret;
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
        /// Creates a new instance of an objected from a packed class container.
        /// </summary>
        /// <param name = "_packedClass">A packed class container.</param>
        /// <returns>The new instance of an object.</returns>
        public static ERFormatDestinationSaveInFolderSettings create(container _packedClass)
        {
            var ret = new ERFormatDestinationSaveInFolderSettings();
            ret.unpack(_packedClass);
            return ret;
        }
    }
    ```

    > [!NOTE]
    > 上記のコードでは、`ERFormatDestinationSaveInFolderSettings` クラスが `static` クラスとして導入されます。 実装オブジェクトには、オブジェクトを作成し、オブジェクトが正しくパックおよび展開プロセスに必要なコンテナーを展開する `static create(container)` メソッドが必要です。 詳細については[パック-アンパック デザイン パターン](/dynamicsax-2012/developer/pack-unpack-design-pattern#aa879675collapse_allen-usax60gifpublic-static-yourclass-createcontainer-_packedobject) を参照してください 。

3. Visual Studio プロジェクトで、`ERFormatDestinationSettings` フォームに新しい拡張子を追加し、カスタム送信先のカスタム UI を実装するコードを記述します。 次の図は、この UI が Visual Studio デザイナーでどのように表示されるかを示しています。

    ![Visual Studio デザイナーでカスタム UI を確認する。](media/er-custom-file-destination-form-extension.png)

4. Visual Studio プロジェクトに新しいクラス (この例では、`ERFormatDestinationSettingsEventHandlers`) を追加し、拡張送信先フォームのイベント ハンドラー コードを記述します。 この手順は、パブリック `ERIFormatFileDestinationSettingsStorage` インターフェイス を実装する必要があります。

    ```xpp
    public class ERFormatDestinationSettingsEventHandlers
    {
        [PostHandlerFor(formStr(ERFormatDestinationSettings), formMethodStr(ERFormatDestinationSettings, init))]
        public static void ERFormatDestinationSettings_Post_init(XppPrePostArgs args)
        {
            FormRun formRun = args.getThis();
            ERIFormatFileDestinationSettingsStorage settingsStorage = args.getThis();
            var settings = ERFormatDestinationSettingsEventHandlers::getSaveInFolderSettings(settingsStorage);

            FormStringControl folderPathControl = formRun.design().controlName(formControlStr(ERFormatDestinationSettings, SaveInFolder_FolderPath));
            folderPathControl.text(settings.parmFolderPath());

            FormCheckBoxControl enabledControl = formRun.design().controlName(formControlStr(ERFormatDestinationSettings, SaveInFolderEnable));
            enabledControl.checked(settings.isEnabled());

            FormCheckBoxControl overwriteControl = formRun.design().controlName(formControlStr(ERFormatDestinationSettings, SaveInFolder_Overwrite));
            overwriteControl.checked(settings.parmOverwrite());
        }

        [PreHandlerFor(formStr(ERFormatDestinationSettings), formMethodStr(ERFormatDestinationSettings, closeOk))]
        public static void ERFormatDestinationSettings_Pre_closeOk(XppPrePostArgs args)
        {
            FormRun formRun = args.getThis();
            ERIFormatFileDestinationSettingsStorage settingsStorage = args.getThis();
            var settings = ERFormatDestinationSettingsEventHandlers::getSaveInFolderSettings(settingsStorage);

            FormStringControl folderPathControl = formRun.design().controlName(formControlStr(ERFormatDestinationSettings, SaveInFolder_FolderPath));
            settings.parmFolderPath(folderPathControl.text());

            FormCheckBoxControl enabledControl = formRun.design().controlName(formControlStr(ERFormatDestinationSettings, SaveInFolderEnable));
            settings.setEnabled(enabledControl.checked());
            
            FormCheckBoxControl overwriteControl = formRun.design().controlName(formControlStr(ERFormatDestinationSettings, SaveInFolder_Overwrite));
            settings.parmOverwrite(overwriteControl.checked());
        }

        private static ERFormatDestinationSaveInFolderSettings getSaveInFolderSettings(ERIFormatFileDestinationSettingsStorage _settingsStorage)
        {
            ERFormatDestinationSaveInFolderSettings ret = _settingsStorage.getSettingsByKey(ERFormatDestinationSaveInFolderSettings::SettingsKey);
            if (ret == null)
            {
                ret = new ERFormatDestinationSaveInFolderSettings();
                _settingsStorage.addSettings(ret);
            }
            return ret;
        }
    }
    ```

5. Visual Studio プロジェクトを再構築します。

## <a name="configure-er-destinations-for-the-er-format-that-you-created-or-imported"></a>作成またはインポートした ER 形式の ER の出力送信先を構成する

1. 作成またはインポートした ER 形式について、前述のコンポーネント (ファイル、フォルダー、マージ、または添付ファイル) の 1 つに対して[アーカイブ](er-destination-type-archive.md) 送信先を構成します。 詳細については、[ER ER コンフィギュレーション先](tasks/er-destinations-2016-11.md) を参照してください。

    ![送信先の設定ダイアログ ボックスでのアーカイブ先のコンフィギュレーション。](media/er-custom-file-destination-destination-setting-archive.png)

2. 選択した ER 形式の同じコンポーネントについて、カスタムの **フォルダーに保存** の保存先を有効にして構成します。

    ![送信先の設定ダイアログ ボックスでのフォルダーに保存の保存先のコンフィギュレーション。](media/er-custom-file-destination-destination-setting-custom.png)

    > [!NOTE] 
    > AOS サービスを実行するサーバーのローカル ファイル システムに、指定したカスタム送信先フォルダー (この例では **c:\\0**) が存在することを確認してください。 それ以外の場合は、[DirectoryNotFoundException](/dotnet/api/system.io.directorynotfoundexception) 例外が実行時にスローされます。

## <a name="run-the-er-format-that-you-created-or-imported"></a>作成またはインポートした ER フォーマットの実行

1. 作成またはインポートした ER 形式を実行します。
2. **組織管理 \> 電子申告 \> 電子申告ジョブ** に移動し、この実行ジョブに対して作成され、生成されたファイルが関連付けられているレコードを検索します。
3. ローカルの **C:\\0** フォルダーを参照して、生成ファイルを見つけます。

## <a name="additional-resources"></a>追加リソース

[電子申告 (ER) の送信先](electronic-reporting-destinations.md)

[Application update 10.0.19 での電子申告フレームワーク API の変更](er-apis-app10-0-19.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
