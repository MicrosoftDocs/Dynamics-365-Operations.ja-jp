---
title: POS で URL を開く
description: この記事には、Dynamics 365 Commerce の製品および顧客検索機能に加えられた改良の概要が含まれます。
author: ShalabhjainMSFT
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.custom: 141393
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: ad82cf1039515e58d1717453ee3fb4e3dafd84fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276430"
---
# <a name="open-url-in-pos"></a>POS で URL を開く

[!include [banner](includes/banner.md)]

この記事では、Dynamics 365 Commerce 販売時点管理 (POS) のボタンをコンフィギュレーションして URL を開く方法について説明します。 この機能はコードのカスタマイズを必要とせず、開発者以外のロールのユーザーがコンフィギュレーションすることもできます。 

この機能では、ボタン グリッド デザイナーを使用して URL を開くことで、POS のボタンをコンフィギュレーションすることができます。 現時点では、これは次のコンフィギュレーションでサポートされています:

- 新しいウィンドウで開きます。
- POS 内で開きます。
- ネイティブ アプリを開きます。

## <a name="open-in-new-window"></a>新しいウィンドウで開く

このコンフィギュレーションは、URL を新しいウィンドウで開くか、アプリ内で開くかどうかを定義します。 アプリ内で Web URL を開くようにコンフィギュレーションされている場合は、サイド ナビゲーション ウィンドウおよび POS 上部のバーが表示され、ユーザー操作が可能になります。 新しいウィンドウで開くようにコンフィギュレーションされている場合は、URL は Windows 用の Modern POS の新しいアプリ ウィンドウ、およびその他のすべての POS クライアントの新しいブラウザー タブで開きます。 これを有効にするには、**新しいウィンドウで開く** オプションを選択して URL をコンフィギュレーションする必要があります。

## <a name="open-within-pos"></a>POS 内で開く

POS 内で Web URL を開くことは、現在 Windows 用 Modern POS に対してのみサポートされています。 他のクライアントでは、この機能は現在開発中で、将来の更新でリリースされる予定です。 これを有効にするには、**新しいウィンドウで開く** オプションを選択せずに URL をコンフィギュレーションする必要があります。

## <a name="open-a-native-app"></a>ネイティブ アプリを開く

この機能では、ネイティブ アプリを開くための Web 以外の URL を指定することもできます。 たとえば、MailTo、SIP、IM、または MSTEAMS などの、ホスト デバイス上のそれぞれのネイティブ アプリで処理できる URL プロトコルを指定できます。 これを有効にするには、**新しいウィンドウで開く** オプションを選択して URL をコンフィギュレーションする必要があります。

- Windows のコンピューターで、Deployment Image Servicing and Management (DISM) を使用してコンピューターを設定している場合は、[既定のアプリケーション アソシエーションをエクスポートまたはインポートする](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) を参照して、既定のプロトコル アソシエーションを設定できます。
- Intune のような MDM を使用して Windows コンピューターを管理している場合は、[ポリシー CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults) を参照してください。
- カスタム Web サイトを構築する開発者の場合は、[URI の規定のアプリを起動する](/windows/uwp/launch-resume/launch-default-app) を参照してください。

## <a name="open-a-native-app-seamlessly"></a>ネイティブ アプリをシームレスに開く

Windows、iOS、および Android では、アプリ プロトコル アソシエーションに基づいてアプリをよりシームレスに開くことが可能になります。 アプリがまだ Web ブラウザから開くことを処理するようにコンフィギュレーションされていない場合、これをコンフィギュレーションするには開発者が必要な場合があります。

- Windows の場合は、[アプリ URI ハンドラーを使用して Web サイトのアプリを有効にする](/windows/uwp/launch-resume/web-to-app-linking) を参照してください。
- iOS の場合は、[開発者向けの汎用リンク](https://developer.apple.com/ios/universal-links/) を参照してください。
- Android の場合は、[Android アプリの操作リンク](https://developer.android.com/training/app-links/)を参照してください。

| クライアント                | 新しいウィンドウで開く | ネイティブ アプリを開く | POS 内で開く | 詳細情報                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| Windows 上の Modern POS | ✓\*                | ✓               | ✓              | \*新しい Modern POS ウィンドウで開く |
| クラウド POS             | ✓\*                | ✓               | x              | \*新しいブラウザー タブで開く        |
| iOS 上の Modern POS     | ✓\*                | ✓               | x              | \*新しいブラウザー タブで開く        |
| Android 上の Modern POS | ✓\*                | ✓               | x              | \*新しいブラウザー タブで開く        |

## <a name="before-you-begin"></a>準備

開始する前に、[販売時点管理 (POS) の画面レイアウト](pos-screen-layouts.md) をコンフィギュレーションする方法を確認します。

## <a name="open-url-in-pos"></a>POS で URL を開く

POS で開くように URL をコンフィギュレーションするには、次の手順を実行します。

1. 本社で、**Retail および Commerce \>チャネル設定 \> POS 設定 \> POS \> 画面レイアウト** に移動します。
2. **ボタン グリッド \> デザイナー** を選択します。
3. 新しいボタンを作成します。
4. **ボタン** プロパティを選択します。
5. アクションとして **URL を開く** を選択します。
6. 使用する URL を入力します。
7. 新しいウィンドウで URL を開くかどうかをコンフィギュレーションします。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
