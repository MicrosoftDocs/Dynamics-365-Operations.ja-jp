---
title: 標準データ エンティティに関する情報を検索します。
description: このトピックでは、Microsoft Dynamics 365 Finance で使用可能な標準データ エンティティに関する情報を取得する方法について説明します。
author: margoc
manager: AnnBe
ms.date: 12/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 202654
ms.assetid: 6ec8ea87-ea1e-4a10-9d67-2b6565c5c62e
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 917ee9386f4d4ec8521fd0c1787edce6d0da2c93
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183434"
---
# <a name="find-information-about-standard-data-entities"></a><span data-ttu-id="41fd4-103">標準データ エンティティに関する情報の検索</span><span class="sxs-lookup"><span data-stu-id="41fd4-103">Find information about standard data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41fd4-104">アプリケーションには、既定のデータ エンティティが数多く含まれています。</span><span class="sxs-lookup"><span data-stu-id="41fd4-104">The application ships with many default data entities.</span></span> <span data-ttu-id="41fd4-105">データ エンティティは頻繁に更新されるため、ドキュメント化のために、データ エンティティ テンプレートを使用して、どのオーダーデータエンティティをインポートする必要があるかを示します。また、各リリースで出荷されるデータ エンティティのリストも使用します。</span><span class="sxs-lookup"><span data-stu-id="41fd4-105">Data entities are frequently updated, so for documentation, we rely on the data entity templates to indicate which order data entities should be imported in, and on reports for a list of data entities that ship with each release.</span></span>

## <a name="configuration-data-packages"></a><span data-ttu-id="41fd4-106">コンフィギュレーション データ パッケージ</span><span class="sxs-lookup"><span data-stu-id="41fd4-106">Configuration data packages</span></span>
<span data-ttu-id="41fd4-107">Microsoft Dynamics Lifecycle Services (LCS) のコンフィギュレーション データ パッケージには、コンフィギュレーション エンティティのスプレッドシートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="41fd4-107">Configuration data packages on Microsoft Dynamics Lifecycle Services (LCS) contain configuration entity spreadsheets.</span></span> <span data-ttu-id="41fd4-108">コンフィギュレーション エンティティ スプレッドシートには、実装の初期ゴールド ビルドを作成するために使用できるベスト プラクティス データが含まれています。</span><span class="sxs-lookup"><span data-stu-id="41fd4-108">Configuration entity spreadsheets contain best practice data that you can use to create an initial golden build of an implementation.</span></span> <span data-ttu-id="41fd4-109">XML ファイルを使用してデータ パッケージ内のデータ エンティティも適切に順序付けされ、1 回のクリックによるインポートを成功させるのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="41fd4-109">The data entities in the data packages are also sequenced appropriately using an XML file to help guarantee a successful single-click import of the data.</span></span> <span data-ttu-id="41fd4-110">データのインポートを指示することをどうしてお勧めしているかを理解していただくために、コンフィギュレーション データ パッケージをダウンロードして確認することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="41fd4-110">We recommend that you download and review the configuration data packages to understand how we recommend that you order your data imports.</span></span> <span data-ttu-id="41fd4-111">詳細については、[データ テンプレートのコンフィギュレーション](configuration-data-templates.md) および [1 つの会社または法人から、別の会社または法人へのコンフィギュレーション データのコピー](copy-configuration.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="41fd4-111">For more information, see [Configuration data templates](configuration-data-templates.md) and [Copy configuration data from one company or legal entity to another](copy-configuration.md).</span></span>

## <a name="data-entity-reports"></a><span data-ttu-id="41fd4-112">データ エンティティ レポート</span><span class="sxs-lookup"><span data-stu-id="41fd4-112">Data entity reports</span></span>
<span data-ttu-id="41fd4-113">Microsoft は、データ エンティティの次のレポートを提供しており、[技術参照レポート](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="41fd4-113">Microsoft provides the following reports for data entities, which can be downloaded from [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep):</span></span>

- <span data-ttu-id="41fd4-114">**データ エンティティ**は、使用可能な各データ エンティティをリストします。</span><span class="sxs-lookup"><span data-stu-id="41fd4-114">**Data entities** lists each data entity that is available.</span></span> <span data-ttu-id="41fd4-115">レポートには、エンティティのデータ ソースとエンティティに含まれるフィールドが示されます。</span><span class="sxs-lookup"><span data-stu-id="41fd4-115">The report indicates the data source of the entity and the fields included in the entity.</span></span> <span data-ttu-id="41fd4-116">このレポートは、データ エンティティが公開されているかどうかも示します。</span><span class="sxs-lookup"><span data-stu-id="41fd4-116">The report also indicates whether the data entity is public.</span></span>
- <span data-ttu-id="41fd4-117">**データ エンティティ フィールド**は、データエンティティの各フィールドと、それが発生したテーブルを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="41fd4-117">**Data entities fields** lists each field in a data entity, and the table that it originates from.</span></span>
- <span data-ttu-id="41fd4-118">**データ エンティティの集計**集計データ エンティティと、それぞれに含まれるフィールドを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="41fd4-118">**Aggregate data entities** lists the aggregate data entities, and the fields that each contains.</span></span>

<span data-ttu-id="41fd4-119">各テーブルとそのテーブルのグループをリスト表示している -- 対象のテーブル レポートを検索する場合もあります。</span><span class="sxs-lookup"><span data-stu-id="41fd4-119">You may also find the Tables report of interest--it lists each table, and its table group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="41fd4-120">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="41fd4-120">Additional resources</span></span>
[<span data-ttu-id="41fd4-121">データ エンティティのホーム ページ</span><span class="sxs-lookup"><span data-stu-id="41fd4-121">Data entities home page</span></span>](data-entities.md)
