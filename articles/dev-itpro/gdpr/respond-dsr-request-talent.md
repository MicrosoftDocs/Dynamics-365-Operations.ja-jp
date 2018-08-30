---
title: "Talent での個人データ要求に対応"
description: "このトピックでは、データ コントローラとして Microsoft Dynamics 365 for Talent をデータ プロセッサとして使用して、欧州連合のGDPR (General Data Protection Regulation) に基づくデータ要求に対応する方法について説明します。"
author: shielasogge
manager: AnnBe
ms.date: 01/31/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: rschloma
ms.search.scope: Operations
ms.custom: 10031
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 0b10765f7517c183745decf3e1d676487621b563
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---


# <a name="respond-to-requests-for-personal-data-in-talent"></a>Talent での個人データ要求に対応

[!include [banner](../includes/banner.md)]

このトピックは、Microsoft Dynamics 365 for Talent を使用する企業と、パートナーおよび独立系ソフトウェア ベンダー (ISV) がデータ主体の権利 (DSR) 要求に適合しているとき、それらの両方の企業に役に立ちます。 欧州連合の一般データ保護規則 (GDPR) および Microsoft が提供する関連するリソースの詳細については、[Microsoft Dynamics 365 for Finance and Operation の GDPR に関するガイド](./gdpr-guide.md) を参照してください。

Talent で、Microsoft はプロセッサとして動作します。 データ プロセッサとして、 Talent はデータ コントローラとしての GDPR 責務に適応させるプロセスと機能を提供します。

## <a name="rights"></a>権限

データ主体は GDPR の下で次の権限を持ち、データ コントローラーは DSR 要求に応じて各権限の下にリストされている行動のいずれかをとることができる。 

### <a name="right-to-view"></a>表示するには右

+ 担当者検索レポートを使用して、DSR 要求の対象となる個人データを検索および収集します。 このレポートの使用の詳細については、[個人検索レポート](gdpr-person-search-report.md) トピックを参照してください。  
+ 高度な検索とフィルターを使用して、特定の個人データを検索し、Microsoft Office のエクスポート機能を使用してそのデータをエクスポートします。
+ 既存のエンティティを追加して、担当者検索レポートを拡張します。 レポートを拡張するのに役立つ情報の詳細については、[独自のデータで個人検索レポートを拡張](gdpr-extend-person-search-report.md) を参照してください。

### <a name="right-to-modify"></a>修正するには右\*

+ 高度な検索とフィルターを使用して修正すべきデータを見つけ、Talent で直接データを修正します。

\* 個人データと見なされるデータの一部は、製品または機能で直接変更することはできません。 このデータは通常、財務法 (税法など)、詐欺防止 (セキュリティ監査証跡)、または業界認定への準拠のために「現状のまま」保たれる金融取引やその他の業務データの一部です 。 コントローラーとして、不正確または未完了の個人データを修正する責任があります。

### <a name="right-to-be-forgotten"></a>消去するには右\*

+ 製品が直接アクションを有効にする場所では、個人データを削除または消去することができます。 コントローラーとして、データ主体の要求が消去された個人データが、支払証明または税の証明などのデータ保持に関する組織のその他のコンプライアンス責務と競合しないようにする必要があります。

\* 個人データと見なされるデータの一部は、製品または機能で直接変更することはできません。 このデータは通常、財務法 (税法など)、詐欺防止 (セキュリティ監査証跡)、または業界認定への準拠のために「現状のまま」保たれる金融取引やその他の業務データの一部です 。 コントローラーとして、不正確または未完了の個人データを修正する責任があります。

### <a name="right-to-port"></a>移植するには右
次のオプションは、データ権利要求に応じて個人データを転送するのに役立ちます。 

+ Microsoft Office アドインを使用して、個人データをエクスポートします。
+ 個人データのエクスポートを可能にするカスタム レポートを作成します。
+ 人物検索レポートを使用または拡張して、データ対象者の個人データのコピー要求に役立つ情報を収集します。

### <a name="right-to-restrict-processing"></a>処理を制限するには右

