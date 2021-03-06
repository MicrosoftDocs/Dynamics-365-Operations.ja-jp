---
title: Microsoft Power Automate 内のビジネス イベント
description: このトピックでは、アプリケーション コネクタを介して Microsoft Power Automate で使用可能となるビジネス イベントに関する情報を提供します。
author: Sunil-Garg
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: sunilg
ms.search.validFrom: Platform update 24
ms.dyn365.ops.version: 2019-02-28
ms.openlocfilehash: c725d4272741b7af38a1e7f9a2645dfc40391133
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941017"
---
# <a name="business-events-in-microsoft-power-automate"></a>Microsoft Power Automate 内のビジネス イベント

[!include[banner](../includes/banner.md)]

ビジネス イベントは アプリケーション コネクタを介して Microsoft Power Automate で使用することができます。 コネクタには **ビジネス イベントの発生時** という名前のトリガーがあります。 このトリガーは、アプリケーションのターゲット インスタンスで使用可能なビジネス イベントの購読に使用することができます。

## <a name="prerequisite"></a>前提条件

ビジネス イベントについて理解することは重要です。 詳細については[ビジネス イベント](home-page.md) のドキュメントを参照してください。

> [!IMPORTANT]
> ビジネス イベントは以前のプラットフォーム リリースでは使用可能でないため、**ビジネス イベント発生時** トリガーは、Platform update 24 またはそれ以降を実行するアプリケーション インスタンスでのみ動作します。

## <a name="subscribing-to-business-events-and-unsubscribing-from-them"></a>ビジネス イベントの購読および購読解除

**ビジネス イベント発生時** トリガーをフローに追加した後、以下の情報を提供する必要があります。

- **インスタンス** – ビジネス イベントが発生するインスタンスのホスト名を指定します。 環境インスタンスは指定されたドロップダウン メニューで利用可能である必要がありますが、環境が一覧表示されていない場合はカスタム値として入力することができます。
- **カテゴリ** - ビジネス イベントのカテゴリを選択します。 **ビジネス イベント** フィールドにそのカテゴリのビジネス イベントが表示されます。
- **ビジネス イベント** - 選択したカテゴリで利用可能なビジネス イベント。
- **法人** - ビジネス イベントが購読されている法人を指定します。 フローは法人でビジネス イベントが発生するときにトリガーされます。 既定では、このフィールドは空白で、ビジネス イベントは **すべて** の法人で購読されます。

フローが保存されると、選択したビジネス イベントに対するサブスクリプションが環境インスタンスに追加されます。 サブスクリプション プロセスの一部として、必要なエンドポイントが設定され、対応するビジネス イベントが有効にされます。

トリガーが削除されるか、フローがオフになっている場合は、ビジネス イベントのエンドポイントが自動的に削除されます。

複数のフローは、同一もしくは異なる法人内の同じビジネス イベントを購読することができます。 1 つのイベントごとの既定のエンドポイント制限は、10 であることに注意してください。 必要に応じて、**ビジネス イベント パラメーター** ページの **イベントごとに許可されるエンドポイント** を調整します。

> [!NOTE]
> Power Automate エンドポイントは、手動で構成することはできません。 上記の説明に従って、エンドポイントは Power Automate で自動的に作成されます。

Microsoft Flow でビジネス イベントを使用する方法については [Microsoft Flow でビジネス イベントを消費する](how-to/how-to-flow.md) を参照してください。 

## <a name="other-ways-to-consume-business-events-in-power-automate"></a>Power Automate 内のビジネス イベントを消費する他の方法

前のセクションでは、コネクタ内でトリガーを使用することにより Power Automate から直接ビジネス イベントを購読する方法について説明しました。 ただし、[Microsoft Power Automate 用イベント グリッド コネクタ](/connectors/azureeventgrid/) を使用することにより、Microsoft Azure Event Grid から Microsoft Power Automate 内のビジネス イベントを消費することもできます。

実装内の他の統合で既に使用されている場合、イベント グリッドは Power Automate 内のビジネス イベントを消費するための実行可能なアプローチである可能性があります。 同じ法人内のビジネス イベントが複数のフローをトリガする必要がある場合、イベント グリッドからビジネス イベントを消費することを検討する必要があります。

このアプローチは、コネクタが Power Automate 内のビジネス イベントで使用可能である場合、ビジネス イベントのエンドポイントとして使用されるメッセージングまたはイベント プラットフォームに対して適用することができます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
