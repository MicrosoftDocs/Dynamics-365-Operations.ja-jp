---
title: 電子申告のフレームワーク API の変更点
description: このトピックでは、電子申告（ER）フレームワークのアプリケーション プログラミング インターフェース（API）が、Microsoft Dynamics 365 Finance  バージョン10.0.11でどのように変更されたかについて説明します。
author: NickSelin
manager: AnnBe
ms.date: 04/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 50156e3a23f5159023795d45776682fb706f7ffc
ms.sourcegitcommit: 88347d0f0ac862a77f269a05f1801d30dc93586e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2020
ms.locfileid: "3260241"
---
# <a name="electronic-reporting-framework-api-changes"></a><span data-ttu-id="8c168-103">電子申告のフレームワーク API の変更点</span><span class="sxs-lookup"><span data-stu-id="8c168-103">Electronic reporting framework API changes</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="8c168-104">このトピックでは、電子申告（ER）フレームワークのアプリケーション プログラミング インターフェース（API）が、Microsoft Dynamics 365 Finance  バージョン10.0.11でどのように変更されたかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8c168-104">This topic describes how the application programming interfaces (APIs) of the Electronic reporting (ER) framework have been changed in Microsoft Dynamics 365 Finance version 10.0.11.</span></span>

## <a name="api-to-run-a-format-mapping-for-the-generation-of-outbound-documents"></a><span data-ttu-id="8c168-105">送信ドキュメントの生成に対して形式マッピングを実行する API</span><span class="sxs-lookup"><span data-stu-id="8c168-105">API to run a format mapping for the generation of outbound documents</span></span>

