---
title: LinkedIn の統合に関するよく寄せられる質問
description: このトピックは、LinkedIn と Microsoft Microsoft Dynamics 365 Talent - Attract 間の統合に関する質問に回答します。
author: hasrivas
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 35428da709f480e1d3842b7e92deacba200326ee
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833095"
---
# <a name="linkedin-integration-faq"></a>LinkedIn の統合に関するよく寄せられる質問

[!include [banner](includes/banner.md)]

LinkedIn は、世界最大規模のオンライン プロフェッショナル ネットワークです。 Microsoft Dynamics Talent: Attract と LinkedIn の統合により、世界の優秀な人材にアクセスできるようになります。 Attract では、ジョブを LinkedIn に直接転記したり、LinkedIn から Attract へ候補者情報を作成することもできます。

## <a name="for-recruiters-and-hiring-managers"></a>採用担当者および採用マネージャー向け

ここでは Attract と LinkedIn を一緒に使う方法に関して、よく寄せられる質問とその回答を示します。

### <a name="what-linkedin-features-do-i-get-with-attract"></a>Attract で、どの LinkedIn 機能を利用できますか。

LinkedIn との Attract 統合により、次のタスクを実行できます。

- [LinkedIn にジョブを転記](./attract-post-jobs-to-linkedin.md) (無料の制限付き一覧として)。
- [Microsoft Dynamics 365 Talent - Attract の LinkedIn Recruiter を使用した候補者のソーシング](./attract-linkedin-recruiter.md#export-linkedin-candidates-to-attract-with-one-click).
- [Microsoft Dynamics 365 Talent - Attract の LinkedIn との統合の設定](./attract-admin-linkedin.md#set-up-apply-with-linkedin-in-attract).

### <a name="what-do-i-need-before-i-can-post-jobs-to-linkedin"></a>ジョブを LinkedIn に転記する前に何が必要ですか。

管理者は、[Attract の LinkedIn 統合をコンフィギュレーション](./attract-admin-linkedin.md#configure-job-posting-to-linkedin) をする必要があります。 その後、準備ができました。

### <a name="how-do-i-post-jobs-to-linkedin-from-attract"></a>Attract から LinkedIn へ、どのようにジョブを転記しますか。

Attract にジョブを作成した後、LinkedIn に対応する**今すぐ転記**ボタンを選択するだけです。 詳細については、[Microsoft Dynamics 365 Talent - Attract から LinkedIn にジョブを転記](./attract-post-jobs-to-linkedin.md#post-jobs-to-linkedin) を参照してください。

### <a name="can-i-get-candidate-information-from-linkedin-into-attract"></a>Linkedln から Attract に応募者情報を取得できますか。

はい。 LinkedIn に良い候補者が表示された場合、Attract に応募者の情報を簡単にエクスポートすることができます。 詳細については、[Microsoft Dynamics 365 Talent - Attract での、LinkedIn Recruiter を使用した候補者のソーシング](attract-linkedin-recruiter.md) を参照してください。

### <a name="how-can-i-get-help-accessing-linkedin-from-attract"></a>Attract から LinkedIn にアクセスする方法を教えてください。

サイン インまたは Attract から LinkedIn へのジョブ転記に問題がある場合は、[LinkedIn と Microsoft Dynamics 365 Talent - Attract の統合に関するトラブルシューティング](./attract-troubleshoot-linkedin.md) を参照してください。

その他の問題については、[Microsoft Dynamics 365 Talent のサポートを取得](./talent-support.md) を参照してください。 LinkedIn のヘルプについては、[Linkedln サポート ページ](https://www.linkedin.com/help) を参照してください。

## <a name="for-admins-and-developers"></a>管理者および開発者向け

ここでは Attract と LinkedIn 間の統合をコンフィギュレーションする方法に関して、よく寄せられる質問とその回答を示します。

### <a name="how-do-i-configure-attract-so-that-recruiters-and-hiring-managers-can-post-jobs-to-linkedin"></a>採用担当者および採用マネージャーが LinkedIn にジョブを転記できるようにするには、どのようにして Attract をコンフィギュレーションしますか。

使用可能なオプションを、管理者センターの **LinkedIn 統合**タブでコンフィギュレーションできます。 詳細については、[Microsoft Dynamics 365 Talent - Attract への LinkedIn の統合の設定](./attract-admin-linkedin.md) を参照してください。

### <a name="can-i-export-candidate-information-from-linkedin"></a>Linkedln から応募者情報をエクスポートできますか。

はい、しかし LinkedIn Recruiter との統合を最初にコンフィギュレーションする必要があります。 詳細については、[Microsoft Dynamics 365 Talent - Attract への LinkedIn の統合の設定](./attract-admin-linkedin.md) を参照してください。

### <a name="how-can-i-post-jobs-to-premium-job-slots-on-linkedin"></a>LinkedIn のプレミアム ジョブ スロットにジョブを転記するにはどうすればよいですか。

たとえ Attract にて、LinkedIn にジョブを転記する強力なソリューションを提供しても、追加の柔軟性が必要になる場合があります。 たとえば、無料の制限付き一覧に加えて、プレミアム ジョブ スロットを転記できるようにしたり、LinkedIn でバッチ ジョブの転記を 1 日に複数回も処理するように設定したりすることができます。

#### <a name="types-of-linkedin-job-posts"></a>LinkedIn のジョブ転記のタイプ

LinkedIn では、次のタイプのジョブを転記できます。

- **制限付き一覧** - 候補者が LinkedIn と会社の LinkedIn ページでジョブを検索すると、検索結果で表示される無料ジョブ転記。 制限付き一覧は、有効な求職者を対象にしています。 このタイプの一覧は、Attract が LinkedIn に提供されるタイプです。 LinkedIn で制限付き一覧のジョブを昇格することはできません。 制限付き一覧を昇格したい場合は、LinkedIn を使用して求人ラッピングを有効にする必要があります。 求人ラッピングに関する詳細については、[求人ラッピングにおける制限付き一覧対プレミアム ジョブ スロット](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping) および [求人ラッピング プラス - よく寄せられる質問](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions) を参照してください。
- **プレミアム ジョブ スロット** - Linkedln フィード、電子メール、および**関心のあるジョブ**など、Linkedln のさまざまな場所に表示される購買済み転記。 プレミアム ジョブ スロットは、受動的な候補者を対象としていますが、ジョブ検索にも表示されます。

Attract では、制限付き一覧として LinkedIn にジョブを転記します。 プレミアム ジョブ スロットを使用する場合は、LinkedIn Recruiter で求人ラッピングを使用する必要があります。 求人ラッピングには、LinkedIn を使用した求人ラッピング契約が必要です。 詳細については、[LinkedIn Recruiter を介して求人ラッピング](https://www.linkedin.com/help/recruiter/answer/79037) を参照してください。

#### <a name="frequency-of-batch-processing-on-linkedin"></a>LinkedIn でのバッチ処理の頻度

LinkedIn は、1 日に 1 回 Attract からバッチでジョブ転記が行われます。 したがって、Attract から転記された後、LinkedIn でジョブが表示されるまでに最大 48 時間かかることがあります。 LinkedIn でより早くジョブを表示する必要がある場合や、追加の柔軟性が必要な場合は、LinkedIn から Recruiter System Connect アプリケーション プログラミング インターフェイス (API) を使用できます。 詳細については、[Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect) を参照してください。

#### <a name="table-of-options-for-job-posting-to-linkedin"></a>LinkedIn に転記するジョブ オプションの一覧

次の表では、LinkedIn にジョブを転記するためのさまざまなオプションについて説明します。 ここには、各オプションの利点と追加情報が含まれています。

|  | Attract | LinkedIn Recruiter から求人ラッピング | Recruiter System Connect API |
|---|---|---|---|
| **説明** | Attract では、XML フィードとして LinkedIn にジョブを転記します。 | 会社は LinkedIn と契約しており、ジョブを転記するための XML フィードを提供しています。 | 顧客は、この API を使用して、Attract と LinkedIn Recruiter 間の情報を同期します。 |
| **どのタイプのジョブを転記できますか。** | 制限付き一覧 | プレミアム ジョブ スロットまたは制限付きリスト | 制限付き一覧 |
| **ジョブを LinkedIn で昇格することはできますか。** | いいえ | プレミアム ジョブ スロット: はい<br>制限付き一覧: いいえ | いいえ |
| **LinkedIn がどのくらいの頻度でジョブを転記しますか。** | 1 日 1 回 | 1 日 1 回 | API によって定義されているように 1 日に複数回 |
| **LinkedIn で推奨されましたか。** | いいえ | はい | いいえ |
| **何が必要ですか。** | Attract の購買 | LinkedIn との求人ラッピング契約とプレミアム ジョブ スロットの購入 | LinkedIn との API 契約 | 
| **どこで詳細情報を得られますか。** | [Microsoft Dynamics 365 Talent - Attract の LinkedIn との統合の設定](./attract-admin-linkedin.md) | [LinkedIn Recruiter から求人ラッピング - 概要](https://www.linkedin.com/help/recruiter/answer/79037) | [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect) |

> [!NOTE]
> Attract でジョブを Linkedln に転記する LinkedIn Recruiter System Connect ライセンスは必要ありません。

## <a name="see-also"></a>参照

[Microsoft Dynamics 365 Talent - Attract の LinkedIn との統合の設定](./attract-admin-linkedin.md)

[Microsoft Dynamics 365 Talent - Attract から LinkedIn への職務の投稿](./attract-post-jobs-to-linkedin.md)

[Microsoft Dynamics 365 Talent - Attract の LinkedIn Recruiter を使用した候補者のソーシング](./attract-linkedin-recruiter.md)

[LinkedIn と Microsoft Dynamics 365 Talent - Attract との統合のトラブルシューティング](./attract-troubleshoot-linkedin.md)
