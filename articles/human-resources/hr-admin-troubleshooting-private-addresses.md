---
title: セキュリティ ロールで個人住所にアクセスする
description: この記事では、顧客が個人住所にアクセスできない問題を解決する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fbe0e8acc1b879e4d7982b33413236432f25f630
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419348"
---
# <a name="access-to-private-addresses-by-security-role"></a>セキュリティ ロールによる個人住所へのアクセス

**払出**

顧客がセキュリティ ロールを複製し、その新しいロールとしてサインインした後は、顧客はプライベートとしてマークされた住所を見ることができません。

**解像度**

問題を解決するには、顧客は複製したセキュリティ ロールのための以下の手順を実行する必要があります。

1. **組織管理\> グローバル アドレス帳 \> グローバル アドレス帳パラメーター** の順に移動します。
2. **プライベートな場所のセキュリティ** タブで、新しいセキュリティ ロールを **利用可能なロール** リストから、**選択されたロール** リストへ移動します。
3. **保存** を選択します。

![グローバル アドレス帳パラメーター ページ](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]