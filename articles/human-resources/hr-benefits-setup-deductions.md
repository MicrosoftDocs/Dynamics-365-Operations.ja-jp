---
title: 控除のコンフィギュレーション
description: Microsoft Dynamics 365 Human Resources の控除を使用して、各給付金について従業員の給与から控除する金額 (必要な場合) を決定します。
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c84e44e784e18c82098d63909f198049ae5f995c
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113259"
---
# <a name="configure-deductions"></a>控除のコンフィギュレーション

Microsoft Dynamics 365 Human Resources の控除を使用して、各給付金について従業員の給与から控除する金額 (必要な場合) を決定します。 控除は日付が有効であるため、控除情報の履歴を記録しておくことができます。 

1. **給付金管理** ワーク スペースの **設定** で、**控除** を選択します。

2. **新規** を選択します。

3. 次のフィールドの値を指定します。

   | フィールド | 説明 |
   | --- | --- |
   | **控除** | 給付金の控除を識別するために使用される固有の ID。 |
   | **説明** | 控除の説明を入力します。 |
   | **開始** | 開始日。 既定値は現在のシステム日付です。 |
   | **有効期限** | 終了日。 既定値は 12/31/2154 で、意味がありません。 |
   | **ヘッダー** | この控除が給与の給付金を処理するときに控除の従業員部分に使用する給与計算システムの見出しコード。 これは、サード パーティの給与計算プロバイダーを使用するときに使用されます。 |
   | **従業員給与控除参照** | 給与計算のために給付金を処理する際に、従業員分の控除に対して、この控除で使用する給与システムの控除コード。 |
   | **金額の見出し** | 給与の給付金を処理するときに、この控除額が従業員の控除部分に使用する給与計算システムの見出しコード。 これは通常、サード パーティの給与計算プロバイダーを使用するときに使用されます。 |
   | **削除可能** | Dynamics 365 for Finance and Operations からエクスポートされた値が給与計算システムで値を削除できるかどうかを指定します。 |
   | **ペアの列** | 対になった隣接する列の見出しと控除額を給与計算システムにエクスポートするかどうかを指定します。 |
   | **変更の有効日** | 給付控除の変更が有効になる日付。 この日付に、システムは自動的に給付控除を変更し、**控除変更の更新** 処理を実行している限り、この控除に関連するすべての給付プランを更新します。 |
   | **控除の変更が完了しています** | 控除更新の変更処理によって給付控除の変更が完了すると、**控除の変更が完了しました** チェック ボックスが自動的に選択されます。 |
   
4. 利益率の設定に対する変更を追跡して維持するには、**アクション** を選択し、**バージョンの維持** を選択します。

5. **保存** を選択します。 


[!INCLUDE[footer-include](../includes/footer-banner.md)]