---
title: フィールドの説明をカスタマイズする
description: この記事では、既存のフィールドの説明をカスタマイズし、独自の説明を追加する方法について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rschloma
ms.search.scope: Operations
ms.custom: 92013
ms.assetid: 94d555d7-28f3-4d94-91b4-6038e2be5047
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: fd6daf3ed299c471888a83606d1e3cf84dea3d40
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537269"
---
# <a name="customize-field-descriptions"></a><span data-ttu-id="d3883-103">フィールドの説明をカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="d3883-103">Customize field descriptions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3883-104">この記事では、既存のフィールドの説明をカスタマイズし、独自の説明を追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d3883-104">This article describes how you can customize existing field descriptions and add your own descriptions.</span></span>

<span data-ttu-id="d3883-105">より複雑なフィールドの説明がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="d3883-105">There are descriptions for some of the more complex fields.</span></span> <span data-ttu-id="d3883-106">フィールド上に置くと、これらの説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3883-106">These descriptions appear when you hover over a field.</span></span> <span data-ttu-id="d3883-107">会社固有の情報を追加する場合などに、これらの説明をカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="d3883-107">You can customize these descriptions if, for example, you want to add company-specific information.</span></span> <span data-ttu-id="d3883-108">また、追加フィールドの説明を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="d3883-108">You can also add descriptions for additional fields.</span></span> <span data-ttu-id="d3883-109">フィールドの説明を作成するには、フィールド コントロールの **HelpText** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3883-109">You create field descriptions by using the **HelpText** property for field controls.</span></span> <span data-ttu-id="d3883-110">**HelpText** プロパティは、以前のバージョンのように、テーブル フィールドとデータ型に指定されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="d3883-110">The **HelpText** property is no longer specified for table fields and data types, as it was in previous versions.</span></span> <span data-ttu-id="d3883-111">また、データ型とテーブル フィールドからフォーム コントロールへの **HelpText** プロパティの継承は廃止されました。</span><span class="sxs-lookup"><span data-stu-id="d3883-111">Additionally, the inheritance of the **HelpText** property from data types and table fields to form controls is obsolete.</span></span> <span data-ttu-id="d3883-112">フィールドの説明は、他のコントロールおよびページで使用可能な情報のコンテキストである、個々のフィールドに対して固有のものです。</span><span class="sxs-lookup"><span data-stu-id="d3883-112">Field descriptions are intended to be specific to an individual field, in the context of the other controls and information that are available on the page.</span></span> <span data-ttu-id="d3883-113">フィールドの説明を追加およびカスタマイズするには、開発環境へのアクセスが必要です。</span><span class="sxs-lookup"><span data-stu-id="d3883-113">To add and customize field descriptions, you must have access to the development environment.</span></span> <span data-ttu-id="d3883-114">その他のメタデータの変更と同様に、Operations の新しいバージョンがリリースされるとき、新しい説明は上書きされるを防ぐために新しいモデルに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3883-114">Like other metadata changes, new descriptions should be added in a new model to prevent them from being overwritten when a new version of Operations is released.</span></span> <span data-ttu-id="d3883-115">詳細については、[カスタマイズ: オーバーレイおよび拡張機能](../extensibility/customization-overlayering-extensions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3883-115">For more information, see [Customization: Overlayering and extensions](../extensibility/customization-overlayering-extensions.md).</span></span>

## <a name="customize-a-field-description-or-add-a-new-description"></a><span data-ttu-id="d3883-116">フィールドの説明をカスタマイズするか、新しい説明を追加する</span><span class="sxs-lookup"><span data-stu-id="d3883-116">Customize a field description or add a new description</span></span>
<span data-ttu-id="d3883-117">同じ手順を使用して、既存のフィールド記述をカスタマイズし、新しいフィールド記述を追加します。</span><span class="sxs-lookup"><span data-stu-id="d3883-117">The same procedure is used to customize existing field descriptions and to add new field descriptions.</span></span> <span data-ttu-id="d3883-118">ただし、既存の説明をカスタマイズする場合に、既存のラベルの参照を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="d3883-118">However, when you customize an existing description, you replace the existing label reference.</span></span>

1.  <span data-ttu-id="d3883-119">アプリケーション エクスプローラーで、関連するページ (フォーム) を検索し、プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="d3883-119">In Application Explorer, find the relevant page (form), and add it to your project.</span></span>
2.  <span data-ttu-id="d3883-120">ページのノードで、関連するフィールド コントロールを探します。</span><span class="sxs-lookup"><span data-stu-id="d3883-120">In the node for the page, find the relevant field control.</span></span> <span data-ttu-id="d3883-121">ラベル ID の一部として使用することができるように、名前をメモしておきます。</span><span class="sxs-lookup"><span data-stu-id="d3883-121">Make a note of the name, so that you can use it as part of the label ID.</span></span>
3.  <span data-ttu-id="d3883-122">説明の新しいラベルを追加します。</span><span class="sxs-lookup"><span data-stu-id="d3883-122">Add a new label for your description.</span></span> <span data-ttu-id="d3883-123">Microsoft が使用する規則に従い、フィールドの説明のためのラベル ファイルに名前を付け、ラベル ファイル ID を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="d3883-123">You can follow the conventions that Microsoft uses to name the label files for field descriptions and to create the label file IDs.</span></span> <span data-ttu-id="d3883-124">詳細については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3883-124">For more information, see the next section.</span></span>
4.  <span data-ttu-id="d3883-125">フィールド制御の **HelpText** プロパティで、ラベルへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="d3883-125">In the **HelpText** property of the field control, add a reference to the label.</span></span>

