---
title: Dynamics 365 Talent の新機能および変更された機能 (2019 年 3 月 20 日)
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-20
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c16082bb18ac5c170aab30f1a2033e0790cbacc1
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2026008"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-20-2019"></a>Dynamics 365 Talent の新機能および変更された機能 (2019 年 3 月 20 日)

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

### <a name="setting-the-audience-on-activities"></a>活動の対象者の設定
システム内の活動で対象者を定義できるようになりました。 関連する活動の処理（面接、スケジュール、フィードバック、および EEO など）は、全候補者、内部の候補者、および外部の候補者に設定できます。 Microsoft Forms、YouTube ビデオ、Web コンテンツなどのカスタム活動は、全候補者、内部の候補者、外部の候補者、または採用チームに配信できます。  

### <a name="improve-career-site-job-discoverability-search-engine-optimization"></a>キャリア サイトの職務の発見可能性の向上：検索エンジン最適化
この機能により、検索エンジン クローラーは、Attract キャリア サイトの人材募集にアクセスしてインデックスを登録できます。 これにより、候補者が人気のある検索エンジンを使って Attract キャリアサイトに投稿された職務を探すことができます。

### <a name="show-login-hint-to-candidates-who-forgot-their-credentials"></a>資格情報を忘れた候補者にログインのヒントを表示します
候補者が保存または電子メールで送信されたリンクを開いているときに、求人に応募するために使用した社会資格情報を忘れた場合、プロバイダー名とユーザー名（難読化済）のヒントが表示されます。 これにより、適切な資格情報を使用して、求人応募にアクセスすることができます。

### <a name="help-internal-candidates-explore-internal-jobs"></a>内部の候補者が内部職務を確認するヘルプ
外部の候補者が採用担当者または採用マネージャの名前を確認できてしまうという問題が修正されました。 内部の候補者のみ、採用チームのメンバーを参照することができるようになりました。 内部の候補者が内部の職務を簡単に確認および応募することができます。 候補者が内部専用の職務を表示または適用するためにリンクにアクセスしようとすると、Azure Active Directory 資格情報の認証が求められます。 内部の候補者はまた、採用チームのメンバーに連絡して、関心を示したり、職務についての詳細を知ることができます。 この機能は、内部の候補者だけが使用できます。 詳細については、[Attract でキャリア サイト機能](./career-site.md) を参照してください。

### <a name="designate-silver-medalists-to-assign-high-value-applicants-for-future-positions"></a>将来の職位に価値の高い申請者を割り当てるため、銀メダリストを指定します。
採用担当者や採用マネージャーは、多くの場合、その役職に適した申請者の現在のリストを保持していますが、その役職はすでに埋められているため、オファーを拡張することはできません。 銀メダリストと呼ばれるそのような申請者は、次回類似の職務が空いたときに採用する時間を短縮することができるので価値があります。 申請者がオファー ステージに進んだ場合、Attract では、採用担当者と採用マネージャーが申請者リストの銀メダリストを指名できるようになりました。 銀メダリストの指定は、職務の申請者リストに表示されますが、これらの申請者が採用担当者または採用マネージャーのプールのメンバーである場合は人材プールビューにも表示されます。 また、その指定は、候補者の人材プールプロファイルの一部として職歴に表示されます。 この機能をプレビューするには、[管理センターの機能の管理](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature) を使用して管理者を有効にします。

### <a name="add-applicants-to-talent-pools"></a>人材プールへ申請者を追加
申請者リストに新しいアクションを提示することで、申請者を人材プールに追加するのが簡単になりました。 **人材プールへの追加**アイコンを選択することで、採用担当者または採用マネージャは、自分の人材プールのリストから選択して、求人の申請者リストから人材プールに申請者を簡単に追加できます。

