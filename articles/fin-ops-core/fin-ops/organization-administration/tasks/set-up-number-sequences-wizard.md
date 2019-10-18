---
title: ウィザードを使用した番号順序の設定
description: このトピックでは、ウィザードを使用して必要なすべての番号順序を同時に設定する方法を説明します。
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f97c4cd6cdb117ebdd67a155478bb6f8d1703541
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178740"
---
# <a name="set-up-number-sequences-using-a-wizard"></a><span data-ttu-id="684cd-103">ウィザードを使用した番号順序の設定</span><span class="sxs-lookup"><span data-stu-id="684cd-103">Set up number sequences using a wizard</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="684cd-104">番号順序は、マスタ データ レコードおよびトランザクション レコードに必要な読みやすい固有 ID の生成に使用されます。</span><span class="sxs-lookup"><span data-stu-id="684cd-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="684cd-105">ID が必要なマスタ データまたはトランザクション レコードは、参照先と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="684cd-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="684cd-106">参照先に新しいレコードを作成するには、事前に番号順序を設定して参照先に関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="684cd-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="684cd-107">このトピックでは、ウィザードを使用して必要なすべての番号順序を同時に設定する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="684cd-107">This topic explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="684cd-108">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="684cd-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="684cd-109">**ナビゲーション > モジュール > 組織管理 > 番号順序 > 番号順序**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="684cd-109">Go to **Navigation > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="684cd-110">**生成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="684cd-110">Select **Generate**.</span></span>
3. <span data-ttu-id="684cd-111">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="684cd-111">Select **Next**.</span></span>

   - <span data-ttu-id="684cd-112">このページでは、ID コード、最小値、および最大値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="684cd-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="684cd-113">また、番号順序を連続させるかどうかも指定できます。</span><span class="sxs-lookup"><span data-stu-id="684cd-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
   - <span data-ttu-id="684cd-114">番号順序に対して番号を事前に割り当てる必要がある場合は、**連続**オプションは選択しないでください。</span><span class="sxs-lookup"><span data-stu-id="684cd-114">Do not select the **Continuous** option if you must preallocate numbers for the number sequence.</span></span> <span data-ttu-id="684cd-115">番号順序の形式にスコープ区分を追加するには、リストから形式を選択し、**スコープを書式に含める**を選択します。</span><span class="sxs-lookup"><span data-stu-id="684cd-115">To add a scope segment to the format of a number sequence, select the format in the list, and then select **Include scope in format**.</span></span> <span data-ttu-id="684cd-116">番号順序の形式からスコープ区分を削除するには、リストから形式を選択し、**書式からスコープを削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="684cd-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then select **Remove scope from format**.</span></span> <span data-ttu-id="684cd-117">自動生成から番号順序を除外するには、リストから番号順序を選択し、**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="684cd-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then select **Delete**.</span></span>  

4. <span data-ttu-id="684cd-118">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="684cd-118">Select **Next**.</span></span>
5. <span data-ttu-id="684cd-119">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="684cd-119">Select **Finish**.</span></span>

