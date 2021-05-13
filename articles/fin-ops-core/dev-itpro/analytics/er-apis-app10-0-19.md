---
title: Application update 10.0.19 での電子申告フレームワーク API の変更
description: このトピックでは、Microsoft Dynamics 365 Finance バージョン 10.0.19 で電子申告 (ER) フレームワークの API がどのように変更されたのかについて説明します。
author: NickSelin
manager: AnnBe
ms.date: 03/29/2021
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
ms.openlocfilehash: 63fc9c3f16a6162a03cc6b130f900006d26b1160
ms.sourcegitcommit: 6c2f5c3b038f696532c335e20b0fbafa155d6858
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "5952121"
---
# <a name="electronic-reporting-framework-api-changes-for-application-update-10019"></a><span data-ttu-id="64468-103">Application update 10.0.19 での電子申告フレームワーク API の変更</span><span class="sxs-lookup"><span data-stu-id="64468-103">Electronic reporting framework API changes for Application update 10.0.19</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="64468-104">このトピックでは、Microsoft Dynamics 365 Finance バージョン 10.0.19 で[電子申告 (ER)](general-electronic-reporting.md) フレームワークのアプリケーション プログラミング インターフェイス (API) がどのように変更されたかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="64468-104">This topic describes how the application programming interfaces (APIs) of the [Electronic reporting (ER)](general-electronic-reporting.md) framework have been changed in Microsoft Dynamics 365 Finance version 10.0.19.</span></span>

## <a name="api-to-extend-the-list-of-er-destinations"></a><a name="er-api-extend-destination"></a> <span data-ttu-id="64468-105">ER 行先のリストを拡張する API</span><span class="sxs-lookup"><span data-stu-id="64468-105">API to extend the list of ER destinations</span></span>

<span data-ttu-id="64468-106">[カスタム](electronic-reporting-destinations.md#destination-types) ER [接続先](electronic-reporting-destinations.md) を実装するには、`ERIFormatFileDestinationSettings` パブリック インターフェイスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64468-106">To implement a [custom](electronic-reporting-destinations.md#destination-types) ER [destination](electronic-reporting-destinations.md), you must use the `ERIFormatFileDestinationSettings` public interface.</span></span>

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

<span data-ttu-id="64468-107">このインターフェイスを使用すると、ER の接続先ダイアログ ボックスでカスタム接続先のパラメータを提供し、設計時に設定できます。</span><span class="sxs-lookup"><span data-stu-id="64468-107">This interface lets you offer parameters of a custom destination in the ER destinations dialog box, so that they can be set at design time.</span></span> <span data-ttu-id="64468-108">その後、構成された接続先を実行時に使用して、生成された[送信](general-electronic-reporting.md#FormatComponentOutbound) ドキュメントを格納できます。</span><span class="sxs-lookup"><span data-stu-id="64468-108">The configured destination can then be used at runtime to store generated [outbound](general-electronic-reporting.md#FormatComponentOutbound) documents.</span></span>

<span data-ttu-id="64468-109">このインターフェイスの詳細については、[生成されるドキュメントのカスタム送信先を実装する](er-custom-file-destination.md) の例を完了してください。</span><span class="sxs-lookup"><span data-stu-id="64468-109">To learn more about this interface, complete the example in [Implement a custom destination for generated documents](er-custom-file-destination.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64468-110">追加リソース</span><span class="sxs-lookup"><span data-stu-id="64468-110">Additional resources</span></span>

[<span data-ttu-id="64468-111">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="64468-111">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="64468-112">電子申告 (ER) の送信先</span><span class="sxs-lookup"><span data-stu-id="64468-112">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
