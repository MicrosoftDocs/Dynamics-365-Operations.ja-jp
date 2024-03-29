---
title: プロジェクトの研修
description: この記事では、Microsoft Dynamics Lifecycle Services (LCS) のプロジェクト オンボード ウィザードについて説明します。
author: vetrivicky
ms.date: 06/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: vetric
ms.search.validFrom: 2020-5-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: f02ffc25bb9a6398639aece91e1245a4bdcb9b9d
ms.sourcegitcommit: fde2867524b6a851628185cbdeee60a6ad918d08
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2022
ms.locfileid: "9592017"
---
# <a name="project-onboarding"></a>プロジェクトの研修

[!include [banner](../includes/banner.md)]


プロジェクト オンボードは、Dynamic 365 Finance、Dynamics 365 Supply Chain Management、Dynamic 365 Retail の新しい実装プロジェクトの主要なコンフィギュレーション コンポーネントを設定するプロセスを通じて、Microsoft Dynamics Lifecycle Services (LCS) のプロジェクト ユーザーをガイドする自己ペースのウィザードによるオンボード エクスペリエンスです。 このウィザードは、実装中および実装後にアクセスすることもできます。また、必要に応じて情報を更新するために使用することもできます。

Microsoft では、お客様から提供された情報を必要としています。 プロジェクトのオンボードを完了するときに、最新かつ正確なデータを提供する必要があります。 プロジェクトのオンボードを完了したら、環境を配置してプロジェクトの実装を続行できます。

プロジェクトのオンボードにアクセスするには、LCS にログインし、メイン メニューで **プロジェクト オンボード** を選択します。

