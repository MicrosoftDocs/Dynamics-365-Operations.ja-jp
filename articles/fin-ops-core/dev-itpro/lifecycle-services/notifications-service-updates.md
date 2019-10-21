---
title: Lifecycle Services (LCS) でサービス更新プログラムに関する通知を受け取る
description: このトピックでは環境へのサービス更新プログラムについて通知を受けるさまざまな方法について説明します。
author: manalidongre
manager: AnnBe
ms.date: 07/02/2019
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
ms.openlocfilehash: 76c660ae5780cc15198a160b614432f61db2ed42
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183199"
---
# <a name="get-notified-about-service-updates-through-lifecycle-services-lcs"></a>Lifecycle Services (LCS) でサービス更新プログラムに関する通知を受け取る

[!include [banner](../includes/banner.md)]

このトピックでは Microsoft からのサービス更新プログラムについて最新の状態に保つ方法を説明します。

Microsoft はサービス更新プログラムを使用して、構成されたサンドボックスおよび実稼働環境を最新のリリース バージョンに更新します。 Microsoft はお客様の環境に対する今後の更新プログラムについて、電子メールおよび Microsoft Dynamics Lifecycle Services (LCS) の通知でお知らせします。

受け取る通知の種類を次に示します:

- **更新が利用可能になった際の通知:** 新しいリリースが一般公開されると、ご利用の実装しているプロジェクトのアクションセンターに Microsoft からの通知が表示されます。 Microsoft による自動更新がされる前に環境に更新を適用する場合は、その更新をプロジェクトのアセットライブラリに保存することができます。 Microsoftが自動更新を行うと、プロジェクトのアセットライブラリに更新のコピーが保存されます。 
- **更新の 5 日前に送信される通知:** Microsoft はお客様の環境を更新する 5 日前にユーザーに通知します。 更新頻度を構成した後で、更新が発生する 5 日前に次回の更新プログラムに関する通知を受け取ります。 これらの通知は 3 つのフォームを取ります:

    - **電子メール通知:** プロジェクト所有者、環境管理者、および追加で環境の関係者としてリストされているユーザーに、次回の更新について電子メールで通知されます。
    - **環境の詳細ページの通知バー:** LCS の環境の詳細ページに表示される通知は、次回の更新についてお客様に知らせます。
    - **更新を反映した今後の更新:** LCS の環境の詳細ページで **管理 &gt; 次回の更新** を選択し、今後の更新プログラムに関する詳細を含むダイアログ ボックスを開きます。

- **更新の 1 時間前に送信される通知:** ダウンタイム時間枠の開始 1 時間前にアプリケーションのユーザーは通知を受け取ります。 この通知は、環境が更新で停止されるためユーザーに作業を保存するよう求めます。
- **更新が完了したときに送信される通知:** Microsoft が構成された環境の更新を完了すると、更新の結果について電子メールで通知されます。 更新が正常に適用されたかに関わらず、この電子メールは常に送信されます。 プロジェクト所有者、環境管理者、および環境の追加の関係者としてリストされているユーザーに送信されます。 Microsoft が何らかの理由で更新プログラムを開始できない場合、電子メールは更新プログラムが開始されなかった理由の説明を含みます。

通知を受け取った後で、何らかの理由により更新を続行できない場合は、一時停止することができます。 構成されたサンドボックス環境および実稼働環境への更新を一時停止する方法の詳細は、[Lifecycle Services (LCS) によるサービスの更新の一時停止](pause-service-updates.md) を参照してください。

1 つのバージョンおよび Microsoft が管理するサービスの更新の詳細は、[1 つのバージョンのサービス更新に関するよく寄せられる質問](../../fin-and-ops/get-started/one-version.md) を参照してください。
