---
title: ER ドキュメント管理ファイルを形式出力で使用する (第 5 部 - 形式の変更および実行)
description: このトピックでは、ER 出力でドキュメント管理ファイル (添付ファイル) を使用するために電子申告 (ER) 形式を構成する方法について説明します。 (第 5 部)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48175de4e58f9def15bf2bf8b10a1348036c88a1af284eb2a3e5f9fbefd649c1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748403"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a>ER ドキュメント管理ファイルを形式出力で使用する (第 5 部 - 形式の変更および実行)

[!include [banner](../../includes/banner.md)]

次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。 これらのステップは DEMF 会社で実行できます。

これらの手順を完了するには、まず 「ER ドキュメント管理ファイルをフォーマット出力で使用する（パート 4：フォーマットを実行する）」に記載の手順を実行する必要があります。

この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a>バイナリ形式のメッセージの生成に添付ファイルを設定するフォーマットを変更します。
1. [組織管理] > [電子申告] > [コンフィギュレーション] に移動します。
2. ツリーで、「Customer invoice model」を選択します。
3. ツリーで、「Customer invoice model\Customer invoice model (custom)」を展開します。
4. ツリーで、「In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message」を選択します。
5. [デザイナー] をクリックします。
    * UNICODEエンコードを使用し、XMLファイルとして生成される出力の請求書メッセージを設定します。  
6. [ルートの追加] をクリックして、ドロップ ダイアログを開きます。
7. ツリーで、[Common\File] を選択します。
8. [名称] フィールドに、「Xmlメッセージ」と入力します。
    * Xml メッセージ  
9. [エンコード] フィールドに、「UTF-8」と入力します。
    * UTF-8  
10. [OK] をクリックします。
    * ZIPファイルとして生成される出力を設定します。  
11. [ルートの追加] をクリックして、ドロップ ダイアログを開きます。
12. ツリーで、「Common\Folder」を選択します。
13. [名称] フィールドに、「Zip出力」と入力します。
    * Zip 出力  
14. [OK] をクリックします。
15. ツリーで、「Zip output」を選択します。
    * 元名称と拡張子を含むファイルとして生成されるZIPファイルに添付ファイルを追加します。  
16. [追加] をクリックしてドロップ ダイアログを開きます。
17. ツリーで、[Common\File] を選択します。
18. [名称] フィールドで、「添付ファイル」を入力します。
    * 添付ファイル  
19. [OK] をクリックします。
20. ツリーで、「Zip output\Attached file」を選択します。
21. [追加] をクリックしてドロップ ダイアログを開きます。
22. ツリーで、「'Text\Base64」を選択します。
23. [OK] をクリックします。

## <a name="map-new-format-elements-to-data-model"></a>新規フォーマットエレメントをデータ モデルにマッピングする
1. [マッピング] タブをクリックします。
2. ツリーで、「model」を展開します。
3. ツリーで、「model\Invoice attachments」を展開します。
4. ツリーで、「Zip output\Attached file\Base64を選択します。
5. ツリーで、「model\Invoice attachments\File content」を選択します。
6. [バインド] をクリックします。
7. ツリーで、「Zip output\Attached file」を選択します。
8. [ファイル名の編集] をクリックします。
9. ツリーで、[model] を展開します。
10. ツリーで、「model\Invoice attachments」を展開します。
11. ツリーで、「model\Invoice attachments\File name」を選択します。
12. [データ ソースの追加] をクリックします。
13. [保存] をクリックします。
14. ページを閉じます。
15. ツリーで、「model\Invoice attachments」を選択します。
16. [バインド] をクリックします。
17. [保存] をクリックします。
18. ページを閉じます。

## <a name="run-the-designed-report-for-the-selected-invoice"></a>選択した請求書についてデザインされたレポートを実行する
1. [実行] をクリックします。
2. () セクションを含む記録を展開します。
3. [フィルター] をクリックします。
4. 顧客請求書仕訳および販売注文のフィールドの行を選択します。
5. 条件 [販売注文]フィールドでの条件フィールドにて、注文番号 000148 を入力します。
    * 000148  
6. [OK] をクリックします。
7. [OK] をクリックします。
    * 生成された出荷を確認します。 XML形式の請求書メッセージに加えて、各添付ファイルに対して単一ファイルが作成されたことに注意していください。 添付ファイルは、バイナリ形式のZIP出力で設定されます。  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]