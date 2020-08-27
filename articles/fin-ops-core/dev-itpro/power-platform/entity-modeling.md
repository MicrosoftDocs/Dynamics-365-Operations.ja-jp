---
title: エンティティ モデリング
description: このトピックでは、Finance and Operations エンティティの仮想エンティティを使用したリレーショナル モデリングの概念について説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 07/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-05-31
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 3326b9c4d99bc3f2d4f1bedc6220b1c2c61a950f
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621422"
---
# <a name="entity-modeling"></a>エンティティ モデリング

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> この機能を使用するには、Finance and Operations アプリのバージョン 10.0.12 が必要ですが、Common Data Service にはサービス更新 189 が必要です。 Common Data Service のリリース情報は、[最新バージョンの利用可能性](https://docs.microsoft.com/business-applications-release-notes/dynamics/released-versions/dynamics-365ce#all-version-availability)ページに発行されています。

> Finance and Operations 仮想エンティティの Common Data Service メタデータで公開されるパブリック エンティティ名は、Finance and Operations エンティティの物理名を使用します。 これは、Finance and Operations アプリの OData メタデータによって公開されるエンティティのパブリック名とは異なる場合があります。

アプリを作成するには、アプリで使用されているエンティティの間でリレーショナル モデリングを実行する機能が必要です。 仮想エンティティのコンテキストでは、Common Data Service の仮想エンティティとネイティブ エンティティが連携して、目的のユーザー エクスペリエンスを実現する必要があります。 このトピックでは、Finance and Operations の仮想エンティティを使用して実装できるリレーショナル モデリングの概念について説明します。

## <a name="generating-virtual-entities"></a>仮想エンティティの生成

既定では、Finance and Operations アプリの仮想エンティティは Common Data Service に存在しません。 ユーザーは、Finance and Operations のリンクされたインスタンスで使用可能なエンティティを表示するために、カタログ エンティティを照会する必要があり ます。 カタログから、ユーザーは 1 つ以上のエンティティを選択し、Common Data Service が仮想エンティティを生成するように要求できます。 この手順については、後のセクションで説明します。

## <a name="entity-fields"></a>エンティティ フィールド

Finance and Operations エンティティに対して仮想エンティティが生成されると、システムによって Common Data Service の対応する仮想エンティティの Finance and Operations エンティティに各フィールドが作成されます。 理想的なケースでは、Finance and Operations と Common Data Service の間でサポートされるデータ型が一致していない場合、両方のエンティティで同じフィールドの総数が同じになり ます。 サポートされているデータ型については、Finance and Operations のプロパティに基づいて Common Data Service のフィールド プロパティが設定されます。

このセクションの残りの部分では、サポートされるデータ型とサポートされていないデータ型について説明します。 Common Data Service にあるフィールドの詳細については、[フィールドの概要](https://docs.microsoft.com/powerapps/maker/common-data-service/fields-overview)を参照してください。

| Finance and Operations のデータ型 | Common Data Service のモデル化されたデータ型 |
|-------------------------------------|------------------------------------------|
| 実績                                | 実数<br><br>考えられる不一致の詳細については、次の表を参照してください。</p> |
| 長い                                | 精度が 0 (ゼロ) に等しい 10 進数 |
| Int                                 | 整数 |
| 文字列 (memo 以外), 文字列 (memo)    | 文字列 – 1 行のテキスト、文字列 – 複数行テキスト |
| UtcDateTime                         | DateTime (DateTimeFormat.DateAndTime, DateTimeBehavior.TimeZoneIndependent)<br><br>Finance and Operations における空の日付 (1900 年 1 月 1 日) は、Common Data Service では null 値として表されます。 |
| 日                                | DateTime - (DateTimeFormat.DateOnly, DateTimeBehavior.TimeZoneIndependent)<br><br>Finance and Operations における空の日付 (1900 年 1 月 1 日) は、Common Data Service では空の値として表されます。 |
| Enum                                | 候補リスト<br><br>Finance and Operations 列挙 (列挙型) は、Common Data Service ではグローバル OptionSet として生成されます。 システム間のマッチングは、値の**外部名**プロパティを使用して行われます。 Common Data Service における列挙型整数値は、システム間で固定されているとは限りません。 したがって、これらの列挙型にも固定 ID が含まれていないので、依存することは避けてください (特に Finance and Operations の拡張可能な列挙型の場合)。 OptionSet を使用するエンティティが更新されると、OptionSet メタデータが更新されます。 |

Finance and Operations における *real* および *long* データ型のフィールドは、Common Data Service で *decimal* データ型としてモデル化されます。 2 つのデータ型の間では、精度と小数点部桁数の不一致があるため、次の動作を考慮する必要があります。

| ユース ケース                                     | 結果の動作 |
|----------------------------------------------|--------------------|
| Common Data Service のほうが精度が高くなります。    | メタデータが同期していない場合、このユース ケースは発生しません。 |
| Finance and Operations のほうが精度が高くなります。 | 読み取り操作時は、Common Data Service では、値が最も近い精度値に丸められます。 値が Common Data Service で編集された場合、Finance and Operations では、値が最も近い精度値に丸められます。 書き込み操作中は、Common Data Service で指定された値が書き込まれます。これは、Finance and Operations がより高い精度をサポートするためです。 |
| Common Data Service のほうがスケールが大きくなります。        | 該当なし |
| Finance and Operations のほうがスケールが大きくなります。     | Common Data Service には Finance and Operations 値が表示されます (1000 億を超える場合でも)。 ただし、精度は低下します。 たとえば、987,654,100,000,000,000 は Common Data Service では "987,654,099,999,999,900" として表示されます。 このフィールドの値を Common Data Service で編集した場合、Common Data Service 検証により、値が最大値を超えてから値が Finance and Operations に送信されるというエラーがスローされます。 |

Common Data Service では、以下の Finance and Operations のデータ型はサポートされていません。 Finance and Operations エンティティのこれらのデータ型のフィールドは、Common Data Service の対応する仮想エンティティで使用できるようになりません。 これらのデータ型のフィールドを Open Data Protocol (OData) アクションのパラメーターとして使用した場合は、それらのアクションを対応する仮想エンティティで使用することはできません。 OData アクションの詳細については、このトピックで後述する [OData アクション](#odata-actions)のセクションを参照してください。

- AnyType
- BLOB
- クラス
- コンテナー
- Guid
- レコード
- 時刻
- UserType
- VarArg
- Void (OData アクションの Void 戻り値の型はサポートされています)。

Common Data Service でサポートされているが、Finance and Operations ではサポートされていないデータ型は、Finance and Operations の仮想エンティティではサポートされません。

## <a name="entity-keyprimary-key"></a>エンティティ キー/主キー

Finance and Operations では、エンティティはエンティティ キーとしてさまざまなデータ型の 1 つ以上のフィールドを持つことができます。 エンティティ キーは、Finance and Operations エンティティのレコードを一意に識別します。 さらに、エンティティのレコードは、Int64 型のレコード ID 主キーによって一意に識別できます。

Common Data Service では、主キーは常にグローバル一意識別子 (GUID) になります。 GUID ベースの主キーを使用すると、Common Data Service 内のエンティティ内のレコードを一意に識別できます。

Finance and Operations と Common Data Service の間のインプリメンテーション ギャップを埋めるため、Finance and Operations の仮想エンティティの主キーは GUID です (Common Data Service に準拠するため)。 この GUID は、最初の 4 バイトのデータ エンティティ ID と、最後の 8 バイトとしてエンティティ内のルート データ ソースのレコード ID で構成されます。 この設計では、GUID をエンティティ キーとして使用するという Common Data Service の要件が満たされています。 また、テーブル ID とレコード ID を使用して、Finance and Operations のエンティティ レコードを一意に識別することもできます。

## <a name="primary-field"></a>基本フィールド

Common Data Service では、各エンティティに基本フィールドが必要です。 このフィールドには、文字列型の単一のフィールドを指定する必要があります。 基本フィールドは、次の場合に Common Data Service で使用されます。

- エンティティに対して作成される既定のビューには、基本フィールドがあります。
- エンティティのクイック ビュー フォームには、基本フィールドが含まれています。
- 別のエンティティへのルックアップがページに追加され、基本フィールドのデータが表示されます。

Common Data Service の基本フィールドの使用に基づき、Finance and Operations の仮想エンティティの基本フィールドは、Finance and Operations の対応するエンティティのエンティティ キーを使用するように設計されてい ます。

Common Data Service の基本フィールドには文字列型のフィールドが 1 つしかないことが想定されているのに対し、Finance and Operations ではさまざまなデータ型の複数のフィールドを持つことができます。 文字列は、連結され、パイプ (\|) によって区切られており、最大 255 文字です。 255 文字を超える値はすべて切り捨てられます。 基本フィールドを表すこの仮想エンティティ フィールドの名前は、**mserp\_primaryfield** になります。

## <a name="relations"></a>リレーション

> [!IMPORTANT]
> 仮想エンティティとネイティブ エンティティを横断する書き込みトランザクションには対応していません。 整合性の確保を保証する方法がないため、この形式のトランザクションは使用しないことを推奨します。

Finance and Operations エンティティのリレーションは、1 対多 (1: n) または多対 1 (n:1) のリレーションとしてモデル化されます。 これらのリレーションは、Common Data Service の仮想エンティティのリレーションシップとしてモデル化されています。 多対多 (n:n) のリレーションは、Finance and Operations ではサポートされていないことに注意してください。

たとえば、Finance and Operations では、エンティティ A がエンティティ B への外部キーを持っている場合、このリレーションは、Common Data Service の仮想エンティティ A で n:1 のリレーションシップとしてモデル化されます。 Common Data Service でのこのリレーションシップのスキーマ名は、名前付け規則 **mserp\_FK\_\<source entity name\>\_\<relation name\>** を使用します。 この名前付け規則では、最大文字列長が 120 文字になっています。 スキーマ名が 120 文字を超える名前を生成するリレーションは、Common Data Service の仮想エンティティで生成されません。

このリレーションシップの外部名は、名前付け規則 **FK\_\<relation name\>** を使用します。 外部名は、Finance and Operations に送信されるクエリが作成されるときの Finance and Operations におけるリレーションを決定するために使用されます。

Common Data Service の仮想エンティティに対してリレーションシップが生成されると、そのルックアップタイプの新しいフィールドがソース エンティティにも追加されます。 前の例では、リレーションシップが作成されると、名前付け規則 **mserp\_fk\_\<target\_entity\>\_id** を使用した新しい検索フィールドがソース エンティティ A に追加されます。Finance and Operations のエンティティに複数のリレーションが存在する可能性があるため 、ソース仮想エンティティには、同じ数のルックアップ フィールド (関連エンティティごとに1つ) が作成されます。 このルックアップ フィールドがページまたはビューに追加されると、関連するエンティティの基本フィールドの値が表示されます。

Common Data Service の仮想エンティティ内のリレーションシップは、Common Data Service の仮想エンティティとしてに既にリレーション内の関連エンティティが存在する場合にのみ生成され ます。 前の例では、エンティティ B が Common Data Service の仮想エンティティとしてに存在しない場合、エンティティ A が仮想エンティティとして生成されたときに、エンティティ B へのリレーションがエンティティ A に作成されません。 このリレーションは、エンティティ B が仮想エンティティとして生成された場合にのみエンティティ A に追加されます。 したがって、Finance and Operations の仮想エンティティが生成されると、検証が行われ、生成される仮想エンティティに完全な機能と機能できるリレーションシップのみが生成されます。

要約すると、次のいずれかの理由により、別の Finance and Operations 仮想エンティティとのリレーションシップが仮想エンティティに存在しない場合があります。

- リレーションシップに参加している Finance and Operations エンティティは、仮想エンティティとして存在しません。
- リレーションシップの名前の長さは、120 文字を超えています。

Finance and Operations 仮想エンティティの一部が Common Data Service で生成されたときにエラーが発生した場合 、仮想エンティティはまったく作成されません。 上記のいずれかの理由でリレーションシップが存在しない場合は、エラーとは見なされません。

### <a name="native-entitytonative-entity-relationships"></a>ネイティブ エンティティ - ネイティブ エンティティ リレーションシップ

ネイティブ エンティティ - ネイティブ エンティティ リレーションシップは、関連するエンティティの GUID を使用してリレーションシップを解決する Common Data Service の標準機能です。 (この GUID はエンティティ キーです)。GUID によって、関連するエンティティの固有のエンティティ レコードが識別されます。

### <a name="virtual-entitytovirtual-entity-relationships"></a>仮想エンティティ - 仮想エンティティのリレーションシップ

2 つの Finance and Operations 仮想エンティティ間のリレーションシップは、Finance and Operations エンティティの関連メタデータによって駆動されます。 前に説明したように、これらのリレーションは、仮想エンティティが生成されたときに Common Data Service でリレーションシップとして生成されます。 Common Data Service のネイティブ エンティティの場合と同様、これらのリレーションシップでは GUID を使用して Finance and Operations のエンティティの固有レコードを識別します。 意味的には、Finance and Operations 仮想エンティティの GUID は、ネイティブ Common Data Service エンティティ上で GUID と同じように動作します。 Finance and Operations 仮想エンティティの GUID の実装に関する情報については、このトピックで前述した[エンティティ キー/主キー](entity-modeling.md#entity-keyprimary-key)セクションを参照してください。

前の例では、関連するエンティティの GUID はエンティティ B のエンティティ キーであり、Finance and Operation でレコードを識別するクエリを作成するために使用されます。 エンティティ A とエンティティ B のリレーションが使用されます。

したがって、実質的に、エンティティ名は、Finance and Operations から取得されるリレーションで使用される唯一の情報です。 エンティティ名によって、関連エンティティの基本フィールドにアクセスできるようになり、ルックアップにそのエンティティを表示できるようになります。 また、関連するエンティティの GUID にアクセスできるため、前に説明したように、他のクエリで使用することができます。 リレーションが Finance and Operations エンティティで構築される実際のフィールドは、まったく使用されません。

### <a name="virtual-entitytonative-entity-relationship"></a>仮想エンティティ - ネイティブ エンティティ リレーションシップ

前に説明したように、GUID は、ネイティブ Common Data Service エンティティ (ネイティブエンティティ - ネイティブエンティティ リレーションシップ) または Finance and Operations 仮想エンティティ (仮想エンティティ - 仮想エンティティ リレーションシップ) 内のレコードを一意に識別するために使用される唯一の情報です。 ただし、Common Data Service のアカウント A の販売注文を Finance and Operations から表示する例について考えてみましょう。 Common Data Service では特定のアカウントに対して販売注文をフィルター処理する必要があるので、このリレーションシップにおいて Finance and Operations に送信されるクエリには、Common Data Service のネイティブ アカウント エンティティの GUID に対する WHERE 句が含まれます。 ただし、Finance and Operations には Common Data Service のエンティティの GUID に関する情報が含まれていないため、クエリから販売注文が返されることはありません。 クエリが成功するのは、Finance and Operations が理解するフィールドに基づく条件を WHERE 句に指定している場合のみです。

したがって、Common Data Service のアカウント エンティティの GUID を Finance and Operations 内のフィールドに置き換えることで、Finance and Operations に送信されるクエリが販売注文の正しい一覧を返すようにすることができます。

この問題を解決して、仮想エンティティ - ネイティブ エンティティのリレーションシップが許可される豊富なシナリオ セットを実現するには、このタイプのエンティティにリレーションシップを追加します。 このリレーションは、仮想エンティティが同期されるときにリレーションシップとして表示されます。

上の例では、SalesOrderHeader 仮想エンティティとアカウント ネイティブエンティティの間のリレーションシップは、アカウント番号と会社フィールドに基づいている必要があります。 既定では、Common Data Service のネイティブ アカウント エンティティには会社フィールドがありません。 この例では、new_testcompany という会社ルックアップ フィールドを、ネイティブ アカウント エンティティに追加します。

次に、new_accountcompanyidx という名前の新しいキーを追加します。このキーは、accountnumber (new_testcompany) と Common Data Service におけるそのアカウント エンティティの固有の行を表します。

次の手順では、X++ でこのリレーションシップを定義します。 次の例は、サンプル X++ コードを示しています。 フィールド、インデックス、およびマッピングの情報の名前は、Common Data Service で作成されたフィールドとインデックスの名前と一致している必要があります。 この例では、"synthaccount" という名前のリレーションシップが、仮想 SalesorderHeader エンティティと Common Data Service 内のネイティブ アカウント エンティティの間に作成されます。 マップされたフィールドは、new_accountcompanyidx インデックスを構成します。 リレーションシップの表示名は @SYS11307 になります。 表示名の先頭に円記号があることを確認します。 これにより、ラベルがリレーションシップを定義して適切に変換されるようになります。

フィールド マッピングは、仮想エンティティのフィールドが、ネイティブ エンティティのフィールドにマップされていることを示します。 フィールド マッピングでは、キーが仮想エンティティ フィールドである、値がネイティブ エンティティ フィールドです。

```x++
[CDSVirtualEntitySyntheticRelationshipAttribute('synthaccount', 'account', 'accountcompanyidx', '\@SYS11307')]
    public static Map syntheticAccountRelationship()
    {
        Map fieldMapping = new Map(Types::String, Types::String);

        // Assumes the Common Data Service account entity has a key on [msdyn_accountnumber, msdyn_companyid]
        // Also assumes that the Common Data Service cdm_Company entity has a key on [msdyn_companycode]
        fieldMapping.insert(fieldStr(CDSVirtualEntityTestEntity, StringField), 'msdyn_accountnumber');
        fieldMapping.insert(fieldStr(CDSVirtualEntityTestEntity, DataAreaId), 'msdyn_companyid');

        return fieldMapping;
    }
```
次の手順では、仮想エンティティを生成または更新して、新しいリレーションシップを取得します。 仮想エンティティとネイティブ エンティティ間のリレーションシップは、作成された後 Common Data Service では更新できないことに注意してください。 更新を行う唯一の方法は、リレーションシップを物理的に削除し、エンティティを更新した後、問題を解決するためにそのエンティティを再度追加して再関連付けする方法です。

このリレーションシップは一般的な GUID ベースのリレーションシップに似ていますが、リレーションシップのクエリ フィルターをバッキング フィールドの制限に変換するための追加のメタデータがあります。 これで生成されたクエリには、Finance and Operations アプリが認識するフィールドに基づく WHERE 句が割り当てられ ます。 その後、クエリによって、フィルター処理された販売注文の一覧が正常に返されます。

### <a name="native-entitytovirtual-entity-relationships"></a>ネイティブ エンティティ - 仮想エンティティ リレーションシップ

<!--HERE-->ネイティブ エンティティ - 仮想エンティティ リレーションシップは、ネイティブ エンティティ - ネイティブ エンティティ リレーションシップと同じように機能します。 ユーザーが Finance and Operations の仮想レコードにネイティブ レコードを関連付けると、その仮想エンティティの GUID がネイティブ エンティティ レコードに保存されます。 既に説明したように、リレーションシップに参加するエンティティには、関連するエンティティの GUID フィールドが含まれます。 したがって、Common Data Service の見積が Finance and Operations 仮想エンティティ内の顧客に関連付けられている場合は、顧客の仮想エンティティの GUID が見積エンティティに保存されます。 この動作により、標準の Common Data Service 機能を使用してレコードを予想どおりに取得できます。

## <a name="enums"></a>列挙

Finance and Operations の列挙型は、Common Data Service の OptionSet としてモデル化されています。 Finance and Operations の仮想エンティティが生成されると、必要な列挙は OptionSet として生成されます。 OptionSet が既に存在する場合は、代わりに使用されます。

## <a name="company"></a>法人

Finance and Operations のエンティティは、会社にバインドすることも、グローバルにすることもできます。 会社にバインドされている Finance and Operations エンティティの仮想エンティティは、Common Data Service の cdm\_company エンティティとのリレーションシップを持ちます。 cdm\_company エンティティは、Common Data Service におけるネイティブ エンティティで あり、Dynamics365Company ソリューションの一部です。 通常と同様、リレーションシップが作成されると、関連するエンティティ (この場合は cdm\_company) の仮想エンティティにも検索フィールドが作成されます。 このルックアップ フィールドは **会社** という名前であり、ユーザーがリストの値を選択したり、関連するレコードの詳細に移動したりできるように、最適なユーザー エクスペリエンスを提供するために使用する必要があります。 **会社コード**と呼ばれるフィールドは、仮想エンティティにも追加されます。 この値は 4 文字の文字列です。 このフィールドは、プログラミングで使用する必要があります。

## <a name="attachments"></a>アタッチメント

Finance and Operations エンティティの添付ファイルは、エンティティごとにサポートされます。 たとえば、請求書ヘッダー エンティティは、[エンティティを通じて添付ファイルを有効](../../fin-ops/organization-administration/configure-document-management.md#how-can-attachments-be-extracted-from-the-system)にするために、請求書に関連する添付ファイル エンティティを実装します。

このタイプのエンティティは、Finance and Operations の対応する添付ファイル エンティティとのリレーションを持ちます。 したがって、これらは前に説明した他の関係と同じパターンに従います。 つまり、添付ファイル機能が実装されている Finance and Operations エンティティは、仮想エンティティを使用して添付ファイルを使用できるようにします。 添付ファイルをサポートしていない Finance and Operations エンティティは、Common Data Service で仮想化された添付ファイルもサポートしません。

Finance and Operations 仮想エンティティでサポートされるのは、添付ファイルの読み取りだけであることに注意してください。 現在、仮想エンティティを使用した添付ファイルの作成、更新、または削除はサポートされていません。

## <a name="odata-actions"></a>OData アクション

Finance and Operations エンティティの OData アクションは、Common Data Service のカスタム アクションとして使用できるようになります。 カスタム アクションと Common Data Service での使用方法の詳細については、[カスタム アクション](https://docs.microsoft.com/powerapps/developer/common-data-service/custom-actions)を参照してください。

次のタイプの入力パラメーターと出力パラメーターがサポートされています。 入力または出力パラメーターのタイプが異なる場合、OData アクションは Common Data Service の SDK メッセージとして表示されません。

- 整数
- 文字列
- Guid
- ブール値
- Date/Datetime

以下は、Finance and Operations エンティティでサポートされる OData アクションの例ですが、Common Data Service の対応する仮想エンティティではサポートされていません。

- RetailStoreTenderTypeTable.queryDistinctTenderTypeIdAndName (RetailStoreTenderTypeTable エンティティのコレクション)
- DocumentRoutingClientApp.syncPrinters (DocumentRoutingClientApp エンティティ)
- DocumentRoutingClientApp.updateJobStatus (DocumentRoutingJobStatus 列挙)
- DimensionCombination.getCombinationDisplayValue (LedgerJournalACType 列挙)

## <a name="labels-and-localization"></a>ラベルとローカライズ

Finance and Operations のエンティティ名やフィールド名など、メタデータに定義されているラベルは、Common Data Service で仮想エンティティが生成されたときに取得されます。 ラベルは、Common Data Service にインストールされている言語ロケールの一覧を渡すことによって取得されます。 Finance and Operations は、Common Data Service でラベル インスタンスを構築するために使用される、ロケール/値セットの一覧として各ラベルを返します。 エンティティの生成または更新時に存在する言語パックのみが含まれます。 また、Finance and Operations には翻訳が提供されたラベルのみが含まれます。 欠落している翻訳がある場合、ラベル ID に戻されます (**\@SYS:DataEntity** など)。 Common Data Service に新しい言語パックをインストールした後、その言語のラベルが Finance and Operations に存在する場合は、新しいラベル情報を取得するように既存のエンティティを更新する必要があります。

ランタイム ラベルは、現在のユーザー コンテキストの言語で返されます。 つまり、Finance and Operations でそのユーザーの UserInfo レコードに指定されている言語で返されます。 この動作は、エラー メッセージにも適用されます。

## <a name="error-handling"></a>エラー処理

Common Data Service の仮想エンティティを介してが呼び出されたときに、エンティティに対するビジネス ロジックの作成、読み取り、更新、および削除 (CRUD) を Finance and Operations が行い、バッキング テーブルが実行されます。 いずれかの例外が Finance and Operations 側でスローされた場合は、エラー ログの最後のメッセージが Common Data Service に戻され、Finance and Operations からのメッセージを含む InvalidPluginExecutionException 例外としてスローされます。 Finance and Operations コードはユーザーのコンテキストで実行されるため、エラー メッセージの言語は、Finance and Operations の UserInfo レコードで指定されている言語に基づきます。 Finance and Operations で情報ログに書き込まれたメッセージに対して例外が発生しなかった場合、Common Data Service には表示されません。

## <a name="calculatedunmapped-fields"></a>計算済み/マップ解除済みフィールド

Finance and Operations エンティティの計算されたフィールドとマップされていないフィールドは、Common Data Service の対応する仮想エンティティでも使用できます。
