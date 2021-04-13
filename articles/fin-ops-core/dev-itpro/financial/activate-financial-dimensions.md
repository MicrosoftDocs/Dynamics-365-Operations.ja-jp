---
title: 財務分析コードの有効化
description: このトピックには、財務分析コード プロセスの有効化に関する情報が含まれています。
author: aprilolson
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 191363
ms.assetid: dd1dd40e-6bff-47b5-bf2e-55b9a4dcde1d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76cf27af69cf0028981b5d0e34f7d1381cc038c1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748151"
---
# <a name="financial-dimension-activation"></a><span data-ttu-id="7d048-103">財務分析コードの有効化</span><span class="sxs-lookup"><span data-stu-id="7d048-103">Financial dimension activation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d048-104">このトピックには、財務分析コード プロセスの有効化に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7d048-104">This topic contains information about the activating financial dimension process.</span></span>

<span data-ttu-id="7d048-105">新しい財務分析コードがシステムに追加されると、分析コードの有効化が実行されるまで財務分析コードを使用できないことを示すメッセージがユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="7d048-105">When a new financial dimension is added to the system, users are prompted with a message stating that the financial dimension is not consumable until Dimension activation is run.</span></span> <span data-ttu-id="7d048-106">分析コードの有効化を実行すると、**DimensionAttributeValueCombination** および **DimensionAttributeValueSet** テーブルで、データベースのスキーマの変更が実行されます。</span><span class="sxs-lookup"><span data-stu-id="7d048-106">When Dimension activation is run, a database schema change occurs in the **DimensionAttributeValueCombination** and **DimensionAttributeValueSet** tables.</span></span> <span data-ttu-id="7d048-107">スキーマの変更により、各財務分析コードのテーブルに新しい列が追加されます。</span><span class="sxs-lookup"><span data-stu-id="7d048-107">The schema change adds a new column to the table for each financial dimension.</span></span> <span data-ttu-id="7d048-108">プロセス中に、スキーマロックは Microsoft SQL Server によって 2 つのテーブルに配置され、テーブルを更新することができます。</span><span class="sxs-lookup"><span data-stu-id="7d048-108">During this process, a schema lock is placed on the two tables by Microsoft SQL Server so that the table can be updated.</span></span> <span data-ttu-id="7d048-109">このプロセスが完了すると、テーブルはもはやロックされていません。</span><span class="sxs-lookup"><span data-stu-id="7d048-109">When the process is complete, the tables are no longer locked.</span></span> <span data-ttu-id="7d048-110">仕訳帳が開いたときにこのプロセスが実行されると、デッドロックが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7d048-110">If this process is attempted when a journal is open, then a deadlock may occur.</span></span> <span data-ttu-id="7d048-111">デッドロックが発生した場合、ユーザーはサーバーからメタデータ エラーを受け取る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7d048-111">If a deadlock occurs, the user could potentially receive a metadata error from the server.</span></span> <span data-ttu-id="7d048-112">セッションを最新の情報に更新して、更新されたメタデータを取得できます。</span><span class="sxs-lookup"><span data-stu-id="7d048-112">Users can refresh the session to get the updated metadata.</span></span> <span data-ttu-id="7d048-113">ユーザーが受け取るメッセージ。</span><span class="sxs-lookup"><span data-stu-id="7d048-113">The message the user receives states:</span></span>

- <span data-ttu-id="7d048-114">プロセスが実行されるまで、どの場所でも、財務分析コードを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="7d048-114">You will not be able to consume the financial dimension anywhere until the process is run.</span></span> <span data-ttu-id="7d048-115">これには、勘定構造に追加することが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7d048-115">This includes adding it to account structures.</span></span>
- <span data-ttu-id="7d048-116">スキーマの変更が発生するため、有効化を実行するには、特別な権限である分析コードの有効化権限が必要です。</span><span class="sxs-lookup"><span data-stu-id="7d048-116">A schema change occurs, therefore a special privilege, the Dimension activation privilege is required to run activation.</span></span>
- <span data-ttu-id="7d048-117">予定されたメンテナンスまたはダウンタイムの際に、これを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d048-117">You should perform this during scheduled maintenance or downtime.</span></span>

<span data-ttu-id="7d048-118">財務分析コードを追加することは、通常、意図的なビジネス プロセスです。</span><span class="sxs-lookup"><span data-stu-id="7d048-118">Adding a financial dimension is typically a deliberate business process.</span></span> <span data-ttu-id="7d048-119">ユーザー受け入れテストなどのマルチ ユーザー環境またはトレーニング環境がある場合、1 人だけがこのプロセスを試行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d048-119">If there is a multi-user environment, such as a user acceptance testing or training environment, only one person should attempt this process.</span></span> <span data-ttu-id="7d048-120">2 番目のオプションは、有効化オプション、**財務分析コードの再構築** を選択したときに使用できます。</span><span class="sxs-lookup"><span data-stu-id="7d048-120">A second option is available when you choose the Activate option, **Rebuild financial dimensions**.</span></span> 

<span data-ttu-id="7d048-121">[![ActWiki2](./media/actwiki2.png)](./media/actwiki2.png)</span><span class="sxs-lookup"><span data-stu-id="7d048-121">[![ActWiki2](./media/actwiki2.png)](./media/actwiki2.png)</span></span> 

<span data-ttu-id="7d048-122">**財務分析コードを再構築** オプションは、初期有効化プロセス中予期しない結果が発生した場合にのみ実行されるプロセスであるため、既定で **いいえ** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="7d048-122">The **Rebuild financial dimensions** option is set to **No** by default, as it is a process that should only be run if unexpected results occur during the initial activation process.</span></span> <span data-ttu-id="7d048-123">再構成することにより、テーブルにすべての財務分析コードと値がドロップされ、再追加されます。</span><span class="sxs-lookup"><span data-stu-id="7d048-123">Rebuilding will drop and readd all financial dimensions and values to the tables.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d048-124">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7d048-124">Additional resources</span></span>

[<span data-ttu-id="7d048-125">財務分析コードの定義</span><span class="sxs-lookup"><span data-stu-id="7d048-125">Define financial dimensions</span></span>](../../../finance/general-ledger/tasks/define-financial-dimensions.md)

[<span data-ttu-id="7d048-126">メンテナンス モード</span><span class="sxs-lookup"><span data-stu-id="7d048-126">Maintenance mode</span></span>](../sysadmin/maintenance-mode.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]