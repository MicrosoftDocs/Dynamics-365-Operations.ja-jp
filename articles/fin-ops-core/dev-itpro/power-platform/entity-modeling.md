---
title: エンティティ モデリング
description: このトピックでは、Finance and Operations エンティティの仮想エンティティを使用したリレーショナル モデリングの概念について説明します。
author: Sunil-Garg
ms.date: 07/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-05-31
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 4eb281f0abc5450cada8eabfb2dcc920776487d2
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062073"
---
# <a name="entity-modeling"></a>エンティティ モデリング

[!include[banner](../includes/banner.md)]



> [!IMPORTANT]
> この機能を使用するには、財務と運用アプリのバージョン 10.0.12 が必要ですが、Dataverse にはサービス更新 189 が必要です。 Dataverse のリリース情報は、[最新バージョンの利用可能性](/business-applications-release-notes/dynamics/released-versions/dynamics-365ce#all-version-availability)ページに発行されています。

> Finance and Operations 仮想エンティティの Dataverse メタデータで公開されるパブリック エンティティ名は、Finance and Operations エンティティの物理名を使用します。 これは、財務と運用アプリの OData メタデータによって公開されるエンティティのパブリック名とは異なる場合があります。

アプリを作成するには、アプリで使用されているエンティティの間でリレーショナル モデリングを実行する機能が必要です。 仮想エンティティのコンテキストでは、Dataverse の仮想エンティティとネイティブ エンティティが連携して、目的のユーザー エクスペリエンスを実現する必要があります。 このトピックでは、Finance and Operations の仮想エンティティを使用して実装できるリレーショナル モデリングの概念について説明します。

## <a name="generating-virtual-entities"></a>仮想エンティティの生成

既定では、財務と運用アプリの仮想エンティティは Dataverse に存在しません。 ユーザーは、Finance and Operations のリンクされたインスタンスで使用可能なエンティティを表示するために、カタログ エンティティを照会する必要があります。 カタログから、ユーザーは 1 つ以上のエンティティを選択し、Dataverse が仮想エンティティを生成するように要求できます。 この手順については、後のセクションで説明します。

## <a name="entity-fields"></a>エンティティ フィールド

Finance and Operations エンティティに対して仮想エンティティが生成されると、システムは Dataverse に対応する仮想エンティティに Finance and Operations エンティティの各フィールドの作成を試みます。 理想的なケースでは、Finance and Operations と Dataverse の間でサポートされているデータ型に不一致がない限り、両方のエンティティでフィールドの総数が同じになります。 サポートされているデータ型は、Finance and Operations のプロパティを基に Dataverse のフィールド プロパティが設定されています。

このセクションの残りの部分では、サポートされるデータ型とサポートされていないデータ型について説明します。 Dataverse にあるフィールドの詳細については、[フィールドの概要](/powerapps/maker/common-data-service/fields-overview)を参照してください。

| Finance and Operations のデータ型 | Dataverse のモデル化されたデータ型 |
|-------------------------------------|------------------------------------------|
| 実績                                | 小数<br><br>考えられる不一致の詳細については、次の表を参照してください。</p> |
| 長い                                | 精度が 0 (ゼロ) に等しい 10 進数 |
| Int                                 | 整数 |
| 文字列 (memo 以外), 文字列 (memo)    | 文字列 – 1 行のテキスト、文字列 – 複数行テキスト |
| UtcDateTime                         | DateTime (DateTimeFormat.DateAndTime, DateTimeBehavior.TimeZoneIndependent)<br><br>Finance and Operations の空の日付 (1900 年 1 月 1 日) は、Dataverse では null 値として表されます。 |
| 日付                                | DateTime - (DateTimeFormat.DateOnly, DateTimeBehavior.TimeZoneIndependent)<br><br>Finance and Operations の空の日付 (1900 年 1 月 1 日) は、Dataverse では空の値として表されます。 |
| Enum                                | 候補リスト<br><br>Finance and Operations 列挙 (列挙型) は、Dataverse ではグローバル OptionSet として生成されます。 システム間のマッチングは、値の **外部名** プロパティを使用して行われます。 Dataverse における列挙型整数値は、システム間で固定されているとは限りません。 したがって、特に Finance and Operations の拡張可能な列挙型の場合は、これらの列挙型にも安定した ID がないため、これらに依存しないでください。 OptionSet を使用するエンティティが更新されると、OptionSet メタデータが更新されます。 |

Finance and Operations の *real* および *long* データ型のフィールドは、Dataverse の *decimal* データ型としてモデル化されます。 2 つのデータ型の間では、精度と小数点部桁数の不一致があるため、次の動作を考慮する必要があります。

| ユース ケース                                     | 結果の動作 |
|----------------------------------------------|--------------------|
| Dataverse のほうが精度が高くなります。    | メタデータが同期していない場合、このユース ケースは発生しません。 |
| Finance and Operations のほうが精度は高くなります。 | 読み取り操作時は、Dataverse では、値が最も近い精度値に丸められます。 値が Dataverse で編集されている場合は、Finance and Operations で最も近い精度の値に丸められます。 Finance and Operations はより高い精度をサポートしているため、書き込み操作中に、Dataverse で指定された値が書き込まれます。 |
| Dataverse のほうがスケールが大きくなります。        | 該当なし |
| Finance and Operations のほうがスケールは大きくなります。     | Dataverse は、1,000 億を超えている場合でも、Finance and Operations 値を示しています。 ただし、精度は低下します。 たとえば、987,654,100,000,000,000 は Dataverse では "987,654,099,999,999,900" として表示されます。 このフィールドの値が Dataverse で編集されている場合、Dataverse 検証では、Finance and Operations に送信される前に、値が最大値を超えていますというエラーがスローされます。 |

Finance and Operations の次のデータ型は、Dataverse ではサポートされていません。 Finance and Operations エンティティのこれらのデータ型のフィールドは、Dataverse の対応する仮想エンティティでは使用できません。 これらのデータ型のフィールドを Open Data Protocol (OData) アクションのパラメーターとして使用した場合は、それらのアクションを対応する仮想エンティティで使用することはできません。 OData アクションの詳細については、このトピックで後述する [OData アクション](#odata-actions)のセクションを参照してください。

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

Dataverse ではサポートされているものの Finance and Operations ではサポートされていないデータ型は、Finance and Operations の仮想エンティティではサポートされていません。

## <a name="entity-keyprimary-key"></a>エンティティ キー/主キー

Finance and Operations では、エンティティはエンティティ キーとしてさまざまなデータ型の 1 つ以上のフィールドを持つことができます。 エンティティ キーは、Finance and Operations エンティティ内のレコードを一意に識別します。 さらに、エンティティのレコードは、Int64 型のレコード ID 主キーによって一意に識別できます。

Dataverse では、主キーは常にグローバル一意識別子 (GUID) になります。 GUID ベースの主キーを使用すると、Dataverse 内のエンティティ内のレコードを一意に識別できます。

Finance and Operations と Dataverse の間の実装ギャップを埋めるために、Finance and Operations の仮想エンティティの主キーは GUID です (Dataverse に準拠するため)。  この GUID は、最初の 4 バイトのデータ エンティティ ID と、最後の 8 バイトとしてエンティティ内のルート データ ソースのレコード ID で構成されます。 この設計では、GUID をエンティティ キーとして使用するという Dataverse の要件が満たされています。 また、テーブル ID とレコード ID を使用して、Finance and Operations のエンティティ レコードを一意に識別することもできます。

Finance and Operations でエンティティを使用する場合、ルート データ ソースには常に一意の RecID があることを確認します。 このデザインに違反すると、Dataverse には対応する仮想エンティティに対して重複するGUID が表示されます。 集計ビューには一意の RecID がない可能性があるという同じ理由で、集計ビューは仮想エンティティ経由ではサポートされません。

## <a name="primary-field"></a>基本フィールド

Dataverse では、各エンティティに基本フィールドが必要です。 このフィールドには、文字列型の単一のフィールドを指定する必要があります。 基本フィールドは、次の場合に Dataverse で使用されます。

- エンティティに対して作成される既定のビューには、基本フィールドがあります。
- エンティティのクイック ビュー フォームには、基本フィールドが含まれています。
- 別のエンティティへのルックアップがページに追加され、基本フィールドのデータが表示されます。

Dataverse の基本フィールドのこの使用に基づき、Finance and Operations の仮想エンティティの基本フィールドは、Finance and Operations の対応するエンティティのエンティティ キーを使用するように設計されています。

Dataverse の基本フィールドには文字列型のフィールドが 1 つだけあることが想定されていますが、Finance and Operations のエンティティ キーにはさまざまなデータ型の複数のフィールドがあるため、エンティティ キー フィールドは文字列に変換されます。 文字列は、連結され、パイプ (\|) によって区切られており、最大 255 文字です。 255 文字を超える値はすべて切り捨てられます。 基本フィールドを表すこの仮想エンティティ フィールドの名前は、**mserp\_primaryfield** になります。

## <a name="relations"></a>リレーション

> [!IMPORTANT]
> 仮想エンティティとネイティブ エンティティを横断する書き込みトランザクションには対応していません。 整合性の確保を保証する方法がないため、この形式のトランザクションは使用しないことを推奨します。

Finance and Operations エンティティのリレーションは、一対多 (1:n) または多対一 (n:1) のリレーションとしてモデル化されます。 これらのリレーションは、Dataverse の仮想エンティティのリレーションシップとしてモデル化されています。 多対多 (n:n) リレーションは、Finance and Operations ではサポートされていないことに注意してください。

たとえば、Finance and Operations では、エンティティ A がエンティティ B への外部キーを持っている場合、このリレーションは、Dataverse の仮想エンティティ A で n:1 のリレーションシップとしてモデル化されます。 Dataverse でのこのリレーションシップのスキーマ名は、名前付け規則 **mserp\_FK\_\<source entity name\>\_\<relation name\>** を使用します。 この名前付け規則では、最大文字列長が 92 文字になっています。 スキーマ名が 92 文字を超える名前を生成するリレーションは、Dataverse の仮想エンティティで生成されません。

このリレーションシップの外部名は、名前付け規則 **FK\_\<relation name\>** を使用します。 外部名は、Finance and Operations に送信されるクエリが作成されるときに、Finance and Operations のリレーションを決定するために使用されます。

Dataverse の仮想エンティティに対してリレーションシップが生成されると、そのルックアップタイプの新しいフィールドがソース エンティティにも追加されます。 前の例では、リレーションシップが作成されると、名前付け規則 **mserp\_fk\_\<target\_entity\>\_id** を使用する新しいルックアップ フィールドがソース エンティティ A に追加されます。Finance and Operations のエンティティに複数のリレーションが存在する可能性があるため 、ソース仮想エンティティには、同じ数のルックアップ フィールド (関連エンティティごとに 1 つ) が作成されます。 このルックアップ フィールドがページまたはビューに追加されると、関連するエンティティの基本フィールドの値が表示されます。

Dataverse の仮想エンティティ内のリレーションシップは、Dataverse の仮想エンティティとしてに既にリレーション内の関連エンティティが存在する場合にのみ生成され ます。 前の例では、エンティティ B が Dataverse の仮想エンティティとしてに存在しない場合、エンティティ A が仮想エンティティとして生成されたときに、エンティティ B へのリレーションがエンティティ A に作成されません。 このリレーションは、エンティティ B が仮想エンティティとして生成された場合にのみエンティティ A に追加されます。 したがって、Finance and Operations の仮想エンティティが生成されると、検証が行われ、生成されている仮想エンティティで完全で機能的なリレーションシップのみが生成されることを確認します。

要約として、次のいずれかの理由により、別の Finance and Operations 仮想エンティティとのリレーションシップが仮想エンティティに存在しない場合があります。

- リレーションシップに参加している Finance and Operations エンティティが、仮想エンティティとして存在していない。
- リレーションシップの名前の長さは、92 文字を超えています。

Dataverse で Finance and Operations 仮想エンティティの一部を生成する際ににエラーが発生した場合、仮想エンティティはまったく作成されないことに注意してください。 上記のいずれかの理由でリレーションシップが存在しない場合は、エラーとは見なされません。

### <a name="native-entitytonative-entity-relationships"></a>ネイティブ エンティティ - ネイティブ エンティティ リレーションシップ

ネイティブ エンティティ - ネイティブ エンティティ リレーションシップは、関連するエンティティの GUID を使用してリレーションシップを解決する Dataverse の標準機能です。 (この GUID はエンティティ キーです)。GUID によって、関連するエンティティの固有のエンティティ レコードが識別されます。

### <a name="virtual-tabletovirtual-table-relationships"></a>仮想テーブル - 仮想テーブル リレーションシップ

2 つの Finance and Operations 仮想エンティティ間のリレーションシップは、Finance and Operations エンティティの関連メタデータによって駆動されます。 前に説明したように、これらのリレーションは、仮想エンティティが生成されたときに Dataverse でリレーションシップとして生成されます。 Dataverse のネイティブ エンティティの動作と同様に、これらのリレーションシップは GUID を使用して Finance and Operations のエンティティの固有レコードを識別します。 意味的には、Finance and Operations 仮想エンティティの GUID は、ネイティブ Dataverse テーブル上で GUID と同じように動作します。 Finance and Operations 仮想エンティティでの GUID の実装については、このトピックで前述した[エンティティ キー/主キー](entity-modeling.md#entity-keyprimary-key) セクションを参照してください。

前の例では、関連するエンティティの GUID はエンティティ B のエンティティ キーであり、Finance and Operation でレコードを識別するクエリを作成するために使用されます。 エンティティ A とエンティティ B のリレーションが使用されます。

したがって、実質的に、エンティティ名は、Finance and Operations から取得されるリレーションで使用される唯一の情報です。 エンティティ名によって、関連エンティティの基本フィールドにアクセスできるようになり、ルックアップにそのエンティティを表示できるようになります。 また、関連するエンティティの GUID にアクセスできるため、前に説明したように、他のクエリで使用することができます。 Finance and Operations エンティティで構築される実際のフィールドは、まったく使用されません。

### <a name="virtual-tabletonative-table-relationship"></a>仮想テーブル - ネイティブ テーブル リレーションシップ

前に説明したように、GUID は、ネイティブ Dataverse テーブル (ネイティブ エンティティ - ネイティブ エンティティ リレーションシップを含む) または Finance and Operations 仮想エンティティ (仮想エンティティ - 仮想エンティティ リレーションシップを含む) 内のレコードを一意に識別するために使用される唯一の情報です。 しかし、Dataverse のアカウント A の Finance and Operations から販売注文を表示する例を考えてみましょう。 このリレーションシップのために Finance and Operations に送信されるクエリには、Dataverse の特定のアカウントに対して販売注文がフィルター処理される必要があるため、Dataverse のネイティブ アカウント エンティティのエンティティ キーの GUID に WHERE 句があります。 ただし、Finance and Operations には Dataverse のエンティティの GUID に関する情報が含まれていないため、クエリが販売注文を返すことはありません。 クエリは、WHERE 句に Finance and Operations が理解するフィールドに基づく条件がある場合にのみ成功します。

それで、Dataverse のアカウント エンティティの GUID を、Finance and Operations のフィールドに置き換えて、Finance and Operations に送信されるクエリが正しい販売注文のリストを返すようにするには、どうすればよいでしょうか?

この問題を解決して、仮想エンティティ - ネイティブ エンティティのリレーションシップが許可される豊富なシナリオ セットを実現するには、このタイプのエンティティにリレーションシップを追加します。 このリレーションは、仮想エンティティが同期されるときにリレーションシップとして表示されます。

上の例では、SalesOrderHeader 仮想エンティティとアカウント ネイティブエンティティの間のリレーションシップは、アカウント番号と会社フィールドに基づいている必要があります。 既定では、Dataverse のネイティブ アカウント エンティティには会社フィールドがありません。 この例では、new_testcompany という会社ルックアップ フィールドを、ネイティブ アカウント エンティティに追加します。

次に、new_accountcompanyidx という名前の新しいキーを追加します。このキーは、accountnumber (new_testcompany) と Dataverse におけるそのアカウント エンティティの固有の行を表します。

次の手順では、X++ でこのリレーションシップを定義します。 次の例は、サンプル X++ コードを示しています。 フィールド、インデックス、およびマッピングの情報の名前は、Dataverse で作成されたフィールドとインデックスの名前と一致している必要があります。 この例では、"synthaccount" という名前のリレーションシップが、仮想 SalesorderHeader エンティティと Dataverse 内のネイティブ アカウント エンティティの間に作成されます。 マップされたフィールドは、new_accountcompanyidx インデックスを構成します。 リレーションシップの表示名は @SYS11307 になります。 表示名の先頭に円記号があることを確認します。 これにより、ラベルがリレーションシップを定義して適切に変換されるようになります。

フィールド マッピングは、仮想エンティティのフィールドが、ネイティブ エンティティのフィールドにマップされていることを示します。 フィールド マッピングでは、キーが仮想エンティティ フィールドである、値がネイティブ エンティティ フィールドです。

```x++
[CDSVirtualEntitySyntheticRelationshipAttribute('synthaccount', 'account', 'accountcompanyidx', '\@SYS11307')]
    public static Map syntheticAccountRelationship()
    {
        Map fieldMapping = new Map(Types::String, Types::String);

        // Assumes the Dataverse account entity has a key on [msdyn_accountnumber, msdyn_companyid]
        // Also assumes that the Dataverse cdm_Company entity has a key on [msdyn_companycode]
        fieldMapping.insert(fieldStr(CDSVirtualEntityTestEntity, StringField), 'msdyn_accountnumber');
        fieldMapping.insert(fieldStr(CDSVirtualEntityTestEntity, DataAreaId), 'msdyn_companyid');

        return fieldMapping;
    }
```
次の手順では、仮想エンティティを生成または更新して、新しいリレーションシップを取得します。 仮想エンティティとネイティブ エンティティ間のリレーションシップは、作成された後 Dataverse では更新できないことに注意してください。 更新を行う唯一の方法は、リレーションシップを物理的に削除し、エンティティを更新した後、問題を解決するためにそのエンティティを再度追加して再関連付けする方法です。

このリレーションシップは一般的な GUID ベースのリレーションシップに似ていますが、リレーションシップのクエリ フィルターをバッキング フィールドの制限に変換するための追加のメタデータがあります。 これで生成されたクエリには、財務と運用アプリが認識するフィールドに基づく WHERE 句が含められるようになります。 その後、クエリによって、フィルター処理された販売注文の一覧が正常に返されます。

### <a name="native-entitytovirtual-entity-relationships"></a>ネイティブ エンティティ - 仮想エンティティ リレーションシップ

<!--HERE-->ネイティブ エンティティ - 仮想エンティティ リレーションシップは、ネイティブ エンティティ - ネイティブ エンティティ リレーションシップと同じように機能します。 ユーザーが Finance and Operations の仮想レコードにネイティブ レコードを関連付けると、その仮想エンティティの GUID がネイティブ エンティティ レコードに保存されます。 既に説明したように、リレーションシップに参加するエンティティには、関連するエンティティの GUID フィールドが含まれます。 したがって、Dataverse の見積が Finance and Operations 仮想エンティティ内の顧客に関連付けられている場合は、顧客の仮想エンティティの GUID が見積エンティティに保存されます。 この動作により、標準の Dataverse 機能を使用してレコードを予想どおりに取得できます。

## <a name="enums"></a>列挙

Finance and Operations の列挙型は、Dataverse の OptionSet としてモデル化されています。 Finance and Operations の仮想エンティティが生成されると、必要な列挙型は OptionSet として生成されます。 OptionSet が既に存在する場合は、代わりに使用されます。

## <a name="company"></a>会社

Finance and Operations のエンティティは、会社にバインドすることも、グローバルにすることもできます。 会社にバインドされている Finance and Operations エンティティの仮想エンティティは、Dataverse の cdm\_company エンティティとのリレーションシップを持ちます。 cdm\_company エンティティは、Dataverse におけるネイティブ エンティティで あり、Dynamics365Company ソリューションの一部です。 通常と同様、リレーションシップが作成されると、関連するエンティティ (この場合は cdm\_company) の仮想エンティティにも検索フィールドが作成されます。 このルックアップ フィールドは **会社** という名前であり、ユーザーがリストの値を選択したり、関連するレコードの詳細に移動したりできるように、最適なユーザー エクスペリエンスを提供するために使用する必要があります。 **会社コード** と呼ばれるフィールドは、仮想エンティティにも追加されます。 この値は 4 文字の文字列です。 このフィールドは、プログラミングで使用する必要があります。

## <a name="attachments"></a>アタッチメント

Finance and Operations エンティティの添付ファイルは、エンティティごとにサポートされます。 たとえば、請求書ヘッダー エンティティは、[エンティティを通じて添付ファイルを有効](../../fin-ops/organization-administration/configure-document-management.md#how-can-attachments-be-extracted-from-the-system)にするために、請求書に関連する添付ファイル エンティティを実装します。

このタイプのエンティティは、Finance and Operations の対応する添付ファイル エンティティと関係があります。 したがって、これらは前に説明した他の関係と同じパターンに従います。 つまり、添付ファイル機能が実装されている Finance and Operations エンティティは、仮想エンティティを使用して添付ファイルを使用できるようにします。 添付ファイルをサポートしていない Finance and Operations エンティティは、Dataverse で仮想化された添付ファイルもサポートしていません。

Finance and Operations 仮想エンティティでサポートされるのは、添付ファイルの読み取りだけであることに注意してください。 現在、仮想エンティティを使用した添付ファイルの作成、更新、または削除はサポートされていません。

## <a name="odata-actions"></a>OData アクション

Finance and Operations エンティティの OData アクションは、Dataverse のカスタム アクションとして使用できるようになります。 カスタム アクションと Dataverse での使用方法の詳細については、[カスタム アクション](/powerapps/developer/common-data-service/custom-actions)を参照してください。

次のタイプの入力パラメーターと出力パラメーターがサポートされています。 入力または出力パラメーターのタイプが異なる場合、OData アクションは Dataverse の SDK メッセージとして表示されません。

- 整数
- 文字列
- Guid
- ブール値
- Date/Datetime

以下は、Finance and Operations エンティティでサポートされているものの、Dataverse の対応する仮想エンティティではサポートされていない OData アクションの例です。

- RetailStoreTenderTypeTable.queryDistinctTenderTypeIdAndName (RetailStoreTenderTypeTable エンティティのコレクション)
- DocumentRoutingClientApp.syncPrinters (DocumentRoutingClientApp エンティティ)
- DocumentRoutingClientApp.updateJobStatus (DocumentRoutingJobStatus 列挙)
- DimensionCombination.getCombinationDisplayValue (LedgerJournalACType 列挙)

## <a name="labels-and-localization"></a>ラベルとローカライズ

Finance and Operations のエンティティ名やフィールド名など、メタデータに定義されているラベルは、Dataverse で仮想エンティティが生成されるときに取得されます。 ラベルは、Dataverse にインストールされている言語ロケールの一覧を渡すことによって取得されます。 Finance and Operations は、Dataverse でラベル インスタンスを構築するために使用される、ロケール/値セットの一覧として各ラベルを返します。 エンティティの生成または更新時に存在する言語パックのみが含まれます。 また、Finance and Operations が翻訳を提供したラベルのみが含まれます。 欠落している翻訳がある場合、ラベル ID に戻されます (**\@SYS:DataEntity** など)。 新しい言語パックが Dataverse にインストールされた後、その言語のラベルが Finance and Operations に存在する場合は、新しいラベル情報を取得するために既存のエンティティを更新する必要があります。

ランタイム ラベルは、現在のユーザー コンテキストの言語で返されます。 つまり、Finance and Operations でそのユーザーの UserInfo レコードに指定されている言語で返されます。 この動作は、エラー メッセージにも適用されます。

## <a name="error-handling"></a>エラー処理

Finance and Operations は、エンティティのビジネス ロジックの作成、読み取り、更新、削除 (CRUD) を実行し、Dataverse の仮想エンティティを介して呼び出されたときにバッキング テーブルを実行します。 なんらかの例外が Finance and Operations 側でスローされた場合は、エラー ログの最後のメッセージが Dataverse に返され、Finance and Operations からのメッセージを含む InvalidPluginExecutionException 例外としてスローされます。 Finance and Operations コードはユーザーのコンテキストで実行されるため、エラー メッセージの言語は、 Finance and Operations の UserInfo レコードで指定されている言語に基づきます。 Finance and Operations で情報ログに書き込まれたメッセージに対して例外が発生しなかった場合、Dataverse には表示されません。

## <a name="calculatedunmapped-fields"></a>計算済み/マップ解除済みフィールド

Finance and Operations エンティティの計算されたフィールドとマップされていないフィールドは、Dataverse の対応する仮想エンティティでも使用できます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]