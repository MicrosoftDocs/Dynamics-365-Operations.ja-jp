---
title: 仕入先カタログのインポート
description: このトピックでは、仕入先カタログ データをインポートするプロセスについて説明します。
author: RichardLuan
manager: tfehr
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, CatVendorCatalogDetails, CatVendorCatalogReleaseApprovedProducts, CatVendorCMRDetails, CatVendorCatalogProductPerCompanyStatus, CatVendorMaintenanceEventLog, CatVendorCatalogReviewTool, CatVendorCatalogFileUpload, CatVendorCatalogMaintenanceRequest, CatVendorCatalogFileInLegalEntity, CatVendorCatalogSchema, CatVendorCatalogFilePreviewPane, CatVendorCatalogImportParameter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: riluan
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 6a6fc2b4fe4245a1fe5b5a7eaafe8cc7fd337ab9
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020757"
---
# <a name="import-vendor-catalogs"></a>仕入先カタログのインポート

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a>仕入先カタログのインポート

Dynamics 365 Supply Chain Management では、購買担当者が、会社の従業員が内部で使用する品目およびサービスを注文する際に使用できるカタログの作成および管理を行えます。 調達カタログを作成するには、製品カタログ データをインポートするか、製品カタログ データを手動で製品マスターに追加することにより、従業員が使用できるようになる品目とサービスを追加できます。 

Microsoft Dynamics 365 クライアントから、仕入先より送信されたカタログ データをアップロードすることができます。

仕入先がユーザーに送信する製品データは、カタログ保守要求 (CMR) ファイルの形式で、XML ファイル形式でなければなりません。 CMR ファイルには、仕入先が会社に提供する製品の詳細が含まれている必要があります。

## <a name="import-vendor-catalog-data"></a>仕入先カタログ データのインポート

仕入先データ カタログをインポートするには、次のタスクを実行する必要があります。

1. データ マッピング ルールが定義されているデータ管理ワークスペースで、プロジェクトを設定します。 **データ管理** を選択し、**データ プロジェクトのロールの設定** を選択します。

2. 調達カテゴリ階層を設定し、仕入先を調達カテゴリに割り当てます。 商品コードを使用している場合は、調達カテゴリに商品コードを追加します。 調達カテゴリ階層の設定の詳細については、次を参照してください。[調達カテゴリ階層の設定](../procurement/tasks/set-up-procurement-category-hierarchy.md)

3. 仕入先をカタログ インポート用にコンフィギュレーションします。 仕入先を選択し、**調達** > **設定** > **仕入先カタログ インポートの構成** を選択します。

4. ワークフローをカタログ インポート用にコンフィギュレーションします。 CMR ファイル テンプレートを作成し、これを仕入先と共有します。

5. **調達** \> **共通** \> **カタログ** \> **仕入先カタログ** を選択して、仕入先のカタログを作成します。 仕入先から受け取るカタログ保守要求 (CMR) ファイルがこのカタログでグループ化されます。 

6. CMR ファイルをアップロードします。

7. 仕入先カタログで製品を確認、承認または却下します。 製品は、調達カテゴリに自動的にマップされます。 

承認済製品は、製品マスターに追加され、選択した法人にリリースされます。 承認済製品のみ調達カタログに追加できます。

## <a name="generate-a-catalog-import-file-template"></a>カタログ インポート ファイル テンプレートの生成

カタログ インポート ファイル テンプレートは、仕入先の製品の CMR ファイルの作成に使用する XSD ファイルです。 CMR ファイルを使用して、新しいカタログの作成、既存のカタログの置換、または既存のカタログの変更を行うことができます。

1. **調達とソーシング** \> **カタログ** \>**仕入先カタログ** を選択し、使用するカタログをダブル クリックします。

2. 現在のカタログ インポート テンプレート (XSD ファイル) をダウンロードします。 **関連情報** グループで、**カタログ** タブ、**アクション ウィンドウ** の、**更新カタログ** ページで、**カタログ テンプレートの生成** をクリックし、**調達カテゴリ** を選択します。

    - **調達カテゴリ** オプションを使用すると、仕入先が製品の提供を許可されている調達カテゴリを含むカタログ テンプレートを生成できます。

3. **名前を付けて保存** ダイアログ ボックスで、カタログ ファイル テンプレートを保管する場所を選択したり、ファイルを保存します。

詳細および例については、このブログ投稿を参照してください: [Dynamics AX の仕入先カタログ](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]