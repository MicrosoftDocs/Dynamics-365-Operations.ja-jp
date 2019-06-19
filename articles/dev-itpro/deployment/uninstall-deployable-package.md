---
title: パッケージのアンインストール
description: このトピックでは、配置可能パッケージを環境から削除する方法について説明します。
author: manado
manager: AnnBe
ms.date: 07/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 24211
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 17207b63a579df40be604f62029139c86e4448bc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550934"
---
# <a name="uninstall-a-package"></a>パッケージのアンインストール

[!include [banner](../includes/banner.md)]

場合によっては、配置可能パッケージをアンインストールする必要があります。 たとえば、ソース コードを再編成することができます。 また、独立系ソフトウェア ベンダー (ISV) 製品はすでに必要がなく、ライセンスを更新していません。 したがって、パッケージを削除する必要があります。

## <a name="remove-a-model"></a>モデルの削除

モデルは、パッケージの一部であるデザイン時の概念です。 モジュール内の唯一のモデルでないモデルは、ソース コードからモデルを削除することができます。 更新されたモジュールを配置するときに古いモジュールが上書きされるため、その他の手順は行う必要がありません。 すべてのオーバーレイ モデルは、このカテゴリに分類されます。 詳細については、[モデルの削除](../dev-tools/models.md#deleting-a-model)を参照してください。

## <a name="prerequisites"></a>前提条件

- いずれかのモデルが削除されるモジュールを参照している場合、そのモジュールから参照を削除する必要があります。 削除する必要がある参照を検索する方法については、[モデルの依存関係の表示](../dev-tools/models.md#viewing-package-dependencies)を参照してください。
- 参照が削除されたすべてのモジュールを構築し展開します。
- モジュールをアンインストールする前に、モジュールへの参照およびモジュールからの参照を削除する必要があります。 モジュールのすべての参照を削除するには、モデルに 1 つのクラスを追加します。 このクラスにコードを含むことはできません。 これにはアプリケーション プラットフォームへの参照のみが含まれます。

## <a name="uninstall-a-package"></a>パッケージのアンインストール

1. **ModuleToRemove.txt** という名前のファイルを作成します。
2. ファイルには、別の行で削除する各モジュールの名前を入力します。 削除する各モジュールの前提条件が完了したことを確認します。
3. 有効な配置可能なパッケージを作成して、**package\\AOSService\\Scripts** フォルダに ModuleToRemove.txt ファイルを保存します。
4. 配置可能パッケージをインストールします。 配置可能パッケージをインストールする方法の詳細については、[クラウド配置に更新プログラムを適用する](apply-deployable-package-system.md)を参照してください。
5. 実稼動環境で、この手順を実行する前に、パッケージがアンインストールされたことを確認します。
