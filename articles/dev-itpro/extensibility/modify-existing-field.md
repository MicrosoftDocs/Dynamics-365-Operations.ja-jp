---
title: "テーブルの既存のフィールドの変更"
description: "このトピックでは、テーブル内の既存のフィールドを変更する方法について説明します。"
author: ivanv-microsoft
manager: AnnBe
ms.date: 07/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: 
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f48298370836764814cf36a8079abaadb7282bac
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="modify-an-existing-field-in-a-table"></a><span data-ttu-id="6a001-103">テーブルの既存のフィールドの変更</span><span class="sxs-lookup"><span data-stu-id="6a001-103">Modify an existing field in a table</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a001-104">テーブル内の既存のフィールドのプロパティを変更するには、まずテーブルの拡張を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a001-104">To modify properties on an existing field in a table, you must first create an extension for the table.</span></span> <span data-ttu-id="6a001-105">次のプロパティを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="6a001-105">You can modify the following properties:</span></span>

- <span data-ttu-id="6a001-106">**ラベル**</span><span class="sxs-lookup"><span data-stu-id="6a001-106">**Label**</span></span>
- <span data-ttu-id="6a001-107">**ヘルプ テキスト**</span><span class="sxs-lookup"><span data-stu-id="6a001-107">**Help text**</span></span>
- <span data-ttu-id="6a001-108">**国地域コード**</span><span class="sxs-lookup"><span data-stu-id="6a001-108">**Country Region Codes**</span></span>
- <span data-ttu-id="6a001-109">**拡張データ型** - 現在選択されている EDT から派生した拡張データ型 (EDT) のみを選択できます。</span><span class="sxs-lookup"><span data-stu-id="6a001-109">**Extended Data Type** – You can select only extended data types (EDTs) that are derived from the currently selected EDT.</span></span> <span data-ttu-id="6a001-110">プロパティ シートのルックアップはフィルタリングされ、それらの EDT のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a001-110">The lookup in the property sheet is filtered so that only those EDTs are shown.</span></span> <span data-ttu-id="6a001-111">たとえば、InventTable テーブルの**重量**フィールドで EDT を編集するには、**BOMMeasureWidth** に基づく派生した EDT を作成できます。次に、**InventTable** 拡張子の**重量**フィールドで、**拡張データ型**プロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="6a001-111">For example, to edit the EDT on the **Weight** field in the InventTable table, you can create a derived EDT that is based on **BOMMeasureWidth**, and then modify the **Extended Data Type** property on the **Weight** field in the **InventTable** extension.</span></span> <span data-ttu-id="6a001-112">この方法で、新しいパッケージが配置されるときに、ユーザー インターフェイスで**幅**フィールドの外観を変更できます。</span><span class="sxs-lookup"><span data-stu-id="6a001-112">In this way, you can modify the look and feel of the **Width** field in the user interface when the new package is deployed.</span></span>

![既存のフィールドの変更](media/modify-table-property.jpg) 

