---
title: 生成されるドキュメントに対するカスタム 送信先の実装
description: このトピックでは、電子申告 (ER) 形式で生成されたドキュメントを格納する ER 送信先リストを拡張する方法について説明します。
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
ms.openlocfilehash: 40016f7b537c71c5ea891f38179f3c76d9bf7ebe
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193580"
---
# <a name="implement-a-custom-destination-for-generated-documents"></a><span data-ttu-id="5d093-103">生成されるドキュメントに対するカスタム 送信先の実装</span><span class="sxs-lookup"><span data-stu-id="5d093-103">Implement a custom destination for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5d093-104">[電子申告 (ER)](general-electronic-reporting.md) フレームワークのアプリケーション プログラミング インターフェイス (API) により、ER [形式](general-electronic-reporting.md#FormatComponentOutbound) で生成されたドキュメントを格納する ER 送信先のリストを[拡張](er-apis-app10-0-19.md#er-api-extend-destination) することができます。</span><span class="sxs-lookup"><span data-stu-id="5d093-104">The application programming interface (API) of the [Electronic reporting (ER)](general-electronic-reporting.md) framework lets you [extend](er-apis-app10-0-19.md#er-api-extend-destination) the list of ER destinations that you can use to store documents that ER [formats](general-electronic-reporting.md#FormatComponentOutbound) generate.</span></span> <span data-ttu-id="5d093-105">このトピックには、カスタマイズされた ER 送信先を実装するために完了する必要のある主要なタスクに関する概要が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5d093-105">This topic includes an overview of the main tasks that you must complete to implement a custom ER destination.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5d093-106">必要条件</span><span class="sxs-lookup"><span data-stu-id="5d093-106">Prerequisites</span></span>

