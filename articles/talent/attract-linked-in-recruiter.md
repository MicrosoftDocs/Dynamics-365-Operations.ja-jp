---
title: "LinkedIn Recruiter によるソーシング"
description: "このトピックでは、ジョブおよびジョブ候補の推奨事項を取得する機械学習の使用に関する情報を提供します。"
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2fc6bf25d303d7d8de8002a923a080b90dcfbeab
ms.openlocfilehash: 106103e2c3d8f3d89aac5140174e5794da22536f
ms.contentlocale: ja-jp
ms.lasthandoff: 10/24/2018

---

# <a name="sourcing-with-linkedin-recruiter"></a>LinkedIn Recruiter によるソーシング
[!include[banner](../includes/banner.md)]

LinkedIn は世界最大の人材データベースで、多くの場合、採用担当者が検索、やり取りおよび採用担当者による入力を検討するジョブの候補者ソースを使用するプライマリ システムです。 Dynamics 365 for Talent と LinkedIn Recruiter の統合: Attract は、ユーザー用に採用および 2 つのシステム間で同期するデータの保存ができます。

> [!NOTE]
> Attract と統合する LinkedIn Recruiter を使えるようにするには、包括採用アドオンおよび LinkedIn Recruiter 席が必要です。

## <a name="set-up-linkedin-recruiter-with-attract"></a>Attract と LinkedIn Recruiter を設定 

LinkedIn Recruiter 能力を使用するには、Attract インスタンスで契約レベルまたは会社レベルのアクセスをコンフィギュレーションする必要があります。 コンフィギュレーション プロセスを完了するには、LinkedIn Recruiter 契約の管理者であるユーザーを処理する必要があります。 Attract で LinkedIn Recruiter をコンフィギュレーションするには、以下の手順を実行します。

1.  管理者として Attract にサインインし、**管理者設定**へ移動します。

2.  左ウィンドウで **LinkedIn 統合**タブをクリックします。

