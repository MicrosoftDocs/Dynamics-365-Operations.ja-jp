---
title: 税が計算されていないか、税額がゼロである
description: この記事では、税額が 0 (ゼロ) になる場合、または税金が計算されていない場合に役立つトラブルシューティングの情報を提供します。
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: f2a5bb0d1cef93ec1fea2e21c1750fe94a454c18
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849847"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a>税金が計算されない、または税額がゼロになる

[!include [banner](../includes/banner.md)]

トランザクションの明細金額は 0 (ゼロ) 以外になりますが、計算されない場合や計算された税額が 0 になることもあります。 この問題のトラブルシューティングを行う場合は、必要に応じて次のセクションの手順に従います。

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a>トランザクションで税コードが正しく選択されていることを確認する

トランザクションで正しい税コードが選択されていない場合、または税コードが選択されていない場合、税金は計算されません。 次の手順に従って、トランザクションで税コードが正しく選択されていることを確認します。 

1. トランザクション明細行で、**明細行の詳細** クイック タブの、**設定** タブの、**消費税** セクションで、**品目消費税グループ** フィールドと **消費税グループ** フィールドに正しい税グループが選択されていることを確認します。 正しい税グループが選択されていない場合は、選択します。

    [![品目消費税グループと消費税グループフィールド。](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)

2. **税** \> **間接税** \> **消費税** \> **消費税グループ** の順に移動します。
3. 適切な消費税グループを選択し、**設定** クイック タブで、**消費税コード** フィールドの税コードをメモします。

    [![消費税グループ ページ。](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)

4. **税** \> **間接税** \> **消費税** \> **品目消費税グループ** の順に移動します。
5. 適切な品目消費税グループを選択し、**設定** クイック タブで、**消費税コード** フィールドの税コードが消費税グループの税コードと一致しているかを確認します。

    [![品目消費税グループ ページ。](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)

6. 税コードが一致しない場合は、消費税コードをグループのいずれかに更新します。

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a>選択した税コードが免税でないか、税率の値が正確かを確認する

税コードが免税の場合、または税率が 0 (ゼロ) の場合、税計算結果は 0 になります。 次の手順に従って、選択した税コードが免税かどうか識別し、正確な税率が適用されていることを確認します。

1. **税** \> **間接税** \> **消費税** \> **消費税グループ** の順に移動します。
2. 適切な消費税グループを選択し、**設定** クイック タブで、**免税** チェック ボックスがオフになっていることを確認します。 選択されている場合はオフにしてください。

    [![消費税グループ ページの免税チェック ボックス。](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)

3. **税** \> **間接税** \> **消費税** \> **消費税コード** の順に移動します。
4. 適切な消費税コードを選択し、**値** フィールドの税率の値が 0 (ゼロ) でないかを確認します。 0 の場合は、フィールドを更新して、正確な税率を設定します。

    [![消費税コード値ページの値フィールド。](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a>ゼロが正しい税額かどうかを判断する

シナリオによっては、税額が 0 (ゼロ) で正しい場合があります。 トランザクションの正確な税額が 0 かどうかを確認するには、次の手順に従います。

1. **一般会計** \> **元帳の設定** \> **総勘定元帳パラメーター** の順に移動します。
2. **消費税** タブの、**計算方法** フィールドで、**合計** が選択されていることを確認します。

    [![総勘定元帳パラメーター ページの計算フィールド。](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)

3. **税** \> **間接税** \> **消費税** \> **消費税コード** の順に移動します。
4. 適切な消費税コードを選択し、**計算** \> **基準金額** を選択して、基準金額が **請求書残高の正味金額** または **その他の売上税金額を含む請求合計** に設定されていることを確認します。 詳細については、[その他の売上税金額を含む請求合計](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts)を参照してください。
5. 手順 2 と 4 で正しい値が設定されている場合は、トランザクションの合計金額が 0 (ゼロ) かどうかを判断します。 合計金額が 0 の場合、予想される結果は税額 0 です。 税額は請求書残高の合計金額に基づいて計算され、1 行ずつ計算されないため、税計算の後、各明細行に税額 0 が割り当てられます。

## <a name="determine-whether-customization-exists"></a>カスタマイズが存在するかどうかの確認

前のセクションの手順を完了し、問題が見つからなかった場合は、カスタマイズが存在するかどうかを確認します。 カスタマイズが存在しない場合、さらにサポートを受けるために Microsoft サービス要求を作成します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
