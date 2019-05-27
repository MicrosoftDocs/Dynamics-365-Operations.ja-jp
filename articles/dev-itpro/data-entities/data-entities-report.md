---
title: 標準データ エンティティに関する情報を検索します。
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations で使用可能な標準データ エンティティに関する情報を取得する方法について説明します。
author: margoc
manager: AnnBe
ms.date: 12/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 202654
ms.assetid: 6ec8ea87-ea1e-4a10-9d67-2b6565c5c62e
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 568b32f7a0cb180ba4f76df0f19c856b925fdf5f
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1505426"
---
# <a name="find-information-about-standard-data-entities"></a><span data-ttu-id="9f822-103">標準データ エンティティに関する情報の検索</span><span class="sxs-lookup"><span data-stu-id="9f822-103">Find information about standard data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f822-104">Microsoft Dynamics 365 for Finance and Operations には、数多くの既定のデータ エンティティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9f822-104">Microsoft Dynamics 365 for Finance and Operations, ships with many default data entities.</span></span> <span data-ttu-id="9f822-105">データ エンティティは頻繁に更新されるため、ドキュメント化のために、データ エンティティ テンプレートを使用して、どのオーダーデータエンティティをインポートする必要があるかを示します。また、各リリースで出荷されるデータ エンティティのリストも使用します。</span><span class="sxs-lookup"><span data-stu-id="9f822-105">Data entities are frequently updated, so for documentation, we rely on the data entity templates to indicate which order data entities should be imported in, and on reports for a list of data entities that ship with each release.</span></span>

## <a name="configuration-data-packages"></a><span data-ttu-id="9f822-106">コンフィギュレーション データ パッケージ</span><span class="sxs-lookup"><span data-stu-id="9f822-106">Configuration data packages</span></span>
<span data-ttu-id="9f822-107">Microsoft Dynamics Lifecycle Services (LCS) のコンフィギュレーション データ パッケージには、コンフィギュレーション エンティティのスプレッドシートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9f822-107">Configuration data packages on Microsoft Dynamics Lifecycle Services (LCS) contain configuration entity spreadsheets.</span></span> <span data-ttu-id="9f822-108">コンフィギュレーション エンティティ スプレッドシートには、Finance and Operations 実装の初期ゴールド ・ ビルドを作成するために使用できるベスト プラクティス データが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9f822-108">Configuration entity spreadsheets contain best practice data that you can use to create an initial golden build of a Finance and Operations implementation.</span></span> <span data-ttu-id="9f822-109">XML ファイルを使用してデータ パッケージ内のデータ エンティティも適切に順序付けされ、1 回のクリックによるインポートを成功させるのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="9f822-109">The data entities in the data packages are also sequenced appropriately using an XML file to help guarantee a successful single-click import of the data.</span></span> <span data-ttu-id="9f822-110">データのインポートを指示することをどうしてお勧めしているかを理解していただくために、コンフィギュレーション データ パッケージをダウンロードして確認することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9f822-110">We recommend that you download and review the configuration data packages to understand how we recommend that you order your data imports.</span></span> <span data-ttu-id="9f822-111">詳細については、[データ テンプレートのコンフィギュレーション](configuration-data-templates.md) および [1 つの会社または法人から、別の会社または法人へのコンフィギュレーション データのコピー](copy-configuration.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f822-111">For more information, see [Configuration data templates](configuration-data-templates.md) and [Copy configuration data from one company or legal entity to another](copy-configuration.md).</span></span>

## <a name="data-entity-reports"></a><span data-ttu-id="9f822-112">データ エンティティ レポート</span><span class="sxs-lookup"><span data-stu-id="9f822-112">Data entity reports</span></span>
<span data-ttu-id="9f822-113">Microsoft は、データ エンティティの次のレポートを提供しており、[技術参照レポート](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="9f822-113">Microsoft provides the following reports for data entities, which can be downloaded from [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep):</span></span>

- <span data-ttu-id="9f822-114">**データ エンティティ**は、使用可能な各データ エンティティをリストします。</span><span class="sxs-lookup"><span data-stu-id="9f822-114">**Data entities** lists each data entity that is available.</span></span> <span data-ttu-id="9f822-115">レポートには、エンティティのデータ ソースとエンティティに含まれるフィールドが示されます。</span><span class="sxs-lookup"><span data-stu-id="9f822-115">The report indicates the data source of the entity and the fields included in the entity.</span></span> <span data-ttu-id="9f822-116">このレポートは、データ エンティティが公開されているかどうかも示します。</span><span class="sxs-lookup"><span data-stu-id="9f822-116">The report also indicates whether the data entity is public.</span></span>
- <span data-ttu-id="9f822-117">**データ エンティティ フィールド**は、データエンティティの各フィールドと、それが発生したテーブルを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="9f822-117">**Data entities fields** lists each field in a data entity, and the table that it originates from.</span></span>
- <span data-ttu-id="9f822-118">**データ エンティティの集計**集計データ エンティティと、それぞれに含まれるフィールドを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="9f822-118">**Aggregate data entities** lists the aggregate data entities, and the fields that each contains.</span></span>

<span data-ttu-id="9f822-119">各テーブルとそのテーブルのグループをリスト表示している -- 対象のテーブル レポートを検索する場合もあります。</span><span class="sxs-lookup"><span data-stu-id="9f822-119">You may also find the Tables report of interest--it lists each table, and its table group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9f822-120">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="9f822-120">Additional resources</span></span>
[<span data-ttu-id="9f822-121">データ エンティティのホーム ページ</span><span class="sxs-lookup"><span data-stu-id="9f822-121">Data entities home page</span></span>](data-entities.md)
