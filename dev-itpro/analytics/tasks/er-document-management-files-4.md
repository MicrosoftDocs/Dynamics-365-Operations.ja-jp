--- 
title: "電子申告 (ER) 用の形式出力でドキュメント管理ファイルを使用するための形式を実行する"
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 6e1d7a54055829a1e9215a44f8eba346291f6717
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="run-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>電子申告 (ER) 用の形式出力でドキュメント管理ファイルを使用するための形式を実行する

[!include[task guide banner](../../includes/task-guide-banner.md)]

次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。 これらのステップは DEMF 会社で実行できます。

これらの手順を完了するには、まず「フォーマット出力でのドキュメント管理ファイルをER使用（パート3：フォーマットの作成）」の手順を実行する必要があります。

この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a>単一請求書の販売注文に必要な添付ファイルを追加する
1. [売掛金勘定] > [請求書] > [未処理の顧客請求書] の順に移動します。
2. クイック フィルターを使用して、レコードを見つけます。 たとえば、「CIV-000148」の値を含む請求書フィールドでフィルターを実行します。
    * CIV-000148  
3. クリックして選択した請求書のリンク先に移動します。
    * CIV-000148  
4. クリックして、[販売注文] フィールドのリンク先に移動します。
    * 000148  
5. 明細行またはヘッダーのフィールドで、ヘッダーのオプションを選択します。
    * ヘッダーを選択して、これが添付の追加先であることを示します。  
6. [添付] をクリックします。
    * この販売注文の添付ファイルとしていくつかのファイルを追加します。 ドキュメント管理がサポートするドキュメント タイプのファイルを使用します (ファイル拡張子DOCX、DPF、XML、JPGなど)。 ER電子メッセージに関連する請求書に添付され、さらに処理されるファイルを閲覧、選択します。  
7. [新規] をクリックします。
8. [ファイル] をクリックします。
9. [新規] をクリックします。
10. [ファイル] をクリックします。
11. ページを閉じます。
12. ページを閉じます。
13. ページを閉じます。
14. ページを閉じます。

## <a name="run-the-designed-report-for-the-selected-invoice"></a>選択した請求書についてデザインされたレポートを実行する
1. [組織管理] > [電子申告] > [コンフィギュレーション] に移動します。
2. ツリーで、「Customer invoice model」を選択します。
3. ツリーで、「Customer invoice model\Customer invoice model (custom)」を展開します。
4. ツリーで、「In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message」を選択します。
5. [実行] をクリックします。
6. () セクションを含む記録を展開します。
7. [フィルター] をクリックします。
8. 顧客請求書仕訳および販売注文のフィールドの行を選択します。
9. [基準] フィールドで、「000148」と入力します。
    * 基準「販売注文」フィールドで、「注文番号000148」を入力します。  
10. [OK] をクリックします。
11. [OK] をクリックします。
    * 生成された出荷を確認します。 各添付ファイルに対して単一のXMLノードが作成されたことに注意してください。 添付ファイルのコンテンツは、MIME (base64) のテキスト形式のXML出力に設定されます。  


