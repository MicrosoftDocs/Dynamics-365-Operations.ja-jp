---
title: Microsoft Power Automate の ビジネス イベント
description: このトピックでは、アプリケーション コネクタを介して Microsoft Power Automate で使用可能となるビジネス イベントに関する情報を提供します。
author: Sunil-Garg
manager: AnnBe
ms.date: 07/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: sunilg
ms.search.validFrom: Platform update 24
ms.dyn365.ops.version: 2019-02-28
ms.openlocfilehash: 29928d4ab04ae64d4d075f15d2eb9f09adbfd2ff
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769774"
---
# <a name="business-events-in-microsoft-power-automate"></a>Microsoft Power Automate の ビジネス イベント

[!include[banner](../includes/banner.md)]

ビジネス イベントは アプリケーション コネクタを介して Microsoft Power Automate で使用することができます。 コネクタには**ビジネス イベントの発生時**という名前のトリガーがあります。 このトリガーは、アプリケーションのターゲット インスタンスで使用可能なビジネス イベントの購読に使用することができます。

## <a name="prerequisite"></a>前提条件

ビジネス イベントについて理解することは重要です。 詳細については[ビジネス イベント](home-page.md) のドキュメントを参照してください。

> [!IMPORTANT]
> ビジネス イベントは以前のプラットフォーム リリースでは使用可能でないため、**ビジネス イベント発生時**トリガーは、Platform update 24 またはそれ以降を実行するアプリケーション インスタンスでのみ動作します。

## <a name="subscribing-to-business-events-and-unsubscribing-from-them"></a>ビジネス イベントの購読および購読解除

**ビジネス イベント発生時** トリガーをフローに追加した後、以下の情報を提供する必要があります。

- **インスタンス** – ビジネス イベントが発生するインスタンスのホスト名を指定します。 環境インスタンスは指定されたドロップダウン メニューで利用可能である必要がありますが、環境が一覧表示されていない場合はカスタム値として入力することができます。
- **カテゴリ** - ビジネス イベントのカテゴリを選択します。 **ビジネス イベント** フィールドにそのカテゴリのビジネス イベントが表示されます。
- **ビジネス イベント** - 選択したカテゴリで利用可能なビジネス イベント。
- **法人** - ビジネス イベントが購読されている法人を指定します。 フローは法人でビジネス イベントが発生するときにトリガーされます。 既定では、このフィールドは空白で、ビジネス イベントは **すべて** の法人で購読されます。

フローが保存されると、選択したビジネス イベントに対するサブスクリプションが環境インスタンスに追加されます。 サブスクリプション プロセスの一部として、必要なエンドポイントが設定され、対応するビジネス イベントが有効にされます。

トリガーまたはフローのいずれかを削除または無効化すると、ビジネス イベントは自動的に購読解除されます。

複数のフローは、同一もしくは異なる法人内の同じビジネス イベントを購読することができます。

> [!NOTE]
> Power Automate エンドポイントは、手動で構成することはできません。 上記の説明に従って、エンドポイントは Power Automate で自動的に作成されます。

Microsoft Flow でビジネス イベントを使用する方法については [Microsoft Flow でビジネス イベントを消費する](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/how-to/how-to-flow) を参照してください。 

## <a name="other-ways-to-consume-business-events-in-power-automate"></a>Power Automate 内のビジネス イベントを消費する他の方法

前のセクションでは、コネクタ内でトリガーを使用することにより Power Automate から直接ビジネス イベントを購読する方法について説明しました。 ただし、 [Microsoft Power Automateのイベント グリッド コネクタ](https://docs.microsoft.com/connectors/azureeventgrid/) を使用して、 Microsoft Azure のイベント グリッド から Microsoft Power Automate のビジネス イベントを使用することもできます。

実装内の他の統合で既に使用されている場合、イベント グリッドは Power Automate 内のビジネス イベントを消費するための実行可能なアプローチである可能性があります。 同じ法人内のビジネス イベントが複数のフローをトリガする必要がある場合、イベント グリッドからビジネス イベントを消費することを検討する必要があります。

このアプローチは、コネクタが Power Automate 内のビジネス イベントで使用可能である場合、ビジネス イベントのエンドポイントとして使用されるメッセージングまたはイベント プラットフォームに対して適用することができます。
