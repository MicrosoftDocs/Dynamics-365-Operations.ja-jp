---
title: 休暇申請ワークフローの作成
description: 休暇および欠勤申請ワークフローを作成して、Dynamics 365 Human Resources で休暇申請を一貫して管理します。
author: andreabichsel
manager: AnnBe
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 209f0ec7236778cc0a828102e554b02206b45b73
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419310"
---
# <a name="create-a-leave-request-workflow"></a>休暇申請ワークフローの作成

Dynamics 365 Human Resources でワークフローを作成して、休暇および欠勤申請を一貫して管理します。 **休暇および欠勤** ワークフローでは、次の操作を行うことができます。

- タスクの定義
- タスクを完了すべきユーザーの決定
- 要求を承認または拒否できるユーザーの指定

## <a name="create-a-leave-and-absence-request-workflow"></a>休暇および欠勤申請ワークフローの作成

1. **休暇および欠勤** のページで、**リンク** タブを選択します。

2. **設定** で、**人事管理ワークフロー** を選択します。

3. **新規** を選択してから、**休暇及び欠勤申請** を選択します。 

4. **このファイルを開きますか ?** メッセージ ボックスが表示されたら、**開く** を選択して、会社の資格情報でサイン インします。

5. ワークフロー エディターを使用して、休暇申請のワークフローを作成します。 ワークフローの作成に関する詳細については、[ワークフローの作成の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.) を参照してください

## <a name="leave-and-absence-request-workflow-data-elements"></a>休暇および欠勤申請ワークフローの日付要素

次のデータ要素を使用して、休暇と欠勤の要求に対してワークフロー内で条件付の承認、または自動承認を作成することができます。

- **金額**
- **コメント**
- **法人**
- **作成者**
- **作成日時**
- **終了日**
- **休暇タイプ**
- **変更者**
- **変更日時**
- **理由コード**
- **申請 ID**
- **入社日**
- **ステータス** 
- **送信日**
- **送信者:**
- **人事による提出**
- **マネージャーによる提出**
- **次のユーザーの代理で提出**
- **ワーカー**
- **作業者タイプ**

これらの例では、次のデータ要素を使用してさまざまなタイプのワークフロー条件を作成する方法を示します：

- 条件付きステートメントで **理由コード** を使用して、理由コード **Surgery** を含む病欠の休暇申請を人事部に提出して承認を得る一方で、その他の理由コードはすべてマネージャーに提出します。 条件付きステートメントの詳細については、[ワークフローの条件付き決定の構成](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow) を参照してください。 

- 自動アクションで **人事担当者による提出** と **マネージャーによる提出** を使用して、これらの役割が従業員に代わって提出する休暇申請を自動的に承認します。 自動アクションの詳細については、[ワークフローでの承認プロセスの構成](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow) を参照してください。

- 条件文または自動アクションで **休暇タイプ** を使用して、特定の休暇タイプの申請をワークフローでどのようにルーティングするかを制御します。

## <a name="see-also"></a>参照

- [休暇の概要](hr-leave-and-absence-overview.md)
