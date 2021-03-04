---
title: Application update 10.0.17 での電子申告フレームワーク API の変更
description: このトピックでは、Microsoft Dynamics 365 Finance バージョン10.0.11 で電子申告 (ER) フレームワーク の API がどのように変更されたのかについて説明します。
author: NickSelin
manager: AnnBe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERFormatDestinationTable
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: dd0e1e5fea1519cbbde036bacb4c57093467e5fa
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130515"
---
# <a name="electronic-reporting-framework-api-changes-for-application-update-10017"></a>Application update 10.0.17 での電子申告フレームワーク API の変更

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Finance バージョン 10.0.17 で電子申告 (ER) フレームワークのアプリケーション プログラミング インターフェイス (API) がどのように変更されたかについて説明します。

## <a name="api-to-run-a-format-mapping-that-provides-a-user-action-code-to-run-action-dependent-destinations"></a>アクションの依存先を実行するためユーザー アクション コードを提供する形式マッピングを実行する <a name="er-api-run-format-with-action-code"></a> API

[送信ドキュメント](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents) を生成するには、ER  [形式マッピング](general-electronic-reporting.md#FormatComponentInbound) を実行する必要があります。 ER フレームワークの[初期](er-apis-app73.md#code-to-run-a-format-mapping-for-data-export) API を使用して ER 形式マッピングを呼び出す場合、形式のコンポーネントに対して構成されている[送信先](electronic-reporting-destinations.md#applicability)はすべて常に実行されます。 このタイプの呼び出しのサンプル コードを確認するには、[レポート サービス クラスを追加する](er-quick-start1-new-solution.md#ServiceClass)を参照してください。

```xpp
// Call ER to generate the report.
ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
if(formatMappingRun.parmShowPromptDialog(true))
{
    formatMappingRun.withParameter(parameters);
    formatMappingRun.withFileDestination(_contract.getFileDestination());
    formatMappingRun.run();
}
```

場合によっては、X++ コードの特定の場所から ER 形式マッピングが呼び出される場合、ER 形式を実行してユーザーが実行するアクションを指定して、その形式に対して構成されているすべての ER 送信先の代わりに、アクション依存先のみが実行されるようにする必要があります。

たとえば、[印刷管理](document-reporting-services.md)設定に基づくER 形式があるとします。 生成されたドキュメントをプレビューするためこの ER 形式を呼び出す場合、[画面](er-destination-type-screen.md)送信先のみが実行されると想定されます。 ただし、同じ ER 形式を呼び出して、生成されたドキュメントを電子メールの送信メッセージの添付ファイルとして送信する場合、[電子メール](er-destination-type-email.md)送信先のみが実行されると想定されます。

これらの結果を得るには、ER 形式に対するアクション依存の ER 送信先を構成する必要があります。 詳細については、[アクション依存の ER 送信先を構成する](er-action-dependent-destinations.md)を参照してください。

構成が完了すると、ER フレームワークの新しい API を使用して、指定されたアクション用に構成された送信先のみを実行するユーザー アクション コードを提供する ER 形式マッピングを呼び出すことができます。 次の例は、前述のサンプル コードを変更してこの新しい API を使用し、**表示** アクションを提供する ER 形式を実行する方法を示しています。

```xpp
// Call ER to generate the report.
ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
if(formatMappingRun.parmShowPromptDialog(true))
{
    formatMappingRun.withParameter(parameters);
    formatMappingRun.withFileDestination(_contract.getFileDestination());

    var formatMappingRunWithAction = formatMappingRun as ERIFormatMappingRunWithDestinationAction;
    formatMappingRunWithAction.withDestinationAction(ERDestinationAction::View);
    formatMappingRun.run();
}
```

> [!IMPORTANT]
> アクション依存先を設定し、指定されたアクション コードを使用して ER フレームワークを強制するには、まず [機能管理](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview#the-feature-management-workspace)ワークスペースで、**異なる PM アクションに対して使用する特定の ER 送信先を構成する** 機能を有効にする必要があります。

## <a name="additional-resources"></a>追加リソース

[電子申告 (ER) の概要](general-electronic-reporting.md)

[電子申告 (ER) の送信先](electronic-reporting-destinations.md)

[カスタム レポートを印刷するための新しい電子申告ソリューションの設計](er-quick-start1-new-solution.md)
