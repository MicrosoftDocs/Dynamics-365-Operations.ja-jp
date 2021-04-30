---
title: Power Apps および Power Automate を使用した Talent の拡張
description: この記事では、Microsoft Power Apps および Microsoft Power Automate を使用する Microsoft Dynamics 365 Human Resources の拡張性シナリオのいくつかの例を説明します。
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b5032c0996ef0dfb80a129deb32b4526794ca228
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892156"
---
# <a name="extend-with-power-apps-and-power-automate"></a>Power Apps および Power Automate を使用した拡張

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

この記事では、Microsoft Power Apps および Microsoft Power Automate を使用する Microsoft Dynamics 365 Human Resources の拡張性シナリオのいくつかの例を説明します。 各例に関連付けられているソリューション パッケージを Power Apps 環境にインポートすることができます。 次に、そのパッケージをガイダンスもしくは組織に適用できるシナリオを実装するための開始点として使用できます。

> [!IMPORTANT]
> このトピックで説明されているテンプレートおよびアプリを「そのまま」使用する場合は、それらをテストして、実装に固有のすべてのシナリオをカバーしていることを確認してください。

## <a name="prerequisites"></a>必要条件

- パッケージをインポートするには、ユーザーは **環境メーカー** のアクセス許可が必要です。
- アプリをエクスポートまたはインポートするには、Power Apps プラン 2 ライセンスもしくは Power Apps プラン 2 試用版ライセンスが必要です。

## <a name="integration-with-microsoft-365-power-automate"></a>Microsoft 365, Power Automate との統合

**Microsoft 365 との統合** アプリを使用すると、Microsoft 365 からサインイン ユーザーのチーム情報を抽出できます。 従業員 ID タイプを抽出するために、人事管理の従業員が照会されます。 マネージャーは従業員 ID タイプの有効期限を確認することができます。 またマネージャーは、従業員 ID タイプが期限切れになる場合に電子メールの通知を送信することもできます。 Power Automate と Power Apps 統合し、このアラームを送信します。 アラームが送信されると、Power Automate から Power Apps に確認が送り返されます。 ID タイプには、運転免許証、パスポート、およびその他受け入れ可能な ID の形式が含まれます。

このアプリは他のシナリオのために拡張することができます。 たとえば、チームの休暇情報、カレンダーのイベント、およびそのチーム固有のイベントを表示するために使用することができます。

**Microsoft 365, Power Automate との統合** アプリをダウンロードするには、Microsoft ダウンロード センターの [Microsoft 365 との統合](https://go.microsoft.com/fwlink/?linkid=2081787) に移動します。

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – SQL 接続と実行

**Power Automate – SQL 接続と実行** テンプレートを Microsoft SQL Server に接続し、SQL クエリを実行できるようにします。

このテンプレートは SQL テーブルを読み取り更新しますが、それを拡張して他のシナリオに使用することができます。 たとえば、Dataverse のステージング テーブルに SQL Server のレコードを入力したり、SQL Server からの増分プッシュを使用してステージング テーブルを定期的に同期するために使用することができます。

データ変換と増分プッシュを有効化するために、高度なクエリがフローに統合されています。

**Power Automate – SQL 接続と実行** テンプレートをダウンロードするには、Microsoft ダウンロード センターの [Power Automate – SQL 接続と実行](https://go.microsoft.com/fwlink/?linkid=2081789) に移動します。

## <a name="additional-resources"></a>追加リソース

[Microsoft Power Platform](/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]