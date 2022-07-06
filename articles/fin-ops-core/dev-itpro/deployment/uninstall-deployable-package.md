---
title: パッケージのアンインストール
description: この記事では、配置可能パッケージを環境から削除する方法について説明します。
author: laneswenka
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: 24211
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3828c6b24c153f97a5108ee2035d3f80b1d8731
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867293"
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
- Microsoft モジュールは削除できません。  試行する場合、検証エラーが Lifecycle Services のパッケージに表示されます。
- AOT の展開可能なパッケージの一部がインストールされている場合、モジュールは削除できません。  モジュールを削除したい場合、ModuleToRemove.txt ファイルにファイル名を追加する前に、パッケージの一部ではないかどうかを確認してください。

## <a name="uninstall-a-package"></a>パッケージのアンインストール

1. **ModuleToRemove.txt** という名前のファイルを作成します。
2. ファイルには、別の行で削除する各モジュールの名前を入力します。 削除する各モジュールの前提条件が完了したことを確認します。
3. 有効な配置可能なパッケージを作成して、**package\\AOSService\\Scripts** フォルダに ModuleToRemove.txt ファイルを保存します。
4. パッケージを Lifecycle Services アセット ライブラリにアップロードします。 アセットが検証を終了するのを待ち、ページの右側にあるアセットの詳細パネルに表示される任意の警告を確認します。
5. 配置可能パッケージをインストールします。 配置可能パッケージをインストールする方法の詳細については、[クラウド配置に更新プログラムを適用する](apply-deployable-package-system.md)を参照してください。
6. 運用環境で、この手順を実行する前に、パッケージがアンインストールされたことを確認します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]