---
title: 無期限休暇の作成
description: この記事では、Microsoft Dynamics 365 Human Resources での無期限休暇の作成方法について説明します。
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 08231d4139209387c3c76923fafdd2061fceb280
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805342"
---
# <a name="create-an-open-ended-leave-of-absence"></a>無期限休暇の作成

> [!IMPORTANT]
> この記事で説明する機能は、Microsoft Dynamics 365 Finance のリリース 10.0.31 以降に今後のリリースの一部として、Finance インフラストラクチャで使用可能になります。

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

無期限の休暇申請を提出すると、Dynamics 365 Human Resources で休暇申請の状態を表示できます。

## <a name="prerequisites"></a>必要条件

1. **機能管理** で、**無期限の休暇** 機能が有効であることを確認します。

    > [!IMPORTANT]
    > オンにした後は、この機能をオフにすることはできません。

2. 休暇の休暇タイプを作成します。
3. 休暇タイプ、説明、ワークフロー ID などの詳細を入力します。
4. **申請タイプ** フィールドで、**休暇** を選択します。
5. 詳細セクションで無期限の休暇の場合は、**無期限** オプションを **はい** に設定します。
6. **職場復帰通知** オプションを **はい** または **いいえ** に設定します。
7. 無期限の休暇申請には、オプションで職場復帰通知を要求することができます。

> [!NOTE]
> この機能を有効にすると、**必要な添付ファイル** 機能が有効になります。

## <a name="request-an-open-ended-leave-of-absence"></a>無期限休暇の申請

1. **従業員セルフ サービス** ワークスペースで、**休暇の残余** タイルの **詳細 (...)** を選択します。
2. 休暇申請を提出するには、**休暇申請** を選択します。
3. **休暇タイプ** と **開始日** フィールドに情報を入力します。 **終了日** フィールドに仮の終了日を入力します。
4. サポート ドキュメントの提出が必要な場合、**添付ファイル** で **アップロード** を選択します。
5. 申請を送信する準備ができたら、**送信** を選択します。 それ以外の場合は、**下書きの保存** を選択します。
6. 無期限の休暇申請を更新するには、申請を選択し、**終了日** フィールドに終了日を入力し、**終了日の確認** オプションを **はい** に設定して、ドキュメントをアップロードします。
7. **職場復帰通知** オプションが **はい** に設定されている場合は、**アップロード** を選択してチェックボックスを選択し、有効な職場復帰通知がアップロード済みであることを確認します。
8. すべての詳細が入力された後、**送信** を選択します。
