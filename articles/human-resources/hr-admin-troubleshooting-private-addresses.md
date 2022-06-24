---
title: セキュリティ ロールで個人住所にアクセスする
description: この記事では、顧客が個人住所にアクセスできない場合の解決方法について説明します。
author: twheeloc
ms.date: 08/19/2021
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
ms.openlocfilehash: 7102bbcbecec0d88351e796e2c63663d956b86f0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849684"
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
