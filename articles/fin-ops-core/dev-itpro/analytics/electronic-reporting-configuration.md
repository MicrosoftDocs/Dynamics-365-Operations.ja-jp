---
title: 電子申告 (ER) コンフィギュレーションの作成
description: この記事では、電子レポートを使用しての構成の作成に役立つ背景情報を提供します。
author: kfend
ms.date: 02/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: f2bc07a2c91a23eea55be25a0525308d8663ecc1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285563"
---
# <a name="create-electronic-reporting-er-configurations"></a>電子申告 (ER) コンフィギュレーションの作成

[!include [banner](../includes/banner.md)]

ローカライズおよび翻訳向け Microsoft Dynamics Lifecycle Services (LCS) ソリューションの要件の一部として、ローカライズ ISV ソリューション プロバイダーは電子申告ツールの使用によって国/地域別機能またはソリューション固有機能を実装する必要があります。 この記事では、電子レポートを使用しての構成の作成に役立つ背景情報を提供します。 この記事は、利用可能な電子レポートドキュメントと今後の電子レポートドキュメントを置き換えるものではありませんが、ローカリゼーション要件の観点から見た補足的なものです。

電子申告 (ER) は、次の 3 つの概念に基づいて、規制による電子申告と支払を作成および管理するのに役立つ、コンフィギュレーション可能なツールです。
 - コーディングの代わりになるコンフィギュレーション
 - 複数の Dynamics 365 Finance リリースで使用する 1 つの構成
 - 簡単または自動的にアップグレード


ER は、LCS を使用して、Microsoft やパートナーが他のパートナーや顧客に電子ドキュメントのコンフィギュレーションを配布する際の単一の共通の方法を提供します。 ER によって、固有の業務要件用にパートナーや顧客が、電子ドキュメントの形式をカスタマイズ、アップグレード、配布することも容易になります。

ER を使用して、ドメイン固有でデータベースに依存しないデータ モデルをドキュメント形式のデータ ソースとして設定できます。 フォーマットは、Excel に似た簡単なビジュアル ツールを使用して、これらのドメインに固有のデータ モデルに基づいて、コンフィギュレーションされます。 データ モデルとフォーマットはバージョン管理をサポートし、フォーマットは有効日になります。


### <a name="main-data-flow"></a>主要データ フロー

[![GER 主要データ フロー。](./media/ger-main-data-flow.jpg)](./media/ger-main-data-flow.jpg)

### <a name="data-model-configuration-creation"></a>データ モデル コンフィギュレーションの作成

可能な限り、Microsoft によってリリースされているデータ モデルを再利用およびカスタマイズするか、必要とされるエンティティとその関係の抽象モデルを導入するビジネス ドメイン領域固有のデータ モデルを作成することをお勧めします。 この方法で、Microsoft によってリリースされる今後の更新プログラムと調整するか、少なくとも異なるシナリオまたは国/地域で必要なさまざまな形式の複数のドメイン固有電子ドキュメントのデザインおよび管理においてモデルを再利用できます。

#### <a name="design-the-data-model-of-the-created-model-configuration"></a>作成されたモデルのコンフィギュレーションのデータ モデルを設計する

データ モデルは、必要なビジネス エンティティと選択したドメイン内でそれらの関係を認識し、説明するように設計されています。 データ モデルは、データ コンテナー (レコード) を使用して、エンティティを表現する記述子で構成されます。 エンティティのプロパティは、データの項目を使用して表現されます。 レコードの定義は、フィールド (データの品目) を含むエンティティです。 各データ項目には固有の名前、ラベル、説明、および値があります。 各データ項目の値は、文字列、整数、実数、日付、列挙型などとして認識されるように設計されています。 また、値は別のレコードまたはレコード リストになる場合があります。 1 つのレコード定義は、データ モデルのルートとして選択できます。 (ルートとは、データ ソース マッピングのモデル全体の開始点です)。この場合、モデルは、1 つの事前定義されたデータ フローによって、データを提供するデータ ソースとして使用されます。 レコードの定義が、データ モデルのルート ディレクトリとして選択されていない場合、データ モデルには、ルートとして形式マッピング ステージに割り当てることができるレコードの定義が含まれます。 このようなモデルのデータ フローは、形式の性質に応じて、複数の方法でデータソースとして定義できます。 たとえば、単一のデータ モデルは、支払ドメイン領域用に設計されます。 このデータ モデルには、法人としての会社、仕入先や顧客、支払いのためのデータ レコード定義を含めることができます。 ただし、形式の性質に従って、データは次の方法で表示される必要があります: 支払人 &gt; 受取人 &gt; 支払。 したがって、単一のデータ モデルでは、次の代替パスに従ってデータを提供できます。

