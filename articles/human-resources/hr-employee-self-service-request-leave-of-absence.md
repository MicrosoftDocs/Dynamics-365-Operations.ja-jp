---
title: 休暇を申請する
description: 休暇申請を提出します。
author: twheeloc
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveofAbsenceRequestEntry, EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e6c98246e94670dd5f882fcbbd1f269e57f66faf
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805290"
---
# <a name="request-a-leave-of-absence"></a>休暇を申請する

>[!Important]
>この記事で説明した機能は、現在スタンドアロンの Dynamics 365 Human Resources の顧客が利用できます。 Finance のリリース 10.0.26 以降に、Finance インフラストラクチャの今後のリリースで、一部またはすべての機能を使用できます。


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

休暇申請を提出すると、Dynamics 365 Human Resources で休暇申請の状態を確認できます。

## <a name="request-a-leave-of-absence"></a>休暇を申請する

1. **従業員セルフサービス** ワークスペースで、**休暇残日数** タイルの **詳細** (...) を選択します。

2. 休暇申請を提出するには、**休暇の申請** を選択します。

3. **休暇タイプ**、**開始日**、**終了日** に情報を入力します。

4. サポート ドキュメントを提出する必要がある場合、**添付ファイル** の中の **アップロード** を選択します。

5. 必要に応じて **コメント** に情報を入力します。

6. 申請を送信する準備ができたら、**送信** を選択します。 それ以外の場合は、**下書きの保存** を選択します。


## <a name="view-leave-of-absence-request-status"></a>休暇申請の状態の表示

1. **従業員セルフサービス** ワークスペースで、**休暇残日数** タイルの **詳細** (...) を選択します。

2. 休暇申請を表示するには、**休暇申請の表示** を選択します。

## <a name="update-a-leave-of-absence-request"></a>休暇申請の更新

1. **従業員セルフ サービス** ワークスペースで、**休暇** タイルの **詳細 (...)** を選択します。
2. 更新する休暇申請を選択し、**休暇の更新** を選択します。
3. **終了日** フィールドで、必要に応じて値を更新し、休暇を延長または短縮します。
4. 終了日を確認した場合は、**終了日の確認** オプション を **はい** に設定します。
5. **終了日の確認** オプションが **はい** に設定された後、職場復帰通知をアップロードできます。 次に、チェックボックスを選択して、職場復帰通知がアップロード済みであることを確認します。
6. **送信** を選択して、休暇申請を更新します。

## <a name="cancel-a-leave-of-absence-request"></a>休暇申請のキャンセル

1. **従業員セルフ サービス** ワークスペースで、**休暇** タイルの **詳細 (...)** を選択します。
2. キャンセルする休暇申請を選択し、**休暇の更新** を選択します。
3. **休暇のキャンセル** オプションを **はい** に設定します。
4. **送信** を選択して、休暇申請をキャンセルします。

## <a name="importing-leave-requests-from-other-systems-or-older-systems"></a>他のシステムまたは古いシステムからの休暇申請のインポート

別のシステムから休暇要求をインポートするには、通常のワークフローを実行して適切な休暇トランザクションを作成する必要があります。 また、休暇バンク トランザクションおよび完了した状態での休暇要求をインポートできます。 休暇要求のみをインポートする場合、休暇バンク トランザクションは自動的に作成されません。

## <a name="see-also"></a>参照

[休暇の中断](hr-leave-and-absence-suspend-leave.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
