---
title: 実装プロジェクトの研修
description: この記事では、Microsoft Dynamics Lifecycle Services (LCS) を使用してプロジェクトをオンボードする方法を説明します。
author: OlgaPetrovaFT
ms.date: 06/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: olpetrov
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: abed49ff05e677013e14f72af3df01451fff77a5
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/31/2022
ms.locfileid: "9387035"
---
# <a name="onboard-an-implementation-project"></a>実装プロジェクトの研修

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics Lifecycle Services (LCS) を使用して、財務と運用プロジェクトをオンボードする方法を説明します。

## <a name="microsoft-365-admin-center"></a>Microsoft 365 管理センター

組織が財務と運用アプリへのサブスクリプションを購入したら、サービスがテナント管理者によって、組織の Azure Active Directory (Azure AD) テナントで有効にされる必要があります。 この記事では、**テナント管理者** とは、**グローバル管理者** のセキュリティ ロールを持つ Azure AD テナントのすべてのユーザーを指します。 Azure AD の詳細については、[Azure Active Directory のロールを理解する](/azure/active-directory/roles/concept-understand-roles)を参照してください。

テナント管理者は、次の手順を完了する必要があります:

1. InPrivate/Incognito ブラウザー セッションを開き、[Microsoft 365 管理センター](https://admin.microsoft.com/) に移動します。
2. テナント管理者の資格情報を使用してサインインします。
3. **請求 > 製品 & サービス** に移動して、配置するアプリケーションに対して有効なサブスクリプションがあることを確認します。 
   > [!NOTE]
   > 有効なサブスクリプションが表示されない場合は、ライセンス パートナーに問い合わせて、サブスクリプション トランザクションの状態を確認してください。 適切な Azure AD テナントのためにサブスクリプションが購入されたことを確認することは重要です。  既定では、すべての Microsoft オンライン サービスが同じ Azure AD テナント上で実行されている必要があります。 オンボードの遅延の最も頻繁な原因は、サブスクリプションが誤った Azure AD テナントに配置されることです。 
4. 問題のサブスクリプションが有効と表示されている場合は、LCS にサインインして実装のプロジェクト作成フローをトリガーすることにより、次のステップに進むことができます。
5. 別のプライベートブラウザータブを開き、[Lifecycle Services](https://lcs.dynamics.com)に移動します。 現在のテナント管理者の資格情報を使用して LCS にアクセスするには、**ログイン** を選択します。
   > [!NOTE]
   > 政府のコミュニティ クラウド (GCC) と他のローカル クラウド配置オプションでは、接続エンドポイントが異なる場合があります。 詳細については、[Dynamics 365 Finance および Dynamics 365 Supply Chain Management の主権クラウドとローカル クラウド展開オプション](../../dev-itpro/deployment/deployment-options-geo.md)を参照してください。
7. 実装プロジェクトのプロビジョニングを完了するために、他の表示されたメッセージを承認して確認します。
8. テナント管理者には、プロビジョニングされた実装プロジェクトのプロジェクト所有者セキュリティ ロールが割り当てられます。  
   > [!NOTE]
   > テナント管理者が実装に参加していない場合は、少なくとも 1 人の追加のプロジェクト所有者を実装プロジェクトに割り当てる必要があります。

   ユーザーに割り当てることができるセキュリティ ロールを含む、LCS ユーザー管理の概要については、 [Lifecycle Services (LCS) のセキュリティのコンフィギュレーション](../../dev-itpro/lifecycle-services/configure-lcs-security.md#configuring-project-security) を参照してください。

## <a name="lcs-implementation-project-workspace"></a>LCS 実装プロジェクト ワークスペース

テナント管理者が財務と運用サブスクリプションの有効化を完了し、必要に応じてプロジェクト ユーザーを追加した後、チーム メンバーは **実装プロジェクト** ワークスペースにアクセスできます。

LCS で完了する最初の手順は、**プロジェクトのオンボード** です。 この手順は、Microsoft が管理するすべての環境を展開する前に、**2019 年 8 月 22 日 (PST) またはそれ以降** に作成されたすべての LCS 実装プロジェクトに必要です。 **プロジェクトのオンボード** 機能には、アクション センターの通知または LCS 実装プロジェクト メニューを使用してアクセスできます。 LCS の **プロジェクト オンボード** にアクセスするには、プロジェクト所有者セキュリティ ロールに割り当てられている必要があります。

LCS を開始するには、[財務と運用アプリの顧客用の Lifecycle Services (LCS)](../../dev-itpro/lifecycle-services/lcs-works-lcs.md) を参照してください。 

## <a name="fasttrack-onboarding-services"></a>FastTrack オンボード サービス

LCS **実装プロジェクト** ワークスペースがプロビジョニングされたら、Microsoft FastTrack チームはオンボードの進捗状況を監視します。 LCS **実装プロジェクト** を作成してから数週間以内にプロジェクトのオンボードを完了しなかった場合、プロジェクト チームにアラームが送信されます。 

FastTrack プログラムおよび提供されるサービスの詳細については、 [Microsoft FastTrack](/dynamics365/fasttrack/) を参照してください。

LCS プロジェクト オンボードの詳細については、[LCS プロジェクト オンボードの](../../dev-itpro/lifecycle-services/project-onboarding.md)を参照してください。


> [!NOTE]
> FastTrack チームからのオンボードに関連するすべての電子メールは Dynamics 365 Onboarding (<ond365@microsoft.com>) から発信されるので、スパムのブロック/フィルターがこの住所からの電子メールを許可していることを確認してください。


## <a name="key-data-to-keep-current-in-lcs"></a>LCS で最新状態にするキー データ

LCS 実装プロジェクトに顧客やパートナー チームから主要なプロジェクト メンバー (プロジェクト マネージャーなど) を追加することをお勧めします。 各人の勤務先電子メールを必ず含めるようにしてください。 この方法で、お客様と協力して、プロジェクトのメンバーが弊社からの重要な連絡を見逃さないよう保証できます。

LCSプロジェクトのマイルストーン日付は、必ず最新の状態に保つようにしてください。 このように、さまざまなプロジェクトステージでお客様と連絡をとれます。 お客様が Go-live 日 により近づいたとき、マイクロソフトは、運用環境を配置する前に、プロジェクトの Go-live 評価のためにお客様と連絡を取ります。

マイルストーンの日付は、LCS 実装方法に格納されます。 詳細については、「顧客向け LCS」記事の[方法](../../dev-itpro/lifecycle-services/lcs-works-lcs.md#methodologies)セクションを参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
