---
title: クライアント FAQ
description: この記事じゃ、Finance and Operations クライアントについてよく寄せられる質問に対する回答を提供します。
author: jasongre
manager: AnnBe
ms.date: 09/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1925c23891a637ba9e9666538323274819692a06
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692921"
---
# <a name="client-faq"></a>クライアント FAQ

[!include [banner](../includes/banner.md)]

この記事じゃ、Finance and Operations クライアントについてよく寄せられる質問に対する回答を提供します。

## <a name="why-arent-symbols-loaded"></a>なぜ記号が読み込まれないのですか。

ブラウザーのセキュリティ設定が、記号を正しく読み込むことを妨げている可能性があります。 この問題を解決するには、次の手順を試してください。

- Internet Explorer でこの問題が発生する場合、**ツール** をクリックしてから、**インターネット オプション** をクリックします。 [インターネット オプション] ダイアログ ボックスの **プライバシー** タブで **レベルのカスタマイズ** をクリックし、**フォントのダウンロード** オプションが選択されていることを確認します。
- それ以外の場合は、信頼済サイトのリストにアプリ サイトを追加する必要があります。

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>Dynamics AX 2012 のリボンがありません。 [アクション ウィンドウ] のタブを常時開いておくことはできますか。

近々この機能を搭載する予定です。 ユーザーはアクション ウィンドウのタブを常時開いておくかどうか選択できるようになります。 それ以外の場合は、使用していないときはタブは折りたたまれ、ページの画面スペースがより広くなります。

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a>右クリックしたときに、ときどき異なるショートカットメニューが表示されるのはなぜですか。

編集可能なフィールドで (またはテキストが選択されている場合に) 右クリックすると、ブラウザーのショートカット メニューが表示されます。 このメニューから、**切り取り**、**コピー**、**貼り付け** コマンドにアクセスできます。 ショートカット メニューにこれらのコマンドを埋め込むことはできません。セキュリティ上の理由から、ブラウザーは、システムのクリップボードにプログラムからアクセスすることを許可していないためです。

読み取り専用コントロールのフィールド ラベルや値を右クリックすると、ショートカット メニューが表示されます。

キーボードでのアクセスを容易にするために、ショートカット メニューを開く機能にキーボード ショートカットを実装する予定です。

## <a name="where-is-the-view-details-functionality"></a>詳細の表示機能はありますか。

**詳細の表示** オプションが、いくつかの方法で使用できます。

- コントロールに **詳細の表示** 機能がある場合、およびコントロールに値がある場合、その値はハイパーリンクとして表示されます。 ハイパーリンクをクリックすると、詳細を含むページを開くことができます。
- また、**詳細の表示** はショートカット メニューのオプションです。 右クリックしたときに、いつショートカット メニューが表示されるかについては、前のセクションを参照してください。
