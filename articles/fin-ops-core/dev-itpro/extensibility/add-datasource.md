---
title: 拡張機能によって、フォームにデータ ソースを追加
description: このトピックでは、拡張機能を使用して、既存のフォームに新しいデータ ソースを追加する方法について説明します。
author: ivanv-microsoft
manager: AnnBe
ms.date: 07/10/2017
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
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 521cd1cd77739d69027b4c87bc7d544d5c6fd6c9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183337"
---
# <a name="add-data-sources-to-forms-through-extension"></a><span data-ttu-id="70ff9-103">拡張機能によって、フォームにデータ ソースを追加</span><span class="sxs-lookup"><span data-stu-id="70ff9-103">Add data sources to forms through extension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70ff9-104">多くの場合、既存のテーブルに保管されている情報は、顧客の要求を満たしていません。</span><span class="sxs-lookup"><span data-stu-id="70ff9-104">Often, the information that is stored in existing tables doesn't satisfy customer requirements.</span></span> <span data-ttu-id="70ff9-105">したがって、追加のテーブルを作成し、それらのテーブルのデータをページに表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="70ff9-105">Therefore, additional tables must be created, and data from those tables must be shown on pages.</span></span>

<span data-ttu-id="70ff9-106">拡張機能を介して既存のフォームに新しいデータ ソースを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="70ff9-106">You can add new data sources to existing forms through extension.</span></span> <span data-ttu-id="70ff9-107">以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="70ff9-107">Follow these steps.</span></span>

1. <span data-ttu-id="70ff9-108">拡張モデルでは、選択したフォームにフォームの拡張機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="70ff9-108">In the extension model, create a form extension for the selected form.</span></span>
1. <span data-ttu-id="70ff9-109">フォーム拡張を右クリックし、**新しいデータ ソース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="70ff9-109">Right-click the form extension, and then select **New Data Source**.</span></span>

    ![フォーム データ ソースの追加](media/AddFormDataSource01.jpg)

1. <span data-ttu-id="70ff9-111">**テーブル** プロパティと、データ ソースのその他のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="70ff9-111">Specify the **Table** property and other required properties on the data source.</span></span> <span data-ttu-id="70ff9-112">たとえば、データ ソースが、フォームの他のデータ ソースにリンクする方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="70ff9-112">For example, define how the data source should be linked with the other data sources for the form.</span></span> 
1. <span data-ttu-id="70ff9-113">次の図に示すように、フィールドを新しいデータ ソースからフォーム デザインにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="70ff9-113">Drag fields from the new data source into the form design, as shown in the following illustration.</span></span>

    ![データ ソースからフォーム デザインへのフィールドの追加](media/AddFormDataSource02.jpg)

1. <span data-ttu-id="70ff9-115">同様の方法で、既存のデータ ソースからフィールドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="70ff9-115">In a similar manner, you can add fields from existing data sources.</span></span> <span data-ttu-id="70ff9-116">たとえば、次の図に示すように、フォームの背後にあるテーブルは、追加のフィールドで拡張された可能性があります。</span><span class="sxs-lookup"><span data-stu-id="70ff9-116">For example, the table behind the form might have been extended with additional fields, as shown in the following illustration.</span></span>

    ![追加のフィールドを持つデータ ソース](media/AddFormDataSource03.jpg)

    > [!TIP]
    > <span data-ttu-id="70ff9-118">フォーム拡張データ ソースを右クリックしてから、**復元** を選択し、新しいフィールドがリストに表示されるようにする場合があります。</span><span class="sxs-lookup"><span data-stu-id="70ff9-118">You might have to right-click the form extension data source and then select **Restore** to make the new fields appear in the list.</span></span>

1. <span data-ttu-id="70ff9-119">次の図に示されるように、これらの新しいフィールドおよびテーブル内でデータを表示して編集できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="70ff9-119">You can now view and edit the data in these new fields and tables, as shown in the following illustration.</span></span>

    ![新しいフィールド](media/AddFormDataSource04.jpg)