### <a name="configure-whether-a-resume-is-required-to-apply-for-a-particular-job"></a>特定の職務に応募するために経歴書が必要かどうかを設定します
顧客のフィードバックに基づいて、採用担当者は特定の職務に応募するときに、アップロードされたファイルの形式で履歴書が必要かどうかを設定できるようになりました。 この設定は、採用プロセスでアクセス可能なアプリケーションの活動の一部です。 有効の場合、申請候補者は全員、この職位に応募するときに経歴書をアップロードするように求められます。 経歴書がアップロードされない限り、申請は完了したと見なされません。 これにより、すべての申請者がトリアージに十分な情報を採用担当者に提供できるようになり、申請者プール内のノイズを減らすことができます。

### <a name="candidates-can-apply-to-a-job-using-their-linkedin-profile"></a>候補者は、LinkedIn プロファイルを使用して求人に応募できます。
LinkedIn の最新のプロファイルをすでに持っている候補者は、そのプロファイルを使ってクリック 1 回で求人に応募することができます。

### <a name="track-how-a-candidate-profile-originated-in-the-system-and-where-your-applicants-discover-the-jobs-they-applied-for"></a>候補者プロファイルがシステム内でどのように作成されたか、および申請者が申請した仕事を見つけた場所を追跡します。
アプリケーションまたは人材プールプロファイルの**プロファイル**ページの候補の詳細の下にあるプロファイルソースを見ることで、特定の候補者のプロファイルが Attract でどのように作成されたかを調べることができるようになりました。 同様に、アプリケーション活動フィードの**アプリケーション活動**で提供されるアプリケーション ソースを調べることで、申請者がどのように職務を見つけたかを知ることができます。 この情報も、人材プール プロファイル内の職務履歴で使用できます。 採用担当者または採用マネージャー候補者を手動で追加すると、申請者または候補者のプロファイルのソースを指定するように要求されます。 候補者が初めて申請するとき、そのプロファイルソースは申請の発生元と同じになります。 この機能をプレビューするには、[管理センターの機能の管理](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature) を使用して管理者を有効にします。 既存の候補者および申請者にはソース情報がないことに注意してください。 ただし、採用担当者は、この情報を手動で追加することができます。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2195 に適用されます

### <a name="attract-integration-throws-duplicate-record-error-for-applications"></a>Attract 統合でアプリケーションの重複レコードエラーが発生する
この更新では、重複レコードに関する問題が修正されています。 この問題は、**人事管理**ワークスペースを開くときに発生します。

### <a name="unable-to-close-form-when-editing-name-sequence"></a>名前の順序を編集するときにフォームを閉じることができません
作業者フォームの名前の順序を編集するときの問題を修正するための変更が行われました。

## <a name="coming-soon"></a>間もなく公開

###  <a name="advanced-compensation-security-fixed-and-variable"></a>高度な報酬セキュリティ (固定および変動)
多くの組織では、報酬および福利厚生の管理者は特定の報酬レコードにのみアクセスできます。 これらは、経営幹部または地域の従業員向けのものである可能性があります。 この変更により、HR は組織内のさまざまな従業員グループの報酬プランを管理および維持できます。 固定および変動プランにはセキュリティ ロールを割り当てることができます。これは、プランへのアクセス権とプランに関連する従業員データ (給与または特別償却レコードなど) を決定します。 アクセス権を持つロールのみが、それらの従業員の報酬を処理できます。

###  <a name="email-support-for-alerts"></a>アラートの電子メールサポート
Finance and Operations のプラットフォーム更新プログラム 24 では、あるイベントによってトリガーされた時、自動的に連絡先に電子メール通知を送信する警告ルールを作成できます。

### <a name="duplicate-employee-check-interface-changes"></a>重複する従業員チェック: インターフェイスの変更
この変更により、名前のフィールドを入力すると重複が検出され、見つかった重複の数がステータスに表示されるようになります。 提供されたリンクを選択して新しいページを開き、検出された一致を使用するかどうかを評価できます。 データ入力の中断を回避するため、重複フォームは自動的に開きません。


