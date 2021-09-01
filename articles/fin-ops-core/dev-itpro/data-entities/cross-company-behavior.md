---
title: データ エンティティの会社間動作
description: このトピックでは、データ エンティティと企業間コンセプトとの関係について説明します。
author: peakerbl
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 25371
ms.assetid: f293d97a-9f70-4c45-91d4-574731892353
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0472caa8a678fe98deae892a65c0840fec19ce05
ms.sourcegitcommit: 7aa7d756e1e98a53da62e03c608a9597ef9893ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/20/2021
ms.locfileid: "7404191"
---
# <a name="cross-company-behavior-of-data-entities"></a>データ エンティティの会社間動作

[!include [banner](../includes/banner.md)]

このトピックでは、データ エンティティと企業間コンセプトとの関係について説明します。 データエンティティのこの側面を理解するには、テーブルとビューが企業間の概念をどのように適用するのかを理解する必要があります。 したがって、このトピックでは、テーブルとビューの概要を説明し、データ エンティティの関連性について説明します。

## <a name="review-of-tables-and-views-for-cross-company"></a>会社間のテーブルとビューの確認

各テーブルには **SaveDataPerCompany** プロパティがあり、各ビューには **AllowCrossCompany** プロパティがあります。 次のテーブルにこれらの 2 つのプロパティを示します。

|      &nbsp;            | テーブル | 表示 |
|------------------------|-------|------|
| プロパティ名          | SaveDataPerCompany | AllowCrossCompany |
| 関連する CRUD モード     | CUD | R |
| 効果のタイミング       | 実行時間、デザイン時 | ほとんどの場合は実行時。 デザイン時に、この設定によりビューは選択したフィールド リストに **dataAreaId** を持ちます。 ただし、特定の **dataAreaId** 値のフィルターが、後の実行時に追加されます。 |
| 値の意味 = はい | デザイン時には、フィールドがアプリケーション オブジェクト ツリー (AOT) に表示されていなくても、システムはテーブルに **dataAreaId** フィールドを自動的に *追加* します。 テーブルのすべてのレコードには、それが所属する会社 (または法人) がタグ付けされています。 システムは自動的に SQL **Where** 句にフィルターを *追加* して、返された行セットを 1 つの **dataAreaId** 値に制限します。 | 実行時に、システムは、基になる Microsoft SQL Server システムに送信する SQL **Select** ステートメントの **Where** 句に **dataAreaId** のフィルターを自動的に追加 *できません*。 したがって、ビューからの SQL **Select** ステートメントは、*複数の* 企業のレコードを含む一連のレコードを返すことができます。 |
| 値の意味 = いいえ  | システムは、テーブルに **dataAreaId** フィールドを追加 *しません*。 テーブルは共有テーブルであると言われています。なぜならレコードには正式な会社固有のデータが含まれていないからです。 | システムは自動的に SQL **Where** 句にフィルターを *追加* して、返された行セットを 1 つの **dataAreaId** 値に制限します。 ただし、ビューの *ルート* データ ソースが共有テーブルである場合、**AllowCrossCompany** プロパティは無視されます。 |

## <a name="comparisons-within-allowcrosscompany--no"></a>AllowCrossCompany 内の比較 = いいえ
次のスクリーンショットでは、**CustomerList** ビューに 2 つのデータ ソースがあります。

- **ルート** – CustTable、**SaveDataPerCompany** が入っているプロパティを **はい** にセットします。
- **非ルート** – DirPartyTable、**SaveDataPerCompany** が入っているプロパティを **いいえ** にセットします。

[![CustomerList ビューには 2 つのデータ ソースがあります。](./media/root.png)](./media/root.png)

次のスクリーンショットが示すように、**CustomerList** 表示は、**AllowCrossCompany** プロパティを **いいえ** に設定しています。

[![AllowCrossCompany プロパティはいいえに設定しています。](./media/crosscomp.png)](./media/crosscomp.png)

**CustomerList** 表示に関する前述の情報が与えられた場合、システムは、SQL **表示の作成** ステートメントを生成して実行することによって、基盤となる SQL Server システムに表示を作成します。

```sql
CREATE VIEW [dbo].[CUSTOMERLIST] 
AS 
       SELECT T1.accountnum AS ACCOUNTNUM, 
              T1.dataareaid AS DATAAREAID,  -- AllowCrossCompany =No caused this line.
              T1.partition  AS PARTITION, 
              T1.recid      AS RECID, 
              T2.partition  AS PARTITION#2, 
              T2.name       AS NAME 
       FROM   custtable T1 
              CROSS JOIN dirpartytable T2 
       WHERE ( T1.party = T2.recid 
              AND ( T1.partition = T2.partition ) ) 
```

### <a name="making-dirpartytable-the-root-data-source"></a>DirPartyTable をルート データ ソースにする

