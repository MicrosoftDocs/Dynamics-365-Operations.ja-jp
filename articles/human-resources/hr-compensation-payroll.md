---
title: 支払準備完了
description: このトピックでは、Dynamics 365 Human Resources で従業員に支払準備完了をマークする方法を説明します。
author: marcelbf
ms.date: 07/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f9aa9e60b51b1801c07981ad120cb77f65fee286
ms.sourcegitcommit: baad2723291774f610324a8054fc14abf3287fe1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/14/2021
ms.locfileid: "6560115"
---
# <a name="ready-to-pay"></a>支払準備完了

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

> [!NOTE]
> 従業員に支払準備完了をマークしたい場合は、まず機能管理で **(プレビュー) 給与統合** 機能を有効にする必要があります。 プレビュー機能を有効にする方法については、[機能の管理](hr-admin-manage-features.md)を参照してください。

この機能により、人事担当者は、給与処理の準備が整っている従業員と、サード パーティの給与計算プロバイダーによって使用される前にアクションが必要な従業員とを理解することができます。

## <a name="mark-employee-as-ready-to-pay"></a>従業員に支払準備完了をマークする

従業員情報を収集して検証することは時間がかかり、エラーも発生しやすくなります。 Dynamics 365 Human Resources は、人事担当者が従業員情報を確認し、簡単に更新できる方法を提供することで、給与処理の準備にかかる時間を削減するのに役立ちます。

従業員に支払準備完了をマークするには:

1. **報酬管理** を開く。 ワークスペースには 2 つのタイルがあります 
    - **支払準備ができている従業員**
    - **支払準備が完了していない従業員**
    ![報酬管理ワークスペース。](./media/hr-ready-to-pay-1-workspace.png)

2. **支払準備が完了していない従業員** を選択します。

3. 検証する従業員を選択します。 **給与タブ** の **支払準備完了** グループで、**検証** を選択します。
    ![従業員を検証する。](./media/hr-ready-to-pay-2-validate.png)

4. 結果を確認するには、**給与タブ** の **支払準備完了** グループで、**結果** を選択します。

## <a name="validation"></a>検証

従業員に支払準備完了をマークする前に、システムがプロファイルの完全性の基本的な検証を実行します。

![結果を検証する。](./media/hr-ready-to-pay-3-results.png)

以下の表で、実行されるそれぞれのアクションに関する詳細を提供します。 

| 検証 | 細目 |
| --- | --- |
| 住所の目的パラメーター | **給与住所の目的を使用** パラメーターがオンになっているかどうかを検証します。 |
| 給与住所 | 作業者のプロファイルに"給与居住の場所"または"給与作業の場所"のいずれかを目的とする住所が少なくとも 1 つあり、1 つの目的につき 1 つの住所であるかどうかを検証します。 |
| 雇用 | 従業員が少なくとも 1 つの雇用 (現在、過去、将来) があるかどうかを確認します。 |
| ID 番号 | パラメーター"給与処理で ID タイプを使用"が"はい"であり、パラメーターに指定されている ID タイプが作業者プロファイルに入力されているかどうかを検証します。 |
| 氏名 | **名** と **姓** が入力されているかどうか確認し、作業者プロファイルが有効かどうかを検証します。|
| ポジション番号 | 作業者に職位が割り当てられているかどうかを確認します。 |
| 生年月日 | 名と姓が入力されているかどうか確認し、作業者プロファイルに **誕生日** が入力されているかどうかを検証します。 |
| 報酬 | 作業者が固定報酬プランに登録されているかどうかを確認します。 |

これらの検証のうち 1 つが失敗した場合は、従業員を支払準備完了としてマークすることはできません。

**支払準備完了** フィールドが **いいえ** の場合、作業者プロファイルを完全にするためにアクションを実行する必要があることを示します。 これによって、どのデータ エンティティへのデータ公開も停止されることはありません。 

## <a name="known-issues"></a>既知の問題

- 機能管理の **合理化された従業員の入力** 機能を無効にする必要があります。 この機能を使用すると、報酬管理ワークスペースのタイルは正常に機能しません。
- 作業者フォームの **給与タブ** と **支払準備完了** グループは、任意のユーザー ロールで使用できます。 

## <a name="see-also"></a>参照

[給与統合 API の概要](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
