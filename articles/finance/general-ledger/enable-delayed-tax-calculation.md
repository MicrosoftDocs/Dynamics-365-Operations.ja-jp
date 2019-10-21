---
title: 仕訳帳の税金計算遅延の有効化
description: このトピックでは、仕訳帳明細行の量が膨大な場合に、**仕訳帳の税金計算遅延の有効化**機能を使用して、税額計算のパフォーマンスを向上させる方法について説明します。
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178619"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a>仕訳帳の税金計算遅延の有効化
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

このトピックでは、仕訳帳明細行の量が膨大な場合に、**仕訳帳の税金計算遅延の有効化**機能を使用して、税額計算のパフォーマンスを向上させる方法について説明します。

仕訳帳の現在の売上税計算の動作は、ユーザーが売上税グループ/品目売上税グループなどの税関連フィールドを更新したときにリアルタイムで発生します。 仕訳帳明細行レベルで更新すると、すべての仕訳帳明細行の税額が再計算されます。 この方法では、ユーザーはリアルタイムに計算された税額を確認できますが、仕訳帳明細行の量が膨大な場合はパフォーマンスの問題が発生することがあります。

この機能は、パフォーマンスの問題を解決するために税金計算を遅延させるオプションを提供します。 この機能が有効になっている場合、ユーザーが "売上税" コマンドをクリックするか、仕訳帳を転記するときにのみ、税額が計算されます。

ユーザーは、次の 3 つのレベルでパラメーターをオンまたはオフにできます。
- 法人ごと
- 仕訳帳名ごと
- 仕訳帳ヘッダーごと

システムは、仕訳帳ヘッダーのパラメーター値を最終値として受け取ります。 仕訳帳ヘッダーのパラメーター値は、既定で仕訳帳名から取得されます。 仕訳帳名のパラメーター値は、仕訳帳名の作成時に総勘定元帳パラメーターの既定値になります。

このパラメーターをオンにすると、仕訳帳の "実際の売上税額" フィールドと "計算済売上税額" のフィールドが除外されます。 そうすることにより、ユーザーが税計算を開始する前にこれら 2 つのフィールドの値は常に 0 を示すことになり、ユーザーを混乱させません。

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a>法人ごとの税金計算遅延の有効化

1. **総勘定元帳 > 元帳の設定 > 総勘定元帳のパラメーター**の順に移動する
2. **売上税**タブをクリックする
3. **一般**クイック タブで、パラメーター**税金計算の遅延**を有効または無効にする

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a>仕訳帳ごとの税金計算遅延の有効化

1. **総勘定元帳 > 仕訳帳の設定 > 仕訳帳名**に移動する
2. **一般**クイック タブで、パラメーター**税金計算の遅延**を有効または無効にする

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a>仕訳帳ごとの税金計算遅延の有効化

1. **総勘定元帳 > 仕訳入力 > 一般仕訳帳**の順に移動する
2. **新規**をクリックする
3. 仕訳帳名を選択する
4. **設定**をクリックする
5. パラメーター**税金計算の遅延**を有効または無効にする

![](media/delayed-tax-calculation-journal-header.png)
