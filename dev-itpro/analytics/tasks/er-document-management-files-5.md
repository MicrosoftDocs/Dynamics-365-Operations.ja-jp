--- 
title: "電子申告 (ER) 用の形式出力でドキュメント管理ファイルを使用するための形式を変更して実行する"
description: "次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。"
author: NickSelin
manager: AnnBe
ms.date: 10/31/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: b6e98c6b5bdbc637045676e7bfa2dcbf7383fe66
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="modify-and-run-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>電子申告 (ER) 用の形式出力でドキュメント管理ファイルを使用するための形式を変更して実行する

[!include[task guide banner](../../includes/task-guide-banner.md)]

次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。 これらのステップは DEMF 会社で実行できます。

これらの手順を完了するには、まず「フォーマット出力でのドキュメント管理ファイルをER使用（パート4：フォーマットの実行）」の手順を実行する必要があります。

この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。


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
5. [基準] フィールドの基準[販売注文」フィールドで、注文番号 000148 を入力します。
    * 000148  
6. [OK] をクリックします。
7. [OK] をクリックします。
    * 生成された出荷を確認します。 XML形式の請求書メッセージに加えて、各添付ファイルに対して単一ファイルが作成されたことに注意していください。 添付ファイルは、バイナリ形式のZIP出力で設定されます。  


