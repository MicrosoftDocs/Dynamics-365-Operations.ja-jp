---
title: Application update 10.0.21 での電子申告フレームワーク API の変更
description: このトピックでは、Microsoft Dynamics 365 Finance バージョン 10.0.21 で電子申告 (ER) フレームワークの API がどのように変更されたのかについて説明します。
author: NickSelin
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERFormatDestinationTable
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 0130aba2ddbc795499f8d6a7b4d52795b19b1761
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413624"
---
# <a name="electronic-reporting-framework-api-changes-for-application-update-10021"></a>Application update 10.0.21 での電子申告フレームワーク API の変更

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Finance バージョン 10.0.21 で電子申告 (ER) フレームワークのアプリケーション プログラミング インターフェイス (API) がどのように変更されたかについて説明します。

## <a name="api-to-enable-users-to-configure-er-destinations-that-are-print-management-record-specific"></a><a name="er-api-set-print-management-record-specific-destination"></a>ユーザーが印刷管理レコード固有の ER 送信先を構成できるようにする API

この新しい API を使用すると、特定のタイプのビジネス ドキュメントに ER の送信先を設定し、設定された名前付き送信先を[印刷管理](document-reporting-services.md)レコードに割り当てることができます。 したがって、ER 送信先を印刷管理レコード固有のものにすることができます。

```xpp
/// <summary>Class for enabling NamedDestinationFeature for current document type.</summary>
/// <remarks>To enable the document type you should wrap a <c>isNamedDestinationEnabledByDocumentType</c> method.</remarks>
public class ERNamedDestinationReportEnabler
{
    /// <summary>Checks that feature enabled for current document type. Make extension for this method.</summary>
    /// <param name = "_typeId">Print mgmt document type</param>
    /// <returns>True if feature enabled.</returns>
    [Wrappable(true), SuppressBPWarning('BPParameterNotUsed', 'Required by signature')]
    public static boolean isNamedDestinationEnabledByDocumentType(PrintMgmtDocumentType _typeId)
    {
        return false;
    }
}
```

## <a name="api-to-run-a-format-mapping-where-the-destination-that-is-provided-is-print-management-record-specific"></a><a name="er-api-pass-print-management-record-specific-destination"></a>提供される送信先が印刷管理レコード固有である形式マッピングを実行するための API

この新しい API を使用すると、名前付きの ER 送信先を使用して、生成されたドキュメントを ER に強制的に送信させることができます。

```xpp
using Microsoft.Dynamics365.LocalizationFramework;

/// <summary>
/// Format mapping run interface to provide an ability to specify destination preset.
/// </summary>
public interface ERIFormatMappingRunWithNamedDestination
{
    /// <summary>
    /// Sets the named destination to the format mapping run object.
    /// </summary>
    /// <param name = "_destinationNamedId">A rec id of named destination.</param>
    /// <returns>The format mapping run object.</returns>
    ERIFormatMappingRun withDestinationNamed(RefRecId _destinationNamedId)
    {
    }
}
```

## <a name="applicability"></a>適用性

名前付きの送信先を設定し、提供された名前付き送信先を ER フレームワークに使用させるには、最初に [機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace)ワークスペースで、**印刷管理品目ごとの ER 送信先設定を許可する** 機能を有効にする必要があります。

## <a name="additional-resources"></a>追加リソース

[電子申告 (ER) の概要](general-electronic-reporting.md)

[電子申告 (ER) の送信先](electronic-reporting-destinations.md)

[コードを変更して、ユーザーが名前付き送信先を構成して使用できるようにする](er-api-named-destinations.md)

[アクション依存の ER 送信先を構成する](er-action-dependent-destinations.md)

[印刷管理レコード固有の ER 送信先を構成する](er-named-destinations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
