---
title: 画像が埋め込まれた Office 形式でレポートを生成するコンフィギュレーションのデザイン
description: この記事では、埋め込み画像を含む Excel と Word 形式で電子ドキュメントを生成する構成をデザインする方法について説明します。
author: kfend
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13cb3cac7369bc68e8b33e4c01f0de0e43689ecb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290337"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>画像が埋め込まれた Office 形式でレポートを生成するコンフィギュレーションのデザイン

[!include [banner](../../includes/banner.md)]

この手順にあるステップを完了するには、まず 「ER 構成プロバイダを作成し、アクティブとしてマークする」 に記載の手順を完了します。 この手順では、電子申告 (ER) コンフィギュレーションを設計して、埋め込み画像を含む Microsoft Excel または Word の電子ドキュメントを生成する方法を説明します。 この手順では、サンプル会社 Litware, Inc. に必要な ER コンフィギュレーションを作成します。USMF データセットを使用してこれらの手順を完了できます。 この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられているユーザー用に作成されています。 開始する前に、次のファイルをダウンロードして保存する必要があります。 

| 説明                                          | ファイル名                   |
|------------------------------------------------------|-----------------------------|
| ER データ モデル構成                          | [cheques.xml 用のモデル](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| ER フォーマット構成                              | [format.xml を印刷する小切手](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| 会社のロゴ画像                                   | [会社の logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| 署名の画像                                      | [Signature image.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| 代替署名画像                          | [Signature image 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| 小切手印刷用の Microsoft Word テンプレート  | [小切手テンプレート Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a>前提条件の確認  
 1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。  
 2. サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。 この構成プロバイダーが表示されない場合は、「構成プロバイダーを作成し、アクティブとしてマークする」 に記載の手順を完了しておく必要があります。   
 3. [コンフィギュレーションをレポートする] をクリックします。  
 
## <a name="add-a-new-er-model-configuration"></a>新しい ER モデル コンフィギュレーションの追加  
 1. 新しいモデルを作成する代わりに、以前に保存した ER モデル コンフィギュレーション ファイル (cheques.xml のモデル) を読み込むことができます。 このファイルには、支払小切手のサンプル データ モデルおよび Dynamics 365 for Operations アプリケーションのデータ コンポーネントへのデータ モデルのマッピングが含まれます。   
 2. [バージョン] クイック タブで、[交換] をクリックします。   
 3. [XML ファイルから読み込む] をクリックします。  
 4. [参照] をクリックし、cheques.xml のモデルを選択します。   
 5. [OK] をクリックします。  
 6. 読み込まれたモデルは、Excel と Word で画像を含むドキュメントを生成するための情報のデータ ソースとして使用されます。  

## <a name="add-a-new-er-format-configuration"></a>新しい ER 形式コンフィギュレーションを追加する  
 1. 新しい形式を作成する代わりに、以前に保存した ER 形式コンフィギュレーション ファイル (format.xml を印刷する小切手) を読み込むことができます。 このファイルには、事前に印刷されたフォームを使用して小切手を印刷する形式のサンプル レイアウトと、データ モデル 「小切手のモデル」 にマッピングしたものが含まれています。   
 2. [交換] をクリックします。  
 3. [XML ファイルから読み込む] をクリックします。  
 4. [参照] をクリックして、format.xml ファイルを印刷する小切手を選択します。   
 5. [OK] をクリックします。  
 6. ツリーで、「小切手のモデル」を展開します。  
 7. ツリーで、「小切手のモデル\小切手の印刷形式」を選択します。  
 8. 読み込まれた形式は、Excel と Word で画像を含むドキュメントを生成するために使用されます。   

## <a name="configure-er-user-parameters"></a>ER ユーザー パラメーターのコンフィギュレーション  
 1. アクション ウィンドウで、[設定] をクリックします。  
 2. [ユーザー パラメーター] をクリックします。  
 3. [設定の実行] フィールドで、[はい] を選択します。  
  「ドラフトを実行する」 フラグをオンにして、選択した形式のドラフト バージョンを開始します。完了したドラフト バージョンではないことに注意してください。  
 4. [OK] をクリックします。  

## <a name="configure-cash--bank-management-parameters"></a>現金 & 銀行管理パラメーターのコンフィギュレーション  
 1. [現金および銀行管理] > [銀行口座] > [銀行口座] の順に移動します。  
 2. クイック フィルターを使用して、値が「USMF OPER」である [銀行口座] フィールドをフィルター処理します。  
 3. アクション ペインで、[設定] をクリックします。  
 4. [小切手] をクリックします。  
 5. [設定] セクションを展開します。  
 6. [編集] をクリックします。  
 7. [会社のロゴ] フィールドで [はい] を選択します。  
 8. [会社のロゴ] をクリックします。  
 9. [変更] をクリックします。  
 10. [参照] をクリックして、以前にダウンロードしたファイル、会社の logo.png を選択します。   
 11. [保存] をクリックします。  
 12. ページを閉じます。  
 13. [署名] セクションを展開します。  
 14. [最初の署名を印刷] フィールドで、[はい] を選択します。  
 15. [変更] をクリックします。  
 16. [参照] をクリックして、以前にダウンロードしたファイル、署名 image.png を選択します。   
 17. [コピー] セクションを展開します。  
 18. [透かし] フィールドで、オプションを選択します。  
 19. [一般的な電子エクスポート形式] フィールドで [はい] を選択します。  
 20. [小切手の印刷フォーム] コンフィギュレーションを選択します。  
 21. これで、小切手を印刷するのに、選択された ER 形式が使用されます。  
 22. [添付] をクリックします。  
 23. [新規] をクリックします。  
 24. [ファイル] をクリックします。  
 25. [参照] をクリックして、以前にダウンロードしたファイル、署名画像 2.png を選択します。   
 26. ページを閉じます。  
 27. ページを閉じます。  
 28. ページを閉じます。  
 29. [現金および銀行管理] > [設定] > [現金および銀行管理パラメーター] の順に移動します。  
 30. [無効な銀行口座での事前通知の作成を許容] フィールドで [はい] を選択します。  
 31. [保存] をクリックします。  
 32. ページを閉じます。  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
