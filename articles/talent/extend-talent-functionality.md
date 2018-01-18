---
title: "Microsoft Dynamics 365 for Talent の機能を拡張します。"
description: "任意の Microsoft PowerApps を作成した場合は、Microsoft Dynamics 365 for Talent 内のリンクからそれらのアプリケーションを開始できます。"
author: rschloma
manager: AnnBe
ms.date: 11/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Talent
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: cfd3b475b113fdab4ceeb3e636fea6c9134ab982
ms.openlocfilehash: 0ab829803634871c9060daa381bd02d7d2bbdf42
ms.contentlocale: ja-jp
ms.lasthandoff: 12/01/2017

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a>Microsoft Dynamics 365 for Talent の機能を拡張します。
任意の Microsoft PowerApps を作成した場合は、Microsoft Dynamics 365 for Talent 内のリンクからそれらのアプリケーションを開始できます。 アプリケーションへのアクセスを設定するには、**システム管理** ワークスペースから開けるコンフィギュレーション ページの Talent で、一部の情報を設定する必要があります。

## <a name="configuring-embedded-powerapps-within-talent"></a>Talent 内の埋め込み型 PowerApps のコンフィギュレーション
**埋め込み型 Microsoft PowerApps の設定** ページを使用して PowerApps アプリケーションを起動する Talent ページを構成します。 **埋め込み型 Microsoft PowerApps の設定** ページを開くには、**システム管理** ワークスペースを開き、**リンク** タブを開きます。**設定** グループから **Microsoft PowerApps** を選択します。 

以下の情報を入力するか、またはこのページで設定します。 

> - 各 PowerApps アプリケーションの内容を説明する名前または識別子。
> - Talent ページに追加する各アプリケーションの固有識別子 (GUID)。 アプリ IDは、PowerApps サイト [powerapps.com](http://powerapps.com/)で使用できます。 
> - ユーザーがアプリケーションまたはレポートを開くことができるページ。 すべての Talent ページが、埋め込み型 PowerApps および Power BI レポートをサポートするわけではありません。 

 > [!NOTE]
 >  ページの上部に表示される表示名ではなく、ページの内部名称を入力します。 内部名称を検索するには、内部名称が必要なページを開き、ページ上の任意の場所で右クリックします。 メニューを開いたら、**フォーム情報** 項目をポイントします。 内部フォーム名が、メニューの **フォーム情報** 項目の横に表示されます。
 
> - アプリケーションがコンテキスト データを取得するフォーム コントロールを指定します。 たとえば、アプリケーションは、作業者に関するデータを使用する場合があります。 **コンテキスト** フィールドで **作業者** ページを入力する場合、アプリケーションを起動すると **作業者** ページが開きます。 **コンテキスト フィールド** の入力はオプションです。 
> - PowerApps アプリケーションを実行するダイアログ ボックスのサイズを設定します。 アプリケーションが電話や大きなデバイスで実行している場合、ユーザー インターフェイスを最適化するため、ダイアログ ボックスがそれぞれ “小“ または “大“ に指定されます。 

どの法人に対してアプリケーションが利用できるか、またはすべての法人に対してアプリケーションを利用できるように指定することもできます。 既定では、PowerApps アプリケーションはすべての法人に対して利用できます。

## <a name="opening-an-application"></a>申請の開始
埋め込み型 PowerApps アプリケーションを構成した場合、指定したアプリケーションへのリンクが Talent 内のページに追加されます。 申請書を開くためのリンクをクリックします。 



