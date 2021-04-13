---
title: 集計の測定への財務分析コードの追加
description: このトピックでは、パワー ユーザーが既製の Power BI レポートに財務分析コードを組み込む方法について説明します。
author: MilindaV2
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.assetid: c04e0a7b-1747-4b88-b729-fd820f8ab600
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 8 for Finance and Operations
ms.openlocfilehash: 8b34896224c47064c997ebe34ecc19be452512a0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754586"
---
# <a name="add-financial-dimensions-to-aggregate-measurements"></a>集計の測定への財務分析コードの追加

[!include [banner](../includes/banner.md)]

この機能により、パワーユーザーは 既成の Microsoft Power BI レポートに財務分析コードを含めることができます。 パワー ユーザーは、財務分析コードを使用する新しい Power BI レポートを作成することもできます。

財務分析コードは、追加情報を保持する勘定科目表を有効にする、ユーザー定義されたコンフィギュレーション データです。 財務分析コードを追加することにより、ユーザーは勘定科目表および財務諸表に含まれる追加のデータ フィールドを構成することができます。 したがって、元帳勘定科目表をそれらのフィールドに基づいて詳しく分析できます。 この機能は、強力な財務報告を提供します。 たとえば、追加した新しい財務分析コードを使用して元帳データを参照できます。 リリースされるときに既製の Power BI レポートに財務分析コードが含まれていないため、これらの追加フィールドを既製のレポートに含める必要があります。 

財務分析コード フィールドがレポートに含まれた後、他のユーザーとレポートを共有できます。 これらの他のユーザーは、財務分析コード フィールドのすべてまたは一部を含むことによって、チャートなどの既存のビジュアルを変更できます。

> [!NOTE]
> この機能は Microsoft Dynamics 365 for Finance and Operations、Enterprise edition (2017 年 7 月) で使用可能です。 プラットフォーム アップデート 8 以降も必要です。 

## <a name="how-does-this-feature-work"></a>この機能はどのように作用しますか。

エンティティ格納は、パワー ユーザーがレポートを作成できる運用データ ウェアハウスです。 エンティティ格納が更新されるときはいつでも、すべての使用可能な財務分析コードがそれに含まれます。 総勘定仕訳元帳レベルの詳細を含む **元帳活動** の集計の測定の例を検討します。

次のリストは、更新されたときに エンティティ格納に格納されるテーブルの一部を示しています。 変更が加えられたテーブルは太字です。

- LedgerActivityMeasure\_LedgerActivityMeasureGroup
- LedgerActivityMeasure\_TransactionDate
- LedgerActivityMeasure\_Currency
- LedgerActivityMeasure\_FiscalPeriodDateAggregtateDimension
- LedgerActivityMeasure\_LedgerFactDimension
- LedgerActivityMeasure\_FiscalYearOffsetDimension
- LedgerActivityMeasure\_MainAccount
- **LedgerActivityMeasure\_DimensionCombination**
- LedgerActivityMeasure\_Ledger
- LedgerActivityMeasure\_MainAccountCategory
- LedgerActivityMeasure\_Company
- LedgerActivityMeasure\_MainAccountLegalEntity
- **LedgerActivityMeasure\_Agreement**
- **LedgerActivityMeasure\_BankAccount**
- **LedgerActivityMeasure\_BusinessUnit**
- **LedgerActivityMeasure\_Campaign**
- **LedgerActivityMeasure\_Cargo**
- **LedgerActivityMeasure\_Cargo\_CN**

システムで定義されている各財務分析コードについて、エンティティ格納で対応するテーブルを確認できる場合があります。

LedgerActivityMeasure\_DimensionCombination テーブルを調べると、フィールドの一覧が拡張され、追加フィールドが含まれていることが分かります。 それぞれの新しいフィールドは、財務分析コードに対応します。 例については、以下は追加のフィールドの一部です。

- 契約 \_FK
- 契約 \_ 内容
- 契約 \_ 値
- BankAccount\_FK
- BankAccount\_説明
- BankAccount\_値
- BusinessUnit\_FK
- BusinessUnit\_説明
- BusinessUnit\_値

