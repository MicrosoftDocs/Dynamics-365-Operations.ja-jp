--- 
title: "源泉徴収税の設定"
description: "源泉徴収税は仕入先に課せられる税金で、売上税トランザクションを作成しません。"
author: twheeloc
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dc4c0745235052cb4145bc7083fef1a88c8bb5c9
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-withholding-tax"></a>源泉徴収税の設定

[!include [task guide banner](../../includes/task-guide-banner.md)]

源泉徴収税は仕入先に課せられる税金で、売上税トランザクションを作成しません。 仕入先支払に対して計算される源泉徴収税は負債です。 このため、源泉徴収税を転記するための有効な勘定は、貸借対照表勘定または負債勘定のみとなります。 このタスク ガイドでは、源泉徴収税の設定方法について説明します。

1. [税] > [間接税] > [源泉徴収税] > [源泉徴収税コード] の順に移動します。
2. [新規] をクリックします。
3. [源泉徴収税コード] フィールドに値を入力します。
4. [源泉徴収税名] フィールドに、源泉徴収税コードの名前を入力します。
5. [主勘定] フィールドで、源泉徴収税の未払税金を転記する主勘定を選択します。
6. [保存] をクリックします。
7. [値] をクリックします。
8. 一覧で、選択された行をマークします。
9. [値] フィールドに、源泉徴収税の計算に使用する割合を入力します。
10. [保存] をクリックします。
11. ページを閉じます。
12. [保存] をクリックします。
13. ページを閉じます。
14. [税] > [間接税] > [源泉徴収税] > [源泉徴収税グループ] の順に移動します。
15. [新規] をクリックします。
16. [源泉徴収税グループ] フィールドで、源泉徴収税グループの ID を入力します。
17. [説明] フィールドに、源泉徴収税グループの名前を入力します。
18. 一覧で、選択された行をマークします。
19. [源泉徴収税コード] フィールドで、源泉徴収税コードを選択します。
20. 一覧で、選択された行のリンクをクリックします。
21. [保存] をクリックします。


