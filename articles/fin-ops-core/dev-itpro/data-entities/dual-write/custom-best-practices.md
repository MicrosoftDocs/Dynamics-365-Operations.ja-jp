---
title: 二重書き込みのカスタマイズに関するガイダンス
description: このトピックでは、二重書き込みのカスタマイズについてのガイダンスを提供します。
author: RamaKrishnamoorthy
ms.date: 09/15/2021
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: ramasri
ms.search.validFrom: 2021-09-15
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e11d9bc43414613cb041814cdefa6a7711d9a49c
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781214"
---
# <a name="customization-guidance-for-dual-write"></a>二重書き込みのカスタマイズに関するガイダンス

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

二重書き込みでは、一部の業務プロセスに対する標準のマップが提供されます。 ただし、フィールド、マップ、または変換を追加する必要がある場合があります。 二重書き込みプラットフォームは拡張可能です。 カスタム マップを作成し、カスタム フィールドを使用して既存のマップを拡張して、Finance and Operations アプリと Microsoft Dataverse の間のデータを同期します。 このトピックでは、これらのカスタマイズのガイダンスとベスト プラクティスについて説明します。

マップをカスタマイズする前に、[テーブル マッピングと列マッピングのカスタマイズ](customizing-mappings.md) でタスクをよく理解する必要があります。

## <a name="guidance-when-the-entity-is-in-both-the-finance-and-operations-app-and-dataverse"></a>エンティティが Finance and Operations アプリおよび Dataverse の両方である場合のガイダンス

エンティティが両方の環境にある場合は、二重書き込みマップを作成します。

+ エンティティの統合キーは、両方の環境で一致する必要があります。 エンティティ キーを使用できない場合は、エンティティ キーを必ず作成してください。 統合キー フィールドは、マップ内で互いにマップされる必要があります。
+ **会社フィールド** はすでにキーの一部なので、エンティティが法人固有の場合、マッピングで **会社フィールド** を表示することはできません。 例については、**顧客グループ (msddn\_customergroups)** エンティティ マッピングを確認します。
+ Finance and Operations 環境または Dataverse 環境のいずれかにフィルターを追加し、特定の条件でのみ二重書き込みマップをトリガーします。 **顧客 V3 - アカウントまたは CDS 連絡先 V2 (連絡先)** マップには例として使用できる複数のフィルターがあります。

## <a name="guidance-when-the-entity-is-in-the-finance-and-operations-app-only"></a>エンティティが Finance and Operations アプリのみである場合のガイダンス

エンティティが Finance and Operations アプリのみである場合、新しいエンティティを Dataverse で作成し、マップを追加します。

+ Finance and Operations エンティティに法人固有のデータが含まれている場合は、新しい Dataverse エンティティの **cdm\_companies** にルックアップ フィールドを必ず追加してください。 Finance and Operations エンティティがグローバルの場合、会社のフィールドは Dataverse エンティティには必須ではありません。
+ Dataverse エンティティにキーを追加して Finance and Operations エンティティ キーを反映します。 二重書き込みには、Finance and Operations 環境と Dataverse 環境の両方で同じエンティティ キーが必要です。 Finance and Operations アプリと Dataverse のキー フィールドは互いにマップされる必要があります。 マッピングに **会社** フィールドを追加しないでください。 例については、**仕入先 V2 - msdyn\_venders mapping** を確認します。

## <a name="guidance-when-the-entity-is-in-dataverse-only"></a>エンティティが Dataverse のみである場合のガイダンス

エンティティが Dataverse のみである場合、新しいエンティティを Finance and Operations 環境で作成し、マップを追加します。

+ 新しいエンティティを作成し、必要なすべてのフィールドを含めます。 エンティティがデータ管理に対して有効であり、OData (データ プロトコルを開く) によって使用できることを確認します。 新しいエンティティの作成方法の詳細については、[データ エンティティの構築と使用](../build-consuming-data-entities.md) を参照してください。
+ Finance and Operations アプリのデータが法人固有の場合は、Dataverse エンティティの **cdm\_companies** にルックアップ フィールドを必ず追加してください。 Finance and Operations エンティティがグローバルの場合、会社のフィールドは Dataverse エンティティには必須ではありません。
+ 両方のエンティティがエンティティ キー フィールドを持っていることを確認します。 二重書き込みには、Finance and Operations 環境と Dataverse 環境の両方で同じエンティティ キーが必要です。 Finance and Operations アプリと Dataverse のキー フィールドは互いにマップされる必要があります。 マッピングに **会社** フィールドを追加しないでください。 例については、**仕入先 V2 - msdyn\_venders mapping** を確認します。

