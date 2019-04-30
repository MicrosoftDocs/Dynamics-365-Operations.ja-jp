---
title: Dynamics 365 for Talent の新機能および変更された機能 (2019 年 2 月 27 日)
description: このトピックでは、Microsoft Dynamics 365 for Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 02/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d8e6a02b43ad60e3a0c4382f98cb808066587da7
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/12/2019
ms.locfileid: "949900"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-27-2019"></a>Dynamics 365 for Talent の新機能および変更された機能 (2019 年 2 月 27 日)

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2163 に適用されます。

### <a name="add-a-custom-fields-menu-item-to-system-administration"></a>システム管理にカスタム フィールドのメニュー項目を追加する

**システム管理**ワークスペースに追加された**カスタム フィールド**メニューに移動します。

### <a name="hide-the-import-and-create-options-for-new-mobile-applications"></a>インポートを非表示にし、新しいモバイル アプリケーションのオプションを作成する

現時点では、Talent で新しいモバイル アプリケーションを作成することはできません。 新しいモバイル エクスペリエンスを作成するオプションは、**モバイル アプリ**メニューから削除されました。

### <a name="variable-compensation-award-dmf-entity"></a>変動報酬 (DMF エンティティ)

今回のリリースでは、**変動報奨** Data Management Framework (DMF) エンティティがエクスポートに使用できるようになりました。

### <a name="uk-addresses-appear-in-the-personnel-management-analytics-page-as-swiss-addresses"></a>英国の住所が、スイスの住所として人事管理分析ページに表示される

今回のリリースでは、市町村で住所が表示されます。 今回のリリースでは、表示機能が従業員の居場所を誤って表現していた問題が修正されています。

### <a name="the-workforce-power-bi-report-shows-an-error-when-a-workers-seniority-date-is-on-leap-day"></a>作業者の勤続日数がうるう日の場合、要員指標 Power BI レポートにエラーが表示される

2 月 29 日に当たる勤続日数を考慮するように Microsoft Power BI が修正されました。

### <a name="employee-fixed-compensation-employee-variable-awards-employee-variable-plans-enrollments-allow-for-custom-fields"></a>従業員の固定報酬、従業員の変動報酬、従業員の変動プラン (登録) はカスタム フィールドを許可する

カスタム フィールドは、従業員の固定報酬、従業員の変動報酬、および従業員の変動プラン (登録) に追加できるようになりました。 既定で利用可能な情報に加えて、従業員の固定報酬および変動報酬プランに関する詳細情報を追跡できるようになりました。 カスタム フィールドは、ユーザー インターフェイスまたは提供されているエンティティを通じて入力および更新できます。

### <a name="other-miscellaneous-bug-fixes"></a>その他の雑費のバグ修正

このリリースには、他のマイナーなバグ修正が含まれています。

## <a name="coming-soon"></a>間もなく公開

### <a name="advanced-compensation-security-fixed-and-variable"></a>高度な報酬セキュリティ (固定および変動)

多くの組織では、報酬および福利厚生の管理者は特定の報酬レコードにのみアクセスできます。 これらのレコードは、経営幹部または地域の従業員向けのものである可能性があります。 この変更により、人事管理 (HR) は組織内のさまざまな従業員数の報酬プランを管理および維持できます。 固定および変動プランに割り当てることができるセキュリティ ロールは、それらのプランへのアクセス権とそれらに関連する従業員データ (たとえば給与情報や特別償却レコードなど) を決定します。 指定されたアクセス権を持つロールのみが、それらの従業員の報酬を処理できます。

### <a name="platform-update-24"></a>プラットフォーム update 24

Microsoft Dynamics 365 for Finance and Operations プラットフォーム更新 24 (2019 年 3 月) の詳細については、[Finance and Operations プラットフォーム更新プログラム 24 (2019 年 3 月) のプレビュー](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24) を参照してください。

### <a name="make-employee-fixed-compensation-available-for-future-position-assignments"></a>従業員の固定報酬を将来の職位の割り当てに使用できるようにする

通常、組織に参加する従業員は、将来の開始日を持っています。 この変更により、将来の職位の割り当てを持つ従業員に対して固定報酬が定義されるようになります。

## <a name="known-issues"></a>既知の問題