[![LinkedIn Recruiter 統合を開始する Attract 管理者ビュー](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3.  **接続**をクリックして設定を開始すると、LinkedIn サインイン手順のガイドが表示されます。

4.  複数の LinkedIn 契約に関する席数を使用する場合は、Attract システムにする契約を選択します。 1 つの LinkedIn 契約のみの場合、この手順は必要ありません。

5.  LinkedIn ウィジェットでは、表示されている統合一覧で管理者の設定を読み込みます。 **Recruiter System 接続**で、**要求**をクリックします。

[![要求 LinkedIn Recruiter 統合への Attract 管理者ビュー](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6.  統合が Attract から要求されると、**パートナー準備完了**と表示され、**採用管理者設定**から有効にする準備が可能です。 このページで**通知パートナー**が表示されたら、しばらく待ち、**通知パートナー**をクリックしてページを最新の情報に更新します。 **パートナー準備完了**と表示されます。

[![完了した要求の Attract 側を示す Attract 管理者ビュー](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

次の手順を完了するには、LinkedIn Recruiter 契約に関する管理特権が必要です。

7.  管理者アカウントを使用して LinkedIn にサインインし、右上の LinkedIn Recruiter に移動します。 

8. 画面上部にある**詳細**メニューで、**管理者設定**をクリックしてから **ATS** タブをクリックします。

Attract システムでは、使用可能なオプションがいくつか表示されます。

9. **In-ATS インジケータ**と **In-ATS プロファイル ウィジェット**に 1 クリック エキスポートのみ有効にする場合、**会社レベルのアクセスを**を選択します。 InMail 履歴、メモの履歴および InMail スタブ プロファイル アクセスをプラスした会社レベル アクセスの機能を有効にする場合は、**契約レベル アクセス**を選択します。

10. LinkedIn Recrioter の**管理者 ATS** 設定から必要なアクセス レベルをオンにします。

[![LinkedIn Recruiter 管理者ビューから Attract 統合にオン](./media/EnableRSC.png)](./media/EnableRSC.png)

12. AttractAdmin として Attract 管理者設定に戻り**LinkedIn 統合**タブを選択します。選択されたアクセス レベルをオンにし、**有効**と表示された Linkedln ウィジェットの積荷を確認できます。

[![LinkedIn Recruiter 統合完了](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="using-linkedin-recruiter-capabilities"></a>LinkedIn Recruiter 能力を使用

Attract 管理者が LinkedIn Recruiter 能力を有効にした後、採用マネージャーおよび採用担当者はアクセス可能です。 これらの能力を使用するには、**ユーザー設定**で LinkedIn アカウントに接続します。 管理者とユーザーの両方の設定を接続した後、いくつかの能力が使用可能になります。

### <a name="in-ats-profile-widget"></a>In-ATS プロファイル ウィジェット

応募者の LinkedIn プロファイルを Attract で表示できます。 ATS 情報がユーザーの LinkedIn 情報と一致すると、Linkedln ウイジェット では候補者のプロファイルが表示されます。

プロファイルを表示するには、ジョブまたは人材プールのいずれかより候補者のプロファイルへ移動します。 候補者のプロファイルにて **LinkedIn** タブを選択し、プロファイル ウィジェットを読み込みます。 プロファイル ウィジェットを使用して、正しい一致であるかどうかを示します。 一致しない場合は、正しい担当者を検索します。 候補者をこのページから LinkedIn Recruiter プロジェクトに保存することもできます。

### <a name="1-click-export"></a>1 クリック エクスポート 

LinkedIn の候補者を調達する間、候補者を現在開いているジョブに 1 クリック エクスポートできます。 1 クリック エクスポートの以下の手順を実行します。 これらの手順を完了する前に、ジョブの採用マネージャーまたは採用担当者のロールが割り当てられており、そのジョブで**見込顧客**ステージが表示されているか確認します。

1.  ジョブを作成し、適切なロールを割り当てた後、ジョブをアクティブにします。

2.  ジョブがアクティブである場合は、LinkedIn Recruiter に移動します。

3.  探している候補者を検索して、プロファイルに移動します。

4.  連絡先カードのジョブ検索ボックスを使用して、タイトルまたは Attract で有効のジョブ ID を使いジョブを検索します。 ジョブが見つからない場合は、**変更 ATS** をクリックして正しい Attract インスタンスを検索します。

5. ジョブを選択して、**エクスポート**をクリックします。 Attract は候補者をフェッチします。

6.  Attract に移動して、それぞれのジョブをオープンします。 ジョブの**見込顧客**ステージで、エクスポートした候補者を検索します。

### <a name="in-ats-indicator"></a>In-ATS インジケーター 

LinkedIn Recruiter を使用すると、候補者が組織内の他のジョブに適用するかどうかの追跡が可能で、ジョブ アプリケーションの異なるステージであることの確認および LinkedIn Recruiter の Attract からフィードバックとコメントの表示が可能です。

1.  LinkedIn Recruiter を開き、探している候補者プロファイルを特定します。

2.  下にスクロールして、候補者プロファイルで **In-ATS** セクションを表示します。

3.  このウィジェットを使用して、LinkedIn Recruiter ビュー内から Attract に存在する候補者の関連情報を表示することができます。

4.  **Jobs & Statuses** タブを選択して、ジョブの一部、最新のステータス、および各ジョブに移動する方法を参照してください。

5.  **面接フィードバック**タブを選択し、面接者が Attract で送信したフィードバックを参照してください。

6.  **メモ**タブを選択し、Attract で申請者にキャプチャされたメモを参照してください。

### <a name="inmail-history"></a>InMail 履歴

LinkedIn InMail 履歴は、LinkedIn Recruiter と契約レベルのアクセスで使用できます。 有効な場合は、候補者とともに全体の InMail 履歴を表示できます。 また、組織の誰が候補者と InMail を交換できたのかも確認できますが、両間でメッセージを表示することはできません。

InMail 履歴を表示するには、応募者のプロファイルから **LinkedIn** タブに移動し、履歴を表示するページの下にスクロールします。 候補者が要求に答え、LinkedIn でプロファイルの共有を選択する場合にのみ、InMail 履歴を表示することができます。 InMail からのメッセージは、数時間ごとに Attract と同期します。

### <a name="notes-history"></a>メモの履歴 

LinkedIn メモの履歴は、LinkedIn Recruiter と契約レベルのアクセスで使用できます。 有効にすると、組織とな異なる採用担当者によってキャプチャされた候補者に関するメモを表示できます。

メモの履歴を表示するには、応募者のプロファイルから **LinkedIn** タブに移動し、履歴を表示するページの下にスクロールします。 LinkedIn Recruiter からの応募者に関するすべてのメモを表示することができます。

### <a name="inmail-stub-profile"></a>InMail スタブ プロファイル

InMail スタブ プロファイルは、LinkedIn Recruiter と契約レベルのアクセスで使用できます。 候補者が組織内のユーザーとその LinkedIn プロファイルの共有に同意する場合は、Attract 候補者を追跡でき、新しい候補者のレコードが各候補者へ作成されます。

候補者の一覧を表示するには、**人材プール**に移動し、システムで作成された LinkedIn 人材プールを参照してください。 この人材プールには、LinkedIn から受信した候補者リストと スタブ プロファイルが含まれています。リストには候補者の名前と姓が表示されています。 候補者が自身の電子メール アドレスを共有すると選択した場合、電子メール IDが表示されます。

