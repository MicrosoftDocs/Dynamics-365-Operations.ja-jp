---
title: 実装プロジェクトの研修
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用してプロジェクトをオンボードする方法を説明します。
author: ClaudiaBetz-Haubold
manager: AnnBe
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: chaubold
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 2876a1208c855899b5d2e38d448649fc611dffc1
ms.sourcegitcommit: f52ddcad105aac4ad2caef709751ff80caf363c0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036942"
---
# <a name="onboard-an-implementation-project"></a>実装プロジェクトの研修

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して Finance and Operations プロジェクトをオンボードする方法を説明します。

## <a name="microsoft-365-admin-center"></a>Microsoft 365 管理ビュー

組織が Finance and Operations のサブスクリプションを購入したら、テナント管理者は、組織の Azure Active Directory (Azure AD) テナントを有効にし、次の手順を完了する必要があります。

1. Inprivate/Incognito ブラウズセッションを開いて、[Microsoft 365 管理センター](https://admin.microsoft.com/)に移動します。
2. テナント管理者の資格情報を使用してログインします。
3. **請求 > 製品 & サービス**に移動して、配置するアプリケーションに対して有効なサブスクリプションがあることを確認します。 
   > [!NOTE]
   > 有効なサブスクリプションが表示されない場合は、ライセンス パートナーに問い合わせて、サブスクリプション トランザクションの状態と、サブスクリプションのテナントを確認してください。 既定では、すべてのMicrosoftオンラインサービスが同じAzure ADテナント上で実行されている必要があります。
4. 問題のサブスクリプションが有効と表示されている場合は、LCS にサインインして実装のプロジェクト作成フローをトリガーすることにより、次のステップに進むことができます。
5. 別のプライベートブラウザータブを開き、[Lifecycle Services](https://lcs.dynamics.com)に移動します。 現在のテナント管理者の資格情報を使用してアクセスするには、**ログイン** を選択します。
6. 実装プロジェクトのプロビジョニングを完了するために、他の表示されたメッセージを承認して確認します。
7. テナント管理者には、プロビジョニングされた実装プロジェクトのプロジェクト所有者セキュリティ ロールが割り当てられます。  
   > [!NOTE]
   > テナント管理者が実装に参加していない場合は、少なくとも 1 人の追加のプロジェクト所有者を実装プロジェクトに割り当てる必要があります。

   ユーザーに割り当てることができるセキュリティ ロールを含む、LCS ユーザー管理の概要については、 [Lifecycle Services (LCS) のセキュリティのコンフィギュレーション](../../dev-itpro/lifecycle-services/configure-lcs-security.md#configuring-project-security) を参照してください。

## <a name="lcs-implementation-project-workspace"></a>LCS 実装プロジェクト ワークスペース

テナント管理者が Finance and Operations サブスクリプションの有効化を完了し、適切なプロジェクト所有者を追加した後、チーム メンバーは **実装プロジェクト** ワークスペースにアクセスできます。

LCS で完了する最初の手順は、**プロジェクトのオンボード**です。 この手順は、Microsoft が管理するすべての環境を展開する前に、**2019 年 8 月 22 日 (PST) またはそれ以降**に作成されたすべての LCS 実装プロジェクトに必要です。 **プロジェクトのオンボード**機能には、アクション センターの通知または LCS 実装プロジェクト メニューを使用してアクセスできます。 LCS の**プロジェクト オンボード**にアクセスするには、プロジェクト所有者セキュリティ ロールに割り当てられている必要があります。

LCS を開始するには、[Finance and Operations アプリ顧客用の Lifecycle Services (LCS)](../../dev-itpro/lifecycle-services/lcs-works-lcs.md) を参照してください。 

## <a name="fasttrack-onboarding-services"></a>FastTrack オンボード サービス

LCS  **実装プロジェクト** ワークスペースがプロビジョニングされたら、Microsoft FastTrack チームはオンボードの進捗状況を監視します。 FastTrack プログラムおよび提供されるサービスの詳細については、 [Microsoft FastTrack](../get-started/fasttrack-dynamics-365-overview.md) を参照してください。

すべてのLCS **実装プロジェクト** は、プロジェクトのオンボードを正常に完了した後に、そのサービスを歓迎する FastTrack チームからの電子メールを受け取ります。 LCS **実装プロジェクト**を作成してから数週間以内にプロジェクトのオンボードを完了しなかった場合、プロジェクト チームにアラームが送信されます。

特定のプロジェクトについては、FastTrack はプロジェクト チームに電子メールを送り、オンボード ミーティング (60 分の会議通話) を提供します。 特定プロジェクトの詳細については、[FastTrack の適格性](../get-started/fasttrack-dynamics-365-overview.md#eligibility-for-fasttrack)を参照してください。 オンボード ミーティングはオプションです。 この通話中に、FastTrack チームは FastTrack プログラムを紹介し、テナントの検証、環境計画、アプリケーション ライフサイクル管理、および運用準備に関する重要なトピックについて説明します。 必要に応じて、通話中に**プロジェクトのオンボード**を完了するようチームを支援します。 プロジェクト マネージャーとデリバリー リーダーのほか、顧客およびパートナーのソリューション設計者がオンボード ミーティングに参加することをお勧めします。 
> [!NOTE]
> FastTrack チームからのオンボードに関連するすべての電子メールは Dynamics 365 Onboarding (<ond365@microsoft.com>) から発信されるので、スパムのブロック/フィルターがこの住所からの電子メールを許可していることを確認してください。


## <a name="key-data-to-keep-current-in-lcs"></a>LCS で最新状態にするキー データ

LCS 実装プロジェクトに主要なプロジェクト メンバー (プロジェクト マネージャーなど) を追加することをお勧めします。 各人の勤務先電子メールを必ず含めるようにしてください。 この方法で、お客様と協力して、プロジェクトのメンバーが弊社からの重要な連絡を見逃さないよう保証できます。

LCSプロジェクトのマイルストーン日付は、必ず最新の状態に保つようにしてください。 このように、さまざまなプロジェクトステージでお客様と連絡をとれます。 お客様が Go-live 日 により近づいたとき、マイクロソフトは、実稼働環境を配置する前に、プロジェクトの Go-live 評価のためにお客様と連絡を取ります。

マイルストーンの日付は、LCS 実装方法に格納されます。 詳細については、「顧客向け LCS」トピックの [方法](../../dev-itpro/lifecycle-services/lcs-works-lcs.md#methodologies) セクションを参照してください。


