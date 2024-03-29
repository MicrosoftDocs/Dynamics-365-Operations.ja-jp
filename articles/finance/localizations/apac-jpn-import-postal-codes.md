---
title: 日本の郵便番号のインポート
description: この記事では、日本の郵便番号をインポートする方法について説明します。
author: EricWangChen
ms.date: 11/22/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: wangchen
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 723430d38ae1f05ee003985224692704d0dc32c2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898044"
---
# <a name="import-postal-codes-for-japan"></a>日本の郵便番号のインポート

[!include [banner](../includes/banner.md)]

日本では、日本郵便局が Dynamics 365 Finance にインポート可能な郵便番号コード ファイルを提供します。 この記事では、郵便番号をインポートするためのプロセスについて説明します。 この例では、デモ データの会社 JPMF を使用します。

## <a name="prepare-the-zip-code-file"></a>郵便番号コード ファイルを準備します。

1. [日本郵便局のホーム ページ](https://www.post.japanpost.jp/zipcode/download.html) からコンマ区切り値 (CSV) ファイルをダウンロードします

2. ファイルを開いて、ファイル エンコードを「Shift JIS」から「UTF-16 LE」に変換します (メモ帳 ++ などのフリー ソフトウェアを使用してソース ファイルを開き、エンコードを UCS-2 LE BOM に変換することができます)。

3. 編集のためファイルを開き、列見出しのために次の行を追加します。

    ```Text
    LocalAuthCode,OldZipCode,ZipCode,PrefectureName,KanaCity,KanaStreetName,State,City,StreetName,MoreZipCodeFlag,SmallerAreaFlag,StreetChomeFlag,MoreStreetFlag,UpdateFlag,Reason
    ```
    
4. ファイルで、7 桁に満たない郵便番号コードには前にゼロを追加します。 7 桁に満たない郵便番号コードは認められません。

## <a name="create-a-data-import-project-and-import-the-data"></a>データのインポート プロジェクトを作成し、データをインポートします。
1. **システム管理** > **ワークスペース** > **データ管理** の順に移動します。
2. **インポート** をクリックしてインポート プロジェクトを作成します。
3. 名前を入力し、**日本の郵便番号** をエンティティの名前として選択します。
4. データ ファイルをアップロードします。
5. インポート プロジェクトのソース ファイル形式を「CSV (Unicode)」に設定します。
6. **インポート** をクリックします。
7. 結果を検証します。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
