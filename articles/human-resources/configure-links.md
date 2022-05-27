---
title: Human Resources から別の環境へのリンクの作成
description: このトピックでは、Microsoft Dynamics 365 Human Resources から別の Dynamics 365 環境へのリンクを作成する方法について説明します。
author: twheeloc
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d20eef4b4861d85ead1d47ca493c3a5c2d2d85e8
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712628"
---
# <a name="create-links-from-human-resources-to-another-finance-environment"></a>Human Resources から別の Finance 環境へのリンクの作成

顧客は、作業中の 2 つの Dynamics 365 環境を持っている場合があります。 たとえば、顧客は Finance インフラストラクチャに Dynamics 365 Human Resources 環境があり、別の Dynamics 365 Finance 環境に接続する必要がある場合があります。 

この機能により、Human Resources ページから別の Finance 環境の特定のページへのリンクが可能になります。 リンクの構成時に、Human Resources でリンクを使用できる場所と、他の環境で開くターゲット ページを指定できます。

> [!Note] 
> この機能を取得するには、**機能管理** で **人事管理ユーザー エクスペリエンスの向上** を有効にする必要があります。

## <a name="configure-target-systems"></a>ターゲット システムの構成

Human Resources では、システム管理者は **Human Resources** ページに表示されるリンクを定義できます。 構成の一部は、リンクのターゲットとして移動する Finance 環境です。 

ターゲット システムを構成するには:
1. **リンクの構成** ページで **ターゲット システムの構成** を選択します。  
2. ターゲット システム名を入力し、Finance 環境の URL を指定します。 ターゲット システムの構成後、リンクを定義することができます。

## <a name="configure-links"></a>リンクを構成する

作成する各リンクには、次の情報が定義されます:
 - **リンク**: リンクの名前。 識別にのみ使用されます。
 - **このリンクを有効にする**: Human Resources ユーザーにリンクを表示する場合、**はい** に設定します。
 - **表示名**: セカンダリ環境へのリンクとして表示される名前を入力します。 
 - **フォームのサーフェス リンク**: リンクを表示するページを選択します。 リンクは、**従業員セルフ サービス** ワークスペースと **ジョブ**、**ポジション**、**作業者**、および **合理化された作業者** のページでのみ表示できます。
 - **グループ**: グループを使用してリンクを整理できます。 既存のグループを選択するか、**グループ** 列を使用して新しいグループを作成します。
 - **ターゲット システム**: **ターゲット システムの構成** オプションを使用して作成されたターゲット システムを選択します。 これは、リンクを使用して移動する時に使用されるセカンダリ環境になります。
 - **ユーザーの現在の会社を使用する**: Finance へ移動する時にユーザーの現在の会社を使用するには、**はい** を選択します。 使用する会社を選択するには、**いいえ** を選択します。
 - **ターゲット** メニュー項目: 移動時にリンクが使用する Finance 環境からメニュー項目を入力します。 直接移動できるメニュー項目は使用可能です。 

   必要なメニュー項目を検索するには:
   1. Finance 環境に移動し、ナビゲーションのターゲットとなるページを開きます。 
   2. URL からメニュー項目をコピーします。 たとえば、リンクにより Finance and Operations の従業員リストに移動したい場合、URL の「&mi」の後に表示される値を入力します。 
   3. この例の従業員リスト ページに移動するメニュー項目は、HcmWorkerListPage_Employees です。

 - **データ ソースへのリンク**: リンクが参照しているデータのソースを選択します。 **作業者** および **職位** など、最も一般的なソースが利用可能です。

### <a name="access-to-links"></a>リンクへのアクセス

**このリンクを有効にする** オプションが **いいえ** に設定されている場合でも、システム管理者は、定義されたページ上で新しく作成されたリンクを参照することができます。 これは、リンクをテストするために、他の従業員に表示されるより前に使用できます。 他のすべてのロールには、**このリンクを有効にする** オプションを **はい** に設定した後、構成されたリンクのみが表示されます。 リンクが表示されるページにアクセスできる従業員は、このリンクにアクセスできます。

ユーザーは、その環境のページにアクセスするために定義されたセカンダリ環境内のセキュリティ権限も持っている必要があります。 そうでない場合、リンクを使用する時に、セキュリティ ダイアログ ボックスが表示されます。
