---
title: Dataverse 仮想テーブル クエリの最適化
description: Dataverse 仮想テーブル クエリのパフォーマンスの最適化およびトラブルシューティング
author: twheeloc
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1f379cd7783cc984666582d2c680a1db013627ce
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070175"
---
# <a name="optimize-dataverse-virtual-table-queries"></a>Dataverse 仮想テーブル クエリの最適化


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



## <a name="issue"></a>出庫

### <a name="overview"></a>概要

Dataverse 仮想テーブルを使用して Dynamics 365 Human Resources との統合やその他のデータ接続を開発する場合、仮想テーブルに対するクエリでパフォーマンスの問題が発生する可能性があります。 クエリの実行が遅い場合、さまざまなクライアントまたはインターフェイスで発生する可能性があります。 たとえば、次のような状況で問題が発生する可能性があります。

- Dataverse Web API を介して仮想テーブルをクエリする場合
- 仮想テーブルに対して Power App を作成する場合
- 仮想テーブルで Power BI レポートを作成する場合

これらのインターフェースはすべて、パフォーマンスの問題を表面化する可能性があります。

Human Resources の Dataverse 仮想テーブルでパフォーマンスが低下する原因の 1 つは、テーブルの[ナビゲーション プロパティ](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) に関連する仮想テーブルの外部キー列です。 仮想テーブルのナビゲーション プロパティが作成されると、関連する仮想テーブルのキー列のキーの値を表す外部キー列がテーブルに自動的に追加されます。 たとえば、**_mshr_fk_person_id_value** 列は、**mshr_dirpersonentity** エンティティの外部キー プロパティを使用して **mshr_hcmworkerbaseentity** エンティティに追加されます。 これらの外部キー列の値がテーブルでどのように維持されるかにより、値をフェッチすると、仮想テーブルに対するクエリのパフォーマンスに悪影響を与える可能性があります。

### <a name="potential-symptoms"></a>潜在的な現象

この影響が見られる例は、作業者 (**mshr_hcmworkerentity**) または基本作業者 (**mshr_hcmworkerbaseentity**) エンティティに対するクエリです。 さまざまな方法でパフォーマンスの問題が発生する可能性があります。

- **クエリの実行が遅い**: 仮想テーブルに対するクエリは予期された結果を返す場合がありますが、クエリの実行が完了するまでに予想よりも時間がかかります。
- **クエリのタイムアウト**: クエリがタイムアウトし次のエラーが返される場合があります。「財務と運用を呼び出すためのトークンが取得されましたが、財務と運用はタイプ InternalServerError のエラーを返しました。」
- **予期しないエラー**: クエリは、「予期しないエラーが発生しました」というメッセージとともにエラー タイプ 400 を返す場合があります。

  ![HcmWorkerBaseEntity のエラー タイプ 400。](./media/HcmWorkerBaseEntityErrorType400.png)

