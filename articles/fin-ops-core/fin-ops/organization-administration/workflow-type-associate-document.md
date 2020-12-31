---
title: ワークフロー ドキュメント クラスをワークフロー タイプと関連付ける
description: このトピックでは、ワークフロー タイプにワークフロー ドキュメント クラスを関連付ける方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 202694
ms.assetid: 33349e0d-d8ac-4d20-8f9b-5f85d4e01004
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 47f76a08aa440a540cfc5f1ada21af5c0f526ceb
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693172"
---
# <a name="associate-a-workflow-document-class-with-a-workflow-type"></a><span data-ttu-id="cbe8a-103">ワークフロー ドキュメント クラスとワークフロー タイプの関連付け</span><span class="sxs-lookup"><span data-stu-id="cbe8a-103">Associate a workflow document class with a workflow type</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cbe8a-104">ワークフローを作成するには、ワークフロー ドキュメント クラスをワークフロー タイプにバインドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cbe8a-104">To create a workflow, you must bind a workflow document class to the workflow type.</span></span> <span data-ttu-id="cbe8a-105">ワークフロー ドキュメント クラスには、ワークフローが使用するテーブル データ フィールドへの参照が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cbe8a-105">The workflow document class contains references to the table data fields that the workflow uses.</span></span> <span data-ttu-id="cbe8a-106">このトピックでは、ワークフロー タイプにワークフロー ドキュメント クラスをバインドする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cbe8a-106">This topic describes how to bind a workflow document class to a workflow type.</span></span>

> [!NOTE]
> <span data-ttu-id="cbe8a-107">**ワークフロー** ウィザードを使用してワークフロー タイプを作成した場合は、ワークフロー ドキュメント クラスをワークフロー タイプに既にバインドしています。</span><span class="sxs-lookup"><span data-stu-id="cbe8a-107">If you used the **Workflow** wizard to create the workflow type, the wizard has already bound the workflow document class to the workflow type.</span></span>

<span data-ttu-id="cbe8a-108">次の手順を開始する前に、コンフィギュレーション ユーザー インターフェイス (UI) の条件に使用されるテーブル フィールドを公開するためのワークフロー ドキュメント クラスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cbe8a-108">Before you begin the following procedure, you must create a workflow document class to expose the table fields that are used for conditions in the configuration user interface (UI).</span></span> <span data-ttu-id="cbe8a-109">詳細については、 [新しいワークフロー ドキュメント クラスの作成](workflow-type-document-create.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cbe8a-109">For more information, see [Create a workflow document class](workflow-type-document-create.md).</span></span>

## <a name="bind-a-workflow-document-class-to-a-workflow-type"></a><span data-ttu-id="cbe8a-110">ワークフロー ドキュメント クラスをワークフロー タイプにバインドする</span><span class="sxs-lookup"><span data-stu-id="cbe8a-110">Bind a workflow document class to a workflow type</span></span>

1. <span data-ttu-id="cbe8a-111">アプリケーション エクスプローラーで、 **ワークフロー** ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="cbe8a-111">In Application Explorer, expand the **Workflow** node.</span></span>
2. <span data-ttu-id="cbe8a-112">**ワークフロー タイプ** ノードで、ワークフロー ドキュメント クラスをバインドするワークフロー タイプを右クリックし、 **プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cbe8a-112">In the **Workflow Types** node, right-click the workflow type that you want to bind a workflow document class to, and then select **Properties**.</span></span>
3. <span data-ttu-id="cbe8a-113">**プロパティ** シートで、 **ドキュメント** プロパティをワークフロー ドキュメントを定義するワークフロー ドキュメント クラスに設定します。</span><span class="sxs-lookup"><span data-stu-id="cbe8a-113">On the **Properties** sheet, set the **Document** property to the workflow document class that defines the workflow document.</span></span>

## <a name="see-also"></a><span data-ttu-id="cbe8a-114">参照</span><span class="sxs-lookup"><span data-stu-id="cbe8a-114">See also</span></span>

[<span data-ttu-id="cbe8a-115">新しいワークフロー タイプの作成</span><span class="sxs-lookup"><span data-stu-id="cbe8a-115">Create a new workflow type</span></span>](workflow-type-create-new.md)

[<span data-ttu-id="cbe8a-116">ワークフロー ドキュメント クラスの作成</span><span class="sxs-lookup"><span data-stu-id="cbe8a-116">Create a workflow document class</span></span>](workflow-type-document-create.md)
