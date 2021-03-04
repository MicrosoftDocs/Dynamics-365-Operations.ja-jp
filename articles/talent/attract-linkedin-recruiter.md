---
title: Attract の LinkedIn Recruiter を使用した候補者のソーシング
description: Microsoft Dynamics 365 Talent - Attract が提供する LinkedIn 統合を使用して、LinkedIn Recruiter から職務候補者をソース化します。
author: andreabichsel
manager: AnnBe
ms.date: 08/31/2020
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
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 96e4660c4958bf5f2a0910bfad770e1e713f800f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528272"
---
# <a name="source-candidates-with-linkedin-recruiter-in-attract"></a>Attract の LinkedIn Recruiter を使用した候補者のソーシング

[!include [banner](includes/banner.md)]

LinkedIn は世界最大のオンライン プロフェッショナル ネットワークで、世界の最高の人材へのアクセスを提供します。 Microsoft Dynamics 365 Talent: Attract では LinkedIn から直接候補者をソース化できます。 したがって、空いている職位を埋めるために必要な人材を見つけるのはこれまで以上に簡単です。 Attract を通じて LinkedIn との接続を設定した後、ワンクリックで職位の LinkedIn 候補者を表示し、Attract にエクスポートできます。

この機能がないようであれば、管理者にお問い合わせください。Attract から LinkedIn Recruiter を利用する前に、管理者は [LinkedIn との統合を設定](./attract-admin-linkedin.md) する必要があります。 その後、LinkedIn Recruiter との接続を設定し、候補者の検索を開始できます。

