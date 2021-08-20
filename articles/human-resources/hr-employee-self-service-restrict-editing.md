---
title: 個人情報の編集の制限
description: Dynamics 365 Human Resources で連絡先情報を編集する従業員を制限します。
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 87977ff004e0785ec1d31fe3abac2728f87e7083348895b58e58f46cd3e79925
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748886"
---
# <a name="restrict-editing-of-personal-information"></a>個人情報の編集の制限

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

このトピックでは、Dynamics 365 Human Resources で従業員が連絡先情報を編集するのを制限する方法について説明します 。 従業員が、ビジネスの場所や電子メール アドレスなど、特定の連絡先情報を編集できないようにすることができます。

> [!NOTE]
> この機能を使用するには、まず機能管理で **(プレビュー) 従業員が特定の目的で住所や連絡先情報の追加または編集を制限する** を有効にする必要があります。 プレビュー機能を有効にする方法については、[機能の管理](hr-admin-manage-features.md)を参照してください。<br><br>![プレビュー機能を有効にする。](./media/hr-employee-self-service-restrict-enable.png)

## <a name="choose-the-information-an-employee-can-add-or-edit"></a>従業員が追加または編集できる情報の選択

1. Human Resources では、**人事管理** を選択し、**リンク** を選択して、**人事管理パラメーター** を選択します。

   ![人事管理パラメーターに移動する。](./media/hr-employee-self-service-human-resources-parameters.png)

2. **人事管理パラメーター** ページで、**従業員セルフ サービス** タブを選択します。

   ![従業員セルフ サービス を選択します。](./media/hr-employee-self-service-tab.png)

3. **従業員セルフ サービス** タブで、従業員に追加または編集してほしくない **住所と連絡先情報** セクションのすべての情報をオフにします。 この例では、**ビジネス** の連絡先情報をオフにしました。

   ![ビジネスの連絡先情報の編集の制限。](./media/hr-employee-self-service-restrict-business.png)

4. **保存** を選択します。

   ![変更の保存。](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a>従業員エクスペリエンス

従業員が連絡先情報を追加または編集するのを制限した後、従業員は情報を表示できますが、変更はできません。

この例では、従業員が **ビジネス** の連絡先情報を編集するのを制限されている場合でも、従業員セルフ サービスの情報を表示できます。

![ビジネスの連絡先情報の表示。](./media/hr-employee-self-service-restrict-view.png)

ただし、従業員がビジネスの連絡先情報を選択すると、**住所の編集** ウィンドウは読み取り専用として表示され、フィールドを一切変更できません。

![ビジネスの連絡先情報は読み取り専用として表示。](./media/hr-employee-self-service-restrict-read-only.png)

さらに、**追加** を選択して新しい住所を追加した場合、**目的** のドロップダウン ボックスから **ビジネス** を選択することはできません。

![従業員がビジネス住所を追加できない。](./media/hr-employee-self-service-restrict-add.png)

**連絡先情報** ページで **個人情報** を選択し、新しい住所を追加すると、従業員は同じ体験をします。 **目的** のドロップダウン ボックスには、追加できる情報の種類のみが表示されます。 

![従業員は目的のドロップダウンでビジネスを選択できない。](./media/hr-employee-self-service-restrict-purpose.png)

**連絡先情報** では、 グリッドに **目的** が表示されます。

![連絡先情報グリッドに目的が表示される。](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a>参照

[従業員およびマネージャー セルフ サービスの概要](hr-employee-manager-self-service-overview.md)<br>
[Human Resources パラメーターのコンフィギュレーション](hr-setup-parameters.md)<br>
[個人情報の編集](hr-employee-manager-self-service-edit-personal-information.md)