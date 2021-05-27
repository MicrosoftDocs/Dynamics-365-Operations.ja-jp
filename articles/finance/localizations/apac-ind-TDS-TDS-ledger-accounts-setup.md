---
title: TDS 勘定科目の設定
description: このトピックでは、源泉徴収税 (TDS) 機能の勘定科目を設定する方法について説明します。
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
ms.openlocfilehash: 93d4cb54488ec0eeee40ca56f3e46f30012f54f5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023387"
---
# <a name="set-up-tds-ledger-accounts"></a><span data-ttu-id="371f0-103">TDS 勘定科目の設定</span><span class="sxs-lookup"><span data-stu-id="371f0-103">Set up TDS ledger accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="371f0-104">このトピックでは、源泉徴収税 (TDS) 機能の勘定科目を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="371f0-104">This topic explains how to set up ledger accounts for the Tax Deducted at Source (TDS) feature.</span></span> <span data-ttu-id="371f0-105">**勘定科目表** ページを使用して、TDS の勘定科目を設定します。</span><span class="sxs-lookup"><span data-stu-id="371f0-105">You use the **Chart of accounts** page to set up ledger accounts for TDS.</span></span>

1. <span data-ttu-id="371f0-106">**一般会計 \> 勘定科目表 \> 勘定 \> 主勘定** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="371f0-106">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**.</span></span>
2. <span data-ttu-id="371f0-107">**概要** タブで **Alt + N** を選択して、TDS 勘定科目を作成し、必要な詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="371f0-107">On the **Overview** tab, select **Alt+N** to create a TDS ledger account, and enter the required details.</span></span>
3. <span data-ttu-id="371f0-108">**設定** タブの **転記タイプ** フィールドで **源泉徴収税** を選択します。</span><span class="sxs-lookup"><span data-stu-id="371f0-108">On the **Setup** tab, in the **Posting type** field, select **Withholding tax**.</span></span>     

    > [!NOTE]
    > <span data-ttu-id="371f0-109">**源泉徴収税** の転記タイプを持つ勘定科目は、TDS 税コードの TDS 売掛金金額を転記するために使用される売掛金勘定としてのみ定義できます。</span><span class="sxs-lookup"><span data-stu-id="371f0-109">Ledger accounts that have a posting type of **Withholding tax** can be defined only as receivable accounts that are used to post the TDS receivable amount for a TDS tax code.</span></span>

4. <span data-ttu-id="371f0-110">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="371f0-110">Close the page.</span></span>
