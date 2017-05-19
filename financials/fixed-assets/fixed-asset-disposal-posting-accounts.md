---
title: "固定資産の処分の転記勘定"
description: "この記事は、資産の処分の総勘定元帳の転記勘定を設定する方法を説明します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 111ff7ec677b699b8455b3a46a2866bd98970527
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="fixed-asset-disposal-posting-accounts"></a>固定資産の処分の転記勘定

[!include[banner](../includes/banner.md)]


この記事は、資産の処分の総勘定元帳の転記勘定を設定する方法を説明します。

[勘定科目] クイック タブの [固定資産の転記プロファイル] のページで、[処分 - 売却] および [処分 - 仕損] を選択して、元帳への転記を設定します。

どちらのトランザクション タイプの場合も、固定資産の処分金額は総勘定元帳の貸方に転記されます。 借方は銀行口座などの相手勘定に転記されます。 固定資産を顧客に売却する場合は、相手勘定ではなく顧客勘定が使用されます。

[処分] をクリックし、次に [売却] または [仕損] をクリックして、固定資産の正味簿価額を元に戻す具体的な勘定を設定します。 また、[処分パラメーター] ページで、[転記金額] フィールドや [売却額のタイプ] フィールドに情報を入力できます。 

低価格プール内の資産に対する処分トランザクションは、低価格プールの正味簿価額を処分金額分だけ減額します。 ただし、資産の売却額が低価格プールの正味簿価額を超えるとき、正味簿価額はゼロに減額されます。






