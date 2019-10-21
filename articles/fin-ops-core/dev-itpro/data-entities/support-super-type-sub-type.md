---
title: スーパー タイプおよびサブ タイプ
description: データ エンティティの継承パターンのサポートについて説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 25331
ms.assetid: d59cefc0-be94-42e9-a22e-87493985dbcd
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04254a8f68018e9823cae117c3c0a8cc109934d6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183422"
---
# <a name="super-types-and-sub-types"></a><span data-ttu-id="ba3eb-103">スーパー タイプおよびサブ タイプ</span><span class="sxs-lookup"><span data-stu-id="ba3eb-103">Super types and sub types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba3eb-104">データ エンティティの継承パターンのサポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-104">Describes support for inheritance patterns in data entities.</span></span>

## <a name="patterns"></a><span data-ttu-id="ba3eb-105">パターン</span><span class="sxs-lookup"><span data-stu-id="ba3eb-105">Patterns</span></span>

<span data-ttu-id="ba3eb-106">継承を含むテーブルのエンティティを作成する方法はいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-106">There are several ways to create entities for tables that involve inheritance:</span></span>

- <span data-ttu-id="ba3eb-107">**データ ソースとしてのリーフ/具象型:** 具象型をデータソースとして使用すると、基本型と現在の型の両方のフィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-107">**Leaf/concrete type as data source:** If a concrete type is used as a data source, fields are displayed for both the base type and the current type.</span></span> <span data-ttu-id="ba3eb-108">たとえば、次のスクリーン ショットでは、DirPerson がデータ ソースである場合、DirPerson および DirPartytable の両方からのデータ ソース フィールドを表示します。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-108">For example, in the following screen shots, if DirPerson is the data source, data source fields from both DirPerson and DirPartytable appear.</span></span>

    <span data-ttu-id="ba3eb-109">[![sub1](./media/sub1.png)](./media/sub1.png)</span><span class="sxs-lookup"><span data-stu-id="ba3eb-109">[![sub1](./media/sub1.png)](./media/sub1.png)</span></span>

    <span data-ttu-id="ba3eb-110">[![sub2](./media/sub2-419x1024.png)](./media/sub2.png)</span><span class="sxs-lookup"><span data-stu-id="ba3eb-110">[![sub2](./media/sub2-419x1024.png)](./media/sub2.png)</span></span>

- <span data-ttu-id="ba3eb-111">**データ ソースとしての抽象タイプ/非リーフ:** 非リーフ タイプをデータ ソースとして使用する場合、基準タイプと現在のタイプの両方にフィールドが表示されますが、派生型のフィールドは表示されません。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-111">**Abstract type/non-leaf as data source:** If a non-leaf type is used as a data source, fields are displayed for both the base type and the current type, but fields from any derived types aren't displayed.</span></span> <span data-ttu-id="ba3eb-112">次のスクリーン ショットに示すように、派生型からのフィールドは派生データ ソースから追加される必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-112">Fields from derived types must be added from derived data sources, as shown in the following screen shot.</span></span>

    <span data-ttu-id="ba3eb-113">[![sub3](./media/sub3.png)](./media/sub3.png)</span><span class="sxs-lookup"><span data-stu-id="ba3eb-113">[![sub3](./media/sub3.png)](./media/sub3.png)</span></span>

## <a name="data-entity-view-wizard"></a><span data-ttu-id="ba3eb-114">データ エンティティの表示ウィザード</span><span class="sxs-lookup"><span data-stu-id="ba3eb-114">Data Entity View wizard</span></span>
<span data-ttu-id="ba3eb-115">**データ エンティティ ビュー** ウィザードを使用すると、継承に含まれるテーブルがプライマリ データ ソース (および追加データ ソース) である場所で、データ エンティティを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-115">You can use the **Data Entity View** wizard to create data entities where the primary data source (and additional data sources) can be tables that are involved in inheritance.</span></span>

> [!NOTE]
> <span data-ttu-id="ba3eb-116">現在、ウィザードは派生データ ソースをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-116">Currently, the wizard doesn't support derived data sources.</span></span> <span data-ttu-id="ba3eb-117">現在の型または基本データ型からフィールドのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-117">It shows only fields from the current type or the base type.</span></span> <span data-ttu-id="ba3eb-118">エンティティを作成した後、手動で派生データ ソースを表示するよう変更できます。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-118">After you create an entity, you can manually modify it to display derived data sources.</span></span>

