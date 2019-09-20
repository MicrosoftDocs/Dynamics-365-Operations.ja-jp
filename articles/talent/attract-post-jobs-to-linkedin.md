---
title: Microsoft Dynamics 365 for Talent - Attract から LinkedIn への職務の転記
description: このトピックでは、Dynamics 365 for Talent - Attract を使用して LinkedIn に職務を転記する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
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
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: f2109f5e90321598eb2317140eef6bcd86ab82f5
ms.sourcegitcommit: c62756cb04549b2ff5de9b93d497e964a340335a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/17/2019
ms.locfileid: "1756179"
---
# <a name="post-jobs-to-linkedin"></a>LinkedIn への職務の投稿

[!include [banner](../includes/banner.md)]

LinkedIn は最大のオンライン プロフェッショナル ネットワークで、世界の最高の人材へのアクセスを提供します。 Microsoft Dynamics 365 for Talent: Attract では、Attract から LinkedIn に職務を直接転記できるため、必要な人材を獲得するのに役立ちます。

Attract を使用すると、追加料金なしで LinkedIn に制限付き一覧を転記できます。 これらの一覧は、Attract などの LinkedIn ソフトウェア パートナーを通じてのみ利用可能です。 会社の LinkedIn ページの**キャリア** パネルには有料の一覧しか表示されないため、この一覧は表示されません。 ただし、潜在的な候補者が使用可能なすべての職務を表示する際には表示されます。 制限付き一覧は、LinkedIn の職務検索でも表示されます。

Attract で[職務を作成](./creating-jobs-attract.md) した後は、ボタンを選択するだけで LinkedIn 上の何千もの潜在的な候補者の前に職務を配置することができます。

次の表に、ユーザー ロールに応じて LinkedIn で実行できるアクションを示します。

| 役割 | 実行できるアクション |
|---|---|
| 管理者 | 転記、再転記、および転記の削除 |
| 採用マネージャー | 読み取り専用 |
| 採用担当者 | 転記、再転記、および転記の削除 |
| 面接者 | アクセス許可なし |
| 読み取り専用 | 読み取り専用 |

Attract でのユーザー ロールの詳細については、[Attract でのセキュリティおよびロールの管理](./security-attract.md) を参照してください。

管理者として、LinkedIn と Attract の統合を構成する方法の詳細が必要な場合は、[LinkedIn との統合の設定](./attract-admin-linkedin.md) を参照してください。

LinkedIn に転記された職務は、ライブ LinkedIn サイトに表示されます。 LinkedIn には職務を転記するためのテスト環境はありません。 したがって、テスト ジョブを誤って転記しないように注意してください。

## <a name="post-jobs-to-linkedin"></a>LinkedIn への職務の投稿

1. Attract で、LinkedIn に転記する職務を開きます。
2. **転記**タブで、LinkedIn に対応する**今すぐ転記**ボタンを選択します。

    [![Attract から LinkedIn への職務の投稿](./media/attract-post-job-to-linkedin.png)](./media/attract-post-job-to-linkedin.png)

3. **"今すぐ応募" Web アドレスの作成**ダイアログ ボックスで、**候補者は次の URL を使用して応募できます**の下にあるオプションを選択します。 **Attract 内のリンク**を選択することをお勧めします。
4. **完了** を選択します。
5. **転記を送信**メッセージ ボックスで、**確認**を選択します。

LinkedIn が正常に転記を完了した後、Attract の**転記**セクションでは LinkedIn のステータスが**転記済**として表示されます。 職務が LinkedIn に表示されるまでに、最大 48 時間かかることがあります。

興味のある候補者が一覧の横にある**表示**を選択すると、職務の詳細と応募方法に関する情報が表示されます。

Attract を介したすべての職務の転記は、制限付き一覧です。 LinkedIn での制限付き一覧の詳細については、[求人ラッピングにおける制限付き一覧対プレミアム ジョブ スロット](https://www.linkedin.com/help/recruiter/answer/79049) を参照してください。

LinkedIn への職務転記に問題がある場合は、[Linkedln への職務転記のトラブルシューティング](./attract-troubleshoot-linkedin.md) を参照してください。

## <a name="see-also"></a>参照

[LinkedIn に関するよく寄せられる質問](./attract-linkedin-faq.md)

[LinkedIn との統合の設定](./attract-admin-linkedin.md)

[職務の作成](./creating-jobs-attract.md)

[LinkedIn Recruiter での候補者のソーシング](./attract-linkedin-recruiter.md)

[LinkedIn との統合のトラブルシューティング](./attract-troubleshoot-linkedin.md)
