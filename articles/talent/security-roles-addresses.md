---
title: セキュリティ ロールによる個人住所へのアクセス
description: このトピックでは、顧客が個人住所にアクセスできない問題を解決する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f8aaa33e5fda404b48548f9a57977dd0ccd53dc1
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518456"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="6ca75-103">セキュリティ ロールによる個人住所へのアクセス</span><span class="sxs-lookup"><span data-stu-id="6ca75-103">Access to private addresses by security role</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6ca75-104">**払出**</span><span class="sxs-lookup"><span data-stu-id="6ca75-104">**Issue**</span></span>

<span data-ttu-id="6ca75-105">顧客がセキュリティ ロールを複製し、その新しいロールとしてサインインした後は、顧客はプライベートとしてマークされた住所を見ることができません。</span><span class="sxs-lookup"><span data-stu-id="6ca75-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="6ca75-106">**解像度**</span><span class="sxs-lookup"><span data-stu-id="6ca75-106">**Resolution**</span></span>

<span data-ttu-id="6ca75-107">問題を解決するには、顧客は複製したセキュリティ ロールのための以下の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ca75-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="6ca75-108">**組織管理\> グローバル アドレス帳 \> グローバル アドレス帳パラメーター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6ca75-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="6ca75-109">**プライベートな場所のセキュリティ**タブで、新しいセキュリティ ロールを**利用可能なロール**リストから、**選択されたロール**リストへ移動します。</span><span class="sxs-lookup"><span data-stu-id="6ca75-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="6ca75-110">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6ca75-110">Select **Save**.</span></span>

![グローバル アドレス帳パラメーター ページ](media/GAD-parameters.png)
