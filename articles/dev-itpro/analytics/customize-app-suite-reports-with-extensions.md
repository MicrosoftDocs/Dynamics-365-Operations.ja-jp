---
title: 拡張機能を使用してアプリ スイート レポートをカスタマイズする
description: このトピックでは、App スイート レポートをカスタマイズするための一連のシナリオについて説明します。
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 266614
ms.assetid: acf73781-08bb-4f59-9956-8f9f295ddd02
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: 8dbe341e992b0ea210077ca08f4806ec8226defd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368456"
---
# <a name="customize-app-suite-reports-by-using-extensions"></a>拡張機能を使用してアプリ スイート レポートをカスタマイズする

[!include [banner](../includes/banner.md)]

このトピックでは、App スイート レポートをカスタマイズするための一連のシナリオについて説明します。

Microsoft Dynamics 365 for Finance and Operations は、カスタム ソリューションをサポートするためのツールの拡張セットを提供します。 標準アプリケーションのレポート ソリューションのカスタマイズは、純粋な拡張モデルを使用して完全にサポートをされています。 このトピックには、アプリケーション スイート コンポーネントをオーバーレイすることなく、標準のアプリケーション レポートに最も一般的なカスタマイズを追加する方法についてのガイダンスが含まれています。 アプリケーションをカスタマイズするときの、拡張ベースのアプローチを使用する主な利点を次に示します。

- コードの重複を最小化して、アプリケーション ソリューションのフットプリントを低減します。
- カスタムレポートには、レポート データ プロバイダー (RDP)、データ コントラクト、および UI ビルダー クラスのビジネス ロジックの更新などの標準ソリューションの拡張機能があります。
- 標準アプリケーション ソリューションは影響を受けず、カスタム レポートと同時に引き続き使用できます。

レポート拡張機能は、標準アプリケーション レポートを中断またはアクセス禁止しません。 代わりに、プラットフォームは、ユーザー セッションのコンテキストに基づいて適切なレポート デザインを選択できるターゲット レポートの実行時の選択をサポートします。 拡張機能を使用するカスタマイズに関する詳細については、[カスタマイズ: オーバーレイおよび拡張機能](../extensibility/customization-overlayering-extensions.md) を参照してください。

## <a name="scenarios"></a>シナリオ
使用可能な柔軟性を実証する 4 つの重要なシナリオがあります。 最初の 2 つのシナリオには、カスタム レポート ソリューションのために既存の RDP クラスの拡張が含まれます。

- [既存のデータセットを展開する](expand-app-suite-report-data-sets.md) – テーブル拡張機能を使用し、カスタム ビジネス ロジックを統合して既存のデータセットにカスタム列を追加します。
- カスタム データセットの作成 – 既存の RDP クラスを拡張してカスタム データセットを返すことによって、アプリケーション レポートにデータを追加します。

その他の 2 つのシナリオでは拡張機能を使用して、カスタム ソリューションにアプリケーション ナビゲーションをリダイレクトする方法に関する情報を提供できます。

- [レポート メニュー項目を拡張する](extend-report-menu-items.md)– アプリケーションのメニュー項目をカスタマイズして、カスタム レポート デザインへの参照をリダイレクトします。
- [ビジネス ドキュメント用のカスタム デザイン](custom-designs-business-docs.md) – デリゲート ハンドラーを使用すると、既存の印刷管理ドキュメント インスタンスに対してカスタム レポート デザインを追加できます。
