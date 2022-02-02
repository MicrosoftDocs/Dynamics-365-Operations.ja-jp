---
title: 製品情報の概要
description: このトピックでは、製品情報の管理に関する情報を提供します。 製品情報の管理では、すべての法人の製品定義、カテゴリ、識別子、および製品の特定のコンフィギュレーションを業務プロセスに合わせて共有します。
author: t-benebo
ms.date: 06/01/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductListPage, EcoResProductVariantMaintainWorkspace, EcoResProductVariantPerCompanyImagePart, EcoResProductRelationType,EcoResProductAvailabilityPart,  EcoResProductReleasedSelect, EcoResProductLookup, EcoResProductVariantsPendingReleaseFormPart, EcoResProductSearchLookup, EcoResProductNumberRename, EcoResDimensionBasedConfigWorkspace, EcoResProductVariantImagePart, EcoResProductImagePart, EcoResProductVariantsPerCompanyPart, InventItemIdLookupByDefaultOrderSetting, EcoResProductReleaseSessions, EcoResProductVariantMaintainWorkspaceConfiguration, EcoResProductProcessManufacturingWorkspaceConfiguration, EcoResProductMasterVariantsPart, EcoResProductDiscreteManufacturingWorkspaceConfiguration, EcoResProductVariantAvailabilityPart, EcoResProductInformationFactBox, EcoResProductLookupTest, EcoResProductImageTest, EcoResProductReleasedRecentlyCreatedFormPart, EcoResPhysicalProductDimensions, PdsMRCRegulatedListItem, EcoResProductAvailabilityPart, PdsMRCRestrictionList, InventItemIdLookupAllocationId, EcoResProductAvailability, EcoResProductEntityAttributeTableFieldAssociation, EcoResProductImagePart, EcoResProductRelation, EcoResProductReleaseAddProduct, EcoResProductPerCompanyListPage, EcoResProductParameters, PdsMRCRestrictedItemByCountryState, EngChgCasePreview, InventTablePreview, PdsMRCItemDetails, EngChgCaseAssociate, PdsMRCCustomerHistory, PdsMRCVendorHistory, PdsMRCRestrictedCountryStateByItem, InventItemIdGroupLookup, InventLocationLookup, PdsMRCValidityIntervalbyCountry, PdsMRCValidityIntervalbyCountry, PdsMRCEventTracker, PdsMRCReportingCountry, PdsMRCDocument, PdsMRCReportingList, PdsMRCItemCAS, GraphicsTestForm, EngChgPicklist
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf814ec7c76ff2a8fd6bb4f7bbf8aec109465e34
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984323"
---
# <a name="product-information-overview"></a>製品情報の概要

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、製品情報の管理に関する情報を提供します。 製品情報の管理では、すべての法人の製品定義、カテゴリ、識別子、および製品の特定のコンフィギュレーションを業務プロセスに合わせて共有します。 

製品情報は、すべての業界のサプライ チェーンとコマース アプリケーションのバックボーンです。 これは、製品に関する情報を集中管理することに重点を置くプロセスや技術を指します (たとえば、サプライ チェーン全体で)。 製品定義、文書、属性、および使用される識別子を共有することは重要です。 ビジネス ソリューションのさまざまなモジュールでは、特定の製品、製品ファミリー、または製品カテゴリに関連する業務プロセスを管理するために製品固有の情報およびコンフィギュレーションが必要です。

## <a name="product-definition"></a>製品定義

製品は、主に、製品番号、名前、および説明によって定義されます。 しかし、製品またはサービスを説明するためには、他のデータも必要です:

- 製品タイプ: 品目またはサービス
- 製品サブタイプ: 特徴的製品または製品マスター
- 製品バリアント モデルの定義:

     - 製品分析コードおよび分析コード グループ
     - 製品の分類
     - 製品コンフィギュレーション モデル

- 製品と 1 つ以上のカテゴリの関連付け
- 製品およびカテゴリ属性の定義
- 製品画像
- アタッチメント
- 測定単位および関連する変換
- すべての名前と説明の翻訳

## <a name="distribution-export-and-import-of-product-data"></a>配分、エクスポート、および製品データのインポート

Supply Chain Management で製品定義を作成することができます。 製品ライフサイクル管理 (PLM)、製品データ管理 (PDM)、製品情報管理 (PIM) システムからインポートすることもできます。 複数の Supply Chain Management インスタンスが使用されている場合、1 つのインスタンスは通常、他のすべてのインスタンスの製品データのマスターとして使用されます。 この方法は、1 つのインスタンスから別のインスタンスへの製品定義データのエクスポートおよびインポートを可能にする大量のデータ エンティティによってサポートされています。

多くのインスタンスへの製品データの配分をサポートするために、Supply Chain Management では Microsoft Dataverse を使用できます。 製品定義は、Supply Chain Management のインスタンスから Microsoft Dataverse にエクスポートできます。 製品定義を使用して、Dynamics 365 Sales などの他のビジネス アプリケーションに製品データをプロビジョニングすることができます。

