---
title: 販売時点管理 (POS) での顧客チェックイン通知を有効にする
description: このトピックでは、Microsoft Dynamics 365 Commerce 販売時点管理 (POS) で顧客チェックイン通知を有効にする方法について説明します。
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b42dc7766f8a69a7409c28d21b49cc96eca18dd4
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271428"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>販売時点管理 (POS) での顧客チェックイン通知を有効にする

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce 販売時点管理 (POS) で顧客チェックイン通知を有効にする方法について説明します。

"ピックアップ可能な注文" のメールには、顧客が店内にいて荷物が運ばれてくるのを待っていることを店舗に通知するリンクやボタンを設けることができます。 顧客はチェックイン確認を受け取り、店舗は POS アプリケーションでタスクとして通知を受け取ります。 このタスクは、販売担当者が顧客の車両に注文を届けるためのプロンプトとして機能します。 したがって、顧客は店舗に入る必要はありません。

顧客のチェックイン ワークフローは、駐車場の番号、車両のメーカー、モデル、色、配送手順など、顧客から追加情報を収集するように構成することもできます。 小売用店舗のスタッフは、この情報を利用して注文のフルフィルメントを円滑化することができます。

## <a name="enable-customer-check-in"></a>顧客チェックインを有効にする

顧客チェックイン機能を有効にすると、Commerce によって注文確認 ID (チャネル参照 ID とも呼ばれます) が生成されます。 また、販売時点管理 (POS) またはコール センター チャネルを通じて作成された注文の注文確認 ID も生成されます。 

Commerce 本部の顧客チェックイン機能をオンにするには、次の手順に従います。

1. **ワークスペース \> 機能管理** に移動します。
2. **チャネル全体で一貫したチャネル参照 ID フォーマットを生成する** 機能を検索します。 
3. 機能を選択し、プロパティ ウィンドウで **今すぐ有効にする** を選択します。 

## <a name="create-a-check-in-confirmation-page"></a>チェックイン確認ページの作成

eコマース サイトで、チェックイン確認エクスペリエンスとして機能する新しいページを作成する必要があります。 このページには、追加の構成を使用して、顧客からの追加情報を収集して注文のフルフィルメントを容易にするフォームを含めることもできます。 ページおよびモジュールの設定方法については、[顧客チェックイン モジュール](check-in-pickup-module.md) を参照してください。

## <a name="configure-the-transactional-email-template"></a>トランザクション メール テンプレートの構成

注文した商品がピックアップ可能になったときに顧客が受け取るトランザクション メールのテンプレートに、**I am here** のリンクまたはボタンを追加する必要があります。 顧客はこのリンクまたはボタンを使用して、注文をピックアップするために到着したことを店舗に通知します。 

通知タイプの **梱包完了済** と、カーブサイド注文のフルフィルメントに使用している配送モードにマッピングされたテンプレートに、リンクまたはボタンを追加します。 テンプレートで、作成したチェックイン確認ページの URL を指す HTML リンクまたはボタンを作成します。 次に例を示します。

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
メール テンプレートの構成方法の詳細については、「[配送モードによるトランザクション メールのカスタマイズ](customize-email-delivery-mode.md)」を参照してください 。 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>POS でチェックイン確認タスクが作成される

顧客が店舗にピックアップのために到着したことを通知すると、チェックイン確認通知が表示され、顧客が注文をピックアップする店舗の POS のタスク リストにタスクが作成されます。 このタスクには、注文のフルフィルメントを行うために必要なすべての顧客および注文情報が含まれています。 このタスクでは、指示フィールドには、追加の情報フォームを使用して顧客から収集された情報が表示されます。 

## <a name="additional-resources"></a>追加リソース

[ピックアップのチェックイン モジュール](check-in-pickup-module.md)
