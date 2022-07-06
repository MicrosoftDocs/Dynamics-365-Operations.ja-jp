---
title: レポート メニューの項目を拡張してユーザーナビゲーションをリダイレクトします。
description: この記事では、ナビゲーションをカスタム レポート ソリューションにリダイレクトするように、既存のアプリケーション メニュー項目を拡張する方法について説明します。
author: RichdiMSFT
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.custom: 266674
ms.assetid: 7bf76862-e320-4a81-81a4-5bda7288e573
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: 0d97027b80901df0d44baa2ae54a498546ddf978
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858697"
---
# <a name="extend-report-menu-items-to-redirect-user-navigation"></a>レポート メニューの項目を拡張してユーザーナビゲーションをリダイレクトします。

[!include [banner](../includes/banner.md)]

この記事では、コード変更を最小限にして、ナビゲーションをカスタム レポート ソリューションにリダイレクトするように、既存のアプリケーション メニュー項目を拡張する方法について説明します。

この記事では、コード変更を最小限にして、ナビゲーションをカスタム レポート ソリューションにリダイレクトするように、既存のアプリケーション メニュー項目を拡張するプロセスについて説明します。 この手法を使用すると、すべての参照を追跡し既存の申請レポートに置き換えることの不便を避けることができます。 アプリケーション ナビゲーションを拡張モデルで定義されているレポートにリダイレクトするには、既存のアプリケーションのメニュー項目を拡張します。 次の図は、一般的なアプリケーションのカスタマイズを示しています。

[![extendingmenuitem。](./media/extendingmenuitem.png)](./media/extendingmenuitem.png)

## <a name="whats-important-to-know"></a>知っている必要がある重要なこと
このソリューションを適用する前に知っておくべき基本的な前提がいくつかあります。

- 拡張メニュー項目を使用して、表示文字列およびターゲットの両方を上書きすることができます。
- この方法は、単純なクエリに基づくレポートから複雑なレポート データ プロバイダー (RDP) に基づくレポートまで、すべてのタイプのレポートに使用できます。
- 拡張メニュー項目は、コントローラ クラスを使用してレポート セッションを編成するレポートおよびソリューションへ直接参照に使用できます。

## <a name="extend-report-menu-items"></a>レポート メニュー項目の拡張
次のチュートリアルでは、メニュー項目の拡張機能を使用して、アプリケーション内のユーザー ナビゲーションをカスタム ソリューションにリダイレクトする方法を示します。 このソリューションには、Fleet Management アプリケーション用のカスタム **顧客リスト** レポートが含まれており、純粋な拡張モデルですべてのアプリケーションのカスタマイズが定義されています。 次の図は、カスタムの **顧客リスト** レポートにアクセスするために使用するメニュー項目を示しています。

[![fleet-workspace-customer-list。](./media/fleet-workspace-customer-list.png)](./media/fleet-workspace-customer-list.png)

1. **アプリケーション カスタマイズの新しいモデルを作成します。** 拡張モデルに関する詳細については、 [拡張機能およびオーバーレイによるカスタマイズ](../extensibility/customization-overlayering-extensions.md) を参照してください。
2. **Microsoft Visual Studioで新しいプロジェクトを作成し、** **カスタム レポートを追加します。** また、すべてのソリューション コンポーネントを追加します。 これらのコンポーネントには、RDP クラスまたはソース クエリ、コントローラー クラス、UI ビルダー (ある場合) が含まれます。
3. **レポートにアクセスするために使用するメニュー項目の拡張機能を作成します。** この例では、出力メニュー項目は **FMCustomerListReport** と名前が付けられています。 メニュー項目の構造を使用して、アプリケーションで公開されているメニュー項目の名前を見つけます。 次の図は、アプリケーション エクスプローラーでのアクションを示しています。

    [![レポートにアクセスするために使用するメニュー項目の拡張機能の作成。](./media/fleet-extension-create-menu-extension-1024x632.png)](./media/fleet-extension-create-menu-extension.png)

4. **メニュー項目の拡張機能のプロパティの変更。** メニュー項目のレポート デザインまたはコントローラ＝の参照を更新して、カスタム ソリューションに直接ナビゲートします。

    > [!NOTE]
    > オブジェクトに対して実行できるプロパティの変更は、元のアプリケーション ソリューションによって異なります。 アプリケーションのレポートは、コントローラーを使用してソリューションを管理する場合、コントローラー クラスがレポートに必要になります。

5. **ソリューションを再構築してカスタム レポートを配置します。**

これで、レポート メニュー項目の拡張を完了しました。 標準のメニュー項目へのナビゲーションは、カスタム レポート ソリューションにリダイレクトされるようになります。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]