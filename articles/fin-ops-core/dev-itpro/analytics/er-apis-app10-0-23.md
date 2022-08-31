---
title: Application update 10.0.23 での電子申告フレームワーク API の変更
description: この記事では、Microsoft Dynamics 365 Finance バージョン 10.0.23 で電子申告 (ER) フレームワーク の API がどのように変更されたのかについて説明します。
author: kfend
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-10-01
ms.dyn365.ops.version: 10.0.23
ms.search.form: ERFormatDestinationTable, ERParameters
ms.openlocfilehash: da82d7ba64a97ac52c35f36e4b296827b68e300b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268811"
---
# <a name="electronic-reporting-framework-api-changes-for-application-update-10023"></a>Application update 10.0.23 での電子申告フレームワーク API の変更

[!include [banner](../includes/banner.md)]

この記事では、[電子申告 (ER)](general-electronic-reporting.md) フレームワークのアプリケーション プログラミング インターフェイス (APIs) が Microsoft Dynamics 365 Finance バージョン 10.0.23 でどのように変化されたかについて説明します。

## <a name="api-to-extend-the-list-of-er-sources-of-inbound-documents"></a><a name="er-api-extend-file-source"></a> 受信ドキュメントの ER ソース リストを拡張する API

受信ドキュメントのカスタム ER [ソース](er-configure-data-import-sharepoint.md#configure-er-sources-for-the-er-format)を実装するには、次のパブリック インターフェイスを使用します。

- `ERIImportFile`
- `ERIImportFileSourceSettings`
- `ERIImportFileSourceSettingsStorage`

```cs
using Microsoft.Dynamics365.LocalizationFramework.XppSupportLayer;

namespace Microsoft.Dynamics365.LocalizationFramework
{
    /// <summary>
    /// The import file object.
    /// </summary>
    public interface ERIImportFile : ERIFile
    {
        /// <summary>
        /// Gets or sets a file source settings key.
        /// </summary>
        string SourceSettingsKey { get; set; }

        /// <summary>
        /// Sets a file id. File ID should be unique string with max length 300.
        /// </summary>
        string FileId { set; }

        /// <summary>
        /// Gets or sets a file name. File name with max length 259.
        /// </summary>
        string Name { get; set; }

        /// <summary>
        /// Gets or sets a file created date time.
        /// </summary>
        utcdatetime CreatedDateTime { get; set; }

        /// <summary>
        /// Sets a file modified date time.
        /// </summary>
        utcdatetime ModifiedDateTime { set; }
    }
}
```

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
using System.IO;

/// <summary>
/// Format source settings required to store settings for a specific sources for the import format.
/// </summary>
/// <remarks>
/// The implementation object should have static create(container) method for a proper packing.
/// </remarks>
public interface ERIImportFileSourceSettings extends SysPackable
{
    /// <summary>
    /// Gets a name of the source.
    /// </summary>
    /// <returns>The name.</returns>
    str getName()
    {
    }

    /// <summary>
    /// Validates the settings.
    /// </summary>
    /// <returns>True, if validated successful; otherwise - false.</returns>
    boolean validate()
    {
    }

    /// <summary>
    /// Determines if current settings are enabled.
    /// </summary>
    /// <returns>True if enabled; otherwise - false.</returns>
    boolean isEnabled()
    {
    }

    /// <summary>
    /// Sets settings enabling state.
    /// </summary>
    /// <param name = "_value">An enabling state.</param>
    void setEnabled(boolean _value)
    {
    }

    /// <summary>
    /// Gets a settings key, this key should start with or be an implementation class name. This key should also be persistent and shouldn't be changed over time.
    /// This key will be used to retrieve this type of settings from a settings storage.
    /// </summary>
    /// <remarks>Examples of good keys: MyCustomFileSourceSettings, MyCustomFileSourceSettings#UniqueKey.</remarks>
    /// <returns>The settings key.</returns>
    str getKey()
    {
    }

    /// <summary>
    /// Creates a file source for current settings.
    /// </summary>
    /// <param name = "_fileMask">A file mask.</param>
    /// <returns>A new instance of a file source.</returns>
    ERIFileSource createFileSource(str _fileMask)
    {
    }

    /// <summary>
    /// Post processing for resulted file. An action after file importing.
    /// </summary>
    /// <param name = "_args">Arguments for file post import process.</param>
    void fileImported(ERFileImportedArgs _args)
    {
    }

}
```

```xpp
/// <summary>
/// Provides access to the source settings storage.
/// </summary>
public interface ERIImportFileSourceSettingsStorage
{
    /// <summary>
    /// Adds settings to the format source settings storage.
    /// </summary>
    /// <param name = "_settings">A given settings to add.</param>
    public void addSettings(ERIImportFileSourceSettings _settings)
    {
    }

    /// <summary>
    /// Gets source settings by the key.
    /// </summary>
    /// <param name = "_key">A given key.</param>
    /// <returns>The source settings.</returns>
    public ERIImportFileSourceSettings getSettingsByKey(str _key)
    {
    }

}
```

このインターフェイスでは、カスタム ソース パラメーターを **ER ソース設定** ダイアログ ボックスで提供し、設計時に設定できるようになっています。 構成済みのソースを使用して、構成済みのカスタム ソースで実行時にインポートする必要のある受信ドキュメントにアクセスできます。

このインターフェイスの詳細については、[受信ドキュメントのカスタム ソースを実装する](er-custom-file-source.md)の例を完了してください。

## <a name="additional-resources"></a>追加リソース

[電子申告 (ER) の概要](general-electronic-reporting.md)

[受信したドキュメントを解析する](er-parse-incoming-documents.md)

[ファイルストレージ用の SharePoint へのアクセスを構成する](er-configure-data-import-sharepoint.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
