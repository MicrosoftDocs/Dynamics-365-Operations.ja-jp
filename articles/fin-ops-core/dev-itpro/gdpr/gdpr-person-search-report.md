---
title: 個人検索レポート
description: この記事では、財務と運用アプリの個人データ レポートに関する情報を提供します。
author: josaw1
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b254d16755e4f6af0917658559db4480620b3fd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284526"
---
# <a name="person-search-report"></a>個人検索レポート

[!include [banner](../includes/banner.md)]

個人検索レポートは、財務と運用アプリの既存のデータ管理フレームワークの機能を強化したものです。 データ管理フレームワークには、ユーザーと、ユーザーが財務と運用アプリケーションで割り当てられる可能性があるロールを定義するために使用される個人データを識別するために Microsoft が作成した、事前パッケージ化されたエンティティ セットが用意されています。 

> [!NOTE]
> レポートは、Dynamics 365 Finance、Supply Chain Management、コマース、および人事管理で使用できます。 Microsoft Dynamics AX 2012 では今のところレポートは使用できません。 個人検索レポートは、バージョン 8.0 で利用可能です。 レポートはバージョン 7.3 (毎月の更新プログラム 7.3.2 経由で配信)、バージョン 7.2 (KB 4132615 経由)、およびバージョン7.1 (KB 4132441 経由 ) でも使用できます。 個人検索レポートが定期的に更新される場合があります。 このレポートを使用する前に、すべての関連する修正プログラムを取得し、適用したことを確認する必要があります。 

グローバル アドレス帳を使用すると、データ モデルで関係者として説明されている人物のインスタンスを作成することができます。 

財務と運用データに、連絡先、顧客、ユーザー、作業者、またはその他の担当者を追加するとき、通常、その担当者のアドレス帳エントリの作成から開始します。 アドレス帳の各ユーザーは関係者と呼ばれ、PartyID が割り当てられます。 担当者は、顧客、ユーザー、または作業者などのシステム内でのロールも保有して、CustID、UserID、WorkerID、および場合によりその他の ロール ID を持ちます。

![アドレス帳の構造。](../../fin-ops/organization-administration/media/address-book-structure.png)

時には、入力して説明するのに使用されている情報を確認したり、またはユーザーが正しいことを識別する場合があります。 データを要求したデータ件名と情報を共有すると便利な状況が生じることもあります。 個人検索レポートは、これらの両方のタスクに役立ちます。

個人検索レポートは拡張可能です。 既存のエンティティに探しているすべての個人データが含まれていないことがわかった場合、それらを拡張することができたり、新しいエンティティを上書きすることができます。 さらに、各エンティティのデータ マッピングを変更して、エクスポートしないフィールドを削除することができます。

担当者検索レポートでは、CustomerID または VendorID などのユーザー用のさまざまな ID を指定できます。 指定した人物にのみ関連する個人データを収集、フィルターして、エンティティ コレクション セットに設定します。

あまりないことですが、1 人のユーザーがシステムに複数回入力される場合があります。 個人検索レポートを使用すると、1 つのレポートに含める各担当者インスタンスを指定できます。 たとえば、Fred Smith という名前のユーザーは、「Fred Smith」および「F」の両方である可能性があります。 D。 アドレス帳の "Smith"。

個人がデータに複数の関係者として存在する可能性があります。 当事者のタイプごとに複数の識別子を提供することができます。各当事者のタイプの個人データは単一のレポートに含まれます。

## <a name="download-the-default-template"></a>既定のテンプレートのダウンロード

個人のテンプレートには、情報をダウンロードするために使用されるエンティティの一覧が含まれます。 テンプレートは、個人検索レポートを使用する前にロードする必要があります。 テンプレートは、バージョン 7.2 以降のデータ管理のテンプレート フォームからロードすることができます。 **データ管理** からテンプレートをダウンロードするには、次の手順を実行します。 

1. **データ管理** ワークスペースを開きます。
2. ワークスペースが初めて開かれた場合は、すべてのデータ エンティティが読み込まれます。 テンプレートをロードする前に、すべてのデータ エンティティをロードする必要があります。
3. **テンプレート** タイルをクリックします。
4. **既定のテンプレートの読み込み** ボタンを選択します。
5. **個人検索** を選択します。
6. **選択済の読み込み** をクリックします。

LCS からテンプレートをダウンロードすることも、7.1 以降のバージョンのインポートすることもできます。 そのためには、次の手順を実行します。
1.  LCS にログインします。
2.  **共有資産ライブラリ** タイルをクリックします。
3.  **データ パッケージ資産** タイプを選択します。
4.  **テンプレート -x.x- 個人の検索** (x.x は現在お使いのアプリケーションのバージョン) という名前のテンプレートをクリックしてダウンロードします。
5.  **データ管理** ワークスペースを開きます。
6.  ワークスペースが初めて開かれた場合は、ワークスペースはすべてのデータ エンティティを読み込みます。 すべてのエンティティは、テンプレートをダウンロードする前に読み込まれます。
7.  **テンプレート** タイルでクリックします。
8.  **個人検索** と呼ばれる新しいテンプレートを作成します。
9.  **テンプレートのインポート** をクリックします。
10. テンプレートを参照して、**アップロード** をクリックします。
11. テンプレートをインポートするには、**OK** をクリックします。


## <a name="generate-a-person-search"></a>個人検索を生成します

個人検索レポートを使用するには、次のタスクを実行する必要があります。

1.  システム管理メニューから個人検索リスト ページを開き、新しい検索を作成します。

    ![個人検索リスト ページ。](../media/gdpr-person-search-list-page.png)

2.  検索には、ID、名前、アドレスの 3 つのオプションがあります。 必要な検索のタイプを追加します。

    ![検索の定義。](../media/gdpr-define-search.png)

3.  結果を表示するために検索を実行します。

4.  結果が有効であることを確認します。 レポートに含めたくない情報を返してくる選択を解除します。

    ![検索結果の確認。](../media/gdpr-review-search-results.png)

5.  **プロセス レポート** を選択し、担当者検索テンプレートを選択します。

    ![レポートの処理。](../media/gdpr-process-report.png)

6.  **OK** を選択します。 データ パッケージが生成されます。

7. パッケージが生成されたら、選択したデータ形式でそれをエクスポートします。 

> [!NOTE]
> レコードに添付されたドキュメントは、データ エクスポートに含まれません。 添付ファイルは手動でダウンロードし、個人データを要求した各個人と共有する必要があります。


## <a name="additional-resources"></a>その他のリソース

GDPR の詳細については、[欧州連合の Web サイト](https://europa.eu/)、[Microsoft Trust Center](https://www.microsoft.com/TrustCenter/Privacy/gdpr/default.aspx) および[一般データ保護規則の概要](./gdpr-guide.md) の情報を参照してください。


### <a name="disclaimer"></a>免責事項
(c)2019 Microsoft Corporation. All rights reserved. このドキュメントは、"現状のまま" 提供されます。 URL およびその他のインターネット Web サイトの参照を含む、このドキュメントの情報および見解は、予告なしに変更することがあります。 このドキュメントの使用上のリスクは、すべてユーザーが負うものとします。 このドキュメントは、Microsoft の製品に含まれる知的財産に対する法律上の権利をお客様に付与するものではありません。 内部での参照を目的とする場合、このドキュメントをコピーして使用できます。 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
