---
title: Microsoft Dynamics 365 Talent のプレビュー機能にアクセス
description: このトピックでは、管理者が Microsoft Dynamics 365 Talent のプレビュー機能を有効にできる方法について説明し、プレビューで現在有効な機能を一覧表示します。
author: tracykeya
manager: AnnBe
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: trkeya
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: e607c2ba4b544d60c97d98bd49b07d912d83ebc6
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008705"
---
# <a name="manage-preview-features"></a>プレビュー機能の管理

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 Talent の人事管理サービス (HCM) 機能の継続的なロールアウトの一環として、お客様にできるだけ早く新しい機能を体験していただきたいと思います。 管理者はそれぞれの環境でプレビュー機能を表示し使用することができます。 これらの機能は、一般的な使用可能性の準備がほぼ整い、および徹底したテストを経ています。 一般提供にリリースする前に、顧客フィードバックおよび検証の最終ラウンドを探しています。

このトピックでは、プレビュー機能を有効にできる方法について説明し、プレビューで現在使用可能な機能を一覧表示します。 このリストは、一般提供にリリースされる機能およびプレビューにリリースされる新しい機能として更新されます。 プレビューに新しい機能がリリースされるときに、通知は表示されません。 ユーザーは、機能を確認し始めます。 Talent の新機能に関する詳細は、[Dynamics 365 Talent の新機能と変更](./whats-new.md) および [Dynamics 365 と Power Platform Release Notes](https://docs.microsoft.com/business-applications-release-notes) を参照してください。

## <a name="enable-or-disable-preview-features"></a>プレビュー機能の有効化または無効化

プレビュー機能にアクセスするには、まず、環境でプレビュー機能を有効にする必要があります。 プレビュー機能の有効化または無効化は、環境に特有のものです。

> [!IMPORTANT]
> **プレビュー機能**設定をオンにして、その環境内の組織にいるすべてのユーザーに対してプレビュー機能を有効にします。 設定をオフにして、プレビュー機能を無効にし、ユーザーがアクセスできないようにします。 プレビュー機能は、Talent でサポートが制限されます。 プライバシーとセキュリティ対策の使用は少なく、Talent サービス レベル契約 (SLA) には含まれません。 個人のデータ (つまり、ユーザーを識別する任意の情報)、または法律上または規制順守要件の対象となるその他のデータを処理するプレビュー機能を使用しないでください。

### <a name="attract"></a>Attract

1. Microsoft Dynamics 365 Talent: Attract にサインインします。
2. 右上隅の**設定**メニュー (ギヤ記号) で、**管理センター**を選択します。
3. **機能管理**タブで**プレビュー機能**の横のオプションを選択すると、青色に変わり**オン**になります。

    ![Attract のプレビュー機能の有効化](./media/attract-enable-preview-features.png)

4. 個々のプレビュー機能の選択を選択または解除します。 何もしない場合は、使用可能なプレビュー機能がすべて有効になります。
5. 新しい機能の表示を開始するブラウザーを更新します。 既にサイン インしているすべてのユーザーは、次にサイン インするときに機能を表示し、または機能をすぐに表示するためにそのブラウザーを更新することができます。

> [!NOTE]
> 一部のプレビュー機能には、追加のコンフィギュレーションが必要な場合があります。 プレビュー機能の横にあるリンクを使用して、設定を完了します。

### <a name="core-hr"></a>Core HR

1. Talent へサインインします。
2. **システム管理**を選択し、**リンク**タブを選択します。
3. **システム管理**ページの**設定**で、**システム パラメータ**を選択します。
4. **システム パラメータ**ページで、**プレビュー機能**タブを選択します。
5. **すべてのユーザーにプレビュー モードを有効化**オプションを**はい**に設定して、プレビュー機能を有効にします。

    ![Core HR のプレビュー機能の有効化](./media/corehr-enable-preview-features.png)

> [!NOTE]
> プレビュー機能を無効にするには同じステップを行いますが、**すべてのユーザーにプレビュー モードを有効化**オプションでは、**いいえ**に設定します。 プレビュー機能を無効にすると、ユーザーがアクセスできなくなり、機能に関連付けられているプロセスでエラーが発生する可能性があります。

### <a name="onboard"></a>研修

現在、Microsoft Dynamics 365 Talent: Onboard で使用できるプレビュー機能はありません。

## <a name="features-that-are-currently-in-preview"></a>現在プレビューにある機能

### <a name="attract"></a>Attract

- [推奨候補者](./intelligent-recommendations.md#candidate-recommendations) – 10 名以上の候補者が履歴書やプロファイルを持っている場合は,仕事の要件を最も満たす候補者がジョブ ページの**考慮する応募者**セクションに表示されます。
- [推奨職務](./intelligent-recommendations.md#job-recommendations) – キャリアサイトに 10 以上のジョブが転記されている場合、Attract が推奨職務を提案します。
- [Broadbean の統合](./posting-jobs-external.md#post-jobs-to-broadbean) – Attract から外部のジョブ転記サイト Broadbean へジョブを転記することができます。 このプレビュー機能を有効にした後、Broadbean ユーザー名、クライアント ID、および暗号化トークンを入力して、設定を完了する必要があります。
- [Analytics](./analytic-reports.md) – Analytics ハブで、採用チームは単一ジョブのキー メトリックスを表示したり、すべてのジョブにわたる集約されたメトリックスも表示することができます。
- [EEO](./activities-attract.md) – 新しい活動タイプでは、定義済みのフォームを使用可能にし、候補者から雇用機会均等 (EEO) および連邦契約遵守プログラム部 (OFCCP) データを収集します。 定義済みフォームを編集することができません。
- [見込顧客の推奨](./intelligent-recommendations.md#prospect-recommendations) – Attract では、以前の応募者と現在の応募者を見直し、職務に適した見込顧客の一覧を提供します。
- [関連情報の検索](./attract-talent-pools.md#search-and-view-candidate-profiles) – 特定のスキル、名前、または教育の背景について、候補者全体のデータベースを検索できます。 Attract はプロファイル全体を検索し、見つかったすべての一致項目を強調表示します。 Attract はまた、候補者に利用可能なすべてのドキュメントを検索し、検索結果をインテリジェントにランク付けします。
- [活動対象者](./whats-new-talent-march-20.md#setting-the-audience-on-activities) – 活動 (面接、スケジュール、またはフィードバックなど) の対象者を、**すべての応募者**、**社内応募者**、または**外部の応募者**に対して設定できます。 YouTube ビデオ、Web コンテンツ、および Microsoft Forms などのカスタム活動を、全候補者、内部の候補者のみ、外部の候補者のみ、または採用チームに配信できます。
- [LinkedIn で適用](./career-site.md#enable-applying-for-jobs-with-linkedin-profiles) – Attract サイトでオプションを設定し、Linkedin を使用してジョブ候補を適用することができます。 この機能は、自分の LinkedIn プロファイルを使い候補者のアプリケーション プロセスを合理化し、キャリア サイトでアプリケーションを自動的に入力することができます。
- [ソース追跡](./source-tracking.md) – Attract では、求人活動のターゲットに役立つ情報を提供することによって、候補者アプリケーションを追跡します。 職務または人材プールに候補者を手動で追加するときに、アプリケーション ソースを選択できます。
- [銀メダリスト](./whats-new-talent-march-20.md#designate-silver-medalists-to-assign-high-value-applicants-for-future-positions) – 組織にとって最適な候補者であるが、現在の職位に対するオファーを拡張していない場合は、銀メダリストとして指定できます。 この機能は、次回に同様の職位を使用できるようになるまでの時間を短縮するのに役立ちます。

### <a name="core-hr"></a>Core HR

- [職位階層データの検証](./whats-new-talent-may-13-2019.md#new-page-to-validate-position-hierarchy-data) – 誤ってインポートされた循環照会の管理階層を検証できます。
- [休暇タイプの理由コードの指定](./whats-new-talent-may-13-2019.md#specify-reason-codes-on-leave-types) – 休暇タイプの理由コードを指定できます。
- [休暇申請の理由コードを要求](./whats-new-talent-may-13-2019.md#require-reason-codes-for-specific-leave-types-on-time-off-requests) – 休暇タイプの理由コードを指定するだけでなく、休暇申請の理由コードを要求することもできます。
- [HR の休暇と不在のトランザクションリストの提供](./whats-new-talent-may-13-2019.md#provide-a-leave-and-absence-transaction-list-for-hr) – 休暇と不在トランザクションの一覧を表示して、休暇のバランスを確認できます。

### <a name="onboard"></a>研修

現在、Onboard で使用できるプレビュー機能はありません。

## <a name="feedback"></a>フィードバック

これらのプレビュー機能の使用経験に関するご意見をお聞かせください。 その他の機能を使用する際に、以下のサイトにて、フィードバックを定期的に転記することをお勧めします。

- [コミュニティ](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – このサイトは、ユーザーが使用ケースを説明したり、質問したり、およびコミュニティ ヘルプを得られる優れたリソースです。
- 製品に必要な機能、または既存の機能に対して行われるべき変更についてお知らせください。 以下のサイトにて、製品アイデアを提案してください。

    - [Attract アイデア](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Core HR アイデア](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)
    - [Onboard アイデア](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

フィードバックまたは製品のレビュー申請には個人データ (ユーザーを識別できる任意の情報) を含めないことを確認してください。 収集した情報はさらに分析されることがありますが、該当するプライバシーに関する法律の下で要求に回答するためには使用されません。 これらのプログラムで個別に収集された個人データは、[Microsoft のプライバシーに関する声明](https://privacy.microsoft.com/privacystatement) の対象となります。

> [!TIP]
> リリースに際して新しいプレビュー機能に関して最新の状態を保つため、このトピックをブックマークし、頻繁に確認してください。

## <a name="see-also"></a>参照

- [Talent アプリの試みまたは購入](https://dynamics.microsoft.com/talent/overview/)
- [新機能](./whats-new.md)
- [リリース ノート](https://docs.microsoft.com/business-applications-release-notes/index)
- [Talent に関するサポートの利用](./talent-support.md)
