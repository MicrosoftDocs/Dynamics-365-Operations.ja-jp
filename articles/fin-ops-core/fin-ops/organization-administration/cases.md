---
title: ケース管理の概要
description: このトピックでは、Microsoft Dynamics AX での、計画、追跡、分析などのケース管理の概要を示します。
author: kfend
ms.date: 11/20/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CaseDetail
audience: IT Pro
ms.reviewer: sericks
ms.custom: 23541
ms.assetid: 4aa0a2da-be45-4dc3-97bf-b84bcf83144c
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ccfc192def2fadf6c408f2b007377260ae28cd4
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984417"
---
# <a name="case-management-overview"></a>ケース管理の概要

[!include [banner](../includes/banner.md)]

ケースの計画、追跡、および分析を行うことで、同様の問題に使用できる効率的な解決策を作成できます。 たとえば、顧客サービス担当者または一般人事担当者がケースを作成することで、より効率的に対処するのに役立つ情報をナレッジ記事で検索できるようになります。 次の例は、組織内のさまざまな状況でケースをどのように使用できるかを示しています。

## <a name="example-how-fabrikam-uses-cases-for-customers-in-the-private-sector"></a>例: Fabrikam 社における民間部門の顧客に対するケースの使用方法

Fabrikam 社の顧客サービス担当者の Lisa が、Fabrikam 社の顧客の Lionel から電話連絡を受けます。 Lionel は、Fabrikam 社が彼の楽器店に設置した新しいサウンド システムの音量レベルを正しく設定できずに困っています。 Lisa は、Lionel に関するケースを作成し、**音量** というカテゴリを割り当てます。 次に、Lisa は優先順位を上げ、ケースに当日対応のサービス レベル アグリーメント (SLA) を割り当てます。 

また、Lisa はケース ログにケースの詳細を入力します。 Lisa は、**音量** カテゴリに関連付けられているナレッジ記事がいくつかあり、その内の 3 件がケースの解決に役立ったとマークされていることに気づきます。 Lisa は、それぞれの記事を開き、解決策を Lionel と相談しますが、新しいサウンド システムで Lionel が抱えている問題には、どの解決策でも対応できません。 Lisa は、音響技術者が 24 時間内に Lionel に電話して問題を解決する作業を行うことを Lionel に伝えます。 

Lisa は、ケースを有効化して一連の活動内容を作成します。 さらに、音響開発チームのメンバーの Terrence に、その活動を割り当てます。 Terrence は、新しい活動が自分に割り当てられていることを発見します。 Terrence は、そのケースを開き、ケース ログでケースに関する情報に目を通します。 Terrence は、前日も同じ問題に対応し、その解決策を作成しています。 Terrence は、Lionel に連絡して問題のこの解決策を伝えます。 また、ケース詳細に入力します。 

Terrence は、自分の解決策で問題に対処できたため、他の人が同じ問題に直面した際に使用できるよう、解決策を文書化することにします。 Terrence は、ドキュメントを **ナレッジ記事** ページに追加して **音量** カテゴリに割り当て、有効な解決策であることを他の Fabrikam 社の従業員が分かるように、手動でランク付けを上げます。 Terrence はケースを次のレベルに引き上げます。 ケースを引き上げることにより、顧客サービス部門の品質保証の担当者である Marie に対して、新しい活動が作成されます。 

Marie は、新しい活動が自分に割り当てらたことを発見し、その活動に関連付けられているケースを開きます。 Marie は、ケースとケースの詳細に目を通して、ケースに対して正しいプロセスが実行されたことを確認します。 Marie は、実際のケース対応時間が SLA で見積もられた概算時間を上回らなかったことを確認します。 さらに、Marie は Terrence が顧客に連絡したこと、および問題点が解決されたことをメモします。 Marie は、顧客が受けた対応とケースの解決に満足します。 また、決済済としてケースを終了します。 Marie がケースを終了すると、自分に割り当てられていた未解決活動も終了します。

## <a name="example-how-city-power--light-uses-cases-for-customers-in-the-public-sector"></a>例: City Power & Light 社における公共部門の顧客に対するケースの使用方法

