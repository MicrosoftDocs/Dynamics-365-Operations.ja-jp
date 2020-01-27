---
title: Power Apps および Power Automate を使用した Talent の拡張
description: このトピックでは、Microsoft Power Apps および Microsoft Power Automate を使用する Microsoft Dynamics 365 Talent の拡張性シナリオのいくつかの例を説明します。
author: negudava
manager: Annbe
ms.date: 05/01/2019
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
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 6c8a583a93c2ceb70d8c3b0e0047e2bf2047b56d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898320"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>Power Apps および Power Automate を使用した Talent の拡張

このトピックでは、Microsoft Power Apps および Microsoft Power Automate を使用する Microsoft Dynamics 365 Talent の拡張性シナリオのいくつかの例を説明します。 各例に関連付けられているソリューション パッケージを Power Apps 環境にインポートすることができます。 次に、そのパッケージをガイダンスもしくは組織に適用できるシナリオを実装するための開始点として使用できます。

> [!IMPORTANT]
> このトピックで説明されているテンプレートおよびアプリを「そのまま」使用する場合は、それらをテストして、実装に固有のすべてのシナリオをカバーしていることを確認してください。


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

Microsoft Dynamics 365: Attract では、フォームが候補者のポータルに表示され、候補者は詳細を記入することができます。 フォームは、職務テンプレートに活動としても埋め込むことができます。

候補者がフォームを送信すると、Microsoft Power Automate はフォーム送信をキャプチャし、データを読み込み、Common Data Service エンティティに格納します。

**Power Automate – フォーム コネクト** テンプレートおよびカスタム エンティティ構造をダウンロードするには、Microsoft ダウンロード センターの [Power Automate – フォーム コネクト](https://go.microsoft.com/fwlink/?linkid=2081988) に移動します。

## <a name="initiate-and-extract-parameters-passed-to-power-apps"></a>Power Apps に渡されたパラメーターの開始と抽出

**Power Apps に渡されたパラメーターの開始と抽出** テンプレートは、Attract に固有のあらゆる Power Apps シナリオの開始点として使用できます。 **求人応募**、**候補者 ID**、および**JobID** など、Attract によって渡されたすべての既定のパラメーターが含まれます。

このテンプレートを使用して候補者評価フォームを取得し、候補者が記入した評価を採用マネージャーが表示できるようにします。

Power Apps を使用して作成されたアプリケーションは、Attract の職務テンプレートに埋め込むことができます。

**Power Apps に渡されるパラメーターの開始および抽出** テンプレートおよびカスタム エンティティの構造をダウンロードするには、Microsoft ダウンロード センターの [Power Apps に渡されるパラメーターの開始および抽出](https://go.microsoft.com/fwlink/?linkid=2081991) に移動します。

## <a name="integration-with-office-365"></a>Office 365 との統合

**Office 365 との統合**アプリケーションを使用して、Microsoft Office 365 からサインイン ユーザーのチーム情報を抽出することができます。 出勤、退勤の詳細および例外の記録を抽出するために、Talent の従業員を参照します。 出勤および退勤の詳細は、カスタム Common Data Service エンティティに格納されます。 これらの詳細は、統合によってサードパーティ製システムから入力されることを前提とします。

このアプリケーションは、他のシナリオに使用できるように拡張することができます。 たとえば、チームの休暇情報、カレンダーのイベント、およびそのチーム固有のイベントを表示するために使用できます。

**Office 365 との統合**アプリケーションおよびカスタム エンティティ構造をダウンロードするには、Microsoft ダウンロード センターの [Office 365 との統合](https://go.microsoft.com/fwlink/?linkid=2081787)に移動します。

## <a name="power-automate--email-notification"></a>Power Automate – 電子メール通知

**Power Automate – 電子メール通知** テンプレートは電子メール通知のシナリオに使用することができます。 採用プロセスのどの段階でも、採用チームが拒否した候補者への通知電子メールをトリガーするために使用できます。

このテンプレートを拡張して、採用プロセス全体を通して候補者ステージの変更を追跡し、採用チームと候補者に通知を送信することができます。

一般に、Common Data Service に格納されているエンティティの場合、Core HR、Attract、または Onboard で発生したイベントに関する通知を送信するようにフローを設定できます。

**Power Automate – 電子メール通知** テンプレートをダウンロードするには、Microsoft ダウンロード センターの [Power Automate – 電子メール通知](https://go.microsoft.com/fwlink/?linkid=2082103) に移動します。

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – SQL 接続と実行

**Power Automate – SQL 接続と実行** テンプレートを Microsoft SQL Server に接続し、SQL クエリを実行できるようにします。

このテンプレートは SQL テーブルの読み取りと更新のために設計されていますが、他のシナリオでも使用できるように拡張することができます。 たとえば、Common Data Service のステージング テーブルに SQL Server のレコードを入力したり、SQL Server からの増分プッシュを使用してステージング テーブルを定期的に同期するために使用できます。

**Power Automate – SQL 接続と実行** テンプレートをダウンロードするには、Microsoft ダウンロード センターの [Power Automate – SQL 接続と実行](https://go.microsoft.com/fwlink/?linkid=2081789) に移動します。

## <a name="power-automate--sharepoint-integration"></a>Power Automate – SharePoint 統合

**Power Automate – SharePoint 統合** テンプレートを使用すると、Microsoft SharePoint リストからデータを読み取り、そのリストを Common Data Service エンティティのフィールド値と比較し、その比較結果を通知電子メールとして送信できます。 

組織では、一連のスキルが緊急に必要とされることがあるかもしれません。 これらのスキルは、SharePoint に SharePoint リストとして格納できます。 候補者が一連の必要なスキルがリストされている仕事に応募するときに、候補者のスキルと SharePoint に格納されているスキルに顕著な一致が見られる場合は、通知電子メールが送信されます。 このように通知があることで、採用担当者は候補者と連絡を取ったり組織全体を通して採用することができるので、緊急に必要とされるポジションはより迅速に埋められます。

このテンプレートは、SharePoint 統合を含むあらゆるシナリオで使用できるように拡張することができます。

**Power Automate  – SharePoint 統合** テンプレートをダウンロードするには、Microsoft ダウンロード センターの [Power Automate – SharePoint 統合](https://go.microsoft.com/fwlink/?linkid=2082109) に移動します。

## <a name="referral-app"></a>照会アプリ
照会アプリを使用すると、共有された人材プールに候補者を追加することができます。 候補者を送信するときに、参照元に**名**、**姓**、**電子メール**、および**リンクトイン URL** を入力できます。 これにより、候補者のソース メタデータに、参照元の情報が設定されます。

このアプリは、参照を送信するための従業員セルフサービス (ESS) に埋め込むことも、社内ポータルでハイパーリンクとして使用してスタンドアロン アプリとして実行することもできます。

**照会アプリ**をダウンロードするには、Microsoft ダウンロード センターの [Dynamics 365 Talent拡張機能ソリューション : 照会アプリ](https://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d)に移動します。 このアプリをインポートしてカスタマイズし、機能を追加することができます。

## <a name="additional-resources"></a>追加リソース

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[テナントと環境間でのアプリケーションの移行](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