[![DirPartyTable をルート データ ソースにします。](./media/dirpar.png)](./media/dirpar.png)

**CustomerList** ビューの 2 つのデータ ソース テーブルの位置を入れ替えて、DirPartyTable テーブルをルート データ ソースにします。

```sql
CREATE VIEW [dbo].[CUSTOMERLISTPARTY] 
AS 
       SELECT T1.name       AS NAME, 
              T1.partition  AS PARTITION, 
              T1.recid      AS RECID, 
              T2.partition  AS PARTITION#2, 
              T2.accountnum AS ACCOUNTNUM 
       FROM   dirpartytable T1 
              CROSS JOIN custtable T2 
       WHERE  ( T2.party = T1.recid 
              AND ( T2.partition = T1.partition ) ) 
go 
```

この場合、SQL の **ビューの作成** ステートメントは、次の 2 つの相違点を除いて同じです。

- **FROM** 句は、最初に DirPartyTable に言及し、次に CustTable に言及します。
- **SELECT** 列には **dataAreaId** の行が含まれて *いません* (DirPartyTable の **SaveDataPerCompany** プロパティが **No** に設定されているため)。

## <a name="limitations-of-tables-and-views"></a>テーブルおよびビューの制限
場合によっては、テーブルおよびビューの会社間の管理機能は求められるほど細かい制御ではない場合があります。 制限を次に示します。

- システム **dataAreaId** フィールド以外の会社または法人フィールドは、**dataAreaId** が行うことができる方法で自動的に認識または処理することはできません。
- 非ルート データソースに **dataAreaId** フィールドがある場合でも、ビューに対する会社間の動作は、ルート データソースのプロパティにはあまりにも制限されています。

たとえば、これは、法人情報が **LegalEntityRecId** にあり、または共有テーブルに **dataAreaId** 列がない場合に発生する可能性があります。

## <a name="design-time-setting-the-primarycompanycontext-property"></a>デザイン時間: PrimaryCompanyContext プロパティの設定
データ エンティティは、テーブルの限界を克服し、企業間機能が関係する場所を表示するのに役立ちます。 データ エンティティは **PrimaryCompanyContext** プロパティがあり、会社 ID に使用するエンティティ フィールドを指定できます。 このプロパティは、次のような方法で柔軟性ときめ細かな制御を提供します。

- フィールドは、エンティティの任意のデータ ソースに由来することができ、ルート データ ソースのフィールドに限定されません。
- このフィールドは、**DataAreaId** 拡張データ型 (EDT) から拡張され、基礎となるシステム **dataAreaId** フィールドに限定されない任意のフィールドにすることができます。
- エンティティにデータ ソースとして共有テーブルのみがあるときであっても、ユーザーの特定の状況にかなう場合は、**PrimaryCompanyContext** プロパティを使用することができます。

次のスクリーンショットは、**FMCustGroupEntity** エンティティの **PrimaryCompanyContext** プロパティに設定された値を示しています。

[![PrimaryCompanyContext プロパティ。](./media/prim1.png)](./media/prim1.png)

**PrimaryCompanyContext** 値が空でない値に設定されている場合、エンティティは共有エンティティとして動作できません。 **dataAreaId** フィールドは、SQL **Create View** ステートメントに追加されます。

```sql
CREATE VIEW [dbo].[FMCUSTGROUPENTITY] 
AS 
       SELECT T1.custgroup   AS GROUPNAME, 
              T1.description AS DESCRIPTION, 
              T1.dataareaid  AS DATAAREAID,   -- dataAreaId is added. 
              T1.recversion  AS RECVERSION, 
              T1.partition   AS PARTITION, 
              T1.recid       AS RECID 
       FROM   fmcustgroup T1 
```

## <a name="run-time-the-behavior-of-data-entities-for-cross-company"></a>実行時: 会社間のデータ エンティティの動作
X++ コードのコンテキストでは、データ エンティティの会社間の動作はテーブルの動作に似ています。 エンティティの **PrimaryCompanyContext** プロパティが値を持たないおよびが空白の場合、エンティティが共有テーブルと同様に動作します。

### <a name="x-when-primarycompanycontext-is-set"></a>X++ PrimaryCompanyContext が設定されている場合

次のテーブルは、**PrimaryCompanyContext** プロパティがフィールド値に設定されている場合の CRUD アクセスでのデータ エンティティの動作を示しています。 X++ と OData の両方のアクセスについて説明しています。

|  &nbsp;       | X++ | OData |
|-------------|-----|-------|
| 読み取り (R)    | 既定では、結果は *常に* **dataAreaId** = 現在の会社によってフィルター処理され、会社間データは **会社間** オプションを使用して取得できます。 | 結果は、**dataAreaId** によってフィルター処理され *ません*。 コンシューマーは明示的にフィルター処理する必要があります。 |
| 書き込み (CUD) | データ エンティティへの CUD アクセスは、常に現在の会社のコンテキストで行われます。 エンティティへの会社間 CUD アクセスが必要である場合、**changeCompany** キーワードを使用します。 | **PrimaryCompanyContext(myDataAreaId)** フィールドの値を設定すると、エンティティへの CUD アクセスを会社のコンシューマーによって実行できます。 フレームワークは必要な **ChangeCompany** アクションを処理します。 |

