---
title: モバイル ワークスペースの請求書承認
description: このトピックでは、請求書承認モバイル ワークスペースに関する情報を提供します。
author: abruer
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 0d19e99776f04eab28eb7371bc0ac90ac046b62af0ad785fd3ab28309cae43ab
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759983"
---
# <a name="invoice-approvals-mobile-workspace"></a>モバイル ワークスペースの請求書承認

[!include [banner](../includes/banner.md)]

このトピックでは、**請求書承認** モバイル ワークスペースに関する情報を提供します。 このワークスペースは、仕入先請求書ヘッダーのワークフロー プロセスを通して割り当てられている請求書の一覧を提供します。 

このモバイル ワークスペースは、Finance and Operations モバイル アプリで使用するためのものです。

## <a name="overview"></a>概要

**請求書承認** モバイル ワークスペースは、買掛金勘定の担当者およびマネージャーが、仕入先請求書ヘッダーのワークフロー プロセスの一部として割り当てられている請求書を表示できるようにします。 請求書情報 (明細行と配送の詳細も含む) を表示して、通知された承認決定を行うことができます。 ワークスペースから、ワークフロー プロセスを通して請求書を移動するアクションを実行できます。 

## <a name="prerequisites"></a>前提条件

このモバイル ワークスペースを使用するには、次の前提条件を満たす必要があります。

<table>
<thead>
<tr class="header">
<th>前提条件</th>
<th>役割</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Microsoft Dynamics 365 Finance は組織内に配置する必要があります。</td>
<td>システム管理者</td>
<td><a href="../deployment/deploy-demo-environment.md">デモ環境の配置</a>を参照してください。
</td>
</tr>
<tr class="even">
<td><strong>請求書承認</strong> モバイル ワークスペースを公開する必要があります。</td>
<td>システム管理者</td>
<td>「<a href="publish-mobile-workspace.md">モバイル ワークスペースの公開</a>」を参照してください。</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>モバイル アプリのダウンロードとインストール

Finance and Operations モバイル アプリのダウンロードとインストール。

-   [Android フォン用](https://go.microsoft.com/fwlink/?linkid=850662)
-   [iPhone 用](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>モバイル アプリにログインします。

1.  モバイル デバイスでアプリを起動します。
2.  Microsoft Dynamics 365 URL を入力します。
3.  初めてサインインすると、ユーザー名とパスワードを要求されます。 資格情報を入力します。
4.  サインインすると、使用可能な会社のワークスペースが表示されます。 なお、システム管理者が後で新しいワークスペースを公開すると、モバイル ワークスペースのリストを更新する必要があります。

    [![プルして更新。](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a>請求書承認モバイル ワークスペースを使用して請求書を承認します。
1.  モバイル デバイスで、**請求書承認** ワークスペースを選択します。
2.  仕入先請求書ヘッダーのワークフロー プロセスによって割り当てられた請求書を選択します。
3.  **請求書の詳細** ページで、仕入先や日付情報などの請求書ヘッダー情報を確認します。
4.  **請求明細行の詳細** ビューで、関係する詳細な情報を表示する請求書の明細行を選択します。
5.  **請求明細行の詳細** ビューで、**配分** を選択して明細行の配分を表示します。 ここで、請求明細行の勘定を表示できます。 表示される情報には、財務分析コードおよび主勘定が含まれます。
6.  **請求明細行の詳細** ページで、**配分** を選択してすべての配分を表示します。 ここで、請求書全体の勘定を表示できます。 表示される情報には、財務分析コードおよび主勘定が含まれます。 
7.  **添付ファイル** を選択して、請求書に添付されているメモまたはファイルを表示します。
8.  **請求書の詳細** ページで、確認プロセスを完了する適切なワークフロー アクションを選択します。
9.  **完了** を選択します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]