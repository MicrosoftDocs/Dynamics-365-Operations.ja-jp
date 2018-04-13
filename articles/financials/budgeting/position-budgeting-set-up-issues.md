---
title: "職位の予算作成のトラブルシューティング"
description: "この記事は、職位の予算作成をコンフィギュレーションするときに提起される可能性のある質問に対する回答を提供します。 これは、予算原価要素、報酬グループ、および報酬グリッドの作成方法に関する、よく寄せられる質問に対処します。"
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f2ef04008a5e6339a2193f9fcc77f2e0e6643557
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="position-budgeting-troubleshooting"></a>職位の予算作成のトラブルシューティング

[!INCLUDE [banner](../includes/banner.md)]

この記事は、職位の予算作成をコンフィギュレーションするときに提起される可能性のある質問に対する回答を提供します。 これは、予算原価要素、報酬グループ、および報酬グリッドの作成方法に関する、よく寄せられる質問に対処します。 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a>人事管理で [予測職位] ページが見つからないのはなぜですか。
---------------------------------------------------------------

予測職位は予算作成に移動されました。

## <a name="why-cant-i-delete-a-budget-cost-element"></a>予算原価要素をどうして削除できませんか
予測職位に割り当てられている予算原価要素は削除できません。 予算原価要素を削除するには、その前に、すべての予測職位からその予算原価要素を削除してください。 **ヒント:** 予算原価要素が割り当てられているすべての職位を検索するには、[**予算原価要素**] ページの原価要素を選択し、[**職位の更新**] をクリックします。 原価要素を使用している職位が上部グリッドに表示されます。

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a>どのように各原価要素を開かずに複数の予測職位から原価要素を削除できますか。
原価要素を削除することはできません。 ただし、予算計画サイクルの日付の範囲外になるように開始日と終了日を変更した場合、その予算計画サイクルの予測職位に原価要素は割り当てられなくなります。 この変更を加えるには、予算原価要素を開き、[**原価計算**] クイックタブで [**日付の変更**] を開き、有効日または有効期限を変更します。 その後、原価要素が割り当てられているすべての予測職位を自動的に更新するには [**OK**] をクリックします。 **ヒント:** この方法を使用する場合、開始日と終了日が該当する範囲外にある**すべての**予測職位から予算原価要素が削除されることに注意してください。 この効果が予定外のことである場合は、予算原価要素を削除する各予測職位を開き、手動で変更を行う必要があります。

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a>予算原価要素の [原価計算] クイック タブに年間金額を入力できないのはどうしてですか。
システムは値を計算するための割合を必要とするので、[**計算基準**] クイック タブに予算原価要素が存在する場合、年間金額を入力できません。 この値を変更するには、[**計算基準**] クイック タブからすべての予算原価要素を削除してください。

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a>予算原価タイプを収入から別の予算原価タイプに変更できないのはどうしてですか。
一部の予算原価要素は、計算の基礎として、収入原価要素を使用します。 [**予算原価タイプ**] フィールドを変更するには、すべての予算原価要素の [**計算基準**] クイック タブから収入原価要素を削除します。

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a>予算原価要素の予算原価要素明細行の日付を変更できないのはどうしてですか
予算原価要素が予測職位によって使用されているときは、予算原価要素明細行の日付を変更できません。 この制限は、予測職位が予算原価要素のガイドラインにかならず準拠するのを保証するために役立ちます。 日付を変更するには、[**原価計算**] クイック タブで [**日付の変更**] をクリックして新しい日付を入力します。 その後、原価要素が割り当てられている予測職位を更新するには [**OK**] をクリックします。

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a>[報酬グループ] ページで予算原価要素の原価を変更できないのはどうしてですか。
予算原価要素は、[**予算原価要素**] ページでのみ作成および変更できます。

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a>予測職位の原価要素の日付を変更するときエラー メッセージが表示されるのはどうしてですか。
予測職位の原価要素明細行の日付は、次の範囲にある必要があります。

-   職位の有効日と有効期限。
-   予算原価要素の有効日と有効期限。
-   予測職位の予算計画プロセスに関連付けられている予算サイクルの開始日と終了日。





