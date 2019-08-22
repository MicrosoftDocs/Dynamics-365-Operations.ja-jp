---
title: Finance and Operations 実装プロジェクトの配送準備
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して Microsoft Dynamics 365 for Finance and Operations プロジェクトをオンボードする方法を説明します。
author: ClaudiaBetz-Haubold
manager: AnnBe
ms.date: 07/29/2019
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
ms.openlocfilehash: 36492b812ed7df813ef8ac8d0bea0679f6317c37
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850765"
---
# <a name="onboard-a-finance-and-operations-implementation-project"></a>Finance and Operations 実装プロジェクトの配送準備

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して Microsoft Dynamics 365 for Finance and Operations プロジェクトをオンボードする方法を説明します。

## <a name="microsoft-365-admin-center"></a>Microsoft 365 管理ビュー

あなたの組織がFinance and Operationsのサブスクリプションを購入したら、次の手順を実行するテナントテナント管理者によって、あなたの組織のAzure Active Directory (Azure AD) テナントを有効にする必要があります。

1. Inprivate/Incognito ブラウズセッションを開いて、[Microsoft 365 管理センター](https://admin.microsoft.com/)に移動します。
2. テナント管理者の資格情報を使用してログインします。
3. **請求 > サブスクリプション** に移動して、有効な **Dynamics 365 Unified Operations** サブスクリプションがある事を確認してください。 
   > [!NOTE]
   > サブスクリプションが表示されない場合は、ライセンスパートナーに問い合わせて、サブスクリプショントランザクションの状態と、サブスクリプションのテナントを確認してください。 既定では、すべてのMicrosoftオンラインサービスが同じAzure ADテナント上で実行されている必要があります。
4. 有効な**Dynamics 365 Unified Operations**サブスクリプションが表示されている場合は、LCSにログインして実装のプロジェクト作成フローをトリガーすることにより、次のステップに進むことができます。
5. 別のプライベートブラウザータブを開き、[Lifecycle Services](https://lcs.dynamics.com)に移動します。 現在のテナント管理者の資格情報を使用してアクセスするには、**ログイン** を選択します。
6. 実装プロジェクトのプロビジョニングを完了するために、他の表示されたメッセージを承認して確認します。
7. テナント管理者には、プロビジョニングされた実装プロジェクトにプロジェクト所有者が割り当てられます。 最後の手順として、テナント管理者は、Dynamics 365 for Finance and Operations 実装に参加するその他の組織やパートナーチームメンバーを追加する必要があります。 これは、LCS 実装プロジェクトメニューから選択された LCS プロジェクトユーザー管理で実行されます。

   ![LCS プロジェクト ユーザー管理](./media/LCSProjectUsersMenu.PNG)
   > [!NOTE]
   > テナント管理者が Finance and Operations の実装に参加していない場合は、追加のプロジェクト所有者を実装プロジェクトに割り当てる必要があります。

   ユーザーに割り当てることができるセキュリティロールの概要については、[プロジェクトセキュリティの構成](../../dev-itpro/lifecycle-services/configure-lcs-security.md#configuring-project-security)を参照してください。

## <a name="lcs-implementation-project-workspace"></a>LCS 実装プロジェクト ワークスペース

テナント管理者が Finance and Operations サブスクリプションの有効化を完了し、適切なユーザーを追加した後、チームメンバーは**実装プロジェクト**にアクセスできます。 

LCS を開始するには、「[Lifecycle Services for Finance and Operations の顧客](../../dev-itpro/lifecycle-services/lcs-works-lcs.md)」を参照します。 

## <a name="fasttrack-onboarding-services"></a>FastTrack オンボード サービス

LCS **実装プロジェクト** ワークスペースがプロビジョニングされた後、Microsoft FastTrack チームはプロジェクト チームに電子メールしてオンボーディング サービスについて議論するための呼出を要求します。 (この電子メールはond365@microsoft.comから発信されるので、スパムのブロック/フィルタがこのアドレスからの電子メールを許可していることを確認してください。) FastTrackプログラムと提供されるサービスの詳細については[Microsoft FastTrack for Dynamics 365](../get-started/fasttrack-dynamics-365-overview.md)を参照してください。

FastTrack Onboarding ミーティングは60分の会議通話です。 呼び出し中に、チームは FastTrack プログラムへ実装チームを紹介し、LCS プロジェクトおよび関連するタスクの初期構成の支援をおこないます。

- Tenant 検証
- LCS の概要
- LCS プロジェクト ユーザーの設定
- Microsoft Azure DevOps の設定
- サブスクリプション見積もりツール/使用状況プロファイラー
- 環境計画
- 環境配置
- サービスの概要、サポート、サービスの正常性
- プランの準備

次に示すプロジェクト ロールの参加者ーはこのオンボード ミーティングに参加することをお勧めします。 その他のロールはオプションです。

**顧客**

- プロジェクト所有者
- Microsoft ビジネス センターの管理者、ライセンスが Microsoft とのボリューム サービス契約を通じて調達された場合

**パートナー**

- デリバリー リード/ソリューション アーキテクト
- プロジェクト マネージャー

## <a name="key-data-to-keep-current-in-lcs"></a>LCS で最新状態にするキー データ

LCS 実装プロジェクトに主要なプロジェクト メンバー (プロジェクト マネージャーなど) を追加することをお勧めします。 各人の勤務先電子メールを必ず含めるようにしてください。 この方法で、お客様と協力して、プロジェクトのメンバーが弊社からの重要な連絡を見逃さないよう保証できます。

LCSプロジェクトのマイルストーン日付は、必ず最新の状態に保つようにしてください。 このように、さまざまなプロジェクトステージでお客様と連絡をとれます。 お客様が Go-live 日 により近づいたとき、マイクロソフトは、実稼働環境を配置する前に、プロジェクトの Go-live 評価のためにお客様と連絡を取ります。

マイルストーンの日付は、LCS 実装方法に格納されます。 詳細については、「顧客向け LCS」トピックの [方法](../../dev-itpro/lifecycle-services/lcs-works-lcs.md#methodologies) セクションを参照してください。

オンボーディング呼び出しはオプションのサービスです。 Finance and Operations の実装を理解しているパートナーは、FastTrack チームのサポートがなくても顧客と共にタスクを処理できます。 そのような場合、プロジェクト ユーザーおよびマイルストーン日付を最新にしておくことが特に重要です。
