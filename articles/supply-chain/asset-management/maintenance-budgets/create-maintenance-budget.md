---
title: メンテナンス予算の作成
description: このトピックでは、資産管理でメンテナンス予算を作成する方法について説明します。
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a375eb7c208479615b2d5e7cf78168ffd7ac8b16c52c85a7ef5a41aa69c947d5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776947"
---
# <a name="create-maintenance-budgets"></a>メンテナンス予算の作成

[!include [banner](../../includes/banner.md)]

 



メンテナンス予算は、予防的メンテナンスに対する予定原価の概要を提供するために使用されます。 予算明細行は、予算期間中に開始予定日を持つメンテナンス スケジュール明細行に基づいて計算されます。

メンテナンス予算は、資産管理の **予防的**、**修正**、および **投資** で使用される原価タイプに基づいています。 投資メンテナンスの予算原価は、予算期間内に交換日、および関連する交換価値がある有効な資産に対して使用されます。 過去の修正日が予算計算に含まれている場合、修繕メンテナンスの予算原価が含められます。 この場合、メンテナンス予算を計算する将来の同じ期間に対して、早い期間からの修正原価が計算されます。

## <a name="create-a-maintenance-budget"></a>メンテナンス予算の作成

1. **資産管理** \> **照会** \> **メンテナンス予算** \> **予算** の順に選択します。
2. **予算の作成** を選択します。
3. **メンテナンス予算** フィールドに、予算 ID を入力します。
4. **説明** フィールドに説明を入力します。
4. **期間** クイック タブの、**開始日** および **終了日** フィールドに、予算期間の開始日と終了日を入力します。
5. 前の期間の実際原価に基づいて計算される修正予算原価を含めるには、**修正開始日** フィールドに、これらの原価を含める期間の開始日を入力します。
6. 予算で必要な詳細レベルに応じて、5 つの **グループ化** クイック タブで関連するオプションを設定します。
7. **OK** を選択します。
8. **予算行** を選択して **メンテナンス予算行** ページを開きます。そこでは、期間に対して作成されたすべての予算行が表示されます。
9. 予算を承認するには、**メンテナンス予算** ページで予算を選択し、**承認** を選択します。 次に、**予算の承認** ダイアログ ボックスで、**OK** を選択します。 **メンテナンス予算** ページの **承認者** フィールドに、ユーザーの名前が入力されます。

    > [!NOTE]
    > メンテナンス予算を承認した後、最初に承認を削除しない限り、**メンテナンス予算行** ページの関連する明細行を再計算または調整することはできません。 メンテナンス予算の承認を削除するには、**メンテナンス予算** ページで予算を選択し、**承認** を選択します。 次に、**予算の承認** ダイアログ ボックスで、**OK** を選択します。

![メンテナンス予算。](media/01-maintenance-budgets.png)

既存の予算をコピーして新しいメンテナンス予算を作成することもできます。 **メンテナンス予算** ページで、コピーする予算を選択をし、次に **コピー** を選択します。 この方法は、たとえば、1 か月分の予算を作成していて、それを他の月にコピーする場合などに役立ちます。

> [!NOTE]
> メンテナンス予算で計算されるのは、メンテナン ススケジュール行に基づく予算原価のみです。 同じ期間の実際原価を計算するには、**資産原価管理** ページで計算を実行します。 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]