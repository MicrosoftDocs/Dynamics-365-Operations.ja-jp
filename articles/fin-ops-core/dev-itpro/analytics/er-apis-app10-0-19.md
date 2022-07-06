---
title: Application update 10.0.19 での電子申告フレームワーク API の変更
description: この記事では、Microsoft Dynamics 365 Finance バージョン 10.0.19 で電子申告 (ER) フレームワーク の API がどのように変更されたのかについて説明します。
author: NickSelin
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERFormatDestinationTable, ERParameters
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-04-23
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: bda8dc15928ab37627c8cbd8ea617d2d9e2eeff0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844588"
---
# <a name="electronic-reporting-framework-api-changes-for-application-update-10019"></a>Application update 10.0.19 での電子申告フレームワーク API の変更

[!include [banner](../includes/banner.md)]


この記事では、[電子申告 (ER)](general-electronic-reporting.md) フレームワークのアプリケーション プログラミング インターフェイス (APIs) が Microsoft Dynamics 365 Finance バージョン 10.0.19 でどのように変化されたかについて説明します。

## <a name="api-to-extend-the-list-of-er-destinations"></a><a name="er-api-extend-destination"></a> ER 行先のリストを拡張する API

[カスタム](electronic-reporting-destinations.md#destination-types) ER [接続先](electronic-reporting-destinations.md) を実装するには、`ERIFormatFileDestinationSettings` パブリック インターフェイスを使用する必要があります。

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
using Microsoft.Dynamics365.LocalizationFramework.Format.FileGeneration;

using SL = Microsoft.Dynamics365.LocalizationFramework.XppSupportLayer;

/// <summary>
/// Destination settings are required to store settings of a FILE destination type for the format file component.
/// </summary>
/// <remarks>
/// The implementation object should have static create(container) method for a proper packing.
/// </remarks>
public interface ERIFormatFileDestinationSettings extends SysPackable
{
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
    /// Gets a name of the destination.
    /// </summary>
    /// <returns>The name.</returns>
    str getName()
    {
    }

    /// <summary>
    /// Creates a file destination for current settings.
    /// </summary>
    /// <param name = "_destinationContext">A destination context.</param>
    /// <param name = "_isGrouped">Determines whether the current file destination is grouped with others.</param>
    /// <returns>A new instance of a file destination.</returns>
    ERIFileDestination createDestination(ERDestinationExecutionContext _destinationContext, boolean _isGrouped)
    {
    }

    /// <summary>
    /// Gets a settings key. This key should start with or be an implementation class name. It should also be persistent and should not be changed over time.
    /// This key will be used to retrieve this type of settings from a settings storage.
    /// </summary>
    /// <remarks>Examples of good keys: MyCustomDestinationSettings, MyCustomDestinationSettings#UniqueKey.</remarks>
    /// <returns>The settings key.</returns>
    str getKey()
    {
    }

    /// <summary>
    /// Validates the settings.
    /// </summary>
    void validate()
    {
    }
}
```

このインターフェイスを使用すると、ER の接続先ダイアログ ボックスでカスタム接続先のパラメータを提供し、設計時に設定できます。 その後、構成された接続先を実行時に使用して、生成された送信 ドキュメントを格納できます。

このインターフェイスの詳細については、[生成されるドキュメントのカスタム送信先を実装する](er-custom-file-destination.md) の例を完了してください。

## <a name="additional-resources"></a>追加リソース

[電子申告 (ER) の概要](general-electronic-reporting.md)

[電子申告 (ER) の送信先](electronic-reporting-destinations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
