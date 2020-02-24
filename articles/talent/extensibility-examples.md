---
title: Power Apps および Power Automate を使用した Talent の拡張
description: この記事では、Microsoft Power Apps および Microsoft Power Automate を使用する Microsoft Dynamics 365 Talent - Attract の拡張性シナリオのいくつかの例を説明します。
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 1051fa4db16bb94cc9d60a91fc3637d7e5305cc2
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029914"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>Power Apps および Power Automate を使用した Talent の拡張

この記事では、Microsoft Power Apps および Microsoft Power Automate を使用する Microsoft Dynamics 365 Talent: Attract の拡張性シナリオのいくつかの例を説明します。 各例に関連付けられているソリューション パッケージを Power Apps 環境にインポートすることができます。 次に、そのパッケージをガイダンスもしくは組織に適用できるシナリオを実装するための開始点として使用できます。

> [!IMPORTANT]
> この記事で説明されているテンプレートおよびアプリを「そのまま」使用する場合は、それらをテストして、実装に固有のすべてのシナリオをカバーしていることを確認してください。


## <a name="prerequisites"></a>必要条件

- パッケージをインポートするには、ユーザーは**環境メーカー**のアクセス許可が必要です。
- アプリをエクスポートまたはインポートするには、Power Apps プラン 2 ライセンスもしくは Power Apps プラン 2 試用版ライセンスが必要です。

## <a name="power-automate--form-connect"></a>Power Automate – フォーム コネクト

**Power Automate – フォーム コネクト** テンプレートは、Microsoft Forms からデータを読み込み、それを Common Data Service エンティティに格納することができます。

このテンプレートは、他のシナリオに使用できるように拡張することができます。 次にいくつか例を挙げます。

- 候補評価をキャプチャします。
- コースのアンケート結果をキャプチャします。
- 人事管理 (HR) の管理者向けの面接質問のライブラリを作成します。
- 面接プロセスの候補者の評価をキャプチャします

Microsoft Dynamics 365: Attract では、候補者が詳細を入力する候補者ポータルでフォームを使用できます。 フォームを職務テンプレートに活動としても埋め込むことができます。

候補者がフォームを送信すると、Microsoft Power Automate はフォーム送信をキャプチャし、データを読み込み、Common Data Service エンティティに格納します。

**Power Automate – フォーム コネクト** テンプレートおよびカスタム エンティティ構造をダウンロードするには、Microsoft ダウンロード センターの [Power Automate – フォーム コネクト](https://go.microsoft.com/fwlink/?linkid=2081988) に移動します。

## <a name="power-automate--sharepoint-integration"></a>Power Automate – SharePoint 統合

**Power Automate – SharePoint 統合** テンプレートを使用すると、Microsoft SharePoint リストからデータを読み取り、そのリストを Common Data Service エンティティのフィールド値と比較し、その比較結果を通知電子メールとして送信できます。 

組織では、一連のスキルが緊急に必要とされることがあるかもしれません。 これらのスキルは、SharePoint に SharePoint リストとして格納できます。 候補者が一連の必要なスキルがリストされている仕事に応募するときに、候補者のスキルと SharePoint に格納されているスキルに顕著な一致が見られる場合は、通知電子メールが送信されます。 これは、組織全体で採用担当者が候補者を採用するのに役立つため、緊急に必要なポジションをより迅速に埋めるのに役立ちます。

このテンプレートは、SharePoint 統合を含むあらゆるシナリオで使用できるように拡張することができます。

**Power Automate  – SharePoint 統合** テンプレートをダウンロードするには、Microsoft ダウンロード センターの [Power Automate – SharePoint 統合](https://go.microsoft.com/fwlink/?linkid=2082109) に移動します。

## <a name="referral-app"></a>照会アプリ

照会アプリを使用すると、共有された人材プールに候補者を追加することができます。 候補者を送信するときに、参照元に**名**、**姓**、**電子メール**、および **LinkedIn URL** を入力できます。 これにより、候補者のソース メタデータに、参照元の情報が設定されます。

このアプリは、参照を送信するための従業員セルフ サービスに埋め込むことも、社内ポータルでハイパーリンクとして使用してスタンドアロン アプリとして実行することもできます。

**照会アプリ**をダウンロードするには、Microsoft ダウンロード センターの [Dynamics 365 Talent拡張機能ソリューション : 照会アプリ](https://www.microsoft.com/download/details.aspx?id=58497)に移動します。 このアプリをインポートしてカスタマイズし、機能を追加することができます。

## <a name="additional-resources"></a>追加リソース

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[テナントと環境間でのアプリケーションの移行](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
