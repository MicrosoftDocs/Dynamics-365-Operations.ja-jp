---
title: 法人の TDS 登録番号の設定
description: このトピックでは、法人の源泉徴収税 (TDS) 登録番号を設定する方法について説明します。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 3550b2b7b305702ffc337ba0a9bb79f60a9de120
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023385"
---
# <a name="set-up-tds-registration-numbers-for-legal-entities"></a><span data-ttu-id="e956b-103">法人の TDS 登録番号の設定</span><span class="sxs-lookup"><span data-stu-id="e956b-103">Set up TDS registration numbers for legal entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e956b-104">このトピックでは、法人の源泉徴収税 (TDS) 登録番号を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e956b-104">This topic explains how to set up Tax Deducted at Source (TDS) registration numbers for legal entities.</span></span>

1. <span data-ttu-id="e956b-105">**組織管理 \> 組織 \> 法人** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e956b-105">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>

    <span data-ttu-id="e956b-106">[![法人ページ](./media/apac-ind-TDS-4.png)](./media/apac-ind-TDS-4.png)</span><span class="sxs-lookup"><span data-stu-id="e956b-106">[![Legal entities page](./media/apac-ind-TDS-4.png)](./media/apac-ind-TDS-4.png)</span></span>

2. <span data-ttu-id="e956b-107">**税金情報** クイック タブの **納税者番号** フィールドに、法人の納税者番号 (PAN) を入力します。</span><span class="sxs-lookup"><span data-stu-id="e956b-107">On the **Tax information** FastTab, in the **Permanent account number** field, enter the permanent account number (PAN) of the legal entity.</span></span>
3. <span data-ttu-id="e956b-108">**Circle 番号** フィールドに、TDS 当局の Circle 番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="e956b-108">In the **Circle number** field, enter the circle number of the TDS authority.</span></span>
4. <span data-ttu-id="e956b-109">**Ward 番号** フィールドに、TDS 当局の Ward 番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="e956b-109">In the **Ward number** field, enter the ward number of the TDS authority.</span></span>
5. <span data-ttu-id="e956b-110">**課税担当者** フィールドに、TDS 当局の課税担当者の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="e956b-110">In the **Assessing officer** field, enter the details of the assessing officer for the TDS authority.</span></span>
6. <span data-ttu-id="e956b-111">**控除担当者のタイプ** フィールドで、法人の控除担当者タイプ カテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="e956b-111">In the **Type of deductor** field, select the deductor type category for the legal entity.</span></span>
7. <span data-ttu-id="e956b-112">アクション ペインで **登録 ID** を選択して、**住所の管理** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="e956b-112">On the Action Pane, select **Registration IDs** to open the **Manage addresses** page.</span></span>
8. <span data-ttu-id="e956b-113">**税金情報** クイック タブで、**追加** または **編集** を選択して **税金情報の管理** ページを開き、税金登録エントリを管理できます。</span><span class="sxs-lookup"><span data-stu-id="e956b-113">On the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>

    <span data-ttu-id="e956b-114">[![住所の管理ページ](./media/apac-ind-TDS-5.png)](./media/apac-ind-TDS-5.png)</span><span class="sxs-lookup"><span data-stu-id="e956b-114">[![Manage addresses page](./media/apac-ind-TDS-5.png)](./media/apac-ind-TDS-5.png)</span></span>

9. <span data-ttu-id="e956b-115">**源泉徴収税** クイック タブの **税勘定番号 (TAN)** フィールドに、登録番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="e956b-115">On the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the registration number.</span></span> <span data-ttu-id="e956b-116">この番号は、4 文字のアルファベット、5 文字の数字、1 文字のアルファベットの順で構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e956b-116">This number must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="e956b-117">次に例を示します: **AXDF87645F**。</span><span class="sxs-lookup"><span data-stu-id="e956b-117">Here is an example: **AXDF87645F**.</span></span>
10. <span data-ttu-id="e956b-118">**名前または説明** フィールドに、源泉徴収税登録番号の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="e956b-118">In the **Name or description** field, enter a description of the withholding tax registration number.</span></span>

    <span data-ttu-id="e956b-119">[![税金情報の管理ページ](./media/apac-ind-TDS-5-1.png)](./media/apac-ind-TDS-5-1.png)</span><span class="sxs-lookup"><span data-stu-id="e956b-119">[![Manage tax information page](./media/apac-ind-TDS-5-1.png)](./media/apac-ind-TDS-5-1.png)</span></span>

11. <span data-ttu-id="e956b-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e956b-120">Close the page.</span></span>
