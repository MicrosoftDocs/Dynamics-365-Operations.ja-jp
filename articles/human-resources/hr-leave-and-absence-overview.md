---
title: 概要
description: Dynamics 365 Human Resources では、休暇および欠勤のワークスペースは、新しい休暇計画を作成するための柔軟なフレームワーク、休暇申請を管理するためのワークフロー、および従業者が休暇を申請するための直観的なセルフ サービス ページを提供します。
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
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
ms.openlocfilehash: ec72d2d741f7f8428a7daa97bb982e9fc00b8c3f
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428970"
---
# <a name="overview"></a>概要

Dynamics 365 Human Resources は、従業員に休暇による大きな益を与える助けになります。 **休暇**ワークスペースは、新しい休暇計画を作成するための柔軟なフレームワーク、休暇申請を管理するためのワークフロー、および従業員が休暇を申請するための直感的なセルフ サービス ページを提供します。 分析では、組織が休暇残日数および休暇計画の用途を測定および監視するのに役立ちます。

## <a name="set-up-leave-and-absence"></a>休暇の設定

従業員の休暇計画を作成する前に、いくつかの設定手順を行う必要があります。

- [休暇パラメーターのコンフィギュレーション](hr-leave-and-absence-parameters.md)
- [作業時間カレンダーの作成](hr-leave-and-absence-working-time-calendar.md)
- [休暇申請ワークフローの作成](hr-leave-and-absence-workflow.md)

## <a name="create-and-manage-leave-plans"></a>休暇計画を作成および管理する

作業者の休暇計画を作成する前に、休暇タイプを作成する必要があります。 休暇計画を作成して初めて、休暇計画に作業者を登録できます。 また、累積処理の実行や、警告の作成、計画の分析の表示をすることもできます。

- [休暇タイプのコンフィギュレーション](hr-leave-and-absence-types.md)
- [休暇計画の作成](hr-leave-and-absence-plans.md)
- [休暇計画への作業者の割り当て](hr-leave-and-absence-enroll.md)
- [休暇計画の累計](hr-leave-and-absence-accrue.md)
- [休暇の分析の表示](hr-leave-and-absence-analytics.md)

## <a name="request-time-off-and-manage-requests"></a>休暇の申請と申請の管理

**従業員セルフ サービス** ワークスペースで、従業員が休暇申請を送信したり、組織がその申請を管理することができます。

- [休暇申請](hr-employee-self-service-request-time-off.md)
- [休暇および欠勤要求の管理](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-known-issues"></a>休暇と欠勤の既知の問題

### <a name="rounding-precision"></a>丸め精度

**丸めのタイプ** を設定する場合、**丸め精度** を設定することはできません。 **丸め精度** は、**休暇および欠勤タイプ** エンティティを使用してのみ設定できます。 

1. **休暇および欠勤タイプ** から、**Excel で開く** を選択して、**休暇および欠勤タイプ** エンティティを開きます。

2. ファイルが開いて有効になったら、**デザイン** を選択します。

3. **休暇および欠勤タイプ** テーブルで、鉛筆オプションを選択して編集します。

4. **丸め精度** と **丸めのタイプ**を選択し、**追加** を選択して、フィールドの一覧に追加します。

5. **更新** を選択し、**完了** を選択します。

6. 休暇タイプまだが設定されていない場合は、休暇タイプごとに **丸めのタイプ** を入力または選択します。 

7. 適切なタイプの **丸め精度** を入力します。

8. **公開** を選択して、変更を Human Resources にプッシュします。

## <a name="leave-and-absence-preview-features"></a>休暇のプレビュー機能

**サンドボックス**環境では、新しい休暇のプレビュー機能を試してみることができます。 プレビュー機能をオンにする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。 

[!include [banner](includes/preview-feature.md)]

プレビュー機能は次のとおりです。

- **会社またはプラン別の有給休暇付与** - すべての会社または単一の会社のいずれかで有給休暇付与プロセスを実行することができます。 特定の会社の特定の休暇および不就業プランについて、有給休暇付与プロセスを実行することもできます。 

- **休暇の購入**: 従業員が購入申請を提出するために休暇ポリシーの購入を有効にして作成できます。 従業員は、購入申請を提出し、申請を反映するように残高を自動的に更新できます。  

- **承認済の休暇申請に添付ファイルを追加する** - 既に承認されている休暇申請に対して添付ファイルを追加することができます。 