<span data-ttu-id="5d093-107">継続的ビルドをサポートするトポロジを配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d093-107">You must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="5d093-108">詳細については、[継続的ビルドとテストの自動化をサポートするトポロジの配置](../perf-test/continuous-build-test-automation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d093-108">For more information, see [Deploy topologies that support continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span> <span data-ttu-id="5d093-109">次のいずれかのロールに対応するこのトポロジにアクセスできる必要があります:</span><span class="sxs-lookup"><span data-stu-id="5d093-109">You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="5d093-110">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="5d093-110">Electronic reporting developer</span></span>
- <span data-ttu-id="5d093-111">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="5d093-111">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="5d093-112">システム管理者</span><span class="sxs-lookup"><span data-stu-id="5d093-112">System administrator</span></span>

<span data-ttu-id="5d093-113">また、このトポロジの開発環境にもアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d093-113">You must also have access to the development environment for this topology.</span></span>

## <a name="create-or-import-an-er-format-configuration"></a><span data-ttu-id="5d093-114">ER フォーマット構成の作成またはインポート</span><span class="sxs-lookup"><span data-stu-id="5d093-114">Create or import an ER format configuration</span></span>

<span data-ttu-id="5d093-115">現在のトポロジでは、[新しい ER フォーマットを作成](tasks/er-format-configuration-2016-11.md) して、カスタマイズされた ER 送信先を使用して格納したいドキュメントを生成します。</span><span class="sxs-lookup"><span data-stu-id="5d093-115">In the current topology, [create a new ER format](tasks/er-format-configuration-2016-11.md) to generate the documents that you plan to store by using a custom ER destination.</span></span> <span data-ttu-id="5d093-116">または、[既存の ER フォーマットをこのトポロジにインポート](general-electronic-reporting-manage-configuration-lifecycle.md) できます。</span><span class="sxs-lookup"><span data-stu-id="5d093-116">Alternatively, you can [import an existing ER format into this topology](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![形式デザイナーのページで ER 形式の構造を確認する](media/er-custom-file-destination-format-structure.png)

> [!IMPORTANT]
> <span data-ttu-id="5d093-118">作成またはインポートする ER フォーマットには、次のフォーマット エレメントのうち少なくとも 1 つを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d093-118">The ER format that you create or import must contain at least one of the following format elements:</span></span>
>
> - <span data-ttu-id="5d093-119">Common\\File</span><span class="sxs-lookup"><span data-stu-id="5d093-119">Common\\File</span></span>
> - <span data-ttu-id="5d093-120">Common\\File attachment</span><span class="sxs-lookup"><span data-stu-id="5d093-120">Common\\File attachment</span></span>
> - <span data-ttu-id="5d093-121">Common\\Folder</span><span class="sxs-lookup"><span data-stu-id="5d093-121">Common\\Folder</span></span>
> - <span data-ttu-id="5d093-122">Excel\\File</span><span class="sxs-lookup"><span data-stu-id="5d093-122">Excel\\File</span></span> 
> - <span data-ttu-id="5d093-123">PDF\\Merger</span><span class="sxs-lookup"><span data-stu-id="5d093-123">PDF\\Merger</span></span>
> - <span data-ttu-id="5d093-124">PDF\\File</span><span class="sxs-lookup"><span data-stu-id="5d093-124">PDF\\File</span></span>

## <a name="extend-the-source-code"></a><span data-ttu-id="5d093-125">ソース コードの拡張</span><span class="sxs-lookup"><span data-stu-id="5d093-125">Extend the source code</span></span>

1. <span data-ttu-id="5d093-126">Microsoft Visual Studio プロジェクトに新しいクラス (この例では `ERFileDestinationFolder`) を追加し、`ERIFileDestination` パブリック インターフェイスを使用してカスタム送信先を実装するコードを記述します。</span><span class="sxs-lookup"><span data-stu-id="5d093-126">Append your Microsoft Visual Studio project with a new class (`ERFileDestinationFolder` in this example), and write code that uses the `ERIFileDestination` public interface to implement your custom destination.</span></span> <span data-ttu-id="5d093-127">次の例では、クラスは、生成されたドキュメントをローカル ファイル システムのフォルダーにファイルとして格納するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="5d093-127">In the following example, the class is designed to store generated documents as files in a folder of the local file system.</span></span>

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

2. <span data-ttu-id="5d093-128">Visual Studio プロジェクト (この例では `ERFormatDestinationSaveInFolderSettings`) に新しいクラスを追加し、`ERIFormatFileDestinationSettings` パブリック インターフェイスを使用して、カスタム送信先の作成方法、パラメーターをストレージ用にパックする方法、およびパラメーターをユーザー インターフェイス (UI) に表示するためにアンパックする方法を指定するコードを記述します。</span><span class="sxs-lookup"><span data-stu-id="5d093-128">Add a new class to your Visual Studio project (`ERFormatDestinationSaveInFolderSettings` in this example) to use the `ERIFormatFileDestinationSettings` public interface to write code that specifies how a custom destination is created, how its parameters are packed for storage, and how its parameters are unpacked for presentation in the user interface (UI).</span></span>

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
    > <span data-ttu-id="5d093-129">上記のコードでは、`ERFormatDestinationSaveInFolderSettings` クラスが `static` クラスとして導入されます。</span><span class="sxs-lookup"><span data-stu-id="5d093-129">In the preceding code, the `ERFormatDestinationSaveInFolderSettings` class is introduced as the `static` class.</span></span> <span data-ttu-id="5d093-130">実装オブジェクトには、オブジェクトを作成し、オブジェクトが正しくパックおよび展開プロセスに必要なコンテナーを展開する `static create(container)` メソッドが必要です。</span><span class="sxs-lookup"><span data-stu-id="5d093-130">The implementation object should have a `static create(container)` method that creates an object and unpacks the container that the object requires for a correct pack-unpack process.</span></span> <span data-ttu-id="5d093-131">詳細については[パック-アンパック デザイン パターン](/dynamicsax-2012/developer/pack-unpack-design-pattern#aa879675collapse_allen-usax60gifpublic-static-yourclass-createcontainer-_packedobject) を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="5d093-131">For more information, see [Pack-Unpack Design Pattern](/dynamicsax-2012/developer/pack-unpack-design-pattern#aa879675collapse_allen-usax60gifpublic-static-yourclass-createcontainer-_packedobject).</span></span>

3. <span data-ttu-id="5d093-132">Visual Studio プロジェクトで、`ERFormatDestinationSettings` フォームに新しい拡張子を追加し、カスタム送信先のカスタム UI を実装するコードを記述します。</span><span class="sxs-lookup"><span data-stu-id="5d093-132">In your Visual Studio project, add a new extension for the `ERFormatDestinationSettings` form, and write code that implements a custom UI for your custom destination.</span></span> <span data-ttu-id="5d093-133">次の図は、この UI が Visual Studio デザイナーでどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="5d093-133">The following illustration shows what this UI looks like in the Visual Studio designer.</span></span>

    ![Visual Studio デザイナーでカスタム UI の 確認](media/er-custom-file-destination-form-extension.png)

4. <span data-ttu-id="5d093-135">Visual Studio プロジェクトに新しいクラス (この例では、`ERFormatDestinationSettingsEventHandlers`) を追加し、拡張送信先フォームのイベント ハンドラー コードを記述します。</span><span class="sxs-lookup"><span data-stu-id="5d093-135">Add another new class (`ERFormatDestinationSettingsEventHandlers` in this example) to your Visual Studio project, and write the event handler code for an extended destination form.</span></span> <span data-ttu-id="5d093-136">この手順は、パブリック `ERIFormatFileDestinationSettingsStorage` インターフェイス を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d093-136">This step requires that the public `ERIFormatFileDestinationSettingsStorage` interface be implemented.</span></span>

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

5. <span data-ttu-id="5d093-137">Visual Studio プロジェクトを再構築します。</span><span class="sxs-lookup"><span data-stu-id="5d093-137">Rebuild your Visual Studio project.</span></span>

## <a name="configure-er-destinations-for-the-er-format-that-you-created-or-imported"></a><span data-ttu-id="5d093-138">作成またはインポートした ER 形式の ER の出力送信先を構成する</span><span class="sxs-lookup"><span data-stu-id="5d093-138">Configure ER destinations for the ER format that you created or imported</span></span>

1. <span data-ttu-id="5d093-139">作成またはインポートした ER 形式について、前述のコンポーネント (ファイル、フォルダー、マージ、または添付ファイル) の 1 つに対して[アーカイブ](er-destination-type-archive.md) 送信先を構成します。</span><span class="sxs-lookup"><span data-stu-id="5d093-139">Configure the [Archive](er-destination-type-archive.md) destination for one of the previously mentioned components (file, folder, merger, or attachment) of the ER format that you created or imported.</span></span> <span data-ttu-id="5d093-140">詳細については、[ER ER コンフィギュレーション先](tasks/er-destinations-2016-11.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d093-140">For more information, see [ER Configure destinations](tasks/er-destinations-2016-11.md).</span></span>

    ![送信先の設定ダイアログ ボックスでのアーカイブ先を構成](media/er-custom-file-destination-destination-setting-archive.png)

2. <span data-ttu-id="5d093-142">選択した ER 形式の同じコンポーネントについて、カスタムの **フォルダーに保存** の保存先を有効にして構成します。</span><span class="sxs-lookup"><span data-stu-id="5d093-142">For the same component of the selected ER format, enable and configure the custom **Save in folder** destination.</span></span>

    ![送信先の設定ダイアログ ボックスでのフォルダーに保存の保存先を構成](media/er-custom-file-destination-destination-setting-custom.png)

    > [!NOTE] 
    > <span data-ttu-id="5d093-144">AOS サービスを実行するサーバーのローカル ファイル システムに、指定したカスタム送信先フォルダー (この例では **c:\\0**) が存在することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="5d093-144">Make sure that the specified custom destination folder (**c:\\0** in this example) is present in the local file system of the server that runs the AOS service.</span></span> <span data-ttu-id="5d093-145">それ以外の場合は、[DirectoryNotFoundException](/dotnet/api/system.io.directorynotfoundexception) 例外が実行時にスローされます。</span><span class="sxs-lookup"><span data-stu-id="5d093-145">Otherwise, a [DirectoryNotFoundException](/dotnet/api/system.io.directorynotfoundexception) exception will be thrown at runtime.</span></span>

## <a name="run-the-er-format-that-you-created-or-imported"></a><span data-ttu-id="5d093-146">作成またはインポートした ER フォーマットの実行</span><span class="sxs-lookup"><span data-stu-id="5d093-146">Run the ER format that you created or imported</span></span>

1. <span data-ttu-id="5d093-147">作成またはインポートした ER 形式を実行します。</span><span class="sxs-lookup"><span data-stu-id="5d093-147">Run the ER format that you created or imported.</span></span>
2. <span data-ttu-id="5d093-148">**組織管理 \> 電子申告 \> 電子申告ジョブ** に移動し、この実行ジョブに対して作成され、生成されたファイルが関連付けられているレコードを検索します。</span><span class="sxs-lookup"><span data-stu-id="5d093-148">Go to **Organization administration \> Electronic reporting \> Electronic reporting jobs**, and find the record that was created for this execution job and that has the generated file attached to it.</span></span>
3. <span data-ttu-id="5d093-149">ローカルの **C:\\0** フォルダーを参照して、生成ファイルを見つけます。</span><span class="sxs-lookup"><span data-stu-id="5d093-149">Browse to the local **C:\\0** folder to find the generated file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d093-150">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5d093-150">Additional resources</span></span>

[<span data-ttu-id="5d093-151">電子申告 (ER) の送信先</span><span class="sxs-lookup"><span data-stu-id="5d093-151">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)

[<span data-ttu-id="5d093-152">Application update 10.0.19 での電子申告フレームワーク API の変更</span><span class="sxs-lookup"><span data-stu-id="5d093-152">Electronic reporting framework API changes for Application update 10.0.19</span></span>](er-apis-app10-0-19.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
