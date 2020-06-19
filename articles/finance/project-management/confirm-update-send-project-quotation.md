---
title: プロジェクト見積の確認、更新、送信
description: このトピックでは、顧客に見積書を送信して確認し、フィードバックに基づいて修正し、見積書を再送信する流れについて説明します。
author: kfend
manager: AnnBe
ms.date: 05/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 7c2f7435ed63702dafb52b0eff57c0f174ff829e
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410240"
---
# <a name="confirm-update-and-send-a-project-quotation"></a>プロジェクト見積の確認、更新、送信

[!include [banner](../includes/banner.md)]

プロジェクトの見積を作成して顧客に送信した後は、見積のステータスを **送信済** に更新する前に顧客から確認を受け取る必要があります。 顧客から要望のあった修正は、見積書の中で更新することができます。 見積のステータスを **送信済** に更新した後は、変更することはできません。 以下の手順では、見積書を送信して確認し、フィードバックに基づいた更新を行い、見積書を再送信する流れで使用するオプションについて説明します。

## <a name="send-a-project-quotation-confirmation"></a>プロジェクト見積の確認を送信する  

確認をする目的で、既存のプロジェクトの見積書を電子メールで送信するか、印刷したコピーとして送信することができます。 

1. **プロジェクト管理と会計** > **見積書** > **プロジェクト見積** に移動します。 
2. **プロジェクト見積** ページで、確認をする目的で送信する見積を選択します。 
3. **生成**グループの、**フォローアップ**タブで、 **確認**を選択します。 
4. **見積の確認** ページで、必要なパラメータを設定します。 たとえば、確認を印刷するには、**印刷**オプションで**印刷の確認**をオンにして、**OK** を選択します。
5. **見積書の送信**ページで、**オプション**を選択し、**印刷先の設定**ページで、見積もりの送信先として**画面**、**電子メール**、**ファイル**、**印刷アーカイブ**、**印刷**を選択し、続いて**設計**エリアで見積書のルーティングの調整を行います。
6. **印刷先の設定** ページで、**OK**を選択します。  

## <a name="update-a-project-quotation"></a>プロジェクトの見積を更新する

既存のプロジェクトの見積を変更するには、見積のステータスを**作成する**必要があります。 既存の見積を更新するには、次の手順を実行します。 

1. **プロジェクト管理と会計** > **見積書** > **プロジェクト見積** に移動します。
2. **プロジェクトの見積** ページで、更新する見積を選択し、アクションウィンドウで **編集** を選択します。
3. 必要なフィールドの情報を更新し、アクション ウィンドウで **保存** を選択します。  

## <a name="send-a-project-quotation-to-a-customer"></a>プロジェクトの見積を顧客に送信する 

1. **プロジェクト管理と会計** > **見積書** > **プロジェクト見積**に移動し、送信するプロジェクトの見積を選択します。
2. **見積**タブの **プロジェクト見積** ページで、**プロセス**グループにて、**見積書の送付**を選択します。 見積のステータスが**送信済**に更新されます。

> [!NOTE]
> ステータスを **送信済** に変更した後は、プロジェクトの見積を変更できません 。
