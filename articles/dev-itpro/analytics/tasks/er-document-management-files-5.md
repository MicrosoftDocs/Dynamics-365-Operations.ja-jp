--- 
title: "ER 出力でドキュメント管理ファイルを使用するための形式の変更および実行"
description: "次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。"
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 5effbecf98e633d07f9e5eb22d3df1a12967c1e4
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="modify-and-run-formats-to-use-document-management-files-in-er-output"></a>ER 出力でドキュメント管理ファイルを使用するための形式の変更および実行

[!include [task guide banner](../../includes/task-guide-banner.md)]

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
    * 生成された出荷を確認します。 XML 形式の請求書メッセージに加えて、各添付ファイルに対して単一ファイルが作成されたことに注意してください。 添付ファイルは、バイナリ形式のZIP出力で設定されます。  


