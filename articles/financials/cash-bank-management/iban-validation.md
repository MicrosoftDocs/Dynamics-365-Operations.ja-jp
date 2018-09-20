---
title: "国際銀行番号 (IBAN) 口座の検証を管理"
description: "このトピックでは、国際銀行番号 (IBAN) 口座の検証を管理する方法を説明します。"
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: ja-jp
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a>国際銀行番号 (IBAN) 口座の検証を管理

[!include [banner](../includes/banner.md)]

国際銀行番号 (IBAN) 口座の検証により、銀行口座に IBAN を追加するときに行われる検証の量が増加します。

IBAN の構造は、Microsoft Dynamics 365 for Finance and Operations に格納され、銀行口座で IBAN を初めて使用するときに自動的に読み込まれます。 銀行口座番号とは、IBAN 番号に対して定義された構造の一部です。 その構造に基づいて、IBAN の口座番号の長さおよび位置が、国または地域ごとの構造で定義されている位置と一致しない場合、警告メッセージが表示されます。

## <a name="set-up-iban-structures"></a>IBAN 構造の設定

1. **現金および銀行管理\>設定\> IBAN 構造**に移動します。
2. 国や地域ごとの IBAN 構造は、自動的に設定されていることに注意してください。
3. 特定の国または地域の構造をカスタマイズする必要がある場合は、それらを編集できます。
4. 構造定義は、それぞれの新しいリリースの一部になります。 **構造をリセットする**メニューを使用して、各更新後に最新の定義を読み込むことができます。

## <a name="validate-the-iban-structure-in-a-bank-account"></a>銀行口座の IBAN 構造を検証

1. **現金および銀行管理\>銀行口座\>銀行口座**に移動します。
2. 銀行口座を作成します。
3. **追加情報**クイック タブで、IBAN を入力します。

    IBAN の口座番号の長さおよび位置が、国または地域ごとの構造で定義されている位置と一致しない場合、メッセージが表示されます。 IBAN の長さが IBAN 構造の長さと一致しない場合は続行できません。

    検証では、銀行口座番号が銀行口座番号を表す IBAN の一部と一致していることも確認します。 銀行口座番号が一致しない場合は、警告メッセージが表示されます。 このメッセージは、警告のみです。 銀行口座番号と一致しない場合でも続行することができます。

