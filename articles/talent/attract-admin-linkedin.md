---
title: Attract と LinkedIn との統合の設定
description: このトピックでは、Attract から Linkedln にジョブを簡単に転記し、採用担当者が候補者の Linkedln プロファイルと採用情報を同期できるように、Microsoft Dynamics 365 Talent - Attract の Linkedln 統合のコンフィギュレーション方法を説明します。
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 4c518fb7036d44aa52c8db859ee3616fc4e58a06
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461780"
---
# <a name="set-up-linkedin-integration-with-attract"></a>Attract と LinkedIn との統合の設定

[!include [banner](includes/banner.md)]

採用担当者および採用マネージャーが、Microsoft Dynamics 365 Talent: Attract と LinkedIn 統合をコンフィギュレーション構成して、主なスキルをご提供します。 Attract では、ジョブを最大の本格的なオンライン ネットワークである LinkedIn に直接転記できます。

Attract を通して LinkedIn に転記したジョブは、制限付き一覧であり、会社に対して追加の費用が発生することはありません。 これらの一覧は、Attract などの LinkedIn ソフトウェア パートナーを通じてのみ利用可能です。 会社の LinkedIn ページの **キャリア** パネルには有料の一覧しか表示されないため、この一覧は表示されません。 ただし、潜在的な候補者が使用可能なすべての職務を表示する際には表示されます。 制限付き一覧は、LinkedIn の職務検索でも表示されます。

Attract では、この人気のあるキャリア サイトからの応募者を探すのに役立つ LinkedIn と統合する方法を 2 とおり用意しています。

- Attract から LinkedIn へジョブを転記します。
- Attract から LinkedIn へ候補者をソーシングします。

両方のオプションを、管理者センターの **LinkedIn 統合** タブで構成します。 管理センターを開くには、<https://attract.talent.dynamics.com/adminsettings> へ移動します。

> [!NOTE]
> Attract で LinkedIn Recruiter 統合を使用するには、[包括採用アドオン](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) および [LinkedIn Recruiter ライセンス](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18) が必要です。 詳細については、[Microsoft Dynamics 365 Talent - Attract のバージョンは何ですか](./attract-comprehensive-hiring.md) を参照してください。

LinkedIn へのジョブ転記に問題がある場合は、[LinkedIn と Microsoft Dynamics 365 Talent - Attract の統合に関するトラブルシューティング](./attract-troubleshoot-linkedin.md) を参照してください。

LinkedIn にジョブ転記するための他の方法については、[Linkedln と Attract の統合に関するよく寄せられる質問](./attract-linkedin-faq.md) を参照してください。

## <a name="configure-job-posting-to-linkedin"></a>LinkedIn へのジョブ転記のコンフィギュレーション

