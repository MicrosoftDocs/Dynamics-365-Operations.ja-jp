---
title: ER ドキュメント管理ファイルを形式出力で使用する (第 1 部 - データ モデルの準備)
description: このトピックでは、ER 出力でドキュメント管理ファイル (添付ファイル) を使用するために電子申告 (ER) 形式を構成する方法について説明します。 (第 1 部)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa4996100a839a8440bad8724680c5799e032064d4a5ec0fbbc0f2af2641b8fb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768418"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a>ER ドキュメント管理ファイルを形式出力で使用する (第 1 部 - データ モデルの準備)

[!include [banner](../../includes/banner.md)]

次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。 これらの手順はどのタイプの企業でも実施できます。

この手順を完了するには、まず 「構成プロバイダーを作成し、有効としてマークする」 に記載の手順を完了する必要があります。

この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Microsoft 提供の設定リストにアクセスする
1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。

    「Litware, Inc.」を確認します プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。  

2. 「Litware, Inc.」を選択します プロバイダー
3. [リポジトリ] をクリックします。

    「運営リソース」のストックがすでにある場合、現在のサブタスクの残りの手順を省略します。  

4. [追加] をクリックしてドロップ ダイアログを開きます。
5. [設定リポジトリ タイプ] フィールドで、「運営 リソース」と入力します。
6. [リポジトリの作成] をクリックします。
7. [OK] をクリックします。

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a>Microsoftが提供する顧客請求書モデル設定を取得する
1. [フィルターの表示] をクリックします。
2. 次のフィルターを適用します: 「フィルターオペレーターから始める」を使用して、「名称」フィールドに「運営リソース」のフィルター値を入力します。「フィルターオペレーターから始める」を使用して、「説明」フィールドにフィルター値を入力します。
3. [フィルターの表示] をクリックします。
4. [開く] をクリックします。
5. ツリーで、「Customer invoice model」を選択します。

    モデル設定「顧客請求書モデル」を選択し、インポートします。  

6. [インポート] をクリックします。

    [選択した設定のバージョン 1 のインポート] をクリックします。  

7. [はい] をクリックします。
8. ページを閉じます。
9. ページを閉じます。
10. [コンフィギュレーションをレポートする] をクリックします。
11. ツリーで、「Customer invoice model」を選択します。

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>ドキュメント管理のファイルへのアクセスをサポートするために取得したモデルを作成します。
Microsoft 提供の設定から取得した顧客請求書モデルの設定を作成します。 この設定を使用してドキュメント管理のファイルにアクセスし、このモデルに基づいて作成する電子ドキュメント用にそれらのファイルを使用します。  
1. [コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。
2. [新規] フィールドで、「名称から取得: 顧客請求書モデル、Microsoft」を入力します。
3. [名称] フィールドに、「顧客請求書モデル（カスタム）」を入力します。
4. [コンフィギュレーションの作成] をクリックします。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]