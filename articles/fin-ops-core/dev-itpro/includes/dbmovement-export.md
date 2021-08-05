---
ms.openlocfilehash: 170fb152d002903f68b658112de38edefdc2241b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356243"
---
サンドボックス **環境詳細** ページで、 **管理** メニューをクリックし、 **データベースの移動** を選択します。

![データベース メニューを移動します。](../database/media/DBMovement_Menu.png)

**エクスポート データベース** アクションが使用できるページでスライダー ウィンドウが開きます。

![データベース メニューをエクスポートします。](../database/media/Export_Menu.png)

サンドボックスの更新やパッケージの展開などの他のサービス操作は、この間実行できません。 ソース環境は Dynamics ユーザーの観点から使用可能になります。  

エクスポートが正常に完了した後に、**環境の詳細** ページのサービス操作からサインアウトします。 **データベースのバックアップ** セクションの **資産ライブラリ** で資産を確認できます。

![資産ライブラリのバックアップ ファイル。](../database/media/AssetLibrary_Backups.png)

**.bacpac** ファイルはここに格納され、インポート用 Tier 1 開発者環境に手動でダウンロードすることができます。 今後、Microsoft は、エクスポート アクションをトリガーし、資産ライブラリで使用可能なバックアップ ファイルを一覧表示するための API を提供します。 これには、バックアップ資産ファイルを自動でダウンロードするための、または Microsoft Azure Storage SDK を使用して、セキュリティで保護された BLOB ストレージに直接コピーするための、セキュリティで保護された URL が含まれます。
