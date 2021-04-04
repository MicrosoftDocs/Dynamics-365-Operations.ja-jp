---
title: アプリケーション データを含むドキュメントを生成するためのコンフィギュレーションのデザイン
description: このトピックでは、電子ドキュメントを生成するために電子申告 (ER) コンフィギュレーションをデザインする方法について説明します。 (パート 1 - コンフィギュレーションのインポート)。
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 217eca9bd1502d4327857720fb2d32a3ec3508ef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563177"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a>アプリケーション データを含むドキュメントを生成するためのコンフィギュレーションのデザイン

[!include [banner](../../includes/banner.md)]

この手順のステップを完了するには、まず「ER アプリケーション データ更新と共にドキュメントを生成する (パート 1: コンフィギュレーションのインポート)」の手順を完了する必要があります。



この手順のステップでは、電子ドキュメントを生成するために電子申告 (ER) コンフィギュレーションを設計する方法について説明します。 この手順では、サンプル会社 Litware, Inc. 用に作成された ER インポート済形式コンフィギュレーションを実行して、電子ドキュメントを生成します。



この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられているユーザー用に作成されています。 これらのステップは、DEMF データ セットを使用して完了することができます。 



開始する前に、DEMF 会社の国コンテキストを DEU (ドイツ) から BEL (ベルギー) に変更します。 [組織管理] > [組織] > [法人] をクリックして、法人 DEMF の基本住所にある国コードを更新します。 アプリケーションを再起動します。


## <a name="run-imported-er-format"></a>インポートされた ER 形式を実行する
1. [組織管理] > [電子申告] > [コンフィギュレーション] に移動します。
2. ツリーで、「イントラスタット (モデル)」を展開します。
3. ツリーで、「イントラスタット (モデル)\イントラスタット (形式)」を選択します。
4. [実行] をクリックします。
    * イントラスタット レポートを生成するために、ER 形式コンフィギュレーションのドラフト バージョンを実行します。  
5. [ファイル名を入力] フィールドに、「intrastat.xml」と入力します。
    * ファイルの名前を指定します。  
6. [OK] をクリックします。
    * 生成した XML ファイルを確認します。  
7. ページを閉じます。
8. [税] > [申告] > [対外貿易] > [イントラスタット] の順に移動します。
    * このフォームを開いて、生成した電子ドキュメントに含まれるイントラスタット トランザクションを表示します。  
9. [イントラスタット アーカイブ] をクリックします。
    * 実行した ER 形式にアプリケーション データ更新の設定が含まれていないため、完了したイントラスタット レポートの詳細はアーカイブされていません。  
10. ページを閉じます。
11. ページを閉じます。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]