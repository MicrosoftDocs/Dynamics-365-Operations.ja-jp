---
title: Attract から Broadbean への職務の投稿
description: このトピックでは、Dynamics 365 Talent - Attract を使用して Broadbean に職務を転記する方法について説明します。
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
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
ms.openlocfilehash: 41fa057606887069a9ea0f1f2178eeaff59f33ca
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461801"
---
# <a name="post-jobs-to-broadbean-from-attract"></a>Attract から Broadbean への職務の投稿

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Attract は、Attract から Broadbean にジョブを直接転記させることにより、必要な人材を獲得するのに役立ちます。 [ジョブを作成](./creating-jobs-attract.md) した後、Broadbean 上で可能性のあるすべてのジョブ候補の前にジョブを配置するには、ボタンをクリックするのみです。

Broadbean にジョブを転記するには、適切な Broadbean のライセンスが必要です。 Broadbean はさまざまな製品やプランを提供しています。 Broadbean ライセンスと価格に関する詳細情報については、[Broadbean にお問い合わせください](https://www.broadbean.com/contact-us/)。

管理者として、Broadbean と Attract の統合を構成する方法の詳細が必要な場合は、[Microsoft Dynamics 365 Talent - Attract での、Broadbean との統合の設定](./attract-admin-job-board-settings.md) を参照してください。

## <a name="post-jobs-to-broadbean"></a>Broadbean への職務の投稿

Broadbean を有効にした後、採用担当者および管理者はジョブを転記できます。 職務の応募 URL が必要です。

1. Attract で、Broadbean に転記する職務を開きます。
2. **転記** セクションで、Broadbean に対応する **今すぐ転記** ボタンを選択します。
3. Broadbean ウィンドウの指示に従います。

Attract から Broadbean に渡される情報は次の通りです。

- 要求 ID
- 職位
- ジョブの説明
- 勤務地
- 応募 URL
- リクルーター情報

Broadbean が正常に転記を完了した後、Attract の **転記** セクションでは Broadbean のステータスが **転記済** として表示されます。

> [!NOTE]
> - Broadbean には **業界** フィールドが必要です。 現時点では、このフィールドは既定で **IT** に設定されています。 ただし、Broadbean ジョブ転記のウィンドウで適切な業界に値を変更できます。
> - Broadbean が、選択したすべての職務ボードにユーザーのジョブ転記を完了するまでには少し時間がかかります。 したがって、Attract では職務の状態更新を提供するまでに、わずかな遅れがある可能性があります。

### <a name="view-a-broadbean-job-posting"></a>Broadbean のジョブ転記を表示する

ジョブを Broadbean に転記した後は、Attract から表示できます。

1. Attract で、Broadbean で表示する職務を開きます。
2. **転記** タブで、Broadbean に対応する省略記号ボタン (**...**) を選択し、**表示** を選択します。

Broadbean のジョブ転記は、新しいウィンドウに表示されます。

### <a name="update-a-broadbean-job-posting"></a>Broadbean のジョブ転記を更新する

Broadbean のジョブ転記は 2 通りの方法で更新できます。

1. Attract で、更新する職務を開きます。
2. **転記** セクションで、Broadbean に対応する **転記を更新** ボタンを選択します。
3. Broadbean ウィンドウで、転記を編集します。

    - または -

1. Attract で、Broadbean で表示する職務を開きます。
2. **転記** セクションで、Broadbean に対応する省略記号ボタン (**...**) を選択し、**表示** を選択します。
3. Broadbean ウィンドウで職務の詳細を編集してから、ジョブを再転記します。 Attract では職務の詳細は変更されません。

### <a name="remove-a-broadbean-job-posting"></a>Broadbean のジョブ転記を削除する

必要に応じて Broadbean からジョブ転記を削除できます。

1. Attract で、削除する職務を開きます。
2. **転記** セクションで、Broadbean に対応する省略記号ボタン (**...**) を選択し、**転記を削除** を選択します。

Broadbean でジョブが削除された後、Attract の Broadbean 項目には **今すぐ転記** ボタンが表示されます。 このボタンが存在するということは、職務が削除されており、もう一度転記できることを示します。

### <a name="troubleshoot-job-posting-to-broadbean"></a>Broadbean へのジョブ転記のトラブルシューティング

Broadbean にジョブを転記できない場合は、これらの手順を実行します。

1. Attract で入力した Broadbean の資格情報が有効で正しいことを確認します。
2. 資格情報が有効で正しい場合、[Broadbean サポート](https://www.broadbean.com/resources/support/) にお問い合わせください。
3. 問題が解消しない場合は、[Microsoft サポート](./talent-support.md) にお問い合わせください。

## <a name="see-also"></a>参照

[Attract でジョブ求人の作成、承認、および投稿](./creating-jobs-attract.md)

[Microsoft Dynamics 365 Talent - Attract における Broadbean 統合の有効化](./attract-admin-job-board-settings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]