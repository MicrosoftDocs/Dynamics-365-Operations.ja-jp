---
title: Invoice Capture ソリューションの詳細設定
description: この記事では、Invoice Capture ソリューションの高度な設定について解説します。
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: a1e24b700d0f30fd90f2619dd6e6687736a86774
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691198"
---
# <a name="invoice-capture-solution-advanced-settings"></a>Invoice Capture ソリューションの詳細設定

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

この記事では、Invoice Capture ソリューションの高度な設定について解説します。

## <a name="create-additional-connections-for-channels"></a>チャネルへの追加接続の作成

異なるチャネルからの請求書の受信を監視するには、電子メールやファイルストレージへの接続を作成する必要があります。 ソリューションで使用される自動フローへのアクセスを許可するには、最初に接続を登録する必要があります。

請求書のインポートには、以下の接続タイプを使用します:

- Office 365 Outlook
- Outlook.com
- OneDrive
- SharePoint

請求書インポート用のチャネルは、詳細な構成ステップで接続を使用します。 ユーザーが特定の接続のチャンネルを作成するには、**管理者** のセキュリティ ロールを付与し、接続を作成する必要があります。

Microsoft Dataverse への接続を作成するには、次の手順に従います。

1. **管理システム \> 既定のソリューション** に移動します。
2. **新規** を選択し、**接続参照** を選択します。
3. **表示名** フィールドに名前を入力します。
4. コネクタに **Microsoft Dataverse** を選択します。
5. 初めて接続を設定する場合は、**新しい接続** を選択します。
6. 表示されるダイアログ ボックスで、Dataverse 接続を作成し、**作成** を選択します。
7. Dataverse アカウントとパスワードを入力します。
8. 検証に合格した後は、接続ページに移動し、**更新** を選択して勘定を選択して、**作成** を選択します。

メールやファイル ストレージの接続を作成するには、次の手順に従います。

1. **接続の作成** ページの **接続の種類** フィールドで、**Office 365 Outlook** を選択します。
2. 電子メール接続の場合は、コネクタに **Outlook.com** または **Office 365 Outlook** を選択できます。 ファイル ストレージ接続の場合は、**OneDrive** または **SharePoint** のいずれかを選択できます。

既存の接続を確認するには、**既定のソリューション \> オブジェクト \> 接続参照** に移動します。 チャネルを作成するユーザーは、特定の電子メールやファイルストレージの接続に加えて、少なくとも 1 つの Dataverse 接続を持っている必要があります。 新しいチャンネルの作成者は、接続の所有者である必要があります。
