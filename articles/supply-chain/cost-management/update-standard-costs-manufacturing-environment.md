---
title: "製造環境での標準原価を更新"
description: "この記事は、製造環境での標準原価の更新方法についてのガイダンスを提供します。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7a5340baad38864388abcfab3235cf459887cba9
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="update-standard-costs-in-a-manufacturing-environment"></a>製造環境での標準原価を更新

[!include[banner](../includes/banner.md)]


この記事は、製造環境での標準原価の更新方法についてのガイダンスを提供します。 

更新は、新しい品目、コスト カテゴリ、または間接原価計算式を反映する場合があります。 また、訂正や原価の変化を反映することもできます。 次の例で示すように、更新の種類は、標準原価の更新に必要な手順に影響を与えます。

-   購入品目の予期される標準原価の変更を入力し、適切な日に品目原価レコードのステータスを**有効**に変更します。 ただし、購入品目を使用する製造品目の原価は再計算しないでください。
-   新しい購入品目の標準原価を入力しますが、新しい購入品目をコンポーネントとして含む部品表 (BOM) バージョンを使用する製造品目の原価は再計算しないでください。
-   購入品目の原価を訂正または変更し、または購入品目に割り当てられている原価グループを変更し、購入品目をコンポーネントとして含む BOM バージョンを使用するすべての製造品目の原価を計算します。
-   原価カテゴリの原価を変更し、その原価カテゴリを使用する工順操作を含む工順バージョンを使用するすべての製造品目の原価を計算します。
-   工順工程に割り当てられているコスト カテゴリ、またはコスト カテゴリに割り当てられているコスト グループを変更します。 それから、そのコスト カテゴリを使用する工順操作を含む工順バージョンを使用するすべての製造品目のコストを計算します。
-   間接原価計算式を変更し、変更によって影響を受けるすべての製造品目の原価を計算します。
-   製造品目の製造サイトを変更または追加し、そのサイトに対する品目の製造原価を計算します。
-   製造品目の原価を計算または再計算し、その製造品目をコンポーネントとして含む BOM バージョンを使用するすべての製造品目の原価を再計算します。
-   定義済み、承認済みで有効な BOM および工順情報を基にして、新しい製造品目の原価を計算します。

いずれの場合も、標準原価の更新方法を慎重に検討する必要があります。