+ たとえば、コースから従業員を削除します。
+ 組織の法的なカウンセリングからのガイダンスに従い、その他の法律または産業委任に準拠するための会社により、必要なデータの処理を制限する権限を会社が拒否する可能性があります。

## <a name="additional-notes-that-apply-to-requests-for-personal-data"></a>個人データの要求に適用される追加のメモ

+ Microsoft Power BI で見つかる個人データは、Talent で入力される情報から生成され、レポート目的でそのアプリケーションに転送されます。 Talent の情報から、レポート、Excel にエクスポートおよび個人検索レポートなどのツールを使用して個人データの要求を満たす必要があります。 DSR 要求を満たすために Power BI から追加の報告を行う必要はありません。 
+ Talent は、レコードに関連付けられたドキュメントをエクスポートしません。 これらの添付ファイルは、手動でダウンロードし、DSR を作成した個人と共有する必要があります。
+ トランザクション データがマスター レコードに関連付けられている場合、レコードは削除できません。 
+ 同様に、転記済または完了済みのトランザクションは削除できません。

### <a name="reasons-why-certain-personal-data-may-not-be-modified-or-deleted-in-talent"></a>Talent で特定の個人データを変更または削除できない理由

次のテーブルは、特定のシナリオで個人データの変更または削除が制限される理由を示しています。

| 理由 | コメント |
|--------|---------|
| 財務、税金、一般会計原則 (GAAP) | 関係者を削除することはできませんが、関係者の名前は更新できます。 |
| 財務、税、GAAP | 現在の作業者のデータは削除できませんが、作業者の名前を更新することはできます。 | 
| GAAP | 転記済または完了済みトランザクションは変更できません。 |

## <a name="additional-information"></a>追加情報

退職済作業者のみ Talent から削除できます。 退職済従業者を削除するには、これらの手順に従います。

+ 作業者職位を削除します。 

    職位の割り当てを削除するには、**作業者** ページで **職位の割り当て** を選択します。 **次の日の時点** および **すべてのレコードを表示** を選択します。 位置番号をドリルインするには、**タイムラインの変更** &gt; **変更の管理** &gt; **職位作業者割り当て**を選択し、削除している作業員に割り当てられている位置の割り当てレコードを削除します。

+ 固定報酬を削除します。

    固定報酬を削除するには、**作業者** ページで **雇用履歴** を選択します。 **雇用履歴** &gt; **雇用** &gt; **固定報酬** を選択し、作業者の固定報酬プランを削除します。

+ 変動報酬登録を削除します。

    変動報酬を削除するには、**作業者** ページで **雇用履歴** を選択します。 **雇用履歴** &gt; **雇用** &gt; **変動報酬プラン登録** を選択し、作業者の変動報酬プランの登録を削除します。

+ 関連付けられている任意のチェックリストを削除します。

    チェックリストを削除するには、**作業者** ページで **チェックリスト** オプションを選択します。

補償は契約者に割り当てられません。 したがって、これらのステップは、前のプロセスでスキップすることができます。

管理者は <https://attract.talent.dynamics.com/personreport> を介して Microsoft Dynamics 365 for Talent:Attract および Microsoft Dynamics 365 for Talent: Onboarding で個人データを検索およびエクスポートできます。

## <a name="additional-resources"></a>その他のリソース
GDPR の詳細については、[欧州連合の Web サイト](http://europa.eu/) および [Microsoft Trust Center](https://www.microsoft.com/en-us/TrustCenter/Privacy/gdpr/default.aspx) を参照してください。



### <a name="disclaimer"></a>免責事項
(c)2018 Microsoft Corporation. All rights reserved. このドキュメントは、"現状のまま" 提供されます。 URL およびその他のインターネット Web サイトの参照を含む、このドキュメントの情報および見解は、予告なしに変更することがあります。 このドキュメントの使用上のリスクは、すべてユーザーが負うものとします。 このドキュメントは、Microsoft の製品に含まれる知的財産に対する法律上の権利をお客様に付与するものではありません。 内部での参照を目的とする場合、このドキュメントをコピーして使用できます。

