---
title: 予算に基づく発注書の作成
description: この手順を使用して、利用可能な予算の確認をする発注書を作成します。
author: JennySong-SH
ms.date: 06/15/2020
ms.topic: business-process
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa9777ad3aa487dfb558879335f93f347b8ac749
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016191"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>予算に基づく発注書の作成

[!include [banner](../../includes/banner.md)]

この手順を使用して、利用可能な予算の確認をする発注書を作成します。

## <a name="review-the-budget-control-configuration"></a>予算管理コンフィギュレーションを確認する

1. **予算作成 > 設定 > 予算管理 > 予算管理行使** に移動します。
1. **利用可能な予算財源** タブを選択します。
1. **伝票と仕訳帳** タブを選択します。
1. **予算管理ルールの定義** タブを選択します。
1. **予算グループの定義** タブを選択します。
1. ページを閉じます。

## <a name="create-a-purchase-order"></a>発注書の作成

1. **調達 > 発注書 > すべての発注書** の順に移動します。
1. **新規** を選択します。
1. **仕入先** フィールドで、値を入力または選択します。
1. **概要** FastTab を展開します。
1. **会計日** フィールドで、日付を選択します。
1. **OK** を選択して新しい発注書を作成し、ダイアログ ボックスを閉じます。
1. **発注書明細行** クイック タブで、ツール バーの **行の追加** を選択して新しい行を追加し、必要に応じて明細行に情報を入力して、注文に品目を追加します。
1. **発注書明細行** クイックタブで、**財務 \> 金額を配布** を選択します。
1. **勘定科目** フィールドで、アカウントを指定します。
1. ページを閉じます。

## <a name="perform-budget-checking"></a>予算確認の実行

1. 行を追加した発注書の処理を続行します。
1. **発注書明細行** クイックタブ ツールバーで、**財務 \> 予算確認を実行する** を選択します。
1. **発注書明細行** クイックタブ ツールバーで、**財務 \> 予算確認エラーまたは警告** を選択します。
1. **予算確認のエラーまたは警告** ダイアログを開きます。 確認の結果を確認し、**閉じる** を選択してダイアログを閉じます。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]