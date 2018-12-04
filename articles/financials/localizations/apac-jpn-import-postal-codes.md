---
title: "日本の郵便番号のインポート"
description: "このトピックでは、日本の郵便番号をインポートする方法について説明します。"
author: yijialuan
manager: AnnBe
ms.date: 05/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 995a2263683ecd311501a36bb6fd895ed5431b26
ms.contentlocale: ja-jp
ms.lasthandoff: 03/26/2018

---

# <a name="import-postal-codes-for-japan"></a>日本の郵便番号のインポート

[!include [banner](../includes/banner.md)]

日本では、日本郵便局が Microsoft Dynamics 365 for Finance and Operations にインポート可能な郵便番号コード ファイルを提供します。 このトピックでは、郵便番号をインポートするためのプロセスについて説明します。 この例では、デモ データの会社 JPMF を使用します。

## <a name="prepare-the-zip-code-file"></a>郵便番号コード ファイルを準備します。

1. 日本郵便局のホーム ページからコンマ区切り値 (CSV) ファイルをダウンロードします: <http://www.post.japanpost.jp/zipcode/download.html>
2. ファイルを編集するために開き、列見出しのために次の行を追加します。

        LocalAuthCode,OldZipCode,ZipCode,PrefectureName,KanaCity,KanaStreetName,State,City,StreetName,MoreZipCodeFlag,SmallerAreaFlag,StreetChomeFlag,MoreStreetFlag,UpdateFlag,Reason

3. ファイルで、7 桁に満たない郵便番号コードには前にゼロを追加します。 (7 桁に満たない郵便番号コードは認められません。)

## <a name="create-a-data-import-project-and-import-the-data"></a>データのインポート プロジェクトを作成し、データをインポートします。
1. [システム管理] > [ワークスペース] > [データ管理] の順に移動します。
2. [インポート] をクリックしてインポート プロジェクトを作成します。
3. 名前を入力し、[日本の郵便番号] をエンティティの名前として選択します。
4. データ ファイルをアップロードします。
5. [インポート] をクリックします。
6. インポート プロセスの結果を検証します。

