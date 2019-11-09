---
title: 拡張機能を使用して、テーブルのプロパティを変更する
description: このトピックでは、拡張機能を使用してテーブルのプロパティを変更する方法について説明します。
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
ms.openlocfilehash: 186863dd669f05465b176bf61cea4deacf5c29ab
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183314"
---
# <a name="modify-table-properties-through-extension"></a><span data-ttu-id="2ca3a-103">拡張機能を使用して、テーブルのプロパティを変更する</span><span class="sxs-lookup"><span data-stu-id="2ca3a-103">Modify table properties through extension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ca3a-104">テーブルのプロパティを変更するには、そのテーブルの拡張を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ca3a-104">To modify properties on a table, you must create an extension of that table.</span></span> <span data-ttu-id="2ca3a-105">アプリケーション エクスプローラーで、テーブルを右クリックしてから**拡張機能を作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ca3a-105">In Application Explorer, right-click the table, and then select **Create extension**.</span></span> <span data-ttu-id="2ca3a-106">次の図に示すとおり、新しいテーブル拡張機能は、選択したプロジェクトに作成されます。</span><span class="sxs-lookup"><span data-stu-id="2ca3a-106">A new table extension is created in the selected project, as shown in the following illustration.</span></span>

![テーブル拡張子の作成](media/ModifyPropertiesOnTable.jpg) 

<span data-ttu-id="2ca3a-108">プロパティ シートで、次のプロパティを変更することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="2ca3a-108">You can now modify the following properties through the property sheet:</span></span>

+ <span data-ttu-id="2ca3a-109">作成者</span><span class="sxs-lookup"><span data-stu-id="2ca3a-109">Created By</span></span>
+ <span data-ttu-id="2ca3a-110">作成日時</span><span class="sxs-lookup"><span data-stu-id="2ca3a-110">Created Date Time</span></span>
+ <span data-ttu-id="2ca3a-111">修正者</span><span class="sxs-lookup"><span data-stu-id="2ca3a-111">Modified By</span></span>
+ <span data-ttu-id="2ca3a-112">変更日時</span><span class="sxs-lookup"><span data-stu-id="2ca3a-112">Modified Date Time</span></span>
+ <span data-ttu-id="2ca3a-113">国地域コード</span><span class="sxs-lookup"><span data-stu-id="2ca3a-113">Country Region Codes</span></span>

<span data-ttu-id="2ca3a-114">**作成者**、**作成日時**、**更新者**、または**変更日時**プロパティを**はい**に設定することにより、対応するフィールドがテーブルに追加されることを保証します。</span><span class="sxs-lookup"><span data-stu-id="2ca3a-114">By setting the **Created By**, **Created Date Time**, **Modified By**, or **Modified Date Time** property to **Yes**, you help guarantee that a corresponding field is added to the table.</span></span> <span data-ttu-id="2ca3a-115">レコードが作成または更新されると、ユーザーに関する、対応する追跡情報がテーブルに格納されます。</span><span class="sxs-lookup"><span data-stu-id="2ca3a-115">Corresponding tracking information about the user is then stored in the table when records are created or updated.</span></span> <span data-ttu-id="2ca3a-116">ベース テーブルで **はい** に設定されている場合、これらのプロパティを **いいえ** に設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="2ca3a-116">You can't set these properties to **No** if they are set to **Yes** on the base table.</span></span>

<span data-ttu-id="2ca3a-117">国または地域コードを一覧に追加することにより、システムが指定された国または地域のコンテキストで実行されているときに、対応するテーブルが適用されることを保証できます。</span><span class="sxs-lookup"><span data-stu-id="2ca3a-117">By adding country or region codes to the list, you help guarantee that the corresponding table is also applicable when the system runs in the context of the specified country or region.</span></span>