- **調整**: クエリはサーバー リソースを過剰に使用し、調整の対象になる可能性があります。 この場合、クエリは次のエラーを返します: 「財務と運用を呼び出すためのトークンが取得されましたが、財務と運用はタイプ 429 のエラーを返しました。」 Human Resources の調整の詳細については [スロットリングに関するよく寄せられる質問](./hr-admin-integration-throttling-faq.md) を参照してください。

  ![HcmWorkerBaseEntity のエラー タイプ 429。](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a>解決策

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a>データ クエリに含める列の数の制限

仮想テーブルの場合、クエリ パフォーマンスを向上させる可能性が最も高い方法の 1 つは、クエリで選択される列の数を制限することです。 クエリ パフォーマンスを最適化するための一般的なガイダンスは、クエリで返される列を必要なプロパティのみに制限することです。 これは特に、仮想テーブルの外部キー列に当てはまります。 統合またはレポートに外部キー列の値が必要ない場合は、外部キー列を除いて、必要な列のみを選択するようにクエリを構成します。

#### <a name="selecting-columns-in-an-odata-query"></a>OData クエリで列の選択

Dataverse Web API を介して仮想テーブルをクエリする場合、**$select** システム クエリ オプションを使用してクエリに含まれる列の数を制限し、結果を返す必要がある列を定義できます。 パフォーマンスを最大限に高めるには、外部キー列 (**_mshr_FK_** 接頭語を持つ列) をクエリから除外します。

たとえば、次の **mshr_hcmworkerbaseentity** エンティティに対するクエリには、外部キー値を除き、**$select** クエリ オプション句に含まれる列のみが含まれます。 これにより、すべてのテーブル列を含むクエリのパフォーマンスが大幅に向上します。

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

選択する列の数を制限するという推奨事項は、**$expand** クエリ オプションを使用して、ナビゲーション プロパティを介して関連する仮想テーブルにクエリを展開する場合にも適用されます。 たとえば、次のクエリには、**mshr_hcmworkerbaseentity** エンティティの列と、**mshr_dirpersonentity** エンティティの拡張列が含まれています。 **$select** クエリ オプションは **$expand** クエリ オプション句に含まれます。

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

**$expand** クエリ オプション句で **$select** クエリ オプションを使用してデータを取得する場合、エンティティ間のナビゲーション プロパティが多対一の関係の場合は、通常のパフォーマンスが向上します。 一対多の関係を展開する場合、クエリ実行時間の同じ減少が見られない場合があります。 Dataverse 仮想テーブルのリレーションシップの定義の詳細については 、[テーブル リレーションシップ](/powerapps/maker/data-platform/create-edit-entity-relationships) を参照してください。

Dataverse Web APIで **$select** および **$expand** システム クエリ オプションを使用する方法の詳細については、[クエリで関連エンティティレコードを取得する](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query) を参照してください。

#### <a name="selecting-columns-in-power-bi"></a>Power BI で列を選択します

Dataverse 仮想テーブルに対して Power BI レポートを構築する際にパフォーマンスが低下が見られる場合、レポートのテーブルから選択した列から外部キー列を除外することでパフォーマンスを改善できます。 たとえば、Power BI Desktop を使用して **mshr_hcmworkerbaseentity** エンティティに対してレポートを作成する場合は、次の手順を使用して、レポート クエリに含めたい列を選択できます。

1. Power BI Desktop で、アクション リボンの **データの取得** ドロップダウン リストから **詳細...** を選択します。
2. **データの取得** ウィンドウで、検索ボックスの **Common Data Service** に入力し、**Common Data Service** コネクタを選択して、**接続** を選択します。
3. Common Data Service ウィンドウの **サーバーの URL** に Dataverse 環境の組織 URI を入力し **OK** を選択します。
  
   ![Dataverse 環境の URI を入力。](./media/PowerBIDataverseURLSetup.png)
  
4. ナビゲーター ウィンドウで、**エンティティ** ノードを展開します。
5. 検索ボックスに **mshr_hcmworkerbaseentity** を入力し、エンティティを選択します。
6. **データの変革** を選択します。
7. Power Query エディター ウィンドウで、**高度なエディター** を選択します。
8. **高度なエディター** ウィンドウで、クエリを以下のように更新し、必要に応じて列を追加または削除します。

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Power Query エディターの詳細エディターでクエリを更新します。](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. **完了** を選択します。

   > [!NOTE]
   > 更新前にクエリからタイプ 429 のエラーを以前に受け取った場合は、クエリを更新して正常に完了する前に、再試行期間を待つ必要がある場合があります。

10. Power Query  エディター アクション リボンで **閉じて適用** をクリックします。

仮想テーブルから選択した列に対して Power BI レポートの構築を開始できます。

#### <a name="selecting-columns-in-power-apps"></a>Power Apps で列を選択します

Dataverse Web API クエリおよび Power BI と同様に、関連するテーブルの列をアプリから除外することにより、Dataverse 仮想テーブルに基づく Power Apps のクエリ パフォーマンスを向上させることができます。 関連テーブルの列がページに含まれている場合、データをフェッチするために作成されたリ要求 URL には、関連テーブルの外部キー プロパティが含まれます。 これは、上記の [OData クエリで列を選択](#selecting-columns-in-power-apps) した例のように、追加のデータ ルックアップが発生してパフォーマンスを低下させます。

これを回避するために、関連するテーブルのデータ フィールドが Power App のどのデータ フォームにも含まれていないことを検証できます。

1. ツリー ビュー ペインで、画面のデータ フォームを選択します。
2. **プロパティ** ペインで、**フィールド** プロパティで **編集** を選択します。
3. **データ** ペインで、選択したフィールドのいずれもデータ ソースの仮想テーブルのフィールドではないことを確認します。

たとえば、アプリのページに含まれるデータ フィールドの 1 つが、**作業者** が関連テーブルである **ThisItem.Worker.Name** などの別のテーブルを参照している場合、データのフェッチのパフォーマンスが低下しする可能性があります。

[Power Apps 監視](/powerapps/maker/monitor-overview) を使用すると、必要な列だけが Power App のデータを取得するためにクエリに含まれている必要があります。 getRows 操作用に作成された URL を表示して、アプリ用に選択した列がデータの取得に最適であることを確認できます。

![Power Apps 監視を使用して getData 操作を分析します。](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a>データ クエリのフィルター処理

クエリの実行のパフォーマンスを改善するもう 1 つの方法は、クエリ結果で返されるレコードの数を制限する方法です。 これを行うには、結果をフィルタリングして、必要なレコードのみを受信するようにします。

クエリ データのフィルター処理の詳細については、[フィルタ結果](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) を参照してください。

### <a name="limiting-the-page-size-of-the-query"></a>クエリのページ サイズの制限

大規模なデータ セットを使用している場合は、データ クエリに `odata.maxpagesize` 優先設定ヘッダーーを追加することで、クエリ結果を複数のページに分割できます。

ページングの詳細については、[ページに返すエンティティの数の指定](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page) を参照してください。

## <a name="see-also"></a>参照

- [構成 Dataverse 仮想テーブル](hr-admin-integration-common-data-service-virtual-entities.md)
- [Human Resources 仮想テーブルに関するよく寄せられる質問](hr-admin-virtual-entity-faq.md)
- [スロットリングに関するよく寄せられる質問](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