- 企業レコード定義がルートとして選択されている場合、買掛金勘定ドメインの 会社 &gt; 仕入先 &gt; 支払いを選択します。
- 顧客レコード定義がルートとして選択されている場合、売掛金勘定ドメインの顧客 &gt; 会社 &gt; 支払いを選択します。

### <a name="format-configuration-creation"></a>フォーマット構成の作成

デザインする新しい電子的な形式の抽象データを保持するために作成される、データ モデル構成を使用します。 新しいフォーマットを作成するときに以前に準備したデータ モデルを使用する場合は、**構成の作成** の **データ モデルに基づくフォーマット** オプションを選択します。 フォーマットのコンフィギュレーションをしたら、フォーマット構造を定義する必要があります。 構造は、XML ファイルまたは Excel テンプレートのサンプルをインポートすることによって、手動または自動で作成できます。 親構成のデータ モデルは、適切なルート コンテナーと共に形式マッピング用に自動的に提供されます。 ただし、形式によって特定の方法でデータを表すことを必須とする場合があります。 したがって、数式デザイナーを使用して、データ コンテナーの仮想データ項目 (計算項目) として式を定義することができます。

> [!NOTE]
> 形式コンポーネントを、テーブルやデータ エンティティ、列挙型、または ER のクラスやオブジェクトなどのデータベースおよびアプリケーション コンポーネントに直接マップすることができますが、この方法はお勧めしません。 同じデータ ソースを使用する一部のビジネス ドメイン領域で、複数の形式が管理される可能性があります。 データベース コンポーネントの構造を変更するたびに、それらのデータベース コンポーネントに対する形式マッピングも変更する必要があります。 これらの変更の原価には、保守している形式の数が乗じられます。 したがって、ドメイン固有のデータ構造の抽象的な記述としてデータ モデルを操作し、単純化と特定のカスタマイズのカバレッジのため、フォーマット要素の直接バインディングをデータベース コンポーネントに使用することをお勧めします。 たとえば、限定された数の保守された形式でこれらの参照が必要な場合に、直接バインディングを使用してカスタム テーブルを参照します。

> [!TIP]
> それでも実行時にデータベースおよびアプリケーション コンポーネントにアクセスする形式コンポーネントを構成するために ER データ ソースを追加する必要がある場合、**形式デザイナー** ページのアクション ウィンドウで **詳細を表示** を選択します。

## <a name="version-control"></a>バージョン管理
電子申告のデザインの背後にある原則の 1 つは、カスタマイズされた拡張メンテナンス モデルを使用して、データ モデルとフォーマットを同時に簡単に配分できることです。 すべてのコンフィギュレーションのバージョン管理、および既存のカスタマイズを 「複製」 してローカライズまたはカスタマイズの実装のための新しいコンフィギュレーションを派生させることができます。 たとえば、Proseware, Inc という名前で表される会社が、Litware, Inc. という会社のサービスにサブスクライブしました。その会社はコンフィギュレーションを返しおよびその中ですべての法的要件をサポートするイントラスタットを提供します。 Litware 社から特定の構成をデータ モデルおよび形式とともに既に受け取っており、それらを配置済みです。 会社は、連邦の要件に加えて、次の地域の要件をサポートする必要がある地域で業務しています。

- イントラスタット トランザクションの詳細の一部として、XML ファイルは他の場所では必要ない統計手順のコードを表示する必要があります。
- イントラスタット返品ヘッダー ブロックに記載されている会社名の長さを 200 文字に制限する必要があります。

これらの要件をサポートし、地方自治体の規制に準拠するためには、これをローカライズ構成として実装する必要があります。 ただし、元のコンフィギュレーションとのリンクを保持しておく必要があり、それにより元のコンフィギュレーションの新しいバージョンとして連邦レベルで導入される将来の変更を採用できるようになります。 したがって、LCS から Litware Inc. の元の設定をインポートし、それを新しいローカライズされた構成として派生させ、必要な変更を導入します。ローカライズされたフォーマットの最初のバージョンを導入してこの作業を完了し、それを内部的に使用し始めます。 Litware 社が、元の構成の新しいバージョンを提供するときはいつでも、マイクロソフトはそのバージョンを LCS からインポートし、ローカライズ構成をこのバージョンにリベースし、新しい連邦要件をサポートするための変更を採用し、次のバージョンのローカライズされた形式を導入することによってこの作業を完了し、それを引き続き内部で使用します。

> [!NOTE]
> 任意のコンフィギュレーションのドラフト・バージョンは、次のような追加アクションのためにローカルで使用可能になる前に「完了」しておく必要があります。
>
> - 新しい形式からのデータ ソースとして参照できるようにします。
> - 構成のインポート/エクスポートなどを使用して、企業またはインスタンス間の構成交換を有効にします。