> [!NOTE]
> プロジェクトのオンボードは、実装プロジェクトで使用できます。また、Microsoft が管理する環境を配置する前に完了する必要があります。 実装プロジェクトの詳細については、[財務と運用アプリの顧客用の Lifecycle Services (LCS)](lcs-works-lcs.md#lcs-workspace-for-the-current-versions-of-the-finance-and-operations-apps) を参照してください。

> [!NOTE]
> プロジェクトのオンボードを完了する前に、データ所在地要件を考慮し、実装プロジェクトが適切な Lifecycle Services (LCS) の地域に作成されていることを確認することが重要です。 さまざまな地域での配置オプションの詳細については、[ローカル地域における Dynamics 365 Finance、Supply Chain Management、および Commerce](../deployment/deployment-options-geo.md) を参照してください。


このオンボード プロセスの詳細については、[実装プロジェクトのオンボード](../../fin-ops/imp-lifecycle/onboard.md#lcs-implementation-project-workspace)を参照してください。また、[財務と運用: Dynamics 365 へのオンボード](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-onboarding-to-dynamics-365-1-10-19) TechTalk もご覧ください。


## <a name="onboarding-steps"></a>オンボード ステップ

プロジェクトのオンボードの各手順は、プロジェクトの実装に関するガイダンスを提供したり、プロジェクトコンテキストに関する情報を収集したりすることによって、FastTrack チームがより優れたサービスを提供できるように設計されています。 ウィザードに正確な情報を入力することによって、Microsoft が実装計画を理解し、適切なガイダンスを提供できるようになります。

ウィザード内を移動するには、**次へ** ボタンと **戻る** ボタンを使用するか、または各ステップを直接選択します。 一部の手順では、ページの右の列に、この手順を完了するのに役立つ追加の文脈情報が表示されます。

## <a name="welcome"></a>ようこそ

**ようこそ** ページには、プロジェクトのオンボードを完了するために必要な一般的なガイダンスと情報が表示されます。

## <a name="project-overview"></a>プロジェクトの概要

- 実装プロジェクトの概要情報を提供します。
- プロジェクトのビジョンと目標をいくつかの文で説明します。 この情報は、達成する目標とプロジェクトの成功を定義する方法を Microsoft が理解するのに役立ちます。
- パートナー MPN ID を指定します。この ID は、実装パートナー チームから取得できます。 パートナーが関係していない場合、またはまだ特定されていない場合は、実装パートナーのドロップダウン リストから適切なオプションを選択します。 正確なパートナー データを提供することは、[FastTrack プログラム](/dynamics365/fasttrack/?toc=/dynamics365/commerce/toc.json) の割り当ての前提条件であることに注意してください。 パートナーに関する適切な情報が提供されていない場合は、重要なサービスの機会を逃してしまう可能性があります。 パートナーを特定したら、MPN ID を更新する必要があります。
- 現在のライセンスを含めた完全ロールアウト後のユーザー ライセンスの予測される数量を指定します。 この番号は、現在のライセンス購入時とは異なる場合があります。 変更が予定されていない場合は、現在のユーザー ライセンス数を入力します。 ライセンス タイプが該当しない場合は、**0** (ゼロ) を入力します。
- インプリメンテーション プロジェクトがデモ プロジェクトの場合、または別のテナントから移動する場合は、詳細を入力します。

## <a name="project-scope"></a>プロジェクト スコープ

- 機能および製品の観点から実装を適用するための計画方法に関する情報を提供します。 この情報は、Microsoft が実装を理解し、必要なガイダンスを提供するのに役立ちます。
- この手順で特定の機能のオプションを **はい** に設定した後、それらの機能に関連する追加データを提供する必要があります。 このデータは、Microsoft が実装の際にお客様に対してより良いやり取りをするために役立ちます。 追加のデータ フィールドは必須です。

## <a name="define-your-team"></a>チームを定義する

- すべてのプロジェクト チーム メンバーが参加していて、コンフィギュレーションされていることを確認します。
- ユーザー リストに有効な電子メール アドレスがある少なくとも 2 人のユーザーに対して、**FastTrack の基本連絡先** オプションを **はい** に設定します。 どのチーム メンバーに対してもこのオプションが **はい** に設定されていない場合は、FastTrack が実装時に実装ガイドのためにすべてのチーム メンバーに連絡します。 必要に応じて、FastTrack から連絡を受ける少なくとも 1 人の顧客と 1 人のパートナー チーム メンバーを指名する必要があります。
- 各チーム メンバーには、プロジェクト セキュリティ ロールおよび実装ロールが割り当てられます。 プロジェクト セキュリティ ロールは LCS プロジェクト ワークスペースへのアクセスに関連しており、実装ロールは、実装チームにおける個々のチーム メンバーのロールに関連しています。 監視対象の電子メール アドレスを持つプロジェクト チーム メンバーの間に、顧客の代表者を含めることを強くお勧めします。

詳細については、[プロジェクト セキュリティのコンフィギュレーション](configure-lcs-security.md#configuring-project-security) および [Dynamics 365 実装のロール](/training/modules/get-started-implementation-project/01-2-roles) を参照してください。

## <a name="define-milestone-dates"></a>マイルストーン日付の定義

- すべての必須マイルストーン ステップを定義します。 マイルストーンは、プロジェクトの方法に関連付けられています。 マイルストーンの日付がまだ決定されていない場合は、仮の日付を使用します。
- マイルストーンの日付を計画の変更に応じて更新します。 Microsoft は、マイルストーンの日付を使用して、各マイルストーンに適切なガイダンスを提供します。 マイルストーンの日付を編集するには、鉛筆の記号を選択します。

## <a name="associate-lcs-with-azure-devops"></a>LCS と Azure DevOps の関連付け

- LC と Azure DevOps を接続し、アプリケーション ライフサイクルを維持します。
- Azure DevOps アカウントのルート URL と、Azure DevOps から取得した個人用アクセス トークンを入力します。 Azure DevOps アカウントは顧客に所属している必要があります。

> [!NOTE]
> LCS では、Azure DevOps のルート URL をレガシー形式で入力する必要があります。 レガシ形式は `https://ACCOUNT.visualstudio.com` で、`https://contoso.visualstudio.com` がその一例です。

## <a name="configure-azure-devops"></a>Azure DevOps のコンフィギュレーション

- LCS とビジネス プロセス モデラー (BPM) との間で作業項目をマップします。
- セットアップを承認します。
- カスタム プロセス テンプレートの使用を選択した場合は、次のベスト プラクティスに従います。

    - 既存の作業項目の種類は削除しないでください。
    - 作業項目の種類の既存の状態は削除しないでください。
    - 必須フィールドを作業項目の種類に追加しないでください。

## <a name="fasttrack"></a>FastTrack

- **FastTrack** ページでは、FastTrack プログラムが紹介されています。 ここでは、プログラムの構成内容と、実装によってそれを活用する方法について説明します。
- Microsoft では、製品やプラットフォームで発生している変更についてのベスト プラクティス ガイダンスや情報を共有し続けているため、既存の [TechTalk](https://community.dynamics.com/365/b/alltechtalks) を視聴し、今後の TechTalk にサブスクライブすることを強くお勧めします。

## <a name="next-steps"></a>次のステップ

**次の手順** ページには、実装の最も重要な側面に関する追加情報が表示されます。 このページには、実装中にいつでもアクセスできます。

## <a name="complete-onboarding"></a>オンボードの完了

- プロジェクトのオンボードを完成させると、実装の次の手順に進むことができます。
- プロジェクトのオンボードは、すべての前のステップが完了した後にのみ完了できます。 前のステップが完了していない場合は、**オンボードの完了** ボタンは使用できません。
- スキップしたステップには、アスタリスク (\*) が付いています。 不足しているステップを表示することもできます。
- プロジェクトのオンボードを完了した後は、プロジェクト スコープの値などの情報の更新を続行できます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
