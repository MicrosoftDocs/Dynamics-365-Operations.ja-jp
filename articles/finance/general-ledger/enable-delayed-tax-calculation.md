---
title: 仕訳帳の税金計算遅延の有効化
description: このトピックでは、仕訳帳明細行の数が非常に大きい場合に、税金計算遅延の機能をオンにして、税額計算のパフォーマンスを向上させる方法について説明します。
author: EricWang
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: fddb6d3a9850b8f2f88f813f9591006637c7e535
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713137"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a>仕訳帳の税金計算遅延の有効化
[!include [banner](../includes/banner.md)]


このトピックでは、仕訳帳の消費税計算を遅らせる方法について説明します。 この機能により、多数の仕訳帳明細行がある場合に、税額計算のパフォーマンスを向上させることができます。

既定では、仕訳帳明細行の消費税金額は、税金に関連するフィールドが更新されるたびに計算されます。 これらのフィールドには、消費税グループと品目消費税グループのフィールドが含まれます。 仕訳帳明細行を更新すると、すべての仕訳帳明細行の税額が再計算されます。 この動作は、ユーザーに対してリアルタイムで計算された税額を表示しますが、仕訳帳明細行の数が非常に大きい場合はパフォーマンスにも影響を与える可能性があります。

税金計算遅延の機能を使用すると、仕訳帳の税額計算を遅らせるため、パフォーマンス問題を修正できます。 この機能が有効になっている場合、**消費税** を選択するか、仕訳帳を転記するときにのみ、税額が計算されます。

消費税の計算は、次の 3 つのレベルで遅らせることができます。

- 法人エンティティ
- 仕訳帳名
- 仕訳帳ヘッダー

システムによって、仕訳帳ヘッダーの設定が優先されます。 既定では、この設定は仕訳帳名から取得されます。 既定では、仕訳帳名の設定は、仕訳帳名の作成時に **一般会計パラメーター** ページの設定から取得されます。 次のセクションでは、法人、仕訳帳名、および仕訳帳ヘッダーの税金計算遅延を有効にする方法について説明します。

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a>法人レベルでの税金計算遅延の有効化

1. **一般会計 \> 元帳の設定 \> 一般会計パラメーター** の順に移動します。
2. **消費税** タブの **全般** クイック タブで、**税金計算遅延** オプションを **はい** に設定します。

![一般会計パラメーターの画像。](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a>仕訳帳名レベルでの税金計算遅延の有効化

1. **一般会計 \> 仕訳帳の設定 \> 仕訳帳名** の順に移動します。
2. **消費税** セクションの **全般** クイック タブで、**税金計算遅延** オプションを **はい** に設定します。

![仕訳帳名の画像。](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a>仕訳帳ヘッダー レベルでの税金計算遅延の有効化

1. **一般会計 \> 仕訳入力 \> 一般仕訳帳** の順に移動します。
2. **新規** を選択します。
3. 仕訳帳名を選択します。
4. **設定** タブで、**税金計算遅延** オプションを **はい** に設定します。

![一般仕訳帳ページの画像。](media/delayed-tax-calculation-journal-header.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
