---
title: 4xx/5xx ステータス コード エラーに対するカスタム応答ページの作成
description: このトピックでは、Microsoft Dynamics 365 Commerce の作成ツールを使用して、4xx と 5xx のステータス コード エラーに対するカスタム応答ページを作成する方法について説明します。
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 060f5e5616624279711f61f582e6a898c7eb7785
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413722"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>4xx/5xx ステータス コード エラーに対するカスタム応答ページの作成


[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce の作成ツールを使用して、4xx と 5xx のステータス コード エラーに対するカスタム応答ページを作成する方法について説明します。

## <a name="overview"></a>概要

要求が成功しなかった場合、サーバーは HTTP ステータス コード エラーの応答を発行します。 ページが見つからない場合は、404 ステータス コードがキャプチャされて返され、サーバー エラーが発生した場合は 500 ステータス コードがキャプチャされて返されます。 Dynamics 365 Commerce では、アプリケーション ユーザーは、これらのステータス コード エラーの応答について、ユーザーに対して表示されるカスタム ステータス コード エラーの応答ページを作成できます。

## <a name="build-a-status-code-error-response-page"></a>ステータス コード エラーの応答ページの構築

ステータス コード エラーの応答ページの構築を開始するには、次の手順を実行します。

1. 優先的に使用する Web ブラウザーで、Dynamics 365 Commerce にサインインします。 
1. 4xx/5xx ステータス コード エラーの応答ページを構築するサイトを選択します。

### <a name="build-the-template"></a>テンプレートの構築

ステータス コード エラーの応答ページのテンプレートの構築を開始するには、次の手順を実行します。

1. **テンプレート** に移動する。
1. **新規** を選択して、ページのテンプレートを作成します。
1. **テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、新規テンプレートの名称を入力し、**OK** を選択します。
1. ステータス コード エラーの応答ページに含める構造に基づいて、テンプレートを構築します。
1. **保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。 

### <a name="build-the-status-code-error-response-page"></a>ステータス コード エラーの応答ページの構築

ステータス コード エラーの応答ページを構築するには、次の手順を実行します。

1. **ページ** に移動します。
1. **新規** を選択して、ページを作成します。
1. **テンプレートの選択** ダイアログボックスでテンプレートを選択し、**ページ名** に、[ステータスコードのエラー応答] ページの名前を入力します。 **ページの URL** フィールドは空白のままにします。
1. ページを構築します。
1. **保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。

> [!NOTE]
> 4xx および 5xx ステータス コード エラー用に個別のステータス コード エラーの応答ページを作成できます。 または、両方のエラー カテゴリに同じ一般的なステータス コード エラーの応答ページを使用できます。

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a>ステータス コード エラーの応答ページのリダイレクトを設定する

ステータス コード エラーの応答ページのリダイレクトを設定するには、次の手順を実行します。

1. **URL \> 新規 \> 新しいエイリアス** に移動して、構築したステータス コード エラーの応答ページを選択します。
1. **エイリアス** フィールドに、リダイレクトを設定するステータス コード エラーの応答ページに応じて、**default-4xx** または **default-5xx** のいずれかを入力します。 これらのエイリアスは公開する必要があります。 そうしない場合、リダイレクトは機能しません。
1. **OK** を選択してリンクをコミットします。

> [!NOTE]
> 両方のエラー カテゴリに対して単一のステータス コード エラー の応答ページを使用している場合は、この手順を繰り返して、もう一方のエラー カテゴリのエイリアスを同じページにリンクします。

## <a name="additional-resources"></a>追加リソース

[テンプレートの使用](work-with-templates.md)

[新しいサイト ページの追加](add-new-page.md)

[ページ URL の作成](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]