Attract から LinkedIn にジョブ転記する前に、[Linkedln 社の ID](https://aka.ms/findID) が必要です。 LinkedIn 社の ID は、LinkedIn で会社を固有に識別する文字列です。 詳細については、[Linkedln 社の ID を Linkedln 職務ボードに関連付ける - よく寄せられる質問](https://aka.ms/findID) を参照してください。

Attract では、ジョブ転記のフィードが LinkedIn に送信され、1 日に 1 回ほどフィードがチェックされます。 ジョブをサイトに転記するのに、最大 48 時間かかります。

LinkedIn に転記された職務は、ライブ LinkedIn サイトに表示されます。 LinkedIn には職務を転記するためのテスト環境はありません。 したがって、テスト ジョブを誤って転記しないように注意してください。 

1. 右上隅の **設定** メニュー (ギヤ記号) で、**管理センター** を選択します。 または、<https://attract.talent.dynamics.com/adminsettings> を参照してください。
2. **Linkedln 統合** タブを選択します。
3. **会社名** に会社名を入力し、**会社の ID** に LinkedIn 社の ID を入力します。 会社名が、会社の LinkedIn ページに表示される名前と一致していることを確認してください。 LinkedIn 会社 ID の詳細については、[Linkedln 会社 ID を Linkedln 職務ボードに関連付ける - よく寄せられる質問](https://www.linkedin.com/help/linkedin/answer/98972) を参照してください。

    組織に関する情報を変更する必要がある場合は、[組織の住所、技術連絡先などの変更](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more) を参照してください。 問題が解決しない場合は、[LinkedIn サポート](https://www.linkedin.com/help/linkedin) に連絡してください。

4. **保存** を選択します。

## <a name="set-up-linkedin-recruiter-with-attract"></a>Attract で LinkedIn Recruiter を設定 

採用担当者が LinkedIn Recruiter を介してジョブを調達するには、Attract の LinkedIn Recruiter と統合をコンフィギュレーションする必要があります。 コンフィギュレーション プロセスを完了するには、組織の LinkedIn Recruiter 契約の管理者であるユーザーを処理する必要があります。

1. 右上隅の **設定** メニュー (ギヤ記号) で、**管理センター** を選択します。 または、<https://attract.talent.dynamics.com/adminsettings> を参照してください。
2. **Linkedln 統合** タブを選択します。

    [![ LinkedIn Recruiter 統合を開始する Attract 管理者ビュー](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. **接続** を選択して、設定を開始します。 LinkedIn の登録手続きについての案内が表示されます。
4. 複数の LinkedIn 契約に関する席数を使用する場合は、Attract システムにする契約を選択します。 1 つの LinkedIn 契約のみの場合、この手順をスキップできます。
5. **Recruiter System Connect (RSC)** で、**要求** を選択します。

    [![ LinkedIn Recruiter 統合を要求する Attract 管理者ビュー](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6. **Recruiter System Connect (RSC)** 設定は、**パートナー準備完了** として表示されるようになります。 このページで **通知パートナー** が表示されたら、しばらく待ち、**通知パートナー** を選択してページを最新の情報に更新します。 これで設定が、**パートナー準備完了** に表示されます。

    [![完了した要求の Attract 側を示す Attract 管理者ビュー](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

7. 以下の手順を完了するには、LinkedIn Recruiter 契約に関する管理特権が必要です。

    1. 自分の管理者アカウントを使用して LinkedIn にログインし、画面右上の **LinkedIn Recruiter** を選択します。 
    2. ページ上部にある **詳細** メニューで、**管理者設定** を選択してから **ATS** タブを選択します。
    3. 1 つの契約に対して 1 回のエクスポートを有効にするには、**契約レベルのアクセス (この契約を使用するすべての座席に対して)** をオンにします。 会社全体でこの機能を有効にするには、**会社レベルのアクセス (会社内のすべての契約に対して)** をオンにします。

    [![LinkedIn Recruiter の管理者ビューから Attract 統合にオン](./media/EnableRSC.png)](./media/EnableRSC.png)

8. Attract 管理センターで、**LinkedIn 統合** タブを選択します。**Recruiter System Connect (RSC)** の設定が、**有効** と表示されます。

    [![LinkedIn Recruiter 統合の完了](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="set-up-apply-with-linkedin-in-attract"></a>Attract と LinkedIn で適用を設定

自分の LinkedIn プロファイルを使用して、ジョブに応募を許可することができます。 LinkedIn の適用に関しては、[すべての場所における Linkedln の機能 - Linkedln の適用](https://blog.linkedin.com/2011/07/24/apply-with-linkedin) を参照してください。

現在プレビューにある機能です。 この手順を実行する前に、LinkedIn の適用が有効になっていることを確認してください。 プレビュー機能の有効化についての詳細は、[Microsoft Dynamics 365 Talent のプレビュー機能の利用](./access-preview-feature.md) を参照してください。

1. 右上隅の **設定** メニュー (ギヤ記号) で、**管理センター** を選択します。 または、<https://attract.talent.dynamics.com/adminsettings> を参照してください。
2. **Linkedln 統合** タブを選択します。

    [![ LinkedIn Recruiter 統合を開始する Attract 管理者ビュー](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. **LinkedIn の適用** の横にある **接続** を選択して、設定を開始します。 LinkedIn の残りのプロセスについての案内が表示されます。

## <a name="see-also"></a>参照

[LinkedIn に関するよく寄せられる質問との Attract 統合](./attract-linkedin-faq.md)

[Attract から外部キャリア サイトへの求人の投稿](./posting-jobs-external.md)

[Microsoft Dynamics 365 Talent - Attract の LinkedIn Recruiter を使用した候補者のソーシング](./attract-linkedin-recruiter.md)

[Attract でジョブ求人の作成、承認、および投稿](./creating-jobs-attract.md)

[LinkedIn と Microsoft Dynamics 365 Talent - Attract との統合のトラブルシューティング](./attract-troubleshoot-linkedin.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]