---
title: 国際銀行番号 (IBAN) 口座の検証を管理
description: この記事では、国際銀行番号 (IBAN) 口座の検証を管理する方法を説明します。
author: twheeloc
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 3d825e8699fbe10e080cd85f15d3d86f8c780f15
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880902"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a>国際銀行番号 (IBAN) 口座の検証を管理

[!include [banner](../includes/banner.md)]

国際銀行番号 (IBAN) の検証により、銀行口座に IBAN を追加するときに行われる検証の量が増加します。

IBAN の構造に関する情報は Microsoft Microsoft Dynamics 365 Finance に保存され、銀行口座で IBAN を初めて使用するときに自動的に読み込まれます。 これには、IBAN の長さ、銀行口座番号と銀行支店コードの開始位置、銀行口座番号と銀行支店コードの長さが含まれています。

## <a name="set-up-iban-structures"></a>IBAN 構造の設定

1. **現金および銀行管理\>設定\> IBAN 構造** に移動します。
2. 国や地域ごとの IBAN 構造は、自動的に設定されていることに注意してください。
3. 特定の国または地域で構造を更新する必要がある場合は、**編集** ボタンを選択します。
4. 構造定義は、それぞれの新しいリリースの一部になります。 **構造をリセットする** メニューを使用して、各更新後に最新の定義を読み込むことができます。

## <a name="validate-the-iban-structure-in-a-bank-account"></a>銀行口座の IBAN 構造を検証

1. **現金および銀行管理\>銀行口座\>銀行口座** に移動します。
2. 銀行口座を作成します。
3. **追加情報** クイック タブで、IBAN を入力します。

    IBAN の長さがそれぞれの国や地域に定義されている長さと一致しない場合、警告メッセージが表示されます。 IBAN の長さが IBAN 構造で指定された長さと一致しない場合は続行できません。

    検証では、銀行口座番号が銀行口座番号を表す IBAN の一部と一致していることも確認します。 銀行口座番号が一致しない場合は、警告メッセージが表示されます。 このメッセージは、警告のみです。 銀行口座番号と一致しない場合でも続行することができます。

    検証では、銀行支店コードが銀行支店コードを表す IBAN の一部と一致していることも確認します。 銀行支店コードには、銀行番号と、多くの場合は追加の銀行支店が含まれます。 銀行支店コードが一致しない場合は、警告メッセージが表示されます。 このメッセージは、警告のみです。 銀行支店コードが一致しない場合でも続行することができます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
