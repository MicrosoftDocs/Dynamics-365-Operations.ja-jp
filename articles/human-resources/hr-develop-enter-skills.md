---
title: スキルの入力
description: 作業者とマネージャは、Dynamics 365 Human Resources でスキルを入力できます。
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: b24d37292a2e9749fb2fde06b9f03fcd13db0bbe
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076602"
---
# <a name="enter-skills"></a>スキルの入力

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resourcesでは、作業者、申請者、連絡担当者の目標スキルまたは実際のスキルを入力できます。 目標スキルとは、その従業員が達成を計画しているスキルです。 実際のスキルとは、従業員が現在持っているスキルです。

## <a name="create-a-workflow-to-auto-approve-skills"></a>スキルの自動承認のワークフローの作成

承認を必要としないスキル入力を設定するには、スキルを自動承認するワークフローを作成する必要があります。

> [!NOTE]
> 作業者が入力するスキルには、常に管理者の承認が必要となります。 このワークフローでは、従業員の代理としてマネージャが入力したスキルの自動承認のみ行います。

1. **人事管理** ワークスペースで、**リンク** を選択します。

2. **設定** で、**人事管理ワークフロー** を選択します。

3. **新規** を選択します。

4. **ワークフローの作成** ウィンドウで、**作業者のスキル** を選択します。

   [![作業者のスキル ワークフローの選択](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)

5. **このファイル を開きますか？** というダイアログで、**開く** を選択します。 メッセージが表示されたら、 資格情報を入力します。

6. ワークフロー エディタで、**スキルの承認** ワークフローの要素を 選択し、その要素をドラッグします。

   [![スキルの承認ワークフロー要素の選択](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)

7. **開始** 要素を **スキル 1 の承認** 要素に関連付け、**スキル1の承認** 要素を **終了** に関連付けます。 **終了** 要素を表示するには、下部までスクロールする必要があるかもしれません。 他の要素の近くまでドラッグできます。

   [![ワークフロー要素の関連付け](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)

8. **スキル 1 の承認** ワークフロー要素をダブルクリックし、**手順 1** の要素を右クリックします。 **ステップ 1** の要素を右クリックし、**プロパティ** を選択します。

9. **プロパティ** ウィンドウで、左側のナビゲーション バーで **条件** を選択します。

10. **次の条件が満たされた場合にのみこのステップを実行** を選択します。

11. **条件の追加** を選択します。 **場所** の後で、**従業員セルフサービス スキル** を選択し、**従業員セルフサービス skills.Person** を選択します。 **である** の後に、**フィールド** を選択し、**ユーザーと相手方の relationship.Person** を選択します。

    [![ 条件の指定](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)

12. 左側のナビゲーション バーで **割り当て** を選択します。

13. **割り当てタイプ** タブで、**階層** を選択します。

14. **階層タイプ:** フィールドの **階層の選択** タブで、**管理者階層** を選択します 。

    [![管理階層の指定](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)

15. **閉じる** を選択し、パンくずキャンバスで **ワークフロー** を選択し、**保存して終了** を選択します。

ワークフロー作成の詳細については、[ワークフロー システムの概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system?toc=/dynamics365/human-resources/toc.json) を参照してください。

## <a name="enter-skills-for-a-worker"></a>作業者のスキルの入力

1. 作業者を選択します。

2. **作業者** ページのアクション バー で 、**人物** を選択し、**スキル** を選択します。

3. **スキル** ページ で、各スキルについて次のフィールドに情報を入力します:

   - **スキル** : スキルを選択します。
   - **レベル タイプ**: 作業者が既に持っているスキルの **実績** を選択するか、作業者が取り組むスキルの **目標** を選択します。
   - **レベル**: 作業者のスキルのレベルを選択します。
   - **レベルの日付け**: 日付を選択するには、カレンダーの日付をクリックします。
   - **査定者**: 該当する場合は、一覧から査定者を選択します。 検索にはフィルターを適用できます。
   - **経験年数** : 経験年数を入力します。
   - **検証済**: スキルが検証された場合は、このチェック ボックスをオンにします。
   - **検証者**: 検証者の名前を入力します。

4. スキルの入力が完了したら、**保存** を選択します。

## <a name="see-also"></a>参照

[スキルの構成](hr-develop-skills.md)<br>
[スキルのマップ](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]