## <a name="add-attributes-to-a-mapping"></a>マッピングへの属性の追加

エンティティが両方の環境に存在しマップされている場合は、属性をマップに追加できます。 詳細については、[テーブル マッピングと列マッピングのカスタマイズ](customizing-mappings.md) を参照してください。

## <a name="create-and-update-operations-dont-trigger-the-synchronization-of-attributes-to-dataverse"></a>操作の作成と更新では、Dataverse への属性の同期はトリガーされない

場合によっては、エンティティが両方の環境に存在しますが、操作の作成および更新によって Dataverse への属性の同期はトリガーされません。 Finance and Operations 仮想マシン (VM) でSQL を使用して、またはテーブル ブラウザーを使用して **BusinessEventsDefinition** テーブルに移動します。 更新された日時 (**RefTableName** フィールド内) とエンティティ名 (**RefEntityName** フィールド内) を持つ影響を受けるテーブルの組み合わせに対するレコードが存在することを確認します。 次の図に例を示します。

![BusinessEventsDefinition テーブル ブラウザー](media/custom-business-event.png)

## <a name="guidance-when-entities-arent-available-in-either-the-finance-and-operations-app-or-dataverse"></a>エンティティが Finance and Operations アプリまたは Dataverse のいずれかで使用できない場合のガイダンス

エンティティがどちらの環境にも存在しない場合は、両方の環境でテーブルを作成し、次の手順に従ってアプリを作成できます。

1. Dataverse で、必要なすべてのフィールドを含む新しいテーブルを作成します。 [カスタム テーブルの作成](/modules/create-manage-entities/2-custom-entity) の手順に従います。 テーブルに法人固有のデータを格納する場合、 Dataverse テーブルの **cdm \_companies** にルックアップ フィールドを必ず追加してください。 テーブルがグローバル データを格納する場合、会社のフィールドは Dataverse テーブルには必須ではありません。
2. Finance and Operations アプリで、必要なすべてのフィールドを含む新しいエンティティを作成します。 エンティティがデータ管理に対して有効であり、OData によって使用できることを確認します。 新しいエンティティの作成方法の詳細については、[データ エンティティの構築と使用](../build-consuming-data-entities.md) を参照してください。
3. テーブル マップの二重書き込みを有効にするには、Dataverse デーブルで代替キーを定義する必要があります。 Dataverse の代替キーの値は、Finance and Operations アプリで定義されているキーと一致する必要があります。 たとえば、Finance and Operations アプリでは、次の図で示すように **CustomerAccount** が **アカウント** テーブルのキーになります。

    ![CustCustomerV3Entity のプロパティ](media/custom-customer-account.png)

    Dataverse では、次の図で示すように **accountnumber** が **アカウント** テーブルのキーとして定義されます。

    ![アカウントの Dataverse キー](media/custom-account-keys.png)

    **顧客 V3** テーブル マップでは、**accountnumber** が **CustomerAccount** にマップされていることがわかります。
    
    ![アカウント番号のテーブル マップ](media/custom-table-map.png)

## <a name="best-practices-for-dual-write"></a>二重書き込みのベスト プラクティス

+ 変更はトランザクションに含む必要があります。 テーブル デザインに基づいてトランザクションごとにレコード数を評価することが重要です。 また、X++ で、プロセスの一部としてトランザクション ブロックがどのように構成されるかを評価することが重要です。 次に 2 つの例を挙げます。

    ```xpp
    ttsbegin;
    // Transaction start
    table1record1.insert();
    table1record2.insert();
    table1record3.insert();
    table1recordN.insert();
    ttscommit;
    // Transaction end
    ```

    ```xpp
    ttsbegin;
    // Transaction start
    while (// loop conditions// )
    {
        table1recordN.insert();
    }
    ttscommit;
    // Transaction end
    ```

+ 次の項目はビジネス イベントで処理されません。 したがって、これらのデータは二重書き込みで処理されません。

    + **doUpdate** メソッド
    + **doInsert** メソッド
    + セット ベースの操作 (**挿入** および **更新**)
    + **skipBusinessEvents(true)** がマークされているレコード