## <a name="label-file-names-and-label-ids"></a><span data-ttu-id="d3883-126">ラベル ファイル名とラベル ID</span><span class="sxs-lookup"><span data-stu-id="d3883-126">Label file names and label IDs</span></span>
<span data-ttu-id="d3883-127">Microsoft が提供するフィールドの説明は、別のラベル ファイルに格納されています。</span><span class="sxs-lookup"><span data-stu-id="d3883-127">The field descriptions that are provided by Microsoft are stored in separate label files.</span></span> <span data-ttu-id="d3883-128">モデルごとのモジュールごとに 1 つのラベル ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="d3883-128">There is one label file per module per model.</span></span> <span data-ttu-id="d3883-129">ラベル ファイル名のパターンは、FieldDescriptions\_*ModuleName*\_*ModelName*.*CountryCode*.label.txt です。</span><span class="sxs-lookup"><span data-stu-id="d3883-129">The pattern for the label file names is FieldDescriptions\_*ModuleName*\_*ModelName*.*CountryCode*.label.txt.</span></span> <span data-ttu-id="d3883-130">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="d3883-130">Here are some examples:</span></span>

-   <span data-ttu-id="d3883-131">FieldDescriptions\_AccountsPayable\_ApplicationFoundation.en-US.label.txt</span><span class="sxs-lookup"><span data-stu-id="d3883-131">FieldDescriptions\_AccountsPayable\_ApplicationFoundation.en-US.label.txt</span></span>
-   <span data-ttu-id="d3883-132">FieldDescriptions\_SystemAdministration\_ApplicationFoundation\_en-US.txt</span><span class="sxs-lookup"><span data-stu-id="d3883-132">FieldDescriptions\_SystemAdministration\_ApplicationFoundation\_en-US.txt</span></span>

<span data-ttu-id="d3883-133">ラベル ID のパターンは @FieldDescriptions\_*ModuleName:PageName*\_*ControlName* です。</span><span class="sxs-lookup"><span data-stu-id="d3883-133">The pattern for label IDs is @FieldDescriptions\_*ModuleName:PageName*\_*ControlName*.</span></span> <span data-ttu-id="d3883-134">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="d3883-134">Here are some examples:</span></span>

- <span data-ttu-id="d3883-135">@FieldDescriptions\_AccountsPayable:CustSettlement\_CustSettlement\_OffsetCompany は、<strong>顧客決済</strong>ページ (CustSettlement) の<strong>会社コード</strong>フィールド (CustSettlement\_OffsetCompany) のラベルの ID です。</span><span class="sxs-lookup"><span data-stu-id="d3883-135">@FieldDescriptions\_AccountsPayable:CustSettlement\_CustSettlement\_OffsetCompany is the ID for the label for the <strong>Company accounts</strong> field (CustSettlement\_OffsetCompany) on the <strong>Customer settlement</strong> page (CustSettlement).</span></span>
- <span data-ttu-id="d3883-136">@FieldDescriptions\_ProcurementAndSourcing:PurchLineBackOrder\_LinkViewCheckBox は、<strong>発注残購買注文明細行</strong> (PurchLineBackOrder) ページ内の<strong>変更ビューのリンク</strong> (LinkViewCheckBox) オプションのラベルの ID です。</span><span class="sxs-lookup"><span data-stu-id="d3883-136">@FieldDescriptions\_ProcurementAndSourcing:PurchLineBackOrder\_LinkViewCheckBox is the ID for the label for the <strong>Link on change view</strong> option (LinkViewCheckBox) on the <strong>Backorder purchase lines</strong> page (PurchLineBackOrder).</span></span>


<a name="additional-resources"></a><span data-ttu-id="d3883-137">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="d3883-137">Additional resources</span></span>
--------

[<span data-ttu-id="d3883-138">クライアントでローカライズ可能なラベルを作成する</span><span class="sxs-lookup"><span data-stu-id="d3883-138">Create and use localizable labels in the client</span></span>](create-localizable-labels-client.md)

[<span data-ttu-id="d3883-139">フィールド説明の表示およびエクスポート</span><span class="sxs-lookup"><span data-stu-id="d3883-139">View and export field descriptions</span></span>](../../fin-and-ops/get-started/view-export-field-descriptions.md)



