---
title: LinkedIn と Microsoft Dynamics 365 Talent - Attract との統合のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Talent - Attract から LinkedIn に職務を転記する際の問題をトラブルシューティングする方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
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
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: b031fd95d2e7fc8405ad96139779091e00bb4d46
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551475"
---
# <a name="troubleshoot-integration-with-linkedin-and-microsoft-dynamics-365-talent---attract"></a>LinkedIn と Microsoft Dynamics 365 Talent - Attract との統合のトラブルシューティング

[!include [banner](../includes/banner.md)]

次の情報は、Microsoft Dynamics 365 Talent: Attract から LinkedIn に職務を転記する際に発生する可能性のある問題のトラブルシューティングに役立ちます。

## <a name="you-cant-sign-in-to-linkedin-from-attract"></a>Attract から LinkedIn にサイン インできない

Attract から LinkedIn にサイン インできない場合は、次の手順をお試しください。

1. Attract で入力した LinkedIn の資格情報が有効で正しいことを確認します。
2. 資格情報が有効で正しい場合、[LinkedIn サポート](https://www.linkedin.com/help/linkedin) にお問い合わせください。
3. 問題が解消しない場合は、[Microsoft サポート](./talent-support.md) にお問い合わせください。

## <a name="job-posts-from-attract-dont-appear-on-linkedin"></a>Attract からの職務の転記が LinkedIn に表示されない

24 時間経過後も LinkedIn に職務が表示されていない場合は、次の手順をお試しください。

1. LinkedIn 会社 ID が LinkedIn 会社ページにマップされ、Attract 管理センターに正しく入力されていることを確認します。 管理センターで LinkedIn 設定を変更する方法の詳細については、[LinkedIn との統合を設定する](attract-admin-linkedin.md) を参照してください。 LinkedIn 会社 ID の詳細については、[Linkedln 会社 ID を Linkedln 職務ボードに関連付ける - よく寄せられる質問](https://www.linkedin.com/help/linkedin/answer/98972) を参照してください。
2. LinkedIn の職務の詳細を確認して、アドレスが完全であることを確認します。 LinkedIn が職務を正常に転記するには、少なくともその職務の都市と国または地域が必要です。
3. 職務が LinkedIn に転記されている別の職務と重複していないことを確認します。 LinkedInは、LinkedIn プレミアム ジョブ スロットまたは別のソースからの限定付き一覧のいずれかと重複する職務を投稿しません。 会社の別のユーザーが、まだ手動で職務を転記していないことを確認します。

## <a name="see-also"></a>参照

[LinkedIn に関するよく寄せられる質問](./attract-linkedin-faq.md)

[Attract から LinkedIn への職務の投稿](./attract-post-jobs-to-linkedin.md)

[LinkedIn Recruiter での候補者のソーシング](./attract-linkedin-recruiter.md)

[職務の作成](./creating-jobs-attract.md)

[LinkedIn との統合のトラブルシューティング](./attract-troubleshoot-linkedin.md)