City Power & Light 社の顧客サービス担当者 Annie は、City Power & Light 社が市の住民から電話連絡を受けます。 Annie は、電話連絡を活動として記録し、通話内容をメモします。 住人は、自分の家に電気がきていないことを Annie に伝えます。 Annie は City Power & Light が問題をできるだけ早く調査、検索、解決することを住人に通知します。 

次に、Annie はケースの作成と、、電話連絡とケースの関連付けを行い、サービス注文を作成します。 Annie は他の住民が停電を報告するために電話する可能性が高いことを知っています。 したがって、顧客サービスのセンターの混乱を回避し、時間を節約するため、Annie は、問題が発生したこと、およびケースとサービス注文を作成したことを、顧客サービス担当者にグループ インスタント メッセージ (IM) で報告します。 Annie は、ケース番号とサービス注文番号を IM に記載します。 その後、City Power & Light 社が停電に関する電話連絡をさらに受けた場合、顧客サービス担当者は、個々の電話連絡に対して活動を作成し、既存のケースに割り当てることができます。

## <a name="example-how-fabrikam-uses-cases-for-employees"></a>例: Fabrikam 社における従業員に対するケースの使用方法

次のシナリオは、異なる場所で働く Fabrikam 社の一般人事担当者が、従業員の問題を処理する際に使用できるケース管理の方法を示しています。

### <a name="in-great-britain"></a>英国内

Fabrikam 社のイギリス部門を担当する一般人事担当者の Christine が、Fabrikam 社の従業員の Peter から電話連絡を受けます。 Peter は、息子が生まれてすぐの 9 週間前に、源泉徴収税の被扶養者の数を変更したことを Christine に伝えます。 Peter の目的は、変更内容がまだ有効になっていない理由を問い合わせることです。 Christine は Peter に関するケースを作成します。 また、Peter の税金情報を確認し、Peter が被扶養者情報を入力したものの、新しい源泉徴収税の開始日を選択していないことを発見します。 Christine は、開始日を選択して変更を再提出する旨の電子メール メッセージを Peter に送ります。 Peter は、Christine のメッセージに返信して、開始日を選択して変更を再提出したことを伝えます。 Christine は、Peter からの電子メール メッセージをケース レコードに添付し、変更が適切に行われて再提出されことを確認してからケースを終了します。

### <a name="in-the-united-states"></a>米国での事例

Fabrikam 社の米国部門を担当する一般人事担当者の Luke が、Fabrikam 社の従業員の Shannon から電子メールを受け取ります。 Shannon は、6 か月前に仕事で怪我をした機械オペレータです。 それ以降、Shannon は医療費の支払を求めて Humongous Insurance 社とやりとりを行っています。 Shannon はこの問題について 4 週間前に Luke に連絡したので、ケースはすでに作成されました。 Shannon の新しい電子メール メッセージには、Humongous Insurance 社からまだ電話連絡がないことが記載されています。 Luke は、既存のケースを開いて Shannon の電子メール メッセージをドキュメントとして追加し、ケース ログに目を通します。 Luke は、このケースを作成した際に、それに **保険** というカテゴリを割り当てました。 Luke は今、**保険** カテゴリに関連付けられている新しいナレッジ記事があることを発見します。 Luke は、ナレッジ記事を読み、Humongous Insurance 社の電話システムが更新中で、すべての電話が使えないことを知ります。 この記事には、保険会社がすべての顧客に電子メール メッセージを送信したものの、保険会社の電子メール システムに問題があるために一部の顧客にメッセージが届かなかったことが記載されています。 有効な保険金を請求中のすべての顧客は Humongous Insurance 社に電子メールまたは郵便で照会を依頼するよう要請しています。 Luke は、保険金請求を解決する方法を記載した電子メール メッセージを Shannon に送ります。 また、ナレッジ記事を役立つ情報のソースとしてランク付けします。 Luke は、保険金請求が解決するのを見届けるため、Shannon と Humongous Insurance 社の両方を今後 4 週間フォローアップできるように別の活動を自分に対して作成します。 4 週間後、Luke は Shannon に連絡します。 Luke は Humongous Insurance 社が Shannon の請求を支払い、彼女がその解決策に満足していることを知ります。 Luke が、ケースのステータスを **解決済み** に変更します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]