>[!IMPORTANT]
>2020 年 7 月 1 日現在、LinkedIn は Internet Explorer 11 をサポートしていません。 ユーザーはまだ Internet Explorer 11 を使用して LinkedIn にアクセスできますが、アップグレードするか別のブラウザーを使用するかを確認するメッセージが表示されます。 詳細については、[サポートされている LinkedIn 用インターネット ブラウザー](https://www.linkedin.com/help/linkedin/answer/4135/supported-internet-browsers-for-linkedin) を参照してください。

## <a name="set-up-your-connection-with-linkedin-recruiter"></a>LinkedIn Recruiter との接続の設定

Attract を通じて LinkedIn Recruiter で作業を開始する前に、LinkedIn Recruiter との接続を設定する必要があります。 このステップでは、LinkedIn Recruiter の資格情報が必要です。

1. ページの右上隅にある **設定** ボタン (ギア アイコン) を選択します。
2. **ユーザー設定** を選択します。
3. **接続** タブで、**LinkedIn** の横にある **接続** を選択します。 LinkedIn が提供する指示に従ってください。

    ![[Attract から LinkedIn Recruiter への接続の設定](./media/attract-set-up-linkedin-recruiter-connection.png)](./media/attract-set-up-linkedin-recruiter-connection.png)

## <a name="view-linkedin-candidates-in-attract"></a>LinkedIn の候補者を Attract で表示する

LinkedIn Recruiter に接続すると、候補者の LinkedIn プロファイルを Attract で表示できます。

>[!NOTE]
>採用者のシートが割り当てられている場合は、完全な情報を閲覧することができます。<br><br>
>採用マネージャーのシートを所有している場合や、何もシートが割り当てられていない場合は、Attract で候補者の LinkedIn タブに移動する前に必ず LinkedIn または LinkedIn Recruiter からサインアウトしてください。 候補者の基本のパブリック プロファイル データ (姓、名など) を確認できるようになります。

1. Attract で、左側にある **職務** または **人材プール** を選択してから、申請者を選択します。

    ![[LinkedIn の候補者を Attract で表示する](./media/attract-view-linkedin-candidates.png)](./media/attract-view-linkedin-candidates.png)

2. 候補者のプロファイルで、**LinkedIn** タブを選択します。候補者のプロファイルと InMail 履歴を表示できます。

   ![候補者の LinkedIn 情報の表示](./media/attract-candidate-linkedin-tab.png)

ここでは、実行できるアクションは次のとおりです。

- **採用活動** タブを選択して、次の情報を表示します。
   
   - 採用担当者メモ (パブリックとプライベートの両方)。 既定では、メモはプライベートになり、メモの所有者にのみ表示されます。
   - InMail 活動 (InMail コンテンツは除く)。 ページの下部までスクロールして、見込顧客との InMail のやり取りを表示し、見込顧客とやり取りしている組織内の他のユーザーを表示します。
   - 候補者の拒否活動

- **InMail を送信** を選択して、Attract を離れずに InMail を送信します。

- **ジョブに保存** を選択すると、Attract を離れずにジョブを保存することができます。

> [!NOTE]
> 候補者の Attract 情報が LinkedIn の情報と一致すると、候補者の LinkedIn プロファイルが Attract に表示されます。 使用される照合ルールは次のとおりです。
> 
> 1. 電子メール アドレスと LinkedIn メンバーID が Attract と LinkedIn で一致すると、候補者のプロファイルが表示されます。 候補者は、LinkedIn プロファイルを Attract からリンクまたはリンク解除するオプションを引き続き使用できます。
> 2. 電子メール アドレスまたは LinkedIn メンバー ID が一致しない場合は、可能性のある候補者の一覧が表示されます。 その後、リスト内の候補を選択し、プロファイルをリンクできます。
> 3. 良好な一致がない場合は、一致が見つからなかったことが通知されます。

## <a name="export-linkedin-candidates-to-attract-with-one-click"></a>LinkedIn 候補者をワンクリックで Attract にエクスポートする

LinkedIn Recruiter で候補者を確認している間は、現在 Attract で開いている職務に候補者をエクスポートできます。 このステップでは、Attract の採用担当者または採用マネージャーのアクセス許可が必要です。 Attract でのロールの詳細については、[Attract でのセキュリティおよびロールの管理](https://docs.microsoft.com/dynamics365/unified-operations/talent/security-attract) を参照してください。

また、職務に候補者ステージがあることを確認する必要があります。 詳細については、[候補者活動](./activities-attract.md#prospect-activity) を参照してください。

1. Attract で職務を作成し、適切なロールを割り当てた後、職務をアクティブにします。
2. LinkedIn Recruiter で、その職務に適した候補者を見つけ、候補者のプロファイルに移動します。
3. 連絡先カードの職務検索ボックスで、タイトルまたは Attract で有効の職務 ID を使い職務を検索します。 職務が見つからない場合は、**変更 ATS** を選択して正しい Attract インスタンスを検索します。
4. 職務を選択してから、**エクスポート** を選択します。
5. Attract で、職務を開きます。 エクスポートされた候補者は、職務の **候補者** タブに表示されます。

## <a name="view-attract-information-in-linkedin-recruiter"></a>LinkedIn Recruiter で Attract の情報を表示する

LinkedIn Recruiter では、候補者が組織内の他の職務に応募したかどうか追跡し、候補者が求人応募のさまざまなステージでどこにいるかを確認し、Attract からのフィードバックとコメントを表示できます。

1. LinkedIn Recruiter を開いて、候補者プロファイルを選択します。
2. **In ATS** をポイントします。
3. Attract に格納されている候補者情報を表示するには、次のいずれかのオプションを選択します。

    - **Jobs & Statuses** – 候補者が所属する職務、最新の状態、および各職務における候補者の進捗状況を確認します。
    - **面接フィードバック** – 面接者が Attract で送信したフィードバックを参照します。
    - **注記** – Attract でこの候補者に対して入力されたメモを確認します。

    ![[LinkedIn Recruiter から Attract 情報を表示する](./media/attract-view-information-from-linkedin-recruiter.png)](./media/attract-view-information-from-linkedin-recruiter.png)

> [!NOTE]
> 候補者が過去の候補者のステージに移動していない場合、候補者と応募のデータは LinkedIn Recruiter とは同期されません。

## <a name="view-linkedin-talent-pools"></a>LinkedIn 人材プールの表示

候補者が LinkedIn プロファイルを組織内の任意のユーザーと共有することに同意した場合、新しい候補者レコードが Attract に作成されます。 これらの候補者は、システムで作成された LinkedIn 人材プールに表示されます。

1. Attract で、左側にある **人材プール** を選択します。
2. LinkedIn 人材プールを選択します。 LinkedIn から候補者とそのスタブ プロファイルの一覧が表示されます。 候補者が共有することを選択した場合、スタブ プロファイルには候補者の姓名と電子メール アドレスが含まれます。

## <a name="see-also"></a>参照

[LinkedIn に関するよく寄せられる質問との Attract 統合](./attract-linkedin-faq.md)

[Microsoft Dynamics 365 Talent - Attract の LinkedIn との統合の設定](./attract-admin-linkedin.md)

[Attract でジョブ求人の作成、承認、および投稿](./creating-jobs-attract.md)

[Microsoft Dynamics 365 Talent - Attract から LinkedIn への職務の投稿](./attract-post-jobs-to-linkedin.md)

[LinkedIn と Microsoft Dynamics 365 Talent - Attract との統合のトラブルシューティング](./attract-troubleshoot-linkedin.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]