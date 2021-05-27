---
title: 陸揚原価の調達パラメーター
description: このトピックでは、陸揚原価モジュールを使用する場合に、関連する調達パラメーターを設定する方法について説明します。
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ccda3bd769a646e2390711883b8e40bec50e4d6a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020986"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="e842d-103">陸揚原価の調達パラメーター</span><span class="sxs-lookup"><span data-stu-id="e842d-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e842d-104">**調達パラメーター** ページには、**陸揚原価** モジュールを使用する場合に特に関連するいくつかの設定があります。</span><span class="sxs-lookup"><span data-stu-id="e842d-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="e842d-105">**調達パラメーター** ページから開く **注文明細行の更新** ダイアログ ボックスを使用して、発注書ヘッダーで変更が加えられたときに発注書明細行を自動的に更新するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e842d-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="e842d-106">この設定を完了するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e842d-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="e842d-107">**調達 \> セットアップ \> 調達パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e842d-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="e842d-108">**全般** タブで 、 **注文明細行の更新** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="e842d-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="e842d-109">**注文明細行の更新** ダイアログ ボックスには、注文ヘッダーのフィールドが一覧表示され、注文明細行の関連フィールドに自動更新を適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="e842d-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="e842d-110">一覧の各フィールドを次のいずれかの値に設定します。</span><span class="sxs-lookup"><span data-stu-id="e842d-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="e842d-111">**常時** – 注文ヘッダーの更新時に注文明細行が自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="e842d-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="e842d-112">**なし** – 注文ヘッダーの更新時に注文明細行を決して更新しません。</span><span class="sxs-lookup"><span data-stu-id="e842d-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="e842d-113">**プロンプト** – 注文明細行を更新するかどうかを選択するように求められます。</span><span class="sxs-lookup"><span data-stu-id="e842d-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
