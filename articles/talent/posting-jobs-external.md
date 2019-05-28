---
title: Attract から外部キャリア サイトにジョブを転記
description: このトピックでは、外部採用サイトにジョブを転記するための Dynamics 365 for Talent - Attract の使用方法について説明します。
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518469"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a>Attract から外部キャリア サイトにジョブを転記

[!include [banner](../includes/banner.md)]

できるだけ多くの資格のある候補者の前で、空いている職位を獲得する必要があります。 Broadbean などの採用サイトは、この目標を達成するのに役立ちます。 Microsoft Dynamics 365 Talent: Attract では Broadbean にジョブを転記し、Microsoft がこの領域で新製品を常に提供できるようにします。

## <a name="post-jobs-to-broadbean"></a>Broadbean へのジョブの転記

Broadbean にジョブを転記する前に、Broadbean との統合をコンフィギュレーションする必要があります。

> [!NOTE]
> - 外部サイトへジョブを転記するには、[包括採用アドオン](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) が必要です。
> - 現在プレビューにある機能です。 試行する場合は、[Attract 管理者の設定で有効にする](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature) を実行します。

### <a name="configure-broadbean-integration"></a>Broadbean との統合をコンフィギュレーションする

1. Attract に管理者としてサインインします。
2. ページの右上隅にある**設定**ボタン (ギヤ記号) を選択して、**管理者センター**を選択します。
3. **職務ボードの設定**タブの **Broadbean との統合を有効にする**セクションで、統合を有効にします。
4. Broadbean に連絡し、**ユーザー名、クライアント ID、暗号化トークン**の情報を入力します。

> [!WARNING]
> Broadbean の資格情報は機密性が高いものです。 したがって、責任を持ってそれらを格納および共有します。 Attract の管理者ロールを持つすべてのユーザーは、これらの資格情報を表示できます。

> [!NOTE]
> Microsoft と Attract は、これらの値を作成し管理することには関与していません。 Attract でそれらを最新の状態に保ち、Broadbean と協力してユーザーの資格情報に関連する問題を解決するのはユーザー個人の責任となりす。

### <a name="post-a-job-to-broadbean"></a>Broadbean へのジョブの転記

Broadbean を有効にした後、採用担当者および管理者はジョブを転記できます。 職務の応募 URL が必要です。

1. Attract で、Broadbean に転記する職務を開きます。
2. **転記**セクションで、Broadbean に対応する**今すぐ転記**ボタンを選択します。
3. Broadbean ウィンドウの指示に従います。

Attract から Broadbean に渡される情報は次の通りです。

- 要求 ID
- 職位
- ジョブの説明
- 勤務地
- 応募 URL
- リクルーター情報

Broadbean が正常に転記を完了した後、Attract の**転記**セクションでは Broadbean のステータスが**転記済**として表示されます。

> [!NOTE]
> - Broadbean には**業界**フィールドが必要です。 現時点では、このフィールドは既定で **IT** に設定されています。 ただし、Broadbean ジョブ転記のウィンドウで適切な業界に値を変更できます。
> - Broadbean が、選択したすべての職務ボードにユーザーのジョブ転記を完了するまでには少し時間がかかります。 したがって、Attract では職務の状態更新を提供するまでに、わずかな遅れがある可能性があります。

### <a name="view-a-broadbean-job-posting"></a>Broadbean のジョブ転記を表示する

ジョブを Broadbean に転記した後は、Attract から表示できます。

1. Attract で、Broadbean で表示する職務を開きます。
2. **転記**セクションで、Broadbean に対応する省略記号ボタン (**...**) を選択し、**表示**を選択します。

Broadbean のジョブ転記は、新しいウィンドウに表示されます。

### <a name="update-a-broadbean-job-posting"></a>Broadbean のジョブ転記を更新する

Broadbean のジョブ転記は 2 通りの方法で更新できます。

1. Attract で、更新する職務を開きます。
2. **転記**セクションで、Broadbean に対応する**転記を更新**ボタンを選択します。
3. Broadbean ウィンドウで、転記を編集します。

- または -

1. Attract で、Broadbean で表示する職務を開きます。
2. **転記**セクションで、Broadbean に対応する省略記号ボタン (**...**) を選択し、**表示**を選択します。
3. Broadbean ウィンドウで職務の詳細を編集してから、ジョブを再転記します。 Attract では職務の詳細は変更されません。

### <a name="remove-a-broadbean-job-posting"></a>Broadbean のジョブ転記を削除する

必要に応じて Broadbean からジョブ転記を削除できます。

1. Attract で、削除する職務を開きます。
2. **転記**セクションで、Broadbean に対応する省略記号ボタン (**...**) を選択し、**転記を削除**を選択します。

Broadbean でジョブが削除された後、Attract の Broadbean 項目には**今すぐ転記**ボタンが表示されます。 このボタンが存在するということは、職務が削除されており、もう一度転記できることを示します。

### <a name="troubleshoot-the-broadbean-integration"></a>Broadbean との統合のトラブルシューティング

Broadbean にジョブを転記できない場合は、これらの手順を実行します。

1. Attract で入力した Broadbean の資格情報が有効で正しいことを確認します。
2. 資格情報が有効で正しい場合、[Broadbean サポート](https://www.broadbean.com/resources/support/) にお問い合わせください。
3. 問題が解消しない場合は、[Microsoft サポート](./talent-support.md) にお問い合わせください。
