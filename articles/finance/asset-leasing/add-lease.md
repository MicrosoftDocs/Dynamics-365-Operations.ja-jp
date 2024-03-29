---
title: リースの追加またはコピー (プレビュー版)
description: この記事では、新しいリースを作成する方法について説明します。これにより、資産リースの情報の入力や、既存のリースから情報をコピーすることができます。
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 798ab3ece45ee6f21694a364cfb7a4ff14a9c8aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880935"
---
# <a name="add-or-copy-leases-preview"></a>リースの追加またはコピー (プレビュー版)

[!include [banner](../includes/banner.md)]

この記事では、資産リースに最初からリースを作成する方法と、既存のリースをコピーしてリースを作成する方法について説明します。 最初からリースを作成するには、新しいリースの情報を入力し、リース スケジュールを作成する必要があります。 ひとつ以上のリースを設定しておくと、既存のリースから情報をコピーして、新しいリースの作成に必要な情報を簡単に編集することができます。

## <a name="create-a-lease"></a>リースの作成

アセット リースでリースを作成するには以下の手順に従ってください。

1. **リースの概要** ページの、アクション ウィンドウで、**新規** を選択します。
2. リースの情報を入力します。 必須フィールドには赤い境界線が表示されます。

リース支払の開始日をリースの開始日より前の日付には設定できません。 リースの支払開始日をリース開始日よりも早く入力すると、エラーメッセージが表示されます。

既定では、**資産リース パラメーター** ページの **支払内訳を許可する** オプションが **はい** に設定されている場合、**リースの詳細** ページの **一般** クイックタブの **支払金額の内訳** オプションは **いいえ** に設定されます。 

**支払金額の内訳** オプションが **はい** に設定されている場合、**支払スケジュール明細行** クイックタブの **支払金額** フィールドはロックされます。 **支払金額の内訳** カタログに後で入力する支払金額の合計に設定します。

**支払金額の内訳** を選択すると、明細化した支払タイプを追加できるページが表示されます。 **支払金額に合計を加算する** ボタンを押すと、**支払金額** フィールドに合計を移動します。

> [!NOTE]
> 明細化した支払金額を追加してから **Esc** キーを選択すると、入力した金額は **支払スケジュール明細行** クイックタブの **支払金額** フィールドに追加されません。 その代わり **支払金額の内訳** ダイアログ ボックスに格納されます。 ダイアログ ボックスに合計金額を表示させる場合は **金額** 列を選択し、選択したまま (または右クリック)、**この列の合計** を選択します。 

**行のコピー** ボタンを押すと、明細化した支払内訳をコピーします。

## <a name="create-a-lease-schedule"></a>リース スケジュールの作成

リースの情報を入力後、次の手順に従ってリース スケジュールを作成します。

> [!NOTE]
> 財務分析コードは、ユーザー定義の財務分析コードに基づいて変更される場合があります。

1. **スケジュールの作成** を選択して、リース帳簿を生成します。 リース帳簿には、支払、償却、減価償却、経費のスケジュールが含まれています。
2. リース帳簿にアクセスし、新しく作成されたスケジュールを表示するには、**帳簿** タブを選択します。

    **帳簿の詳細** ページには、割り当てられている帳簿ごとにリースがどのように計上されるかが示されます。 ここでは、リースのスケジュールを表示できます。

    支払スケジュールには、**リースの追加** ページの **支払スケジュール明細行** タブの入力が含まれます。 各支払額や変動支払を変更することも可能です。 リース負債は、変更された支払スケジュールに基づいて計算されます。

    > [!NOTE]
    > リース支払の開始日には、リースの開始日以降を指定してください。 支払の開始日がリースの開始日よりも早い場合は、エラー メッセージが表示されます。 

4. 支払スケジュールの確認が完了したら、**スケジュールの確認** を選択します。 スケジュールを確認した後は、そのリースを編集できなくなります。

    > [!NOTE]
    > **リースの追加** ページの支払スケジュール明細行から自動的にリース期間が計算され ます。
    >
    > リース期間を月単位で計算する場合は、特定の支払スケジュール明細行の開始日と終了日の差分が検出されます。 その後、次の支払スケジュール明細行に移動し、差分を再び検索します。 最後に、すべての金額を合計して、月単位でのリース期間を決定します。

5. 計算された期限の経費を表示するには、**負債償却スケジュール**  ページを開きます。 計算された定額減価償却を表示するには、**資産減価償却スケジュール** ページを開きます。
6. 計算された金額の確認が完了したら、**当初認識** ページで当初認識の仕訳入力を作成できます。 仕訳帳が作成されたことを示すメッセージが表示されます。

    > [!NOTE]
    > 仕訳帳エントリは、手動でエントリを転記するまで一般会計に転記されません。

7. 転記前に、提案された当初認識のエントリを確認するには、**資産のリース仕訳帳を選択** します。

    > [!NOTE]
    > 資産のリース仕訳帳は手動で作成できません。 リースのスケジュールが作成されると、自動的に作成されます。

8. 当初認識仕訳帳エントリを確認し、転記の準備ができている場合は、**転記** を選択して、一般会計における資産の使用権 (ROU) とリース負債を認識します。

## <a name="copy-a-lease"></a>リースのコピー

資産のリースではリースの詳細をコピーして、同じ情報を持つ新しいリースを作成することができます。 コピーしたリースのスケジュールを作成する前に、リース フィールドを変更することができます。

1. **リースの概要** ページで、コピーするリースを選択し、[アクション] ウィンドウで **リースのコピー** を選択します。

    > [!NOTE]
    > リース ID の番号順に **手動** パラメーターをオフにした場合、そのシーケンスの次の番号はコピーされたリースのリース ID として自動的に生成されます。 **手動** のパラメーターが有効になっている場合は、リース のコピーを続行する前に、リースIDの入力を求めるメッセージが表示されます。

2. **コピー** を選択します。 選択したリースのリースの詳細が新しいリースにコピーされます。 その後、保存する前に新しいリースの詳細を編集して、リース スケジュールを作成することができます。

## <a name="asset-leasing-journal"></a>資産リース仕訳帳

資産リースで作成されたすべての仕訳帳エントリは、資産リース仕訳帳に含まれています。 **資産のリース仕訳帳**  ページ (**資産のリース契約 \> 仕訳帳のエントリ \> 資産のリース仕訳帳**) では、転記ステータス別にフィルタリングし、特定の仕訳帳エントリと伝票を表示して、未転記仕訳帳エントリを転記することができます。

> [!NOTE]
> 資産のリース仕訳帳は手動で作成できません。 リースのスケジュールが作成されると、自動的に作成されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
