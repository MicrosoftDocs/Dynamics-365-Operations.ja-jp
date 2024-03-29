---
title: ER ドキュメント管理ファイルを形式出力で使用する (第 2 部 - データ モデルの拡張)
description: この記事では、ER 出力でドキュメント管理ファイル (添付ファイル) を使用するために電子申告 (ER) 形式を構成する方法について説明します。 (第 2 部)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
ms.openlocfilehash: 9d0d87d23bcdf537d638502fb5217f32fd1b328e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290997"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a>ER ドキュメント管理ファイルを形式出力で使用する (第 2 部 - データ モデルの拡張)

[!include [banner](../../includes/banner.md)]

次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。 これらの手順はどのタイプの企業でも実施できます。

これらの手順を完了するには、まず 「フォーマット出力のドキュメント管理ファイルを ER 使用する（パート1：データモデルを作成）」 作業ガイドに記載の手順を完了する必要があります。

この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a>データモデルを拡張して、そのモデルにあるドキュメント管理ファイルを表示します。
1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。
2. [コンフィギュレーションをレポートする] をクリックします。
3. ツリーで、「Customer invoice model」を選択します。
4. ツリーで、[Customer invoice model\Customer invoice model (custom)]を選択します。
5. [デザイナー] をクリックします。
6. ツリーで、「Customer invoice(InvoiceCustomer)」を選択します。
    * このデータ モデルを拡張して、販売注文に添付されたファイルに適用させます。この販売注文は電子的処理の請求書に関連付けられています。  
7. [新規] をクリックすると、ドロップ ダイアログが開きます。
8. [名称] フィールドで、「添付請求書」を入力します。
    * 添付請求書  
9. [品目タイプ] フィールドで、「レコード リスト」を選択します。
10. [追加] をクリックします。
11. [新規] をクリックすると、ドロップ ダイアログが開きます。
12. [名称] フィールドで、「ファイルコンテンツ」を入力します。
    * ファイルの内容  
13. [品目タイプ] フィールドで、「コンテナー」を選択します。
14. [追加] をクリックします。
15. [新規] をクリックすると、ドロップ ダイアログが開きます。
16. [名称] フィールドで、「ファイル名」を入力します。
    * ファイル名  
17. [品目タイプ] フィールドで、「String」を選択します。
18. [追加] をクリックします。

## <a name="map-new-data-model-elements-to-data-sources"></a>新規データ モデル・エレメントをデータ ソースにマッピングする
1. [モデルからデータ ソースへのマップ] をクリックします。
2. クイック フィルターを使用し、 「InvoiceCustomer」の値により「定義」フィールドでフィルターします。
    * 顧客への請求  
    * 新規モデルエレメントを該当するデータソースにマッピングします。  
3. [デザイナー] をクリックします。
4. ツリーで、「Invoice attachments」を選択します。
5. ツリーで、「Invoice attachments」を展開します。
6. ツリーで、「Invoice attachments\File name」を選択します。
7. [編集] をクリックします。
8. 「式」フィールドで、「CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'.'originalFileName()」を入力します。
    * CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'.'originalFileName()'  
9. [保存] をクリックします。
10. ページを閉じます。
11. ツリーで、「Invoice attachments\File content」を選択します。
12. [編集] をクリックします。
13. 「式」フィールドで、「CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'.'getFileContentAsContainer()」を入力します。
    * CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'.'getFileContentAsContainer()'  
14. [保存] をクリックします。
15. ページを閉じます。
16. ツリーで、「Invoice attachments」を選択します。
17. [編集] をクリックします。
18. 「式」フィールドで、「CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents」を入力します。
    * CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'  
19. [保存] をクリックします。
20. ページを閉じます。
21. [保存] をクリックします。
22. ページを閉じます。
23. ページを閉じます。
24. ページを閉じます。
25. [状態の変更] をクリックします。
26. [完了] をクリックします。
27. [OK] をクリックします。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
