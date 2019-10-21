---
title: ワークフロー タイプのクエリの作成
description: このトピックでは、ワークフロー タイプのクエリを作成する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: 202694
ms.assetid: 33349e0d-d8ac-4d20-8f9b-5f85d4e01004
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 06b83be6e870f374433b278c2943d9a1d3e991ce
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180478"
---
# <a name="create-a-query-for-a-workflow-type"></a><span data-ttu-id="6b86a-103">ワークフロー タイプのクエリの作成</span><span class="sxs-lookup"><span data-stu-id="6b86a-103">Create a query for a workflow type</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b86a-104">ワークフロー タイプを作成する前に、ワークフロー ドキュメントのテーブル フィールドにアクセスするクエリを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b86a-104">Before you create a workflow type, you must create a query that will access the table fields for the workflow document.</span></span> <span data-ttu-id="6b86a-105">このトピックでは、ワークフロー タイプのクエリを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6b86a-105">This topic describes how to create a query for a workflow type.</span></span>

## <a name="create-a-query-for-a-workflow-type"></a><span data-ttu-id="6b86a-106">ワークフロー タイプのクエリの作成</span><span class="sxs-lookup"><span data-stu-id="6b86a-106">Create a query for a workflow type</span></span>

1. <span data-ttu-id="6b86a-107">新しいクエリを作成するには、次のいずれかのステップを実行します</span><span class="sxs-lookup"><span data-stu-id="6b86a-107">Follow one of these steps to create a new query:</span></span>

    + <span data-ttu-id="6b86a-108">アプリケーション エクスプローラーで、 **クエリ** ノードを右クリックしてから、 **新しいクエリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b86a-108">In Application Explorer, right-click the **Queries** node, and then select **New Query**.</span></span> <span data-ttu-id="6b86a-109">クエリ グループは、 **クエリ** ノードの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="6b86a-109">A query group appears under the **Queries** node.</span></span> <span data-ttu-id="6b86a-110">新しいクエリを右クリックし、 **名前の変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b86a-110">Right-click the new query, and then select **Rename**.</span></span> <span data-ttu-id="6b86a-111">クエリの名前を入力します</span><span class="sxs-lookup"><span data-stu-id="6b86a-111">Enter a name for the query.</span></span>
    + <span data-ttu-id="6b86a-112">**プロジェクト** メニューの **新しい項目の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b86a-112">On the **Project** menu, select **Add new item**.</span></span> <span data-ttu-id="6b86a-113">**新しい項目の追加** ダイアログ ボックスで、 **クエリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b86a-113">In the **Add new item** dialog box, select **Query**.</span></span> <span data-ttu-id="6b86a-114">クエリ名を入力し、 **作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b86a-114">Enter a name for the query, and then select **Create**.</span></span>

2. <span data-ttu-id="6b86a-115">新しいクエリを展開し、 **データ ソース** ノードを右クリックして、 **新しいデータ ソース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b86a-115">Expand the new query, right-click the **Data Sources** node, and then select **New Data Source**.</span></span> <span data-ttu-id="6b86a-116">データ ソースグ ループは、 **データ ソース** ノードの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="6b86a-116">A data source group appears under the **Data Sources** node.</span></span>
3. <span data-ttu-id="6b86a-117">新しいデータ ソース グループを右クリックし、 **プロパティ**  を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b86a-117">Right-click the new data source group, and then select **Properties**.</span></span>
4. <span data-ttu-id="6b86a-118">**プロパティ** シートで、ワークフローを定義しているドキュメント タイプのメイン テーブルに対して **テーブル** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6b86a-118">On the **Properties** sheet, set the **Table** property to the main table for the document type that you're defining a workflow for.</span></span>
5. <span data-ttu-id="6b86a-119">アプリケーション オブジェクト ツリー (AOT) で、新しいクエリを右クリックし、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b86a-119">In the Application Object Tree (AOT), right-click the new query, and then select **Save**.</span></span>

<span data-ttu-id="6b86a-120">クエリの作成方法の詳細については、 [AOTを使用したクエリの作成](https://docs.microsoft.com/dynamicsax-2012/developer/how-to-create-queries-by-using-the-aot) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b86a-120">For more information about how to create queries, see [Create queries by using the AOT](https://docs.microsoft.com/dynamicsax-2012/developer/how-to-create-queries-by-using-the-aot).</span></span>
