---
title: AX 2009 の移行 - パッケージ テンプレートの作成
description: このトピックでは、Microsoft Dynamics AX 2009 から Finance and Operations へデータを移行するために使用できるパッケージ テンプレートを作成する方法について説明します。
author: kfend
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2018-06-21
ms.dyn365.ops.version: Platform update 17
ms.openlocfilehash: 4469c12bc67bc9ecdc0bece1c0509c0c4a3bd453
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550897"
---
# <a name="ax-2009-migration--create-package-templates"></a><span data-ttu-id="9e6af-103">AX 2009 の移行 － パッケージ テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="9e6af-103">AX 2009 migration – Create package templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e6af-104">パッケージを作成するには、事前に定義された順序に従います。</span><span class="sxs-lookup"><span data-stu-id="9e6af-104">Packages are created by following a predefined sequence.</span></span> <span data-ttu-id="9e6af-105">この順序は、データ エンティティが互いに持つ依存関係に基づいています。</span><span class="sxs-lookup"><span data-stu-id="9e6af-105">This sequence is based on the dependencies that the data entities have on each another.</span></span> <span data-ttu-id="9e6af-106">これらの依存関係のため、データ エンティティをインポートする場合、定義されている順序でデータ エンティティをインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e6af-106">Because of these dependencies, when you import data entities, you must import the data entities in the defined order.</span></span> <span data-ttu-id="9e6af-107">そうしないと、インポートおよびコンフィギュレーション中に問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9e6af-107">Otherwise, you might encounter issues during import and configuration.</span></span>

<span data-ttu-id="9e6af-108">データ移行ツール (DMT) には、次の図に示すように、20 の事前に定義されたテンプレートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="9e6af-108">The Data migration tool (DMT) provides twenty predefined templates, as shown in the following illustration.</span></span>

<span data-ttu-id="9e6af-109">[![データ エンティティ インポート テンプレートの一覧](./media/data-entity-templates.png)](./media/data-entity-templates.png)</span><span class="sxs-lookup"><span data-stu-id="9e6af-109">[![Data entity import template list](./media/data-entity-templates.png)](./media/data-entity-templates.png)</span></span>

<span data-ttu-id="9e6af-110">既存のテンプレートをカスタマイズできます。または、必要に応じて、独自のテンプレートを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="9e6af-110">You can customize an existing template, or you can create your own templates as you require.</span></span>

<span data-ttu-id="9e6af-111">この手順に従って、移行用のテンプレートで使用されるエンティティの一覧を表示して選択します。</span><span class="sxs-lookup"><span data-stu-id="9e6af-111">Follow these steps to view and select the entity lists that will be used in the templates for migration.</span></span>

1. <span data-ttu-id="9e6af-112">Microsoft Dynamics AX 2009 で、**データ移行** \> **共通フォーム** \> **エンティティ リスト**を順にクリックしてから、**順序の適用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e6af-112">In Microsoft Dynamics AX 2009, click **Data migration** \> **Common forms** \> **Entity list**, and then click **Apply sequence**.</span></span> <span data-ttu-id="9e6af-113">メッセージ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9e6af-113">Close the message box.</span></span>
2. <span data-ttu-id="9e6af-114">正しい法人が選択されていることを確認し、**表示** フィールドで、すべてのエンティティまたは移行のために考慮すべきエンティティのみのいずれを表示するかを選択します。</span><span class="sxs-lookup"><span data-stu-id="9e6af-114">Verify that the correct legal entity is selected, and then, in the **Show** field, select to view either all entities or only those entities that should be considered for migration.</span></span>
3. <span data-ttu-id="9e6af-115">**テンプレート名** フィールドで、テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="9e6af-115">In the **Template name** field, select a template.</span></span>
4. <span data-ttu-id="9e6af-116">**選択されているモジュール** ウィンドウで、移行するデータ エンティティを含むモジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="9e6af-116">In the **Module selected** pane, select the module that contains the data entities to migrate.</span></span>
5. <span data-ttu-id="9e6af-117">**エンティティの詳細** タブで、移行するすべてのエンティティ行の **移行対象として選択** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="9e6af-117">On the **Entity details** tab, select the **Select for migration** check box for every entity line that you want to migrate.</span></span>
6. <span data-ttu-id="9e6af-118">**順序の適用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e6af-118">Click **Apply sequence**.</span></span>
7. <span data-ttu-id="9e6af-119">カスタマイズされたテンプレートを作成するには、アプリケーション オブジェクト ツリーで、**リソース** に移動し、XML 形式で新しいテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="9e6af-119">To create a customized template, in the Application Object Tree, go to **Resources**, and create a new template in XML format.</span></span>