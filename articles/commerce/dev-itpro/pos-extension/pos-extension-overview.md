---
title: POS 拡張機能の概要
description: このトピックでは、新しい独立した POS 拡張モデルおよびシールド SDK を使用して POS 拡張機能を作成する方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 26857a258f313cd5197292328b69ca075d699014
ms.sourcegitcommit: fd15b02fc9caa1c05e56abdc276a7f4b23b0d8f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/29/2021
ms.locfileid: "5960152"
---
# <a name="point-of-sale-pos-extension-overview"></a>販売時点管理 (POS) 拡張機能の概要

[!include [banner](../../../includes/banner.md)]

Retail SDK の POS 拡張機能を使用して、POS アプリケーションを個別に拡張することができます。 POS のユーザー エクスペリエンスの変更と作成、標準の機能拡張または変更の実行、検証の追加、カスタム機能の追加を行うことができます。 拡張機能を使用すると、次のことが可能です。

+ POS UI の拡張: ビューに応じて、カスタム列、アプリ バー ボタン、およびカスタム コントロールを追加します。 画面レイアウト デザイナーを使用した、カート ビューとようこそ画面サポートの構成。 他のビューは、カスタム コードを記述して拡張できます。
+ POS ビジネス ロジックのオーバーライド: POS ビジネス ロジックを拡張し、POS 要求ハンドラーをオーバーライドしてカスタム ロジックを追加します。
+ プレトリガーとポストトリガー: POS 操作の前または後にカスタム ロジックを追加します。
+ APIの使用: POS によって、拡張機能のシナリオで使用できる API と UX のコントロールが公開されます。
+ カスタム UX と API: POS を拡張してカスタム ビューおよび API を追加し、新しい機能と特徴をサポートします。
+ カスタム操作: カスタム操作を追加してカスタム機能を実行します。

これらのトピックでは、独立した POS 拡張モデルおよびシールド SDK を使用して POS 拡張機能を作成する方法について説明します。 このトピックは、Retail ソフトウェア開発キット (SDK) バージョン 10.0.18 以降に適用されます。

+ [POS 拡張機能を開始する](pos-extension-getting-started.md)
+ [POS 拡張機能パッケージ プロジェクトの作成](create-pos-extension-package.md)
+ [Modern POS 拡張 appx ファイルの作成](create-pos-extension-appx.md)
+ [POS 拡張機能のデバッグ](debug-pos-extension.md)

## <a name="supported-apps"></a>対応アプリ

コード ベースは異なる POS アプリケーションでも同じですが、拡張機能のパッケージ化、配置方法、および表示方法は、プラットフォームとアプリ タイプによって異なります。 作成したカスタマイズは、異なるアプリのコードの複製または書き直しを行わずに、異なるアプリ タイプで使用できす。 アプリ固有の拡張機能コンポーネントが存在する場合がありますが、拡張機能コードの大部分はアプリ全体で使用できます。

次の表にあるアプリの POS 拡張機能を作成できます。

 アプリ | 説明
---|---
販売時点管理 (POS) | POS では、レジ担当者、販売在庫担当者、在庫担当者、店長など、第一線の作業者がさまざまなコマース操作を実行できます。 Dynamics 365 Commerce ソリューションは、これらの操作をプラットフォームおよびフォーム ファクター間で実行するためのさまざまなデバイス タイプを提供します。
Modern 販売時点管理 (MPOS) | MPOS は、Windows デバイスで実行されるユニバーサル Windows プラットフォーム (UTC) アプリです。 MPOS クライアントは、Hardware Station を使用して、キャッシュ ドロワー、クレジット カード リーダー、プリンターなどの周辺機器とも通信できます。
クラウド販売時点管理 (CPOS) | CPOS は、ブラウザで実行される POS のホストされたバージョンです。 CPOS アプリは、クラウドに配置されます。
Store Commerce | Microsoft Dynamics 365 Commerce の Store Commerce アプリは、Windows デバイスで実行される Microsoft Store からの Windows アプリです。 Store Commerce アプリでは、アプリを表示するのに Chromium エンジンを使用します。 Chromium エンジンは、Windows の ネイティブの JavaScript UWP アプリよりも表示パフォーマンスが優れています。 Store Commerce が MPOS と完全に同等の機能を持つようになった場合、Store Commerce は MPOS に置き換えられます。 現時点では、Store Commerce はオフラインでの実行をサポートしません (Retail Server への接続がない場合)。
iOS ハイブリッド アプリ | iOS ハイブリッド アプリは iOS デバイスで実行されるシェル アプリ (ラッパー) です。 シェルで CPOS をホストします。
Android ハイブリッド アプリ | Android ハイブリッド アプリは Android デバイスで実行されるシェル アプリです。 シェルで CPOS をホストします。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
