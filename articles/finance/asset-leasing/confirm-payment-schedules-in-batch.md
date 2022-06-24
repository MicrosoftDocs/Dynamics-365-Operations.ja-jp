---
title: 資産リースの支払いスケジュールをバッチで確認する
description: この記事では、複数の支払スケジュールをバッチで確認する方法について説明します。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymConfirmationDetails
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: bd75e22f6407d6bc25a78c1dfeacf70022238e94
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895054"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a>資産リースの支払いスケジュールをバッチで確認する

[!include [banner](../includes/banner.md)]

この記事では、複数の支払スケジュールをバッチで確認する方法について説明します。 支払スケジュールを、リース期間や確認バッチプロセスで確認します。 仕訳入力は、確認済の支払スケジュールが設定されたリースのみを転記できます。 支払スケジュールの確認は、そのリースの財務情報の最終承認として機能します。 支払リース料やリース期間など、リースに関する財務情報の将来的な変更はすべてリースの調整に該当し、その方法で処理する必要があります。

複数の支払スケジュールを確認するには、次の手順に従います。

1. **資産リース \> 定期 \> 確認バッチ** に移動します。
2. **確認バッチ** ページで、**確認バッチ** を選択します。
3. 表示されるダイアログ ボックスで、確認する帳簿をフィルター処理します。

    - 特定のリース グループに含まれるすべての帳簿を確認するには、**リース グループ** フィールドでグループを選択します。
    - 特定の帳簿を確認するには、**帳簿 ID** フィールドで帳簿を選択します。
    - すべての帳簿を確認するには、**すべての帳簿** パラメーターをオンにします。

新しく確認した帳簿の情報は、**確認済の帳簿** ページに表示されます。 支払スケジュールを確認した後、リースに対して当初認識の仕訳入力を転記できます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
