---
title: 注文検索モジュール
description: このトピックでは、注文検索モジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: fa61a20ffd9a31f800c48b71832be7547952119f
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472637"
---
# <a name="order-lookup-module"></a>注文検索モジュール

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

このトピックでは、注文検索モジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。

注文検索モジュールは、顧客が e コマース サイトで行った注文を検索するのに使用できるフォームを提供します。 これは、[ゲスト チェックアウトの注文の検索を有効にする](order-lookup-guest.md)の一部として使用されます。 注文検索モジュールは、e コマース サイト、小売販売時点管理 (POS)、またはコール センターから送信された注文を検索するために使用できます。 このフォームは、ゲスト ユーザーと登録ユーザーのどちらから送信された注文も取得できます。

次の図は、注文検索モジュールによって表示されるフォームの例を示しています。 顧客がフォームに入力して **注文の検索** を選択すると、注文詳細ページへリダイレクトされます。

![ページ上の注文検索モジュールのフォーム。](./media/OrderLookup_module.PNG)

## <a name="order-lookup-module-properties&quot;></a>注文検索モジュールのプロパティ

| プロパティ名     | 先頭値     | 説明 |
|-------------------|-----------|-------------|
| ヘッダー           | テキスト      | フォームの上部に表示されるヘッダー (たとえば、&quot;注文の検索")。 |
| リッチ テキスト         | リッチ テキスト | ヘッダーの下部にオプションで表示される説明。 |
| 注文のステータス タイプ | Enum      | <p>注文確認 ID に加えて、フォームから顧客に要求される情報のタイプを選択します。 次の値が現在サポートされています:</p><ul><li><b>電子メール</b> – このフォームには、顧客が注文を行った際に使用した電子メール アドレスを入力できるフィールドが含まれます。</li><li><b>なし</b> – このフォームでは、注文確認 ID 以外の情報は要求されません。</li></ul> |

## <a name="add-an-order-lookup-module-to-a-page"></a>注文検索モジュールをページに追加する

注文検索モジュールは、e コマース サイトのどのページの本文にも追加できます。 注文検索モジュールを使用してゲスト チェックアウトの注文の検索を有効にしたい場合、必ずユーザーのサインインが必要ないページに追加してください。 Commerce サイト ビルダー ツリー ビューでページの **サインインが必要?** の設定を見つけるには、**既定のページ (必須)** スロットを選択し、右ウィンドウの下部を確認します。

## <a name="additional-resources"></a>追加リソース

[ゲスト チェックアウトの注文の検索を有効にする](order-lookup-guest.md)

[モジュール ライブラリの概要](starter-kit-overview.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]