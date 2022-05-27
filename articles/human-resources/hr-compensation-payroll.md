---
title: 支払準備完了
description: このトピックでは、Dynamics 365 Human Resources で従業員に支払準備完了をマークする方法を説明します。
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-07-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 62d86de9c0ad6d6d7ee8375f7664f96e2a30783d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693811"
---
# <a name="ready-to-pay"></a>支払準備完了


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

> [!NOTE]
> 従業員に支払準備完了をマークしたい場合は、まず機能管理で **(プレビュー) 給与統合** 機能を有効にする必要があります。 プレビュー機能を有効にする方法については、[機能の管理](hr-admin-manage-features.md)を参照してください。

この機能により、人事担当者は、給与処理の準備が整っている従業員と、サード パーティの給与計算プロバイダーによって使用される前にアクションが必要な従業員とを理解することができます。

## <a name="mark-employee-as-ready-to-pay"></a>従業員に支払準備完了をマークする

従業員情報を収集して検証することは時間がかかり、エラーも発生しやすくなります。 Dynamics 365 Human Resources は、人事担当者が従業員情報を確認し、簡単に更新できる方法を提供することで、給与処理の準備にかかる時間を削減するのに役立ちます。

従業員に支払準備完了をマークするには:

1. **報酬管理** を開く。 ワークスペースには 2 つのタイルがあります: 
    - **支払準備ができている従業員**
    - **支払準備が完了していない従業員**
    ![報酬管理ワークスペース。](./media/hr-ready-to-pay-1-workspace.png)

2. **支払準備が完了していない従業員** を選択します。

3. 検証する従業員を選択します。 **給与タブ** の **支払準備完了** グループで、**検証** を選択します。
    ![従業員を検証する。](./media/hr-ready-to-pay-2-validate.png)

4. 結果を確認するには、**給与タブ** の **支払準備完了** グループで、**結果** を選択します。

## <a name="validation"></a>検証

従業員に支払い準備完了をマークする前に、従業員プロフィールの完全性が検証されます。

![結果を検証する。](./media/hr-ready-to-pay-3-results.png)

| 検証 | 細目 |
| --- | --- |
| **住所の目的パラメーター** | **給与住所の使用目的** パラメーターが選択されていることを確認します。 |
| **給与住所** | 従業員プロファイルは、目的が **給与支払者の居住地** または **給与支払者の勤務地** となっている住所が 1 つ以上あり、目的ごとに 1 つの住所しかないことを確認します。 |
| **雇用** | 従業員が少なくとも 1 つの雇用 (現在、過去、将来) があるかどうかを確認します。 |
| **ID 番号** | **人事管理パラメーター** ページの **給与計算における識別情報の使用** フィールドが **はい** であり、パラメーターに示された識別タイプが従業員プロファイルに記入されているかどうかを確認します。 |
| **氏名** | **姓** フィールド と **名** フィールドの入力を確認します。|
| **ポジション番号** | 作業者に職位が割り当てられているかどうかを確認します。 |
| **生年月日** | **誕生日** フィールドに入力を確認します。 |
| **報酬** | 作業者が固定報酬プランに登録されているかどうかを確認します。 |

これらの検証のうち 1 つが失敗した場合は、従業員を支払準備完了としてマークすることはできません。

**支払準備完了** フィールドが **いいえ** の場合、作業者プロファイルを完全にするためにアクションを実行する必要があることを示します。 これによって、どのデータ エンティティへのデータ公開も停止されることはありません。 

## <a name="process-automation"></a>プロセスの自動化

[プロセス オートメーション](/dynamics365/fin-ops-core/dev-itpro/sysadmin/process-automation)を使用すると、すべての従業員の検証を自動化できます 。 **報酬管理** ワークスペースで、**リンク**\>**パラメーター**\>**プロセス の自動化** に移動します。

## <a name="see-also"></a>参照

[給与統合 API の概要](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
