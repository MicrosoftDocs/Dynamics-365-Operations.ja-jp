---
title: ER 形式の出力 (パート 3 - 形式の作成) におけるドキュメント管理ファイルの使用
description: このトピックでは、ER 出力でドキュメント管理ファイルを使用するために電子申告形式を構成する方法について説明します。 (パート 3)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0cb052e2895cd0eb7f5c3bea9f33d988ef54dfb11e2e31c4212706b7fdaada79
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766388"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a>ER 形式の出力 (パート 3 - 形式の作成) におけるドキュメント管理ファイルの使用

[!include [banner](../../includes/banner.md)]

次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。 これらの手順はどのタイプの企業でも実施できます。

これらの手順を完了するには、まず 「フォーマット出力のドキュメント管理ファイルを ER 使用する（パート2：データモデルを拡張）」作業ガイドに記載の手順を完了する必要があります。

この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。


## <a name="create-a-format-to-process-invoices"></a>請求書を処理するフォーマットを作成する
1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。
2. [コンフィギュレーションをレポートする] をクリックします。
3. ツリーで、「Customer invoice model」を選択します。
4. ツリーで、[Customer invoice model\Customer invoice model (custom)]を選択します。
    * 販売注文に添付されるファイル情報がある電子メッセージを生成するにはフォーマットを作成します。当該ファイルは電子処理請求書に関連付けられています。  
5. [コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。
6. [新規] フィールドで、「データモデル・顧客請求書モデル（カスタム）に基づくフォーマット」を入力します。
7. [名称] フィールドに、「電子請求書サンプル メッセージ」を入力します。
    * 電子請求書のサンプル メッセージ  
8. [データモデル定義] フィールドで、値を入力または選択します。
    * 顧客への請求  
9. [コンフィギュレーションの作成] をクリックします。

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a>添付ファイルをMIME形式のメッセージにする設定のフォーマットをデザインする
1. [デザイナー] をクリックします。
2. [ルートの追加] をクリックして、ドロップ ダイアログを開きます。
3. ツリーで、[XML\Element] を選択します。
4. [名称] フィールドに、「Invoice」を入力します。
    * 請求書  
5. [OK] をクリックします。
6. [追加] をクリックしてドロップ ダイアログを開きます。
7. ツリーで、[XML\Attribute] を選択します。
8. [名称] フィールドに、「SalesOrder」を入力します。
    * SalesOrder  
9. [OK] をクリックします。
10. [属性を加える] をクリックします。
11. [名称] フィールドで、「InvoiceNumber」を入力します。
    * InvoiceNumber  
12. [OK] をクリックします。
13. [属性を加える] をクリックします。
14. [名称] フィールドに、「'InvoiceAmount」を入力します。
    * InvoiceAmount  
15. [OK] をクリックします。
16. [追加] をクリックしてドロップ ダイアログを開きます。
17. ツリーで、[XML\Element] を選択します。
18. [名称] フィールドに、「EnclosedDocs」を入力します。
    * EnclosedDocs  
19. [OK] をクリックします。
20. ツリーで、「Invoice\EnclosedDocs」を選択します。
21. [エレメントの追加] をクリックします。
22. [名前] フィールドで、「Document」を入力します。
    * 書類  
23. [OK] をクリックします。
24. ツリーで、「Invoice\EnclosedDocs\Document」を選択します。
25. [追加] をクリックしてドロップ ダイアログを開きます。
26. ツリーで、[XML\Attribute] を選択します。
27. [名称] フィールドで、「FileName」を入力します。
    * FileName  
28. [OK] をクリックします。
29. [追加] をクリックしてドロップ ダイアログを開きます。
30. ツリーで、[XML\Element] を選択します。
31. [名称] フィールドで、「FileContent」を入力します。
    * FileContent  
32. [OK] をクリックします。
33. ツリーで、「Invoice\EnclosedDocs\Document\FileContent」を選択します。
34. [追加] をクリックしてドロップ ダイアログを開きます。
35. ツリーで、「'Text\Base64」を選択します。
36. [OK] をクリックします。

## <a name="map-format-elements-to-data-model-as-data-source"></a>フォーマットエレメントをデータソースとしてデータ モデルにマッピングする
1. ツリーで、「Invoice\SalesOrder」を選択します。
2. [マッピング] タブをクリックします。
3. ツリーで、[model] を展開します。
4. ツリーで、「model\Sales order number(SalesId)」を選択します。
5. [バインド] をクリックします。
6. ツリーで、「Invoice\InvoiceNumber」を選択します。
7. ツリーで、「model\Base invoice(InvoiceBase)」を展開します。
8. ツリーで、「model\Base invoice(InvoiceBase)\Invoice number(Id)」を選択します。
9. [バインド] をクリックします。
10. ツリーで、「Invoice\InvoiceAmount」を選択します。
11. ツリーで、「model\Base invoice(InvoiceBase)\Invoice amount(Amount)」を選択します。
12. [バインド] をクリックします。
13. ツリーで、「model\Invoice attachments」を展開します。
14. ツリーで、「model\Invoice attachments\File content」を選択します。
15. ツリーで、「Invoice\EnclosedDocs\Document\FileContent\Base64」を選択します。
16. [バインド] をクリックします。
17. ツリーで、「model\Invoice attachments\File name」を選択します。
18. ツリーで、「Invoice\EnclosedDocs\Document\FileName」を選択します。
19. [バインド] をクリックします。
20. ツリーで、「model\Invoice attachments」を選択します。
21. ツリーで、「Invoice\EnclosedDocs\Document」を選択します。
22. [バインド] をクリックします。
23. [保存] をクリックします。
24. ページを閉じます。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]