**仕入先** という名前の新しい財務分析コードをユーザーが定義した場合、エンティティ格納が更新されると、LedgerActivityMeasure \_仕入先という新しいテーブルが追加されます。

LedgerActivityMeasure\_DimensionCombination テーブルには、次の新しいフィールド セットも含められます。

- 仕入先\_FK
- 仕入先\_説明
- 仕入先\_値

## <a name="how-a-power-bi-report-author-can-create-reports-that-use-financial-dimensions"></a>Power BI レポート作成者が財務分析コードを使用するレポートを作成する方法

ビジネス ユーザーは、Power BI デスクトップを使用して財務分析コードを使用する新しいレポートを作成することができます。 財務分析コードを使用する既存のレポートを更新して、追加のフィールドを含めることができます。

この例では、元帳活動メジャー グループを使用するレポートを作成するために Power BI デスクトップを使用します。 

1. 開発環境で、Power BI desktop を使用してエンティティ ストア データベースに接続します。 
2. 次のテーブルを選択します。

    - LedgerActivityMeasure\_LedgerActivityMeasureGroup
    - LedgerActivityMeasure\_FiscalPeriodDateAggregtateDimension
    - LedgerActivityMeasure\_DimensionCombination

3. Power BI デスクトップの **リレーションシップの管理** オプションを使用して、テーブル フィールド間に以下のリレーションシップを定義します。

    - **LedgerActivityMeasure\_LedgerActivityMeasureGroup.LEDGERDIMENSION** および **LedgerActivityMeasure\_DimensionCombination.DIMENTIONCOMBINATIONRECID** 間の結合を定義します。
    - **LedgerActivityMeasure\_LedgerActivityMeasureGroup.LEDGERGREGORIANDATEID** および **LedgerActivityMeasure\_FiscalPeriodDateAggregateDimension.LEDGERPERIODGREGORIANDATEID** 間の結合を定義します。

4. **販売** および **YearName** フィールドを使用するマトリックス レポートを作成します。 レポートは次の例のようになります。

    ![販売および YearName フィールドを使用するマトリックス レポートの例](media/d1d0e190896bec3a755b9b586a3cb657.png)

    次に、財務分析コード値を追加します。

5. Power BI デスクトップのフィールドの一覧で、**LedgerActivityMeasure\_DimensionCombination** テーブルを展開します。 次のように、分析コード フィールドの一覧がテーブル フィールドに拡張されていることを確認します。

    ![テーブル フィールドに拡張された分析コード フィールドのリスト](media/b5099b0c03fa16f0c2ab70943c7cce8b.png)

6. レポートに **BusinessUnit\_Description** フィールドを含めます。 これで、レポートに、次の例のように、業務単位ごとの販売が表示されます。

    ![事業単位ごとの販売を示すレポート](media/c39e94631896301db6675d36fc9d3886.png)

    **BusinessUnit\_description** フィールドおよび **BusinessUnit\_Value** フィールドがあることを確認します。 値フィールドを使用すると、列のソートに使用できる数値を取得できます。

7. 新しい財務分析コードを定義し、エンティティ ストアを更新します。 
8. 更新が完了したら、**LedgerActivityMeasure\_DimensionCombination** テーブルを右クリックして、**データの更新** を選択します。 定義した新しい財務分析コードが、レポートに使用できるフィールドの一覧に反映されていることを確認します。

    ![データの更新](media/6d345e2f68dfb0413daebfd5f469db2c.png)

9. 新しい財務分析コード フィールドをレポートに含めることができます。

### <a name="creating-reports-that-use-expanded-financial-dimension-tables"></a>展開済の財務分析コード テーブルを使用するレポートを作成しています

先に説明したように、新しいテーブルはエンティティ格納で作成されました。 各財務分析コード フィールドは、新しいテーブルにも追加されます。 新しいテーブルには、名前、値、および説明の個々のフィールドが含まれています。

新しいテーブルに、レポートの作成に使用される LedgerActivityMeasure\_DimensionCombination テーブルと結合するために使用できるキーが含まれていることを確認します。 これらの追加テーブルのフィールドを使用する場合は、レポートにフィールドを含め、キーを使用して関連付けるだけです。

1. 作成済みのレポートを開きます。

    ここで、レポートに財務分析コード テーブルを追加します。

