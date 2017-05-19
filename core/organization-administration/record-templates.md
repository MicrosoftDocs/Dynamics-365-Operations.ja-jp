---
title: "レコード テンプレートを作成する"
description: "この記事は、レコード テンプレートの概念を紹介し、情報を共有するレコードを作成して使用する方法を説明します。"
author: pvillads
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 7efa0858de75d23f35eb71a3dd4f1d18ed9240e6
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="create-record-templates"></a>レコード テンプレートを作成する

[!include[banner](../includes/banner.md)]


この記事は、レコード テンプレートの概念を紹介し、情報を共有するレコードを作成して使用する方法を説明します。

レコード テンプレートを使用すると、Microsoft Dynamics 365 for Operations でレコードをもっと迅速に作成することができます。 Microsoft Dynamics 365 for Operations のレコード タイプの一部のみを対象としたレコード テンプレートを作成できます。 たとえば、サンフランシスコにあるレンタカー事業のレンタル情報を入力するとします。 顧客のほとんどは、サンフランシスコ周辺から来ますから、レンタル フォームの [**州**]、[**国**]、[**市町村**] フィールドに値を自動的に記入できれば、良いでしょう。 [**注記:**] テンプレートを適用できるのは、アクセス権のある Dynamics 365 for Operations の領域だけです。 ただし、すべてのユーザーが使用できるテンプレートを作成している場合、新しいレコードを作成すると、すべてのテンプレートのタイトルが、本人と他のユーザーに表示されます。 テンプレートを命名する場合には、これを考慮してください。 たとえば、法人の一部の従業員に歩合給が支払われていることが機密事項の場合、「コミッション」などの、用語が含まれる名前の使用を避けてください。 アクセス許可がある 1 つ以上のテンプレートが特定のフォームに存在し、そのフォームで新しいレコードを作成するときには、[**目的のテンプレートの選択**] ページが表示されます。 一覧からテンプレートを選択すると、新しいレコードが作成されて、選択したテンプレートに基づく既定の情報が設定されます。 新しいレコードを作成するときにテンプレートを使用しない場合は、[**テンプレートの選択**] ページの [**今後このメッセージを表示しない**] チェック ボックスをオンにします。 テンプレート選択ダイアログ ボックスを再び表示するには、レコードを右クリックし、[**レコード情報**] をクリックして、[**テンプレート選択の表示**] をクリックします。