動的および迅速な組織では、製品情報のデータが毎日変わることに注意してください。 したがって、正確および実際の製品データの管理は、それ自体が重要な業務プロセスです。

## <a name="product-masters-and-product-variants"></a>製品マスターと製品バリアント

製品がお客様の要件に迅速に適応されなければならないアジャイル環境では、製品定義は、特徴的製品の代わりに一連の製品を指定します。 Supply Chain Management では、これらの汎用製品は *製品マスター* として知られています。 製品マスターは、特徴的製品が業務プロセスでどのように説明され、動作されるかを指定する定義およびルールを保持します。 これらの定義に基づいて、特徴的製品を生成できます。 これらの特徴的製品は、*製品バリアント* として知られています。

製品マスターは製品分析コード グループおよびビジネス ルールを指定するコンフィギュレーション テクノロジに関連付けられています。 製品分析コード (色、サイズ、スタイル、およびコンフィギュレーション) は、関連製品の特定の動作を定義および追跡するためにアプリケーション全体で使用できる特定の属性セットです。 これらの分析コードは、ユーザーが製品を検索して識別するのにも役立ちます。

## <a name="configuration-technologies"></a>コンフィギュレーション テクノロジ

3 つのコンフィギュレーション テクノロジから選択できます:

- 事前定義されたバリアントは、事前定義された品目分析コードによって定義されます。 バリアント定義には、色、スタイル、およびサイズなど、特定の有効な分析コードの組み合わせの定義が含まれます。 各組み合わせは、特徴的製品のバリアントを生成します。
- 分析コードベースのコンフィギュレーションでは、通常、製造シナリオで使用され、部品表 (BOM) の定義でコンフィギュレーション分析コードを使用できるようにします。 特定のコンフィギュレーションが選択されていると、計画および生産のコンフィギュレーションで有効な BOM 明細行のサブセットが使用されます。 1 つの共有 BOM が製品のすべてのコンフィギュレーションに使用されるため、この概念は *グローバル BOM* としても知られています。
- 制約ベースの構成では、製品コンフィギュレーション モデルを使用して、すべての可能な属性および 1 つのモデルですべての可能な製品のバリアントを記述するために必要なコンポーネントについて説明します。 属性の組み合わせの制約は、正規表現またはテーブル制約ベースによって表すことができます。 コンフィギュレーション モデルおよびコンフィギュレーションは、製品情報管理においてより重要になり、すべての業界で使用されています。

Supply Chain Management の実装を計画する場合は、業務プロセスの正しいコンフィギュレーション テクノロジを選択することが非常に重要です。 製品は、実装後に 1 つのモデルから別のモデルに変換することはできません。

## <a name="product-variant-model-definition-workspace"></a>製品バリアント モデル定義のワークスペース

**製品バリアント モデル定義** ワークスペースは、製品マスターの概要を示します。 特定の法人へのマスターおよび関連するバリアントのリリースのステータスも示します。

## <a name="released-products"></a>リリースされた製品

特定の法人にリリースされる製品は、*リリース済製品* として知られています。 製品は一度に 1 つの法人または多くの法人に一括してリリースすることができます。 製品のさまざまなプロパティおよび属性を法人単位で追加する必要がある場合には、**リリース済製品の保守** ワークスペースで、各法人または法人の下位組織で最近リリースされた製品を監視および完了させることができます。

### <a name="released-product-maintenance-workspace"></a>[リリース済製品の保守] ワークスペース

**リリース済製品の保守** メニュー項目から **リリース済製品の保守** ワークスペースをコンフィギュレーションすることができます。 カテゴリ階層およびカテゴリを選択し、ワークスペースをフィルタ処理します。 ワークスペース内の関連する製品データを調整するには、**最近リリース済の製品** および **リリース済製品の停止** のタイム フェンスを日数で定義することもできます。

ワークスペースは、タイルの集計および 2 つのリストで構成されます。 **オープンなケース** リストでは、完了および終了していない選択した製品カテゴリ階層内の製品の製品変更ケースが表示されます。 **最近リリース済** リストには、ワークスペースのコンフィギュレーションで設定されているタイム フェンス内にリリースされた製品が表示されます。 一覧の各品目について、検証が実行され、および検証ステータスが表示されます。 このステータスは、法人の必要なコンフィギュレーションが完了していないことを示す場合があります。 一覧から、**リリース済製品の詳細**、**製品属性の保守**、**製品カテゴリの保守**、**既定の注文設定**、および製品の必要なコンフィギュレーションを完了する **テキストの翻訳** ページに直接アクセスできます。

### <a name="manually-creating-a-new-released-product"></a>新たにリリースされた製品を手動で作成する

組織の業務プロセスおよびこの機能を使用するかどうかに関するルールに応じて、リリース済み製品を手動で一度に作成することができます。 この機能は、新しい製品を作成し、それを現在の法人に自動的にリリースします。 新しい製品を作成するには、**リリース済製品の保守** ワークスペース、または **リリースされた製品** リスト ページ内の **リリース済製品** をクリックします。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]