+ ビジネス イベントは、マップされているデータ ソースに登録する必要があります。 外部結合を使用し、Finance and Operations アプリで読み取り専用としてマークされているデータ ソースは追跡されません。
+ 変更は、Finance and Operations アプリでマップされたフィールドに変更がある場合にのみトリガーされます。 Costomer Engagement アプリでは、フィールドの変更はすべて二重書き込み同期をトリガーします。
+ すべてのフィルター評価は、有効な結果を提供する必要があります。
+ データ ソースは、マップされたフィールドが 1 つも指定されていない場合は追跡されません。
+ Finance and Operations アプリのエンティティ リレーションシップでは、2 つのエンティティがリンクされ、同じトランザクション内の 2 つのレコードの間にリレーションシップが存在していることを二重書き込みで指定する必要があります。 両方の親レコードと子レコードが関連するエンティティで同じトランザクションの一部である場合、二重書き込みバッチ処理はレコード挿入の順番付けが明示的に定義され、考慮されるエンティティ リレーションシップに依存しています。 Finance and Operations アプリのビジネス プロセスに複数のエンティティが含まれ、Costomer Engagement アプリでバッジ モードとして有効にされている場合、二重書き込みにはエンティティ上で識別され、定義されるためのリレーションシップが必要です。 次の図は、**販売注文ヘッダー V2** と **販売注文行 V2** とのリレーションシップを示しています。

    ![Finance and Operations アプリでのリレーションシップ](media/custom-sales-order.png)

+ パフォーマンスの問題を防ぐには、レコード変更のために複数のイベントを発生させる二重書き込みデータ テーブルで多数のデータ ソースを使用しないでください。 二重書き込みで不要なフィールドをマップしないようにし、テーブルおよびエンティティでの過剰なビジネス ロジックを回避します。
+ Finance and Operations アプリのカスタム エンティティが会社固有の場合 (つまり、エンティティの主な会社コンテキスト プロパティが **DataAreaId** になっている場合)、関連する Dataverse テーブルはキー列の 1 つとして会社ルックアップを持つ必要があります。 共有エンティティと会社固有のエンティティとのマッピングは許可されません。 Finance and Operations アプリ エンティティが共有か、または会社固有かを決定するには、Visual Studio アプリケーション エクスプローラーで **エンティティ** プロパティを確認します。 詳細については、[会社間のデータ エンティティの動作](../cross-company-behavior.md) を参照してください。

    ![SalesOrderLineEntity のプロパティ](media/custom-data-entity-view.png)

## <a name="filter-guidance-for-maps"></a>マップのフィルター ガイダンス

フォルターは Finance and Operations エンティティと Dataverse テーブルの両方に適用できます。 フィルターは、二重書き込みマップ上にあるフィールドにのみ適用する必要があります。 二重書き込みマップに追加する前に、フィルターの結果を確認します。

Finance and Operations エンティティの場合、実行可能な X++ クラスで次のコード例を使用してフィルター式を検証できます。 式とエンティティ名を置き換え、クラスを実行します。

```xpp
var entityName = "PROJECTENTITY";
var filterExpression = '(ParentProject == "")';
Query query = new Query();
query.literals(NoYes::Yes);
QueryBuildDataSource qbd =
query.addDataSource(tablename2id(entityName));
qbd.addRange(fieldname2id(qbd.table(),identifierStr(RecVersion))).
value(filterExpression);
qbd.addSelectionField(fieldname2id(qbd.table(),identifierStr(RecId)));
QueryRun qRun = new QueryRun(query);
// This provides the actual SQL statement to execute
var actualSqlStatement = query.getSQLStatement();
while(qRun.next())
{
    var rec = qRun.get(tableName2Id(entityName));
}
```

Dataverse テーブルの場合は、OData 式にフィルター条件として式を追加することで、フィルター式を検証できます。

```powerappsfl
https://<Env URL>/api/data/v9.0/<TableName>?$filter=<fieldname> eq <value>
```

フィルターの詳細と例については、[フィルター処理の例とパターン](dual-write-faq.md#where-can-i-find-examples-and-patterns-for-filtering-dual-write-maps) を参照してください。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
