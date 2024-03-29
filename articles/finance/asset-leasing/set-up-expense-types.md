---
title: 経費タイプの設定
description: この記事では、資産リースで資産タイプを設定する方法について説明します。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseExpenseTypeTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9978041059437d5d3556236c7ac02c00db93f933
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908041"
---
# <a name="set-up-expense-types"></a>経費タイプの設定

[!include [banner](../includes/banner.md)]

この記事では、資産リースで資産タイプを設定する方法について説明します。 支払スケジュールによって表されない原価は、*経費原価* と呼ばれます。 このような原価の例としては、税金、一般的な領域保守にかかる費用、保険料などがあります。

## <a name="add-an-administrative-expense-type"></a>管理経費タイプの追加

1. **資産リース \> 設定 \> 経費タイプ** の順に移動します。
2. **新規** を選択します。
3. 適切なフィールドに、新しい経費タイプと説明を入力します。

## <a name="assign-accounts-to-administrative-costs"></a>管理原価に対する勘定の割り当て

次に、勘定を経費タイプに関連付けます。 これらの勘定は、経費スケジュール エントリが転記されると借方に転記されます。 相手勘定は、各リースの **履行費用支払スケジュール** 明細行に対して指定されます。

1. **資産絵イース \> 設定 \> 資産リース パラメーター** の順に移動します。
2. **勘定** タブの **履行費用** クイックタブの **経費タイプ** フィールドで、経費タイプを選択します。
3. **追加** を選択します。
4. **帳簿タイプ** フィールドで、管理原価にリンクする帳簿タイプを選択します。

    > [!NOTE]
    > 同じ経費勘定に複数の帳簿タイプを関連付けることができます。

5. **勘定コード** フィールドで、この帳簿をどのリースに適用するかを指定します。

    - **すべて** – 帳簿をすべてのリースに適用します。
    - **グループ** – 特定のリース グループに帳簿を適用します。
    - **テーブル** – 帳簿を特定のリースに適用します。

6. **グループ** または **テーブル** を **勘定コード** フィールドで選択した場合、勘定番号またはグループ番号を **勘定/グループ番号** フィールドで選択します。
7. 該当するフィールドで、ファイナンス リースの主勘定と、オペレーティング リースの主勘定を選択します。

これらの手順を完了したら、選択したリースの **リース詳細** ページに **履行費用支払スケジュール** 明細行を使用して経費を追加できます。 別の方法として、新しいリースを作成するときに経費を追加することもできます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
