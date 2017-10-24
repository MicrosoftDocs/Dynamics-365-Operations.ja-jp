---
title: "Finance and Operations クライアントのよく寄せられる質問"
description: "この記事は、Microsoft Dynamics 365 for Finance and Operations クライアントについてよく寄せられる質問に対する回答を提供します。"
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 55d4fa4629d203aa888fe6400126a872d2eee000
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="finance-and-operations-client-faq"></a>Finance and Operations クライアントのよく寄せられる質問

[!include[banner](../includes/banner.md)]


この記事は、Microsoft Dynamics 365 for Finance and Operations クライアントについてよく寄せられる質問に対する回答を提供します。

<a name="why-arent-symbols-loaded-when-i-use-finance-and-operations"></a>Finance and Operations の使用時に、なぜ記号が読み込まれないのですか。
-----------------------------------------------------------------

ブラウザーのセキュリティ設定が、記号を正しく読み込むことを妨げている可能性があります。 この問題を解決するには、次の手順を試してください。

-   Internet Explorer でこの問題が発生する場合、[**ツール**] をクリックしてから、[**インターネット オプション**] をクリックします。  [インターネット オプション] ダイアログ ボックスの [**プライバシー**] タブで [**レベルのカスタマイズ**] をクリックし、[**フォントのダウンロード**] オプションが選択されていることを確認します。
-   それ以外の場合は、信頼済サイトのリストに Finance and Operations を追加する必要があります。

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>Dynamics AX 2012 のリボンがありません。 [アクション ウィンドウ] のタブを常時開いておくことはできますか。
近々この機能を搭載する予定です。 ユーザーはアクション ウィンドウのタブを常時開いておくかどうか選択できるようになります。 それ以外の場合は、使用していないときはタブは折りたたまれ、ページの画面スペースがより広くなります。

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-rightclick"></a>右クリックしたときに、ときどき異なるショートカット メニューが表示されるのは、なぜですか。
編集可能なフィールドで (またはテキストが選択されている場合に) 右クリックすると、ブラウザーのショートカット メニューが表示されます。 このメニューから、[**切り取り**] 、[**コピー**] 、[**貼り付け**] コマンドにアクセスできます。 Finance and Operations ショートカット メニューにこれらのコマンドを埋め込むことはできません。セキュリティ上の理由から、ブラウザーは、システムのクリップボードにプログラムからアクセスすることを許可していないためです。

読み取り専用コントロールのフィールド ラベルや値を右クリックすると、Finance and Operations ショートカット メニューが表示されます。

キーボードでのアクセスを容易にするために、Finance and Operations ショートカット メニューを開く機能にキーボード ショートカットを実装する予定です。

## <a name="where-is-the-view-details-functionality-in-finance-and-operations"></a>Finance and Operations に、詳細の表示機能はありますか。
[**詳細の表示**] オプションが、いくつかの方法で使用できます。

-   コントロールに [**詳細の表示**] 機能がある場合、およびコントロールに値がある場合、その値はハイパーリンクとして表示されます。 ハイパーリンクをクリックすると、詳細を含むページを開くことができます。
-   また、[**詳細の表示**] は、Finance and Operations ショートカット メニューのオプションです。 右クリックしたときに、いつ Finance and Operations ショートカット メニューが表示されるかについては、前のセクションを参照してください。





