---
title: 源泉徴収税の設定
description: このトピックでは、源泉徴収税を設定する方法について説明します。
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 135cca434a1689bf22ee468894dcf8746071e7ca
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144700"
---
# <a name="set-up-withholding-tax"></a>源泉徴収税の設定

[!include [banner](../../includes/banner.md)]

このトピックでは、源泉徴収税を設定する方法について説明します。 *源泉徴収税*は仕入先に課せられる税金で、売上税トランザクションを作成しません。 仕入先支払に対して計算される源泉徴収税は負債です。 このため、源泉徴収税を転記するための有効な勘定は、貸借対照表勘定または負債勘定のみとなります。 このタスク ガイドでは、源泉徴収税の設定方法について説明します。

1. **ナビゲーション ウィンドウ > モジュール > 税 > 間接税 > 源泉徴収税 > 源泉徴収税コード**の順に移動します。
2. **新規** を選択します。
3. **源泉徴収税コード** フィールドに値を入力します。
4. **源泉徴収税名**フィールドに、源泉徴収税コードの名前を入力します。
5. **主勘定**フィールドで、源泉徴収税の未払税金を転記する主勘定を選択します。
6. **保存** を選択します。
7. **値**を選択し、リスト内の目的のレコードをマークします。
8. **値**フィールドに、源泉徴収税の計算に使用する割合を入力します。
9. **保存** を選択します。
10. ページを閉じます。
11. **保存** を選択します。
12. ページを閉じます。
13. **ナビゲーション ウィンドウ > モジュール > 税 > 間接税 > 源泉徴収税 > 源泉徴収税グループ**の順に移動します。
14. **新規** を選択します。
15. **源泉徴収税グループ** フィールドで、源泉徴収税グループの ID を入力します。
16. **説明**フィールドに、源泉徴収税グループの名前を入力します。
17. **源泉徴収税コード** フィールドで、源泉徴収税コードを選択します。
18. **保存** を選択します。
19. ページを閉じます。

