---
title: ユーザー指定のチームの所有者
description: このトピックでは、既定のチーム所有者を使用する代わりに、ユーザー指定のチーム所有者を設定する方法について説明します。
author: sabinn-msft
ms.date: 04/26/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2021-04-26
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3219b02e79861a72d3ab2fdb986cec54474f05be
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097222"
---
# <a name="user-specified-team-owner"></a><span data-ttu-id="8a934-103">ユーザー指定のチームの所有者</span><span class="sxs-lookup"><span data-stu-id="8a934-103">User-specified team owner</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8a934-104">Finance and Operations アプリでは、グローバル テーブルは会社または法人に関連付けられません。</span><span class="sxs-lookup"><span data-stu-id="8a934-104">In Finance and Operations apps, global tables are not associated with a company or legal entity.</span></span> <span data-ttu-id="8a934-105">これらのテーブルでは、二重書き込みを使用して Microsoft Dataverse に書き込む場合、チームを指定することができますが、所有者として既定のチームを使用できません。</span><span class="sxs-lookup"><span data-stu-id="8a934-105">For these tables, you can specify a team and not use a default team as owner when writing to Microsoft Dataverse using dual-write.</span></span> 

<span data-ttu-id="8a934-106">既定では、二重書き込みを有効にする場合、ルートの事業単位の既定チームは二重書き込みを通して統合されたすべての行の既定の所有者になります。</span><span class="sxs-lookup"><span data-stu-id="8a934-106">By default, when you enable dual-write, the root business unit’s default team will become the default owner for all rows integrated through dual-write.</span></span> <span data-ttu-id="8a934-107">これらのレコードへのアクセスをユーザーのサブセットに限定する場合は、これは必要ではないかもしれません。</span><span class="sxs-lookup"><span data-stu-id="8a934-107">This may not be what you want when you want to limit access to these records to just a subset of users.</span></span> <span data-ttu-id="8a934-108">組織が対応するチームを持つ事業単位で複数の部門を定義し、その下に対応するチームを持つのは珍しいことではありません。</span><span class="sxs-lookup"><span data-stu-id="8a934-108">It’s not uncommon for an organization to have multiple departments defined by business units with corresponding teams under them.</span></span> <span data-ttu-id="8a934-109">既定のチームのすべてのユーザーによって、二重書き込みを介して統合されたすべてのレコードにアクセスされることを望まないとします。</span><span class="sxs-lookup"><span data-stu-id="8a934-109">You don’t want all users of the default team to have access to all the records integrated via dual-write.</span></span> <span data-ttu-id="8a934-110">このような場合は、それらのレコードの所有者として、グローバル テーブルごとに異なるチームを指定できます。</span><span class="sxs-lookup"><span data-stu-id="8a934-110">In these situations, you can specify a different team for each global table as an owner for these records.</span></span> 

## <a name="change-the-owning-team"></a><span data-ttu-id="8a934-111">所有チームの変更</span><span class="sxs-lookup"><span data-stu-id="8a934-111">Change the owning team</span></span>

<span data-ttu-id="8a934-112">**テーブル マッピング** で、**グローバル製品** のようなグローバル テーブル マップを選択する場合、**所有チームの更新** セクションでチームのリストを表示できます。</span><span class="sxs-lookup"><span data-stu-id="8a934-112">When you select a global table map such as **Global Products**, under **Table mappings**, you can view the list of teams in the **Update owning team** section.</span></span> <span data-ttu-id="8a934-113">既定では、二重書き込みでは既定のチームが使用され、これは空白の値で示されます。</span><span class="sxs-lookup"><span data-stu-id="8a934-113">By default, dual-write uses the default team, which is indicated by a blank value.</span></span> <span data-ttu-id="8a934-114">新しいバージョンで新しいマップを作成した後に、所有チームの一覧から新しいチームをピッキングして新しい値を保存することで、既定の動作を変更します。</span><span class="sxs-lookup"><span data-stu-id="8a934-114">After you create a new map with a new version, you change the default behavior by picking a new team from the owning team list and then save the new value.</span></span> <span data-ttu-id="8a934-115">**所有チーム** フィールドには次のスクリーンショットが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8a934-115">The **Owning team** field is shown in the following screenshot.</span></span>

:::image type="content" source="media/owning-team-1.png" alt-text="所有チームの更新":::
  
>[!NOTE]
> <span data-ttu-id="8a934-117">所有チームを設定した後は、初期同期とライブ同期の両方を実行できます。所有チームの設定は、環境をまたがって転送されません。</span><span class="sxs-lookup"><span data-stu-id="8a934-117">After you set the owning team, it works across both initial and live sync. The owning team setting does not transfer across environments.</span></span> 

## <a name="view-the-owning-team-after-initial-sync"></a><span data-ttu-id="8a934-118">初期同期後の所有チームの表示</span><span class="sxs-lookup"><span data-stu-id="8a934-118">View the owning team after initial sync</span></span>

<span data-ttu-id="8a934-119">初期同期を実行した後、統合されたレコードに所有者が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8a934-119">After you run the initial sync, the owner is shown in the integrated records.</span></span> <span data-ttu-id="8a934-120">次のスクリーンショットでは、所有者は **グローバル製品** テーブル マップで、統合されたレコードのために **dwteam** を **売上** に変更しました。　</span><span class="sxs-lookup"><span data-stu-id="8a934-120">In the following screenshot, the owner has changed from **dwteam** to **Sales** for the integrated records in **Global Product** table map.</span></span>
  
:::image type="content" source="media/owning-team-2.png" alt-text="既定およびユーザー指定のチームとの初期同期":::
  
[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