### <a name="changes-to-the-core-hr-integration-template-talent-common-data-service-to-finance-and-operations"></a>Core HR 統合テンプレートに対する変更 (Talent Common Data Service から Finance and Operations)
Core HR のテンプレートは、「高度なクエリ テンプレート」に更新されています。 したがって、既定では、高度なクエリはこのテンプレートを使用して作成されたプロジェクトに使用できます。 さらに、既定のマッピング機能は、高度なクエリ エディターでのみ表示されます。 (既定のマッピング機能は「FN」としてマッピングに表示されます)。

マッピング エラーの詳細については、[Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年12月14 日)](https://docs.microsoft.com/dynamics365/unified-operations/talent/whats-new-talent-december-14) を参照してください。

新しいテンプレートを使用するには、新しいプロジェクトを作成し、新しい Talent 統合テンプレートを選択します。

既存のテンプレートを更新するには、これらの手順を実行します。

1. 次のマッピングを更新します:

    - **ジョブ職位から職位:** このマッピングを削除します。
    - **ジョブ職位から職位親ジョブ割り当て:** このマッピングを削除します。
    - **ジョブ職位から基本職位:** 新しいマッピングを**ジョブ職位** Common Data Service エンティティから**基本職位** Finance and Operations エンティティに追加します。 シーケンス内の職位 7 に移動します。

        [![ジョブ職位から基本職位マッピング](./media/CDS-Mapping1.png)](./media/CDS-Mapping1.png)

    - **ジョブ職位から職位の詳細:** 新しいマッピングを**ジョブ職位** Common Data Service エンティティから**職位の詳細** Finance and Operations エンティティに追加します。 シーケンス内の職位 8 に移動します。

        [![ジョブ職位から職位の詳細マッピング](./media/CDS-Mapping2.png)](./media/CDS-Mapping2.png)

    - **ジョブ職位から職位の期間:** 新しいマッピングを**ジョブ職位** Common Data Service エンティティから**職位の期間** Finance and Operations エンティティに追加します。

        [![ジョブ職位から職位の期間マッピング](./media/CDS-Mapping3.png)](./media/CDS-Mapping3.png)

    - **ジョブ職位から職位階層:** 新しいマッピングを**ジョブ職位** Common Data Service エンティティから**職位階層** Finance and Operations エンティティに追加します。 **高度なクエリ**を選択して、高度なクエリをプロジェクトに対して使用できるようにします。

       [![高度なクエリ ボタン](./media/CDS-Advanced-Query.png)](./media/CDS-Advanced-Query.png)

2. 次のマッピングを追加します。
    
    [![マッピング](./media/CDS-Mapping4.png)](./media/CDS-Mapping4.png)

    1. cdm_jobpositionnumber cdm_jobspositionnumb... = POSITIONID cdm_parentjobpositionid.cdm-jobpositionnumb... = PARENTPOSITIONID cdm_validfrom cdm_validfrom = VALIDFROM cdm_validto cdm_validto = VALIDTO
       
    2. **検索**フィールドの隣の**高度なクエリおよびフィルター処理**リンクを選択します。  

    3. **cdm_parentjobpositionid.cdm_jobpositionnumber** 列を検索し、その右側にある下矢印ボタンを選択します。

    4. 表示されるダイアログ ボックスで、**空にする**を選択します。

    5. **列の追加 \> 条件付き列の追加**を選択して、HIERARCHYTYPENAME の既定値の変換を追加します。

        [![条件付き列のコマンドの追加](./media/Add-column.png)](./media/Add-column.png)

    6. **条件付き列の追加**ダイアログ ボックスに、新しい列の名前として **HIERARCHYTYPENAME** と入力します。
    7. 条件の **If** の部分で、任意のフィールドを選択して、リレーションシップとして**次の値に等しい**を使用し、任意の値を入力します。 条件の **Then** および **Otherwise** の部分で、既定値を指定します。 この場合は、両方の部分に**行**を入力します。

        [![条件付きの列のダイアログ ボックスの追加](./media/Add-conditional-column.png)](./media/Add-conditional-column.png)

    8. **OK** を選択して、**高度なクエリおよびフィルター処理**ダイアログ ボックスを閉じます。
    9. **マッピング タスク**ページで、HIERARCHYTYPENAME の別のマッピングを作成するソースとして新しい列を選択します。

        [![マッピング](./media/CDS-Mapping5.png)](./media/CDS-Mapping5.png)
