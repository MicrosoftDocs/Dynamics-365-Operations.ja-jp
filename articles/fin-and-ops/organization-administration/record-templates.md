---
title: レコード テンプレート
description: この記事は、レコード テンプレートの概念を紹介し、情報を共有するレコードを作成して使用する方法を説明します。
author: pvillads
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 426fd8fafec061b649cbb31109ffe8fabc24917d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545676"
---
# <a name="record-templates"></a>レコード テンプレート

[!include [banner](../includes/banner.md)]

この記事は、レコード テンプレートの概念を紹介し、情報を共有するレコードを作成して使用する方法を説明します。

Microsoft Dynamics 365 for Finance and Operations のレコード テンプレートは、レコードをもっと迅速に作成することができます。 Microsoft Dynamics 365 for Finance and Operations のレコード タイプの一部のみを対象としたレコード テンプレートを作成できます。

たとえば、 サンフランシスコにあるレンタカー事業のレンタル情報を入力するとします。 顧客のほとんどは、サンフランシスコ周辺から来ますから、レンタル フォームの **州**、**国**、**市町村** フィールドに値を自動的に記入できれば、良いでしょう。

> [!NOTE]
> テンプレートを適用できるのは、アクセス権のある Finance and Operations の領域だけです。 ただし、すべてのユーザーが使用できるテンプレートを作成している場合、新しいレコードを作成すると、すべてのテンプレートのタイトルが、本人と他のユーザーに表示されます。 テンプレートを命名する場合には、これを考慮してください。 たとえば、法人の一部の従業員に歩合給が支払われていることが機密事項の場合、「コミッション」などの、用語が含まれる名前の使用を避けてください。

アクセス許可がある 1 つ以上のテンプレートが特定のフォームに存在し、そのフォームで新しいレコードを作成するときには、**目的のテンプレートの選択** ページが表示されます。 一覧からテンプレートを選択すると、新しいレコードが作成されて、選択したテンプレートに基づく既定の情報が設定されます。 新しいレコードを作成するときにテンプレートを使用しない場合は、**テンプレートの選択** ページの **今後このメッセージを表示しない** チェック ボックスをオンにします。 テンプレート選択ダイアログ ボックスを再び表示するには、レコードを右クリックし、**レコード情報** をクリックして、**テンプレート選択の表示** をクリックします。