<span data-ttu-id="8c168-106">[送信ドキュメント](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents) を生成するには、ER  [形式マッピング](general-electronic-reporting.md#FormatComponentInbound) を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c168-106">To generate an [outbound document](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents), you must run an ER [format mapping](general-electronic-reporting.md#FormatComponentInbound).</span></span> <span data-ttu-id="8c168-107">ほとんどの ER 形式のマッピングには、**データ モデル** 型のデータ ソースが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8c168-107">Most ER format mappings contain a data source of the **Data model** type.</span></span> <span data-ttu-id="8c168-108">実行時には、特定の [モデル マッピング](general-electronic-reporting.md#data-model-and-model-mapping-components)が、データソースが設定されている [データモデル](general-electronic-reporting.md#data-model-and-model-mapping-components) の実装として識別される必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c168-108">At runtime, a specific [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) must be identified as the implementation of the [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) that the data source has been configured for.</span></span>

<span data-ttu-id="8c168-109">ER フレームワークの [初期](er-apis-app73.md#code-to-run-a-format-mapping-for-data-export) API を使用してソースコードの実行ポイントから ER 形式のマッピングを呼び出すと、モデル マッピング コンポーネントを含む、対応する ER [構成](general-electronic-reporting.md#Configuration)の設定（既定のモデルマッピング フラグと国/地域コード）を考慮したモデル マッピングが見つかります。</span><span class="sxs-lookup"><span data-stu-id="8c168-109">When the [initial](er-apis-app73.md#code-to-run-a-format-mapping-for-data-export) API of the ER framework is used to call an ER format mapping from an execution point in the source code, a model mapping is found that takes into account the settings (the default model mapping flag and country/region codes) of the corresponding ER [configurations](general-electronic-reporting.md#Configuration) that contain a model mapping component.</span></span> <span data-ttu-id="8c168-110">詳細については、[国のコンテキスト依存 ER モデル マッピングを構成する](er-country-dependent-model-mapping.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c168-110">For more information, see [Configure country context dependent ER model mappings](er-country-dependent-model-mapping.md).</span></span>

<span data-ttu-id="8c168-111">場合によっては、X++ コードの特定の場所から ER 形式のマッピングが呼び出された場合、最も適切なモデル マッピングを検索するための追加の基準を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c168-111">In some cases, when an ER format mapping is called from a specific place in the X++ code, you must specify additional criteria to find the most appropriate model mapping.</span></span> <span data-ttu-id="8c168-112">たとえば、ER 形式マッピングは、2 つのモデル マッピングを持つデータ モデルを使用して設定されています。</span><span class="sxs-lookup"><span data-stu-id="8c168-112">For example, an ER format mapping has been configured by using a data model that you have two model mappings for.</span></span> <span data-ttu-id="8c168-113">最初のモデルマッピングは、現在使用可能なすべての実行ポイントから、この ER 形式のマッピングを呼び出すたびに円滑に実行されるようにするため、既定のモデルマッピングとしてマークされています。</span><span class="sxs-lookup"><span data-stu-id="8c168-113">The first model mapping is marked as a default model mapping, because it ensures the smooth execution of this ER format mapping whenever it's called, from every execution point that is currently available.</span></span> <span data-ttu-id="8c168-114">X + + では、この ER 形式マッピングを呼び出す新たな実行ポイントを実装します。</span><span class="sxs-lookup"><span data-stu-id="8c168-114">In X++, you implement a new execution point to call this ER format mapping from.</span></span> <span data-ttu-id="8c168-115">この方法では、この呼び出しの他の条件（指定された引数や現在のアプリケーション インスタンスの利用可能なリソースなど）によって、そのモデルマッピングの方がより良いパフォーマンスを発揮すると判断されるため、データモデルに2番目のモデルマッピングを使用するように強制します。</span><span class="sxs-lookup"><span data-stu-id="8c168-115">In this way, you force the data model to use the second model mapping, because that model mapping will perform better, given the other conditions of this call (for example, the arguments that are provided and the available resources of the current application instance).</span></span>

<span data-ttu-id="8c168-116">この設定を完了するには、統合ポイントを使用してモデル マッピングを構成します。</span><span class="sxs-lookup"><span data-stu-id="8c168-116">To complete this setup, configure your model mapping with an integration point.</span></span> <span data-ttu-id="8c168-117">**データソース** ウィンドウでは、この統合ポイントのコンポーネントとして、モデル マッピングの単一のデータソースを選択できます。</span><span class="sxs-lookup"><span data-stu-id="8c168-117">In the **Data sources** pane, you can select a single data source of your model mapping as the component of this integration point.</span></span> <span data-ttu-id="8c168-118">続いて **編集** を選択して、このデータ ソースのプロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="8c168-118">Then select **Edit** to change the properties of this data source.</span></span>

![編集を選択して、このデータ ソースのプロパティを変更します。](./media/er-api-ds-integration-point1.png)

<span data-ttu-id="8c168-120">**データソースのプロパティ** ダイアログ ボックスで、**統合ポイント** オプションを **はい** に設定すると、データソースを統合ポイントのコンポーネントとしてマークできます。</span><span class="sxs-lookup"><span data-stu-id="8c168-120">In the **Data source properties** dialog box, you can set the **Integration point** option to **Yes** to mark the data source as the component of the integration point.</span></span>

![統合ポイント オプションの設定](./media/er-api-ds-integration-point2.png)

<span data-ttu-id="8c168-122">ER フレームワークの新しい API を使用して ER 形式のマッピングを呼び出し、特定の統合ポイントを含むように設定されたモデル マッピングを強制的に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="8c168-122">You can then use the new API of the ER framework to call an ER format mapping and force it to use a model mapping that has been configured to contain a specific integration point.</span></span> <span data-ttu-id="8c168-123">次の例では、この新しい API の使用方法を解説します。</span><span class="sxs-lookup"><span data-stu-id="8c168-123">The following example shows how this new API can be used.</span></span>

```
using Microsoft.Dynamics365.LocalizationFramework;
using Microsoft.Dynamics365.LocalizationFramework.XppSupportLayer;

class ERIntegrationPointCodeSamples extends RunBaseBatch
{
    private ERFormatMappingId formatMappingId;

    public void run()
    {
        var runner = ERObjectsFactory::createFormatMappingRunByFormatMappingId(this.formatMappingId, 'OutboundFileName', true);
        var integration_point = new ERIntegrationPointFactory().WithObjectIntegrationPoint('SalesInvoiceDP').ToIntegrationPoint();
        /// new ERIntegrationPointFactory().WithTableRecordsIntegrationPoint(tableName)
        /// new ERIntegrationPointFactory().WithTableIntegrationPoint(tableName)
        /// new ERIntegrationPointFactory().WithObjectIntegrationPoint(className)
        /// new ERIntegrationPointFactory().WithClassIntegrationPoint(className)
        runner.withIntegrationPoint(integration_point).run();
    }
}
```

> [!NOTE]
> - <span data-ttu-id="8c168-124">モデルマッピング統合ポイントのコンポーネントとしてマークできるのは、**テーブル レコード**、**テーブル**、**クラス**、**オブジェクト**タイプのデータソースのみです。</span><span class="sxs-lookup"><span data-stu-id="8c168-124">Only a data source of the **Table record**, **Table**, **Class**, or **Object** type can be marked as the component of the model mapping integration point.</span></span>
> - <span data-ttu-id="8c168-125">現在、モデルマッピング統合ポイントの構成要素として使用できるデータ ソースは単一のものに限られています。</span><span class="sxs-lookup"><span data-stu-id="8c168-125">Currently, only a single data source can be used as the component of the model mapping integration point.</span></span>
> - <span data-ttu-id="8c168-126">その他の既存の基準に加えて、統合ポイントは最適なモデル マッピングの選択時に考慮されます。</span><span class="sxs-lookup"><span data-stu-id="8c168-126">In addition to other existing criteria, the integration point will be considered during the selection of the most appropriate model mapping.</span></span>
> - <span data-ttu-id="8c168-127">実行時に、実行中の ER 形式のマッピングに適用可能なモデル マッピングの中から、要求された統合ポイントを持つモデル マッピングが複数検出された場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="8c168-127">At runtime, an error will occur if more than one model mapping that has the requested integration point is found among the model mappings that are applicable to the ER format mapping that is running.</span></span>

## <a name="api-to-show-a-format-mapping-lookup"></a><span data-ttu-id="8c168-128">フォーマット マッピング ルックアップを表示する API</span><span class="sxs-lookup"><span data-stu-id="8c168-128">API to show a format mapping lookup</span></span>

<span data-ttu-id="8c168-129">ER フレームワークの [初期](er-apis-app73.md#code-to-display-a-format-mapping-lookup)の API は、ER 形式のマッピングを検索するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8c168-129">The [initial](er-apis-app73.md#code-to-display-a-format-mapping-lookup) API of the ER framework is used to look up the ER format mappings.</span></span> <span data-ttu-id="8c168-130">データ モデル名とコンテナー名をテキスト定数として使用します。</span><span class="sxs-lookup"><span data-stu-id="8c168-130">It uses the data model name and container name as text constants.</span></span> <span data-ttu-id="8c168-131">このルックアップでは、以下すべての条件を満たす one data model の ER 形式マッピングのみを提供しています：</span><span class="sxs-lookup"><span data-stu-id="8c168-131">This lookup offers only the ER format mappings of the one data model that meets both these conditions:</span></span>

- <span data-ttu-id="8c168-132">この名前は指定されています。</span><span class="sxs-lookup"><span data-stu-id="8c168-132">It has the specified names.</span></span>
- <span data-ttu-id="8c168-133">その基準は ER 構成リストで最初に満たされています。</span><span class="sxs-lookup"><span data-stu-id="8c168-133">Its criteria were met first in the ER configurations list.</span></span>

<span data-ttu-id="8c168-134">ER フレームワークの新しい API により、構成された統合ポイントを使用して同じルックアップを実装することができます。</span><span class="sxs-lookup"><span data-stu-id="8c168-134">The new API of the ER framework lets you use the configured integration point to implement the same lookup.</span></span> <span data-ttu-id="8c168-135">このルックアップは、指定された統合ポイントを持つモデル マッピングが利用可能な **データモデル** タイプのデータソースを含むすべての ER 形式のマッピングを提供します。</span><span class="sxs-lookup"><span data-stu-id="8c168-135">This lookup offers all the ER format mappings that contain a data source of the **Data model** type that a model mapping that has the specified integration point is available for.</span></span> <span data-ttu-id="8c168-136">このルックアップで提供される ER 形式のマッピングは、データソースとして異なるモデル マッピングを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="8c168-136">The ER format mappings that are offered in this lookup can use different model mappings as data sources.</span></span>

<span data-ttu-id="8c168-137">次の例では、この新しい API の使用方法を解説します。</span><span class="sxs-lookup"><span data-stu-id="8c168-137">The following example shows how this new API can be used.</span></span>

```
using Microsoft.Dynamics365.LocalizationFramework;
using Microsoft.Dynamics365.LocalizationFramework.XppSupportLayer;

class ERIntegrationPointCodeSamples extends RunBaseBatch
{
    private ERFormatMappingId formatMappingId;

    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        var integration_point = new ERIntegrationPointFactory().WithIntegrationPointKey('SalesInvoiceDP').ToIntegrationPoint();
        ERObjectsFactory::createFormatMappingTableLookupForIntegrationPoint(
            integration_point,
            _referenceGroupControl
            ).performFormLookup();
    }
}
```