<span data-ttu-id="ba3eb-119">次のスクリーン ショットは、DirPartyTable がプライマリ データ ソースである、ウィザードを使用して作成されたデータ エンティティを示しています。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-119">The following screen shots show a data entity that was created by using the wizard, where DirPartyTable is the primary data source.</span></span>

<span data-ttu-id="ba3eb-120">[![sub4](./media/sub4.png)](./media/sub4.png)</span><span class="sxs-lookup"><span data-stu-id="ba3eb-120">[![sub4](./media/sub4.png)](./media/sub4.png)</span></span>

1. <span data-ttu-id="ba3eb-121">データ ソース テーブルを **DirPartyTabl** に更新します。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-121">Update the data source table to **DirPartyTabl**.</span></span>

    <span data-ttu-id="ba3eb-122">[![sub5](./media/sub5.png)](./media/sub5.png)</span><span class="sxs-lookup"><span data-stu-id="ba3eb-122">[![sub5](./media/sub5.png)](./media/sub5.png)</span></span>

2. <span data-ttu-id="ba3eb-123">データ ソース テーブルを **DirPartyTable** に更新します。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-123">Update the data source table to **DirPartyTable**.</span></span>

    <span data-ttu-id="ba3eb-124">[![sub6](./media/sub6.png)](./media/sub6.png)</span><span class="sxs-lookup"><span data-stu-id="ba3eb-124">[![sub6](./media/sub6.png)](./media/sub6.png)</span></span>

## <a name="run-time"></a><span data-ttu-id="ba3eb-125">実行時間</span><span class="sxs-lookup"><span data-stu-id="ba3eb-125">Run time</span></span>
<span data-ttu-id="ba3eb-126">継承に関連するエンティティの実行時動作があります。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-126">There is run-time behavior for entities that related to inheritance.</span></span>

### <a name="creating-entities-for-specified-types"></a><span data-ttu-id="ba3eb-127">指定したタイプのエンティティを作成しています</span><span class="sxs-lookup"><span data-stu-id="ba3eb-127">Creating entities for specified types</span></span>

<span data-ttu-id="ba3eb-128">この例では、個別の**個人**および**組織**エンティティを作成します。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-128">In this example, we create separate **Person** and **Organization** entities.</span></span> <span data-ttu-id="ba3eb-129">**担当者** エンティティのプライマリ データ ソースは DirPerson で、**組織** エンティティのプライマリ データ ソースは DirOrganization です。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-129">The primary data source for the **Person** entity is DirPerson, and the primary data source for the **Organization** entity is DirOrganization.</span></span> <span data-ttu-id="ba3eb-130">この方法は、次のスクリーン ショットに反映されていますが、特別なランタイム コードを記述する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-130">This approach, which is reflected in the following screen shots, doesn't require that you write any special run-time code.</span></span>

<span data-ttu-id="ba3eb-131">[![sub7](./media/sub7.png)](./media/sub7.png)</span><span class="sxs-lookup"><span data-stu-id="ba3eb-131">[![sub7](./media/sub7.png)](./media/sub7.png)</span></span>

<span data-ttu-id="ba3eb-132">[![sub8](./media/sub8-419x1024.png)](./media/sub8.png)</span><span class="sxs-lookup"><span data-stu-id="ba3eb-132">[![sub8](./media/sub8-419x1024.png)](./media/sub8.png)</span></span>

### <a name="creating-entities-for-generalized-types"></a><span data-ttu-id="ba3eb-133">一般化されたタイプのエンティティを作成しています</span><span class="sxs-lookup"><span data-stu-id="ba3eb-133">Creating entities for generalized types</span></span>

<span data-ttu-id="ba3eb-134">この例では、単一のエンティティである**パーティ**を作成して、**個人**および**組織**の両方に使用できます。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-134">In this example, we create a single entity, **Party**, that can be used for both **Person** and **Organization**.</span></span> <span data-ttu-id="ba3eb-135">プライマリ データ ソースが DirPartyTable で、派生データ ソースが DirPerson と DirOrganization です。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-135">The primary data source is DirPartyTable, and derived data sources are DirPerson and DirOrganization.</span></span> <span data-ttu-id="ba3eb-136">新しいエンティティには、次のようなフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-136">The new entity contains the following kinds of fields:</span></span>

