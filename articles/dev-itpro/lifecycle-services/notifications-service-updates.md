---
title: Lifecycle Services (LCS) でサービス更新プログラムに関する通知を受け取る
description: このトピックでは環境へのサービス更新プログラムについて通知を受けるさまざまな方法について説明します。
author: manalidongre
manager: AnnBe
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a4247da70ec3c24c9d735a2b7ef57dc7af73c8a0
ms.sourcegitcommit: 0bd0215d0735ed47b1b8af93a80bcdbf7ca2cc49
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/08/2019
ms.locfileid: "790309"
---
# <a name="get-notified-about-service-updates-through-lifecycle-services-lcs"></a>Lifecycle Services (LCS) でサービス更新プログラムに関する通知を受け取る

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/coming-soon.md)]

このトピックでは Microsoft からのサービス更新プログラムについて最新の状態に保つ方法を説明します。

Microsoft はサービス更新プログラムを使用して、構成されたサンドボックスおよび実稼働環境を最新のリリース バージョンに更新します。 Microsoft はお客様の環境に対する今後の更新プログラムについて、電子メールおよび Microsoft Dynamics Lifecycle Services (LCS) の通知でお知らせします。

受け取る通知の種類を次に示します:

- **更新の 5 日前に送信される通知:** Microsoft はお客様の環境を更新する 5 日前にユーザーに通知します。 更新頻度を構成した後で、更新が発生する 5 日前に次回の更新プログラムに関する通知を受け取ります。 これらの通知は 3 つのフォームを取ります:

    - **電子メール通知:** プロジェクト所有者、環境管理者、および追加で環境の関係者としてリストされているユーザーに、次回の更新について電子メールで通知されます。
    - **環境の詳細ページの通知バー:** LCS の環境の詳細ページに表示される通知は、次回の更新についてお客様に知らせます。
    - **更新を反映した今後の更新:** LCS の環境の詳細ページで **管理 &gt; 次回の更新** を選択し、今後の更新プログラムに関する詳細を含むダイアログ ボックスを開きます。

- **更新の 1 時間前に送信される通知:** ダウンタイム時間枠の開始 1 時間前に Microsoft Dynamics 365 for Finance and Operations のユーザーは通知を受け取ります。 この通知は、環境が更新で停止されるためユーザーに作業を保存するよう求めます。
- **更新が完了したときに送信される通知:** Microsoft が構成された環境の更新を完了すると、更新の結果について電子メールで通知されます。 更新が正常に適用されたかに関わらず、この電子メールは常に送信されます。 プロジェクト所有者、環境管理者、および環境の追加の関係者としてリストされているユーザーに送信されます。 Microsoft が何らかの理由で更新プログラムを開始できない場合、電子メールは更新プログラムが開始されなかった理由の説明を含みます。

通知を受け取った後で、何らかの理由により更新を続行できない場合は、一時停止することができます。 構成されたサンドボックス環境および実稼働環境への更新を一時停止する方法の詳細は、[Lifecycle Services (LCS) によるサービスの更新の一時停止](pause-service-updates.md) を参照してください。

1 つのバージョンおよび Microsoft が管理するサービスの更新の詳細は、[1 つのバージョンのサービス更新に関するよく寄せられる質問](../../fin-and-ops/get-started/one-version.md) を参照してください。