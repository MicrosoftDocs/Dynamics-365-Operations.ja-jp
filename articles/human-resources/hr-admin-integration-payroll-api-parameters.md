---
title: 給与統合のパラメーター
description: この記事では、Dynamics 365 Human Resources 給与統合のパラメーターについて説明します。
author: marcelbf
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-17
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7d784909fc8c5fa05557566b62b19802cd2acece
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896103"
---
# <a name="payroll-integration-parameters"></a>給与統合のパラメーター


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources 給与統合を使用する前に、この記事で説明するパラメーターを設定する必要があります。

## <a name="enable-payroll-address"></a>給与住所の有効化

給与住所を使用するには、給与統合タブの[共有パラメーター フォーム](hr-setup-shared-parameters.md) から給与住所を有効にする必要があります。

## <a name="define-the-identification-type"></a>識別タイプを定義する

[給与従業員エンティティ](hr-admin-integration-payroll-api-payroll-employee.md) の識別タイプ ID を公開するには、会社ごとに、[人事管理パラメーターのコンフィギュレーション](hr-setup-shared-parameters.md) を行う必要があります。

1. **報酬管理** ワークスペースのリンクの下にある **人事管理パラメーター** を選択します。 
2. **給与統合** タブで、次のフィールドの値を指定します。

| フィールド | 説明 |
| --- | --- |
| 給与処理で ID タイプを使用する | このオプションを選択すると、選択したタイプ ID が給与従業員エンティティに公開されます。 |
| ID タイプ | [給与従業員エンティティ](hr-admin-integration-payroll-api-payroll-employee.md) のフィールド **mshr_payrollemployeeentityid** で公開される識別タイプです。 |

## <a name="see-also"></a>参照

[給与統合 API の概要](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
