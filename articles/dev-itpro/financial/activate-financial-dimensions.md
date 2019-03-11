---
title: 財務分析コードの有効化
description: このトピックには、財務分析コード プロセスの有効化に関する情報が含まれています。
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 191363
ms.assetid: dd1dd40e-6bff-47b5-bf2e-55b9a4dcde1d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44499cad4a9acd0f6f87b0fa0865d9e09ca3c0e4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368915"
---
# <a name="financial-dimension-activation"></a><span data-ttu-id="c3fe1-103">財務分析コードの有効化</span><span class="sxs-lookup"><span data-stu-id="c3fe1-103">Financial dimension activation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3fe1-104">このトピックには、財務分析コード プロセスの有効化に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c3fe1-104">This topic contains information about the activating financial dimension process.</span></span>

<span data-ttu-id="c3fe1-105">新しい財務分析コードがシステムに追加されると、分析コードの有効化が実行されるまで財務分析コードを使用できないことを示すメッセージがユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c3fe1-105">When a new financial dimension is added to the system, users are prompted with a message stating that the financial dimension is not consumable until Dimension activation is run.</span></span> <span data-ttu-id="c3fe1-106">分析コードの有効化を実行すると、**DimensionAttributeValueCombination** および **DimensionAttributeValueSet** テーブルで、データベースのスキーマの変更が実行されます。</span><span class="sxs-lookup"><span data-stu-id="c3fe1-106">When Dimension activation is run, a database schema change occurs in the **DimensionAttributeValueCombination** and **DimensionAttributeValueSet** tables.</span></span> <span data-ttu-id="c3fe1-107">スキーマの変更により、各財務分析コードのテーブルに新しい列が追加されます。</span><span class="sxs-lookup"><span data-stu-id="c3fe1-107">The schema change adds a new column to the table for each financial dimension.</span></span> <span data-ttu-id="c3fe1-108">プロセス中に、スキーマロックは Microsoft SQL Server によって 2 つのテーブルに配置され、テーブルを更新することができます。</span><span class="sxs-lookup"><span data-stu-id="c3fe1-108">During this process, a schema lock is placed on the two tables by Microsoft SQL Server so that the table can be updated.</span></span> <span data-ttu-id="c3fe1-109">このプロセスが完了すると、テーブルはもはやロックされていません。</span><span class="sxs-lookup"><span data-stu-id="c3fe1-109">When the process is complete, the tables are no longer locked.</span></span> <span data-ttu-id="c3fe1-110">仕訳帳が開いたときにこのプロセスが実行されると、デッドロックが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c3fe1-110">If this process is attempted when a journal is open, then a deadlock may occur.</span></span> <span data-ttu-id="c3fe1-111">これが発生した場合、ユーザーはサーバーからメタデータ エラーを受け取る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c3fe1-111">If this happens, the user could potentially receive a metadata error from the server.</span></span> <span data-ttu-id="c3fe1-112">セッションを最新の情報に更新して、更新されたメタデータを取得できます。</span><span class="sxs-lookup"><span data-stu-id="c3fe1-112">Users can refresh the session to get the updated metadata.</span></span> <span data-ttu-id="c3fe1-113">ユーザーが受け取るメッセージ。</span><span class="sxs-lookup"><span data-stu-id="c3fe1-113">The message the user receives states:</span></span>

-   <span data-ttu-id="c3fe1-114">プロセスが実行されるまで、どの場所でも、財務分析コードを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="c3fe1-114">You will not be able to consume the financial dimension anywhere until the process is run.</span></span> <span data-ttu-id="c3fe1-115">これには、勘定構造に追加することが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c3fe1-115">This includes adding it to account structures.</span></span>
-   <span data-ttu-id="c3fe1-116">スキーマの変更が発生するため、有効化を実行するには、特別な権限である分析コードの有効化権限が必要です。</span><span class="sxs-lookup"><span data-stu-id="c3fe1-116">A schema change occurs, therefore a special privilege, the Dimension activation privilege is required to run activation.</span></span>
-   <span data-ttu-id="c3fe1-117">予定されたメンテナンスまたはダウンタイムの際に、これを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3fe1-117">You should perform this during scheduled maintenance or downtime.</span></span>

<span data-ttu-id="c3fe1-118">財務分析コードを追加することは、通常、非常に意図的な業務プロセスです。</span><span class="sxs-lookup"><span data-stu-id="c3fe1-118">Adding a financial dimension is typically a very deliberate business process.</span></span> <span data-ttu-id="c3fe1-119">ユーザー受け入れテストなどのマルチ ユーザー環境またはトレーニング環境がある場合、1 人だけがこのプロセスを試行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3fe1-119">If there is a multi-user environment, such as a user acceptance testing or training environment, only one person should attempt this process.</span></span> <span data-ttu-id="c3fe1-120">2 番目のオプションは、有効化オプション、**財務分析コードの再構築**を選択したときに使用できます。</span><span class="sxs-lookup"><span data-stu-id="c3fe1-120">A second option is available when you choose the Activate option, **Rebuild financial dimensions**.</span></span> 

<span data-ttu-id="c3fe1-121">[![ActWiki2](./media/actwiki2.png)](./media/actwiki2.png)</span><span class="sxs-lookup"><span data-stu-id="c3fe1-121">[![ActWiki2](./media/actwiki2.png)](./media/actwiki2.png)</span></span> 

<span data-ttu-id="c3fe1-122">**財務分析コードを再構築** オプションは、初期有効化プロセス中予期しない結果が発生した場合にのみ実行されるプロセスであるため、既定で **いいえ** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="c3fe1-122">The **Rebuild financial dimensions** option is set to **No** by default, as it is a process that should only be run if unexpected results occur during the initial activation process.</span></span> <span data-ttu-id="c3fe1-123">これにより、すべての財務分析コードと値がドロップされ、テーブルに再追加されます。</span><span class="sxs-lookup"><span data-stu-id="c3fe1-123">This will drop and re-add all financial dimensions and values to the tables.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3fe1-124">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="c3fe1-124">Additional resources</span></span>

[<span data-ttu-id="c3fe1-125">財務分析コード を設定する (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="c3fe1-125">Set up financial dimensions (Task guide)</span></span>](../../financials/general-ledger/tasks/define-financial-dimensions.md)

[<span data-ttu-id="c3fe1-126">メンテナンス モード</span><span class="sxs-lookup"><span data-stu-id="c3fe1-126">Maintenance mode</span></span>](../sysadmin/maintenance-mode.md)



