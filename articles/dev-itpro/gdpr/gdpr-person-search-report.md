---
title: "個人検索レポート"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations の個人データ レポートについて説明します。"
author: rschloma
manager: AnnBe
ms.date: 01/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 21a933fd242791d03a3cc44ebdfa7b8de1baa11b
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="the-person-search-report"></a>個人検索レポート

[!INCLUDE [banner](../includes/banner.md)]

担当者検索レポートは、Microsoft Dynamics 365 for Finance and Operations の既存のデータ管理フレームワークの機能強化です。 データ管理フレームワークには、担当者と、担当者が Finance and Operations で割り当てられる可能性があるロールを定義するために使用される個人データを識別するために Microsoft が作成した、事前パッケージ化されたエンティティ セットが用意されています。 

> [!Note]
> 個人検索レポートは、今後のリリースで使用可能になります。 使用可能な場合、Finance and Operations、Microsoft Dynamics 365 for Retail、および Microsoft Dynamics 365 for Talent でレポートを使用することができます。 このトピックの Finance and Operations への参照は、Retail と Talent にも当てはまります。 このレポートは現在、Microsoft Dynamics AX 2012 では使用できません。 

Finance and Operations のグローバル アドレス帳を使用すると、データ モデルで関係者として説明されている人物のインスタンスを作成することができます。 

Finance and Operations データに、連絡先、顧客、ユーザー、作業者、またはその他の担当者を追加するとき、通常、その担当者のアドレス帳エントリの作成から開始します。 アドレス帳の各ユーザーは関係者と呼ばれ、PartyID が割り当てられます。 担当者は、顧客、ユーザー、または作業者などのシステム内でのロールも保有して、CustID、UserID、WorkerID、および場合によりその他の ロール ID を持ちます。

![アドレス帳の構成](../../fin-and-ops/organization-administration/media/address-book-structure.png)

時には、入力して説明するのに使用されている情報を確認したり、または Finance and Operations のユーザーが正しいことを識別する場合があります。 データを要求したデータ件名と情報を共有すると便利な状況が生じることもあります。 個人検索レポートは、これらの両方のタスクに役立ちます。

個人検索レポートは拡張可能です。 既存のエンティティに探しているすべての個人データが含まれていないことがわかった場合、それらを拡張することができたり、新しいエンティティを上書きすることができます。 さらに、各エンティティのデータ マッピングを変更して、エクスポートしないフィールドを削除することができます。

担当者検索レポートでは、CustomerID または VendorID などのユーザー用のさまざまな ID を指定できます。 指定した人物にのみ関連する個人データを収集、フィルターして、エンティティ コレクション セットに設定します。

あまりないことですが、1 人のユーザーがシステムに複数回入力される場合があります。 個人検索レポートを使用すると、1 つのレポートに含める各担当者インスタンスを指定できます。 たとえば、Fred Smith という名前のユーザーは、「Fred Smith」および「F」の両方である可能性があります。 D。 アドレス帳の "Smith"。

個々が Finance and Operations のデータに複数の関係者として存在する可能性があります。 当事者のタイプごとに複数の識別子を提供することができます。各当事者のタイプの個人データは単一のレポートに含まれます。

個人検索レポートを使用するには、次のタスクを実行する必要があります。

1.  システム管理メニューから個人検索リスト ページを開き、新しい検索を作成します。

    ![個人の検索リスト ページ](../media/gdpr-person-search-list-page.png)

2.  検索には、ID、名前、アドレスの 3 つのオプションがあります。 必要な検索のタイプを追加します。

    ![検索の定義](../media/gdpr-define-search.png)

3.  結果を表示するために検索を実行します。

4.  結果が有効であることを確認します。 レポートに含めたくない情報を返してくる選択を解除します。

    ![検索結果の確認](../media/gdpr-review-search-results.png)

5.  **プロセス レポート** を選択し、担当者検索テンプレートを選択します。

    ![レポートを処理する](../media/gdpr-process-report.png)

6.  **OK**を選択します。 データ パッケージが生成されます。

7. パッケージが生成されたら、選択したデータ形式でそれをエクスポートします。 

> レコードに添付されたドキュメントは、データ エクスポートに含まれません。 添付ファイルは手動でダウンロードし、個人データを要求した各個人と共有する必要があります。

## <a name="additional-resources"></a>その他のリソース

GDPR の詳細については、[欧州連合の Web サイト](http://europa.eu/)、[Microsoft Trust Center](https://www.microsoft.com/en-us/TrustCenter/Privacy/gdpr/default.aspx) および [Microsoft Dynamics 365 for Finance and Operations の GDPR に関するガイド](./gdpr-guide.md) のトピックの情報を参照してください。


### <a name="disclaimer"></a>免責事項
(c)2018 Microsoft Corporation. All rights reserved. このドキュメントは、"現状のまま" 提供されます。 URL およびその他のインターネット Web サイトの参照を含む、このドキュメントの情報および見解は、予告なしに変更することがあります。 このドキュメントの使用上のリスクは、すべてユーザーが負うものとします。 このドキュメントは、Microsoft の製品に含まれる知的財産に対する法律上の権利をお客様に付与するものではありません。 内部での参照を目的とする場合、このドキュメントをコピーして使用できます。 

