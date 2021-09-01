---
title: 実装プロジェクトの研修
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用してプロジェクトをオンボードする方法を説明します。
author: ClaudiaBetz-Haubold
ms.date: 05/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: chaubold
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 4d7e8a24f361145e5efa8610552e1b4383927f435cf72df8aa52b6c6495ed994
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754970"
---
# <a name="onboard-an-implementation-project"></a>実装プロジェクトの研修

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して Finance and Operations プロジェクトをオンボードする方法を説明します。

## <a name="microsoft-365-admin-center"></a>Microsoft 365 管理ビュー

組織が Finance and Operations のサブスクリプションを購入したら、テナント管理者は、組織の Azure Active Directory (Azure AD) テナントを有効にし、次の手順を完了する必要があります。

1. InPrivate/Incognito ブラウズ セッションを開いて、[Microsoft 365 管理センター](https://admin.microsoft.com/) に移動します。
2. テナント管理者の資格情報を使用してログインします。
3. **請求 > 製品 & サービス** に移動して、配置するアプリケーションに対して有効なサブスクリプションがあることを確認します。 
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

テナント管理者が Finance and Operations サブスクリプションの有効化を完了し、適切なプロジェクト所有者を追加した後、チーム メンバーは **実装プロジェクト** ワークスペースにアクセスできます。

LCS で完了する最初の手順は、**プロジェクトのオンボード** です。 この手順は、Microsoft が管理するすべての環境を展開する前に、**2019 年 8 月 22 日 (PST) またはそれ以降** に作成されたすべての LCS 実装プロジェクトに必要です。 **プロジェクトのオンボード** 機能には、アクション センターの通知または LCS 実装プロジェクト メニューを使用してアクセスできます。 LCS の **プロジェクト オンボード** にアクセスするには、プロジェクト所有者セキュリティ ロールに割り当てられている必要があります。

LCS を開始するには、[Finance and Operations アプリ顧客用の Lifecycle Services (LCS)](../../dev-itpro/lifecycle-services/lcs-works-lcs.md) を参照してください。 

## <a name="fasttrack-onboarding-services"></a>FastTrack オンボード サービス

LCS **実装プロジェクト** ワークスペースがプロビジョニングされたら、Microsoft FastTrack チームはオンボードの進捗状況を監視します。 LCS **実装プロジェクト** を作成してから数週間以内にプロジェクトのオンボードを完了しなかった場合、プロジェクト チームにアラームが送信されます。 

FastTrack プログラムおよび提供されるサービスの詳細については、 [Microsoft FastTrack](/dynamics365/fasttrack/) を参照してください。

LCS プロジェクト オンボードの詳細については、[LCS プロジェクト オンボードの](../../dev-itpro/lifecycle-services/project-onboarding.md)を参照してください。


> [!NOTE]
> FastTrack チームからのオンボードに関連するすべての電子メールは Dynamics 365 Onboarding (<ond365@microsoft.com>) から発信されるので、スパムのブロック/フィルターがこの住所からの電子メールを許可していることを確認してください。


## <a name="key-data-to-keep-current-in-lcs"></a>LCS で最新状態にするキー データ

LCS 実装プロジェクトに顧客やパートナー チームから主要なプロジェクト メンバー (プロジェクト マネージャーなど) を追加することをお勧めします。 各人の勤務先電子メールを必ず含めるようにしてください。 この方法で、お客様と協力して、プロジェクトのメンバーが弊社からの重要な連絡を見逃さないよう保証できます。

LCSプロジェクトのマイルストーン日付は、必ず最新の状態に保つようにしてください。 このように、さまざまなプロジェクトステージでお客様と連絡をとれます。 お客様が Go-live 日 により近づいたとき、マイクロソフトは、実稼働環境を配置する前に、プロジェクトの Go-live 評価のためにお客様と連絡を取ります。

マイルストーンの日付は、LCS 実装方法に格納されます。 詳細については、「顧客向け LCS」トピックの [方法](../../dev-itpro/lifecycle-services/lcs-works-lcs.md#methodologies) セクションを参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]