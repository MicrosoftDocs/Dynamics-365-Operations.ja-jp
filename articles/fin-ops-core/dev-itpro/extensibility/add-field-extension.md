---
title: 拡張機能を使用してテーブルにフィールドを追加
description: このトピックでは、テーブル拡張機能を使用してテーブルにフィールドを追加する方法について説明します。
author: ivanv-microsoft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-06-01
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 3a8c671e1d36603a963b2eecb756a713e40055c7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183336"
---
# <a name="add-fields-to-tables-through-extension"></a><span data-ttu-id="6a7cd-103">拡張機能を使用してテーブルにフィールドを追加</span><span class="sxs-lookup"><span data-stu-id="6a7cd-103">Add fields to tables through extension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a7cd-104">既存のテーブルに新しいフィールドを追加するには、まずテーブル拡張を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a7cd-104">To add a new field to an existing table, you must first create a table extension.</span></span> <span data-ttu-id="6a7cd-105">たとえば、リリース済製品の半径を持つフィールドを追加するには、次の図に示すように、モデル内で InventTable テーブルの拡張機能を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a7cd-105">For example, to add a field that holds the radius of the released product, you must create an extension for the InventTable table in your model, as shown in the following illustration.</span></span>

![拡張子の作成](media/TableNewField01.jpg) 

<span data-ttu-id="6a7cd-107">モデル内でフィールドをテーブルに追加するのと同様に、フィールドを拡張機能に追加することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6a7cd-107">You can now add the field to the extension, just as you would add a field to a table in your model.</span></span> <span data-ttu-id="6a7cd-108">2 つの方法を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6a7cd-108">You can use two methods:</span></span>

+ <span data-ttu-id="6a7cd-109">デザイナーで、**フィールド** ノードを右クリックし、**新規**を選択してから、追加するフィールドのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="6a7cd-109">In the designer, right-click the **Fields** node, select **New**, and then select the type of field to add.</span></span>
+ <span data-ttu-id="6a7cd-110">プロジェクトから既存の Extended Data Type または Base Enumeration を**フィールド**ノードにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="6a7cd-110">Drag an existing Extended Data Type or Base Enumeration from your project onto the **Fields** node.</span></span>

<span data-ttu-id="6a7cd-111">完了したら、新しいフィールドのプロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="6a7cd-111">When you've finished, you can modify the properties of the new field.</span></span> <span data-ttu-id="6a7cd-112">次の図では、**ラベル** プロパティのみが変更されました。</span><span class="sxs-lookup"><span data-stu-id="6a7cd-112">In the following illustration, only the **Label** property was modified.</span></span>

![新しいフィールドのプロパティの変更](media/TableNewField02.jpg)

<span data-ttu-id="6a7cd-114">必要に応じて、新しいフィールドを既存のフィールド グループのいずれか、または作成する新しいフィールド グループに追加することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6a7cd-114">You can now optionally add the new field either to one of the existing field groups or to a new field group that you create.</span></span> <span data-ttu-id="6a7cd-115">次の図では、**半径**フィールドが **PhysicalDimensions** フィールド グループに追加されました。</span><span class="sxs-lookup"><span data-stu-id="6a7cd-115">In the following illustration, the **Radius** field was added to the **PhysicalDimensions** field group.</span></span>

![フィールド グループへの新しいフィールドの追加](media/TableNewField03.jpg)

<span data-ttu-id="6a7cd-117">コンパイルとデータベースの同期の後、ユーザー インターフェイスで新しいフィールドを表示および編集することができます。</span><span class="sxs-lookup"><span data-stu-id="6a7cd-117">After compilation and synchronization of the database, you can see and edit the new field in the user interface.</span></span>

![ユーザー インターフェイスの新しいフィールド](media/TableNewField04.jpg)