次の X++ コード例は、**PrimaryCompanyContext** プロパティが **dataAreaId** に設定されている、**FMCustGroupEntity** にアクセスします。

[![PrimaryCompanyContext プロパティが DataAreaId に設定されています。](./media/fmcust.png)](./media/fmcust.png)

[![X++ コード例は FMCustGroupEntity にアクセスします。](./media/snip-550x1024.png)](./media/snip.png)

### <a name="x-when-primarycompanycontext-is-empty"></a>X++ PrimaryCompanyContext が空の場合

データ エンティティに関して **PrimaryCompanyContext** プロパティが設定されていると、ビュー スキーマに **dataAreaId** フィールドが作成され、**PrimaryCompanyContext** フィールドにマップされます。 次のテーブルは、**PrimaryCompanyContext** プロパティが空の場合の CRUD アクセスでのデータ エンティティの動作を示しています。 X++ と OData の両方のアクセスについて説明しています。

|     &nbsp;   | X++                                                                                                                              | OData |
|-------------|----------------------------------------------------------------------------------------------------------------------------------|-------|
| 読み取り (R)    | システム **dataAreaId** フィールドがビュー スキーマに作成されないため、結果はフィルター処理されません。                                   | (R with X++ の場合と同じ) |
| 書き込み (CUD) | 設定する主な企業コンテキストはありません。 したがって、エンティティへの CUD アクセスは、常に現在の会社のコンテキストです。 | (CUD with X++ の場合と同じ) |

現在の例では、**FMCustomerGroupGlobalEntity** エンティティで **PrimaryCompanyContext** プロパティに割り当てられている値はありません。

[![PrimaryCompanyContext プロパティに割り当てられている値はありません。](./media/ent1.png)](./media/ent1.png)

ただし、FMCustGroup テーブルの **dataAreaId** フィールドは、**LegalEntity** という名前の通常のフィールドとして **FMCustomerGroupGlobalEntity** にマップされます。 この例では、FMCustGroup テーブルは **FMCustomerGroupGlobalEntity** のルート データ ソースです。 ただし、システムの自動メカニズムをバイパスする非公式な方法でこの **dataAreaId** フィールドを使用しています。 これらすべての詳細は **法人** フィールドの次のスクリーンショットに表示されます。

[![LegalEntity フィールド。](./media/ent2.png)](./media/ent2.png)

> [!NOTE]
> *法人エンティティ* および *データ エンティティ* の両方が *エンティティ* という語を使用していますが、混合しないでください。 法人およびデータ エンティティは、まったく異なる 2 つの概念です。 **PrimaryCompanyContext** プロパティが空のとき、SQL の **ビューの作成** ステートメントには、通常、システムの **dataAreaId** 列についての記述は含まれていません。 ただし、現在の例では、データ エンティティの **LegalEntity** 通常フィールドが原因で **dataAreaId** が「半参照」になります。 このフィールドは、次の SQL ステートメントに表示されます。

```sql
CREATE VIEW [dbo].[FMCUSTOMERGROUPGLOBALENTITY] 
AS 
       SELECT T1.custgroup   AS NAME, 
              T1.description AS DESCRIPTION, 
              T1.dataareaid  AS LEGALENTITY,   -- dataAreadId is named LegalEntity. 
              T1.recversion  AS RECVERSION, 
              T1.partition   AS PARTITION, 
              T1.recid       AS RECID 
       FROM   fmcustgroup T1 
```

### <a name="purpose-of-this-example"></a>この例の目的

この例では、2 つの目的があります。

- バッキング テーブルが会社固有だとしても、共有データを既定で表示します。
- **LegalEntity** という名のレギュラー フィールドを使用して、データ エンティティのコンシューマーが、フィルター処理または **dataAreaId** を適用するようにします。

### <a name="test-data"></a>テスト データ

**テーブル ブラウザー** ページの次のスクリーンショットは、X++ テスト コードが実行される前の **FMCustomerGroupGlobalEntity** エンティティにあるテスト データを示しています。

[![テーブル ブラウザー ページ。](./media/ent3.png)](./media/ent3.png)

### <a name="x-code"></a>X++ コード

共有エンティティと共に X++ テスト コードがどのように機能するかを次に示します。

- 読み取りのために共有モードでデータ エンティティにアクセスします。
- 新しいレコードが作成されたときに、1 つの特定の会社があるデータ エンティティにアクセスします。

[![X++ テスト コード。](./media/snip2.png)](./media/snip2.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
