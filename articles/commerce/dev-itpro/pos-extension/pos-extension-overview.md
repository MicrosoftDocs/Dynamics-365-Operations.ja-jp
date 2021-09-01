---
title: POS 拡張機能の概要
description: このトピックでは、新しい独立した POS 拡張モデルおよびシールドされたソフトウェア開発キット (SDK) を使用して販売時点管理 (POS) 拡張機能を作成する方法に関する情報を提供します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: intro-internal
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 4a4686c62a70024410e1a00505436418d7a150655b4ec5960be257471d3480b1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755870"
---
# <a name="pos-extension-overview"></a>POS 拡張機能の概要

[!include [banner](../../../includes/banner.md)]

販売時点管理 (POS) アプリは、Retail ソフトウェア開発キット (SDK) のPOS拡張機能を使用して独自に拡張できます。 POS のユーザー エクスペリエンスの変更と作成、標準の機能拡張または変更、検証の追加、カスタム機能の追加を行うことができます。

拡張機能は、次の方法で実現できます。

+ **POS ユーザー インターフェース (UI) の拡張:** ビューに応じて、カスタム列、アプリ バー ボタン、およびカスタム コントロールを追加することができます。 カート ビューとウェルカム ページは、画面レイアウト デザイナーを使用して構成することができます。 他のビューは、カスタム コードを記述して拡張できます。
+ **POS ビジネス ロジックのオーバーライド:** POS 要求ハンドラーをオーバーライドして POS ビジネス ロジックを拡張し、カスタム ロジックを追加することができます。
+ **プレトリガーとポストトリガー:** POS 操作の前または後にカスタム ロジックを追加することができます。
+ **API の使用:** POS によって、拡張機能のシナリオで使用できる API と ユーザー エクスペリエンス (UX) のコントロールが公開されます。
+ **カスタム UX と API:** POS を拡張して、新しい機能や仕様をサポートするカスタム ビューおよび API を追加することができます。
+ **カスタム操作の追加:** カスタム操作を追加してカスタム機能を実行することができます。

次のトピックでは、独立した POS 拡張モデルおよびシールド SDK を使用して POS 拡張機能を作成する方法について説明します。

+ [POS 拡張機能の使用を開始する](pos-extension-getting-started.md)
+ [POS 拡張機能パッケージ プロジェクトの作成](create-pos-extension-package.md)
+ [Modern POS 拡張パッケージの .appx ファイルの作成](create-pos-extension-appx.md)
+ [POS 拡張機能のデバッグ](debug-pos-extension.md)

このトピックは、Retail SDK 10.0.18 以降に適用されます。

## <a name="supported-apps"></a>対応アプリ

POS アプリは異なっていても、コード ベースは同じです。 ただし、プラットフォームとアプリ タイプに応じて、拡張機能のパッケージ化、配置、および表示の方法が異なります。 作成したカスタマイズは、異なるアプリのコードの複製または書き直しの要求を行わずに、アプリ タイプ全体で使用できます。 拡張機能コンポーネントがアプリ固有のものである場合がありますが、拡張機能コードの大部分はアプリ全体で使用できます。

次の表に、POS 拡張機能を作成できるアプリを示します。

|  アプリ | 説明 |
|---|---|
| 販売時点管理 (POS) | POS により、レジ担当者、販売在庫担当者、在庫担当者、店長など、第一線の作業者がさまざまなコマース操作を実行することができます。 Microsoft Dynamics 365 Commerce ソリューションは、これらの操作をプラットフォームおよびフォーム ファクター間で実行できるように、さまざまなデバイス タイプを提供します。 |
| Modern 販売時点管理 (MPOS) | MPOS は、Windows デバイスで実行されるユニバーサル Windows プラットフォーム (UTC) アプリです。 MPOS クライアントは、Hardware Station を使用して、キャッシュ ドロワー、クレジット カード リーダー、プリンターなどの周辺機器とも通信できます。 |
| クラウド販売時点管理 (CPOS) | CPOS は、ブラウザーで実行される POS のホストされたバージョンです。 CPOS アプリは、クラウドに配置されます。 |
| Store Commerce | Dynamics 365 Commerce の Store Commerce アプリは、Windows デバイスで実行される Microsoft Store からの Windows アプリです。 アプリの表示には、Curomium エンジンが使用されます。 Chromium エンジンは、Windows の ネイティブの JavaScript UWP アプリよりも表示パフォーマンスが優れています。 Store Commerce が MPOS と完全に同等の機能を持つようになった場合、MPOS は置き換えられます。 現時点では、Store Commerce はオフラインでの実行をサポートしません (Retail Server への接続がない場合)。 |
| iOS ハイブリッド アプリ | iOS ハイブリッド アプリは iOS デバイスで実行されるシェル アプリ (ラッパー) です。 シェルで CPOS をホストします。 |
| Android ハイブリッド アプリ | Android ハイブリッド アプリは Android デバイスで実行されるシェル アプリです。 シェルで CPOS をホストします。 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