## <a name="electronic-reporting-domain-coverage"></a>電子申告ドメイン補充
複数の標準コンフィギュレーションは、特定の国/地域の電子レポート要件を満たすために使用できます。 次のリストは、ビジネス ドメインにグループ化された形式のコンフィギュレーションの例を示しています。 使用可能かつサポートされている構成の完全な最新リストを入手するには、構成リポジトリ セットアップを開いて、リソースまたは LCS 資産ライブラリからインポートできる構成を表示します。 

- 監査ファイル

    - FEC
    - GDPdU...

- 支払 (ISO20022)

    - SEPA CT
    - SEPA DD
    - JBA
    - BACS...

- 統計レポート

    - EU イントラスタット...

- 税務報告書

    - CIS
    - BAS
    - ELSTER
    - EU 販売リスト...

- 顧客の E-Invoice

    - OIOUBL...
    
## <a name="your-solution-uptake"></a>ソリューションの取得
電子レポート機能を ER に移動する方法を選択することができます。 ただし、移動を計画する際には、次の高レベルの手順を検討する必要があります。

1. 現在ソリューションが提供している電子レポート機能を確認します。
2. 支払および電子請求書などのソリューションの対象となるドメイン領域を識別します。
3. Microsoft 提供のコンフィギュレーションを確認します。 ベースとして使用できるコンフィギュレーションが見つかることがあります。 たとえば、ソリューションが SEPA CT 支払形式をカスタマイズする場合、SEPA CT コンフィギュレーションを拡張する必要があります。
4. 既存のモデルまたは形式、または新しいモデルまたは形式のいずれかに基づく新しいコンフィギュレーションを作成します。
5. ユーザーがレポートの実行時に選択する必要がある入力パラメータと、レポートの内容の検証を定義します。
6. 算術、文字列、データ、または他の利用可能な Excel のような関数を使用して、モデルとのマッピングを定義します。
7. 該当する場合は、ラベルと翻訳をさまざまな言語に定義します。
8. 名前付き範囲を持つテンプレートを定義し、必要に応じて Excel レポートの構成からリンクを設定します。

## <a name="terminology"></a>用語

| 相談                 | 定義 |
|----------------------|------------|
| ER                  | 電子申告は、政府機関、銀行、および他の関係者と情報交換するための電子申告の作成を簡略化するエンジンです。 現在、電子レポートはテキスト、XML および OpenXML スプレッドシート形式書式をサポートしており、より多くの形式をサポートするために拡張機能インターフェイスを提供します。 |
| 変換       | データのソースで行う必要がある典型的なアクションが形式に出力として送信される前に、変換を導入し、形式コンポーネントにアタッチすることができます。 変換は、1 つの値をパラメーターとし、別の値を返す ER フォーミュラです。 たとえば、スペースを含む多くの形式フィールドがあり、フィールドがエクスポートされる際、スペースはスペースごとに置換される必要があります。 この場合、ジョブを実行するために、文字列の引数を取得して REPLACE 関数を使用する変換を作成できます。 文字列コンポーネントを作成して、その変換に関連付けることができます。 |
| データ モデル           | データ モデルは、データの構造体を提供します。 この構造体は、このドメインの報告要件を満たすために、特定のビジネス ドメイン領域を詳細に抽象的に記述するために使用されます。 |
| 構成        | 管理および実行可能で、バージョン管理をサポートするデータ ソースへのマッピングと組み合わせるデータのモデルまたは形式のいずれかのコンテナーです。 構成は、財務と運用のインスタンス間で電子ドキュメント形式の交換を整理するためにインポートまたはエクスポートされるエンティティです。 |
| 派生アクション        | 新しい構成を作成する基準として既に存在しているコンフィギュレーションを使用する工程です。 |
| 再ベース アクション        | 新しいバージョンの基本構成で導入された変更を使用して派生したコンフィギュレーションを更新する工程です。 バージョン番号は、リベース初期化段階で選択されます。 |
| 更新の競合      | リベース アクション中に検出された競合。新しいベース バージョンには派生のバージョンで調整されている形式/マッピング要素 (名前、プロパティなど) の調整も含まれています。 |
| 再配置競合  | リベース アクション中に検出された競合。新しいベース バージョンには派生のバージョンで調整されている形式/マッピング要素 (名前、プロパティなど) の調整も含まれています。 |
| 重複競合 | リベース アクション中に検出された競合。新しいベース バージョンには派生バージョンにも入力されている要素と同じ形式要素 (つまり、同じ名前と子コンポーネントを持つ) が導入されています。 |

## <a name="additional-resources"></a>追加リソース

[電子申告 (ER) の概要](general-electronic-reporting.md)

[電子申告 (ER) コンフィギュレーション ライフサイクルの管理](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

