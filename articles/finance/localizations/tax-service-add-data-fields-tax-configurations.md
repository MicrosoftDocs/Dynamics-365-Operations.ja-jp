---
title: 税コンフィギュレーションにデータ フィールドを追加する
description: このトピックでは、データ フィールドを追加して税コンフィギュレーションをカスタマイズする方法について説明します。
author: kailiang
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b9d9fce81151ad70d57c69e389e238a6f9137d56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819427"
---
# <a name="add-data-fields-in-tax-configurations"></a><span data-ttu-id="e9281-103">税コンフィギュレーションにデータ フィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="e9281-103">Add data fields in tax configurations</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="e9281-104">このトピックでは、[税統合で追加されたデータ フィールド](tax-service-add-data-fields-tax-integration-by-extension.md)を使用して、税コンフィギュレーション をカスタマイズする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e9281-104">This topic explains how to customize tax configurations by using [data fields that are added in the tax integration](tax-service-add-data-fields-tax-integration-by-extension.md).</span></span>

## <a name="customize-the-tax-data-model"></a><span data-ttu-id="e9281-105">税データ モデルをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="e9281-105">Customize the tax data model</span></span>

1. <span data-ttu-id="e9281-106">Microsoft Dynamics 365 Finance で、**電子申告** \> **税コンフィギュレーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e9281-106">In Microsoft Dynamics 365 Finance, go to **Electronic Reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="e9281-107">コンフィギュレーション ツリーで、**税データ モデル - ヨーロッパ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9281-107">In the configuration tree, select **Tax Data Model - Europe**.</span></span> <span data-ttu-id="e9281-108">次に、アクション ウィンドウで、**構成の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9281-108">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="e9281-109">ドロップダウン ダイアログ ボックスで、**名前から派生した課税対象ドキュメント モデル (税データ モデル -- ヨーロッパ、Microsoft** オプション) を選択し、新しい税データ モデルの名前を入力し、**コンフィギュレーションの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9281-109">In the drop-down dialog box, select the **Taxable document model derived from Name: Tax Data Model -- Europe, Microsoft** option, enter a name for the new tax data model, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="e9281-110">作成した税データ モデルを選択し、アクション ウィンドウで **デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9281-110">Select the tax data model that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="e9281-111">データ モデル ツリーを展開し、**明細行** を 選択して、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9281-111">Expand the data model tree, select **Lines**, and then select **New**.</span></span>
6. <span data-ttu-id="e9281-112">**ノードの作成** ダイアログ ボックスに名前を入力し、アイテムの種類を指定して、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9281-112">In the **Create node** dialog box, enter a name, specify the item type, and then select **Add**.</span></span>
7. <span data-ttu-id="e9281-113">必要な列を追加します。</span><span class="sxs-lookup"><span data-stu-id="e9281-113">Add any required columns.</span></span>
8. <span data-ttu-id="e9281-114">アクション ウィンドウで、**保存** を選択してから、**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9281-114">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="e9281-115">ページを閉じて、完成したバージョンの税データ モデルを表示します。</span><span class="sxs-lookup"><span data-stu-id="e9281-115">Close the page, and view the completed version of your tax data model.</span></span>

## <a name="customize-the-tax-configuration"></a><span data-ttu-id="e9281-116">税コンフィギュレーションをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="e9281-116">Customize the tax configuration</span></span>

1. <span data-ttu-id="e9281-117">Finance で、**電子申告** \> **税コンフィギュレーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e9281-117">In Finance, go to **Electronic reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="e9281-118">コンフィギュレーション ツリーで、**税コンフィギュレーション - ヨーロッパ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9281-118">In the configuration tree, select **Tax Configuration -- Europe**.</span></span> <span data-ttu-id="e9281-119">次に、アクション ウィンドウで、**構成の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9281-119">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="e9281-120">ドロップダウン ダイアログ ボックスで、**名前から派生した税サービス (税コンフィギュレーション -- ヨーロッパ、Microsoft** オプション) を選択し、新しい税コンフィギュレーションの名前を入力し、**コンフィギュレーションの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9281-120">In the drop-down dialog box, select the **Tax service configuration derived from Name: Tax Configuration -- Europe, Microsoft** option, enter a name for the new tax configuration, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="e9281-121">作成した税コンフィギュレーションを選択し、アクション ウィンドウで **デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9281-121">Select the tax configuration that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="e9281-122">**プロパティ** セクションの **データ モデル** フィールドで、先に作成したカスタマイズされた税データ モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="e9281-122">In the **Properties** section, in the **Data model** field, select the customized tax data model that you created earlier.</span></span>
6. <span data-ttu-id="e9281-123">**データ モデル バージョン** フィールドで、税データ モデルの完成したバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="e9281-123">In the **Data model version** field, select the completed version of the tax data model.</span></span>
7. <span data-ttu-id="e9281-124">**追加** を選択し、必要な税対策を追加します。</span><span class="sxs-lookup"><span data-stu-id="e9281-124">Select **Add**, and add the required tax measures.</span></span>
8. <span data-ttu-id="e9281-125">アクション ウィンドウで、**保存** を選択してから、**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9281-125">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="e9281-126">ページを閉じて、完成したバージョンの税コンフィギュレーションを表示します。</span><span class="sxs-lookup"><span data-stu-id="e9281-126">Close page, and view the completed version of your tax configuration.</span></span>

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a><span data-ttu-id="e9281-127">カスタマイズされた税コンフィギュレーションでの税機能の実装</span><span class="sxs-lookup"><span data-stu-id="e9281-127">Implement tax features in the customized tax configuration</span></span>

1. <span data-ttu-id="e9281-128">Regulatory Configuration Services (RCS) で、**グローバリゼーション機能**\>**税** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e9281-128">In Regulatory Configuration Service (RCS), go to **Globalization Features** \> **Tax**.</span></span>
2. <span data-ttu-id="e9281-129">**追加** を選択し、新しい機能に関する情報を入力し、**機能の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9281-129">Select **Add**, enter information about the new feature, and then select **Create feature**.</span></span>
3. <span data-ttu-id="e9281-130">**バージョン** タブで機能を選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9281-130">On the **Versions** tab, select the feature, and then select **Edit**.</span></span>
4. <span data-ttu-id="e9281-131">**全般** タブの **コンフィギュレーション バージョン** フィールドで、カスタマイズされた税コンフィギュレーションおよびバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="e9281-131">On the **General** tab, in the **Configuration version** field, select the customized tax configuration and version.</span></span>
5. <span data-ttu-id="e9281-132">**列の管理** ダイアログ ボックスで、カスタマイズした税対策に含めるヘッダーおよび行の列を選択し、右矢印ボタンを選択して **選択した列** リストに追加します 。</span><span class="sxs-lookup"><span data-stu-id="e9281-132">In the **Manage columns** dialog box, select the header and line columns that you want to include in your customized tax measure, and then select the right arrow button to add them to the **Selected columns** list.</span></span>
