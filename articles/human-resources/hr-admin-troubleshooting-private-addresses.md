---
title: セキュリティ ロールで個人住所にアクセスする
description: この記事では、顧客が個人住所にアクセスできない場合の解決方法について説明します。
author: twheeloc
ms.date: 09/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c1db052937b03817f22b37c50b9f1b319579cb2
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702106"
---
# <a name="access-to-private-addresses-by-security-role"></a>セキュリティ ロールで個人住所にアクセスする


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**払出**

顧客がセキュリティ ロールを複製し、その新しいロールとしてサインインした後は、顧客はプライベートとしてマークされた住所を見ることができません。

**解像度**

問題を解決するには、顧客は複製したセキュリティ ロールのための以下の手順を実行する必要があります。

1. **組織管理\> グローバル アドレス帳 \> グローバル アドレス帳パラメーター** の順に移動します。
2. **プライベートな場所のセキュリティ** タブで、新しいセキュリティ ロールを **利用可能なロール** リストから、**選択されたロール** リストへ移動します。
3. **保存** を選択します。

![グローバル アドレス帳パラメーター ページ。](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
