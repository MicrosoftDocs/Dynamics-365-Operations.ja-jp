---
title: Application update 10.0.17 での電子申告フレームワーク API の変更
description: このトピックでは、Microsoft Dynamics 365 Finance バージョン10.0.11 で電子申告 (ER) フレームワーク の API がどのように変更されたのかについて説明します。
author: NickSelin
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERFormatDestinationTable
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ffc453e83732d374b502ebe5f3857710d5a96f4c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751194"
---
# <a name="electronic-reporting-framework-api-changes-for-application-update-10017"></a><span data-ttu-id="666ce-103">Application update 10.0.17 での電子申告フレームワーク API の変更</span><span class="sxs-lookup"><span data-stu-id="666ce-103">Electronic reporting framework API changes for Application update 10.0.17</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="666ce-104">このトピックでは、Microsoft Dynamics 365 Finance バージョン 10.0.17 で電子申告 (ER) フレームワークのアプリケーション プログラミング インターフェイス (API) がどのように変更されたかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="666ce-104">This topic describes how the application programming interfaces (APIs) of the Electronic reporting (ER) framework have been changed in Microsoft Dynamics 365 Finance version 10.0.17.</span></span>

## <a name="api-to-run-a-format-mapping-that-provides-a-user-action-code-to-run-action-dependent-destinations"></a><span data-ttu-id="666ce-105">アクションの依存先を実行するためユーザー アクション コードを提供する形式マッピングを実行する <a name="er-api-run-format-with-action-code"></a> API</span><span class="sxs-lookup"><span data-stu-id="666ce-105"><a name="er-api-run-format-with-action-code"></a>API to run a format mapping that provides a user action code to run action-dependent destinations</span></span>

<span data-ttu-id="666ce-106">[送信ドキュメント](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents) を生成するには、ER  [形式マッピング](general-electronic-reporting.md#FormatComponentInbound) を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="666ce-106">To generate an [outbound document](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents), you must run an ER [format mapping](general-electronic-reporting.md#FormatComponentInbound).</span></span> <span data-ttu-id="666ce-107">ER フレームワークの[初期](er-apis-app73.md#code-to-run-a-format-mapping-for-data-export) API を使用して ER 形式マッピングを呼び出す場合、形式のコンポーネントに対して構成されている[送信先](electronic-reporting-destinations.md#applicability)はすべて常に実行されます。</span><span class="sxs-lookup"><span data-stu-id="666ce-107">When the [initial](er-apis-app73.md#code-to-run-a-format-mapping-for-data-export) API of the ER framework is used to call an ER format mapping, all [destinations](electronic-reporting-destinations.md#applicability) that were configured for components of the format are always run.</span></span> <span data-ttu-id="666ce-108">このタイプの呼び出しのサンプル コードを確認するには、[レポート サービス クラスを追加する](er-quick-start1-new-solution.md#ServiceClass)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="666ce-108">To review the sample code for a call of this type, see [Add a report service class](er-quick-start1-new-solution.md#ServiceClass).</span></span>

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

<span data-ttu-id="666ce-109">場合によっては、X++ コードの特定の場所から ER 形式マッピングが呼び出される場合、ER 形式を実行してユーザーが実行するアクションを指定して、その形式に対して構成されているすべての ER 送信先の代わりに、アクション依存先のみが実行されるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="666ce-109">In some cases, when an ER format mapping is called from a specific place in the X++ code, you must specify an action that the user performs by running an ER format, so that only action-dependent destinations are run instead of all the ER destinations that are configured for that format.</span></span>

<span data-ttu-id="666ce-110">たとえば、[印刷管理](document-reporting-services.md)設定に基づくER 形式があるとします。</span><span class="sxs-lookup"><span data-stu-id="666ce-110">For example, you have an ER format that is based on [Print management](document-reporting-services.md) settings.</span></span> <span data-ttu-id="666ce-111">生成されたドキュメントをプレビューするためこの ER 形式を呼び出す場合、[画面](er-destination-type-screen.md)送信先のみが実行されると想定されます。</span><span class="sxs-lookup"><span data-stu-id="666ce-111">When you call this ER format to preview a generated document, you expect that only the [Screen](er-destination-type-screen.md) destination will be run.</span></span> <span data-ttu-id="666ce-112">ただし、同じ ER 形式を呼び出して、生成されたドキュメントを電子メールの送信メッセージの添付ファイルとして送信する場合、[電子メール](er-destination-type-email.md)送信先のみが実行されると想定されます。</span><span class="sxs-lookup"><span data-stu-id="666ce-112">However, when you call the same ER format to send a generated document as the attachment of an outbound email message, you expect that only the [Email](er-destination-type-email.md) destination will be run.</span></span>

<span data-ttu-id="666ce-113">これらの結果を得るには、ER 形式に対するアクション依存の ER 送信先を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="666ce-113">To achieve these results, you must configure action-dependent ER destinations for the ER format.</span></span> <span data-ttu-id="666ce-114">詳細については、[アクション依存の ER 送信先を構成する](er-action-dependent-destinations.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="666ce-114">For more information, see [Configure action-dependent ER destinations](er-action-dependent-destinations.md).</span></span>

<span data-ttu-id="666ce-115">構成が完了すると、ER フレームワークの新しい API を使用して、指定されたアクション用に構成された送信先のみを実行するユーザー アクション コードを提供する ER 形式マッピングを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="666ce-115">After you've completed the configuration, you can use the new API of the ER framework to call an ER format mapping that provides a user action code that runs only destinations that were configured for the provided action.</span></span> <span data-ttu-id="666ce-116">次の例は、前述のサンプル コードを変更してこの新しい API を使用し、**表示** アクションを提供する ER 形式を実行する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="666ce-116">The following example shows how you can change the previously mentioned sample code to use this new API to run an ER format that provides the **View** action.</span></span>

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
> <span data-ttu-id="666ce-117">アクション依存先を設定し、指定されたアクション コードを使用して ER フレームワークを強制するには、まず [機能管理](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview#the-feature-management-workspace)ワークスペースで、**異なる PM アクションに対して使用する特定の ER 送信先を構成する** 機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="666ce-117">To set up action-dependent destinations and force the ER framework to use the provided action code, you must first turn on the **Configure specific ER destinations to be used for different PM actions** feature in the [Feature management](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview#the-feature-management-workspace) workspace.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="666ce-118">追加リソース</span><span class="sxs-lookup"><span data-stu-id="666ce-118">Additional resources</span></span>

[<span data-ttu-id="666ce-119">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="666ce-119">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="666ce-120">電子申告 (ER) の送信先</span><span class="sxs-lookup"><span data-stu-id="666ce-120">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)

[<span data-ttu-id="666ce-121">カスタム レポートを印刷するための新しい電子申告ソリューションの設計</span><span class="sxs-lookup"><span data-stu-id="666ce-121">Design a new ER solution to print a custom report</span></span>](er-quick-start1-new-solution.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]