- <span data-ttu-id="ba3eb-137">**一般的な属性** -**個人**または**組織**に固有ではない属性 (例: **名前**)</span><span class="sxs-lookup"><span data-stu-id="ba3eb-137">**Common attributes** – Attributes that aren't specific to **Person** or **Organization**, such as **Name**.</span></span> <span data-ttu-id="ba3eb-138">これらのフィールドは、DirPartyTable にマップされます。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-138">These fields are mapped to DirPartyTable.</span></span>
- <span data-ttu-id="ba3eb-139">**個人の固有の属性** – **性別**、**配偶者の有無**など。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-139">**Person-specific attributes** – **Gender**, **Marital Status**, and so on.</span></span> <span data-ttu-id="ba3eb-140">これらのフィールドは、派生データ ソース DirPartyTable\_DirPerson にマップされます。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-140">These fields are mapped to derived data source DirPartyTable\_DirPerson.</span></span>
- <span data-ttu-id="ba3eb-141">**組織に固有の属性** – **OrgNumber**、**ABC** などです。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-141">**Organization-specific attributes** – **OrgNumber**, **ABC**, and so on.</span></span> <span data-ttu-id="ba3eb-142">これらのフィールドは、派生データ ソース DirPartyTable\_DirOrganization にマップされます。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-142">These fields are mapped to derived data source DirPartyTable\_DirOrganization.</span></span>

<span data-ttu-id="ba3eb-143">[![sub9](./media/sub9.png)](./media/sub9.png)</span><span class="sxs-lookup"><span data-stu-id="ba3eb-143">[![sub9](./media/sub9.png)](./media/sub9.png)</span></span>

<span data-ttu-id="ba3eb-144">デザイン時のタスクとして、ひとつのデータエンティティで基本型と複数の派生型のフィールドをマッピングします。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-144">Mapping fields from base and multiple derived types in a single data entity is a design-time task.</span></span> <span data-ttu-id="ba3eb-145">ただし、実行時に、各派生型が作成されるときを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-145">However, at run time, we must specify when each derived type should be created.</span></span> <span data-ttu-id="ba3eb-146">これは、**InstanceRelationType** などのフィールドに基づいても、異なるタイプを表す **String** を使用するように計算カラムを作成もできます。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-146">This can be based on fields such as **InstanceRelationType**, or a computed column can be created to use **String** to represent different types.</span></span> <span data-ttu-id="ba3eb-147">**関係者**エンティティの例で、**PartyType** 計算列を作成して**個人**および**組織**の派生型を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-147">In the **Party** entity example, a **PartyType** computed column can be created to represent the **Person** and **Organization** derived types.</span></span> <span data-ttu-id="ba3eb-148">次のコード スニペットは、このアプローチを示しています。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-148">The following code snippet illustrates this approach.</span></span>

<span data-ttu-id="ba3eb-149">[![sub10](./media/sub10.png)](./media/sub10.png)</span><span class="sxs-lookup"><span data-stu-id="ba3eb-149">[![sub10](./media/sub10.png)](./media/sub10.png)</span></span>

<span data-ttu-id="ba3eb-150">この例では、**関係者**タイプは DirPartyTable の **InstanceRelationType** 列を使用して計算されます。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-150">In this example, the **Party** type is computed by using the **InstanceRelationType** column on DirPartyTable.</span></span> <span data-ttu-id="ba3eb-151">この方法は、データを読み取るために機能します。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-151">This approach works for reading data.</span></span> <span data-ttu-id="ba3eb-152">ただし、**作成**または**更新**操作を行うには、タイプに基づいて、データ エンティティの **initializeEntityDataSource** メソッドを上書きするコードを記述する必要があり、およびデータ ソースの実行時コンテキスト バッファに対する派生型の正しいインスタンスを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba3eb-152">However, to do **Create** or **Update** operations, you must write code where you override the **initializeEntityDataSource** method on the data entity, based on type, and set a correct instance of the derived type for the data source run-time context buffer.</span></span>

<span data-ttu-id="ba3eb-153">[![sub11](./media/sub11.png)](./media/sub11.png)</span><span class="sxs-lookup"><span data-stu-id="ba3eb-153">[![sub11](./media/sub11.png)](./media/sub11.png)</span></span>
