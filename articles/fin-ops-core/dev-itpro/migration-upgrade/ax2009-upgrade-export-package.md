---
title: AX 2009 の移行 － パッケージのエクスポート
description: このトピックは、Microsoft Dynamics AX 2009 から Finance and Operations に移行するためにデータ パッケージをエクスポートする方法について説明します。
author: kfend
manager: AnnBe
ms.date: 06/26/2018
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
ms.openlocfilehash: 947f2e91b719e785e515d558289de88caf96ad15
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183171"
---
# <a name="ax-2009-migration--export-packages"></a><span data-ttu-id="0c931-103">AX 2009 の移行 - パッケージのエクスポート</span><span class="sxs-lookup"><span data-stu-id="0c931-103">AX 2009 migration – Export packages</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c931-104">Microsoft Dynamics AX 2009 のデータのインポート/エクスポート フレームワーク (DIXF) サービスを使用して、Finance and Operations に移行する必要があるデータを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="0c931-104">You can use the Data Import/Export Framework (DIXF) service in Microsoft Dynamics AX 2009 to retrieve data that must be migrated to  Finance and Operations.</span></span> <span data-ttu-id="0c931-105">エクスポート プロセスは、ジョブ ID を使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="0c931-105">The export process is completed through a job ID.</span></span> <span data-ttu-id="0c931-106">エクスポートする場合は、エクスポート ジョブを定義する方法を指定できます。</span><span class="sxs-lookup"><span data-stu-id="0c931-106">When you export, you can specify how the export job is defined.</span></span> <span data-ttu-id="0c931-107">エクスポートするソース データ、変換値、およびフィールド マップを選択できます。</span><span class="sxs-lookup"><span data-stu-id="0c931-107">You can select the source data to export, the conversion value, and the field mapping.</span></span> <span data-ttu-id="0c931-108">各ソースにクエリを適用して、エクスポートされる内容を制限することもできます。</span><span class="sxs-lookup"><span data-stu-id="0c931-108">You can also apply a query to each source to limit what is exported.</span></span>

<span data-ttu-id="0c931-109">データ移行ツール (DMT) が生成するエクスポート パッケージは、1 つまたは複数のデータ エンティティで構成できます。</span><span class="sxs-lookup"><span data-stu-id="0c931-109">The export package that the Data migration tool (DMT) generates can consist of one or many data entities.</span></span> <span data-ttu-id="0c931-110">標準的なデータ パッケージは、インポートなどの特定のタスクのエンティティ グループで構成されています。</span><span class="sxs-lookup"><span data-stu-id="0c931-110">A typical data package consists of a group of entities for a specific task, such as import.</span></span> <span data-ttu-id="0c931-111">たとえば、システムの設定に必要なデータ エンティティは、1 つのデータ パッケージの一部である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0c931-111">For example, the data entities that are required for system setup might be part of one data package.</span></span> <span data-ttu-id="0c931-112">データ パッケージの形式は、パッケージ マニフェスト、パッケージ ヘッダー、および含まれているデータ エンティティの追加ファイルを含む圧縮ファイルです。</span><span class="sxs-lookup"><span data-stu-id="0c931-112">The format of a data package is a compressed file that contains a package manifest, a package header, and any additional files for the data entities that are included.</span></span>

<span data-ttu-id="0c931-113">データ パッケージを作成する前に、何を含める必要があるかを計画します。</span><span class="sxs-lookup"><span data-stu-id="0c931-113">Before you create a data package, plan out what should be included.</span></span> <span data-ttu-id="0c931-114">この方法で、正しいエンティティ、エンティティの順序、およびフィールドが含まれていることを保証します。</span><span class="sxs-lookup"><span data-stu-id="0c931-114">In this way, you help guarantee that the correct entities, entity sequence, and fields are included.</span></span>

<span data-ttu-id="0c931-115">データ パッケージをエクスポートするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0c931-115">Follow these steps to export the data package.</span></span>

1. <span data-ttu-id="0c931-116">AX 2009 の、ナビゲーション ウィンドウで、**データ移行** \> **共通** \> **移行グループの作成** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c931-116">In AX 2009, in the navigation pane, click **Data migration** \> **Common** \> **Create migration group**.</span></span>
2. <span data-ttu-id="0c931-117">**移行グループ** フォームで、エクスポートする移行グループを選択し、**今すぐエクスポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c931-117">In the **Migration group** form, select the migration group to export, and then click **Export now**.</span></span>
3. <span data-ttu-id="0c931-118">**データのエクスポート** フォームで、必要に応じてエクスポート ファイル パスを更新し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c931-118">In the **Export data** form, update the export file path as required, and then click **OK**.</span></span>