2. Power BI desktop で、メニューの **最近のソース** をクリックしてから、**AXDW** データ接続を選択します。 テーブル ナビゲーターが表示されます。
3. レポートの **LedgerActivityMeasure\_LegalEntity** テーブルを選択します。

    > [!NOTE]
    > 開発またはデモ環境を使用している場合、**LegalEntity** はデモ データで定義されている財務分析コードであるため、このテーブルが表示されます。 独自のデータで作業している場合、表示されるテーブルは定義した財務分析コードに対応します。

    ここで、レポートにある既存のテーブルに選択したテーブルを関連付けます。 

4. レポートで、**リレーションシップの管理** ダイアログ ボックスを開きます。
5. **LedgerActivityMeasure\_DimensionCombination.LegalEntity\_FK** を **LedgerActivityMeasure\_LegalEntity.KEY\_** に結合します。

手順 3 で別の分析コード テーブルを選択する場合は、対応する **FieldName\_FK** フィールドを組み合わせテーブルから分析コード テーブルの **KEY\_** フィールドに関連付ける必要があります。

## <a name="how-a-developer-can-enable-financial-dimensions"></a>開発者が財務分析コードを有効にする方法

エンティティ格納内の展開されている財務分析コードを表示する前に、開発者は集計測定の財務分析コードの使用を有効にする必要があります。 ベスト プラクティスとしては、財務データが含まれている集計測定をモデル化するときに財務分析コードが含まれている必要があります。 財務分析コードを含めるには、「財務分析コード テーブル」に基づく集計分析コードを作成します。 先に見たように、財務分析コード テーブルを使用して作成する集計分析コードはランタイムに展開されます。

### <a name="what-are-financial-dimension-tables"></a>財務分析コード テーブルとは

財務分析コード テーブルは、財務分析コード データを含むベース テーブルです。 例では、**DimensionAttributeValueCombination** および **DimensionAttributeValueSet** があります。

これらの 2 つのテーブルに基づくテーブル、ビュー、またはエンティティを使用する場合、集計分析コードのフィールドは実行時に展開されます。

LedgerActivityMeasure 集計の測定の次の例を考慮してください。

![LedgerActivityMeasure 集計の DimensionCombination 集計ディメンション](media/08437296a512478e99b3c377170edeee.png)

DimensionCombination は、DimensionAttributeValueCombination ベース テーブルを使用してモデル化される集計分析コードです。 この場合、開発者は LedgerActivityMeasureGroup メジャー グループを使用して集計分析コードを参照しました。

実行時に、システムで新しい財務分析コードが定義されると新しい分析コード フィールドが追加されます。(つまり、DimensionCombination テーブルが展開されます。)

### <a name="creating-role-playing-financial-dimensions"></a>ロールプレイング財務分析コードを作成しています

元帳データを使用して報告するとき、基本アカウントと相手勘定に関する報告が必要なことがあります。 例については、元帳トランザクションが 1 つの勘定から別の勘定への金額の転送を含む場合、基本勘定は「元」勘定、相手勘定は、「先」勘定になります。 このパターンは、*ロールプレイング ディメンション* パターンとして知られています。

基本勘定と相手勘定の両方がトランザクション データに関連付けられている必要があります。 したがって、基本勘定と相手勘定の両方の財務分析コード フィールドを拡張する必要があります。 ここで、この要件をどのように満たすことができるかを確認します。 以下の例について考えます。

![ロール プレイの分析コード例](media/062a0d860fe1633a6616bca6e871f95e.png)

LedgerActivityMeaureGroup の 2 つの分析コード参照をモデル化しました。 最初の参照、DimensionCombinationは、**LedgerDimension** フィールドを使用して結合されます。 このトピックの前のところでこのパターンを確認しました。

2 番目の参照、OffsetDimensionCombination は、同じ分析コードへの別の参照です。 DimensionCombination 集計分析コードを再使用し、それに新しい名前を付けました。 2 番目のケースでは、**OffsetLedgerDimension** フィールドを使用して参加できます。

実行時に、システムは両方の分析コードを追加のフィールドに展開します。 したがって、主およびオフセットの分析コード フィールドについてレポートすることができます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]